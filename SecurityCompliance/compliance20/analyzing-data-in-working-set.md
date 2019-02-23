---
title: Analyser les données d'une plage de travail dans Advanced eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ae024f423ac9b4ab9210ddfab519093a9fee3e42
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216794"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a>Analyser les données d'une plage de travail dans Advanced eDiscovery (aperçu)

Lorsque le nombre de documents collectés est important, il peut s'avérer difficile de les examiner tous. Advanced eDiscovery (aperçu) fournit un certain nombre d'outils pour analyser les documents afin de réduire le volume des documents à examiner sans perte d'informations et pour vous aider à organiser les documents de manière cohérente. Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants:

- [Détecter des quasi-duplicatas](near-duplicates.md)
- [Threading de messagerie](email-threading.md)
- [Thèmes](themes.md)

Pour analyser les données d'une plage de travail:

1. ConFigurez les paramètres d'analyse pour votre cas. Pour plus d'informations, consultez la rubrique [configurer les paramètres de recherche et d'analyse](configure-search-analytics-settings.md).
2. Ouvrez le jeu de travail que vous souhaitez analyser.
3. Accédez à «gérer le jeu de travail».
4. Cliquez sur «analyser».

Vous pouvez vérifier la progression de l'analyse dans l'onglet travaux de votre cas.

 Une fois l'analyse terminée, vous pouvez afficher le rapport d'analyse, exécuter des requêtes dans votre jeu de travail sur les sorties de l'analyse (pour plus d'informations, consultez [la rubrique Query dans votre jeu de travail](working-set-search.md)) et afficher les documents connexes d'un document donné (pour plus d'informations, consultez la rubrique [ Examen des données dans le jeu de travail](reviewing-data-in-working-set.md)).

## <a name="analytics-report"></a>Rapport d'analyse

Pour afficher un rapport d'analyse pour votre jeu de travail:

1. Ouvrez votre jeu de travail.
2. Accédez à «gérer le jeu de travail».
3. Cliquez sur «État».

L'État comprend quatre composants de l'analyse:

- **Répartition** : le nombre de messages électroniques, de pièces jointes et de documents en vrac a été trouvé dans le jeu de travail.

- **Documents (à l'exception des pièces jointes)** : le nombre de documents en vrac était des tableaux croisés dynamiques, des doublons uniques proches d'un tableau croisé dynamique ou un doublon exact d'un autre document.

- **E-mails** : nombre de messages électroniques inclusifs, copies inclusives, déductions inclusives ou aucun des éléments ci-dessus.

- **Pièces jointes** : nombre de pièces jointes uniques ou en double d'une pièce jointe différente dans la plage de travail.