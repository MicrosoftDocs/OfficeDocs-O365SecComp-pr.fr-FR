---
title: Prise en charge de la validation des messages signés DKIM
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: Exchange Online Protection (EOP) et Exchange Online prennent en charge la validation entrante des messages DKIM (Domain Keys Identified Mail). Il s'agit d'une méthode de validation des messages envoyés depuis le domaine dont ils indiquent provenir et qui n'ont pas été usurpés par un autre utilisateur. Elle associe un message électronique à l'organisation responsable de son envoi. La vérification DKIM est automatiquement utilisée pour tous les messages envoyés dans le cadre de communications IPv6. (Pour plus d'informations sur la prise en charge d'IPv6, voir Prise en charge des messages entrants anonymes sur IPv6.)
ms.openlocfilehash: d2fab69847732bb7ed54f943d2c7845e06084936
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002256"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="4864a-107">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="4864a-107">Support for validation of DKIM signed messages</span></span>

<span data-ttu-id="4864a-p102">Exchange Online Protection (EOP) et Exchange Online prennent en charge la validation entrante des messages DKIM ([Domain Keys Identified Mail](https://www.rfc-editor.org/rfc/rfc6376.txt)). Il s'agit d'une méthode de validation des messages envoyés depuis le domaine dont ils indiquent provenir et qui n'ont pas été usurpés par un autre utilisateur. Elle associe un message électronique à l'organisation responsable de son envoi. La vérification DKIM est automatiquement utilisée pour tous les messages envoyés dans le cadre de communications IPv6. (Pour plus d'informations sur la prise en charge d'IPv6, voir [Prise en charge des messages entrants anonymes sur IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span><span class="sxs-lookup"><span data-stu-id="4864a-p102">Exchange Online Protection (EOP) and Exchange Online support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages. DKIM is a method for validating that a message was sent from the domain it says it originated from and that it was not spoofed by someone else. It ties an email message to the organization responsible for sending it. DKIM verification is automatically used for all messages sent over IPv6 communications. (For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>
  
<span data-ttu-id="4864a-p103">La technologie DKIM valide un message signé numériquement qui apparaît dans l'en-tête réservé à la signature DKIM au niveau des en-têtes de message. Les résultats d'une validation par signature DKIM sont intégrés à l'en-tête des résultats d'authentification, conformément à la norme RFC 7001 ([champ de l'en-tête du message permettant d'indiquer le statut d'authentification du message](https://www.rfc-editor.org/rfc/rfc7001.txt)). Le texte de l'en-tête du message ressemble à peu près à ce qui suit (où contoso.com correspond à l'expéditeur) :</span><span class="sxs-lookup"><span data-stu-id="4864a-p103">DKIM validates a digitally signed message that appears in the DKIM-Signature header in the message headers. The results of a DKIM-Signature validation is stamped in the Authentication-Results header which conforms with RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt)). The message header text appears similar to the following (where contoso.com is the sender):</span></span>
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
<span data-ttu-id="4864a-116">Les administrateurs peuvent créer des [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) Exchange à partir des résultats d’une validation DKIM pour filtrer ou acheminer des messages en fonction de leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="4864a-116">Admins can create Exchange [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) on the results of a DKIM validation to filter or route messages as needed.</span></span> 
  

