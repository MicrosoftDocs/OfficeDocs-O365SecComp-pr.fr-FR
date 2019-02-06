---
title: Principes de base d’Office 365 de défense contre les attaques par déni de Service
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Comment Microsoft utilise les principes fondamentaux d’absorber, la détection et atténuation dans sa défense contre les attaques de déni de service (DoS).
ms.openlocfilehash: e313d5514e9bc493db78bebffca24a0fae4cbca7
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741097"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Principes fondamentaux de défense contre les attaques par déni de service

Les trois principaux principes lors de la défense contre les attaques de déni de service sur le réseau est absorber, la détection et atténuation. Absorber se produit avant la détection et détection se produit avant l’atténuation. Absorber est la meilleure défense attaques de déni de service. Si l’attaque ne peut pas être détectée, il ne peut pas être atténué. Mais si même la plus petite attaques DOS ne peut pas être pris en charge, puis services ne sont pas survivre suffisamment longtemps pour que l’attaque être détecté.

Bien sûr, il n’est généralement pas rentables pour la plupart des organisations d’acquérir la capacité supplémentaire nécessaire pour absorber les attaques par déni de service, comme cela nécessite un investissement considérable dans les technologies et techniques. Cela met en évidence l’avantage de la sécurité de l’utilisation des services de cloud Microsoft. l’échelle de réception de nos services permet de nous permettent de protection réseau fort à nos clients de cloud de manière rentable. Mais même à notre à l’échelle, cependant, il doit toujours exister un équilibre entre absorber, la détection et atténuation. Pour que l’équilibre, nous étudier les taux de croissance d’une attaque pour évaluer combien il nous faut absorber.

Détection est un véritable jeu. Vous devez rechercher en permanence pour les nouveaux modes sont vous attaquer ou essaient de contrer vos systèmes. Détecter - > atténuer - > détecter - > atténuer, etc., est un état définitive, persistent continuera indéfiniment.

## <a name="defending-against-dos-attacks"></a>Défense contre les attaques de déni de service

Pour protéger correctement une attaque par déni de service, au plus tôt détection est essentielle. En détectant les attaques avant que le système est surchargé, défenses peuvent exécuter un plan d’action.

La formule suivante vous aidera à élever à la durée de l’impact d’une attaque par déni de service :

   **Capacité maximale (en octets/s) / taux de croissance (en octets/s) = durée Impact (en octets/s)**

Si l’heure détection se produit après l’heure-impact, il est probable que l’attaque par déni de service sera réussi. Si l’heure détection se produit avant l’impact de l’heure, les services attaques doivent rester en ligne et accessible, si les stratégies d’atténuation sont utilisées. Par conséquent, il existe seulement deux choses qui peuvent être effectuées pour la défense contre les attaques de déni de service :
- Augmenter la capacité pour augmenter la limite de capacité maximale (qui à son tour fournit davantage de temps pour détecter une attaque) ; ou
- Réduire le temps de détecter.

Augmentation de la capacité a un impact direct fiscal. Microsoft recommande que les clients développent au moins base absorber la capacité, pour s’assurer qu’ils peuvent résister à un niveau de l’attaque par déni de service. La capacité d’absorber réel varie client, que chaque client a son propre seuils d’exposition, les risques et financier. Enfin, pour des raisons économiques, investissements en matière de recherche et l’heure de manière à réduire la détection de l’heure sont généralement la défense plus rentable.
