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
description: ''
ms.openlocfilehash: 86d858994f95176ea4d415405c4043f7e7c5308e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155006"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="5182f-102">Charger des données autres qu’Office 365 dans un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="5182f-102">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="5182f-103">Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="5182f-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="5182f-104">Avec la fonctionnalité d’importation de contenu autre que Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans un jeu de réexamens afin qu’il soit analysé avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="5182f-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a review set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="5182f-105">Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="5182f-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="5182f-106">Advanced eDiscovery nécessite un abonnement Office 365 E3 avec le complément de conformité avancé ou un abonnement E5 pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5182f-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="5182f-107">Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="5182f-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="5182f-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5182f-108">Before you begin</span></span>

<span data-ttu-id="5182f-109">L’utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cet article requiert les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="5182f-109">Using the upload Non-Office 365 feature as described in this article requires that you have the following:</span></span>

- <span data-ttu-id="5182f-110">Un abonnement Office 365 ou Microsoft 365 E5 ou un abonnement E3 avec l’abonnement de complément de conformité avancé.</span><span class="sxs-lookup"><span data-stu-id="5182f-110">An Office 365 or Microsoft 365 E5 subscription or an E3 subscription with the Advanced Compliance add-on subscription.</span></span>

- <span data-ttu-id="5182f-111">Tous les dépositaires dont le contenu n’est pas Office 365 seront chargés doivent disposer d’une licence E3 avec une licence de complément de conformité avancée ou avoir une licence E5.</span><span class="sxs-lookup"><span data-stu-id="5182f-111">All custodians whose non-Office 365 content will be uploaded must have E3 license with an Advanced Compliance add-on license or have an E5 license.</span></span>

- <span data-ttu-id="5182f-112">Un cas de découverte électronique avancé existant.</span><span class="sxs-lookup"><span data-stu-id="5182f-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="5182f-113">Les dépositaires doivent être ajoutés à l’incident avant le chargement des données non Office 365 qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="5182f-113">Custodians must be added to the case before you upload the non-Office 365 data that's associated to them.</span></span>

- <span data-ttu-id="5182f-114">Tous les fichiers qui seront téléchargés doivent se trouver dans des dossiers, où chaque dossier est associé à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="5182f-114">All files that will be uploaded must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="5182f-115">Les noms de ces dossiers doivent utiliser le format d’affectation de noms suivant: *alias @ NomDomaine*.</span><span class="sxs-lookup"><span data-stu-id="5182f-115">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="5182f-116">L' *alias @ DomainName* doit être l’alias et le domaine Office 365 de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5182f-116">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="5182f-117">Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="5182f-117">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="5182f-118">Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* ; les fichiers libres ne sont pas autorisés dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="5182f-118">The root folder can only contain the *alias@domainname* folders; loose files aren't allowed in the root folder.</span></span>

   <span data-ttu-id="5182f-119">Par exemple, la structure de dossiers pour les données non-Office 365 que vous souhaitez télécharger serait semblable à la suivante:</span><span class="sxs-lookup"><span data-stu-id="5182f-119">For example, the folder structure for the non-Office 365 data that you want to upload would be similar to the following:</span></span>

   - <span data-ttu-id="5182f-120">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5182f-120">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="5182f-121">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5182f-121">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="5182f-122">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5182f-122">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="5182f-123">Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont les adresses SMTP des dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="5182f-123">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Structure de dossier de téléchargement de données non Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="5182f-125">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5182f-125">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>

- <span data-ttu-id="5182f-126">Outils de stockage Microsoft Azure installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="5182f-126">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="5182f-127">Installez AzCopy en procédant comme suit:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="5182f-127">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="5182f-128">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5182f-128">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="5182f-129">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="5182f-129">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="5182f-130">Cliquez sur l’onglet **examiner les ensembles** , puis sélectionnez l’ensemble de révision sur lequel vous souhaitez charger les données Non Office 365.</span><span class="sxs-lookup"><span data-stu-id="5182f-130">Click the **review sets** tab, then select the review set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="5182f-131">Si vous n’avez pas encore créé de jeu de révision, vous pouvez le faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="5182f-131">If you have not already created a review set, you can do so now.</span></span>  <span data-ttu-id="5182f-132">Enfin, cliquez sur **gérer le jeu de révision** , puis sur Afficher les **téléchargements** dans la vignette des données \* \* autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="5182f-132">Finally, click **Manage review set** and then click **View uploads** in the \*\*Non-Office 365 data tile.</span></span>

2. <span data-ttu-id="5182f-133">Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l’Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="5182f-133">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

   ![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="5182f-135">La première étape de l’Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.</span><span class="sxs-lookup"><span data-stu-id="5182f-135">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="5182f-136">Une fois la préparation terminée, cliquez sur le bouton **suivant: charger des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="5182f-136">Once preparation is completed, click the **Next: Upload files** button.</span></span>

   ![Importation-préparation de non-Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="5182f-138">Dans l’étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l’emplacement des fichiers**, c’est ici que se trouvent les données autres que Office 365 que vous prévoyez d’importer.</span><span class="sxs-lookup"><span data-stu-id="5182f-138">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="5182f-139">La définition de l’emplacement correct garantit la mise à jour correcte de la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="5182f-139">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

   > [!NOTE]
   > <span data-ttu-id="5182f-140">Si vous n’avez pas encore installé AzCopy, vous pouvez le faire à partir de là:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="5182f-140">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="5182f-141">Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** .</span><span class="sxs-lookup"><span data-stu-id="5182f-141">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="5182f-142">Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="5182f-142">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="5182f-143">Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="5182f-143">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

   ![Fichiers d’importation/exportation non Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Importation AzCopy non-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="5182f-146">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="5182f-146">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="5182f-147">Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant: traiter les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="5182f-147">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="5182f-148">Cela démarrera le traitement, l’extraction de texte et l’indexation des fichiers téléchargés.</span><span class="sxs-lookup"><span data-stu-id="5182f-148">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="5182f-149">Vous pouvez suivre la progression du traitement ou dans l’onglet **travaux** .  Une fois terminé, les nouveaux fichiers seront disponibles dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="5182f-149">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the review set.</span></span>  <span data-ttu-id="5182f-150">Une fois le traitement terminé, vous pouvez faire disparaître l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5182f-150">Once processing is complete, you can dismiss the wizard.</span></span>

   ![Fichiers de processus d’importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

