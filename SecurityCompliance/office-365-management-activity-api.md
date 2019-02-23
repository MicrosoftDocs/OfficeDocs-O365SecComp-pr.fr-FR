---
title: API Activité de gestion Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Résumé succinct de l'API activité de gestion d'Office 365.
ms.openlocfilehash: df90eba0d019a862d4699f3e2aa0a04e88b0c371
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214574"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="f9c0c-103">API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="f9c0c-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="f9c0c-p101">Microsoft fournit des services de création de rapports qui permettent aux administrateurs d'obtenir des informations transactionnelles agrégées sur leur client Office 365. L' [API activité de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) utilise une conception standard RESTful et OAuth v2 pour l'authentification, ce qui facilite le lancement de l'expérimentation des données et leur ingestion dans les applications et les outils de visualisation. L'API fournit un flux de données qui inclut des informations sur l'activité de l'utilisateur, de l'administrateur, des opérations et de la sécurité dans Office 365. Les données peuvent être conservées à des fins de réglementation ou associées à des données de journal fournies à partir d'une infrastructure locale ou d'autres sources pour créer une solution de surveillance pour les opérations, la sécurité et la conformité dans l'ensemble de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="f9c0c-p102">L'API d'activité de gestion Office 365 fournit des informations sur les différents événements et actions de l'utilisateur, de l'administrateur, du système et de stratégie à partir des journaux d'activité Office 365 et Azure Active Directory. L'API fournit un schéma d'audit cohérent avec plus de 10 champs communs à tous les services. Cela permet aux organisations de se connecter facilement entre les événements et de créer des raisons de conséquence sur les données. Des dizaines de fournisseurs de logiciels indépendants (ISV) ont conclu un partenariat avec Microsoft et des solutions bâties basées sur l'API. Certaines solutions sont axées uniquement sur les données Office 365, tandis que d'autres permettent d'ingérer les données de plusieurs fournisseurs de Cloud et de systèmes locaux afin de créer une vue unifiée de toutes les opérations, de la sécurité et de l'activité liée à la conformité. Pour plus d'informations, reportez-vous à la [référence API activité de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="f9c0c-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
