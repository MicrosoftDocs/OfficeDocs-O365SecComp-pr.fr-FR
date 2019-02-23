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
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'Découvrez les éléments non indexés dans Exchange et SharePoint que vous pouvez inclure dans une recherche de contenu exécutée via le centre &amp; de sécurité conformité Office 365. '
ms.openlocfilehash: 028a0468e352121c64e12fbec209658dc32f9bbe
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219494"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Éléments partiellement indexés dans la recherche de contenu dans Office 365

Une recherche de contenu exécutée à partir du centre de &amp; sécurité conformité Office 365 inclut automatiquement les éléments partiellement indexés dans les résultats de recherche estimés lorsque vous exécutez une recherche. Les éléments partiellement indexés sont des éléments de boîte aux lettres Exchange et des documents sur SharePoint et des sites OneDrive entreprise qui n'ont pas été complètement indexés pour la recherche. Dans Exchange, un élément partiellement indexé contient généralement un fichier, d'un type de fichier qui ne peut pas être indexé, attaché à un message électronique. Voici quelques autres raisons pour lesquelles les éléments ne peuvent pas être indexés pour la recherche et sont renvoyés en tant qu'éléments partiellement indexés lors de l'exécution d'une recherche: 
  
- Le type de fichier n'est pas reconnu ou n'est pas pris en charge pour l'indexation.
    
-  Les messages contiennent un fichier joint sans gestionnaire valide, tel que des fichiers image; Il s'agit de la cause la plus fréquente d'éléments de courrier électronique partiellement indexés. 
    
- Le type de fichier est pris en charge pour l’indexation, mais une erreur d’indexation s’est produite pour un fichier spécifique.
    
- Le nombre de fichiers joints à un message électronique est trop important.
    
- Un fichier joint à un message électronique est trop volumineux.
    
- Un fichier est chiffré avec des technologies autres que Microsoft.
    
- Un fichier est protégé par mot de passe.
    
> [!NOTE]
> La plupart des organisations Office 365 disposent de moins de 1% de contenu par volume et de moins de 12% en taille partiellement indexée. La raison de la différence entre volume et taille est que les fichiers plus volumineux ont une probabilité plus élevée de contenir du contenu qui ne peut pas être complètement indexé. 
  
Pour les enquêtes légales, votre organisation peut être amenée à passer en revue les éléments partiellement indexés. Vous pouvez également spécifier s'il faut inclure des éléments partiellement indexés lorsque vous exportez des résultats de recherche vers un ordinateur local ou lorsque vous préparez les résultats pour l'analyse avec Office 365 Advanced eDiscovery. Pour plus d'informations, reportez-vous à la rubrique recherche [d'éléments partiellement indexés dans Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Types de fichier non indexés pour la recherche

Certains types de fichiers, tels que les fichiers bitmap ou MP3, ne contiennent pas de contenu pouvant être indexé. Par conséquent, les serveurs d'indexation de recherche dans Exchange et SharePoint ne procèdent pas à l'indexation de texte intégral sur ces types de fichiers. Ces types de fichiers sont considérés comme des types de fichiers non pris en charge. Il existe également des types de fichiers pour lesquels l'indexation de texte intégral a été désactivée, par défaut ou par un administrateur. Les types de fichiers non pris en charge et désactivés sont étiquetés comme éléments non indexés dans les recherches de contenu. Comme indiqué précédemment, les éléments partiellement indexés peuvent être inclus dans le jeu de résultats de recherche lorsque vous exécutez une recherche, exportez les résultats de la recherche vers un ordinateur local ou préparez les résultats de recherche pour Advanced eDiscovery. 
  
Pour obtenir une liste de formats de fichier pris en charge et désactivés, consultez les rubriques suivantes :
  
