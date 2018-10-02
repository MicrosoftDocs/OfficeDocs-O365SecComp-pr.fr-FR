---
title: Limites pour la recherche de contenu dans la sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/30/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: 'En savoir plus sur les limites en vigueur pour la fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité, telles que le nombre maximal de recherches simultanées. '
ms.openlocfilehash: 917351f380c81ebfabfd4b3ff05a534c65c8f318
ms.sourcegitcommit: b6473cd6ba3f9ac79dc6a2040fc148020dfbe464
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "25358373"
---
# <a name="limits-for-content-search-in-the-office-365-security-amp-compliance-center"></a>Limites pour la recherche de contenu dans la sécurité Office 365 &amp; centre de conformité

> [!NOTE]
> Les limites de cette rubrique sont différentes des limites en cours pour la découverte électronique inaltérable dans Exchange Online et pour le centre eDiscovery dans SharePoint Online. 
  
Différentes limites s’appliquent à la fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité. Cette recherche include exécuté sur la page de **recherche de contenu** et de la recherche qui sont associés à une affaire eDiscovery. Ces limites permettant d’assurer l’intégrité et la qualité des services fournis aux organisations Office 365. Il existe également des limites liées à l’indexation des messages électroniques dans Exchange Online pour la recherche. Vous ne pouvez pas modifier la recherche de contenu ou l’indexation des limites de messagerie, mais vous devez connaître les afin que ces limites peut prendre en considération lors de la planification, en cours d’exécution et le dépannage des recherches de contenu. 
  
 **Contenu de cette rubrique**
  
