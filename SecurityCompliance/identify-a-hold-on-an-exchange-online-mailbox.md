---
title: Comment identifier le type de conservation placé sur une boîte aux lettres Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
description: Découvrez comment identifier les différents types de conservation pouvant être placés sur une boîte aux lettres Office 365. Ces types de conservation incluent les conservations pour litige, la découverte électronique et les stratégies de rétention d’Office 365. Vous pouvez également déterminer si un utilisateur a été exclu d’une stratégie de rétention à l’échelle de l’organisation.
ms.openlocfilehash: 29ae9d7ba8be2bf0064c163605aee9ad8fd5fd07
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154196"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Comment identifier le type de conservation placé sur une boîte aux lettres Exchange Online

Cet article explique comment identifier des suspensions placées sur des boîtes aux lettres Exchange Online dans Office 365.

Office 365 offre plusieurs méthodes permettant à votre organisation d’empêcher la suppression définitive du contenu de la boîte aux lettres. Cela permet à votre organisation de conserver du contenu pour respecter les règles de conformité normales ou pour la durée de l’enquête ou d’autres types d’investigation. Voici une liste des fonctionnalités de rétention (également ** appelées conservations) dans Office 365:

- **Conservation pour litige** -conservations appliquées aux boîtes aux lettres utilisateur dans Exchange Online.

- **conservations de découverte électronique** qui sont associées à un cas eDiscovery dans le centre de sécurité et de conformité. les conservations eDiscovery peuvent être appliquées aux boîtes aux lettres des utilisateurs et dans la boîte aux lettres correspondante pour les groupes Office 365 et Microsoft Teams.

- **Conservation** inaltérable appliquées aux boîtes aux lettres des utilisateurs à l’aide de l’outil de blocage de découverte électronique & dans le centre d’administration Exchange dans Exchange Online.