- **** - [Formats de fichiers Exchange indexés par la recherche Exchange](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **Exchange** - [Get-searchdocumentformat permet](https://go.microsoft.com/fwlink/p/?LinkID=724037)
    
- **** Extensions de[nom de fichier analysées et types de fichiers analysés par défaut dans SharePoint](https://go.microsoft.com/fwlink/p/?LinkID=404033)  - 
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Les messages et les documents contenant des types de fichiers partiellement indexés peuvent être renvoyés dans les résultats de la recherche.

Tous les messages électroniques comportant une pièce jointe partiellement indexée ou tous les documents SharePoint partiellement indexés ne sont pas renvoyés automatiquement en tant qu'éléments partiellement indexés. Cela est dû au fait que d'autres propriétés de message ou de document, telles que la propriété **Subject** dans les messages électroniques et les propriétés **title** ou **Author** des documents, sont indexées et disponibles pour être recherchées. Par exemple, une recherche par mot clé pour «Financial» renverra des éléments avec une pièce jointe partiellement indexée si ce mot clé apparaît dans l'objet d'un message électronique ou dans le nom de fichier ou le titre d'un document. Toutefois, si le mot clé apparaît uniquement dans le corps du fichier, le message ou le document est renvoyé sous la forme d'un élément partiellement indexé. 
  
De même, les messages avec des pièces jointes et des documents dont le type de fichier est partiellement indexé sont inclus dans les résultats de la recherche lorsque d'autres propriétés de message ou de document, indexées et utilisables, répondent aux critères de recherche. Les propriétés de message qui sont indexées pour la recherche incluent les dates d'envoi et de réception, l'expéditeur et le destinataire, le nom de fichier d'une pièce jointe et le texte dans le corps du message. Les propriétés de document indexées pour la recherche incluent les dates de création et de modification. Par conséquent, même si une pièce jointe de message peut être un élément partiellement indexé, le message sera inclus dans les résultats de la recherche normale si la valeur d'autres propriétés de message ou de document correspond aux critères de recherche.
  
Pour obtenir la liste des propriétés de messagerie et de document que vous pouvez rechercher à l'aide de la fonctionnalité &amp; de recherche du centre de sécurité conformité, consultez la rubrique [requêtes par Mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  

  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Éléments partiellement indexés inclus dans les résultats de la recherche
<a name="unindexeditemsresults"> </a>

Votre organisation peut être amenée à identifier et à effectuer des analyses supplémentaires sur des éléments partiellement indexés afin de déterminer ce qu'ils sont, ce qu'ils contiennent et s'ils sont pertinents pour une enquête spécifique. Comme expliqué précédemment, les éléments partiellement indexés des emplacements de contenu à rechercher sont automatiquement inclus dans les résultats de recherche estimés. Vous avez la possibilité d'inclure ces éléments partiellement indexés lorsque vous exportez des résultats de recherche ou préparez les résultats de recherche pour Advanced eDiscovery. Pour inclure des éléments partiellement indexés lorsque vous exportez des résultats de recherche ou que vous les préparez pour Advanced eDiscovery, sélectionnez l'une des options pour inclure les éléments dont le format n'est pas reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons.
  
Gardez les points suivants à l'esprit concernant les éléments partiellement indexés:
  
- Lorsque vous exécutez une recherche de contenu, le nombre total et la taille des éléments partiellement indexés (renvoyés par la requête de recherche) sont affichés dans les statistiques de recherche dans le volet d'informations, comme étiqueté «éléments non indexés».
    
- Lorsque vous exportez des résultats de recherche et incluez des éléments partiellement indexés, les éléments Exchange partiellement indexés sont exportés dans un fichier PST distinct pour chaque boîte aux lettres dans laquelle ils se trouvent, ou sous forme de messages individuels si vous sélectionnez l'option de téléchargement des éléments Exchange en tant que messages. les éléments SharePoint partiellement indexés sont exportés dans **** un dossier nommé non analysable.
    
- Si la recherche à partir de laquelle vous exportez les résultats est une recherche d'emplacements de contenu spécifiques ou de tous les emplacements de contenu de votre organisation, seuls les éléments non indexés des emplacements de contenu contenant des éléments correspondant aux critères de recherche seront exportés. En d'autres termes, si aucun résultat de recherche n'est trouvé dans une boîte aux lettres ou un site, tous les éléments non indexés de cette boîte aux lettres ou de ce site ne seront pas exportés. Cela est dû au fait que l'exportation d'éléments partiellement indexés à partir de nombreux emplacements de l'organisation peut augmenter la probabilité d'erreurs d'exportation et augmenter le temps nécessaire pour exporter et télécharger les résultats de la recherche.
    
    Pour exporter des éléments partiellement indexés de tous les emplacements de contenu pour une recherche, configurez la recherche de sorte qu'elle renvoie tous les éléments (en supprimant les mots clés de la requête de recherche), puis exportez uniquement les éléments partiellement indexés lorsque vous exportez les résultats de la recherche (en cliquant **uniquement sur les éléments dont le format n'est pas reconnu sont chiffrés ou n'ont pas été indexés pour d'autres raisons sous les options de** **sortie**.
    
- Si vous choisissez d'inclure tous les éléments de boîte aux lettres dans les résultats de la recherche ou si une requête de recherche ne spécifie pas de mots clés ou uniquement une plage de dates, les éléments partiellement indexés ne peuvent pas être copiés dans le fichier PST qui contient les éléments partiellement indexés. Cela est dû au fait que tous les éléments, y compris les éléments partiellement indexés, sont automatiquement inclus dans les résultats de la recherche standard.
    
- Les éléments partiellement indexés ne peuvent pas être prévisualisés. Vous devez exporter les résultats de la recherche pour afficher les éléments partiellement indexés renvoyés par la recherche.

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Éléments partiellement indexés exclus des résultats de la recherche

Si un élément est partiellement indexé mais qu'il ne répond pas aux critères de requête de recherche, il ne sera pas inclus en tant qu'élément partiellement indexé dans les résultats de la recherche. En d'autres termes, l'élément est exclu des résultats de la recherche. Par exemple, imaginons que vous exécutiez une recherche et que vous n'incluez pas de mots clés ou de propriétés, car vous souhaitez inclure tout le contenu. Mais vous incluez une condition de plage de dates pour la requête. Si un élément partiellement indexé se trouve en dehors de cette plage de dates, il ne sera pas inclus en tant qu'élément partiellement indexé. Les plages de dates sont un moyen efficace d'exclure des éléments partiellement indexés de vos résultats de recherche.
  
De même, si vous choisissez d'inclure les éléments partiellement indexés lorsque vous exportez les résultats d'une recherche, les éléments partiellement indexés exclus des résultats de la recherche ne seront pas exportés.
  
Une exception à cette règle est lorsque vous créez un blocage basé sur une requête qui est associé à un cas de découverte électronique. Si vous créez une conservation basée sur une requête, tous les éléments partiellement indexés sont placés en conservation. Cela inclut les éléments partiellement indexés qui ne correspondent pas aux critères de requête de recherche et aux éléments partiellement indexés qui peuvent se trouver en dehors d'une condition de plage de dates. Pour plus d'informations sur la création de conservations basées sur une requête, voir l'étape 4 dans [les cas de découverte électronique dans le centre de sécurité Office 365 Security &](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>Limites d'indexation pour les messages dans la recherche de contenu

Le tableau suivant décrit les limites d'indexation susceptibles d'entraîner le renvoi d'un message électronique sous la forme d'un élément partiellement indexé dans une recherche de contenu dans Office 365.
  
Pour obtenir la liste des limites d'indexation pour les documents SharePoint, consultez la rubrique [limites de recherche pour SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Limite d'indexation**|**Commentaires**|**Description**|
|:-----|:-----|:-----|
|Taille maximale des pièces jointes (à l'exception des fichiers Excel)  <br/> |150 Mo  <br/> |Taille maximale d'une pièce jointe de courrier électronique qui analysera l'indexation. Toute pièce jointe dont la taille est supérieure à cette limite n'est pas analysée pour l'indexation et le message avec la pièce jointe est marqué comme partiellement indexé.<br/><br/> **Remarque:** L'analyse est le processus dans lequel le service d'indexation extrait le texte de la pièce jointe, supprime les caractères superflus, tels que la ponctuation et les espaces, puis divise le texte en mots (dans un processus appelé «tokening»), qui sont ensuite stockés dans l'index.           |
|Taille maximale des fichiers Excel  <br/> |4 MO  <br/> |Taille maximale d'un fichier Excel situé sur un site ou jointe à un message électronique qui sera analysé pour l'indexation. Tout fichier Excel dont la taille est supérieure à cette limite n'est pas analysé, et le fichier ou le message électronique avec le fichier joint est marqué comme non indexée.  <br/> |
|Nombre maximal de pièces jointes  <br/> |250  <br/> |Nombre maximal de fichiers joints à un message électronique qui seront analysés pour l'indexation. Si un message contient plus de 250 pièces jointes, les 250 premières pièces jointes sont analysées et indexées, et le message est marqué comme partiellement indexé car il contient des pièces jointes supplémentaires qui n'ont pas été analysées.  <br/> |
|Profondeur maximale des pièces jointes  <br/> |0,30  <br/> |Nombre maximal de pièces jointes imbriquées qui sont analysées. Par exemple, si un message électronique est associé à un autre message et que le message joint contient un document Word joint, le document Word et le message joint sont indexés. Ce comportement se poursuivra pendant jusqu'à 30 pièces jointes imbriquées.  <br/> |
|Nombre maximal d'images attachées  <br/> |0  <br/> |Une image jointe à un message électronique est ignorée par l'analyseur et n'est pas indexée.  <br/> |
|Temps maximal passé à analyser un élément  <br/> |30 secondes  <br/> |Un maximum de 30 secondes est passé à analyser un élément pour l'indexation. Si la durée d'analyse est supérieure à 30 secondes, l'élément est marqué comme partiellement indexé.  <br/> |
|Sortie maximale de l'analyseur  <br/> |2 millions de caractères  <br/> |Quantité maximale de sortie de texte de l'analyseur qui est indexée. Par exemple, si l'analyseur a extrait 8 millions caractères d'un document, seuls les 2 premiers caractères sont indexés.  <br/> |
|Nombre maximal de jetons d'annotation  <br/> |2 millions  <br/> |Lorsqu'un message électronique est indexé, chaque mot est annoté avec des instructions de traitement différentes qui définissent le mode d'indexation de Word. Chaque ensemble d'instructions de traitement est appelé un jeton d'annotation. Pour maintenir la qualité de service dans Office 365, il existe une limite de 2 millions jetons d'annotation pour un message électronique.  <br/> |
|Taille maximale du corps dans l'index  <br/> |67 millions caractères  <br/> |Nombre total de caractères dans le corps d'un message électronique et toutes ses pièces jointes. Lorsqu'un message électronique est indexé, tout le texte dans le corps du message et dans toutes les pièces jointes est concaténé dans une chaîne unique. La taille maximale de cette chaîne indexée est de 67 millions caractères.  <br/> |
|Nombre maximal de jetons uniques dans le corps  <br/> |1 million  <br/> |Comme expliqué précédemment, les jetons sont le résultat de l'extraction de texte du contenu, la suppression de la ponctuation et des espaces, puis sa division en mots (appelés jetons) stockés dans l'index. Par exemple, l'expression `"cat, mouse, bird, dog, dog"` contient 5 jetons. Mais seulement 4 sont des jetons uniques. Il existe une limite de 1 million jetons uniques par message électronique, ce qui permet d'éviter que l'index soit trop volumineux avec des jetons aléatoires.<br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Plus d'informations sur les éléments partiellement indexés
<a name="moreinfo"> </a>

- Comme indiqué précédemment, étant donné que les propriétés de message et de document et leurs métadonnées sont indexées, une recherche par mot clé peut renvoyer des résultats si ce mot clé apparaît dans les métadonnées indexées. Toutefois, cette même recherche par mot clé peut ne pas renvoyer le même élément si le mot clé ne s'affiche que dans le contenu d'un élément dont le type de fichier n'est pas pris en charge. Dans ce cas, l'élément est renvoyé sous la forme d'un élément partiellement indexé.
    
- Si un élément partiellement indexé est inclus dans les résultats de la recherche, car il répond aux critères de requête de recherche (et n'a pas été exclu), il ne sera pas inclus en tant qu'élément partiellement indexé dans les statistiques de recherche estimées. En outre, elle ne sera pas incluse avec des éléments partiellement indexés lorsque vous exportez les résultats de la recherche.
    
- Bien qu'un type de fichier soit pris en charge pour l'indexation et indexé, il peut y avoir des erreurs d'indexation ou de recherche qui entraînent le renvoi d'un fichier sous la forme d'un élément partiellement indexé. Par exemple, la recherche d'un fichier Excel très volumineux peut avoir partiellement réussi (car les 4 premiers Mo sont indexés), mais échoue, car la limite de taille de fichier est dépassée. Dans ce cas, il est possible que le même fichier soit renvoyé avec les résultats de la recherche et comme un élément partiellement indexé.
    
- Les fichiers joints chiffrés avec les technologies Microsoft sont indexés et peuvent faire l'objet d'une recherche. Les fichiers chiffrés avec les technologies non-Microsoft sont partiellement indexés.
    
- Les messages électroniques chiffrés avec S/MIME sont partiellement indexés. Cela inclut les messages chiffrés avec ou sans pièces jointes.
    
- Les messages protégés par la Gestion des droits relatifs à l’information (IRM) sont indexés et seront inclus dans les résultats de la recherche s’ils correspondent à la requête de recherche.

## <a name="see-also"></a>Voir aussi

[Examen d’éléments partiellement indexés dans eDiscovery Office 365](investigating-partially-indexed-items-in-ediscovery.md)

