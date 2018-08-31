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
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Définir l’option Ignorer le texte pour l’analyse dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
La fonctionnalité d’ignorer le texte peut être appliquée à tout ou partie des modules avancés eDiscovery suivants : analyser (près de doublons, les Threads de messagerie, des thèmes) et la pertinence. Texte ignoré n’apparaît pas dans les fichiers s’affichés dans la pertinence et l’analyse/calculs ignore le texte ignoré.
  
Si la fonctionnalité d’ignorer le texte a été précédemment définie pour les modules que vous ont déjà exécuté, le paramètre ignorer le texte sera maintenant protégé d’être modifiée. Toutefois, la fonctionnalité d’ignorer le texte pour le module de la pertinence permettre toujours être modifiée à tout moment.
  
## <a name="how-ignore-text-filters-are-applied"></a>L’application des filtres d’ignorer le texte

Plusieurs texte ignorer les filtres sont appliqués dans l’ordre qu’ils ont été entrés. Pour modifier l’ordre dans lequel elles sont appliquées, ils doivent être supprimés et les données dans l’ordre souhaité.
  
Par exemple, si le contenu de texte est : « DAVE BOB ALICE CAROL veille », les éléments suivants sont des exemples d’entrées d’ignorer le texte et les résultats :
  
||||
|:-----|:-----|:-----|
|**Ignorer les entrées de texte** <br/> |**==\>** <br/> |**Résultats** <br/> |
|« ALICE », « BOB CAROL »  <br/> |==\>  <br/> |« DAVE VEILLE »  <br/> |
|« ALICE », « BOB ALICE CAROL »  <br/> |==\>  <br/> |« DAVE BOB CAROL VEILLE »  <br/> |
   
La deuxième entrée d’ignorer le texte n’est pas implémentée, car la chaîne est introuvable en tant que telles après que le premier texte ignorer a été appliqué.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>Utiliser des expressions régulières lors de la définition d’ignorer le texte

Expressions régulières sont prises en charge lors de la définition d’ignorer le texte. Voici des exemples de syntaxe d’expression régulière et l’utilisation :
  
- Pour supprimer (ignorer) le texte à partir du début jusqu'à la fin d’une ligne :
    
     `Begin(.*)$`
    
    où « Begin » est l’occurrence de cette chaîne dans la ligne initiale.
    
    Par exemple, pour le texte suivant :
    
    **« Ceci est première phrase et la première ligne**
    
    **Ceci est la deuxième phrase et la deuxième ligne »**
    
    l’Expression régulière first(.\*) $ entraînera :
    
    **« Ceci est**
    
    **Ceci est la deuxième phrase et la deuxième ligne »**
    
- Pour supprimer la responsabilité et instructions juridiques automatiquement insérées à la fin des threads de messagerie :
    
     `Begin(.|\s)*End`
    
    où « Begin » et « Fin » sont des chaînes uniques au début et fin d’un paragraphe de texte habillé. 
    
    Par exemple, l’expression régulière suivante supprimera responsabilité et instructions juridiques qui ont été dans le thread de messagerie entre les chaînes de début et de fin :
    
    **Ce message contient des informations confidentielles (. | \s)\*si la vérification est requise demandez une version papier**
    
- Pour supprimer une notification d’exclusion (y compris les caractères spéciaux) : 
    
    Par exemple, pour le texte suivant (avec la notification d’exclusion représenté par x) : 
    
    **/\*\ Ce message contient des informations confidentielles. xxxx xxxx**
    
    **xxxx xxxx xxxx xxxx xxxx xxxx xxxx**
    
    **xxxx xxxx si la vérification est requise, demandez une version papier. /\*\**
    
    l’expression régulière à supprimer de la notification d’exclusion ci-dessus doit être : 
    
    **\/\\*\\Ce message contient des informations confidentielles\.(. | \s)\* si la vérification est requise demandez une version papier\.\/\\*\\**
    
- Règles de l’expression régulière :
    
  - Tous les caractères qui ne font pas partie de l’alphabet à l’exception des espaces, « _ » et «- » doit être précédé par «\".
    
  - Le champ eExpression régulière peut être une longueur illimitée.
    
> [!TIP]
> Pour une explication et détaillées sur la syntaxe des expressions régulières, voir : [Langage des expressions régulières - référence rapide](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx). 
  
## <a name="define-ignore-text-rule"></a>Définir la règle d’ignorer le texte

1. Dans la **gérer \> analyse \> analyser les options** onglet, dans la section **Ignorer le texte** , cliquez sur le **+** icône pour ajouter une règle. 
    
2. Dans la boîte de dialogue **Ajouter du texte ignorer** , dans le champ **nom** , tapez un nom pour la règle d’ignorer le texte. 
    
    ![Ajouter le texte ignoré](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. Dans la zone de **texte** , tapez le texte est ignoré. Le champ de texte permet à un nombre illimité de caractères. 
    
    > [!TIP]
    > Comme indiqué dans la fenêtre ci-dessus, cliquez sur l' **ampoule** pour afficher les indications de la règle de texte ignorer la syntaxe courantes. 
  
4. Activez la case à cocher **respecter la casse** , si vous le souhaitez. 
    
5. Dans la liste **appliquer à** , sélectionnez les modules avancés de découverte électronique à laquelle appliquer la définition. 
    
6. Si vous souhaitez une série de tests sur exemple de texte, tapez exemple de texte dans la zone de texte de **Saisie** , cliquez sur **tester**. Les résultats sont affichés dans la zone de texte de **sortie** . 
    
7. Cliquez sur **OK** pour enregistrer la règle d’ignorer le texte. La règle d’ignorer le texte définie est affichée. 
    
    ![Définir le nom du texte ignoré](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Présentation de similarité de document](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définition des options d’analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Analyse de la configuration des paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Affichage des résultats d’analyse](view-analyze-results-in-advanced-ediscovery.md)

