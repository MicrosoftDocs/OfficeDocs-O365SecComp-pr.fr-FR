---
title: Afficher les statistiques de mots clés pour les résultats de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Utiliser la fonctionnalité de statistiques de la recherche pour afficher et comparer les statistiques pour plusieurs recherches de contenu de la sécurité Office 365 &amp; centre de conformité. Vous pouvez également configurer la liste des mots clés lorsque vous créez ou modifiez une requête de recherche pour obtenir les statistiques améliorées montrant le nombre d’éléments mis en correspondance chaque mot clé ou une phrase de mots clés.
ms.openlocfilehash: cb71b30b32ff6a24cd68ea5728063c2997d8ada0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528166"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Afficher les statistiques de mots clés pour les résultats de recherche de contenu

Après avoir créé et exécuter une recherche de contenu, vous pouvez afficher des statistiques sur les résultats de recherche estimés. Cela inclut un résumé des résultats de recherche (comme le résumé de l’estimation des résultats de recherche affichés dans le volet de détails), les statistiques de requête tels que le nombre d’emplacements de contenu avec les éléments qui correspondent à la requête de recherche et le nom des emplacements de contenu dont les éléments correspondants plus. Vous pouvez afficher des statistiques pour une ou plusieurs recherches de contenu. Cela vous permet pour comparer les résultats de plusieurs recherches rapidement et de prendre des décisions concernant l’efficacité de vos requêtes de recherche.
  
En outre, vous pouvez configurer des recherches de nouveaux et existants pour retourner les statistiques pour chaque mot clé dans une requête de recherche. Cela vous permet de comparer le nombre de résultats pour chaque mot clé dans une requête et de comparer les statistiques de mots clés à partir de plusieurs recherches.
  
Vous pouvez également télécharger les statistiques de recherche et les statistiques de mots clés dans un fichier CSV. Cela vous permet d’utiliser les fonctionnalités de filtrage et de tri dans Excel pour comparer les résultats et établir des rapports pour vos résultats de recherche.
  
## <a name="get-statistics-for-content-searches"></a>Obtenir les statistiques pour les recherches de contenu

Pour afficher les statistiques de recherches de contenu :
  
1. De sécurité Office 365 &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**.
    
