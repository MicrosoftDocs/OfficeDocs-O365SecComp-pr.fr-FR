---
title: Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d'attente, différés ou retournés lors du processus de filtrage Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 17e5955195c4e38299712fb9161822984b2a643a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026221"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="26b2d-103">Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP</span><span class="sxs-lookup"><span data-stu-id="26b2d-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="26b2d-104">Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d'attente, différés ou retournés lors du processus de filtrage Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="26b2d-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="26b2d-105">**Q. Pourquoi le courrier électronique est-il mis en file d'attente ?**</span><span class="sxs-lookup"><span data-stu-id="26b2d-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="26b2d-p101">R. Les messages sont mis en file d'attente ou différés si le service n'est pas en mesure d'établir une connexion au serveur du destinataire en vue de la remise. Les messages ne sont pas différés si le réseau du destinataire renvoie une erreur de la série 500.</span><span class="sxs-lookup"><span data-stu-id="26b2d-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="26b2d-109">**Q. Dans quelles circonstances un message est-il différé ?**</span><span class="sxs-lookup"><span data-stu-id="26b2d-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="26b2d-p102">R. Les messages sont retenus s'il est impossible d'établir une connexion au serveur du destinataire et que celui-ci renvoie une « défaillance temporaire », comme une expiration de connexion, un refus de connexion ou une erreur de la série 400. En cas de défaillance permanente, comme une erreur de la série 500, le message est renvoyé à l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="26b2d-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="26b2d-113">**Q. Combien de temps un message reste-t-il en attente et quel est l'intervalle des nouvelles tentatives ?**</span><span class="sxs-lookup"><span data-stu-id="26b2d-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="26b2d-p103">R. Les messages différés resteront dans nos files d'attente pendant 2 jours. Les nouvelles tentatives d'envoi de message sont basées sur les erreurs que nous recevons à partir du système de messagerie du destinataire. En moyenne, les messages sont renvoyés toutes les 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="26b2d-p103">A. Messages in deferral will remain in our queues for 2 days. Message retry attempts are based on the error we get back from the recipient's mail system. On average, messages are retried every 5 minutes.</span></span>
  
 <span data-ttu-id="26b2d-118">**Q. Après la restauration du serveur de messagerie, comment les messages mis en file d'attente sont-ils distribués ?**</span><span class="sxs-lookup"><span data-stu-id="26b2d-118">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="26b2d-p104">R. Une fois que votre serveur de messagerie est restauré, tous les messages mis en file d'attente sont automatiquement traités dans l'ordre dans lequel ils ont été reçus et mis en file d'attente lorsque le serveur est devenu indisponible.</span><span class="sxs-lookup"><span data-stu-id="26b2d-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

