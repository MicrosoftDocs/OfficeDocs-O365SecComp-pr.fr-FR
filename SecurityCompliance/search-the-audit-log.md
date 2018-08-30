---
title: Le journal d’audit pour l’activité utilisateur et d’administration de recherche dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Le journal d’audit de Office 365 est un journal d’audit unifiée. Pourquoi un audit unifié se connecter ? Étant donné que les événements à partir de la plupart des services Office 365 que vous êtes organisation s’abonne à sont enregistrées dans un journal d’audit unique que vous pouvez rechercher. Cela signifie que vous pouvez rechercher des utilisateurs et l’activité d’administration dans ces services :'
ms.openlocfilehash: 7a6a552b1d2569c9e21fe20b39d474dafc026172
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527955"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="f22fa-106">Le journal d’audit pour l’activité utilisateur et d’administration de recherche dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f22fa-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="f22fa-p102">Le journal d’audit de Office 365 est un journal d’audit unifiée. Pourquoi un audit unifié se connecter ? Étant donné que les événements à partir de la plupart des services Office 365 que vous êtes organisation s’abonne à sont enregistrées dans un journal d’audit unique que vous pouvez rechercher. Cela signifie que vous pouvez rechercher des utilisateurs et l’activité d’administration dans ces services :</span><span class="sxs-lookup"><span data-stu-id="f22fa-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="f22fa-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="f22fa-111">SharePoint</span></span>
- <span data-ttu-id="f22fa-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="f22fa-112">OneDrive</span></span>
- <span data-ttu-id="f22fa-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f22fa-113">Exchange</span></span>
- <span data-ttu-id="f22fa-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f22fa-114">Azure Active Directory</span></span>
- <span data-ttu-id="f22fa-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f22fa-115">Microsoft Teams</span></span>
- <span data-ttu-id="f22fa-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f22fa-116">eDiscovery</span></span>
- <span data-ttu-id="f22fa-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="f22fa-117">Power BI</span></span>
- <span data-ttu-id="f22fa-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="f22fa-118">Yammer</span></span>
- <span data-ttu-id="f22fa-119">Sway</span><span class="sxs-lookup"><span data-stu-id="f22fa-119">Sway</span></span>
- <span data-ttu-id="f22fa-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="f22fa-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="f22fa-121">Configurer l’audit</span><span class="sxs-lookup"><span data-stu-id="f22fa-121">Set up auditing</span></span>
  
<span data-ttu-id="f22fa-122">Il existe quelques éléments à effectuer avant de rechercher le journal d’audit de Office 365.</span><span class="sxs-lookup"><span data-stu-id="f22fa-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="f22fa-123">[Activer la recherche des journaux d’audit](turn-audit-log-search-on-or-off.md) pour démarrer l’enregistrement des événements que vous pouvez rechercher</span><span class="sxs-lookup"><span data-stu-id="f22fa-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="f22fa-124">[Activer l’audit de boîte aux lettres](enable-mailbox-auditing.md) , vous pouvez rechercher les événements liés à la boîte aux lettres ; par exemple lorsqu’un utilisateur se connecte à leurs boîte aux lettres ou purge des éléments de leur dossier éléments récupérables</span><span class="sxs-lookup"><span data-stu-id="f22fa-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="f22fa-125">Recherche dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="f22fa-125">Search the audit log</span></span>
  
<span data-ttu-id="f22fa-126">Après avoir activé l’audit, vous recherchez des centaines des différents types d’événements à partir de plusieurs services Office 365.</span><span class="sxs-lookup"><span data-stu-id="f22fa-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="f22fa-127">[Recherche le journal d’audit](search-the-audit-log-in-security-and-compliance.md) des activités d’utilisateur et d’administration</span><span class="sxs-lookup"><span data-stu-id="f22fa-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="f22fa-128">[Comprendre les propriétés détaillées](detailed-properties-in-the-office-365-audit-log.md) de chaque enregistrement d’audit inclus dans les résultats de recherche</span><span class="sxs-lookup"><span data-stu-id="f22fa-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="f22fa-129">[Rechercher les activités liées à la découverte](search-for-ediscovery-activities-in-the-audit-log.md) effectuée par les responsables de la conformité et les administrateurs</span><span class="sxs-lookup"><span data-stu-id="f22fa-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
