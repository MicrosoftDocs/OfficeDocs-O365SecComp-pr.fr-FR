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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241567"
---
# <a name="view-documents-in-a-working-set"></a><span data-ttu-id="de7cf-102">Afficher des documents dans un ensemble de travail</span><span class="sxs-lookup"><span data-stu-id="de7cf-102">View documents in a working set</span></span>

<span data-ttu-id="de7cf-103">Advanced eDiscovery (préversion) affiche du contenu à l'aide de plusieurs observateurs à des fins différentes.</span><span class="sxs-lookup"><span data-stu-id="de7cf-103">Advanced eDiscovery (Preview) displays content via several viewers each with different purposes.</span></span> <span data-ttu-id="de7cf-104">Les différentes visionneuses peuvent être utilisées en cliquant sur n'importe quel document d'une plage de travail.</span><span class="sxs-lookup"><span data-stu-id="de7cf-104">The various viewers can be used by clicking on any document within a working set.</span></span> <span data-ttu-id="de7cf-105">Les visionneuses actuellement fournies sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="de7cf-105">The viewers currently provided are:</span></span>

- <span data-ttu-id="de7cf-106">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="de7cf-106">File metadata</span></span>
- <span data-ttu-id="de7cf-107">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="de7cf-107">Native view</span></span>
- <span data-ttu-id="de7cf-108">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="de7cf-108">Text view</span></span>
- <span data-ttu-id="de7cf-109">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="de7cf-109">Annotate view</span></span>
- <span data-ttu-id="de7cf-110">Vue conVertie</span><span class="sxs-lookup"><span data-stu-id="de7cf-110">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="de7cf-111">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="de7cf-111">File metadata</span></span>

<span data-ttu-id="de7cf-112">Ce panneau peut être activé/désactivé pour afficher diverses métadonnées associées au document.</span><span class="sxs-lookup"><span data-stu-id="de7cf-112">This panel can be toggled on/off to display various metadata associated with the document.</span></span> <span data-ttu-id="de7cf-113">Bien que la grille des résultats de la recherche puisse être personnalisée pour afficher des métadonnées spécifiques, il peut s'avérer difficile de faire défiler horizontalement les données lors de la révision des données.</span><span class="sxs-lookup"><span data-stu-id="de7cf-113">Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data.</span></span> <span data-ttu-id="de7cf-114">Le panneau métadonnées de fichier permet à un utilisateur de basculer sur une vue dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="de7cf-114">The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="de7cf-115">Panneau métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="de7cf-115">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="de7cf-116">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="de7cf-116">Native view</span></span>

<span data-ttu-id="de7cf-117">La visionneuse Native affiche l'affichage le plus enrichi d'un document.</span><span class="sxs-lookup"><span data-stu-id="de7cf-117">The Native viewer displays the richest view of a document.</span></span> <span data-ttu-id="de7cf-118">Il prend en charge des centaines de types de fichiers et permet d'afficher l'expérience la plus réelle vers Native possible.</span><span class="sxs-lookup"><span data-stu-id="de7cf-118">It supports hundreds of file types and is meant to display the truest to native experience possible.</span></span> <span data-ttu-id="de7cf-119">Pour les fichiers Microsoft Office, par exemple, la visionneuse exploite Office Online pour afficher du contenu tel que des commentaires de document, des formules Excel, des lignes/colonnes masquées, des notes PowerPoint, etc. Pour plus d'informations sur les visionneuses Office Online, \[reportez-vous à l'article suivant:\]</span><span class="sxs-lookup"><span data-stu-id="de7cf-119">For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="de7cf-120">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="de7cf-120">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="de7cf-121">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="de7cf-121">Text view</span></span>

<span data-ttu-id="de7cf-122">La visionneuse de texte fournit une vue du texte extrait d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="de7cf-122">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="de7cf-123">Elle ignore toutes les images incorporées et la mise en forme, mais elle est très performante si un utilisateur tente de comprendre le contenu rapidement.</span><span class="sxs-lookup"><span data-stu-id="de7cf-123">It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly.</span></span> <span data-ttu-id="de7cf-124">L'affichage de texte comprend également d'autres fonctionnalités:</span><span class="sxs-lookup"><span data-stu-id="de7cf-124">Text view also includes other features:</span></span>

  - <span data-ttu-id="de7cf-125">Le compteur de ligne facilite la référence à des parties spécifiques d'un document.</span><span class="sxs-lookup"><span data-stu-id="de7cf-125">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="de7cf-126">Mise en surbrillance des résultats de recherche, qui met en surbrillance les termes dans le document, ainsi que la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="de7cf-126">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="de7cf-127">L'affichage diff fournit un affichage de comparaison qui met en surbrillance les différences textuelles lors de l'affichage des documents en double.</span><span class="sxs-lookup"><span data-stu-id="de7cf-127">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="de7cf-128">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="de7cf-128">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="de7cf-129">Vue diff</span><span class="sxs-lookup"><span data-stu-id="de7cf-129">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="de7cf-130">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="de7cf-130">Annotate view</span></span>

<span data-ttu-id="de7cf-131">L'affichage anNoted propose des fonctionnalités qui permettent aux utilisateurs d'appliquer un balisage à un document, notamment:</span><span class="sxs-lookup"><span data-stu-id="de7cf-131">The Annotate view provides features that allow users to apply markup on a document including:</span></span>

  - <span data-ttu-id="de7cf-132">Zone Redactions: les utilisateurs peuvent dessiner un cadre sur le document afin de masquer le contenu sensible</span><span class="sxs-lookup"><span data-stu-id="de7cf-132">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="de7cf-133">Crayon: les utilisateurs peuvent effectuer un dessin à main levée sur un document afin d'attirer l'attention sur certaines parties d'un document.</span><span class="sxs-lookup"><span data-stu-id="de7cf-133">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="de7cf-134">Sélectionner les annotations: les utilisateurs peuvent sélectionner des annotations dans un document afin de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="de7cf-134">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="de7cf-135">Activer/désactiver la transparence des annotations: rend les annotations semi-transparentes afin d'afficher le contenu derrière l'annotation.</span><span class="sxs-lookup"><span data-stu-id="de7cf-135">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="de7cf-136">Page précédente: navigue jusqu'à la page précédente</span><span class="sxs-lookup"><span data-stu-id="de7cf-136">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="de7cf-137">Page suivante: accède à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="de7cf-137">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="de7cf-138">Accéder à la page – l'utilisateur peut entrer un numéro de page spécifique vers lequel naviguer</span><span class="sxs-lookup"><span data-stu-id="de7cf-138">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="de7cf-139">Zoom: définir le niveau de zoom pour l'affichage des annotations</span><span class="sxs-lookup"><span data-stu-id="de7cf-139">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="de7cf-140">Rotation: l'utilisateur peut faire pivoter le document vers la droite</span><span class="sxs-lookup"><span data-stu-id="de7cf-140">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="de7cf-141">Search: l'utilisateur peut effectuer des recherches dans un document et accéder aux différents accès au sein du document.</span><span class="sxs-lookup"><span data-stu-id="de7cf-141">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="de7cf-142">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="de7cf-142">Annotate view</span></span>
    ](../media/Reviewimage1.png)