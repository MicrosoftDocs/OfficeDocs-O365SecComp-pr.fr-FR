---
title: Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Après une boîte aux lettres Office 365 est inactive, vous pouvez modifier la durée de la suspension ou la stratégie de rétention Office 365 affecté à la boîte aux lettres inactive. La durée d’attente définit des éléments de la durée dans les éléments récupérables de conservation des dossiers.
ms.openlocfilehash: e3d1d6c7ec0311813dfa1144cc960d2fed9e160d
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038057"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a>Modifier la durée d’attente pour une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive est utilisée pour conserver l'e-mail d'un ancien employé une fois qu'il quitte votre organisation. Une boîte aux lettres devient inactive lorsqu'une conservation pour litige, une conservation inaltérable, une stratégie de rétention Office 365 ou une conservation associée à un cas eDiscovery est appliquée à la boîte aux lettres, et avant que le compte d'utilisateur Office 365 correspondant ne soit supprimé. Le contenu d'une boîte aux lettres inactive est conservé pendant la durée de la conservation appliquée à la boîte aux lettres avant qu'elle ne soit définie comme inactive. La durée de la conservation définit la durée de conservation des éléments dans le dossier Éléments récupérables. Lorsque la durée de conservation expire pour un élément du dossier Éléments récupérables, l'élément est supprimé définitivement (purgé) de la boîte aux lettres inactive. Une fois qu'une boîte aux lettres devient inactive, vous pouvez modifier la conservation ou la stratégie de rétention Office 365 affectée à la boîte aux lettres inactive.
  
> [!IMPORTANT]
> Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour modifier la durée de la suspension d’un litige sur une boîte aux lettres inactive. Vous ne pouvez pas utiliser le centre d’administration Exchange (CAE). Mais vous pouvez utiliser Exchange Online PowerShell ou le CAE pour modifier la durée de la suspension d’an In-Place Hold. Vous pouvez utiliser la sécurité de 365 Office &amp; centre de conformité ou de la sécurité &amp; PowerShell du centre de conformité pour modifier la durée d’attente pour une stratégie de rétention d’Office 365.
    
