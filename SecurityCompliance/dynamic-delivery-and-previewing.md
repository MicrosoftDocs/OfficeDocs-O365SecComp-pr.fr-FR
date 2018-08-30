---
title: Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/28/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Lorsque vous configurez vos stratégies de pièces jointes sûres DAV, vous choisissez remise dynamique afin d’éviter les retards de message et permettent aux utilisateurs d’afficher un aperçu des pièces jointes qui sont analysés.
ms.openlocfilehash: 23017f4f995dfe6a90479d83af9522531d7bf96b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527507"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="3aeb9-103">Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe</span><span class="sxs-lookup"><span data-stu-id="3aeb9-103">Dynamic delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="3aeb9-p101">Remise dynamique est une option qui peut être sélectionnée pour. Lisez cet article pour en savoir plus sur remise dynamique et les fonctionnalités d’aperçu de pièce jointe dans les [Pièces jointes fiables de DAV dans Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p101">Dynamic delivery is an option that can be selected for . Read this article to learn about dynamic delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="3aeb9-106">Fonctionnement de la remise dynamique</span><span class="sxs-lookup"><span data-stu-id="3aeb9-106">How dynamic delivery works</span></span>

<span data-ttu-id="3aeb9-p102">Lorsque vous [configurez des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md), vous pouvez choisir parmi plusieurs options, telles que le **bloc**, **Remplacer**et **Remise dynamique**. Selon la façon dont vos stratégies sont configurées, destinataires de courriers électroniques peuvent patienter quelques instants secondaire dans la remise du courrier électronique tandis que les pièces jointes sont analysés. Pour éviter les retards de message, choisissez **Remise dynamique**.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p102">When you [set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md), you can choose from several options, such as **Block**, **Replace**, and **Dynamic Delivery**. Depending on how your policies are configured, email recipients can experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
<span data-ttu-id="3aeb9-p103">L’option de distribution dynamique élimine les retards de courrier électronique en envoyant le corps d’un message électronique par le biais d’avec un espace réservé pour chaque pièce jointe. L’espace réservé reste jusqu'à ce que la pièce jointe est analysée par [Les pièces jointes fiables de DAV dans Office 365](atp-safe-attachments.md). Destinataires de courriers électroniques pouvant lire et répondre à leurs messages électroniques immédiatement, sachant que les pièces jointes sont en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p103">The dynamic delivery option eliminates email delays by sending the body of an email message through with a placeholder for each email attachment. The placeholder remains until the attachment is scanned by [ATP Safe Attachments in Office 365](atp-safe-attachments.md). Email recipients can read and respond to their email messages right away, knowing that their attachments are being analyzed.</span></span>
  
<span data-ttu-id="3aeb9-p104">La plupart des fichiers PDF et Office documents peuvent être affichés en mode sans échec pendant l’analyse DAV. Si une pièce jointe n’est pas compatible avec le Générateur d’aperçu dynamique de remise, destinataires de courriers électroniques voient l’espace réservé de pièce jointe jusqu'à ce que l’analyse des pièces jointes sûres DAV est terminée.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the dynamic delivery previewer, email recipients see the attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>
  
