---
title: Gestion des utilisateurs de messagerie dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP).
ms.openlocfilehash: 2e266d4dd31c3bd614c1b4f8afa17ca747890385
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692613"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="207a2-103">Gestion des utilisateurs de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="207a2-103">Manage mail users in EOP</span></span>

<span data-ttu-id="207a2-p101">La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP). Vous pouvez gérer les utilisateurs de différentes manières dans EOP.</span><span class="sxs-lookup"><span data-stu-id="207a2-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="207a2-106">Utilisation de la synchronisation d'annuaires pour gérer les utilisateurs de messagerie : si votre entreprise dispose de comptes d'utilisateur dans un environnement Active Directory local, vous pouvez synchroniser ces comptes sur Azure Active Directory (AD), où des copies des comptes sont stockées dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="207a2-106">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud.</span></span> <span data-ttu-id="207a2-107">Lorsque vous synchronisez vos comptes d'utilisateur sur Azure Active Directory, vous pouvez consulter ces utilisateurs dans le volet **Destinataires** du Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="207a2-107">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC).</span></span> <span data-ttu-id="207a2-108">L'utilisation de la synchronisation d'annuaires est recommandée.</span><span class="sxs-lookup"><span data-stu-id="207a2-108">Using directory synchronization is recommended.</span></span> 
    
- <span data-ttu-id="207a2-109">Utilisation du CAE pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="207a2-109">Use the EAC to manage mail users: Add and manage mail users directly in the EAC.</span></span> <span data-ttu-id="207a2-110">Il s'agit du moyen le plus facile pour ajouter des utilisateurs de messagerie et cette méthode est également utile pour ajouter un utilisateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="207a2-110">This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>
    
- <span data-ttu-id="207a2-111">Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie en exécutant Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="207a2-111">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell.</span></span> <span data-ttu-id="207a2-112">Cette méthode est utile pour ajouter plusieurs enregistrements et pour la création de scripts.</span><span class="sxs-lookup"><span data-stu-id="207a2-112">This method is useful for adding multiple records and creating scripts.</span></span>
    
> [!NOTE]
> <span data-ttu-id="207a2-113">Vous pouvez ajouter des utilisateurs dans le centre d'administration 365 de Microsoft, mais ces utilisateurs ne peuvent pas être utilisés comme destinataires de courrier.</span><span class="sxs-lookup"><span data-stu-id="207a2-113">You can add users in the Microsoft 365 admin center, however these users can't be used as mail recipients.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="207a2-114">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="207a2-114">Before you begin</span></span>

- <span data-ttu-id="207a2-p105">Les procédures décrites dans cette rubrique requièrent des autorisations spécifiques. Consultez chaque procédure pour savoir quelles autorisations sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="207a2-p105">Procedures in this topic require specific permissions. See each procedure for its permissions information.</span></span>
    
- <span data-ttu-id="207a2-117">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013**Raccourcis clavier dans le Centre d'administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="207a2-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="207a2-p106">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="207a2-p106">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="207a2-121">Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="207a2-121">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="207a2-122">Cette section fournit des informations sur la gestion des utilisateurs de messagerie électronique à l’aide de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="207a2-122">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="207a2-123">Si vous utilisez la synchronisation d'annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le centre d'administration 365 de Microsoft, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="207a2-123">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="207a2-124">En effet, la synchronisation d'annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage.</span><span class="sxs-lookup"><span data-stu-id="207a2-124">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="207a2-125">Il est recommandé d'utiliser la synchronisation d'annuaires avec les fonctionnalités suivantes: > **Outlook Safe sender and blocked sender lists** -lors de la synchronisation avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service.</span><span class="sxs-lookup"><span data-stu-id="207a2-125">Using directory synchronization is recommended for use with the following features: > **Outlook safe sender and blocked sender lists** - When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="207a2-126">Cela permet aux utilisateurs de gérer leurs propres listes d’expéditeurs autorisés et bloqués en fonction de l’utilisateur et du domaine.</span><span class="sxs-lookup"><span data-stu-id="207a2-126">This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis.</span></span><span data-ttu-id="207a2-127"> > *\*Blocage du périmètre basé sur l'annuaire (DBEB)** pour plus d'informations sur DBEB, voir [use Directory based Edge blockIng to Reject messages sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="207a2-127"> > *\*Directory Based Edge Blocking (DBEB)** - For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span><span data-ttu-id="207a2-128"> > *\*Mise en quarantaine du courrier** indésirable de l'utilisateur final: pour accéder à la mise en quarantaine du courrier indésirable de l'utilisateur final, les utilisateurs finaux doivent avoir un ID d'utilisateur et un mot de passe Office 365 valide.</span><span class="sxs-lookup"><span data-stu-id="207a2-128"> > *\*End user spam quarantine** - In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="207a2-129">Les clients qui utilisent EOP pour la protection des boîtes aux lettres locales doivent être des utilisateurs de messagerie électronique valides.</span><span class="sxs-lookup"><span data-stu-id="207a2-129">EOP customers protecting on-premises mailboxes must be valid email users.</span></span><span data-ttu-id="207a2-130"> > *\*Règles de flux de messagerie** : lorsque vous utilisez la synchronisation d'annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, puis vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) qui ciblent des utilisateurs spécifiques et/ou groupes sans avoir à les ajouter manuellement via le centre d'administration Exchange ou Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="207a2-130"> > *\*Mail flow rules** - When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="207a2-131">Notez que les [groupes de distribution dynamique](https://go.microsoft.com/fwlink/?LinkId=507569) ne peuvent pas être synchronisés via la synchronisation d'annuaires.</span><span class="sxs-lookup"><span data-stu-id="207a2-131">Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span> 
  
 <span data-ttu-id="207a2-132">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="207a2-132">**Before you begin**</span></span>
  
