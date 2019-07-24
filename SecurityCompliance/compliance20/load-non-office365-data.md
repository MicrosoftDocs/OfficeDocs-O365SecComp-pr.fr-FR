---
title: Charger des données autres qu’Office 365 dans un jeu à réviser
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
description: Importer des données non-Office 365 vers un jeu de réexamen dans un cas avancé de découverte électronique.
ms.openlocfilehash: 37f8c2a5c97452845152e2a12578b9d243ab6711
ms.sourcegitcommit: 82ee560bf3ac84079764cbb4a2d858c321f65145
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2019
ms.locfileid: "35840846"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="9a935-103">Charger des données autres qu’Office 365 dans un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="9a935-103">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="9a935-104">Tous les documents que vous devez analyser dans Advanced eDiscovery sont situés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a935-104">Not all documents that you need to analyze in Advanced eDiscovery are located in Office 365.</span></span> <span data-ttu-id="9a935-105">Avec la fonctionnalité d’importation de données non-Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne se trouvent pas dans Office 365 vers un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="9a935-105">With the non-Office 365 data import feature in Advanced eDiscovery, you can upload documents that aren't located in Office 365 to a review set.</span></span> <span data-ttu-id="9a935-106">Cet article vous explique comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="9a935-106">This article shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="9a935-107">Advanced eDiscovery nécessite un abonnement Microsoft 365 ou Office 365 E5 pour votre organisation ou un abonnement E3 avec l’abonnement de complément de conformité avancé.</span><span class="sxs-lookup"><span data-stu-id="9a935-107">Advanced eDiscovery requires an Microsoft 365 or Office 365 E5 subscription for your organization or an E3 subscription with the Advanced Compliance add-on subscription.</span></span> <span data-ttu-id="9a935-108">Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="9a935-108">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="9a935-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9a935-109">Before you begin</span></span>

<span data-ttu-id="9a935-110">L’utilisation de la fonctionnalité de téléchargement non-Office 365 décrite dans cet article requiert les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9a935-110">Using the upload non-Office 365 feature described in this article requires that you have the following:</span></span>

- <span data-ttu-id="9a935-111">Tous les dépositaires auxquels vous souhaitez associer un contenu non-Office 365 doivent se voir attribuer une licence E5 ou une licence E3 avec une licence de module complémentaire de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="9a935-111">All custodians that you want to associate non-Office 365 content to must be assigned an E5 license, or an E3 license with an Advanced Compliance add-on license.</span></span>

- <span data-ttu-id="9a935-112">Un cas de découverte électronique avancé existant.</span><span class="sxs-lookup"><span data-stu-id="9a935-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="9a935-113">Les dépositaires doivent être ajoutés à l’incident avant de pouvoir télécharger et d’associer les données non Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a935-113">Custodians must be added to the case before you can upload and associate the non-Office 365 data to them.</span></span>

- <span data-ttu-id="9a935-114">Les données non-Office 365 doivent être un type de fichier pris en charge par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9a935-114">Non-Office 365 data must be a file type that's supported by Advanced eDiscovery.</span></span> <span data-ttu-id="9a935-115">Pour plus d’informations, consultez la rubrique [types de fichiers pris en charge dans Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="9a935-115">For more information, see [Supported file types in Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span></span>

