---
title: Intelligence des menaces d’Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection: M365-security-compliance
description: Découvrez comment les fonctionnalités d'aide à la décision dans la protection avancée contre les menaces peuvent vous aider à rechercher des menaces contre votre organisation, à répondre aux programmes malveillants, au hameçonnage et à d'autres attaques détectées par Office 365 pour votre part, et à rechercher des indicateurs de menace.
ms.openlocfilehash: a55a17bae141c394ba01e1526615c5c1687340a2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216554"
---
# <a name="office-365-threat-intelligence"></a><span data-ttu-id="0f176-103">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="0f176-103">Office 365 Threat Intelligence</span></span>

<span data-ttu-id="0f176-104">Les fonctionnalités d'aide à la décision dans Office 365 protection avancée contre les menaces aident les analystes et administrateurs de la sécurité à protéger les utilisateurs d'Office 365 de leur organisation:</span><span class="sxs-lookup"><span data-stu-id="0f176-104">Threat intelligence capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="0f176-105">Faciliter l'identification, la surveillance et la compréhension des attaques</span><span class="sxs-lookup"><span data-stu-id="0f176-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="0f176-106">Aider à résoudre rapidement les menaces dans Exchange Online et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0f176-106">Helping to quickly address threats in Exchange Online and SharePoint Online</span></span>
    
3. <span data-ttu-id="0f176-107">Fourniture d'informations et de connaissances pour vous aider à empêcher les attaques contre leur organisation</span><span class="sxs-lookup"><span data-stu-id="0f176-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="0f176-p101">**Threat Intelligence fait désormais partie d'Office 365 Advanced Threat Protection Plan 2**, inclus dans certains abonnements, tels que [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 entreprise E5, Office 365 Éducation a5, etc. Si votre organisation dispose d'un abonnement qui n'inclut pas la protection avancée contre les menaces pour Office 365, vous pouvez acheter l'ATP en tant que module complémentaire. Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="0f176-p101">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="0f176-110">Qu'est-ce qui change?</span><span class="sxs-lookup"><span data-stu-id="0f176-110">What's changing?</span></span>

<span data-ttu-id="0f176-p102">Auparavant, Office 365 Threat Intelligence était inclus dans les abonnements, comme Office 365 entreprise E5. C'est toujours le cas, bien que les fonctionnalités d'aide à la décision fassent désormais partie du plan 2 de protection avancée contre les menaces Office 365 (ce qui est inclus dans Office 365 entreprise E5).</span><span class="sxs-lookup"><span data-stu-id="0f176-p102">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5. This is still the case, although Threat Intelligence features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="0f176-p103">En outre, Office 365 Threat Intelligence était auparavant disponible à l'achat en tant que module complémentaire pour Office 365 pour les clients professionnels. Désormais, l'intelligence des menaces est incluse dans Office 365 Advanced Threat Protection Plan 2. Pour en savoir plus, consultez la rubrique [offres et tarifs pour la protection avancée contre les menaces d'Office 365](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="0f176-p103">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers. Now, Threat Intelligence is included in Office 365 Advanced Threat Protection Plan 2. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="0f176-116">Voici ce que cela signifie:</span><span class="sxs-lookup"><span data-stu-id="0f176-116">Here's what all this means:</span></span>

- <span data-ttu-id="0f176-117">**Si votre organisation dispose déjà d'Office 365 entreprise E5**, vous disposez déjà d'un plan 2 de protection avancée contre les menaces et cela inclut des fonctionnalités d'aide à la décision.</span><span class="sxs-lookup"><span data-stu-id="0f176-117">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat Intelligence capabilities.</span></span>

- <span data-ttu-id="0f176-p104">**Si votre organisation disposait auparavant d'office 365 Threat Intelligence (mais pas office 365 Advanced Threat Protection) en tant que module complémentaire** d'un autre abonnement Office 365, vous bénéficierEz d'Office 365 Advanced Threat Protection Plan 2. Cela inclut les fonctionnalités avancées de protection contre les menaces et d'aide à la décision.</span><span class="sxs-lookup"><span data-stu-id="0f176-p104">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2. This includes Advanced Threat Protection and Threat Intelligence capabilities.</span></span> 

- <span data-ttu-id="0f176-p105">**Si votre organisation disposait auparavant d'office 365 protection avancée contre les menaces (mais pas office 365 Threat Intelligence) en tant que module complémentaire** d'un autre abonnement Office 365, vous disposeRez d'Office 365 Advanced Threat Protection Plan 1. Cela inclut la protection avancée contre les menaces (mais pas les fonctionnalités d'aide à la décision).</span><span class="sxs-lookup"><span data-stu-id="0f176-p105">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1. This includes Advanced Threat Protection (but not Threat Intelligence capabilities).</span></span>

<span data-ttu-id="0f176-122">Pour plus d'informations, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) .</span><span class="sxs-lookup"><span data-stu-id="0f176-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-intelligence-capabilities"></a><span data-ttu-id="0f176-123">Prise en main des fonctionnalités d'aide à la décision</span><span class="sxs-lookup"><span data-stu-id="0f176-123">Get started with threat intelligence capabilities</span></span>

<span data-ttu-id="0f176-124">Utilisez les ressources suivantes pour en savoir plus sur l'intelligence des menaces et sur la façon dont vous pouvez l'utiliser pour maintenir les personnes de votre organisation plus sûres.</span><span class="sxs-lookup"><span data-stu-id="0f176-124">Use the following resources to learn more about threat intelligence, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="0f176-125">[Prise en main de l'intelligence des menaces](get-started-with-ti.md) (cela inclut des informations sur les rôles requis)</span><span class="sxs-lookup"><span data-stu-id="0f176-125">[Get started with Threat Intelligence](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="0f176-126">En savoir plus sur les suivis de menace-nouveau et notable</span><span class="sxs-lookup"><span data-stu-id="0f176-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="0f176-127">Rechercher et identifier les messages électroniques malveillants qui ont été remis</span><span class="sxs-lookup"><span data-stu-id="0f176-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="0f176-128">Utiliser un simulateur d'attaque</span><span class="sxs-lookup"><span data-stu-id="0f176-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="0f176-129">Intégrer Threat Intelligence à Windows Defender : Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0f176-129">Integrate Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="0f176-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f176-130">Related topics</span></span>

[<span data-ttu-id="0f176-131">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0f176-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="0f176-132">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0f176-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="0f176-133">Autorisations dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="0f176-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

