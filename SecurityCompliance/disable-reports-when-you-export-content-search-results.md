---
title: Désactiver les rapports lorsque vous exportez des résultats de la recherche de contenu de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Modifiez le Registre de Windows sur votre ordinateur local pour désactiver les rapports lorsque vous exportez les résultats d’une recherche de contenu à partir de la sécurité de 365 Office &amp; Comliance centre. Désactivation de ces rapports, vous pouvez accélérer le temps de téléchargement et économiser de l’espace disque.
ms.openlocfilehash: 3c09e0563ddd4469f21950dc3a698ce08b0014df
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528628"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="a433c-104">Désactiver les rapports lorsque vous exportez des résultats de la recherche de contenu de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a433c-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="a433c-p102">Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour exporter les résultats d’une recherche de contenu dans la sécurité &amp; centre de conformité, l’outil crée automatiquement et exporte les deux rapports qui contiennent des informations supplémentaires sur le contenu exporté. Ces rapports sont le fichier Results.csv et le fichier Manifest.xml (voir la section [Forum aux questions sur la désactivation d’exporter des rapports](#frequently-asked-questions-about-disabling-export-reports) dans cette rubrique pour obtenir des descriptions détaillées de ces rapports). Étant donné que ces fichiers peuvent être très volumineux, vous pouvez accélérer le temps de téléchargement et économiser de l’espace disque en empêchant l’exportation de ces fichiers. Vous pouvez procéder en modifiant le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de recherche. Si vous souhaitez inclure les rapports à une date ultérieure, vous pouvez modifier le paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="a433c-p102">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content. These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports). Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported. You can do this by changing the Windows Registry on the computer that you use to export the search results. If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="a433c-110">Créer des paramètres de Registre pour désactiver les rapports d’exportation</span><span class="sxs-lookup"><span data-stu-id="a433c-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="a433c-111">Effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour exporter les résultats à une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="a433c-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="a433c-112">Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="a433c-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="a433c-113">Effectuez une ou les deux étapes suivantes, en fonction de rapport d’exportation que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="a433c-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="a433c-114">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="a433c-114">**Results.csv**</span></span>
    
      <span data-ttu-id="a433c-115">Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, DisableResultsCsv.reg.</span><span class="sxs-lookup"><span data-stu-id="a433c-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="a433c-116">**Manifest.Xml**</span><span class="sxs-lookup"><span data-stu-id="a433c-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="a433c-117">Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier de .reg ; par exemple, DisableManifestXml.reg.</span><span class="sxs-lookup"><span data-stu-id="a433c-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="a433c-118">Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur le fichier .reg que vous avez créée lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="a433c-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="a433c-119">Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification.</span><span class="sxs-lookup"><span data-stu-id="a433c-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="a433c-120">Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="a433c-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="a433c-121">L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.</span><span class="sxs-lookup"><span data-stu-id="a433c-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="a433c-122">Modifier les paramètres de Registre pour réactiver l’exportation des rapports</span><span class="sxs-lookup"><span data-stu-id="a433c-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="a433c-p103">Si vous avez désactivé les rapports Results.csv et Manifest.xml en créant les fichiers .reg dans la procédure précédente, vous pouvez modifier ces fichiers pour réactiver un rapport afin qu’il est exporté avec les résultats de recherche. Là encore, effectuez la procédure suivante sur l’ordinateur que vous utiliserez pour exporter les résultats à une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="a433c-p103">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results. Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="a433c-125">Fermez l’outil d’exportation de découverte électronique Office 365 si elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="a433c-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="a433c-126">Modification des modification des fichiers .reg que vous avez créé dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="a433c-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="a433c-127">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="a433c-127">**Results.csv**</span></span>
    
        <span data-ttu-id="a433c-p104">Ouvrir le fichier DisableResultsCsv.reg dans le bloc-notes, modifiez la valeur `False` à `True`, puis enregistrez le fichier. Par exemple, une fois que vous avez modifié le fichier, il ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="a433c-p104">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="a433c-130">**Manifest.Xml**</span><span class="sxs-lookup"><span data-stu-id="a433c-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="a433c-p105">Ouvrir le fichier DisableManifestXml.reg dans le bloc-notes, modifiez la valeur `False` à `True`, puis enregistrez le fichier. Par exemple, une fois que vous avez modifié le fichier, il ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="a433c-p105">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="a433c-133">Dans l’Explorateur Windows, cliquez sur ou double-cliquez sur un fichier .reg que vous avez modifié à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="a433c-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="a433c-134">Dans la fenêtre de contrôle d’accès utilisateur, cliquez sur **Oui** pour laisser l’Éditeur du Registre que la modification.</span><span class="sxs-lookup"><span data-stu-id="a433c-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="a433c-135">Lorsque vous y êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="a433c-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="a433c-136">L’Éditeur du Registre affiche un message indiquant que le paramètre a été correctement ajouté au Registre.</span><span class="sxs-lookup"><span data-stu-id="a433c-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="a433c-137">Forum aux questions sur la désactivation des rapports d’exportation</span><span class="sxs-lookup"><span data-stu-id="a433c-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="a433c-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="a433c-138"></span></span>

 <span data-ttu-id="a433c-139">**Quels sont les rapports Results.csv et Manifest.xml ?**</span><span class="sxs-lookup"><span data-stu-id="a433c-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="a433c-140">Les fichiers Manifest.xml et les Results.csv contiennent plus d’informations sur le contenu qui a été exporté.</span><span class="sxs-lookup"><span data-stu-id="a433c-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="a433c-p106">**Results.csv** document Microsoft Excel qui contient des informations sur chaque élément qui peut être téléchargé comme un résultat de recherche. Pour le courrier électronique, le journal de résultat contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="a433c-p106">**Results.csv** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="a433c-143">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="a433c-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="a433c-144">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="a433c-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="a433c-145">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="a433c-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="a433c-146">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="a433c-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="a433c-p107">Si le message est un message en double si vous avez activé la déduplication lors de l’exportation des résultats de la recherche. Les messages en double aura une valeur dans la colonne **Parent ItemId** qui identifie le message comme un doublon. La valeur dans la colonne **ID d’élément Parent** est identique à la valeur dans la colonne **DocumentId élément** du message qui a été exporté.</span><span class="sxs-lookup"><span data-stu-id="a433c-p107">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results. Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate. The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="a433c-150">Pour les documents à partir de SharePoint et OneDrive pour les sites de l’entreprise, le journal de résultat contient des informations sur tous les documents, y compris :</span><span class="sxs-lookup"><span data-stu-id="a433c-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="a433c-151">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="a433c-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="a433c-152">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="a433c-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="a433c-153">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="a433c-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="a433c-154">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="a433c-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="a433c-p108">Un manifest fichier **manifest.XML** (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de recherche. Les informations contenues dans cet état sont identique à l’état Results.csv, mais il est au format spécifié par le modèle de référence découverte électronique (EDRM). Pour plus d’informations sur EDRM, accédez à [https://www.edrm.net](https://www.edrm.net).</span><span class="sxs-lookup"><span data-stu-id="a433c-p108">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results. The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM). For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="a433c-158">**Quand dois-je désactiver exportation ces rapports ?**</span><span class="sxs-lookup"><span data-stu-id="a433c-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="a433c-p109">Cela dépend de vos besoins spécifiques. Bon nombre d’organisations ne nécessite pas plus d’informations sur les résultats de la recherche et n’avez pas besoin de ces rapports.</span><span class="sxs-lookup"><span data-stu-id="a433c-p109">It depends on your specific needs. Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="a433c-161">**Quel ordinateur dois-je faire ?**</span><span class="sxs-lookup"><span data-stu-id="a433c-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="a433c-162">Vous devez modifier le paramètre de Registre sur un ordinateur local que vous exécutez l’outil d’exportation de découverte électronique Office 365 sur.</span><span class="sxs-lookup"><span data-stu-id="a433c-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="a433c-163">**Après modification de ce paramètre, dois-je redémarrer l’ordinateur ?**</span><span class="sxs-lookup"><span data-stu-id="a433c-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="a433c-p110">Non, vous n’êtes pas obligé de redémarrer l’ordinateur. Mais si l’outil d’exportation de découverte électronique Office 365 est en cours d’exécution, vous devez fermer, puis redémarrez après avoir modifié le paramètre de Registre.</span><span class="sxs-lookup"><span data-stu-id="a433c-p110">No, you don't have to restart the computer. But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="a433c-166">**Est une clé de Registre existante obtenir modifiée ou est une nouvelle clé sont créée ?**</span><span class="sxs-lookup"><span data-stu-id="a433c-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="a433c-p111">Une nouvelle clé de Registre est créée la première fois que vous exécutez le fichier .reg que vous avez créé dans la procédure décrite dans cette rubrique. Puis le paramètre est modifié à chaque fois que vous modifiez et réexécutez la modifier le fichier .reg.</span><span class="sxs-lookup"><span data-stu-id="a433c-p111">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
