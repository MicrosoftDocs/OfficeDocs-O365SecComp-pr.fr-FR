---
title: Conception d’un site d’équipe SharePoint Online isolé
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Résumé : Découvrez comment concevoir des sites d’équipe SharePoint Online.'
ms.openlocfilehash: 09748fcc22a4a48efc4346ff75a225db612a0ef4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257164"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="1c761-103">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1c761-103">Design an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="1c761-104">**Résumé :** Découvrez comment concevoir des sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1c761-104">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="1c761-105">Cet article vous aide à faire les bons choix de conception avant de créer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="1c761-105">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="1c761-106">Phase 1 : choix des groupes SharePoint et des niveaux d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1c761-106">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="1c761-107">Chaque site d’équipe SharePoint Online par défaut est créé avec les groupes SharePoint suivants :</span><span class="sxs-lookup"><span data-stu-id="1c761-107">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>
  
- <span data-ttu-id="1c761-108">\<Membres du name> de site</span><span class="sxs-lookup"><span data-stu-id="1c761-108">\<site name> Members</span></span>
    
- <span data-ttu-id="1c761-109">\<Visiteurs du site name></span><span class="sxs-lookup"><span data-stu-id="1c761-109">\<site name> Visitors</span></span>
    
- <span data-ttu-id="1c761-110">\<Propriétaires de sites name></span><span class="sxs-lookup"><span data-stu-id="1c761-110">\<site name> Owners</span></span>
    
<span data-ttu-id="1c761-111">Ces groupes sont différents des groupes Office 365 et Azure Active Directory (AD), et permettent d’attribuer des autorisations pour l’utilisation des ressources du site.</span><span class="sxs-lookup"><span data-stu-id="1c761-111">These groups are separate from Office 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>
  
<span data-ttu-id="1c761-p101">L’ensemble des autorisations qui déterminent ce que le membre d’un groupe SharePoint peut faire dans un site est un niveau d’autorisation. Il existe trois niveaux d’autorisation par défaut pour un site d’équipe SharePoint Online : Modification, Lecture et Contrôle total. Le tableau suivant indique la corrélation par défaut des groupes SharePoint et les niveaux d’autorisation affectés :</span><span class="sxs-lookup"><span data-stu-id="1c761-p101">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level. There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control. The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>
  
|<span data-ttu-id="1c761-115">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="1c761-115">**SharePoint group**</span></span>|<span data-ttu-id="1c761-116">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="1c761-116">**Permission level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c761-117">\<Membres du name> de site</span><span class="sxs-lookup"><span data-stu-id="1c761-117">\<site name> Members</span></span>  <br/> |<span data-ttu-id="1c761-118">Modifier</span><span class="sxs-lookup"><span data-stu-id="1c761-118">Edit</span></span>  <br/> |
|<span data-ttu-id="1c761-119">\<Visiteurs du site name></span><span class="sxs-lookup"><span data-stu-id="1c761-119">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="1c761-120">Lecture</span><span class="sxs-lookup"><span data-stu-id="1c761-120">Read</span></span>  <br/> |
|<span data-ttu-id="1c761-121">\<Propriétaires de sites name></span><span class="sxs-lookup"><span data-stu-id="1c761-121">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="1c761-122">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="1c761-122">Full control</span></span>  <br/> |
   
 <span data-ttu-id="1c761-p102">**Conseil :** vous pouvez créer des groupes SharePoint et des niveaux d’autorisation supplémentaires. Cependant, nous vous recommandons d’utiliser les groupes SharePoint par défaut et les niveaux d’autorisation pour votre site SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="1c761-p102">**Best practice:** You can create additional SharePoint groups and permission levels. However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>
  
<span data-ttu-id="1c761-125">Voici les groupes et les niveaux d'autorisation SharePoint par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c761-125">Here are the default SharePoint groups and permission levels.</span></span>
  
