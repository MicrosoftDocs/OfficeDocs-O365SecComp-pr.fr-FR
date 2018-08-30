---
title: Augmenter le quota des éléments récupérables pour les boîtes aux lettres placées en conservation
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Activer la boîte aux lettres d’archive et activer l’archivage pour augmenter la taille du dossier éléments récupérables pour une boîte aux lettres dans Office 365 développer automatiquement. '
ms.openlocfilehash: 2e7149ef10152a11dc638c04b61a261440b539b8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527627"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="a584a-103">Augmenter le quota des éléments récupérables pour les boîtes aux lettres placées en conservation</span><span class="sxs-lookup"><span data-stu-id="a584a-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="a584a-p101">La stratégie de rétention par défaut, appelée stratégie MRM par défaut, qui est appliquées automatiquement vers les nouvelles boîtes aux lettres dans Exchange Online contient une balise de rétention nommé récupérables éléments 14 jours déplacement vers l’archive. Cette balise de rétention déplace les éléments à partir du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur dans le dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive l’expiration de la période de rétention de 14 jours pour un élément. Pour ce faire, la boîte aux lettres de l’utilisateur archive doit être activé. Si la boîte aux lettres d’archivage n’est pas activé, aucune action, ce qui signifie que les éléments dans les éléments récupérables blocage du dossier à une boîte aux lettres ne sont pas déplacés vers la boîte aux lettres d’archivage après expiration de la période de rétention de 14 jours. Rien n’est supprimé à partir d’une boîte aux lettres en attente, il est possible que le quota de stockage pour le dossier éléments récupérables peut être dépassé, surtout si la boîte aux lettres de l’utilisateur archive n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="a584a-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="a584a-p102">Pour réduire le risque de dépassement de cette limite, le quota de stockage pour le dossier éléments récupérables est automatiquement augmenté de 30 Go à 100 Go lors d’une suspension est placée dans une boîte aux lettres dans Exchange Online. Si la boîte aux lettres d’archive est activé, le quota de stockage pour le dossier éléments récupérables dans la boîte aux lettres d’archive est également passent de 30 Go à 100 Go. Si l’archivage automatique-développement des fonctionnalités dans Exchange Online est activé, le quota de stockage pour le dossier éléments récupérables dans l’archive de l’utilisateur sera illimité.</span><span class="sxs-lookup"><span data-stu-id="a584a-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="a584a-112"> Le tableau suivant résume le quota de stockage pour le dossier Éléments récupérables.</span><span class="sxs-lookup"><span data-stu-id="a584a-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="a584a-113">**Emplacement du dossier Éléments récupérables**</span><span class="sxs-lookup"><span data-stu-id="a584a-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="a584a-114">**Boîtes aux lettres non placées en conservation**</span><span class="sxs-lookup"><span data-stu-id="a584a-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="a584a-115">**Boîtes aux lettres placées en conservation**</span><span class="sxs-lookup"><span data-stu-id="a584a-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a584a-116">Boîte aux lettres principale</span><span class="sxs-lookup"><span data-stu-id="a584a-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="a584a-117">30 Go</span><span class="sxs-lookup"><span data-stu-id="a584a-117">30 GB</span></span>  <br/> |<span data-ttu-id="a584a-118">100 Go</span><span class="sxs-lookup"><span data-stu-id="a584a-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="a584a-119">Boîte aux lettres d’archive<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a584a-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="a584a-120">Illimité</span><span class="sxs-lookup"><span data-stu-id="a584a-120">Unlimited</span></span>  <br/> |<span data-ttu-id="a584a-121">Illimité</span><span class="sxs-lookup"><span data-stu-id="a584a-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="a584a-122">**Quota de stockage total pour le dossier Éléments récupérables**</span><span class="sxs-lookup"><span data-stu-id="a584a-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="a584a-123">Illimité</span><span class="sxs-lookup"><span data-stu-id="a584a-123">Unlimited</span></span>  <br/> |<span data-ttu-id="a584a-124">Illimité</span><span class="sxs-lookup"><span data-stu-id="a584a-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a584a-p103"><sup>\*</sup>Quota de stockage initial de la boîte aux lettres d’archive est de 100 Go pour les utilisateurs disposant d’une licence Exchange Online (Plan 2). Toutefois, lors de l’extension automatique d’archivage est activé, le quota de stockage pour l’archivage de l’utilisateur et le dossier éléments récupérables dans l’archive est illimité. Pour plus d’informations sur l’extension automatique d’archivage, consultez la rubrique [vue d’ensemble de l’archivage illimité dans Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="a584a-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on, the storage quota for the user's archive and the Recoverable Items folder in the archive is unlimited. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="a584a-128">Lorsque le quota de stockage pour le dossier Éléments récupérables dans la boîte aux lettres principale d’une boîte aux lettres placée en conservation est proche de sa limite, vous pouvez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a584a-128">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="a584a-p104">**Activer la boîte aux lettres d’archivage et d’activer l’archivage automatique-développement** - vous pouvez activer une capacité de stockage illimitée pour le dossier éléments récupérables simplement par l’activation de la boîte aux lettres d’archive et puis activer la fonctionnalité d’archivage automatique-développement dans Exchange En ligne. Le résultat de 100 Go pour le dossier éléments récupérables dans la boîte aux lettres principale et un nombre illimité de capacité de stockage pour le dossier éléments récupérables dans l’archive de l’utilisateur. Voir comment : [Activer les boîtes aux lettres archive de sécurité Office 365 &amp; centre de conformité](enable-archive-mailboxes.md) et [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="a584a-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 100 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a584a-p105">Après avoir activé l’archivage pour une boîte aux lettres qui est proche dépassant le quota de stockage pour le dossier éléments récupérables, vous voudrez peut-être exécuter l’Assistant dossier géré pour déclencher manuellement l’assistant pour traiter la boîte aux lettres afin que les éléments arrivés à expiration sont déplacés le Dossier éléments récupérables dans la boîte aux lettres d’archive. Pour plus d’informations, voir [l’étape 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Notez que les autres éléments de boîte aux lettres de l’utilisateur peuvent être déplacés vers la nouvelle boîte aux lettres d’archive. Prendre en compte pour présenter à l’utilisateur que cela peut se produire après l’activation de la boîte aux lettres d’archive.</span><span class="sxs-lookup"><span data-stu-id="a584a-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="a584a-p106">**Créer une stratégie de rétention personnalisée pour les boîtes aux lettres sur Maintenez** - outre l’activation de la boîte aux lettres d’archive et développer automatiquement l’archivage pour les boîtes aux lettres sur un litige ou blocage sur Place, vous pourriez également créer une stratégie de rétention personnalisée pour les boîtes aux lettres sur mettre en attente. Cela nous allons vous appliquer une stratégie de rétention aux boîtes aux lettres en attente qui diffère de la stratégie MRM par défaut qui est appliqué aux boîtes aux lettres qui ne sont pas en attente. Cela vous permet pour appliquer des balises de rétention sont spécialement conçues pour les boîtes aux lettres en attente. Cela comprend la création d’une nouvelle balise de rétention du dossier éléments récupérables.</span><span class="sxs-lookup"><span data-stu-id="a584a-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="a584a-140">Le reste de cette rubrique décrit les procédures détaillées de création d’une stratégie de rétention personnalisée pour les boîtes aux lettres placées en conservation.</span><span class="sxs-lookup"><span data-stu-id="a584a-140">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="a584a-141">Étape 1 : Création d’une balise de rétention pour le dossier Éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="a584a-141">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="a584a-142">[[Étape 2 : créer une nouvelle stratégie de rétention des boîtes aux lettres en attente](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="a584a-142">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="a584a-143">Étape 3 : Application de la nouvelle stratégie de rétention aux boîtes aux lettres placées en conservation</span><span class="sxs-lookup"><span data-stu-id="a584a-143">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="a584a-144">(Facultatif) Étape 4 : Exécution de l’Assistant Dossier géré pour appliquer les nouveaux paramètres de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-144">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="a584a-145">Étape 1 : Création d’une balise de rétention personnalisée pour le dossier Éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="a584a-145">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="a584a-p107">La première étape consiste à créer une balise de rétention personnalisée (appelée balise de stratégie de rétention ou RPT) pour le dossier éléments récupérables. Comme expliqué précédemment, ce rapport déplace les éléments à partir du dossier éléments récupérables dans la boîte aux lettres principale de l’utilisateur dans le dossier éléments récupérables dans la boîte aux lettres de l’utilisateur archive. Vous devez utiliser PowerShell pour créer un rapport pour le dossier éléments récupérables. Vous ne pouvez pas utiliser le centre d’administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="a584a-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. [<span data-ttu-id="a584a-150">Connect to Exchange Online using remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="a584a-150">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. <span data-ttu-id="a584a-151">Exécutez la commande suivante pour créer une balise de stratégie de rétention pour le dossier Éléments récupérables : </span><span class="sxs-lookup"><span data-stu-id="a584a-151">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="a584a-p108">Par exemple, la commande suivante crée une balise de stratégie de rétention pour le dossier Éléments récupérables nommée « Éléments récupérables 30 jours pour les boîtes aux lettres en conservation », avec une période de rétention de 30 jours. Cela signifie que 30 jours après qu’un élément a été placé dans le dossier Éléments récupérables, il est déplacé vers le dossier Éléments récupérables de la boîte aux lettres d’archivage de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a584a-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="a584a-p109">Il est recommandé que la période de rétention (définie par le paramètre _AgeLimitForRetention_ ) pour le rapport éléments récupérables est la même que la période de rétention des éléments supprimés pour les boîtes aux lettres qui est appliquée à l’arborescence RPT. Cela permet à un utilisateur la période de rétention des éléments supprimés ensemble pour récupérer des éléments supprimés avant qu’ils sont déplacés vers la boîte aux lettres d’archive. Dans l’exemple précédent, la période de rétention a été définie sur 30 jours basés sur l’hypothèse que la période de rétention des éléments supprimés pour les boîtes aux lettres est également de 30 jours. Une boîte aux lettres Exchange Online est configuré pour conserver les éléments supprimés pendant 14 jours par défaut. Mais vous pouvez modifier ce paramètre pour un maximum de 30 jours. Pour plus d’informations, voir [Modifier la période de rétention des éléments supprimés pour une boîte aux lettres dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span><span class="sxs-lookup"><span data-stu-id="a584a-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="a584a-160">Étape 2 : Création d’une stratégie de rétention pour les boîtes aux lettres placées en conservation</span><span class="sxs-lookup"><span data-stu-id="a584a-160">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="a584a-p110">L’étape suivante consiste à créer une stratégie de rétention et à lui ajouter des balises de rétention, y compris la balise de stratégie de rétention des éléments récupérables que vous avez créée à l’étape 1. Cette nouvelle stratégie sera appliquée aux boîtes aux lettres placées en conservation dans l’étape suivante. </span><span class="sxs-lookup"><span data-stu-id="a584a-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="a584a-p111">Avant de créer la stratégie de rétention, déterminez les balises de rétention supplémentaires que vous souhaitez ajouter. Pour obtenir une liste des balises de rétention qui sont ajoutées à la stratégie MRM par défaut et pour plus d’informations sur la création des balises de rétention, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a584a-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="a584a-165">Valeur par défaut de la stratégie de rétention dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a584a-165">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="a584a-166">Dossiers par défaut prenant en charge les balises de stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-166">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="a584a-167">La section « Créer une balise de rétention » dans la rubrique [créer une stratégie de rétention](https://go.microsoft.com/fwlink/p/?LinkId=404422) .</span><span class="sxs-lookup"><span data-stu-id="a584a-167">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="a584a-168">Vous pouvez utiliser le centre d’administration Exchange ou Exchange Online PowerShell pour créer une stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="a584a-168">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="a584a-169">Utilisation du Centre d'administration Exchange pour créer une stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-169">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="a584a-170">Dans le CAE, accédez à **gestion de la conformité** \> de **stratégies de rétention**, puis cliquez sur **Ajouter** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="a584a-170">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="a584a-171">Sur la page **Nouvelle stratégie de rétention**, sous **Nom**, saisissez un nom qui décrit l’objectif de la stratégie de rétention ; par exemple, **MRM Policy for Mailboxes on Hold**. </span><span class="sxs-lookup"><span data-stu-id="a584a-171">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="a584a-172">Sous **les balises de rétention**, cliquez sur **Ajouter** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="a584a-172">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="a584a-173">Dans la liste des balises de rétention, sélectionnez la balise de stratégie de rétention des éléments récupérables que vous avez créée à l’étape 1, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a584a-173">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![Sélectionnez la balise de rétention Éléments récupérables personnalisée](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="a584a-p112">Sélectionnez des balises de rétention supplémentaires à ajouter à la stratégie de rétention. Par exemple, vous pouvez ajouter les mêmes balises qui sont incluses dans la stratégie MRM par défaut.</span><span class="sxs-lookup"><span data-stu-id="a584a-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="a584a-177">Lorsque vous avez fini d’ajouter les balises de rétention, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a584a-177">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="a584a-178">Cliquez sur **Enregistrer** pour créer la stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="a584a-178">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="a584a-179">Les balises de rétention liées à la stratégie de rétention sont affichées dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="a584a-179">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![Des balises de conservation liées à la stratégie de rétention sont affichées dans le volet de détails](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="a584a-181">Utiliser Exchange Online PowerShell pour créer une stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-181">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="a584a-182">Exécutez la commande suivante pour créer une stratégie de rétention pour les boîtes aux lettres placées en conservation. </span><span class="sxs-lookup"><span data-stu-id="a584a-182">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="a584a-183">Par exemple, la commande suivante crée la stratégie de rétention et les balises de rétention liées qui sont présentées dans l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="a584a-183">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="a584a-184">Étape 3 : Application de la nouvelle stratégie de rétention aux boîtes aux lettres placées en conservation</span><span class="sxs-lookup"><span data-stu-id="a584a-184">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="a584a-p113">La dernière étape consiste à appliquer la nouvelle stratégie de rétention que vous avez créé à l’étape 2 pour les boîtes aux lettres en attente dans votre organisation. Vous pouvez utiliser le centre d’administration Exchange ou Exchange Online PowerShell pour appliquer la stratégie de rétention à une boîte aux lettres unique ou à plusieurs boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a584a-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="a584a-187">Utilisation du Centre d’administration Exchange pour appliquer la nouvelle stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-187">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="a584a-188">Accédez à **Destinataires**\> **Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="a584a-188">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="a584a-189">Dans la liste affichée, sélectionnez la boîte aux lettres que vous voulez appliquer la stratégie de rétention à, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="a584a-189">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="a584a-190">Sur la page **Boîte aux lettres de l’utilisateur**, cliquez sur **Fonctionnalités de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="a584a-190">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="a584a-191">Sous **Stratégie de rétention**, sélectionnez la stratégie de rétention que vous avez créée à l’étape 2, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a584a-191">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="a584a-192">Vous pouvez aussi utiliser le Centre d’administration Exchange pour appliquer la stratégie de rétention à plusieurs boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a584a-192">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="a584a-193">Accédez à **Destinataires**\> **Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="a584a-193">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="a584a-194">Dans la liste affichée, utilisez les touches Maj ou Ctrl pour sélectionner plusieurs boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a584a-194">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="a584a-195">Dans le volet d'informations, cliquez sur **Plus d'options**.</span><span class="sxs-lookup"><span data-stu-id="a584a-195">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="a584a-196">Sous **Stratégie de rétention**, cliquez sur **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="a584a-196">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="a584a-197">Sur la page **Attribuer la stratégie de rétention en bloc**, sélectionnez la stratégie de rétention que vous avez créée à l’étape 2, puis cliquez sur **Enregistrer**. </span><span class="sxs-lookup"><span data-stu-id="a584a-197">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="a584a-198">Utiliser Exchange Online PowerShell pour appliquer la nouvelle stratégie de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-198">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="a584a-p114">Vous pouvez utiliser Exchange Online PowerShell pour appliquer une nouvelle stratégie de rétention à une seule boîte aux lettres. Mais la puissance de PowerShell est que vous pouvez l’utiliser pour identifier rapidement toutes les boîtes aux lettres dans votre organisation qui sont en attente pour litige ou blocage sur Place, puis appliquent la nouvelle stratégie de rétention à toutes les boîtes aux lettres sur blocage dans une seule commande. Voici quelques exemples d’utilisation de PowerShell Exchange pour appliquer une stratégie de rétention à une ou plusieurs boîtes aux lettres. Tous les exemples appliquent la stratégie de rétention qui a été créée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a584a-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="a584a-203">Cet exemple applique la nouvelle stratégie de rétention à la boîte aux lettres de Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="a584a-203">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="a584a-204">Cet exemple applique la nouvelle stratégie de rétention à toutes les boîtes aux lettres de l’organisation qui sont placées en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="a584a-204">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="a584a-205">Cet exemple applique la nouvelle stratégie de rétention à toutes les boîtes aux lettres de l’organisation qui sont placées en conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a584a-205">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="a584a-206">Vous pouvez utiliser la cmdlet **Get-Mailbox** pour vérifier que la nouvelle stratégie de rétention a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="a584a-206">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="a584a-207">Voici quelques exemples pour vérifier que les commandes des exemples précédents appliquent la stratégie de rétention « stratégie MRM pour les boîtes aux lettres en conservation » aux boîtes aux lettres placées en conservation sur litige et aux boîtes aux lettres en conservation inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a584a-207">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="a584a-208">(Facultatif) Étape 4 : Exécution de l’Assistant Dossier géré pour appliquer les nouveaux paramètres de rétention</span><span class="sxs-lookup"><span data-stu-id="a584a-208">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="a584a-p115">Après avoir appliqué la nouvelle stratégie de rétention aux boîtes aux lettres en attente, il peut prendre jusqu'à sept jours dans Exchange Online pour l’Assistant dossier géré à traiter ces boîtes aux lettres en utilisant les paramètres de la nouvelle stratégie de rétention. Au lieu d’attendre exécuter l’Assistant dossier géré, vous pouvez utiliser l’applet de commande **Start-ManagedFolderAssistant** pour déclencher manuellement l’assistant pour traiter les boîtes aux lettres que vous avez appliqué à la nouvelle stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="a584a-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="a584a-211">Exécutez la commande suivante pour démarrer l’Assistant Dossier géré pour la boîte aux lettres de Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="a584a-211">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="a584a-212">Exécutez les commandes suivantes pour démarrer l’Assistant Dossier géré pour toutes les boîtes aux lettres placées en conservation.</span><span class="sxs-lookup"><span data-stu-id="a584a-212">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="a584a-213">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="a584a-213">More information</span></span>

- <span data-ttu-id="a584a-p116">Une fois que la boîte aux lettres de l’utilisateur archive, prenez en compte pour présenter à l’utilisateur que les autres éléments dans leur boîte aux lettres (pas seulement les éléments dans le dossier éléments récupérables) peuvent être déplacés vers la boîte aux lettres d’archive. Il s’agit, car la stratégie MRM par défaut qui est affecté à des boîtes aux lettres Exchange Online contient une balise de rétention (nommé par défaut de 2 ans à déplacer vers l’archive) qui déplace les éléments dans la boîte aux lettres d’archive deux ans après la date de l’élément a été remis à la boîte aux lettres ou créé par le utilisateur. Pour plus d’informations, voir [Stratégie de rétention par défaut dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span><span class="sxs-lookup"><span data-stu-id="a584a-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="a584a-p117">Une fois que la boîte aux lettres de l’utilisateur archive, vous pourrez également indiquer à l’utilisateur qu’ils peuvent récupérer les éléments supprimés dans le dossier éléments récupérables dans leur boîte aux lettres d’archive. Cela dans Outlook en sélectionnant le dossier **Éléments supprimés** dans la boîte aux lettres d’archivage, puis en cliquant sur **Récupérer les éléments supprimés de serveur** sous l’onglet **accueil** . Pour plus d’informations sur la récupération des éléments supprimés, consultez la rubrique [récupérer les éléments supprimés dans Outlook pour Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span><span class="sxs-lookup"><span data-stu-id="a584a-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
