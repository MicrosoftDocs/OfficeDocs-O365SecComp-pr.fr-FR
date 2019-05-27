---
title: 'Purge automatique zéro heure : protection contre le courrier indésirable et les programmes malveillants'
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/11/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: La suppression automatique de zéro heure (ZAP) est une fonctionnalité de protection de la messagerie qui détecte les messages contenant du courrier indésirable ou des programmes malveillants qui ont déjà été remis dans la boîte de réception de vos utilisateurs, puis rend le contenu malveillant inoffensif. Le mode de fonctionnement de ZAP dépend du type de contenu malveillant détecté.
ms.openlocfilehash: e6faef4c123ea2db38a27b49ff0ee49b237ec75c
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408349"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="edb9b-104">Purge automatique zéro heure : protection contre le courrier indésirable et les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="edb9b-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="edb9b-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="edb9b-105">Overview</span></span>

<span data-ttu-id="edb9b-106">La suppression automatique de zéro heure (ZAP) est une fonctionnalité de protection de la messagerie qui détecte les messages contenant des messages hameçons, des courriers indésirables ou des programmes malveillants qui ont déjà été remis dans la boîte de réception de vos utilisateurs, puis rend le contenu malveillant inoffensif.</span><span class="sxs-lookup"><span data-stu-id="edb9b-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="edb9b-107">Le mode de fonctionnement de ZAP dépend du type de contenu malveillant détecté; les messages peuvent être zapped en raison du contenu, des URL ou des pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="edb9b-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="edb9b-108">ZAP est disponible avec la protection Exchange Online par défaut incluse avec tout abonnement Office 365 qui contient des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="edb9b-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="edb9b-109">L’option ZAP est activée par défaut, mais les conditions suivantes doivent être remplies:</span><span class="sxs-lookup"><span data-stu-id="edb9b-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="edb9b-110">L' **action de courrier** indésirable est définie sur déplacer le **message vers le dossier**courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="edb9b-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <span data-ttu-id="edb9b-111">Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s’applique uniquement à un ensemble d’utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres soient filtrées par la méthode ZAP.</span><span class="sxs-lookup"><span data-stu-id="edb9b-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="edb9b-112">Les utilisateurs ont conservé leurs paramètres de courrier indésirable par défaut et n’ont pas désactivé la protection contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="edb9b-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="edb9b-113">(Pour plus d’informations sur les options utilisateur dans Outlook, consultez [la rubrique modifier le niveau de protection dans le filtre Courrier](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) indésirable.)</span><span class="sxs-lookup"><span data-stu-id="edb9b-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-zap-works"></a><span data-ttu-id="edb9b-114">Fonctionnement de l’ZAP</span><span class="sxs-lookup"><span data-stu-id="edb9b-114">How ZAP works</span></span>

<span data-ttu-id="edb9b-115">Office 365 met à jour quotidiennement les signatures du moteur de blocage du courrier indésirable et des programmes malveillants en temps réel.</span><span class="sxs-lookup"><span data-stu-id="edb9b-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="edb9b-116">Toutefois, vos utilisateurs peuvent toujours recevoir des messages malveillants dans leur boîte de réception pour diverses raisons, notamment si le contenu est arme après remise aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="edb9b-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="edb9b-117">ZAP les résout en surveillant en continu les mises à jour des signatures Office 365 courrier indésirable et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="edb9b-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="edb9b-118">ZAP peut rechercher et supprimer les messages précédemment remis qui se trouvent déjà dans les boîtes de réception des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="edb9b-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span>

- <span data-ttu-id="edb9b-119">Pour les messages identifiés comme courrier indésirable, la méthode ZAP déplace les messages non lus dans le dossier courrier indésirable des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="edb9b-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span>

- <span data-ttu-id="edb9b-120">Pour les messages identifiés comme hameçonnage, la méthode ZAP déplace les messages vers le dossier courrier indésirable des utilisateurs, que l’e-mail ait été lu ou non.</span><span class="sxs-lookup"><span data-stu-id="edb9b-120">For mail that is identified as phish, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="edb9b-121">Pour les programmes malveillants nouvellement détectés, ZAP supprime les pièces jointes des messages électroniques, que l’e-mail ait été lu ou non.</span><span class="sxs-lookup"><span data-stu-id="edb9b-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span>
  
<span data-ttu-id="edb9b-122">L’action ZAP est transparente pour l’utilisateur de boîte aux lettres; elles ne sont pas notifiées en cas de déplacement d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="edb9b-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span> <span data-ttu-id="edb9b-123">Le message ne doit pas être âgé de plus de 2 jours.</span><span class="sxs-lookup"><span data-stu-id="edb9b-123">Message must not be older than 2 days.</span></span>
  
