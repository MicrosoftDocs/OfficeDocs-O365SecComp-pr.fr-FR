---
title: Vue d’ensemble du gestionnaire de plan de gestion de fichiers
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.
ms.openlocfilehash: d972a7ea6507e51c4efaaef30c98d55a87912417
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454826"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="88daf-103">Vue d’ensemble du gestionnaire de plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="88daf-103">Overview of file plan manager</span></span>

<span data-ttu-id="88daf-104">Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.</span><span class="sxs-lookup"><span data-stu-id="88daf-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Page de plan de gestion de fichiers](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="88daf-106">Accès au gestionnaire de plan de fichiers</span><span class="sxs-lookup"><span data-stu-id="88daf-106">Accessing file plan manager</span></span>

<span data-ttu-id="88daf-107">Les deux conditions requises pour accéder au gestionnaire de plan de gestion de fichiers sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88daf-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="88daf-108">Un abonnement Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="88daf-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="88daf-109">L’affectation de l’un des rôles suivants du centre de sécurité et de conformité à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="88daf-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="88daf-110">Gestionnaire de conservation</span><span class="sxs-lookup"><span data-stu-id="88daf-110">Retention Manager</span></span>
    - <span data-ttu-id="88daf-111">Gestionnaire de conservation en lecture seule</span><span class="sxs-lookup"><span data-stu-id="88daf-111">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="88daf-112">Navigation dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="88daf-112">Navigating your file plan</span></span>

<span data-ttu-id="88daf-113">Le gestionnaire de plan de gestion de fichiers permet d’afficher tous les paramètres de vos étiquettes et stratégies de conservation sur un même écran, en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="88daf-113">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="88daf-114">Notez que les étiquettes de conservation créées en dehors du plan de gestion de fichiers seront disponibles dans le plan de gestion de fichiers, et inversement.</span><span class="sxs-lookup"><span data-stu-id="88daf-114">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="88daf-115">Sur l’onglet des **étiquettes du plan de gestion de fichiers**, les informations et fonctionnalités supplémentaires suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="88daf-115">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="88daf-116">Colonnes de paramètres des étiquettes</span><span class="sxs-lookup"><span data-stu-id="88daf-116">Label settings columns</span></span>
 
- <span data-ttu-id="88daf-p101">**Basé sur** identifie le type de déclencheur qui marque le début de la période de conservation. Les valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="88daf-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="88daf-119">Événement</span><span class="sxs-lookup"><span data-stu-id="88daf-119">Event</span></span>
    - <span data-ttu-id="88daf-120">Date de création</span><span class="sxs-lookup"><span data-stu-id="88daf-120">When created</span></span>
    - <span data-ttu-id="88daf-121">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="88daf-121">When last modified</span></span>
    - <span data-ttu-id="88daf-122">Date d’étiquetage</span><span class="sxs-lookup"><span data-stu-id="88daf-122">When labeled</span></span>
- <span data-ttu-id="88daf-p102">**Enregistrement** identifie si l’élément devient un enregistrement déclaré lorsque l’étiquette est appliquée. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88daf-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="88daf-125">Non</span><span class="sxs-lookup"><span data-stu-id="88daf-125">No</span></span>
    - <span data-ttu-id="88daf-126">Oui</span><span class="sxs-lookup"><span data-stu-id="88daf-126">Yes</span></span>
    - <span data-ttu-id="88daf-127">Oui (réglementaire)</span><span class="sxs-lookup"><span data-stu-id="88daf-127">Yes(Regulatory)</span></span>
- <span data-ttu-id="88daf-p103">**Conservation** identifie le type de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88daf-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="88daf-130">Conserver</span><span class="sxs-lookup"><span data-stu-id="88daf-130">Keep</span></span>
    - <span data-ttu-id="88daf-131">Conserver et supprimer</span><span class="sxs-lookup"><span data-stu-id="88daf-131">Keep and delete</span></span>
    - <span data-ttu-id="88daf-132">Supprimer</span><span class="sxs-lookup"><span data-stu-id="88daf-132">Delete</span></span>
- <span data-ttu-id="88daf-p104">**Destination** détermine ce qu’il advient du contenu à la fin de la période de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="88daf-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="88daf-135">null</span><span class="sxs-lookup"><span data-stu-id="88daf-135">null</span></span>
    - <span data-ttu-id="88daf-136">Aucune action</span><span class="sxs-lookup"><span data-stu-id="88daf-136">No action</span></span>
    - <span data-ttu-id="88daf-137">Suppression automatique</span><span class="sxs-lookup"><span data-stu-id="88daf-137">Auto-delete</span></span>
    - <span data-ttu-id="88daf-138">Examen requis (également appelé Examen de destination)</span><span class="sxs-lookup"><span data-stu-id="88daf-138">Review required (aka Disposition review)</span></span>

