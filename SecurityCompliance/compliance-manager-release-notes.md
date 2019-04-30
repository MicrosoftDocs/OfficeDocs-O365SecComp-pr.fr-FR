---
title: Notes de publication du gestionnaire de conformité Microsoft
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Le gestionnaire de conformité Microsoft est un outil d'évaluation des risques gratuit basé sur un flux de travail dans le portail d'approbation de service Microsoft. Le gestionnaire de conformité vous permet de suivre, d'affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473064"
---
# <a name="release-notes-for-compliance-manager-preview"></a>Notes de publication pour le gestionnaire de conformité (aperçu)

La préversion publique du gestionnaire de conformité vous permet d'accéder en avant-première aux fonctionnalités et mises à jour à venir.

Vous pouvez utiliser l'outil [Gestionnaire de conformité](https://servicetrust.microsoft.com/ComplianceManager) mis à jour sur le [portail d'approbation de service](https://servicetrust.microsoft.com) pour suivre, attribuer et vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.

## <a name="whats-new-in-compliance-manager-preview"></a>Nouveautés du gestionnaire de conformité (aperçu)

- **Intégration avec le score de sécurité Microsoft:** Le gestionnaire de conformité prend en charge l'intégration avec le [score de sécurité Microsoft](microsoft-secure-score.md) en mappant les actions gérées par le client à plus de 50 actions de score sécurisé. Lorsque vous terminez une action mappée dans le score de sécurité, l'action du gestionnaire de conformité correspondante est automatiquement mise à jour.

- **Importer des évaluations personnalisées:** Outre les évaluations intégrées, le gestionnaire de conformité prend désormais en charge l'importation des modèles personnalisés, ce qui vous permet de créer des évaluations personnalisées pour n'importe quel produit ou service, ainsi que pour n'importe quelle norme ou réglementation.

- **Éléments d'action:** Les éléments d'action sont maintenant des éléments individuels et de nombreux incluent une collection de télémétrie provenant de l'API graphique Microsoft Secure score. Dans la mesure du possible, les recommandations d'action technique ont maintenant des liens vers la page de configuration applicable dans le service Office 365.

- **Gestion des clients:** Nouvelle interface de gestion des nouveaux éléments de données dans le gestionnaire de conformité (aperçu):
    - **Dimensions:** Afficher, ajouter et personnaliser des métadonnées pour des modèles, des évaluations et des éléments d'action qui vous permettent de créer des tableaux croisés dynamiques personnalisés pour les filtres.
    - **Propriétaires:** Spécifiez un propriétaire pour chaque élément d'action.
    - **Actions des clients:** Gérez la liste complète des éléments actions inclus dans le gestionnaire de conformité (aperçu) et activez/désactivez la surveillance du score sécurisé pour les éléments d'action intégrés avec le score sécurisé.

- **Score de conformité mis à jour**: la méthodologie a changé pour prendre en charge la synchronisation avec le score de sécurité Microsoft. Le système de score supprime les crédits de contrôle gérés par Microsoft et se concentre uniquement sur l'exécution des contrôles gérés par le client.

## <a name="known-issues-in-compliance-manager-preview"></a>Problèmes connus dans le gestionnaire de conformité (aperçu)

Les sections suivantes couvrent les problèmes connus à résoudre dans les prochaines versions du gestionnaire de conformité.

### <a name="compliance-score"></a>Score de conformité

- Lorsque les éléments d'action sont marqués comme **n'étant pas dans l'étendue**, le score attribué à l'action n'est pas exclu du calcul du score de conformité. Les éléments d'action marqués comme **n'étant pas inclus dans l'étendue** ne doivent pas augmenter votre score de conformité.

### <a name="microsoft-managed-controls"></a>Contrôles gérés par Microsoft

- La date de test pour les contrôles gérés par Microsoft n'apparaît pas dans l'interface utilisateur, même si elle est incluse dans l'évaluation. Pour afficher les informations de date de test, vous devez exporter l'évaluation.

### <a name="customization"></a>Personnalisation

- L'ajout de contrôles personnalisés permet d'ajouter un nouveau contrôle à une famille de contrôle existante, mais il ne vous permet pas d'ajouter une nouvelle famille de contrôles.
- Cette version ne prend pas en charge la liaison d'éléments d'action ou l'ajout d'éléments actions ou de contrôles à une évaluation.
- Si vous créez une action personnalisée, vous ne pouvez pas la modifier ou la supprimer.

### <a name="control-families-not-shown-in-assessments"></a>Familles de contrôle non affichées dans les évaluations

- Lorsque vous importez un modèle, toutes les évaluations basées sur ce modèle reflètent toutes les familles de contrôle qui font partie du modèle. Toutefois, si vous ajoutez de nouvelles familles de contrôle au modèle, les évaluations existantes ne refléteront pas les modifications. Seules les nouvelles évaluations créées à partir du modèle mis à jour reflètent les modifications.

### <a name="filters"></a>Filtres

- Le filtrage des éléments d'action ou des contrôles ne produit pas toujours des résultats corrects.

### <a name="templates"></a>Modèles

- Les modèles archivés sont modifiables et ne doivent pas être modifiables.
- Les modèles verrouillés permettent la création d'une évaluation alors qu'ils ne le devraient pas. Le verrouillage d'un modèle est destiné à empêcher son utilisation pour créer des évaluations.

### <a name="export"></a>Exporter

- L'exportation de modèle vers JSON échoue lorsque l'état du modèle est défini sur **importé** ou **en attente d'approbation**.

### <a name="supported-browsers"></a>Navigateurs pris en charge

- Les versions les plus récentes de Microsoft Edge, chrome et Safari sont prises en charge.
- Dans certaines circonstances, les données mises à jour ne s'affichent pas tant que votre navigateur n'est pas actualisé.
- La version d'évaluation de Microsoft Edge n'est pas prise en charge, mais n'a pas de problèmes connus.
- Internet Explorer n'est pas pris en charge.

### <a name="session-timeout"></a>Délai d'expiration de session

- Lorsqu'une session arrive à expiration, une erreur «un problème est survenu» peut apparaître. Pour résoudre ce dernier, accédez au [Gestionnaire de conformité](https://servicetrust.microsoft.com/ComplianceManager) et reconnectez-vous.