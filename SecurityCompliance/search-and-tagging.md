---
title: Recherche et balisage
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans Advanced eDiscovery, le module de recherche et de marquage vous permet de rechercher, de prévisualiser et d'organiser les documents dans votre cas. Actuellement, ce module est en version bêta.
ms.openlocfilehash: d5fdf12621bfb2064f3782b947fa4be386d544d1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219204"
---
# <a name="search-and-tagging"></a><span data-ttu-id="448d9-104">Recherche et balisage</span><span class="sxs-lookup"><span data-stu-id="448d9-104">Search and Tagging</span></span>

<span data-ttu-id="448d9-p102">Dans Advanced eDiscovery, le module de recherche et de marquage vous permet de rechercher, de prévisualiser et d'organiser les documents dans votre cas. Actuellement, ce module est en version bêta. Pour une brève démonstration de la recherche et du balisage, voir la vidéo [gérer vos données à l'aide de la vidéo Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) .</span><span class="sxs-lookup"><span data-stu-id="448d9-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="448d9-p103">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="448d9-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="448d9-110">Rechercher les documents dans votre cas</span><span class="sxs-lookup"><span data-stu-id="448d9-110">Search the documents in your case</span></span>

<span data-ttu-id="448d9-p104">Une fois que vous avez traité des documents dans un cas avancé eDiscovery (et si vous le souhaitez), vous pouvez utiliser la recherche et le balisage pour rechercher des documents, puis les organiser en appliquant des balises propres à la casse (également appelées étiquettes). Vous pouvez définir une requête de recherche à l'aide des cartes de condition fournies ou à l'aide d'un langage de requête KQL dans la carte de condition de mots-clés. La syntaxe KQL commune, telle que AND, OR, NOT et NEAR (n) sont prises en charge, ainsi que les caractères génériques à caractères multiples (\*).</span><span class="sxs-lookup"><span data-stu-id="448d9-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="448d9-p105">Le tableau suivant répertorie les propriétés que vous pouvez rechercher à l'aide d'une requête de mot clé KQL. Vous pouvez également utiliser une carte de condition dans l'outil de recherche avancée eDiscovery pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="448d9-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="448d9-116">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="448d9-116">**Property**</span></span>|<span data-ttu-id="448d9-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="448d9-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="448d9-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="448d9-118">**caselabel**</span></span> <br/> | <span data-ttu-id="448d9-119">Nom de la balise créée/appliquée lorsqu'un document est balisé.</span><span class="sxs-lookup"><span data-stu-id="448d9-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="448d9-120">**gardien**</span><span class="sxs-lookup"><span data-stu-id="448d9-120">**custodian**</span></span> <br/> | <span data-ttu-id="448d9-121">Dépositaire associé à un document; soumis à des limitations.</span><span class="sxs-lookup"><span data-stu-id="448d9-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="448d9-122">**jours**</span><span class="sxs-lookup"><span data-stu-id="448d9-122">**date**</span></span> <br/> | <span data-ttu-id="448d9-123">Date d'envoi du courrier électronique; Date de modification des documents de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="448d9-124">**combinaison**</span><span class="sxs-lookup"><span data-stu-id="448d9-124">**fileid**</span></span> <br/> | <span data-ttu-id="448d9-125">ID de fichier dans le cas.</span><span class="sxs-lookup"><span data-stu-id="448d9-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="448d9-126">**filetype**</span><span class="sxs-lookup"><span data-stu-id="448d9-126">**filetype**</span></span> <br/> | <span data-ttu-id="448d9-127">Extension de fichier native.</span><span class="sxs-lookup"><span data-stu-id="448d9-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="448d9-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="448d9-128">**fileclass**</span></span> <br/> | <span data-ttu-id="448d9-129">Courrier électronique, document ou pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="448d9-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="448d9-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="448d9-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="448d9-131">Expéditeur du courrier électronique; auteur des documents de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="448d9-132">**longueur**</span><span class="sxs-lookup"><span data-stu-id="448d9-132">**size**</span></span> <br/> | <span data-ttu-id="448d9-133">Taille du fichier en Ko.</span><span class="sxs-lookup"><span data-stu-id="448d9-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="448d9-134">**subjecttitle**</span><span class="sxs-lookup"><span data-stu-id="448d9-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="448d9-135">L'objet de la messagerie; titre des documents de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="448d9-136">**bcc**</span><span class="sxs-lookup"><span data-stu-id="448d9-136">**bcc**</span></span> <br/> | <span data-ttu-id="448d9-137">Champ CCI d'un message électronique.</span><span class="sxs-lookup"><span data-stu-id="448d9-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="448d9-138">**cc**</span><span class="sxs-lookup"><span data-stu-id="448d9-138">**cc**</span></span> <br/> | <span data-ttu-id="448d9-139">Champ CC d'un message électronique.</span><span class="sxs-lookup"><span data-stu-id="448d9-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="448d9-140">**auront**</span><span class="sxs-lookup"><span data-stu-id="448d9-140">**participants**</span></span> <br/> | <span data-ttu-id="448d9-141">Adresse de messagerie de tous les participants d'un thread de messagerie, y compris pour les liens manquants.</span><span class="sxs-lookup"><span data-stu-id="448d9-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="448d9-142">**ont**</span><span class="sxs-lookup"><span data-stu-id="448d9-142">**received**</span></span> <br/> | <span data-ttu-id="448d9-143">Date à laquelle un message électronique a été reçu.</span><span class="sxs-lookup"><span data-stu-id="448d9-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="448d9-144">**destinataires**</span><span class="sxs-lookup"><span data-stu-id="448d9-144">**recipients**</span></span> <br/> | <span data-ttu-id="448d9-145">Destinataires d'un e-mail, inclus dans les champs à, CC ou CCI.</span><span class="sxs-lookup"><span data-stu-id="448d9-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="448d9-146">**expéditeur**</span><span class="sxs-lookup"><span data-stu-id="448d9-146">**sender**</span></span> <br/> | <span data-ttu-id="448d9-147">Expéditeur d'un message électronique.</span><span class="sxs-lookup"><span data-stu-id="448d9-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="448d9-148">**LastModifiedDate**</span><span class="sxs-lookup"><span data-stu-id="448d9-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="448d9-149">Date de la dernière modification d'un document de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="448d9-150">**envoyés**</span><span class="sxs-lookup"><span data-stu-id="448d9-150">**sent**</span></span> <br/> | <span data-ttu-id="448d9-151">Date d'envoi d'un message électronique.</span><span class="sxs-lookup"><span data-stu-id="448d9-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="448d9-152">**À**</span><span class="sxs-lookup"><span data-stu-id="448d9-152">**to**</span></span> <br/> | <span data-ttu-id="448d9-153">Destinataire figurant dans le champ à d'un message électronique.</span><span class="sxs-lookup"><span data-stu-id="448d9-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="448d9-154">**créés**</span><span class="sxs-lookup"><span data-stu-id="448d9-154">**author**</span></span> <br/> | <span data-ttu-id="448d9-155">Auteur d'un document de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="448d9-156">**title**</span><span class="sxs-lookup"><span data-stu-id="448d9-156">**title**</span></span> <br/> | <span data-ttu-id="448d9-157">Titre d'un document de site.</span><span class="sxs-lookup"><span data-stu-id="448d9-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="448d9-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="448d9-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="448d9-159">Thème dominant d'un élément.</span><span class="sxs-lookup"><span data-stu-id="448d9-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="448d9-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="448d9-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="448d9-161">Thèmes associés à un élément.</span><span class="sxs-lookup"><span data-stu-id="448d9-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="448d9-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="448d9-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="448d9-163">Centile de lecture d'un élément pour le problème défini par [issuenum].</span><span class="sxs-lookup"><span data-stu-id="448d9-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="448d9-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="448d9-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="448d9-165">Score de pertinence d'un élément pour le problème défini par [issuenum].</span><span class="sxs-lookup"><span data-stu-id="448d9-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="448d9-166">**relevancetag_ [TagName]**\*\*</span><span class="sxs-lookup"><span data-stu-id="448d9-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="448d9-167">Si un élément a été marqué manuellement pour des éléments de pertinence, la balise définie par [TagName].</span><span class="sxs-lookup"><span data-stu-id="448d9-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="448d9-168">\*Disponible uniquement si le module thèmes a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="448d9-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="448d9-169">\*\*Disponible uniquement si le module de pertinence a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="448d9-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="448d9-p106">Vous pouvez également utiliser une carte de condition dans l'outil de recherche avancée eDiscovery pour ajouter une condition (pour les propriétés sélectionnées) à une requête de recherche. La capture d'écran suivante montre les conditions qui peuvent être ajoutées à une requête. La colonne **Group** indique si la propriété s'applique aux messages électroniques, aux documents de site ou aux deux (indiqué par la valeur *Common*). Cette colonne identifie également les propriétés pouvant faire l'objet d'une recherche après l'exécution du module de pertinence.</span><span class="sxs-lookup"><span data-stu-id="448d9-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Conditions de recherche dans l'outil de recherche avancée eDiscovery](media/AeDSearchConditions.png)

<span data-ttu-id="448d9-175">Pour plus d'informations sur les propriétés pouvant faire l'objet d'une recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="448d9-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="448d9-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="448d9-176">See also</span></span>

[<span data-ttu-id="448d9-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="448d9-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-178">Présentation de l'évaluation en matière de pertinence</span><span class="sxs-lookup"><span data-stu-id="448d9-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-179">Balisage et évaluation</span><span class="sxs-lookup"><span data-stu-id="448d9-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-180">Étiquetage et formation à la pertinence</span><span class="sxs-lookup"><span data-stu-id="448d9-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-181">Analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="448d9-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-182">Choix en fonction des résultats</span><span class="sxs-lookup"><span data-stu-id="448d9-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="448d9-183">Évaluation de l'analyse de pertinence</span><span class="sxs-lookup"><span data-stu-id="448d9-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

