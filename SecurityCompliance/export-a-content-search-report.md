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
# <a name="export-a-content-search-report"></a><span data-ttu-id="5a911-104">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="5a911-104">Export a Content Search report</span></span>

<span data-ttu-id="5a911-105">Au lieu de l’exportation de l’ensemble de la recherche des résultats à partir d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité (et à partir d’une recherche de contenu qui est associé à un cas de découverte électronique), vous pouvez uniquement exporter les mêmes rapports qui sont générées lorsque vous Exporter les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="5a911-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="5a911-p102">Lorsque vous exportez un état, il est téléchargé vers un dossier qui a le même nom que la recherche de contenu, mais qui est ajouté avec *_ReportsOnly* . Par exemple, si la recherche de contenu est nommée *ContosoCase0815* , le rapport est téléchargé vers un dossier nommé *ContosoCase0815_ReportsOnly* . Pour obtenir la liste de documents qui sont inclus dans le rapport, voir [ce qui est inclus dans le rapport](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="5a911-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5a911-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5a911-109">Before you begin</span></span>

- <span data-ttu-id="5a911-p103">Pour exporter un rapport de recherche de contenu, vous devez attribuer le rôle de gestion de recherche de la conformité de sécurité Office 365 &amp; centre de conformité. Ce rôle est attribué pour les groupes de rôles intégrés eDiscovery Manager et la gestion de l’organisation. Il n’est pas affecté par défaut au groupe de rôles de gestion de l’organisation. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5a911-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="5a911-p104">Lorsque vous exportez un état, les données sont stockées temporairement dans une zone de stockage unique Windows Azure dans le nuage Microsoft avant qu’il est téléchargé sur votre ordinateur local. Vérifiez que votre organisation peut se connecter au point de terminaison dans Azure, qui est \*\* \*. blob.core.windows.net\*\* (le caractère générique représente un identificateur unique pour votre exportation). Les données de résultats de recherche sont supprimées de la zone de stockage Azure deux semaines après sa création.</span><span class="sxs-lookup"><span data-stu-id="5a911-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="5a911-117">L’ordinateur que vous utilisez pour exporter les résultats de recherche doit répondre aux exigences système suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a911-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="5a911-118">versions 32 ou 64 bits de Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="5a911-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="5a911-119">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="5a911-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="5a911-120">un navigateur pris en charge :</span><span class="sxs-lookup"><span data-stu-id="5a911-120">A supported browser:</span></span>
    
    - <span data-ttu-id="5a911-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5a911-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="5a911-122">ou</span><span class="sxs-lookup"><span data-stu-id="5a911-122">or</span></span>
    
    - <span data-ttu-id="5a911-123">Microsoft Internet Explorer 10 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="5a911-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="5a911-p105">**Remarque :** Microsoft ne fabrique extensions tierces ou les modules complémentaires pour les applications ClickOnce. Exportation des résultats de recherche à l’aide d’un navigateur non pris en charge avec des extensions tierces ou les modules complémentaires n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5a911-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
    
## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="5a911-126">Générer et télécharger un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="5a911-126">Generate and download a Content Search report</span></span>

<span data-ttu-id="5a911-127">Les étapes pour générer et télécharger un rapport de recherche de contenu sont très similaires à effectuer l’exportation des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="5a911-127">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="5a911-128">Étape 1 : Générer le rapport pour l’exportation</span><span class="sxs-lookup"><span data-stu-id="5a911-128">Step 1: Generate the report for export</span></span>

