---
title: Indexation avancée des données des consignataires
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218664"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="d6ee3-102">Indexation avancée des données des consignataires</span><span class="sxs-lookup"><span data-stu-id="d6ee3-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="d6ee3-p101">Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tout contenu dans Office 365 considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.  Ce processus est appelé *indexation avancée*. Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l'existence d'images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d'indexation sont rencontrées.  Pour en savoir plus sur les éléments partiellement indexés, consultez la rubrique [éléments partiellement indexés dans la recherche de contenu dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="d6ee3-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="d6ee3-107">Affichage des résultats de l'indexation avancée</span><span class="sxs-lookup"><span data-stu-id="d6ee3-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="d6ee3-p102">Une fois le processus d'indexation avancé terminé, vous pouvez comprendre l'efficacité du nouveau traitement.  Dans la vue d'indexation dépositaire, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.  L'index hybride est l'emplacement où Advanced eDiscovery (aperçu) stocke le contenu retraité.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="d6ee3-p103">Le graphique inclut également le nombre d'éléments nécessitant une correction et un autre graphique d'erreurs par type de fichier. Pour plus d'informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="d6ee3-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="d6ee3-113">Mise à jour des index avancés pour les dépositaires</span><span class="sxs-lookup"><span data-stu-id="d6ee3-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="d6ee3-p104">Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tous les éléments partiellement indexés sont ré-traités. Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d'un utilisateur.  Si nécessaire, vous pouvez mettre à jour les index.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="d6ee3-p105">La mise à jour des index de dépositaire est un processus de longue durée. Il est recommandé de ne pas mettre à jour les index plus d'une fois par jour dans un cas.</span><span class="sxs-lookup"><span data-stu-id="d6ee3-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
