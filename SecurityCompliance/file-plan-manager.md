---
title: Vue d’ensemble du gestionnaire de plan de gestion de fichiers
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.
ms.openlocfilehash: 4feacf20444591f6da2d55a928a81e86b56c5d9a
ms.sourcegitcommit: 9f34ace6bbe3d5e07e24ebaae96613750869cddf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25019275"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="0a0ba-103">Vue d’ensemble du gestionnaire de plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="0a0ba-103">Overview of file plan manager</span></span>

<span data-ttu-id="0a0ba-104">Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Page de plan de gestion de fichiers](media/file-plan-page.png)

## <a name="important-this-feature-is-currently-available-only-as-part-of-the-office-365-preview-program"></a><span data-ttu-id="0a0ba-106">Important : cette fonctionnalité est actuellement disponible uniquement dans le cadre du programme Office 365 Preview.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-106">Important: This feature is currently available only as part of the Office 365 Preview program</span></span>

<span data-ttu-id="0a0ba-107">Cette fonctionnalité s’affichera dans votre client uniquement si votre organisation est inscrite au programme Office 365 Preview.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-107">You will see this feature in your tenant only if your organization has enrolled in the Office 365 Preview program.</span></span>

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="0a0ba-108">Accès au gestionnaire de plan de fichiers</span><span class="sxs-lookup"><span data-stu-id="0a0ba-108">Accessing file plan manager</span></span>

<span data-ttu-id="0a0ba-109">Les deux conditions requises pour accéder au gestionnaire de plan de gestion de fichiers sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-109">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="0a0ba-110">Un abonnement Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-110">An Office 365 Enterprise E5 subscription with user licenses.</span></span>
- <span data-ttu-id="0a0ba-111">L’affectation de l’un des rôles suivants du centre de sécurité et de conformité à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-111">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="0a0ba-112">Gestionnaire de conservation</span><span class="sxs-lookup"><span data-stu-id="0a0ba-112">Retention Manager</span></span>
    - <span data-ttu-id="0a0ba-113">Gestionnaire de conservation en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a0ba-113">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="0a0ba-114">Navigation dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="0a0ba-114">Navigating your file plan</span></span>

<span data-ttu-id="0a0ba-115">Le gestionnaire de plan de gestion de fichiers permet d’afficher tous les paramètres de vos étiquettes et stratégies de conservation sur un même écran, en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-115">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="0a0ba-116">Notez que les étiquettes de conservation créées en dehors du plan de gestion de fichiers seront disponibles dans le plan de gestion de fichiers, et inversement.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-116">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="0a0ba-117">Sur l’onglet des **étiquettes du plan de gestion de fichiers**, les informations et fonctionnalités supplémentaires suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-117">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="0a0ba-118">Colonnes de paramètres des étiquettes</span><span class="sxs-lookup"><span data-stu-id="0a0ba-118">Label settings columns</span></span>
 
- <span data-ttu-id="0a0ba-p101">**Basé sur** identifie le type de déclencheur qui marque le début de la période de conservation. Les valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="0a0ba-121">Événement</span><span class="sxs-lookup"><span data-stu-id="0a0ba-121">Event</span></span>
    - <span data-ttu-id="0a0ba-122">Date de création</span><span class="sxs-lookup"><span data-stu-id="0a0ba-122">When created</span></span>
    - <span data-ttu-id="0a0ba-123">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="0a0ba-123">When last modified</span></span>
    - <span data-ttu-id="0a0ba-124">Date d’étiquetage</span><span class="sxs-lookup"><span data-stu-id="0a0ba-124">When labeled</span></span>
- <span data-ttu-id="0a0ba-p102">**Enregistrement** identifie si l’élément devient un enregistrement déclaré lorsque l’étiquette est appliquée. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="0a0ba-127">Non</span><span class="sxs-lookup"><span data-stu-id="0a0ba-127">No</span></span>
    - <span data-ttu-id="0a0ba-128">Oui</span><span class="sxs-lookup"><span data-stu-id="0a0ba-128">Yes</span></span>
    - <span data-ttu-id="0a0ba-129">Oui (réglementaire)</span><span class="sxs-lookup"><span data-stu-id="0a0ba-129">Yes(Regulatory)</span></span>
- <span data-ttu-id="0a0ba-p103">**Conservation** identifie le type de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="0a0ba-132">Conserver</span><span class="sxs-lookup"><span data-stu-id="0a0ba-132">Keep</span></span>
    - <span data-ttu-id="0a0ba-133">Conserver et supprimer</span><span class="sxs-lookup"><span data-stu-id="0a0ba-133">Keep and delete</span></span>
    - <span data-ttu-id="0a0ba-134">Supprimer</span><span class="sxs-lookup"><span data-stu-id="0a0ba-134">Delete</span></span>
