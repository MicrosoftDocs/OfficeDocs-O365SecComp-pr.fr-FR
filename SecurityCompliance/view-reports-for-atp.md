---
title: Afficher les rapports de Protection de menace avancées d’Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection: M365-security-compliance
description: Découvrez comment trouver et utiliser les rapports pour Office 365 avancée contre les menaces de sécurité &amp; centre de conformité.
ms.openlocfilehash: a27fdf6c7d04a2526873047d4e2a33bb283878b3
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995225"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="a4910-103">Afficher les rapports de Protection de menace avancées d’Office 365</span><span class="sxs-lookup"><span data-stu-id="a4910-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="a4910-p101">Si votre organisation a [Contre les menaces avancées Office 365](office-365-atp.md) (DAV) et que vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez utiliser plusieurs rapports DAV dans la sécurité &amp; centre de conformité. (Accédez aux **rapports** \> **tableau de bord**.)</span><span class="sxs-lookup"><span data-stu-id="a4910-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="a4910-p102">Rapports DAV incluent le [rapport d’état de Protection de menace](#threat-protection-status-report), le [rapport de Types de fichiers DAV](#atp-file-types-report)et le [rapport de Disposition de Message DAV](#atp-message-disposition-report). Cet article décrit les rapports DAV et inclut des liens vers [des rapports supplémentaires à afficher](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="a4910-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="a4910-109">Rapport d’état de Protection de menace</span><span class="sxs-lookup"><span data-stu-id="a4910-109">Threat Protection Status report</span></span>

