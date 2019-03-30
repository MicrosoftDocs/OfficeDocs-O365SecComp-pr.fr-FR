---
title: Examen d’éléments partiellement indexés dans eDiscovery Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Les éléments partiellement indexés (également appelés éléments non indexés) sont des éléments de boîte aux lettres Exchange et des documents sur les sites SharePoint et OneDrive qui n'ont pas été complètement indexés pour la recherche de contenu. Dans cet article, vous pouvez découvrir pourquoi les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu'éléments partiellement indexés, identifier les erreurs de recherche pour les éléments partiellement indexés et utiliser un script PowerShell pour déterminer l'exposition de votre organisation à l'e-mail partiellement indexé. sous.
ms.openlocfilehash: d6b1326498780a5d40e49ff22aa1ac7d16bee8e4
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000887"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a>Examen d’éléments partiellement indexés dans eDiscovery Office 365

Une recherche de contenu exécutée à partir du centre de sécurité & conformité inclut automatiquement les éléments partiellement indexés dans les résultats de recherche estimés lors de l'exécution d'une recherche. Les éléments partiellement indexés sont des éléments de boîte aux lettres Exchange et des documents sur SharePoint et des sites OneDrive entreprise qui n'ont pas été complètement indexés pour la recherche. La plupart des messages électroniques et des documents de site sont indexés, car ils sont inclus dans les [limites d'indexation pour les messages électroniques](limits-for-content-search.md#indexing-limits-for-email-messages). Toutefois, certains éléments peuvent dépasser ces limites d'indexation et seront partiellement indexés. Voici d'autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu'éléments partiellement indexés lors de l'exécution d'une recherche de contenu:
  
- Les messages électroniques contiennent un fichier joint d'un type de fichier qui ne peut pas être indexé; dans la plupart des cas, le type de fichier n'est [pas reconnu ou n'est pas pris en charge pour l'indexation](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search) .
    
- Les messages électroniques comportent un fichier joint sans gestionnaire valide, tel que des fichiers image; Il s'agit de la cause la plus fréquente d'éléments de courrier électronique partiellement indexés
    
- Trop de fichiers joints à un message électronique
    
- Un fichier joint à un message électronique est trop volumineux
    
- Le type de fichier est pris en charge pour l'indexation, mais une erreur d'indexation s'est produite pour un fichier spécifique.
    
Bien qu'elle varie, la plupart des entreprises Office 365 les clients disposent de moins de 1% du contenu par volume et de moins de 12% de contenu par taille partiellement indexée. La raison de la différence entre le volume et la taille est que les fichiers volumineux ont une probabilité plus élevée de contenir du contenu qui ne peut pas être complètement indexé.
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a>Pourquoi le nombre d'éléments partiellement indexés change pour une recherche?

Une fois que vous avez exécuté une recherche de contenu dans le centre de sécurité & Compliance Center, le nombre total et la taille des éléments partiellement indexés des emplacements qui ont été recherchés sont répertoriés dans les statistiques de résultats de recherche qui s'affichent dans les statistiques détaillées de la recherche. Remarque ces éléments sont appelés *éléments* non indexés dans les statistiques de la recherche. Voici quelques éléments qui affecteront le nombre d'éléments partiellement indexés renvoyés dans les résultats de la recherche: 
  
- Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et la taille) des éléments de résultat de recherche et des éléments partiellement indexés. Toutefois, lorsque les résultats de cette même recherche sont exportés, l'élément est inclus uniquement avec le jeu de résultats de recherche; elle n'est pas incluse en tant qu'élément partiellement indexé.
    
