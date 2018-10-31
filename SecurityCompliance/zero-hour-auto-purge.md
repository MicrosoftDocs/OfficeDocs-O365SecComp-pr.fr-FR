---
title: Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857242"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="d4d04-104">Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="d4d04-104">Zero-hour auto purge - protection against spam and malware</span></span>

<span data-ttu-id="d4d04-p102">Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="d4d04-107">ZAP est disponible avec la valeur par défaut Exchange Online Protection est fourni avec un abonnement à Office 365 qui contient les boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d4d04-107">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>
  
## <a name="how-does-zap-work"></a><span data-ttu-id="d4d04-108">Comment fonctionne la ZAP ?</span><span class="sxs-lookup"><span data-stu-id="d4d04-108">How does ZAP work?</span></span>

<span data-ttu-id="d4d04-p103">Met à jour les signatures de moteur et des programmes malveillants contre le courrier indésirable dans Office 365 en temps réel au quotidien. Toutefois, les utilisateurs peuvent encore avoir des messages remis à leurs boîtes aux lettres pour différentes raisons, y compris lorsque le contenu a été weaponized une fois qu’il a été remis tout d’abord aux utilisateurs malveillants. SUPPRIMER les adresses cela en surveillant en permanence des mises à jour pour les signatures de courrier indésirable et les programmes malveillants Office 365, et peut par conséquent rechercher et supprimer des messages remis précédemment déjà dans la boîte de réception. Pour le courrier électronique qui a été déjà identifié comme courrier indésirable, ZAP déplace les messages non lus pour le dossier de courrier indésirable de l’utilisateur. Pour les logiciels malveillants nouvellement détecté, ZAP supprime les pièces jointes à partir du message électronique, quelle que soit la si le message a été lu ou non. L’inverse est vrai pour les messages qui ont été incorrectement classés comme malveillants.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p103">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including when the content was weaponized at a time after it was first delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures, and can therefore find and remove previously delivered messages already in inboxes. For mail that was already identified as spam, ZAP moves unread messages to the user's Junk mail folder. For newly detected malware, ZAP removes the attachments from the email message, regardless of whether the mail was read or not. The reverse is true for messages that were incorrectly classified as malicious.</span></span>
  
<span data-ttu-id="d4d04-115">L’action ZAP est transparente pour l’utilisateur de boîte aux lettres, qu’il n’est pas avertie que le message a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d4d04-115">The ZAP action is seamless for the mailbox user, he or she is not notified the mail has been moved.</span></span>
  
