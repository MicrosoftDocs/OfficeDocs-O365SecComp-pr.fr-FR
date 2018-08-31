---
title: Vue d’ensemble de la gestion des appareils mobiles (Mobile Device Manager) pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: Vous pouvez gérer et sécuriser les périphériques mobiles s’ils étaient connectés à votre organisation Office 365 à l’aide de la gestion des périphériques mobiles pour Office 365. Les appareils mobiles tels que les smartphones et tablettes qui servent à accéder aux travail courrier, calendrier, contacts et documents lire une grande partie de s’assurer que les employés effectuer leur travail et à tout moment, depuis n’importe où. Il est donc essentiel que vous aider à protéger les informations de votre organisation lorsque des personnes utilisent des périphériques. Vous pouvez utiliser Mobile Device Manager pour Office 365 pour définir des règles d’accès et les stratégies de sécurité des appareils et pour réinitialiser les appareils mobiles s’ils sont perdus ou volés.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272489"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a>Vue d’ensemble de la gestion des appareils mobiles (Mobile Device Manager) pour Office 365

Vous pouvez gérer et sécuriser les périphériques mobiles s’ils étaient connectés à votre organisation Office 365 à l’aide de la gestion des périphériques mobiles pour Office 365. Les appareils mobiles tels que les smartphones et tablettes qui servent à accéder aux travail courrier, calendrier, contacts et documents lire une grande partie de s’assurer que les employés effectuer leur travail et à tout moment, depuis n’importe où. Il est donc essentiel que vous aider à protéger les informations de votre organisation lorsque des personnes utilisent des périphériques. Vous pouvez utiliser Mobile Device Manager pour Office 365 pour définir des règles d’accès et les stratégies de sécurité des appareils et pour réinitialiser les appareils mobiles s’ils sont perdus ou volés.
  
![Mobile Device Manager sur le téléphone Android](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a>Quels types d’appareils pouvez-vous gérer ?

Vous pouvez utiliser Mobile Device Manager pour Office 365 pour gérer plusieurs types d’appareils mobiles tels que Windows Phone, Android, iPhone et iPad. Pour gérer les appareils mobiles utilisés par des personnes dans votre organisation, chaque personne doit avoir une licence Office 365 applicable et leur appareil doit être inscrit dans Mobile Device Manager pour Office 365. 
  
Pour voir quel Mobile Device Manager pour Office 365 prend en charge pour chaque type de périphérique, voir [Fonctionnalités de gestion des périphériques mobiles pour Office 365](capabilities-of-mobile-device-management.md).
  
## <a name="setup-steps-for-mdm"></a>Étapes de configuration pour Mobile Device Manager

Un administrateur global d’Office 365 doit effectuer les étapes suivantes pour activer et configurer Mobile Device Manager pour Office 365. Suivez les instructions de la rubrique sur [la configuration de Mobile Device Manager pour Office 365](set-up-mobile-device-management.md) pour voir la procédure détaillée. Voici un résumé rapide : 
  
> Étape 1 : Activer Mobile Device Manager pour Office 365 en suivant les étapes de la [valeur up Mobile Device Management (MDM) dans Office 365](set-up-mobile-device-management.md).
    
> Étape 2 : Configurer Mobile Device Manager pour Office 365, par exemple, création d’un certificat APNs pour gérer les appareils iOS et ajout d’un enregistrement de nom de domaine DNS (Domain Name System) pour votre domaine prendre en charge Windows Phone.
    
> Étape 3 : Créer des stratégies d’appareil et les appliquer à des groupes d’utilisateurs. Lorsque vous effectuez cette opération, vos utilisateurs obtiendrez un [message d’inscription sur leur appareil](enroll-your-mobile-device.md). Et lorsqu’ils réalisé l’inscription, leurs appareils seront limitées par les stratégies que vous avez configuré les.
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a>Tâches de gestion des périphériques

Une fois que vous avez Mobile Device Manager pour Office 365, configurer et vos utilisateurs ont inscrit leurs périphériques, vous pouvez gérer les périphériques, bloquez l’accès ou réinitialiser un appareil, si nécessaire. Pour plus d’informations sur [certaines tâches courantes de gestion des périphériques](manage-devices-in-mdm.md), y compris where effectuer les tâches.
  
## <a name="other-ways-to-manage-devices-and-apps"></a>Autres méthodes de gestion des applications et des périphériques

Si vous avez besoin de plus de fonctionnalités Mobile Device Manager pour Office 365 inclut, extraire cette [comparaison des fonctionnalités de Mobile Device Manager et Microsoft Intune](choose-between-mdm-and-intune.md) pour voir si un abonnement Intune doit répondre aux besoins de votre organisation. 
  
Si vous devez simplement la gestion des applications mobiles (MAM), par exemple des personnes de mise à jour des projets de travail sur leurs appareils, Intune fournit une autre option outre l’inscription et la gestion des périphériques. Un abonnement Intune vous permet de configurer les stratégies MAM à l’aide du portail Azure, même si les périphériques de personnes ne sont pas inscrits dans Intune. Voir [protéger les données d’application à l’aide de stratégies MAM](https://go.microsoft.com/fwlink/?LinkId=825439). 
  
## <a name="see-also"></a>Voir aussi

[Obtenir plus d’informations sur les périphériques gérés par Mobile Device Manager](get-details-about-mdm-managed-devices.md)

[Configurer Mobile Device Manager pour Office 365](set-up-mobile-device-management.md)
  
[Inscrire les appareils mobiles dans Mobile Device Manager](enroll-your-mobile-device.md)
  
[Gérer les périphériques inscrits dans Mobile Device Manager](manage-devices-in-mdm.md)

