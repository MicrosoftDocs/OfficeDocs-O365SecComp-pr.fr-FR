---
title: Marquage et évaluation dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: "Examinez les étapes pour effectuer une formation à l'évaluation, notamment des fichiers de marquage, et en examinant les résultats de l'évaluation dans Office 365 Advanced eDiscovery. "
ms.openlocfilehash: 02dae23b6489b40243272beea1d79e871ca6a911
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217934"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="95f54-103">Marquage et évaluation dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="95f54-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="95f54-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="95f54-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="95f54-106">Cette section décrit la procédure pour le module d'évaluation de la pertinence eDiscovery avancée.</span><span class="sxs-lookup"><span data-stu-id="95f54-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="95f54-107">Exécution de la formation et de l'analyse de l'évaluation</span><span class="sxs-lookup"><span data-stu-id="95f54-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="95f54-108">Sous l' **onglet \> suivi de pertinence** , cliquez sur **évaluation** pour démarrer l'évaluation de cas.</span><span class="sxs-lookup"><span data-stu-id="95f54-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="95f54-109">Dans le cadre de cette procédure, un exemple d'ensemble d'évaluation de 500 fichiers est créé \*\*\*\* et l'onglet balise s'affiche, qui contient le panneau balisage, le contenu du fichier et d'autres options de marquage.</span><span class="sxs-lookup"><span data-stu-id="95f54-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![Onglet Balise de pertinence pour l’évaluation](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="95f54-111">Examinez chaque fichier dans l'exemple, déterminez la pertinence du fichier pour chaque problème de cas, et marquez le fichier à l'aide des boutons pertinence (R), non pertinent (NR) et ignorer dans le volet de **marquage** .</span><span class="sxs-lookup"><span data-stu-id="95f54-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="95f54-p102">L'évaluation requiert 500 fichiers balisés. Si les fichiers sont «ignorés», vous recevrez plus de fichiers à balise.</span><span class="sxs-lookup"><span data-stu-id="95f54-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="95f54-114">Après avoir balisé tous les fichiers de l'exemple, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="95f54-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="95f54-p103">La marge d'erreur et la richesse de l'évaluation actuelle sont calculées et affichées sous l'onglet de **suivi de pertinence** , avec des détails détaillés par problème, comme illustré ci-dessous. Plus de détails sur cette boîte de dialogue sont décrits dans la section «examen des résultats des évaluations» plus loin.</span><span class="sxs-lookup"><span data-stu-id="95f54-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![Suivi de pertinence - Évaluation](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="95f54-p104">Par défaut, nous vous recommandons de passer à l'étape suivante par défaut lorsque l'indicateur de progression de l'évaluation du problème est terminé, indiquant que l'exemple d'évaluation a été révisé et que des fichiers appropriés ont été marqués. > sinon, si vous voulez afficher les résultats de l'onglet de **suivi** et contrôler la marge d'erreur et l'étape suivante, cliquez sur **modifier** en regard de l' **étape suivante**, sélectionnez **continuer l'évaluation**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="95f54-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="95f54-p105">Cliquez sur **modifier** à droite de la case à cocher **évaluation** pour afficher et spécifier les paramètres d'évaluation par problème. Une boîte de dialogue de **niveau d'évaluation** s'affiche pour chaque problème, comme illustré dans l'exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="95f54-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![Problème de cas de niveau d’évaluation](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="95f54-123">Les paramètres suivants du problème sont calculés et affichés dans la boîte de dialogue **niveau d'évaluation** :</span><span class="sxs-lookup"><span data-stu-id="95f54-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="95f54-p106">**Marge d'erreur cible pour les estimations de rappel**: en fonction de cette valeur, le nombre estimé de fichiers supplémentaires nécessaires à la révision est calculé. La marge utilisée pour le rappel est supérieure à 75% et avec un niveau de confiance de 95%.</span><span class="sxs-lookup"><span data-stu-id="95f54-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="95f54-126">**Fichiers d'évaluation supplémentaires requis**: indique le nombre de fichiers nécessaires si les exigences actuelles de marge d'erreur n'ont pas été respectées.</span><span class="sxs-lookup"><span data-stu-id="95f54-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="95f54-127">Pour ajuster la marge d'erreur actuelle et observer l'effet de différentes marges d'erreur (par problème):</span><span class="sxs-lookup"><span data-stu-id="95f54-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="95f54-128">Dans la liste **Sélectionner un problème** , sélectionnez un problème.</span><span class="sxs-lookup"><span data-stu-id="95f54-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="95f54-129">Dans **marge d'erreur cible pour les estimations de rappel**, entrez une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="95f54-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="95f54-130">Cliquez sur **mettre à jour les valeurs** pour voir l'impact des ajustements.</span><span class="sxs-lookup"><span data-stu-id="95f54-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="95f54-131">Cliquez sur **avancé** dans la boîte de dialogue **niveau d'évaluation** pour voir les paramètres et détails supplémentaires suivants:</span><span class="sxs-lookup"><span data-stu-id="95f54-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![Vue avancée de problème de cas de niveau d’évaluation](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="95f54-133">**Richesse estimée**: richesse estimée en fonction des résultats de l'évaluation actuelle</span><span class="sxs-lookup"><span data-stu-id="95f54-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="95f54-p107">**Pour le rappel présumé**: par défaut, la marge d'erreur cible s'applique au rappel supérieur à 75%. Cliquez sur **modifier** si vous souhaitez modifier ce paramètre et contrôler la marge d'erreur sur une plage de valeurs de rappel différente.</span><span class="sxs-lookup"><span data-stu-id="95f54-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="95f54-p108">**Niveau de confiance**: par défaut, la marge d'erreur recommandée pour la confiance est de 95%. Cliquez sur **modifier** si vous souhaitez modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="95f54-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="95f54-138">**Marge d'erreur de richesse attendue**: en fonction des valeurs mises à jour, il s'agit de la marge d'erreur attendue de la richesse, après examen de tous les fichiers d'évaluation supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="95f54-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="95f54-139">**Fichiers d'évaluation supplémentaires requis**: étant donné les valeurs mises à jour, le nombre de fichiers d'évaluation supplémentaires qui doivent être vérifiés pour atteindre la cible.</span><span class="sxs-lookup"><span data-stu-id="95f54-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="95f54-140">**Nombre total de fichiers d'évaluation requis**: étant donné les valeurs mises à jour, le nombre total de fichiers d'évaluation requis pour la révision.</span><span class="sxs-lookup"><span data-stu-id="95f54-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="95f54-141">**Nombre prévu de fichiers pertinents lors de l'évaluation**: étant donné les valeurs mises à jour, le nombre prévu de fichiers pertinents dans l'intégralité de l'évaluation une fois que tous les fichiers d'évaluation supplémentaires sont examinés.</span><span class="sxs-lookup"><span data-stu-id="95f54-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="95f54-p109">Cliquez sur recalculer les **valeurs**si les paramètres sont modifiés. Lorsque vous avez terminé, cliquez sur **OK** pour enregistrer les modifications (ou **suivant** lorsqu'il y a plusieurs problèmes à consulter ou modifier, puis **Terminer**).</span><span class="sxs-lookup"><span data-stu-id="95f54-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="95f54-144">Lorsqu'il existe plusieurs problèmes, une fois que tous les problèmes ont été vérifiés ou ajustés, un **niveau d'évaluation: Résumé** s'affiche, comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95f54-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Résumé de niveau d’évaluation](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="95f54-146">Une fois l'évaluation terminée, passez à l'étape suivante de la formation pertinente.</span><span class="sxs-lookup"><span data-stu-id="95f54-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="95f54-147">Examen des résultats de l'évaluation</span><span class="sxs-lookup"><span data-stu-id="95f54-147">Reviewing assessment results</span></span>

<span data-ttu-id="95f54-148">Une fois qu'un exemple d'évaluation est balisé, les résultats de l'évaluation sont calculés et affichés sous l'onglet suivi de pertinence.</span><span class="sxs-lookup"><span data-stu-id="95f54-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="95f54-149">Les résultats suivants s'affichent dans l'affichage de suivi étendu:</span><span class="sxs-lookup"><span data-stu-id="95f54-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="95f54-150">Évaluation de la marge d'erreur actuelle pour les estimations de rappel</span><span class="sxs-lookup"><span data-stu-id="95f54-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="95f54-151">Richesse estimée</span><span class="sxs-lookup"><span data-stu-id="95f54-151">Estimated richness</span></span>
    
- <span data-ttu-id="95f54-152">Fichiers d'évaluation supplémentaires requis (pour révision)</span><span class="sxs-lookup"><span data-stu-id="95f54-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="95f54-p110">L'évaluation de la marge d'erreur actuelle est la marge d'erreur recommandée par Advanced eDiscovery. Le numéro affiché pour le «fichiers d'évaluation supplémentaires requis» correspond à cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="95f54-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="95f54-p111">L'indicateur de progression de l'évaluation indique le niveau d'exécution de l'évaluation, en fonction de la marge d'erreur actuelle. Lorsque l'évaluation est en cours, l'utilisateur balise un autre exemple d'évaluation.</span><span class="sxs-lookup"><span data-stu-id="95f54-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="95f54-157">Lorsque l'indicateur de progression de l'évaluation indique l'évaluation terminée, cela signifie que la révision de l'exemple d'évaluation a été effectuée et que des fichiers appropriés ont été marqués.</span><span class="sxs-lookup"><span data-stu-id="95f54-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="95f54-158">L'affichage de suivi étendu présente l'étape suivante recommandée, les statistiques d'évaluation et l'accès aux résultats détaillés.</span><span class="sxs-lookup"><span data-stu-id="95f54-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="95f54-p112">Lorsque la richesse est très faible, le nombre de fichiers d'évaluation supplémentaires nécessaires pour atteindre un nombre minimal de fichiers pertinents pour produire des statistiques utiles est très élevé. Advanced eDiscovery vous recommande de passer à la formation. L'indicateur de progression de l'évaluation est ombré et aucune statistique n'est disponible.</span><span class="sxs-lookup"><span data-stu-id="95f54-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="95f54-p113">En l'absence de stabilisation statistiquement basée statistiquement, les résultats seront moins élevés. Toutefois, ces résultats peuvent être utilisés pour rechercher des fichiers pertinents lorsque vous n'avez pas besoin de connaître le pourcentage de fichiers pertinents trouvés. De même, cet État peut être utilisé pour former des problèmes avec une faible richesse, où les scores de pertinence peuvent accélérer l'accès aux fichiers pertinents à un problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="95f54-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="95f54-p114">Dans l' **onglet \> suivi de pertinence** , affichage des problèmes étendus, les options d'affichage suivantes sont disponibles: > l'étape suivante recommandée, telle que l' **étape suivante: le marquage** peut être contourné (par problème) en cliquant sur le bouton **modifier** pour son à droite, puis en sélectionnant une autre étape dans l' **étape suivante**. Lorsque l'indicateur de progression de l'évaluation n'est pas terminé, l'option évaluation est recommandée suivant, pour baliser les fichiers d'évaluation et augmenter la précision des statistiques. > vous pouvez modifier la marge d'erreur et évaluer son impact en cliquant sur **modifier**, puis dans la **boîte de dialogue niveau d'évaluation**, en modifiant la **marge d'erreur cible pour les estimations de rappel**, et en cliquant sur **mettre à jour les valeurs**. De plus, dans cette boîte de dialogue, vous pouvez afficher les options avancées en cliquant sur **avancé**. > vous pouvez afficher des statistiques supplémentaires sur le niveau d'évaluation et leur impact en cliquant sur **affichage**. Dans la boîte de dialogue résultats détaillés affichés, les statistiques sont disponibles par problème, lorsqu'il y a au moins 500 fichiers d'évaluation marqués et que 18 fichiers sont balisés comme pertinents pour le problème.</span><span class="sxs-lookup"><span data-stu-id="95f54-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95f54-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95f54-171">See also</span></span>

[<span data-ttu-id="95f54-172">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="95f54-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="95f54-173">Présentation de l'évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="95f54-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95f54-174">Étiquetage et formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="95f54-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95f54-175">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="95f54-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95f54-176">Choix en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="95f54-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95f54-177">Évaluation de l'analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="95f54-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

