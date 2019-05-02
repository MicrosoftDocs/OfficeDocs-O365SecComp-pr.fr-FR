---
title: Ajouter des données d’un ensemble de révision à un autre ensemble de révision
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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527162"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="fb314-102">Ajouter des données à un jeu de révision à partir d’un autre ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="fb314-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="fb314-103">Dans certains cas, il peut s’avérer nécessaire de supprimer une partie des documents d’un ensemble de révision et de les utiliser individuellement dans un autre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="fb314-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="fb314-104">Ceci est particulièrement utile si vous avez consulté du contenu dans un jeu de révision et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.</span><span class="sxs-lookup"><span data-stu-id="fb314-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="fb314-105">Utilisez le flux de travail suivant pour ajouter du contenu d’un jeu de révision à un autre.</span><span class="sxs-lookup"><span data-stu-id="fb314-105">Use the following workflow to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="fb314-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fb314-106">Before you begin</span></span>

<span data-ttu-id="fb314-107">Avant de commencer, vous devez créer un nouveau jeu de révision auquel ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="fb314-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="fb314-108">Un nouvel ensemble de révision peut être ajouté sous l’onglet **ensembles de révision** de la case.</span><span class="sxs-lookup"><span data-stu-id="fb314-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="fb314-109">Pour plus d’informations, consultez la rubrique [Manage Review sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="fb314-109">For more information, see [Manage review sets](managing-review-sets.md).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="fb314-110">Étape 1: identifier le contenu à ajouter à un autre ensemble de validation</span><span class="sxs-lookup"><span data-stu-id="fb314-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="fb314-111">Vous pouvez ajouter du contenu à un jeu de vérification en sélectionnant des e-mails et des documents dans la grille du document ou tous les éléments d’un résultat de recherche.</span><span class="sxs-lookup"><span data-stu-id="fb314-111">You can add content to a review set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="fb314-112">Si vous choisissez d’ajouter des éléments sélectionnés, sélectionnez les éléments, cliquez sur **action**, puis sur **Ajouter à un autre ensemble de réexamen**.</span><span class="sxs-lookup"><span data-stu-id="fb314-112">If choosing to add selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Ajouter à un autre ensemble de révision](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="fb314-114">Étape 2: spécification des options d’ajout à un autre ensemble de réexamen</span><span class="sxs-lookup"><span data-stu-id="fb314-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="fb314-115">Dans la page **Ajouter à un autre jeu de réexamen** , choisissez l’ensemble de révision auquel vous souhaitez ajouter les éléments.</span><span class="sxs-lookup"><span data-stu-id="fb314-115">In the **Add to another review set** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="fb314-116">Indiquez si vous souhaitez ajouter **tous les résultats de recherche ou les** **éléments sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="fb314-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="fb314-117">Informations supplémentaires fournit des options pour inclure toutes les métadonnées des éléments et pour finir si les balises de document doivent être incluses dans le nouveau jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="fb314-117">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new review set.</span></span>  <span data-ttu-id="fb314-118">Une fois que vous avez cliqué sur **OK** , un nouveau travail est créé pour ajouter le contenu à un jeu de révision; vous pouvez surveiller la progression de cette tâche dans l’onglet **travail** . Pour plus d’informations, consultez la rubrique [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="fb314-118">After clicking **Ok** a new job will be created to add the content to a review set; you can monitor the progress of that job on the **Job** tab. For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>

![Ajouter à un autre ensemble de révision](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
