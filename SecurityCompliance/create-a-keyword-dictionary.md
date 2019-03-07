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
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="5ac08-105">Créer un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="5ac08-105">Create a keyword dictionary</span></span>

<span data-ttu-id="5ac08-p102">La protection contre la perte de données (DLP) dans Office 365 permet d’identifier, de surveiller et de protéger les informations sensibles. Pour identifier des informations sensibles, vous devrez parfois rechercher des mots clés, notamment pour identifier du contenu générique (par exemple, des communications liées au secteur de la santé) ou du langage inapproprié ou explicite. Vous pouvez créer des listes de mots clés dans les types d’informations sensibles, mais la taille de ces listes de mots clés est limitée, et vous devez modifier le code XML pour créer ou modifier ces listes. Les dictionnaires de mots clés simplifient la gestion des mots clés et à plus grande échelle, permettent la prise en charge de 100 000 termes par dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p102">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information. Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication) or inappropriate or explicit language. While you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them. Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="5ac08-110">Étapes de base de la création d’un dictionnaire de mots clés</span><span class="sxs-lookup"><span data-stu-id="5ac08-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="5ac08-p103">Les mots clés de votre dictionnaire peuvent provenir de diverses sources, le plus souvent d’un fichier (par exemple, comme une liste .csv ou .txt), d’une liste à laquelle vous accédez directement dans la cmdlet ou d’un dictionnaire existant. Lorsque vous créez un dictionnaire de mots clés, vous suivez les mêmes étapes fondamentales :</span><span class="sxs-lookup"><span data-stu-id="5ac08-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list), from a list you enter directly in the cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="5ac08-113">**Connexion au Centre de sécurité &amp; PowerShell** : consultez [cet article](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="5ac08-113">**Connect to Security &amp; Compliance Center PowerShell** - see [this topic](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="5ac08-114">**Définition ou chargement de vos mots clés à partir de la source prévue** : étant donné que la cmdlet permettant de créer un dictionnaire de mots clés accepte une liste de mots clés séparés par des virgules, cette étape varie légèrement en fonction de l’origine de vos mots clés.</span><span class="sxs-lookup"><span data-stu-id="5ac08-114">**Define or load your keywords from your intended source** - the cmdlet to create a keyword dictionary accepts a comma-separated list of keywords, so this step will vary slightly depending on where your keywords come from.</span></span> 
    
3. <span data-ttu-id="5ac08-115">**Codage de vos mots clés** : une fois chargés, les mots clés sont convertis en un tableau d’octets avant d’être importés.</span><span class="sxs-lookup"><span data-stu-id="5ac08-115">**Encode your keywords** - once loaded, they're converted to a byte array before they're imported.</span></span> 
    
4. <span data-ttu-id="5ac08-116">**Création de votre dictionnaire** : choisissez un nom et une description, puis créez votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="5ac08-116">**Create your dictionary** - choose a name and description and create your dictionary.</span></span> 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a><span data-ttu-id="5ac08-117">Création d’un dictionnaire de mots clés à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="5ac08-117">Create a keyword dictionary from a file</span></span>

