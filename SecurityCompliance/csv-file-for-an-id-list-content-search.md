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
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="284f1-104">Préparer un fichier CSV pour une liste d’ID de recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="284f1-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="284f1-p102">Vous pouvez rechercher les messages électroniques spécifique de boîte aux lettres et d’autres éléments de boîte aux lettres à l’aide d’une liste d’ID Exchange. Pour créer une recherche de liste d’ID (auparavant appelée une recherche ciblée), vous envoyer un fichier (CSV) de valeurs séparées par des virgules qui identifie les éléments de boîte aux lettres spécifique à rechercher. Ce fichier CSV, vous utilisez le fichier **Results.csv** ou le fichier **Items.csv non indexés** sont inclus lorsque vous exportez les résultats de recherche de contenu ou que vous exportez un rapport de recherche de contenu à partir d’et de la recherche de contenu existante. Puis modifier un de ces fichiers pour indiquer les éléments spécifiques pour rechercher et puis créer une nouvelle recherche de liste d’ID et envoyer le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="284f1-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="284f1-109">Voici une vue d’ensemble rapide du processus de création d’une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="284f1-110">Créer et exécuter une recherche de contenu nouveau ou guidé dans la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="284f1-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="284f1-p103">Exporter les résultats de recherche de contenu ou l’exportation de l’état de la recherche de contenu. Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="284f1-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="284f1-113">Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="284f1-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="284f1-114">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="284f1-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="284f1-p104">Modifier le fichier **Results.csv** ou **Items.csv non indexés** et identifier les éléments de boîte aux lettres spécifique que vous souhaitez inclure dans la recherche de la liste des ID. Voir les [instructions](#prepare-the-csv-file-for-an-id-list-search) de préparation d’un fichier CSV pour une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="284f1-p105">Créer une liste d’ID de recherche (voir les [instructions](#create-an-id-list-search)) et envoyer le fichier CSV que vous avez préparé. Recherche uniquement la requête de recherche qui est créée pour les éléments sélectionnés dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="284f1-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="284f1-p106">ID liste recherches sont uniquement pris en charge pour les éléments de boîte aux lettres. Vous ne pouvez pas rechercher pour SharePoint et documents OneDrive dans un ID de liste de recherche.</span><span class="sxs-lookup"><span data-stu-id="284f1-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="284f1-p107">**Pourquoi créer une recherche de liste d’ID ?** Si vous ne parvenez pas à déterminer que si un élément ne répond à une demande de découverte électronique basée sur les métadonnées dans les fichiers **Results.csv** ou **Items.csv non indexés** , vous pouvez utiliser une recherche de liste d’ID pour trouver, afficher un aperçu, puis l’exporter que cet élément pour déterminer s’il a sensible à la casse vous êtes étudie. ID liste recherches sont généralement utilisés pour rechercher et retourner un ensemble spécifique d’éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="284f1-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="284f1-124">Préparer le fichier CSV pour une recherche de liste d’ID</span><span class="sxs-lookup"><span data-stu-id="284f1-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="284f1-p108">Après avoir exporté les résultats de la recherche ou du rapport pour une recherche de contenu, vous pouvez effectuer les étapes suivantes pour préparer le fichier CSV pour une recherche de liste d’ID. Chaque élément de la recherche de la liste des ID identifie ce fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="284f1-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="284f1-p109">Notez que vous pouvez utiliser un fichier CSV à partir d’une recherche incluant les comptes OneDrive et sites SharePoint, mais vous pouvez sélectionner *uniquement* les éléments de boîte aux lettres pour une recherche de liste d’ID. Si vous sélectionnez un document dans SharePoint ou OneDrive, le fichier CSV échouera validation lorsque vous créez une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="284f1-129">Ouvrez le fichier **Results.csv** ou **Items.csv non indexés** dans Excel.</span><span class="sxs-lookup"><span data-stu-id="284f1-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="284f1-p110">Insérer une nouvelle colonne et nommez-le **sélectionnés**. Peu importe où vous ajoutez la colonne. Pour des raisons pratiques, envisagez d’insertion vers la gauche de la première colonne.</span><span class="sxs-lookup"><span data-stu-id="284f1-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="284f1-p111">Dans la colonne **sélectionnée** , tapez **Oui** dans la cellule qui correspond à l’élément que vous souhaitez rechercher. Répétez cette étape pour chaque élément que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="284f1-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="284f1-p112">Lorsque vous ouvrez le fichier CSV dans Excel, le format de données pour la colonne **ID de Document** est modifié en **Général**. Ainsi, dans l’affichage de l’ID de document pour un élément dans la notation scientifique. Par exemple, le document QU'ID de « 481037338205 » est affiché sous la forme « 4.81037E + 11 » vous devez effectuer la procédure suivante pour modifier le format de données de la colonne **ID de Document** **numéro** pour restaurer le format correct pour l’ID de document. Si vous ne le faites pas, la recherche de liste d’ID qui utilise le fichier CSV échouera.</span><span class="sxs-lookup"><span data-stu-id="284f1-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="284f1-139">Avec le bouton droit de la colonne **ID de Document** entier, puis sélectionnez le **Format de cellule**.</span><span class="sxs-lookup"><span data-stu-id="284f1-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="284f1-140">Dans la zone **catégorie** , cliquez sur **nombre**.</span><span class="sxs-lookup"><span data-stu-id="284f1-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="284f1-p113">Modifier le nombre de décimales à **0**, puis cliquez sur **OK** pour enregistrer vos modifications. Notez que les valeurs dans la colonne ID de Document sont modifiées en numéros.</span><span class="sxs-lookup"><span data-stu-id="284f1-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="284f1-143">Voici un exemple de l’un fichier CSV est prêt à être soumis à une recherche de contenu de liste ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Exemple d’un fichier CSV pour une recherche de contenu ciblé](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="284f1-p114">Enregistrez le fichier CSV ou utiliser **Enregistrer sous** pour enregistrer le fichier avec le nom de fichier différent. Dans les deux cas, veillez à enregistrer le fichier au format CSV.</span><span class="sxs-lookup"><span data-stu-id="284f1-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="284f1-147">Créer une recherche de liste d’ID</span><span class="sxs-lookup"><span data-stu-id="284f1-147">Create an ID list search</span></span>

<span data-ttu-id="284f1-148">L’étape suivante consiste à créer une liste d’ID de recherche de contenu et envoyer le fichier CSV que vous avez préparé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="284f1-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="284f1-p115">Vous devez créer une recherche de liste d’ID ne plus de 2 jours après avoir exporté les résultats ou un état à partir d’une recherche de contenu. Si la recherche des résultats ou un état où exportés remonte à plus de 2 jours, vous devez ré-exporter les résultats de recherche ou un état pour générer les fichiers CSV mis à jour. Vous pouvez ensuite préparer un des fichiers CSV mis à jour et permet de créer une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="284f1-152">Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**.</span><span class="sxs-lookup"><span data-stu-id="284f1-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="284f1-153">Dans la page de **recherche** , cliquez sur la flèche en regard de l’option ![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nouvelle recherche**, puis cliquez sur **Rechercher par ID de liste**.</span><span class="sxs-lookup"><span data-stu-id="284f1-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Cliquez sur Rechercher par ID de liste à partir de la nouvelle liste déroulante de recherche](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="284f1-155">Dans la fenêtre **de recherche à la liste d’ID de** mobile, nom de la recherche (et éventuellement le décrire) puis cliquez sur **Parcourir** et sélectionnez le fichier CSV que vous avez préparé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="284f1-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="284f1-p116">Office 365 tente de valider le fichier CSV. Si la validation échoue, un message d’erreur s’affiche qui peuvent vous aider à résoudre les erreurs de validation. Le fichier CSV doit être validés pour créer une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="284f1-159">Après le CSV fichier est validé avec succès, cliquez sur **recherche** pour la recherche de la liste des ID de créer.</span><span class="sxs-lookup"><span data-stu-id="284f1-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="284f1-160">Voici un exemple de résultats de la recherche estimés et la requête qui est générée pour une recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Requête de recherche pour une recherche de contenu ciblée dans le volet détails](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="284f1-162">Notez que le nombre d’éléments estimées affichées dans les statistiques pour la recherche de l’ID doit correspondre au nombre d’éléments que vous avez sélectionné dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="284f1-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="284f1-163">Afficher un aperçu ou exporter les éléments renvoyés par la recherche de la liste des ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="284f1-p117">Si vous déplacez une boîte aux lettres après la création d’une recherche de liste d’ID, la requête pour la recherche ne renvoie pas les éléments spécifiés. C’est parce que la propriété **DocumentId** des éléments de boîte aux lettres sont modifiées lors d’une boîte aux lettres est déplacée. Dans l’instance rare lorsqu’une boîte aux lettres est déplacée après avoir créé une recherche de la liste des ID, vous devez créer une recherche de contenu (ou mettre à jour les résultats de recherche pour la recherche de contenu existante), puis exporter la recherche des résultats ou un état pour générer les fichiers CSV mis à jour qui peuvent être utilisés  Pour créer une nouvelle recherche de liste d’ID.</span><span class="sxs-lookup"><span data-stu-id="284f1-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
