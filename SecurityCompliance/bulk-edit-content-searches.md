---
title: Modification en bloc des recherches de contenu de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Utilisez l’éditeur de recherche en bloc de sécurité Office 365 &amp; centre de conformité pour modifier rapidement les emplacements de requête et de contenu pour une ou plusieurs recherches de contenu.
ms.openlocfilehash: 45c9a3fc4bcc5e5d8ce9945d3094bfb4a39d6dcf
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527987"
---
# <a name="bulk-edit-content-searches-in-the-office-365-security-amp-compliance-center"></a>Modification en bloc des recherches de contenu de sécurité Office 365 &amp; centre de conformité

Vous pouvez utiliser l’éditeur de recherche en bloc de sécurité Office 365 &amp; centre de conformité pour modifier plusieurs recherches de contenu en même temps. À l’aide de cet outil vous permet de modifier rapidement les emplacements de requête et de contenu pour une ou plusieurs recherches. Vous pouvez réexécuter la recherche et obtenir des résultats de recherche estimés nouvelle pour les recherches révisés. L’éditeur vous permet également de copier et coller des requêtes et les emplacements de contenu à partir d’un fichier texte ou un fichier Microsoft Excel. Cela signifie que vous pouvez utiliser l’outil de statistiques de la recherche pour afficher les statistiques d’une ou plusieurs recherches, les statistiques d’exportation vers un fichier CSV dans laquelle vous pouvez modifier les requêtes et les emplacements de contenu dans Excel. Ensuite, vous utilisez l’éditeur de recherche en bloc pour ajouter les requêtes révisés et les emplacements de contenu pour les recherches. Une fois que vous avez modifié une ou plusieurs recherches, vous pouvez redémarrer les et obtenir des résultats de recherche estimés nouveau.
  
