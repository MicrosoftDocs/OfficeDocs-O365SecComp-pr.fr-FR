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
# <a name="virus-detection-in-sharepoint-online"></a>Détection de virus dans SharePoint Online

Office 365 peut aider à protéger votre environnement contre les logiciels malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent vers SharePoint Online. Les fichiers sont analysées après leur téléchargement. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier.
  
> [!IMPORTANT]
> Ces fonctionnalités antivirues dans SharePoint Online sont un moyen de contenir des virus. Ils ne sont pas destinés à un seul point de défense contre les programmes malveillants de votre environnement. Nous conseillons de tous les clients à évaluer et implémenter la protection contre les logiciels malveillants à différents niveaux et appliquer les meilleures pratiques pour la sécurisation de votre infrastructure d’entreprise. Pour plus d’informations sur les stratégies et les meilleures pratiques, voir [meilleures pratiques de sécurité pour Office 365](security-best-practices.md). 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?

Office 365 utilise un moteur de détection de virus courantes. Le moteur s’exécute de manière asynchrone dans SharePoint Online et analyse les fichiers après leur téléchargement. Lorsqu’un fichier est trouvé pour contenir un virus, elle est marquée afin qu’il ne peut pas être téléchargé à nouveau. Dans 2018 avril, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.
  
Voici ce qui se passe :
  
1. Un utilisateur télécharge un fichier dans SharePoint Online.
    
2. Le moteur de détection de virus analyse le fichier.
    
3. Si un virus est détecté, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?

Si un fichier est infecté par un virus, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide de l’Explorateur.
  
Voici ce qui se passe :
  
1. Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.
    
2. L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté. L’option pour télécharger le fichier et essayer de nettoyer à l’aide de son propre logiciel antivirus est proposée à l’utilisateur.

> [!NOTE]
> Vous pouvez utiliser l’applet de commande Set-SPOTenant avec le paramètre **DisallowInfectedFileDownload** à ne pas autoriser les utilisateurs à télécharger un fichier détecté, même dans la fenêtre d’avertissement antivirus. Voir [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?

Si les utilisateurs synchroniser des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive.exe) ou le précédent OneDrive client de synchronisation Business (Groove.exe), si un fichier contient un virus, le client de synchronisation ne le télécharger. Le client de synchronisation affiche une notification que le fichier ne peut pas être synchronisé.
  

