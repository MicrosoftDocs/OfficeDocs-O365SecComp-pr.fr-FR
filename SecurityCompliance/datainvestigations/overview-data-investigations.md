---
title: Vue d’ensemble des enquêtes de données (aperçu) dans Microsoft 365
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
description: Cet article décrit la nouvelle outil d’évaluation des données (aperçu) de Microsoft 365.
ms.openlocfilehash: 1e7621d577d8d08fd27dc7e20e6b8e7a3491236f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150676"
---
# <a name="overview-of-data-investigations-preview-in-microsoft-365"></a>Vue d’ensemble des enquêtes de données (aperçu) dans Microsoft 365

Une fuite de données se produit lorsqu’un document contenant du contenu confidentiel, sensible ou malveillant est publié dans un environnement non approuvé. Lors de la détection d’un détournement de données, il est important de contenir rapidement l’environnement, d’évaluer la taille et les emplacements du détournement, d’examiner les activités de l’utilisateur et de supprimer les données déplacées du service. À l’aide de la nouvelle outil d’analyse des données (aperçu), vous pouvez rechercher des données sensibles, malveillantes ou déplacées dans Office 365, examiner ce qui s’est passé et prendre les mesures appropriées pour corriger le problème.  

Cet article décrit l’utilisation des fonctionnalités de l’outil nouvelles enquêtes de données (aperçu) pour résoudre un scénario de débordement de données.

## <a name="data-investigations-preview-workflow"></a>Flux de travail enquêtes de données (aperçu) 

Les sections suivantes décrivent chaque étape du flux de travail intégré dans les enquêtes de données (aperçu). La capture d’écran ci-dessous illustre l’onglet **Accueil** d’une enquête nommée *risque élevé: fuite de documents financiers*. 

![Flux de travail dans l’outil d’enquêtes des données](../media/DataInvestigationsWorkflow.png)

## <a name="search-for-sensitive-malicious-or-misplaced-data"></a>Rechercher des données sensibles, malveillantes ou égarées

Utilisez l’onglet **recherches** pour créer des recherches afin de trouver le bureau 365 pour les données que vous souhaitez corriger. Vous pouvez créer et exécuter des recherches basées sur des requêtes pour identifier un ensemble de messages électroniques et de documents susceptibles de contenir des données déduites, puis les collecter comme preuves à examiner et à analyser. En outre, vous pouvez utiliser l’outil de recherche pour afficher un aperçu des exemples de documents et afficher des statistiques de recherche qui peuvent vous aider à affiner et améliorer les résultats de la recherche. Une fois que vous avez vérifié que les résultats de la recherche contiennent toutes les données pertinentes pour l’enquête, vous ajoutez les résultats de la recherche à l’ensemble de preuves afin de poursuivre l’évaluation, d’influer sur l’évaluation et de prendre des mesures correctives si nécessaire. Pour plus d’informations, consultez la rubrique [Rechercher des données dans une enquête](search-for-data.md).

## <a name="review-and-investigate-evidence"></a>Examiner et examiner les preuves

Utilisez l’onglet **preuve** pour examiner les données que vous avez collectées à partir du service actif, qui dans ce cas est Office 365. Les données de l’ensemble de preuves sont un instantané des résultats de la recherche que vous avez collectés. Lorsque vous ajoutez des résultats de recherche en tant que preuve, un processus est déclenché pour extraire des fichiers, des métadonnées et du texte. Une fois le processus terminé, l’outil d’investigation de données génère un nouvel index de toutes les données et l’ajoute à un ensemble de preuves. Pour toutes les analyses sensibles au temps, cela vous permet de contenir rapidement l’environnement en supprimant les données situées dans les emplacements de contenu d’origine (dans le service réel) lors de l’enquête sur les preuves que vous avez collectées dans un environnement en quarantaine. Une fois les preuves collectées, vous pouvez exécuter des requêtes supplémentaires pour affiner les données par plage de temps, types de fichiers, propriétaires de données et autres types de conditions. Par exemple, à l’aide de l’auteur, de l’expéditeur et des conditions de destinataire, vous pouvez identifier rapidement les personnes qui étaient impliquées dans le déversement des données et si l’une des données propagées a été partagée avec des personnes extérieures à votre organisation.

