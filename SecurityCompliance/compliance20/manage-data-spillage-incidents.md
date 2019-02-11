---
title: Gérer un incident débordements de données dans Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit l’utilisation du nouvel outil enquêtes (Preview) de données dans le centre de conformité de & sécurité pour Microsoft Office 365 pour gérer un incident débordements de données.
ms.openlocfilehash: d7adc17d01a0ae2ad6b7bfb7052862a5a6419882
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706175"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a>Gérer un incident débordements de données dans Microsoft 365 

Débordements de données est lorsque l’utilisateur relâche un document confidentiel dans un environnement non fiable. Lorsqu’un incident débordements de données est détecté, il est important évaluer rapidement la taille et l’emplacement de l’écoulement, examinez les activités utilisateur et puis vider définitivement les données dispersées à partir du système.

## <a name="scope-of-this-article"></a>Portée de cet article

Cet article fournit une liste d’instructions sur la façon de supprimer définitivement des éléments de boîtes aux lettres Office 365 afin qu’ils ne sont plus accessibles ou récupérables par les utilisateurs ou les administrateurs. 

> [!NOTE]
> Lorsque vous supprimez des éléments situés dans un SharePoint ou de OneDrive pour le site de l’entreprise, ils sont conservés pendant jours 93 depuis le moment où que vous les supprimer de leur emplacement d’origine.

## <a name="scenario"></a>Scénario

Vous êtes informés d’un incident débordements de données où un employé partagé sans le savoir un document confidentiel avec plusieurs personnes par courrier électronique. Vous voulez évaluer rapidement qui a reçu ce document, à l’intérieur et à l’extérieur de votre organisation. Une fois que vous avez examiner l’incident, que vous souhaitez partager vos résultats avec les autres investigateurs et passez en revue, puis supprimer définitivement les données dispersées à partir d’Office 365. Une fois l’enquête terminée, vous souhaitez supprimer tous les éléments de preuve. 

## <a name="workflow"></a>Flux de travail

Voici le flux de travail pour l’utilisation de données enquêtes (Preview) pour gérer un incident débordements de données :

1.  Créer une enquête de données.

2.  Recherchez les données dispersées.

3.  Passez en revue et examiner l’incident.

4.  Supprimer définitivement les données dispersées.

5.  Fermez ou supprimez l’enquête.


## <a name="before-you-begin"></a>Avant de commencer

- Vous allez utiliser l’outil de données enquêtes (Preview) dans le centre de conformité de & Office 365 sécurité pour créer une enquête, recherchez les données dispersées, passez en revue et analyser. Ensuite, vous allez utiliser sécurité & PowerShell du centre de conformité pour supprimer définitivement les données dispersées Office 365. 

- Pour créer une enquête, vous devez être membre du groupe de rôles d’administrateur de la conformité dans le centre de conformité de & sécurité.

- Pour supprimer des messages, vous devez être membre du groupe de rôles de gestion de l’organisation dans le centre de conformité de & sécurité ou attribuer le rôle de recherche et de Purge. Pour plus d’informations sur l’ajout d’utilisateurs à un groupe de rôles, voir [Autoriser les utilisateurs à la sécurité de & centre de conformité](../grant-access-to-the-security-and-compliance-center.md). 

- Pour contrôler les boîtes aux lettres utilisateur et les comptes de OneDrive un enquêteur peut effectuer des recherches, votre organisation peut définir des limites de conformité. Pour plus d’informations, voir [définir des limites de conformité pour les enquêtes eDiscovery](../set-up-compliance-boundaries.md). 

## <a name="step-1-create-a-data-investigation"></a>Étape 1 : Créer une enquête de données

Pour créer une enquête de données :

1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le centre de conformité & sécurité, cliquez sur **Données enquêtes**.
 
4. Dans la page **Données enquêtes (Preview)** , cliquez sur **créer une nouvelle enquête**.
    
5. Dans la page flottant **nouvelle enquête de données** , nommez l’enquête (requis), puis tapez un numéro d’enquête facultatif et une description. Notez que le nom doit être unique dans votre organisation.