<span data-ttu-id="207a2-133">Obtenez les autorisations nécessaires et préparez la synchronisation d'annuaires, comme décrit dans la rubrique [Préparer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span><span class="sxs-lookup"><span data-stu-id="207a2-133">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories"></a><span data-ttu-id="207a2-134">Pour synchroniser les annuaires d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="207a2-134">To synchronize user directories</span></span>

1. <span data-ttu-id="207a2-135">Activez la synchronisation d'annuaires, comme décrit dans la rubrique [Activer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span><span class="sxs-lookup"><span data-stu-id="207a2-135">Activate directory synchronization, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>
    
2. <span data-ttu-id="207a2-136">Configurez votre ordinateur de synchronisation d'annuaires, comme décrit dans la rubrique [Configurer votre ordinateur de synchronisation d'annuaires](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span><span class="sxs-lookup"><span data-stu-id="207a2-136">Set up your directory synchronization computer, as described in [Set up your directory sync computer](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span></span>
    
3. <span data-ttu-id="207a2-137">Synchronisez vos annuaires, comme décrit dans la rubrique [Utiliser l'Assistant Configuration pour synchroniser vos annuaires](http://go.microsoft.com/fwlink/?LinkId=308912).</span><span class="sxs-lookup"><span data-stu-id="207a2-137">Synchronize your directories, as described in [Use the Configuration Wizard to sync your directories](http://go.microsoft.com/fwlink/?LinkId=308912).</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="207a2-p109">Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site.</span><span class="sxs-lookup"><span data-stu-id="207a2-p109">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span> 
  
4. <span data-ttu-id="207a2-141">Activez les utilisateurs synchronisés, comme décrit dans la rubrique [Activer les utilisateurs synchronisés](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span><span class="sxs-lookup"><span data-stu-id="207a2-141">Activate synced users, as described in [Activate synced users](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span></span>
    
5. <span data-ttu-id="207a2-142">Gérez la synchronisation d'annuaires, comme décrit dans la rubrique [Gérer la synchronisation d'annuaires](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span><span class="sxs-lookup"><span data-stu-id="207a2-142">Manage directory synchronization, as described in [Manage directory synchronization](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span></span>
    
6. <span data-ttu-id="207a2-p110">Vérifiez qu'EOP effectue la synchronisation correctement. Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="207a2-p110">Verify that EOP is synchronizing correctly. In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span> 
    
## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="207a2-145">Utilisation du CAE pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="207a2-145">Use the EAC to manage mail users</span></span>

<span data-ttu-id="207a2-146">Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="207a2-146">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
 <span data-ttu-id="207a2-147">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="207a2-147">**Before you begin**</span></span>
  
<span data-ttu-id="207a2-p111">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="207a2-p111">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
  
### <a name="to-add-a-mail-user-in-the-eac"></a><span data-ttu-id="207a2-150">Pour ajouter un utilisateur de messagerie dans le CAE</span><span class="sxs-lookup"><span data-stu-id="207a2-150">To add a mail user in the EAC</span></span>

1. <span data-ttu-id="207a2-151">Créez un utilisateur de messagerie électronique en accédant à **Destinataires** \> **Contacts** dans le CAE, puis cliquez sur **Nouveau +**.</span><span class="sxs-lookup"><span data-stu-id="207a2-151">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>
    
2. <span data-ttu-id="207a2-152">Sur la page **Nouvel utilisateur de messagerie**, saisissez les informations de l'utilisateur, notamment les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="207a2-152">On the **New mail user** page, enter the user's information, including the following:</span></span> 
    
   ****

|<span data-ttu-id="207a2-153">**Propriété d'utilisateur de messagerie**</span><span class="sxs-lookup"><span data-stu-id="207a2-153">**Mail user property**</span></span>|<span data-ttu-id="207a2-154">**Description**</span><span class="sxs-lookup"><span data-stu-id="207a2-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="207a2-155">**Prénom**, **Initiales** et **Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="207a2-155">**First name**, **Initials**, and **Last name**</span></span> <br/> |<span data-ttu-id="207a2-156">Dans les zones appropriées, saisissez le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207a2-156">Type the user's full name in the appropriate boxes.</span></span>  <br/> |
|<span data-ttu-id="207a2-157">**Nom complet**</span><span class="sxs-lookup"><span data-stu-id="207a2-157">**Display name**</span></span> <br/> |<span data-ttu-id="207a2-p112">Saisissez le nom (64 caractères maximum). Par défaut, cette zone est renseignée avec les noms que vous avez entrés dans les champs **Prénom**, **Initiales** et **Nom de famille**, le cas échéant. Le nom complet est requis.  </span><span class="sxs-lookup"><span data-stu-id="207a2-p112">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.  </span></span><br/> |
|<span data-ttu-id="207a2-161">**Alias**</span><span class="sxs-lookup"><span data-stu-id="207a2-161">**Alias**</span></span> <br/> |<span data-ttu-id="207a2-p113">Saisissez un alias unique pour l'utilisateur (64 caractères maximum). L'alias est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="207a2-p113">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>  <br/> |
|<span data-ttu-id="207a2-164">**Adresse de messagerie externe**</span><span class="sxs-lookup"><span data-stu-id="207a2-164">**External email address**</span></span> <br/> |<span data-ttu-id="207a2-165">Saisissez l'adresse de messagerie électronique externe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207a2-165">Type the external email address of the user.</span></span>  <br/> |
|<span data-ttu-id="207a2-166">**ID utilisateur**</span><span class="sxs-lookup"><span data-stu-id="207a2-166">**User id**</span></span> <br/> |<span data-ttu-id="207a2-p114">Saisissez le nom que l'utilisateur de messagerie utilisera pour se connecter au service. Le nom de connexion de l'utilisateur est constitué du nom d'utilisateur à gauche du symbole (@) et d'un suffixe à droite. Généralement, le suffixe est le nom du domaine dans lequel le compte d'utilisateur réside.</span><span class="sxs-lookup"><span data-stu-id="207a2-p114">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>  <br/> |
|<span data-ttu-id="207a2-170">**Nouveau mot de passe**</span><span class="sxs-lookup"><span data-stu-id="207a2-170">**New password**</span></span> <br/> |<span data-ttu-id="207a2-p115">Saisissez le mot de passe que l'utilisateur de messagerie utilisera pour se connecter au service. Assurez-vous que le mot de passe que vous saisissez est conforme aux exigences de longueur, de complexité et d'historique de mot de passe du domaine dans lequel vous créez le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207a2-p115">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>  <br/> |
|<span data-ttu-id="207a2-173">**Confirmer le mot de passe**</span><span class="sxs-lookup"><span data-stu-id="207a2-173">**Confirm password**</span></span> <br/> |<span data-ttu-id="207a2-174">Ressaisissez le mot de passe pour le confirmer.</span><span class="sxs-lookup"><span data-stu-id="207a2-174">Retype the password to confirm it.</span></span>  <br/> |
   
3. <span data-ttu-id="207a2-p116">Cliquez sur **Nouveau** pour créer l’utilisateur de messagerie. Le nouvel utilisateur doit apparaître dans la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="207a2-p116">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span> 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a><span data-ttu-id="207a2-177">Pour modifier ou supprimer un utilisateur de messagerie dans le CAE</span><span class="sxs-lookup"><span data-stu-id="207a2-177">To edit or remove a mail user in the EAC</span></span>

- <span data-ttu-id="207a2-178">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="207a2-178">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="207a2-179">Dans la liste des utilisateurs, cliquez sur l'utilisateur que vous souhaitez afficher ou modifier, puis sélectionnez **modifier** ![l'icône](../media/ITPro-EAC-EditIcon.gif) modifier pour mettre à jour les paramètres utilisateur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="207a2-179">In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed.</span></span> <span data-ttu-id="207a2-180">Vous pouvez modifier le nom, l'alias ou les coordonnées de l'utilisateur et vous pouvez enregistrer des informations détaillées sur le rôle de l'utilisateur dans l'organisation.</span><span class="sxs-lookup"><span data-stu-id="207a2-180">You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization.</span></span> <span data-ttu-id="207a2-181">Vous pouvez également sélectionner un utilisateur, puis cliquer sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif) pour le supprimer.</span><span class="sxs-lookup"><span data-stu-id="207a2-181">You can also select a user and then choose **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a><span data-ttu-id="207a2-182">Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="207a2-182">Use remote Windows PowerShell to manage mail users</span></span>

<span data-ttu-id="207a2-183">Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie à l’aide de Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="207a2-183">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
 <span data-ttu-id="207a2-184">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="207a2-184">**Before you begin**</span></span>
  
- <span data-ttu-id="207a2-p118">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="207a2-p118">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
    
- <span data-ttu-id="207a2-187">Gardez à l'esprit que lorsque vous créez des utilisateurs de messagerie à l'aide de cmdlets PowerShell à distance, vous pouvez être confronté à des limitations.</span><span class="sxs-lookup"><span data-stu-id="207a2-187">Be aware that when creating mail users by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="207a2-188">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="207a2-188">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="207a2-189">Pour découvrir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online Protection à l'aide d'une session PowerShell distante](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="207a2-189">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
 <span data-ttu-id="207a2-190">**Pour ajouter un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="207a2-190">**To add a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="207a2-191">Cet exemple illustre la création d'un compte d'utilisateur à extension messagerie avec la cmdlet [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) pour l'utilisateur Jeffrey Zeng, avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="207a2-191">This example uses the [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span> 
  
- <span data-ttu-id="207a2-192">Le prénom est Jeffrey et le nom est Zeng.</span><span class="sxs-lookup"><span data-stu-id="207a2-192">The first name is Jeffrey and the last name is Zeng.</span></span>
    
- <span data-ttu-id="207a2-193">Le nom est Jeffrey et le nom d'affichage est Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="207a2-193">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>
    
- <span data-ttu-id="207a2-194">L'alias est jeffreyz.</span><span class="sxs-lookup"><span data-stu-id="207a2-194">The alias is jeffreyz.</span></span>
    
- <span data-ttu-id="207a2-195">L'adresse de messagerie externe est jzeng@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="207a2-195">The external email address is jzeng@tailspintoys.com.</span></span>
    
- <span data-ttu-id="207a2-196">Le nom de connexion à Office 365 est jeffreyz@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="207a2-196">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>
    
- <span data-ttu-id="207a2-197">Le mot de passe est Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="207a2-197">The password is Pa$$word1.</span></span>
    
```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 <span data-ttu-id="207a2-198">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="207a2-198">**To verify that this worked**</span></span>
  
<span data-ttu-id="207a2-199">Exécutez la cmdlet [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) comme suit pour afficher les informations relatives au nouvel utilisateur de messagerie Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="207a2-199">Run the [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet as follows to display information about new mail user Jeffrey Zeng:</span></span> 
  
```Powershell
Get-User "Jeffrey Zeng"

```

 <span data-ttu-id="207a2-200">**Pour modifier les propriétés d'un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="207a2-200">**To edit the properties of a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="207a2-201">Utilisez les cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) et [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) pour afficher et modifier les propriétés des utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="207a2-201">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlets to view or change properties for mail users.</span></span> 
  
<span data-ttu-id="207a2-202">Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="207a2-202">This example sets the external email address for Pilar Pinilla.</span></span>
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="207a2-203">Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="207a2-203">This example sets the Company property for all mail users to Contoso.</span></span>
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 <span data-ttu-id="207a2-204">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="207a2-204">**To verify that this worked**</span></span>
  
<span data-ttu-id="207a2-p119">Dans l'exemple précédent où nous avons modifié les propriétés de l'utilisateur de messagerie nommé Pilar Pinilla, utilisez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour vérifier les modifications. (Vous pouvez afficher plusieurs propriétés pour plusieurs contacts de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="207a2-p119">In the previous example where we changed the properties for mail user Pilar Pinella, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. (Note that you can view multiple properties for multiple mail contacts.)</span></span> 
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

<span data-ttu-id="207a2-207">Dans l'exemple précédent où la propriété Company a été définie sur Contoso pour tous les utilisateurs de messagerie, exécutez la commande suivante pour vérifier les modifications :</span><span class="sxs-lookup"><span data-stu-id="207a2-207">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="207a2-208">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="207a2-208">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span> 
  
 <span data-ttu-id="207a2-209">**Pour supprimer un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="207a2-209">**To remove a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="207a2-210">Cet exemple utilise la cmdlet [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) pour supprimer l'utilisateur Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="207a2-210">This example uses the [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet to delete user Jeffrey Zeng:</span></span> 
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="207a2-211">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="207a2-211">**To verify that this worked**</span></span>
  
<span data-ttu-id="207a2-p120">Exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit. Vous devriez obtenir un message d'erreur car l'utilisateur n'existe plus.</span><span class="sxs-lookup"><span data-stu-id="207a2-p120">Run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows. You should get an error message since the user no longer exists.</span></span> 
  
```Powershell
Get-Recipient Jeffrey | fl
```


