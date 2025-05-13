---
lab:
  title: Implémenter des améliorations pour les résultats de la recherche
---

# Implémenter des améliorations pour les résultats de la recherche

Vous disposez d’un service de recherche existant utilisé par une application de réservation de vacances. Vous avez constaté que la pertinence des résultats de recherche a un impact sur le nombre de réservations que vous obtenez. Vous venez aussi d’ajouter des hôtels situés au Portugal et vous aimeriez proposer le portugais comme langue prise en charge.

Dans cet exercice, vous allez ajouter un profil de score pour améliorer la pertinence des résultats de la recherche. Ensuite, vous allez utiliser Azure AI Services pour ajouter des descriptions en portugais de tous vos hôtels.

> **Remarque** Pour effectuer cet exercice, vous aurez besoin d’un abonnement Microsoft Azure. Si vous n’en avez pas, vous pouvez vous inscrire à une évaluation gratuite dans la page [https://azure.com/free](https://azure.com/free?azure-portal=true).

## Créer des ressources Azure

Vous allez créer un service Recherche Azure AI et importer des exemples de données sur des hôtels.

1. Connectez-vous au [portail Azure](https://portal.azure.com/learn.docs.microsoft.com?azure-portal=true).
1. Sélectionnez **+ Créer une ressource**.
1. Recherchez **recherche**, puis sélectionnez **Recherche Azure AI**.
1. Sélectionnez **Créer**.
1. Sélectionnez **Créer nouveau** sous Groupe de ressources et nommez-le **learn-advanced-search**.
1. Dans **Nom du service**, entrez **advanced-search-service-12345**. Le nom doit être globalement unique, alors ajoutez des chiffres aléatoires à la fin du nom.
1. Sélectionnez une région prise en charge proche de vous.
1. Utilisez les valeurs par défaut pour le **niveau tarifaire**.
1. Sélectionnez **Revoir + créer**.
1. Sélectionnez **Create** (Créer).
1. Attendez que les ressources se déploient, puis sélectionnez **Accéder à la ressource**.

### Importer des exemples de données dans le service de recherche

Importez les exemples de données.

1. Dans le volet **Vue d’ensemble**, sélectionnez **Importer des données**.

    ![Capture d’écran montrant le menu Importer les données.](../media/05-media/import-data-new.png)
1. Dans le volet **Importer des données**, dans la liste déroulante **Source de données**, sélectionnez **Exemples**.
1. Sélectionnez **hotels-sample**.

1. Sous l’onglet **Ajouter des compétences cognitives (facultatif)**, développez **Attacher AI Services**, puis sélectionnez **Créer une ressource AI Services**.

    ![Capture d’écran montrant la sélection et l’ajout d’Azure AI Services.](../media/05-media/add-cognitive-services-new.png)

### Créer un service Azure AI pour prendre en charge des traductions

1. Sous un nouvel onglet, connectez-vous au portail Azure.
1. Dans **Groupe de ressources**, sélectionnez **learn-advanced-search**.
1. Dans **Région**, sélectionnez la même région que celle que vous avez choisie pour le service de recherche.
1. Dans **Nom**, entrez **learn-cognitive-translator-12345** ou un nom de votre choix. Le nom doit être globalement unique, alors ajoutez des chiffres aléatoires à la fin du nom.
1. Dans **Niveau tarifaire**, sélectionnez **Standard S0**.
1. Cochez **En cochant cette case, j’ai reconnu que j’ai lu et compris tous les termes ci-dessous**.
1. Sélectionnez **Revoir + créer**.
1. Sélectionnez **Create** (Créer).
1. Une fois les ressources créées, fermez l’onglet.

### Ajouter un enrichissement de traduction

1. Sous l’onglet **Ajouter des compétences cognitives** (facultatif), sélectionnez Actualiser.
1. Sélectionnez le nouveau service **learn-cognitive-translator-12345**.
1. Développez la section **Ajouter des enrichissements**.
    ![Capture d’écran montrant l’ajout de la traduction portugaise.](../media/05-media/add-translation-enrichment-new.png)
1. Sélectionnez **Traduire le texte**, remplacez **Langue cible** par **Portugais**, puis **Nom de champ** par **Description_pt**.
1. Sélectionnez **Suivant : Personnaliser l’index cible**.

### Modifier le champ pour stocker le texte traduit

1. Sous l’onglet **Personnaliser l’index cible**, faites défiler la liste de champs jusqu’en bas et remplacez **Analyseur** par **Portugais (Portugal) - Microsoft** pour le champ **Description_pt**.
1. Sélectionnez **Suivant : Créer un indexeur**.
1. Sélectionnez **Envoyer**.

    L’index est créé, l’indexeur va s’exécuter et 50 documents contenant des exemples de données sur les hôtels vont être importés.
1. Dans le volet **Vue d’ensemble**, sélectionnez **Index**, puis **hotels-sample-index**.
1. Sélectionnez **Rechercher** pour voir le JSON de tous les documents inclus dans l’index.
1. Recherchez **Description_pt** dans les résultats (vous pouvez pour cela utiliser **Ctrl+F**) : vous pouvez remarquer qu’il ne s’agit pas d’une traduction en portugais de la description en anglais, mais que cela se présente à la place comme ceci :

    ```json
    "Description_pt": "45",
    ```

Le portail Azure part du principe que le premier champ du document a besoin d’être traduit. Il utilise donc la compétence de traduction actuelle pour traduire le `HotelId`.

### Mettre à jour l’ensemble de compétences pour traduire le champ approprié dans le document

1. En haut de la page, sélectionnez le service de recherche via le lien **advanced-search-service-12345 |Indexes**.
1. Sélectionnez **Ensembles de compétences** sous Gestion de la recherche dans le volet gauche, puis sélectionnez **hotels-sample-skillset**.
1. Modifiez le document JSON, remplacez la ligne 9 par :

    ```json
    "context": "/document/Description",
    ```

1. Remplacez la langue par défaut par Anglais à la ligne 11 :

    ```json
    "defaultFromLanguageCode": "en",
    ```

1. Remplacez le champ source à la ligne 15 par :

    ```json
    "source": "/document/Description",
    ```

1. Cliquez sur **Enregistrer**.
1. En haut de la page, sélectionnez le service de recherche via le lien **advanced-search-service-12345 | Skillsets**.
1. Dans le volet **Vue d’ensemble**, sélectionnez **Indexeurs**, puis **hotels-sample-indexer**.
1. Sélectionnez **Modifier le fichier JSON**.
1. Remplacez le champ source à la ligne 20 par :

    ```json
    "sourceFieldName": "/document/Description/Description_pt",
    ```

1. Cliquez sur **Enregistrer**.
1. Sélectionnez **Réinitialiser**, puis **Oui**.
1. Sélectionnez **Exécuter**, puis **Oui**.

### Tester l’index mis à jour

1. En haut de la page, sélectionnez le service de recherche via le lien **advanced-search-service-12345 | Indexers**.
1. Dans le volet **Vue d’ensemble**, sélectionnez **Index**, puis **hotels-sample-index**.
1. Sélectionnez **Rechercher** pour voir le JSON de tous les documents inclus dans l’index.
1. Recherchez **Description_pt** dans les résultats et remarquez la présence d’une description en portugais.

    ```json
    "Description_pt": "O maior resort durante todo o ano da área oferecendo mais de tudo para suas férias – pelo melhor valor!  O que você pode desfrutar enquanto estiver no resort, além das praias de areia de 1,5 km do lago? Confira nossas atividades com certeza para excitar tanto os jovens quanto os jovens hóspedes do coração. Temos tudo, incluindo ser chamado de \"Propriedade do Ano\" e um \"Top Ten Resort\" pelas principais publicações.",
    ```

1. Vous allez maintenant rechercher les hôtels qui offrent une vue sur un lac. Vous allez commencer par utiliser une recherche simple qui retourne seulement `HotelName`, `Description`, `Category` et `Tags`. Dans **Chaîne de requête**, entrez cette recherche :

    `lake + view&$select=HotelName,Description,Category,Tags&$count=true`

    Parcourez les résultats et essayez de trouver les champs qui correspondent aux termes de recherche `lake` et `view`. Notez cet hôtel et sa position :

    ```json
    {
      "@search.score": 0.9433406,
      "HotelName": "Lady Of The Lake B & B",
      "Description": "Nature is Home on the beach.  Save up to 30 percent. Valid Now through the end of the year. Restrictions and blackout may apply.",
      "Category": "Luxury",
      "Tags": [
        "laundry service",
        "concierge",
        "view"
      ]
    },
    ```

Cet hôtel a correspondu au terme « lake » dans le champ `HotelName` et au terme « view » dans le champ `Tags`. Vous voulez stimuler les correspondances des termes dans le champ `Description` plutôt que dans le nom de l’hôtel. Idéalement, cet hôtel doit figurer en dernier dans les résultats.

## Ajouter un profil de score pour améliorer les résultats de la recherche

1. Sélectionnez l’onglet **Profils de scoring**.
1. Sélectionnez **+ Ajouter un profil de scoring**.
1. Dans **Nom du profil**, entrez **boost-description-categories**.
1. Ajoutez les champs et les pondérations suivants sous **Pondérations** :

    ![Capture d’écran de pondérations en cours d’ajout à un profil de score.](../media/05-media/add-weights-new.png)
1. Dans **Nom du champ**, sélectionnez **Description**.
1. Pour **Pondération**, entrez **5**.
1. Dans **Nom du champ**, sélectionnez **Catégorie**.
1. Pour **Pondération**, entrez **3**.
1. Dans **Nom du champ**, sélectionnez **Étiquettes**.
1. Pour **Pondération**, entrez **2**.
1. Sélectionnez **Enregistrer**.
1. Sélectionnez **Enregistrer** en haut.

### Tester l’index mis à jour

1. Revenez à l’onglet **Explorateur de recherche** de la page **hotels-sample-index**.
1. Dans **Chaîne de requête**, entrez la même recherche que précédemment :

    `lake + view&$select=HotelName,Description,Category,Tags&$count=true`

    Examinez les résultats de la recherche.

    ```json
    {
      "@search.score": 3.5707965,
      "HotelName": "Lady Of The Lake B & B",
      "Description": "Nature is Home on the beach.  Save up to 30 percent. Valid Now through the end of the year. Restrictions and blackout may apply.",
      "Category": "Luxury",
      "Tags": [
        "laundry service",
        "concierge",
        "view"
      ]
    }
    ```

    Le score de recherche a augmenté, de **0,9433406** à **3,5707965**. Toutefois, tous les autres hôtels ont des scores calculés plus élevés. Cet hôtel figure maintenant en dernier dans les résultats.

## Nettoyage

Maintenant que vous avez terminé l’exercice, supprimez toutes les ressources dont vous n’avez plus besoin.

1. Dans le portail Azure, sélectionnez **Groupes de ressources**.
1. Sélectionnez le groupe de ressources dont vous n’avez plus besoin, puis **Supprimer le groupe de ressources**.
