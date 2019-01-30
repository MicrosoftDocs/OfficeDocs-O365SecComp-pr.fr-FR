---
title: Correction d’erreur lors du traitement des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607718"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="189ca-102">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="189ca-102">Error remediation when processing data</span></span>

<span data-ttu-id="189ca-p101">Correction d’erreur permet aux administrateurs de découverte électronique à résoudre les problèmes liés aux données qui empêchent le traitement correctement le contenu eDiscovery avancée (Preview). Par exemple, les fichiers qui sont protégés par mot de passe ne peuvent pas être traités dans la mesure où les fichiers sont verrouillés ou chiffrés. À l’aide de la correction d’erreur, les administrateurs de découverte électronique peuvent télécharger des fichiers avec ces erreurs, supprimez la protection par mot de passe et un télécharger les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="189ca-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="189ca-106">Utilisez la procédure suivante pour convertir des fichiers avec des erreurs dans les cas eDiscovery avancées (Preview).</span><span class="sxs-lookup"><span data-stu-id="189ca-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="189ca-107">Création d’une session de correction d’erreur pour résoudre les fichiers avec traitement des erreurs</span><span class="sxs-lookup"><span data-stu-id="189ca-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="189ca-108">Si la fermeture de l’Assistant de correction d’erreur à tout moment au cours de la procédure suivante, vous pouvez retourner à la session de correction d’erreur à partir de l’onglet **de traitement** en sélectionnant **correctives d’erreur** dans le menu déroulant **affichage** .</span><span class="sxs-lookup"><span data-stu-id="189ca-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="189ca-109">Sous l’onglet **de traitement** dans un cas eDiscovery avancées (Preview), sélectionnez **les erreurs** dans le menu déroulant **affichage** .</span><span class="sxs-lookup"><span data-stu-id="189ca-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="189ca-p102">Sélectionnez les erreurs que vous souhaitez convertir en cliquant sur le bouton d’option en regard du type d’erreur ou un type de fichier.  Dans l’exemple suivant, nous allons corriger un fichier protégé de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="189ca-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="189ca-112">Cliquez sur **+ Nouveau correction d’erreur**.</span><span class="sxs-lookup"><span data-stu-id="189ca-112">Click **+ New error remediation**.</span></span>

    ![Correction d’erreur](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="189ca-114">La session de correction d’erreur commencera commençant par une étape de préparation où les fichiers ayant subi une erreur qui sont déplacés vers un emplacement sécurisé Azure à télécharger.</span><span class="sxs-lookup"><span data-stu-id="189ca-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Préparation de la correction d’erreur](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="189ca-116">Une fois la préparation terminée, cliquez sur **suivant : télécharger des fichiers** pour poursuivre le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="189ca-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Télécharger des fichiers](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="189ca-p103">Pour télécharger des fichiers, spécifiez le **chemin d’accès de Destination pour le téléchargement**; Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier doit être téléchargé.  Le chemin d’accès par défaut, % USERPROFILE%\Downloads\errors, pointe vers le dossier Téléchargements connecté l’utilisateur. Cela peut être modifié selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="189ca-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="189ca-120">Nous vous recommandons d’utiliser un chemin d’accès local au lieu d’un chemin d’accès réseau distant pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="189ca-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="189ca-121">Si vous n’avez pas installé AzCopy, vous pouvez l’installer à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="189ca-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="189ca-p104">Copiez la commande prédéfinie en cliquant sur **Copier dans le Presse-papiers**. Démarrez une invite de commandes windows, collez la commande, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="189ca-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="189ca-124">Les fichiers sont téléchargés.</span><span class="sxs-lookup"><span data-stu-id="189ca-124">The files will be downloaded.</span></span>

    ![Préparation de la correction d’erreur](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="189ca-126">Si vous avez des problèmes d’exécution de cette commande, voir https://go.microsoft.com/fwlink/?linkid=2038117 pour des conseils de dépannage.</span><span class="sxs-lookup"><span data-stu-id="189ca-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="189ca-p105">Après avoir téléchargé les fichiers, vous pouvez les résoudre un outil approprié. Pour les fichiers protégés par mot de passe, il existe un certain nombre de mot de passe que vous pouvez utiliser des outils de décodage. Si vous connaissez les mots de passe pour les fichiers, vous pouvez les ouvrir et supprimer le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="189ca-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="189ca-p106">INFORMATIQUE est important de conserver les noms de fichier et la structure de répertoire des fichiers corrigés intactes.  Toutes les conventions d’affectation de noms utilisés dans les fichiers téléchargés et les dossiers vous permettent d’associer les fichiers remdiated à l’original.</span><span class="sxs-lookup"><span data-stu-id="189ca-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="189ca-p107">Retournez à la découverte électronique avancée (Preview) et cliquez sur **suivant : télécharger les fichiers**.  Ce est déplacés à l’étape suivante où vous pouvez désormais télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="189ca-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![Télécharger des fichiers](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="189ca-135">Spécifier l’emplacement des fichiers corrigés dans la zone de texte **chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **Copier dans un clibpboard**.</span><span class="sxs-lookup"><span data-stu-id="189ca-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="189ca-136">Collez la commande dans une invite de commandes Windows et appuyez sur **entrée** pour télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="189ca-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="189ca-138">Enfin, revenez à la découverte électronique avancée (Preview) et cliquez sur **suivant : traitement des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="189ca-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="189ca-p108">Lorsque le traitement est terminé.  Vous pouvez revenir à la plage de travail et consultez le fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="189ca-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="189ca-141">Que se passe-t-il lorsque les fichiers sont résolues.</span><span class="sxs-lookup"><span data-stu-id="189ca-141">What happens when files are remediated</span></span>

<span data-ttu-id="189ca-142">Lorsque des fichiers corrigés sont téléchargés, les métadonnées d’origine sont conservée à l’exception des champs suivants :</span><span class="sxs-lookup"><span data-stu-id="189ca-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="189ca-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="189ca-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="189ca-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="189ca-144">ExtractedTextSize</span></span>
- <span data-ttu-id="189ca-145">HasText</span><span class="sxs-lookup"><span data-stu-id="189ca-145">HasText</span></span>
- <span data-ttu-id="189ca-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="189ca-146">IsErrorRemediate</span></span>
- <span data-ttu-id="189ca-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="189ca-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="189ca-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="189ca-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="189ca-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="189ca-149">LoadId</span></span>
- <span data-ttu-id="189ca-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="189ca-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="189ca-151">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="189ca-151">ProcessingStatus</span></span>
- <span data-ttu-id="189ca-152">Texte</span><span class="sxs-lookup"><span data-stu-id="189ca-152">Text</span></span>
- <span data-ttu-id="189ca-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="189ca-153">WordCount</span></span>
- <span data-ttu-id="189ca-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="189ca-154">WorkingsetId</span></span>

<span data-ttu-id="189ca-155">Pour une définition de tous les champs de métadonnées de document d’eDiscovery avancée (Preview), voir [les champs de métadonnées de Document](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="189ca-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>