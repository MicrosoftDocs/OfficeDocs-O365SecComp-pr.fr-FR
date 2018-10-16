---
title: Comment identifier le type de conservation placé sur une boîte aux lettres Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Découvrez comment identifier les différents types d’attente qui peuvent être placées sur une boîte aux lettres Office 365. Ces types de suspensions incluent litige, suspensions eDiscovery et des stratégies de rétention Office 365. Vous pouvez également déterminer si un utilisateur a été exclu d’une stratégie de rétention de l’entreprise
ms.openlocfilehash: 821ec2a8be9ecd89a13ad9ad0378bc6e24fcee1e
ms.sourcegitcommit: b164d4af65709133e0b512a4327a70fae13a974d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25577073"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Comment identifier le type de conservation placé sur une boîte aux lettres Exchange Online

Cet article explique comment identifier les suspensions placées sur les boîtes aux lettres Exchange Online dans Office 365.

Office 365 offre plusieurs manières dont votre organisation peut empêcher le contenu de la boîte aux lettres d’être définitivement supprimé. Cela permet à votre organisation conserver le contenu pour répondre aux élèves en conformité ou pendant la durée du département juridique ou d’autres types d’enquêtes. Voici une liste des fonctionnalités de rétention (également appelée *contient*) dans Office 365 :

- **Litige** - suspensions appliquées aux boîtes aux lettres dans Exchange Online.

- **maintenez la touche e-Discovery** - suspensions qui sont associés à un cas de découverte électronique dans la sécurité et le centre de conformité. SUSPENSIONS eDiscovery peuvent être appliquées aux boîtes aux lettres utilisateur et dans la boîte aux lettres pour les groupes d’Office 365 et Microsoft Teams.

- **In-Place Hold** - suspensions appliquées aux boîtes aux lettres de l’utilisateur à l’aide de la recherche de découverte électronique & outil blocage dans Exchange admin center dans Exchange Online.

