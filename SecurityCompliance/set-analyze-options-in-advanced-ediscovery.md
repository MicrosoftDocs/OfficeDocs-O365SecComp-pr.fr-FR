---
title: Définir les options d'analyse dans Office 365 Advanced eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Passez en revue les étapes de configuration des options pour le processus Analyze dans Office 365 Advanced eDiscovery, y compris les thèmes de quasi-duplication, les threads de messagerie et les thèmes.  '
ms.openlocfilehash: 4689638f5cebe2ef17fcea5a13ff06edc29e5930
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260890"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="0893a-103">Définir les options d'analyse dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0893a-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="0893a-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="0893a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="0893a-106">Dans Advanced eDiscovery, définissez les options d'analyse avant d'exécuter Analyze.</span><span class="sxs-lookup"><span data-stu-id="0893a-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="0893a-107">Définir les options d'analyse</span><span class="sxs-lookup"><span data-stu-id="0893a-107">Set Analyze options</span></span>

<span data-ttu-id="0893a-108">Ouvrez **Prepare prepare \> prepare** \*\*\*\* \> Setup.</span><span class="sxs-lookup"><span data-stu-id="0893a-108">Open **Prepare \> Analyze** \> **Setup**.</span></span> <span data-ttu-id="0893a-109">La fenêtre suivante s'affiche.</span><span class="sxs-lookup"><span data-stu-id="0893a-109">The following window is displayed.</span></span>
  
