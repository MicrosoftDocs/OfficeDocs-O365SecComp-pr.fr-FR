---
title: Exécuter les données d’analyse pour investiguer plus rapidement
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
ms.openlocfilehash: 9516035fb6c758fdff1852249fff2815f19af559
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257612"
---
# <a name="run-analytics-to-investigate-faster"></a>Exécuter les données d’analyse pour investiguer plus rapidement

Lorsqu'une collection de preuves est volumineuse, il peut s'avérer difficile de les examiner tous. Un ensemble de preuves inclut souvent plusieurs copies de messages ou de documents de courrier identiques ou similaires. Les enquêtes de données (préversion) fournissent un certain nombre d'outils d'analyse qui peuvent vous aider à réduire le volume des documents qui doivent être analysés sans aucune perte de données. Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants:

- [Détecter des quasi-duplicatas](near-duplicates.md)

- [Threading de messagerie](email-threading.md)

- [Thèmes](themes.md)

Pour analyser les données d'un ensemble de preuves:

1. ConFigurez les paramètres d'analyse pour votre enquête. Pour plus d'informations, consultez la rubrique [configurer les paramètres de recherche et d'analyse](configure-search-analytics-settings.md).

2. Ouvrez l'ensemble de preuves.

3. Cliquez sur **gérer les preuves**.

4. Sous **analyse**, cliquez sur **analyser**.

Vous pouvez vérifier la progression de l'analyse dans l'onglet **travaux** de votre enquête. Le type de travail déclenché est nommé **analyse en cours d'exécution**.

 Une fois l'analyse terminée, vous pouvez afficher la liste des doublons ou des doublons exacts du document que vous examinez dans le volet droit. Pour sélectionner tous les doublons du document que vous affichez, vous pouvez facilement le faire à l'aide de ce panneau. Pour en savoir plus sur les autres fonctionnalités de ce panneau, voir [examiner les données dans les preuves](review-data-in-evidence.md). 

Vous pouvez également exécuter des requêtes supplémentaires dans votre preuve à l'aide des sorties de l'analyse comme themes. Pour plus d'informations, consultez [la rubrique Query the Data in Evidence](evidence-query.md).

## <a name="analytics-report"></a>Rapport d'analyse

Pour afficher un rapport d'analyse pour vos preuves:

1. Ouvrez l'ensemble de preuves.

2. Cliquez sur **gérer les preuves**.

3. Sous **analyse**, cliquez sur **afficher le rapport**.

L'État comprend quatre composants de l'analyse:

- **Répartition** : nombre de messages électroniques bruts, de pièces jointes et de documents trouvés dans l'ensemble de preuves.

- **E-mails** : nombre de messages eamil inclusifs, inclusifs, moins de copies inclusives ou aucun des éléments ci-dessus.
   - InClusif: dernier message dans le thread de courrier électronique qui contient l'historique précédent et nécessite une révision.
   - InClusif: le message dans le fil de discussion qui contient une ou plusieurs pièces jointes qui doivent être réexaminées.
   - Copies inclusives: message qui est une copie d'un autre message moins inclusive ou inclusif (Subject and Body).

- **Pièces jointes** : nombre de pièces jointes qui sont uniques ou des doublons d'une autre pièce jointe dans la même preuve.

- **Documents (à l'exception des pièces jointes)** : le nombre de documents uniques qui nécessitent une révision, par exemple, le document le plus représentatif de l'ensemble presque dupliqué ou un doublon exact d'un autre document).