---
title: Intégration SIEM avec Office 365 Threat Intelligence and Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Intégrez le serveur SIEM de votre organisation avec Office 365 Threat Intelligence et Advanced Threat Protection avec l'API de gestion des activités Office 365.
ms.openlocfilehash: cecfb3910520ddf535c50bbe4bccbf200ae8e121
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212734"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Intégration SIEM avec Office 365 Threat Intelligence and Advanced Threat Protection

Si votre organisation utilise un serveur de gestion des événements et des incidents de sécurité (SIEM), vous pouvez intégrer Office 365 Threat Intelligence et Advanced Threat Protection avec votre serveur SIEM. L'intégration SIEM vous permet d'afficher des informations, telles que des programmes malveillants détectés par Office 365 Advanced protection and Threat Intelligence, dans vos rapports de serveur SIEM. Pour configurer l'intégration SIEM, vous utilisez l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

L'API de gestion des activités Office 365 récupère des informations sur les actions et événements d'utilisateur, d'administrateur, de système et de stratégie à partir des journaux d'activité Office 365 et Azure Active Directory de votre organisation. Le [schéma de protection avancée contre](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) les menaces et d'aide à la décision d'Office 365 fonctionne avec l'intelligence des menaces et/ou la protection avancée contre les menaces, de sorte que si votre organisation dispose d'une protection avancée contre les menaces, mais pas de l'intelligence des menaces (ou vice versa), vous pouvez Utilisez toujours cette même API pour votre intégration de serveur SIEM. 

Le serveur SIEM ou un autre système similaire doit interroger l' **audit.** charge de travail générale pour accéder aux événements de détection. Pour plus d'informations, consultez la rubrique [prise en main des API de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Vous devez être un administrateur général Office 365 ou avoir le rôle administrateur de sécurité affecté au centre de sécurité & Compliance Center pour configurer l'intégration SIEM avec Office 365 Advanced Threat Protection.<br/>L'enregistrement d'audit doit être activé pour votre environnement Office 365. Pour obtenir de l'aide, voir [activer ou désactiver la recherche dans le journal d'audit Office 365](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Voir aussi

[Intelligence des menaces d’Office 365](office-365-ti.md)

[Protection avancée contre les menaces dans Office 365](office-365-atp.md)

[Rapports intelligents et Insights dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Autorisations dans le centre de sécurité &amp; conformité Office 365](permissions-in-the-security-and-compliance-center.md)
  