<span data-ttu-id="3aeb9-p105">Comme chaque pièce jointe est désactivée, elle est automatiquement rattaché au message électronique d’origine. Si une pièce jointe est déterminée malveillants, il est envoyé à la mise en quarantaine, où une personne dans l’équipe de sécurité de votre organisation (comme un administrateur général Office 365 ou un administrateur de sécurité) peut [Gérer les messages mis en quarantaine dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p105">As each attachment is cleared, it is automatically reattached to the original email message. If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="3aeb9-117">Que se passe-t-il lorsqu’une personne envoie un message électronique qui contient une pièce jointe ?</span><span class="sxs-lookup"><span data-stu-id="3aeb9-117">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="3aeb9-p106">Supposons qu’une organisation de leur [stratégie de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md)est à l’aide de remise dynamique et un utilisateur reçoit un message électronique contenant une pièce jointe. Maintenant Supposons que cette personne est sur le point de transférer le message électronique à une autre personne. Que se passe-t-il ? Cela dépend si les destinataires supplémentaires sont inclus dans les stratégies de pièces jointes sûres DAV.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p106">Suppose that an organization is using dynamic delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person is about to forward the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="3aeb9-122">Si un destinataire est couverte par une stratégie de pièces jointes sûres DAV à l’aide de l’option de distribution dynamique, le destinataire voit l’espace réservé, avec la possibilité d’afficher un aperçu des fichiers compatibles.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-122">If a recipient is covered by an ATP Safe Attachments policy using the dynamic delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="3aeb9-123">Si un destinataire n’est pas couvert par une stratégie de pièces jointes sûres DAV, puis le courrier électronique et la pièce jointe passeront, sans pièces jointes sûres DAV analyse ou des espaces réservés de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3aeb9-123">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="3aeb9-124">Les tâches requises pour la remise dynamique fonctionne ?</span><span class="sxs-lookup"><span data-stu-id="3aeb9-124">What's required for dynamic delivery to work?</span></span>

- <span data-ttu-id="3aeb9-125">Votre organisation doit avoir [Contre les menaces avancées Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="3aeb9-125">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="3aeb9-126">Stratégies doivent être définis pour les pièces jointes sûres DAV à l’aide de l’option de distribution dynamique (voir [l’ensemble des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="3aeb9-126">Policies must be defined for ATP Safe Attachments using the dynamic delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="3aeb9-127">Courrier électronique de votre organisation doit être hébergé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3aeb9-127">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="3aeb9-128">Y a-t-il des scénarios pour lesquels la remise dynamique n’est pas disponible ?</span><span class="sxs-lookup"><span data-stu-id="3aeb9-128">Are there scenarios for which dynamic delivery is not available?</span></span>

<span data-ttu-id="3aeb9-p107">Il existe certains scénarios dans lesquels remise dynamique n’est pas pris en charge. Ce sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p107">There are certain scenarios in which dynamic delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="3aeb9-131">Messages électroniques stockés dans des dossiers publics</span><span class="sxs-lookup"><span data-stu-id="3aeb9-131">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="3aeb9-132">Messages électroniques qui sont routés d’absence du bureau, puis de nouveau dans la boîte aux lettres de l’utilisateur à l’aide de règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="3aeb9-132">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="3aeb9-133">Messages qui sont déplacés (automatiquement ou manuellement) en dehors de la boîte aux lettres hébergée dans d’autres emplacements, y compris les dossiers d’archivage</span><span class="sxs-lookup"><span data-stu-id="3aeb9-133">Messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="3aeb9-134">Messages qui sont supprimés</span><span class="sxs-lookup"><span data-stu-id="3aeb9-134">Messages that are deleted</span></span>
    
- <span data-ttu-id="3aeb9-135">Dossier de recherche de boîte aux lettres d’un utilisateur qui se trouve dans un état d’erreur</span><span class="sxs-lookup"><span data-stu-id="3aeb9-135">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="3aeb9-p108">Environnements dans lesquels un administrateur Exchange Online a activé Exclaimer. (Voir [les Messages avec pièces jointes ne sont pas remis lors de la remise dynamique DAV et Exclaimer sont utilisés](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span><span class="sxs-lookup"><span data-stu-id="3aeb9-p108">Environments in which an Exchange Online admin has enabled Exclaimer. (See [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="3aeb9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aeb9-138">Related topics</span></span>

[<span data-ttu-id="3aeb9-139">Protection de Microsoft Office 365 menace avancées</span><span class="sxs-lookup"><span data-stu-id="3aeb9-139">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="3aeb9-140">Pièces jointes DAV Safe dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3aeb9-140">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="3aeb9-141">Définir des stratégies de pièces jointes sûres DAV dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3aeb9-141">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="3aeb9-142">Liens DAV Safe dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3aeb9-142">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)

[<span data-ttu-id="3aeb9-143">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="3aeb9-143">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

