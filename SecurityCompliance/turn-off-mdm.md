---
title: Comment faire pour désactiver la gestion des périphériques mobiles dans Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Suivez ces étapes pour arrêter les stratégies de Mobile Device Manager à partir de la mise en œuvre pour les appareils mobiles dans votre organisation Office 365.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272219"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a>Comment faire pour désactiver la gestion des périphériques mobiles dans Office 365

Pour désactiver efficacement Mobile Device Manager pour Office 365, vous supprimez des groupes de personnes (défini par les groupes de sécurité) les stratégies de gestion de périphériques, ou supprimez les stratégies eux-mêmes. 
  
- Supprimer des groupes d’utilisateurs en supprimant les groupes de sécurité utilisateur à partir des stratégies d’appareil que vous avez créé. 
    
- Désactiver Mobile Device Manager pour tout le monde en supprimant toutes les stratégies d’appareil mobile Device Manager. 
    
Ces options supprimera l’application Mobile Device Manager pour les périphériques de votre organisation. Malheureusement, vous ne pouvez pas simplement « mise hors service « Mobile Device Manager pour Office 365 après que vous l’avez configuré.
  
> [!IMPORTANT]
> N’oubliez pas de l’impact sur les périphériques des utilisateurs lorsque vous supprimez des groupes de sécurité utilisateur de stratégies ou supprimez les stratégies eux-mêmes. Par exemple, les profils de messagerie et les messages électroniques mis en cache peuvent être supprimés, en fonction de l’appareil. Voir : [Quel est l’impact des stratégies de sécurité sur les différents types d’appareils ?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a>Supprimer des groupes de sécurité utilisateur de stratégies d’appareil mobile Device Manager

1. Accédez à **sécurité &amp; centre de conformité** \> **prévention des pertes de données** \> **stratégies de sécurité de l’appareil**.
    
2. Sélectionnez une stratégie de périphérique, puis cliquez sur ![icône Modifier](media/O365-MDM-CreatePolicy-EditIcon.gif) **Modifier la stratégie**.
    
3. Sous **déploiement**, cliquez sur **: supprimer**.
    
    Sous **groupes**, sélectionnez un groupe de sécurité.
    
4.  Cliquez sur **Supprimer**.
    
5. Cliquez sur **Enregistrer**.
    
## <a name="remove-mdm-device-policies"></a>Supprimer des stratégies d’appareil mobile Device Manager

1. Accédez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **stratégies de sécurité des périphériques**.
    
2. Sélectionnez une stratégie de périphérique, puis cliquez sur ![Image de la Corbeille peut icône. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Supprimer la stratégie**.
    
3. Dans la boîte de dialogue **Avertissement** , cliquez sur **Oui**. 
    

