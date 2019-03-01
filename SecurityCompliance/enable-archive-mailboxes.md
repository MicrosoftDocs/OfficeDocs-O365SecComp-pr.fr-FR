---
title: Activer les boîtes aux lettres d'archivage dans &amp; le centre de sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Utilisez le centre de sécurité &amp; conformité d'Office 365 pour activer les boîtes aux lettres d'archivage afin de prendre en charge les exigences de rétention, eDiscovery et de conservation des messages de votre organisation.
ms.openlocfilehash: 39cd5fd8d7991b787d95e39e4994dc9b0786522c
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341795"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="fb402-103">Activer les boîtes aux lettres d'archivage dans &amp; le centre de sécurité conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="fb402-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="fb402-p101">L'archivage dans Office 365 (également appelé archivage inaltérable) fournit aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire. Une fois que vous avez activé les boîtes aux lettres d'archivage, les utilisateurs peuvent accéder aux messages et les stocker dans leurs boîtes aux lettres d'archivage à l'aide de Microsoft Outlook et Outlook sur le Web (anciennement Outlook Web App). Les utilisateurs peuvent également déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d'archivage. Ils peuvent également récupérer des éléments supprimés du dossier éléments récupérables dans leur boîte aux lettres d'archivage à l'aide de l'outil récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="fb402-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App). Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="fb402-p102">Office 365 offre une quantité illimitée de stockage d'archives grâce à la fonctionnalité d'archivage à extension automatique. Lorsque l'archivage à extension automatique est activé, puis que le quota de stockage initial dans la boîte aux lettres d'archivage d'un utilisateur est atteint, Office 365 ajoute automatiquement de l'espace de stockage supplémentaire. Cela signifie que les utilisateurs ne manqueront pas d'espace de stockage de boîte aux lettres et que vous n'aurez pas à gérer les éléments après l'activation initiale de la boîte aux lettres d'archivage et activez l'archivage à extension automatique pour votre organisation. Pour plus d'informations, reportez-vous à la rubrique [Overview of Unlimited Archiving in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="fb402-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="fb402-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fb402-112">Before you begin</span></span>

