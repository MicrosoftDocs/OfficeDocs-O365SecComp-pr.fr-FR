---
title: Nouveautés du centre de conformité Microsoft 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Tout comme les fonctionnalités du centre de conformité Microsoft 365, notre contenu d’aide est toujours évolutif. Nous créons en permanence de nouveaux articles, en mettant à jour ceux existants et en apportant des modifications en fonction de vos commentaires. Découvrez les nouveautés et mises à jour ce mois-ci.
ms.openlocfilehash: e7600c2f84d0b591c6114c2a61c77d8e2c664056
ms.sourcegitcommit: 9fd606e8d912f4507fbcd9f1fcb9dfcfd20de08b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2019
ms.locfileid: "36980800"
---
# <a name="recent-updates-to-microsoft-365-compliance-content"></a>Mises à jour récentes du contenu de conformité Microsoft 365

Tout comme les fonctionnalités du centre de conformité Microsoft 365, notre contenu d’aide est toujours évolutif. Nous créons en permanence de nouveaux articles, en mettant à jour ceux existants et en apportant des modifications en fonction de vos commentaires. Jetez un œil aux nouveautés et mises à jour ce mois-ci-dessous.

> [!TIP]
> Pour rester au fait des dernières mises à jour des fonctionnalités dans le centre de conformité Microsoft 365, consultez les nouveautés [du centre de conformité microsoft 365](whats-new.md).

## <a name="august-2019"></a>Août 2019

### <a name="auditing"></a>Audit

[Gérer l’audit des boîtes aux lettres](enable-mailbox-auditing.md#more-information) mises<br>Ajout de détails sur la façon dont les événements de journal d’audit de boîte aux lettres sont disponibles uniquement pour les utilisateurs disposant de licences E5 ou de boîtes aux lettres pour lesquelles l’audit de boîte aux lettres a été activé manuellement par un administrateur. De nouveaux conseils sur l’utilisation de la cmdlet **Search-MailboxAuditLog** dans Exchange Online PowerShell pour rechercher dans le journal d’audit des boîtes aux lettres les utilisateurs sans licence E5.

[Effectuer des recherches dans le journal d’audit Office 365 pour résoudre les scénarios courants](auditing-troubleshooting-scenarios.md#investigate-why-there-was-a-successful-login-by-a-user-outside-your-organization) mises<br>Nouvelle section relative à l’utilisation de l’authentification directe pour examiner les connexions réussies par des utilisateurs externes.

### <a name="content-search--ediscovery"></a>Recherche de contenu & eDiscovery

[Configurer le filtrage des autorisations pour la recherche de contenu](permissions-filtering-for-content-search.md#using-a-filters-list-to-combine-filter-types) mises<br>Ajout de détails sur l’utilisation d’une liste de filtres, qui vous permet d’ajouter une boîte aux lettres et des filtres de site à un seul filtre d’autorisations de recherche.

[Recherche de contenu dans Office 365](content-search.md#searching-disconnected-or-de-licensed-mailboxes) mises<br>Ajout de détails sur la recherche de boîtes aux lettres déconnectées ou sous licence.

[Recherche de contenu dans Office 365](content-search.md#searching-for-content-in-a-sharepoint-multi-geo-environment) mises<br>
[Configurer les limites de conformité pour les enquêtes de découverte électronique dans Office 365](set-up-compliance-boundaries.md#searching-and-exporting-content-in-multi-geo-environments) mises<br>Ajout de détails aux deux articles sur la recherche de contenu dans des environnements multi-géo SharePoint.

### <a name="data-governance"></a>Gouvernance des données

[Vue d’ensemble d’un archivage illimité dans Office 365](unlimited-archiving.md#how-auto-expanding-archiving-works) mises<br>Ajout de détails sur la façon dont Office 365 ajoute un maximum de 20 Archives auxiliaires pour un total de 1 to de stockage supplémentaire.

### <a name="data-investigations"></a>Enquêtes de données

[Supprimer des éléments de leur emplacement d’origine](datainvestigations/delete-items-from-original-locations.md) nouveaux<br>Désormais disponible en aperçu, vous pouvez sélectionner des éléments dans un jeu de preuves, puis les supprimer de leur emplacement d’origine dans Exchange, SharePoint et OneDrive.

[Gérer un incident de fuite de données dans Microsoft 365](datainvestigations/manage-data-spillage-incidents.md#step-4-delete-the-spilled-data) mises<br>Ajout de détails sur l’utilisation de la nouvelle fonctionnalité « supprimer des éléments de leur emplacement d’origine » pour supprimer les données propagées.

### <a name="permissions"></a>Autorisations

[Autorisations dans le centre de conformité microsoft 365 et le centre de sécurité microsoft 365](permissions-microsoft-365-compliance-security.md) nouveaux<br>Les nouveaux groupes de rôles Azure Active Directory ont été publiés dans la version préliminaire publique.

### <a name="records-management"></a>Gestion des enregistrements

[Vue d’ensemble du gestionnaire de plan de gestion de fichiers (mis à jour)](file-plan-manager.md#export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews)<br>Ajout d’un tableau qui répertorie les valeurs valides à utiliser dans le modèle Excel.

### <a name="supervision"></a>Supervision

[Stratégies de surveillance dans Office 365](supervision-policies.md) mises<br>Clarification de la prise en charge des listes de distribution et des groupes Office 365, ajout de conseils pour les correspondances de mots clés dans les e-mails et les pièces jointes et clarification de la prise en charge d’Outlook au sein des canaux teams

### <a name="windows-information-protection"></a>Protection des informations Windows

[Liste des applications Microsoft pour une utilisation avec la protection des informations Windows (WIP)](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/enlightened-microsoft-apps-and-wip) mises <br>Microsoft 3D Viewer est désormais un outil d’application.
