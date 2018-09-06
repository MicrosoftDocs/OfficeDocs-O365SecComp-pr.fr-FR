---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: 3f3130bec3cde4cdc1343a0140a9013deacfc519
ms.sourcegitcommit: d85fc77cba3a17d5ddf215e2f506f61b499e0cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839108"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="13755-103">Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="13755-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="13755-104">Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. </span><span class="sxs-lookup"><span data-stu-id="13755-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="13755-105">
Lorsque les messages électroniques d’un expéditeur sont bloqués, ce dernier une notification d’échec de remise (impossible d’envoyer le message) qui fournit des informations spécifiques sur les étapes à suivre pour débloquer les messages.</span><span class="sxs-lookup"><span data-stu-id="13755-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="13755-p101">Non seulement des utilisateurs individuels peuvent être bloquées par les domaines de service, mais les sites Web spécifiques, et adresses IP peuvent aussi être bloquées. Dans certains cas, des domaines ou des sites Web peuvent être ajoutés à une liste d’adresses bloquées seulement car ils apparaissent dans un message de courrier indésirable. En tant que l’administrateur Office 365, vous pouvez essayer d’obtenir des utilisateurs, sites Web, des domaines et supprimées à partir de listes d’interdiction tiers des adresses IP. Utilisez les liens de la table en bas de cette rubrique pour contacter chaque tiers, puis suivez les instructions. Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer de la liste des expéditeurs bloqués à l’aide du [portail libre-service de retrait de la liste](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="13755-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="13755-p102">Vous pouvez configurer des paramètres de courrier indésirable sortant afin de recevoir une notification lorsque les messages d’un utilisateur Office 365 sont classés comme courrier indésirable. Une fois que le problème lié à la boîte aux lettres de l’utilisateur est résolu, vous pouvez le retirer de la liste rouge.</span><span class="sxs-lookup"><span data-stu-id="13755-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="13755-114">Retirer un compte de messagerie Office 365 de la liste rouge</span><span class="sxs-lookup"><span data-stu-id="13755-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="13755-p103">Vous effectuez cette tâche dans la sécurité pour Microsoft Office 365 & centre de conformité (SCC). Pour plus d’informations sur le contrôle de code source, [accédez au portail Office 365 sécurité & centre de conformité](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="13755-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="13755-117">À l’aide d’un compte disposant de privilèges d’administrateur général Office 365, vous connecter dans le centre de conformité et de sécurité pour Microsoft Office 365 et dans la liste de gauche, développez **Threat Management**, sélectionnez **passer en revue les**, puis **Restricted Professionnel ou de l’école Les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="13755-117">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="13755-118">Pour accéder directement à la page **Utilisateurs restreints** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="13755-118">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="13755-p104">Cette page contient la liste des utilisateurs qui ont été bloqués à partir de l’envoi de courrier à l’extérieur de votre organisation.  Recherchez les utilisateurs que vous souhaitez supprimer les restrictions, puis cliquez sur **Débloquer**.</span><span class="sxs-lookup"><span data-stu-id="13755-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user(s) you wish to remove restrictions and then click on **Unblock**.</span></span>

3. <span data-ttu-id="13755-121">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="13755-121">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="13755-p105">Il existe une limite au nombre de fois qu’un compte peut être non bloquée par l’administrateur du client. Si la limite d’un utilisateur a été dépassée, un message d’erreur s’affiche. Vous devrez contacter le Support pour débloquer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13755-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="13755-124">Listes rouges tierces</span><span class="sxs-lookup"><span data-stu-id="13755-124">Third-party block lists</span></span>

|<span data-ttu-id="13755-125">**Nom de la liste**</span><span class="sxs-lookup"><span data-stu-id="13755-125">**List Name**</span></span>|<span data-ttu-id="13755-126">**Portail de retrait de la liste**</span><span class="sxs-lookup"><span data-stu-id="13755-126">**Delisting Portal**</span></span>|<span data-ttu-id="13755-127">**Pour plus d'informations**</span><span class="sxs-lookup"><span data-stu-id="13755-127">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13755-128">URIBL</span><span class="sxs-lookup"><span data-stu-id="13755-128">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="13755-129">Site Web URIBL</span><span class="sxs-lookup"><span data-stu-id="13755-129">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="13755-130">SURBL</span><span class="sxs-lookup"><span data-stu-id="13755-130">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="13755-131">Présentation de données de réputation d’URI SURBL</span><span class="sxs-lookup"><span data-stu-id="13755-131">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="13755-132">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="13755-132">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="13755-133">Présentation du filtrage DNSBL</span><span class="sxs-lookup"><span data-stu-id="13755-133">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="13755-134">invaluement</span><span class="sxs-lookup"><span data-stu-id="13755-134">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="13755-135">liste de blocage du courrier indésirable de liste</span><span class="sxs-lookup"><span data-stu-id="13755-135">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="13755-136">Phishtank</span><span class="sxs-lookup"><span data-stu-id="13755-136">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="13755-137">PhishTank Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="13755-137">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="13755-138">Exchange Online Protection utilise également des listes rouges tiers pour le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="13755-138">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="13755-139">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="13755-139">For more information</span></span>

[<span data-ttu-id="13755-140">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="13755-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="13755-141">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="13755-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="13755-142">Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365</span><span class="sxs-lookup"><span data-stu-id="13755-142">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

