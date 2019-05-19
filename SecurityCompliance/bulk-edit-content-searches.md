---
title: Modifier en bloc les recherches de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Utilisez l’éditeur de recherche en bloc dans le centre de sécurité et de conformité dans Office 365 ou Microsoft 365 pour modifier rapidement les emplacements de requête et de contenu pour une ou plusieurs recherches de contenu.
ms.openlocfilehash: d4f79cc323b752d020606e22ff72a47bc03e9ae9
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152216"
---
# <a name="bulk-edit-content-searches"></a>Modifier en bloc les recherches de contenu

Vous pouvez utiliser l’éditeur de recherche en bloc dans l’outil de recherche de contenu pour modifier plusieurs recherches en même temps. Cet outil vous permet de modifier rapidement les emplacements de requête et de contenu pour une ou plusieurs recherches. Vous pouvez ensuite ré-exécuter les recherches et obtenir de nouveaux résultats de recherche estimés pour les recherches modifiées. L’éditeur vous permet également de copier et coller des requêtes et des emplacements de contenu à partir d’un fichier Microsoft Excel ou texte. Cela signifie que vous pouvez utiliser l’outil statistiques de recherche pour afficher les statistiques d’une ou de plusieurs recherches, exporter les statistiques vers un fichier CSV dans lequel vous pouvez modifier les requêtes et les emplacements de contenu dans Excel. Ensuite, vous utilisez l’éditeur de recherche en bloc pour ajouter les requêtes et les emplacements de contenu révisés aux recherches. Une fois que vous avez modifié une ou plusieurs recherches, vous pouvez les redémarrer et obtenir de nouveaux résultats de recherche estimés.
  
