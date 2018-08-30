---
title: Rechercher du contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/4/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: df2d1e0f-b476-42c9-aade-4a260b24f193
description: Utiliser l’outil de découverte électronique de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour trouver rapidement les e-mails de boîtes aux lettres Exchange, des documents dans les sites SharePoint et les emplacements de OneDrive et les conversations dans Skype pour les entreprises de messagerie instantanée.
ms.openlocfilehash: b9595f66633cca762ea74eaa9402f50ec08c2d7c
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229976"
---
# <a name="search-for-content-in-office-365"></a>Rechercher du contenu dans Office 365

Utiliser l’outil de recherche de contenu de la sécurité &amp; centre de conformité pour trouver rapidement les e-mails de boîtes aux lettres Exchange, des documents dans les sites SharePoint et les emplacements de OneDrive et les conversations dans Skype pour les entreprises de messagerie instantanée. Vous pouvez utiliser l’outil de recherche de contenu pour la recherche pour le courrier électronique, les documents et les conversations dans Office 365 les outils de collaboration tels que Microsoft Teams et Office 365 groupes de messagerie instantanée.
  
## <a name="search-for-content"></a>Recherche de contenu

La première étape consiste à démarrer à l’aide de l’outil de recherche de contenu pour choisir les emplacements de contenu pour rechercher et configurer une requête de mot clé pour rechercher des éléments spécifiques. Ou bien, vous pouvez simplement rien dans la requête et renvoyer tous les éléments dans les emplacements cibles.
  
- [Créer et exécuter](content-search.md) une recherche de contenu 
    
- [Génération de requêtes de recherche et d’utiliser des conditions](keyword-queries-and-search-conditions.md) pour affiner la recherche 
    
- [Configurer les autorisations de recherche le filtrage](permissions-filtering-for-content-search.md) afin qu’un gestionnaire de découverte électronique peut uniquement rechercher le sous-ensemble de boîtes aux lettres ou des sites dans votre organisation 
    
- [Exécuter une recherche de liste d’ID](csv-file-for-an-id-list-content-search.md) pour rechercher des messages électroniques spécifiques 
    
- [Boîtes aux lettres de recherche basée sur le cloud](search-cloud-based-mailboxes-for-on-premises-users.md) pour les utilisateurs locaux dans Office 365

- [Afficher les statistiques de mots clés](view-keyword-statistics-for-content-search.md) pour les résultats de recherche et puis affiner la requête si nécessaire 
    
- [Recherche de données tierce](use-content-search-to-search-third-party-data-that-was-imported.md) que votre organisation a importés vers Office 365 
    
- [Modification](bulk-edit-content-searches.md) de la requête et les emplacements de contenu pour plusieurs recherches 
    
## <a name="perform-actions-on-content-you-find"></a>Effectuer des actions sur le contenu que vous trouvez

Après avoir exécuté une recherche et affiner selon les besoins, l’étape suivante consiste à effectuer une opération avec les résultats renvoyés par la recherche. Vous pouvez exporter et télécharger les résultats sur votre ordinateur local ou dans le cas d’une attaque par courrier électronique dans votre organisation, vous pouvez supprimer les résultats d’une recherche de boîtes aux lettres utilisateur.
  
- [Exporter les résultats d’une recherche de contenu](export-search-results.md) et les télécharger sur votre ordinateur local 
    
- [Rechercher et supprimer les messages électroniques](search-for-and-delete-messages-in-your-organization.md) , tels que les messages que le contenu d’un virus, les pièces jointes dangereuses ou hameçonnage 
    
- [Exporter un rapport](export-a-content-search-report.md) sur les résultats d’une recherche de contenu, sans exporter les résultats réels 
    
- [Augmenter la vitesse de téléchargement](increase-download-speeds-when-exporting-ediscovery-results.md) lorsque vous exportez des résultats de la recherche 
    
## <a name="learn-more-about-content-search"></a>Pour plus d’informations sur la recherche de contenu

Recherche de contenu est facile à utiliser, mais il est également un outil puissant. Arrière-plan, il y a beaucoup de passer. Plus vous connaissez à son sujet et connaître son comportement et ses limitations, plus vous utiliserez pour les besoins de recherche et d’enquête de votre organisation. En savoir plus sur :
  
- [Partiellement indexé éléments dans Exchange et SharePoint](partially-indexed-items-in-content-search.md) et comment inclure ou exclure lorsque vous exportez et téléchargez les résultats de recherche 
    
- [Examiner les éléments indexés partiellement](investigating-partially-indexed-items-in-ediscovery.md) et déterminer l’exposition de votre organisation 
    
- [Limites de l’outil de recherche de contenu](limits-for-content-search.md), tels que le nombre maximal de recherches que vous pouvez exécuter en même temps et le nombre maximal d’emplacements de contenu que vous pouvez inclure dans une seule recherche 
    
- [Durée et les résultats de la recherche](differences-between-estimated-and-actual-ediscovery-search-results.md) et les raisons pourquoi il peut y avoir des différences entre eux lorsque vous exportez et téléchargez les résultats de la recherche 
    
- [La déduplication dans les résultats de recherche](de-duplication-in-ediscovery-search-results.md) que vous pouvez activer lorsque vous exportez des messages électroniques qui sont le résultat d’une recherche 
    
## <a name="use-scripts-for-advanced-scenarios"></a>Utiliser des scripts pour des scénarios avancés

Vous devrez parfois des tâches plus avancées, complexe et répétitives recherche de contenu. Dans ce cas, il est simple et rapide pour utiliser les commandes PowerShell la sécurité &amp; centre de conformité. Pour vous aider à simplifier ce processus, nous avons créé un numéro de sécurité &amp; scripts PowerShell de centre de conformité pour vous aider à effectuer des tâches liées à la recherche de contenu complexes.
  
- [Boîte aux lettres spécifique de recherche et les dossiers de site](use-content-search-for-targeted-collections.md) (appelé un *ciblés collection* ) lorsque vous êtes convaincu que les éléments réactifs à un cas sont situés dans ce dossier 
    
- Pour obtenir la liste des utilisateurs de [Rechercher la boîte aux lettres et l’emplacement de OneDrive](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md) 
    
- [Créer, rapport et de supprimer plusieurs recherches](create-report-on-and-delete-multiple-content-searches.md) rapidement et efficacement identifier et éliminez les données de recherche 
    
- [Cloner une recherche de contenu](clone-a-content-search.md) et de comparer rapidement les résultats des requêtes de recherche de mot clé différent s’exécutent sur les mêmes emplacements de contenu ; ou utilisez le script pour économiser du temps sans avoir à saisir un grand nombre d’emplacements de contenu lorsque vous créez une nouvelle recherche 
    

