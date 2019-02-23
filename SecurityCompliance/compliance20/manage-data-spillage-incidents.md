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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit l'utilisation de l'outil nouvelles enquêtes de données (aperçu) dans le centre de sécurité & de la sécurité d'Office 365 pour gérer un incident de fuite de données.
ms.openlocfilehash: 93cbbed8763f0af31ab8d4e32348f01bfda17a2a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218124"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Gérer un incident de fuite de données dans Microsoft 365 

Le débordement de données se fait lorsqu'un document confidentiel est publié dans un environnement non approuvé. Lors de la détection d'un incident de débordement de données, il est important d'évaluer rapidement la taille et les emplacements du détournement, d'examiner les activités de l'utilisateur et de purger définitivement les données propagées du système.

## <a name="scope-of-this-article"></a>Portée de cet article

Cet article fournit une liste d'instructions sur la suppression définitive d'éléments des boîtes aux lettres Office 365 de sorte qu'ils ne soient plus accessibles ou récupérables par les utilisateurs ou les administrateurs. 

> [!NOTE]
> Lorsque vous supprimez des éléments situés dans un site SharePoint ou OneDrive entreprise, ils sont conservés pendant 93 jours après leur suppression de leur emplacement d'origine.

## <a name="scenario"></a>Scénario

Vous êtes informé d'un incident de fuite de données dans lequel un employé a volontairement partagé un document hautement confidentiel avec plusieurs personnes par courrier électronique. Vous souhaitez évaluer rapidement qui a reçu ce document, à l'intérieur et à l'extérieur de votre organisation. Une fois que vous avez examiné l'incident, vous envisagez de partager vos découvertes avec d'autres investigateurs pour les examiner, puis de supprimer définitivement les données propagées d'Office 365. Une fois l'enquête terminée, vous souhaitez supprimer toutes les preuves. 

## <a name="workflow"></a>Flux de travail

Voici le flux de travail pour l'utilisation des enquêtes de données (préversion) pour gérer un incident de fuite de données:

1.  Créez une enquête sur les données.

2.  Recherchez les données déduites.

3.  Examinez et examinez l'incident.

4.  Supprimez définitivement les données déversées.

5.  Fermez ou supprimez l'enquête.


## <a name="before-you-begin"></a>Avant de commencer

- Vous utiliserez l'outil d'analyse des données (aperçu) dans le centre de conformité Office 365 Security & pour créer une enquête, rechercher les données propagées, puis les examiner et les analyser. Vous utiliserez ensuite le centre de sécurité & Compliance Center PowerShell pour supprimer définitivement les données déduites d'Office 365. 

- Pour créer une enquête, vous devez être membre du groupe de rôles Administrateur de conformité dans le centre de sécurité & Compliance Center.

