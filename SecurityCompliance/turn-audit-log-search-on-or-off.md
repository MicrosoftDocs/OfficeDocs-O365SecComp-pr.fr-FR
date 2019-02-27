---
title: Activer ou désactiver la recherche dans un journal d’audit Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Vous pouvez activer la fonctionnalité de recherche de journal d'audit dans le centre &amp; de sécurité conformité Office 365. Si vous changez d'avis, vous pouvez le désactiver à tout moment. Lorsque le paramètre de recherche du journal d'audit est désactivé, les administrateurs ne peuvent pas rechercher dans le journal d'audit Office 365 des activités de l'utilisateur et de l'administrateur dans votre organisation.
ms.openlocfilehash: 17b98cce26054d073006fa78c55fe418b5f327d8
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295457"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Activer ou désactiver la recherche dans un journal d’audit Office 365

Vous (ou un autre administrateur) devez activer la journalisation d'audit pour pouvoir commencer à rechercher dans le journal d'audit Office 365. Lorsque la recherche du journal d'audit dans le &amp; Centre de sécurité conformité Office 365 est activée, l'activité de l'utilisateur et de l'administrateur de votre organisation est enregistrée dans le journal d'audit et conservée pendant 90 jours. Toutefois, il se peut que votre organisation ne souhaite pas enregistrer et conserver les données du journal d'audit. Vous pouvez également utiliser une application de gestion des événements et des informations de sécurité tierces pour accéder à vos données d'audit. Dans ce cas, un administrateur global peut désactiver la recherche dans le journal d'audit dans Office 365.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez disposer du rôle journaux d'audit dans Exchange Online pour activer ou désactiver la recherche dans le journal d'audit dans votre organisation Office 365. Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité et gestion de l'organisation dans la page **autorisations** du centre d'administration Exchange. Les administrateurs globaux dans Office 365 sont membres du groupe de rôles gestion de l'organisation dans Exchange Online. 
    
    > [!IMPORTANT]
    > Les utilisateurs doivent disposer d'autorisations dans Exchange Online pour activer ou désactiver la recherche dans le journal d'audit. Si vous affectez des utilisateurs au rôle journaux d' **** audit sur la page autorisations &amp; dans le centre de sécurité conformité, ils ne pourront pas activer ou désactiver la recherche dans le journal d'audit. Cela est dû au fait que la cmdlet sous-jacente est une applet de commande Exchange Online. 
  
- Si vous désactivez la recherche dans le journal d'audit dans Office 365, vous pouvez toujours utiliser l'API activité de gestion d'Office 365 pour accéder aux données d'audit de votre organisation. La désActivation de la recherche du journal d'audit en suivant les étapes décrites dans cet article signifie qu'aucun résultat n'est renvoyé lorsque vous effectuez &amp; une recherche dans le journal d'audit à l'aide du centre de sécurité et de l'applet de commande **Search-UnifiedAuditLog** dans Exchange Online. PowerShell. Toutefois, si vous avez autorisé une application à accéder aux données d'audit de votre organisation via l'API activité de gestion d'Office 365, ces applications continueront à fonctionner. 
    
- Pour obtenir des instructions pas à pas sur la recherche dans le journal d'audit Office 365, voir [Search the audit log dans le &amp; Centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).
    
## <a name="turn-on-audit-log-search"></a>Activer la recherche du journal d'audit

Vous pouvez utiliser le centre &amp; de sécurité conformité ou PowerShell pour activer la recherche dans le journal d'audit dans Office 365. L'activation de la recherche de journal d'audit peut prendre plusieurs heures avant de pouvoir renvoyer des résultats lors de la recherche dans le journal d'audit. Vous devez disposer du rôle journaux d'audit dans Exchange Online pour activer la recherche dans le journal d'audit.
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a>Utiliser le centre &amp; de sécurité conformité pour activer la recherche dans le journal d'audit

1. Dans le centre &amp; de sécurité conformité, accédez à recherche dans le \> **Journal d'audit**de la **recherche &amp; ** .
    
2. Cliquez sur **Démarrer l'enregistrement des activités de l'utilisateur et de l'administrateur**.
    
    ![Cliquez sur Démarrer l'enregistrement des activités de l'utilisateur et de l'administrateur pour activer l'audit.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    Une boîte de dialogue s'affiche, indiquant que l'activité de l'utilisateur et de l'administrateur dans votre organisation sera enregistrée dans le journal d'audit Office 365 et disponible pour être affichée dans un rapport. 
    
3. Cliquez sur **Activer**.
    
    Un message s'affiche indiquant que le journal d'audit est en cours de préparation et que vous pouvez exécuter une recherche dans quelques heures après la fin de la préparation.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>Utiliser PowerShell pour activer la recherche dans le journal d'audit

1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Exécutez la commande PowerShell suivante pour activer la recherche dans le journal d'audit dans Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    Un message s'affiche indiquant que la modification peut prendre jusqu'à 60 minutes.
  
## <a name="turn-off-audit-log-search"></a>Désactiver la recherche de journal d'audit

Vous devez utiliser PowerShell à distance connecté à votre organisation Exchange Online pour désactiver la recherche de journal d'audit. De la même manière que pour activer la recherche dans le journal d'audit, vous devez disposer du rôle journaux d'audit dans Exchange Online pour désactiver la recherche de journal d'audit.
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Exécutez la commande PowerShell suivante pour désactiver la recherche dans le journal d'audit dans Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. Après un certain temps, vérifiez que la recherche dans le journal d'audit est désactivée (désactivée). Deux méthodes s'offrent à vous:
    
    - Dans PowerShell, exécutez la commande suivante:

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        La valeur de `False` pour la propriété _UnifiedAuditLogIngestionEnabled_ indique que la recherche du journal d'audit est désactivée. 
    
    - Dans le centre &amp; de sécurité conformité, accédez à recherche dans le \> **Journal d'audit**de **recherche &amp; ** , puis cliquez sur **Rechercher**.
    
      Un message s'affiche indiquant que la recherche du journal d'audit n'est pas activée. 
    
      ![Un message est dispayed si l'audit est désactivé](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
