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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454986"
---
# <a name="query-the-data-in-a-working-set"></a>Interroger les données d’un ensemble de travail

Dans la plupart des cas, il est utile de pouvoir approfondir ce qui se trouve dans un jeu de travail et de les organiser de manière plus efficace. Les requêtes dans un jeu de travail vous permettent de le faire en vous permettant de vous concentrer sur un sous-ensemble de documents qui répondent aux critères définis par vous à la fois.

## <a name="creating-and-running-a-query-within-a-working-set"></a>Création et exécution d'une requête dans une plage de travail

Pour créer et exécuter une requête dans votre plage de travail, cliquez sur «nouvelle requête» dans votre jeu de travail. Une fois que vous avez nommé votre requête et défini les conditions, cliquez sur «Enregistrer» pour exécuter la requête. Pour exécuter une requête qui a été précédemment enregistrée, il suffit de cliquer sur la requête enregistrée. RePortez-vous à champs de métadonnées de [document](document-metadata-fields.md) pour obtenir la liste des métadonnées que vous pouvez rechercher.

## <a name="building-your-query"></a>Création de votre requête

Vous pouvez créer votre requête à l'aide d'une combinaison de cartes de conditions et de langage de requête dans la carte de condition de mots-clés.

### <a name="condition-card"></a>Carte de condition

Chaque champ pouvant faire l'objet d'une recherche dans un jeu de travail est doté d'une carte de condition correspondante que vous pouvez utiliser pour créer votre requête.

Il existe plusieurs types de cartes de condition:
- FREETEXT: la carte de condition FREETEXT est utilisée pour les champs de texte tels que subject. Vous pouvez répertorier plusieurs termes de recherche en les séparant par une virgule.
- Date: la carte de condition de date est utilisée pour les champs de date tels que date de dernière modification.
- Options de recherche: la carte de condition options de recherche fournit une liste des valeurs possibles pour le champ particulier dans votre plage de travail. Cette valeur est utilisée pour les champs tels que sender, où il existe un nombre fini de valeurs possibles dans votre plage de travail.
- Mot-clé: la carte de condition de mot-clé est une instance spécifique de la carte de condition FREETEXT que vous pouvez utiliser pour rechercher des termes ou utiliser le langage de requête KQL dans. Voir ci-dessous pour plus de détails.

### <a name="query-language"></a>Langage de requête

Outre les cartes de condition, vous pouvez utiliser un langage de requête de type KQL dans la carte de mots-clés pour créer votre requête. Le langage de requête prend en charge la syntaxe KQL standard comme AND, OR, NOT et NEAR (n). Le caractère générique (?) et caractère générique (*) est également pris en charge.