---
title: Examen et réponse contre les menaces Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Découvrez comment les fonctionnalités d’aide à la décision dans Office 365 protection avancée contre les menaces peuvent vous aider à rechercher des menaces contre votre organisation, à répondre aux programmes malveillants, au hameçonnage et à d’autres attaques détectées par Office 365 pour votre part, et à rechercher des menaces. confirme.
ms.openlocfilehash: c8b0815368e80151f8ee55161b9bcbaa98065228
ms.sourcegitcommit: b9d8a43cb3afcdc8820bc9470c5707eff8fc6616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34852808"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="0aeca-103">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="0aeca-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="0aeca-104">Les fonctionnalités d’enquête et de réponse aux menaces dans [Office 365 Advanced Threat Protection](office-365-atp.md) aident les analystes et administrateurs de la sécurité à protéger les utilisateurs d’Office 365 de leur organisation:</span><span class="sxs-lookup"><span data-stu-id="0aeca-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="0aeca-105">Faciliter l’identification, la surveillance et la compréhension des attaques</span><span class="sxs-lookup"><span data-stu-id="0aeca-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="0aeca-106">Aider à résoudre rapidement les menaces dans Exchange Online, SharePoint Online, OneDrive entreprise et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="0aeca-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="0aeca-107">Fourniture d’informations et de connaissances pour vous aider à empêcher les attaques contre leur organisation</span><span class="sxs-lookup"><span data-stu-id="0aeca-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="0aeca-108">Une enquête et une réponse automatisées pour les menaces critiques basées sur la messagerie</span><span class="sxs-lookup"><span data-stu-id="0aeca-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="0aeca-109">Office **365 Advanced Threat Protection and Threat Response and Response (anciennement appelé office 365 Threat Intelligence) est désormais office 365 Advanced Threat Protection Plan 2**, ainsi que des fonctionnalités de protection contre les menaces supplémentaires incluses dans le certains abonnements, tels que [microsoft 365 E5](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/business), Office 365 E5, Office 365 a5, etc. Si votre organisation dispose d’un abonnement qui n’inclut pas la protection avancée contre les menaces pour Office 365, vous pouvez acheter l’ATP en tant que module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="0aeca-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 E5](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 E5, Office 365 A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="0aeca-110">Pour plus d’informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="0aeca-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="0aeca-111">Qu’est-ce qui change?</span><span class="sxs-lookup"><span data-stu-id="0aeca-111">What's changing?</span></span>

<span data-ttu-id="0aeca-112">Auparavant, Office 365 Threat Intelligence était inclus dans les abonnements, comme Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="0aeca-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 E5.</span></span> <span data-ttu-id="0aeca-113">C’est toujours le cas, car les fonctionnalités d’enquête et de réponse aux menaces font désormais partie du plan 2 de protection avancée contre les menaces Office 365 (inclus dans Office 365 E5).</span><span class="sxs-lookup"><span data-stu-id="0aeca-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 E5).</span></span> 

<span data-ttu-id="0aeca-114">En outre, Office 365 Threat Intelligence était auparavant disponible à l’achat en tant que module complémentaire pour Office 365 pour les clients professionnels.</span><span class="sxs-lookup"><span data-stu-id="0aeca-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="0aeca-115">À présent, ces fonctionnalités sont incluses dans Office 365 Advanced Threat Protection Plan 2 (ainsi que toutes les fonctionnalités d’Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="0aeca-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="0aeca-116">Pour en savoir plus, consultez la rubrique [offres et tarifs pour la protection avancée contre les menaces d’Office 365](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="0aeca-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="0aeca-117">Voici ce que cela signifie:</span><span class="sxs-lookup"><span data-stu-id="0aeca-117">Here's what all this means:</span></span>

- <span data-ttu-id="0aeca-118">**Si votre organisation dispose déjà d’Office 365 E5**, vous disposez déjà d’un plan 2 de protection avancée contre les menaces, ainsi que des fonctionnalités d’enquête et de réponse aux menaces.</span><span class="sxs-lookup"><span data-stu-id="0aeca-118">**If your organization already has Office 365 E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="0aeca-119">**Si votre organisation disposait auparavant d’office 365 Threat Intelligence (mais pas office 365 Advanced Threat Protection) en tant que module complémentaire** d’un autre abonnement Office 365, vous aurez maintenant Office 365 Advanced Threat Protection Plan 2, et cela inclut fonctionnalités d’enquête et de réponse aux menaces.</span><span class="sxs-lookup"><span data-stu-id="0aeca-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="0aeca-120">**Si votre organisation disposait auparavant d’office 365 protection avancée contre les menaces (mais pas office 365 Threat Intelligence) en tant que module complémentaire** d’un autre abonnement Office 365, vous bénéficierez désormais d’Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="0aeca-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="0aeca-121">Cela inclut le plan 1 de protection avancée contre les menaces Office 365 (mais pas les fonctionnalités d’enquête et de réponse aux menaces).</span><span class="sxs-lookup"><span data-stu-id="0aeca-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="0aeca-122">Pour plus d’informations, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) .</span><span class="sxs-lookup"><span data-stu-id="0aeca-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="0aeca-123">Prise en main des fonctionnalités d’enquête et de réponse aux menaces</span><span class="sxs-lookup"><span data-stu-id="0aeca-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="0aeca-124">Utilisez les ressources suivantes pour en savoir plus sur les fonctionnalités d’enquête et de réponse aux menaces dans Office 365, ainsi que sur la façon dont vous pouvez les utiliser pour sécuriser davantage les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0aeca-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="0aeca-125">[Prise en main de l’enquête et de la réponse aux menaces](get-started-with-ti.md) (cela inclut des informations sur les rôles requis)</span><span class="sxs-lookup"><span data-stu-id="0aeca-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="0aeca-126">En savoir plus sur les suivis de menace-nouveau et notable</span><span class="sxs-lookup"><span data-stu-id="0aeca-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="0aeca-127">Gagnez du temps et des efforts avec les fonctionnalités d’analyse et de réponse automatisées (AIR)</span><span class="sxs-lookup"><span data-stu-id="0aeca-127">Save time and effort with Automated Investigation and Response (AIR) capabilities</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="0aeca-128">Utiliser l’Explorateur de menaces (ou les détections en temps réel) pour identifier et étudier le contenu malveillant dans les messages électroniques et les fichiers</span><span class="sxs-lookup"><span data-stu-id="0aeca-128">Use Threat Explorer (or real-time detections) to identify and investigate malicious content in email and files</span></span>](threat-explorer.md)
    
- [<span data-ttu-id="0aeca-129">Rechercher et d’examiner le courrier électronique malveillant qui a été distribué</span><span class="sxs-lookup"><span data-stu-id="0aeca-129">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="0aeca-130">Utiliser un simulateur d’attaque pour simuler des attaques et augmenter la sensibilisation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0aeca-130">Use Attack Simulator to simulate attacks and increase user awareness</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="0aeca-131">Intégration des fonctionnalités d’enquête et de réponse aux menaces avec la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="0aeca-131">Integrate Threat Investigation and Response capabilities with Microsoft Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="0aeca-132">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="0aeca-132">Related topics</span></span>

[<span data-ttu-id="0aeca-133">Affichages Threat Explorer</span><span class="sxs-lookup"><span data-stu-id="0aeca-133">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="0aeca-134">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0aeca-134">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="0aeca-135">Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0aeca-135">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="0aeca-136">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="0aeca-136">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