<span data-ttu-id="fb402-p103">Vous devez disposer du rôle destinataires de messagerie dans Exchange Online pour activer ou désactiver les boîtes aux lettres d'archivage. Par défaut, ce rôle est affecté aux groupes de rôles Gestion des destinataires et gestion de l'organisation dans la page **autorisations** du centre d'administration Exchange. Si vous ne voyez pas la page d' **Archive** dans &amp; le centre de sécurité conformité, demandez à votre administrateur de vous accorder les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fb402-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="fb402-116">Activation d'une boîte aux lettres d'archivage</span><span class="sxs-lookup"><span data-stu-id="fb402-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="fb402-117">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="fb402-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="fb402-118">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="fb402-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="fb402-119">Dans le volet gauche du centre de &amp; sécurité conformité, cliquez sur **Archives**de **gouvernance** \> des données.</span><span class="sxs-lookup"><span data-stu-id="fb402-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="fb402-p104">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb402-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="fb402-122">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Cliquez sur activer dans le volet d'informations de l'utilisateur sélectionné pour activer la boîte aux lettres d'archivage.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="fb402-124">Dans le volet d'informations de l'utilisateur sélectionné, cliquez sur **activer**.</span><span class="sxs-lookup"><span data-stu-id="fb402-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="fb402-p105">Un avertissement s'affiche indiquant que si vous activez la boîte aux lettres d'archivage, les éléments de la boîte aux lettres de l'utilisateur qui sont antérieurs à la stratégie d'archivage affectée à la boîte aux lettres seront déplacés vers la nouvelle boîte aux lettres d'archivage. La stratégie d'archivage par défaut qui fait partie de la stratégie de rétention attribuée aux boîtes aux lettres Exchange Online déplace des éléments vers la boîte aux lettres d'archivage deux ans après la date à laquelle l'élément a été remis à la boîte aux lettres ou créé par l'utilisateur. Pour plus d'informations, reportez-vous à la section **plus** d'informations de cet article.</span><span class="sxs-lookup"><span data-stu-id="fb402-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="fb402-128">Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="fb402-p106">La création de la boîte aux lettres d'archivage peut prendre quelques instants. Lors de sa création, la **boîte aux lettres d'archivage: activée** s'affiche dans le volet d'informations de l'utilisateur sélectionné. Vous devrez peut-être \*\*\*\* ![cliquer sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour les informations dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="fb402-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="fb402-p107">Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails. </span><span class="sxs-lookup"><span data-stu-id="fb402-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="fb402-134">Désactiver une boîte aux lettres d'archivage</span><span class="sxs-lookup"><span data-stu-id="fb402-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="fb402-p108">Vous pouvez également utiliser la page **Archive** du centre de &amp; sécurité conformité pour désactiver la boîte aux lettres d'archivage d'un utilisateur. Une fois que vous avez désactivé une boîte aux lettres d'archivage, vous pouvez la reconnecter à la boîte aux lettres principale de l'utilisateur dans les 30 jours qui suivent sa désactivation. Dans ce cas, le contenu d'origine de la boîte aux lettres d'archivage est restauré. Après 30 jours, le contenu de la boîte aux lettres d'archivage d'origine est supprimé définitivement et ne peut pas être récupéré. Par conséquent, si vous réactivez l'archive plus de 30 jours après l'avoir désactivée, une nouvelle boîte aux lettres d'archivage est créée.</span><span class="sxs-lookup"><span data-stu-id="fb402-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="fb402-p109">Notez que la stratégie d'archivage par défaut affectée aux boîtes aux lettres des utilisateurs déplace les éléments vers la boîte aux lettres d'archivage deux ans après la date de remise de l'élément. Si vous désactivez la boîte aux lettres d'archivage d'un utilisateur, aucune action n'est effectuée sur les éléments de boîte aux lettres et ils resteront dans la boîte aux lettres principale de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb402-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="fb402-142">Pour désactiver une boîte aux lettres d'archivage:</span><span class="sxs-lookup"><span data-stu-id="fb402-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="fb402-143">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="fb402-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="fb402-144">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="fb402-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="fb402-145">Dans le volet gauche du centre de &amp; sécurité conformité, cliquez sur **Archives**de **gouvernance** \> des données.</span><span class="sxs-lookup"><span data-stu-id="fb402-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="fb402-p110">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb402-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="fb402-148">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="fb402-149">Dans le volet des détails, cliquez sur **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="fb402-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="fb402-150">Un message d'avertissement s'affiche indiquant que vous aurez 30 jours pour réactiver la boîte aux lettres d'archivage et qu'après 30 jours, toutes les informations dans l'archive seront définitivement supprimées.</span><span class="sxs-lookup"><span data-stu-id="fb402-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="fb402-151">Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="fb402-p111">La désactivation de la boîte aux lettres d'archivage peut prendre quelques instants. Lorsqu'elle est désactivée, la **boîte aux lettres** d'archivage est affichée dans le volet d'informations de l'utilisateur sélectionné. Vous devrez peut-être \*\*\*\* ![cliquer sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour les informations dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="fb402-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="fb402-p112">Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails. </span><span class="sxs-lookup"><span data-stu-id="fb402-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="fb402-157">Utiliser Exchange Online PowerShell pour activer ou désactiver les boîtes aux lettres d'archivage</span><span class="sxs-lookup"><span data-stu-id="fb402-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="fb402-p113">Vous pouvez également utiliser Exchange Online PowerShell pour activer les boîtes aux lettres d'archivage. La principale raison d'utiliser PowerShell est que vous pouvez rapidement activer la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fb402-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="fb402-p114">La première étape consiste à vous connecter à Exchange Online PowerShell. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="fb402-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="fb402-162">Une fois que vous êtes connecté à Exchange Online, vous pouvez exécuter les commandes des sections suivantes pour activer ou désactiver les boîtes aux lettres d'archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="fb402-163">Activation des boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="fb402-163">Enable archive mailboxes</span></span>

