---
title: Modifier la durée de la conservation pour une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Une fois qu’une boîte aux lettres Office 365 est devenue inactive, vous pouvez modifier la durée de la conservation ou de la stratégie de rétention d’Office 365 affectée à la boîte aux lettres inactive. La durée de la conservation définit la durée de conservation des éléments dans le dossier Éléments récupérables.
ms.openlocfilehash: 7840131af3df32b8b8e5a0faa1b101f9ec8ef541
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155566"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a>Modifier la durée de la conservation pour une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive est utilisée pour conserver l'e-mail d'un ancien employé une fois qu'il quitte votre organisation. Une boîte aux lettres devient inactive lorsqu'une conservation pour litige, une conservation inaltérable, une stratégie de rétention Office 365 ou une conservation associée à un cas eDiscovery est appliquée à la boîte aux lettres, et avant que le compte d'utilisateur Office 365 correspondant ne soit supprimé. Le contenu d'une boîte aux lettres inactive est conservé pendant la durée de la conservation appliquée à la boîte aux lettres avant qu'elle ne soit définie comme inactive. La durée de la conservation définit la durée de conservation des éléments dans le dossier Éléments récupérables. Lorsque la durée de conservation expire pour un élément du dossier Éléments récupérables, l'élément est supprimé définitivement (purgé) de la boîte aux lettres inactive. Une fois qu'une boîte aux lettres devient inactive, vous pouvez modifier la conservation ou la stratégie de rétention Office 365 affectée à la boîte aux lettres inactive.
  
> [!IMPORTANT]
> Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
## <a name="before-you-begin"></a>Avant de commencer

- You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. Vous pouvez utiliser le centre de sécurité et de conformité ou le centre de sécurité & Compliance Center PowerShell pour modifier la durée de la conservation pour une stratégie de rétention Office 365.
    
