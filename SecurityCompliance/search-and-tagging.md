---
title: Recherche et marquage
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666144"
---
# <a name="search-and-tagging"></a>Recherche et marquage

Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta. Pour une brève démonstration de recherche et de marquage, voir la vidéo de [gérer vos données avec eDiscovery avancée](https://www.youtube.com/watch?v=VaPYL3DHP6I) .

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="search-the-documents-in-your-case"></a>Recherche les documents dans votre cas.

Après avoir traitement des documents dans un cas eDiscovery avancées (et éventuellement exécuter le module d’analyse ou la pertinence), vous pouvez utiliser la recherche et le balisage pour rechercher des documents et de les organiser en appliquant des balises spécifique (également appelées étiquettes). Vous pouvez définir une requête de recherche à l’aide de cartes de la condition fournie ou à l’aide d’un langage de requête KQL comparables dans les mots clés condition carte. La syntaxe de KQL courants, tels que AND, OR, NOT et NEAR(n) sont pris en charge, ainsi que des caractère multiples caractère générique (*). 

Le tableau suivant répertorie les propriétés que vous pouvez rechercher à l’aide d’une requête de mot clé KQL. Vous pouvez également utiliser une carte de condition pour dans l’outil de recherche de découverte électronique avancée pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche.

|**Propriété**|**Description**|
|:-----|:-----|
|**caselabel** <br/> | Nom de la balise créé/appliquée lorsqu’un document est marqué. <br/> |
|**dépositaire** <br/> | Le dépositaire associé à un document ; limitations de l’objet. <br/> |
|**date** <br/> | Envoyé date pour le courrier électronique ; la date de modification de documents du site. <br/> |
|**fileid** <br/> | L’ID du fichier dans le cas. <br/> |
|**FileType** <br/> | L’extension de fichier natif. <br/> |
|**fileclass** <br/> | Courrier électronique, document ou pièce jointe. <br/> |
|**senderauthor** <br/> | L’expéditeur pour le courrier électronique ; l’auteur des documents du site. <br/> |
|**taille** <br/> | La taille du fichier en Ko. <br/> |
|**subjecttitle** <br/> | L’objet du courrier électronique ; titre de documents du site. <br/> |
|**bcc** <br/> | Le champ Cci d’un message électronique. <br/> |
|**cc** <br/> | Le champ Cc d’un message électronique. <br/> |
|**participants** <br/> | L’adresse de messagerie de tous les participants dans un thread de messagerie, y compris les liens manquants. <br/> |
|**reçus** <br/> | La date de que réception un message électronique. <br/> |
|**destinataires** <br/> | Destinataires d’un message électronique, inclus sur l’à, Cc ou Cci champs. <br/> |
|**expéditeur** <br/> | L’expéditeur d’un message électronique. <br/> |
|**LastModifiedDate** <br/> | La dernière date de modification de document d’un site. <br/> |
|**envoyé** <br/> | La date d’envoi d’un message électronique. <br/> |
|**À** <br/> | Le destinataire est répertorié dans le champ d’un message électronique. <br/> |
|**auteur** <br/> | L’auteur d’un document de site. <br/> |
|**title** <br/> | Le titre d’un document de site. <br/> |
|**dominanttheme**\* <br/> | Le thème principal d’un élément. <br/> |
|**themeslist**\* <br/> | Thèmes qui sont associés à un élément. <br/> |
|**readpercentile_ [issuenum]**\*\* <br/> | Le centile de lecture d’un élément, sur le problème défini par [issuenum]. <br/> |
|**relevancescore_ [issuenum]**\*\* <br/> | Le score de pertinence d’un élément, sur le problème défini par [issuenum]. <br/> |
|**relevancetag_ [tagname]**\*\* <br/> | Si un élément a été balisée manuellement pour la pertinence, la balise définie par [tagname]. <br/> |
|||

\*Disponible uniquement si le module de thèmes a été exécuté.

\*\*Disponible uniquement si le module de la pertinence a été exécuté.

Vous pouvez également utiliser une carte de condition dans l’outil de recherche de découverte électronique avancée pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche. La capture d’écran suivante montre les conditions pouvant être ajoutée à une requête. La colonne **groupe** indique si la propriété s’applique à la messagerie, les documents du site ou les deux (indiquée par la valeur *commune*). Cette colonne identifie également les propriétés utilisables dans une requête qui sont disponibles après avoir exécuté le module de la pertinence.

![Conditions de recherche dans l’outil de recherche avancée eDiscovery](media/AeDSearchConditions.png)

Pour plus d’informations sur les propriétés de recherche, voir [requêtes de mot clé et les conditions de recherche](keyword-queries-and-search-conditions.md).
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

