---
title: Déployer des sites SharePoint Online pour trois niveaux de protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: 'Résumé : Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.'
ms.openlocfilehash: 69da99c29d3527285547ed824e45fb7aa31e1910
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999257"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="a0788-103">Déployer des sites SharePoint Online pour trois niveaux de protection</span><span class="sxs-lookup"><span data-stu-id="a0788-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

 <span data-ttu-id="a0788-104">**Résumé :** Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="a0788-104">**Summary:** Create and configure SharePoint Online team sites for various levels of information protection.</span></span>
  
<span data-ttu-id="a0788-p101">Utilisez les étapes de cet article pour concevoir et déployer des sites d’équipe SharePoint Online de base de référence, sensibles et hautement confidentiels. Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="a0788-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="a0788-107">Sites d’équipe SharePoint Online de base de référence</span><span class="sxs-lookup"><span data-stu-id="a0788-107">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="a0788-p102">La protection Base de référence inclut les sites d’équipe publics et privés. Les sites d’équipe publics peuvent être découverts et sont accessibles par toute personne de l’organisation. Les sites privés peuvent être découverts et sont accessibles seulement par les membres du groupe Office 365 associé au site d’équipe. Ces deux types de sites d’équipe permettent aux membres de partager le site avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a0788-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="a0788-112">Public</span><span class="sxs-lookup"><span data-stu-id="a0788-112">Public</span></span>

<span data-ttu-id="a0788-113">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations publics, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a0788-113">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="a0788-114">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="a0788-114">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="a0788-115">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="a0788-115">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="a0788-116">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="a0788-116">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="a0788-117">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="a0788-117">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="a0788-118">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="a0788-118">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="a0788-119">Dans **Nom du Site**, tapez un nom pour le site d’équipe public.</span><span class="sxs-lookup"><span data-stu-id="a0788-119">In **Site name**, type a name for the public team site.</span></span> 
    
6. <span data-ttu-id="a0788-120">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="a0788-120">In **Team site description**, type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="a0788-121">Dans **Paramètres de confidentialité**, sélectionnez **Public - tout le monde dans l’organisation peut accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0788-121">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="a0788-122">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a0788-122">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="a0788-123">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a0788-123">Here is your resulting configuration.</span></span>
  
