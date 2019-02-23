---
title: Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.
ms.openlocfilehash: 70feb265e95741406dbf170c6be70bd83b2ec081
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223523"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online

Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.
  
> [!NOTE]
> Nous avons repoussé la date d'échéance pour la création de nouvelles conservations inaltérables dans Exchange Online (dans Office 365 et les offres Exchange Online autonomes). Mais plus tard cette année ou l'année prochaine, vous ne serez pas en mesure de créer de nouvelles conservations inaltérables dans Exchange Online. En guise d'alternative à l'utilisation des conservations inaltérables, vous pouvez utiliser des [cas eDiscovery](https://go.microsoft.com/fwlink/?linkid=780738) ou des [stratégies](https://go.microsoft.com/fwlink/?linkid=827811) de rétention dans le centre de sécurité &amp; conformité Office 365. Après avoir mis hors service les nouvelles conservations inaltérables, vous pourrez toujours modifier les conservations inaltérables existantes et créer de nouvelles conservations inaltérables dans Exchange Server 2013 et les déploiements hybrides Exchange seront toujours pris en charge. De plus, vous pourrez toujours placer des boîtes aux lettres en conservation pour litige. 
  
Vous avez peut-être une situation dans laquelle une personne a quitté votre organisation, et son compte d'utilisateur et sa boîte aux lettres correspondants ont été supprimés. Ensuite, vous réalisez des informations dans la boîte aux lettres qui doivent être conservées. Que pouvez-vous faire? Si la période de rétention de boîte aux lettres supprimée n'a pas expiré, vous pouvez placer une conservation inaltérable dans la boîte aux lettres supprimée (appelée boîte aux lettres supprimée (récupérable)) et la transformer en boîte aux lettres inactive. Une *boîte aux lettres inactive* est utilisée pour conserver le courrier d'un ancien employé une fois qu'il quitte votre organisation. Le contenu d'une boîte aux lettres inactive est conservé pendant la durée de la conservation inaltérable qui a été placée sur la boîte aux lettres supprimée (récupérable) lorsqu'elle est devenue inactive. Une fois la boîte aux lettres inactive, vous pouvez effectuer une recherche dans la boîte aux lettres en utilisant la découverte électronique inaltérable dans Exchange Online, la &amp; recherche de contenu dans le centre de sécurité conformité Office 365 ou le centre EDiscovery dans SharePoint Online. 
  
> [!NOTE]
> Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée (ou rendue inactive) dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée ou rendue inactive. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez utiliser l'applet de commande **New-MailboxSearch** dans Windows PowerShell pour placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable). Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE) ni le centre de découverte électronique SharePoint Online. 
    
- Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Exécutez la commande suivante pour obtenir les informations d'identité sur les boîtes aux lettres supprimées (récupérables) de votre organisation. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Pour plus d'informations sur les boîtes aux lettres inactives, consultez la rubrique [vue d'ensemble des boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable) pour rendre la boîte aux lettres inactive

Utilisez l'applet de commande **New-MailboxSearch** pour rendre inactive une boîte aux lettres supprimée (récupérable). Pour plus d'informations, voir [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).
  
1. Créez une variable contenant les propriétés de la boîte aux lettres supprimée (récupérable). 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGuid** pour identifier la boîte aux lettres supprimée (récupérable). Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres supprimée (récupérable) peuvent avoir la même adresse SMTP principale. 
  
2. Créez une conservation inaltérable et placez-la sur la boîte aux lettres supprimée (récupérable). Dans cet exemple, aucune durée de suspension n’est spécifiée. Cela signifie que les éléments seront suspendus indéfiniment ou jusqu’à ce que la suspension soit supprimée de la boîte aux lettres inactive.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   Vous pouvez également spécifier une durée de suspension lorsque vous créez la conservation inaltérable. Cet exemple conserve des éléments de la boîte aux lettres inactive pendant environ sept ans.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. Après un certain temps, exécutez l’une des commandes suivantes pour vérifier que la boîte aux lettres supprimée (récupérable) est une boîte aux lettres inactive.
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    Ou
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a>Plus d’informations

Une fois la boîte aux lettres supprimée (récupérable) devenue inactive, il existe plusieurs façons de gérer la boîte aux lettres. Pour plus d'informations, voir :
  
- [Modifier la durée de conservation pour une boîte aux lettres inactive](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [Récupérer une boîte aux lettres inactive](recover-an-inactive-mailbox.md)
    
- [Restaurer une boîte aux lettres inactive](restore-an-inactive-mailbox.md)
    
- [Supprimer une boîte aux lettres inactive](delete-an-inactive-mailbox.md) (en supprimant la conservation)
