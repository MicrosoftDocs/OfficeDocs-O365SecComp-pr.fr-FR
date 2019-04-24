---
title: Stratégie DoS de Microsoft Office 365
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
description: Vue d'ensemble de la stratégie de défense de Microsoft concernant la gestion des attaques par déni de service (DoS).
ms.openlocfilehash: acc0c74ae9ed434d4718d7b8b3bd9429b3245d46
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262546"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Stratégie de défense contre les attaques par déni de service de Microsoft

La stratégie de Microsoft pour la défense contre les attaques par déni de service sur le réseau (DoS) est quelque peu unique en raison de notre échelle et de votre empreinte internationale. Cette mise à l'ampleur permet à Microsoft d'utiliser des stratégies et des techniques que peu d'organisations (fournisseurs ou organisations client) peuvent faire correspondre. La pierre angulaire de notre stratégie DoS consiste à tirer parti de notre présence internationale. Microsoft s'engage à utiliser des fournisseurs Internet, des fournisseurs de pairs (publics et privés) et des sociétés privées dans le monde entier, ce qui nous donne une présence importante sur Internet (ce qui est le cas pour tous les 18 mois). Le fait de disposer d'une présence de grande taille permet à Microsoft d'absorber les attaques sur une très grande surface.

Étant donné notre nature unique, Microsoft utilise des processus de détection et de minimisation qui diffèrent de ceux utilisés par les grandes entreprises. Notre stratégie est basée sur une séparation de la détection et de l'atténuation, ainsi qu'une atténuation globale distribuée par le biais de notre grand nombre d'entre elles. De nombreuses entreprises utilisent des solutions tierces qui détectent et atténuent les attaques sur le serveur Edge. À mesure que notre capacité de périmètre a augmenté, il est devenu évident que l'importance de toute attaque contre des contours individuels ou spécifiques était très faible. En raison de notre configuration unique, nous avons séparé les composants de détection et de minimisation. Nous avons déployé la détection à plusieurs niveaux qui nous permet de détecter les attaques plus près de leurs points de saturation tout en conservant une atténuation globale au niveau du périmètre. Cette stratégie garantit que nous pouvons gérer plusieurs attaques simultanées.

L'une des défenses les plus efficaces et les plus coûteuses employées par Microsoft contre les attaques DoS consiste à réduire notre surface d'attaque. Cela nous permettra de supprimer le trafic indésirable sur le serveur Edge, par opposition à l'analyse, le traitement et le nettoyage des données incorporées.

Au niveau de l'interface avec le réseau public, Microsoft utilise des périphériques de sécurité à usage spécial pour le pare-feu, la traduction d'adresses réseau et les fonctions de filtrage IP. Nous utilisons également le routage de chemins d'accès multiples (ECMP) à coût égal global. Le routage ECMP global est une infrastructure réseau qui garantit qu'il existe plusieurs chemins globaux pour atteindre un service. Grâce à ces chemins multiples, une attaque contre le service doit être limitée à la région d'où provient l'attaque: d'autres régions ne doivent pas être affectées par cette attaque, car les utilisateurs finaux utiliseront d'autres chemins pour atteindre le service dans ces régions. Nous avons également développé notre propre système de corrélation et de détection de DoS interne qui utilise des données de flux, des mesures de performances et d'autres informations. Il s'agit d'un service Cloud de l'échelle hyperdimension exécuté dans Microsoft Azure qui analyse les données collectées à partir de différents points sur les réseaux et les services Microsoft. Une équipe de réponse aux incidents DoS entre plusieurs charges de travail identifie les rôles et les responsabilités entre les équipes, les critères de remontée des problèmes, ainsi que les protocoles permettant d'engager diverses équipes et de gérer les incidents. Ces solutions fournissent une protection réseau contre les attaques DoS.

Enfin, les charges de travail basées sur le Cloud sont configurées avec des seuils optimisés en fonction de leur protocole et de l'utilisation de la bande passante pour protéger de manière unique cette charge de travail.
