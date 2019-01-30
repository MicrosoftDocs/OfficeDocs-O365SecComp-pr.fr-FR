---
title: Analyse des données dans un jeu de travail d’eDiscovery avancée (Preview)
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
ms.openlocfilehash: a6284204fd709bcf936688f36f38f6b3283b1f98
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607651"
---
# <a name="analyzing-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="17a41-102">Analyse des données dans un jeu de travail d’eDiscovery avancée (Preview)</span><span class="sxs-lookup"><span data-stu-id="17a41-102">Analyzing data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="17a41-p101">Lorsque le nombre de documents collectées est important, il peut être très difficile passer en revue toutes les. Découverte avancée (Preview) fournit un certain nombre d’outils pour analyser les documents pour réduire le volume de documents à réviser sans perte d’informations et pour vous aider à organiser les documents de manière cohérente. Pour en savoir plus sur ces fonctionnalités, voir :</span><span class="sxs-lookup"><span data-stu-id="17a41-p101">When the number of collected documents is large, it can be quite difficult to review them all. Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner. To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="17a41-106">Près de la détection des doublons</span><span class="sxs-lookup"><span data-stu-id="17a41-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="17a41-107">Threads de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="17a41-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="17a41-108">Thèmes</span><span class="sxs-lookup"><span data-stu-id="17a41-108">Themes</span></span>](themes.md)

<span data-ttu-id="17a41-109">Pour analyser des données dans un jeu de travail :</span><span class="sxs-lookup"><span data-stu-id="17a41-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="17a41-p102">Configurer les paramètres analytique pour votre cas. Pour plus d’informations, voir [configurer les paramètres de recherche et analytique](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="17a41-p102">Configure analytics settings for your case. For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="17a41-112">Ouvrez le jeu de travail que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="17a41-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="17a41-113">Accédez à « Gérer les jeu de travail ».</span><span class="sxs-lookup"><span data-stu-id="17a41-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="17a41-114">Cliquez sur « Analyser ».</span><span class="sxs-lookup"><span data-stu-id="17a41-114">Click "Analyze".</span></span>

<span data-ttu-id="17a41-115">Vous pouvez vérifier la progression de l’analyse dans l’onglet tâches dans votre cas.</span><span class="sxs-lookup"><span data-stu-id="17a41-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="17a41-116">Une fois l’analyse terminée, vous pouvez afficher le rapport analytique, les requêtes exécutées au sein de votre travail sur les sorties de l’analyse (pour plus d’informations, voir [requête au sein de votre travail définie](working-set-search.md)) et consultez les documents associés d’un document donné (pour plus d’informations, voir [ Examen des données dans le jeu de travail](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="17a41-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="17a41-117">Rapport Analytique</span><span class="sxs-lookup"><span data-stu-id="17a41-117">Analytics report</span></span>

<span data-ttu-id="17a41-118">Pour afficher un rapport analytique pour votre jeu de travail :</span><span class="sxs-lookup"><span data-stu-id="17a41-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="17a41-119">Ouvrez votre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="17a41-119">Open your working set.</span></span>
2. <span data-ttu-id="17a41-120">Accédez à « Gérer les jeu de travail ».</span><span class="sxs-lookup"><span data-stu-id="17a41-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="17a41-121">Cliquez sur « Report ».</span><span class="sxs-lookup"><span data-stu-id="17a41-121">Click "Report".</span></span>

<span data-ttu-id="17a41-122">Le rapport comporte quatre composants d’analyse :</span><span class="sxs-lookup"><span data-stu-id="17a41-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="17a41-123">**Répartition** - combien les messages électroniques, pièces jointes et des documents libres ont été trouvées dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="17a41-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="17a41-124">**Documents (à l’exclusion des pièces jointes)** - nombre de documents libre ont été tableaux croisés dynamiques, uniques près de doublons du tableau croisé dynamique ou un doublon exact d’un autre document.</span><span class="sxs-lookup"><span data-stu-id="17a41-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="17a41-125">**Messages électroniques** - combien de messages ont été inclusives, copies inclus, des inconvénients inclus ou aucun d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="17a41-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="17a41-126">**Pièces jointes** - nombre de pièces jointes ont été uniques ou d’une pièce jointe autre adresse e-mail dans le jeu de travail les doublons.</span><span class="sxs-lookup"><span data-stu-id="17a41-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>