[Limites de la recherche de contenu](limits-for-content-search.md#searchlimits)
  
[L’indexation des limites pour les messages électroniques](limits-for-content-search.md#indexinglimits)
  
[Plus d’informations](limits-for-content-search.md#moreinfo)
  
## <a name="content-search-limits"></a>Limites de la recherche de contenu
<a name="searchlimits"> </a>

Le tableau suivant répertorie les limites de recherche dans la sécurité &amp; centre de conformité.
  
|**Description de la limite**|**Limite**|
|:-----|:-----|
|Le nombre maximal de boîtes aux lettres ou des sites qui peuvent être recherchées dans une seule recherche de contenu  <br/> |Aucune limite  <br/> |
|Le nombre maximal de recherches de contenu qui peut être exécuté en même temps dans votre organisation.  <br/> |Aucune limite  <br/> |
|Le nombre maximal de recherches de contenu qu’un utilisateur unique peut lancer en même temps. Notez que cette limite est atteinte plus probablement lorsque l’utilisateur tente de démarrer plusieurs recherches à l’aide de la **Get-ComplianceSearch \| ComplianceSearch-démarrer** commande PowerShell de centre de conformité et de sécurité.<br/> |10   <br/> |
|Le nombre maximal d’éléments par boîte aux lettres de l’utilisateur qui s’affichent sur la page d’aperçu lors de l’aperçu des résultats de la recherche de contenu.  <br/> |100  <br/> |
|Le nombre maximal d’éléments trouvés dans toutes les boîtes aux lettres utilisateur sont affichés dans la page Aperçu lors de l’aperçu des résultats de la recherche de contenu. Les éléments les plus récents sont affichés.  <br/> |1 000  <br/> |
|Le nombre maximal de boîtes aux lettres d’utilisateur qui peuvent être affichés pour les résultats de la recherche. S’il n’y a plus de 1 000 boîtes aux lettres qui contiennent du contenu qui correspond à la requête de recherche, uniquement les principaux 1000 boîtes aux lettres avec les résultats de recherche plus sera disponibles pour l’aperçu.  <br/> |1 000  <br/> |
|Le nombre maximal d’éléments trouvés dans SharePoint et OneDrive pour les sites entreprise qui sont affichés sur la page d’aperçu lors de l’aperçu des résultats de la recherche de contenu. Les éléments les plus récents sont affichés.  <br/> |200  <br/> |
|Le nombre maximal de sites qui peuvent être affichés pour les résultats de la recherche (dans SharePoint et OneDrive entreprise). S’il y a plus de 200 sites total qui contiennent du contenu qui correspond à la requête de recherche, uniquement les sites récurrents 200 avec les résultats de recherche plus sera disponibles pour l’aperçu.  <br/> |200  <br/> |
|Le nombre maximal d’éléments par boîte aux lettres de dossiers publics qui sont affichés sur la page d’aperçu lors de l’aperçu des résultats de la recherche de contenu.  <br/> |100  <br/> |
|Le nombre maximal d’éléments trouvés dans toutes les boîtes aux lettres de dossiers publics qui sont affichés sur la page d’aperçu lors de l’aperçu des résultats de la recherche de contenu.  <br/> |200  <br/> |
|Le nombre maximal de boîtes aux lettres publiques qui peuvent être affichés pour les résultats de la recherche. S’il n’y a plus de 500 boîtes aux lettres de dossiers publics qui contiennent du contenu qui correspond à la requête de recherche, uniquement les principaux 500 dossiers publics boîtes aux lettres avec les résultats de recherche plus sera disponibles pour l’aperçu.  <br/> |500  <br/> |
|Le nombre maximal de caractères de la requête de recherche (y compris les opérateurs et conditions) pour une recherche de contenu.  <br/><br/> **Remarque :** Cette limite prend effet une fois que la requête est développée, ce qui signifie que la requête sera obtenir développée par rapport à chacun des mots clés. Par exemple, si une requête de recherche a 15 mots clés et des paramètres supplémentaires et conditions, la requête est développée 15 heures, chacun avec les paramètres et les conditions dans la requête. Même si le nombre de caractères dans la requête de recherche peut-être être inférieures à la limite, il est donc la requête étendue qui peut-être contribuer à le dépassement de cette limite.<br/> |**Boîtes aux lettres :** 10 000  <br/> **Sites :** lors de la recherche de tous les sites ou 2 000 lors de la recherche de sites jusqu'à 20 <sup>1</sup> à 4 000 <br/> |
|Nombre maximal de variantes renvoyé lors de l’utilisation d’un caractère générique préfixe pour rechercher une phrase exacte dans une requête de recherche ou lors de l’utilisation d’un caractère générique préfixe et l’opérateur booléen **NEAR** ou **ONEAR** .  <br/> |10 000 <sup>2</sup> <br/> |
|Le nombre minimal de caractères alpha pour des caractères génériques de préfixe ; par exemple, `time*`, `one*`, ou `set*`.  <br/> |3   <br/> |
|Le nombre maximal de boîtes aux lettres dans une recherche de contenu que vous pouvez supprimer les éléments dans en effectuant une action « recherche et purge » (à l’aide de la **ComplianceSearchAction-New-purger** commande). Si la recherche de contenu que vous effectuez une action de vidage pour possède plusieurs boîtes aux lettres source à cette limite, l’action de purge échouera. Pour plus d’informations sur la recherche et la purge, voir [Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md).<br/> |50 000  <br/> |
   
> [!NOTE]
> <sup>1</sup> lors de la recherche SharePoint et OneDrive pour des sites, les caractères dans les URL des sites recherchés sont comptés par rapport à cette limite.<br/> <sup>2</sup> pour les requêtes non phrase (une valeur de mot clé qui n’utilise pas de doubles guillemets) nous utilisons un index préfixe spécial. Nous indique qu’un mot se produit dans un document, mais pas où il se trouve dans le document. Pour faire une requête d’expression (une valeur de mot clé entre guillemets doubles), nous devons comparer la position dans le document pour les mots dans la phrase. Cela signifie que nous ne pouvons pas utiliser l’index de préfixe pour les requêtes d’une expression. Dans ce cas, nous allons élargir en interne la requête avec tous les mots possibles qui développe le préfixe ; par exemple, `"time*"` peut se développer pour `"time OR timer OR times OR timex OR timeboxed OR …"`. 10 000 est le nombre maximal de variantes que peut en modifier le mot pas le nombre de documents correspondant à la requête. Il n’existe aucune limite supérieure pour les termes non phrase. 
  
[Return to top](limits-for-content-search.md#top)
  
## <a name="indexing-limits-for-email-messages"></a>L’indexation des limites pour les messages électroniques
<a name="indexinglimits"> </a>

Le tableau suivant décrit les limites d’indexation pouvant entraîner un message électronique est renvoyé comme un élément non indexé ou d’un élément partiellement indexé dans les résultats d’une recherche de contenu.
  
|**Limite d’indexation**|**Commentaires**|**Description**|
|:-----|:-----|:-----|
|Taille maximale des pièces jointes (à l’exclusion de fichiers Excel)  <br/> |150 Mo  <br/> |La taille maximale d’une pièce jointe qui analysera pour l’indexation. Toutes les pièces jointes sont supérieure à cette limite ne sont pas être analysée pour l’indexation et le message avec la pièce jointe est marqué comme partiellement indexé.<br/> <br/>**Remarque :** L’analyse est le processus où le service d’indexation extrait le texte de la pièce jointe, supprime les caractères tels que des signes de ponctuation et les espaces inutiles et divise le texte en mots (dans un processus appelé création de jetons), qui sont stockés dans l’index.           |
|Taille maximale des fichiers Excel  <br/> |4 MO  <br/> |La taille maximale d’un fichier Excel située sur un site ou attaché à un message électronique qui sera analysé pour l’indexation. N’importe quel fichier Excel supérieur à cette limite ne sont pas être analysée, et le fichier ou le courrier électronique le message avec la pièce jointe est marqué comme non indexés.  <br/> |
|Nombre maximal de pièces jointes  <br/> |250  <br/> |Le nombre maximal de fichiers joints à un message électronique qui sera analysé pour l’indexation. Si un message contient plus de 250 pièces jointes, les pièces 250 premiers jointes sont analysés et indexés, et le message est marqué comme partiellement indexé parce qu’il avait des pièces jointes supplémentaires qui n’ont pas été analysés.  <br/> |
|Profondeur maximale des pièces jointes  <br/> |30  <br/> |Le nombre maximal de pièces jointes imbriquées qui sont analysés. Par exemple, si un message électronique est un autre message attaché et le message joint est un document Word joint, le document Word et le message joint seront indexés. Ce comportement continuera de pièces jointes imbriquées jusqu'à 30.  <br/> |
|Nombre maximal d’images attachés  <br/> |0  <br/> |Une image qui est attachée à un message électronique est ignorée par l’analyseur et n’est pas indexée.  <br/> |
|Durée maximale passé à l’analyse d’un élément  <br/> |30 secondes  <br/> |Un maximum de 30 secondes est passé à l’analyse d’un élément pour l’indexation. Si la durée d’analyse dépasse 30 secondes, l’élément est marqué comme étant partiellement indexé.  <br/> |
|Sortie de l’analyseur maximale  <br/> |2 millions de caractères  <br/> |La quantité maximale de sortie de texte de l’analyseur qui est indexée. Par exemple, si l’analyseur extrait 8 millions de caractères à partir d’un document, uniquement les premiers 2 millions de caractères sont indexées.  <br/> |
|Jetons d’annotation maximale  <br/> |2 millions  <br/> |Lorsqu’un message électronique est indexé, chaque mot est annoté avec des instructions de traitement qui spécifient comment que word doit être indexée. Chaque jeu d’instructions de traitement est appelé un jeton d’annotation. Pour maintenir la qualité de service dans Office 365, il existe une limite de jetons d’annotation 2 millions d’un message électronique.  <br/> |
|Taille maximale du corps de l’index  <br/> |67 millions de caractères  <br/> |Nombre total de caractères dans le corps d’un message électronique et ses pièces jointes. Lorsqu’un message électronique est indexé, tout le texte dans le corps du message et dans toutes les pièces jointes est concaténé dans une chaîne unique. La taille maximale de cette chaîne qui est indexée est 67 millions de caractères.  <br/> |
|Jetons uniques maximales dans le corps  <br/> |1 million  <br/> |Expliqué précédemment, les jetons sont le résultat de l’extraction du contenu de texte, la suppression des signes de ponctuation et les espaces et divisant en mots (appelées jetons) qui sont stockés dans l’index. Par exemple, l’expression `"cat, mouse, bird, dog, dog"` contient des 5 jetons. Mais uniquement 4 de ces jetons uniques. Il existe une limite de 1 million de jetons unique par message électronique, ce qui permet d’empêcher l’index devient trop importante avec des jetons aléatoires.<br/> |
   
[Return to top](limits-for-content-search.md#top)
  
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

Il existe des aspects liés aux différentes limites supplémentaires de la recherche de contenu, tels que l’exportation des résultats de la recherche et l’indexation de contenu. Pour obtenir une description de ces limites, consultez les rubriques suivantes :
  
- 
    
- [Éléments partiellement indexés dans la recherche de contenu dans Office 365](partially-indexed-items-in-content-search.md)
    
- [Examen d’éléments partiellement indexés dans eDiscovery Office 365](investigating-partially-indexed-items-in-ediscovery.md)
    
- [Limites de la recherche de SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
Pour plus d’informations sur les recherches de contenu, voir :
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
    
[Return to top](limits-for-content-search.md#top)
  

