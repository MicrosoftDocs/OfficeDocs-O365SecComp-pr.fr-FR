---
title: Exécuter le module Processus et charger des données dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Découvrez comment utiliser le centre de sécurité &amp; conformité Office 365 pour accéder à Office 365 Advanced eDiscovery et exécuter le module process pour un cas.  '
ms.openlocfilehash: 95c73c034ed2ffa1c45f9aacd8463c497a842859
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217604"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="f4f1a-103">Exécuter le module Processus et charger des données dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f4f1a-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="f4f1a-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="f4f1a-106">Cette section décrit les fonctionnalités du module Advanced eDiscovery Process.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="f4f1a-p102">En plus des données de fichier, les métadonnées telles que le type de fichier, l'extension, l'emplacement ou le chemin d'accès, la date et l'heure de création, l'auteur, le dépositaire et l'objet peuvent être chargées dans eDiscovery avancée et enregistrées pour chaque cas. Certaines métadonnées sont calculées par Advanced eDiscovery, par exemple, lors du chargement des fichiers natifs.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="f4f1a-p103">Advanced eDiscovery fournit des valeurs de métadonnées système, telles que des regroupements proches ou des scores de pertinence. D'autres métadonnées, telles que les annotations de fichier, peuvent être ajoutées par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="f4f1a-111">Processus en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="f4f1a-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="f4f1a-p104">Les numéros de lot sont affectés à un fichier pendant le processus pour permettre le suivi des fichiers. Le numéro de lot permet également l'identification des lots de processus pour les options de retraitement. Des filtres supplémentaires sont disponibles pour le filtrage par numéro de lot et par session.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="f4f1a-115">Procédez comme suit pour exécuter le processus.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="f4f1a-116">[Ouvrez le centre de sécurité &amp; conformité Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f1a-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="f4f1a-117">Accédez à la **découverte électronique** de l' \*\* &amp; enquête\*\* \> , puis cliquez sur **accéder à Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="f4f1a-118">Dans Advanced eDiscovery, sélectionnez la casse appropriée dans la page **incidents** affichés et cliquez sur **atteindre la casse**.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="f4f1a-119">Dans **préparer** \> \*\*\*\* \> **le**processus de préparation, sélectionnez un conteneur dans la liste des conteneurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Cliquez sur traiter pour ajouter les résultats de la recherche à la demande de devis](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="f4f1a-121">Cliquez sur **Paramètres avancés...** si vous voulez ajouter le conteneur comme fichiers de départ ou sous forme de fichiers pré-balisés.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="f4f1a-p105">Utilisez des fichiers de départ pour accélérer la formation des problèmes de faible richesse (généralement 2% ou moins). Pour les fichiers de départ, il est recommandé de sélectionner un grand nombre de fichiers de manière significative et de traiter environ 20-50 de dollars par problème (trop de fichiers de départ peuvent biaiser les résultats de la pertinence). Les fichiers de départ doivent être vérifiés par la même personne qui entraînera le problème.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="f4f1a-p106">Utilisez des fichiers pré-balisés pour automatiser la formation à la pertinence. Vous devez marquer au moins 1 500 fichiers et conserver la proportion de fichiers pertinents pour les fichiers non pertinents le même que dans la collection ajoutée à la pertinence. Ces fichiers doivent être balisés manuellement, et vous devez être sûr de la qualité du marquage.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Capture d'écran de la page des paramètres avancés pour le traitement des fichiers de commandes](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="f4f1a-129">Dans la section **Seed** :</span><span class="sxs-lookup"><span data-stu-id="f4f1a-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="f4f1a-p107">Sélectionnez **marquer comme fichiers de départ** pour marquer le conteneur comme fichiers de départ. Vous devez également choisir de les affecter par problème à partir de la liste déroulante **pour le problème** . Choisissez **pertinent** ou **non pertinent** dans la liste déroulante de **balises** .</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f4f1a-133">Une fois que vous avez défini les fichiers en tant que **Seed**, vous ne pouvez pas les marquer comme étant **préalablement balisés**.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="f4f1a-134">Dans la section **fichiers pré-balisés** :</span><span class="sxs-lookup"><span data-stu-id="f4f1a-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="f4f1a-p108">Sélectionnez **marquer comme fichiers pré-balisés** pour marquer le conteneur comme des fichiers pré-balisés. Vous devez également les affecter par problème à partir de la liste déroulante **pour le problème** . Choisissez **pertinent** ou **non pertinent** dans la liste déroulante de **balises** .</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f4f1a-138">Une fois que vous avez défini les fichiers comme étant **déjà balisés**, vous ne pouvez pas les marquer comme **Seed**.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="f4f1a-p109">Dans la section **étiquetage des courriers électroniques** . définir la partie d'un message électronique traité devant être marquée comme amorce ou pré-balisage.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="f4f1a-p110">Pour commencer, cliquez sur **traiter**. Une fois terminé, les résultats du processus sont affichés.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="f4f1a-143">Module Si vous devez attribuer des sources de données à un dépositaire spécifique, vous pouvez ajouter et modifier les noms des dépositaires dans les \*\*\*\* \> **dépositaires** \> pour **gérer** et attribuer des dépositaires à **attribuer**.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="f4f1a-144">Si vous ajoutez au cas, vous pouvez de nouveau traiter.</span><span class="sxs-lookup"><span data-stu-id="f4f1a-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4f1a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4f1a-145">See also</span></span>

[<span data-ttu-id="f4f1a-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f4f1a-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f4f1a-147">Affichage des résultats de module de processus</span><span class="sxs-lookup"><span data-stu-id="f4f1a-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