Pour plus d’informations sur l’utilisation de l’outil de statistiques de la recherche, voir [Afficher les statistiques de mots clés pour les résultats de recherche de contenu](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Utilisez l’éditeur de recherche en bloc pour modifier les requêtes

1. Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**.
    
2. Dans la liste de recherche, sélectionnez un ou plusieurs recherches, puis cliquez sur **Éditeur de recherche en bloc** ![bouton Éditeur de recherche en bloc](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png).
    
    ![Sélectionnez un ou plusieurs recherches, puis cliquez sur Éditeur de recherche en bloc](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    Les informations suivantes s’affiche dans la page de **requêtes** de l’éditeur de recherche en bloc. 
    
    ![La page Éditeur de recherche en bloc affiche les requêtes pour la recherche sélectionnée](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a la colonne de **recherche** affiche le nom de la recherche de contenu. Comme indiqué précédemment, vous pouvez modifier la requête pour plusieurs recherches. 
    
    b. la colonne de **requête** affiche la requête pour la recherche de contenu répertorié dans la colonne de **recherche** . Si la requête a été créée à l’aide de la fonctionnalité de liste de mots clés, les mots clés sont séparés par le texte ** `(c:s)` **. Cela indique que les mots clés sont connectés par l’opérateur **OR** . En outre, si la requête comprend les conditions, les mots clés et les conditions sont séparées par le texte ** `(c:c)` **. Cela indique que les mots clés (ou phases de mot clé) sont connectés aux conditions par l’opérateur **AND** . Par exemple, dans la capture d’écran précédente le pour la recherche ContosoSearch1, la requête KQL qui équivaut à `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` serait `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`.
    
3. Pour modifier une requête, cliquez dans la cellule de la requête que vous souhaitez modifier et effectuez l’une des opérations suivantes. Notez que la cellule est entourée d’une zone bleue lorsque vous cliquez dessus.
    
   - Dans la cellule, tapez la nouvelle requête. Notez que vous ne pouvez pas modifier une partie de la requête. Vous avez besoin de taper l’intégralité de la requête.
    
      Ou
    
    - Coller une nouvelle requête dans la cellule. Cette procédure suppose que vous avez copié le texte de requête à partir d’un fichier, par exemple un fichier texte ou un fichier Excel.
    
4. Une fois que vous avez modifié une ou plusieurs requêtes sur la page de **requêtes** , cliquez sur **Enregistrer**.
    
    La requête modifiée s’affiche dans la colonne de **requête** pour la recherche sélectionnée. 
    
5. Cliquez sur **Fermer** pour fermer l’éditeur de recherche en bloc. 
    
6. Dans la page de **recherche de contenu** , sélectionnez la recherche que vous avez modifié, cliquez sur **Rechercher pour redémarrer la recherche à l’aide de la requête modifiée** . 
    
Voici quelques conseils pour la modification des requêtes à l’aide de l’éditeur de recherche en bloc :
  
- Copiez la requête existante (à l’aide de **Ctrl C** ) dans un fichier texte. Modifier la requête dans le fichier texte, puis copiez la requête modifiée et collez-la (à l’aide de **Ctrl V** ) dans la cellule dans la page de **requêtes** . 
    
- Vous pouvez également copier des requêtes à partir d’autres applications (tel que Microsoft Word ou Microsoft Excel). Toutefois, sachez que vous pouvez ajouter par inadvertance caractères non pris en charge pour une requête à l’aide de l’éditeur de recherche en bloc. La meilleure façon pour empêcher que des caractères non pris en charge est de taper la requête dans une cellule dans la page de **requêtes** . Vous pouvez également copier une requête à partir de Word ou Excel et puis collez-le dans le fichier dans un éditeur de texte, tel que Microsoft Notepad. Enregistrez le fichier texte, puis sélectionnez **ANSI** dans la liste déroulante **codage** . Cette action supprime tous les caractères non pris en charge et de mise en forme. Ensuite, vous pouvez copier et coller la requête à partir du fichier texte à la page **requêtes** . 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Utilisez l’éditeur de recherche en bloc pour modifier les emplacements de contenu

1. Dans l’éditeur de recherche en bloc pour une ou plusieurs recherches sélectionnés, cliquez sur **Activer l’éditeur d’emplacement en bloc**, puis cliquez sur le lien vers les **emplacements** qui s’affiche dans la page. 
    
    Les informations suivantes s’affiche dans la page **emplacements** de l’éditeur de recherche en bloc. 
    
    ![Cliquez sur Activer en bloc emplacement éditeur, puis cliquez sur emplacements pour ajouter ou supprimer des emplacements de contenu](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **pour rechercher les boîtes aux lettres**de cette section affiche une colonne pour chaque ligne pour chaque boîte aux lettres qui est inclus dans la recherche et recherche de contenu sélectionné. Une coche indique que la boîte aux lettres est inclus dans la recherche. Vous pouvez ajouter des boîtes aux lettres supplémentaires à une recherche en tapant l’adresse de messagerie de la boîte aux lettres dans une ligne vide puis en cliquant sur la case à cocher pour la recherche de contenu que vous souhaitez ajouter. Ou vous pouvez supprimer une boîte aux lettres à partir d’une recherche en désactivant la case à cocher.
    
    b. **les sites SharePoint pour rechercher**cette section affiche une ligne pour chaque site SharePoint et OneDrive inclus dans chaque sélectionné recherche de contenu. Une coche indique que le site est inclus dans la recherche. Vous pouvez ajouter des sites supplémentaires à une recherche en tapant l’URL du site dans une ligne vide et puis en cliquant sur la case à cocher pour la recherche de contenu que vous souhaitez ajouter à. Ou vous pouvez supprimer un site à partir d’une recherche en désactivant la case à cocher.
    
    c. **autres options de recherche**de cette section indique si les dossiers publics et les éléments non indexées sont incluses dans la recherche. Pour inclure ces, assurez-vous que la case à cocher est activée. Pour les supprimer, désactivez la case à cocher.
    
2. Une fois que vous avez modifié une ou plusieurs des sections sur la page **emplacements** , cliquez sur **Enregistrer**.
    
    Les emplacements de contenu révisés sont affichés dans la section appropriée pour les recherches sélectionnés.
    
3. Cliquez sur **Fermer** pour fermer l’éditeur de recherche en bloc. 
    
4. Dans la page **recherche de contenu** , sélectionnez la recherche que vous avez modifié, cliquez sur **Rechercher pour redémarrer la recherche en utilisant les emplacements de contenu révisés** . 
    
Voici quelques conseils pour la modification des emplacements de contenu à l’aide de l’éditeur de recherche en bloc :
  
- Vous pouvez modifier le contenu de recherche pour rechercher toutes les boîtes aux lettres ou des sites dans l’organisation en tapant **tous** dans une ligne vide dans la section **pour rechercher les boîtes aux lettres** ou des **sites SharePoint pour rechercher** et puis en cliquant sur la case à cocher. 
    
- Vous pouvez ajouter plusieurs emplacements de contenu à une ou plusieurs recherches en copiant plusieurs lignes à partir d’un fichier texte ou un fichier Excel et de coller dans une section dans la page **emplacements** . Une fois que vous ajoutez de nouveaux emplacements, veillez à sélectionner la case à cocher de chaque recherche que vous souhaitez ajouter l’emplacement. 
    
    > [!TIP]
    > Pour générer une liste d’adresses de messagerie pour tous les utilisateurs de votre organisation, exécutez la commande PowerShell à l’étape 2 de la [Recherche de contenu utilisés pour rechercher les boîtes aux lettres et OneDrive pour le site de l’entreprise pour une liste d’utilisateurs](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Ou utilisez le script dans [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) pour générer une liste de tous les OneDrive pour les sites dans votre organisation. Notez que vous devez ajouter l’URL de votre du domaine du site Mon site dans l’organisation (par exemple, https://contoso-my.sharepoint.com) à OneDrive pour les sites qui est créé par le script. Après avoir la liste des adresses de messagerie ou OneDrive pour les sites de l’entreprise, vous pouvez copiez et collez-les à la page **emplacements** dans l’éditeur de recherche en bloc. 
  
- Une fois que vous cliquez sur **Enregistrer** pour enregistrer les modifications dans l’éditeur de recherche en bloc, l’adresse de messagerie pour les boîtes aux lettres que vous avez ajouté à une recherche sera validée. Si l’adresse de messagerie n’existe pas, un message d’erreur s’affiche indiquant que la boîte aux lettres est introuvable. Notez que les URL de sites ne sont pas validés. 
  

