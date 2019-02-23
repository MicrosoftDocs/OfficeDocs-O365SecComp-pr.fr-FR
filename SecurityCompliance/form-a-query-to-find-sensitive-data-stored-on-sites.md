---
title: Créer une requête pour trouver des données sensibles stockées sur des sites
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: Avec la protection contre la perte de données (DLP) dans SharePoint Online, vous pouvez découvrir des documents qui contiennent des données sensibles sur l'ensemble de votre client. Après avoir découvert les documents, vous pouvez travailler avec les propriétaires de documents pour protéger les données. Cette rubrique peut vous aider à créer une requête pour rechercher des données sensibles.
ms.openlocfilehash: 3dc1081d4627f1a26c50eed84f733c31a3f6c194
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217234"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>Créer une requête pour trouver des données sensibles stockées sur des sites

Les utilisateurs stockent souvent des données sensibles, telles que des numéros de carte de crédit, des numéros de sécurité sociale ou des informations personnelles sur leurs sites, ce qui peut exposer une organisation à un risque considérable de perte de données. Les documents stockés sur des sites, y compris les sites OneDrive entreprise, peuvent être partagés avec des personnes en dehors de l'organisation qui ne doivent pas avoir accès aux informations. Avec la protection contre la perte de données (DLP) dans SharePoint Online, vous pouvez découvrir des documents qui contiennent des données sensibles sur l'ensemble de votre client. Après avoir découvert les documents, vous pouvez travailler avec les propriétaires de documents pour protéger les données. Cette rubrique peut vous aider à créer une requête pour rechercher des données sensibles.
  
