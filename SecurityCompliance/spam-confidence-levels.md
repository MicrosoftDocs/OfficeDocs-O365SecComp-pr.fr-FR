---
title: Seuils de probabilité de courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275644"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="c9797-106">Seuils de probabilité de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c9797-106">Spam confidence levels</span></span>

<span data-ttu-id="c9797-p102">Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="c9797-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="c9797-111">**Valeur SCL**</span><span class="sxs-lookup"><span data-stu-id="c9797-111">**SCL Rating**</span></span>|<span data-ttu-id="c9797-112">**Interprétation de la probabilité de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="c9797-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="c9797-113">**Action par défaut**</span><span class="sxs-lookup"><span data-stu-id="c9797-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9797-114">-1</span><span class="sxs-lookup"><span data-stu-id="c9797-114">-1</span></span>  <br/> |<span data-ttu-id="c9797-115">Courrier non indésirable provenant d'un expéditeur sûr, un destinataire sûr ou une adresse IP inscrite sur une liste sûre (partenaire approuvé)</span><span class="sxs-lookup"><span data-stu-id="c9797-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner)</span></span>  <br/> |<span data-ttu-id="c9797-116">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c9797-116">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="c9797-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="c9797-117">0, 1</span></span>  <br/> |<span data-ttu-id="c9797-118">Courrier non indésirable car le message a été analysé et identifié comme sûr</span><span class="sxs-lookup"><span data-stu-id="c9797-118">Non-spam because the message was scanned and determined to be clean</span></span>  <br/> |<span data-ttu-id="c9797-119">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c9797-119">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="c9797-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="c9797-120">5, 6</span></span>  <br/> | <span data-ttu-id="c9797-121">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c9797-121">Spam</span></span>  <br/> |<span data-ttu-id="c9797-122">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c9797-122">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="c9797-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="c9797-123">7, 8, 9</span></span>  <br/> |<span data-ttu-id="c9797-124">Courrier indésirable à probabilité élevée</span><span class="sxs-lookup"><span data-stu-id="c9797-124">High confidence spam</span></span>  <br/> |<span data-ttu-id="c9797-125">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c9797-125">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
   
> [!TIP]
> <span data-ttu-id="c9797-p103">Les évaluations SCL de 2, 3, 4, 7 et 8 ne sont pas définies par le service. Une valeur SCL de 5 ou 6 est considérée comme suspecte de courrier indésirable, ce qui est moins sûr qu'une valeur SCL de 9, ce qui est considéré comme un courrier indésirable. Des actions différentes pour le courrier indésirable et le courrier indésirable à niveau de confiance peuvent être configurées via vos stratégies de filtrage de contenu dans le centre d'administration Exchange. Pour plus d'informations, consultez [la rubrique Configuration de vos stratégies de filtrage du courrier](configure-your-spam-filter-policies.md)indésirable. Vous pouvez également définir la valeur de contrôle d'accès SCL pour les messages qui correspondent à des conditions spécifiques à l'aide de règles de transport, comme décrit dans [la rubrique use mail Flow Rules to Set the Spam Confidence Level (SCL) dans les messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Si vous utilisez une règle de transport pour définir une valeur SCL de 7, 8 ou 9, le message sera traité comme du courrier indésirable à niveau de confiance élevé.</span><span class="sxs-lookup"><span data-stu-id="c9797-p103">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service. An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam. Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). You can also set the SCL rating for messages that match specific conditions by using Transport rules, as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). If you use a transport rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="c9797-p104">![Icône rapide pour LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Vous débutez avec Office 365 ?**         Découvrez les cours vidéo gratuits pour **Office 365 admins and IT pros** proposés par LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="c9797-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   

