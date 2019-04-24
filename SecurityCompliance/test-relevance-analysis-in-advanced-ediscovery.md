---
title: Tester l'analyse de pertinence dans Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: "Découvrez comment utiliser l'onglet test après le calcul par lot dans Office 365 Advanced eDiscovery pour tester, comparer et valider la qualité globale du traitement.  "
ms.openlocfilehash: 735a6d8088b4696e2ebc348db435a11914bd0b10
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259970"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="a1124-103">Tester l'analyse de pertinence dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a1124-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="a1124-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a1124-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a1124-106">L'onglet test dans Advanced eDiscovery vous permet de tester, de comparer et de valider la qualité globale du traitement.</span><span class="sxs-lookup"><span data-stu-id="a1124-106">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="a1124-107">Ces tests sont effectués après le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="a1124-107">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="a1124-108">En marquant les fichiers dans la collection, un expert détermine si chaque fichier balisé est pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="a1124-108">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="a1124-109">Dans les scénarios à un ou plusieurs problèmes, les tests sont généralement effectués par problème.</span><span class="sxs-lookup"><span data-stu-id="a1124-109">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="a1124-110">Les résultats peuvent être affichés après chaque test, et les résultats des tests peuvent être retravaillés avec les exemples de fichiers de test spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a1124-110">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="a1124-111">Test du reste</span><span class="sxs-lookup"><span data-stu-id="a1124-111">Testing the rest</span></span>

<span data-ttu-id="a1124-112">Le test «tester le reste» permet de valider les décisions de Culling, par exemple, pour examiner uniquement les fichiers situés au-dessus d'un score de pertinence spécifique basé sur les résultats avancés avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="a1124-112">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="a1124-113">L'expert examine un échantillon de fichiers sous un score de démarcation sélectionné pour évaluer le nombre de fichiers appropriés dans cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="a1124-113">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="a1124-114">Ce test fournit des statistiques et une comparaison entre l'ensemble de révision et le test la population Rest.</span><span class="sxs-lookup"><span data-stu-id="a1124-114">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="a1124-115">Les résultats du jeu de révision sont ceux calculés par pertinence lors de la formation.</span><span class="sxs-lookup"><span data-stu-id="a1124-115">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="a1124-116">Les résultats incluent des calculs en fonction des paramètres et des paramètres d'entrée, tels que:</span><span class="sxs-lookup"><span data-stu-id="a1124-116">The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="a1124-117">Tester des statistiques sur le nombre de fichiers dans un exemple et identifier les fichiers appropriés.</span><span class="sxs-lookup"><span data-stu-id="a1124-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="a1124-118">Comparaison tabulaire des paramètres de population du jeu de révision et des autres, par exemple, le nombre de fichiers, le nombre estimé de fichiers pertinents, la richesse estimée et le coût moyen de la recherche d'un fichier supplémentaire pertinent.</span><span class="sxs-lookup"><span data-stu-id="a1124-118">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file.</span></span> <span data-ttu-id="a1124-119">Les paramètres de coût des paramètres peuvent être définis par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="a1124-119">Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="a1124-120">Ouvrez l' **onglet \> test de pertinence** .</span><span class="sxs-lookup"><span data-stu-id="a1124-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="a1124-121">Dans l'onglet **test** , cliquez sur **nouveau test**.</span><span class="sxs-lookup"><span data-stu-id="a1124-121">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="a1124-122">La boîte de dialogue **créer un test** s'affiche, comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a1124-122">The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Résultats de pertinence du test Tester les éléments restants](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="a1124-124">Dans **nom du test**et **Description**, tapez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="a1124-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="a1124-125">Dans la liste **type de test** , sélectionnez **tester le reste**</span><span class="sxs-lookup"><span data-stu-id="a1124-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="a1124-126">Dans la liste **problème/catégorie** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="a1124-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="a1124-127">Dans la liste **charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="a1124-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="a1124-128">En **lecture%**, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence de la limite.</span><span class="sxs-lookup"><span data-stu-id="a1124-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="a1124-129">Dans **définir la taille**, ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1124-129">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="a1124-130">Notez que les icônes de restauration restaureront les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1124-130">Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="a1124-131">Cliquez sur **Démarrer**le balisage.</span><span class="sxs-lookup"><span data-stu-id="a1124-131">Click **Start tagging**.</span></span> <span data-ttu-id="a1124-132">Un échantillon de test est généré.</span><span class="sxs-lookup"><span data-stu-id="a1124-132">A test sample is generated.</span></span>
    
