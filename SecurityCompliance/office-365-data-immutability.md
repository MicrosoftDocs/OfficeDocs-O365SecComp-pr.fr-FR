---
title: Office 365 données immuabilité
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
description: Définit et décrit l'immuabilité des données, ou les données qui doivent être détectables et qui ne peuvent pas être détruites ou modifiées.
ms.openlocfilehash: b23a62dd95ec2ca554997fc667d89e6979e5b747
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262866"
---
# <a name="immutability-in-office-365"></a>Immuabilité dans Office 365
Pour certaines organisations, le respect de la réglementation, les exigences de gouvernance interne ou le risque de contentieux nécessitent la conservation de la messagerie et des données associées sous une forme découvrable. Toutes les données du système doivent être découvrables et aucune ne peut être détruite ou modifiée. Le terme standard du secteur est «immuabilité». 

Les méthodes traditionnelles d'obtention d'immuabilité ont généralement fonctionné en déplacant les messages électroniques vers un emplacement de stockage distinct en lecture seule. Bien que ces systèmes visent l'objectif de la conservation des éléments de boîte aux lettres pour la découverte, ils affectent souvent l'expérience utilisateur de manière significative en supprimant les éléments conservés du flux de travail quotidien personnalisé. Pour les professionnels de l'informatique, cette approche de l'immuabilité nécessite le déploiement et la maintenance continue d'une infrastructure de serveur et de stockage distincte. La découverte proprement dite est effectuée avec des outils externes au système de messagerie, avec des coûts de déploiement et de maintenance associés.

Grâce à la configuration des fonctionnalités de stratégie de rétention et de conservation sur place de l'archivage dans Office 365, et en association avec les services de la suite Office 365, comme Exchange Online, SharePoint Online, OneDrive entreprise et Skype entreprise, l'archivage dans Office 365 peut conserver et conserver de nombreuses classes de données entrantes, internes et sortantes, notamment:
- Communications par courrier électronique entrant et sortant
- Livres et enregistrements contenus dans un formulaire électronique ou dans des documents en ligne partagés
- Demandes de réunion
- Situées
- Messages instantanés
- Documents partagés pendant les réunions en ligne
- Messages vocaux

De plus, Microsoft a développé des fonctionnalités complémentaires pour permettre [l'archivage des données](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) provenant d'autres sources via l'intégration de solutions de capture et de gestion de données tierces. Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité d'Office 365 aux données, notamment la mise en attente pour litige, la découverte électronique et la conservation inaltérable, la recherche de conformité, l'archivage inaltérable, l'audit et les stratégies de réTention. Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées. Vous pouvez rechercher des données tierces à l’aide de la découverte électronique inaltérable ou de la recherche de conformité. Vous pouvez également appliquer des stratégies d’archivage et de rétention aux données tierces, de la même manière que pour les données Microsoft. En bref, l'archivage des données tierces dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

L'archivage dans Office 365 fournit des valeurs mobilières et des commissions Exchange (SEC) pour la règle de stockage conforme à la norme 17A -4, et conserve les fichiers permanents de toutes les données collectées dans un format non réinscriptible et non effaçable à l'aide de stratégies de rétention sur place et de stratégies de conservation. , y compris le verrouillage de conservation. Notamment :
- Tous les enregistrements stockés à l'aide des stratégies de rétention indiquées ci-dessus sont conservés dans une zone de stockage dédiée à partir de l'PurVIEW de l'utilisateur ordinaire. De plus, seuls les utilisateurs autorisés peuvent accéder à ces enregistrements et les Rechercher, mais ils ne peuvent pas les modifier ou les supprimer.
- Les métadonnées de chaque élément incluent un horodatage utilisé dans le calcul de la durée de rétention. Les horodatages sont appliqués lorsqu'un nouvel élément est reçu ou créé et qu'il ne peut pas être modifié ou supprimé par la suite des métadonnées.
- L'archivage dans Office 365 permet aux utilisateurs de combiner différentes stratégies de rétention et actions de conservation pour créer des stratégies de rétention granulaires afin de définir le type ou l'emplacement des éléments à immuablement conserver, ainsi que la durée de cette conservation.
- La fonctionnalité de verrouillage de conservation permet aux utilisateurs de choisir s'ils souhaitent appliquer une stratégie restrictive à la stratégie. Une stratégie de restriction interdit à quiconque de pouvoir supprimer, désactiver ou modifier la stratégie de rétention. Cela signifie que lorsque le verrouillage de conservation est activé, il ne peut pas être désactivé et aucun mécanisme n'existe sous lequel les données des dépositaires existants collectées par les stratégies de rétention en place peuvent être remplacées, modifiées, effacées ou supprimées au cours du période de conservation. De plus, le délai d'attente défini par le verrouillage de conservation ne peut pas être raccourci ou réduit. Elle peut toutefois être allongée, dans le cas d'une obligation légale de continuer la rétention des données stockées, comme indiqué ci-dessus. Le verrouillage de conservation garantit que personne, pas même les administrateurs ou ceux disposant d'un accès de contrôle, ne modifient pas les paramètres ou ne remplacent ou n'effacent pas les données qui ont été stockées, en configurant l'archivage dans Office 365 conformément aux instructions indiquées dans la version 2003 de la version de SEC. Règle 17A -4.

Pour permettre aux clients de mieux comprendre comment Office 365 peut être utilisé pour répondre à leurs obligations réglementaires, en particulier en ce qui concerne la réglementation 17A -4, nous avons publié un [livre blanc](https://go.microsoft.com/fwlink/?linkid=830440) sur l'archivage Exchange Online, SharePoint Online, OneDrive pour les entreprises et Skype entreprise. Le livre blanc fournit également une analyse approfondie des fonctionnalités et des fonctionnalités d'archivage d'Office 365 en fonction de chacune des exigences de la norme SEC 17A -4 et démontre aux clients soumis à la façon dont l'archivage Office 365 peut les activer pour répondre à ces besoins. requise.