<span data-ttu-id="a4910-p103">Le rapport **d’État de Protection de menace** est un affichage simple qui rassemble des informations concernant les e-mails malveillants et contenu malveillant détecté et bloqué par [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) et [Office 365 DAV](office-365-atp.md). Le rapport fournit un nombre de messages unique contenant du code malveillant (fichiers ou des adresses de site Web (URL)) bloqués par le moteur anti-programme malveillant, [heures zéro automatique purge (ZAP)](zero-hour-auto-purge.md)et fonctionnalités DAV, telles que des [Liens fiables DAV](atp-safe-links.md), [Safe DAV agrégé Pièces jointes](atp-safe-attachments.md)et les [fonctionnalités anti-hameçonnage de DAV](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="a4910-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a4910-p104">Un rapport d’état de Protection de menace est disponible pour les clients qui ont des [Office 365 DAV](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP) ; Toutefois, les informations qui s’affiche dans le rapport d’état de Protection des menaces pour les clients disposant contiendra probablement que les clients EOP peuvent afficher des données différentes. Par exemple, le rapport d’état de Protection des menaces pour les clients DAV contient plus d’informations sur [les fichiers malveillants détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](atp-for-spo-odb-and-teams.md). Ces informations sont spécifiques à DAV, afin que les clients qui ont EOP mais pas DAV ne seront affiche pas ces détails dans leur état de Protection de menace.</span><span class="sxs-lookup"><span data-stu-id="a4910-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="a4910-115">Pour afficher le rapport d’état de Protection de menace, dans le [sécurité &amp; centre de conformité](https://protection.office.com), accédez aux **rapports** \> **tableau de bord** \> **État de Protection de menace**.</span><span class="sxs-lookup"><span data-stu-id="a4910-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Rapport d’état de Protection de menace DAV](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="a4910-117">Pour obtenir le statut détaillé d’un jour, pointez sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="a4910-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Données d’état de Protection de menace DAV pour un jour](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="a4910-p105">Par défaut, le rapport d’état de Protection de menace affiche les données pour les sept derniers jours. Toutefois, vous pouvez choisir les **filtres** et modifier la plage de dates pour afficher les données de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="a4910-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Filtres d’état de Protection de menace DAV](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="a4910-122">Vous pouvez également utiliser le menu **Afficher les données** pour modifier les informations affichées dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a4910-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Options d’affichage pour le rapport d’état de Protection de menace DAV](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="a4910-124">Rapport sur les Types de fichier DAV</span><span class="sxs-lookup"><span data-stu-id="a4910-124">ATP File Types report</span></span>

<span data-ttu-id="a4910-125">Le rapport de **Types de fichiers DAV** indique le type de fichiers détecté comme malveillants par les [Pièces jointes sûres DAV](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="a4910-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="a4910-126">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://protection.office.com), accédez aux **rapports** \> **tableau de bord** \> **Types de fichiers DAV**.</span><span class="sxs-lookup"><span data-stu-id="a4910-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Rapport sur les Types de fichier DAV](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="a4910-128">Lorsque vous placez sur un jour donné, vous pouvez voir la répartition des types de fichiers malveillants qui ont été détectés par les [Pièces jointes sûres DAV](atp-safe-attachments.md) et [anti-spam &amp; protection anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="a4910-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Données de rapport de Types de fichiers DAV pour un jour](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="a4910-130">Rapport de Disposition de Message DAV</span><span class="sxs-lookup"><span data-stu-id="a4910-130">ATP Message Disposition report</span></span>

<span data-ttu-id="a4910-131">Le rapport de **Disposition de Message DAV** indique les actions qui ont été prises pour les messages électroniques qui ont été détectés comme ayant un contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="a4910-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="a4910-132">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://protection.office.com), accédez aux **rapports** \> **tableau de bord** \> **Destruction du Message DAV**.</span><span class="sxs-lookup"><span data-stu-id="a4910-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Rapport de Disposition Message DAV](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="a4910-134">Lorsque vous placez sur une barre dans le graphique, vous pouvez voir les actions exécutées pour le courrier électronique détecté pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="a4910-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Données de rapport de suspension des messages DAV pour un jour](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="a4910-136">Pour afficher des rapports supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a4910-136">Additional reports to view</span></span>

<span data-ttu-id="a4910-137">Outre les rapports DAV décrites dans cet article, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="a4910-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="a4910-138">Type de rapport</span><span class="sxs-lookup"><span data-stu-id="a4910-138">Report type</span></span>  |<span data-ttu-id="a4910-139">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="a4910-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="a4910-140">**Rapports de sécurité de messagerie**, comme un principaux expéditeurs et destinataires rapport, un rapport de messagerie de l’usurpation d’identité et un rapport des détections de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a4910-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="a4910-141">Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="a4910-142">**Explorateur de solutions** (également appelé Threat Explorer, il est inclus dans [Office 365 menaces](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="a4910-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="a4910-143">Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="a4910-p106">**Résultats EOP et DAV** (Il s’agit un rapport personnalisé, que vous générez à l’aide de PowerShell). Ce rapport contient des informations, telles que le domaine, Date, Type d’événement, Direction, Action et nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="a4910-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="a4910-146">Référence d’applet de commande Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="a4910-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="a4910-p107">**Détections EOP et DAV** (Il s’agit un rapport personnalisé, que vous générez à l’aide de PowerShell). Ce rapport contient plus d’informations sur les fichiers malveillants ou URL, les tentatives de hameçonnage, l’emprunt d’identité et autres menaces potentielles de courrier électronique ou de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a4910-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="a4910-149">Référence d’applet de commande Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="a4910-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="a4910-150">Les autorisations requises pour afficher les rapports DAV ?</span><span class="sxs-lookup"><span data-stu-id="a4910-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="a4910-151">Pour pouvoir afficher et utiliser les rapports décrits dans cet article, **vous devez disposer d’un rôle approprié attribué à la sécurité &amp; centre de conformité et le centre d’administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="a4910-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="a4910-152">Pour la sécurité &amp; centre de conformité, vous devez disposer d’un des rôles suivants est attribué :</span><span class="sxs-lookup"><span data-stu-id="a4910-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="a4910-153">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="a4910-153">Organization Management</span></span>
    - <span data-ttu-id="a4910-154">Administrateur de la sécurité (il peut être assigné dans le centre d’administration Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="a4910-154">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>
    - <span data-ttu-id="a4910-155">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="a4910-155">Security Reader</span></span>

- <span data-ttu-id="a4910-156">Pour Exchange Online, vous devez disposer d’un des rôles suivants est attribué centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) ou à l’aide des applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) :</span><span class="sxs-lookup"><span data-stu-id="a4910-156">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="a4910-157">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="a4910-157">Organization Management</span></span>
    - <span data-ttu-id="a4910-158">Gestion de l’organisation en affichage seul</span><span class="sxs-lookup"><span data-stu-id="a4910-158">View-only Organization Management</span></span>
    - <span data-ttu-id="a4910-159">Rôle Destinataires en affichage uniquement</span><span class="sxs-lookup"><span data-stu-id="a4910-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="a4910-160">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-160">Compliance Management</span></span>

<span data-ttu-id="a4910-161">Pour plus d’informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4910-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="a4910-162">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="a4910-163">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a4910-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="a4910-164">Que se passe-t-il si les rapports ne sont pas affichant les données ?</span><span class="sxs-lookup"><span data-stu-id="a4910-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="a4910-p108">Si vous ne voyez pas les données dans vos rapports DAV, vérifiez que vos stratégies sont correctement configurés. Votre organisation doit avoir des [stratégies DAV fiables liens](set-up-atp-safe-links-policies.md) et [pièces jointes sûres DAV stratégies](set-up-atp-safe-attachments-policies.md) définies dans l’ordre de protection DAV pour mettre en place. Consultez également la [protection contre le courrier indésirable et anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="a4910-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="a4910-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4910-168">Related topics</span></span>

[<span data-ttu-id="a4910-169">Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="a4910-170">Créer une planification pour un état de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="a4910-171">Configurer et télécharger un rapport personnalisé dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a4910-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

