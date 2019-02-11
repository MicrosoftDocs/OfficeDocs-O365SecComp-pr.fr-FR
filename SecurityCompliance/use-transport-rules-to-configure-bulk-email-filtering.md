---
title: Utiliser les règles de flux de messagerie pour configurer des messages électroniques en masse de filtrage dans Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Administrateurs peuvent apprendre à utiliser les règles de flux de messagerie dans Exchange Online Protection pour le filtrage de courrier électronique en bloc.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382805"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="368d5-103">Utiliser les règles de flux de messagerie pour configurer des messages électroniques en masse de filtrage dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="368d5-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="368d5-p101">Vous pouvez définir des filtres de contenu à l'échelle de l'entreprise pour le courrier indésirable et le courrier en masse à l'aide des stratégies de filtrage de contenu du courrier indésirable par défaut. Consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md) et [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) sur la façon de définir les stratégies de filtrage de contenu.</span><span class="sxs-lookup"><span data-stu-id="368d5-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="368d5-p102">Si vous souhaitez plus d’options pour filtrer les messages en bloc, vous pouvez créer des règles de flux de messagerie (également connu sous les règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvées dans les messages électroniques en masse. Tout message contenant ces caractéristiques sera être marqué comme courrier indésirable. Ces règles permettent de réduire la quantité de courrier indésirable que reçoit votre organisation.</span><span class="sxs-lookup"><span data-stu-id="368d5-p102">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
<span data-ttu-id="368d5-109">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="368d5-109">**Notes**:</span></span>

