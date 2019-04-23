---
title: Ajouter des données d'une plage de travail à une autre
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
ms.openlocfilehash: e9e34d112cb84c27fec35e752eb2bfcbfe3136a3
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958235"
---
# <a name="add-data-to-a-working-set-from-another-working-set"></a><span data-ttu-id="b3e39-102">Ajouter des données à un jeu de travail à partir d'une autre plage de travail</span><span class="sxs-lookup"><span data-stu-id="b3e39-102">Add data to a working set from another working set</span></span>
<span data-ttu-id="b3e39-103">Dans certains cas, il peut s'avérer nécessaire de détourer une partie des documents d'une plage de travail et de les manipuler individuellement dans un autre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="b3e39-103">In some cases, it may be necessary to carve out a portion of documents from one working set and work with them individually in another working set.</span></span>  <span data-ttu-id="b3e39-104">Ceci est particulièrement utile si vous avez fait des sélections de contenu dans un jeu de travail et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.</span><span class="sxs-lookup"><span data-stu-id="b3e39-104">This is especially useful if you've culled content in a working set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="b3e39-105">Utilisez le flux de travail suivant pour ajouter du contenu d'un jeu de travail à un autre.</span><span class="sxs-lookup"><span data-stu-id="b3e39-105">Use the following workflow to add content from one working set to another.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="b3e39-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b3e39-106">Before you start</span></span>
<span data-ttu-id="b3e39-107">Avant de commencer, vous devez créer une nouvelle plage de travail.</span><span class="sxs-lookup"><span data-stu-id="b3e39-107">Before you start, you'll need to create a new working set.</span></span>  <span data-ttu-id="b3e39-108">Vous pouvez ajouter une nouvelle plage de travail par le biais de l'onglet *jeux de travail* [pour en savoir plus](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span><span class="sxs-lookup"><span data-stu-id="b3e39-108">A new working set can be added through the *Working sets* tab [Learn more](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span></span>

## <a name="step-1-identify-content-to-add-to-another-working-set"></a><span data-ttu-id="b3e39-109">Étape 1: identifier le contenu à ajouter à un autre jeu de travail</span><span class="sxs-lookup"><span data-stu-id="b3e39-109">Step 1: Identify content to add to another working set</span></span>
<span data-ttu-id="b3e39-110">Vous pouvez ajouter du contenu à une plage de travail en sélectionnant e-mails et documents dans la grille du document ou tous les éléments d'un résultat de recherche.</span><span class="sxs-lookup"><span data-stu-id="b3e39-110">You can add content to a working set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="b3e39-111">Si vous choisissez d'ajouter des éléments sélectionnés, sélectionnez les éléments, puis cliquez sur le menu déroulant *action* , puis *Ajouter à un autre jeu de travail*.</span><span class="sxs-lookup"><span data-stu-id="b3e39-111">If choosing to add selected items, select the items and click the *Action* drop down then *Add to another working set*.</span></span>

![Ajouter à une autre plage de travail](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-workings-set"></a><span data-ttu-id="b3e39-113">Étape 2: spécification des options d'ajout à un autre ensemble de tâches</span><span class="sxs-lookup"><span data-stu-id="b3e39-113">Step 2: Specify options for adding to another workings set</span></span>
<span data-ttu-id="b3e39-114">Dans le menu démenu *Ajouter à un autre jeu de travail* , sélectionnez d'abord le jeu de travail auquel vous souhaitez ajouter les éléments.</span><span class="sxs-lookup"><span data-stu-id="b3e39-114">In the *Add to another working set options* flyout, first choose the working set you want to add the items to.</span></span>  <span data-ttu-id="b3e39-115">Indiquez si vous souhaitez ajouter tous les résultats de recherche ou les éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="b3e39-115">Choose whether to add All search results or Selected items.</span></span>  <span data-ttu-id="b3e39-116">Informations supplémentaires fournit des options pour inclure toutes les métadonnées des éléments et pour finir si les balises de document doivent être incluses dans la nouvelle plage de travail.</span><span class="sxs-lookup"><span data-stu-id="b3e39-116">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new working set.</span></span>  <span data-ttu-id="b3e39-117">Une fois que vous avez cliqué sur *OK* , un nouveau travail est créé pour ajouter le contenu à un jeu de travail, vous pouvez surveiller la progression de ce ![travail dans l'onglet [travaux](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) . ajouter à une autre plage de travail](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span><span class="sxs-lookup"><span data-stu-id="b3e39-117">After clicking *OK* a new job will be created to add the content to a working set, you can monitor the progress of that job in the [Jobs](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) tab. ![Add to another working set](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span></span>
