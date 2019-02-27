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
ms.openlocfilehash: b177fc292c748f21907621196dc28d6b8fe17959
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296787"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="b7bf9-102">Charger les données ne provenant pas d’Office 365 dans un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="b7bf9-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="b7bf9-p101">Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365. Avec la fonctionnalité d'importation de contenu autre que Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans un jeu de travail afin de les analyser avec Advanced eDiscovery. Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="b7bf9-p102">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b7bf9-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b7bf9-108">Before you begin</span></span>
<span data-ttu-id="b7bf9-109">L'utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b7bf9-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="b7bf9-110">Un Office 365 E3 avec le complément de conformité avancé ou l'abonnement E5.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="b7bf9-111">Tous les dépositaires dont le contenu n'est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="b7bf9-112">Un cas eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="b7bf9-p103">Tous les fichiers de téléchargement rassemblé dans des dossiers contenant un dossier par dépositaire et le nom de ces dossiers se présente à l'alias de format *@ nomdomaine* . L' *alias @ NomDomaine* doit être l'alias et le domaine Office 365 des utilisateurs. Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine. Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="b7bf9-117">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery outils de stockage Microsoft Azure installé sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="b7bf9-118">Installez AzCopy en procédant comme suit:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="b7bf9-118">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="b7bf9-119">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b7bf9-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="b7bf9-p104">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.  Cliquez sur l'onglet **jeux de travail** , puis sélectionnez la plage de travail que vous souhaitez utiliser pour charger les données Non Office 365.  Si vous n'avez pas encore créé de jeu de travail, vous pouvez le faire maintenant.  Enfin, cliquez sur **gérer les tâches définies** , puis **afficher les téléchargements** dans la section données non-Office 365</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="b7bf9-124">Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l'Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="b7bf9-p105">La première étape de l'Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.  Une fois que la préparation est comfaite, cliquez sur le bouton **suivant: charger des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Importation-préparation de non-Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="b7bf9-p106">Dans l'étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l'emplacement des fichiers**, c'est ici que se trouvent les données autres que Office 365 que vous prévoyez d'importer.  La définition de l'emplacement correct garantit la mise à jour correcte de la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="b7bf9-131">Si vous n'avez pas encore installé AzCopy, vous pouvez le faire à partir de là:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="b7bf9-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="b7bf9-p107">Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** . Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.  Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l'étape suivante.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Fichiers d'importation/exportation non Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importation AzCopy non-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="b7bf9-p108">Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant: traiter les fichiers** .  Cela démarrera le traitement, l'extraction de texte et l'indexation des fichiers téléchargés.  Vous pouvez suivre la progression du traitement ou dans l'onglet **travaux** .  Une fois terminé, les nouveaux fichiers seront disponibles dans le jeu de travail.  Une fois le traitement terminé, vous pouvez faire disparaître l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="b7bf9-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Fichiers de processus d'importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

