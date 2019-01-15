---
title: Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Découvrez où aller pour afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou équipes et comment effectuer une action sur ces fichiers.
ms.openlocfilehash: 435e1f449003f670f698c4e6813e18f5e83c498d
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014796"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams

[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation à partir des fichiers malveillants dans les bibliothèques de documents et des sites d’équipe. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour savoir comment afficher des informations sur les fichiers détectés et les actions à effectuer. 

Afin d’effectuer les tâches décrites dans cet article, vous devez disposer nécessaires [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Afficher les rapports avec des informations sur les fichiers détectés

Pour afficher l’état et des informations détaillées sur les fichiers qui ont été détectés par Office 365 DAV, vous pouvez utiliser le rapport d’état de Protection de menace.
  
1. Dans la [Office 365 sécurité &amp; centre de conformité](https://protection.office.com), cliquez sur **rapports** \> **tableau de bord** \> **État de Protection de menace**.
    
2. Dans le coin supérieur droit du rapport, cliquez sur **Afficher la table de détails**.
    
3. Afficher la liste des fichiers qui ont été détectés dans le rapport.
    
4. Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris les actions effectuées, le nom de fichier, le chemin d’accès du fichier et plus.
    
5. Sélectionnez l’onglet **Analyse avancée** pour afficher des informations, telles qu’observée comportement et analyse les détails. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Afficher et agir sur les fichiers de mise en quarantaine

1. De sécurité Office 365 &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **révision** \> **mise en quarantaine**.
    
2. Dans le coin supérieur gauche, modifiez le filtre de **courrier électronique** au **contenu**.
    
3. Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris l’URL du fichier.
    
4. Choisissez une action disponible.
    
  - Choisissez **version &amp; rapport** à débloquer le fichier. 
    
    Sélectionnez **Envoyer le rapport à Microsoft** à enregistrer le fichier comme un faux positif dans Microsoft. 
    
  - Cliquez sur **Télécharger le fichier** à étudier davantage le fichier. 
    
  - Cliquez sur **Supprimer** pour supprimer le fichier de la liste des éléments mis en quarantaine. Si vous choisissez cette option, vous devez également supprimer le fichier à partir de sa bibliothèque respectif dans SharePoint Online, OneDrive pour les professionnels ou Teams Microsoft. Cette option ne pas débloquer un fichier ouvert ou partagé. 
    
5. Cliquez sur **Fermer** pour fermer les détails d’un élément sélectionné. 
  
  

