---
title: Évitez les caractères non valides dans vos règles de filtrage du courrier indésirable et de la stratégie de filtrage du courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Fournit une aide pour les administrateurs qui ont des caractères non valides dans leur configuration anti-spam et rencontrez des problèmes lors de la tentative d’utilisation de la sécurité &amp; centre de conformité.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018733"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="5e4a2-103">Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et la stratégie de filtrage de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="5e4a2-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="5e4a2-p101">Auparavant, les administrateurs Office 365 installé et configuré les règles de filtrage du courrier indésirable et de la stratégie de filtrage du courrier indésirable à l’aide du centre d’administration Exchange (EAC). Maintenant, vous utilisez la sécurité &amp; centre de conformité pour gérer la votre configuration de blocage du courrier indésirable. Les caractères suivants ont été pris en charge dans le CAE, mais ne sont pas pris en charge pour une utilisation dans la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="5e4a2-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="5e4a2-107">**Caractères non valides :**</span><span class="sxs-lookup"><span data-stu-id="5e4a2-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="5e4a2-108">Si vos règles de filtrage du courrier indésirable ou votre stratégie de filtrage du courrier indésirable contient l’un des caractères non valides, vous pouvez rencontrer un ou plusieurs de ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="5e4a2-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="5e4a2-109">Vous ne puissiez pas à trouver les règles de stratégie de sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="5e4a2-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="5e4a2-110">Vous pouvez recevoir des erreurs lorsque vous essayez d’obtenir les règles de stratégie à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5e4a2-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="5e4a2-111">Vous pouvez trouver que les paramètres de stratégie ne pas exécuter ou exécutent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="5e4a2-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="5e4a2-112">Supprimer les caractères non valides de la stratégie de filtrage du courrier indésirable et les règles</span><span class="sxs-lookup"><span data-stu-id="5e4a2-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="5e4a2-113">Une fois que vous avez identifié les stratégies et les règles qui contiennent des caractères non valides, vous pouvez modifier les noms à l’aide des applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5e4a2-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="5e4a2-114">[Se connecter à Exchange Online à l’aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5e4a2-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="5e4a2-115">Pour modifier le nom de la stratégie de filtrage du courrier indésirable, exécutez l’applet de commande Set-HostedContentFilterPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="5e4a2-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="5e4a2-116">Pour modifier le nom d’une règle de filtrage du courrier indésirable, exécutez l’applet de commande Set-HostedContentFilterRule comme suit :</span><span class="sxs-lookup"><span data-stu-id="5e4a2-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="5e4a2-117">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5e4a2-117">For more information</span></span>

[<span data-ttu-id="5e4a2-118">Gestion de la sécurité des menaces &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="5e4a2-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="5e4a2-119">Set-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="5e4a2-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="5e4a2-120">Set-HostedContentFilterRule</span><span class="sxs-lookup"><span data-stu-id="5e4a2-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
