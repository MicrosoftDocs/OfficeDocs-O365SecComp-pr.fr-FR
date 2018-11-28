---
title: Activer le complément Signaler le message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Découvrez comment activer le complément de Message de rapport pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou la totalité de votre organisation.
ms.openlocfilehash: f35899d3f0be9ee07cb6dae5c5fec40395948340
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706368"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="8716f-103">Activer le complément Signaler le message</span><span class="sxs-lookup"><span data-stu-id="8716f-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="8716f-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="8716f-104">Overview</span></span>

<span data-ttu-id="8716f-p101">Le complément de Message de rapport pour Outlook et Outlook sur le Web permet aux utilisateurs de créer facilement des rapports e-mail mal classé, fiables ou malveillantes, Microsoft et ses filiales pour l’analyse. Microsoft utilise ces envois pour améliorer l’efficacité des technologies de protection de courrier électronique. En outre, si votre organisation utilise [Office 365 avancée protection contre les menaces](office-365-atp.md) ou des [Menaces Office 365](office-365-ti.md), le complément de Message de rapport fournit l’équipe de sécurité de votre organisation des informations utiles, qu'ils peuvent utiliser pour examiner et mettre à jour stratégies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8716f-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="8716f-p102">Par exemple, supposons que personnes signalent un grand nombre de messages phishing. Cette surfaces d’informations dans le [Tableau de bord de sécurité](security-dashboard.md) et autres rapports. L’équipe de sécurité de votre organisation permettre utiliser ces informations comme une indication que les stratégies anti-hameçonnage devront être mis à jour. Ou, si un grand nombre de messages qui ont été marqués comme courrier indésirable comme légitime à l’aide du complément de Message de rapport signalez des personnes, l’équipe de sécurité de votre organisation devront ajuster les [stratégies de blocage du courrier indésirable](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8716f-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="8716f-112">Le complément de Message de rapport fonctionne avec votre abonnement Office 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="8716f-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="8716f-113">Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="8716f-113">Outlook on the Web</span></span>
 - <span data-ttu-id="8716f-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="8716f-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="8716f-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8716f-115">Outlook 2016</span></span>
 - <span data-ttu-id="8716f-116">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="8716f-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="8716f-117">Outlook inclus avec Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="8716f-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="8716f-118">Si vous êtes un utilisateur individuel, vous pouvez [Activer le complément de Message de rapport par vous-même](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="8716f-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="8716f-p103">Si vous êtes un administrateur global d’Office 365 ou un administrateur Exchange Online et Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez [Activer le complément de Message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization). Le rapport de Message Add-In est désormais disponible par le biais de [Déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="8716f-p103">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="8716f-121">Obtenez le Message de rapport de complément pour vous-même</span><span class="sxs-lookup"><span data-stu-id="8716f-121">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="8716f-122">Dans [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), recherchez le [complément de Message de rapport](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="8716f-122">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="8716f-123">Choisissez **obtenir maintenant IT**.</span><span class="sxs-lookup"><span data-stu-id="8716f-123">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="8716f-124">![Déclaration de Message - maintenant](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-124">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="8716f-p104">Passez en revue les termes du contrat de stratégie de confidentialité et d’utilisation. Puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="8716f-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="8716f-127">Connectez-vous à votre messagerie électronique Office 365 à l’aide de votre travail compte école (pour une utilisation professionnelle) ou votre compte Microsoft (pour une utilisation personnelle).</span><span class="sxs-lookup"><span data-stu-id="8716f-127">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="8716f-128">Une fois que le complément est installé et activé, vous verrez les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8716f-128">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="8716f-129">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="8716f-129">In Outlook the icon looks like this:</span></span> <br/> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="8716f-131">Dans Outlook Web App, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="8716f-131">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="8716f-133">Étape suivante, découvrez comment [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="8716f-133">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="8716f-134">Obtenir et activer le complément de Message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="8716f-134">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8716f-p105">Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche. En outre, Exchange doit être configuré pour utiliser l’authentification OAuth pour plus d’informations, voir [Configuration requise pour Exchange (centralisée le déploiement des compléments)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="8716f-p105">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="8716f-137">Accédez à la [page des compléments et des Services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365 nouveau.</span><span class="sxs-lookup"><span data-stu-id="8716f-137">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="8716f-138">![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-138">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="8716f-139">Choisissez **+ déployer le complément**.</span><span class="sxs-lookup"><span data-stu-id="8716f-139">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="8716f-140">![Cliquez sur déployer le complément](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-140">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="8716f-141">Dans l’écran nouveau complément, passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8716f-141">In the New Add-In screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="8716f-142">![Nouveau complément plus d’informations](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-142">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="8716f-143">Sélectionnez **Ajouter un complément à partir de l’Office Store**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8716f-143">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="8716f-144">![Vous voulez ajouter un nouveau complément](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-144">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="8716f-145">Pour un Message de rapport et dans la liste des résultats, en regard du complément Message d’état de la recherche, cliquez sur Ajouter.</span><span class="sxs-lookup"><span data-stu-id="8716f-145">Search for Report Message, and in the list of results, next to the Report Message Add-In, choose Add.</span></span><br/>![Rechercher un Message de rapport, puis choisissez Ajouter](media/NewAddInScreen3.png)<br/>
    
6. <span data-ttu-id="8716f-147">Dans l’écran de Message de rapport, passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8716f-147">On the Report Message screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="8716f-148">![Détails du Message](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-148">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="8716f-149">Spécifier les paramètres utilisateur par défaut pour Outlook, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8716f-149">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="8716f-150">![Signaler les paramètres par défaut des messages pour Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-150">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="8716f-151">Spécifier qui obtient le Message de rapport Add-in, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8716f-151">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="8716f-152">![Qui obtient le Message de rapport complément](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-152">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="8716f-153">Nous vous recommandons de [paramétrage d’une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span><span class="sxs-lookup"><span data-stu-id="8716f-153">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="8716f-p106">Selon ce que vous sélectionné à l’aide de l’Assistant, les personnes de votre organisation auront le [complément de Message d’état](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponibles. Les personnes dans votre organisation, voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8716f-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="8716f-156">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="8716f-156">In Outlook the icon looks like this:</span></span> <br/> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="8716f-158">Dans Outlook Web App, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="8716f-158">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="8716f-160">Définir une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8716f-160">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8716f-161">Vous devez être administrateur Exchange Online pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="8716f-161">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="8716f-p107">Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation. Cela après avoir téléchargé et activé le complément de Message de rapport pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8716f-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="8716f-164">Dans le centre d’administration Exchange, choisissez **flux de messagerie** \> **règles**.</span><span class="sxs-lookup"><span data-stu-id="8716f-164">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="8716f-165">Choisissez **+** \> **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="8716f-165">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="8716f-166">Dans la zone **nom** , tapez un nom, tel que des envois.</span><span class="sxs-lookup"><span data-stu-id="8716f-166">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="8716f-167">Dans la liste **appliquer cette règle si** , sélectionnez **l’adresse du destinataire inclut...**.</span><span class="sxs-lookup"><span data-stu-id="8716f-167">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="8716f-168">Dans l’écran **spécifier les mots ou expressions** , ajoutez `junk@office365.microsoft.com` et `phish@office365.microsoft.com`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8716f-168">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="8716f-169">![Spécifier les adresses de courrier indésirable et de phishing pour la règle](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-169">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="8716f-170">Dans la liste **effectuer les opérations suivantes** , choisissez **Cci du message pour...**.</span><span class="sxs-lookup"><span data-stu-id="8716f-170">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="8716f-171">Ajouter un administrateur global, un administrateur de sécurité et/ou lecteur de sécurité qui doit recevoir une copie de chaque message électronique qui signalent à Microsoft les personnes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8716f-171">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="8716f-172">![Ajouter un administrateur global ou de sécurité pour recevoir une copie de chaque message signalé](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-172">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="8716f-173">Sélectionnez **Auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**.</span><span class="sxs-lookup"><span data-stu-id="8716f-173">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="8716f-174">Sous **Choisir un mode de cette règle**, cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="8716f-174">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="8716f-175">![Définir une règle pour obtenir une copie de chaque message signalé](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-175">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="8716f-176">Sélectionnez **Save (Enregistrer)**.</span><span class="sxs-lookup"><span data-stu-id="8716f-176">Choose **Save**.</span></span> 
    
<span data-ttu-id="8716f-p108">À cette règle en place, chaque fois qu’une personne de votre organisation signale un message électronique à l’aide du complément Message de rapport, votre administrateur général, administrateur de sécurité et/ou lecteur sécurité reçoit une copie de ce message. Ces informations permettent de vous permet de définir ou ajuster les stratégies, telles que les stratégies de [Liaisons sans échec de Office 365 DAV](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="8716f-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="8716f-179">Vérifier ou modifier les paramètres pour le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="8716f-179">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="8716f-180">Vous pouvez consulter et modifier les paramètres par défaut pour le rapport de Message complément dans la [page Services et compléments](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="8716f-180">You can review and edit the default settings for the Report Message Add-In in the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8716f-181">Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="8716f-181">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="8716f-182">Accédez à la [page des compléments et des Services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365 nouveau.</span><span class="sxs-lookup"><span data-stu-id="8716f-182">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="8716f-183">![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="8716f-183">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="8716f-184">Recherchez et sélectionnez le rapport de Message Add-In.</span><span class="sxs-lookup"><span data-stu-id="8716f-184">Find and select the Report Message Add-In.</span></span><br/>![Recherchez et sélectionnez le complément de Message de rapport](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="8716f-186">Dans l’écran de Message de rapport, passez en revue et modifier les paramètres comme il convient pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8716f-186">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Complément de paramètres pour le Message d’état](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="8716f-188">Découvrez comment utiliser le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="8716f-188">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="8716f-189">Consultez la rubrique [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="8716f-189">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="8716f-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8716f-190">Related topics</span></span>

[<span data-ttu-id="8716f-191">Utiliser le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="8716f-191">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="8716f-192">Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="8716f-192">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="8716f-193">Afficher les rapports de Protection de menace avancées d’Office 365</span><span class="sxs-lookup"><span data-stu-id="8716f-193">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="8716f-194">Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="8716f-194">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

