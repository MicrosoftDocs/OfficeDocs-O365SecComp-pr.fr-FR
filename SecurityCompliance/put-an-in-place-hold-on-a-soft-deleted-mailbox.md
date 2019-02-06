---
title: Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.
ms.openlocfilehash: e666ac608ec224bf97caa947be2cb42b742c6fa9
ms.sourcegitcommit: ca97beff215d154b6ab006ce1222056434fde1a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29740796"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="7fd40-104">Placer une conservation inaltérable dans une boîte aux lettres supprimée (récupérable) dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7fd40-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="7fd40-p102">Découvrez comment créer une conservation inaltérable pour une boîte aux lettres supprimée (récupérable) pour la rendre inactive et conserver son contenu. Vous pouvez ensuite utiliser les outils de découverte électronique Microsoft pour rechercher la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7fd40-p103">Nous avons retardée de la date d’échéance pour créer de nouvelles archives permanentes dans Exchange Online (dans les plans autonomes Office 365 et Exchange Online). Mais cette année ou le début d’année, vous ne pourrez créer des archives permanentes dans Exchange Online. Comme alternative à l’utilisation d’archives permanentes, vous pouvez utiliser des [cas eDiscovery](https://go.microsoft.com/fwlink/?linkid=780738) ou [stratégies de rétention](https://go.microsoft.com/fwlink/?linkid=827811) de sécurité Office 365 &amp; centre de conformité. Une fois que nous mettre hors service new archives permanentes, vous pourrez toujours modifier existant archives permanentes et création archives permanentes dans Exchange Server 2013 et les déploiements Exchange hybride seront toujours être prise en charge. Et, vous pourrez toujours placer les boîtes aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p103">We've postponed the deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="7fd40-p104">Vous devrez peut-être une situation où une personne a quitté votre organisation et leur compte d’utilisateur correspondant et la boîte aux lettres ont été supprimées. Ensuite, vous constatez des informations dans la boîte aux lettres qui doive être conservés. Que pouvez-vous faire ? Si la période de rétention de boîte aux lettres supprimée n’a pas expiré, vous pouvez placer une conservation inaltérable dans la boîte aux lettres supprimée (appelé une boîte aux lettres supprimée) et rendre une boîte aux lettres inactive. Une *boîte aux lettres inactive* est utilisée pour conserver le courrier électronique d’un ancien employé une fois qu’il quitte l’organisation. Le contenu d’une boîte aux lettres inactive est conservé pour la durée de la conservation inaltérable qui était est placée sur la boîte aux lettres supprimée lorsqu’il a été effectué inactif. Une fois la boîte aux lettres inactive, vous pouvez rechercher la boîte aux lettres dans Exchange Online, recherche de contenu de sécurité Office 365 à l’aide de la découverte électronique locale &amp; centre de conformité, ou le centre eDiscovery dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7fd40-p105">Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée (ou rendue inactive) dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée ou rendue inactive.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="7fd40-123">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7fd40-123">Before you begin</span></span>

- <span data-ttu-id="7fd40-p106">Vous devez utiliser l'applet de commande **New-MailboxSearch** dans Windows PowerShell pour placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable). Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE) ni le centre de découverte électronique SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="7fd40-126">Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="7fd40-126">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="7fd40-127">Exécutez la commande suivante pour obtenir les informations d'identité sur les boîtes aux lettres supprimées (récupérables) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7fd40-127">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="7fd40-128">Pour plus d’informations sur les boîtes aux lettres inactives, voir [vue d’ensemble des boîtes aux lettres inactives dans Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="7fd40-128">For more information about inactive mailboxes, see [Overview of inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="7fd40-129">Placer une conservation inaltérable sur une boîte aux lettres supprimée (récupérable) pour rendre la boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7fd40-129">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>

<span data-ttu-id="7fd40-p107">Utilisez l'applet de commande **New-MailboxSearch** pour rendre inactive une boîte aux lettres supprimée (récupérable). Pour plus d'informations, voir [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fd40-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="7fd40-132">Créez une variable contenant les propriétés de la boîte aux lettres supprimée (récupérable).</span><span class="sxs-lookup"><span data-stu-id="7fd40-132">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > <span data-ttu-id="7fd40-p108">Dans la commande précédente, utilisez la valeur de la propriété **DistinguishedName** ou **ExchangeGuid** pour identifier la boîte aux lettres supprimée (récupérable). Ces propriétés sont uniques pour chaque boîte aux lettres de votre organisation, alors qu'une boîte aux lettres active et une boîte aux lettres supprimée (récupérable) peuvent avoir la même adresse SMTP principale.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="7fd40-p109">Créez une conservation inaltérable et placez-la sur la boîte aux lettres supprimée (récupérable). Dans cet exemple, aucune durée de suspension n’est spécifiée. Cela signifie que les éléments seront suspendus indéfiniment ou jusqu’à ce que la suspension soit supprimée de la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   <span data-ttu-id="7fd40-p110">Vous pouvez également spécifier une durée de suspension lorsque vous créez la conservation inaltérable. Cet exemple conserve des éléments de la boîte aux lettres inactive pendant environ sept ans.</span><span class="sxs-lookup"><span data-stu-id="7fd40-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. <span data-ttu-id="7fd40-140">Après un certain temps, exécutez l’une des commandes suivantes pour vérifier que la boîte aux lettres supprimée (récupérable) est une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="7fd40-140">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    <span data-ttu-id="7fd40-141">Ou</span><span class="sxs-lookup"><span data-stu-id="7fd40-141">Or</span></span>
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a><span data-ttu-id="7fd40-142">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7fd40-142">More information</span></span>

<span data-ttu-id="7fd40-p111">Une fois la boîte aux lettres supprimée (récupérable) devenue inactive, il existe plusieurs façons de gérer la boîte aux lettres. Pour plus d'informations, voir :</span><span class="sxs-lookup"><span data-stu-id="7fd40-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- [<span data-ttu-id="7fd40-145">Modifier la durée de conservation pour une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7fd40-145">Change the hold duration for an inactive mailbox</span></span>](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [<span data-ttu-id="7fd40-146">Récupérer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7fd40-146">Recover an inactive mailbox</span></span>](recover-an-inactive-mailbox.md)
    
- [<span data-ttu-id="7fd40-147">Restaurer une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="7fd40-147">Restore an inactive mailbox</span></span>](restore-an-inactive-mailbox.md)
    
- <span data-ttu-id="7fd40-148">[Supprimer une boîte aux lettres inactive](delete-an-inactive-mailbox.md) (en supprimant la suspension)</span><span class="sxs-lookup"><span data-stu-id="7fd40-148">[Delete an inactive mailbox](delete-an-inactive-mailbox.md) (by removing the hold)</span></span>
