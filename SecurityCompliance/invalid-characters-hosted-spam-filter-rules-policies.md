---
title: Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et la stratégie de filtrage
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Fournit de l'aide aux administrateurs qui ont des caractères non valides dans leur configuration de blocage du courrier indésirable et &amp; génèrent des problèmes lors de la tentative d'utilisation du centre de sécurité conformité.
ms.openlocfilehash: 797389da26823b6528c2aee0baaa118fbfcf7942
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32253952"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="c8411-103">Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et votre stratégie de filtrage</span><span class="sxs-lookup"><span data-stu-id="c8411-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="c8411-104">Auparavant, les administrateurs Office 365 configurent et configurent les règles de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable à l'aide du centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8411-104">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange admin center (EAC).</span></span> <span data-ttu-id="c8411-105">À présent, vous utilisez le &amp; Centre de sécurité conformité pour gérer la configuration de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c8411-105">Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration.</span></span> <span data-ttu-id="c8411-106">Les caractères suivants étaient pris en charge dans le centre d'administration Exchange mais ne sont pas &amp; pris en charge dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="c8411-106">The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="c8411-107">**Caractères non valides:**</span><span class="sxs-lookup"><span data-stu-id="c8411-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="c8411-108">Si vos règles de filtrage du courrier indésirable ou votre stratégie de filtrage du courrier indésirable contient l'un des caractères non valides, vous pouvez rencontrer un ou plusieurs des problèmes suivants:</span><span class="sxs-lookup"><span data-stu-id="c8411-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="c8411-109">Il se peut que vous ne puissiez pas trouver la stratégie ou les &amp; règles dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="c8411-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="c8411-110">Vous pouvez recevoir des erreurs lors de la tentative d'obtention des règles ou de la stratégie à l'aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8411-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="c8411-111">Vous pouvez constater que la stratégie ou les paramètres ne s'exécutent pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c8411-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="c8411-112">Supprimer les caractères non valides de la stratégie et des règles de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c8411-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="c8411-113">Une fois que vous avez identifié la stratégie et les règles qui contiennent des caractères non valides, vous pouvez modifier les noms à l'aide des applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8411-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="c8411-114">[Connectez-vous à Exchange Online à l'aide de Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="c8411-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="c8411-115">Pour modifier le nom de la stratégie de filtrage du courrier indésirable, exécutez la cmdlet Set-HostedContentFilterPolicy comme suit:</span><span class="sxs-lookup"><span data-stu-id="c8411-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="c8411-116">Pour modifier le nom d'une règle de filtrage du courrier indésirable, exécutez la cmdlet Set-Hostedcontentfilterrule permet comme suit:</span><span class="sxs-lookup"><span data-stu-id="c8411-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="c8411-117">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="c8411-117">For more information</span></span>

[<span data-ttu-id="c8411-118">Gestion des menaces dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c8411-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="c8411-119">Set-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="c8411-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="c8411-120">Set-Hostedcontentfilterrule permet</span><span class="sxs-lookup"><span data-stu-id="c8411-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
