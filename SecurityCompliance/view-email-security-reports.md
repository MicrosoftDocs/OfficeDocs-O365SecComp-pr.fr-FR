---
title: Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/27/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
description: Découvrez comment trouver et utiliser les rapports de sécurité de messagerie pour votre organisation avec Office 365 pour entreprises. Rapports de sécurité de messagerie sont disponibles dans la sécurité &amp; centre de conformité.
ms.openlocfilehash: 72039afd52cd6e9da7dfd05bb67aac2c7e7db001
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706418"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="4fcf0-104">Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-104">View email security reports in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="4fcf0-p102">Une série de rapports de sécurité de messagerie sont disponibles dans le [sécurité &amp; centre de conformité](https://security.microsoft.com) pour vous aider à voir la façon dont des fonctionnalités anti-spam et contre les programmes malveillants dans Office 365 sont protège votre organisation. Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans la sécurité &amp; centre de conformité en accédant aux **rapports** \> **tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p102">A variety of email security reports are available in the [Security &amp; Compliance Center](https://security.microsoft.com) to help you see how anti-spam and anti-malware features in Office 365 are protecting your organization. If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security &amp; Compliance Center by going to **Reports** \> **Dashboard**.</span></span>
  
![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="4fcf0-108">Vos rapports de sécurité de messagerie sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fcf0-108">Your email security reports include the following:</span></span>
  
- <span data-ttu-id="4fcf0-109">[Rapport d’état de Protection de menace](view-email-security-reports.md#tps) (nouveau) !</span><span class="sxs-lookup"><span data-stu-id="4fcf0-109">[Threat Protection Status report](view-email-security-reports.md#tps) (new!)</span></span> 
    
- [<span data-ttu-id="4fcf0-110">Rapport des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4fcf0-110">Malware Detections report</span></span>](view-email-security-reports.md#maldet)
    
- [<span data-ttu-id="4fcf0-111">Rapport de programmes malveillants supérieure</span><span class="sxs-lookup"><span data-stu-id="4fcf0-111">Top Malware report</span></span>](#top-malware-report)
    
- [<span data-ttu-id="4fcf0-112">État des expéditeurs et destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="4fcf0-112">Top Senders and Recipients report</span></span>](view-email-security-reports.md#topsenders)
    
- [<span data-ttu-id="4fcf0-113">Rapport de messagerie usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-113">Spoof Mail report</span></span>](#spoof-mail-report)
    
- [<span data-ttu-id="4fcf0-114">Rapport des détections de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4fcf0-114">Spam Detections report</span></span>](#spam-detections-report)
    
- [<span data-ttu-id="4fcf0-115">Rapport envoyés et reçus par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4fcf0-115">Sent and received email report</span></span>](view-email-security-reports.md#sentreceivedemail)
    
- <span data-ttu-id="4fcf0-116">[Rapport de messages signalés par les utilisateurs](view-email-security-reports.md#userreported) (nouveau) !</span><span class="sxs-lookup"><span data-stu-id="4fcf0-116">[User-reported messages report](view-email-security-reports.md#userreported) (new!)</span></span> 
    
## <a name="threat-protection-status-report-new"></a><span data-ttu-id="4fcf0-117">Menaces de rapport d’état de Protection (nouveau) !</span><span class="sxs-lookup"><span data-stu-id="4fcf0-117">Threat Protection Status report (new!)</span></span>

<span data-ttu-id="4fcf0-p103">Nouveau rapport **d’État de Protection de menace** est un rapport dynamique qui affiche la messagerie qui a été détecté et bloqué par Exchange Online Protection. Ce rapport affiche des informations sur le courrier identifié comme une tentative de hameçonnage ou de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p103">The new **Threat Protection Status** report is a smart report that shows malicious email that was detected and blocked by Exchange Online Protection. This report shows information about email identified as malware or a phishing attempt.</span></span> 

> [!NOTE]
> <span data-ttu-id="4fcf0-p104">Un rapport d’état de Protection de menace est disponible pour les clients qui ont des [Office 365 DAV](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP) ; Toutefois, les informations qui s’affiche dans le rapport d’état de Protection des menaces pour les clients disposant contiendra probablement que les clients EOP peuvent afficher des données différentes. Par exemple, clients EOP peuvent afficher plus d’informations sur les logiciels malveillants détectés dans le courrier électronique, mais pas plus d’informations sur [les fichiers malveillants détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](atp-for-spo-odb-and-teams.md), une fonctionnalité spécifique DAV. ([En savoir plus sur les rapports DAV](view-reports-for-atp.md)).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, EOP customers can view information about malware detected in email, but not information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md), an ATP-specific capability. ([Learn more about ATP reports](view-reports-for-atp.md).)</span></span>
  
<span data-ttu-id="4fcf0-123">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **État de Protection de menace**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-123">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Rapport d’état de Protection de menace](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
<span data-ttu-id="4fcf0-p105">Lorsque vous ouvrez le rapport d’état de Protection de menace, le rapport montre les données pour les sept derniers jours par défaut ; Vous pouvez toutefois, cliquez sur **filtres** et modifier la plage de dates pendant 90 jours de détail. Ce rapport est utile pour l’affichage de l’efficacité et l’impact des fonctionnalités d’Exchange Online Protection de votre organisation et pour l’analyse des tendances à long terme.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p105">When you first open the Threat Protection Status report, the report shows data for the past seven days by default; however, you can click **Filters** and change the date range for up to 90 days of detail. This report is useful for viewing the effectiveness and impact of your organization's Exchange Online Protection features, and for longer-term trending.</span></span> 
  
![Filtres du rapport d’état de la Protection des menaces](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
<span data-ttu-id="4fcf0-128">Vous pouvez également choisir si, pour afficher les données pour le courrier électronique identifié comme malveillants, e-mail identifié comme un hameçonnage tente ou courrier identifié comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-128">You can also choose whether to view data for email identified as malicious, email identified as a phishing attempts, or email identified as containing malware.</span></span>
  
![Options d’affichage du rapport état de la Protection des menaces](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a><span data-ttu-id="4fcf0-130">Rapport des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4fcf0-130">Malware Detections report</span></span>

<span data-ttu-id="4fcf0-131">Le rapport des **Détections de programmes malveillants** indique le nombre de messages entrant et sortant ont été détecté comme contenant des programmes malveillants de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-131">The **Malware Detections** report shows how many incoming and outgoing messages were detected as containing malware for your organization.</span></span> 
  
<span data-ttu-id="4fcf0-132">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Détections de programmes malveillants**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-132">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Malware Detections**.</span></span>
  
![Exemple de rapport Détections de programmes malveillants](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
<span data-ttu-id="4fcf0-p106">Similaire à d’autres rapports, comme le rapport d’état de Protection de menace, le rapport affiche données pour les sept derniers jours par défaut. Toutefois, vous pouvez choisir de **filtres** pour modifier la plage de dates.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p106">Similar to other reports, like the Threat Protection Status report, the report displays data for the past seven days by default. However, you can choose **Filters** to change the date range.</span></span> 
  
## <a name="top-malware-report"></a><span data-ttu-id="4fcf0-136">Rapport de programmes malveillants supérieure</span><span class="sxs-lookup"><span data-stu-id="4fcf0-136">Top Malware report</span></span>

<span data-ttu-id="4fcf0-137">Le rapport de **Programmes malveillants haut** montre les différents types de programme malveillant détecté par Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-137">The **Top Malware** report shows the various kinds of malware that was detected by Exchange Online.</span></span> 
  
<span data-ttu-id="4fcf0-138">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Malveillant haut**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-138">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Top Malware**.</span></span>
  
![SCC - EOP principaux programmes malveillants](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
<span data-ttu-id="4fcf0-140">Lorsque vous placez sur un coin du graphique en secteurs, vous pouvez voir le nom d’un type de programmes malveillants et le nombre de messages a été détecté comme ayant que les logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-140">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>
  
<span data-ttu-id="4fcf0-141">Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-141">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Ce rapport présente les principaux programmes malveillants détectés pour votre organisation](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
<span data-ttu-id="4fcf0-143">Sous le graphique, vous verrez une liste de programmes malveillants détectés et le nombre de messages a été détecté comme ayant que les logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-143">Below the chart, you'll see a list of detected malware and how many messages were detected as having that malware.</span></span>
  
## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="4fcf0-144">État des expéditeurs et destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="4fcf0-144">Top Senders and Recipients report</span></span>

<span data-ttu-id="4fcf0-145">Le rapport **principaux expéditeurs et destinataires** est un graphique en secteurs vos principaux expéditeurs d’e-mails.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-145">The **Top Senders and Recipients** report is a pie chart showing your top email senders.</span></span> 
  
<span data-ttu-id="4fcf0-146">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **principaux expéditeurs et destinataires**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-146">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Top Senders and Recipients**.</span></span>
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> principaux expéditeurs et destinataires](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
<span data-ttu-id="4fcf0-148">Lorsque vous placez sur un coin du graphique en secteurs, vous pouvez voir un nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-148">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>
  
<span data-ttu-id="4fcf0-149">Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-149">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="4fcf0-p107">Utilisez la liste **Afficher les données de** choisir d’afficher les données pour émetteurs, destinataires, destinataires du courrier indésirable et destinataires des programmes malveillants. Vous pouvez également voir qui a reçu le programme malveillant détecté par la protection contre les menaces avancées.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p107">Use the **Show data for** list to choose whether to view data for top senders, receivers, spam recipients, and malware recipients. You can also see who received malware that was detected by Advanced Threat Protection.</span></span> 
  
![Utilisez la liste Afficher les données pour afficher des informations spécifiques](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
<span data-ttu-id="4fcf0-153">Sous le graphique, vous verrez qui les expéditeurs de courriers supérieure ou destinataires ont été, ainsi que d’un nombre de messages envoyés ou reçus pour la période de temps donnée.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-153">Below the chart, you'll see who the top email senders or recipients were, along with a count of messages sent or received for the given time period.</span></span>
  
## <a name="spoof-mail-report"></a><span data-ttu-id="4fcf0-154">Rapport de messagerie usurpation d’identité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-154">Spoof Mail report</span></span>

<span data-ttu-id="4fcf0-155">Le rapport de **Messagerie de l’usurpation d’identité** indique le nombre de messages messagerie usurpation d’identité ont été détecté et parmi ceux-ci, celles qui ont été considérés comme étant « bon » (mail usurpation d’identité pour des raisons professionnelles légitimes).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-155">The **Spoof Mail** report shows how many spoof mail messages were detected, and of those, which ones were considered "good" (spoof mail done for legitimate business reasons).</span></span> 
  
<span data-ttu-id="4fcf0-156">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Messagerie usurpation d’identité**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-156">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Spoof Mail**.</span></span>
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> messagerie usurpation d’identité](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
<span data-ttu-id="4fcf0-158">Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre de messages messagerie usurpation d’identité fournie par le biais de.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-158">When you hover over a day in the chart, you can see how many spoof mail messages came through.</span></span>
  
<span data-ttu-id="4fcf0-159">Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-159">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
## <a name="spam-detections-report"></a><span data-ttu-id="4fcf0-160">Rapport des détections de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4fcf0-160">Spam Detections report</span></span>

<span data-ttu-id="4fcf0-161">Le rapport de **Détections de courrier indésirable** présente tout le contenu du courrier indésirable bloqué par Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-161">The **Spam Detections** report shows all the spam content blocked by Exchange Online.</span></span> 
  
<span data-ttu-id="4fcf0-162">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Détections de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-162">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Spam Detections**.</span></span>
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> détections de courrier indésirable d’EOP](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
<span data-ttu-id="4fcf0-p108">Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre d’éléments ont été bloqué dans la journée, ainsi que la manière dont les éléments sont classés. Par exemple, vous pouvez voir le nombre de messages de courrier indésirable ont été filtré, et le nombre d’éléments provenant d’une adresse IP (Internet Protocol) bloqués.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p108">When you hover over a day in the chart, you can see how many items were blocked that day, as well as how those items are categorized. For example, you can see how many spam messages were filtered, and how many items came from a blocked Internet Protocol (IP) address.</span></span>
  
<span data-ttu-id="4fcf0-166">Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-166">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
![Le rapport des détections de courrier indésirable indique le nombre de messages de courrier indésirable ont été bloqué ou filtré](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
<span data-ttu-id="4fcf0-p109">Sous le graphique, vous verrez une liste d’éléments de courrier indésirable détectés. Sélectionnez un élément pour afficher des informations supplémentaires, telles que si l’élément de courrier indésirable a été entrants ou sortants, son ID de message et son destinataire.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p109">Below the chart, you'll see a list of spam items that were detected. Select an item to view additional information, such as whether the spam item was inbound or outbound, its message ID, and its recipient.</span></span>
  
## <a name="sent-and-received-email-report"></a><span data-ttu-id="4fcf0-170">Rapport envoyés et reçus par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4fcf0-170">Sent and received email report</span></span>

<span data-ttu-id="4fcf0-171">Le rapport **envoyé et le courrier entrant** est un rapport dynamique qui affiche des informations sur les e-mails entrants et sortants, y compris les détections de courrier indésirable, les logiciels malveillants et e-mail identifié comme « bon ».</span><span class="sxs-lookup"><span data-stu-id="4fcf0-171">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> 
  
<span data-ttu-id="4fcf0-172">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **envoyés et le courrier entrant**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-172">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Sent and received email**.</span></span>
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> envoyés et le courrier entrant](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
<span data-ttu-id="4fcf0-p110">Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre de messages est arrivé, et comment ces messages sont classés. Par exemple, vous pouvez voir le nombre de messages qui ont été détecté comme contenant des programmes malveillants, et combien ont été identifiés comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p110">When you hover over a day in the chart, you can see how many messages came in, and how those messages are categorized. For example, you can see how many messages were detected as containing malware, and how many were identified as spam.</span></span>
  
<span data-ttu-id="4fcf0-176">Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-176">Click (or tap) the report to open it in a new browser window, where you can get a more detailed view of the report.</span></span>
  
<span data-ttu-id="4fcf0-177">Vous pouvez utiliser la liste **décomposer par** pour afficher les informations par type ou par le sens (entrant et sortant).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-177">You can use the **Break down by** list to view information by type or by direction (incoming and outgoing).</span></span> 
  
![Utilisez la liste arrêt vers le bas par pour afficher les informations par type ou la direction](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
<span data-ttu-id="4fcf0-p111">Sous le graphique, vous verrez une liste de catégories de messagerie, tels que **GoodMail**, **SpamContentFiltered**et ainsi de suite. Sélectionnez une catégorie pour afficher des informations supplémentaires, telles que les actions qui ont été prises pour les logiciels malveillants et si la messagerie est entrant ou sortant.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p111">Below the chart, you'll see a list of email categories, such as **GoodMail**, **SpamContentFiltered**, and so on. Select a category to view additional information, such as actions that were taken for malware, and whether email was incoming or outgoing.</span></span>
  
![Ce rapport vous informe des autres détections de message, anti-spam et contre les programmes malveillants](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a><span data-ttu-id="4fcf0-182">Rapport de messages signalés par les utilisateurs (nouveau) !</span><span class="sxs-lookup"><span data-stu-id="4fcf0-182">User-reported messages report (new!)</span></span>

<span data-ttu-id="4fcf0-183">Le rapport **messages signalés par les utilisateurs** présente des informations sur les messages électroniques que les utilisateurs ont signalé comme indésirable, les tentatives de hameçonnage ou bon courrier électronique à l’aide [complément de Message de rapport](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-183">The **User-reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md).</span></span>
  
<span data-ttu-id="4fcf0-p112">Plus d’informations sont disponibles pour chaque message, y compris le motif de livraison, une telle exception de stratégie de courrier indésirable ou règle de flux de messagerie configurées pour votre organisation. Pour afficher plus d’informations, sélectionnez un élément dans la liste des rapports à l’utilisateur, puis afficher les informations sur les onglets **Résumé** et les **Détails** .</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p112">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization. To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span> 
  
![Le rapport Messages User-Reported indique aux utilisateurs de messages marquées comme indésirable, pas indésirable ou hameçonnage tentatives.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
<span data-ttu-id="4fcf0-187">Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fcf0-187">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), do one of the following:</span></span>
  
- <span data-ttu-id="4fcf0-188">Accédez à **gestion de menace** \> **tableau de bord** \> **messages signalés par les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-188">Go to **Threat management** \> **Dashboard** \> **User-reported messages**.</span></span>
    
- <span data-ttu-id="4fcf0-189">Accédez à **gestion de menace** \> **révision** \> **messages signalés par les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-189">Go to **Threat management** \> **Review** \> **User-reported messages**.</span></span>
    
![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> révision \> messages indiqué par utilisateur](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> <span data-ttu-id="4fcf0-p113">Dans la commande pour le rapport messages signalés par les utilisateurs de fonctionner correctement, **l’enregistrement d’audit doit être activée** pour votre environnement Office 365. Cela s’effectue généralement par toute personne ayant le rôle journaux d’Audit affecté dans Exchange Online. Pour plus d’informations, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p113">In order for the User-reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="4fcf0-194">Les autorisations requises pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="4fcf0-194">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="4fcf0-195">Pour pouvoir afficher et utiliser les rapports décrits dans cet article, vous devez disposer d’un rôle approprié est affecté de la sécurité &amp; centre de conformité et le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fcf0-195">In order to view and use the reports described in this article, you must have an appropriate role assigned in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>

- <span data-ttu-id="4fcf0-196">Pour la sécurité &amp; centre de conformité, vous devez disposer d’un des rôles suivants est attribué :</span><span class="sxs-lookup"><span data-stu-id="4fcf0-196">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="4fcf0-197">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="4fcf0-197">Organization Management</span></span>
    - <span data-ttu-id="4fcf0-198">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-198">Security Administrator</span></span>
    - <span data-ttu-id="4fcf0-199">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-199">Security Reader</span></span>

- <span data-ttu-id="4fcf0-200">Pour Exchange Online, vous devez disposer d’un des rôles suivants est attribué :</span><span class="sxs-lookup"><span data-stu-id="4fcf0-200">For Exchange Online, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="4fcf0-201">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="4fcf0-201">Organization Management</span></span>
    - <span data-ttu-id="4fcf0-202">Gestion de l’organisation en affichage seul</span><span class="sxs-lookup"><span data-stu-id="4fcf0-202">View-only Organization Management</span></span>
    - <span data-ttu-id="4fcf0-203">Rôle Destinataires en affichage uniquement</span><span class="sxs-lookup"><span data-stu-id="4fcf0-203">View-Only Recipients role</span></span>
    - <span data-ttu-id="4fcf0-204">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-204">Compliance Management</span></span>

<span data-ttu-id="4fcf0-205">Pour plus d’informations, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fcf0-205">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="4fcf0-206">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-206">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="4fcf0-207">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4fcf0-207">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="4fcf0-208">Que se passe-t-il si les rapports ne sont pas affichant les données ?</span><span class="sxs-lookup"><span data-stu-id="4fcf0-208">What if the reports aren't showing data?</span></span>

<span data-ttu-id="4fcf0-p114">Si vous ne voyez pas les données dans vos rapports, vérifiez que vos stratégies sont correctement configurés. Pour plus d’informations, consultez la rubrique [protection contre le courrier indésirable et anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf0-p114">If you are not seeing data in your reports, double-check that your policies are set up correctly. To learn more, see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="4fcf0-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fcf0-211">Related topics</span></span>

[<span data-ttu-id="4fcf0-212">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="4fcf0-212">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="4fcf0-213">Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-213">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="4fcf0-214">Créer une planification pour un état de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-214">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="4fcf0-215">Configurer et télécharger un rapport personnalisé dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="4fcf0-215">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

