---
title: Examen d’éléments partiellement indexés dans eDiscovery Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Partiellement des éléments indexés (également les éléments d’appel non indexé) sont des éléments de boîte aux lettres Exchange et des documents dans SharePoint et OneDrive que des sites pour une raison quelconque n’ont pas été entièrement indexée pour la recherche de contenu. Dans cet article, découvrez pourquoi les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments indexés partiellement, identifier les erreurs de recherche pour les éléments indexés partiellement et utiliser un script PowerShell pour déterminer l’exposition de votre organisation pour les courriers électroniques partiellement indexés éléments.
ms.openlocfilehash: 98f794e80ea8a6016887ff139bc5b546c438f093
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038077"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a>Examen d’éléments partiellement indexés dans eDiscovery Office 365

Une recherche de contenu que vous exécutez à partir de la sécurité de 365 Office &amp; centre de conformité inclut automatiquement les éléments indexés partiellement dans les résultats de recherche estimés lorsque vous exécutez une recherche. Éléments indexés partiellement sont des éléments de boîte aux lettres Exchange et des documents dans SharePoint et OneDrive pour les sites d’entreprise qui n’ont pas été entièrement indexés pour la recherche pour une raison quelconque. La plupart des messages électroniques et des documents du site sont indexés, car ils peuvent être classées dans les [limites d’indexation pour les messages électroniques](limits-for-content-search.md#indexinglimits). Toutefois, certains éléments peuvent dépasser ces limites d’indexation et seront partiellement indexés. Vous trouverez ici les autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments indexés partiellement lorsque vous exécutez une recherche de contenu :
  
- Messages électroniques disposent d’un fichier joint d’un type de fichier qui ne peuvent pas être indexé ; dans la plupart des cas, le type de fichier est [inconnue ou non pris en charge pour l’indexation](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)
    
- Messages électroniques disposent d’une pièce jointe sans un gestionnaire valide, tels que les fichiers image ; Il s’agit de la cause la plus courante d’éléments de messagerie partiellement indexés
    
- Trop de fichiers joints à un message électronique
    
- Un fichier joint à un message électronique est trop grand
    
- Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique
    
Bien qu’il varie, la plupart des clients Office 365 organisations ont moins de 1 % du contenu par volume et inférieur à 12 % du contenu par taille est partiellement indexé. La raison de la différence entre le volume par rapport à la taille est que probabilité contenant le contenu qui ne peuvent pas être indexé complètement les fichiers plus volumineux.
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a>Pourquoi le nombre d’éléments indexés partiellement ne change pas pour une recherche ?

Après avoir exécuté une recherche de contenu de sécurité Office 365 &amp; centre de conformité, le nombre et la taille des éléments partiellement indexés dans les emplacements qui ont été exclus sont répertoriés dans les statistiques de résultats de recherche sont affichés dans les statistiques détaillées de la recherche. Remarque Il s’agit des *éléments non indexés* dans les statistiques de la recherche. Voici quelques points auront une incidence sur le nombre d’éléments indexés partiellement qui sont retournés dans les résultats de recherche : 
  
- Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et taille) des éléments de résultat de recherche et d’éléments indexés partiellement. Toutefois, lorsque les résultats de la même que la recherche sont exportées, l’élément est inclus uniquement avec le jeu de résultats de recherche ; Il n’a pas inclus en tant qu’un élément partiellement indexé.
    
- Si vous spécifiez une plage de dates pour une requête de recherche (à inclure dans la requête de mot clé) ou à l’aide d’une condition, n’importe quel élément partiellement indexé qui ne correspond pas à la plage de dates n’est pas inclus dans le nombre d’éléments indexés partiellement. Uniquement les éléments indexés partiellement qui tombent dans une plage de dates sont inclus dans le nombre d’éléments indexés partiellement.
    
 **Remarque :** Éléments indexés partiellement situés dans SharePoint et OneDrive sites *ne sont pas* inclus dans l’estimation des éléments indexés partiellement qui est affichée dans les statistiques détaillées de la recherche. Toutefois, les éléments indexés partiellement peuvent être exportés lorsque vous exportez les résultats d’une recherche de contenu. Par exemple, si vous ne rechercher que les sites dans une recherche de contenu, l’estimation du nombre partiellement éléments indexés sera zéro. 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a>Calcul du rapport entre les éléments indexés partiellement dans votre organisation

