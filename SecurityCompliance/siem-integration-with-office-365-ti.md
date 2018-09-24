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
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="a1c60-103">Intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées</span><span class="sxs-lookup"><span data-stu-id="a1c60-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="a1c60-p101">Si votre organisation utilise un serveur de gestion (SIEM) d’incident et des événements de sécurité, vous pouvez intégrer Office 365 menaces et protection contre les menaces avancées avec votre serveur SIEM. Intégration SIEM vous permet d’afficher des informations, telles que les logiciels malveillants détectés par Office 365 Advanced Protection et sur les menaces, dans les rapports de serveur SIEM. Pour configurer l’intégration de SIEM, vous utilisez l' [API de gestion d’Office 365 activité](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="a1c60-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="a1c60-p102">L’API de gestion Office 365 activité récupère des informations sur l’utilisateur, d’administration et actions de stratégie et d’événements à partir d’Office 365 et les journaux d’activité Azure Active Directory de votre organisation. [Office 365 avancée protection contre les menaces et les menaces schéma](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) fonctionne avec les menaces et/ou avancée contre les menaces, afin que si votre organisation a contre les menaces avancées, mais pas sur les menaces (ou vice versa), vous pouvez toujours utiliser la même API pour l’intégration de votre serveur la SIEM.</span><span class="sxs-lookup"><span data-stu-id="a1c60-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="a1c60-p103">Le serveur SIEM ou un autre système similaire doit interroger la charge de travail **audit.general** aux événements de détection d’accès. Pour en savoir plus, voir [mise en route des API de gestion Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="a1c60-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a1c60-111">Vous devez être un administrateur global d’Office 365 ou avoir le rôle d’administrateur de sécurité affecté dans le centre de conformité & de sécurité à configurer l’intégration SIEM avec Office 365 menaces et de protection contre les menaces avancées.</span><span class="sxs-lookup"><span data-stu-id="a1c60-111">You must be an Office 365 global administrator or have the security administrator role assigned in the Security & Compliance Center to set up SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection.</span></span><br/><span data-ttu-id="a1c60-p104">Enregistrement d’audit doit être activée pour votre environnement Office 365. Pour obtenir l’aide à ce sujet, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="a1c60-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c60-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1c60-114">Related topics</span></span>

[<span data-ttu-id="a1c60-115">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="a1c60-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="a1c60-116">Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a1c60-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="a1c60-117">Active les rapports et les vues d’ensemble de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a1c60-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="a1c60-118">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="a1c60-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

