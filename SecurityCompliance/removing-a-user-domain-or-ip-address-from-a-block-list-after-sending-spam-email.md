---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/01/2018
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
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614398"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="1abd8-103">Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="1abd8-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="1abd8-p101">Si un utilisateur envoie des messages électroniques en continu d’Office 365 qui est considéré comme du courrier indésirable, ils seront bloquées d’envoyer plus de messages. L’utilisateur est répertorié dans le service en tant qu’incorrect sortant expéditeur et reçoit un rapport de remise (NDR) indique :</span><span class="sxs-lookup"><span data-stu-id="1abd8-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="1abd8-p102">Votre message n’a pas pu être remis car vous n’ont pas été reconnue comme un expéditeur valide. La raison la plus courante est que votre adresse de messagerie est soupçonné d’envoyer du courrier indésirable et qu’il a n’est plus autorisé à envoyer des messages à l’extérieur de votre organisation. Contactez votre administrateur de messagerie.  Serveur distant a retourné « 550 5.1.8 accès refusé, expéditeur sortant incorrecte »</span><span class="sxs-lookup"><span data-stu-id="1abd8-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="1abd8-110">Les administrateurs de client reçoit également une alerte indiquant que l’utilisateur a été restreint d’envoyer des messages sortants plus.</span><span class="sxs-lookup"><span data-stu-id="1abd8-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1abd8-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1abd8-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="1abd8-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="1abd8-112"></span></span>

<span data-ttu-id="1abd8-113">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="1abd8-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="1abd8-p103">Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez la rubrique « entrée anti-spam dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1abd8-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="1abd8-p104">La procédure suivante peut également être effectuée par le biais de PowerShell à distance. Utilisez l’applet de commande Get-BlockedSenderAddress pour obtenir la liste des utilisateurs restreints et Remove-BlockedSenderAddress permet de supprimer la restriction. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="1abd8-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="1abd8-119">Supprimer les restrictions pour un compte de messagerie Office 365 bloqué</span><span class="sxs-lookup"><span data-stu-id="1abd8-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="1abd8-p105">Vous effectuez cette tâche dans le & de sécurité pour Microsoft Office 365 centre de conformité (SCC). Pour plus d’informations sur le contrôle de code source, [accédez à la & Office 365 sécurité Centre de conformité](go-to-the-securitycompliance-center.md) . Vous devez être dans la **Gestion de l’organisation** ou le groupe de rôles **d’Administrateur de sécurité** pour pouvoir exécuter ces fonctions. Pour plus d’informations sur les groupes de rôles de contrôle de code source, [accédez à autorisations dans le centre de conformité de & Office 365 sécurité](permissions-in-the-security-and-compliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="1abd8-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="1abd8-124">À l’aide d’un compte disposant de privilèges d’administrateur général Office 365, vous connecter dans le centre de conformité et de sécurité pour Microsoft Office 365 et dans la liste de gauche, développez **Threat Management**, sélectionnez **passer en revue les**, puis **Restricted Professionnel ou de l’école Les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="1abd8-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="1abd8-125">Pour accéder directement à la page **Utilisateurs restreints** (anciennement appelé le centre d’Action) de la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="1abd8-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="1abd8-p106">Cette page contient la liste des utilisateurs qui ont été bloqués à partir de l’envoi de courrier à l’extérieur de votre organisation.  Recherchez l’utilisateur que vous souhaitez supprimer les restrictions sur, puis cliquez sur **Débloquer**.</span><span class="sxs-lookup"><span data-stu-id="1abd8-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="1abd8-128">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="1abd8-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1abd8-p107">Il existe une limite au nombre de fois qu’un compte peut être non bloquée par l’administrateur du client. Si la limite d’un utilisateur a été dépassée, un message d’erreur s’affiche. Vous devrez contacter le Support pour débloquer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1abd8-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span></br></br> <span data-ttu-id="1abd8-131">Il peut prendre jusqu'à 1 heure avant que l’utilisateur soit débloquer.</span><span class="sxs-lookup"><span data-stu-id="1abd8-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="1abd8-132">Listes rouges tierces</span><span class="sxs-lookup"><span data-stu-id="1abd8-132">Third-party block lists</span></span>

<span data-ttu-id="1abd8-p108">Exchange Online Protection utilise également des listes rouges tiers pour aider à prendre des décisions de filtrage du courrier indésirable. Les utilisateurs, des sites Web, des domaines et des adresses IP peuvent être ajoutés pour bloquer des listes figurant dans un message de courrier indésirable pour. En tant que l’administrateur Office 365, vous devriez obtenir ces objets supprimés des fournisseurs de listes de tiers si elles vous appartient.</span><span class="sxs-lookup"><span data-stu-id="1abd8-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="1abd8-p109">Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer à l’aide du [portail libre-service de retrait de la liste](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span><span class="sxs-lookup"><span data-stu-id="1abd8-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="1abd8-138">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1abd8-138">For more information</span></span>

[<span data-ttu-id="1abd8-139">Répondre à un compte de messagerie compromis</span><span class="sxs-lookup"><span data-stu-id="1abd8-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="1abd8-140">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="1abd8-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="1abd8-141">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="1abd8-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="1abd8-142">Autorisations dans le centre de conformité de & de sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="1abd8-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

