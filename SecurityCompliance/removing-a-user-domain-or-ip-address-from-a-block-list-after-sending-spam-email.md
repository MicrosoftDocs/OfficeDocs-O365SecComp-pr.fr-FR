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
ms.openlocfilehash: 3ffd8b65d6994699093237e9f9a0a3aaa802f5e2
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223083"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="48dfc-103">Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="48dfc-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="48dfc-p101">Si un utilisateur envoie continuellement des messages électroniques à partir d'Office 365 classé comme courrier indésirable, ils ne pourront plus envoyer d'autres messages. L'utilisateur est mentionné dans le service en tant qu'expéditeur sortant incorrect et reçoit une notification d'échec de remise qui indique:</span><span class="sxs-lookup"><span data-stu-id="48dfc-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="48dfc-p102">Votre message n'a pas pu être remis car vous n'avez pas été reconnu comme un expéditeur valide. La raison la plus fréquente de ce message est que votre adresse de courrier est suspecte d'envoyer du courrier indésirable et qu'elle n'est plus autorisée à envoyer des messages en dehors de votre organisation. Contactez votre administrateur de courrier électronique pour obtenir de l'aide.  Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect "</span><span class="sxs-lookup"><span data-stu-id="48dfc-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="48dfc-110">Les administrateurs de client reçoivent également une alerte indiquant que l'utilisateur n'a pas été autorisé à envoyer des messages sortants supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="48dfc-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="48dfc-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="48dfc-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="48dfc-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="48dfc-112"></span></span>

<span data-ttu-id="48dfc-113">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="48dfc-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="48dfc-p103">Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la rubrique «entrée anti-courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="48dfc-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="48dfc-p104">La procédure suivante peut également être effectuée via PowerShell à distance. Utilisez la cmdlet Get-BlockedSenderAddress pour obtenir la liste des utilisateurs avec accès restreint et Remove-BlockedSenderAddress pour supprimer la restriction. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="48dfc-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="48dfc-119">Supprimer les restrictions pour un compte de messagerie Office 365 bloqué</span><span class="sxs-lookup"><span data-stu-id="48dfc-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="48dfc-p105">Vous effectuez cette tâche dans le centre de sécurité & conformité Office 365 (SCC). [Accédez au centre de sécurité & de sécurité Office 365](go-to-the-securitycompliance-center.md) pour plus d'informations sur SCC. Vous devez être dans le groupe de rôles gestion de l' **organisation** ou **administrateur de sécurité** pour effectuer ces fonctions. [Accédez à autorisations dans le centre de sécurité & de la sécurité Office 365](permissions-in-the-security-and-compliance-center.md) pour plus d'informations sur les groupes de rôles SCC.</span><span class="sxs-lookup"><span data-stu-id="48dfc-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="48dfc-124">À l'aide d'un compte professionnel ou scolaire disposant de privilèges d'administrateur général Office 365, connectez-vous au centre de sécurité et conformité Office 365 et, dans la liste de gauche, développez **gestion des menaces**, choisissez **examiner**, puis choisissez **restreint. Les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="48dfc-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="48dfc-125">Pour accéder directement à la page **utilisateurs restreints** (anciennement appelé centre de maintenance) dans le &amp; Centre de sécurité conformité, utilisez l'URL suivante: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="48dfc-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="48dfc-p106">Cette page contient la liste des utilisateurs qui ont été bloqués pour l'envoi de messages à l'extérieur de votre organisation.  Recherchez l'utilisateur pour lequel vous souhaitez supprimer les restrictions, puis cliquez \*\*\*\* sur débloquer.</span><span class="sxs-lookup"><span data-stu-id="48dfc-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="48dfc-128">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="48dfc-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="48dfc-p107">Le nombre de fois qu'un compte peut être débloqué par l'administrateur client est limité. Si la limite pour un utilisateur a été dépassée, un message d'erreur s'affiche. Vous devrez ensuite contacter le support technique pour débloquer l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48dfc-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span><br/><br/> <span data-ttu-id="48dfc-131">La déblocage de l'utilisateur peut prendre jusqu'à 1 heure.</span><span class="sxs-lookup"><span data-stu-id="48dfc-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="48dfc-132">Listes rouges tierces</span><span class="sxs-lookup"><span data-stu-id="48dfc-132">Third-party block lists</span></span>

<span data-ttu-id="48dfc-p108">Exchange Online Protection utilise également des listes rouges tierces pour vous aider à prendre des décisions en matière de filtrage du courrier indésirable. Les utilisateurs, les sites Web, les domaines et les adresses IP peuvent être ajoutés aux listes bloquées uniquement pour apparaître dans un message de courrier indésirable. En tant qu'administrateur Office 365, vous devez essayer d'obtenir ces objets supprimés des fournisseurs de liste tiers s'ils vous appartiennent.</span><span class="sxs-lookup"><span data-stu-id="48dfc-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="48dfc-p109">Si une personne extérieure à Office 365 ne peut pas envoyer de messages à votre compte Office 365, il se peut que son compte figure dans la liste des expéditeurs bloqués externes. Les utilisateurs externes à Office 365 peuvent essayer de se supprimer eux-mêmes à l'aide du portail de retrait [libre-service](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span><span class="sxs-lookup"><span data-stu-id="48dfc-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="48dfc-138">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="48dfc-138">For more information</span></span>

[<span data-ttu-id="48dfc-139">Réponse à un compte de messagerie compromis</span><span class="sxs-lookup"><span data-stu-id="48dfc-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="48dfc-140">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="48dfc-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="48dfc-141">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="48dfc-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="48dfc-142">Autorisations dans le centre de sécurité & de sécurité Office 365</span><span class="sxs-lookup"><span data-stu-id="48dfc-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

