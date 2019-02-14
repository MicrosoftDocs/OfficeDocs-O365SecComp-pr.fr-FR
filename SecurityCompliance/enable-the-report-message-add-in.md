---
title: Activer le complément Signaler le message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le complément de Message de rapport pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou la totalité de votre organisation.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995155"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="92b05-103">Activer le complément Signaler le message</span><span class="sxs-lookup"><span data-stu-id="92b05-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="92b05-104">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="92b05-104">Overview</span></span>

<span data-ttu-id="92b05-p101">Le complément de Message de rapport pour Outlook et Outlook sur le web permet aux utilisateurs de créer facilement des rapports e-mail mal classé, fiables ou malveillantes, Microsoft et ses filiales pour l’analyse. Microsoft utilise ces envois pour améliorer l’efficacité des technologies de protection de courrier électronique. En outre, si votre organisation utilise [Office 365 avancée protection contre les menaces](office-365-atp.md) ou des [Menaces Office 365](office-365-ti.md), le complément de Message de rapport fournit l’équipe de sécurité de votre organisation des informations utiles, qu'ils peuvent utiliser pour examiner et mettre à jour stratégies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="92b05-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="92b05-p102">Par exemple, supposons que personnes signalent un grand nombre de messages phishing. Cette surfaces d’informations dans le [Tableau de bord de sécurité](security-dashboard.md) et autres rapports. L’équipe de sécurité de votre organisation permettre utiliser ces informations comme une indication que les stratégies anti-hameçonnage devront être mis à jour. Ou, si un grand nombre de messages qui ont été marqués comme courrier indésirable comme légitime à l’aide du complément de Message de rapport signalez des personnes, l’équipe de sécurité de votre organisation devront ajuster les [stratégies de blocage du courrier indésirable](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="92b05-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="92b05-112">Le complément de Message de rapport fonctionne avec votre abonnement Office 365 et les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="92b05-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="92b05-113">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="92b05-113">Outlook on the web</span></span>
 - <span data-ttu-id="92b05-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="92b05-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="92b05-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92b05-115">Outlook 2016</span></span>
 - <span data-ttu-id="92b05-116">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="92b05-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="92b05-117">Outlook inclus avec Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="92b05-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="92b05-p103">Le complément de Message de rapport pour Outlook et Outlook sur le web est pas exactement la même chose que le [Filtre de courrier indésirable Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), mais peuvent être utilisés pour marquer le courrier indésirable, pas indésirable ou une tentative de hameçonnage. Le complément de Message de rapport pour Outlook et Outlook sur le web avertit Microsoft messagerie mal classé, tandis que le filtre de courrier indésirable Outlook est utilisé pour organiser les messages électroniques dans la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92b05-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="92b05-120">Si vous êtes un utilisateur individuel, vous pouvez [Activer le complément de Message de rapport par vous-même](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="92b05-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="92b05-p104">Si vous êtes un administrateur global d’Office 365 ou un administrateur Exchange Online et Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez [Activer le complément de Message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization). Le rapport de Message Add-In est désormais disponible par le biais de [Déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="92b05-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="92b05-123">Obtenez le Message de rapport de complément pour vous-même</span><span class="sxs-lookup"><span data-stu-id="92b05-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="92b05-124">Dans [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), recherchez le [complément de Message de rapport](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="92b05-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="92b05-125">Choisissez **obtenir maintenant IT**.</span><span class="sxs-lookup"><span data-stu-id="92b05-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="92b05-126">![Déclaration de Message - maintenant](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="92b05-p105">Passez en revue les termes du contrat de stratégie de confidentialité et d’utilisation. Puis cliquez sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="92b05-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="92b05-129">Connectez-vous à Office 365 à l’aide de votre travail compte école (pour une utilisation professionnelle) ou votre compte Microsoft (pour une utilisation personnelle).</span><span class="sxs-lookup"><span data-stu-id="92b05-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="92b05-130">Une fois que le complément est installé et activé, vous verrez les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="92b05-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="92b05-131">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="92b05-131">In Outlook, the icon looks like this:</span></span> <br/> ![Signaler l’icône Message complément pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="92b05-133">Dans Outlook Web App (ou Outlook sur le web), l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="92b05-133">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook sur l’icône Ajouter dans un Message de rapport](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="92b05-135">Étape suivante, découvrez comment [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="92b05-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="92b05-136">Obtenir et activer le complément de Message de rapport pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="92b05-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92b05-p106">Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche. En outre, Exchange doit être configuré pour utiliser l’authentification OAuth pour plus d’informations, voir [Configuration requise pour Exchange (centralisée le déploiement des compléments)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="92b05-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="92b05-139">Accédez à la [page des Services & des compléments](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="92b05-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="92b05-140">![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="92b05-141">Choisissez **+ déployer le complément**.</span><span class="sxs-lookup"><span data-stu-id="92b05-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="92b05-142">![Cliquez sur déployer le complément](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="92b05-143">Dans l’écran **Nouveau complément** , passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="92b05-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="92b05-144">![Nouveau complément plus d’informations](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="92b05-145">Sélectionnez **Ajouter un complément à partir de l’Office Store**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="92b05-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="92b05-146">![Vous voulez ajouter un nouveau complément](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="92b05-147">Pour **Un Message de rapport**et dans la liste des résultats, en regard de la **Macro complémentaire rapport de Message**de la recherche, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="92b05-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="92b05-148">![Rechercher un Message de rapport, puis choisissez Ajouter](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="92b05-149">Dans l’écran de **Message de rapport** , passez en revue les informations, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="92b05-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="92b05-150">![Détails du Message](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="92b05-151">Spécifier les paramètres utilisateur par défaut pour Outlook, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="92b05-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="92b05-152">![Signaler les paramètres par défaut des messages pour Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="92b05-153">Spécifier qui obtient le Message de rapport Add-in, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="92b05-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="92b05-154">![Qui obtient le Message de rapport complément](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="92b05-155">Nous vous recommandons de [paramétrage d’une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="92b05-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="92b05-p107">Selon ce que vous avez sélectionné lorsque vous configurez le complément (étapes 7 et 8 ci-dessus), les personnes de votre organisation auront le [Message de rapport de compléments](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponibles. Les personnes dans votre organisation, voient les icônes suivantes :</span><span class="sxs-lookup"><span data-stu-id="92b05-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="92b05-158">Dans Outlook, l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="92b05-158">In Outlook, the icon looks like this:</span></span> <br/> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="92b05-160">Dans Outlook Web App (ou Outlook sur le web), l’icône ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="92b05-160">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="92b05-162">Lorsque vous avertir les utilisateurs du complément de Message de rapport, inclure un lien à [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="92b05-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="92b05-163">Définir une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="92b05-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92b05-164">Vous devez être administrateur Exchange Online pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="92b05-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="92b05-p108">Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation. Cela après avoir téléchargé et activé le complément de Message de rapport pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="92b05-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="92b05-167">Dans le centre d’administration Exchange, choisissez **flux de messagerie** \> **règles**.</span><span class="sxs-lookup"><span data-stu-id="92b05-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="92b05-168">Choisissez **+** \> **créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="92b05-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="92b05-169">Dans la zone **nom** , tapez un nom, tel que des envois.</span><span class="sxs-lookup"><span data-stu-id="92b05-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="92b05-170">Dans la liste **appliquer cette règle si** , sélectionnez **l’adresse du destinataire inclut...**.</span><span class="sxs-lookup"><span data-stu-id="92b05-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="92b05-171">Dans l’écran **spécifier les mots ou expressions** , ajoutez `junk@office365.microsoft.com` et `phish@office365.microsoft.com`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="92b05-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="92b05-172">![Spécifier les adresses de courrier indésirable et de phishing pour la règle](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="92b05-173">Dans la liste **effectuer les opérations suivantes** , choisissez **Cci du message pour...**.</span><span class="sxs-lookup"><span data-stu-id="92b05-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="92b05-174">Ajouter un administrateur global, un administrateur de sécurité et/ou lecteur de sécurité qui doit recevoir une copie de chaque message électronique qui signalent à Microsoft les personnes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="92b05-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="92b05-175">![Ajouter un administrateur global ou de sécurité pour recevoir une copie de chaque message signalé](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="92b05-176">Sélectionnez **Auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**.</span><span class="sxs-lookup"><span data-stu-id="92b05-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="92b05-177">Sous **Choisir un mode de cette règle**, cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="92b05-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="92b05-178">![Définir une règle pour obtenir une copie de chaque message signalé](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="92b05-179">Sélectionnez **Save (Enregistrer)**.</span><span class="sxs-lookup"><span data-stu-id="92b05-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="92b05-p109">À cette règle en place, chaque fois qu’une personne de votre organisation signale un message électronique à l’aide du complément Message de rapport, votre administrateur général, administrateur de sécurité et/ou lecteur sécurité reçoit une copie de ce message. Ces informations permettent de vous permet de définir ou modifier des stratégies, telles que les stratégies de [Liaisons sans échec de Office 365 DAV](atp-safe-links.md) ou vos paramètres de [blocage du courrier indésirable](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="92b05-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="92b05-182">Découvrez comment utiliser le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="92b05-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="92b05-183">Consultez la rubrique [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="92b05-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="92b05-184">Vérifier ou modifier les paramètres pour le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="92b05-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="92b05-185">Vous pouvez consulter et modifier les paramètres par défaut pour le complément de Message de rapport dans la [page des Services & Add-Ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="92b05-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="92b05-186">Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="92b05-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="92b05-187">Accédez à la [page des Services & des compléments](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="92b05-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="92b05-188">![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="92b05-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="92b05-189">Recherchez et sélectionnez le complément de Message de rapport.</span><span class="sxs-lookup"><span data-stu-id="92b05-189">Find and select the Report Message add-in.</span></span><br/>![Recherchez et sélectionnez le complément de Message de rapport](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="92b05-191">Dans l’écran de Message de rapport, passez en revue et modifier les paramètres comme il convient pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="92b05-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Complément de paramètres pour le Message d’état](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="92b05-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b05-193">Related topics</span></span>

[<span data-ttu-id="92b05-194">Utiliser le complément de Message de rapport</span><span class="sxs-lookup"><span data-stu-id="92b05-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="92b05-195">Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="92b05-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="92b05-196">Afficher les rapports de Protection de menace avancées d’Office 365</span><span class="sxs-lookup"><span data-stu-id="92b05-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="92b05-197">Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="92b05-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

