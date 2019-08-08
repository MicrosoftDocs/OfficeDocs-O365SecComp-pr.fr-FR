---
title: Créer un dictionnaire de mots clés
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/11/2019
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Pour identifier des informations sensibles, vous devrez parfois rechercher des mots clés, notamment pour identifier du contenu générique (par exemple, des communications liées au secteur de la santé) ou du langage inapproprié ou explicite. Vous pouvez créer des listes de mots clés dans les types d’informations sensibles, mais la taille de ces listes de mots clés est limitée, et vous devez modifier le code XML pour créer ou modifier ces listes. Les dictionnaires de mots clés simplifient la gestion des mots clés et, à plus grande échelle, permettent la prise en charge de 100 000 termes par dictionnaire.
ms.openlocfilehash: 5e99cad328115ad6b49982ea4c5749cdea6e43ed
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230788"
---
# <a name="create-a-keyword-dictionary"></a>Créer un dictionnaire de mots clés

La protection contre la perte de données (DLP) dans Office 365 peut identifier, surveiller et protéger vos informations sensibles. L’identification des informations sensibles nécessite parfois la recherche de mots clés, notamment lors de l’identification de contenu générique (par exemple, la communication liée aux soins de santé) ou d’une langue inappropriée ou explicite. Bien que vous puissiez créer des listes de mots clés dans des types d’informations sensibles, les listes de mots clés sont limitées en taille et nécessitent la modification du code XML pour les créer ou les modifier. Les dictionnaires de mots clés facilitent la gestion des mots-clés et à une échelle plus grande, prenant en charge jusqu’à 100 000 termes par dictionnaire.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Étapes de base de la création d’un dictionnaire de mots clés

Les mots clés de votre dictionnaire peuvent provenir de diverses sources, le plus souvent d’un fichier (par exemple, une liste .csv ou .txt) importé dans le service ou par cmdlet PowerShell, d’une liste à laquelle vous accédez directement dans la cmdlet PowerShell ou d’un dictionnaire existant. Lorsque vous créez un dictionnaire de mots clés, vous suivez les mêmes étapes fondamentales :
  
