---
title: Utilisez le module de la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Découvrez le module de la pertinence dans Office 365 avancée eDiscovery, y compris un flux de travail et les instructions et les étapes pour passer en revue les fichiers et de formation.  '
ms.openlocfilehash: 2cf75ef95291c5393367ce01fb0cd660f9b99145
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527863"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="67448-103">Utilisez le module de la pertinence dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="67448-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="67448-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="67448-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="67448-p102">Dans découverte avancée, le module de la pertinence inclut la formation de la pertinence et la vérification des fichiers associés à un cas. Le flux de travail de pertinence est affichée et décrite comme suit :</span><span class="sxs-lookup"><span data-stu-id="67448-p102">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Flux de travail de pertinence](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="67448-109">**Cycles d’évaluation et de suivi**:</span><span class="sxs-lookup"><span data-stu-id="67448-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="67448-110">**Évaluation**: découverte avancée permet au plus tôt évaluation basée sur un échantillon aléatoire des fichiers et utilise cette évaluation pour appliquer les décisions pour déterminer les performances du processus de codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="67448-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="67448-111">**Suivi**: eDiscovery avancée calcule et affiche les résultats intermédiaires de l’évaluation lors de l’analyse statistique validité du processus.</span><span class="sxs-lookup"><span data-stu-id="67448-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="67448-112">**Cycles de formation et de suivi**:</span><span class="sxs-lookup"><span data-stu-id="67448-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="67448-113">**Balise**: découverte avancée prend connaissance des critères de pertinence spécifiques à chaque problème basée sur l’expert itératif et liaison de fichiers individuels.</span><span class="sxs-lookup"><span data-stu-id="67448-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="67448-114">**Suivi**: eDiscovery avancée calcule et affiche les résultats intermédiaires de la formation de pertinence lors de l’analyse statistique validité du processus.</span><span class="sxs-lookup"><span data-stu-id="67448-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="67448-115">**Calcul du lot**: découverte avancée prend les critères de la pertinence cumulés et enregistrés, s’applique à la collection de l’intégralité du fichier et génère des résultats de la pertinence pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="67448-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="67448-116">**Décider**: eDiscovery Avancé affiche les résultats de l’analyse appliquée au cas entière après le calcul du lot et affiche les données pour prendre des décisions de révision de document.</span><span class="sxs-lookup"><span data-stu-id="67448-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="67448-117">**Test**: résultats eDiscovery avancées peuvent être testées pour vérifier la validité et l’efficacité du traitement avancé eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="67448-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="67448-118">Recommandations pour la formation de la pertinence et passer en revue les</span><span class="sxs-lookup"><span data-stu-id="67448-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="67448-119">Voici une vue d’ensemble d’instructions pour la formation de la pertinence et passer en revue les :</span><span class="sxs-lookup"><span data-stu-id="67448-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="67448-p103">**Erreurs et les incohérences**: si des erreurs de liaison sont effectuées au cours de formation, revenir aux exemples de fichier précédente pour y remédier. S’il y trop grand nombre d’erreurs à corriger ou il existe un nouveau point de vue de l’incident ou un problème, les critères de la pertinence doivent être redéfinis par l’administrateur et redémarré la formation de pertinence.</span><span class="sxs-lookup"><span data-stu-id="67448-p103">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="67448-122">**Balisage et formation**:</span><span class="sxs-lookup"><span data-stu-id="67448-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="67448-p104">Les fichiers doivent être référencées en fonction du contenu uniquement. Ne pas tenir compte des métadonnées, telles que les dépositaires, la date ou chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="67448-p104">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="67448-125">Considérez date indications plage du texte pour marquer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="67448-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="67448-126">Considérez les images graphiques incorporés pour marquer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="67448-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="67448-p105">Si l’affichage d’un fichier à l’aide de l’icône de **mise en forme de texte** lors de la liaison, considérez la mise en forme de texte. Par exemple, un mot barré (une ligne horizontale par le biais de son centre de suppression) est considéré comme toujours par pertinence dans le cadre du texte analysé.</span><span class="sxs-lookup"><span data-stu-id="67448-p105">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text. For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="67448-p106">Ignorer le texte appliqué à la pertinence (tel que défini par le Gestionnaire d’incidents ou d’un administrateur) sera supprimé dans le contenu du fichier affiché dans l’affichage de texte dans la pertinence. Si les valeurs de texte de la case à cocher Ignorer ont été définies après la pertinence de la formation déjà démarré, le nouveau texte ignoré sera appliqué à des exemples de fichiers créés à partir du point dans lequel il a été défini. La fonctionnalité d’ignorer le texte doit être utilisée avec précaution, comme son utilisation peut réduire les performances de l’analyse des fichiers</span><span class="sxs-lookup"><span data-stu-id="67448-p106">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="67448-p107">Utilisez l’option **Ignorer le balisage** uniquement lorsque cela est nécessaire. EDiscovery avancée ne pas former basé sur les fichiers ignorés. Évaluation, s’il est difficile de déterminer si un fichier est pertinent, il est préférable de balise en tant que Relevant (R) ou non pertinent (NR) chaque fois que possible au lieu de sélectionner **Ignorer**. Lors de la découverte avancée évalue la formation, il sera visible bien ces types de fichiers ont été traités.</span><span class="sxs-lookup"><span data-stu-id="67448-p107">Use the **Skip tagging** option only when necessary. Advanced eDiscovery does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="67448-136">Même avec une petite quantité de texte extrait les fichiers doit être référencées en formation R/NR, plutôt que « Ignorer », lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="67448-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="67448-137">Marquage peut avoir un impact sur le classifieur tant que le fichier est accessible en lecture et peut être marqué comme R/NR.</span><span class="sxs-lookup"><span data-stu-id="67448-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="67448-138">Le numéro de séquence de fichier dans la liste de fichiers exemple affichée sous l’onglet **balise** permet à l’utilisateur revenir à la commande affichée d’origine des fichiers.</span><span class="sxs-lookup"><span data-stu-id="67448-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="67448-p108">Vous pouvez revenir en arrière à n’importe quel échantillon et modifier le balisage de l’évaluation et de formation définie des fichiers. Les modifications seront appliquées lors de la création de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="67448-p108">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="67448-141">Excel analysé les fichiers au format PDF doivent être traitées comme des fichiers Excel natifs pour marquer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="67448-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="67448-p109">En cas de doute concernant le balisage de la pertinence d’un fichier, contactez un expert. Liaison incorrecte au cours de la formation de pertinence peut entraîner la perte de temps plus loin dans le processus et peut également avoir un impact négatif sur la qualité globales des résultats de la.</span><span class="sxs-lookup"><span data-stu-id="67448-p109">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="67448-144">Mots clés qui ont été définis dans le mot clé listes seront affichera dans les couleurs pour aider l’utilisateur à identifier les fichiers appropriés lors de la liaison.</span><span class="sxs-lookup"><span data-stu-id="67448-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="67448-p110">**Calcul du lot**: les fichiers qui ont été marquées comme R/NR par l’expert reçoit un score de 0 ou 100. Cela s’applique au balisage avant le calcul de lot. Si l’expert basculer le problème inactif après le calcul du lot et suite marquage ce problème, les notes nouvellement balisés ne sera pas 100/0, mais plutôt le score d’origine.</span><span class="sxs-lookup"><span data-stu-id="67448-p110">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="67448-148">**Problèmes et échantillonnage mode**: problèmes sont généralement désactivées lors de leur travail est terminé (la stabilisation de formation de la pertinence et calcul de lot a été effectuée), lorsque les problèmes sont annulées, ou lorsqu’un autre utilisateur travaille sur les problèmes.</span><span class="sxs-lookup"><span data-stu-id="67448-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="67448-149">Étapes de la formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="67448-149">Steps in Relevance training</span></span>

<span data-ttu-id="67448-p111">Dans la **la pertinence \> suivi** onglet, eDiscovery avancée fournit des recommandations sur la façon de procéder de la transformation, avec les étapes suivantes. Les implications sont décrits ci-dessous lors de chacune des étapes suivantes est recommandé dans le processus de formation de pertinence.</span><span class="sxs-lookup"><span data-stu-id="67448-p111">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="67448-152">Marquer / continuer balisage : passer en revue les fichiers et la pertinence de la liaison effectuée par un expert pour chaque fichier et émettre au sein d’un échantillon.</span><span class="sxs-lookup"><span data-stu-id="67448-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="67448-153">Implication : Un exemple existant doit être marqué.</span><span class="sxs-lookup"><span data-stu-id="67448-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="67448-154">Évaluation / continuer d’évaluation : permet de validation au plus tôt de la pertinence des cas de problème et un aperçu de la pertinence de la population fichier importée pour le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="67448-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="67448-155">Implication : Plus d’évaluation est requis ou recommandée.</span><span class="sxs-lookup"><span data-stu-id="67448-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="67448-156">Formation / continuer de formation : processus pendant les options avancées eDiscovery étudient l’expert qui est marquer les fichiers exemples et acquiert la possibilité d’identifier les critères de la pertinence pertinentes pour chaque problème dans le contexte de chaque cas.</span><span class="sxs-lookup"><span data-stu-id="67448-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="67448-157">Implication : Le problème a besoin de plus de formations ; l’exemple suivant doit être créé et avec balise.</span><span class="sxs-lookup"><span data-stu-id="67448-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="67448-p112">Calcul du lot : processus de pertinence dans les paramètres avancés eDiscovery prend les connaissances acquises au cours de la phase de formation et s’applique à la population entière de fichier. Tous les fichiers dans le groupe de fichiers pertinentes sont évalués pour la pertinence et reçoivent un score de pertinence.</span><span class="sxs-lookup"><span data-stu-id="67448-p112">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="67448-160">Implication : Le problème a stabilisation et calcul de lot peut être effectuée.</span><span class="sxs-lookup"><span data-stu-id="67448-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="67448-161">Rattrapage : Pertinence indique quand un expert passe en revue et balises d’un échantillon de fichiers sélectionnés à partir d’une charge de fichiers supplémentaires pendant un scénario de déploiement charge.</span><span class="sxs-lookup"><span data-stu-id="67448-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="67448-162">Implication : Un nouveau chargement a été ajouté et rattrapage est nécessaire pour continuer à travailler.</span><span class="sxs-lookup"><span data-stu-id="67448-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="67448-163">Ajouter une balise à des incohérences : processus identifie via un algorithme de découverte électronique avancées, des incohérences dans le fichier de balisage processus ayant un impact négatif sur l’analyse.</span><span class="sxs-lookup"><span data-stu-id="67448-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="67448-164">Implication : L’exemple suivant inclut les fichiers qui ont été marquées dans les exemples précédents, et leur marquage doit être rétablie.</span><span class="sxs-lookup"><span data-stu-id="67448-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="67448-165">Mettre à jour de classifieur : permet à l’utilisateur à appliquer le marquage ou de l’amorçage des modifications.</span><span class="sxs-lookup"><span data-stu-id="67448-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="67448-166">Implication : Liaison et l’amorçage des modifications peuvent être appliquées sans avoir à exécuter manuellement un autre exemple de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="67448-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="67448-167">En attente : la pertinence de la formation processus est terminée.</span><span class="sxs-lookup"><span data-stu-id="67448-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="67448-168">Implication : Aucune formation de pertinence n’est requise à ce stade.</span><span class="sxs-lookup"><span data-stu-id="67448-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="67448-169">Bien qu’eDiscovery avancée vous guide à travers le processus, avec recommandé de suivre les étapes ci-après à différents stades, il vous permet également de naviguer entre les onglets et les pages et faites des choix de répondre à des situations qui peuvent être pertinentes à votre cas, le problème, ou processus de révision de documents.</span><span class="sxs-lookup"><span data-stu-id="67448-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="67448-p113">Il est possible d’accepter ou de remplacer l’étape suivante eDiscovery avancées choix de traitement. Si vous souhaitez effectuer une étape de l’étape suivante recommandée, cliquez sur l' **étape suivante** répertoriées dans l’affichage de l’étendue de problème dans la boîte de dialogue et cliquez sur le bouton **Modifier** en regard de l’étape suivante, sélectionnez une autre option étape suivante.</span><span class="sxs-lookup"><span data-stu-id="67448-p113">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67448-172">Certaines options peuvent rester désactivées après déverrouillage comme ils ne sont pas pris en charge pour une utilisation à ce stade du processus.</span><span class="sxs-lookup"><span data-stu-id="67448-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67448-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67448-173">See also</span></span>

[<span data-ttu-id="67448-174">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="67448-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-175">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="67448-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-176">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="67448-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-177">Marquage et formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="67448-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-178">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="67448-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-179">Selon les résultats de la sélection du conteneur</span><span class="sxs-lookup"><span data-stu-id="67448-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="67448-180">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="67448-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

