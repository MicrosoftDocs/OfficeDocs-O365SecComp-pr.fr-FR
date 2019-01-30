---
title: Charger des données de non Office 365 dans un jeu de travail
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
ms.openlocfilehash: 427b4c8c9dfffe351827a6869ae26a5356d646d8
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607688"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="906a4-102">Charger des données de non Office 365 dans un jeu de travail</span><span class="sxs-lookup"><span data-stu-id="906a4-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="906a4-p101">Pas de tous les documents que vous devrez peut-être analyser avec Office 365 avancée de découverte électronique résidera dans Office 365. Avec le contenu Non-Office 365 importer la fonctionnalité de découverte avancé, que vous pouvez télécharger des documents qui ne live dans Office 365 dans un jeu de travail afin qu’il est analysé avec eDiscovery avancée. Cette procédure indique comment intégrer vos documents non Office 365 à eDiscovery avancée pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="906a4-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="906a4-p102">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="906a4-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="906a4-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="906a4-108">Before you begin</span></span>
<span data-ttu-id="906a4-109">À l’aide de la fonctionnalité de téléchargement Non-Office 365 comme décrit dans cette procédure suppose que :</span><span class="sxs-lookup"><span data-stu-id="906a4-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
* <span data-ttu-id="906a4-110">Un Office 365 E3 avec le module complémentaire de conformité avancée ou abonnement E5</span><span class="sxs-lookup"><span data-stu-id="906a4-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
* <span data-ttu-id="906a4-111">Tous les dépositaires non Office 365 dont le contenu sera téléchargé doivent avoir E3 avec le module complémentaire de conformité avancée ou licences E5</span><span class="sxs-lookup"><span data-stu-id="906a4-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
* <span data-ttu-id="906a4-112">Un cas de découverte électronique existant</span><span class="sxs-lookup"><span data-stu-id="906a4-112">An existing eDiscovery case</span></span>
* <span data-ttu-id="906a4-p103">Tous les fichiers de téléchargement regroupés dans les dossiers où il existe un dossier par dépositaire et nom des dossiers dans ce format *alias@domainname* . *alias@domainname* doit être domaine et l’alias d’utilisateurs Office 365. Vous pouvez regrouper tous les dossiers *alias@domainname* dans un dossier racine. Le dossier racine ne peut contenir les dossiers *alias@domainname* , il ne doit exister aucun fichier libre dans le dossier racine</span><span class="sxs-lookup"><span data-stu-id="906a4-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder</span></span>
* <span data-ttu-id="906a4-117">Un compte qui est installé sur un ordinateur ayant accès à la structure de dossier contenu Office 365 eDiscovery administrateur Microsoft Azure stockage outils ou un gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="906a4-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>
* <span data-ttu-id="906a4-118">Installer AzCopy, vous pouvez le faire à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="906a4-118">Install AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="906a4-119">Télécharger du contenu d’Office 365 en découverte avancée</span><span class="sxs-lookup"><span data-stu-id="906a4-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>
1. <span data-ttu-id="906a4-p104">En tant qu’un gestionnaire eDiscovery ou eDiscovery administrateur, ouvrez eDiscovery avancé, puis le cas pour les données non Office 365 seront téléchargées.  Cliquez sur l’onglet **jeux de travail** , puis sélectionnez le jeu de travail que vous souhaitez charger les données Non-Office 365.  Si vous n’avez pas déjà créé un jeu de travail, vous pouvez le faire maintenant.  Enfin, cliquez sur **Gérer les rouages** puis **téléchargements affichage** dans la section de données Non-Office 365</span><span class="sxs-lookup"><span data-stu-id="906a4-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="906a4-124">Cliquez sur le bouton **télécharger des fichiers** pour démarrer l’Assistant Importation de données Non-Office 365.</span><span class="sxs-lookup"><span data-stu-id="906a4-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Télécharger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="906a4-p105">La première étape dans l’Assistant prépare simplement un blob Azure sécurisé pour les téléchargement de fichiers.  Une fois la préparation de compelted, cliquez sur le **suivant : télécharger les fichiers** bouton.</span><span class="sxs-lookup"><span data-stu-id="906a4-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Non Office 365 importer - préparation](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="906a4-p106">Dans l’étape de **télécharger des fichiers** , spécifiez le **chemin d’accès à l’emplacement des fichiers**, il s’agit où se trouve les données Non-Office 365 que vous prévoyez d’importation.  Définition de l’emplacement correct garantit la AzCopy commande correctement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="906a4-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="906a4-131">Si vous n’avez pas déjà installé AzCopy, vous pouvez effectuer cela à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="906a4-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="906a4-p107">Copiez la commande prédéfinie en cliquant sur le lien **Copier dans le Presse-papiers** . Démarrez une invite de commandes windows, collez la commande et appuyez sur ENTRÉE.  Les fichiers seront téléchargés vers le stockage blob Azure sécurisé pour l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="906a4-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Importation non-Office 365 - télécharger des fichiers](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importation non Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="906a4-p108">Enfin, renvoyer à la conformité de & sécurité, cliquez sur le **suivant : traitement des fichiers** bouton.  Ceci va démarrer le traitement, extraction de texte et l’indexation des fichiers téléchargés.  Vous pouvez suivre la progression de traitement ici ou dans l’onglet **tâches** .  Une fois terminé, les nouveaux fichiers seront disponibles dans le jeu de travail.  Une fois le traitement est terminé, vous pouvez fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="906a4-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Importation non-Office 365 - traiter les fichiers](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

