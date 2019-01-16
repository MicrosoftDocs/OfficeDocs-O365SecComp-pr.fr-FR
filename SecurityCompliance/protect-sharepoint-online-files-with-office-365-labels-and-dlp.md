---
title: Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
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
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: 'Résumé : Appliquez des étiquettes Office 365 et des stratégies de protection contre la perte de données pour des sites d’équipe SharePoint Online, avec différents niveaux de protection des informations.'
ms.openlocfilehash: fd2fedf23b4e65bd32642b8528548f8a85533051
ms.sourcegitcommit: 6ff0233b5a1a07595f8b4d55db6b1327bcaa174c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28023439"
---
# <a name="protect-sharepoint-online-files-with-office-365-labels-and-dlp"></a><span data-ttu-id="0d6f7-103">Protéger les fichiers SharePoint Online avec des étiquettes Office 365 et la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="0d6f7-103">Protect SharePoint Online files with Office 365 labels and DLP</span></span>

 <span data-ttu-id="0d6f7-104">**Résumé :** Appliquez des étiquettes Office 365 et des stratégies de protection contre la perte de données pour des sites d’équipe SharePoint Online, avec différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-104">**Summary:** Apply Office 365 labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="0d6f7-p101">Suivez les étapes décrites dans cet article pour créer et déployer des étiquettes Office 365 et des stratégies DLP pour des sites d’équipe SharePoint Online de référence, sensibles et hautement confidentiels. Pour en savoir plus sur ces trois niveaux de protection, consultez la rubrique [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p101">Use the steps in this article to design and deploy Office 365 labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="0d6f7-107">Procédure</span><span class="sxs-lookup"><span data-stu-id="0d6f7-107">How this works</span></span>
1. <span data-ttu-id="0d6f7-p102">Créez les étiquettes de votre choix et publiez-les. La publication de ces étiquettes peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p102">Create the desired labels and publish these. It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="0d6f7-110">Pour les sites SharePoint souhaités, modifiez les paramètres de bibliothèque de documents pour appliquer une étiquette à des éléments dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-110">For the desired SharePoint sites, edit the document library settings to apply a label to items in the library.</span></span>
3. <span data-ttu-id="0d6f7-111">Créez des stratégies DLP pour exécuter des actions en fonction des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-111">Create DLP policies to take action based on the labels.</span></span>

<span data-ttu-id="0d6f7-p103">Lorsque les utilisateurs ajoutent un document à la bibliothèque, le document reçoit l’étiquette affectée par défaut. Les utilisateurs peuvent modifier l’étiquette si nécessaire. Lorsqu’un utilisateur partage un document en dehors de l’organisation, DLP vérifie si une étiquette est affectée et exécute l’action appropriée si une stratégie DLP correspond à l’étiquette. DLP vérifie l’existence d’autres correspondances de stratégie, comme la protection des fichiers avec des numéros de carte bancaire si ce type de stratégie est configuré.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p103">When users add a document to the library, the document will receive the assigned label by default. Users can change the label, if needed. When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label. DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="office-365-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="0d6f7-116">Étiquettes Office 365 pour vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d6f7-116">Office 365 labels for your SharePoint Online sites</span></span>

<span data-ttu-id="0d6f7-117">Il existe trois phases pour créer et attribuer des étiquettes Office 365 à des sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-117">There are three phases to creating and then assigning Office 365 labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-office-365-label-names"></a><span data-ttu-id="0d6f7-118">Phase 1 : Déterminer les noms des étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="0d6f7-118">Phase 1: Determine the Office 365 label names</span></span>

