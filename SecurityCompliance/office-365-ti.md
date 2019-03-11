---
title: Enquête et réponse aux menaces Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/09/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Découvrez comment les fonctionnalités d'aide à la décision dans la protection avancée contre les menaces peuvent vous aider à rechercher des menaces contre votre organisation, à répondre aux programmes malveillants, au hameçonnage et à d'autres attaques détectées par Office 365 pour votre part, et à rechercher des indicateurs de menace.
ms.openlocfilehash: 1d076ed6ca48b8423ad92d5ea71bd87167b8519a
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30523998"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="e7a24-103">Enquête et réponse aux menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="e7a24-103">Office 365 Threat Investigation and Response</span></span>

<span data-ttu-id="e7a24-104">Les fonctionnalités d'enquête et de réponse aux menaces dans Office 365 Advanced Threat Protection aident les analystes et administrateurs de la sécurité à protéger les utilisateurs d'Office 365 de leur organisation:</span><span class="sxs-lookup"><span data-stu-id="e7a24-104">Threat investigation and response capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="e7a24-105">Faciliter l'identification, la surveillance et la compréhension des attaques</span><span class="sxs-lookup"><span data-stu-id="e7a24-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="e7a24-106">Aider à résoudre rapidement les menaces dans Exchange Online, SharePoint Online, un lecteur pour les entreprises et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="e7a24-106">Helping to quickly address threats in Exchange Online, SharePoint Online, One Drive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="e7a24-107">Fourniture d'informations et de connaissances pour vous aider à empêcher les attaques contre leur organisation</span><span class="sxs-lookup"><span data-stu-id="e7a24-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="e7a24-108">Une enquête et une réponse automatisées pour les menaces critiques basées sur la messagerie</span><span class="sxs-lookup"><span data-stu-id="e7a24-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="e7a24-109">**Office 365 Threat Investigation and Responses (précédemment appelé office 365 Threat Intelligence) fait désormais partie de la section office 365 Advanced THreat protection plan 2**, qui est incluse dans certains abonnements, tels que [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d'un abonnement qui n'inclut pas la protection avancée contre les menaces pour Office 365, vous pouvez acheter l'ATP en tant que module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="e7a24-109">**Office 365 THreat Investigation and Responses (previously known as Office 365 Threat Intelligence) is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="e7a24-110">Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="e7a24-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="e7a24-111">Qu'est-ce qui change?</span><span class="sxs-lookup"><span data-stu-id="e7a24-111">What's changing?</span></span>

<span data-ttu-id="e7a24-112">Auparavant, les fonctionnalités d'enquête et de réponses aux menaces Office 365 étaient incluses dans les abonnements, comme Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="e7a24-112">Formerly, Office 365 Threat investigation and responses capabilities were included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="e7a24-113">Ce n'est pas toujours le cas et ces fonctionnalités font désormais partie du plan 2 Office 365 Advanced Threat Protection Plan 2 (inclus dans Office 365 entreprise E5).</span><span class="sxs-lookup"><span data-stu-id="e7a24-113">This is still the case, and now these features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="e7a24-114">En outre, Office 365 Threat enquête and Response capbailities était auparavant disponible à l'achat en tant que module complémentaire pour Office 365 pour les clients professionnels.</span><span class="sxs-lookup"><span data-stu-id="e7a24-114">In addition, Office 365 Threat investigation and response capbailities were formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="e7a24-115">À présent, ces fonctionnalités sont incluses dans Office 365 Advanced Threat Protection Plan 2 (qui inclut également Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="e7a24-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (which also includes Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="e7a24-116">Pour en savoir plus, consultez la rubrique [offres et tarifs pour la protection avancée contre les menaces d'Office 365](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="e7a24-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="e7a24-117">Voici ce que cela signifie:</span><span class="sxs-lookup"><span data-stu-id="e7a24-117">Here's what all this means:</span></span>

- <span data-ttu-id="e7a24-118">**Si votre organisation dispose déjà d'Office 365 entreprise E5**, vous disposez déjà d'un plan 2 de protection avancée contre les menaces, ainsi que des fonctionnalités d'enquête et de réponse aux menaces.</span><span class="sxs-lookup"><span data-stu-id="e7a24-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat investigation and response capabilities.</span></span>

- <span data-ttu-id="e7a24-119">**Si votre organisation disposait auparavant d'office 365 Threat Intelligence (mais pas office 365 Advanced Threat Protection) en tant que module complémentaire** d'un autre abonnement Office 365, vous bénéficierEz d'Office 365 Advanced Threat Protection Plan 2.</span><span class="sxs-lookup"><span data-stu-id="e7a24-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2.</span></span> <span data-ttu-id="e7a24-120">Cela inclut la protection avancée contre les menaces plan 1, ainsi que les fonctionnalités d'enquête et de réponse aux menaces.</span><span class="sxs-lookup"><span data-stu-id="e7a24-120">This includes Advanced Threat Protection Plan 1 and Threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="e7a24-121">**Si votre organisation disposait auparavant d'office 365 protection avancée contre les menaces (mais pas office 365 Threat Intelligence) en tant que module complémentaire** d'un autre abonnement Office 365, vous disposeRez d'Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="e7a24-121">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="e7a24-122">Cela inclut la protection avancée contre les menaces (mais pas les fonctionnalités de investigaiton et de réponse).</span><span class="sxs-lookup"><span data-stu-id="e7a24-122">This includes Advanced Threat Protection (but not Threat investigaiton and response capabilities).</span></span>

<span data-ttu-id="e7a24-123">Pour plus d'informations, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) .</span><span class="sxs-lookup"><span data-stu-id="e7a24-123">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigaiton-and-response-capabilities"></a><span data-ttu-id="e7a24-124">Prise en main des fonctionnalités de investigaiton et de réponse aux menaces</span><span class="sxs-lookup"><span data-stu-id="e7a24-124">Get started with threat investigaiton and response capabilities</span></span>

<span data-ttu-id="e7a24-125">Utilisez les ressources suivantes pour en savoir plus sur les fonctionnalités d'enquête et de réponse aux menaces dans Office 365, ainsi que sur la façon dont vous pouvez les utiliser pour sécuriser davantage les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e7a24-125">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="e7a24-126">[Prise en main de l'enquête et de la réponse aux menaces](get-started-with-ti.md) (cela inclut des informations sur les rôles requis)</span><span class="sxs-lookup"><span data-stu-id="e7a24-126">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="e7a24-127">En savoir plus sur les suivis de menace-nouveau et notable</span><span class="sxs-lookup"><span data-stu-id="e7a24-127">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="e7a24-128">Rechercher et identifier les messages électroniques malveillants qui ont été remis</span><span class="sxs-lookup"><span data-stu-id="e7a24-128">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="e7a24-129">Utiliser un simulateur d'attaque</span><span class="sxs-lookup"><span data-stu-id="e7a24-129">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="e7a24-130">Intégration de l'enquête de menace et de la réponse avec Windows Defender-protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e7a24-130">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="e7a24-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a24-131">Related topics</span></span>

[<span data-ttu-id="e7a24-132">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="e7a24-132">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="e7a24-133">Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e7a24-133">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="e7a24-134">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="e7a24-134">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 