- <span data-ttu-id="0a0ba-p104">**Destination** détermine ce qu’il advient du contenu à la fin de la période de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="0a0ba-137">null</span><span class="sxs-lookup"><span data-stu-id="0a0ba-137">Null</span></span>
    - <span data-ttu-id="0a0ba-138">Aucune action</span><span class="sxs-lookup"><span data-stu-id="0a0ba-138">No action necessary.</span></span>
    - <span data-ttu-id="0a0ba-139">Suppression automatique</span><span class="sxs-lookup"><span data-stu-id="0a0ba-139">Auto-delete</span></span>
    - <span data-ttu-id="0a0ba-140">Examen requis (également appelé Examen de destination)</span><span class="sxs-lookup"><span data-stu-id="0a0ba-140">Review required (aka Disposition review)</span></span>

![Paramètres des étiquettes dans le plan de gestion de fichiers](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="0a0ba-142">Colonnes des descripteurs de plan de gestion de fichiers pour les étiquettes</span><span class="sxs-lookup"><span data-stu-id="0a0ba-142">Label file plan descriptors columns</span></span>

<span data-ttu-id="0a0ba-p105">Vous pouvez désormais inclure plus d’informations dans la configuration de vos étiquettes de conservation. L’insertion de descripteurs de plan de gestion de fichiers dans les étiquettes permet de gérer et d’organiser plus facilement votre plan.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="0a0ba-p106">Pour vous aider à démarrer, le gestionnaire de plan de gestion de fichiers fournit des valeurs prédéfinies prêtes à être utilisées pour : Fonction/service, Catégorie, Type d’autorité et Mise en service/citation. Vous pouvez ajouter de nouvelles valeurs de descripteur de plan de gestion de fichiers lorsque vous créez ou modifiez une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="0a0ba-147">Voici une vue de l’étape des descripteurs de plan de gestion des fichiers lors de la création ou de la modification d’une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-147">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Descripteurs de plan de gestion de fichiers](media/file-plan-descriptors.png)

<span data-ttu-id="0a0ba-149">Voici une vue des colonnes de descripteurs du plan de gestion de fichiers dans l’onglet des étiquettes du gestionnaire de plan gestion de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-149">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="0a0ba-151">Export d’étiquettes depuis votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="0a0ba-151">Export labels out of your file plan</span></span>

<span data-ttu-id="0a0ba-152">Depuis le gestionnaire de plan de gestion de fichiers, vous pouvez exporter les détails de toutes les étiquettes de conservation dans un fichier .csv pour vous aider à fournir des évaluations périodiques de conformité aux responsables de la gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-152">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="0a0ba-153">Pour exporter toutes les étiquettes de conservation, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Exporter les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-153">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Option d’export de plan de gestion de fichiers](media/file-plan-export-labels-option.png)

<span data-ttu-id="0a0ba-155">Un fichier \*.csv contenant toutes les étiquettes de conservation existantes s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-155">A \*.csv file containing all existing retention labels will open.</span></span>

![Fichier CSV affichant toutes les étiquettes de conservation](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="0a0ba-157">Import d’étiquettes dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="0a0ba-157">Import labels into your file plan</span></span>

<span data-ttu-id="0a0ba-158">Dans le gestionnaire de plan de gestion de fichiers, vous pouvez importer de nouvelles étiquettes en bloc mais aussi modifier des étiquettes de conservation existantes.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-158">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="0a0ba-159">Pour importer de nouvelles étiquettes de conservation et mettre à jour des étiquettes de conservation existantes, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Importer les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-159">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Option d’import de plan de gestion de fichiers](media/file-plan-import-labels-option.png)

![Option de téléchargement d’un modèle de plan de gestion de fichiers vide](media/file-plan-blank-template-option.png)

<span data-ttu-id="0a0ba-162">Téléchargez un modèle vide (ou démarrez à partir d’un export de votre plan de gestion de fichiers actuel).</span><span class="sxs-lookup"><span data-stu-id="0a0ba-162">Download a blank template (or start from an export of your current file plan).</span></span>

![Modèle de plan de gestion de fichiers vide ouvert dans Excel](media/file-plan-blank-template.png)

<span data-ttu-id="0a0ba-164">Complétez le modèle (des informations de référence sur les valeurs valides pouvant être saisies seront bientôt disponibles).</span><span class="sxs-lookup"><span data-stu-id="0a0ba-164">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Modèle de plan de gestion de fichiers complété](media/file-plan-filled-out-template.png)

<span data-ttu-id="0a0ba-166">Chargez le modèle complété et le gestionnaire de plan de gestion de fichiers validera les entrées et affichera les statistiques d’importation.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-166">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Statistiques d’importation de plan de gestion de fichiers](media/file-plan-import-statistics.png)

<span data-ttu-id="0a0ba-168">Une fois l’importation terminée, accédez à nouveau au gestionnaire de plan de gestion de fichiers pour attribuer de nouvelles étiquettes aux stratégies nouvelles ou existantes.</span><span class="sxs-lookup"><span data-stu-id="0a0ba-168">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Option de publication d’étiquettes](media/file-plan-publish-labels-option.png)

