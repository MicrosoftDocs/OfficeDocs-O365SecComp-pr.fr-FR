---
title: Utiliser le module de pertinence pour analyser les données dans les preuves
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
ms.openlocfilehash: 3aa37a6778947934759eb652a9367559b9ef838b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257282"
---
# <a name="use-the-relevance-module-to-analyze-data-in-evidence"></a><span data-ttu-id="eb16b-102">Utiliser le module de pertinence pour analyser les données dans les preuves</span><span class="sxs-lookup"><span data-stu-id="eb16b-102">Use the Relevance module to analyze data in evidence</span></span>

<span data-ttu-id="eb16b-103">Dans les enquêtes de données (préversion), le module de pertinence inclut la formation pertinente et la révision des fichiers liés à une enquête.</span><span class="sxs-lookup"><span data-stu-id="eb16b-103">In Data Investigations (Preview), the Relevance module includes the Relevance training and review of files related to an investigation.</span></span> <span data-ttu-id="eb16b-104">Le flux de travail de pertinence est illustré et décrit comme suit:</span><span class="sxs-lookup"><span data-stu-id="eb16b-104">The Relevance workflow is shown and described as follows:</span></span>
  
![Flux de travail de pertinence](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="eb16b-106">**Cycles d'évaluation et de suivi**:</span><span class="sxs-lookup"><span data-stu-id="eb16b-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="eb16b-107">**Évaluation**: permet une évaluation précoce basée sur un échantillon aléatoire de fichiers et utilise cette évaluation pour appliquer des décisions afin de déterminer les performances du processus de codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="eb16b-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="eb16b-108">**Track**: calculer et afficher les résultats intermédiaires de l'évaluation tout en surveillant la validité statistique du processus.</span><span class="sxs-lookup"><span data-stu-id="eb16b-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="eb16b-109">**Cycles de formation et de suivi**</span><span class="sxs-lookup"><span data-stu-id="eb16b-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="eb16b-110">**Tag**: enquêtes sur les données (préversion) apprend des critères de pertinence spécifiques à chaque problème en fonction de la révision itérative et du balisage des fichiers individuels d'un expert.</span><span class="sxs-lookup"><span data-stu-id="eb16b-110">**Tag**: Data Investigations (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="eb16b-111">**Track**: calculer et afficher les résultats intermédiaires de la formation à la pertinence tout en surveillant la validité statistique du processus.</span><span class="sxs-lookup"><span data-stu-id="eb16b-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="eb16b-112">**Calcul par lots**: les critères de pertinence accumulés et appris sont appliqués à l'ensemble de la collection de fichiers et un score de pertinence est généré pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="eb16b-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="eb16b-113">**Décider**: les résultats de l'analyse appliquée à l'ensemble de la casse sont affichés après le calcul du lot, et les données utilisées pour prendre des décisions de révision de document sont affichées.</span><span class="sxs-lookup"><span data-stu-id="eb16b-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="eb16b-114">**Test**: les résultats peuvent être testés pour vérifier la validité et l'efficacité du traitement des analyses de données (aperçu).</span><span class="sxs-lookup"><span data-stu-id="eb16b-114">**Test**: Results can be tested to verify the validity and effectiveness of the Data Investigations (Preview) processing.</span></span>

- <span data-ttu-id="eb16b-115">**Recherche**: une fois le flux de travail de pertinence terminé, vous pouvez utiliser la sortie telle que le centile de lecture d'un document pour votre problème lors de l'exécution d'une requête dans votre plage de travail.</span><span class="sxs-lookup"><span data-stu-id="eb16b-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="eb16b-116">Instructions pour la formation et la révision de pertinence</span><span class="sxs-lookup"><span data-stu-id="eb16b-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="eb16b-117">Vous trouverez ci-dessous une vue d'ensemble des directives de formation et de révision:</span><span class="sxs-lookup"><span data-stu-id="eb16b-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="eb16b-118">**Erreurs et**incohérences: si des erreurs de marquage sont effectuées pendant l'apprentissage, revenez aux exemples de fichiers précédents pour les corriger.</span><span class="sxs-lookup"><span data-stu-id="eb16b-118">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="eb16b-119">S'il y a trop d'erreurs à corriger ou qu'il existe une nouvelle perspective ou un problème, les critères de pertinence doivent être redéfinis par l'administrateur et l'apprentissage de pertinence doit être redémarré.</span><span class="sxs-lookup"><span data-stu-id="eb16b-119">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="eb16b-120">**Balisage et formation**:</span><span class="sxs-lookup"><span data-stu-id="eb16b-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="eb16b-121">Les fichiers doivent être balisés en fonction du contenu uniquement.</span><span class="sxs-lookup"><span data-stu-id="eb16b-121">Files should be tagged based on content only.</span></span> <span data-ttu-id="eb16b-122">Ne considérez pas les métadonnées, telles que le dépositaire, la date ou le chemin d'accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="eb16b-122">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="eb16b-123">Ne pas tenir compte des indications de plage de dates dans le texte lors du marquage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb16b-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="eb16b-124">Ne considérez pas les images graphiques incorporées lors du balisage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb16b-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="eb16b-125">Ignorer le texte appliqué à la pertinence sera supprimé dans le contenu du fichier affiché dans l'affichage de texte en pertinence.</span><span class="sxs-lookup"><span data-stu-id="eb16b-125">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="eb16b-126">Si les valeurs pour ignorer le texte ont été définies après l'apprentissage de pertinence déjà démarré, le nouveau texte ignoré est appliqué aux fichiers d'exemple créés à partir du point dans lequel ils ont été définis.</span><span class="sxs-lookup"><span data-stu-id="eb16b-126">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="eb16b-127">La fonctionnalité ignorer le texte doit être utilisée avec précaution, car son utilisation peut réduire les performances de l'analyse des fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb16b-127">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="eb16b-128">Utilisez l'option **Ignorer** le balisage uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="eb16b-128">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="eb16b-129">Les enquêtes de données (préversion) ne sont pas basées sur les fichiers ignorés.</span><span class="sxs-lookup"><span data-stu-id="eb16b-129">Data Investigations (Preview) does not train based on skipped files.</span></span> <span data-ttu-id="eb16b-130">Dans l'évaluation, s'il est difficile de déterminer si un fichier est pertinent, il est préférable de baliser comme pertinentes (R) ou non pertinente (NR) autant que possible, au lieu de sélectionner **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="eb16b-130">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="eb16b-131">Lorsque les enquêtes sur les données (aperçu) évaluent la formation, il est possible que ces types de fichiers aient été traités.</span><span class="sxs-lookup"><span data-stu-id="eb16b-131">When Data Investigations (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="eb16b-132">Même les fichiers avec une très petite quantité de texte extrait doivent être balisés en formation sous la forme R/NR, plutôt qu'en tant que «Skip», lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="eb16b-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="eb16b-133">Le marquage peut avoir un impact sur le classifieur tant que le fichier est lisible et peut être marqué comme R/NR.</span><span class="sxs-lookup"><span data-stu-id="eb16b-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="eb16b-134">Le numéro de séquence de fichier de la liste des fichiers d' \*\*\*\* exemple affichés sous l'onglet balise permet à l'utilisateur de revenir à l'ordre d'affichage d'origine des fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb16b-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="eb16b-135">Vous pouvez revenir à n'importe quel exemple et modifier le balisage des fichiers d'évaluation et de jeu de formation.</span><span class="sxs-lookup"><span data-stu-id="eb16b-135">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="eb16b-136">Les modifications seront appliquées lors de la création de l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="eb16b-136">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="eb16b-137">Les fichiers Excel numérisés au format PDF doivent être traités de la même manière que les fichiers Excel natifs lors du balisage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="eb16b-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="eb16b-138">En cas de doute sur le balisage de pertinence d'un fichier, consultez un expert.</span><span class="sxs-lookup"><span data-stu-id="eb16b-138">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="eb16b-139">Un balisage inCorrect lors de la formation sur la pertinence peut entraîner un manque de temps dans le processus et peut également avoir un impact négatif sur la qualité des résultats globaux.</span><span class="sxs-lookup"><span data-stu-id="eb16b-139">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="eb16b-140">Les mots clés définis dans les listes de mots clés s'affichent dans des couleurs pour aider l'utilisateur à identifier les fichiers appropriés lors du marquage.</span><span class="sxs-lookup"><span data-stu-id="eb16b-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="eb16b-141">**Calcul par lots**: les fichiers marqués comme R/NR par l'expert recevront un score de 0 ou de 100.</span><span class="sxs-lookup"><span data-stu-id="eb16b-141">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="eb16b-142">Cela s'applique au marquage effectué avant le calcul du lot.</span><span class="sxs-lookup"><span data-stu-id="eb16b-142">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="eb16b-143">Si l'expert a activé le problème sur inActif après le calcul par lot et a continué à marquer ce problème, les scores nouvellement marqués ne seront pas 100/0 mais plutôt le score d'origine.</span><span class="sxs-lookup"><span data-stu-id="eb16b-143">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="eb16b-144">**Problèmes et mode d'échantillonnage**: les problèmes sont généralement désactivés lorsqu'ils sont terminés (la formation à la pertinence est stabilisée et le calcul par lot a été effectué), lors de l'annulation des problèmes ou lorsqu'un autre utilisateur travaille sur les problèmes.</span><span class="sxs-lookup"><span data-stu-id="eb16b-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="eb16b-145">Étapes de la formation pertinente</span><span class="sxs-lookup"><span data-stu-id="eb16b-145">Steps in Relevance training</span></span>

<span data-ttu-id="eb16b-146">Dans l' **onglet \> suivi de pertinence** , les enquêtes de données fournissent des recommandations sur la façon de procéder au traitement, avec les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb16b-146">In the **Relevance \> Track** tab, Data investigations provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="eb16b-147">Les implications sont décrites ci-dessous quand chacune des étapes suivantes est recommandée dans le processus de formation à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="eb16b-147">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="eb16b-148">Balisage/continuer le balisage: révision de fichier et balisage de pertinence effectuée par un expert pour chaque fichier et problème au sein d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="eb16b-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="eb16b-149">Implication: un échantillon existant doit être balisé.</span><span class="sxs-lookup"><span data-stu-id="eb16b-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="eb16b-150">Évaluation/continue Assessment: permet une validation précoce de la pertinence du problème et une vue préliminaire de la pertinence du remplissage du fichier importés pour le cas en cours.</span><span class="sxs-lookup"><span data-stu-id="eb16b-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="eb16b-151">Implication: une évaluation plus grande est requise ou recommandée.</span><span class="sxs-lookup"><span data-stu-id="eb16b-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="eb16b-152">Formation/poursuivez la formation: processus au cours duquel les enquêtes sur les données sont apprises auprès de l'expert qui balise les échantillons de fichiers et qui permettent d'identifier les critères de pertinence pertinents pour chaque problème dans le contexte de chaque cas.</span><span class="sxs-lookup"><span data-stu-id="eb16b-152">Training / Continue training: Process during which Data investigations learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="eb16b-153">Implication: le problème nécessite une formation supplémentaire; l'exemple suivant doit être créé et balisé.</span><span class="sxs-lookup"><span data-stu-id="eb16b-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="eb16b-154">Calcul par lot: processus de pertinence dans lequel les enquêtes de données prennent les connaissances acquises pendant l'étape de formation et les appliquent à l'ensemble du remplissage du fichier.</span><span class="sxs-lookup"><span data-stu-id="eb16b-154">Batch calculation: Relevance process in which Data investigations takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="eb16b-155">Tous les fichiers du groupe de fichiers pertinent sont évalués à des fins de pertinence et reçoivent un score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="eb16b-155">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="eb16b-156">Implication: le problème est stabilisé et le calcul par lot peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="eb16b-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="eb16b-157">Rattrapage: pertinence indique quand un expert examine et marque un échantillon de fichiers sélectionnés à partir d'une charge de fichier supplémentaire lors d'un scénario de charge en continu.</span><span class="sxs-lookup"><span data-stu-id="eb16b-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="eb16b-158">Implication: une nouvelle charge a été ajoutée et l'interCeption est nécessaire pour continuer à travailler.</span><span class="sxs-lookup"><span data-stu-id="eb16b-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="eb16b-159">Incohérences de balise: le processus identifie, via un algorithme d'analyse des données, des incohérences dans le processus de marquage de fichiers susceptibles d'avoir un impact négatif sur l'analyse.</span><span class="sxs-lookup"><span data-stu-id="eb16b-159">Tag inconsistencies: Process identifies, via an Data investigations algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="eb16b-160">Implication: l'exemple suivant inclut des fichiers qui ont été balisés dans les exemples précédents, et leur balisage doit être rétablie.</span><span class="sxs-lookup"><span data-stu-id="eb16b-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="eb16b-161">Mettre à jour le classifieur: permet à l'utilisateur d'appliquer des balises ou des modifications.</span><span class="sxs-lookup"><span data-stu-id="eb16b-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="eb16b-162">Implication: les modifications de marquage et d'amorçage peuvent être appliquées sans avoir à exécuter manuellement un autre exemple de pertinence.</span><span class="sxs-lookup"><span data-stu-id="eb16b-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="eb16b-163">En attente: le processus d'apprentissage de pertinence est terminé.</span><span class="sxs-lookup"><span data-stu-id="eb16b-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="eb16b-164">Implication: aucune formation pertinente n'est requise à ce stade.</span><span class="sxs-lookup"><span data-stu-id="eb16b-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="eb16b-165">Bien que les enquêtes de données vous guident tout au long du processus, avec les étapes suivantes recommandées à différentes étapes, il vous permet également de naviguer entre les onglets et les pages, et de faire des choix pour répondre aux situations susceptibles de concerner votre cas, problème ou processus de révision de documents.</span><span class="sxs-lookup"><span data-stu-id="eb16b-165">Although Data investigations guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="eb16b-166">Il est possible d'accepter ou de remplacer les analyses de données par les choix de traitement de l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="eb16b-166">It is possible to accept or override Data investigations Next step processing choices.</span></span> <span data-ttu-id="eb16b-167">Si vous souhaitez effectuer une étape différente de l'étape suivante recommandée, cliquez sur l' **étape suivante** figurant dans la boîte de dialogue Affichage du problème développé dans la boîte de dialogue, cliquez sur le bouton **modifier** en regard de l'étape suivante, puis sélectionnez une autre étape suivante.</span><span class="sxs-lookup"><span data-stu-id="eb16b-167">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eb16b-168">Certaines options peuvent rester désactivées après un déverrouillage, car elles ne sont pas prises en charge à ce stade du processus.</span><span class="sxs-lookup"><span data-stu-id="eb16b-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="eb16b-169">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="eb16b-169">More information</span></span>

[<span data-ttu-id="eb16b-170">Présentation de l'évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="eb16b-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eb16b-171">Balisage et évaluation</span><span class="sxs-lookup"><span data-stu-id="eb16b-171">Tagging and assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eb16b-172">Étiquetage et formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="eb16b-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eb16b-173">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="eb16b-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eb16b-174">Choix en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="eb16b-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eb16b-175">Évaluation de l'analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="eb16b-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="eb16b-176">InterRoger les données dans les preuves</span><span class="sxs-lookup"><span data-stu-id="eb16b-176">Query the data in evidence</span></span>](evidence-query.md)
