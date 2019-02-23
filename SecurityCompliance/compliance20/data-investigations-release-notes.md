---
title: Notes de publication pour les enquêtes sur les données (aperçu) dans Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit la nouvelle version de Advanced eDiscovery (Preview) dans Microsoft 365.
ms.openlocfilehash: 851712d6eae876f4c74c4d3322de487d3ff14858
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212804"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Notes de publication pour les enquêtes sur les données (aperçu) dans Microsoft 365

Vous pouvez utiliser l'outil nouvelles enquêtes de données (aperçu) dans Microsoft 365 pour trier, examiner et résoudre les problèmes liés aux données, tels qu'un incident de débordement de données ou une enquête interne. La préversion publique des analyses de données vous permet d'accéder en avant-première aux fonctionnalités et mises à jour à venir. Pour accéder en avant-première aux fonctionnalités les plus récentes, créez une nouvelle enquête sur les enquêtes de données (aperçu) dans le centre de sécurité & de la sécurité d'Office 365. Pour savoir comment procéder, voir [gérer un incident de fuite de données dans Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Nouveautés 

- **Enquêtes** : vous pouvez regrouper les recherches et les incidents en créant une enquête. Gérer les personnes pouvant accéder à l'enquête en ajoutant ou en supprimant des membres.  Vous pouvez également sélectionner et marquer vos recherches favorites. Suivre et surveiller l'activité au sein et à travers des enquêtes à l'aide de nouveaux tableaux de bord. Une fois votre enquête terminée, vous pouvez la fermer ou la supprimer.

- **Personnes intéressantes** : lorsque vous ajoutez des utilisateurs à des enquêtes en tant que personnes intéressantes, vous pouvez voir leur boîte aux lettres, le compte OneDrive entreprise et les sites Microsoft Teams. Vous pouvez les utiliser pour étendre vos recherches de contenu d'enquête. Pour approfondir votre attention sur une personne intéressante, vous pouvez également afficher les enregistrements d'audit relatifs à leurs activités dans Office 365 et d'autres services Microsoft.

- **Recherches** : créez une recherche à l'échelle de l'organisation à l'aide de diverses conditions de recherche. Si vous savez des utilisateurs ou des sites à rechercher, vous pouvez le faire en ajoutant ces utilisateurs en tant que personnes intéressantes ou en spécifiant des emplacements de site dans l'Assistant de création de la recherche. 

- **Incidents** : créez un nouvel incident et ajoutez les résultats de la recherche que vous souhaitez examiner. Vous pouvez passer en revue des documents individuels, les annoter pour laisser des notes d'enquête et exporter les résultats pour les déplacer vers un autre environnement. 

- **Révision** : utilisez une vue native, texte et presque native pour examiner les documents ajoutés à un incident. Vous pouvez également appliquer des analyses aux documents pour regrouper les éléments par doublons, les threads de messagerie et les thèmes, ce qui peut aider à examiner l'incident. 

- **Biffer, Baliser et** annoter: Biffer du texte, appliquer des balises et créer des annotations lors de la révision des documents.
  
- **Indexation profonde** : s'il existe des éléments partiellement indexés, ils seront réindexés à la demande afin que toutes les données soient disponibles pour la recherche.

- **Correction d'erreur** : correction ou téléchargement des erreurs de traitement. Cela inclut la prise en charge de la correction pour les types de fichiers volumineux, les fichiers protégés par mot de passe et d'autres problèmes liés aux erreurs d'indexation. 

- **Travaux** : suivre l'état des processus de longue durée.

- **Supprimer des éléments de boîte aux lettres** de manière irréversible: dans les situations urgentes, vous devrez peut-être supprimer définitivement les éléments mal placés. Pour ce faire, vous pouvez exécuter la commande **New-ComplianceSearchAction-purge-PurgeType permet HardDelete** dans Security _AMP_ Compliance Center PowerShell pour supprimer définitivement des éléments des boîtes aux lettres. Pour plus d'informations, consultez la rubrique [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).