Vous pouvez également exécuter l’analyse avancée sur les preuves que vous collectez. Cela peut vous fournir des thèmes généraux et organiser des preuves par des threads de messagerie, des doublons exacts et des doublons pour faciliter votre enquête. Vous pouvez passer en revue les documents dans l’affichage de texte extrait ou dans le format de fichier natif, et les baliser avec les résultats de l’enquête. Pour plus d’informations, reportez-vous aux rubriques suivantes :

  - [Consulter les données dans des preuves](review-data-in-evidence.md)

  - [Exécuter les données d’analyse pour investiguer plus rapidement](run-analytics-to-investigate-faster.md)


## <a name="managing-people-of-interest"></a>Gestion des personnes concernées

Utilisez l’onglet **personnes d’intérêt** pour ajouter et gérer les personnes que vous avez identifiées comme des personnes intéressantes lors de votre enquête sur les preuves. Lorsque vous ajoutez des personnes intéressantes, leurs sources de données, telles que leur compte de boîte aux lettres et OneDrive, sont identifiées et mappées. Vous pouvez ensuite étendre les recherches supplémentaires en recherchant uniquement les emplacements de contenu de ces personnes. Lorsqu’elles sont délimitées par des personnes intéressantes, les recherches sont plus efficaces et précises car l’outil réexécute toutes les données non indexées telles que les images ou les types de fichiers non pris en charge. Dans l’onglet **personnes d’intérêt** , vous pouvez également afficher et rechercher les activités de ces personnes dans le journal d’audit afin d’aider davantage votre enquête. Vous pouvez ajouter d’autres personnes intéressantes tout au long de l’enquête. Pour plus d’informations, consultez la rubrique [Manage People of Interest](manage-people-of-interest.md)a investigation.

## <a name="indexing-the-data-of-people-of-interest"></a>Indexation des données des personnes concernées

L’ajout d’une personne intéressante à une enquête réindexe tous les éléments partiellement indexés des sources de données de la personne. Ce processus est appelé *indexation avancée*. L’indexation avancée retraite les données telles que les images et les types de fichiers non pris en charge de sorte que ces données soient entièrement détectables lorsque vous exécutez des recherches pour collecter des données pour une enquête. Utilisez l’onglet **traitement** pour surveiller l’état de l’indexation avancée et corriger les erreurs de traitement susceptibles de se produire à l’aide d’un processus appelé *Correction des erreurs*. Pour plus d’informations, consultez la rubrique [erreur de correction lors du traitement des données pour une enquête](error-remediation.md).

## <a name="exporting-data"></a>Exportation de données

Si vous souhaitez exporter des données, utilisez l' **** onglet exports pour gérer une tâche d’exportation et télécharger des données à partir de l’ensemble de preuves. Lorsque vous exportez des preuves, les données sont téléchargées vers un emplacement de stockage Azure, puis peuvent être téléchargées sur un ordinateur local. Sous l’onglet **exportations** , vous pouvez obtenir l’URL de l’emplacement de stockage Azure et la clé d’estimation du stockage, qui sont toutes deux nécessaires pour télécharger les données exportées. Pour plus d’informations, consultez la rubrique [exporter des données à partir d’une enquête](export-data.md).

## <a name="managing-jobs"></a>Gestion des travaux

Utilisez l’onglet **travaux** pour surveiller les processus de longue durée pour les tâches liées à l’enquête. Cela inclut les travaux d’exécution des recherches, l’ajout de données à un jeu de preuves, la réindexation des données et l’exportation des preuves. Par exemple, vous pouvez créer une recherche dans l’onglet **recherches** qui inclut un grand nombre de sources de données. L’état de ce processus de recherche s’affiche sous l’onglet **travaux** . Pour plus d’informations, consultez [la rubrique gérer des travaux dans une enquête sur les données](manage-jobs.md).

## <a name="configuring-investigation-settings"></a>Configuration des paramètres d’enquête

Utilisez l’onglet **paramètres** pour configurer les paramètres à l’échelle de l’enquête. Cela inclut l’ajout de membres à une enquête, la fermeture ou la suppression d’une enquête, ainsi que la configuration du comportement de recherche et d’analyse. Pour plus d’informations, consultez la rubrique [configure Settings in Data investigations (Preview)](configure-settings-datainvestigations.md).
