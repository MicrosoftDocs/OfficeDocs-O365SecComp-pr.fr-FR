---
title: Analyse de la pertinence de test dans Office 365 avancée de découverte électronique
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Découvrez comment utiliser l’onglet Test après le calcul de lot dans Office 365 avancée de découverte électronique à tester, comparer et valider la qualité globale de traitement.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528121"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="33ac5-103">Analyse de la pertinence de test dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="33ac5-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="33ac5-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="33ac5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="33ac5-p102">L’onglet Test d’eDiscovery avancée vous permet de test, comparer et valider la qualité globale de traitement. Ces tests sont effectuées après le calcul de lot. En les balisant les fichiers de la collection, à un expert rend le jugement final si chaque fichier avec balise est réellement pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="33ac5-p103">Dans les scénarios uniques et plusieurs problèmes, tests sont généralement effectuées par le problème. Les résultats sont affichés après chaque test, et peuvent être réorganisation des résultats des tests avec spécifié d’exemples de fichiers de test.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="33ac5-111">Test du reste</span><span class="sxs-lookup"><span data-stu-id="33ac5-111">Testing the rest</span></span>

<span data-ttu-id="33ac5-p104">Le test « Tester le reste » est utilisé pour valider les décisions élimination, par exemple, pour consulter uniquement les fichiers ci-dessus un score démarcation la pertinence spécifique en fonction des résultats final eDiscovery avancées. L’expert examine un échantillon de fichiers sous un score limite sélectionné à évaluer le nombre de fichiers appropriés dans cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="33ac5-p105">Ce test fournit des statistiques et une comparaison entre l’ensemble de la révision et le Test de la population Rest. Les résultats de l’ensemble de révision sont ceux calculés par pertinence au cours de formation. Les résultats incluent des calculs, en fonction des paramètres et des paramètres d’entrée, tels que :</span><span class="sxs-lookup"><span data-stu-id="33ac5-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="33ac5-117">Tester les statistiques du nombre de fichiers d’exemple dans un exemple et identifié les fichiers appropriés.</span><span class="sxs-lookup"><span data-stu-id="33ac5-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="33ac5-p106">Tabulaire comparaison des paramètres de remplissage de l’ensemble de la révision et le reste, par exemple, le nombre de fichiers, une estimation du nombre de fichiers concernés, richesse estimé et le coût moyen de trouver un fichier pertinent supplémentaire. Paramètres coût peuvent être définis par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="33ac5-120">Ouvrir le **pertinence \> Test** onglet.</span><span class="sxs-lookup"><span data-stu-id="33ac5-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="33ac5-p107">Dans l’onglet **Test** , cliquez sur **Nouveau test**. La boîte de dialogue **créer de test** s’affiche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Résultats de pertinence du test Tester les éléments restants](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="33ac5-124">Dans **nom du Test**et **Description**, tapez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="33ac5-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="33ac5-125">Dans la liste **type de Test** , sélectionnez **le reste de Test**</span><span class="sxs-lookup"><span data-stu-id="33ac5-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="33ac5-126">Dans la **problème / catégorie** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="33ac5-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="33ac5-127">Dans la liste **de charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="33ac5-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="33ac5-128">Dans **% lecture**, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence de la coupure.</span><span class="sxs-lookup"><span data-stu-id="33ac5-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="33ac5-p108">Dans **définir la taille**, ou acceptez la valeur par défaut. Notez que les icônes de restauration restaure les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="33ac5-p109">Cliquez sur **Démarrer la liaison**. Un exemple de test est généré.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="33ac5-133">Passez en revue et ajouter une balise à chacun des fichiers dans le **la pertinence \> balise** onglet et lorsque vous avez terminé, cliquez sur **Calculer**.</span><span class="sxs-lookup"><span data-stu-id="33ac5-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="33ac5-p110">Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour voir les résultats des tests. Un exemple est illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![Résultats du test Tester les éléments restants](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="33ac5-137">Dans la figure ci-dessus, la section **paramètres de l’exemple** de la table contient plus d’informations sur le nombre de fichiers dans l’exemple par l’expert et le nombre de fichiers pertinents trouvés dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="33ac5-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="33ac5-p111">La section **paramètres de remplissage** de la table contient les résultats des tests, y compris la population set passer en revue les fichiers avec une note inférieure à la limite sélectionné et population « Le reste » des fichiers dont le score au-dessus de la limite sélectionnée. Pour chaque type de remplissage, les résultats suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="33ac5-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="33ac5-140">Inclut des fichiers avec % lecture - limite indiquée</span><span class="sxs-lookup"><span data-stu-id="33ac5-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="33ac5-141">Le nombre total de fichiers</span><span class="sxs-lookup"><span data-stu-id="33ac5-141">The total number of files</span></span> 
    
