---
title: Créer une suspension pour litige dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218654"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="1f0d3-102">Créer une suspension pour litige dans Office 365</span><span class="sxs-lookup"><span data-stu-id="1f0d3-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="1f0d3-p101">Vous pouvez placer une boîte aux lettres en conservation pour litige pour conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés et les versions d'origine des éléments modifiés. Lorsque vous placez une boîte aux lettres utilisateur en conservation pour litige, le contenu de la boîte aux lettres d'archivage de l'utilisateur (si elle est activée) est également conservé. Lorsque vous créez une suspension, vous pouvez spécifier une durée de conservation (également appelée *conservation basée sur l'heure*) afin que les éléments supprimés et modifiés soient conservés pendant une période spécifiée, puis supprimés définitivement de la boîte aux lettres. Vous pouvez également conserver indéfiniment le contenu (appelé *conservation*infinie) ou jusqu'à ce que la conservation pour litige ne soit supprimée. Si vous spécifiez une période de durée de blocage, elle est calculée à partir de la date de réception d'un message ou de la création d'un élément de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="1f0d3-108">Voici ce qui se passe lorsque vous créez une suspension pour litige.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="1f0d3-109">Les éléments définitivement supprimés par l'utilisateur sont conservés dans le dossier éléments récupérables de la boîte aux lettres de l'utilisateur pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="1f0d3-110">Les éléments purgés du dossier éléments récupérables par l'utilisateur sont conservés pendant la durée de la conservation.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="1f0d3-111">Le quota de stockage pour le dossier éléments récupérables est passé de 30 Go à 110 Go.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="1f0d3-112">Les éléments dans les boîtes aux lettres principale et d'archivage de l'utilisateur sont conservés</span><span class="sxs-lookup"><span data-stu-id="1f0d3-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="1f0d3-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1f0d3-113">Before you begin</span></span>

- <span data-ttu-id="1f0d3-p102">Pour placer une boîte aux lettres Exchange Online en conservation pour litige, une licence Exchange Online plan 2 doit lui être attribuée. Si une licence Exchange Online plan 1 est attribuée à une boîte aux lettres, vous devez lui attribuer une licence d'archivage Exchange Online distincte pour la mettre en attente.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="1f0d3-116">Placer une boîte aux lettres en conservation pour litige dans le centre d'administration Office 365</span><span class="sxs-lookup"><span data-stu-id="1f0d3-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="1f0d3-117">Voici les étapes à suivre pour placer un maibox en conservation pour litige à l'aide du centre d'administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="1f0d3-118">Accédez à https://portal.office.com/adminportal/home et connectez-vous à l'aide de votre compte d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="1f0d3-119">Cliquez sur utilisateurs**actifs** dans le volet de navigation de gauche. \*\*\*\* > </span><span class="sxs-lookup"><span data-stu-id="1f0d3-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="1f0d3-120">Sélectionnez l'utilisateur dont vous souhaitez placer la boîte aux lettres en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="1f0d3-121">Sur la page de survol, cliquez sur **paramètres de messagerie**, puis cliquez sur **modifier** en regard de **conservation pour litige**.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="1f0d3-122">Sur la page **conservation pour litige** , cliquez sur le bouton bascule pour activer la conservation pour litige et renseignez les paramètres facultatifs suivants qui sont affichés:</span><span class="sxs-lookup"><span data-stu-id="1f0d3-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    <span data-ttu-id="1f0d3-p103">a. **Hold durée (jours)** : cette zone permet de créer une conservation basée sur le temps et de spécifier la durée pendant laquelle les éléments de boîte aux lettres sont conservés lorsque la boîte aux lettres est placée en conservation pour litige. La durée est calculée à partir de la date de réception ou de création d'un élément de boîte aux lettres. Si vous laissez cette zone vide, les éléments sont conservés indéfiniment ou jusqu'à ce que la conservation soit supprimée. Utilisez l'intervalle jours pour spécifier la durée.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="1f0d3-p104">b. **note** : cette zone permet d'informer l'utilisateur que sa boîte aux lettres est en conservation pour litige. La note apparaît sur la page informations sur le compte dans la boîte aux lettres de l'utilisateur si elle utilise Outlook 2010 ou une version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="1f0d3-p105">c. **page Web** : utilisez cette zone pour diriger l'utilisateur vers un site Web pour obtenir plus d'informations sur la conservation pour litige. Cette URL apparaît sur la page informations sur le compte dans la boîte aux lettres de l'utilisateur, si elle utilise Outlook 2010 ou une version ultérieure. Pour accéder à cette page, les utilisateurs peuvent cliquer sur **fichier** dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="1f0d3-137">Cliquez sur **Enregistrer** pour créer la conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="1f0d3-138">Une fois la conservation créée, les paramètres de messagerie de la page de survol indiquent que la conservation pour litige est activée pour l'utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1f0d3-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

<span data-ttu-id="1f0d3-140">Pour plus d'informations sur la création et la gestion des conservations pour litige et sur l'utilisation d'Exchange Online PowerShell pour créer en bloc des conservations pour litige, consultez [la rubrique placer une boîte aux lettres en conservation pour litige](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="1f0d3-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
