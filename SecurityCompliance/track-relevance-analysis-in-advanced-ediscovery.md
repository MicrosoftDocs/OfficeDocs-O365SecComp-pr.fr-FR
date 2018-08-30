---
title: Suivre l’analyse de la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Découvrez comment afficher et interpréter l’état de la pertinence de la configuration et les résultats de problèmes dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528757"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="3a1ac-103">Suivre l’analyse de la pertinence dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="3a1ac-103">Track Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="3a1ac-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="3a1ac-106">D’eDiscovery avancée, l’onglet suivi de la pertinence affiche la validité de la formation de pertinence effectuée dans l’onglet balise calculée et indique l’étape suivante à prendre dans le processus de formation itératif à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-106">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="3a1ac-107">Suivi de l’état de formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="3a1ac-107">Tracking Relevance training status</span></span>

1. <span data-ttu-id="3a1ac-108">Afficher les détails suivants de la pertinence de la piste pour les problèmes, comme illustré dans l’exemple suivant d’une boîte de dialogue **nom du problème** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-108">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span> 
    
  - <span data-ttu-id="3a1ac-p102">**Évaluation**: cet indicateur de progression indique dans quelle mesure la pertinence de formation effectuées à ce stade est parvenu à la cible d’évaluation en termes de marge d’erreur. La plus grande richesse des résultats la pertinence de la formation est également affiché.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p102">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error. The richness of the Relevance training results is also displayed.</span></span> 
    
  - <span data-ttu-id="3a1ac-p103">**Formation**: cet affichage d’indicateur et info-bulle sur l’avancement indique la formation de la pertinence des résultats de la stabilité et une échelle numérique indiquant le nombre d’exemples de formation pertinence marqués pour chaque problème. L’expert surveille la progression du processus de formation de pertinence itératif.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p103">**Training**: This color-coded progress indicator and tool-tip display indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue. The expert monitors the progress of the iterative Relevance training process.</span></span> 
    
  - <span data-ttu-id="3a1ac-113">**Calcul du lot**: cet indicateur de progression fournit des informations sur la réalisation de calcul de lot.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-113">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
    
  - <span data-ttu-id="3a1ac-114">**Étape suivante**: affiche la recommandation pour la prochaine étape à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-114">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
    
    <span data-ttu-id="3a1ac-p104">Dans l’exemple, une évaluation correctement effectuée pour un problème indiqué par l’indicateur de progression terminé couleur et la coche est affichée. Marquage est en cours, mais celle-ci est considérée comme instable (état de la stabilité apparaissent également dans une info-bulle). La recommandation étape suivante est « formation ».</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p104">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark. Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip). The next step recommendation is "Training".</span></span> 
    
    ![Formation de suivi de pertinence étape 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="3a1ac-p105">La vue étendue affiche les options et les informations supplémentaires. La marge d’erreur actuel affiché est la marge d’erreur d’un rappel dans l’état actuel de l’évaluation, étant donnée les fichiers d’évaluation (déjà référencé) existant.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p105">The expanded view displays additional information and options. The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="3a1ac-p106">La phase d’évaluation peut être ignorée en désactivant la case à cocher **évaluation** par le problème, puis pour « tous les problèmes ». Toutefois, par conséquent, il n’y aura aucuns statistiques pour ce problème. > Si vous décochez la case à cocher **évaluation** uniquement peut être effectuée avant l’évaluation est effectuée. Il existe plusieurs problèmes dans un cas, évaluation est contournée uniquement si la case à cocher est désactivée pour chaque problème</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p106">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="3a1ac-125">Lors de l’évaluation n’est pas achevée avec le premier exemple de jeu de fichiers, évaluation peut être l’étape suivante pour marquer le plus de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-125">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span> 
    
    <span data-ttu-id="3a1ac-p107">Dans **la pertinence** \> **le suivi**, l’indicateur de progression de formation et info-bulle indiquent l’estimation du nombre d’échantillons supplémentaires nécessaires pour atteindre la stabilité. Cette estimation fournit des indications pour la formation supplémentaire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p107">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability. This estimate provides a guideline for the additional training needed.</span></span>
    
    ![Formation de suivi de pertinence](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="3a1ac-p108">Lorsque vous avez terminé de marquer et si vous souhaitez continuer de formation, cliquez sur **formation**. Exemple d’ensemble de fichiers est généré à partir du fichier chargé définie pour une formation supplémentaire. Puis, vous revenez à l’onglet balise pour baliser et former plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p108">When you're done tagging and if you need to continue training, click **Training**. Another sample set of files is generated from the loaded file set for additional training. You are then returned to the Tag tab to tag and train more files.</span></span>
    
### <a name="reaching-stable-training-levels"></a><span data-ttu-id="3a1ac-132">Atteindre les niveaux de formation stable</span><span class="sxs-lookup"><span data-stu-id="3a1ac-132">Reaching stable training levels</span></span>

<span data-ttu-id="3a1ac-133">Une fois les fichiers d’évaluation ont atteint un niveau stable de formation, eDiscovery avancée est prêt pour le calcul de lot.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-133">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a1ac-p109">En règle générale, après que trois stable des exemples de formation, l’étape suivante est « Calcul du lot ». Il peut exister des exceptions, par exemple, lorsqu’il y avait des modifications pour le marquage des fichiers à partir des exemples précédents ou lorsque les fichiers d’amorçage ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p109">Usually, after three stable training samples, the next step is "Batch calculation". There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="3a1ac-136">Effectuer le calcul de lot</span><span class="sxs-lookup"><span data-stu-id="3a1ac-136">Performing Batch calculation</span></span>

<span data-ttu-id="3a1ac-137">Calcul du lot est exécuté en tant que l’étape suivante après que la formation est terminée (lorsque l’état stable formation est indiqué par la barre de progression, une coche et l’état stable dans l’info-bulle.) Calcul du lot s’applique à la base de connaissances acquise au cours de la formation de pertinence pour l’intégralité du fichier de la population, pour évaluer la pertinence des fichiers et affecter les résultats de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-137">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="3a1ac-p110">Lorsqu’il existe plusieurs problèmes, calcul du lot s’effectue par le problème. Lors du calcul de lot, l’avancement est analysé lors du traitement de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p110">When there is more than one issue, Batch calculation is done per issue. During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="3a1ac-p111">Dans ce cas, l’étape suivante recommandée est « None », qui indique qu’aucune formation pertinence itérative supplémentaire n’est nécessaire à ce stade. La phase suivante est la **la pertinence \> Decide** onglet.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p111">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point. The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="3a1ac-142">Si vous souhaitez importer de nouveaux fichiers après le calcul de lot, l’administrateur peut ajouter les fichiers importés à une charge de nouveau.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-142">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a1ac-p112">Si vous cliquez sur **Annuler** lors du calcul de lot, le processus enregistre ce qui a déjà été exécuté. Si vous exécutez à nouveau calcul du lot, le processus se poursuit à partir du dernier point exécuté.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p112">If you click **Cancel** during Batch calculation, the process saves what was already executed. If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="3a1ac-145">Évaluation de la cohérence de liaison</span><span class="sxs-lookup"><span data-stu-id="3a1ac-145">Assessing tagging consistency</span></span>

<span data-ttu-id="3a1ac-p113">S’il existe des incohérences de marquer le fichier, il peut affecter l’analyse. La découverte avancée la cohérence des processus de balisage peut être utilisée lorsque les résultats ne sont pas optimaux ou cohérence est dans le doute. Une liste de fichiers de façon incohérente avec balise possibles est renvoyée, et ils peuvent être consultés et nouveau balisés, si nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p113">If there are inconsistencies in file tagging, it can affect the analysis. The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt. A list of possible inconsistently tagged files is returned, and they can be reviewed and re-tagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a1ac-p114">Après avoir au moins sept arrondit formation évaluation suivante, la cohérence de balisage peut être affichée dans **la pertinence** \> **suivi** \> **problème** \> **résultats détaillés** \> **cours de formation**. Cette révision est effectuée pour un seul problème à la fois.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p114">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**. This review is done for one issue at a time.</span></span> 
  
1. <span data-ttu-id="3a1ac-151">Dans **pertinence \> suivi**, développez la ligne d’un problème.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-151">In **Relevance \> Track**, expand an issue's row.</span></span>
    
2. <span data-ttu-id="3a1ac-152">À droite de **l’étape suivante**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-152">To the right of **Next step**, click **Modify**.</span></span>
    
3. <span data-ttu-id="3a1ac-153">Sélectionnez l’option de **l’étape suivante** , après sept exemples de formation **incohérences de balise** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-153">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
    
4. <span data-ttu-id="3a1ac-p115">Sélectionnez les **incohérences de la balise**. L’onglet **balise** s’ouvre, affichant une liste des incohérences pour baliser nouveau que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p115">Select **Tag inconsistencies**. The **Tag** tab opens displaying a list of the inconsistencies to re-tag as necessary.</span></span> 
    
5. <span data-ttu-id="3a1ac-p116">Cliquez sur **Calculer** pour valider les modifications. L’étape suivante après que le marquage des incohérences est « formation ».</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p116">Click **Calculate** to submit the changes. The next step after tagging inconsistencies is "Training".</span></span> 
    
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="3a1ac-158">Affichage et utilisation des résultats de la pertinence</span><span class="sxs-lookup"><span data-stu-id="3a1ac-158">Viewing and using Relevance results</span></span>

<span data-ttu-id="3a1ac-p117">Dans la **la pertinence \> suivi** onglet, développez la ligne d’un problème et en regard des **résultats détaillés**, cliquez sur **Afficher**. Les volets de résultats détaillés sont affichées, comme indiqué et décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p117">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**. The Detailed results panes are displayed, as shown and described below.</span></span>
  
![Résultats détaillés de la formation de pertinence](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="3a1ac-162">Résumé de liaison</span><span class="sxs-lookup"><span data-stu-id="3a1ac-162">Tagging summary</span></span>

 <span data-ttu-id="3a1ac-163">Dans l’exemple ci-dessous, le **balisage synthèse** affiche des totaux pour chaque fichier rattrapage marquer le processus, de formation et évaluation.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-163">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span> 
  
![Résumé du marquage du suivi de pertinence](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="3a1ac-165">Keywords</span><span class="sxs-lookup"><span data-stu-id="3a1ac-165">Keywords</span></span>

<span data-ttu-id="3a1ac-p118">Un mot clé est une chaîne unique, word, une expression ou séquence de mots dans un fichier identifiée par eDiscovery avancée comme un indicateur significatif si un fichier est pertinent. Mot clé et poids en fichiers marqués comme pertinents de liste colonnes « Include », et les colonnes « Exclure » répertorie les mots clés et poids en fichiers marqués comme non pertinents.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p118">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant. The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="3a1ac-p119">EDiscovery avancée assigne les valeurs de poids de mot clé positive ou négative. Plus le poids est élevé, plus la probabilité qu’un fichier dans lequel apparaît le mot clé est affecté un score de pertinence plus élevé lors du calcul de lot.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p119">Advanced eDiscovery assigns negative or positive keyword weight values. The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span> 
  
<span data-ttu-id="3a1ac-170">La liste de découverte électronique avancée des mots clés peut servir à compléter une liste générée par un expert ou dans un contrôle de validité indirect à tout moment dans le fichier de processus de révision.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-170">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="3a1ac-171">Cours de formation</span><span class="sxs-lookup"><span data-stu-id="3a1ac-171">Training progress</span></span>

<span data-ttu-id="3a1ac-172">Le volet **Des cours de formation** inclut un formation affichage en cours de graphique et la qualité indicateur, comme illustré dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-172">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span> 
  
![Avancement de la formation de suivi de pertinence](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 <span data-ttu-id="3a1ac-174">**Indicateur de qualité de formation**: affiche l’évaluation de la cohérence de liaison comme suit :</span><span class="sxs-lookup"><span data-stu-id="3a1ac-174">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="3a1ac-p120">**Bonne**: fichiers marqués régulièrement. (Vert clair affichées)</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p120">**Good**: Files are tagged consistently. (Green light displayed)</span></span>
    
- <span data-ttu-id="3a1ac-p121">**Moyenne**: certains fichiers peuvent être marqués de façon incohérente. (Jaune clair affichées)</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p121">**Medium**: Some files may be tagged inconsistently. (Yellow light displayed)</span></span>
    
- <span data-ttu-id="3a1ac-p122">**Avertissement**: nombre de fichiers peut-être être marqué de façon incohérente. (Rouge clair affichées)</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p122">**Warning**: Many files may be tagged inconsistently. (Red light displayed)</span></span>
    
 <span data-ttu-id="3a1ac-p123">**Graphique des cours de formation**: indique le degré de stabilité de formation de pertinence après un nombre de cycles de formation de pertinence par rapport à la valeur de mesure-F. Comme nous déplacer de gauche à droite dans le graphique, la permet de réduire intervalle de confiance et est utilisée, ainsi que la mesure F, eDiscovery avancée pertinence afin de déterminer la stabilité lorsque la formation de la pertinence des résultats sont optimisées.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p123">**Training progress graph**: Shows the degree of Relevance training stability after a number of Relevance training cycles in comparison to the F-measure value. As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a1ac-p124">La pertinence utilise une mesure F-mesure où rappel reçoit deux fois plus poids précision F2. Pour les cas avec la plus grande richesse haute (plus de 25 %), utilise la pertinence F1 (rapport 1:1). Le rapport de mesure F peut être configuré dans **le programme d’installation de la pertinence** \> **Paramètres avancés**.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p124">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision. For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio). The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span> 
  
### <a name="batch-calculation-results"></a><span data-ttu-id="3a1ac-186">Résultats du calcul de lot</span><span class="sxs-lookup"><span data-stu-id="3a1ac-186">Batch calculation results</span></span>

<span data-ttu-id="3a1ac-187">Le volet de **résultats de calcul** inclut le nombre de fichiers qui ont été marqués pour la pertinence, comme suit :</span><span class="sxs-lookup"><span data-stu-id="3a1ac-187">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="3a1ac-188">**Opération réussie**</span><span class="sxs-lookup"><span data-stu-id="3a1ac-188">**Success**</span></span>
    
- <span data-ttu-id="3a1ac-189">**Vide**: ne contient aucun texte, par exemple, seuls les espaces/onglets</span><span class="sxs-lookup"><span data-stu-id="3a1ac-189">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
    
- <span data-ttu-id="3a1ac-190">**Échec**: en raison de la taille d’un nombre excessif ou n’a pas pu être lues.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-190">**Failed**: Due to excessive size or could not be read</span></span>
    
- <span data-ttu-id="3a1ac-191">**Ignoré**: en raison de la taille d’un nombre excessif</span><span class="sxs-lookup"><span data-stu-id="3a1ac-191">**Ignored**: Due to excessive size</span></span>
    
- <span data-ttu-id="3a1ac-192">**Nebulous**: contient du texte sans signification ou aucune fonctionnalité pertinentes pour le problème</span><span class="sxs-lookup"><span data-stu-id="3a1ac-192">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
    
> [!NOTE]
> <span data-ttu-id="3a1ac-193">Vide, échec, ignoré ou Nebulous reçoit un score de pertinence de -1.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-193">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span> 
  
### <a name="training-statistics"></a><span data-ttu-id="3a1ac-194">Statistiques de formation</span><span class="sxs-lookup"><span data-stu-id="3a1ac-194">Training statistics</span></span>

<span data-ttu-id="3a1ac-195">Le volet des **statistiques de formation** affiche les statistiques et les graphiques en fonction des résultats à partir de la formation de la pertinence de la découverte électronique avancées.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-195">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![Statistiques de la formation de suivi de pertinence](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="3a1ac-197">Cet affichage montre les points suivants :</span><span class="sxs-lookup"><span data-stu-id="3a1ac-197">This view shows the following:</span></span>
  
- <span data-ttu-id="3a1ac-p125">**Taux de révision rappel**: comparaison des résultats en fonction de la pertinence de scores dans un examen hypothèse linéaire. Rappel est estimée étant donné la taille de jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p125">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review. Recall is estimated given the review set size set.</span></span>
    
- <span data-ttu-id="3a1ac-200">**Paramètres**: Cumulative calculé statistiques relatives à la révision par rapport à la population de fichier pour le dossier entier.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-200">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
    
- <span data-ttu-id="3a1ac-201">**Passez en revue**: pourcentage de fichiers pour passer en revue en fonction de cette limite.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-201">**Review**: Percentage of files to review based on this cutoff.</span></span>
    
- <span data-ttu-id="3a1ac-202">**Rappeler**: pourcentage de pertinents des fichiers dans le jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-202">**Recall**: Percentage of Relevant files in the review set.</span></span> 
    
- <span data-ttu-id="3a1ac-p126">**Distribution par score de pertinence**: fichiers dans l’affichage gris foncé vers la gauche sont sous le score de coupure. Une info-bulle affiche le score de pertinence et le pourcentage de fichiers associé dans le fichier de révision défini en fonction du nombre total de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3a1ac-p126">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a1ac-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a1ac-205">See also</span></span>

[<span data-ttu-id="3a1ac-206">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="3a1ac-206">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="3a1ac-207">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="3a1ac-207">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3a1ac-208">Exécution et évaluation de révision</span><span class="sxs-lookup"><span data-stu-id="3a1ac-208">Performing and reviewing Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3a1ac-209">Effectue la formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="3a1ac-209">Performing Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3a1ac-210">Prendre des décisions basées sur les résultats</span><span class="sxs-lookup"><span data-stu-id="3a1ac-210">Making decisions based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="3a1ac-211">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="3a1ac-211">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

