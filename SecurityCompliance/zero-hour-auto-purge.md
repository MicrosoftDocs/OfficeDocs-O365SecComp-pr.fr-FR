---
title: Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
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
ms.openlocfilehash: ac181a7c57b4b16a952ff9c046edbff1380828d1
ms.sourcegitcommit: 791d23e1c2dea622b6ef77a6e2bde32e1d31a41b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999973"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="df578-104">Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="df578-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="df578-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="df578-105">Overview</span></span>

<span data-ttu-id="df578-p102">Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.</span><span class="sxs-lookup"><span data-stu-id="df578-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="df578-108">ZAP est disponible avec la valeur par défaut Exchange Online Protection est fourni avec un abonnement à Office 365 qui contient les boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="df578-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="df578-109">ZAP est activée par défaut, mais les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="df578-109">ZAP is turned on by default, but the folowing conditions must be met:</span></span>
  
- <span data-ttu-id="df578-110">**Action du courrier indésirable** est défini sur **déplacer le message vers le dossier courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="df578-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="df578-111">Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s’applique uniquement à un ensemble d’utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres à être filtré par ZAP.</span><span class="sxs-lookup"><span data-stu-id="df578-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="df578-p103">Les utilisateurs ont conservé leur valeur par défaut des paramètres de courrier indésirable et n’ont pas activé la protection contre le courrier indésirable. (Pour plus d’informations sur les options de l’utilisateur dans Outlook, voir [Modifier le niveau de protection dans le filtre de courrier indésirable](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .)</span><span class="sxs-lookup"><span data-stu-id="df578-p103">Users have kept their default junk mail settings, and have not turned off junk email protection. (See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="df578-114">Comment fonctionne la ZAP ?</span><span class="sxs-lookup"><span data-stu-id="df578-114">How does ZAP work?</span></span>

<span data-ttu-id="df578-p104">Met à jour les signatures de moteur et des programmes malveillants contre le courrier indésirable dans Office 365 en temps réel au quotidien. Toutefois, les utilisateurs peuvent encore avoir malveillants messages remis dans leur boîte de réception pour plusieurs raisons, notamment si le contenu est weaponized après avoir fourni aux utilisateurs. SUPPRIMER les adresses de cette en surveillant en permanence des mises à jour pour les signatures de courrier indésirable et les programmes malveillants Office 365. ZAP permettre rechercher et supprimer des messages livrés qui figurent déjà dans la boîte de réception des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df578-p104">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures. ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 
- <span data-ttu-id="df578-119">Pour le courrier électronique identifié comme courrier indésirable, ZAP déplace les messages non lus pour le dossier de courrier indésirable des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="df578-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 
- <span data-ttu-id="df578-120">Pour les logiciels malveillants nouvellement détecté, ZAP supprime les pièces jointes des messages électroniques, quelle que soit ou non le courrier électronique a été lu.</span><span class="sxs-lookup"><span data-stu-id="df578-120">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="df578-121">L’action ZAP est transparente pour l’utilisateur de boîte aux lettres ; ils ne sont pas avertis si un message électronique est déplacé.</span><span class="sxs-lookup"><span data-stu-id="df578-121">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="df578-122">Autoriser les listes, [les règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l’utilisateur final ou des filtres supplémentaires sont prioritaires sur ZAP.</span><span class="sxs-lookup"><span data-stu-id="df578-122">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="df578-123">Pour vérifier ou configurer une stratégie de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="df578-123">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="df578-124">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="df578-124">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>
2. <span data-ttu-id="df578-125">Sous **Gestion des menaces**, choisissez le **blocage du courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="df578-125">Under **Threat management**, choose **Anti-spam**.</span></span>
3. <span data-ttu-id="df578-126">Passez en revue les paramètres standards.</span><span class="sxs-lookup"><span data-stu-id="df578-126">Review the standard settings.</span></span> 
4. <span data-ttu-id="df578-p105">Si vous souhaitez personnaliser vos paramètres, sélectionnez l’onglet **personnalisé** et activer **les paramètres personnalisés**. Modifier vos paramètres et si vous le souhaitez, choisissez **+ créer une stratégie** pour ajouter une nouvelle stratégie.</span><span class="sxs-lookup"><span data-stu-id="df578-p105">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**. Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="df578-129">Pour voir si ZAP déplacé votre message</span><span class="sxs-lookup"><span data-stu-id="df578-129">To see if ZAP moved your message</span></span>

<span data-ttu-id="df578-130">Si vous souhaitez voir si ZAP déplacé votre message, vous pouvez utiliser le [rapport d’état de Protection de menace](view-email-security-reports.md#threat-protection-status-report-new) (ou du [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="df578-130">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report-new) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="df578-131">Pour désactiver ZAP</span><span class="sxs-lookup"><span data-stu-id="df578-131">To disable ZAP</span></span>
  
<span data-ttu-id="df578-132">Si vous souhaitez désactiver supprimer pour votre client Office 365, ou un ensemble d’utilisateurs, utilisez le paramètre **ZapEnabled** de [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.</span><span class="sxs-lookup"><span data-stu-id="df578-132">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="df578-133">Dans l’exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée « Test ».</span><span class="sxs-lookup"><span data-stu-id="df578-133">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="df578-134">FAQ</span><span class="sxs-lookup"><span data-stu-id="df578-134">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="df578-135">Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="df578-135">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="df578-p106">Vous devez suivre le processus de création de rapports normal de faux positifs. La seule raison pour laquelle le message est déplacé vers le dossier courrier indésirable à partir de la boîte de réception serait parce que le service a déterminé que le message a été le courrier indésirable ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="df578-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="df578-138">Que se passe-t-il si utiliser la mise en quarantaine Office 365 au lieu du dossier courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="df578-138">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="df578-139">ZAP ne déplacer des messages en quarantaine à partir de la boîte de réception à ce stade.</span><span class="sxs-lookup"><span data-stu-id="df578-139">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="df578-140">Que se passe-t-il si j’ai une règle de flux de messagerie personnalisé (bloquer / règle Autoriser) ?</span><span class="sxs-lookup"><span data-stu-id="df578-140">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="df578-p107">Règles créées par des administrateurs (règles de flux de messagerie) ou bloquer et autoriser les règles sont prioritaires. Ces messages sont exclues les critères de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="df578-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="df578-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df578-143">Related Topics</span></span>

[<span data-ttu-id="df578-144">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="df578-144">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="df578-145">Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs</span><span class="sxs-lookup"><span data-stu-id="df578-145">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

