---
title: Vue d'ensemble d'un archivage illimité dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Découvrez la croissance automatique de l'archivage dans Office 365, qui offre un stockage d'archive illimité pour les boîtes aux lettres Exchange Online.
ms.openlocfilehash: 4ed1260cdf348d0bd29d88952ab69d234f044c26
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296647"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="b9c6a-103">Vue d'ensemble d'un archivage illimité dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c6a-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="b9c6a-p101">Dans Office 365, les boîtes aux lettres d'archivage fournissent aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire. Une fois la boîte aux lettres d'archivage d'un utilisateur activée, jusqu'à 100 Go d'espace de stockage supplémentaire est disponible. Lorsque le quota de stockage de 100 Go est atteint, les organisations devaient contacter Microsoft pour demander un espace de stockage supplémentaire pour une boîte aux lettres d'archivage. Cela n'est plus le cas. La nouvelle fonctionnalité d'archivage illimitée dans Office 365 (appelée *archivage à extension automatique*) offre une quantité illimitée de stockage dans les boîtes aux lettres d'archivage. À présent, lorsque le quota de stockage dans la boîte aux lettres d'archivage est atteint, Office 365 augmente automatiquement la taille de l'archive, ce qui signifie que les utilisateurs ne peuvent pas manquer d'espace de stockage de boîte aux lettres et que les administrateurs n'ont pas à demander un stockage supplémentaire pour les boîtes aux lettres d'archivage. .</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="b9c6a-110">Pour obtenir des instructions détaillées sur l'activation de l'archivage à extension automatique, consultez la rubrique [activation de l'archivage illimité dans Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="b9c6a-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b9c6a-p102">L'archivage à extension automatique prend également en charge les boîtes aux lettres partagées. Pour activer l'archivage pour une boîte aux lettres partagée, une licence Exchange Online plan 2 ou une licence Exchange Online plan 1 avec une licence d'archivage Exchange Online est requise.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="b9c6a-113">Fonctionnement de l'archivage en développement automatique</span><span class="sxs-lookup"><span data-stu-id="b9c6a-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="b9c6a-p103">Comme expliqué précédemment, un espace de stockage de boîte aux lettres supplémentaire est créé lorsque la boîte aux lettres d'archivage d'un utilisateur est activée. Lorsque l'archivage à extension automatique est activé, Office 365 vérifie régulièrement la taille de la boîte aux lettres d'archivage. Lorsqu'une boîte aux lettres d'archivage est proche de sa limite de stockage, Office 365 crée automatiquement un espace de stockage supplémentaire pour l'archive. Si l'utilisateur manque d'espace de stockage supplémentaire, Office 365 ajoute davantage d'espace de stockage à l'archive de l'utilisateur. Ce processus se produit automatiquement, ce qui signifie que les administrateurs n'ont pas besoin de demander un stockage d'archivage supplémentaire ou de gérer l'archivage à extension automatique.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="b9c6a-119">Voici une présentation rapide du processus.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-119">Here's a quick overview of the process.</span></span>
  
