---
title: Vue d’ensemble du gestionnaire de plan de gestion de fichiers
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.
ms.openlocfilehash: b7d80ff6a7f78e592462fe2723a87383e046015f
ms.sourcegitcommit: 6eb51931242d07abde2e37f1bd57d13bc724f0de
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34547969"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="95dfa-103">Vue d’ensemble du gestionnaire de plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="95dfa-103">Overview of file plan manager</span></span>

<span data-ttu-id="95dfa-104">Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.</span><span class="sxs-lookup"><span data-stu-id="95dfa-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Page de plan de gestion de fichiers](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="95dfa-106">Accès au gestionnaire de plan de fichiers</span><span class="sxs-lookup"><span data-stu-id="95dfa-106">Accessing file plan manager</span></span>

<span data-ttu-id="95dfa-107">Les deux conditions requises pour accéder au gestionnaire de plan de gestion de fichiers sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="95dfa-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="95dfa-108">Un abonnement Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="95dfa-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="95dfa-109">L’affectation de l’un des rôles suivants du centre de sécurité et de conformité à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="95dfa-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="95dfa-110">Gestionnaire de conservation</span><span class="sxs-lookup"><span data-stu-id="95dfa-110">Retention Manager</span></span>
    - <span data-ttu-id="95dfa-111">Gestionnaire de conservation en lecture seule</span><span class="sxs-lookup"><span data-stu-id="95dfa-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="95dfa-112">Étiquettes de rétention par défaut et stratégie d’étiquette</span><span class="sxs-lookup"><span data-stu-id="95dfa-112">Default retention labels and label policy</span></span>

<span data-ttu-id="95dfa-113">S’il n’existe aucune des étiquettes de rétention dans le centre de sécurité et conformité, la première fois que vous sélectionnez **Offre Fichier** dans le volet de navigation gauche, cela crée une stratégie d’étiquette appelée **Stratégie de Publication de Gouvernance des Données par défaut**.</span><span class="sxs-lookup"><span data-stu-id="95dfa-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="95dfa-114">Cette stratégie d’étiquette contient trois étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="95dfa-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="95dfa-115">**Processus opérationnels**</span><span class="sxs-lookup"><span data-stu-id="95dfa-115">**Operational procedure**</span></span>
- <span data-ttu-id="95dfa-116">**Entreprise générale**</span><span class="sxs-lookup"><span data-stu-id="95dfa-116">**Business general**</span></span>
- <span data-ttu-id="95dfa-117">**Accord Contrat**</span><span class="sxs-lookup"><span data-stu-id="95dfa-117">**Contract agreement**</span></span>

<span data-ttu-id="95dfa-118">Ces étiquettes de rétention sont uniquement configurées pour conserver le contenu, et non supprimer le contenu.</span><span class="sxs-lookup"><span data-stu-id="95dfa-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="95dfa-119">Cette stratégie d’étiquette peut être publiée dans l’ensemble de votre organisation et peut être désactivée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="95dfa-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="95dfa-120">Vous pouvez déterminer qui a ouvert le Gestionnaire d’Offre de fichiers et désactivé l’expérience de première exécution en passant en revue le journal d’audit pour les activités **Créé la stratégie de rétention** et **Créé la configuration de rétention pour une stratégie de rétention**.</span><span class="sxs-lookup"><span data-stu-id="95dfa-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="95dfa-121">En raison des commentaires des clients, nous avons supprimé cette fonctionnalité qui crée les étiquettes de rétention par défaut et la stratégie d’étiquette de rétention mentionnées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="95dfa-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="95dfa-122">Vous ne verrez que ces étiquettes de rétention et la stratégie d’étiquette de rétention si vous avez ouvert le gestionnaire de plan de gestion des fichiers avant le 11 avril 2019.</span><span class="sxs-lookup"><span data-stu-id="95dfa-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="95dfa-123">Navigation dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="95dfa-123">Navigating your file plan</span></span>

