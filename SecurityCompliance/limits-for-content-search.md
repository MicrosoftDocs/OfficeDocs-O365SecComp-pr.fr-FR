---
title: Limites de recherche de contenu dans le centre de &amp; sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: 'Découvrez les limites en vigueur pour la fonctionnalité de recherche de contenu dans le centre de &amp; sécurité conformité Office 365, comme le nombre maximal de recherches simultanées. '
ms.openlocfilehash: 711aedf8df80bfe2c769721b8c16b01fb705c289
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213284"
---
# <a name="limits-for-content-search-in-the-office-365-security-amp-compliance-center"></a>Limites de recherche de contenu dans le centre de &amp; sécurité conformité Office 365

> [!NOTE]
> Les limites de cette rubrique sont différentes des limites actuelles de la découverte électronique inaltérable dans Exchange Online et pour le centre eDiscovery dans SharePoint Online. 
  
Différentes limites sont appliquées à la fonctionnalité de recherche de contenu dans le centre &amp; de sécurité conformité Office 365. Cela inclut les recherches exécutées sur la page de **recherche de contenu** et les recherches associées à un cas de découverte électronique. Ces limites contribuent à maintenir l'intégrité et la qualité des services fournis aux organisations Office 365. Il existe également des limites liées à l'indexation des messages électroniques dans Exchange Online pour la recherche. Vous ne pouvez pas modifier la recherche de contenu ou les limites d'indexation de messagerie, mais vous devez en tenir compte pour pouvoir prendre ces limites en considération lors de la planification, de l'exécution et du dépannage des recherches de contenu. 
  
## <a name="content-search-limits"></a>Limites de la recherche de contenu

Le tableau suivant répertorie les limites de recherche dans &amp; le centre de sécurité et de conformité.
  
