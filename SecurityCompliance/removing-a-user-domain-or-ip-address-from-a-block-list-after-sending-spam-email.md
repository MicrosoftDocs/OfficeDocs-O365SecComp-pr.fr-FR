---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/16/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. '
ms.openlocfilehash: 295d92fc6a1cd26783b18304a2d119d2ea0d7f1f
ms.sourcegitcommit: b164d4af65709133e0b512a4327a70fae13a974d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25577063"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="09a7a-103">Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="09a7a-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="09a7a-p101">Si un utilisateur envoie des messages électroniques en continu d’Office 365 qui est considéré comme du courrier indésirable, ils seront bloquées d’envoyer plus de messages. L’utilisateur est répertorié dans le service en tant qu’incorrect sortant expéditeur et reçoit un rapport de remise (NDR) indique :</span><span class="sxs-lookup"><span data-stu-id="09a7a-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="09a7a-p102">Votre message n’a pas pu être remis car vous n’ont pas été reconnue comme un expéditeur valide. La raison la plus courante est que votre adresse de messagerie est soupçonné d’envoyer du courrier indésirable et qu’il a n’est plus autorisé à envoyer des messages à l’extérieur de votre organisation. Contactez votre administrateur de messagerie.  Serveur distant a retourné « 550 5.1.8 accès refusé, expéditeur sortant incorrecte »</span><span class="sxs-lookup"><span data-stu-id="09a7a-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="09a7a-p103">Vous pouvez configurer vos paramètres de stratégie de courrier indésirable sortant afin que vous recevez une notification lorsqu’un utilisateur d’Office 365 est bloqué à partir de l’envoi de courrier électronique. Après avoir résolu le problème de boîte aux lettres de l’utilisateur, vous pouvez supprimer le bloc de cet expéditeur.</span><span class="sxs-lookup"><span data-stu-id="09a7a-p103">You can configure your outbound spam policy settings so that you get a notification when an Office 365 user is blocked from sending email. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="09a7a-112">Retirer un compte de messagerie Office 365 de la liste rouge</span><span class="sxs-lookup"><span data-stu-id="09a7a-112">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="09a7a-p104">Vous effectuez cette tâche dans la sécurité pour Microsoft Office 365 & centre de conformité (SCC). Pour plus d’informations sur le contrôle de code source, [accédez au portail Office 365 sécurité & centre de conformité](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="09a7a-p104">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="09a7a-115">À l’aide d’un compte disposant de privilèges d’administrateur général Office 365, vous connecter dans le centre de conformité et de sécurité pour Microsoft Office 365 et dans la liste de gauche, développez **Threat Management**, sélectionnez **passer en revue les**, puis **Restricted Professionnel ou de l’école Les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="09a7a-115">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="09a7a-116">Pour accéder directement à la page **Utilisateurs restreints** (anciennement appelé le centre d’Action) de la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="09a7a-116">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="09a7a-p105">Cette page contient la liste des utilisateurs qui ont été bloqués à partir de l’envoi de courrier à l’extérieur de votre organisation.  Recherchez l’utilisateur que vous souhaitez supprimer les restrictions sur, puis cliquez sur **Débloquer**.</span><span class="sxs-lookup"><span data-stu-id="09a7a-p105">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="09a7a-119">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="09a7a-119">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="09a7a-p106">Il existe une limite au nombre de fois qu’un compte peut être non bloquée par l’administrateur du client. Si la limite d’un utilisateur a été dépassée, un message d’erreur s’affiche. Vous devrez contacter le Support pour débloquer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09a7a-p106">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="09a7a-122">Listes rouges tierces</span><span class="sxs-lookup"><span data-stu-id="09a7a-122">Third-party block lists</span></span>

<span data-ttu-id="09a7a-p107">Exchange Online Protection utilise également des listes rouges tiers pour aider à prendre des décisions de filtrage du courrier indésirable. Les utilisateurs, des sites Web, des domaines et des adresses IP peuvent être ajoutés pour bloquer des listes figurant dans un message de courrier indésirable pour. En tant que l’administrateur Office 365, vous devriez obtenir ces objets supprimés des fournisseurs de listes de tiers si elles vous appartient.</span><span class="sxs-lookup"><span data-stu-id="09a7a-p107">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="09a7a-p108">Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer à l’aide du [portail libre-service de retrait de la liste](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span><span class="sxs-lookup"><span data-stu-id="09a7a-p108">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="09a7a-128">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="09a7a-128">For more information</span></span>

[<span data-ttu-id="09a7a-129">Répondre à un compte de messagerie compromis</span><span class="sxs-lookup"><span data-stu-id="09a7a-129">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="09a7a-130">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="09a7a-130">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="09a7a-131">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="09a7a-131">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

  

  

