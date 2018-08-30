---
title: Exécuter le module de processus et charger des données dans Office 365 avancée de découverte électronique
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Découvrez comment utiliser le Office 365 Security &amp; centre de conformité pour accéder à Office 365 avancée de découverte électronique et exécuter le module de processus pour un cas.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528113"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c0582-103">Exécuter le module de processus et charger des données dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="c0582-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="c0582-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="c0582-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="c0582-106">Cette section décrit les fonctionnalités du module processus eDiscovery avancées.</span><span class="sxs-lookup"><span data-stu-id="c0582-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="c0582-p102">En plus des données de fichiers, des métadonnées telles que le type de fichier, extension, emplacement ou chemin d’accès, date de création et heure, auteur, dépositaire et subject, peuvent être chargée dans avancée eDiscovery et enregistré pour chaque cas. Certaines métadonnées sont calculée en découverte avancée, par exemple, lors du chargement de fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="c0582-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="c0582-p103">Découverte avancée fournit système des valeurs de métadonnées, telles que les regroupements en double ou les résultats de la pertinence. Autres métadonnées, telles que des annotations de fichier, peuvent être ajoutée par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c0582-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="c0582-111">Processus en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="c0582-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="c0582-p104">Numéros de lot sont affectés à un fichier au cours du processus permettant d’assurer le suivi des fichiers. Le numéro de lot permet également d’identification de traitement par lots d’options retraitement. Filtres supplémentaires sont disponibles pour le filtrage des sessions et le numéro de lot.</span><span class="sxs-lookup"><span data-stu-id="c0582-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="c0582-115">Effectuez les étapes suivantes pour exécuter la procédure.</span><span class="sxs-lookup"><span data-stu-id="c0582-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="c0582-116">[Ouvrir la sécurité Office 365 &amp; centre de conformité](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="c0582-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="c0582-117">Accédez à **recherche &amp; enquête** \> **eDiscovery** , puis cliquez sur **Aller à la découverte électronique avancée**.</span><span class="sxs-lookup"><span data-stu-id="c0582-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="c0582-118">Découverte électronique avancée, sélectionnez le cas échéant dans la page en **cas** et cliquez sur **Atteindre la casse**.</span><span class="sxs-lookup"><span data-stu-id="c0582-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="c0582-119">Dans **Prepare** \> **processus** \> **le programme d’installation**, sélectionnez un conteneur de la liste des conteneurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="c0582-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Cliquez sur le processus pour ajouter les résultats de recherche à la casse](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="c0582-121">Si vous souhaitez ajouter le conteneur en tant que fichiers de départ ou en tant que fichiers balisés préalable, cliquez sur **paramètres... avancés** .</span><span class="sxs-lookup"><span data-stu-id="c0582-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="c0582-p105">Utiliser les fichiers d’amorçage pour accélérer la formation pour les problèmes avec la plus grande richesse faible (généralement 2 % ou moins). Pour les fichiers d’amorçage, il est recommandé que vous sélectionnez plusieurs fichiers inclut-elle pertinents et traiter sur 20 et 50 graines par problème (trop de fichiers d’amorçage pouvant incliner les résultats de la pertinence). Fichiers d’amorçage doivent être examinées par la personne qui sera former le problème.</span><span class="sxs-lookup"><span data-stu-id="c0582-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="c0582-p106">Fichiers balisés préalable permet d’automatiser la formation de pertinence. Vous devez ajouter une balise au moins 1 500 fichiers et conserver la proportion d’aux fichiers non pertinents identique à celle de la collection à ajouter à la pertinence. Ces fichiers doivent être marqués manuellement, et vous devez être assuré de la qualité de la liaison de.</span><span class="sxs-lookup"><span data-stu-id="c0582-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Capture d’écran d’avancée de page de paramètres de traitement par lot les fichiers](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="c0582-129">Dans la section **valeur de départ** :</span><span class="sxs-lookup"><span data-stu-id="c0582-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="c0582-p107">Choisissez **Marquer en tant que fichiers d’amorçage** pour marquer le conteneur en tant que fichiers d’amorçage. Vous devez également affecter par un problème dans la **problème** liste déroulante. À partir de la **balise de** liste déroulante, choisissez **pertinent** ou **non pertinents** .</span><span class="sxs-lookup"><span data-stu-id="c0582-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c0582-133">Une fois que vous définissez des fichiers en tant que **valeur de départ**, vous ne peut pas les marquer comme **préalable avec balise**.</span><span class="sxs-lookup"><span data-stu-id="c0582-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="c0582-134">Dans la section **fichiers balisés préalable** :</span><span class="sxs-lookup"><span data-stu-id="c0582-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="c0582-p108">Choisissez **Marquer en tant que fichiers préalable avec balise** pour marquer le conteneur en tant que fichiers préalable avec balise. Vous devez également affecter par un problème dans la **problème** liste déroulante. À partir de la **balise de** liste déroulante, choisissez **pertinent** ou **non pertinents** .</span><span class="sxs-lookup"><span data-stu-id="c0582-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c0582-138">Une fois que vous définissez fichiers **préalable avec balise**, vous ne peut pas les marquer comme **valeur de départ**.</span><span class="sxs-lookup"><span data-stu-id="c0582-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="c0582-p109">Dans la section **Marquer le courrier électronique** . ensemble de quelle partie d’un message électronique traité doivent être marquées comme semences ou préalable avec balise.</span><span class="sxs-lookup"><span data-stu-id="c0582-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="c0582-p110">Pour commencer, cliquez sur **le processus**. Une fois terminé, les résultats de processus sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c0582-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="c0582-143">(Facultatif) Si vous avez besoin affecter des sources de données à un dépositaire spécifique, vous pouvez ajouter ou modifier les noms de dépositaire dans **dépositaires** \> dépositaires **Gérer** et attribuer dans **dépositaires** \> **affecter**.</span><span class="sxs-lookup"><span data-stu-id="c0582-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="c0582-144">Si vous ajoutez à la casse, vous pouvez traiter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="c0582-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0582-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0582-145">See also</span></span>

[<span data-ttu-id="c0582-146">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="c0582-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c0582-147">Affichage des résultats de module de processus</span><span class="sxs-lookup"><span data-stu-id="c0582-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

