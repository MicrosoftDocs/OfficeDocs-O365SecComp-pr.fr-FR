---
title: Configuration des balises actives pour l’identification de la détection des privilèges client dans Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153966"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="34970-102">Configuration des balises actives pour une révision assistée par ML dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="34970-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="34970-103">Les fonctionnalités d’apprentissage automatique dans Advanced eDiscovery sont destinées à faciliter le processus de décision sur les documents.</span><span class="sxs-lookup"><span data-stu-id="34970-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="34970-104">Les balises actives permettent de mettre en place les fonctionnalités d’apprentissage automatique dans l’emplacement où sont enregistrées les décisions: les balises et les groupes de balises.</span><span class="sxs-lookup"><span data-stu-id="34970-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="34970-105">Lorsque vous créez un groupe de balises actives, les décisions du modèle ML mappées sur le groupe sont affichées en ligne avec les balises dans le groupe pour vous aider à afficher les informations en ligne, où elles sont le plus logiques.</span><span class="sxs-lookup"><span data-stu-id="34970-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="34970-106">Procédure de configuration d’un groupe de balises actives</span><span class="sxs-lookup"><span data-stu-id="34970-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="34970-107">Dans un jeu de révision, accédez à **Manage Review Set** -> **Manage Tags**.</span><span class="sxs-lookup"><span data-stu-id="34970-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="34970-108">Cliquez sur le menu déroulant en regard d' **Ajouter un groupe** de balises et sélectionnez **Ajouter un groupe de balises actives**.</span><span class="sxs-lookup"><span data-stu-id="34970-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="34970-109">Sélectionnez le modèle que vous souhaitez mapper à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="34970-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="34970-110">Cette opération crée une section de balise et N balises enfants, où N représente le nombre de sorties possibles du modèle.</span><span class="sxs-lookup"><span data-stu-id="34970-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="34970-111">Par exemple, le modèle de détection des privilèges du client avocat a deux sorties possibles: privilégié et non privilégié; la sélection de ce modèle crée deux balises enfants dans l’ensemble de révision, chacune correspondant à l’une des sorties possibles.</span><span class="sxs-lookup"><span data-stu-id="34970-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="34970-112">Renommez le groupe de balises et les balises en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="34970-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="34970-113">Utilisation d’un groupe de balises actives</span><span class="sxs-lookup"><span data-stu-id="34970-113">How to use a smart tag group</span></span>

<span data-ttu-id="34970-114">Lors de l’examen d’un document, les résultats du modèle seront exposés en regard de la valeur de balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="34970-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="34970-115">Par exemple, si vous disposez d’un groupe de balises actives pour la détection des privilèges du client et que vous révisez un document que le modèle a décidé est potentiellement privilégié, vous verrez le motif de cette balise en regard de la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="34970-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="34970-116">Il est important de noter que la balise n’est pas automatiquement appliquée; pour toutes les opérations et les objectifs, les balises d’un groupe de balises actives agissent de la même manière que les balises normales, à l’exception du fait qu’ils exposent les résultats du modèle en regard de ces derniers, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="34970-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>