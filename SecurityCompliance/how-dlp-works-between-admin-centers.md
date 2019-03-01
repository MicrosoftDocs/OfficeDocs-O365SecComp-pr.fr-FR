---
title: Fonctionnement de DLP entre le centre de sécurité & conformité et le centre d'administration Exchange
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
description: Découvrez comment DLP dans le centre de sécurité & Compliance Center fonctionne avec DLP et les règles de flux de messagerie (règles de transport) dans le centre d'administration Exchange.
ms.openlocfilehash: c20cf5d4e7b83a726b104a57b89f2d8f765d7f16
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341485"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a><span data-ttu-id="66c64-103">Fonctionnement de DLP entre le centre de sécurité & conformité et le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="66c64-103">How DLP works between the Security & Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="66c64-104">Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d'administration différents:</span><span class="sxs-lookup"><span data-stu-id="66c64-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="66c64-p101">Dans le **Centre de sécurité _AMP_ Compliance Center**, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive et Exchange. Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici. Pour plus d'informations, reportez-vous [à la rubrique DLP dans le centre de sécurité _AMP_ conformité](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="66c64-p101">In the **Security & Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security & Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="66c64-p102">Dans le **Centre d'administration Exchange**, vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange. Cette stratégie peut utiliser des règles de flux de messagerie Exchange (également appelées règles de transport), de sorte qu'elle dispose de plus d'options spécifiques pour gérer le courrier électronique. Pour plus d'informations, consultez [la rubrique DLP dans le centre d'administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="66c64-p102">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email. For more information, see [DLP in the Exchange admin center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="66c64-111">Les stratégies DLP créées dans ces centres d'administration fonctionnent côte à côte-cette rubrique explique comment procéder.</span><span class="sxs-lookup"><span data-stu-id="66c64-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Pages DLP dans le centre de sécurité et de conformité et centre d'administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="66c64-113">Fonctionnement de DLP dans le centre de sécurité & Compliance Center avec DLP et les règles de flux de messagerie dans le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="66c64-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="66c64-p103">Une fois que vous avez créé une stratégie DLP dans le centre de sécurité & conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie. Si la stratégie inclut Exchange Online, la stratégie est synchronisée et appliquée exactement de la même manière qu'une stratégie DLP créée dans le centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="66c64-p103">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="66c64-p104">Si vous avez créé des stratégies DLP dans le centre d'administration Exchange, ces stratégies continueront à fonctionner côte à côte avec des stratégies pour les messages électroniques que vous créez dans le centre de sécurité & Compliance Center. Toutefois, Notez que les règles créées dans le centre d'administration Exchange ont priorité. Toutes les règles de flux de messagerie Exchange sont traitées en premier, puis les règles DLP du centre de sécurité & conformité sont traitées.</span><span class="sxs-lookup"><span data-stu-id="66c64-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="66c64-119">Cela signifie que:</span><span class="sxs-lookup"><span data-stu-id="66c64-119">This means that:</span></span>
  
- <span data-ttu-id="66c64-120">Les messages bloqués par les règles de flux de messagerie Exchange ne sont pas analysés par les règles DLP créées dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="66c64-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>
    
- <span data-ttu-id="66c64-121">Si une règle de flux de messagerie Exchange modifie un message de manière à ce qu'il corresponde à une stratégie DLP dans le centre de sécurité & Compliance Center (par exemple, ajout d'utilisateurs externes), les règles DLP détecteront ceci et appliqueront la stratégie si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="66c64-121">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="66c64-122">Notez également que les règles de flux de messagerie Exchange qui utilisent l'action «arrêter le traitement» n'affectent pas le traitement des règles DLP dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="66c64-122">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="66c64-123">Conseils de stratégie dans le centre de sécurité & Compliance Center vs du centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="66c64-123">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="66c64-p105">Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d'administration Exchange, soit avec les stratégies DLP créées dans le centre de sécurité & Compliance Center, mais pas dans les deux. Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu'à partir d'un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="66c64-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="66c64-p106">Si vous avez configuré des conseils de stratégie dans le centre d'administration Exchange, tous les conseils de stratégie que vous configurez dans le centre de sécurité & conformité n'apparaissent pas aux utilisateurs dans Outlook sur le Web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils dans le centre d'administration Exchange. Cela permet de s'assurer que vos règles de flux de messagerie Exchange actuelles continueront de fonctionner jusqu'à ce que vous choisissiez de basculer vers le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="66c64-p106">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center. This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="66c64-128">Notez que si les conseils de stratégie ne peuvent être tracés qu'à partir d'un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous utilisez des stratégies DLP dans le centre de sécurité et le centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="66c64-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
  

