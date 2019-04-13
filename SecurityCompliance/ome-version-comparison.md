---
title: Comparaison des versions d'Office 365 message enCryption (OME)
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Explique les différences entre les fonctionnalités fournies avec les différentes versions d'Office 365 le chiffrement de messages et la façon dont les deux continuent de fonctionner ensemble.
ms.openlocfilehash: bb13208e2b630c8a6217b78b48a4cd3bb4b0de79
ms.sourcegitcommit: 895f67531f2b4afe46c7487ca5b44555ca791bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/12/2019
ms.locfileid: "31836838"
---
# <a name="compare-versions-of-ome"></a>Comparez les versions de OME

Cet article compare le chiffrement de messages Office 365 hérité (OME) aux nouvelles fonctionnalités OME. Les nouvelles fonctionnalités sont une fusion et une version plus récente de OME et de la gestion des droits relatifs à l'information (IRM). Les caractéristiques uniques du déploiement dans GCC High sont également décrites. Nous allons également découvrir comment les deux peuvent coexister dans votre organisation Office 365.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Comparaison côte à côte des fonctionnalités et des fonctionnalités

|                                   |Anciennes fonctionnalités       |                   |Fonctionnalités nouvelles              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Fonctionnalité**                     | **OME hérité**    | **IRM**           | **Nouvelles fonctionnalités OME** |
|*Envoi d'un message chiffré*        |À l'aide des règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook Desktop ou Outlook sur le Web; ou via les règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook Desktop, Outlook pour Mac ou Outlook sur le Web; via les règles de flux de messagerie Exchange (également appelées règles de transport) et la protection contre la perte de données (DLP) d'Office 365|
|*Modèle de gestion des droits*       |   S/O      |Option ne pas transférer et modèles personnalisés|Option ne pas transférer, option de chiffrement uniquement et modèles personnalisés|
|*Type de destinataire*                   |Destinataires internes et externes|Destinataires internes uniquement         |Destinataires internes et externes|
|*Expérience pour les destinataires internes*|Les destinataires reçoivent un message HTML, qu'ils téléchargent et ouvrent dans un navigateur Web ou une application mobile|Expérience incorporée native dans les clients Outlook|Expérience incorporée native pour les destinataires Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (pas de téléchargement ou d'application requis).|
|*Expérience pour les destinataires externes*|Les destinataires reçoivent un message HTML, qu'ils téléchargent et ouvrent dans un navigateur Web ou une application mobile|S/O|Expérience incorporée native pour les destinataires Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (pas de téléchargement ou d'application requis).|
|*Autorisations des pièces jointes*           |Aucune restriction sur les pièces jointes|Les pièces jointes sont protégées|Les pièces jointes sont protégées pour l'option ne pas transférer et les modèles personnalisés. Les administrateurs peuvent choisir de protéger ou non les pièces jointes pour l'option de chiffrement uniquement.|
|*Apporter votre propre prise en charge de la clé (BYOK)*|Aucune                |Aucune               |BYOK pris en charge          |
||

## <a name="advantages-of-the-new-ome-capabilities-over-legacy-ome"></a>Avantages des nouvelles fonctionnalités OME par rapport aux OME héritées

Les nouvelles fonctionnalités offrent les avantages suivants:

- Possibilité d'utiliser le chiffrement uniquement (ce qui permet une collaboration sécurisée), ne pas transférer et des restrictions personnalisées.
- Les expéditeurs peuvent envoyer des messages chiffrés avec les nouvelles fonctionnalités manuellement à partir d'Outlook Desktop, Outlook pour Mac et Outlook sur les clients Web.
- Les destinataires d'Office 365 peuvent utiliser une expérience en ligne dans les clients Outlook pris en charge. Par ailleurs, les administrateurs peuvent choisir d'afficher une expérience personnalisée pour les destinataires d'Office 365.
- Les comptes en dehors d'Office 365, tels que Gmail, Yahoo et les comptes Microsoft, sont fédérés avec le portail OME, ce qui offre une meilleure expérience utilisateur pour ces destinataires. Toutes les autres identités utilisent un code d'accès unique pour accéder aux messages chiffrés.
- Les administrateurs peuvent personnaliser la personnalisation et créer plusieurs modèles de personnalisation.
- Les administrateurs peuvent révoquer les courriers chiffrés avec les nouvelles fonctionnalités.
- Les nouvelles fonctionnalités fournissent des rapports d'utilisation détaillés &amp; via le centre de sécurité conformité.

