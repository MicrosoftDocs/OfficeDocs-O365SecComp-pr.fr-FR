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
description: Utilisez des mots clés et des conditions pour limiter l'étendue de la recherche lors de la recherche de données lors de l'utilisation de l'enquête sur les données dans Microsoft 365.
ms.openlocfilehash: eeca1bf7ff89d1b7f79ceeed3334668e354f035a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262884"
---
# <a name="build-search-queries"></a>Créer des requêtes de recherche

Lors de la création de requêtes de recherche, vous pouvez utiliser des mots clés pour rechercher du contenu et des conditions spécifiques afin de limiter l'étendue de la recherche afin de renvoyer les éléments les plus pertinents pour votre enquête.

![Utiliser des mots clés et des conditions pour affiner les résultats d'une recherche](../media/SearchQueryBox.png)

## <a name="keyword-searches"></a>Recherches par Mots clés

Tapez une requête de mot clé dans la zone **Mots clés** de la requête de recherche. Vous pouvez spécifier des mots clés, des propriétés de message électronique (par exemple, des dates d'envoi et de réception) ou des propriétés de document (telles que des noms de fichiers ou la date de la dernière modification d'un document). Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme **and**, **or**, **not**et **near**. Vous pouvez également rechercher des informations sensibles (telles que des numéros de sécurité sociale) dans des documents dans SharePoint et OneDrive (pas dans les messages électroniques) ou Rechercher des documents qui ont été partagés en externe. Si vous laissez la zone **Mots clés** vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de la recherche.
    
Vous pouvez également cliquer sur la case à cocher **afficher la liste de mots clés** et tapez un mot clé ou une expression de mot clé dans chaque ligne. Dans ce cas, les mots clés de chaque ligne sont connectés par un opérateur logique (représenté par *c:s*) qui est similaire à la fonctionnalité de l'opérateur **or** de la requête de recherche qui est créée. Cela signifie que les éléments qui contiennent un mot clé dans n'importe quelle ligne seront inclus dans les résultats de la recherche.

![Utiliser la liste de mots clés pour obtenir des statistiques sur chaque mot clé dans la requête](../media/KeywordListSearch.png)

Pourquoi utiliser la liste de mots clés? Vous pouvez obtenir des statistiques qui indiquent le nombre d'éléments qui correspondent à chaque mot clé dans la liste de mots clés. Cela peut vous aider à identifier rapidement les mots clés qui sont les plus efficaces (et les moins). Vous pouvez également utiliser une phrase de mots clés (entourée de parenthèses) dans une ligne de la liste des mots-clés. Pour plus d'informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).

> [!NOTE]
> Pour réduire les problèmes causés par les longues listes de mots clés, vous devez disposer d'un maximum de 20 lignes dans la liste des mots clés.

## <a name="conditions"></a>Conditions
    
Vous pouvez ajouter des conditions de recherche pour affiner l'étendue d'une recherche et renvoyer un ensemble de résultats plus raffiné. Chaque condition ajoute une clause à la requête de recherche créée et exécutée lors du démarrage de la recherche. Une condition est logiquement connectée à la requête de mot-clé (spécifiée dans la zone de mot clé) par un opérateur logique (représenté par *c:c*) qui est similaire à la fonctionnalité de l'opérateur **and** . Cela signifie que les éléments doivent satisfaire à la fois la requête de mot clé et une ou plusieurs conditions à inclure dans les résultats de la recherche. C’est ainsi que les conditions contribuent à affiner vos résultats. Pour obtenir la liste et la description des conditions que vous pouvez utiliser dans une requête de recherche, consultez la section «conditions de recherche» dans la rubrique [requêtes de mots clés et conditions de recherche](../keyword-queries-and-search-conditions.md#search-conditions).
