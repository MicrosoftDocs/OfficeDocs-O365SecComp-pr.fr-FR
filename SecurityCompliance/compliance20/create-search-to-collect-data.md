---
title: Créer une recherche pour collecter des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 773137cbfc73d449766e04bf7eccc77f8bdd0cca
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706135"
---
# <a name="create-a-search-to-collect-data"></a>Créer une recherche pour collecter des données

Sous l’onglet de **recherche** dans votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **la recherche de nouveau** suivant de l’Assistant.

## <a name="name-your-search-and-give-description"></a>Donnez un nom votre recherche et description

Chaque recherche avec un incident doit avoir un nom unique. Vous pouvez éventuellement fournir une description pour votre recherche. 

## <a name="define-your-conditions"></a>Définir vos conditions de travail

Vous pouvez définir les conditions de recherche à l’aide de cartes condition prédéfinis ou à l’aide du langage de requête de mot clé (KQL). Pour plus d’informations, voir [créer des requêtes de recherche](building-search-queries.md).

## <a name="choose-the-custodians-to-search-from"></a>Choisissez les dépositaires pour la recherche à partir de

Une fois que vous avez défini vos conditions, vous devez choisir les emplacements à rechercher. Une façon de procéder est en spécifiant les dépositaires que vous avez déjà ajouté à la casse que vous souhaitez rechercher. En sélectionnant un dépositaire, vous allez exécuter la recherche par rapport à toutes les sources de données mappées sur le dépositaire. Pour plus d’informations sur l’ajout de dépositaires à votre cas et gérer les sources de données, voir [utiliser les dépositaires](managing-custodians.md) .

## <a name="choose-non-custodial-locations"></a>Choisir des emplacements non garde

Dans certains cas, vous pouvez souhaiter rechercher des sources de données qui ne sont pas mappés à un dépositaire. Dans ce cas, vous pouvez spécifier les emplacements que vous souhaitez rechercher, ou choisissez de rechercher tous les emplacements de contenu d’un service Office 365 (par exemple, la recherche SharePoint et OneDrive de toutes les boîtes aux lettres Exchange ou de tous les sites de commerce).