## <a name="unique-characteristics-of-office-365-message-encryption-in-a-gcc-high-deployment"></a>Caractéristiques uniques d'Office 365 le chiffrement de messages dans un déploiement de GCC High

Si vous envisagez d'utiliser le chiffrement de messages Office 365 dans un environnement de GCC High, il existe certaines caractéristiques uniques concernant l'expérience utilisateur des destinataires.

### <a name="encrypted-email-from-gcc-high-to-gcc-high-recipients"></a>Messages chiffrés de GCC haut aux destinataires de GCC

Les expéditeurs peuvent chiffrer manuellement les courriers électroniques dans Outlook pour PC et Mac et Outlook sur le Web, ou les organisations peuvent configurer une stratégie pour chiffrer les messages électroniques à l'aide des règles de flux de messagerie Exchange.

Les destinataires à l'intérieur de GCC bénéficient de la même expérience de lecture incorporée dans Outlook pour PC et Mac et d'Outlook sur le Web que tous les autres utilisateurs d'Office 365.

### <a name="encrypted-email-from-gcc-high-to-non-gcc-high-recipients"></a>Courrier chiffré de GCC haut aux destinataires non GCC élevés

Les expéditeurs au sein de GCC High peuvent envoyer des messages chiffrés en dehors de la limite supérieure GCC.

Tous les destinataires en dehors de GCC High, y compris les utilisateurs d'Office 365 commerciaux, les utilisateurs Outlook.com, ainsi que d'autres utilisateurs d'autres fournisseurs de courrier, tels que Gmail et Yahoo, reçoivent un message de wrapper qui redirige le destinataire vers le portail OME où le destinataire est en mesure de lire et répondre à un message.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Coexistence de OME hérités et des nouvelles fonctionnalités dans le même client

Vous pouvez utiliser les OME hérités et les nouvelles fonctionnalités dans le même client. En tant qu'administrateur, vous pouvez choisir la version de OME que vous souhaitez utiliser lors de la création de vos règles de flux de messagerie.

- Pour spécifier la version héritée de OME, utilisez l'action de règle de flux de messagerie Exchange **appliquer la version précédente de OME**.
- Pour spécifier les nouvelles fonctionnalités, utilisez l'action de règle de flux de messagerie Exchange **appliquer le chiffrement de messages Office 365 et protection des droits**.

Les utilisateurs peuvent envoyer manuellement des messages chiffrés avec les nouvelles fonctionnalités depuis Outlook Desktop, Outlook pour Mac et Outlook sur le Web.

## <a name="migrate-from-legacy-ome-to-the-new-capabilities"></a>Migrer de OME hérité vers les nouvelles fonctionnalités

Bien que les deux versions de OME puissent coexister, nous vous recommandons vivement de modifier vos anciennes règles de flux de messagerie qui utilisent l'action de règle pour **appliquer la version précédente de OME** afin d'utiliser les nouvelles fonctionnalités. Mettre à jour ces règles pour utiliser l'action de règle de flux de messagerie **appliquer le chiffrement de messages Office 365 et la protection des droits**. Pour obtenir des instructions, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="get-started-with-ome"></a>Prise en main de OME

En règle générale, les nouvelles fonctionnalités OME sont automatiquement activées pour votre organisation Office 365. Pour plus d'informations sur les nouvelles fonctionnalités OME au sein de votre organisation, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).

La version héritée de OME est automatiquement activée pour votre organisation Office 365 si vous avez activé Azure information protection. Auparavant, les OME hérités fonctionnaient même si Azure information protection n'était pas activé. Ce n'est plus le cas.

Pour commencer à utiliser les OME héritées, si vous avez activé Azure information protection, configurez simplement les règles de flux de messagerie qui utilisent l'action **de règle applique la version précédente de OME**. Pour obtenir des instructions, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).