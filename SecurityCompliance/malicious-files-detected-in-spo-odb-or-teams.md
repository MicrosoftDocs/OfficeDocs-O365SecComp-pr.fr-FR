---
title: Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: Découvrez où aller pour afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou teams et comment effectuer des actions sur ces fichiers.
ms.openlocfilehash: f5304f78ddec884748dd7d1090e2a7895044d045
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259832"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams

[Office 365 ATP pour SharePoint, OneDrive et Microsoft](atp-for-spo-odb-and-teams.md) teams protège votre organisation contre les fichiers malveillants dans les bibliothèques de documents et les sites d'équipe. Lorsqu'un fichier malveillant est détecté, ce fichier est bloqué afin que personne ne puisse l'ouvrir, le copier, le déplacer ou le partager tant que d'autres actions ne sont pas effectuées par l'équipe de sécurité de l'organisation. Lisez cet article pour savoir comment afficher des informations sur les fichiers détectés et connaître les actions à effectuer. 

Pour effectuer les tâches décrites dans cet article, vous devez disposer des [autorisations nécessaires pour le centre de &amp; sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Affichage des rapports avec des informations sur les fichiers détectés

Pour afficher l'État et des informations détaillées sur les fichiers qui ont été détectés par la protection avancée contre les menaces d'Office 365, vous pouvez utiliser le rapport d'état de protection contre les menaces.
  
1. dans le [centre de sécurité &amp; conformité Office 365](https://protection.office.com), choisissez **rapports** \> **tableau de bord** \> de **Protection contre les menaces**.
    
2. Dans le coin supérieur droit du rapport, choisissez **afficher le tableau des détails**.
    
3. Affichez la liste des fichiers détectés dans le rapport.
    
4. Sélectionnez un élément dans la liste pour afficher des informations détaillées, notamment les actions prises, le nom de fichier, le chemin d'accès au fichier, et bien plus encore.
    
5. Choisissez l'onglet **analyse avancée** pour afficher des informations, telles que le comportement observé et les détails de l'analyse. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Afficher et effectuer des actions sur les fichiers en quarantaine

1. dans le centre de sécurité &amp; conformité d'Office 365, sélectionnez **gestion** \> des menaces- **vérification** \> de la **mise en quarantaine**.
    
2. Dans le coin supérieur gauche, modifiez le filtre de **courrier électronique** en **contenu**.
    
3. Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris l'URL du fichier.
    
4. Choisissez une action disponible.
    
  - Choisissez **Release &amp; Report** pour débloquer le fichier. 
    
    Sélectionnez **Envoyer le rapport à Microsoft** pour signaler le fichier comme faux positif à Microsoft. 
    
  - Choisissez **Télécharger un fichier** pour rechercher plus d'renseignements sur le fichier. 
    
  - Choisissez **supprimer** pour supprimer le fichier de la liste des éléments mis en quarantaine. Si vous choisissez cette option, vous devez également supprimer le fichier de sa bibliothèque respective dans SharePoint Online, OneDrive entreprise ou Microsoft Teams. Cette option ne débloque pas l'ouverture ou le partage d'un fichier. 
    
5. Cliquez sur **Fermer** pour fermer les détails d'un élément sélectionné. 
  
  

