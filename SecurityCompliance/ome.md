---
title: Chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/6/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l'intérieur et à l'extérieur de votre organisation. Le chiffrement des messages électroniques permet de s'assurer que seuls les destinataires prévus peuvent afficher le contenu du message.
ms.openlocfilehash: eae2b6ca4756fc90837c2bfac4b5eae20001d37a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220284"
---
# <a name="office-365-message-encryption"></a>Chiffrement de messages Office 365

Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l'intérieur et à l'extérieur de votre organisation. Le chiffrement de messages Office 365 fonctionne avec Outlook.com, Yahoo!, Gmail et d'autres services de messagerie. Le chiffrement des messages électroniques permet de s'assurer que seuls les destinataires prévus peuvent afficher le contenu du message.
  
Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Utilisez le tableau suivant pour trouver rapidement les informations dont vous avez besoin.
  
|||
|:-----|:-----|
|Lisez cet article...  <br/> |Si vous êtes...  <br/> |
|[En savoir plus sur les messages protégés dans Office 365](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |Utilisateur final qui souhaite en savoir plus sur le fonctionnement des messages chiffrés et sur les options disponibles.  <br/> |
|[Comment ouvrir un message protégé?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |Utilisateur final souhaitant lire un message protégé qui vous a été envoyé. Cet article contient des informations sur la lecture de messages dans plusieurs versions d'Outlook et de comptes de messagerie différents, y compris ceux qui se trouvent en dehors d'Office 365 tels que les comptes Gmail et Yahoo!.  <br/> |
|[Envoyer, afficher et répondre à des messages chiffrés dans Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |Un utilisateur final qui souhaite envoyer, afficher ou répondre à un message chiffré à partir d'Outlook. Même si vous n'êtes pas membre d'une organisation Office 365, vous recevez toujours une notification de messages chiffrés qui vous sont envoyés dans Outlook. Utilisez cet article pour obtenir des instructions sur la façon d'afficher et de répondre aux messages chiffrés envoyés à partir d'Office 365.  <br/> |
|[Envoyer un message chiffré ou signé numériquement](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |Un utilisateur final qui souhaite envoyer, afficher ou répondre à des messages chiffrés à l'aide d'Outlook pour Mac. Cet article décrit également l'utilisation de méthodes de chiffrement autres que OME, telles que S/MIME.  <br/> |
|[Afficher des messages chiffrés sur votre appareil Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |Un utilisateur final qui a reçu un message chiffré avec le chiffrement de messages Office 365 sur votre appareil Android, vous pouvez utiliser l'application OME Viewer gratuite pour afficher le message et envoyer une réponse chiffrée. Cet article explique comment procéder.  <br/> |
|[Afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |Un utilisateur final qui a reçu un message chiffré avec le chiffrement de messages Office 365 sur votre iPhone ou iPad, vous pouvez utiliser l'application gratuite OME Viewer pour afficher le message et envoyer une réponse chiffrée. Cet article explique comment procéder.  <br/> |
|Office 365 message enCryption (OME) (cet article)  <br/> |Un administrateur Office 365 ou Exchange Online protection qui souhaite savoir où trouver des ressources supplémentaires.  <br/> |
|[Comparez les versions de OME](ome-version-comparison.md)  <br/> |Un administrateur Office 365 ou Exchange Online Protection souhaitant connaître les différences entre le chiffrement de messages Office 365 hérité et les nouvelles fonctionnalités OME, ainsi que la façon dont ils peuvent travailler ensemble.  <br/> |
|[FAQ sur le chiffrement de messages Office 365](ome-faq.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui souhaite des réponses aux questions fréquemment posées, notamment des licences et une comparaison entre les nouvelles fonctionnalités et les OME héritées.  <br/> |
|[Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365](set-up-new-message-encryption-capabilities.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui souhaite apprendre à configurer les nouvelles fonctionnalités de chiffrement des messages Office 365 pour votre organisation Office 365.  <br/> |
|[Définir des règles de flux de courrier pour le chiffrement du courriers dans Office 365](define-mail-flow-rules-to-encrypt-email.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui a déjà configuré le chiffrement de messages Office 365 et vous êtes prêt à définir des règles de flux de messagerie pour chiffrer automatiquement les messages électroniques envoyés à partir de votre organisation.  <br/> |
|[Gérer le chiffrement de messages Office 365](manage-office-365-message-encryption.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui a déjà configuré le chiffrement de messages Office 365 et souhaite configurer des paramètres facultatifs pour OME.  <br/> |
|[Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui souhaite appliquer votre marque de société pour personnaliser l'apparence des messages électroniques de chiffrement des messages Office 365 de votre organisation et le contenu du portail OME.  <br/> |
|[Révocation de courrier de chiffrement de messages Office 365](revoke-ome-encrypted-mail.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui souhaite révoquer un courrier électronique chiffré à l'aide du chiffrement de messages Office 365.  <br/> |
|Chiffrement de messages Office 365 dans la description de la [stratégie de message et du service de conformité](https://technet.microsoft.com/en-us/library/5c43c8eb-f8f7-4b5a-a743-b1dab7dc2fc8#bkmk_O365_MessageEncryption) <br/> |Recherche d'une description détaillée de la fonctionnalité de chiffrement des messages Office 365, y compris les UGS prises en charge, disponibles auprès d'Office 365.  <br/> |
|[Informations héritées pour le chiffrement de messages Office 365](legacy-information-for-message-encryption.md) <br/> |Un administrateur Office 365 ou Exchange Online protection qui a déjà configuré le chiffrement de messages Office 365 et vous souhaitez obtenir des informations sur la façon dont OME fonctionnait avant la publication des nouvelles fonctionnalités. Bien que vous ne pouvez pas configurer un nouveau déploiement à l'aide de OME sans les nouvelles fonctionnalités, Microsoft continue de prendre en charge les déploiements existants.  <br/> |
||

Le reste de cet article s'applique aux nouvelles fonctionnalités OME.
  
## <a name="how-office-365-message-encryption-works"></a>Fonctionnement du chiffrement de messages Office 365

Le chiffrement de messages Office 365 est un service en ligne qui repose sur Microsoft Azure Rights Management (Azure RMS) qui fait partie d'Azure information protection. Les administrateurs d'Office 365 peuvent définir des règles de flux de messagerie pour déterminer les conditions de chiffrement. Par exemple, une règle peut exiger le chiffrement de tous les messages adressés à un destinataire spécifique.
  
Lorsqu'une personne envoie un message électronique dans Exchange Online correspondant à une règle de flux de messagerie de chiffrement, le message est chiffré avant d'être envoyé. Tous les utilisateurs finaux Office 365 qui utilisent des clients Outlook pour lire le courrier électronique natif de la lecture de la première classe pour les messages chiffrés et protégés par des droits, même s'ils ne se trouvent pas dans la même organisation que l'expéditeur. Les clients Outlook pris en charge incluent Outlook Desktop, Outlook Mac, Outlook Mobile sur iOS et Android, et Outlook sur le Web (anciennement appelé Outlook Web App).
  
Les destinataires des messages chiffrés qui reçoivent des messages chiffrés ou protégés par des droits envoyés à leurs comptes Outlook.com, Gmail et Yahoo peuvent facilement s'authentifier auprès du portail OME à l'aide de leur compte Microsoft, ou des informations d'identification Gmail ou Yahoo.
  
Les utilisateurs finaux qui lisent des messages chiffrés ou protégés par des droits sur des clients autres qu'Outlook utilisent également le portail OME pour afficher les messages chiffrés et protégés par des droits qu'ils reçoivent.
  
Nous avons augmenté les limites de taille pour les messages et les pièces jointes que vous pouvez chiffrer à l'aide du chiffrement de messages Office 365. Pour plus d'informations sur les limites, consultez la rubrique [limites d'Exchange Online.](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
  
## <a name="defining-rules-for-office-365-message-encryption"></a>Définir les règles pour le chiffrement de messages Office 365

Pour activer les nouvelles fonctionnalités pour le chiffrement de messages Office 365, les administrateurs Exchange Online et Exchange Online protection doivent définir des règles de flux de messagerie. Ces règles déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés. Lorsqu'une action de chiffrement est définie pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés avant d'être envoyés.
  
Les règles de flux de messagerie sont flexibles, ce qui vous permet de combiner des conditions afin de répondre à des exigences spécifiques en matière de sécurité dans une seule règle. Par exemple, vous pouvez créer une règle pour chiffrer tous les messages qui contiennent des mots clés spécifiés et qui sont adressés à des destinataires externes. Les nouvelles fonctionnalités pour le chiffrement de messages Office 365 chiffrent également les réponses provenant de destinataires de messages électroniques chiffrés.
  
Pour plus d'informations sur la création de règles de flux de messagerie afin de tirer parti des nouvelles fonctionnalités OME, voir [define Rules for Office 365 message](define-mail-flow-rules-to-encrypt-email.md)Encryption.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Envoyer, consulter et répondre à des messages électroniques chiffrés

Avec le chiffrement de messages Office 365, les utilisateurs peuvent envoyer des messages chiffrés à partir d'Outlook et d'Outlook sur le Web. En outre, les administrateurs peuvent configurer des règles de flux de messagerie dans Office 365 pour chiffrer automatiquement les messages électroniques en fonction de la correspondance de mots clés ou d'autres conditions.
  
Les destinataires des messages chiffrés qui se trouvent dans les organisations Office 365 peuvent lire ces messages de façon transparente dans n'importe quelle version d'Outlook, y compris Outlook pour PC, Outlook pour Mac, Outlook sur le Web, Outlook pour iOS et Outlook pour Android. Les utilisateurs qui reçoivent des messages chiffrés sur d'autres clients de messagerie peuvent afficher les messages dans le portail OME.
  
Pour obtenir des conseils détaillés sur la façon d'envoyer et d'afficher des messages chiffrés, consultez les articles suivants:
  
- [Comment ouvrir un message protégé?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx)

- [Envoyer, afficher et répondre à des messages chiffrés dans Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx)

## <a name="get-started-with-the-new-ome-capabilities"></a>Prise en main des nouvelles fonctionnalités OME

Si vous êtes prêt à commencer à utiliser les nouvelles fonctionnalités de OME au sein de votre organisation, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).
