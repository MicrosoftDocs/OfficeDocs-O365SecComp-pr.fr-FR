---
title: Exporter un rapport de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Au lieu d'exporter les résultats réels d'une recherche de contenu dans le centre &amp; de sécurité conformité Office 365, vous pouvez simplement exporter un rapport de résultats de recherche. Le rapport contient un résumé des résultats de la recherche et un document avec des informations détaillées sur chaque élément à exporter.
ms.openlocfilehash: 12799474bfb099c521f72cd3902173d42b17d4dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216234"
---
# <a name="export-a-content-search-report"></a>Exporter un rapport de recherche de contenu

Au lieu d'exporter l'ensemble complet des résultats de recherche à partir d'une recherche de contenu &amp; dans le centre de sécurité conformité Office 365 (et à partir d'une recherche de contenu associée à un cas eDiscovery), vous pouvez simplement exporter les mêmes rapports générés lorsque vous exporter les résultats de la recherche.
  
Lorsque vous exportez un État, il est téléchargé dans un dossier portant le même nom que la recherche de contenu, mais il est ajouté avec *_ReportsOnly* . Par exemple, si la recherche de contenu est nommée *ContosoCase0815* , le rapport est téléchargé dans un dossier nommé *ContosoCase0815_ReportsOnly* . Pour obtenir la liste des documents inclus dans le rapport, voir [ce qui est inclus dans le rapport](#whats-included-in-the-report).

## <a name="before-you-begin"></a>Avant de commencer

- Pour exporter un rapport de recherche de contenu, vous devez disposer du rôle de gestion de la recherche de conformité dans &amp; le centre de sécurité conformité Office 365. Ce rôle est affecté aux groupes de rôles du gestionnaire eDiscovery intégré et de la gestion de l'organisation. Il n'est pas affecté par défaut au groupe de rôles gestion de l'organisation. Pour plus d'informations, consultez [la rubrique attribution d'autorisations eDiscovery dans &amp; le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).
    
- Lorsque vous exportez un État, les données sont stockées temporairement dans une zone de stockage Windows Azure unique dans le Cloud Microsoft avant d'être téléchargée sur votre ordinateur local. assurez-vous que votre organisation peut se connecter au point de terminaison dans Azure, c'est-à-dire ** \*. blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation). Les données de résultats de recherche sont supprimées de la zone de stockage Azure deux semaines après sa création. 
    
- L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :
    
  - versions 32 ou 64 bits de Windows 7 et versions ultérieures
    
  - Microsoft .NET Framework 4,7
    
  - un navigateur pris en charge :
    
    - Microsoft Edge
    
      ou
    
    - Microsoft Internet Explorer 10 et versions ultérieures
    
    **Remarque:** Microsoft ne fabrique pas d'extensions ou de modules complémentaires tiers pour les applications ClickOnce. L'exportation des résultats de recherche à l'aide d'un navigateur non pris en charge avec des extensions ou des modules complémentaires tiers n'est pas prise en charge. 

- Si la taille totale estimée des résultats renvoyés par une recherche de contenu&nbsp;dépasse 20 to, l'exportation du rapport échoue. Pour réussir l'exportation du rapport, essayez de limiter l'étendue et de réexécuter la recherche de sorte que la taille estimée des résultats soit&nbsp;inférieure à 20 to.

- L'exportation de rapports de recherche de contenu compte sur le nombre maximal d'exportations en cours d'exécution en même temps et le nombre maximal d'exportations qu'un utilisateur unique peut exécuter. Pour plus d'informations sur les limites d'exportation, voir [Export content Search Results from the Office 365 Security _AMP_ Compliance Center](export-search-results.md#export-limits).

## <a name="generate-and-download-a-content-search-report"></a>Générer et télécharger un rapport de recherche de contenu

Les étapes de génération et de téléchargement d'un rapport de recherche de contenu sont très similaires à l'exportation des résultats de la recherche.
  
## <a name="step-1-generate-the-report-for-export"></a>Étape 1: générer le rapport pour l'exportation

La première étape consiste à préparer le rapport en vue de son téléchargement sur votre ordinateur. Lorsque vous le rapport, les documents de rapport sont téléchargés vers une zone de stockage Azure dans le Cloud Microsoft.
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Sur la page **recherche de contenu** , sélectionnez une recherche. 
    
5. Dans le volet d'informations, sous **Exporter le rapport vers un ordinateur**, cliquez sur **générer un rapport**.
    
    > [!NOTE]
    > Si les résultats d'une recherche sont antérieurs à 7 jours, vous êtes invité à mettre à jour les résultats de la recherche. Dans ce cas, annulez l'exportation, cliquez sur **mettre à jour les résultats** de la recherche dans le volet d'informations de la recherche sélectionnée, puis redémarrez l'exportation des rapports une fois les résultats mis à jour. 
  
6. Sur la page **exporter un rapport** , sous **inclure ces éléments de la recherche**, choisissez l'une des options suivantes:
    
    - exporter uniquement les éléments indexés ;
    
    - exporter les éléments indexés et non indexés ;
    
    - exporter uniquement les éléments non indexés.
    
    Pour plus d'informations sur les éléments non indexés, voir [éléments partiellement indexés dans la recherche de contenu](partially-indexed-items-in-content-search.md).
    
7. Choisissez d'inclure les statistiques de recherche pour toutes les versions des documents SharePoint. Cette option n'est disponible que si les sources de contenu de la recherche incluent des sites SharePoint ou OneDrive entreprise.
    
8. Cliquez sur **générer un rapport**.
    
    Le rapport de résultats de recherche est préparé pour le téléchargement, ce qui signifie que les documents de rapport seront téléchargés vers la zone de stockage Azure du Cloud Microsoft. Lorsque le rapport est prêt à être téléchargé, le lien **Télécharger le rapport** est affiché sous **Exporter le rapport vers un ordinateur** dans le volet d'informations. 
    
> [!NOTE]
> Vous pouvez également exporter un rapport pour une recherche de contenu associée à un cas de découverte électronique. Pour ce faire, accédez à **enquête &amp; ** \> de recherche **eDiscovery**, sélectionnez un cas, puis **** ![cliquez sur modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)l'icône modifier. Sur la **** ![page](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **recherches** , sélectionnez une recherche, puis cliquez sur Exporter les résultats de la recherche d'exportation **exporter un rapport**. 
  
## <a name="step-2-download-the-report"></a>Étape 2: Télécharger le rapport

L'étape suivante consiste à télécharger le rapport à partir de la zone de stockage Azure sur votre ordinateur local.
  
1. Dans le volet d'informations de la recherche pour laquelle vous avez généré le rapport, sous exporter le rapport **vers un ordinateur**, cliquez sur **Télécharger le rapport**.
    
    La page **Télécharger le rapport** s'affiche et contient les informations suivantes sur le rapport afin qu'il soit téléchargé sur votre ordinateur. 
    
    - Le nombre d’éléments à télécharger.
    
    - La taille totale estimée des éléments à télécharger.
    
    - Le fait que indexé ou non indexée sera exporté. Les éléments non indexés sont des éléments dont le format est reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons.
    
    - Si les versions des documents SharePoint seront téléchargés.
    
    - État du processus d'exportation des rapports. Vous pouvez commencer à télécharger le rapport même si la préparation du rapport n'est pas terminée.
    
2. Sous **Exporter la clé**, cliquez sur **copier dans le presse-papiers**. Vous utiliserez cette clé à l'étape 5 pour télécharger le rapport.
    
    > [!IMPORTANT]
    > Étant donné qu'une personne peut installer et démarrer l'outil d'exportation de découverte électronique, puis utiliser cette clé pour télécharger le rapport de recherche, veillez à protéger cette clé comme vous le feriez pour protéger les mots de passe ou d'autres informations relatives à la sécurité. 
  
3. Cliquez sur **Télécharger le rapport**.
    
4. Si vous êtes invité à installer l' **outil d'exportation de découverte électronique MicrosoftOffice 365**, cliquez sur **installer**.
    
5. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. 
    
6. Cliquez sur **Parcourir** pour spécifier l'emplacement où vous souhaitez télécharger le rapport. 
    
7. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d'exportation de découverte électronique** affiche des informations d'État sur le processus d'exportation, y compris une estimation du nombre (et de la taille) des éléments restants à télécharger. Une fois le processus d'exportation terminé, vous pouvez accéder aux fichiers à l'emplacement où ils ont été téléchargés. 
    
> [!NOTE]
> Vous pouvez télécharger le rapport pour une recherche de contenu associée à un cas de découverte électronique. Pour ce faire, accédez à **enquête &amp; ** \> de recherche **eDiscovery**, sélectionnez un cas, puis **** ![cliquez sur modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)l'icône modifier. Dans la page **exportations** , sélectionnez une exportation de rapport, puis cliquez sur **Télécharger le rapport** dans le volet d'informations. 
  
## <a name="whats-included-in-the-report"></a>Éléments inclus dans le rapport

Lorsque vous générez et exportez un rapport sur les résultats d'une recherche de contenu, les documents suivants sont téléchargés:
  
- **Exporter le résumé** : un document Excel qui contient un résumé de l'exportation. Cela inclut des informations telles que le nombre de sources de contenu qui ont été recherchées, le nombre de résultats de recherche à partir de chaque emplacement de contenu, le nombre estimé d'éléments, le nombre réel d'éléments qui seront exportés et la taille estimée et réelle des éléments qui seraient exportées. 
    
    > [!NOTE]
    > Si vous incluez des éléments non indexés lors de l'exportation du rapport, le nombre total d'éléments non indexés est inclus dans le nombre total de résultats de recherche estimés et dans le nombre total de résultats de recherche téléchargés (si vous deviez exporter les résultats de la recherche) répertoriés dans le Exporter un rapport de synthèse. En d'autres termes, le nombre total d'éléments qui seront téléchargés est égal au nombre total de résultats estimés et au nombre total d'éléments non indexés. 
  
- **Manifest** : fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche. 
    
- **Results** -un document Excel contenant une ligne avec des informations sur chaque élément indexé qui serait exporté avec les résultats de la recherche. Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, notamment: 
    
  - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
    
  - la date à laquelle le message a été envoyé ou reçu ;
    
  - l’objet du message ;
    
  - l’expéditeur et les destinataires du message.
    
    Pour les documents provenant de sites SharePoint et OneDrive entreprise, le journal des résultats contient des informations sur chaque document, notamment:
    
  - l’URL du document ;
    
  - l’URL de la collection de sites qui héberge le document ;
    
  - la date à laquelle le document a été modifié pour la dernière fois ;
    
  - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
    > [!NOTE]
    > Le nombre de lignes dans l'état des **résultats** doit être égal au nombre total de résultats de recherche qui seront téléchargés moins le nombre total d'éléments figurant dans le rapport des **éléments** non indexés. 
  
- **Éléments** non indexés: document Excel qui contient des informations sur les éléments non indexés qui seraient inclus dans les résultats de la recherche. Si vous n'incluez pas d'éléments non indexés lorsque vous générez le rapport des résultats de la recherche, ce rapport sera toujours téléchargé, mais il sera vide.
