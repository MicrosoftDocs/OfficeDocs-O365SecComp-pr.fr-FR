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
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="fe6d3-102">Créer une recherche pour collecter des données</span><span class="sxs-lookup"><span data-stu-id="fe6d3-102">Create a search to collect data</span></span>

<span data-ttu-id="fe6d3-103">Sous l’onglet **recherches** de votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **nouvelle recherche** et en suivant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="fe6d3-104">Nommer votre recherche et donner une description</span><span class="sxs-lookup"><span data-stu-id="fe6d3-104">Name your search and give description</span></span>

<span data-ttu-id="fe6d3-105">Chaque recherche avec un cas doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="fe6d3-106">Vous pouvez éventuellement fournir une description pour votre recherche.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="fe6d3-107">Définir vos conditions</span><span class="sxs-lookup"><span data-stu-id="fe6d3-107">Define your conditions</span></span>

<span data-ttu-id="fe6d3-108">Vous pouvez définir les conditions de votre recherche à l’aide des cartes de condition prédéfinies ou du langage KQL (Keyword Query Language).</span><span class="sxs-lookup"><span data-stu-id="fe6d3-108">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="fe6d3-109">Pour plus d’informations, consultez la rubrique [créer des requêtes de recherche](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="fe6d3-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="fe6d3-110">Choisir les dépositaires à rechercher</span><span class="sxs-lookup"><span data-stu-id="fe6d3-110">Choose the custodians to search from</span></span>

<span data-ttu-id="fe6d3-111">Une fois que vous avez défini vos conditions, vous devez choisir les emplacements sur lesquels vous souhaitez effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="fe6d3-112">Pour ce faire, vous pouvez spécifier les dépositaires que vous avez déjà ajoutés au cas dans lequel vous souhaitez effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="fe6d3-113">En sélectionnant un dépositaire, vous lancez la recherche par rapport à toutes les sources de données mappées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="fe6d3-114">Pour plus d’informations sur l’ajout de dépositaires à votre cas et sur la gestion de leurs sources de données, voir [utiliser des dépositaires](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6d3-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="fe6d3-115">Choisir les emplacements non privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="fe6d3-115">Choose non-custodial locations</span></span>

<span data-ttu-id="fe6d3-116">Dans certains cas, vous souhaiterez peut-être Rechercher des sources de données qui ne sont pas mappées à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="fe6d3-117">Dans ce cas, vous pouvez spécifier les emplacements de recherche, ou choisir de rechercher tous les emplacements de contenu pour un service Office 365 spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange ou tous les sites SharePoint et OneDrive entreprise).</span><span class="sxs-lookup"><span data-stu-id="fe6d3-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>