<span data-ttu-id="5a911-p106">La première étape consiste à préparer l’état pour le téléchargement de l’exportation de votre ordinateur. Lorsque vous le rapport, le rapport de documents sont téléchargés vers une zone de stockage Azure dans Microsoft cloud.</span><span class="sxs-lookup"><span data-stu-id="5a911-p106">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="5a911-131">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="5a911-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="5a911-132">Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="5a911-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="5a911-133">Dans le volet gauche du Centre de sécurité et de conformité, cliquez sur **Recherches &amp; enquêtes** \> **Recherche de contenu**.</span><span class="sxs-lookup"><span data-stu-id="5a911-133">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="5a911-134">Dans la page de **recherche de contenu** , sélectionnez une recherche.</span><span class="sxs-lookup"><span data-stu-id="5a911-134">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="5a911-135">Dans le volet de détails, sous **Exporter le rapport à un ordinateur**, cliquez sur **Générer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="5a911-135">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5a911-p107">Si les résultats d’une recherche datent de plus de 7 jours, vous êtes invité à mettre à jour les résultats de recherche. Dans ce cas, annuler l’exportation et cliquez sur **résultats de la recherche mise à jour** dans le volet de détails de la recherche sélectionnée, puis démarrer l’exportation de rapports une fois que les résultats sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5a911-p107">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="5a911-138">Dans la page **Exporter un état** , sous **inclure ces éléments de la recherche**, choisissez une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a911-138">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="5a911-139">exporter uniquement les éléments indexés ;</span><span class="sxs-lookup"><span data-stu-id="5a911-139">Export only indexed items</span></span>
    
    - <span data-ttu-id="5a911-140">exporter les éléments indexés et non indexés ;</span><span class="sxs-lookup"><span data-stu-id="5a911-140">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="5a911-141">exporter uniquement les éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="5a911-141">Export only unindexed items</span></span>
    
    <span data-ttu-id="5a911-142">Pour plus d’informations sur les éléments non indexées, voir [partiellement indexé des éléments de recherche de contenu](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="5a911-142">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="5a911-p108">Choisir d’inclure les statistiques de recherche pour toutes les versions de documents SharePoint. Cette option apparaît uniquement si les sources de contenu de la recherche inclut les sites SharePoint ou OneDrive.</span><span class="sxs-lookup"><span data-stu-id="5a911-p108">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="5a911-145">Cliquez sur **Générer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="5a911-145">Click **Generate report**.</span></span>
    
    <span data-ttu-id="5a911-p109">Le rapport de résultats de recherche est préparé pour le téléchargement, ce qui signifie que les documents de rapport seront téléchargés dans la zone de stockage Azure dans le nuage de Microsoft. Lorsque le rapport est prêt pour le téléchargement, le lien **Télécharger le rapport** s’affiche sous **Exporter le rapport à un ordinateur** dans le volet détails.</span><span class="sxs-lookup"><span data-stu-id="5a911-p109">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5a911-p110">Vous pouvez aussi exporter un état pour une recherche de contenu qui est associé à une affaire eDiscovery. Pour ce faire, accédez à **recherche &amp; enquête** \> **eDiscovery**, sélectionnez un dossier, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Dans la page de **recherche** , sélectionnez une recherche, puis cliquez sur **Exporter** ![icône de résultats de recherche d’exportation](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exporter un état**.</span><span class="sxs-lookup"><span data-stu-id="5a911-p110">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="5a911-151">Étape 2 : Télécharger le rapport</span><span class="sxs-lookup"><span data-stu-id="5a911-151">Step 2: Download the report</span></span>

<span data-ttu-id="5a911-152">L’étape suivante consiste à télécharger le rapport à partir de la zone de stockage Azure sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5a911-152">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="5a911-153">Dans le volet de détails de la recherche que vous avez généré le rapport, sous **état sur un ordinateur de l’exportation**, cliquez sur **Télécharger le rapport**.</span><span class="sxs-lookup"><span data-stu-id="5a911-153">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="5a911-154">La page de **téléchargement du rapport** s’affiche et contient des informations à propos du rapport jusqu'à être téléchargé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5a911-154">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="5a911-155">Le nombre d’éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="5a911-155">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="5a911-156">La taille totale estimée des éléments à télécharger.</span><span class="sxs-lookup"><span data-stu-id="5a911-156">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="5a911-p111">Si indexés ou non indexés seront exportés. Éléments non indexées sont des éléments qui ont un format reconnu, qui sont chiffrées ou n’ont pas été indexés pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="5a911-p111">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="5a911-159">Si les versions des documents SharePoint seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="5a911-159">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="5a911-p112">L’état du processus d’exportation de rapport. Vous pouvez démarrer le téléchargement du rapport, même si la préparation de l’état n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="5a911-p112">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="5a911-p113">**Exporter la clé**, cliquez sur **Copier dans le Presse-papiers**. Vous allez utiliser cette clé à l’étape 5 pour télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="5a911-p113">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="5a911-164">Étant donné que tout le monde peut installer et démarrer l’outil d’exportation de découverte électronique et ensuite utiliser cette clé pour télécharger le rapport de recherche, veillez à prendre des précautions pour protéger cette clé comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="5a911-164">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="5a911-165">Cliquez sur **Télécharger le rapport**.</span><span class="sxs-lookup"><span data-stu-id="5a911-165">Click **Download report**.</span></span>
    
4. <span data-ttu-id="5a911-166">Si vous êtes invité à installer **Microsoft Office 365 eDiscovery outil d’exportation**, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="5a911-166">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="5a911-167">Dans l’**outil d’exportation de découverte électronique**, collez la clé d’exportation que vous avez copiée à l’étape 2 dans la zone appropriée. </span><span class="sxs-lookup"><span data-stu-id="5a911-167">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="5a911-168">Cliquez sur **Parcourir** pour spécifier l’emplacement où vous souhaitez télécharger le rapport.</span><span class="sxs-lookup"><span data-stu-id="5a911-168">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="5a911-169">Cliquez sur **Démarrer** pour télécharger les résultats de recherche sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5a911-169">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="5a911-p114">L' **outil d’exportation de découverte électronique** affiche les informations sur le processus d’exportation, y compris une estimation du nombre (et taille) des autres éléments à télécharger. Une fois le processus d’exportation terminée, vous pouvez accéder les fichiers à l’emplacement où ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="5a911-p114">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5a911-p115">Vous pouvez télécharger le rapport pour une recherche de contenu qui est associé à une affaire eDiscovery. Pour ce faire, accédez à **recherche &amp; enquête** \> **eDiscovery**, sélectionnez un dossier, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Dans la page **exportation** , sélectionnez une exportation de rapport, puis cliquez sur **Télécharger le rapport** dans le volet détails.</span><span class="sxs-lookup"><span data-stu-id="5a911-p115">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="5a911-175">Ce qui est inclus dans le rapport</span><span class="sxs-lookup"><span data-stu-id="5a911-175">What's included in the report</span></span>

<span data-ttu-id="5a911-176">Lorsque vous générez et exportez un rapport sur les résultats d’une recherche de contenu, les documents suivants sont téléchargés :</span><span class="sxs-lookup"><span data-stu-id="5a911-176">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="5a911-p116">**Exporter la synthèse** - document Microsoft Excel contenant un résumé de l’exportation. Cela inclut des informations telles que le nombre de sources de contenu qui ont été exclus, le nombre de résultats de recherche à partir de chaque emplacement de contenu, l’estimation du nombre d’éléments, le nombre d’éléments doit être exportés et la taille estimée et réelle des éléments qui doit être exporté.</span><span class="sxs-lookup"><span data-stu-id="5a911-p116">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="5a911-p117">Si vous incluez des éléments non indexés lors de l’exportation du rapport, le nombre d’éléments non indexés est inclus dans le nombre total de résultats de la recherche estimés et le nombre total de résultats de recherche téléchargé (si vous n’avez pour exporter les résultats de recherche) qui sont répertoriés dans le Exporter le rapport de synthèse. En d’autres termes, le nombre total d’éléments qui doit être téléchargé est égal au nombre total de résultats de l’estimation et le nombre total d’éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="5a911-p117">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="5a911-181">**Manifeste** - un fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="5a911-181">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="5a911-p118">**Résultats** - document Microsoft Excel qui contient une ligne avec des informations concernant chaque élément indexé qui doit être exporté avec les résultats de recherche. Pour le courrier électronique, le journal de résultat contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="5a911-p118">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="5a911-184">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="5a911-184">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="5a911-185">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="5a911-185">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="5a911-186">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="5a911-186">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="5a911-187">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="5a911-187">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="5a911-188">Pour les documents à partir de SharePoint et OneDrive pour les sites de l’entreprise, le journal de résultats contient des informations sur tous les documents, y compris :</span><span class="sxs-lookup"><span data-stu-id="5a911-188">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="5a911-189">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="5a911-189">The URL for the document.</span></span>
    
  - <span data-ttu-id="5a911-190">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="5a911-190">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="5a911-191">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="5a911-191">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="5a911-192">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="5a911-192">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5a911-193">Le nombre de lignes dans le rapport de **résultats** doit être égal au nombre total de résultats de recherche doit être téléchargée moins le nombre total d’éléments répertoriés dans le rapport **d’Éléments non indexés** .</span><span class="sxs-lookup"><span data-stu-id="5a911-193">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="5a911-p119">**Éléments non indexés** - document Microsoft Excel qui contient des informations sur tous les éléments non indexées doivent figurer dans les résultats de recherche. Si vous n’incluez pas les éléments non indexés lorsque vous générez le rapport de résultats de recherche, ce rapport est toujours téléchargé, mais sera vide.</span><span class="sxs-lookup"><span data-stu-id="5a911-p119">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
