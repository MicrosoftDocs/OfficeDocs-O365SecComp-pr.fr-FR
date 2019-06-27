---
title: Vue d’ensemble des barrières de l’information
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/26/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez les barrières relatives aux informations pour garantir la conformité de la communication à l’aide de Microsoft teams au sein de votre organisation.
ms.openlocfilehash: 6565fc28d70ac6ff9a6f4df6edc75b89d19ae29a
ms.sourcegitcommit: 1c254108c522d0cb44023565268b5041d07748aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/27/2019
ms.locfileid: "35279472"
---
# <a name="information-barriers-preview"></a>Barrières des informations (aperçu)

## <a name="overview"></a>Vue d’ensemble

Les services de Cloud Computing Microsoft incluent de puissantes fonctionnalités de communication et de collaboration. Mais supposons que vous souhaitiez restreindre les communications entre deux groupes afin d’éviter un conflit d’intérêts au sein de votre organisation. Vous pouvez aussi souhaiter restreindre les communications entre certaines personnes au sein de votre organisation afin de protéger les informations internes. Microsoft 365 permet la communication et la collaboration entre les groupes et les organisations, de sorte qu’y a-t-il un moyen de restreindre les communications entre des groupes d’utilisateurs spécifiques lorsque cela est nécessaire? Avec des barrières d’informations, vous pouvez le faire! 

Les barrières pour les informations sont maintenant en avant-première à partir de Microsoft Teams. Lorsque ces fonctionnalités sont disponibles pour votre organisation, un administrateur de conformité ou un administrateur des barrières de l’information peut définir des stratégies pour autoriser ou empêcher les communications entre les groupes d’utilisateurs dans Microsoft Teams. Les stratégies de barrière des informations peuvent être utilisées pour des situations comme celles-ci:

- Un commerçant en journée ne peut pas appeler une personne de l’équipe marketing
- Le personnel financier travaillant sur les informations confidentielles d’une société ne peut pas recevoir d’appels de certains groupes au sein de son organisation
- Une équipe interne avec des éléments secrets commerciaux ne peut pas appeler ou converser en ligne avec des personnes appartenant à certains groupes au sein de leur organisation.
- Une équipe de recherche peut uniquement appeler ou converser en ligne avec une équipe de développement de produit

Pour tous ces exemples de scénarios (et plus), des stratégies de barrière des informations peuvent être définies pour empêcher ou autoriser les communications dans Microsoft Teams. De telles stratégies peuvent empêcher les personnes d’appeler ou de converser avec celles qu’ils ne doivent pas utiliser, ou d’autoriser les utilisateurs à communiquer uniquement avec des groupes spécifiques dans Microsoft Teams. Avec des stratégies de barrière des informations en vigueur, chaque fois que des utilisateurs couverts par ces stratégies tentent de communiquer avec d’autres personnes dans Microsoft Teams, des vérifications sont effectuées pour empêcher (ou autoriser) la communication (comme défini par les stratégies de barrière des informations). Pour en savoir plus sur l’expérience utilisateur avec des barrières d’informations, consultez la rubrique [barrières relatives aux informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).

> [!NOTE]
> Les barrières d’informations ne s’appliquent pas aux communications de messagerie ou au partage de fichiers via SharePoint Online ou OneDrive. En outre, les barrières de l’information sont indépendantes des [limites de conformité](set-up-compliance-boundaries.md).

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

## <a name="concepts-of-information-barrier-policies"></a>Concepts des stratégies de barrière des informations

Il est utile de savoir quels sont les concepts sous-jacents des stratégies de barrière des informations:

- Les **attributs de compte d’utilisateur** sont définis dans Azure Active Directory (ou Exchange Online). Ces attributs peuvent inclure le service, la fonction, l’emplacement, le nom de l’équipe et d’autres détails du profil de travail. 

- Les **segments** sont des ensembles d’utilisateurs définis dans le centre de conformité & la sécurité d’Office 365 à l’aide d’un **attribut de compte d’utilisateur**sélectionné. (Reportez-vous à la [liste des attributs pris en charge](information-barriers-attributes.md).) 

- Les **stratégies de barrière des informations** déterminent les limites ou restrictions de communication. Lorsque vous définissez des stratégies de barrière des informations, vous avez le choix entre deux types de stratégies:
    - Les stratégies «bloquer» empêchent un segment de communiquer avec un autre segment.
    - Les stratégies «autoriser» permettent à un segment de communiquer avec certains autres segments seulement.

- Une **application de stratégie** est exécutée une fois toutes les stratégies de barrière des informations définies et vous êtes prêt à les appliquer dans votre organisation.

## <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur les barrières d’informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [Voir les attributs pouvant être utilisés pour les stratégies de barrière des informations](information-barriers-attributes.md)
- [Définir des stratégies pour les barrières des informations](information-barriers-policies.md) 

