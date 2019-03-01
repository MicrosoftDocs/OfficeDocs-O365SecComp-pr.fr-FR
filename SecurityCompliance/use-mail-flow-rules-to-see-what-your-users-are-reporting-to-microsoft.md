---
title: Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
ms.collection:
- M365-security-compliance
description: Vous pouvez créer une règle de flux de messagerie Exchange pour empêcher vos utilisateurs d'envoyer des messages électroniques à Microsoft à des fins d'analyse et de les utiliser dans vos propres processus de sécurité.
ms.openlocfilehash: e93c90074ad2d143a964b928d8e868bee24acba2
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341165"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="776c3-103">Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft</span><span class="sxs-lookup"><span data-stu-id="776c3-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="776c3-p101">Il existe plusieurs façons d'envoyer des messages faux positifs et faux négatifs à Microsoft pour analyse. En tant qu'administrateur, vous pouvez utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs signalent à Microsoft comme courrier indésirable, non-courrier indésirable et hameçonnage. Pour plus d'informations, consultez la rubrique soumettre des courriers indésirables, des courriers indésirables [et des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). À l'inverse, vous pouvez créer une règle de flux de messagerie Exchange (également appelée règle de transport) pour empêcher vos utilisateurs d'envoyer des messages électroniques à Microsoft à des fins d'analyse et de les utiliser dans vos propres processus de sécurité.</span><span class="sxs-lookup"><span data-stu-id="776c3-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange mail flow rule (also known as a transport rule) to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="776c3-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="776c3-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="776c3-109">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="776c3-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="776c3-p102">Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée «règles de flux de messagerie» dans la rubrique [stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) et l'entrée «stratégies de boîte aux lettres Outlook sur le Web» dans la rubrique [clients and Mobile](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) Devices Permissions.</span><span class="sxs-lookup"><span data-stu-id="776c3-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Mail flow rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook on the web mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="776c3-112">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="776c3-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="776c3-113">Utiliser le CAE pour créer une règle de flux de messagerie afin d'afficher le courrier signalé comme indésirable, comme hameçonnage et comme non indésirable par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="776c3-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="776c3-114">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="776c3-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="776c3-115">Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.</span><span class="sxs-lookup"><span data-stu-id="776c3-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="776c3-116">Nommez la règle, puis cliquez sur **Autres options**.</span><span class="sxs-lookup"><span data-stu-id="776c3-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="776c3-117">Sous **Appliquer cette règle si**, sélectionnez **Le destinataire**, puis **l'adresse comprend l'un des mots suivants**.</span><span class="sxs-lookup"><span data-stu-id="776c3-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="776c3-118">Dans la zone **spécifier des mots ou des expressions**, effectuez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="776c3-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="776c3-p103">Tapez `abuse@messaging.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis tapez `junk@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Ces adresses de messagerie sont utilisées pour envoyer des messages faux négatifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="776c3-p103">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="776c3-p104">Tapez `phish@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Cette adresse de messagerie est utilisée pour envoyer les messages hameçons manqués à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="776c3-p104">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="776c3-p105">Tapez `false_positive@messaging.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis tapez `not_junk@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Ces adresses de messagerie sont utilisées pour envoyer des messages faux positifs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="776c3-p105">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="776c3-125">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="776c3-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="776c3-126">Sous **Effectuer les opérations suivantes**, sélectionnez **Envoyer le message en Cci vers...**, puis sélectionnez les boîtes aux lettres où vous voulez recevoir les messages.</span><span class="sxs-lookup"><span data-stu-id="776c3-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="776c3-p106">Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d'autres sélections. Nous vous recommandons de tester la règle pendant une période avant de l'appliquer. Voir [les procédures pour les règles de flux de messagerie](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="776c3-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="776c3-p107">Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles.</span><span class="sxs-lookup"><span data-stu-id="776c3-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="776c3-132">Une fois la règle créée et appliquée, tous les messages envoyés à partir de votre organisation aux adresses de messagerie spécifiées seront copiés vers la boîte aux lettres spécifiée.</span><span class="sxs-lookup"><span data-stu-id="776c3-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

