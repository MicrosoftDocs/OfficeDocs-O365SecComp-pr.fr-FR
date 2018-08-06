---
title: Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. '
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026331"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="45265-103">Suppression d’un utilisateur, d’un domaine ou d’une adresse IP d’une liste rouge après l’envoi de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="45265-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="45265-104">Si un utilisateur envoie en continu des messages électroniques classés comme courriers indésirables depuis Office 365, ses envois seront bloqués. </span><span class="sxs-lookup"><span data-stu-id="45265-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="45265-105">
Lorsque les messages électroniques d’un expéditeur sont bloqués, ce dernier une notification d’échec de remise (impossible d’envoyer le message) qui fournit des informations spécifiques sur les étapes à suivre pour débloquer les messages.</span><span class="sxs-lookup"><span data-stu-id="45265-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="45265-p101">Non seulement des utilisateurs individuels peuvent être bloquées par les domaines de service, mais les sites Web spécifiques, et adresses IP peuvent aussi être bloquées. Dans certains cas, des domaines ou des sites Web peuvent être ajoutés à une liste d’adresses bloquées seulement car ils apparaissent dans un message de courrier indésirable. En tant que l’administrateur Office 365, vous pouvez essayer d’obtenir des utilisateurs, sites Web, des domaines et supprimées à partir de listes d’interdiction tiers des adresses IP. Utilisez les liens de la table en bas de cette rubrique pour contacter chaque tiers, puis suivez les instructions. Si une personne extérieure à Office 365 ne peuvent pas envoyer des messages à votre compte Office 365, leur compte peut se trouver sur la liste des expéditeurs bloqués externe. Les utilisateurs en dehors d’Office 365 peuvent tenter de se supprimer de la liste des expéditeurs bloqués à l’aide du [portail libre-service de retrait de la liste](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="45265-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="45265-p102">Vous pouvez configurer des paramètres de courrier indésirable sortant afin de recevoir une notification lorsque les messages d’un utilisateur Office 365 sont classés comme courrier indésirable. Une fois que le problème lié à la boîte aux lettres de l’utilisateur est résolu, vous pouvez le retirer de la liste rouge.</span><span class="sxs-lookup"><span data-stu-id="45265-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="45265-114">Retirer un compte de messagerie Office 365 de la liste rouge</span><span class="sxs-lookup"><span data-stu-id="45265-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="45265-p103">Vous effectuez cette tâche dans le centre d’administration Exchange (CAE). Consultez la rubrique [Centre d’administration Exchange dans Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) pour plus d’informations sur le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="45265-p103">You complete this task in the Exchange admin center (EAC). Check out [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) for details about the EAC.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="45265-117">Vous ne verrez pas le centre de maintenance, sauf si vous vous trouvez dans le centre d’administration Exchange pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="45265-117">You won't see the action center unless you're in the EAC for Exchange Online.</span></span> 
  
1. <span data-ttu-id="45265-118">Dans le CAE, accédez à **protection** \> **Centre de maintenance**.</span><span class="sxs-lookup"><span data-stu-id="45265-118">In the EAC, navigate to **protection** \> **action center**.</span></span>
    
    ![Accéder au Centre de maintenance dans le Centre d’administration Exchange](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. <span data-ttu-id="45265-120">Sélectionnez l’icône **Rechercher** et entrez l’adresse SMTP de l’utilisateur bloqué.</span><span class="sxs-lookup"><span data-stu-id="45265-120">Select the **Search** icon, and then enter the SMTP address of the blocked user.</span></span> 
    
    ![Rechercher un utilisateur bloqué dans le Centre de maintenance](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. <span data-ttu-id="45265-122">Cliquez sur **Débloquer le compte** dans le volet Description.</span><span class="sxs-lookup"><span data-stu-id="45265-122">Click **Unblock Account** in the description pane.</span></span> 
    
    ![Débloquer un utilisateur dans le Centre de maintenance](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. <span data-ttu-id="45265-124">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="45265-124">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="45265-p104">Il existe une limite au nombre de déblocages d’un compte par l’administrateur client. Le dépassement de la limite pour un utilisateur entraîne l’affichage d’un message d’erreur. Contactez le support pour débloquer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45265-p104">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. Contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="45265-127">Listes rouges tierces</span><span class="sxs-lookup"><span data-stu-id="45265-127">Third-party block lists</span></span>

|<span data-ttu-id="45265-128">**Nom de la liste**</span><span class="sxs-lookup"><span data-stu-id="45265-128">**List Name**</span></span>|<span data-ttu-id="45265-129">**Portail de retrait de la liste**</span><span class="sxs-lookup"><span data-stu-id="45265-129">**Delisting Portal**</span></span>|<span data-ttu-id="45265-130">**Pour plus d'informations**</span><span class="sxs-lookup"><span data-stu-id="45265-130">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45265-131">URIBL</span><span class="sxs-lookup"><span data-stu-id="45265-131">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="45265-132">Site Web URIBL</span><span class="sxs-lookup"><span data-stu-id="45265-132"> URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="45265-133">SURBL</span><span class="sxs-lookup"><span data-stu-id="45265-133">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="45265-134">Présentation de données de réputation d’URI SURBL</span><span class="sxs-lookup"><span data-stu-id="45265-134">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="45265-135">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="45265-135">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="45265-136">Présentation du filtrage DNSBL</span><span class="sxs-lookup"><span data-stu-id="45265-136">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="45265-137">invaluement</span><span class="sxs-lookup"><span data-stu-id="45265-137">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="45265-138">liste de blocage du courrier indésirable de liste</span><span class="sxs-lookup"><span data-stu-id="45265-138">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="45265-139">Phishtank</span><span class="sxs-lookup"><span data-stu-id="45265-139">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="45265-140">PhishTank Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="45265-140">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="45265-141">Exchange Online Protection utilise également des listes rouges tiers pour le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="45265-141">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="45265-142">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="45265-142">For more information</span></span>

[<span data-ttu-id="45265-143">Configurer la stratégie anti-courrier indésirable sortant</span><span class="sxs-lookup"><span data-stu-id="45265-143">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="45265-144">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="45265-144">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="45265-145">Utilisation du portail Supprimer de la liste pour vous supprimer de la liste des expéditeurs bloqués Office 365</span><span class="sxs-lookup"><span data-stu-id="45265-145">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