- Pour se connecter à Exchange Online PowerShell ou de sécurité &amp; PowerShell du centre de conformité, voir une des rubriques suivantes :
    
  - [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [Connexion au Centre de sécurité &amp; conformité Office 365 PowerShell](https://go.microsoft.com/fwlink/?linkid=799771)
    
- Notez que les conservations associées aux cas eDiscovery sont des conservations infinies, ce qui signifie qu'il n'existe aucune durée de conservation à modifier. Les éléments sont mis en conservation indéfiniment ou jusqu'à ce que la conservation et la boîte aux lettres inactive soient supprimées.
    
- Pour plus d’informations sur les boîtes aux lettres inactives, voir [boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Étape 1 : Identifier les blocages sur une boîte aux lettres inactive

Étant donné que différents types de conservations ou une ou plusieurs stratégies de rétention Office 365 peuvent figurer dans une boîte aux lettres inactive, la première étape consiste à identifier les conservations sur une boîte aux lettres inactive.
  
Exécutez la commande suivante dans Exchange Online PowerShell pour afficher les informations de conservation pour toutes les boîtes aux lettres inactives dans votre organisation.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
La valeur **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est litige. Si une conservation inaltérable, maintenez la touche eDiscovery ou stratégie de rétention Office 365 est placée sur une boîte aux lettres inactive, un GUID de la stratégie de blocage ou de rétention s’affiche comme valeur de la propriété **InPlaceHolds** . Par exemple, voici les résultats pour les boîtes aux lettres inactives 5. 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
Le tableau suivant indique les cinq différents types de conservations qui ont été utilisés pour chaque boîte aux lettres inactive.
  
|**Boîte aux lettres inactive**|**Type de conservation**|**Comment identifier la conservation dans la boîte aux lettres inactive**|
|:-----|:-----|:-----|
|Ann Beebe  <br/> |Conservation pour litige  <br/> |La propriété  *LitigationHoldEnabled*  est définie sur  `True`.  <br/> |
|Pilar Pinilla  <br/> |Conservation inaltérable  <br/> |La propriété  *InPlaceHolds*  contient le GUID de la conservation inaltérable appliquée à la boîte aux lettres inactive. Vous pouvez déterminer qu'il s'agit d'une conservation inaltérable, car l'ID ne commence pas par un préfixe.  <br/> Vous pouvez utiliser la commande  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` dans Exchange Online PowerShell pour obtenir des informations sur la conservation inaltérable dans la boîte aux lettres inactive.  <br/> |
|Mario Necaise  <br/> |Stratégie de rétention d’Office 365 à l’échelle de l’organisation de la sécurité &amp; centre de conformité  <br/> |La propriété *InPlaceHolds* est vide. Cela indique qu’un ou plusieurs (Exchange échelle) ou à l’échelle de l’organisation Office 365 stratégie de rétention est appliquée à la boîte aux lettres inactive. Dans ce cas, vous pouvez exécuter le « Get-OrganizationConfig | Select-Object - ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nom FL'<br/><br/>
|Carol Olson  <br/> |Stratégie de rétention Office 365 dans la sécurité &amp; centre de conformité appliquée aux boîtes aux lettres spécifiques  <br/> |La propriété  *InPlaceHolds*  contient le GUID de la stratégie de rétention Office 365 qui est appliqué à la boîte aux lettres inactive. Vous pouvez déterminer qu'il s'agit d'une stratégie de rétention qui est appliquée à des boîtes aux lettres spécifiques, car le GUID commence par le préfixe  `mbx`. Notez que si le GUID de la stratégie de rétention appliquée à la boîte aux lettres inactive commence par le préfixe  `skp`, cela indique que la stratégie de rétention est appliquée à des conversations Skype Entreprise.  <br/><br/> À la stratégie de rétention identité Office 365 qui est appliqué à la boîte aux lettres inactive, exécutez la commande suivante dans la sécurité &amp; PowerShell du centre de conformité.<br/><br/> « Get-RetentionCompliancePolicy<retention policy GUID without prefix> | Nom FL` <br/><br/>Be sure to remove the  `mbx` or  `skp' préfixe lorsque vous exécutez cette commande.  <br/> |
|Abraham McMahon  <br/> |blocage de cas de découverte électronique dans la sécurité &amp; centre de conformité  <br/> |La propriété  *InPlaceHolds*  contient le GUID de la conservation du cas eDiscovery qui figure dans la boîte aux lettres inactive. Vous pouvez déterminer qu'il s'agit d'une mise en conservation de cas eDiscovery, car le GUID commence par le préfixe  `UniH`.  <br/> Vous pouvez utiliser la `Get-CaseHoldPolicy` applet de commande de la sécurité &amp; PowerShell du centre de conformité pour obtenir des informations sur le cas de découverte électronique qui est associée à la suspension de la boîte aux lettres inactive. Par exemple, vous pouvez exécuter la commande « Get-CaseHoldPolicy<hold GUID without prefix> | Nom FL` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/> `$CaseHold.CaseId Get-ComplianceCase | Nom FL'<br/><br/><br/> **Remarque :** Nous ne recommandons pas à l’aide de la découverte électronique conserve de boîtes aux lettres inactives. C’est parce que cas eDiscovery sont destinés aux cas liés au temps spécifiques liées à un problème juridique. Dans certains cas, une affaire juridique se termine sans doute et la suspension associée au cas sera supprimée et le cas de découverte électronique sera fermé (ou supprimé). En fait, si une suspension est placée sur une boîte aux lettres inactive est associée à un cas eDiscovery et le blocage est terminé ou le cas de découverte électronique est fermé ou supprimé, la boîte aux lettres inactive est définitivement supprimé. 

Pour plus d’informations sur les stratégies de rétention Office 365, voir [vue d’ensemble des stratégies de rétention](retention-policies.md).
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>Étape 2 : Modifier la durée de la conservation pour une boîte aux lettres inactive

Après avoir identifié le type de conservation placé sur la boîte aux lettres inactive (et s'il y a plusieurs conservations), l'étape suivante consiste à modifier la durée de la conservation. 
  
### <a name="change-the-duration-for-a-litigation-hold"></a>Modifier la durée pour une conservation pour litige

Voici comment utiliser Exchange Online PowerShell pour modifier la durée de la conservation pour litige appliquée à une boîte aux lettres inactive. Vous ne pouvez pas utiliser le CAE. Exécutez la commande suivante pour modifier la durée de la conservation. Dans cet exemple, la durée de la conservation est modifiée pendant une période illimitée.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

Les éléments de la boîte aux lettres inactive sont alors conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée ou que la durée de la conservation soit remplacée par une autre valeur.
  
> [!TIP]
> La meilleure façon d'identifier une boîte aux lettres inactive est d'utiliser sa valeur **Distinguished Name** ou **Exchange GUID**. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres. 
  
### <a name="change-the-duration-for-an-in-place-hold"></a>Modifier la durée pour une conservation inaltérable

 Vous pouvez utiliser le CAE ou Exchange Online PowerShell pour modifier la durée d'une conservation inaltérable. 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a>Utiliser le CAE pour modifier la durée de la conservation

1. Si vous connaissez le nom de la conservation inaltérable que vous souhaitez modifier, accédez à l’étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom de la conservation inaltérable qui est placé sur la boîte aux lettres inactive. Utilisez le GUID In-Place Hold que vous avez obtenu à [l’étape 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.
    
3. Sélectionnez la In-Place Hold vous souhaitez modifier, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Sur le **In-Place eDiscovery &amp; attente** propriétés, cliquez sur le **Blocage sur Place**. 
    
5. Effectuez l'une des opérations suivantes sur la durée de la conservation actuelle :
    
1. Cliquez sur **Bloquer indéfiniment** pour bloquer les éléments pendant une période illimitée. 
    
2. Cliquez sur **spécifier nombre de jours pendant lesquels conserver les éléments par rapport à leur date de réception** pour contenir les éléments pour une période spécifique. Tapez le nombre de jours pendant lesquels vous souhaitez bloquer les éléments. 
    
    ![Capture d'écran de la modification de la durée d'une conservation inaltérable](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. Cliquez sur **Enregistrer**.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Utiliser Exchange Online PowerShell pour modifier la durée de conservation

1. Si vous connaissez le nom de la conservation inaltérable que vous souhaitez modifier, accédez à l’étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom de la conservation inaltérable qui est placé sur la boîte aux lettres inactive. Utilisez le GUID In-Place Hold que vous avez obtenu à [l’étape 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. Exécutez la commande suivante pour modifier la durée du blocage. Dans cet exemple, la durée de la conservation est devenue 2 555 jours (environ 7 ans). 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     Pour modifier la durée de la conservation sur une période illimitée, utilisez  _-ItemHoldPeriod unlimited_.
  
## <a name="more-information"></a>Plus d’informations

- **Comment la durée de la conservation est-elle calculée pour un élément dans une boîte aux lettres inactive ?** La durée est calculée à partir de la date de réception ou de création d'origine d'un élément de boîte aux lettres. 
    
- **Que se passe-t-il lorsque la durée de la conservation arrive à expiration ?** Lorsque la durée de la conservation arrive à expiration pour un élément de boîte aux lettres dans le dossier Éléments récupérables, l'élément est supprimé définitivement (purgé) de la boîte aux lettres inactive. S'il n'existe aucune durée spécifiée pour la conservation placée sur la boîte aux lettres inactive, les éléments du dossier Éléments récupérables ne sont jamais supprimés définitivement (sauf si la durée de la conservation de la boîte aux lettres inactive est modifiée). 
    
- **Une stratégie de rétention Exchange est-elle toujours traitée sur les boîtes aux lettres inactives ?** Si une stratégie de rétention Exchange (la fonctionnalité de gestion des enregistrements de messagerie, ou MRM, dans Exchange Online) a été appliquée à une boîte aux lettres lorsqu'elle est devenue inactive, les stratégies de suppression (qui sont des balises de rétention configurées avec une action de rétention **Delete** ) continueront à être traitées sur la boîte aux lettres inactive. Cela signifie que les éléments marqués avec une stratégie de suppression sont déplacés vers le dossier Éléments récupérables à l'expiration de la période de rétention. Ces éléments sont supprimés définitivement de la boîte aux lettres inactive à l'expiration de la durée de la conservation d'un élément. 
    
    À l'inverse, les stratégies d'archivage (qui sont des balises de rétention configurées avec une action de rétention **MoveToArchive** ) incluses dans la stratégie de rétention attribuée à une boîte aux lettres inactive sont ignorées. Cela signifie que les éléments dans une boîte aux lettres inactive qui sont marqués avec une stratégie d'archivage restent dans la boîte aux lettres principale à l'expiration de la période de rétention. Ils ne sont pas déplacés vers la boîte aux lettres d'archivage ni vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage. Étant donné qu'un utilisateur ne peut pas se connecter à une boîte aux lettres inactive, il est inutile d'utiliser des ressources du centre de données pour traiter des stratégies d'archivage. 
    
- **Pour vérifier la nouvelle durée de la conservation, exécutez l'une des commandes suivantes.** La première commande est pour Conservation pour litige et la seconde est pour Conservation inaltérable. 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- **Comme les boîtes aux lettres ordinaires, l'Assistant Dossier géré traite également les boîtes aux lettres inactives.** Dans Exchange Online, l'Assistant Dossier géré traite les boîtes aux lettres environ tous les 7 jours. Après avoir modifié la durée de la conservation pour une boîte aux lettres inactive, vous pouvez utiliser la cmdlet **Start-ManagedFolderAssistant** pour démarrer immédiatement le traitement de la nouvelle durée de la conservation pour la boîte aux lettres inactive. Exécutez la commande suivante. 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- **Si un grand nombre de conservations sont appliquées à une boîte aux lettres inactive, l'ensemble des GUID de suspension ne sera pas affiché.** Vous pouvez exécuter la commande suivante pour afficher les GUID pour toutes les conservations (sauf pour les conservations pour litige) qui figurent dans une boîte aux lettres inactive. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
