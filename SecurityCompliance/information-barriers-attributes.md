---
title: Attributs des stratégies de barrière des informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/28/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez cet article comme référence pour différents attributs que vous pouvez utiliser dans les stratégies de barrière des informations.
ms.openlocfilehash: 1537dae2c99555a9257bbe5c3f9754a1f975fbbe
ms.sourcegitcommit: 8f399f260687d17a497a15bcc644187c277ea8fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2019
ms.locfileid: "35462405"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Attributs des stratégies de barrière des informations (aperçu)

Certains attributs d’Azure Active Directory peuvent être utilisés pour segmenter les utilisateurs. Une fois les segments définis, ces segments peuvent être utilisés comme filtres pour les stratégies de barrière des informations. Par exemple, vous pouvez utiliser **Department** pour définir des segments d’utilisateurs par service au sein de votre organisation (en supposant qu’aucun employé ne travaille pour deux départements en même temps). 

Cet article explique comment utiliser des attributs avec des barrières d’informations et fournit une liste des attributs qui peuvent être utilisés. Pour en savoir plus sur les barrières d’informations, consultez les ressources suivantes:
- [Barrières des informations (aperçu)](information-barriers.md)
- [Définir des stratégies pour les barrières d’informations dans Microsoft Teams (aperçu)](information-barriers-policies.md)
- [Modifier (ou supprimer) des stratégies de barrière des informations (aperçu)](information-barriers-edit-segments-policies.md.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Comment utiliser les attributs dans les stratégies de barrière des informations

Les attributs mentionnés dans cet article peuvent être utilisés pour définir ou modifier des segments d’utilisateurs. Vos segments définis servent de paramètres (appelés valeurs *UserGroupFilter* ) dans les [stratégies de barrière des informations](information-barriers-policies.md).

1. Déterminez l’attribut que vous souhaitez utiliser pour définir des segments. (Reportez-vous à la section [référence](#reference) de cet article.)

2. Assurez-vous que les valeurs des comptes d’utilisateur sont renseignées pour les attributs sélectionnés à l’étape 1. Affichez les détails du compte d’utilisateur et, si nécessaire, modifiez les comptes d’utilisateur pour inclure les valeurs d’attribut. 

    - Pour modifier plusieurs comptes (ou utiliser PowerShell pour modifier un seul compte), voir [configure User Account Properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).

    - Pour modifier un seul compte, voir [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).

3. [Définissez des segments à l’aide de PowerShell](information-barriers-policies.md#define-segments-using-powershell), comme dans les exemples suivants:

    |Exemple  |Applet de commande  |
    |---------|---------|
    |Définition d’un segment nommé Segment1 à l’aide de l’attribut Department     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
    |Définissez un segment appelé Segmenta à l’aide de l’attribut MemberOf (Supposons que cet attribut contient des noms de groupe, par exemple «BlueGroup»).     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
    |Définissez un segment appelé DayTraders à l’aide de ExtensionAttribute1 (Supposons que cet attribut contient des fonctions, telles que «DayTrader»).|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

    > [!TIP]
    > Lorsque vous définissez des segments, utilisez le même attribut pour tous vos segments. Par exemple, si vous définissez des segments à l’aide de *Department*, définissez tous les segments à l’aide de *Department*. Ne définissez pas de segments à l’aide de *Department* et d’autres à l’aide de *memberOf*. Assurez-vous que vos segments ne se chevauchent pas; chaque utilisateur doit être affecté à un seul segment. 

## <a name="reference"></a>Référence

Le tableau suivant répertorie les attributs que vous pouvez utiliser avec les barrières d’informations.

|Nom de la propriété Azure Active Directory<br/>(Nom complet LDAP)  |Nom de la propriété Exchange  |
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



