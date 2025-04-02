---
lab:
  title: Ajouter des données à un index à l’aide de l’API push
---

# Ajouter des données à un index à l’aide de l’API push

Vous souhaitez découvrir comment créer un index Recherche Azure AI et charger des documents dans cet index en utilisant du code C#.

Dans cet exercice, vous allez cloner une solution C# existante et l’exécuter pour optimiser la taille de lot en vue de charger des documents. Vous allez ensuite utiliser cette taille de lot et charger efficacement des documents à l’aide d’une approche à thread.

> **Remarque** Pour effectuer cet exercice, vous avez besoin d’un abonnement Microsoft Azure. Si vous n’en avez pas, vous pouvez vous inscrire à un essai gratuit sur [https://azure.com/free](https://azure.com/free?azure-portal=true).

## Configurer vos ressources Azure

Pour gagner du temps, sélectionnez ce modèle Azure Resource Manager afin de créer les ressources dont vous aurez besoin plus tard dans l’exercice :

1. [Déployer des ressources sur Azure](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMicrosoftLearning%2Fmslearn-knowledge-mining%2Fmain%2FLabfiles%2F07-exercise-add-to-index-use-push-api%20lab-files%2Fazuredeploy.json) : sélectionnez ce lien pour créer vos ressources Azure AI.
    ![Capture d’écran des options affichées dans le cadre du déploiement de ressources vers Azure.](../media/07-media/deploy-azure-resources.png)
1. Dans **Groupe de ressources**, sélectionnez **Créer**, nommez-le **cog-search-language-exe**.
1. Dans **Région**, sélectionnez une [région prise en charge](/azure/ai-services/language-service/custom-text-classification/service-limits#regional-availability) proche de vous.
1. Le **Préfixe de ressource** doit être globalement unique. Veuillez donc entrer un préfixe constitué d’un nombre aléatoire et de caractères en minuscules, par exemple **acs118245**.
1. Dans **Emplacement**, sélectionnez la même région que celle que vous avez choisie ci-dessus.
1. Sélectionnez **Revoir + créer**.
1. Sélectionnez **Create** (Créer).
1. Une fois le déploiement terminé, sélectionnez **Accéder au groupe de ressources** pour voir toutes les ressources que vous avez créées.

    ![Capture d’écran montrant toutes les ressources Azure déployées.](../media/07-media/azure-resources-created.png)

## Copier les informations de l’API REST du service Recherche Azure AI

1. Dans la liste des ressources, sélectionnez le service de recherche que vous avez créé. Dans l’exemple ci-dessus, **acs118245-search-service**.
1. copiez le nom du service de recherche dans un fichier texte.

    ![Capture d’écran de la section Clés d’un service de recherche.](../media/07-media/search-api-keys-exercise-version.png)
1. Sur la gauche, sélectionnez **Clés**, puis copiez la **Clé d’administration primaire** dans le même fichier texte.

## Cloner le référentiel dans Cloud Shell

Vous allez développer votre code à l’aide de Cloud Shell à partir du portail Azure. Les fichiers de code de votre application ont été fournis dans un référentiel GitHub.

> **Conseil** : si vous avez déjà cloné le référentiel **mslearn-knowledge-mining** récemment, vous pouvez ignorer cette tâche. Dans le cas contraire, procédez comme suit pour le cloner dans votre environnement de développement.

1. Dans le portail Azure, cliquez sur le bouton **[\>_]** à droite de la barre de recherche, en haut de la page, pour créer un environnement Cloud Shell dans le portail Azure, puis sélectionnez un environnement ***PowerShell***. Cloud Shell fournit une interface de ligne de commande dans un volet situé en bas du portail Azure.

    > **Remarque** : si vous avez déjà créé un Cloud Shell qui utilise un environnement *Bash*, basculez-le vers ***PowerShell***.

1. Dans la barre d’outils Cloud Shell, dans le menu **Paramètres**, sélectionnez **Accéder à la version classique** (cela est nécessaire pour utiliser l’éditeur de code).

    > **Conseil** : lorsque vous collez des commandes dans cloudshell, la sortie peut prendre une grande quantité de mémoire tampon d’écran. Vous pouvez effacer le contenu de l’écran en saisissant la commande `cls` pour faciliter le focus sur chaque tâche.

1. Dans le volet PowerShell, entrez les commandes suivantes pour cloner le référentiel GitHub pour cet exercice :

    ```
    rm -r mslearn-knowledge-mining -f
    git clone https://github.com/microsoftlearning/mslearn-knowledge-mining mslearn-knowledge-mining
    ```

1. Une fois le référentiel cloné, accédez au dossier contenant les fichiers de code de l’application :  

    ```
   cd mslearn-knowledge-mining/Labfiles/07-exercise-add-to-index-use-push-api/OptimizeDataIndexing
    ```

## Configuration de votre application

1. À l’aide de la commande `ls`, vous pouvez afficher le contenu du dossier **OptimizeDataIndexing**. Notez qu’il contient un fichier `appsettings.json` pour les paramètres de configuration.

1. Saisissez la commande suivante pour modifier le fichier de configuration fourni :

    ```
   code appsettings.json
    ```

    Le fichier s’ouvre dans un éditeur de code.

    ![Capture d’écran montrant le contenu du fichier appsettings.json.](../media/07-media/update-app-settings.png)

1. Collez le nom de votre service de recherche et la clé d’administration primaire.

    ```json
    {
      "SearchServiceUri": "https://acs118245-search-service.search.windows.net",
      "SearchServiceAdminApiKey": "YOUR_SEARCH_SERVICE_KEY",
      "SearchIndexName": "optimize-indexing"
    }
    ```

    Le fichier de paramètres devrait ressembler à celui ci-dessus.
   
1. Une fois que vous avez remplacé les espaces réservés, utilisez la commande **Ctrl+S** pour enregistrer vos modifications, puis utilisez la commande **Ctrl+Q** pour fermer l’éditeur de code tout en gardant la ligne de commande Cloud Shell ouverte.
1. Ensuite, dans le terminal, entrez `dotnet run` et appuyez sur **Entrée**.

    ![Capture d’écran montrant l’application s’exécutant dans VS Code avec une exception.](../media/07-media/debug-application.png)

    La sortie indique que dans ce cas, la taille de lot la plus performante est de 900 documents, avec le taux de transfert le plus élevé (Mo/seconde).
   
    >**Note** : vos valeurs de taux de transfert peuvent être différentes de ce qui est affiché dans la capture d’écran. Toutefois, la taille de lot la plus performante doit toujours être la même. 

## Modifier le code pour implémenter le threading et une stratégie d’interruption et de nouvelle tentative

Il existe un code commenté qui est prêt à modifier l’application pour utiliser des threads visant à charger des documents dans l’index de recherche.

1. Entrez la commande suivante pour ouvrir le fichier de code de l’application cliente :

    ```
   code Program.cs
    ```

1. Commentez les lignes 38 et 39 comme suit :

    ```csharp
    //Console.WriteLine("{0}", "Finding optimal batch size...\n");
    //await TestBatchSizesAsync(searchClient, numTries: 3);
    ```

1. Décommentez les lignes 41 à 49.

    ```csharp
    long numDocuments = 100000;
    DataGenerator dg = new DataGenerator();
    List<Hotel> hotels = dg.GetHotels(numDocuments, "large");

    Console.WriteLine("{0}", "Uploading using exponential backoff...\n");
    await ExponentialBackoff.IndexDataAsync(searchClient, hotels, 1000, 8);

    Console.WriteLine("{0}", "Validating all data was indexed...\n");
    await ValidateIndexAsync(indexClient, indexName, numDocuments);
    ```

    Le code qui contrôle la taille de lot et le nombre de threads est `await ExponentialBackoff.IndexDataAsync(searchClient, hotels, 1000, 8)`. La taille de lot est de 1 000 et les threads sont huit.

    ![Capture d’écran montrant tout le code modifié.](../media/07-media/thread-code-ready.png)

    Votre code devrait ressembler à celui ci-dessus.

1. Enregistrez les changements apportés.
1. Sélectionnez votre terminal, puis appuyez sur n’importe quelle touche pour mettre fin au processus en cours d’exécution si ce n’est pas déjà fait.
1. Exécutez `dotnet run` dans le terminal.

    L’application démarre huit threads, puis chaque thread termine l’écriture d’un nouveau message dans la console :

    ```powershell
    Finished a thread, kicking off another...
    Sending a batch of 1000 docs starting with doc 57000...
    ```

    Une fois le chargement de 100 000 documents terminé, l’application écrit un résumé (ce qui peut prendre un certain temps) :

    ```powershell
    Ended at: 9/1/2023 3:25:36 PM
    
    Upload time total: 00:01:18:0220862
    Upload time per batch: 780.2209 ms
    Upload time per document: 0.7802 ms
    
    Validating all data was indexed...
    
    Waiting for service statistics to update...
    
    Document Count is 100000
    
    Waiting for service statistics to update...
    
    Index Statistics: Document Count is 100000
    Index Statistics: Storage Size is 71453102
    
    ``````

Explorez le code dans la procédure `TestBatchSizesAsync` pour voir comment le code teste les performances de la taille de lot.

Explorez le code dans la procédure `IndexDataAsync` pour voir comment le code gère le threading.

Explorez le code dans `ExponentialBackoffAsync` pour voir comment le code implémente une stratégie de nouvelle tentative suite à une interruption exponentielle.

Vous pouvez rechercher et vérifier que les documents ont été ajoutés à l’index dans le portail Azure.

![Capture d’écran montrant l’index de recherche avec 100 000 documents.](../media/07-media/check-search-service-index.png)

## Nettoyage

Maintenant que vous avez terminé l’exercice, supprimez toutes les ressources dont vous n’avez plus besoin. Commencez par le code cloné sur votre ordinateur. Ensuite, supprimez les ressources Azure.

1. Dans le **portail Azure**, sélectionnez Groupes de ressources.
1. Sélectionnez le groupe de ressources que vous avez créé pour cet exercice.
1. Sélectionnez **Supprimer le groupe de ressources**. 
1. Confirmez la suppression, puis sélectionnez **Supprimer**.
1. Sélectionnez les ressources dont vous n’avez pas besoin, puis sélectionnez **Supprimer**.
