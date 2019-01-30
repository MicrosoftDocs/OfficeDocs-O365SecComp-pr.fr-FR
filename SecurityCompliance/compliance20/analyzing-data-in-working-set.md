---
title: Analyse des données dans un jeu de travail d’eDiscovery avancée (Preview)
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
description: ''
ms.openlocfilehash: a6284204fd709bcf936688f36f38f6b3283b1f98
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607651"
---
# <a name="analyzing-data-in-a-working-set-in-advanced-ediscovery-preview"></a>Analyse des données dans un jeu de travail d’eDiscovery avancée (Preview)

Lorsque le nombre de documents collectées est important, il peut être très difficile passer en revue toutes les. Découverte avancée (Preview) fournit un certain nombre d’outils pour analyser les documents pour réduire le volume de documents à réviser sans perte d’informations et pour vous aider à organiser les documents de manière cohérente. Pour en savoir plus sur ces fonctionnalités, voir :

- [Près de la détection des doublons](near-duplicates.md)
- [Threads de courrier électronique](email-threading.md)
- [Thèmes](themes.md)

Pour analyser des données dans un jeu de travail :

1. Configurer les paramètres analytique pour votre cas. Pour plus d’informations, voir [configurer les paramètres de recherche et analytique](configure-search-analytics-settings.md).
2. Ouvrez le jeu de travail que vous souhaitez analyser.
3. Accédez à « Gérer les jeu de travail ».
4. Cliquez sur « Analyser ».

Vous pouvez vérifier la progression de l’analyse dans l’onglet tâches dans votre cas.

 Une fois l’analyse terminée, vous pouvez afficher le rapport analytique, les requêtes exécutées au sein de votre travail sur les sorties de l’analyse (pour plus d’informations, voir [requête au sein de votre travail définie](working-set-search.md)) et consultez les documents associés d’un document donné (pour plus d’informations, voir [ Examen des données dans le jeu de travail](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>Rapport Analytique

Pour afficher un rapport analytique pour votre jeu de travail :

1. Ouvrez votre jeu de travail.
2. Accédez à « Gérer les jeu de travail ».
3. Cliquez sur « Report ».

Le rapport comporte quatre composants d’analyse :

- **Répartition** - combien les messages électroniques, pièces jointes et des documents libres ont été trouvées dans le jeu de travail.

- **Documents (à l’exclusion des pièces jointes)** - nombre de documents libre ont été tableaux croisés dynamiques, uniques près de doublons du tableau croisé dynamique ou un doublon exact d’un autre document.

- **Messages électroniques** - combien de messages ont été inclusives, copies inclus, des inconvénients inclus ou aucun d'entre eux.

- **Pièces jointes** - nombre de pièces jointes ont été uniques ou d’une pièce jointe autre adresse e-mail dans le jeu de travail les doublons.