- <span data-ttu-id="368d5-110">Avant de créer des règles de flux de la messagerie documenté cette rubrique, nous vous recommandons de lire tout d’abord [Quelle est la différence entre courrier indésirable et les messages électroniques en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md) et [valeurs au niveau de réclamation en bloc](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="368d5-110">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
- <span data-ttu-id="368d5-p103">Les procédures suivantes permettent de marquer un message comme indésirable à l'échelle de votre organisation toute entière. Toutefois, vous pouvez ajouter une condition afin de n'appliquer ces règles qu'à des destinataires spécifiques de votre organisation. De cette façon, les paramètres de filtrage restrictif des messages électroniques ne s'appliqueront qu'à quelques utilisateurs particulièrement ciblés et le reste de vos utilisateurs (qui reçoivent en général les messages électroniques en masse auxquels ils se sont inscrits) ne seront pas concernés.</span><span class="sxs-lookup"><span data-stu-id="368d5-p103">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="368d5-114">Créer des règles de flux de messagerie pour filtrer les messages électroniques en masse basés sur les modèles de texte</span><span class="sxs-lookup"><span data-stu-id="368d5-114">Create mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="368d5-115">Dans le Centre d'administration Exchange (CAE), accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="368d5-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="368d5-116">Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="368d5-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="368d5-117">Indiquez le nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="368d5-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="368d5-p104">Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps correspond à ces modèles de texte**.</span><span class="sxs-lookup"><span data-stu-id="368d5-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="368d5-120">Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions régulières suivantes, qui figurent généralement dans les messages électroniques en masse, puis cliquez sur **OK** lorsque vous avez terminé :</span><span class="sxs-lookup"><span data-stu-id="368d5-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="368d5-121">Si vous ne parvenez pas à visualiser le contenu de ce message électronique\, veuillez</span><span class="sxs-lookup"><span data-stu-id="368d5-121">If you are unable to view the content of this email\, please</span></span>
    
   - <span data-ttu-id="368d5-122">\\>(safe )?unsubscribe( here)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="368d5-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
   - <span data-ttu-id="368d5-123">Si vous ne souhaitez plus recevoir de communications comme celle-ci\, veuillez</span><span class="sxs-lookup"><span data-stu-id="368d5-123">If you do not wish to receive further communications like this\, please</span></span>
    
   - <span data-ttu-id="368d5-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="368d5-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
   - <span data-ttu-id="368d5-127">Pour ne plus recevoir ces\s+messages\:http\://</span><span class="sxs-lookup"><span data-stu-id="368d5-127">To stop receiving these\s+emails\:http\://</span></span>
    
   - <span data-ttu-id="368d5-128">Pour annuler l'abonnement à \w+ (e\-?letter|e?-?mail|bulletin d'informations)</span><span class="sxs-lookup"><span data-stu-id="368d5-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
   - <span data-ttu-id="368d5-129">ne( souhaitez)? plus( que)? recevoir \w+ message électronique</span><span class="sxs-lookup"><span data-stu-id="368d5-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
   - <span data-ttu-id="368d5-130">Si vous ne parvenez pas à visualiser le contenu de ce message\, cliquez ici</span><span class="sxs-lookup"><span data-stu-id="368d5-130">If you are unable to view the content of this email\, please click here</span></span>
    
   - <span data-ttu-id="368d5-131">Pour vous assurer que vous recevez (vos offres quotidiennes|nos messages électroniques)\, ajoutez</span><span class="sxs-lookup"><span data-stu-id="368d5-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
   - <span data-ttu-id="368d5-132">Si vous ne souhaitez plus recevoir ces courriers</span><span class="sxs-lookup"><span data-stu-id="368d5-132">If you no longer wish to receive these emails</span></span>
    
   - <span data-ttu-id="368d5-133">pour modifier vos (préférences d'abonnement|préférences ou vous désinscrire)</span><span class="sxs-lookup"><span data-stu-id="368d5-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
   - <span data-ttu-id="368d5-134">cliquez (ici pour|sur le bouton) annuler l'abonnement</span><span class="sxs-lookup"><span data-stu-id="368d5-134">click (here to|the) unsubscribe</span></span>
    
   <span data-ttu-id="368d5-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="368d5-135">**Notes**:</span></span>

   - <span data-ttu-id="368d5-p106">La liste ci-dessus n’est pas un ensemble complet des expressions régulières dans les messages électroniques en masse ; plus d’informations peut être ajouté ou supprimé selon vos besoins. Toutefois, il est un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="368d5-p106">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
   - <span data-ttu-id="368d5-p107">La recherche des mots ou des modèles de texte dans l’objet ou d’autres champs d’en-tête dans le message se produit *une fois que* le message a été décodées du transfert de contenu MIME méthode qui a été utilisé pour transmettre le message entre les serveurs SMTP en texte ASCII binaire de codage. Vous ne pouvez pas utiliser les conditions ou exceptions pour rechercher le texte brut (en règle générale, Base64) codé les valeurs de l’objet ou d’autres champs d’en-tête dans les messages.</span><span class="sxs-lookup"><span data-stu-id="368d5-p107">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="368d5-140">Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="368d5-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="368d5-141">Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="368d5-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="368d5-p108">La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="368d5-p108">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="368d5-145">Si votre action configurée est le message en quarantaine plutôt que d’envoyer à un dossier de courrier indésirable de destinataires, le message est envoyé à la mise en quarantaine administrateur comme une correspondance de règle de flux de messagerie et il ne sera pas disponible dans la quarantaine de l’utilisateur final ou par le biais de l’utilisateur final notifications de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="368d5-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="368d5-146">Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="368d5-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="368d5-147">Enregistrez la règle.</span><span class="sxs-lookup"><span data-stu-id="368d5-147">Save the rule.</span></span>
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="368d5-148">Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des phrases</span><span class="sxs-lookup"><span data-stu-id="368d5-148">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="368d5-149">Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="368d5-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="368d5-150">Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="368d5-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="368d5-151">Indiquez le nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="368d5-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="368d5-p109">Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps inclut l'un de ces mots**.</span><span class="sxs-lookup"><span data-stu-id="368d5-p109">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="368d5-154">Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions suivantes, qui figurent généralement dans les messages électroniques en masse, et cliquez sur **OK** lorsque vous avez terminé :</span><span class="sxs-lookup"><span data-stu-id="368d5-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="368d5-155">pour modifier vos préférences ou annuler votre abonnement</span><span class="sxs-lookup"><span data-stu-id="368d5-155">to change your preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="368d5-156">Modifier les préférences de messagerie ou annuler l'abonnement</span><span class="sxs-lookup"><span data-stu-id="368d5-156">Modify email preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="368d5-157">Ceci est un message promotionnel</span><span class="sxs-lookup"><span data-stu-id="368d5-157">This is a promotional email</span></span>
    
   - <span data-ttu-id="368d5-158">Ce message vous a été envoyé suite à votre demande d'abonnement</span><span class="sxs-lookup"><span data-stu-id="368d5-158">You are receiving this email because you requested a subscription</span></span>
    
   - <span data-ttu-id="368d5-159">cliquez ici pour vous désinscrire</span><span class="sxs-lookup"><span data-stu-id="368d5-159">click here to unsubscribe</span></span>
    
   - <span data-ttu-id="368d5-160">Ce message vous a été envoyé car vous êtes abonné</span><span class="sxs-lookup"><span data-stu-id="368d5-160">You have received this email because you are subscribed</span></span>
    
   - <span data-ttu-id="368d5-161">Si vous ne souhaitez plus recevoir notre bulletin d'informations</span><span class="sxs-lookup"><span data-stu-id="368d5-161">If you no longer wish to receive our email newsletter</span></span>
    
   - <span data-ttu-id="368d5-162">pour vous désinscrire de ce bulletin d'informations</span><span class="sxs-lookup"><span data-stu-id="368d5-162">to unsubscribe from this newsletter</span></span>
    
   - <span data-ttu-id="368d5-163">Si ce message ne s'affiche pas correctement</span><span class="sxs-lookup"><span data-stu-id="368d5-163">If you have trouble viewing this email</span></span>
    
   - <span data-ttu-id="368d5-164">Ceci est un message publicitaire</span><span class="sxs-lookup"><span data-stu-id="368d5-164">This is an advertisement</span></span>
    
   - <span data-ttu-id="368d5-165">vous souhaitez annuler l'abonnement ou modifier votre</span><span class="sxs-lookup"><span data-stu-id="368d5-165">you would like to unsubscribe or change your</span></span>
    
   - <span data-ttu-id="368d5-166">afficher ce message électronique sous forme de page web</span><span class="sxs-lookup"><span data-stu-id="368d5-166">view this email as a webpage</span></span>
    
   - <span data-ttu-id="368d5-167">Vous recevez ce message car vous êtes abonné</span><span class="sxs-lookup"><span data-stu-id="368d5-167">You are receiving this email because you are subscribed</span></span>
    
   <span data-ttu-id="368d5-p110">**Remarque**: une fois encore, cette liste n’est pas un ensemble complet des phrases présentes dans les messages électroniques en masse ; plus d’informations peut être ajouté ou supprimé selon vos besoins. Toutefois, il est un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="368d5-p110">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="368d5-170">Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="368d5-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="368d5-171">Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="368d5-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="368d5-p111">La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="368d5-p111">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="368d5-175">Si votre action configurée est le message en quarantaine plutôt que d’envoyer à un dossier de courrier indésirable de destinataires, le message est envoyé à la mise en quarantaine administrateur comme une correspondance de règle de flux de messagerie et il ne sera pas disponible dans la quarantaine de l’utilisateur final ou par le biais de l’utilisateur final notifications de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="368d5-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="368d5-176">Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="368d5-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="368d5-177">Enregistrez la règle.</span><span class="sxs-lookup"><span data-stu-id="368d5-177">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="368d5-178">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="368d5-178">For more information</span></span>

[<span data-ttu-id="368d5-179">Quelle est la différence entre courrier indésirable et message électronique en masse ?</span><span class="sxs-lookup"><span data-stu-id="368d5-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="368d5-180">Valeurs BCL</span><span class="sxs-lookup"><span data-stu-id="368d5-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="368d5-181">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="368d5-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="368d5-182">Options de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="368d5-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
