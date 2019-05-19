---
title: Exécuter le module de processus et charger des données dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Découvrez comment utiliser le centre de sécurité &amp; conformité Office 365 pour accéder à Office 365 Advanced eDiscovery et exécuter le module process pour un cas.  '
ms.openlocfilehash: 89a4be9bf56f35d9d9cbd88494bcae5a5a10fe7a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157016"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d9b7c-103">Exécuter le module de processus et charger des données dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d9b7c-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="d9b7c-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d9b7c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="d9b7c-106">Cette section décrit les fonctionnalités du module Advanced eDiscovery Process.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="d9b7c-107">En plus des données de fichier, les métadonnées telles que le type de fichier, l’extension, l’emplacement ou le chemin d’accès, la date et l’heure de création, l’auteur, le dépositaire et l’objet peuvent être chargées dans eDiscovery avancée et enregistrées pour chaque cas.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-107">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case.</span></span> <span data-ttu-id="d9b7c-108">Certaines métadonnées sont calculées par Advanced eDiscovery, par exemple, lors du chargement des fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-108">Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="d9b7c-109">Advanced eDiscovery fournit des valeurs de métadonnées système, telles que des regroupements proches ou des scores de pertinence.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-109">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores.</span></span> <span data-ttu-id="d9b7c-110">D’autres métadonnées, telles que les annotations de fichier, peuvent être ajoutées par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-110">Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="d9b7c-111">Processus en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="d9b7c-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="d9b7c-112">Les numéros de lot sont affectés à un fichier pendant le processus pour permettre le suivi des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-112">Batch numbers are assigned to a file during Process to allow the tracking of files.</span></span> <span data-ttu-id="d9b7c-113">Le numéro de lot permet également l’identification des lots de processus pour les options de retraitement.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-113">The batch number also enables identification of Process batches for reprocessing options.</span></span> <span data-ttu-id="d9b7c-114">Des filtres supplémentaires sont disponibles pour le filtrage par numéro de lot et par session.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-114">Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="d9b7c-115">Procédez comme suit pour exécuter le processus.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="d9b7c-116">[Ouvrez le centre de sécurité &amp; conformité Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="d9b7c-117">Accédez à la **découverte électronique** de l' \*\* &amp; enquête\*\* \> , puis cliquez sur **accéder à Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="d9b7c-118">Dans Advanced eDiscovery, sélectionnez la casse appropriée dans la page **incidents** affichés et cliquez sur **atteindre la casse**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="d9b7c-119">Dans **préparer** \> \*\*\*\* \> **le**processus de préparation, sélectionnez un conteneur dans la liste des conteneurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Cliquez sur traiter pour ajouter les résultats de la recherche à la demande de devis](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="d9b7c-121">Cliquez sur **Paramètres avancés...** si vous voulez ajouter le conteneur comme fichiers de départ ou sous forme de fichiers pré-balisés.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="d9b7c-122">Utilisez des fichiers de départ pour accélérer la formation des problèmes de faible richesse (généralement 2% ou moins).</span><span class="sxs-lookup"><span data-stu-id="d9b7c-122">Use seed files to accelerate training for issues with low richness (usually 2%, or less).</span></span> <span data-ttu-id="d9b7c-123">Pour les fichiers de départ, il est recommandé de sélectionner un grand nombre de fichiers de manière significative et de traiter environ 20-50 de dollars par problème (trop de fichiers de départ peuvent biaiser les résultats de la pertinence).</span><span class="sxs-lookup"><span data-stu-id="d9b7c-123">For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results).</span></span> <span data-ttu-id="d9b7c-124">Les fichiers de départ doivent être vérifiés par la même personne qui entraînera le problème.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-124">Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="d9b7c-125">Utilisez des fichiers pré-balisés pour automatiser la formation à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-125">Use pre-tagged files to automate Relevance training.</span></span> <span data-ttu-id="d9b7c-126">Vous devez marquer au moins 1 500 fichiers et conserver la proportion de fichiers pertinents pour les fichiers non pertinents le même que dans la collection ajoutée à la pertinence.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-126">You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance.</span></span> <span data-ttu-id="d9b7c-127">Ces fichiers doivent être balisés manuellement, et vous devez être sûr de la qualité du marquage.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-127">These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Capture d’écran de la page des paramètres avancés pour le traitement des fichiers de commandes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="d9b7c-129">Dans la section **Seed** :</span><span class="sxs-lookup"><span data-stu-id="d9b7c-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="d9b7c-130">Sélectionnez **marquer comme fichiers de départ** pour marquer le conteneur comme fichiers de départ.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-130">Choose **Mark as seed files** to mark the container as seed files.</span></span> <span data-ttu-id="d9b7c-131">Vous devez également choisir de les affecter par problème à partir de la liste déroulante **pour le problème** .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-131">You also need choose to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="d9b7c-132">Choisissez **pertinent** ou **non pertinent** dans la liste déroulante de **balises** .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-132">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="d9b7c-133">Une fois que vous avez défini les fichiers en tant que **Seed**, vous ne pouvez pas les marquer comme étant **préalablement balisés**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="d9b7c-134">Dans la section **fichiers pré-balisés** :</span><span class="sxs-lookup"><span data-stu-id="d9b7c-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="d9b7c-135">Sélectionnez **marquer comme fichiers pré-balisés** pour marquer le conteneur comme des fichiers pré-balisés.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-135">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files.</span></span> <span data-ttu-id="d9b7c-136">Vous devez également les affecter par problème à partir de la liste déroulante **pour le problème** .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-136">You also need to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="d9b7c-137">Choisissez **pertinent** ou **non pertinent** dans la liste déroulante de **balises** .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-137">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="d9b7c-138">Une fois que vous avez défini les fichiers comme étant **déjà balisés**, vous ne pouvez pas les marquer comme **Seed**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="d9b7c-139">Dans la section **étiquetage des courriers électroniques** .</span><span class="sxs-lookup"><span data-stu-id="d9b7c-139">In the **Email tagging** section.</span></span> <span data-ttu-id="d9b7c-140">définir la partie d’un message électronique traité devant être marquée comme amorce ou pré-balisage.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-140">set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="d9b7c-141">Pour commencer, cliquez sur **traiter**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-141">To begin, click **Process**.</span></span> <span data-ttu-id="d9b7c-142">Une fois terminé, les résultats du processus sont affichés.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-142">When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="d9b7c-143">Module Si vous devez attribuer des sources de données à un dépositaire spécifique, vous pouvez ajouter et modifier les noms des dépositaires dans les \*\*\*\* \> **dépositaires** \> pour **gérer** et attribuer des dépositaires à **attribuer**.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="d9b7c-144">Si vous ajoutez au cas, vous pouvez de nouveau traiter.</span><span class="sxs-lookup"><span data-stu-id="d9b7c-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9b7c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9b7c-145">See also</span></span>

[<span data-ttu-id="d9b7c-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d9b7c-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d9b7c-147">Affichage des résultats de module de processus</span><span class="sxs-lookup"><span data-stu-id="d9b7c-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

