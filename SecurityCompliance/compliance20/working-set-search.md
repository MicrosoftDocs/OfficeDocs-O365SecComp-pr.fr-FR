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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454986"
---
# <a name="query-the-data-in-a-working-set"></a><span data-ttu-id="822ee-102">Interroger les données d’un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="822ee-102">Query the data in a working set</span></span>

<span data-ttu-id="822ee-103">Dans la plupart des cas, il est utile de pouvoir approfondir ce qui se trouve dans un jeu de travail et de les organiser de manière plus efficace.</span><span class="sxs-lookup"><span data-stu-id="822ee-103">In most cases, it will be useful to be able to dig deeper into what is there in a working set and organize them to review more efficiently.</span></span> <span data-ttu-id="822ee-104">Les requêtes dans un jeu de travail vous permettent de le faire en vous permettant de vous concentrer sur un sous-ensemble de documents qui répondent aux critères définis par vous à la fois.</span><span class="sxs-lookup"><span data-stu-id="822ee-104">Queries within a working set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-working-set"></a><span data-ttu-id="822ee-105">Création et exécution d'une requête dans une plage de travail</span><span class="sxs-lookup"><span data-stu-id="822ee-105">Creating and running a query within a working set</span></span>

<span data-ttu-id="822ee-106">Pour créer et exécuter une requête dans votre plage de travail, cliquez sur «nouvelle requête» dans votre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="822ee-106">In order to create and run a query within your working set, click on "New Query" in your working set.</span></span> <span data-ttu-id="822ee-107">Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur «Enregistrer» pour exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="822ee-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="822ee-108">Pour exécuter une requête qui a été précédemment enregistrée, il suffit de cliquer sur la requête enregistrée.</span><span class="sxs-lookup"><span data-stu-id="822ee-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="822ee-109">RePortez-vous à champs de métadonnées de [document](document-metadata-fields.md) pour obtenir la liste des métadonnées que vous pouvez rechercher.</span><span class="sxs-lookup"><span data-stu-id="822ee-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="822ee-110">Création de votre requête</span><span class="sxs-lookup"><span data-stu-id="822ee-110">Building your query</span></span>

<span data-ttu-id="822ee-111">Vous pouvez créer votre requête à l'aide d'une combinaison de cartes de conditions et de langage de requête dans la carte de condition de mots-clés.</span><span class="sxs-lookup"><span data-stu-id="822ee-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span>

### <a name="condition-card"></a><span data-ttu-id="822ee-112">Carte de condition</span><span class="sxs-lookup"><span data-stu-id="822ee-112">Condition card</span></span>

<span data-ttu-id="822ee-113">Chaque champ pouvant faire l'objet d'une recherche dans un jeu de travail est doté d'une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="822ee-113">Every searchable field in a working set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="822ee-114">Il existe plusieurs types de cartes de condition:</span><span class="sxs-lookup"><span data-stu-id="822ee-114">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="822ee-115">FREETEXT: la carte de condition FREETEXT est utilisée pour les champs de texte tels que subject.</span><span class="sxs-lookup"><span data-stu-id="822ee-115">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="822ee-116">Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="822ee-116">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="822ee-117">Date: la carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="822ee-117">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="822ee-118">Options de recherche: la carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre plage de travail.</span><span class="sxs-lookup"><span data-stu-id="822ee-118">Search options: search options condition card will provide a list of possible values for the particular field in your working set.</span></span> <span data-ttu-id="822ee-119">Cette valeur est utilisée pour les champs tels que sender, où il existe un nombre fini de valeurs possibles dans votre plage de travail.</span><span class="sxs-lookup"><span data-stu-id="822ee-119">This is used for fields such as sender, where there is a finite number of possible values in your working set.</span></span>
- <span data-ttu-id="822ee-120">Mot-clé: la carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans.</span><span class="sxs-lookup"><span data-stu-id="822ee-120">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="822ee-121">Voir ci-dessous pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="822ee-121">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="822ee-122">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="822ee-122">Query language</span></span>

<span data-ttu-id="822ee-123">Outre les cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête.</span><span class="sxs-lookup"><span data-stu-id="822ee-123">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="822ee-124">Le langage de requête prend en charge la syntaxe KQL standard comme AND, OR, NOT et NEAR (n).</span><span class="sxs-lookup"><span data-stu-id="822ee-124">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="822ee-125">Le caractère générique (?) et caractère générique (\*) est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="822ee-125">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>