- <span data-ttu-id="33ac5-142">Estimation du nombre de fichiers concernés</span><span class="sxs-lookup"><span data-stu-id="33ac5-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="33ac5-143">La plus grande richesse estimée</span><span class="sxs-lookup"><span data-stu-id="33ac5-143">The estimated richness</span></span> 
    
- <span data-ttu-id="33ac5-144">Le coût moyen de révision de recherche d’un autre fichier pertinent</span><span class="sxs-lookup"><span data-stu-id="33ac5-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="33ac5-145">Test de la section</span><span class="sxs-lookup"><span data-stu-id="33ac5-145">Testing the slice</span></span>

<span data-ttu-id="33ac5-146">Le « tester le secteur « test exécute le test similaire à « Tester le reste » de test, mais à un segment du fichier définie comme spécifié par la pertinence de la lecture %.</span><span class="sxs-lookup"><span data-stu-id="33ac5-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="33ac5-147">Ouvrir le **pertinence \> Test** onglet.</span><span class="sxs-lookup"><span data-stu-id="33ac5-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="33ac5-p112">Dans l’onglet **Test** , cliquez sur **Nouveau test**. La boîte de dialogue **créer de test** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="33ac5-150">Dans **nom du Test** et **Description**, tapez les informations.</span><span class="sxs-lookup"><span data-stu-id="33ac5-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="33ac5-151">Dans la liste **type de Test** , sélectionnez **Test le secteur**.</span><span class="sxs-lookup"><span data-stu-id="33ac5-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="33ac5-152">Dans la liste de **problème** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="33ac5-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="33ac5-153">Dans la liste **de charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="33ac5-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="33ac5-154">Dans **% lecture entre**, acceptez les valeurs de la plage minimale et maximale par défaut ou sélectionnez des valeurs pour les résultats de la pertinence de la coupure.</span><span class="sxs-lookup"><span data-stu-id="33ac5-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="33ac5-155">Dans **définir la taille**, sélectionnez une valeur, ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="33ac5-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="33ac5-156">Les icônes de restauration permet de restaurer la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="33ac5-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="33ac5-p113">Cliquez sur **Démarrer la liaison**. Un exemple de test est généré.</span><span class="sxs-lookup"><span data-stu-id="33ac5-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="33ac5-159">Passez en revue et ajouter une balise à chacun des fichiers dans le **la pertinence \> balise** onglet et lorsque vous avez terminé, cliquez sur **Calculer**.</span><span class="sxs-lookup"><span data-stu-id="33ac5-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="33ac5-160">Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour voir les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="33ac5-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="33ac5-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33ac5-161">See also</span></span>

[<span data-ttu-id="33ac5-162">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="33ac5-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="33ac5-163">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="33ac5-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="33ac5-164">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="33ac5-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="33ac5-165">Marquage et formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="33ac5-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="33ac5-166">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="33ac5-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="33ac5-167">Selon les résultats de la sélection du conteneur</span><span class="sxs-lookup"><span data-stu-id="33ac5-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

