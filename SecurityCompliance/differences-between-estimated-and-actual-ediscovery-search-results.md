---
title: Différences entre les résultats de recherche réels et estimés eDiscovery dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/13/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
ms.assetid: 8f20ca4f-a908-46ec-99e6-9890d269ecf2
description: 'Comprendre pourquoi les résultats de recherche réels et estimés peuvent varier dans les recherches exécuter avec les outils de découverte électronique dans Office 365. '
ms.openlocfilehash: b68f5ea2a24d3229a65b360f390284374a1efd39
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037997"
---
# <a name="differences-between-estimated-and-actual-ediscovery-search-results-in-office-365"></a>Différences entre les résultats de recherche réels et estimés eDiscovery dans Office 365

Cette rubrique s’applique aux recherches que vous pouvez exécuter à l’aide d’un des outils de découverte électronique Microsoft suivants :  <br/>  
- Contenu de recherche dans la sécurité Office 365 &amp; centre de conformité  <br/>  
- EDiscovery sur Place dans le centre d’administration Exchange (EAC)  <br/>  
- Le centre eDiscovery dans SharePoint Online  <br/> 
   
Lorsque vous exécutez une recherche eDiscovery, vous utilisez l’outil de renverra une estimation du nombre d’éléments (et leur taille totale) qui répondent aux critères de recherche. Par exemple, lorsque vous exécutez une recherche dans la sécurité &amp; centre de conformité, la recherche estimés résultats sont affichés dans le volet d’informations pour la recherche sélectionnée.
  
![Estimation des résultats affichés dans le volet de détails de la recherche sélectionnée](media/74e4ce83-40be-41a9-b60f-5ad447e79fe4.png)
  
Il s’agit de la même estimation de la taille totale et le nombre d’éléments qui est affiché dans l’outil d’exportation lorsque vous exportez des résultats à un ordinateur local eDiscovery et dans le rapport résumé d’exportation qui est téléchargé avec les résultats de recherche.
  
**Estimation des résultats dans l’outil d’exportation de découverte électronique**

![Résultats estimés dans l’outil d’exportation de la découverte électronique](media/d34312a5-0ee6-49aa-9460-7ea0015a6e66.png)
  
**Estimation résultats dans un rapport de synthèse exporter**

![Les résultats de recherche estimés sont inclus dans le rapport Résumé d’exportation](media/44b579da-86c2-4f33-81b5-84d604003eda.png)
  
Toutefois, comme vous pouvez le constater dans la capture d’écran précédente du rapport résumé d’exportation, la taille et le nombre de résultats de la recherche sont réellement téléchargés sont différents de celui de la taille et le nombre de résultats de recherche estimés. 
  
![Différence entre les résultats de recherche estimés et téléchargés](media/84aef318-230f-430d-9d9e-02f21342d364.png)
  
Voici quelques raisons de ces différences :
  
- **L’affichage des résultats sont estimés** - estimation des résultats de recherche sont simplement que, une estimation (et pas un nombre réel) des éléments qui répondent aux critères de la requête de recherche. Pour compiler l’estimation des éléments Exchange, une liste d’ID qui répondent aux critères de recherche de message est demandée à partir de la base de données Exchange par l’outil de découverte électronique que vous utilisez. Mais lorsque vous exportez les résultats de recherche, la nouvelle exécution de la recherche et les messages réels sont récupérées à partir de la base de données Exchange. Donc ces différences peuvent se produire en raison de la détermination des estimation du nombre d’éléments et le nombre d’éléments. 
    
- **Les modifications qui se produire entre le moment lorsque estimation et l’exportation de résultats de la recherche** - lorsque vous exportez des résultats de la recherche, la recherche est redémarrage pour collecter que les éléments les plus récents dans l’index de recherche qui répondent aux critères de recherche. Il est possible d’autres éléments ont été créés, envoyés ou reçus qui répondent aux critères de recherche dans le temps entre lorsque les résultats de recherche estimés ont été recueillis et lorsque les résultats de recherche ont été exportés. Il est également possible que les éléments qui ont été dans l’index de recherche lorsque les résultats de recherche ont été estimées ne sont plus il, car ils ont été supprimés de l’emplacement du contenu avant d’exporter les résultats de la recherche. Pour atténuer ce problème consiste à spécifier une plage de dates pour une recherche eDiscovery. Une autre méthode consiste à placer une suspension sur les emplacements de contenu afin que les éléments sont conservés et ne peuvent pas être supprimés. 
    