<span data-ttu-id="0d6f7-p104">Dans cette phase, vous déterminez les noms de vos étiquettes Office 365 pour les quatre niveaux de protection des informations appliqués aux sites d’équipe SharePoint Online. Le tableau suivant répertorie les noms recommandés pour chaque niveau.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p104">In this phase, you determine the names of your Office 365 labels for the four levels of information protection applied to SharePoint Online team sites. The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="0d6f7-121">**Niveau de protection du site d’équipe SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="0d6f7-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="0d6f7-122">**Nom de l’étiquette**</span><span class="sxs-lookup"><span data-stu-id="0d6f7-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d6f7-123">Base de référence - Public</span><span class="sxs-lookup"><span data-stu-id="0d6f7-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="0d6f7-124">Public interne</span><span class="sxs-lookup"><span data-stu-id="0d6f7-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="0d6f7-125">Base de référence - Privé</span><span class="sxs-lookup"><span data-stu-id="0d6f7-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="0d6f7-126">Private</span><span class="sxs-lookup"><span data-stu-id="0d6f7-126">Private</span></span>  <br/> |
|<span data-ttu-id="0d6f7-127">Sensible</span><span class="sxs-lookup"><span data-stu-id="0d6f7-127">Sensitive</span></span>  <br/> |<span data-ttu-id="0d6f7-128">Sensible</span><span class="sxs-lookup"><span data-stu-id="0d6f7-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="0d6f7-129">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="0d6f7-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="0d6f7-130">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="0d6f7-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-office-365-labels"></a><span data-ttu-id="0d6f7-131">Phase 2 : Créer les étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="0d6f7-131">Phase 2: Create the Office 365 labels</span></span>

<span data-ttu-id="0d6f7-132">Dans cette phase, vous créez puis vous publiez vos étiquettes déterminées pour les différents niveaux de protection des informations.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
<span data-ttu-id="0d6f7-133">Pour créer les étiquettes, vous pouvez utiliser le Centre d’administration Office 365 ou Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-133">To create the labels, you can use the Office 365 Admin center or Microsoft PowerShell.</span></span>
  
### <a name="create-office-365-labels-with-the-office-365-admin-center"></a><span data-ttu-id="0d6f7-134">Créer des étiquettes Office 365 avec le Centre d’administration Office 365</span><span class="sxs-lookup"><span data-stu-id="0d6f7-134">Create Office 365 labels with the Office 365 Admin center</span></span>