![Protection de base pour un site d’équipe SharePoint Online public.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="a0788-125">Private</span><span class="sxs-lookup"><span data-stu-id="a0788-125">Private</span></span>

<span data-ttu-id="a0788-126">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations privés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a0788-126">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="a0788-127">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="a0788-127">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="a0788-128">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="a0788-128">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="a0788-129">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="a0788-129">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="a0788-130">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="a0788-130">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="a0788-131">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="a0788-131">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="a0788-132">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="a0788-132">In **Site name**, type a name for the private team site.</span></span> 
    
6. <span data-ttu-id="a0788-133">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="a0788-133">In **Team site description,** type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="a0788-134">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0788-134">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="a0788-135">Dans le volet **Qui voulez-vous ajouter ?**, dans **Ajouter des membres**, tapez les noms des comptes d’utilisateurs qui ont accès à ce site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="a0788-135">On the **Who do you want to add?** pane, in **Add members**, type the names of user accounts that have access to this private team site.</span></span>
    
9. <span data-ttu-id="a0788-136">Quand vous avez fini d’ajouter l’ensemble initial des membres au site, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a0788-136">When you are done adding the initial set of members to the site, click **Finish**</span></span>
    
<span data-ttu-id="a0788-137">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a0788-137">Here is your resulting configuration.</span></span>
  
![Protection de base pour le site d’équipe SharePoint Online privé.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="a0788-139">Sites d’équipe SharePoint Online sensibles</span><span class="sxs-lookup"><span data-stu-id="a0788-139">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="a0788-140">Un site d’équipe SharePoint Online sensible est un site d’équipe isolé. En d’autres termes, les autorisations sont contrôlées selon l’appartenance de l’utilisateur à des groupes SharePoint, et non selon son appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="a0788-140">A sensitive SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="a0788-141">La création d’un site d’équipe isolé se déroule en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="a0788-141">To create an isolated team site, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="a0788-142">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="a0788-142">Step 1: Design your isolated site</span></span>

<span data-ttu-id="a0788-143">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="a0788-143">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="a0788-144">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0788-144">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="a0788-145">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0788-145">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="a0788-146">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="a0788-146">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="a0788-147">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-147">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="a0788-148">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="a0788-148">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="a0788-149">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="a0788-149">**SharePoint group**</span></span>|<span data-ttu-id="a0788-150">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="a0788-150">**Permission level**</span></span>|<span data-ttu-id="a0788-151">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="a0788-151">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0788-152">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-152">[site name] Members</span></span>  <br/> |<span data-ttu-id="a0788-153">Éditer</span><span class="sxs-lookup"><span data-stu-id="a0788-153">Edit</span></span>  <br/> |<span data-ttu-id="a0788-154">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-154">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="a0788-155">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-155">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="a0788-156">Lire</span><span class="sxs-lookup"><span data-stu-id="a0788-156">Read</span></span>  <br/> |<span data-ttu-id="a0788-157">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-157">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="a0788-158">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-158">[site name] Owners</span></span>  <br/> |<span data-ttu-id="a0788-159">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="a0788-159">Full control</span></span>  <br/> |<span data-ttu-id="a0788-160">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-160">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="a0788-p105">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-p105">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="a0788-163">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="a0788-163">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="a0788-164">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="a0788-164">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="a0788-165">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="a0788-165">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="a0788-166">Déterminer les comptes d’utilisateur et les groupes à ajouter à chacun de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-166">Determine the user accounts and groups to add to each of your access groups.</span></span>
    
- <span data-ttu-id="a0788-167">Créer les groupes d’accès, et ajouter les utilisateurs et les groupes membres.</span><span class="sxs-lookup"><span data-stu-id="a0788-167">Create the access groups and add the user and group members.</span></span>
    
<span data-ttu-id="a0788-168">Pour la procédure détaillée, consultez la **phase 1** de [Déployer un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="a0788-168">For the detailed steps, see **Phase 1** of [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="a0788-169">Ensuite, vous devez créer le site d’équipe SharePoint Online en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="a0788-169">Next, you create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="a0788-170">Connectez-vous au centre d’administration avec un compte qui servira également à gérer le site d’équipe SharePoint Online (par un administrateur SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="a0788-170">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="a0788-171">Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="a0788-171">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="a0788-172">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="a0788-172">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="a0788-173">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="a0788-173">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="a0788-174">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="a0788-174">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="a0788-175">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="a0788-175">In **Site name**, type a name for the private team site.</span></span>
    
6. <span data-ttu-id="a0788-176">Dans **Description du site d’équipe**, tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="a0788-176">In **Team site description**, type an optional description.</span></span>
    
7. <span data-ttu-id="a0788-177">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a0788-177">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="a0788-178">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a0788-178">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="a0788-179">Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez les autorisations en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="a0788-179">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>
  
1. <span data-ttu-id="a0788-180">Choisissez le Nom d’utilisateur principal (UPN) de l’administrateur informatique ou d’une autre personne qui sera chargée de répondre aux demandes d’accès au site (belindan@contoso.com est un exemple d’UPN).</span><span class="sxs-lookup"><span data-stu-id="a0788-180">Determine the User Principal Name (UPN) of the IT administrator or other person who will be responsible for responding to and addressing requests for access to the site (belindan@contoso.com is an example of a UPN).</span></span> 
    
2. <span data-ttu-id="a0788-181">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.</span><span class="sxs-lookup"><span data-stu-id="a0788-181">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
3. <span data-ttu-id="a0788-182">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="a0788-182">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
4. <span data-ttu-id="a0788-183">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="a0788-183">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
5. <span data-ttu-id="a0788-184">Dans la boîte de dialogue **Paramètres des demandes d’accès** :</span><span class="sxs-lookup"><span data-stu-id="a0788-184">In the **Access Requests Settings** dialog box:</span></span>
    
  - <span data-ttu-id="a0788-185">Décochez les cases **Autoriser les membres à partager le site, ainsi que des fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site**.</span><span class="sxs-lookup"><span data-stu-id="a0788-185">Clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes.</span></span>
    
  - <span data-ttu-id="a0788-186">Tapez le nom d’utilisateur principal de votre administrateur informatique de l’étape 1 dans **Envoyer toutes les demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="a0788-186">Type the UPN of your IT administrator from step 1 in **Send all requests for access**.</span></span>
    
  - <span data-ttu-id="a0788-187">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0788-187">Click **OK**.</span></span>
    
6. <span data-ttu-id="a0788-188">Sous l’onglet **Autorisations** de votre navigateur, cliquez sur **Membres de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a0788-188">On the **Permissions** tab of your browser, click **[site name] Members** in the list.</span></span>
    
7. <span data-ttu-id="a0788-189">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="a0788-189">In **People and Groups**, click **New**.</span></span>
    
8. <span data-ttu-id="a0788-190">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des membres de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="a0788-190">In the **Share** dialog box, type the name of your site members access group for this site, select it, and then click **Share**.</span></span>
    
9. <span data-ttu-id="a0788-191">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="a0788-191">Click the back button on your browser.</span></span>
    
10. <span data-ttu-id="a0788-192">Cliquez sur **Propriétaires de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a0788-192">Click **[site name] Owners** in the list.</span></span>
    
11. <span data-ttu-id="a0788-193">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="a0788-193">In **People and Groups**, click **New**.</span></span>
    
12. <span data-ttu-id="a0788-194">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des administrateurs de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="a0788-194">In the **Share** dialog box, type the name of the site administrators access group for this site, select it, and then click **Share**.</span></span>
    
13. <span data-ttu-id="a0788-195">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="a0788-195">Click the back button on your browser.</span></span>
    
14. <span data-ttu-id="a0788-196">Cliquez sur **Visiteurs de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a0788-196">Click **[site name] Visitors** in the list.</span></span>
    
15. <span data-ttu-id="a0788-197">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="a0788-197">In **People and Groups**, click **New**.</span></span>
    
16. <span data-ttu-id="a0788-198">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des personnes consultant ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="a0788-198">In the **Share** dialog box, type the name of the site viewers access group for this site, select it, and then click **Share**.</span></span>
    
17. <span data-ttu-id="a0788-199">Fermez l’onglet **Autorisations** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="a0788-199">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="a0788-200">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="a0788-200">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="a0788-201">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="a0788-201">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="a0788-202">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="a0788-202">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="a0788-203">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="a0788-203">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="a0788-204">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a0788-204">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="a0788-205">La possibilité pour les non-membres de demander l’accès est activée.</span><span class="sxs-lookup"><span data-stu-id="a0788-205">The ability for non-members to request access is enabled.</span></span>
    
<span data-ttu-id="a0788-206">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a0788-206">Here is your resulting configuration.</span></span>
  
![Protection des données sensibles d’un site d’équipe SharePoint Online isolé.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="a0788-208">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a0788-208">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="a0788-209">Sites d’équipe SharePoint Online hautement confidentiels</span><span class="sxs-lookup"><span data-stu-id="a0788-209">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="a0788-210">Un site d’équipe SharePoint Online hautement confidentiel est un site d’équipe isolé, ce qui signifie que les autorisations sont contrôlées via l’appartenance à des groupes SharePoint, au lieu de l’appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="a0788-210">A highly confidential SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="a0788-211">Pour créer un site d’équipe isolé pour des informations et une collaboration hautement confidentielles, vous devez procéder en deux étapes principales.</span><span class="sxs-lookup"><span data-stu-id="a0788-211">To create an isolated team site for highly confidential information and collaboration, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="a0788-212">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="a0788-212">Step 1: Design your isolated site</span></span>

<span data-ttu-id="a0788-213">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="a0788-213">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="a0788-214">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0788-214">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="a0788-215">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0788-215">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="a0788-216">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="a0788-216">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="a0788-217">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-217">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="a0788-218">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="a0788-218">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="a0788-219">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="a0788-219">**SharePoint group**</span></span>|<span data-ttu-id="a0788-220">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="a0788-220">**Permission level**</span></span>|<span data-ttu-id="a0788-221">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="a0788-221">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0788-222">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-222">[site name] Members</span></span>  <br/> |<span data-ttu-id="a0788-223">Éditer</span><span class="sxs-lookup"><span data-stu-id="a0788-223">Edit</span></span>  <br/> |<span data-ttu-id="a0788-224">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-224">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="a0788-225">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-225">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="a0788-226">Lire</span><span class="sxs-lookup"><span data-stu-id="a0788-226">Read</span></span>  <br/> |<span data-ttu-id="a0788-227">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-227">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="a0788-228">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-228">[site name] Owners</span></span>  <br/> |<span data-ttu-id="a0788-229">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="a0788-229">Full control</span></span>  <br/> |<span data-ttu-id="a0788-230">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="a0788-230">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="a0788-p107">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-p107">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="a0788-233">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="a0788-233">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="a0788-234">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="a0788-234">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="a0788-235">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="a0788-235">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="a0788-236">déterminer les utilisateurs et les membres du groupe de chacun de vos groupes d’accès ;</span><span class="sxs-lookup"><span data-stu-id="a0788-236">Determine the user and group members of each of your access groups</span></span>
    
- <span data-ttu-id="a0788-237">créer les groupes d’accès et ajouter les utilisateurs et les membres du groupe ;</span><span class="sxs-lookup"><span data-stu-id="a0788-237">Create the access groups and add the user and group members</span></span>
    
- <span data-ttu-id="a0788-238">créer un site d’équipe isolé qui utilise vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="a0788-238">Create an isolated team site that uses your access groups</span></span>
    
<span data-ttu-id="a0788-239">Pour la procédure détaillée, consultez [Déployer un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="a0788-239">For the detailed steps, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="a0788-240">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="a0788-240">The results of the permission settings are:</span></span>
  
- <span data-ttu-id="a0788-241">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="a0788-241">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="a0788-242">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="a0788-242">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="a0788-243">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="a0788-243">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="a0788-244">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a0788-244">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="a0788-245">La possibilité pour les non-membres de demander l’accès est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a0788-245">The ability for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="a0788-246">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a0788-246">Here is your resulting configuration.</span></span>
  
![Protection avec un niveau de confidentialité élevé pour un site d’équipe SharePoint Online isolé.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="a0788-248">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a0788-248">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="a0788-249">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a0788-249">Next step</span></span>

[<span data-ttu-id="a0788-250">Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="a0788-250">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)

## <a name="see-also"></a><span data-ttu-id="a0788-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0788-251">See also</span></span>

[<span data-ttu-id="a0788-252">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a0788-252">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="a0788-253">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="a0788-253">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="a0788-254">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="a0788-254">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
