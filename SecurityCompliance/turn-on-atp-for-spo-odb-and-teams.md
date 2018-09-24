---
title: Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft
ms.author: derng
author: derng
manager: laurawi
ms.date: 5/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Découvrez comment activer DAV pour SharePoint, OneDrive et les équipes, notamment comment définir des alertes pour les fichiers détectés.
ms.openlocfilehash: bb99aee0887f15f065a47d691c59ce47639bdc32
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972236"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft

[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation de partager des fichiers malveillants par inadvertance. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour activer DAV pour SharePoint, OneDrive et les équipes, définir des alertes pour être averti des fichiers détectés et effectuer les étapes suivantes. 
  
> [!TIP]
> Afin d’effectuer les tâches décrites dans cet article, vous devez disposer des autorisations nécessaires affectées dans Office 365 et de la sécurité &amp; centre de conformité.
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Activer ATP pour SharePoint, OneDrive et Microsoft Teams

 **Avant de commencer cette procédure, assurez-vous que l’enregistrement d’audit est déjà activé pour votre environnement Office 365**. Cela s’effectue généralement par toute personne ayant le rôle journaux d’Audit affecté dans Exchange Online. Pour plus d’informations, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).
  
1. En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com), puis connectez-vous avec votre compte professionnel ou de l’école.
    
2. De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Pièces jointes fiables**.
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> stratégie](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. Sélectionnez **Activer DAV pour SharePoint, OneDrive et les équipes Microsoft**.
    
    ![Activer la protection contre les menaces avancée pour SharePoint Online, OneDrive entreprise et les équipes Microsoft](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. Cliquez sur **Enregistrer**.
    
5. Passez en revue (et, selon le cas, modifier) [des stratégies de pièces jointes fiables](set-up-atp-safe-attachments-policies.md) et des [stratégies de liens fiables](set-up-atp-safe-links-policies.md)de votre organisation.
    
6. (Recommandé) En tant qu’administrateur global ou un administrateur SharePoint Online, exécutez l’applet de commande **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** la valeur *true* . <br/><br/>Le paramètre *true* blocs toutes les actions (à l’exception de la suppression) pour les fichiers détectés. Personnes ne peut pas ouvrir, déplacer, copier ou partager des fichiers détectés.<br/><br/>Définition du paramètre sur *false* bloque toutes les actions à l’exception de suppression et le téléchargement. Personnes peuvent choisir d’accepter le risque et télécharger un fichier détecté.<br/><br/>Nous vous recommandons de définir le paramètre sur *true*. 
   
7. Autoriser jusqu'à 30 minutes pour que vos modifications à répartir pour tous les centres de données Office 365.
    
8. (Recommandé) Passez à définir des alertes pour les fichiers détectés.
    
> [!TIP]
> Pour plus d’informations sur l’utilisation de PowerShell avec Office 365, voir [Gestion d’Office 365 avec PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, consultez la rubrique [que faire lorsqu’un fichier malveillant est détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2). 
  
## <a name="set-up-alerts-for-detected-files"></a>Définir des alertes pour les fichiers détectés

Pour recevoir une notification lorsqu’un fichier dans SharePoint Online, OneDrive pour les professionnels ou Microsoft Teams a été identifié comme malveillant, vous pouvez configurer une alerte.
  
1. De sécurité Office 365 &amp; centre de conformité, sélectionnez **alertes** \> **Gérer les alertes**.
    
2. Choisissez **nouvelle stratégie de l’alerte**.
    
3. Spécifiez un nom pour l’alerte. Par exemple, vous pouvez taper des fichiers malveillants dans des bibliothèques.
    
4. Tapez une description de l’alerte. Par exemple, vous pouvez taper notifie administrateurs lorsque des fichiers malveillants sont détectées dans SharePoint Online, OneDrive ou Teams Microsoft.
    
5. Dans la section **Envoyer cette alerte lorsque...** , procédez comme suit : 
    
  - Dans la liste des **activités** , choisissez **malveillant détecté dans le fichier**.
    
  - Laissez le champ **utilisateurs** vide. 
    
6. Dans la section **Envoyer cette alerte...** , sélectionnez un ou plusieurs administrateurs globaux, les administrateurs de sécurité ou les lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté. 
    
7. Cliquez sur **Enregistrer**.
    
> [!TIP]
> Pour plus d’informations sur les alertes, voir [créer des alertes de l’activité de sécurité Office 365 &amp; centre de conformité](create-activity-alerts.md). 
  
## <a name="next-steps"></a>Étapes suivantes

- [Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams](malicious-files-detected-in-spo-odb-or-teams.md)
    
- [Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365](manage-quarantined-messages-and-files.md)
    
## <a name="related-topics"></a>Voir aussi

[Office 365 - Protection avancée contre les menaces](office-365-atp.md)
  
[Afficher les rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md)
  
[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

