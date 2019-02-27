---
title: Différences entre les résultats de recherche de découverte électronique estimée et réelle dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/13/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- SPO160
- MOE150
ms.assetid: 8f20ca4f-a908-46ec-99e6-9890d269ecf2
description: 'Comprendre pourquoi les résultats de recherche estimés et réels peuvent varier en fonction des recherches exécutées avec les outils eDiscovery dans Office 365. '
ms.openlocfilehash: d3edc73d94d51c2582b6ef2077c5e4c834d1ff82
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296117"
---
# <a name="differences-between-estimated-and-actual-ediscovery-search-results-in-office-365"></a>Différences entre les résultats de recherche de découverte électronique estimée et réelle dans Office 365

Cette rubrique s'applique aux recherches que vous pouvez exécuter à l'aide de l'un des outils Microsoft eDiscovery suivants:  <br/>  
- Recherche de contenu dans le centre de &amp; sécurité conformité Office 365  <br/>  
- Découverte électronique inaltérable dans le centre d'administration Exchange  <br/>  
- Le centre eDiscovery dans SharePoint Online  <br/> 
   
Lorsque vous exécutez une recherche de découverte électronique, l'outil que vous utilisez renvoie une estimation du nombre d'éléments (et leur taille totale) correspondant aux critères de recherche. Par exemple, lorsque vous effectuez une recherche dans le centre &amp; de sécurité conformité, les résultats de recherche estimés s'affichent dans le volet d'informations de la recherche sélectionnée.
  
![Estimation des résultats affichés dans le volet de détails de la recherche sélectionnée](media/74e4ce83-40be-41a9-b60f-5ad447e79fe4.png)
  
Il s'agit de la même estimation de la taille totale et du nombre d'éléments affichés dans l'outil d'exportation de découverte électronique lorsque vous exportez les résultats vers un ordinateur local et dans le rapport de synthèse d'exportation téléchargé avec les résultats de la recherche.
  
**Résultats estimés dans l'outil d'exportation de découverte électronique**

![Résultats estimés dans l’outil d’exportation de la découverte électronique](media/d34312a5-0ee6-49aa-9460-7ea0015a6e66.png)
  
**Résultats estimés dans le rapport de synthèse d'exportation**

![Les résultats de recherche estimés sont inclus dans le rapport Résumé d’exportation](media/44b579da-86c2-4f33-81b5-84d604003eda.png)
  
Toutefois, comme vous pouvez le constater dans la capture d'écran précédente du rapport Résumé de l'exportation, la taille et le nombre de résultats de recherche réels réellement téléchargés diffèrent de la taille et du nombre de résultats de recherche estimés. 
  
![Différence entre les résultats de recherche estimés et téléchargés](media/84aef318-230f-430d-9d9e-02f21342d364.png)
  
Voici les raisons de ces différences:
  
- **La manière dont les résultats sont estimés** : une estimation des résultats de la recherche est juste, une estimation (et non un nombre réel) des éléments qui répondent aux critères de requête de recherche. Pour compiler l'estimation des éléments Exchange, une liste des ID de message correspondant aux critères de recherche est demandée à partir de la base de données Exchange par l'outil eDiscovery que vous utilisez. Toutefois, lorsque vous exportez les résultats de la recherche, la recherche est réexécutée et les messages réels sont extraits de la base de données Exchange. Par conséquent, ces différences peuvent résulter de la manière dont le nombre d'éléments estimé et le nombre réel d'éléments sont déterminés. 
    
- **Modifications qui se produisent entre le moment où vous évaluez et** exportez les résultats de la recherche: lorsque vous exportez les résultats de la recherche, la recherche est redémarrée pour recueillir les éléments les plus récents de l'index de recherche qui répondent aux critères de recherche. Il est possible que des éléments supplémentaires ont été créés, envoyés ou reçus et répondent aux critères de recherche entre le moment où les résultats de la recherche estimés ont été collectés et le moment où les résultats de la recherche ont été exportés. Il est également possible que les éléments qui se trouvaient dans l'index de recherche lorsque les résultats de la recherche étaient estimés ne soient plus présents, car ils ont été supprimés de l'emplacement du contenu avant l'exportation des résultats de la recherche. Pour atténuer ce problème, vous pouvez spécifier une plage de dates pour une recherche de découverte électronique. Une autre méthode consiste à placer un blocage sur les emplacements de contenu afin que les éléments soient conservés et ne peuvent pas être purgés. 
    
