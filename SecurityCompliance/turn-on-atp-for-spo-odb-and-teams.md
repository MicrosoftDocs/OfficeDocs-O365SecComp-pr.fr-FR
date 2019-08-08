---
title: Activer la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
description: Découvrez comment activer la protection avancée contre les menaces pour SharePoint, OneDrive et Teams, y compris comment définir des alertes pour les fichiers détectés.
ms.openlocfilehash: f399d8b9b07e3c6847c389f24b563c2226bf41a8
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231068"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="a566d-103">Activer la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="a566d-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a566d-104">Cet article est destiné aux clients professionnels qui disposent d' [Office 365 Advanced Threat Protection](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="a566d-104">This article is intended for business customers who have [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="a566d-105">Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur les liens fiables dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="a566d-105">If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="a566d-106">[Office 365 ATP pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) protège votre organisation contre le partage accidentel de fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="a566d-106">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="a566d-107">Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin que personne ne puisse l’ouvrir, le copier, le déplacer ou le partager tant que d’autres actions ne sont pas effectuées par l’équipe de sécurité de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="a566d-107">When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team.</span></span> <span data-ttu-id="a566d-108">Lisez cet article pour activer la protection avancée contre les menaces pour SharePoint, OneDrive et Teams, configurer des alertes pour être averti des fichiers détectés et suivre les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a566d-108">Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="a566d-109">Pour définir (ou modifier) des stratégies ATP, vous devez disposer d’un rôle approprié.</span><span class="sxs-lookup"><span data-stu-id="a566d-109">To define (or edit) ATP policies, you must be assigned an appropriate role.</span></span> <span data-ttu-id="a566d-110">Certains exemples sont décrits dans le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="a566d-110">Some examples are described in the following table:</span></span>

