---
title: Défense contre les attaques par déni de service dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Vue d'ensemble des attaques par déni de service (DoS).
ms.openlocfilehash: a7e67fcc87867190f345c5dad14e38a473420eab
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262816"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="fcd9d-103">Défense contre les attaques par déni de service dans Office 365</span><span class="sxs-lookup"><span data-stu-id="fcd9d-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="fcd9d-104">Introduction</span><span class="sxs-lookup"><span data-stu-id="fcd9d-104">Introduction</span></span>
<span data-ttu-id="fcd9d-105">Microsoft propose une infrastructure de confiance pour plus de 200 services Cloud, notamment Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype et Xbox Live hébergés dans notre Cloud global infrastructure de plus de 100 centres de informations.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="fcd9d-106">En tant qu'organisation mondiale avec une présence Internet importante et de nombreuses propriétés Internet importantes qui fournissent des services en nuage, Microsoft est une cible commune et commune aux pirates et autres personnes malveillantes.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-106">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="fcd9d-107">Le réseau, la couche communication entre les clients et le Cloud Microsoft, est l'une des principales cibles d'attaques malveillantes.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-107">The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="fcd9d-108">En fait, depuis de nombreuses années, Microsoft a cessé de se conformer de façon continue et permanente sous certaines conditions de cyber basées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-108">In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="fcd9d-109">Presque toutes les fois, au moins une des propriétés Internet de Microsoft rencontre une attaque.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-109">At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack.</span></span> <span data-ttu-id="fcd9d-110">Sans systèmes d'atténuation fiables et persistants capables de se défendre contre ces attaques, les services Cloud de Microsoft seraient hors ligne et indisponibles pour les clients.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-110">Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="fcd9d-111">Microsoft utilise des principes de sécurité de défense en profondeur pour protéger ses services et réseaux Cloud.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="fcd9d-112">Définition et symptômes des attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="fcd9d-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="fcd9d-113">Pour attaquer les services réseau, il est possible de créer plusieurs requêtes sur les hôtes d'un service afin de submerger le réseau et les serveurs afin de refuser les services aux utilisateurs légitimes.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-113">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="fcd9d-114">Il s'agit d'une attaque par déni de service (DoS).</span><span class="sxs-lookup"><span data-stu-id="fcd9d-114">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="fcd9d-115">Lorsque l'attaque est effectuée par plusieurs acteurs, points de terminaison et/ou vecteurs, elle est considérée comme une attaque de déni de service distribuée.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-115">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="fcd9d-116">Bien que les moyens, les motivations et les cibles varient, les attaques DoS et DDoS consistent généralement en les efforts de la personne ou des personnes pour empêcher un site ou un service Internet de fonctionner correctement ou de façon temporaire ou indéfinie.</span><span class="sxs-lookup"><span data-stu-id="fcd9d-116">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="fcd9d-117">L'équipe américaine de préparation de l' [urgence informatique](https://www.us-cert.gov/) (US-CERT) définit les symptômes des attaques par déni:</span><span class="sxs-lookup"><span data-stu-id="fcd9d-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="fcd9d-118">Ralentissement des performances réseau (lors de l'ouverture de fichiers ou accès aux sites Internet)</span><span class="sxs-lookup"><span data-stu-id="fcd9d-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="fcd9d-119">Indisponibilité d'un site Web</span><span class="sxs-lookup"><span data-stu-id="fcd9d-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="fcd9d-120">ImPossibilité d'accéder à un site Web</span><span class="sxs-lookup"><span data-stu-id="fcd9d-120">Inability to access a Web site</span></span>
- <span data-ttu-id="fcd9d-121">Augmentation spectaculaire du courrier indésirable reçu</span><span class="sxs-lookup"><span data-stu-id="fcd9d-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="fcd9d-122">Déconnexion d'une connexion Internet câblée ou sans fil</span><span class="sxs-lookup"><span data-stu-id="fcd9d-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="fcd9d-123">Perte d'accès à long terme pour le Web ou tout service Internet</span><span class="sxs-lookup"><span data-stu-id="fcd9d-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcd9d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcd9d-124">Related Topics</span></span>
- [<span data-ttu-id="fcd9d-125">Principes fondamentaux de défense contre les attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="fcd9d-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="fcd9d-126">Stratégie de défense contre les attaques par déni de service de Microsoft</span><span class="sxs-lookup"><span data-stu-id="fcd9d-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="fcd9d-127">Protection des services de Cloud Computing Microsoft contre les attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="fcd9d-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
