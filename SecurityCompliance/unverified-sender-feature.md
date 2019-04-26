---
title: Identifier les messages suspects dans Outlook.com et Outlook sur le Web
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Pour empêcher les messages de hameçonnage d'atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l'expéditeur est bien ce qu'il dit, et marquez les messages suspects comme courrier indésirable.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345894"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a><span data-ttu-id="7b525-103">Identifier les messages suspects dans Outlook.com et Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7b525-103">Identify suspicious messages in Outlook.com and Outlook on the web</span></span>

<span data-ttu-id="7b525-104">Pour empêcher les messages de hameçonnage d'atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l'expéditeur est bien ce qu'il dit, et marquez les messages suspects comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7b525-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b525-105">Lorsqu'un message est marqué comme frauduleux de hameçonnage, Outlook.com et Outlook sur le Web affichent un avertissement en haut de la page, mais vous pouvez toujours ouvrir les liens figurant dans le message.</span><span class="sxs-lookup"><span data-stu-id="7b525-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="7b525-106">Comment puis-je identifier un message suspect dans ma boîte de réception?</span><span class="sxs-lookup"><span data-stu-id="7b525-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="7b525-107">Outlook.com et Outlook sur le Web affichent des indicateurs lorsque l'expéditeur d'un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l'adresse de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7b525-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="7b525-108">Un «?» apparaît dans l'image de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="7b525-108">You see a '?' in the sender image</span></span>

<span data-ttu-id="7b525-109">Lorsque Outlook.com et Outlook sur le Web ne peuvent pas vérifier l'identité de l'expéditeur à l'aide des techniques d'authentification de messagerie, ils affichent un «?» dans la photo de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7b525-109">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span>

