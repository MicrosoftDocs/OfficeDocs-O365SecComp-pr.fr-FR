---
title: Vue d’ensemble de la solution avancée eDiscovery dans Microsoft 365
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
description: Cet article décrit la nouvelle version de Advanced eDiscovery dans Microsoft 365.
ms.openlocfilehash: a29e156cee9af1f5bf4ef3339614a1db52254d6c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154996"
---
# <a name="overview-of-the-advanced-ediscovery-solution-in-microsoft-365"></a>Vue d’ensemble de la solution avancée eDiscovery dans Microsoft 365

La solution eDiscovery avancée de Microsoft 365 repose sur les fonctionnalités d’analyse et de découverte électronique existantes dans Office 365. Cette nouvelle solution, appelée *Advanced eDiscovery*, fournit un flux de travail de bout en bout pour conserver, collecter, examiner, analyser et exporter du contenu réactif aux investigations internes et externes de votre organisation. Il permet également aux équipes juridiques de gérer l’ensemble du flux de travail de notification de suspension légale pour communiquer avec les dépositaires impliqués dans un cas. 

## <a name="alignment-with-edrm"></a>Alignement avec EDRM

Le flux de travail intégré de Advanced eDiscovery s’aligne sur le processus eDiscovery décrit par le modèle de référence de découverte électronique (EDRM). 

![Modèle de référence de découverte électronique (EDRM)](../media/EDRMv1.png)

(Image source courtoisie de edrm.net. L’image source a été mise à disposition sous la licence non à l’attribution 3,0 Creative.

À un niveau élevé, voici comment Advanced eDiscovery prend en charge le flux de travail EDRM:

- **Identification** -une fois que vous avez identifié les personnes intéressantes pour une enquête, vous pouvez les ajouter en tant que dépositaires (également appelés dépositaires de *données*, car ils peuvent posséder des informations pertinentes pour l’enquête) vers une avancée cas de découverte électronique. Une fois que les utilisateurs sont ajoutés en tant que dépositaires, il est facile de conserver, de collecter et de consulter les documents des dépositaires.

- **Préservation** : pour conserver et protéger les données relatives à une enquête, la fonctionnalité eDiscovery avancée vous permet de placer une suspension légale sur les sources de données associées aux dépositaires dans un cas. Vous pouvez également placer des données non privatives de place en conservation. De plus, Advanced eDiscovery dispose d’un flux de travail de communications intégré qui vous permet d’envoyer des notifications de conservation légale aux dépositaires et d’effectuer le suivi de leurs remerciements.

- **Collection** : une fois que vous avez identifié (et préservé) les sources de données pertinentes pour l’enquête, vous pouvez utiliser l’outil de recherche intégré dans Advanced eDiscovery Search for and Collect Live Data from the privatives Data sources (et les sources de données non privatives de cœur). , le cas échéant) susceptibles de concerner le cas.

- **Processing** -une fois que vous avez collecté toutes les données pertinentes pour le cas, l’étape suivante consiste à le traiter pour révision et analyse. Dans Advanced eDiscovery, cela signifie que les données sur place que vous avez identifiées dans la phase de collecte sont copiées vers un emplacement de stockage Azure (appelé « *jeu de révision*»), ce qui vous fournit une vue statique des données de cas. 
 
- **Révision** -une fois que des données ont été ajoutées à un jeu de révisions, vous pouvez afficher des documents spécifiques et exécuter des requêtes supplémentaires pour réduire les données à celles qui sont les plus pertinentes pour le cas. En outre, vous pouvez annoter et marquer des documents spécifiques.
 
- **Analysis** -Advanced eDiscovery fournit des outils d’analyse intégrés qui vous aident à approfondir les données de l’ensemble de vérifications que vous déterminez n’est pas pertinent pour l’enquête. En plus de réduire le volume des données pertinentes, Advance eDiscovery (aperçu) vous aide également à enregistrer les coûts de la révision légale en vous permettant d’organiser le contenu afin de faciliter et d’améliorer l’efficacité du processus de révision.

- **Production** et **Présentation** : lorsque vous êtes prêt, vous pouvez exporter des documents à partir d’un jeu de vérification pour révision légale. Vous pouvez exporter des documents dans leur format d’origine ou dans un format spécifié par EDRM afin qu’ils puissent être importés dans des applications tierces.

