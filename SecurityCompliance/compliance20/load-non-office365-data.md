---
title: Charger les données ne provenant pas d’Office 365 dans un ensemble de travail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 2ac12cf8c447e3341724d9e853da0f32b7c232fb
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958695"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="1ecfa-102">Charger les données ne provenant pas d’Office 365 dans un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="1ecfa-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="1ecfa-103">Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="1ecfa-104">Avec la fonctionnalité d'importation de contenu autre que Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans un jeu de travail afin de les analyser avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="1ecfa-105">Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="1ecfa-106">Advanced eDiscovery nécessite un abonnement Office 365 E3 avec le complément de conformité avancé ou un abonnement E5 pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="1ecfa-107">Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d'évaluation d'Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="1ecfa-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1ecfa-108">Before you begin</span></span>
<span data-ttu-id="1ecfa-109">L'utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="1ecfa-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="1ecfa-110">Un Office 365 E3 avec le complément de conformité avancé ou l'abonnement E5.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="1ecfa-111">Tous les dépositaires dont le contenu n'est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="1ecfa-112">Un cas eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="1ecfa-113">Tous les fichiers de téléchargement rassemblé dans des dossiers contenant un dossier par dépositaire et le nom de ces dossiers se présente à l'alias de format *@ nomdomaine* .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-113">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* .</span></span> <span data-ttu-id="1ecfa-114">L' *alias @ NomDomaine* doit être l'alias et le domaine Office 365 des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-114">The *alias@domainname* must be users Office 365 alias and domain.</span></span> <span data-ttu-id="1ecfa-115">Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-115">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="1ecfa-116">Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-116">The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

   <span data-ttu-id="1ecfa-117">La structure de dossiers pour les données non Office 365 que vous prévoyez de télécharger doit ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="1ecfa-117">The folder structure for the non-Office 365 data you plan to upload should look something like the following:</span></span>

   - <span data-ttu-id="1ecfa-118">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1ecfa-118">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="1ecfa-119">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1ecfa-119">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="1ecfa-120">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1ecfa-120">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="1ecfa-121">Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont des adresses SMTP des dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-121">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are SMTP addresses of custodians in the case.</span></span>

![Structure de dossier de téléchargement de données non Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="1ecfa-123">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery outils de stockage Microsoft Azure installé sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-123">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="1ecfa-124">Installez AzCopy en procédant comme suit:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="1ecfa-124">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="1ecfa-125">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1ecfa-125">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="1ecfa-126">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-126">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="1ecfa-127">Cliquez sur l'onglet **jeux de travail** , puis sélectionnez la plage de travail que vous souhaitez utiliser pour charger les données Non Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-127">Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="1ecfa-128">Si vous n'avez pas encore créé de jeu de travail, vous pouvez le faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-128">If you have not already created a working set, you can do so now.</span></span>  <span data-ttu-id="1ecfa-129">Enfin, cliquez sur **gérer les tâches définies** , puis **afficher les téléchargements** dans la section données non-Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-129">Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section.</span></span>

2. <span data-ttu-id="1ecfa-130">Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l'Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-130">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="1ecfa-132">La première étape de l'Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-132">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="1ecfa-133">Une fois la préparation terminée, cliquez sur le bouton **suivant: charger des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-133">Once preparation is completed, click the **Next: Upload files** button.</span></span>

![Importation-préparation de non-Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="1ecfa-135">Dans l'étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l'emplacement des fichiers**, c'est ici que se trouvent les données autres que Office 365 que vous prévoyez d'importer.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-135">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="1ecfa-136">La définition de l'emplacement correct garantit la mise à jour correcte de la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-136">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="1ecfa-137">Si vous n'avez pas encore installé AzCopy, vous pouvez le faire à partir de là:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="1ecfa-137">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="1ecfa-138">Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-138">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="1ecfa-139">Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-139">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="1ecfa-140">Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-140">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Fichiers d'importation/exportation non Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importation AzCopy non-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

> [!NOTE]
> <span data-ttu-id="1ecfa-143">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="1ecfa-143">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="1ecfa-144">Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant: traiter les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-144">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="1ecfa-145">Cela démarrera le traitement, l'extraction de texte et l'indexation des fichiers téléchargés.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-145">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="1ecfa-146">Vous pouvez suivre la progression du traitement ou dans l'onglet **travaux** .  Une fois terminé, les nouveaux fichiers seront disponibles dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-146">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.</span></span>  <span data-ttu-id="1ecfa-147">Une fois le traitement terminé, vous pouvez faire disparaître l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-147">Once processing is complete, you can dismiss the wizard.</span></span>

![Fichiers de processus d'importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