- Si vous spécifiez une plage de dates pour une requête de recherche (en l'incluant dans la requête de mot clé ou à l'aide d'une condition), tout élément partiellement indexé ne correspondant pas à la plage de dates n'est pas inclus dans le nombre d'éléments partiellement indexés. Seuls les éléments partiellement indexés qui appartiennent à la plage de dates sont inclus dans le nombre d'éléments partiellement indexés.
    
 **Remarque:** Les éléments partiellement indexés situés dans les sites SharePoint et OneDrive ne *sont pas* inclus dans l'estimation des éléments partiellement indexés affichés dans les statistiques détaillées de la recherche. Toutefois, les éléments partiellement indexés peuvent être exportés lorsque vous exportez les résultats d'une recherche de contenu. Par exemple, si vous recherchez uniquement des sites dans une recherche de contenu, le nombre estimé des éléments partiellement indexés est égal à zéro. 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a>Calcul du ratio d'éléments partiellement indexés dans votre organisation

Pour comprendre l'exposition de votre organisation à des éléments partiellement indexés, vous pouvez effectuer une recherche sur tout le contenu de toutes les boîtes aux lettres (à l'aide d'une requête de mot-clé vide). Dans l'exemple ci-dessous, il y a 56 208 (4 830 Mo) d'éléments entièrement indexés et 470 (316 Mo) partiellement indexés.
  
![Exemple de statistiques de recherche affichant des éléments partiellement indexés](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
Vous pouvez déterminer le pourcentage d'éléments partiellement indexés à l'aide des calculs suivants.
  
 **Pour calculer le ratio d'éléments partiellement indexés dans votre organisation, procédez comme suit:**

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
À l'aide des résultats de recherche de l'exemple précédent,. 84% de tous les éléments de boîte aux lettres sont partiellement indexés.
  
 **Pour calculer le pourcentage de la taille des éléments partiellement indexés de votre organisation:**

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

Par conséquent, dans l'exemple précédent, 6,54% de la taille totale des éléments de boîte aux lettres proviennent d'éléments partiellement indexés. Comme indiqué précédemment, la plupart des entreprises 365 organisations disposent de moins de 1% du contenu par volume et de moins de 12% de contenu par taille partiellement indexée.

## <a name="working-with-partially-indexed-items"></a>Utilisation d'éléments partiellement indexés

Dans les cas où vous devez examiner partiellement des éléments pour vérifier qu'ils ne contiennent pas d'informations pertinentes, vous pouvez [exporter un rapport de recherche de contenu](export-a-content-search-report.md) qui contient des informations sur les éléments partiellement indexés. Lorsque vous exportez un rapport de recherche de contenu, veillez à choisir l'une des options d'exportation qui incluent des éléments partiellement indexés. 
  
![Choisir la deuxième ou troisième option pour exporter des éléments partiellement indexés](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
Lorsque vous exportez des résultats de recherche de contenu ou un rapport de recherche de contenu à l'aide de l'une de ces options, l'exportation inclut un rapport nommé éléments non indexés. csv. Ce rapport inclut la plupart des mêmes informations que le fichier ResultsLog. csv; Toutefois, le fichier éléments non indexés. csv inclut également deux champs liés à des éléments partiellement indexés: les balises d' **erreur** et les **propriétés d'erreur**. Ces champs contiennent des informations sur l'erreur d'indexation pour chaque élément partiellement indexé. L'utilisation des informations de ces deux champs peut vous aider à déterminer si l'erreur d'indexation pour un impact particulier a une incidence sur votre enquête. Si c'est le cas, vous pouvez effectuer une recherche de contenu ciblé et extraire et exporter des messages électroniques spécifiques et des documents SharePoint ou OneDrive pour les examiner afin de déterminer s'ils sont pertinents pour votre enquête. Pour obtenir des instructions pas à pas, voir [Prepare a CSV file for a targetEd content Search in Office 365](csv-file-for-an-id-list-content-search.md).
  
 **Remarque:** Le fichier éléments non indexés. csv contient également des champs nommés **type d'erreur** et message d' **erreur**. Il s'agit de champs hérités qui contiennent des informations similaires aux informations des champs balises d' **erreur** et **propriétés d'erreur** , mais avec des informations moins détaillées. Vous pouvez ignorer ces champs hérités en toute sécurité. 
  
## <a name="errors-related-to-partially-indexed-items"></a>Erreurs liées à des éléments partiellement indexés

Les balises d'erreur sont constituées de deux informations, l'erreur et le type de fichier. Par exemple, dans cette paire erreur/type de message:

```
 parseroutputsize_xls
```

   
 `parseroutputsize`est l'erreur et `xls` est le type de fichier du fichier dans lequel l'erreur s'est produite. Dans les cas où le type de fichier n'a pas été reconnu ou que le type de fichier n'est pas applicable à `noformat` l'erreur, vous verrez la valeur à la place du type de fichier. 
  
Voici une liste des erreurs d'indexation et une description de la cause possible de l'erreur.
  
|**Balise Error**|**Description**|
|:-----|:-----|
| `attachmentcount` <br/> |Un message électronique contient trop de pièces jointes et certaines de ces pièces jointes n'ont pas été traitées.  <br/> |
| `attachmentdepth` <br/> |Le plan de recherche de contenu et l'analyseur de documents ont trouvé trop de niveaux de pièces jointes imbriqués dans d'autres pièces jointes. Certaines de ces pièces jointes n'ont pas été traitées.  <br/> |
| `attachmentrms` <br/> |Le décodage d'une pièce jointe a échoué car elle était protégée par RMS.  <br/> |
| `attachmentsize` <br/> |Un fichier joint à un message électronique est trop volumineux et n'a pas pu être traité.  <br/> |
| `indexingtruncated` <br/> |Lors de l'écriture du message électronique traité dans l'index, l'une des propriétés indexable était trop volumineuse et a été tronquée. Les propriétés tronquées sont répertoriées dans le champ propriétés de l'erreur.  <br/> |
| `invalidunicode` <br/> |Un message électronique contient du texte qui n'a pas pu être traité en tant que format Unicode valide. L'indexation de cet élément est peut-être incomplète.  <br/> |
| `parserencrypted` <br/> |Le contenu de la pièce jointe ou du message électronique est chiffré et Office 365 n'a pas pu décoder le contenu.  <br/> |
| `parsererror` <br/> |Une erreur inconnue s'est produite lors de l'analyse. Cela résulte généralement d'un problème logiciel ou d'un blocage de service.  <br/> |
| `parserinputsize` <br/> |Une pièce jointe était trop volumineuse pour être gérée par l'analyseur, et l'analyse de cette pièce jointe n'a pas été effectuée ou n'a pas été terminée.  <br/> |
| `parsermalformed` <br/> |Une pièce jointe est mal formée et n'a pas pu être gérée par l'analyseur. Ce résultat peut provenir d'anciens formats de fichiers, de fichiers créés par des logiciels incompatibles ou de virus prétendant être autres que réclamés.  <br/> |
| `parseroutputsize` <br/> |La sortie de l'analyse d'une pièce jointe était trop volumineuse et devait être tronquée.  <br/> |
| `parserunknowntype` <br/> |Une pièce jointe a un type de fichier qu'Office 365 n'a pas pu détecter.  <br/> |
| `parserunsupportedtype` <br/> |Une pièce jointe a un type de fichier détecté par Office 365could, mais l'analyse de ce type de fichier n'est pas prise en charge.  <br/> |
| `propertytoobig` <br/> |La valeur d'une propriété de messagerie dans la Banque d'Exchange est trop grande pour être récupérée et le message n'a pas pu être traité. Cela ne se produit généralement que pour la propriété Body d'un message électronique.  <br/> |
| `retrieverrms` <br/> |Le extracteur de contenu n'a pas pu décoder un message protégé par RMS.  <br/> |
| `wordbreakertruncated` <br/> |Trop de mots ont été identifiés dans le document lors de l'indexation. Le traitement de la propriété s'est arrêté lorsque la limite est atteinte, et la propriété est tronquée.  <br/> |
   
Les champs d'erreur décrivent les champs qui sont affectés par l'erreur de traitement répertoriée dans le champ balises d'erreur. Si vous recherchez une propriété telle que `subject` ou `participants`, les erreurs contenues dans le corps du message n'ont pas d'impact sur les résultats de votre recherche. Cela peut être utile lorsque vous déterminez exactement quels éléments partiellement indexés vous pouvez être amené à approfondir votre enquête.
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a>Utilisation d'un script PowerShell pour déterminer l'exposition de votre organisation à des éléments de courrier électronique partiellement indexés

Les étapes suivantes montrent comment exécuter un script PowerShell qui recherche tous les éléments dans toutes les boîtes aux lettres Exchange, puis génère un rapport sur le ratio d'éléments de messagerie partiellement indexés de votre organisation (par nombre et taille) et affiche le nombre d'éléments (et leur type de fichier) pour chaque erreur d'indexation qui se produit. Utilisez les descriptions de balise Error de la section précédente pour identifier l'erreur d'indexation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `PartiallyIndexedItems.ps1`.

```
  write-host "**************************************************"
  write-host "     Security & Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
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
   
2. [Connectez-vous au centre de sécurité _AMP_ Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).
    
3. Dans Security & Compliance Center PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l'étape 1, puis exécutez le script. par exemple:

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
Voici un exemple de la sortie renvoyée par le script.
  
![Exemple de sortie d'un script qui génère un rapport sur l'exposition de votre organisation à des éléments de courrier électronique partiellement indexés](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
Remarques :
  
1. Le nombre total et la taille des éléments de courrier électronique, et le ratio de votre organisation pour les éléments de courrier électronique partiellement indexés (par nombre et par taille)
    
2. Balises d'erreur de liste et types de fichiers correspondants pour lesquels l'erreur s'est produite.
  
## <a name="see-also"></a>Voir aussi

[Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)
