---
title: Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.
ms.openlocfilehash: b4ef4ee26e98c8234f64d0879391f8fec89ffd3c
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038247"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online

Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.
  
> [!NOTE]
> Nous avons retardée de la date d’échéance 1 juillet 2017 pour créer de nouvelles archives permanentes dans Exchange en ligne (dans les plans autonomes Office 365 et Exchange Online). Mais cette année ou le début d’année, vous ne pourrez créer des archives permanentes dans Exchange Online. Comme alternative à l’utilisation d’archives permanentes, vous pouvez utiliser des [cas eDiscovery](https://go.microsoft.com/fwlink/?linkid=780738) ou [stratégies de rétention](https://go.microsoft.com/fwlink/?linkid=827811) de sécurité Office 365 &amp; centre de conformité. Une fois que nous mettre hors service new archives permanentes, vous pourrez toujours modifier existant archives permanentes et création archives permanentes dans Exchange Server 2013 et les déploiements Exchange hybride seront toujours être prise en charge. Et, vous pourrez toujours placer les boîtes aux lettres en conservation pour litige. 
  
Vous devrez peut-être une situation où une personne a quitté votre organisation et leur compte d’utilisateur correspondant et la boîte aux lettres ont été supprimées. Ensuite, vous constatez des informations dans la boîte aux lettres qui doive être conservés. Que pouvez-vous faire ? Si la période de rétention de boîte aux lettres supprimée n’a pas expiré, vous pouvez placer une conservation inaltérable dans la boîte aux lettres supprimée (appelé une boîte aux lettres supprimée) et rendre une boîte aux lettres inactive. Une *boîte aux lettres inactive* est utilisée pour conserver le courrier électronique d’un ancien employé une fois qu’il quitte l’organisation. Le contenu d’une boîte aux lettres inactive est conservé pour la durée de la conservation inaltérable qui était est placée sur la boîte aux lettres supprimée lorsqu’il a été effectué inactif. Une fois la boîte aux lettres inactive, vous pouvez rechercher la boîte aux lettres dans Exchange Online, recherche de contenu de sécurité Office 365 à l’aide de la découverte électronique locale &amp; centre de conformité, ou le centre eDiscovery dans SharePoint Online. 
  
> [!NOTE]
> Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée (ou rendue inactive) dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée ou rendue inactive. 
  
## <a name="before-you-begin"></a>Avant de commencer
<a name="sectionSection0"> </a>

- Vous devez utiliser l'applet de commande **New-MailboxSearch** dans Windows PowerShell pour placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable). Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE) ni le centre de découverte électronique SharePoint Online. 
    
- Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Exécutez la commande suivante pour obtenir les informations d'identité sur les boîtes aux lettres supprimées (récupérables) de votre organisation. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Pour de plus amples informations sur les boîtes aux lettres inactives, consultez la rubrique [Boîtes aux lettres inactives dans Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable) pour rendre la boîte aux lettres inactive
<a name="sectionSection1"> </a>

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

## <a name="more-information"></a>Plus d'informations
<a name="sectionSection2"> </a>

Une fois la boîte aux lettres supprimée (récupérable) devenue inactive, il existe plusieurs façons de gérer la boîte aux lettres. Pour plus d'informations, voir :
  
- [Modifier la durée de la conservation pour une boîte aux lettres inactive dans Exchange Online](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [Récupérer une boîte aux lettres inactive dans Exchange Online](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [Restaurer une boîte aux lettres inactive dans Exchange Online](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [Supprimer un blocage d'une boîte aux lettres inactive dans Exchange Online](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    

