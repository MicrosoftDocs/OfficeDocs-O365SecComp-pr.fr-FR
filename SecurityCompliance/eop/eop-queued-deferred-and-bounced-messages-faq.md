---
title: Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d'attente, différés ou retournés lors du processus de filtrage Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 7d584d8356cfca805427c5dd41dc3dee2ee57e85
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150266"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>Questions fréquemment posées sur les messages mis en file d’attente, différés et retournés dans EOP

Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d'attente, différés ou retournés lors du processus de filtrage Microsoft Exchange Online Protection (EOP).
  
 **Q. Pourquoi le courrier électronique est-il mis en file d'attente ?**
  
R. Les messages sont mis en file d'attente ou différés si le service n'est pas en mesure d'établir une connexion au serveur du destinataire en vue de la remise. Les messages ne sont pas différés si le réseau du destinataire renvoie une erreur de la série 500.
  
 **Q. Dans quelles circonstances un message est-il différé ?**
  
R. Les messages sont retenus s'il est impossible d'établir une connexion au serveur du destinataire et que celui-ci renvoie une « défaillance temporaire », comme une expiration de connexion, un refus de connexion ou une erreur de la série 400. En cas de défaillance permanente, comme une erreur de la série 500, le message est renvoyé à l'expéditeur.
  
 **Q. Combien de temps un message reste-t-il en attente et quel est l'intervalle des nouvelles tentatives ?**
  
R. Les messages différés resteront dans nos files d'attente pendant 2 jours. Les nouvelles tentatives d'envoi de message sont basées sur les erreurs que nous recevons à partir du système de messagerie du destinataire. Les premiers nombre de retards sont 15 minutes ou moins, avec les nouvelles tentatives suivantes (au cours d’une demi-douzaine ou par conséquent), ce qui augmente l’intervalle entre plusieurs tentatives et une durée maximale de 60 minutes. L’expansion de la durée de l’intervalle est dynamique, en prenant en compte plusieurs variables telles que les tailles de file d’attente et la priorité des messages internes. En standard, il faut 15 minutes (ou moins) pour commencer, puis les prochaines heures à 60 mins max.
  
 **Q. Après la restauration du serveur de messagerie, comment les messages mis en file d'attente sont-ils distribués ?**
  
R. Une fois que votre serveur de messagerie est restauré, tous les messages mis en file d'attente sont automatiquement traités dans l'ordre dans lequel ils ont été reçus et mis en file d'attente lorsque le serveur est devenu indisponible. 
  

