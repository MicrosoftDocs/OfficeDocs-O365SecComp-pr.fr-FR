---
title: Limites avancées eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez les limites en vigueur pour la solution eDiscovery avancée dans Microsoft 365. Cela inclut les limites de cas, les limites d’indexation et les limites de recherche lors de l’utilisation de l’outil de recherche pour collecter les données de cas.
ms.openlocfilehash: 622d2669457a2a1e84909aadae9b653ca37684ce
ms.sourcegitcommit: 803baca9f99a6691fb41a3308e799752e4d8f20c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35222288"
---
# <a name="limits-in-advanced-ediscovery"></a>Limites définies dans Advanced eDiscovery

Cet article décrit les limites de la solution eDiscovery avancée dans Microsoft 365.

## <a name="case-limits"></a>Limites de cas

Le tableau suivant répertorie les limites pour les cas dans Advanced eDiscovery.

|**Description de la limite**|**Limite**|
|:-----|:-----|
|Nombre total de documents pouvant être ajoutés à un cas (pour tous les jeux de révision dans un cas).  <br/> |1 million  <br/> |
|Taille totale des fichiers par jeu de charges.  <br/> |100 Go  <br/> |
|Quantité totale de données chargées dans un cas par jour.<br/> |2 TO <br/> |
|Nombre maximal de charges par cas.  <br/> |0,15 <br/> |
|Nombre maximal de jeux de révision par cas.  <br/> |vingtaine <br/> |
|||

## <a name="indexing-limits"></a>Limites d’indexation

Le tableau suivant répertorie les limites d’indexation dans Advanced eDiscovery.

|**Description de la limite**|**Limite**|
  |:-----|:-----|
  |Nombre maximal de caractères extraits d’un fichier unique.  <br/> |10 millions<sup>1</sup> <br/> |
  |Taille maximale d’un fichier unique.   <br/> |100 Mo<sup></sup> <br/> |
  |Profondeur maximale des éléments incorporés dans un document.  <br/> |25<sup>1</sup> <br/> |
  |Taille maximale des fichiers traités par la reconnaissance optique de caractères (OCR).  <br/> |24 Mo<sup>1</sup> <br/> |  
|||

## <a name="search-limits"></a>Limites de la recherche

Les limites décrites dans cette section concernent l’utilisation de l’outil de recherche de l’onglet **recherches** pour collecter des données pour un cas. Pour plus d’informations, reportez-vous à [la rubrique collecte de données pour un cas dans Advanced eDiscovery](collecting-data-for-ediscovery.md).

