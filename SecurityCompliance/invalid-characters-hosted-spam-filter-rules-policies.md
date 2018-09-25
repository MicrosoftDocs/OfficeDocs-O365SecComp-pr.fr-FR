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
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et la stratégie de filtrage de courrier indésirable 

Auparavant, les administrateurs Office 365 installé et configuré les règles de filtrage du courrier indésirable et de la stratégie de filtrage du courrier indésirable à l’aide du centre d’administration Exchange (EAC). Maintenant, vous utilisez la sécurité &amp; centre de conformité pour gérer la votre configuration de blocage du courrier indésirable. Les caractères suivants ont été pris en charge dans le CAE, mais ne sont pas pris en charge pour une utilisation dans la sécurité &amp; centre de conformité.  

**Caractères non valides :**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Si vos règles de filtrage du courrier indésirable ou votre stratégie de filtrage du courrier indésirable contient l’un des caractères non valides, vous pouvez rencontrer un ou plusieurs de ces problèmes :
- Vous ne puissiez pas à trouver les règles de stratégie de sécurité &amp; centre de conformité.
- Vous pouvez recevoir des erreurs lorsque vous essayez d’obtenir les règles de stratégie à l’aide de Windows PowerShell.
- Vous pouvez trouver que les paramètres de stratégie ne pas exécuter ou exécutent comme prévu.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Supprimer les caractères non valides de la stratégie de filtrage du courrier indésirable et les règles

Une fois que vous avez identifié les stratégies et les règles qui contiennent des caractères non valides, vous pouvez modifier les noms à l’aide des applets de commande Windows PowerShell. 

1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Pour modifier le nom de la stratégie de filtrage du courrier indésirable, exécutez l’applet de commande Set-HostedContentFilterPolicy comme suit :
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Pour modifier le nom d’une règle de filtrage du courrier indésirable, exécutez l’applet de commande Set-HostedContentFilterRule comme suit :
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Pour plus d’informations

[Gestion de la sécurité des menaces &amp; centre de conformité](threat-management.md)
  
[Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[Set-HostedContentFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
