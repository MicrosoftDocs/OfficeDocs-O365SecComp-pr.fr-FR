---
title: Fonctionnement de DLP entre le centre &amp; de sécurité et le centre d'administration Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans le centre &amp; de sécurité conformité fonctionne avec DLP et les règles de transport dans le centre d'administration Exchange.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215644"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="96925-103">Fonctionnement de DLP entre le centre &amp; de sécurité et le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96925-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="96925-104">Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d'administration différents:</span><span class="sxs-lookup"><span data-stu-id="96925-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="96925-p101">Dans le **Centre &amp; de sécurité conformité**, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive et Exchange. Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici. Pour plus d'informations, reportez-vous [à la rubrique DLP dans le centre de sécurité &amp; conformité](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="96925-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="96925-p102">Dans le **Centre d'administration Exchange**, vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange. Cette stratégie peut utiliser des règles de transport Exchange, de sorte qu'elle dispose de plus d'options spécifiques pour gérer le courrier électronique. Pour plus d'informations, consultez [la rubrique DLP dans le centre d'administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="96925-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="96925-111">Les stratégies DLP créées dans ces centres d'administration fonctionnent côte à côte-cette rubrique explique comment procéder.</span><span class="sxs-lookup"><span data-stu-id="96925-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP dans le centre de sécurité et de conformité et centre d'administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="96925-113">Fonctionnement de DLP dans le &amp; Centre de sécurité conformité avec DLP et les règles de transport dans le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96925-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="96925-p103">Une fois que vous avez créé une stratégie DLP &amp; dans le centre de sécurité conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie. Si la stratégie inclut Exchange Online, la stratégie est synchronisée et appliquée exactement de la même manière qu'une stratégie DLP créée dans le centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="96925-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="96925-p104">Si vous avez créé des stratégies DLP dans le centre d'administration Exchange, ces stratégies continueront à fonctionner côte à côte avec n'importe quelle stratégie pour le courrier électronique &amp; que vous créez dans le centre de sécurité et de conformité. Toutefois, Notez que les règles créées dans le centre d'administration Exchange ont priorité. Toutes les règles de transport Exchange sont traitées en premier, puis les règles DLP du &amp; Centre de sécurité conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="96925-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="96925-119">Cela signifie que:</span><span class="sxs-lookup"><span data-stu-id="96925-119">This means that:</span></span>
  
- <span data-ttu-id="96925-120">Les messages bloqués par les règles de transport Exchange ne sont pas analysés par les règles DLP &amp; créées dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="96925-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="96925-121">Si une règle de transport Exchange modifie un message de manière à ce qu'elle corresponde à une stratégie DLP dans le &amp; Centre de sécurité conformité, comme l'ajout d'utilisateurs externes, les règles DLP le détectera et appliqueront la stratégie si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="96925-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="96925-122">Notez également que les règles de transport Exchange qui utilisent l'action «arrêter le traitement» n'affectent pas le traitement des règles &amp; DLP dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="96925-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="96925-123">Conseils de stratégie dans le &amp; Centre de sécurité conformité et dans le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="96925-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="96925-p105">Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d'administration Exchange, soit &amp; avec les stratégies DLP créées dans le centre de sécurité conformité, mais pas dans les deux. Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu'à partir d'un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="96925-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="96925-p106">Si vous avez configuré des conseils de stratégie dans le centre d'administration Exchange, tous les conseils de stratégie que &amp; vous configurez dans le centre de sécurité conformité ne s'afficheront pas aux utilisateurs dans Outlook sur le Web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils dans le centre d'administration Exchange. Cela garantit que vos règles de transport Exchange actuelles continueront de fonctionner jusqu'à ce que vous choisissiez de &amp; basculer vers le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="96925-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="96925-128">Notez que si les conseils de stratégie ne peuvent être tracés qu'à partir d'un seul emplacement, les notifications par courrier électronique sont toujours envoyées, &amp; même si vous utilisez des stratégies DLP dans le centre d'administration et Exchange.</span><span class="sxs-lookup"><span data-stu-id="96925-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

