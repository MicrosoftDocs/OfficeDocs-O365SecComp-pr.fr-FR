---
title: Recherche et balisage
ms.author: chrfox
author: chrfox
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans Advanced eDiscovery, le module de recherche et de marquage vous permet de rechercher, de prévisualiser et d’organiser les documents dans votre cas. Actuellement, ce module est en version bêta.
ms.openlocfilehash: b3e660e6dca014323cfd06f10c14747751aeb386
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158536"
---
# <a name="search-and-tagging"></a>Recherche et balisage

Dans Advanced eDiscovery, le module de recherche et de marquage vous permet de rechercher, de prévisualiser et d’organiser les documents dans votre cas. Actuellement, ce module est en version bêta. Pour une brève démonstration de la recherche et du balisage, voir la vidéo [gérer vos données à l’aide de la vidéo Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) .

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Rechercher les documents dans votre cas

Une fois que vous avez traité des documents dans un cas avancé eDiscovery (et si vous le souhaitez), vous pouvez utiliser la recherche et le balisage pour rechercher des documents, puis les organiser en appliquant des balises propres à la casse (également appelées étiquettes). Vous pouvez définir une requête de recherche à l’aide des cartes de condition fournies ou à l’aide d’un langage de requête KQL dans la carte de condition de mots-clés. La syntaxe KQL commune, telle que AND, OR, NOT et NEAR (n) sont prises en charge, ainsi que les caractères génériques à caractères multiples (*). 

Le tableau suivant répertorie les propriétés que vous pouvez rechercher à l’aide d’une requête de mot clé KQL. Vous pouvez également utiliser une carte de condition dans l’outil de recherche avancée eDiscovery pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche.

|**Propriété**|**Description**|
|:-----|:-----|
|**caselabel** <br/> | Nom de la balise créée/appliquée lorsqu’un document est balisé. <br/> |
|**gardien** <br/> | Dépositaire associé à un document; soumis à des limitations. <br/> |
|**date** <br/> | Date d’envoi du courrier électronique; Date de modification des documents de site. <br/> |
|**combinaison** <br/> | ID de fichier dans le cas. <br/> |
|**filetype** <br/> | Extension de fichier native. <br/> |
|**fileclass** <br/> | Courrier électronique, document ou pièce jointe. <br/> |
|**senderauthor** <br/> | Expéditeur du courrier électronique; auteur des documents de site. <br/> |
|**size** <br/> | Taille du fichier en Ko. <br/> |
|**subjecttitle** <br/> | L’objet de la messagerie; titre des documents de site. <br/> |
|**bbc** <br/> | Champ CCI d’un message électronique. <br/> |
|**cc** <br/> | Champ CC d’un message électronique. <br/> |
|**participants** <br/> | Adresse de messagerie de tous les participants d’un thread de messagerie, y compris pour les liens manquants. <br/> |
|**received** <br/> | Date à laquelle un message électronique a été reçu. <br/> |
|**recipients** <br/> | Destinataires d’un e-mail, inclus dans les champs à, CC ou CCI. <br/> |
|**sender** <br/> | Expéditeur d’un message électronique. <br/> |
|**LastModifiedDate** <br/> | Date de la dernière modification d’un document de site. <br/> |
|**sent** <br/> | Date d’envoi d’un message électronique. <br/> |
|**to** <br/> | Destinataire figurant dans le champ à d’un message électronique. <br/> |
|**créés** <br/> | Auteur d’un document de site. <br/> |
|**title** <br/> | Titre d’un document de site. <br/> |
|**dominanttheme**\* <br/> | Thème dominant d’un élément. <br/> |
|**themeslist**\* <br/> | Thèmes associés à un élément. <br/> |
|**readpercentile_[issuenum]**\*\* <br/> | Centile de lecture d’un élément pour le problème défini par [issuenum]. <br/> |
|**relevancescore_[issuenum]**\*\* <br/> | Score de pertinence d’un élément pour le problème défini par [issuenum]. <br/> |
|**relevancetag_ [TagName]**\*\* <br/> | Si un élément a été marqué manuellement pour des éléments de pertinence, la balise définie par [TagName]. <br/> |
|||

\*Disponible uniquement si le module thèmes a été exécuté.

\*\*Disponible uniquement si le module de pertinence a été exécuté.

Vous pouvez également utiliser une carte de condition dans l’outil de recherche avancée eDiscovery pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche. La capture d’écran suivante montre les conditions qui peuvent être ajoutées à une requête. La colonne **Group** indique si la propriété s’applique aux messages électroniques, aux documents de site ou aux deux (indiqué par la valeur *Common*). Cette colonne identifie également les propriétés pouvant faire l’objet d’une recherche après l’exécution du module de pertinence.

![Conditions de recherche dans l’outil de recherche avancée eDiscovery](media/AeDSearchConditions.png)

Pour plus d’informations sur les propriétés pouvant faire l’objet d’une recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche](keyword-queries-and-search-conditions.md).
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de l’évaluation en matière de pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Balisage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Étiquetage et formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l’analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

