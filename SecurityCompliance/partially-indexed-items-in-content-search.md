---
title: Éléments partiellement indexés dans la recherche de contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/11/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.UnindexedItemsLearnMore
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'En savoir plus sur les éléments non indexés dans Exchange et SharePoint que vous pouvez inclure dans une recherche de contenu exécuté par le biais de la sécurité de 365 Office &amp; centre de conformité. '
ms.openlocfilehash: 4624985a9c80313d0222470e6cfb2c56495f2142
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527630"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Éléments partiellement indexés dans la recherche de contenu dans Office 365

Une recherche de contenu que vous exécutez à partir de la sécurité de 365 Office &amp; centre de conformité inclut automatiquement les éléments indexés partiellement dans les résultats de recherche estimés lorsque vous exécutez une recherche. Éléments indexés partiellement sont des éléments de boîte aux lettres Exchange et des documents dans SharePoint et OneDrive pour les sites d’entreprise qui n’ont pas été entièrement indexés pour la recherche pour une raison quelconque. Dans Exchange, un élément indexé partiellement contient généralement un fichier, d’un type de fichier qui ne peuvent pas être indexé, qui est attaché à un message électronique. Voici quelques autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu’éléments indexés partiellement lorsque vous exécutez une recherche : 
  
- Le type de fichier est non reconnu ou non pris en charge pour l’indexation.
    
-  Les messages ont une pièce jointe sans un gestionnaire valide, tels que les fichiers image ; Il s’agit de la cause la plus courante d’éléments de messagerie partiellement indexé. 
    
- Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique.
    
- Le nombre de fichiers joints à un message électronique est trop important.
    
- Un fichier joint à un message électronique est trop volumineux.
    
- Un fichier est chiffré avec des technologies autres que Microsoft.
    
- Un fichier est protégé par mot de passe.
    
> [!NOTE]
> La plupart des organisations Office 365 ont moins de 1 % du contenu par volume et inférieur à 12 % par taille est partiellement indexé. La raison de la différence entre le volume et la taille est que probabilité contenant le contenu qui ne peuvent pas être indexé complètement les fichiers plus volumineux. 
  
