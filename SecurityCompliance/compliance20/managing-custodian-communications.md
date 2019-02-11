---
title: Utilisation de communications d’eDiscovery avancée (Preview)
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
description: ''
ms.openlocfilehash: 962bd13f66ec8fe4f3385656f1241dd5fb5c4dcf
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695040"
---
# <a name="work-with-communications-in-advanced-ediscovery-preview"></a>Utilisation de communications d’eDiscovery avancée (Preview)

Découverte avancée (Preview) permet de services juridiques simplifier leurs processus autour de suivi et de distribution des notifications de conservation légale. La fonctionnalité de communications dépositaire permet des services juridiques gérer et automatiser leurs processus de conservation légale entier--de notifications et rappels escalades--au même endroit.

## <a name="what-is-a-legal-hold-notification"></a>Qu’est une notification de conservation légale ?

Une notification de conservation légale (également appelé un *litige maintenez*) est une notification envoyée à partir du département juridique d’une organisation aux employés, personnel temporaire ou autres conservateurs de données. Ces notifications enseigner dépositaires pour conserver stockées électroniquement informations ainsi que les documents qui peuvent être pertinentes à une affaire juridique active ou imminente. Équipes juridiques doivent savoir que chaque dépositaire a reçu, lu, compris et accepté de respecter les consignes donnés.

## <a name="the-legal-hold-notification-process"></a>Le département juridique maintenez le processus de notification

Une organisation a un droit pour conserver les informations pertinentes lorsqu’il a eu connaissance un imminente de litige ou. Afin de respecter les exigences de conservation, l’organisation doit immédiatement informer dépositaires potentiels leur obligation de conserver les informations appropriées. 

Avec eDiscovery avancée (Preview), les équipes juridiques peuvent créer et personnaliser leur flux de travail de notification de conservation légale. La fonctionnalité de Communications dépositaire permet aux équipes juridiques configurer les flux de travail et les mentions suivantes :

1. **Notez d’émission**: un avis de conservation légale est émis (ou initié) par une notification du département juridique à dépositaires qui pourrait disposer d’informations sur la nature de cas. Cette notification demande à ces dépositaires pour conserver les informations qui peuvent être nécessaires pour la découverte. 
   
2.  **Notez réattribution**: pendant un incident, dépositaires peuvent être nécessaires pour conserver plus ou moins d’informations qu’a été indiqués précédemment. Dans ce scénario, vous pouvez mettre à jour l’avis de suspension existant et republication à votre dépositaires.

3.  **Notez version**: une fois qu’une question est résolue et le dépositaire n’est plus soumis à un droit de conservation, le dépositaire peut être annulée afin que les informations sont n’est plus conservées si n’est pas nécessaire. En outre, votre dépositaire est communiquée qui ils ne sont plus sous le droit de conservation et des instructions en attente sur la reprise de leurs activités.

4. **Transformation et rappels**: dans certains cas, simplement émettre un avis n’est pas suffisante pour satisfaire aux exigences légales. Chaque notification, équipes juridiques peuvent de planifier un ensemble de rappel et escalade des flux de travail automatiquement suivi avec dépositaires ne répond pas.

    - **Rappels**: après un avis de conservation légale a été émis ou nouveau émis à un ensemble de dépositaires, une organisation peut configurer des rappels pour avertir dépositaires ne répond pas. 

    - **Transformation**: dans certains cas, si un dépositaire reste ne répond pas même après un ensemble de rappels, l’équipe juridique peut configurer un flux de travail d’escalade pour notifier le dépositaire et son responsable.

## <a name="role-groups-and-permissions"></a>Autorisations et les groupes de rôles 

Les équipes juridiques peuvent contrôler et leur activité d’incident à l’aide de groupes de rôles liés à la découverte électronique et les autorisations dans le centre de conformité de & sécurité de segment. 

Pour créer et gérer les notifications de conservation légale, un utilisateur doit faire partie des groupes de rôles suivants :

- **Gestionnaire de découverte électronique** - membres de ce groupe de rôles peut créer et gérer des affaires eDiscovery. Ils peuvent ajouter et supprimer des membres, placez dépositaires et emplacements de contenu sur maintenant, gérer les notifications de conservation légale, créer et modifier des recherches de contenu associé à un cas, exporter les résultats d’une recherche de contenu et préparer les résultats de la recherche pour l’analyse de la catégorie Avancé découverte électronique (Preview). Il existe deux sous-groupes dans ce groupe de rôles. La différence entre ces sous-groupes repose sur étendue.

  - **gestionnaire eDiscovery** - peuvent afficher et gérer les cas eDiscovery ou qu’ils créent un membre. Si un autre gestionnaire d’eDiscovery crée un cas mais n’ajoute pas un gestionnaire de deuxième eDiscovery en tant que membre de ce cas, la deuxième eDiscovery gestionnaire sera en mesure d’afficher ou d’ouvrir le cas dans la page de découverte électronique dans le centre de conformité de & sécurité. eDiscovery responsables permettre également accéder à leurs cas d’eDiscovery avancée (Preview) pour effectuer les tâches d’analyse.

  - **eDiscovery administrateur** - peuvent effectuer toutes les tâches de gestion des dossiers qu’un gestionnaire eDiscovery peut faire. En outre, une administrateur de découverte électronique peut :
    
    - Afficher tous les cas répertoriés sur la page Découverte électronique.
    - Gérer tous les cas dans l’organisation une fois qu’ils s’ajoutent en tant que membre de la casse.
    - Accédez aux données cas d’eDiscovery avancée (Preview) pour tous les cas dans l’organisation.

Pour plus d’informations, voir [attribuer des autorisations de découverte électronique dans le centre de conformité de & Office 365 sécurité](../assign-ediscovery-permissions.md).