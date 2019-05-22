---
title: Expéditeur non vérifié
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.
ms.openlocfilehash: 92458a93a4da3e449061e4d2a4ba312d635c42cc
ms.sourcegitcommit: 7f00f765e8fa674ce1c8c66f5b89b6bea45e13ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2019
ms.locfileid: "34341622"
---
# <a name="unverified-sender"></a><span data-ttu-id="4cb13-103">Expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="4cb13-103">Unverified Sender</span></span>

<span data-ttu-id="4cb13-104">Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4cb13-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cb13-105">Lorsqu’un message est marqué comme frauduleux de hameçonnage, Outlook.com et Outlook sur le Web affichent un avertissement en haut de la page, mais vous pouvez toujours ouvrir les liens figurant dans le message.</span><span class="sxs-lookup"><span data-stu-id="4cb13-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="4cb13-106">Comment puis-je identifier un message suspect dans ma boîte de réception?</span><span class="sxs-lookup"><span data-stu-id="4cb13-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="4cb13-107">Outlook.com et Outlook sur le Web affichent des indicateurs lorsque l’expéditeur d’un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l’adresse de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4cb13-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="4cb13-108">Comment gérer les messages qui reçoivent le traitement de l’expéditeur non vérifié</span><span class="sxs-lookup"><span data-stu-id="4cb13-108">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="4cb13-109">Si vous êtes un client Office 365, vous pouvez gérer cette fonctionnalité via le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="4cb13-109">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="4cb13-110">Dans le centre de sécurité & de la sécurité d’Office 365, les administrateurs du client peuvent activer ou désactiver la fonctionnalité de protection contre l’usurpation d’identité dans le cadre de la stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4cb13-110">In the Office 365 Security & Compliance Center, tenant admins can turn the feature on, or off, through the Anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="4cb13-111">En outre, elle peut être gérée via la cmdlet «Set-Antiphishpolicy permet».</span><span class="sxs-lookup"><span data-stu-id="4cb13-111">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="4cb13-112">Pour plus d’informations, consultez la rubrique anti-phishing protection in Office 365 et Set-Antiphishpolicy permet.</span><span class="sxs-lookup"><span data-stu-id="4cb13-112">For more details, see Anti-phishing protection in Office 365 and Set-AntiPhishPolicy.</span></span>

    ![Modification des expéditeurs non authentifiés dans l’interface graphique.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="4cb13-114">Si un administrateur a identifié un faux positif et qu’un expéditeur ne doit pas recevoir le traitement de l’expéditeur non vérifié, il peut effectuer l’une des actions suivantes pour ajouter l’expéditeur à la liste des usurpations d’identité usurpée:</span><span class="sxs-lookup"><span data-stu-id="4cb13-114">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="4cb13-115">Ajoutez la paire de domaines par le biais de la vue d’aide à la décision.</span><span class="sxs-lookup"><span data-stu-id="4cb13-115">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="4cb13-116">Pour plus d’informations, voir procédure pas à pas: usurpation d’information</span><span class="sxs-lookup"><span data-stu-id="4cb13-116">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="4cb13-117">Ajoutez la paire de domaines via l’applet de commande PhishFilterPolicy.</span><span class="sxs-lookup"><span data-stu-id="4cb13-117">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="4cb13-118">Pour plus d’informations, voir Set-PhishFilterPolicy et protection contre la falsification dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4cb13-118">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="4cb13-119">En outre, nous n’appliquons pas le traitement de l’expéditeur non vérifié s’il a été remis à la boîte de réception via une liste verte d’administration, y compris les règles de transport de messagerie (ETR), la liste des domaines approuvés (stratégie anti-spam), la liste des expéditeurs approuvés ou un utilisateur a défini cet utilisateur comme «expéditeur approuvé» dans son utilitaire.</span><span class="sxs-lookup"><span data-stu-id="4cb13-119">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="4cb13-120">Un «?» apparaît dans l’image de l’expéditeur</span><span class="sxs-lookup"><span data-stu-id="4cb13-120">You see a '?' in the sender image</span></span>

<span data-ttu-id="4cb13-121">Lorsque Outlook.com et Outlook sur le Web ne peuvent pas vérifier l’identité de l’expéditeur à l’aide des techniques d’authentification de messagerie, ils affichent un «?» dans la photo de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4cb13-121">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![Le message n’a pas passé la vérification](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="4cb13-123">Les messages qui ne parvient pas à s’authentifier ne sont pas tous malveillants.</span><span class="sxs-lookup"><span data-stu-id="4cb13-123">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="4cb13-124">Toutefois, vous devez être prudent quant à l’interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4cb13-124">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="4cb13-125">Ou, si vous reconnaissez un expéditeur qui ne possède pas de «?» normalement dans l’image de l’expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l’expéditeur est usurpé.</span><span class="sxs-lookup"><span data-stu-id="4cb13-125">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="4cb13-126">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="4cb13-126">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="4cb13-127">Quels critères les Outlook.com et Outlook sur le Web utilisent-ils pour ajouter les propriétés «?» et «via»?</span><span class="sxs-lookup"><span data-stu-id="4cb13-127">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="4cb13-128">Pour le «?» de l’image de l’expéditeur: Outlook.com requiert que le message passe l’authentification SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="4cb13-128">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="4cb13-129">Pour plus d’informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="4cb13-129">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="4cb13-130">Pour la balise via: si le domaine de l’adresse de l’expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l’un de ces deux champs (en préférant la signature DKIM).</span><span class="sxs-lookup"><span data-stu-id="4cb13-130">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the-"></a><span data-ttu-id="4cb13-131">Comment supprimer le «?»?</span><span class="sxs-lookup"><span data-stu-id="4cb13-131">How do I remove the '?'</span></span>

<span data-ttu-id="4cb13-132">Pour le «?» de l’image de l’expéditeur: en tant qu’expéditeur, vous devez authentifier votre message avec SPF ou DKIM.</span><span class="sxs-lookup"><span data-stu-id="4cb13-132">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="4cb13-133">Pour la balise via: en tant qu’expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l’adresse de provenance ou qu’il s’agit d’un sous-domaine de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4cb13-133">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="4cb13-134">Est-ce que Outlook.com et Outlook sur le Web s’affichent pour chaque message qui ne passe pas l’authentification?</span><span class="sxs-lookup"><span data-stu-id="4cb13-134">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="4cb13-135">Pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="4cb13-135">Not necessarily.</span></span> <span data-ttu-id="4cb13-136">Outlook.com et Outlook sur le Web peuvent avoir d’autres propriétés dans le message pour authentifier l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="4cb13-136">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cb13-137">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="4cb13-137">Related topics</span></span>

[<span data-ttu-id="4cb13-138">Protéger votre compte de messagerie Outlook.com</span><span class="sxs-lookup"><span data-stu-id="4cb13-138">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="4cb13-139">Gérer les abus, le hameçonnage ou l’usurpation d’identité dans Outlook.com</span><span class="sxs-lookup"><span data-stu-id="4cb13-139">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="4cb13-140">Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="4cb13-140">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