6. Sous **vous souhaitez configurer des paramètres supplémentaires après avoir créé cette enquête ?**, effectuez l’une des opérations suivantes :

    - Cliquez sur **Oui** pour créer l’enquête et afficher la page **paramètres** dans le nouveau dossier. Cela vous permet d’ajouter des membres à l’enquête.
    
    - Cliquez sur **non** pour créer l’enquête simplement et les afficher dans la liste des incidents dans la page **Données enquêtes (Preview)** . Si vous choisissez cette option, vous sera ajoutée comme le seul membre de l’enquête et les paramètres de recherche et analytique par défaut sera utilisé. Vous pouvez ajouter des membres ou modifier les paramètres une fois l’enquête est créée.

7. Cliquez sur **Enregistrer** pour créer l’enquête.

    La nouvelle enquête est affichée dans la liste dans la page **Données enquêtes (Preview)** . 

8. Pour ouvrir une enquête, cliquez sur le nom de l’enquête. 

    L’onglet **accueil** pour l’enquête est affiché. 

> [!TIP]
> Envisagez d’établir une convention d’affectation de noms pour les enquêtes et fournir autant d’informations que possible dans le nom et la description afin de localiser et de faire ultérieurement si nécessaire.
 
## <a name="step-2-search-for-the-spilled-data"></a>Étape 2 : Recherche des données dispersées 
 
Si vous connaissez les utilisateurs que vous souhaitez rechercher des données dispersées, vous pouvez les ajouter en tant que personnes dignes d’intérêt pour mapper des sources de données à l’enquête et rechercher rapidement leurs boîtes aux lettres et le compte OneDrive. Pour ajouter des personnes dignes d’intérêt pour l’enquête, cliquez sur **personnes dignes d’intérêt**, puis cliquez sur **Ajouter des personnes dignes d’intérêt**. 

