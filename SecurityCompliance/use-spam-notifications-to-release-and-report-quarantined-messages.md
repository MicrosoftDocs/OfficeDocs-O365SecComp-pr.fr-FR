---
title: Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
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
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492723"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a>Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365

Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.
  
> [!TIP]
> Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l'option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](https://go.microsoft.com/fwlink/?LinkId=800313). 
  
Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l'heure (au format UTC ou UTC) du dernier message de la liste. La liste inclut les éléments suivants pour chaque message:
  
- **Expéditeur** Nom d'envoi et adresse de messagerie du message en quarantaine. 
    
- **Objet** Texte de l'objet du message en quarantaine. 
    
- **Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine. 
    
- **Taille** Taille du message, en kilo-octets (Ko). 
    
Actuellement, il existe deux actions que vous pouvez effectuer avec un message en quarantaine:
  
- **Publier dans la boîte de réception** Choisissez cette adresse pour envoyer le message vers votre boîte de réception, où vous pouvez l'afficher. 
    
- **Signaler comme légitime** Choisissez cette adresse pour envoyer une copie du message à Microsoft pour analyse. L'équipe du courrier indésirable évalue et analyse le message, puis, selon les résultats de l'analyse, adapte les règles de filtre de courrier indésirable pour autoriser le message. 
    
Prenez en considération ce qui suit :
  
- Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l'utilisateur. Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.
    
- Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.
    

