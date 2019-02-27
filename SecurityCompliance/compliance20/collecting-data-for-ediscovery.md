---
title: Collecter des données pour un cas dans Advanced eDiscovery (aperçu)
ms.author: esclee
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
ms.openlocfilehash: bcc307cc08954dd3cc69e8905747393d79f97b04
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297097"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="f5f16-102">Collecter des données pour un cas dans Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="f5f16-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="f5f16-p101">Une fois que vous avez identifié les dépositaires et les sources de données intéressantes pour votre cas, il est temps d'identifier l'ensemble des documents dans lesquels vous souhaitez approfondir votre attention. Vous pouvez utiliser l'outil de recherche dans Advanced eDiscovery (préversion) pour identifier ces derniers dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f5f16-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="f5f16-p102">Une fois que vous avez exécuté une recherche, vous pouvez afficher des statistiques sur les éléments récupérés, tels que les emplacements qui avaient le plus d'éléments correspondant à la requête de recherche. Vous pouvez également afficher un aperçu d'un sous-ensemble des résultats. Une fois que vous avez identifié l'ensemble des documents que vous souhaitez examiner, vous pouvez ajouter les résultats de la recherche à un jeu de travail à collecter et traiter.</span><span class="sxs-lookup"><span data-stu-id="f5f16-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="f5f16-108">Créer une recherche</span><span class="sxs-lookup"><span data-stu-id="f5f16-108">Create a search</span></span>

<span data-ttu-id="f5f16-p103">Cliquez sur **nouvelle recherche** sous l'onglet **recherches** pour démarrer un assistant qui vous guide tout au long de la procédure de création d'une recherche. Pour plus d'informations sur la création d'une recherche, voir [Create a Search to Collect Data](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="f5f16-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="f5f16-p104">Après la création d'une recherche, une page de menu volant contenant des informations s'affiche. Notez que les **statistiques** et les boutons d' **Aperçu** sont initialement estompés, car la recherche n'est pas encore terminée. Vous pouvez suivre la progression de la recherche dans l'onglet **recherches** .</span><span class="sxs-lookup"><span data-stu-id="f5f16-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="f5f16-114">Afficher les statistiques et les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="f5f16-114">View search results and statistics</span></span>
<span data-ttu-id="f5f16-p105">Il existe deux composants d'une recherche de contenu: statistiques (estimations) et aperçu. À mesure que chacun de ces composants est complet, l'état affiché dans les colonnes correspondantes de l'onglet **recherches** passe de \*\*\*\* de à à **en cours** à **terminé**.</span><span class="sxs-lookup"><span data-stu-id="f5f16-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="f5f16-p106">Une fois l'estimation de la recherche terminée, cliquez sur la recherche pour afficher la page de menu volant, qui affiche certaines statistiques de haut niveau sur les résultats de la recherche. À ce stade, le bouton **statistiques** est actif. Vous pouvez cliquer dessus pour afficher les statistiques de recherche, telles que:</span><span class="sxs-lookup"><span data-stu-id="f5f16-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="f5f16-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="f5f16-120">Summary</span></span>
- <span data-ttu-id="f5f16-121">Emplacements les plus fréquents</span><span class="sxs-lookup"><span data-stu-id="f5f16-121">Top locations</span></span>
- <span data-ttu-id="f5f16-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="f5f16-122">Queries</span></span>
- <span data-ttu-id="f5f16-123">Affinements</span><span class="sxs-lookup"><span data-stu-id="f5f16-123">Refiners</span></span>

<span data-ttu-id="f5f16-124">Pour plus d'informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="f5f16-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="f5f16-p107">Une fois l'aperçu terminé, le bouton **Aperçu** est actif. Cliquez dessus pour afficher un aperçu d'un sous-ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="f5f16-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="f5f16-127">Ajout de résultats de recherche à un jeu de travail</span><span class="sxs-lookup"><span data-stu-id="f5f16-127">Adding search results to a working set</span></span>

<span data-ttu-id="f5f16-p108">Lorsque vous êtes prêt à collecter et à traiter tous les résultats d'une recherche, vous pouvez le faire en l'ajoutant à un jeu de travail. Pour plus d'informations, consultez [la rubrique ajouter des données à un jeu de travail](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="f5f16-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 