---
title: Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 03/14/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Si votre administrateur Active les notifications pour les utilisateurs, vous recevrez un message de notification répertoriant les messages envoyés à votre boîte aux lettres identifiés comme courriers indésirables, en masse ou par hameçonnage. Vous pouvez publier ou signaler des messages après leur notification.
ms.openlocfilehash: 499af3ae2934eed19e421918af07a45b72fe2518
ms.sourcegitcommit: f57d411e06c955d648dfa1a2a473aa45416e1377
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2019
ms.locfileid: "36620478"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a>Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365

Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.
  
> [!TIP]
> Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l’option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](https://go.microsoft.com/fwlink/?LinkId=800313). 
  
Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l’heure (au format UTC ou UTC) du dernier message de la liste. La liste inclut les éléments suivants pour chaque message:
  
- **Expéditeur** Nom d’envoi et adresse de messagerie du message en quarantaine. 
    
- **Objet** Texte de l'objet du message en quarantaine. 
    
- **Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine. 
    
- **Taille** Taille du message, en kilo-octets (Ko). 
    
Voici les actions que vous pouvez effectuer avec un message en quarantaine:

- **Affichez un aperçu** du message si vous souhaitez afficher un aperçu du contenu ou de l’en-tête avant de prendre une mesure.

- **Téléchargez** le message si vous souhaitez consulter le message et les pièces jointes (le cas échéant) sur votre appareil avant de prendre une mesure.

- **Release** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 envoie le message à votre boîte aux lettres.

- **Release & autoriser l’expéditeur** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs et destinataires approuvés pour les futurs courriers électroniques. Gardez à l’esprit que votre administrateur peut avoir d’autres configurations autoriser/bloquer des organisations qui remplacent votre liste d’expéditeurs autorisés.

- **Release & Report**, si le message n’est pas indésirable et que vous voulez envoyer le message à votre boîte aux lettres et le signaler à Microsoft pour analyse.

- **Bloquer l’expéditeur** si vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs bloqués.

Prenez en considération ce qui suit :
  
- Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l’utilisateur. Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.
    
- Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.
    

