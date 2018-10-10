---
title: Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft
ms.author: derng
author: derng
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Découvrez comment activer DAV pour SharePoint, OneDrive et les équipes, notamment comment définir des alertes pour les fichiers détectés.
ms.openlocfilehash: eb3687f6afd2e7f9a3698944019bcdb8dcbff5ae
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454291"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="a9bbb-103">Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft</span><span class="sxs-lookup"><span data-stu-id="a9bbb-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="a9bbb-p101">[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation de partager des fichiers malveillants par inadvertance. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour activer DAV pour SharePoint, OneDrive et les équipes, définir des alertes pour être averti des fichiers détectés et effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="a9bbb-107">Afin d’effectuer les tâches décrites dans cet article, vous devez disposer des autorisations nécessaires affectées dans Office 365 et de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-107">In order to perform the tasks described in this article, you must have the necessary permissions assigned in Office 365 and in the Security &amp; Compliance Center.</span></span>
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="a9bbb-108">Activer ATP pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a9bbb-108">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

 <span data-ttu-id="a9bbb-p102">**Avant de commencer cette procédure, assurez-vous que l’enregistrement d’audit est déjà activé pour votre environnement Office 365**. Cela s’effectue généralement par toute personne ayant le rôle journaux d’Audit affecté dans Exchange Online. Pour plus d’informations, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p102">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="a9bbb-112">En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com), puis connectez-vous avec votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-112">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="a9bbb-113">De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Pièces jointes fiables**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-113">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span>
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> stratégie](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. <span data-ttu-id="a9bbb-115">Sélectionnez **Activer DAV pour SharePoint, OneDrive et les équipes Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-115">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>
    
    ![Activer la protection contre les menaces avancée pour SharePoint Online, OneDrive entreprise et les équipes Microsoft](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. <span data-ttu-id="a9bbb-117">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-117">Click **Save**.</span></span>
    
5. <span data-ttu-id="a9bbb-118">Passez en revue (et, selon le cas, modifier) [des stratégies de pièces jointes fiables](set-up-atp-safe-attachments-policies.md) et des [stratégies de liens fiables](set-up-atp-safe-links-policies.md)de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-118">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="a9bbb-119">(Recommandé) En tant qu’administrateur global ou un administrateur SharePoint Online, exécutez l’applet de commande **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** la valeur *true* .</span><span class="sxs-lookup"><span data-stu-id="a9bbb-119">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*  .</span></span> <br/><span data-ttu-id="a9bbb-p103">Le paramètre *true* blocs toutes les actions (à l’exception de la suppression) pour les fichiers détectés. Personnes ne peut pas ouvrir, déplacer, copier ou partager des fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p103">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files. </span></span><br/><span data-ttu-id="a9bbb-p104">Définition du paramètre sur *false* bloque toutes les actions à l’exception de suppression et le téléchargement. Personnes peuvent choisir d’accepter le risque et télécharger un fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p104">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file. </span></span><br/><span data-ttu-id="a9bbb-124">Nous vous recommandons de définir le paramètre sur *true*.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-124">We recommend setting the parameter to *true*.</span></span> 
   
7. <span data-ttu-id="a9bbb-125">Autoriser jusqu'à 30 minutes pour que vos modifications à répartir pour tous les centres de données Office 365.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-125">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="a9bbb-126">(Recommandé) Passez à définir des alertes pour les fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-126">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="a9bbb-p105">Pour plus d’informations sur l’utilisation de PowerShell avec Office 365, voir [Gestion d’Office 365 avec PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, consultez la rubrique [que faire lorsqu’un fichier malveillant est détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p105">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="a9bbb-129">Définir des alertes pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="a9bbb-129">Set up alerts for detected files</span></span>

<span data-ttu-id="a9bbb-130">Pour recevoir une notification lorsqu’un fichier dans SharePoint Online, OneDrive pour les professionnels ou Microsoft Teams a été identifié comme malveillant, vous pouvez configurer une alerte.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-130">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="a9bbb-131">De sécurité Office 365 &amp; centre de conformité, sélectionnez **alertes** \> **Gérer les alertes**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-131">In the Office 365 Security &amp; Compliance Center, choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="a9bbb-132">Choisissez **nouvelle stratégie de l’alerte**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-132">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="a9bbb-p106">Spécifiez un nom pour l’alerte. Par exemple, vous pouvez taper des fichiers malveillants dans des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p106">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="a9bbb-p107">Tapez une description de l’alerte. Par exemple, vous pouvez taper notifie administrateurs lorsque des fichiers malveillants sont détectées dans SharePoint Online, OneDrive ou Teams Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-p107">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="a9bbb-137">Dans la section **Envoyer cette alerte lorsque...** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a9bbb-137">In the **Send this alert when...** section, do the following:</span></span> 
    
  - <span data-ttu-id="a9bbb-138">Dans la liste des **activités** , choisissez **malveillant détecté dans le fichier**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-138">In the **Activities** list, choose **Detected malware in file**.</span></span>
    
  - <span data-ttu-id="a9bbb-139">Laissez le champ **utilisateurs** vide.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-139">Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="a9bbb-140">Dans la section **Envoyer cette alerte...** , sélectionnez un ou plusieurs administrateurs globaux, les administrateurs de sécurité ou les lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-140">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="a9bbb-141">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a9bbb-141">Click **Save**.</span></span>
    
<span data-ttu-id="a9bbb-142">Pour plus d’informations sur les alertes, voir [créer des alertes de l’activité de sécurité Office 365 &amp; centre de conformité](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="a9bbb-142">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="a9bbb-143">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a9bbb-143">Next steps</span></span>

- [<span data-ttu-id="a9bbb-144">Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a9bbb-144">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
- [<span data-ttu-id="a9bbb-145">Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a9bbb-145">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    
## <a name="related-topics"></a><span data-ttu-id="a9bbb-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9bbb-146">Related topics</span></span>

[<span data-ttu-id="a9bbb-147">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a9bbb-147">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="a9bbb-148">Afficher les rapports pour Office 365 avancée protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a9bbb-148">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="a9bbb-149">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a9bbb-149">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

