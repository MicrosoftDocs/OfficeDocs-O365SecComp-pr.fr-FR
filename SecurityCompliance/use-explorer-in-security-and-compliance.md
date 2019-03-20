---
title: Utiliser Threat Explorer dans le centre &amp; de sécurité conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Découvrez l'Explorateur (également appelé Explorateur de menaces) dans le &amp; Centre de sécurité conformité.
ms.openlocfilehash: 0c86792d8ed84b43b28bde31004dc95d2fa2b547
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693613"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="6958d-103">Utiliser Threat Explorer dans le centre &amp; de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="6958d-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="6958d-104">Si votre organisation dispose d' [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)et que vous disposez des autorisations nécessaires, vous pouvez utiliser l'Explorateur de menaces pour identifier et analyser les menaces.</span><span class="sxs-lookup"><span data-stu-id="6958d-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="6958d-105">Par exemple, vous pouvez identifier et supprimer un courrier électronique malveillant qui a été remis, ou consulter un programme malveillant qui a été intercepté par les fonctionnalités de sécurité d'Office 365.</span><span class="sxs-lookup"><span data-stu-id="6958d-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="6958d-106">L'Explorateur de menaces (également appelé Explorateur) est un outil puissant quasiment en temps réel pour aider les équipes des opérations de sécurité à examiner et à répondre &amp; aux menaces dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="6958d-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="6958d-108">Pour utiliser l'Explorateur, dans le &amp; Centre de sécurité conformité, accédez à l' **Explorateur**de **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="6958d-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6958d-109">Office 365 Threat Intelligence est désormais Office 365 Advanced Threat Protection Plan 2, ainsi que d'autres fonctionnalités de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="6958d-109">Office 365 Threat Intelligence is now Office 365 Advanced Threat Protection Plan 2, along with additional threat protection capabilities.</span></span> <span data-ttu-id="6958d-110">Pour en savoir plus, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="6958d-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="6958d-111">Vue d'ensemble de l'Explorateur</span><span class="sxs-lookup"><span data-stu-id="6958d-111">Explorer overview</span></span>

<span data-ttu-id="6958d-112">L'Explorateur affiche des informations sur les programmes malveillants suspects et les messages hameçons dans Office 365, ainsi que d'autres menaces et risques de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6958d-112">Explorer displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> <span data-ttu-id="6958d-113">Lorsque vous ouvrez l'Explorateur pour la première fois, l'affichage par défaut affiche les détections de programmes malveillants par courrier électronique pour les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6958d-113">When you first open Explorer, the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="6958d-114">Explorer peut également afficher les fonctionnalités de protection de la sécurité dans Office 365, notamment les [liens fiables](atp-safe-links.md) et [les pièces jointes fiables](atp-safe-attachments.md) , et peut être modifié pour afficher les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6958d-114">Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span> <span data-ttu-id="6958d-115">Si vous disposez d'une version d'évaluation de commun pour Office 365 Advanced Threat Protection Plan 2 ou Office 365 E5, vous ne verrez que les détections et les données de messagerie des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="6958d-115">If you have a trial subcription for Office 365 Advanced Threat Protection Plan 2 or Office 365 E5, you will only see detections and email data for the past 7 days.</span></span>
  
