---
title: Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: "Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement. Le service respecte les expéditeurs et les domaines autorisés en inspectant l'adresse RFC 5321.MailFrom, tandis qu'Outlook ajoute l'adresse RFC 5322.From à la liste des expéditeurs autorisés d'un utilisateur. (Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)"
ms.openlocfilehash: cc0f74fccade2e9b3cb96bbab9ec72936df24bae
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670599"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc

Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement. Le service Office 365 respecte les expéditeurs et les domaines approuvés en inspectant l'adresse RFC 5321. MailFrom et l'adresse RFC 5322. from, tandis qu'Outlook ajoute l'adresse RFC 5322. from à la liste des expéditeurs approuvés d'un utilisateur. (Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)
  
L'adresse SMTP MAIL FROM, aussi connue sous le nom « adresse RFC 5321.MailFrom », est l'adresse de messagerie utilisée pour effectuer les vérifications SPF. Si le courrier électronique ne peut être remis, il s'agit du chemin vers lequel le message de retour est envoyé. C'est cette adresse électronique qui est placée dans le chemin de retour des en-têtes de message par défaut, mais il est possible pour l'expéditeur de désigner une adresse de chemin de retour différente.
  
L'adresse de l'expéditeur dans les en-têtes de message, aussi connue sous le nom « adresse RFC 5322.From », est l'adresse de messagerie affichée dans le client de messagerie, comme Outlook.
  
La plupart du temps, les adresses 5321.MailFrom et 5322.From sont identiques. C'est généralement le cas pour la communication entre deux-personnes. Toutefois, lorsqu'un courrier électronique est envoyé à la place d'une autre personne, les adresses sont souvent différentes. Cela se produit généralement avec les messages de courrier indésirable.
  
Par exemple, supposons que la compagnie aérienne Blue Yonder Airlines ait demandé à la société Margie's Travel d'envoyer sa publicité par courrier électronique. Vous obtenez alors un message dans votre boîte de réception provenant de l'expéditeur blueyonder@news.blueyonderairlines.com. Dans ce cas, l'adresse 5321. MailFrom est blueyonder.airlines@margiestravel.com et blueyonder@news.blueyonderairlines.com est l'adresse 5322. from qui est la personne, qui est affichée dans Outlook. Étant donné que le service respecte l'adresse RFC 5322. from, pour empêcher le filtrage de ce message, vous pouvez ajouter l'adresse RFC 5322. from comme expéditeur approuvé dans Outlook (en tant qu'utilisateur) ou, si vous êtes administrateur, configurer une règle de flux de messagerie comme indiqué sur le blocage du courrier indésirable. [ Section protection](anti-spam-protection.md) .
  

