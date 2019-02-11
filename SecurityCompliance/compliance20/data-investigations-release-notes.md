---
title: Notes de publication de données enquêtes (Preview) dans Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit la nouvelle version de découverte avancée (Preview) dans Microsoft 365.
ms.openlocfilehash: 90bcbd4cae1e410e1544352a776ba4cbbedfa429
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695060"
---
# <a name="release-notes-for-data-investigations-preview-in-microsoft-365"></a>Notes de publication de données enquêtes (Preview) dans Microsoft 365

Vous pouvez utiliser le nouvel outil données enquêtes (Preview) dans Microsoft 365 triage, examiner et corriger les données liées incidents, par exemple un incident débordements de données ou une enquête interne. Les enquêtes de visualisation de données Public offre Profitez d’un accès aux mises à jour et les fonctionnalités à venir. Pour accéder au plus tôt aux fonctionnalités plus récentes, créez une nouvelle enquête dans les enquêtes de données (Preview) dans le centre de conformité de & Office 365 sécurité. Pour en savoir plus, consultez la rubrique [gérer un incident débordements de données dans Microsoft 365](manage-data-spillage-incidents.md).

## <a name="whats-new"></a>Nouveautés 

- **Enquêtes** - vous pouvez regrouper les recherches et les incidents en créant une enquête. Gérer les personnes autorisées à accéder en ajoutant ou supprimant des membres de l’enquête.  Vous pouvez également sélectionner et marquer vos examens favoris. Le suivi et surveiller l’activité dans les enquêtes à l’aide de nouveaux tableaux de bord. Une fois que vous avez terminé vos recherches, vous pouvez fermer ou le supprimer.

- **Personnes dignes d’intérêt** – lorsque vous ajoutez des utilisateurs aux enquêtes en tant que personnes dignes d’intérêt, vous pouvez voir leur boîte aux lettres, OneDrive compte professionnel et les sites Microsoft Teams. Vous pouvez utiliser leur étendue de votre recherche de contenu investigation. Pour examiner une personne d’intérêt, vous pouvez également afficher auditer les enregistrements liés à leurs activités dans Office 365 et d’autres services Microsoft.

- **Recherche** – créer une recherche de l’entreprise en utilisant divers condition de recherche. Si vous connaissez les utilisateurs ou les sites que vous recherchez, vous pouvez le faire en ajoutant les utilisateurs en tant que personnes d’intérêt ou spécifier des emplacements de sites dans l’Assistant Création de recherche. 

- **Incidents** – créer un nouvel incident et ajoutez des résultats de recherche que vous souhaitez consulter. Vous pouvez réviser des documents individuels, annoter pour laisser les notes de l’enquête et exporter des résultats à déplacer vers un autre environnement. 

- **Passez en revue** – utilisez un natif, texte et pratiquement natifs vue pour passer en revue les documents ajoutés à un incident. Vous pouvez également appliquer analytique à des documents pour regrouper les éléments en doublons, les threads de messagerie et les thèmes, qui peuvent aider votre révision de l’incident. 

- **Redact, ajoutez une balise et annoter** – procéder texte, appliquer des balises et effectuer des annotations lors de la révision de documents.
  
- **L’indexation en profondeur** – s’il y a des éléments partiellement indexés, ils seront indexés de nouveau à la demande afin que toutes les données seront disponibles pour la recherche.

- **Correction d’erreur** – appliquer des mesures correctives ou téléchargement de traitement des erreurs. Cela inclut la prise en charge de la mise à jour pour les types de fichiers volumineux, le mot de passe protégé des fichiers et autres problèmes liés à l’indexation des erreurs. 

- **Travaux** – suivre l’état des processus de longue durée.

- **Dur-supprimer les éléments de boîte aux lettres** - dans les situations d’urgence, vous devrez peut-être supprimer définitivement les éléments mal placés. Pour ce faire, vous pouvez exécuter la **New-ComplianceSearchAction-purger - PurgeType HardDelete** commande sécurité & PowerShell du centre de conformité pour supprimer définitivement les éléments de boîtes aux lettres. Pour plus d’informations, voir [New-ComplianceSearchAction](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearchaction).