- **Éléments** non indexés: les éléments non indexés pour la recherche peuvent entraîner des différences entre les résultats de recherche estimés et les résultats de recherche réels. Par exemple, la découverte électronique inaltérable dans Exchange et le centre eDiscovery dans SharePoint n'incluent pas les éléments non indexés (qui ne répondent pas aux critères de recherche) lorsque vous exécutez une recherche pour estimer les résultats de la recherche. Toutefois, vous pouvez inclure des éléments non indexés lorsque vous exportez les résultats de la recherche. Si vous incluez des éléments non indexés lors de l'exportation des résultats de la recherche, d'autres éléments sont peut-être exportés. Cela entraîne une différence entre les résultats de recherche estimés et exportés. 
    
    Lorsque vous utilisez l'outil de recherche de contenu &amp; dans le centre de sécurité conformité, vous avez la possibilité d'inclure des éléments non indexés dans l'estimation de la recherche. Le nombre d'éléments non indexés renvoyés par la recherche est affiché dans le volet d'informations avec les autres résultats estimés de la recherche. Tous les éléments non indexés seraient également inclus dans la taille totale des résultats de recherche estimés. Lorsque vous exportez des résultats de recherche, vous avez la possibilité d'inclure ou de ne pas inclure les éléments non indexés. La manière dont vous configurez ces options peut entraîner des différences entre les résultats de recherche estimés et ceux qui sont téléchargés. 
    
- **Exportation des résultats d'une recherche de contenu incluant tous les emplacements de contenu** : si la recherche à partir de laquelle vous exportez les résultats provient de la recherche de tous les emplacements de contenu de votre organisation, seuls les éléments de contenu non indexés contenant les éléments qui correspondent aux critères de recherche seront exportés. En d'autres termes, si aucun résultat de recherche n'est trouvé dans une boîte aux lettres ou un site, tous les éléments non indexés de cette boîte aux lettres ou de ce site ne seront pas exportés. Toutefois, les éléments non indexés de tous les emplacements de contenu (même ceux qui ne contiennent pas d'éléments qui correspondent à la requête de recherche) sont inclus dans les résultats de recherche estimés. 
    
    Par ailleurs, si la recherche dont vous exportez les résultats à partir d'emplacements de contenu spécifiques inclus, les éléments non indexés (qui ne sont pas exclus par les critères de recherche) de tous les emplacements de contenu spécifiés dans la recherche seront exportés. Dans ce cas, le nombre estimé d'éléments non indexés et le nombre d'éléments non indexés réellement exportés doivent être identiques.
    
    La raison de l'impossibilité d'exporter des éléments non indexés de tous les emplacements de l'organisation est qu'elle augmente la probabilité d'erreurs d'exportation et augmente le temps nécessaire pour exporter et télécharger les résultats de la recherche.
    
- **Formats de fichiers bruts et formats de fichiers** exportés: pour les éléments Exchange, la taille estimée des résultats de la recherche est calculée à l'aide de la taille des messages Exchange bruts. Toutefois, les messages électroniques sont exportés dans un fichier PST ou sous forme de messages individuels (qui sont mis en forme en tant que fichiers EML). Ces deux options d'exportation utilisent un autre format de fichier que les messages Exchange bruts, ce qui a pour effet que la taille totale du fichier exporté est différente de la taille estimée du fichier. 
    
- **Versions de document** : pour les documents SharePoint, plusieurs versions d'un document ne sont pas incluses dans les résultats de recherche estimés. Toutefois, vous avez la possibilité d'inclure toutes les versions de document lorsque vous exportez les résultats de la recherche, ce qui augmente le nombre réel (et la taille totale) des documents exportés. 
    
