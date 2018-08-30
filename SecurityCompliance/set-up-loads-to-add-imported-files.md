---
title: Définissez la charge pour ajouter les fichiers importés dans Office 365 avancée de découverte électronique
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Passez en revue les étapes pour ajouter les fichiers importés au dernier chargement défini ou par lot, des fichiers avant d’effectuer la formation de la pertinence dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528625"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="e62e5-103">Définissez la charge pour ajouter les fichiers importés dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="e62e5-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="e62e5-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="e62e5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="e62e5-p102">Dans découverte avancée, une charge est un nouveau lot de fichiers ajoutés à un cas. Par défaut, une charge est définie et tous les fichiers importés sont ajoutés. Avant d’effectuer la formation de pertinence, les fichiers importés doivent être ajoutés à la charge.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="e62e5-109">Prenez en compte les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="e62e5-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="e62e5-p103">Nouveaux fichiers connus pour être semblable aux fichiers précédentes chargés dans la base de données de dossier ou la charge précédente des fichiers a été un jeu aléatoire à partir de la collection de fichiers. Dans ce cas, ajoutez les fichiers importés pour le chargement du fichier en cours.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="e62e5-p104">Nouveaux fichiers sont différents des précédents (par exemple, à partir d’une autre source), ou vous ne connaissez pas qu’ils sont similaires ou différentes charges précédente. Dans ce scénario, ajoutez les fichiers importés vers un nouveau fichier charger. Découverte avancée détecte un scénario de charge matériel, appelle un processus rattrapage, verrouille la formation de la pertinence et les calculs par lots jusqu'à ce que rattrapage terminée, la nouvelle charge est intégrée et formée.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="e62e5-115">Ajout de fichiers importés à la charge actuelle</span><span class="sxs-lookup"><span data-stu-id="e62e5-115">Adding imported files to the current load</span></span>

