---
title: Fonctionne de DLP entre la sécurité &amp; centre de conformité et le centre d’administration Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans la sécurité &amp; centre de conformité fonctionne avec des règles DLP et de transport dans le centre d’administration Exchange.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528379"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="96b5c-103">Fonctionne de DLP entre la sécurité &amp; centre de conformité et le centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96b5c-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="96b5c-104">Dans Office 365, vous pouvez créer une stratégie de protection contre la perte données dans deux centres d’administration différentes :</span><span class="sxs-lookup"><span data-stu-id="96b5c-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="96b5c-p101">Dans la **sécurité &amp; centre de conformité**, vous pouvez créer une seule stratégie DLP pour vous aider à protéger le contenu dans SharePoint, OneDrive et Exchange. Lorsque cela est possible, nous vous conseillons de créer une stratégie DLP ici. Pour plus d’informations, voir [DLP dans la sécurité &amp; centre de conformité](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="96b5c-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="96b5c-p102">Dans le **Centre d’administration Exchange**, vous pouvez créer une stratégie DLP pour vous aider à protéger le contenu uniquement dans Exchange. Cette stratégie permet de règles de transport Exchange, il n’a plus d’options spécifiques à la gestion du courrier électronique. Pour plus d’informations, voir [DLP dans le centre d’administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="96b5c-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="96b5c-111">Les stratégies DLP créé dans l’administration ces centres de fonctionnent côte à côte - cette rubrique explique comment.</span><span class="sxs-lookup"><span data-stu-id="96b5c-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP de sécurité et de centre de conformité et de centre d’administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="96b5c-113">Comment DLP dans la sécurité &amp; centre de conformité fonctionne avec des règles DLP et de transport dans le centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96b5c-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="96b5c-p103">Après avoir créé une stratégie DLP dans la sécurité &amp; centre de conformité, la stratégie est déployée sur tous les sites inclus dans la stratégie. Si la stratégie inclut Exchange Online, de la stratégie synchronisé il et appliqués dans exactement comme une stratégie DLP créée dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="96b5c-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="96b5c-p104">Si vous avez créé des stratégies DLP dans le centre d’administration Exchange, les stratégies continueront de fonctionner côte à côte avec toutes les stratégies pour le courrier électronique que vous créez dans la sécurité &amp; centre de conformité. Mais, notez que les règles créées dans le centre d’administration Exchange sont prioritaires. Toutes les règles de transport Exchange sont traités en premier, puis le DLP à partir de la sécurité des règles &amp; centre de conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="96b5c-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="96b5c-119">Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="96b5c-119">This means that:</span></span>
  
- <span data-ttu-id="96b5c-120">Messages bloqués par les règles de transport Exchange ne sont analysés par les règles DLP créées dans la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="96b5c-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="96b5c-121">Si une règle de transport Exchange modifie un message d’une manière qui entraîne sa correspondent à une stratégie DLP dans la sécurité &amp; centre de conformité - tels que l’ajout d’utilisateurs externes - puis les règles DLP détecte cela et appliquer la stratégie selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="96b5c-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="96b5c-122">Également note que le traitement de DLP n’affectent pas les règles de transport Exchange qui utilisent l’action « arrêter le traitement » règles de la sécurité &amp; centre de conformité - allez encore être traitées.</span><span class="sxs-lookup"><span data-stu-id="96b5c-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="96b5c-123">Conseils de stratégie de sécurité &amp; centre de conformité et le centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96b5c-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="96b5c-p105">Conseils de stratégie peuvent travailler avec les stratégies DLP et créés dans le centre d’administration Exchange, ou avec des stratégies DLP créées dans la sécurité des règles de flux de messagerie &amp; centre de conformité, mais pas les deux. Il s’agit, car ces stratégies sont stockées dans des emplacements différents, mais les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="96b5c-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="96b5c-p106">Si vous avez configuré les conseils de stratégie dans le centre d’administration Exchange, les conseils de stratégie que vous configurez dans la sécurité &amp; centre de conformité n’apparaîtra pas aux utilisateurs dans Outlook sur le web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils fournis dans le centre d’administration Exchange. Cela garantit que vos règles de transport Exchange en cours continue à fonctionner jusqu'à ce que vous choisissez de basculer vers la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="96b5c-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="96b5c-128">Notez que les notifications de messagerie pendant que les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement, sont toujours envoyés, même si vous utilisez des stratégies DLP dans la sécurité &amp; centre de conformité et le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="96b5c-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

