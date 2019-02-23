---
title: Comparaison des versions de chiffrement des messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Explique les différences entre les fonctionnalités fournies avec les différentes versions d'Office 365 le chiffrement de messages, ainsi que la façon dont les deux continuent de fonctionner ensemble.
ms.openlocfilehash: 477fbe8f9d71bd92225a7ba5043576f164933b4e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216674"
---
# <a name="compare-versions-of-ome"></a>Comparez les versions de OME

Cet article compare le chiffrement de messages Office 365 hérité aux nouvelles fonctionnalités OME. Les nouvelles fonctionnalités sont une fusion et une version plus récente du OME et de la gestion des droits relatifs à l'information (IRM). Nous allons également découvrir comment les deux peuvent coexister dans votre organisation Office 365.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Comparaison côte à côte des fonctionnalités et des fonctionnalités

|                                   |Anciennes fonctionnalités       |                   |Fonctionnalités nouvelles              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Fonctionnalité**                     | **OME hérité**    | **IRM**           | **Nouvelles fonctionnalités OME** |
|*Envoi d'un message chiffré*        |À l'aide des règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook Desktop ou Outlook sur le Web; ou via les règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook Desktop, Outlook pour Mac ou Outlook sur le Web; par le biais des règles de transport Exchange et d'Office 365 protection contre la perte de données (DLP)|
|*Modèle de gestion des droits*       |   S/O      |Option ne pas transférer et modèles personnalisés|Option ne pas transférer, option de chiffrement uniquement et modèles personnalisés|
|*Type de destinataire*                   |Destinataires internes et externes|Destinataires internes uniquement         |Destinataires internes et externes|
|*Expérience pour les destinataires internes*|Les destinataires reçoivent un message HTML, qu'ils téléchargent et ouvrent dans un navigateur Web ou une application mobile|Expérience incorporée native dans les clients Outlook|Expérience incorporée native pour les destinataires Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (pas de téléchargement ou d'application requis).|
|*Expérience pour les destinataires externes*|Les destinataires reçoivent un message HTML, qu'ils téléchargent et ouvrent dans un navigateur Web ou une application mobile|S/O|Expérience incorporée native pour les destinataires Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (pas de téléchargement ou d'application requis).|
|*Autorisations des pièces jointes*           |Aucune restriction sur les pièces jointes|Les pièces jointes sont protégées|Les pièces jointes sont protégées pour l'option ne pas transférer et les modèles personnalisés. Les administrateurs peuvent choisir de protéger ou non les pièces jointes pour l'option de chiffrement uniquement.|
|*Apporter votre propre prise en charge de la clé (BYOK)*|Aucune                |Aucune               |BYOK pris en charge          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>Avantages de l'utilisation des nouvelles fonctionnalités OME sur les OME héritées

Les nouvelles fonctionnalités offrent les avantages suivants:

- Possibilité d'utiliser le chiffrement uniquement (ce qui permet une collaboration sécurisée), ne pas transférer, ainsi que les restrictions personnalisées.
- Les expéditeurs peuvent envoyer des messages chiffrés avec les nouvelles fonctionnalités manuellement à partir d'Outlook Desktop, Outlook pour Mac et Outlook sur les clients Web.
- Les destinataires d'Office 365 peuvent utiliser une expérience en ligne dans les clients Outlook pris en charge. Par ailleurs, les administrateurs peuvent choisir d'afficher une expérience personnalisée pour les destinataires d'Office 365.
- Les comptes en dehors d'Office 365, tels que Gmail, Yahoo et les comptes Microsoft, sont fédérés avec le portail OME, ce qui offre une meilleure expérience utilisateur pour ces destinataires. Toutes les autres identités utilisent un code d'accès unique pour accéder aux messages chiffrés.
- Les administrateurs peuvent personnaliser la personnalisation et créer plusieurs modèles de personnalisation.
- Les administrateurs peuvent révoquer les courriers chiffrés avec les nouvelles fonctionnalités.
- Les nouvelles fonctionnalités fournissent des rapports d'utilisation détaillés &amp; via le centre de sécurité conformité.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Coexistence de OME hérités et des nouvelles fonctionnalités dans le même client

Vous pouvez utiliser les OME hérités et les nouvelles fonctionnalités dans le même client. En tant qu'administrateur, vous pouvez choisir la version de OME que vous souhaitez utiliser lors de la création de vos règles de flux de messagerie.

- Pour spécifier la version héritée de OME, utilisez l'action de règle de flux de messagerie Exchange «appliquer la version précédente de OME».
- Pour spécifier les nouvelles fonctionnalités, utilisez l'action de règle de flux de messagerie Exchange «appliquer le chiffrement de messages et la protection des droits Office 365».

Les utilisateurs peuvent également envoyer des messages chiffrés avec les nouvelles fonctionnalités manuellement à partir d'Outlook Desktop, Outlook pour Mac et Outlook sur les clients Web.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>Migration de OME hérité vers les nouvelles fonctionnalités

Bien que les deux versions de OME puissent coexister, nous vous recommandons vivement de modifier vos anciennes règles de flux de messagerie qui utilisent l'action de règle «appliquer la version précédente de OME» pour utiliser les nouvelles fonctionnalités en spécifiant l'action de règle de flux de messagerie «appliquer le chiffrement de messages Office 365 et protection des droits. Pour obtenir des instructions, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="getting-started-with-ome"></a>Prise en main de OME

En règle générale, les nouvelles fonctionnalités OME sont automatiquement activées pour votre organisation Office 365. Si vous êtes prêt à commencer à utiliser les nouvelles fonctionnalités de OME au sein de votre organisation, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).

La version héritée de OME est automatiquement activée pour votre organisation Office 365 si vous avez activé Azure information protection. Auparavant, les OME hérités fonctionnaient même si Azure information protection n'était pas activé. Ce n'est plus le cas.

Pour commencer à utiliser les OME héritées, si vous avez activé Azure information protection, il vous suffit de configurer des règles de flux de messagerie qui utilisent l'action de règle «appliquer la version précédente de OME». Pour obtenir des instructions, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).