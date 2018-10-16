---
title: Supprimer des éléments dans le dossier éléments récupérables de nuage des boîtes aux lettres en attente - aide d’administration
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Pour les administrateurs : supprimer des éléments dans le dossier des éléments récupérables d’un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres se trouve en conservation légale. Il s’agit d’un moyen efficace pour supprimer les données sont répandues par inadvertance dans Office 365.'
ms.openlocfilehash: 9174e953ebdd7f0032f411b99a814aeacd880a1e
ms.sourcegitcommit: dd58ed6fd424272e361bc3c109ecd6d63d673048
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "25566885"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="ddcdd-104">Supprimer des éléments dans le dossier éléments récupérables de nuage des boîtes aux lettres en attente - aide d’administration</span><span class="sxs-lookup"><span data-stu-id="ddcdd-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="ddcdd-p102">Le dossier éléments récupérables pour une boîte aux lettres Exchange Online existe pour protéger contre les suppressions accidentelles ou malveillantes. Il est également utilisé pour stocker les éléments qui sont conservés et accessibles par les fonctionnalités de conformité d’Office 365, telles que le blocage et eDiscovery recherches. Toutefois, dans certaines situations, organisations peut-être été involontairement conservées dans le dossier éléments récupérables qui ils doivent supprimer des données. Par exemple, un utilisateur peut envoyer sans le savoir ou transférer un message électronique qui contient des informations sensibles ou qui peut avoir des conséquences graves. Même si le message est définitivement supprimé, il peut être conservée indéfiniment car une conservation légale a été placée dans la boîte aux lettres. Ce scénario est appelé débordements de données, car les données a été involontairement répandues dans Office 365. Dans ce cas, vous pouvez supprimer des éléments dans le dossier des éléments récupérables d’un utilisateur pour une boîte aux lettres Exchange Online, même si cette boîte aux lettres est mis en attente avec l’une des fonctionnalités de blocage différents dans Office 365. Ces types de suspensions comprennent contient des litiges, archives permanentes, suspensions eDiscovery et des stratégies de rétention Office 365 créés de sécurité Office 365 &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="ddcdd-p103">Cet article explique comment supprimer des éléments dans le dossier éléments récupérables pour les boîtes aux lettres en nuage qui sont en attente. Cette procédure implique la désactivation de l’accès à la boîte aux lettres et de désactivation de récupération d’élément unique, désactivation de l’Assistant dossier géré à partir de la boîte aux lettres de traitement, supprimer temporairement la suspension, supprimer des éléments à partir du dossier éléments récupérables et retour puis la boîte aux lettres à sa configuration précédente. Voici le processus :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="ddcdd-116">Étape 1 : Collecter des informations sur la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="ddcdd-117">Étape 2 : Préparation de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="ddcdd-118">Étape 3 : Suppression de toutes les suspensions à partir de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="ddcdd-119">Étape 4 : Supprimer la suspension de délai d’attente de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="ddcdd-120">Étape 5 : Supprimer des éléments dans le dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="ddcdd-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="ddcdd-121">Étape 6 : Rétablir la boîte aux lettres à son état précédent</span><span class="sxs-lookup"><span data-stu-id="ddcdd-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="ddcdd-p104">Les procédures décrites dans cet article entraînera données définitivement supprimés (définitivement) à partir d’une boîte aux lettres Exchange Online. Cela signifie que les messages que vous supprimez à partir du dossier éléments récupérables ne peuvent pas être récupérés et ne sont pas disponibles pour la récupération sur demande juridique ou autres à des fins de conformité. Si vous souhaitez supprimer des messages à partir d’une boîte aux lettres qui est mis en attente dans le cadre d’un litige, blocage sur Place, maintenez la touche e-Discovery, ou stratégie de rétention Office 365 créée de sécurité Office 365 &amp; centre de conformité, vérifiez auprès de votre gestion des enregistrements ou le département juridique Services avant la suppression de la suspension. Votre organisation peut avoir une stratégie qui définit si une boîte aux lettres sur blocage ou un incident débordements de données est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="ddcdd-126">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ddcdd-126">Before you begin</span></span>

