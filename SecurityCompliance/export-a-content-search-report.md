---
title: Exporter un rapport de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/25/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Au lieu d’exporter les résultats d’une recherche de contenu de sécurité Office 365 réels &amp; centre de conformité, vous pouvez uniquement exporter un rapport de résultats de recherche. Le rapport contient un résumé des résultats de recherche et d’un document avec des informations détaillées sur chaque élément qui aurait à exporter.
ms.openlocfilehash: 45415f25754b4549a919e4ce56853a6ae09a9bdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527509"
---
# <a name="export-a-content-search-report"></a>Exporter un rapport de recherche de contenu

Au lieu de l’exportation de l’ensemble de la recherche des résultats à partir d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité (et à partir d’une recherche de contenu qui est associé à un cas de découverte électronique), vous pouvez uniquement exporter les mêmes rapports qui sont générées lorsque vous Exporter les résultats de recherche.
  
Lorsque vous exportez un état, il est téléchargé vers un dossier qui a le même nom que la recherche de contenu, mais qui est ajouté avec *_ReportsOnly* . Par exemple, si la recherche de contenu est nommée *ContosoCase0815* , le rapport est téléchargé vers un dossier nommé *ContosoCase0815_ReportsOnly* . Pour obtenir la liste de documents qui sont inclus dans le rapport, voir [ce qui est inclus dans le rapport](#whats-included-in-the-report).

## <a name="before-you-begin"></a>Avant de commencer

- Pour exporter un rapport de recherche de contenu, vous devez attribuer le rôle de gestion de recherche de la conformité de sécurité Office 365 &amp; centre de conformité. Ce rôle est attribué pour les groupes de rôles intégrés eDiscovery Manager et la gestion de l’organisation. Il n’est pas affecté par défaut au groupe de rôles de gestion de l’organisation. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
- Lorsque vous exportez un état, les données sont stockées temporairement dans une zone de stockage unique Windows Azure dans le nuage Microsoft avant qu’il est téléchargé sur votre ordinateur local. Vérifiez que votre organisation peut se connecter au point de terminaison dans Azure, qui est ** \*. blob.core.windows.net** (le caractère générique représente un identificateur unique pour votre exportation). Les données de résultats de recherche sont supprimées de la zone de stockage Azure deux semaines après sa création. 
    
- L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :
    
  - versions 32 ou 64 bits de Windows 7 et versions ultérieures
    
  - Microsoft .NET Framework 4.7
    
  - un navigateur pris en charge :
    
    - Microsoft Edge
    
      ou
    
    - Microsoft Internet Explorer 10 et versions ultérieures
    
    **Remarque :** Microsoft ne fabrique extensions tierces ou les modules complémentaires pour les applications ClickOnce. Exportation des résultats de recherche à l’aide d’un navigateur non pris en charge avec des extensions tierces ou les modules complémentaires n’est pas pris en charge. 
    
## <a name="generate-and-download-a-content-search-report"></a>Générer et télécharger un rapport de recherche de contenu

Les étapes pour générer et télécharger un rapport de recherche de contenu sont très similaires à effectuer l’exportation des résultats de recherche.
  
## <a name="step-1-generate-the-report-for-export"></a>Étape 1 : Générer le rapport pour l’exportation

La première étape consiste à préparer l’état pour le téléchargement de l’exportation de votre ordinateur. Lorsque vous le rapport, le rapport de documents sont téléchargés vers une zone de stockage Azure dans Microsoft cloud.
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.
    
4. Dans la page de **recherche de contenu** , sélectionnez une recherche. 
    
5. Dans le volet de détails, sous **Exporter le rapport à un ordinateur**, cliquez sur **Générer un rapport**.
    
    > [!NOTE]
    > Si les résultats d’une recherche datent de plus de 7 jours, vous êtes invité à mettre à jour les résultats de recherche. Dans ce cas, annuler l’exportation et cliquez sur **résultats de la recherche mise à jour** dans le volet de détails de la recherche sélectionnée, puis démarrer l’exportation de rapports une fois que les résultats sont mis à jour. 
  
6. Dans la page **Exporter un état** , sous **inclure ces éléments de la recherche**, choisissez une des options suivantes :
    
    - exporter uniquement les éléments indexés ;
    
    - exporter les éléments indexés et non indexés ;
    
    - exporter uniquement les éléments non indexés.
    
    Pour plus d’informations sur les éléments non indexées, voir [partiellement indexé des éléments de recherche de contenu](partially-indexed-items-in-content-search.md).
    
7. Choisir d’inclure les statistiques de recherche pour toutes les versions de documents SharePoint. Cette option apparaît uniquement si les sources de contenu de la recherche inclut les sites SharePoint ou OneDrive.
    
8. Cliquez sur **Générer un rapport**.
    
    Le rapport de résultats de recherche est préparé pour le téléchargement, ce qui signifie que les documents de rapport seront téléchargés dans la zone de stockage Azure dans le nuage de Microsoft. Lorsque le rapport est prêt pour le téléchargement, le lien **Télécharger le rapport** s’affiche sous **Exporter le rapport à un ordinateur** dans le volet détails. 
    
> [!NOTE]
> Vous pouvez aussi exporter un état pour une recherche de contenu qui est associé à une affaire eDiscovery. Pour ce faire, accédez à **recherche &amp; enquête** \> **eDiscovery**, sélectionnez un dossier, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Dans la page de **recherche** , sélectionnez une recherche, puis cliquez sur **Exporter** ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exporter un état**. 
  
## <a name="step-2-download-the-report"></a>Étape 2 : Télécharger le rapport

L’étape suivante consiste à télécharger le rapport à partir de la zone de stockage Azure sur votre ordinateur local.
  
1. Dans le volet de détails de la recherche que vous avez généré le rapport, sous **état sur un ordinateur de l’exportation**, cliquez sur **Télécharger le rapport**.
    
    La page de **téléchargement du rapport** s’affiche et contient des informations à propos du rapport jusqu'à être téléchargé sur votre ordinateur. 
    
    - Le nombre d’éléments à télécharger.
    
    - La taille totale estimée des éléments à télécharger.
    
    - Si indexés ou non indexés seront exportés. Éléments non indexées sont des éléments qui ont un format reconnu, qui sont chiffrées ou n’ont pas été indexés pour d’autres raisons.
    
    - Si les versions des documents SharePoint seront téléchargés.
    
    - L’état du processus d’exportation de rapport. Vous pouvez démarrer le téléchargement du rapport, même si la préparation de l’état n’est pas terminée.
    
2. **Exporter la clé**, cliquez sur **Copier dans le Presse-papiers**. Vous allez utiliser cette clé à l’étape 5 pour télécharger le rapport.
    
    > [!IMPORTANT]
    > Étant donné que tout le monde peut installer et démarrer l’outil d’exportation de découverte électronique et ensuite utiliser cette clé pour télécharger le rapport de recherche, veillez à prendre des précautions pour protéger cette clé comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité. 
  
3. Cliquez sur **Télécharger le rapport**.
    
4. Si vous êtes invité à installer **Microsoft Office 365 eDiscovery outil d’exportation**, cliquez sur **installer**.
    
5. Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. 
    
6. Cliquez sur **Parcourir** pour spécifier l’emplacement où vous souhaitez télécharger le rapport. 
    
7. Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur. 
    
    L' **outil d’exportation de découverte électronique** affiche les informations sur le processus d’exportation, y compris une estimation du nombre (et taille) des autres éléments à télécharger. Une fois le processus d’exportation terminée, vous pouvez accéder les fichiers à l’emplacement où ils ont été téléchargés. 
    
> [!NOTE]
> Vous pouvez télécharger le rapport pour une recherche de contenu qui est associé à une affaire eDiscovery. Pour ce faire, accédez à **recherche &amp; enquête** \> **eDiscovery**, sélectionnez un dossier, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Dans la page **exportation** , sélectionnez une exportation de rapport, puis cliquez sur **Télécharger le rapport** dans le volet détails. 
  
## <a name="whats-included-in-the-report"></a>Ce qui est inclus dans le rapport

Lorsque vous générez et exportez un rapport sur les résultats d’une recherche de contenu, les documents suivants sont téléchargés :
  
- **Exporter la synthèse** - document Microsoft Excel contenant un résumé de l’exportation. Cela inclut des informations telles que le nombre de sources de contenu qui ont été exclus, le nombre de résultats de recherche à partir de chaque emplacement de contenu, l’estimation du nombre d’éléments, le nombre d’éléments doit être exportés et la taille estimée et réelle des éléments qui doit être exporté. 
    
    > [!NOTE]
    > Si vous incluez des éléments non indexés lors de l’exportation du rapport, le nombre d’éléments non indexés est inclus dans le nombre total de résultats de la recherche estimés et le nombre total de résultats de recherche téléchargé (si vous n’avez pour exporter les résultats de recherche) qui sont répertoriés dans le Exporter le rapport de synthèse. En d’autres termes, le nombre total d’éléments qui doit être téléchargé est égal au nombre total de résultats de l’estimation et le nombre total d’éléments non indexés. 
  
- **Manifeste** - un fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de recherche. 
    
- **Résultats** - document Microsoft Excel qui contient une ligne avec des informations concernant chaque élément indexé qui doit être exporté avec les résultats de recherche. Pour le courrier électronique, le journal de résultat contient des informations sur chaque message, y compris : 
    
  - l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;
    
  - la date à laquelle le message a été envoyé ou reçu ;
    
  - l’objet du message ;
    
  - l’expéditeur et les destinataires du message.
    
    Pour les documents à partir de SharePoint et OneDrive pour les sites de l’entreprise, le journal de résultats contient des informations sur tous les documents, y compris :
    
  - l’URL du document ;
    
  - l’URL de la collection de sites qui héberge le document ;
    
  - la date à laquelle le document a été modifié pour la dernière fois ;
    
  - le nom du document (qui se trouve dans la colonne Objet du journal des résultats).
    
    > [!NOTE]
    > Le nombre de lignes dans le rapport de **résultats** doit être égal au nombre total de résultats de recherche doit être téléchargée moins le nombre total d’éléments répertoriés dans le rapport **d’Éléments non indexés** . 
  
- **Éléments non indexés** - document Microsoft Excel qui contient des informations sur tous les éléments non indexées doivent figurer dans les résultats de recherche. Si vous n’incluez pas les éléments non indexés lorsque vous générez le rapport de résultats de recherche, ce rapport est toujours téléchargé, mais sera vide.