1. Utilisez le **Centre de sécurité & conformité** ([https://protection.office.com](https://protection.office.com)) ou connectez-vous au **Centre de &amp; sécurité conformité Office 365**.
    
2. **Définissez ou chargez vos mots clés à partir de la source voulue**. L’Assistant et l’applet de commande acceptent une liste de mots clés séparés par des virgules pour créer un dictionnaire de mots clés personnalisé, de sorte que cette étape varie légèrement en fonction de l’emplacement d’origine de vos mots-clés. Une fois chargés, les mots clés sont encodés et convertis en un tableau d’octets avant d’être importés.
    
3. **Créez votre dictionnaire**. Choisissez un nom et une description, puis créez votre dictionnaire.

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a>Créer un dictionnaire de mots clés à l’aide du centre de sécurité & conformité

Procédez comme suit pour créer et importer des mots clés pour un dictionnaire personnalisé :

1. Connectez-vous au centre de sécurité &[https://protection.office.com](https://protection.office.com)conformité ().

2. Accédez à **Classifications > Types d’informations sensibles**.

3. Sélectionnez **Créer** et entrez un **Nom** et une **Description** pour votre type d’informations sensibles, puis sélectionnez **Suivant**

4. Sélectionnez **Ajouter un élément**, puis sélectionnez **Dictionnaire (grands mots clés)** dans la liste déroulante **Détecter le contenu contenant**.

5. Sélectionnez **Ajouter un dictionnaire**

6. Sous le Contrôle de recherche, sélectionnez **Vous pouvez créer de nouveaux dictionnaires de mots clés ici**.

7. Entrez un **Nom** pour votre dictionnaire personnalisé.

8. Sélectionnez **Importer**, puis sélectionnez **À partir d’un fichier texte** ou **À partir d’un fichier CSV** selon votre type de fichier de mots clés.

9. Dans la boîte de dialogue du fichier, sélectionnez le fichier de mots clés sur votre PC local ou sur votre partage de fichiers réseau, puis sélectionnez **Ouvrir**.

10. Sélectionnez **Enregistrer**, puis sélectionnez votre dictionnaire personnalisé dans la liste **Dictionnaires de mots clés**.

11. Sélectionnez **Ajouter**, puis **Suivant**.

12. Passez en revue et finalisez vos sélections de type d’informations sensibles, puis sélectionnez **Terminer**.
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a>Création d’un dictionnaire de mots clés à partir d’un fichier avec PowerShell

Lorsque vous avez besoin de créer un dictionnaire volumineux, il est souvent nécessaire d’utiliser des mots clés à partir d’un fichier ou d’une liste exportée à partir d’une autre source. Dans ce cas, vous allez créer un dictionnaire de mots clés contenant une liste de langues inappropriées à l’écran dans le courrier électronique externe. Vous devez d’abord vous [connecter au centre &amp; de sécurité conformité d’Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
1. Copiez les mots clés dans un fichier texte et assurez-vous que chaque mot clé est sur une ligne distincte.
    
2. Enregistrez le fichier texte avec le codage Unicode. Dans le Bloc-notes \> **Enregistrer sous** \> **Codage** \> **Unicode**.
    
3. Lisez le fichier dans une variable en exécutant la cmdlet suivante :
    
    ```
    $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
    ```

4. Créez le dictionnaire en exécutant la cmdlet suivante :
    
    ```
    New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
    ```

## <a name="modifying-an-existing-keyword-dictionary"></a>Modification d’un dictionnaire de mots clés existant

Vous devrez peut-être modifier des mots clés dans l’un de vos dictionnaires de mots clés ou modifier l’un des dictionnaires intégrés. Pour l’instant, vous ne pouvez mettre à jour qu’un dictionnaire de mots clés personnalisé avec PowerShell. 

Par exemple, nous allons modifier certains termes dans PowerShell, enregistrer les termes localement où vous pouvez les modifier dans un éditeur, puis mettre à jour les termes précédents en place. 

Tout d’abord, récupérez l’objet Dictionary :
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

L' `$dict` impression affiche les différentes variables. Les mots-clés eux-mêmes sont stockés dans un objet sur `$dict.KeywordDictionary` le serveur principal, mais ils contiennent une représentation sous forme de chaîne de ceux-ci, que vous utiliserez pour modifier le dictionnaire. 

Avant de modifier le dictionnaire, vous devez réactiver la chaîne de termes dans un tableau à l' `.split(',')` aide de la méthode. Ensuite, vous allez nettoyer les espaces indésirables entre les mots clés à `.trim()` l’aide de la méthode, en ne laissant que les mots clés à utiliser. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

Vous allez maintenant supprimer certains termes du dictionnaire. Étant donné que l’exemple de dictionnaire ne contient que quelques mots clés, vous pourriez simplement passer directement à l’exportation et à la modification du dictionnaire dans le Bloc-notes, mais les dictionnaires contiennent généralement une grande quantité de texte. Vous allez donc découvrir d’abord cette méthode pour les modifier facilement dans PowerShell.
  
Dans la dernière étape, vous avez enregistré les mots clés dans un tableau. Il existe plusieurs façons de [supprimer des éléments dans un tableau](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), mais une approche simple consiste à créer un tableau des termes à supprimer du dictionnaire et à copier uniquement les termes dans celui-ci de dictionnaire qui ne figurent pas dans la liste des termes à supprimer.
  
Exécutez la commande `$terms` pour afficher la liste actuelle des termes. La sortie de la commande se présente comme suit : 
  
```
aarskog's syndrome
abandonment
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipoproteinemia
abiotrophy
ablatio
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Exécutez cette commande pour spécifier les termes à supprimer :
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

Exécutez cette commande pour supprimer réellement les termes de la liste :
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

Exécutez la commande `$updatedTerms` pour afficher la liste mise à jour des termes. La sortie de la commande se présente comme suit (les termes spécifiés ont été supprimés) : 
  
```
aarskog's syndrome
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipo proteinemia
abiotrophy
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Enregistrez maintenant le dictionnaire localement et ajoutez quelques termes supplémentaires. Vous pourriez ajouter les termes ici dans PowerShell, mais vous devrez quand même exporter le fichier localement pour vous assurer qu’il a été enregistré avec le codage Unicode et qu’il contient la marque BOM.
  
Exécutez la commande suivante pour enregistrer le dictionnaire localement :
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

À présent, ouvrez simplement le fichier, ajoutez les termes supplémentaires et enregistrez-le avec le codage Unicode (UTF-16). Chargez ensuite les termes mis à jour et mettez à jour le dictionnaire en place.
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

Le dictionnaire a été mis à jour. Notez que le champ `Identity` prend le nom du dictionnaire. Si vous vouliez également modifier le nom de votre dictionnaire à l’aide la cmdlet `set-`, vous n’aviez qu’à ajouter le paramètre `-Name` au-dessus avec le nouveau nom de votre dictionnaire. 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a>Utilisation des dictionnaires de mots clés dans les types d’informations sensibles personnalisés et les stratégies DLP

Les dictionnaires de mots clés peuvent être utilisés dans le cadre des exigences de correspondance pour un type d’informations sensibles personnalisé, ou comme un type d’informations sensibles proprement dit. Ces deux conditions vous obligent à créer un [type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type-in-scc-powershell.md). Suivez les instructions de l’article lié pour créer un type d’informations sensibles. Une fois que vous avez le fichier XML, vous aurez besoin de l’identificateur de GUID pour le dictionnaire pour pouvoir l’utiliser.
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

Pour obtenir l’identité de votre dictionnaire, exécutez la commande suivante et copiez la valeur de la propriété **Identité** : 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

Le résultat de la commande ressemble à ceci :
  
```
RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255
Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f
Name              : Diseases
Description       : Names of diseases and injuries from ICD-10-CM lexicon
KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo
                    proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,
                    abrami's disease, abramo
IsValid           : True
ObjectState       : Unchanged
```

Collez l’identité dans le code XML de votre type personnalisé d’informations sensibles et chargez-le. Votre dictionnaire s’affiche désormais dans votre liste de types d’informations sensibles et vous pouvez l’utiliser directement dans votre stratégie en indiquant le nombre de mots clés qui doivent correspondre.
  
```
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```


