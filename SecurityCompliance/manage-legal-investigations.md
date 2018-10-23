---
title: Gérer les enquêtes légales dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e
description: Utilisez les cas eDiscovery de sécurité Office 365 &amp; centre de conformité pour gérer l’enquête juridique de votre organisation. Si vous disposez d’un abonnement E5, vous pouvez analyser plus données cas à l’aide de l’analytique de texte, ordinateur apprentissage et des fonctionnalités de codage prévision d’eDiscovery avancée.
ms.openlocfilehash: 4e7b9117b3f0cb2fd6d4e70a7767f3cbe7b79724
ms.sourcegitcommit: 01813cb9bbc2400d21bc99144745af953f9356e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2018
ms.locfileid: "25719048"
---
# <a name="manage-legal-investigations-in-office-365"></a>Gérer les enquêtes légales dans Office 365

Les organisations ont plusieurs raisons pour répondre à une affaire juridique impliquant certains cadres ou autres employés de votre organisation. Cela peut impliquer rapidement recherche et conservation pour plus d’informations spécifiques enquête dans le courrier électronique, des documents, des conversations par messagerie instantanées et autres emplacements de contenu utilisés par des personnes dans leurs tâches quotidiennes. Vous pouvez effectuer ces et nombreuses autres activités similaires de sécurité Office 365 à l’aide des outils cas eDiscovery &amp; centre de conformité.
  