|**Description de la limite**|**Limite**|
|:-----|:-----|
|Nombre maximal de boîtes aux lettres ou de sites pouvant faire l’objet d’une recherche dans une seule recherche.  <br/> |Sans limite  <br/> |
|Nombre maximal de recherches pouvant être exécutées en même temps.  <br/> |Sans limite  <br/> | 
|Nombre maximal de recherches qu’un utilisateur peut démarrer en même temps.  <br/> |10   <br/> | 
|Nombre maximal de caractères pour une requête de recherche (y compris les opérateurs et les conditions).  <br/> |**Boîtes aux lettres**: 10 000<br/>**Sites**: 4 000 lors de la recherche sur tous les sites ou 2 000 lors de la recherche sur 20 sites <sup>2</sup> <br/> |
|Nombre minimal de caractères alpha pour les caractères génériques de préfixe; par exemple **,\* un ou un** **défini\***. <br/> |3  <br/> |  
|Nombre maximal de variantes renvoyées lors de l’utilisation d’un caractère générique de préfixe pour rechercher une expression exacte ou avec un caractère générique de préfixe et l’opérateur booléen **near** ou **ONEAR** .  <br/> |10 000 <sup>3</sup> <br/> |
|Nombre maximal d’éléments par boîte aux lettres utilisateur qui s’affichent sur la page d’aperçu pour les recherches. Les éléments les plus récents sont affichés.   <br/> |100  <br/> |
|Nombre maximal d’éléments de toutes les boîtes aux lettres affichés sur la page d’aperçu pour les recherches.  <br/> |1,000  <br/> |
|Nombre maximal de boîtes aux lettres qui peuvent être prévisualisées pour les résultats de la recherche.  S’il y a plus de 1000 boîtes aux lettres contenant des éléments qui correspondent à la requête de recherche, seules les 1 000 premières boîtes aux lettres avec le plus de résultats sont disponibles pour l’aperçu.<br/> |1,000  <br/> |
|Nombre maximal d’éléments provenant de sites SharePoint et OneDrive entreprise affichés sur la page d’aperçu pour les recherches. Les éléments les plus récents sont affichés.  <br/> |200  <br/> |
|Nombre maximal de sites SharePoint et OneDrive entreprise pouvant être prévisualisés pour les résultats de la recherche. S’il y a plus de 200 sites contenant des éléments qui correspondent à la requête de recherche, seuls les premiers sites 200 avec le plus de résultats sont disponibles pour l’aperçu.  <br/> |200  <br/> |
|Nombre maximal d’éléments par boîte aux lettres de dossiers publics affiché sur la page d’aperçu pour les recherches.  <br/> |100  <br/> |
|Nombre maximal d’éléments trouvés dans tous les éléments de boîte aux lettres de dossiers publics affichés sur la page d’aperçu pour les recherches.  <br/> |200  <br/> |
|Nombre maximal de boîtes aux lettres de dossiers publics pouvant être prévisualisées pour les résultats de la recherche. S’il existe plus de 500 boîtes aux lettres de dossiers publics contenant des éléments qui correspondent à la requête de recherche, seules les 500 premières boîtes aux lettres avec le plus de résultats sont disponibles pour l’aperçu.  <br/> |500  <br/> |
|||

## <a name="viewer-limits"></a>Limites de la visionneuse

|**Description de la limite**|**Limite**|
  |:-----|:-----|
  |Taille maximale du fichier Excel pouvant être consulté dans la visionneuse native.  <br/> |4 MO  <br/> |
|||

## <a name="review-set-download-limits"></a>Vérifier les limites de téléchargement des jeux

|**Description de la limite**|**Limite**|
|:-----|:-----|
|Taille totale du fichier ou nombre maximal de documents téléchargés à partir d’un jeu de révision.  <br/> |3 Mo ou 50 documents <sup>4</sup>|
|||

<br/>
<br/>

> [!NOTE]
> <sup>1</sup> tout élément qui dépasse une limite de fichier s’affiche en tant qu’erreur de traitement.<br/>
> <sup>2</sup> lors de la recherche de sites SharePoint et OneDrive entreprise, les caractères des URL des sites recherchés décomptent de cette limite.<br/>
> <sup>3</sup> pour les requêtes sans expression (valeur de mot clé qui n’utilise pas de guillemets doubles), nous utilisons un index de préfixe spécial. Cela indique qu’un mot a lieu dans un document, mais pas à son emplacement dans le document. Pour effectuer une requête d’expression (valeur de mot clé avec des guillemets doubles), nous devons comparer la position dans le document pour les mots de l’expression. Cela signifie que nous ne pouvons pas utiliser l’index de préfixe pour les requêtes d’expression. Dans ce cas, nous développons la requête en interne avec tous les mots que le préfixe développe; par exemple, **l'\* heure** peut se développer sur **«heure, minuteur ou temps, ou Timex ou timeboxed ou...»**. La limite de 10 000 est le nombre maximal de variantes que le mot peut développer, pas le nombre de documents correspondant à la requête. Il n’existe pas de limite supérieure pour les termes autres que les expressions.<br/>
> <sup>4</sup> cette limite s’applique au téléchargement des documents sélectionnés à partir d’un jeu de révision. Elle ne s’applique pas à l’exportation de documents à partir d’un jeu de révision. Pour plus d’informations sur le téléchargement et l’exportation de documents, voir [Export case Data in Advanced eDiscovery](exporting-data-ediscover20.md). <br/>

