---
title: Vue d’ensemble des barrières de l’information
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez les barrières relatives aux informations pour garantir la conformité de la communication à l’aide de Microsoft teams au sein de votre organisation.
ms.openlocfilehash: e37c97ae8a5e3777e2a30432e8289abadae8f14c
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587043"
---
# <a name="information-barriers"></a>Barrières des informations

## <a name="overview"></a>Vue d’ensemble

Les services de Cloud Computing Microsoft incluent de puissantes fonctionnalités de communication et de collaboration. Mais supposons que vous souhaitiez restreindre les communications entre deux groupes afin d’éviter un conflit d’intérêts au sein de votre organisation. Vous pouvez aussi souhaiter restreindre les communications entre certaines personnes au sein de votre organisation afin de protéger les informations internes. Microsoft 365 permet la communication et la collaboration entre les groupes et les organisations, de sorte qu’y a-t-il un moyen de restreindre les communications entre des groupes d’utilisateurs spécifiques lorsque cela est nécessaire? Avec des barrières d’informations, vous pouvez le faire! 

Les barrières de l’information sont désormais déployées à partir de Microsoft Teams. Si votre [abonnement](#required-licenses-and-permissions) inclut des barrières d’informations, un administrateur de conformité ou un administrateur des barrières de l’information peut définir des stratégies pour autoriser ou empêcher les communications entre les groupes d’utilisateurs dans Microsoft Teams. Les stratégies de barrière des informations peuvent être utilisées pour des situations comme celles-ci:

- Un commerçant en journée ne peut pas appeler une personne de l’équipe marketing
- Le personnel financier travaillant sur les informations confidentielles d’une société ne peut pas recevoir d’appels de certains groupes au sein de son organisation
- Une équipe interne avec des éléments secrets commerciaux ne peut pas appeler ou converser en ligne avec des personnes appartenant à certains groupes au sein de leur organisation.
- Une équipe de recherche peut uniquement appeler ou converser en ligne avec une équipe de développement de produit

Pour tous ces exemples de scénarios (et plus), des stratégies de barrière des informations peuvent être définies pour empêcher ou autoriser les communications dans Microsoft Teams. De telles stratégies peuvent empêcher les personnes d’appeler ou de converser avec celles qu’ils ne doivent pas utiliser, ou d’autoriser les utilisateurs à communiquer uniquement avec des groupes spécifiques dans Microsoft Teams. Avec des stratégies de barrière des informations en vigueur, chaque fois que des utilisateurs couverts par ces stratégies tentent de communiquer avec d’autres personnes dans Microsoft Teams, des vérifications sont effectuées pour empêcher (ou autoriser) la communication (comme défini par les stratégies de barrière des informations). Pour en savoir plus sur l’expérience utilisateur avec des barrières d’informations, consultez la rubrique [barrières relatives aux informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

> [!IMPORTANT]
> Actuellement, les barrières de l’information ne s’appliquent pas aux communications de messagerie ou au partage de fichiers via SharePoint Online ou OneDrive. En outre, les barrières de l’information sont indépendantes des [limites de conformité](set-up-compliance-boundaries.md).<p>Avant de définir et d’appliquer des stratégies de barrière des informations, assurez-vous que votre organisation ne dispose pas des [stratégies de carnet d’adresses Exchange](https://docs.microsoft.com/en-us/exchange/address-books/address-book-policies/address-book-policies) en vigueur. (Les barrières d’informations sont basées sur les stratégies de carnet d’adresses.) 

## <a name="what-happens-with-information-barriers"></a>Qu’en est-il des barrières de l’information?

Lorsque des stratégies de barrière des informations sont en place, les personnes qui ne doivent pas communiquer avec d’autres utilisateurs spécifiques ne peuvent pas trouver, sélectionner, converser ou appeler ces utilisateurs. Avec des barrières d’informations, des vérifications sont en place pour empêcher toute communication non autorisée.

Initialement, les barrières relatives aux informations s’appliquent aux conversations et canaux Microsoft teams uniquement. Dans Microsoft Teams, les stratégies de barrière des informations déterminent et bloquent les types de communications non autorisés suivants:
- Recherche d’un utilisateur
- Ajout d’un membre à une équipe
- Démarrage d’une session de conversation avec une personne
- Démarrage d’une conversation de groupe
- Invitation d’une personne à participer à une réunion
- Partage d’un écran
- Passer un appel 

Si les personnes impliquées sont incluses dans une stratégie de barrière des informations pour empêcher l’activité, elles ne pourront pas continuer. En outre, il est possible que tout le monde inclus dans une stratégie de barrière des informations ne puisse pas communiquer avec d’autres personnes dans Microsoft Teams. Lorsque les personnes affectées par les stratégies de barrière des informations font partie de la même conversation de groupe ou d’équipe, elles peuvent être supprimées de ces sessions de conversation et il se peut que la communication avec le groupe ne soit pas autorisée.

Pour en savoir plus sur l’expérience utilisateur avec des barrières d’informations, consultez la rubrique [barrières relatives aux informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

## <a name="required-licenses-and-permissions"></a>Licences et autorisations requises

Les barrières de l’information se dérouleront maintenant et sont incluses dans les abonnements, telles que:

- Microsoft 365 E5
- Office 365 E5
- Conformité avancée Office 365
- Microsoft 365 E5 protection des informations et conformité

Pour plus d’informations, consultez [la rubrique solutions de conformité](https://products.office.com/business/security-and-compliance/compliance-solutions).

Pour [définir ou modifier des stratégies de barrière des informations](information-barriers-policies.md), vous devez disposer de l’un des rôles suivants:

- Administrateur général Microsoft 365
- Administrateur général Office 365 
- Administrateur de conformité
- IB gestion de la conformité (il s’agit d’un nouveau rôle!)

(Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de conformité des & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md).)

Vous devez être familiarisé avec les applets de commande PowerShell pour définir, valider ou modifier des stratégies de barrière des informations. Bien que nous fournissons plusieurs exemples d’applets de commande PowerShell dans l' [article de procédure](information-barriers-policies.md), vous devez connaître les détails supplémentaires, tels que les paramètres, pour votre organisation.

## <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur les barrières d’informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

- [Voir les attributs pouvant être utilisés pour les stratégies de barrière des informations](information-barriers-attributes.md)

- [Définir des stratégies pour les barrières des informations](information-barriers-policies.md)

- [Modifier (ou supprimer) des stratégies de barrière des informations](information-barriers-edit-segments-policies.md.md) 

