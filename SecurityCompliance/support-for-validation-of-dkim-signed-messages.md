---
title: Prise en charge de la validation des messages signés DKIM
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: En savoir plus sur la validation des messages signés DKIM dans Exchange Online Protection et Exchange Online
ms.openlocfilehash: 75c104af4b3e6126bac37024de2c7f6ab337a028
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643266"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Prise en charge de la validation des messages signés DKIM

Exchange Online Protection (EOP) et Exchange Online prennent en charge la validation entrante des messages DKIM ([Domain Keys Identified Mail](https://www.rfc-editor.org/rfc/rfc6376.txt)). Il s'agit d'une méthode de validation des messages envoyés depuis le domaine dont ils indiquent provenir et qui n'ont pas été usurpés par un autre utilisateur. Elle associe un message électronique à l'organisation responsable de son envoi. La vérification DKIM est automatiquement utilisée pour tous les messages envoyés dans le cadre de communications IPv6. Office 365 prend également en charge DKIM lorsque le courrier électronique est envoyé via IPv4. (Pour plus d'informations sur la prise en charge d'IPv6, voir [Prise en charge des messages entrants anonymes sur IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)
  
La technologie DKIM valide un message signé numériquement qui apparaît dans l'en-tête réservé à la signature DKIM au niveau des en-têtes de message. Les résultats d'une validation par signature DKIM sont intégrés à l'en-tête des résultats d'authentification, conformément à la norme RFC 7001 ([champ de l'en-tête du message permettant d'indiquer le statut d'authentification du message](https://www.rfc-editor.org/rfc/rfc7001.txt)). Le texte de l'en-tête du message ressemble à peu près à ce qui suit (où contoso.com correspond à l'expéditeur) :
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Les administrateurs peuvent créer des [règles de flux de messagerie](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) Exchange (également appelées règles de transport) sur les résultats d’une validation DKIM pour filtrer ou acheminer les messages selon vos besoins. 
  

