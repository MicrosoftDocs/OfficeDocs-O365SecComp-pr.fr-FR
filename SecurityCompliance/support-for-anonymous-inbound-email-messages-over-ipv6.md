---
title: Prise en charge des messages entrants anonymes sur IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Découvrez comment configurer la prise en charge pour les messages provenant de sources IPv6 anonymes pour Exchange Online Protection et Exchange Online.
ms.openlocfilehash: 0d324ce6e0ff0ff9104ef597176b09a5a319abc7
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255809"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Prise en charge des messages entrants anonymes sur IPv6

Exchange Online Protection (EOP) et Exchange Online prend en charge la réception de messages électroniques entrants anonymes sur IPv6 communications provenant d’expéditeurs qui ne pas envoyer des messages sur Transport Layer Security (TLS). Vous pouvez choisir de recevoir des messages en demandant cette fonctionnalité dans le Support Microsoft en ouvrant le centre d’administration Office 365 à IPv6 [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), en cliquant sur la **prise en charge**, puis en cliquant sur **nouvelle demande de service**). Si vous n’adhésion au protocole IPv6, vous allez continuer à recevoir des messages sur IPv4.
  
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
  

