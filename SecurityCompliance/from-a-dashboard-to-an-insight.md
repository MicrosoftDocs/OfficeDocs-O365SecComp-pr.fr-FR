---
title: Procédure pas à pas. D’un tableau de bord à un aperçu
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
description: Découvrez comment vous pouvez passer un tableau de bord pour un aperçu des actions recommandées dans la sécurité &amp; centre de conformité.
ms.openlocfilehash: 933bf6e86bc1ddce9259d071b69654f68e4dd370
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706148"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="dd9a9-103">Procédure pas à pas. D’un tableau de bord à un aperçu</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="dd9a9-104">Si vous utilisez pour [des rapports et des vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md), il peut vous aider à voir comment vous pouvez accéder facilement à partir d’un tableau de bord à un aperçu et les actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="dd9a9-p101">Il s’agit d’une des procédures pas à pas plusieurs pour la sécurité &amp; centre de conformité. Pour voir les procédures pas à pas supplémentaires, consultez la section [Rubriques connexes](#related-topics) .</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p101">This is one of several walkthroughs for the Security &amp; Compliance Center. To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="dd9a9-107">Procédure pas à pas : à partir d’un tableau de bord pour un aperçu</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="dd9a9-p102">Examinons le flux à partir d’un tableau de bord à un rapport à un aperçu et une action. (Ceci est un exemple brève [aide à la décision usurpation d’identité](learn-about-spoof-intelligence.md) .)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p102">Let's walk through the flow from a dashboard to a report to an insight and action. (This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="dd9a9-p103">Nous commençons par le tableau de bord de sécurité dans le [sécurité &amp; centre de conformité](https://security.microsoft.com). (Accédez à **gestion de menace** \> **tableau de bord**.)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p103">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://security.microsoft.com). (Go to **Threat management** \> **Dashboard**.)</span></span>
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> tableau de bord](media/05a38660-eb13-4960-a266-11809c453d95.png)
  
2. <span data-ttu-id="dd9a9-p104">Dans la ligne **Insights** , nous constatons un aperçu indiquant que nous devons examiner certains domaines susceptibles d’être suspects. (Dans la ligne de **Détails** , cliquez sur **les paires de domaine**).</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p104">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious. (In the **Insights** row, click **Domain pairs**.)</span></span>
    
    ![La ligne Insights mentionne les problèmes potentiels usurpation d’identité](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)
  
3. <span data-ttu-id="dd9a9-p105">Nous obtenir la liste des activités liées à l’usurpation d’aide à la décision. Il s’agit d’instances où les messages électroniques ont été envoyés qui semblent provient de notre organisation, mais, en fait, envoyés à partir d’une autre organisation. L’objectif est de déterminer si les messages usurpés sont autorisés ou non.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p105">We get a list of activities related to spoof intelligence. These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization. The goal is to determine whether the spoofed messages are authorized or not.</span></span>
    
    ![Informations d’aide à la décision usurpation d’identité](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)
  
    <span data-ttu-id="dd9a9-p106">Dans cette liste, nous pouvons trier les informations par le nombre de messages et l’usurpation dernière détection de date. (Cliquez sur les en-têtes de colonne, telles que **Message compter** ou **dernière détection** pour voir comment tri works.)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p106">In this list, we can sort the information by message count, date the spoofing was last detected, and more. (Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="dd9a9-p107">Sélection d’un élément dans la liste s’ouvre un volet où nous pouvons voir plus d’informations, y compris les messages électroniques similaires qui ont été détectés. (Cliquez sur un élément dans la liste et passez en revue les informations et les recommandations).</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p107">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected. (Click an item in the list, and review the information and recommendations.)</span></span>
    
    ![Sélection d’un élément s’ouvre un volet d’informations](media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)
  
5. <span data-ttu-id="dd9a9-p108">Notez qu’en haut du volet, nous ont la possibilité d’ajouter l’expéditeur à la liste des expéditeurs autorisés de notre entreprise. (N’activez pas **Autoriser les ajouter l’expéditeur 'AllowedtoSpoof' à la liste** jusqu'à ce que vous êtes sûr de que vouloir faire. [En savoir plus sur l’aide à la décision usurpation d’identité](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-p108">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list. (Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this. [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span>
    
    ![Vous pouvez autoriser un expéditeur](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)
  
<span data-ttu-id="dd9a9-129">De cette façon, nous pouvez passer d’un tableau de bord à insights et actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="dd9a9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd9a9-130">Related topics</span></span>

[<span data-ttu-id="dd9a9-131">Procédure pas à pas : à partir d’un aperçu à un rapport détaillé</span><span class="sxs-lookup"><span data-stu-id="dd9a9-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="dd9a9-132">Procédure pas à pas : à partir d’un rapport détaillé d’une analyse</span><span class="sxs-lookup"><span data-stu-id="dd9a9-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