Pour les enquêtes légales, votre organisation peut être nécessaire pour passer en revue les éléments indexés partiellement. Vous pouvez également spécifier s’il faut inclure des éléments indexés partiellement lorsque vous exportez des résultats de la recherche sur un ordinateur local ou lorsque vous vous préparez les résultats d’analyse avec Office 365 avancée de découverte électronique. Pour plus d’informations, voir [Investigating partiellement indexé éléments dans Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Types de fichier non indexés pour la recherche

Certains types de fichiers, tels que Bitmap ou les fichiers MP3 ne contiennent pas le contenu qui peut être indexé. Par conséquent, la recherche d’indexation des serveurs Exchange et SharePoint n’effectuent pas l’indexation de texte intégral sur ces types de fichiers. Ces types de fichiers sont considérés comme des types de fichiers non pris en charge. Il existe également des types de fichiers pour lesquels l’indexation de texte intégral a été désactivé, par défaut ou par un administrateur. Types de fichiers non pris en charge et désactivés sont étiquetées en tant qu’éléments non indexés dans les recherches de contenu. Comme indiqués précédemment, partiellement indexés éléments peuvent être inclus dans le jeu de résultats de recherche lorsque vous exécutez une recherche, exporter les résultats de recherche vers un ordinateur local, ou préparer des résultats de la recherche avancée eDiscovery. 
  
Pour obtenir une liste de formats de fichier pris en charge et désactivés, consultez les rubriques suivantes :
  
- **Exchange** - [formats de fichiers indexés par la recherche Exchange](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **Exchange** - [Get-SearchDocumentFormat](https://go.microsoft.com/fwlink/p/?LinkID=724037)
    
- **SharePoint** - [extensions de nom de fichier et analysés par défaut des types de fichiers dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkID=404033)
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Messages et des documents avec partiellement indexé fichier types peuvent être renvoyés dans les résultats de recherche

Non à chaque message électronique comportant une pièce jointe de fichiers indexés partiellement ou tous les documents indexés partiellement SharePoint sont renvoyé automatiquement comme un élément partiellement indexé. C’est parce que l’autre message ou des propriétés de document, telles que la propriété **Subject** dans les messages électroniques et les propriétés de **titre** ou **l’auteur** des documents sont indexés et prêts à être recherché. Par exemple, une recherche par mot-clé de « financial » renvoie les éléments ayant une pièce jointe de fichiers indexés partiellement si ce mot clé s’affiche dans l’objet d’un message électronique ou le nom de fichier ou le titre d’un document. Toutefois, si le mot clé apparaît uniquement dans le corps du fichier, le message ou le document est retourné en tant qu’un élément partiellement indexé. 
  
De même, messages avec pièces jointes de fichiers indexés partiellement et des documents d’un type de fichier indexés partiellement sont inclus dans les résultats de recherche lorsque d’autres propriétés de message ou un document, qui sont indexés et vous pouvez, aux critères de recherche. Propriétés de message qui sont indexées pour la recherche incluent les dates envoyés et reçus, expéditeur ou destinataire, le nom de fichier d’une pièce jointe et le texte dans le corps du message. Propriétés de document indexées pour la recherche incluent les dates de création et de modification. Ainsi, même si une pièce jointe peut être un élément partiellement indexé, le message sera inclus dans les résultats de recherche standard si la valeur d’autres propriétés de message ou un document correspond aux critères de recherche.
  
Pour obtenir la liste des propriétés de messagerie et de document que vous pouvez rechercher à l’aide de la fonctionnalité de recherche dans la sécurité &amp; centre de conformité, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).
  

  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Éléments indexés partiellement inclus dans les résultats de recherche
<a name="unindexeditemsresults"> </a>

Votre organisation peut être requise pour identifier et effectuer des analyses supplémentaires sur des éléments indexés partiellement pour déterminer ce qu’ils sont, ce qu’ils contiennent et qu’ils soient pertinents pour une enquête spécifique. Comme expliqué précédemment, les éléments indexés partiellement dans les emplacements de contenu sont recherchés sont inclus automatiquement dans les résultats de recherche estimés. Vous avez la possibilité d’inclure ces éléments indexés partiellement lorsque vous exportez les résultats de recherche ou préparez les résultats de recherche avancée eDiscovery. Pour inclure les éléments indexés partiellement lorsque vous préparation pour la découverte avancée ou exportation des résultats de la recherche, sélectionnez une des options pour inclure des éléments qui ont un format non reconnu, qui sont chiffrées ou n’ont pas été indexés pour d’autres raisons.
  
Gardez les points suivants à l’esprit les éléments indexés partiellement :
  
- Lorsque vous exécutez une recherche de contenu, le nombre et la taille des éléments indexés partiellement (renvoyées par la requête de recherche) sont affichés dans les statistiques de recherche dans le volet détails, comme indiqué en tant que « éléments non indexés ».
    
- Lorsque vous exportez les résultats de la recherche et incluez les éléments indexés partiellement, des éléments Exchange partiellement indexés sont exportés vers un fichier PST distinct pour chaque boîte aux lettres dans laquelle ils se trouvent, ou en tant que messages individuels si vous sélectionnez l’option pour télécharger les éléments Exchange en tant que messages. les éléments SharePoint partiellement indexés sont exportés vers un dossier nommé **Uncrawlable**.
    
- Si vous exportez des résultats de la recherche a été une recherche dans les emplacements de contenu spécifiques ou tous les emplacements de contenu dans votre organisation, uniquement les éléments non indexées à partir d’emplacements de contenu qui contiennent des éléments qui correspondent aux critères de recherche doit être exportées. En d’autres termes, si aucun résultat de recherche n’est détectée dans une boîte aux lettres ou d’un site, tous les éléments non indexés dans cette boîte aux lettres ou d’un site ne sont pas exportées. La raison en est que l’exportation d’éléments indexés partiellement à partir de nombreux emplacements dans l’organisation peut augmenter la probabilité d’erreurs d’exportation et augmenter le temps que nécessaire pour exporter et télécharger les résultats de recherche.
    
    Pour exporter les éléments partiellement indexées à partir de tous les emplacements de contenu pour une recherche, configurer la recherche pour retourner tous les éléments (en supprimant des mots clés à partir de la requête de recherche) puis exporter que partiellement indexé éléments lorsque vous exportez les résultats de recherche (en cliquant sur **uniquement éléments qui ont un format non reconnu, sont chiffrées ou n’ont pas été indexés pour d’autres raisons** sous **options de sortie**).
    
- Si vous choisissez d’inclure tous les éléments de boîte aux lettres dans les résultats de recherche, ou si une requête de recherche ne spécifie pas les mots clés ou uniquement spécifie une plage de dates, éléments indexés partiellement ne peuvent pas être copiés dans le fichier PST contenant les éléments indexés partiellement. Il s’agit, car tous les éléments, y compris tous les éléments indexés partiellement, seront automatiquement inclus dans les résultats de recherche standard.
    
- Éléments indexés partiellement ne sont pas disponibles pour être affichés. Vous devez exporter les résultats de recherche pour afficher les éléments indexés partiellement renvoyés par la recherche.

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Éléments indexés partiellement exclus des résultats de recherche

Si un élément est partiellement indexé, mais il ne répond pas aux critères de la requête de recherche, il ne sera inclus comme un élément partiellement indexé dans les résultats de recherche. En d’autres termes, l’élément est exclu de résultats de la recherche. Par exemple, supposons que vous n’incluez pas les mots clés ou les propriétés parce que vous souhaitez inclure tous les contenus et exécutez une recherche. Mais vous incluez une condition de plage de dates pour la requête. Si un élément indexé partiellement se situe en dehors de cette plage de dates, il ne sera inclus comme un élément partiellement indexé. Plages de dates sont un moyen efficace pour exclure les éléments indexés partiellement vos résultats de recherche.
  
De même, si vous choisissez d’inclure les éléments indexés partiellement lorsque vous exportez les résultats d’une recherche, des éléments indexés partiellement qui ont été exclus des résultats de la recherche ne sont pas exportées.
  
Une exception à cette règle est lorsque vous créez un blocage de requête qui est associée à une affaire eDiscovery. Si vous créez une suspension basée sur une requête, tous les éléments indexés partiellement sont mis en attente. Cela inclut les éléments partiellement indexés qui ne correspondent pas aux critères de la requête de recherche et des éléments indexés partiellement qui peuvent être inclus en dehors d’une condition de plage de date. Pour plus d’informations sur la création de requête-based blocages, voir l’étape 4 en [cas de découverte de la sécurité pour Microsoft Office 365 et le centre de conformité](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>L’indexation des limites pour les messages de la recherche de contenu

Le tableau suivant décrit les limites d’indexation pouvant entraîner un message électronique renvoyé sous la forme d’un élément partiellement indexé dans une recherche de contenu dans Office 365.
  
Pour obtenir la liste de l’indexation des limites pour les documents SharePoint, voir [limites de recherche pour SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Limite d’indexation**|**Commentaires**|**Description**|
|:-----|:-----|:-----|
|Taille maximale des pièces jointes (à l’exclusion de fichiers Excel)  <br/> |150 Mo  <br/> |La taille maximale d’une pièce jointe qui analysera pour l’indexation. Toutes les pièces jointes sont supérieure à cette limite ne sont pas être analysée pour l’indexation et le message avec la pièce jointe est marqué comme partiellement indexé.<br/><br/> **Remarque :** L’analyse est le processus où le service d’indexation extrait le texte de la pièce jointe, supprime les caractères tels que des signes de ponctuation et les espaces inutiles et divise le texte en mots (dans un processus appelé création de jetons), qui sont stockés dans l’index.           |
|Taille maximale des fichiers Excel  <br/> |4 MO  <br/> |La taille maximale d’un fichier Excel située sur un site ou attaché à un message électronique qui sera analysé pour l’indexation. N’importe quel fichier Excel supérieur à cette limite ne sont pas être analysée, et le fichier ou le courrier électronique le message avec la pièce jointe est marqué comme non indexés.  <br/> |
|Nombre maximal de pièces jointes  <br/> |250  <br/> |Le nombre maximal de fichiers joints à un message électronique qui sera analysé pour l’indexation. Si un message contient plus de 250 pièces jointes, les pièces 250 premiers jointes sont analysés et indexés, et le message est marqué comme partiellement indexé parce qu’il avait des pièces jointes supplémentaires qui n’ont pas été analysés.  <br/> |
|Profondeur maximale des pièces jointes  <br/> |30  <br/> |Le nombre maximal de pièces jointes imbriquées qui sont analysés. Par exemple, si un message électronique est un autre message attaché et le message joint est un document Word joint, le document Word et le message joint seront indexés. Ce comportement continuera de pièces jointes imbriquées jusqu'à 30.  <br/> |
|Nombre maximal d’images attachés  <br/> |0  <br/> |Une image qui est attachée à un message électronique est ignorée par l’analyseur et n’est pas indexée.  <br/> |
|Durée maximale passé à l’analyse d’un élément  <br/> |30 secondes  <br/> |Un maximum de 30 secondes est passé à l’analyse d’un élément pour l’indexation. Si la durée d’analyse dépasse 30 secondes, l’élément est marqué comme étant partiellement indexé.  <br/> |
|Sortie de l’analyseur maximale  <br/> |2 millions de caractères  <br/> |La quantité maximale de sortie de texte de l’analyseur qui est indexée. Par exemple, si l’analyseur extrait 8 millions de caractères à partir d’un document, uniquement les premiers 2 millions de caractères sont indexées.  <br/> |
|Jetons d’annotation maximale  <br/> |2 millions  <br/> |Lorsqu’un message électronique est indexé, chaque mot est annoté avec des instructions de traitement qui spécifient comment que word doit être indexée. Chaque jeu d’instructions de traitement est appelé un jeton d’annotation. Pour maintenir la qualité de service dans Office 365, il existe une limite de jetons d’annotation 2 millions d’un message électronique.  <br/> |
|Taille maximale du corps de l’index  <br/> |67 millions de caractères  <br/> |Nombre total de caractères dans le corps d’un message électronique et ses pièces jointes. Lorsqu’un message électronique est indexé, tout le texte dans le corps du message et dans toutes les pièces jointes est concaténé dans une chaîne unique. La taille maximale de cette chaîne qui est indexée est 67 millions de caractères.  <br/> |
|Jetons uniques maximales dans le corps  <br/> |1 million  <br/> |Expliqué précédemment, les jetons sont le résultat de l’extraction du contenu de texte, la suppression des signes de ponctuation et les espaces et divisant en mots (appelées jetons) qui sont stockés dans l’index. Par exemple, l’expression `"cat, mouse, bird, dog, dog"` contient des 5 jetons. Mais uniquement 4 de ces jetons uniques. Il existe une limite de 1 million de jetons unique par message électronique, ce qui permet d’empêcher l’index devient trop importante avec des jetons aléatoires.<br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Plus d’informations sur les éléments indexés partiellement
<a name="moreinfo"> </a>

- Comme indiqué précédemment, étant donné que les propriétés de message et des documents et leurs métadonnées sont indexées, une recherche par mot-clé peut retourner des résultats si ce mot clé s’affiche dans les métadonnées indexées. Toutefois, ce même recherche de mot clé ne renvoie pas l’élément même si le mot clé n’apparaît dans le contenu d’un élément avec un type de fichier non pris en charge. Dans ce cas, l’élément est retourné en tant qu’un élément partiellement indexé.
    
- Si un élément partiellement indexé est inclus dans les résultats de recherche, car elle répondait aux critères de requête de recherche (et n’a pas été exclu) il ne sera inclus comme un élément partiellement indexé dans les statistiques de la recherche estimés. En outre, il ne sera inclus dans les éléments indexés partiellement lorsque vous exportez des résultats de la recherche.
    
- Bien qu’un type de fichier est pris en charge pour l’indexation et est indexé, il peut être l’indexation ou la recherche des erreurs susceptibles de provoquer un fichier à renvoyer comme un élément partiellement indexé. Par exemple, recherche dans un fichier Excel de très grande taille peut être partiellement (car la première 4 Mo sont indexés), mais échoue car la limite de taille de fichier est dépassée. Dans ce cas, il est possible que le même fichier est renvoyé avec les résultats de recherche, comme un élément partiellement indexé.
    
- Fichiers joints chiffrés avec des technologies Microsoft sont indexés et peuvent être recherchés. Fichiers chiffrés avec des technologies non Microsoft sont partiellement indexés.
    
- Les messages électroniques chiffrés avec S/MIME sont partiellement indexés. Cela inclut les messages chiffrés avec ou sans pièces jointes.
    
- Les messages protégés par la Gestion des droits relatifs à l’information (IRM) sont indexés et seront inclus dans les résultats de la recherche s’ils correspondent à la requête de recherche.

## <a name="see-also"></a>Voir aussi

[Examen d’éléments partiellement indexés dans eDiscovery Office 365](investigating-partially-indexed-items-in-ediscovery.md)

