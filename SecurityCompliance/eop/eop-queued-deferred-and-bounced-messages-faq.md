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
ms.openlocfilehash: 4b2c902adacd6e72e587aadaceecd22dd0084d85
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686424"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a>Questions fréquemment posées sur les messages mis en file d'attente, différés et retournés dans EOP

Cette rubrique fournit des réponses aux questions fréquemment posées sur les messages mis en file d'attente, différés ou retournés lors du processus de filtrage Microsoft Exchange Online Protection (EOP).
  
 **Q. Pourquoi le courrier électronique est-il mis en file d'attente ?**
  
R. Les messages sont mis en file d'attente ou différés si le service n'est pas en mesure d'établir une connexion au serveur du destinataire en vue de la remise. Les messages ne sont pas différés si le réseau du destinataire renvoie une erreur de la série 500.
  
 **Q. Dans quelles circonstances un message est-il différé ?**
  
R. Les messages sont retenus s'il est impossible d'établir une connexion au serveur du destinataire et que celui-ci renvoie une « défaillance temporaire », comme une expiration de connexion, un refus de connexion ou une erreur de la série 400. En cas de défaillance permanente, comme une erreur de la série 500, le message est renvoyé à l'expéditeur.
  
 **Q. Combien de temps un message reste-t-il en attente et quel est l'intervalle des nouvelles tentatives ?**
  
A messages report reste dans nos files d’attente pendant deux jours. Nouvelle tentative est basées sur l’erreur, que nous obtenons à partir du système de messagerie du destinataire. Premières Reports peu sont 15 minutes ou moins, avec des tentatives suivantes (sur la dizaine de moitié suivant ou ainsi) en augmentant l’intervalle sur plusieurs tentatives pour un maximum de 60 minutes. Le développement de durée intervalle est dynamique, en tenant compte de plusieurs variables, telles que les tailles de file d’attente et la priorité du message interne. Dans basic, il est de 15 minutes (ou moins) pour démarrer, puis en développant à partir de là sur les quelques heures suivant à 60 minutes maximum.
  
 **Q. Après la restauration du serveur de messagerie, comment les messages mis en file d'attente sont-ils distribués ?**
  
R. Une fois que votre serveur de messagerie est restauré, tous les messages mis en file d'attente sont automatiquement traités dans l'ordre dans lequel ils ont été reçus et mis en file d'attente lorsque le serveur est devenu indisponible. 
  