<span data-ttu-id="5ac08-p104">Lorsque vous avez besoin de créer un dictionnaire volumineux, c’est souvent pour utiliser des mots clés d’un fichier ou d’une liste exportée à partir d’une autre source. Dans ce cas, créez un dictionnaire de mots clés contenant une liste de termes inappropriés à rechercher dans les e-mails externes. Vous devez d’abord vous [connecter au Centre de sécurité Office 365 &amp; conformité PowerShell](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="5ac08-p104">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source. In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email. You need to first [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/fr-FR/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="5ac08-121">Copiez les mots clés dans un fichier texte et assurez-vous que chaque mot clé est sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="5ac08-121">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="5ac08-p105">Enregistrez le fichier texte avec le codage Unicode. Dans le Bloc-notes \> **Enregistrer sous** \> **Codage** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p105">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="5ac08-124">Lisez le fichier dans une variable en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="5ac08-124">Read the file into a variable by running this cmdlet:</span></span>
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. <span data-ttu-id="5ac08-125">Créez le dictionnaire en exécutant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="5ac08-125">Create the dictionary by running this cmdlet:</span></span>
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="5ac08-126">Modification d’un dictionnaire de mots clés existant</span><span class="sxs-lookup"><span data-stu-id="5ac08-126">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="5ac08-p106">Vous devrez peut-être modifier les mots clés de l’un de vos dictionnaires de mots clés, ou modifier l’un des dictionnaires intégrés. Dans cet exemple, nous allons modifier certains termes dans PowerShell, enregistrer les termes localement pour que vous puissiez les modifier dans un éditeur, puis mettre à jour les termes précédents déjà en place. Tout d’abord, récupérez l’objet dictionnaire :</span><span class="sxs-lookup"><span data-stu-id="5ac08-p106">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries. In this example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place. First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="5ac08-p107">L’impression de `$dict` permet d’afficher les différentes variables. Les mots clés eux-mêmes sont stockés dans un objet sur le serveur principal, mais `$dict.KeywordDictionary` contient une représentation de chaîne de ceux-ci, que vous allez utiliser pour modifier le dictionnaire. Avant de modifier ce dernier, vous devez convertir la chaîne de termes en un tableau à l’aide de la méthode `.split(',')`. Ensuite, nettoyez les espaces indésirables entre les mots clés avec la méthode `.trim()` ; laissez uniquement les mots clés à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p107">Printing  `$dict` will show the various variables. The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary. Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method. Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="5ac08-p108">Vous allez maintenant supprimer certains termes du dictionnaire. Étant donné que l’exemple de dictionnaire ne contient que quelques mots clés, vous pourriez simplement passer directement à l’exportation et à la modification du dictionnaire dans le Bloc-notes, mais les dictionnaires contiennent généralement une grande quantité de texte. Vous allez donc découvrir d’abord cette méthode pour les modifier facilement dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p108">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="5ac08-p109">Dans la dernière étape, vous avez enregistré les mots clés dans un tableau. Il existe plusieurs façons de [supprimer des éléments dans un tableau](https://go.microsoft.com/fwlink/p/?linkid=852620), mais une approche simple consiste à créer un tableau des termes à supprimer du dictionnaire et à copier uniquement les termes dans celui-ci de dictionnaire qui ne figurent pas dans la liste des termes à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p109">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://go.microsoft.com/fwlink/p/?linkid=852620), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="5ac08-p110">Exécutez la commande `$terms` pour afficher la liste actuelle des termes. La sortie de la commande se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="5ac08-p110">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="5ac08-140">Exécutez cette commande pour spécifier les termes à supprimer :</span><span class="sxs-lookup"><span data-stu-id="5ac08-140">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="5ac08-141">Exécutez cette commande pour supprimer réellement les termes de la liste :</span><span class="sxs-lookup"><span data-stu-id="5ac08-141">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="5ac08-p111">Exécutez la commande `$updatedTerms` pour afficher la liste mise à jour des termes. La sortie de la commande se présente comme suit (les termes spécifiés ont été supprimés) :</span><span class="sxs-lookup"><span data-stu-id="5ac08-p111">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="5ac08-p112">Enregistrez maintenant le dictionnaire localement et ajoutez quelques termes supplémentaires. Vous pourriez ajouter les termes ici dans PowerShell, mais vous devrez quand même exporter le fichier localement pour vous assurer qu’il a été enregistré avec le codage Unicode et qu’il contient la marque BOM.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p112">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="5ac08-146">Exécutez la commande suivante pour enregistrer le dictionnaire localement :</span><span class="sxs-lookup"><span data-stu-id="5ac08-146">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="5ac08-p113">À présent, ouvrez simplement le fichier, ajoutez les termes supplémentaires et enregistrez-le avec le codage Unicode (UTF-16). Chargez ensuite les termes mis à jour et mettez à jour le dictionnaire en place.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p113">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="5ac08-p114">Le dictionnaire a été mis à jour. Notez que le champ `Identity` prend le nom du dictionnaire. Si vous vouliez également modifier le nom de votre dictionnaire à l’aide la cmdlet `set-`, vous n’aviez qu’à ajouter le paramètre `-Name` au-dessus avec le nouveau nom de votre dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p114">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="5ac08-152">Utilisation des dictionnaires de mots clés dans les types d’informations sensibles personnalisés et les stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="5ac08-152">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="5ac08-p115">Les dictionnaires de mots clés peuvent être utilisés dans le cadre de la configuration requise de recherche pour un type personnalisé d’informations sensibles ou en tant que type d’informations sensibles eux-mêmes. Les deux cas nécessitent la [création d’un type personnalisé d’informations sensibles dans le Centre de Conformité et Sécurité Office 365 PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Suivez les instructions dans l’article lié pour créer un type d’informations sensibles. Une fois que vous avez le fichier XML, vous aurez besoin de l’identificateur GUID du dictionnaire pour utiliser ce dernier.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p115">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves. Both require [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Follow the instructions in the linked article to create a sensitive information type. Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="5ac08-157">Pour obtenir l’identité de votre dictionnaire, exécutez la commande suivante et copiez la valeur de la propriété **Identité** :</span><span class="sxs-lookup"><span data-stu-id="5ac08-157">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="5ac08-158">Le résultat de la commande ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="5ac08-158">The output of the command looks like this:</span></span>
  
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

<span data-ttu-id="5ac08-p116">Collez l’identité dans le code XML de votre type personnalisé d’informations sensibles et chargez-le. Votre dictionnaire s’affiche désormais dans votre liste de types d’informations sensibles et vous pouvez l’utiliser directement dans votre stratégie en indiquant le nombre de mots clés qui doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="5ac08-p116">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
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


