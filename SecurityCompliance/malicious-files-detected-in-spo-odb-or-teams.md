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
ms.openlocfilehash: 370e5e3d4d7fd5f35caa8ef993f6245d15ee9999
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454271"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams

[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation à partir des fichiers malveillants dans les bibliothèques de documents et des sites d’équipe. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour savoir comment afficher des informations sur les fichiers détectés et les actions à effectuer. 

Afin d’effectuer les tâches décrites dans cet article, vous devez disposer nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Afficher les rapports avec des informations sur les fichiers détectés

Pour afficher l’état et des informations détaillées sur les fichiers qui ont été détectés par Office 365 DAV, vous pouvez utiliser le rapport d’état Threat protection.
  
1. De sécurité Office 365 &amp; centre de conformité, cliquez sur **rapports** \> **tableau de bord** \> **état de protection de menace**.
    
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
  
## <a name="related-topics"></a>Voir aussi

[Protection avancée contre les menaces dans Office 365](office-365-atp.md)
  
[Afficher les rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md)
  
[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)

[Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365](manage-quarantined-messages-and-files.md)
  

