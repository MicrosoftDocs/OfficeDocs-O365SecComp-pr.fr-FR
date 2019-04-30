---
title: Méthodologie du score de conformité
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
ms.openlocfilehash: 120aede52d67375f60145412f5d210509ac57581
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473065"
---
# <a name="compliance-score-methodology-preview"></a>Méthodologie du score de conformité (aperçu)

> [!NOTE]
> Le Score de conformité ne reflète pas forcément la conformité absolue de l’organisation avec une norme ou une réglementation spécifique. Il indique les contrôles que vous avez adoptés pour réduire les risques liés à la protection des données personnelles. Aucun service ne peut garantir que vous êtes en conformité avec une norme ou une réglementation. Le Score de conformité ne doit donc en aucun cas être considéré comme une garantie du respect des réglementations en vigueur.

Le tableau de bord du gestionnaire de conformité affiche un score de conformité total pour les évaluations dans chaque vignette d'évaluation. Il s'agit du score de conformité global pour l'évaluation et de l'accumulation de points reçus pour chaque contrôle implémenté et testé dans l'évaluation. Pour une nouvelle évaluation, le score de conformité a une valeur initiale pour les contrôles gérés par Microsoft inclus testés par des tiers indépendants. Le score de conformité peut vous aider à hiérarchiser les évaluations et les contrôles à mettre en évidence pour améliorer votre position de conformité globale.

Les valeurs de score de conformité affichées pour le contrôle sont appliquées *dans leur intégralité* à la note de conformité totale en cas de réussite/échec. Le contrôle est implémenté et réussit le test d'évaluation suivant ou non. Il n'existe pas de crédit partiel pour une implémentation partielle. Les points affectés sont ajoutés au score de conformité lorsque le contrôle a:

- Le statut de l' **implémentation** est égal à **implémenté** ou **autre implémentation** et,
- Le **résultat des tests** est égal à **passé**.

## <a name="compliance-score"></a>Score de conformité
  
Dans le gestionnaire de conformité, les scores de référence passent du niveau de contrôle au niveau de l'élément d'action. Les scores sont basés sur l'objectif (Détectiveing, préventive ou corrective) et l'application (discrétionnaire ou obligatoire) de l'action.

Les éléments d'action sont mappés aux contrôles et lorsqu'un contrôle est mappé à plusieurs éléments d'action, la somme des scores d'action est le score de contrôle. La somme du score de contrôle pour tous les contrôles dans une évaluation donnée est le score d'évaluation. Le score moyen de toutes les évaluations dans un groupe est le score de conformité pour ce groupe.
  
### <a name="mandatory-or-discretionary-controls"></a>Contrôles obligatoires ou discrétionnaires
  
 Les **contrôles obligatoires** sont des contrôles qui ne peuvent pas être contournés intentionnellement ou accidentellement. Un exemple de contrôle obligatoire commun est une stratégie de mot de passe géré de manière centralisée qui définit les exigences de longueur, de complexité et d'expiration des mots de passe. Les utilisateurs doivent se conformer à ces exigences pour accéder au système.
  
 Les **contrôles discrétionnaires** reposent sur les utilisateurs pour comprendre la stratégie et agir en conséquence. Par exemple, une stratégie imposant aux utilisateurs de verrouiller leur ordinateur lorsqu'ils le quittent est un contrôle discrétionnaire, car il s'appuie sur l'utilisateur.
  
### <a name="preventative-detective-or-corrective-controls"></a>Contrôles de prévention, de détective ou de correction
  
 Les **contrôles de prévention** sont des contrôles qui empêchent des risques spécifiques. Par exemple, la protection des informations sur REST à l'aide du chiffrement est un contrôle préventif contre les attaques et les violations. La séparation des tâches est un contrôle préventive permettant de gérer le conflit d'intérêt et de se protéger contre la fraude.
  
 Les **contrôles de détective** sont des contrôles qui surveillent activement les systèmes pour identifier les problèmes ou les comportements irréguliers qui représentent un risque ou qui peuvent être utilisés pour détecter des intrusions ou déterminer si une violation s'est produite. Audit de l'accès au système et actions d'administration privilégiées l'audit est des types de contrôles de surveillance du détective. Conformité réglementaire les audits sont un type de contrôle de détective utilisé pour détecter les problèmes de processus.
  
Les **contrôles de correction** sont des contrôles qui tentent de limiter les effets néfastes d'un incident de sécurité à un minimum, de prendre des mesures correctives pour réduire l'effet immédiat, et de renverser les dommages, si possible. La réponse aux incidents de confidentialité est un contrôle correct pour limiter les dommages et restaurer les systèmes à un état opérationnel après une violation.
  
Chaque contrôle a une valeur affectée dans le gestionnaire de conformité en fonction du risque qu'il représente:

|**Type**|**Score attribué**|
|:-----|:-----|
| PréVentif obligatoire | vingt |
| Discrétionnaire préVentif | 4,9 |
| Détective obligatoire | 3 |
| Discrétion de détective | 0,1 |
| Correction obligatoire | 3 |
| Correction discrétionnaire corrective | 0,1 |
  
## <a name="action-item-workflow"></a>Flux de travail d'élément d'action

Voici le flux de travail de base pour un élément d'action standard:
  
1. Le délégué en matière de conformité, de risque, de confidentialité et/ou de protection des données d'une organisation affecte une tâche à une personne de l'Organisation pour implémenter un contrôle. Cette personne peut être:

    - Un propriétaire de stratégie d'entreprise.
    - Un implémenteur informatique.
    - Une autre personne de l'organisation responsable de l'exécution de la tâche.

2. Cette personne effectue les tâches nécessaires pour implémenter le contrôle, télécharge la preuve de l'implémentation dans le gestionnaire de conformité et marque le contrôle lié à l'élément d'action comme implémenté. Une fois ces tâches terminées, elles affectent l'élément d'action à un évaluateur pour validation.

    Les évaluateurs peuvent être:

    - Des évaluateurs internes qui effectuent la validation des contrôles au sein d'une organisation.
    - Des évaluateurs externes qui examinent, vérifient et certifient la conformité, tels que les organisations indépendantes tierces qui auditent les services Cloud de Microsoft.

3. L'évaluateur valide le contrôle et examine les preuves, puis marque le contrôle comme évalué et les résultats de l'évaluation.

Une fois que tous les contrôles associés à une évaluation sont évalués, l'évaluation est terminée.