- Pour vous connecter à Exchange Online PowerShell ou le centre de sécurité & conformité PowerShell, consultez l’une des rubriques suivantes:
    
  - [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [Se connecter au centre de conformité Office 365 Security& PowerShell](https://go.microsoft.com/fwlink/?linkid=799771)
    
- Notez que les conservations associées aux cas eDiscovery sont des conservations infinies, ce qui signifie qu'il n'existe aucune durée de conservation à modifier. Les éléments sont mis en conservation indéfiniment ou jusqu'à ce que la conservation et la boîte aux lettres inactive soient supprimées.
    
- Pour plus d’informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Étape 1 : Identifier les blocages sur une boîte aux lettres inactive

Étant donné que différents types de conservations ou une ou plusieurs stratégies de rétention Office 365 peuvent figurer dans une boîte aux lettres inactive, la première étape consiste à identifier les conservations sur une boîte aux lettres inactive.
  
Exécutez la commande suivante dans Exchange Online PowerShell pour afficher les informations de conservation pour toutes les boîtes aux lettres inactives dans votre organisation.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
La valeur de **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est en conservation pour litige. Si une conservation inaltérable, une conservation eDiscovery ou une stratégie de rétention Office 365 est appliquée à une boîte aux lettres inactive, un GUID pour la conservation ou la stratégie de rétention est affiché en tant que valeur pour la propriété **InPlaceHolds**. Par exemple, le code suivant montre les résultats pour 5 boîtes aux lettres inactives. 
  
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
|Mario Necaise  <br/> |Stratégie de rétention Office 365 à l’échelle de l’organisation dans le centre de sécurité & Compliance Center  <br/> |La propriété  *InPlaceHolds*  est vide. Cela indique qu'une ou plusieurs stratégies de rétention Office 365 (à l'échelle d'Exchange) ou à l'échelle de l'organisation sont appliquées à la boîte aux lettres inactive. Dans ce cas, vous pouvez exécuter la commande  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> <br/>Pour identifier la stratégie de rétention Office 365 qui est appliquée à la boîte aux lettres inactive, exécutez la commande suivante dans Security & Compliance Center PowerShell.  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|Carol Olson  <br/> |Stratégie de rétention Office 365 dans le centre de sécurité & conformité appliquée à des boîtes aux lettres spécifiques  <br/> |La propriété  *InPlaceHolds*  contient le GUID de la stratégie de rétention Office 365 qui est appliqué à la boîte aux lettres inactive. Vous pouvez déterminer qu'il s'agit d'une stratégie de rétention qui est appliquée à des boîtes aux lettres spécifiques, car le GUID commence par le préfixe  `mbx`. Notez que si le GUID de la stratégie de rétention appliquée à la boîte aux lettres inactive commence par le préfixe  `skp`, cela indique que la stratégie de rétention est appliquée à des conversations Skype Entreprise.  <br/><br/> Pour identifier la stratégie de rétention Office 365 qui est appliquée à la boîte aux lettres inactive, exécutez la commande suivante dans Security & Compliance Center PowerShell.<br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/>N'oubliez pas de supprimer le préfixe  `mbx` ou  `skp` lorsque vous exécutez cette commande.  <br/> |
|Abraham McMahon  <br/> |conservation des cas eDiscovery dans le centre de sécurité & Compliance Center  <br/> |La propriété  *InPlaceHolds*  contient le GUID de la conservation du cas eDiscovery qui figure dans la boîte aux lettres inactive. Vous pouvez déterminer qu'il s'agit d'une mise en conservation de cas eDiscovery, car le GUID commence par le préfixe  `UniH`.  <br/> Vous pouvez utiliser l' `Get-CaseHoldPolicy` applet de commande dans Security _AMP_ Compliance Center PowerShell pour obtenir des informations sur le cas eDiscovery auquel est associée la conservation de la boîte aux lettres inactive. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` lorsque vous exécutez cette commande.  <br/><br/> Pour identifier le cas eDiscovery associé à la conservation dans la boîte aux lettres inactive, exécutez les commandes suivantes.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> **Remarque:** Il n’est pas recommandé d’utiliser des suspensions eDiscovery pour les boîtes aux lettres inactives. En effet, les cas eDiscovery sont destinés à cas spécifiques, limités dans le temps et liés à un problème juridique. À un moment ou un autre, un dossier juridique se terminera probablement, et les conservations associées au cas seront supprimées et le cas eDiscovery sera fermé (ou supprimé). En fait, si une conservation figurant dans une boîte aux lettres inactive est associée à un cas eDiscovery et que la conservation est libérée, ou le cas eDiscovery est fermé ou supprimé, la boîte aux lettres inactive est définitivement supprimée. 

Pour plus d’informations sur les stratégies de rétention Office 365, voir [Overview of](retention-policies.md)Retention Policies.
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>Étape 2 : Modifier la durée de la conservation pour une boîte aux lettres inactive

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

1. Si vous connaissez le nom de la conservation inaltérable que vous souhaitez modifier, passez à l'étape suivante. Sinon, exécutez la commande suivante pour obtenir le nom de la conservation inaltérable placée sur la boîte aux lettres inactive. Utilisez le GUID de conservation inaltérable que vous avez obtenu à l' [étape 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
3. Sélectionnez la conservation inaltérable à modifier, puis cliquez sur **modifier** ![l’icône](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)modifier.
    
4. On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**. 
    
5. Effectuez l'une des opérations suivantes sur la durée de la conservation actuelle :
    
1. Cliquez sur **Bloquer indéfiniment** pour bloquer les éléments pendant une période illimitée. 
    
2. Cliquez sur **spécifier le nombre de jours de conservation des éléments par rapport à leur date de réception** pour conserver les éléments d’une période donnée. Type the number of days that you want to hold items for. 
    
    ![Capture d'écran de la modification de la durée d'une conservation inaltérable](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. Cliquez sur **Enregistrer**.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Utiliser Exchange Online PowerShell pour modifier la durée de conservation

1. Si vous connaissez le nom de la conservation inaltérable que vous souhaitez modifier, passez à l’étape suivante. Sinon, exécutez la commande suivante pour obtenir le nom de la conservation inaltérable placée sur la boîte aux lettres inactive. Utilisez le GUID de conservation inaltérable que vous avez obtenu à l' [étape 1](#step-1-identify-the-holds-on-an-inactive-mailbox).

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
