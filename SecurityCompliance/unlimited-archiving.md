---
title: Vue d’ensemble de l’archivage illimité dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: En savoir plus sur Développer automatiquement l’archivage dans Office 365, qui fournit un nombre illimité d’archivage pour les boîtes aux lettres Exchange Online.
ms.openlocfilehash: a762a0fb8295a645957404c1c88881f40329f7a1
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782121"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="4afab-103">Vue d’ensemble de l’archivage illimité dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4afab-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="4afab-p101">Dans Office 365, les boîtes aux lettres d’archive fournissent aux utilisateurs d’espace de stockage des boîtes aux lettres supplémentaires. Une fois que la boîte aux lettres de l’utilisateur archive est activé, jusqu'à 100 Go de stockage supplémentaire est disponible. Lorsque le quota de stockage de 100 Go est atteinte, les organisations devaient contacter Microsoft pour une demande d’espace de stockage supplémentaire pour une boîte aux lettres d’archive. Qui n’est plus le cas. La nouvelle fonctionnalité d’archivage illimitée dans Office 365 (appelée *Développer automatiquement l’archivage*) fournit un nombre illimité de stockage de boîtes aux lettres d’archive. Désormais, lorsque le quota de stockage dans la boîte aux lettres d’archive est atteinte, Office 365 augmente automatiquement la taille de l’archive, ce qui signifie que les utilisateurs ne seront pas exécutés en dehors de l’espace de stockage de boîtes aux lettres et les administrateurs ne doivent demander un stockage supplémentaire pour les boîtes aux lettres d’archive .</span><span class="sxs-lookup"><span data-stu-id="4afab-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="4afab-110">Pour obtenir des instructions pas à pas pour activer la développer automatiquement l’archivage, voir [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="4afab-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4afab-p102">Développer automatiquement l’archivage également prend en charge les boîtes aux lettres partagées. Pour activer l’archivage pour une boîte aux lettres partagée, une licence Exchange Online Plan 2 ou une licence Exchange Online Plan 1 avec une licence de l’archivage Exchange Online est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4afab-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="4afab-113">Fonctionnement de l’archivage comment développer automatiquement</span><span class="sxs-lookup"><span data-stu-id="4afab-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="4afab-p103">Comme expliqué précédemment, d’autres boîtes aux lettres d’espace de stockage est créé lors de la boîte aux lettres de l’utilisateur archive est activé. Lors de l’extension automatique d’archivage est activé, Office 365 vérifie périodiquement la taille de la boîte aux lettres d’archive. Lorsqu’une boîte aux lettres d’archive obtient a presque atteint sa limite de stockage, Office 365 crée automatiquement espace de stockage supplémentaire pour l’archive. Si l’utilisateur s’exécute en dehors de cet espace de stockage supplémentaire, Office 365 ajoute davantage d’espace de stockage pour l’archivage de l’utilisateur. Ce processus se produit automatiquement, ce qui signifie que les administrateurs ne peuvent pas demander d’archivage supplémentaires ou gérer développer automatiquement l’archivage.</span><span class="sxs-lookup"><span data-stu-id="4afab-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="4afab-119">Voici une vue d’ensemble rapide du processus.</span><span class="sxs-lookup"><span data-stu-id="4afab-119">Here's a quick overview of the process.</span></span>
  
![Vue d’ensemble du processus d’archivage automatique-développement](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="4afab-p104">L’archivage est activé pour une boîte aux lettres utilisateur ou d’une boîte aux lettres partagée. Une boîte aux lettres d’archive avec 100 Go d’espace de stockage est créé, et le quota d’avertissement pour la boîte aux lettres d’archive est défini sur 90 Go.</span><span class="sxs-lookup"><span data-stu-id="4afab-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="4afab-p105">Un administrateur permet de développer automatiquement l’archivage pour la boîte aux lettres. Puis, lorsque la boîte aux lettres d’archivage (y compris le dossier éléments récupérables) atteint 90 Go, il est converti en une archive développer automatiquement et Office 365 ajoute l’espace de stockage dans l’archive. Notez qu’il peut prendre jusqu'à 30 jours pour l’espace de stockage supplémentaire être mis en service.</span><span class="sxs-lookup"><span data-stu-id="4afab-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="4afab-126">Office 365 ajoute automatiquement l’espace de stockage dans l’archive lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4afab-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4afab-p106">Si une boîte aux lettres est mis en attente ou affecté à une stratégie de rétention d’Office 365, le quota de stockage pour les boîtes aux lettres d’archive est augmenté à 110 Go lorsque développer automatiquement l’archivage est activé. De même, le quota d’avertissement d’archivage est augmenté à 100 Go.</span><span class="sxs-lookup"><span data-stu-id="4afab-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="4afab-129">Quel est déplacé vers l’espace de stockage d’archive supplémentaires ?</span><span class="sxs-lookup"><span data-stu-id="4afab-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="4afab-p107">Pour optimiser l’utilisation du stockage d’archives développer automatiquement, les dossiers peuvent obtenir déplacés. Office 365 détermine quels dossiers sont déplacées lorsque stockage supplémentaire est ajouté à l’archive. Lorsqu’un dossier est déplacé, un sous-dossier est créé sous le dossier d’origine dans la partie de l’archive de la liste des dossiers dans Outlook. Ce nouveau sous-dossier pointe vers les éléments qui ont été déplacés. La convention d’affectation de noms par Office 365 pour nommer ce dossier est ** \<nom du dossier\>_yyyy (imposée mmm jj, aaaa h_mm)**, où :</span><span class="sxs-lookup"><span data-stu-id="4afab-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="4afab-135">**aaaa** est l’année que les messages dans le dossier ont été reçus.</span><span class="sxs-lookup"><span data-stu-id="4afab-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="4afab-136">**mmm jj, aaaa h_m** est la date et l’heure auxquelles le sous-dossier a été créé par Office 365, au format UTC, en fonction du fuseau horaire de l’utilisateur et les paramètres régionaux dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="4afab-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="4afab-137">Les captures d’écran suivante affiche une liste de dossiers avant et après que les messages sont déplacés dans une archive développé automatique.</span><span class="sxs-lookup"><span data-stu-id="4afab-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="4afab-138">**Avant de stockage supplémentaire est ajouté.**</span><span class="sxs-lookup"><span data-stu-id="4afab-138">**Before additional storage is added**</span></span>
  
![Liste des dossiers de boîte aux lettres de l’archivage avant de développer automatiquement une archive est mis en service](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="4afab-140">**Après l’ajout d’espace de stockage supplémentaire**</span><span class="sxs-lookup"><span data-stu-id="4afab-140">**After additional storage is added**</span></span>
  
![Liste des dossiers de boîte aux lettres de l’archive après que développer automatiquement une archive est mis en service](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="4afab-142">Conditions requises pour Outlook pour accéder aux éléments dans une archive développé automatique</span><span class="sxs-lookup"><span data-stu-id="4afab-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="4afab-143">Pour accéder aux messages qui sont stockés dans une archive développé automatique, les utilisateurs doivent employer un des clients Outlook suivants :</span><span class="sxs-lookup"><span data-stu-id="4afab-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="4afab-144">Outlook 2016 pour Windows</span><span class="sxs-lookup"><span data-stu-id="4afab-144">Outlook 2016 for Windows</span></span>
    
- <span data-ttu-id="4afab-145">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="4afab-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="4afab-146">Outlook 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="4afab-146">Outlook 2016 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4afab-p108">Les utilisateurs Outlook 2013 peuvent uniquement accéder aux éléments qui ont été stockés à l’origine dans leur boîte aux lettres d’archive. Ils ne pourront pour accéder aux éléments qui sont déplacés vers un stockage d’archives supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4afab-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="4afab-149">Voici quelques éléments à prendre en compte lors de l’utilisation d’Outlook ou Outlook sur le web pour accéder aux messages stockés dans une archive développé automatique.</span><span class="sxs-lookup"><span data-stu-id="4afab-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="4afab-150">Vous pouvez accéder de n’importe quel dossier dans votre boîte aux lettres archive, y compris celles qui ont été déplacés vers la zone de stockage étendu automatique.</span><span class="sxs-lookup"><span data-stu-id="4afab-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="4afab-p109">Vous pouvez rechercher des éléments qui ont été déplacés vers une zone de stockage supplémentaire qu’en recherchant le dossier lui-même. Cela signifie que vous devez sélectionner le dossier d’archivage dans la liste des dossiers pour sélectionner l’option de **Dossier actif** en tant que l’étendue de recherche. De même, si un dossier dans une zone de stockage étendu automatique contient des sous-dossiers, vous devez rechercher chaque sous-dossier séparément.</span><span class="sxs-lookup"><span data-stu-id="4afab-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="4afab-154">Élément de compte dans Outlook et lu/des nombres (dans Outlook et Outlook sur le web) dans une archive développé automatique peuvent ne pas être précis.</span><span class="sxs-lookup"><span data-stu-id="4afab-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="4afab-155">Vous pouvez supprimer des éléments dans un sous-dossier qui pointe vers une zone de stockage étendu automatique, mais le dossier lui-même ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="4afab-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="4afab-156">Vous ne pouvez pas utiliser la fonctionnalité récupérer les éléments supprimés pour récupérer un élément a été supprimé d’une zone de stockage étendu automatique.</span><span class="sxs-lookup"><span data-stu-id="4afab-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="4afab-157">Développer automatiquement l’archivage et autres fonctionnalités de conformité d’Office 365</span><span class="sxs-lookup"><span data-stu-id="4afab-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="4afab-158">Cette section décrit la relation entre développer automatiquement l’archivage conformité Office 365 et autres fonctionnalités de gouvernance des données.</span><span class="sxs-lookup"><span data-stu-id="4afab-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="4afab-159">**découverte électronique** - lorsque vous utilisez un outil de découverte électronique Office 365, tels que de la recherche de contenu ou In-Place eDiscovery, les zones de stockage supplémentaire dans une archive développé automatique sont inclus dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="4afab-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="4afab-160">**Rétention** - lorsque vous mettre en attente une boîte aux lettres dans Exchange Online à l’aide des outils tels que litige ou en cas de découverte électronique contient et stratégies de rétention de sécurité Office 365 &amp; centre de conformité, le contenu situé dans une archive développé automatique est également mis en attente.</span><span class="sxs-lookup"><span data-stu-id="4afab-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security &amp; Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="4afab-161">**Messagerie (MRM) de gestion des enregistrements** - si vous utilisez des stratégies de suppression de MRM dans Exchange Online pour supprimer définitivement les éléments de boîte aux lettres ayant expiré, éléments arrivés à expiration situés dans l’archive de développé automatique seront également supprimés.</span><span class="sxs-lookup"><span data-stu-id="4afab-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="4afab-p110">**Importer le service** - vous pouvez utiliser le service Office 365 importer pour importer des fichiers PST vers l’archive de développé automatique d’un utilisateur. Vous pouvez importer jusqu'à 100 Go de données à partir des fichiers PST boîte aux lettres d’archive de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4afab-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="4afab-164">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="4afab-164">More information</span></span>

<span data-ttu-id="4afab-165">Pour obtenir des informations sur l’extension automatique d’archivage, consultez la rubrique [Office 365 : Forum aux questions des Archives développer automatiquement](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span><span class="sxs-lookup"><span data-stu-id="4afab-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>