---
title: API Activité de gestion Office 365
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
- M365-analytics
description: Résumé succinct de l'API activité de gestion d'Office 365.
ms.openlocfilehash: 3405eaac000111fb5d5f054edcbe6816aa9af9e7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262556"
---
# <a name="office-365-management-activity-api"></a>API Activité de gestion Office 365
Microsoft fournit des services de création de rapports qui permettent aux administrateurs d'obtenir des informations transactionnelles agrégées sur leur client Office 365. L' [API activité de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) utilise une conception standard RESTful et OAuth v2 pour l'authentification, ce qui facilite le lancement de l'expérimentation des données et leur ingestion dans les applications et les outils de visualisation. L'API fournit un flux de données qui inclut des informations sur l'activité de l'utilisateur, de l'administrateur, des opérations et de la sécurité dans Office 365. Les données peuvent être conservées à des fins de réglementation ou associées à des données de journal fournies à partir d'une infrastructure locale ou d'autres sources pour créer une solution de surveillance pour les opérations, la sécurité et la conformité dans l'ensemble de l'entreprise.

L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory. L'API fournit un schéma d'audit cohérent avec plus de 10 champs communs à tous les services. Cela permet aux organisations de se connecter facilement entre les événements et de créer des raisons de conséquence sur les données. Des dizaines de fournisseurs de logiciels indépendants (ISV) ont conclu un partenariat avec Microsoft et des solutions bâties basées sur l'API. Certaines solutions sont axées uniquement sur les données Office 365, tandis que d'autres permettent d'ingérer les données de plusieurs fournisseurs de Cloud et de systèmes locaux afin de créer une vue unifiée de toutes les opérations, de la sécurité et de l'activité liée à la conformité. Pour plus d'informations, reportez-vous à la [référence API activité de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).
