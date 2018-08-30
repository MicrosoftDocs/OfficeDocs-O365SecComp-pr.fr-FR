---
title: Défense contre les attaques par déni de Service dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Vue d’ensemble des attaques par déni de Service (DoS).
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527495"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="ed00c-103">Défense contre les attaques par déni de Service dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ed00c-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="ed00c-104">Présentation</span><span class="sxs-lookup"><span data-stu-id="ed00c-104">Introduction</span></span>
<span data-ttu-id="ed00c-105">Microsoft fournit une infrastructure fiable pour plus de 200 services en nuage, y compris Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype et Xbox Live qui sont hébergées dans notre nuage global infrastructure de centres de données plus de 100.</span><span class="sxs-lookup"><span data-stu-id="ed00c-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="ed00c-p101">En tant qu’une organisation globale avec une présence Internet significative et de nombreuses propriétés visibles Internet qui fournissent des services en nuage, Microsoft est une cible volumineux, courantes des pirates informatiques et d’autres personnes malveillantes. --Le réseau de la couche de communication entre les clients et le Cloud Microsoft--est un des objectifs principaux d’attaques malveillantes. En fait, de nombreuses années, Microsoft a été en continu et de façon permanente sous une forme d’opérations sur le réseau. Presque à tout moment, au moins une des propriétés de Internet de Microsoft rencontre une forme d’attaque. Sans systèmes atténuation fiable et permanente qui protège contre les attaques, les services en nuage de Microsoft serait en mode hors connexion et indisponible pour les clients.</span><span class="sxs-lookup"><span data-stu-id="ed00c-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="ed00c-111">Microsoft utilise les principes de sécurité de défense en profondeur pour protéger ses services en nuage et les réseaux.</span><span class="sxs-lookup"><span data-stu-id="ed00c-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="ed00c-112">Définition et symptômes d’attaques par déni de Service</span><span class="sxs-lookup"><span data-stu-id="ed00c-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="ed00c-p102">Une manière d’attaques de services réseau consiste à créer de nombreuses demandes par rapport à des hôtes d’un service de provoquer une saturation du réseau et les serveurs refus de service pour les utilisateurs légitimes. Il est appelé une attaque de par déni de service (DoS). Lors de l’attaque par plusieurs acteurs, des points de terminaison et/ou des vecteurs, il est appelé une attaque de (par déni) distribuée par déni de service. Bien que les moyens, motifs et cibles varient, les attaques par déni de service et par déni se composent généralement des efforts d’une personne ou les personnes pour empêcher un site Internet ou le service de fonctionner correctement ou tout titre temporaire ou indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="ed00c-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="ed00c-117">Les [États-Unis Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) définit les symptômes d’attaques DoS à inclure :</span><span class="sxs-lookup"><span data-stu-id="ed00c-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="ed00c-118">Anormalement ralentir les performances du réseau (lors de l’ouverture de fichiers ou d’accéder aux sites Internet)</span><span class="sxs-lookup"><span data-stu-id="ed00c-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="ed00c-119">Indisponibilité d’un site Web</span><span class="sxs-lookup"><span data-stu-id="ed00c-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="ed00c-120">Impossibilité d’accéder à un site Web</span><span class="sxs-lookup"><span data-stu-id="ed00c-120">Inability to access a Web site</span></span>
- <span data-ttu-id="ed00c-121">Augmentation considérable de courrier indésirable entrant</span><span class="sxs-lookup"><span data-stu-id="ed00c-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="ed00c-122">Déconnexion d’une connexion Internet sans fil ou câblée</span><span class="sxs-lookup"><span data-stu-id="ed00c-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="ed00c-123">Perte à long terme de l’accès sur le Web ou les services Internet</span><span class="sxs-lookup"><span data-stu-id="ed00c-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed00c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed00c-124">Related Topics</span></span>
- [<span data-ttu-id="ed00c-125">Principes fondamentaux de la défense contre les attaques par déni de Service</span><span class="sxs-lookup"><span data-stu-id="ed00c-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="ed00c-126">Stratégie de défense par déni de Service de Microsoft</span><span class="sxs-lookup"><span data-stu-id="ed00c-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="ed00c-127">Protection contre les attaques par déni de Service des Services de Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="ed00c-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