<span data-ttu-id="95dfa-124">Le gestionnaire de plan de gestion de fichiers permet d’afficher tous les paramètres de vos étiquettes et stratégies de conservation sur un même écran, en toute simplicité.</span><span class="sxs-lookup"><span data-stu-id="95dfa-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="95dfa-125">Notez que les étiquettes de conservation créées en dehors du plan de gestion de fichiers seront disponibles dans le plan de gestion de fichiers, et inversement.</span><span class="sxs-lookup"><span data-stu-id="95dfa-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="95dfa-126">Sur l’onglet des **étiquettes du plan de gestion de fichiers**, les informations et fonctionnalités supplémentaires suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="95dfa-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="95dfa-127">Colonnes de paramètres des étiquettes</span><span class="sxs-lookup"><span data-stu-id="95dfa-127">Label settings columns</span></span>

- <span data-ttu-id="95dfa-p103">**Basé sur** identifie le type de déclencheur qui marque le début de la période de conservation. Les valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="95dfa-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="95dfa-130">Événement</span><span class="sxs-lookup"><span data-stu-id="95dfa-130">Event</span></span>
    - <span data-ttu-id="95dfa-131">Date de création</span><span class="sxs-lookup"><span data-stu-id="95dfa-131">When created</span></span>
    - <span data-ttu-id="95dfa-132">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="95dfa-132">When last modified</span></span>
    - <span data-ttu-id="95dfa-133">Date d’étiquetage</span><span class="sxs-lookup"><span data-stu-id="95dfa-133">When labeled</span></span>
- <span data-ttu-id="95dfa-p104">**Enregistrement** identifie si l’élément devient un enregistrement déclaré lorsque l’étiquette est appliquée. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="95dfa-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="95dfa-136">Non</span><span class="sxs-lookup"><span data-stu-id="95dfa-136">No</span></span>
    - <span data-ttu-id="95dfa-137">Oui</span><span class="sxs-lookup"><span data-stu-id="95dfa-137">Yes</span></span>
    - <span data-ttu-id="95dfa-138">Oui (réglementaire)</span><span class="sxs-lookup"><span data-stu-id="95dfa-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="95dfa-p105">**Conservation** identifie le type de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="95dfa-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="95dfa-141">Conserver</span><span class="sxs-lookup"><span data-stu-id="95dfa-141">Keep</span></span>
    - <span data-ttu-id="95dfa-142">Conserver et supprimer</span><span class="sxs-lookup"><span data-stu-id="95dfa-142">Keep and delete</span></span>
    - <span data-ttu-id="95dfa-143">Supprimer</span><span class="sxs-lookup"><span data-stu-id="95dfa-143">Delete</span></span>
- <span data-ttu-id="95dfa-p106">**Destination** détermine ce qu’il advient du contenu à la fin de la période de conservation. Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="95dfa-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="95dfa-146">null</span><span class="sxs-lookup"><span data-stu-id="95dfa-146">null</span></span>
    - <span data-ttu-id="95dfa-147">Aucune action</span><span class="sxs-lookup"><span data-stu-id="95dfa-147">No action</span></span>
    - <span data-ttu-id="95dfa-148">Suppression automatique</span><span class="sxs-lookup"><span data-stu-id="95dfa-148">Auto-delete</span></span>
    - <span data-ttu-id="95dfa-149">Examen requis (également appelé Examen de destination)</span><span class="sxs-lookup"><span data-stu-id="95dfa-149">Review required (aka Disposition review)</span></span>

![Paramètres des étiquettes dans le plan de gestion de fichiers](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a><span data-ttu-id="95dfa-151">Colonnes des descripteurs de plan de gestion de fichiers pour les étiquettes</span><span class="sxs-lookup"><span data-stu-id="95dfa-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="95dfa-p107">Vous pouvez désormais inclure plus d’informations dans la configuration de vos étiquettes de conservation. L’insertion de descripteurs de plan de gestion de fichiers dans les étiquettes de rétention permet de gérer et d’organiser plus facilement votre plan.</span><span class="sxs-lookup"><span data-stu-id="95dfa-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="95dfa-p108">Pour vous aider à démarrer, le gestionnaire de plan de gestion de fichiers fournit des valeurs prédéfinies prêtes à être utilisées pour : Fonction/service, Catégorie, Type d’autorité et Mise en service/citation. Vous pouvez ajouter de nouvelles valeurs de descripteur de plan de gestion de fichiers lorsque vous créez ou modifiez une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="95dfa-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="95dfa-156">Voici une vue de l’étape des descripteurs de plan de gestion des fichiers lors de la création ou de la modification d’une étiquette de conservation.</span><span class="sxs-lookup"><span data-stu-id="95dfa-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Descripteurs de plan de gestion de fichiers](media/file-plan-descriptors.png)