![Options Définir l’analyse](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="0893a-111">**Quasi-doublons et threads de messagerie** Activez cette case à coCher si vous souhaitez exécuter l'analyse.</span><span class="sxs-lookup"><span data-stu-id="0893a-111">**Near-duplicates and email threads** Check this box if you want to run the analysis.</span></span> <span data-ttu-id="0893a-112">Elle est sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="0893a-112">It is selected by default.</span></span> 
  
 <span data-ttu-id="0893a-113">**Similarité des documents** Entrez la valeur de seuil des quasi-doublons ou acceptez la valeur par défaut de 65%.</span><span class="sxs-lookup"><span data-stu-id="0893a-113">**Document similarity** Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="0893a-114">**Thèmes** Activez cette case à coCher pour traiter tous les fichiers et leur affecter des thèmes.</span><span class="sxs-lookup"><span data-stu-id="0893a-114">**Themes**Check this box to process all files and assign themes to them.</span></span> <span data-ttu-id="0893a-115">Par défaut, cette case à cocher n'est pas activée.</span><span class="sxs-lookup"><span data-stu-id="0893a-115">By default, this check box is not selected.</span></span> <span data-ttu-id="0893a-116">Entrez les options suivantes si vous souhaitez effectuer le traitement des thèmes.</span><span class="sxs-lookup"><span data-stu-id="0893a-116">Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="0893a-117">**Nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer.</span><span class="sxs-lookup"><span data-stu-id="0893a-117">**Max number of themes**Enter or select a value for the number of themes to create.</span></span> <span data-ttu-id="0893a-118">La valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="0893a-118">The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0893a-119">L'augmentation du nombre de thèmes a une incidence sur les performances, ainsi que sur la capacité d'un thème à généraliser.</span><span class="sxs-lookup"><span data-stu-id="0893a-119">Increasing the number of themes affects performance, as well as the ability of a theme to generalize.</span></span> <span data-ttu-id="0893a-120">Plus le nombre de thèmes est élevé, plus il est granulaire.</span><span class="sxs-lookup"><span data-stu-id="0893a-120">The higher the number of themes, the more granular they are.</span></span> <span data-ttu-id="0893a-121">Par exemple, si un jeu de thèmes 50 inclut un thème tel que «basket-ball, Spurs, déToureurs, Lakers»; 300 les thèmes peuvent inclure des thèmes distincts: «Spurs», «Clipper», «Lakers».</span><span class="sxs-lookup"><span data-stu-id="0893a-121">For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers".</span></span> <span data-ttu-id="0893a-122">Si vous n'avez pas conscience du thème «basket» et si vous utilisez cette fonctionnalité pour ECA, voir le thème «basket» peut être utile.</span><span class="sxs-lookup"><span data-stu-id="0893a-122">If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful.</span></span> <span data-ttu-id="0893a-123">Toutefois, si le traitement avait trop de thèmes, il se peut que vous ne trouviez jamais le mot «basket-ball» et que des Spurs et des déCoupages soient des thèmes de basket-ball intéressants à consulter, plutôt que des éléments qui se trouvent sur les bottes et utilisés pour les cheveux.</span><span class="sxs-lookup"><span data-stu-id="0893a-123">But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="0893a-124">**Thèmes suggérés** Vous pouvez suggérer des mots de thème pour contrôler le traitement des thèmes.</span><span class="sxs-lookup"><span data-stu-id="0893a-124">**Suggested themes** You can suggest theme words to control Themes processing.</span></span> <span data-ttu-id="0893a-125">Advanced eDiscovery se concentrera sur ces suggestions de mots et tentera de créer un ou plusieurs thèmes pertinents, en fonction des paramètres «nombre maximal de thèmes».</span><span class="sxs-lookup"><span data-stu-id="0893a-125">Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="0893a-126">Par exemple, si le mot suggéré est «ordinateur» et que vous avez spécifié «2» comme «nombre maximal de thèmes», Advanced eDiscovery essaiera de générer deux thèmes liés au mot «ordinateur».</span><span class="sxs-lookup"><span data-stu-id="0893a-126">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer".</span></span> <span data-ttu-id="0893a-127">Les deux thèmes peuvent être «logiciels informatiques» et «matériel informatique», par exemple.</span><span class="sxs-lookup"><span data-stu-id="0893a-127">The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="0893a-129">Pour afficher, ajouter ou modifier des thèmes suggérés, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="0893a-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="0893a-130">Dans le panneau **thèmes suggérés** , cliquez sur l'icône](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) **Ajouter** ![une icône Ajouter pour ajouter un thème.</span><span class="sxs-lookup"><span data-stu-id="0893a-130">In the **Suggested themes** panel, click the **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme.</span></span> <span data-ttu-id="0893a-131">Dans le panneau **Ajouter un thème suggéré** , ajoutez les mots, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="0893a-131">In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="0893a-132">Dans **nombre de thèmes**, sélectionnez une valeur pour déterminer le nombre de thèmes que la fonctionnalité eDiscovery avancée essaiera de générer pour ces mots (la valeur par défaut est 1 thème).</span><span class="sxs-lookup"><span data-stu-id="0893a-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="0893a-133">Cliquez sur **Enregistrer** , puis fermez la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0893a-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0893a-134">Le nombre total de thèmes inclut les thèmes suggérés.</span><span class="sxs-lookup"><span data-stu-id="0893a-134">The total number of themes includes Suggested Themes.</span></span> <span data-ttu-id="0893a-135">Le total des thèmes suggérés ne peut pas dépasser le nombre total de thèmes.</span><span class="sxs-lookup"><span data-stu-id="0893a-135">The total Suggested Themes cannot exceed the total themes.</span></span> <span data-ttu-id="0893a-136">S'il existe de nombreux thèmes suggérés par rapport au nombre total de thèmes, seuls quelques «nouveaux» thèmes seront détectés par le système, car la plupart des thèmes seront dédiés aux thèmes suggérés.</span><span class="sxs-lookup"><span data-stu-id="0893a-136">If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="0893a-137">**Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** :</span><span class="sxs-lookup"><span data-stu-id="0893a-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="0893a-138">**Créer et appliquer un modèle**: calcule les thèmes par modèles à partir d'un segment des fichiers, puis distribue les fichiers entre eux.</span><span class="sxs-lookup"><span data-stu-id="0893a-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="0893a-139">**Créer un modèle**: calcule un modèle de thèmes à partir d'un segment des fichiers.</span><span class="sxs-lookup"><span data-stu-id="0893a-139">**Create model**: Calculates a themes model from a segment of the files.</span></span> <span data-ttu-id="0893a-140">Le processus d'application de la Division des fichiers est réalisé séparément à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="0893a-140">The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="0893a-141">**Appliquer le modèle**: cette option n'est visible que si un modèle a été créé précédemment et n'a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="0893a-141">**Apply model**: This option is only shown if a model was created previously and not yet applied.</span></span> <span data-ttu-id="0893a-142">Cela permet de diviser les fichiers en fonction des thèmes.</span><span class="sxs-lookup"><span data-stu-id="0893a-142">This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="0893a-143">Vous pouvez également [définir ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) et [définir les paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md) d'analyse pour l'analyse.</span><span class="sxs-lookup"><span data-stu-id="0893a-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="0893a-144">Après avoir défini ces options, cliquez sur **analyser** pour exécuter.</span><span class="sxs-lookup"><span data-stu-id="0893a-144">After you've set these options, click **Analyze** to run.</span></span> <span data-ttu-id="0893a-145">[Afficher les résultats](view-analyze-results-in-advanced-ediscovery.md) de l'analyse sont affichés.</span><span class="sxs-lookup"><span data-stu-id="0893a-145">[View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0893a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0893a-146">See also</span></span>

[<span data-ttu-id="0893a-147">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0893a-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0893a-148">Présentation de la similarité des documents</span><span class="sxs-lookup"><span data-stu-id="0893a-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0893a-149">Définir le texte ignoré</span><span class="sxs-lookup"><span data-stu-id="0893a-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0893a-150">Paramètres avancés Définir l’analyse</span><span class="sxs-lookup"><span data-stu-id="0893a-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0893a-151">Afficher les résultats de l'analyse</span><span class="sxs-lookup"><span data-stu-id="0893a-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

