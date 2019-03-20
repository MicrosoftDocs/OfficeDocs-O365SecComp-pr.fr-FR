---
title: Intégration de serveur SIEM à Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: "Résumé: consultez cet article pour obtenir une vue d'ensemble de l'intégration de serveur SIEM à Microsoft 365."
ms.openlocfilehash: 905f6fc9b6fd62748e25c27d6e5cdbedacc0f806
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693643"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Intégration de serveur SIEM aux services et applications Microsoft 365

## <a name="overview"></a>Vue d’ensemble

Si votre organisation utilise un serveur de gestion des événements et des informations de sécurité (SIEM), ou si vous envisagez d'obtenir rapidement un serveur SIEM, vous vous demandez peut-être comment l'intégrer à votre Microsoft 365, y compris Office 365 Enterprise. La nécessité d'un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation. Microsoft 365 offre plusieurs fonctionnalités de sécurité; Toutefois, si votre organisation dispose de contenu et d'applications sur site et dans le Cloud (comme dans le cas d'un déploiement de Cloud hybride), vous pouvez envisager d'ajouter un serveur SIEM pour une protection supplémentaire. Ou, si votre organisation a des exigences de sécurité particulièrement rigoureuses que vous devez respecter, vous pouvez envisager d'ajouter un serveur SIEM à votre environnement.

## <a name="siem-server-integration-microsoft-365"></a>Intégration de serveur SIEM Microsoft 365

Un serveur SIEM peut recevoir des données à partir d'un large éventail de services et d'applications Microsoft 365. Le tableau suivant répertorie plusieurs applications et services Microsoft 365, ainsi que des entrées de serveur SIEM et l'endroit où aller pour en savoir plus sur l'intégration de serveur SIEM. 

| Service ou application Microsoft 365 | Entrées de serveur SIEM | Ressources pour en savoir plus |
| --- | --- | --- |
| [Office 365 - Protection avancée contre les menaces](office-365-atp.md) <br/>   ou   <br/>[Office 365 Threat Intelligence](office-365-ti.md) | Journaux d'audit | [Intégration SIEM avec Office 365 protection avancée contre les menaces](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Intégration des journaux | [Intégration SIEM à la sécurité des applications Cloud Microsoft](https://docs.microsoft.com/cloud-app-security/siem) |
| [Sécurité de l’application cloud Office 365](office-365-cas-overview.md) | Intégration des journaux | [Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | Intégration des journaux | [Attirez les alertes sur vos outils SIEM](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Centre de sécurité Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Protection contre les menaces et détection des menaces) | Alertes | [Exportation de données de sécurité Azure vers la configuration SIEM-pipeline-aperçu](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Azure Active Directory Identity Protection](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Journaux d'audit | [Intégration des journaux d'audit Azure Active Directory](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Advanced Threat Analytics](https://docs.microsoft.com/azure/security/azure-threat-detection) | Intégration des journaux | [Référence du journal ATA SIEM](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>La journalisation d'audit doit être activée.

Assurez-vous que la journalisation d'audit est activée avant de configurer l'intégration de serveur SIEM. 

- Pour SharePoint Online, OneDrive entreprise et Azure Active Directory, [la journalisation d'audit est activée dans le centre de sécurité _AMP_ Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Pour Exchange Online, la [journalisation d'audit est activée avec Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>Voir aussi

[Adoption du cloud et solutions hybrides](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Guides de laboratoire de test d’adoption cloud](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


