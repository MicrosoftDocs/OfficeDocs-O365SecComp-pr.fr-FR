---
title: Créer une requête pour trouver des données sensibles stockées sur des sites
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: Avec data loss prevention (DLP) dans SharePoint Online, vous pouvez découvrir des documents qui contiennent des données sensibles au sein de votre client. Après avoir découvert les documents, vous pouvez travailler avec les propriétaires de document pour protéger les données. Cette rubrique peut vous aider à créer une requête pour rechercher des données sensibles.
ms.openlocfilehash: c30cb2e4b93e1a7db90f3e3f922f406285c6f692
ms.sourcegitcommit: 81e06e09bf5ca8e3f51b164d6251b1c35b3285cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "25829185"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>Créer une requête pour trouver des données sensibles stockées sur des sites

Les utilisateurs souvent stockent des données sensibles, telles que des numéros de carte de crédit, numéros de sécurité sociale, ou personnel, sur leurs sites et au fil du temps cela peut exposer une organisation à risque de perte de données. Documents stockés sur les sites, notamment OneDrive pour les sites — peuvent être partagés avec des personnes en dehors de l’organisation qui ne doit pas avoir accès aux informations. Avec data loss prevention (DLP) dans SharePoint Online, vous pouvez découvrir des documents qui contiennent des données sensibles au sein de votre client. Après avoir découvert les documents, vous pouvez travailler avec les propriétaires de document pour protéger les données. Cette rubrique peut vous aider à créer une requête pour rechercher des données sensibles.
  
