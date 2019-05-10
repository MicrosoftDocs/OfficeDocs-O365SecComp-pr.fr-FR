---
title: Configuration de la détection des droits du client dans Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835064"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="84322-102">Configuration de la détection des privilèges client (préversion) dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="84322-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="84322-103">Un aspect majeur et coûteux de la partie révision de n’importe quel processus de découverte est l’analyse du contenu privilégié.</span><span class="sxs-lookup"><span data-stu-id="84322-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="84322-104">Advanced eDiscovery offre une détection des contenus privilégiés dans votre cas afin que vous puissiez améliorer l’efficacité de ce processus.</span><span class="sxs-lookup"><span data-stu-id="84322-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="84322-105">Dans la mesure où cette fonctionnalité est actuellement en version bêta, un administrateur eDiscovery doit s’abonner à la fonctionnalité pour l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="84322-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="84322-106">Comment fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="84322-106">How does it work?</span></span>

<span data-ttu-id="84322-107">Lorsque la fonctionnalité est activée, lorsque vous analysez un jeu de révision dans un cas, tous les documents sont exécutés par le biais du modèle de détection des privilèges du client avocat.</span><span class="sxs-lookup"><span data-stu-id="84322-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="84322-108">Le modèle examine les deux éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="84322-108">The model looks at two things:</span></span>

- <span data-ttu-id="84322-109">Contenu: le modèle ML détermine la probabilité que le contenu du document soit légal.</span><span class="sxs-lookup"><span data-stu-id="84322-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="84322-110">Participants: s’il existe une liste d’avocats téléchargés par l’utilisateur pour le client, le modèle compare les participants du document à la liste afin de déterminer si le document a au moins un participant à un avocat.</span><span class="sxs-lookup"><span data-stu-id="84322-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="84322-111">Le modèle génère trois valeurs pour chaque document, qui seront toutes recherchées dans un ensemble de révision:</span><span class="sxs-lookup"><span data-stu-id="84322-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="84322-112">Score de contenu: probabilité que le document soit de nature légale (score compris entre 0 et 1)</span><span class="sxs-lookup"><span data-stu-id="84322-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="84322-113">A avocat: true si l’un des participants se trouve dans la liste des avocats chargés, false dans le cas contraire ou s’il n’y a pas de liste d’avocats.</span><span class="sxs-lookup"><span data-stu-id="84322-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="84322-114">Potentiellement privilégié: vrai si le score de contenu est supérieur au seuil ou a un participant à un avocat, faux dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84322-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="84322-115">Préversion de la détection des privilèges client</span><span class="sxs-lookup"><span data-stu-id="84322-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="84322-116">Étape 1: s’abonner à avocat-détection des privilèges client (administrateur eDiscovery)</span><span class="sxs-lookup"><span data-stu-id="84322-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="84322-117">Étant donné que la détection des privilèges du client est une fonctionnalité d’aperçu, votre administrateur eDiscovery doit s’abonner pour que la fonctionnalité soit disponible dans vos cas.</span><span class="sxs-lookup"><span data-stu-id="84322-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="84322-118">Accédez à «configurer les fonctionnalités expérimentales» à partir de la page Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="84322-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="84322-119">Cliquez sur «gérer la détection de droits client».</span><span class="sxs-lookup"><span data-stu-id="84322-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="84322-120">Cliquez sur le bouton bascule pour activer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="84322-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="84322-121">Étape 2: télécharger une liste d’avocats (facultatif)</span><span class="sxs-lookup"><span data-stu-id="84322-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="84322-122">Pour tirer pleinement parti de la détection des privilèges du client pour les avocats, nous vous recommandons de fournir une liste des adresses de messagerie des avocats ou des personnes morales qui travaillent pour la société.</span><span class="sxs-lookup"><span data-stu-id="84322-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="84322-123">La liste doit être un CSV sans en-tête, avec une adresse de messagerie par ligne.</span><span class="sxs-lookup"><span data-stu-id="84322-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="84322-124">Exploitation de la détection de privilèges client</span><span class="sxs-lookup"><span data-stu-id="84322-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="84322-125">Étape 1: analyser un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="84322-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="84322-126">Lorsque vous analysez votre jeu de révision, la détection des privilèges du client est également exécutée.</span><span class="sxs-lookup"><span data-stu-id="84322-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="84322-127">Pour en savoir plus sur l’analyse des données dans l’ensemble de révision, reportez-vous à [analyser les données d’un jeu de vérification dans Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="84322-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="84322-128">Étape 2: créer un groupe de balises actives avec le modèle de détection de privilège client</span><span class="sxs-lookup"><span data-stu-id="84322-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="84322-129">L’utilisation d’un groupe de balises actives est l’une des principales façons dont vous pouvez utiliser les résultats de la détection des droits du client dans votre processus de révision.</span><span class="sxs-lookup"><span data-stu-id="84322-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="84322-130">Les groupes de balises actives prennent les résultats d’un modèle ML et affichent les résultats du modèle en ligne en regard des balises, afin que vous puissiez facilement utiliser les résultats du modèle, le cas échéant, et utiliser les balises dans votre processus de révision comme vous le feriez avec d’autres balises dans votre panneau de marquage.</span><span class="sxs-lookup"><span data-stu-id="84322-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span>

- <span data-ttu-id="84322-131">Dans «gérer les balises», cliquez sur «Ajouter une balise».</span><span class="sxs-lookup"><span data-stu-id="84322-131">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="84322-132">Sélectionnez «avocat-détection des privilèges client».</span><span class="sxs-lookup"><span data-stu-id="84322-132">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="84322-133">Vous verrez qu’un groupe de balises et deux balises, correspondant aux résultats possibles du modèle, ont été créés.</span><span class="sxs-lookup"><span data-stu-id="84322-133">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="84322-134">Renommez le groupe de balises et les balises comme vous le jugez adapté à votre révision.</span><span class="sxs-lookup"><span data-stu-id="84322-134">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="84322-135">Étape 3: utiliser le groupe de balises actives pour la révision des privilèges</span><span class="sxs-lookup"><span data-stu-id="84322-135">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="84322-136">Lorsque vous examinez un document, si le modèle a déterminé que le document est potentiellement privilégié, la balise active correspondante expose le résultat:</span><span class="sxs-lookup"><span data-stu-id="84322-136">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="84322-137">Si le contenu du document peut être légal, une étiquette «contenu légal» apparaît en regard de la balise active correspondante.</span><span class="sxs-lookup"><span data-stu-id="84322-137">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="84322-138">Si le document a un participant qui se trouve dans la liste des avocats téléchargés, une étiquette «avocat» apparaît en regard de la balise active correspondante.</span><span class="sxs-lookup"><span data-stu-id="84322-138">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>