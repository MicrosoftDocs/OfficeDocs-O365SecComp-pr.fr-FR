---
title: Détection de virus dans SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365 peut aider à protéger votre environnement contre les logiciels malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent vers SharePoint Online. Les fichiers sont analysées après leur téléchargement. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528358"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="a109f-105">Détection de virus dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a109f-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="a109f-p102">Office 365 peut aider à protéger votre environnement contre les logiciels malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent vers SharePoint Online. Les fichiers sont analysées après leur téléchargement. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier.</span><span class="sxs-lookup"><span data-stu-id="a109f-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a109f-p103">Ces fonctionnalités antivirues dans SharePoint Online sont un moyen de contenir des virus. Ils ne sont pas destinés à un seul point de défense contre les programmes malveillants de votre environnement. Nous conseillons de tous les clients à évaluer et implémenter la protection contre les logiciels malveillants à différents niveaux et appliquer les meilleures pratiques pour la sécurisation de votre infrastructure d’entreprise. Pour plus d’informations sur les stratégies et les meilleures pratiques, voir [meilleures pratiques de sécurité pour Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="a109f-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="a109f-113">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="a109f-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="a109f-p104">Office 365 utilise un moteur de détection de virus courantes. Le moteur s’exécute de manière asynchrone dans SharePoint Online et analyse les fichiers après leur téléchargement. Lorsqu’un fichier est trouvé pour contenir un virus, elle est marquée afin qu’il ne peut pas être téléchargé à nouveau. Dans 2018 avril, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="a109f-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="a109f-118">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="a109f-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="a109f-119">Un utilisateur télécharge un fichier dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a109f-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="a109f-120">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="a109f-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="a109f-121">Si un virus est détecté, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="a109f-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="a109f-122">Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="a109f-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="a109f-123">Si un fichier est infecté par un virus, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="a109f-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="a109f-124">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="a109f-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="a109f-125">Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a109f-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="a109f-126">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté et bénéficie de l’option pour télécharger le fichier et essayer de nettoyer à l’aide de son propre logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="a109f-126">The user is given a warning that a virus has been detected, and is given the option to download the file and attempt to clean it using their own virus software.</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="a109f-127">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="a109f-127">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="a109f-p105">Si les utilisateurs synchroniser des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive.exe) ou le précédent OneDrive client de synchronisation Business (Groove.exe), si un fichier contient un virus, le client de synchronisation ne le télécharger. Le client de synchronisation affiche une notification que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="a109f-p105">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

