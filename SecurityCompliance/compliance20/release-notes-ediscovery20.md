---
title: Notes de publication pour Advanced eDiscovery (aperçu)
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
description: Cet article contient les notes de publication pour Advanced eDiscovery (aperçu).
ms.openlocfilehash: 32a02c16fd30e740fcc6e1c99b46775b97590a28
ms.sourcegitcommit: 15202bba32313534da2478b0cd215f32a10c9ef4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30684353"
---
# <a name="release-notes-for-advanced-ediscovery-preview"></a><span data-ttu-id="ba673-103">Notes de publication pour Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="ba673-103">Release notes for Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="ba673-104">Le programme de préversion public pour Advanced eDiscovery est le moyen d'accéder en avant-première aux fonctionnalités et mises à jour à venir.</span><span class="sxs-lookup"><span data-stu-id="ba673-104">The Public Preview program for Advanced eDiscovery is the way to get early access to the upcoming functionality and updates.</span></span> <span data-ttu-id="ba673-105">Pour accéder en avant-première aux fonctionnalités les plus récentes, il vous suffit de créer et d'utiliser un cas avancé eDiscovery (aperçu) dans le centre de sécurité & de la sécurité d'Office 365.</span><span class="sxs-lookup"><span data-stu-id="ba673-105">To get early access to the newest features, just create and use an Advanced eDiscovery (Preview) case in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="ba673-106">Voir [Create a New case](create-new-ediscovery-case.md).</span><span class="sxs-lookup"><span data-stu-id="ba673-106">See [Create a new case](create-new-ediscovery-case.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="ba673-107">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ba673-107">Known issues</span></span>

<span data-ttu-id="ba673-108">**Microsoft Forms**</span><span class="sxs-lookup"><span data-stu-id="ba673-108">**Microsoft Forms**</span></span>

- <span data-ttu-id="ba673-109">Les données correspondant à un formulaire créé avant le 31 janvier 2019 ne pourront pas être recherchées lors de l'utilisation de l'outil de recherche dans Advanced eDiscovery (Preview) pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ba673-109">The data corresponding to a form created before January 31, 2019 will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="ba673-110">Les formulaires créés après cette date seront disponibles pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="ba673-110">Forms created after this date will be available to search.</span></span>

- <span data-ttu-id="ba673-111">Un formulaire créé par un utilisateur peut toujours recevoir des réponses même après la suppression de l'utilisateur qui a créé le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ba673-111">A form created by a user can still receive responses even after the user who created the Form is deleted.</span></span> <span data-ttu-id="ba673-112">Toutefois, les données correspondantes de ces réponses (qui ont eu lieu après la suppression de la boîte aux lettres de dépositaire) ne peuvent pas être recherchées lors de l'utilisation de l'outil de recherche dans Advanced eDiscovery (Preview) pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ba673-112">However, the corresponding data for those responses (that occurred after the custodian mailbox was deleted) will not be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span>
 
<span data-ttu-id="ba673-113">**Microsoft Sway**</span><span class="sxs-lookup"><span data-stu-id="ba673-113">**Microsoft Sway**</span></span>

- <span data-ttu-id="ba673-114">Si un utilisateur modifie un Sway juste avant la suppression du compte d'utilisateur pour le propriétaire de ce Sway, il se peut que ces modifications ne puissent pas être recherchées lors de l'utilisation de l'outil de recherche dans Advanced eDiscovery (Preview) pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ba673-114">If a user edits a sway just prior to the deletion of the user account for the owner of that sway, then those changes may not be be searchable when using the Search tool in Advanced eDiscovery (Preview) to search custodian mailboxes.</span></span> <span data-ttu-id="ba673-115">Sway bloque les modifications apportées à un Sway dès qu'il reçoit un signal indiquant que le compte a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ba673-115">Sway blocks changes to to a sway as soon as it receives a signal that the account was deleted.</span></span> <span data-ttu-id="ba673-116">Toutefois, il existe une petite chance qu'un Sway puisse être modifié avant la réception de ce signal.</span><span class="sxs-lookup"><span data-stu-id="ba673-116">However, there's a small chance that a sway can be edited before this signal is received.</span></span>

## <a name="issues-fixed-in-this-release"></a><span data-ttu-id="ba673-117">Problèmes résolus dans cette version</span><span class="sxs-lookup"><span data-stu-id="ba673-117">Issues fixed in this release</span></span>

- <span data-ttu-id="ba673-118">DCR: gestion des exceptions pour les éléments non indexés et les éléments orphelins</span><span class="sxs-lookup"><span data-stu-id="ba673-118">DCR: Exception handling for unindexed items and orphaned items</span></span>
- <span data-ttu-id="ba673-119">DCR: notifications de blocage</span><span class="sxs-lookup"><span data-stu-id="ba673-119">DCR: Hold notifications</span></span>
- <span data-ttu-id="ba673-120">DCR: dépositaires dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ba673-120">DCR: Custodians in eDiscovery</span></span>

## <a name="whats-new"></a><span data-ttu-id="ba673-121">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ba673-121">What’s new</span></span>

