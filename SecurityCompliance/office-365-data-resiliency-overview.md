---
title: Résistance des données dans Office 365
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
description: Comprendre la résistance des données dans Microsoft Office 365.
ms.openlocfilehash: 7d43c766615ff1520c6529427116c42795da8565
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528378"
---
# <a name="data-resiliency-in-office-365"></a>Résistance des données dans Office 365

## <a name="introduction"></a>Présentation
Étant donné la nature complexe du cloud computing, Microsoft est ayant à l’esprit qu’il n’est pas un cas de si surviendront, mais lors de. Nous concevoir des services en nuage afin d’optimiser la fiabilité et de limiter l’impact négatif sur les clients lorsque des problèmes incorrectes. Nous avons déplacé au-delà de la stratégie de compter sur une infrastructure physique complexe traditionnelle et nous avons redondance directement dans les services en nuage. Nous utilisons une combinaison d’une infrastructure physique moins complexe et plus intelligent logiciel qui intègre la résistance des données de nos services et offre une haute disponibilité à nos clients. 

## <a name="resiliency-and-recoverability-are-built-in"></a>Résilience et récupération sont intégrés 
Création de résilience et de récupération démarre en partant du principe que l’infrastructure sous-jacente et les processus échouera à un moment donné : matériel (infrastructure) échoue, l’homme font des erreurs et logiciel aura bugs. Il serait incorrect de dire que les développeurs de logiciels n’étaient pas penser que ces éléments avant le nuage, comment ces problèmes ont été traités dans une implémentation informatique typique étaient très différent avant le nuage : 
- Tout d’abord, matériel et l’infrastructure des protections étaient importantes. Cela signifie ayant des centres de données avec la fiabilité 99,99 % nécessaire une puissance et de redondance du réseau et les serveurs ont été implémentées avec le matériel de clustering, deux blocs d’alimentation, les deux interfaces réseau, etc.. 
- Deuxièmement, le processus a prépondérante. Les équipes opérationnelles conservée procédures rigoureux, modification windows ont été utilisées, et il a souvent été surcharge de gestion de projet importantes. 
- Troisièmement, déploiement a eu lieu à un rythme glacial. Déploiement sans propriétaire de la source du code destiné à attendre des correctifs et version majeure versions remplacement du matériel nécessaires et des dépenses en capital important. En outre, la seule façon de résoudre un problème a été restaurée. Par conséquent, la plupart des organisations informatiques seraient déployer des versions majeures uniquement pour éviter le travail pour maintenir à jour. 
- Enfin, l’échelle des systèmes déployés, ainsi que le niveau de leur interdépendance a été historiquement beaucoup plus petite qu’elle est maintenant. 

Aujourd'hui, les clients s’attendent innovations de Microsoft sans compromettre la qualité, et il s’agit d’une des raisons pourquoi les logiciels et des services de Microsoft sont créés avec résilience et de récupération à l’esprit. 

## <a name="office-365-data-resiliency-principles"></a>Principes de résilience de données Office 365 
Résistance fait référence à la capacité d’un service en nuage pour résister à certains types de défaillances et restent encore entièrement fonctionnelle du point de vue des clients. Résistance des données signifie que quel que soit le rôle échecs se produisent dans Office 365, les données client critiques demeurent intactes et non affecté. À cette fin, Office 365 services ont été conçus cinq principes résistance spécifique : 
- Il est des données critiques et non critiques. Données non critique (par exemple, si un message a été lu) peuvent être supprimées dans les scénarios d’échecs rares. Les données critiques (par exemple, les données client telles que les messages électroniques) doivent être protégées au coût extrême. Comme un objectif de conception, les messages remis sont toujours critique, et notamment si un message a été lu est non critique. 
- Copie des données du client doit être séparés en zones différentes pannes ou autant de panne domaines que possible (par exemple, centres de données accessibles par les informations d’identification uniques (processus, serveur ou opérateur)) pour assurer l’isolation de l’échec. 
- Les données client critiques doivent être surveillées de l’échec de n’importe quelle partie d’atomicité, cohérence, Isolation, durabilité (acide). 
- Données client doivent être protégées contre une corruption. Il doit être activement analysés ou surveillés, réparable et récupérables. 
- La plupart des résultats de la perte de données à partir des actions de client, permettent aux clients de récupérer leurs propres une interface utilisateur graphique qui permet de restaurer des éléments supprimés par inadvertance à l’aide. 
 
Par le biais de la création de services en nuage ces principes associée robuste de test et de validation, Office 365 peut atteindre et dépasser les besoins des clients tout en garantissant une plate-forme pour l’innovation continue et d’amélioration du produit. 

## <a name="related-links"></a>Liens connexes

- [Traitement de Corruption des données](office-365-dealing-with-data-corruption.md)
- [Protection des logiciels et des programmes malveillants](office-365-malware-and-ransomware-protection.md)
- [Surveillance et spontanée](office-365-monitoring-and-self-healing.md)
- [Résistance des données Exchange](office-365-exchange-data-resiliency.md)
- [Résistance des données SharePoint](office-365-sharepoint-data-resiliency.md)