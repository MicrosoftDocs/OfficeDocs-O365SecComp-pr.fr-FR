---
title: Destruction des données Office 365
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
description: Vue d’ensemble des stratégies de Microsoft concernant le recyclage, élimination ou la destruction des disques Office 365 centre de données et des serveurs.
ms.openlocfilehash: c9950be4919520f2f46badaa4a7d4cfce5c55b45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527844"
---
# <a name="office-365-data-destruction"></a>Destruction des données Office 365
Microsoft a des stratégies Standard de gestion des données qui résout recycle et élimination des disques durs et des serveurs de retraite ou ayant échoués. Avant de réutiliser les disques dans Office 365, Microsoft effectue un processus de nettoyage physique est cohérent avec National Institute of Standards et technologie la Publication spéciale 800-88 ([SP NIST 800-88 instructions pour le nettoyage des médias](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) ). Tous les lecteurs de disques dans Office 365 sont chiffrées à l’aide de chiffrement au niveau de volume BitLocker, en pratique, effacement compatibles 800-88 NIST SP n’est pas nécessaire. Néanmoins, il est toujours effectué par Microsoft.

Échec de disques utilisés dans Office 365 centres de données sont physiquement détruits et audités via le processus ISO. Les moyens d’élimination appropriée sont déterminée par le type d’élément. Pour les disques durs qui ne peut pas être effacées, Microsoft utilise un processus de destruction détruit le support (par exemple, disintegrates, pulverizes ou incinerates) et la récupération des informations impossible. Microsoft conserve également tous les enregistrements de la destruction. Microsoft effectue un processus de nettoyage similaire sur les serveurs soient réutilisés dans Office 365. Ces instructions englobent nettoyage électronique et physique.

Les disques ne peut pas être réutilisés à l’aide d’un processus de destruction physique est effectué sur le site dans le centre de données contenant les destruction des disques sont supprimés. Support de stockage indiqué pour suppression est placé dans des emplacements sécurisés situés dans chaque zone du centre de données. Chaque station de magasin sécurisé est contrôlée par la surveillance vidéo. Une fois qu’un emplacement de disposition atteint environ 50 % de la capacité, l’équipe de Services de sites contacte l’équipe de sécurité physique pour coordonner sa suppression. Personnel des Services de site, de supprimer l’emplacement de disposition sous escorte par un responsable de la sécurité de jusqu'à ce qu’il est placé dans une zone de stockage sécurisée à attendre la destruction des données. Stratégies et des procédures régissant la gestion des données portant des périphériques au cours de suppression sont testées régulièrement, y compris des procédures pour vous assurer de la condition de machines approuvés pour la destruction.

Dans le processus de destruction de données, le disque est effacé tout d’abord d’une manière qui est compatible avec NIST 800-88 (si possible), puis il est placé dans un shredder industriel et démoli physiquement. Microsoft conserve la responsabilité pour les biens en laissant le centre de données utilisant NIST SP 800-88 cohérente nettoyage/le vidage, destruction de biens, chiffrement, précis inventaire, suivi et protection authenticité d’au cours du transport. Ce processus est surveillé par circuit fermé télévision et un certificat de Destruction est émise à la fin.

Microsoft utilise les unités d’effacement des données à partir de [Solutions de protocole extrême](http://www.enterprisedataerasure.com/) (EPS). EPS logiciel prend en charge SP NIST 800-88 requise pour le nettoyage et le vidage/secure effacement. Avant de nettoyage ou de destruction, un inventaire est créé par le Gestionnaire de ressources de Microsoft. Si un fournisseur est utilisé pour la destruction, le fournisseur fournit un certificat de destruction pour chaque ressource détruit, qui est validé par le Gestionnaire de ressources.