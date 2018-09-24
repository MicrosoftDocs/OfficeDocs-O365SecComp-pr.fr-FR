---
title: Intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Intégrer le serveur de votre organisation SIEM avec Office 365 menaces et contre les menaces avancées avec l’API de gestion Office 365 activité.
ms.openlocfilehash: 057d8ac101b96f37846ac751645934279d45dc88
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972256"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées

Si votre organisation utilise un serveur de gestion (SIEM) d’incident et des événements de sécurité, vous pouvez intégrer Office 365 menaces et protection contre les menaces avancées avec votre serveur SIEM. Intégration SIEM vous permet d’afficher des informations, telles que les logiciels malveillants détectés par Office 365 Advanced Protection et sur les menaces, dans les rapports de serveur SIEM. Pour configurer l’intégration de SIEM, vous utilisez l' [API de gestion d’Office 365 activité](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

L’API de gestion Office 365 activité récupère des informations sur l’utilisateur, d’administration et actions de stratégie et d’événements à partir d’Office 365 et les journaux d’activité Azure Active Directory de votre organisation. [Office 365 avancée protection contre les menaces et les menaces schéma](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) fonctionne avec les menaces et/ou avancée contre les menaces, afin que si votre organisation a contre les menaces avancées, mais pas sur les menaces (ou vice versa), vous pouvez toujours utiliser la même API pour l’intégration de votre serveur la SIEM. 

Le serveur SIEM ou un autre système similaire doit interroger la charge de travail **audit.general** aux événements de détection d’accès. Pour en savoir plus, voir [mise en route des API de gestion Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Vous devez être un administrateur global d’Office 365 ou avoir le rôle d’administrateur de sécurité affecté dans le centre de conformité & de sécurité à configurer l’intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées.<br/>Enregistrement d’audit doit être activée pour votre environnement Office 365. Pour obtenir l’aide à ce sujet, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Voir aussi

[Office 365 Threat Intelligence](office-365-ti.md)

[Office 365 - Protection avancée contre les menaces](office-365-atp.md)

[Active les rapports et les vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md)
  
[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

