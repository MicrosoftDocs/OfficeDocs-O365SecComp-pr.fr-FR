---
title: Prise en charge des messages entrants anonymes sur IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/4/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Exchange Online Protection (EOP) et Exchange Online prend en charge la réception de messages électroniques entrants anonymes sur IPv6 communications provenant d’expéditeurs qui ne pas envoyer des messages sur Transport Layer Security (TLS). Vous pouvez choisir de recevoir des messages en demandant cette fonctionnalité UNRESOLVED_TOKEN_VAL(exMCSS) en ouvrant le centre d’administration Office 365 à IPv6 https://portal.office.com/adminportal/home, en cliquant sur la prise en charge, puis en cliquant sur Nouvelle demande de service). Si vous n’adhésion au protocole IPv6, vous allez continuer à recevoir des messages sur IPv4.
ms.openlocfilehash: a07e79732e9027d5848b787101be11066b5f0cb5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026291"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Prise en charge des messages entrants anonymes sur IPv6

Exchange Online Protection (EOP) et Exchange Online prennent en charge la réception de messages électroniques entrants anonymes dans le cadre de communications IPv6 provenant d'expéditeurs qui n'envoient pas de messages via le protocole TLS (Transport Layer Security). Vous pouvez accepter de recevoir des messages sur IPv6 en demandant à bénéficier de cette fonctionnalité auprès de UNRESOLVED_TOKEN_VAL(exMCSS) en ouvrant le Centre d'administration Office 365 à l'adresse [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), et en cliquant sur **Support**, puis sur **Nouvelle demande de service**. Si vous refusez les communications IPv6, vous continuerez à recevoir vos messages via le protocole IPv4.
  
Les expéditeurs qui transmettent des messages au service sur IPv6 doivent respecter les deux conditions suivantes :
  
1. L'adresse IPv6 d'envoi doit posséder un enregistrement PTR valide ([enregistrement DNS inversé](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) de l'adresse IPv6 d'envoi). 
    
2. L'expéditeur doit répondre aux exigences de l'étape de vérification SPF (définie dans le fichier [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou de l'étape de [vérification DKIM](http://dkim.org/) (définie dans le fichier [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).
    
Quelle que soit votre configuration, vous devez remplir ces conditions pour utiliser IPv6. Si ces deux conditions sont remplies, le message est traité par le processus normal de filtrage des courriers électroniques proposé par le service. Si l'une ou l'autre de ces conditions n'est pas remplie, le message est rejeté et l'une des réponses 450 suivantes apparaît :
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
Si vous n'avez pas accepté de recevoir des messages sur IPv6 et que l'expéditeur tente de forcer l'envoi d'un message sur IPv6 en se connectant manuellement au serveur de messagerie, le message sera rejeté et une réponse 550 de ce type apparaîtra :
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>Pour plus d'informations

[Prise en charge de la validation des messages signés DKIM](support-for-validation-of-dkim-signed-messages.md)
  