- <span data-ttu-id="9a935-116">Tous les fichiers téléchargés vers un jeu de révision doivent se trouver dans des dossiers, où chaque dossier est associé à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="9a935-116">All files that are uploaded to a review set must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="9a935-117">Les noms de ces dossiers doivent utiliser le format d’affectation de noms suivant: *alias @ NomDomaine*.</span><span class="sxs-lookup"><span data-stu-id="9a935-117">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="9a935-118">L' *alias @ DomainName* doit être l’alias et le domaine Office 365 de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9a935-118">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="9a935-119">Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="9a935-119">You can collect all the *alias@domainname* folders in a root folder.</span></span> <span data-ttu-id="9a935-120">Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* .</span><span class="sxs-lookup"><span data-stu-id="9a935-120">The root folder can only contain the *alias@domainname* folders.</span></span> <span data-ttu-id="9a935-121">Les fichiers libres dans le dossier racine ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9a935-121">Loose files in the root folder aren't supported.</span></span>

   <span data-ttu-id="9a935-122">La structure de dossiers pour les données non-Office 365 que vous souhaitez télécharger serait semblable à l’exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="9a935-122">The folder structure for the non-Office 365 data that you want to upload would be similar to the following example:</span></span>

   - <span data-ttu-id="9a935-123">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a935-123">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="9a935-124">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a935-124">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="9a935-125">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9a935-125">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="9a935-126">Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont les adresses SMTP des dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="9a935-126">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Structure de dossier de téléchargement de données non Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="9a935-128">Un compte qui est affecté au groupe de rôles gestionnaire eDiscovery (et ajouté en tant qu’administrateur eDiscovery).</span><span class="sxs-lookup"><span data-stu-id="9a935-128">An account that is assigned to the eDiscovery Manager role group (and added as eDiscovery Administrator).</span></span>

- <span data-ttu-id="9a935-129">Outils de stockage Microsoft Azure installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a935-129">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span> <span data-ttu-id="9a935-130">Pour installer AzCopy, consultez la rubrique [prise en main de AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="9a935-130">To install AzCopy, see [Get started with AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span> <span data-ttu-id="9a935-131">Veillez à installer AzCopy à l’emplacement par défaut, à savoir **% ProgramFiles (x86)% \ Microsoft SDKs\Azure\AzCopy**.</span><span class="sxs-lookup"><span data-stu-id="9a935-131">Be sure to install AzCopy in the default location, which is **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span></span>


## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="9a935-132">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9a935-132">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="9a935-133">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="9a935-133">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  

2. <span data-ttu-id="9a935-134">Cliquez sur réviser les **ensembles**, puis sélectionnez le jeu de révision pour lequel télécharger les données non Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a935-134">Click **Review sets**, and then select the review set to upload the non-Office 365 data to.</span></span>  <span data-ttu-id="9a935-135">Si vous n’avez pas d’ensemble de révision, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="9a935-135">If you don't have a review set, you can create one.</span></span> 
 
3. <span data-ttu-id="9a935-136">Dans l’ensemble de révision, cliquez sur **gérer l’ensemble**de révisions, puis sur **afficher les téléchargements** dans la vignette **données autres que Office 365** .</span><span class="sxs-lookup"><span data-stu-id="9a935-136">In the review set, click **Manage review set**, and then click **View uploads** on the **Non-Office 365 data** tile.</span></span>

