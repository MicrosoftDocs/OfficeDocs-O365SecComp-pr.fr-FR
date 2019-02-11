---
title: Statistiques de recherche
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: 0cfc1e5f04887cbdbcc0be8854fc50d6f9b5f1f2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706005"
---
# <a name="search-statistics"></a>Statistiques de recherche

Une manière, vous pouvez valider vos résultats de recherche consiste à consulter les statistiques sur les résultats pour vous assurer qu’ils s’alignent à vos attentes. Lorsqu’une recherche est terminée, les statistiques de haut niveau sont affichés dans la fenêtre Détails de recherche mobile :
- Nombre et le volume des éléments récupérés par la recherche
- Nombre et le volume des partiellement indexé/non indexés les éléments qui ont été détectés dans les emplacements de recherche
- Nombre de boîtes aux lettres et les emplacements de recherche. Afin d’afficher des statistiques plus détaillées, cliquez sur « Statistiques » à partir de la fenêtre Détails de recherche mobile.

## <a name="summary"></a>Résumé

Dans l’affichage de synthèse, vous pouvez voir les résultats de recherche par type d’emplacement (par exemple, Exchange). Pour chaque type d’emplacement, vous pouvez voir :
- Nombre d’emplacements dont les éléments qui remplissent les conditions de recherche
- Nombre d’éléments à partir de ces emplacements qui remplissent les conditions de recherche
- Volume total des éléments répondant aux conditions de la recherche.

## <a name="top-locations"></a>Emplacements supérieurs

Dans la vue des emplacements supérieure, vous voyez les emplacements individuels avec le plus de correspondances. Pour chaque emplacement, vous voyez s’afficher :
- Nom de l’emplacement (par exemple, les URL SharePoint)
- Type d'emplacement
- Nombre d’éléments qui remplissent les conditions de recherche
- Volume total des éléments répondant aux conditions de la recherche.

## <a name="queries"></a>Requêtes

Si vous avez utilisé le mot clé (c:s) ou des lignes de mots clés dans votre requête, vous pouvez voir la répartition de votre requête en mode de requêtes par type d’emplacement. Pour chaque type d’emplacement, vous voyez s’afficher :

- Partie : cette colonne aura soit le mot « Principal » ou « Mots clés ». « Principal » signifie que la ligne affiche les statistiques sur l’intégralité de la requête, tandis que « Mots clés » signifie qu’un des composants de requête.

- Requête : le composant de requête fait référence la ligne. Si la partie est « Principal », il s’agit de l’intégralité de la requête ; Si le composant a été « Mots clés », vous verrez un des composants de requête ici.
  
  - Lorsque vous recherchez toutes les boîtes aux lettres contenuédition (en spécifiant ne pas les mots clés), la requête réelle est (taille > = 0) afin que tous les éléments sont retournés.
  
  - Lors de la recherche OneDrive et SharePoint Online pour les sites, les deux composants suivants sont ajoutés :
    
    - PAS IsExternalContent:1 - exclut tout le contenu d’une organisation de SharePoint sur site
    
    - PAS isOneNotePage : 1 - exclut tous les fichiers OneNote, car il s’agit des doublons de n’importe quel document qui correspond à la requête de recherche.

- Nombre d’emplacements dont les éléments qui remplissent les conditions de recherche.

- Nombre d’éléments à partir de ces emplacements qui remplissent les conditions de recherche.

- Volume total des éléments répondant aux conditions de la recherche.

## <a name="refiners"></a>Affinements

Pour les boîtes aux lettres Exchange, le mode affinements offre des répartitions supplémentaires par ItemClass, l’expéditeur et destinataire. Pour chaque emplacement et affinement de la valeur, vous pouvez voir le nombre de documents qui ont été renvoyé par la recherche.