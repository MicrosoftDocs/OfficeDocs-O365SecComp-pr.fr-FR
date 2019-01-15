---
title: Détection de virus dans SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 01/14/2019
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
ms.openlocfilehash: ab02d2d4e82e9427ec6b512490f94ccc9c14b54e
ms.sourcegitcommit: 5ccc3dd0d1c087bffd3a8fc807d5d1750f046eeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2019
ms.locfileid: "28009590"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="559f0-105">Détection de virus dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="559f0-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="559f0-p102">Office 365 peut aider à protéger votre environnement contre les logiciels malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent vers SharePoint Online. Les fichiers sont analysées après leur téléchargement. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier.</span><span class="sxs-lookup"><span data-stu-id="559f0-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="559f0-p103">Ces fonctionnalités antivirues dans SharePoint Online sont un moyen de contenir des virus. Ils ne sont pas destinés à un seul point de défense contre les programmes malveillants de votre environnement. Nous conseillons de tous les clients à évaluer et implémenter la protection contre les logiciels malveillants à différents niveaux et appliquer les meilleures pratiques pour la sécurisation de votre infrastructure d’entreprise. Pour plus d’informations sur les stratégies et les meilleures pratiques, voir [meilleures pratiques de sécurité pour Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="559f0-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="559f0-113">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="559f0-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="559f0-p104">Office 365 utilise un moteur de détection de virus courantes. Le moteur s’exécute de manière asynchrone dans SharePoint Online et analyse les fichiers après leur téléchargement. Lorsqu’un fichier est trouvé pour contenir un virus, elle est marquée afin qu’il ne peut pas être téléchargé à nouveau. Dans 2018 avril, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="559f0-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="559f0-118">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="559f0-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="559f0-119">Un utilisateur télécharge un fichier dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="559f0-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="559f0-120">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="559f0-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="559f0-121">Si un virus est détecté, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="559f0-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="559f0-122">Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="559f0-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="559f0-123">Si un fichier est infecté par un virus, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="559f0-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="559f0-124">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="559f0-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="559f0-125">Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="559f0-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="559f0-p105">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté. L’option pour télécharger le fichier et essayer de nettoyer à l’aide de son propre logiciel antivirus est proposée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="559f0-p105">The user is given a warning that a virus has been detected. The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="559f0-p106">Vous pouvez utiliser l’applet de commande Set-SPOTenant avec le paramètre **DisallowInfectedFileDownload** à ne pas autoriser les utilisateurs à télécharger un fichier détecté, même dans la fenêtre d’avertissement antivirus. Voir [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="559f0-p106">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window. See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="559f0-130">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="559f0-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="559f0-p107">Si les utilisateurs synchroniser des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive.exe) ou le précédent OneDrive client de synchronisation Business (Groove.exe), si un fichier contient un virus, le client de synchronisation ne le télécharger. Le client de synchronisation affiche une notification que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="559f0-p107">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