4. <span data-ttu-id="9a935-137">Cliquez sur **Télécharger les fichiers** pour démarrer l’Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="9a935-137">Click **Upload files** to start the Non-Office 365 data import wizard.</span></span>

   ![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   <span data-ttu-id="9a935-139">La première étape de l’Assistant prépare un emplacement de stockage Azure sécurisé fourni par Microsoft pour télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="9a935-139">The first step in the wizard prepares a secure Microsoft-provided Azure Storage location to upload the files to.</span></span>  <span data-ttu-id="9a935-140">Une fois la préparation terminée, le bouton **suivant: charger les fichiers** devient actif.</span><span class="sxs-lookup"><span data-stu-id="9a935-140">When the preparation is completed, the **Next: Upload files** button becomes active.</span></span>

   ![Non-Office 365 Import: prepare](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. <span data-ttu-id="9a935-142">Cliquez sur **suivant: charger les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="9a935-142">Click **Next: Upload files**.</span></span>

6. <span data-ttu-id="9a935-143">Sur la page **Télécharger les fichiers** , procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9a935-143">On the **Upload files** page, do the following:</span></span>

   ![Importation non Office 365: Télécharger des fichiers](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   <span data-ttu-id="9a935-145">a.</span><span class="sxs-lookup"><span data-stu-id="9a935-145">a.</span></span> <span data-ttu-id="9a935-146">Dans la zone **chemin d’accès à l’emplacement des fichiers** , vérifiez ou tapez l’emplacement du dossier racine dans lequel vous avez stocké les données non Office 365 que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="9a935-146">In the **Path to location of files** box, verify or type the location of the root folder where you've stored the non-Office 365 data you want to upload.</span></span> <span data-ttu-id="9a935-147">Par exemple, pour l’emplacement des fichiers d’exemple présentés dans la **section avant de commencer**, vous devez taper **%USERPROFILE\Downloads\nonO365**.</span><span class="sxs-lookup"><span data-stu-id="9a935-147">For example, for the location of the example files shown in the **Before you begin section**, you would type **%USERPROFILE\Downloads\nonO365**.</span></span> <span data-ttu-id="9a935-148">La fourniture de l’emplacement correct garantit que la commande AzCopy affichée dans la zone sous le chemin est correctement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="9a935-148">Providing the correct location ensures the AzCopy command displayed in box under the path is properly updated.</span></span>

   <span data-ttu-id="9a935-149">b.</span><span class="sxs-lookup"><span data-stu-id="9a935-149">b.</span></span> <span data-ttu-id="9a935-150">Cliquez sur **copier dans le presse-papiers** pour copier la commande affichée dans la zone.</span><span class="sxs-lookup"><span data-stu-id="9a935-150">Click **Copy to clipboard** to copy the command that is displayed in the box.</span></span> <span data-ttu-id="9a935-151">Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="9a935-151">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="9a935-152">Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="9a935-152">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

7. <span data-ttu-id="9a935-153">Démarrez une invite de commandes Windows, collez la commande que vous avez copiée à l’étape précédente, puis appuyez sur **entrée** pour démarrer la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="9a935-153">Start a Windows command prompt, paste the command that you copied in the previous step, and then press **Enter** to start the AzCopy command.</span></span>  <span data-ttu-id="9a935-154">Une fois que vous avez démarré la commande, les fichiers non-Office 365 sont téléchargés vers l’emplacement de stockage Azure préparé à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="9a935-154">After you start the command, the non-Office 365 files will be uploaded to the Azure Storage location that was prepared in step 4.</span></span>

   ![Importation non-Office 365: AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="9a935-156">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="9a935-156">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

8. <span data-ttu-id="9a935-157">Revenez dans le centre de sécurité & conformité, puis cliquez sur **suivant: traiter les fichiers** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="9a935-157">Go back to the Security & Compliance Center, and click **Next: Process files** in the wizard.</span></span>  <span data-ttu-id="9a935-158">Cela lance le traitement, l’extraction de texte et l’indexation des fichiers non-Office 365 qui ont été téléchargés vers l’emplacement de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="9a935-158">This initiates processing, text extraction, and indexing of the non-Office 365 files that were uploaded to the Azure Storage location.</span></span>  

9. <span data-ttu-id="9a935-159">Effectuez le suivi de la progression du traitement des fichiers non-Office 365 sur la page des **fichiers de processus** ou sur l’onglet **travaux** en affichant un travail nommé **ajout de données non Office 365 à un jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="9a935-159">Track the progress of processing the non-Office 365 files on the **Process files** page or on the **Jobs** tab by viewing a job named **Adding non-Office 365 data to a review set**.</span></span>  <span data-ttu-id="9a935-160">Une fois le travail terminé, les nouveaux fichiers seront disponibles dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="9a935-160">After the job is finished, the new files will be available in the review set.</span></span>

   ![Importation non Office 365: fichiers de processus](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. <span data-ttu-id="9a935-162">Une fois le traitement terminé, vous pouvez fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="9a935-162">After the processing is finished, you can close the wizard.</span></span>