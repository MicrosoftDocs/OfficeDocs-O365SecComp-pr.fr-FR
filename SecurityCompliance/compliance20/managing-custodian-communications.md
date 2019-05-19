---
title: Utiliser les communications dans Advanced eDiscovery
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
description: Advanced eDiscovery facilite la gestion du flux de travail de notification de conservation légale concernant la notification des dépositaires en cours d’investigation.
ms.openlocfilehash: cf5c8f5e932993255bda2cb959657c2c6ded3163
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154906"
---
# <a name="work-with-communications-in-advanced-ediscovery"></a>Utiliser les communications dans Advanced eDiscovery

Advanced eDiscovery permet aux services juridiques de simplifier leurs processus de suivi et de distribution des notifications de conservation légale. L’outil de communication des dépositaires permet aux services juridiques de gérer et d’automatiser l’ensemble du processus de conservation légale, des notifications initiales, des rappels et des escalades, le tout en un seul et même endroit.

## <a name="what-is-a-legal-hold-notification"></a>Qu’est-ce qu’une notification de conservation légale?

Une notice légale (également appelée conservation pour *litige*) est une notification envoyée par le service juridique d’une organisation aux employés, au personnel concerné ou aux dépositaires de données qui peuvent être utiles à une enquête légale. Ces notifications indiquent aux dépositaires de conserver les informations stockées électroniquement ainsi que tout contenu susceptible d’être pertinent pour une question juridique active ou imminente. Les équipes juridiques doivent savoir que chaque dépositaire a reçu, lu, compris et qu’il a accepté de se conformer aux instructions données.

## <a name="the-legal-hold-notification-process"></a>Processus de notification de conservation légale

Une organisation a le droit de conserver les informations pertinentes lorsqu’elle apprend une enquête sur litige ou réglementaire imminente. Afin de se conformer aux exigences de conservation d’une enquête, l’organisation doit immédiatement informer les dépositaires potentiels de leur obligation de conserver les informations pertinentes.

Grâce à la fonctionnalité eDiscovery avancée, les équipes juridiques peuvent créer et personnaliser leur flux de travail de notification de conservation légale. L’outil de communication du dépositaire permet à teams de configurer les notifications et les flux de travail suivants:

1. **Notice d’émission**: une notice légale est émise (ou engagée) par une notification du service juridique aux dépositaires qui peuvent avoir des informations pertinentes sur la cause de l’affaire. Cette note indique aux dépositaires de conserver les informations susceptibles d’être nécessaires à la découverte.
   
2.  **Notification de nouvelle émission**: pendant un cas, les dépositaires peuvent être tenus de conserver du contenu supplémentaire (ou moins de contenu) que celui précédemment demandé. Dans ce scénario, vous pouvez mettre à jour l’avis de suspension existant et le ré-émettre aux dépositaires.

3.  **Avis de publication**: une fois qu’une question est résolue et que le dépositaire n’est plus soumis à une exigence de conservation, le dépositaire peut être libéré à partir du cas. En outre, vous pouvez informer le dépositaire qu’il n’est plus nécessaire de conserver le contenu et fournir des instructions sur la reprise de son activité professionnelle normale en ce qui concerne ses données.

4. **Rappels et escalades**: dans certains cas, il suffit d’émettre une notification pour répondre aux exigences de la découverte légale. À chaque notification, les équipes juridiques peuvent planifier un ensemble de flux de travail de rappel et de signalisation pour assurer un suivi automatique des dépositaires qui ne répondent pas.

    - **Rappels**: lorsqu’un avis de mise en attente légale a été émis ou réédité pour un ensemble de dépositaires, une organisation peut configurer des rappels pour prévenir les dépositaires qui ne répondent pas.

    - **Escalades**: dans certains cas, si un dépositaire ne répond pas même après un certain laps de temps, l’équipe juridique peut configurer un flux de travail de signalisation pour informer les dépositaires qui ne répondent pas et leur responsable.

## <a name="role-groups-and-permissions"></a>Groupes de rôles et autorisations 

Les équipes juridiques peuvent contrôler et isoler leur activité de cas à l’aide de groupes de rôles et d’autorisations liés à la découverte électronique dans le centre de sécurité & Compliance Center. 

Pour créer et gérer des notifications de conservation légale, un utilisateur doit faire partie des groupes de rôles suivants:

- **Gestionnaire eDiscovery** : les membres de ce groupe de rôles peuvent créer et gérer des cas eDiscovery. Ils peuvent ajouter et supprimer des membres, placer des dépositaires et des emplacements de contenu en conservation, gérer des notifications de conservation légale, créer et modifier des recherches de contenu associées à un cas, exporter les résultats d’une recherche de contenu et préparer des résultats de recherche pour analyse dans Advanced découverte. Il existe deux sous-groupes dans ce groupe de rôles. Ces sous-groupes ont différents rôles.

  - **Gestionnaire eDiscovery** : permet d’afficher et de gérer les cas eDiscovery qu’ils créent ou dont ils sont membres. Si un autre gestionnaire eDiscovery crée un cas mais n’ajoute pas de deuxième gestionnaire eDiscovery en tant que membre de ce dernier, le deuxième gestionnaire eDiscovery ne pourra pas afficher ou ouvrir le cas sur la page eDiscovery dans le centre de sécurité & Compliance Center. les gestionnaires eDiscovery peuvent également accéder à leurs incidents dans Advanced eDiscovery pour effectuer des tâches d’analyse.

  - **administrateur eDiscovery** : peut effectuer toutes les tâches de gestion des dossiers qu’un gestionnaire eDiscovery peut effectuer. De plus, un administrateur de découverte électronique peut :
    
    - Afficher tous les cas répertoriés sur la page Découverte électronique.
    - Gérez tous les cas dans l’organisation une fois qu’ils ont été ajoutés en tant que membre du cas.
    - Accéder aux données de cas dans Advanced eDiscovery pour tous les cas de l’organisation.

Pour plus d’informations, consultez [la rubrique attribution d’autorisations eDiscovery dans le centre de sécurité _AMP_ Compliance Center](../assign-ediscovery-permissions.md).