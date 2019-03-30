---
title: Gérer les enquêtes juridiques dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: Utilisez des cas eDiscovery dans le centre de sécurité & Compliance dans Office 365 pour gérer l'enquête légale de votre organisation. Si vous disposez d'un abonnement E5, vous pouvez analyser les données de cas en utilisant les fonctionnalités d'analyse de texte, d'apprentissage automatique et de codage prédictif de Advanced eDiscovery.
ms.openlocfilehash: 5bfa4719f2bb065a7064e7dc9d02778a4d032da8
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999917"
---
# <a name="manage-legal-investigations-in-office-365"></a>Gérer les enquêtes juridiques dans Office 365

Les organisations ont de nombreuses raisons de répondre à un cas juridique impliquant certains cadres ou d'autres employés de votre organisation. Il peut être nécessaire de trouver et de contourner rapidement des informations spécifiques dans des e-mails, des documents, des conversations de messagerie instantanée et dans d'autres emplacements de contenu de contenu, utilisés par les employés dans leurs tâches quotidiennes. Vous pouvez effectuer ces opérations et de nombreuses autres activités similaires à l'aide des outils de cas eDiscovery dans le centre de sécurité & Compliance Center.
  
[Gérer les enquêtes juridiques avec des cas eDiscovery](#manage-legal-investigations-with-ediscovery-cases)
  
[Analyser les données de cas à l'aide d'Office 365 Advanced eDiscovery](#analyze-case-data-using-office-365-advanced-ediscovery)
  
**Vous souhaitez savoir comment Microsoft gère ses enquêtes eDiscovery?** Voici un livre [blanc technique](https://go.microsoft.com/fwlink/?linkid=852161) que vous pouvez télécharger et qui explique comment nous utilisons les mêmes outils de recherche et d'enquête Office 365 pour gérer notre flux de travail eDiscovery interne.
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>Gérer les enquêtes juridiques avec des cas eDiscovery

les cas eDiscovery vous permettent de contrôler qui peut créer, consulter et gérer des cas eDiscovery dans votre organisation. Les cas d'utilisation permettent d'ajouter des membres et de contrôler les types d'actions qu'ils peuvent effectuer, de mettre en attente les emplacements de contenu pertinents pour un cas juridique et d'utiliser l'outil de recherche de contenu pour rechercher des contenus susceptibles de répondre à votre cas. Ensuite, vous pouvez également exporter et télécharger ces résultats pour une meilleure analyse par les relecteurs externes. Si votre organisation Office 365 dispose d'un abonnement E5, vous pouvez également préparer les résultats de recherche pour l'analyse dans Advanced eDiscovery.
  
- [Gérer votre flux de travail eDiscovery](ediscovery-cases.md) en créant et en utilisant des cas eDiscovery pour chaque enquête légale que votre organisation doit entreprendre 
    
- [Attribuer des autorisations eDiscovery](assign-ediscovery-permissions.md) pour contrôler qui peut créer et gérer des cas eDiscovery dans votre organisation 
    
- [Configuration des limites de conformité](set-up-compliance-boundaries.md) pour contrôler les emplacements de contenu utilisateur que les gestionnaires eDiscovery peuvent rechercher 
    
- [Rechercher du contenu](search-for-content.md) au sein de votre organisation 
    
- [Préparer le contenu de cas pour Advanced eDiscovery afin de](prepare-search-results-for-advanced-ediscovery.md) pouvoir effectuer des analyses à l'aide d'outils d'analyse puissants de Advanced eDiscovery, tels que la reconnaissance optique de caractères, le Threading de messagerie et le codage prédictif 
    
### <a name="use-scripts-for-advanced-scenarios"></a>Utiliser des scripts pour les scénarios avancés

Comme dans la section précédente qui répertoriait les scripts pour les scénarios de recherche de contenu, nous avons également créé des scripts PowerShell du centre de sécurité & pour vous aider à gérer les cas de découverte électronique.
  
- [Créer un rapport de conservation de découverte électronique](create-a-report-on-holds-in-ediscovery-cases.md) contenant des informations sur toutes les suspensions associées aux cas de découverte électronique dans votre organisation 
    
- [Ajouter des boîtes aux lettres et des emplacements OneDrive](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) pour une liste d'utilisateurs à une conservation eDiscovery 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a>Analyser les données de cas à l'aide d'Office 365 Advanced eDiscovery

Office 365 Advanced eDiscovery repose sur les fonctionnalités de recherche de contenu et eDiscovery décrites dans les sections précédentes. Après avoir créé un cas de découverte électronique, placez les emplacements des dépositaires en conservation et collectez des données susceptibles de répondre à l'incident, vous pouvez ensuite analyser les données à l'aide de l'analyse de texte, de l'apprentissage automatique et des fonctionnalités de codage prédictive d'Advanced découverte. Cela peut aider votre organisation à traiter rapidement des milliers de messages électroniques, de documents et d'autres types de données pour trouver les éléments les plus pertinents pour un cas spécifique. De plus, nous avons unifié la gestion des cas et Advanced eDiscovery afin de pouvoir gérer de façon transparente le même cas dans le centre de sécurité & Compliance Center.
  
> [!NOTE]
> Pour analyser les données d'un utilisateur à l'aide de Advanced eDiscovery, l'utilisateur (le dépositaire des données) doit disposer d'une licence Office 365 E5. Par ailleurs, les utilisateurs disposant d'une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome. Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n'ont pas besoin d'une licence E5. 
  
### <a name="get-started"></a>Prise en main

Le moyen le plus rapide de commencer à utiliser Advanced eDiscovery est de créer un incident et de préparer les résultats de la recherche dans le centre de sécurité & Compliance Center, de charger ces résultats dans Advanced eDiscovery, puis d'exécuter l'analyse rapide pour analyser les données de cas, puis d'exporter les résultats. à des fins de révision externe.
  
- [Obtenir une vue d'ensemble rapide](quick-setup-for-advanced-ediscovery.md) du flux de travail eDiscovery avancé 
    
- [Configurer des utilisateurs et des cas](set-up-users-and-cases-in-advanced-ediscovery.md) pour Advanced eDiscovery en créant un cas, en attribuant des autorisations eDiscovery et en ajoutant des membres de cas, tout en utilisant le centre de sécurité _AMP_ Compliance Center 
    
- [Préparer et charger les données de recherche](prepare-data-for-advanced-ediscovery.md) dans le cas d'Advanced eDiscovery 
    
- [Charger les données non-Office 365](import-non-office-365-data-into-advanced-ediscovery.md) dans un cas pour les analyser dans Advanced eDiscovery 
    
- [Utiliser l'analyse rapide](use-express-analysis-in-advanced-ediscovery.md) pour analyser rapidement les données dans un cas, puis exporter facilement les résultats 
    
### <a name="analyze-data"></a>Analyser les données

Une fois que les données de recherche sont chargées dans le cas dans Advanced eDiscovery, vous utiliserez le module analyze pour commencer l'analyse. La première partie du processus d'analyse consiste à organiser des fichiers dans des groupes de fichiers uniques, des doublons et des doublons (également connus sous le titre de similitudes de documents). Ensuite, vous allez réorganiser les données dans des groupes hiérarchiques de threads et de thèmes de messagerie et, éventuellement, définir des filtres de texte ignorés pour exclure certains textes de l'analyse. Ensuite, vous allez exécuter l'analyse et afficher les résultats.
  
- [En savoir plus sur la similarité des documents](understand-document-similarity-in-advanced-ediscovery.md) pour vous préparer à l'analyse des données dans Advanced eDiscovery 
    
- [Configurez les options](set-analyze-options-in-advanced-ediscovery.md) pour les doublons, les thèmes et le thread électronique, puis exécutez le module Analyze. 
    
- [Configurez ignorer les filtres de texte](set-ignore-text-in-advanced-ediscovery.md) pour exclure le texte et les chaînes de texte de l'analyse; ces filtres ignoreront également le texte lorsque vous exécuterez l'analyse de pertinence. 
    
- [Afficher les résultats](view-analyze-results-in-advanced-ediscovery.md) du processus d'analyse 
    
- [Configurer les paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md) pour le processus d'analyse 
    
### <a name="set-up-relevance-training"></a>Configuration de l’entraînement de pertinence

Le codage prédictif (appelé pertinence) dans Advanced eDiscovery vous permet de former le système sur ce que vous recherchez en vous permettant de prendre des décisions (indiquant si un élément est pertinent ou non) sur un petit ensemble de documents.
  
- [En savoir plus sur la configuration de la formation pertinente](manage-relevance-setup-in-advanced-ediscovery.md) , le marquage des fichiers pertinents pour un cas et la définition des problèmes liés aux incidents 
    
- [Définition des problèmes de cas](define-issues-and-assign-users.md) et affectation de chaque problème à un utilisateur qui lancera les fichiers 
    
- [Ajouter des fichiers importés à la charge actuelle ou nouvelle](set-up-loads-to-add-imported-files.md) qui sera ajoutée à la formation pertinence; une charge est un nouveau lot de fichiers qui sont ajoutés à un cas, puis utilisés pour une formation pertinente. 
    
- [Définir les mots clés](define-highlighted-keywords-and-advanced-options.md) en surbrillance qui peuvent être ajoutés à la formation pertinence; Cela vous permet d'identifier plus facilement les fichiers qui sont pertinents pour un cas 
    
### <a name="run-the-relevance-module"></a>Exécuter le module de pertinence

Après avoir configuré la formation, vous êtes prêt à exécuter le module de pertinence et à évaluer l'efficacité des paramètres de formation, ce qui vous permet de déterminer si vous devez effectuer des formations supplémentaires ou si vous êtes prêt à commencer à marquer les fichiers en tant que pertinentes pour votre cas.
  
- [En savoir plus sur le processus de pertinence](use-relevance-in-advanced-ediscovery.md) et le processus itératif d'évaluation, de marquage, de suivi et de nouvelle formation basé sur un exemple de jeu de fichiers 
    
- [En savoir plus sur l'évaluation](assessment-in-relevance-in-advanced-ediscovery.md) , lorsqu'un expert connaissant le cas révise un ensemble de fichiers de cas et détermine l'efficacité de la formation à la pertinence 
    
- [Évaluer les fichiers de cas](tagging-and-assessment-in-advanced-ediscovery.md) pour calculer l'efficacité ( *richesse* ) des paramètres de formation, puis marquer les fichiers comme pertinents ou non pertinents pour votre cas; Cela vous aide à déterminer si la formation actuelle est suffisante ou si vous devez ajuster les paramètres de formation. 
    
- [Effectuer la formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md) une fois l'évaluation terminée, puis une nouvelle fois sur les fichiers comme pertinents ou non pertinents pour les problèmes que vous avez définis pour le cas 
    
- [Suivre le](track-relevance-analysis-in-advanced-ediscovery.md) processus d'analyse de pertinence afin de déterminer si la formation à la pertinence a atteint votre objectif d'évaluation (appelé *État de formation stable* ) ou si une formation supplémentaire est nécessaire; vous pouvez également afficher les résultats de pertinence pour chaque problème de cas 
    
- [Prendre des décisions en fonction de l'analyse de pertinence](decision-based-on-the-results-in-advanced-ediscovery.md) pour déterminer la taille des fichiers de cas résultants pouvant être exportés à des fins de révision 
    
- [Tester la qualité de l'analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md) afin de valider les décisions de Culling prises lors du processus de pertinence 
    
### <a name="export-results"></a>Exporter les résultats

La dernière étape de l'analyse des données de cas dans Advanced eDiscovery consiste à exporter les résultats de l'analyse pour la révision externe.
  
- [En savoir plus sur l'exportation de données de cas](export-case-data-in-advanced-ediscovery.md)
    
- [Exporter les données de cas](export-results-in-advanced-ediscovery.md)
    
- [Affichage de l’historique du lot et exportation des résultats antérieurs](view-batch-history-and-export-past-results.md)
    
- [Exportation des champs d’un rapport](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a>Autres outils eDiscovery avancés

Advanced eDiscovery offre des outils et des fonctionnalités supplémentaires au-delà de l'analyse des données de cas, de l'analyse de pertinence et de l'exportation de données.
  
- [Exécuter des rapports eDiscovery avancés](run-reports-in-advanced-ediscovery.md)
    
- [Définir les paramètres de cas et de client](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [Utilitaires eDiscovery avancés](use-advanced-ediscovery-utilities.md)