<span data-ttu-id="95dfa-158">Voici une vue des colonnes de descripteurs du plan de gestion de fichiers dans l’onglet des étiquettes du gestionnaire de plan gestion de fichiers.</span><span class="sxs-lookup"><span data-stu-id="95dfa-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a><span data-ttu-id="95dfa-160">Exporter toutes les étiquettes de rétention existantes pour analyser et/ou effectuer des révisions en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="95dfa-160">Export all existing retention labels to analyze and/or perform offline reviews</span></span>

<span data-ttu-id="95dfa-161">Depuis le gestionnaire de plan de gestion de fichiers, vous pouvez exporter les détails de toutes les étiquettes de conservation dans un fichier .csv pour vous aider à fournir des évaluations périodiques de conformité aux responsables de la gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="95dfa-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="95dfa-162">Pour exporter toutes les étiquettes de conservation, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Exporter les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="95dfa-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Option d’export de plan de gestion de fichiers](media/file-plan-export-labels-option.png)

<span data-ttu-id="95dfa-164">Un fichier \*.csv contenant toutes les étiquettes de conservation existantes s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="95dfa-164">A \*.csv file containing all existing retention labels will open.</span></span>

![Fichier CSV affichant toutes les étiquettes de conservation](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a><span data-ttu-id="95dfa-166">Import d’étiquettes de rétention dans votre plan de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="95dfa-166">Import labels into your file plan</span></span>

<span data-ttu-id="95dfa-167">Dans le gestionnaire de plan de gestion de fichiers, vous pouvez importer de nouvelles étiquettes de rétention en bloc mais aussi modifier des étiquettes de rétention existantes.</span><span class="sxs-lookup"><span data-stu-id="95dfa-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="95dfa-168">Pour importer de nouvelles étiquettes de rétention et mettre à jour des étiquettes de rétention existantes, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Importer les étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="95dfa-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Option d’import de plan de gestion de fichiers](media/file-plan-import-labels-option.png)

![Option de téléchargement d’un modèle de plan de gestion de fichiers vide](media/file-plan-blank-template-option.png)

<span data-ttu-id="95dfa-171">Téléchargez un modèle vide (ou démarrez à partir d’un export de votre plan de gestion de fichiers actuel).</span><span class="sxs-lookup"><span data-stu-id="95dfa-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Modèle de plan de gestion de fichiers vide ouvert dans Excel](media/file-plan-blank-template.png)

<span data-ttu-id="95dfa-173">Complétez le modèle (prochainement : informations de référence sur les combinaisons valides de valeurs pour une seule étiquette de rétention).</span><span class="sxs-lookup"><span data-stu-id="95dfa-173">Fill-out the template (coming soon: reference information about valid value combinations for a single retention label).</span></span>

![Modèle de plan de gestion de fichiers complété](media/file-plan-filled-out-template.png)

<span data-ttu-id="95dfa-175">Chargez le modèle complété et le gestionnaire de plan de gestion de fichiers validera les entrées et affichera les statistiques d’importation.</span><span class="sxs-lookup"><span data-stu-id="95dfa-175">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Statistiques d’importation de plan de gestion de fichiers](media/file-plan-import-statistics.png)

<span data-ttu-id="95dfa-177">En cas d’erreur de validation, l’importation de plan de fichiers continuera à valider chaque entrée dans le fichier d’importation et affichera toutes les erreurs faisant référence aux numéros de ligne/ligne dans le fichier d’importation, copiera les résultats d’erreur affichés afin de pouvoir facilement revenir au fichier d’importation et corriger les erreurs.</span><span class="sxs-lookup"><span data-stu-id="95dfa-177">In the event there is a validation error, file plan import will continue to validate every entry in the import file and display all errors referencing line/row numbers in the import file, copy the displayed error results so that you can easilly return to the import file and correct the errors.</span></span> 

<span data-ttu-id="95dfa-178">Une fois l’importation terminée, accédez à nouveau au gestionnaire de plan de gestion de fichiers pour attribuer de nouvelles étiquettes de rétention aux stratégies de rétention nouvelles ou existantes.</span><span class="sxs-lookup"><span data-stu-id="95dfa-178">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Option de publication d’étiquettes](media/file-plan-publish-labels-option.png)

