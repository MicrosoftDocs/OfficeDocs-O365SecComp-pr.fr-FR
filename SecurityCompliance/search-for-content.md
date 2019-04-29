---
title: Rechercher du contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Utilisez l'outil eDiscovery de la recherche de contenu dans le centre de sécurité & Compliance Center pour trouver rapidement des messages électroniques dans des boîtes aux lettres Exchange, des documents dans des sites SharePoint et des emplacements OneDrive, et des conversations de messagerie instantanée dans Skype entreprise.
ms.openlocfilehash: 3e8e0594cac700fe37ee7a4a6c889dbf862cd0fb
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33403012"
---
# <a name="search-for-content-in-office-365"></a>Rechercher du contenu dans Office 365

Utilisez l'outil de recherche de contenu dans le centre de sécurité & Compliance Center pour rechercher rapidement le courrier électronique dans les boîtes aux lettres Exchange, les documents dans les sites SharePoint et les emplacements OneDrive, ainsi que les conversations de messagerie instantanée dans Skype entreprise. Vous pouvez utiliser l'outil de recherche de contenu pour rechercher des courriers électroniques, des documents et des conversations de messagerie instantanée dans les outils de collaboration Office 365 tels que les groupes Microsoft teams et Office 365.
  
## <a name="search-for-content"></a>Recherche de contenu

La première étape consiste à utiliser l'outil de recherche de contenu pour choisir les emplacements de contenu à rechercher et configurer une requête de mot clé afin de rechercher des éléments spécifiques. Vous pouvez également laisser la requête vide et renvoyer tous les éléments dans les emplacements cibles.
  
- [Créer et exécuter](content-search.md) une recherche de contenu 
    
- [Créer des requêtes de recherche et utiliser des conditions](keyword-queries-and-search-conditions.md) pour affiner votre recherche 
    
- [Configurer le filtrage des autorisations de recherche](permissions-filtering-for-content-search.md) pour permettre à un gestionnaire eDiscovery de rechercher uniquement des sous-ensembles de boîtes aux lettres ou de sites dans votre organisation 
    
- [Exécuter une recherche de liste d'ID](csv-file-for-an-id-list-content-search.md) pour rechercher des messages électroniques spécifiques 
    
- [Rechercher des boîtes aux lettres en nuage](search-cloud-based-mailboxes-for-on-premises-users.md) pour les utilisateurs locaux dans Office 365

- [Afficher les statistiques des mots clés](view-keyword-statistics-for-content-search.md) pour les résultats d'une recherche et affiner la requête si nécessaire 
    
- [Rechercher des données](use-content-search-to-search-third-party-data-that-was-imported.md) tierces que votre organisation a importées dans Office 365 
    
- [Modification en bloc](bulk-edit-content-searches.md) des emplacements de requête et de contenu pour plusieurs recherches 
    
- [Nouvelle tentative de recherche de contenu](retry-failed-content-search.md) pour résoudre une erreur d'emplacement de contenu

- [Conserver les destinataires CCI](https://docs.microsoft.com/exchange/policy-and-compliance/holds/preserve-bcc-recipients-and-group-members) pour pouvoir les Rechercher 


## <a name="perform-actions-on-content-you-find"></a>Effectuer des actions sur le contenu que vous trouvez

Après avoir exécuté une recherche et l'avoir affinée si nécessaire, l'étape suivante consiste à effectuer une opération avec les résultats renvoyés par la recherche. Vous pouvez exporter et télécharger les résultats sur votre ordinateur local ou dans le cas d'une attaque par courrier électronique dans votre organisation, vous pouvez supprimer les résultats d'une recherche à partir de boîtes aux lettres utilisateur.
  
- [Exporter les résultats d'une recherche de contenu](export-search-results.md) et les télécharger sur votre ordinateur local 
    
- [Rechercher et supprimer des messages électroniques](search-for-and-delete-messages-in-your-organization.md) , tels que des messages dont le contenu est un virus, une pièce jointe dangereuse ou des messages de hameçonnage 
    
- [Exporter un rapport](export-a-content-search-report.md) sur les résultats d'une recherche de contenu, sans exporter les résultats réels 
    
- [Augmentation de la vitesse de téléchargement lors de l'exportation des résultats de](increase-download-speeds-when-exporting-ediscovery-results.md) recherche 
    
## <a name="learn-more-about-content-search"></a>En savoir plus sur la recherche de contenu

La recherche de contenu est facile à utiliser, mais elle est également un outil puissant. En arrière-plan, il y a beaucoup de choses. Plus vous en saurez plus sur le service informatique et vous comprenez son comportement et ses limitations, plus vous l'utiliserez pour répondre aux besoins de recherche et d'enquête de votre organisation. Pour en savoir plus, approfondissez les sujets suivants :
  
- [Éléments partiellement indexés dans Exchange et SharePoint](partially-indexed-items-in-content-search.md) , et comment les inclure ou les exclure lorsque vous exportez et téléchargez des résultats de recherche 
    
- [Examen des éléments partiellement indexés](investigating-partially-indexed-items-in-ediscovery.md) et détermination de l'exposition de votre organisation à ceux-ci 
    
- [Limites de l'outil de recherche de contenu](limits-for-content-search.md), telles que le nombre maximal de recherches que vous pouvez exécuter simultanément et le nombre maximal d'emplacements de contenu que vous pouvez inclure dans une seule recherche 
    
- Les [résultats de recherche estimés et réels](differences-between-estimated-and-actual-ediscovery-search-results.md) , ainsi que les raisons pour lesquelles il peut y avoir des différences entre eux lorsque vous exportez et téléchargez des résultats de recherche 
    
- [Déduplication dans les résultats](de-duplication-in-ediscovery-search-results.md) de la recherche que vous pouvez activer lorsque vous exportez des messages électroniques qui sont les résultats d'une recherche 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Utiliser des scripts pour les scénarios avancés

Parfois, vous devez effectuer des tâches de recherche de contenu plus complexes, complexes et répétitives. Dans ce cas, il est plus facile et rapide d'utiliser des commandes PowerShell dans le centre de sécurité & Compliance Center. Pour faciliter cette opération, nous avons créé un certain nombre de scripts PowerShell du centre de sécurité & pour vous aider à effectuer des tâches complexes liées à la recherche de contenu.
  
- [Recherche de dossiers de site et de boîte aux lettres spécifiques](use-content-search-for-targeted-collections.md) (appelé une *collection ciblée* ) lorsque vous êtes certain que les éléments réactifs à un cas se trouvent dans ce dossier 
    
- [Rechercher dans la boîte aux lettres et l'emplacement OneDrive](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) une liste d'utilisateurs 
    
- [Créer, générer des rapports et supprimer plusieurs recherches](create-report-on-and-delete-multiple-content-searches.md) pour identifier et détruire rapidement et efficacement les données de recherche 
    
- [Cloner une recherche de contenu](clone-a-content-search.md) et comparer rapidement les résultats de différentes requêtes de recherche par mot clé exécutées sur les mêmes emplacements de contenu; ou utiliser le script pour gagner du temps en évitant d'entrer un grand nombre d'emplacements de contenu lors de la création d'une recherche 
    

