---
title: Créer des requêtes de recherche
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
ms.openlocfilehash: e62d486b102fa035ae21b379d30bb0657b82acc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242502"
---
# <a name="build-search-queries"></a><span data-ttu-id="cc6b4-102">Créer des requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="cc6b4-102">Build search queries</span></span>

<span data-ttu-id="cc6b4-103">Lors de la création de votre requête, vous pouvez utiliser différents mots clés et conditions pour définir les éléments à rechercher.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="cc6b4-104">Recherches par Mots clés</span><span class="sxs-lookup"><span data-stu-id="cc6b4-104">Keyword searches</span></span>

<span data-ttu-id="cc6b4-105">Tapez une requête de recherche dans la zone **Mots clés** .</span><span class="sxs-lookup"><span data-stu-id="cc6b4-105">Type a search query in **Keywords** box.</span></span> <span data-ttu-id="cc6b4-106">Vous pouvez spécifier des mots clés, des propriétés de message telles que les dates d’envoi et de réception, ou des propriétés de document telles que les noms de fichier ou la date de dernière modification d’un document.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-106">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="cc6b4-107">Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**, **not**et **near**.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-107">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="cc6b4-108">Vous pouvez également rechercher des informations sensibles (telles que des numéros de sécurité sociale) dans des documents ou Rechercher des documents qui ont été partagés en externe.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-108">You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally.</span></span> <span data-ttu-id="cc6b4-109">Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-109">If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="cc6b4-110">Vous pouvez également cliquer sur la case à cocher **afficher la liste de mots clés** et sur tapez un mot clé dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-110">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row.</span></span> <span data-ttu-id="cc6b4-111">Dans ce cas, les mots clés de chaque ligne sont connectés par un opérateur logique ( **c:s**) qui est similaire à la fonctionnalité de l'opérateur **or** de la requête de recherche créée.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-111">If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="cc6b4-112">Pourquoi utiliser la liste de mots clés?</span><span class="sxs-lookup"><span data-stu-id="cc6b4-112">Why use the keyword list?</span></span> <span data-ttu-id="cc6b4-113">Vous pouvez obtenir des statistiques qui indiquent le nombre d'éléments qui correspondent à chaque mot clé.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-113">You can get statistics that show how many items match each keyword.</span></span> <span data-ttu-id="cc6b4-114">Cela peut vous aider à identifier rapidement les mots clés les plus efficaces (et les moins).</span><span class="sxs-lookup"><span data-stu-id="cc6b4-114">This can help you quickly identify which keywords are the most (and least) effective.</span></span> <span data-ttu-id="cc6b4-115">Vous pouvez également utiliser une phrase de mots clés (entourée de parenthèses) dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-115">You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span> <span data-ttu-id="cc6b4-116">Pour plus d'informations sur les statistiques de recherche, consultez la rubrique statistiques de [recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="cc6b4-116">For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="cc6b4-117">Conditions</span><span class="sxs-lookup"><span data-stu-id="cc6b4-117">Conditions</span></span>
    
<span data-ttu-id="cc6b4-118">Vous pouvez ajouter des conditions de recherche pour affiner une recherche et renvoyer un ensemble de résultats plus raffiné.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-118">You can add search conditions to narrow a search and return a more refined set of results.</span></span> <span data-ttu-id="cc6b4-119">Chaque condition ajoute une clause à la requête de recherche créée et exécutée lors du démarrage de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-119">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="cc6b4-120">Une condition est logiquement liée à la requête de mot-clé (spécifiée dans la zone de mot clé) par un opérateur logique (**c:c**) qui est similaire à la fonctionnalité de l'opérateur **and** .</span><span class="sxs-lookup"><span data-stu-id="cc6b4-120">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="cc6b4-121">Cela signifie que les éléments doivent répondre à la fois à la requête de mot clé et à une ou plusieurs conditions à inclure dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-121">That means that items have to satisfy both the keyword query and one or more conditions to be included in the results.</span></span> <span data-ttu-id="cc6b4-122">C’est ainsi que les conditions contribuent à affiner vos résultats.</span><span class="sxs-lookup"><span data-stu-id="cc6b4-122">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="cc6b4-123">Pour obtenir la liste et la description des conditions que vous pouvez utiliser dans une requête de recherche, consultez la section «conditions de recherche» dans [requêtes de mots clés et conditions de recherche pour la recherche de contenu](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="cc6b4-123">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


