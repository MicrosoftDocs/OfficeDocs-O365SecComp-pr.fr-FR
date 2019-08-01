---
title: Correction d’erreur lors du traitement des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5168196dcac8a2cb3809f43fabb470c0f64cd0f7
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048139"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="cd22e-102">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="cd22e-102">Error remediation when processing data</span></span>

<span data-ttu-id="cd22e-103">La correction des erreurs permet aux administrateurs eDiscovery de rectifier les problèmes de données qui empêchent la découverte électronique avancée de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="cd22e-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="cd22e-104">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car les fichiers sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="cd22e-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="cd22e-105">À l’aide de la correction des erreurs, les administrateurs eDiscovery peuvent télécharger des fichiers avec de telles erreurs, supprimer la protection par mot de passe, puis télécharger les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="cd22e-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="cd22e-106">Utilisez le flux de travail suivant pour corriger les fichiers avec des erreurs dans les cas avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="cd22e-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="cd22e-107">Créer une session d’erreur de correction pour corriger les fichiers avec des erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="cd22e-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="cd22e-108">Si l’Assistant de correction d’erreur est fermé à tout moment au cours de la procédure suivante, vous pouvez revenir à la session d’erreur de correction à partir de l’onglet **traitement** en sélectionnant **erreur correction** dans le menu déroulant **vue** .</span><span class="sxs-lookup"><span data-stu-id="cd22e-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="cd22e-109">Sous l’onglet **traitement** dans un cas avancé eDiscovery, sélectionnez **Erreurs** dans le menu déroulant **affichage** .</span><span class="sxs-lookup"><span data-stu-id="cd22e-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="cd22e-110">Sélectionnez les erreurs que vous souhaitez corriger en cliquant sur la case d’option en regard du type d’erreur ou du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="cd22e-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="cd22e-111">Dans l’exemple suivant, nous effectuons la correction d’un fichier protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="cd22e-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="cd22e-112">Cliquez sur **nouvelle erreur de correction**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-112">Click **New error remediation**.</span></span>

    ![Correction des erreurs](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="cd22e-114">La session de correction d’erreur commence par une phase de préparation dans laquelle les fichiers contenant des erreurs sont copiés vers un emplacement de stockage Azure fourni par Microsoft afin que vous puissiez les télécharger sur votre ordinateur local pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="cd22e-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Préparation de la correction des erreurs](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="cd22e-116">Une fois la préparation terminée, cliquez sur **suivant: Télécharger les fichiers** pour continuer le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="cd22e-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Télécharger des fichiers](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="cd22e-118">Pour télécharger des fichiers, spécifiez le **chemin de destination pour le téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="cd22e-119">Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="cd22e-119">This is a path on your local computer where the file will be downloaded.</span></span>  <span data-ttu-id="cd22e-120">Le chemin d’accès par défaut,%USERPROFILE%\Downloads\errors, pointe vers le dossier downloads de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="cd22e-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="cd22e-121">Vous pouvez modifier ce chemin si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cd22e-121">You can change this path if necessary.</span></span> <span data-ttu-id="cd22e-122">Si vous le modifiez, nous vous recommandons d’utiliser un chemin d’accès local au lieu d’un chemin d’accès réseau distant pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="cd22e-122">If you do change it, we recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

6. <span data-ttu-id="cd22e-123">Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-123">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="cd22e-124">Démarrez une invite de commandes Windows, collez la commande, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-124">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="cd22e-125">Les fichiers sont téléchargés.</span><span class="sxs-lookup"><span data-stu-id="cd22e-125">The files are downloaded.</span></span>

    ![Préparation de la correction des erreurs](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="cd22e-127">Vous devez utiliser AzCopy v 8.1 pour utiliser la commande fournie sur la page Télécharger les **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="cd22e-127">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="cd22e-128">Vous devez également utiliser AzCopy v 8.1 pour télécharger les fichiers à l’étape 10 ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cd22e-128">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="cd22e-129">Pour installer cette version de AzCopy, consultez [la rubrique transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="cd22e-129">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="cd22e-130">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="cd22e-130">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="cd22e-131">Après avoir téléchargé les fichiers, vous pouvez les corriger à l’aide d’un outil approprié.</span><span class="sxs-lookup"><span data-stu-id="cd22e-131">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="cd22e-132">Pour les fichiers protégés par mot de passe, il existe plusieurs outils de craquage de mot de passe que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="cd22e-132">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="cd22e-133">Si vous connaissiez les mots de passe des fichiers, vous pouvez les ouvrir et supprimer la protection par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="cd22e-133">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="cd22e-134">Il est important de conserver la structure de répertoire et les noms de fichier des fichiers corrigés dans l’élément tact.</span><span class="sxs-lookup"><span data-stu-id="cd22e-134">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="cd22e-135">Toutes les conventions d’affectation de noms utilisées dans les fichiers et les dossiers téléchargés permettent d’associer à nouveau les fichiers remdiated à l’original.</span><span class="sxs-lookup"><span data-stu-id="cd22e-135">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="cd22e-136">À présent, revenez à Advanced eDiscovery et cliquez sur **suivant: upload files**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-136">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="cd22e-137">Cette opération passe à l’étape suivante, dans laquelle vous pouvez à présent télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd22e-137">This will move to the next step where you can now upload the files.</span></span>

    ![Charger des fichiers](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="cd22e-139">Spécifiez l’emplacement des fichiers corrigés dans la zone **de texte chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-139">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="cd22e-140">Collez la commande dans une invite de commande Windows et appuyez sur **entrée** pour charger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd22e-140">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="cd22e-142">Revenez à Advanced eDiscovery et cliquez sur **Next: process files**.</span><span class="sxs-lookup"><span data-stu-id="cd22e-142">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="cd22e-143">Une fois le traitement terminé.</span><span class="sxs-lookup"><span data-stu-id="cd22e-143">When processing is complete.</span></span>  <span data-ttu-id="cd22e-144">Vous pouvez revenir à l’ensemble de révision et voir le fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="cd22e-144">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="cd22e-145">Que se passe-t-il lorsque les fichiers sont convertis?</span><span class="sxs-lookup"><span data-stu-id="cd22e-145">What happens when files are remediated</span></span>

<span data-ttu-id="cd22e-146">Lorsque les fichiers résolus sont téléchargés, les métadonnées d’origine sont conservées, à l’exception des champs suivants:</span><span class="sxs-lookup"><span data-stu-id="cd22e-146">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="cd22e-147">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="cd22e-147">ExtractedTextSize</span></span>
- <span data-ttu-id="cd22e-148">HasText</span><span class="sxs-lookup"><span data-stu-id="cd22e-148">HasText</span></span>
- <span data-ttu-id="cd22e-149">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="cd22e-149">IsErrorRemediate</span></span>
- <span data-ttu-id="cd22e-150">LoadId</span><span class="sxs-lookup"><span data-stu-id="cd22e-150">LoadId</span></span>
- <span data-ttu-id="cd22e-151">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="cd22e-151">ProcessingErrorMessage</span></span>
- <span data-ttu-id="cd22e-152">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="cd22e-152">ProcessingStatus</span></span>
- <span data-ttu-id="cd22e-153">Texte</span><span class="sxs-lookup"><span data-stu-id="cd22e-153">Text</span></span>
- <span data-ttu-id="cd22e-154">WordCount</span><span class="sxs-lookup"><span data-stu-id="cd22e-154">WordCount</span></span>
- <span data-ttu-id="cd22e-155">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="cd22e-155">WorkingsetId</span></span>

<span data-ttu-id="cd22e-156">Pour obtenir une définition de tous les champs de métadonnées de document dans Advanced eDiscovery, consultez la rubrique [document Metadata Fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="cd22e-156">For a definition of all document metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
