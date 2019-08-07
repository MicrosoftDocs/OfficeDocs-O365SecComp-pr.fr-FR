---
title: Gestion d'un site d'équipe SharePoint Online isolé
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: "Résumé : Découvrez comment gérer votre site d'équipe SharePoint Online isolé."
ms.openlocfilehash: e6ed86421ec199ce785e2daff5e9c5447939e69b
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36053079"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="687ef-103">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="687ef-103">Manage an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="687ef-104">**Résumé :** Découvrez comment gérer votre site d'équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="687ef-104">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>
  
<span data-ttu-id="687ef-105">Cet article vous explique comment gérer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="687ef-105">This article describes common management operations for an isolated SharePoint Online team site.</span></span>
  
## <a name="add-a-new-user"></a><span data-ttu-id="687ef-106">Ajouter un nouvel utilisateur</span><span class="sxs-lookup"><span data-stu-id="687ef-106">Add a new user</span></span>

<span data-ttu-id="687ef-107">Lorsqu’un nouvel utilisateur rejoint le site, vous devez choisir son niveau de participation :</span><span class="sxs-lookup"><span data-stu-id="687ef-107">When someone new joins the site, you must decide their level of participation in the site:</span></span>
  
- <span data-ttu-id="687ef-108">Administration : ajoutez le compte du nouvel utilisateur au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-108">Administration: Add the new user account to the site admins access group</span></span>
    
- <span data-ttu-id="687ef-109">Collaboration active : ajoutez le compte de l'utilisateur au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="687ef-109">Active collaboration: Add the user account to the site members access group</span></span>
    
- <span data-ttu-id="687ef-110">Consultation : ajoutez le compte de l'utilisateur au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-110">Viewing: Add the user account to the site viewers access group</span></span>
    
<span data-ttu-id="687ef-111">Si vous gérez des comptes d’utilisateur et des groupes par le biais des services de domaine Active Directory (AD DS), ajoutez les utilisateurs appropriés aux groupes d’accès appropriés en utilisant vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.</span><span class="sxs-lookup"><span data-stu-id="687ef-111">If you are managing user accounts and groups through Active Directory Domain Services (AD DS), add the appropriate users to the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="687ef-112">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou Microsoft PowerShell:</span><span class="sxs-lookup"><span data-stu-id="687ef-112">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or Microsoft PowerShell:</span></span>
  
- <span data-ttu-id="687ef-113">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les utilisateurs appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="687ef-113">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>
    
