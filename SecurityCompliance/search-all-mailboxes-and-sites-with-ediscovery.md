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
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a>Rechercher dans toutes les boîtes aux lettres et tous les sites à l’aide du centre eDiscovery

Dans le centre eDiscovery dans Office 365, vous pouvez rechercher toutes les boîtes aux lettres Exchange Online, SharePoint Online et des OneDrive pour les sites d’entreprise dans une recherche de découverte électronique unique. Pour rechercher toutes les sources de contenu dans l’organisation, un gestionnaire de découverte électronique doit avoir les autorisations de découverte électronique approprié pour chaque source de contenu. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Un gestionnaire eDiscovery doit disposer des autorisations appropriées pour effectuer une recherche dans une source de contenu. Pour plus d’informations sur l’attribution des autorisations de découverte électronique sur les sites et les boîtes aux lettres, voir les rubriques suivantes : 
    
  - [Attribution d'autorisations eDiscovery dans Exchange](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [Attribuer des autorisations eDiscovery dans SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [Attribuer des autorisations de découverte électronique aux sites OneDrive Entreprise](assign-permissions-to-onedrive-for-business-sites.md)
    
- Vous pouvez rechercher un maximum de 10 000 boîtes aux lettres et un nombre illimité de SharePoint Online et OneDrive pour les sites dans une requête de recherche de découverte électronique unique. Toutefois, si vous spécifiez les sites spécifiques à rechercher, la limite est de 100 sites.
    
- Voir la section [plus d’informations](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) pour une description des limites lors de l’affichage des résultats lors de la recherche de tous les sites et les boîtes aux lettres. 
    
- Pour plus d’informations sur la création de requêtes de recherche dans le centre eDiscovery, consultez [créer et requêtes eDiscovery exécution](https://go.microsoft.com/fwlink/p/?LinkID=404032).
    
## <a name="search-all-locations"></a>Rechercher dans tous les emplacements

1. Dans le centre eDiscovery, ouvrez le cas de découverte électronique pour lequel vous souhaitez exécuter la requête de recherche.
    
2. Sous **recherche et exportation**, cliquez sur une requête existante ou cliquez sur **nouvel élément** pour créer une nouvelle requête de recherche. 
    
3. Dans la page de requête de recherche, dans la section **Sources**, cliquez sur **Modifier l’étendue de requête**.
    
4. Sur la page **Modifier l’étendue de requête**, cliquez sur **Tout rechercher**, puis sélectionnez les emplacements de contenu dans lesquels effectuer la recherche.
    
  - Sélectionnez **Exchange** pour rechercher toutes les boîtes aux lettres. 
    
  - Sélectionnez **SharePoint** pour rechercher tous les SharePoint Online et OneDrive pour les sites de l’entreprise. 
    
  - Sélectionnez **Exchange** et **SharePoint** pour rechercher tous les emplacements de contenu dans votre organisation. 
    
![Rechercher dans tous les sites et toutes les boîtes aux lettres](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. Cliquez sur **OK** pour enregistrer les modifications. 
    
6. Complétez ou modifiez d’autres informations sur la page de requête de recherche, telles que la requête de mot clé, la plage de dates ou la limitation des types spécifiques de contenu dans lesquels effectuer la recherche. Lorsque vous êtes prêt à exécuter la requête, cliquez sur **Rechercher**. 
    
## <a name="more-information"></a>Plus d'informations
<a name="moreinfo"> </a>

- Les 500 premières boîtes aux lettres et les 500 premiers sites avec le plus de résultats sont répertoriés sous **Sources** sur la page **Requête**. 
    
- Le nombre total d’éléments trouvés dans toutes les sources de contenu et leur taille totale combinée s’affichent sous **Sources** sur la page **Requête**. 
 
    
- Vous pouvez prévisualiser les 200 résultats de recherche les plus récents situés dans les boîtes aux lettres Exchange ou les sites SharePoint sur la page **Requête**. 
    
    La capture d’écran suivante montre un exemple de résultats de recherche affichés sur la page **Requête** lors de la recherche dans tous les sites et boîtes aux lettres. 
    
    ![Capture d’écran des résultats de recherche de tous les emplacements](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

