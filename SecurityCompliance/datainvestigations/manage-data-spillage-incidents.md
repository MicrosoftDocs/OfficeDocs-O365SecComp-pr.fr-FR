---
title: Gérer un incident de fuite de données dans Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit l’utilisation de l’outil nouvelles enquêtes de données (aperçu) dans le centre de sécurité & Compliance pour gérer un incident de déversement de données.
ms.openlocfilehash: 93199ad1f548e999dce9ad79ab311a57345b8772
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36649923"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Gérer un incident de fuite de données dans Microsoft 365

Les données sont libérées lorsqu’un document contenant des informations confidentielles, sensibles ou malveillantes est publié dans un environnement non approuvé. Lors de la détection d’un incident de volume de données, il est important de contenir rapidement l’environnement, d’évaluer la taille et les emplacements du détournement, d’examiner les activités de l’utilisateur et de supprimer les données déplacées du service. À l’aide de l’outil d’analyse des données (aperçu), vous pouvez rechercher des données sensibles, malveillantes ou déplacées dans Office 365, enquêter pour savoir ce qui s’est passé et prendre les mesures appropriées.  

## <a name="scope-of-this-article"></a>Portée de cet article

Cet article fournit une liste d’instructions sur la suppression définitive d’éléments des boîtes aux lettres Office 365 de sorte qu’ils ne soient plus accessibles ou récupérables par les utilisateurs ou les administrateurs. 

> [!NOTE]
> Lorsque vous supprimez des éléments situés dans un site SharePoint ou OneDrive entreprise, ils sont conservés pendant 93 jours après leur suppression de leur emplacement d’origine.

## <a name="scenario"></a>Scénario

Vous êtes informé d’un incident de fuite de données dans lequel un employé a volontairement partagé un document hautement confidentiel avec plusieurs personnes par courrier électronique. Vous souhaitez évaluer rapidement qui a reçu ce document, à l’intérieur et à l’extérieur de votre organisation. Une fois que vous avez examiné l’incident, vous envisagez de partager vos découvertes avec d’autres investigateurs pour les examiner, puis de supprimer définitivement les données déduites de votre organisation Office 365. Une fois l’enquête terminée, vous souhaitez supprimer toutes les preuves. 

> [!IMPORTANT]
> Bien que vous puissiez supprimer définitivement les données déplacées au sein de votre organisation, toutes les données déplacées à l’extérieur de votre organisation ne peuvent pas être supprimées avec ces fonctionnalités.

## <a name="workflow"></a>Flux de travail

Voici le flux de travail pour l’utilisation des enquêtes de données (préversion) pour gérer un incident de fuite de données:

1.  Créez une enquête sur les données.

2.  Recherchez des données sensibles, malveillantes ou égarées et collectez-les en tant que preuves.

3.  Examinez et examinez les preuves.

4.  Supprimez définitivement les données déversées.

5.  Fermez ou supprimez l’enquête.


## <a name="before-you-begin"></a>Avant de commencer

- Pour créer une enquête sur les données, Rechercher du contenu et supprimer des données déduites, vous devez être membre du groupe de rôles Data investigation dans le centre de sécurité & Compliance Center.