- **Éléments non indexés** - éléments non indexés pour la recherche peut provoquer des différences entre les résultats de recherche réels et estimés. Par exemple, découverte électronique inaltérable dans Exchange et le centre eDiscovery dans SharePoint n’incluez pas les éléments non indexés (qui ne répondent aux critères de recherche) lorsque vous exécutez une recherche pour estimer les résultats de recherche. Mais vous pouvez inclure les éléments non indexés lorsque vous exportez les résultats de recherche. Si vous incluez des éléments non indexés lors de l’exportation des résultats de la recherche, il peut y avoir plusieurs éléments qui sont exportés. Cela entraîne une différence entre les résultats de recherche estimés et exporté. 
    
    Lors de l’utilisation de l’outil de recherche de contenu dans la sécurité &amp; centre de conformité, vous avez la possibilité d’inclure les éléments non indexés dans l’estimation de la recherche. Le nombre d’éléments non indexés renvoyés par la recherche est répertorié dans le volet de détails, ainsi que les autres résultats de recherche estimés. Tous les éléments non indexés doit également être inclus dans la taille totale de l’estimation des résultats de recherche. Lorsque vous exportez des résultats de la recherche, vous avez la possibilité d’inclure ou pas inclure les éléments non indexés. Comment configurer ces options peut entraîner des différences entre estimée et des résultats de la recherche sont téléchargés. 
    
- **Exporter les résultats d’une recherche de contenu qui inclut tous les emplacements de contenu** - si vous exportez des résultats de la recherche a été une recherche de tous les emplacements de contenu dans votre organisation, puis uniquement les éléments non indexées à partir d’emplacements de contenu qui contiennent les éléments qui correspondent aux critères de recherche seront exportés. En d’autres termes, si aucun résultat de recherche n’est détectée dans une boîte aux lettres ou d’un site, tous les éléments non indexés dans cette boîte aux lettres ou d’un site ne sont pas exportées. Toutefois, les éléments non indexées à partir de tous les emplacements de contenu (même ceux qui ne contiennent pas les éléments qui correspondent à la requête de recherche) figureront dans les résultats de recherche estimés. 
    
    Sinon, si vous exportez des résultats de la recherche inclus les emplacements de contenu spécifiques, des éléments non indexés (qui ne sont pas exclus par les critères de recherche) à partir de tous les emplacements de contenu spécifiés dans la recherche seront exportés. Dans ce cas, l’estimation du nombre d’éléments non indexés et le nombre d’éléments non indexés effectivement exportée doivent être le même.
    
    La raison de l’exportation ne pas d’éléments non indexées à partir de chaque emplacement dans l’organisation est, car il peut augmenter la probabilité d’erreurs d’exportation et augmenter le temps que nécessaire pour exporter et télécharger les résultats de recherche.
    
- **Formats de fichiers brutes et formats de fichier exporté** - éléments pour Exchange, la taille estimée des résultats de recherche est calculé à l’aide de la taille des messages Exchange brute. Toutefois, les messages électroniques sont exportés dans un fichier PST ou sous forme de messages individuels (qui sont mis en forme en tant que fichiers EML). Les deux de ces options d’exportation utilisent un autre fichier format brutes messages Exchange, qui se traduit par la taille du fichier exporté est différente de la taille de fichier estimée. 
    
- **Les versions de document** - documents pour SharePoint, plusieurs versions d’un document ne sont pas inclus dans les résultats de recherche estimés. Mais vous avez la possibilité d’inclure toutes les versions de document lorsque vous exportez les résultats de recherche, ce qui augmentent le nombre réel (et la taille totale) des documents exportés. 
    
