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
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004071"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Défense contre les attaques par déni de service dans Office 365

## <a name="introduction"></a>Introduction
Microsoft propose une infrastructure de confiance pour plus de 200 services Cloud, notamment Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype et Xbox Live hébergés dans notre Cloud global infrastructure de plus de 100 centres de informations.

En tant qu'organisation mondiale avec une présence Internet importante et de nombreuses propriétés Internet importantes qui fournissent des services en nuage, Microsoft est une cible commune et commune aux pirates et autres personnes malveillantes. Le réseau, la couche communication entre les clients et le Cloud Microsoft, est l'une des principales cibles d'attaques malveillantes. En fait, depuis de nombreuses années, Microsoft a cessé de se conformer de façon continue et permanente sous certaines conditions de cyber basées sur le réseau. Presque toutes les fois, au moins une des propriétés Internet de Microsoft rencontre une attaque. Sans systèmes d'atténuation fiables et persistants capables de se défendre contre ces attaques, les services Cloud de Microsoft seraient hors ligne et indisponibles pour les clients.

Microsoft utilise des principes de sécurité de défense en profondeur pour protéger ses services et réseaux Cloud. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Définition et symptômes des attaques par déni de service
Pour attaquer les services réseau, il est possible de créer plusieurs requêtes sur les hôtes d'un service afin de submerger le réseau et les serveurs afin de refuser les services aux utilisateurs légitimes. Il s'agit d'une attaque par déni de service (DoS). Lorsque l'attaque est effectuée par plusieurs acteurs, points de terminaison et/ou vecteurs, elle est considérée comme une attaque de déni de service distribuée. Bien que les moyens, les motivations et les cibles varient, les attaques DoS et DDoS consistent généralement en les efforts de la personne ou des personnes pour empêcher un site ou un service Internet de fonctionner correctement ou de façon temporaire ou indéfinie.

L'équipe américaine de préparation de l' [urgence informatique](https://www.us-cert.gov/) (US-CERT) définit les symptômes des attaques par déni:
- Ralentissement des performances réseau (lors de l'ouverture de fichiers ou accès aux sites Internet)
- Indisponibilité d'un site Web
- ImPossibilité d'accéder à un site Web
- Augmentation spectaculaire du courrier indésirable reçu
- Déconnexion d'une connexion Internet câblée ou sans fil
- Perte d'accès à long terme pour le Web ou tout service Internet

## <a name="related-topics"></a>Rubriques connexes
- [Principes fondamentaux de défense contre les attaques par déni de service](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Stratégie de défense contre les attaques par déni de service de Microsoft](office-365-microsoft-dos-defense-strategy.md)
- [Protection des services de Cloud Computing Microsoft contre les attaques par déni de service](office-365-defending-cloud-services-against-dos-attacks.md)
