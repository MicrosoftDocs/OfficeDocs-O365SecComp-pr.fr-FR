---
title: Gestion des utilisateurs de messagerie dans EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP).
ms.openlocfilehash: 69ed6460966a399ac5b1e3cf71bd985917bec82c
ms.sourcegitcommit: f57d411e06c955d648dfa1a2a473aa45416e1377
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2019
ms.locfileid: "36620488"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="71ce2-103">Gestion des utilisateurs de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="71ce2-103">Manage mail users in EOP</span></span>

<span data-ttu-id="71ce2-p101">La définition des utilisateurs de messagerie constitue une partie importante de la gestion du service Exchange Online Protection (EOP). Vous pouvez gérer les utilisateurs de différentes manières dans EOP.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="71ce2-106">Utilisation de la synchronisation d'annuaires pour gérer les utilisateurs de messagerie : si votre entreprise dispose de comptes d'utilisateur dans un environnement Active Directory local, vous pouvez synchroniser ces comptes sur Azure Active Directory (AD), où des copies des comptes sont stockées dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="71ce2-106">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud.</span></span> <span data-ttu-id="71ce2-107">Lorsque vous synchronisez vos comptes d'utilisateur sur Azure Active Directory, vous pouvez consulter ces utilisateurs dans le volet **Destinataires** du Centre d'administration Exchange (CAE).</span><span class="sxs-lookup"><span data-stu-id="71ce2-107">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC).</span></span> <span data-ttu-id="71ce2-108">L'utilisation de la synchronisation d'annuaires est recommandée.</span><span class="sxs-lookup"><span data-stu-id="71ce2-108">Using directory synchronization is recommended.</span></span> 
    
- <span data-ttu-id="71ce2-109">Utilisation du CAE pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="71ce2-109">Use the EAC to manage mail users: Add and manage mail users directly in the EAC.</span></span> <span data-ttu-id="71ce2-110">Il s'agit du moyen le plus facile pour ajouter des utilisateurs de messagerie et cette méthode est également utile pour ajouter un utilisateur à la fois.</span><span class="sxs-lookup"><span data-stu-id="71ce2-110">This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>
    
- <span data-ttu-id="71ce2-111">Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie : ajoutez et gérez les utilisateurs de messagerie en exécutant Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="71ce2-111">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell.</span></span> <span data-ttu-id="71ce2-112">Cette méthode est utile pour ajouter plusieurs enregistrements et pour la création de scripts.</span><span class="sxs-lookup"><span data-stu-id="71ce2-112">This method is useful for adding multiple records and creating scripts.</span></span>
    
> [!NOTE]
> <span data-ttu-id="71ce2-113">Vous pouvez ajouter des utilisateurs dans le centre d’administration 365 de Microsoft, mais ces utilisateurs ne peuvent pas être utilisés comme destinataires de courrier.</span><span class="sxs-lookup"><span data-stu-id="71ce2-113">You can add users in the Microsoft 365 admin center, however these users can't be used as mail recipients.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="71ce2-114">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="71ce2-114">Before you begin</span></span>

- <span data-ttu-id="71ce2-p105">Les procédures décrites dans cette rubrique requièrent des autorisations spécifiques. Consultez chaque procédure pour savoir quelles autorisations sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p105">Procedures in this topic require specific permissions. See each procedure for its permissions information.</span></span>
    
