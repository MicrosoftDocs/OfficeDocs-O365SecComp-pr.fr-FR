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
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="3e261-102">Créer une recherche pour collecter des données</span><span class="sxs-lookup"><span data-stu-id="3e261-102">Create a search to collect data</span></span>

<span data-ttu-id="3e261-103">Sous l’onglet de **recherche** dans votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **la recherche de nouveau** suivant de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="3e261-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="3e261-104">Donnez un nom votre recherche et description</span><span class="sxs-lookup"><span data-stu-id="3e261-104">Name your search and give description</span></span>

<span data-ttu-id="3e261-p101">Chaque recherche avec un incident doit avoir un nom unique. Vous pouvez éventuellement fournir une description pour votre recherche.</span><span class="sxs-lookup"><span data-stu-id="3e261-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="3e261-107">Définir vos conditions de travail</span><span class="sxs-lookup"><span data-stu-id="3e261-107">Define your conditions</span></span>

<span data-ttu-id="3e261-p102">Vous pouvez définir les conditions de recherche à l’aide de cartes condition prédéfinis ou à l’aide du langage de requête de mot clé (KQL). Pour plus d’informations, voir [créer des requêtes de recherche](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="3e261-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="3e261-110">Choisissez les dépositaires pour la recherche à partir de</span><span class="sxs-lookup"><span data-stu-id="3e261-110">Choose the custodians to search from</span></span>

<span data-ttu-id="3e261-p103">Une fois que vous avez défini vos conditions, vous devez choisir les emplacements à rechercher. Une façon de procéder est en spécifiant les dépositaires que vous avez déjà ajouté à la casse que vous souhaitez rechercher. En sélectionnant un dépositaire, vous allez exécuter la recherche par rapport à toutes les sources de données mappées sur le dépositaire. Pour plus d’informations sur l’ajout de dépositaires à votre cas et gérer les sources de données, voir [utiliser les dépositaires](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="3e261-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="3e261-115">Choisir des emplacements non garde</span><span class="sxs-lookup"><span data-stu-id="3e261-115">Choose non-custodial locations</span></span>

<span data-ttu-id="3e261-p104">Dans certains cas, vous pouvez souhaiter rechercher des sources de données qui ne sont pas mappés à un dépositaire. Dans ce cas, vous pouvez spécifier les emplacements que vous souhaitez rechercher, ou choisissez de rechercher tous les emplacements de contenu d’un service Office 365 (par exemple, la recherche SharePoint et OneDrive de toutes les boîtes aux lettres Exchange ou de tous les sites de commerce).</span><span class="sxs-lookup"><span data-stu-id="3e261-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>