[Gérer les enquêtes légales avec cas eDiscovery](#manage-legal-investigations-with-ediscovery-cases)
  
[Analyser les données de dossiers à l’aide d’Office 365 avancée de découverte électronique](#analyze-case-data-using-office-365-advanced-ediscovery)
  
**Pour connaître la façon dont Microsoft gère ses enquêtes eDiscovery ?** Voici un [livre blanc](https://go.microsoft.com/fwlink/?linkid=852161) que vous pouvez télécharger qui explique comment nous utilisons les outils de recherche et d’enquête même Office 365 pour gérer notre flux de travail interne eDiscovery.
   
## <a name="manage-legal-investigations-with-ediscovery-cases"></a>Gérer les enquêtes légales avec cas eDiscovery

Découverte des cas vous permettent de contrôler qui peut créer, accéder et gérer des affaires eDiscovery dans votre organisation. Pour ajouter des membres et contrôle les types d’actions qu’ils peuvent effectuer, placer une suspension sur les emplacements de contenu approprié à une affaire juridique et utilisez l’outil de recherche de contenu pour rechercher les emplacements de blocage pour le contenu qui peut être réactif à un cas de cas d’utilisation. Ensuite, vous pouvez également exporter et télécharger ces résultats pour une analyse approfondie des réviseurs externes. Si votre organisation Office 365 dispose d’un abonnement de E5, vous pouvez également préparer des résultats de recherche pour l’analyse d’eDiscovery avancée.
  
- [Gérer votre flux de travail eDiscovery](ediscovery-cases.md) en créant et en utilisant cas eDiscovery pour chaque enquête juridique de votre organisation dispose d’entreprendre 
    
- [Attribuer des autorisations de découverte électronique](assign-ediscovery-permissions.md) à contrôler qui peut créer et gérer des affaires eDiscovery dans votre organisation 
    
- [Configurer des limites de conformité](set-up-compliance-boundaries.md) pour contrôler les emplacements de contenu utilisateur qui peuvent de rechercher des gestionnaires de découverte électronique 
    
- [Recherche de contenu](search-for-content.md) dans votre organisation 
    
- [Contenu du dossier préparer pour la découverte avancée](prepare-search-results-for-advanced-ediscovery.md) afin que vous pouvez effectuer à l’aide de l’analyse puissants analytique de découverte électronique outils avancés, tels que la reconnaissance optique de caractères, les threads de messagerie et de codage prédictive 
    
### <a name="use-scripts-for-advanced-scenarios"></a>Utiliser des scripts pour des scénarios avancés

Comme la section précédente qui répertoriés des scripts pour les scénarios de recherche de contenu, nous avons créé également une sécurité &amp; scripts PowerShell de centre de conformité pour vous aider à gérer des affaires eDiscovery.
  
- [Rapport de suspension créer une découverte électronique](create-a-report-on-holds-in-ediscovery-cases.md) qui contient des informations sur toutes les contient associé au cas eDiscovery dans votre organisation 
    
- [Ajouter les boîtes aux lettres et les emplacements de OneDrive](use-a-script-to-add-users-to-a-hold-in-ediscovery.md) pour une liste d’utilisateurs à une découverte électronique permanente 
  
## <a name="analyze-case-data-using-office-365-advanced-ediscovery"></a>Analyser les données de dossiers à l’aide d’Office 365 avancée de découverte électronique

Office 365 avancées eDiscovery s’appuie sur les fonctions de recherche et eDiscovery contenues décrites dans les sections précédentes. Après avoir créé un cas eDiscovery, place des emplacements dépositaire blocage et collectant des données qui peuvent être sensible à la casse, vous pouvez analyser puis davantage les données à l’aide de l’analytique de texte, l’ordinateur de la formation et les fonctionnalités de codage prédictives des options avancées découverte électronique. Cela peut aider votre organisation à traiter rapidement des milliers de messages électroniques, des documents et autres types de données pour rechercher les éléments qui sont probables pertinents pour un cas spécifique. Et, nous avons unifiée de gestion et découverte avancée afin que vous pouvez gérer en toute transparence la même casse au sein de la sécurité &amp; centre de conformité.
  
> [!NOTE]
> Pour analyser les données d’un utilisateur à l’aide de la découverte électronique avancée, l’utilisateur (le dépositaire des données) doit être affecté à une licence Office 365 E5. Autrement, les utilisateurs possédant une licence Office 365 E1 ou E3 peuvent être affectés à une licence autonome de découverte avancée. Les administrateurs et des agents de conformité qui sont affectées à des cas et utilisent eDiscovery avancée pour analyser des données inutile d’une licence E5. 
  
### <a name="get-started"></a>Prise en main

Pour prendre en main eDiscovery avancée le plus rapide consiste à créer un cas et de préparer les résultats de la recherche de la sécurité &amp; centre de conformité, charger les résultats d’eDiscovery avancée et exécutez analyse Express pour analyser les cas de données, puis l’exporter le résultats de la révision externe.
  
- [Obtenez un aperçu rapide](quick-setup-for-advanced-ediscovery.md) du flux de travail avancées eDiscovery 
    
- [Configurer les utilisateurs et les cas](set-up-users-and-cases-in-advanced-ediscovery.md) eDiscovery avancé en créant un incident, attribution d’autorisations de découverte et ajout de cas membres, tout à l’aide de la sécurité &amp; centre de conformité 
    
- [Préparer et charger des données de recherche](prepare-data-for-advanced-ediscovery.md) dans le cas d’eDiscovery avancée 
    
- [Charger les données non Office 365](import-non-office-365-data-into-advanced-ediscovery.md) dans à un cas à analyser de découverte électronique avancée 
    
- [Analyse d’utilisation Express](use-express-analysis-in-advanced-ediscovery.md) pour analyser rapidement les données dans un cas et puis exporter facilement les résultats 
    
### <a name="analyze-data"></a>Analyser les données

Une fois que les données de recherche sont chargées dans le cas d’eDiscovery avancé, vous allez utiliser le module d’analyse pour démarrer l’analyse. La première partie du processus d’analyse se compose d’organisation des fichiers dans des groupes de fichiers uniques, doublons et près de doublons (également appelé similarité de document). Vous devez regrouper les données à nouveau hiérarchique des threads de messagerie et les thèmes, puis, si vous le souhaitez, set ignorer les filtres de texte pour exclure certain texte d’analyse. Vous allez exécuter l’analyse, puis afficher les résultats.
  
- [Obtenir des informations sur la similarité de document](understand-document-similarity-in-advanced-ediscovery.md) pour vous préparer à l’analyse des données d’eDiscovery avancée 
    
- [Définir les options](set-analyze-options-in-advanced-ediscovery.md) pour près de doublons, thèmes et messagerie threading, puis exécutez le module d’analyse 
    
- [Définir des filtres d’ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) à exclure des chaînes de texte et le texte d’en cours d’analyse ; Ces filtres également ignore le texte lorsque vous exécutez l’analyse de la pertinence 
    
- [Afficher les résultats](view-analyze-results-in-advanced-ediscovery.md) du processus d’analyse 
    
- [Configurer les paramètres avancé](set-analyze-advanced-settings-in-advanced-ediscovery.md) pour le processus d’analyse 
    
### <a name="set-up-relevance-training"></a>Configurer la formation de pertinence

Prédictive codage (appelée pertinence) de la catégorie Avancé eDiscovery vous permet de former le système sur ce que vous cherchez en vous laissant pour prendre des décisions (si un élément est pertinent ou non) sur un petit jeu de documents.
  
- [En savoir plus sur la configuration de formation de pertinence](manage-relevance-setup-in-advanced-ediscovery.md) , marquer des fichiers qui sont pertinents pour un cas et la définition de cas de problèmes 
    
- [Problèmes de cas définir](define-issues-and-assign-users.md) et affecter chaque problème à un utilisateur qui sera former les fichiers 
    
- [Ajouter les fichiers importés nouvelle ou en cours de chargement](set-up-loads-to-add-imported-files.md) qui sera ajouté à la formation de pertinence ; une charge est un nouveau lot de fichiers qui sont ajoutés à un cas et puis utilisés pour la formation de pertinence 
    
- [Définir mise en surbrillance des mots clés](define-highlighted-keywords-and-advanced-options.md) qui peuvent être ajoutés à la formation de pertinence ; Cela vous permet de mieux identifier les fichiers qui sont pertinents pour un incident 
    
### <a name="run-the-relevance-module"></a>Exécuter le module de la pertinence

Après l’installation de formation, vous êtes prêt à exécuter le module de la pertinence et évaluer l’efficacité des paramètres de formation cette résultats dans un classement de pertinence qui vous aideront à décider si vous devez effectuer une formation supplémentaire ou si vous êtes prêt à démarrer le balisage de fichiers en tant que appropriée à votre cas.
  
- [Découvrez le processus de la pertinence](use-relevance-in-advanced-ediscovery.md) et le processus d’évaluation itératif, marquage, le suivi et recyclage basé sur exemple d’ensemble de fichiers 
    
- [Obtenir des informations sur l’évaluation](assessment-in-relevance-in-advanced-ediscovery.md) , où un expert connaissant le cas examine un ensemble de dossiers et détermine l’efficacité de la formation de pertinence 
    
- [Évaluer les fichiers cas](tagging-and-assessment-in-advanced-ediscovery.md) pour calculer l’efficacité (appelée *richesse* ) de paramètres de la formation, puis fichiers balise pertinent ou non pertinents pour votre cas ; Cela vous permet de déterminer si la formation en cours est suffisante ou si vous devez ajuster les paramètres de formation. 
    
- [Effectuer la formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md) après évaluation est terminée, puis à nouveau balise fichiers comme pertinentes ou pas utiles pour les problèmes que vous avez définie pour le cas 
    
- Processus de [suivi de l’analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md) afin de déterminer si formation de pertinence est parvenu votre cible d’évaluation (appelé *état stable formation* ) ou plus de formations si nécessaire ; Vous pouvez également afficher les résultats de la pertinence pour chaque problème de cas 
    
- [Prendre des décisions basées sur l’analyse de pertinence](decision-based-on-the-results-in-advanced-ediscovery.md) pour déterminer que la taille du jeu résultant des cas de fichiers qui peuvent être exportés pour révision 
    
- [Test de la qualité de l’analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md) pour valider les décisions élimination prises au cours du processus de pertinence 
    
### <a name="export-results"></a>Exporter les résultats

La dernière étape de l’analyse des données de cas d’eDiscovery avancée est pour exporter les résultats de l’analyse pour révision externe.
  
- [En savoir plus sur l’exportation de données de dossiers](export-case-data-in-advanced-ediscovery.md)
    
- [Exporter des données de cas](export-results-in-advanced-ediscovery.md)
    
- [Afficher l’historique des commandes et exporter des résultats antérieurs](view-batch-history-and-export-past-results.md)
    
- [Champs du rapport d’exportation](export-report-fields-in-advanced-ediscovery.md)
    
### <a name="other-advanced-ediscovery-tools"></a>Autres outils avancés eDiscovery

Découverte avancée fournit des outils supplémentaires et fonctionnalités au-delà d’analyser les données de cas, l’analyse de la pertinence et d’exporter des données.
  
- [Exécuter des rapports avancées eDiscovery](run-reports-in-advanced-ediscovery.md)
    
- [Définir des paramètres de la casse et client](define-case-and-tenant-settings-in-advanced-ediscovery.md)
    
- [Utilitaires de découverte électronique avancées](use-advanced-ediscovery-utilities.md)
