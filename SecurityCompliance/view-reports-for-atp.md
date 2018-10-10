---
title: Afficher les rapports de Protection de menace avancées d’Office 365
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
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Découvrez comment trouver et utiliser les rapports pour Office 365 avancée contre les menaces de sécurité &amp; centre de conformité.
ms.openlocfilehash: 4a76c6a5b888142dc4c35af432fa61916145d648
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454301"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="3f0e2-103">Afficher les rapports de Protection de menace avancées d’Office 365</span><span class="sxs-lookup"><span data-stu-id="3f0e2-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="3f0e2-p101">Si votre organisation a [Contre les menaces avancées Office 365](office-365-atp.md) (DAV) et que vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez utiliser plusieurs rapports DAV dans la sécurité &amp; centre de conformité. (Accédez aux **rapports** \> **tableau de bord**.)</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="3f0e2-p102">Rapports DAV incluent le [rapport d’état de protection de menace](#threat-protection-status-report), le [rapport de Types de fichiers DAV](#atp-file-types-report)et le [rapport de Disposition de Message DAV](#atp-message-disposition-report). Cet article décrit les rapports DAV et inclut des liens vers [des rapports supplémentaires à afficher](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p102">ATP reports include the [Threat protection status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="3f0e2-109">Rapport d’état Threat protection</span><span class="sxs-lookup"><span data-stu-id="3f0e2-109">Threat protection status report</span></span>

<span data-ttu-id="3f0e2-p103">Le rapport **d’état de protection de menace** est un affichage simple qui rassemble des informations concernant les e-mails malveillants et contenu malveillant détecté et bloqué par Exchange Online et de protection contre les menaces avancées. Le rapport fournit un nombre de messages unique contenant du code malveillant (fichiers ou URL) bloquées par le moteur anti-programme malveillant, [heures zéro automatique purge (ZAP)](zero-hour-auto-purge.md)et fonctionnalités protection contre les menaces avancées, telles que [Des liens fiables DAV](atp-safe-links.md), [DAV agrégé Pièces jointes sûres](atp-safe-attachments.md)et les [fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p103">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by Exchange Online and Advanced Threat Protection. The report provides an aggregated count of unique email messages with malicious content (files or URLs) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Advanced Threat Protection features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md).</span></span>
  
<span data-ttu-id="3f0e2-112">Pour afficher le rapport d’état Threat protection, de la sécurité &amp; centre de conformité, accédez aux **rapports** \> **tableau de bord** \> **état de protection de menace**.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-112">To view the Threat protection status report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
  
![Rapport d’état de Protection de menace DAV](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="3f0e2-114">Pour obtenir le statut détaillé d’un jour, pointez sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-114">To get detailed status for a day, hover over the graph.</span></span>
  
![Données d’état de Protection de menace DAV pour un jour](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="3f0e2-p104">Par défaut, le rapport d’état Threat protection affiche les données pour les sept derniers jours. Toutefois, vous pouvez choisir les **filtres** et modifier la plage de dates pour afficher les données de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p104">By default, the Threat protection status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Filtres d’état de Protection de menace DAV](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="3f0e2-119">Vous pouvez également utiliser le menu **Afficher les données** pour modifier les informations affichées dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-119">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Options d’affichage pour le rapport d’état de Protection de menace DAV](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="3f0e2-121">Rapport sur les Types de fichier DAV</span><span class="sxs-lookup"><span data-stu-id="3f0e2-121">ATP File Types report</span></span>

<span data-ttu-id="3f0e2-122">Le rapport de **Types de fichiers DAV** indique le type de fichiers détecté comme malveillants par les [Pièces jointes sûres DAV](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-122">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="3f0e2-123">Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux **rapports** \> **tableau de bord** \> **Types de fichiers DAV**.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-123">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Rapport sur les Types de fichier DAV](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="3f0e2-125">Lorsque vous placez sur un jour donné, vous pouvez voir la répartition des types de fichiers malveillants qui ont été détectés par les [Pièces jointes sûres DAV](atp-safe-attachments.md) et [anti-spam &amp; protection anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-125">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Données de rapport de Types de fichiers DAV pour un jour](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="3f0e2-127">Rapport de Disposition de Message DAV</span><span class="sxs-lookup"><span data-stu-id="3f0e2-127">ATP Message Disposition report</span></span>

<span data-ttu-id="3f0e2-128">Le rapport de **Disposition de Message DAV** indique les actions qui ont été prises pour les messages électroniques qui ont été détectés comme ayant un contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-128">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="3f0e2-129">Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux **rapports** \> **tableau de bord** \> **Destruction du Message DAV**.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-129">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Rapport de Disposition Message DAV](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="3f0e2-131">Lorsque vous placez sur une barre dans le graphique, vous pouvez voir les actions exécutées pour le courrier électronique détecté pour ce jour.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-131">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Données de rapport de suspension des messages DAV pour un jour](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="3f0e2-133">Pour afficher des rapports supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3f0e2-133">Additional reports to view</span></span>

<span data-ttu-id="3f0e2-p105">Outre les rapports DAV décrites dans cet article, les [rapports de sécurité de messagerie](view-email-security-reports.md) sont disponibles dans la sécurité &amp; centre de conformité. Rapports de sécurité de messagerie incluent un [rapport de destinataires et les principaux expéditeurs](view-email-security-reports.md#top-senders-and-recipients-report), un [rapport de messagerie de l’usurpation d’identité](view-email-security-reports.md#spoof-mail-report), un [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report)et plus.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p105">In addition to the ATP reports described in this article, [email security reports](view-email-security-reports.md) are available in the Security &amp; Compliance Center. Email security reports include a [Top Senders and Recipients report](view-email-security-reports.md#top-senders-and-recipients-report), a [Spoof Mail report](view-email-security-reports.md#spoof-mail-report), a [Spam Detections report](view-email-security-reports.md#spam-detections-report), and more.</span></span>
  
<span data-ttu-id="3f0e2-136">Et, si votre organisation dispose des [Informations sur les menaces Office 365](office-365-ti.md), vous pouvez également [Utilisez l’Explorateur de la sécurité &amp; centre de conformité](use-explorer-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-136">And, if your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can also [Use Explorer in the Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md).</span></span>
  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="3f0e2-137">Les autorisations requises pour afficher les rapports DAV ?</span><span class="sxs-lookup"><span data-stu-id="3f0e2-137">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="3f0e2-138">Pour pouvoir afficher et utiliser les rapports décrits dans cet article, vous devez disposer d’un rôle approprié est affecté de la sécurité &amp; centre de conformité et dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f0e2-138">In order to view and use the reports described in this article, you must have an appropriate role assigned in the Security &amp; Compliance Center and in the Exchange Admin Center.</span></span>
  
|<span data-ttu-id="3f0e2-139">**Groupe de rôles**</span><span class="sxs-lookup"><span data-stu-id="3f0e2-139">**Role group**</span></span>|<span data-ttu-id="3f0e2-140">**Où affecté**</span><span class="sxs-lookup"><span data-stu-id="3f0e2-140">**Where assigned**</span></span>|<span data-ttu-id="3f0e2-141">**En savoir plus**</span><span class="sxs-lookup"><span data-stu-id="3f0e2-141">**Learn more**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3f0e2-142">Un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3f0e2-142">One of the following:</span></span>  <br/>  <span data-ttu-id="3f0e2-143">Gestion de l'organisation</span><span class="sxs-lookup"><span data-stu-id="3f0e2-143">Organization Management</span></span>  <br/>  <span data-ttu-id="3f0e2-144">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-144">Security Administrator</span></span>  <br/>  <span data-ttu-id="3f0e2-145">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-145">Security Reader</span></span>  <br/> |<span data-ttu-id="3f0e2-146">Sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-146">Security &amp; Compliance Center</span></span>  <br/> |[<span data-ttu-id="3f0e2-147">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-147">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md) <br/> |
| <span data-ttu-id="3f0e2-148">Un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3f0e2-148">One of the following:</span></span>  <br/>  <span data-ttu-id="3f0e2-149">Gestion de l'organisation</span><span class="sxs-lookup"><span data-stu-id="3f0e2-149">Organization Management</span></span>  <br/>  <span data-ttu-id="3f0e2-150">Gestion de l'organisation en affichage seul</span><span class="sxs-lookup"><span data-stu-id="3f0e2-150">View-only Organization Management</span></span>  <br/>  <span data-ttu-id="3f0e2-151">Rôle Destinataires en affichage uniquement</span><span class="sxs-lookup"><span data-stu-id="3f0e2-151">View-Only Recipients role</span></span>  <br/>  <span data-ttu-id="3f0e2-152">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-152">Compliance Management</span></span>  <br/> |<span data-ttu-id="3f0e2-153">Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="3f0e2-153">Exchange Admin Center</span></span>  <br/> |[<span data-ttu-id="3f0e2-154">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3f0e2-154">Feature permissions in Exchange Online</span></span>](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="3f0e2-155">Que se passe-t-il si les rapports ne sont pas affichant les données ?</span><span class="sxs-lookup"><span data-stu-id="3f0e2-155">What if the reports aren't showing data?</span></span>

<span data-ttu-id="3f0e2-p106">Si vous ne voyez pas les données dans vos rapports, vérifiez que vos stratégies sont correctement configurés. Votre organisation doit avoir des [stratégies DAV fiables liens](set-up-atp-safe-links-policies.md) et [pièces jointes sûres DAV stratégies](set-up-atp-safe-attachments-policies.md) définies dans l’ordre de protection DAV pour mettre en place. Consultez également la [protection contre le courrier indésirable et anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="3f0e2-p106">If you are not seeing data in your reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="3f0e2-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f0e2-159">Related topics</span></span>

[<span data-ttu-id="3f0e2-160">Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-160">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="3f0e2-161">Créer une planification pour un état de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-161">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="3f0e2-162">Configurer et télécharger un rapport personnalisé dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3f0e2-162">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