Sous l’onglet de **recherche** , vous pouvez créer des recherches pour trouver les données dispersées. Vous allez utiliser la même requête de recherche qui vous permet de trouver les données dispersées à supprimer ces messages même à [l’étape 4](##step-4:-permanently-delete-the-spilled-data). Pour plus d’informations sur la création de recherches, voir [créer une recherche pour recueillir des données](create-search-to-collect-data.md).

Après avoir exécuté la recherche, vous pouvez afficher un aperçu des exemples de résultats de la recherche et afficher les statistiques de recherche pour évaluer l’efficacité de votre requête de recherche. Une fois que vous identifiez les éléments que vous voulez supprimer d’Office 365, vous pouvez cliquez sur l’onglet **Incidents** et puis créer un incident et ajouter les résultats de recherche qui contient ces éléments. 

Pour ce faire, cliquez sur la recherche que vous souhaitez examiner. Dans la page mobile, cliquez sur **Ajouter les résultats à un incident** , suivez les instructions. Puis dans l’incident, passez en revue les documents individuels, examinez qui a accès à des documents et exporter les documents. Pour supprimer les documents au lieu de les revoir, accédez à [l’étape 4](##step-4:-permanently-delete-the-spilled-data). 

> [!IMPORTANT]
> Les mots clés que vous utilisez dans la requête de recherche peuvent contenir des données réelles dispersées que vous recherchez. Par exemple, si vous recherchez des documents contenant un numéro de sécurité sociale et que vous l’utilisez en tant qu’un mot clé dans la requête de recherche, vous devez supprimer la requête par la suite pour éviter de débordements. Vous pouvez supprimer recherche ou l’enquête entière à [l’étape 5](##step-5:-close-or-delete-investigation). 

## <a name="step-3-review-and-investigate"></a>Étape 3 : Passez en revue et recherchez 

Lors de l’enquête, accédez à l’onglet **Incidents** et cliquez sur l’incident que vous avez créé à l’étape précédente. Une fois la tâche de traitement est terminée et les résultats de recherche sont ajoutés à l’incident, vous pouvez consulter des documents individuels dans leur format natif, format de texte ou un format près. Vous pouvez créer des requêtes supplémentaires pour affiner la liste des documents et des documents de balise pour indiquer les résultats de votre recherche.

Pour regrouper les documents et obtenir une assistance supplémentaire pour révision, cliquez sur **Gérer les incidents**. Dans la fenêtre **Analytique** , cliquez sur **analyser**. Cela s’exécutera analytique avancées telles que la détection des doublons, messagerie threading et l’analyse du thème. Pour plus d’informations, voir :

- [Détecter des quasi-duplicatas](near-duplicates.md)
- [Threading de messagerie](email-threading.md)
- [Thèmes](themes.md)

Pour déterminer les utilisateurs qui sont impliqués dans les débordements de données, vous pouvez créer une nouvelle requête dans l’incident et utiliser ensuite l’expéditeur/auteur et les conditions de destinataires. Cela créera une liste de tous les expéditeurs, les destinataires et les auteurs de données collectées qui a été ajoutées à l’incident. Veillez à examiner la liste pour déterminer si des utilisateurs externes sont dans la liste. Pour plus d’informations, voir [conditions de recherche](../keyword-queries-and-search-conditions.md#search-conditions).

## <a name="step-4-permanently-delete-the-spilled-data"></a>Étape 4 : Supprimer définitivement les données dispersées

### <a name="deleting-mailbox-items"></a>Suppression d’éléments de boîte aux lettres

Une fois que vous passez en revue et validez que les résultats de recherche contiennent uniquement les messages électroniques qui doivent être supprimés, vous pouvez les supprimer définitivement en exécutant la **New-ComplianceSearchAction-purger - PurgeType HardDelete** commande sécurité & la conformité Centre PowerShell. Pour plus d’informations, voir [Rechercher et supprimer les messages électroniques](../search-for-and-delete-messages-in-your-organization.md). 

Notez que si la récupération d’élément unique est activée pour les boîtes aux lettres dans votre organisation, les éléments supprimés définitivement seront conservés dans le dossier éléments récupérables de l’utilisateur (et accessibles par les administrateurs) jusqu'à ce que la période de rétention éléments supprimés (valeur par défaut est 14 jours). En outre, si une des boîtes aux lettres qui contiennent des données dispersées sont soumis à une suspension légale ou affectés à une stratégie de rétention, message purgé est conservé dans le dossier éléments récupérables jusqu'à ce que le blocage est supprimé ou de la boîte aux lettres est exclu de stratégies de rétention. Pour les messages de suppression définitive immédiatement, vous devez effectuer les tâches d’ajout. Pour plus d’informations, voir [Supprimer des éléments dans les éléments récupérables dossier de boîtes aux lettres en nuage sur contenir ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).  

> [!IMPORTANT]
> Renseignez-vous auprès de votre gestion des enregistrements ou les services juridiques avant la suppression d’une stratégie de blocage ou de rétention. Votre organisation peut avoir une stratégie qui définit si une boîte aux lettres sur blocage ou un incident débordements de données est prioritaire. 

### <a name="deleting-site-items"></a>Suppression d’éléments de site

Pour supprimer définitivement un document à partir d’un site SharePoint ou un OneDrive pour un compte professionnel, vous devez supprimer et vous devrez supprimer à partir du site, puis supprimez-le de la Corbeille de la collection de sites. Pour obtenir des instructions, consultez la rubrique [Supprimer des documents dans SharePoint et OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).

Vous pouvez également supprimer une collection de sites contenant des données dispersées. Pour plus d’informations, voir [suppression d’une collection de sites](https://docs.microsoft.com/sharepoint/delete-site-collection).

## <a name="step-5-close-or-delete-the-investigation"></a>Étape 5 : Fermer ou de supprimer l’enquête

Après la suppression de documents dans les emplacements de contenu source (boîtes aux lettres ou des sites), vous aurez toujours des copies de ces documents que vous avez ajouté aux incidents dans le cadre de votre enquête. Pour éviter d’autres débordements de données, vous devez envisager la suppression de l’enquête.

Pour supprimer une enquête :

1. Sous l’onglet **paramètres** , cliquez sur **informations de l’enquête**.

2. Cliquez sur **Supprimer le cas**. 

Si vous n’avez pas besoin de supprimer l’enquête ou si vous souhaitez enregistrer les informations que vous avez collectées lors de l’enquête, vous pouvez cliquer sur **Fermer le cas**. Ultérieurement, vous pouvez rouvrir enquêtes fermés.