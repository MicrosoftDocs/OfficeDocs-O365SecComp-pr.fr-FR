---
title: Afficher des documents dans un ensemble de travail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: ''
ms.openlocfilehash: 1502308fab4f27ed9e93e1dff204bdddf6ae726e
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357455"
---
# <a name="view-documents-in-a-working-set"></a><span data-ttu-id="60fb4-102">Afficher des documents dans un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="60fb4-102">View documents in a working set</span></span>

<span data-ttu-id="60fb4-p101">Advanced eDiscovery (préversion) affiche du contenu à l'aide de plusieurs observateurs à des fins différentes. Les différentes visionneuses peuvent être utilisées en cliquant sur n'importe quel document d'une plage de travail. Les visionneuses actuellement fournies sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="60fb4-p101">Advanced eDiscovery (Preview) displays content via several viewers each with different purposes. The various viewers can be used by clicking on any document within a working set. The viewers currently provided are:</span></span>

- <span data-ttu-id="60fb4-106">Métadonnées de fichier  
</span><span class="sxs-lookup"><span data-stu-id="60fb4-106">File metadata</span></span>
- <span data-ttu-id="60fb4-107">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="60fb4-107">Native view</span></span>
- <span data-ttu-id="60fb4-108">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="60fb4-108">Text view</span></span>
- <span data-ttu-id="60fb4-109">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="60fb4-109">Annotate view</span></span>
- <span data-ttu-id="60fb4-110">Vue conVertie</span><span class="sxs-lookup"><span data-stu-id="60fb4-110">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="60fb4-111">Métadonnées de fichier  
</span><span class="sxs-lookup"><span data-stu-id="60fb4-111">File metadata</span></span>

<span data-ttu-id="60fb4-p102">Ce panneau peut être activé/désactivé pour afficher diverses métadonnées associées au document. Bien que la grille des résultats de la recherche puisse être personnalisée pour afficher des métadonnées spécifiques, il peut s'avérer difficile de faire défiler horizontalement les données lors de la révision des données. Le panneau métadonnées de fichier permet à un utilisateur de basculer sur une vue dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="60fb4-p102">This panel can be toggled on/off to display various metadata associated with the document. Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data. The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="60fb4-115">Panneau métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="60fb4-115">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="60fb4-116">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="60fb4-116">Native view</span></span>

<span data-ttu-id="60fb4-p103">La visionneuse Native affiche l'affichage le plus enrichi d'un document. Il prend en charge des centaines de types de fichiers et permet d'afficher l'expérience la plus réelle vers Native possible. Pour les fichiers Microsoft Office, par exemple, la visionneuse exploite Office Online pour afficher du contenu tel que des commentaires de document, des formules Excel, des lignes/colonnes masquées, des notes PowerPoint, etc. Pour plus d'informations sur les visionneuses Office Online, \[reportez-vous à l'article suivant:\]</span><span class="sxs-lookup"><span data-stu-id="60fb4-p103">The Native viewer displays the richest view of a document. It supports hundreds of file types and is meant to display the truest to native experience possible. For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="60fb4-120">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="60fb4-120">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="60fb4-121">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="60fb4-121">Text view</span></span>

<span data-ttu-id="60fb4-p104">La visionneuse de texte fournit une vue du texte extrait d'un fichier. Elle ignore toutes les images incorporées et la mise en forme, mais elle est très performante si un utilisateur tente de comprendre le contenu rapidement. L'affichage de texte comprend également d'autres fonctionnalités:</span><span class="sxs-lookup"><span data-stu-id="60fb4-p104">The Text viewer provides a view of the extracted text of a file. It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly. Text view also includes other features:</span></span>

  - <span data-ttu-id="60fb4-125">Le compteur de ligne facilite la référence à des parties spécifiques d'un document.</span><span class="sxs-lookup"><span data-stu-id="60fb4-125">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="60fb4-126">Mise en surbrillance des résultats de recherche, qui met en surbrillance les termes dans le document, ainsi que la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="60fb4-126">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="60fb4-127">L'affichage diff fournit un affichage de comparaison qui met en surbrillance les différences textuelles lors de l'affichage des documents en double.</span><span class="sxs-lookup"><span data-stu-id="60fb4-127">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="60fb4-128">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="60fb4-128">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="60fb4-129">Vue diff</span><span class="sxs-lookup"><span data-stu-id="60fb4-129">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="60fb4-130">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="60fb4-130">Annotate view</span></span>

<span data-ttu-id="60fb4-131">L'affichage anNoted propose des fonctionnalités qui permettent aux utilisateurs d'appliquer un balisage à un document, notamment:</span><span class="sxs-lookup"><span data-stu-id="60fb4-131">The Annotate view provides features that allow users to apply markup on a document including:</span></span>

  - <span data-ttu-id="60fb4-132">Zone Redactions: les utilisateurs peuvent dessiner un cadre sur le document afin de masquer le contenu sensible</span><span class="sxs-lookup"><span data-stu-id="60fb4-132">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="60fb4-133">Crayon: les utilisateurs peuvent effectuer un dessin à main levée sur un document afin d'attirer l'attention sur certaines parties d'un document.</span><span class="sxs-lookup"><span data-stu-id="60fb4-133">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="60fb4-134">Sélectionner les annotations: les utilisateurs peuvent sélectionner des annotations dans un document afin de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="60fb4-134">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="60fb4-135">Activer/désactiver la transparence des annotations: rend les annotations semi-transparentes afin d'afficher le contenu derrière l'annotation.</span><span class="sxs-lookup"><span data-stu-id="60fb4-135">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="60fb4-136">Page précédente: navigue jusqu'à la page précédente</span><span class="sxs-lookup"><span data-stu-id="60fb4-136">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="60fb4-137">Page suivante: accède à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="60fb4-137">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="60fb4-138">Accéder à la page – l'utilisateur peut entrer un numéro de page spécifique vers lequel naviguer</span><span class="sxs-lookup"><span data-stu-id="60fb4-138">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="60fb4-139">Zoom: définir le niveau de zoom pour l'affichage des annotations</span><span class="sxs-lookup"><span data-stu-id="60fb4-139">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="60fb4-140">Rotation: l'utilisateur peut faire pivoter le document vers la droite</span><span class="sxs-lookup"><span data-stu-id="60fb4-140">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="60fb4-141">Search: l'utilisateur peut effectuer des recherches dans un document et accéder aux différents accès au sein du document.</span><span class="sxs-lookup"><span data-stu-id="60fb4-141">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="60fb4-142">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="60fb4-142">Annotate view</span></span>
    ](../media/Reviewimage1.png)