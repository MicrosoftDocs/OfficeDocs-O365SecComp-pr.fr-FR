---
title: Analyser les données d’un ensemble de vérification dans Advanced eDiscovery
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
ms.openlocfilehash: c765234e1aa0738415f66f90b66ebce0fcab2505
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527150"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a>Analyser les données d’un ensemble de vérification dans Advanced eDiscovery

Lorsque le nombre de documents collectés est important, il peut s’avérer difficile de les examiner tous. Advanced eDiscovery fournit un certain nombre d’outils pour analyser les documents afin de réduire le volume des documents à examiner sans perte de données et pour vous aider à organiser les documents de manière cohérente. Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants:

- [Détecter des quasi-duplicatas](near-duplicates.md)

- [Threading de messagerie](email-threading.md)

- [Thèmes](themes.md)

Pour analyser les données d’un ensemble de révision:

1. Configurez les paramètres d’analyse pour votre cas. Pour plus d’informations, consultez la rubrique [configurer les paramètres de recherche et d’analyse](configure-search-analytics-settings.md).

2. Ouvrez l’ensemble de révision à analyser.

3. Cliquez sur **gérer le jeu de révision**.

4. Cliquez sur **analyser**.

Vous pouvez vérifier la progression de l’analyse sous l’onglet **tâches** du cas.

 Une fois l’analyse terminée, vous pouvez afficher le rapport d’analyse, exécuter des requêtes dans votre jeu de révisions sur les sorties de l’analyse (voir la rubrique relative à la [recherche dans l’ensemble de révision](review-set-search.md)) et afficher les documents connexes d’un document donné (voir [Review Data in Review Set](reviewing-data-in-review-set.md)).

## <a name="analytics-report"></a>Rapport d’analyse

Pour afficher un rapport d’analyse pour un jeu de révisions:

1. Ouvrez l’ensemble de révision.

2. Cliquez sur **gérer le jeu de révision**.

3. Cliquez sur **rapport**.

L’État comprend quatre composants de l’analyse:

- **Répartition** : le nombre de messages électroniques, de pièces jointes et de documents en vrac a été trouvé dans l’ensemble de révision.

- **Documents (à l’exception des pièces jointes)** : le nombre de documents en vrac était des tableaux croisés dynamiques, des doublons uniques proches d’un tableau croisé dynamique ou un doublon exact d’un autre document.

- **E-mails** : nombre de messages électroniques inclus, copies inclusives, déductions inclusives ou aucun des éléments ci-dessus.

- **Pièces jointes** : le nombre de pièces jointes de courrier électronique sont uniques ou des doublons d’une autre pièce jointe dans l’ensemble de révision.