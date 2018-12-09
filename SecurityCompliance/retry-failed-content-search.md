---
title: Nouvelle tentative d’une recherche de contenu pour corriger une erreur d’emplacement de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez le bouton Réessayer pour résoudre les recherches de contenu contenant des erreurs de l’emplacement du contenu.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210183"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="877a4-103">Nouvelle tentative d’une recherche de contenu pour corriger une erreur d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="877a4-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="877a4-104">Lorsque vous utilisez la recherche de contenu de la sécurité pour Microsoft Office 365 et le centre de conformité pour rechercher un très grand nombre de boîtes aux lettres (par exemple, la recherche au moins 100 000 boîtes aux lettres en une seule recherche de contenu), vous obtiendrez des erreurs de recherche qui sont similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="877a4-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="877a4-p101">Ces erreurs (avec les codes d’erreur de CS008-009 et CS012-002) indiquent que la recherche de contenu a échoué rechercher les emplacements de contenu spécifiques ; Dans cet exemple, deux boîtes aux lettres n’ont pas été exclus. Ces erreurs s’affichent dans la page de flottant état détails de la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="877a4-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="877a4-107">Cause des erreurs de l’emplacement du contenu</span><span class="sxs-lookup"><span data-stu-id="877a4-107">Cause of content location errors</span></span>

<span data-ttu-id="877a4-p102">Lorsque vous recherchez un grand nombre de boîtes aux lettres, la recherche est distribuée sur des milliers de serveurs dans un centre de données Microsoft. À tout moment, des serveurs spécifiques peuvent être dans l’état de redémarrage ou en cours de basculement pour les copies redondantes. Dans ces cas, la requête de recherche de contenu pour récupérer des données expire. Dans l’exemple précédent, les erreurs pour les boîtes aux lettres ayant échoué ont été le résultat de l’expiration de recherche.</span><span class="sxs-lookup"><span data-stu-id="877a4-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="877a4-112">Résolution des erreurs de l’emplacement du contenu</span><span class="sxs-lookup"><span data-stu-id="877a4-112">Resolving content location errors</span></span>

<span data-ttu-id="877a4-p103">Redémarrer la recherche entraînent souvent des erreurs similaires sur différents serveurs. Au lieu de redémarrer la recherche, cliquez sur le bouton **Réessayer** qui s’affiche en haut de la page de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="877a4-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Cliquez sur Réessayer pour résoudre les erreurs de l’emplacement du contenu](media/retrycontentsearch3.png)

<span data-ttu-id="877a4-p104">Ainsi, la nouvelle tentative de la recherche uniquement pour les boîtes aux lettres ayant échoué. Lorsque vous relancez la recherche, les autres résultats ont été correctement renvoyées sont conservés.</span><span class="sxs-lookup"><span data-stu-id="877a4-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="877a4-118">Conseils pour éviter les erreurs de l’emplacement du contenu</span><span class="sxs-lookup"><span data-stu-id="877a4-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="877a4-119">Voici quelques causes Ajout d’erreurs de l’emplacement du contenu et des conseils pour vous aider à éviter lors de la recherche de grandes quantités de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="877a4-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="877a4-p105">La boîte aux lettres en cours de recherche peut être occupé en raison de l’activité de l’utilisateur. Dans ce cas, le service de recherche peut limiter elle-même pour empêcher l’indisponibilité de la boîte aux lettres. Pour éviter ce problème, essayez d’exécuter des recherches pendant les heures creuses.</span><span class="sxs-lookup"><span data-stu-id="877a4-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="877a4-p106">La requête de recherche peut être récupération trop de contenu à partir de la boîte aux lettres. Si possible, essayez de limiter l’étendue de la recherche à l’aide de mots clés, des plages de dates et des conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="877a4-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="877a4-p107">Trop de mots clés ou expressions lorsque vous créez une requête de recherche à l’aide de la [liste des mots clés](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Lorsque vous exécutez une requête de recherche qui utilise la liste des mots clés, le service exécute essentiellement une recherche distincte pour chaque ligne dans la liste des mots clés afin que les statistiques peuvent être générées. Si vous utilisez la liste des mots clés dans les requêtes de recherche, réduisez le nombre de lignes dans la liste des mots clés ou divisez les mots clés numéros en plus petits listes et créer une nouvelle recherche pour chaque liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="877a4-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="877a4-128">Pour réduire les problèmes causés par mot clé grandes listes, vous êtes limité à un maximum de 20 lignes dans la liste des mots clés d’une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="877a4-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="877a4-p108">Trop de recherche est en cours sur la même boîte aux lettres en même temps. Si possible, essayez d’exécuter une recherche à la fois sur n’importe quel une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="877a4-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="877a4-p109">Recherche trop grand nombre de boîtes aux lettres en une seule recherche. La probabilité d’erreurs de l’emplacement du contenu augmente lorsque vous recherchez un très grand nombre de boîtes aux lettres. Si possible, essayez d’exécuter plusieurs recherches afin que chaque recherche inclut un sous-ensemble de boîtes aux lettres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="877a4-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="877a4-p110">Maintenance requis est en cours d’exécution sur la boîte aux lettres. Si ce problème se produit probablement rarement, attendre un peu alors que lorsqu’il reçoit l’erreur d’emplacement de contenu, puis relancez la recherche.</span><span class="sxs-lookup"><span data-stu-id="877a4-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
