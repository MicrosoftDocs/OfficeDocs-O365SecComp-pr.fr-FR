---
title: Gérer les périphériques inscrits dans la gestion des périphériques mobiles dans Office 365
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
- MBS150
- MET150
ms.assetid: 28dd276b-beeb-4c5b-8b22-7551186127fe
description: Suivez ces étapes pour définir des Mobile Device Management (MDM) dans Office 365.
ms.openlocfilehash: 3a84b6904b866e07eb4efabe0f39041b282d0ba9
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272309"
---
# <a name="manage-devices-enrolled-in-mobile-device-management-in-office-365"></a>Gérer les périphériques inscrits dans la gestion des périphériques mobiles dans Office 365

La gestion des périphériques mobiles intégrées à Office 365 vous aident à sécuriser et gérer des appareils mobiles de vos utilisateurs comme iPhone, des tablettes, Androïd, et les téléphones Windows. La première étape consiste à se connecter à Office 365 et [configurer Mobile Device Manager pour Office 365](set-up-mobile-device-management.md). 
  
Une fois que vous avez configuré, les personnes dans votre organisation doit [s’inscrire leurs périphériques](enroll-your-mobile-device.md) dans le service. Ensuite, vous pouvez utiliser Mobile Device Manager pour Office 365 pour gérer les périphériques de votre organisation. Par exemple, vous pouvez utiliser les stratégies de sécurité de périphérique pour aider à limiter l’accès à la messagerie ou autres services, afficher les rapports de périphériques et réinitialiser un appareil à distance. Vous accédez généralement à le [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) pour effectuer ces tâches. 
  
## <a name="device-management-tasks"></a>Tâches de gestion des périphériques

Pour obtenir le panneau de gestion de périphériques, procédez comme suit. 
  
1. Accédez au Centre d’administration Office 365.
    
2. Tapez gestion des périphériques mobiles dans le champ de recherche et sélectionnez **Gestion des périphériques mobiles** dans la liste des résultats. 
    
    ![Type de gestionnaire de périphériques mobiles dans le champ de recherche O365](media/e2e2f1c0-e543-431a-959b-e26c2ba328a7.png)
  
Une fois que vous avez Mobile Device Manager pour Office 365, configurer, voici comment vous pouvez gérer les appareils mobiles dans votre organisation. 
  
|**Pour ce faire...**|**Procédez comme suit**|
|:-----|:-----|
|Réinitialiser un appareil  <br/> |Dans le panneau de gestion des périphériques, sélectionnez le *nom du périphérique* , puis **réinitialisation complète à** pour supprimer toutes les informations ou **sélective balayage** pour supprimer uniquement les informations d’organisation sur l’appareil.  <br/> Consultez la rubrique [Réinitialiser un appareil dans Office 365](wipe-a-mobile-device.md).  <br/> |
|Bloquer l'accès des appareils non pris en charge à la messagerie Exchange à l'aide d'Exchange ActiveSync  <br/> |Dans le panneau de gestion des périphériques, sélectionnez **Bloquer**.  <br/> |
|Définir des stratégies de périphérique, telles que les exigences de mot de passe et les paramètres de sécurité  <br/> |Dans le panneau de gestion des périphériques, cliquez sur \> **stratégies de sécurité des périphériques** \> **Ajouter +**.  <br/> Voir [créer et déployer des stratégies de sécurité des périphériques](create-device-security-policies.md).  <br/> |
|Afficher la liste des appareils bloqués  <br/> |Dans le panneau de gestion des périphériques, sous **Sélectionnez un affichage** sur **bloqué**.  <br/> ||
|Débloquer un appareil non pris en charge ou non conforme pour un utilisateur ou un groupe d'utilisateurs  <br/> | Vous pouvez débloquer les périphériques non conformes différemment en fonction de votre situation. Choisissez une des options suivantes :<br/>  Supprimer les utilisateurs du groupe de sécurité, que la stratégie a été appliquée au. Accédez au **Centre d’administration Office 365** \> **groupes**, puis sélectionnez * nom du groupe *. Cliquez sur **Modifier les administrateurs et les membres**.<br/>  Supprimer le groupe de sécurité que les utilisateurs sont un membre à partir de la stratégie de périphérique. Accédez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **stratégies de sécurité des périphériques**. Sélectionnez * nom de la stratégie périphérique *, puis cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **déploiement**.<br/>  Débloquer tous les périphériques non conformes pour une stratégie de périphérique. Accédez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **stratégies de sécurité des périphériques**. Sélectionnez le *nom de stratégie de périphérique* , puis cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif) \> **conditions d’accès**. Sélectionnez **Autoriser violation d’accès et de rapport**.<br/>  Pour débloquer un périphérique non conforme ou non pris en charge pour un utilisateur ou un groupe d’utilisateurs, accédez à atteindre **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **Device management** \> **accès aux appareils de gérer les paramètres **. Ajouter un groupe de sécurité avec les membres que vous souhaitez exclure de l’interdit l’accès à Office 365. Voir [créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration d’Office 365](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> |
|Obtenir plus d’informations sur les périphériques de votre organisation  <br/> |Pour obtenir plus d’informations telles que les périphériques sont inscrits et compatibles avec les stratégies de sécurité de périphérique, suivez les étapes décrites dans [obtenir plus d’informations sur les périphériques gérés par Mobile Device Manager](get-details-about-mdm-managed-devices.md).  <br/> |
|Supprimer des utilisateurs afin de leurs périphériques ne sont plus gérés par Mobile Device Manager  <br/> |Modifier le groupe de sécurité qui a des stratégies de gestion des périphériques pour Mobile Device Manager supprimer l’utilisateur. Voir [créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration d’Office 365](https://support.office.com/article/55c96b32-e086-4c9e-948b-a018b44510cb).<br/> Pour supprimer Mobile Device Manager de tous vos utilisateurs Office 365, voir [désactiver la gestion des périphériques mobiles dans Office 365](turn-off-mdm.md).  <br/> |
   

