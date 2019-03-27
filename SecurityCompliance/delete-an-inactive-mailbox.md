---
title: Supprimer une boîte aux lettres inactive dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: Lorsque vous n'avez plus besoin de conserver le contenu d'une boîte aux lettres Office 365 inactive, vous pouvez supprimer définitivement la boîte aux lettres inactive en supprimant la conservation. Après avoir supprimé la conservation, la boîte aux lettres inactive est marquée pour suppression et est définitivement supprimée après traitement.
ms.openlocfilehash: 51f3181e77db2f36976f01f349f1c628f1e67bcf
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30899983"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a>Supprimer une boîte aux lettres inactive dans Office 365

Une boîte aux lettres inactive est utilisée pour conserver le courrier électronique d'un ancien employé une fois qu'il quitte votre organisation. Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez le supprimer de façon définitive en supprimant le blocage. En outre, il est possible que plusieurs blocages soient placés sur une boîte aux lettres inactive. Par exemple, une boîte aux lettres inactive peut être placée en suspension pour litige et sur une ou plusieurs blocages sur place. De plus, une stratégie de rétention Office 365 (créée dans le &amp; Centre de sécurité conformité d'Office 365) peut être appliquée à la boîte aux lettres inactive. Vous devez supprimer toutes les conservations et les stratégies de rétention d'Office 365 d'une boîte aux lettres inactive pour les supprimer. Une fois que vous avez supprimé les suspensions et les stratégies de rétention, la boîte aux lettres inactive est marquée pour suppression et est définitivement supprimée après traitement.
  
> [!IMPORTANT]
> Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable. 
  
Consultez la section [Plus d'informations](#more-information) pour obtenir une description de ce qui se produit après la suppression des blocages d'une boîte aux lettres inactive. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser Exchange Online PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive. Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE). Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Vous pouvez utiliser Exchange Online PowerShell ou le centre d'administration Exchange pour supprimer un blocage sur place d'une boîte aux lettres inactive. 
    
- Vous pouvez copier le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres avant de supprimer la conservation et de supprimer une boîte aux lettres inactive. Pour plus d'informations, consultez la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).
    
- Si vous supprimez la conservation ou la stratégie de rétention Office 365 d'une boîte aux lettres inactive et que la période de rétention de boîte aux lettres supprimée (récupérable) pour la boîte aux lettres a expiré, la boîte aux lettres sera définitivement supprimée. Après sa suppression, elle ne peut pas être récupérée. Avant de supprimer la conservation, vérifiez que vous n'avez plus besoin du contenu de la boîte aux lettres. Si vous souhaitez réactiver une boîte aux lettres inactive, vous pouvez la récupérer. Pour plus d'informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
- Pour plus d'informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Étape 1 : Identifier les blocages sur une boîte aux lettres inactive

Comme indiqué précédemment, une stratégie de rétention de conservation pour litige, conservation inaltérable ou Office 365 peut être placée sur une boîte aux lettres inactive. La première étape consiste à identifier les blocages sur une boîte aux lettres inactive.
  
Exécutez la commande suivante pour afficher les informations de blocage pour toutes les boîtes aux lettres inactives dans votre organisation.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

La valeur de **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est en suspension pour litige. Si un blocage sur place est placé sur une boîte aux lettres inactive, le GUID du blocage s'affiche comme valeur pour la propriété **InPlaceHolds**. Par exemple, les résultats suivants pour deux boîtes aux lettres inactives affichent qu'une suspension pour litige est placée sur Ann Beebe et que deux blocages sur place sont placés sur Pilar Pinilla. 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> Si un grand nombre de blocages sur place est placé sur une boîte aux lettres inactive, tous les GUID de blocage sur place ne seront pas affichés. Vous pouvez exécuter la commande suivante pour afficher tous les GUID de conservation inaltérable:`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a>Étape 2 : Supprimer une blocage d'une boîte aux lettres inactive

Après avoir identifié le type de blocage placé sur la boîte aux lettres inactive (et s'il y a plusieurs blocages), l'étape suivante consiste à supprimer les blocages sur la boîte aux lettres. Comme indiqué précédemment, vous devez supprimer tous les blocages pour supprimer définitivement une boîte aux lettres inactive. 
  
### <a name="remove-a-litigation-hold"></a>Supprimer une suspension pour litige

Comme indiqué précédemment, vous devez utiliser Windows PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive. Vous ne pouvez pas utiliser le CAE. Exécutez la commande suivante pour supprimer une suspension pour litige.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> La meilleure façon d'identifier une boîte aux lettres inactive est d'utiliser son nom unique ou sa valeur GUID Exchange. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres. 
  
### <a name="remove-in-place-holds"></a>Supprimer des blocages sur place

 Il existe deux façons de supprimer un blocage sur place à partir d'une boîte aux lettres inactive : 
  
- **Supprimer l'objet de conservation** inaltérable Si la boîte aux lettres inactive que vous souhaitez supprimer définitivement est la seule boîte aux lettres source pour une conservation inaltérable, vous pouvez simplement supprimer l'objet de blocage sur place. 
    
    > [!NOTE]
    > Vous devez désactiver le blocage avant de pouvoir supprimer un objet de blocage sur place. Si vous essayez de supprimer un objet de blocage sur place ayant le blocage activé, vous recevrez un message d'erreur. 
  
- **Supprimer la boîte aux lettres inactive comme boîte aux lettres source d'une conservation inaltérable** Si vous souhaitez conserver d'autres boîtes aux lettres sources pour une conservation inaltérable, vous pouvez supprimer la boîte aux lettres inactive de la liste des boîtes aux lettres sources et conserver l'objet de conservation inaltérable. 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a>Utiliser le Centre d'administration Exchange (CAE) pour supprimer un blocage sur place

1. Si vous connaissez le nom du blocage sur place à supprimer, vous pouvez passer à l'étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom du blocage sur place placé sur la boîte aux lettres inactive que vous souhaitez supprimer définitivement. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
3. Sélectionnez la conservation inaltérable à supprimer, puis cliquez sur **modifier** ![l'icône](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)modifier.
    
4. On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.
    
5. On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).
    
6. Dans le message d'avertissement, cliquez sur **Oui** pour supprimer le blocage sur place. 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a>Utiliser Exchange Online PowerShell pour supprimer une conservation inaltérable

1. Créez une variable qui contient les propriétés du blocage sur place à supprimer. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Désactivez le blocage sur le blocage sur place.
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. Supprimez le blocage sur place.
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Utilisez le CAE pour supprimer une boîte aux lettres inactive d'un blocage sur place

1. Si vous connaissez le nom du blocage sur place placé sur la boîte aux lettres inactive, vous pouvez passer à l'étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom du blocage sur place placé sur la boîte aux lettres. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
3. Sélectionnez le blocage sur place placé sur la boîte aux lettres inactive, puis cliquez sur **modifier** ![l'icône](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)modifier.
    
4. On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.
    
5. Dans la liste des boîtes aux lettres source, cliquez sur le nom de la boîte aux lettres inactive à supprimer, puis cliquez sur **Supprimer**![Icône Suppression](media/adf01106-cc79-475c-8673-065371c1897b.gif).
    
6. Cliquez sur **Enregistrer** pour enregistrer la modification. Un message s'affiche indiquant que l'opération a réussi. 
    
7. Répétez les étapes 1 à 6 pour supprimer d'autres blocages sur place placés sur la boîte aux lettres inactive.
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Utiliser Exchange Online PowerShell pour supprimer une boîte aux lettres inactive d'une conservation inaltérable

Si le blocage sur place contient un grand nombre de boîtes aux lettres source, il est possible que la boîte aux lettres inactive ne soit pas répertoriée sur la page **Sources** dans le CAE. Jusqu'à 3 000 boîtes aux lettres s'affichent sur la page **Sources** lorsque vous modifiez un blocage sur place. Si une boîte aux lettres inactive n'est pas affichée sur la page **sources** , vous pouvez utiliser Exchange Online PowerShell pour la supprimer de la conservation inaltérable. 
  
1. Créez une variable qui contient les propriétés du blocage sur place placé sur la boîte aux lettres inactive. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Vérifiez que la boîte aux lettres inactive est répertoriée comme une boîte aux lettres source pour le blocage sur place. 
    
```
  $InPlaceHold.Sources
```

   **Remarque:** La propriété *sources* de la conservation inaltérable identifie les boîtes aux lettres source en fonction de leurs propriétés *legacyExchangeDN* . Étant donné que cette propriété identifie les boîtes aux lettres inactives de façon unique, l'utilisation de la propriété *Sources* du blocage sur place permet d'empêcher la suppression de la boîte aux lettres incorrecte. Cela permet également d'éviter les problèmes si deux boîtes aux lettres ont le même alias ou la même adresse SMTP. 
   
3. Supprimez la boîte aux lettres inactive dans la liste des boîtes aux lettres sources dans la variable. Veillez à utiliser le **LegacyExchangeDN** de la boîte aux lettres inactive qui est renvoyé par la commande à l'étape précédente. 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source dans la variable.
    
```
  $InPlaceHold.Sources
```

5. Modifiez le blocage sur place avec la liste mise à jour des boîtes aux lettres source, qui n'inclut pas la boîte aux lettres inactive.
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source pour le blocage sur place.
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a>Plus d’informations

- **Une boîte aux lettres inactive est un type de boîte aux lettres supprimée (récupérable).** Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée. 
    
- **Que se passe-t-il après avoir supprimé la conservation sur une boîte aux lettres inactive ?** La boîte aux lettres est traitée comme d'autres boîtes aux lettres supprimées (récupérables) et est marquée pour suppression définitive après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable) de 30 jours. Ce délai de rétention commence à la date à laquelle la boîte aux lettres a été rendue inactive pour la première fois. Cette date est appelée la date supprimée (récupérable), qui représente la date de suppression du compte utilisateur Office 365 correspondant ou la date de suppression de la boîte aux lettres Exchange Online avec la cmdlet **Remove-Mailbox**. La date supprimée (récupérable) n'est pas la date de suppression du blocage. 
    
- **Une boîte aux lettres inactive est-elle définitivement supprimée immédiatement après la suppression de la conservation ?** Si la date supprimée (récupérable) pour une boîte aux lettres inactive est de plus de 30 jours, la boîte aux lettres n'est pas supprimée définitivement dès que vous supprimez la conservation. La boîte aux lettres sera marquée pour suppression définitive et sera supprimée lors de son prochain traitement. 
    
- **Quel est l'impact de la période de rétention de la boîte aux lettres supprimée (récupérable) sur les boîtes aux lettres inactives ?** Si la date supprimée (récupérable) pour une boîte aux lettres inactive se situe plus de 30 jours avant la date de la suppression de la conservation, la boîte aux lettres est marquée pour suppression définitive. Par contre, si la date supprimée (récupérable) d'une boîte aux lettres inactive se situe dans les 30 derniers jours et que vous supprimez la conservation, vous pouvez récupérer la boîte aux lettres jusqu'à l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable). Pour plus d'informations, consultez la rubrique [supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). Après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable), vous devez suivre les procédures de récupération d'une boîte aux lettres inactive. Pour plus d'informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).
    
- **Comment afficher des informations sur une boîte aux lettres inactive après la suppression de la conservation ?** Après la suppression d'une conservation et la restauration de la boîte aux lettres inactive vers une boîte aux lettres supprimée (récupérable), elle n'est pas renvoyée à l'aide du paramètre *InactiveMailboxOnly* avec la cmdlet **Get-Mailbox** . Cependant, vous pouvez afficher des informations sur la boîte aux lettres à l'aide de la commande **Get-Mailbox -SoftDeletedMailbox**. Par exemple : 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
Dans l'exemple ci-dessus, la propriété *WhenSoftDeleted* identifie la date supprimée (récupérable), qui, dans cet exemple, est le 30 octobre 2014. Si cette boîte aux lettres supprimée (récupérable) était auparavant une boîte aux lettres inactive pour laquelle la conservation a été supprimée, elle sera définitivement supprimée 30 jours après la valeur de la propriété *WhenSoftDeleted* . Dans ce cas, la boîte aux lettres est définitivement supprimée après le 30 novembre 2014.

