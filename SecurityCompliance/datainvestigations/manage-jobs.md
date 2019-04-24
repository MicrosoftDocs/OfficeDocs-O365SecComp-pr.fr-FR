---
title: Gérer les travaux dans les enquêtes de données
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
ms.openlocfilehash: 3b144fbf5f00f3dbb017ac176c75677970f2f7f2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258182"
---
# <a name="manage-jobs-in-data-investigations-preview"></a>Gérer les travaux dans les enquêtes de données (aperçu)

Voici une liste des travaux (qui sont généralement des processus de longue durée) qui sont suivis sous l'onglet **travaux** d'une enquête dans les enquêtes de données (aperçu). Ces travaux sont déclenchés par les actions de l'utilisateur lors de l'utilisation et de la gestion des enquêtes.

| Type du travail            | Description     |
| :----------------- | :----------     |
|Ajout de données à un jeu de preuves | Un utilisateur ajoute les résultats d'une recherche à un ensemble de preuves.  Pour plus d'informations, consultez la rubrique [Rechercher des données dans une enquête](search-for-data.md). |
|Ajout de données à un autre ensemble de preuves | Un utilisateur ajoute des documents d'un ensemble de preuves à un ensemble de preuves différent dans le même cas.|
|Ajout de données non-Office 365 à un jeu de preuves | Un utilisateur télécharge des données non-Office 365 vers un jeu de preuves. Les données sont également indexées pendant ce processus. Par exemple, les fichiers d'un serveur de fichiers local ou d'un ordinateur client sont téléchargés vers un jeu de preuves. Pour plus d'informations, voir [charger des données non-Office 365 dans des preuves](load-non-office365-data.md).| 
|Ajout de données corrigées à un ensemble de preuves | Les données avec des erreurs de traitement sont corrigées et rechargées dans un jeu de preuves. Pour plus d'informations, consultez la rubrique [erreur de correction lors du traitement des données pour une enquête](error-remediation.md). | 
|Comparaison des jeux de charges | Un utilisateur examine les différences entre les différents jeux de charges dans un jeu de preuves. Un jeu de charges est une instance de l'ajout de données à un jeu de preuves. Par exemple, si vous ajoutez les résultats de deux recherches différentes dans le même jeu de preuves, chacun d'entre eux représenterait un jeu de charges. Pour plus d'informations, consultez la rubrique [Manage Load Sets](manage-load-sets.md). |
|Conversion de documents biffés au format PDF|Une fois qu'un utilisateur a annoté un document dans un jeu de preuves et rédige une partie de celui-ci, il peut choisir de convertir le document rédigé en fichier PDF. Cela permet de s'assurer que la partie biffée n'est pas visible lorsque le document est exporté pour présentation. Pour plus d'informations, voir [examiner les données dans les preuves](review-data-in-evidence.md). |
|Estimation des résultats de recherche | Après qu'un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l'outil de recherche recherche dans l'index les éléments qui correspondent à la requête de recherche et prépare une estimation qui inclut le nombre et la taille totale de tous les éléments par la recherche, et le nombre de sources de données Sea rched.  Pour plus d'informations, consultez la rubrique [Rechercher des données dans une enquête](search-for-data.md). | 
|Préparation des données pour l'exportation | Un utilisateur exporte des documents à partir d'un ensemble de preuves. Une fois le processus d'exportation terminé, les utilisateurs peuvent télécharger les données exportées sur un ordinateur local. Pour plus d'informations, consultez la rubrique [exporter des données à partir d'une enquête](export-data.md). | 
|Préparation de la résolution des erreurs |Lorsqu'un utilisateur sélectionne un fichier et crée une nouvelle correction d'erreur dans la vue d'erreur sous l'onglet **traitement** d'une enquête, la première étape du processus consiste à télécharger le fichier contenant l'erreur de traitement vers un emplacement de stockage Azure dans le Cloud Microsoft. Ce travail effectue le suivi de la progression du processus de chargement. Pour plus d'informations sur le flux de travail de correction des erreurs, voir [Error inmédiation lors du traitement des données pour une enquête](error-remediation.md).| 
|Préparation de l'aperçu de la recherche | Après qu'un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l'outil de recherche prépare un exemple de sous-ensemble d'éléments (correspondant à la requête de recherche) qui peut être affiché en aperçu. L'aperçu des résultats de la recherche peut vous aider à déterminer l'efficacité de la recherche.  Pour plus d'informations, consultez la rubrique [Rechercher des données dans une enquête](search-for-data.md). | 
|Réindexation des données des personnes concernées | Lorsque vous ajoutez une personne intéressante à une enquête, tous les éléments partiellement indexés dans les sources de données sélectionnées de la personne concernée sont réindexés par un processus appelé *indexation avancée*. Cette tâche est également déclenchée lorsque vous cliquez sur **mettre à jour l'index** dans la vue d'index sous l'onglet **traitement** d'une enquête. Pour plus d'informations, reportez-vous à [indexation avancée des données pour une enquête](index-data-people-of-interest.md).
|Exécution de l'analyse | Un utilisateur analyse les données d'un ensemble de preuves en exécutant des outils d'analyse tels que la détection de la détection des doublons, l'analyse du thread électronique et l'analyse des thèmes. Pour plus d'informations, reportez-vous [à exécuter Analytics pour effectuer des recherches plus rapidement](run-analytics-to-investigate-faster.md). | 
|Marquage des documents | Cette tâche est déclenchée lorsqu'un utilisateur clique sur **Démarrer le marquage du travail** dans le **panneau balisage** lors de la révision des documents dans un jeu de preuves. Un utilisateur peut démarrer ce travail après avoir balisé des documents dans un ensemble de preuves, puis en les sélectionnant dans le panneau afficher le document. Pour plus d'informations, voir [tag documents in Evidence](tag-documents.md). | 
|||
