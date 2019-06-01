---
title: Vue d’ensemble des barrières de l’information
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez les barrières relatives aux informations pour garantir la conformité de la communication à l’aide de Microsoft teams au sein de votre organisation.
ms.openlocfilehash: e52a62ca0b80aed577be1978b81c8a01ac2371b9
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668292"
---
# <a name="information-barriers-preview"></a>Barrières des informations (aperçu)

Les services de Cloud Computing Microsoft incluent de puissantes fonctionnalités de communication et de collaboration. Mais supposons que vous souhaitiez restreindre les communications entre deux groupes afin d’éviter un conflit d’intérêts au sein de votre organisation. Vous pouvez aussi souhaiter restreindre les communications entre certaines personnes au sein de votre organisation afin de protéger les informations internes. Microsoft 365 permet la communication et la collaboration entre les groupes et les organisations, de sorte qu’y a-t-il un moyen de restreindre les communications entre des groupes d’utilisateurs spécifiques lorsque cela est nécessaire? Avec des barrières d’informations, vous pouvez le faire! 

Les barrières pour les informations sont maintenant en avant-première à partir de Microsoft Teams. Lorsque ces fonctionnalités sont disponibles pour votre organisation, un administrateur de conformité ou un administrateur des barrières de l’information peut définir des stratégies pour autoriser ou empêcher les communications entre les groupes d’utilisateurs dans Microsoft Teams. Les stratégies de barrière des informations peuvent être utilisées pour des situations comme celles-ci:

- Un commerçant en journée ne peut pas appeler une personne de l’équipe marketing
- Le personnel financier travaillant sur les informations confidentielles d’une société ne peut pas recevoir d’appels de certains groupes au sein de son organisation
- Une équipe interne avec des éléments secrets commerciaux ne peut pas appeler ou converser en ligne avec des personnes appartenant à certains groupes au sein de leur organisation.
- Une équipe de recherche peut uniquement appeler ou converser en ligne avec une équipe de développement de produit

Pour tous ces exemples de scénarios (et plus), des stratégies de barrière des informations peuvent être définies pour empêcher ou autoriser les communications dans Microsoft Teams. De telles stratégies peuvent empêcher les personnes d’appeler ou de converser avec celles qu’ils ne doivent pas utiliser, ou d’autoriser les utilisateurs à communiquer uniquement avec des groupes spécifiques dans Microsoft Teams. Avec des stratégies de barrière des informations en vigueur, chaque fois que des utilisateurs couverts par ces stratégies tentent de communiquer avec d’autres personnes dans Microsoft Teams, des vérifications sont effectuées pour empêcher (ou autoriser) la communication (comme défini par les stratégies de barrière des informations). 

> [!NOTE]
> Les barrières d’informations ne s’appliquent pas aux communications de messagerie ou au partage de fichiers via SharePoint Online ou OneDrive.

Les stratégies de barrière des informations s’appliquent aux types d’activités de communication suivants:

- Recherche d’un utilisateur
- Ajout d’un membre à une équipe
- Démarrage d’une session de conversation avec une personne
- Démarrage d’une conversation de groupe 
- Invitation d’une personne à participer à une réunion
- Partage d’un écran 
- Passer un appel

Si les personnes impliquées sont incluses dans une stratégie de barrière des informations qui empêche l’activité, elles ne pourront pas continuer. Pour en savoir plus sur l’expérience utilisateur avec des barrières d’informations, consultez la rubrique [barrières relatives aux informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

Actuellement, les stratégies de barrière des informations sont définies et gérées dans Office 365 à l’aide d’applets de commande PowerShell. Cette opération est généralement réalisée par un administrateur de conformité ou un administrateur global, et nécessite une bonne connaissance des applets de commande PowerShell (et des paramètres). Pour en savoir plus, consultez la rubrique [PowerShell (pour la définition des barrières relatives aux informations)](information-barriers-policies.md#powershell).

## <a name="required-licenses-and-permissions"></a>Licences et autorisations requises

**Actuellement, la fonctionnalité de barrière des informations est en**préversion privée. Lorsque ces fonctionnalités sont généralement disponibles, elles sont incluses dans les abonnements, par exemple:

- Microsoft 365 E5
- Office 365 E5
- Conformité avancée Office 365
- Microsoft 365 E5 protection des informations et conformité

Pour plus d’informations, consultez [la rubrique solutions de conformité](https://products.office.com/business/security-and-compliance/compliance-solutions).

Pour [définir ou modifier des stratégies de barrière des informations](information-barriers-policies.md), vous devez disposer de l’un des rôles suivants:

- Administrateur général Microsoft 365
- Administrateur général Office 365 
- Administrateur de conformité
- Administrateur des barrières de l’information

Vous devez être familiarisé avec les applets de commande PowerShell pour définir, valider ou modifier des stratégies de barrière des informations. Bien que nous fournissons plusieurs exemples d’applets de commande PowerShell dans les [procédures](information-barriers-policies.md), vous devez connaître les détails supplémentaires, tels que les paramètres, pour votre organisation.

## <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur les barrières d’informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [Voir les attributs pouvant être utilisés pour les stratégies de barrière des informations](information-barriers-attributes.md)
- [Définir des stratégies pour les barrières des informations](information-barriers-policies.md) 

