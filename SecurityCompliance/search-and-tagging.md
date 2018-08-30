---
title: Recherche et marquage
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528182"
---
# <a name="search-and-tagging"></a><span data-ttu-id="b4df1-104">Recherche et marquage</span><span class="sxs-lookup"><span data-stu-id="b4df1-104">Search and Tagging</span></span>

<span data-ttu-id="b4df1-p102">Dans découverte avancée, le module de recherche et de balisage vous permet de recherche, à afficher et organiser les documents dans votre cas. Ce module est actuellement en version bêta.</span><span class="sxs-lookup"><span data-stu-id="b4df1-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta.</span></span>

> [!NOTE]
> <span data-ttu-id="b4df1-p103">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="b4df1-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="b4df1-109">Recherche les documents dans votre cas.</span><span class="sxs-lookup"><span data-stu-id="b4df1-109">Search the documents in your case</span></span>

<span data-ttu-id="b4df1-p104">Une fois que vous avez traité des documents d’eDiscovery avancée et éventuellement exécuter le module d’analyse ou le module de la pertinence, vous pouvez utiliser la recherche et à l’aide de balisage pour rechercher les documents dans le cas et organiser les balises spécifique. Vous pouvez définir vos requêtes en utilisant les cartes condition fournie, ou via un langage de requête KQL comparables dans les mots clés condition carte. La syntaxe de KQL courants, tels que AND, OR, NOT et NEAR(n) sont pris en charge, ainsi que des caractère multiples caractère générique (\*). Ces propriétés sont prises en charge dans le nom de propriété de langage de requête :</span><span class="sxs-lookup"><span data-stu-id="b4df1-p104">Once you have processed documents in Advanced eDiscovery and optionally run the Analyze module or the Relevance module, you can use Search and Tagging to search through the documents in the case and organize them using case-specific tags. You can define your queries using the provided condition cards, or through a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*). These properties are supported in the query language property name:</span></span>

