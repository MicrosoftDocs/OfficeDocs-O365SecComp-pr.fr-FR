---
title: Afficher les statistiques de mot clé pour les résultats de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Utilisez la fonctionnalité statistiques de recherche pour afficher et comparer les statistiques de plusieurs recherches de contenu dans &amp; le centre de sécurité conformité Office 365. Vous pouvez également configurer la liste de mots clés lors de la création ou de la modification d'une requête de recherche pour obtenir des statistiques améliorées qui indiquent le nombre d'éléments correspondant à chaque expression de mot clé ou mot clé.
ms.openlocfilehash: c62f04e690661a5a7022fa00f727d1be39e74f12
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214824"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Afficher les statistiques de mot clé pour les résultats de recherche de contenu

Une fois que vous avez créé et exécuté une recherche de contenu, vous pouvez afficher des statistiques sur les résultats de recherche estimés. Cela inclut un résumé des résultats de la recherche (semblable au résumé des résultats de recherche estimés affichés dans le volet d'informations), les statistiques de la requête telles que le nombre d'emplacements de contenu avec des éléments qui correspondent à la requête de recherche et le nom des emplacements de contenu qui ont le plus de correspondances. Vous pouvez afficher des statistiques pour une ou plusieurs recherches de contenu. Cela vous permet de comparer rapidement les résultats de plusieurs recherches et de prendre des décisions sur l'efficacité de vos requêtes de recherche.
  
En outre, vous pouvez configurer des recherches nouvelles et existantes pour renvoyer des statistiques pour chaque mot clé dans une requête de recherche. Cela vous permet de comparer le nombre de résultats pour chaque mot clé dans une requête et de comparer les statistiques de mots clés de plusieurs recherches.
  
Vous pouvez également télécharger les statistiques de recherche et les statistiques sur les mots clés dans un fichier CSV. Cela vous permet d'utiliser les fonctionnalités de filtrage et de tri dans Excel pour comparer les résultats et préparer des rapports pour les résultats de la recherche.
  
## <a name="get-statistics-for-content-searches"></a>Obtenir des statistiques pour les recherches de contenu

Pour afficher les statistiques des recherches de contenu:
  
1. dans le centre de sécurité &amp; conformité Office 365, accédez à recherche de \> **contenu**d' **enquête de recherche &amp; ** .
    
2. Dans la liste des recherches, sélectionnez une ou plusieurs recherches, puis cliquez sur ****![le bouton](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)statistiques de recherche de statistiques de recherche.
    
    ![Sélectionnez plusieurs recherches, puis cliquez sur statistiques de recherche.](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. Sur la page **statistiques de recherche** , cliquez sur l'un des liens suivants pour afficher les statistiques sur les recherches sélectionnées. 
    
    **Résumé**
    
    Cette page affiche des statistiques similaires à celles affichées dans le volet d'informations sur la page **recherche de contenu** . Les statistiques de toutes les recherches sélectionnées sont affichées. Notez que vous pouvez également réexécuter les recherches sélectionnées à partir de cette page pour mettre à jour les statistiques. 
    
    ![Résumé des statistiques pour les recherches sélectionnées](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    a. nom de la recherche de contenu. Comme indiqué précédemment, vous pouvez afficher et comparer les statistiques de plusieurs recherches.
    
    b. type d'emplacement de contenu dans lequel la recherche a été effectuée. Chaque ligne affiche des statistiques pour les boîtes aux lettres, les sites et les dossiers publics à partir de la recherche spécifiée.
    
    c. le nombre d'emplacements de contenu contenant des éléments qui correspondent à la requête de recherche. Pour les boîtes aux lettres, cette statistique inclut également le nombre de boîtes aux lettres d'archivage qui contiennent des éléments qui correspondent à la requête de recherche.
    
    d. nombre total d'éléments de tous les emplacements de contenu spécifiés qui correspondent à la requête de recherche. Les messages électroniques, les éléments de calendrier et les documents sont des exemples de types d'éléments. Si un élément contient plusieurs instances d'un mot clé recherché, il n'est compté qu'une seule fois dans le nombre total d'éléments. Par exemple, si vous recherchez des mots «stock» ou «fraude» et qu'un message électronique contient trois occurrences du mot «stock», il n'est compté qu'une seule fois dans la colonne **éléments** . 
    
    e. taille totale de tous les éléments trouvés dans l'emplacement de contenu spécifié qui correspondent à la requête de recherche. 
    
    **Requêtes**
    
    Cette page affiche des statistiques sur la requête de recherche.
    
    ![Statistiques de requête de recherche pour les recherches sélectionnées](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    a. nom de la recherche de contenu pour laquelle la ligne contient des statistiques de requête.
    
    b. le type d'emplacement de contenu auquel s'appliquent les statistiques de requête.
    
    c. cette colonne indique la partie de la requête de recherche à laquelle les statistiques sont applicables. **Primary** indique l'ensemble de la requête de recherche. Si vous utilisez une liste de mots clés lors de la création ou de la modification d'une requête de recherche, les statistiques de chaque composant de la requête sont incluses dans ce tableau. Pour plus d'informations, rePortez-vous à la section [obtenir des statistiques sur les mots clés pour les recherches de contenu](#get-keyword-statistics-for-content-searches) de cet article. 
    
    d. cette colonne contient la requête de recherche en cours qui est exécutée par l'outil de recherche de contenu. Notez que l'outil ajoute automatiquement quelques composants supplémentaires à la requête que vous créez. 

    - Lorsque vous recherchez tout le contenu dans des boîtes aux lettres (en ne spécifiant pas de mots clés), la `size>=0` requête mot clé réelle est de sorte que tous les éléments soient renvoyés. 
    
     - Lorsque vous effectuez des recherches dans des sites SharePoint Online et OneDrive entreprise, les deux composants suivants sont ajoutés:
    
          **Non IsExternalContent: 1** -exclut le contenu d'une organisation SharePoint locale. 
    
          **Non IsOneNotePage: 1** -exclut tous les fichiers OneNote, car il s'agit de doublons de tous les documents qui correspondent à la requête de recherche. 

    
    e. nombre d'emplacements de contenu (spécifiés par la colonne * * type d'emplacement * *) qui contiennent des éléments correspondant à la requête de recherche indiquée dans la colonne **requête** . 
    
    f. nombre d'éléments (à partir de l'emplacement de contenu spécifié) qui correspondent à la requête de recherche indiquée dans la colonne **requête** . Comme expliqué précédemment, si un élément contient plusieurs instances d'un mot clé recherché, il n'est compté qu'une seule fois dans cette colonne. 
    
    g. taille totale de tous les éléments trouvés (dans l'emplacement de contenu spécifié) qui correspondent à la requête de recherche dans la colonne **requête** . 
    
    **Emplacements les plus fréquents**
    
    Cette page affiche des statistiques sur le nombre d'éléments qui correspondent à la requête de recherche dans chaque emplacement de contenu recherché. Les 1 000 premiers emplacements sont affichés. Si vous affichez les statistiques de plusieurs recherches, les premiers 1 000 emplacements de chaque recherche sont affichés. Notez qu'un emplacement de contenu n'est pas inclus sur cette page s'il ne contient aucun élément correspondant à la requête de recherche.
    
    ![Statistiques sur le nombre d'éléments trouvés dans les emplacements de contenu ayant fait l'objet d'une recherche](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    a. nom de l'emplacement de contenu.
    
    b. le type d'emplacement de contenu auquel les statistiques d'emplacement sont applicables.
    
    c. il existe des colonnes pour chaque recherche dont vous affichez les statistiques. Cette colonne indique le nombre (et la taille totale) des éléments qui correspondent à la requête de recherche dans chaque emplacement de contenu. Notez que lorsque vous affichez des statistiques pour plusieurs recherches, la mention «NA» dans cette colonne indique que l'emplacement de contenu n'a pas été inclus dans cette recherche. 

## <a name="get-keyword-statistics-for-content-searches"></a>Obtenir des statistiques sur les mots clés pour les recherches de contenu

Comme expliqué précédemment, la page **requêtes** affiche la requête de recherche et le nombre (et la taille) des éléments qui correspondent à la requête. Si vous utilisez une liste de mots clés lors de la création ou de la modification d'une requête de recherche, vous pouvez obtenir des statistiques améliorées qui indiquent le nombre d'éléments correspondant à chaque mot clé ou phrase de mots-clés. Cela peut vous aider à identifier rapidement les parties de la requête qui sont les plus efficaces (et les moins). Par exemple, si un mot clé renvoie un grand nombre d'éléments, vous pouvez choisir d'affiner la requête de mot clé pour affiner les résultats de la recherche. Vous pouvez configurer une liste de mots clés lors de la création ou de la modification d'une recherche de contenu. 




  
Pour créer une liste de mots clés et afficher les statistiques de mots clés pour une recherche de contenu:
  
1. dans le centre de sécurité &amp; conformité Office 365, accédez à recherche de \> **contenu**d' **enquête de recherche &amp; ** .
    
2. Dans la liste des recherches de contenu, cliquez sur et sur une recherche, **** ![puis sur modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)l'icône modifier.
    
3. Cliquez sur **requête** , puis effectuez les opérations suivantes: 
    
    ![Cliquez sur la case à cocher Afficher la liste de mots clés et tapez un mot clé dans chaque ligne.](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    a. cliquez sur la case à cocher **afficher la liste de mots clés** . 
    
    b. tapez un mot clé ou une phase de mot clé dans une ligne dans le tableau des mots-clés. Par exemple, tapez **budget** dans la première ligne, puis tapez **sécurité** dans la deuxième ligne. 
    
4. Après avoir ajouté les mots clés pour lesquels vous souhaitez effectuer une recherche et obtenir des statistiques, cliquez sur **Rechercher** pour exécuter la recherche révisée. 
    
5. Une fois la recherche terminée, sélectionnez-la dans la liste des recherches, puis cliquez **** ![sur le bouton](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)statistiques de recherche de statistiques de recherche. Vous pouvez également afficher et comparer des statistiques de mots clés pour plusieurs recherches.
    
6. Sur la page **statistiques de recherche** , cliquez sur **requête** pour afficher les statistiques des mots-clés des recherches sélectionnées. 
    
    ![Les statistiques de chaque mot-clé pour les recherches sélectionnées sont affichées.](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Comme indiqué dans la capture d'écran précédente, les statistiques de chaque mot clé s'affichent; Cela inclut: 
    
    - Statistiques de mots clés pour chaque type d'emplacement de contenu inclus dans la recherche.
    
    - La requête de recherche en cours pour chaque mot-clé, qui inclut toutes les conditions de la requête de recherche. 
    
    - La requête de recherche complète (identifiée comme **principale** dans la colonne **partie** ) et les statistiques de la requête complète. Notez qu'il s'agit des mêmes statistiques affichées dans la page de **Résumé** . 

> [!NOTE]
> Pour vous aider à réduire les problèmes causés par des listes de mots clés volumineux, vous êtes désormais limité à un maximum de 20 lignes dans la liste de mots clés d'une requête de recherche.
