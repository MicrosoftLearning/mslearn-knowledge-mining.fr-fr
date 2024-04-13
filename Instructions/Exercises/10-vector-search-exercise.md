---
lab:
  title: Utiliser l’API REST pour exécuter des requêtes de recherche vectorielle
---

# Utiliser l’API REST pour exécuter des requêtes de recherche vectorielle

Dans cet exercice, vous allez configurer votre projet, créer un index, charger vos documents et exécuter des requêtes.

Pour cet exercice, vous aurez besoin des éléments suivants :

- L’application [Postman](https://www.postman.com/downloads/)
- Un abonnement Azure
- Service Search Azure AI
- L’exemple de collection Postman situé dans ce référentiel – *Vector-Search-Quickstart.postman_collection v1.0 json*.

> **Remarque** Si nécessaire, vous trouverez plus d’informations sur l’application Postman [ici](https://learn.microsoft.com/en-us/azure/search/search-get-started-rest).

## Configuration de votre projet

Commencez par configurer votre projet en effectuant les étapes suivantes :

1. Prenez note de l’**URL** et de la **Clé** dans votre service Recherche Azure AI.

    ![Illustration de l’emplacement pour le nom et les clés du service.](../media/vector-search/search keys.png)

1. Téléchargez l’[exemple de collection Postman](https://github.com/MicrosoftLearning/mslearn-knowledge-mining/blob/main/Labfiles/10-vector-search/Vector%20Search.postman_collection%20v1.0.json).
1. Ouvrez Postman et importez la collection en sélectionnant le bouton **Importer**, puis faites glisser et déposez le dossier de la collection dans la zone.

    ![Image de la boîte de dialogue Importer](../media/vector-search/import.png)

1. Sélectionnez le bouton **Dupliquer (fork)** pour créer une duplication de la collection et ajoutez un nom unique.
1. Cliquez avec le bouton droit sur le nom de votre collection, puis sélectionnez **Modifier**.
1. Sélectionnez l’onglet **Variables** et entrez les valeurs suivantes en utilisant le service de recherche et les noms d’index de votre service Recherche Azure AI :

    ![Diagramme montrant un exemple de paramètres de variable](../media/vector-search/variables.png)

1. Enregistrez vos modifications en sélectionnant le bouton **Enregistrer**.

Vous êtes prêt à envoyer vos demandes au service Recherche Azure AI.

## Créer un index

Ensuite, créez votre index dans Postman :

1. Sélectionnez **PUT Create/Update Index** dans le menu latéral.
1. Mettez à jour l’URL avec vos valeurs pour **search-service-name**, **index-name** et **api-version** que vous avez notées précédemment.
1. Sélectionnez l’onglet **Corps** pour voir la réponse.
1. Définissez le **index-name** sur la valeur de votre nom d’index de votre URL, puis sélectionnez **Envoyer**.

Vous devez voir un code d’état de type **200** qui indique une requête réussie.

## Charger des documents

108 documents sont inclus dans la requête Charger des documents, chacun ayant un ensemble complet d’incorporations pour les champs **titleVector** et **contentVector**.

1. Sélectionnez **POST Upload Docs** dans le menu latéral.
1. Mettez à jour l’URL avec vos valeurs pour **search-service-name**, **index-name** et **api-version** comme auparavant.
1. Sélectionnez l’onglet **Corps** pour voir la réponse, puis sélectionnez **Envoyer**.

Vous devez voir un code d’état de type **200** indiquant la réussite de votre requête.

## Exécuter des requêtes

1. Essayez maintenant d’exécuter les requêtes suivantes sur le menu latéral. Pour cela, veillez à mettre à jour l’URL chaque fois comme auparavant, puis envoyez une requête en sélectionnant **Envoyer** :

    - Recherche vectorielle unique
    - Recherche vectorielle unique avec filtre
    - Recherche hybride simple
    - Recherche hybride simple avec filtre
    - Recherche interchamps
    - Recherche multirequête

1. Sélectionnez l’onglet **Corps** pour voir la réponse et visualiser les résultats.

Vous devez voir un code d’état de type **200** qui indique une requête réussie.