Pour comprendre l’exposition de votre organisation aux éléments partiellement indexés, vous pouvez exécuter une recherche pour tout le contenu de toutes les boîtes aux lettres (en utilisant une requête de mot clé vide). Dans l’exemple ci-dessous, il existe 56,208 (4,830 Mo) entièrement indexés 470 (316 Mo) et les éléments partiellement des éléments indexés.
  
![Exemple d’affichage de statistiques de recherche partiellement des éléments indexés](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
Vous pouvez déterminer le pourcentage d’éléments indexés partiellement en utilisant les calculs suivants.
  
 **Pour calculer le taux d’éléments indexés partiellement dans votre organisation :**

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
À l’aide de l’exemple précédent, les résultats de recherche. 84 % de tous les éléments de boîtes aux lettres sont partiellement indexé.
  
 **Pour calculer le pourcentage de la taille des éléments indexés partiellement dans votre organisation :**

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

Dans l’exemple précédent, 6.54 % de la taille totale des éléments de boîte aux lettres sont donc à partir des éléments indexés partiellement. Comme indiqué plus haut, la plupart des organisations Office 365 les clients disposent de moins de 1 % du contenu par volume et inférieur à 12 % du contenu par taille est partiellement indexé.

## <a name="working-with-partially-indexed-items"></a>Utilisation partiellement des éléments indexés

Dans le cas lorsque vous devez examiner partiellement éléments pour valider qu’ils ne contiennent pas les informations pertinentes, vous pouvez [Exporter un rapport de recherche de contenu](export-a-content-search-report.md) qui contient des informations sur les éléments indexés partiellement. Lorsque vous exportez un rapport de recherche de contenu, veillez à choisir une des options d’exportation qui inclut les éléments indexés partiellement. 
  
![Choisissez l’option deuxième ou troisième pour exporter les éléments indexés partiellement](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
Lorsque vous exportez des résultats de la recherche de contenu ou un rapport de recherche de contenu à l’aide d’une de ces options, l’exportation inclut un rapport nommé Items.csv non indexés. Ce rapport inclut la plupart des mêmes informations que le fichier ResultsLog.csv ; Toutefois, le fichier Items.csv non indexés inclut également deux champs relatives aux éléments indexés partiellement : **Balises d’erreur** et les **Propriétés de l’erreur**. Ces champs contiennent des informations sur l’erreur d’indexation pour chaque élément partiellement indexé. Utilisation des informations de ces deux champs peut vous aider à déterminer si l’erreur d’indexation pour un particulier a un impact sur votre investigation. Si c’est le cas, effectuez une recherche de contenu ciblée et récupérer et exporter des messages électroniques spécifiques et des documents SharePoint ou OneDrive afin que vous pouvez examiner pour déterminer si elles sont pertinents pour votre investigation. Pour obtenir des instructions détaillées, voir [préparer un fichier CSV pour une recherche de contenu ciblé dans Office 365](csv-file-for-an-id-list-content-search.md).
  
 **Remarque :** Le fichier Items.csv non indexés contienne également des champs nommés **Type d’erreur** et le **Message d’erreur**. Il s’agit hérités champs qui contiennent des informations semblables aux informations dans les champs de **Balises d’erreur** et les **Propriétés de l’erreur** , mais avec des informations moins détaillées. Vous pouvez ignorer ces champs hérités. 
  
## <a name="errors-related-to-partially-indexed-items"></a>Erreurs liées aux éléments indexés partiellement

Balises d’erreur sont constituées de deux éléments d’information, l’erreur et le type de fichier. Par exemple, dans cette paire/filetype de l’erreur :

```
 parseroutputsize_xls
```

   
 `parseroutputsize`est l’erreur et `xls` est le type de fichier du fichier s’est produit l’erreur. Dans les cas ont le type de fichier n’a pas été reconnu ou le type de fichier a été ne s’applique pas à l’erreur, vous pouvez visualiser la valeur `noformat` à la place du type de fichier. 
  
Voici une liste de l’indexation des erreurs et une description de la cause de l’erreur.
  
|**Balise erreur**|**Description**|
|:-----|:-----|
| `attachmentcount` <br/> |Un message électronique a trop de pièces jointes, et certains de ces pièces jointes n’ont pas été traités.  <br/> |
| `attachmentdepth` <br/> |L’Analyseur de documents et d’extracteur de contenu trouvés trop de niveaux de pièces jointes imbriquées dans d’autres pièces jointes. Certains de ces pièces jointes n’ont pas été traités.  <br/> |
| `attachmentrms` <br/> |Une pièce jointe a échoué, car il a été protégés par RMS de décodage.  <br/> |
| `attachmentsize` <br/> |Un fichier joint à un message électronique est trop volumineux et n’ont pas pu être traité.  <br/> |
| `indexingtruncated` <br/> |Lors de l’écriture du message électronique traitées à l’index, une des propriétés indexables était trop volumineux et a été tronquée. Les propriétés tronquées sont répertoriées dans le champ de propriétés de l’erreur.  <br/> |
| `invalidunicode` <br/> |Un message électronique contenue du texte qui n’ont pas pu être traité en tant que Unicode valide. L’indexation de cet élément peut être incomplète.  <br/> |
| `parserencrypted` <br/> |Le contenu de pièce jointe ou un message électronique est chiffré et Office 365 n’a pas pu décoder le contenu.  <br/> |
| `parsererror` <br/> |Une erreur inconnue s’est produite pendant l’analyse. Cela provient généralement d’un bogue logiciel ou une panne du service.  <br/> |
| `parserinputsize` <br/> |Une pièce jointe est trop grande pour l’analyseur pour gérer et l’analyse de la pièce jointe ne l’avez pas ou n’a pas été achevée.  <br/> |
| `parsermalformed` <br/> |Une pièce jointe est incorrecte et n’ont pas pu être gérée par l’analyseur. Ce résultat de peuvent ancien fichier formats, les fichiers créés par un logiciel incompatible, ou des virus se faisant passer pour quelque chose autre que demandé.  <br/> |
| `parseroutputsize` <br/> |La sortie de l’analyse d’une pièce jointe est trop volumineux et doit être tronquée.  <br/> |
| `parserunknowntype` <br/> |Une pièce jointe a rencontré un type de fichier Office 365 n’a pas pu détecter.  <br/> |
| `parserunsupportedtype` <br/> |Une pièce jointe a rencontré un type de fichier Office 365could détecter, mais l’analyse de ce type de fichier n’est pas pris en charge.  <br/> |
| `propertytoobig` <br/> |La valeur d’une propriété de messagerie dans Exchange Store était trop grand pour être récupéré et le message n’a pas pu être traité. Cela seulement se produit généralement à la propriété corps d’un message électronique.  <br/> |
| `retrieverrms` <br/> |Échec de l’extracteur de contenu décoder un message protégé par RMS.  <br/> |
| `wordbreakertruncated` <br/> |Trop de mots ont été identifiés dans le document lors de l’indexation. Arrêt du traitement de la propriété lors de la limite, et la propriété est tronquée.  <br/> |
   
Champs d’erreur décrivent les champs qui sont affectés par l’erreur de traitement indiqué dans le champ balises d’erreur. Si vous recherchez une propriété telle que `subject` ou `participants`, erreurs dans le corps du message n’affecte pas les résultats de la recherche. Cela peut être utile pour déterminer exactement quels éléments indexés partiellement vous devrez peut-être étudier.
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a>À l’aide d’un script PowerShell pour déterminer l’exposition de votre organisation aux éléments de messagerie électronique partiellement indexés

Les étapes suivantes vous montrent comment exécuter un script PowerShell qui recherche tous les éléments de toutes les boîtes aux lettres Exchange, puis génère un rapport sur les taux de votre organisation d’éléments de messagerie partiellement indexé (en fonction du nombre et taille) et affiche le nombre d’éléments (et leur type de fichier) pour chaque erreur d’indexation qui se produit. Utilisez les descriptions de balise d’erreur dans la section précédente pour identifier l’erreur d’indexation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `PartiallyIndexedItems.ps1`.

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. [Se connecter à Office 365 sécurité &amp; centre de conformité PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).
    
3. Dans la sécurité &amp; PowerShell du centre de conformité, accédez au dossier où vous avez enregistré le script à l’étape 1, puis exécutez le script ; par exemple :

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
Voici un exemple du résultat retourné par le script de sites.
  
![Exemple de sortie de script qui génère un rapport sur l’exposition de votre organisation aux éléments de messagerie électronique partiellement indexés](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
Notez les points suivants :
  
1. Le nombre total et la taille des éléments de courrier électronique, ainsi que les taux de votre organisation partiellement indexé d’éléments de messagerie (en fonction du nombre et taille)
    
2. Les balises d’une erreur de liste et les types de fichiers pour lequel l’erreur s’est produite.
  
## <a name="see-also"></a>Voir aussi

[Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)
