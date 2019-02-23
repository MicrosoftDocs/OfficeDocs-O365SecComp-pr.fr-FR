---
title: Créer une recherche pour collecter des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 09af09c4a538bb43fed5fce044eb1be60c235aaa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212644"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="76c5f-102">Créer une recherche pour collecter des données</span><span class="sxs-lookup"><span data-stu-id="76c5f-102">Create a search to collect data</span></span>

<span data-ttu-id="76c5f-103">Sous l'onglet **recherches** de votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **nouvelle recherche** et en suivant l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="76c5f-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="76c5f-104">Nommer votre recherche et donner une description</span><span class="sxs-lookup"><span data-stu-id="76c5f-104">Name your search and give description</span></span>

<span data-ttu-id="76c5f-p101">Chaque recherche avec un cas doit avoir un nom unique. Vous pouvez éventuellement fournir une description pour votre recherche.</span><span class="sxs-lookup"><span data-stu-id="76c5f-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="76c5f-107">Définir vos conditions</span><span class="sxs-lookup"><span data-stu-id="76c5f-107">Define your conditions</span></span>

<span data-ttu-id="76c5f-p102">Vous pouvez définir les conditions de votre recherche à l'aide des cartes de condition prédéfinies ou du langage KQL (Keyword Query Language). Pour plus d'informations, consultez la rubrique [créer des requêtes de recherche](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="76c5f-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="76c5f-110">Choisir les dépositaires à rechercher</span><span class="sxs-lookup"><span data-stu-id="76c5f-110">Choose the custodians to search from</span></span>

<span data-ttu-id="76c5f-p103">Une fois que vous avez défini vos conditions, vous devez choisir les emplacements sur lesquels vous souhaitez effectuer la recherche. Pour ce faire, vous pouvez spécifier les dépositaires que vous avez déjà ajoutés au cas dans lequel vous souhaitez effectuer une recherche. En sélectionnant un dépositaire, vous lancez la recherche par rapport à toutes les sources de données mappées au dépositaire. Pour plus d'informations sur l'ajout de dépositaires à votre cas et sur la gestion de leurs sources de données, voir [utiliser des dépositaires](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="76c5f-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="76c5f-115">Choisir les emplacements non privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="76c5f-115">Choose non-custodial locations</span></span>

<span data-ttu-id="76c5f-p104">Dans certains cas, vous souhaiterez peut-être Rechercher des sources de données qui ne sont pas mappées à un dépositaire. Dans ce cas, vous pouvez spécifier les emplacements de recherche, ou choisir de rechercher tous les emplacements de contenu pour un service Office 365 spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange ou tous les sites SharePoint et OneDrive entreprise).</span><span class="sxs-lookup"><span data-stu-id="76c5f-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>