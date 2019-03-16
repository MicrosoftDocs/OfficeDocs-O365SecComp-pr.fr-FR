---
title: Interroger les données d’un ensemble de travail
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
ms.openlocfilehash: 3000a066bf69f71327801035e7c270cc602565ac
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30639011"
---
# <a name="query-the-data-in-a-working-set"></a><span data-ttu-id="70a32-102">Interroger les données d’un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="70a32-102">Query the data in a working set</span></span>

<span data-ttu-id="70a32-103">Dans la plupart des cas, il est utile de pouvoir approfondir ce qui se trouve dans un jeu de travail et de les organiser de manière plus efficace.</span><span class="sxs-lookup"><span data-stu-id="70a32-103">In most cases, it will be useful to be able to dig deeper into what is there in a working set and organize them to review more efficiently.</span></span> <span data-ttu-id="70a32-104">Les requêtes dans un jeu de travail vous permettent de le faire en vous permettant de vous concentrer sur un sous-ensemble de documents qui répondent aux critères définis par vous à la fois.</span><span class="sxs-lookup"><span data-stu-id="70a32-104">Queries within a working set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-working-set"></a><span data-ttu-id="70a32-105">Création et exécution d'une requête dans une plage de travail</span><span class="sxs-lookup"><span data-stu-id="70a32-105">Creating and running a query within a working set</span></span>

<span data-ttu-id="70a32-106">Pour créer et exécuter une requête dans votre plage de travail, cliquez sur «nouvelle requête» dans votre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="70a32-106">In order to create and run a query within your working set, click on "New Query" in your working set.</span></span> <span data-ttu-id="70a32-107">Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur «Enregistrer» pour exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="70a32-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="70a32-108">Pour exécuter une requête qui a été précédemment enregistrée, il suffit de cliquer sur la requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="70a32-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="70a32-109">RePortez-vous à champs de métadonnées de [document](document-metadata-fields.md) pour obtenir la liste des métadonnées que vous pouvez rechercher.</span><span class="sxs-lookup"><span data-stu-id="70a32-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="70a32-110">Création de votre requête</span><span class="sxs-lookup"><span data-stu-id="70a32-110">Building your query</span></span>

<span data-ttu-id="70a32-111">Vous pouvez créer votre requête à l'aide d'une combinaison de cartes de conditions et de langage de requête dans la carte de condition de mots-clés.</span><span class="sxs-lookup"><span data-stu-id="70a32-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span> <span data-ttu-id="70a32-112">Vous pouvez regrouper les cartes de condition ensemble comme un bloc pour concevoir une requête plus complexe.</span><span class="sxs-lookup"><span data-stu-id="70a32-112">You can group condition cards together as a block to craft a more complex query.</span></span>

### <a name="condition-card"></a><span data-ttu-id="70a32-113">Carte de condition</span><span class="sxs-lookup"><span data-stu-id="70a32-113">Condition card</span></span>

<span data-ttu-id="70a32-114">Chaque champ pouvant faire l'objet d'une recherche dans un jeu de travail est doté d'une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="70a32-114">Every searchable field in a working set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="70a32-115">Il existe plusieurs types de cartes de condition:</span><span class="sxs-lookup"><span data-stu-id="70a32-115">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="70a32-116">FREETEXT: la carte de condition FREETEXT est utilisée pour les champs de texte tels que subject.</span><span class="sxs-lookup"><span data-stu-id="70a32-116">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="70a32-117">Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="70a32-117">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="70a32-118">Date: la carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="70a32-118">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="70a32-119">Options de recherche: la carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre plage de travail.</span><span class="sxs-lookup"><span data-stu-id="70a32-119">Search options: search options condition card will provide a list of possible values for the particular field in your working set.</span></span> <span data-ttu-id="70a32-120">Cette valeur est utilisée pour les champs, tels que sender, où il existe un nombre fini de valeurs possibles dans votre plage de travail.</span><span class="sxs-lookup"><span data-stu-id="70a32-120">This is used for fields, such as sender, where there is a finite number of possible values in your working set.</span></span>
- <span data-ttu-id="70a32-121">Mot-clé: la carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans.</span><span class="sxs-lookup"><span data-stu-id="70a32-121">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="70a32-122">Voir ci-dessous pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="70a32-122">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="70a32-123">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="70a32-123">Query language</span></span>

<span data-ttu-id="70a32-124">Outre les cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="70a32-124">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="70a32-125">Le langage de requête prend en charge la syntaxe KQL standard comme AND, OR, NOT et NEAR (n).</span><span class="sxs-lookup"><span data-stu-id="70a32-125">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="70a32-126">Le caractère générique (?) et caractère générique (\*) est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="70a32-126">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>

## <a name="filter"></a><span data-ttu-id="70a32-127">Filtre</span><span class="sxs-lookup"><span data-stu-id="70a32-127">Filter</span></span>

<span data-ttu-id="70a32-128">Outre les requêtes que vous pouvez enregistrer, vous pouvez superposer des conditions supplémentaires à la volée à vos résultats de requête à l'aide de filtres.</span><span class="sxs-lookup"><span data-stu-id="70a32-128">In addition to queries that you can save, you can overlay additional conditions on the fly to your query results using filters.</span></span> <span data-ttu-id="70a32-129">Les filtres diffèrent des requêtes de différentes manières:</span><span class="sxs-lookup"><span data-stu-id="70a32-129">Filters differ from queries in a few significant ways:</span></span>
- <span data-ttu-id="70a32-130">Les filtres sont transitoires (c'est-à-dire qu'ils ne sont pas conservés sur différentes sessions), tandis que les requêtes sont enregistrées dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="70a32-130">Filters are transient (i.e. they do not persist over different sessions), whereas queries are saved to the working set.</span></span>
- <span data-ttu-id="70a32-131">Les filtres sont toujours additifs; les filtres s'appliquent au-dessus de la requête que vous avez appliquée pour le moment, tandis que l'application d'une requête remplace la requête en vigueur.</span><span class="sxs-lookup"><span data-stu-id="70a32-131">Filters are always additive; filters will apply on top of the query you have in effect at the moment, whereas applying a query will replace the query in effect.</span></span>