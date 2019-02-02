---
title: Comparaison des versions de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Explique les différences dans les fonctionnalités fournies avec différentes versions d’Office 365 Message Encryption ainsi que la manière dont les deux continuent à travailler ensemble.
ms.openlocfilehash: a418d840c7e0eb50ae076bf2b03164bef9488058
ms.sourcegitcommit: 88f3982217c29b558e3f9e838bcb425da395dd5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2019
ms.locfileid: "29708541"
---
# <a name="compare-versions-of-ome"></a>Comparer les versions d’OME

Cet article compare hérité chiffrement de messages Office 365 pour les nouvelles fonctionnalités d’OME. Les nouvelles fonctionnalités sont une fusion et une version plus récente de l’Information Rights Management (IRM) et OME. Nous allons également aborder comment les deux peuvent coexister au sein de votre organisation Office 365.

||
|:-----|
|Cet article fait partie d’une plus grande série d’articles sur Office 365 Message Encryption. Cet article est destiné aux administrateurs et les professionnels de l’informatique. Si vous êtes simplement vous recherchez des informations sur l’envoi ou la réception d’un message chiffré, vous trouverez la liste des articles inclus dans [Office 365 Message Encryption (OME)](ome.md) et recherchez l’article qui vous convient le mieux à vos besoins. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>Comparaison côte à côte des fonctionnalités et des capacités

|                                   |Anciens composants fonctionnels       |                   |Fonctionnalités nouvelles              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**Fonctionnalité**                     | **OME hérité**    | **IRM**           | **Nouvelles fonctionnalités de OME** |
|*Envoyer un message chiffré*        |Par le biais de règles de flux de messagerie Exchange|Utilisateur final initiée à partir du bureau Outlook ou Outlook sur le Web ; ou Exchange par le biais de règles de flux de messagerie.|Utilisateur final initiée à partir du bureau Outlook, Outlook pour Mac ou Outlook sur le Web ; par le biais de règles de Transport Exchange et Office 365 Data Loss Prevention (DLP)|
|*Modèle de gestion des droits*       |   S/O      |Effectuez l’option pas transférer et modèles personnalisés|Option pas transférer, option chiffrer uniquement, et de modèles personnalisés|
|*Type de destinataire*                   |Destinataires internes et externes|Destinataires internes         |Destinataires internes et externes|
|*Expérience pour un destinataire interne*|Destinataires reçoivent un message HTML, qu’ils téléchargent et ouvrent dans un navigateur web ou d’une application mobile|Expérience native insérée dans les clients Outlook|Expérience inline natif pour les destinataires d’Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (aucun téléchargement ou application requis).|
|*Expérience des destinataires externes*|Destinataires reçoivent un message HTML, qu’ils téléchargent et ouvrent dans un navigateur web ou d’une application mobile|S/O|Expérience inline natif pour les destinataires d’Office 365. Tous les autres destinataires peuvent lire le message à partir du portail OME (aucun téléchargement ou application requis).|
|*Autorisations de pièces jointes*           |Aucune restriction sur les pièces jointes|Pièces jointes sont protégées.|Pièces jointes sont protégées pour l’option ne pas transférer les modèles personnalisés. Administrateurs peuvent choisir si les pièces jointes pour l’option chiffrer uniquement sont protégées ou non.|
|*Intégrez vos propres prise en charge de la clé (BYOK)*|Aucun                |Aucun               |BYOK pris en charge          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>Avantages de l’utilisation des nouvelles fonctionnalités OME sur OME hérité

Les nouvelles fonctionnalités offrent les avantages suivants :

- Possibilité d’utiliser chiffrer uniquement (ce qui permet une collaboration sécurisée), ne pas transférer, ainsi que les restrictions personnalisées.
- Les expéditeurs peuvent envoyer des messages chiffrés avec les nouvelles fonctionnalités manuellement à partir du bureau d’Outlook, Outlook pour Mac et Outlook sur les clients web.
- Obtenir des destinataires d’Office 365 utiliser une expérience en ligne dans les clients Outlook pris en charge. Autrement, administrateurs peuvent choisir d’afficher destinataires Office 365 une expérience personnalisée.
- Comptes en dehors d’Office 365, tels que des comptes Gmail, Yahoo! et Microsoft, sont fédérés avec le portail OME, qui fournit une meilleure expérience utilisateur pour ces destinataires. Tous les autres identités utilisent un code secret unique pour accéder aux messages chiffrés.
- Administrateurs peuvent personnaliser le marquage et créer plusieurs modèles de personnalisation.
- Administrateurs peuvent révoquer des messages électroniques chiffrés avec les nouvelles fonctionnalités.
- Les nouvelles fonctionnalités de fournissent des rapports d’utilisation détaillés par le biais de la sécurité &amp; centre de conformité.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>Coexistence d’OME hérité et les nouvelles fonctionnalités dans le même client

Vous pouvez utiliser à la fois OME hérité et les nouvelles fonctionnalités dans le même client. En tant qu’administrateur, cela en choisissant quelle version d’OME à utiliser lors de la création des règles de flux de votre messagerie.

- Pour spécifier la version héritée de OME, utilisez l’action de règle flux de la messagerie Exchange « Appliquer la version précédente d’OME ».
- Pour spécifier les nouvelles fonctionnalités, utilisez l’Exchange messagerie flux règle action « Appliquer Office 365 Message chiffrement et les droits de protection ».

Les utilisateurs peuvent également envoyer des messages chiffré avec les nouvelles fonctionnalités manuellement à partir du bureau d’Outlook, Outlook pour Mac et Outlook sur les clients web.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>Migration de OME hérité vers les nouvelles fonctionnalités

Même si les deux versions d’OME peuvent coexister, il est fortement recommandé que modifier votre anciennes règles de flux de messagerie qui utilisent l’action de règle « Appliquer la version précédente d’OME » pour utiliser les nouvelles fonctionnalités en spécifiant l’action de règle de flux de messagerie « s’appliquent Office 365 Message Encryption et de protection des droits ». Pour plus d’informations, voir [définir les règles de flux des messages pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

## <a name="getting-started-with-ome"></a>Mise en route avec OME

En règle générale, les nouvelles fonctionnalités OME sont automatiquement activées pour votre organisation Office 365. Si vous êtes prêt à commencer à utiliser les nouvelles fonctionnalités OME au sein de votre organisation, consultez [configurer des nouvelles fonctionnalités d’Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).

La version héritée de OME est automatiquement activée pour votre organisation Office 365 si vous avez activé la Protection des informations Azure. Dans le passé, OME hérité fonctionne même si la Protection des informations Azure n’a pas été activée. Il n’est plus le cas.

Pour commencer à utiliser OME hérité, si vous avez activé la Protection des informations Azure, il vous souhaitez est de configurer les règles de flux de messagerie qui utilisent l’action de règle « Appliquer la version précédente d’OME ». Pour plus d’informations, voir [définir les règles de flux des messages pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).