- <span data-ttu-id="71ce2-117">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013**Raccourcis clavier dans le Centre d'administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="71ce2-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="71ce2-p106">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="71ce2-p106">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="71ce2-121">Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="71ce2-121">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="71ce2-122">Cette section fournit des informations sur la gestion des utilisateurs de messagerie électronique à l’aide de la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="71ce2-122">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="71ce2-123">Si vous utilisez la synchronisation d’annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le centre d’administration 365 de Microsoft, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="71ce2-123">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="71ce2-124">En effet, la synchronisation d'annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage.</span><span class="sxs-lookup"><span data-stu-id="71ce2-124">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="71ce2-125">Il est recommandé d’utiliser la synchronisation d’annuaires avec les fonctionnalités suivantes: > **Outlook Safe sender and blocked sender lists** -lors de la synchronisation avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service.</span><span class="sxs-lookup"><span data-stu-id="71ce2-125">Using directory synchronization is recommended for use with the following features: > **Outlook safe sender and blocked sender lists** - When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="71ce2-126">Cela permet aux utilisateurs de gérer leurs propres listes d’expéditeurs autorisés et bloqués en fonction de l’utilisateur et du domaine.</span><span class="sxs-lookup"><span data-stu-id="71ce2-126">This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis.</span></span><span data-ttu-id="71ce2-127"> > **Blocage du périmètre basé sur l’annuaire (DBEB)** pour plus d’informations sur DBEB, voir [use Directory based Edge Blocking to Reject messages sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="71ce2-127"> > **Directory Based Edge Blocking (DBEB)** - For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span><span data-ttu-id="71ce2-128"> > **Mise en quarantaine du courrier** indésirable de l’utilisateur final: pour accéder à la mise en quarantaine du courrier indésirable de l’utilisateur final, les utilisateurs finaux doivent avoir un ID d’utilisateur et un mot de passe Office 365 valide.</span><span class="sxs-lookup"><span data-stu-id="71ce2-128"> > **End user spam quarantine** - In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password.</span></span> <span data-ttu-id="71ce2-129">Les clients qui utilisent EOP pour la protection des boîtes aux lettres locales doivent être des utilisateurs de messagerie électronique valides.</span><span class="sxs-lookup"><span data-stu-id="71ce2-129">EOP customers protecting on-premises mailboxes must be valid email users.</span></span><span data-ttu-id="71ce2-130"> > **Règles de flux de messagerie** : lorsque vous utilisez la synchronisation d’annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, puis vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) qui ciblent des utilisateurs spécifiques et/ou groupes sans avoir à les ajouter manuellement via le centre d’administration Exchange ou Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71ce2-130"> > **Mail flow rules** - When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="71ce2-131">Notez que les [groupes de distribution dynamique](https://go.microsoft.com/fwlink/?LinkId=507569) ne peuvent pas être synchronisés via la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="71ce2-131">Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span> 
  
 <span data-ttu-id="71ce2-132">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="71ce2-132">**Before you begin**</span></span>
  
