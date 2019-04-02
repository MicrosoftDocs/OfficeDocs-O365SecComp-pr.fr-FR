---
title: Examiner les données dans les preuves
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030072"
---
# <a name="review-data-in-evidence"></a><span data-ttu-id="93cf9-102">Examiner les données dans les preuves</span><span class="sxs-lookup"><span data-stu-id="93cf9-102">Review data in evidence</span></span>

<span data-ttu-id="93cf9-103">**Evidence** est un instantané des résultats de recherche que vous avez collectés.</span><span class="sxs-lookup"><span data-stu-id="93cf9-103">**Evidence** is a snapshot of search results that you collected.</span></span> <span data-ttu-id="93cf9-104">Lorsque vous ajoutez des résultats de recherche à une preuve, un processus est déclenché pour extraire des fichiers, des métadonnées et du texte.</span><span class="sxs-lookup"><span data-stu-id="93cf9-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text.</span></span> <span data-ttu-id="93cf9-105">Ensuite, le système génère un nouvel index de toutes les données et ajoute des **preuves**.</span><span class="sxs-lookup"><span data-stu-id="93cf9-105">Then, the system builds a new index of all the data and adds to **Evidence**.</span></span> 

<span data-ttu-id="93cf9-106">Pour tout incident sensible au temps, cela vous permet de rapidement contenir l'environnement en supprimant les données à l'emplacement d'origine lors de l'examen des preuves recréées dans un environnement en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="93cf9-106">For any time-sensitive incidents, this allows you to quickly contain the environment by deleting data at original locations while investigating re-created evidence in a quarantined environment.</span></span> <span data-ttu-id="93cf9-107">Une fois les preuves collectées, vous pouvez passer en revue les différents documents dans leur format natif, format texte ou quasi-natif.</span><span class="sxs-lookup"><span data-stu-id="93cf9-107">Once evidence is collected, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="93cf9-108">En outre, vous pouvez exécuter des requêtes pour affiner les données par plage de temps, types de fichiers, propriétaires de données et de nombreuses autres cartes de condition.</span><span class="sxs-lookup"><span data-stu-id="93cf9-108">Additionally, you can run queries to narrow the data by time range, file types, data owners, and many other condition cards.</span></span> <span data-ttu-id="93cf9-109">À l'aide des cartes de condition auteur/expéditeur/destinataire, vous pouvez rapidement examiner les personnes impliquées dans le renversement et s'il existe des partages externes.</span><span class="sxs-lookup"><span data-stu-id="93cf9-109">Using Author/Sender/Recipient condition cards, you can quickly examine who are involved in the spill and if there have been any external shares.</span></span> <span data-ttu-id="93cf9-110">Pour plus d'informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="93cf9-110">For more information, see:</span></span>

  - [<span data-ttu-id="93cf9-111">InterRoger les données dans les preuves</span><span class="sxs-lookup"><span data-stu-id="93cf9-111">Query the data in evidence</span></span>](evidence-query.md)

