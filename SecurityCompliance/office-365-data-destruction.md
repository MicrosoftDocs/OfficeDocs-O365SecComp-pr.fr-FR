---
title: Destruction des données Office 365
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
description: Vue d'ensemble des stratégies de Microsoft relatives au recyclage, à la suppression ou à la destruction des serveurs et des lecteurs de disque du centre de l'Office 365.
ms.openlocfilehash: fec6065434fa9fa555a057c68eca60082225652c
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004141"
---
# <a name="office-365-data-destruction"></a>Destruction des données Office 365

## <a name="physical-data-destruction"></a>Destruction de données physiques

Microsoft propose des stratégies standard de gestion des données qui traite du recyclage et de la suppression des disques durs et des serveurs ayant échoué ou remis à niveau. Avant de réutiliser des lecteurs de disque dans Office 365, Microsoft effectue un processus de nettoyage physique cohérent avec National Institute of Standards and Technology Special Publication 800-88 ([NIST SP 800-88 Guidelines for Media assainiing](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) ). Tous les lecteurs de disque dans Office 365 sont chiffrés à l'aide du chiffrement au niveau du volume BitLocker, dans la pratique, l'effacement conforme à la norme NIST SP 800-88 n'est pas nécessaire. Néanmoins, il est toujours exécuté par Microsoft.

Les disques défaillants utilisés dans les centres de 365 Office sont physiquement détruits et audités via le processus ISO. Les moyens de suppression appropriés sont déterminés par le type d'élément. Pour les disques durs qui ne peuvent pas être effacés, Microsoft utilise un processus de destruction qui détruit les médias (par exemple, discombines, pulvérisés ou incinérés) et rend impossible la récupération des informations. Microsoft conserve également tous les enregistrements de la destruction. Microsoft effectue un processus de nettoyage similaire sur les serveurs qui sont réutilisés dans Office 365. Ces instructions englobent la désinfection électronique et physique.

Les lecteurs de disque qui ne peuvent pas être réutilisés sont éliminés à l'aide d'un processus de destruction physique effectué sur site dans le centre de contenu contenant les disques en cours de destruction. Les supports de stockage désignés pour l'élimination sont placés dans des emplacements sécurisés situés dans chaque zone du centre de donnée. Chaque station de casier sécurisée est surveillée par la surveillance vidéo. Une fois qu'un casier de suppression atteint environ 50% de capacité, l'équipe des services de site contacte l'équipe de sécurité physique pour coordonner sa suppression. Le personnel des services de site supprime ensuite le casier de suppression sous escorte par un responsable de la sécurité jusqu'à ce qu'il soit placé dans une zone de stockage sécurisé pour attendre la destruction des données. Les stratégies et les procédures régissant le traitement des dispositifs de support des données pendant la destruction sont régulièrement testées, y compris les procédures pour garantir l'état des machines approuvées pour la destruction.

Dans le processus de destruction des données, le disque est d'abord effacé d'une manière conforme à l'Institut NIST 800-88 (si possible), puis il est placé dans un broyeur industriel et Demolished physiquement. Microsoft gère les responsabilités pour les biens quittant le centre de recherche à l'aide de l'Institut NIST SP 800-88 cohérent de nettoyage/Purge des ressources, de destruction des biens, de chiffrement, d'inventaire, de suivi et de protection de la chaîne de conservation pendant le transport. Ce processus est contrôlé via une télévision de circuit fermé et un certificat de destruction est émis au terme de l'opération.

Microsoft utilise les unités d'effacement des données des protocoles EPS ( [Extreme Protocol solutions](http://www.enterprisedataerasure.com/) ). Le logiciel EPS prend en charge la configuration requise pour le SP 800-88 pour le nettoyage et la purge et l'effacement sécurisé. Avant de procéder au nettoyage ou à la destruction, un inventaire est créé par le gestionnaire de ressources Microsoft. Si un fournisseur est utilisé pour la destruction, le fournisseur fournit un certificat de destruction pour chaque ressource détruite, qui est validée par le gestionnaire des biens.

## <a name="virtual-data-destruction"></a>Destruction de données virtuelles

Microsoft possède des stratégies et des procédures de gestion des données qui gèrent également la destruction virtuelle efficace des données afin de se protéger contre la possibilité de partage des données de manière inappropriée entre les locataires de services ou d'être accessibles après suppression définitive du service. Les données qui sont supprimées du service dans un seul client ne sont pas accessibles à un autre client de service même si une partie ou la totalité du même stockage physique sous-jacent est réattribuée ultérieurement. Il s'agit d'un résultat des effets composés de plusieurs technologies de virtualisation et de fragmentation utilisées pour mettre à l'évolution des environnements virtuels, les comportements de suppression actifs des applications au sein de chaque client de service (par exemple, la mise à [zéro de page](https://docs.microsoft.com/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)) et le processus de chiffrement de contenu multimédia et de contenu d'application.