![Vue d'ensemble du processus d'archivage à extension automatique](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="b9c6a-p104">L'archivage est activé pour une boîte aux lettres d'utilisateur ou une boîte aux lettres partagée. Une boîte aux lettres d'archivage de 100 Go d'espace de stockage est créée et le quota d'avertissement pour la boîte aux lettres d'archivage est défini sur 90 Go.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="b9c6a-p105">Un administrateur permet l'archivage à extension automatique pour la boîte aux lettres. Ensuite, lorsque la boîte aux lettres d'archivage (y compris le dossier éléments récupérables) atteint 90 Go, elle est convertie en une archive à extension automatique et Office 365 ajoute de l'espace de stockage à l'archive. Notez que le temps de mise en service de l'espace de stockage supplémentaire peut prendre jusqu'à 30 jours.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="b9c6a-126">Office 365 ajoute automatiquement davantage d'espace de stockage à l'archive lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b9c6a-p106">Si une boîte aux lettres est placée en conservation ou affectée à une stratégie de rétention Office 365, le quota de stockage du maibox d'archivage est augmenté de 110 Go lorsque l'archivage à extension automatique est activé. De même, le quota d'avertissement d'archivage est porté à 100 Go.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="b9c6a-129">Qu'est-ce qui est déplacé vers l'espace de stockage d'archive supplémentaire?</span><span class="sxs-lookup"><span data-stu-id="b9c6a-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="b9c6a-p107">Pour utiliser efficacement le stockage d'archives à extension automatique, les dossiers peuvent être déplacés. Office 365 détermine quels dossiers sont déplacés lorsque du stockage supplémentaire est ajouté à l'archive. Lorsqu'un dossier est déplacé, un sous-dossier est automatiquement créé sous le dossier d'origine dans la partie Archive de la liste des dossiers dans Outlook. Ce nouveau sous-dossier pointe vers les éléments qui ont été déplacés. la convention d'affectation de noms utilisée par Office 365 pour nommer ce dossier est \*\* \<le nom\>de dossier _yyyy (créé sur mmm dd, yyyy h_mm)\*\*, où:</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="b9c6a-135">**yyyy** est l'année de réception des messages dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="b9c6a-136">**MMM DD, yyyy h_m** est la date et l'heure auxquelles le sous-dossier a été créé par Office 365, au format UTC, basé sur le fuseau horaire et les paramètres régionaux de l'utilisateur dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="b9c6a-137">Les captures d'écran suivantes montrent une liste des dossiers avant et après le déplacement des messages dans une archive étendue automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="b9c6a-138">**Avant l'ajout d'un espace de stockage supplémentaire**</span><span class="sxs-lookup"><span data-stu-id="b9c6a-138">**Before additional storage is added**</span></span>
  
![Liste des dossiers de la boîte aux lettres d'archivage avant la mise en service de l'archive à extension automatique](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="b9c6a-140">**Après l'ajout d'un espace de stockage supplémentaire**</span><span class="sxs-lookup"><span data-stu-id="b9c6a-140">**After additional storage is added**</span></span>
  
![Liste des dossiers de la boîte aux lettres d'archivage après mise en service de l'archive à extension automatique](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="b9c6a-142">Conditions requises par Outlook pour accéder aux éléments dans une archive étendue automatiquement</span><span class="sxs-lookup"><span data-stu-id="b9c6a-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="b9c6a-143">Pour accéder aux messages stockés dans une archive étendue automatiquement, les utilisateurs doivent utiliser l'un des clients Outlook suivants:</span><span class="sxs-lookup"><span data-stu-id="b9c6a-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="b9c6a-144">Outlook 2016 ou Outlook 2019 pour Windows</span><span class="sxs-lookup"><span data-stu-id="b9c6a-144">Outlook 2016 or Outlook 2019 for Windows</span></span>
    
- <span data-ttu-id="b9c6a-145">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="b9c6a-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="b9c6a-146">Outlook 2016 ou Outlook 2019 pour Mac</span><span class="sxs-lookup"><span data-stu-id="b9c6a-146">Outlook 2016 or Outlook 2019 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="b9c6a-p108">Les utilisateurs d'Outlook 2013 peuvent uniquement accéder aux éléments qui étaient initialement stockés dans leur boîte aux lettres d'archivage. Ils ne pourront pas accéder aux éléments déplacés vers un stockage d'archivage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="b9c6a-149">Voici quelques éléments à prendre en compte lors de l'utilisation d'Outlook ou d'Outlook sur le Web pour accéder aux messages stockés dans un archivage développé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="b9c6a-150">Vous pouvez accéder à n'importe quel dossier de votre boîte aux lettres d'archivage, y compris ceux qui ont été déplacés vers la zone de stockage étendu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="b9c6a-p109">Vous pouvez rechercher des éléments qui ont été déplacés vers une zone de stockage supplémentaire uniquement en effectuant une recherche dans le dossier proprement dit. Cela signifie que vous devez sélectionner le dossier d'archivage dans la liste des dossiers pour sélectionner l'option **dossier actif** comme étendue de recherche. De même, si un dossier d'une zone de stockage à extension automatique contient des sous-dossiers, vous devez effectuer une recherche dans chaque sous-dossier séparément.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="b9c6a-154">Le nombre d'éléments dans Outlook et le nombre de lectures/non de lectures (dans Outlook et Outlook sur le Web) dans une archive étendue automatiquement peuvent ne pas être précis.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="b9c6a-155">Vous pouvez supprimer des éléments dans un sous-dossier qui pointe vers une zone de stockage à extension automatique, mais le dossier proprement dit ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="b9c6a-156">Vous ne pouvez pas utiliser la fonctionnalité récupérer les éléments supprimés pour récupérer un élément qui a été supprimé d'une zone de stockage à extension automatique.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="b9c6a-157">Extension de l'archivage et autres fonctionnalités de conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c6a-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="b9c6a-158">Cette section décrit la fonctionnalité entre l'archivage et les autres fonctionnalités de conformité et de gouvernance des données Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="b9c6a-159">**découverte électronique** : lorsque vous utilisez un outil ediscovery Office 365, tel que la recherche de contenu ou la découverte électronique inaltérable, les zones de stockage supplémentaires dans une archive étendue automatiquement sont également recherchées.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="b9c6a-160">\*\*\*\* Rétention: lorsque vous placez une boîte aux lettres en conservation à l'aide d'outils comme la conservation pour litige dans Exchange Online ou de stratégies de rétention de cas eDiscovery dans le centre de sécurité &, le contenu situé dans un archivage développé automatiquement est également mis en attente.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security & Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="b9c6a-161">**Gestion des enregistrements de messagerie (MRM)** : Si vous utilisez des stratégies de suppression MRM dans Exchange Online pour supprimer définitivement des éléments de boîte aux lettres expirés, les éléments expirés situés dans l'archive étendue automatiquement seront également supprimés.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="b9c6a-p110">**Import service** : vous pouvez utiliser le service d'importation Office 365 pour importer des fichiers PST dans l'archive étendue automatiquement. Vous pouvez importer jusqu'à 100 Go de données à partir de fichiers PST vers la boîte aux lettres d'archivage de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="b9c6a-164">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b9c6a-164">More information</span></span>

<span data-ttu-id="b9c6a-165">Pour plus d'informations techniques sur l'archivage à extension automatique, consultez la rubrique [Office 365: Forum aux questions](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)sur les archives.</span><span class="sxs-lookup"><span data-stu-id="b9c6a-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>