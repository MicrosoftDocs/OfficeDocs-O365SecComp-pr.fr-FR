---
title: Recherche et marquage
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666144"
---
# <a name="search-and-tagging"></a><span data-ttu-id="37432-104">Recherche et marquage</span><span class="sxs-lookup"><span data-stu-id="37432-104">Search and Tagging</span></span>

<span data-ttu-id="37432-p102">Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta. Pour une brève démonstration de recherche et de marquage, voir la vidéo de [gérer vos données avec eDiscovery avancée](https://www.youtube.com/watch?v=VaPYL3DHP6I) .</span><span class="sxs-lookup"><span data-stu-id="37432-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="37432-p103">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="37432-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="37432-110">Recherche les documents dans votre cas.</span><span class="sxs-lookup"><span data-stu-id="37432-110">Search the documents in your case</span></span>

<span data-ttu-id="37432-p104">Après avoir traitement des documents dans un cas eDiscovery avancées (et éventuellement exécuter le module d’analyse ou la pertinence), vous pouvez utiliser la recherche et le balisage pour rechercher des documents et de les organiser en appliquant des balises spécifique (également appelées étiquettes). Vous pouvez définir une requête de recherche à l’aide de cartes de la condition fournie ou à l’aide d’un langage de requête KQL comparables dans les mots clés condition carte. La syntaxe de KQL courants, tels que AND, OR, NOT et NEAR(n) sont pris en charge, ainsi que des caractère multiples caractère générique (\*).</span><span class="sxs-lookup"><span data-stu-id="37432-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="37432-p105">Le tableau suivant répertorie les propriétés que vous pouvez rechercher à l’aide d’une requête de mot clé KQL. Vous pouvez également utiliser une carte de condition pour dans l’outil de recherche de découverte électronique avancée pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="37432-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="37432-116">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="37432-116">**Property**</span></span>|<span data-ttu-id="37432-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="37432-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37432-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="37432-118">**caselabel**</span></span> <br/> | <span data-ttu-id="37432-119">Nom de la balise créé/appliquée lorsqu’un document est marqué.</span><span class="sxs-lookup"><span data-stu-id="37432-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="37432-120">**dépositaire**</span><span class="sxs-lookup"><span data-stu-id="37432-120">**custodian**</span></span> <br/> | <span data-ttu-id="37432-121">Le dépositaire associé à un document ; limitations de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37432-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="37432-122">**date**</span><span class="sxs-lookup"><span data-stu-id="37432-122">**date**</span></span> <br/> | <span data-ttu-id="37432-123">Envoyé date pour le courrier électronique ; la date de modification de documents du site.</span><span class="sxs-lookup"><span data-stu-id="37432-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="37432-124">**fileid**</span><span class="sxs-lookup"><span data-stu-id="37432-124">**fileid**</span></span> <br/> | <span data-ttu-id="37432-125">L’ID du fichier dans le cas.</span><span class="sxs-lookup"><span data-stu-id="37432-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="37432-126">**FileType**</span><span class="sxs-lookup"><span data-stu-id="37432-126">**filetype**</span></span> <br/> | <span data-ttu-id="37432-127">L’extension de fichier natif.</span><span class="sxs-lookup"><span data-stu-id="37432-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="37432-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="37432-128">**fileclass**</span></span> <br/> | <span data-ttu-id="37432-129">Courrier électronique, document ou pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="37432-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="37432-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="37432-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="37432-131">L’expéditeur pour le courrier électronique ; l’auteur des documents du site.</span><span class="sxs-lookup"><span data-stu-id="37432-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="37432-132">**taille**</span><span class="sxs-lookup"><span data-stu-id="37432-132">**size**</span></span> <br/> | <span data-ttu-id="37432-133">La taille du fichier en Ko.</span><span class="sxs-lookup"><span data-stu-id="37432-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="37432-134">**subjecttitle**</span><span class="sxs-lookup"><span data-stu-id="37432-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="37432-135">L’objet du courrier électronique ; titre de documents du site.</span><span class="sxs-lookup"><span data-stu-id="37432-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="37432-136">**bcc**</span><span class="sxs-lookup"><span data-stu-id="37432-136">**bcc**</span></span> <br/> | <span data-ttu-id="37432-137">Le champ Cci d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="37432-138">**cc**</span><span class="sxs-lookup"><span data-stu-id="37432-138">**cc**</span></span> <br/> | <span data-ttu-id="37432-139">Le champ Cc d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="37432-140">**participants**</span><span class="sxs-lookup"><span data-stu-id="37432-140">**participants**</span></span> <br/> | <span data-ttu-id="37432-141">L’adresse de messagerie de tous les participants dans un thread de messagerie, y compris les liens manquants.</span><span class="sxs-lookup"><span data-stu-id="37432-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="37432-142">**reçus**</span><span class="sxs-lookup"><span data-stu-id="37432-142">**received**</span></span> <br/> | <span data-ttu-id="37432-143">La date de que réception un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="37432-144">**destinataires**</span><span class="sxs-lookup"><span data-stu-id="37432-144">**recipients**</span></span> <br/> | <span data-ttu-id="37432-145">Destinataires d’un message électronique, inclus sur l’à, Cc ou Cci champs.</span><span class="sxs-lookup"><span data-stu-id="37432-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="37432-146">**expéditeur**</span><span class="sxs-lookup"><span data-stu-id="37432-146">**sender**</span></span> <br/> | <span data-ttu-id="37432-147">L’expéditeur d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="37432-148">**LastModifiedDate**</span><span class="sxs-lookup"><span data-stu-id="37432-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="37432-149">La dernière date de modification de document d’un site.</span><span class="sxs-lookup"><span data-stu-id="37432-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="37432-150">**envoyé**</span><span class="sxs-lookup"><span data-stu-id="37432-150">**sent**</span></span> <br/> | <span data-ttu-id="37432-151">La date d’envoi d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="37432-152">**À**</span><span class="sxs-lookup"><span data-stu-id="37432-152">**to**</span></span> <br/> | <span data-ttu-id="37432-153">Le destinataire est répertorié dans le champ d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="37432-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="37432-154">**auteur**</span><span class="sxs-lookup"><span data-stu-id="37432-154">**author**</span></span> <br/> | <span data-ttu-id="37432-155">L’auteur d’un document de site.</span><span class="sxs-lookup"><span data-stu-id="37432-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="37432-156">**title**</span><span class="sxs-lookup"><span data-stu-id="37432-156">**title**</span></span> <br/> | <span data-ttu-id="37432-157">Le titre d’un document de site.</span><span class="sxs-lookup"><span data-stu-id="37432-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="37432-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="37432-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="37432-159">Le thème principal d’un élément.</span><span class="sxs-lookup"><span data-stu-id="37432-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="37432-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="37432-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="37432-161">Thèmes qui sont associés à un élément.</span><span class="sxs-lookup"><span data-stu-id="37432-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="37432-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="37432-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="37432-163">Le centile de lecture d’un élément, sur le problème défini par [issuenum].</span><span class="sxs-lookup"><span data-stu-id="37432-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="37432-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="37432-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="37432-165">Le score de pertinence d’un élément, sur le problème défini par [issuenum].</span><span class="sxs-lookup"><span data-stu-id="37432-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="37432-166">**relevancetag_ [tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="37432-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="37432-167">Si un élément a été balisée manuellement pour la pertinence, la balise définie par [tagname].</span><span class="sxs-lookup"><span data-stu-id="37432-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="37432-168">\*Disponible uniquement si le module de thèmes a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="37432-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="37432-169">\*\*Disponible uniquement si le module de la pertinence a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="37432-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="37432-p106">Vous pouvez également utiliser une carte de condition dans l’outil de recherche de découverte électronique avancée pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche. La capture d’écran suivante montre les conditions pouvant être ajoutée à une requête. La colonne **groupe** indique si la propriété s’applique à la messagerie, les documents du site ou les deux (indiquée par la valeur *commune*). Cette colonne identifie également les propriétés utilisables dans une requête qui sont disponibles après avoir exécuté le module de la pertinence.</span><span class="sxs-lookup"><span data-stu-id="37432-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Conditions de recherche dans l’outil de recherche avancée eDiscovery](media/AeDSearchConditions.png)

<span data-ttu-id="37432-175">Pour plus d’informations sur les propriétés de recherche, voir [requêtes de mot clé et les conditions de recherche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="37432-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37432-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37432-176">See also</span></span>

[<span data-ttu-id="37432-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="37432-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-178">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="37432-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-179">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="37432-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-180">Marquage et formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="37432-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-181">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="37432-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-182">Selon les résultats de la sélection du conteneur</span><span class="sxs-lookup"><span data-stu-id="37432-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="37432-183">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="37432-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

