---
title: Office 365 - Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams.
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 11/08/2018
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
ms.collection:
- M365-security-compliance
description: Étendez la protection avancée contre les menaces Office 365 aux fichiers dans SharePoint Online, OneDrive entreprise et Microsoft teams pour activer la collaboration en toute sécurité pour votre organisation.
ms.openlocfilehash: d9d99041d002a6c43d7b6918f53aabb93f82339a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220604"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Office 365 - Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams.

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Vue d'ensemble de la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams

Les personnes partagent régulièrement des fichiers et collaborent à l'aide de SharePoint, de OneDrive et de Microsoft Teams. Avec [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), votre organisation peut collaborer de manière plus sûre. La protection avancée contre les menaces permet de détecter et de bloquer les fichiers identifiés comme étant malveillants dans les sites d'équipe et les bibliothèques de documents.  
  
## <a name="how-it-works"></a>Fonctionnement

Lorsqu'un fichier dans SharePoint Online, OneDrive entreprise et Microsoft teams a été identifié comme malveillant, la protection avancée contre les menaces s'intègre directement aux magasins de fichiers pour verrouiller ce fichier. L'image suivante montre un exemple de fichier malveillant détecté dans une bibliothèque.
  
[![Fichiers dans OneDrive entreprise avec un fichier détecté comme malveillant](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Bien que le fichier bloqué figure toujours dans la bibliothèque de documents et les applications Web, mobiles ou de bureau, le fichier bloqué ne peut pas être ouvert, copié, déplacé ou partagé. Toutefois, les utilisateurs peuvent supprimer un fichier bloqué. Voici un exemple de ce à quoi ressemble l'appareil mobile d'un utilisateur:
  
[![Suppression d'un fichier bloqué de OneDrive entreprise à partir de l'application mobile OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
En fonction de la configuration d'Office 365, les personnes peuvent ou non télécharger un fichier bloqué. Voici ce à quoi ressemble un fichier bloqué sur l'appareil mobile d'un utilisateur:
  
[![Téléchargement d'un fichier bloqué dans OneDrive entreprise](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Pour plus d'informations, reportez-vous à [activer l'ATP Office 365 pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md).
  
## <a name="keep-these-points-in-mind"></a>Gardez les points suivants à l'esprit

- La protection avancée contre les menaces n'analysera pas chaque fichier unique dans SharePoint Online, OneDrive entreprise ou Microsoft Teams. C'est par conception. Les fichiers sont analysés de manière asynchrone, par le biais d'un processus qui utilise des événements d'activité de partage et d'invité, ainsi que des signaux de menace et heuristiques pour identifier les fichiers malveillants.

- Assurez-vous que vos sites SharePoint sont configurés pour utiliser l' [expérience moderne](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). Lorsqu'un fichier est identifié comme malveillant et bloqué, les utilisateurs peuvent voir qu'il s'est produit dans l'expérience moderne, mais pas dans l'affichage classique. La protection contre l'ATP s'applique si l'expérience moderne ou la vue standard est utilisée; Toutefois, les indicateurs visuels signalant qu'un fichier est bloqué sont présents uniquement dans l'expérience moderne.
    
- Les fichiers identifiés comme étant malveillants dans SharePoint Online, OneDrive entreprise ou Microsoft teams s'afficheront dans des [rapports pour office 365 protection avancée contre les menaces](view-reports-for-atp.md) et dans l'Explorateur de menaces (partie d' [Office 365 Threat Intelligence](office-365-ti.md)).
    
- La fonctionnalité ATP fait partie de la stratégie globale de protection contre les menaces de votre organisation, qui inclut la protection contre le courrier indésirable et les programmes malveillants, ainsi que des liens fiables et des pièces jointes fiables. Pour en savoir plus, consultez la rubrique Protégez-vous [contre les menaces dans Office 365](protect-against-threats.md).
    
- Un administrateur SharePoint Online peut déterminer s'il faut autoriser les utilisateurs à télécharger des fichiers détectés comme malveillants. Pour ce faire, exécutez l'applet de commande PowerShell Set-SPOTenant à l'aide d'un paramètre DisallowInfectedFileDownload (voir [activer l'ATP Office 365 pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md)).
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a>Mise en quarantaine dans la protection avancée contre les menaces pour SharePoint Online, OneDrive entreprise et Microsoft teams

 À compter du 2018 mai, les fonctionnalités de [mise](quarantine-email-messages.md) en quarantaine &amp; dans le centre de sécurité conformité sont étendues à la protection avancée contre les menaces pour SharePoint Online, OneDrive entreprise et Microsoft Teams.
  
Lorsqu'un fichier dans SharePoint Online, OneDrive entreprise ou Microsoft teams est identifié comme malveillant, outre l'ATP empêche le fichier d'être ouvert ou partagé, ce fichier est inclus dans la liste des éléments mis en quarantaine. (Dans le centre &amp; de sécurité conformité, accédez à la **** \> **mise en quarantaine** et au filtre **du contenu**de la **gestion** \> des menaces.) 
  
Si vous faites partie de l'équipe de sécurité Office 365 de votre organisation et que vous disposez des [autorisations nécessaires dans le &amp; Centre de sécurité conformité d'Office 365](permissions-in-the-security-and-compliance-center.md), vous pouvez télécharger, publier, signaler et supprimer des fichiers détectés comme malveillants par la protection avancée contre les menaces. à partir de la quarantaine.
  
- Le fait de **libérer et de signaler** un fichier supprime le bloc ATP sur le fichier dans le site d'équipe ou la bibliothèque de documents respectif pour SharePoint, OneDrive ou Microsoft Teams. Les utilisateurs peuvent alors ouvrir, partager et télécharger le fichier. En cas de sélection de l'option **Envoyer un rapport à Microsoft** , le fichier est signalé comme faux positif pour Microsoft. 
    
- La **Suppression d'un fichier** supprime le fichier de la quarantaine; Toutefois, l'ouverture ou le partage du fichier est toujours bloqué. Le fichier doit également être supprimé dans sa bibliothèque de documents ou son site d'équipe respectif (SharePoint Online, OneDrive entreprise ou Microsoft Teams). 
    
- Le **téléchargement d'un fichier** vous permet de télécharger et d'analyser le fichier pour tous les faux positifs. 
    
## <a name="next-steps"></a>Étapes suivantes

1. [Activer la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md)
    
2. [Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams](malicious-files-detected-in-spo-odb-or-teams.md)
    
