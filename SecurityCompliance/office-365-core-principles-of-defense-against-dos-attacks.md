---
title: Principes de base de la protection Office 365 contre les attaques par déni de service
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Utilisation des principes de base de l'absorption, de la détection et de l'atténuation dans sa défense contre les attaques par déni de service (DoS).
ms.openlocfilehash: 17dc583258cdb4781dbe2a715e1ce153ee769ed3
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091006"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="1ec39-103">Principes fondamentaux de défense contre les attaques par déni de service</span><span class="sxs-lookup"><span data-stu-id="1ec39-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>

<span data-ttu-id="1ec39-p101">Les trois principes fondamentaux de la défense contre les attaques DoS sur le réseau sont l'absorption, la détection et l'atténuation. L'absorption se produit avant la détection et la détection a lieu avant l'atténuation. L'absorption est la meilleure défense contre les attaques DoS. Si l'attaque ne peut pas être détectée, elle ne peut pas être atténuée. Toutefois, si même la plus petite attaque de refus de service ne peut pas être absorbée, les services ne seront pas en mesure de survivre suffisamment longtemps pour que l'attaque soit détectée.</span><span class="sxs-lookup"><span data-stu-id="1ec39-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="1ec39-p102">Bien évidemment, il n'est généralement pas raisonnable de faire en sorte que la plupart des organisations achètent les capacités excédentaires nécessaires pour absorber les attaques par déni de service, car cela nécessite un investissement considérable en matière de technologies et de compétences techniques. Cela met en évidence l'un des avantages en matière de sécurité liés à l'utilisation des services de Cloud Computing Microsoft; la grande ampleur de nos services nous permet de fournir une protection réseau solide à nos clients Cloud de façon rentable. Toutefois, même à notre montée en taille, il doit encore y avoir un équilibre entre l'absorption, la détection et l'atténuation. Pour trouver cet équilibre, nous évaluons le taux de croissance d'une attaque afin d'estimer le montant à absorber.</span><span class="sxs-lookup"><span data-stu-id="1ec39-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="1ec39-p103">La détection est un jeu de chat et de souris. Vous devez constamment Rechercher les nouvelles façons dont les personnes s'attaquent ou tentent de contrer vos systèmes. Detect-> mitigation-> Detect-> minimisation, etc., est un État perpétuel, persistant, qui se poursuivra indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="1ec39-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="1ec39-116">Défense contre les attaques DoS</span><span class="sxs-lookup"><span data-stu-id="1ec39-116">Defending Against DoS Attacks</span></span>

<span data-ttu-id="1ec39-p104">Pour être en mesure de vous défendre contre une attaque DoS, la détection précoce est essentielle. En détectant une attaque avant que le système ne soit submergé, les défenseurs peuvent exécuter un plan de réponse.</span><span class="sxs-lookup"><span data-stu-id="1ec39-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="1ec39-119">La formule suivante vous aidera à évaluer approximativement le temps nécessaire à l'impact d'une attaque DoS:</span><span class="sxs-lookup"><span data-stu-id="1ec39-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="1ec39-120">**Capacité maximale (en octets/s)/taux de croissance (en octets/s) = temps d'impact (en octets/s)**</span><span class="sxs-lookup"><span data-stu-id="1ec39-120">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in bytes/sec)**</span></span>

<span data-ttu-id="1ec39-p105">Si le délai de détection a lieu après l'impact, il est probable que l'attaque de refus de service se produise. Si le délai de détection a lieu avant l'impact, les services en cours d'attaque doivent rester en ligne et accessibles, si des stratégies de minimisation sont utilisées. Ainsi, il y a deux choses à faire pour vous défendre contre les attaques de refus de déni de compte:</span><span class="sxs-lookup"><span data-stu-id="1ec39-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="1ec39-124">Augmentation de la capacité pour augmenter le plafond de la capacité maximale (qui, à son tour, offre plus de temps pour détecter une attaque); des</span><span class="sxs-lookup"><span data-stu-id="1ec39-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="1ec39-125">Réduisez le temps de détection.</span><span class="sxs-lookup"><span data-stu-id="1ec39-125">Decrease the time to detect.</span></span>

<span data-ttu-id="1ec39-p106">Une augmentation de la capacité a un impact fiscal direct. Microsoft recommande aux clients de développer au moins une capacité d'absorption de base pour s'assurer qu'ils peuvent survivre à un certain niveau d'attaques DoS. La capacité d'absorption réelle varie selon le client et le client, car chaque client a ses propres seuils d'exposition, de risque et de dépenses financières. Enfin, pour des raisons économiques, les investissements en matière de recherche et de temps pour réduire le temps de détection sont généralement la défense la plus économique.</span><span class="sxs-lookup"><span data-stu-id="1ec39-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
