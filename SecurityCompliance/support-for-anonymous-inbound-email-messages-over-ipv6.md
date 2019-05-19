---
title: Prise en charge des messages entrants anonymes sur IPv6
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
description: Découvrez comment configurer la prise en charge des messages anonymes provenant de sources IPv6 pour Exchange Online Protection et Exchange Online.
ms.openlocfilehash: 87317188a4564fccd968b00c9a93dc1b963c142b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158186"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Prise en charge des messages entrants anonymes sur IPv6

Exchange Online Protection (EOP) et Exchange Online prennent en charge la réception de messages électroniques entrants anonymes dans le cadre de communications IPv6 provenant d'expéditeurs qui n'envoient pas de messages via le protocole TLS (Transport Layer Security). Vous pouvez vous abonner pour recevoir des messages via IPv6 en demandant cette fonctionnalité au support Microsoft en ouvrant le centre d’administration Microsoft [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home)365 à l’adresse, en cliquant sur **support**, puis en cliquant sur **nouvelle demande de service**). Si vous refusez les communications IPv6, vous continuerez à recevoir vos messages via le protocole IPv4.
  
Les expéditeurs qui transmettent des messages au service sur IPv6 doivent respecter les deux conditions suivantes :
  
1. L'adresse IPv6 d'envoi doit posséder un enregistrement PTR valide ([enregistrement DNS inversé](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) de l'adresse IPv6 d'envoi). 
    
2. L'expéditeur doit répondre aux exigences de l'étape de vérification SPF (définie dans le fichier [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou de l'étape de [vérification DKIM](http://dkim.org/) (définie dans le fichier [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).
    
Quelle que soit votre configuration, vous devez remplir ces conditions pour utiliser IPv6. Si ces deux conditions sont remplies, le message est traité par le processus normal de filtrage des courriers électroniques proposé par le service. Si l'une ou l'autre de ces conditions n'est pas remplie, le message est rejeté et l'une des réponses 450 suivantes apparaît :
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
Si vous n'avez pas accepté de recevoir des messages sur IPv6 et que l'expéditeur tente de forcer l'envoi d'un message sur IPv6 en se connectant manuellement au serveur de messagerie, le message sera rejeté et une réponse 550 de ce type apparaîtra :
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>Pour plus d’informations

[Prise en charge de la validation des messages signés DKIM](support-for-validation-of-dkim-signed-messages.md)
  