Pour plus d’informations sur l’utilisation de l’outil statistiques de recherche, voir [afficher les statistiques des mots clés pour les résultats de la recherche de contenu](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Utiliser l’éditeur de recherche en bloc pour modifier les requêtes

1. Accédez à [https://protection.office.com](https://protection.office.com), puis cliquez sur **recherche de contenu**de **recherche** \> .
    
2. Dans la liste des recherches, sélectionnez une ou plusieurs recherches, puis cliquez sur le bouton ![](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png)éditeur de recherche en bloc de l’éditeur de **recherche en** bloc.
    
    ![Sélectionnez une ou plusieurs recherches, puis cliquez sur éditeur de recherche en bloc.](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    Les informations suivantes s’affichent dans la page **requêtes** de l’éditeur de recherche en bloc. 
    
    ![La page de l’éditeur de recherche en bloc affiche les requêtes pour les recherches sélectionnées.](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a. La colonne de **recherche** affiche le nom de la recherche de contenu. Comme indiqué précédemment, vous pouvez modifier la requête pour plusieurs recherches. 
    
    b. La colonne **requête** affiche la requête pour la recherche de contenu figurant dans la colonne **recherche** . Si la requête a été créée à l’aide de la fonctionnalité de liste de mots clés, les mots `(c:s)`clés sont séparés par le texte * * **. Cela indique que les mots clés sont connectés par l’opérateur **or** . En outre, si la requête inclut des conditions, les mots clés et les conditions sont séparés par le texte `(c:c)`* * **. Cela indique que les mots clés (ou phases de mots clés) sont connectés aux conditions par l’opérateur **and** . Par exemple, dans la capture d’écran précédente The for Search ContosoSearch1, la requête KQL qui est `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` équivalente `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`à.
    
3. Pour modifier une requête, cliquez dans la cellule de la requête que vous souhaitez modifier et effectuez l’une des opérations suivantes. Notez que la cellule est entouré d’un cadre bleu lorsque vous cliquez dessus.
    
   - Tapez la nouvelle requête dans la cellule. Notez que vous ne pouvez pas modifier une partie de la requête. Vous devez taper toute la requête.
    
      Ou
    
    - Colle une nouvelle requête dans la cellule. Cela suppose que vous ayez copié le texte de la requête à partir d’un fichier, tel qu’un fichier texte ou un fichier Excel.
    
4. Une fois que vous avez modifié une ou plusieurs requêtes dans la page **requêtes** , cliquez sur **Enregistrer**.
    
    La requête révisée est affichée dans la colonne **requête** de la recherche sélectionnée. 
    
5. Cliquez sur **Fermer** pour fermer l’éditeur de recherche en bloc. 
    
6. Sur la page **recherche de contenu** , sélectionnez la recherche que vous avez modifiée, puis cliquez sur **Démarrer** la recherche pour relancer la recherche à l’aide de la requête révisée. 
    
Voici quelques conseils pour modifier les requêtes à l’aide de l’éditeur de recherche en bloc:
  
- Copiez la requête existante (à l’aide de **Ctrl C** ) dans un fichier texte. Modifiez la requête dans le fichier texte, puis copiez-la et collez-la (à l’aide de la **combinaison de touches Ctrl V** ) dans la cellule de la page **requêtes** . 
    
- Vous pouvez également copier des requêtes à partir d’autres applications (telles que Microsoft Word ou Microsoft Excel). Toutefois, sachez que vous pouvez ajouter par inadvertance des caractères non pris en charge à une requête à l’aide de l’éditeur de recherche en bloc. La meilleure façon d’empêcher les caractères non pris en charge est de taper simplement la requête dans une cellule sur la page **requêtes** . Vous pouvez aussi copier votre requête à partir de Word ou d'Excel, puis la coller dans un éditeur de texte brut, comme le Bloc-notes Microsoft. Enregistrez ensuite le fichier texte, puis sélectionnez **ANSI** dans la liste déroulante **Encodage**. Cette action supprime tout le formatage et tous les caractères non pris en charge. Ensuite, vous pouvez copier et coller la requête à partir du fichier texte vers la page **requêtes** . 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Utiliser l’éditeur de recherche en bloc pour modifier les emplacements de contenu

1. Dans l’éditeur de recherche en bloc pour une ou plusieurs recherches sélectionnées, cliquez sur **activer l’éditeur de localisation en bloc**, puis cliquez sur le lien **emplacements** qui s’affiche sur la page. 
    
    Les informations suivantes s’affichent dans la page **emplacements** de l’éditeur de recherche en bloc. 
    
    ![Cliquez sur Activer l’éditeur de l’emplacement en bloc, puis cliquez sur emplacements pour ajouter ou supprimer des emplacements de contenu.](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **Boîtes aux lettres à rechercher** Cette section affiche une colonne pour chaque recherche de contenu sélectionnée et la ligne pour chaque boîte aux lettres incluse dans la recherche. Une coche indique que la boîte aux lettres est incluse dans la recherche. Vous pouvez ajouter des boîtes aux lettres supplémentaires à une recherche en tapant l’adresse de messagerie de la boîte aux lettres dans une ligne vide, puis en cliquant sur la case à cocher de la recherche de contenu à laquelle vous souhaitez l’ajouter. Ou vous pouvez supprimer une boîte aux lettres d’une recherche en désélectionnant la case à cocher.
    
    b. **Sites SharePoint à rechercher** Cette section affiche une ligne pour chaque site SharePoint et OneDrive qui est inclus dans chaque recherche de contenu sélectionnée. Une coche indique que le site est inclus dans la recherche. Vous pouvez ajouter des sites supplémentaires à une recherche en tapant l’URL du site dans une ligne vide, puis en cliquant sur la case à cocher de la recherche de contenu à laquelle vous souhaitez l’ajouter. Ou vous pouvez supprimer un site d’une recherche en désélectionnant la case à cocher.
    
    c. **Autres options de recherche** Cette section indique si les éléments et les dossiers publics non indexés sont inclus dans la recherche. Pour inclure ces éléments, vérifiez que la case est cochée. Pour les supprimer, désactivez la case à cocher.
    
2. Une fois que vous avez modifié une ou plusieurs sections de la page **emplacements** , cliquez sur **Enregistrer**.
    
    Les emplacements de contenu révisés sont affichés dans la section appropriée pour les recherches sélectionnées.
    
3. Cliquez sur **Fermer** pour fermer l’éditeur de recherche en bloc. 
    
4. Sur la page **recherche de contenu** , sélectionnez la recherche que vous avez modifiée, puis cliquez sur **Démarrer** la recherche pour relancer la recherche à l’aide des emplacements de contenu révisés. 
    
Voici quelques conseils pour modifier les emplacements de contenu à l’aide de l’éditeur de recherche en bloc:
  
- Vous pouvez modifier les recherches de contenu pour effectuer une recherche dans toutes les boîtes aux lettres ou tous les sites de l’organisation en tapant **tous les** éléments dans une ligne vide dans la section **boîtes aux lettres à rechercher** ou **sites SharePoint à rechercher** , puis en cliquant sur la case à cocher. 
    
- Vous pouvez ajouter plusieurs emplacements de contenu à une ou plusieurs recherches en copiant plusieurs lignes à partir d’un fichier texte ou d’un fichier Excel, puis en les collant dans une section de la page **emplacements** . Une fois que vous avez ajouté de nouveaux emplacements, veillez à activer la case à cocher pour chaque recherche à laquelle vous souhaitez ajouter l’emplacement. 
    
    > [!TIP]
    > Pour générer une liste d’adresses de messagerie pour tous les utilisateurs de votre organisation, exécutez la commande PowerShell à l’étape 2 dans [utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et le site OneDrive entreprise](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Ou utilisez le script dans [créer une liste de tous les emplacements onedrive de votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) pour générer une liste de tous les sites onedrive entreprise de votre organisation. Notez que vous devez ajouter l’URL du domaine de site mon site organization’s (par exemple, https://contoso-my.sharepoint.com) aux sites OneDrive entreprise créés par le script. Une fois que vous avez une liste d’adresses de messagerie ou de sites OneDrive entreprise, vous pouvez les copier et les coller dans la page **emplacements** de l’éditeur de recherche en bloc. 
  
- Une fois que vous avez cliqué sur **Enregistrer** pour enregistrer les modifications apportées à l’éditeur de recherche en bloc, l’adresse de messagerie des boîtes aux lettres que vous avez ajoutées à une recherche est validée. Si l’adresse de messagerie n’existe pas, un message d’erreur s’affiche indiquant que la boîte aux lettres est introuvable. Notez que les URL des sites ne sont pas validées. 
  

