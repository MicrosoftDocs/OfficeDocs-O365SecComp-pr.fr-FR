---
title: Afficher les rapports pour Office 365 protection avancée contre les menaces
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
description: Découvrez comment trouver et utiliser des rapports pour Office 365 protection avancée contre les menaces dans &amp; le centre de sécurité conformité.
ms.openlocfilehash: c45224155d2e72edda1e0f0eced879e152b49629
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "30062612"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="35da9-103">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="35da9-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="35da9-p101">Si votre organisation dispose d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) et que vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez utiliser plusieurs rapports ATP dans &amp; le centre de sécurité conformité. (Accédez au \*\*\*\* \> **tableau de bord**rapports.)</span><span class="sxs-lookup"><span data-stu-id="35da9-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![Le tableau &amp; de bord du centre de sécurité conformité peut vous aider à déterminer le fonctionnement de la protection avancée contre les menaces](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="35da9-p102">Les rapports ATP incluent le rapport d' [État de protection contre les menaces](#threat-protection-status-report), le [rapport de types de fichiers ATP](#atp-file-types-report)et le [rapport de disposition de messages ATP](#atp-message-disposition-report). Cet article décrit les rapports ATP et inclut des liens vers d' [autres rapports à afficher](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="35da9-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="35da9-109">Rapport d'état de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="35da9-109">Threat Protection Status report</span></span>

<span data-ttu-id="35da9-p103">Le rapport d' **État de protection contre les menaces** est une vue unique qui rassemble des informations sur le contenu malveillant et les e-mails malveillants détectés et bloqués par [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) et [Office 365 ATP](office-365-atp.md). Le rapport fournit un nombre agrégé de messages électroniques uniques avec du contenu malveillant (des fichiers ou des adresses de sites Web (URL)) bloqués par le moteur anti-programme malveillant, la [purge automatique avec zéro heure (supprimable)](zero-hour-auto-purge.md)et les fonctionnalités ATP, telles que les [liens fiables ATP](atp-safe-links.md), le service [ATP Safe Pièces jointes](atp-safe-attachments.md)et [fonctionnalités anti-hameçonnage ATP](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="35da9-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="35da9-p104">Un rapport d'état de protection contre les menaces est disponible pour les clients qui ont [Office 365 ATP](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP); Toutefois, les informations affichées dans le rapport d'état de protection contre les menaces pour les clients ATP contiennent probablement des données différentes de celles que peuvent afficher les clients EOP. Par exemple, le rapport d'état de protection contre les menaces pour les clients ATP contient des informations sur les [fichiers malveillants détectés dans SharePoint Online, OneDrive ou Microsoft teams](atp-for-spo-odb-and-teams.md). Ces informations sont spécifiques à la protection avancée contre les menaces, de sorte que les clients qui disposent d'EOP mais pas de la fonctionnalité ATP ne verront pas ces détails dans le rapport d'état de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="35da9-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="35da9-115">Pour afficher le rapport d'état de protection contre les menaces, dans le [Centre de sécurité &amp; conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> de **protection contre les menaces**.</span><span class="sxs-lookup"><span data-stu-id="35da9-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Rapport d'état de protection contre les menaces ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="35da9-117">Pour obtenir l'état détaillé d'une journée, pointez sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="35da9-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Données d'état de protection contre les menaces ATP pendant une journée](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="35da9-p105">Par défaut, le rapport d'état de protection contre les menaces affiche les données des sept derniers jours. Toutefois, vous pouvez choisir **filtres** et modifier la plage de dates pour afficher les données pour 90 jours maximum.</span><span class="sxs-lookup"><span data-stu-id="35da9-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Filtres d'état de protection contre les menaces ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="35da9-122">Vous pouvez également utiliser le menu **afficher les données par** pour modifier les informations affichées dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="35da9-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Affichage des options pour le rapport d'état de protection contre les menaces ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="35da9-124">Rapport de types de fichiers ATP</span><span class="sxs-lookup"><span data-stu-id="35da9-124">ATP File Types report</span></span>

<span data-ttu-id="35da9-125">Le rapport **types de fichiers ATP** indique le type de fichiers détectés comme malveillants par des [pièces jointes sûres ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="35da9-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="35da9-126">Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **types de fichiers DAV**du **tableau de bord** \> des **rapports** \> .</span><span class="sxs-lookup"><span data-stu-id="35da9-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Rapport de types de fichiers ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="35da9-128">Lorsque vous placez le curseur de la souris sur un jour particulier, vous pouvez voir la répartition des types de fichiers malveillants détectés par les [pièces jointEs fiables ATP](atp-safe-attachments.md) et la protection contre les [programmes malveillants contre le courrier indésirable &amp; dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="35da9-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Données de rapport sur les types de fichiers ATP pendant une journée](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="35da9-130">Rapport de disposition des messages ATP</span><span class="sxs-lookup"><span data-stu-id="35da9-130">ATP Message Disposition report</span></span>

<span data-ttu-id="35da9-131">Le rapport de **disposition des messages ATP** indique les actions qui ont été effectuées pour les messages électroniques détectés comme présentant du contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="35da9-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="35da9-132">Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à rapports **tableau de bord** \> des **rapports** \> **ATP**.</span><span class="sxs-lookup"><span data-stu-id="35da9-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Rapport de disposition des messages ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="35da9-134">Lorsque vous placez le curseur de la souris sur une barre du graphique, vous pouvez voir les actions effectuées pour les messages électroniques détectés pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="35da9-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Données de rapport de disposition de messages ATP pendant une journée](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="35da9-136">Rapports supplémentaires à afficher</span><span class="sxs-lookup"><span data-stu-id="35da9-136">Additional reports to view</span></span>

<span data-ttu-id="35da9-137">Outre les rapports ATP décrits dans cet article, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="35da9-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="35da9-138">Type de rapport</span><span class="sxs-lookup"><span data-stu-id="35da9-138">Report type</span></span>  |<span data-ttu-id="35da9-139">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="35da9-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="35da9-140">**Rapports de sécurité de messagerie**, tels que le rapport des expéditeurs et des destinataires, un rapport de courrier indésirable et un rapport de détection du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="35da9-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="35da9-141">Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="35da9-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="35da9-142">**Explorateur** (également appelé «Explorateur de menaces», cela est inclus dans [Office 365 Threat Intelligence](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="35da9-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="35da9-143">Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="35da9-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="35da9-p106">**Résultats EOP et ATP** (Il s'agit d'un rapport personnalisé que vous générez à l'aide de PowerShell). Ce rapport contient des informations, telles que le domaine, la date, le type d'événement, la direction, l'action et le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="35da9-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="35da9-146">Référence de l'applet de commande Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="35da9-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="35da9-p107">**Détections EOP et ATP** (Il s'agit d'un rapport personnalisé que vous générez à l'aide de PowerShell). Ce rapport contient des détails sur les URL ou les fichiers malveillants, les tentatives de hameçonnage, l'emprunt d'identité et d'autres menaces potentielles dans les messages électroniques ou les fichiers.</span><span class="sxs-lookup"><span data-stu-id="35da9-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="35da9-149">Référence de l'applet de commande Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="35da9-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="35da9-150">Quelles sont les autorisations nécessaires pour afficher les rapports ATP?</span><span class="sxs-lookup"><span data-stu-id="35da9-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="35da9-151">Pour afficher et utiliser les rapports décrits dans cet article, **vous devez disposer d'un rôle approprié pour le centre de sécurité &amp; et le centre d'administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="35da9-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="35da9-152">Pour le centre &amp; de sécurité conformité, vous devez disposer de l'un des rôles suivants:</span><span class="sxs-lookup"><span data-stu-id="35da9-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="35da9-153">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="35da9-153">Organization Management</span></span>
    - <span data-ttu-id="35da9-154">Administrateur de la sécurité (qui peut être affecté dans le centre d'administration Azure[https://aad.portal.azure.com](https://aad.portal.azure.com)Active Directory ())</span><span class="sxs-lookup"><span data-stu-id="35da9-154">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="35da9-155">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="35da9-155">Security Reader</span></span>

- <span data-ttu-id="35da9-156">Pour Exchange Online, vous devez disposer de l'un des rôles suivants, qui est affecté dans le centre[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)d'administration Exchange () ou avec des applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="35da9-156">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="35da9-157">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="35da9-157">Organization Management</span></span>
    - <span data-ttu-id="35da9-158">Gestion de l’organisation en affichage seul</span><span class="sxs-lookup"><span data-stu-id="35da9-158">View-only Organization Management</span></span>
    - <span data-ttu-id="35da9-159">Rôle Destinataires en affichage uniquement</span><span class="sxs-lookup"><span data-stu-id="35da9-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="35da9-160">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="35da9-160">Compliance Management</span></span>

<span data-ttu-id="35da9-161">Pour en savoir plus, consultez les ressources suivantes:</span><span class="sxs-lookup"><span data-stu-id="35da9-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="35da9-162">Autorisations dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="35da9-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="35da9-163">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="35da9-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="35da9-164">Qu'en est-il si les rapports n'affichent pas de données?</span><span class="sxs-lookup"><span data-stu-id="35da9-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="35da9-p108">Si vous ne voyez pas de données dans vos rapports ATP, vérifiez que vos stratégies sont correctement configurées. Votre organisation doit avoir des [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) et des [stratégies de pièces jointEs approuvées ATP](set-up-atp-safe-attachments-policies.md) définies afin que la protection ATP soit mise en place. Consultez également la rubrique protection contre le [courrier indésirable et les programmes malveillants dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="35da9-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="35da9-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35da9-168">Related topics</span></span>

[<span data-ttu-id="35da9-169">Rapports et informations dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="35da9-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="35da9-170">Créer une planification pour un rapport dans le centre &amp; de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="35da9-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="35da9-171">Configurer et télécharger un rapport personnalisé dans le centre de &amp; sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="35da9-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