- **Déduplication** : pour les éléments Exchange, la déduplication réduit le nombre d'éléments exportés. Vous avez la possibilité de dédupliquer les résultats de la recherche lorsque vous les exportez. Pour les messages Exchange, cela signifie qu'une seule instance d'un message est exportée, même si ce message est susceptible d'être trouvé dans plusieurs boîtes aux lettres. Les résultats de recherche estimés incluent chaque instance d'un message. Par conséquent, si vous choisissez l'option de déduplication lors de l'exportation des résultats de recherche, le nombre réel d'éléments exportés peut être considérablement inférieur au nombre estimé d'éléments. 
    
    Une autre chose à garder à l'esprit si vous choisissez l'option de déduplication est que tous les éléments Exchange sont exportés dans un fichier PST unique et que la structure de dossiers des boîtes aux lettres source n'est pas conservée. Le fichier PST exporté contient simplement les éléments de courrier électronique. Toutefois, un rapport de résultats de recherche contient une entrée pour chaque message exporté qui identifie la boîte aux lettres source où se trouve le message. Cela vous permet d'identifier toutes les boîtes aux lettres qui contiennent un message en double. Si vous n'activez pas la déduplication, un fichier PST distinct est exporté pour chaque boîte aux lettres incluse dans la recherche. 
    
## <a name="exporting-unindexed-items-from-the-ediscovery-center-in-sharepoint-online"></a>Exportation d'éléments non indexés à partir du centre eDiscovery dans SharePoint Online

Dans le centre eDiscovery de SharePoint Online, vous avez la possibilité d'inclure du contenu non indexé (à partir d'Exchange et SharePoint) lorsque vous exportez les résultats d'une recherche de découverte électronique. Pour ce faire, sélectionnez l'option **inclure les éléments chiffrés ou dont le format n'est pas reconnu** . Les éléments non indexés (également appelés «non analysables dans SharePoint») sont des éléments dans Exchange et SharePoint qui n'ont pas été indexés pour la recherche. Les éléments Exchange non indexés sont répertoriés dans le rapport **Erreurs d'index Exchange** qui est inclus lorsque vous exportez les résultats de la recherche. De même, les éléments non indexés SharePoint sont répertoriés dans le rapport d' **Erreurs d'index SharePoint** . Lorsque vous exportez des éléments non indexés, ils sont téléchargés **** vers un dossier nommé non analysable. Les éléments Exchange non indexés sont inclus dans un fichier PST; chaque document non indexé provenant de SharePoint est également téléchargé. Le nombre d'éléments non indexés (le cas échéant) sont répertoriés dans chaque rapport d'erreurs d'index. Le nombre d'éléments non indexés dans les rapports doit correspondre au nombre d'éléments non indexés qui sont téléchargés. 
  
 **Quelles sont les raisons pour lesquelles le nombre d'éléments non indexés exportés ne correspond pas au nombre d'éléments dans le rapport d'erreurs d'index?** Comme expliqué précédemment, il est possible que les éléments aient été purgés d'Office 365 entre l'heure d'exécution de la recherche et l'heure d'exportation des résultats de la recherche. Une anomalie similaire peut se produire pour les éléments non indexés. Par exemple, l'index de recherche est peut-être obsolète lorsque les résultats de la recherche sont exportés. Cela signifie qu'un élément non indexé qui a été exporté avec les résultats de la recherche peut ne pas figurer dans le rapport Erreurs d'index, car l'élément n'a pas été indexé lors de l'exportation des résultats de la recherche. Cela entraînerait l'exportation de plus d'éléments non indexés que ceux répertoriés dans le rapport d'erreurs d'index. De même, un élément non indexé figurant dans le rapport d'erreurs d'index a pu être purgé d'Office 365 avant la mise à jour de l'index de recherche. Cela entraînerait un moins grand nombre d'éléments non indexés à exporter que ce qui est répertorié dans le rapport d'erreurs d'index. 
  
> [!NOTE]
> Si vous ne sélectionnez pas l'option **inclure les éléments chiffrés ou dont le format n'est pas reconnu** lorsque vous exportez des résultats de recherche ou que vous venez de télécharger les rapports, les rapports d'erreur d'index sont téléchargés, mais ils n'ont aucune entrée. Cela ne signifie pas qu'il n'y a aucune erreur d'indexation. Cela signifie simplement que les éléments non indexés n'ont pas été inclus dans l'exportation. 
  

