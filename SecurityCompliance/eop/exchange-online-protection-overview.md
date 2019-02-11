---
title: Vue d'ensemble d'Exchange Online Protection
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 01/31/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft Exchange Online Protection (EOP) est un service de filtrage du courrier électronique dans le nuage, qui contribue à protéger votre organisation contre le courrier indésirable et les logiciels malveillants, ainsi que contre les violations de politique de messagerie.
ms.openlocfilehash: 16f2f423b6e517cf204e4b4f6a2949baebfd6223
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686363"
---
# <a name="exchange-online-protection-overview"></a><span data-ttu-id="09d72-103">Vue d'ensemble d'Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="09d72-103">Exchange Online Protection overview</span></span>

<span data-ttu-id="09d72-p101">Microsoft Exchange Online Protection (EOP) est un service de filtrage du courrier électronique dans le nuage, qui contribue à protéger votre organisation contre le courrier indésirable et les logiciels malveillants, ainsi que contre les violations de stratégie de messagerie. EOP peut simplifier la gestion de votre environnement de messagerie et alléger bon nombre des tâches liées à la maintenance du matériel et des logiciels locaux.</span><span class="sxs-lookup"><span data-stu-id="09d72-p101">Microsoft Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware, and includes features to safeguard your organization from messaging-policy violations. EOP can simplify the management of your messaging environment and alleviate many of the burdens that come with maintaining on-premises hardware and software.</span></span>
  
<span data-ttu-id="09d72-106">Les principales manières d'utiliser EOP pour protéger la messagerie sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="09d72-106">The following are the primary ways you can use EOP for messaging protection:</span></span>
  
- <span data-ttu-id="09d72-107">**Dans un scénario autonome** EOP offre une protection de messagerie en nuage pour votre environnement Microsoft Exchange Server 2013 sur site, versions héritées d’Exchange Server, ou pour n’importe quel autre local solution de messagerie SMTP.</span><span class="sxs-lookup"><span data-stu-id="09d72-107">**In a standalone scenario** EOP provides cloud-based email protection for your on-premises Microsoft Exchange Server 2013 environment, legacy Exchange Server versions, or for any other on-premises SMTP email solution.</span></span> 
    
- <span data-ttu-id="09d72-108">**Dans le cadre d'une installation Microsoft Exchange Online** Par défaut, EOP protège les boîtes aux lettres Microsoft Exchange Online hébergées dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="09d72-108">**As a part of Microsoft Exchange Online** By default, EOP protects Microsoft Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="09d72-109">**Dans un déploiement hybride** EOP peut être configuré pour protéger votre environnement de messagerie et contrôler le routage de messagerie quand vous disposez d'une combinaison de boîtes aux lettres locales et en nuage.</span><span class="sxs-lookup"><span data-stu-id="09d72-109">**In a hybrid deployment** EOP can be configured to protect your messaging environment and control mail routing when you have a mix of on-premises and cloud mailboxes.</span></span> 
    
## <a name="how-eop-works"></a><span data-ttu-id="09d72-110">Fonctionnement d'EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-110">How EOP works</span></span>

<span data-ttu-id="09d72-111">Pour comprendre le fonctionnement d'EOP, il est utile devoir comment le courrier entrant est traité :</span><span class="sxs-lookup"><span data-stu-id="09d72-111">To understand how EOP works, it helps to see how it processes incoming email:</span></span>
  
![Traitement de messagerie EOP](../media/EOP-email-processing.png)
  
