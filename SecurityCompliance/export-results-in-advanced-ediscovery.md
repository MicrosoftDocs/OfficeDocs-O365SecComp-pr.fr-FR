---
title: Exporter les résultats dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Découvrez comment définir les options d’exportation des résultats à partir d’Office 365 avancée eDiscovery, y compris la procédure permettant de spécifier des paramètres pour un lot d’exportation. '
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528694"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c3a65-103">Exporter les résultats dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="c3a65-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c3a65-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="c3a65-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c3a65-106">Cette rubrique décrit les options de configuration d’exportation avancées eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="c3a65-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="c3a65-107">**Dans cette rubrique :**</span><span class="sxs-lookup"><span data-stu-id="c3a65-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="c3a65-108">Définition des sessions et exporter les lots</span><span class="sxs-lookup"><span data-stu-id="c3a65-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="c3a65-109">Exportations incrémentielles et supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c3a65-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="c3a65-110">Définir les paramètres d’exportation de lot</span><span class="sxs-lookup"><span data-stu-id="c3a65-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="c3a65-111">Exporter des fichiers de sortie de rapport</span><span class="sxs-lookup"><span data-stu-id="c3a65-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="c3a65-112">Définition des sessions et exporter les lots</span><span class="sxs-lookup"><span data-stu-id="c3a65-112">Defining export batches and sessions</span></span>
<span data-ttu-id="c3a65-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="c3a65-113"></span></span>

<span data-ttu-id="c3a65-p102">Un lot d’exportation permet de traitement de l’exportation à l’aide d’un ensemble de paramètres définis. EDiscovery avancée vous permet de vous permet de définir des lots pour personnaliser chaque exportation.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="c3a65-p103">Les paramètres sont définis par lot d’exportation. Un lot appelé « Exporter par lots 01 » est créé par défaut pour le premier lot d’un cas. Vous pouvez également modifier le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="c3a65-119">Une session de l’exportation est l’exécution de la découverte avancée exportation au sein d’un lot d’exportation.</span><span class="sxs-lookup"><span data-stu-id="c3a65-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="c3a65-120">Exportations incrémentielles et supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c3a65-120">Incremental and additional exports</span></span>
<span data-ttu-id="c3a65-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="c3a65-121"></span></span>

<span data-ttu-id="c3a65-p104">Vous pouvez exécuter plusieurs sessions d’exportation au sein d’un lot d’exportation, pour garantir des résultats cohérents selon le même modèle d’exportation et les paramètres. Pour chaque session au sein d’un lot, vous pouvez exporter analytique nouvellement traitement des données d’incidents et traiter chaque « incrémentielle ».</span><span class="sxs-lookup"><span data-stu-id="c3a65-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="c3a65-p105">Afin d’exporter à l’aide d’un ensemble de paramètres différent, vous devez d’abord créer un nouveau lot. La première session dans le nouveau lot produira des résultats pour les fichiers traités jusque-là, dans le cas ou non ces fichiers ont été importés et traités sur une ou plusieurs importations. Chaque lot recalcule les tableaux croisés dynamiques, similarité, inclusives, etc.. Sessions utilisent les paramètres définis pour le lot et ne pas recalculer des tableaux croisés dynamiques, similarité, inclusives, etc., pour l’exécution de chaque session.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="c3a65-p106">Par exemple, supposons un cas a été importé et ses données analysées. Afin de récupérer la proximité des doublons et messagerie Threading des résultats pour les données incrémentielles, cliquez sur **créer exporter la session** dans le même lot qui a été utilisé précédemment pour exporter des données.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="c3a65-129">Définir les paramètres d’exportation de lot</span><span class="sxs-lookup"><span data-stu-id="c3a65-129">Set up batch export parameters</span></span>
<span data-ttu-id="c3a65-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="c3a65-130"></span></span>