- **Stratégie de rétention office 365** - conserve le contenu dans les boîtes aux lettres dans Exchange Online et dans la boîte aux lettres pour les groupes d’Office 365 et Microsoft Teams. Vous pouvez créer une rétention stratégie conserve Skype pour des Conversations, qui sont stockés dans les boîtes aux lettres utilisateur.

  Il existe deux types de stratégies de rétention Office 365 qui peuvent être affectés aux boîtes aux lettres.

    - **Stratégies de rétention emplacement spécifique** : il s’agit de stratégies attribuées pour les emplacements de contenu d’utilisateurs spécifiques. L’applet de commande **Get-Mailbox** dans Exchange Online PowerShell vous permet d’obtenir des informations sur les stratégies de rétention affectés à des boîtes aux lettres spécifiques.

    - **Stratégies de rétention de l’entreprise** : il s’agit de stratégies qui sont affectés à tous les emplacements de contenu dans votre organisation. L’applet de commande **Get-OrganizationConfig** dans Exchange Online PowerShell vous permet d’obtenir des informations sur les stratégies de rétention de l’entreprise. Pour plus d’informations, voir la section « Application d’une stratégie de rétention à un ensemble de l’organisation ou des sites spécifiques » dans [les stratégies de rétention de vue d’ensemble d’Office 365](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Étiquettes de office 365** - si un utilisateur s’applique une étiquette d’Office 365 (celui qui est configuré pour conserver le contenu ou conserver et puis supprimer le contenu) à *tout* dossier ou un élément dans leur boîte aux lettres, une suspension est placé sur la boîte aux lettres comme si la boîte aux lettres a été mis en cas de litige Blocage ou affectés à une stratégie de rétention d’Office 365. Pour plus d’informations, voir la section [identification boîtes aux lettres sur une suspension, car une étiquette a été appliquée à un dossier ou un élément](#identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item) dans cet article.

Pour gérer les boîtes aux lettres en attente, vous devrez peut-être identifier le type de suspension est placé dans une boîte aux lettres afin que vous pouvez effectuer des tâches telles que la modification de la durée d’attente, titre temporaire ou permanent suppression de la suspension ou à l’exception d’une boîte aux lettres à partir d’une stratégie de rétention d’Office 365. Dans ce cas, la première étape consiste à identifier le type de suspension placé dans la boîte aux lettres. Et parce que plusieurs suspensions (et les différents types de suspensions) peuvent être placées sur une seule boîte aux lettres, vous devez identifier toutes les suspensions placées sur une boîte aux lettres si vous voulez supprimer ou modifier ces suspensions.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Étape 1 : Obtenir le GUID de suspensions placées sur une boîte aux lettres

Vous pouvez exécuter les deux applets de commande suivantes dans Exchange Online PowerShell pour obtenir le GUID de la suspension sont placés dans une boîte aux lettres. Après avoir obtenu un GUID, vous l’utilisez pour identifier la suspension spécifique à l’étape 2. Notez que pour litige contient ne sont pas identifiés par un GUID. Blocage pour litige est activés ou désactivés pour une boîte aux lettres.

- **Get-Mailbox** - Utilisez cette applet de commande pour déterminer si le litige est activé pour une boîte aux lettres et pour obtenir les GUID pour la découverte électronique conserve, archives permanentes et les stratégies de rétention Office 365 spécifiquement attribuées à une boîte aux lettres. Le résultat de cette applet de commande indique également si une boîte aux lettres a été explicitement exclu une stratégie de rétention de l’entreprise.

- **Get-OrganizationConfig** - Utilisez cette applet de commande pour obtenir les identificateurs GUID des stratégies de rétention de l’entreprise.

Pour vous connecter à Exchange Online PowerShell, voir [se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Exécutez la commande suivante pour obtenir des informations sur les suspensions appliquées à une boîte aux lettres de stratégies de rétention Office 365.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> S’il existe trop grand nombre de valeurs dans la propriété InPlaceHolds et tous les s’affichent, vous pouvez exécuter la `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque GUID sur une ligne distincte.

Le tableau suivant décrit comment identifier les différents types de suspensions en fonction des valeurs dans la propriété *InPlaceHolds* lorsque vous exécutez l’applet de commande **Get-Mailbox** .


|Type de conservation  |Exemple de valeur  |Comment identifier la suspension  |
|---------|---------|---------|
|Conservation pour litige     |    `True`     |     Blocage pour litige est activé pour une boîte aux lettres si la propriété *LitigationHoldEnabled* est définie sur `True`.    |
|blocage eDiscovery     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   La *propriété InPlaceHolds* contient le GUID de n’importe quel suspension associé à un cas de découverte électronique dans la sécurité et le centre de conformité. Vous pouvez indiquer il s’agit d’un blocage eDiscovery, car le GUID commence par la `UniH` préfixe (ce qui indique une attente unifiée).      |
|Blocage local     |     `c0ba3ce811b6432a8751430937152491` <br/> ou <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     La propriété *InPlaceHolds* contient le GUID de la conservation inaltérable qui est placé sur la boîte aux lettres. Vous pouvez indiquer il s’agit d’une conservation inaltérable, car le GUID ne soit commence par un préfixe ou il commence par la `cld` préfixe.     |
|Office 365 stratégie de rétention spécifiquement la boîte aux lettres     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> ou <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     La propriété InPlaceHolds contient le GUID de la stratégie de rétention n’importe quel emplacement spécifique qui est appliqué à la boîte aux lettres. Vous pouvez identifier les stratégies de rétention, car le GUID commence par la `mbx` ou `skp` préfixe. Le `skp` préfixe indique que la stratégie de rétention est appliquée aux Skype pour des conversations dans la boîte aux lettres de l’utilisateur.    |
|Exclus d’une stratégie de rétention à l’échelle de l’organisation Office 365     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Si une boîte aux lettres est exclu d’une stratégie de rétention à l’échelle de l’organisation Office 365, le GUID de la stratégie de rétention est exclu de la boîte aux lettres est affiché dans la propriété InPlaceHolds et identifié par le `-mbx` préfixe.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Si la propriété *InPlaceHolds* est vide lorsque vous exécutez l’applet de commande **Get-Mailbox** , toujours il peut y avoir au moins une échelle de l’organisation Office 365 de rétention appliquée à la boîte aux lettres. Exécutez la commande suivante dans Exchange Online PowerShell pour obtenir une liste de GUID pour les stratégies de rétention d’Office 365 à l’échelle de l’organisation.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> S’il existe trop grand nombre de valeurs dans la propriété InPlaceHolds et tous les s’affichent, vous pouvez exécuter la `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque GUID sur une ligne distincte.

Le tableau suivant décrit les différents types de suspensions d’échelle de l’organisation et comment identifier chaque type basé sur les GUID contenus dans la propriété *InPlaceHolds* lorsque vous exécutez l’applet de commande **Get-OrganizationConfig** .


|Type de conservation  |Exemple de valeur  |Description  |
|---------|---------|---------|
|Stratégies de rétention 365 Office appliqué aux boîtes aux lettres Exchange, les dossiers publics Exchange et les équipes salles de conversation    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Stratégies de rétention de l’entreprise appliquent aux boîtes aux lettres Exchange, des dossiers publics Exchange, et 1xN conversations dans Microsoft Teams sont identifiées par le GUID qui commencent par la `mbx` préfixe. Notez que les conversations 1xN sont stockées dans la boîte aux lettres de participants à la conversation individuelles.      |
|Office 365 stratégie de rétention des messages canal Office 365 groupes et les équipes     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Échelle de l’organisation de rétention appliquée aux groupes de Office 365 et les messages de canal dans Microsoft Teams est identifiées par le GUID qui commencent par la `grp` préfixe. Notez que les messages de canal sont stockés dans la boîte aux lettres de groupe qui est associé à un Team Microsoft.     |

Pour plus d’informations de rétention appliquée à Microsoft Teams, consultez la section « Emplacement des équipes » [vue d’ensemble des stratégies de rétention](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Présentation du format de la valeur de InPlaceHolds de stratégies de rétention

Outre le préfixe (mbx, skp ou groupe) qui identifie un élément dans la propriété InPlaceHolds comme une stratégie de rétention Office 365, la valeur contient également un suffixe qui identifie le type d’action de rétention est configuré pour la stratégie. Par exemple, le suffixe de l’action est mise en surbrillance en gras dans les exemples suivants :

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

Le tableau suivant définit les trois actions de rétention possibles :

|Valeur  |Description  |
|---------|---------|
|**1**     | Indique la stratégie de rétention est configurée pour supprimer des éléments ; la stratégie ne conserve des éléments.        |
|**2**    |    Indique la stratégie de rétention est configurée pour contenir les éléments ; la stratégie ne supprime pas les éléments après l’expiration de la période de rétention.     |
|**3**     |   Indique la stratégie de rétention est configurée pour contenir les éléments et les supprimer après expiration de la période de rétention.      |

Pour plus d’informations sur les actions de rétention, voir la section « Soutènement de contenu pour une période spécifique » dans la [vue d’ensemble des stratégies de rétention](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Étape 2 : Utiliser le GUID pour identifier la suspension

Après avoir obtenu le GUID d’une suspension est appliquée à une boîte aux lettres, l’étape suivante consiste à utiliser ce GUID pour identifier la suspension. Les sections suivantes montrent comment identifier le nom de la mise en attente (et autres informations) à l’aide de la suspension GUID.

### <a name="ediscovery-holds"></a>SUSPENSIONS eDiscovery

Exécutez les commandes suivantes dans PowerShell du centre de conformité et de sécurité pour identifier un blocage eDiscovery qui est appliqué à la boîte aux lettres. Utiliser le GUID (notamment le préfixe UniH) pour la découverte électronique en attente que vous avez identifié à l’étape 1. La première commande crée une variable qui contient des informations sur la suspension ; Cette variable est utilisée dans les autres commandes. La deuxième commande affiche le nom du cas eDiscovery qu'est associée à la suspension. La troisième commande affiche le nom de la suspension et une liste des boîtes aux lettres à que la suspension s’applique.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Pour vous connecter à PowerShell du centre de conformité et de sécurité, voir [se connecter à Office 365 sécurité & PowerShell du centre de conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>Archives permanentes

Exécutez la commande suivante dans Exchange Online PowerShell pour identifier la In-Place Hold qui est appliqué à la boîte aux lettres. Utilisez le GUID pour la conservation inaltérable que vous avez identifié à l’étape 1. La commande affiche le nom de la suspension et une liste des boîtes aux lettres à que la suspension s’applique.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Notez que si le GUID pour la conservation inaltérable commence par la `cld` prefix, veillez à inclure le préfixe lors de l’exécution de la commande précédente.

### <a name="office-365-retention-policies"></a>Stratégies de rétention Office 365

Exécutez la commande suivante dans PowerShell du centre de conformité et de sécurité pour l’identité de la stratégie de rétention d’Office 365 (emplacement spécifique ou à l’échelle de l’organisation) qui est appliquée à la boîte aux lettres. Utilisez le GUID (notamment le préfixe mbx, skp ou groupe ou le suffixe d’action) que vous avez identifié à l’étape 1.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-label-has-been-applied-to-a-folder-or-item"></a>Identifier les boîtes aux lettres sur stocker, car une étiquette a été appliquée à un dossier ou un élément

Chaque fois qu’un utilisateur s’applique une étiquette qui est configurée pour conserver le contenu ou conserver et puis supprimer le contenu à un dossier ou un élément dans leur boîte aux lettres, la propriété de la boîte aux lettres *ComplianceTagHoldApplied* est définie sur **True**. Dans ce cas, la boîte aux lettres est considéré comme être mise en attente, comme s’il a été mis en attente pour litige ou affecté à une stratégie de rétention d’Office 365. Lorsque la propriété *ComplianceTagHoldApplied* est définie sur **True**, les éléments suivants peuvent se produire :

- Si la boîte aux lettres ou le compte d’utilisateur de l’utilisateur Office 365 est supprimé, la boîte aux lettres devient une [boîte aux lettres inactive](inactive-mailboxes-in-office-365.md).
- Vous ne pourrez pas désactiver la boîte aux lettres (la boîte aux lettres principale ou la boîte aux lettres archive, s’il est activé).
- Éléments dans la boîte aux lettres peuvent être conservés plus longtemps que prévu. Il s’agit, car la boîte aux lettres est en attente et par conséquent aucun élément n’est définitivement supprimés (définitivement).

Pour afficher la valeur de la propriété *ComplianceTagHoldApplied* , exécutez la commande suivante dans Exchange Online PowerShell :

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Pour plus d’informations sur les étiquettes, voir [vue d’ensemble d’Office 365 étiquettes](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>La gestion des boîtes aux lettres sur le délai de blocage

Une fois que n’importe quel type de suspension est supprimé d’une boîte aux lettres, la valeur de la propriété de la boîte aux lettres *DelayHoldApplied* est définie sur **True**. Cela se produit la prochaine fois que l’Assistant dossier géré traite la boîte aux lettres et détecte qu’une suspension a été supprimée. Est appelé un *délai de blocage* et signifie que la suppression effective de la suspension est différée pendant 30 jours empêcher les données d’être définitivement supprimés (définitivement) de la boîte aux lettres. Cela permet d’administrateurs permet de rechercher ou de récupérer des éléments de boîte aux lettres qui seront purgés une fois la suspension est réellement supprimée. Lorsque le délai est suspendu sur la boîte aux lettres, la boîte aux lettres est considérée en attente pour une durée illimitée, en tant que si la boîte aux lettres a été litige. Après 30 jours, la suspension de délai d’attente expire et Office 365 tente automatiquement de supprimer la suspension de délai d’attente (en définissant la propriété *DelayHoldApplied* sur **False**) afin que le blocage soit réellement supprimé. Après la propriété *DelayHoldApplied* sur **False**, les éléments qui sont marquées pour suppression seront purgés la prochaine fois que la boîte aux lettres est traitée par l’Assistant dossier géré.

Pour afficher la valeur de la propriété *DelayHoldApplied* pour une boîte aux lettres, exécutez la commande suivante dans Exchange Online PowerShell.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Pour supprimer la suspension de délai d’attente avant son expiration, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell : 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Notez que vous devez être affecté au rôle suspens pour raisons juridiques dans Exchange Online à utiliser le paramètre *RemoveDelayHoldApplied* 

Pour supprimer la suspension de délai d’attente sur une boîte aux lettres inactive, exécutez la commande suivante dans Exchange Online PowerShell :

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> La meilleure façon de spécifier une boîte aux lettres inactive dans la commande précédente consiste à utiliser sa valeur de nom unique ou le GUID de Exchange. À l’aide d’une de ces valeurs permet d’éviter que par inadvertance spécifiant la boîte aux lettres incorrect. 

## <a name="next-steps"></a>Étapes suivantes

Après avoir identifié les suspensions appliquées à une boîte aux lettres, vous pouvez effectuer des tâches telles que la modification de la durée de la suspension, temporairement ou supprimer définitivement la suspension, ou dans le cas des stratégies de rétention Office 365, à l’exception d’une boîte aux lettres inactive à partir de la stratégie. Pour plus d’informations sur l’exécution de tâches relatives aux suspensions, voir l’une des rubriques suivantes :

- Exécutez le [Set-RetentionCompliancePolicy - AddExchangeLocationException \<boîte aux lettres utilisateur >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) commande PowerShell de centre de conformité et de sécurité à exclure d’une boîte aux lettres à partir d’une stratégie de rétention d’Office 365 à l’échelle de l’organisation. Notez que cette commande peut uniquement être utilisée pour les stratégies de rétention où est égale à la valeur de la propriété *ExchangeLocation* `All`.

- Exécutez le [Set-Mailbox - ExcludeFromOrgHolds \<conserver GUID sans le préfixe ou le suffixe >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) command dans Exchange Online PowerShell pour exclure une boîte aux lettres inactive d’une stratégie de rétention d’Office 365 à l’échelle de l’organisation.

- [Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)

- [Supprimer des éléments en attente dans le dossier Éléments récupérables des boîtes aux lettres basées sur le cloud](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
