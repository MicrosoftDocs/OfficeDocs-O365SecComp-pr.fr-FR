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
description: Définit et décrit l’immuabilité des données dans Office 365.
ms.openlocfilehash: bc9805be446ad1d696e20a4bee6e449b311970fe
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622444"
---
# <a name="immutability-in-office-365"></a>Immuabilité dans Office 365

La conformité réglementaire, les exigences de gouvernance interne ou les risques de contentieux imposent aux organisations de conserver le courrier électronique et les données associées sous une forme découvrable. Toutes les données du système doivent être découvrables et aucune ne peut être détruite ou modifiée. Le terme standard du secteur est «immuabilité».

Les méthodes traditionnelles d’immuabilité ont généralement fonctionné en déplacant les messages électroniques vers un emplacement de stockage distinct en lecture seule. Bien que ces systèmes visent l’objectif de la conservation des éléments de boîte aux lettres pour la découverte, ils affectent souvent l’expérience utilisateur en supprimant les éléments conservés du flux de travail quotidien personnalisé. Pour les professionnels de l’informatique, cette approche d’immuabilité nécessite le déploiement et la maintenance continue d’une infrastructure de serveur et de stockage distincte. La découverte est effectuée avec des outils externes au système de messagerie et inclut des coûts de déploiement et de maintenance associés.

Grâce aux fonctionnalités de stratégie de rétention et de conservation sur place de l’archivage dans Office 365 et de ses services, vous pouvez conserver et conserver de nombreuses classes de données entrantes, internes et sortantes. Cela inclut:

- Communications par courrier électronique entrant et sortant
- Livres et enregistrements contenus dans un formulaire électronique ou dans des documents en ligne partagés
- Demandes de réunion
- Situées
- Messages instantanés
- Documents partagés pendant les réunions en ligne
- Messages vocaux

De plus, Microsoft a développé des fonctionnalités complémentaires pour permettre [l’archivage des données](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) provenant d’autres sources via l’intégration de solutions de capture et de gestion de données tierces. Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité d’Office 365 aux données, notamment:

- [Conservation pour litige](create-a-litigation-hold.md)
- [Découverte électronique inaltérable et conservation inaltérable](manage-legal-investigations.md)
- [Recherche de conformité](search-for-content.md)
- [Archivage local](enable-archive-mailboxes.md)
- [Audit de boîte aux lettres](enable-mailbox-auditing.md)
- [Stratégies de rétention](retention-policies.md)

Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées. Vous pouvez rechercher des données tierces à l’aide de la découverte électronique inaltérable ou de la recherche de conformité. Vous pouvez également appliquer des stratégies d’archivage et de rétention à des données tierces, comme vous pouvez le faire pour Microsoft Data. L’archivage de données tierces dans Office 365 aide votre organisation à respecter les stratégies gouvernementales et réglementaires.

L’archivage dans Office 365 fournit des valeurs mobilières et des commissions Exchange (SEC) pour la règle de stockage compatible 17A -4. Office 365 conserve les fichiers permanents de toutes les données collectées dans un format non réinscriptible et non effaçable en utilisant des stratégies de rétention sur place et des stratégies de conservation, notamment le verrouillage de la conservation.

Notamment :

- Tous les enregistrements stockés à l’aide des stratégies de rétention indiquées ci-dessus sont conservés dans une zone de stockage dédiée à partir de l’PurVIEW de l’utilisateur ordinaire. Seuls les utilisateurs autorisés peuvent accéder à ces enregistrements et les Rechercher, mais ils ne peuvent pas les modifier ou les supprimer.
- Les métadonnées de chaque élément incluent un horodatage utilisé dans le calcul de la durée de rétention. Les horodatages sont appliqués lorsqu’un nouvel élément est reçu ou créé et qu’il ne peut pas être modifié ou supprimé des métadonnées.
- L’archivage dans Office 365 permet aux utilisateurs de combiner différentes stratégies de rétention et des actions de conservation pour créer des stratégies de rétention granulaires. Ces stratégies définissent le type ou l’emplacement des éléments conservés et la durée de conservation.
- La fonctionnalité de verrouillage de conservation permet aux utilisateurs de choisir s’il faut appliquer une stratégie restrictive à la stratégie. Une stratégie restrictive interdit à quiconque de pouvoir supprimer, désactiver ou modifier la stratégie de rétention. Cela signifie que lorsque le verrouillage de conservation est activé, il ne peut pas être désactivé et aucun mécanisme n’existe sous lequel les données provenant de dépositaires existants collectées par les stratégies de rétention en place peuvent être remplacées, modifiées, effacées ou supprimées au cours du période de conservation. De plus, le délai d’attente défini par le verrouillage de conservation ne peut pas être raccourci ou réduit. Elle peut toutefois être allongée, dans le cas d’une obligation légale de continuer la rétention des données stockées, comme indiqué ci-dessus. Le verrouillage de conservation garantit que personne, pas même les administrateurs ou ceux disposant d’un accès de contrôle, ne modifient pas les paramètres ou ne remplacent ou n’effacent pas les données qui ont été stockées, en configurant l’archivage dans Office 365 conformément aux instructions indiquées dans la version 2003 de la version de SEC. Règle 17A -4.

Pour comprendre comment Office 365 vous aide à respecter les obligations réglementaires, notamment en ce qui concerne la réglementation 17A -4, consultez ce [livre blanc](https://go.microsoft.com/fwlink/?linkid=830440) qui traite de l’archivage Exchange Online, de SharePoint Online, de OneDrive entreprise et de Skype entreprise. Le livre blanc fournit également une analyse approfondie des fonctionnalités et des fonctionnalités d’archivage d’Office 365 en fonction de chacune des exigences de la norme SEC 17A -4 et démontre aux clients soumis à la façon dont l’archivage Office 365 peut les activer pour répondre à ces besoins. requise.