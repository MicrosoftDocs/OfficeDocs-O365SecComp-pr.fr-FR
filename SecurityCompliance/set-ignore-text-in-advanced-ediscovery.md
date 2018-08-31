---
title: Définir l’option Ignorer le texte pour l’analyse dans Office 365 avancée de découverte électronique
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
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Découvrez comment définir une règle pour ignorer un texte spécifique lors de l’utilisation les modules Analyse et processus d’eDiscovery Office 365 avancés.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528145"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="42700-103">Définir l’option Ignorer le texte pour l’analyse dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="42700-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="42700-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="42700-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="42700-p102">La fonctionnalité d’ignorer le texte peut être appliquée à tout ou partie des modules avancés eDiscovery suivants : analyser (près de doublons, les Threads de messagerie, des thèmes) et la pertinence. Texte ignoré n’apparaît pas dans les fichiers s’affichés dans la pertinence et l’analyse/calculs ignore le texte ignoré.</span><span class="sxs-lookup"><span data-stu-id="42700-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="42700-p103">Si la fonctionnalité d’ignorer le texte a été précédemment définie pour les modules que vous ont déjà exécuté, le paramètre ignorer le texte sera maintenant protégé d’être modifiée. Toutefois, la fonctionnalité d’ignorer le texte pour le module de la pertinence permettre toujours être modifiée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="42700-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="42700-110">L’application des filtres d’ignorer le texte</span><span class="sxs-lookup"><span data-stu-id="42700-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="42700-p104">Plusieurs texte ignorer les filtres sont appliqués dans l’ordre qu’ils ont été entrés. Pour modifier l’ordre dans lequel elles sont appliquées, ils doivent être supprimés et les données dans l’ordre souhaité.</span><span class="sxs-lookup"><span data-stu-id="42700-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="42700-113">Par exemple, si le contenu de texte est : « DAVE BOB ALICE CAROL veille », les éléments suivants sont des exemples d’entrées d’ignorer le texte et les résultats :</span><span class="sxs-lookup"><span data-stu-id="42700-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="42700-114">**Ignorer les entrées de texte**</span><span class="sxs-lookup"><span data-stu-id="42700-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="42700-115">**Résultats**</span><span class="sxs-lookup"><span data-stu-id="42700-115">**Results**</span></span> <br/> |
|<span data-ttu-id="42700-116">« ALICE », « BOB CAROL »</span><span class="sxs-lookup"><span data-stu-id="42700-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="42700-117">« DAVE VEILLE »</span><span class="sxs-lookup"><span data-stu-id="42700-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="42700-118">« ALICE », « BOB ALICE CAROL »</span><span class="sxs-lookup"><span data-stu-id="42700-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="42700-119">« DAVE BOB CAROL VEILLE »</span><span class="sxs-lookup"><span data-stu-id="42700-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="42700-120">La deuxième entrée d’ignorer le texte n’est pas implémentée, car la chaîne est introuvable en tant que telles après que le premier texte ignorer a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="42700-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="42700-121">Utiliser des expressions régulières lors de la définition d’ignorer le texte</span><span class="sxs-lookup"><span data-stu-id="42700-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="42700-p105">Expressions régulières sont prises en charge lors de la définition d’ignorer le texte. Voici des exemples de syntaxe d’expression régulière et l’utilisation :</span><span class="sxs-lookup"><span data-stu-id="42700-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="42700-124">Pour supprimer (ignorer) le texte à partir du début jusqu'à la fin d’une ligne :</span><span class="sxs-lookup"><span data-stu-id="42700-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="42700-125">où « Begin » est l’occurrence de cette chaîne dans la ligne initiale.</span><span class="sxs-lookup"><span data-stu-id="42700-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="42700-126">Par exemple, pour le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="42700-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="42700-127">**« Ceci est première phrase et la première ligne**</span><span class="sxs-lookup"><span data-stu-id="42700-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="42700-128">**Ceci est la deuxième phrase et la deuxième ligne »**</span><span class="sxs-lookup"><span data-stu-id="42700-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="42700-129">l’Expression régulière first(.\*) $ entraînera :</span><span class="sxs-lookup"><span data-stu-id="42700-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="42700-130">**« Ceci est**</span><span class="sxs-lookup"><span data-stu-id="42700-130">**"This is**</span></span>
    
    <span data-ttu-id="42700-131">**Ceci est la deuxième phrase et la deuxième ligne »**</span><span class="sxs-lookup"><span data-stu-id="42700-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="42700-132">Pour supprimer la responsabilité et instructions juridiques automatiquement insérées à la fin des threads de messagerie :</span><span class="sxs-lookup"><span data-stu-id="42700-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="42700-133">où « Begin » et « Fin » sont des chaînes uniques au début et fin d’un paragraphe de texte habillé.</span><span class="sxs-lookup"><span data-stu-id="42700-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="42700-134">Par exemple, l’expression régulière suivante supprimera responsabilité et instructions juridiques qui ont été dans le thread de messagerie entre les chaînes de début et de fin :</span><span class="sxs-lookup"><span data-stu-id="42700-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="42700-135">**Ce message contient des informations confidentielles (. | \s)\*si la vérification est requise demandez une version papier**</span><span class="sxs-lookup"><span data-stu-id="42700-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="42700-136">Pour supprimer une notification d’exclusion (y compris les caractères spéciaux) :</span><span class="sxs-lookup"><span data-stu-id="42700-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="42700-137">Par exemple, pour le texte suivant (avec la notification d’exclusion représenté par x) :</span><span class="sxs-lookup"><span data-stu-id="42700-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="42700-138">**/\*\ Ce message contient des informations confidentielles. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="42700-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="42700-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="42700-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="42700-140">\**xxxx xxxx si la vérification est requise, demandez une version papier. /\*\**</span><span class="sxs-lookup"><span data-stu-id="42700-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="42700-141">l’expression régulière à supprimer de la notification d’exclusion ci-dessus doit être :</span><span class="sxs-lookup"><span data-stu-id="42700-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="42700-142">**\/\\*\\Ce message contient des informations confidentielles\.(. | \s)\* si la vérification est requise demandez une version papier\.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="42700-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="42700-143">Règles de l’expression régulière :</span><span class="sxs-lookup"><span data-stu-id="42700-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="42700-144">Tous les caractères qui ne font pas partie de l’alphabet à l’exception des espaces, « _ » et «- » doit être précédé par «\".</span><span class="sxs-lookup"><span data-stu-id="42700-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="42700-145">Le champ eExpression régulière peut être une longueur illimitée.</span><span class="sxs-lookup"><span data-stu-id="42700-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="42700-146">Pour une explication et détaillées sur la syntaxe des expressions régulières, voir : [Langage des expressions régulières - référence rapide](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="42700-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="42700-147">Définir la règle d’ignorer le texte</span><span class="sxs-lookup"><span data-stu-id="42700-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="42700-148">Dans la **gérer \> analyse \> analyser les options** onglet, dans la section **Ignorer le texte** , cliquez sur le **+** icône pour ajouter une règle.</span><span class="sxs-lookup"><span data-stu-id="42700-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="42700-149">Dans la boîte de dialogue **Ajouter du texte ignorer** , dans le champ **nom** , tapez un nom pour la règle d’ignorer le texte.</span><span class="sxs-lookup"><span data-stu-id="42700-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Ajouter le texte ignoré](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="42700-p106">Dans la zone de **texte** , tapez le texte est ignoré. Le champ de texte permet à un nombre illimité de caractères.</span><span class="sxs-lookup"><span data-stu-id="42700-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="42700-153">Comme indiqué dans la fenêtre ci-dessus, cliquez sur l' **ampoule** pour afficher les indications de la règle de texte ignorer la syntaxe courantes.</span><span class="sxs-lookup"><span data-stu-id="42700-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="42700-154">Activez la case à cocher **respecter la casse** , si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="42700-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="42700-155">Dans la liste **appliquer à** , sélectionnez les modules avancés de découverte électronique à laquelle appliquer la définition.</span><span class="sxs-lookup"><span data-stu-id="42700-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="42700-p107">Si vous souhaitez une série de tests sur exemple de texte, tapez exemple de texte dans la zone de texte de **Saisie** , cliquez sur **tester**. Les résultats sont affichés dans la zone de texte de **sortie** .</span><span class="sxs-lookup"><span data-stu-id="42700-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="42700-p108">Cliquez sur **OK** pour enregistrer la règle d’ignorer le texte. La règle d’ignorer le texte définie est affichée.</span><span class="sxs-lookup"><span data-stu-id="42700-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![Définir le nom du texte ignoré](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="42700-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42700-161">See also</span></span>

[<span data-ttu-id="42700-162">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="42700-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="42700-163">Présentation de similarité de document</span><span class="sxs-lookup"><span data-stu-id="42700-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="42700-164">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="42700-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="42700-165">Analyse de la configuration des paramètres avancés</span><span class="sxs-lookup"><span data-stu-id="42700-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="42700-166">Affichage des résultats d’analyse</span><span class="sxs-lookup"><span data-stu-id="42700-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