2. Dans la liste de recherche, sélectionnez un ou plusieurs recherches, puis cliquez sur **les statistiques de recherche**![bouton recherche statistiques](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).
    
    ![Sélectionnez plusieurs recherches, puis cliquez sur les statistiques de recherche](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. Dans la page de **statistiques de la recherche** , cliquez sur un des liens suivants pour afficher des statistiques sur les recherches sélectionnés. 
    
    **Résumé**
    
    Cette page affiche les statistiques similaires à celles affichées dans le volet de détails sur la page de **recherche de contenu** . Statistiques pour toutes les recherches sélectionnées sont affichées. Notez que vous pouvez également réexécuter la recherche sélectionnées à partir de cette page pour mettre à jour les statistiques. 
    
    ![Résumé des statistiques pour la recherche sélectionnée](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    r. le nom de la recherche de contenu. Comme indiqué précédemment, vous pouvez afficher et comparer les statistiques de plusieurs recherches.
    
    b. le type d’emplacement du contenu qui a été recherché. Chaque ligne affiche les statistiques de boîtes aux lettres, les sites et les dossiers publics à partir de la recherche spécifiée.
    
    c. le nombre d’emplacements de contenu contenant les éléments qui correspondent à la requête de recherche. Pour les boîtes aux lettres, cette statistique inclut également le nombre de boîtes aux lettres archive qui contiennent des éléments qui correspondent à la requête de recherche.
    
    d. le nombre total d’éléments de l’ensemble spécifié les emplacements de contenu qui correspondent à la requête de recherche. Les exemples de types d’éléments de messages électroniques, éléments de calendrier et des documents. Si un élément contient plusieurs instances d’un mot clé qui est recherchée, elle est comptée uniquement une seule fois dans le nombre total d’éléments. Par exemple, si vous recherchez des mots « stock » ou « fraude » et un message électronique contient trois occurrences du mot « stock », elle est comptée uniquement une seule fois dans la colonne **éléments** . 
    
    e. la taille totale de tous les éléments qui ont été trouvées dans l’emplacement du contenu spécifié qui correspondent à la requête de recherche. 
    
    **Requêtes**
    
    Cette page affiche les statistiques relatives à la requête de recherche.
    
    ![Statistiques de requête de recherche pour les recherches sélectionnés](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    r. le nom de la recherche de contenu qui contient des statistiques de requête pour la ligne.
    
    b. le type d’emplacement du contenu qui concernent les statistiques des requêtes.
    
    c. cette colonne indique quelle partie de la requête de recherche concernent les statistiques. **Principal** indique la requête de recherche. Si vous utilisez une liste de mots-clés lorsque vous créez ou modifiez une requête de recherche, les statistiques pour chaque composant de la requête sont inclus dans ce tableau. Consultez la section [obtenir les statistiques de mots clés pour les recherches de contenu](#get-keyword-statistics-for-content-searches) de cet article pour plus d’informations. 
    
    d. cette colonne contienne la recherche des requêtes exécutées par l’outil de recherche de contenu. Notez que l’outil ajoute automatiquement quelques composants supplémentaires à la requête que vous créez. 

    - Lors de la recherche pour tous les content de boîtes aux lettres (ne pas, en spécifiant les mots clés) la requête de mot clé réel est `size>=0` afin que tous les éléments sont retournés. 
    
     - Lors de la recherche OneDrive et SharePoint Online pour les sites, les deux composants suivants sont ajoutés :
    
          **Pas IsExternalContent:1** - exclut tout le contenu d’une organisation de SharePoint sur site. 
    
          **Pas IsOneNotePage:1** - exclut tous les fichiers OneNote, car il s’agit des doublons de n’importe quel document qui correspond à la requête de recherche. 

    
    e. le nombre d’emplacements de contenu (spécifié par la ** type d’emplacement ** colonne) qui contiennent des éléments qui correspondent à la requête de recherche répertoriée dans la colonne de la **requête** . 
    
    f. le nombre d’éléments (à partir de l’emplacement du contenu spécifié) qui correspondent à la requête de recherche répertoriée dans la colonne de la **requête** . Comme expliqué précédemment, si un élément contient plusieurs instances d’un mot clé qui est recherchée, elle est comptée uniquement une seule fois dans cette colonne. 
    
    g. la taille totale de tous les éléments qui ont été détectés (à l’emplacement de contenu spécifié) qui correspondent à la requête de recherche dans la colonne de la **requête** . 
    
    **Emplacements supérieurs**
    
    Cette page affiche les statistiques sur le nombre d’éléments qui correspondent à la requête de recherche dans chaque emplacement du contenu qui a été recherché. Les emplacements de haut 1 000 sont affichés. Si vous affichez les statistiques de plusieurs recherches, les emplacements de 1 000 supérieurs de chaque recherche sont affichés. Notez qu’un emplacement de contenu n’est pas inclus dans cette page si elle ne contient pas tous les éléments qui correspondent à la requête de recherche.
    
    ![Statistiques sur le nombre d’éléments trouvés dans les emplacements de contenu qui ont été exclus](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    r. le nom de l’emplacement du contenu.
    
    b. le type d’emplacement du contenu qui concernent les statistiques d’emplacement.
    
    c. il existe des colonnes pour chaque recherche que vous affichez les statistiques de. Cette colonne affiche le nombre (et la taille totale) d’éléments qui correspondent à la requête de recherche dans chaque emplacement du contenu. Notez que lorsque vous affichez les statistiques de plusieurs recherches, « NA » dans cette colonne indique que l’emplacement du contenu n’a pas été inclus dans cette recherche. 

## <a name="get-keyword-statistics-for-content-searches"></a>Obtenir les statistiques de mots clés pour les recherches de contenu

Précédente comme expliqué, la page de **requêtes** affiche la requête de recherche et le nombre (et la taille) d’éléments qui correspondent à la requête. Si vous utilisez une liste de mots-clés lorsque vous créez ou modifiez une requête de recherche, vous pouvez obtenir les statistiques améliorées montrant le nombre d’éléments correspondent à chaque mot clé ou une phrase de mots clés. Cela peut vous aider à identifier rapidement les parties de la requête sont les plus (et moins) efficaces. Par exemple, si un mot clé renvoie un grand nombre d’éléments, vous pouvez choisir d’affiner la requête de mot clé pour limiter les résultats de recherche. Vous pouvez configurer une liste des mots clés lorsque vous créez ou modifiez une recherche de contenu. 
  
Pour créer une liste des mots clés et afficher les statistiques de mots clés pour une recherche de contenu :
  
1. De sécurité Office 365 &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**.
    
2. Dans la liste des recherches de contenu, cliquez sur et une recherche, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Cliquez sur **requête** , puis effectuez les opérations suivantes : 
    
    ![Cliquez sur la case à cocher Afficher mot clé liste, tapez un mot clé dans chaque ligne](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    a. Cliquez sur la case à cocher **Afficher la liste des mots clés** . 
    
    b. Tapez un mot clé ou la phase de mot clé dans une ligne dans le tableau de mots clés. Par exemple, tapez **budgétaire** de la première ligne et tapez **sécurité** dans la deuxième ligne. 
    
4. Après avoir ajouté les mots clés que vous souhaitez rechercher et obtenir des statistiques de, cliquez sur **Rechercher** pour lancer la recherche révisée. 
    
5. Lors de la recherche est terminée, sélectionnez-le dans la liste de recherche, puis cliquez sur **les statistiques de recherche** ![bouton recherche statistiques](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png). Vous pouvez également afficher et comparer les statistiques de mots clés pour plusieurs recherches.
    
6. Dans la page de **statistiques de la recherche** , cliquez sur **requête** pour afficher les statistiques de mots clés pour la recherche sélectionnée. 
    
    ![Les statistiques de chaque mot clé pour la recherche sélectionnée sont affichées.](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Comme le montre la capture d’écran précédente, les statistiques de chaque mot clé sont affichées ; Cela inclut : 
    
    - Statistiques de mots clés pour chaque type d’emplacement de contenu inclus dans la recherche.
    
    - La requête de recherche pour chaque mot clé, qui inclut toutes les conditions de la requête de recherche. 
    
    - La requête de recherche complète (identifié comme **principale** dans la colonne **composant** ) et les statistiques de la requête terminée. Notez que ce sont les mêmes statistiques affichés sur la page de **Résumé** . 