<span data-ttu-id="09d72-p102">Un message entrant à l’origine traverse le filtrage des connexions, qui vérifie la réputation de l’expéditeur et examine le message pour les logiciels malveillants. La majorité du courrier indésirable est arrêtée à ce stade et supprimée par EOP. Continuent de messages par le biais de filtrage de stratégie, où les messages sont évaluées par rapport aux règles de transport personnalisé que vous créez ou appliquer à partir d’un modèle. Par exemple, vous pouvez avoir une règle qui envoie une notification à un responsable de l’arrivée de messagerie d’un expéditeur spécifique. (Contrôles de protection contre la perte de données également se produisent à ce stade, si vous disposez des fonctionnalités ; pour plus d’informations sur la disponibilité des fonctionnalités, voir la [Description du Service Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Ensuite, messages passent par le filtrage du contenu, où le contenu est activé pour la terminologie ou propriétés communes de courrier indésirable. Un message déterminé le courrier indésirable par le filtre de contenu peut être envoyé vers le dossier de courrier indésirable d’un utilisateur ou à la mise en quarantaine, entre autres options, en fonction de vos paramètres. Une fois un message est un succès de ces différentes couches de protection, il est remis au destinataire.</span><span class="sxs-lookup"><span data-stu-id="09d72-p102">An incoming message initially passes through connection filtering, which checks the sender's reputation and inspects the message for malware. The majority of spam is stopped at this point and deleted by EOP. Messages continue through policy filtering, where messages are evaluated against custom transport rules that you create or enforce from a template. For example, you can have a rule that sends a notification to a manager when mail arrives from a specific sender. (Data loss prevention checks also occur at this point, if you have that feature; for information about feature availability, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Next, messages pass through content filtering, where content is checked for terminology or properties common to spam. A message determined to be spam by the content filter can be sent to a user's Junk Email folder or to the quarantine, among other options, based on your settings. After a message passes all of these protection layers successfully, it's delivered to the recipient.</span></span>
  
### <a name="eop-datacenters"></a><span data-ttu-id="09d72-120">Centres de données EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-120">EOP datacenters</span></span>

<span data-ttu-id="09d72-p103">EOP s'exécute sur un réseau mondial de centres de données conçus pour offrir une disponibilité optimale. Par exemple, si un centre de données devient indisponible, les courriers électroniques sont automatiquement routés vers un autre centre de données sans interruption du service. Les serveurs de chaque centre de données acceptent les messages à votre place, en créant une couche de séparation entre votre organisation et Internet, réduisant ainsi la charge pesant sur vos serveurs. Grâce à ce réseau à haut niveau de disponibilité, Microsoft peut garantir que le courrier atteint votre organisation en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="09d72-p103">EOP runs on a worldwide network of datacenters that are designed to provide the best availability. For example, if a datacenter becomes unavailable, email messages are automatically routed to another datacenter without any interruption in service. Servers in each datacenter accept messages on your behalf, providing a layer of separation between your organization and the Internet, thereby reducing load on your servers. Through this highly available network, Microsoft can ensure that email reaches your organization in a timely manner.</span></span> 
  
<span data-ttu-id="09d72-p104">EOP effectue l'équilibrage de charge entre les centres de données, mais uniquement au sein d'une région. Si votre système est mis en service dans une région, tous vos messages seront traités sur la base du routage de courrier propre à cette région. La liste suivante présente le fonctionnement du routage de courrier régional pour les centres de données EOP :</span><span class="sxs-lookup"><span data-stu-id="09d72-p104">EOP performs load balancing between datacenters but only within a region. If you're provisioned in one region all your messages will be processed using the mail routing for that region. The following list shows the how regional mail routing works for the EOP datacenters:</span></span>
  
    
- <span data-ttu-id="09d72-128">En Europe, au Moyen-Orient et en Afrique (région EMEA), toutes les boîtes aux lettres Exchange Online sont situées dans des centres de données EMEA et tous les messages sont routés via des centres de données EMEA pour le filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="09d72-128">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="09d72-129">Dans Asie-Pacifique (centre de données), toutes les boîtes aux lettres Exchange Online sont trouvent dans des centres de données APAC, mais les messages sont acheminés actuellement par le biais de centres de données APAC pour le filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="09d72-129">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, but messages are currently routed through APAC datacenters for EOP filtering.</span></span>
=======
- <span data-ttu-id="09d72-p105">En Amérique, toutes les boîtes aux lettres Exchange Online se trouvent dans des centres de données américain, à l’exception de l’Amérique du Sud où les centres de données au Brésil et Chili sont utilisés et au Canada, où les centres de données au Canada sont utilisés. Tous les messages électroniques, y compris les messages pour les clients en Amérique du Sud et au Canada, sont acheminés via des centres de données local pour le filtrage EOP ; courrier électronique placés en quarantaine est stocké dans le centre de données où se trouve le client.</span><span class="sxs-lookup"><span data-stu-id="09d72-p105">In the Americas, all Exchange Online mailboxes are located in U.S. datacenters, with the exception of South America where datacenters in Brazil and Chile are used and in Canada where datacenters in Canada are used. All email messages, including messages for customers in South America and Canada, are routed through local datacenters for EOP filtering; quaratined email is stored in the datacenter where the tenant is located.</span></span>
    
- <span data-ttu-id="09d72-132">En Europe, au Moyen-Orient et en Afrique (région EMEA), toutes les boîtes aux lettres Exchange Online sont situées dans des centres de données EMEA et tous les messages sont routés via des centres de données EMEA pour le filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="09d72-132">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="09d72-133">Dans Asie-Pacifique (centre de données), toutes les boîtes aux lettres Exchange Online sont trouvent dans des centres de données APAC et messages sont actuellement acheminés via APAC des centres de données pour le filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="09d72-133">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, and messages are currently routed through APAC datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="09d72-134">En ce qui concerne le nuage communautaire propre aux gouvernements (CCG), toutes les boîtes aux lettres Exchange Online sont situées dans des centres de données américains et tous les messages sont routés via ces centres de données pour le filtrage EOP.</span><span class="sxs-lookup"><span data-stu-id="09d72-134">For the Government Community Cloud (GCC), all Exchange Online mailboxes are located in U.S. datacenters and all messages are routed through U.S. datacenters for EOP filtering.</span></span>
    
## <a name="eop-plans-and-features"></a><span data-ttu-id="09d72-135">Plans et fonctionnalités d'EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-135">EOP plans and features</span></span>

<span data-ttu-id="09d72-136">Les plans d'abonnement EOP disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="09d72-136">The following are the available EOP subscription plans:</span></span>
  
- <span data-ttu-id="09d72-137">**EOP autonome** EOP protège vos boîtes de données locales.</span><span class="sxs-lookup"><span data-stu-id="09d72-137">**EOP standalone** Where EOP protects your on-premises mailboxes.</span></span> 
    
- <span data-ttu-id="09d72-138">**Fonctionnalités EOP dans Exchange Online** EOP protège vos boîtes aux lettres Exchange Online en nuage.</span><span class="sxs-lookup"><span data-stu-id="09d72-138">**EOP features in Exchange Online** Where EOP protects your Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="09d72-139">**Licence d'accès client Exchange Enterprise avec Services** EOP protège vos boîtes aux lettres sur site, comme EOP autonome, et inclut des fonctionnalités de protection contre la perte de données et de reporting à l'aide de services web.</span><span class="sxs-lookup"><span data-stu-id="09d72-139">**Exchange Enterprise CAL with Services** Where EOP protects your on-premises mailboxes, like EOP standalone, and includes data loss prevention (DLP) and reporting using web services.</span></span> 
    
<span data-ttu-id="09d72-140">Pour plus d'informations sur la configuration requise, les limites importantes et la disponibilité des fonctionnalités dans tous les plans d'abonnement EOP, voir [Description du service de protection Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span><span class="sxs-lookup"><span data-stu-id="09d72-140">For information about requirements, important limits, and feature availability across all EOP subscription plans, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span></span>
  
## <a name="setting-up-eop"></a><span data-ttu-id="09d72-141">Configuration d'EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-141">Setting up EOP</span></span>

<span data-ttu-id="09d72-p106">La configuration d'EOP peut être simple, en particulier dans le cas d'une organisation de taille modeste appliquant un nombre restreint de règles de conformité. En revanche, si votre organisation est de grande taille, avec plusieurs domaines, des règles de conformité personnalisées ou un flux de messagerie hybride, la configuration peut nécessiter plus de temps et de travail de planification.</span><span class="sxs-lookup"><span data-stu-id="09d72-p106">Setting up EOP can be simple, especially in the case of a small organization with a handful of compliance rules. However, if you have a large organization with multiple domains, custom compliance rules, or hybrid mail flow, set up can take more planning and time.</span></span>
  
<span data-ttu-id="09d72-144">Si vous avez déjà acheté EOP, consultez la rubrique [Configurer votre service EOP](set-up-your-eop-service.md) pour être certain d'accomplir toutes les étapes nécessaires à la configuration d'EOP pour la protection de votre environnement de messagerie.</span><span class="sxs-lookup"><span data-stu-id="09d72-144">If you've already purchased EOP, see [Set up your EOP service](set-up-your-eop-service.md) to ensure that you complete all the steps necessary to configure EOP to protect your messaging environment.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="09d72-145">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="09d72-145">For more information</span></span>

[<span data-ttu-id="09d72-146">Fonctionnalités EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-146">EOP features</span></span>](eop-features.md)
  
[<span data-ttu-id="09d72-147">Vidéos pour démarrer avec EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-147">Videos for getting started with EOP</span></span>](videos-for-getting-started-with-eop.md)
  
[<span data-ttu-id="09d72-148">Forum Aux Questions d'ordre général concernant Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="09d72-148">EOP general FAQ</span></span>](eop-general-faq.md)
  
<span data-ttu-id="09d72-149">Questions fréquemment posées sur les messages mis en file d’attente, différés et retournés dans EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-149">[EOP queued, deferred, and bounced messages FAQ](eop-queued-deferred-and-bounced-messages-faq.md)</span></span>
  
[<span data-ttu-id="09d72-150">FAQ sur l'administration déléguée</span><span class="sxs-lookup"><span data-stu-id="09d72-150">Delegated administration FAQ</span></span>](delegated-administration-faq.md)
  
[<span data-ttu-id="09d72-151">Déplacement de domaines et de paramètres d'une organisation EOP vers une autre organisation EOP</span><span class="sxs-lookup"><span data-stu-id="09d72-151">Move domains and settings from one EOP organization to another EOP organization</span></span>](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  

