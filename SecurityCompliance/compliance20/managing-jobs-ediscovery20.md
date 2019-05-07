---
title: Gérer les travaux dans Advanced eDiscovery
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
ms.openlocfilehash: 4d306f6f1a37fad0aa5e3f92cafdb29b1ea37d1c
ms.sourcegitcommit: 25595bc8fae96bc23b7b6d7102a22f37878987c0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33641610"
---
# <a name="manage-jobs-in-advanced-ediscovery"></a>Gérer les travaux dans Advanced eDiscovery

Voici une liste des travaux (qui sont généralement des processus de longue durée) qui sont suivis sous l’onglet **travaux** d’un cas dans Advanced eDiscovery. Ces travaux sont déclenchés par les actions de l’utilisateur lors de l’utilisation et de la gestion des incidents.

| Type du travail            | Description     |
| :----------------- | :----------     |
|Ajout de données à un ensemble de révision | Un utilisateur ajoute les résultats d’une recherche à un jeu de révision. Cette tâche est composée de deux sous-travaux: </br> </br>• **GatheringItems** -une liste d’éléments qui correspondent à la requête de recherche (et la source de données Office 365 dans laquelle ils sont situés) est générée. </br>• Ingestion **_AMP_ indexation** : les éléments qui correspondent à la requête de recherche sont copiés vers un emplacement de stockage Azure (dans ** un processus appelé ingestion), puis ces éléments dans l’emplacement de stockage Azure sont réindexés. Ce nouvel index est utilisé lors de l’interrogation et de l’analyse d’éléments dans le jeu de données. </br></br>Pour plus d’informations, consultez [la rubrique ajouter des résultats de recherche à un jeu de révision](add-data-to-review-set.md). |
|Ajout de données à un autre ensemble de vérification | Un utilisateur ajoute des documents à partir d’un ensemble de réexamen dans le même cas. Pour plus d’informations, consultez [la rubrique ajouter des données à un jeu de réexamen à partir d’un autre ensemble de révision](add-data-to-review-set-from-another-review-set.md).|
|Ajout de données non-Office 365 à un jeu de révision | Un utilisateur télécharge des données non-Office 365 vers un jeu de révision. Les données sont également indexées pendant ce processus. Par exemple, les fichiers d’un serveur de fichiers local ou d’un ordinateur client sont chargés dans un jeu de révision. Pour plus d’informations, voir [charger des données non-Office 365 dans un jeu de révision](load-non-office365-data.md).| 
|Ajout de données corrigées à un jeu de révision | Les données avec des erreurs de traitement sont corrigées et rechargées dans un jeu de révision. Pour plus d’informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md). | 
|Comparaison des jeux de charges | Un utilisateur examine les différences entre les différents jeux de charges dans un jeu de réexamen. Un jeu de charges est une instance de l’ajout de données à un jeu de réexamen. Par exemple, si vous ajoutez les résultats de deux recherches différentes au même jeu de réexamen, chacun d’entre eux représenterait un jeu de charges. Pour plus d’informations, consultez la rubrique [Manage Load Sets](manage-load-sets.md). |
|Conversion de documents biffés au format PDF|Une fois qu’un utilisateur a annoté un document dans un jeu de révision et rédige une partie de celui-ci, il peut choisir de convertir le document rédigé en fichier PDF. Cela permet de s’assurer que la partie biffée n’est pas visible si le document est exporté pour présentation. Pour plus d’informations, consultez [la rubrique View documents in a Review Set](annotating-and-redacting-documents.md). |
|Estimation des résultats de recherche | Après qu’un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l’outil de recherche recherche dans l’index les éléments qui correspondent à la requête de recherche et prépare une estimation qui inclut le nombre et la taille totale de tous les éléments par la recherche, et le nombre de sources de données Sear ched.  Pour plus d’informations, reportez-vous [à la rubrique Collect Data for a case](collecting-data-for-ediscovery.md). | 
|Préparation des données pour l’exportation | Un utilisateur exporte des documents à partir d’un à partir d’un ensemble de révision. Une fois le processus d’exportation terminé, les utilisateurs peuvent télécharger les données exportées sur un ordinateur local. Pour plus d’informations, consultez la rubrique [Export case Data](exporting-data-ediscover20.md). | 
|Préparation de la résolution des erreurs |Lorsqu’un utilisateur sélectionne un fichier et crée une nouvelle correction d’erreur dans la vue d’erreur sous l’onglet **traitement** d’un cas, la première étape du processus consiste à télécharger le fichier contenant l’erreur de traitement vers un emplacement de stockage Azure dans le Cloud Microsoft. Ce travail effectue le suivi de la progression du processus de chargement. Pour plus d’informations sur le flux de travail de correction des erreurs, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md). | 
|Préparation de l’aperçu de la recherche | Après qu’un utilisateur a créé et exécuté une nouvelle recherche (ou ré-exécute une recherche existante), l’outil de recherche prépare un exemple de sous-ensemble d’éléments (correspondant à la requête de recherche) qui peut être affiché en aperçu. L’aperçu des résultats de la recherche vous permet de déterminer l’efficacité de la recherche.  Pour plus d’informations, reportez-vous [à la rubrique Collect Data for a case](collecting-data-for-ediscovery.md#view-search-results-and-statistics). | 
|Réindexation des données du dépositaire | Lorsque vous ajoutez un dépositaire à un cas, tous les éléments partiellement indexés des sources de données sélectionnées du dépositaire sont réindexés par un processus appelé *indexation avancée*. Cette tâche est également déclenchée lorsque vous cliquez sur **mettre à jour l’index** dans la vue index sous l’onglet **traitement** d’un cas. Pour plus d’informations, consultez la rubrique [Advanced Indexing of dépositaire Data](indexing-custodian-data.md).
|Exécution de l’analyse | Un utilisateur analyse les données d’un jeu de réexamen en exécutant des outils d’analyse eDiscovery avancés, tels que la détection de la détection des doublons, l’analyse du Threading de messagerie et l’analyse des thèmes. Pour plus d’informations, consultez [la rubrique Analyze Data in a Review Set](analyzing-data-in-review-set.md). | 
|Marquage des documents | Cette tâche est déclenchée lorsqu’un utilisateur clique sur **Démarrer le marquage du travail** dans le **panneau balisage** lors de la révision des documents dans un jeu de révision. Un utilisateur peut démarrer ce travail après le marquage des documents dans un ensemble de révision, puis les sélectionner en bloc dans le panneau document d’affichage. Pour plus d’informations, voir [tag documents in a Review Set](tagging-documents.md). | 
|||


## <a name="job-status"></a>État du travail

Le tableau suivant décrit les différents États d’État pour les travaux.

| Statut           | Description     |
| :----------------- | :----------     |
| Submitted | Une nouvelle tâche a été créée.  La date et l’heure auxquelles le travail a été soumis s’affichent dans la colonne **créé** sous l’onglet **travaux** . |
| Échec de l’envoi | Échec de l’envoi du travail.  Essayez de réexécuter l’action qui a déclenché le travail. |
| En cours | Le travail est en cours, vous pouvez surveiller la progression de la tâche dans l’onglet **travaux** . |
| Satisfaisant | Le travail s’est terminé avec succès. La date et l’heure de fin du travail s’affichent dans la colonne **terminé** de l’onglet **travaux** . |
| Partiellement réussi | Le travail a été partiellement réussi. |
| Failed | Échec du travail.  Essayez de réexécuter l’action qui a déclenché le travail. Si la tâche échoue pour la deuxième fois, nous vous recommandons de contacter le support Microsoft et de fournir les informations de support du travail. |
