---
title: Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Vous pouvez modifier le la taille par défaut des fichiers PST qui est téléchargé sur votre ordinateur lorsque vous exportez des résultats de recherche eDiscovery.
ms.openlocfilehash: d38189c437154dbe27a084230d4d3fd4de418ece
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527568"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="43f58-103">Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery</span><span class="sxs-lookup"><span data-stu-id="43f58-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="43f58-p101">Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour exporter les résultats de la messagerie d’une recherche de découverte électronique à partir de différents outils Microsoft eDiscovery, la taille par défaut d’un fichier PST qui peut être exporté est de 10 Go. Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Une des raisons à cela étant un fichier PST tiennent sur un support amovible, tel un DVD, un CD-ROM ou une clé USB.</span><span class="sxs-lookup"><span data-stu-id="43f58-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="43f58-107">L’outil d’exportation de découverte électronique Office 365 est utilisée pour exporter les résultats de recherche lors de l’utilisation de la recherche de contenu de sécurité Office 365 &amp; centre de conformité, eDiscovery sur Place dans Exchange Online et le centre eDiscovery dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="43f58-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="43f58-108">Créer un paramètre de Registre pour modifier la taille des fichiers PST lors de l’exportation de résultats de recherche eDiscovery</span><span class="sxs-lookup"><span data-stu-id="43f58-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="43f58-109">Effectuez la procédure suivante sur l’ordinateur que vous allez utiliser pour exporter les résultats d’une recherche eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="43f58-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="43f58-110">Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="43f58-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="43f58-111">Enregistrez le texte suivant dans un fichier de Registre de fenêtre à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, PstExportSize.reg.</span><span class="sxs-lookup"><span data-stu-id="43f58-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="43f58-p102">Dans l’exemple ci-dessus, le `PstSizeLimitInBytes` valeur est définie sur 1 073 741 824 octets ou environ 1 Go. Voici quelques autres exemples de valeurs pour le `PstSizeLimitInBytes` paramètre.</span><span class="sxs-lookup"><span data-stu-id="43f58-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="43f58-114">**Taille en Go (environ)**</span><span class="sxs-lookup"><span data-stu-id="43f58-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="43f58-115">**Taille en octets**</span><span class="sxs-lookup"><span data-stu-id="43f58-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="43f58-116">.7 GO (700 MO)</span><span class="sxs-lookup"><span data-stu-id="43f58-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="43f58-117">751619277</span><span class="sxs-lookup"><span data-stu-id="43f58-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="43f58-118">2 Go</span><span class="sxs-lookup"><span data-stu-id="43f58-118">2 GB</span></span>  <br/> |<span data-ttu-id="43f58-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="43f58-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="43f58-120">4 Go</span><span class="sxs-lookup"><span data-stu-id="43f58-120">4 GB</span></span>  <br/> |<span data-ttu-id="43f58-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="43f58-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="43f58-122">8 Go</span><span class="sxs-lookup"><span data-stu-id="43f58-122">8 GB</span></span>  <br/> |<span data-ttu-id="43f58-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="43f58-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="43f58-124">Modifier la `PstSizeLimitInBytes` valeur à la taille maximale de votre choix d’un fichier PST lorsque vous exportez les résultats de recherche, puis enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="43f58-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="43f58-125">Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créée lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="43f58-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="43f58-126">Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification.</span><span class="sxs-lookup"><span data-stu-id="43f58-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="43f58-127">Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="43f58-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="43f58-128">L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.</span><span class="sxs-lookup"><span data-stu-id="43f58-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="43f58-129">Vous pouvez répéter les étapes 3 à 6 pour modifier la valeur pour le `PstSizeLimitInBytes` paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="43f58-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="43f58-130">Forum aux questions sur la modification de la taille par défaut des fichiers PST lors de l’exportation de résultats de recherche eDiscovery</span><span class="sxs-lookup"><span data-stu-id="43f58-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="43f58-131">**Pourquoi est la valeur par défaut taille 10 Go ?**</span><span class="sxs-lookup"><span data-stu-id="43f58-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="43f58-132">La taille par défaut de 10 Go a été en fonction des commentaires des clients ; 10 Go est un bon équilibre entre la quantité de contenu dans un fichier PST unique et avec un risque de corruption de fichier minimal optimale.</span><span class="sxs-lookup"><span data-stu-id="43f58-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="43f58-133">**Dois-je augmenter ou diminuer la taille par défaut des fichiers PST ?**</span><span class="sxs-lookup"><span data-stu-id="43f58-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="43f58-p103">Les clients ont tendance à diminuer la limite de taille afin que les résultats de recherche adapté sur un support amovible qu’ils peuvent physiquement expédier autres emplacements dans leur organisation. Nous ne recommandons pas augmenter la taille par défaut, car il est supérieure à 10 Go peut-être des problèmes de corruption des fichiers PST.</span><span class="sxs-lookup"><span data-stu-id="43f58-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="43f58-136">**Quel ordinateur dois-je faire ?**</span><span class="sxs-lookup"><span data-stu-id="43f58-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="43f58-137">Vous devez modifier le paramètre de Registre sur un ordinateur local que vous exécutez l’outil d’exportation de découverte électronique Office 365 sur.</span><span class="sxs-lookup"><span data-stu-id="43f58-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="43f58-138">**Après modification de ce paramètre, dois-je redémarrer l’ordinateur ?**</span><span class="sxs-lookup"><span data-stu-id="43f58-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="43f58-p104">Non, vous n’êtes pas obligé de redémarrer l’ordinateur. Mais, si l’outil d’exportation de découverte électronique Office 365 est en cours d’exécution, vous devrez fermer et le redémarrage après vous modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="43f58-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="43f58-141">**Est une clé de Registre existante obtenir modifiée ou est une nouvelle clé sont créée ?**</span><span class="sxs-lookup"><span data-stu-id="43f58-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="43f58-p105">Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans cette procédure. Puis le paramètre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg.</span><span class="sxs-lookup"><span data-stu-id="43f58-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