- **La déduplication** - éléments pour Exchange, la déduplication réduit le nombre d’éléments qui sont exportés. Vous avez la possibilité de suppression des doublons les résultats de recherche lorsque vous exportez les. Pour les messages Exchange, cela signifie qu’une seule instance d’un message est exportée, même si ce message peut être trouvé dans plusieurs boîtes aux lettres. Les résultats de recherche estimés incluent chaque instance d’un message. Si vous choisissez l’option la déduplication lors de l’exportation des résultats de la recherche, le nombre d’éléments qui sont exportés peut être très inférieur à l’estimation du nombre d’éléments. 
    
    Une autre chose à prendre en compte si vous choisissez l’option la déduplication est que tous les éléments d’Exchange sont exportées dans un seul fichier PST et la structure de dossiers de boîtes aux lettres source n’est pas conservée. Le fichier exporté contient uniquement les éléments de courrier électronique. Toutefois, un rapport de résultats de recherche contient une entrée pour chaque message exporté qui identifie la boîte aux lettres source où se trouve le message. Cela permet d’identifier toutes les boîtes aux lettres contenant un message en double. Si vous n’activez pas la déduplication, un fichier PST distinct est exporté pour chaque boîte aux lettres inclus dans la recherche. 
    
## <a name="exporting-unindexed-items-from-the-ediscovery-center-in-sharepoint-online"></a>Exportation d’éléments non indexées à partir du centre de découverte électronique dans SharePoint Online

Dans le centre eDiscovery dans SharePoint Online, vous avez la possibilité d’inclure du contenu non indexée (à partir d’Exchange et SharePoint) lorsque vous exportez les résultats d’une recherche eDiscovery. Pour cela, en sélectionnant l’option **inclure les éléments qui sont chiffrées ou ont un format non reconnu** . Éléments non indexés (également appelées uncrawlable dans SharePoint) sont des éléments dans Exchange et SharePoint qui n’ont pas été indexé pour la recherche pour une raison quelconque. Éléments Exchange non indexées sont répertoriés dans le rapport **d’Erreurs d’Index Exchange** inclus lorsque vous exportez des résultats de la recherche. De même, les éléments SharePoint non indexés sont répertoriés dans le rapport **d’Erreurs d’Index SharePoint** . Lorsque vous exportez des éléments non indexés, ils sont téléchargés vers un dossier nommé **Uncrawlable**. Éléments Exchange non indexés sont inclus dans un fichier PST. chaque document non indexée à partir de SharePoint est trop téléchargé. Le nombre d’éléments non indexés (le cas échéant) sont répertoriés dans chaque rapport d’erreurs index. Le nombre d’éléments non indexés dans les rapports doit correspondre au nombre d’éléments non indexées sont téléchargés. 
  
 **Quelles sont les raisons si le nombre d’éléments non indexés exportés ne correspondre pas le nombre d’éléments dans le rapport d’erreurs index ?** Comme expliqué précédemment, il est possible que les éléments ont été purgés entre l’exécution de l’estimation de la recherche et le temps que les résultats de recherche ont été exportés à partir d’Office 365. Une incohérence similaire peut se produire pour les éléments non indexés. Par exemple, l’index de recherche peut être date lorsque les résultats de la recherche sont exportées. Cela signifie qu’un élément non indexé qui a été exporté avec les résultats de recherche ne pas être répertorié dans le rapport d’erreurs index, car l’élément n’a pas été indexé au moment où que les résultats de recherche ont été exportés. Cela donne lieu à des éléments plus non indexées en cours d’exportation que celles énumérées dans le rapport d’erreurs index. De même, un élément non indexée répertorié dans le rapport d’erreurs index pourrait ont été purgé à partir d’Office 365 avant mise à jour de l’index de recherche. Cela donne lieu à moins d’éléments non indexées sont en cours d’exportation que celles énumérées dans le rapport d’erreurs index. 
  
> [!NOTE]
> Si vous n’activez pas l’option **inclure les éléments qui sont chiffrées ou ont un format non reconnu** lorsque vous exportez des résultats de recherche ou téléchargez les rapports, les rapports d’erreurs index sont téléchargés mais ne sont pas toutes les entrées. Cela ne signifie pas que ne contient pas les erreurs d’indexation. Cela signifie simplement que les éléments non indexés n’ont pas été inclus dans l’exportation. 
  

