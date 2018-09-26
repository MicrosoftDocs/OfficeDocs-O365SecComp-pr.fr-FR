---
title: Créer un litige dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037957"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="ade19-102">Créer un litige dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ade19-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="ade19-p101">Vous pouvez placer une boîte aux lettres en conservation pour litige à conserver tous les contenus de boîte aux lettres, notamment les éléments supprimés et les versions d’origine d’éléments modifiés. Lorsque vous placez une boîte aux lettres utilisateur litige, contenu dans la boîte aux lettres de l’utilisateur archive (si elle est activée) est également conservé. Lorsque vous créez une suspension, vous pouvez spécifier une durée d’attente (également appelée une *archive temporaire*) afin que supprimés et les éléments modifiés sont conservés pendant une période spécifiée et suppression définitive de la boîte aux lettres. Ou vous pouvez simplement conserver le contenu indéfiniment (appelé une *attente infinie*) ou jusqu'à ce que le litige est supprimé. Si vous ne spécifiez pas une durée de suspension, il est calculée à partir de la date de réception d’un message ou un élément de boîte aux lettres est créé.</span><span class="sxs-lookup"><span data-stu-id="ade19-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="ade19-108">C’est ici que se passe-t-il lorsque vous créez un litige.</span><span class="sxs-lookup"><span data-stu-id="ade19-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="ade19-109">Éléments sont définitivement supprimés par l’utilisateur sont conservées dans le dossier éléments récupérables de boîte aux lettres de l’utilisateur pendant la durée de la suspension.</span><span class="sxs-lookup"><span data-stu-id="ade19-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="ade19-110">Les éléments qui sont supprimés du dossier éléments récupérables par l’utilisateur sont conservés pendant la durée de la suspension.</span><span class="sxs-lookup"><span data-stu-id="ade19-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="ade19-111">Le quota de stockage pour le dossier éléments récupérables est passent de 30 Go à 110 Go.</span><span class="sxs-lookup"><span data-stu-id="ade19-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="ade19-112">Éléments de principal de l’utilisateur et les boîtes aux lettres d’archivage sont conservés.</span><span class="sxs-lookup"><span data-stu-id="ade19-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="ade19-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ade19-113">Before you begin</span></span>

- <span data-ttu-id="ade19-p102">Pour placer une boîte aux lettres Exchange Online litige, il doit être attribué une licence Exchange Online Plan 2. Si une boîte aux lettres est attribué une licence Exchange Online Plan 1, vous devrez affecter maintenez une licence séparée de l’archivage Exchange Online à placer dans.</span><span class="sxs-lookup"><span data-stu-id="ade19-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="ade19-116">Placer une boîte aux lettres en conservation pour litige dans le centre d’administration d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ade19-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="ade19-117">Voici les étapes pour placer une boîtes aux lettres en conservation pour litige utilisant le centre d’administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="ade19-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="ade19-118">Accédez à https://portal.office.com/adminportal/home et connectez-vous à l’aide de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="ade19-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="ade19-119">Cliquez sur **utilisateurs** > **utilisateurs actifs** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="ade19-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="ade19-120">Sélectionnez l’utilisateur de boîte aux lettres que vous souhaitez mettre en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="ade19-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="ade19-121">Dans la page volants, cliquez sur **paramètres de messagerie**, puis cliquez sur **Modifier** en regard de **litige**.</span><span class="sxs-lookup"><span data-stu-id="ade19-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="ade19-122">Dans la page **litige** , cliquez sur le bouton pour activer litige et effectuer les paramètres facultatifs suivants qui sont affichent :</span><span class="sxs-lookup"><span data-stu-id="ade19-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1.png](media/O365-LitigationHold1.png)

    <span data-ttu-id="ade19-p103">a **durée de suspension (jours)** -Utilisez cette boîte pour créer une suspension basé sur le temps et spécifier la durée de conservation des éléments de boîte aux lettres lors de la boîte aux lettres est mis en attente pour litige. La durée est calculée à partir de la date d’un élément de boîte aux lettres est reçu ou créé. Si vous laissez ce champ vide, les éléments sont conservés indéfiniment ou jusqu'à ce que le blocage est supprimé. Jours permet de spécifier la durée.</span><span class="sxs-lookup"><span data-stu-id="ade19-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="ade19-p104">b. **Remarque** - Utilisez cette boîte pour informer l’utilisateur à leur boîte aux lettres est litige. La note apparaît dans la page informations de compte dans la boîte aux lettres de l’utilisateur s’il utilise Outlook 2010 ou version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur le **fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="ade19-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="ade19-p105">c. **page Web** - Utilisez cette boîte pour diriger l’utilisateur vers un site Web pour plus d’informations sur le litige. Cette URL apparaît dans la page informations de compte dans la boîte aux lettres de l’utilisateur s’ils utilisent Outlook 2010 ou version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur le **fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="ade19-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="ade19-137">Cliquez sur **Enregistrer** pour créer le litige.</span><span class="sxs-lookup"><span data-stu-id="ade19-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="ade19-138">Après avoir créé la suspension, les paramètres de messagerie dans la page volants montre que litige est activé pour l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ade19-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2.png](media/O365-LitigationHold2.png)

<span data-ttu-id="ade19-140">Pour plus d’informations sur la création et la gestion des suspensions en cas de litige et à l’aide d’Exchange Online PowerShell pour litige contient création en bloc, voir [archive une boîte aux lettres en conservation pour litige](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="ade19-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
