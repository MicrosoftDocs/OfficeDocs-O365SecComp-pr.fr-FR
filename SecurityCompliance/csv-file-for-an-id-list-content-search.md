---
title: Préparer un fichier CSV pour une recherche de contenu de liste d'ID dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Utilisez le fichier results. csv ou unindexed Items. csv à partir d'une recherche de contenu existante pour créer une recherche de liste d'ID qui renvoie un message électronique spécifique. Les recherches de liste d'ID sont généralement utilisées pour renvoyer des éléments de boîte aux lettres partiellement indexés.
ms.openlocfilehash: 558a8512ed133995b2cc1d0d8b78fd7f08d11168
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296737"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="33de5-104">Préparer un fichier CSV pour une recherche de contenu de liste d'ID dans Office 365</span><span class="sxs-lookup"><span data-stu-id="33de5-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="33de5-p102">Vous pouvez rechercher des messages électroniques de boîte aux lettres spécifiques et d'autres éléments de boîte aux lettres à l'aide d'une liste d'ID Exchange. Pour créer une recherche de liste d'ID (anciennement appelée recherche ciblée), vous devez soumettre un fichier de valeurs séparées par des virgules (CSV) qui identifie les éléments de boîte aux lettres spécifiques à rechercher. Pour ce fichier CSV, vous utilisez le fichier **results. csv** ou le fichier d' **éléments non indexés. csv** qui est inclus lorsque vous exportez les résultats de recherche de contenu ou que vous exportez un rapport de recherche de contenu à partir de et de la recherche de contenu existante. Ensuite, modifiez l'un de ces fichiers pour indiquer les éléments spécifiques à rechercher, puis créez une nouvelle recherche de liste d'ID et soumettez le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="33de5-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="33de5-109">Voici une présentation rapide du processus de création d'une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="33de5-110">Créez et exécutez une recherche de contenu, nouvelle ou guidée, &amp; dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="33de5-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="33de5-p103">ExPortez les résultats de la recherche de contenu ou exportez le rapport de recherche de contenu. Pour plus d'informations, voir:</span><span class="sxs-lookup"><span data-stu-id="33de5-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="33de5-113">Exporter les résultats de la recherche de contenu du &amp; Centre de sécurité conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="33de5-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="33de5-114">Exporter un rapport de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="33de5-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="33de5-p104">Modifiez le fichier **results. csv** ou **unindexed Items. csv** et identifiez les éléments de boîte aux lettres spécifiques que vous souhaitez inclure dans la recherche de la liste d'ID. Consultez les [instructions](#prepare-the-csv-file-for-an-id-list-search) relatives à la préparation d'un fichier CSV pour une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="33de5-p105">Créez une recherche de liste d'ID (voir les [instructions](#create-an-id-list-search)) et soumettez le fichier CSV que vous avez préparé. La requête de recherche créée ne recherche que les éléments sélectionnés dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="33de5-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="33de5-p106">Les recherches de liste d'ID sont prises en charge uniquement pour les éléments de boîte aux lettres. Vous ne pouvez pas Rechercher des documents SharePoint et OneDrive dans une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="33de5-p107">**Pourquoi créer une recherche de liste d'ID?** Si vous ne parvenez pas à déterminer si un élément répond à une demande eDiscovery basée sur les métadonnées dans les fichiers **results. csv** ou **éléments non indexés. csv** , vous pouvez utiliser une recherche de liste d'ID pour rechercher, prévisualiser, puis exporter cet élément afin de déterminer s'il est répondez à l'affaire que vous étudiez. Les recherches de liste d'ID sont généralement utilisées pour rechercher et renvoyer un ensemble spécifique d'éléments non indexés.</span><span class="sxs-lookup"><span data-stu-id="33de5-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="33de5-124">Préparer le fichier CSV pour une recherche de liste d'ID</span><span class="sxs-lookup"><span data-stu-id="33de5-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="33de5-p108">Après avoir exporté les résultats de recherche ou le rapport pour une recherche de contenu, vous pouvez effectuer les étapes suivantes pour préparer le fichier CSV à une recherche de liste d'ID. Ce fichier CSV identifiera tous les éléments de la recherche de la liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="33de5-p109">Notez que vous pouvez utiliser un fichier CSV à partir d'une recherche qui inclut des sites SharePoint et des comptes OneDrive, mais vous pouvez sélectionner *uniquement* des éléments de boîte aux lettres pour une recherche de liste d'ID. Si vous sélectionnez un document dans SharePoint ou OneDrive, la validation du fichier CSV échoue lorsque vous créez une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="33de5-129">Ouvrez le fichier **results. csv** ou **éléments non indexés. csv** dans Excel.</span><span class="sxs-lookup"><span data-stu-id="33de5-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="33de5-p110">Insérez une nouvelle colonne et nommez-la **sélectionnée**. L'endroit où vous insérez la colonne n'a pas d'importance. Pour des raisons de commodité, envisagez de l'insérer à gauche de la première colonne.</span><span class="sxs-lookup"><span data-stu-id="33de5-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="33de5-p111">Dans la colonne **sélectionné** , tapez **Oui** dans la cellule correspondant à l'élément que vous souhaitez rechercher. Répétez cette étape pour chaque élément que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="33de5-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="33de5-p112">Lorsque vous ouvrez le fichier CSV dans Excel, le format de données de la colonne **ID de document** est modifié en **général**. Cela entraîne l'affichage de l'ID de document pour un élément en notation scientifique. Par exemple, l'ID de document «481037338205» est affiché sous la forme «4.81037 E + 11», vous devez effectuer les étapes suivantes pour modifier le format de données de la colonne d' **ID de document** sur **Number** afin de restaurer le format correct pour l'ID de document. Si vous ne le faites pas, la recherche de liste d'ID qui utilise le fichier CSV échouera.</span><span class="sxs-lookup"><span data-stu-id="33de5-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="33de5-139">Cliquez avec le bouton droit sur toute la colonne **ID de document** et sélectionnez mettre en **forme les cellules**.</span><span class="sxs-lookup"><span data-stu-id="33de5-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="33de5-140">Dans la zone **catégorie** , cliquez sur **nombre**.</span><span class="sxs-lookup"><span data-stu-id="33de5-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="33de5-p113">Modifiez le nombre de décimales en **0**, puis cliquez sur **OK** pour enregistrer vos modifications. Notez que les valeurs de la colonne ID de document sont remplacées par des numéros.</span><span class="sxs-lookup"><span data-stu-id="33de5-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="33de5-143">Voici un exemple de fichier CSV qui est prêt à être soumis pour une recherche de contenu de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Exemple de fichier CSV pour une recherche de contenu ciblée](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="33de5-p114">Enregistrez le fichier CSV ou utilisez la **fonction Enregistrer sous** pour enregistrer le fichier sous un autre nom. Dans les deux cas, veillez à enregistrer le fichier au format CSV.</span><span class="sxs-lookup"><span data-stu-id="33de5-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="33de5-147">Créer une recherche de liste d'ID</span><span class="sxs-lookup"><span data-stu-id="33de5-147">Create an ID list search</span></span>

<span data-ttu-id="33de5-148">L'étape suivante consiste à créer une nouvelle recherche de contenu de liste d'ID et à envoyer le fichier CSV que vous avez préparé à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="33de5-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="33de5-p115">Vous devez créer une recherche de liste d'ID au plus 2 jours après avoir exporté les résultats ou le rapport à partir d'une recherche de contenu. Si les résultats de la recherche ou le rapport exportés depuis plus de 2 jours, vous devez réexporter les résultats de la recherche ou le rapport pour générer des fichiers CSV mis à jour. Vous pouvez ensuite préparer l'un des fichiers CSV mis à jour et l'utiliser pour créer une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="33de5-152">Dans le centre &amp; de sécurité conformité, accédez à recherche de \> **contenu**d' \*\*enquête de recherche &amp; \*\* .</span><span class="sxs-lookup"><span data-stu-id="33de5-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="33de5-153">Sur la **page recherche** , cliquez sur la flèche en ![regard de](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) ajouter une icône **nouvelle recherche**, puis cliquez sur **Rechercher par ID**.</span><span class="sxs-lookup"><span data-stu-id="33de5-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Cliquez sur Rechercher par ID dans la liste déroulante nouvelle recherche.](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="33de5-155">Dans le menu démenu de **recherche par ID** , nommez la recherche (et éventuellement la Décrivez), puis cliquez sur **Parcourir** et sélectionnez le fichier CSV que vous avez préparé à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="33de5-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="33de5-p116">Office 365 tente de valider le fichier CSV. Si la validation échoue, un message d'erreur s'affiche pour vous aider à résoudre les erreurs de validation. Le fichier CSV doit être validé correctement pour créer une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="33de5-159">Une fois le fichier CSV correctement validé, cliquez sur **Rechercher** pour créer la recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="33de5-160">Voici un exemple des résultats de recherche estimés et de la requête générée pour une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Requête de recherche pour une recherche de contenu ciblé dans le volet d'informations](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="33de5-162">Notez que le nombre d'éléments estimés affichés dans les statistiques pour la recherche d'ID doit correspondre au nombre d'éléments que vous avez sélectionnés dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="33de5-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="33de5-163">PréVisualisez ou exportez les éléments renvoyés par la recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="33de5-p117">Si vous déplacez une boîte aux lettres après avoir créé une recherche de liste d'ID, la requête de la recherche ne renverra pas les éléments spécifiés. En effet, la propriété **DocumentID** pour les éléments de boîte aux lettres est modifiée lorsqu'une boîte aux lettres est déplacée. Dans l'instance rare lorsqu'une boîte aux lettres est déplacée après la création d'une recherche de liste d'ID, vous devez créer une nouvelle recherche de contenu (ou mettre à jour les résultats de recherche pour la recherche de contenu existante), puis exporter les résultats de la recherche ou le rapport pour générer des fichiers CSV mis à jour pouvant être utilisés  pour créer une recherche de liste d'ID.</span><span class="sxs-lookup"><span data-stu-id="33de5-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
