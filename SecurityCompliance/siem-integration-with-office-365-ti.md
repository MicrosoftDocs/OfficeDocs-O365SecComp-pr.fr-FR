---
title: Intégration SIEM avec Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Menaces Office 365 à l’aide de l’API de gestion Office 365 activité s’intègrent server SIEM de votre organisation.
ms.openlocfilehash: 82aeeea53bf87f1555fa68b2784b8fe38a435e15
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528357"
---
# <a name="siem-integration-with-office-365-threat-intelligence"></a><span data-ttu-id="cd5b4-103">Intégration SIEM avec Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="cd5b4-103">SIEM integration with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="cd5b4-p101">Si votre organisation utilise un serveur de gestion (SIEM) d’incident et des événements de sécurité, vous pouvez intégrer Office 365 menaces avec votre serveur SIEM. Cela vous permet d’afficher des informations, telles que les logiciels malveillants détectés par Office 365 menaces, dans les rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="cd5b4-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence with your SIEM server. This enables you to view information, such as malware detected by Office 365 Threat Intelligence, in your SIEM server reports.</span></span>
  
## <a name="use-the-office-365-activity-management-api"></a><span data-ttu-id="cd5b4-106">Utiliser l’API de gestion activité Office 365</span><span class="sxs-lookup"><span data-stu-id="cd5b4-106">Use the Office 365 Activity Management API</span></span>

<span data-ttu-id="cd5b4-p102">Pour intégrer Office 365 menaces à votre serveur SIEM, utilisez l’API de gestion Office 365 activité. Cette API récupère des informations sur l’utilisateur, d’administration et actions de stratégie et d’événements à partir des journaux d’activité de votre organisation Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cd5b4-p102">To integrate Office 365 Threat Intelligence with your SIEM server, use the Office 365 Activity Management API. This API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure AD activity logs.</span></span> 
  
<span data-ttu-id="cd5b4-109">Vous devez être un administrateur global d’Office 365 ou avoir le rôle d’administrateur de sécurité affecté de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd5b4-109">You must be an Office 365 global administrator or have the security administrator role assigned in the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="cd5b4-110">Voir la [référence de l’API d’activité de gestion Office 365](https://msdn.microsoft.com/en-us/office-365/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="cd5b4-110">See [Office 365 Management Activity API reference](https://msdn.microsoft.com/en-us/office-365/office-365-management-activity-api-reference).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="cd5b4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd5b4-111">Related topics</span></span>

[<span data-ttu-id="cd5b4-112">Intelligence des menaces d’Office 365</span><span class="sxs-lookup"><span data-stu-id="cd5b4-112">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="cd5b4-113">Protection contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="cd5b4-113">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="cd5b4-114">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="cd5b4-114">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