- <span data-ttu-id="ba673-122">**Reconception de la navigation dans le centre de sécurité _AMP_ Compliance Center** – Advanced EDiscovery (Preview) a une nouvelle apparence.</span><span class="sxs-lookup"><span data-stu-id="ba673-122">**Redesigned navigation in the Security & Compliance Center** – Advanced eDiscovery (Preview) has a new look and feel.</span></span> <span data-ttu-id="ba673-123">Utilisez Advanced eDiscovery (aperçu) pour gérer davantage votre flux de travail de cas.</span><span class="sxs-lookup"><span data-stu-id="ba673-123">Use Advanced eDiscovery (Preview) to manage more of your case workflow.</span></span>

- <span data-ttu-id="ba673-124">**Gestion des cas** : il existe une prise en charge supplémentaire pour les nouveaux types de cas.</span><span class="sxs-lookup"><span data-stu-id="ba673-124">**Case management** – There’s additional support for new case types.</span></span> <span data-ttu-id="ba673-125">Vous pouvez également sélectionner et enregistrer vos dossiers récents et favoris.</span><span class="sxs-lookup"><span data-stu-id="ba673-125">You can also select and save your recent and favorite cases.</span></span> <span data-ttu-id="ba673-126">Suivre et surveiller l'activité dans et dans les cas à l'aide de nouveaux tableaux de bord.</span><span class="sxs-lookup"><span data-stu-id="ba673-126">Track and monitor activity within and across cases using new dashboards.</span></span>

- <span data-ttu-id="ba673-127">**Gestion** des dépositaires: ajoutez et supprimez des utilisateurs comme dépositaires de données dans un cas.</span><span class="sxs-lookup"><span data-stu-id="ba673-127">**Custodian management** – Add and remove users as data custodians within a case.</span></span>

- <span data-ttu-id="ba673-128">**Intégration d'Exchange, de onedrive et** de teams: ajoutez automatiquement la boîte aux lettres actuelle d'un utilisateur, le compte OneDrive entreprise et les sites Microsoft teams à un cas.</span><span class="sxs-lookup"><span data-stu-id="ba673-128">**Exchange, OneDrive, and Teams Integration** – Automatically add a user’s current mailbox, OneDrive for Business account, and Microsoft Teams sites to a case.</span></span> 

- <span data-ttu-id="ba673-129">**Communications** des dépositaires: envoyez et gérez les notifications de conservation légale au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ba673-129">**Custodian communications** – Send and manage legal hold notifications on behalf of your organization.</span></span>

- <span data-ttu-id="ba673-130">**Portail dépositaire** : nouveau portail pour les dépositaires pour accéder à leurs notifications d'attente actives.</span><span class="sxs-lookup"><span data-stu-id="ba673-130">**Custodian portal** – New portal for custodians to access their active hold notices.</span></span>

- <span data-ttu-id="ba673-131">**Indexation profonde** : ré-analyse des éléments partiellement indexés à la demande.</span><span class="sxs-lookup"><span data-stu-id="ba673-131">**Deep indexing** – Re-crawl partially indexed items on demand.</span></span>

- <span data-ttu-id="ba673-132">**Correction d'erreur** : correction ou téléchargement des erreurs de traitement; Il s'agit notamment de la prise en charge des types de fichiers volumineux, des fichiers protégés par mot de passe et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="ba673-132">**Error remediation** – Remediate or download processing errors; this include remediation support for large file types, password protected files, and more.</span></span> 

- <span data-ttu-id="ba673-133">**Améliorations de la recherche** : permet de créer une recherche en identifiant des dépositaires et/ou des emplacements.</span><span class="sxs-lookup"><span data-stu-id="ba673-133">**Improvements to search** – Create a search by identifying custodians and/or locations.</span></span>

- <span data-ttu-id="ba673-134">**Jeux de travail** : Gérez, suivez et auditez des ensembles de documents statiques.</span><span class="sxs-lookup"><span data-stu-id="ba673-134">**Working sets** – Manage, track, and audit static sets of documents.</span></span>

- <span data-ttu-id="ba673-135">**Révision** : utilisez une vue native, texte et quasi native pour examiner les documents ajoutés à votre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="ba673-135">**Review** – Use a native, text, and near-native view to review documents added to your working set.</span></span>

- <span data-ttu-id="ba673-136">**Biffer, Baliser et** annoter: Biffer du texte, appliquer des balises et créer des annotations lors de la révision des documents.</span><span class="sxs-lookup"><span data-stu-id="ba673-136">**Redact, tag, and annotate** – Redact text, apply tags, and make annotations as you review documents.</span></span>
  
- <span data-ttu-id="ba673-137">\*\*\*\* Analyse assistée: exploitez l'analyse de découverte électronique pour rechercher, Rechercher et effectuer des recherches dans un jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="ba673-137">**Analytics-powered review**– Leverage eDiscovery analytics to find, search, and cull results within a working set.</span></span>

- <span data-ttu-id="ba673-138">**Travaux** : suivre l'état des processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="ba673-138">**Jobs** – Track status of long-running processes.</span></span>

- <span data-ttu-id="ba673-139">**Nouvelles activités d'audit** : suivez et affichez les nouvelles activités d'audit pour Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="ba673-139">**New audit activities** – Track and view new audit activity for Advanced eDiscovery.</span></span>
