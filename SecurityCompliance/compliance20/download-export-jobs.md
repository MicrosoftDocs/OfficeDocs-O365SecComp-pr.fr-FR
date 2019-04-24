---
title: Télécharger l’exportation des travaux
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
ms.openlocfilehash: 904bc5f8a6d6cef937d55336e8f383957713769a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251896"
---
# <a name="download-export-jobs"></a><span data-ttu-id="b7a9f-102">Télécharger l’exportation des travaux</span><span class="sxs-lookup"><span data-stu-id="b7a9f-102">Download export jobs</span></span>

<span data-ttu-id="b7a9f-103">Toutes les données exportées sont ajoutées à un objet BLOB Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-103">All exported data is added to a Microsoft Azure blob.</span></span> <span data-ttu-id="b7a9f-104">Cela fournit plusieurs options pour gérer les données en aval.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-104">This provides multiple options to handle the data downstream.</span></span> <span data-ttu-id="b7a9f-105">Il existe plusieurs façons d'accéder à un objet BLOB Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-105">There are several ways to access an Azure blob.</span></span> <span data-ttu-id="b7a9f-106">L'une des méthodes consiste à utiliser l'Explorateur de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-106">One method is to use Azure Storage Explorer.</span></span> <span data-ttu-id="b7a9f-107">Cette méthode prend en charge la connexion, la navigation et le téléchargement simples.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-107">This method supports simple connection, browsing and downloading.</span></span> <span data-ttu-id="b7a9f-108">Pour plus d'informations, reportez-vous à<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span><span class="sxs-lookup"><span data-stu-id="b7a9f-108">For more information, visit <https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span></span>

1.  <span data-ttu-id="b7a9f-109">Pour télécharger du contenu à la fin d'une opération d'exportation, accédez à l'onglet exportations et sélectionnez un travail d'exportation.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-109">To download content after an export job is complete, go to the Exports tab and select an export job.</span></span>

2.  <span data-ttu-id="b7a9f-110">Copiez le texte dans la section «emplacements» de la fenêtre mobile.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-110">Copy the text in the “Locations” section of the flyout.</span></span>

![](../media/eDiscoExportJob.png)

3.  <span data-ttu-id="b7a9f-111">Ouvrez l'Explorateur de stockage Azure et cliquez sur le bouton «se connecter»</span><span class="sxs-lookup"><span data-stu-id="b7a9f-111">Open Azure Storage Explorer and click the “Connect” button</span></span>

![](../media/AzureStorageConnect.png)

4.  <span data-ttu-id="b7a9f-112">Sélectionnez «utiliser un URI de signature d'accès partagé», puis cliquez sur suivant.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-112">Select “Use a shared access signature URI” and click next</span></span>

![](../media/AzureStorageConnect2.png)

5.  <span data-ttu-id="b7a9f-113">Collez le texte de l'emplacement dans la zone de texte URI, puis cliquez sur suivant.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-113">Paste the Location text in the URI text box and click next</span></span>

![](../media/AzureStorageConnect3.png)

6.  <span data-ttu-id="b7a9f-114">Cliquez sur se connecter.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-114">Click Connect</span></span>

![](../media/AzureStorageConnect4.png)

<span data-ttu-id="b7a9f-115">Cette opération ajoute l'exportation en tant qu'objet dans les comptes de stockage/services SAS/conteneurs d'objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-115">This will add the export as an object in Storage Accounts/SAS-Attached Services/Blob Containers.</span></span> <span data-ttu-id="b7a9f-116">Vous serez en mesure d'explorer l'exportation et de télécharger l'ensemble ou des parties de l'exportation.</span><span class="sxs-lookup"><span data-stu-id="b7a9f-116">You will be able to explore the export and download all or portions of the export.</span></span>

![](../media/AzureStorageConnect5.png)