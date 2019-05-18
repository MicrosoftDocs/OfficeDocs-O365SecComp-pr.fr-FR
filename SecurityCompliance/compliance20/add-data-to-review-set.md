---
title: Ajouter des résultats de recherche à un jeu à réviser
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
description: ''
ms.openlocfilehash: 4de390972672509422e055cd3fd6a9f65d54a7ba
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155236"
---
# <a name="add-search-results-to-a-review-set"></a>Ajouter des résultats de recherche à un jeu à réviser

Lorsque vous êtes satisfait des résultats d’une recherche et que vous êtes prêt à passer en revue et à analyser ces résultats de recherche, vous pouvez les ajouter à un jeu de révision dans le cas. La copie des données d’origine dans l’ensemble de révision facilite également le processus de révision et d’analyse en vous fournissant des outils d’analyse avancés, tels que la détection de thèmes, la détection de proximité et l’identification des threads de messagerie. Vous pouvez également ajouter des données provenant de sources de données autres que Office 365 à un jeu de réexamen afin que vous puissiez examiner ces données en plus des données que vous collectez à partir d’Office 365.

Lorsque vous ajoutez les résultats d’une recherche à un jeu de réviseurs (les ensembles de vérification se trouvent sous l’onglet **ensembles de vérification** du cas), les deux événements suivants se produisent:

- Tous les éléments dans les résultats de la recherche sont copiés à partir de la source de données d’origine dans les services Live Office 365 et copiés dans un emplacement de stockage Azure sécurisé dans le Cloud Microsoft.

- Tous les éléments (y compris le contenu et les métadonnées) sont réindexés de sorte que toutes les données du jeu de révision soient entièrement utilisables lors de la révision des données de cas. La réindexation des données permet d’effectuer des recherches complètes et très rapides lorsque vous recherchez des données dans l’ensemble de vérifications lors de l’enquête de cas.

Pour ajouter des données à un jeu de réexamens, cliquez sur une recherche dans l’onglet **recherches** , puis cliquez sur **Ajouter des résultats à examiner le jeu** sur la page de menu volant.

![Ajout de données à un ensemble de révision](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

Notez que vous pouvez ajouter à un jeu de réexamen existant ou créer un jeu de révision.  Si vous ajoutez à un nouveau jeu de réexamen, spécifiez son nom, puis cliquez sur **Ajouter**.

![Sélectionner un jeu de révision](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

L’ajout de données à un jeu de révision est un processus long. Ce processus inclut la collecte d’éléments à partir des sources de données d’origine dans Office 365 (par exemple, à partir de boîtes aux lettres et de sites), leur copie vers l’emplacement ** de stockage Azure (ce processus de copie est également appelé «ingestion»), puis la réindexation des éléments. Vous pouvez suivre la progression sous l’onglet **travaux** ou sur l’onglet **recherches** en surveillant l’État dans la colonne **données ajoutées à l’ensemble** de modifications. Une fois le traitement de l’ensemble de vérifications terminé, cliquez sur l’onglet **ensembles** de vérifications dans le cas, puis cliquez sur le jeu de révision pour démarrer le processus de filtrage, d’examen, de marquage et d’exportation des données dans l’ensemble de révision.

## <a name="add-a-sample-to-a-review-set"></a>Ajouter un échantillon à un jeu de révision

Si vous souhaitez valider les résultats d’une recherche plus en détail avant de les ajouter à un jeu de révision, vous pouvez ajouter un échantillon des résultats de la recherche à un jeu de révision au lieu d’ajouter tout.

Pour ajouter un exemple à un jeu de réexamens, cliquez sur une recherche sous l’onglet **recherches** et cliquez sur **exemple** sur la page de la fenêtre volante. Sur la page **paramètres d’échantillonnage** , choisissez l’une des options suivantes:

- **Niveau de confiance%** et **intervalle de confiance%** : les éléments ajoutés au jeu de révision sont déterminés par les paramètres statistiques que vous définissez. Si vous utilisez généralement un niveau de confiance et un intervalle lors de l’échantillonnage des résultats, spécifiez-les dans les zones de liste déroulante. Dans le cas contraire, utilisez les paramètres par défaut.

- **Échantillon aléatoire%** : les éléments ajoutés au jeu de révision sont basés sur une sélection aléatoire du pourcentage spécifié du nombre total d’éléments renvoyés par la recherche.

Après avoir sélectionné et configuré l’une des options précédentes, sélectionnez un jeu de révision existant auquel ajouter l’exemple, puis cliquez sur **Envoyer**. Une fois encore, vous pouvez suivre l’avancement sous l’onglet **travaux** ou sur l’onglet **recherches** en surveillant l’État dans la colonne **données ajoutées à l’ensemble** de modifications.