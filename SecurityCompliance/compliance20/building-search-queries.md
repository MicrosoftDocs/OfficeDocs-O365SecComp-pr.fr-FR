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
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296217"
---
# <a name="build-search-queries"></a><span data-ttu-id="1da39-102">Créer des requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="1da39-102">Build search queries</span></span>

<span data-ttu-id="1da39-103">Lors de la création de votre requête, vous pouvez utiliser différents mots clés et conditions pour définir les éléments à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1da39-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="1da39-104">Recherches par Mots clés</span><span class="sxs-lookup"><span data-stu-id="1da39-104">Keyword searches</span></span>

<span data-ttu-id="1da39-p101">Tapez une requête de recherche dans la zone **Mots clés** . Vous pouvez spécifier des mots clés, des propriétés de message, telles que des dates d'envoi et de réception, ou des propriétés de document, telles que des noms de fichiers ou la date de la dernière modification d'un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**, **not**et **near**. Vous pouvez également rechercher des informations sensibles (telles que des numéros de sécurité sociale) dans des documents ou Rechercher des documents qui ont été partagés en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="1da39-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="1da39-p102">Vous pouvez également cliquer sur la case à cocher **afficher la liste de mots clés** et sur tapez un mot clé dans chaque ligne. Dans ce cas, les mots clés de chaque ligne sont connectés par un opérateur logique ( **c:s**) qui est similaire à la fonctionnalité de l'opérateur **or** de la requête de recherche créée.</span><span class="sxs-lookup"><span data-stu-id="1da39-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="1da39-p103">Pourquoi utiliser la liste de mots clés? Vous pouvez obtenir des statistiques qui indiquent le nombre d'éléments qui correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés les plus efficaces (et les moins). Vous pouvez également utiliser une phrase de mots clés (entourée de parenthèses) dans une ligne. Pour plus d'informations sur les statistiques de recherche, consultez la rubrique statistiques de [recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="1da39-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="1da39-117">Conditions</span><span class="sxs-lookup"><span data-stu-id="1da39-117">Conditions</span></span>
    
<span data-ttu-id="1da39-p104">Vous pouvez ajouter des conditions de recherche pour affiner une recherche et renvoyer un ensemble de résultats plus raffiné. Chaque condition ajoute une clause à la requête de recherche créée et exécutée lors du démarrage de la recherche. Une condition est logiquement liée à la requête de mot-clé (spécifiée dans la zone de mot clé) par un opérateur logique (**c:c**) qui est similaire à la fonctionnalité de l'opérateur **and** . Cela signifie que les éléments doivent répondre à la fois à la requête de mot clé et à une ou plusieurs conditions à inclure dans les résultats. Voici comment les conditions vous aident à affiner vos résultats. Pour obtenir la liste et la description des conditions que vous pouvez utiliser dans une requête de recherche, consultez la section «conditions de recherche» dans [requêtes de mots clés et conditions de recherche pour la recherche de contenu](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="1da39-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


