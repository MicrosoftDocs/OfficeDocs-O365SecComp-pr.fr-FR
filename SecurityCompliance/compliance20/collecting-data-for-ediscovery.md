---
title: Collecter des données pour un cas de découverte électronique avancée (Preview)
ms.author: esclee
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
ms.openlocfilehash: 11e2c336512c91d65bd046c3022d5375ebecde4a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695050"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="6e442-102">Collecter des données pour un cas de découverte électronique avancée (Preview)</span><span class="sxs-lookup"><span data-stu-id="6e442-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="6e442-p101">Une fois que vous avez identifié dépositaires et sources de données qui présentent un intérêt pour votre cas, il est temps pour identifier l’ensemble de documents pour approfondir. Vous pouvez utiliser l’outil de recherche de découverte électronique avancée (Preview) pour identifier des emplacements garde et non garde dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="6e442-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="6e442-p102">Après avoir exécuté une recherche, vous serez en mesure d’afficher des statistiques sur les éléments récupérés telles que les emplacements qui avait la plupart des éléments qui correspondent à la requête de recherche. Vous pouvez également afficher un aperçu un sous-ensemble des résultats. Lorsque vous avez identifié l’ensemble de documents que vous souhaitez examiner, vous pouvez ajouter les résultats de recherche à une plage de travail pour collecter et traiter.</span><span class="sxs-lookup"><span data-stu-id="6e442-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="6e442-108">Créer une recherche</span><span class="sxs-lookup"><span data-stu-id="6e442-108">Create a search</span></span>

<span data-ttu-id="6e442-p103">Cliquez sur l’onglet **recherches** **nouvelle recherche** démarre un Assistant qui vous guide à travers la création d’une recherche. Pour plus d’informations sur la création d’une recherche, voir [créer une recherche pour recueillir des données](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="6e442-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="6e442-p104">Après la création d’une recherche, une page mobile avec des détails s’affiche. Notez que les boutons de **statistiques** et **Aperçu** initialement grisés, car la recherche n’est pas encore terminée. Vous pouvez conserver le suivi de la progression de la recherche sous l’onglet de **recherche** .</span><span class="sxs-lookup"><span data-stu-id="6e442-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="6e442-114">Afficher les résultats de recherche et des statistiques</span><span class="sxs-lookup"><span data-stu-id="6e442-114">View search results and statistics</span></span>
<span data-ttu-id="6e442-p105">Il existe deux composants d’une recherche de contenu : aperçu et statistiques (estimations). En tant que chacun de ces composants terminées, vous verrez l’état affiché dans les colonnes correspondantes dans l’onglet **recherches** changer de **soumis** **en cours** sur **terminée**.</span><span class="sxs-lookup"><span data-stu-id="6e442-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="6e442-p106">Une fois l’estimation de la recherche est terminée, cliquez sur la recherche pour afficher la page flottant, qui affiche des statistiques de haut niveau sur les résultats de la recherche. À ce stade, le bouton **statistiques** sera actif. Vous pouvez cliquer dessus pour afficher les statistiques de la recherche, tels que :</span><span class="sxs-lookup"><span data-stu-id="6e442-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="6e442-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="6e442-120">Summary</span></span>
- <span data-ttu-id="6e442-121">Emplacements supérieurs</span><span class="sxs-lookup"><span data-stu-id="6e442-121">Top locations</span></span>
- <span data-ttu-id="6e442-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="6e442-122">Queries</span></span>
- <span data-ttu-id="6e442-123">Affinements</span><span class="sxs-lookup"><span data-stu-id="6e442-123">Refiners</span></span>

<span data-ttu-id="6e442-124">Pour plus d’informations sur les statistiques de recherche, voir [les statistiques de recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="6e442-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="6e442-p107">Une fois que l’aperçu est terminé, le bouton **Aperçu** sera actif. Cliquez dessus pour afficher un aperçu d’un sous-ensemble des résultats de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="6e442-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="6e442-127">Ajout des résultats de recherche à une plage de travail</span><span class="sxs-lookup"><span data-stu-id="6e442-127">Adding search results to a working set</span></span>

<span data-ttu-id="6e442-p108">Lorsque vous êtes prêt à collecter et à traiter tous les résultats d’une recherche, vous pouvez le faire en l’ajoutant à un jeu de travail. Pour plus d’informations, voir [Ajouter des données à un jeu de travail](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="6e442-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 