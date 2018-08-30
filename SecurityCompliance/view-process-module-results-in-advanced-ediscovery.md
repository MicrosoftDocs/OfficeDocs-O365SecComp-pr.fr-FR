---
title: Afficher les résultats du module dans Office 365 avancée de découverte électronique
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Découvrez comment trouver les résultats d’un Module de processus s’exécutent dans Office 365 avancée eDiscovery, y compris l’état de tâche et processus de synthèse.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527517"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="852f4-103">Afficher les résultats du module dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="852f4-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="852f4-104">Après la **préparation** \> **processus** est lancé, vous pouvez afficher la progression et les résultats.</span><span class="sxs-lookup"><span data-stu-id="852f4-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="852f4-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="852f4-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="852f4-107">État de la tâche de processus</span><span class="sxs-lookup"><span data-stu-id="852f4-107">Process task status</span></span>

<span data-ttu-id="852f4-108">Dans **Prepare** \> **processus** \> de **résultats**, la page affiche l’état actuel (si le processus est en cours d’exécution) ou le dernier état de tâche de statut de processus comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="852f4-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![État de tâche du module de processus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="852f4-110">Les tâches affichées peuvent varier en fonction des options de processus sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="852f4-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="852f4-111">**Inventaire**: découverte avancée parcourt tous les fichiers sélectionnés pour le processus et effectue la collecte de données de base.</span><span class="sxs-lookup"><span data-stu-id="852f4-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="852f4-112">**Calculer les signatures**: calcule les signatures numériques MD5.</span><span class="sxs-lookup"><span data-stu-id="852f4-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="852f4-p102">**Extraction de composés**: extraits internes ou qu’il contient des fichiers de manière récursive à partir des fichiers composés (par exemple, PST, ZIP, MSG). Fichiers extraits sont stockés dans le dossier de cas de la casse.</span><span class="sxs-lookup"><span data-stu-id="852f4-p102">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG). Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="852f4-115">**Base de données de synchronisation**: processus de base de données interne.</span><span class="sxs-lookup"><span data-stu-id="852f4-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="852f4-p103">**Copie du fichier**: fichiers de processus de copie. Cette tâche est toujours affichée, même si l’option de fichiers copie avancée est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="852f4-p103">**File copy**: Copies Process files. This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="852f4-p104">**Extraction de texte**: lorsque des fichiers natives, eDiscovery avancée extrait le texte de ces fichiers à l’aide de DTSearch. Le texte extrait de ces fichiers est stocké en tant que fichiers texte dans le dossier de cas.</span><span class="sxs-lookup"><span data-stu-id="852f4-p104">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch. The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="852f4-120">**Mise à jour des métadonnées**: traite des métadonnées chargées.</span><span class="sxs-lookup"><span data-stu-id="852f4-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="852f4-121">**Finalizing**: traitement interne qui finalise les données de chargée de dossiers (par exemple, identifier les fichiers d’erreur et la réussite).</span><span class="sxs-lookup"><span data-stu-id="852f4-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="852f4-p105">État de la tâche : affiché après la fin d’une tâche. Lors de l’exécutant des tâches, la durée d’exécution s’affiche.</span><span class="sxs-lookup"><span data-stu-id="852f4-p105">Task status: Displayed after task completion. While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="852f4-124">Les tâches achevées peuvent également inclure les totaux des terminé le traitement des fichiers ou avec des erreurs.</span><span class="sxs-lookup"><span data-stu-id="852f4-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="852f4-p106">« Annuler » fournit une option de restauration pour arrêter l’exécution des processus et puis restaurer le remplissage de données précédent ou l’enregistrée des données traitées. Restauration efface les données traitées. Si vous ne souhaitez pas les données traitées perte option Sélectionner la « Annuler » dans cette fenêtre pour choisir de ne pas annuler (par exemple, vous souhaitez recharger ces fichiers).</span><span class="sxs-lookup"><span data-stu-id="852f4-p106">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data. Rollback clears all processed data. If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="852f4-128">Résumé du processus</span><span class="sxs-lookup"><span data-stu-id="852f4-128">Process summary</span></span>

<span data-ttu-id="852f4-129">Dans Prepare \> processus \> résultats \> processus synthèse, une répartition des résultats fichier chargé est affichée en fonction des résultats de traitement et des erreurs de fichier réussie.</span><span class="sxs-lookup"><span data-stu-id="852f4-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="852f4-130">Les volets de présentent un affichage graphique des statistiques du fichier importé, comme suit :</span><span class="sxs-lookup"><span data-stu-id="852f4-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="852f4-131">**Processus de synthèse s’accumulent**d : tous les fichiers dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="852f4-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="852f4-132">**Procédure de résumé**: les fichiers chargement à partir de la dernière session ou action.</span><span class="sxs-lookup"><span data-stu-id="852f4-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="852f4-133">**Dernière familles**: informations dans le cas (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="852f4-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="852f4-134">Si les fichiers **d’amorçage** ont été ajoutés, le nombre de fichiers d’amorçage est répertorié par le problème a été définie pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="852f4-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="852f4-135">Si le marquage des fichiers **d’amorçage** a échoué, qui est également observé.</span><span class="sxs-lookup"><span data-stu-id="852f4-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="852f4-136">Si les fichiers **balisés préalables** ont été ajoutés, le nombre de fichiers avec des balises est répertorié par problème qui a été défini pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="852f4-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="852f4-137">Si le marquage des fichiers **balisés préalable** a échoué, qui est également observé.</span><span class="sxs-lookup"><span data-stu-id="852f4-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Résumé de module de processus](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="852f4-139">Résumé du processus cumulés et dernière graphiques</span><span class="sxs-lookup"><span data-stu-id="852f4-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="852f4-140">La barre de gauche inclut Source + fichiers extraits : c'est-à-dire tous les fichiers trouvés.</span><span class="sxs-lookup"><span data-stu-id="852f4-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="852f4-141">Le droit de la barre, traitées, inclut :</span><span class="sxs-lookup"><span data-stu-id="852f4-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="852f4-142">Fichiers avec des erreurs de chargement</span><span class="sxs-lookup"><span data-stu-id="852f4-142">Files with load errors</span></span>
    
- <span data-ttu-id="852f4-143">Fichiers chargés avec succès, qui peuvent inclure :</span><span class="sxs-lookup"><span data-stu-id="852f4-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="852f4-144">**Existant**: les fichiers qui ont été chargés avant et sont désormais chargés (notamment les doublons).</span><span class="sxs-lookup"><span data-stu-id="852f4-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="852f4-145">**Texte**: fichiers uniques avec du texte.</span><span class="sxs-lookup"><span data-stu-id="852f4-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="852f4-146">**Texte non**: vider les fichiers texte, des fichiers texte native vide, des fichiers non texte natives.</span><span class="sxs-lookup"><span data-stu-id="852f4-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="852f4-147">**Dupliquer**s: fichiers en double avec du texte.</span><span class="sxs-lookup"><span data-stu-id="852f4-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="852f4-148">Dernière traiter les erreurs</span><span class="sxs-lookup"><span data-stu-id="852f4-148">Last process errors</span></span>

<span data-ttu-id="852f4-149">Dans Prepare \> processus \> résultats \> dernier processus, les détails des erreurs dans la dernière session ou action effectuée s’affichent.</span><span class="sxs-lookup"><span data-stu-id="852f4-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Erreurs de module de processus](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="852f4-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852f4-151">See also</span></span>

[<span data-ttu-id="852f4-152">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="852f4-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="852f4-153">Le module de processus en cours d’exécution et de chargement des données</span><span class="sxs-lookup"><span data-stu-id="852f4-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

