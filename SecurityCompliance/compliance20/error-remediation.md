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
ms.openlocfilehash: c9c2660929037430535c9b612218563c51b1f056
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490791"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="f4a70-102">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="f4a70-102">Error remediation when processing data</span></span>

<span data-ttu-id="f4a70-103">La correction des erreurs permet aux administrateurs eDiscovery de rectifier les problèmes de données qui empêchent la découverte électronique avancée de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="f4a70-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="f4a70-104">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car les fichiers sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="f4a70-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="f4a70-105">À l’aide de la correction des erreurs, les administrateurs eDiscovery peuvent télécharger des fichiers avec de telles erreurs, supprimer la protection par mot de passe, puis télécharger les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="f4a70-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="f4a70-106">Utilisez le flux de travail suivant pour corriger les fichiers avec des erreurs dans les cas avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="f4a70-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="f4a70-107">Créer une session d’erreur de correction pour corriger les fichiers avec des erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="f4a70-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="f4a70-108">Si l’Assistant de correction d’erreur est fermé à tout moment au cours de la procédure suivante, vous pouvez revenir à la session d’erreur de correction à partir de l’onglet **traitement** en sélectionnant **erreur correction** dans le menu déroulant **vue** .</span><span class="sxs-lookup"><span data-stu-id="f4a70-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="f4a70-109">Sous l’onglet **traitement** dans un cas avancé eDiscovery, sélectionnez **Erreurs** dans le menu déroulant **affichage** .</span><span class="sxs-lookup"><span data-stu-id="f4a70-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="f4a70-110">Sélectionnez les erreurs que vous souhaitez corriger en cliquant sur la case d’option en regard du type d’erreur ou du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="f4a70-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="f4a70-111">Dans l’exemple suivant, nous effectuons la correction d’un fichier protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f4a70-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="f4a70-112">Cliquez sur **nouvelle erreur de correction**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-112">Click **New error remediation**.</span></span>

    ![Correction des erreurs](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="f4a70-114">La session de correction d’erreur commence par une phase de préparation dans laquelle les fichiers contenant des erreurs sont copiés vers un emplacement de stockage Azure fourni par Microsoft afin que vous puissiez les télécharger sur votre ordinateur local pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="f4a70-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Préparation de la correction des erreurs](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="f4a70-116">Une fois la préparation terminée, cliquez sur **suivant: Télécharger les fichiers** pour continuer le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f4a70-116">After the preparation is complete, click **Next: Download files** to proceed with download.</span></span>

    ![Télécharger des fichiers](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="f4a70-118">Pour télécharger des fichiers, spécifiez le **chemin de destination pour le téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="f4a70-119">Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="f4a70-119">This is a path on your local computer where the file is downloaded.</span></span>  <span data-ttu-id="f4a70-120">Le chemin d’accès par défaut,%USERPROFILE%\Downloads\errors, pointe vers le dossier downloads de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="f4a70-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="f4a70-121">Vous pouvez modifier ce chemin si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f4a70-121">You can change this path if necessary.</span></span> <span data-ttu-id="f4a70-122">Si vous le modifiez, nous vous recommandons d’utiliser un chemin d’accès local pour obtenir les meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="f4a70-122">If you do change it, we recommend that you use a local file path for the best performance.</span></span> <span data-ttu-id="f4a70-123">N’utilisez pas de chemin d’accès réseau distant.</span><span class="sxs-lookup"><span data-stu-id="f4a70-123">Don't use a remote network path.</span></span>

6. <span data-ttu-id="f4a70-124">Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-124">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="f4a70-125">Démarrez une invite de commandes Windows, collez la commande, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-125">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="f4a70-126">Les fichiers sont téléchargés.</span><span class="sxs-lookup"><span data-stu-id="f4a70-126">The files are downloaded.</span></span>

    ![Préparer la correction des erreurs](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="f4a70-128">Vous devez utiliser AzCopy v 8.1 pour utiliser la commande fournie sur la page Télécharger les **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="f4a70-128">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="f4a70-129">Vous devez également utiliser AzCopy v 8.1 pour télécharger les fichiers à l’étape 10 ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f4a70-129">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="f4a70-130">Pour installer cette version de AzCopy, consultez [la rubrique transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="f4a70-130">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="f4a70-131">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="f4a70-131">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="f4a70-132">Après avoir téléchargé les fichiers, vous pouvez les corriger à l’aide d’un outil approprié.</span><span class="sxs-lookup"><span data-stu-id="f4a70-132">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="f4a70-133">Pour les fichiers protégés par mot de passe, il existe plusieurs outils de craquage de mot de passe que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="f4a70-133">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="f4a70-134">Si vous connaissiez les mots de passe des fichiers, vous pouvez les ouvrir et supprimer la protection par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f4a70-134">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="f4a70-135">Il est important de conserver la structure de répertoire et les noms de fichier des fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="f4a70-135">It's important that you retain the directory structure and file names of the remediated files.</span></span> <span data-ttu-id="f4a70-136">Les noms de chemin d’accès des fichiers et dossiers téléchargés permettent d’associer les fichiers corrigés aux fichiers d’origine.</span><span class="sxs-lookup"><span data-stu-id="f4a70-136">The path names of the downloaded files and folders make it possible to associate the remediated files with the original files.</span></span>  <span data-ttu-id="f4a70-137">Si la structure du répertoire ou les noms de fichier sont modifiés, vous recevez l’erreur `Cannot apply Error Remediation to the current Workingset`suivante:.</span><span class="sxs-lookup"><span data-stu-id="f4a70-137">If the directory structure or file names are changed, you'll receive the following error: `Cannot apply Error Remediation to the current Workingset`.</span></span>

8. <span data-ttu-id="f4a70-138">À présent, revenez à Advanced eDiscovery et cliquez sur **suivant: upload files**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-138">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="f4a70-139">Cette opération passe à l’étape suivante, dans laquelle vous pouvez à présent télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f4a70-139">This will move to the next step where you can now upload the files.</span></span>

    ![Charger des fichiers](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="f4a70-141">Spécifiez l’emplacement des fichiers corrigés dans la zone **de texte chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-141">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="f4a70-142">Collez la commande dans une invite de commande Windows et appuyez sur **entrée** pour charger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f4a70-142">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="f4a70-144">Revenez à Advanced eDiscovery et cliquez sur **Next: process files**.</span><span class="sxs-lookup"><span data-stu-id="f4a70-144">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="f4a70-145">Une fois le traitement terminé.</span><span class="sxs-lookup"><span data-stu-id="f4a70-145">When processing is complete.</span></span> <span data-ttu-id="f4a70-146">Vous pouvez revenir à l’ensemble de révision et voir le fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="f4a70-146">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="f4a70-147">Que se passe-t-il lorsque les fichiers sont convertis?</span><span class="sxs-lookup"><span data-stu-id="f4a70-147">What happens when files are remediated</span></span>

<span data-ttu-id="f4a70-148">Lorsque les fichiers résolus sont téléchargés, les métadonnées d’origine sont conservées, à l’exception des champs suivants:</span><span class="sxs-lookup"><span data-stu-id="f4a70-148">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="f4a70-149">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="f4a70-149">ExtractedTextSize</span></span>
- <span data-ttu-id="f4a70-150">HasText</span><span class="sxs-lookup"><span data-stu-id="f4a70-150">HasText</span></span>
- <span data-ttu-id="f4a70-151">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="f4a70-151">IsErrorRemediate</span></span>
- <span data-ttu-id="f4a70-152">LoadId</span><span class="sxs-lookup"><span data-stu-id="f4a70-152">LoadId</span></span>
- <span data-ttu-id="f4a70-153">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f4a70-153">ProcessingErrorMessage</span></span>
- <span data-ttu-id="f4a70-154">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="f4a70-154">ProcessingStatus</span></span>
- <span data-ttu-id="f4a70-155">Texte</span><span class="sxs-lookup"><span data-stu-id="f4a70-155">Text</span></span>
- <span data-ttu-id="f4a70-156">WordCount</span><span class="sxs-lookup"><span data-stu-id="f4a70-156">WordCount</span></span>
- <span data-ttu-id="f4a70-157">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="f4a70-157">WorkingsetId</span></span>

<span data-ttu-id="f4a70-158">Pour obtenir une définition de tous les champs de métadonnées dans Advanced eDiscovery, consultez la rubrique [document Metadata Fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="f4a70-158">For a definition of all metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
