---
title: Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft
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
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Découvrez comment activer DAV pour SharePoint, OneDrive et les équipes, notamment comment définir des alertes pour les fichiers détectés.
ms.openlocfilehash: e413f0b57186dc1364b63e14985ef0f54ca7e442
ms.sourcegitcommit: 0cc6083bd8cb2f7bbf18847149c6d5239f2a6403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26699937"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="4bf43-103">Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft</span><span class="sxs-lookup"><span data-stu-id="4bf43-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="4bf43-p101">[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation de partager des fichiers malveillants par inadvertance. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour activer DAV pour SharePoint, OneDrive et les équipes, définir des alertes pour être averti des fichiers détectés et effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="4bf43-107">Afin d’effectuer les tâches décrites dans cet article, vous devez disposer des autorisations nécessaires affectées dans Office 365 et de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="4bf43-107">In order to perform the tasks described in this article, you must have the necessary permissions assigned in Office 365 and in the Security &amp; Compliance Center.</span></span>
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="4bf43-108">Activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4bf43-108">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

 <span data-ttu-id="4bf43-p102">**Avant de commencer cette procédure, assurez-vous que l’enregistrement d’audit est déjà activé pour votre environnement Office 365**. Cela s’effectue généralement par toute personne ayant le rôle journaux d’Audit affecté dans Exchange Online. Pour plus d’informations, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="4bf43-p102">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="4bf43-112">En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com), puis connectez-vous avec votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="4bf43-112">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="4bf43-113">De sécurité Office 365 &amp; centre de conformité, dans le volet de navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Pièces jointes fiables**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-113">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="4bf43-114">![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> stratégie](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="4bf43-114">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="4bf43-115">Sélectionnez **Activer DAV pour SharePoint, OneDrive et les équipes Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-115">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="4bf43-116">![Activer la protection contre les menaces avancée pour SharePoint Online, OneDrive entreprise et les équipes Microsoft](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="4bf43-116">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="4bf43-117">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-117">Click **Save**.</span></span>
    
5. <span data-ttu-id="4bf43-118">Passez en revue (et, selon le cas, modifier) [des stratégies de pièces jointes fiables](set-up-atp-safe-attachments-policies.md) et des [stratégies de liens fiables](set-up-atp-safe-links-policies.md)de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4bf43-118">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="4bf43-119">(Recommandé) En tant qu’administrateur global ou un administrateur SharePoint Online, exécutez l’applet de commande **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** la valeur *true*.</span><span class="sxs-lookup"><span data-stu-id="4bf43-119">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="4bf43-p103">Le paramètre *true* blocs toutes les actions (à l’exception de la suppression) pour les fichiers détectés. Personnes ne peut pas ouvrir, déplacer, copier ou partager des fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p103">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="4bf43-p104">Définition du paramètre sur *false* bloque toutes les actions à l’exception de suppression et le téléchargement. Personnes peuvent choisir d’accepter le risque et télécharger un fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p104">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="4bf43-124">Autoriser jusqu'à 30 minutes pour que vos modifications à répartir pour tous les centres de données Office 365.</span><span class="sxs-lookup"><span data-stu-id="4bf43-124">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="4bf43-125">(Recommandé) Passez à définir des alertes pour les fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="4bf43-125">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="4bf43-126">Pour plus d’informations sur l’utilisation de PowerShell avec Office 365, voir [Gestion d’Office 365 avec PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="4bf43-126">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="4bf43-127">Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, consultez la rubrique [que faire lorsqu’un fichier malveillant est détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="4bf43-127">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="4bf43-128">Définir des alertes pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="4bf43-128">Set up alerts for detected files</span></span>

<span data-ttu-id="4bf43-129">Pour recevoir une notification lorsqu’un fichier dans SharePoint Online, OneDrive pour les professionnels ou Microsoft Teams a été identifié comme malveillant, vous pouvez configurer une alerte.</span><span class="sxs-lookup"><span data-stu-id="4bf43-129">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="4bf43-130">De sécurité Office 365 &amp; centre de conformité, sélectionnez **alertes** \> **Gérer les alertes**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-130">In the Office 365 Security &amp; Compliance Center, choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="4bf43-131">Choisissez **nouvelle stratégie de l’alerte**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-131">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="4bf43-p105">Spécifiez un nom pour l’alerte. Par exemple, vous pouvez taper des fichiers malveillants dans des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p105">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="4bf43-p106">Tapez une description de l’alerte. Par exemple, vous pouvez taper notifie administrateurs lorsque des fichiers malveillants sont détectées dans SharePoint Online, OneDrive ou Teams Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p106">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="4bf43-136">Dans la section **Envoyer cette alerte lorsque...** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4bf43-136">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="4bf43-p107">a. dans la liste des **activités** , choisissez **malveillant détecté dans le fichier**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p107">a. In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="4bf43-p108">b. Laissez le champ **utilisateurs** vide.</span><span class="sxs-lookup"><span data-stu-id="4bf43-p108">b. Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="4bf43-141">Dans la section **Envoyer cette alerte...** , sélectionnez un ou plusieurs administrateurs globaux, les administrateurs de sécurité ou les lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="4bf43-141">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="4bf43-142">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4bf43-142">Click **Save**.</span></span>
    
<span data-ttu-id="4bf43-143">Pour plus d’informations sur les alertes, voir [créer des alertes de l’activité de sécurité Office 365 &amp; centre de conformité](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="4bf43-143">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="4bf43-144">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4bf43-144">Next steps</span></span>

1. [<span data-ttu-id="4bf43-145">Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4bf43-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="4bf43-146">Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4bf43-146">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

