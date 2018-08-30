---
title: Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Découvrez comment configurer le Registre Windows pour augmenter le débit de données lorsque je télécharge des résultats de la recherche et rechercher des données à partir de la sécurité de 365 Office &amp; centre de conformité et Office 365 avancée eDiscovery.
ms.openlocfilehash: 3f456f5ee0312d4d4d7b95f868520e6756a90fd1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528761"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="cf320-103">Augmenter la vitesse de téléchargement lors de l’exportation des résultats de recherche de découverte électronique à partir d’Office 365</span><span class="sxs-lookup"><span data-stu-id="cf320-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="cf320-p101">Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour télécharger les résultats d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité ou télécharger des données à partir d’Office 365 avancée eDiscovery, l’outil démarrent un certain nombre d’exportation simultanée opérations pour télécharger les données sur votre ordinateur local. Par défaut, le nombre d’opérations simultanées est défini à 8 fois le nombre de cœurs de l’ordinateur que vous utilisez pour télécharger les données. Par exemple, si vous avez un ordinateur double cœur (ce qui signifie que deux unités centrales sur une puce), le numéro par défaut des opérations d’exportation simultanées est de 16. Pour augmenter le débit de transfert de données et accélérer le processus de téléchargement, vous pouvez augmenter le nombre d’opérations simultanées en configurant un paramètre de Registre Windows sur l’ordinateur que vous utilisez pour télécharger les résultats de recherche. Pour accélérer le processus de téléchargement, nous vous recommandons de commencer avec un paramètre de 24 opérations simultanées.</span><span class="sxs-lookup"><span data-stu-id="cf320-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="cf320-p102">Si vous téléchargez des résultats de la recherche sur un réseau de faible bande passante, l’augmentation de ce paramètre peut avoir un impact négatif. Sinon, vous pourrez peut-être augmenter le paramètre à plus de 24 opérations simultanées dans un réseau à bande passante élevée (le nombre maximal d’opérations simultanées est 512). Après avoir configuré ce paramètre de Registre, vous devrez peut-être modifier pour trouver le nombre optimal d’opérations simultanées pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="cf320-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="cf320-112">Créer un paramètre de Registre pour modifier le nombre d’opérations simultanées lors de l’exportation des données</span><span class="sxs-lookup"><span data-stu-id="cf320-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="cf320-113">Effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour télécharger les résultats de la recherche de la sécurité &amp; centre de conformité ou des données à partir de la découverte électronique avancée.</span><span class="sxs-lookup"><span data-stu-id="cf320-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="cf320-114">Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="cf320-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="cf320-115">Enregistrez le texte suivant dans un fichier de Registre de fenêtre à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, ConcurrentOperations.reg.</span><span class="sxs-lookup"><span data-stu-id="cf320-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="cf320-116">Précédente comme expliqué, nous vous recommandons de démarrer avec 24 opérations simultanées, puis modifier ce paramètre en fonction.</span><span class="sxs-lookup"><span data-stu-id="cf320-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="cf320-117">Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="cf320-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="cf320-118">Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification.</span><span class="sxs-lookup"><span data-stu-id="cf320-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="cf320-119">Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="cf320-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="cf320-120">L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.</span><span class="sxs-lookup"><span data-stu-id="cf320-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="cf320-121">Vous pouvez répéter les étapes 2 à 5 pour modifier la valeur pour le `DownloadConcurrency` paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="cf320-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="cf320-p103">Une fois que vous créez ou modifiez la `DownloadConcurrency` clé de Registre, veillez à créer une nouvelle tâche d’exportation ou redémarrer une tâche d’exportation existante pour les résultats de recherche ou les données que vous souhaitez télécharger. Voir la section [plus d’informations](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cf320-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="cf320-124">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="cf320-124">More information</span></span>

- <span data-ttu-id="cf320-p104">Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans cette procédure. Le `DownloadConcurrency` paramètre de Registre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg.</span><span class="sxs-lookup"><span data-stu-id="cf320-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="cf320-p105">L’outil d’exportation de découverte électronique Office 365 utilise l' [utilitaire AzCopy Azure](https://go.microsoft.com/fwlink/?linkid=849949) pour télécharger les données de recherche à partir de la sécurité &amp; centre de conformité ou d’eDiscovery avancée. Configuration de la `DownloadConcurrency` paramètre de Registre est similaire à l’aide du paramètre **/NC** lors de l’exécution de l’utilitaire AzCopy. Si le paramètre de Registre de `"DownloadConcurrency=24"` aurait le même effet que l’utilisation de la valeur du paramètre de `/NC:24` avec l’utilitaire AzCopy.</span><span class="sxs-lookup"><span data-stu-id="cf320-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="cf320-p106">Si vous arrêtez un téléchargement d’exportation qui est en cours, puis redémarrez (en essayant de télécharger à nouveau les résultats de recherche), l’outil d’exportation de découverte électronique Office 365 tente de reprendre le téléchargement même. Ainsi, si vous démarrez un téléchargement, arrêter, puis modifier la `DownloadConcurrency` Registre définition, le téléchargement probablement échouera si vous le redémarrer (en cliquant sur **Télécharger exporté les résultats**). Il s’agit, car l’outil d’exportation tente de reprendre le téléchargement précédent à l’aide des paramètres qui ne sont pas valides, car vous avez modifié le paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="cf320-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="cf320-p107">Par conséquent, après avoir modifié le `DownloadConcurrency` clé de Registre, n’oubliez pas de redémarrer la tâche d’exportation (en cliquant sur **redémarrer exportation**) de la sécurité &amp; centre de conformité. Vous pouvez télécharger les résultats exportés. Pour plus d’informations sur l’exportation de données et les résultats de la recherche, voir :</span><span class="sxs-lookup"><span data-stu-id="cf320-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="cf320-136">Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="cf320-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="cf320-137">Exporter les résultats dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="cf320-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    
