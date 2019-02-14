---
title: Intégration du serveur SIEM avec Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
- M365-security-compliance
description: 'Résumé : Lisez cet article pour obtenir une vue d’ensemble de l’intégration du serveur SIEM avec Microsoft 365.'
ms.openlocfilehash: a6e139d14a7ea3625b2d2fffec5ad5d913ea9184
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995195"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Intégration du serveur SIEM avec 365 Microsoft services et applications

## <a name="overview"></a>Vue d'ensemble

Si votre organisation utilise un serveur d’informations sur la sécurité et de gestion de l’événement (SIEM), ou si vous envisagez d’obtenir un serveur SIEM bientôt, vous vous demandez peut-être comment qui vous intégrer à votre 365 de Microsoft, notamment Office 365 pour entreprises. Si vous avez besoin d’un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation. Microsoft 365 offre une variété de fonctionnalités de sécurité ; Toutefois, si votre organisation dispose de contenu et des applications sur site et dans le nuage (comme dans le cas d’un déploiement de cloud hybride), vous pouvez envisager l’ajout d’un serveur SIEM pour une protection supplémentaire. Ou, si votre organisation a des exigences de sécurité particulièrement stricts à respecter, vous pouvez ajouter un serveur SIEM à votre environnement.

## <a name="siem-server-integration-microsoft-365"></a>Intégration du serveur SIEM 365 Microsoft

Un serveur SIEM peut recevoir des données à partir d’une grande variété d’applications et services Microsoft 365. Le tableau suivant répertorie plusieurs 365 Microsoft services et applications ainsi que les entrées du serveur SIEM et où aller pour en savoir plus sur l’intégration du serveur SIEM. 

| Service Microsoft 365 ou l’Application | Entrées du serveur SIEM | Ressources pour en savoir plus |
| --- | --- | --- |
| [Protection avancée contre les menaces dans Office 365](office-365-atp.md) <br/>   ou   <br/>[Intelligence des menaces d’Office 365](office-365-ti.md) | Journaux d'audit | [Intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Intégration du journal | [Intégration SIEM avec Microsoft Cloud Application Security](https://docs.microsoft.com/cloud-app-security/siem) |
| [Sécurité des applications cloud Office 365](office-365-cas-overview.md) | Intégration du journal | [Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | Intégration du journal | [Extraction des alertes à vos outils SIEM](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Centre de sécurité Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Protection contre les menaces et détection) | Alertes | [Exportation des données de sécurité Azure SIEM - Configuration de Pipeline - aperçu](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Protection d’identité Azure Active Directory](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Journaux d'audit | [Intégrer des journaux d’audit d’Azure Active Directory](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Menaces évoluées Azure Analytique](https://docs.microsoft.com/azure/security/azure-threat-detection) | Intégration du journal | [Référence du journal ATA SIEM](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>Enregistrement d’audit doit être activé.

Assurez-vous que l’enregistrement d’audit est activée avant de configurer l’intégration du serveur SIEM. 

- Pour SharePoint Online, OneDrive for Business et Azure Active Directory, [l’enregistrement d’audit est activé dans le centre de conformité de & sécurité](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Pour Exchange Online, [l’enregistrement d’audit est activée avec Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>Voir aussi

[Adoption du cloud et solutions hybrides](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Guides de laboratoire de test d’adoption cloud](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


