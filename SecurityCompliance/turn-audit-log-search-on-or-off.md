---
title: Activer ou désactiver la recherche dans un journal d’audit Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Vous pouvez activer la fonctionnalité de recherche du journal d’Audit de sécurité Office 365 &amp; centre de conformité. Si vous changez d’avis, vous pouvez activer if désactiver à tout moment. Lors de la recherche du journal d’Audit est désactivé, administrateurs ne peuvent pas rechercher le journal d’audit de Office 365 pour l’activité utilisateur et d’administration dans votre organisation.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528117"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Activer ou désactiver la recherche dans un journal d’audit Office 365

Vous (ou un autre administrateur) devez activer l’enregistrement d’audit avant de commencer la recherche dans le journal d’audit de Office 365. Lorsque d’audit de recherche de journal de sécurité Office 365 &amp; centre de conformité est activée, les activités d’utilisateur et d’administration à partir de votre organisation sont enregistrée dans le journal d’audit et conservées pendant 90 jours. Toutefois, votre organisation ne peut pas souhaite enregistrer et conserver les données du journal d’audit. Ou vous pouvez utiliser une application de gestion (SIEM) des informations et des événements de sécurité tiers à accéder à vos données d’audit. Dans ce cas, un administrateur global peut désactiver la recherche de journal d’audit dans Office 365.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être affecté le rôle journaux d’Audit dans Exchange Online à activer ou désactiver la recherche des journaux d’audit dans votre organisation Office 365. Par défaut, ce rôle est attribué aux groupes de rôle de gestion de la conformité et de gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Les administrateurs globaux dans Office 365 sont membres du groupe de rôles de gestion de l’organisation dans Exchange Online. 
    
    > [!IMPORTANT]
    > Les utilisateurs doivent être affectées des autorisations dans Exchange Online pour activer ou désactiver la recherche des journaux d’audit. Si vous affectez le rôle journaux d’Audit dans la page **autorisations** de sécurité des utilisateurs &amp; centre de conformité, ils ne pourront activer ou désactiver la recherche des journaux d’audit. Il s’agit de l’applet de commande sous-jacente étant une applet de commande Exchange Online. 
  
- Si vous désactivez la recherche des journaux d’audit dans Office 365, vous pouvez toujours utiliser l’API d’activité de gestion Office 365 pour accéder aux données d’audit pour votre organisation. Désactivation de la recherche des journaux d’audit en suivant les étapes décrites dans cet article signifie qu’aucun résultat n’est renvoyés lorsque vous recherchez dans le journal d’audit à l’aide de la sécurité &amp; centre de conformité ou lorsque vous exécutez l’applet de commande **Search-UnifiedAuditLog** dans Exchange Online PowerShell. Toutefois, si vous avez autorisé n’importe quelle application pour accéder aux données d’audit de votre organisation par le biais de l’API d’activité de gestion Office 365, ces applications continueront de fonctionner. 
    
- Pour le journal d’audit dans des instructions détaillées sur la recherche Office 365, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).
    
## <a name="turn-on-audit-log-search"></a>Activer la recherche des journaux d’audit

Vous pouvez utiliser la sécurité &amp; centre de conformité ou PowerShell pour activer la recherche des journaux d’audit dans Office 365. Cela peut prendre plusieurs heures après l’activation de la recherche du journal d’audit avant de résultats lorsque vous recherchez le journal d’audit. Vous devez être affecté le rôle journaux d’Audit dans Exchange Online pour activer la recherche des journaux d’audit.
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a>Utilisez la sécurité &amp; centre de conformité pour activer la recherche des journaux d’audit

1. Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche des journaux d’Audit**.
    
2. Cliquez sur **Démarrer l’enregistrement d’utilisateur et des activités d’administration**.
    
    ![Cliquez sur Démarrer l’enregistrement d’utilisateur et des activités d’administration pour activer l’audit](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    Une boîte de dialogue s’affiche indiquant qu’utilisateur et l’activité d’administration dans votre organisation seront enregistrés dans le journal d’audit d’Office 365 et disponible pour l’affichage dans un rapport. 
    
3. Cliquez sur **Activer**.
    
    Un message s’affiche indiquant que le journal d’audit est préparé et que vous pouvez exécuter une recherche en quelques heures après que la préparation est terminée.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>Utilisation de PowerShell pour activer la recherche des journaux d’audit

1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Exécutez la commande PowerShell suivante pour activer la recherche des journaux d’audit dans Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    Un message s’affiche indiquant qu’il peut prendre jusqu'à 60 minutes pour que les modifications prennent effet.
  
## <a name="turn-off-audit-log-search"></a>Désactiver la recherche du journal d’audit

Vous devez utiliser PowerShell distant connecté à votre organisation Exchange Online pour désactiver la recherche des journaux d’audit. Similaire à l’activation de la recherche des journaux d’audit, vous devez être affecté le rôle journaux d’Audit dans Exchange Online pour désactiver la recherche des journaux d’audit.
  
1. [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. Exécutez la commande PowerShell suivante pour désactiver la recherche des journaux d’audit dans Office 365.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. Après un certain temps, vérifiez que recherche des journaux d’audit est activée (désactivé). Il existe deux façons de procéder :
    
    - Dans PowerShell, exécutez la commande suivante :

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        La valeur de `False` pour _UnifiedAuditLogIngestionEnabled_ propriété indique que recherche des journaux d’audit est désactivée. 
    
    - Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche des journaux d’Audit**, puis cliquez sur **Rechercher**.
    
      Un message s’affiche indiquant que recherche des journaux d’audit n’est pas activée. 
    
      ![Un message est dispayed si l’audit est désactivé](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
