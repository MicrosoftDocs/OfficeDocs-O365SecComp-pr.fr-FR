---
title: Notes de publication du gestionnaire de conformité Microsoft
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Le gestionnaire de conformité Microsoft est un outil d'évaluation des risques gratuit basé sur un flux de travail dans le portail d'approbation de service Microsoft. Le gestionnaire de conformité vous permet de suivre, d'affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473064"
---
# <a name="release-notes-for-compliance-manager-preview"></a><span data-ttu-id="e37df-104">Notes de publication pour le gestionnaire de conformité (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e37df-104">Release Notes for Compliance Manager (Preview)</span></span>

<span data-ttu-id="e37df-105">La préversion publique du gestionnaire de conformité vous permet d'accéder en avant-première aux fonctionnalités et mises à jour à venir.</span><span class="sxs-lookup"><span data-stu-id="e37df-105">The public preview of Compliance Manager provides you with early access to upcoming functionality and updates.</span></span>

<span data-ttu-id="e37df-106">Vous pouvez utiliser l'outil [Gestionnaire de conformité](https://servicetrust.microsoft.com/ComplianceManager) mis à jour sur le [portail d'approbation de service](https://servicetrust.microsoft.com) pour suivre, attribuer et vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e37df-106">You can use the updated [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) tool on the [Service Trust Portal](https://servicetrust.microsoft.com) to track, assign, and verify regulatory compliance activities related to Microsoft cloud services.</span></span>

## <a name="whats-new-in-compliance-manager-preview"></a><span data-ttu-id="e37df-107">Nouveautés du gestionnaire de conformité (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e37df-107">What’s new in Compliance Manager (Preview)</span></span>

- <span data-ttu-id="e37df-108">**Intégration avec le score de sécurité Microsoft:** Le gestionnaire de conformité prend en charge l'intégration avec le [score de sécurité Microsoft](microsoft-secure-score.md) en mappant les actions gérées par le client à plus de 50 actions de score sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e37df-108">**Integration with Microsoft Secure Score:** Compliance Manager supports integration with [Microsoft Secure Score](microsoft-secure-score.md) by mapping customer-managed Actions to more than 50 Secure Score actions.</span></span> <span data-ttu-id="e37df-109">Lorsque vous terminez une action mappée dans le score de sécurité, l'action du gestionnaire de conformité correspondante est automatiquement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e37df-109">When you complete a mapped action in Secure Score, the corresponding Compliance Manager Action is automatically updated.</span></span>

- <span data-ttu-id="e37df-110">**Importer des évaluations personnalisées:** Outre les évaluations intégrées, le gestionnaire de conformité prend désormais en charge l'importation des modèles personnalisés, ce qui vous permet de créer des évaluations personnalisées pour n'importe quel produit ou service, ainsi que pour n'importe quelle norme ou réglementation.</span><span class="sxs-lookup"><span data-stu-id="e37df-110">**Import custom Assessments:** In addition to built-in Assessments, Compliance Manager now supports importing custom Templates, enabling you to create custom Assessments for any product or service and any standard or regulation.</span></span>

- <span data-ttu-id="e37df-111">**Éléments d'action:** Les éléments d'action sont maintenant des éléments individuels et de nombreux incluent une collection de télémétrie provenant de l'API graphique Microsoft Secure score.</span><span class="sxs-lookup"><span data-stu-id="e37df-111">**Actions Items:** Action Items are now individual items and many include telemetry collection from the Microsoft Secure Score Graph API.</span></span> <span data-ttu-id="e37df-112">Dans la mesure du possible, les recommandations d'action technique ont maintenant des liens vers la page de configuration applicable dans le service Office 365.</span><span class="sxs-lookup"><span data-stu-id="e37df-112">Where possible, technical action recommendations now have links to the applicable configuration page in the Office 365 service.</span></span>

- <span data-ttu-id="e37df-113">**Gestion des clients:** Nouvelle interface de gestion des nouveaux éléments de données dans le gestionnaire de conformité (aperçu):</span><span class="sxs-lookup"><span data-stu-id="e37df-113">**Tenant Management:** New interface for managing new data elements in Compliance Manager (Preview):</span></span>
    - <span data-ttu-id="e37df-114">**Dimensions:** Afficher, ajouter et personnaliser des métadonnées pour des modèles, des évaluations et des éléments d'action qui vous permettent de créer des tableaux croisés dynamiques personnalisés pour les filtres.</span><span class="sxs-lookup"><span data-stu-id="e37df-114">**Dimensions:** View, add and customize metadata for Templates, Assessments, and Action Items that allow you to create custom pivots for filters.</span></span>
    - <span data-ttu-id="e37df-115">**Propriétaires:** Spécifiez un propriétaire pour chaque élément d'action.</span><span class="sxs-lookup"><span data-stu-id="e37df-115">**Owners:** Specify an owner for each Action Item.</span></span>
    - <span data-ttu-id="e37df-116">**Actions des clients:** Gérez la liste complète des éléments actions inclus dans le gestionnaire de conformité (aperçu) et activez/désactivez la surveillance du score sécurisé pour les éléments d'action intégrés avec le score sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e37df-116">**Customer Actions:** Manage the complete list of Actions Items included in Compliance Manager (Preview) and enable/disable Secure Score monitoring for Action Items that are integrated with Secure Score.</span></span>

- <span data-ttu-id="e37df-117">**Score de conformité mis à jour**: la méthodologie a changé pour prendre en charge la synchronisation avec le score de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e37df-117">**Updated Compliance Score**: The methodology has changed to support syncing with Microsoft Secure Score.</span></span> <span data-ttu-id="e37df-118">Le système de score supprime les crédits de contrôle gérés par Microsoft et se concentre uniquement sur l'exécution des contrôles gérés par le client.</span><span class="sxs-lookup"><span data-stu-id="e37df-118">The scoring system removes the Microsoft-managed control credits and focuses solely on the completion of customer-managed controls.</span></span>

## <a name="known-issues-in-compliance-manager-preview"></a><span data-ttu-id="e37df-119">Problèmes connus dans le gestionnaire de conformité (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e37df-119">Known issues in Compliance Manager (Preview)</span></span>

<span data-ttu-id="e37df-120">Les sections suivantes couvrent les problèmes connus à résoudre dans les prochaines versions du gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="e37df-120">The following sections cover known issues to be resolved in upcoming releases of Compliance Manager.</span></span>

### <a name="compliance-score"></a><span data-ttu-id="e37df-121">Score de conformité</span><span class="sxs-lookup"><span data-stu-id="e37df-121">Compliance Score</span></span>

- <span data-ttu-id="e37df-122">Lorsque les éléments d'action sont marqués comme **n'étant pas dans l'étendue**, le score attribué à l'action n'est pas exclu du calcul du score de conformité.</span><span class="sxs-lookup"><span data-stu-id="e37df-122">When Action Items are marked as **Not in Scope**, the score assigned to the Action Item is not excluded from the Compliance Score calculation.</span></span> <span data-ttu-id="e37df-123">Les éléments d'action marqués comme **n'étant pas inclus dans l'étendue** ne doivent pas augmenter votre score de conformité.</span><span class="sxs-lookup"><span data-stu-id="e37df-123">Action Items marked **Not in Scope** should not increase your Compliance Score.</span></span>

### <a name="microsoft-managed-controls"></a><span data-ttu-id="e37df-124">Contrôles gérés par Microsoft</span><span class="sxs-lookup"><span data-stu-id="e37df-124">Microsoft-managed Controls</span></span>

- <span data-ttu-id="e37df-125">La date de test pour les contrôles gérés par Microsoft n'apparaît pas dans l'interface utilisateur, même si elle est incluse dans l'évaluation.</span><span class="sxs-lookup"><span data-stu-id="e37df-125">The test date for Microsoft-managed controls is not appearing in the UI, even when included in the Assessment.</span></span> <span data-ttu-id="e37df-126">Pour afficher les informations de date de test, vous devez exporter l'évaluation.</span><span class="sxs-lookup"><span data-stu-id="e37df-126">To see test date information, you must export the Assessment.</span></span>

### <a name="customization"></a><span data-ttu-id="e37df-127">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="e37df-127">Customization</span></span>

- <span data-ttu-id="e37df-128">L'ajout de contrôles personnalisés permet d'ajouter un nouveau contrôle à une famille de contrôle existante, mais il ne vous permet pas d'ajouter une nouvelle famille de contrôles.</span><span class="sxs-lookup"><span data-stu-id="e37df-128">Adding custom Controls enables adding a new control to an existing control family, but it does not allow you to add a new Control Family.</span></span>
- <span data-ttu-id="e37df-129">Cette version ne prend pas en charge la liaison d'éléments d'action ou l'ajout d'éléments actions ou de contrôles à une évaluation.</span><span class="sxs-lookup"><span data-stu-id="e37df-129">This release does not support linking Action Items or adding Actions Items or Controls to an Assessment.</span></span>
- <span data-ttu-id="e37df-130">Si vous créez une action personnalisée, vous ne pouvez pas la modifier ou la supprimer.</span><span class="sxs-lookup"><span data-stu-id="e37df-130">If you create a custom Action, you cannot edit or delete it.</span></span>

### <a name="control-families-not-shown-in-assessments"></a><span data-ttu-id="e37df-131">Familles de contrôle non affichées dans les évaluations</span><span class="sxs-lookup"><span data-stu-id="e37df-131">Control Families Not Shown in Assessments</span></span>

- <span data-ttu-id="e37df-132">Lorsque vous importez un modèle, toutes les évaluations basées sur ce modèle reflètent toutes les familles de contrôle qui font partie du modèle.</span><span class="sxs-lookup"><span data-stu-id="e37df-132">When you import a Template, all Assessments based on that Template will reflect all Control Families that are part of the Template.</span></span> <span data-ttu-id="e37df-133">Toutefois, si vous ajoutez de nouvelles familles de contrôle au modèle, les évaluations existantes ne refléteront pas les modifications.</span><span class="sxs-lookup"><span data-stu-id="e37df-133">But if you add new Control Families to the Template, any existing Assessments will not reflect the changes.</span></span> <span data-ttu-id="e37df-134">Seules les nouvelles évaluations créées à partir du modèle mis à jour reflètent les modifications.</span><span class="sxs-lookup"><span data-stu-id="e37df-134">Only new Assessments created off the updated Template will reflect the changes.</span></span>

### <a name="filters"></a><span data-ttu-id="e37df-135">Filtres</span><span class="sxs-lookup"><span data-stu-id="e37df-135">Filters</span></span>

- <span data-ttu-id="e37df-136">Le filtrage des éléments d'action ou des contrôles ne produit pas toujours des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="e37df-136">Filtering on Action Items or Controls does not consistently produce correct results.</span></span>

### <a name="templates"></a><span data-ttu-id="e37df-137">Modèles</span><span class="sxs-lookup"><span data-stu-id="e37df-137">Templates</span></span>

- <span data-ttu-id="e37df-138">Les modèles archivés sont modifiables et ne doivent pas être modifiables.</span><span class="sxs-lookup"><span data-stu-id="e37df-138">Archived templates are editable and they should not be editable.</span></span>
- <span data-ttu-id="e37df-139">Les modèles verrouillés permettent la création d'une évaluation alors qu'ils ne le devraient pas.</span><span class="sxs-lookup"><span data-stu-id="e37df-139">Locked templates allow for Assessment creation when they should not.</span></span> <span data-ttu-id="e37df-140">Le verrouillage d'un modèle est destiné à empêcher son utilisation pour créer des évaluations.</span><span class="sxs-lookup"><span data-stu-id="e37df-140">Locking a Template is meant to prevent it from being used to create Assessments.</span></span>

### <a name="export"></a><span data-ttu-id="e37df-141">Exporter</span><span class="sxs-lookup"><span data-stu-id="e37df-141">Export</span></span>

- <span data-ttu-id="e37df-142">L'exportation de modèle vers JSON échoue lorsque l'état du modèle est défini sur **importé** ou **en attente d'approbation**.</span><span class="sxs-lookup"><span data-stu-id="e37df-142">Template export to JSON fails when the template status is set to **Imported** or **Pending Approval**.</span></span>

### <a name="supported-browsers"></a><span data-ttu-id="e37df-143">Navigateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="e37df-143">Supported browsers</span></span>

- <span data-ttu-id="e37df-144">Les versions les plus récentes de Microsoft Edge, chrome et Safari sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e37df-144">The latest versions of Microsoft Edge, Chrome, and Safari are supported.</span></span>
- <span data-ttu-id="e37df-145">Dans certaines circonstances, les données mises à jour ne s'affichent pas tant que votre navigateur n'est pas actualisé.</span><span class="sxs-lookup"><span data-stu-id="e37df-145">There may be instances where updated data does not appear until your browser is refreshed.</span></span>
- <span data-ttu-id="e37df-146">La version d'évaluation de Microsoft Edge n'est pas prise en charge, mais n'a pas de problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="e37df-146">The preview version of Microsoft Edge is not supported but has no known issues.</span></span>
- <span data-ttu-id="e37df-147">Internet Explorer n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e37df-147">Internet Explorer is not supported.</span></span>

### <a name="session-timeout"></a><span data-ttu-id="e37df-148">Délai d'expiration de session</span><span class="sxs-lookup"><span data-stu-id="e37df-148">Session timeout</span></span>

- <span data-ttu-id="e37df-149">Lorsqu'une session arrive à expiration, une erreur «un problème est survenu» peut apparaître.</span><span class="sxs-lookup"><span data-stu-id="e37df-149">When a session times out, a “Something went wrong” error may appear.</span></span> <span data-ttu-id="e37df-150">Pour résoudre ce dernier, accédez au [Gestionnaire de conformité](https://servicetrust.microsoft.com/ComplianceManager) et reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="e37df-150">To resolve, go to [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) and log in again.</span></span>