---
title: Configurer des chargements pour ajouter des fichiers importés dans Office 365 Advanced eDiscovery
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: "Passez en revue les étapes nécessaires pour ajouter des fichiers importés à la dernière charge ou un lot de fichiers défini avant d'effectuer une formation pertinente dans Office 365 Advanced eDiscovery.  "
ms.openlocfilehash: 8c5101628b468719f8aa4f81a4c73cbbb226105f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215984"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c9006-103">Configurer des chargements pour ajouter des fichiers importés dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c9006-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c9006-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="c9006-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c9006-p102">Dans Advanced eDiscovery, une charge est un nouveau lot de fichiers ajouté à un cas. Par défaut, une charge est définie et tous les fichiers importés sont ajoutés à celle-ci. Avant d'effectuer une formation pertinente, les fichiers importés doivent être ajoutés au chargement.</span><span class="sxs-lookup"><span data-stu-id="c9006-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="c9006-109">Examinez les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="c9006-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="c9006-p103">Les nouveaux fichiers sont semblables aux fichiers précédents chargés dans la base de données de cas, ou le chargement de fichiers précédent était un jeu aléatoire à partir de la collection de fichiers. Dans ce cas, ajoutez les fichiers importés au chargement du fichier en cours.</span><span class="sxs-lookup"><span data-stu-id="c9006-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="c9006-p104">Les nouveaux fichiers sont différents des fichiers précédents (par exemple, à partir d'une autre source) ou vous n'avez pas connaissance préalable qu'ils sont similaires ou différents des charges précédentes. Dans ce scénario, ajoutez les fichiers importés à un nouveau chargement de fichier. Advanced eDiscovery reconnaît qu'il s'agit d'un scénario de charge propagée, appelle un processus de rattrapage, verrouille la formation à la pertinence et calcule les lots jusqu'à ce que la rattrapage soit terminée, et la nouvelle charge est intégrée et exercée.</span><span class="sxs-lookup"><span data-stu-id="c9006-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="c9006-115">Ajout de fichiers importés à la charge actuelle</span><span class="sxs-lookup"><span data-stu-id="c9006-115">Adding imported files to the current load</span></span>