- <span data-ttu-id="ddcdd-127">Vous devez être affectées à la fois des rôles de gestion suivants dans Exchange Online pour rechercher et supprimer des messages à partir du dossier éléments récupérables à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="ddcdd-p105">**Recherche de boîte aux lettres** - ce rôle permet pour rechercher les boîtes aux lettres dans votre organisation. Les administrateurs Exchange ne sont pas affectés à ce rôle par défaut. Pour assigner vous-même ce rôle, ajoutez-vous en tant que membre du groupe de rôles de gestion de la découverte dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="ddcdd-p106">**Boîte aux lettres importer exporter** : ce rôle permet à pour supprimer des messages de boîte aux lettres d’un utilisateur. Par défaut, ce rôle n’est pas affecté à un groupe de rôles. Pour supprimer les messages des boîtes aux lettres des utilisateurs, vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="ddcdd-p107">La procédure décrite dans cet article n’est pas pris en charge pour les boîtes aux lettres inactives. C'est-à-dire, car vous ne pouvez pas réappliquer une attente (ou la stratégie de rétention Office 365) à une boîte aux lettres inactive après que l’avoir supprimé. Lorsque vous supprimez une suspension à partir d’une boîte aux lettres inactive, elle est remplacée par une boîte aux lettres supprimée normal et est définitivement supprimé de votre organisation après son traitement par l’Assistant dossier géré.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="ddcdd-p108">Vous ne pouvez pas effectuer cette procédure pour une boîte aux lettres qui a été affecté à une stratégie de rétention d’Office 365 verrouillée avec un verrou de conservation. C’est parce qu’un verrou de conservation vous empêche de suppression ou à l’exception de la boîte aux lettres à partir de la stratégie de rétention Office 365 et de désactiver l’Assistant dossier géré sur la boîte aux lettres. Pour plus d’informations sur le verrouillage des stratégies de rétention, voir [verrouillage d’une stratégie de rétention](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="ddcdd-p109">Si une boîte aux lettres n’est pas mis en attente (ou ne possède pas de récupération d’élément unique), vous pouvez simplement supprimer les éléments du dossier éléments récupérables. Pour plus d’informations, voir [Rechercher et supprimer les messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="ddcdd-142">Étape 1 : Collecter des informations sur la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="ddcdd-p110">Cette première étape consiste à collecter les propriétés sélectionnées à partir de la boîte aux lettres cible auront une incidence sur cette procédure. Veillez à noter ces paramètres ou de les enregistrer dans un fichier texte, car vous allez modifier certaines de ces propriétés et puis rétablir les valeurs d’origine à l’étape 6, après la suppression d’éléments à partir du dossier éléments récupérables. Voici une liste des propriétés de boîte aux lettres que vous devez recueillir.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="ddcdd-146">*SingleItemRecoveryEnabled* et *RetainDeletedItemsFor* ; Si nécessaire, vous devez désactiver la récupération unique et augmenter la période de rétention des éléments supprimés à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="ddcdd-p111">*LitigationHoldEnabled* et *InPlaceHolds* ; Vous devez identifier toutes les suspensions placées sur la boîte aux lettres afin que vous pouvez les supprimer temporairement à l’étape 3. Voir la section [plus d’informations](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) pour obtenir des conseils sur la façon d’identifier la suspension de type qui peut-être être placée sur une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="ddcdd-p112">En outre, vous devez obtenir les paramètres d’accès client de la boîte aux lettres afin que vous pouvez temporairement désactiver afin que le propriétaire (ou autres utilisateurs) ne peut pas accéder à la boîte aux lettres au cours de cette procédure. Enfin, vous pouvez obtenir la taille actuelle et le nombre d’éléments dans le dossier éléments récupérables. Après la suppression d’éléments dans le dossier éléments récupérables à l’étape 5, vous allez utiliser ces informations pour vérifier que les éléments ont été supprimées réellement.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="ddcdd-p113">[Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Veillez à utiliser un nom d’utilisateur et le mot de passe pour un compte d’administrateur qui a été affecté les rôles de gestion dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="ddcdd-154">Exécutez la commande suivante pour obtenir des informations sur la récupération d’élément unique et la période de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="ddcdd-p114">Si la récupération d’élément unique est activée, vous devrez désactiver à l’étape 2. Si la période de rétention des éléments supprimés n’est pas définie pour des 30 derniers jours (la valeur maximale dans Exchange Online), puis vous pouvez augmenter à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="ddcdd-157">Exécutez la commande suivante pour obtenir des paramètres d’accès pour la boîte aux lettres de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="ddcdd-158">Vous allez désactiver toutes ces méthodes d’accès à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="ddcdd-159">Exécutez la commande suivante pour obtenir des informations sur les suspensions appliquées à la boîte aux lettres de stratégies de rétention Office 365.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="ddcdd-160">S’il existe trop grand nombre de valeurs dans la propriété *InPlaceHolds* et tous les s’affichent, vous pouvez exécuter la `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque valeur sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="ddcdd-161">Exécutez la commande suivante pour obtenir des informations sur les stratégies de rétention d’Office 365 à l’échelle de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="ddcdd-162">Si votre organisation dispose des stratégies de rétention à l’échelle de l’organisation Office 365, vous devrez exclure la boîte aux lettres de ces stratégies à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="ddcdd-163">S’il existe trop grand nombre de valeurs dans la propriété *InPlaceHolds* et tous les s’affichent, vous pouvez exécuter la `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` commande pour afficher chaque valeur sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="ddcdd-164">Exécutez la commande suivante pour obtenir la taille actuelle et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="ddcdd-165">Si la boîte aux lettres de l’utilisateur archive est activé, exécutez la commande suivante pour obtenir la taille et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans leur boîte aux lettres d’archive.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="ddcdd-p115">Lorsque vous supprimez des éléments à l’étape 5, vous pouvez choisir de supprimer ou pas supprimer des éléments dans le dossier éléments récupérables de boîte aux lettres de l’utilisateur principal d’archivage. Notez que si l’extension automatique d’archivage est activé pour la boîte aux lettres, les éléments dans une boîte aux lettres d’archive auxiliaire ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="ddcdd-168">Étape 2 : Préparation de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="ddcdd-169">Après la collecte et l’enregistrement des informations sur la boîte aux lettres, l’étape suivante consiste à préparer la boîte aux lettres en effectuant les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="ddcdd-170">**Désactiver l’accès client aux boîtes aux lettres** afin que le propriétaire de la boîte aux lettres ne peut pas accéder à leur boîte aux lettres et apportez des modifications aux données de boîte aux lettres au cours de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="ddcdd-171">**Augmenter la période de rétention des éléments supprimés** de 30 jours (la valeur maximale dans Exchange Online) afin que les éléments ne sont pas supprimés du dossier éléments récupérables avant de les supprimer à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="ddcdd-172">**Désactiver la récupération d’élément unique** afin que les articles ne seront pas conservées (pendant la durée de la période de rétention des éléments supprimés) après leur suppression à partir du dossier éléments récupérables à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="ddcdd-173">**Désactiver l’Assistant dossier géré** afin qu’elle ne traiter la boîte aux lettres et conserver les éléments supprimés à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="ddcdd-174">Dans Exchange Online PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="ddcdd-p116">Exécutez la commande suivante pour désactiver tous les accès au client à la boîte aux lettres. La syntaxe de la commande suppose que toutes les méthodes d’accès client ont été activés dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="ddcdd-p117">Cela peut prendre jusqu'à 60 minutes pour désactiver toutes les méthodes d’accès client pour la boîte aux lettres. Notez que la désactivation de ces méthodes d’accès ne déconnecter le propriétaire de boîte aux lettres qu'ils êtes actuellement connectés. Si le propriétaire n’est pas connecté, puis ils ne pourront accéder à leur boîte aux lettres après que ces méthodes d’accès sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="ddcdd-p118">Exécutez la commande suivante pour augmenter la période de rétention des éléments supprimés de la valeur maximale de 30 jours. Cela suppose que la valeur actuelle est inférieure à 30 jours.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="ddcdd-182">Exécutez la commande suivante pour désactiver la récupération d’élément unique.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="ddcdd-p119">Cela peut prendre jusqu'à 60 minutes pour désactiver la récupération d’élément unique. Ne pas supprimer des éléments dans le dossier éléments récupérables jusqu'à ce que cette période écoulée.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="ddcdd-p120">Exécutez la commande suivante pour empêcher l’Assistant dossier géré de traiter la boîte aux lettres. Comme expliqué précédemment, vous pouvez désactiver l’Assistant dossier géré uniquement si une stratégie de rétention d’Office 365 avec un verrou de conservation n’est pas appliquée à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="ddcdd-187">Étape 3 : Suppression de toutes les suspensions à partir de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="ddcdd-p121">Avant de pouvoir supprimer des éléments à partir du dossier éléments récupérables de la dernière étape consiste à supprimer toutes les suspensions (que vous avez identifié à l’étape 1) placées sur la boîte aux lettres. Toutes les suspensions doivent être supprimées afin que les éléments ne seront pas conservées après leur suppression à partir du dossier éléments récupérables. Les sections suivantes contiennent des informations sur la suppression de différents types de suspensions sur une boîte aux lettres. Voir la section [plus d’informations](#more-information) pour obtenir des conseils sur la façon d’identifier la suspension de type qui peut-être être placée sur une boîte aux lettres. Pour plus d’informations, voir [Comment faire pour identifier le type de blocage placé dans une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="ddcdd-193">Comme indiqué précédemment, vérifiez auprès de votre gestion des enregistrements ou les services juridiques avant la suppression d’une suspension à partir d’une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="ddcdd-194">Conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="ddcdd-194">Litigation Hold</span></span>
  
