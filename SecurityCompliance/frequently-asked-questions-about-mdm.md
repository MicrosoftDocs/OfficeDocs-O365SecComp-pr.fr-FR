---
title: Forum aux questions sur la gestion des périphériques mobiles pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 3871f99c-c9db-4a23-86f9-902c1b02f58d
description: Cet article contient des questions fréquemment posées sur Mobile Device Management (MDM) pour Office 365, une fonctionnalité qui permet de gérer et sécuriser les périphériques mobiles dans Office 365.
ms.openlocfilehash: 6c4a5b3603d392b3d83769cd0f17450ce70565be
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272269"
---
# <a name="frequently-asked-questions-about-mobile-device-management-for-office-365"></a>Forum aux questions sur la gestion des périphériques mobiles pour Office 365

Cet article contient des questions fréquemment posées sur Mobile Device Management (MDM) pour Office 365, une fonctionnalité qui permet de gérer et sécuriser les périphériques mobiles dans Office 365.
  
## <a name="faqs"></a>FAQ

- [Comment puis-je obtenir Mobile Device Manager pour Office 365 ? Il n’apparaît pas dans le centre d’administration Office 365](#how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center)
    
- [Comment puis-je commencer avec la gestion des périphériques dans Mobile Device Manager](#how-can-i-get-started-with-device-management-in-mdm)
    
- [J’essaie de configurer Mobile Device Manager, mais elle semble bloquée. L’intégrité du Service Office 365 a été indiquant « mise en service » pendant un certain temps. Que puis-je faire ?](#im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do)
    
- [Que puis-je faire en cas d’échec de l’inscription de l’appareil ?](#what-can-i-do-if-device-enrollment-fails)
    
- [Quelle est la différence entre Intune et Mobile Device Manager pour Office 365 ?](#whats-the-difference-between-intune-and-mdm-for-office-365)
    
- [Comment les stratégies fonctionnent pour Mobile Device Manager ? Comment configurer les ? Désactiver les ?](#how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them)
    
- [Puis-je basculer de la gestion des appareils Exchange ActiveSync pour Mobile Device Manager pour Office 365 ?](#can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365)
    
- [Configurer Mobile Device Manager mais je souhaite maintenant pour le supprimer. Quelles sont les étapes ?](#i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps)
    
- [Toujours besoin d’aide](#still-need-help)
    
## <a name="how-can-i-get-mdm-for-office-365-i-dont-see-it-in-the-office-365-admin-center"></a>Comment puis-je obtenir Mobile Device Manager pour Office 365 ? Il n’apparaît pas dans le centre d’administration Office 365

Nous avons terminé le déploiement de cette fonctionnalité pour les clients Office 365. Recherchez l’onglet **Gestion des périphériques** dans le [Atteindre la Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Si vous ne voyez pas, n’hésitez pas. Voir [toujours besoin d’aide ?](#still-need-help), et nous allons vous aider à démarrer. 
  
## <a name="how-can-i-get-started-with-device-management-in-mdm"></a>Comment puis-je commencer avec la gestion des périphériques dans Mobile Device Manager

Il existe quatre étapes de mise en route avec Mobile Device Manager pour Office 365 (en savoir plus d’informations dans [Set up Mobile Device Management (MDM) dans Office 365](set-up-mobile-device-management.md)) :
  
1. **Activer MDM.** Accédez à la [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) et sélectionnez **Gestion des périphériques**. Cliquez sur **quelques** pour lancer le processus d’activation. 
    
2. **Terminer la configuration de Mobile Device Manager**. Cela peut nécessiter la configuration de certificats APNs et mises à jour pour les enregistrements DNS pour votre domaine. 
    
3. **Stratégies de créer**. Créer des stratégies de gestion des périphériques et les appliquer à des groupes d’utilisateurs qui sont [configurés dans les groupes de sécurité](create-device-security-policies.md). Nous vous recommandons de commencer par le déploiement des stratégies pour un petit groupe de test. Dans la sécurité &amp; centre de conformité, sélectionnez **les stratégies de sécurité de périphérique**.
    
4. **Utilisateurs inscrire des périphériques.** Les utilisateurs ayant une stratégie qui leur sont appliquée sont invités à [inscrire leurs périphériques](enroll-your-mobile-device.md) lorsqu’ils essaient d’accéder aux données d’Office 365 (en utilisant leur client de messagerie, par exemple). 
    
## <a name="im-trying-to-set-up-mdm-but-it-seems-stuck-the-office-365-service-health-has-been-showing-provisioning-for-a-while-what-can-i-do"></a>J’essaie de configurer Mobile Device Manager, mais elle semble bloquée. L’intégrité du Service Office 365 a été indiquant « mise en service » pendant un certain temps. Que puis-je faire ?

Elle peut prendre un certain temps pour préparer le service à vous. Lors de la mise en service est terminée, vous verrez la gestion des périphériques mobiles pour Office 365 page. Si vous avez attendu 24 heures et l’état est toujours **mise en service**, consultez [toujours besoin d’aide ?](#still-need-help) et nous allons vous aider à l’origine du problème. 
  
## <a name="what-can-i-do-if-device-enrollment-fails"></a>Que puis-je faire en cas d’échec de l’inscription de l’appareil ?

Si vous rencontrez des difficultés pour un appareil inscrit, commencez par vérifier les éléments suivants :
  
- Assurez-vous que le périphérique n’est pas déjà inscrit avec un autre fournisseur de gestion des appareils mobiles, tels que Intune.
    
- Assurez-vous que le périphérique est défini sur la date et l’heure.
    
- Basculer vers un autre Wi-Fi ou le réseau cellulaire sur l’appareil.
    
- Pour les appareils Android ou iOS, désinstallez et réinstallez l’application de portail d’entreprise Intune sur l’appareil.
    
Si l’inscription toujours ne fonctionne pas, [essayez les étapes de dépannage supplémentaires](troubleshoot-mdm.md).
  
## <a name="whats-the-difference-between-intune-and-mdm-for-office-365"></a>Quelle est la différence entre Intune et Mobile Device Manager pour Office 365 ?

Les deux Mobile Device Manager pour Office 365 et Intune fournissent des solutions basées sur le nuage pour la gestion des périphériques de votre organisation. Utilisez cette [comparaison côte à côte](choose-between-mdm-and-intune.md) des deux services pour vous aider à décider si l’utilisation de Intune ou Mobile Device Manager pour Office 365 est le meilleur ajustement pour vous. 
  
## <a name="how-do-policies-work-for-mdm-how-do-i-set-them-up-disable-them"></a>Comment les stratégies fonctionnent pour Mobile Device Manager ? Comment configurer les ? Désactiver les ?

Après avoir terminé l’installation initiale pour Mobile Device Manager pour Office 365, vous [créez des stratégies et les appliquer à des groupes d’utilisateurs](create-device-security-policies.md) dans [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8). Pour les utilisateurs qui concernent les stratégies, les stratégies d’obliger les utilisateurs à inscrire leurs périphériques dans Mobile Device Manager pour Office 365 avant de l’appareil peut servir à accéder aux données d’Office 365. Les stratégies que vous définissez déterminent les paramètres pour les appareils mobiles, par exemple, la fréquence à laquelle les mots de passe doivent être réinitialisés ou de si le chiffrement des données est nécessaire. 
  
Nous fournissent des instructions étape par étape pour [créer et déployer des stratégies de sécurité des périphériques](create-device-security-policies.md). Vous créez les stratégies de sécurité &amp; centre de conformité et vous pouvez désactiver une ou plusieurs stratégies en revenant à la sécurité &amp; centre de conformité et de modification de la stratégie pour supprimer le groupe appliqué. Ou vous pouvez choisir ne pas à supprimer complètement de la stratégie.
  
Si vous souhaitez exclure un groupe d’utilisateurs spécifique ne soient pas affectés par les stratégies, vous pouvez ajouter un groupe au groupe d’exclusion. Dans la sécurité &amp; centre de conformité, sous l’onglet **périphériques** , sélectionnez **Gérer les paramètres d’accès au périphérique**, puis ajoutez le groupe à le **existe-t-il un groupe de sécurité que vous souhaitez exclure de contrôle d’accès ?** section. 
  
## <a name="can-i-switch-from-exchange-activesync-device-management-to-mdm-for-office-365"></a>Puis-je basculer de la gestion des appareils Exchange ActiveSync pour Mobile Device Manager pour Office 365 ?

Si vous utilisez déjà des [stratégies Exchange ActiveSync](https://go.microsoft.com/fwlink/?LinkId=615145) pour gérer les appareils mobiles, vous pouvez démarrer à l’aide de Mobile Device Manager pour Office 365 en suivant les étapes pour [définir des Mobile Device Management (MDM) dans Office 365](set-up-mobile-device-management.md).
  
Lorsque vous appliquez les stratégies que vous créez dans Mobile Device Manager pour Office 365 pour les groupes d’utilisateurs, ces politiques remplacent les stratégies de boîte aux lettres d’appareil mobile Exchange ActiveSync et les règles d’accès aux périphériques que vous avez précédemment créé dans le centre d’administration Exchange pour les utilisateurs. 
  
Une fois un périphérique Mobile Device Manager est inscrit pour Office 365, toute stratégie de boîte aux lettres d’appareil mobile Exchange ActiveSync ou la règle d’accès aux périphériques appliquée au périphérique sera ignoré.
  
## <a name="i-set-up-mdm-but-now-i-want-to-remove-it-what-are-the-steps"></a>Configurer Mobile Device Manager mais je souhaite maintenant pour le supprimer. Quelles sont les étapes ?

Malheureusement, vous ne pouvez pas simplement « mise hors service « Mobile Device Manager pour Office 365 après que vous l’avez configuré. Mais vous pouvez le supprimer des groupes d’utilisateurs en supprimant les groupes de sécurité utilisateur à partir des stratégies d’appareil que vous avez créé. Ou bien, désactiver pour tout le monde en supprimant les stratégies d’appareil afin qu’ils ne sont pas en place et ne sont pas appliquées. Découvrez [comment désactiver la gestion des périphériques mobiles dans Office 365](turn-off-mdm.md).
  
## <a name="still-need-help"></a>Besoin d’aide ?

[![Obtenir de l’aide dans les forums de la communauté Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administrateurs : Se connecter et créer une demande de service](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administrateurs : Appelez le support technique](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

  

