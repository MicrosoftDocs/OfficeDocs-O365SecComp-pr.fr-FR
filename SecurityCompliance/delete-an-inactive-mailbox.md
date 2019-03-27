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
# <a name="delete-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="ab0c0-104">Supprimer une boîte aux lettres inactive dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ab0c0-104">Delete an inactive mailbox in Office 365</span></span>

<span data-ttu-id="ab0c0-105">Une boîte aux lettres inactive est utilisée pour conserver le courrier électronique d'un ancien employé une fois qu'il quitte votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-105">An inactive mailbox is used to preserve a former employee's email after he or she leaves your organization.</span></span> <span data-ttu-id="ab0c0-106">Si vous n'avez plus besoin du contenu d'une boîte aux lettres inactive, vous pouvez le supprimer de façon définitive en supprimant le blocage.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-106">When you no longer need to preserve the contents of an inactive mailbox, you can permanently delete the inactive mailbox by removing the hold.</span></span> <span data-ttu-id="ab0c0-107">En outre, il est possible que plusieurs blocages soient placés sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-107">Also, it's possible that multiple holds might be placed on an inactive mailbox.</span></span> <span data-ttu-id="ab0c0-108">Par exemple, une boîte aux lettres inactive peut être placée en suspension pour litige et sur une ou plusieurs blocages sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-108">For example, an inactive mailbox might be placed on Litigation Hold and on one or more In-Place Holds.</span></span> <span data-ttu-id="ab0c0-109">De plus, une stratégie de rétention Office 365 (créée dans le &amp; Centre de sécurité conformité d'Office 365) peut être appliquée à la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-109">Additionally, an Office 365 retention policy (created in the Office 365 Security &amp; Compliance Center) might be applied to the inactive mailbox.</span></span> <span data-ttu-id="ab0c0-110">Vous devez supprimer toutes les conservations et les stratégies de rétention d'Office 365 d'une boîte aux lettres inactive pour les supprimer.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-110">You have to remove all holds and Office 365 retention policies from an inactive mailbox to delete it.</span></span> <span data-ttu-id="ab0c0-111">Une fois que vous avez supprimé les suspensions et les stratégies de rétention, la boîte aux lettres inactive est marquée pour suppression et est définitivement supprimée après traitement.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-111">After you remove the holds and retention policies, the inactive mailbox is marked for deletion and is permanently deleted after it's processed.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ab0c0-p103">Nous avons reporté l'échéance du 1er juillet 2017 afin de créer des conservations inaltérables pour rendre une boîte aux lettres inactive. Cependant, plus tard cette année ou au début de l'année prochaine, vous ne pourrez plus créer de conservations inaltérables dans Exchange Online. Actuellement, seules les conservations pour litige et les stratégies de rétention Office 365 peuvent être utilisées pour créer une boîte aux lettres inactive. Toutefois, les boîtes aux lettres inactives existantes qui se trouvent en conservation inaltérable seront toujours prises en charge. Vous pouvez continuer à gérer les conservations inaltérables sur les boîtes aux lettres inactives. Cela inclut la modification de la durée d'une conservation inaltérable et la suppression définitive d'une boîte aux lettres inactive en supprimant la conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
<span data-ttu-id="ab0c0-117">Consultez la section [Plus d'informations](#more-information) pour obtenir une description de ce qui se produit après la suppression des blocages d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-117">See the [More information](#more-information) section for a description of what happens after holds are removed from an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="ab0c0-118">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ab0c0-118">Before you begin</span></span>

- <span data-ttu-id="ab0c0-119">Vous devez utiliser Exchange Online PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-119">You have to use Exchange Online PowerShell to remove a Litigation Hold from an inactive mailbox.</span></span> <span data-ttu-id="ab0c0-120">Vous ne pouvez pas utiliser le Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-120">You can't use the Exchange admin center (EAC).</span></span> <span data-ttu-id="ab0c0-121">Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-121">For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span> <span data-ttu-id="ab0c0-122">Vous pouvez utiliser Exchange Online PowerShell ou le centre d'administration Exchange pour supprimer un blocage sur place d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-122">You can use Exchange Online PowerShell or the EAC to remove an In-Place Hold from an inactive mailbox.</span></span> 
    
- <span data-ttu-id="ab0c0-123">Vous pouvez copier le contenu d'une boîte aux lettres inactive vers une autre boîte aux lettres avant de supprimer la conservation et de supprimer une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-123">You can copy the contents of an inactive mailbox to another mailbox before you remove the hold and delete an inactive mailbox.</span></span> <span data-ttu-id="ab0c0-124">Pour plus d'informations, consultez la rubrique [restaurer une boîte aux lettres inactive dans Office 365](restore-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-124">For details, see [Restore an inactive mailbox in Office 365](restore-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="ab0c0-125">Si vous supprimez la conservation ou la stratégie de rétention Office 365 d'une boîte aux lettres inactive et que la période de rétention de boîte aux lettres supprimée (récupérable) pour la boîte aux lettres a expiré, la boîte aux lettres sera définitivement supprimée.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-125">If you remove the hold or Office 365 retention policy from an inactive mailbox and the soft-deleted mailbox retention period for the mailbox has expired, the mailbox will be permanently deleted.</span></span> <span data-ttu-id="ab0c0-126">Après sa suppression, elle ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-126">After it's deleted, it can't be recovered.</span></span> <span data-ttu-id="ab0c0-127">Avant de supprimer la conservation, vérifiez que vous n'avez plus besoin du contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-127">Before you remove the hold, be sure that you no longer need the contents in the mailbox.</span></span> <span data-ttu-id="ab0c0-128">Si vous souhaitez réactiver une boîte aux lettres inactive, vous pouvez la récupérer.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-128">If you want to re-activate an inactive mailbox, you can recover it.</span></span> <span data-ttu-id="ab0c0-129">Pour plus d'informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-129">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="ab0c0-130">Pour plus d'informations sur les boîtes aux lettres inactives, consultez la rubrique [inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-130">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="ab0c0-131">Étape 1 : Identifier les blocages sur une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ab0c0-131">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="ab0c0-132">Comme indiqué précédemment, une stratégie de rétention de conservation pour litige, conservation inaltérable ou Office 365 peut être placée sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-132">As previously stated, a Litigation Hold, In-Place Hold, or Office 365 retention policy might be placed on an inactive mailbox.</span></span> <span data-ttu-id="ab0c0-133">La première étape consiste à identifier les blocages sur une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-133">The first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="ab0c0-134">Exécutez la commande suivante pour afficher les informations de blocage pour toutes les boîtes aux lettres inactives dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-134">Run the following command to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

<span data-ttu-id="ab0c0-p108">La valeur de **True** pour la propriété **LitigationHoldEnabled** indique que la boîte aux lettres inactive est en suspension pour litige. Si un blocage sur place est placé sur une boîte aux lettres inactive, le GUID du blocage s'affiche comme valeur pour la propriété **InPlaceHolds**. Par exemple, les résultats suivants pour deux boîtes aux lettres inactives affichent qu'une suspension pour litige est placée sur Ann Beebe et que deux blocages sur place sont placés sur Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p108">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold is placed on an inactive mailbox, the GUID for the hold is displayed as the value for the **InPlaceHolds** property. For example, the following results for two inactive mailboxes show that a Litigation Hold is placed on Ann Beebe and that two In-Place Holds are placed on Pilar Pinilla.</span></span> 
  
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
> <span data-ttu-id="ab0c0-138">Si un grand nombre de blocages sur place est placé sur une boîte aux lettres inactive, tous les GUID de blocage sur place ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-138">If a lot of In-Place Holds are placed on an inactive mailbox, not all of the In-Place Hold GUIDs will be displayed.</span></span> <span data-ttu-id="ab0c0-139">Vous pouvez exécuter la commande suivante pour afficher tous les GUID de conservation inaltérable:`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span><span class="sxs-lookup"><span data-stu-id="ab0c0-139">You can run the following command to display all the In-Place Hold GUIDs:  `Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`</span></span>
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a><span data-ttu-id="ab0c0-140">Étape 2 : Supprimer une blocage d'une boîte aux lettres inactive</span><span class="sxs-lookup"><span data-stu-id="ab0c0-140">Step 2: Remove a hold from an inactive mailbox</span></span>

<span data-ttu-id="ab0c0-p110">Après avoir identifié le type de blocage placé sur la boîte aux lettres inactive (et s'il y a plusieurs blocages), l'étape suivante consiste à supprimer les blocages sur la boîte aux lettres. Comme indiqué précédemment, vous devez supprimer tous les blocages pour supprimer définitivement une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p110">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to remove the holds on the mailbox. As previously stated, you have to remove all holds to permanently delete an inactive mailbox.</span></span> 
  
### <a name="remove-a-litigation-hold"></a><span data-ttu-id="ab0c0-143">Supprimer une suspension pour litige</span><span class="sxs-lookup"><span data-stu-id="ab0c0-143">Remove a Litigation Hold</span></span>

<span data-ttu-id="ab0c0-p111">Comme indiqué précédemment, vous devez utiliser Windows PowerShell pour supprimer une suspension pour litige d'une boîte aux lettres inactive. Vous ne pouvez pas utiliser le CAE. Exécutez la commande suivante pour supprimer une suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p111">As previously stated, you have to use Windows PowerShell to remove a Litigation Hold from an inactive mailbox. You can't use the EAC. Run the following command to remove a Litigation Hold.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> <span data-ttu-id="ab0c0-p112">La meilleure façon d'identifier une boîte aux lettres inactive est d'utiliser son nom unique ou sa valeur GUID Exchange. L'une de ces valeurs permet d'empêcher de spécifier par inadvertance la mauvaise boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p112">The best way to identify an inactive mailbox is by using its Distinguished Name or Exchange GUID value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="remove-in-place-holds"></a><span data-ttu-id="ab0c0-149">Supprimer des blocages sur place</span><span class="sxs-lookup"><span data-stu-id="ab0c0-149">Remove In-Place Holds</span></span>

 <span data-ttu-id="ab0c0-150">Il existe deux façons de supprimer un blocage sur place à partir d'une boîte aux lettres inactive :</span><span class="sxs-lookup"><span data-stu-id="ab0c0-150">There are two ways to remove an In-Place Hold from an inactive mailbox:</span></span> 
  
- <span data-ttu-id="ab0c0-151">**Supprimer l'objet de conservation** inaltérable Si la boîte aux lettres inactive que vous souhaitez supprimer définitivement est la seule boîte aux lettres source pour une conservation inaltérable, vous pouvez simplement supprimer l'objet de blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-151">**Delete the In-Place Hold object** If the inactive mailbox that you want to permanently delete is the only source mailbox for an In-Place Hold, you can just delete the In-Place Hold object.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ab0c0-p113">Vous devez désactiver le blocage avant de pouvoir supprimer un objet de blocage sur place. Si vous essayez de supprimer un objet de blocage sur place ayant le blocage activé, vous recevrez un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p113">You have to disable the hold before you can delete an In-Place Hold object. If you try to delete an In-Place Hold object that has the hold enabled, you'll receive an error message.</span></span> 
  
- <span data-ttu-id="ab0c0-154">**Supprimer la boîte aux lettres inactive comme boîte aux lettres source d'une conservation inaltérable** Si vous souhaitez conserver d'autres boîtes aux lettres sources pour une conservation inaltérable, vous pouvez supprimer la boîte aux lettres inactive de la liste des boîtes aux lettres sources et conserver l'objet de conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-154">**Remove the inactive mailbox as a source mailbox of an In-Place Hold** If you want to retain other source mailboxes for an In-Place Hold, you can remove the inactive mailbox from the list of source mailboxes and keep the In-Place Hold object.</span></span> 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a><span data-ttu-id="ab0c0-155">Utiliser le Centre d'administration Exchange (CAE) pour supprimer un blocage sur place</span><span class="sxs-lookup"><span data-stu-id="ab0c0-155">Use the EAC to delete an In-Place Hold</span></span>

1. <span data-ttu-id="ab0c0-p114">Si vous connaissez le nom du blocage sur place à supprimer, vous pouvez passer à l'étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom du blocage sur place placé sur la boîte aux lettres inactive que vous souhaitez supprimer définitivement. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p114">If you know the name of the In-Place Hold that you want to delete, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox that you want to permanently delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="ab0c0-159">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-159">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="ab0c0-160">Sélectionnez la conservation inaltérable à supprimer, puis cliquez sur **modifier** ![l'icône](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)modifier.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-160">Select the In-Place Hold you want to delete, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="ab0c0-161">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-161">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**, uncheck the **Place content matching the search query in selected mailboxes on hold** box, and then click **Save**.</span></span>
    
5. <span data-ttu-id="ab0c0-162">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-162">On the **In-Place eDiscovery &amp; Hold** page, select the In-Place Hold again, and then click **Delete**![Delete icon](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).</span></span>
    
6. <span data-ttu-id="ab0c0-163">Dans le message d'avertissement, cliquez sur **Oui** pour supprimer le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-163">On the warning, click **Yes** to delete the In-Place Hold.</span></span> 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a><span data-ttu-id="ab0c0-164">Utiliser Exchange Online PowerShell pour supprimer une conservation inaltérable</span><span class="sxs-lookup"><span data-stu-id="ab0c0-164">Use Exchange Online PowerShell to delete an In-Place Hold</span></span>

1. <span data-ttu-id="ab0c0-p115">Créez une variable qui contient les propriétés du blocage sur place à supprimer. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p115">Create a variable that contains the properties of the In-Place Hold that you want to delete. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="ab0c0-167">Désactivez le blocage sur le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-167">Disable the hold on the In-Place Hold.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. <span data-ttu-id="ab0c0-168">Supprimez le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-168">Delete the In-Place Hold.</span></span>
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="ab0c0-169">Utilisez le CAE pour supprimer une boîte aux lettres inactive d'un blocage sur place</span><span class="sxs-lookup"><span data-stu-id="ab0c0-169">Use the EAC to remove an inactive mailbox from an In-Place Hold</span></span>

1. <span data-ttu-id="ab0c0-p116">Si vous connaissez le nom du blocage sur place placé sur la boîte aux lettres inactive, vous pouvez passer à l'étape suivante. Dans le cas contraire, exécutez la commande suivante pour obtenir le nom du blocage sur place placé sur la boîte aux lettres. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p116">If you know the name of the In-Place Hold that's placed on the inactive mailbox, you can go to the next step. Otherwise, run the following command to get the name of the In-Place Hold placed on the mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. <span data-ttu-id="ab0c0-173">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-173">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="ab0c0-174">Sélectionnez le blocage sur place placé sur la boîte aux lettres inactive, puis cliquez sur **modifier** ![l'icône](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)modifier.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-174">Select the In-Place Hold that is placed on the inactive mailbox, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="ab0c0-175">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-175">On the **In-Place eDiscovery &amp; Hold** properties page, click **Sources**.</span></span>
    
5. <span data-ttu-id="ab0c0-176">Dans la liste des boîtes aux lettres source, cliquez sur le nom de la boîte aux lettres inactive à supprimer, puis cliquez sur **Supprimer**![Icône Suppression](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-176">In the list of source mailboxes, click the name of the inactive mailbox that you want to remove, and then click **Remove**![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif).</span></span>
    
6. <span data-ttu-id="ab0c0-p117">Cliquez sur **Enregistrer** pour enregistrer la modification. Un message s'affiche indiquant que l'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p117">Click **Save** to save the change. A message is displayed saying the operation was successfully completed.</span></span> 
    
7. <span data-ttu-id="ab0c0-179">Répétez les étapes 1 à 6 pour supprimer d'autres blocages sur place placés sur la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-179">Repeat steps 1 through 6 to remove other In-Place Holds placed on the inactive mailbox.</span></span>
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a><span data-ttu-id="ab0c0-180">Utiliser Exchange Online PowerShell pour supprimer une boîte aux lettres inactive d'une conservation inaltérable</span><span class="sxs-lookup"><span data-stu-id="ab0c0-180">Use Exchange Online PowerShell to remove an inactive mailbox from an In-Place Hold</span></span>

<span data-ttu-id="ab0c0-181">Si le blocage sur place contient un grand nombre de boîtes aux lettres source, il est possible que la boîte aux lettres inactive ne soit pas répertoriée sur la page **Sources** dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-181">If the In-Place Hold contains a large number of source mailboxes, it's possible the inactive mailbox won't be listed on the **Sources** page in the EAC.</span></span> <span data-ttu-id="ab0c0-182">Jusqu'à 3 000 boîtes aux lettres s'affichent sur la page **Sources** lorsque vous modifiez un blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-182">Up to 3,000 mailboxes are displayed on the **Sources** page when you edit an In-Place Hold.</span></span> <span data-ttu-id="ab0c0-183">Si une boîte aux lettres inactive n'est pas affichée sur la page **sources** , vous pouvez utiliser Exchange Online PowerShell pour la supprimer de la conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-183">If an inactive mailbox isn't listed on the **Sources** page, you can use Exchange Online PowerShell to remove it from the In-Place Hold.</span></span> 
  
1. <span data-ttu-id="ab0c0-p119">Créez une variable qui contient les propriétés du blocage sur place placé sur la boîte aux lettres inactive. Utilisez le GUID du blocage sur place obtenu à l'[Étape 1 : Identifier les blocages sur une boîte aux lettres inactive](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p119">Create a variable that contains the properties of the In-Place Hold placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1: Identify the holds on an inactive mailbox](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. <span data-ttu-id="ab0c0-186">Vérifiez que la boîte aux lettres inactive est répertoriée comme une boîte aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-186">Verify that the inactive mailbox is listed as a source mailbox for the In-Place Hold.</span></span> 
    
```
  $InPlaceHold.Sources
```

   <span data-ttu-id="ab0c0-187">**Remarque:** La propriété *sources* de la conservation inaltérable identifie les boîtes aux lettres source en fonction de leurs propriétés *legacyExchangeDN* .</span><span class="sxs-lookup"><span data-stu-id="ab0c0-187">**Note:** The *Sources* property of the In-Place Hold identifies the source mailboxes by their *LegacyExchangeDN* properties.</span></span> <span data-ttu-id="ab0c0-188">Étant donné que cette propriété identifie les boîtes aux lettres inactives de façon unique, l'utilisation de la propriété *Sources* du blocage sur place permet d'empêcher la suppression de la boîte aux lettres incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-188">Because this property uniquely identifies inactive mailboxes, using the *Sources* property from the In-Place Hold helps prevent removing the wrong mailbox.</span></span> <span data-ttu-id="ab0c0-189">Cela permet également d'éviter les problèmes si deux boîtes aux lettres ont le même alias ou la même adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-189">This also helps to avoid issues if two mailboxes have the same alias or SMTP address.</span></span> 
   
3. <span data-ttu-id="ab0c0-p121">Supprimez la boîte aux lettres inactive dans la liste des boîtes aux lettres sources dans la variable. Veillez à utiliser le **LegacyExchangeDN** de la boîte aux lettres inactive qui est renvoyé par la commande à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p121">Remove the inactive mailbox from the list of source mailboxes in the variable. Be sure to use the **LegacyExchangeDN** of the inactive mailbox that's returned by the command in the previous step.</span></span> 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. <span data-ttu-id="ab0c0-192">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source dans la variable.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-192">Verify that the inactive mailbox is removed from the list of source mailboxes in the variable.</span></span>
    
```
  $InPlaceHold.Sources
```

5. <span data-ttu-id="ab0c0-193">Modifiez le blocage sur place avec la liste mise à jour des boîtes aux lettres source, qui n'inclut pas la boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-193">Modify the In-Place Hold with the updated list of source mailboxes, which doesn't include the inactive mailbox.</span></span>
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. <span data-ttu-id="ab0c0-194">Vérifiez que la boîte aux lettres inactive est supprimée de la liste des boîtes aux lettres source pour le blocage sur place.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-194">Verify that the inactive mailbox is removed from the list of source mailboxes for the In-Place Hold.</span></span>
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a><span data-ttu-id="ab0c0-195">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="ab0c0-195">More information</span></span>

- <span data-ttu-id="ab0c0-p122">**Une boîte aux lettres inactive est un type de boîte aux lettres supprimée (récupérable).** Dans Exchange Online, une boîte aux lettres supprimée (récupérable) est une boîte aux lettres qui a été supprimée mais qui peut être récupérée pendant une période de rétention spécifique. Le délai de rétention d'une boîte aux lettres supprimée (récupérable) dans Exchange Online est de 30 jours. Ainsi, la boîte aux lettres peut être récupérée dans les 30 jours qui suivent le moment où elle a été supprimée (récupérable). Après 30 jours, une boîte aux lettres supprimée (récupérable) est marquée pour suppression définitive et ne peut pas être récupérée.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p122">**An inactive mailbox is a type of soft-deleted mailbox.** In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered within 30 days of being soft-deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered.</span></span> 
    
- <span data-ttu-id="ab0c0-p123">**Que se passe-t-il après avoir supprimé la conservation sur une boîte aux lettres inactive ?** La boîte aux lettres est traitée comme d'autres boîtes aux lettres supprimées (récupérables) et est marquée pour suppression définitive après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable) de 30 jours. Ce délai de rétention commence à la date à laquelle la boîte aux lettres a été rendue inactive pour la première fois. Cette date est appelée la date supprimée (récupérable), qui représente la date de suppression du compte utilisateur Office 365 correspondant ou la date de suppression de la boîte aux lettres Exchange Online avec la cmdlet **Remove-Mailbox**. La date supprimée (récupérable) n'est pas la date de suppression du blocage.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p123">**What happens after you remove the hold on an inactive mailbox?** The mailbox is treated like other soft-deleted mailboxes and is marked for permanent deletion after the 30-day soft-deleted mailbox retention period expires. This retention period starts on the date when the mailbox was first made inactive. This date is known as the soft-deleted date, which is the date the corresponding Office 365 user account was deleted or when the Exchange Online mailbox was deleted with the **Remove-Mailbox** cmdlet. The soft-deleted date isn't the date on which you remove the hold.</span></span> 
    
- <span data-ttu-id="ab0c0-p124">**Une boîte aux lettres inactive est-elle définitivement supprimée immédiatement après la suppression de la conservation ?** Si la date supprimée (récupérable) pour une boîte aux lettres inactive est de plus de 30 jours, la boîte aux lettres n'est pas supprimée définitivement dès que vous supprimez la conservation. La boîte aux lettres sera marquée pour suppression définitive et sera supprimée lors de son prochain traitement.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-p124">**Is an inactive mailbox permanently deleted immediately after the hold is removed?** If the soft-deleted date for an inactive mailbox is older than 30 days, the mailbox won't be permanently deleted as soon as you remove the hold. The mailbox will be marked for permanent deletion and is deleted the next time it's processed.</span></span> 
    
- <span data-ttu-id="ab0c0-209">**Quel est l'impact de la période de rétention de la boîte aux lettres supprimée (récupérable) sur les boîtes aux lettres inactives ?**</span><span class="sxs-lookup"><span data-stu-id="ab0c0-209">**How does the soft-deleted mailbox retention period affect inactive mailboxes?**</span></span> <span data-ttu-id="ab0c0-210">Si la date supprimée (récupérable) pour une boîte aux lettres inactive se situe plus de 30 jours avant la date de la suppression de la conservation, la boîte aux lettres est marquée pour suppression définitive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-210">If the soft-deleted date for an inactive mailbox is more than 30 days before the date the hold was removed, the mailbox is marked for permanent deletion.</span></span> <span data-ttu-id="ab0c0-211">Par contre, si la date supprimée (récupérable) d'une boîte aux lettres inactive se situe dans les 30 derniers jours et que vous supprimez la conservation, vous pouvez récupérer la boîte aux lettres jusqu'à l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-211">But if an inactive mailbox has a soft-deleted date within the last 30 days and you remove the hold, you can recover the mailbox up until the soft-deleted mailbox retention period expires.</span></span> <span data-ttu-id="ab0c0-212">Pour plus d'informations, consultez la rubrique [supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-212">For details, see [Delete or restore user mailboxes in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835).</span></span> <span data-ttu-id="ab0c0-213">Après l'expiration de la période de rétention de la boîte aux lettres supprimée (récupérable), vous devez suivre les procédures de récupération d'une boîte aux lettres inactive.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-213">After the soft-deleted mailbox retention period expires, you have follow the procedures for recovering an inactive mailbox.</span></span> <span data-ttu-id="ab0c0-214">Pour plus d'informations, consultez la rubrique [récupérer une boîte aux lettres inactive dans Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-214">For details, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
- <span data-ttu-id="ab0c0-215">**Comment afficher des informations sur une boîte aux lettres inactive après la suppression de la conservation ?**</span><span class="sxs-lookup"><span data-stu-id="ab0c0-215">**How do you display information about an inactive mailbox after the hold is removed?**</span></span> <span data-ttu-id="ab0c0-216">Après la suppression d'une conservation et la restauration de la boîte aux lettres inactive vers une boîte aux lettres supprimée (récupérable), elle n'est pas renvoyée à l'aide du paramètre *InactiveMailboxOnly* avec la cmdlet **Get-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="ab0c0-216">After a hold is removed and the inactive mailbox is reverted back to a soft-deleted mailbox, it won't be returned by using the  *InactiveMailboxOnly*  parameter with the **Get-Mailbox** cmdlet.</span></span> <span data-ttu-id="ab0c0-217">Cependant, vous pouvez afficher des informations sur la boîte aux lettres à l'aide de la commande **Get-Mailbox -SoftDeletedMailbox**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-217">But you can display information about the mailbox by using the **Get-Mailbox -SoftDeletedMailbox** command.</span></span> <span data-ttu-id="ab0c0-218">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ab0c0-218">For example:</span></span> 
    
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
  
<span data-ttu-id="ab0c0-219">Dans l'exemple ci-dessus, la propriété *WhenSoftDeleted* identifie la date supprimée (récupérable), qui, dans cet exemple, est le 30 octobre 2014.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-219">In the above example, the *WhenSoftDeleted* property identifies the soft-deleted date, which in this example is October 30, 2014.</span></span> <span data-ttu-id="ab0c0-220">Si cette boîte aux lettres supprimée (récupérable) était auparavant une boîte aux lettres inactive pour laquelle la conservation a été supprimée, elle sera définitivement supprimée 30 jours après la valeur de la propriété *WhenSoftDeleted* .</span><span class="sxs-lookup"><span data-stu-id="ab0c0-220">If this soft-deleted mailbox was previously an inactive mailbox for which the hold was removed, it will be permanently deleted 30 days after the value of the *WhenSoftDeleted* property.</span></span> <span data-ttu-id="ab0c0-221">Dans ce cas, la boîte aux lettres est définitivement supprimée après le 30 novembre 2014.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-221">In this case, the mailbox is permanently deleted after November 30, 2014.</span></span>

