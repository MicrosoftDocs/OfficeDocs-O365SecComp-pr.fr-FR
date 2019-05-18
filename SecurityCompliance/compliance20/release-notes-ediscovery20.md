---
title: Notes de publication pour Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article contient les notes de publication pour Advanced eDiscovery.
ms.openlocfilehash: f3d26b1c84746581ccf32e1d4aada079fc21dfb3
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154886"
---
# <a name="release-notes-for-advanced-ediscovery"></a>Notes de publication pour Advanced eDiscovery

Le programme de préversion public pour Advanced eDiscovery est le moyen d’accéder en avant-première aux fonctionnalités et mises à jour à venir. Pour accéder en avant-première aux fonctionnalités les plus récentes, il vous suffit de créer et d’utiliser un cas avancé de découverte électronique dans le centre de sécurité & Compliance Center. Voir [Create a New case](create-new-ediscovery-case.md).

## <a name="known-issues"></a>Problèmes connus

**Microsoft Forms**

- Les données correspondant à un formulaire créé avant le 31 janvier 2019 ne pourront pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire. Les formulaires créés après cette date seront disponibles pour la recherche.

- Un formulaire créé par un utilisateur peut toujours recevoir des réponses même après la suppression de l’utilisateur qui a créé le formulaire. Toutefois, les données correspondantes de ces réponses (qui ont eu lieu après la suppression de la boîte aux lettres de dépositaire) ne peuvent pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire.
 
**Microsoft Sway**

- Si un utilisateur modifie un Sway juste avant la suppression du compte d’utilisateur pour le propriétaire de ce Sway, il se peut que ces modifications ne puissent pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire. Sway bloque les modifications apportées à un Sway dès qu’il reçoit un signal indiquant que le compte a été supprimé. Toutefois, il existe une petite chance qu’un Sway puisse être modifié avant la réception de ce signal.

## <a name="issues-fixed-in-this-release"></a>Problèmes résolus dans cette version

- DCR: gestion des exceptions pour les éléments non indexés et les éléments orphelins
- DCR: notifications de blocage
- DCR: dépositaires dans eDiscovery

## <a name="whats-new"></a>Nouveautés

- **Reconception de la navigation dans le centre de sécurité _AMP_ Compliance Center** : Advanced eDiscovery a une nouvelle apparence. Utilisez Advanced eDiscovery pour gérer davantage votre flux de travail de cas.

- **Gestion des cas** : il existe une prise en charge supplémentaire pour les nouveaux types de cas. Vous pouvez également sélectionner et enregistrer vos dossiers récents et favoris. Suivre et surveiller l’activité dans et dans les cas à l’aide de nouveaux tableaux de bord.

- **Gestion** des dépositaires: ajoutez et supprimez des utilisateurs comme dépositaires de données dans un cas.

- **Intégration d’Exchange, de onedrive et** de teams: ajoutez automatiquement la boîte aux lettres actuelle d’un utilisateur, le compte OneDrive entreprise et les sites Microsoft teams à un cas. 

- **Communications** des dépositaires: envoyez et gérez les notifications de conservation légale au nom de votre organisation.

- **Portail dépositaire** : nouveau portail pour les dépositaires pour accéder à leurs notifications d’attente actives.

- **Indexation profonde** : ré-analyse des éléments partiellement indexés à la demande.

- **Correction d’erreur** : correction ou téléchargement des erreurs de traitement; Il s’agit notamment de la prise en charge des types de fichiers volumineux, des fichiers protégés par mot de passe et bien plus encore. 

- **Améliorations de la recherche** : permet de créer une recherche en identifiant des dépositaires et/ou des emplacements.

- **Examiner les ensembles** : gérer, suivre et auditer des ensembles de documents statiques.

- **Révision** : utilisez une vue native, texte et quasi native pour consulter les documents ajoutés à votre jeu de révision.

- **Biffer, Baliser et** annoter: Biffer du texte, appliquer des balises et créer des annotations lors de la révision des documents.
  
- **** Analyse assistée: Tirez parti de l’analyse avancée de la découverte électronique pour rechercher, Rechercher et effectuer des recherches dans un jeu de révision.

- **Travaux** : suivre l’état des processus de longue durée.

- **Nouvelles activités d’audit** : suivez et affichez les nouvelles activités d’audit pour Advanced eDiscovery.