## <a name="advanced-ediscovery-workflow"></a>Flux de travail eDiscovery avancé

Les sections suivantes décrivent chaque étape du flux de travail intégré de bout en bout dans Advanced eDiscovery. La capture d’écran suivante montre l’onglet **Accueil** d’un cas nommé *responsabilité du produit 2019002*. Remarque les onglets de flux de travail en haut de la page sont séquencés pour s’aligner avec le processus EDRM. 

Pour plus d’informations sur le flux de travail de bout en bout dans Advanced eDiscovery, reportez-vous à cette [vidéo de mécanique Microsoft](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Les onglets dans Advanced eDiscovery suivent le flux de travail EDRM](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Gestion des dépositaires

Utilisez l' **** onglet dépositaires pour ajouter et gérer les personnes que vous avez identifiées comme des personnes intéressantes dans le cas. Lorsque vous ajoutez des dépositaires, vous pouvez rapidement effectuer des actions liées aux dépositaires, telles que la mise en attente légale sur les sources de données des dépositaires, comme leur compte de boîte aux lettres et OneDrive, la communication avec des dépositaires et la recherche de sources de données de dépositaires pour collecter du contenu. Cela est pertinent pour le cas. À mesure que le cas progresse, il est facile d’ajouter de nouveaux dépositaires ou de libérer des dépositaires à partir du cas. Pour plus d’informations, consultez la rubrique [utiliser des dépositaires dans Advanced eDiscovery](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Gestion des notifications de conservation légale

Utilisez l’onglet **communications** pour gérer le processus de communication avec les dépositaires dans le cas. Une notice légale indique aux dépositaires de conserver tout contenu susceptible d’être pertinent pour le cas. Les équipes juridiques doivent être en mesure de suivre que les avis ont été reçus, lus et reconnus par les dépositaires. Le flux de travail de communication dans Advanced eDiscovery vous permet de créer et d’envoyer des notifications initiales, des rappels, des notifications de publication et des escalades si les dépositaires ne reconnaissent pas une notification de blocage. Pour plus d’informations, consultez la rubrique [utilisation des communications dans Advanced eDiscovery](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Gestion de la conservation du contenu

Lorsque vous ajoutez un dépositaire à un cas, vous avez la possibilité de placer une conservation sur des données privatives. Utilisez l' **** onglet suspensions pour gérer le blocage créé lorsque vous ajoutez des dépositaires, et pour gérer les suspensions légales supplémentaires associées au cas (par exemple, vous pouvez identifier et mettre en attente des sources de données non privatives de place). Vous pouvez également modifier n’importe quelle conservation dans le cas et en faire une conservation basée sur une requête de sorte que seul le contenu correspondant à la requête soit placé en conservation. Par exemple, vous pouvez ajouter une plage de dates à la suspension afin que seul le contenu créé dans une date spécifique soit dans l’intervalle préservé. Vous pouvez également obtenir des statistiques sur le contenu en attente, supprimer la conservation une fois qu’elle n’est plus pertinente pour le cas ou la supprimer. Pour plus d’informations, consultez la rubrique Manage holds [in Advanced eDiscovery](managing-holds.md).

## <a name="indexing-custodian-data"></a>Indexation des données des dépositaires

Lorsque vous ajoutez un dépositaire et les sources de données privatives de Troie correspondantes à un cas, tout élément partiellement indexé d’une source de données de dépositaire est ré-indexé (par un processus appelé *indexation avancée*). Cela permet de trouver des informations privatives de cœur, telles que des images, des types de fichiers non pris en charge et d’autres contenus potentiellement non indexés, qui peuvent être entièrement recherchés lorsque vous effectuez des recherches pour collecter des données pour le cas. Utilisez l’onglet **traitement** pour surveiller l’état des erreurs d’indexation et de traitement avancées (à l’aide d’un processus appelé correction des *Erreurs*.) Pour plus d’informations, voir [corriger les erreurs de traitement dans Advanced eDiscovery](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Collecte des données d’un cas

L’onglet **recherches** permet de créer des recherches pour rechercher des sources de données privatives de Troie et non-privatives de place dans Office 365 pour le contenu pertinent pour le cas. Vous pouvez créer et exécuter des recherches basées sur des requêtes (à l’aide de mots clés et de conditions) pour identifier un ensemble de messages électroniques et de documents pertinents pour le cas et que vous souhaitez examiner et analyser dans les étapes suivantes dans le flux de travail de découverte électronique. Vous pouvez créer une ou plusieurs recherches associées au cas. En outre, vous pouvez utiliser l’outil de recherche pour afficher un aperçu des exemples de documents et afficher des statistiques de recherche qui peuvent vous aider à affiner et améliorer les résultats de la recherche. Une fois que vous avez vérifié que les résultats de la recherche contiennent toutes les données pertinentes pour le cas, vous ajoutez les résultats de la recherche à un jeu de révision pour une révision, une analyse et, si nécessaire, l’élimination. Pour plus d’informations, reportez-vous à [la rubrique collecte de données pour un cas dans Advanced eDiscovery](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzing-case-data"></a>Révision et analyse des données de cas

Utilisez l’onglet **examiner les ensembles** pour examiner et analyser le contenu que vous avez collecté à partir du système réel et ajouté à un jeu de révision. Un *ensemble de révision* est une collection statique de ces données (en d’autres termes, une copie hors connexion) de données privatives de temps (et, le cas échéant, de données non privatives) que vous avez collectées au cours de la phase précédente du flux de travail de découverte électronique. Lorsque vous ajoutez des résultats de recherche à un ensemble de révision, un processus est déclenché qui extrait les fichiers des conteneurs, extrait les métadonnées et extrait le texte. Une fois le processus terminé, le système génère un nouvel index de toutes les données collectées auprès des dépositaires et ajoutés à l’ensemble de révision. Une fois que les données sont ajoutées à l’ensemble de vérification, vous pouvez exécuter des requêtes supplémentaires pour affiner les données de cas, afficher les données au format texte ou au format de fichier natif, et annoter, biffer et baliser les documents dans l’ensemble de révision. En outre, vous pouvez effectuer des analyses avancées, telles que l’identification de la duplication de documents, le Threading de courrier électronique et les thèmes. Une fois que vous avez consulté les données uniquement sur ce qui est pertinent pour le cas, vous pouvez télécharger les documents directement ou les exporter, ainsi que les métadonnées de fichier, les annotations et les balises. Pour plus d’informations, reportez-vous aux rubriques suivantes :

  - [Vérifier les données de cas dans Advanced eDiscovery](reviewing-data-in-review-set.md)
  - [Analyser les données d’un ensemble de vérification dans Advanced eDiscovery](analyzing-data-in-review-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportation de données à des fins de révision et de présentation

Une fois que vous avez exporté les données à partir d’un jeu de révision, utilisez l’onglet **exportations** pour gérer une tâche d’exportation et télécharger des données à partir d’un jeu de révision. Lorsque vous exportez un jeu de révision, les données sont téléchargées vers un emplacement de stockage Azure, puis peuvent être téléchargées sur un ordinateur local. Vous pouvez obtenir la clé d’évaluation de l’emplacement et du stockage nécessaire pour télécharger les données exportées dans l’onglet **exportations** . Pour plus d’informations, consultez la rubrique [Export case Data in Advanced eDiscovery](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Gestion des travaux

Utilisez l’onglet **travaux** pour surveiller les processus de longue durée pour les tâches liées à la casse que vous avez lancées. Les exemples de travaux incluent ceux liés à la réindexation, à la recherche et à l’exportation des données de cas. Par exemple, vous pouvez créer une recherche dans l’onglet **recherches** qui inclut un grand nombre de sources de données. L’état de ce processus de recherche s’affiche sous l’onglet **travaux** . Pour plus d’informations, consultez la rubrique [gestion des travaux dans Advanced eDiscovery](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Configuration des paramètres de cas

Utilisez l’onglet **paramètres** pour configurer les paramètres à l’échelle de l’incident. Cela inclut l’ajout de membres à un cas, la fermeture ou la suppression d’un cas et la configuration du comportement de recherche et d’analyse. Pour plus d’informations, consultez la rubrique [configure case Settings in Advanced eDiscovery](configuring-case-settings-ediscovery20.md).
