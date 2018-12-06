---
title: Installer le complément Surveillance pour la version de bureau d’Outlook
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Installer le complément Office 365 surveillance pour la version de bureau d’Outlook
ms.openlocfilehash: b0cb0d78ab5f8887628528dd53b49fb15de44126
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180864"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="d499c-103">Installer le complément Surveillance pour la version de bureau d’Outlook</span><span class="sxs-lookup"><span data-stu-id="d499c-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="d499c-p101">Pour passer en revue les communications identifiées par une stratégie de surveillance, utilisez relecteurs le complément de contrôle pour Outlook et Outlook web app. Le complément est installé automatiquement dans Outlook web app pour tous les relecteurs spécifiés dans la stratégie. Cependant, réviseurs doivent exécuter certaines étapes de l’installer dans la version de bureau d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="d499c-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d499c-p102">Utilisateurs contrôlés par des stratégies de surveillance doivent avoir une licence d’Office 365 entreprise E3 avec le module complémentaire de conformité avancée ou être inclus dans un abonnement à Office 365 entreprise E5. Si vous n’avez un plan d’entreprise E5 existant et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d499c-p102">Users monitored by supervision policies must have either an Office 365 Enterprise E3 license with the Advanced Compliance add-on or be included in an Office 365 Enterprise E5 subscription. If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="d499c-109">Étape 1 : Copier l’adresse de la boîte aux lettres de surveillance</span><span class="sxs-lookup"><span data-stu-id="d499c-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="d499c-110">Pour installer le complément pour Outlook du bureau, vous devez l’adresse pour la boîte aux lettres de surveillance qui a été créé dans le cadre de la configuration de stratégie de surveillance.</span><span class="sxs-lookup"><span data-stu-id="d499c-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d499c-111">Si un autre utilisateur la stratégie, vous devez obtenir cette adresse à partir de celles-ci pour installer le complément.</span><span class="sxs-lookup"><span data-stu-id="d499c-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span>
 
 <span data-ttu-id="d499c-112">**Pour rechercher l’adresse de boîte aux lettres de surveillance**</span><span class="sxs-lookup"><span data-stu-id="d499c-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="d499c-113">Se connecter à la [sécurité &amp; centre de conformité](https://protection.office.com) à l’aide des informations d’identification d’un compte d’administration dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="d499c-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>
    
2. <span data-ttu-id="d499c-114">Accédez à **la gouvernance des données** \> **surveillance**.</span><span class="sxs-lookup"><span data-stu-id="d499c-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="d499c-115">Cliquez sur la stratégie de surveillance qui collecte les communications que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="d499c-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="d499c-116">Dans la stratégie de détails flottant, sous \*\* boîte aux lettres de surveillance \*\*, copiez l’adresse.</span><span class="sxs-lookup"><span data-stu-id="d499c-116">In the policy details flyout, under \*\* Supervision mailbox \*\*, copy the address.</span></span><br/>![La section « Boîte aux lettres de surveillance » de volant de détails d’une stratégie de surveillance avec l’adresse de boîte aux lettres de surveillance mis en surbrillance](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="d499c-118">Étape 2 : Configurer la boîte aux lettres de contrôle d’accès du bureau d’Outlook</span><span class="sxs-lookup"><span data-stu-id="d499c-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="d499c-119">Ensuite, relecteurs vous devrez exécuter deux commandes Exchange Online PowerShell afin qu’ils peuvent connecter Outlook à la boîte aux lettres de surveillance.</span><span class="sxs-lookup"><span data-stu-id="d499c-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="d499c-p103">Connexion à Exchange Online PowerShell. [Comment faire ceci ?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="d499c-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="d499c-122">Exécutez les commandes suivantes, où *SupervisoryReview{GUID}@domain.onmicrosoft.com* est l’adresse que vous avez copié à l’étape 1 ci-dessus et *utilisateur* est le nom du relecteur doivent se connecter à la boîte aux lettres de surveillance à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d499c-122">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in Step 3.</span></span>
    - ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```<br/>
    - ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```
    
3. <span data-ttu-id="d499c-123">Attendez au moins une heure avant de passer à l’étape 3 ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d499c-123">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="d499c-124">Étape 3 : Créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance</span><span class="sxs-lookup"><span data-stu-id="d499c-124">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="d499c-125">La dernière étape, relecteurs vous devrez créer un profil Outlook pour se connecter à la boîte aux lettres de surveillance.</span><span class="sxs-lookup"><span data-stu-id="d499c-125">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span>
 
> [!NOTE]
> <span data-ttu-id="d499c-p104">Pour créer un nouveau profil Outlook, vous allez utiliser les paramètres de messagerie dans le panneau de configuration Windows. Le chemin d’accès que vous prenez pour accéder à ces paramètres peut-être dépendre d’un système d’exploitation Windows (Windows 7, Windows 8 ou Windows 10) que vous utilisez et la version d’Outlook est installée.</span><span class="sxs-lookup"><span data-stu-id="d499c-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="d499c-128">Ouvrez le panneau de configuration, et dans la zone de **recherche** en haut de la fenêtre, tapez **Mail**.</span><span class="sxs-lookup"><span data-stu-id="d499c-128">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="d499c-p105">(Ne savez pas comment atteindre le panneau de configuration ? Voir [où est le panneau de configuration ?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span><span class="sxs-lookup"><span data-stu-id="d499c-p105">(Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="d499c-131">Ouvrez l’application de **messagerie** .</span><span class="sxs-lookup"><span data-stu-id="d499c-131">Open the **Mail** app.</span></span>
    
3. <span data-ttu-id="d499c-132">Dans la **Configuration de la messagerie - Outlook**, cliquez sur **Afficher les profils**.</span><span class="sxs-lookup"><span data-stu-id="d499c-132">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="d499c-133">![La « configuration de la messagerie - Outlook' boîte de dialogue avec le bouton Afficher les profils en surbrillance](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="d499c-133">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="d499c-p106">Dans la **messagerie**, cliquez sur **Ajouter**. Puis, dans le **Nouveau profil**, entrez un nom pour la boîte aux lettres de surveillance (par exemple, **surveillance**).</span><span class="sxs-lookup"><span data-stu-id="d499c-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="d499c-136">![La boîte de dialogue « Nouveau profil » l’affichage du nom « Surveillance » dans la zone Nom du profil](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="d499c-136">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="d499c-137">Dans **Outlook de se connecter à Office 365**, cliquez sur **se connecter à un autre compte**.</span><span class="sxs-lookup"><span data-stu-id="d499c-137">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="d499c-138">![Le message « Outlook de se connecter à Office 365 » avec le lien « Se connecter à un autre compte » en surbrillance](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="d499c-138">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="d499c-139">Dans la **Configuration de compte automatique**, sélectionnez **configuration manuelle ou types de serveurs supplémentaires**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d499c-139">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="d499c-p107">**Sélectionnez votre Type de compte**, choisissez **Office 365**. Puis, dans la zone **Adresse de messagerie** , entrez l’adresse de la boîte aux lettres de surveillance que vous avez copié précédemment.</span><span class="sxs-lookup"><span data-stu-id="d499c-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="d499c-142">![La page « Choisir votre propre Type de compte de la boîte de dialogue Ajouter un compte dans Outlook affiche la boîte de « Adresse de messagerie » mise en surbrillance.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="d499c-142">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="d499c-143">Lorsque vous y êtes invité, entrez vos informations d’identification d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="d499c-143">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="d499c-144">Si elle réussit, vous verrez le \*\*surveillance - \<nom de la stratégie\> \*\* dossier répertorié dans la vue liste des dossiers dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="d499c-144">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span>