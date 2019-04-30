---
title: Nouvelle tentative de recherche de contenu pour résoudre une erreur d'emplacement de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez le bouton nouvelle tentative pour résoudre les recherches de contenu présentant des erreurs d'emplacement de contenu.
ms.openlocfilehash: 0963bccfe88a74b82ec3155469ca6d892bf2f7d8
ms.sourcegitcommit: 72e8a74b55fe7f56b50e30ff10a635734b5a3220
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33472379"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="ebf69-103">Nouvelle tentative de recherche de contenu pour résoudre une erreur d'emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="ebf69-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="ebf69-104">Lorsque vous utilisez la recherche de contenu dans le centre de sécurité et de conformité pour rechercher un grand nombre de boîtes aux lettres, vous pouvez obtenir des erreurs de recherche semblables à celles-ci:</span><span class="sxs-lookup"><span data-stu-id="ebf69-104">When you use Content Search in the security and compliance center to search a large number of mailboxes, you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="ebf69-105">Ces erreurs (avec les codes d'erreur CS008-009 et CS012-002) indiquent que la recherche de contenu n'a pas pu Rechercher des emplacements de contenu spécifiques; dans cet exemple, deux boîtes aux lettres n'ont pas été recherchées.</span><span class="sxs-lookup"><span data-stu-id="ebf69-105">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched.</span></span> <span data-ttu-id="ebf69-106">Ces erreurs s'affichent sur la page de menu volant des détails de l'état de la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="ebf69-106">These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="ebf69-107">Cause des erreurs d'emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="ebf69-107">Cause of content location errors</span></span>

<span data-ttu-id="ebf69-108">Lors de la recherche d'un grand nombre de boîtes aux lettres, la recherche est répartie entre des milliers de serveurs dans un centre de contenu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ebf69-108">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter.</span></span> <span data-ttu-id="ebf69-109">À tout moment, des serveurs spécifiques peuvent être en état de redémarrage ou en cours de basculement vers des copies redondantes.</span><span class="sxs-lookup"><span data-stu-id="ebf69-109">At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies.</span></span> <span data-ttu-id="ebf69-110">Dans l'un ou l'autre de ces cas, la demande de récupération de données de la recherche de contenu expire.</span><span class="sxs-lookup"><span data-stu-id="ebf69-110">In either of these cases, the Content Search's request to retrieve data will timeout.</span></span> <span data-ttu-id="ebf69-111">Dans l'exemple précédent, les erreurs des boîtes aux lettres qui ont échoué étaient le résultat du dépassement du délai de la recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-111">In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="ebf69-112">Résolution des erreurs d'emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="ebf69-112">Resolving content location errors</span></span>

<span data-ttu-id="ebf69-113">Le redémarrage de la recherche entraîne souvent des erreurs similaires sur différents serveurs.</span><span class="sxs-lookup"><span data-stu-id="ebf69-113">Restarting the search will often result in similar errors on different servers.</span></span> <span data-ttu-id="ebf69-114">Au lieu de relancer la recherche, cliquez sur \*\*\*\* le bouton Réessayer qui s'affiche en haut de la page des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-114">Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Cliquez sur le bouton réEssayer pour résoudre les erreurs d'emplacement de contenu](media/retrycontentsearch3.png)

<span data-ttu-id="ebf69-116">Cela entraînera la nouvelle tentative de recherche uniquement pour les boîtes aux lettres qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="ebf69-116">This will result in the retrying the search only for the mailboxes that failed.</span></span> <span data-ttu-id="ebf69-117">Lorsque vous effectuez une nouvelle tentative de recherche, les autres résultats renvoyés avec succès sont conservés.</span><span class="sxs-lookup"><span data-stu-id="ebf69-117">When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="ebf69-118">Conseils pour éviter les erreurs d'emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="ebf69-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="ebf69-119">Voici quelques causes supplémentaires des erreurs d'emplacement de contenu et des conseils pour vous aider à les éviter lors de la recherche d'un grand nombre de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="ebf69-120">La boîte aux lettres recherchée est peut-être occupée en raison de l'activité de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebf69-120">The mailbox being searched might be busy due to user activity.</span></span> <span data-ttu-id="ebf69-121">Dans ce cas, le service de recherche peut limiter lui-même pour empêcher la boîte aux lettres de devenir indisponible.</span><span class="sxs-lookup"><span data-stu-id="ebf69-121">In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable.</span></span> <span data-ttu-id="ebf69-122">Pour éviter cela, essayez d'exécuter des recherches en dehors des heures d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="ebf69-122">To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="ebf69-123">La requête de recherche peut extraire trop de contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-123">The search query might be retrieving too much content from the mailbox.</span></span> <span data-ttu-id="ebf69-124">Dans la mesure du possible, essayez de limiter l'étendue de la recherche à l'aide de mots clés, de plages de dates et de conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-124">If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="ebf69-125">Trop de mots clés ou d'expressions de mots clés lorsque vous créez une requête de recherche à l'aide de la [liste des mots clés](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches).</span><span class="sxs-lookup"><span data-stu-id="ebf69-125">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches).</span></span> <span data-ttu-id="ebf69-126">Lorsque vous exécutez une requête de recherche qui utilise la liste de mots-clés, le service exécute essentiellement une recherche distincte pour chaque ligne de la liste de mots clés afin de pouvoir générer des statistiques.</span><span class="sxs-lookup"><span data-stu-id="ebf69-126">When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated.</span></span> <span data-ttu-id="ebf69-127">Si vous utilisez la liste de mots-clés dans les requêtes de recherche, réduisez le nombre de lignes dans la liste de mots clés ou divisez les mots clés en listes plus petites et créez une recherche différente pour chaque liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="ebf69-127">If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ebf69-128">Pour vous aider à réduire les problèmes causés par des listes de mots clés volumineux, vous êtes désormais limité à un maximum de 20 lignes dans la liste de mots clés d'une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="ebf69-129">Trop de recherches sont effectuées simultanément sur la même boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-129">Too many searches are being performed on the same mailbox at the same time.</span></span> <span data-ttu-id="ebf69-130">Si possible, essayez d'exécuter une recherche à la fois sur une seule boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-130">If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="ebf69-131">Recherche d'un trop grand nombre de boîtes aux lettres dans une seule recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-131">Searching too many mailboxes in a single search.</span></span> <span data-ttu-id="ebf69-132">La probabilité d'erreurs d'emplacement de contenu augmente lors de la recherche d'un très grand nombre de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-132">The probability of content location errors increases when searching a very large number of mailboxes.</span></span> <span data-ttu-id="ebf69-133">Si possible, essayez d'exécuter plusieurs recherches de sorte que chaque recherche comprenne un sous-ensemble de boîtes aux lettres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ebf69-133">If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="ebf69-134">La maintenance requise est effectuée sur la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ebf69-134">Required maintenance is being performed on the mailbox.</span></span> <span data-ttu-id="ebf69-135">Bien que cette cause se produise probablement rarement, patientez quelques instants après avoir reçu l'erreur d'emplacement de contenu, puis recommencez la recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf69-135">Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
