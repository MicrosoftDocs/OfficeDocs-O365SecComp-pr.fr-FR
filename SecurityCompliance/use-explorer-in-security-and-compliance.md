---
title: Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
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
ms.openlocfilehash: 4a28626d0e643d7a7b96a34656e7678c71a86c66
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241966"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="58c9f-103">Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="58c9f-103">Use Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="58c9f-p101">Si votre organisation dispose d' [Office 365 Threat Intelligence](office-365-ti.md)et que vous disposez des autorisations nécessaires, vous pouvez utiliser l'Explorateur pour identifier et analyser les menaces. Par exemple, vous pouvez identifier et supprimer un courrier électronique malveillant qui a été remis, ou consulter un programme malveillant qui a été intercepté par les fonctionnalités de sécurité d'Office 365. L'Explorateur (également appelé «Explorateur de menaces») est un très puissant rapport en temps réel dans &amp; le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p101">If your organization has [Office 365 Threat Intelligence](office-365-ti.md), and you have the necessary permissions, you can use Explorer to identify and analyze threats. For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features. Explorer (also referred to as Threat Explorer) is a powerful near real-time report in the Security &amp; Compliance Center.</span></span>
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="58c9f-108">Pour utiliser l'Explorateur, dans le &amp; Centre de sécurité conformité, accédez à l' **Explorateur**de **gestion** \> des menaces.</span><span class="sxs-lookup"><span data-stu-id="58c9f-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58c9f-p102">Depuis le mois de février 2019 et le déploiement sur les prochains mois, Office 365 Threat Intelligence est devenu Office 365 Advanced Threat Protection Plan 2, avec des fonctionnalités supplémentaires de protection contre les menaces. Pour en savoir plus, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="58c9f-p102">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="58c9f-111">Vue d'ensemble de l'Explorateur</span><span class="sxs-lookup"><span data-stu-id="58c9f-111">Explorer overview</span></span>

<span data-ttu-id="58c9f-p103">L'Explorateur affiche des informations sur les programmes malveillants suspects dans les messages électroniques et les fichiers dans Office 365, ainsi que d'autres menaces et risques de sécurité pour votre organisation. Lorsque vous ouvrez l'Explorateur pour la première fois, la vue par défaut affiche des détections de programmes malveillants depuis les 7 derniers jours. Explorer peut également afficher les fonctionnalités de protection de la sécurité dans Office 365, notamment les [liens fiables](atp-safe-links.md) et [les pièces jointes fiables](atp-safe-attachments.md) , et peut être modifié pour afficher les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p103">Explorer displays information about suspected malware in email and files in Office 365, as well as other security threats and risks to your organization. When you first open Explorer, the default view shows malware detections from antivirus for the past 7 days. Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span>
  