- Pour supprimer des messages, vous devez être membre du groupe de rôles gestion de l'organisation dans le centre de sécurité & Compliance Center ou être affecté de la recherche et du rôle de purge. Pour plus d'informations sur l'ajout d'utilisateurs à un groupe de rôles, consultez [la rubrique accorder aux utilisateurs l'accès au centre de sécurité _AMP_ conformité](../grant-access-to-the-security-and-compliance-center.md). 

- Pour contrôler les boîtes aux lettres utilisateur et les comptes OneDrive qu'un enquêteur peut rechercher, votre organisation peut définir des limites de conformité. Pour plus d'informations, conFigurez [les limites de conformité pour les enquêtes de découverte électronique](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Étape 1: créer une enquête de données

Pour créer une enquête sur les données:

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le centre de sécurité & conformité, cliquez sur **analyses de données**.
 
4. Dans la page **enquêtes de données (aperçu)** , cliquez sur **créer une nouvelle enquête**.
    
5. Sur la page nouveau menu volant d'analyse des **données** , donnez un nom à l'enquête (obligatoire), puis tapez un numéro d'enquête facultatif et une description. Notez que le nom doit être unique dans votre organisation.

6. Sous **voulez-vous configurer des paramètres supplémentaires après avoir créé cette enquête?**, effectuez l'une des opérations suivantes:

    - Cliquez sur **Oui** pour créer l'enquête, puis affichez la page **paramètres** dans le nouvel incident. Cela vous permet d'ajouter des membres à l'enquête.
    
    - Cliquez sur **non** pour créer l'enquête et l'afficher dans la liste des incidents dans la page enquêtes sur les **données (aperçu)** . Si vous choisissez cette option, vous serez ajouté en tant que membre unique de l'enquête et les paramètres de recherche et d'analyse par défaut seront utilisés. Vous pouvez ajouter des membres ou modifier des paramètres à tout moment après la création de l'enquête.

7. Cliquez sur **Enregistrer** pour créer l'enquête.

    La nouvelle enquête est affichée dans la liste de la page enquêtes sur les **données (aperçu)** . 

8. Pour ouvrir une enquête, cliquez sur le nom de l'enquête. 

    L'onglet **Accueil** de l'enquête s'affiche. 

> [!TIP]
> Songez à établir une convention d'affectation de noms pour les enquêtes et fournissez autant d'informations que possible dans le nom et la description afin de pouvoir localiser et faire référence à ultérieurement si nécessaire.
 
## <a name="step-2-search-for-the-spilled-data"></a>Étape 2: Rechercher les données déversées 
 
Si vous identifiez les utilisateurs pour lesquels vous souhaitez rechercher des données déduites, vous pouvez les ajouter en tant que personnes intéressantes pour mapper leurs sources de données à l'enquête et effectuer rapidement des recherches dans leurs comptes de boîte aux lettres et OneDrive. Pour ajouter des personnes intéressantes pour l'enquête, cliquez sur **personnes intéressantes**, puis sur **Ajouter des personnes intéressantes**. 

Dans l'onglet **recherches** , vous pouvez créer des recherches pour trouver les données déversées. Vous allez utiliser la même requête de recherche que celle que vous avez utilisée pour trouver les données déversées afin de supprimer ces mêmes messages à l' [étape 4](##step-4:-permanently-delete-the-spilled-data). Pour plus d'informations sur la création de recherches, voir [créer une recherche pour collecter des données](create-search-to-collect-data.md).

Après avoir exécuté la recherche, vous pouvez prévisualiser des exemples de résultats de recherche et afficher des statistiques de recherche pour évaluer l'efficacité de votre requête de recherche. Une fois que vous avez identifié les éléments que vous souhaitez supprimer d'Office 365, vous pouvez cliquer sur l'onglet **incidents** , puis créer un incident et ajouter des résultats de recherche qui contiennent ces éléments. 

Pour ce faire, cliquez sur la recherche que vous souhaitez examiner. Sur la page de la fenêtre volante, cliquez sur **Ajouter les résultats à l'incident** et suivez les instructions. Ensuite, dans l'incident, vous pouvez passer en revue des documents individuels, examiner qui a eu accès aux documents et exporter les documents. Pour supprimer simplement les documents au lieu de les passer en revue, passez à l' [étape 4](##step-4:-permanently-delete-the-spilled-data). 

> [!IMPORTANT]
> Les mots clés que vous utilisez dans la requête de recherche peuvent contenir les données propagées réelles que vous recherchez. Par exemple, si vous recherchez des documents contenant un numéro de sécurité sociale et que vous l'utilisez comme mot clé dans la requête de recherche, vous devez supprimer la requête par la suite afin d'éviter toute aggravation. Vous pouvez supprimer la recherche ou supprimer l'intégralité de l'analyse à l' [étape 5](##step-5:-close-or-delete-investigation). 

## <a name="step-3-review-and-investigate"></a>Étape 3: vérifier et examiner 

Dans l'enquête, accédez à l'onglet **incidents** et cliquez sur l'incident que vous avez créé à l'étape précédente. Une fois le travail de traitement terminé et les résultats de la recherche ajoutés à l'incident, vous pouvez passer en revue les différents documents dans leur format natif, format texte ou quasi-natif. Vous pouvez créer des requêtes supplémentaires pour affiner la liste des documents et marquer des documents pour indiquer les conclusions de votre enquête.

Pour regrouper des documents et obtenir de l'aide supplémentaire pour votre révision, cliquez sur **gérer l'incident**. Dans la vignette **analyse** , cliquez sur **analyser**. Cette opération exécute des analyses avancées, telles que la détection des doublons, le Threading de messagerie électronique et l'analyse de thème. Pour plus d'informations, voir:

- [Détecter des quasi-duplicatas](near-duplicates.md)
- [Threading de messagerie](email-threading.md)
- [Thèmes](themes.md)

Pour déterminer les utilisateurs impliqués dans le débordement des données, vous pouvez créer une nouvelle requête dans l'incident, puis utiliser les conditions de l'expéditeur/auteur et des destinataires. Cette opération permet de créer une liste de tous les expéditeurs, destinataires et auteurs figurant dans les données collectées ajoutées à l'incident. Veillez à examiner la liste pour déterminer s'il existe des utilisateurs externes dans la liste. Pour plus d'informations, consultez la rubrique [conditions de recherche](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-permanently-delete-the-spilled-data"></a>Étape 4: supprimer définitivement les données déduites

### <a name="deleting-mailbox-items"></a>Suppression d'éléments de boîte aux lettres

Après avoir examiné et vérifié que les résultats de la recherche contiennent uniquement les messages électroniques qui doivent être supprimés, vous pouvez les supprimer définitivement en exécutant la commande **New-ComplianceSearchAction-purge-PurgeType permet HardDelete** dans Security & Compliance. Centre PowerShell. Pour obtenir des instructions, consultez la rubrique [Rechercher et supprimer des messages électroniques](../search-for-and-delete-messages-in-your-organization.md). 

Notez que si la récupération d'élément unique est activée pour les boîtes aux lettres de votre organisation, les éléments définitivement supprimés sont conservés dans le dossier éléments récupérables de l'utilisateur (et accessible par les administrateurs) jusqu'à la fin de la période de rétention des éléments supprimés (la valeur par défaut est 14 jours). De plus, si l'une des boîtes aux lettres contenant des données propagées est en conservation légale ou affectée à une stratégie de rétention, le message purgé est conservé dans le dossier éléments récupérables jusqu'à ce que la conservation soit supprimée ou que la boîte aux lettres soit exclue des stratégies de rétention. Pour supprimer définitivement les messages immédiatement, vous devez effectuer des tâches d'ajout. Pour obtenir des instructions, consultez [la rubrique supprimer des éléments dans le dossier éléments récupérables des boîtes aux lettres en nuage en conservation ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Vérifiez auprès de votre gestion des enregistrements ou de vos services juridiques avant de supprimer une stratégie de conservation ou de rétention. Votre organisation peut avoir une stratégie qui détermine si une boîte aux lettres en attente ou un incident de débordement de données est prioritaire. 

### <a name="deleting-site-items"></a>Suppression d'éléments de site

Pour supprimer définitivement un document d'un site SharePoint ou d'un compte OneDrive entreprise, vous devez le supprimer, puis le supprimer du site, puis le supprimer de la corbeille de la collection de sites. Pour obtenir des instructions, consultez la rubrique [supprimer des documents dans SharePoint et OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Vous pouvez également supprimer une collection de sites entière susceptible de contenir des données déplacées. Pour obtenir des instructions, consultez [la rubrique supprimer une collection de sites](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Étape 5: fermer ou supprimer l'enquête

Une fois que vous avez supprimé des documents dans les emplacements de contenu source (boîtes aux lettres ou sites), vous aurez toujours des copies de ces documents que vous avez ajoutées aux incidents dans le cadre de votre enquête. Pour éviter d'autres enduits de données, vous devez envisager de supprimer l'enquête.

Pour supprimer une enquête:

1. Dans l'onglet **paramètres** , cliquez sur informations sur l' **enquête**.

2. Cliquez sur **supprimer le cas**. 

Si vous n'avez pas besoin de supprimer l'enquête ou si vous souhaitez enregistrer les informations que vous avez collectées pendant l'enquête, vous pouvez cliquer sur **Fermer le cas**. À une date ultérieure, vous pouvez rouvrir les enquêtes terminées.