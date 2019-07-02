---
title: Chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l’intérieur et à l’extérieur de votre organisation. Le chiffrement des messages électroniques permet de s’assurer que seuls les destinataires prévus peuvent afficher le contenu du message.
ms.openlocfilehash: f6f6f59225d267d08ba20e1fdea219dc5d890ed5
ms.sourcegitcommit: b9d8a43cb3afcdc8820bc9470c5707eff8fc6616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34852858"
---
# <a name="office-365-message-encryption"></a>Chiffrement de messages Office 365

Les messageries électroniques sont souvent utilisées pour échanger des informations sensibles. Par exemple : rapports et états financiers, contrats juridiques, informations confidentielles sur des produits, comptes rendus et prévisions de ventes, données médicales relatives à des patients ou informations sur les clients et le personnel. Il s'en suit que les boîtes aux lettres deviennent vite des référentiels contenant de gros volumes d'informations potentiellement sensibles. C'est pourquoi, toute fuite d'informations peut constituer une véritable menace pour votre organisation.

Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l’intérieur et à l’extérieur de votre organisation. Le chiffrement de messages Office 365 fonctionne avec Outlook.com, Yahoo!, Gmail et d’autres services de messagerie. Le chiffrement des messages électroniques permet de s’assurer que seuls les destinataires prévus peuvent afficher le contenu du message.
  
Le reste de cet article s’applique aux nouvelles fonctionnalités OME.
  
## <a name="how-office-365-message-encryption-works"></a>Fonctionnement du chiffrement de messages Office 365

