---
title: En se basant sur les résultats dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Découvrez comment l’onglet décider d’eDiscovery avancée de Office 365 fournit les données qui peuvent vous aider à déterminent la taille adéquate de l’ensemble de la révision de dossiers. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527817"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="68cfb-103">En se basant sur les résultats dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="68cfb-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="68cfb-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="68cfb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="68cfb-106">Dans découverte avancée, l’onglet Decide fournit des informations supplémentaires pour l’affichage et utilisation des statistiques d’aide à la décision pour déterminer la taille de l’ensemble de la révision de dossiers.</span><span class="sxs-lookup"><span data-stu-id="68cfb-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="68cfb-107">À l’aide de l’onglet décider</span><span class="sxs-lookup"><span data-stu-id="68cfb-107">Using the Decide tab</span></span>

![Décision de pertinence](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="68cfb-109">Cet onglet comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="68cfb-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="68cfb-110">**Problème**: à partir de là, vous pouvez sélectionner le problème d’intérêt dans la liste.</span><span class="sxs-lookup"><span data-stu-id="68cfb-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="68cfb-p102">**Rapport de rappel de la révision**: comparaison des avancées de révision eDiscovery en fonction des résultats de la pertinence. Le point de limite dans le graphique représente le pourcentage de fichiers pour passer en revue, mappé à un score de pertinence. Il est utilisé dans la phase de Test de la pertinence et en tant qu’un seuil d’exportation pour élimination. Le point de coupure par défaut, le nombre de fichiers pour passer en revue est au niveau du point dans lequel l’équilibre entre la précision et de rappel est optimal. Le point de coupure réel doit être déterminé par l’utilisateur en fonction des objectifs et les compromis de coût (révision %) et les risques (rappel %). À l’aide du curseur, vous pouvez régler le point de coupure et l’impact sur le graphique et les paramètres, consultez la rubrique lorsque vous ajustez le pourcentage de fichiers appropriés doivent être récupérées et avant de valider une décision.</span><span class="sxs-lookup"><span data-stu-id="68cfb-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="68cfb-p103">**Paramètres**: passez en revue, rappelez-vous, paramètres pertinents et Total coût suivante sont les statistiques calculées cumulatives se rapporte à la révision par rapport à la collection pour le cas de toute. Définitions de ces paramètres sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="68cfb-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="68cfb-118">**Passez en revue**: pourcentage de fichiers pour passer en revue en fonction de cette limite.</span><span class="sxs-lookup"><span data-stu-id="68cfb-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="68cfb-119">**Rappeler**: pourcentage de fichiers appropriés dans le jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="68cfb-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="68cfb-120">**Suivant pertinents**: coût d’examiner et d’identifier un fichier pertinent supplémentaire qui n’est pas actuellement à la révision défini.</span><span class="sxs-lookup"><span data-stu-id="68cfb-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="68cfb-p104">**Coût total**: coût pour l’examen de ce pourcentage des fichiers de dossiers. Paramètres coût peuvent être définis par le Gestionnaire d’incident.</span><span class="sxs-lookup"><span data-stu-id="68cfb-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="68cfb-p105">**Distribution par score de pertinence**: fichiers dans l’affichage gris foncé vers la gauche sont sous le score de coupure. Une info-bulle affiche le score de pertinence et le pourcentage de fichiers associé dans le fichier de révision défini en fonction du nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="68cfb-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="68cfb-p106">Le volet de détails étendu affiche des détails supplémentaires. Fichiers dans les illustrations de la collection n’incluent pas de fichiers vides ou confus. Illustrations de fichiers famille représentent les fichiers qui ne sont pas chargés dans la pertinence encore prise en compte dans le cadre de la famille.</span><span class="sxs-lookup"><span data-stu-id="68cfb-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68cfb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68cfb-128">See also</span></span>

[<span data-ttu-id="68cfb-129">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="68cfb-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="68cfb-130">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="68cfb-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="68cfb-131">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="68cfb-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="68cfb-132">Effectue la formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="68cfb-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="68cfb-133">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="68cfb-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="68cfb-134">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="68cfb-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

