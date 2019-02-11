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
# <a name="build-search-queries"></a>Créer des requêtes de recherche

Dans la création de votre requête, vous pouvez utiliser différents mots clés et les conditions pour définir les éléments à rechercher.

## <a name="keyword-searches"></a>Recherches par mot-clé

Dans la zone **mots clés** , tapez une requête de recherche. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que **AND**, **OR**, **pas**et **NEAR**. Vous pouvez également rechercher des informations sensibles (comme les numéros de sécurité sociale) dans des documents ou de recherche pour les documents qui ont été partagées en externe. Si vous laissez la zone mot clé vide, tout le contenu situé dans les emplacements de contenu spécifiés sera inclus dans les résultats de recherche.
    
Sinon, vous pouvez cliquer sur la case à cocher **Afficher la liste des mots clés** et le type d’un mot clé dans chaque ligne. Si vous procédez ainsi, les mots clés dans chaque ligne sont connectés par un opérateur logique ( **c:s**) des fonctionnalités similaires à l’opérateur **OR** dans la requête de recherche qui est créée. 
    
Pourquoi utiliser la liste des mots clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments correspondent à chaque mot clé. Cela peut vous aider à identifier rapidement les mots clés qui sont le plus (et moins) efficaces. Vous pouvez également utiliser une phrase de mots clés (entourée parenthèses) dans une ligne. Pour plus d’informations sur les statistiques de recherche, voir [statistique de recherche](search-statistics.md).

## <a name="conditions"></a>Conditions
    
Vous pouvez ajouter des conditions de recherche pour affiner la recherche et de renvoyer un jeu de résultats plus précis. Chaque condition ajoute une clause à la requête de recherche qui est créée et exécutée lorsque vous démarrez la recherche. Une condition est logiquement connectée à la requête de mot clé (spécifiée dans la zone mots clés) par un opérateur logique (**c : c**) des fonctionnalités similaires à l’opérateur **et** . Cela signifie que les éléments ont afin de répondre à la requête de mot clé et une ou plusieurs conditions à inclure dans les résultats. Il s’agit de comment conditions vous aider à limiter les résultats. Pour une liste et une description des conditions que vous pouvez utiliser dans une requête de recherche, voir la section « Conditions de recherche » dans les [requêtes de mot clé et les conditions de recherche pour la recherche de contenu](../keyword-queries-and-search-conditions.md#search-conditions).


