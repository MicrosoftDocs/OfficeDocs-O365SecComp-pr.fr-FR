---
title: Interroger les données d’un jeu à réviser
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 446f3f2588a79cb328476db490f1f555448b5ce7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154006"
---
# <a name="query-the-data-in-a-review-set"></a>Interroger les données d’un jeu à réviser

Dans la plupart des cas, il est utile de pouvoir approfondir ce qui se trouve dans un ensemble de révision et de les organiser de manière plus efficace. Les requêtes au sein d’un ensemble de révision vous permettent de le faire en vous permettant de vous concentrer sur un sous-ensemble de documents qui répondent aux critères définis simultanément.

## <a name="creating-and-running-a-query-within-a-review-set"></a>Création et exécution d’une requête au sein d’un ensemble de révision

Pour créer et exécuter une requête dans votre jeu de révision, cliquez sur «nouvelle requête» dans votre jeu de révision. Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur «Enregistrer» pour exécuter la requête. Pour exécuter une requête qui a été précédemment enregistrée, il suffit de cliquer sur la requête enregistrée. Reportez-vous à champs de métadonnées de [document](document-metadata-fields.md) pour obtenir la liste des métadonnées que vous pouvez rechercher.

## <a name="building-your-query"></a>Création de votre requête

Vous pouvez créer votre requête à l’aide d’une combinaison de cartes de conditions et de langage de requête dans la carte de condition de mots-clés. Vous pouvez regrouper les cartes de condition ensemble comme un bloc pour concevoir une requête plus complexe.

### <a name="condition-card"></a>Carte de condition

Chaque champ pouvant faire l’objet d’une recherche dans un jeu de révision dispose d’une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.

Il existe plusieurs types de cartes de condition:
- FREETEXT: la carte de condition FREETEXT est utilisée pour les champs de texte tels que subject. Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.
- Date: la carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.
- Options de recherche: la carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre jeu de révision. Cette valeur est utilisée pour les champs, tels que sender, où il existe un nombre fini de valeurs possibles dans votre ensemble de révision.
- Mot-clé: la carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans. Voir ci-dessous pour plus de détails.

### <a name="query-language"></a>Langage de requête

Outre les cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête. Le langage de requête prend en charge la syntaxe KQL standard comme AND, OR, NOT et NEAR (n). Le caractère générique (?) et caractère générique (*) est également pris en charge.

## <a name="filter"></a>Filtrer

Outre les requêtes que vous pouvez enregistrer, vous pouvez superposer des conditions supplémentaires à la volée à vos résultats de requête à l’aide de filtres. Les filtres diffèrent des requêtes de différentes manières:
- Les filtres sont transitoires (c’est-à-dire qu’ils ne sont pas conservés sur différentes sessions), tandis que les requêtes sont enregistrées dans l’ensemble de révision.
- Les filtres sont toujours additifs; les filtres s’appliquent au-dessus de la requête que vous avez appliquée pour le moment, tandis que l’application d’une requête remplace la requête en vigueur.