---
title: Limites de ressources Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Informations sur les ressources limitant pour les différentes applications d’Office 365.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528767"
---
# <a name="resource-limits"></a><span data-ttu-id="23ba9-103">Limites des ressources</span><span class="sxs-lookup"><span data-stu-id="23ba9-103">Resource Limits</span></span>

<span data-ttu-id="23ba9-p101">Limites des ressources sont appliquées à l’aide des quotas (limites) et de limitation. Azure Active Directory et les services Office 365 individuels utilisent les deux. Limites sont propres au service et modifier au fil du temps, comme l’ajout de nouvelles fonctionnalités. Pour plus d’informations sur les limites pour les différents services, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="23ba9-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="23ba9-108">Limites du service Active Directory et les restrictions Azure</span><span class="sxs-lookup"><span data-stu-id="23ba9-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="23ba9-109">Limites d'Exchange Online</span><span class="sxs-lookup"><span data-stu-id="23ba9-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="23ba9-110">Limites d'Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="23ba9-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="23ba9-111">Limitations et frontières logicielles SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="23ba9-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="23ba9-112">Skype pour les limites de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="23ba9-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="23ba9-113">API REST de Yammer et limites de débit</span><span class="sxs-lookup"><span data-stu-id="23ba9-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="23ba9-114">Limites de taille de fichier dans balancement</span><span class="sxs-lookup"><span data-stu-id="23ba9-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="23ba9-p102">Outre ces limites, plusieurs mécanismes de limitation sont utilisées dans Azure Active Directory et Office 365. Limitation du service est particulièrement importante, étant donné que les ressources réseau dans des centres de données de Microsoft sont optimisées pour le large éventail de clients qui utilisent les services. Mécanismes de limitation sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="23ba9-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="23ba9-118">Azure Active Directory et Office 365 fonctionnalité au niveau utilisateur limitation limiter le nombre de transactions ou d’appels simultanés (par script ou code) qui peuvent être effectuées par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="23ba9-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="23ba9-p103">Valeur par défaut PowerShell stratégie de limitation est assignée à chaque client lors de la création du client. Ces paramètres affectent les autres éléments, tels que le nombre maximal de sessions simultanées PowerShell pouvant être ouvert par un administrateur unique.</span><span class="sxs-lookup"><span data-stu-id="23ba9-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="23ba9-121">Chaque client Exchange Online possède une stratégie Exchange Web Services (EWS) par défaut qui est réglée pour les opérations EWS du client et de limitation qui s’applique à tous les clients Outlook.</span><span class="sxs-lookup"><span data-stu-id="23ba9-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
