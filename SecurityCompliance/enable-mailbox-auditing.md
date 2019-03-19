---
title: Gérer l'audit des boîtes aux lettres
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: La journalisation d'audit de boîte aux lettres est activée par défaut dans Microsoft 365 (également appelée audit de boîte aux lettres par défaut ou audit de boîte aux lettres par défaut). En d'autres termes, certaines actions effectuées par les propriétaires de boîtes aux lettres, les délégués et les administrateurs sont automatiquement enregistrées dans un journal d'audit de boîte aux lettres, dans lequel vous pouvez rechercher des activités effectuées sur la boîte aux lettres.
ms.openlocfilehash: 604b7fc26c2e97a5efce28fe844fbd066196c4ce
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670629"
---
# <a name="manage-mailbox-auditing"></a>Gérer l'audit des boîtes aux lettres
  
À compter du 1er janvier 2019, Microsoft Active la journalisation d'audit des boîtes aux lettres par défaut pour toutes les organisations Microsoft 365. En d'autres termes, certaines actions effectuées par les propriétaires de boîtes aux lettres, les délégués et les administrateurs sont automatiquement journalisées, et les enregistrements d'audit de boîte aux lettres correspondants sont disponibles lorsque vous les recherchez dans le journal d'audit de boîte aux lettres. Avant que l'audit des boîtes aux lettres ait été activé par défaut, vous devez l'activer manuellement pour chaque boîte aux lettres d'utilisateur de votre organisation. 

Voici quelques avantages de l'audit des boîtes aux lettres par défaut:

- L'audit est activé par défaut lorsque vous créez une nouvelle boîte aux lettres. Vous n'aurez pas à l'activer manuellement pour les nouveaux utilisateurs. 

- Vous n'aurez pas à gérer les actions de boîte aux lettres qui sont auditées. Un ensemble défini d'actions de boîte aux lettres est audité par défaut pour chaque type de connexion. Ces [types d'ouverture de session](#mailbox-actions-logged-by-default) sont Owner, Delegate et admin.

- Les nouvelles actions de boîte aux lettres publiées par Microsoft seront auditées par défaut. Lorsque Microsoft publie une nouvelle action de boîte aux lettres (en particulier celles qui contribuent à protéger votre organisation et vous aide à effectuer des enquêtes de manière légale), elle est automatiquement ajoutée à la liste des actions de boîte aux lettres auditées par défaut. Cela signifie que vous n'avez pas besoin d'ajouter de nouvelles actions à la liste des actions de boîte aux lettres effectuées par les propriétaires, les délégués ou les administrateurs. 

- Assurez-vous que vous auditez les mêmes actions pour toutes les boîtes aux lettres afin de disposer d'une stratégie d'audit de boîte aux lettres cohérente au sein de votre organisation.

> [!TIP]
> Il est important de garder à l'esprit qu'avec la version d'audit des boîtes aux lettres activée par défaut, vous n'avez rien à faire pour gérer l'audit des boîtes aux lettres. Toutefois, si vous souhaitez en savoir plus, modifier le comportement par défaut ou le désactiver, cet article peut vous aider à le faire.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>Vérifier que l'audit de boîte aux lettres activé est activé par défaut

Pour vérifier que l'audit de boîte aux lettres activé par défaut est activé pour votre organisation, exécutez la commande suivante dans [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell):

```
Get-OrganizationConfig | FL AuditDisabled
``` 

La valeur **false** indique que l'audit des boîtes aux lettres activé par défaut est activé pour votre organisation. 

Lorsque l'audit de boîte aux lettres activé est activé par défaut (lorsque la propriété *AuditDisabled* est **** définie sur false), le paramètre d'organisation remplace le paramètre d'audit de boîte aux lettres d'une boîte aux lettres spécifique. Par exemple, si la propriété *AuditEnabled* d'une boîte aux lettres est définie sur **false**, mais que l'audit de boîte aux lettres activé par défaut est activé pour votre organisation, les actions de boîte aux lettres par défaut seront auditées pour cette boîte aux lettres. Si l'audit des boîtes aux lettres a été explicitement désactivé pour une boîte aux lettres spécifique et que vous souhaitez toujours le désactiver, vous pouvez configurer le contournement de l'audit des boîtes aux lettres pour le propriétaire de la boîte aux lettres et d'autres utilisateurs auxquels l'accès à la boîte aux lettres a été délégué. Pour plus d'informations, reportez-vous à la section Contournement de l' [enregistrement d'audit des boîtes aux lettres](#bypass-mailbox-audit-logging) dans cet article.

> [!NOTE]
> Lorsque l'audit de boîte aux lettres activé est activé par défaut, la propriété *AuditEnabled* d'une boîte aux lettres n'est pas remplacée par la **valeur true** si elle était définie sur **false**. En d'autres termes, l'audit de boîte aux lettres sur par défaut ignore la propriété *AuditEnabled* pour une boîte aux lettres.

## <a name="supported-mailbox-types"></a>Types de boîtes aux lettres pris en charge

Le tableau suivant indique les types de boîtes aux lettres actuellement pris en charge par l'audit des boîtes aux lettres par défaut:

|Type de boîte aux lettres|Pris en charge|Non pris en charge|
|:---------|:---------:|:---------:|
|Boîtes aux lettres utilisateur    |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         |
|Boîtes aux lettres partagées    |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |       |
|Boîtes aux lettres de groupe Office 365    |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)         |         |
|Boîtes aux lettres de ressources    |      |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |
|Boîtes aux lettres de dossiers publics    |       |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)  |
||||

