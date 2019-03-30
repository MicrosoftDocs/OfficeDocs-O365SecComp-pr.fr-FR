---
title: Gérer les travaux dans Advanced eDiscovery (aperçu)
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
ms.openlocfilehash: a5b9975803e0243f873bdd5f538dbc5e62907327
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997050"
---
# <a name="manage-jobs-in-advanced-ediscovery-preview"></a>Gérer les travaux dans Advanced eDiscovery (aperçu)

Voici une liste des travaux (qui sont généralement des processus de longue durée) qui sont suivis sous l'onglet **travaux** d'un cas dans Advanced EDiscovery (aperçu). Ces travaux sont déclenchés par les actions de l'utilisateur lors de l'utilisation et de la gestion des incidents.

| Type du travail            | Description     |
| :----------------- | :----------     |
|Ajout de données à une plage de travail | Un utilisateur ajoute les résultats d'une recherche à une plage de travail.  Pour plus d'informations, consultez [la rubrique ajouter des résultats de recherche à un jeu de travail](add-data-to-working-set.md). |
|Ajout de données à un autre jeu de travail | Un utilisateur ajoute des documents d'une plage de travail à une plage de travail différente dans le même cas.|
|Ajout de données non Office 365 à un jeu de travail | Un utilisateur télécharge des données non-Office 365 vers une plage de travail. Les données sont également indexées pendant ce processus. Par exemple, les fichiers d'un serveur de fichiers local ou d'un ordinateur client sont téléchargés vers un jeu de travail. Pour plus d'informations, voir [charger des données non-Office 365 dans un jeu de travail](load-non-office365-data.md).| 
|Ajout de données corrigées à une plage de travail | Les données avec des erreurs de traitement sont corrigées et rechargées dans un jeu de travail. Pour plus d'informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md). | 
|Comparaison des jeux de charges | Un utilisateur examine les différences entre les différents jeux de charges dans un jeu de travail. Un jeu de charges est une instance de l'ajout de données à une plage de travail. Par exemple, si vous ajoutez les résultats de deux recherches différentes au même jeu de travail, chacune d'elles représenterait un jeu de charges. Pour plus d'informations, consultez la rubrique [Manage Load Sets](manage-load-sets.md). |
|Conversion de documents biffés au format PDF|Une fois qu'un utilisateur a annoté un document dans une plage de travail et rédige une partie de celui-ci, il peut choisir de convertir le document rédigé en fichier PDF. Cela permet de s'assurer que la partie biffée n'est pas visible si le document est exporté pour présentation. Pour plus d'informations, consultez [la rubrique afficher des documents dans un jeu de travail](annotating-and-redacting-documents.md). |
|Estimation des résultats de recherche | Après qu'un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l'outil de recherche recherche dans l'index les éléments qui correspondent à la requête de recherche et prépare une estimation qui inclut le nombre et la taille totale de tous les éléments par la recherche, et le nombre de sources de données Sear CHED.  Pour plus d'informations, reportez-vous [à la rubrique Collect Data for a case](collecting-data-for-ediscovery.md). | 
|Préparation des données pour l'exportation | Un utilisateur exporte des documents FEOM à partir d'une plage de travail. Une fois le processus d'exportation terminé, les utilisateurs peuvent télécharger les données exportées sur un ordinateur local. Pour plus d'informations, consultez la rubrique [Export case Data](exporting-data-ediscover20.md). | 
|Préparation de la résolution des erreurs |Lorsqu'un utilisateur sélectionne un fichier et crée une nouvelle correction d'erreur dans la vue d'erreur sous l'onglet **traitement** d'un cas, la première étape du processus consiste à télécharger le fichier contenant l'erreur de traitement vers un emplacement de stockage Azure dans le Cloud Microsoft. Ce travail effectue le suivi de la progression du processus de chargement. Pour plus d'informations sur le flux de travail de correction des erreurs, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md). | 
|Préparation de l'aperçu de la recherche | Après qu'un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l'outil de recherche prépare un exemple de sous-ensemble d'éléments (correspondant à la requête de recherche) qui peut être affiché en aperçu. L'aperçu des résultats de la recherche vous permet de déterminer l'efficacité de la recherche.  Pour plus d'informations, reportez-vous [à la rubrique Collect Data for a case](collecting-data-for-ediscovery.md#view-search-results-and-statistics). | 
|Réindexation des données du dépositaire | Lorsque vous ajoutez un dépositaire à un cas, tous les éléments partiellement indexés des sources de données sélectionnées du dépositaire sont réindexés par un processus appelé *indexation avancée*. Cette tâche est également déclenchée lorsque vous cliquez sur **mettre à jour l'index** dans la vue index sous l'onglet **traitement** d'un cas. Pour plus d'informations, consultez la rubrique [Advanced Indexing of dépositaire Data](indexing-custodian-data.md).
|Exécution de l'analyse | Un utilisateur analyse les données d'un jeu de travail en exécutant des outils d'analyse eDiscovery avancés, tels que la détection de la détection des doublons, l'analyse du Threading de messagerie et l'analyse des thèmes. Pour plus d'informations, consultez [la rubrique Analyze Data in a Working Set](analyzing-data-in-working-set.md). | 
|Marquage des documents | Cette tâche est déclenchée lorsqu'un utilisateur clique sur **Démarrer le marquage du travail** dans le **panneau marquage** lors de l'examen des documents dans une plage de travail. Un utilisateur peut démarrer ce travail après avoir balisé des documents dans un jeu de travail, puis en les sélectionnant dans le panneau afficher le document. Pour plus d'informations, voir [tag documents in a Working](tagging-documents.md). | 
|||