- <span data-ttu-id="b4df1-114">caselabel : balises créé/appliquées dans la recherche et le balisage dans ce cas</span><span class="sxs-lookup"><span data-stu-id="b4df1-114">caselabel: tags created/applied in Search and Tagging for this case</span></span> 
- <span data-ttu-id="b4df1-115">dépositaires : dépositaires affectés dans ce cas - soumises aux limitations</span><span class="sxs-lookup"><span data-stu-id="b4df1-115">custodians: custodians assigned in the case - subject to limitations</span></span>
- <span data-ttu-id="b4df1-116">date : date pour le courrier électronique d’envoi, date pour les documents de modification</span><span class="sxs-lookup"><span data-stu-id="b4df1-116">date: sent date for email, modified date for documents</span></span>
- <span data-ttu-id="b4df1-117">fileid : ID de fichier dans le cas</span><span class="sxs-lookup"><span data-stu-id="b4df1-117">fileid: file ID within the case</span></span>
- <span data-ttu-id="b4df1-118">FileType : extension de fichier native</span><span class="sxs-lookup"><span data-stu-id="b4df1-118">filetype: native file extension</span></span>
- <span data-ttu-id="b4df1-119">fileclass : courrier électronique, document ou pièce jointe</span><span class="sxs-lookup"><span data-stu-id="b4df1-119">fileclass: email, document, or attachment</span></span>
- <span data-ttu-id="b4df1-120">senderauthor : l’expéditeur pour les courriers électroniques, auteur pour les documents</span><span class="sxs-lookup"><span data-stu-id="b4df1-120">senderauthor: sender for emails, author for documents</span></span>
- <span data-ttu-id="b4df1-121">taille : taille du fichier dans la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="b4df1-121">size: size of the file in KB</span></span>
- <span data-ttu-id="b4df1-122">subjecttitle : objet pour les courriers électroniques, titre pour les documents</span><span class="sxs-lookup"><span data-stu-id="b4df1-122">subjecttitle: subject for emails, title for documents</span></span>
- <span data-ttu-id="b4df1-123">bcc</span><span class="sxs-lookup"><span data-stu-id="b4df1-123">bcc</span></span>
- <span data-ttu-id="b4df1-124">cc</span><span class="sxs-lookup"><span data-stu-id="b4df1-124">cc</span></span>
- <span data-ttu-id="b4df1-125">participants : les adresses de tous les participants dans un thread de messagerie, y compris les liens manquants de messagerie</span><span class="sxs-lookup"><span data-stu-id="b4df1-125">participants: Email addresses of all participants in an email thread, including for missing links</span></span>
- <span data-ttu-id="b4df1-126">reçus : date de réception</span><span class="sxs-lookup"><span data-stu-id="b4df1-126">received: received date</span></span>
- <span data-ttu-id="b4df1-127">destinataires : noms des destinataires ou des adresses (à, cc, Cci) de messagerie</span><span class="sxs-lookup"><span data-stu-id="b4df1-127">recipients: email recipient names or addresses (to, cc, bcc)</span></span>
- <span data-ttu-id="b4df1-128">expéditeur</span><span class="sxs-lookup"><span data-stu-id="b4df1-128">sender</span></span>
- <span data-ttu-id="b4df1-129">LastModifiedDate : dernière modification d’un document</span><span class="sxs-lookup"><span data-stu-id="b4df1-129">lastmodifieddate: last modified date of a document</span></span>
- <span data-ttu-id="b4df1-130">envoyés : date d’un message électronique d’envoi</span><span class="sxs-lookup"><span data-stu-id="b4df1-130">sent: sent date of an email</span></span>
- <span data-ttu-id="b4df1-131">à</span><span class="sxs-lookup"><span data-stu-id="b4df1-131">to</span></span>
- <span data-ttu-id="b4df1-132">auteur : auteur d’un message électronique</span><span class="sxs-lookup"><span data-stu-id="b4df1-132">author: author of an email</span></span>
- <span data-ttu-id="b4df1-133">titre : titre d’un document</span><span class="sxs-lookup"><span data-stu-id="b4df1-133">title: title of a document</span></span>
- <span data-ttu-id="b4df1-134">dominanttheme : thème principal d’un élément\*</span><span class="sxs-lookup"><span data-stu-id="b4df1-134">dominanttheme: dominant theme of an item\*</span></span>
- <span data-ttu-id="b4df1-135">themeslist : des thèmes qui sont associés à un élément\*</span><span class="sxs-lookup"><span data-stu-id="b4df1-135">themeslist: themes that are associated with an item\*</span></span>
- <span data-ttu-id="b4df1-136">readpercentile_ [issuenum] : lire centile d’un élément à problème [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="b4df1-136">readpercentile_[issuenum]: read percentile of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="b4df1-137">relevancescore_ [issuenum] : score de pertinence d’un élément à problème [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="b4df1-137">relevancescore_[issuenum]: relevance score of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="b4df1-138">relevancetag_ [issuenum] : si un élément a été marqué manuellement pour la pertinence, sa balise pour [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="b4df1-138">relevancetag_[issuenum]: if an item has been manually tagged for relevance, its tag for [issuenum]\*\*</span></span>

<span data-ttu-id="b4df1-139">\*Disponible uniquement si le module de thèmes a été exécuté \* \* disponible uniquement si le module de la pertinence a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="b4df1-139">\* Only available if the Themes module has been run \*\* Only available if the Relevance module has been run</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4df1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4df1-140">See also</span></span>

[<span data-ttu-id="b4df1-141">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="b4df1-141">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-142">Évaluation de la présentation de la pertinence</span><span class="sxs-lookup"><span data-stu-id="b4df1-142">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-143">Marquage et évaluation</span><span class="sxs-lookup"><span data-stu-id="b4df1-143">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-144">Marquage et formation de pertinence</span><span class="sxs-lookup"><span data-stu-id="b4df1-144">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-145">Analyse de la pertinence de suivi</span><span class="sxs-lookup"><span data-stu-id="b4df1-145">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-146">Selon les résultats de la sélection du conteneur</span><span class="sxs-lookup"><span data-stu-id="b4df1-146">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b4df1-147">Test d’analyse de la pertinence</span><span class="sxs-lookup"><span data-stu-id="b4df1-147">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

