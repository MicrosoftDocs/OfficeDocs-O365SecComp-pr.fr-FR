---
title: Rechercher dans toutes les boîtes aux lettres et tous les sites à l’aide du centre eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: Dans le centre eDiscovery dans Office 365, vous pouvez rechercher toutes les boîtes aux lettres Exchange Online, SharePoint Online et des OneDrive pour les sites d’entreprise dans une recherche de découverte électronique unique. Pour rechercher toutes les sources de contenu dans l’organisation, un gestionnaire de découverte électronique doit avoir les autorisations de découverte électronique approprié pour chaque source de contenu.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527943"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a><span data-ttu-id="8af88-104">Rechercher dans toutes les boîtes aux lettres et tous les sites à l’aide du centre eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8af88-104">Search all mailboxes and sites using the eDiscovery Center</span></span>

<span data-ttu-id="8af88-p102">Dans le centre eDiscovery dans Office 365, vous pouvez rechercher toutes les boîtes aux lettres Exchange Online, SharePoint Online et des OneDrive pour les sites d’entreprise dans une recherche de découverte électronique unique. Pour rechercher toutes les sources de contenu dans l’organisation, un gestionnaire de découverte électronique doit avoir les autorisations de découverte électronique approprié pour chaque source de contenu.</span><span class="sxs-lookup"><span data-stu-id="8af88-p102">In the eDiscovery Center in Office 365, you can search all Exchange Online mailboxes, SharePoint Online sites, and OneDrive for Business sites in a single eDiscovery search. To search all content sources in the organization, an eDiscovery manager must be assigned the appropriate eDiscovery permissions for each content source.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="8af88-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8af88-107">Before you begin</span></span>