![Les groupes et les niveaux d'autorisation SharePoint par défaut pour un site SharePoint Online.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="1c761-127">Phase 2 : attribution des autorisations aux utilisateurs membres de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="1c761-127">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="1c761-p103">Vous pouvez attribuer des autorisations aux utilisateurs en ajoutant leur compte d’utilisateur, ou un groupe Office 365 ou Azure AD dont est membre le compte d’utilisateur, aux groupes SharePoint. Une fois ajoutés, les comptes d’utilisateur Office 365 reçoivent, directement ou indirectement via l’appartenance à un groupe Office 365 ou Azure AD, le niveau d’autorisation associé au groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c761-p103">You can assign permissions to users by adding their user account, or an Office 365 or Azure AD group of which the user account is a member, to the SharePoint groups. Once added, the Office 365 user accounts, either directly or indirectly via membership in an Office 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>
  
<span data-ttu-id="1c761-130">En prenant l’exemple des groupes SharePoint par défaut :</span><span class="sxs-lookup"><span data-stu-id="1c761-130">Using the default SharePoint groups as an example:</span></span>
  
- <span data-ttu-id="1c761-131">Les membres du groupe SharePoint \*\* \<name> membres du site\*\* , qui peuvent inclure à la fois des comptes d'utilisateur et des groupes, se voient attribuer le niveau d'autorisation **modifier**</span><span class="sxs-lookup"><span data-stu-id="1c761-131">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>
    
- <span data-ttu-id="1c761-132">Les membres du groupe SharePoint \*\* \<name> visiteurs du site\*\* , qui peuvent inclure à la fois des comptes d'utilisateur et des groupes, se voient attribuer le niveau d'autorisation **lecture**</span><span class="sxs-lookup"><span data-stu-id="1c761-132">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>
    
- <span data-ttu-id="1c761-133">Les membres du groupe SharePoint \*\* \<name> propriétaires de site\*\* , qui peuvent inclure à la fois des comptes d'utilisateur et des groupes, se voient attribuer le niveau d'autorisation **contrôle total** .</span><span class="sxs-lookup"><span data-stu-id="1c761-133">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>
    
 <span data-ttu-id="1c761-p104">**Conseil :** même si vous pouvez gérer les autorisations dans chaque compte d’utilisateur, nous vous recommandons plutôt d’utiliser un seul groupe Azure AD, appelé groupe d’accès. Cela simplifie la gestion des autorisations via l’appartenance au groupe d’accès, plutôt que via la gestion de la liste des comptes d’utilisateur pour chaque groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c761-p104">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead. This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>
  
<span data-ttu-id="1c761-p105">Les groupes Azure AD pour Office 365 sont différents des groupes Office 365. Les groupes Azure AD apparaissent dans le Centre d’administration Office. Leur **type** est défini sur **Sécurité** et ils n’ont pas d’adresse e-mail. Les groupes Azure AD peuvent être gérés dans :</span><span class="sxs-lookup"><span data-stu-id="1c761-p105">Azure AD groups for Office 365 are different than Office 365 groups. Azure AD groups appear in the Office Admin center with their **Type** set to **Security** and do not have an email address. Azure AD groups can be managed within:</span></span>
  
- <span data-ttu-id="1c761-139">Windows Server Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="1c761-139">Windows Server Active Directory (AD)</span></span>
    
    <span data-ttu-id="1c761-p106">Ces groupes ont été créés dans votre infrastructure locale Windows Server AD et ont été synchronisés avec votre abonnement Office 365. Dans le Centre d’administration Office, ils affichent l’**état\*\*\*\*Synchronisés avec Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="1c761-p106">These are groups that have been created in your on-premises Windows Server AD infrastructure and synchronized to your Office 365 subscription. In the Office Admin center, these groups have a **Status** of **Synched with active directory**.</span></span>
    
- <span data-ttu-id="1c761-142">Office 365</span><span class="sxs-lookup"><span data-stu-id="1c761-142">Office 365</span></span>
    
    <span data-ttu-id="1c761-p107">Ces groupes ont été créés à l’aide du Centre d’administration Office, du portail Azure ou de Microsoft PowerShell. Dans le Centre d’administration Office, ils affichent l’**état\*\*\*\*Cloud**.</span><span class="sxs-lookup"><span data-stu-id="1c761-p107">These are groups that have been created using either the Office Admin center, the Azure portal, or Microsoft PowerShell. In the Office Admin center, these groups have a **Status** of **Cloud**.</span></span>
    
 <span data-ttu-id="1c761-145">**Conseil :** si vous utilisez Windows Server AD en local et que vous le synchronisez avec votre abonnement Office 365, gérez vos utilisateurs et groupes avec Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="1c761-145">**Best practice:** If you are using Windows Server AD on-premises and synchronizing with your Office 365 subscription, perform your user and group management with Windows Server AD.</span></span>
  
<span data-ttu-id="1c761-146">Pour les sites d’équipe SharePoint Online isolés, voici à quoi ressemble la structure recommandée du groupe :</span><span class="sxs-lookup"><span data-stu-id="1c761-146">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>
  
|<span data-ttu-id="1c761-147">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="1c761-147">**SharePoint group**</span></span>|<span data-ttu-id="1c761-148">**Groupe d’accès basé sur Azure AD**</span><span class="sxs-lookup"><span data-stu-id="1c761-148">**Azure AD-based access group**</span></span>|<span data-ttu-id="1c761-149">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="1c761-149">**Permission level**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c761-150">\<Membres du name> de site</span><span class="sxs-lookup"><span data-stu-id="1c761-150">\<site name> Members</span></span>  <br/> |<span data-ttu-id="1c761-151">\<Membres du name> de site</span><span class="sxs-lookup"><span data-stu-id="1c761-151">\<site name> Members</span></span>  <br/> |<span data-ttu-id="1c761-152">Modifier</span><span class="sxs-lookup"><span data-stu-id="1c761-152">Edit</span></span>  <br/> |
|<span data-ttu-id="1c761-153">\<Visiteurs du site name></span><span class="sxs-lookup"><span data-stu-id="1c761-153">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="1c761-154">\<Visionneuses de site name></span><span class="sxs-lookup"><span data-stu-id="1c761-154">\<site name> Viewers</span></span>  <br/> |<span data-ttu-id="1c761-155">Lecture</span><span class="sxs-lookup"><span data-stu-id="1c761-155">Read</span></span>  <br/> |
|<span data-ttu-id="1c761-156">\<Propriétaires de sites name></span><span class="sxs-lookup"><span data-stu-id="1c761-156">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="1c761-157">\<Administrateurs de site name></span><span class="sxs-lookup"><span data-stu-id="1c761-157">\<site name> Admins</span></span>  <br/> |<span data-ttu-id="1c761-158">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="1c761-158">Full control</span></span>  <br/> |
   
 <span data-ttu-id="1c761-p108">**Conseil :** même si vous pouvez utiliser des groupes Office 365 ou Azure AD en tant que membres des groupes SharePoint, nous vous recommandons d’utiliser les groupes Azure AD. Grâce aux groupes Azure AD, gérés via Windows Server AD ou Office 365, vous bénéficiez d’une plus grande flexibilité pour attribuer des autorisations avec les groupes imbriqués.</span><span class="sxs-lookup"><span data-stu-id="1c761-p108">**Best practice:** Although you can use either Office 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups. Azure AD groups, managed either through Windows Server AD or Office 365, give you more flexibility to use nested groups to assign permissions.</span></span>
  
<span data-ttu-id="1c761-161">Voici les groupes SharePoint par défaut configurés pour utiliser les groupes d'accès basé sur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1c761-161">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>
  
![Utilisation de groupes d'accès en tant que membres des groupes de sites SharePoint Online par défaut.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
<span data-ttu-id="1c761-163">Lorsque vous concevez les trois groupes d’accès, rappelez-vous de ceci :</span><span class="sxs-lookup"><span data-stu-id="1c761-163">When designing the three access groups, keep the following in mind:</span></span>
  
- <span data-ttu-id="1c761-164">Le groupe d'accès \*\* \<administrateurs de site name>\*\* doit contenir seulement quelques membres, correspondant à un petit nombre d'administrateurs SharePoint Online qui gèrent le site d'équipe.</span><span class="sxs-lookup"><span data-stu-id="1c761-164">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>
    
- <span data-ttu-id="1c761-165">La plupart des membres de votre site se trouvent dans les groupes d'accès \*\* \<name> des membres\*\* du site ou \*\* \<des visionneuses de site name>\*\* .</span><span class="sxs-lookup"><span data-stu-id="1c761-165">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups.</span></span> <span data-ttu-id="1c761-166">Étant donné que les membres du site dans le groupe d'accès \*\* \<membres du site name>\*\* ont la possibilité de supprimer ou de modifier les ressources du site, réfléchissez bien à son appartenance.</span><span class="sxs-lookup"><span data-stu-id="1c761-166">Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership.</span></span> <span data-ttu-id="1c761-167">En cas de doute, ajoutez le membre du site au groupe d'accès \*\* \<name> les utilisateurs du site\*\* .</span><span class="sxs-lookup"><span data-stu-id="1c761-167">When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>
    
<span data-ttu-id="1c761-168">Voici un exemple des groupes SharePoint et des groupes d'accès pour un site isolé nommé ProjectX.</span><span class="sxs-lookup"><span data-stu-id="1c761-168">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>
  
![Exemple d'utilisation de groupes d'accès pour un site SharePoint Online nommé ProjectX.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="1c761-170">Phase 3: utiliser des groupes Azure AD imbriqués</span><span class="sxs-lookup"><span data-stu-id="1c761-170">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="1c761-171">Pour un projet impliquant un petit nombre d’utilisateurs, vous pouvez ajouter, dans la plupart des cas, un seul niveau de groupes d’accès basés sur Azure AD aux groupes SharePoint du site.</span><span class="sxs-lookup"><span data-stu-id="1c761-171">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios.</span></span> <span data-ttu-id="1c761-172">Toutefois, si vous avez un grand nombre de personnes et que ces personnes sont déjà membres de groupes Azure AD établis, vous pouvez plus facilement attribuer des autorisations SharePoint à l'aide de groupes imbriqués ou de groupes qui contiennent d'autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="1c761-172">However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>
  
<span data-ttu-id="1c761-p111">Par exemple, vous souhaitez créer un site d’équipe SharePoint Online isolé pour favoriser la collaboration entre les responsables des services ventes, marketing, ingénierie, juridique et support technique, mais ils ont déjà leur propre groupe de comptes de responsable. Au lieu de créer un groupe pour les nouveaux membres du site et d’y placer tous les comptes de responsable un par un, placez les groupes de responsables existants pour chaque service dans le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="1c761-p111">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership. Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>
  
 <span data-ttu-id="1c761-p112"> Si vous partagez un abonnement Office 365 avec d’autres organisations, il peut s’avérer difficile de gérer un seul niveau de groupe pour le site isolé d’une organisation en raison du nombre important de comptes d’utilisateur. Dans ce cas, vous pouvez utiliser les groupes Azure AD imbriqués pour chaque organisation dont les groupes gèrent les autorisations.</span><span class="sxs-lookup"><span data-stu-id="1c761-p112">If you are sharing an Office 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts. In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>
  
<span data-ttu-id="1c761-177">Pour utiliser les groupes Azure AD imbriqués, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1c761-177">To use nested Azure AD groups:</span></span>
  
1. <span data-ttu-id="1c761-178">Identifiez ou créez les groupes Azure AD qui contiendront les comptes d’utilisateur et ajoutez les comptes d’utilisateur en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="1c761-178">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>
    
2. <span data-ttu-id="1c761-179">Créez le groupe d’accès basé sur Azure AD conteneur qui contiendra les autres groupes Azure AD et ajoutez ces groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="1c761-179">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>
    
3.  <span data-ttu-id="1c761-180"> Pour définir le niveau d’accès approprié pour le groupe d’accès conteneur, identifiez le groupe SharePoint et définissez le niveau d’autorisation correspondant.</span><span class="sxs-lookup"><span data-stu-id="1c761-180">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1c761-181">Vous ne pouvez pas utiliser des groupes Office 365 imbriqués.</span><span class="sxs-lookup"><span data-stu-id="1c761-181">You cannot use nested Office 365 groups.</span></span> 
  
<span data-ttu-id="1c761-182">Voici un exemple de groupes Azure AD imbriqués pour le groupe d'accès au membre ProjectX.</span><span class="sxs-lookup"><span data-stu-id="1c761-182">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>
  
![Un exemple d'utilisation de groupes d'accès imbriqués pour le groupe d'accès membres pour le site ProjectX.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
<span data-ttu-id="1c761-184">Étant donné que tous les comptes d'utilisateur dans les équipes de recherche, d'ingénierie et de projet sont destinés à être membres de site, il est plus facile d'ajouter leurs groupes Azure AD au groupe d'accès membres ProjectX.</span><span class="sxs-lookup"><span data-stu-id="1c761-184">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="1c761-185">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1c761-185">Next step</span></span>

<span data-ttu-id="1c761-186">Lorsque vous êtes prêt à créer et à configurer un site isolé en production, consultez la rubrique [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="1c761-186">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1c761-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c761-187">See Also</span></span>

[<span data-ttu-id="1c761-188">Sites d'équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="1c761-188">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="1c761-189">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1c761-189">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="1c761-190">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1c761-190">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