<span data-ttu-id="e62e5-p105">Tous les fichiers importés doivent être ajoutés à une charge de traitement d’eDiscovery avancée. Les fichiers importés sont ajoutés à la dernière charge définie. Si vous importez des fichiers supplémentaires ultérieurement, ils doivent également être ajoutés à la charge.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="e62e5-119">Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Onglet Charges de configuration de pertinence](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="e62e5-p106">**Fichiers Include**: sélectionnez une option pour les fichiers à inclure. Par défaut, ajout de fichiers à la charge actuelle est basé sur la population « Tous les fichiers ».</span><span class="sxs-lookup"><span data-stu-id="e62e5-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="e62e5-p107">Chargez tous les fichiers réforme disponibles dans la pertinence. Si vous souhaitez charger uniquement un sous-ensemble des fichiers disponibles, voir tout d’abord cycle avec prise en charge, comme le chargement des sous-ensembles peut affecter la formation de pertinence.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="e62e5-125">Dans la **gestion de la charge**, sélectionnez une charge.</span><span class="sxs-lookup"><span data-stu-id="e62e5-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="e62e5-p108">Cliquez sur **Ajouter des fichiers**. Les fichiers sont ajoutés à la charge et un message de confirmation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="e62e5-128">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-128">Click **OK**.</span></span>
    
<span data-ttu-id="e62e5-129">Les fichiers peuvent maintenant être traités d’eDiscovery avancée pertinence pour les fichiers de formation.</span><span class="sxs-lookup"><span data-stu-id="e62e5-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="e62e5-130">Modification d’un nom de la charge au sein d’un cas</span><span class="sxs-lookup"><span data-stu-id="e62e5-130">Editing a load name within a case</span></span>

<span data-ttu-id="e62e5-131">Si vous modifiez le nom de la charge, il est recommandé d’utiliser un nom qui est important pour le cas.</span><span class="sxs-lookup"><span data-stu-id="e62e5-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="e62e5-132">Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="e62e5-p109">Dans la liste de la **gestion de la charge** , sélectionnez une charge, cliquez sur l’icône **Modifier** . La fenêtre Modifier la charge est affichée.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="e62e5-135">Entrez les modifications, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="e62e5-136">Ajout de fichiers importés dans un nouveau chargement</span><span class="sxs-lookup"><span data-stu-id="e62e5-136">Adding imported files to a new load</span></span>

<span data-ttu-id="e62e5-137">Après avoir démarré la formation de pertinence ou par lot des calculs, vous souhaiterez peut-être importer et traiter un ensemble de fichiers supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e62e5-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="e62e5-p110">Au cours de peut être réduite, vous pouvez créer, balise et analyser l’ensemble de rattrapage. Découverte avancée compare son évaluation des fichiers pertinents et Non-pertinents de la charge de nouveau à celles de chargements précédents. En fonction des résultats, vous êtes invité à prendre des décisions de rattrapage, si nécessaire et confirmé eDiscovery fournit des recommandations en fonction des informations à recevoir la pertinence.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="e62e5-141">Relatifs des charges et les fonctionnalités rattrapage varie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e62e5-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="e62e5-142">Lorsque vous importez un nouveau fichier charger après le calcul de lot, eDiscovery avancée détermine dans quelle mesure les fichiers peuvent être classées dans une des catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="e62e5-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="e62e5-143">Similaire (homogène) : un arrondi nouvel, personnalisé de formation de la pertinence n’est pas obligatoire et la base de connaissances alloué à partir de la charge précédente peut être appliqué « comme est » à la charge de nouveau.</span><span class="sxs-lookup"><span data-stu-id="e62e5-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="e62e5-144">Distinct (hétérogène) : un arrondi nouvel, personnalisé de formation de pertinence est nécessaire, et la base de connaissances alloué à partir de la charge précédente ne peut pas être appliqué.</span><span class="sxs-lookup"><span data-stu-id="e62e5-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="e62e5-145">Ces termes font référence au niveau de similarité de fichiers entre les charges et non au sein de la charge.</span><span class="sxs-lookup"><span data-stu-id="e62e5-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="e62e5-p111">Lorsque vous importez un nouveau fichier charger au cours de formation de pertinence (avant le calcul du lot), rattrapage vous permet de continuer formation pertinence sur l’ensemble de fichiers États-Unis. Découverte avancée ne pas estimer si la charge de nouveau est similaire à ou distinct de la charge précédente. Il simplement de collecte des informations sur la nouvelle charge et permet la pertinence de la formation continue sur les anciens et les nouveaux ensembles de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="e62e5-149">Lorsqu’il existe plusieurs problèmes en formation pertinence ainsi que les problèmes après le calcul de lot, le processus de rattrapage est effectué une fois pour tous les problèmes et les résultats sont calculées et affichées pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="e62e5-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e62e5-p112">La taille de l’échantillon rattrapage peut-être varier. Il dépend de la taille de la charge de nouveau par rapport à la charge précédente et le nombre d’échantillons effectué avant l’ajout de la charge de nouveau. L’exemple de rattrapage est généralement un ensemble de 200 à 2 000 fichiers à partir de la charge de nouveau.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="e62e5-p113">Rattrapage arrête toutes les autres tâches et requiert marquer le fichier individuel et révision. Par conséquent, vous pouvez réduire une surcharge lorsque vous ajoutez des fichiers volumineux par lots.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="e62e5-155">Ajout d’un nouveau chargement de fichiers à l’aide de rattrapage et propagée charge</span><span class="sxs-lookup"><span data-stu-id="e62e5-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="e62e5-156">Dans la **la pertinence \> le programme d’installation de la pertinence** , sélectionnez **la charge**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="e62e5-p114">Sous **Gestion des charges**, cliquez sur le **+** icône pour ajouter une charge. Un message de confirmation s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="e62e5-p115">Cliquez sur **Oui** pour continuer. La boîte de dialogue **Nouveau charger** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e62e5-161">Vous ne pouvez ajouter un nouveau chargement que si les actions effectuées à la charge précédente.</span><span class="sxs-lookup"><span data-stu-id="e62e5-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="e62e5-p116">Dans la boîte de dialogue **nouveau de charge** , tapez les informations de **charger le nom** et la **Description** et puis cliquez sur **OK**. Découverte avancée ajoute un nouveau chargement.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="e62e5-p117">Pour importer le nouveau fichier de charge, cliquez sur **Ajouter des fichiers**. Tous les nouveaux fichiers sont ajoutés à cette charge. Une fois la découverte avancée importe les fichiers, il reconnaît le scénario de charge matériel et indique rattrapage en tant que l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="e62e5-167">Cliquez sur **rattrapage** au bas de la boîte de dialogue pour exécuter le scénario.</span><span class="sxs-lookup"><span data-stu-id="e62e5-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="e62e5-168">Un seul ensemble de rattrapage, généralement contenant 200 à 2 000 fichiers à partir de la charge de nouveau, est créé pour tous les problèmes permettre de marquer le fichier simultané.</span><span class="sxs-lookup"><span data-stu-id="e62e5-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="e62e5-169">Plus d’informations sont fournies sur si les charges sont similaires ou distinct, eDiscovery avancée fusionnées ou fractionnées automatiquement de la charge et informations relatives au traitement de l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="e62e5-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="e62e5-p118">Vous pouvez ensuite baliser des fichiers et exécuter une opération de calculer. Le balisage permet de pertinence déterminer si les charges sont similaires ou distinctes et vous permet de continuer à travailler sur le nouveau jeu de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="e62e5-172">Une fois la révision, l’ensemble de rattrapage afficher **pertinence \> suivi** pour les résultats de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="e62e5-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="e62e5-173">Si le chargement du fichier a été ajouté au cours de formation de pertinence (ce qui signifie que le problème n’a pas encore été par le biais de calcul du lot), **la formation continuer** est l’étape suivante, quel que soit le résultat rattrapage.</span><span class="sxs-lookup"><span data-stu-id="e62e5-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="e62e5-p119">Les charges précédents et nouveau sont traitées comme une charge et formation pertinence continue sur l’ensemble États-Unis. Vous sont maintenant terminées avec cette procédure et que vous pouvez continuer de formation de pertinence.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="e62e5-176">Si la nouvelle charge a été ajoutée après le calcul de lot, passez à la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="e62e5-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="e62e5-177">Pour les charges de nouveau ajoutés après le calcul de lot, eDiscovery avancé détermine si la nouvelle charge est similaire à ou différent du précédente se charge, comme suit :</span><span class="sxs-lookup"><span data-stu-id="e62e5-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="e62e5-p120">Si la charge a été trouvée pour être similaire : aucune formation pertinence supplémentaire n’est nécessaire. Le tableau de bord affiche l’étape suivante recommandée consiste à exécuter ** calcul du lot ** pour calculer des résultats de la pertinence de la charge de nouveau. Charge a été trouvée pour être similaire, afin que l’analyse de classifieur précédente peut être exécutée sur les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run ** Batch calculation ** again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="e62e5-p121">Si la charge a été trouvée distincte : formation plus la pertinence est nécessaire et l’étape suivante consiste à la décision rattrapage. Sélectionnez une décision rattrapage comme suit :</span><span class="sxs-lookup"><span data-stu-id="e62e5-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="e62e5-p122">Si vous sélectionnez **charges de fusion**, avancée eDiscovery fusionne les charges précédents et nouveau pour le jeu de formation. Bien que le premier chargement est passé par le biais de calcul de lot, plus de formations est nécessaire. Continuer la formation charges précédents et nouveau ensemble. Calcul de lot puis réexécuter et les résultats de calcul de lot précédentes doivent être ignorées. Choisissez cette sélection lorsque des résultats de la pertinence de charges existantes peuvent être recalculées, par exemple, lors de la révision des charges de fichier existant n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="e62e5-p123">Si vous sélectionnez **charge fractionné**, continuer formation pertinence uniquement sur la charge de nouveau. Dans ce cas, scores de calcul de lot précédentes reste inchangée. Choisissez cette option lorsque existants scores de pertinence pour charges existantes ne peuvent pas être recalculées, par exemple, passer en revue les charges existant a déjà démarré. Résultats de la pertinence sont gérés séparément à partir de ce point et ne peuvent pas être fusionnées.</span><span class="sxs-lookup"><span data-stu-id="e62e5-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="e62e5-192">Cliquez sur **Continuer formation**.</span><span class="sxs-lookup"><span data-stu-id="e62e5-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e62e5-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e62e5-193">See also</span></span>

[<span data-ttu-id="e62e5-194">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="e62e5-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="e62e5-195">Définition des problèmes et affectation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e62e5-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="e62e5-196">Définition de mise en surbrillance des mots clés et avancées options</span><span class="sxs-lookup"><span data-stu-id="e62e5-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