## <a name="mailbox-actions-logged-by-default"></a>Actions de boîte aux lettres journalisées par défaut

Un ensemble d'actions de boîte aux lettres est enregistré par défaut pour chacun des types d'ouverture de session suivants:  

   - **Owner** : propriétaire de la boîte aux lettres. 
   
   - **Delegate** : un autre utilisateur auquel l'autorisation SendAs, SendOnBehalf ou FullAccess est attribuée à la boîte aux lettres d'une personne. Notez qu'un administrateur disposant de l'autorisation FullAccess sur la boîte aux lettres d'un utilisateur est également considéré comme un utilisateur délégué.
   
    - **Administrateur** : les boîtes aux lettres sont considérées comme accessibles par un type d'ouverture de session d'administrateur uniquement dans les scénarios suivants:
    
       - Lorsqu'une boîte aux lettres est recherchée avec l'un des outils Microsoft eDiscovery suivants: 

         - Recherche de contenu dans le centre de conformité.
       
         -  eDiscovery ou Advanced eDiscovery dans le centre de conformité.
       
         - Découverte électronique inaltérable dans Exchange Online.
       - Lorsque l' [Éditeur MAPI Microsoft Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=204086) est utilisé pour accéder à la boîte aux lettres.     

Le tableau suivant répertorie les actions de boîte aux lettres actuellement enregistrées par défaut pour chaque type d'ouverture de session.

|Actions d'administration|Actions de délégué|Actions du propriétaire|
|:---------|:---------|:---------|
|Créer    |Créer       | HardDelete        |
|HardDelete    |HardDelete        |MoveToDeletedItems       |
|MoveToDeletedItems    |MoveToDeletedItems         |SoftDelete         |
|SendAs    |SendAs      |    Mettre à jour     |
|SendOnBehalf    |SendOnBehalf       |UpdateCalendarDelegation        |
|SoftDelete     |SoftDelete      | UpdateFolderPermissions        |
|Mettre à jour    |Mettre à jour       |UpdateInboxRules         |
|UpdateCalendarDelegation    | UpdateFolderPermissions        |         |
|UpdateFolderPermissions     | UpdateInboxRules        |         |
|UpdateInboxRules     |         |         |
||||

Voici les descriptions de ces actions de boîte aux lettres. 

|Action de boîte aux lettres|Description|
|:---------|:---------|
|**Créer** <br/> |Un élément a été créé dans le dossier calendrier, contacts, notes ou tâches dans la boîte aux lettres; par exemple, une nouvelle demande de réunion est créée. Notez que la création, l'envoi ou la réception d'un message n'est pas audité. En outre, la création d'un dossier de boîte aux lettres n'est pas auditée.  <br/> |
|**HardDelete** <br/> |Un message a été purgé du dossier Éléments récupérables.  <br/> |
|**MoveToDeletedItems** <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |
|**SendAs** <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |
|**SendOnBehalf** <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |
|**SoftDelete** <br/> |Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.  <br/> |
|**Update** <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |
|**UpdateCalendarDelegation** <br/> |Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à une autre personne de la même organisation des autorisations pour gérer le calendrier du propriétaire de la boîte aux lettres.  <br/> |
|**UpdateFolderPermissions** <br/> |Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d'une boîte aux lettres et aux messages qu'ils hébergent.  <br/> |
|**UpdateInboxRules** <br/> |Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Les règles de boîte de réception sont utilisées pour traiter les messages dans la boîte de réception de l'utilisateur en fonction des conditions spécifiées et prendre des mesures lorsque les conditions d'une règle sont remplies, telles que le transfert d'un message vers un dossier spécifié ou la suppression d'un message.  <br/> |
|||

