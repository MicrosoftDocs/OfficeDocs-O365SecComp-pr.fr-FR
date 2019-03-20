---
title: Placement d'une boîte aux lettres en conservation pour litige
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. '
ms.openlocfilehash: a4d0939ffed32a8442b4b705bd15804b9f3eb7ea
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693123"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="5298f-103">Placement d'une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="5298f-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="5298f-104">Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu de la boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés.</span><span class="sxs-lookup"><span data-stu-id="5298f-104">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items.</span></span> <span data-ttu-id="5298f-105">Lorsque vous placez la boîte aux lettres d'un utilisateur en conservation pour litige, le contenu de la boîte aux lettres d'archivage de l'utilisateur (si elle est activée) est également placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="5298f-105">When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold.</span></span> <span data-ttu-id="5298f-106">Les éléments supprimés et modifiés sont conservés pendant une période spécifiée, ou jusqu'à ce que vous supprimiez la boîte aux lettres de la conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-106">Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold.</span></span> <span data-ttu-id="5298f-107">Tous ces éléments de boîte aux lettres sont renvoyés dans une recherche de [Découverte électronique locale](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx).</span><span class="sxs-lookup"><span data-stu-id="5298f-107">All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5298f-108">La conservation pour litige conserve les éléments dans le dossier Éléments récupérables de la boîte aux lettres de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5298f-108">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox.</span></span> <span data-ttu-id="5298f-109">En fonction du nombre et de la taille des éléments supprimés ou modifiés, la taille du dossier Éléments récupérables de la boîte aux lettres peut augmenter rapidement.</span><span class="sxs-lookup"><span data-stu-id="5298f-109">Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly.</span></span> <span data-ttu-id="5298f-110">Le dossier Éléments récupérables est configuré avec un quota élevé par défaut.</span><span class="sxs-lookup"><span data-stu-id="5298f-110">The Recoverable Items folder is configured with a high quota by default.</span></span> <span data-ttu-id="5298f-111">Dans Exchange Online, ce quota augmente automatiquement lorsque vous placez une boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-111">In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold.</span></span> <span data-ttu-id="5298f-112">Dans Exchange Server 2013, nous vous recommandons de surveiller les boîtes aux lettres placées en conservation pour litige sur une base hebdomadaire afin de s'assurer qu'elles n'atteignent pas les limites des quotas d'éléments récupérables.</span><span class="sxs-lookup"><span data-stu-id="5298f-112">In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="5298f-113">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5298f-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="5298f-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-114"></span></span>

