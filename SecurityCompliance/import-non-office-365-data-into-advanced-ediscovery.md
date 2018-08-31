---
title: Importer du contenu Office 365 pour l’analyse de découverte électronique avancées
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Comment les étapes pour importer du contenu qui n’est pas stocké dans O365 dans un Azure blob afin qu’il peut être analysé avec AeD
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528766"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="fee73-103">Importer du contenu Office 365 pour l’analyse de découverte électronique avancées</span><span class="sxs-lookup"><span data-stu-id="fee73-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="fee73-p101">Pas de tous les documents que vous devrez peut-être analyser avec Office 365 avancée de découverte électronique résidera dans Office 365. Avec le contenu Non-Office 365 importer la fonctionnalité eDiscovery avancé, que vous pouvez télécharger des documents qui ne live dans Office 365 (à l’exception des fichiers PST) dans un objet blob cas stockage Azure liées et les analyser avec eDiscovery avancée. Cette procédure indique comment intégrer vos documents non Office 365 à eDiscovery avancée pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fee73-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fee73-p102">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="fee73-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fee73-p103">Vous pouvez acheter un abonnement de module complémentaire Office 365 avancée eDiscovery données stockage pour le contenu d’Office 365. Il s’agit exclusivement disponible pour le contenu qui doit être analysées avec eDiscovery avancée. Suivez les étapes décrites dans [acheter ou de modifier et de module complémentaire pour Office 365 pour professionnels](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) et acheter Office 365 avancée eDiscovery stockage module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="fee73-p103">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content. This is exclusively available for content that is to be analyzed with Advanced eDiscovery. Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="fee73-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fee73-112">Before you begin</span></span>

<span data-ttu-id="fee73-113">À l’aide de la fonctionnalité de téléchargement Non-Office 365 comme décrit dans cette procédure suppose que :</span><span class="sxs-lookup"><span data-stu-id="fee73-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="fee73-114">Un Office 365 E3 avec le module complémentaire de conformité avancée ou abonnement E5</span><span class="sxs-lookup"><span data-stu-id="fee73-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="fee73-115">Tous les dépositaires non Office 365 dont le contenu sera téléchargé doivent avoir E3 avec le module complémentaire de conformité avancée ou licences E5</span><span class="sxs-lookup"><span data-stu-id="fee73-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="fee73-116">Un cas de découverte électronique existant</span><span class="sxs-lookup"><span data-stu-id="fee73-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="fee73-p104">Tous les fichiers de téléchargement regroupés dans les dossiers où il existe un dossier par dépositaire et nom des dossiers dans ce format *alias@domainname* . *alias@domainname* doit être domaine et l’alias d’utilisateurs Office 365. Vous pouvez regrouper tous les dossiers *alias@domainname* dans un dossier racine. Le dossier racine ne peut contenir les dossiers *alias@domainname* , il ne doit exister aucun fichier libre dans le dossier racine</span><span class="sxs-lookup"><span data-stu-id="fee73-p104">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  . The  *alias@domainname*  must be users Office 365 alias and domain. You can collect all the  *alias@domainname*  folders into a root folder. The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="fee73-121">Un compte qui est un gestionnaire eDiscovery ou un administrateur d’eDiscovery</span><span class="sxs-lookup"><span data-stu-id="fee73-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="fee73-122">[Outils de stockage Microsoft Azure](https://aka.ms/downloadazcopy) installé sur un ordinateur ayant accès à la structure de dossier contenu Office 365.</span><span class="sxs-lookup"><span data-stu-id="fee73-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="fee73-123">Télécharger du contenu d’Office 365 en découverte avancée</span><span class="sxs-lookup"><span data-stu-id="fee73-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="fee73-p105">En tant qu’un gestionnaire eDiscovery ou eDiscovery administrateur, ouvrez **eDiscovery**, puis le cas pour les données non Office 365 seront téléchargées. Si vous avez besoin créer un cas, voir [gérer des affaires eDiscovery de sécurité Office 365 &amp; centre de conformité](manage-ediscovery-cases.md)</span><span class="sxs-lookup"><span data-stu-id="fee73-p105">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to. If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="fee73-126">Cliquez sur **Basculer vers eDiscovery avancée**</span><span class="sxs-lookup"><span data-stu-id="fee73-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="fee73-127">Sous **type de Source** , sélectionnez **données Non-Office 365**.</span><span class="sxs-lookup"><span data-stu-id="fee73-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="fee73-p106">Cliquez sur **Ajouter conteneur**. Nommez le conteneur et ajouter une description.</span><span class="sxs-lookup"><span data-stu-id="fee73-p106">Click **Add container**. Name the container and add a description.</span></span>
    
