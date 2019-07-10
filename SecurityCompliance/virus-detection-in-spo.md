---
title: Détection de virus dans SharePoint Online
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 01/14/2019
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Office 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online. Les fichiers sont analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.
ms.openlocfilehash: 8b15ac8e82082c2c6d940986d2018fa559835146
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598340"
---
# <a name="virus-detection-in-sharepoint-online"></a>Détection de virus dans SharePoint Online

Office 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online. Les fichiers sont analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.
  
> [!IMPORTANT]
> Ces fonctionnalités antivirus dans SharePoint Online sont un moyen de contenir des virus. Ils ne sont pas destinés à être utilisés comme point de défense unique contre les programmes malveillants pour votre environnement. Nous encourageons tous les clients à évaluer et à mettre en œuvre une protection contre les programmes malveillants à différentes couches et à appliquer les meilleures pratiques pour sécuriser votre infrastructure d’entreprise. Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez [les meilleures pratiques en matière de sécurité pour Office 365](security-best-practices.md). 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online?

Office 365 utilise un moteur de détection de virus courant. Le moteur s’exécute de façon asynchrone au sein de SharePoint Online et analyse les fichiers après leur chargement. Lorsqu’un fichier contient un virus, il est signalé de sorte qu’il ne puisse pas être téléchargé à nouveau. En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.
  
Voici ce qui se passe:
  
1. Un utilisateur télécharge un fichier vers SharePoint Online.
    
2. Le moteur de détection de virus analyse le fichier.
    
3. Si un virus est détecté, le moteur antivirus définit une propriété sur le fichier indiquant qu’il est infecté.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>Que se passe-t-il lorsqu’un utilisateur essaie de télécharger un fichier infecté à l’aide du navigateur?

Si un fichier est infecté par un virus, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide du navigateur.
  
Voici ce qui se passe:
  
1. Un utilisateur ouvre un navigateur Web et essaie de télécharger un fichier infecté à partir de SharePoint Online.
    
2. L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté. L’utilisateur a la possibilité de télécharger le fichier et d’essayer de le nettoyer à l’aide de son propre logiciel antivirus.

> [!NOTE]
> Vous pouvez utiliser la cmdlet Set-SPOTenant avec le paramètre **DisallowInfectedFileDownload** pour empêcher les utilisateurs de télécharger un fichier détecté, même dans la fenêtre d’avertissement antivirus. Consultez la rubrique [DisallowInfectedFileDownloadhttps://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)] (.
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté?

Que les utilisateurs synchronisent des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive. exe) ou le client de synchronisation OneDrive entreprise précédent (Groove. exe), si un fichier contient un virus, le client de synchronisation ne le télécharge pas. Le client de synchronisation affiche une notification indiquant que le fichier ne peut pas être synchronisé.
  

