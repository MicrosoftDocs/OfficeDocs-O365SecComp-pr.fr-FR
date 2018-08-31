---
title: Préparer un fichier CSV pour une liste d’ID de recherche de contenu dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Pour créer une recherche de liste d’ID qui renvoie un message électronique spécifique, utilisez le fichier Results.csv ou Items.csv non indexées à partir d’une recherche de contenu existante. ID liste recherches sont généralement utilisés pour renvoyer des éléments de boîte aux lettres partiellement indexé.
ms.openlocfilehash: 28e4a66e5c9be1817881004b1e4b3a3e6d4bfdb9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528497"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>Préparer un fichier CSV pour une liste d’ID de recherche de contenu dans Office 365

Vous pouvez rechercher les messages électroniques spécifique de boîte aux lettres et d’autres éléments de boîte aux lettres à l’aide d’une liste d’ID Exchange. Pour créer une recherche de liste d’ID (auparavant appelée une recherche ciblée), vous envoyer un fichier (CSV) de valeurs séparées par des virgules qui identifie les éléments de boîte aux lettres spécifique à rechercher. Ce fichier CSV, vous utilisez le fichier **Results.csv** ou le fichier **Items.csv non indexés** sont inclus lorsque vous exportez les résultats de recherche de contenu ou que vous exportez un rapport de recherche de contenu à partir d’et de la recherche de contenu existante. Puis modifier un de ces fichiers pour indiquer les éléments spécifiques pour rechercher et puis créer une nouvelle recherche de liste d’ID et envoyer le fichier CSV. 
  
Voici une vue d’ensemble rapide du processus de création d’une recherche de liste d’ID.
  
1. Créer et exécuter une recherche de contenu nouveau ou guidé dans la sécurité &amp; centre de conformité.
    
