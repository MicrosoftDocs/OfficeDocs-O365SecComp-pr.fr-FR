---
title: Sécuriser des sites SharePoint Online dans un environnement de développement et de test
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 06/18/2019
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 06af70f3-e7dc-4ee2-a385-fb4d61a5e93b
description: 'Résumé : Créez des sites d’équipe SharePoint Online publics, privés, sensibles et hautement confidentiels dans un environnement de développement/test.'
ms.openlocfilehash: 148db19c8902735829a5849901723b5f2f200b74
ms.sourcegitcommit: 3ffd188a7fd547ae343ccf14361c1e4300f88de0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2019
ms.locfileid: "35059542"
---
# <a name="secure-sharepoint-online-sites-in-a-devtest-environment"></a><span data-ttu-id="60507-103">Sécuriser des sites SharePoint Online dans un environnement de développement et de test</span><span class="sxs-lookup"><span data-stu-id="60507-103">Secure SharePoint Online sites in a dev/test environment</span></span>

 <span data-ttu-id="60507-104">**Résumé :** Créez des sites d’équipe SharePoint Online publics, privés, sensibles et hautement confidentiels dans un environnement de développement/test.</span><span class="sxs-lookup"><span data-stu-id="60507-104">**Summary:** Create public, private, sensitive, and highly confidential SharePoint Online team sites in a dev/test environment.</span></span>
  
