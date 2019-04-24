---
title: Limites des ressources Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Résumé: informations sur les limites de ressources pour les différentes applications dans Office 365.'
ms.openlocfilehash: d4315923ea1ab09e2e7651fb2fcaddb085871d4d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262406"
---
# <a name="resource-limits"></a><span data-ttu-id="e3eea-103">Limites de ressources</span><span class="sxs-lookup"><span data-stu-id="e3eea-103">Resource Limits</span></span>

<span data-ttu-id="e3eea-104">Les limites des ressources sont appliquées à l'aide de quotas (limites) et de la limitation.</span><span class="sxs-lookup"><span data-stu-id="e3eea-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="e3eea-105">Azure Active Directory et les services Office 365 individuels utilisent les deux.</span><span class="sxs-lookup"><span data-stu-id="e3eea-105">Azure Active Directory and the individual Office 365 services use both.</span></span> <span data-ttu-id="e3eea-106">Les limites sont propres aux services et changent au fil du temps lorsque de nouvelles fonctionnalités sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="e3eea-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="e3eea-107">Pour plus d'informations sur les limites actuelles pour les différents services, consultez les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="e3eea-107">For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="e3eea-108">Limites et restrictions du service Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e3eea-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="e3eea-109">Limites d’Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e3eea-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="e3eea-110">Limites d’Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="e3eea-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="e3eea-111">Limites et frontières des logiciels SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e3eea-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="e3eea-112">Limites de Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="e3eea-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="e3eea-113">API REST Yammer et limites de débit</span><span class="sxs-lookup"><span data-stu-id="e3eea-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="e3eea-114">Limites de taille de fichier dans Sway</span><span class="sxs-lookup"><span data-stu-id="e3eea-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="e3eea-115">En plus de ces limites, plusieurs mécanismes de limitation sont utilisés dans Azure Active Directory et Office 365.</span><span class="sxs-lookup"><span data-stu-id="e3eea-115">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365.</span></span> <span data-ttu-id="e3eea-116">La limitation au sein du service est particulièrement importante, étant donné que les ressources réseau dans les centres de données de Microsoft sont optimisées pour l'ensemble des clients qui utilisent les services.</span><span class="sxs-lookup"><span data-stu-id="e3eea-116">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="e3eea-117">Les mécanismes de limitation sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="e3eea-117">Throttling mechanisms include:</span></span>
- <span data-ttu-id="e3eea-118">Azure Active Directory et Office 365 fonctionnalité de limitation au niveau de l'utilisateur, ce qui limite le nombre de transactions ou d'appels simultanés (par script ou code) qui peuvent être exécutés par un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3eea-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="e3eea-119">Une stratégie de limitation PowerShell par défaut est attribuée à chaque client lors de la création du client.</span><span class="sxs-lookup"><span data-stu-id="e3eea-119">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="e3eea-120">Ces paramètres affectent d'autres éléments, tels que le nombre maximal de sessions PowerShell simultanées pouvant être ouvertes par un administrateur unique.</span><span class="sxs-lookup"><span data-stu-id="e3eea-120">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="e3eea-121">Chaque client Exchange Online a une stratégie de services Web Exchange (EWS) par défaut ajustée pour les opérations clientes EWS et la limitation qui s'applique à tous les clients Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3eea-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