<span data-ttu-id="fb402-164">Exécutez la commande suivante pour activer la boîte aux lettres d'archivage pour un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb402-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="fb402-165">Exécutez la commande suivante pour activer la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation (dont la boîte aux lettres d'archivage n'est pas activée actuellement).</span><span class="sxs-lookup"><span data-stu-id="fb402-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="fb402-166">Désactivation des boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="fb402-166">Disable archive mailboxes</span></span>

<span data-ttu-id="fb402-167">Exécutez la commande suivante pour désactiver la boîte aux lettres d'archivage pour un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb402-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="fb402-168">Exécutez la commande suivante pour désactiver la boîte aux lettres d'archivage pour tous les utilisateurs de votre organisation (dont la boîte aux lettres d'archivage est activée).</span><span class="sxs-lookup"><span data-stu-id="fb402-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="fb402-169">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="fb402-169">More information</span></span>
  
- <span data-ttu-id="fb402-p115">Les boîtes aux lettres d'archivage vous permettent, ainsi qu'à vos utilisateurs, de répondre aux exigences de rétention, de découverte électronique et de conservation de votre organisation. Par exemple, vous pouvez utiliser la stratégie de rétention Exchange de votre organisation pour déplacer le contenu de boîte aux lettres vers la boîte aux lettres d'archivage des utilisateurs. Lorsque vous utilisez l'outil de recherche de contenu dans &amp; le centre de sécurité conformité pour rechercher du contenu spécifique dans la boîte aux lettres d'un utilisateur, la boîte aux lettres d'archivage de l'utilisateur est également recherchée. En outre, lorsque vous placez une conservation pour litige ou que vous appliquez une stratégie de rétention Office 365 à la boîte aux lettres d'un utilisateur, les éléments de la boîte aux lettres d'archivage sont également conservés.</span><span class="sxs-lookup"><span data-stu-id="fb402-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="fb402-p116">Lorsqu'une boîte aux lettres d'archivage est activée, les utilisateurs peuvent stocker des messages dans leur boîte aux lettres d'archivage. Les utilisateurs peuvent accéder à leurs boîtes aux lettres d'archivage à l'aide de Microsoft Outlook et d'Outlook sur le Web. À l'aide de l'une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d'archivage et déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d'archivage. Les utilisateurs peuvent également récupérer des éléments supprimés du dossier éléments récupérables dans leur boîte aux lettres d'archivage à l'aide de l'outil récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="fb402-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="fb402-p117">Une fois les boîtes aux lettres d'archivage activées, votre organisation peut tirer parti de la stratégie de rétention Exchange par défaut (également appelée gestion des enregistrements de messagerie ou stratégie MRM) qui est automatiquement affectée à chaque boîte aux lettres. Lorsqu'une boîte aux lettres d'archivage est activée, la stratégie de rétention Exchange par défaut effectue automatiquement les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="fb402-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="fb402-180">Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d'un utilisateur à sa boîte aux lettres d'archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="fb402-181">Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l'utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage.</span><span class="sxs-lookup"><span data-stu-id="fb402-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="fb402-182">Pour plus d'informations sur les boîtes aux lettres d'archivage et les stratégies de rétention Exchange, voir:</span><span class="sxs-lookup"><span data-stu-id="fb402-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
    
  - [<span data-ttu-id="fb402-183">Balises et stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="fb402-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="fb402-184">Stratégie de réTention par défaut dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fb402-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="fb402-185">Configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres de votre organisation Office 365</span><span class="sxs-lookup"><span data-stu-id="fb402-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
