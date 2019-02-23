---
title: Remise et aperçu dynamiques avec les pièces jointes sécurisées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Lorsque vous configurez vos stratégies de pièces jointes approuvées ATP, vous choisissez la remise dynamique pour éviter les retards de message et permettre aux utilisateurs de prévisualiser les pièces jointes en cours d'analyse.
ms.openlocfilehash: 1fb221d28a4089db8a4278903107c610d6825f5e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218394"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="abded-103">Remise et aperçu dynamiques avec les pièces jointes sécurisées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="abded-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="abded-p101">**Résumé**: la remise dynamique est une option qui peut être sélectionnée pour [les pièces jointes fiables ATP](atp-safe-attachments.md). Lisez cet article pour en savoir plus sur la remise dynamique et les fonctionnalités d'aperçu des pièces jointes dans [les pièces jointEs approuvéEs ATP dans Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="abded-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="abded-p102">Lorsque des [stratégies de pièces jointEs approuvéEs ATP sont configurées](set-up-atp-safe-attachments-policies.md) pour votre organisation, il existe plusieurs options pour la gestion des pièces jointes. Ces éléments incluent le **blocage**, le **remplacement**et la **remise dynamique**. En fonction de la configuration des stratégies de pièces jointes approuvées ATP, les destinataires peuvent observer un retard mineur lors de la remise du courrier électronique pendant l'analyse de leurs pièces jointes. Pour éviter les retards de message, choisissez **remise dynamique**.</span><span class="sxs-lookup"><span data-stu-id="abded-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="abded-110">Fonctionnement de la remise dynamique</span><span class="sxs-lookup"><span data-stu-id="abded-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="abded-p103">La remise dynamique élimine les retards de messagerie en envoyant le corps d'un message électronique au destinataire avec un espace réservé pour chaque pièce jointe de courrier électronique. L'espace réservé reste jusqu'à ce qu'une copie de la pièce jointe soit analysée et considérée comme fiable par [les pièces jointEs sûres ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="abded-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="abded-113">À mesure que chaque pièce jointe est effacée, elle est disponible pour l'ouverture ou le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="abded-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="abded-114">Si une pièce jointe est considérée comme malveillante, elle est envoyée en quarantaine, où une personne de l'équipe de sécurité de votre organisation (par exemple, un administrateur général ou un administrateur de sécurité d'Office 365) peut [gérer les messages mis en quarantaine dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="abded-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="abded-p104">La plupart des documents PDF et Office peuvent être prévisualisés en mode sans échec pendant l'analyse de l'ATP. Si une pièce jointe n'est pas compatible avec le prévisualisation dynamique de remise, les destinataires de courrier voient une balise d'emplacement de pièce jointe jusqu'à la fin de l'analyse des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="abded-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

> [!TIP]
> <span data-ttu-id="abded-117">Si vous utilisez un appareil mobile et que les fichiers PDF ne sont pas rendus dans le prévisualiseur de remise dynamique, essayez de vous connecter à Office 365 à l'aide de votre navigateur mobile.</span><span class="sxs-lookup"><span data-stu-id="abded-117">If you're using a mobile device, and PDFs are not rendering in Dynamic Delivery previewer at first, try signing into Office 365 using your mobile browser.</span></span>

<span data-ttu-id="abded-118">Avec la remise dynamique, les utilisateurs peuvent lire et répondre immédiatement à leurs messages électroniques, tandis que leurs pièces jointes sont en cours d'analyse.</span><span class="sxs-lookup"><span data-stu-id="abded-118">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="abded-p105">L'analyse des pièces jointes approuvées ATP a lieu dans la région où se trouvent vos données Office 365. Pour plus d'informations sur la géographie du centre de données, voir [où se trouvent vos données?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="abded-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="abded-121">Que se passe-t-il lorsque quelqu'un transfère un courrier électronique qui contient une pièce jointe?</span><span class="sxs-lookup"><span data-stu-id="abded-121">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="abded-p106">Supposons qu'une organisation utilise une remise dynamique pour sa [stratégie de pièces jointEs approuvéEs ATP](set-up-atp-safe-attachments-policies.md), et qu'une personne reçoit un e-mail contenant une pièce jointe. Supposons maintenant que cette personne transfère le message électronique à une autre personne. Que se passe-t-il? Cela dépend du fait que les destinataires supplémentaires sont inclus dans les stratégies de pièces jointes approuvées ATP.</span><span class="sxs-lookup"><span data-stu-id="abded-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="abded-126">Si un destinataire est couvert par une stratégie de pièces jointes approuvées ATP à l'aide de l'option de remise dynamique, le destinataire voit alors l'espace réservé, avec la possibilité de prévisualiser les fichiers compatibles.</span><span class="sxs-lookup"><span data-stu-id="abded-126">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="abded-127">Si un destinataire n'est pas couvert par une stratégie de pièces jointes approuvées pour la protection avancée contre les menaces, les messages électroniques et les pièces jointes sont transmis, sans analyse des pièces jointes fiables ATP ou espaces réservés aux pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="abded-127">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="abded-128">Qu'est-ce qui est requis pour que la remise dynamique fonctionne?</span><span class="sxs-lookup"><span data-stu-id="abded-128">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="abded-129">Votre organisation doit disposer d' [Office 365 protection avancée contre les menaces](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="abded-129">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="abded-130">Les stratégies doivent être définies pour les pièces jointes de niveau de sécurité ATP à l'aide de l'option de remise dynamique (voir [configurer des stratégies de pièces jointes de sécurité ATP dans Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="abded-130">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="abded-131">L'adresse de messagerie de votre organisation doit être hébergée dans Office 365</span><span class="sxs-lookup"><span data-stu-id="abded-131">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="abded-132">Existe-t-il des scénarios pour lesquels la remise dynamique n'est pas disponible?</span><span class="sxs-lookup"><span data-stu-id="abded-132">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="abded-p107">Il existe certains scénarios dans lesquels la remise dynamique n'est pas prise en charge. Ces éléments sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="abded-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="abded-135">Messages électroniques figurant dans des dossiers publics</span><span class="sxs-lookup"><span data-stu-id="abded-135">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="abded-136">Messages électroniques qui sont acheminés vers la boîte aux lettres de l'utilisateur, puis reversez-les à l'aide de règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="abded-136">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="abded-137">Messages électroniques déplacés (automatiquement ou manuellement) en dehors de la boîte aux lettres hébergée et à d'autres emplacements, y compris les dossiers d'archivage</span><span class="sxs-lookup"><span data-stu-id="abded-137">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="abded-138">Messages électroniques supprimés</span><span class="sxs-lookup"><span data-stu-id="abded-138">Email messages that are deleted</span></span>
    
- <span data-ttu-id="abded-139">Dossier de recherche de boîte aux lettres d'un utilisateur en état d'erreur</span><span class="sxs-lookup"><span data-stu-id="abded-139">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="abded-p108">Environnements dans lesquels un administrateur Exchange Online a activé Exclaimer. Pour résoudre ce message, consultez la rubrique [les messages avec des pièces jointes ne sont pas remis lorsque la remise et l'exclaimEment dynamiques ATP sont utilisés](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="abded-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="abded-142">Messages chiffrés à l'aide de [S/MIME (Secure/Multipurpose Internet Mail Extensions)](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="abded-142">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>

