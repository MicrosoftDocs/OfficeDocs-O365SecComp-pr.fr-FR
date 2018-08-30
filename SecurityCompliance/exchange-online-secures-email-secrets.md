---
title: Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
description: En plus du Centre Office 365 confiance qui fournit des informations de conformité, de confidentialité et de sécurité pour Office 365, vous voudrez peut-être savoir comment Office 365 vous aide à protéger les clés secrètes que vous fournissez dans ses centres de données. Nous utilisons une technologie appelée Gestionnaire de clé distribué (DKM).
ms.openlocfilehash: a8fe1a2c9393958a391ec69a9a476a06de8c7576
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528626"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="0442b-104">Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0442b-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="0442b-105">Cet article décrit la façon dont Microsoft protège les informations confidentielles figurant dans vos courriers électroniques dans ses centres de données.</span><span class="sxs-lookup"><span data-stu-id="0442b-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="0442b-106">Comment sécurisons-nous les informations confidentielles que vous indiquez ?</span><span class="sxs-lookup"><span data-stu-id="0442b-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="0442b-p102">En plus du Centre Office 365 confiance qui fournit des [informations de conformité pour Office 365, de confidentialité et de sécurité](https://go.microsoft.com/fwlink/?linkid=874644), vous voudrez peut-être savoir comment Office 365 vous aide à protéger les clés secrètes que vous fournissez dans ses centres de données. Nous utilisons une technologie appelée Gestionnaire de clé distribué (DKM).</span><span class="sxs-lookup"><span data-stu-id="0442b-p102">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters. We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="0442b-p103">Le Gestionnaire de clés distribuées (DKM) est une fonctionnalité côté client qui utilise un ensemble de clés secrètes pour chiffrer et déchiffrer des informations. Seuls les membres d’un groupe de sécurité spécifiques dans les services de domaine Active Directory peuvent accéder à ces clés dans le but de déchiffrer les données chiffrées par le Gestionnaire de clés distribuées. Dans Exchange Online, seuls certains comptes de service sous lesquels les processus Exchange sont exécutés font partie de ce groupe de sécurité. Dans le cadre de la procédure opérationnelle standard dans le centre de données, les informations d’identification qui font partie de ce groupe de sécurité ne sont communiquées à aucun être humain, et par conséquent aucun être humain n’a accès aux clés qui peuvent déchiffrer les informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="0442b-p103">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information. Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM. In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group. As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="0442b-p104">À des fins de débogage, de résolution des problèmes ou d’audit, un administrateur de centre de données doit demander un accès élevé pour obtenir des informations d’identification temporaires qui font partie du groupe de sécurité. Ce processus requiert plusieurs niveaux d’approbation juridique. Si l’accès est accordé, toutes les activités font l’objet d’une journalisation et d’un audit. En outre, l’accès est accordé uniquement pour un intervalle de temps défini suite auquel il expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0442b-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="0442b-p105">Pour une protection supplémentaire, la technologie DKM inclut l’archivage et la substitution de clé automatisés. Ainsi, vous pouvez continuer à accéder à votre contenu plus ancien sans devoir utiliser la même clé indéfiniment.
</span><span class="sxs-lookup"><span data-stu-id="0442b-p105">For extra protection, DKM technology includes automated key rollover and archiving. This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="0442b-119">Où le Gestionnaire de clés distribuées est-il utilisé dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="0442b-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="0442b-p106">Microsoft utilise le Gestionnaire de clés distribuées pour chiffrer vos informations confidentielles dans les centres de données Exchange Online. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0442b-p106">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters. For example:</span></span>
  
- <span data-ttu-id="0442b-p107">Les informations d’identification de compte de messagerie pour les comptes connectés. Les comptes connectés sont des comptes tiers, tels que les comptes de messagerie Hotmail, Gmail et Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="0442b-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>
    
- <span data-ttu-id="0442b-p108">Les droits de touches racine de gestion des services (RMS). Il s’agit des clés de client qui sont que soit importés à partir de RMS Azure ou de déploiements de RMS Services de domaine Active Directory local du client qui sont utilisés pour chiffrer et déchiffrer les messages électroniques avec RMS ou Office 365 Message Encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="0442b-p108">Rights Management service (RMS) root keys. These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="0442b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0442b-127">Related topics</span></span>

[<span data-ttu-id="0442b-128">Chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0442b-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="0442b-129">Informations de référence technique de chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0442b-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="0442b-130">Service d’assurance de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="0442b-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  