<span data-ttu-id="c9006-p105">Tous les fichiers importés doivent être ajoutés à une charge pour être traités dans Advanced eDiscovery. Les fichiers imPortés sont ajoutés au dernier chargement défini. Si vous importez des fichiers supplémentaires ultérieurement, ceux-ci doivent également être ajoutés au chargement.</span><span class="sxs-lookup"><span data-stu-id="c9006-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="c9006-119">Dans l' \*\* \> onglet Configuration\*\* de pertinence de pertinence, sélectionnez **charges**.</span><span class="sxs-lookup"><span data-stu-id="c9006-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Onglet Charges de configuration de pertinence](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="c9006-p106">**Fichiers include**: sélectionnez une option pour les fichiers à inclure. Par défaut, l'ajout de fichiers à la charge actuelle est basé sur le remplissage «tous les fichiers».</span><span class="sxs-lookup"><span data-stu-id="c9006-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="c9006-p107">Chargez tous les fichiers de Culling disponibles en toute pertinence. Si vous envisagez de ne charger qu'un sous-ensemble des fichiers disponibles, consultez d'abord la prise en charge, car le chargement de sous-ensembles peut affecter la formation à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="c9006-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="c9006-125">Dans la gestion de la **charge**, sélectionnez un chargement.</span><span class="sxs-lookup"><span data-stu-id="c9006-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="c9006-p108">Cliquez sur **Ajouter des fichiers**. Les fichiers sont ajoutés au chargement et un message de confirmation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="c9006-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="c9006-128">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9006-128">Click **OK**.</span></span>
    
<span data-ttu-id="c9006-129">Les fichiers peuvent désormais être traités dans l'intérêt de la découverte électronique avancée pour l'apprentissage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9006-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="c9006-130">Modification d'un nom de charge dans un cas</span><span class="sxs-lookup"><span data-stu-id="c9006-130">Editing a load name within a case</span></span>

<span data-ttu-id="c9006-131">Si vous modifiez le nom de la charge, il est recommandé d'utiliser un nom qui est significatif pour le cas.</span><span class="sxs-lookup"><span data-stu-id="c9006-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="c9006-132">Dans l' \*\* \> onglet Configuration\*\* de pertinence de pertinence, sélectionnez **charges**.</span><span class="sxs-lookup"><span data-stu-id="c9006-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="c9006-p109">Dans la liste **charges de gestion** , sélectionnez une charge, puis cliquez sur l'icône **modifier** . La fenêtre Modifier la charge s'affiche.</span><span class="sxs-lookup"><span data-stu-id="c9006-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="c9006-135">Entrez les modifications, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9006-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="c9006-136">Ajout de fichiers importés à une nouvelle charge</span><span class="sxs-lookup"><span data-stu-id="c9006-136">Adding imported files to a new load</span></span>

<span data-ttu-id="c9006-137">Après avoir commencé la formation pertinente ou effectué un calcul par lot, vous souhaiterez peut-être importer et traiter un ensemble de fichiers supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c9006-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="c9006-p110">Lors de l'interCeption, vous pouvez créer, marquer et analyser l'ensemble de rattrapage. Advanced eDiscovery compare son évaluation des fichiers pertinents et non pertinents dans le nouveau chargement à ceux des chargements précédents. En fonction des résultats, vous êtes invité à prendre des décisions de rattrapage, si nécessaire, et Advanced eDiscovery fournit des recommandations basées sur les informations de pertinence à recevoir.</span><span class="sxs-lookup"><span data-stu-id="c9006-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="c9006-141">Les charges de roulement et les fonctionnalités de rattrapage varient comme suit:</span><span class="sxs-lookup"><span data-stu-id="c9006-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="c9006-142">Lorsque vous importez une nouvelle charge de fichier après le calcul par lot, Advanced eDiscovery détermine dans quelle mesure les fichiers appartiennent à l'une des catégories suivantes:</span><span class="sxs-lookup"><span data-stu-id="c9006-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="c9006-143">Semblable (homogène): une formation de type nouvelle de pertinence personnalisée n'est pas requise et les connaissances allouées à partir de la charge précédente peuvent être appliquées «en l'aspect» à la nouvelle charge.</span><span class="sxs-lookup"><span data-stu-id="c9006-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="c9006-144">Distinct (hétérogène): une formation de série de pertinence personnalisée est requise et les connaissances allouées à partir de la charge précédente ne peuvent pas être appliquées.</span><span class="sxs-lookup"><span data-stu-id="c9006-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="c9006-145">Ces termes font référence au niveau de similarité des fichiers entre les charges et non dans les charges.</span><span class="sxs-lookup"><span data-stu-id="c9006-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="c9006-p111">Lors de l'importation d'une nouvelle charge de fichier lors de l'apprentissage de pertinence (avant le calcul par lot), l'interCeption vous permet de continuer la formation pertinente sur le jeu de fichiers-Unis. Advanced eDiscovery n'évalue pas si la nouvelle charge est similaire ou différente de la charge précédente. Il collecte simplement des informations sur la nouvelle charge et active une formation pertinente pour continuer sur les nouveaux et les derniers ensembles de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9006-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="c9006-149">Lorsqu'il existe plusieurs problèmes de formation pertinente, ainsi que des problèmes après le calcul par lot, le processus de rattrapage est effectué une fois pour tous les problèmes, et les résultats sont calculés et affichés pour chaque problème.</span><span class="sxs-lookup"><span data-stu-id="c9006-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c9006-p112">La taille de l'exemple de rattrapage peut varier. Cela dépend de la taille de la nouvelle charge par rapport aux charges précédentes et du nombre d'échantillons terminés avant l'ajout de la nouvelle charge. L'exemple de rattrapage est généralement un ensemble de 200 à 2 000 fichiers à partir de la nouvelle charge.</span><span class="sxs-lookup"><span data-stu-id="c9006-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="c9006-p113">Rattrapage arrête toutes les autres tâches et nécessite une balise et une révision de fichier individuelles. Par conséquent, vous pouvez réduire la charge liée à l'ajout de nouveaux fichiers dans des lots volumineux.</span><span class="sxs-lookup"><span data-stu-id="c9006-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="c9006-155">Ajout d'une nouvelle charge de fichier à l'aide de charges de rattrapage et de laminage</span><span class="sxs-lookup"><span data-stu-id="c9006-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="c9006-156">Dans l' \*\* \> onglet Configuration\*\* de pertinence de pertinence, sélectionnez **charges**.</span><span class="sxs-lookup"><span data-stu-id="c9006-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="c9006-p114">Sous **chargez la gestion**, **+** cliquez sur l'icône pour ajouter une charge. Un message de confirmation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="c9006-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="c9006-p115">Cliquez sur **Oui** pour continuer. La boîte de dialogue **Ajouter un nouveau chargement** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="c9006-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c9006-161">Vous pouvez ajouter une nouvelle charge uniquement si les actions ont été effectuées au chargement précédent.</span><span class="sxs-lookup"><span data-stu-id="c9006-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="c9006-p116">Dans la boîte de dialogue **Ajouter un nouveau chargement** , tapez les informations dans **charger le nom** et la **Description** , puis cliquez sur **OK**. Advanced eDiscovery ajoute une nouvelle charge.</span><span class="sxs-lookup"><span data-stu-id="c9006-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="c9006-p117">Pour importer le nouveau fichier de chargement, cliquez sur **Ajouter des fichiers**. Tous les nouveaux fichiers sont ajoutés à cette charge. Une fois que Advanced eDiscovery importe les fichiers, il reconnaît le scénario de charge propagée et indique qu'il s'agit de l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="c9006-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="c9006-167">Cliquez \*\*\*\* sur rattraper en bas de la boîte de dialogue pour exécuter le scénario.</span><span class="sxs-lookup"><span data-stu-id="c9006-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="c9006-168">Un seul jeu de rattrapage, contenant généralement 200 à 2 000 fichiers à partir de la nouvelle charge, est créé pour tous les problèmes afin d'autoriser la balise de fichier simultanée.</span><span class="sxs-lookup"><span data-stu-id="c9006-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="c9006-169">Des informations détaillées précisent si les charges sont similaires ou distinctes, si Advanced eDiscovery a fusionné ou fractionné le chargement automatique, ainsi que des informations sur le traitement à l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="c9006-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="c9006-p118">Vous pouvez ensuite baliser les fichiers et exécuter une opération Calculate. Le balisage permet de déterminer si les charges sont similaires ou distinctes et vous permet de continuer à travailler sur le nouveau jeu de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9006-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="c9006-172">Une fois le jeu de rattrapage révisé, affichez le \*\*suivi de pertinence \> \*\* pour les résultats de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="c9006-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="c9006-173">Si le nouveau chargement de fichier a été ajouté au cours de la formation à la pertinence (ce qui signifie que le problème n'a pas encore été effectué par le calcul par lot), poursuivez la **formation** à l'étape suivante, quels que soient les résultats de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="c9006-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="c9006-p119">Les charges nouvelles et précédentes sont traitées en une seule charge et une formation pertinente se poursuit sur l'ensemble américain. Vous avez maintenant terminé cette procédure et pouvez continuer la formation pertinente.</span><span class="sxs-lookup"><span data-stu-id="c9006-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="c9006-176">Si le nouveau chargement a été ajouté après le calcul par lot, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="c9006-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="c9006-177">Pour les nouvelles charges ajoutées après le calcul par lot, Advanced eDiscovery détermine si la nouvelle charge est similaire ou différente des charges précédentes, comme suit:</span><span class="sxs-lookup"><span data-stu-id="c9006-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="c9006-p120">Si les charges étaient similaires: aucune formation sur la pertinence supplémentaire n'est nécessaire. Le tableau de bord affiche l'étape suivante recommandée: exécuter \* \* calcul de lot \* \* à nouveau pour calculer les scores de pertinence pour le nouveau chargement. Les charges ont été similaires, de sorte que l'analyse de classifieur précédente peut être exécutée sur les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9006-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run \*\* Batch calculation \*\* again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="c9006-p121">Si les charges ont été jugées distinctes: une formation plus pertinente est nécessaire et l'étape suivante est la décision de rattrapage. Sélectionnez une décision de rattrapage comme suit:</span><span class="sxs-lookup"><span data-stu-id="c9006-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="c9006-p122">Si vous sélectionnez **fusionner les charges**, Advanced eDiscovery fusions Previous et New loads pour le jeu de formation. Bien que la première charge passe par le calcul par lot, une formation supplémentaire est nécessaire. Poursuivez l'apprentissage des nouvelles et des versions précédentes. Le calcul du lot s'exécutera de nouveau et les notes de calcul du lot précédent doivent être ignorées. Choisissez cette sélection lorsque les scores de pertinence pour les charges existantes peuvent être recalculés, par exemple, lorsque la révision des chargements de fichiers existants n'a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="c9006-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="c9006-p123">Si vous sélectionnez **fractionner les charges**, ne poursuivez la formation à pertinence que sur le nouveau chargement. Dans ce cas, les scores de calcul du lot précédent resteront tels quels. Choisissez cette option lorsque les scores de pertinence existants pour les charges existantes ne peuvent pas être recalculés, par exemple, si la révision des charges existantes a déjà commencé. Les scores de pertinence sont gérés séparément à ce stade et ne peuvent pas être fusionnés.</span><span class="sxs-lookup"><span data-stu-id="c9006-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="c9006-192">Cliquez sur **Continuer la formation**.</span><span class="sxs-lookup"><span data-stu-id="c9006-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9006-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9006-193">See also</span></span>

[<span data-ttu-id="c9006-194">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c9006-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c9006-195">Définition des sujets et affectation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c9006-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="c9006-196">Définition des mots clés surlignés et des options avancées</span><span class="sxs-lookup"><span data-stu-id="c9006-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

