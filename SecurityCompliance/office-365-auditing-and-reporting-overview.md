---
title: L’audit et les rapports dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Vue d’ensemble de fonctionnalités dans Office 365, ainsi que pour l’Assurance Service de création de rapports et de l’audit.
ms.openlocfilehash: 055a24523260bf14220d5436dcdd010f31f5d8cd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528380"
---
# <a name="auditing-and-reporting-in-office-365"></a>L’audit et les rapports dans Office 365

## <a name="introduction"></a>Présentation
Services de cloud computing Microsoft inclut plusieurs audit et rapports de fonctionnalités que les clients peuvent utiliser pour effectuer le suivi d’utilisateur et l’activité d’administration au sein de leurs clients, tels que les modifications apportées à leurs paramètres de configuration de client SharePoint Online et Exchange Online et les modifications apportées par les utilisateurs aux documents et autres éléments. Clients peuvent utiliser les informations d’audit et les rapports disponibles dans les services en nuage pour mieux gérer l’expérience utilisateur, réduire les risques et remplir les obligations de conformité.

## <a name="office-365-security--compliance-center"></a>Centre de conformité et sécurité dans Office 365
[Office 365 sécurité & centre de conformité](https://support.office.com/article/Go-to-the-Office-365-Security-Compliance-Center-7e696a40-b86b-4a20-afcc-559218b7b1b8) est un portail unique pour la protection de vos données dans Office 365, et il inclut de nombreux audit et fonctions de rapport. Il s’agit d’une évolution du centre de conformité Office 365. La sécurité et le centre de conformité est conçu pour les organisations dont les données protection ou en matière de conformité ou qui souhaitent auditer l’activité utilisateur et l’administrateur. Vous pouvez utiliser la sécurité et le centre de conformité pour gérer la conformité pour toutes les données de votre organisation Office 365. Vous pouvez accéder à la sécurité et le centre de conformité à [http://protection.office.com](http://protection.office.com/) à l’aide de votre compte d’administrateur Office 365.

La sécurité et le centre de conformité inclut les volets de navigation qui vous permettre d’accéder à plusieurs fonctionnalités :
- **Alertes** - vous permet de gérer les alertes, afficher les alertes relatives à la sécurité, et gérer les alertes avancés à l’aide de la [Gestion de la sécurité avancée](https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475). 
- **Autorisations** - vous permet d' [attribuer des autorisations](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) telles que l’administrateur de conformité, eDiscovery Manager et d’autres personnes à des personnes dans votre organisation afin qu’ils puissent effectuer des tâches dans la sécurité et le centre de conformité. Vous pouvez affecter des autorisations pour la plupart des fonctionnalités de la sécurité et le centre de conformité, mais les autres autorisations doivent être configurées à l’aide du centre d’administration Exchange et le centre d’administration SharePoint.
- **Gestion des menaces** - vous permet de créer et appliquer des stratégies de gestion des périphériques à l’aide de la [Gestion des périphériques mobiles Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), pour définir des stratégies de [Prévention des pertes de données](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) pour votre organisation, pour configurer le filtrage, le courrier anti-programme malveillant, DomainKeys DKIM (Identified Mail), les pièces jointes fiables, liens fiables et autorisations d’application.
- **Gouvernance de données** - vous permet d' [Importer le courrier électronique ou des données SharePoint à partir d’autres systèmes dans Office 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [configurer des boîtes aux lettres d’archivage](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)et définir des [stratégies de rétention](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) pour la messagerie et autres contenus au sein de votre organisation.
- **Recherche & enquête** - fournit des outils de [recherche de contenu](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [journal d’audit](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), mise en quarantaine et [Gestion des cas eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) rapidement les détails en activité entre les boîtes aux lettres d’Exchange Online, groupes et les dossiers publics, SharePoint En ligne et OneDrive for Business.
- **Rapports** - vous permet d’accéder rapidement aux [rapports](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) pour SharePoint Online, OneDrive pour les entreprises, Exchange Online et Azure AD.
- **Assurance de Service** - fournit des informations sur la façon dont Microsoft gère sécurité, de confidentialité et de conformité aux normes globales pour Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune et autres services en nuage. Inclut également accès à des tiers ISO, sociale et autres rapports d’audit, ainsi que des contrôles audités, qui fournit des détails sur les différents contrôles qui ont été testés et vérifiés par les auditeurs tiers d’Office 365.

## <a name="service-assurance"></a>Assurance de service
Nombre de nos clients dans les secteurs régulés sont soumises aux exigences de conformité complète. Pour effectuer leurs propre évaluation des risques, les clients doivent souvent des informations détaillées sur la façon dont Office 365 gère la sécurité et la confidentialité de leurs données. Microsoft s’engage à la sécurité et la confidentialité des données du client dans ses services de cloud et obtenant client approbation en fournissant une vue transparente de ses opérations et accès aisé aux rapports de conformité indépendant et évaluations.

Service Assurance fournit la transparence des opérations et des informations sur la façon dont Microsoft gère la sécurité, la confidentialité et la conformité des données du client dans Office 365. Il inclut des rapports d’audit tiers ainsi que d’une bibliothèque de livres blancs, des questions fréquentes et autres documents sur Office 365 sujets tels que le chiffrement des données, la résistance des données, la gestion des incidents sécurité et bien plus encore. Les clients peuvent utiliser ces informations pour effectuer leurs propres évaluations des risques réglementaires. Responsables de la conformité peuvent attribuer le rôle de « Service Assurance utilisateur » accorder aux utilisateurs l’accès à l’Assurance de Service. L’administrateur de clients peut également fournir des utilisateurs externes, tels que les auditeurs indépendants, l’accès à des informations dans le tableau de bord pour l’Assurance Service via le [Portail de confiance Microsoft Cloud Service](http://aka.ms/STP) (STP). Pour plus d’informations sur la façon d’accéder à la STP, visitez le site [prendre en main le portail du Service gestion de la confidentialité pour Office 365 pour entreprises, Azure et Dynamics CRM Online abonnements](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>OneDrive entreprise centre d’administration
Le nouveau centre d’administration Microsoft OneDrive permet de rapidement et facilement gérer OneDrive votre organisation paramètres d’entreprise à un seul endroit. Pour utiliser le centre d’administration de OneDrive, vous devez autoriser l’accès aux onedrive.com. Vous devez également être un administrateur global pour votre organisation ou un administrateur personnalisé avec le rôle d’administrateur SharePoint. Accéder à la présentation de centre d’administration Business à OneDrive [https://admin.onedrive.com](https://admin.onedrive.com/).

Les principales fonctionnalités incluent une zone de conformité qui offre aux administrateurs des liens vers le centre de conformité et de sécurité pour Microsoft Office 365 pour les scénarios clés telles que la recherche dans le journal d’audit, utilisation de DLP, de conservation, découverte et d’alerte.

## <a name="related-links"></a>Liens connexes
- [Fonctionnalités de recherche et de découverte électronique](office-365-ediscovery-and-search-features.md)
- [Fonctionnalités de création de rapports Office 365](office-365-reporting-features.md)
- [Activités de gestion d’Office 365 API](office-365-management-activity-api.md)
- [Migrations de boîtes aux lettres Office 365](office-365-mailbox-migrations.md)
- [Enregistrement interne pour ingénierie Office 365](office-365-internal-logging.md)