|**Description de la limite**|**Limite**|
|:-----|:-----|
|Nombre maximal de boîtes aux lettres ou de sites qui peuvent être recherchées dans une recherche de contenu unique  <br/> |Sans limite  <br/> |
|Nombre maximal de recherches de contenu pouvant être exécutées en même temps dans votre organisation.  <br/> |Sans limite  <br/> |
|Nombre maximal de recherches de contenu qu'un utilisateur peut démarrer simultanément. Notez que cette limite est probablement atteinte lorsque l'utilisateur tente de démarrer plusieurs recherches à l'aide de la commande **get \| -ComplianceSearch Start-ComplianceSearch** dans le centre de sécurité & Compliance Center PowerShell.<br/> |10   <br/> |
|Nombre maximal d'éléments par boîte aux lettres utilisateur qui s'affichent dans la page d'aperçu lors de la prévisualisation des résultats de la recherche de contenu.  <br/> |100  <br/> |
|Nombre maximal d'éléments trouvés dans toutes les boîtes aux lettres utilisateur qui s'affichent dans la page d'aperçu lors de la prévisualisation des résultats de la recherche de contenu. Les éléments les plus récents sont affichés.  <br/> |1,000  <br/> |
|Nombre maximal de boîtes aux lettres utilisateur pouvant être prévisualisées pour les résultats de la recherche. S'il y a plus de 1000 boîtes aux lettres qui contiennent du contenu correspondant à la requête de recherche, seules les 1000 premières boîtes aux lettres avec le plus de résultats de recherche seront disponibles pour l'aperçu.  <br/> |1,000  <br/> |
|Nombre maximal d'éléments trouvés dans SharePoint et de sites OneDrive entreprise affichés dans la page d'aperçu lors de la prévisualisation des résultats de la recherche de contenu. Les éléments les plus récents sont affichés.  <br/> |200  <br/> |
|Nombre maximal de sites (dans SharePoint et OneDrive entreprise) pouvant être prévisualisés pour les résultats de la recherche. S'il existe plus de 200 total de sites qui contiennent du contenu correspondant à la requête de recherche, seuls les premiers sites 200 avec le plus de résultats de recherche seront disponibles pour l'aperçu.  <br/> |200  <br/> |
|Nombre maximal d'éléments par boîte aux lettres de dossiers publics affichés dans la page d'aperçu lors de la prévisualisation des résultats de la recherche de contenu.  <br/> |100  <br/> |
|Nombre maximal d'éléments trouvés dans toutes les boîtes aux lettres de dossiers publics qui s'affichent dans la page d'aperçu lors de la prévisualisation des résultats de la recherche de contenu.  <br/> |200  <br/> |
|Nombre maximal de boîtes aux lettres publiques pouvant être prévisualisées pour les résultats de la recherche. S'il y a plus de 500 boîtes aux lettres de dossiers publics qui contiennent du contenu correspondant à la requête de recherche, seules les 500 premières boîtes aux lettres de dossiers publics avec le plus de résultats de recherche seront disponibles pour l'aperçu.  <br/> |500  <br/> |
|Nombre maximal de caractères pour la requête de recherche (y compris les opérateurs et les conditions) pour une recherche de contenu.  <br/><br/> **Remarque:** Cette limite prend effet après l'extension de la requête, ce qui signifie que la requête est développée par rapport à chacun des mots clés. Par exemple, si une requête de recherche comporte 15 Mots clés et des paramètres et conditions supplémentaires, la requête est développée 15 fois, chacune avec les autres paramètres et conditions de la requête. Par conséquent, même si le nombre de caractères dans la requête de recherche est inférieur à la limite, il s'agit de la requête étendue susceptible de contribuer au dépassement de cette limite.<br/> |**Boîtes aux lettres:** 10 000  <br/> **Sites:** 4 000 lors de la recherche sur tous les sites ou 2 000 lors de la recherche sur 20 sites <sup>1</sup> <br/> |
|Nombre maximal de variantes renvoyées lors de l'utilisation d'un caractère générique de préfixe pour rechercher une expression exacte dans une requête de recherche ou lorsque vous utilisez un caractère générique de préfixe et l'opérateur booléen **near** ou **ONEAR** .  <br/> |10 000 <sup>2</sup> <br/> |
|Nombre minimal de caractères alpha pour les caractères génériques de préfixe; par exemple, `time*` `one*`, ou `set*`.  <br/> |3   <br/> |
|Nombre maximal de boîtes aux lettres dans une recherche de contenu que vous pouvez supprimer des éléments à l'aide d'une action de recherche et de purge (à l'aide de la commande **New-ComplianceSearchAction-purge** ). Si la recherche de contenu pour laquelle vous effectuez une action de vidage pour a plus de boîtes aux lettres source que cette limite, l'action de vidage échouera. Pour plus d'informations sur la recherche et le vidage, voir [Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md).<br/> |50 000  <br/> |
   
> [!NOTE]
> <sup>1</sup> lors de la recherche de sites SharePoint et OneDrive entreprise, les caractères des URL des sites en cours de recherche sont comptabilisés par rapport à cette limite.<br/> <sup>2</sup> pour les requêtes sans expression (valeur de mot clé qui n'utilise pas de guillemets doubles), nous utilisons un index de préfixe spécial. Cela indique qu'un mot a lieu dans un document, mais pas à son emplacement dans le document. Pour effectuer une requête d'expression (valeur de mot clé avec des guillemets doubles), nous devons comparer la position dans le document pour les mots de l'expression. Cela signifie que nous ne pouvons pas utiliser l'index de préfixe pour les requêtes d'expression. Dans ce cas, nous développons la requête en interne avec tous les mots que le préfixe développe; par exemple, `"time*"` peut se développer `"time OR timer OR times OR timex OR timeboxed OR …"`sur. 10 000 est le nombre maximal de variantes que le mot peut développer, pas le nombre de documents correspondant à la requête. Il n'existe pas de limite supérieure pour les termes autres que les expressions. 
  
## <a name="indexing-limits-for-email-messages"></a>Limites d'indexation pour les messages électroniques

Le tableau suivant décrit les limites d'indexation qui peuvent entraîner le renvoi d'un message électronique sous la forme d'un élément non indexé ou partiellement indexé dans les résultats d'une recherche de contenu.
  
|**Limite d'indexation**|**Commentaires**|**Description**|
|:-----|:-----|:-----|
|Taille maximale des pièces jointes (à l'exception des fichiers Excel)  <br/> |150 Mo  <br/> |Taille maximale d'une pièce jointe de courrier électronique qui analysera l'indexation. Toute pièce jointe dont la taille est supérieure à cette limite n'est pas analysée pour l'indexation et le message avec la pièce jointe est marqué comme partiellement indexé.<br/> <br/>**Remarque:** L'analyse est le processus dans lequel le service d'indexation extrait le texte de la pièce jointe, supprime les caractères superflus, tels que la ponctuation et les espaces, puis divise le texte en mots (dans un processus appelé «tokening»), qui sont ensuite stockés dans l'index.           |
|Taille maximale des fichiers Excel  <br/> |4 MO  <br/> |Taille maximale d'un fichier Excel situé sur un site ou jointe à un message électronique qui sera analysé pour l'indexation. Tout fichier Excel dont la taille est supérieure à cette limite n'est pas analysé, et le fichier ou le message électronique avec le fichier joint est marqué comme non indexée.  <br/> |
|Nombre maximal de pièces jointes  <br/> |250  <br/> |Nombre maximal de fichiers joints à un message électronique qui seront analysés pour l'indexation. Si un message contient plus de 250 pièces jointes, les 250 premières pièces jointes sont analysées et indexées, et le message est marqué comme partiellement indexé car il contient des pièces jointes supplémentaires qui n'ont pas été analysées.  <br/> |
|Profondeur maximale des pièces jointes  <br/> |0,30  <br/> |Nombre maximal de pièces jointes imbriquées qui sont analysées. Par exemple, si un message électronique est associé à un autre message et que le message joint contient un document Word joint, le document Word et le message joint sont indexés. Ce comportement se poursuivra pendant jusqu'à 30 pièces jointes imbriquées.  <br/> |
|Nombre maximal d'images attachées  <br/> |0  <br/> |Une image jointe à un message électronique est ignorée par l'analyseur et n'est pas indexée.  <br/> |
|Temps maximal passé à analyser un élément  <br/> |30 secondes  <br/> |Un maximum de 30 secondes est passé à analyser un élément pour l'indexation. Si la durée d'analyse est supérieure à 30 secondes, l'élément est marqué comme partiellement indexé.  <br/> |
|Sortie maximale de l'analyseur  <br/> |2 millions de caractères  <br/> |Quantité maximale de sortie de texte de l'analyseur qui est indexée. Par exemple, si l'analyseur a extrait 8 millions caractères d'un document, seuls les 2 premiers caractères sont indexés.  <br/> |
|Nombre maximal de jetons d'annotation  <br/> |2 millions  <br/> |Lorsqu'un message électronique est indexé, chaque mot est annoté avec des instructions de traitement différentes qui définissent le mode d'indexation de Word. Chaque ensemble d'instructions de traitement est appelé un jeton d'annotation. Pour maintenir la qualité de service dans Office 365, il existe une limite de 2 millions jetons d'annotation pour un message électronique.  <br/> |
|Taille maximale du corps dans l'index  <br/> |67 millions caractères  <br/> |Nombre total de caractères dans le corps d'un message électronique et toutes ses pièces jointes. Lorsqu'un message électronique est indexé, tout le texte dans le corps du message et dans toutes les pièces jointes est concaténé dans une chaîne unique. La taille maximale de cette chaîne indexée est de 67 millions caractères.  <br/> |
|Nombre maximal de jetons uniques dans le corps  <br/> |1 million  <br/> |Comme expliqué précédemment, les jetons sont le résultat de l'extraction de texte du contenu, la suppression de la ponctuation et des espaces, puis sa division en mots (appelés jetons) stockés dans l'index. Par exemple, l'expression `"cat, mouse, bird, dog, dog"` contient 5 jetons. Mais seulement 4 sont des jetons uniques. Il existe une limite de 1 million jetons uniques par message électronique, ce qui permet d'éviter que l'index soit trop volumineux avec des jetons aléatoires.<br/> |
  
## <a name="more-information"></a>Plus d’informations

Il existe des limites supplémentaires liées à différents aspects de la recherche de contenu, telles que l'exportation des résultats de recherche et l'indexation du contenu. Pour obtenir une description de ces limites, consultez les rubriques suivantes:
  
- [Exporter les résultats de la recherche de contenu](export-search-results.md#export-limits)
    
- [Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)
    
- [Examen d’éléments partiellement indexés dans eDiscovery Office 365](investigating-partially-indexed-items-in-ediscovery.md)
    
- [Limites de recherche pour SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
Pour plus d'informations sur les recherches de contenu, voir:
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