- <span data-ttu-id="687ef-114">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="687ef-114">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span> <span data-ttu-id="687ef-115">Pour ajouter un compte d'utilisateur à un groupe d'accès en utilisant son nom d'utilisateur principal (UPN), exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="687ef-115">To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="687ef-116">Pour un fichier texte qui contient toutes les commandes PowerShell et une feuille de calcul de configuration Excel qui génère des commandes PowerShell en fonction des noms de compte de vos utilisateurs et groupes, téléchargez le [kit de déploiement du site d'équipe SharePoint Online isolé](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span><span class="sxs-lookup"><span data-stu-id="687ef-116">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 

<span data-ttu-id="687ef-117">Pour ajouter un compte d’utilisateur à un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="687ef-117">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="687ef-118">Ajouter un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="687ef-118">Add a new group</span></span>

<span data-ttu-id="687ef-119">Pour ajouter un accès à un groupe, vous devez choisir le niveau de participation de tous les membres du groupe sur le site :</span><span class="sxs-lookup"><span data-stu-id="687ef-119">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>
  
- <span data-ttu-id="687ef-120">Administration : ajoutez le groupe d'utilisateurs au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-120">Administration: Add the group to the site admins access group</span></span>
    
- <span data-ttu-id="687ef-121">Collaboration active : ajoutez le groupe d'utilisateurs au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="687ef-121">Active collaboration: Add the group to the site members access group</span></span>
    
- <span data-ttu-id="687ef-122">Consultation : ajoutez le groupe d'utilisateurs au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-122">Viewing: Add the group to the site viewers access group</span></span>
    
<span data-ttu-id="687ef-123">Si vous gérez des comptes d’utilisateur et des groupes via AD DS, ajoutez les groupes appropriés aux groupes appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="687ef-123">If you are managing user accounts and groups through AD DS, add the appropriate groups to the appropriate groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="687ef-124">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:</span><span class="sxs-lookup"><span data-stu-id="687ef-124">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="687ef-125">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les groupes appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="687ef-125">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>
    
- <span data-ttu-id="687ef-126">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="687ef-126">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
 <span data-ttu-id="687ef-127">Ensuite, utilisez les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="687ef-127">Then, use the following PowerShell commands:</span></span>
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="687ef-128">Supprimer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="687ef-128">Remove a user</span></span>

<span data-ttu-id="687ef-129">Lorsque l'accès d'un utilisateur doit être supprimé du site, supprimez-le du groupe d'accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="687ef-129">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="687ef-130">Administration : supprimez le compte d'utilisateur du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-130">Administration: Remove the user account from the site admins access group</span></span>
    
- <span data-ttu-id="687ef-131">Collaboration active : supprimez le compte d'utilisateur du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="687ef-131">Active collaboration: Remove the user account from the site members access group</span></span>
    
- <span data-ttu-id="687ef-132">Consultation : supprimez le compte d'utilisateur du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-132">Viewing: Remove the user account from the site viewers access group</span></span>
    
<span data-ttu-id="687ef-133">Si vous gérez des comptes d’utilisateur et des groupes via AD DS, supprimez les utilisateurs appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="687ef-133">If you are managing user accounts and groups through AD DS, remove the appropriate users from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="687ef-134">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:</span><span class="sxs-lookup"><span data-stu-id="687ef-134">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="687ef-135">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les utilisateurs appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="687ef-135">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>
    
- <span data-ttu-id="687ef-136">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="687ef-136">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
<span data-ttu-id="687ef-137">Pour supprimer un compte d'utilisateur d'un groupe d'accès en utilisant son UPN, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="687ef-137">To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="687ef-138">Pour supprimer un compte d’utilisateur d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="687ef-138">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="687ef-139">Supprimer un groupe</span><span class="sxs-lookup"><span data-stu-id="687ef-139">Remove a group</span></span>

<span data-ttu-id="687ef-140">Pour supprimer l’accès d’un groupe, supprimez le groupe du groupe d’accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="687ef-140">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="687ef-141">Administration : supprimez le groupe du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-141">Administration: Remove the group from the site admins access group</span></span>
    
- <span data-ttu-id="687ef-142">Collaboration active : supprimez le groupe du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="687ef-142">Active collaboration: Remove the group from the site members access group</span></span>
    
- <span data-ttu-id="687ef-143">Consultation : supprimez le groupe du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="687ef-143">Viewing: Remove the group from the site viewers access group</span></span>
    
<span data-ttu-id="687ef-144">Si vous gérez des comptes d’utilisateur et des groupes par le biais de Windows Server Active Directory, supprimez les groupes appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.</span><span class="sxs-lookup"><span data-stu-id="687ef-144">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="687ef-145">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:</span><span class="sxs-lookup"><span data-stu-id="687ef-145">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="687ef-146">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les groupes appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="687ef-146">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>
    
- <span data-ttu-id="687ef-147">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="687ef-147">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>    
<span data-ttu-id="687ef-148">Pour supprimer un groupe d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="687ef-148">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="687ef-149">Création d’un sous-dossier de documents avec des autorisations personnalisées</span><span class="sxs-lookup"><span data-stu-id="687ef-149">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="687ef-p104">Il arrive que des utilisateurs travaillant dans un site isolé aient besoin d'un espace privé pour travailler en équipe. Pour les sites SharePoint Online, vous pouvez créer un sous-dossier dans le dossier Documents du site et affecter des autorisations personnalisées. Les personnes non autorisées ne verront pas ce sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="687ef-p104">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>
  
<span data-ttu-id="687ef-153">Pour créer un sous-dossier de documents avec des autorisations personnalisées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="687ef-153">To create a documents subfolder with custom permissions, do the following:</span></span>
  
1. <span data-ttu-id="687ef-p105">Connectez-vous à Office 365 avec un compte membre du groupe d'accès Administrateurs du site. Pour plus d'informations, consultez la rubrique [Se connecter à Office 365 pour les entreprises](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="687ef-p105">Sign in to Office 365 with an account that is a member of the admins access group for the site. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="687ef-156">Accédez au site d'équipe isolé, puis cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="687ef-156">Go to the isolated team site and click **Documents**.</span></span>
    
3. <span data-ttu-id="687ef-157">Accédez au dossier dans le dossier de documents qui contiendra le sous-dossier bénéficiant d’autorisations personnalisées, créez le dossier, puis ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="687ef-157">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>
    
4. <span data-ttu-id="687ef-158">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="687ef-158">Click **Share**.</span></span>
    
5. <span data-ttu-id="687ef-159">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="687ef-159">Click **Shared with > Advanced**.</span></span>
    
6. <span data-ttu-id="687ef-160">Cliquez sur **Arrêter l'héritage des autorisations**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="687ef-160">Click **Stop inheriting permissions**, and then click **OK**.</span></span>
    
7. <span data-ttu-id="687ef-161">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="687ef-161">Click **Share**.</span></span>
    
8. <span data-ttu-id="687ef-162">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="687ef-162">Click **Shared with > Advanced**.</span></span>
    
9. <span data-ttu-id="687ef-163">Cliquez sur **Accorder des autorisations > Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="687ef-163">Click **Grant Permissions > Shared with > Advanced**.</span></span>
    
10. <span data-ttu-id="687ef-164">Sur la page Autorisations, cliquez sur Membres de **\<nom du site> dans la liste**.</span><span class="sxs-lookup"><span data-stu-id="687ef-164">On the permissions page, click **\<site name> Members in the list**.</span></span>
    
11. <span data-ttu-id="687ef-165">Sur la page Membres de **\<nom du site>**, cochez la case en regard du groupe d’accès Membres du site, cliquez sur **Actions**, sur **Supprimer des utilisateurs du groupe**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="687ef-165">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>
    
12. <span data-ttu-id="687ef-166">Pour ajouter des membres à ce sous-dossier, cliquez sur **Nouveau > Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="687ef-166">To add specific members to this subfolder, click **New > Add users**.</span></span>
    
13. <span data-ttu-id="687ef-167">Dans la boîte de dialogue **Partager**, saisissez les noms des comptes d'utilisateur qui peuvent collaborer sur des fichiers du sous-dossier, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="687ef-167">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>
    
14. <span data-ttu-id="687ef-168">Actualisez la page web pour afficher les nouveaux résultats.</span><span class="sxs-lookup"><span data-stu-id="687ef-168">Refresh the web page to see the new results.</span></span>
    
15. <span data-ttu-id="687ef-169">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Visiteurs de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent afficher les fichiers du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="687ef-169">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>
    
16. <span data-ttu-id="687ef-170">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Propriétaires de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent gérer les autorisations du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="687ef-170">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>
    
17. <span data-ttu-id="687ef-171">Fermez l’onglet **Utilisateurs et groupes** dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="687ef-171">Close the **People and Groups** tab in your browser.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="687ef-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="687ef-172">See Also</span></span>

[<span data-ttu-id="687ef-173">Sites d’équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="687ef-173">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="687ef-174">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="687ef-174">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="687ef-175">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="687ef-175">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