2. Exporter les résultats de recherche de contenu ou l’exportation de l’état de la recherche de contenu. Pour plus d’informations, voir :
    
    - [Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
    - [Exporter un rapport de recherche de contenu](export-a-content-search-report.md)
    
3. Modifier le fichier **Results.csv** ou **Items.csv non indexés** et identifier les éléments de boîte aux lettres spécifique que vous souhaitez inclure dans la recherche de la liste des ID. Voir les [instructions](#prepare-the-csv-file-for-an-id-list-search) de préparation d’un fichier CSV pour une recherche de liste d’ID. 
    
4. Créer une liste d’ID de recherche (voir les [instructions](#create-an-id-list-search)) et envoyer le fichier CSV que vous avez préparé. Recherche uniquement la requête de recherche qui est créée pour les éléments sélectionnés dans le fichier CSV.
    
> [!NOTE]
> ID liste recherches sont uniquement pris en charge pour les éléments de boîte aux lettres. Vous ne pouvez pas rechercher pour SharePoint et documents OneDrive dans un ID de liste de recherche. 
  
 **Pourquoi créer une recherche de liste d’ID ?** Si vous ne parvenez pas à déterminer que si un élément ne répond à une demande de découverte électronique basée sur les métadonnées dans les fichiers **Results.csv** ou **Items.csv non indexés** , vous pouvez utiliser une recherche de liste d’ID pour trouver, afficher un aperçu, puis l’exporter que cet élément pour déterminer s’il a sensible à la casse vous êtes étudie. ID liste recherches sont généralement utilisés pour rechercher et retourner un ensemble spécifique d’éléments non indexés. 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>Préparer le fichier CSV pour une recherche de liste d’ID

Après avoir exporté les résultats de la recherche ou du rapport pour une recherche de contenu, vous pouvez effectuer les étapes suivantes pour préparer le fichier CSV pour une recherche de liste d’ID. Chaque élément de la recherche de la liste des ID identifie ce fichier CSV.
  
Notez que vous pouvez utiliser un fichier CSV à partir d’une recherche incluant les comptes OneDrive et sites SharePoint, mais vous pouvez sélectionner *uniquement* les éléments de boîte aux lettres pour une recherche de liste d’ID. Si vous sélectionnez un document dans SharePoint ou OneDrive, le fichier CSV échouera validation lorsque vous créez une recherche de liste d’ID. 
  
1. Ouvrez le fichier **Results.csv** ou **Items.csv non indexés** dans Excel. 
    
2. Insérer une nouvelle colonne et nommez-le **sélectionnés**. Peu importe où vous ajoutez la colonne. Pour des raisons pratiques, envisagez d’insertion vers la gauche de la première colonne.
    
3. Dans la colonne **sélectionnée** , tapez **Oui** dans la cellule qui correspond à l’élément que vous souhaitez rechercher. Répétez cette étape pour chaque élément que vous souhaitez rechercher. 
    
    > [!IMPORTANT]
    > Lorsque vous ouvrez le fichier CSV dans Excel, le format de données pour la colonne **ID de Document** est modifié en **Général**. Ainsi, dans l’affichage de l’ID de document pour un élément dans la notation scientifique. Par exemple, le document QU'ID de « 481037338205 » est affiché sous la forme « 4.81037E + 11 » vous devez effectuer la procédure suivante pour modifier le format de données de la colonne **ID de Document** **numéro** pour restaurer le format correct pour l’ID de document. Si vous ne le faites pas, la recherche de liste d’ID qui utilise le fichier CSV échouera. 
  
4. Avec le bouton droit de la colonne **ID de Document** entier, puis sélectionnez le **Format de cellule**.
    
5. Dans la zone **catégorie** , cliquez sur **nombre**.
    
6. Modifier le nombre de décimales à **0**, puis cliquez sur **OK** pour enregistrer vos modifications. Notez que les valeurs dans la colonne ID de Document sont modifiées en numéros. 
    
    Voici un exemple de l’un fichier CSV est prêt à être soumis à une recherche de contenu de liste ID.
    
    ![Exemple d’un fichier CSV pour une recherche de contenu ciblé](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. Enregistrez le fichier CSV ou utiliser **Enregistrer sous** pour enregistrer le fichier avec le nom de fichier différent. Dans les deux cas, veillez à enregistrer le fichier au format CSV. 
  
## <a name="create-an-id-list-search"></a>Créer une recherche de liste d’ID

L’étape suivante consiste à créer une liste d’ID de recherche de contenu et envoyer le fichier CSV que vous avez préparé à l’étape précédente.
  
> [!IMPORTANT]
> Vous devez créer une recherche de liste d’ID ne plus de 2 jours après avoir exporté les résultats ou un état à partir d’une recherche de contenu. Si la recherche des résultats ou un état où exportés remonte à plus de 2 jours, vous devez ré-exporter les résultats de recherche ou un état pour générer les fichiers CSV mis à jour. Vous pouvez ensuite préparer un des fichiers CSV mis à jour et permet de créer une recherche de liste d’ID. 
  
1. Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**.
    
2. Dans la page de **recherche** , cliquez sur la flèche en regard de l’option ![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nouvelle recherche**, puis cliquez sur **Rechercher par ID de liste**.
    
    ![Cliquez sur Rechercher par ID de liste à partir de la nouvelle liste déroulante de recherche](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. Dans la fenêtre **de recherche à la liste d’ID de** mobile, nom de la recherche (et éventuellement le décrire) puis cliquez sur **Parcourir** et sélectionnez le fichier CSV que vous avez préparé à l’étape précédente. 
    
    Office 365 tente de valider le fichier CSV. Si la validation échoue, un message d’erreur s’affiche qui peuvent vous aider à résoudre les erreurs de validation. Le fichier CSV doit être validés pour créer une recherche de liste d’ID.
    
4. Après le CSV fichier est validé avec succès, cliquez sur **recherche** pour la recherche de la liste des ID de créer. 
    
    Voici un exemple de résultats de la recherche estimés et la requête qui est générée pour une recherche de liste d’ID.
    
    ![Requête de recherche pour une recherche de contenu ciblée dans le volet détails](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    Notez que le nombre d’éléments estimées affichées dans les statistiques pour la recherche de l’ID doit correspondre au nombre d’éléments que vous avez sélectionné dans le fichier CSV.
    
5. Afficher un aperçu ou exporter les éléments renvoyés par la recherche de la liste des ID.
    
> [!NOTE]
> Si vous déplacez une boîte aux lettres après la création d’une recherche de liste d’ID, la requête pour la recherche ne renvoie pas les éléments spécifiés. C’est parce que la propriété **DocumentId** des éléments de boîte aux lettres sont modifiées lors d’une boîte aux lettres est déplacée. Dans l’instance rare lorsqu’une boîte aux lettres est déplacée après avoir créé une recherche de la liste des ID, vous devez créer une recherche de contenu (ou mettre à jour les résultats de recherche pour la recherche de contenu existante), puis exporter la recherche des résultats ou un état pour générer les fichiers CSV mis à jour qui peuvent être utilisés  Pour créer une nouvelle recherche de liste d’ID. 
