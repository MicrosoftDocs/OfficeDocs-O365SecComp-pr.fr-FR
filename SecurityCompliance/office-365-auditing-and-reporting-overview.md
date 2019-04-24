---
title: Audit et création de rapports dans les services Cloud de Microsoft
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
description: Vue d'ensemble des fonctionnalités d'audit et de création de rapports dans Office 365, Microsoft 365 et service assurance.
ms.openlocfilehash: a5df0dcb6f762723c6ec0102b2c39f1bc157720c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262966"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Audit et création de rapports dans les services Cloud de Microsoft

## <a name="introduction"></a>Introduction
Les services Cloud Microsoft incluent plusieurs fonctionnalités d'audit et de création de rapports que les clients peuvent utiliser pour effectuer le suivi de l'activité des utilisateurs et de l'administration au sein de leur client, telles que les modifications apportées à leurs paramètres de configuration client Exchange Online et SharePoint Online. et les modifications apportées par les utilisateurs aux documents et autres éléments. Les clients peuvent utiliser les informations d'audit et les rapports disponibles dans nos services Cloud pour gérer plus efficacement l'expérience utilisateur, réduire les risques et respecter les obligations de conformité.

## <a name="security--compliance-centers"></a>Centre de sécurité & conformité
Le centre de sécurité [& de sécurité Office 365](https://protection.office.com), le centre de [sécurité Microsoft 365](https://security.microsoft.com)et le [Centre de conformité Microsoft 365](https://compliance.microsoft.com) sont des portails d'un seul point pour protéger les données de votre organisation, et ils incluent un grand nombre d'audits et de rapports offre. Ces centres sont conçus pour les organisations qui ont des besoins en matière de protection des données ou de conformité, ou qui souhaitent auditer l'activité des utilisateurs et des administrateurs. Vous pouvez accéder à ces centres à l'aide de votre compte d'administrateur d'abonnement.

Ces centres incluent des volets de navigation qui vous permettent d'accéder à plusieurs fonctionnalités:
- **Alertes** : permet de gérer les alertes, d'afficher les alertes liées à la sécurité et de gérer les alertes avancées à l'aide de la [sécurité des applications Cloud d'Office 365](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/office-365-cas-overview). 
- **Autorisations** : vous permet d' [attribuer des autorisations](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) telles que l'administrateur de la conformité, le gestionnaire eDiscovery et d'autres personnes à votre organisation afin qu'ils puissent effectuer des tâches dans ces centres. Vous pouvez attribuer des autorisations pour la plupart des fonctionnalités de chaque centre, mais les autres autorisations doivent être configurées à l'aide du centre d'administration Exchange et du centre d'administration SharePoint.
- **Gestion des menaces** : permet de créer et d'appliquer des stratégies de gestion des appareils à l'aide de la [gestion des appareils mobiles Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), afin de configurer les stratégies de [protection contre la perte de données](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) pour votre organisation, afin de configurer le filtrage du courrier électronique, protection contre les programmes malveillants, le courrier électronique DomainKeys Identified identifié, les pièces jointes fiables, les liens fiables et les applications OAuth.
- **Gouvernance des données** : permet d' [importer des données de messagerie ou des données SharePoint à partir d'autres systèmes dans Office 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), de [configurer des boîtes aux lettres](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)d'archivage et de définir des [stratégies](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) de rétention pour le courrier électronique et d'autres contenus au sein de votre organisation.
- **Search & investigation** : fournit des outils de [recherche de contenu](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), de [Journal d'audit](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), de mise en quarantaine et de [gestion des cas eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) pour explorer rapidement les activités dans les boîtes aux lettres, les groupes et les dossiers publics Exchange Online, SharePoint En ligne et OneDrive entreprise.
- **Rapports** : vous permet d'accéder rapidement aux [rapports](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) pour SharePoint Online, OneDrive entreprise, Exchange Online et Azure ad.
- **Service assurance** -fournit des informations sur la façon dont Microsoft gère la sécurité, la confidentialité et la conformité avec les normes globales pour Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune et d'autres services Cloud. Inclut également l'accès à des rapports d'audit, tels que ISO, SOC et d'autres rapports, ainsi que des contrôles audités, qui fournissent des détails sur les différents contrôles qui ont été testés et vérifiés par des auditeurs tiers d'Office 365.

## <a name="service-assurance"></a>Service assurance
De nombreux clients dans les industries réglementées sont soumis à des exigences de conformité étendues. Pour effectuer leurs évaluations des risques propres, les clients ont souvent besoin d'informations détaillées sur la façon dont Office 365 maintient la sécurité et la confidentialité de leurs données. Microsoft s'engage à respecter la sécurité et la confidentialité des données des clients dans ses services Cloud et à bénéficier d'une relation de confiance client en fournissant une vue transparente de ses opérations et un accès facile aux rapports et aux évaluations de conformité indépendantes.

Service assurance fournit la transparence des opérations et des informations sur la façon dont Microsoft conserve la sécurité, la confidentialité et la conformité des données client dans Office 365. Elle inclut des rapports d'audit tiers, ainsi qu'une bibliothèque de livres blancs, de FAQ et d'autres documents sur les sujets Office 365, tels que le chiffrement des données, la résilience des données, la gestion des incidents de sécurité, etc. Les clients peuvent utiliser ces informations pour effectuer leurs propres évaluations de risques réglementaires. Les responsables de la conformité peuvent affecter le rôle «utilisateur d'assurance de service» pour permettre aux utilisateurs d'accéder à l'assurance de service. L'administrateur client peut également fournir aux utilisateurs externes, tels que des auditeurs indépendants, un accès aux informations du tableau de bord service assurance via le [portail d'approbation de service Cloud Microsoft](http://aka.ms/STP) (STP). Pour plus d'informations sur la façon d'accéder au protocole STP, consultez [la prise en main du portail de confiance des services pour Office 365 pour les abonnements pour les entreprises, Azure et Dynamics CRM Online](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>Centre d'administration de OneDrive entreprise
Le nouveau centre d'administration Microsoft OneDrive vous permet de gérer rapidement et facilement les paramètres OneDrive entreprise de votre organisation à un seul endroit. Pour utiliser le centre d'administration OneDrive, vous devez autoriser l'accès à onedrive.com. Vous devez également être administrateur général de votre organisation ou administrateur personnalisé avec le rôle d'administrateur SharePoint. Accédez à l'aperçu du centre d'administration de [https://admin.onedrive.com](https://admin.onedrive.com/)OneDrive entreprise à l'adresse.

Les fonctionnalités clés incluent une zone de conformité qui fournit aux administrateurs des liens vers le centre de gestion approprié pour les scénarios clés tels que la recherche dans le journal d'audit, l'utilisation de DLP, la rétention, la découverte électronique et l'alerte.

## <a name="related-links"></a>Liens connexes
- [eDiscovery et fonctionnalités de recherche](office-365-ediscovery-and-search-features.md)
- [Fonctionnalités de création de rapports Office 365](office-365-reporting-features.md)
- [API Activité de gestion Office 365](office-365-management-activity-api.md)
- [Migrations de boîtes aux lettres Office 365](office-365-mailbox-migrations.md)
- [Journalisation interne pour Office 365 Engineering](office-365-internal-logging.md)