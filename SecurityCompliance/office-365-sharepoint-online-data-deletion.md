---
title: Suppression de données en ligne Office 365 SharePoint
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
description: Explication de la suppression des données dans SharePoint Online.
ms.openlocfilehash: 97f3eaea471c08ba61c0fc749b806c1960c0182f
ms.sourcegitcommit: ee1d7037d9ad14d7f0dbc53114177a3d04614d6e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25402038"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a>Suppression de données en ligne SharePoint dans Office 365

SharePoint Online stocke les objets en tant que code abstrait au sein des bases de données application. Lorsqu’un utilisateur télécharge un fichier dans SharePoint Online, ce fichier est dissocié et converti en code d’application et stocké dans plusieurs tableaux sur plusieurs bases de données. Dans SharePoint Online, tout le contenu qui télécharge un client est divisé en segments, chiffrés (potentiellement avec plusieurs clés AES 256 bits) et réparti sur le centre de données. Pour plus d’informations spécifiques à propos du processus de segmentation et le chiffrement, voir [chiffrement dans le nuage de Microsoft](office-365-encryption-in-the-microsoft-cloud-overview.md). Services de protection des données sont fournies pour empêcher la perte de données SharePoint Online. Plus précisément, les sauvegardes sont effectuées toutes les 12 heures et conservés pendant 14 jours.

Lorsque vous supprimez le contenu d’un site SharePoint Online, il n'est pas immédiatement supprimé. Il est envoyé à un Site Corbeille, où elle peut être restaurée, si nécessaire. (Voir [restaurer les éléments supprimés de la Corbeille de collection de sites](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) pour les étapes de restauration). La durée de rétention de Corbeille de Site par défaut est d’environ 90 jours. Si vous supprimez le contenu à partir d’un Site de la Corbeille, il est envoyé vers le Site Collection Corbeille, ayant une durée de rétention de jours 93. La durée de conservation des éléments dans la Corbeille peut être configurée par un administrateur, mais en l’absence de qui, la période de rétention par défaut est environ 90 jours. Le le stockage du site recycle bin compte dans le quota de stockage de collection de sites et le [Seuil d’affichage de liste](https://support.office.com/article/List-View-Threshold-b8588dae-9387-48c2-9248-c24122f07c59).

Lorsque vous supprimez une collection de sites, vous êtes également supprimer la hiérarchie de sites dans la collection, y compris toutes les informations utilisateur et de contenu :
- les documents et bibliothèques de documents ;
- Listes et données de liste
- Paramètres de configuration de site
- Informations de rôle et de sécurité liées au site ou ses sous-sites
- Sous-sites du site Web, leur contenu et l’utilisateur informations niveau supérieur

Avant de supprimer une collection de sites, nous vous recommandons de que consulter la Description du Service SharePoint Online pour votre projet, qui décrit la planification de sauvegarde de données gérée par Microsoft pour les sites SharePoint Online. Notez que les restaurations à partir de sauvegardes peuvent sont également uniquement pour les collections de sites ou des sous-sites, pas pour les fichiers, des listes ou bibliothèques. Si vous devez récupérer ceux, utilisez la Corbeille. Si vous supprimez par inadvertance une collection de sites, il peut être restauré à partir de la Corbeille de la Collection de sites par un administrateur de Collection de sites dans les jours 93.

Disque dur suppression se produit lorsqu’un utilisateur purge des éléments supprimés de la Corbeille de Site et la rétention et les périodes de sauvegarde d’expiration, ou lorsqu’un administrateur supprime définitivement une collection de sites à l’aide de l’applet de [commande Remove-SPODeletedSite](https://docs.microsoft.com/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). Lorsqu’un utilisateur dur supprime (supprime définitivement ou purge) contenu dans SharePoint Online, la toutes les clés de chiffrement pour les segments supprimés sont également supprimés. Les blocs sur les disques qui précédemment stockées les segments supprimés sont marqués comme étant inutilisée et disponible pour les réutiliser.