- **Stratégie de rétention Office 365** : conserve le contenu des boîtes aux lettres utilisateur dans Exchange Online et dans la boîte aux lettres correspondante pour les groupes Office 365 et Microsoft Teams. Vous pouvez créer une stratégie de rétention qui conserve les conversations Skype entreprise, qui sont stockées dans des boîtes aux lettres utilisateur.

  Il existe deux types de stratégies de rétention Office 365 pouvant être attribuées à des boîtes aux lettres.

    - Stratégies de rétention d' **emplacement spécifiques** : il s’agit de stratégies affectées aux emplacements de contenu d’utilisateurs spécifiques. Vous utilisez la cmdlet **Get-Mailbox** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention affectées à des boîtes aux lettres spécifiques.

    - **Stratégies** de rétention à l’échelle de l’Organisation: ce sont des stratégies qui sont affectées à tous les emplacements de contenu de votre organisation. Vous utilisez la cmdlet **Get-OrganizationConfig** dans Exchange Online PowerShell pour obtenir des informations sur les stratégies de rétention à l’échelle de l’organisation.
  Pour plus d’informations, consultez la section «application d’une stratégie de rétention à une organisation ou des emplacements spécifiques» dans [vue d’ensemble des stratégies de rétention Office 365](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

- **Étiquettes de rétention office 365** : si un utilisateur applique une étiquette de rétention Office 365 (une étiquette configurée pour conserver le contenu ou conserver et supprimer du contenu) pour *un* dossier ou un élément de sa boîte aux lettres, une conservation est placée sur la boîte aux lettres comme si elle était mise en attente pour litige ou affectation à une stratégie de rétention Office 365. Pour plus d’informations, consultez la section [identification des boîtes aux lettres en attente, car une étiquette de rétention a été appliquée à un dossier ou à une](#identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item) section d’élément de cet article.

Pour gérer les boîtes aux lettres en conservation, il se peut que vous deviez identifier le type de blocage placé sur une boîte aux lettres afin de pouvoir effectuer des tâches telles que la modification de la durée de la conservation, la suppression temporaire ou définitive de la conservation ou l’exclusion d’une boîte aux lettres d’une stratégie de rétention Office 365. Dans ce cas, la première étape consiste à identifier le type de conservation placé sur la boîte aux lettres. Étant donné que plusieurs conservations (et différents types de suspensions) peuvent être placées sur une seule boîte aux lettres, vous devez identifier toutes les suspensions placées sur une boîte aux lettres si vous voulez les supprimer ou les modifier.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Étape 1: obtention du GUID pour les suspensions placées sur une boîte aux lettres

Vous pouvez exécuter les deux cmdlets suivantes dans Exchange Online PowerShell pour obtenir le GUID des suspensions placées sur une boîte aux lettres. Une fois que vous avez obtenu un GUID, vous l’utilisez pour identifier la conservation spécifique à l’étape 2. Notez que les conservations pour litige ne sont pas identifiées par un GUID. Les conservations pour litige sont activées ou désactivées pour une boîte aux lettres.

- **Get-Mailbox** -Utilisez cette cmdlet pour déterminer si la conservation pour litige est activée pour une boîte aux lettres et pour obtenir les GUID pour les conservations eDiscovery, les conservations inaltérables et les stratégies de rétention Office 365 spécifiquement attribuées à une boîte aux lettres. La sortie de cette applet de commande indique également si une boîte aux lettres a été explicitement exclue d’une stratégie de rétention à l’échelle de l’organisation.

- **Get-OrganizationConfig** -Utilisez cette cmdlet pour obtenir les GUID pour les stratégies de rétention à l’échelle de l’organisation.

Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Exécutez la commande suivante pour obtenir des informations sur les conservations et les stratégies de rétention Office 365 appliquées à une boîte aux lettres.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> S’il y a trop de valeurs dans la propriété InPlaceHolds et qu’elles ne sont pas toutes affichées, vous pouvez `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` exécuter la commande pour afficher chaque GUID sur une ligne distincte.

Le tableau suivant décrit comment identifier différents types de suspensions en fonction des valeurs de la propriété *InPlaceHolds* lorsque vous exécutez la cmdlet **Get-Mailbox** .


|Type de conservation  |Exemple de valeur  |Comment identifier la conservation  |
|---------|---------|---------|
|Conservation pour litige     |    `True`     |     La conservation pour litige est activée pour une boîte ** aux lettres si la propriété `True`LitigationHoldEnabled est définie sur.    |
|conservation eDiscovery     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   La *propriété InPlaceHolds* contient le GUID de n’importe quelle conservation associée à un cas eDiscovery dans le centre de sécurité et de conformité. Vous pouvez indiquer qu’il s’agit d’une conservation eDiscovery, car le `UniH` GUID commence par le préfixe (qui désigne une conservation unifiée).      |
|Blocage local     |     `c0ba3ce811b6432a8751430937152491` <br/> ou <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     La propriété *InPlaceHolds* contient le GUID de la conservation inaltérable qui est placée sur la boîte aux lettres. Vous pouvez indiquer qu’il s’agit d’une conservation inaltérable, car le GUID ne commence pas par un préfixe ou il `cld` commence par le préfixe.     |
|Stratégie de rétention Office 365 spécifiquement appliquée à la boîte aux lettres     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> ou <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     La propriété InPlaceHolds contient les GUID de n’importe quelle stratégie de rétention d’emplacement spécifique qui est appliquée à la boîte aux lettres. Vous pouvez identifier les stratégies de rétention, car `mbx` le GUID `skp` commence par le ou le préfixe. Le `skp` préfixe indique que la stratégie de rétention est appliquée aux conversations Skype entreprise dans la boîte aux lettres de l’utilisateur.    |
|Exclu d’une stratégie de rétention Office 365 à l’échelle de l’Organisation     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Si une boîte aux lettres est exclue d’une stratégie de rétention Office 365 à l’échelle de l’organisation, le GUID de la stratégie de rétention à laquelle la boîte `-mbx` aux lettres est exclue s’affiche dans la propriété InPlaceHolds et est identifié par le préfixe.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Si la propriété *InPlaceHolds* est vide lorsque vous exécutez la cmdlet **Get-Mailbox** , il peut y avoir une ou plusieurs stratégies de rétention Office 365 à l’échelle de l’organisation appliquées à la boîte aux lettres. Exécutez la commande suivante dans Exchange Online PowerShell pour obtenir la liste des GUID pour les stratégies de rétention Office 365 à l’échelle de l’organisation.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> S’il y a trop de valeurs dans la propriété InPlaceHolds et qu’elles ne sont pas toutes affichées, vous pouvez `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` exécuter la commande pour afficher chaque GUID sur une ligne distincte.

Le tableau suivant décrit les différents types de conservations à l’échelle de l’organisation et comment identifier chaque type en fonction des GUID contenus dans la propriété *InPlaceHolds* lorsque vous exécutez la cmdlet **Get-OrganizationConfig** .


|Type de conservation  |Exemple de valeur  |Description  |
|---------|---------|---------|
|Stratégies de rétention Office 365 appliquées aux boîtes aux lettres Exchange, aux dossiers publics Exchange et aux conversations teams    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Les stratégies de rétention à l’échelle de l’organisation appliquées aux boîtes aux lettres Exchange, aux dossiers publics Exchange et aux conversations 1xN dans Microsoft teams `mbx` sont identifiées par des GUID qui commencent par le préfixe. Notez que les conversations 1xN sont stockées dans la boîte aux lettres des participants individuels de la conversation.      |
|Stratégie de rétention Office 365 appliquée aux groupes Office 365 groupes et teams messages de canal     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Les stratégies de rétention à l’échelle de l’organisation appliquées aux groupes Office 365 et aux messages de canal dans Microsoft teams sont identifiées par des GUID qui commencent par le `grp` préfixe. Notez que les messages de canal sont stockés dans la boîte aux lettres de groupe qui est associée à une équipe Microsoft.     |

Pour plus d’informations sur les stratégies de rétention appliquées à Microsoft Teams, consultez la section «emplacement des équipes» [vue d’ensemble des stratégies de](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations)rétention.

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Présentation du format de la valeur InPlaceHolds pour les stratégies de rétention

Outre le préfixe (MBX, SKP ou GRP) qui identifie un élément dans la propriété InPlaceHolds en tant que stratégie de rétention Office 365, la valeur contient également un suffixe qui identifie le type d’action de rétention configuré pour la stratégie. Par exemple, le suffixe d’action est mis en surbrillance en gras dans les exemples suivants:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

Le tableau suivant définit les trois actions de rétention possibles:

|Valeur  |Description  |
|---------|---------|
|**0,1**     | Indique que la stratégie de rétention est configurée pour supprimer des éléments; la stratégie ne conserve pas d’éléments.        |
|**n°2**    |    Indique que la stratégie de rétention est configurée pour conserver les éléments; la stratégie ne supprime pas les éléments après l’expiration de la période de rétention.     |
|**3**     |   Indique que la stratégie de rétention est configurée pour conserver les éléments, puis les supprimer après l’expiration de la période de rétention.      |

Pour plus d’informations sur les actions de rétention, voir la section «conservation du contenu pendant une période de temps spécifique» dans [vue d’ensemble des stratégies](retention-policies.md#retaining-content-for-a-specific-period-of-time)de rétention.
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Étape 2: utilisation du GUID pour identifier la conservation

Une fois que vous avez obtenu le GUID pour une conservation appliquée à une boîte aux lettres, l’étape suivante consiste à utiliser ce GUID pour identifier la conservation. Les sections suivantes montrent comment identifier le nom de la conservation (et d’autres informations) à l’aide du GUID de suspension.

### <a name="ediscovery-holds"></a>conservations eDiscovery

Exécutez les commandes suivantes dans Security & Compliance Center PowerShell pour identifier une conservation eDiscovery appliquée à la boîte aux lettres. Utilisez le GUID (sans le préfixe UniH) pour le blocage eDiscovery que vous avez identifié à l’étape 1. La première commande crée une variable qui contient des informations sur la conservation; Cette variable est utilisée dans les autres commandes. La deuxième commande affiche le nom du cas eDiscovery auquel la conservation est associée. La troisième commande affiche le nom de la conservation et la liste des boîtes aux lettres auxquelles elle s’applique.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Pour vous connecter au centre de sécurité & Compliance Center PowerShell, consultez [la rubrique Connect to Security _AMP_ Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>Archives permanentes

Exécutez la commande suivante dans Exchange Online PowerShell pour identifier la conservation inaltérable qui est appliquée à la boîte aux lettres. Utilisez le GUID pour le blocage sur place que vous avez identifié à l’étape 1. La commande affiche le nom de la conservation et la liste des boîtes aux lettres auxquelles la conservation s’applique.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Notez que si le GUID de la conservation inaltérable commence par le `cld` préfixe, veillez à inclure le préfixe lors de l’exécution de la commande précédente.

### <a name="office-365-retention-policies"></a>Stratégies de rétention Office 365

Exécutez la commande suivante dans Security & Compliance Center PowerShell pour identifier la stratégie de rétention Office 365 (à l’échelle de l’organisation ou spécifique) appliquée à la boîte aux lettres. Utilisez le GUID (sans inclure le préfixe MBX, SKP ou GRP ou le suffixe d’action) que vous avez identifié à l’étape 1.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="identifying-mailboxes-on-hold-because-a-retention-label-has-been-applied-to-a-folder-or-item"></a>Identification des boîtes aux lettres en attente, car une étiquette de rétention a été appliquée à un dossier ou à un élément

Chaque fois qu’un utilisateur applique une étiquette de rétention configurée pour conserver le contenu ou conserver, puis supprimer le contenu d’un dossier ou d’un élément de sa boîte aux lettres, la propriété de boîte aux lettres *ComplianceTagHoldApplied* est définie sur **true**. Dans ce cas, la boîte aux lettres est considérée comme étant en attente, comme si elle était placée en conservation pour litige ou affectée à une stratégie de rétention Office 365. Lorsque la propriété *ComplianceTagHoldApplied* est définie sur **true**, les événements suivants peuvent se produire:

- Si la boîte aux lettres ou le compte d’utilisateur Office 365 de l’utilisateur est supprimé, la boîte aux lettres devient une [boîte aux lettres inactive](inactive-mailboxes-in-office-365.md).
- Vous ne pourrez pas désactiver la boîte aux lettres (la boîte aux lettres principale ou la boîte aux lettres d’archivage, si elle est activée).
- Les éléments de la boîte aux lettres peuvent être conservés plus longtemps que prévu. Cela est dû au fait que la boîte aux lettres est en attente et que, par conséquent, aucun élément ne sera supprimé définitivement (purgé).

Pour afficher la valeur de la propriété *ComplianceTagHoldApplied* , exécutez la commande suivante dans Exchange Online PowerShell:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Pour plus d’informations sur les étiquettes de rétention, consultez la rubrique [vue d’ensemble des étiquettes de rétention Office 365](labels.md).

## <a name="managing-mailboxes-on-delay-hold"></a>Gestion des boîtes aux lettres en attente de retard

Après la suppression d’un type de conservation d’une boîte aux lettres, la valeur de la propriété de boîte aux lettres *DelayHoldApplied* est définie sur **true**. Cela se produit la prochaine fois que l’Assistant dossier géré traite la boîte aux lettres et détecte qu’une conservation a été supprimée. Cette opération est appelée *retard de conservation* et signifie que la suppression effective de la conservation est retardée de 30 jours pour empêcher la suppression définitive des données de la boîte aux lettres. Les administrateurs peuvent ainsi Rechercher ou récupérer les éléments de boîte aux lettres qui seront purgés après la suppression effective de la conservation. Lorsqu’une boîte aux lettres est suspendue, la boîte aux lettres est toujours considérée comme suspendue pendant une durée illimitée, comme si la boîte aux lettres était en conservation pour litige. Au bout de 30 jours, le délai d’attente expire et Office 365 tente automatiquement de supprimer le blocage de délai (en définissant la propriété *DelayHoldApplied* sur **false**) de sorte que la suspension soit réellement supprimée. Une fois que la propriété *DelayHoldApplied* a la **valeur false**, les éléments marqués pour suppression sont purgés lors du prochain traitement de la boîte aux lettres par l’Assistant dossier géré.

Pour afficher la valeur de la propriété *DelayHoldApplied* pour une boîte aux lettres, exécutez la commande suivante dans Exchange Online PowerShell.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Pour supprimer le délai d’attente avant qu’il expire, vous pouvez exécuter la commande suivante dans Exchange Online PowerShell: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Notez que vous devez disposer du rôle conservation légal dans Exchange Online pour utiliser le paramètre *RemoveDelayHoldApplied* 

Pour supprimer la conservation différée sur une boîte aux lettres inactive, exécutez la commande suivante dans Exchange Online PowerShell:

```
Set-Mailbox <DN or Exchange GUID> -InactiveMailbox -RemoveDelayHoldApplied
```

> [!TIP]
> La meilleure façon de spécifier une boîte aux lettres inactive dans la commande précédente consiste à utiliser son nom unique ou sa valeur de GUID Exchange. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres. 

## <a name="next-steps"></a>Étapes suivantes

Une fois que vous avez identifié les conservations appliquées à une boîte aux lettres, vous pouvez effectuer des tâches telles que modifier la durée de la suspension, temporairement ou définitivement la suppression de la conservation, ou dans le cas des stratégies de rétention Office 365, à l’exception d’une boîte aux lettres inactive de la stratégie. Pour plus d’informations sur l’exécution de tâches relatives aux suspensions, consultez l’une des rubriques suivantes:

- Exécutez la commande [Set-retentioncompliancepolicy permet- \<AddExchangeLocationException user Mailbox>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) dans Security & Compliance Center PowerShell pour exclure une boîte aux lettres d’une stratégie de rétention Office 365 à l’échelle de l’organisation. Notez que cette commande ne peut être utilisée que pour les stratégies de rétention ** pour lesquelles la valeur `All`de la propriété exchangelocation permet est égale à.

- Exécutez le [GUID de conservation Set- \<Mailbox-ExcludeFromOrgHolds sans préfixe ou commande Suffix>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) dans Exchange Online PowerShell pour exclure une boîte aux lettres inactive d’une stratégie de rétention Office 365 à l’échelle de l’organisation.

- [Modifier la durée de la conservation pour une boîte aux lettres inactive dans Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Supprimer une boîte aux lettres inactive dans Office 365](delete-an-inactive-mailbox.md)

- [Supprimer des éléments en attente dans le dossier Éléments récupérables des boîtes aux lettres basées sur le cloud](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)
