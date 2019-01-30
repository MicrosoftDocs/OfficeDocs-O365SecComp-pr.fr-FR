---
title: Indexation de données dépositaire avancée
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
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607648"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="e8eb9-102">Indexation de données dépositaire avancée</span><span class="sxs-lookup"><span data-stu-id="e8eb9-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="e8eb9-p101">Lorsqu’un dépositaire est ajouté à une affaire eDiscovery avancées (Preview), n’importe quel contenu dans Office 365 qui était considéré comme partiellement indexé est de transformation pour le rendre entièrement modifiable.  Ce processus est appelé *indexation avancée*. Contenu peut être indexé partiellement pour plusieurs raisons, y compris l’existence des images, des types de fichiers non pris en charge ou lorsque les limites de taille de fichier d’indexation rencontrés.  Pour en savoir plus sur les éléments indexés partiellement, voir [partiellement indexé des éléments de la recherche de contenu dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="e8eb9-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="e8eb9-107">Affichage des résultats d’indexation avancées</span><span class="sxs-lookup"><span data-stu-id="e8eb9-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="e8eb9-p102">Une fois le processus d’indexation avancé terminé, vous pouvez obtenir une bonne compréhension de l’efficacité de traiter à nouveau.  Dans la vue dépositaire l’indexation, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.  L’index de hybride est où eDiscovery avancée (Preview) stocke le contenu nouveau traité.</span><span class="sxs-lookup"><span data-stu-id="e8eb9-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="e8eb9-p103">Le graphique inclut également le nombre d’éléments qui nécessitent une conversion et une autre graphique d’erreurs par type de fichier. Pour plus d’informations, voir [correction d’erreur lors du traitement des données](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="e8eb9-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="e8eb9-113">Mise à jour des index avancées pour dépositaires</span><span class="sxs-lookup"><span data-stu-id="e8eb9-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="e8eb9-p104">Lorsqu’un dépositaire est ajouté à une affaire eDiscovery avancées (Preview), tous les éléments indexés partiellement sont nouveau traités. Toutefois, avec le temps, les éléments indexés plus partiellement peuvent être ajoutés à un compte d’utilisateur boîte aux lettres ou OneDrive.  Si nécessaire, vous pouvez mettre à jour les index.</span><span class="sxs-lookup"><span data-stu-id="e8eb9-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="e8eb9-p105">Mise à jour des index dépositaire est un processus long. Il est recommandé de ne pas mettre index plusieurs fois par jour dans un cas.</span><span class="sxs-lookup"><span data-stu-id="e8eb9-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