|<span data-ttu-id="a566d-111">Role</span><span class="sxs-lookup"><span data-stu-id="a566d-111">Role</span></span>  |<span data-ttu-id="a566d-112">WHERE/How Assigned</span><span class="sxs-lookup"><span data-stu-id="a566d-112">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="a566d-113">Administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="a566d-113">Office 365 Global Administrator</span></span> |<span data-ttu-id="a566d-114">La personne qui s’inscrit pour acheter Office 365 est un administrateur global par défaut.</span><span class="sxs-lookup"><span data-stu-id="a566d-114">The person who signs up to buy Office 365 is a global admin by default.</span></span> <span data-ttu-id="a566d-115">(Pour en savoir plus, consultez la rubrique [à propos des rôles d’administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="a566d-115">(See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="a566d-116">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="a566d-116">Security Administrator</span></span> |<span data-ttu-id="a566d-117">Centre d’administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()</span><span class="sxs-lookup"><span data-stu-id="a566d-117">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="a566d-118">Gestion de l’organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a566d-118">Exchange Online Organization Management</span></span> |<span data-ttu-id="a566d-119">Centre d’administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)()</span><span class="sxs-lookup"><span data-stu-id="a566d-119">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="a566d-120">ou</span><span class="sxs-lookup"><span data-stu-id="a566d-120">or</span></span> <br>  <span data-ttu-id="a566d-121">Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="a566d-121">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="a566d-122">Activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a566d-122">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="a566d-123">**Avant de commencer cette procédure, assurez-vous que la journalisation d’audit est déjà activée pour votre environnement Office 365**.</span><span class="sxs-lookup"><span data-stu-id="a566d-123">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**.</span></span> <span data-ttu-id="a566d-124">Cette opération est généralement réalisée par une personne disposant du rôle journaux d’audit dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a566d-124">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="a566d-125">Pour plus d’informations, voir [activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="a566d-125">For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="a566d-126">Accédez à [https://protection.office.com](https://protection.office.com), puis connectez-vous à l’aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="a566d-126">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="a566d-127">Dans le centre de sécurité &amp; conformité Office 365, dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez stratégie de **pièces jointes approuvées**par la **stratégie** \> .</span><span class="sxs-lookup"><span data-stu-id="a566d-127">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="a566d-128">![Dans le centre &amp; de sécurité conformité, sélectionnez stratégie \> de gestion des menaces.](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="a566d-128">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="a566d-129">Sélectionnez Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.</span><span class="sxs-lookup"><span data-stu-id="a566d-129">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="a566d-130">![Activer la protection avancée contre les menaces pour SharePoint Online, OneDrive entreprise et Microsoft teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="a566d-130">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="a566d-131">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a566d-131">Click **Save**.</span></span>
    
5. <span data-ttu-id="a566d-132">Vérifiez (et, le cas échéant, modifiez) les stratégies de [pièces jointes](set-up-atp-safe-attachments-policies.md) approuvées et les [stratégies de liens fiables](set-up-atp-safe-links-policies.md)de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a566d-132">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="a566d-133">Recommandation En tant qu’administrateur général ou administrateur SharePoint Online, exécutez la cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** défini sur *true*.</span><span class="sxs-lookup"><span data-stu-id="a566d-133">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="a566d-134">La définition du paramètre sur *true* bloque toutes les actions (à l’exception de la suppression) des fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="a566d-134">Setting the parameter to *true* blocks all actions (except Delete) for detected files.</span></span> <span data-ttu-id="a566d-135">Les utilisateurs ne peuvent pas ouvrir, déplacer, copier ou partager des fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="a566d-135">People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="a566d-136">La définition du paramètre \*\* sur false bloque toutes les actions à l’exception de Delete et download.</span><span class="sxs-lookup"><span data-stu-id="a566d-136">Setting the parameter to *false* blocks all actions except Delete and Download.</span></span> <span data-ttu-id="a566d-137">Les utilisateurs peuvent choisir d’accepter le risque et de télécharger un fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="a566d-137">People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="a566d-138">Autorisez jusqu’à 30 minutes pour que vos modifications soient diffusées sur tous les centres de calcul Office 365.</span><span class="sxs-lookup"><span data-stu-id="a566d-138">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="a566d-139">Recommandation Passez à la configuration des alertes pour les fichiers détectés.</span><span class="sxs-lookup"><span data-stu-id="a566d-139">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="a566d-140">Pour en savoir plus sur l’utilisation de PowerShell avec Office 365, voir [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="a566d-140">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="a566d-141">Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, consultez la rubrique [que faire lorsqu’un fichier malveillant est trouvé dans SharePoint Online, OneDrive ou Microsoft teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="a566d-141">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="a566d-142">Configurer des alertes pour les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="a566d-142">Set up alerts for detected files</span></span>

<span data-ttu-id="a566d-143">Pour recevoir une notification lorsqu’un fichier dans SharePoint Online, OneDrive entreprise ou Microsoft teams a été identifié comme malveillant, vous pouvez configurer une alerte.</span><span class="sxs-lookup"><span data-stu-id="a566d-143">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="a566d-144">Dans le [Centre de sécurité &amp; conformité Office 365](https://protection.office.com), sélectionnez **alertes** \> **gérer les alertes**.</span><span class="sxs-lookup"><span data-stu-id="a566d-144">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="a566d-145">Choisissez **nouvelle stratégie d’alerte**.</span><span class="sxs-lookup"><span data-stu-id="a566d-145">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="a566d-146">Spécifiez un nom pour l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a566d-146">Specify a name for the alert.</span></span> <span data-ttu-id="a566d-147">Par exemple, vous pouvez taper des fichiers malveillants dans les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="a566d-147">For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="a566d-148">Tapez une description pour l’alerte.</span><span class="sxs-lookup"><span data-stu-id="a566d-148">Type a description for the alert.</span></span> <span data-ttu-id="a566d-149">Par exemple, vous pouvez taper avertir les administrateurs lorsque des fichiers malveillants sont détectés dans SharePoint Online, OneDrive ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a566d-149">For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="a566d-150">Dans la section **Envoyer cette alerte quand...** , procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="a566d-150">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="a566d-151">a.</span><span class="sxs-lookup"><span data-stu-id="a566d-151">a.</span></span> <span data-ttu-id="a566d-152">Dans la liste **activités** , sélectionnez **programmes malveillants détectés dans le fichier**.</span><span class="sxs-lookup"><span data-stu-id="a566d-152">In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="a566d-153">b.</span><span class="sxs-lookup"><span data-stu-id="a566d-153">b.</span></span> <span data-ttu-id="a566d-154">Laissez le champ **utilisateurs** vide.</span><span class="sxs-lookup"><span data-stu-id="a566d-154">Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="a566d-155">Dans la section **Envoyer cette alerte à...** , sélectionnez un ou plusieurs administrateurs globaux, administrateurs de sécurité ou lecteurs de sécurité qui doivent recevoir une notification lorsqu’un fichier malveillant est détecté.</span><span class="sxs-lookup"><span data-stu-id="a566d-155">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="a566d-156">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a566d-156">Click **Save**.</span></span>
    
<span data-ttu-id="a566d-157">Pour en savoir plus sur les alertes, consultez [la rubrique créer des alertes d' &amp; activité dans le centre de sécurité conformité Office 365](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="a566d-157">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="a566d-158">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a566d-158">Next steps</span></span>

1. [<span data-ttu-id="a566d-159">Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="a566d-159">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="a566d-160">Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a566d-160">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