![Le message n'a pas passé la vérification](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="7b525-111">Les messages qui ne parvient pas à s'authentifier ne sont pas tous malveillants.</span><span class="sxs-lookup"><span data-stu-id="7b525-111">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="7b525-112">Toutefois, vous devez être prudent quant à l'interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7b525-112">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="7b525-113">Ou, si vous reconnaissez un expéditeur qui ne possède pas de «?» normalement dans l'image de l'expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l'expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="7b525-113">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a><span data-ttu-id="7b525-114">L'adresse de l'expéditeur est différente de celle qui apparaît dans l'adresse de l'expéditeur</span><span class="sxs-lookup"><span data-stu-id="7b525-114">The sender's address is different than what appears in the From address</span></span>

<span data-ttu-id="7b525-115">Bien souvent, l'adresse de messagerie que vous voyez dans un message est différente de celle que vous voyez dans l'adresse de l'adresse.</span><span class="sxs-lookup"><span data-stu-id="7b525-115">Frequently, the email address you see in a message is different than what you see in the From address.</span></span> <span data-ttu-id="7b525-116">Parfois, les auteurs de phishing essaient de vous tromper en pensant que l'expéditeur est une personne qui n'est pas vraiment.</span><span class="sxs-lookup"><span data-stu-id="7b525-116">Sometimes phishers try to trick you into thinking that the sender is someone other than who they really are.</span></span>

<span data-ttu-id="7b525-117">Lorsque Outlook.com et Outlook sur le Web détectent une différence entre l'adresse réelle de l'expéditeur et l'adresse de l'adresse de, ils affichent l'expéditeur réel à l'aide de la balise via, qui est soulignée.</span><span class="sxs-lookup"><span data-stu-id="7b525-117">When Outlook.com and Outlook on the web detect a difference between the sender's actual address and the address on the From address, they show the actual sender using the via tag, which will be underlined.</span></span>

![texte de remplacement de l'expéditeur non vérifié](media/unverified-sender-feature1.png)

<span data-ttu-id="7b525-119">Dans cet exemple, le domaine `suspicious.com` d'envoi est authentifié, mais celui-ci est `unknown@contoso.com` placé dans l'adresse de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7b525-119">In this example, the sending domain `suspicious.com` is authenticated, but the sender put `unknown@contoso.com` in the From address.</span></span>

<span data-ttu-id="7b525-120">Tous les messages avec une balise via ne sont pas suspects.</span><span class="sxs-lookup"><span data-stu-id="7b525-120">Not every message with a via tag is suspicious.</span></span> <span data-ttu-id="7b525-121">Toutefois, si vous ne reconnaissez pas un message avec une balise via, soyez prudent lors de l'interaction avec celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7b525-121">However, if you don't recognize a message with a via tag, you should be cautious about interacting with it.</span></span>

<span data-ttu-id="7b525-122">Dans Outlook.com et le nouveau Outlook sur le Web, vous pouvez placer le curseur sur le nom ou l'adresse de l'expéditeur dans la liste des messages pour voir son adresse de messagerie, sans avoir à ouvrir le message.</span><span class="sxs-lookup"><span data-stu-id="7b525-122">In Outlook.com and the new Outlook on the web, you can hover your cursor over a sender's name or address in the message list to see their email address, without needing to open the message.</span></span>

![Prise en main de OneDrive](media/get-started-with-onedrive-message.png)

<span data-ttu-id="7b525-124">Comment savoir si vous utilisez le nouveau Outlook sur le Web?</span><span class="sxs-lookup"><span data-stu-id="7b525-124">How do you know if you're using the new Outlook on the web?</span></span> <span data-ttu-id="7b525-125">Consultez les exemples suivants:</span><span class="sxs-lookup"><span data-stu-id="7b525-125">See the following examples:</span></span>

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="7b525-127">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="7b525-127">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="7b525-128">Quels critères les Outlook.com et Outlook sur le Web utilisent-ils pour ajouter les propriétés «?» et «via»?</span><span class="sxs-lookup"><span data-stu-id="7b525-128">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="7b525-129">Pour le «?» de l'image de l'expéditeur: Outlook.com requiert que le message passe l'authentification SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="7b525-129">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="7b525-130">Pour plus d'informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l'usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="7b525-130">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="7b525-131">Pour la balise via: si le domaine de l'adresse de l'expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l'un de ces deux champs (en préférant la signature DKIM).</span><span class="sxs-lookup"><span data-stu-id="7b525-131">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a><span data-ttu-id="7b525-132">Puis-je remplacer ces propriétés par le biais de l'IP autorisé, la règle de transport Exchange autorise ou les expéditeurs approuvés?</span><span class="sxs-lookup"><span data-stu-id="7b525-132">Can I override these properties with IP Allows, Exchange Transport Rule Allows, or safe senders?</span></span>

<span data-ttu-id="7b525-133">Vous ne pouvez pas remplacer ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b525-133">You can't override these properties.</span></span>

### <a name="how-do-i-remove-these-properties"></a><span data-ttu-id="7b525-134">Comment puis-je supprimer ces propriétés?</span><span class="sxs-lookup"><span data-stu-id="7b525-134">How do I remove these properties?</span></span>

<span data-ttu-id="7b525-135">Pour le «?» de l'image de l'expéditeur: en tant qu'expéditeur, vous devez authentifier votre message avec SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="7b525-135">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="7b525-136">Pour la balise via: en tant qu'expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l'adresse de provenance ou qu'il s'agit d'un sous-domaine de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7b525-136">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="7b525-137">Est-ce que Outlook.com et Outlook sur le Web s'affichent pour chaque message qui ne passe pas l'authentification?</span><span class="sxs-lookup"><span data-stu-id="7b525-137">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="7b525-138">Pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="7b525-138">Not necessarily.</span></span> <span data-ttu-id="7b525-139">Outlook.com et Outlook sur le Web peuvent avoir d'autres propriétés dans le message pour authentifier l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7b525-139">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b525-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b525-140">Related topics</span></span>

[<span data-ttu-id="7b525-141">Protéger votre compte de messagerie Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7b525-141">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="7b525-142">Gérer les abus, le hameçonnage ou l'usurpation d'identité dans Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7b525-142">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="7b525-143">Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7b525-143">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
