<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" original="markdown" source-language="en-US" target-language="fr-FR">
    <header>
      <tool tool-id="JunoTransformer" tool-name="JunoTransformer" tool-version="1.0.0" tool-company="Microsoft"><transformer-options xmlns="urn:microsoft:content:juno:1.0"><option name="TargetXliffVersion" value="V1"/><option name="ArtToXliff" value="False"/><option name="UseParagraphMarker" value="False"/><option name="ExposeLinkTitleText" value="False"/><option name="ReplaceNewlineWithWhitespace" value="False"/><option name="LockAtSign" value="False"/><option name="ExposeImageTitleText" value="True"/><option name="LockBackslashEscapeChars" value="False"/><option name="PairHtmlTags" value="False"/><option name="TrimBoundingPhTags" value="False"/><option name="MergeAdjacentPhTags" value="False"/><option name="LinkifyHeaders" value="False"/></transformer-options></tool>
    </header>
    <body>
      <group id="content" extype="content">
        <group id="p101-PARA"><group id="s101-PARA"><trans-unit id="101" translate="yes" xml:space="preserve" restype="x-metadata">
          <source>Create an Azure AI Search solution</source><target>Créer une solution Recherche Azure AI</target>
        </trans-unit></group></group>
        <group id="p102-PARA"><group id="s102-PARA"><trans-unit id="102" translate="yes" xml:space="preserve">
          <source>Create an Azure AI Search solution</source><target>Créer une solution Recherche Azure AI</target>
        </trans-unit></group></group>
        <group id="p103-PARA"><group id="s103-PARA"><trans-unit id="103" translate="yes" xml:space="preserve">
          <source>All organizations rely on information to make decisions, answer questions, and function efficiently.</source><target>Toutes les organisations s’appuient sur des informations pour prendre des décisions, répondre à des questions et fonctionner efficacement.</target>
        </trans-unit></group></group>
        <group id="p104-PARA"><group id="s104-PARA"><trans-unit id="104" translate="yes" xml:space="preserve">
          <source>The problem for most organizations is not a lack of information, but the challenge of finding and  extracting the information from the massive set of documents, databases, and other sources in which the information is stored.</source><target>Le problème pour la plupart des organisations n’est pas un manque d’informations, mais la difficulté de trouver et d’extraire les informations à partir de l’ensemble des documents, bases de données et autres sources dans lesquelles les informations sont stockées.</target>
        </trans-unit></group></group>
        <group id="p105-PARA"><group id="s105-PARA"><trans-unit id="105" translate="yes" xml:space="preserve">
          <source>For example, suppose <bpt id="p1">*</bpt>Margie's Travel<ept id="p1">*</ept> is a travel agency that specializes in organizing trips to cities around the world.</source><target>Par exemple, supposons que <bpt id="p1">*</bpt>Margie’s Travel<ept id="p1">*</ept> est une agence de voyages spécialisée dans l’organisation de voyages dans des villes du monde entier.</target>
        </trans-unit></group></group>
        <group id="p106-PARA"><group id="s106-PARA"><trans-unit id="106" translate="yes" xml:space="preserve">
          <source>Over time, the company has amassed a huge amount of information in documents such as brochures, as well as reviews of hotels submitted by customers.</source><target>Au fil du temps, l’entreprise a accumulé de grandes quantités d’informations dans des documents tels que des brochures, ainsi que des critiques d’hôtels soumises par des clients.</target>
        </trans-unit></group></group>
        <group id="p107-PARA"><group id="s107-PARA"><trans-unit id="107" translate="yes" xml:space="preserve">
          <source>This data is a valuable source of insights for travel agents and customers as they plan trips, but the sheer volume of data can make it difficult to find relevant information to answer a specific customer question.</source><target>Ces données sont une source précieuse d’insights pour les agents de voyages et les clients lorsqu’ils planifient des voyages, mais le volume de données peut compliquer la recherche d’informations pertinentes pour répondre à une question de client spécifique.</target>
        </trans-unit></group></group>
        <group id="p108-PARA"><group id="s108-PARA"><trans-unit id="108" translate="yes" xml:space="preserve">
          <source>To address this challenge, Margie's Travel can use Azure AI Search to implement a solution in which the documents are indexed and enriched by using AI skills to make them easier to search.</source><target>Pour relever ce défi, Margie’s Travel peut utiliser la recherche Azure AI pour implémenter une solution dans laquelle les documents sont indexés et enrichis à l’aide de compétences de l’IA pour faciliter leur recherche.</target>
        </trans-unit></group></group>
        <group id="p109-PARA"><group id="s109-PARA"><trans-unit id="109" translate="yes" xml:space="preserve">
          <source>Create Azure resources</source><target>Créer des ressources Azure</target>
        </trans-unit></group></group>
        <group id="p110-PARA"><group id="s110-PARA"><trans-unit id="110" translate="yes" xml:space="preserve">
          <source>The solution you will create for Margie's Travel requires the following resources in your Azure subscription:</source><target>La solution que vous allez créer pour Margie’s Travel nécessite les ressources suivantes dans votre abonnement Azure :</target>
        </trans-unit></group></group>
        <group id="p111-PARA"><group id="s111-PARA"><trans-unit id="111" translate="yes" xml:space="preserve">
          <source>An <bpt id="p1">**</bpt>Azure AI Search<ept id="p1">**</ept> resource, which will manage indexing and querying.</source><target>Une ressource <bpt id="p1">**</bpt>Recherche Azure AI<ept id="p1">**</ept>, qui va gérer l’indexation et l’interrogation.</target>
        </trans-unit></group></group>
        <group id="p112-PARA"><group id="s112-PARA"><trans-unit id="112" translate="yes" xml:space="preserve">
          <source>An <bpt id="p1">**</bpt>Azure AI Services<ept id="p1">**</ept> resource, which provides AI services for skills that your search solution can use to enrich the data in the data source with AI-generated insights.</source><target>Une ressource <bpt id="p1">**</bpt>Azure AI services<ept id="p1">**</ept>, qui fournit les services d’IA pour les compétences que votre solution de recherche peut utiliser pour enrichir les données de la source de données avec des aperçus générés par l’IA.</target>
        </trans-unit></group></group>
        <group id="p113-PARA"><group id="s113-PARA"><trans-unit id="113" translate="yes" xml:space="preserve">
          <source>A <bpt id="p1">**</bpt>Storage account<ept id="p1">**</ept> with a blob container in which the documents to be searched are stored.</source><target>Un <bpt id="p1">**</bpt>compte de stockage<ept id="p1">**</ept> avec un conteneur blob dans lequel les documents à rechercher sont stockés.</target>
        </trans-unit></group></group>
        <group id="p114-PARA"><group id="s114-PARA"><trans-unit id="114" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Important<ept id="p1">**</ept>: Your Azure AI Search and Azure AI Services resources must be in the same location!</source><target><bpt id="p1">**</bpt>Important :<ept id="p1">**</ept> vos ressources Recherche Azure AI et Azure AI Services doivent se trouver au même endroit !</target>
        </trans-unit></group></group>
        <group id="p115-PARA"><group id="s115-PARA"><trans-unit id="115" translate="yes" xml:space="preserve">
          <source>Create an Azure AI Search resource</source><target>Créer une ressource Recherche Azure AI</target>
        </trans-unit></group></group>
        <group id="p116-PARA"><group id="s116-PARA"><trans-unit id="116" translate="yes" xml:space="preserve">
          <source>In a web browser, open the Azure portal at <ph id="ph1">`https://portal.azure.com`</ph>, and sign in using the Microsoft account associated with your Azure subscription.</source><target>Ouvrez le portail Azure à l’adresse <ph id="ph1">`https://portal.azure.com`</ph> et connectez-vous avec le compte Microsoft associé à votre abonnement Azure.</target>
        </trans-unit></group></group>
        <group id="p117-PARA"><group id="s117-PARA"><trans-unit id="117" translate="yes" xml:space="preserve">
          <source>Select the <bpt id="p1">**</bpt>&amp;#65291;Create a resource<ept id="p1">**</ept> button, search for <bpt id="p2">*</bpt>search<ept id="p2">*</ept>, and create an <bpt id="p3">**</bpt>Azure AI Search<ept id="p3">**</ept> resource with the following settings:</source><target>Sélectionnez le bouton <bpt id="p1">**</bpt>&amp;#65291;Créer une ressource<ept id="p1">**</ept>, recherchez <bpt id="p2">*</bpt>recherche<ept id="p2">*</ept>, puis créez une ressource <bpt id="p3">**</bpt>Recherche Azure AI<ept id="p3">**</ept> avec les paramètres suivants :</target>
        </trans-unit></group></group>
        <group id="p118-PARA"><group id="s118-PARA"><trans-unit id="118" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Subscription<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Your Azure subscription<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Abonnement<ept id="p1">**</ept> : <bpt id="p2">*</bpt>votre abonnement Azure<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p119-PARA"><group id="s119-PARA"><trans-unit id="119" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Resource group<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Create a new resource group (if you are using a restricted subscription, you may not have permission to create a new resource group - use the one provided)<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Groupe de ressources<ept id="p1">**</ept> : <bpt id="p2">*</bpt>Créez un groupe de ressources. (Si vous utilisez un abonnement restreint, vous n’avez peut-être pas l’autorisation de créer un groupe de ressources. Dans ce cas, utilisez le groupe fourni.)<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p120-PARA"><group id="s120-PARA"><trans-unit id="120" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Service name<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Enter a unique name<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Nom du service<ept id="p1">**</ept> : <bpt id="p2">*</bpt>entrez un nom unique<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p121-PARA"><group id="s121-PARA"><trans-unit id="121" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Location<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Select a location - note that your Azure AI Search and Azure AI Services resources must be in the same location<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Emplacement<ept id="p1">**</ept> : <bpt id="p2">*</bpt>sélectionnez un emplacement. Vos ressources Recherche Azure AI et Azure AI Services doivent se trouver au même emplacement<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p122-PARA"><group id="s122-PARA"><trans-unit id="122" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Pricing tier<ept id="p1">**</ept>: Basic</source><target><bpt id="p1">**</bpt>Niveau tarifaire<ept id="p1">**</ept> : De base</target>
        </trans-unit></group></group>
        <group id="p123-PARA"><group id="s123-PARA"><trans-unit id="123" translate="yes" xml:space="preserve">
          <source>Wait for deployment to complete, and then go to the deployed resource.</source><target>Attendez la fin du déploiement, puis accédez à la ressource déployée.</target>
        </trans-unit></group></group>
        <group id="p124-PARA"><group id="s124-PARA"><trans-unit id="124" translate="yes" xml:space="preserve">
          <source>Review the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page on the blade for your Azure AI Search resource in the Azure portal.</source><target>Passez en revue la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> du panneau de votre ressource Recherche Azure AI dans le Portail Azure.</target>
        </trans-unit></group></group>
        <group id="p125-PARA"><group id="s125-PARA"><trans-unit id="125" translate="yes" xml:space="preserve">
          <source>Here, you can use a visual interface to create, test, manage, and monitor the various components of a search solution; including data sources, indexes, indexers, and skillsets.</source><target>Ici, vous pouvez utiliser une interface visuelle pour créer, tester, gérer et surveiller les différents composants d’une solution de recherche ; y compris les sources de données, les index, les indexeurs et les ensembles de compétences.</target>
        </trans-unit></group></group>
        <group id="p126-PARA"><group id="s126-PARA"><trans-unit id="126" translate="yes" xml:space="preserve">
          <source>Create an Azure AI Services resource</source><target>Créer une ressource Azure AI Services</target>
        </trans-unit></group></group>
        <group id="p127-PARA"><group id="s127-PARA"><trans-unit id="127" translate="yes" xml:space="preserve">
          <source>If you don't already have one in your subscription, you'll need to provision an <bpt id="p1">**</bpt>Azure AI Services<ept id="p1">**</ept> resource.</source><target>Si vous n’en avez pas encore dans votre abonnement, vous devez approvisionner une ressource <bpt id="p1">**</bpt>Azure AI Services<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p128-PARA"><group id="s128-PARA"><trans-unit id="128" translate="yes" xml:space="preserve">
          <source>Your search solution will use this to enrich the data in the datastore with AI-generated insights.</source><target>Votre solution de recherche va l’utiliser pour enrichir les données dans le magasin de données avec des insights générés par IA.</target>
        </trans-unit></group></group>
        <group id="p129-PARA"><group id="s129-PARA"><trans-unit id="129" translate="yes" xml:space="preserve">
          <source>Return to the home page of the Azure portal, and then select the <bpt id="p1">**</bpt>&amp;#65291;Create a resource<ept id="p1">**</ept> button, search for <bpt id="p2">*</bpt>Azure AI Services<ept id="p2">*</ept>, and create an <bpt id="p3">**</bpt>Azure AI Services<ept id="p3">**</ept> resource with the following settings:</source><target>Revenez à la page d’accueil du Portail Azure, puis sélectionnez le bouton <bpt id="p1">**</bpt>&amp;#65291;Créer une ressource<ept id="p1">**</ept>, recherchez <bpt id="p2">*</bpt>Azure AI Services<ept id="p2">*</ept>, puis créez une ressource <bpt id="p3">**</bpt>Azure AI Services<ept id="p3">**</ept> avec les paramètres suivants :</target>
        </trans-unit></group></group>
        <group id="p130-PARA"><group id="s130-PARA"><trans-unit id="130" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Subscription<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Your Azure subscription<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Abonnement<ept id="p1">**</ept> : <bpt id="p2">*</bpt>votre abonnement Azure<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p131-PARA"><group id="s131-PARA"><trans-unit id="131" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Resource group<ept id="p1">**</ept>: <bpt id="p2">*</bpt>The same resource group as your Azure AI Search resource<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Groupe de ressources<ept id="p1">**</ept> : <bpt id="p2">*</bpt> le même groupe de ressources que votre ressource Recherche Azure AI<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p132-PARA"><group id="s132-PARA"><trans-unit id="132" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Region<ept id="p1">**</ept>: <bpt id="p2">*</bpt>The same location as your Azure AI Search resource<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Région<ept id="p1">**</ept> : <bpt id="p2">*</bpt> le même emplacement que votre ressource Recherche Azure AI<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p133-PARA"><group id="s133-PARA"><trans-unit id="133" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Name<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Enter a unique name<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Nom<ept id="p1">**</ept> : <bpt id="p2">*</bpt>Entrez un nom unique.<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p134-PARA"><group id="s134-PARA"><trans-unit id="134" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Pricing tier<ept id="p1">**</ept>: Standard S0</source><target><bpt id="p1">**</bpt>Niveau tarifaire<ept id="p1">**</ept> : Standard S0</target>
        </trans-unit></group></group>
        <group id="p135-PARA"><group id="s135-PARA"><trans-unit id="135" translate="yes" xml:space="preserve">
          <source>Select the required checkboxes and create the resource.</source><target>Cochez les cases nécessaires et créez la ressource.</target>
        </trans-unit></group></group>
        <group id="p136-PARA"><group id="s136-PARA"><trans-unit id="136" translate="yes" xml:space="preserve">
          <source>Wait for deployment to complete, and then view the deployment details.</source><target>Attendez la fin du déploiement, puis visualisez les détails du déploiement.</target>
        </trans-unit></group></group>
        <group id="p137-PARA"><group id="s137-PARA"><trans-unit id="137" translate="yes" xml:space="preserve">
          <source>Create a storage account</source><target>Créez un compte de stockage.</target>
        </trans-unit></group></group>
        <group id="p138-PARA"><group id="s138-PARA"><trans-unit id="138" translate="yes" xml:space="preserve">
          <source>Return to the home page of the Azure portal, and then select the <bpt id="p1">**</bpt>&amp;#65291;Create a resource<ept id="p1">**</ept> button, search for <bpt id="p2">*</bpt>storage account<ept id="p2">*</ept>, and create a <bpt id="p3">**</bpt>Storage account<ept id="p3">**</ept> resource with the following settings:</source><target>Revenez à la page d’accueil du portail Azure, puis sélectionnez le bouton <bpt id="p1">**</bpt>&amp;#65291;Créer une ressource<ept id="p1">**</ept>, recherchez <bpt id="p2">*</bpt>Compte de stockage<ept id="p2">*</ept>, puis créez une ressource <bpt id="p3">**</bpt>Compte de stockage<ept id="p3">**</ept> avec les paramètres suivants :</target>
        </trans-unit></group></group>
        <group id="p139-PARA"><group id="s139-PARA"><trans-unit id="139" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Subscription<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Your Azure subscription<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Abonnement<ept id="p1">**</ept> : <bpt id="p2">*</bpt>votre abonnement Azure<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p140-PARA"><group id="s140-PARA"><trans-unit id="140" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Resource group<ept id="p1">**</ept>: *<bpt id="p2">*</bpt>The same resource group as your Azure AI Search and Azure AI Services resources<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Groupe de ressources<ept id="p1">**</ept> : <bpt id="p2">*</bpt>identique au groupe de ressources de vos ressources Recherche Azure AI et Azure AI Services<ept id="p2">*</ept>.</target>
        </trans-unit></group></group>
        <group id="p141-PARA"><group id="s141-PARA"><trans-unit id="141" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Storage account name<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Enter a unique name<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Nom du compte de stockage<ept id="p1">**</ept> : <bpt id="p2">*</bpt>entrez un nom unique<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p142-PARA"><group id="s142-PARA"><trans-unit id="142" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Region<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Choose any available region<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Région<ept id="p1">**</ept> : <bpt id="p2">*</bpt>choisissez n’importe quelle région disponible<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p143-PARA"><group id="s143-PARA"><trans-unit id="143" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Performance<ept id="p1">**</ept>: Standard</source><target><bpt id="p1">**</bpt>Performances<ept id="p1">**</ept> : standard</target>
        </trans-unit></group></group>
        <group id="p144-PARA"><group id="s144-PARA"><trans-unit id="144" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Replication<ept id="p1">**</ept>: Locally-redundant storage (LRS)</source><target><bpt id="p1">**</bpt>Réplication<ept id="p1">**</ept> : Stockage localement redondant (LRS)</target>
        </trans-unit></group></group>
        <group id="p145-PARA"><group id="s145-PARA"><trans-unit id="145" translate="yes" xml:space="preserve">
          <source>On the <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> tab, check the box next to <bpt id="p2">*</bpt>Allow enabling anonymous access on individual containers<ept id="p2">*</ept></source><target>Sous l’onglet <bpt id="p1">**</bpt>Avancé<ept id="p1">**</ept>, vérifiez que l’option <bpt id="p2">*</bpt>Autoriser l’activation de l’accès anonyme sur des conteneurs individuels<ept id="p2">*</ept> est cochée.</target>
        </trans-unit></group></group>
        <group id="p146-PARA"><group id="s146-PARA"><trans-unit id="146" translate="yes" xml:space="preserve">
          <source>Wait for deployment to complete, and then go to the deployed resource.</source><target>Attendez la fin du déploiement, puis accédez à la ressource déployée.</target>
        </trans-unit></group></group>
        <group id="p147-PARA"><group id="s147-PARA"><trans-unit id="147" translate="yes" xml:space="preserve">
          <source>On the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page, note the <bpt id="p2">**</bpt>Subscription ID<ept id="p2">**</ept> -this identifies the subscription in which the storage account is provisioned.</source><target>Dans la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept>, notez l’<bpt id="p2">**</bpt>ID d’abonnement<ept id="p2">**</ept> : il identifie l’abonnement dans lequel le compte de stockage est provisionné.</target>
        </trans-unit></group></group>
        <group id="p148-PARA"><group id="s148-PARA"><trans-unit id="148" translate="yes" xml:space="preserve">
          <source>On the <bpt id="p1">**</bpt>Access keys<ept id="p1">**</ept> page, note that two keys have been generated for your storage account.</source><target>Dans la page <bpt id="p1">**</bpt>Clés d’accès<ept id="p1">**</ept>, notez que deux clés ont été générées pour votre compte de stockage.</target>
        </trans-unit></group></group>
        <group id="p149-PARA"><group id="s149-PARA"><trans-unit id="149" translate="yes" xml:space="preserve">
          <source>Then select <bpt id="p1">**</bpt>Show keys<ept id="p1">**</ept> to view the keys.</source><target>Sélectionnez ensuite <bpt id="p1">**</bpt>Afficher les clés<ept id="p1">**</ept> pour afficher les clés.</target>
        </trans-unit></group></group>
        <group id="p150-PARA"><group id="s150-PARA"><trans-unit id="150" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Tip<ept id="p1">**</ept>: Keep the <bpt id="p2">**</bpt>Storage Account<ept id="p2">**</ept> blade open - you will need the subscription ID and one of the keys in the next procedure.</source><target><bpt id="p1">**</bpt>Conseil<ept id="p1">**</ept> : Laissez le panneau <bpt id="p2">**</bpt>Compte de stockage<ept id="p2">**</ept> ouvert. Vous aurez besoin de l’ID d’abonnement et de l’une des clés de la procédure suivante.</target>
        </trans-unit></group></group>
        <group id="p151-PARA"><group id="s151-PARA"><trans-unit id="151" translate="yes" xml:space="preserve">
          <source>Prepare to develop an app in Visual Studio Code</source><target>Préparer le développement d’une application dans Visual Studio Code</target>
        </trans-unit></group></group>
        <group id="p152-PARA"><group id="s152-PARA"><trans-unit id="152" translate="yes" xml:space="preserve">
          <source>You'll develop your search app using Visual Studio Code.</source><target>Vous allez développer votre application de recherche en utilisant Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p153-PARA"><group id="s153-PARA"><trans-unit id="153" translate="yes" xml:space="preserve">
          <source>The code files for your app have been provided in a GitHub repo.</source><target>Les fichiers de code de votre application ont été fournis dans un référentiel GitHub.</target>
        </trans-unit></group></group>
        <group id="p154-PARA"><group id="s154-PARA"><trans-unit id="154" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Tip<ept id="p1">**</ept>: If you have already cloned the <bpt id="p2">**</bpt>mslearn-knowledge-mining<ept id="p2">**</ept> repo, open it in Visual Studio code.</source><target><bpt id="p1">**</bpt>Conseil<ept id="p1">**</ept> : Si vous avez déjà cloné le référentiel <bpt id="p2">**</bpt>mslearn-knowledge-mining<ept id="p2">**</ept>, ouvrez-le dans Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p155-PARA"><group id="s155-PARA"><trans-unit id="155" translate="yes" xml:space="preserve">
          <source>Otherwise, follow these steps to clone it to your development environment.</source><target>Dans le cas contraire, procédez comme suit pour le cloner dans votre environnement de développement.</target>
        </trans-unit></group></group>
        <group id="p156-PARA"><group id="s156-PARA"><trans-unit id="156" translate="yes" xml:space="preserve">
          <source>Start Visual Studio Code.</source><target>Démarrez Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p157-PARA"><group id="s157-PARA"><trans-unit id="157" translate="yes" xml:space="preserve">
          <source>Open the palette (SHIFT+CTRL+P) and run a <bpt id="p1">**</bpt>Git: Clone<ept id="p1">**</ept> command to clone the <ph id="ph1">`https://github.com/MicrosoftLearning/mslearn-knowledge-mining`</ph> repository to a local folder (it doesn't matter which folder).</source><target>Ouvrez la palette (Maj+CTRL+P) et exécutez une commande <bpt id="p1">**</bpt>Git : Cloner<ept id="p1">**</ept> pour cloner le référentiel <ph id="ph1">`https://github.com/MicrosoftLearning/mslearn-knowledge-mining`</ph> vers un dossier local (peu importe quel dossier).</target>
        </trans-unit></group></group>
        <group id="p158-PARA"><group id="s158-PARA"><trans-unit id="158" translate="yes" xml:space="preserve">
          <source>When the repository has been cloned, open the folder in Visual Studio Code.</source><target>Lorsque le référentiel a été cloné, ouvrez le dossier dans Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p159-PARA"><group id="s159-PARA"><trans-unit id="159" translate="yes" xml:space="preserve">
          <source>Wait while additional files are installed to support the C# code projects in the repo.</source><target>Attendez que des fichiers supplémentaires soient installés pour prendre en charge les projets de code C# dans le référentiel.</target>
        </trans-unit></group></group>
        <group id="p160-PARA"><group id="s160-PARA"><trans-unit id="160" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: If you are prompted to add required assets to build and debug, select <bpt id="p2">**</bpt>Not Now<ept id="p2">**</ept>.</source><target><bpt id="p1">**</bpt>Remarque<ept id="p1">**</ept> : si vous êtes invité à ajouter des ressources requises pour générer et déboguer, sélectionnez <bpt id="p2">**</bpt>Not Now<ept id="p2">**</ept> (Pas maintenant).</target>
        </trans-unit></group></group>
        <group id="p161-PARA"><group id="s161-PARA"><trans-unit id="161" translate="yes" xml:space="preserve">
          <source>Upload Documents to Azure Storage</source><target>Charger des documents sur Stockage Azure</target>
        </trans-unit></group></group>
        <group id="p162-PARA"><group id="s162-PARA"><trans-unit id="162" translate="yes" xml:space="preserve">
          <source>Now that you have the required resources, you can upload some documents to your Azure Storage account.</source><target>Maintenant que vous disposez des ressources requises, vous pouvez charger certains documents sur votre compte Stockage Azure.</target>
        </trans-unit></group></group>
        <group id="p163-PARA"><group id="s163-PARA"><trans-unit id="163" translate="yes" xml:space="preserve">
          <source>In Visual Studio Code, in the <bpt id="p1">**</bpt>Explorer<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Labfiles\01-azure-search<ept id="p2">**</ept> folder and select <bpt id="p3">**</bpt>UploadDocs.cmd<ept id="p3">**</ept>.</source><target>Dans Visual Studio Code, dans le volet <bpt id="p1">**</bpt>Explorateur<ept id="p1">**</ept>, développez le dossier <bpt id="p2">**</bpt>Labfiles\01-azure-search<ept id="p2">**</ept>, puis sélectionnez <bpt id="p3">**</bpt>UploadDocs.cmd<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p164-PARA"><group id="s164-PARA"><trans-unit id="164" translate="yes" xml:space="preserve">
          <source>Edit the batch file to replace the <bpt id="p1">**</bpt>YOUR_SUBSCRIPTION_ID<ept id="p1">**</ept>, <bpt id="p2">**</bpt>YOUR_AZURE_STORAGE_ACCOUNT_NAME<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>YOUR_AZURE_STORAGE_KEY<ept id="p3">**</ept> placeholders with the appropriate subscription ID, Azure storage account name, and Azure storage account key values for the storage account you created previously.</source><target>Modifiez le fichier de commandes pour remplacer les espaces réservés <bpt id="p1">**</bpt>YOUR_SUBSCRIPTION_ID<ept id="p1">**</ept>, <bpt id="p2">**</bpt>YOUR_AZURE_STORAGE_ACCOUNT_NAME<ept id="p2">**</ept> et <bpt id="p3">**</bpt>YOUR_AZURE_STORAGE_KEY<ept id="p3">**</ept> avec l'ID d'abonnement, le nom du compte de stockage Azure et les valeurs de clé du compte de stockage Azure appropriés pour le compte de stockage que vous avez créé précédemment.</target>
        </trans-unit></group></group>
        <group id="p165-PARA"><group id="s165-PARA"><trans-unit id="165" translate="yes" xml:space="preserve">
          <source>Save your changes, and then right-click the <bpt id="p1">**</bpt>01-azure-search<ept id="p1">**</ept> folder and open an integrated terminal.</source><target>Enregistrez vos modifications, puis cliquez avec le bouton droit sur le dossier <bpt id="p1">**</bpt>01-azure-search<ept id="p1">**</ept> et ouvrez un terminal intégré.</target>
        </trans-unit></group></group>
        <group id="p166-PARA"><group id="s166-PARA"><trans-unit id="166" translate="yes" xml:space="preserve">
          <source>Enter the following command to sign into your Azure subscription by using the Azure CLI.</source><target>Entrez la commande suivante pour vous connecter à votre abonnement Azure à l’aide d’Azure CLI.</target>
        </trans-unit></group></group>
        <group id="p167-PARA"><group id="s167-PARA"><trans-unit id="167" translate="yes" xml:space="preserve">
          <source>A web browser tab will open and prompt you to sign into Azure.</source><target>Un onglet de navigateur web s’ouvre et vous invite à vous connecter à Azure.</target>
        </trans-unit></group></group>
        <group id="p168-PARA"><group id="s168-PARA"><trans-unit id="168" translate="yes" xml:space="preserve">
          <source>Do so, and then close the browser tab and return to Visual Studio Code.</source><target>Pour ce faire, fermez l’onglet du navigateur et revenez à Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p169-PARA"><group id="s169-PARA"><trans-unit id="169" translate="yes" xml:space="preserve">
          <source>Enter the following command to run the batch file.</source><target>Entrez la commande suivante pour exécuter le fichier de commandes.</target>
        </trans-unit></group></group>
        <group id="p170-PARA"><group id="s170-PARA"><trans-unit id="170" translate="yes" xml:space="preserve">
          <source>This will create a blob container in your storage account and upload the documents in the <bpt id="p1">**</bpt>data<ept id="p1">**</ept> folder to it.</source><target>Cela crée un conteneur d’objets blob dans votre compte de stockage et charge les documents dans le dossier de <bpt id="p1">**</bpt>données<ept id="p1">**</ept> vers celui-ci.</target>
        </trans-unit></group></group>
        <group id="p171-PARA"><group id="s171-PARA"><trans-unit id="171" translate="yes" xml:space="preserve">
          <source>Index the documents</source><target>Indexer les documents</target>
        </trans-unit></group></group>
        <group id="p172-PARA"><group id="s172-PARA"><trans-unit id="172" translate="yes" xml:space="preserve">
          <source>Now that you have the documents in place, you can create a search solution by indexing them.</source><target>Maintenant que vous disposez des documents en place, vous pouvez créer une solution de recherche en les indexant.</target>
        </trans-unit></group></group>
        <group id="p173-PARA"><group id="s173-PARA"><trans-unit id="173" translate="yes" xml:space="preserve">
          <source>In the Azure portal, browse to your Azure AI Search resource.</source><target>Dans le Portail Azure, accédez à votre ressource Recherche Azure AI.</target>
        </trans-unit></group></group>
        <group id="p174-PARA"><group id="s174-PARA"><trans-unit id="174" translate="yes" xml:space="preserve">
          <source>Then, on its <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Import data<ept id="p2">**</ept>.</source><target>Ensuite, dans sa page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept>, sélectionnez <bpt id="p2">**</bpt>Importer des données<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p175-PARA"><group id="s175-PARA"><trans-unit id="175" translate="yes" xml:space="preserve">
          <source>On the <bpt id="p1">**</bpt>Connect to your data<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data Source<ept id="p2">**</ept> list, select <bpt id="p3">**</bpt>Azure Blob Storage<ept id="p3">**</ept>.</source><target>Dans la page <bpt id="p1">**</bpt>Se connecter à vos données<ept id="p1">**</ept>, dans la liste <bpt id="p2">**</bpt>Source de données<ept id="p2">**</ept>, sélectionnez <bpt id="p3">**</bpt>Stockage Blob Azure<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p176-PARA"><group id="s176-PARA"><trans-unit id="176" translate="yes" xml:space="preserve">
          <source>Then complete the data store details with the following values:</source><target>Renseignez ensuite les détails du magasin de données avec les valeurs suivantes :</target>
        </trans-unit></group></group>
        <group id="p177-PARA"><group id="s177-PARA"><trans-unit id="177" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Data Source<ept id="p1">**</ept>: Azure Blob Storage</source><target><bpt id="p1">**</bpt>Source de données<ept id="p1">**</ept> : Stockage Blob Azure</target>
        </trans-unit></group></group>
        <group id="p178-PARA"><group id="s178-PARA"><trans-unit id="178" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Data source name<ept id="p1">**</ept>: margies-data</source><target><bpt id="p1">**</bpt>Nom de la source de données<ept id="p1">**</ept> : margies-data</target>
        </trans-unit></group></group>
        <group id="p179-PARA"><group id="s179-PARA"><trans-unit id="179" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Data to extract<ept id="p1">**</ept>: Content and metadata</source><target><bpt id="p1">**</bpt>Données à extraire<ept id="p1">**</ept> : Contenu et métadonnées</target>
        </trans-unit></group></group>
        <group id="p180-PARA"><group id="s180-PARA"><trans-unit id="180" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Parsing mode<ept id="p1">**</ept>: Default</source><target><bpt id="p1">**</bpt>Mode d’analyse<ept id="p1">**</ept> : Par défaut</target>
        </trans-unit></group></group>
        <group id="p181-PARA"><group id="s181-PARA"><trans-unit id="181" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Connection string<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Select <bpt id="p3">**</bpt>Choose an existing connection<ept id="p3">**</ept>. Then select your storage account, and finally select the <bpt id="p4">**</bpt>margies<ept id="p4">**</ept> container that was created by the UploadDocs.cmd script.<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Chaîne de connexion<ept id="p1">**</ept> : <bpt id="p2">*</bpt>Sélectionnez <bpt id="p3">**</bpt>Choisir une connexion existante<ept id="p3">**</ept>. Sélectionnez ensuite le compte de stockage, puis le conteneur <bpt id="p4">**</bpt>margies<ept id="p4">**</ept> créé par le script UploadDocs.cmd.<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p182-PARA"><group id="s182-PARA"><trans-unit id="182" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Managed identity authentication<ept id="p1">**</ept>: None</source><target><bpt id="p1">**</bpt>Authentification d’identité managée<ept id="p1">**</ept> : Aucun</target>
        </trans-unit></group></group>
        <group id="p183-PARA"><group id="s183-PARA"><trans-unit id="183" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Container name<ept id="p1">**</ept>: margies</source><target><bpt id="p1">**</bpt>Nom du conteneur<ept id="p1">**</ept> : margies</target>
        </trans-unit></group></group>
        <group id="p184-PARA"><group id="s184-PARA"><trans-unit id="184" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Blob folder<ept id="p1">**</ept>: <bpt id="p2">*</bpt>Leave this blank<ept id="p2">*</ept></source><target><bpt id="p1">**</bpt>Dossier d’objets blob<ept id="p1">**</ept> : <bpt id="p2">*</bpt>laissez ce champ vide<ept id="p2">*</ept></target>
        </trans-unit></group></group>
        <group id="p185-PARA"><group id="s185-PARA"><trans-unit id="185" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept>: Brochures and reviews in Margie's Travel web site.</source><target><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> : Brochures et évaluations sur le site web Margie’s Travel.</target>
        </trans-unit></group></group>
        <group id="p186-PARA"><group id="s186-PARA"><trans-unit id="186" translate="yes" xml:space="preserve">
          <source>Proceed to the next step (<bpt id="p1">*</bpt>Add cognitive skills<ept id="p1">*</ept>).</source><target>Passez à l’étape suivante (<bpt id="p1">*</bpt>Ajouter des compétences cognitives<ept id="p1">*</ept>).</target>
        </trans-unit></group></group>
        <group id="p187-PARA"><group id="s187-PARA"><trans-unit id="187" translate="yes" xml:space="preserve">
          <source>in the <bpt id="p1">**</bpt>Attach Azure AI Services<ept id="p1">**</ept> section, select your Azure AI Services resource.</source><target>Dans la section <bpt id="p1">**</bpt>Attacher Azure AI Services<ept id="p1">**</ept>, sélectionnez votre ressource Azure AI Services.</target>
        </trans-unit></group></group>
        <group id="p188-PARA"><group id="s188-PARA"><trans-unit id="188" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>Add enrichments<ept id="p1">**</ept> section:</source><target>Dans la section <bpt id="p1">**</bpt>Ajouter des enrichissements<ept id="p1">**</ept> :</target>
        </trans-unit></group></group>
        <group id="p189-PARA"><group id="s189-PARA"><trans-unit id="189" translate="yes" xml:space="preserve">
          <source>Change the <bpt id="p1">**</bpt>Skillset name<ept id="p1">**</ept> to <bpt id="p2">**</bpt>margies-skillset<ept id="p2">**</ept>.</source><target>Remplacez le <bpt id="p1">**</bpt>Nom de l’ensemble de compétences<ept id="p1">**</ept> par <bpt id="p2">**</bpt>margies-skillset<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p190-PARA"><group id="s190-PARA"><trans-unit id="190" translate="yes" xml:space="preserve">
          <source>Select the option <bpt id="p1">**</bpt>Enable OCR and merge all text into merged_content field<ept id="p1">**</ept>.</source><target>Sélectionnez l’option <bpt id="p1">**</bpt>Activer la reconnaissance optique de caractères et fusionner tout le texte dans le champ merged_content<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p191-PARA"><group id="s191-PARA"><trans-unit id="191" translate="yes" xml:space="preserve">
          <source>Ensure that the <bpt id="p1">**</bpt>Source data field<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>merged_content<ept id="p2">**</ept>.</source><target>Vérifiez que le <bpt id="p1">**</bpt>champ Données sources<ept id="p1">**</ept> est défini sur <bpt id="p2">**</bpt>merged_content<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p192-PARA"><group id="s192-PARA"><trans-unit id="192" translate="yes" xml:space="preserve">
          <source>Leave the <bpt id="p1">**</bpt>Enrichment granularity level<ept id="p1">**</ept> as <bpt id="p2">**</bpt>Source field<ept id="p2">**</ept>, which is set the entire contents of the document being indexed; but note that you can change this to extract information at more granular levels, like pages or sentences.</source><target>Laissez le <bpt id="p1">**</bpt>niveau de granularité de l’enrichissement<ept id="p1">**</ept> comme <bpt id="p2">**</bpt>Champ source<ept id="p2">**</ept>, qui est défini sur l’ensemble des contenus du document indexé. Notez cependant que vous pouvez modifier cette option pour extraire des informations à des niveaux plus précis, tels que des pages ou des phrases.</target>
        </trans-unit></group></group>
        <group id="p193-PARA"><group id="s193-PARA"><trans-unit id="193" translate="yes" xml:space="preserve">
          <source>Select the following enriched fields:</source><target>Sélectionnez les champs enrichis suivants :</target>
        </trans-unit></group></group>
        <group id="p194-PARA"><group id="s194-PARA"><trans-unit id="194" translate="yes" xml:space="preserve">
          <source>Cognitive Skill</source><target>Compétence cognitive</target>
        </trans-unit></group></group>
        <group id="p195-PARA"><group id="s195-PARA"><trans-unit id="195" translate="yes" xml:space="preserve">
          <source>Parameter</source><target>Paramètre</target>
        </trans-unit></group></group>
        <group id="p196-PARA"><group id="s196-PARA"><trans-unit id="196" translate="yes" xml:space="preserve">
          <source>Field name</source><target>Nom du champ</target>
        </trans-unit></group></group>
        <group id="p197-PARA"><group id="s197-PARA"><trans-unit id="197" translate="yes" xml:space="preserve">
          <source>Extract location names</source><target>Extraire les noms d’emplacement</target>
        </trans-unit></group></group>
        <group id="p198-PARA"><group id="s198-PARA"><trans-unit id="198" translate="yes" xml:space="preserve">
          <source>locations</source><target>locations</target>
        </trans-unit></group></group>
        <group id="p199-PARA"><group id="s199-PARA"><trans-unit id="199" translate="yes" xml:space="preserve">
          <source>Extract key phrases</source><target>Extraire les phrases clés</target>
        </trans-unit></group></group>
        <group id="p200-PARA"><group id="s200-PARA"><trans-unit id="200" translate="yes" xml:space="preserve">
          <source>keyphrases</source><target>keyphrases</target>
        </trans-unit></group></group>
        <group id="p201-PARA"><group id="s201-PARA"><trans-unit id="201" translate="yes" xml:space="preserve">
          <source>Detect language</source><target>Détecter la langue</target>
        </trans-unit></group></group>
        <group id="p202-PARA"><group id="s202-PARA"><trans-unit id="202" translate="yes" xml:space="preserve">
          <source>language</source><target>langage</target>
        </trans-unit></group></group>
        <group id="p203-PARA"><group id="s203-PARA"><trans-unit id="203" translate="yes" xml:space="preserve">
          <source>Generate tags from images</source><target>Générer les balises des images</target>
        </trans-unit></group></group>
        <group id="p204-PARA"><group id="s204-PARA"><trans-unit id="204" translate="yes" xml:space="preserve">
          <source>imageTags</source><target>imageTags</target>
        </trans-unit></group></group>
        <group id="p205-PARA"><group id="s205-PARA"><trans-unit id="205" translate="yes" xml:space="preserve">
          <source>Generate captions from images</source><target>Générer les légendes des images</target>
        </trans-unit></group></group>
        <group id="p206-PARA"><group id="s206-PARA"><trans-unit id="206" translate="yes" xml:space="preserve">
          <source>imageCaption</source><target>imageCaption</target>
        </trans-unit></group></group>
        <group id="p207-PARA"><group id="s207-PARA"><trans-unit id="207" translate="yes" xml:space="preserve">
          <source>Double-check your selections (it can be difficult to change them later).</source><target>Vérifiez vos sélections (il peut être difficile de les modifier ultérieurement).</target>
        </trans-unit></group></group>
        <group id="p208-PARA"><group id="s208-PARA"><trans-unit id="208" translate="yes" xml:space="preserve">
          <source>Then proceed to the next step (<bpt id="p1">*</bpt>Customize target index<ept id="p1">*</ept>).</source><target>Passez ensuite à l’étape suivante (<bpt id="p1">*</bpt>Personnaliser l’index cible<ept id="p1">*</ept>).</target>
        </trans-unit></group></group>
        <group id="p209-PARA"><group id="s209-PARA"><trans-unit id="209" translate="yes" xml:space="preserve">
          <source>Change the <bpt id="p1">**</bpt>Index name<ept id="p1">**</ept> to <bpt id="p2">**</bpt>margies-index<ept id="p2">**</ept>.</source><target>Remplacez le <bpt id="p1">**</bpt>nom de l’index<ept id="p1">**</ept> par <bpt id="p2">**</bpt>margies-index<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p210-PARA"><group id="s210-PARA"><trans-unit id="210" translate="yes" xml:space="preserve">
          <source>Ensure that the <bpt id="p1">**</bpt>Key<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept> and leave the <bpt id="p3">**</bpt>Suggester name<ept id="p3">**</ept> blank and <bpt id="p4">**</bpt>Search mode<ept id="p4">**</ept> at its default.</source><target>Vérifiez que la <bpt id="p1">**</bpt>Clé<ept id="p1">**</ept> est définie sur <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept>, et laissez le <bpt id="p3">**</bpt>Nom du suggesteur<ept id="p3">**</ept> vide et le <bpt id="p4">**</bpt>Mode de recherche<ept id="p4">**</ept> par défaut.</target>
        </trans-unit></group></group>
        <group id="p211-PARA"><group id="s211-PARA"><trans-unit id="211" translate="yes" xml:space="preserve">
          <source>Make the following changes to the index fields, leaving all other fields with their default settings (<bpt id="p1">**</bpt>IMPORTANT<ept id="p1">**</ept>: you may need to scroll to the right to see the entire table):</source><target>Apportez les modifications suivantes aux champs d’index, en laissant tous les autres champs avec leurs paramètres par défaut (<bpt id="p1">**</bpt>IMPORTANT<ept id="p1">**</ept> : vous devrez peut-être faire défiler vers la droite pour afficher la table entière) :</target>
        </trans-unit></group></group>
        <group id="p212-PARA"><group id="s212-PARA"><trans-unit id="212" translate="yes" xml:space="preserve">
          <source>Field name</source><target>Nom du champ</target>
        </trans-unit></group></group>
        <group id="p213-PARA"><group id="s213-PARA"><trans-unit id="213" translate="yes" xml:space="preserve">
          <source>Retrievable</source><target>Récupérable</target>
        </trans-unit></group></group>
        <group id="p214-PARA"><group id="s214-PARA"><trans-unit id="214" translate="yes" xml:space="preserve">
          <source>Filterable</source><target>Filtrable</target>
        </trans-unit></group></group>
        <group id="p215-PARA"><group id="s215-PARA"><trans-unit id="215" translate="yes" xml:space="preserve">
          <source>Sortable</source><target>Triable</target>
        </trans-unit></group></group>
        <group id="p216-PARA"><group id="s216-PARA"><trans-unit id="216" translate="yes" xml:space="preserve">
          <source>Facetable</source><target>À choix multiples</target>
        </trans-unit></group></group>
        <group id="p217-PARA"><group id="s217-PARA"><trans-unit id="217" translate="yes" xml:space="preserve">
          <source>Searchable</source><target>Peut faire l’objet d’une recherche</target>
        </trans-unit></group></group>
        <group id="p218-PARA"><group id="s218-PARA"><trans-unit id="218" translate="yes" xml:space="preserve">
          <source>metadata_storage_size</source><target>metadata_storage_size</target>
        </trans-unit></group></group>
        <group id="p219-PARA"><group id="s219-PARA"><trans-unit id="219" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p220-PARA"><group id="s220-PARA"><trans-unit id="220" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p221-PARA"><group id="s221-PARA"><trans-unit id="221" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p222-PARA"><group id="s222-PARA"><trans-unit id="222" translate="yes" xml:space="preserve">
          <source>metadata_storage_last_modified</source><target>metadata_storage_last_modified</target>
        </trans-unit></group></group>
        <group id="p223-PARA"><group id="s223-PARA"><trans-unit id="223" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p224-PARA"><group id="s224-PARA"><trans-unit id="224" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p225-PARA"><group id="s225-PARA"><trans-unit id="225" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p226-PARA"><group id="s226-PARA"><trans-unit id="226" translate="yes" xml:space="preserve">
          <source>metadata_storage_name</source><target>metadata_storage_name</target>
        </trans-unit></group></group>
        <group id="p227-PARA"><group id="s227-PARA"><trans-unit id="227" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p228-PARA"><group id="s228-PARA"><trans-unit id="228" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p229-PARA"><group id="s229-PARA"><trans-unit id="229" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p230-PARA"><group id="s230-PARA"><trans-unit id="230" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p231-PARA"><group id="s231-PARA"><trans-unit id="231" translate="yes" xml:space="preserve">
          <source>metadata_author</source><target>metadata_author</target>
        </trans-unit></group></group>
        <group id="p232-PARA"><group id="s232-PARA"><trans-unit id="232" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p233-PARA"><group id="s233-PARA"><trans-unit id="233" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p234-PARA"><group id="s234-PARA"><trans-unit id="234" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p235-PARA"><group id="s235-PARA"><trans-unit id="235" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p236-PARA"><group id="s236-PARA"><trans-unit id="236" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p237-PARA"><group id="s237-PARA"><trans-unit id="237" translate="yes" xml:space="preserve">
          <source>locations</source><target>locations</target>
        </trans-unit></group></group>
        <group id="p238-PARA"><group id="s238-PARA"><trans-unit id="238" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p239-PARA"><group id="s239-PARA"><trans-unit id="239" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p240-PARA"><group id="s240-PARA"><trans-unit id="240" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p241-PARA"><group id="s241-PARA"><trans-unit id="241" translate="yes" xml:space="preserve">
          <source>keyphrases</source><target>keyphrases</target>
        </trans-unit></group></group>
        <group id="p242-PARA"><group id="s242-PARA"><trans-unit id="242" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p243-PARA"><group id="s243-PARA"><trans-unit id="243" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p244-PARA"><group id="s244-PARA"><trans-unit id="244" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p245-PARA"><group id="s245-PARA"><trans-unit id="245" translate="yes" xml:space="preserve">
          <source>language</source><target>langage</target>
        </trans-unit></group></group>
        <group id="p246-PARA"><group id="s246-PARA"><trans-unit id="246" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p247-PARA"><group id="s247-PARA"><trans-unit id="247" translate="yes" xml:space="preserve">
          <source><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</source><target><ph id="ph1">&amp;nbsp;</ph><ph id="ph2">&amp;nbsp;</ph><ph id="ph3">&amp;nbsp;</ph><ph id="ph4">&amp;nbsp;</ph><ph id="ph5">&amp;nbsp;</ph><ph id="ph6">&amp;nbsp;</ph>&amp;#10004;</target>
        </trans-unit></group></group>
        <group id="p248-PARA"><group id="s248-PARA"><trans-unit id="248" translate="yes" xml:space="preserve">
          <source>Double-check your selections, paying particular attention to ensure that the correct <bpt id="p1">**</bpt>Retrievable<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Filterable<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Sortable<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Facetable<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>Searchable<ept id="p5">**</ept> options are selected for each field  (it can be difficult to change them later).</source><target>Vérifiez vos sélections, en veillant à ce que les options <bpt id="p1">**</bpt>Récupérables<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Filtrables<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Triables<ept id="p3">**</ept>, <bpt id="p4">**</bpt>À choix multiples<ept id="p4">**</ept> et avec une<bpt id="p5">**</bpt>Possibilité de recherche<ept id="p5">**</ept> soient sélectionnées pour chaque champ (il peut être difficile de les modifier ultérieurement).</target>
        </trans-unit></group></group>
        <group id="p249-PARA"><group id="s249-PARA"><trans-unit id="249" translate="yes" xml:space="preserve">
          <source>Then proceed to the next step (<bpt id="p1">*</bpt>Create an indexer<ept id="p1">*</ept>).</source><target>Passez ensuite à l’étape suivante (<bpt id="p1">*</bpt>Créer un indexeur<ept id="p1">*</ept>).</target>
        </trans-unit></group></group>
        <group id="p250-PARA"><group id="s250-PARA"><trans-unit id="250" translate="yes" xml:space="preserve">
          <source>Change the <bpt id="p1">**</bpt>Indexer name<ept id="p1">**</ept> to <bpt id="p2">**</bpt>margies-indexer<ept id="p2">**</ept>.</source><target>Remplacez le <bpt id="p1">**</bpt>Nom de l’index<ept id="p1">**</ept> par <bpt id="p2">**</bpt>margies-index<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p251-PARA"><group id="s251-PARA"><trans-unit id="251" translate="yes" xml:space="preserve">
          <source>Leave the <bpt id="p1">**</bpt>Schedule<ept id="p1">**</ept> set to <bpt id="p2">**</bpt>Once<ept id="p2">**</ept>.</source><target>Laissez la <bpt id="p1">**</bpt>Planification<ept id="p1">**</ept> définie sur <bpt id="p2">**</bpt>Une fois<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p252-PARA"><group id="s252-PARA"><trans-unit id="252" translate="yes" xml:space="preserve">
          <source>Expand the <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> options, and ensure that the <bpt id="p2">**</bpt>Base-64 encode keys<ept id="p2">**</ept> option is selected (generally encoding keys make the index more efficient).</source><target>Développez les options <bpt id="p1">**</bpt>Avancées<ept id="p1">**</ept>, puis vérifiez que l’option <bpt id="p2">**</bpt>Clés d’encodage en base-64<ept id="p2">**</ept> est sélectionnée (en général, les clés d’encodage rendent l’index plus efficace).</target>
        </trans-unit></group></group>
        <group id="p253-PARA"><group id="s253-PARA"><trans-unit id="253" translate="yes" xml:space="preserve">
          <source>Select <bpt id="p1">**</bpt>Submit<ept id="p1">**</ept> to create the data source, skillset, index, and indexer.</source><target>Sélectionnez <bpt id="p1">**</bpt>Envoyer<ept id="p1">**</ept> pour créer la source de données, les compétences, l’index et l’indexeur.</target>
        </trans-unit></group></group>
        <group id="p254-PARA"><group id="s254-PARA"><trans-unit id="254" translate="yes" xml:space="preserve">
          <source>The indexer is run automatically and runs the indexing pipeline, which:</source><target>L’indexeur est exécuté automatiquement et exécute le pipeline d’indexation, qui :</target>
        </trans-unit></group></group>
        <group id="p255-PARA"><group id="s255-PARA"><trans-unit id="255" translate="yes" xml:space="preserve">
          <source>Extracts the document metadata fields and content from the data source</source><target>Extrait les champs de métadonnées des documents et le contenu de la source de données</target>
        </trans-unit></group></group>
        <group id="p256-PARA"><group id="s256-PARA"><trans-unit id="256" translate="yes" xml:space="preserve">
          <source>Runs the skillset of cognitive skills to generate additional enriched fields</source><target>Exécute l’ensemble de compétences de compétences cognitives pour générer des champs enrichis supplémentaires</target>
        </trans-unit></group></group>
        <group id="p257-PARA"><group id="s257-PARA"><trans-unit id="257" translate="yes" xml:space="preserve">
          <source>Maps the extracted fields to the index.</source><target>Mappe les champs extraits à l’index.</target>
        </trans-unit></group></group>
        <group id="p258-PARA"><group id="s258-PARA"><trans-unit id="258" translate="yes" xml:space="preserve">
          <source>In the bottom half of the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page for your Azure AI Search resource, view the <bpt id="p2">**</bpt>Indexers<ept id="p2">**</ept> tab, which should show the newly created <bpt id="p3">**</bpt>margies-indexer<ept id="p3">**</ept>.</source><target>Dans la moitié inférieure de la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> de votre ressource Recherche Azure AI, affichez l’onglet <bpt id="p2">**</bpt>Indexeurs<ept id="p2">**</ept>, qui devrait montrer l’index <bpt id="p3">**</bpt>margies-indexer<ept id="p3">**</ept> nouvellement créé.</target>
        </trans-unit></group></group>
        <group id="p259-PARA"><group id="s259-PARA"><trans-unit id="259" translate="yes" xml:space="preserve">
          <source>Wait a few minutes, and click <bpt id="p1">**</bpt><ph id="ph1">&amp;orarr;</ph> Refresh<ept id="p1">**</ept> until the <bpt id="p2">**</bpt>Status<ept id="p2">**</ept> indicates success.</source><target>Attendez quelques minutes, puis cliquez sur <bpt id="p1">**</bpt><ph id="ph1">&amp;orarr;</ph> Actualiser<ept id="p1">**</ept> jusqu’à ce que l’<bpt id="p2">**</bpt>État<ept id="p2">**</ept> indique la réussite.</target>
        </trans-unit></group></group>
        <group id="p260-PARA"><group id="s260-PARA"><trans-unit id="260" translate="yes" xml:space="preserve">
          <source>Search the index</source><target>Rechercher l’index</target>
        </trans-unit></group></group>
        <group id="p261-PARA"><group id="s261-PARA"><trans-unit id="261" translate="yes" xml:space="preserve">
          <source>Now that you have an index, you can search it.</source><target>Maintenant que vous avez un index, vous pouvez y effectuer des recherches.</target>
        </trans-unit></group></group>
        <group id="p262-PARA"><group id="s262-PARA"><trans-unit id="262" translate="yes" xml:space="preserve">
          <source>At the top of the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page for your Azure AI Search resource, select <bpt id="p2">**</bpt>Search explorer<ept id="p2">**</ept>.</source><target>En haut de la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> de votre ressource Recherche Azure AI, sélectionnez <bpt id="p2">**</bpt>Explorateur de recherche<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p263-PARA"><group id="s263-PARA"><trans-unit id="263" translate="yes" xml:space="preserve">
          <source>In Search explorer, in the <bpt id="p1">**</bpt>Query string<ept id="p1">**</ept> box, enter <ph id="ph1">`*`</ph> (a single asterisk), and then select <bpt id="p2">**</bpt>Search<ept id="p2">**</ept>.</source><target>Dans l’Explorateur de recherche, dans la zone <bpt id="p1">**</bpt>Chaîne de requête<ept id="p1">**</ept>, entrez <ph id="ph1">`*`</ph> (un astérisque unique), puis sélectionnez <bpt id="p2">**</bpt>Rechercher<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p264-PARA"><group id="s264-PARA"><trans-unit id="264" translate="yes" xml:space="preserve">
          <source>This query retrieves all documents in the index in JSON format.</source><target>Cette requête extrait tous les documents dans l’index au format JSON.</target>
        </trans-unit></group></group>
        <group id="p265-PARA"><group id="s265-PARA"><trans-unit id="265" translate="yes" xml:space="preserve">
          <source>Examine the results and note the fields for each document, which contain document content, metadata, and enriched data extracted by the cognitive skills you selected.</source><target>Examinez les résultats et notez les champs de chaque document, qui contiennent du contenu, des métadonnées et des données enrichies extraites par les compétences cognitives que vous avez sélectionnées.</target>
        </trans-unit></group></group>
        <group id="p266-PARA"><group id="s266-PARA"><trans-unit id="266" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>View<ept id="p1">**</ept> menu, select <bpt id="p2">**</bpt>JSON view<ept id="p2">**</ept> and note that the JSON request for the search is shown, like this:</source><target>Dans le menu <bpt id="p1">**</bpt>Affichage<ept id="p1">**</ept> , sélectionnez <bpt id="p2">**</bpt>Affichage SJON<ept id="p2">**</ept> et vérifiez que la requête JSON pour la recherche est affichée, comme ici :</target>
        </trans-unit></group></group>
        <group id="p267-PARA"><group id="s267-PARA"><trans-unit id="267" translate="yes" xml:space="preserve">
          <source>Modify the JSON request to include the <bpt id="p1">**</bpt>count<ept id="p1">**</ept> parameter as shown here:</source><target>Modifiez la requête JSON pour inclure le paramètre <bpt id="p1">**</bpt>count<ept id="p1">**</ept> comme indiqué ici :</target>
        </trans-unit></group></group>
        <group id="p268-PARA"><group id="s268-PARA"><trans-unit id="268" translate="yes" xml:space="preserve">
          <source>Submit the modified search.</source><target>Envoyez la recherche modifiée.</target>
        </trans-unit></group></group>
        <group id="p269-PARA"><group id="s269-PARA"><trans-unit id="269" translate="yes" xml:space="preserve">
          <source>This time, the results include a <bpt id="p1">**</bpt><ph id="ph1">@odata.count</ph><ept id="p1">**</ept> field at the top of the results that indicates the number of documents returned by the search.</source><target>Cette fois, les résultats incluent un champ <bpt id="p1">**</bpt><ph id="ph1">@odata.count</ph><ept id="p1">**</ept> en haut des résultats qui indique le nombre de documents retournés par la recherche.</target>
        </trans-unit></group></group>
        <group id="p270-PARA"><group id="s270-PARA"><trans-unit id="270" translate="yes" xml:space="preserve">
          <source>Try the following query:</source><target>Essayez la requête suivante :</target>
        </trans-unit></group></group>
        <group id="p271-PARA"><group id="s271-PARA"><trans-unit id="271" translate="yes" xml:space="preserve">
          <source>This time the results include only the file name, author, and any locations mentioned in the document content.</source><target>Cette fois, les résultats incluent uniquement le nom de fichier, l’auteur et tous les emplacements mentionnés dans le contenu du document.</target>
        </trans-unit></group></group>
        <group id="p272-PARA"><group id="s272-PARA"><trans-unit id="272" translate="yes" xml:space="preserve">
          <source>The file name and author are in the <bpt id="p1">**</bpt>metadata_storage_name<ept id="p1">**</ept> and <bpt id="p2">**</bpt>metadata_author<ept id="p2">**</ept> fields, which were extracted from the source document.</source><target>Le nom de fichier et l’auteur se trouvent dans les champs <bpt id="p1">**</bpt>metadata_storage_name<ept id="p1">**</ept> et <bpt id="p2">**</bpt>metadata_author<ept id="p2">**</ept>, qui ont été extraits du document source.</target>
        </trans-unit></group></group>
        <group id="p273-PARA"><group id="s273-PARA"><trans-unit id="273" translate="yes" xml:space="preserve">
          <source>The <bpt id="p1">**</bpt>locations<ept id="p1">**</ept> field was generated by a cognitive skill.</source><target>Le champ <bpt id="p1">**</bpt>emplacements<ept id="p1">**</ept> a été généré par une compétence cognitive.</target>
        </trans-unit></group></group>
        <group id="p274-PARA"><group id="s274-PARA"><trans-unit id="274" translate="yes" xml:space="preserve">
          <source>Now try the following query string:</source><target>Essayez la chaîne de requête suivante :</target>
        </trans-unit></group></group>
        <group id="p275-PARA"><group id="s275-PARA"><trans-unit id="275" translate="yes" xml:space="preserve">
          <source>This search finds documents that mention "New York" in any of the searchable fields, and returns the file name and key phrases in the document.</source><target>Cette recherche recherche des documents qui mentionnent « New York » dans l’un des champs pouvant faire l’objet d’une recherche et retourne le nom de fichier et les expressions clés du document.</target>
        </trans-unit></group></group>
        <group id="p276-PARA"><group id="s276-PARA"><trans-unit id="276" translate="yes" xml:space="preserve">
          <source>Let's try one more query:</source><target>Essayons une de requête supplémentaire :</target>
        </trans-unit></group></group>
        <group id="p277-PARA"><group id="s277-PARA"><trans-unit id="277" translate="yes" xml:space="preserve">
          <source>This query returns the filename of any documents authored by <bpt id="p1">*</bpt>Reviewer<ept id="p1">*</ept> that mention "New York".</source><target>Cette requête retourne le nom de fichier des documents créés par le <bpt id="p1">*</bpt>Réviseur<ept id="p1">*</ept> qui mentionnent « New York ».</target>
        </trans-unit></group></group>
        <group id="p278-PARA"><group id="s278-PARA"><trans-unit id="278" translate="yes" xml:space="preserve">
          <source>Explore and modify definitions of search components</source><target>Explorer et modifier les définitions des composants de recherche</target>
        </trans-unit></group></group>
        <group id="p279-PARA"><group id="s279-PARA"><trans-unit id="279" translate="yes" xml:space="preserve">
          <source>The components of the search solution are based on JSON definitions, which you can view and edit in the Azure portal.</source><target>Les composants de la solution de recherche sont basés sur des définitions JSON que vous pouvez afficher et modifier dans le portail Azure.</target>
        </trans-unit></group></group>
        <group id="p280-PARA"><group id="s280-PARA"><trans-unit id="280" translate="yes" xml:space="preserve">
          <source>While you can use the portal to create and modify search solutions, it's often desirable to define the search objects in JSON and use the Azure AI Service REST interface to create and modify them.</source><target>Bien que vous puissiez utiliser le portail pour créer et modifier des solutions de recherche, il est souvent souhaitable de définir les objets de recherche au format JSON et d’utiliser l’interface REST d’Azure AI Services pour les créer et les modifier.</target>
        </trans-unit></group></group>
        <group id="p281-PARA"><group id="s281-PARA"><trans-unit id="281" translate="yes" xml:space="preserve">
          <source>Get the endpoint and key for your Azure AI Search resource</source><target>Obtenir le point de terminaison et la clé de votre ressource Recherche Azure AI</target>
        </trans-unit></group></group>
        <group id="p282-PARA"><group id="s282-PARA"><trans-unit id="282" translate="yes" xml:space="preserve">
          <source>In the Azure portal, return to the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page for your Azure AI Search resource; and in the top section of the page, find the <bpt id="p2">**</bpt>Url<ept id="p2">**</ept> for your resource (which looks like <bpt id="p3">**</bpt><ph id="ph1">https://resource_name.search.windows.net</ph><ept id="p3">**</ept>) and copy it to the clipboard.</source><target>Dans le Portail Azure, revenez à la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> de votre ressource Recherche Azure AI. Puis, dans la section supérieure de la page, recherchez l’<bpt id="p2">**</bpt>URL<ept id="p2">**</ept> de votre ressource (qui ressemble à <bpt id="p3">**</bpt><ph id="ph1">https://resource_name.search.windows.net</ph><ept id="p3">**</ept>) et copiez-la dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p283-PARA"><group id="s283-PARA"><trans-unit id="283" translate="yes" xml:space="preserve">
          <source>In Visual Studio Code, in the Explorer pane, expand the <bpt id="p1">**</bpt>01-azure-search<ept id="p1">**</ept> folder and its <bpt id="p2">**</bpt>modify-search<ept id="p2">**</ept> subfolder, and select <bpt id="p3">**</bpt>modify-search.cmd<ept id="p3">**</ept> to open it.</source><target>Dans Visual Studio Code, dans le volet Explorateur, développez le dossier <bpt id="p1">**</bpt>01-azure-search<ept id="p1">**</ept> et son sous-dossier <bpt id="p2">**</bpt>modify-search<ept id="p2">**</ept>, puis sélectionnez <bpt id="p3">**</bpt>modify-search.cmd<ept id="p3">**</ept> pour l’ouvrir.</target>
        </trans-unit></group></group>
        <group id="p284-PARA"><group id="s284-PARA"><trans-unit id="284" translate="yes" xml:space="preserve">
          <source>You will use this script file to run <bpt id="p1">*</bpt>cURL<ept id="p1">*</ept> commands that submit JSON to the Azure AI Service REST interface.</source><target>Vous allez utiliser ce fichier de script pour exécuter des commandes <bpt id="p1">*</bpt>cURL<ept id="p1">*</ept> qui envoient JSON à l’interface REST d’Azure AI Services.</target>
        </trans-unit></group></group>
        <group id="p285-PARA"><group id="s285-PARA"><trans-unit id="285" translate="yes" xml:space="preserve">
          <source>In <bpt id="p1">**</bpt>modify-search.cmd<ept id="p1">**</ept>, replace the <bpt id="p2">**</bpt>YOUR_SEARCH_URL<ept id="p2">**</ept> placeholder with the URL you copied to the clipboard.</source><target>Dans <bpt id="p1">**</bpt>modify-search.cmd<ept id="p1">**</ept>, remplacez l’espace réservé <bpt id="p2">**</bpt>YOUR_SEARCH_URL<ept id="p2">**</ept> par l’URL que vous avez copiée dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p286-PARA"><group id="s286-PARA"><trans-unit id="286" translate="yes" xml:space="preserve">
          <source>In the Azure portal, view the <bpt id="p1">**</bpt>Keys<ept id="p1">**</ept> page for your Azure AI Search resource, and copy the <bpt id="p2">**</bpt>Primary admin key<ept id="p2">**</ept> to the clipboard.</source><target>Dans le Portail Azure, affichez la page <bpt id="p1">**</bpt>Clés<ept id="p1">**</ept> de votre ressource Recherche Azure AI et copiez la <bpt id="p2">**</bpt>Clé d’administration principale<ept id="p2">**</ept> dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p287-PARA"><group id="s287-PARA"><trans-unit id="287" translate="yes" xml:space="preserve">
          <source>In Visual Studio Code, replace the <bpt id="p1">**</bpt>YOUR_ADMIN_KEY<ept id="p1">**</ept> placeholder with the key you copied to the clipboard.</source><target>Dans Visual Studio Code, remplacez l’espace réservé <bpt id="p1">**</bpt>YOUR_ADMIN_KEY<ept id="p1">**</ept> par la clé que vous avez copiée dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p288-PARA"><group id="s288-PARA"><trans-unit id="288" translate="yes" xml:space="preserve">
          <source>Save the changes to <bpt id="p1">**</bpt>modify-search.cmd<ept id="p1">**</ept> (but don't run it yet!)</source><target>Enregistrez les modifications apportées à <bpt id="p1">**</bpt>modify-search.cmd<ept id="p1">**</ept> (mais ne l’exécutez pas encore !)</target>
        </trans-unit></group></group>
        <group id="p289-PARA"><group id="s289-PARA"><trans-unit id="289" translate="yes" xml:space="preserve">
          <source>Review and modify the skillset</source><target>Passer en revue et modifier l’ensemble de compétences</target>
        </trans-unit></group></group>
        <group id="p290-PARA"><group id="s290-PARA"><trans-unit id="290" translate="yes" xml:space="preserve">
          <source>In Visual studio Code, in the <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> folder, open <bpt id="p2">**</bpt>skillset.json<ept id="p2">**</ept>.</source><target>Dans Visual Studio Code, dans le dossier <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept>, ouvrez <bpt id="p2">**</bpt>skillset.json<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p291-PARA"><group id="s291-PARA"><trans-unit id="291" translate="yes" xml:space="preserve">
          <source>This shows a JSON definition for <bpt id="p1">**</bpt>margies-skillset<ept id="p1">**</ept>.</source><target>Cela montre une définition JSON pour <bpt id="p1">**</bpt>margies-skillset<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p292-PARA"><group id="s292-PARA"><trans-unit id="292" translate="yes" xml:space="preserve">
          <source>At the top of the skillset definition, note the <bpt id="p1">**</bpt>cognitiveServices<ept id="p1">**</ept> object, which is used to connect your Azure AI Services resource to the skillset.</source><target>En haut de la définition de l’ensemble de compétences, notez l’objet <bpt id="p1">**</bpt>cognitiveServices<ept id="p1">**</ept> qui est utilisé pour connecter votre ressource Azure AI Services à l’ensemble de compétences.</target>
        </trans-unit></group></group>
        <group id="p293-PARA"><group id="s293-PARA"><trans-unit id="293" translate="yes" xml:space="preserve">
          <source>In the Azure portal, open your Azure AI Services resource (<bpt id="p1">&lt;u&gt;</bpt>not<ept id="p1">&lt;/u&gt;</ept> your Azure AI Search resource!) and view its <bpt id="p2">**</bpt>Keys<ept id="p2">**</ept> page.</source><target>Dans le Portail Azure, ouvrez votre ressource Azure AI Services (<bpt id="p1">&lt;u&gt;</bpt>pas<ept id="p1">&lt;/u&gt;</ept> votre ressource Recherche Azure AI !) et affichez sa page <bpt id="p2">**</bpt>Clés<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p294-PARA"><group id="s294-PARA"><trans-unit id="294" translate="yes" xml:space="preserve">
          <source>Then copy <bpt id="p1">**</bpt>Key 1<ept id="p1">**</ept> to the clipboard.</source><target>Copiez ensuite la <bpt id="p1">**</bpt>Clé 1<ept id="p1">**</ept> dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p295-PARA"><group id="s295-PARA"><trans-unit id="295" translate="yes" xml:space="preserve">
          <source>In Visual Studio Code, in <bpt id="p1">**</bpt>skillset.json<ept id="p1">**</ept>, replace the <bpt id="p2">**</bpt>YOUR_COGNITIVE_SERVICES_KEY<ept id="p2">**</ept> placeholder with the Azure AI Services key you copied to the clipboard.</source><target>Dans Visual Studio Code, dans <bpt id="p1">**</bpt>skillset.json<ept id="p1">**</ept>, remplacez l’espace réservé <bpt id="p2">**</bpt>YOUR_COGNITIVE_SERVICES_KEY<ept id="p2">**</ept> par la clé Azure AI Services que vous avez copiée dans le presse-papiers.</target>
        </trans-unit></group></group>
        <group id="p296-PARA"><group id="s296-PARA"><trans-unit id="296" translate="yes" xml:space="preserve">
          <source>Scroll through the JSON file, noting that it includes definitions for the skills you created using the Azure AI Search user interface in the Azure portal.</source><target>Faites défiler le fichier JSON en notant qu’il inclut des définitions pour les compétences que vous avez créées à l’aide de l’interface utilisateur de Recherche Azure AI dans le Portail Azure.</target>
        </trans-unit></group></group>
        <group id="p297-PARA"><group id="s297-PARA"><trans-unit id="297" translate="yes" xml:space="preserve">
          <source>At the bottom of the list of skills, an additional skill has been added with the following definition:</source><target>En bas de la liste des compétences, une compétence supplémentaire a été ajoutée avec la définition suivante :</target>
        </trans-unit></group></group>
        <group id="p298-PARA"><group id="s298-PARA"><trans-unit id="298" translate="yes" xml:space="preserve">
          <source>The new skill is named <bpt id="p1">**</bpt>get-sentiment<ept id="p1">**</ept>, and for each <bpt id="p2">**</bpt>document<ept id="p2">**</ept> level in a document, it, will evaluate the text found in the <bpt id="p3">**</bpt>merged_content<ept id="p3">**</ept> field of the document being indexed (which includes the source content as well as any text extracted from images in the content).</source><target>La nouvelle compétence est nommée <bpt id="p1">**</bpt>get-sentiment<ept id="p1">**</ept> et, pour chaque niveau de <bpt id="p2">**</bpt>document<ept id="p2">**</ept> d’un document, elle évalue le texte trouvé dans le champ <bpt id="p3">**</bpt>merged_content<ept id="p3">**</ept> du document indexé (qui inclut le contenu source ainsi que tout texte extrait d’images dans le contenu).</target>
        </trans-unit></group></group>
        <group id="p299-PARA"><group id="s299-PARA"><trans-unit id="299" translate="yes" xml:space="preserve">
          <source>It uses the extracted <bpt id="p1">**</bpt>language<ept id="p1">**</ept> of the document (with a default of English), and evaluates a label for the sentiment of the content.</source><target>Il utilise la <bpt id="p1">**</bpt>langue<ept id="p1">**</ept> extraite du document (avec une valeur par défaut anglais) et évalue une étiquette pour le sentiment du contenu.</target>
        </trans-unit></group></group>
        <group id="p300-PARA"><group id="s300-PARA"><trans-unit id="300" translate="yes" xml:space="preserve">
          <source>Values for the sentiment label can be "positive", "negative", "neutral", or "mixed".</source><target>Les valeurs de l’étiquette de sentiment peuvent être « positives », « négatives », « neutres » ou « mixtes ».</target>
        </trans-unit></group></group>
        <group id="p301-PARA"><group id="s301-PARA"><trans-unit id="301" translate="yes" xml:space="preserve">
          <source>This label is then output as a new field named <bpt id="p1">**</bpt>sentimentLabel<ept id="p1">**</ept>.</source><target>Cette étiquette est ensuite générée sous la forme d’un nouveau champ nommé <bpt id="p1">**</bpt>sentimentLabel<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p302-PARA"><group id="s302-PARA"><trans-unit id="302" translate="yes" xml:space="preserve">
          <source>Save the changes you've made to <bpt id="p1">**</bpt>skillset.json<ept id="p1">**</ept>.</source><target>Enregistrez les modifications que vous avez apportées à <bpt id="p1">**</bpt>skillset.json<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p303-PARA"><group id="s303-PARA"><trans-unit id="303" translate="yes" xml:space="preserve">
          <source>Review and modify the index</source><target>Passer en revue et modifier l’index</target>
        </trans-unit></group></group>
        <group id="p304-PARA"><group id="s304-PARA"><trans-unit id="304" translate="yes" xml:space="preserve">
          <source>In Visual studio Code, in the <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> folder, open <bpt id="p2">**</bpt>index.json<ept id="p2">**</ept>.</source><target>Dans Visual Studio Code, dans le dossier <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept>, ouvrez <bpt id="p2">**</bpt>index.json<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p305-PARA"><group id="s305-PARA"><trans-unit id="305" translate="yes" xml:space="preserve">
          <source>This shows a JSON definition for <bpt id="p1">**</bpt>margies-index<ept id="p1">**</ept>.</source><target>Cela montre une définition JSON pour <bpt id="p1">**</bpt>margies-index<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p306-PARA"><group id="s306-PARA"><trans-unit id="306" translate="yes" xml:space="preserve">
          <source>Scroll through the index and view the field definitions.</source><target>Faites défiler l’index et affichez les définitions de champ.</target>
        </trans-unit></group></group>
        <group id="p307-PARA"><group id="s307-PARA"><trans-unit id="307" translate="yes" xml:space="preserve">
          <source>Some fields are based on metadata and content in the source document, and others are the results of skills in the skillset.</source><target>Certains champs sont basés sur les métadonnées et le contenu dans le document source, et d’autres sont les résultats des compétences dans l’ensemble de compétences.</target>
        </trans-unit></group></group>
        <group id="p308-PARA"><group id="s308-PARA"><trans-unit id="308" translate="yes" xml:space="preserve">
          <source>At the end of the list of fields that you defined in the Azure portal, note that two additional fields have been added:</source><target>À la fin de la liste des champs que vous avez définis dans le portail Azure, notez que deux champs supplémentaires ont été ajoutés :</target>
        </trans-unit></group></group>
        <group id="p309-PARA"><group id="s309-PARA"><trans-unit id="309" translate="yes" xml:space="preserve">
          <source>The <bpt id="p1">**</bpt>sentiment<ept id="p1">**</ept> field will be used to add the output from the <bpt id="p2">**</bpt>get-sentiment<ept id="p2">**</ept> skill that was added the skillset.</source><target>Le champ <bpt id="p1">**</bpt>sentiment<ept id="p1">**</ept> sera utilisé pour ajouter la sortie de la compétence <bpt id="p2">**</bpt>get-sentiment<ept id="p2">**</ept> qui a été ajoutée à l’ensemble de compétences.</target>
        </trans-unit></group></group>
        <group id="p310-PARA"><group id="s310-PARA"><trans-unit id="310" translate="yes" xml:space="preserve">
          <source>The <bpt id="p1">**</bpt>url<ept id="p1">**</ept> field will be used to add the URL for each indexed document to the index, based on the <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept> value extracted from the data source.</source><target>Le champ <bpt id="p1">**</bpt>url<ept id="p1">**</ept> sera utilisé pour ajouter l’URL de chaque document indexé à l’index, en fonction de la valeur <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept> extraite de la source de données.</target>
        </trans-unit></group></group>
        <group id="p311-PARA"><group id="s311-PARA"><trans-unit id="311" translate="yes" xml:space="preserve">
          <source>Note that index already includes the <bpt id="p1">**</bpt>metadata_storage_path<ept id="p1">**</ept> field, but it's used as the index key and Base-64 encoded, making it efficient as a key but requiring client applications to decode it if they want to use the actual URL value as a field.</source><target>Notez que l’index inclut déjà le champ <bpt id="p1">**</bpt>metadata_storage_path<ept id="p1">**</ept> , mais qu’il est utilisé comme clé d’index et codé en base 64, ce qui le rend efficace en tant que clé, mais que les applications clientes doivent le décoder s’ils souhaitent utiliser la valeur d’URL réelle en tant que champ.</target>
        </trans-unit></group></group>
        <group id="p312-PARA"><group id="s312-PARA"><trans-unit id="312" translate="yes" xml:space="preserve">
          <source>Adding a second field for the unencoded value resolves this problem.</source><target>L’ajout d’un deuxième champ pour la valeur non codée résout ce problème.</target>
        </trans-unit></group></group>
        <group id="p313-PARA"><group id="s313-PARA"><trans-unit id="313" translate="yes" xml:space="preserve">
          <source>Review and modify the indexer</source><target>Passer en revue et modifier l’indexeur</target>
        </trans-unit></group></group>
        <group id="p314-PARA"><group id="s314-PARA"><trans-unit id="314" translate="yes" xml:space="preserve">
          <source>In Visual studio Code, in the <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> folder, open <bpt id="p2">**</bpt>indexer.json<ept id="p2">**</ept>.</source><target>Dans Visual Studio Code, dans le dossier <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept>, ouvrez <bpt id="p2">**</bpt>indexer.json<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p315-PARA"><group id="s315-PARA"><trans-unit id="315" translate="yes" xml:space="preserve">
          <source>This shows a JSON definition for <bpt id="p1">**</bpt>margies-indexer<ept id="p1">**</ept>, which maps fields extracted from document content and metadata (in the <bpt id="p2">**</bpt>fieldMappings<ept id="p2">**</ept> section), and values extracted by skills in the skillset (in the <bpt id="p3">**</bpt>outputFieldMappings<ept id="p3">**</ept> section), to fields in the index.</source><target>Cela montre une définition JSON pour <bpt id="p1">**</bpt>margies-indexer<ept id="p1">**</ept>, qui mappe les champs extraits du contenu et des métadonnées du document (dans la section <bpt id="p2">**</bpt>fieldMappings<ept id="p2">**</ept>) et les valeurs extraites par les compétences de l’ensemble de compétences (dans la section <bpt id="p3">**</bpt>outputFieldMappings<ept id="p3">**</ept> ), aux champs dans l’index.</target>
        </trans-unit></group></group>
        <group id="p316-PARA"><group id="s316-PARA"><trans-unit id="316" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>fieldMappings<ept id="p1">**</ept> list, note the mapping for the <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept> value to the base-64 encoded key field.</source><target>Dans la liste <bpt id="p1">**</bpt>fieldMappings<ept id="p1">**</ept>, notez le mappage de la valeur <bpt id="p2">**</bpt>metadata_storage_path<ept id="p2">**</ept> au champ clé codé en base 64.</target>
        </trans-unit></group></group>
        <group id="p317-PARA"><group id="s317-PARA"><trans-unit id="317" translate="yes" xml:space="preserve">
          <source>This was created when you assigned the <bpt id="p1">**</bpt>metadata_storage_path<ept id="p1">**</ept> as the key and selected the option to encode the key in the Azure portal.</source><target>Cela a été créé lorsque vous avez affecté le <bpt id="p1">**</bpt>metadata_storage_path<ept id="p1">**</ept> en tant que clé et sélectionné l’option pour encoder la clé dans le portail Azure.</target>
        </trans-unit></group></group>
        <group id="p318-PARA"><group id="s318-PARA"><trans-unit id="318" translate="yes" xml:space="preserve">
          <source>Additionally, a new mapping explicitly maps the same value to the <bpt id="p1">**</bpt>url<ept id="p1">**</ept> field, but without the Base-64 encoding:</source><target>En outre, un nouveau mappage mappe explicitement la même valeur au champ <bpt id="p1">**</bpt>url<ept id="p1">**</ept>, mais sans le codage en base 64 :</target>
        </trans-unit></group></group>
        <group id="p319-PARA"><group id="s319-PARA"><trans-unit id="319" translate="yes" xml:space="preserve">
          <source>All of the other metadata and content fields in the source document are implicitly mapped to fields of the same name in the index.</source><target>Tous les autres champs de métadonnées et de contenu du document source sont implicitement mappés aux champs du même nom dans l’index.</target>
        </trans-unit></group></group>
        <group id="p320-PARA"><group id="s320-PARA"><trans-unit id="320" translate="yes" xml:space="preserve">
          <source>Review the <bpt id="p1">**</bpt>ouputFieldMappings<ept id="p1">**</ept> section, which maps outputs from the skills in the skillset to index fields.</source><target>Passez en revue la section <bpt id="p1">**</bpt>ouputFieldMappings<ept id="p1">**</ept>, qui mappe les sorties des compétences de l’ensemble de compétences aux champs d’index.</target>
        </trans-unit></group></group>
        <group id="p321-PARA"><group id="s321-PARA"><trans-unit id="321" translate="yes" xml:space="preserve">
          <source>Most of these reflect the choices you made in the user interface, but the following mapping has been added to map the <bpt id="p1">**</bpt>sentimentLabel<ept id="p1">**</ept> value extracted by your sentiment skill to the <bpt id="p2">**</bpt>sentiment<ept id="p2">**</ept> field you added to the index:</source><target>La plupart de ces choix reflètent les choix que vous avez effectués dans l’interface utilisateur, mais le mappage suivant a été ajouté pour mapper la valeur <bpt id="p1">**</bpt>sentimentLabel<ept id="p1">**</ept> extraite par votre compétence de sentiment au champ de <bpt id="p2">**</bpt>sentiment<ept id="p2">**</ept> que vous avez ajouté à l’index :</target>
        </trans-unit></group></group>
        <group id="p322-PARA"><group id="s322-PARA"><trans-unit id="322" translate="yes" xml:space="preserve">
          <source>Use the REST API to update the search solution</source><target>Utiliser l’API REST pour mettre à jour la solution de recherche</target>
        </trans-unit></group></group>
        <group id="p323-PARA"><group id="s323-PARA"><trans-unit id="323" translate="yes" xml:space="preserve">
          <source>Right-click the <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> folder and open an integrated terminal.</source><target>Cliquez avec le bouton droit de la souris sur le dossier <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> et ouvrez un terminal intégré.</target>
        </trans-unit></group></group>
        <group id="p324-PARA"><group id="s324-PARA"><trans-unit id="324" translate="yes" xml:space="preserve">
          <source>In the terminal pane for the <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept> folder, enter the following command to run the <bpt id="p2">**</bpt>modify-search.cmd<ept id="p2">**</ept> script, which submits the JSON definitions to the REST interface and initiates the indexing.</source><target>Dans le volet terminal du dossier <bpt id="p1">**</bpt>modify-search<ept id="p1">**</ept>, entrez la commande suivante pour exécuter le script <bpt id="p2">**</bpt>modify-search.cmd<ept id="p2">**</ept>, qui soumet les définitions JSON à l’interface REST et lance l’indexation.</target>
        </trans-unit></group></group>
        <group id="p325-PARA"><group id="s325-PARA"><trans-unit id="325" translate="yes" xml:space="preserve">
          <source>When the script has finished, return to the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page for your Azure AI Search resource in the Azure portal and view the <bpt id="p2">**</bpt>Indexers<ept id="p2">**</ept> page.</source><target>Une fois le script terminé, revenez à la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> de votre ressource Recherche Azure AI dans le Portail Azure et affichez la page <bpt id="p2">**</bpt>Indexeurs<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p326-PARA"><group id="s326-PARA"><trans-unit id="326" translate="yes" xml:space="preserve">
          <source>The periodically select <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> to track the progress of the indexing operation.</source><target>Sélectionnez <bpt id="p1">**</bpt>Actualiser<ept id="p1">**</ept> régulièrement pour suivre la progression de l’opération d’indexation.</target>
        </trans-unit></group></group>
        <group id="p327-PARA"><group id="s327-PARA"><trans-unit id="327" translate="yes" xml:space="preserve">
          <source>It may take a minute or so to complete.</source><target>Cette opération peut prendre environ une minute.</target>
        </trans-unit></group></group>
        <group id="p328-PARA"><group id="s328-PARA"><trans-unit id="328" translate="yes" xml:space="preserve">
          <source><bpt id="p1">*</bpt>There may be some warnings for a few documents that are too large to evaluate sentiment. Often sentiment analysis is performed at the page or sentence level rather than the full document; but in this case scenario, most of the documents - particularly the hotel reviews, are short enough for useful document-level sentiment scores to be evaluated.<ept id="p1">*</ept></source><target><bpt id="p1">*</bpt>Il peut y avoir quelques avertissements pour quelques documents qui sont trop grands pour évaluer le sentiment. Souvent, l'analyse des sentiments est effectuée au niveau de la page ou de la phrase plutôt qu'au niveau du document complet ; mais dans ce scénario, la plupart des documents, en particulier les critiques d'hôtels, sont suffisamment courts pour que des scores de sentiments utiles au niveau du document puissent être évalués.<ept id="p1">*</ept></target>
        </trans-unit></group></group>
        <group id="p329-PARA"><group id="s329-PARA"><trans-unit id="329" translate="yes" xml:space="preserve">
          <source>Query the modified index</source><target>Interroger l’index modifié</target>
        </trans-unit></group></group>
        <group id="p330-PARA"><group id="s330-PARA"><trans-unit id="330" translate="yes" xml:space="preserve">
          <source>At the top of the blade for your Azure AI Search resource, select <bpt id="p1">**</bpt>Search explorer<ept id="p1">**</ept>.</source><target>En haut de l’onglet de votre ressource Recherche Azure AI, sélectionnez <bpt id="p1">**</bpt>Explorateur de recherche<ept id="p1">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p331-PARA"><group id="s331-PARA"><trans-unit id="331" translate="yes" xml:space="preserve">
          <source>In Search explorer, in the <bpt id="p1">**</bpt>Query string<ept id="p1">**</ept> box, submit the following JSON query:</source><target>Dans l’Explorateur de recherche, dans la zone <bpt id="p1">**</bpt>Chaîne de requête<ept id="p1">**</ept>, envoyez la requête JSON suivante :</target>
        </trans-unit></group></group>
        <group id="p332-PARA"><group id="s332-PARA"><trans-unit id="332" translate="yes" xml:space="preserve">
          <source>This query retrieves the <bpt id="p1">**</bpt>url<ept id="p1">**</ept>, <bpt id="p2">**</bpt>sentiment<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>keyphrases<ept id="p3">**</ept> for all documents that mention <bpt id="p4">*</bpt>London<ept id="p4">*</ept> authored by <bpt id="p5">*</bpt>Reviewer<ept id="p5">*</ept> that have a positive <bpt id="p6">**</bpt>sentiment<ept id="p6">**</ept> label (in other words, positive reviews that mention London)</source><target>Cette requête récupère l’<bpt id="p1">**</bpt>URL<ept id="p1">**</ept>, le <bpt id="p2">**</bpt>sentiment<ept id="p2">**</ept> et les <bpt id="p3">**</bpt>phrases clés<ept id="p3">**</ept> pour tous les documents qui mentionnent <bpt id="p4">*</bpt>Londres<ept id="p4">*</ept> créés par <bpt id="p5">*</bpt>Reviewer<ept id="p5">*</ept> qui ont une étiquette de <bpt id="p6">**</bpt>sentiment<ept id="p6">**</ept> positive (en d’autres termes, des critiques positives qui mentionnent Londres)</target>
        </trans-unit></group></group>
        <group id="p333-PARA"><group id="s333-PARA"><trans-unit id="333" translate="yes" xml:space="preserve">
          <source>Close the <bpt id="p1">**</bpt>Search explorer<ept id="p1">**</ept> page to return to the <bpt id="p2">**</bpt>Overview<ept id="p2">**</ept> page.</source><target>Fermez la page <bpt id="p1">**</bpt>Explorateur de recherche<ept id="p1">**</ept> pour revenir à la page <bpt id="p2">**</bpt>Vue d’ensemble<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p334-PARA"><group id="s334-PARA"><trans-unit id="334" translate="yes" xml:space="preserve">
          <source>Create a search client application</source><target>Créer une application cliente de recherche</target>
        </trans-unit></group></group>
        <group id="p335-PARA"><group id="s335-PARA"><trans-unit id="335" translate="yes" xml:space="preserve">
          <source>Now that you have a useful index, you can use it from a client application.</source><target>Maintenant que vous avez un index utile, vous pouvez l’utiliser à partir d’une application cliente.</target>
        </trans-unit></group></group>
        <group id="p336-PARA"><group id="s336-PARA"><trans-unit id="336" translate="yes" xml:space="preserve">
          <source>You can do this by consuming the REST interface, submitting requests and receiving responses in JSON format over HTTP; or you can use the software development kit (SDK) for your preferred programming language.</source><target>Vous pouvez le faire en consommant l’interface REST, en envoyant des demandes et en recevant des réponses au format JSON via HTTP ; ou vous pouvez utiliser le kit de développement logiciel (SDK) pour votre langage de programmation préféré.</target>
        </trans-unit></group></group>
        <group id="p337-PARA"><group id="s337-PARA"><trans-unit id="337" translate="yes" xml:space="preserve">
          <source>In this exercise, we'll use the SDK.</source><target>Dans cet exercice, nous allons utiliser le kit de développement logiciel (SDK).</target>
        </trans-unit></group></group>
        <group id="p338-PARA"><group id="s338-PARA"><trans-unit id="338" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: You can choose to use the SDK for either <bpt id="p2">**</bpt>C#<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Python<ept id="p3">**</ept>.</source><target><bpt id="p1">**</bpt>Remarque<ept id="p1">**</ept> : Vous pouvez choisir d’utiliser le kit de développement logiciel (SDK) pour <bpt id="p2">**</bpt>C#<ept id="p2">**</ept> ou <bpt id="p3">**</bpt>Python<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p339-PARA"><group id="s339-PARA"><trans-unit id="339" translate="yes" xml:space="preserve">
          <source>In the steps below, perform the actions appropriate for your preferred language.</source><target>Dans les étapes qui suivent, effectuez les actions appropriées pour votre langage préféré.</target>
        </trans-unit></group></group>
        <group id="p340-PARA"><group id="s340-PARA"><trans-unit id="340" translate="yes" xml:space="preserve">
          <source>Get the endpoint and keys for your search resource</source><target>Obtenir le point de terminaison et les clés de votre ressource de recherche</target>
        </trans-unit></group></group>
        <group id="p341-PARA"><group id="s341-PARA"><trans-unit id="341" translate="yes" xml:space="preserve">
          <source>In the Azure portal, on the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> page for your Azure AI Search resource, note the <bpt id="p2">**</bpt>Url<ept id="p2">**</ept> value, which should be similar to <bpt id="p3">**</bpt>https://<bpt id="p4">*</bpt>your_resource_name<ept id="p4">*</ept>.search.windows.net<ept id="p3">**</ept>.</source><target>Dans le Portail Azure, dans la page <bpt id="p1">**</bpt>Vue d’ensemble<ept id="p1">**</ept> de votre ressource Recherche Azure AI, notez la valeur de l’<bpt id="p2">**</bpt>URL<ept id="p2">**</ept>, qui doit être similaire à <bpt id="p3">**</bpt>https://<bpt id="p4">*</bpt>your_resource_name<ept id="p4">*</ept>.search.windows.net<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p342-PARA"><group id="s342-PARA"><trans-unit id="342" translate="yes" xml:space="preserve">
          <source>This is the endpoint for your search resource.</source><target>Il s’agit du point de terminaison de votre ressource de recherche.</target>
        </trans-unit></group></group>
        <group id="p343-PARA"><group id="s343-PARA"><trans-unit id="343" translate="yes" xml:space="preserve">
          <source>On the <bpt id="p1">**</bpt>Keys<ept id="p1">**</ept> page, note that there are two <bpt id="p2">**</bpt>admin<ept id="p2">**</ept> keys, and a single <bpt id="p3">**</bpt>query<ept id="p3">**</ept> key.</source><target>Dans la page <bpt id="p1">**</bpt>Clés<ept id="p1">**</ept> , notez qu’il existe deux clés d’<bpt id="p2">**</bpt>administration<ept id="p2">**</ept> et une seule clé de <bpt id="p3">**</bpt>requête<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p344-PARA"><group id="s344-PARA"><trans-unit id="344" translate="yes" xml:space="preserve">
          <source>An <bpt id="p1">*</bpt>admin<ept id="p1">*</ept> key is used to create and manage search resources; a <bpt id="p2">*</bpt>query<ept id="p2">*</ept> key is used by client applications that only need to perform search queries.</source><target>Une clé d’<bpt id="p1">*</bpt>administration<ept id="p1">*</ept> est utilisée pour créer et gérer des ressources de recherche. Une clé de <bpt id="p2">*</bpt>requête<ept id="p2">*</ept> est utilisée par les applications clientes qui doivent uniquement effectuer des requêtes de recherche.</target>
        </trans-unit></group></group>
        <group id="p345-PARA"><group id="s345-PARA"><trans-unit id="345" translate="yes" xml:space="preserve">
          <source><bpt id="p1">*</bpt>You will need the endpoint and query key for your client application.<ept id="p1">*</ept></source><target><bpt id="p1">*</bpt>Vous aurez besoin du point de terminaison et de la clé de requête pour votre application cliente.<ept id="p1">*</ept></target>
        </trans-unit></group></group>
        <group id="p346-PARA"><group id="s346-PARA"><trans-unit id="346" translate="yes" xml:space="preserve">
          <source>Prepare to use the Azure AI Search SDK</source><target>Se préparer à l’utilisation du kit de développement logiciel (SDK) de Recherche Azure AI</target>
        </trans-unit></group></group>
        <group id="p347-PARA"><group id="s347-PARA"><trans-unit id="347" translate="yes" xml:space="preserve">
          <source>In Visual Studio Code, in the <bpt id="p1">**</bpt>Explorer<ept id="p1">**</ept> pane, browse to the <bpt id="p2">**</bpt>01-azure-search<ept id="p2">**</ept> folder and expand the <bpt id="p3">**</bpt>C-Sharp<ept id="p3">**</ept> or <bpt id="p4">**</bpt>Python<ept id="p4">**</ept> folder depending on your language preference.</source><target>Dans Visual Studio Code, dans le volet <bpt id="p1">**</bpt>Explorateur<ept id="p1">**</ept>, accédez au dossier <bpt id="p2">**</bpt>01-azure-search<ept id="p2">**</ept>, puis développez le dossier <bpt id="p3">**</bpt>C-Sharp<ept id="p3">**</ept> ou <bpt id="p4">**</bpt>Python<ept id="p4">**</ept>, en fonction de votre préférence de langage.</target>
        </trans-unit></group></group>
        <group id="p348-PARA"><group id="s348-PARA"><trans-unit id="348" translate="yes" xml:space="preserve">
          <source>Right-click the <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> folder and open an integrated terminal.</source><target>Cliquez avec le bouton droit de la souris sur le dossier <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> et ouvrez un terminal intégré.</target>
        </trans-unit></group></group>
        <group id="p349-PARA"><group id="s349-PARA"><trans-unit id="349" translate="yes" xml:space="preserve">
          <source>Then install the Azure AI Search SDK package by running the appropriate command for your language preference:</source><target>Installez ensuite le package du kit de développement logiciel (SDK) de Recherche Azure AI en exécutant la commande appropriée pour votre préférence de langage :</target>
        </trans-unit></group></group>
        <group id="p350-PARA"><group id="s350-PARA"><trans-unit id="350" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>C#<ept id="p1">**</ept></source><target><bpt id="p1">**</bpt>C#<ept id="p1">**</ept></target>
        </trans-unit></group></group>
        <group id="p351-PARA"><group id="s351-PARA"><trans-unit id="351" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Python<ept id="p1">**</ept></source><target><bpt id="p1">**</bpt>Python<ept id="p1">**</ept></target>
        </trans-unit></group></group>
        <group id="p352-PARA"><group id="s352-PARA"><trans-unit id="352" translate="yes" xml:space="preserve">
          <source>View the contents of the <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> folder, and note that it contains a file for configuration settings:</source><target>Affichez le contenu du dossier <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept>, et notez qu’il contient un fichier pour les paramètres de configuration :</target>
        </trans-unit></group></group>
        <group id="p353-PARA"><group id="s353-PARA"><trans-unit id="353" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>C#<ept id="p1">**</ept>: appsettings.json</source><target><bpt id="p1">**</bpt>C#<ept id="p1">**</ept> : appsettings.json</target>
        </trans-unit></group></group>
        <group id="p354-PARA"><group id="s354-PARA"><trans-unit id="354" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Python<ept id="p1">**</ept>: .env</source><target><bpt id="p1">**</bpt>Python<ept id="p1">**</ept> : .env</target>
        </trans-unit></group></group>
        <group id="p355-PARA"><group id="s355-PARA"><trans-unit id="355" translate="yes" xml:space="preserve">
          <source>Open the configuration file and update the configuration values it contains to reflect the <bpt id="p1">**</bpt>endpoint<ept id="p1">**</ept> and <bpt id="p2">**</bpt>query key<ept id="p2">**</ept> for your Azure AI Search resource.</source><target>Ouvrez le fichier de configuration et mettez à jour les valeurs de configuration qu’il contient pour refléter le <bpt id="p1">**</bpt>point de terminaison<ept id="p1">**</ept> et la <bpt id="p2">**</bpt>clé de requête<ept id="p2">**</ept> de votre ressource Recherche Azure AI.</target>
        </trans-unit></group></group>
        <group id="p356-PARA"><group id="s356-PARA"><trans-unit id="356" translate="yes" xml:space="preserve">
          <source>Save your changes.</source><target>Enregistrez vos modifications.</target>
        </trans-unit></group></group>
        <group id="p357-PARA"><group id="s357-PARA"><trans-unit id="357" translate="yes" xml:space="preserve">
          <source>Explore code to search an index</source><target>Explorer le code pour rechercher un index</target>
        </trans-unit></group></group>
        <group id="p358-PARA"><group id="s358-PARA"><trans-unit id="358" translate="yes" xml:space="preserve">
          <source>The <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> folder contains code files for a web application (a Microsoft C# <bpt id="p2">*</bpt>ASP.NET Razor<ept id="p2">*</ept> web application or a Python <bpt id="p3">*</bpt>Flask<ept id="p3">*</ept> application), which includes search functionality.</source><target>Le dossier <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> contient des fichiers de code pour une application web (une application web Microsoft C# <bpt id="p2">*</bpt>ASP.NET Razor<ept id="p2">*</ept> ou une application <bpt id="p3">*</bpt>Flask<ept id="p3">*</ept> Python), qui inclut des fonctionnalités de recherche.</target>
        </trans-unit></group></group>
        <group id="p359-PARA"><group id="s359-PARA"><trans-unit id="359" translate="yes" xml:space="preserve">
          <source>Open the following code file in the web application, depending on your choice of programming language:</source><target>Ouvrez le fichier de code suivant dans l’application web, en fonction de votre choix de langage de programmation :</target>
        </trans-unit></group></group>
        <group id="p360-PARA"><group id="s360-PARA"><trans-unit id="360" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>C#<ept id="p1">**</ept>:Pages/Index.cshtml.cs</source><target><bpt id="p1">**</bpt>C#<ept id="p1">**</ept> : Pages/Index.cshtml.cs</target>
        </trans-unit></group></group>
        <group id="p361-PARA"><group id="s361-PARA"><trans-unit id="361" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Python<ept id="p1">**</ept>: app.py</source><target><bpt id="p1">**</bpt>Python<ept id="p1">**</ept> : app.py</target>
        </trans-unit></group></group>
        <group id="p362-PARA"><group id="s362-PARA"><trans-unit id="362" translate="yes" xml:space="preserve">
          <source>Near the top of the code file, find the comment <bpt id="p1">**</bpt>Import search namespaces<ept id="p1">**</ept>, and note the namespaces that have been imported to work with the Azure AI Search SDK:</source><target>En haut du fichier de code, recherchez le commentaire <bpt id="p1">**</bpt>Importer les espaces de noms de recherche<ept id="p1">**</ept> et notez les espaces de noms importés pour travailler avec le kit de développement logiciel (SDK) de Recherche Azure AI :</target>
        </trans-unit></group></group>
        <group id="p363-PARA"><group id="s363-PARA"><trans-unit id="363" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>search_query<ept id="p1">**</ept> function, find the comment <bpt id="p2">**</bpt>Create a search client<ept id="p2">**</ept>, and note that the code creates a <bpt id="p3">**</bpt>SearchClient<ept id="p3">**</ept> object using the endpoint and query key for your Azure AI Search resource:</source><target>Dans la fonction <bpt id="p1">**</bpt>search_query<ept id="p1">**</ept>, recherchez le commentaire <bpt id="p2">**</bpt>Créer un client de recherche<ept id="p2">**</ept> et notez que le code crée un objet <bpt id="p3">**</bpt>SearchClient<ept id="p3">**</ept> à l’aide du point de terminaison et de la clé de requête pour votre ressource Recherche Azure AI :</target>
        </trans-unit></group></group>
        <group id="p364-PARA"><group id="s364-PARA"><trans-unit id="364" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>search_query<ept id="p1">**</ept> function, find the comment <bpt id="p2">**</bpt>Submit search query<ept id="p2">**</ept>, and review the code to submit a search for the specified text with the following options:</source><target>Dans la fonction <bpt id="p1">**</bpt>search_query<ept id="p1">**</ept>, recherchez le commentaire <bpt id="p2">**</bpt>Envoyer une requête de recherche<ept id="p2">**</ept> et passez en revue le code pour lancer une recherche pour le texte spécifié avec les options suivantes :</target>
        </trans-unit></group></group>
        <group id="p365-PARA"><group id="s365-PARA"><trans-unit id="365" translate="yes" xml:space="preserve">
          <source>A <bpt id="p1">*</bpt>search mode<ept id="p1">*</ept> that requires <bpt id="p2">**</bpt>all<ept id="p2">**</ept> of the individual words in the search text are found.</source><target>Un <bpt id="p1">*</bpt>mode de recherche<ept id="p1">*</ept> qui nécessite que <bpt id="p2">**</bpt>tous<ept id="p2">**</ept> les mots individuels dans le texte de recherche soient trouvés.</target>
        </trans-unit></group></group>
        <group id="p366-PARA"><group id="s366-PARA"><trans-unit id="366" translate="yes" xml:space="preserve">
          <source>The total number of documents found by the search is included in the results.</source><target>Le nombre total de documents trouvés par la recherche est inclus dans les résultats.</target>
        </trans-unit></group></group>
        <group id="p367-PARA"><group id="s367-PARA"><trans-unit id="367" translate="yes" xml:space="preserve">
          <source>The results are filtered to include only documents that match the provided filter expression.</source><target>Les résultats sont filtrés pour inclure uniquement les documents qui correspondent à l’expression de filtre fournie.</target>
        </trans-unit></group></group>
        <group id="p368-PARA"><group id="s368-PARA"><trans-unit id="368" translate="yes" xml:space="preserve">
          <source>The results are sorted into the specified sort order.</source><target>Les résultats sont triés dans l’ordre de tri spécifié.</target>
        </trans-unit></group></group>
        <group id="p369-PARA"><group id="s369-PARA"><trans-unit id="369" translate="yes" xml:space="preserve">
          <source>Each discrete value of the <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept> field is returned as a <bpt id="p2">*</bpt>facet<ept id="p2">*</ept> that can be used to display pre-defined values for filtering.</source><target>Chaque valeur discrète du champ <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept> est retournée en tant que <bpt id="p2">*</bpt>facette<ept id="p2">*</ept> qui peut être utilisée pour afficher des valeurs prédéfinies pour le filtrage.</target>
        </trans-unit></group></group>
        <group id="p370-PARA"><group id="s370-PARA"><trans-unit id="370" translate="yes" xml:space="preserve">
          <source>Up to three extracts of the <bpt id="p1">**</bpt>merged_content<ept id="p1">**</ept> and <bpt id="p2">**</bpt>imageCaption<ept id="p2">**</ept> fields with the search terms highlighted are included in the results.</source><target>Jusqu’à trois extraits des champs <bpt id="p1">**</bpt>merged_content<ept id="p1">**</ept> et <bpt id="p2">**</bpt>imageCaption<ept id="p2">**</ept> avec les termes de recherche mis en surbrillance sont inclus dans les résultats.</target>
        </trans-unit></group></group>
        <group id="p371-PARA"><group id="s371-PARA"><trans-unit id="371" translate="yes" xml:space="preserve">
          <source>The results include only the fields specified.</source><target>Les résultats incluent uniquement les champs spécifiés.</target>
        </trans-unit></group></group>
        <group id="p372-PARA"><group id="s372-PARA"><trans-unit id="372" translate="yes" xml:space="preserve">
          <source>Explore code to render search results</source><target>Explorer le code pour afficher les résultats de la recherche</target>
        </trans-unit></group></group>
        <group id="p373-PARA"><group id="s373-PARA"><trans-unit id="373" translate="yes" xml:space="preserve">
          <source>The web app already includes code to process and render the search results.</source><target>L’application web inclut déjà du code pour traiter et afficher les résultats de la recherche.</target>
        </trans-unit></group></group>
        <group id="p374-PARA"><group id="s374-PARA"><trans-unit id="374" translate="yes" xml:space="preserve">
          <source>Open the following code file in the web application, depending on your choice of programming language:</source><target>Ouvrez le fichier de code suivant dans l’application web, en fonction de votre choix de langage de programmation :</target>
        </trans-unit></group></group>
        <group id="p375-PARA"><group id="s375-PARA"><trans-unit id="375" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>C#<ept id="p1">**</ept>:Pages/Index.cshtml</source><target><bpt id="p1">**</bpt>C#<ept id="p1">**</ept> : Pages/Index.cshtml</target>
        </trans-unit></group></group>
        <group id="p376-PARA"><group id="s376-PARA"><trans-unit id="376" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Python<ept id="p1">**</ept>: templates/search.html</source><target><bpt id="p1">**</bpt>Python<ept id="p1">**</ept> : templates/search.html</target>
        </trans-unit></group></group>
        <group id="p377-PARA"><group id="s377-PARA"><trans-unit id="377" translate="yes" xml:space="preserve">
          <source>Examine the code, which renders the page on which the search results are displayed.</source><target>Examinez le code, qui affiche la page sur laquelle les résultats de la recherche sont affichés.</target>
        </trans-unit></group></group>
        <group id="p378-PARA"><group id="s378-PARA"><trans-unit id="378" translate="yes" xml:space="preserve">
          <source>Observe that:</source><target>Observez que :</target>
        </trans-unit></group></group>
        <group id="p379-PARA"><group id="s379-PARA"><trans-unit id="379" translate="yes" xml:space="preserve">
          <source>The page begins with a search form that the user can use to submit a new search (in the Python version of the application, this form is defined in the <bpt id="p1">**</bpt>base.html<ept id="p1">**</ept> template), which is referenced at the beginning of the page.</source><target>La page commence par un formulaire de recherche que l’utilisateur peut utiliser pour soumettre une nouvelle recherche (dans la version Python de l’application, ce formulaire est défini dans le modèle <bpt id="p1">**</bpt>base.html<ept id="p1">**</ept> ), qui est référencé au début de la page.</target>
        </trans-unit></group></group>
        <group id="p380-PARA"><group id="s380-PARA"><trans-unit id="380" translate="yes" xml:space="preserve">
          <source>A second form is then rendered, enabling the user to refine the search results.</source><target>Un deuxième formulaire est ensuite rendu, ce qui permet à l’utilisateur d’affiner les résultats de la recherche.</target>
        </trans-unit></group></group>
        <group id="p381-PARA"><group id="s381-PARA"><trans-unit id="381" translate="yes" xml:space="preserve">
          <source>The code for this form:</source><target>Code de ce formulaire :</target>
        </trans-unit></group></group>
        <group id="p382-PARA"><group id="s382-PARA"><trans-unit id="382" translate="yes" xml:space="preserve">
          <source>Retrieves and displays the count of documents from the search results.</source><target>Récupère et affiche le nombre de documents à partir des résultats de la recherche.</target>
        </trans-unit></group></group>
        <group id="p383-PARA"><group id="s383-PARA"><trans-unit id="383" translate="yes" xml:space="preserve">
          <source>Retrieves the facet values for the <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept> field and displays them as an option list for filtering.</source><target>Récupère les valeurs de facette du champ <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept> et les affiche en tant que liste d’options pour le filtrage.</target>
        </trans-unit></group></group>
        <group id="p384-PARA"><group id="s384-PARA"><trans-unit id="384" translate="yes" xml:space="preserve">
          <source>Creates a drop-down list of sort options for the results.</source><target>Crée une liste déroulante d’options de tri pour les résultats.</target>
        </trans-unit></group></group>
        <group id="p385-PARA"><group id="s385-PARA"><trans-unit id="385" translate="yes" xml:space="preserve">
          <source>The code then iterates through the search results, rendering each result as follows:</source><target>Le code effectue ensuite une itération dans les résultats de la recherche, en montrant chaque résultat comme suit :</target>
        </trans-unit></group></group>
        <group id="p386-PARA"><group id="s386-PARA"><trans-unit id="386" translate="yes" xml:space="preserve">
          <source>Display the <bpt id="p1">**</bpt>metadata_storage_name<ept id="p1">**</ept> (file name) field as a link to the address in the <bpt id="p2">**</bpt>url<ept id="p2">**</ept> field.</source><target>Affichez le champ <bpt id="p1">**</bpt>metadata_storage_name<ept id="p1">**</ept> (nom de fichier) en tant que lien vers l’adresse dans le champ de l’<bpt id="p2">**</bpt>URL<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p387-PARA"><group id="s387-PARA"><trans-unit id="387" translate="yes" xml:space="preserve">
          <source>Displaying <bpt id="p1">*</bpt>highlights<ept id="p1">*</ept> for search terms found in the <bpt id="p2">**</bpt>merged_content<ept id="p2">**</ept> and <bpt id="p3">**</bpt>imageCaption<ept id="p3">**</ept> fields to help show the search terms in context.</source><target>Affichage de <bpt id="p1">*</bpt>surbrillances<ept id="p1">*</ept> pour les termes de recherche trouvés dans les champs <bpt id="p2">**</bpt>merged_content<ept id="p2">**</ept> et <bpt id="p3">**</bpt>imageCaption<ept id="p3">**</ept> pour vous aider à afficher les termes de recherche dans le contexte.</target>
        </trans-unit></group></group>
        <group id="p388-PARA"><group id="s388-PARA"><trans-unit id="388" translate="yes" xml:space="preserve">
          <source>Display the <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept>, <bpt id="p2">**</bpt>metadata_storage_size<ept id="p2">**</ept>, <bpt id="p3">**</bpt>metadata_storage_last_modified<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>language<ept id="p4">**</ept> fields.</source><target>Affichez les champs <bpt id="p1">**</bpt>metadata_author<ept id="p1">**</ept>, <bpt id="p2">**</bpt>metadata_storage_size<ept id="p2">**</ept>, <bpt id="p3">**</bpt>metadata_storage_last_modified<ept id="p3">**</ept> et <bpt id="p4">**</bpt>langage<ept id="p4">**</ept> .</target>
        </trans-unit></group></group>
        <group id="p389-PARA"><group id="s389-PARA"><trans-unit id="389" translate="yes" xml:space="preserve">
          <source>Display the <bpt id="p1">**</bpt>sentiment<ept id="p1">**</ept> label for the document.</source><target>Affichez l’étiquette de <bpt id="p1">**</bpt>sentiment<ept id="p1">**</ept> du document.</target>
        </trans-unit></group></group>
        <group id="p390-PARA"><group id="s390-PARA"><trans-unit id="390" translate="yes" xml:space="preserve">
          <source>Can be positive, negative, neutral, or mixed.</source><target>Peut être positif, négatif, neutre ou mixte.</target>
        </trans-unit></group></group>
        <group id="p391-PARA"><group id="s391-PARA"><trans-unit id="391" translate="yes" xml:space="preserve">
          <source>Display the first five <bpt id="p1">**</bpt>keyphrases<ept id="p1">**</ept> (if any).</source><target>Affichez les cinq premiers <bpt id="p1">**</bpt>keyphrases<ept id="p1">**</ept> (le cas échéant).</target>
        </trans-unit></group></group>
        <group id="p392-PARA"><group id="s392-PARA"><trans-unit id="392" translate="yes" xml:space="preserve">
          <source>Display the first five <bpt id="p1">**</bpt>locations<ept id="p1">**</ept> (if any).</source><target>Affichez les cinq premiers <bpt id="p1">**</bpt>emplacements<ept id="p1">**</ept> (le cas échéant).</target>
        </trans-unit></group></group>
        <group id="p393-PARA"><group id="s393-PARA"><trans-unit id="393" translate="yes" xml:space="preserve">
          <source>Display the first five <bpt id="p1">**</bpt>imageTags<ept id="p1">**</ept> (if any).</source><target>Affichez les cinq premiers <bpt id="p1">**</bpt>imagesTags<ept id="p1">**</ept> (le cas échéant).</target>
        </trans-unit></group></group>
        <group id="p394-PARA"><group id="s394-PARA"><trans-unit id="394" translate="yes" xml:space="preserve">
          <source>Run the web app</source><target>Exécuter l’application web</target>
        </trans-unit></group></group>
        <group id="p395-PARA"><group id="s395-PARA"><trans-unit id="395" translate="yes" xml:space="preserve">
          <source>return to the integrated terminal for the <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> folder, and enter the following command to run the program:</source><target>revenez au terminal intégré pour le dossier <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept>, puis entrez la commande suivante pour exécuter le programme :</target>
        </trans-unit></group></group>
        <group id="p396-PARA"><group id="s396-PARA"><trans-unit id="396" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>C#<ept id="p1">**</ept></source><target><bpt id="p1">**</bpt>C#<ept id="p1">**</ept></target>
        </trans-unit></group></group>
        <group id="p397-PARA"><group id="s397-PARA"><trans-unit id="397" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Python<ept id="p1">**</ept></source><target><bpt id="p1">**</bpt>Python<ept id="p1">**</ept></target>
        </trans-unit></group></group>
        <group id="p398-PARA"><group id="s398-PARA"><trans-unit id="398" translate="yes" xml:space="preserve">
          <source>In the message that is displayed when the app starts successfully, follow the link to the running web application (<bpt id="p1">*</bpt><ph id="ph1">http://localhost:5000/</ph><ept id="p1">*</ept> or <bpt id="p2">*</bpt><ph id="ph2">http://127.0.0.1:5000/</ph><ept id="p2">*</ept>) to open the Margies Travel site in a web browser.</source><target>Dans le message qui s’affiche lorsque l’application démarre correctement, suivez le lien vers l’application web en cours d’exécution ( <bpt id="p1">*</bpt><ph id="ph1">http://localhost:5000/</ph><ept id="p1">*</ept> ou <bpt id="p2">*</bpt><ph id="ph2">http://127.0.0.1:5000/</ph><ept id="p2">*</ept> ) pour ouvrir le site Margies Travel dans un navigateur web.</target>
        </trans-unit></group></group>
        <group id="p399-PARA"><group id="s399-PARA"><trans-unit id="399" translate="yes" xml:space="preserve">
          <source>In the Margie's Travel website, enter <bpt id="p1">**</bpt>London hotel<ept id="p1">**</ept> into the search box and click <bpt id="p2">**</bpt>Search<ept id="p2">**</ept>.</source><target>Dans le site web Margie’s Travel, entrez <bpt id="p1">**</bpt>hôtel Londres<ept id="p1">**</ept> dans la zone de recherche, puis cliquez sur <bpt id="p2">**</bpt>Rechercher<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p400-PARA"><group id="s400-PARA"><trans-unit id="400" translate="yes" xml:space="preserve">
          <source>Review the search results.</source><target>Examinez les résultats de recherche.</target>
        </trans-unit></group></group>
        <group id="p401-PARA"><group id="s401-PARA"><trans-unit id="401" translate="yes" xml:space="preserve">
          <source>They include the file name (with a hyperlink to the file URL), an extract of the file content with the search terms (<bpt id="p1">*</bpt>London<ept id="p1">*</ept> and <bpt id="p2">*</bpt>hotel<ept id="p2">*</ept>) emphasized, and other attributes of the file from the index fields.</source><target>Ils incluent le nom de fichier (avec un lien hypertexte vers l’URL de fichier), un extrait du contenu du fichier avec les termes de recherche (<bpt id="p1">*</bpt>hôtel<ept id="p1">*</ept> et <bpt id="p2">*</bpt>Londres<ept id="p2">*</ept>) mis en évidence, et d’autres attributs du fichier à partir des champs d’index.</target>
        </trans-unit></group></group>
        <group id="p402-PARA"><group id="s402-PARA"><trans-unit id="402" translate="yes" xml:space="preserve">
          <source>Observe that the results page includes some user interface elements that enable you to refine the results.</source><target>Notez que la page de résultats inclut certains éléments d’interface utilisateur qui vous permettent d’affiner les résultats.</target>
        </trans-unit></group></group>
        <group id="p403-PARA"><group id="s403-PARA"><trans-unit id="403" translate="yes" xml:space="preserve">
          <source>These include:</source><target>notamment :</target>
        </trans-unit></group></group>
        <group id="p404-PARA"><group id="s404-PARA"><trans-unit id="404" translate="yes" xml:space="preserve">
          <source>A <bpt id="p1">*</bpt>filter<ept id="p1">*</ept> based on a facet value for the <bpt id="p2">**</bpt>metadata_author<ept id="p2">**</ept> field.</source><target>Un <bpt id="p1">*</bpt>filtre<ept id="p1">*</ept> basé sur une valeur de facette pour le champ <bpt id="p2">**</bpt>metadata_author<ept id="p2">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p405-PARA"><group id="s405-PARA"><trans-unit id="405" translate="yes" xml:space="preserve">
          <source>This demonstrates how you can use <bpt id="p1">*</bpt>facetable<ept id="p1">*</ept> fields to return a list of <bpt id="p2">*</bpt>facets<ept id="p2">*</ept> - fields with a small set of discrete values that can displayed as potential filter values in the user interface.</source><target>Cela montre comment utiliser des champs <bpt id="p1">*</bpt>à choix multiples<ept id="p1">*</ept> pour renvoyer une liste de <bpt id="p2">*</bpt>facettes<ept id="p2">*</ept> - champs avec un petit ensemble de valeurs discrètes qui peuvent s’afficher comme valeurs de filtre potentielles dans l’interface utilisateur.</target>
        </trans-unit></group></group>
        <group id="p406-PARA"><group id="s406-PARA"><trans-unit id="406" translate="yes" xml:space="preserve">
          <source>The ability to <bpt id="p1">*</bpt>order<ept id="p1">*</ept> the results based on a specified field and sort direction (ascending or descending).</source><target>Possibilité d’<bpt id="p1">*</bpt>ordonner<ept id="p1">*</ept> les résultats en fonction d’un champ spécifié et d’une direction de tri (croissant ou décroissant).</target>
        </trans-unit></group></group>
        <group id="p407-PARA"><group id="s407-PARA"><trans-unit id="407" translate="yes" xml:space="preserve">
          <source>The default order is based on <bpt id="p1">*</bpt>relevancy<ept id="p1">*</ept>, which is calculated as a <bpt id="p2">**</bpt>search.score()<ept id="p2">**</ept> value based on a <bpt id="p3">*</bpt>scoring profile<ept id="p3">*</ept> that evaluates the frequency and importance of search terms in the index fields.</source><target>L’ordre par défaut est basé sur la <bpt id="p1">*</bpt>pertinence<ept id="p1">*</ept>, qui est calculé en tant que valeur <bpt id="p2">**</bpt>search.score()<ept id="p2">**</ept> basée sur un <bpt id="p3">*</bpt>profil de score<ept id="p3">*</ept> qui évalue la fréquence et l’importance des termes de recherche dans les champs d’index.</target>
        </trans-unit></group></group>
        <group id="p408-PARA"><group id="s408-PARA"><trans-unit id="408" translate="yes" xml:space="preserve">
          <source>Select the <bpt id="p1">**</bpt>Reviewer<ept id="p1">**</ept> filter and the <bpt id="p2">**</bpt>Positive to negative<ept id="p2">**</ept> sort option, and then select <bpt id="p3">**</bpt>Refine Results<ept id="p3">**</ept>.</source><target>Sélectionnez le filtre <bpt id="p1">**</bpt>Réviseur<ept id="p1">**</ept> et l’option de tri <bpt id="p2">**</bpt>Positif à négatif<ept id="p2">**</ept>, puis sélectionnez <bpt id="p3">**</bpt>Affiner les résultats<ept id="p3">**</ept>.</target>
        </trans-unit></group></group>
        <group id="p409-PARA"><group id="s409-PARA"><trans-unit id="409" translate="yes" xml:space="preserve">
          <source>Observe that the results are filtered to include only reviews, and sorted based on the sentiment label.</source><target>Notez que les résultats sont filtrés pour inclure uniquement les révisions et triés en fonction de l’étiquette de sentiment.</target>
        </trans-unit></group></group>
        <group id="p410-PARA"><group id="s410-PARA"><trans-unit id="410" translate="yes" xml:space="preserve">
          <source>In the <bpt id="p1">**</bpt>Search<ept id="p1">**</ept> box, enter a new search for <bpt id="p2">**</bpt>quiet hotel in New York<ept id="p2">**</ept> and review the results.</source><target>Dans la zone de <bpt id="p1">**</bpt>Recherche<ept id="p1">**</ept>, entrez une nouvelle recherche d’<bpt id="p2">**</bpt>hôtel calme à New York<ept id="p2">**</ept> et passez en revue les résultats.</target>
        </trans-unit></group></group>
        <group id="p411-PARA"><group id="s411-PARA"><trans-unit id="411" translate="yes" xml:space="preserve">
          <source>Try the following search terms:</source><target>Essayez les termes de recherche suivants :</target>
        </trans-unit></group></group>
        <group id="p412-PARA"><group id="s412-PARA"><trans-unit id="412" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Tower of London<ept id="p1">**</ept> (observe that this term is identified as a <bpt id="p2">*</bpt>key phrase<ept id="p2">*</ept> in some documents).</source><target><bpt id="p1">**</bpt>Tour de Londres<ept id="p1">**</ept> (observez que ce terme est identifié comme une <bpt id="p2">*</bpt>expression clé<ept id="p2">*</ept> dans certains documents).</target>
        </trans-unit></group></group>
        <group id="p413-PARA"><group id="s413-PARA"><trans-unit id="413" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>skyscraper<ept id="p1">**</ept> (observe that this word doesn't appear in the actual content of any documents, but is found in the <bpt id="p2">*</bpt>image captions<ept id="p2">*</ept> and <bpt id="p3">*</bpt>image tags<ept id="p3">*</ept> that were generated for images in some documents).</source><target><bpt id="p1">**</bpt>gratte-ciel<ept id="p1">**</ept> (observez que ce mot n’apparaît pas dans le contenu réel des documents, mais se trouve dans les <bpt id="p2">*</bpt>légendes d’image<ept id="p2">*</ept> et les <bpt id="p3">*</bpt>balises d’image<ept id="p3">*</ept> qui ont été générées pour les images dans certains documents).</target>
        </trans-unit></group></group>
        <group id="p414-PARA"><group id="s414-PARA"><trans-unit id="414" translate="yes" xml:space="preserve">
          <source><bpt id="p1">**</bpt>Mojave desert<ept id="p1">**</ept> (observe that this term is identified as a <bpt id="p2">*</bpt>location<ept id="p2">*</ept> in some documents).</source><target><bpt id="p1">**</bpt>Désert de Mojave<ept id="p1">**</ept> (observez que ce terme est identifié comme un <bpt id="p2">*</bpt>emplacement<ept id="p2">*</ept> dans certains documents).</target>
        </trans-unit></group></group>
        <group id="p415-PARA"><group id="s415-PARA"><trans-unit id="415" translate="yes" xml:space="preserve">
          <source>Close the browser tab containing the Margie's Travel web site and return to Visual Studio Code.</source><target>Fermez l’onglet du navigateur contenant le site web Margie’s Travel et revenez à Visual Studio Code.</target>
        </trans-unit></group></group>
        <group id="p416-PARA"><group id="s416-PARA"><trans-unit id="416" translate="yes" xml:space="preserve">
          <source>Then in the Python terminal for the <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> folder (where the dotnet or flask application is running), enter Ctrl+C to stop the app.</source><target>Ensuite, dans le terminal Python du dossier <bpt id="p1">**</bpt>margies-travel<ept id="p1">**</ept> (où l’application dotnet ou flask est en cours d’exécution), entrez CTRL + C pour arrêter l’application.</target>
        </trans-unit></group></group>
        <group id="p417-PARA"><group id="s417-PARA"><trans-unit id="417" translate="yes" xml:space="preserve">
          <source>More information</source><target>Plus d’informations</target>
        </trans-unit></group></group>
        <group id="p418-PARA"><group id="s418-PARA"><trans-unit id="418" translate="yes" xml:space="preserve">
          <source>To learn more about Azure AI Search, see the <bpt id="p1">[</bpt>Azure AI Search documentation<ept id="p1">](https://docs.microsoft.com/azure/search/search-what-is-azure-search)</ept>.</source><target>Pour en savoir plus sur la plateforme Recherche Azure AI, consultez la <bpt id="p1">[</bpt>documentation de Recherche Azure AI<ept id="p1">](https://docs.microsoft.com/azure/search/search-what-is-azure-search)</ept>.</target>
        </trans-unit></group></group>
      </group>
    </body>
  </file>
</xliff>