Le chiffrement de messages Office 365 est un service en ligne qui repose sur Microsoft Azure Rights Management (Azure RMS) qui fait partie d’Azure information protection. Cela inclut les stratégies de chiffrement, d’identité et d’autorisation pour sécuriser votre courrier électronique. Vous pouvez chiffrer les messages à l’aide des modèles de gestion des droits, de l' [option ne pas transférer](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)et de l' [option de chiffrement uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

Les utilisateurs peuvent ensuite chiffrer les messages électroniques et une variété de pièces jointes Office 365 à l’aide de ces options. Pour obtenir la liste complète des types de pièces jointes prises en charge, voir [«types de fichiers couverts par les stratégies IRM lorsqu’ils sont attachés à des messages» dans Introduction to IRM for email messages](https://support.office.com/article/bb643d33-4a3f-4ac7-9770-fd50d95f58dc#FileTypesforIRM).

En tant qu’administrateur, vous pouvez également définir des règles de flux de messagerie pour appliquer cette protection. Par exemple, vous pouvez créer une règle qui nécessite le chiffrement de tous les messages adressés à un destinataire spécifique, ou contenant des mots spécifiques dans la ligne d’objet, et spécifier que les destinataires ne peuvent pas copier ou imprimer le contenu du message.

Contrairement à la version précédente de OME, les nouvelles fonctionnalités fournissent une expérience d’expéditeur unifiée, que vous envoyiez du courrier à l’intérieur de votre organisation ou à des destinataires en dehors d’Office 365. De plus, les destinataires qui reçoivent un message électronique protégé envoyé à un compte Office 365 dans Outlook 2016 ou Outlook sur le Web ne doivent effectuer aucune action supplémentaire pour afficher le message. Elle fonctionne de façon transparente. Les destinataires qui utilisent d’autres clients de messagerie et des fournisseurs de services de messagerie ont également une expérience améliorée. Pour plus d’informations, consultez la rubrique [en savoir plus sur les messages protégés dans Office 365](https://support.office.com/article/Learn-about-protected-messages-in-Office-365-2baf3ac7-12db-40a4-8af7-1852204b4b67) et [Comment ouvrir un message protégé](https://support.office.com/article/How-do-I-open-a-protected-message-1157a286-8ecc-4b1e-ac43-2a608fbf3098).

Pour obtenir une liste détaillée des différences entre la version précédente de OME et les nouvelles fonctionnalités OME, consultez la rubrique [compare versions of OME](ome-version-comparison.md).

Lorsqu’une personne envoie un message électronique qui correspond à une règle de flux de messagerie de chiffrement, le message est chiffré avant d’être envoyé. Tous les utilisateurs finaux Office 365 qui utilisent des clients Outlook pour lire le courrier électronique natif de la lecture de la première classe pour les messages chiffrés et protégés par des droits, même s’ils ne se trouvent pas dans la même organisation que l’expéditeur. Les clients Outlook pris en charge incluent Outlook Desktop, Outlook Mac, Outlook Mobile sur iOS et Android, et Outlook sur le Web (anciennement appelé Outlook Web App).
  
Les destinataires des messages chiffrés qui reçoivent des messages chiffrés ou protégés par des droits envoyés à leurs comptes Outlook.com, Gmail et Yahoo reçoivent un courrier de wrapper qui les dirige vers le portail OME où ils peuvent facilement s’authentifier à l’aide d’un compte Microsoft, Gmail ou Informations d’identification yahoo.
  
Les utilisateurs finaux qui lisent des messages chiffrés ou protégés par des droits sur des clients autres qu’Outlook utilisent également le portail OME pour afficher les messages chiffrés et protégés par des droits qu’ils reçoivent.

En outre, si l’expéditeur du courrier protégé est dans GCC High et que le destinataire est en dehors de GCC High, y compris les utilisateurs commerciaux 365 de commerce, les utilisateurs de Outlook.com et les utilisateurs d’autres fournisseurs de courrier tels que Gmail, le destinataire reçoit un courrier de wrapper qui redirige vers Portail OME dans lequel le destinataire peut lire le message et y répondre. Dans le cas contraire, si l’expéditeur et le destinataire sont tous les deux dans l’environnement de GCC High, puis les destinataires qui utilisent des clients Outlook pour lire le courrier électronique natif de la lecture de première classe pour les messages chiffrés et protégés par des droits, même s’ils ne se trouvent pas dans la même organisation comme expéditeur. Pour plus d’informations sur les différentes expériences de GCC High, voir [compare versions of OME](ome-version-comparison.md).
  
Nous avons augmenté les limites de taille pour les messages et les pièces jointes que vous pouvez chiffrer à l’aide de OME. Pour plus d’informations sur les limites, consultez la rubrique [limites d’Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx).

## <a name="how-office-365-advanced-message-encryption-works-on-top-of-ome"></a>Fonctionnement du chiffrement de messages avancé Office 365 sur OME

Le chiffrement de messages avancé Office 365 permet de créer plusieurs modèles de personnalisation afin que vous puissiez affiner le contrôle du courrier des destinataires et créer des expériences personnalisées pour prendre en charge une structure d’organisation diversifiée.

Le chiffrement de messages avancé dans Office 365 vous aide à respecter les obligations de conformité qui nécessitent un contrôle plus flexible de l’accès des destinataires externes aux messages chiffrés. Avec le chiffrement de messages avancé dans Office 365, en tant qu’administrateur, vous pouvez contrôler les e-mails sensibles partagés hors de l’organisation à l’aide de stratégies automatiques qui détectent des types d’informations sensibles (par exemple, des données personnelles, des ID financiers ou d’assurance maladie) ou des mots clés à améliorer. protection en arrivant à expiration de l’accès via un portail Web sécurisé aux e-mails chiffrés. En outre, en tant qu’administrateur, vous pouvez contrôler les e-mails chiffrés accessibles en externe via un portail Web Office 365 en révoquant l’accès à un e-mail à tout moment.

La révocation et l’expiration des messages fonctionnent uniquement pour les courriers électroniques que vos utilisateurs envoient à des destinataires extérieurs à votre organisation Office 365. En outre, les destinataires doivent accéder au courrier électronique par le biais du portail Web. Pour vous assurer que le destinataire utilise le portail pour recevoir des courriers électroniques, vous configurez un modèle de personnalisation qui applique le wrapper. Ensuite, vous appliquez le modèle de personnalisation dans une règle de flux de messagerie. Pour plus d’informations sur le chiffrement de messages avancé, consultez la rubrique [Office 365 Advanced message](ome-advanced-message-encryption.md)Encryption.

## <a name="defining-rules-for-office-365-message-encryption"></a>Définir les règles pour le chiffrement de messages Office 365

Pour activer les nouvelles fonctionnalités pour le chiffrement de messages Office 365, les administrateurs Exchange Online et Exchange Online protection doivent définir des règles de flux de messagerie. Ces règles déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés. Lorsqu’une action de chiffrement est définie pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés avant d’être envoyés.
  
Les règles de flux de messagerie sont flexibles, ce qui vous permet de combiner des conditions afin de répondre à des exigences spécifiques en matière de sécurité dans une seule règle. Par exemple, vous pouvez créer une règle pour chiffrer tous les messages qui contiennent les mots-clés spécifiés et adressés à des destinataires externes. Les nouvelles fonctionnalités pour le chiffrement de messages Office 365 chiffrent également les réponses provenant de destinataires de messages électroniques chiffrés.
  
Pour plus d’informations sur la création de règles de flux de messagerie afin de tirer parti des nouvelles fonctionnalités OME, voir [define Rules for Office 365 message](define-mail-flow-rules-to-encrypt-email.md)Encryption.
  
## <a name="get-started-with-the-new-ome-capabilities"></a>Prise en main des nouvelles fonctionnalités OME

Si vous êtes prêt à commencer à utiliser les nouvelles fonctionnalités de OME au sein de votre organisation, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).

## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Envoyer, consulter et répondre à des messages électroniques chiffrés

Avec le chiffrement de messages Office 365, les utilisateurs peuvent envoyer des messages chiffrés à partir d’Outlook et d’Outlook sur le Web. En outre, les administrateurs peuvent configurer des règles de flux de messagerie dans Office 365 pour chiffrer automatiquement les messages électroniques en fonction de la correspondance de mots clés ou d’autres conditions.
  
Les destinataires des messages chiffrés qui se trouvent dans les organisations Office 365 peuvent lire ces messages de façon transparente dans n’importe quelle version d’Outlook, y compris Outlook pour PC, Outlook pour Mac, Outlook sur le Web, Outlook pour iOS et Outlook pour Android. Les utilisateurs qui reçoivent des messages chiffrés sur d’autres clients de messagerie peuvent afficher les messages dans le portail OME.
  
Pour obtenir des conseils détaillés sur la façon d’envoyer et d’afficher des messages chiffrés, consultez les articles suivants:
  
|||
|:-----|:-----|
|Lisez cet article...  <br/> |Si vous êtes...  <br/> |
|[En savoir plus sur les messages protégés dans Office 365](https://support.office.com/article/2baf3ac7-12db-40a4-8af7-1852204b4b67.aspx) <br/> |Utilisateur final qui souhaite en savoir plus sur le fonctionnement des messages chiffrés et sur les options disponibles.  <br/> |
|[Comment ouvrir un message protégé?](https://support.office.com/article/1157a286-8ecc-4b1e-ac43-2a608fbf3098.aspx) <br/> |Utilisateur final souhaitant lire un message protégé qui vous a été envoyé. Cet article contient des informations sur la lecture de messages dans plusieurs versions d’Outlook et de comptes de messagerie différents, y compris ceux qui se trouvent en dehors d’Office 365 tels que Gmail et Yahoo! compte.  <br/> |
|[Envoyer, afficher et répondre à des messages chiffrés dans Outlook](https://support.office.com/article/eaa43495-9bbb-4fca-922a-df90dee51980.aspx) <br/> |Un utilisateur final qui souhaite envoyer, afficher ou répondre à un message chiffré à partir d’Outlook. Même si vous n’êtes pas membre d’une organisation Office 365, vous recevez toujours une notification de messages chiffrés qui vous sont envoyés dans Outlook. Utilisez cet article pour obtenir des instructions sur la manière d’afficher et de répondre aux messages chiffrés envoyés à partir d’Office 365.  <br/> |
|[Envoyer un message chiffré ou signé numériquement](https://support.office.com/article/a18ecf7f-a7ac-4edd-b02e-687b05eff547) <br/> |Un utilisateur final qui souhaite envoyer, afficher ou répondre à des messages chiffrés à l’aide d’Outlook pour Mac. Cet article décrit également l’utilisation de méthodes de chiffrement autres que OME, telles que S/MIME.  <br/> |
|[Afficher des messages chiffrés sur votre appareil Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> |Un utilisateur final qui a reçu un message chiffré avec le chiffrement de messages Office 365 sur votre appareil Android, vous pouvez utiliser l’application OME Viewer gratuite pour afficher le message et envoyer une réponse chiffrée. Cet article explique comment procéder.  <br/> |
|[Afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |Un utilisateur final qui a reçu un message chiffré avec le chiffrement de messages Office 365 sur votre iPhone ou iPad, vous pouvez utiliser l’application gratuite OME Viewer pour afficher le message et envoyer une réponse chiffrée. Cet article explique comment procéder.  <br/> |
||