- <span data-ttu-id="5298f-115">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="5298f-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="5298f-116">Il se peut que vous deviez attendre 60 minutes avant que le paramètre Conservation pour litige ne soit actif.</span><span class="sxs-lookup"><span data-stu-id="5298f-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="5298f-p103">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Conservation inaltérable » dans la rubrique [Stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="5298f-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="5298f-119">Pour placer une boîte aux lettres Exchange Online en conservation pour litige, une licence Exchange Online (plan 2) doit lui être attribuée.</span><span class="sxs-lookup"><span data-stu-id="5298f-119">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license.</span></span> <span data-ttu-id="5298f-120">Si une boîte aux lettres dispose d’une licence Exchange Online (Plan 1), vous devez lui attribuer une licence Archivage Exchange Online distincte pour la placer en conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="5298f-120">If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="5298f-121">Comme expliqué précédemment, lorsque vous placez une conservation pour litige dans la boîte aux lettres d'un utilisateur, le contenu de la boîte aux lettres d'archivage de l'utilisateur est également placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="5298f-121">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold.</span></span> <span data-ttu-id="5298f-122">Si vous placez une conservation pour litige sur une boîte aux lettres principale locale dans un déploiement hybride Exchange, la boîte aux lettres d'archivage informatique (si elle est activée) est également mise en attente.</span><span class="sxs-lookup"><span data-stu-id="5298f-122">If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="5298f-123">Dans Exchange Online, le quota pour le dossier éléments récupérables est automatiquement augmenté à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-123">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold.</span></span> <span data-ttu-id="5298f-124">La taille par défaut de ce dossier est de 30 Go.</span><span class="sxs-lookup"><span data-stu-id="5298f-124">The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="5298f-125">La conservation pour litige conserve les éléments supprimés, ainsi que les versions originales des éléments modifiés jusqu'à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="5298f-125">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed.</span></span> <span data-ttu-id="5298f-126">Vous pouvez éventuellement spécifier une durée d'attente, ce qui permet de conserver un élément de boîte aux lettres pendant la durée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5298f-126">You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period.</span></span> <span data-ttu-id="5298f-127">Si vous spécifiez une durée d'attente, cette dernière débute à partir de la date de réception d'un message ou de la date de création d'un élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-127">If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> <span data-ttu-id="5298f-128">Pour conserver les éléments qui répondent aux critères spécifiés, utilisez une conservation inaltérable pour créer une conservation basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="5298f-128">To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold.</span></span> <span data-ttu-id="5298f-129">Pour plus d'informations, consultez la rubrique [créer ou supprimer une conservation](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)inaltérable.</span><span class="sxs-lookup"><span data-stu-id="5298f-129">For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="5298f-130">Pour utiliser l'environnement de ligne de commande Exchange Management Shell pour mettre en attente une boîte aux lettres Exchange Online, vous devez utiliser Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5298f-130">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell.</span></span> <span data-ttu-id="5298f-131">Pour plus d'informations, voir [Connexion à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="5298f-131">For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="5298f-132">La mise en attente pour litige dans une boîte aux lettres de dossiers publics n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5298f-132">Placing a Litigation Hold on a public folder mailbox isn't supported.</span></span> <span data-ttu-id="5298f-133">Vous devez utiliser la conservation inaltérable pour placer une conservation sur des dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="5298f-133">You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="5298f-134">Utilisation du Centre d’administration Exchange pour mettre une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="5298f-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="5298f-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-135"></span></span>

1. <span data-ttu-id="5298f-136">Accédez à **Destinataires** \> **Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="5298f-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="5298f-137">Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres que vous souhaitez placer en conservation pour litige \*\*\*\* ![, puis cliquez](media/ITPro-EAC-EditIcon.gif)sur modifier l'icône modifier.</span><span class="sxs-lookup"><span data-stu-id="5298f-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="5298f-138">Dans la page Propriétés de boîte aux lettres, cliquez sur **fonctionnalités de boîte aux lettres.**</span><span class="sxs-lookup"><span data-stu-id="5298f-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="5298f-139">Sous **Conservation pour litige : désactivée**, cliquez sur **Activer** pour mettre la boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="5298f-140">Sur la page **Conservation pour litige**, entrez les informations facultatives suivantes :</span><span class="sxs-lookup"><span data-stu-id="5298f-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="5298f-p110">**Durée de conservation pour litige (en nombre de jours)** Cette zone permet de spécifier la durée de conservation des éléments de boîte aux lettres lorsque la boîte aux lettres est conservée pour litige. La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres. Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu'à ce que la conservation soit annulée. Indiquez la période en nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="5298f-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="5298f-145">**Remarque** Cette zone permet d'informer l'utilisateur de la conservation pour litige de sa boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-145">**Note** Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="5298f-146">La note apparaît dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5298f-146">The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="5298f-147">**URL** Cette zone permet de diriger l'utilisateur vers un site web pour plus d'informations sur la conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-147">**URL** Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="5298f-148">Cette URL apparaît dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5298f-148">This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="5298f-149">Cliquez sur **Enregistrer** sur la page **Conservation pour litige**, puis cliquez sur **Enregistrer** sur la page des propriétés de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="5298f-150">Utiliser l'environnement Shell pour placer une boîte aux lettres en conservation pour litige indéfiniment</span><span class="sxs-lookup"><span data-stu-id="5298f-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="5298f-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-151"></span></span>

<span data-ttu-id="5298f-p113">Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige. Les éléments de la boîte aux lettres sont conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée.</span><span class="sxs-lookup"><span data-stu-id="5298f-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="5298f-154">Lorsque vous placez une boîte aux lettres en conservation pour litige indéfiniment (en ne spécifiant aucune durée), la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="5298f-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="5298f-155">Utiliser l'environnement de lignes de commande Exchange Management Shell pour mettre une boîte aux lettres en conservation pour litige et conserver des éléments pendant une durée spécifiée</span><span class="sxs-lookup"><span data-stu-id="5298f-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="5298f-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-156"></span></span>

<span data-ttu-id="5298f-157">Dans cet exemple, la boîte aux lettres bsuneja@contoso.com est placée en conservation pour litige et les éléments sont conservés pendant 2 555 jours (environ 7 ans).</span><span class="sxs-lookup"><span data-stu-id="5298f-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="5298f-158">Utiliser l'environnement Shell pour placer toutes les boîtes aux lettres en conservation pour litige pendant une durée spécifiée</span><span class="sxs-lookup"><span data-stu-id="5298f-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="5298f-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-159"></span></span>

<span data-ttu-id="5298f-160">Votre organisation peut exiger que toutes les données de boîte aux lettres soient conservées pendant une période de temps spécifique.</span><span class="sxs-lookup"><span data-stu-id="5298f-160">Your organization may require that all mailbox data be preserved for a specific period of time.</span></span> <span data-ttu-id="5298f-161">Avant de placer toutes les boîtes aux lettres d'une organisation en conservation pour litige, prenez en compte les points suivants:</span><span class="sxs-lookup"><span data-stu-id="5298f-161">Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="5298f-162">Dans cet exemple, toutes les boîtes aux lettres utilisateur de l'organisation sont placées en conservation pour litige pendant un an (365 jours).</span><span class="sxs-lookup"><span data-stu-id="5298f-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="5298f-163">Cet exemple utilise la cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) pour récupérer toutes les boîtes aux lettres de l'organisation, spécifie un filtre de destinataires pour inclure toutes les boîtes aux lettres utilisateur, puis canalise la liste des boîtes aux lettres vers la cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) pour activer la conservation pour litige et durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="5298f-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="5298f-164">Pour conserver toutes les boîtes aux lettres d'utilisateurs pour une durée indéterminée, exécutez la commande précédente, mais n'incluez pas le paramètre  _LitigationHoldDuration_.</span><span class="sxs-lookup"><span data-stu-id="5298f-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="5298f-165">Consultez la section [Plus d'informations](#moreinfo.md) pour obtenir des exemples d'utilisation d'autres propriétés de destinataire dans un filtre pour inclure ou exclure une ou plusieurs boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="5298f-166">Utiliser l'environnement de commande Exchange Management Shell pour supprimer une boîte aux lettres en conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="5298f-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="5298f-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-167"></span></span>

<span data-ttu-id="5298f-168">Dans cet exemple, la conservation pour litige de la boîte aux lettres bsuneja@contoso.com est supprimée.</span><span class="sxs-lookup"><span data-stu-id="5298f-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="5298f-169">P</span><span class="sxs-lookup"><span data-stu-id="5298f-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="5298f-170">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="5298f-170">How do you know this worked?</span></span>
<span data-ttu-id="5298f-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-171"></span></span>

<span data-ttu-id="5298f-172">Pour vérifier que vous avez correctement placé une boîte aux lettres en conservation pour litige, effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5298f-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="5298f-173">Dans le CAE, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5298f-173">In the EAC:</span></span>
    
1. <span data-ttu-id="5298f-174">Accédez à **Destinataires**\> **Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="5298f-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="5298f-175">Dans la liste des boîtes aux lettres utilisateur, cliquez sur la boîte aux lettres pour laquelle vous souhaitez vérifier les paramètres de conservation \*\*\*\* ![pour litige,](media/ITPro-EAC-EditIcon.gif)puis cliquez sur modifier l'icône de modification.</span><span class="sxs-lookup"><span data-stu-id="5298f-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="5298f-176">Dans la page Propriétés de boîte aux lettres, cliquez sur **fonctionnalités de boîte aux lettres.**</span><span class="sxs-lookup"><span data-stu-id="5298f-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="5298f-177">Sous **Conservation pour litige**, vérifiez que la conservation est activée.</span><span class="sxs-lookup"><span data-stu-id="5298f-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="5298f-p115">Cliquez sur **Afficher les détails** pour vérifier la date et l'auteur de la conservation pour litige de la boîte aux lettres. Vous pouvez également vérifier ou modifier les valeurs dans les zones facultatives **Durée de conservation pour litige (en nombre de jours)**, **Remarque** et **URL**.</span><span class="sxs-lookup"><span data-stu-id="5298f-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="5298f-180">Dans l'environnement de commande Exchange Management Shell, exécutez l'une des commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="5298f-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="5298f-181">ou</span><span class="sxs-lookup"><span data-stu-id="5298f-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="5298f-182">Si une boîte aux lettres est placée en conservation pour litige indéfiniment, la valeur de la propriété de boîte aux lettres  _LitigationHoldDuration_ est définie sur  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="5298f-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="5298f-183">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5298f-183">More information</span></span>
<span data-ttu-id="5298f-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="5298f-184"></span></span>

- <span data-ttu-id="5298f-185">Si votre organisation exige la conservation de toutes les données de boîtes aux lettres pendant une période spécifique, réfléchissez aux éléments suivants avant de placer toutes les boîtes aux lettres de l'organisation en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="5298f-p116">Lorsque vous utilisez la commande précédente pour mettre en conservation toutes les boîtes aux lettres d'une organisation (ou un sous-ensemble de boîtes aux lettres correspondant à un filtre de destinataire spécifié), seules les boîtes aux lettres existantes au moment de l'exécution de la commande sont placées en conservation. Si vous créez des boîtes aux lettres par la suite, vous devrez exécuter à nouveau la commande pour les placer en conservation. Si vous créez fréquemment des boîtes aux lettres, vous pouvez exécuter la commande en tant que tâche planifiée aussi souvent que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5298f-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="5298f-189">Le placement de toutes les boîtes aux lettres en conservation pour litige peut avoir une incidence considérable sur la taille des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-189">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes.</span></span> <span data-ttu-id="5298f-190">Dans une organisation Exchange Server 2013, planifiez un stockage adéquat pour répondre aux exigences de conservation de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5298f-190">In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="5298f-191">Le dossier éléments récupérables a sa propre limite de stockage, de sorte que les éléments dans le dossier ne sont pas pris en compte dans la limite de stockage de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-191">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit.</span></span> <span data-ttu-id="5298f-192">Comme expliqué précédemment, la conservation des données de boîte aux lettres pendant une longue période entraînera la croissance du dossier éléments récupérables dans la boîte aux lettres et l'archive d'un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5298f-192">As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive.</span></span> <span data-ttu-id="5298f-193">Pour tenir compte de cette augmentation dans Exchange Online, le quota pour le dossier éléments récupérables est automatiquement augmenté de 30 Go à 100 Go lorsque vous placez une boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="5298f-193">To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="5298f-194">Dans Exchange Server 2013, la limite de stockage par défaut pour le dossier éléments récupérables est également de 30 Go.</span><span class="sxs-lookup"><span data-stu-id="5298f-194">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB.</span></span> <span data-ttu-id="5298f-195">Nous vous recommandons de surveiller régulièrement la taille de ce dossier pour vous assurer qu'il n'atteint pas la limite.</span><span class="sxs-lookup"><span data-stu-id="5298f-195">We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit.</span></span> <span data-ttu-id="5298f-196">Pour plus d'informations, consultez la rubrique [dossier éléments récupérables](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="5298f-196">For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="5298f-p120">La commande précédente permettant de placer en conservation toutes les boîtes aux lettres utilise un filtre de destinataire qui renvoie toutes les boîtes aux lettres d'utilisateurs. Vous pouvez utiliser d'autres propriétés de destinataire pour renvoyer une liste de boîtes aux lettres spécifiques que vous pouvez ensuite rediriger vers la cmdlet **Set-Mailbox** pour placer une conservation pour litige sur ces boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5298f-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="5298f-p121">Voici quelques exemples d'utilisation des cmdlets **Get-Mailbox** et **Get-Recipient** pour renvoyer un sous-ensemble de boîtes aux lettres sur la base de propriétés de boîte aux lettres ou d'utilisateur courantes. Ces exemples supposent que les propriétés de boîte aux lettres appropriées (telles que  _CustomAttributeN_ ou  _Department_) aient été renseignées.</span><span class="sxs-lookup"><span data-stu-id="5298f-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    <span data-ttu-id="5298f-p122">Vous pouvez utiliser d'autres propriétés de boîte aux lettres utilisateur dans un filtre pour inclure ou exclure des boîtes aux lettres. Pour plus d'informations, voir [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="5298f-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

