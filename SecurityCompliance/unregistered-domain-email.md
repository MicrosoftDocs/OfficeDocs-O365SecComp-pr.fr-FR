---
title: Courrier électronique de domaine non inscrit
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Si vous envoyez un volume élevé de messagerie du domaine ou non, vous courez le risque de votre courrier électronique bloqué. Lisez cet article pour en savoir plus.
ms.openlocfilehash: f2b60f492197bf0dadb702a1c3f184c2d7e56bf1
ms.sourcegitcommit: 7b85c22fc85ec19e4b44a07e91bfa9ade768185a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "23998598"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="3cd73-104">Non domaine Email : Ce que vous devez connaître</span><span class="sxs-lookup"><span data-stu-id="3cd73-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="3cd73-p102">Permet à Office 365 pour les clients afin de relayer des messages via Exchange Online Protection (EOP). Un exemple pris en charge serait lorsque les utilisateurs ont une boîte aux lettres Office 365 et une personne externe les envoie un courrier électronique mais transfert de messages est configuré afin qu’il repasse à la boîte aux lettres externe. Il s’agit généralement dans les environnements de formation où les participants à tirer parti de leur interface électronique mais toujours obtenir courriels relatifs à l’école. Un autre exemple est lorsque des clients se trouvent dans un scénario hybride et des serveurs locaux envoyer un message électronique s’en déconnecter EOP.</span><span class="sxs-lookup"><span data-stu-id="3cd73-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premise servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="3cd73-109">Problèmes liés à des domaines non enregistrés</span><span class="sxs-lookup"><span data-stu-id="3cd73-109">Problems with unregistered domains</span></span>

<span data-ttu-id="3cd73-p103">Le problème est lorsque les serveurs locaux compromises et finissent par le relais d’un volume important de courrier indésirable en dehors d’EOP. Dans la plupart des cas, les connecteurs droite sont-ils mais courrier électronique est envoyé à partir de domaines non enregistrés, également appelé non. Office 365 autorise un montant raisonnable du courrier provenant de domaines ou non, mais un domaine accepté doit être configuré dans le centre d’administration pour chaque domaine que vous envisagez de l’envoi d’absence du bureau.</span><span class="sxs-lookup"><span data-stu-id="3cd73-p103">The problem is when on-premise servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="3cd73-p104">Une fois compromis, les clients n’est pas autorisées d’envoyer des messages sortants pour les domaines non enregistrés. Les utilisateurs recevront un rapport de remise (NDR) indique :</span><span class="sxs-lookup"><span data-stu-id="3cd73-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="3cd73-p105">550 5.7.750 Service non disponible. Client bloqué à partir de l’envoi à partir de domaines non enregistrés</span><span class="sxs-lookup"><span data-stu-id="3cd73-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="3cd73-117">Déblocage client afin d’envoyer à nouveau</span><span class="sxs-lookup"><span data-stu-id="3cd73-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="3cd73-118">Il existe plusieurs choses que vous devez faire si vous êtes bloqué pour l’envoi à partir de domaines non enregistrés :</span><span class="sxs-lookup"><span data-stu-id="3cd73-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="3cd73-p106">Assurez-vous que vous avez enregistré tous vos domaines dans le centre d’administration Office 365. Vous pouvez trouver plus d’informations [ici](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="3cd73-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="3cd73-p107">Verrouiller vos serveurs sur site et vous assurer qu’ils ne sont pas compromises. Il existe de nombreux facteurs impliqués ici, en particulier si elles sont des serveurs tiers, mais vous devez être en mesure de vous assurer que tous les messages envoyés par ce serveur sont légitime.</span><span class="sxs-lookup"><span data-stu-id="3cd73-p107">Lock down your on-premise servers and ensure that they are not compromised. There are many factors involved here, especially if these are third-party servers, but you will need to be able to make sure all mail leaving that server is legitimate.</span></span>

<span data-ttu-id="3cd73-p108">Une fois que vous avez terminé, vous devez appeler le Support de Microsoft et demander à obtenir votre client déblocage pour renvoyer à partir de domaines ou non.  Il est utile de fournir le code d’erreur, mais vous devez prouver que votre environnement est sécurisé et que le courrier indésirable n’est pas envoyé à nouveau. Vous pouvez trouver plus d’informations [ici](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="3cd73-p108">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="3cd73-126">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3cd73-126">For more information</span></span>

[<span data-ttu-id="3cd73-127">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3cd73-127">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="3cd73-128">Rapports de non-remise la messagerie dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3cd73-128">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="3cd73-129">Configurer le transfert du courrier pour une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="3cd73-129">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="3cd73-130">Comment configurer une application ou un périphérique multi-fonction pour envoyer des courriers électroniques à l’aide d’Office 365</span><span class="sxs-lookup"><span data-stu-id="3cd73-130">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="3cd73-131">[Gérer les domaines acceptés dans Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="3cd73-131">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
