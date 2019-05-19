---
title: Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/2/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
ms.collection:
- M365-security-compliance
description: "Lorsqu'un expéditeur est bloqué du service en raison de l'envoi de courrier indésirable sortant, l'administrateur de domaine spécifié dans Configurer la stratégie anti-courrier indésirable sortant reçoit un courrier électronique de notification semblable à celui-ci :"
ms.openlocfilehash: e30717332358693df3c4e56e58d0679ce3acf2d7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158506"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="d2347-103">Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="d2347-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="d2347-104">Lorsqu'un expéditeur est bloqué du service en raison de l'envoi de courrier indésirable sortant, l'administrateur de domaine spécifié dans [Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md) reçoit un courrier électronique de notification semblable à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="d2347-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="d2347-105">**Adresse de l'expéditeur :** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d2347-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="d2347-106">**Objet :** Notification de courrier indésirable sortant : \<  *nom du compte*  \> a été bloqué du service d'envoi de courriers électroniques sortants</span><span class="sxs-lookup"><span data-stu-id="d2347-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="d2347-107">**Corps :** Il s'agit d'une réponse automatique du système d'analyse du courrier indésirable d'Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="d2347-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="d2347-p101">Vous êtes contacté car nous avons détecté de grandes quantités de courriers électroniques marqués comme courriers indésirables, ou tout autre comportement suspect, en provenance de votre organisation. L'envoi de courriers électroniques a été désactivé pour les comptes de messagerie suivants (ils peuvent toujours recevoir des courriers électroniques) :</span><span class="sxs-lookup"><span data-stu-id="d2347-p101">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization. The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="d2347-110">\< *nom du compte*  \></span><span class="sxs-lookup"><span data-stu-id="d2347-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="d2347-p102">Il est probable que ce compte de messagerie ait été compromis. Suivez les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="d2347-p102">It is likely that this email account has been compromised. Please follow these steps:</span></span>
  
1. <span data-ttu-id="d2347-113">Essayez de résoudre ce problème de votre côté en :</span><span class="sxs-lookup"><span data-stu-id="d2347-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="d2347-114">modifiant le mot de passe du compte ;</span><span class="sxs-lookup"><span data-stu-id="d2347-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="d2347-115">déterminant comment le compte a été compromis ;</span><span class="sxs-lookup"><span data-stu-id="d2347-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="d2347-116">prenant des précautions pour vous assurer que cette vulnérabilité ne sera pas exploitée à nouveau ;</span><span class="sxs-lookup"><span data-stu-id="d2347-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="d2347-117">confirmant que tous les messages posant problème ont été supprimés de votre file d'attente des messages.</span><span class="sxs-lookup"><span data-stu-id="d2347-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="d2347-118">Contactez le support Microsoft via le canal de contact que vous avez l'habitude d'utiliser.</span><span class="sxs-lookup"><span data-stu-id="d2347-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="d2347-119">Expliquez qu'un utilisateur ne peut pas envoyer de courriers électroniques et que le problème a été traité.</span><span class="sxs-lookup"><span data-stu-id="d2347-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="d2347-120">L'agent crée un ticket de support avec les informations que vous fournissez et le transfère afin de débloquer l'adresse de messagerie ou le domaine.</span><span class="sxs-lookup"><span data-stu-id="d2347-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="d2347-121">Une fois que l'adresse a été débloquée et qu'aucun autre problème n'est en attente, vous serez contacté et averti du déblocage.</span><span class="sxs-lookup"><span data-stu-id="d2347-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="d2347-122">Merci de nous aider dans la lutte contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="d2347-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="d2347-123">Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="d2347-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="d2347-124">\*\*REMARQUE : ne répondez pas à ce courrier électronique car il est envoyé à partir d'une adresse non contrôlée\*\*</span><span class="sxs-lookup"><span data-stu-id="d2347-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="d2347-125">Vous pouvez également contacter le support via les options documentées dans [Help and support for EOP](eop/help-and-support-for-eop.md).</span><span class="sxs-lookup"><span data-stu-id="d2347-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