<span data-ttu-id="edb9b-124">Les listes d’autorisation, les [règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l’utilisateur final ou les filtres supplémentaires prévalent sur zap.</span><span class="sxs-lookup"><span data-stu-id="edb9b-124">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="edb9b-125">Pour examiner ou configurer une stratégie de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="edb9b-125">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="edb9b-126">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="edb9b-126">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="edb9b-127">Sous **gestion des menaces**, sélectionnez **blocage du courrier**indésirable.</span><span class="sxs-lookup"><span data-stu-id="edb9b-127">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="edb9b-128">Passez en revue les paramètres standard.</span><span class="sxs-lookup"><span data-stu-id="edb9b-128">Review the standard settings.</span></span>

4. <span data-ttu-id="edb9b-129">Si vous souhaitez personnaliser vos paramètres, sélectionnez l’onglet **personnalisé** et activez **paramètres personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="edb9b-129">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**.</span></span> <span data-ttu-id="edb9b-130">Modifiez vos paramètres et, si vous le souhaitez, cliquez sur **+ créer une stratégie** pour ajouter une nouvelle stratégie.</span><span class="sxs-lookup"><span data-stu-id="edb9b-130">Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span>

## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="edb9b-131">Pour savoir si ZAP a déplacé votre message</span><span class="sxs-lookup"><span data-stu-id="edb9b-131">To see if ZAP moved your message</span></span>

<span data-ttu-id="edb9b-132">Si vous voulez savoir si ZAP a déplacé votre message, vous pouvez utiliser le [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report) [(et les détections en temps réel)](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="edb9b-132">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) or [Threat Explorer (and real-time detections)](threat-explorer.md).</span></span>

## <a name="to-disable-zap"></a><span data-ttu-id="edb9b-133">Pour désactiver ZAP</span><span class="sxs-lookup"><span data-stu-id="edb9b-133">To disable ZAP</span></span>
  
<span data-ttu-id="edb9b-134">Si vous souhaitez désactiver ZAP pour votre client 365 Office ou un ensemble d’utilisateurs, utilisez le paramètre **ZapEnabled** de la cmdlet [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.</span><span class="sxs-lookup"><span data-stu-id="edb9b-134">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>

<span data-ttu-id="edb9b-135">Dans l’exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée «test».</span><span class="sxs-lookup"><span data-stu-id="edb9b-135">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="edb9b-136">FAQ</span><span class="sxs-lookup"><span data-stu-id="edb9b-136">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="edb9b-137">Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable?</span><span class="sxs-lookup"><span data-stu-id="edb9b-137">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="edb9b-138">Vous devez suivre le processus de création de rapports normal pour les [faux positifs](prevent-email-from-being-marked-as-spam.md).</span><span class="sxs-lookup"><span data-stu-id="edb9b-138">You should follow the normal reporting process for [false-positives](prevent-email-from-being-marked-as-spam.md).</span></span> <span data-ttu-id="edb9b-139">La seule raison pour laquelle le message est déplacé de la boîte de réception vers le dossier de courrier indésirable est que le service a déterminé que le message était du courrier indésirable ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="edb9b-139">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="edb9b-140">Que faire en cas d’utilisation de la mise en quarantaine Office 365 au lieu du dossier courrier indésirable?</span><span class="sxs-lookup"><span data-stu-id="edb9b-140">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="edb9b-141">ZAP ne déplace pas les messages en quarantaine dans la boîte de réception pour le moment.</span><span class="sxs-lookup"><span data-stu-id="edb9b-141">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="edb9b-142">Que se passe-t-il si j’utilise une règle de flux de messagerie personnalisée (règle bloquer/autoriser)?</span><span class="sxs-lookup"><span data-stu-id="edb9b-142">What if I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="edb9b-143">Les règles créées par les administrateurs (règles de flux de messagerie) ou les règles de blocage et d’autorisation sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="edb9b-143">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="edb9b-144">Ces messages sont exclus des critères de fonctionnalité de sorte que le flux de messagerie suit l’action de la règle (règle bloquer/autoriser).</span><span class="sxs-lookup"><span data-stu-id="edb9b-144">Such messages are excluded from the feature criteria so the mail flow will follow the rule action (Block/Allow Rule).</span></span>

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rule"></a><span data-ttu-id="edb9b-145">Que se passe-t-il si un message est déplacé vers un autre dossier (par exemple, la règle de boîte de réception)?</span><span class="sxs-lookup"><span data-stu-id="edb9b-145">What if a message is moved to another folder (e.g. Inbox rule)?</span></span>
<span data-ttu-id="edb9b-146">ZAP fonctionne toujours dans ce cas, sauf si le message a été supprimé ou se trouve dans un courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="edb9b-146">ZAP still works in this case, unless the message has been deleted or is in Junk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edb9b-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edb9b-147">Related Topics</span></span>

[<span data-ttu-id="edb9b-148">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="edb9b-148">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="edb9b-149">Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs</span><span class="sxs-lookup"><span data-stu-id="edb9b-149">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)