<span data-ttu-id="d4d04-116">Autoriser les listes, [les règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l’utilisateur final ou des filtres supplémentaires sont prioritaires sur ZAP.</span><span class="sxs-lookup"><span data-stu-id="d4d04-116">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
 <span data-ttu-id="d4d04-117">**Contenu de cet article :**</span><span class="sxs-lookup"><span data-stu-id="d4d04-117">**In this article:**</span></span>
  
> [<span data-ttu-id="d4d04-118">Définir la stratégie de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="d4d04-118">Set spam filter policy</span></span>](zero-hour-auto-purge.md#BK_SetSpam)
    
> [<span data-ttu-id="d4d04-119">Voir si ZAP déplacé votre message</span><span class="sxs-lookup"><span data-stu-id="d4d04-119">See if ZAP moved your message</span></span>](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [<span data-ttu-id="d4d04-120">Désactiver ZAP</span><span class="sxs-lookup"><span data-stu-id="d4d04-120">Disable ZAP</span></span>](zero-hour-auto-purge.md#BK_Posh)
    
> [<span data-ttu-id="d4d04-121">FAQ</span><span class="sxs-lookup"><span data-stu-id="d4d04-121">FAQ</span></span>](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a><span data-ttu-id="d4d04-122">Utilisation de ZAP</span><span class="sxs-lookup"><span data-stu-id="d4d04-122">Working with ZAP</span></span>

<span data-ttu-id="d4d04-123">ZAP est activée par défaut, mais vous avez pour vous assurer que les deux conditions sont remplies :</span><span class="sxs-lookup"><span data-stu-id="d4d04-123">ZAP is turned on by default, but you do have to make sure a couple of conditions are met:</span></span>
  
- <span data-ttu-id="d4d04-124">Stratégie de filtrage du courrier indésirable est défini sur [déplacer le message vers le dossier courrier indésirable](zero-hour-auto-purge.md#BK_SetSpam).</span><span class="sxs-lookup"><span data-stu-id="d4d04-124">Spam filter policy is set to [Move message to Junk Email folder](zero-hour-auto-purge.md#BK_SetSpam).</span></span>
    
    <span data-ttu-id="d4d04-125">Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s’applique uniquement à un ensemble d’utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres à être filtré par ZAP.</span><span class="sxs-lookup"><span data-stu-id="d4d04-125">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>
    
- <span data-ttu-id="d4d04-126">L’utilisateur [Options \> courrier indésirable](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span><span class="sxs-lookup"><span data-stu-id="d4d04-126">The user's [Options \> Junk Email](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span></span>
    
<span data-ttu-id="d4d04-127">Si vous souhaitez [voir si ZAP déplacé votre message](zero-hour-auto-purge.md#BK_DidZAPMove), vous pouvez utiliser l’outil de suivi des messages Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d4d04-127">If you want [to see if ZAP moved your message](zero-hour-auto-purge.md#BK_DidZAPMove), you can use the Exchange Online message trace tool.</span></span>
  
<span data-ttu-id="d4d04-128">Administrateurs peuvent également [désactiver ZAP](zero-hour-auto-purge.md#BK_Posh) à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4d04-128">Admins can also [disable ZAP](zero-hour-auto-purge.md#BK_Posh) by using PowerShell.</span></span> 
  
 <span data-ttu-id="d4d04-129">**Pour définir la stratégie de filtrage du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="d4d04-129">**To set spam filter policy**</span></span>
  
1. <span data-ttu-id="d4d04-130">Se connecter à la [permettant de se connecter à Office 365 pour professionnels](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) et choisissez **protection** \> **filtre de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="d4d04-130">Sign in to the [Where to sign in to Office 365 for business](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) and choose **protection** \> **spam filter**.</span></span> 
    
    ![Dans le CAE choisissez protection, puis de filtre de courrier indésirable](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. <span data-ttu-id="d4d04-132">Choisissez la stratégie de filtrage que vous souhaitez ajuster, ou choisissez **Ajouter**![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) pour créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="d4d04-132">Either choose the filter policy you want to adjust, or choose **add**![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) to create a new one.</span></span> 
    
    <span data-ttu-id="d4d04-p104">Dans la capture d’écran précédente, la stratégie est nommée « Default », mais si vous créez des stratégies de filtrage du courrier indésirable supplémentaire vous pouvez leur donner un nom différent. Vous pouvez également appliquer la stratégie à un ensemble limité d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p104">In the previous screen shot, the policy is named "Default", but if you create additional spam filter policies you can give them a different name. You can also apply the policy to only a limited set of users.</span></span>
    
3. <span data-ttu-id="d4d04-135">Dans la fenêtre de la stratégie, choisissez **actions en bloc et de courrier indésirable**et assurez-vous que **le courrier indésirable** est défini sur **déplacer le message vers le dossier courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="d4d04-135">In the policy window, choose **spam and bulk actions**, and make sure that **Spam** is set to **Move message to Junk Email folder**.</span></span> 
    
    <span data-ttu-id="d4d04-136">Si vous choisissez **Enregistrer** à ce stade, la stratégie s’applique à votre organisation cliente Office 365.</span><span class="sxs-lookup"><span data-stu-id="d4d04-136">If you choose **Save** at this point, the policy applies to your Office 365 tenant.</span></span> 
    
    ![Définir les actions en bloc et de courrier indésirable pour déplacer le message vers le dossier courrier indésirable](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. <span data-ttu-id="d4d04-p105">Si vous avez créé une nouvelle stratégie et que vous voulez appliquer la stratégie à un ensemble d’utilisateurs, faites défiler jusqu'à la section **Appliquée à** la fenêtre de filtre de stratégie et dans les contrôles de menu Choisir les **destinataires**, **domaine**ou les **appartenances aux groupes** , vous vous souhaitez appliquer la stratégie. Vous pouvez également définir des exceptions et conditions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p105">If you created a new policy, and you want to apply the policy to only a set of users, scroll to the **Applied To** section in the policy filter window, and in the menu controls choose the **recipients**, **domain**, or **group memberships** you want to apply the policy to. You can also set additional conditions and exceptions.</span></span> 
    
    ![Dans la section appliquée à choisir les destinataires](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    <span data-ttu-id="d4d04-141">Cliquez sur **Enregistrer** pour appliquer la stratégie aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d4d04-141">Choose **Save** to apply the policy to the selected users.</span></span> 
    
 <span data-ttu-id="d4d04-142">**Pour voir si ZAP déplacé votre message**</span><span class="sxs-lookup"><span data-stu-id="d4d04-142">**To see if ZAP moved your message**</span></span>
  
- <span data-ttu-id="d4d04-143">Vous pouvez utiliser [trouver et résoudre les problèmes de remise de courrier électronique comme un Office 365 pour professionnels admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) pour déterminer si le message a été déplacé par ZAP :</span><span class="sxs-lookup"><span data-stu-id="d4d04-143">You can use the [Find and fix email delivery issues as an Office 365 for business admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) to determine if the message was moved by ZAP:</span></span> 
    
    <span data-ttu-id="d4d04-144">Rechercher le texte « heures zéro automatique Purge (ZAP) » dans vos informations de suivi pour identifier un message qui a été déplacé par ZAP.</span><span class="sxs-lookup"><span data-stu-id="d4d04-144">Look for the text "Zero-Hour Auto Purge (ZAP)" in your trace details to identify a message that was moved by ZAP.</span></span>
    
 <span data-ttu-id="d4d04-145">**Pour désactiver ZAP**</span><span class="sxs-lookup"><span data-stu-id="d4d04-145">**To disable ZAP**</span></span>
  
- <span data-ttu-id="d4d04-146">Si vous souhaitez désactiver supprimer pour votre client Office 365, ou un ensemble d’utilisateurs, utilisez le paramètre **ZapEnabled** de [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.</span><span class="sxs-lookup"><span data-stu-id="d4d04-146">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
    <span data-ttu-id="d4d04-147">Dans l’exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée « Test ».</span><span class="sxs-lookup"><span data-stu-id="d4d04-147">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a><span data-ttu-id="d4d04-148">FAQ</span><span class="sxs-lookup"><span data-stu-id="d4d04-148">FAQ</span></span>
<span data-ttu-id="d4d04-149"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="d4d04-149"></span></span>

 <span data-ttu-id="d4d04-150">**Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable ?**</span><span class="sxs-lookup"><span data-stu-id="d4d04-150">**What happens if a legitimate message is moved to the junk mail folder?**</span></span>
  
<span data-ttu-id="d4d04-p106">Vous devez suivre le processus de création de rapports normal de faux positifs. La seule raison pour laquelle le message est déplacé vers le dossier courrier indésirable à partir de la boîte de réception serait parce que le service a déterminé que le message a été le courrier indésirable ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
 <span data-ttu-id="d4d04-153">**Que se passe-t-il si utiliser la mise en quarantaine Office 365 au lieu du dossier courrier indésirable ?**</span><span class="sxs-lookup"><span data-stu-id="d4d04-153">**What if I use the Office 365 quarantine instead of the junk mail folder?**</span></span>
  
<span data-ttu-id="d4d04-154">ZAP ne déplacer des messages en quarantaine à partir de la boîte de réception à ce stade.</span><span class="sxs-lookup"><span data-stu-id="d4d04-154">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
 <span data-ttu-id="d4d04-155">**Que se passe-t-il si j’ai une règle de flux de messagerie personnalisé (bloquer / règle Autoriser) ?**</span><span class="sxs-lookup"><span data-stu-id="d4d04-155">**What If I have a custom mail flow rule (Block/ Allow Rule)?**</span></span>
  
<span data-ttu-id="d4d04-p107">Règles créées par des administrateurs (règles de flux de messagerie) ou bloquer et autoriser les règles sont prioritaires. Ces messages sont exclues les critères de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d4d04-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="d4d04-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d04-158">Related Topics</span></span>
<span data-ttu-id="d4d04-159"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="d4d04-159"></span></span>

[<span data-ttu-id="d4d04-160">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d4d04-160">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="d4d04-161">Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs</span><span class="sxs-lookup"><span data-stu-id="d4d04-161">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

