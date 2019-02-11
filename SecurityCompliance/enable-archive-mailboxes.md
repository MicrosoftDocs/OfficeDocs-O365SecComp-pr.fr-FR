---
title: Activer des boîtes aux lettres d’archive de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Utilisez le Office 365 Security &amp; centre de conformité pour activer des boîtes aux lettres d’archive de prise en charge de la rétention des messages de votre organisation, eDiscovery, maintenir des exigences.
ms.openlocfilehash: 1c290cf19b396221dac702efd1395911e8a51631
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327096"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="7b5d7-103">Activer des boîtes aux lettres d’archive de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="7b5d7-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="7b5d7-p101">L’archivage dans Office 365 (également appelée In-Place Archiving) fournit aux utilisateurs d’espace de stockage des boîtes aux lettres supplémentaires. Une fois que vous allumez boîtes aux lettres d’archivage, les utilisateurs peuvent accéder et stocker des messages dans leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et les utilisateurs d’Outlook Web App peut également déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d’archive. Ils peuvent également récupérer des éléments supprimés à partir du dossier éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil de récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook Web App. Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="7b5d7-p102">Office 365 propose un nombre illimité de stockage d’archives avec la fonctionnalité d’archivage automatique en expansion. Lorsque développer automatiquement l’archivage est activé, puis le quota de stockage initiale dans la boîte aux lettres de l’utilisateur archive est atteint, Office 365 ajoute automatiquement espace de stockage supplémentaire. Cela signifie que les utilisateurs ne seront pas exécutés en dehors de l’espace de stockage de boîtes aux lettres et vous n’aurez pas à gérer les rien après avoir initialement activer la boîte aux lettres d’archive et activer l’archivage pour votre organisation développer automatiquement. Pour plus d’informations, voir [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="7b5d7-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7b5d7-112">Before you begin</span></span>

<span data-ttu-id="7b5d7-p103">Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online pour activer ou désactiver des boîtes aux lettres d’archive. Par défaut, ce rôle est attribué aux groupes de rôles gestion des destinataires et la gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Si vous ne voyez pas la page **d’Archive** dans la sécurité &amp; du centre de conformité, demandez à votre administrateur vous assignez les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="7b5d7-116">Activation d'une boîte aux lettres d'archivage</span><span class="sxs-lookup"><span data-stu-id="7b5d7-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="7b5d7-117">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7b5d7-118">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="7b5d7-119">Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="7b5d7-p104">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="7b5d7-122">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Cliquez sur Activer dans le volet de détails de l’utilisateur sélectionné pour activer la boîte aux lettres d’archive](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="7b5d7-124">Dans le volet de détails de l’utilisateur sélectionné, cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="7b5d7-p105">Un avertissement s’affiche indiquant que si vous activez la boîte aux lettres d’archivage, les éléments de boîte aux lettres de l’utilisateur qui sont antérieurs à la stratégie d’archivage attribuée à la boîte aux lettres seront déplacées vers la nouvelle boîte aux lettres d’archive. La stratégie d’archivage par défaut qui fait partie de la stratégie de rétention affectée à des boîtes aux lettres Exchange Online déplace des éléments vers la boîte aux lettres d’archive deux ans après la date de l’élément a été remis à la boîte aux lettres ou créé par l’utilisateur. Pour plus d’informations, consultez la section **informations supplémentaires** dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="7b5d7-128">Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="7b5d7-p106">Elle peut prendre quelques instants pour créer la boîte aux lettres d’archive. Lors de sa création, **boîte aux lettres d’Archive : activé** s’affiche dans le volet de détails de l’utilisateur sélectionné. Vous devrez peut-être cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="7b5d7-p107">Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails. </span><span class="sxs-lookup"><span data-stu-id="7b5d7-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="7b5d7-134">Désactiver une boîte aux lettres d'archivage</span><span class="sxs-lookup"><span data-stu-id="7b5d7-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="7b5d7-p108">Vous pouvez également utiliser la page **Archive** dans la sécurité &amp; centre de conformité pour désactiver la boîte aux lettres de l’utilisateur archive. Une fois que vous avez désactivé une boîte aux lettres d’archivage, vous pouvez vous reconnecter à la boîte aux lettres principale de l’utilisateur dans les 30 jours de le désactiver. Dans ce cas, le contenu d’origine de la boîte aux lettres d’archivage est restauré. Après 30 jours, le contenu de la boîte aux lettres d’archive d’origine est supprimé définitivement et ne peuvent pas être récupéré. Si vous réactivez l’archive plus de 30 jours après l’avoir désactivé, une nouvelle boîte aux lettres d’archive est créé.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="7b5d7-p109">Notez que la stratégie d’archivage par défaut attribué aux boîtes aux lettres des utilisateurs déplace les éléments dans la boîte aux lettres d’archive deux ans après la date de l’élément est remis. Si vous désactivez les boîtes aux lettres de l’utilisateur archive, aucune action ne sera entreprise sur les éléments de boîte aux lettres et qu’ils restent dans la boîte aux lettres principale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="7b5d7-142">Pour désactiver une boîte aux lettres d’archivage :</span><span class="sxs-lookup"><span data-stu-id="7b5d7-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="7b5d7-143">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7b5d7-144">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="7b5d7-145">Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="7b5d7-p110">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="7b5d7-148">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="7b5d7-149">Dans le volet des détails, cliquez sur **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="7b5d7-150">Un message d’avertissement s’affiche indiquant que vous aurez 30 jours pour réactiver la boîte aux lettres d’archivage et qu’après 30 jours, toutes les informations dans l’archive seront définitivement supprimées.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="7b5d7-151">Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="7b5d7-p111">Elle peut prendre quelques instants pour désactiver la boîte aux lettres d’archive. Lorsqu’il est désactivé, **boîte aux lettres d’Archive : désactivé** s’affiche dans le volet de détails de l’utilisateur sélectionné. Vous devrez peut-être cliquer sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="7b5d7-p112">Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails. </span><span class="sxs-lookup"><span data-stu-id="7b5d7-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="7b5d7-157">Utiliser Exchange Online PowerShell pour activer ou désactiver des boîtes aux lettres d’archive</span><span class="sxs-lookup"><span data-stu-id="7b5d7-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="7b5d7-p113">Vous pouvez également utiliser Exchange Online PowerShell pour activer des boîtes aux lettres d’archive. La raison principale à utiliser PowerShell est que vous pouvez activer rapidement la boîte aux lettres d’archive pour tous les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="7b5d7-p114">La première étape consiste à se connecter à Exchange Online PowerShell. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="7b5d7-162">Une fois que vous êtes connecté à Exchange Online, vous pouvez exécuter les commandes dans les sections suivantes pour activer ou désactiver des boîtes aux lettres d’archive.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="7b5d7-163">Activation des boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="7b5d7-163">Enable archive mailboxes</span></span>

<span data-ttu-id="7b5d7-164">Exécutez la commande suivante pour activer la boîte aux lettres d’archivage pour un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="7b5d7-165">Exécutez la commande suivante pour activer la boîte aux lettres d’archive pour tous les utilisateurs de votre organisation (boîte aux lettres d’archivage n’est actuellement pas activée).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="7b5d7-166">Désactivation des boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="7b5d7-166">Disable archive mailboxes</span></span>

<span data-ttu-id="7b5d7-167">Exécutez la commande suivante pour désactiver la boîte aux lettres d’archivage pour un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="7b5d7-168">Exécutez la commande suivante pour désactiver la boîte aux lettres d’archive pour tous les utilisateurs de votre organisation (boîte aux lettres d’archive est actuellement activé).</span><span class="sxs-lookup"><span data-stu-id="7b5d7-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="7b5d7-169">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7b5d7-169">More information</span></span>
  
- <span data-ttu-id="7b5d7-p115">Boîtes aux lettres d’archive aider à vous et vos utilisateurs pour répondre à la rétention de votre organisation, eDiscovery et maintenez la configuration requise. Par exemple, vous pouvez utiliser la stratégie de rétention de votre organisation Exchange pour déplacer le contenu de la boîte aux lettres boîte aux lettres d’archivage des utilisateurs. Lorsque vous utilisez l’outil de recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher les boîtes aux lettres d’un utilisateur pour un contenu spécifique, boîte aux lettres de l’utilisateur archive sera également recherché. Et, lorsque vous placez un litige ou appliquez une stratégie de rétention Office 365 pour les boîtes aux lettres d’un utilisateur, les éléments dans la boîte aux lettres d’archivage sont également conservées.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="7b5d7-p116">Lorsqu’une boîte aux lettres d’archive est activé, les utilisateurs peuvent stocker des messages dans leur boîte aux lettres d’archive. Les utilisateurs peuvent accéder leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et Outlook Web App en utilisant une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d’archivage et de déplacer ou copier des messages entre leur boîte aux lettres principale et leur boîte aux lettres d’archive. Les utilisateurs peuvent également récupérer les éléments supprimés du dossier éléments récupérables dans leur boîte aux lettres d’archive à l’aide de l’outil de récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook Web App. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="7b5d7-p117">Une fois l’archivage de boîtes aux lettres sont activées, votre organisation peut tirer parti de la stratégie par défaut Exchange rétention (également appelée stratégie de gestion des enregistrements de messagerie ou MRM) qui est automatiquement attribuée à chaque boîte aux lettres. Lorsqu’une boîte aux lettres d’archive est activé, la stratégie de rétention par défaut Exchange automatiquement les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b5d7-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="7b5d7-180">Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d'un utilisateur à sa boîte aux lettres d'archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="7b5d7-181">Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l'utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d'archivage.</span><span class="sxs-lookup"><span data-stu-id="7b5d7-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="7b5d7-182">Pour plus d’informations sur les boîtes aux lettres d’archive et des stratégies de rétention d’Exchange, voir :</span><span class="sxs-lookup"><span data-stu-id="7b5d7-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="7b5d7-183">Balises et stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="7b5d7-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="7b5d7-184">Valeur par défaut de la stratégie de rétention dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7b5d7-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="7b5d7-185">Configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365</span><span class="sxs-lookup"><span data-stu-id="7b5d7-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
