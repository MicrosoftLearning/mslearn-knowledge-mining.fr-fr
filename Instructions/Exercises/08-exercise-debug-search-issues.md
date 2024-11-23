---
lab:
  title: Déboguer les problèmes liés à la recherche
---

# Déboguer les problèmes liés à la recherche

Vous avez créé votre solution de recherche, mais vous remarquez la présence d’avertissements sur l’indexeur.

Dans cet exercice, vous allez créer une solution Recherche Azure AI, importer des exemples de données, puis résoudre un avertissement sur l’indexeur.

> **Remarque** Pour effectuer cet exercice, vous aurez besoin d’un abonnement Microsoft Azure. Si vous n’en avez pas, vous pouvez vous inscrire à une évaluation gratuite dans la page [https://azure.com/free](https://azure.com/free?azure-portal=true).

## Créer une solution de recherche

Avant de pouvoir utiliser une session de débogage, vous devez créer un service de recherche Azure AI.

1. [Déployer des ressources vers Azure](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FMicrosoftLearning%2Fmslearn-knowledge-mining%2Fmain%2FLabfiles%2F08-debug-search%2Fazuredeploy.json) - Si vous êtes sur une machine virtuelle hébergée, copiez ce lien et collez-le dans le navigateur de la machine virtuelle. Sinon, sélectionnez ce lien pour déployer toutes les ressources dont vous avez besoin dans le portail Azure.

    ![Capture d’écran du modèle de déploiement arm avec des champs remplis.](../media/08-media/arm-template-deployment.png)

1. Dans **Groupe de ressources**, sélectionnez le groupe de ressources qui vous a été fourni ou sélectionnez **Créer** et saisissez **debug-search-exercise**.
1. Sélectionnez la **région** la plus proche de vous, ou utilisez la valeur par défaut.
1. Pour le **Préfixe de ressource**, saisissez **debugsearch** et ajoutez une combinaison aléatoire de nombres ou de caractères pour vous assurer que le nom de stockage est unique.
1. Dans Emplacement, sélectionnez la même région que celle utilisée ci-dessus.
1. Au bas du volet, sélectionnez **Vérifier + créer**.
1. Attendez que la ressource soit déployée, puis sélectionnez **Accéder au groupe de ressources**.

## Importer des exemples de données et configurer des ressources

Une fois vos ressources créées, vous pouvez importer vos données sources.

1. Dans les ressources répertoriées, accédez au compte de stockage. Accédez à **Configuration** dans le volet de gauche, définissez **Autoriser l’accès anonyme Blob** sur **Activé**, puis sélectionnez **Enregistrer**.
1. Revenez à votre groupe de ressources, puis sélectionnez le service de recherche.
1. Dans le volet **Vue d’ensemble**, sélectionnez **Importer des données**.

      ![Capture d’écran montrant le menu Importer des données sélectionné.](../media/08-media/import-data.png)

1. Dans le volet Importer des données, sélectionnez **Exemples** comme Source de données.

      ![Capture d’écran montrant les champs remplis.](../media/08-media/import-data-selection-screen-small.png)

1. Dans la liste des exemples, sélectionnez **hotels-sample**.
1. Sélectionnez **Suivant : Ajouter des compétences cognitives (facultatif)**.
1. Développez la section **Ajouter des enrichissements**.

    ![Capture d’écran des options d’ajout d’enrichissements.](../media/08-media/add-enrichments.png)

1. Sélectionnez **Compétences cognitives de texte**.
1. Sélectionnez **Suivant : Personnaliser l’index cible**.
1. Conservez les valeurs par défaut, puis sélectionnez **Suivant : Créer un indexeur**.
1. Sélectionnez **Envoyer**.

## Utiliser une session de débogage pour résoudre les avertissements sur votre indexeur

L’indexeur commence maintenant à ingérer 50 documents. Cependant, si vous examinez l’état de l’indexeur, vous constatez qu’il y a des avertissements.

![Capture d’écran montrant 150 avertissements sur l’indexeur.](../media/08-media/indexer-warnings.png)

1. Sélectionnez **Sessions de débogage** dans le volet gauche.
1. Sélectionnez **+ Ajouter une session de débogage**.
1. Fournissez un nom pour la session, puis sélectionnez **hotel-sample-indexer** pour le **Modèle d’indexeur**.
1. Sélectionnez votre compte de stockage à partir du champ **Compte de stockage**. Cela crée automatiquement un conteneur de stockage pour vous permettre de stocker les données de débogage.
1. Laissez la case d’authentification à l’aide d’une identité managée non cochée.
1. Cliquez sur **Enregistrer**.
1. Une fois créée, la session de débogage s’exécute automatiquement sur les données de votre service de recherche. Elle doit se terminer avec des erreurs/avertissements.

    Le graphe des dépendances vous montre une erreur sur trois compétences pour chaque document.
    ![Capture d’écran montrant les trois erreurs sur un document enrichi.](../media/08-media/debug-session-errors.png)

    > **Note** : il est possible qu’une erreur s’affiche concernant la connexion au compte de stockage et la configuration des identités managées. Cela se produit si vous essayez de déboguer trop rapidement après avoir activé l’accès anonyme Blob. L’exécution de la session de débogage doit toujours fonctionner. Actualiser la fenêtre du navigateur après quelques minutes devrait supprimer l’avertissement.

1. Dans le graphique des dépendances, sélectionnez l’un des nœuds de compétence qui possèdent une erreur.
1. Dans le volet d’informations des compétences, sélectionnez **Erreurs/Avertissements(1)**.

    Les détails sont les suivants :

    *Code de langue non valide « (Inconnu) ». Langues prises en charge : af, am, ar, as, az, bg, bn, bs, ca, cs, cy, da, de, el, en, es, et, eu, fa, fi, fr, ga, gl, gu, he, hi, hr, hu, hy, id, it, ja, ka, kk, km, kn, ko, ku, ky, lo, lt, lv, mg, mk, ml, mn, mr, ms, my, ne, nl, no, or, pa, pl, ps, pt-BR, pt-PT, ro, ru, sk, sl, so, sq, sr, ss, sv, sw, ta, te, th, tr, ug, uk, ur, uz, vi, zh-Hans, zh-Hant. Pour plus d’informations, consultez https://aka.ms/language-service/language-support.*

    Si vous examinez le graphique des dépendances, la compétence Détection de langue possède des sorties vers les trois compétences avec des erreurs. Si vous examinez les paramètres des compétences avec des erreurs, vous verrez que l’entrée de compétence à l’origine de l’erreur est `languageCode`.

1. Dans le graphe des dépendances, sélectionnez **Détection de langue**.

    ![Capture d’écran montrant les paramètres de la compétence Détection de langue.](../media/08-media/language-detection-skill-settings.png)
    Si vous examinez le code JSON des paramètres de compétence, vous pouvez voir que le champ utilisé pour déduire la langue est `HotelId`.

    Ce champ est à l’origine de l’erreur, car la compétence ne peut pas déterminer la langue en fonction d’un ID.

## Résoudre l’avertissement sur l’indexeur

1. Sélectionnez **Source** sous Entrées, puis remplacez la valeur du champ par `/document/Description`.
1. Cliquez sur **Enregistrer**.
1. Sélectionnez **Exécuter**. L’indexeur ne doit plus indiquer d’erreurs ou d’avertissements. L’ensemble de compétences peut maintenant être mis à jour.

    ![Capture d’écran montrant une exécution complète sans erreurs.](../media/08-media/debug-session-complete.png)
   
1. Sélectionnez **Valider les modifications** pour envoyer les modifications apportées dans cette session à votre indexeur.
1. Cliquez sur **OK**. Vous pouvez maintenant supprimer votre session.

Vous devez maintenant vérifier que votre ensemble de compétences est attaché à une ressource Azure AI Services, sans quoi vous allez atteindre le quota de base et l’indexeur va dépasser le délai d’expiration. 

1. Pour cela, sélectionnez **Ensembles de compétences** dans le volet gauche, puis sélectionnez votre **hotels-sample-skillset**.

    ![Capture d’écran montrant la liste des ensemble de compétences.](../media/08-media/update-skillset.png)
1. Sélectionnez **Connecter le service IA**, puis sélectionnez la ressource de services IA dans la liste.

    ![Capture d’écran montrant la ressource Azure AI Services à attacher à l’ensemble de compétences.](../media/08-media/skillset-attach-service.png)
1. Sélectionnez **Enregistrer**.

1. Exécutez maintenant votre indexeur pour mettre à jour les documents avec les enrichissements d’IA corrigés. Pour cela, sélectionnez **Indexeurs** dans le volet gauche, sélectionnez **hotels-sample-indexer**, puis sélectionnez **Exécuter**.  Quand il a fini de s’exécuter, vous devez normalement voir que le nombre d’avertissements est maintenant de zéro.

    ![Capture d’écran montrant tout ce qui a été résolu.](../media/08-media/warnings-fixed-indexer.png)

## Nettoyage

 Maintenant que vous avez terminé l’exercice, si vous avez fini d’explorer les services Recherche Azure AI, supprimez les ressources Azure que vous avez créées au cours de l’exercice. Pour cela, le moyen le plus simple est de supprimer le groupe de ressources **debug-search-exercise**.
