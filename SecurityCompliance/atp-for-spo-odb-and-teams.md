---
title: Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Étendre Office 365 avancée protection contre les menaces de fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams pour permettre une collaboration plus sûre pour votre organisation.
ms.openlocfilehash: ea1c77273be70ce27f60bfaeae3544d605553a32
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528525"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft

Personnes régulièrement les fichiers de partager et collaborer à l’aide de SharePoint, OneDrive et Teams Microsoft. Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut collaborer de manière plus sûre. DAV permet de détecter et de bloquer les fichiers qui sont identifiés comme malveillants dans les sites d’équipe et des bibliothèques de documents. Lisez cet article pour obtenir une vue d’ensemble de DAV pour SharePoint Online, OneDrive pour les entreprises et Teams Microsoft, puis effectuer les étapes suivantes. 
  
> [!TIP]
> Pour effectuer les tâches décrites dans cet article, vous devez être un administrateur global d’Office 365 ou un administrateur de sécurité. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-it-works"></a>Fonctionnement

Lorsqu’un fichier dans SharePoint Online, OneDrive entreprise et Microsoft Teams a été identifié comme malveillants, DAV intègre directement les magasins de fichiers pour verrouiller ce fichier. L’image suivante montre un exemple d’un fichier malveillant détecté dans une bibliothèque.
  
[![Capture d’écran de fichiers dans OneDrive entreprise avec identifié comme malveillants](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Bien que les fichiers bloqués apparaît toujours dans la bibliothèque de documents et le web, les applications de bureau ou mobiles, les fichiers bloqués ne peut pas être ouvert, copié, déplacé ou partagé. Personnes peuvent, toutefois, supprimer un fichier bloqué. Voici un exemple de rôle qui ressemble à sur appareil mobile d’un utilisateur :
  
[![Capture d’écran de la suppression d’un fichier bloqué depuis OneDrive entreprise de l’application mobile OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Selon la configuration de Office 365, les personnes peuvent ou ne peut pas avoir la possibilité de télécharger un fichier bloqué. Voici ce que le téléchargement d’un fichier bloqué sur l’appareil mobile d’un utilisateur :
  
[![Capture d’écran de téléchargement d’un fichier bloqué dans OneDrive entreprise](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Pour plus d’informations, voir [activer Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](turn-on-atp-for-spo-odb-and-teams.md).
  
### <a name="keep-the-following-points-in-mind"></a>Gardez les points suivants à l’esprit

- DAV n’analyse pas chaque fichier dans SharePoint Online, OneDrive pour les professionnels ou Teams Microsoft. Il s’agit de par sa conception. Les fichiers sont analysés en mode asynchrone, via un processus qui utilise des événements d’activité partage et invité ainsi que heuristique actives et les signaux des menaces pour identifier les fichiers malveillants.
    
- Les fichiers qui sont identifiés comme malveillants dans SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams s’afficheront dans les [rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md) et dans l’Explorateur de menace (partie des [Informations sur les menaces Office 365](office-365-ti.md)).
    
- DAV fait partie de threat protection stratégie globale votre organisation, qui inclut anti-spam et protection anti-programme malveillant, ainsi que des liens fiables et pièces jointes fiables. Pour plus d’informations, consultez la rubrique [protection contre les menaces dans Office 365](protect-against-threats.md).
    
- Un administrateur SharePoint Online permettre déterminer s’il faut permettre aux utilisateurs de télécharger des fichiers qui sont détectés comme malveillants. Cette opération est effectuée en exécutant la cmdlet Set-SPOTenant PowerShell à l’aide d’un paramètre DisallowInfectedFileDownload (voir [activer Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](turn-on-atp-for-spo-odb-and-teams.md)).
    
## <a name="new-quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a>(Nouveau) ! Mise en quarantaine dans DAV pour SharePoint Online, OneDrive entreprise et les équipes Microsoft

 ** À partir de fin mai 2018, les fonctionnalités de [mise en quarantaine](quarantine-email-messages.md) dans la sécurité &amp; centre de conformité sont accordées à DAV pour SharePoint Online, OneDrive entreprise et Microsoft Teams. **
  
Lorsqu’un fichier dans SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams est identifiée comme malveillants, outre DAV bloquer le fichier ouvert ou partagé, ce fichier est inclus dans une liste d’éléments mis en quarantaine. (Dans la sécurité &amp; centre de conformité, accédez à la **Gestion des menaces** \> **révision** \> **mise en quarantaine** et filtrage de contenu.) 
  
Si vous faites partie de l’équipe de sécurité de votre organisation Office 365 et nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md), vous pouvez télécharger, version, rapport et supprimer des fichiers qui sont détectés comme malveillants par DAV à partir de la mise en quarantaine.
  
- **Création de rapports et de la libération** d’un fichier supprime le bloc de DAV sur le fichier dans la bibliothèque de documents ou site d’équipe respectifs pour SharePoint, OneDrive ou Teams Microsoft. Les utilisateurs peuvent ensuite ouvrir, partager et téléchargez le fichier. Et, lorsque l’option **Envoyer le rapport à Microsoft** est sélectionnée, le fichier est signalé comme un faux positif à Microsoft. 
    
- **Suppression d’un fichier** supprime le fichier de mise en quarantaine ; Toutefois, le fichier est toujours bloqué d’être ouvert ou partagé. Le fichier doit être supprimé dans son site respectifs document bibliothèque ou de l’équipe (SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams). 
    
- **Téléchargement d’un fichier** vous permet de télécharger et d’analyser le fichier pour n’importe quel nombre de faux positifs. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft](turn-on-atp-for-spo-odb-and-teams.md)
    
- [Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a>Voir aussi

[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  
[Afficher les rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md)
  
[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  