5. <span data-ttu-id="fee73-130">Sélectionnez le conteneur nouvellement ajouté à partir de la liste du conteneur et copiez l’URL qui s’affiche dans le volet de détails du conteneur, puis fermez le volet</span><span class="sxs-lookup"><span data-stu-id="fee73-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="fee73-131">Ouvrez une invite de commandes en tant qu’administrateur et accédez au répertoire au dossier où vous avez installé des AzCopy...</span><span class="sxs-lookup"><span data-stu-id="fee73-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="fee73-132">Construire la ligne de commande AzCopy pour télécharger les fichiers comme suit :</span><span class="sxs-lookup"><span data-stu-id="fee73-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="fee73-p107">AzCopy /Source : « *chemin d’accès complet au dossier racine sur l’ordinateur local* » /Dest : » *URL conteneur jusqu'à, mais non compris la ?* » /DestSAS : » *reste de l’url de conteneur à partir de la ? à la fin* « / S.</span><span class="sxs-lookup"><span data-stu-id="fee73-p107">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*  " /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="fee73-135">Par exemple, à l’aide de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="fee73-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="fee73-136">dossier racine - données C:\Collected</span><span class="sxs-lookup"><span data-stu-id="fee73-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="fee73-137">url du conteneur - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;PPS = NonOfficeData15 %7 C 0&amp;sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA % 3D</span><span class="sxs-lookup"><span data-stu-id="fee73-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="fee73-138">la syntaxe de ligne de commande AzCopy serait :</span><span class="sxs-lookup"><span data-stu-id="fee73-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="fee73-139">Pour plus d’informations sur Azcopy syntaxe voir, [transférer des données avec l’AzCopy sur Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span><span class="sxs-lookup"><span data-stu-id="fee73-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="fee73-140">Il doit y avoir un seul dossier racine par utilisateur et le nom du dossier doit être au format *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="fee73-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="fee73-p108">Une fois les dossiers de téléchargement, revenez au eDiscovery avancée. Le contenu dans les dossiers que vous avez téléchargé est maintenant prêt à être traitée dans eDiscovery avancée. Sélectionnez le conteneur, cliquez sur le bouton de processus. Pour plus d’informations sur la découverte électronique avancée traitement voir, [exécutez le module de processus et charger des données dans Office 365 avancée de découverte électronique](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="fee73-p108">Once the folders have finished uploading, switch back to Advanced eDiscovery. The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery. Select the container and click the Process button. For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="fee73-p109">Une fois le conteneur est correctement traité d’eDiscovery avancé, vous serez n’est plus en mesure d’ajouter du contenu à l’espace de stockage SAS dans Azure. Si vous collectez contenu supplémentaire et que vous souhaitez ajouter à la casse pour l’analyse de découverte électronique avancé, vous devez créer un nouveau conteneur de **données Non-Office 365** et répétez cette procédure.</span><span class="sxs-lookup"><span data-stu-id="fee73-p109">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure. If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="fee73-147">Si le conteneur *ne traite pas correctement en raison de problèmes d’attribution de noms de dossiers* et résoudre les problèmes, vous devez toujours créer un nouveau conteneur et la reconnexion et télécharger en utilisant les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="fee73-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span> 
  

