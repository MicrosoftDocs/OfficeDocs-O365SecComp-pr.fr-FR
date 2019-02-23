---
title: Défense contre les attaques par déni de service dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Vue d'ensemble des attaques par déni de service (DoS).
ms.openlocfilehash: 246704bff18c07d9b76281ae3c7071cd0d747630
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220504"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="47d79-103">Défense contre les attaques par déni de service dans Office 365</span><span class="sxs-lookup"><span data-stu-id="47d79-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="47d79-104">Introduction</span><span class="sxs-lookup"><span data-stu-id="47d79-104">Introduction</span></span>
<span data-ttu-id="47d79-105">Microsoft propose une infrastructure de confiance pour plus de 200 services Cloud, notamment Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype et Xbox Live hébergés dans notre Cloud global infrastructure de plus de 100 centres de informations.</span><span class="sxs-lookup"><span data-stu-id="47d79-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="47d79-p101">En tant qu'organisation mondiale avec une présence Internet importante et de nombreuses propriétés Internet importantes qui fournissent des services en nuage, Microsoft est une cible commune et commune aux pirates et autres personnes malveillantes. Le réseau, la couche communication entre les clients et le Cloud Microsoft, est l'une des principales cibles d'attaques malveillantes. En fait, depuis de nombreuses années, Microsoft a cessé de se conformer de façon continue et permanente sous certaines conditions de cyber basées sur le réseau. Presque toutes les fois, au moins une des propriétés Internet de Microsoft rencontre une attaque. Sans systèmes d'atténuation fiables et persistants capables de se défendre contre ces attaques, les services Cloud de Microsoft seraient hors ligne et indisponibles pour les clients.</span><span class="sxs-lookup"><span data-stu-id="47d79-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="47d79-111">Microsoft utilise des principes de sécurité de défense en profondeur pour protéger ses services et réseaux Cloud.</span><span class="sxs-lookup"><span data-stu-id="47d79-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="47d79-112">Définition et symptômes des attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="47d79-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="47d79-p102">Pour attaquer les services réseau, il est possible de créer plusieurs requêtes sur les hôtes d'un service afin de submerger le réseau et les serveurs afin de refuser les services aux utilisateurs légitimes. Il s'agit d'une attaque par déni de service (DoS). Lorsque l'attaque est effectuée par plusieurs acteurs, points de terminaison et/ou vecteurs, elle est considérée comme une attaque de déni de service distribuée. Bien que les moyens, les motivations et les cibles varient, les attaques DoS et DDoS consistent généralement en les efforts de la personne ou des personnes pour empêcher un site ou un service Internet de fonctionner correctement ou de façon temporaire ou indéfinie.</span><span class="sxs-lookup"><span data-stu-id="47d79-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="47d79-117">L'équipe américaine de préparation de l' [urgence informatique](https://www.us-cert.gov/) (US-CERT) définit les symptômes des attaques par déni:</span><span class="sxs-lookup"><span data-stu-id="47d79-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="47d79-118">Ralentissement des performances réseau (lors de l'ouverture de fichiers ou accès aux sites Internet)</span><span class="sxs-lookup"><span data-stu-id="47d79-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="47d79-119">Indisponibilité d'un site Web</span><span class="sxs-lookup"><span data-stu-id="47d79-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="47d79-120">ImPossibilité d'accéder à un site Web</span><span class="sxs-lookup"><span data-stu-id="47d79-120">Inability to access a Web site</span></span>
- <span data-ttu-id="47d79-121">Augmentation spectaculaire du courrier indésirable reçu</span><span class="sxs-lookup"><span data-stu-id="47d79-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="47d79-122">Déconnexion d'une connexion Internet câblée ou sans fil</span><span class="sxs-lookup"><span data-stu-id="47d79-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="47d79-123">Perte d'accès à long terme pour le Web ou tout service Internet</span><span class="sxs-lookup"><span data-stu-id="47d79-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="47d79-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47d79-124">Related Topics</span></span>
- [<span data-ttu-id="47d79-125">Principes fondamentaux de défense contre les attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="47d79-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="47d79-126">Stratégie de défense contre les attaques par déni de service de Microsoft</span><span class="sxs-lookup"><span data-stu-id="47d79-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="47d79-127">Protection des services de Cloud Computing Microsoft contre les attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="47d79-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
