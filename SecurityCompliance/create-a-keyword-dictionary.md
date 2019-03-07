---
title: Créer un dictionnaire de mots clés
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Pour identifier des informations sensibles, vous devrez parfois rechercher des mots clés, notamment pour identifier du contenu générique (par exemple, des communications liées au secteur de la santé) ou du langage inapproprié ou explicite. Vous pouvez créer des listes de mots clés dans les types d’informations sensibles, mais la taille de ces listes de mots clés est limitée, et vous devez modifier le code XML pour créer ou modifier ces listes. Les dictionnaires de mots clés simplifient la gestion des mots clés et, à plus grande échelle, permettent la prise en charge de 100 000 termes par dictionnaire.
ms.openlocfilehash: 6f0ca634e903509e9c0a92472501341eff7aa3fe
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454836"
---
# <a name="create-a-keyword-dictionary"></a>Créer un dictionnaire de mots clés

La protection contre la perte de données (DLP) dans Office 365 permet d’identifier, de surveiller et de protéger les informations sensibles. Pour identifier des informations sensibles, vous devrez parfois rechercher des mots clés, notamment pour identifier du contenu générique (par exemple, des communications liées au secteur de la santé) ou du langage inapproprié ou explicite. Vous pouvez créer des listes de mots clés dans les types d’informations sensibles, mais la taille de ces listes de mots clés est limitée, et vous devez modifier le code XML pour créer ou modifier ces listes. Les dictionnaires de mots clés simplifient la gestion des mots clés et à plus grande échelle, permettent la prise en charge de 100 000 termes par dictionnaire.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Étapes de base de la création d’un dictionnaire de mots clés

Les mots clés de votre dictionnaire peuvent provenir de diverses sources, le plus souvent d’un fichier (par exemple, comme une liste .csv ou .txt), d’une liste à laquelle vous accédez directement dans la cmdlet ou d’un dictionnaire existant. Lorsque vous créez un dictionnaire de mots clés, vous suivez les mêmes étapes fondamentales :
  
1. **Connexion au Centre de sécurité &amp; PowerShell** : consultez [cet article](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. **Définition ou chargement de vos mots clés à partir de la source prévue** : étant donné que la cmdlet permettant de créer un dictionnaire de mots clés accepte une liste de mots clés séparés par des virgules, cette étape varie légèrement en fonction de l’origine de vos mots clés. 
    
3. **Codage de vos mots clés** : une fois chargés, les mots clés sont convertis en un tableau d’octets avant d’être importés. 
    
4. **Création de votre dictionnaire** : choisissez un nom et une description, puis créez votre dictionnaire. 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a>Création d’un dictionnaire de mots clés à partir d’un fichier

Lorsque vous avez besoin de créer un dictionnaire volumineux, c’est souvent pour utiliser des mots clés d’un fichier ou d’une liste exportée à partir d’une autre source. Dans ce cas, créez un dictionnaire de mots clés contenant une liste de termes inappropriés à rechercher dans les e-mails externes. Vous devez d’abord vous [connecter au Centre de sécurité Office 365 &amp; conformité PowerShell](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
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

Vous devrez peut-être modifier les mots clés de l’un de vos dictionnaires de mots clés, ou modifier l’un des dictionnaires intégrés. Dans cet exemple, nous allons modifier certains termes dans PowerShell, enregistrer les termes localement pour que vous puissiez les modifier dans un éditeur, puis mettre à jour les termes précédents déjà en place. Tout d’abord, récupérez l’objet dictionnaire :
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

L’impression de `$dict` permet d’afficher les différentes variables. Les mots clés eux-mêmes sont stockés dans un objet sur le serveur principal, mais `$dict.KeywordDictionary` contient une représentation de chaîne de ceux-ci, que vous allez utiliser pour modifier le dictionnaire. Avant de modifier ce dernier, vous devez convertir la chaîne de termes en un tableau à l’aide de la méthode `.split(',')`. Ensuite, nettoyez les espaces indésirables entre les mots clés avec la méthode `.trim()` ; laissez uniquement les mots clés à utiliser. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

Vous allez maintenant supprimer certains termes du dictionnaire. Étant donné que l’exemple de dictionnaire ne contient que quelques mots clés, vous pourriez simplement passer directement à l’exportation et à la modification du dictionnaire dans le Bloc-notes, mais les dictionnaires contiennent généralement une grande quantité de texte. Vous allez donc découvrir d’abord cette méthode pour les modifier facilement dans PowerShell.
  
Dans la dernière étape, vous avez enregistré les mots clés dans un tableau. Il existe plusieurs façons de [supprimer des éléments dans un tableau](https://go.microsoft.com/fwlink/p/?linkid=852620), mais une approche simple consiste à créer un tableau des termes à supprimer du dictionnaire et à copier uniquement les termes dans celui-ci de dictionnaire qui ne figurent pas dans la liste des termes à supprimer.
  
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

Les dictionnaires de mots clés peuvent être utilisés dans le cadre de la configuration requise de recherche pour un type personnalisé d’informations sensibles ou en tant que type d’informations sensibles eux-mêmes. Les deux cas nécessitent la [création d’un type personnalisé d’informations sensibles dans le Centre de Conformité et Sécurité Office 365 PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Suivez les instructions dans l’article lié pour créer un type d’informations sensibles. Une fois que vous avez le fichier XML, vous aurez besoin de l’identificateur GUID du dictionnaire pour utiliser ce dernier.
  
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


