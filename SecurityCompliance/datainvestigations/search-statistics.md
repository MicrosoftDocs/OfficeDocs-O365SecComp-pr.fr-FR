---
title: Statistiques de recherche
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
ms.openlocfilehash: 99310723ed0c157c45363c45c4cca56200d263a7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153596"
---
# <a name="search-statistics"></a>Statistiques de recherche

Un moyen efficace de valider les résultats de la recherche lors de l’examen d’un incident de données consiste à consulter les statistiques de vos résultats de recherche pour vous assurer qu’ils s’alignent sur vos attentes. Une fois la recherche terminée, les statistiques de haut niveau suivantes s’affichent sous **État** sur la page de menu volant des détails de recherche:

![Page de menu volant de recherche statisics sur les détails de la recherche](../media/SearchDetailsFlyout.png)

- Nombre et taille estimés des éléments correspondant aux critères de recherche.

- Nombre et taille des éléments partiellement indexés (également appelés *éléments*non indexés) qui ne peuvent pas faire l’objet d’une recherche, mais qui ont été trouvés dans les emplacements de contenu qui ont été inclus dans la recherche.

- Nombre de boîtes aux lettres et de sites ayant fait l’objet d’une recherche.

Pour afficher des statistiques plus détaillées, cliquez sur **statistiques** sur la page de menu volant détails de la recherche. Sur la page **statistiques de recherche** , vous pouvez afficher le résumé de la recherche, l’emplacement du niveau supérieur contenant les éléments qui correspondent aux résultats de la recherche, ainsi que des statistiques détaillées sur la requête de recherche.

![Liste déroulante des statistiques de recherche](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a>Résumé

Dans l’affichage de **synthèse** , vous pouvez voir les résultats de la recherche décomposés par type d’emplacement (par exemple, des emplacements de boîtes aux lettres Exchange et des sites SharePoint). Les informations suivantes s’affichent pour chaque type d’emplacement:

- Nombre d’emplacements qui ont des éléments correspondant aux critères de recherche.

- Nombre total d’éléments de chaque type d’emplacement correspondant aux critères de recherche.

- Taille totale des éléments de chaque type d’emplacement correspondant aux critères de recherche.

## <a name="top-locations"></a>Emplacements les plus fréquents

Dans l’affichage des **emplacements de niveau supérieur** , vous pouvez voir les emplacements de contenu individuels avec le plus grand nombre d’éléments correspondant aux critères de recherche. Pour chaque emplacement de contenu, les informations suivantes sont affichées:

- Nom de l’emplacement; l’adresse de messagerie des boîtes aux lettres et l’URL des sites SharePoint

- Type d’emplacement

- Nombre d’éléments correspondant aux critères de recherche

- Taille totale de tous les éléments correspondant aux critères de recherche.

## <a name="queries"></a>Requêtes

Dans l’affichage **requêtes** , vous pouvez afficher des statistiques détaillées pour chaque composant de la requête de recherche. Si vous avez utilisé la liste de mots clés dans la requête de recherche, vous pouvez afficher les statistiques améliorées dans l’affichage **requêtes** qui indiquent le nombre d’éléments qui correspondent à chaque mot clé ou expression de mot clé. Cela peut vous aider à identifier rapidement les parties de la requête qui sont les plus efficaces (et les moins). 

Les informations suivantes sont affichées dans l’affichage **requêtes** :

 - **Type d’emplacement** : type d’emplacement de contenu pour les statistiques affichées dans la ligne.

- **Partie** : cette colonne affiche l’une des valeurs suivantes: **Primary** ou **Keyword**. **Principal** signifie que la ligne présente des statistiques sur l’ensemble de la requête; **Mot clé** signifie que les statistiques de la ligne sont pour l’un des composants de requête.

- **Condition** : composant de requête réel de la requête de recherche à laquelle la ligne fait référence. Si la valeur dans la colonne **composant** est **principale**, les statistiques de l’ensemble de la requête de recherche sont affichées; Si la valeur est **mot clé**, les statistiques du composant de la requête affichée dans la colonne **requête** sont affichées. Par exemple, si la liste de mots-clés a été utilisée, les statistiques l’un des mots-clés sont affichés.

  Voici quelques autres éléments à connaître concernant les statistiques affichées dans la colonne **requêtes** :
  
  - Lorsque vous recherchez tout le contenu dans des boîtes aux lettres (en ne spécifiant aucun mot-clé), la requête réelle est **(dimensionner > = 0)** de sorte que tous les éléments soient renvoyés.
  
  - Lorsque vous effectuez des recherches dans des sites SharePoint et OneDrive, les deux composants suivants sont ajoutés à la requête de recherche:
    
    **Non IsExternalContent: 1** -cela exclut le contenu d’une organisation SharePoint locale
    
    **Non isOneNotePage: 1** -cela exclut tous les fichiers OneNote, car il s’agit de doublons de tous les documents qui correspondent à la requête de recherche.

- **Emplacements dans la recherche** Nombre d’emplacements de contenu contenant des éléments qui correspondent à la requête de recherche pour la partie ou la condition affichée dans la ligne. Notez que les boîtes aux lettres d’archivage sont comptabilisées comme un emplacement distinct si elles contiennent des éléments qui correspondent aux critères de recherche.

- **Items** : nombre total d’éléments correspondant aux critères de recherche pour le composant ou la condition affiché dans la ligne.

- **Size** : nombre total d’éléments correspondant aux critères de recherche pour le composant ou la condition affiché dans la ligne.