<span data-ttu-id="c3a65-p107">L’outil d’exportation eDiscovery est utilisée pour exporter les résultats de la recherche de découverte avancée sur votre ordinateur local. Pour augmenter le débit de transfert de données et accélérer le processus d’exportation, vous pouvez configurer un paramètre de Registre Windows sur l’ordinateur qui vous permet d’exporter les résultats de recherche. Si vous souhaitez augmenter la vitesse de téléchargement, configurer les paramètres de Registre avant de configurer les paramètres d’exportation. Pour plus d’informations, voir [augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span><span class="sxs-lookup"><span data-stu-id="c3a65-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="c3a65-135">Dans découverte avancée, sélectionnez un cas, cliquez sur **Exporter** \> **le programme d’installation**.</span><span class="sxs-lookup"><span data-stu-id="c3a65-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
  - <span data-ttu-id="c3a65-136">Dans la liste **Exporter le lot** , sélectionnez le nom ou exporter les résultats dans un lot d’exportation 01, (la feuille par défaut).</span><span class="sxs-lookup"><span data-stu-id="c3a65-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="c3a65-p108">Pour exporter les résultats pour les nouveaux fichiers ajoutés à un cas existant, continuez avec votre lot en cours. Pour créer une session dans le lot, sélectionnez le même numéro de traitement par lots et cliquez sur **créer exporter la session** , vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="c3a65-p109">Pour exporter vers un nouveau lot, cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)et entrez un nouveau nom dans **nom de la feuille** (ou acceptez celui par défaut) et une description dans la **description de lot**. Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p109">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="c3a65-141">Pour modifier un nom ou une description, sélectionnez le nom de **l’exportation de lot**, cliquez sur **Modifier** ![icône Modifier](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), puis modifiez les champs.</span><span class="sxs-lookup"><span data-stu-id="c3a65-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c3a65-p110">Après avoir exécuté les sessions pour un lot d’exportation, ils ne peuvent pas être supprimés. En outre, les seuls certains paramètres peuvent être modifiés une fois que la première session est exécutée.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="c3a65-144">Pour créer un lot d’exportation en double, choisissez le **lot d’exportation en double**![créer une icône de lot d’exportation en double](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) et entrez un nom et une description pour le lot en double dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="c3a65-144">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="c3a65-145">Pour supprimer un lot d’exportation, cliquez sur **Supprimer**![supprimer une icône d’exportation de lot](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="c3a65-145">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="c3a65-146">Pour afficher l’historique d’un lot, cliquez sur **historique de lot**![icône historique d’affichage](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="c3a65-146">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="c3a65-147">Sous **remplissage**, sélectionnez **inclure uniquement les fichiers au-dessus note coupure** et/ou de **lot d’exportation affiner** si vous souhaitez ajuster les paramètres de votre lot d’exportation.</span><span class="sxs-lookup"><span data-stu-id="c3a65-147">Under **Population**,Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="c3a65-p111">Si vous sélectionnez **inclure uniquement les fichiers au-dessus note coupure**, le **problème** est activé. Si le score de pertinence du fichier est supérieure au score de limite pour le problème sélectionné, le fichier sera exporté, sauf si elle est exclu par le filtre « pour révision ».</span><span class="sxs-lookup"><span data-stu-id="c3a65-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
<span data-ttu-id="c3a65-p112">Si vous sélectionnez **lot d’exportation affiner**, la **déduplication** et filtrer par « Pour révision » champ cases d’option sont activés. Si vous choisissez **la déduplication**, puis les fichiers en double seront filtrés en fonction de la stratégie définie [cas niveau (valeur par défaut) : à partir de chaque ensemble de fichiers en double dans le cas d’entier, un seul fichier sera déduplication duped. Niveau dépositaire : à partir de chaque ensemble de fichiers en double de la même dépositaire, un seul fichier sera déduplication duped.] La sortie d’exportation contient un enregistrement de tous les fichiers en double. Si vous choisissez champ **Filter by « pour passer en revue les'** , sélectionnez **Modifier sous métadonnées** pour entrer vos paramètres de champ **« pour révision »** . Sélectionnez **inclure les fichiers d’entrée** à inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver ce paramètre pour accélérer le processus d’exportation. Notez que les fichiers natifs seront exportés dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="c3a65-157">Sous **métadonnées**, sélectionnez parmi les options suivantes dans la liste **Exporter le modèle** (une seule fois par session).</span><span class="sxs-lookup"><span data-stu-id="c3a65-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="c3a65-p113">**Standard**: ensemble de base des éléments de données, les métadonnées et les propriétés. Utilisez cette option lorsque importer des données a déjà été traitées dans découverte avancée et d’exporter des données sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d’exportation sont créés et remplis.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="c3a65-p114">**Tous les**: ensemble de toutes les données de traitement, ainsi que les scores d’analyser et de la pertinence de métadonnées standard. Ce modèle est requis lors de la découverte électronique avancée effectue le traitement et des données de fichier sont téléchargées vers un système externe pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="c3a65-163">**Problèmes**: sélectionnez **Tous les problèmes** ou un problème spécifique que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="c3a65-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="c3a65-164">Sous **Destination**:</span><span class="sxs-lookup"><span data-stu-id="c3a65-164">Under **Destination**:</span></span>
    
  - <span data-ttu-id="c3a65-165">**Télécharger sur l’ordinateur local**</span><span class="sxs-lookup"><span data-stu-id="c3a65-165">**Download to local machine**</span></span>
    
  - <span data-ttu-id="c3a65-166">**Exporter vers définies par l’utilisateur de blob Azure**: Si cette option est activée, vous pouvez spécifier un jeton d’URL et les associations de conteneur.</span><span class="sxs-lookup"><span data-stu-id="c3a65-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c3a65-p115">Une fois qu’un package d’exportation est stocké dans blob Azure définis par l’utilisateur, les données ne sont plus gérées par eDiscovery avancée ; Il est géré par l’objet blob Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur l’objet blob Azure.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="c3a65-169">**Jeton de session exportation futurs SAS enregistrer**: s’il est activé, le jeton SAS sera chiffré dans la base de données interne de découverte électronique avancées pour une utilisation future.</span><span class="sxs-lookup"><span data-stu-id="c3a65-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c3a65-p116">Actuellement, le jeton SAS expire après un mois. Si vous essayez de télécharger après plus d’un mois, que vous devez annuler la dernière session, puis l’exporter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="c3a65-172">Cliquez sur **Modifier** pour définir le » pour passer en revue les « paramètres de champ.</span><span class="sxs-lookup"><span data-stu-id="c3a65-172">Click **Modify** to set the "for review' field settings.</span></span> 
    
> ![Configurer pour passer en revue les paramètres de champ pour un lot d’exportation](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> <span data-ttu-id="c3a65-174">Dans **les messages électroniques** , sélectionnez les messages électroniques que vous souhaitez exporter :</span><span class="sxs-lookup"><span data-stu-id="c3a65-174">In **Emails** select the emails you want to export:</span></span> 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> <span data-ttu-id="c3a65-175">Dans les **Documents** , sélectionnez les documents que vous souhaitez exporter :</span><span class="sxs-lookup"><span data-stu-id="c3a65-175">In **Documents** select the documents you want to export:</span></span> 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> <span data-ttu-id="c3a65-176">Dans les **pièces jointes** , sélectionnez les pièces jointes que vous souhaitez exporter</span><span class="sxs-lookup"><span data-stu-id="c3a65-176">In **Attachments** select the attachments you want to export</span></span> 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> <span data-ttu-id="c3a65-p117">Dans **divers** , vous pouvez choisir pour **traiter les pièces jointes en tant que documents**, **traiter les messages électroniques en tant que documents**ou **développer pour inclure des fichiers de votre famille**. Lorsque vous choisissez **développer pour inclure des fichiers de votre famille**, pour chaque fichier est marqué pour révision, tous les fichiers de la même famille également signalées.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p117">In **Micellaneous** you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
    Choose **Save** to save the settings. 
    
7. <span data-ttu-id="c3a65-179">Une fois que vous spécifiez les paramètres d’exportation, pour démarrer le traitement d’exportation, cliquez sur **créer exporter la session**.</span><span class="sxs-lookup"><span data-stu-id="c3a65-179">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="c3a65-p118">Pendant l’exportation, l’état est affiché dans **l’état de la tâche**. Les résultats sont affichés dans **l’exportation de synthèse**.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p118">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
8. <span data-ttu-id="c3a65-182">Dans la fenêtre **téléchargement de fichiers** , cliquez sur **Copier dans le Presse-papiers** pour copier la clé d’exportation.</span><span class="sxs-lookup"><span data-stu-id="c3a65-182">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![Télécharger des fichiers](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. <span data-ttu-id="c3a65-184">Cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c3a65-184">Click **Close**.</span></span> 
    
    <span data-ttu-id="c3a65-185">L’outil d’exportation de découverte est démarré.</span><span class="sxs-lookup"><span data-stu-id="c3a65-185">The eDiscovery Export Tool is started.</span></span>
    
    ![Outil d’exportation de la découverte électronique](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. <span data-ttu-id="c3a65-187">Dans l' **outil d’exportation de découverte électronique**:</span><span class="sxs-lookup"><span data-stu-id="c3a65-187">In the **eDiscovery Export Tool**:</span></span>
    
1. <span data-ttu-id="c3a65-188">**Collez la Signature accès partagé qui sera utilisé pour se connecter à la source**, collez dans la clé d’exportation qui youcopied dans le Presse-papiers à l’étape 7.</span><span class="sxs-lookup"><span data-stu-id="c3a65-188">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
2. <span data-ttu-id="c3a65-189">Cliquez sur **Parcourir** pour sélectionner l’emplacement cible pour le stockage des fichiers d’exportation téléchargé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c3a65-189">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
11. <span data-ttu-id="c3a65-p119">Cliquez sur **Démarrer**. Les fichiers d’exportation sont téléchargés sur l’ordinateur local. Si vous avez choisi **d’Exporter vers blob Azure de défini par l’utilisateur** à l’étape 4, la session est exportée vers une destination d’URL de stockage Blob de votre choix.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p119">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span> 
    
<span data-ttu-id="c3a65-192">Pour une description complète des champs dans le rapport d’exportation, voir [exporter des champs du rapport](export-report-fields-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="c3a65-192">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="c3a65-193">Exporter des fichiers de sortie de rapport</span><span class="sxs-lookup"><span data-stu-id="c3a65-193">Export report output files</span></span>
<span data-ttu-id="c3a65-194"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="c3a65-194"></span></span>

<span data-ttu-id="c3a65-195">Le tableau suivant répertorie les fichiers de sortie qui sont générées lorsque vous exécutez un lot d’exportation.</span><span class="sxs-lookup"><span data-stu-id="c3a65-195">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="c3a65-196">**Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="c3a65-196">**File name**</span></span>|<span data-ttu-id="c3a65-197">**Type de fichier**</span><span class="sxs-lookup"><span data-stu-id="c3a65-197">**File type**</span></span>|<span data-ttu-id="c3a65-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3a65-198">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3a65-199">Résumé de l’exportation</span><span class="sxs-lookup"><span data-stu-id="c3a65-199">Export summary</span></span>  <br/> |<span data-ttu-id="c3a65-200">CSV</span><span class="sxs-lookup"><span data-stu-id="c3a65-200">csv</span></span>  <br/> |<span data-ttu-id="c3a65-201">Un fichier journal généré par l’outil d’exportation de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="c3a65-201">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="c3a65-202">Suivi</span><span class="sxs-lookup"><span data-stu-id="c3a65-202">Trace</span></span>  <br/> |<span data-ttu-id="c3a65-203">txt</span><span class="sxs-lookup"><span data-stu-id="c3a65-203">txt</span></span>  <br/> |<span data-ttu-id="c3a65-204">Un fichier journal généré par l’outil d’exportation de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="c3a65-204">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="c3a65-205">Fichiers texte extrait</span><span class="sxs-lookup"><span data-stu-id="c3a65-205">Extracted text files</span></span>  <br/> |<span data-ttu-id="c3a65-206">Dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="c3a65-206">File folder</span></span>  <br/> |<span data-ttu-id="c3a65-207">Dossier qui contient les fichiers texte extrait les fichiers exportés.</span><span class="sxs-lookup"><span data-stu-id="c3a65-207">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="c3a65-208">Entrée ou fichiers natifs</span><span class="sxs-lookup"><span data-stu-id="c3a65-208">Input or native files</span></span>  <br/> |<span data-ttu-id="c3a65-209">Dossier de fichiers</span><span class="sxs-lookup"><span data-stu-id="c3a65-209">File folder</span></span>  <br/> |<span data-ttu-id="c3a65-210">Dossier qui contient les fichiers natifs et d’entrée des fichiers exportés.</span><span class="sxs-lookup"><span data-stu-id="c3a65-210">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="c3a65-211">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="c3a65-211">Export list</span></span>  <br/> |<span data-ttu-id="c3a65-212">xlsx</span><span class="sxs-lookup"><span data-stu-id="c3a65-212">xlsx</span></span>  <br/> |<span data-ttu-id="c3a65-p120">Métadonnées de fichiers exportés au format xlsx. Champs dans les fichiers sont appliquent aux modèles utilisateur sélectionne à exporter. Si nécessaire, plusieurs fichiers sont créés, chacun contient des lignes de 100 à 150 Ko. Si une certaine valeur contient plus de caractères qu’une cellule Excel peut contenir (actuellement la limite est de 32 767 caractères), puis la valeur est supprimée à la longueur maximale autorisée. Si une valeur est tronquée, couleur d’arrière-plan de la cellule est rouge pour indiquer à l’utilisateur. » Participants e-mail » sont un exemple d’un champ qui dépasse la limite de longueur, si le message électronique a été envoyé à une distribution de grande taille. Pour plus d’informations sur les champs de sortie, voir [exporter des champs du rapport](export-report-fields-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a65-p120">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="c3a65-219">Charger le fichier</span><span class="sxs-lookup"><span data-stu-id="c3a65-219">Load file</span></span>  <br/> |<span data-ttu-id="c3a65-220">CSV</span><span class="sxs-lookup"><span data-stu-id="c3a65-220">csv</span></span>  <br/> |<span data-ttu-id="c3a65-p121">Métadonnées de fichiers exportés au format csv pour le chargement dans une autre application. Champs dans les fichiers sont appliquent aux modèles utilisateur sélectionne à exporter.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p121">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="c3a65-223">Indicateur de réussite</span><span class="sxs-lookup"><span data-stu-id="c3a65-223">Success indicator</span></span>  <br/> |<span data-ttu-id="c3a65-224">txt</span><span class="sxs-lookup"><span data-stu-id="c3a65-224">txt</span></span>  <br/> |<span data-ttu-id="c3a65-p122">Ne créés lors de l’exportation pour un 3ème partie blob Azure. Si l’exportation a abouti, le fichier sera créé. En cas d’échec, complet ou partiel réussite le fichier ne sera pas créé. Fichier sera créé dans le dossier racine, permettant de suivi automatique sur les différents statuts de lots/sessions d’exportation. Il s’agit d’un fichier vide. Son nom est : TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span><span class="sxs-lookup"><span data-stu-id="c3a65-p122">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3a65-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3a65-231">See also</span></span>
<span data-ttu-id="c3a65-232"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="c3a65-232"></span></span>

[<span data-ttu-id="c3a65-233">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="c3a65-233">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c3a65-234">Affichage de l’historique des commandes et l’exportation des résultats antérieurs</span><span class="sxs-lookup"><span data-stu-id="c3a65-234">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="c3a65-235">Programme d’installation rapide pour la découverte Office 365 avancée</span><span class="sxs-lookup"><span data-stu-id="c3a65-235">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="c3a65-236">Champs du rapport d’exportation</span><span class="sxs-lookup"><span data-stu-id="c3a65-236">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c3a65-237">Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365</span><span class="sxs-lookup"><span data-stu-id="c3a65-237">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

