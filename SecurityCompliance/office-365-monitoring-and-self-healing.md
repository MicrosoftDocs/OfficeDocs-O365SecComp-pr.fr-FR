---
title: Analyse d’Office 365 et d’autoréparation
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
description: Informations sur Office 365 surveillance et spontanée fonctionnalités.
ms.openlocfilehash: ff9471eaa6117ca3d7761549bca9ab629020fe79
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527702"
---
# <a name="office-365-monitoring-and-self-healing"></a>Analyse d’Office 365 et d’autoréparation
Étant donné l’échelle d’Office 365, il est impossible de conserver les données client résistantes et contre les programmes malveillants sans surveillance intégrées est complète, alertes qui est intelligent et spontanée qui soient rapide et fiable. Surveillance d’un ensemble de services à l’échelle d’Office 365 est très difficile. Nouvelles mentalités et méthodologies nécessaires pour être introduite et ensembles de toute nouvelles technologie ont été créés pour faire fonctionner et gérer le service dans un environnement global connecté. Nous avons éloignée de l’approche de collecte de données de surveillance et le filtrage traditionnel à créer des alertes pour une approche basée sur l’analyse des données ; prendre des signaux et création de confiance dans ces données, puis en utilisant automation de récupérer ou de résoudre le problème. Cette approche permet de prendre des personnes en dehors de l’équation de récupération, qui à son tour rend opérations erreur les moins coûteux, plus rapide et moins sujet. 

Fondamentaux liés à Office 365 surveillance est un ensemble de technologies qui comprend des données Insights, notre moteur s’appuie sur Azure, SQL Azure et [open source diffusion en continu de la technologie de base de données](http://cassandra.apache.org/). Il est conçu pour collecter et regrouper les données et atteindre les conclusions. Actuellement, il traite les événements de plus de 500 millions par heure à partir des serveurs plus de 100 000 (~ 15 To par jour) éparpillés dans des dizaines de centres de données dans plusieurs régions, et ces numéros deviennent. 

Office 365 utilise *en dehors de surveillance*, qui consiste à créer les transactions synthétiques pour tester tout ce qui est important. Par exemple, dans Exchange Online chaque scénario teste chaque base de données dans le monde de manière dispersée, fournissant couverture continue de tous les éléments qui réside dans le système pratiquement toutes les cinq minutes. À partir de plusieurs emplacements, les transactions de test 250 millions par jour sont effectuées pour créer une base robuste ou la pulsation du service. 

Office 365 utilise également le concept *L’alerte rouge*, qui réduit vers le bas tous les signaux des surveillance de tous les ordinateurs de nos centres de données quelque chose gérable par un être humain. Le concept est assez simple : si quelque chose qui se passe sur plusieurs signaux, il doit y avoir quelque chose sur. Il n’est pas sur la génération de confiance dans un signal, il s’agit de devoir fidélité raisonnable pour chaque signal afin que vous obtenez une plus grande précision. Ce système de surveillance est si puissant que nous n’avons pas 24 x 7 personnel regarder nos moniteurs ; Il nous est la machine s’active si elle détecte un problème, auquel cas il de la page le personnel sur appel ou plus souvent comme c’est le cas, il sera simplement continuez et résoudre le problème. Une fois nous commencer la collecte des signaux et génération d’alertes rouge les, nous pouvons commencer effectuant dans toutes les partitions de notre service. 

En fonction de la combinaison de l’alerte d’échec et les alertes rouge, cette alerte indique exactement quels composants pourrait avoir un problème, et que le système est sur le point pour essayer de résoudre le problème en lui-même par redémarrage d’un serveur de boîtes aux lettres. 

En plus de rétablissement automatique des fonctions, telles que la restauration d’une page unique, Exchange Online inclut plusieurs fonctionnalités qui utilisent une approche de surveillance et spontanée qui se concentre sur la conservation de l’utilisateur final. Ces fonctionnalités incluent la *Disponibilité gérée*, qui fournit des actions intégrées de surveillance et de récupération et AutoReseed, ce qui rétablit automatiquement la redondance de base de données après une défaillance de disque. 

## <a name="managed-availability"></a>Disponibilité gérée 
Disponibilité gérée fournit une solution de vérification et de récupération de native d’intégrité qui surveille et protège les actions de récupération orientés grâce à l’utilisateur final. Disponibilité gérée est l’intégration des actions de surveillance et de récupération intégrées à la plate-forme de haute disponibilité d’Exchange. Il est conçu pour détecter et résoudre des problèmes dès qu’ils se produisent et sont découvertes par le système. Contrairement aux solutions précédentes de surveillance externes et techniques pour Exchange, gestion de la disponibilité n’essaie pas identifier ou communiquer la cause d’un problème. Au lieu de cela, il se concentre sur les aspects de récupération qui traitent les trois zones clés de l’expérience utilisateur final : 
- **Disponibilité** - utilisateurs peuvent-ils accéder au service ? 
- **Latence** - quelle est l’expérience des utilisateurs ? 
- **Erreurs** - sont les utilisateurs peuvent-ils faire ce qu’ils veulent ? 

Disponibilité gérée est une fonctionnalité interne qui s’exécute sur chaque serveur d’Office 365 exécutant Exchange Online. Il interroge et analyse des centaines de mesures d’intégrité par seconde. Si un élément est trouvé à un problème, la plupart du temps, il est fixe automatiquement. Mais il sera toujours problèmes de disponibilité gérée ne sera pas en mesure de résoudre son propre. Dans ce cas, la disponibilité gérée transmettra le problème à une équipe de support technique Office 365 au moyen de la journalisation des événements. 

## <a name="autoreseed"></a>AutoReseed 
Serveurs Exchange Online sont déployés dans une configuration qui stocke plusieurs bases de données et leur flux de journal sur le même disque non RAID. Cette configuration est souvent appelée *juste un tas de disques* (JBOD) car aucune mécanismes de redondance de stockage, telles que RAID, ne sont utilisés pour dupliquer les données sur le disque. Lors de la défaillance d’un disque dans un environnement JBOD, les données qu’il contient sont perdues. 

En fonction de la taille d’Exchange Online et le fait que déployé qu’il contient sont millions de lecteurs de disque, les défaillances de disque une occurrence régulière dans Exchange Online. En fait, plus de 100 échouent tous les jours. Lors de la défaillance d’un disque dans un déploiement d’entreprise locale, un administrateur doit manuellement remplacer le disque défaillant et restaurer les données affectées. Dans un déploiement en nuage la taille d’Office 365, opérateurs (administrateurs du nuage) remplacement manuellement des disques est ni pratique ni rentables. 

Réamorçage automatique ou *AutoReseed*, est une fonctionnalité qui est le remplacement de ce qui est normalement contrôlée par l’opérateur d’action en réponse à une défaillance de disque ou autre problème qui nécessite un réamorçage d’une copie de base de données d’événement d’endommagement de base de données. AutoReseed est conçu pour restaurer automatiquement la redondance de base de données après une défaillance de disque à l’aide de disques de secours qui ont été mis en service sur le système. En cas d’échec d’un disque, les copies de base de données stockées sur ce disque sont automatiquement redéfinies sur un disque de rechange préconfiguré sur le serveur, restaurant ainsi la redondance. 