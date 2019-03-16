---
title: Interroger les données d’un ensemble de travail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3000a066bf69f71327801035e7c270cc602565ac
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30639011"
---
# <a name="query-the-data-in-a-working-set"></a>Interroger les données d’un ensemble de travail

Dans la plupart des cas, il est utile de pouvoir approfondir ce qui se trouve dans un jeu de travail et de les organiser de manière plus efficace. Les requêtes dans un jeu de travail vous permettent de le faire en vous permettant de vous concentrer sur un sous-ensemble de documents qui répondent aux critères définis par vous à la fois.

## <a name="creating-and-running-a-query-within-a-working-set"></a>Création et exécution d'une requête dans une plage de travail

Pour créer et exécuter une requête dans votre plage de travail, cliquez sur «nouvelle requête» dans votre jeu de travail. Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur «Enregistrer» pour exécuter la requête. Pour exécuter une requête qui a été précédemment enregistrée, il suffit de cliquer sur la requête enregistrée. RePortez-vous à champs de métadonnées de [document](document-metadata-fields.md) pour obtenir la liste des métadonnées que vous pouvez rechercher.

## <a name="building-your-query"></a>Création de votre requête

Vous pouvez créer votre requête à l'aide d'une combinaison de cartes de conditions et de langage de requête dans la carte de condition de mots-clés. Vous pouvez regrouper les cartes de condition ensemble comme un bloc pour concevoir une requête plus complexe.

### <a name="condition-card"></a>Carte de condition

Chaque champ pouvant faire l'objet d'une recherche dans un jeu de travail est doté d'une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.

Il existe plusieurs types de cartes de condition:
- FREETEXT: la carte de condition FREETEXT est utilisée pour les champs de texte tels que subject. Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.
- Date: la carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.
- Options de recherche: la carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre plage de travail. Cette valeur est utilisée pour les champs, tels que sender, où il existe un nombre fini de valeurs possibles dans votre plage de travail.
- Mot-clé: la carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans. Voir ci-dessous pour plus de détails.

### <a name="query-language"></a>Langage de requête

Outre les cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête. Le langage de requête prend en charge la syntaxe KQL standard comme AND, OR, NOT et NEAR (n). Le caractère générique (?) et caractère générique (*) est également pris en charge.

## <a name="filter"></a>Filtre

Outre les requêtes que vous pouvez enregistrer, vous pouvez superposer des conditions supplémentaires à la volée à vos résultats de requête à l'aide de filtres. Les filtres diffèrent des requêtes de différentes manières:
- Les filtres sont transitoires (c'est-à-dire qu'ils ne sont pas conservés sur différentes sessions), tandis que les requêtes sont enregistrées dans le jeu de travail.
- Les filtres sont toujours additifs; les filtres s'appliquent au-dessus de la requête que vous avez appliquée pour le moment, tandis que l'application d'une requête remplace la requête en vigueur.