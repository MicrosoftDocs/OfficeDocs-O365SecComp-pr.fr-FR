---
title: Stratégie de défense DoS de Microsoft Office 365
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
description: Vue d’ensemble de la stratégie de défense de Microsoft pour traiter les attaques par déni de service (DoS).
ms.openlocfilehash: f172db5080ef73402c7e9bc61720eb0f87e844ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527505"
---
# <a name="microsofts-denial-of-service-defense-strategy"></a>Stratégie de défense par déni de Service de Microsoft

La stratégie de protection contre les attaques réseau par déni de service (DoS) de Microsoft est relativement unique en raison de notre à l’échelle et l’empreinte globale. Cette échelle permet à Microsoft d’utiliser des stratégies et techniques que peu d’organisations (fournisseurs ou aux entreprises) peut correspondre. La pièce maîtresse de notre stratégie DoS exploite notre présence globale. Microsoft s’engage avec Internet, homologation fournisseurs (public et privé) et privées sociétés du monde entier, faites-nous part de présence Internet significative (qui, à ce jour, double autour de tous les 18 mois). Cette présence grandes permet de Microsoft d’absorber les attaques entre une très grande surface d’exposition.

Étant donné notre nature unique, Microsoft utilise des processus de détection et l’atténuation qui diffèrent de ceux utilisés par les grandes entreprises. Notre stratégie est basé sur une séparation de détection et atténuation, ainsi que d’atténuation internationale par le biais de nos nombreux bords. De nombreuses entreprises utilisent des solutions tierces qui détectent et atténuer les attaques sur le bord. Comme notre capacité edge est devenu, il est apparu que l’importance d’une attaque sur les bords individuels ou particuliers a été très faible. En raison de notre configuration unique, nous avons séparés par les composants de détection et l’atténuation. Nous avons déployé détection multiniveau qui permet de détecter les attaques de plus près à leur point de saturation tout en conservant atténuation globale sur le bord. Cette stratégie garantit que nous pouvons gérer plusieurs attaques simultanées.

Parmi les défenses plus efficaces et économique employés par Microsoft contre les attaques de déni de service consiste à réduire la surface d’attaque. Cela permet de supprimer le trafic indésirable sur le bord, au lieu d’analyse, de traitement et de nettoyage des données inline.

Dans l’interface avec le réseau public, Microsoft utilise les dispositifs de sécurité spéciaux pour le pare-feu, traduction d’adresses réseau et les fonctions de filtrage IP. Nous utilisons également le routage global égal Coût multi-path (ECMP). Le routage ECMP globale est une infrastructure de réseau garantissant qu’il existe plusieurs chemins d’accès globales pour atteindre un service. Grâce à ces plusieurs chemins d’accès, une attaque contre le service doit être limitée à la région d'où provient l’attaque – autres régions doivent être affectées par cette attaque, comme les utilisateurs finaux utiliseriez autres chemins d’accès pour atteindre le service dans les régions. Nous avons également développé notre propre DoS corrélation et la détection de système interne qui utilise des données du flux, les mesures de performances et d’autres informations. Il s’agit d’un service en nuage hyperscale s’exécutant dans Microsoft Azure qui analyse les données collectées à partir de différents points sur les réseaux Microsoft et des services. Une équipe de réponse aux incidents de charges de travail DoS identifie les rôles et responsabilités entre les équipes, les critères d’escalade et les protocoles pour engager des différentes équipes et pour la gestion des incidents. Ces solutions permettent la protection du réseau contre les attaques de déni de service.

Enfin, des charges de travail basées sur le nuage sont configurées avec les seuils optimisées en fonction de leur protocole et l’utilisation de la bande passante doit protéger de manière unique cette charge de travail.