Pour obtenir la liste complète des actions de boîte aux lettres, y compris les actions qui sont disponibles mais qui ne sont pas incluses dans le jeu d'actions par défaut, consultez la section [actions d'audit de boîte aux lettres](#mailbox-auditing-actions) dans cet article.

> [!IMPORTANT]
> Si vous avez explicitement configuré les actions de boîte aux lettres à auditer pour tout type d'ouverture de session avant l'audit des boîtes aux lettres activé par défaut pour l'organisation, la configuration existante de la boîte aux lettres sera prioritaire et ne sera pas remplacée par la boîte aux lettres par défaut. actions décrites dans cette section. Si vous souhaitez rétablir les actions de boîte aux lettres par défaut à tout moment, exécutez la commande **Set-Mailbox-DefaultAuditSet** . Pour plus d'informations sur cette procédure, reportez-vous à la section [restaurer les actions de boîte aux lettres par défaut](#restore-the-default-mailbox-actions) de cet article.

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>Vérifier que les actions de boîte aux lettres par défaut sont journalisées pour chaque type d'ouverture de session

Avec la publication de l'audit des boîtes aux lettres activée par défaut, une nouvelle propriété de boîte aux lettres nommée *DefaultAuditSet* a été ajoutée. Cette propriété indique si les actions de boîte aux lettres par défaut (gérées par Microsoft) sont auditées pour chaque type de connexion pour une boîte aux lettres spécifiée. Vous pouvez exécuter la commande suivante pour afficher les valeurs de cette propriété:

```
Get-Mailbox <username> | FL DefaultAuditSet
```

La valeur `Admin, Delegate, Owner` indique que les actions de boîte aux lettres par défaut pour les trois types d'ouverture de session sont auditées et qu'un administrateur de votre organisation n' *a pas* modifié les actions pour un type d'ouverture de session. Remarque Il s'agit de l'État par défaut après activation initiale de l'audit des boîtes aux lettres dans votre organisation. 

Si un administrateur de votre organisation a modifié les actions de boîte aux lettres qui sont auditées pour un type d'ouverture de session (à l'aide de la cmdlet **Set-Mailbox** avec les paramètres *AuditAdmin*, *AuditDelegate*ou *AuditOwner* ), la valeur de la propriété *DefaultAuditSet* sera différente de la valeur par défaut. Par exemple, une valeur de `Owner` indique que seules les actions de boîte aux lettres par défaut pour le propriétaire de la boîte aux lettres sont auditées `Delegate` , `Admin` et que les actions pour et ont été modifiées. Si aucune valeur n'est affichée pour la propriété *DefaultAuditSet* (également appelée valeur *null* ), les actions de boîte aux lettres pour les trois types d'ouverture de session ont été modifiées.

Consultez la section [modifier ou restaurer les actions de boîte aux lettres enregistrées par défaut](#change-or-restore-mailbox-actions-logged-by-default) de cet article pour plus d'informations sur la modification des actions de boîte aux lettres auditées.

### <a name="display-a-list-of-mailbox-actions-logged-by-default"></a>Afficher la liste des actions de boîte aux lettres enregistrées par défaut

Vous pouvez exécuter les commandes suivantes dans Exchange Online PowerShell pour afficher la liste des actions de boîte aux lettres qui sont actuellement associées à une boîte aux lettres pour chaque type d'ouverture de session:

**Actions du propriétaire**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditOwner
```

**Actions de délégué**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditDelegate
```

**Actions d'administration**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>Modifier ou restaurer les actions de boîte aux lettres enregistrées par défaut

Comme expliqué précédemment, l'un des principaux avantages de l'audit de boîte aux lettres par défaut est que vous n'avez pas besoin de gérer les actions des boîtes aux lettres qui sont auditées. Microsoft effectue cette opération pour vous et ajoute automatiquement les nouvelles actions de boîte aux lettres à auditer par défaut lors de leur publication. Toutefois, votre organisation peut avoir des raisons d'auditer un ensemble d'actions de boîte aux lettres qui sont différentes de celles par défaut. Cette section explique comment modifier les actions de boîte aux lettres qui sont auditées pour chaque type d'ouverture de session et comment rétablir les actions par défaut gérées par Microsoft.

> [!IMPORTANT]
> Si vous modifiez les actions de boîte aux lettres d'un utilisateur qui sont enregistrées par défaut (comme décrit dans la section suivante), toutes les nouvelles actions de boîte aux lettres publiées par Microsoft ne seront pas auditées pour ces boîtes aux lettres. Vous devrez ajouter explicitement une nouvelle action de boîte aux lettres à la liste des actions qui sont auditées pour un type d'ouverture de session.

### <a name="change-the-mailbox-actions-to-audit"></a>Modifier les actions de boîte aux lettres en audit

Vous pouvez utiliser la cmdlet **Set-Mailbox** avec les paramètres *AuditAdmin*, *AuditDelegate*ou *AuditOwner* pour modifier les actions de boîte aux lettres qui sont auditées, en fonction du type d'ouverture de session. Étant donné que ces paramètres liés à l'audit sont des paramètres à valeurs multiples (ce qui signifie qu'ils peuvent avoir plusieurs valeurs), il existe deux manières différentes de les modifier.

- Vous pouvez spécifier plusieurs actions de boîte aux lettres qui remplacent les actions existantes à l'aide `action1,action2,...actionN`de la syntaxe suivante:.

- Vous pouvez ajouter ou supprimer une ou plusieurs actions de boîte aux lettres sans affecter les enregistrements existants à l'aide `@{Add="action1","value2"}` de `@{Remove="action1","action2"}`la syntaxe suivante: ou.

Quelle que soit la méthode utilisée pour modifier les actions de boîte aux lettres auditées, les actions de boîte aux lettres auditées par défaut (pour le type de connexion que vous avez modifié) ne seront plus gérées par Microsoft. En outre, la valeur du type de connexion que vous avez modifié ne s'affichera pas dans le paramètre de boîte aux lettres *DefaultAuditSet* [précédemment décrit](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type).

Voici quelques exemples d'utilisation de l'une de ces méthodes pour modifier les actions de boîte aux lettres à auditer pour chacun des différents types d'ouverture de session. 

Cet exemple modifie les actions de boîte aux lettres d'administrateur en écrasant les actions par défaut avec SoftDelete et HardDelete. 

```
Set-Mailbox <username> -AuditAdmin HardDelete,SoftDelete
```

Cet exemple montre comment ajouter l'action owner MailboxLogin. 

```
Set-Mailbox <username> -AuditOwner @{Add="MailboxLogin"}
```

Cet exemple montre comment supprimer l'action de délégué MoveToDeletedItems.

```
Set-Mailbox <username> -AuditDelegate @{Remove="MoveToDeletedItems"}
```

#### <a name="checking-the-defaultauditset-property"></a>Vérification de la propriété DefaultAuditSet

Une fois que vous avez modifié les actions de boîte aux lettres par défaut pour un type d'ouverture de session, la propriété *DefaultAuditSet* de la boîte aux lettres est automatiquement mise à jour pour refléter cette modification. Par exemple, si vous exécutez `Get-Mailbox <username> | FL DefaultAuditSet` après la première fois que vous ajoutez ou supprimez une action de propriétaire de boîte aux lettres, la commande `Admin, Delegate`renverra uniquement une valeur de. Cela indique que les actions de boîte aux lettres par défaut pour le propriétaire ont été modifiées. cela signifie également que les nouvelles actions de propriétaire de boîte aux lettres libérées par Microsoft ne seront pas automatiquement ajoutées à cette boîte aux lettres. Il en est de même pour la modification des actions de boîte aux lettres pour le type d'ouverture de session admin ou Delegate.

### <a name="restore-the-default-mailbox-actions"></a>Restaurer les actions de boîte aux lettres par défaut

Si vous avez apporté des modifications aux actions de boîte aux lettres qui sont auditées pour un type d'ouverture de session, vous pouvez restaurer les actions de boîte `Set-Mailbox -DefaultAuditSet` aux lettres par défaut auditées en exécutant la commande. Lorsque vous procédez ainsi, les événements suivants se produisent:

- La liste actuelle des actions de boîte aux lettres est remplacée par les actions de boîte aux lettres par défaut pour le type d'ouverture de session approprié.
 
- Toutes les nouvelles actions de boîte aux lettres publiées par Microsoft seront automatiquement ajoutées à la liste pour le type d'ouverture de session approprié.

- La [propriété de boîte aux lettres DefaultAuditSet](#checking-the-defaultauditset-property) sera mise à jour pour inclure le type d'ouverture de session approprié.

Pour restaurer les actions de boîte aux lettres par défaut pour tous les types d'ouverture de session, exécutez la commande suivante:

```
Set-Mailbox <username> -DefaultAuditSet Admin,Delegate,Owner
```

Vous pouvez utiliser cette commande pour restaurer les actions de boîte aux lettres par défaut pour tous les types d'ouverture de session (à l'aide des valeurs **admin**, **Delegate**ou **owner** pour le paramètre *DefaultAuditSet* .)

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>Désactiver l'audit des boîtes aux lettres par défaut pour votre organisation

Si, pour une raison quelconque, votre organisation décide qu'elle ne souhaite pas auditer les actions de boîte aux lettres, vous pouvez désactiver l'audit des boîtes aux lettres par défaut pour l'ensemble de votre organisation en exécutant la commande suivante dans Exchange Online PowerShell:

```
Set-OrganizationConfig -AuditDisabled $true
```

Lorsque l'audit de boîte aux lettres activé est désactivé par défaut (la propriété *AuditDisabled* est définie sur **true**) pour l'organisation, les événements suivants se produisent:

- L'audit des boîtes aux lettres est désactivé pour votre organisation.

- Aucune action de boîte aux lettres ne sera auditée (à partir du moment où l'audit est désactivé pour l'organisation), même si la propriété *AuditEnabled* d'une boîte aux lettres est définie sur **true**.

- L'audit des boîtes aux lettres n'est pas activé pour les nouvelles boîtes aux lettres et la définition de la propriété *AuditEnabled* sur une nouvelle boîte aux lettres (ou existante) sur **true** sera ignorée.

- Tout paramètre d'association de contournement d'audit de boîte aux lettres (configuré à l'aide de l'applet de commande **Set-MailboxAuditBypassAssociation** ) est ignoré.

- Les enregistrements d'audit de boîte aux lettres existants sont conservés jusqu'à l'expiration de la limite d'âge du journal d'audit de l'enregistrement.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>Activer l'audit de boîte aux lettres par défaut

Pour réactiver l'audit des boîtes aux lettres pour votre organisation, exécutez simplement la commande suivante dans Exchange Online PowerShell:

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>Contournement de l'enregistrement d'audit de boîte aux lettres

Actuellement, vous ne pouvez pas désactiver l'audit de boîte aux lettres pour des boîtes aux lettres spécifiques lorsque l'audit de boîte aux lettres activé par défaut est activé dans votre organisation. Par exemple, la définition de la propriété de boîte aux lettres *AuditEnabled* sur **false** est ignorée.  Toutefois, vous pouvez toujours utiliser la cmdlet **Set-MailboxAuditBypassAssociation** dans Exchange Online PowerShell pour empêcher la journalisation des actions de boîte aux lettres effectuées par des utilisateurs spécifiques. Lorsque vous contournez l'audit de boîte aux lettres, les actions de boîte aux lettres effectuées par un utilisateur spécifique ne sont pas auditées, quelle que soit la boîte aux lettres sur laquelle ces actions sont exécutées. Si vous ignorez l'audit des boîtes aux lettres pour un utilisateur spécifique, les actions du propriétaire de la boîte aux lettres effectuées par cet utilisateur ne seront pas consignées. Si ce même utilisateur se voit attribuer des autorisations sur la boîte aux lettres d'un autre utilisateur (ou une boîte aux lettres partagée), les actions de délégué effectuées par le premier utilisateur ne sont pas non plus consignées.

Pour contourner la journalisation d'audit de boîte aux lettres pour un utilisateur spécifique, exécutez la commande suivante:

```
Set-MailboxAuditBypassAssociation -Identity <username> -AuditByPassEnabled $true
```

Pour vérifier que l'audit est contourné pour l'utilisateur spécifié, exécutez la commande suivante:

```
Get-MailboxAuditBypassAssociation -Identity <username> | FL AuditByPassEnabled
```

La valeur **true** indique que l'enregistrement d'audit de boîte aux lettres est contourné pour cet utilisateur.

## <a name="mailbox-auditing-actions"></a>Actions d'audit de boîte aux lettres
  
Le tableau suivant récapitule les actions qui sont auditées pour chaque type d'ouverture de session de l'utilisateur. Dans le tableau, un astérisque ( **\*** ) indique que l'action est enregistrée par défaut. Un **non** indique qu'une action ne peut pas être enregistrée pour ce type d'ouverture de session. Notez qu'un administrateur disposant de l'autorisation accès total à la boîte aux lettres d'un utilisateur est considéré comme un utilisateur délégué. 
  
|**Action**|**Description**|**Administrateur**|**Délégué**|**Owner**|
|:-----|:-----|:-----|:-----|:-----|
|**Copier** <br/> |Un message a été copié dans un autre dossier.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Create** <br/> |Un élément est créé dans le dossier calendrier, contacts, notes ou tâches de la boîte aux lettres; par exemple, une nouvelle demande de réunion est créée. Notez que la création, l'envoi ou la réception d'un message n'est pas audité. En outre, la création d'un dossier de boîte aux lettres n'est pas auditée.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui  <br/> |
|**FolderBind**\** <br/> |Un utilisateur a accédé au dossier de boîte aux lettres. Cette action est également enregistrée lorsque l’administrateur ou un délégué ouvre la boîte aux lettres.  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|**HardDelete** <br/> |Un message a été purgé du dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**MailboxLogin** <br/> |L'utilisateur est connecté à sa boîte aux lettres.  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|**MessageBind**\*** <br/> |Un message a été affiché dans le volet de visualisation ou ouvert.  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|**Déplacer** <br/> |Un message a été déplacé vers un autre dossier.  <br/> |Oui  <br/> |Oui  <br/> |Oui  <br/> |
|**MoveToDeletedItems** <br/> |Un message a été supprimé et déplacé vers le dossier Éléments supprimés.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**SendAs** <br/> |Un message a été envoyé à l’aide de l’autorisation SendAs. Cela signifie qu’un autre utilisateur a envoyé le message comme s’il provenait du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Non  <br/> |
|**SendOnBehalf** <br/> |Un message a été envoyé à l’aide de l’autorisation SendOnBehalf. Cela signifie qu’un autre utilisateur a envoyé le message de la part du propriétaire de la boîte aux lettres. Le message indique au destinataire de la part de qui le message a été envoyé et qui a envoyé réellement le message.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Non  <br/> |
|**SoftDelete** <br/> |Un message a été définitivement supprimé ou supprimé (récupérable) du dossier Éléments supprimés. Les éléments supprimés récupérables sont déplacés vers le dossier Éléments récupérables.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**Update** <br/> |Un message ou ses propriétés ont été modifiés.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**UpdateCalendarDelegation** <br/> |Une délégation de calendrier a été affectée à une boîte aux lettres. La délégation de calendrier donne à une autre personne de l'Organisation des autorisations pour gérer le calendrier du propriétaire de la boîte aux lettres.  <br/> |Oui\*  <br/> |Non  <br/> |Oui\*  <br/> |
|**UpdateFolderPermissions** <br/> |Une autorisation de dossier a été modifiée. Les autorisations de dossier contrôlent les utilisateurs de votre organisation qui peuvent accéder aux dossiers d'une boîte aux lettres et aux messages qu'ils hébergent.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
|**UpdateInboxRules** <br/> |Une règle de boîte de réception a été ajoutée, supprimée ou modifiée. Les règles de boîte de réception sont utilisées pour traiter les messages dans la boîte de réception de l'utilisateur en fonction des conditions spécifiées et prendre des mesures lorsque les conditions d'une règle sont remplies, telles que le transfert d'un message vers un dossier spécifié ou la suppression d'un message.  <br/> |Oui\*  <br/> |Oui\*  <br/> |Oui\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Auditée par défaut lorsque l'audit de boîte aux lettres par défaut est activé pour le type d'ouverture de session. <br/><br/>  <sup>\*\*</sup>Les enregistrements d'audit pour les actions de liaison de dossiers effectuées par des délégués sont consolidés. Un enregistrement d'audit est généré pour l'accès à un dossier individuel dans un intervalle de temps de 24 heures. <br/><br/> L'action MessageBind a été déconseillée dans Exchange Online, et n'est plus disponible pour être ajoutée à la liste des actions de boîte aux lettres pour le type d'ouverture de session de l'administrateur. <sup> \* \* \* </sup> 

## <a name="more-information"></a>Plus d’informations

- Par défaut, les enregistrements du journal d'audit de boîte aux lettres sont conservés pendant 90 jours, puis supprimés. Vous pouvez modifier la limite d'âge des enregistrements du journal d'audit à l'aide de la commande **Set-Mailbox-AuditLogAgeLimit** dans Exchange Online PowerShell. Notez que l'augmentation de la limite d'âge par défaut pour les enregistrements d'audit de boîte aux lettres n'affecte pas la limite d'âge de 90 jours pour les enregistrements de journal d'audit de boîte aux lettres dans le journal d'audit de Microsoft 365. Par exemple, si vous augmentez la limite d'âge pour les enregistrements du journal d'audit de boîte aux lettres à 365 jours, un enregistrement d'audit de boîte aux lettres pourra faire l'objet d'une recherche dans le journal d'audit 365 de Microsoft pour 90 jours après l'événement correspondant. Dans ce cas, vous devez rechercher dans le journal d'audit de la boîte aux lettres de l'utilisateur des enregistrements datant de plus de 90 jours. Pour plus d'informations sur la recherche des journaux d'audit de boîte aux lettres, consultez la rubrique [Search-MailboxAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog).

- Si vous avez modifié la propriété *AuditLogAgeLimit* d'une boîte aux lettres avant que l'audit des boîtes aux lettres soit activé par défaut pour l'organisation, la limite d'âge de journal d'audit existante de cette boîte aux lettres ne sera pas modifiée; en d'autres termes, l'audit de boîte aux lettres sur par défaut n'a pas d'effet sur la limite d'âge actuelle pour les enregistrements d'audit de boîte aux lettres.

- Les enregistrements du journal d'audit de boîte aux lettres sont stockés ** dans un sous-dossier (nommé audits) dans le dossier éléments récupérables de la boîte aux lettres de chaque utilisateur. Gardez les points suivants à l'esprit concernant les enregistrements d'audit de boîte aux lettres et le dossier éléments récupérables.
   
    - Les enregistrements d'audit de boîte aux lettres comptent sur le quota de stockage du dossier éléments récupérables, qui est de 30 Go par défaut (le quota d'avertissement est de 20 Go). Notez que le quota de stockage pour le dossier éléments récupérables est automatiquement augmenté de 100 Go (quota d'avertissement de 90 Mo) lorsqu'une boîte aux lettres est placée sur une boîte aux lettres ou que la boîte aux lettres est affectée à une stratégie de rétention dans le centre de conformité.

    - Les enregistrements d'audit de boîte aux lettres comptent également sur la [limite de dossier pour le dossier éléments récupérables](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits). Le nombre maximal d'éléments (qui sont des enregistrements d'audit dans ce cas) qui peuvent être stockés dans le sous-dossier audits est de 3 millions éléments. 

      > [!NOTE]
      > Il est peu probable que l'audit de boîte aux lettres par défaut ait un impact sur le quota de stockage ou le nombre maximal de dossiers pour le dossier éléments récupérables. 

    - Vous pouvez exécuter la commande suivante dans Exchange Online PowerShell pour afficher la taille et le nombre d'éléments dans le sous-dossier audits du dossier éléments récupérables: 
       ```
       Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | FL FolderPath,FolderSize,ItemsInFolder
       ```

     - Vous ne pouvez pas accéder directement à un enregistrement de journal d'audit dans le dossier éléments récupérables; au lieu de cela, vous utilisez la cmdlet **Search-MailboxAuditLog** ou recherchez dans le journal d'audit de Microsoft 365 des enregistrements d'audit de boîte aux lettres.

- Si une boîte aux lettres est placée en conservation ou affectée à une stratégie de rétention dans le centre de conformité, les enregistrements du journal d'audit sont toujours conservés pendant la durée définie par la propriété *AuditLogAgeLimit* de la boîte aux lettres (qui est définie par défaut à 90 jours). Pour conserver les enregistrements du journal d'audit plus longtemps pour les boîtes aux lettres en attente, vous devez augmenter la période de rétention en augmentant la valeur de la propriété *AuditLogAgeLimit* .