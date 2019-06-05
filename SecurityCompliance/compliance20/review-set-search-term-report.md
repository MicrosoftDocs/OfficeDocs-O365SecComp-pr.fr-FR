---
title: Générer un rapport de termes de recherche pour un jeu de révision
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 877c0017359ab9193c4cae81cbef4240909053a8
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34714993"
---
# <a name="generate-search-term-report-for-a-review-set"></a>Générer un rapport de termes de recherche pour un jeu de révision

Dans eDiscovery, l’une des conditions les plus fréquemment utilisées pour demander des documents consiste à utiliser des termes de recherche par mot clé. En identifiant les documents qui contiennent les mots clés spécifiques (également appelés *termes*) qui sont importants pour un cas, les réviseurs peuvent commencer à comprendre ce qu’ils font face. Dans Advanced eDiscovery dans Microsoft 365, vous pouvez le faire précisément en générant des rapports de termes de recherche sur les requêtes sauvegardées au sein d’un ensemble de révision.

## <a name="step-1-create-a-saved-query-in-the-review-set"></a>Étape 1: créer une requête enregistrée dans l’ensemble de révision

Pour générer un rapport de termes de recherche pertinent, créez une requête enregistrée qui définit l’ensemble des documents dans l’ensemble de révision pour lequel vous souhaitez générer un rapport de termes de recherche. Par exemple, vous pouvez utiliser une plage de dates ou le jeu de termes de recherche réel (à l’aide de la carte de condition de mots-clés) pour créer la requête. Pour en savoir plus sur les requêtes Set de révision, consultez [la rubrique Query the Data in a Review Set](review-set-search.md).

## <a name="step-2-generate-a-search-term-report"></a>Étape 2: générer un rapport de termes de recherche

Il existe deux façons de générer un rapport de termes de recherche: via le menu contextuel de la requête enregistrée que vous avez créée à l’étape 1, ou via la console de gestion des rapports sur les termes de la recherche.

- Pour utiliser le menu contextuel, ouvrez le menu contextuel de la requête enregistrée que vous avez créée à l’étape 1, puis cliquez sur **générer un rapport de termes de recherche**.

- Pour utiliser la console de gestion, accédez à **Manage Review set > view search term**Reports, cliquez sur **New**, puis sélectionnez la requête enregistrée que vous avez créée à l’étape 1.

Ensuite, entrez les termes sur lesquels vous souhaitez créer un rapport, séparés par des sauts de ligne; Si la requête enregistrée que vous avez créée à l’étape 1 condition de mot-clé utilisée, la page de menu volant est pré-renseignée avec les termes de la première carte de condition de mot clé utilisée dans la requête enregistrée.

Ensuite, sélectionnez jusqu’à trois tableaux croisés dynamiques à afficher, puis cliquez sur **générer**pour démarrer le travail de génération de l’état de la recherche.

### <a name="what-is-a-pivot"></a>Qu’est-ce qu’un tableau croisé dynamique?

Les tableaux croisés dynamiques indiquent comment le rapport sera organisé. Prenons l’exemple suivant.

- La requête enregistrée extrait 10 documents: Doc1 à Doc10.

- Doc1, Doc2, Doc3, doc4, Doc5, Doc6 et Doc7 contiennent le terme «eDiscovery».

- Doc6, Doc7, Doc8, Doc9 et Doc10 contiennent le terme «enquête».

- Doc1, Doc3, Doc5, Doc7, Doc9 proviennent du dépositaire A.

- Doc2, doc4, Doc6, Doc8, Doc10 proviennent du dépositaire B.

Dans ce cas, si vous générez un rapport de terme de recherche sur les termes «eDiscovery» et «investigation» et pivot sur les dépositaires, l’état de terme de recherche serait organisé comme suit:

- «eDiscovery»-dépositaire A: 4 documents

- «eDiscovery»-dépositaire B: 3 documents

- "Enquête"-dépositaire A: 2 documents

- "Enquête": dépositaire B: 3 documents

## <a name="step-3-download-report"></a>Étape 3: Télécharger le rapport

Dans la console de gestion des termes de recherche, vous pouvez suivre l’état d’une tâche de rapport de termes de recherche précédemment créée. Une fois le travail terminé, vous pouvez cliquer sur la ligne de l’état de terme de recherche et cliquer sur «Télécharger» pour télécharger l’état de terme de recherche dans un format CSV. Il y aura une ligne par (terme de recherche, tableaux croisés dynamiques) tuple, et chaque ligne contiendra les informations suivantes:

- Combien de documents ont été extraits?

- Combien de fois le terme de recherche a-t-il été trouvé dans les documents?

- Quel est le volume total des documents extraits?

- Combien de familles ont été récupérées?

- Quel est le nombre total de documents de ces familles, y compris les documents qui n’ont pas le terme de recherche?

- Quel est le volume total de ce qui précède?