![Paramètres des étiquettes dans le plan de gestion de fichiers](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="88daf-140">Colonnes des descripteurs de plan de gestion de fichiers pour les étiquettes</span><span class="sxs-lookup"><span data-stu-id="88daf-140">Label file plan descriptors columns</span></span>

<span data-ttu-id="88daf-p105">Vous pouvez désormais inclure plus d’informations dans la configuration de vos étiquettes de conservation. L’insertion de descripteurs de plan de gestion de fichiers dans les étiquettes permet de gérer et d’organiser plus facilement votre plan.</span><span class="sxs-lookup"><span data-stu-id="88daf-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="88daf-p106">Pour vous aider à démarrer, le gestionnaire de plan de gestion de fichiers fournit des valeurs prédéfinies prêtes à être utilisées pour : Fonction/service, Catégorie, Type d’autorité et Mise en service/citation. Vous pouvez ajouter de nouvelles valeurs de descripteur de plan de gestion de fichiers lorsque vous créez ou modifiez une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="88daf-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="88daf-145">Voici une vue de l’étape des descripteurs de plan de gestion des fichiers lors de la création ou de la modification d’une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="88daf-145">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Descripteurs de plan de gestion de fichiers](media/file-plan-descriptors.png)

<span data-ttu-id="88daf-147">Voici une vue des colonnes de descripteurs du plan de gestion de fichiers dans l’onglet des étiquettes du gestionnaire de plan gestion de fichiers.</span><span class="sxs-lookup"><span data-stu-id="88daf-147">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="88daf-149">Export d’étiquettes depuis votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="88daf-149">Export labels out of your file plan</span></span>

<span data-ttu-id="88daf-150">Depuis le gestionnaire de plan de gestion de fichiers, vous pouvez exporter les détails de toutes les étiquettes de conservation dans un fichier .csv pour vous aider à fournir des évaluations périodiques de conformité aux responsables de la gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="88daf-150">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="88daf-151">Pour exporter toutes les étiquettes de conservation, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Exporter les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="88daf-151">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Option d’export de plan de gestion de fichiers](media/file-plan-export-labels-option.png)

<span data-ttu-id="88daf-153">Un fichier \*.csv contenant toutes les étiquettes de conservation existantes s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="88daf-153">A \*.csv file containing all existing retention labels will open.</span></span>

![Fichier CSV affichant toutes les étiquettes de conservation](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="88daf-155">Import d’étiquettes dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="88daf-155">Import labels into your file plan</span></span>

<span data-ttu-id="88daf-156">Dans le gestionnaire de plan de gestion de fichiers, vous pouvez importer de nouvelles étiquettes en bloc mais aussi modifier des étiquettes de conservation existantes.</span><span class="sxs-lookup"><span data-stu-id="88daf-156">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="88daf-157">Pour importer de nouvelles étiquettes de conservation et mettre à jour des étiquettes de conservation existantes, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Importer les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="88daf-157">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Option d’import de plan de gestion de fichiers](media/file-plan-import-labels-option.png)

![Option de téléchargement d’un modèle de plan de gestion de fichiers vide](media/file-plan-blank-template-option.png)

<span data-ttu-id="88daf-160">Téléchargez un modèle vide (ou démarrez à partir d’un export de votre plan de gestion de fichiers actuel).</span><span class="sxs-lookup"><span data-stu-id="88daf-160">Download a blank template (or start from an export of your current file plan).</span></span>

![Modèle de plan de gestion de fichiers vide ouvert dans Excel](media/file-plan-blank-template.png)

<span data-ttu-id="88daf-162">Complétez le modèle (des informations de référence sur les valeurs valides pouvant être saisies seront bientôt disponibles).</span><span class="sxs-lookup"><span data-stu-id="88daf-162">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Modèle de plan de gestion de fichiers complété](media/file-plan-filled-out-template.png)

<span data-ttu-id="88daf-164">Chargez le modèle complété et le gestionnaire de plan de gestion de fichiers validera les entrées et affichera les statistiques d’importation.</span><span class="sxs-lookup"><span data-stu-id="88daf-164">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Statistiques d’importation de plan de gestion de fichiers](media/file-plan-import-statistics.png)

<span data-ttu-id="88daf-166">Une fois l’importation terminée, accédez à nouveau au gestionnaire de plan de gestion de fichiers pour attribuer de nouvelles étiquettes aux stratégies nouvelles ou existantes.</span><span class="sxs-lookup"><span data-stu-id="88daf-166">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Option de publication d’étiquettes](media/file-plan-publish-labels-option.png)

