---
title: Courrier électronique de domaine non enregistré
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Si vous envoyez un volume important de courrier non enregistré de domaine, vous risquez de bloquer le blocage de votre courrier. Lisez cet article pour en savoir plus.
ms.openlocfilehash: bef39780438a6d9669354bddaed391b2364badf8
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220774"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="48a0e-104">Courrier électronique de domaine non enregistré: ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="48a0e-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="48a0e-p102">Office 365 permet aux clients de relayer certains messages via Exchange Online Protection (EOP). Par exemple, lorsque les utilisateurs disposent d'une boîte aux lettres Office 365 et que quelqu'un les envoie à une boîte aux lettres externe, le transfert de courrier est configuré de manière à ce qu'il redevienne la boîte aux lettres externe de l'utilisateur. Il s'agit le plus souvent dans les environnements d'éducation où les étudiants veulent tirer parti de leur interface de messagerie personnelle mais recevoir des courriers électroniques liés à l'école. Un autre exemple est lorsque les clients sont dans un scénario hybride et disposent de serveurs sur site qui envoient des messages provenant d'EOP.</span><span class="sxs-lookup"><span data-stu-id="48a0e-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="48a0e-109">Problèmes liés aux domaines non enregistrés</span><span class="sxs-lookup"><span data-stu-id="48a0e-109">Problems with unregistered domains</span></span>

<span data-ttu-id="48a0e-p103">Le problème est lié au fait que les serveurs sur site sont compromis et finissent par relayer un volume important de courrier indésirable de EOP. Dans presque tous les cas, les connecteurs corrects sont configurés, mais les courriers électroniques sont envoyés depuis les domaines non enregistrés, également appelés domaines. Office 365 autorise une quantité raisonnable de courrier provenant de domaines non enregistrés, mais un domaine accepté doit être configuré dans le centre d'administration pour chaque domaine que vous envisagez d'envoyer à.</span><span class="sxs-lookup"><span data-stu-id="48a0e-p103">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="48a0e-p104">Une fois compromis, les clients ne pourront pas envoyer de messages sortants pour les domaines non enregistrés. Les utilisateurs reçoivent une notification d'échec de remise qui indique:</span><span class="sxs-lookup"><span data-stu-id="48a0e-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="48a0e-p105">550 5.7.750 service non disponible. Le client a bloqué l'envoi à partir de domaines non enregistrés</span><span class="sxs-lookup"><span data-stu-id="48a0e-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="48a0e-117">Déblocage du client afin de le renvoyer</span><span class="sxs-lookup"><span data-stu-id="48a0e-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="48a0e-118">Il y a plusieurs choses à faire si vous êtes bloqué pour l'envoi à partir de domaines non enregistrés:</span><span class="sxs-lookup"><span data-stu-id="48a0e-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="48a0e-p106">Assurez-vous d'enregistrer tous vos domaines dans le centre d'administration Office 365. Vous trouverez plus d'informations [ici](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="48a0e-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="48a0e-p107">Recherchez les connecteurs inhabituels. Les acteurs malveillants vont souvent créer de nouveaux connecteurs entrants dans votre client Office 365 pour envoyer du courrier indésirable. Vous trouverez plus d'informations sur la vérification de vos connecteurs [ici](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="48a0e-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="48a0e-124">Verrouillez vos serveurs locaux et assurez-vous qu'ils ne sont pas compromis.</span><span class="sxs-lookup"><span data-stu-id="48a0e-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="48a0e-p108">Il existe de nombreux facteurs impliqués, en particulier s'il s'agit de serveurs tiers. Quelle que soit la fonctionnalité, vous devez être en mesure de confirmer que tout le courrier sortant de vos serveurs est légitime.</span><span class="sxs-lookup"><span data-stu-id="48a0e-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="48a0e-p109">Une fois la procédure terminée, vous devez appeler le support Microsoft et demander à ce que votre locataire débloquée pour envoyer à nouveau des domaines non enregistrés.  Le fait de fournir le code d'erreur est utile, mais vous devrez prouver que votre environnement est sécurisé et que le courrier indésirable ne sera pas renvoyé. Vous trouverez plus d'informations sur l'ouverture d'un cas de support [ici](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="48a0e-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="48a0e-130">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="48a0e-130">For more information</span></span>

[<span data-ttu-id="48a0e-131">Protection contre le courrier indésirable pour Office 365</span><span class="sxs-lookup"><span data-stu-id="48a0e-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="48a0e-132">Envoyer les notifications d'échec de remise par courrier électronique dans Office 365</span><span class="sxs-lookup"><span data-stu-id="48a0e-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="48a0e-133">Configurer le transfert du courrier pour une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="48a0e-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="48a0e-134">Comment configurer une application ou un périphérique multi-fonction pour envoyer des courriers électroniques à l’aide d’Office 365</span><span class="sxs-lookup"><span data-stu-id="48a0e-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="48a0e-135">[Gérer les domaines acceptés dans Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="48a0e-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