<span data-ttu-id="93cf9-112">Pour regrouper des documents et obtenir de l'aide supplémentaire pour votre révision, cliquez sur **gérer les preuves**.</span><span class="sxs-lookup"><span data-stu-id="93cf9-112">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="93cf9-113">Dans la vignette **analyse** , cliquez sur **analyser**.</span><span class="sxs-lookup"><span data-stu-id="93cf9-113">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="93cf9-114">Cette opération exécute des analyses avancées, telles que la détection des doublons, le Threading de messagerie électronique et l'analyse de thème.</span><span class="sxs-lookup"><span data-stu-id="93cf9-114">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="93cf9-115">Par la suite, vous pouvez voir les thèmes généraux des données et organiser les documents par des threads de messagerie, des doublons exacts et des doublons pour faciliter votre examen.</span><span class="sxs-lookup"><span data-stu-id="93cf9-115">Afterwards, you can see the general themes of the data and also organize documents by email threads, exact duplicates and near duplicates to facilitate your investigation.</span></span> <span data-ttu-id="93cf9-116">Pour plus d'informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="93cf9-116">For more information, see:</span></span>

  - [<span data-ttu-id="93cf9-117">Exécuter des analyses pour une analyse plus rapide</span><span class="sxs-lookup"><span data-stu-id="93cf9-117">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a><span data-ttu-id="93cf9-118">Afficher les documents dans les preuves</span><span class="sxs-lookup"><span data-stu-id="93cf9-118">View documents in evidence</span></span>

<span data-ttu-id="93cf9-119">L'analyse des données (préversion) affiche du contenu via plusieurs visionneuses à des fins différentes.</span><span class="sxs-lookup"><span data-stu-id="93cf9-119">Data investigation (Preview) displays content via several viewers each with different purposes.</span></span> <span data-ttu-id="93cf9-120">Les différents observateurs peuvent être utilisés en cliquant sur n'importe quel document dans **Evidence**.</span><span class="sxs-lookup"><span data-stu-id="93cf9-120">The various viewers can be used by clicking on any document in **Evidence**.</span></span> <span data-ttu-id="93cf9-121">Les visionneuses actuellement fournies sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="93cf9-121">The viewers currently provided are:</span></span>

- <span data-ttu-id="93cf9-122">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="93cf9-122">File metadata</span></span>
- <span data-ttu-id="93cf9-123">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="93cf9-123">Native view</span></span>
- <span data-ttu-id="93cf9-124">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="93cf9-124">Text view</span></span>
- <span data-ttu-id="93cf9-125">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="93cf9-125">Annotate view</span></span>
- <span data-ttu-id="93cf9-126">Vue conVertie</span><span class="sxs-lookup"><span data-stu-id="93cf9-126">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="93cf9-127">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="93cf9-127">File metadata</span></span>

<span data-ttu-id="93cf9-128">Ce panneau peut être activé/désactivé pour afficher diverses métadonnées associées au document.</span><span class="sxs-lookup"><span data-stu-id="93cf9-128">This panel can be toggled on/off to display various metadata associated with the document.</span></span> <span data-ttu-id="93cf9-129">Bien que la grille des résultats de la recherche puisse être personnalisée pour afficher des métadonnées spécifiques, il peut s'avérer difficile de faire défiler horizontalement les données lors de la révision des données.</span><span class="sxs-lookup"><span data-stu-id="93cf9-129">Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data.</span></span> <span data-ttu-id="93cf9-130">Le panneau métadonnées de fichier permet à un utilisateur de basculer sur une vue dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="93cf9-130">The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="93cf9-131">Panneau métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="93cf9-131">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="93cf9-132">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="93cf9-132">Native view</span></span>

<span data-ttu-id="93cf9-133">La visionneuse Native affiche l'affichage le plus enrichi d'un document.</span><span class="sxs-lookup"><span data-stu-id="93cf9-133">The Native viewer displays the richest view of a document.</span></span> <span data-ttu-id="93cf9-134">Il prend en charge des centaines de types de fichiers et permet d'afficher l'expérience la plus réelle vers Native possible.</span><span class="sxs-lookup"><span data-stu-id="93cf9-134">It supports hundreds of file types and is meant to display the truest to native experience possible.</span></span> <span data-ttu-id="93cf9-135">Pour les fichiers Microsoft Office, par exemple, la visionneuse exploite Office Online pour afficher du contenu tel que des commentaires de document, des formules Excel, des lignes/colonnes masquées, des notes PowerPoint, etc. Pour plus d'informations sur les visionneuses Office Online, \[reportez-vous à l'article suivant:\]</span><span class="sxs-lookup"><span data-stu-id="93cf9-135">For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="93cf9-136">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="93cf9-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="93cf9-137">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="93cf9-137">Text view</span></span>

<span data-ttu-id="93cf9-138">La visionneuse de texte fournit une vue du texte extrait d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="93cf9-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="93cf9-139">Elle ignore toutes les images incorporées et la mise en forme, mais elle est très performante si un utilisateur tente de comprendre le contenu rapidement.</span><span class="sxs-lookup"><span data-stu-id="93cf9-139">It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly.</span></span> <span data-ttu-id="93cf9-140">L'affichage de texte comprend également d'autres fonctionnalités:</span><span class="sxs-lookup"><span data-stu-id="93cf9-140">Text view also includes other features:</span></span>

  - <span data-ttu-id="93cf9-141">Le compteur de ligne facilite la référence à des parties spécifiques d'un document.</span><span class="sxs-lookup"><span data-stu-id="93cf9-141">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="93cf9-142">Mise en surbrillance des résultats de recherche, qui met en surbrillance les termes dans le document, ainsi que la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="93cf9-142">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="93cf9-143">L'affichage diff fournit un affichage de comparaison qui met en surbrillance les différences textuelles lors de l'affichage des documents en double.</span><span class="sxs-lookup"><span data-stu-id="93cf9-143">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="93cf9-144">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="93cf9-144">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="93cf9-145">Vue diff</span><span class="sxs-lookup"><span data-stu-id="93cf9-145">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="93cf9-146">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="93cf9-146">Annotate view</span></span>