<span data-ttu-id="60507-105">Cet article fournit des instructions pas à pas pour créer un environnement de développement et de test qui inclut les quatre types différents de sites d’équipe SharePoint Online pour la solution de [sécurisation des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="60507-105">This article provides step-by-step instructions to create a dev/test environment that includes the four different types of SharePoint Online team sites for the [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md) solution.</span></span>
  
![Les quatre sites d’équipe dans l’environnement de développement/test SharePoint Online sécurisé.](media/b0fea489-359c-4c85-a0ad-e4efb4a1e47f.png)
  
<span data-ttu-id="60507-107">Utilisez cet environnement de développement/test pour expérimenter les comportements de protection des informations et optimiser les paramètres en fonction de vos besoins avant de déployer des sites d’équipe SharePoint Online en production.</span><span class="sxs-lookup"><span data-stu-id="60507-107">Use this dev/test environment to experiment with the information protection behaviors and fine-tune settings for your specific needs before deploying SharePoint Online team sites in production.</span></span>
  
## <a name="phase-1-create-your-devtest-environment"></a><span data-ttu-id="60507-108">Phase 1 : Créer votre environnement de développement et de test</span><span class="sxs-lookup"><span data-stu-id="60507-108">Phase 1: Create your dev/test environment</span></span>

<span data-ttu-id="60507-109">Dans cette phase, vous obtenez des abonnements d’évaluation pour Office 365 et Enterprise Mobility + Security (EMS) pour une organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="60507-109">In this phase, you obtain trial subscriptions for Office 365 and Enterprise Mobility + Security (EMS) for a fictional organization.</span></span>
  
<span data-ttu-id="60507-110">Suivez d’abord les instructions de la **Phase 2** de l’[environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span><span class="sxs-lookup"><span data-stu-id="60507-110">First, follow the instructions in **Phase 2** of the [Office 365 dev/test environment](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).</span></span>
  
<span data-ttu-id="60507-111">Ensuite, inscrivez-vous à l’abonnement d’évaluation EMS et ajoutez-le à la même organisation que votre abonnement d’évaluation Office 365.</span><span class="sxs-lookup"><span data-stu-id="60507-111">Next, sign up for the EMS trial subscription and add it to the same organization as your Office 365 trial subscription.</span></span>
  
1. <span data-ttu-id="60507-112">Si nécessaire, connectez-vous au[Centre d’administration Microsoft 365](https://admin.microsoft.com) avec les identifiants du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-112">If needed, sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="60507-113">Dans le volet de navigation de gauche, cliquez sur **Facturation > Acheter des services**.</span><span class="sxs-lookup"><span data-stu-id="60507-113">In the left navigation, click **Billing > Purchase services**.</span></span>
    
3. <span data-ttu-id="60507-p101">Dans la page **Acheter des services**, recherchez l’élément **Enterprise Mobility + Security E5**. Pointez votre souris dessus et cliquez sur **Démarrer l’essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="60507-p101">On the **Purchase services** page, find the **Enterprise Mobility + Security E5** item. Hover your mouse pointer over it and click **Start free trial**.</span></span>
    
4. <span data-ttu-id="60507-116">Dans la page **Confirmer votre commande**, cliquez sur **Essayer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="60507-116">On the **Confirm your order** page, click **Try now**.</span></span>
    
5. <span data-ttu-id="60507-117">Dans la page **Réception de la commande**, cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="60507-117">On the **Order receipt** page, click **Continue**.</span></span>
    
<span data-ttu-id="60507-118">Ensuite, activez la licence Enterprise Mobility + Security E5 pour votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="60507-118">Next, enable the Enterprise Mobility + Security E5 license for your global administrator account.</span></span>
  
1. <span data-ttu-id="60507-119">Sous l’onglet **Centre d’administration Microsoft 365** de votre navigateur, dans le volet de navigation gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="60507-119">On the **Microsoft 365 admin center** tab in your browser, in the left navigation, click **Users > Active users**.</span></span>
    
2. <span data-ttu-id="60507-120">Cliquez sur votre compte Administrateur général, puis cliquez sur **Modifier** pour les **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="60507-120">Click your global administrator account, and then click **Edit** for **Product licenses**.</span></span>
    
3. <span data-ttu-id="60507-121">Dans le volet **Licences de produit**, activez la licence de produit pour **Enterprise Mobility + Security E5** en sélectionnant **Activer**, cliquez sur **Enregistrer**, cliquez deux fois sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="60507-121">On the **Product licenses** pane, turn the product license for **Enterprise Mobility + Security E5** to **On**, click **Save,** and then click **Close** twice.</span></span>
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups-and-users"></a><span data-ttu-id="60507-122">Phase 2 : Création et configuration de vos groupes et utilisateurs Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="60507-122">Phase 2: Create and configure your Azure Active Directory (AD) groups and users</span></span>

<span data-ttu-id="60507-123">Dans cette phase, vous créez et vous configurez les groupes et les utilisateurs Azure AD de votre organisation fictive.</span><span class="sxs-lookup"><span data-stu-id="60507-123">In this phase, you create and configure the Azure AD groups and users for your fictional organization.</span></span>
  
<span data-ttu-id="60507-124">Commencez par créer un ensemble de groupes pour une organisation standard avec le portail Azure.</span><span class="sxs-lookup"><span data-stu-id="60507-124">First, create a set of groups for a typical organization with the Azure portal.</span></span>
  
1. <span data-ttu-id="60507-p102">Créez un onglet distinct dans votre navigateur, puis accédez au portail Azure à l’adresse [https://portal.azure.com](https://portal.azure.com). Si nécessaire, connectez-vous avec les informations d’identification du compte Administrateur général de votre abonnement d’essai Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="60507-p102">Create a separate tab in your browser, and then go to the Azure portal at [https://portal.azure.com](https://portal.azure.com). If needed, sign in with the credentials of the global administrator account for your Office 365 E5 trial subscription.</span></span>
    
2. <span data-ttu-id="60507-127">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes**.</span><span class="sxs-lookup"><span data-stu-id="60507-127">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="60507-128">Dans le panneau **Groupes - Tous les groupes**, cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="60507-128">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="60507-129">Dans le panneau **Groupe** :</span><span class="sxs-lookup"><span data-stu-id="60507-129">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="60507-130">Sélectionnez **Office 365** dans **Type de groupe**.</span><span class="sxs-lookup"><span data-stu-id="60507-130">Select **Office 365** in **Group type**.</span></span>
    
  - <span data-ttu-id="60507-131">Tapez **C-Suite** dans le champ **Nom**.</span><span class="sxs-lookup"><span data-stu-id="60507-131">Type **C-Suite** in **Name**.</span></span>
    
  - <span data-ttu-id="60507-132">Sélectionnez **Affecté** dans le champ **Type d’appartenance**.</span><span class="sxs-lookup"><span data-stu-id="60507-132">Select **Assigned** in **Membership type**.</span></span>
      
5. <span data-ttu-id="60507-133">Cliquez sur **Créer** et fermez le panneau **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="60507-133">Click **Create**, and then close the **Group** blade.</span></span>
    
6. <span data-ttu-id="60507-134">Répétez les étapes 3 à 5 pour les noms de groupe suivants :</span><span class="sxs-lookup"><span data-stu-id="60507-134">Repeat steps 3-5 for the following group names:</span></span>
    
  - <span data-ttu-id="60507-135">Équipe Informatique</span><span class="sxs-lookup"><span data-stu-id="60507-135">IT staff</span></span>
    
  - <span data-ttu-id="60507-136">Équipe Recherche</span><span class="sxs-lookup"><span data-stu-id="60507-136">Research staff</span></span>
    
  - <span data-ttu-id="60507-137">Équipe Standard</span><span class="sxs-lookup"><span data-stu-id="60507-137">Regular staff</span></span>
    
  - <span data-ttu-id="60507-138">Équipe Marketing</span><span class="sxs-lookup"><span data-stu-id="60507-138">Marketing staff</span></span>
    
  - <span data-ttu-id="60507-139">Équipe Ventes</span><span class="sxs-lookup"><span data-stu-id="60507-139">Sales staff</span></span>
    
7. <span data-ttu-id="60507-140">Gardez l’onglet du portail Azure ouvert dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="60507-140">Keep the Azure portal tab in your browser open.</span></span>
    
<span data-ttu-id="60507-141">Ensuite, configurez l’octroi de licence automatique afin que des licences soient automatiquement attribuées aux membres de vos groupes pour les abonnements Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="60507-141">Next, you configure automatic licensing so that members of your groups are automatically assigned licenses for your Office 365 and EMS subscriptions.</span></span>
  
1. <span data-ttu-id="60507-142">Dans le portail Azure, cliquez sur **Azure Active Directory > Licences > Tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="60507-142">In the Azure portal, click **Azure Active Directory > Licenses > All products**.</span></span>
    
2. <span data-ttu-id="60507-143">Dans la liste, sélectionnez **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5**, puis cliquez sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="60507-143">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **Assign**.</span></span>
    
3. <span data-ttu-id="60507-144">Dans le panneau **Affecter une licence**, cliquez sur **Utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="60507-144">In the **Assign license** blade, click **Users and groups**.</span></span>
    
4. <span data-ttu-id="60507-145">Dans la liste des groupes, sélectionnez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="60507-145">In the list of groups, select the following:</span></span>
    
  - <span data-ttu-id="60507-146">C-Suite</span><span class="sxs-lookup"><span data-stu-id="60507-146">C-Suite</span></span>
    
  - <span data-ttu-id="60507-147">Équipe Informatique</span><span class="sxs-lookup"><span data-stu-id="60507-147">IT staff</span></span>
    
  - <span data-ttu-id="60507-148">Équipe Recherche</span><span class="sxs-lookup"><span data-stu-id="60507-148">Research staff</span></span>
    
  - <span data-ttu-id="60507-149">Équipe Standard</span><span class="sxs-lookup"><span data-stu-id="60507-149">Regular staff</span></span>
    
  - <span data-ttu-id="60507-150">Équipe Marketing</span><span class="sxs-lookup"><span data-stu-id="60507-150">Marketing staff</span></span>
    
  - <span data-ttu-id="60507-151">Équipe de vente</span><span class="sxs-lookup"><span data-stu-id="60507-151">Sales staff</span></span>
    
5. <span data-ttu-id="60507-152">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="60507-152">Click **Select**, and then click **Assign**.</span></span>
    
6. <span data-ttu-id="60507-153">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="60507-153">Close the Azure portal tab in your browser.</span></span>
    
<span data-ttu-id="60507-154">Ensuite, [connectez -vous au module PowerShell Azure Active Directory pour le module Graphique](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="60507-154">Next, you [Connect with the Azure Active Directory PowerShell for Graph module ](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="60507-155">Renseignez le nom de votre organisation, votre emplacement et un mot de passe commun, puis exécutez les commandes suivantes à partir de l’invite de commandes PowerShell ou de l’environnement de script intégré (ISE) pour créer des comptes d’utilisateur et les ajouter à leurs groupes :</span><span class="sxs-lookup"><span data-stu-id="60507-155">Fill in your organization name, your location, and a common password, and then run these commands from the PowerShell command prompt or Integrated Script Environment (ISE) to create user accounts and add them to their groups:</span></span>
  
```
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$groupName="C-Suite"
$userNames=@("CEO","CFO","CIO") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Research staff"
$userNames=@("Researcher1") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Regular staff"
$userNames=@("Regular1", "Regular2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Marketing staff"
$userNames=@("Marketing1", "Marketing2") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
$groupName="Sales staff"
$userNames=@("SalesPerson1") 
$groupID=(Get-AzureADGroup | Where { $_.DisplayName -eq $groupName }).ObjectID
ForEach ($element in $userNames){ 
New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -UsageLocation $location 
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $element }).ObjectID -ObjectId $groupID
}
```

> [!NOTE]
> <span data-ttu-id="60507-156">L’utilisation ici d’un mot de passe courant est pour l’automatisation et la simplicité de configuration pour un environnement de développement et de test.</span><span class="sxs-lookup"><span data-stu-id="60507-156">The use of a common password here is for automation and ease of configuration for a dev/test environment.</span></span> <span data-ttu-id="60507-157">Bien évidemment, cela est hautement déconseillé pour les abonnements de production.</span><span class="sxs-lookup"><span data-stu-id="60507-157">Obviously, this is highly discouraged for production subscriptions.</span></span> 
  
<span data-ttu-id="60507-158">Utilisez ces étapes pour vérifier que la gestion des licences basée sur un groupe fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="60507-158">Use these steps to verify that group-based licensing is working correctly.</span></span>
  
1. <span data-ttu-id="60507-159">Sous l’onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur la vignette **Administration**.</span><span class="sxs-lookup"><span data-stu-id="60507-159">From the **Microsoft Office Home** tab of your browser, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="60507-160">Sous le nouvel onglet **Centre d’administration Office** de votre navigateur, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="60507-160">From the new **Office Admin center** tab of your browser, click **Users**.</span></span>
    
3. <span data-ttu-id="60507-161">Dans la liste des utilisateurs, cliquez sur **PDG**.</span><span class="sxs-lookup"><span data-stu-id="60507-161">In the list of users, click **CEO**.</span></span>
    
4. <span data-ttu-id="60507-162">Dans le volet qui affiche les propriétés du compte d’utilisateur **PDG**, vérifiez que les licences **Enterprise Mobility + Security E5** et **Office 365 Enterprise E5** lui ont été affectées (dans **Licences de produit**).</span><span class="sxs-lookup"><span data-stu-id="60507-162">In the pane that lists the properties of the **CEO** user account, verify that it has been assigned the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses (in **Product licenses**).</span></span>
    
## <a name="phase-3-create-office-365-retention-labels"></a><span data-ttu-id="60507-163">Phase 3: Créer des étiquettes de rétention Office 365</span><span class="sxs-lookup"><span data-stu-id="60507-163">Phase 3: Create Office 365 retention labels</span></span>

<span data-ttu-id="60507-164">Dans cette phase, vous allez créer les étiquettes correspondant aux différents niveaux de sécurité pour les dossiers de documents du site d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="60507-164">In this phase, you create the retention labels for the different levels of security for SharePoint Online team site documents folders.</span></span>


1. <span data-ttu-id="60507-165">Se connecter au[portail de conformité de Microsoft 365](https://compliance.microsoft.com) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="60507-165">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com) with your global admin account.</span></span>
    
2. <span data-ttu-id="60507-166">Sous l’onglet **Accueil- Conformité Microsoft 365** de votre navigateur, cliquez sur **Classifications > Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="60507-166">From the **Home - Microsoft 365 compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
3. <span data-ttu-id="60507-167">Cliquez sur **Étiquettes de rétention > Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="60507-167">Click **Retention labels > Create a label**.</span></span>
    
4. <span data-ttu-id="60507-168">Dans le volet**Nommer votre étiquette**, saisissez**Public Interne**dans**Nommer votre étiquette**, puis cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-168">On the **Name your label** pane, type **Internal Public** in **Name your label**, and then click **Next**.</span></span>

5. <span data-ttu-id="60507-169">Sur le volet**descripteurs de plan fichier**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-169">On the **File plan descriptors** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="60507-170">Dans le volet**Paramètres d’étiquette**, définissez, si nécessaire, la**Rétention** sur **Activé** puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-170">On the **Label settings** pane, if needed, set **Retention** to **On**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="60507-171">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="60507-171">On the **Review your settings** pane, click **Create the label**.</span></span>
    
8. <span data-ttu-id="60507-172">Répétez les étapes 3 à 7 pour les étiquettes supplémentaires avec ces noms :</span><span class="sxs-lookup"><span data-stu-id="60507-172">Repeat steps 3-7 for additional labels with these names:</span></span>
    
  - <span data-ttu-id="60507-173">Private</span><span class="sxs-lookup"><span data-stu-id="60507-173">Private</span></span>
    
  - <span data-ttu-id="60507-174">Sensible</span><span class="sxs-lookup"><span data-stu-id="60507-174">Sensitive</span></span>
    
  - <span data-ttu-id="60507-175">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="60507-175">Highly Confidential</span></span>
  
9. <span data-ttu-id="60507-176">Dans le volet **Accueil > Étiquettes**, cliquez sur **Publier des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="60507-176">From the **Home > Labels** pane, click **Publish labels**.</span></span>
    
10. <span data-ttu-id="60507-177">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Choisir les étiquettes à publier**.</span><span class="sxs-lookup"><span data-stu-id="60507-177">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
11. <span data-ttu-id="60507-178">Dans le volet **Choisir des étiquettes**, cliquez sur **Ajouter** et sélectionnez les quatre étiquettes.</span><span class="sxs-lookup"><span data-stu-id="60507-178">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
12. <span data-ttu-id="60507-179">Cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="60507-179">Click **Done**.</span></span>
    
13. <span data-ttu-id="60507-180">Dans le volet **Choisir les étiquettes à publier**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-180">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
14. <span data-ttu-id="60507-181">Dans le volet **Choisir les emplacements**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-181">On the **Choose locations** pane, click **Next**.</span></span>
    
15. <span data-ttu-id="60507-182">Dans le volet **Nom de votre stratégie**, saisissez **Exemple d’organisation** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-182">On the **Name your policy** pane, type **Example organization** in **Name**, and then click **Next**.</span></span>
    
16. <span data-ttu-id="60507-183">Dans le volet **Vérifier vos paramètres**, cliquez sur **Publier les étiquettes**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="60507-183">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>
    
## <a name="phase-4-create-your-sharepoint-online-team-sites"></a><span data-ttu-id="60507-184">Phase 4 : Création de vos sites d’équipe SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="60507-184">Phase 4: Create your SharePoint Online team sites</span></span>

<span data-ttu-id="60507-185">Dans cette phase, vous créez et vous configurez les quatre types de sites d’équipe SharePoint Online pour votre exemple d’organisation.</span><span class="sxs-lookup"><span data-stu-id="60507-185">In this phase, you create and configure the four types of SharePoint Online team sites for your example organization.</span></span>
  
### <a name="organization-wide-team-site"></a><span data-ttu-id="60507-186">Site d’équipe au niveau de l’organisation</span><span class="sxs-lookup"><span data-stu-id="60507-186">Organization wide team site</span></span>

<span data-ttu-id="60507-187">Pour créer une base de référence de site d’équipe SharePoint Online public, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="60507-187">To create a baseline public SharePoint Online team site, do the following:</span></span>
  
1. <span data-ttu-id="60507-188">Si nécessaire, connectez-vous au[portail Office 365](https://portal.office.com) avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-188">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="60507-189">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="60507-189">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="60507-190">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="60507-190">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="60507-191">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="60507-191">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="60507-192">Dans **Nom du site**, tapez **Toute l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="60507-192">In **Site name**, type **Organization wide**.</span></span> 
    
6. <span data-ttu-id="60507-193">Dans **Description du site d’équipe**, tapez **Site SharePoint pour toute l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="60507-193">In **Team site description**, type **SharePoint site for the entire organization**.</span></span>
    
7. <span data-ttu-id="60507-194">Dans **Paramètres de confidentialité**, sélectionnez **Public - tout le monde dans l’organisation peut accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-194">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-195">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="60507-195">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="60507-196">Ensuite, configurez le dossier des documents du site d’équipe Toute l’organisation pour l’étiquette Publique interne.</span><span class="sxs-lookup"><span data-stu-id="60507-196">Next, configure the documents folder of the Organization wide team site for the Internal Public label.</span></span>
  
1. <span data-ttu-id="60507-197">Sous l’onglet **Toute l’organisation - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="60507-197">In the **Organization wide-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="60507-198">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-198">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="60507-199">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-199">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="60507-200">Dans **Paramètres - Appliquer une étiquette**, sélectionnez **Interne public**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-200">In **Settings-Apply Label**, select **Internal Public**, and then click **Save**.</span></span>
    
### <a name="project-1-team-site"></a><span data-ttu-id="60507-201">Site d’équipe Projet 1</span><span class="sxs-lookup"><span data-stu-id="60507-201">Project 1 team site</span></span>

<span data-ttu-id="60507-202">Pour créer un site d’équipe SharePoint Online privé de base de référence pour un projet au sein de l’organisation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="60507-202">To create a baseline private SharePoint Online team site for a project within the organization, do the following:</span></span>
  
1. <span data-ttu-id="60507-203">Si nécessaire, connectez-vous au[portail Office 365](https://portal.office.com) avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-203">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="60507-204">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="60507-204">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="60507-205">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="60507-205">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="60507-206">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="60507-206">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="60507-207">Dans **Nom du site**, tapez **Projet 1**.</span><span class="sxs-lookup"><span data-stu-id="60507-207">In **Site name**, type **Project 1**.</span></span> 
    
6. <span data-ttu-id="60507-208">Dans **Description du site d’équipe**, tapez **Site SharePoint pour Projet 1**.</span><span class="sxs-lookup"><span data-stu-id="60507-208">In **Team site description,** type **SharePoint site for Project 1**.</span></span>
    
7. <span data-ttu-id="60507-209">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-209">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-210">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="60507-210">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="60507-211">Ensuite, configurez le dossier des documents du site d’équipe Projet 1 pour l’étiquette Privé.</span><span class="sxs-lookup"><span data-stu-id="60507-211">Next, configure the documents folder of the Project 1 team site for the Private label.</span></span>
  
1. <span data-ttu-id="60507-212">Sous l’onglet **Projet 1 - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="60507-212">In the **Project 1-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="60507-213">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-213">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="60507-214">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-214">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="60507-215">Dans **Paramètres - Appliquer une étiquette**, sélectionnez **Privé**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-215">In **Settings-Apply Label**, select **Private**, and then click **Save**.</span></span>
    
### <a name="marketing-campaigns-team-site"></a><span data-ttu-id="60507-216">Site d’équipe des campagnes marketing</span><span class="sxs-lookup"><span data-stu-id="60507-216">Marketing campaigns team site</span></span>

<span data-ttu-id="60507-217">Pour créer un site d’équipe SharePoint Online isolé de niveau sensible pour les ressources des campagnes marketing, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="60507-217">To create a sensitive-level isolated SharePoint Online team site for marketing campaign resources, do the following:</span></span>

 
1. <span data-ttu-id="60507-218">Si nécessaire, connectez-vous au[portail Office 365](https://portal.office.com) avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-218">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="60507-219">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="60507-219">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="60507-220">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="60507-220">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="60507-221">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="60507-221">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="60507-222">Dans **Nom du site d’équipe**, tapez **Campagnes marketing**.</span><span class="sxs-lookup"><span data-stu-id="60507-222">In **Team site name**, type **Marketing campaigns**.</span></span>
    
6. <span data-ttu-id="60507-223">Dans **Description du site d’équipe**, tapez **Site SharePoint pour les ressources des campagnes marketing (sensible)**.</span><span class="sxs-lookup"><span data-stu-id="60507-223">In **Team site description**, type **SharePoint site for marketing campaign resources (sensitive)**.</span></span>
    
7.  <span data-ttu-id="60507-224">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-224">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-225">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="60507-225">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
9. <span data-ttu-id="60507-226">Dans le nouvel onglet **Campagnes marketing** de votre navigateur, cliquez sur l’icône des paramètres dans la barre d’outils, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="60507-226">On the new **Marketing campaigns** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
10. <span data-ttu-id="60507-227">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="60507-227">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
11. <span data-ttu-id="60507-228">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="60507-228">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>
    
12. <span data-ttu-id="60507-229">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site, ainsi que des fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site**, saisissez **ITAdmin1@**\<nom de votre organisation>**.onmicrosoft.com** dans le champ **Envoyer toutes les demandes d’accès à**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-229">In the **Access Request Settings** dialog box, clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes, type **ITAdmin1@**\<your organization name>**.onmicrosoft.com** in **Send all requests for access**, and then click **OK**.</span></span>
    
13. <span data-ttu-id="60507-230">Cliquez sur **Membres de Campagnes marketing** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="60507-230">Click **Marketing campaigns Members** in the list.</span></span>
    
14. <span data-ttu-id="60507-231">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="60507-231">On the **People and Groups** page, click **New**.</span></span>
    
15. <span data-ttu-id="60507-232">Dans la boîte de dialogue **Partager**, saisissez **Personnel marketing**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="60507-232">In the **Share** dialog box, type **Marketing staff**, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="60507-233">Répétez les étapes 14 et 15 pour le compte utilisateur **Researcher1**.</span><span class="sxs-lookup"><span data-stu-id="60507-233">Repeat steps 14 and 15 for the **Researcher1** user account.</span></span>
    
17. <span data-ttu-id="60507-234">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="60507-234">Click the back button on your browser.</span></span>
    
18. <span data-ttu-id="60507-235">Cliquez sur **Propriétaires de campagnes marketing** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="60507-235">Click **Marketing campaigns Owners** in the list.</span></span>
    
19. <span data-ttu-id="60507-236">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="60507-236">On the **People and Groups** page, click **New**.</span></span>
    
20. <span data-ttu-id="60507-237">Dans la boîte de dialogue **Partager**, saisissez **Équipe informatique**, sélectionnez-la, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="60507-237">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>
    
21. <span data-ttu-id="60507-238">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="60507-238">Click the back button on your browser.</span></span>
    
22. <span data-ttu-id="60507-239">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **Campagnes marketing - Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="60507-239">Close the **People and Groups** tab in your browser, click the **Marketing campaigns-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="60507-240">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="60507-240">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="60507-241">Le groupe SharePoint **Campagnes marketing - Membres** contient seulement le groupe **Campagnes marketing** (qui contient le compte d’utilisateur Administrateur global), le groupe **Équipe Marketing** (qui contient les comptes d’utilisateur Marketing1 et Marketing2) et le compte d’utilisateur **Chercheur1**.</span><span class="sxs-lookup"><span data-stu-id="60507-241">The **Marketing campaigns-Members** SharePoint group contains only the **Marketing campaigns** group (which contains the global administrator user account), the **Marketing staff** group (which contains the Marketing1 and Marketing2 user accounts), and the **Researcher1** user account.</span></span>
    
- <span data-ttu-id="60507-242">Le groupe SharePoint **Campagnes marketing - Propriétaires** contient seulement le groupe **Équipe Informatique** (qui contient seulement les comptes d’utilisateur ITAdmin1 et ITAdmin2).</span><span class="sxs-lookup"><span data-stu-id="60507-242">The **Marketing campaigns-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>
    
- <span data-ttu-id="60507-243">Le groupe SharePoint **Campagnes marketing - Visiteurs** ne contient aucun groupe ni compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60507-243">The **Marketing campaigns-Visitors** SharePoint group contains no groups or user accounts.</span></span>
    
- <span data-ttu-id="60507-244">Les membres ne peuvent pas modifier les autorisations au niveau du site (ceci peut être fait seulement par les membres du groupe **Campagnes marketing - Propriétaires**).</span><span class="sxs-lookup"><span data-stu-id="60507-244">Members cannot modify site-level permissions (this can only be done by members of the **Marketing campaigns-Owners** group).</span></span>
    
- <span data-ttu-id="60507-245">Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, mais peuvent demander d’avoir accès au site. Un courrier électronique sera envoyé à la boîte aux lettres du compte d’utilisateur ITAdmin1.</span><span class="sxs-lookup"><span data-stu-id="60507-245">Other user accounts cannot access the site or its resources, but can request access to the site, which will send an email to the ITAdmin1 user account mailbox.</span></span>
    
<span data-ttu-id="60507-246">Ensuite, configurez le dossier de documents du site d’équipe Campagnes marketing pour l’étiquette Sensible.</span><span class="sxs-lookup"><span data-stu-id="60507-246">Next, configure the documents folder of the Marketing campaigns team site for the Sensitive label.</span></span>
  
1. <span data-ttu-id="60507-247">Sous l’onglet **Campagne marketing - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="60507-247">In the **Marketing campaigns-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="60507-248">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-248">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="60507-249">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-249">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="60507-250">Dans **Paramètres - Appliquer l’étiquette**, sélectionnez **Sensible**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-250">In **Settings-Apply Label**, select **Sensitive**, and then click **Save**.</span></span>
    
<span data-ttu-id="60507-251">Ensuite, configurez une stratégie de protection contre la perte de données qui avertit les utilisateurs quand ils partagent un document à l’extérieur de l’organisation sur un site d’équipe SharePoint Online avec l’étiquette Sensible, qui inclut le site Campagnes marketing.</span><span class="sxs-lookup"><span data-stu-id="60507-251">Next, configure a data loss prevention (DLP) policy that notifies users when they share a document on a SharePoint Online team site with the Sensitive label, which includes the Marketing campaigns site, outside the organization.</span></span>

1. <span data-ttu-id="60507-252">Se connecter au[portail de conformité de Microsoft 365](https://compliance.microsoft.com/) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="60507-252">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with your global admin account.</span></span>
    
2. <span data-ttu-id="60507-253">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="60507-253">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="60507-254">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="60507-254">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="60507-255">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-255">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="60507-256">Dans le volet **Nom de votre stratégie**, saisissez les **sites d’équipe SharePoint Online avec étiquette Sensible** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-256">In the **Name your policy** pane, type **Sensitive label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="60507-257">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-257">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="60507-258">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-258">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-259">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="60507-259">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="60507-260">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="60507-260">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="60507-261">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Sensible**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="60507-261">In the **Retention labels** pane, click **Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="60507-262">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-262">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="60507-263">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-263">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="60507-264">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="60507-264">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="60507-265">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="60507-265">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="60507-266">Dans la zone de texte, saisissez ou collez l’un des conseils suivants, selon si vous avez implémenté Azure Information Protection pour protéger les fichiers hautement confidentiels :</span><span class="sxs-lookup"><span data-stu-id="60507-266">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="60507-p104">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="60507-p104">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="60507-270">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-270">Click **OK**.</span></span>
    
17. <span data-ttu-id="60507-271">Dans le volet Office **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-271">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="60507-272">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-272">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="60507-273">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="60507-273">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
  
### <a name="company-strategy-team-site"></a><span data-ttu-id="60507-274">Site d’équipe Stratégie d’entreprise</span><span class="sxs-lookup"><span data-stu-id="60507-274">Company strategy team site</span></span>

<span data-ttu-id="60507-275">Pour créer un site d’équipe SharePoint Online isolé au niveau Hautement confidentiel pour les ressources d’entreprise stratégiques des dirigeants de l’organisation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="60507-275">To create an isolated SharePoint Online team site at the highly confidential level for strategic company resources of the chief executives of the organization, do the following:</span></span>
  
1. <span data-ttu-id="60507-276">Si nécessaire, connectez-vous au[portail Office 365](https://portal.office.com) avec les informations d’identification du compte d’administrateur général de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-276">If needed, sign in to the [Office 365 portal](https://portal.office.com) with the credentials of the global administrator account of your trial subscription.</span></span>
    
2. <span data-ttu-id="60507-277">Dans la liste des vignettes, cliquez sur **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="60507-277">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="60507-278">Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.</span><span class="sxs-lookup"><span data-stu-id="60507-278">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="60507-279">Dans la page **Créer un site**, cliquez sur **Site d’équipe**.</span><span class="sxs-lookup"><span data-stu-id="60507-279">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="60507-280">Dans **Nom du site d’équipe**, tapez **Stratégie de l’entreprise**.</span><span class="sxs-lookup"><span data-stu-id="60507-280">In **Team site name**, type **Company strategy**.</span></span>
    
6. <span data-ttu-id="60507-281">Dans **Description du site d’équipe**, tapez **Site SharePoint pour la stratégie de l’entreprise (Hautement confidentiel)**.</span><span class="sxs-lookup"><span data-stu-id="60507-281">In **Team site description**, type **SharePoint site for company strategy (highly confidential)**.</span></span>
    
7.  <span data-ttu-id="60507-282">Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-282">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-283">Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="60507-283">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
9. <span data-ttu-id="60507-284">Dans le nouvel onglet **Stratégie d’entreprise** de votre navigateur, cliquez sur l’icône des paramètres dans la barre d’outils, puis sur **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="60507-284">On the new **Company strategy** tab in your browser, in the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
10. <span data-ttu-id="60507-285">Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.</span><span class="sxs-lookup"><span data-stu-id="60507-285">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
11. <span data-ttu-id="60507-286">Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.</span><span class="sxs-lookup"><span data-stu-id="60507-286">In the new **Permissions** tab in your browser, click **Access Request Settings**.</span></span>
    
12. <span data-ttu-id="60507-287">Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les membres à inviter d’autres personnes sur le groupe de membres du site** (afin que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-287">In the **Access Request Settings** dialog box, clear **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
13. <span data-ttu-id="60507-288">Cliquez sur les **Membres de l’équipe Stratégie d’entreprise** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="60507-288">Click **Company strategy Members** in the list.</span></span>
    
14. <span data-ttu-id="60507-289">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="60507-289">On the **People and Groups** page, click **New**.</span></span>
    
15. <span data-ttu-id="60507-290">Dans la boîte de dialogue **Partager**, saisissez **C-Suite**, sélectionnez-le, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="60507-290">In the **Share** dialog box, type **C-Suite**, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="60507-291">Cliquez sur les **Propriétaires de la stratégie d’entreprise** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="60507-291">Click **Company strategy Owners** in the list.</span></span>
    
17. <span data-ttu-id="60507-292">Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="60507-292">On the **People and Groups** page, click **New**.</span></span>
    
18. <span data-ttu-id="60507-293">Dans la boîte de dialogue **Partager**, saisissez **Équipe informatique**, sélectionnez-la, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="60507-293">In the **Share** dialog box, type **IT staff**, select it, and then click **Share**.</span></span>
    
19. <span data-ttu-id="60507-294">Cliquez sur le bouton de retour de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="60507-294">Click the back button on your browser.</span></span>
    
20. <span data-ttu-id="60507-295">Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **Stratégie d’entreprise - Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.</span><span class="sxs-lookup"><span data-stu-id="60507-295">Close the **People and Groups** tab in your browser, click the **Company strategy-Home** tab in your browser, and then close the **Site permissions** pane.</span></span>
    
<span data-ttu-id="60507-296">Voici les résultats de la configuration des autorisations :</span><span class="sxs-lookup"><span data-stu-id="60507-296">Here are the results of configuring permissions:</span></span>
  
- <span data-ttu-id="60507-297">Le groupe SharePoint **Stratégie de l’entreprise - Membres** contient seulement le groupe **C-Suite** (qui contient uniquement les comptes d’utilisateur PDG, Directeur financier et Directeur informatique) et le groupe **Stratégie de l’entreprise** (qui contient uniquement le compte d’utilisateur de l’administrateur général).</span><span class="sxs-lookup"><span data-stu-id="60507-297">The **Company strategy-Members** SharePoint group contains only the **C-Suite** group (which contains only the CEO, CFO, and CIO user accounts) and the **Company strategy** group (which contains only the global administrator user account).</span></span>
    
- <span data-ttu-id="60507-298">Le groupe SharePoint **Stratégie de l’entreprise - Propriétaires** contient seulement le groupe **Équipe Informatique** (qui contient seulement les comptes d’utilisateur ITAdmin1 et ITAdmin2).</span><span class="sxs-lookup"><span data-stu-id="60507-298">The **Company strategy-Owners** SharePoint group contains only the **IT staff** group (which contains only the ITAdmin1 and ITAdmin2 user accounts).</span></span>
    
- <span data-ttu-id="60507-299">Le groupe SharePoint **Stratégie de l’entreprise - Visiteurs** ne contient aucun groupe ni compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60507-299">The **Company strategy-Visitors** SharePoint group contains no groups or user accounts.</span></span>
    
- <span data-ttu-id="60507-300">Les membres ne peuvent pas modifier les autorisations au niveau du site (ceci peut être fait seulement par les membres du groupe **Stratégie de l’entreprise - Propriétaires**).</span><span class="sxs-lookup"><span data-stu-id="60507-300">Members cannot modify site-level permissions (this can only be done by members of the **Company strategy-Owners** group).</span></span>
    
- <span data-ttu-id="60507-p105">Les autres comptes d’utilisateur ne peuvent ni accéder au site ou à ses ressources, ni demander l’accès au site. Des autorisations supplémentaires pour le site doivent être octroyées par l’administrateur général ou un membre du groupe **Stratégie de l’entreprise - Propriétaires**.</span><span class="sxs-lookup"><span data-stu-id="60507-p105">Other user accounts cannot access the site or its resources or request access to the site. Additional permissions to the site must be done by the global administrator or by a member of the **Company strategy-Owners** group.</span></span>
    
<span data-ttu-id="60507-303">Ensuite, configurez le dossier de documents du site d’équipe Stratégie d’entreprise pour l’étiquette Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="60507-303">Next, configure the documents folder of the Company strategy team site for the Highly Confidential label.</span></span>
  
1. <span data-ttu-id="60507-304">Sous l’onglet **Stratégie de l’entreprise - Accueil** de votre navigateur, cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="60507-304">In the **Company strategy-Home** tab of your browser, click **Documents**.</span></span>
    
2. <span data-ttu-id="60507-305">Cliquez sur l’icône des paramètres, puis cliquez sur **Paramètres de la bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-305">Click the settings icon, and then click **Library settings**.</span></span>
    
3. <span data-ttu-id="60507-306">Sous **Autorisations et gestion**, cliquez sur **Appliquer l’étiquette aux éléments de cette bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="60507-306">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
4. <span data-ttu-id="60507-307">Dans **Paramètres - Appliquer une étiquette**, sélectionnez **Hautement confidentiel**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-307">In **Settings-Apply Label**, select **Highly Confidential**, and then click **Save**.</span></span>
    
<span data-ttu-id="60507-308">Ensuite, configurez une stratégie de protection contre la perte de données qui bloque les utilisateurs quand ils partagent un document à l’extérieur de l’organisation sur un site d’équipe SharePoint Online avec l’étiquette Hautement confidentiel, qui inclut le site Stratégie de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="60507-308">Next, configure a DLP policy that blocks users when they share a document on a SharePoint Online team site with the Highly Confidential label, which includes the Company strategy site, outside the organization.</span></span>
  
1. <span data-ttu-id="60507-309">Se connecter au[portail de conformité de Microsoft 365](https://compliance.microsoft.com/) avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="60507-309">Sign in to the [Microsoft 365 compliance portal](https://compliance.microsoft.com/) with your global admin.</span></span>
    
2. <span data-ttu-id="60507-310">Sous le nouvel onglet **Conformité Microsoft 365** de votre navigateur, cliquez sur **Stratégie > Protection contre la perte de données**.</span><span class="sxs-lookup"><span data-stu-id="60507-310">On the new **Microsoft 365 compliance** tab in your browser, click **Policies > Data loss prevention**.</span></span>
    
3. <span data-ttu-id="60507-311">Dans le volet **Accueil > Protection contre la perte de données**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="60507-311">In the **Home > Data loss prevention** pane, click **Create a policy**.</span></span>
    
4. <span data-ttu-id="60507-312">Dans le volet **Utiliser un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-312">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="60507-313">Dans le volet **Nom de votre stratégie**, saisissez les **sites d’équipe SharePoint Online avec étiquette Hautement confidentiel** sous **Nom**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-313">In the **Name your policy** pane, type **Highly Confidential label SharePoint Online team sites** in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="60507-314">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-314">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="60507-315">Dans la liste des emplacements, désactivez les emplacements **Courrier Exchange**, **Comptes OneDrive** et **Messages de conversations et de canaux Teams**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-315">In the list of locations, disable the **Exchange email**, **OneDrive accounts**, and **Teams chat and channel messages** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="60507-316">Dans le volet **Personnalisez le type de contenu que vous voulez protéger**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="60507-316">In the **Customize the type of content you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="60507-317">Dans le volet **Choisissez les types de contenu à protéger**, cliquez sur **Ajouter** dans la zone déroulante, puis sélectionnez **Étiquettes de rétention**.</span><span class="sxs-lookup"><span data-stu-id="60507-317">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Retention labels**.</span></span>
    
10. <span data-ttu-id="60507-318">Dans le volet **Étiquettes de rétention**, cliquez sur **Ajouter**, sélectionnez l’étiquette **Hautement confidentiel**, puis cliquez sur **Ajouter** et sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="60507-318">In the **Retention labels** pane, click **Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="60507-319">Dans le volet **Choisir les types de contenu à protéger**, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="60507-319">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="60507-320">Dans le volet **Personnaliser les types d’informations sensibles que vous souhaitez protéger**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-320">In the **Customize the type of content you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="60507-321">Dans le volet **Que faire en cas de détection d’informations sensibles ?**, cliquez sur **Personnaliser l’info-bulle et l’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="60507-321">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="60507-322">Dans le volet **Personnaliser les conseils et les notifications par e-mail de la stratégie**, cliquez sur **Personnaliser le texte de l’info-bulle de la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="60507-322">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="60507-323">Dans la zone de texte, saisissez ou collez l’un des conseils suivants, selon si vous avez implémenté Azure Information Protection pour protéger les fichiers hautement confidentiels :</span><span class="sxs-lookup"><span data-stu-id="60507-323">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="60507-p106">Pour partager un fichier avec un utilisateur extérieur à l’organisation, téléchargez-le et ouvrez-le. Cliquez sur Fichier > Protéger le document > Chiffrer avec mot de passe, puis indiquez un mot de passe fort. Envoyez le mot de passe par e-mail ou un autre moyen de communication.</span><span class="sxs-lookup"><span data-stu-id="60507-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
16. <span data-ttu-id="60507-327">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-327">Click **OK**.</span></span>
    
17. <span data-ttu-id="60507-328">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-328">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>

18. <span data-ttu-id="60507-329">Dans le volet **Voulez-vous activer la stratégie ou d’abord effectuer des tests ?**, cliquez sur **Oui, l’activer maintenant**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="60507-329">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="60507-330">Dans le volet **Vérifier vos paramètres**, cliquez sur **Créer**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="60507-330">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
   
    
<span data-ttu-id="60507-331">Suivez ensuite les instructions contenues dans [Comment activer Azure Rights Management à partir du Centre d’administration Microsoft 365](https://docs.microsoft.com/information-protection/deploy-use/activate-office365).</span><span class="sxs-lookup"><span data-stu-id="60507-331">Next, follow the instructions in [Activate Azure RMS with the Microsoft 365 admin center](https://docs.microsoft.com/information-protection/deploy-use/activate-office365).</span></span>
  
<span data-ttu-id="60507-332">Ensuite, configurez Azure Information Protection avec une nouvelle stratégie et une sous-étiquette délimitée pour le groupe C-Suite pour la protection et les autorisations en suivant ces étapes :</span><span class="sxs-lookup"><span data-stu-id="60507-332">Next, configure Azure Information Protection with a new policy and sub-label scoped for the C-Suite group for protection and permissions with the following steps:</span></span>
  
1. <span data-ttu-id="60507-333">Si cela est nécessaire, connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de votre compte administrateur général.</span><span class="sxs-lookup"><span data-stu-id="60507-333">If needed, sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with your global admin account.</span></span>
    
2. <span data-ttu-id="60507-334">Dans un nouvel onglet de votre navigateur, accédez au portail Azure ([https://portal.azure.com](https://portal.azure.com)).</span><span class="sxs-lookup"><span data-stu-id="60507-334">In a separate tab of your browser, go to the Azure portal ([https://portal.azure.com](https://portal.azure.com)).</span></span>
    
3. <span data-ttu-id="60507-335">Si vous configurez Azure Information Protection pour la première fois, consultez ces [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span><span class="sxs-lookup"><span data-stu-id="60507-335">If this is the first time you are configuring Azure Information Protection, see these [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span></span>
    
4. <span data-ttu-id="60507-336">Dans le volet Liste, cliquez sur **Tous les services**, saisissez **Informations**, puis cliquez sur **Azure Information Protection**.</span><span class="sxs-lookup"><span data-stu-id="60507-336">In the list pane, click **All services**, type **information**, and then click **Azure Information Protection**.</span></span>

5. <span data-ttu-id="60507-337">Cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="60507-337">Click **Labels**.</span></span>
    
6. <span data-ttu-id="60507-338">Cliquez avec le bouton droit de la souris sur l’étiquette **Hautement confidentiel**, puis sur **Ajouter une sous-étiquette**.</span><span class="sxs-lookup"><span data-stu-id="60507-338">Right-click the **Highly Confidential** label, and then click **Add a sub-label**.</span></span>
    
7. <span data-ttu-id="60507-339">Saisissez **Membres C-Suite** dans **Nom** et **Description**.</span><span class="sxs-lookup"><span data-stu-id="60507-339">Type **C-Suite members** in **Name** and **Description**.</span></span>
    
8. <span data-ttu-id="60507-340">Cliquez sur **Protéger** dans **Définir les autorisations pour les documents et les e-mails contenant cette étiquette**.</span><span class="sxs-lookup"><span data-stu-id="60507-340">In **Set permissions for documents and emails containing this label**, click **Protect**.</span></span>
    
9. <span data-ttu-id="60507-341">Dans la section **Protection**, cliquez sur **Azure (clé cloud)**.</span><span class="sxs-lookup"><span data-stu-id="60507-341">In the **Protection** section, click **Azure (cloud key)**.</span></span>
    
10. <span data-ttu-id="60507-342">Dans le panneau **Protection**, sous **Paramètres de protection**, cliquez sur **+ Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="60507-342">On the **Protection** blade, under **Protection settings**, click **+ Add permissions**.</span></span>
    
11. <span data-ttu-id="60507-343">Dans le panneau **Ajouter des autorisations**, sous **Spécifier les utilisateurs et les groupes**, cliquez sur **+ Parcourir le répertoire**.</span><span class="sxs-lookup"><span data-stu-id="60507-343">On the **Add permissions** blade, under **Specify users and groups**, click **+ Browse directory**.</span></span>
    
12. <span data-ttu-id="60507-344">Dans le volet **Utilisateurs et groupes AAD**, sélectionnez **C-Suite**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="60507-344">On the **AAD Users and Groups** pane, select **C-Suite**, and then click **Select**.</span></span>
    
13. <span data-ttu-id="60507-345">Sous **Choisir les autorisations parmi les autorisations personnalisées prédéfinies ou définies**, cliquez sur **Personnalisé**, puis sur les cases à cocher **Afficher les droits**, **Modifier le contenu**, **Enregistrer**, **Répondre**, et **Répondre à tous**.</span><span class="sxs-lookup"><span data-stu-id="60507-345">Under **Choose permissions from the preset or set custom**, click **Custom**, and then click the **View Rights**, **Edit Content**, **Save**, **Reply**, and **Reply all** check boxes.</span></span>
    
14. <span data-ttu-id="60507-346">Cliquez deux fois sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-346">Click **OK** twice.</span></span>
    
15. <span data-ttu-id="60507-347">Dans le panneau **Sous-étiquette**, cliquez sur **Enregistrer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-347">On the **Sub-label** blade, click **Save**, and then click **OK**.</span></span>

16. <span data-ttu-id="60507-348">Dans le panneau **Azure Information Protection**, cliquez sur **Stratégies > + Ajouter une nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="60507-348">On the **Azure Information protection** blade, click **Policies > + Add a new policy**.</span></span>
    
17. <span data-ttu-id="60507-349">Tapez **CompanyStrategy** dans **Nom de la stratégie** et **Étiquette pour les documents dans le site d’équipe Stratégie d’entreprise** dans **Description**.</span><span class="sxs-lookup"><span data-stu-id="60507-349">Type **CompanyStrategy** in **Policy name** and **Documents in the Company strategy team site** in **Description**.</span></span>
    
18. <span data-ttu-id="60507-350">Cliquez sur**Sélectionner les utilisateurs ou groupes devant recevoir cette stratégie > Utilisateurs/Groupes**, puis sélectionnez **C-Suite**.</span><span class="sxs-lookup"><span data-stu-id="60507-350">Click **Select which users or groups get this policy > User/Groups**, and then select **C-Suite**.</span></span>
    
19. <span data-ttu-id="60507-351">Cliquez sur **Sélectionner > OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-351">Click **Select > OK**.</span></span>

20. <span data-ttu-id="60507-p107">Cliquez sur **Ajouter ou supprimer des étiquettes**. Dans le volet **Stratégie : Ajouter ou supprimer des étiquettes**, cliquez sur **C-Suite**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-p107">Click **Add or remove labels**. In the **Policy: Add or remove labels** pane, click **C-Suite**, and then click **OK**.</span></span>   

21. <span data-ttu-id="60507-354">Cliquez sur **Enregistrer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="60507-354">Click **Save**, and then click **OK**.</span></span>
    
<span data-ttu-id="60507-355">Pour protéger un document avec Azure Information Protection et cette nouvelle étiquette, vous devez [installer le client Azure Information Protection](https://docs.microsoft.com/information-protection/rms-client/install-client-app) sur une machine de test, installer Office à partir du centre d’administration, puis vous connecter à partir de Microsoft Word avec un compte du groupe **C-Suite** de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-355">To protect a document with Azure Information Protection and this new label, you must [install the Azure Information Protection client](https://docs.microsoft.com/information-protection/rms-client/install-client-app) on a test machine, install Office from the admin center, and then sign in from Microsoft Word with an account in the **C-Suite** group of your trial subscription.</span></span>
  
<span data-ttu-id="60507-356">Vous êtes maintenant prêt à créer des documents dans ces quatre sites et à tester l’accès à ceux-ci avec différents comptes d’utilisateur de votre abonnement d’essai.</span><span class="sxs-lookup"><span data-stu-id="60507-356">You are now ready to create documents in these four sites and test access to them with various user accounts in your trial subscription.</span></span>
  
<span data-ttu-id="60507-357">Voici la configuration globale pour les quatre sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="60507-357">Here is the overall configuration for all four SharePoint Online team sites.</span></span>
  
![Les quatre sites d’équipe dans l’environnement de développement/test SharePoint Online sécurisé.](media/b0fea489-359c-4c85-a0ad-e4efb4a1e47f.png)
  
## <a name="next-step"></a><span data-ttu-id="60507-359">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="60507-359">Next step</span></span>

<span data-ttu-id="60507-360">Quand vous êtes prêt à effectuer le déploiement en production de sites SharePoint Online sécurisés, consultez [Sécuriser des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md) pour obtenir des informations détaillées et des liens vers des articles sur le déploiement étape par étape.</span><span class="sxs-lookup"><span data-stu-id="60507-360">When you are ready for production deployment of secure SharePoint Online sites, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md) for detailed information and links to step-by-step deployment articles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60507-361">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60507-361">See Also</span></span>

[<span data-ttu-id="60507-362">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="60507-362">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="60507-363">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="60507-363">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="60507-364">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="60507-364">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)




