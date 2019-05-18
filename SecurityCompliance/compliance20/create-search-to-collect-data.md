---
title: Créer une recherche pour collecter des données
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
ms.openlocfilehash: 360ba6a67d43a0b78b1104ae64885697009bb222
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155106"
---
# <a name="create-a-search-to-collect-data"></a>Créer une recherche pour collecter des données

Sous l’onglet **recherches** de votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **nouvelle recherche** et en suivant l’Assistant.

## <a name="name-your-search-and-give-description"></a>Nommer votre recherche et donner une description

Chaque recherche avec un cas doit avoir un nom unique. Vous pouvez éventuellement fournir une description pour votre recherche. 

## <a name="define-your-conditions"></a>Définir vos conditions

Vous pouvez définir les conditions de votre recherche à l’aide des cartes de condition prédéfinies ou du langage KQL (Keyword Query Language). Pour plus d’informations, consultez la rubrique [créer des requêtes de recherche](building-search-queries.md).

## <a name="choose-the-custodians-to-search-from"></a>Choisir les dépositaires à rechercher

Une fois que vous avez défini vos conditions, vous devez choisir les emplacements sur lesquels vous souhaitez effectuer la recherche. Pour ce faire, vous pouvez spécifier les dépositaires que vous avez déjà ajoutés au cas dans lequel vous souhaitez effectuer une recherche. En sélectionnant un dépositaire, vous lancez la recherche par rapport à toutes les sources de données mappées au dépositaire. Pour plus d’informations sur l’ajout de dépositaires à votre cas et sur la gestion de leurs sources de données, voir [utiliser des dépositaires](managing-custodians.md) .

## <a name="choose-non-custodial-locations"></a>Choisir les emplacements non privatives de cœur

Dans certains cas, vous souhaiterez peut-être Rechercher des sources de données qui ne sont pas mappées à un dépositaire. Dans ce cas, vous pouvez spécifier les emplacements de recherche, ou choisir de rechercher tous les emplacements de contenu pour un service Office 365 spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange ou tous les sites SharePoint et OneDrive entreprise).