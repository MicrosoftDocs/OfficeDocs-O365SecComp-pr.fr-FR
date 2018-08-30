---
title: Utiliser l’analyse Express dans Office 365 avancée de découverte électronique
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Découvrez comment exécuter le mode d’analyse Express d’eDiscovery Office 365 avancée
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527966"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="63091-103">Utiliser l’analyse Express dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="63091-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="63091-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="63091-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="63091-106">Vous pouvez utiliser **Express analyse** pour analyser rapidement un cas et exporter les résultats.</span><span class="sxs-lookup"><span data-stu-id="63091-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="63091-p102">Vous pouvez utiliser une analyse rapide pour calculer la proximité des doublons et les threads de messagerie et calculer des thèmes. Vous pouvez également définir certains paramètres de similarité de documents, des thèmes et des fichiers d’exportation dans les [Paramètres avancés pour l’analyse Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span><span class="sxs-lookup"><span data-stu-id="63091-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="63091-109">Exécuter l’analyse Express</span><span class="sxs-lookup"><span data-stu-id="63091-109">Run Express analysis</span></span>

1. <span data-ttu-id="63091-110">Dans l’onglet **analyse Express** (1), sélectionnez un conteneur pour activer la ** Express analyse ** (2) et les boutons **Paramètres avancés** .</span><span class="sxs-lookup"><span data-stu-id="63091-110">In the **Express analysis** (1) tab, select a container to enable the ** Express analysis ** (2), and **Advanced settings** buttons.</span></span> 
    
    ![Capture d’écran de la page analyse Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="63091-112">Sous l’onglet **paramètres d’analyse**:</span><span class="sxs-lookup"><span data-stu-id="63091-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="63091-p103">Vérifiez **calculer la proximité des doublons et threads de messagerie** si vous souhaitez exécuter l’analyse. Il est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="63091-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="63091-p104">Vérifiez les **Thèmes calculer** pour traiter tous les fichiers et leur attribuer des thèmes. Il est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="63091-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="63091-117">Sous **destination d’exportation**:</span><span class="sxs-lookup"><span data-stu-id="63091-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="63091-118">Vérifiez le **télécharger sur l’ordinateur local** à télécharger sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="63091-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="63091-119">Si vous l’activez **Exporter vers définies par l’utilisateur de blob Azure** vous pouvez également spécifier un jeton d’URL et les associations de conteneur.</span><span class="sxs-lookup"><span data-stu-id="63091-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="63091-p105">Une fois qu’un package d’exportation est stocké dans blob Azure définis par l’utilisateur, les données ne sont plus gérées par eDiscovery avancée. Il est géré par l’objet blob Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur l’objet blob Azure.</span><span class="sxs-lookup"><span data-stu-id="63091-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="63091-123">**Jeton de session exportation futurs SAS enregistrer**: s’il est activé, le jeton SAS sera chiffré dans la base de données interne de découverte électronique avancées pour une utilisation future.</span><span class="sxs-lookup"><span data-stu-id="63091-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="63091-p106">Actuellement, le jeton SAS expire après un mois. Si vous essayez de télécharger après plus d’un mois, que vous devez annuler la dernière session, puis l’exporter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="63091-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="63091-126">Pour démarrer l’analyse express avec par défaut les paramètres, choisissez **Express analyse**et affiche la page **état de la tâche**</span><span class="sxs-lookup"><span data-stu-id="63091-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="63091-127">Dans la page **état de la tâche** , vous pouvez développer les **processus**, **analyser** et **exporter des** onglets pour afficher plus d’informations sur l’exécution expresse.</span><span class="sxs-lookup"><span data-stu-id="63091-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Capture d’écran d’avancée eDiscovery Express analyse tâche page d’état](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="63091-129">Sélectionnez la page **Résumé de l’analyse de Express** pour répertorier des informations détaillées sur l’exécution.</span><span class="sxs-lookup"><span data-stu-id="63091-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="63091-p107">Au bas de la page **Résumé de l’analyse de Express** , sélectionnez **Télécharger la dernière session** pour télécharger le tp de fichiers analyse votre ordinateur local. Vous devez tout d’abord télécharger l’outil d’exportation eDiscovery et collez la clé d’exportation à l’outil d’exportation de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="63091-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="63091-132">Paramètres avancés pour l’analyse Express</span><span class="sxs-lookup"><span data-stu-id="63091-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="63091-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="63091-133"></span></span>

<span data-ttu-id="63091-134">Vous pouvez également définir des **Paramètres avancés** pour modifier les paramètres d’analyse par défaut Express.</span><span class="sxs-lookup"><span data-stu-id="63091-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="63091-135">Dans la section **analyse** :</span><span class="sxs-lookup"><span data-stu-id="63091-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="63091-136">Dans la **proximité des doublons et threads de messagerie**, entrez la valeur de **similarité de Document** , ou acceptez la valeur par défaut de 65 %.</span><span class="sxs-lookup"><span data-stu-id="63091-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="63091-p108">Le **nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="63091-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="63091-p109">Augmentation du nombre de thèmes affecte les performances, ainsi que la capacité d’un thème pour généraliser. Plus le nombre de thèmes, le plus granulaires, ils se trouvent. Par exemple, si un ensemble de 50 thèmes include un thème tels que « Basketball, rapide, pince, Lakers » ; 300 thèmes peuvent inclure des thèmes distincts : « Incite », « TONDEUSE », « Lakers ». Si vous n’avez aucune prise de conscience du thème « Basketball » et que vous utilisez cette fonctionnalité pour ECA, voir le thème « Basketball » peut être utile. Mais, si le traitement a un trop grand nombre de thèmes, vous visualiserez jamais le mot « Basketball » et peut ne pas savez que rapide et tondeuse est bonnes thèmes Basketball pour passer en revue, au lieu d’articles qui passent sur démarre et utilisés pour cheveux.</span><span class="sxs-lookup"><span data-stu-id="63091-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="63091-p110">Dans les **thèmes suggérés** choisissez **Modifier** pour nous transmettre vos suggestions de mots de thème pour contrôler le traitement des thèmes. Découverte avancée sera se concentrer sur ces mots suggérés et essayez de créer un ou plusieurs thèmes pertinents, en fonction des paramètres « Max nombre de thèmes ».</span><span class="sxs-lookup"><span data-stu-id="63091-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="63091-p111">Par exemple, si le mot suggéré est « computer », et vous avez spécifié « 2 » comme « nombre maximal de thèmes », eDiscovery avancée essaiera générer des thèmes de deux qui sont associées au mot « computer ». Les deux thèmes est « logiciel » et « matériel informatique », par exemple.</span><span class="sxs-lookup"><span data-stu-id="63091-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="63091-149">**Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** :</span><span class="sxs-lookup"><span data-stu-id="63091-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="63091-150">**Créer et appliquer le modèle**: calcule des thèmes par les modèles d’un segment des fichiers et puis distribue les fichiers entre eux.</span><span class="sxs-lookup"><span data-stu-id="63091-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="63091-p112">**Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers. Le processus d’appliquer de la division de fichiers s’effectue séparément à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="63091-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="63091-p113">**Appliquer modèle**: cette option ne s’affiche que si un modèle a été créé précédemment et n’est pas encore appliqué. Il divise les fichiers selon les thèmes.</span><span class="sxs-lookup"><span data-stu-id="63091-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="63091-155">Dans la section **Exporter** :</span><span class="sxs-lookup"><span data-stu-id="63091-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="63091-156">Dans le **lot sélectionnez Exporter**:</span><span class="sxs-lookup"><span data-stu-id="63091-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="63091-157">Dans la liste **Exporter le lot** , sélectionnez le nom ou exporter les résultats dans un lot d’exportation 01, (la feuille par défaut).</span><span class="sxs-lookup"><span data-stu-id="63091-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="63091-p114">Pour exporter les résultats pour les nouveaux fichiers ajoutés à un cas existant, continuez avec votre lot en cours. Pour créer une session dans le lot, sélectionnez le même numéro de traitement par lots et cliquez sur **créer exporter la session** , vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="63091-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="63091-p115">Pour exporter vers un nouveau lot, cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) et entrez un nouveau nom dans **nom de la feuille** (ou acceptez celui par défaut) et une description dans la **description de lot**. Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="63091-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="63091-162">Pour modifier un nom ou une description, sélectionnez le nom de **l’exportation de lot**, cliquez sur **Modifier** ![icône Modifier](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), puis modifiez les champs.</span><span class="sxs-lookup"><span data-stu-id="63091-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="63091-p116">Après avoir exécuté les sessions pour un lot d’exportation, ils ne peuvent pas être supprimés. En outre, les seuls certains paramètres peuvent être modifiés une fois que la première session est exécutée.</span><span class="sxs-lookup"><span data-stu-id="63091-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="63091-165">Pour créer un lot d’exportation en double, choisissez le **lot d’exportation en double**![créer une icône de lot d’exportation en double](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) et entrez un nom et une description pour le lot en double dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="63091-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="63091-166">Pour supprimer un lot d’exportation, cliquez sur **Supprimer**![supprimer une icône d’exportation de lot](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="63091-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="63091-167">Pour afficher l’historique d’un lot, cliquez sur **historique de lot**![icône historique d’affichage](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="63091-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="63091-p117">Sous Définir p **opulation :** sélectionnez **inclure uniquement les fichiers au-dessus note coupure** et/ou de **lot d’exportation affiner** si vous souhaitez ajuster les paramètres de votre lot d’exportation. Si vous sélectionnez **inclure uniquement les fichiers au-dessus note coupure**, le **problème** est activée, et si le score de pertinence du fichier est supérieure au score de limite pour le problème sélectionné, le fichier est exporté. Le fichier doit être exporté, sauf si elle est exclu par le ' filtre **pour révision** . Si vous sélectionnez **lot d’exportation affiner**, la **déduplication** et **Filter by « Pour passer en revue les » champ** cases d’option sont activées. Si vous choisissez **la déduplication**, puis fichiers doublons seront être filtrées mise en fonction de la stratégie définie : [cas niveau (valeur par défaut) : à partir de chaque ensemble de fichiers en double dans le cas d’entier, un seul fichier sera déduplication duped. Niveau dépositaire : à partir de chaque ensemble de fichiers en double de la même dépositaire, un seul fichier sera duped retrait. Un enregistrement de tous les fichiers en double est disponible dans la sortie de l’exportation. Si vous choisissez champ **Filter by « pour passer en revue les'** , sélectionnez **Modifier sous métadonnées** pour entrer vos paramètres de champ **« pour révision »**. Sélectionnez **inclure les fichiers d’entrée**à inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver cette option pour accélérer le processus d’exportation. Notez que les fichiers natifs seront exportés dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="63091-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="63091-179">Sous **définir métadonnées**, sélectionnez parmi les options suivantes dans la liste **Exporter le modèle** (une seule fois par session).</span><span class="sxs-lookup"><span data-stu-id="63091-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="63091-p118">**Standard**: ensemble de base des éléments de données, les métadonnées et les propriétés. Utilisez cette option lorsque importer des données a déjà été traitées dans découverte avancée et d’exporter des données sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d’exportation sont créés et remplis.</span><span class="sxs-lookup"><span data-stu-id="63091-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="63091-p119">**Tous les**: ensemble de toutes les données de traitement, ainsi que les scores d’analyser et de la pertinence de métadonnées standard. Ce modèle est requis lors de la découverte électronique avancée effectue le traitement et des données de fichier sont téléchargées vers un système externe pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="63091-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="63091-185">**Problèmes**: sélectionnez **Tous les problèmes** ou un problème spécifique que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="63091-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="63091-186">Cliquez sur **OK**pour enregistrer les paramètres avancés, **restauration par défaut** à utiliser les valeurs par défaut, ou **Annuler** pour annuler la configuration des paramètres avancés.</span><span class="sxs-lookup"><span data-stu-id="63091-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63091-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63091-187">See also</span></span>
<span data-ttu-id="63091-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="63091-188"></span></span>

[<span data-ttu-id="63091-189">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="63091-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

