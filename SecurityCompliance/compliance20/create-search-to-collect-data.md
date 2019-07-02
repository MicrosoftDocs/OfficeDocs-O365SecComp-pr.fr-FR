---
title: Create a search
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
ms.openlocfilehash: 1aa4ce6e406e4b3a3b72b9d93f651416b1fc65f9
ms.sourcegitcommit: 803baca9f99a6691fb41a3308e799752e4d8f20c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35222248"
---
# <a name="create-a-search"></a><span data-ttu-id="2e1ea-102">Create a search</span><span class="sxs-lookup"><span data-stu-id="2e1ea-102">Create a search</span></span>

<span data-ttu-id="2e1ea-103">Sous l’onglet **recherches** de votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **nouvelle recherche** et en suivant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-it-a-description"></a><span data-ttu-id="2e1ea-104">Nommez votre recherche et donnez-lui une description.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-104">Name your search and give it a description</span></span>

<span data-ttu-id="2e1ea-105">Chaque recherche avec un cas doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="2e1ea-106">Vous pouvez éventuellement fournir une description pour votre recherche.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-search-query-and-conditions"></a><span data-ttu-id="2e1ea-107">Définition de la requête et des conditions de recherche</span><span class="sxs-lookup"><span data-stu-id="2e1ea-107">Define your search query and conditions</span></span>

<span data-ttu-id="2e1ea-108">Vous pouvez définir la requête de mots clés et les conditions de la recherche à l’aide des cartes de condition prédéfinies ou du langage de requête de mot clé (KQL).</span><span class="sxs-lookup"><span data-stu-id="2e1ea-108">You can define the keywords query and any conditions for the search by using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="2e1ea-109">Pour plus d’informations, consultez la rubrique [créer des requêtes de recherche](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="2e1ea-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="2e1ea-110">Choisir les dépositaires à rechercher</span><span class="sxs-lookup"><span data-stu-id="2e1ea-110">Choose the custodians to search from</span></span>

<span data-ttu-id="2e1ea-111">Une fois que vous avez défini vos conditions, vous devez choisir les emplacements sur lesquels vous souhaitez effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="2e1ea-112">Pour ce faire, vous pouvez spécifier les dépositaires que vous avez déjà ajoutés au cas dans lequel vous souhaitez effectuer une recherche.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="2e1ea-113">En sélectionnant un dépositaire, vous lancez la recherche par rapport à toutes les sources de données mappées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="2e1ea-114">Pour plus d’informations sur l’ajout de dépositaires à votre cas et sur la gestion de leurs sources de données, voir [utiliser des dépositaires](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1ea-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="2e1ea-115">Choisir les emplacements non privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="2e1ea-115">Choose non-custodial locations</span></span>

<span data-ttu-id="2e1ea-116">Dans certains cas, vous souhaiterez peut-être Rechercher des sources de données qui ne sont pas mappées à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="2e1ea-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="2e1ea-117">Dans ce cas, vous pouvez spécifier les emplacements de recherche, ou choisir de rechercher tous les emplacements de contenu pour un service Office 365 spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange ou tous les sites SharePoint et OneDrive entreprise).</span><span class="sxs-lookup"><span data-stu-id="2e1ea-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>