- <span data-ttu-id="8af88-p103">Un gestionnaire eDiscovery doit disposer des autorisations appropriées pour effectuer une recherche dans une source de contenu. Pour plus d’informations sur l’attribution des autorisations de découverte électronique sur les sites et les boîtes aux lettres, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8af88-p103">An eDiscovery manager must be assigned the appropriate permissions to search a content source. For more information about assigning eDiscovery permissions to mailboxes and sites, see the following:</span></span> 
    
  - [<span data-ttu-id="8af88-110">Attribution d'autorisations eDiscovery dans Exchange</span><span class="sxs-lookup"><span data-stu-id="8af88-110">Assign eDiscovery permissions in Exchange</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [<span data-ttu-id="8af88-111">Attribuer des autorisations eDiscovery dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8af88-111">Assign eDiscovery permissions in SharePoint Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [<span data-ttu-id="8af88-112">Attribuer des autorisations de découverte électronique aux sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="8af88-112">Assign eDiscovery permissions to OneDrive for Business sites</span></span>](assign-permissions-to-onedrive-for-business-sites.md)
    
- <span data-ttu-id="8af88-p104">Vous pouvez rechercher un maximum de 10 000 boîtes aux lettres et un nombre illimité de SharePoint Online et OneDrive pour les sites dans une requête de recherche de découverte électronique unique. Toutefois, si vous spécifiez les sites spécifiques à rechercher, la limite est de 100 sites.</span><span class="sxs-lookup"><span data-stu-id="8af88-p104">You can search a maximum of 10,000 mailboxes and an unlimited number of SharePoint Online and OneDrive for Business sites in a single eDiscovery search query. However, if you specify the specific sites to search, the limit is 100 sites.</span></span>
    
- <span data-ttu-id="8af88-115">Voir la section [plus d’informations](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) pour une description des limites lors de l’affichage des résultats lors de la recherche de tous les sites et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8af88-115">See the [More information](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) section for a description of the limits when viewing the results when searching all mailboxes and sites.</span></span> 
    
- <span data-ttu-id="8af88-116">Pour plus d’informations sur la création de requêtes de recherche dans le centre eDiscovery, consultez [créer et requêtes eDiscovery exécution](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span><span class="sxs-lookup"><span data-stu-id="8af88-116">For more information about creating search queries in the eDiscovery Center, see [Create and run eDiscovery queries](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span></span>
    
## <a name="search-all-locations"></a><span data-ttu-id="8af88-117">Rechercher dans tous les emplacements</span><span class="sxs-lookup"><span data-stu-id="8af88-117">Search all locations</span></span>

1. <span data-ttu-id="8af88-118">Dans le centre eDiscovery, ouvrez le cas de découverte électronique pour lequel vous souhaitez exécuter la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="8af88-118">In the eDiscovery Center, open the eDiscovery case that you want to run the search query for.</span></span>
    
2. <span data-ttu-id="8af88-119">Sous **recherche et exportation**, cliquez sur une requête existante ou cliquez sur **nouvel élément** pour créer une nouvelle requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="8af88-119">Under **Search and Export**, click an existing query or click **New item** to create a new search query.</span></span> 
    
3. <span data-ttu-id="8af88-120">Dans la page de requête de recherche, dans la section **Sources**, cliquez sur **Modifier l’étendue de requête**.</span><span class="sxs-lookup"><span data-stu-id="8af88-120">On the search query page, in the **Sources** section, click **Modify Query Scope**.</span></span>
    
4. <span data-ttu-id="8af88-121">Sur la page **Modifier l’étendue de requête**, cliquez sur **Tout rechercher**, puis sélectionnez les emplacements de contenu dans lesquels effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="8af88-121">On the **Modify Query Scope** page, click **Search everything**, and select the content locations to search.</span></span>
    
  - <span data-ttu-id="8af88-122">Sélectionnez **Exchange** pour rechercher toutes les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8af88-122">Select **Exchange** to search all mailboxes.</span></span> 
    
  - <span data-ttu-id="8af88-123">Sélectionnez **SharePoint** pour rechercher tous les SharePoint Online et OneDrive pour les sites de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8af88-123">Select **SharePoint** to search all SharePoint Online and OneDrive for Business sites.</span></span> 
    
  - <span data-ttu-id="8af88-124">Sélectionnez **Exchange** et **SharePoint** pour rechercher tous les emplacements de contenu dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8af88-124">Select both **Exchange** and **SharePoint** to search all content locations in your organization.</span></span> 
    
![Rechercher dans tous les sites et toutes les boîtes aux lettres](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. <span data-ttu-id="8af88-126">Cliquez sur **OK** pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="8af88-126">Click **OK** to save the changes.</span></span> 
    
6. <span data-ttu-id="8af88-p105">Complétez ou modifiez d’autres informations sur la page de requête de recherche, telles que la requête de mot clé, la plage de dates ou la limitation des types spécifiques de contenu dans lesquels effectuer la recherche. Lorsque vous êtes prêt à exécuter la requête, cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="8af88-p105">Complete or revise other information on the search query page, such as the keyword query, the date range, or narrowing the specific types of content to search for. When you're ready to run the query, click **Search**.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="8af88-129">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="8af88-129">More information</span></span>
<span data-ttu-id="8af88-130"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="8af88-130"></span></span>

- <span data-ttu-id="8af88-131">Les 500 premières boîtes aux lettres et les 500 premiers sites avec le plus de résultats sont répertoriés sous **Sources** sur la page **Requête**.</span><span class="sxs-lookup"><span data-stu-id="8af88-131">The top 500 mailboxes and the top 500 sites with the most results are listed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="8af88-132">Le nombre total d’éléments trouvés dans toutes les sources de contenu et leur taille totale combinée s’affichent sous **Sources** sur la page **Requête**. 
</span><span class="sxs-lookup"><span data-stu-id="8af88-132">The total number of items found in all content sources and their combined total size are displayed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="8af88-133">Vous pouvez prévisualiser les 200 résultats de recherche les plus récents situés dans les boîtes aux lettres Exchange ou les sites SharePoint sur la page **Requête**.</span><span class="sxs-lookup"><span data-stu-id="8af88-133">You can preview the 200 most recent search results located in Exchange mailboxes or SharePoint sites on the **Query** page.</span></span> 
    
    <span data-ttu-id="8af88-134">La capture d’écran suivante montre un exemple de résultats de recherche affichés sur la page **Requête** lors de la recherche dans tous les sites et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8af88-134">The following screenshot shows an example of the search results displayed on the **Query** page when you search all mailboxes and sites.</span></span> 
    
    ![Capture d’écran des résultats de recherche de tous les emplacements](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