<span data-ttu-id="ddcdd-195">Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer un litige à partir de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="ddcdd-p122">Semblable à la désactivation de la récupération d’élément unique et les méthodes d’accès client, il peut prendre jusqu'à 60 minutes pour supprimer le litige. Ne pas supprimer des éléments à partir du dossier éléments récupérables jusqu'à ce que cette période écoulée.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="ddcdd-198">Blocage local</span><span class="sxs-lookup"><span data-stu-id="ddcdd-198">In-Place Hold</span></span>
  
<span data-ttu-id="ddcdd-p123">Exécutez la commande suivante dans Exchange Online PowerShell pour identifier la In-Place Hold qui est placé sur la boîte aux lettres. Utilisez le GUID pour la conservation inaltérable que vous avez identifié à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="ddcdd-p124">Après avoir identifié la conservation inaltérable, vous pouvez utiliser le centre d’administration Exchange (EAC) ou Exchange Online PowerShell pour supprimer la boîte aux lettres de la suspension. Pour plus d’informations, voir [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="ddcdd-203">Office 365 de rétention appliquée à des boîtes aux lettres spécifiques</span><span class="sxs-lookup"><span data-stu-id="ddcdd-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="ddcdd-p125">Exécutez la commande suivante [Office 365 sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la stratégie de rétention d’Office 365 est appliquée à la boîte aux lettres. Utilisez le GUID (non compris le `mbx` ou `skp` préfixe) pour la stratégie de rétention que vous avez identifié à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="ddcdd-206">Après avoir identifié la stratégie de rétention, accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifiez la stratégie de rétention que vous avez identifié à l’étape précédente et supprimer la boîte aux lettres à partir de la liste des destinataires qui sont inclus dans la stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="ddcdd-207">Stratégies de rétention de l’organisation Office 365</span><span class="sxs-lookup"><span data-stu-id="ddcdd-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="ddcdd-p126">Échelle de l’organisation et les stratégies de rétention à l’échelle Exchange Office 365 sont appliquées à chaque boîte aux lettres dans l’organisation. Ils sont appliqués au niveau de l’organisation (et non le niveau de boîte aux lettres) et sont renvoyées lorsque vous exécutez l’applet de commande **Get-OrganizationConfig** à l’étape 1. Exécutez la commande suivante [sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier les stratégies de rétention d’Office 365 à l’échelle de l’organisation. Utilisez le GUID (non compris le `mbx` préfixe) pour les stratégies de rétention de l’organisation que vous avez identifié à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="ddcdd-p127">Après avoir identifié les stratégies de rétention de l’organisation Office 365, accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifier chaque stratégie de rétention de l’organisation que vous avez identifié dans la précédente étape, puis ajoutez la boîte aux lettres à la liste des destinataires exclus. Cette opération supprimera boîte aux lettres de l’utilisateur de la stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="ddcdd-214">Étiquettes de rétention d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ddcdd-214">Office 365 retention labels</span></span>

<span data-ttu-id="ddcdd-p128">Chaque fois qu’un utilisateur s’applique une étiquette qui est configurée pour conserver le contenu ou conserver et puis supprimer le contenu à un dossier ou un élément dans leur boîte aux lettres, la propriété de la boîte aux lettres *ComplianceTagHoldApplied* est définie sur **True**. Dans ce cas, la boîte aux lettres est considéré comme être mise en attente, comme s’il a été mis en attente pour litige ou affecté à une stratégie de rétention d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="ddcdd-217">Pour afficher la valeur de la propriété *ComplianceTagHoldApplied* , exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="ddcdd-p129">Une fois que vous avez identifié qu’une boîte aux lettres est sur en attente, car une étiquette de rétention est appliquée à un dossier ou un élément, vous pouvez utiliser l’outil de recherche de contenu dans la sécurité et centre de conformité pour rechercher les éléments étiquetés à l’aide de la condition de recherche ComplianceTag. Pour plus d’informations, consultez la section « Conditions de recherche » dans les [requêtes de mot clé et les conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="ddcdd-220">Pour plus d’informations sur les étiquettes, voir [vue d’ensemble d’Office 365 étiquettes](labels.md).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="ddcdd-221">contient des cas de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="ddcdd-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="ddcdd-p130">Exécutez les commandes suivantes [sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/?linkid=627084) pour identifier la suspension associée à un cas de découverte électronique qui est appliqué à la boîte aux lettres. Utilisez le GUID (non compris le `UniH` préfixe) pour la découverte électronique maintenez que vous avez identifié à l’étape 1. Notez que la deuxième commande affiche le nom du cas eDiscovery que la suspension associée ; la troisième commande affiche le nom de la suspension.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="ddcdd-p131">Une fois que vous avez identifié le nom de la casse eDiscovery et la suspension, accédez à la **recherche &amp; enquête** \> page de **découverte électronique** dans la sécurité &amp; centre de conformité, ouvrez le cas et supprimer la boîte aux lettres de la suspension. Pour plus d’informations, voir [gérer des affaires eDiscovery de sécurité Office 365 &amp; centre de conformité](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="ddcdd-227">Étape 4 : Supprimer la suspension de délai d’attente de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ddcdd-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="ddcdd-p132">Une fois que n’importe quel type de suspension est supprimé d’une boîte aux lettres, la valeur de la propriété de la boîte aux lettres *DelayHoldApplied* est définie sur **True**. Est appelé un *délai de blocage* et signifie que la suppression effective de la suspension est différée pendant 30 jours empêcher les données d’être définitivement supprimés (définitivement) de la boîte aux lettres.   Lorsque le délai est suspendu sur la boîte aux lettres, la boîte aux lettres est considérée en attente pour une durée illimitée, en tant que si la boîte aux lettres a été litige. (L’objectif d’une suspension du délai d’attente est Administrateurs de donner la possibilité permet de rechercher ou de récupérer des éléments de boîte aux lettres qui seront purgés après la suppression d’une suspension.) Noe qu’après 30 jours, le délai d’attente expire et Office 365 tente automatiquement de supprimer la suspension de délai d’attente (en définissant la propriété *DelayHoldApplied* sur **False**) afin que le blocage soit réellement supprimé.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This is called a *delay hold* and means that the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted (purged) from the mailbox.   When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.) Noe that after 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold will be actually removed.</span></span> 

<span data-ttu-id="ddcdd-p133">Avant de pouvoir supprimer des éléments à l’étape 5, vous devez supprimer la suspension de délai d’attente de la boîte aux lettres. Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer la suspension de délai d’attente :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. Run the following command in Exchange Online PowerShell to remove the delay hold:</span></span> 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="ddcdd-234">Notez que vous devez être affecté au rôle suspens pour raisons juridiques dans Exchange Online à utiliser le paramètre *RemoveDelayHoldApplied* .</span><span class="sxs-lookup"><span data-stu-id="ddcdd-234">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

<span data-ttu-id="ddcdd-235">Pour vérifier que la suspension du délai d’attente a été supprimée, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-235">To verify that delay hold has been removed, run the following command.</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="ddcdd-236">La valeur **False** pour la propriété *DelayHoldApplied* indique le délai a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-236">The value of **False** for the *DelayHoldApplied* property indicates the delay has been removed.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="ddcdd-237">Étape 5 : Supprimer des éléments dans le dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="ddcdd-237">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="ddcdd-p134">Vous êtes maintenant prêt à supprimer les éléments dans le dossier éléments récupérables à l’aide de l’applet de commande [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) dans Exchange Online PowerShell. Vous disposez de trois options lors de l’exécution de l’applet de commande **Search-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p134">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="ddcdd-240">Copier des éléments dans une boîte aux lettres cible avant de les supprimer afin que vous pouvez consulter les articles, si nécessaire, avant de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-240">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="ddcdd-241">Copier des éléments dans une boîte aux lettres cible et les supprimer dans la même commande.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-241">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="ddcdd-242">Supprimer des éléments sans les copier dans une boîte aux lettres cible.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-242">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="ddcdd-p135">Notez que les éléments dans le dossier éléments récupérables de boîte aux lettres de l’utilisateur principal d’archivage est également supprimé lorsque vous exécutez le \*\* Search-Mailbox \*\* applet de commande. Pour éviter ce problème, vous pouvez inclure le commutateur *DoNotIncludeArchive* . Et comme indiqué précédemment, si l’extension automatique d’archivage est activé pour la boîte aux lettres, les \*\* Search-Mailbox \*\* applet de commande ne les éléments supprimés dans une boîte aux lettres d’archive auxiliaire. Pour plus d’informations sur l’extension automatique d’archivage, consultez la rubrique [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p135">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the \*\* Search-Mailbox \*\* cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ddcdd-p136">Si vous incluez une requête de recherche (à l'aide du paramètre  *SearchQuery*  ), la cmdlet **Search-Mailbox** renverra au maximum 10 000 éléments dans les résultats de recherche. Ainsi, si vous incluez une requête de recherche, vous devrez peut-être exécuter la commande **Search-Mailbox** plusieurs fois pour supprimer plus de 10 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p136">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="ddcdd-p137">Les exemples suivants montrent la syntaxe de commande pour chacune de ces options. Ces exemples utilisent le `-SearchQuery size>0` valeur de paramètre, qui supprime tous les éléments de tous les sous-dossiers du dossier éléments récupérables. Si vous devez supprimer uniquement les éléments qui correspondent aux conditions spécifiques, vous pouvez également utiliser le paramètre *SearchQuery* pour spécifier d’autres conditions, telles que l’objet d’un message ou une plage de dates. Consultez les [autres exemples d’utilisation le paramètre SearchQuery](#other-examples-of-using-the-searchquery-parameter) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p137">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="ddcdd-253">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="ddcdd-253">Example 1</span></span>

<span data-ttu-id="ddcdd-p138">Cet exemple copie tous les éléments dans le dossier éléments récupérables de l’utilisateur dans un dossier de boîte aux lettres de découverte de votre organisation. Cela vous permet de passer en revue les avant de vous les supprimez définitivement.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p138">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="ddcdd-p139">Dans l’exemple précédent, il n’est pas nécessaire de copier des éléments dans la boîte aux lettres de découverte. Vous pouvez copier des messages dans une boîte aux lettres cible. Toutefois, pour empêcher l’accès aux données de boîte aux lettres potentiellement sensibles, il est recommandé de copier des messages dans une boîte aux lettres qui dispose d’un accès limité au personnel autorisé. Par défaut, l’accès à la boîte aux lettres de découverte par défaut est limité aux membres du groupe de rôles de gestion de la découverte dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p139">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="ddcdd-260">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="ddcdd-260">Example 2</span></span>

<span data-ttu-id="ddcdd-261">Cet exemple copie tous les éléments dans le dossier éléments récupérables de l’utilisateur dans un dossier de boîte aux lettres de découverte de votre organisation, puis supprime les éléments du dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-261">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="ddcdd-262">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="ddcdd-262">Example 3</span></span>

<span data-ttu-id="ddcdd-263">Cet exemple supprime tous les éléments dans le dossier éléments récupérables de l’utilisateur, sans les copier dans une boîte aux lettres cible.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-263">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="ddcdd-264">Autres exemples d’utilisation le paramètre SearchQuery</span><span class="sxs-lookup"><span data-stu-id="ddcdd-264">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="ddcdd-p140">Voici quelques exemples d’utilisation le paramètre *SearchQuery* pour rechercher des messages spécifiques. Si vous utilisez le paramètre *SearchQuery* pour rechercher des éléments spécifiques, envisagez de copier les résultats de recherche dans une boîte aux lettres cible afin que vous pouvez examiner les résultats de recherche et ensuite modifier la requête si nécessaire avant de supprimer les résultats d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p140">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="ddcdd-267">Cet exemple renvoie des messages qui contiennent une expression spécifique dans le champ objet.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-267">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="ddcdd-268">Cet exemple renvoie des messages qui ont été envoyés au sein de la plage de dates spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-268">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="ddcdd-269">Cet exemple renvoie des messages qui ont été envoyés à la personne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-269">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="ddcdd-270">Vérifiez que les éléments ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="ddcdd-270">Verify that items were deleted</span></span>

<span data-ttu-id="ddcdd-p141">Pour vérifier que vous avez bien supprimé des éléments à partir du dossier éléments récupérables d’une boîte aux lettres, la cmdlet **Get-MailboxFolderStatistics** dans Exchange Online PowerShell pour vérifier la taille et le nombre d’éléments dans le dossier éléments récupérables. Vous pouvez comparer ces statistiques avec celles que vous avez collectées à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p141">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="ddcdd-273">Pour obtenir la taille actuelle et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur, exécutez la commande suivante dans.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-273">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="ddcdd-274">Exécutez la commande suivante pour obtenir la taille et le nombre total d’éléments dans des dossiers et les sous-dossiers du dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-274">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="ddcdd-275">Étape 6 : Rétablir la boîte aux lettres à son état précédent</span><span class="sxs-lookup"><span data-stu-id="ddcdd-275">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="ddcdd-p142">L’étape finale consiste à rétablir la boîte aux lettres à sa configuration précédente. Cela signifie réinitialiser les propriétés que vous avez modifié à l’étape 2 et réappliquer la suspension que vous avez supprimé à l’étape 3. Cela inclut :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p142">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="ddcdd-p143">Modification de la période de rétention des éléments supprimés retour à sa valeur précédente. Autrement, vous pouvez laissez ce définie sur 30 jours, la valeur maximale dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p143">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="ddcdd-281">Réactivation de récupération d’élément unique.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-281">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="ddcdd-282">Réactivation les méthodes d’accès client afin que le propriétaire peut accéder à leur boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-282">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="ddcdd-283">Réappliquer les suspensions et les stratégies de rétention Office 365 que vous avez supprimé.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-283">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="ddcdd-284">Réactivation de l’Assistant dossier géré pour traiter la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-284">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="ddcdd-285">Nous vous conseillons d’attendre 24 heures après l’application réutilisation d’une suspension ou un Office 365 rétention stratégie (et vérifier qu’il est en place) avant de vous réactivez l’Assistant dossier géré pour traiter la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-285">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="ddcdd-286">Dans Exchange Online PowerShell, procédez comme suit (dans l’ordre spécifié).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-286">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="ddcdd-p144">Exécuter la commande suivante pour modifier la période de rétention des éléments supprimés retour à sa valeur d’origine. Cela suppose que le paramètre précédent est inférieure à 30 jours ; par exemple 14 jours.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p144">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="ddcdd-289">Exécutez la commande suivante pour réactiver récupération d’élément unique.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-289">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="ddcdd-290">Exécutez la commande suivante pour réactiver toutes les méthodes d’accès client pour la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-290">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="ddcdd-p145">Réappliquer la suspension que vous avez supprimé à l’étape 3. Selon le type d’attente, utilisez une des procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p145">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="ddcdd-293">**Conservation pour litige**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-293">**Litigation Hold**</span></span>
    
    <span data-ttu-id="ddcdd-294">Exécutez la commande suivante pour réactiver un litige pour la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-294">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="ddcdd-295">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-295">**In-Place Hold**</span></span>
    
    <span data-ttu-id="ddcdd-296">Utiliser le centre d’administration Exchange (ou Exchange Online PowerShell) pour ajouter la boîte aux lettres à la In-Place Hold.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-296">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="ddcdd-297">**Office 365 de rétention appliquée à des boîtes aux lettres spécifiques**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-297">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="ddcdd-p146">Utilisez la sécurité &amp; centre de conformité pour ajouter la boîte aux lettres à la stratégie de rétention d’Office 365. Accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifiez la stratégie de rétention et ajoutez la boîte aux lettres à la liste de destinataires auxquels la stratégie de rétention est appliquée à.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p146">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="ddcdd-300">**Stratégies de rétention de l’organisation Office 365**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-300">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="ddcdd-p147">Si vous avez supprimé une échelle de l’organisation ou de la stratégie de rétention Exchange à l’échelle par l’exclusion de la stratégie, puis utiliser la sécurité &amp; centre de conformité pour supprimer la boîte aux lettres à partir de la liste d’exclure les utilisateurs. Accédez à la **gouvernance de Date** \> page de **rétention** dans la sécurité &amp; centre de conformité, modifier la stratégie de rétention de l’entreprise et supprimer la boîte aux lettres à partir de la liste des destinataires exclus. Cette opération sera réappliquer la stratégie de rétention aux boîtes aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p147">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="ddcdd-304">**contient des cas de découverte électronique**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-304">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="ddcdd-p148">Utilisez la sécurité &amp; centre de conformité pour ajouter la boîte aux lettres sauvegarder la suspension associé à une affaire eDiscovery. Accédez à la **recherche &amp; enquête** \> page de **découverte électronique** dans la sécurité &amp; centre de conformité, ouvrez le cas et ajoutez la boîte aux lettres à la suspension.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p148">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="ddcdd-p149">Exécutez la commande suivante pour autoriser l’Assistant dossier géré à traiter à nouveau de la boîte aux lettres. Comme indiqué plus haut, nous vous conseillons d’attendre 24 heures après l’application réutilisation d’une suspension ou un Office 365 rétention stratégie (et vérifier qu’il est en place) avant de vous réactivez l’Assistant dossier géré.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p149">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="ddcdd-309">Pour vérifier que la boîte aux lettres a été rétablie à sa configuration précédente, vous pouvez exécuter les commandes suivantes et comparez les paramètres à celles que vous avez collectées à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-309">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="ddcdd-310">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="ddcdd-310">More information</span></span>

<span data-ttu-id="ddcdd-p150">Voici un tableau qui décrit comment identifier les différents types de suspensions en fonction des valeurs dans la propriété *InPlaceHolds* lorsque vous exécutez les applets de commande **Get-Mailbox** ou **Get-OrganizationConfig** . Pour plus d’informations, voir [Comment faire pour identifier le type de blocage placé dans une boîte aux lettres Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p150">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="ddcdd-313">Comme indiqué, vous devez supprimer toutes les suspensions et stratégies de rétention d’Office 365 à partir d’une boîte aux lettres avant de supprimer les éléments dans le dossier éléments récupérables.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-313">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="ddcdd-314">**Type de conservation**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-314">**Hold type**</span></span>|<span data-ttu-id="ddcdd-315">**Exemple de valeur**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-315">**Example value**</span></span>|<span data-ttu-id="ddcdd-316">**Comment identifier la suspension**</span><span class="sxs-lookup"><span data-stu-id="ddcdd-316">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ddcdd-317">Conservation pour litige</span><span class="sxs-lookup"><span data-stu-id="ddcdd-317">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="ddcdd-318">La propriété  *LitigationHoldEnabled*  est définie sur  `True`.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-318">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="ddcdd-319">Blocage local</span><span class="sxs-lookup"><span data-stu-id="ddcdd-319">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="ddcdd-p151">La propriété *InPlaceHolds* contient le GUID de la conservation inaltérable qui est placé sur la boîte aux lettres. Vous pouvez indiquer qu'il s’agit d’une conservation inaltérable, car le GUID ne commence pas par un préfixe.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p151">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="ddcdd-322">Vous pouvez utiliser la commande  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span><span class="sxs-lookup"><span data-stu-id="ddcdd-322">You can use the  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span></span> | <span data-ttu-id="ddcdd-323">FL' command dans Exchange Online PowerShell pour obtenir des informations sur la conservation inaltérable dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-323">FL\` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="ddcdd-324">Stratégies de rétention Office 365 dans la sécurité &amp; centre de conformité appliquée aux boîtes aux lettres spécifiques</span><span class="sxs-lookup"><span data-stu-id="ddcdd-324">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="ddcdd-325">ou</span><span class="sxs-lookup"><span data-stu-id="ddcdd-325">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="ddcdd-p152">Lorsque vous exécutez l’applet de commande **Get-Mailbox** , la propriété *InPlaceHolds* contient également les GUID d’Office 365 les stratégies de rétention appliquées à la boîte aux lettres. Vous pouvez identifier les stratégies de rétention, car le GUID commence par la `mbx` préfixe. Notez que si le GUID de la stratégie de rétention commence par la `skp` préfixe, ce qui indique que la stratégie de rétention est appliquée aux Skype pour des conversations.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p152">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="ddcdd-329">Pour la stratégie de rétention identité Office 365 qui est appliqué à la boîte aux lettres, exécutez la commande suivante dans la sécurité &amp; PowerShell du centre de conformité :</span><span class="sxs-lookup"><span data-stu-id="ddcdd-329">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/><span data-ttu-id="ddcdd-330">« Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="ddcdd-330">\`Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="ddcdd-331">Nom FL`<br/><br/>Be sure to remove the  `mbx` or  `skp' préfixe lorsque vous exécutez cette commande.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-331">FL Name`<br/><br/>Be sure to remove the  `mbx` or  `skp\` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="ddcdd-332">Stratégies de rétention d’Office 365 à l’échelle de l’organisation de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="ddcdd-332">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="ddcdd-333">Aucune valeur</span><span class="sxs-lookup"><span data-stu-id="ddcdd-333">No value</span></span>  <br/> <span data-ttu-id="ddcdd-334">ou</span><span class="sxs-lookup"><span data-stu-id="ddcdd-334">or</span></span>  <br/>  <span data-ttu-id="ddcdd-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(indique que la boîte aux lettres est exclu d’une stratégie de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="ddcdd-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="ddcdd-336">Même si la propriété *InPlaceHolds* est vide lorsque vous exécutez l’applet de commande **Get-Mailbox** , toujours il peut y avoir au moins une échelle de l’organisation Office 365 de rétention appliquée à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="ddcdd-337">Pour vérifier cela, vous pouvez exécuter le « Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="ddcdd-337">To verify this, you can run the  \`Get-OrganizationConfig</span></span> | <span data-ttu-id="ddcdd-338">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="ddcdd-338">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="ddcdd-339">Nom FL`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `mbx -`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696 »</span><span class="sxs-lookup"><span data-stu-id="ddcdd-339">FL Name`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696\`</span></span> <br/> |
|<span data-ttu-id="ddcdd-340">blocage de cas de découverte électronique dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="ddcdd-340">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="ddcdd-p153">La propriété *InPlaceHolds* contient également le GUID de n’importe quel suspension associé à un cas de découverte électronique dans la sécurité &amp; centre de conformité peuvent être placées sur la boîte aux lettres. Vous pouvez indiquer il s’agit d’un blocage cas eDiscovery, car le GUID commence par la `UniH` préfixe.</span><span class="sxs-lookup"><span data-stu-id="ddcdd-p153">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="ddcdd-p154">Vous pouvez utiliser la `Get-CaseHoldPolicy` applet de commande de la sécurité &amp; PowerShell du centre de conformité pour obtenir des informations sur le cas de découverte électronique qui est associée à la suspension de la boîte aux lettres. Par exemple, vous pouvez exécuter la commande « Get-CaseHoldPolicy<hold GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="ddcdd-p154">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  \`Get-CaseHoldPolicy <hold GUID without prefix></span></span> | <span data-ttu-id="ddcdd-345">Nom FL` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/>`$CaseHold.CaseId Get-ComplianceCase</span><span class="sxs-lookup"><span data-stu-id="ddcdd-345">FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId</span></span> | <span data-ttu-id="ddcdd-346">Nom FL'</span><span class="sxs-lookup"><span data-stu-id="ddcdd-346">FL Name\`</span></span>


