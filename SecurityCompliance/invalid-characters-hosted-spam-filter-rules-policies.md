---
title: Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et la stratégie de filtrage
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 9/24/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Fournit de l’aide aux administrateurs qui ont des caractères non valides dans leur configuration de blocage du courrier indésirable et &amp; génèrent des problèmes lors de la tentative d’utilisation du centre de sécurité conformité.
ms.openlocfilehash: 0e7dcb40d8e54045caa55083e2cbf0585a80869d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154159"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et votre stratégie de filtrage 

Auparavant, les administrateurs Office 365 configurent et configurent les règles de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable à l’aide du centre d’administration Exchange. À présent, vous utilisez le &amp; Centre de sécurité conformité pour gérer la configuration de blocage du courrier indésirable. Les caractères suivants étaient pris en charge dans le centre d’administration Exchange mais ne sont pas &amp; pris en charge dans le centre de sécurité conformité.  

**Caractères non valides:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Si vos règles de filtrage du courrier indésirable ou votre stratégie de filtrage du courrier indésirable contient l’un des caractères non valides, vous pouvez rencontrer un ou plusieurs des problèmes suivants:
- Il se peut que vous ne puissiez pas trouver la stratégie ou les &amp; règles dans le centre de sécurité conformité.
- Vous pouvez recevoir des erreurs lors de la tentative d’obtention des règles ou de la stratégie à l’aide de Windows PowerShell.
- Vous pouvez constater que la stratégie ou les paramètres ne s’exécutent pas comme prévu.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Supprimer les caractères non valides de la stratégie et des règles de filtrage du courrier indésirable

Une fois que vous avez identifié la stratégie et les règles qui contiennent des caractères non valides, vous pouvez modifier les noms à l’aide des applets de commande Windows PowerShell. 

1. [Connectez-vous à Exchange Online à l’aide de Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Pour modifier le nom de la stratégie de filtrage du courrier indésirable, exécutez la cmdlet Set-HostedContentFilterPolicy comme suit:
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Pour modifier le nom d’une règle de filtrage du courrier indésirable, exécutez la cmdlet Set-Hostedcontentfilterrule permet comme suit:
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Pour plus d’informations

[Gestion des menaces dans le &amp; Centre de sécurité conformité](threat-management.md)
  
[Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Set-Hostedcontentfilterrule permet](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
