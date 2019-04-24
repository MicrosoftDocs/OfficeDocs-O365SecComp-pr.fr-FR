---
title: Définir l'option ignorer le texte pour l'analyse dans Office 365 Advanced eDiscovery
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
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: "Découvrez comment définir la règle pour ignorer le texte spécifique lors de l'utilisation des modules Analyze et process dans Office 365 Advanced eDiscovery.  "
ms.openlocfilehash: 3a4c1d17a9a56d3018509a8dcfd6b49abb951676
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260820"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Définir l'option ignorer le texte pour l'analyse dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
La fonctionnalité ignorer le texte peut être appliquée à tout ou partie des modules avancés eDiscovery suivants: Analyze (Near-Duplicates, threads de messagerie, thèmes) et pertinence. Le texte ignoré n'apparaît pas dans les fichiers affichés par pertinence, et l'analyse/les calculs ignorent le texte ignoré.
  
Si la fonctionnalité ignorer le texte a été précédemment définie pour les modules qui ont déjà été exécutés, le paramètre ignorer le texte est maintenant protégé de la modification. Toutefois, la fonctionnalité ignorer le texte pour le module de pertinence peut toujours être modifiée à tout moment.
  
## <a name="how-ignore-text-filters-are-applied"></a>Procédure d'application des filtres de texte

Les filtres de texte ignoré multiples sont appliqués dans l'ordre dans lequel ils ont été entrés. Pour modifier l'ordre dans lequel ils sont appliqués, vous devez les supprimer et les saisir à nouveau dans l'ordre souhaité.
  
Par exemple, si le contenu de texte est: «DAVE BOB ALICE CAROL veille», Voici des exemples d'entrées de texte ignorées et des résultats:
  
||||
|:-----|:-----|:-----|
|**Ignorer les entrées de texte** <br/> |**==\>** <br/> |**Results** <br/> |
|«ALICE», «BOB CAROL»  <br/> |==\>  <br/> |«DAVID RÉVEILLON»  <br/> |
|«ALICE», «BOB ALICE CAROL»  <br/> |==\>  <br/> |«DAVE BOB CAROL VEILLE»  <br/> |
   
La seconde entrée de texte ignorer n'est pas implémentée car la chaîne est introuvable comme telle après l'application du premier texte d'ignorer.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>Utiliser des expressions régulières lors de la définition d'un texte ignoré

Les expressions régulières sont prises en charge pour une utilisation lors de la définition d'un texte ignoré. Voici des exemples de syntaxe et d'utilisation des expressions régulières:
  
- Pour supprimer (ignorer) le texte début jusqu'à la fin d'une ligne:
    
     `Begin(.*)$`
    
    où «Begin» est l'occurrence initiale de cette chaîne dans la ligne.
    
    Par exemple, pour le texte suivant:
    
    **«Il s'agit de la première phrase et de la première ligne**
    
    **Il s'agit de la deuxième phrase et de la deuxième ligne»**
    
    première expression régulière (.\*) $ entraînera:
    
    **"Ceci est**
    
    **Il s'agit de la deuxième phrase et de la deuxième ligne»**
    
- Pour supprimer les clauses d'exclusion de responsabilité et les instructions légales insérées automatiquement à la fin des threads de messagerie:
    
     `Begin(.|\s)*End`
    
    où «Begin» et «end» sont des chaînes uniques au début et à la fin d'un paragraphe de texte renvoyé à la page. 
    
    Par exemple, l'expression régulière suivante supprime les clauses d'exclusion de responsabilité et les instructions légales qui se trouvaient dans le fil de messagerie entre les chaînes de début et de fin:
    
    **Ce message contient des informations confidentielles (. | \s)\*si la vérification est requise, demandez une version de copie papier.**
    
- Pour supprimer une clause d'exclusion de responsabilité (y compris des caractères spéciaux): 
    
    Par exemple, pour le texte suivant (avec la clause d'exclusion de responsabilité représentée par x): 
    
    **/\*\ Ce message contient des informations confidentielles. xxxx xxxx**
    
    **xxxx xxxx xxxx xxxx xxxx xxxx xxxx**
    
    **xxxx xxxx si la vérification est requise, demandez une version en copie papier. /\*\**
    
    l'expression régulière permettant de supprimer la clause d'exclusion de responsabilité ci-dessus doit être: 
    
    **\/\\*\\Ce message contient des informations\.confidentielles (. | \s)\* si la vérification est requise, demandez une version\. de copie papier.\/\\*\\**
    
- Règles d'expression régulière:
    
  - Tous les caractères qui ne font pas partie de l'alphabet, à l'exception de l'espace (s), «_» et «-»\", doivent être précédés de «.
    
  - Le champ eExpression normal peut avoir une longueur illimitée.
    
> [!TIP]
> Pour obtenir une explication et la syntaxe détaillée des expressions régulières, voir: [Regular Expression Language-aide-mémoire](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx). 
  
## <a name="define-ignore-text-rule"></a>Définir la règle de texte ignorer

1. Dans l' **onglet \> gérer \> ** l'analyse et les options, dans la section **Ignorer** le texte **+** , cliquez sur l'icône pour ajouter une règle. 
    
2. Dans la boîte de dialogue **Ajouter le texte ignorer** , dans le champ **nom** , tapez un nom pour la règle ignorer le texte. 
    
    ![Ajouter le texte ignoré](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. Dans la zone de **texte** , tapez le texte à ignorer. Le champ de texte autorise un nombre illimité de caractères. 
    
    > [!TIP]
    > Comme indiqué dans la fenêtre ci-dessus, cliquez sur **ampoule** pour afficher les instructions de syntaxe courantes pour la règle ignorer le texte. 
  
4. Activez la case à cocher **respecter la casse** , si vous le souhaitez. 
    
5. Dans la liste **appliquer à** , sélectionnez les modules avancés eDiscovery dans lesquels appliquer la définition. 
    
6. Si vous souhaitez une série de tests sur un exemple de texte, tapez exemple de texte dans la zone de texte de **saisie** , puis cliquez sur **test**. Les résultats s'affichent dans la zone de texte de **sortie** . 
    
7. Cliquez sur **OK** pour enregistrer la règle ignorer le texte. La règle de texte ignorer est affichée. 
    
    ![Définir le nom du texte ignoré](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de la similarité des documents](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définition des options d'analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Définition des paramètres avancés d'analyse](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Affichage des résultats de l'analyse](view-analyze-results-in-advanced-ediscovery.md)

