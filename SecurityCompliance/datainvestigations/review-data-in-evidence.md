---
title: Examiner les données dans les preuves
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
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030072"
---
# <a name="review-data-in-evidence"></a>Examiner les données dans les preuves

**Evidence** est un instantané des résultats de recherche que vous avez collectés. Lorsque vous ajoutez des résultats de recherche à une preuve, un processus est déclenché pour extraire des fichiers, des métadonnées et du texte. Ensuite, le système génère un nouvel index de toutes les données et ajoute des **preuves**. 

Pour tout incident sensible au temps, cela vous permet de rapidement contenir l'environnement en supprimant les données à l'emplacement d'origine lors de l'examen des preuves recréées dans un environnement en quarantaine. Une fois les preuves collectées, vous pouvez passer en revue les différents documents dans leur format natif, format texte ou quasi-natif. En outre, vous pouvez exécuter des requêtes pour affiner les données par plage de temps, types de fichiers, propriétaires de données et de nombreuses autres cartes de condition. À l'aide des cartes de condition auteur/expéditeur/destinataire, vous pouvez rapidement examiner les personnes impliquées dans le renversement et s'il existe des partages externes. Pour plus d'informations, consultez les rubriques suivantes :

  - [InterRoger les données dans les preuves](evidence-query.md)

Pour regrouper des documents et obtenir de l'aide supplémentaire pour votre révision, cliquez sur **gérer les preuves**. Dans la vignette **analyse** , cliquez sur **analyser**. Cette opération exécute des analyses avancées, telles que la détection des doublons, le Threading de messagerie électronique et l'analyse de thème. Par la suite, vous pouvez voir les thèmes généraux des données et organiser les documents par des threads de messagerie, des doublons exacts et des doublons pour faciliter votre examen. Pour plus d'informations, consultez les rubriques suivantes :

  - [Exécuter des analyses pour une analyse plus rapide](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a>Afficher les documents dans les preuves

L'analyse des données (préversion) affiche du contenu via plusieurs visionneuses à des fins différentes. Les différents observateurs peuvent être utilisés en cliquant sur n'importe quel document dans **Evidence**. Les visionneuses actuellement fournies sont les suivantes:

- Métadonnées de fichier
- Affichage natif
- Affichage de texte
- AnNoter l'affichage
- Vue conVertie

## <a name="file-metadata"></a>Métadonnées de fichier

Ce panneau peut être activé/désactivé pour afficher diverses métadonnées associées au document. Bien que la grille des résultats de la recherche puisse être personnalisée pour afficher des métadonnées spécifiques, il peut s'avérer difficile de faire défiler horizontalement les données lors de la révision des données. Le panneau métadonnées de fichier permet à un utilisateur de basculer sur une vue dans la visionneuse.

![Panneau métadonnées de fichier
](../media/Reviewimage2.png)

## <a name="native-view"></a>Affichage natif

La visionneuse Native affiche l'affichage le plus enrichi d'un document. Il prend en charge des centaines de types de fichiers et permet d'afficher l'expérience la plus réelle vers Native possible. Pour les fichiers Microsoft Office, par exemple, la visionneuse exploite Office Online pour afficher du contenu tel que des commentaires de document, des formules Excel, des lignes/colonnes masquées, des notes PowerPoint, etc. Pour plus d'informations sur les visionneuses Office Online, \[reportez-vous à l'article suivant:\]

![Affichage natif
](../media/Reviewimage3.png)

## <a name="text-view"></a>Affichage de texte

La visionneuse de texte fournit une vue du texte extrait d'un fichier. Elle ignore toutes les images incorporées et la mise en forme, mais elle est très performante si un utilisateur tente de comprendre le contenu rapidement. L'affichage de texte comprend également d'autres fonctionnalités:

  - Le compteur de ligne facilite la référence à des parties spécifiques d'un document.

  - Mise en surbrillance des résultats de recherche, qui met en surbrillance les termes dans le document, ainsi que la barre de défilement

  - L'affichage diff fournit un affichage de comparaison qui met en surbrillance les différences textuelles lors de l'affichage des documents en double.

![Affichage de texte
](../media/Reviewimage4.png)

![Vue diff
](../media/Reviewimage5.png)

## <a name="annotate-view"></a>AnNoter l'affichage

L'affichage anNoted propose des fonctionnalités qui permettent aux utilisateurs d'appliquer un balisage à un document lors de l'enquête, notamment:

  - Zone Redactions: les utilisateurs peuvent dessiner un cadre sur le document afin de masquer le contenu sensible

  - Crayon: les utilisateurs peuvent effectuer un dessin à main levée sur un document afin d'attirer l'attention sur certaines parties d'un document.

  - Sélectionner les annotations: les utilisateurs peuvent sélectionner des annotations dans un document afin de les supprimer.

  - Activer/désactiver la transparence des annotations: rend les annotations semi-transparentes afin d'afficher le contenu derrière l'annotation.

  - Page précédente: navigue jusqu'à la page précédente

  - Page suivante: accède à la page suivante.

  - Accéder à la page – l'utilisateur peut entrer un numéro de page spécifique vers lequel naviguer

  - Zoom: définir le niveau de zoom pour l'affichage des annotations

  - Rotation: l'utilisateur peut faire pivoter le document vers la droite

  - Search: l'utilisateur peut effectuer des recherches dans un document et accéder aux différents accès au sein du document.
    
    ![AnNoter l'affichage
    ](../media/Reviewimage1.png)

Notez que ces annotations se trouvent sur les données collectées en tant que preuves, et non à leur emplacement d'origine dans le système actif. 

## <a name="more-information"></a>Plus d’informations

Le tableau suivant répertorie les limites pour les preuves dans les enquêtes de données (aperçu).  Tous les éléments qui dépassent le nombre maximal de fichiers sont affichés en tant qu'erreurs de traitement.
    
  |**Description de la limite**|**Limite**|
  |:-----|:-----|
  |Nombre maximal de collections de preuves  <br/> |50  <br/> |
  |Nombre total de documents pouvant être ingérés dans un cas (pour toutes les collections de preuves de l'enquête)  <br/> |1 million  <br/> |
  |Taille totale des fichiers par charge  <br/> |100 Go  <br/> |
  |Taille maximale d'un fichier unique   <br/> |100 Mo  <br/> |
  |Nombre maximal de caractères extraits à partir d'un seul fichier  <br/> |10 millions  <br/> |
  |Profondeur des éléments incorporés dans un document  <br/> |25  <br/> |
  