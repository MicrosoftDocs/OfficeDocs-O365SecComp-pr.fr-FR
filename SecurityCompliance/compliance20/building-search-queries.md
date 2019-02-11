---
title: Créer des requêtes de recherche
ms.author: markjjo
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
ms.openlocfilehash: c337b49491fca11e0ba5bc13d22ac3e54038c400
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695070"
---
# <a name="build-search-queries"></a><span data-ttu-id="dec5c-102">Créer des requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="dec5c-102">Build search queries</span></span>

<span data-ttu-id="dec5c-103">Dans la création de votre requête, vous pouvez utiliser différents mots clés et les conditions pour définir les éléments à rechercher.</span><span class="sxs-lookup"><span data-stu-id="dec5c-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="dec5c-104">Recherches par mot-clé</span><span class="sxs-lookup"><span data-stu-id="dec5c-104">Keyword searches</span></span>

<span data-ttu-id="dec5c-p101">Dans la zone **mots clés** , tapez une requête de recherche. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **AND**, **OR**, **pas**et **NEAR**. Vous pouvez également rechercher des informations sensibles (comme les numéros de sécurité sociale) dans des documents ou de recherche pour les documents qui ont été partagées en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="dec5c-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="dec5c-p102">Sinon, vous pouvez cliquer sur la case à cocher **Afficher la liste des mots clés** et le type d’un mot clé dans chaque ligne. Si vous procédez ainsi, les mots clés dans chaque ligne sont connectés par un opérateur logique ( **c:s**) des fonctionnalités similaires à l’opérateur **OR** dans la requête de recherche qui est créée.</span><span class="sxs-lookup"><span data-stu-id="dec5c-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="dec5c-p103">Pourquoi utiliser la liste des mots clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés qui sont le plus (et moins) efficaces. Vous pouvez également utiliser une phrase de mots clés (entourée parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [statistique de recherche](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="dec5c-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="dec5c-117">Conditions</span><span class="sxs-lookup"><span data-stu-id="dec5c-117">Conditions</span></span>
    
<span data-ttu-id="dec5c-p104">Vous pouvez ajouter des conditions de recherche pour affiner la recherche et de renvoyer un jeu de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par un opérateur logique (**c : c**) des fonctionnalités similaires à l’opérateur **et** . Cela signifie que les éléments ont afin de répondre à la requête de mot clé et une ou plusieurs conditions à inclure dans les résultats. Il s’agit de comment conditions vous aider à limiter les résultats. Pour une liste et une description des conditions que vous pouvez utiliser dans une requête de recherche, voir la section « Conditions de recherche » dans les [requêtes de mot clé et les conditions de recherche pour la recherche de contenu](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="dec5c-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


