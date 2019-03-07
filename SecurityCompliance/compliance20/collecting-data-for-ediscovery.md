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
ms.openlocfilehash: fb4b36841394576c44667f9677507c5655179e45
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455416"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="8fe23-102">Collecter des données pour un cas dans Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="8fe23-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="8fe23-103">Une fois que vous avez identifié les dépositaires et les sources de données intéressantes pour votre cas, il est temps d'identifier l'ensemble des documents dans lesquels vous souhaitez approfondir votre attention.</span><span class="sxs-lookup"><span data-stu-id="8fe23-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="8fe23-104">Vous pouvez utiliser l'outil de recherche dans Advanced eDiscovery (préversion) pour identifier ces derniers dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="8fe23-104">You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="8fe23-105">Une fois que vous avez exécuté une recherche, vous pouvez afficher des statistiques sur les éléments récupérés, tels que les emplacements qui avaient le plus d'éléments correspondant à la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="8fe23-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="8fe23-106">Vous pouvez également afficher un aperçu d'un sous-ensemble des résultats.</span><span class="sxs-lookup"><span data-stu-id="8fe23-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="8fe23-107">Une fois que vous avez identifié l'ensemble des documents que vous souhaitez examiner, vous pouvez ajouter les résultats de la recherche à un jeu de travail à collecter et traiter.</span><span class="sxs-lookup"><span data-stu-id="8fe23-107">When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="8fe23-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="8fe23-108">Create a search</span></span>

<span data-ttu-id="8fe23-109">Cliquez sur **nouvelle recherche** sous l'onglet **recherches** pour démarrer un assistant qui vous guide tout au long de la procédure de création d'une recherche.</span><span class="sxs-lookup"><span data-stu-id="8fe23-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="8fe23-110">Pour plus d'informations sur la création d'une recherche, voir [Create a Search to Collect Data](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="8fe23-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="8fe23-111">Après la création d'une recherche, une page de menu volant contenant des informations s'affiche.</span><span class="sxs-lookup"><span data-stu-id="8fe23-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="8fe23-112">Notez que les **statistiques** et les boutons d' **Aperçu** sont initialement estompés, car la recherche n'est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="8fe23-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="8fe23-113">Vous pouvez suivre la progression de la recherche dans l'onglet **recherches** .</span><span class="sxs-lookup"><span data-stu-id="8fe23-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="8fe23-114">Afficher les statistiques et les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="8fe23-114">View search results and statistics</span></span>
<span data-ttu-id="8fe23-115">Il existe deux composants d'une recherche de contenu: statistiques (estimations) et aperçu.</span><span class="sxs-lookup"><span data-stu-id="8fe23-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="8fe23-116">À mesure que chacun de ces composants est complet, l'état affiché dans les colonnes correspondantes de l'onglet **recherches** passe de \*\*\*\* de à à **en cours** à **terminé**.</span><span class="sxs-lookup"><span data-stu-id="8fe23-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="8fe23-117">Une fois l'estimation de la recherche terminée, cliquez sur la recherche pour afficher la page de menu volant, qui affiche certaines statistiques de haut niveau sur les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="8fe23-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="8fe23-118">À ce stade, le bouton **statistiques** est actif.</span><span class="sxs-lookup"><span data-stu-id="8fe23-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="8fe23-119">Vous pouvez cliquer dessus pour afficher les statistiques de recherche, telles que:</span><span class="sxs-lookup"><span data-stu-id="8fe23-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="8fe23-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="8fe23-120">Summary</span></span>
- <span data-ttu-id="8fe23-121">Emplacements les plus fréquents</span><span class="sxs-lookup"><span data-stu-id="8fe23-121">Top locations</span></span>
- <span data-ttu-id="8fe23-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="8fe23-122">Queries</span></span>

<span data-ttu-id="8fe23-123">Pour plus d'informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="8fe23-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="8fe23-124">Une fois l'aperçu terminé, le bouton **Aperçu** est actif.</span><span class="sxs-lookup"><span data-stu-id="8fe23-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="8fe23-125">Cliquez dessus pour afficher un aperçu d'un sous-ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="8fe23-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="8fe23-126">Ajout de résultats de recherche à un jeu de travail</span><span class="sxs-lookup"><span data-stu-id="8fe23-126">Adding search results to a working set</span></span>

<span data-ttu-id="8fe23-127">Lorsque vous êtes prêt à collecter et à traiter tous les résultats d'une recherche, vous pouvez le faire en l'ajoutant à un jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="8fe23-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set.</span></span> <span data-ttu-id="8fe23-128">Pour plus d'informations, consultez [la rubrique ajouter des données à un jeu de travail](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="8fe23-128">For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 