![L'Explorateur affiche des informations sur les programmes malveillants principaux et les utilisateurs ciblés](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="58c9f-116">Utilisez le menu Affichage pour modifier les informations affichées.</span><span class="sxs-lookup"><span data-stu-id="58c9f-116">Use the View menu to change what information is displayed.</span></span>
  
![Menu Affichage de l'Explorateur](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="58c9f-p104">L'Explorateur dispose de plusieurs fonctionnalités de filtrage et d'interrogation qui vous permettent d'explorer les détails, tels que les principaux utilisateurs ciblés, les principales familles de programmes malveillants et bien plus encore. Chaque type de rapport offre plusieurs façons d'afficher et d'explorer les données.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p104">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, and more. Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58c9f-p105">N'utilisez pas de caractères génériques, tels qu'un astérisque (\*) ou un point d'interrogation (?), avec l'Explorateur. Lorsque vous effectuez une recherche dans le champ Subject pour les messages électroniques, l'Explorateur effectue une correspondance partielle et génère des résultats similaires à une recherche par caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p105">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer. When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="58c9f-122">Courrier \> malveillant de messagerie</span><span class="sxs-lookup"><span data-stu-id="58c9f-122">Email \> Malware</span></span>

<span data-ttu-id="58c9f-123">Cet affichage montre les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="58c9f-123">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="58c9f-124">Afficher les informations dans le graphique par famille de programmes malveillants, domaine de l'expéditeur, adresse IP de l'expéditeur, état de protection (actions prises par les fonctionnalités et stratégies de protection contre les menaces dans Office 365) et technologie de détection (comment le programme malveillant a été détecté).</span><span class="sxs-lookup"><span data-stu-id="58c9f-124">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="58c9f-126">Sous le graphique, affichez les détails des principales familles de programmes malveillants, des utilisateurs ciblés le plus ciblés et d'autres détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="58c9f-126">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="58c9f-127">Courrier \> hameçon</span><span class="sxs-lookup"><span data-stu-id="58c9f-127">Email \> Phish</span></span>

<span data-ttu-id="58c9f-128">Cet affichage montre les messages électroniques identifiés comme des tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="58c9f-128">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="58c9f-129">Afficher les informations par domaine de l'expéditeur, adresse IP de l'expéditeur et état de protection (actions prises par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365).</span><span class="sxs-lookup"><span data-stu-id="58c9f-129">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Afficher les données sur l'e-mail identifiées comme tentatives de hameçonnage](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="58c9f-131">Sous le graphique, affichez plus de détails sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="58c9f-131">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="58c9f-132">E-mail \> signalé par l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="58c9f-132">Email \> User-reported</span></span>

<span data-ttu-id="58c9f-133">Cet affichage montre le courrier électronique que les utilisateurs ont signalés comme courrier indésirable, non légitime ou courrier électronique de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="58c9f-133">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="58c9f-134">Afficher les informations par type de rapport (indique que l'utilisateur a déterminé qu'il s'agit d'un courrier indésirable, n'est pas un courrier indésirable ou un hameçonnage), et par raison du motif de remise (pourquoi les messages ont été envoyés à un emplacement spécifique, comme une stratégie de filtrage du courrier indésirable, une règle de flux de messagerie, une liste d'expéditeurs etc.).</span><span class="sxs-lookup"><span data-stu-id="58c9f-134">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Afficher des données sur les utilisateurs de messagerie signalés comme indésirables, non légitimes ou par hameçonnage](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="58c9f-136">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, l'adresse IP de l'expéditeur, l'utilisateur qui a signalé le message comme courrier indésirable, légitime, ou hameçon, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="58c9f-136">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="58c9f-137">Courrier \> électronique de tous les messages</span><span class="sxs-lookup"><span data-stu-id="58c9f-137">Email \> All mail</span></span>

<span data-ttu-id="58c9f-138">Cette vue affiche une vue d'ensemble de l'activité de messagerie, y compris le courrier électronique identifié comme malveillant en raison d'un hameçonnage ou d'un programme malveillant, ainsi que tous les messages non malveillants (e-mail normal, courrier indésirable et courrier en nombre).</span><span class="sxs-lookup"><span data-stu-id="58c9f-138">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="58c9f-139">Si vous obtenez une erreur indiquant un **trop grand nombre de données à afficher**, ajoutez un filtre et, si nécessaire, Affinez la plage de dates que vous visualisez.</span><span class="sxs-lookup"><span data-stu-id="58c9f-139">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="58c9f-p106">Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser. Dans notre exemple, nous avons utilisé la **technologie de détection** en tant que filtre (plusieurs options sont disponibles). Afficher les informations de l'expéditeur, du domaine de l'expéditeur, des destinataires, de l'objet, du nom de fichier de la pièce jointe, de la famille de programmes malveillants, du statut de protection (actions effectuées par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365), de la technologie de détection (comment le programme malveillant a été détecté) et plus d'.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p106">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button. In our example, we used **Detection technology** as a filter (there are several options available). View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Afficher les données sur les messages détectés par la technologie de détection](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="58c9f-144">Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, le destinataire, l'expéditeur, l'État, etc.</span><span class="sxs-lookup"><span data-stu-id="58c9f-144">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="58c9f-145">Programme \> malveillant de contenu</span><span class="sxs-lookup"><span data-stu-id="58c9f-145">Content \> Malware</span></span>

<span data-ttu-id="58c9f-146">Cet affichage montre les fichiers identifiés comme étant malveillants dans SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="58c9f-146">This view shows files that were identified as malicious in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="58c9f-147">Afficher des informations par famille de programmes malveillants, technologie de détection (comment le programme malveillant a été détecté) et charge de travail (OneDrive, SharePoint ou Teams).</span><span class="sxs-lookup"><span data-stu-id="58c9f-147">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="58c9f-149">Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de la pièce jointe, la charge de travail, la taille du fichier, la dernière personne qui a modifié le fichier, etc.</span><span class="sxs-lookup"><span data-stu-id="58c9f-149">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="58c9f-150">(Nouveau!) Fonctionnalités de cliquer-filtrer</span><span class="sxs-lookup"><span data-stu-id="58c9f-150">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="58c9f-p107">La nouveauté d'Explorer est la possibilité de cliquer pour filtrer. À compter du 2018 mai, lorsque vous cliquez sur un élément dans la légende, cet élément devient un filtre pour le rapport. Par exemple, supposons que nous examinons l'affichage programmes malveillants dans l'Explorateur:</span><span class="sxs-lookup"><span data-stu-id="58c9f-p107">New to Explorer is the ability to click to filter. Beginning in late May 2018, when you click an item in the legend, that item becomes a filter for the report. For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="58c9f-155">Si \*\*\*\* vous cliquez sur détonation de la protection avancée contre les menaces dans ce graphique, les résultats sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="58c9f-155">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorateur filtré pour afficher uniquement les résultats de la déTonation ATO](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="58c9f-p108">Dans cet affichage, nous examinons à présent les données des fichiers qui ont été détonants par [les pièces jointEs approuvées par Office 365 ATP](atp-safe-attachments.md). Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques qui avaient des pièces jointes détectées par des pièces jointes sûres ATP.</span><span class="sxs-lookup"><span data-stu-id="58c9f-p108">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md). Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Détails spécifiques sur les messages électroniques avec des pièces jointes détectées](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="58c9f-160">La sélection d'un ou de plusieurs éléments active le menu **actions** , qui offre plusieurs choix parmi lesquels choisir pour les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="58c9f-160">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![La sélection d'un élément active le menu actions](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="58c9f-162">La possibilité de filtrer un clic et d'accéder à des détails spécifiques peut vous faire gagner du temps lors de l'enquête sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="58c9f-162">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="58c9f-163">Comment puis-je obtenir Explorer?</span><span class="sxs-lookup"><span data-stu-id="58c9f-163">How do I get Explorer?</span></span>

<span data-ttu-id="58c9f-164">L'Explorateur est inclus dans [Office 365 Threat Intelligence](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="58c9f-164">Explorer is included in [Office 365 Threat Intelligence](office-365-ti.md).</span></span> 

<span data-ttu-id="58c9f-p109">Vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou à un lecteur de sécurité, afin d'afficher et d'utiliser l'Explorateur. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="58c9f-p109">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="58c9f-167">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="58c9f-167">Related topics</span></span>

[<span data-ttu-id="58c9f-168">Rapports et informations dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="58c9f-168">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="58c9f-169">Rechercher et identifier les messages électroniques malveillants qui ont été remis (Office 365 Threat Intelligence)</span><span class="sxs-lookup"><span data-stu-id="58c9f-169">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="58c9f-170">Protection contre le courrier indésirable et les programmes malveillants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="58c9f-170">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

