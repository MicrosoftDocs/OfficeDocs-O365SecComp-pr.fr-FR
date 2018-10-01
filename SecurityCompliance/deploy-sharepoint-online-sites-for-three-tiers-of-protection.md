---
title: Déployer des sites SharePoint Online pour trois niveaux de protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 06/05/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
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
ms.openlocfilehash: 54392194f7ac5ce90337df3f33e23db595b1aa5c
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345826"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="cbea8-103">Déployer des sites SharePoint Online pour trois niveaux de protection</span><span class="sxs-lookup"><span data-stu-id="cbea8-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

 <span data-ttu-id="cbea8-104">**Résumé :** Créez et configurez des sites d’équipe SharePoint Online avec différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="cbea8-104">**Summary:** Create and configure SharePoint Online team sites for various levels of information protection.</span></span>
  
<span data-ttu-id="cbea8-p101">Utilisez les étapes de cet article pour concevoir et déployer des sites d’équipe SharePoint Online de base de référence, sensibles et hautement confidentiels. Pour plus d’informations sur ces trois niveaux de protection, consultez [Sécuriser des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="cbea8-107">Sites d’équipe SharePoint Online de base de référence</span><span class="sxs-lookup"><span data-stu-id="cbea8-107">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="cbea8-p102">La protection Base de référence inclut les sites d’équipe publics et privés. Les sites d’équipe publics peuvent être découverts et sont accessibles par toute personne de l’organisation. Les sites privés peuvent être découverts et sont accessibles seulement par les membres du groupe Office 365 associé au site d’équipe. Ces deux types de sites d’équipe permettent aux membres de partager le site avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cbea8-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="cbea8-112">Public</span><span class="sxs-lookup"><span data-stu-id="cbea8-112">Public</span></span>

<span data-ttu-id="cbea8-113">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations publics, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cbea8-113">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="cbea8-p103">Connectez-vous au portail Office 365 avec un compte qui sera également utilisé pour administrer le site d’équipe SharePoint Online (un administrateur SharePoint Online). Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p103">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="cbea8-116">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-116">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="cbea8-117">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-117">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="cbea8-118">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-118">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="cbea8-119">Dans **Nom du Site**, tapez un nom pour le site d’équipe public.</span><span class="sxs-lookup"><span data-stu-id="cbea8-119">In **Site name**, type a name for the public team site.</span></span> 
    
6. <span data-ttu-id="cbea8-120">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="cbea8-120">In **Team site description**, type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="cbea8-121">Dans **Paramètres de confidentialité**, sélectionnez **Public - tout le monde dans l’organisation peut accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-121">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="cbea8-122">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-122">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="cbea8-123">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="cbea8-123">Here is your resulting configuration.</span></span>
  
![Protection de base pour un site d’équipe SharePoint Online public.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="cbea8-125">Private</span><span class="sxs-lookup"><span data-stu-id="cbea8-125">Private</span></span>

<span data-ttu-id="cbea8-126">Pour créer un site d’équipe SharePoint Online de base de référence avec un accès et des autorisations privés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cbea8-126">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="cbea8-p104">Connectez-vous au portail Office 365 avec un compte qui sera également utilisé pour administrer le site d’équipe SharePoint Online (un administrateur SharePoint Online). Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p104">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="cbea8-129">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-129">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="cbea8-130">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-130">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="cbea8-131">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-131">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="cbea8-132">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="cbea8-132">In **Site name**, type a name for the private team site.</span></span> 
    
6. <span data-ttu-id="cbea8-133">Dans **Description du site d’équipe**, tapez une description de l’objectif du site.</span><span class="sxs-lookup"><span data-stu-id="cbea8-133">In **Team site description,** type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="cbea8-134">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-134">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="cbea8-135">Dans le volet **Qui voulez-vous ajouter ?**, dans **Ajouter des membres**, tapez les noms des comptes d’utilisateurs qui ont accès à ce site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="cbea8-135">On the **Who do you want to add?** pane, in **Add members**, type the names of user accounts that have access to this private team site.</span></span>
    
9. <span data-ttu-id="cbea8-136">Quand vous avez fini d’ajouter l’ensemble initial des membres au site, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-136">When you are done adding the initial set of members to the site, click **Finish**</span></span>
    
<span data-ttu-id="cbea8-137">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="cbea8-137">Here is your resulting configuration.</span></span>
  
![Protection de base pour le site d’équipe SharePoint Online privé.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="cbea8-139">Sites d’équipe SharePoint Online sensibles</span><span class="sxs-lookup"><span data-stu-id="cbea8-139">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="cbea8-140">Un site d’équipe SharePoint Online sensible est un site d’équipe isolé. En d’autres termes, les autorisations sont contrôlées selon l’appartenance de l’utilisateur à des groupes SharePoint, et non selon son appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="cbea8-140">A sensitive SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="cbea8-141">La création d’un site d’équipe isolé se déroule en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="cbea8-141">To create an isolated team site, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="cbea8-142">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="cbea8-142">Step 1: Design your isolated site</span></span>

<span data-ttu-id="cbea8-143">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="cbea8-143">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="cbea8-144">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cbea8-144">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="cbea8-145">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cbea8-145">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="cbea8-146">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="cbea8-146">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="cbea8-147">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-147">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="cbea8-148">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="cbea8-148">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="cbea8-149">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="cbea8-149">**SharePoint group**</span></span>|<span data-ttu-id="cbea8-150">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="cbea8-150">**Permission level**</span></span>|<span data-ttu-id="cbea8-151">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="cbea8-151">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbea8-152">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-152">[site name] Members</span></span>  <br/> |<span data-ttu-id="cbea8-153">Éditer</span><span class="sxs-lookup"><span data-stu-id="cbea8-153">Edit</span></span>  <br/> |<span data-ttu-id="cbea8-154">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-154">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="cbea8-155">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-155">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="cbea8-156">Lire</span><span class="sxs-lookup"><span data-stu-id="cbea8-156">Read</span></span>  <br/> |<span data-ttu-id="cbea8-157">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-157">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="cbea8-158">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-158">[site name] Owners</span></span>  <br/> |<span data-ttu-id="cbea8-159">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="cbea8-159">Full control</span></span>  <br/> |<span data-ttu-id="cbea8-160">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-160">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="cbea8-p105">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-p105">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="cbea8-163">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-163">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="cbea8-164">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="cbea8-164">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="cbea8-165">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="cbea8-165">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="cbea8-166">Déterminer les comptes d’utilisateur et les groupes à ajouter à chacun de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-166">Determine the user accounts and groups to add to each of your access groups.</span></span>
    
- <span data-ttu-id="cbea8-167">Créer les groupes d’accès, et ajouter les utilisateurs et les groupes membres.</span><span class="sxs-lookup"><span data-stu-id="cbea8-167">Create the access groups and add the user and group members.</span></span>
    
<span data-ttu-id="cbea8-168">Pour la procédure détaillée, consultez la **phase 1** de [Déployer un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-168">For the detailed steps, see **Phase 1** of [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="cbea8-169">Ensuite, vous devez créer le site d’équipe SharePoint Online en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="cbea8-169">Next, you create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="cbea8-p106">Connectez-vous au portail Office 365 avec un compte qui sera également utilisé pour administrer le site d’équipe SharePoint Online (un administrateur SharePoint Online). Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p106">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="cbea8-172">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-172">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="cbea8-173">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-173">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="cbea8-174">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-174">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="cbea8-175">Dans **Nom du site**, tapez un nom pour le site d’équipe privé.</span><span class="sxs-lookup"><span data-stu-id="cbea8-175">In **Site name**, type a name for the private team site.</span></span>
    
6. <span data-ttu-id="cbea8-176">Dans **Description du site d’équipe**, tapez une description facultative.</span><span class="sxs-lookup"><span data-stu-id="cbea8-176">In **Team site description**, type an optional description.</span></span>
    
7. <span data-ttu-id="cbea8-177">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-177">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="cbea8-178">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-178">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="cbea8-179">Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez les autorisations en suivant cette procédure.</span><span class="sxs-lookup"><span data-stu-id="cbea8-179">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>
  
1. <span data-ttu-id="cbea8-p107">Choisissez le Nom d’utilisateur principal (UPN) de l’administrateur informatique ou d’une autre personne qui sera chargée de répondre aux demandes d’accès au site (belindan@contoso.com est un exemple d’UPN). Notez cet UPN ici : ![](./media/Common-Images/TableLine.png).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p107">Determine the User Principal Name (UPN) of the IT administrator or other person who will be responsible for responding to and addressing requests for access to the site (belindan@contoso.com is an example of a UPN). Write that UPN here: ![](./media/Common-Images/TableLine.png).</span></span>
    
2. <span data-ttu-id="cbea8-182">Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-182">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
3. <span data-ttu-id="cbea8-183">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-183">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
4. <span data-ttu-id="cbea8-184">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-184">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
5. <span data-ttu-id="cbea8-185">Dans la boîte de dialogue **Paramètres des demandes d’accès** :</span><span class="sxs-lookup"><span data-stu-id="cbea8-185">In the **Access Requests Settings** dialog box:</span></span>
    
  - <span data-ttu-id="cbea8-186">Décochez les cases **Autoriser les membres à partager le site, ainsi que des fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-186">Clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes.</span></span>
    
  - <span data-ttu-id="cbea8-187">Tapez le nom d’utilisateur principal de votre administrateur informatique de l’étape 1 dans **Envoyer toutes les demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-187">Type the UPN of your IT administrator from step 1 in **Send all requests for access**.</span></span>
    
  - <span data-ttu-id="cbea8-188">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-188">Click **OK**.</span></span>
    
6. <span data-ttu-id="cbea8-189">Sous l’onglet **Autorisations** de votre navigateur, cliquez sur **Membres de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cbea8-189">On the **Permissions** tab of your browser, click **[site name] Members** in the list.</span></span>
    
7. <span data-ttu-id="cbea8-190">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-190">In **People and Groups**, click **New**.</span></span>
    
8. <span data-ttu-id="cbea8-191">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des membres de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-191">In the **Share** dialog box, type the name of your site members access group for this site, select it, and then click **Share**.</span></span>
    
9. <span data-ttu-id="cbea8-192">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cbea8-192">Click the back button on your browser.</span></span>
    
10. <span data-ttu-id="cbea8-193">Cliquez sur **Propriétaires de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cbea8-193">Click **[site name] Owners** in the list.</span></span>
    
11. <span data-ttu-id="cbea8-194">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-194">In **People and Groups**, click **New**.</span></span>
    
12. <span data-ttu-id="cbea8-195">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des administrateurs de site pour ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-195">In the **Share** dialog box, type the name of the site administrators access group for this site, select it, and then click **Share**.</span></span>
    
13. <span data-ttu-id="cbea8-196">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cbea8-196">Click the back button on your browser.</span></span>
    
14. <span data-ttu-id="cbea8-197">Cliquez sur **Visiteurs de [nom du site]** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="cbea8-197">Click **[site name] Visitors** in the list.</span></span>
    
15. <span data-ttu-id="cbea8-198">Dans **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-198">In **People and Groups**, click **New**.</span></span>
    
16. <span data-ttu-id="cbea8-199">Dans la boîte de dialogue **Partager**, tapez le nom du groupe d’accès des personnes consultant ce site, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-199">In the **Share** dialog box, type the name of the site viewers access group for this site, select it, and then click **Share**.</span></span>
    
17. <span data-ttu-id="cbea8-200">Fermez l’onglet **Autorisations** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="cbea8-200">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="cbea8-201">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="cbea8-201">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="cbea8-202">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-202">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="cbea8-203">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-203">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="cbea8-204">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-204">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="cbea8-205">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-205">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="cbea8-206">La possibilité pour les non-membres de demander l’accès est activée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-206">The ability for non-members to request access is enabled.</span></span>
    
<span data-ttu-id="cbea8-207">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="cbea8-207">Here is your resulting configuration.</span></span>
  
![Protection des données sensibles d’un site d’équipe SharePoint Online isolé.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="cbea8-209">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-209">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="cbea8-210">Sites d’équipe SharePoint Online hautement confidentiels</span><span class="sxs-lookup"><span data-stu-id="cbea8-210">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="cbea8-211">Un site d’équipe SharePoint Online hautement confidentiel est un site d’équipe isolé, ce qui signifie que les autorisations sont contrôlées via l’appartenance à des groupes SharePoint, au lieu de l’appartenance au groupe Office 365 associé au site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="cbea8-211">A highly confidential SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="cbea8-212">Pour créer un site d’équipe isolé pour des informations et une collaboration hautement confidentielles, vous devez procéder en deux étapes principales.</span><span class="sxs-lookup"><span data-stu-id="cbea8-212">To create an isolated team site for highly confidential information and collaboration, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="cbea8-213">Étape 1 : Concevoir votre site isolé</span><span class="sxs-lookup"><span data-stu-id="cbea8-213">Step 1: Design your isolated site</span></span>

<span data-ttu-id="cbea8-214">Pour concevoir votre site d’équipe isolé, vous devez déterminer :</span><span class="sxs-lookup"><span data-stu-id="cbea8-214">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="cbea8-215">Vos groupes et vos niveaux d’autorisation SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cbea8-215">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="cbea8-216">L’ensemble de groupes d’accès qui seront membres de vos groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cbea8-216">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="cbea8-217">L’ensemble de groupes d’accès recommandé est le suivant : un pour les membres du site, un pour les personnes consultant le site et un pour les administrateurs du site.</span><span class="sxs-lookup"><span data-stu-id="cbea8-217">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="cbea8-218">Si vous utilisez des groupes imbriqués au sein de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-218">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="cbea8-219">Par exemple, la structure des groupes et les niveaux d’autorisations recommandés se présentent comme ceci :</span><span class="sxs-lookup"><span data-stu-id="cbea8-219">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="cbea8-220">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="cbea8-220">**SharePoint group**</span></span>|<span data-ttu-id="cbea8-221">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="cbea8-221">**Permission level**</span></span>|<span data-ttu-id="cbea8-222">**Groupe d’accès (exemples)**</span><span class="sxs-lookup"><span data-stu-id="cbea8-222">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbea8-223">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-223">[site name] Members</span></span>  <br/> |<span data-ttu-id="cbea8-224">Éditer</span><span class="sxs-lookup"><span data-stu-id="cbea8-224">Edit</span></span>  <br/> |<span data-ttu-id="cbea8-225">Membres de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-225">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="cbea8-226">Visiteurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-226">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="cbea8-227">Lire</span><span class="sxs-lookup"><span data-stu-id="cbea8-227">Read</span></span>  <br/> |<span data-ttu-id="cbea8-228">Personnes consultant [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-228">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="cbea8-229">Propriétaires de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-229">[site name] Owners</span></span>  <br/> |<span data-ttu-id="cbea8-230">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="cbea8-230">Full control</span></span>  <br/> |<span data-ttu-id="cbea8-231">Administrateurs de [nom du site]</span><span class="sxs-lookup"><span data-stu-id="cbea8-231">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="cbea8-p108">Les groupes et les niveaux d’autorisation SharePoint sont créés par défaut pour un site d’équipe. Vous devez déterminer les noms de vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-p108">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="cbea8-234">Pour plus d’informations sur le processus de conception, consultez [Concevoir un site d’équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-234">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="cbea8-235">Étape 2 : Déployer votre site isolé</span><span class="sxs-lookup"><span data-stu-id="cbea8-235">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="cbea8-236">Pour déployer votre site isolé, vous devez d’abord :</span><span class="sxs-lookup"><span data-stu-id="cbea8-236">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="cbea8-237">déterminer les utilisateurs et les membres du groupe de chacun de vos groupes d’accès ;</span><span class="sxs-lookup"><span data-stu-id="cbea8-237">Determine the user and group members of each of your access groups</span></span>
    
- <span data-ttu-id="cbea8-238">créer les groupes d’accès et ajouter les utilisateurs et les membres du groupe ;</span><span class="sxs-lookup"><span data-stu-id="cbea8-238">Create the access groups and add the user and group members</span></span>
    
- <span data-ttu-id="cbea8-239">créer un site d’équipe isolé qui utilise vos groupes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbea8-239">Create an isolated team site that uses your access groups</span></span>
    
<span data-ttu-id="cbea8-240">Pour la procédure détaillée, consultez [Déployer un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-240">For the detailed steps, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="cbea8-241">Voici les résultats que vous devez escompter :</span><span class="sxs-lookup"><span data-stu-id="cbea8-241">The results of the permission settings are:</span></span>
  
- <span data-ttu-id="cbea8-242">Le groupe SharePoint **Propriétaires de [nom du site]** contient le groupe d’accès Administrateurs du site, dans lequel tous les membres ont le niveau d’autorisation **Contrôle total**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-242">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="cbea8-243">Le groupe SharePoint **Membres de [nom du site]** contient le groupe d’accès Membres du site, dans lequel tous les membres ont le niveau d’autorisation **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-243">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="cbea8-244">Le groupe SharePoint **Visiteurs de [nom du site]** contient le groupe d’accès Visiteurs du site, dans lequel tous les membres ont le niveau d’autorisation **Lire**.</span><span class="sxs-lookup"><span data-stu-id="cbea8-244">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="cbea8-245">La possibilité pour les membres d’inviter d’autres membres est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-245">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="cbea8-246">La possibilité pour les non-membres de demander l’accès est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-246">The ability for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="cbea8-247">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="cbea8-247">Here is your resulting configuration.</span></span>
  
![Protection avec un niveau de confidentialité élevé pour un site d’équipe SharePoint Online isolé.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="cbea8-249">Les membres du site, via l’appartenance à un des groupes d’accès, peuvent désormais collaborer sur les ressources du site de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cbea8-249">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="cbea8-250">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="cbea8-250">Next step</span></span>

[<span data-ttu-id="cbea8-251">Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="cbea8-251">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)
    
## <a name="see-also"></a><span data-ttu-id="cbea8-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbea8-252">See also</span></span>

[<span data-ttu-id="cbea8-253">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="cbea8-253">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="cbea8-254">Sécuriser les sites SharePoint Online dans un environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="cbea8-254">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="cbea8-255">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="cbea8-255">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="cbea8-256">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="cbea8-256">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




