---
title: Utiliser les communications dans Advanced eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 916691e1f2470ef9e9e54d9dfe06c5277a92ba53
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241251"
---
# <a name="work-with-communications-in-advanced-ediscovery-preview"></a>Utiliser les communications dans Advanced eDiscovery (aperçu)

Advanced eDiscovery (aperçu) permet aux services juridiques de simplifier leurs processus de suivi et de distribution des notifications de conservation légale. La fonctionnalité de communication des dépositaires permet aux services juridiques de gérer et d'automatiser l'ensemble de leurs processus de conservation légale: à partir de notifications, rappels et escalades--tout en un seul.

## <a name="what-is-a-legal-hold-notification"></a>Qu'est-ce qu'une notification de conservation légale?

Une notice légale (également appelée conservation pour *litige*) est une notification envoyée par le service juridique d'une organisation aux employés, au personnel concerné ou à d'autres dépositaires de données. Ces notifications indiquent aux dépositaires de conserver les informations stockées électroniquement (ESI), ainsi que tout matériel pouvant être pertinent à une question juridique active ou imminente. Les équipes juridiques doivent savoir que chaque dépositaire a reçu, lu et compris, et accepté de se conformer aux instructions données.

## <a name="the-legal-hold-notification-process"></a>Processus de notification de conservation légale

Une organisation a le droit de conserver les informations pertinentes lorsqu'elle apprend une enquête sur litige ou réglementaire imminente. Afin de se conformer à ses exigences de conservation, l'organisation doit immédiatement informer les dépositaires potentiels de leur obligation de conserver les informations pertinentes. 

Avec Advanced eDiscovery (aperçu), les équipes juridiques peuvent créer et personnaliser leur flux de travail de notification de conservation légale. La fonctionnalité de communications des dépositaires permet aux équipes juridiques de configurer les notifications et les flux de travail suivants:

1. **Notice d'émission**: une notice légale est émise (ou engagée) par une notification du service juridique aux dépositaires qui peuvent avoir des informations pertinentes sur la cause de l'affaire. Cette note demande à ces dépositaires de conserver toutes les informations susceptibles d'être nécessaires à la découverte. 
   
2.  **Notification de nouvelle émission**: pendant un cas, les dépositaires peuvent être tenus de conserver des informations supplémentaires ou moins détaillées que celles précédemment demandées. Dans ce scénario, vous pouvez mettre à jour l'avis de suspension existant et le réémettre à vos dépositaires.

3.  **Avis de publication**: une fois qu'une question est résolue et que le dépositaire n'est plus soumis à un droit à la conservation, le dépositaire peut être libéré afin que les informations ne soient plus conservées si elles ne sont plus nécessaires. En outre, votre dépositaire est informé qu'il ne fait plus l'objet d'une conservation et qu'il dispose d'instructions en suspens pour reprendre son activité.

4. **Rappels et escalades**: dans certains cas, la seule façon d'émettre une notification est insuffisante pour répondre aux exigences de la découverte légale. À chaque notification, les équipes juridiques peuvent planifier un ensemble de flux de travail de rappel et de signalisation pour assurer un suivi automatique des dépositaires qui ne répondent pas.

    - **Rappels**: lorsqu'un avis de mise en attente légale a été émis ou réédité pour un ensemble de dépositaires, une organisation peut configurer des rappels pour prévenir les dépositaires qui ne répondent pas. 

    - **Escalades**: dans certains cas, si un dépositaire ne répond pas, même après un ensemble de rappels, l'équipe juridique peut configurer un flux de travail de signalisation pour avertir le dépositaire et son responsable.

## <a name="role-groups-and-permissions"></a>Groupes de rôles et autorisations 

Les équipes juridiques peuvent contrôler et segmenter leur activité de cas à l'aide de groupes de rôles et d'autorisations liés à la découverte électronique dans le centre de sécurité & Compliance Center. 

Pour créer et gérer des notifications de conservation légale, un utilisateur doit faire partie des groupes de rôles suivants:

- **Gestionnaire eDiscovery** : les membres de ce groupe de rôles peuvent créer et gérer des cas eDiscovery. Ils peuvent ajouter et supprimer des membres, placer des dépositaires et des emplacements de contenu en conservation, gérer des notifications de conservation légale, créer et modifier des recherches de contenu associées à un cas, exporter les résultats d'une recherche de contenu et préparer des résultats de recherche pour analyse dans Advanced eDiscovery (aperçu). Il existe deux sous-groupes dans ce groupe de rôles. Ces sous-groupes ont différents rôles.

  - **Gestionnaire eDiscovery** : permet d'afficher et de gérer les cas eDiscovery qu'ils créent ou dont ils sont membres. Si un autre gestionnaire eDiscovery crée un cas mais n'ajoute pas de deuxième gestionnaire eDiscovery en tant que membre de ce dernier, le deuxième gestionnaire eDiscovery ne pourra pas afficher ou ouvrir le cas sur la page eDiscovery dans le centre de sécurité & Compliance Center. les gestionnaires eDiscovery peuvent également accéder à leurs incidents dans Advanced eDiscovery (aperçu) pour effectuer des tâches d'analyse.

  - **administrateur eDiscovery** : peut effectuer toutes les tâches de gestion des dossiers qu'un gestionnaire eDiscovery peut effectuer. De plus, un administrateur de découverte électronique peut :
    
    - Afficher tous les cas répertoriés sur la page Découverte électronique.
    - Gérez tous les cas dans l'organisation une fois qu'ils ont été ajoutés en tant que membre du cas.
    - Accéder aux données de cas dans Advanced eDiscovery (aperçu) pour tous les cas de l'organisation.

Pour plus d'informations, consultez [la rubrique Assign eDiscovery Permissions in the Office 365 Security _AMP_ Compliance Center](../assign-ediscovery-permissions.md).