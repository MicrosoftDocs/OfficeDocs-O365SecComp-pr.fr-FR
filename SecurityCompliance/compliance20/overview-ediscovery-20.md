---
title: Vue d’ensemble d’eDiscovery avancée (Preview) dans Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article décrit la nouvelle version de découverte avancée (Preview) dans Microsoft 365.
ms.openlocfilehash: aed4739db02ffda83319ada5b1c5fdf20426a1fa
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607661"
---
# <a name="overview-of-advanced-ediscovery-preview-in-microsoft-365"></a>Vue d’ensemble d’eDiscovery avancée (Preview) dans Microsoft 365

Microsoft a publié simplement une version d’évaluation de l’outil de découverte électronique avancé mis à jour qui s’appuie sur les fonctionnalités de découverte électronique existant dans Office 365. Cette version d’évaluation, appelée *eDiscovery avancée (Preview)*, fournit un flux de travail de bout en bout pour conserver les collecter, passez en revue, analyser et exporter du contenu qui répond aux enquêtes internes et externes de votre organisation. 

## <a name="alignment-with-edrm"></a>Alignement avec EDRM

Le flux de travail intégré d’eDiscovery avancée (Preview) s’aligne sur le processus de découverte électronique indiqué par le modèle de référence découverte électronique (EDRM). 

![Le modèle de référence de la découverte électronique (EDRM)](../media/EDRMv1.png)

(Source de l’image avec l’autorisation edrm.net. L’image source a été effectuée disponible sous Creative Commons Attribution 3.0 Unported licence.)

À un niveau élevé, eDiscovery comment avancées Voici (Preview) prend en charge le flux de travail EDRM :

- **Identification** - après avoir identifié les personnes potentiels d’intérêt dans une enquête, vous pouvez les ajouter en tant que dépositaires (également appelés *dépositaires de données*, car ils peuvent posséder des informations relatives à l’enquête) à un avancé cas de découverte électronique (Preview). Une fois que les utilisateurs sont ajoutés en tant que dépositaires, il est facile de conserver, collecter et passez en revue les documents dépositaire.

- **Conservation** - pour conserver et protéger les données qui s’appliquent à une enquête, avancé eDiscovery (Preview) vous permet de que positionner une conservation légale sur les sources de données qui sont associées aux dépositaires dans un cas. Vous pouvez également placer les données non garde en attente. En outre, eDiscovery avancée (Preview) a un flux de travail intégrés communications afin de pouvoir envoyer une conservation légale des notifications à dépositaires et suivre leurs accusés de réception.

- **Collection** - après avoir identifié (et conservés) les sources de données relatives à l’enquête, vous pouvez utiliser l’outil de recherche intégrées dans eDiscovery avancées (Preview) et de collecte de données live à partir de sources de données garde (et non garde sources de données, le cas échéant) qui peuvent être pertinentes à la casse.

- **Traitement** - une fois que vous avez collecté toutes les données relatives à la casse, l’étape suivante est traiter à l’analyse et passer en revue les autres. D’eDiscovery avancée (Preview), cela signifie les données sur place que vous avez identifié dans la phase de collecte sont copiées dans l’emplacement de stockage Azure (appelé un *jeu de travail*), qui fournit une vue statique des données des cases. 
 
- Jeu de **révision** - une fois que les données ont été ajoutées à une travail, vous pouvez afficher des documents spécifiques et exécuter des requêtes supplémentaires à  
 
- **Analyse** - avancée de découverte électronique (Preview) fournit des outils analytique intégré qui vous aideront à éliminez les données à partir de la plage de travail que vous déterminez n’est pas en rapport avec l’investigation. En plus de réduire le volume des données pertinentes, eDiscovery avance (Preview) vous permet également de réduire les coûts de révision légale en vous permettant d’organiser le contenu pour faciliter le processus de révision et plus efficace.

- **Production** et **présentation** - lorsque vous êtes prêt, vous pouvez exporter des documents à partir d’un jeu de travail de révision légale. Vous pouvez exporter des documents dans leur format natif ou dans un format spécifié par EDRM afin qu’ils peuvent être importés dans les applications de passer en revue les tiers.

## <a name="advanced-ediscovery-preview-workflow"></a>Flux de travail eDiscovery avancées (Preview)