![L'Explorateur affiche des informations sur les programmes malveillants principaux et les utilisateurs ciblés](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="6958d-117">Utilisez le menu Affichage pour modifier les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="6958d-117">Use the View menu to change what information is displayed.</span></span>
  
![Menu Affichage de l'Explorateur](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="6958d-119">L'Explorateur dispose de plusieurs fonctionnalités de filtrage et d'interrogation qui vous permettent d'explorer les détails, tels que les principaux utilisateurs ciblés, les principales familles de programmes malveillants, la technologie de détection et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="6958d-119">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="6958d-120">Chaque type de rapport offre plusieurs façons d'afficher et d'explorer les données.</span><span class="sxs-lookup"><span data-stu-id="6958d-120">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6958d-121">N'utilisez pas de caractères génériques, tels qu'un astérisque (\*) ou un point d'interrogation (?), avec l'Explorateur.</span><span class="sxs-lookup"><span data-stu-id="6958d-121">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer.</span></span> <span data-ttu-id="6958d-122">Lorsque vous effectuez une recherche dans le champ Subject pour les messages électroniques, l'Explorateur effectue une correspondance partielle et génère des résultats similaires à une recherche par caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="6958d-122">When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="6958d-123">Courrier \> malveillant de messagerie</span><span class="sxs-lookup"><span data-stu-id="6958d-123">Email \> Malware</span></span>

<span data-ttu-id="6958d-124">Cet affichage montre les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="6958d-124">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="6958d-125">Afficher les informations dans le graphique par famille de programmes malveillants, domaine de l'expéditeur, adresse IP de l'expéditeur, état de protection (actions prises par les fonctionnalités et stratégies de protection contre les menaces dans Office 365) et technologie de détection (comment le programme malveillant a été détecté).</span><span class="sxs-lookup"><span data-stu-id="6958d-125">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="6958d-127">Sous le graphique, affichez les détails des principales familles de programmes malveillants, des utilisateurs ciblés le plus ciblés et d'autres détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6958d-127">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="6958d-128">Courrier \> hameçon</span><span class="sxs-lookup"><span data-stu-id="6958d-128">Email \> Phish</span></span>

<span data-ttu-id="6958d-129">Cet affichage montre les messages électroniques identifiés comme des tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6958d-129">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="6958d-130">Afficher les informations par domaine de l'expéditeur, adresse IP de l'expéditeur et état de protection (actions prises par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365).</span><span class="sxs-lookup"><span data-stu-id="6958d-130">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Afficher les données sur l'e-mail identifiées comme tentatives de hameçonnage](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="6958d-132">Sous le graphique, affichez plus de détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6958d-132">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="6958d-133">E-mail \> signalé par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="6958d-133">Email \> User-reported</span></span>

<span data-ttu-id="6958d-134">Cet affichage montre le courrier électronique que les utilisateurs ont signalés comme courrier indésirable, non légitime ou courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="6958d-134">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="6958d-135">Afficher les informations par type de rapport (indique que l'utilisateur a déterminé qu'il s'agit d'un courrier indésirable, n'est pas un courrier indésirable ou un hameçonnage), et par raison du motif de remise (pourquoi les messages ont été envoyés à un emplacement spécifique, comme une stratégie de filtrage du courrier indésirable, une règle de flux de messagerie, une liste d'expéditeurs etc.).</span><span class="sxs-lookup"><span data-stu-id="6958d-135">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Afficher des données sur les utilisateurs de messagerie signalés comme indésirables, non légitimes ou par hameçonnage](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="6958d-137">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, l'adresse IP de l'expéditeur, l'utilisateur qui a signalé le message comme courrier indésirable, légitime, ou hameçon, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="6958d-137">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="6958d-138">Courrier \> électronique de tous les messages</span><span class="sxs-lookup"><span data-stu-id="6958d-138">Email \> All mail</span></span>

<span data-ttu-id="6958d-139">Cette vue affiche une vue d'ensemble de l'activité de messagerie, y compris le courrier électronique identifié comme malveillant en raison d'un hameçonnage ou d'un programme malveillant, ainsi que tous les messages non malveillants (e-mail normal, courrier indésirable et courrier en nombre).</span><span class="sxs-lookup"><span data-stu-id="6958d-139">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="6958d-140">Si vous obtenez une erreur indiquant un **trop grand nombre de données à afficher**, ajoutez un filtre et, si nécessaire, Affinez la plage de dates que vous visualisez.</span><span class="sxs-lookup"><span data-stu-id="6958d-140">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="6958d-141">Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="6958d-141">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="6958d-142">Dans notre exemple, nous avons utilisé la **technologie de détection** en tant que filtre (plusieurs options sont disponibles).</span><span class="sxs-lookup"><span data-stu-id="6958d-142">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="6958d-143">Afficher les informations de l'expéditeur, du domaine de l'expéditeur, des destinataires, de l'objet, du nom de fichier de la pièce jointe, de la famille de programmes malveillants, du statut de protection (actions effectuées par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365), de la technologie de détection (comment le programme malveillant a été détecté) et plus d'.</span><span class="sxs-lookup"><span data-stu-id="6958d-143">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Afficher les données sur les messages détectés par la technologie de détection](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="6958d-145">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, le destinataire, l'expéditeur, l'État, etc.</span><span class="sxs-lookup"><span data-stu-id="6958d-145">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="6958d-146">Programme \> malveillant de contenu</span><span class="sxs-lookup"><span data-stu-id="6958d-146">Content \> Malware</span></span>

<span data-ttu-id="6958d-147">Cet affichage montre les fichiers identifiés comme étant malveillants par Office 365 protection avancée contre les menaces dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6958d-147">This view shows files that were identified as malicious by Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="6958d-148">Afficher des informations par famille de programmes malveillants, technologie de détection (comment le programme malveillant a été détecté) et charge de travail (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="6958d-148">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="6958d-150">Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de la pièce jointe, la charge de travail, la taille du fichier, la dernière personne qui a modifié le fichier, etc.</span><span class="sxs-lookup"><span data-stu-id="6958d-150">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="6958d-151">(Nouveau!) Fonctionnalités de cliquer-filtrer</span><span class="sxs-lookup"><span data-stu-id="6958d-151">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="6958d-152">La nouveauté d'Explorer est la possibilité de cliquer pour filtrer.</span><span class="sxs-lookup"><span data-stu-id="6958d-152">New to Explorer is the ability to click to filter.</span></span> <span data-ttu-id="6958d-153">Lorsque vous cliquez sur un élément dans la légende, cet élément devient un filtre pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="6958d-153">When you click an item in the legend, that item becomes a filter for the report.</span></span> <span data-ttu-id="6958d-154">Par exemple, supposons que nous examinons l'affichage programmes malveillants dans l'Explorateur:</span><span class="sxs-lookup"><span data-stu-id="6958d-154">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="6958d-156">Si \*\*\*\* vous cliquez sur détonation de la protection avancée contre les menaces dans ce graphique, les résultats sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="6958d-156">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorateur filtré pour afficher uniquement les résultats de la déTonation ATO](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="6958d-158">Dans cet affichage, nous examinons à présent les données des fichiers qui ont été détonants par [les pièces jointEs approuvées par Office 365 ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="6958d-158">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="6958d-159">Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques qui avaient des pièces jointes détectées par des pièces jointes sûres ATP.</span><span class="sxs-lookup"><span data-stu-id="6958d-159">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Détails spécifiques sur les messages électroniques avec des pièces jointes détectées](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="6958d-161">La sélection d'un ou de plusieurs éléments active le menu **actions** , qui offre plusieurs choix parmi lesquels choisir pour les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="6958d-161">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![La sélection d'un élément active le menu actions](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="6958d-163">La possibilité de filtrer un clic et d'accéder à des détails spécifiques peut vous faire gagner du temps lors de l'enquête sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="6958d-163">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="6958d-164">Comment puis-je obtenir Explorer?</span><span class="sxs-lookup"><span data-stu-id="6958d-164">How do I get Explorer?</span></span>

<span data-ttu-id="6958d-165">L'Explorateur est inclus dans [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="6958d-165">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="6958d-166">Vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou à un lecteur de sécurité, afin d'afficher et d'utiliser l'Explorateur.</span><span class="sxs-lookup"><span data-stu-id="6958d-166">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer.</span></span> <span data-ttu-id="6958d-167">Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6958d-167">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="6958d-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6958d-168">Related topics</span></span>

[<span data-ttu-id="6958d-169">Rapports et informations dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="6958d-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="6958d-170">Rechercher et identifier les messages électroniques malveillants qui ont été remis (Office 365 Threat Invesitgation and Response)</span><span class="sxs-lookup"><span data-stu-id="6958d-170">Find and investigate malicious email that was delivered (Office 365 Threat Invesitgation and Response)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="6958d-171">Protection contre le courrier indésirable et les programmes malveillants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6958d-171">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

