---
title: Comprendre l’évaluation dans la pertinence dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Obtenir une vue d’ensemble de la phase d’évaluation et de son rôle dans la détermination de la plus grande richesse des problèmes au cours de formation de la pertinence dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528112"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="fd20a-103">Comprendre l’évaluation dans la pertinence dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="fd20a-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="fd20a-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="fd20a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="fd20a-p102">EDiscovery avancé permet d’évaluation au plus tôt, par exemple, pour les problèmes définis et les données importées pour un cas. Découverte avancée permet l’expert pour prendre des décisions relatives à une approche à adopter et de les appliquer au projet de révision de document.</span><span class="sxs-lookup"><span data-stu-id="fd20a-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="fd20a-108">Évaluation de la présentation</span><span class="sxs-lookup"><span data-stu-id="fd20a-108">Understanding assessment</span></span>

<span data-ttu-id="fd20a-p103">Évaluation, l’expert examine un ensemble aléatoire de fichiers au moins 500, qui sont utilisées pour déterminer la plus grande richesse des problèmes et pour produire des statistiques qui reflètent les résultats de la formation. Évaluation réussit cas assez de fichiers pertinents pour atteindre un niveau statistique qui aide eDiscovery avancé pour fournir des statistiques exactes et déterminer efficacement la stabilisation point dans le processus de formation de pertinence.</span><span class="sxs-lookup"><span data-stu-id="fd20a-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="fd20a-p104">Plus que le nombre de pertinents fichiers dans le jeu d’évaluation, plus précis les statistiques et l’efficacité de l’algorithme de la stabilité. Le nombre de fichiers appropriées dans les fichiers d’évaluation dépend du problème. Plus grande richesse est le pourcentage estimé de fichiers appropriés dans le jeu de pertinent pour un problème. Problèmes avec une plus grande richesse atteindra un nombre de fichiers concernés plus rapidement que les problèmes avec la plus grande richesse inférieur. Problèmes avec la plus grande richesse très faible (par exemple, 2 % ou moins) nécessite une évaluation de très grande taille définie pour atteindre un nombre important de fichiers concernés.</span><span class="sxs-lookup"><span data-stu-id="fd20a-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="fd20a-p105">Statistiques, qui sont présentées dans les onglets de suivi et de décider au cours de formation et après le calcul de lot, incluent les estimations de rappel pour passer en revue les différents ensembles. Statistiques, estimations sont basées sur un échantillon définir (dans ce cas, les fichiers d’évaluation) incluent la marge d’erreur et le niveau de confiance de cette marge d’erreur. Par exemple, rappel estimée à 80 % peut-être une marge d’erreur de plus ou moins de 5 % avec un niveau de confiance de 95 %. Cela signifie que le rappel estimé est réellement 75-85 % et cette estimation a 95 % de confiance. Plus le jeu d’évaluation, la marge d’erreur devient plus petite et les statistiques sont plus précis.</span><span class="sxs-lookup"><span data-stu-id="fd20a-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="fd20a-p106">Une fois l’expert examine un ensemble d’évaluation initiale de 500 fichiers, la pertinence est en mesure de déterminer la marge d’erreur des valeurs de rappel en cours. La pertinence définit également une marge par défaut d’erreur indiquant qu’il est recommandé d’atteindre pour optimiser l’ensemble de l’évaluation. Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="fd20a-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="fd20a-124">Si l’évaluation déjà définie a engendré une marge d’erreur de plus ou moins 10 %, la pertinence recommande à passer à la formation (aucune évaluation supplémentaire n’est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="fd20a-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="fd20a-125">Si le jeu d’évaluation a engendré une marge d’erreur de plus ou moins 13 %, la pertinence peut vous recommandons de la révision d’un autre ensemble de fichiers d’évaluation pour atteindre une marge inférieure.</span><span class="sxs-lookup"><span data-stu-id="fd20a-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="fd20a-126">Si plus grande richesse est très faible, la pertinence est recommandé d’arrêt évaluation même si la marge d’erreur est importante (sans statistiques difficile), car l’ensemble de l’évaluation nécessaire atteindre une marge d’erreur utile est trop importante.</span><span class="sxs-lookup"><span data-stu-id="fd20a-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="fd20a-p107">Chaque problème a son propre richesse, la marge actuelle d’erreur et par conséquent, une estimation du nombre de fichiers d’évaluation supplémentaires. L’ensemble suivant d’évaluation est créée en fonction du nombre maximal de fichiers (jusqu'à 1 000 dans un jeu unique).</span><span class="sxs-lookup"><span data-stu-id="fd20a-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="fd20a-p108">Vous pouvez accepter les recommandations de la pertinence ou la marge d’erreur actuelle en fonction de vos besoins. La marge actuelle par défaut d’erreur est déterminée pour le rappel à égale ou supérieure à 75 %.</span><span class="sxs-lookup"><span data-stu-id="fd20a-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fd20a-p109">La phase d’évaluation peut être ignorée, dans le **la pertinence \> suivi** onglet dans l’affichage pour un problème, en désactivant la case à cocher **évaluation** par le problème, puis pour « tous les problèmes ». Toutefois, par conséquent, il n’y aura aucuns statistiques pour ce problème. > Si vous décochez la case à cocher **évaluation** uniquement peut être effectuée avant l’évaluation est effectuée. Il existe plusieurs problèmes dans un cas, évaluation est contournée uniquement si la case à cocher est désactivée pour chaque problème</span><span class="sxs-lookup"><span data-stu-id="fd20a-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd20a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd20a-135">See also</span></span>

[<span data-ttu-id="fd20a-136">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="fd20a-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="fd20a-137">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="fd20a-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fd20a-138">Marquage et formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="fd20a-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fd20a-139">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="fd20a-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fd20a-140">Selon les résultats de la sélection du conteneur</span><span class="sxs-lookup"><span data-stu-id="fd20a-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="fd20a-141">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="fd20a-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

