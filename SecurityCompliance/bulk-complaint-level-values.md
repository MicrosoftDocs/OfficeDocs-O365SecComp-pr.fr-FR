---
title: Valeurs BCL
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: Les vers de publipostage en bloc ont des modèles d'envoi différents, ainsi que des pratiques de création de contenu et d'acquisition de liste variées. Certains sont de bons vers de publipostage en bloc et envoient des messages désirés comportant un contenu pertinent à leurs abonnés. Ces messages entraînent peu de réclamations de la part des destinataires. D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires. Pour distinguer ces types de vers de publipostage en bloc, une évaluation BCL (Bulk Complaint Level) est réalisée sur les messages qui en proviennent. Les évaluations BCL vont de 1 à 9 selon la probabilité de réclamations dues au ver de publipostage en bloc. Un expéditeur disposant d'une évaluation BCL de 9 peut entraîner un grand nombre de réclamations de la part des destinataires, tandis qu'un autre expéditeur ayant une évaluation BCL de 3 n'en générera probablement pas beaucoup. Microsoft utilise des sources internes et tierces pour identifier le courrier en masse et déterminer l'évaluation BCL appropriée. Cette évaluation est présentée dans l'en-tête X-Microsoft-Antispam de chaque message. Pour plus d'informations sur cet en-tête de message, voir En-têtes de messages anti-courrier indésirable.
ms.openlocfilehash: 490823f045e2e3fcf6b537d9717ab12abc323da6
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152126"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="7e8ce-112">Valeurs BCL</span><span class="sxs-lookup"><span data-stu-id="7e8ce-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="7e8ce-p102">Les vers de publipostage en bloc ont des modèles d'envoi différents, ainsi que des pratiques de création de contenu et d'acquisition de liste variées. Certains sont de bons vers de publipostage en bloc et envoient des messages désirés comportant un contenu pertinent à leurs abonnés. Ces messages entraînent peu de réclamations de la part des destinataires. D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires. Pour distinguer ces types de vers de publipostage en bloc, une évaluation BCL (Bulk Complaint Level) est réalisée sur les messages qui en proviennent. Les évaluations BCL vont de 1 à 9 selon la probabilité de réclamations dues au ver de publipostage en bloc. Un expéditeur disposant d'une évaluation BCL de 9 peut entraîner un grand nombre de réclamations de la part des destinataires, tandis qu'un autre expéditeur ayant une évaluation BCL de 3 n'en générera probablement pas beaucoup. Microsoft utilise des sources internes et tierces pour identifier le courrier en masse et déterminer l'évaluation BCL appropriée. Cette évaluation est présentée dans l'en-tête **X-Microsoft-Antispam** de chaque message. Pour plus d'informations sur cet en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="7e8ce-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="7e8ce-123">Vous pouvez vous servir des valeurs BCL pour définir le niveau de filtrage en bloc souhaité pour votre organisation en suivant les étapes décrites dans la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="7e8ce-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="7e8ce-p103">D'autres valeurs BCL sont ajoutées et seront incluses ici à l'avenir. Le tableau suivant répertorie et décrit les valeurs BCL actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="7e8ce-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e8ce-126">**Valeur BCL**</span><span class="sxs-lookup"><span data-stu-id="7e8ce-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="7e8ce-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e8ce-127">**Description**</span></span> <br/> |
|<span data-ttu-id="7e8ce-128">0</span><span class="sxs-lookup"><span data-stu-id="7e8ce-128">0</span></span>  <br/> |<span data-ttu-id="7e8ce-129">Le message ne provient pas d'un expéditeur en bloc.</span><span class="sxs-lookup"><span data-stu-id="7e8ce-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="7e8ce-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="7e8ce-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="7e8ce-131">Le message provient d'un expéditeur en bloc qui génère peu de réclamations.</span><span class="sxs-lookup"><span data-stu-id="7e8ce-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="7e8ce-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="7e8ce-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="7e8ce-133">Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.</span><span class="sxs-lookup"><span data-stu-id="7e8ce-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="7e8ce-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="7e8ce-134">8, 9</span></span>  <br/> |<span data-ttu-id="7e8ce-135">Le message provient d'un expéditeur en bloc qui génère un grand nombre de réclamations</span><span class="sxs-lookup"><span data-stu-id="7e8ce-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   