<span data-ttu-id="93cf9-147">L'affichage anNoted propose des fonctionnalités qui permettent aux utilisateurs d'appliquer un balisage à un document lors de l'enquête, notamment:</span><span class="sxs-lookup"><span data-stu-id="93cf9-147">The Annotate view provides features that allow users to apply markup on a document during investigation including:</span></span>

  - <span data-ttu-id="93cf9-148">Zone Redactions: les utilisateurs peuvent dessiner un cadre sur le document afin de masquer le contenu sensible</span><span class="sxs-lookup"><span data-stu-id="93cf9-148">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="93cf9-149">Crayon: les utilisateurs peuvent effectuer un dessin à main levée sur un document afin d'attirer l'attention sur certaines parties d'un document.</span><span class="sxs-lookup"><span data-stu-id="93cf9-149">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="93cf9-150">Sélectionner les annotations: les utilisateurs peuvent sélectionner des annotations dans un document afin de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="93cf9-150">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="93cf9-151">Activer/désactiver la transparence des annotations: rend les annotations semi-transparentes afin d'afficher le contenu derrière l'annotation.</span><span class="sxs-lookup"><span data-stu-id="93cf9-151">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="93cf9-152">Page précédente: navigue jusqu'à la page précédente</span><span class="sxs-lookup"><span data-stu-id="93cf9-152">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="93cf9-153">Page suivante: accède à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="93cf9-153">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="93cf9-154">Accéder à la page – l'utilisateur peut entrer un numéro de page spécifique vers lequel naviguer</span><span class="sxs-lookup"><span data-stu-id="93cf9-154">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="93cf9-155">Zoom: définir le niveau de zoom pour l'affichage des annotations</span><span class="sxs-lookup"><span data-stu-id="93cf9-155">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="93cf9-156">Rotation: l'utilisateur peut faire pivoter le document vers la droite</span><span class="sxs-lookup"><span data-stu-id="93cf9-156">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="93cf9-157">Search: l'utilisateur peut effectuer des recherches dans un document et accéder aux différents accès au sein du document.</span><span class="sxs-lookup"><span data-stu-id="93cf9-157">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="93cf9-158">AnNoter l'affichage</span><span class="sxs-lookup"><span data-stu-id="93cf9-158">Annotate view</span></span>
    ](../media/Reviewimage1.png)

<span data-ttu-id="93cf9-159">Notez que ces annotations se trouvent sur les données collectées en tant que preuves, et non à leur emplacement d'origine dans le système actif.</span><span class="sxs-lookup"><span data-stu-id="93cf9-159">Note that these annotations are on data collected as evidence, not at its original location in live system.</span></span> 

## <a name="more-information"></a><span data-ttu-id="93cf9-160">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="93cf9-160">More information</span></span>

<span data-ttu-id="93cf9-161">Le tableau suivant répertorie les limites pour les preuves dans les enquêtes de données (aperçu).</span><span class="sxs-lookup"><span data-stu-id="93cf9-161">The following table lists the limits for evidence in Data Investigations (Preview).</span></span>  <span data-ttu-id="93cf9-162">Tous les éléments qui dépassent le nombre maximal de fichiers sont affichés en tant qu'erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="93cf9-162">Any items that exceed the single file maximums will show up as processing errors.</span></span>
    
  |<span data-ttu-id="93cf9-163">**Description de la limite**</span><span class="sxs-lookup"><span data-stu-id="93cf9-163">**Description of limit**</span></span>|<span data-ttu-id="93cf9-164">**Limite**</span><span class="sxs-lookup"><span data-stu-id="93cf9-164">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="93cf9-165">Nombre maximal de collections de preuves</span><span class="sxs-lookup"><span data-stu-id="93cf9-165">Maximum number of evidence collections</span></span>  <br/> |<span data-ttu-id="93cf9-166">50</span><span class="sxs-lookup"><span data-stu-id="93cf9-166">50</span></span>  <br/> |
  |<span data-ttu-id="93cf9-167">Nombre total de documents pouvant être ingérés dans un cas (pour toutes les collections de preuves de l'enquête)</span><span class="sxs-lookup"><span data-stu-id="93cf9-167">Total number of documents that can be ingested into a case (for all evidence collections in the investigation)</span></span>  <br/> |<span data-ttu-id="93cf9-168">1 million</span><span class="sxs-lookup"><span data-stu-id="93cf9-168">1 million</span></span>  <br/> |
  |<span data-ttu-id="93cf9-169">Taille totale des fichiers par charge</span><span class="sxs-lookup"><span data-stu-id="93cf9-169">Total file size per load</span></span>  <br/> |<span data-ttu-id="93cf9-170">100 Go</span><span class="sxs-lookup"><span data-stu-id="93cf9-170">100 GB</span></span>  <br/> |
  |<span data-ttu-id="93cf9-171">Taille maximale d'un fichier unique</span><span class="sxs-lookup"><span data-stu-id="93cf9-171">Maximum size of single file</span></span>   <br/> |<span data-ttu-id="93cf9-172">100 Mo</span><span class="sxs-lookup"><span data-stu-id="93cf9-172">100 MB</span></span>  <br/> |
  |<span data-ttu-id="93cf9-173">Nombre maximal de caractères extraits à partir d'un seul fichier</span><span class="sxs-lookup"><span data-stu-id="93cf9-173">Maximum number of characters extracted from a single file</span></span>  <br/> |<span data-ttu-id="93cf9-174">10 millions</span><span class="sxs-lookup"><span data-stu-id="93cf9-174">10 million</span></span>  <br/> |
  |<span data-ttu-id="93cf9-175">Profondeur des éléments incorporés dans un document</span><span class="sxs-lookup"><span data-stu-id="93cf9-175">Depth of embedded items in a document</span></span>  <br/> |<span data-ttu-id="93cf9-176">25</span><span class="sxs-lookup"><span data-stu-id="93cf9-176">25</span></span>  <br/> |
  