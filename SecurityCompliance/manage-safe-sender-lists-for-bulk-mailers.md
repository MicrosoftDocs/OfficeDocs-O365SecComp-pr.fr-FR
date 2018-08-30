---
title: Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc
ms.author: krowley
author: kccross
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
description: "Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement. Le service respecte les expéditeurs et les domaines autorisés en inspectant l'adresse RFC 5321.MailFrom, tandis qu'Outlook ajoute l'adresse RFC 5322.From à la liste des expéditeurs autorisés d'un utilisateur. (Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)"
ms.openlocfilehash: 9442bb39e15b9db9a826472dd6110a8fa14130c6
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002993"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a>Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc

Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement. Le service respecte les expéditeurs et les domaines autorisés en inspectant l'adresse RFC 5321.MailFrom, tandis qu'Outlook ajoute l'adresse RFC 5322.From à la liste des expéditeurs autorisés d'un utilisateur. (Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)
  
L'adresse SMTP MAIL FROM, aussi connue sous le nom « adresse RFC 5321.MailFrom », est l'adresse de messagerie utilisée pour effectuer les vérifications SPF. Si le courrier électronique ne peut être remis, il s'agit du chemin vers lequel le message de retour est envoyé. C'est cette adresse électronique qui est placée dans le chemin de retour des en-têtes de message par défaut, mais il est possible pour l'expéditeur de désigner une adresse de chemin de retour différente.
  
L'adresse de l'expéditeur dans les en-têtes de message, aussi connue sous le nom « adresse RFC 5322.From », est l'adresse de messagerie affichée dans le client de messagerie, comme Outlook.
  
La plupart du temps, les adresses 5321.MailFrom et 5322.From sont identiques. C'est généralement le cas pour la communication entre deux-personnes. Toutefois, lorsqu'un courrier électronique est envoyé à la place d'une autre personne, les adresses sont souvent différentes. Cela se produit généralement avec les messages de courrier indésirable.
  
Par exemple, supposons que la compagnie aérienne Blue Yonder Airlines ait demandé à la société Margie's Travel d'envoyer sa publicité par courrier électronique. Vous obtenez alors un message dans votre boîte de réception provenant de l'expéditeur blueyonder@news.blueyonderairlines.com. Dans ce cas, l'adresse 5321.MailFrom est blueyonder.airlines@margiestravel.com et l'adresse blueyonder@news.blueyonderairlines.com est l'adresse 5322.From, soit celle que vous voyez dans Outlook. Comme le service respecte l'adresse RFC 5322.From, pour éviter que ce message ne soit filtré, vous pouvez simplement ajouter l'adresse RFC 5322.From comme expéditeur autorisé dans Outlook.
  

