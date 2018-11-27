---
title: Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
description: En savoir plus sur l’Explorateur de solutions (également appelé Threat Explorer) dans la sécurité &amp; centre de conformité.
ms.openlocfilehash: 1b3088028651b445d890333a25804902843d915d
ms.sourcegitcommit: 7f45890ecfa5e15575df4e3ebe472a8dd8d99112
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2018
ms.locfileid: "26674919"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="75d7c-103">Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="75d7c-103">Use Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="75d7c-p101">Si votre organisation dispose [d’Informations sur les menaces Office 365](office-365-ti.md)et que vous disposez des autorisations nécessaires, vous pouvez utiliser l’Explorateur de solutions pour identifier et analyser les menaces. Par exemple, vous pouvez identifier et supprimer le courrier électronique malveillant qui a été remis ou voir des programmes malveillants qui a été détectée par les fonctionnalités de sécurité d’Office 365. Explorateur de solutions (également appelé Explorateur menace) est une puissante près de rapports en temps réel de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p101">If your organization has [Office 365 Threat Intelligence](office-365-ti.md), and you have the necessary permissions, you can use Explorer to identify and analyze threats. For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features. Explorer (also referred to as Threat Explorer) is a powerful near real-time report in the Security &amp; Compliance Center.</span></span>
  
![Accédez à gestion de menace \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="75d7c-108">Pour utiliser l’Explorateur de solutions, dans la sécurité &amp; centre de conformité, accédez à la **Gestion des menaces** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="75d7c-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="75d7c-109">Vue d’ensemble de l’Explorateur de solutions</span><span class="sxs-lookup"><span data-stu-id="75d7c-109">Explorer overview</span></span>

<span data-ttu-id="75d7c-p102">Explorateur de solutions affiche des informations sur soupçonnés d’être anti-programme malveillant dans le message électronique fichiers dans Office 365, ainsi que les menaces de sécurité et autres risques à votre organisation. Lorsque vous ouvrez Explorateur de solutions, la vue par défaut affiche les détections de programmes malveillants d’antivirus pour les 7 derniers jours. Explorateur de solutions permettre également afficher sécurité fonctionnalités de protection dans Office 365, notamment des [Liens fiables](atp-safe-links.md) et les [Pièces jointes fiables](atp-safe-attachments.md) et peut être modifié pour afficher les données pour les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p102">Explorer displays information about suspected malware in email and files in Office 365, as well as other security threats and risks to your organization. When you first open Explorer, the default view shows malware detections from antivirus for the past 7 days. Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span>
  
![Explorateur affiche des informations sur les principaux programmes malveillants et ciblé aux utilisateurs](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="75d7c-114">Pour modifier les informations affichées, utilisez le menu Affichage.</span><span class="sxs-lookup"><span data-stu-id="75d7c-114">Use the View menu to change what information is displayed.</span></span>
  
![Le menu Affichage de l’Explorateur de solutions](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="75d7c-p103">Explorateur de solutions a plusieurs filtrage et interrogation des fonctionnalités qui vous permettent d’examiner les détails, tels que haut ciblés utilisateurs et familles principaux programmes malveillants. Chaque type de rapport offre plusieurs manières d’afficher et Explorer les données.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p103">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, and more. Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75d7c-p104">Ne pas utiliser de caractères génériques, comme un astérisque (\*) ou un point d’interrogation ( ?), avec l’Explorateur de solutions. Lorsque vous recherchez dans le champ objet pour les messages électroniques, Explorer effectuera rendement et mise en correspondance des résultats partiels similaires à une recherche par caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p104">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer. When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="75d7c-120">Messagerie \> programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="75d7c-120">Email \> Malware</span></span>

<span data-ttu-id="75d7c-121">Cet affichage montre les messages électroniques identifiés comme contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="75d7c-121">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="75d7c-122">Afficher des informations dans le graphique à la famille de logiciels malveillants, domaine de l’expéditeur, IP de l’expéditeur, l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365) et technologie de détection (comment le programme malveillant détecté).</span><span class="sxs-lookup"><span data-stu-id="75d7c-122">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="75d7c-124">Sous le graphique, afficher les détails des familles principaux programmes malveillants, haut destiné aux utilisateurs et plus d’informations sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="75d7c-124">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="75d7c-125">Messagerie \> hameçonnage</span><span class="sxs-lookup"><span data-stu-id="75d7c-125">Email \> Phish</span></span>

<span data-ttu-id="75d7c-126">Cet affichage montre les messages électroniques identifiés comme les tentatives de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="75d7c-126">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="75d7c-127">Afficher des informations à l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365), IP de l’expéditeur et le domaine de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="75d7c-127">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Afficher les données sur le courrier électronique identifié comme tentatives de hameçonnage](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="75d7c-129">Sous le graphique, permet d’afficher plus d’informations sur des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="75d7c-129">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="75d7c-130">Messagerie \> signalés par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="75d7c-130">Email \> User-reported</span></span>

<span data-ttu-id="75d7c-131">Cet affichage montre électroniques que les utilisateurs ont signalé comme indésirable, pas indésirable ou hameçonnage e-mail.</span><span class="sxs-lookup"><span data-stu-id="75d7c-131">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="75d7c-132">Afficher les informations par type de rapport (détermination de l’utilisateur que le courrier électronique a été indésirable, pas indésirable ou hameçonnage) et le motif de livraison (raisons pourquoi messagerie est passée à un emplacement spécifique, par exemple une stratégie de filtrage du courrier indésirable, une règle de flux de messagerie, une liste des expéditeurs bloqués, une liste des expéditeurs, etc.).</span><span class="sxs-lookup"><span data-stu-id="75d7c-132">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Afficher les données sur les utilisateurs de messagerie signalé comme indésirable, pas indésirable ou hameçonnage](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="75d7c-134">Sous le graphique, permet d’afficher plus d’informations sur les e-mails spécifiques, telles que la ligne objet, adresse IP de l’expéditeur, l’utilisateur qui a signalé le message comme indésirable courrier indésirable, ou hameçonnage et non plus.</span><span class="sxs-lookup"><span data-stu-id="75d7c-134">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="75d7c-135">Messagerie \> tous les messages</span><span class="sxs-lookup"><span data-stu-id="75d7c-135">Email \> All mail</span></span>

<span data-ttu-id="75d7c-136">Cet affichage présente une vue de toutes les d’activité de courrier électronique, y compris courrier identifié comme malveillants due à l’hameçonnage ou des programmes malveillants, ainsi que tous les messages non malveillantes (messagerie normal, spam et courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="75d7c-136">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="75d7c-137">Si vous obtenez une erreur indiquant **trop grande quantité de données afficher**, ajouter un filtre et, si nécessaire, limitez la plage de dates que vous visualisez.</span><span class="sxs-lookup"><span data-stu-id="75d7c-137">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="75d7c-p105">Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton d’actualisation. Dans notre exemple, nous avons utilisé la **technologie de détection** comme filtre (il existe plusieurs options disponibles). Afficher des informations à l’expéditeur, domaine de l’expéditeur, destinataires, subject, nom de fichier de pièce jointe, famille de logiciels malveillants, l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365), technologie de détection (comment le programme malveillant détecté), et plus.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p105">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button. In our example, we used **Detection technology** as a filter (there are several options available). View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Afficher les données sur l’e-mail détecté par la technologie de détection](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="75d7c-142">Sous le graphique, permet d’afficher plus d’informations sur les messages de messagerie spécifiques, telles que la ligne objet, destinataire, expéditeur, statut et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="75d7c-142">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="75d7c-143">Contenu \> programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="75d7c-143">Content \> Malware</span></span>

<span data-ttu-id="75d7c-144">Cet affichage indique les fichiers qui ont été identifiés comme malveillants dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft.</span><span class="sxs-lookup"><span data-stu-id="75d7c-144">This view shows files that were identified as malicious in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="75d7c-145">Afficher les informations par la technologie de détection famille, de programmes malveillants (comment le programme malveillant détecté) et la charge de travail (SharePoint, OneDrive ou équipes).</span><span class="sxs-lookup"><span data-stu-id="75d7c-145">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="75d7c-147">Sous le graphique, permet d’afficher plus d’informations sur les fichiers spécifiques, telles que le nom de fichier de pièce jointe, la charge de travail, la taille de fichier qui a modifié le fichier et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="75d7c-147">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="75d7c-148">(Nouveau) ! Cliquez sur-filtre de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="75d7c-148">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="75d7c-p106">Nouveau pour Explorer est la possibilité de cliquer sur pour filtrer. Liaison tardive 2018 mai, lorsque vous cliquez sur un élément dans la légende, à partir de cet élément devienne un filtre pour le rapport. Par exemple, supposons que nous cherchons à l’affichage de programmes malveillants dans l’Explorateur de solutions :</span><span class="sxs-lookup"><span data-stu-id="75d7c-p106">New to Explorer is the ability to click to filter. Beginning in late May 2018, when you click an item in the legend, that item becomes a filter for the report. For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Accédez à gestion de menace \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="75d7c-153">En cliquant sur **DAV détonation** dans les résultats de ce graphique dans un affichage semblable à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="75d7c-153">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer filtré pour afficher uniquement les résultats de détonation assembler](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="75d7c-p107">Dans cet affichage, nous recherchons maintenant au niveau des données pour les fichiers qui ont été detonated par [Office 365 DAV approuvés en pièce jointe](atp-safe-attachments.md). Sous le graphique, nous pouvons voir plus d’informations sur les messages électroniques spécifiques qui avaient des pièces jointes qui ont été détectés par les pièces jointes sûres DAV.</span><span class="sxs-lookup"><span data-stu-id="75d7c-p107">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md). Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Détails spécifiques sur les messages électroniques contenant des pièces jointes détectés](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="75d7c-158">Sélection d’un ou plusieurs éléments Active le menu **Actions** , ce qui offre plusieurs options parmi lesquelles choisir pour les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="75d7c-158">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Sélection d’un élément Active le menu Actions](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="75d7c-160">La possibilité de filtrer en un clic et accédez à des détails spécifiques permettre enregistrer beaucoup de temps dans l’analyse des menaces.</span><span class="sxs-lookup"><span data-stu-id="75d7c-160">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="75d7c-161">Comment obtenir de l’Explorateur de solutions ?</span><span class="sxs-lookup"><span data-stu-id="75d7c-161">How do I get Explorer?</span></span>

<span data-ttu-id="75d7c-162">Explorer est inclus dans [Office 365 menaces](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="75d7c-162">Explorer is included in [Office 365 Threat Intelligence](office-365-ti.md).</span></span> 

<span data-ttu-id="75d7c-p108">Vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou un lecteur de sécurité, afin d’afficher et utiliser l’Explorateur de solutions. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="75d7c-p108">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="75d7c-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d7c-165">Related topics</span></span>

[<span data-ttu-id="75d7c-166">Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="75d7c-166">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="75d7c-167">Rechercher et vérifier le courrier électronique malveillant qui a été remis (Office 365 Threat Intelligence)</span><span class="sxs-lookup"><span data-stu-id="75d7c-167">Find and investigate malicious email that was delivered (Office 365 Threat Intelligence)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="75d7c-168">Protection contre le courrier indésirable et les programmes malveillants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="75d7c-168">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

