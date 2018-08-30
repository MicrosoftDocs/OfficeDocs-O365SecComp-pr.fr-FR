---
title: Office 365 données fixes
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
description: Définit et explique les données fixes ou des données qui doivent pouvoir être détectées et ne peut pas être détruit ou a été modifié.
ms.openlocfilehash: 3a9e897734c1805e25a2e2dd5e0c5f8a3e3de3fd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528376"
---
# <a name="immutability-in-office-365"></a>Immuabilité dans Office 365
Pour certaines organisations, conformité aux exigences réglementaires, de gouvernance interne ou pour litige risque requièrent la conservation du courrier électronique et des données associées dans un formulaire détectable. Toutes les données dans le système doivent pouvoir être détectées, et aucune peuvent être détruits ou a été modifié. Le terme normalisés pour ce est « immuabilité. » 

Les méthodes traditionnelles d’immuabilité ont travaillé généralement en déplaçant les messages électroniques vers un emplacement de stockage distinct, en lecture seule. Alors que ces systèmes servent de conservation des éléments de boîte aux lettres pour la découverte, ils affectent souvent l’expérience utilisateur de manières significatives en supprimant conservés les éléments à partir de ce flux de travail habituel. Pour les professionnels de l’informatique, cette approche immuabilité nécessite le déploiement et la maintenance continue d’une infrastructure de serveur et de stockage distincte. Détection proprement dite est effectuée avec des outils externes pour le système de messagerie, avec déploiement associé et les coûts de maintenance.

Grâce à la configuration de la rétention des archives et les fonctionnalités de stratégie de conservation de l’archivage dans Office 365 et en association avec les services dans la suite Office 365, tels que Exchange Online, SharePoint Online, OneDrive entreprise et Skype pour les entreprises, l’archivage dans Office 365 peut conserver et conserver de nombreuses classes de données internes entrantes et sortantes, y compris :
- Communications de messagerie entrante et sortante
- Livres et documents figurant dans le formulaire de messagerie ou des documents en ligne
- Demandes de réunion
- Télécopie
- Messages instantanés
- Documents partagés au cours des réunions en ligne
- Messages vocaux

En outre, Microsoft a développé des fonctionnalités module complémentaire pour permettre [l’archivage des données](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) provenant d’autres sources par le biais de l’intégration avec des tiers de capture de données et des solutions de gestion. Après l’importation des données tierces, vous pouvez appliquer des fonctionnalités de conformité d’Office 365 pour les données, y compris litige, In-Place eDiscovery et la suspension, recherche de conformité, d’archivage sur Place, audit et stratégies de rétention. Par exemple, lorsqu’une boîte aux lettres est mis en attente pour litige, des données tierces seront préservées. Vous pouvez rechercher des données tierces à l’aide de la découverte électronique locale ou la recherche de conformité. Ou vous pouvez appliquer l’archivage et les stratégies de rétention pour des données tierces comme vous pouvez utiliser pour les données de Microsoft. En bref, l’archivage des données tierces dans Office 365 peut aider votre organisation respecter les administrations et réglementaires.

L’archivage dans Office 365 fournit un stockage compatibles 17 a-4 règle Securities and Exchange Commission (s) et conserve les fichiers définitive de toutes les données collectées dans un format non réinscriptible et non effaçable à l’aide de stratégies de rétention sur place et les stratégies de conservation , y compris le verrouillage de conservation. Plus particulièrement :
- Tous les enregistrements sont stockés à l’aide de stratégies de rétention ci-dessus sont conservées dans une zone de stockage dédié en dehors des limites de l’utilisateur ordinaire. En outre, seuls les utilisateurs autorisés peuvent accéder et rechercher ces enregistrements, mais Impossible de modifier ou les effacer.
- Métadonnées pour chaque élément incluent un cachet de date qui est utilisée dans le calcul de la durée de rétention. Horodatages sont appliquées lors de la réception d’un nouvel élément créé et ne peuvent pas être par la suite modifié ou supprimé à partir des métadonnées.
- L’archivage dans Office 365 permet aux utilisateurs de combiner des stratégies de rétention différentes et suspendre des actions pour créer des stratégies de rétention précise pour définir le type ou l’emplacement des éléments à être conservés immuable et la durée de conservation de ce type.
- La fonctionnalité de verrouillage de conservation permet aux utilisateurs de choisir s’il souhaite rendre la stratégie d’une stratégie restrictive. Une stratégie restrictive interdit la possibilité de supprimer, désactiver ou modifier la stratégie de rétention. Cela signifie qu’une fois la conservation de verrouillage est activé, il ne peut pas être désactivée, et aucun mécanisme ne se trouvent sous les toutes les données à partir de dépositaires existantes qui ont été collectées par la conservation place des politiques risquent d’être remplacées, modifié, effacement ou supprimé au cours de la période de conservation. En outre, la période définie par le verrouillage de conservation de suspension ne peut pas raccourcie ou réduite. Toutefois, peut être prolongés, dans le cas d’une obligation légale pour continuer la rétention des données stockées, comme indiqué ci-dessus. Verrouillage de conservation garantit que personne, pas même les administrateurs ou ayant certaines contrôler l’accès, peut modifier les paramètres ou remplacer ou effacer les données qui ont été stockées, transfert de l’archivage dans Office 365 inséré dans les instructions énoncées dans la version 2003 de s Règle 17 a-4.

Pour les clients de mieux comprendre comment Office 365 peuvent être exploitées pour répondre aux obligations réglementaires, notamment par rapport à la configuration requise de règle 17 a-4, nous avons publié un [livre blanc](https://go.microsoft.com/fwlink/?linkid=830440) qui traite de l’archivage Exchange Online, SharePoint Online, les OneDrive pour les entreprises et Skype pour les entreprises. Le livre blanc fournit une analyse approfondie des fonctionnalités d’archivage d’Office 365 et de fonctionnalités par rapport à chacun des exigences sous SEC 17 a-4 également et montre aux clients régulés comment Office 365 d’archivage peut leur permettre de répondre à ces configuration requise.