- Pour contrôler les boîtes aux lettres utilisateur et les comptes OneDrive qu’un enquêteur peut rechercher, votre organisation peut définir des limites de conformité. Pour plus d’informations, configurez [les limites de conformité pour les enquêtes de découverte électronique](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Étape 1: créer une enquête de données

Pour créer une enquête dans l’outil d’analyse des données (aperçu):

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide d’un compte membre du groupe de rôles Data investigation.
    
3. Dans le centre de sécurité et de conformité, cliquez sur **analyses de données**.
 
4. Dans la page **enquêtes de données (aperçu)** , cliquez sur **créer une nouvelle enquête**.
    
5. Sur la page nouveau menu volant d’analyse des **données** , donnez un nom à l’enquête (obligatoire), puis tapez un numéro d’enquête facultatif et une description. Le nom doit être unique dans votre organisation.

6. Sous **voulez-vous configurer des paramètres supplémentaires après avoir créé cette enquête?**, effectuez l’une des opérations suivantes:

    - Cliquez sur **Oui** pour créer l’enquête, puis affichez la page **paramètres** dans le nouvel incident. Cela vous permet d’ajouter des membres à l’enquête.
    
    - Cliquez sur **non** pour créer l’enquête et l’afficher dans la liste des incidents dans la page enquêtes sur les **données (aperçu)** . Si vous choisissez cette option, vous serez ajouté en tant que membre unique de l’enquête et les paramètres de recherche et d’analyse par défaut seront utilisés. Vous pouvez ajouter des membres ou modifier les paramètres à tout moment après la création de l’enquête.

7. Cliquez sur **Enregistrer** pour créer l’enquête.

    La nouvelle enquête est affichée dans la liste de la page enquêtes sur les **données (aperçu)** . 

8. Pour ouvrir une enquête, cliquez sur le nom de l’enquête. 

    L’onglet **Accueil** de l’enquête s’affiche. 

> [!TIP]
> Songez à établir une convention d’affectation de noms pour les enquêtes et fournissez autant d’informations que possible dans le nom et la description afin de pouvoir les localiser et y faire référence ultérieurement si nécessaire.
 
## <a name="step-2-search-for-the-spilled-data"></a>Étape 2: Rechercher les données déversées 
 
Si vous identifiez les utilisateurs pour lesquels vous souhaitez rechercher des données déduites, vous pouvez les ajouter en tant que personnes intéressantes pour mapper leurs sources de données à l’enquête et effectuer rapidement des recherches dans leurs comptes de boîte aux lettres et OneDrive. Pour ajouter des personnes intéressantes pour l’enquête, cliquez sur **personnes intéressantes**, puis sur **Ajouter des personnes intéressantes**. Pour plus d’informations, consultez la rubrique [Manage People of Interest](manage-people-of-interest.md).

Dans l’onglet **recherches** , vous pouvez créer des recherches pour trouver les données déversées. Pour plus d’informations sur la création de recherches, voir [Rechercher des données dans une enquête](search-for-data.md).

Après avoir exécuté la recherche, vous pouvez prévisualiser des exemples de résultats de recherche et afficher des statistiques de recherche pour évaluer l’efficacité de votre requête de recherche. Après avoir identifié les éléments que vous souhaitez supprimer d’Office 365, vous pouvez ajouter les résultats de la recherche à un jeu de preuves. Pour ce faire, cliquez sur la recherche que vous souhaitez examiner. Sur la page de menu volant, cliquez sur **Ajouter des résultats à des preuves** et suivez les instructions. Ensuite, dans l’ensemble de preuves, vous pouvez passer en revue des documents individuels, examiner qui a eu accès aux documents et exporter les documents. Pour supprimer les documents (ou un sous-ensemble de documents) au lieu de les revoir, passez à l' [étape 4](#step-4-delete-the-spilled-data). 

> [!IMPORTANT]
> Les mots clés que vous utilisez dans la requête de recherche peuvent contenir les données propagées réelles que vous recherchez. Par exemple, si vous recherchez des documents contenant un numéro de sécurité sociale et que vous l’utilisez comme mot clé dans la requête de recherche, vous devez supprimer la requête ultérieurement afin d’éviter tout débordement. Vous pouvez supprimer la recherche ou supprimer l’intégralité de l’analyse à l' [étape 5](#step-5-close-or-delete-the-investigation). 

## <a name="step-3-review-and-investigate"></a>Étape 3: vérifier et examiner 

Dans l’enquête, accédez à l’onglet **preuve** et cliquez sur l’ensemble de preuves que vous avez créé à l’étape précédente. Une fois le travail de traitement terminé et les résultats de la recherche ajoutés à la preuve, vous pouvez passer en revue des documents individuels au format natif, au format texte ou au format quasi natif. Vous pouvez créer des requêtes supplémentaires pour affiner la liste des documents et marquer des documents pour indiquer les conclusions de votre enquête. Pour plus d’informations, voir [examiner les données dans les preuves](review-data-in-evidence.md)

Pour regrouper des documents et obtenir de l’aide supplémentaire pour votre révision, cliquez sur **gérer les preuves**. Dans la vignette **analyse** , cliquez sur **analyser**. Cela exécute des analyses avancées, telles que la détection des doublons, le Threading de messagerie électronique et l’analyse de thème. Pour plus d’informations, reportez-vous aux rubriques suivantes :

- [Exécuter les données d’analyse pour investiguer plus rapidement](run-analytics-to-investigate-faster.md)
- [Détecter des quasi-duplicatas](near-duplicates.md)
- [Threading de messagerie](email-threading.md)
- [Thèmes](themes.md)

Pour déterminer les utilisateurs impliqués dans le débordement des données, vous pouvez créer une requête dans l’ensemble de preuves, puis utiliser les conditions de l’expéditeur/auteur et des destinataires. Cette méthode crée une liste de tous les expéditeurs, destinataires et auteurs figurant dans les données collectées qui ont été ajoutées à la preuve. Veillez à examiner la liste pour déterminer s’il existe des utilisateurs externes. Pour plus d’informations sur l’utilisation de conditions pour limiter les résultats de recherche, consultez la rubrique [conditions de recherche](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-delete-the-spilled-data"></a>Étape 4: supprimer les données propagées

À l’aide de l’outil d’examen des données, vous pouvez supprimer des éléments de leur emplacement d’origine. Par exemple, vous pouvez supprimer des éléments de boîtes aux lettres, de sites SharePoint et de comptes OneDrive au sein de votre organisation. N’oubliez pas que, étant donné que vous avez collecté des éléments en tant que preuves (en ajoutant les résultats de la recherche à l’ensemble de preuves à l’étape 2), vous disposez de copies des éléments dans l’ensemble de preuves pour les examiner ou les conserver.

Pour supprimer des éléments de leur emplacement d’origine:

1. Dans l’ensemble de preuves, sélectionnez les éléments que vous souhaitez supprimer. Si vous sélectionnez des éléments joints à un message électronique, le message électronique parent est également sélectionné et supprimé. 
 
2. Cliquez sur **action** , puis sur **Supprimer les éléments des emplacements d’origine**.

   ![Cliquez sur action, puis sur supprimer les éléments des emplacements d’origine](../media/DataInvestigationsDeleteItems1.png)

3. Sur la page de menu volant, vérifiez le nombre d’éléments et les documents enfants associés qui seront supprimés, puis cliquez sur **supprimer**.

Pour l’instant, lorsque vous supprimez des éléments de leur emplacement d’origine, les éléments sont supprimés de manière récupérable. Cela signifie que les éléments supprimés seront conservés jusqu’à ce que la période de récupération des éléments supprimés de l’élément expire. Cela signifie également que les utilisateurs peuvent récupérer ces éléments. Pour plus d’informations sur ce qui se produit lorsque des éléments sont supprimés de boîtes aux lettres et de sites, consultez [la rubrique supprimer des éléments de leur emplacement d’origine](delete-items-from-original-locations.md).

## <a name="step-5-close-or-delete-the-investigation"></a>Étape 5: fermer ou supprimer l’enquête

Une fois que vous avez supprimé des documents dans les emplacements de contenu source (boîtes aux lettres ou sites) dans le service actif, vous disposez toujours de copies de ces documents que vous avez ajoutées à des preuves dans le cadre de votre enquête. Pour éviter d’autres enduits de données, vous devez envisager de supprimer l’enquête proprement dite.

Pour supprimer une enquête:

1. Dans l’onglet **paramètres** , cliquez sur informations sur l' **enquête**.

2. Cliquez sur **Supprimer l’enquête**. 

Si vous n’avez pas besoin de supprimer l’enquête ou si vous souhaitez enregistrer les informations que vous avez collectées pendant l’enquête, vous pouvez cliquer sur **Fermer le cas**. Ensuite, vous pouvez rouvrir des enquêtes fermées.
