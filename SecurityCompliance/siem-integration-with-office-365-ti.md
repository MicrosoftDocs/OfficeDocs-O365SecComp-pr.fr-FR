---
title: Intégration SIEM avec Office 365 protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
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
description: Intégrez le serveur SIEM de votre organisation avec Office 365 protection avancée contre les menaces et les événements de menace associés dans l’API de gestion des activités Office 365.
ms.openlocfilehash: 4bfc82be273bb4581aa49bbbbdab613bd87b1b89
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600901"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="2ed85-103">Intégration SIEM avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2ed85-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="2ed85-104">Si votre organisation utilise un serveur de gestion des événements et des incidents de sécurité (SIEM), vous pouvez intégrer Office 365 Advanced Threat Protection à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="2ed85-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="2ed85-105">L’intégration SIEM vous permet d’afficher des informations, telles que des programmes malveillants ou des hameçons détectés par Office 365 Advanced protection, dans vos rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="2ed85-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="2ed85-106">Pour configurer l’intégration SIEM, vous utilisez l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="2ed85-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="2ed85-107">L’API de gestion des activités Office 365 récupère des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2ed85-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="2ed85-108">Le [schéma de protection avancée contre les menaces office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) fonctionne avec la protection avancée contre les menaces, de sorte que si votre organisation a le plan 1 ou plan 2 ou Office 365 E5 Office 365 Advanced Threat Protection, vous pouvez toujours utiliser cette même API pour votre intégration de serveur Siem.</span><span class="sxs-lookup"><span data-stu-id="2ed85-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="2ed85-109">Le serveur SIEM ou un autre système similaire doit interroger l' **audit.** charge de travail générale pour accéder aux événements de détection.</span><span class="sxs-lookup"><span data-stu-id="2ed85-109">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="2ed85-110">Pour plus d’informations, consultez la rubrique [prise en main des API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="2ed85-110">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="2ed85-111">En outre, les valeurs suivantes de **AuditLogRecordType** sont pertinentes pour les événements ATP Office 365:</span><span class="sxs-lookup"><span data-stu-id="2ed85-111">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="2ed85-112">Énumération : AuditLogRecordType - Type : Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="2ed85-112">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="2ed85-113">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="2ed85-113">AuditLogRecordType</span></span>

|<span data-ttu-id="2ed85-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ed85-114">Value</span></span>|<span data-ttu-id="2ed85-115">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="2ed85-115">Member name</span></span>|<span data-ttu-id="2ed85-116">Description</span><span class="sxs-lookup"><span data-stu-id="2ed85-116">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ed85-117">vingt</span><span class="sxs-lookup"><span data-stu-id="2ed85-117">28</span></span>|<span data-ttu-id="2ed85-118">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="2ed85-118">ThreatIntelligence</span></span>|<span data-ttu-id="2ed85-119">Événements d’hameçonnage et de programmes malveillants depuis Exchange Online Protection et Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="2ed85-119">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="2ed85-120">41</span><span class="sxs-lookup"><span data-stu-id="2ed85-120">41</span></span>|<span data-ttu-id="2ed85-121">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="2ed85-121">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="2ed85-122">Les événements de la protection avancée contre les menaces des liens approuvés ATP (temps de blocage) et de blocage d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ed85-122">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="2ed85-123">47</span><span class="sxs-lookup"><span data-stu-id="2ed85-123">47</span></span>|<span data-ttu-id="2ed85-124">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="2ed85-124">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="2ed85-125">Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft teams à partir d’Office 365 protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="2ed85-125">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="2ed85-126">Vous devez être un administrateur général Office 365 ou faire en sorte que le rôle administrateur de sécurité soit affecté au centre de sécurité & conformité afin de configurer l’intégration SIEM avec Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="2ed85-126">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="2ed85-127">L’enregistrement d’audit doit être activé pour votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ed85-127">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="2ed85-128">Pour obtenir de l’aide, voir [activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="2ed85-128">To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed85-129">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="2ed85-129">Related topics</span></span>

[<span data-ttu-id="2ed85-130">Enquête et réponse aux menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="2ed85-130">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)

[<span data-ttu-id="2ed85-131">Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2ed85-131">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="2ed85-132">Rapports intelligents et Insights dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="2ed85-132">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="2ed85-133">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="2ed85-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  