10. <span data-ttu-id="a1124-133">Examinez et marquez chacun des fichiers dans l'onglet de la balise de \*\*pertinence \> \*\* et, lorsque vous avez fini, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="a1124-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="a1124-134">Sous l'onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="a1124-134">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="a1124-135">Un exemple est illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="a1124-135">An example is shown in the following figure.</span></span> 
    
    ![Résultats du test Tester les éléments restants](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="a1124-137">Dans la figure ci-dessus, la section **exemple de paramètres** du tableau contient des détails sur le nombre de fichiers dans l'exemple marqué par l'expert, ainsi que le nombre de fichiers pertinents trouvés dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a1124-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="a1124-138">La section **paramètres de remplissage** du tableau contient les résultats des tests, y compris le remplissage de l'ensemble des fichiers dont le score est inférieur à la limite sélectionnée et la population de fichiers Rest dont le score est supérieur à la limite sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a1124-138">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="a1124-139">Pour chaque population, les résultats suivants s'affichent:</span><span class="sxs-lookup"><span data-stu-id="a1124-139">For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="a1124-140">Inclut des fichiers dont la limite de lecture est% indiquée</span><span class="sxs-lookup"><span data-stu-id="a1124-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="a1124-141">Nombre total de fichiers</span><span class="sxs-lookup"><span data-stu-id="a1124-141">The total number of files</span></span> 
    
- <span data-ttu-id="a1124-142">Estimation du nombre de fichiers pertinents</span><span class="sxs-lookup"><span data-stu-id="a1124-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="a1124-143">La richesse estimée</span><span class="sxs-lookup"><span data-stu-id="a1124-143">The estimated richness</span></span> 
    
- <span data-ttu-id="a1124-144">Coût moyen de la recherche d'un autre fichier pertinent</span><span class="sxs-lookup"><span data-stu-id="a1124-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="a1124-145">Test du secteur</span><span class="sxs-lookup"><span data-stu-id="a1124-145">Testing the slice</span></span>

<span data-ttu-id="a1124-146">Le test «test the Slice» effectue un test semblable au test «test the Rest», mais à un segment de l'ensemble de fichiers, tel que spécifié par la pertinence% de lecture.</span><span class="sxs-lookup"><span data-stu-id="a1124-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="a1124-147">Ouvrez l' **onglet \> test de pertinence** .</span><span class="sxs-lookup"><span data-stu-id="a1124-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="a1124-148">Dans l'onglet **test** , cliquez sur **nouveau test**.</span><span class="sxs-lookup"><span data-stu-id="a1124-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="a1124-149">La boîte de dialogue **créer un test** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="a1124-149">The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="a1124-150">Dans **nom** et **Description**du test, entrez les informations.</span><span class="sxs-lookup"><span data-stu-id="a1124-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="a1124-151">Dans la liste **type de test** , sélectionnez **tester la section**.</span><span class="sxs-lookup"><span data-stu-id="a1124-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="a1124-152">Dans la liste **problème** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="a1124-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="a1124-153">Dans la liste **charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="a1124-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="a1124-154">En **lecture% entre**, acceptez les valeurs par défaut de plage basse et haute ou sélectionnez des valeurs pour les scores de pertinence de la limite.</span><span class="sxs-lookup"><span data-stu-id="a1124-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="a1124-155">Dans **définir la taille**, sélectionnez une valeur ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1124-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="a1124-156">Les icônes de restauration restaureront la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1124-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="a1124-157">Cliquez sur **Démarrer**le balisage.</span><span class="sxs-lookup"><span data-stu-id="a1124-157">Click **Start tagging**.</span></span> <span data-ttu-id="a1124-158">Un échantillon de test est généré.</span><span class="sxs-lookup"><span data-stu-id="a1124-158">A test sample is generated.</span></span>
    
10. <span data-ttu-id="a1124-159">Examinez et marquez chacun des fichiers dans l'onglet de la balise de \*\*pertinence \> \*\* et, lorsque vous avez fini, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="a1124-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="a1124-160">Sous l'onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="a1124-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a1124-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1124-161">See also</span></span>

[<span data-ttu-id="a1124-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a1124-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a1124-163">Présentation de l'évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="a1124-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1124-164">Balisage et évaluation</span><span class="sxs-lookup"><span data-stu-id="a1124-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1124-165">Étiquetage et formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="a1124-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1124-166">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="a1124-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a1124-167">Choix en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="a1124-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

