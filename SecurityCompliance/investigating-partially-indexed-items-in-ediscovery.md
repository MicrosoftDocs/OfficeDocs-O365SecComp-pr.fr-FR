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
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a><span data-ttu-id="3f81c-104">Examen d’éléments partiellement indexés dans eDiscovery Office 365</span><span class="sxs-lookup"><span data-stu-id="3f81c-104">Investigating partially indexed items in Office 365 eDiscovery</span></span>

<span data-ttu-id="3f81c-p102">Une recherche de contenu que vous exécutez à partir de la sécurité de 365 Office &amp; centre de conformité inclut automatiquement les éléments indexés partiellement dans les résultats de recherche estimés lorsque vous exécutez une recherche. Éléments indexés partiellement sont des éléments de boîte aux lettres Exchange et des documents dans SharePoint et OneDrive pour les sites d’entreprise qui n’ont pas été entièrement indexés pour la recherche pour une raison quelconque. La plupart des messages électroniques et des documents du site sont indexés, car ils peuvent être classées dans les [limites d’indexation pour les messages électroniques](limits-for-content-search.md#indexinglimits). Toutefois, certains éléments peuvent dépasser ces limites d’indexation et seront partiellement indexés. Vous trouverez ici les autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments indexés partiellement lorsque vous exécutez une recherche de contenu :</span><span class="sxs-lookup"><span data-stu-id="3f81c-p102">A Content Search that you run from the Office 365 Security &amp; Compliance Center automatically includes partially indexed items in the estimated search results when you run a search. Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search. Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexinglimits). However, some items may exceed these indexing limits, and will be partially indexed. Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="3f81c-110">Messages électroniques disposent d’un fichier joint d’un type de fichier qui ne peuvent pas être indexé ; dans la plupart des cas, le type de fichier est [inconnue ou non pris en charge pour l’indexation](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span><span class="sxs-lookup"><span data-stu-id="3f81c-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="3f81c-111">Messages électroniques disposent d’une pièce jointe sans un gestionnaire valide, tels que les fichiers image ; Il s’agit de la cause la plus courante d’éléments de messagerie partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="3f81c-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="3f81c-112">Trop de fichiers joints à un message électronique</span><span class="sxs-lookup"><span data-stu-id="3f81c-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="3f81c-113">Un fichier joint à un message électronique est trop grand</span><span class="sxs-lookup"><span data-stu-id="3f81c-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="3f81c-114">Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique</span><span class="sxs-lookup"><span data-stu-id="3f81c-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="3f81c-p103">Bien qu’il varie, la plupart des clients Office 365 organisations ont moins de 1 % du contenu par volume et inférieur à 12 % du contenu par taille est partiellement indexé. La raison de la différence entre le volume par rapport à la taille est que probabilité contenant le contenu qui ne peuvent pas être indexé complètement les fichiers plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p103">Although it varies, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed. The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="3f81c-117">Pourquoi le nombre d’éléments indexés partiellement ne change pas pour une recherche ?</span><span class="sxs-lookup"><span data-stu-id="3f81c-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="3f81c-p104">Après avoir exécuté une recherche de contenu de sécurité Office 365 &amp; centre de conformité, le nombre et la taille des éléments partiellement indexés dans les emplacements qui ont été exclus sont répertoriés dans les statistiques de résultats de recherche sont affichés dans les statistiques détaillées de la recherche. Remarque Il s’agit des *éléments non indexés* dans les statistiques de la recherche. Voici quelques points auront une incidence sur le nombre d’éléments indexés partiellement qui sont retournés dans les résultats de recherche :</span><span class="sxs-lookup"><span data-stu-id="3f81c-p104">After you run a Content Search in the Office 365 Security &amp; Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search. Note these are called  *unindexed items*  in the search statistics. Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="3f81c-p105">Si un élément est partiellement indexé et correspond à la requête de recherche, il est inclus dans le nombre (et taille) des éléments de résultat de recherche et d’éléments indexés partiellement. Toutefois, lorsque les résultats de la même que la recherche sont exportées, l’élément est inclus uniquement avec le jeu de résultats de recherche ; Il n’a pas inclus en tant qu’un élément partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p105">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items. However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="3f81c-p106">Si vous spécifiez une plage de dates pour une requête de recherche (à inclure dans la requête de mot clé) ou à l’aide d’une condition, n’importe quel élément partiellement indexé qui ne correspond pas à la plage de dates n’est pas inclus dans le nombre d’éléments indexés partiellement. Uniquement les éléments indexés partiellement qui tombent dans une plage de dates sont inclus dans le nombre d’éléments indexés partiellement.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p106">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items. Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="3f81c-p107">**Remarque :** Éléments indexés partiellement situés dans SharePoint et OneDrive sites *ne sont pas* inclus dans l’estimation des éléments indexés partiellement qui est affichée dans les statistiques détaillées de la recherche. Toutefois, les éléments indexés partiellement peuvent être exportés lorsque vous exportez les résultats d’une recherche de contenu. Par exemple, si vous ne rechercher que les sites dans une recherche de contenu, l’estimation du nombre partiellement éléments indexés sera zéro.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p107">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search. However, partially indexed items can be exported when you export the results of a Content Search. For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="3f81c-128">Calcul du rapport entre les éléments indexés partiellement dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="3f81c-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="3f81c-p108">Pour comprendre l’exposition de votre organisation aux éléments partiellement indexés, vous pouvez exécuter une recherche pour tout le contenu de toutes les boîtes aux lettres (en utilisant une requête de mot clé vide). Dans l’exemple ci-dessous, il existe 56,208 (4,830 Mo) entièrement indexés 470 (316 Mo) et les éléments partiellement des éléments indexés.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p108">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query). In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Exemple d’affichage de statistiques de recherche partiellement des éléments indexés](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="3f81c-132">Vous pouvez déterminer le pourcentage d’éléments indexés partiellement en utilisant les calculs suivants.</span><span class="sxs-lookup"><span data-stu-id="3f81c-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="3f81c-133">**Pour calculer le taux d’éléments indexés partiellement dans votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="3f81c-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="3f81c-134">À l’aide de l’exemple précédent, les résultats de recherche. 84 % de tous les éléments de boîtes aux lettres sont partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="3f81c-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="3f81c-135">**Pour calculer le pourcentage de la taille des éléments indexés partiellement dans votre organisation :**</span><span class="sxs-lookup"><span data-stu-id="3f81c-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="3f81c-p109">Dans l’exemple précédent, 6.54 % de la taille totale des éléments de boîte aux lettres sont donc à partir des éléments indexés partiellement. Comme indiqué plus haut, la plupart des organisations Office 365 les clients disposent de moins de 1 % du contenu par volume et inférieur à 12 % du contenu par taille est partiellement indexé.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p109">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items. As previously stated, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="3f81c-138">Utilisation partiellement des éléments indexés</span><span class="sxs-lookup"><span data-stu-id="3f81c-138">Working with partially indexed items</span></span>

<span data-ttu-id="3f81c-p110">Dans le cas lorsque vous devez examiner partiellement éléments pour valider qu’ils ne contiennent pas les informations pertinentes, vous pouvez [Exporter un rapport de recherche de contenu](export-a-content-search-report.md) qui contient des informations sur les éléments indexés partiellement. Lorsque vous exportez un rapport de recherche de contenu, veillez à choisir une des options d’exportation qui inclut les éléments indexés partiellement.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p110">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items. When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![Choisissez l’option deuxième ou troisième pour exporter les éléments indexés partiellement](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="3f81c-p111">Lorsque vous exportez des résultats de la recherche de contenu ou un rapport de recherche de contenu à l’aide d’une de ces options, l’exportation inclut un rapport nommé Items.csv non indexés. Ce rapport inclut la plupart des mêmes informations que le fichier ResultsLog.csv ; Toutefois, le fichier Items.csv non indexés inclut également deux champs relatives aux éléments indexés partiellement : **Balises d’erreur** et les **Propriétés de l’erreur**. Ces champs contiennent des informations sur l’erreur d’indexation pour chaque élément partiellement indexé. Utilisation des informations de ces deux champs peut vous aider à déterminer si l’erreur d’indexation pour un particulier a un impact sur votre investigation. Si c’est le cas, effectuez une recherche de contenu ciblée et récupérer et exporter des messages électroniques spécifiques et des documents SharePoint ou OneDrive afin que vous pouvez examiner pour déterminer si elles sont pertinents pour votre investigation. Pour obtenir des instructions détaillées, voir [préparer un fichier CSV pour une recherche de contenu ciblé dans Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="3f81c-p111">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv. This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**. These fields contain information about the indexing error for each partially indexed item. Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation. If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation. For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="3f81c-p112">**Remarque :** Le fichier Items.csv non indexés contienne également des champs nommés **Type d’erreur** et le **Message d’erreur**. Il s’agit hérités champs qui contiennent des informations semblables aux informations dans les champs de **Balises d’erreur** et les **Propriétés de l’erreur** , mais avec des informations moins détaillées. Vous pouvez ignorer ces champs hérités.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p112">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**. These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information. You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="3f81c-151">Erreurs liées aux éléments indexés partiellement</span><span class="sxs-lookup"><span data-stu-id="3f81c-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="3f81c-p113">Balises d’erreur sont constituées de deux éléments d’information, l’erreur et le type de fichier. Par exemple, dans cette paire/filetype de l’erreur :</span><span class="sxs-lookup"><span data-stu-id="3f81c-p113">Error tags are made up of two pieces of information, the error and the file type. For example, in this error/filetype pair:</span></span>

```
 parseroutputsize_xls
```

   
 <span data-ttu-id="3f81c-p114">`parseroutputsize`est l’erreur et `xls` est le type de fichier du fichier s’est produit l’erreur. Dans les cas ont le type de fichier n’a pas été reconnu ou le type de fichier a été ne s’applique pas à l’erreur, vous pouvez visualiser la valeur `noformat` à la place du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p114">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on. In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="3f81c-156">Voici une liste de l’indexation des erreurs et une description de la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3f81c-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="3f81c-157">**Balise erreur**</span><span class="sxs-lookup"><span data-stu-id="3f81c-157">**Error tag**</span></span>|<span data-ttu-id="3f81c-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f81c-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="3f81c-159">Un message électronique a trop de pièces jointes, et certains de ces pièces jointes n’ont pas été traités.</span><span class="sxs-lookup"><span data-stu-id="3f81c-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="3f81c-p115">L’Analyseur de documents et d’extracteur de contenu trouvés trop de niveaux de pièces jointes imbriquées dans d’autres pièces jointes. Certains de ces pièces jointes n’ont pas été traités.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p115">The content retriever and document parser found too many levels of attachments nested inside other attachments. Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="3f81c-162">Une pièce jointe a échoué, car il a été protégés par RMS de décodage.</span><span class="sxs-lookup"><span data-stu-id="3f81c-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="3f81c-163">Un fichier joint à un message électronique est trop volumineux et n’ont pas pu être traité.</span><span class="sxs-lookup"><span data-stu-id="3f81c-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="3f81c-p116">Lors de l’écriture du message électronique traitées à l’index, une des propriétés indexables était trop volumineux et a été tronquée. Les propriétés tronquées sont répertoriées dans le champ de propriétés de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p116">When writing the processed email message to the index, one of the indexable properties was too large and was truncated. The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="3f81c-p117">Un message électronique contenue du texte qui n’ont pas pu être traité en tant que Unicode valide. L’indexation de cet élément peut être incomplète.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p117">An email message contained text that couldn't be processed as valid Unicode. Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="3f81c-168">Le contenu de pièce jointe ou un message électronique est chiffré et Office 365 n’a pas pu décoder le contenu.</span><span class="sxs-lookup"><span data-stu-id="3f81c-168">The content of attachment or email message is encrypted, and Office 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="3f81c-p118">Une erreur inconnue s’est produite pendant l’analyse. Cela provient généralement d’un bogue logiciel ou une panne du service.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p118">An unknown error occurred during parsing. This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="3f81c-171">Une pièce jointe est trop grande pour l’analyseur pour gérer et l’analyse de la pièce jointe ne l’avez pas ou n’a pas été achevée.</span><span class="sxs-lookup"><span data-stu-id="3f81c-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="3f81c-p119">Une pièce jointe est incorrecte et n’ont pas pu être gérée par l’analyseur. Ce résultat de peuvent ancien fichier formats, les fichiers créés par un logiciel incompatible, ou des virus se faisant passer pour quelque chose autre que demandé.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p119">An attachment was malformed and couldn't be handled by the parser. This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="3f81c-174">La sortie de l’analyse d’une pièce jointe est trop volumineux et doit être tronquée.</span><span class="sxs-lookup"><span data-stu-id="3f81c-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="3f81c-175">Une pièce jointe a rencontré un type de fichier Office 365 n’a pas pu détecter.</span><span class="sxs-lookup"><span data-stu-id="3f81c-175">An attachment had a file type that Office 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="3f81c-176">Une pièce jointe a rencontré un type de fichier Office 365could détecter, mais l’analyse de ce type de fichier n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3f81c-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="3f81c-p120">La valeur d’une propriété de messagerie dans Exchange Store était trop grand pour être récupéré et le message n’a pas pu être traité. Cela seulement se produit généralement à la propriété corps d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p120">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed. This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="3f81c-179">Échec de l’extracteur de contenu décoder un message protégé par RMS.</span><span class="sxs-lookup"><span data-stu-id="3f81c-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="3f81c-p121">Trop de mots ont été identifiés dans le document lors de l’indexation. Arrêt du traitement de la propriété lors de la limite, et la propriété est tronquée.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p121">Too many words were identified in the document during indexing. Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="3f81c-p122">Champs d’erreur décrivent les champs qui sont affectés par l’erreur de traitement indiqué dans le champ balises d’erreur. Si vous recherchez une propriété telle que `subject` ou `participants`, erreurs dans le corps du message n’affecte pas les résultats de la recherche. Cela peut être utile pour déterminer exactement quels éléments indexés partiellement vous devrez peut-être étudier.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p122">Error fields describe which fields are affected by the processing error listed in the Error Tags field. If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search. This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="3f81c-185">À l’aide d’un script PowerShell pour déterminer l’exposition de votre organisation aux éléments de messagerie électronique partiellement indexés</span><span class="sxs-lookup"><span data-stu-id="3f81c-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="3f81c-p123">Les étapes suivantes vous montrent comment exécuter un script PowerShell qui recherche tous les éléments de toutes les boîtes aux lettres Exchange, puis génère un rapport sur les taux de votre organisation d’éléments de messagerie partiellement indexé (en fonction du nombre et taille) et affiche le nombre d’éléments (et leur type de fichier) pour chaque erreur d’indexation qui se produit. Utilisez les descriptions de balise d’erreur dans la section précédente pour identifier l’erreur d’indexation.</span><span class="sxs-lookup"><span data-stu-id="3f81c-p123">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs. Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="3f81c-188">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `PartiallyIndexedItems.ps1`.</span><span class="sxs-lookup"><span data-stu-id="3f81c-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

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
   
2. <span data-ttu-id="3f81c-189">[Se connecter à Office 365 sécurité &amp; centre de conformité PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="3f81c-189">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="3f81c-190">Dans la sécurité &amp; PowerShell du centre de conformité, accédez au dossier où vous avez enregistré le script à l’étape 1, puis exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="3f81c-190">In Security &amp; Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
<span data-ttu-id="3f81c-191">Voici un exemple du résultat retourné par le script de sites.</span><span class="sxs-lookup"><span data-stu-id="3f81c-191">Here's an example fo the output returned by the script.</span></span>
  
![Exemple de sortie de script qui génère un rapport sur l’exposition de votre organisation aux éléments de messagerie électronique partiellement indexés](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="3f81c-193">Notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="3f81c-193">Note the following:</span></span>
  
1. <span data-ttu-id="3f81c-194">Le nombre total et la taille des éléments de courrier électronique, ainsi que les taux de votre organisation partiellement indexé d’éléments de messagerie (en fonction du nombre et taille)</span><span class="sxs-lookup"><span data-stu-id="3f81c-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="3f81c-195">Les balises d’une erreur de liste et les types de fichiers pour lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3f81c-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f81c-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f81c-196">See also</span></span>

[<span data-ttu-id="3f81c-197">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3f81c-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
