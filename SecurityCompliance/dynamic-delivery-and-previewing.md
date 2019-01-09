---
title: Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: Lorsque vous configurez vos stratégies de pièces jointes sûres DAV, vous choisissez remise dynamique afin d’éviter les retards de message et permettent aux utilisateurs d’afficher un aperçu des pièces jointes qui sont analysés.
ms.openlocfilehash: 95c270e871c3febb13eef8c4374d996fc763315b
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769828"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="43cec-103">Remise dynamique et l’aperçu avec Office 365 DAV approuvés en pièce jointe</span><span class="sxs-lookup"><span data-stu-id="43cec-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="43cec-p101">**Résumé**: remise dynamique est une option qui peut être sélectionnée pour les [Pièces jointes fiables DAV](atp-safe-attachments.md). Lisez cet article pour en savoir plus sur remise dynamique et les fonctionnalités d’aperçu de pièce jointe dans les [Pièces jointes fiables de DAV dans Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="43cec-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="43cec-p102">Lorsque [les stratégies de pièces jointes sûres DAV sont configurés](set-up-atp-safe-attachments-policies.md) pour votre organisation, il existe plusieurs options pour la gestion des pièces jointes. Cela inclut les **Bloquer**, **Remplacer**et **Remise dynamique**. Selon la configuration des stratégies de pièces jointes sûres DAV, destinataires de courriers électroniques peuvent rencontrer un délai d’attente secondaire dans la remise du courrier électronique tandis que les pièces jointes sont analysés. Pour éviter les retards de message, choisissez **Remise dynamique**.</span><span class="sxs-lookup"><span data-stu-id="43cec-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="43cec-110">Fonctionnement de distribution dynamique</span><span class="sxs-lookup"><span data-stu-id="43cec-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="43cec-p103">Remise dynamique élimine les retards de courrier électronique en envoyant le corps d’un message électronique par le biais d’au destinataire avec un espace réservé pour chaque pièce jointe. L’espace réservé reste jusqu'à ce qu’une copie de la pièce jointe est analysée et déterminée sûrs par les [Pièces jointes sûres DAV](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="43cec-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="43cec-113">Comme chaque pièce jointe est désactivée, il est disponible pour ouvrir ou télécharger.</span><span class="sxs-lookup"><span data-stu-id="43cec-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="43cec-114">Si une pièce jointe est déterminée malveillants, il est envoyé à la mise en quarantaine, où une personne dans l’équipe de sécurité de votre organisation (comme un administrateur général Office 365 ou un administrateur de sécurité) peut [Gérer les messages mis en quarantaine dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="43cec-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="43cec-p104">La plupart des fichiers PDF et Office documents peuvent être affichés en mode sans échec pendant l’analyse DAV. Si une pièce jointe n’est pas compatible avec le Générateur d’aperçu de distribution dynamique, destinataires de courriers électroniques voient un espace réservé de pièce jointe jusqu'à ce que l’analyse des pièces jointes sûres DAV est terminée.</span><span class="sxs-lookup"><span data-stu-id="43cec-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

<span data-ttu-id="43cec-117">Avec remise dynamique, les personnes pouvant lire et répondre à leurs messages électroniques immédiatement, tandis que les pièces jointes sont en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="43cec-117">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="43cec-p105">Pièces jointes sûres DAV analyse prend place dans la même zone où résident vos données d’Office 365. Pour plus d’informations sur la zone géographique de centre de données, voir [où se trouvent vos données situées ?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="43cec-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="43cec-120">Que se passe-t-il lorsqu’une personne envoie un message électronique qui contient une pièce jointe ?</span><span class="sxs-lookup"><span data-stu-id="43cec-120">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="43cec-p106">Supposons qu’une organisation de leur [stratégie de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md)est à l’aide de remise dynamique et un utilisateur reçoit un message électronique contenant une pièce jointe. Maintenant Supposons que cette personne transfère le message électronique à une autre personne. Que se passe-t-il ? Cela dépend si les destinataires supplémentaires sont inclus dans les stratégies de pièces jointes sûres DAV.</span><span class="sxs-lookup"><span data-stu-id="43cec-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="43cec-125">Si un destinataire est couverte par une stratégie de pièces jointes sûres DAV à l’aide de l’option de distribution dynamique, le destinataire voit l’espace réservé, avec la possibilité d’afficher un aperçu des fichiers compatibles.</span><span class="sxs-lookup"><span data-stu-id="43cec-125">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="43cec-126">Si un destinataire n’est pas couvert par une stratégie de pièces jointes sûres DAV, puis le courrier électronique et la pièce jointe passeront, sans pièces jointes sûres DAV analyse ou des espaces réservés de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="43cec-126">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="43cec-127">Les tâches requises pour la remise dynamique fonctionne ?</span><span class="sxs-lookup"><span data-stu-id="43cec-127">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="43cec-128">Votre organisation doit avoir [Contre les menaces avancées Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="43cec-128">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="43cec-129">Stratégies doivent être définis pour les pièces jointes sûres DAV à l’aide de l’option de distribution dynamique (voir [l’ensemble des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="43cec-129">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="43cec-130">Courrier électronique de votre organisation doit être hébergé dans Office 365</span><span class="sxs-lookup"><span data-stu-id="43cec-130">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="43cec-131">Y a-t-il des scénarios pour lesquels la remise dynamique n’est pas disponible ?</span><span class="sxs-lookup"><span data-stu-id="43cec-131">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="43cec-p107">Il existe certains scénarios dans lesquels remise dynamique n’est pas pris en charge. Ce sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="43cec-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="43cec-134">Messages électroniques stockés dans des dossiers publics</span><span class="sxs-lookup"><span data-stu-id="43cec-134">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="43cec-135">Messages électroniques qui sont routés d’absence du bureau, puis de nouveau dans la boîte aux lettres de l’utilisateur à l’aide de règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="43cec-135">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="43cec-136">Messages électroniques qui sont déplacés (automatiquement ou manuellement) en dehors de la boîte aux lettres hébergée dans d’autres emplacements, y compris les dossiers d’archivage</span><span class="sxs-lookup"><span data-stu-id="43cec-136">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="43cec-137">Messages électroniques supprimés</span><span class="sxs-lookup"><span data-stu-id="43cec-137">Email messages that are deleted</span></span>
    
- <span data-ttu-id="43cec-138">Dossier de recherche de boîte aux lettres d’un utilisateur qui se trouve dans un état d’erreur</span><span class="sxs-lookup"><span data-stu-id="43cec-138">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="43cec-p108">Environnements dans lesquels un administrateur Exchange Online a activé Exclaimer. Pour résoudre ce problème, voir [les Messages avec pièces jointes ne sont pas remis lors de la remise dynamique DAV et Exclaimer sont utilisées](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="43cec-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="43cec-141">Messages chiffrés avec [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="43cec-141">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>
    