> [!NOTE]
> La découverte électronique, ou eDiscovery et DLP sont des fonctionnalités Premium qui nécessitent [SharePoint Online plan 2](https://go.microsoft.com/fwlink/?LinkId=510080). 
  
## <a name="forming-a-basic-dlp-query"></a>Création d'une requête DLP de base

Il existe trois parties qui composent une requête DLP de base: SensitiveType, plage de nombre et plage de confiance. Comme illustré dans le graphique suivant, **SensitiveType: «\<type\>»** est obligatoire, et**|\<\> la plage de nombre** et la plage de**|\<confiance\> ** sont facultatives. 
  
![Exemple de requête divisée en obligatoire et facultative](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>Type d'informations sensibles - Obligatoire

Qu'est-ce que chaque composant? Les requêtes DLP SharePoint commencent généralement par la `SensitiveType:"` propriété et un nom de type d'information à partir de l'inventaire des types d' `"` [informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999)et se terminent par un. Vous pouvez également utiliser le nom d'un [type d'informations sensibles personnalisé](create-a-custom-sensitive-information-type.md) que vous avez créé pour votre organisation. Par exemple, vous pouvez trouver des documents qui contiennent des numéros de carte de crédit. Dans ce cas, vous devez utiliser le format suivant: `SensitiveType:"Credit Card Number"`. Étant donné que vous n'avez pas inclus une plage de nombre ou une plage de confiance, la requête renvoie tous les documents dans lesquels un numéro de carte de crédit est détecté. Il s'agit de la requête la plus simple que vous pouvez exécuter et renvoie le plus de résultats. N'oubliez pas que l'orthographe et l'espacement du type sensible sont importants. 
  
### <a name="ranges---optional"></a>Plages - facultatives

Les deux parties suivantes sont des plages, donc examinons rapidement à quoi ressemble une plage. Dans les requêtes DLP de SharePoint, une plage de base est représentée par deux nombres séparés par deux points, à savoir `[number]..[number]`:. Par exemple, si `10..20` est utilisé, cette plage capturerait les numéros de 10 à 20. Il existe de nombreuses combinaisons de plage différentes et plusieurs sont abordées dans cette rubrique. 
  
Nous allons ajouter une plage de nombre à la requête. Vous pouvez utiliser la plage de nombre pour définir le nombre d'occurrences d'informations sensibles qu'un document doit contenir avant qu'il ne soit inclus dans les résultats de la requête. Par exemple, si vous souhaitez que votre requête renvoie uniquement les documents qui contiennent exactement cinq numéros de carte de crédit, `SensitiveType:"Credit Card Number|5"`utilisez ce qui suit:. La plage de nombre peut également vous aider à identifier les documents qui présentent de hauts niveaux de risque. Par exemple, votre organisation peut considérer comme des documents ayant au moins cinq numéros de carte de crédit un risque élevé. Pour rechercher les documents qui composent ce critère, utilisez la `SensitiveType:"Credit Card Number|5.."`requête suivante:. Vous pouvez également rechercher des documents contenant au moins cinq numéros de carte de crédit à l'aide de `SensitiveType:"Credit Card Number|..5"`cette requête:. 
  
#### <a name="confidence-range"></a>Plage de confiance

Enfin, la plage de confiance est le niveau de confiance que le type sensible détecté est effectivement une correspondance. Les valeurs de la plage de confiance fonctionnent de la même manière que la plage de comptage. Vous pouvez créer une requête sans inclure de plage de nombre. Par exemple, pour rechercher des documents comportant n'importe quel nombre de numéros de carte de crédit, si la plage de confiance est de 85% ou plus, vous utiliserez cette requête: `SensitiveType:"Credit Card Number|*|85.."`. 
  
> [!IMPORTANT]
> L'astérisque ( `*`) est un caractère générique qui signifie que n'importe quelle valeur fonctionne. Vous pouvez utiliser le caractère générique ( `*`) dans la plage de nombre ou dans la plage de confiance, mais pas dans un type sensible. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>Propriétés de requête supplémentaires et opérateurs de recherche disponibles dans le centre eDiscovery

DLP dans SharePoint introduit également la propriété LastSensitiveContentScan, qui peut vous aider à rechercher des fichiers analysés dans une période spécifique. Pour obtenir des exemples de `LastSensitiveContentScan` requête avec la propriété, consultez les [exemples de requêtes complexes](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) dans la section suivante. 
  
Vous pouvez utiliser non seulement des propriétés spécifiques à DLP pour créer une requête, mais aussi des propriétés de recherche de découverte `Author` électronique `FileExtension`SharePoint standard, telles que ou. Vous pouvez utiliser des opérateurs pour créer des requêtes complexes. Pour obtenir la liste des propriétés et des opérateurs disponibles, consultez la rubrique [utilisation des propriétés et des opérateurs de recherche avec](https://go.microsoft.com/fwlink/?LinkId=510093) le billet de blog eDiscovery. 
  
## <a name="examples-of-complex-queries"></a>Exemples

Les exemples suivants utilisent différents types, propriétés et opérateurs sensibles pour illustrer la manière dont vous pouvez affiner vos requêtes pour trouver exactement ce que vous recherchez.
  
|**Rogation**|**Explication**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |Le nom peut sembler étrange, car il est tellement long, mais il s'agit du nom correct pour ce type sensible. Veillez à utiliser des noms exacts à partir de l' [inventaire des types d'informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999). Vous pouvez également utiliser le nom d'un [type d'informations sensibles personnalisé](create-a-custom-sensitive-information-type.md) que vous avez créé pour votre organisation.<br/> |
| `SensitiveType:"Credit Card Number|1..4294967295|1..100"` <br/> |Renvoie les documents avec au moins une correspondance au type sensible «numéro de carte de crédit». Les valeurs de chaque plage sont les valeurs minimale et maximale respectives. Un moyen plus simple d'écrire cette requête est `SensitiveType:"Credit Card Number"`, mais où se trouve le plaisir?<br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018"` <br/> |Cette fonction renvoie des documents avec 5-25 numéros de carte de crédit qui ont été analysés le 11 août, 2018 et 13 août 2018.  <br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018" NOT FileExtension:XLSX` <br/> |Cette fonction renvoie des documents avec 5-25 numéros de carte de crédit qui ont été analysés le 11 août, 2018 et 13 août 2018. Les fichiers avec une extension XLSX ne sont pas inclus dans les résultats de la requête.  `FileExtension` est l'une des nombreuses propriétés que vous pouvez inclure dans une requête. Pour plus d'informations, voir [utilisation des propriétés de recherche et des opérateurs avec eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093).<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |Cela renvoie les documents contenant un numéro de carte de crédit ou un numéro de sécurité sociale.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>Exemples

Toutes les requêtes ne sont pas égales. Le tableau suivant donne des exemples de requêtes qui ne fonctionnent pas avec DLP dans SharePoint et explique pourquoi.
  
|**Requête non prise en charge**|**Reason**|
|:-----|:-----|
| `SensitiveType:"Credit Card Number|.."` <br/> |Vous devez ajouter au moins un nombre.  <br/> |
| `SensitiveType:"NotARule"` <br/> |«NotARule» n'est pas un nom de type sensible valide. Seuls les noms des [types d'informations sensibles stockent](https://go.microsoft.com/fwlink/?LinkID=509999) le travail dans les requêtes DLP.<br/> |
| `SensitiveType:"Credit Card Number|0"` <br/> |Zéro n'est pas valide comme valeur minimale ou valeur maximale dans une plage.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |Il peut être difficile de voir, mais il y a un espace supplémentaire entre «crédit» et «carte» qui rend la requête incorrecte. Utilisez des noms de types sensibles exactes à partir de l' [inventaire des types d'informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999).<br/> |
| `SensitiveType:"Credit Card Number|1. .3"` <br/> |La partie deux périodes ne doit pas être séparée par un espace.  <br/> |
| `SensitiveType:"Credit Card Number| |1..|80.."` <br/> |Il y a trop de délimiteurs de canaux (|). Suivez ce format à la place:`SensitiveType: "Credit Card Number|1..|80.."` <br/> |
| `SensitiveType:"Credit Card Number|1..|80..101"` <br/> |Étant donné que les valeurs de confiance représentent un pourcentage, elles ne peuvent pas dépasser 100. Choisissez plutôt un nombre compris entre 1 et 100.  <br/> |
   
## <a name="for-more-information"></a>Pour plus d’informations

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
  
[Exécuter une recherche de contenu dans le centre de &amp; sécurité conformité Office 365](run-a-content-search-in-the-security-and-compliance-center.md)
  
[Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
  

