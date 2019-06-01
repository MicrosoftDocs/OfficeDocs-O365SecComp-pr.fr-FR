---
title: Attributs des stratégies de barrière des informations
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
description: Utilisez cet article comme référence pour différents attributs que vous pouvez utiliser dans les stratégies de barrière des informations.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668296"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Attributs des stratégies de barrière des informations (aperçu)

Certains attributs d’Azure Active Directory peuvent être utilisés pour segmenter les utilisateurs. Les segments sont ensuite utilisés comme filtres pour les stratégies de barrière des informations. Par exemple, vous pouvez utiliser **Department** pour définir des segments d’utilisateurs par service au sein de votre organisation (en supposant qu’aucun employé ne travaille pour deux départements en même temps). 

Cet article fournit une liste d’attributs qui peuvent être utilisés. Pour en savoir plus sur les barrières d’informations, consultez les ressources suivantes:
- [Barrières des informations (aperçu)](information-barriers.md)
- [Définir des stratégies pour les barrières d’informations dans Microsoft Teams (aperçu)](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Comment utiliser les attributs dans les stratégies de barrière des informations

Les attributs mentionnés dans cet article peuvent être utilisés pour définir (ou modifier) des segments d’utilisateurs. Les segments sont utilisés comme paramètres (UserGroupFilter) dans les stratégies de barrière des informations, comme illustré dans les exemples suivants:

|Exemple  |Applet de commande  |
|---------|---------|
|Définition d’un segment nommé Segment1 à l’aide de l’attribut Department     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|Définissez un segment appelé Segmenta à l’aide de l’attribut MemberOf (Supposons que cet attribut contient des noms de groupe, par exemple «BlueGroup»).     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|Définissez un segment appelé DayTraders à l’aide de ExtensionAttribute1 (Supposons que cet attribut contient des fonctions, telles que «DayTrader»).|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

Lorsque vous définissez des segments, utilisez le même attribut pour tous vos segments. Par exemple, si vous définissez des segments à l’aide de *Department*, définissez tous les segments à l’aide de *Department*. Ne définissez pas de segments à l’aide de *Department* et d’autres à l’aide de *memberOf*. Assurez-vous que vos segments ne se chevauchent pas; chaque utilisateur doit être affecté à un seul segment. 

Pour en savoir plus, consultez la rubrique [define segments using PowerShell](information-barriers-policies.md#define-segments-using-powershell).

## <a name="reference"></a>Référence

Le tableau suivant répertorie les attributs que vous pouvez utiliser avec les barrières d’informations.

|Nom de la propriété Azure Active Directory (nom complet LDAP)  |Nom de la propriété Exchange  |
|---------|---------|
|Processeur       | Processeur        |
|Company     |Company         |
|Service     |Service         |
|ExtensionAttribute1 |CustomAttribute1  |
|ExtensionAttribute2 |CustomAttribute2  |
|ExtensionAttribute3 |CustomAttribute3  |
|ExtensionAttribute4 |CustomAttribute4  |
|ExtensionAttribute5 |CustomAttribute5  |
|ExtensionAttribute6 |CustomAttribute6  |
|ExtensionAttribute7 |CustomAttribute7  |
|ExtensionAttribute8 |CustomAttribute8  |
|ExtensionAttribute9 |CustomAttribute9  |
|ExtensionAttribute10 |CustomAttribute10  |
|ExtensionAttribute11 |CustomAttribute11  |
|ExtensionAttribute12 |CustomAttribute12  |
|ExtensionAttribute13 |CustomAttribute13  |
|ExtensionAttribute14 |CustomAttribute14  |
|ExtensionAttribute15 |CustomAttribute15  |
|MSExchExtensionCustomAttribute1 |ExtensionCustomAttribute1 |
|MSExchExtensionCustomAttribute2 |ExtensionCustomAttribute2 |
|MSExchExtensionCustomAttribute3 |ExtensionCustomAttribute3 |
|MSExchExtensionCustomAttribute4 |ExtensionCustomAttribute4 |
|MSExchExtensionCustomAttribute5 |ExtensionCustomAttribute5 |
|MailNickname |Alias |
|PhysicalDeliveryOfficeName |Office |
|PostalCode |PostalCode |
|ProxyAddresses |EmailAddresses |
|StreetAddress |StreetAddress |
|TargetAddress |ExternalEmailAddress |
|UsageLocation |UsageLocation |
|UserPrincipalName  |UserPrincipalName  |
|Courrier Outlook   |WindowsEmailAddress    |
|Description    |Description    |
|MemberOf   |MemberOfGroup  |

## <a name="related-topics"></a>Sujets associés

[Définir des stratégies pour les barrières d’informations dans Microsoft Teams (aperçu)](information-barriers-policies.md)

[Dépannage des barrières relatives aux informations (aperçu)](information-barriers-troubleshooting.md)

[Barrières des informations (aperçu)](information-barriers.md)