1. <span data-ttu-id="0d6f7-p105">Connectez-vous au portail Office 365 avec un compte disposant du rôle Administrateur de sécurité ou Administrateur d’entreprise. Pour obtenir de l’aide, consultez la rubrique [Se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p105">Sign in to the Office 365 portal with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="0d6f7-137">Sous l’onglet **Accueil Microsoft Office**, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-137">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="0d6f7-138">Sous le nouvel onglet **Centre d’administration Office** de votre navigateur, cliquez sur **Centres d’administration > Sécurité &amp; conformité**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-138">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
4. <span data-ttu-id="0d6f7-139">Sous le nouvel onglet **Accueil - Sécurité &amp; conformité de votre navigateur**, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-139">From the new **Home - Security &amp; Compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
5. <span data-ttu-id="0d6f7-140">Depuis le volet Office **Accueil > Étiquettes**, cliquez sur l’onglet **Rétention**, puis cliquez sur **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-140">From the **Home > Labels** pane, click the **Retention** tab, and then click **Create a label**.</span></span>
    
6. <span data-ttu-id="0d6f7-141">Dans le volet Office **Nom de l’étiquette**, entrez le nom de l’étiquette ainsi qu’une description pour les administrateurs et les utilisateurs, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-141">On the **Name your label** pane, type the name of the label, and then click **Next**.</span></span>

7. <span data-ttu-id="0d6f7-142">Dans le volet **Paramètres de l’étiquette**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-142">On the **Label settings** pane, click **Next**.</span></span>
    
8. <span data-ttu-id="0d6f7-143">Dans le volet Office **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-143">On the **Review your settings** pane, click **Create this label**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="0d6f7-144">Répétez les étapes 5 à 8 pour les autres étiquettes.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-144">Repeat steps 5-8 for your additional labels.</span></span>
    
### <a name="create-office-365-labels-with-powershell"></a><span data-ttu-id="0d6f7-145">Créer des étiquettes Office 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d6f7-145">Create Office 365 labels with PowerShell</span></span>

1. <span data-ttu-id="0d6f7-146">[Connectez-vous au Centre Sécurité &amp; conformité d’Office 365 en utilisant PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) à distance, et spécifiez les informations d’identification d’un compte disposant du rôle Administrateur de la sécurité ou Administrateur de la société.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-146">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) and specify the credentials of an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="0d6f7-147">Complétez la liste des noms d’étiquette, puis exécutez ces commandes à l’invite de commandes PowerShell :</span><span class="sxs-lookup"><span data-stu-id="0d6f7-147">Fill out the list of label names, and then run these commands at the PowerShell command prompt:</span></span>
    
  ```
  $labelNames=@(<list of label names, each enclosed in quotes and separated by commas>)
ForEach ($element in $labelNames){ New-ComplianceTag -Name $element }
  ```

### <a name="publish-your-new-labels"></a><span data-ttu-id="0d6f7-148">Publier vos nouvelles étiquettes</span><span class="sxs-lookup"><span data-stu-id="0d6f7-148">Publish your new labels</span></span>

<span data-ttu-id="0d6f7-149">Ensuite, procédez comme suit pour publier les nouvelles étiquettes Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-149">Next, use these steps to publish the new Office 365 labels.</span></span>
  
1. <span data-ttu-id="0d6f7-150">Dans le volet Office **Accueil > Étiquettes** du Centre de sécurité et conformité, cliquez sur l’onglet **Rétention**, puis sur &amp;**Publier les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-150">From the **Home > Labels** pane of the Security &amp; Compliance Center, click the **Retention** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="0d6f7-151">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-151">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="0d6f7-152">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-152">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
4. <span data-ttu-id="0d6f7-153">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-153">Click **Done**.</span></span>
    
5. <span data-ttu-id="0d6f7-154">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-154">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="0d6f7-155">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-155">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="0d6f7-156">Dans le volet **Nom de votre stratégie**, entrez un nom pour désigner l’ensemble des étiquettes dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-156">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="0d6f7-157">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-157">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-office-365-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="0d6f7-158">Phase 3 : Appliquer les étiquettes Office 365 à vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d6f7-158">Phase 3: Apply the Office 365 labels to your SharePoint Online sites</span></span>

<span data-ttu-id="0d6f7-159">Utilisez ces étapes pour appliquer les étiquettes Office 365 aux dossiers de documents de vos sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-159">Use these steps to apply the Office 365 labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="0d6f7-160">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-160">From the **Microsoft Office Home** tab of your browser, click the **SharePoint** tile.</span></span>
    
2. <span data-ttu-id="0d6f7-161">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur un site auquel vous devez affecter une étiquette Office 365.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-161">On the new **SharePoint** tab in your browser, click a site that needs an Office 365 label assigned.</span></span>
    
3. <span data-ttu-id="0d6f7-162">Sous le nouvel onglet du Site SharePoint de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-162">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="0d6f7-163">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-163">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="0d6f7-164">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-164">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="0d6f7-165">Dans **Paramètres-Appliquer une étiquette**, sélectionnez l’étiquette de votre choix, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-165">In **Settings-Apply Label**, select the appropriate label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="0d6f7-166">Fermez l’onglet du site SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-166">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="0d6f7-167">Répétez les étapes 3 à 8 pour affecter des étiquettes Office 365 à vos autres sites SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-167">Repeat steps 3-8 to assign Office 365 labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="0d6f7-168">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-168">Here is your resulting configuration.</span></span>
  
![Étiquettes Office 365 pour les quatre types de sites d’équipe SharePoint Online.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="0d6f7-170">Stratégies de protection contre la perte de données pour vos sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d6f7-170">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="0d6f7-171">Suivez ces étapes pour configurer une stratégie DLP qui avertit les utilisateurs lorsqu’ils partagent un document sur un site d’équipe sensible SharePoint Online externe à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-171">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="0d6f7-172">Sous l’onglet **Accueil Microsoft Office**, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-172">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="0d6f7-173">Sous le nouvel onglet **Centre d’administration Office** de votre navigateur, cliquez sur **Centres d’administration > Sécurité &amp; conformité**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-173">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
3. <span data-ttu-id="0d6f7-174">Sous le nouvel onglet **Sécurité &amp; conformité** de votre navigateur, cliquez sur **Protection contre la perte de données > Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-174">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
4. <span data-ttu-id="0d6f7-175">Dans le volet **Protection contre la perte de données**, cliquez sur **+ Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-175">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
5. <span data-ttu-id="0d6f7-176">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-176">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="0d6f7-177">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-177">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="0d6f7-178">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-178">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="0d6f7-179">Dans la liste des emplacements, désactivez les emplacements **Messagerie Exchange** et **Comptes OneDrive**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-179">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="0d6f7-180">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-180">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="0d6f7-181">Dans le volet**Choisir les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone de liste déroulante, puis cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-181">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="0d6f7-182">Dans le volet **Étiquettes**, cliquez sur **+ Ajouter**, sélectionnez l’étiquette **Sensible**, cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-182">In the **Labels** pane, click **+ Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="0d6f7-183">Dans le volet**Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-183">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="0d6f7-184">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-184">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="0d6f7-185">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-185">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="0d6f7-186">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-186">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="0d6f7-187">Dans la zone de texte, saisissez ou collez l’un des conseils suivants, selon si vous avez implémenté Azure Information Protection pour protéger les fichiers hautement confidentiels :</span><span class="sxs-lookup"><span data-stu-id="0d6f7-187">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="0d6f7-p106">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="0d6f7-p107">Les fichiers hautement confidentiels sont protégés par chiffrement. Seuls les utilisateurs externes qui y ont été autorisés par votre service informatique peuvent lire ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="0d6f7-193">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-193">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="0d6f7-194">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-194">Click **OK**.</span></span>
    
17. <span data-ttu-id="0d6f7-195">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-195">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
18. <span data-ttu-id="0d6f7-196">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-196">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="0d6f7-197">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-197">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="0d6f7-198">Voici le résultat de votre configuration pour les sites d’équipe SharePoint Online sensibles.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-198">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![Stratégie DLP pour un site d’équipe SharePoint Online isolé utilisant l’étiquette Office 365 Données sensibles.](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="0d6f7-200">Utilisez ces étapes pour configurer une stratégie de protection contre la perte de données qui bloque les utilisateurs quand ils partagent un document sur un site d’équipe SharePoint Online hautement confidentiel à l’extérieur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-200">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="0d6f7-201">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Sécurité &amp; conformité**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-201">From the **Microsoft Office Home** tab in your browser, click the **Security &amp; Compliance** tile.</span></span>
    
2. <span data-ttu-id="0d6f7-202">Sous le nouvel onglet **Sécurité &amp; conformité** de votre navigateur, cliquez sur **Protection contre la perte de données > Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-202">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
3. <span data-ttu-id="0d6f7-203">Dans le volet **Protection contre la perte de données**, cliquez sur **+ Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-203">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
4. <span data-ttu-id="0d6f7-204">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-204">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="0d6f7-205">Dans le volet **Nom de votre stratégie**, entrez le nom de la stratégie DLP hautement sensible dans **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-205">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="0d6f7-206">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-206">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="0d6f7-207">Dans la liste des emplacements, désactivez les emplacements **Messagerie Exchange** et **Comptes OneDrive**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-207">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="0d6f7-208">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-208">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="0d6f7-209">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone de liste déroulante, puis cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-209">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="0d6f7-210">Dans le volet **Étiquettes**, cliquez sur **+ Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, cliquez sur **Ajouter**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-210">In the **Labels** pane, click **+ Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="0d6f7-211">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-211">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="0d6f7-212">Dans le volet **Personnaliser les types d’informations sensibles que vous voulez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-212">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="0d6f7-213">Dans le volet **Que voulez-vous faire si nous détectons des informations confidentielles ?**, cliquez sur **Personnaliser l’info-bulle et la messagerie électronique**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-213">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="0d6f7-214">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-214">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="0d6f7-215">Dans la zone de texte, tapez ou collez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0d6f7-215">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="0d6f7-p108">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="0d6f7-219">Vous pouvez également saisir ou coller votre propre conseil de stratégie pour expliquer aux utilisateurs comment partager un fichier en dehors de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-219">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="0d6f7-220">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-220">Click **OK**.</span></span>
    
17. <span data-ttu-id="0d6f7-221">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-221">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
18. <span data-ttu-id="0d6f7-222">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-222">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="0d6f7-223">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-223">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="0d6f7-224">Voici le résultat de votre configuration pour les sites d’équipe SharePoint Online hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="0d6f7-224">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![Stratégie DLP pour un site d’équipe SharePoint Online isolé utilisant l’étiquette Office 365 Hautement confidentiel.](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="0d6f7-226">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0d6f7-226">Next step</span></span>

[<span data-ttu-id="0d6f7-227">Protéger les fichiers SharePoint Online avec Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="0d6f7-227">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="0d6f7-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d6f7-228">See Also</span></span>

[<span data-ttu-id="0d6f7-229">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0d6f7-229">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="0d6f7-230">Sécuriser les sites SharePoint Online dans un environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="0d6f7-230">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="0d6f7-231">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="0d6f7-231">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="0d6f7-232">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="0d6f7-232">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