<span data-ttu-id="71ce2-133">Obtenez les autorisations nécessaires et préparez la synchronisation d'annuaires, comme décrit dans la rubrique [Préparer la synchronisation d'annuaires](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span><span class="sxs-lookup"><span data-stu-id="71ce2-133">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories-with-azure-active-directory-connect-aad-connect"></a><span data-ttu-id="71ce2-134">Pour synchroniser les annuaires d’utilisateurs avec Azure Active Directory Connect (AAD Connect)</span><span class="sxs-lookup"><span data-stu-id="71ce2-134">To synchronize user directories with Azure Active Directory Connect (AAD Connect)</span></span>

<span data-ttu-id="71ce2-135">Pour synchroniser les utilisateurs avec Azure Active Directory (AAD), vous devez d’abord **activer la synchronisation**d’annuaires, comme décrit dans la rubrique activation de la [synchronisation](https://go.microsoft.com/fwlink/p/?LinkId=308909)d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="71ce2-135">To synchronize users to Azure Active Directory (AAD) you first have to **activate directory synchronization**, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>

<span data-ttu-id="71ce2-136">Ensuite, l’installation et la configuration d’un ordinateur local pour exécuter AAD Connect (si vous n’avez pas encore besoin de vérifier à l’avance).</span><span class="sxs-lookup"><span data-stu-id="71ce2-136">Next is the installation and configuration of an on-premises computer to run AAD Connect (if you don't already have one -- something worth checking ahead of time).</span></span> <span data-ttu-id="71ce2-137">L’article ci-dessous indique comment configurer et synchroniser vos comptes sur site vers Azure AD avec AAD Connect.</span><span class="sxs-lookup"><span data-stu-id="71ce2-137">The article below tells you how to setup and synchronize your accounts from on-premises to Azure AD with AAD Connect.</span></span>

[<span data-ttu-id="71ce2-138">La configuration d’AAD Connect, la méthode rapide.</span><span class="sxs-lookup"><span data-stu-id="71ce2-138">Setting up AAD Connect, the express way.</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-express)

<span data-ttu-id="71ce2-139">Avant d’effectuer cette opération, assurez-vous que [vous remplissez les conditions préalables] (https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-prerequisiteset [Choisissez votre type d’installation](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-select-installation).</span><span class="sxs-lookup"><span data-stu-id="71ce2-139">But before you do that work, make certain [you meet prerequisites](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-prerequisites, and [choose your installation type](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-select-installation).</span></span> <span data-ttu-id="71ce2-140">Le lien publié ci-dessus est un petit article pour les installations rapides.</span><span class="sxs-lookup"><span data-stu-id="71ce2-140">The link posted above is to a short article for express installs.</span></span> <span data-ttu-id="71ce2-141">Vous pouvez également trouver des articles sur les [installations personnalisées](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom)ou [l’authentification directe](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-quick-start) si elles sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="71ce2-141">You can also find articles on [custom installations](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom), or [pass-through authentication](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-quick-start) if they're needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71ce2-142">Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71ce2-142">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest.</span></span> <span data-ttu-id="71ce2-143">Ce compte permet de lire et de synchroniser vos informations Active Directory sur site.</span><span class="sxs-lookup"><span data-stu-id="71ce2-143">This account is used to read and synchronize your on-premises Active Directory information.</span></span> <span data-ttu-id="71ce2-144">Pour que la synchronisation d’annuaires fonctionne correctement, assurez-vous que le protocole TCP 443 sur votre serveur de synchronisation d’annuaires local est ouvert.</span><span class="sxs-lookup"><span data-stu-id="71ce2-144">In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open</span></span> 

<span data-ttu-id="71ce2-145">Après avoir configuré votre synchronisation, assurez-vous de vérifier que EOP effectue une synchronisation correcte.</span><span class="sxs-lookup"><span data-stu-id="71ce2-145">After configuring your sync, be sure to verify that EOP is synchronizing correctly.</span></span> <span data-ttu-id="71ce2-146">Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="71ce2-146">In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span>
    
## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="71ce2-147">Utilisation du CAE pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="71ce2-147">Use the EAC to manage mail users</span></span>

<span data-ttu-id="71ce2-148">Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="71ce2-148">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
 <span data-ttu-id="71ce2-149">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="71ce2-149">**Before you begin**</span></span>
  
<span data-ttu-id="71ce2-p113">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="71ce2-p113">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
  
### <a name="to-add-a-mail-user-in-the-eac"></a><span data-ttu-id="71ce2-152">Pour ajouter un utilisateur de messagerie dans le CAE</span><span class="sxs-lookup"><span data-stu-id="71ce2-152">To add a mail user in the EAC</span></span>

1. <span data-ttu-id="71ce2-153">Créez un utilisateur de messagerie électronique en accédant à **Destinataires** \> **Contacts** dans le CAE, puis cliquez sur **Nouveau +**.</span><span class="sxs-lookup"><span data-stu-id="71ce2-153">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>
    
2. <span data-ttu-id="71ce2-154">Sur la page **Nouvel utilisateur de messagerie**, saisissez les informations de l'utilisateur, notamment les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="71ce2-154">On the **New mail user** page, enter the user's information, including the following:</span></span> 
    
   ****

|<span data-ttu-id="71ce2-155">**Propriété d'utilisateur de messagerie**</span><span class="sxs-lookup"><span data-stu-id="71ce2-155">**Mail user property**</span></span>|<span data-ttu-id="71ce2-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="71ce2-156">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71ce2-157">**Prénom**, **Initiales** et **Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="71ce2-157">**First name**, **Initials**, and **Last name**</span></span> <br/> |<span data-ttu-id="71ce2-158">Dans les zones appropriées, saisissez le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71ce2-158">Type the user's full name in the appropriate boxes.</span></span>  <br/> |
|<span data-ttu-id="71ce2-159">**Nom complet**</span><span class="sxs-lookup"><span data-stu-id="71ce2-159">**Display name**</span></span> <br/> |<span data-ttu-id="71ce2-p114">Saisissez le nom (64 caractères maximum). Par défaut, cette zone est renseignée avec les noms que vous avez entrés dans les champs **Prénom**, **Initiales** et **Nom de famille**, le cas échéant. Le nom complet est requis.  </span><span class="sxs-lookup"><span data-stu-id="71ce2-p114">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.  </span></span><br/> |
|<span data-ttu-id="71ce2-163">**Alias**</span><span class="sxs-lookup"><span data-stu-id="71ce2-163">**Alias**</span></span> <br/> |<span data-ttu-id="71ce2-p115">Saisissez un alias unique pour l'utilisateur (64 caractères maximum). L'alias est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p115">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>  <br/> |
|<span data-ttu-id="71ce2-166">**Adresse de messagerie externe**</span><span class="sxs-lookup"><span data-stu-id="71ce2-166">**External email address**</span></span> <br/> |<span data-ttu-id="71ce2-167">Saisissez l'adresse de messagerie électronique externe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71ce2-167">Type the external email address of the user.</span></span>  <br/> |
|<span data-ttu-id="71ce2-168">**ID utilisateur**</span><span class="sxs-lookup"><span data-stu-id="71ce2-168">**User id**</span></span> <br/> |<span data-ttu-id="71ce2-p116">Saisissez le nom que l'utilisateur de messagerie utilisera pour se connecter au service. Le nom de connexion de l'utilisateur est constitué du nom d'utilisateur à gauche du symbole (@) et d'un suffixe à droite. Généralement, le suffixe est le nom du domaine dans lequel le compte d'utilisateur réside.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p116">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>  <br/> |
|<span data-ttu-id="71ce2-172">**Nouveau mot de passe**</span><span class="sxs-lookup"><span data-stu-id="71ce2-172">**New password**</span></span> <br/> |<span data-ttu-id="71ce2-p117">Saisissez le mot de passe que l'utilisateur de messagerie utilisera pour se connecter au service. Assurez-vous que le mot de passe que vous saisissez est conforme aux exigences de longueur, de complexité et d'historique de mot de passe du domaine dans lequel vous créez le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p117">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>  <br/> |
|<span data-ttu-id="71ce2-175">**Confirmer le mot de passe**</span><span class="sxs-lookup"><span data-stu-id="71ce2-175">**Confirm password**</span></span> <br/> |<span data-ttu-id="71ce2-176">Ressaisissez le mot de passe pour le confirmer.</span><span class="sxs-lookup"><span data-stu-id="71ce2-176">Retype the password to confirm it.</span></span>  <br/> |
   
3. <span data-ttu-id="71ce2-p118">Cliquez sur **Nouveau** pour créer l’utilisateur de messagerie. Le nouvel utilisateur doit apparaître dans la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p118">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span> 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a><span data-ttu-id="71ce2-179">Pour modifier ou supprimer un utilisateur de messagerie dans le CAE</span><span class="sxs-lookup"><span data-stu-id="71ce2-179">To edit or remove a mail user in the EAC</span></span>

- <span data-ttu-id="71ce2-180">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="71ce2-180">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="71ce2-181">Dans la liste des utilisateurs, cliquez sur l’utilisateur que vous souhaitez afficher ou modifier, puis sélectionnez **modifier** ![l’icône](../media/ITPro-EAC-EditIcon.gif) modifier pour mettre à jour les paramètres utilisateur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="71ce2-181">In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed.</span></span> <span data-ttu-id="71ce2-182">Vous pouvez modifier le nom, l'alias ou les coordonnées de l'utilisateur et vous pouvez enregistrer des informations détaillées sur le rôle de l'utilisateur dans l'organisation.</span><span class="sxs-lookup"><span data-stu-id="71ce2-182">You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization.</span></span> <span data-ttu-id="71ce2-183">Vous pouvez également sélectionner un utilisateur, puis cliquer sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif) pour le supprimer.</span><span class="sxs-lookup"><span data-stu-id="71ce2-183">You can also select a user and then choose **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a><span data-ttu-id="71ce2-184">Utiliser Windows PowerShell à distance pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="71ce2-184">Use remote Windows PowerShell to manage mail users</span></span>

<span data-ttu-id="71ce2-185">Cette section fournit des informations sur l’ajout et la gestion des utilisateurs de messagerie à l’aide de Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="71ce2-185">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
 <span data-ttu-id="71ce2-186">**Avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="71ce2-186">**Before you begin**</span></span>
  
- <span data-ttu-id="71ce2-p120">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="71ce2-p120">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
    
- <span data-ttu-id="71ce2-189">Gardez à l'esprit que lorsque vous créez des utilisateurs de messagerie à l'aide de cmdlets PowerShell à distance, vous pouvez être confronté à des limitations.</span><span class="sxs-lookup"><span data-stu-id="71ce2-189">Be aware that when creating mail users by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="71ce2-190">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="71ce2-190">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="71ce2-191">Pour découvrir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online Protection à l'aide d'une session PowerShell distante](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="71ce2-191">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
 <span data-ttu-id="71ce2-192">**Pour ajouter un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="71ce2-192">**To add a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="71ce2-193">Cet exemple illustre la création d'un compte d'utilisateur à extension messagerie avec la cmdlet [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) pour l'utilisateur Jeffrey Zeng, avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="71ce2-193">This example uses the [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span> 
  
- <span data-ttu-id="71ce2-194">Le prénom est Jeffrey et le nom est Zeng.</span><span class="sxs-lookup"><span data-stu-id="71ce2-194">The first name is Jeffrey and the last name is Zeng.</span></span>
    
- <span data-ttu-id="71ce2-195">Le nom est Jeffrey et le nom d'affichage est Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="71ce2-195">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>
    
- <span data-ttu-id="71ce2-196">L'alias est jeffreyz.</span><span class="sxs-lookup"><span data-stu-id="71ce2-196">The alias is jeffreyz.</span></span>
    
- <span data-ttu-id="71ce2-197">L'adresse de messagerie externe est jzeng@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="71ce2-197">The external email address is jzeng@tailspintoys.com.</span></span>
    
- <span data-ttu-id="71ce2-198">Le nom de connexion à Office 365 est jeffreyz@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="71ce2-198">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>
    
- <span data-ttu-id="71ce2-199">Le mot de passe est Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="71ce2-199">The password is Pa$$word1.</span></span>
    
```Powershell
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 <span data-ttu-id="71ce2-200">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="71ce2-200">**To verify that this worked**</span></span>
  
<span data-ttu-id="71ce2-201">Exécutez la cmdlet [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) comme suit pour afficher les informations relatives au nouvel utilisateur de messagerie Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="71ce2-201">Run the [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet as follows to display information about new mail user Jeffrey Zeng:</span></span> 
  
```Powershell
Get-User "Jeffrey Zeng"

```

 <span data-ttu-id="71ce2-202">**Pour modifier les propriétés d'un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="71ce2-202">**To edit the properties of a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="71ce2-203">Utilisez les cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) et [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) pour afficher et modifier les propriétés des utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="71ce2-203">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlets to view or change properties for mail users.</span></span> 
  
<span data-ttu-id="71ce2-204">Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="71ce2-204">This example sets the external email address for Pilar Pinilla.</span></span>
  
```Powershell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="71ce2-205">Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="71ce2-205">This example sets the Company property for all mail users to Contoso.</span></span>
  
```Powershell
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 <span data-ttu-id="71ce2-206">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="71ce2-206">**To verify that this worked**</span></span>
  
<span data-ttu-id="71ce2-p121">Dans l'exemple précédent où nous avons modifié les propriétés de l'utilisateur de messagerie nommé Pilar Pinilla, utilisez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour vérifier les modifications. (Vous pouvez afficher plusieurs propriétés pour plusieurs contacts de messagerie.)</span><span class="sxs-lookup"><span data-stu-id="71ce2-p121">In the previous example where we changed the properties for mail user Pilar Pinella, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. (Note that you can view multiple properties for multiple mail contacts.)</span></span> 
  
```Powershell
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

<span data-ttu-id="71ce2-209">Dans l'exemple précédent où la propriété Company a été définie sur Contoso pour tous les utilisateurs de messagerie, exécutez la commande suivante pour vérifier les modifications :</span><span class="sxs-lookup"><span data-stu-id="71ce2-209">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```Powershell
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="71ce2-210">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="71ce2-210">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span> 
  
 <span data-ttu-id="71ce2-211">**Pour supprimer un utilisateur de messagerie à l'aide de PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="71ce2-211">**To remove a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="71ce2-212">Cet exemple utilise la cmdlet [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) pour supprimer l'utilisateur Jeffrey Zeng :</span><span class="sxs-lookup"><span data-stu-id="71ce2-212">This example uses the [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet to delete user Jeffrey Zeng:</span></span> 
  
```Powershell
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="71ce2-213">**Pour vérifier que cela a fonctionné**</span><span class="sxs-lookup"><span data-stu-id="71ce2-213">**To verify that this worked**</span></span>
  
<span data-ttu-id="71ce2-p122">Exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit. Vous devriez obtenir un message d'erreur car l'utilisateur n'existe plus.</span><span class="sxs-lookup"><span data-stu-id="71ce2-p122">Run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows. You should get an error message since the user no longer exists.</span></span> 
  
```Powershell
Get-Recipient Jeffrey | fl
```


