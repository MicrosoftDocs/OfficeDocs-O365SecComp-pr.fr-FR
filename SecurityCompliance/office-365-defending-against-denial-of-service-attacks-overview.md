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
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Défense contre les attaques par déni de Service dans Office 365

## <a name="introduction"></a>Présentation
Microsoft fournit une infrastructure fiable pour plus de 200 services en nuage, y compris Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype et Xbox Live qui sont hébergées dans notre nuage global infrastructure de centres de données plus de 100.

En tant qu’une organisation globale avec une présence Internet significative et de nombreuses propriétés visibles Internet qui fournissent des services en nuage, Microsoft est une cible volumineux, courantes des pirates informatiques et d’autres personnes malveillantes. --Le réseau de la couche de communication entre les clients et le Cloud Microsoft--est un des objectifs principaux d’attaques malveillantes. En fait, de nombreuses années, Microsoft a été en continu et de façon permanente sous une forme d’opérations sur le réseau. Presque à tout moment, au moins une des propriétés de Internet de Microsoft rencontre une forme d’attaque. Sans systèmes atténuation fiable et permanente qui protège contre les attaques, les services en nuage de Microsoft serait en mode hors connexion et indisponible pour les clients.

Microsoft utilise les principes de sécurité de défense en profondeur pour protéger ses services en nuage et les réseaux. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Définition et symptômes d’attaques par déni de Service
Une manière d’attaques de services réseau consiste à créer de nombreuses demandes par rapport à des hôtes d’un service de provoquer une saturation du réseau et les serveurs refus de service pour les utilisateurs légitimes. Il est appelé une attaque de par déni de service (DoS). Lors de l’attaque par plusieurs acteurs, des points de terminaison et/ou des vecteurs, il est appelé une attaque de (par déni) distribuée par déni de service. Bien que les moyens, motifs et cibles varient, les attaques par déni de service et par déni se composent généralement des efforts d’une personne ou les personnes pour empêcher un site Internet ou le service de fonctionner correctement ou tout titre temporaire ou indéfiniment.

Les [États-Unis Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) définit les symptômes d’attaques DoS à inclure :
- Anormalement ralentir les performances du réseau (lors de l’ouverture de fichiers ou d’accéder aux sites Internet)
- Indisponibilité d’un site Web
- Impossibilité d’accéder à un site Web
- Augmentation considérable de courrier indésirable entrant
- Déconnexion d’une connexion Internet sans fil ou câblée
- Perte à long terme de l’accès sur le Web ou les services Internet

## <a name="related-topics"></a>Voir aussi
- [Principes fondamentaux de la défense contre les attaques par déni de Service](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Stratégie de défense par déni de Service de Microsoft](office-365-microsoft-dos-defense-strategy.md)
- [Protection contre les attaques par déni de Service des Services de Cloud Microsoft](office-365-defending-cloud-services-against-dos-attacks.md)