> [!NOTE]
> Découverte électronique, ou eDiscovery et DLP sont les fonctionnalités premium qui nécessitent [SharePoint Online Plan 2](https://go.microsoft.com/fwlink/?LinkId=510080). 
  
## <a name="forming-a-basic-dlp-query"></a>Création d'une requête DLP de base

Il existe trois composants qui constituent une requête de base DLP : SensitiveType, compter les plages et confiance. Comme illustré dans le graphique suivant, **SensitiveType : «\<type\>»** est nécessaire et les deux**|\<count plage\> ** et**|\<plage confiance\> ** sont facultatives. 
  
![Exemple de requête divisée en obligatoire et facultative](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>Type d'informations sensibles - Obligatoire

Qu’est chaque composant ? Requêtes de SharePoint DLP généralement commencent par la propriété `SensitiveType:"` et un type d’information de nom à partir de l' [inventaire types d’informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999)et se termine par un `"`. Vous pouvez également utiliser le nom d’un [type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md) que vous avez créé pour votre organisation. Par exemple, que vous recherchez des documents contenant des numéros de carte de crédit. Dans ce cas, vous utiliseriez le format suivant : `SensitiveType:"Credit Card Number"`. Étant donné que vous n’avez pas confiance plage ou count, la requête renvoie tous les documents dans lesquels un numéro de carte de crédit est détecté. Il s’agit de la requête plus simple que vous pouvez exécuter, et elle renvoie les résultats de la plupart des. N’oubliez pas que l’orthographe et l’espacement du type sensible est importante. 
  
### <a name="ranges---optional"></a>Plages - facultatives

Les deux les deux composants sont plages, examinons rapidement examiner ce à quoi ressemble une plage. Dans les requêtes de SharePoint DLP, une plage de base est représentée par deux chiffres séparés par deux points, ce qui ressemble à ceci : `[number]..[number]`. Par exemple, si `10..20` est utilisé, cette plage de capturer les numéros de 10 à 20. Il existe plusieurs combinaisons différentes plage et plusieurs sont abordées dans cette rubrique. 
  
Ajoutons une tranche à la requête. Vous pouvez utiliser la plage de nombre pour définir le nombre d’occurrences d’informations sensibles, qu'un document doit contenir avant qu’il est inclus dans les résultats de requête. Par exemple, si vous souhaitez que la requête renvoie uniquement les documents qui contiennent des numéros de carte de crédit exactement cinq, utilisez ce : `SensitiveType:"Credit Card Number|5"`. Tranche peut également vous aider à identifier les documents qui présentent des degrés de risque. Par exemple, votre organisation peut prendre en compte les documents avec cinq ou plusieurs numéros de carte de crédit un risque élevé. Pour rechercher des documents, à raison de ce critère, vous utiliseriez cette requête : `SensitiveType:"Credit Card Number|5.."`. Sinon, vous pouvez rechercher des documents avec cinq ou moins les numéros de carte de crédit à l’aide de cette requête : `SensitiveType:"Credit Card Number|..5"`. 
  
#### <a name="confidence-range"></a>Plage de confiance

Enfin, la plage de niveau de confiance est le niveau de confiance que le type de sensible détecté est en fait une correspondance. Les valeurs de la plage de confiance fonctionnent de la même façon à compter de plage. Vous pouvez former une requête sans y compris une plage de nombre. Par exemple, pour rechercher des documents avec n’importe quel nombre de numéros de carte de crédit, tant que la plage de niveau de confiance est de 85 pour cent ou plus, vous devez utiliser cette requête : `SensitiveType:"Credit Card Number|*|85.."`. 
  
> [!IMPORTANT]
> L’astérisque ( `*`) est un caractère générique qui signifie que tout fonctionne de la valeur. Vous pouvez utiliser le caractère générique ( `*`) dans la plage de nombre ou de la plage de niveau de confiance, mais pas dans un type sensible. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>Propriétés de requête supplémentaires et opérateurs de recherche disponibles dans le centre eDiscovery

DLP dans SharePoint introduit également la LastSensitiveContentScan propriété, qui peut vous aider à rechercher des fichiers analysés au sein d’une période spécifique. Pour des exemples de requête avec le `LastSensitiveContentScan` propriété, consultez les [exemples de requêtes complexes](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) dans la section suivante. 
  
Vous pouvez utiliser des propriétés spécifiques DLP pour créer une requête, mais aussi propriétés de recherche de découverte électronique SharePoint standard, tel que `Author` ou `FileExtension`. Vous pouvez utiliser des opérateurs pour créer des requêtes complexes. Pour la liste des propriétés disponibles et les opérateurs, consultez le blog [à l’aide des propriétés de recherche et les opérateurs eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093) . 
  
## <a name="examples-of-complex-queries"></a>Exemples

Les exemples suivants utilisent différents types sensibles, des propriétés et des opérateurs pour illustrer comment vous pouvez affiner vos requêtes pour trouver exactement ce que vous cherchez.
  
|**Requête**|**Explication**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |Le nom peut sembler étrange, car il est autant de temps, mais il est le nom correct de ce type sensible. Veillez à utiliser le nom exact de l' [inventaire des types d’informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999). Vous pouvez également utiliser le nom d’un [type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md) que vous avez créé pour votre organisation.<br/> |
| « SensitiveType : numéro de carte de crédit »|1..4294967295|1..100"' <br/> |Cela renvoie les documents contenant au moins une correspondance au type sensible « Numéro de carte de crédit. » Les valeurs pour chaque plage sont les valeurs minimales et maximales respectifs. Un moyen plus simple pour écrire cette requête est `SensitiveType:"Credit Card Number"`, mais où est la fête qui ?<br/> |
| « SensitiveType : numéro de carte de crédit »| 5..25" et LastSensitiveContentScan:"8/11/2018..8/13/2018 « » <br/> |Il en résulte des documents avec des numéros de carte de crédit 5-25 qui ont été analysés à partir de 11 août 2018 par le biais du 13 août 2018.  <br/> |
| « SensitiveType : numéro de carte de crédit »| 5..25" et LastSensitiveContentScan:"8/11/2018..8/13/2018 « FileExtension:XLSX pas » <br/> |Il en résulte des documents avec des numéros de carte de crédit 5-25 qui ont été analysés à partir de 11 août 2018 par le biais du 13 août 2018. Les fichiers avec une extension XLSX ne sont pas inclus dans les résultats de requête.  `FileExtension` est une des nombreuses propriétés que vous pouvez inclure dans une requête. Pour plus d’informations, voir [utilisation des propriétés de recherche et les opérateurs eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093).<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |Cela renvoie les documents contenant un numéro de carte de crédit ou un numéro de sécurité sociale.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>Exemples

Toutes les requêtes sont égales. Le tableau suivant donne des exemples de requêtes qui ne fonctionnent pas avec DLP dans SharePoint et explique pourquoi.
  
|**Requête non prise en charge**|**Reason**|
|:-----|:-----|
| « SensitiveType : numéro de carte de crédit »|.." ` <br/> |Vous devez ajouter au moins un nombre.  <br/> |
| `SensitiveType:"NotARule"` <br/> |« NotARule » n’est pas un nom valide de type sensibles. Seuls les noms de l' [inventaire des types d’informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999) fonctionnent dans les requêtes DLP.<br/> |
| « SensitiveType : numéro de carte de crédit »|0"' <br/> |Zéro n’est pas valide en tant que la valeur minimale ou la valeur maximale d’une plage.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |Il est peut être difficile de voir, mais il est l’espace supplémentaire entre « Crédit » et « Carte », ce qui rend la requête non valide. Utiliser des noms de type sensibles exact de l' [inventaire des types d’informations sensibles](https://go.microsoft.com/fwlink/?LinkID=509999).<br/> |
| « SensitiveType : numéro de carte de crédit »|1. 3"' <br/> |La partie deux périodes ne doivent pas être séparée par un espace.  <br/> |
| « SensitiveType : numéro de carte de crédit »| |1...|80.. » » <br/> |Il existe trop de barre verticale délimiteurs (|). Respecter le format : « SensitiveType : numéro de carte de crédit »|1...|80.. » » <br/> |
| « SensitiveType : numéro de carte de crédit »|1...|80..101"' <br/> |Étant donné que les valeurs de niveau de confiance représentent un pourcentage, ils ne peut pas dépasser 100. Choisissez un numéro entre 1 et 100 à la place.  <br/> |
   
## <a name="for-more-information"></a>Pour plus d’informations

[Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
  
[Exécuter une recherche de contenu de la sécurité Office 365 &amp; centre de conformité](run-a-content-search-in-the-security-and-compliance-center.md)
  
[Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
  

