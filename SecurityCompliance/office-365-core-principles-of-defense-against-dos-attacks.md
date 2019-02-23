---
title: Principes de base de la protection Office 365 contre les attaques par déni de service
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Utilisation des principes de base de l'absorption, de la détection et de l'atténuation dans sa défense contre les attaques par déni de service (DoS).
ms.openlocfilehash: dfe179924f7414b0120697023f3daf7e6b6661b6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216004"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Principes fondamentaux de défense contre les attaques par déni de service

Les trois principes fondamentaux de la défense contre les attaques DoS sur le réseau sont l'absorption, la détection et l'atténuation. L'absorption se produit avant la détection et la détection a lieu avant l'atténuation. L'absorption est la meilleure défense contre les attaques DoS. Si l'attaque ne peut pas être détectée, elle ne peut pas être atténuée. Toutefois, si même la plus petite attaque de refus de service ne peut pas être absorbée, les services ne seront pas en mesure de survivre suffisamment longtemps pour que l'attaque soit détectée.

Bien évidemment, il n'est généralement pas raisonnable de faire en sorte que la plupart des organisations achètent les capacités excédentaires nécessaires pour absorber les attaques par déni de service, car cela nécessite un investissement considérable en matière de technologies et de compétences techniques. Cela met en évidence l'un des avantages en matière de sécurité liés à l'utilisation des services de Cloud Computing Microsoft; la grande ampleur de nos services nous permet de fournir une protection réseau solide à nos clients Cloud de façon rentable. Toutefois, même à notre montée en taille, il doit encore y avoir un équilibre entre l'absorption, la détection et l'atténuation. Pour trouver cet équilibre, nous évaluons le taux de croissance d'une attaque afin d'estimer le montant à absorber.

La détection est un jeu de chat et de souris. Vous devez constamment Rechercher les nouvelles façons dont les personnes s'attaquent ou tentent de contrer vos systèmes. Detect-> mitigation-> Detect-> minimisation, etc., est un État perpétuel, persistant, qui se poursuivra indéfiniment.

## <a name="defending-against-dos-attacks"></a>Défense contre les attaques DoS

Pour être en mesure de vous défendre contre une attaque DoS, la détection précoce est essentielle. En détectant une attaque avant que le système ne soit submergé, les défenseurs peuvent exécuter un plan de réponse.

La formule suivante vous aidera à évaluer approximativement le temps nécessaire à l'impact d'une attaque DoS:

   **Capacité maximale (en octets/s)/taux de croissance (en octets/s) = temps d'impact (en octets/s)**

Si le délai de détection a lieu après l'impact, il est probable que l'attaque de refus de service se produise. Si le délai de détection a lieu avant l'impact, les services en cours d'attaque doivent rester en ligne et accessibles, si des stratégies de minimisation sont utilisées. Ainsi, il y a deux choses à faire pour vous défendre contre les attaques de refus de déni de compte:
- Augmentation de la capacité pour augmenter le plafond de la capacité maximale (qui, à son tour, offre plus de temps pour détecter une attaque); des
- Réduisez le temps de détection.

Une augmentation de la capacité a un impact fiscal direct. Microsoft recommande aux clients de développer au moins une capacité d'absorption de base pour s'assurer qu'ils peuvent survivre à un certain niveau d'attaques DoS. La capacité d'absorption réelle varie selon le client et le client, car chaque client a ses propres seuils d'exposition, de risque et de dépenses financières. Enfin, pour des raisons économiques, les investissements en matière de recherche et de temps pour réduire le temps de détection sont généralement la défense la plus économique.
