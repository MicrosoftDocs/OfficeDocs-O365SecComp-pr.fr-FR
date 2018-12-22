---
title: Suppression de données en ligne Office 365 SharePoint
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Explication de la suppression des données dans SharePoint Online.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411160"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="d0372-103">Suppression de données en ligne SharePoint dans Office 365</span><span class="sxs-lookup"><span data-stu-id="d0372-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="d0372-p101">SharePoint Online stocke les objets en tant que code abstrait au sein des bases de données application. Lorsqu’un utilisateur télécharge un fichier dans SharePoint Online, ce fichier est dissocié et converti en code d’application et stocké dans plusieurs tableaux sur plusieurs bases de données. Dans SharePoint Online, tout le contenu qui télécharge un client est divisé en segments, chiffrés (potentiellement avec plusieurs clés AES 256 bits) et réparti sur le centre de données. Pour plus d’informations spécifiques à propos du processus de segmentation et le chiffrement, voir [chiffrement dans le nuage de Microsoft](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0372-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="d0372-p102">Dans SharePoint Online, les éléments sont conservés pendant jours 93 depuis le moment où que vous les supprimer de leur emplacement d’origine. Ils restent dans la Corbeille du site toute la durée, à moins que quelqu'un les supprime à partir de là, ou vide que Corbeille. Dans ce cas, les éléments accédez à la collection de sites Corbeille, où qu’ils restent pour le reste des jours 93. Pour obtenir des informations sur la restauration d’éléments supprimés, voir [restaurer des éléments dans la Corbeille d’un site SharePoint](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) et [restaurer les éléments supprimés de la Corbeille de collection de sites](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). La durée de rétention Corbeille n’est pas configurable dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="d0372-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="d0372-113">Lorsque vous supprimez une collection de sites, vous êtes également supprimer la hiérarchie de sites dans la collection et tout le contenu au sein de celles-ci :</span><span class="sxs-lookup"><span data-stu-id="d0372-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="d0372-114">les documents et bibliothèques de documents ;</span><span class="sxs-lookup"><span data-stu-id="d0372-114">Documents and document libraries</span></span>
- <span data-ttu-id="d0372-115">Listes et données de liste</span><span class="sxs-lookup"><span data-stu-id="d0372-115">Lists and list data</span></span>
- <span data-ttu-id="d0372-116">Paramètres de configuration de site</span><span class="sxs-lookup"><span data-stu-id="d0372-116">Site configuration settings</span></span>
- <span data-ttu-id="d0372-117">Informations de rôle et de sécurité liées au site ou ses sous-sites</span><span class="sxs-lookup"><span data-stu-id="d0372-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="d0372-118">Sous-sites du site Web, leur contenu et l’utilisateur informations niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="d0372-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="d0372-119">Si vous supprimez par inadvertance une collection de sites, il peut être restauré par un global ou SharePoint admin à l’aide du centre d’administration de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d0372-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="d0372-p103">Disque dur suppression se produit lorsqu’un utilisateur purge des éléments supprimés de la collection de sites Corbeille, lorsque les périodes de rétention et sauvegarde arrivent à expiration, ou lorsqu’un administrateur supprime définitivement une collection de sites à l’aide de l’applet de [commande Remove-SPODeletedSite](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). Lorsqu’un utilisateur dur supprime (supprime définitivement ou purge) contenu dans SharePoint Online, la toutes les clés de chiffrement pour les segments supprimés sont également supprimés. Les blocs sur les disques qui précédemment stockées les segments supprimés sont marqués comme étant inutilisée et disponible pour les réutiliser.</span><span class="sxs-lookup"><span data-stu-id="d0372-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
