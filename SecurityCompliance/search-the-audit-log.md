---
title: Rechercher les activités des utilisateurs et des administrateurs dans le journal d’audit Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: "Le journal d'audit Office 365 est un journal d'audit unifié. Pourquoi un journal d'audit unifié? Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d'audit que vous pouvez rechercher. Cela signifie que vous pouvez rechercher l'activité de l'utilisateur et de l'administrateur dans les services suivants:"
ms.openlocfilehash: d964a1404dd022ba9b56e5d86766c5fc6eabf10a
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296517"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="29778-106">Rechercher les activités des utilisateurs et des administrateurs dans le journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="29778-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="29778-p102">Le journal d'audit Office 365 est un journal d'audit unifié. Pourquoi un journal d'audit unifié? Étant donné que les événements provenant de la plupart des services Office 365 auxquels vous êtes abonné, sont enregistrés dans un seul journal d'audit que vous pouvez rechercher. Cela signifie que vous pouvez rechercher l'activité de l'utilisateur et de l'administrateur dans les services suivants:</span><span class="sxs-lookup"><span data-stu-id="29778-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="29778-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="29778-111">SharePoint</span></span>
- <span data-ttu-id="29778-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="29778-112">OneDrive</span></span>
- <span data-ttu-id="29778-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="29778-113">Exchange</span></span>
- <span data-ttu-id="29778-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="29778-114">Azure Active Directory</span></span>
- <span data-ttu-id="29778-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="29778-115">Microsoft Teams</span></span>
- <span data-ttu-id="29778-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="29778-116">eDiscovery</span></span>
- <span data-ttu-id="29778-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="29778-117">Power BI</span></span>
- <span data-ttu-id="29778-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="29778-118">Yammer</span></span>
- <span data-ttu-id="29778-119">Sway</span><span class="sxs-lookup"><span data-stu-id="29778-119">Sway</span></span>
- <span data-ttu-id="29778-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="29778-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="29778-121">Configurer l'audit</span><span class="sxs-lookup"><span data-stu-id="29778-121">Set up auditing</span></span>
  
<span data-ttu-id="29778-122">Vous devez effectuer quelques opérations avant de pouvoir effectuer une recherche dans le journal d'audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="29778-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="29778-123">[Activer la recherche du journal d'audit](turn-audit-log-search-on-or-off.md) pour commencer l'enregistrement des événements que vous pouvez rechercher</span><span class="sxs-lookup"><span data-stu-id="29778-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="29778-124">[Activer l'audit de boîte aux lettres](enable-mailbox-auditing.md) pour pouvoir Rechercher des événements liés à une boîte aux lettres; par exemple lorsqu'un utilisateur se connecte à sa boîte aux lettres ou purge des éléments de son dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="29778-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="29778-125">Rechercher le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="29778-125">Search the audit log</span></span>
  
<span data-ttu-id="29778-126">Après avoir activé l'audit, vous recherchez des centaines de types d'événements individuels à partir de plusieurs services Office 365.</span><span class="sxs-lookup"><span data-stu-id="29778-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="29778-127">Rechercher les activités de l'utilisateur et de l'administrateur dans [le journal d'audit](search-the-audit-log-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="29778-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="29778-128">[Comprendre les propriétés détaillées](detailed-properties-in-the-office-365-audit-log.md) de chaque enregistrement d'audit inclus dans les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="29778-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="29778-129">[Rechercher les activités de découverte électronique](search-for-ediscovery-activities-in-the-audit-log.md) effectuées par les administrateurs et les responsables de la conformité</span><span class="sxs-lookup"><span data-stu-id="29778-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
