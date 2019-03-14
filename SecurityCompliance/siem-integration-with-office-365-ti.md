---
title: Intégration SIEM avec Office 365 protection avancée contre les menaces
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
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: Intégrez le serveur SIEM de votre organisation avec Office 365 protection avancée contre les menaces et les événements de menace associés dans l'API de gestion des activités Office 365.
ms.openlocfilehash: fa9dcda0556684b748068cbe5ee848ba443d7667
ms.sourcegitcommit: f25a667e4c7d11c43c87604d576f1e6d6155b14f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2019
ms.locfileid: "30536174"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a>Intégration SIEM avec Office 365 protection avancée contre les menaces

Si votre organisation utilise un serveur de gestion des événements et des incidents de sécurité (SIEM), vous pouvez intégrer Office 365 Advanced Threat Protection à votre serveur SIEM. L'intégration SIEM vous permet d'afficher des informations, telles que des programmes malveillants ou des hameçons détectés par Office 365 Advanced protection, dans vos rapports de serveur SIEM. Pour configurer l'intégration SIEM, vous utilisez l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

L'API de gestion des activités Office 365 récupère des informations sur les actions et événements d'utilisateur, d'administrateur, de système et de stratégie à partir des journaux d'activité Office 365 et Azure Active Directory de votre organisation. Le [schéma de protection avancée contre les menaces office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) fonctionne avec la protection avancée contre les menaces, de sorte que si votre organisation a le plan 1 ou plan 2 ou Office 365 E5 Office 365 Advanced Threat Protection, vous pouvez toujours utiliser cette même API pour votre intégration de serveur Siem. 

Le serveur SIEM ou un autre système similaire doit interroger l' **audit.** charge de travail générale pour accéder aux événements de détection. Pour plus d'informations, consultez la rubrique [prise en main des API de gestion d'Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). En outre, les valeurs suivantes de **AuditLogRecordType** sont pertinentes pour les événements ATP Office 365:

### <a name="enum-auditlogrecordtype---type-edmint32"></a>Énumération : AuditLogRecordType - Type : Edm.Int32

#### <a name="auditlogrecordtype"></a>AuditLogRecordType

|Valeur|Nom du membre|Description|
|:-----|:-----|:-----|
|vingt|ThreatIntelligence|Événements d’hameçonnage et de programmes malveillants depuis Exchange Online Protection et Office 365 Advanced Threat Protection.|
|41|ThreatIntelligenceUrl|Les événements de la protection avancée contre les menaces des liens approuvés ATP (temps de blocage) et de blocage d'Office 365.|
|47|ThreatIntelligenceAtpContent|Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft teams à partir d'Office 365 protection avancée contre les menaces.|

> [!IMPORTANT]
> Vous devez être un administrateur général Office 365 ou avoir le rôle administrateur de sécurité affecté au centre de sécurité & Compliance Center pour configurer l'intégration SIEM avec Office 365 Advanced Threat Protection.<br/>L'enregistrement d'audit doit être activé pour votre environnement Office 365. Pour obtenir de l'aide, voir [activer ou désactiver la recherche dans le journal d'audit Office 365](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Voir aussi

[Enquête et réponse aux menaces Office 365](office-365-ti.md)

[Office 365 - Protection avancée contre les menaces](office-365-atp.md)

[Rapports intelligents et Insights dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  