Les sections suivantes décrivent chaque étape dans le flux de travail intégré d’eDiscovery avancée (Preview). La capture d’écran suivante montre l’onglet **accueil** d’un dossier nommé *2019002 de responsabilité du produit*. Notez que les onglets de flux de travail dans la partie supérieure de la page de séquence pour aligner le processus EDRM. 

Pour plus d’informations sur le flux de travail de bout en bout d’eDiscovery avancée (Preview), voir ce [Mécanisme Microsoft vidéo](https://go.microsoft.com/fwlink/?linkid=2066133). 

![Onglets de découverte électronique avancée (Preview) suivent le flux de travail EDRM](../media/aedisco-homepage-1.png)

## <a name="managing-custodians"></a>Gestion des dépositaires

Pour ajouter et gérer les personnes que vous avez identifié en tant que personnes dignes d’intérêt dans ce cas, utilisez l’onglet **dépositaires** . Lorsque vous ajoutez dépositaires, vous pouvez effectuer les actions liées aux dépositaires telles que l’émission d’une procédure juridique dépositaire sources de données, telles que leur boîte aux lettres et le compte OneDrive, rapidement communiquer avec dépositaires et sources de données dépositaire pour recueillir le contenu de recherche qui s’applique à la casse. En tant que la progression d’un dossier, il est facile à ajouter nouveau dépositaires ou la dernière version dépositaires du cas. Pour plus d’informations, voir [utilisation des dépositaires d’eDiscovery avancée (Preview)](managing-custodians.md).

## <a name="managing-legal-hold-notifications"></a>Gestion des notifications de conservation légale

Pour gérer le processus de communication avec les dépositaires dans ce cas, utilisez l’onglet **Communications** . Un avis de conservation légale indique dépositaires pour conserver tout contenu qui peut-être être pertinente à la casse. Les équipes juridiques doivent être en mesure d’effectuer le suivi des notifications ont été reçues, lisez et reconnues par dépositaires. Le flux de travail de communications d’eDiscovery avancée (Preview) vous permet de créez et envoyez des notifications initiales, rappels, version notifications et escalades si dépositaires échouent de reconnaître une notification de suspension. Pour plus d’informations, voir [utilisation de communications d’eDiscovery avancée (Preview)](managing-custodian-communications.md).

## <a name="managing-content-preservation"></a>Gestion des archives de contenu

Lorsque vous ajoutez un dépositaire à un cas, vous avez la possibilité de placer un blocage sur des données garde. Utilisez l’onglet **contient** pour gérer la suspension créée lorsque vous ajoutez dépositaires et gérer juridique supplémentaire conserve associé à la casse ; par exemple, vous pouvez identifier et placer une suspension sur des sources de données non garde. Vous pouvez également modifier tout blocage dans le cas et rendre une suspension basée sur une requête afin qu’uniquement le contenu qui correspond à la requête est mis en attente ; par exemple, vous pouvez ajouter une plage de dates à la suspension afin que seul le contenu qui a été créé au sein d’une date spécifique dans la plage de conservé. Vous pouvez également obtenir les statistiques sur le contenu qui est en attente, supprimer la suspension après lorsqu’il n’est plus pertinent pour le cas ou le supprimer. Pour plus d’informations, voir [Gestion des suspensions d’eDiscovery avancée (Preview)](managing-holds.md).

## <a name="indexing-custodian-data"></a>L’indexation de données dépositaire

Lorsque vous ajoutez un dépositaire et les sources de données garde correspondant à un cas, n’importe quel élément partiellement indexée à partir d’une source de données dépositaire est indexée à nouveau (par un processus appelé *indexation avancée*). Ainsi, contenu garde comme les images, les types de fichiers non pris en charge et tout autre contenu potentiellement non indexé être entièrement recherché lorsque vous exécutez des recherches pour recueillir des données relatives à la casse. Utilisez l’onglet **de traitement** pour surveiller l’état d’indexation avancée et de correction de traitement des erreurs (à l’aide d’un AV de processus *correction d’erreur*). Pour plus d’informations, voir [fixation de traitement des erreurs d’eDiscovery avancée (Preview)](processing-data-for-case.md).

## <a name="collecting-case-data"></a>Collecte de données de dossiers

Utilisez l’onglet de **recherche** pour créer des recherches à la place garde de recherche et les sources de données non garde dans Office 365 pour le contenu correspondant à la casse. Vous pouvez créer et lancer des recherches basée sur une requête (à l’aide de mots clés et des conditions) pour identifier un ensemble les messages électroniques et les documents qui sont pertinents pour le cas et que vous souhaitent davantage de révision et d’analyser dans les étapes suivantes dans le flux de travail eDiscovery. Vous pouvez créer une ou plusieurs recherches associées à la casse. En outre, vous pouvez utiliser l’outil de recherche pour afficher un aperçu des exemples de documents et afficher les statistiques de recherche qui peuvent aider à affiner et améliorent les résultats de recherche. Une fois que vous êtes satisfait que les résultats de recherche contiennent toutes les données sont pertinentes pour le cas, vous ajoutez les résultats de recherche à une plage de travail pour l’examen, analyse et si nécessaire, l’élimination. Pour plus d’informations, voir la [collecte de données pour un cas de découverte électronique avancée (Preview)](collecting-data-for-ediscovery.md).

## <a name="reviewing-and-analyzig-case-data"></a>Révision et analyzig des données de cas

Utilisez l’onglet **jeux de travail** , ou passez en revue et analyser le contenu que vous avez collectées à partir du système live et ajouté à une plage de travail. Un *jeu de travail* est une collection statique (en d’autres termes, une copie en mode hors connexion de données) de données garde (et le cas échéant, les données non garde) que vous avez collectées dans la phase précédente du flux de travail eDiscovery. Lorsque vous ajoutez des résultats de la recherche à une plage de travail, qui extrait les fichiers de conteneurs, extrait les métadonnées et extrait le texte est déclenché par un processus. Lorsque ce processus est terminé, le système crée un nouvel index de toutes les données collectées à partir de dépositaires et ajouté à la plage de travail. Une fois que les données sont ajoutées à la plage de travail, vous pouvez exécuter des requêtes supplémentaires pour limiter les données des dossiers, afficher les données sous forme de texte ou dans le format de fichier natif et annoter, procéder et définir de baliser les documents dans le travail. En outre, vous pouvez effectuer analytique avancés tels qu’identifier la duplication des documents, de thread de messagerie et les thèmes. Une fois que vous avez éliminées les données à celles qui sont pertinents pour le cas, vous pouvez télécharger des documents de téléchargement directement ou les exporter ainsi que toutes les balises, les annotations et les métadonnées de fichier. Pour plus d’informations, voir :

  - [Examen des données de cas d’eDiscovery avancée (Preview)](reviewing-data-in-working-set.md)
  - [Analyse des données dans un jeu de travail d’eDiscovery avancée (Preview)](analyzing-data-in-working-set.md)

## <a name="exporting-data-for-review-and-presentation"></a>Exportation des données de révision et de présentation

Après avoir exporté les données à partir d’un jeu de travail, utilisez l’onglet **exporte** pour gérer une tâche d’exportation et de télécharger des données à partir d’un jeu de travail. Lorsque vous exportez un jeu de travail, les données sont téléchargées vers un emplacement de stockage Azure et puis ne sont disponibles pour être téléchargé sur un ordinateur local. Vous pouvez obtenir l’emplacement et évaluer le stockage nécessaire pour télécharger les données exportées sous l’onglet **exporte** la clé. Pour plus d’informations, voir [exportation de données de dossiers d’eDiscovery avancée (Preview)](exporting-data-ediscover20.md).

## <a name="managing-jobs"></a>Gestion des travaux

Utilisez l’onglet **tâches** pour surveiller les processus de longue durée pour les tâches liées à la casse que vous avez lancé, recherches en tant que la réindexation, recherches et exportations. Par exemple, vous pouvez créer une nouvelle recherche sur l’onglet de **recherche** qui inclut un grand nombre de sources de données. L’état de ce processus de recherche s’affiche dans l’onglet **tâches** . Pour plus d’informations, voir [Gestion des travaux d’eDiscovery avancée (Preview)](managing-jobs-ediscovery20.md).

## <a name="configuring-case-settings"></a>Configuration des paramètres de la cas

Utilisez l’onglet **paramètres** pour configurer les paramètres de l’incident. Cela inclut l’ajout de membres à un incident, clôture ou suppression d’un cas et la configuration de recherche et analytique le comportement. Pour plus d’informations, consultez [Configuration des paramètres cas d’eDiscovery avancée (Preview)](configuring-case-settings-ediscovery20.md).

