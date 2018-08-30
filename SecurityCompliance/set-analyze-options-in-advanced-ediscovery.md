---
title: Définir les options d’analyse dans Office 365 avancée de découverte électronique
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Passez en revue les étapes pour configurer les options pour le processus d’analyse d’Office 365 avancée eDiscovery, y compris près de doublons, les threads de messagerie et des thèmes.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528093"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="a2796-103">Définir les options d’analyse dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="a2796-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="a2796-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a2796-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a2796-106">Dans Paramètres avancés eDiscovery, définissez les options d’analyse avant d’exécuter l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a2796-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="a2796-107">Définir les options d’analyse</span><span class="sxs-lookup"><span data-stu-id="a2796-107">Set Analyze options</span></span>

<span data-ttu-id="a2796-p102">Open **préparer \> analyser** \> **le programme d’installation**. La fenêtre suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a2796-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Options Définir l’analyse](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="a2796-p103">**Près de doublons et les threads de messagerie** Cette case à cocher si vous souhaitez exécuter l’analyse. Il est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2796-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="a2796-113">**Similarité de document** Entrez la valeur de seuil des doublons Near ou acceptez la valeur par défaut de 65 %.</span><span class="sxs-lookup"><span data-stu-id="a2796-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="a2796-p104">**Thèmes** Cochez cette case pour traiter tous les fichiers et leur attribuer des thèmes. Par défaut, cette case à cocher n’est pas sélectionnée. Entrez les options suivantes si vous souhaitez effectuer des thèmes de traitement.</span><span class="sxs-lookup"><span data-stu-id="a2796-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="a2796-p105">**Nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="a2796-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="a2796-p106">Augmentation du nombre de thèmes affecte les performances, ainsi que la capacité d’un thème pour généraliser. Plus le nombre de thèmes, le plus granulaires, ils se trouvent. Par exemple, si un ensemble de 50 thèmes include un thème tels que « Basketball, rapide, pince, Lakers » ; 300 thèmes peuvent inclure des thèmes distincts : « Incite », « TONDEUSE », « Lakers ». Si vous n’avez aucune prise de conscience du thème « Basketball » et que vous utilisez cette fonctionnalité pour ECA, voir le thème « Basketball » peut être utile. Mais, si le traitement a un trop grand nombre de thèmes, vous visualiserez jamais le mot « Basketball » et peut ne pas savez que rapide et tondeuse est bonnes thèmes Basketball pour passer en revue, au lieu d’articles qui passent sur démarre et utilisés pour cheveux.</span><span class="sxs-lookup"><span data-stu-id="a2796-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="a2796-p107">**Thèmes suggérés** Vous pouvez proposer des mots de thème pour contrôler le traitement des thèmes. Découverte avancée sera se concentrer sur ces mots suggérés et essayez de créer un ou plusieurs thèmes pertinents, en fonction des paramètres « Max nombre de thèmes ».</span><span class="sxs-lookup"><span data-stu-id="a2796-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="a2796-p108">Par exemple, si le mot suggéré est « computer », et vous avez spécifié « 2 » comme « nombre maximal de thèmes », eDiscovery avancée essaiera générer des thèmes de deux qui sont associées au mot « computer ». Les deux thèmes est « logiciel » et « matériel informatique », par exemple.</span><span class="sxs-lookup"><span data-stu-id="a2796-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="a2796-129">Pour afficher, ajouter ou modifier des thèmes suggérées, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="a2796-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="a2796-p109">Dans le panneau de configuration **des thèmes suggérés** , cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icône pour ajouter un thème. Dans le volet **Ajouter suggérée thème** , ajoutez les mots, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="a2796-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="a2796-132">Dans **nombre de thèmes**, sélectionnez une valeur pour déterminer le nombre de thèmes eDiscovery avancée essaieront de générer ces termes (valeur par défaut est 1 thème).</span><span class="sxs-lookup"><span data-stu-id="a2796-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="a2796-133">Cliquez sur **Enregistrer** , puis fermez la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a2796-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="a2796-p110">Le nombre total de thèmes inclut des thèmes suggéré. Les thèmes suggérés total ne peut pas dépasser les thèmes total. S’il existe de nombreux thèmes suggérée par rapport aux thèmes total, uniquement quelques thèmes de « nouveau » seront détectés par le système, car la plupart des thèmes sera consacrée aux thèmes suggéré.</span><span class="sxs-lookup"><span data-stu-id="a2796-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="a2796-137">**Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** :</span><span class="sxs-lookup"><span data-stu-id="a2796-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="a2796-138">**Créer et appliquer le modèle**: calcule des thèmes par les modèles d’un segment des fichiers et puis distribue les fichiers entre eux.</span><span class="sxs-lookup"><span data-stu-id="a2796-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="a2796-p111">**Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers. Le processus d’appliquer de la division de fichiers s’effectue séparément à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="a2796-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="a2796-p112">**Appliquer modèle**: cette option ne s’affiche que si un modèle a été créé précédemment et n’est pas encore appliqué. Il divise les fichiers selon les thèmes.</span><span class="sxs-lookup"><span data-stu-id="a2796-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="a2796-143">Vous pouvez également [définir ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) et [définir Analyze paramètres avancé](set-analyze-advanced-settings-in-advanced-ediscovery.md) pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a2796-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="a2796-p113">Une fois que vous avez défini ces options, cliquez sur **analyse** à exécuter. [Affichage analyser les résultats](view-analyze-results-in-advanced-ediscovery.md) sont affichés.</span><span class="sxs-lookup"><span data-stu-id="a2796-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2796-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2796-146">See also</span></span>

[<span data-ttu-id="a2796-147">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="a2796-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a2796-148">Présentation de similarité de document</span><span class="sxs-lookup"><span data-stu-id="a2796-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a2796-149">Définir le texte de la case à cocher Ignorer</span><span class="sxs-lookup"><span data-stu-id="a2796-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a2796-150">Paramètres avancés Définir l’analyse</span><span class="sxs-lookup"><span data-stu-id="a2796-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a2796-151">Afficher les résultats d’analyse</span><span class="sxs-lookup"><span data-stu-id="a2796-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

