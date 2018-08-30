---
title: Créer et déployer des stratégies de sécurité des appareils
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/9/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewDevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: d310f556-8bfb-497b-9bd7-fe3c36ea2fd6
description: 'Étapes pour créer et déployer des stratégies de sécurité pour la gestion des périphériques mobiles dans Office 365 qui peuvent aider à protéger les informations de votre organisation sur Office 365 contre les accès. '
ms.openlocfilehash: ab1fc1960a3e55eb3080dde7df0ec742c58b2cc7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272069"
---
# <a name="create-and-deploy-device-security-policies"></a>Créer et déployer des stratégies de sécurité des appareils

Vous pouvez utiliser la gestion des périphériques mobiles pour Office 365 pour créer des stratégies de sécurité qui aident à protéger les informations de votre organisation sur Office 365 contre les accès. Vous pouvez appliquer des stratégies à n’importe quel appareil mobile dans votre organisation où l’utilisateur de l’appareil possède une licence Office 365 applicable et a inscrit le périphérique Mobile Device Manager pour Office 365.
  
## <a name="before-you-begin"></a>Avant de commencer

- Découvrez les périphériques, les applications de périphérique mobile et les paramètres de sécurité Mobile Device Manager pour Office 365 prend en charge. Voir les [fonctionnalités de gestion des appareils mobiles pour Office 365](capabilities-of-mobile-device-management.md).
    
- Créer des groupes de sécurité qui incluent des utilisateurs Office 365 que vous souhaitez déployer des stratégies et pour les utilisateurs que vous souhaitez exclure de l’interdit l’accès à Office 365. Il est recommandé qu’avant de déployer une nouvelle stratégie pour votre organisation, vous testez la stratégie à déployer sur un petit nombre d’utilisateurs. Vous pouvez créer et utiliser un groupe de sécurité qui inclut uniquement par vous-même ou un petit nombre Office 365 d’utilisateurs que vous pouvant tester la stratégie. Pour plus d’informations sur les groupes de sécurité, voir [créer, modifier ou supprimer un groupe de sécurité](https://go.microsoft.com/fwlink/p/?LinkId=518555).
    
- **Important :** Avant de pouvoir créer une stratégie d’appareil mobile, vous devez activer et configurer Mobile Device Manager pour Office 365. Consultez la rubrique [vue d’ensemble de la gestion des appareils mobiles pour Office 365](overview-of-mdm.md).
    
- Pour créer et déployer des stratégies de gestion des appareils mobiles dans Office 365, vous devez être administrateur global Office 365. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](https://support.office.com/article/d10608af-7934-490a-818e-e68f17d0e9c1).
    
- Avant de déployer des stratégies, permettent à votre organisation de connaître l’impact potentiel d’inscrire un périphérique Mobile Device Manager pour Office 365. Selon la façon dont vous configurez les stratégies, les périphériques non conformes peuvent être bloquées d’accéder à Office 365 et données, y compris les applications installées, des photos et des informations personnelles sur un appareil inscrit, peuvent être supprimées.
    
> [!NOTE]
> Stratégies et règles d’accès créées dans Mobile Device Manager pour Office 365 remplacera les stratégies de boîte aux lettres d’appareil mobile Exchange ActiveSync et les règles d’accès aux périphériques créés dans le centre d’administration Exchange. Une fois un périphérique Mobile Device Manager est inscrit pour Office 365, toute stratégie de boîte aux lettres d’appareil mobile Exchange ActiveSync ou la règle d’accès aux périphériques appliquée au périphérique sera ignoré. Pour plus d’informations sur Exchange ActiveSync, consultez la rubrique [Exchange ActiveSync dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="step-1-create-a-security-policy-and-deploy-to-a-test-group"></a>Étape 1 : Créer une stratégie de sécurité et le déployer dans un groupe de test

Avant de commencer, assurez-vous que vous avez activé et configuré Mobile Device Manager pour Office 365. Pour plus d’informations, voir [Vue d’ensemble de gestion des périphériques mobiles pour Office 365](overview-of-mdm.md) . 
  
1. Dans Office 365, dans la sécurité &amp; centre de conformité, accédez à la **protection contre la perte de données** \> **stratégies de sécurité des périphériques**.
    
    > [!NOTE]
    > Les **stratégies de sécurité d’appareil** apparaîtra dans le menu uniquement une fois que vous avez activé la gestion des appareils mobiles. 
  
2. Choisissez **+ créer une stratégie**.
    
    ![Création d’une stratégie de périphérique MDN sous stratégies de sécurité des périphériques](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
3. Spécifiez un **nom** et une **Description** pour la nouvelle stratégie, puis cliquez sur **suivant**.
    
    ![Définition d’un nom pour la stratégie de sécurité du périphérique](media/d382e845-4a7f-4f72-8a09-813ea4cbd0c4.png)
  
4. Sur le **quelles conditions voulez-vous ont sur les appareils ?** page, spécifier la configuration requise à appliquer aux appareils mobiles dans votre organisation, puis cliquez sur **suivant**.
    
    ![La page Paramètres de la stratégie de sécurité des périphériques](media/186b3bd5-5e3d-4059-978f-94113111a8ca.png)
  
5. Sur le **que voulez-vous configurer ?** page, spécifiez les autres exigences à appliquer aux appareils mobiles dans votre organisation, puis cliquez sur **suivant**.
    
6. Sur le **vous souhaitez appliquer cette stratégie maintenant ?** page, sélectionnez **Oui**, puis **+ Ajouter**. 
    
    ![Ajouter la stratégie](media/89ab7cab-1b7a-4c78-9aa6-3db7d7667f8e.png)
  
7. Sélectionnez l’ou les groupes qui vous allez tester la stratégie avant de déployer dans votre organisation, puis cliquez sur **Ajouter**.
    
8. Choisissez **Suivant**.
    
9. Passez en revue et confirmer les détails de la nouvelle stratégie de périphérique, puis choisissez **créer cette stratégie**.
    
    ![Choisissez créer cette stratégie finsih création d’une stratégie de périphérique](media/e410bcf3-8a36-44ed-9fea-00e742db06fb.png)
  
10. Cliquez sur **Fermer**.
    
Chaque utilisateur la stratégie s’applique à aura la stratégie répercutée sur leur appareil la prochaine fois qu’ils se connectent à Office 365 à l’aide de leur appareil mobile. Si les utilisateurs n’ont pas eu une stratégie appliquée à leur appareil mobile, puis après le déploiement de la stratégie, qu’ils vous recevez une notification sur leur appareil qui comprend les [étapes nécessaires pour inscrire et activer Mobile Device Manager pour Office 365](https://go.microsoft.com/fwlink/?LinkId=615272). Jusqu'à ce qu’ils s’exécutent l’inscription, l’accès par courrier électronique, OneDrive et autres services sont limités. Lorsqu’ils ont terminé d’inscription à l’aide de l’application de portail d’entreprise Intune, ils pourront utiliser les services et la stratégie sera appliquée à leur appareil.
  
## <a name="step-2-verify-your-policy-works"></a>Étape 2 : Vérifier le fonctionnement d’une stratégie

Une fois que vous avez créé une stratégie de sécurité, vous devez vérifier que la stratégie fonctionne comme prévu avant de le déployer dans votre organisation.
  
1. Dans Office 365, accédez à **sécurité &amp; centre de conformité** \> **prévention des pertes de données** \> **Gestion des périphériques**.
    
2. Dans la page **Gestion des périphériques mobiles pour Office 365** , vérifiez l’état des périphériques de l’utilisateur dont la stratégie appliquée. Vous pouvez filtrer ou trier par **tous les** pour afficher tous les périphériques ou **bloqué** pour afficher les périphériques bloqués. 
    
    ![Affichage des périphériques qui sont gérés par Mobile Device Manager](media/5c9fd069-b716-40d8-9b36-f9cfeae2139f.png)
  
3. Vous pouvez également effectuer une réinitialisation à distance complète ou sélective sur l’appareil. Pour obtenir des instructions, consultez la rubrique [Réinitialiser un appareil mobile dans Office 365](wipe-a-mobile-device.md).
    
## <a name="step-3-deploy-a-policy-to-your-organization"></a>Étape 3 : Déployer une stratégie dans votre organisation

Une fois que vous avez créé une stratégie d’appareil mobile et vérifié qu’il fonctionne comme prévu, le déployer dans votre organisation.
  
1. Dans Office 365, accédez à **sécurité &amp; centre de conformité** \> **prévention des pertes de données** \> **stratégies de sécurité des périphériques**.
    
2. Sélectionnez la stratégie que vous souhaitez déployer, puis choisissez **Modifier la stratégie** dans le \< _nom de la stratégie_ \> Panneau de configuration.  
    
3. Sélectionnez l’onglet **Déploiement**. 
    
4. Dans l’onglet **déploiement** , choisissez **Oui** ci-dessus **Sélectionnez un ou plusieurs groupes de sécurité qui contiennent les personnes que vous voulez appliquer cette stratégie** , puis sur **Ajouter**.
    
  - Dans le volet **Sélectionner un groupe** , vous pouvez rechercher un groupe à ajouter, vous pouvez filtrer par alias ou par nom complet. Vous pouvez également ajouter un groupe existant dans la liste de **groupes** . 
    
    Vous pouvez ajouter plusieurs groupes pour appliquer la stratégie.
    
    Cliquez sur **Ajouter** au bas du panneau. 
    
5. Cliquez sur **Enregistrer** sous l’onglet **déploiement** . 
    
    ![Déployer stratégie Mobile Device Manager dans votre organisation.](media/dc3e7fe5-201a-4e45-abe3-fc93e0b59028.png)
  
Chaque utilisateur la stratégie s’applique à aura la stratégie répercutée sur leur appareil la prochaine fois qu’ils se connectent à Office 365 à partir de leur appareil mobile. Si les utilisateurs n’ont pas eu une stratégie appliquée à leur appareil mobile, ils allez [recevoir une notification sur leur appareil](https://go.microsoft.com/fwlink/?LinkId=615272) avec les étapes pour inscrire et l’activer pour Mobile Device Manager pour Office 365. Une fois qu’ils réalisé l’inscription, la stratégie sera appliquée à leur appareil. 
  
## <a name="step-4-block-email-access-for-unsupported-devices"></a>Étape 4 : Bloquer courrier l’accès pour les périphériques non pris en charge

Pour aider à sécuriser les informations de votre organisation, vous devez bloquer access application pour Office 365 les courriers électroniques pour les appareils mobiles qui ne sont pas pris en charge par Mobile Device Manager pour Office 365. Pour obtenir la liste des périphériques pris en charge, voir [fonctionnalités de gestion des périphériques mobiles intégrées à Office 365](capabilities-of-mobile-device-management.md) . Pour ce faire : 
  
1. Accédez à la sécurité &amp; centre de conformité\> **prévention des pertes de données** \> **stratégies de sécurité des périphériques**.
    
2. Sélectionnez **Gérer les paramètres d’accès des périphériques de l’organisation**.
    
    ![Accéder au centre de conformité \> périphériques et cliquez sur Lier les paramètres d’accès de gérer les périphériques.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Pour bloquer les périphériques non pris en charge, choisissez **bloc** sous **Si un périphérique n’est pas pris en charge par Mobile Device Manager pour Office 365, procédez comme vous souhaitez autoriser ou bloquer à partir de l’aide d’un compte Exchange pour accéder à leur messagerie de votre organisation** \> **Enregistrer**.
  
## <a name="step-5-choose-security-groups-to-be-excluded-from-conditional-access-checks"></a>Étape 5 : Choisir les groupes de sécurité à exclure des vérifications d’accès conditionnel

Si vous souhaitez exclure certaines personnes des vérifications d’accès conditionnel sur leur appareil mobile et que vous avez créé un ou plusieurs groupes de sécurité pour ces personnes, ajoutez les groupes de sécurité ici. Aucune stratégie ne sera appliquée aux appareils mobiles pris en charge des membres de ces groupes.
  
1. Accédez à la sécurité &amp; centre de conformité\> **prévention des pertes de données** \> **stratégies de sécurité des périphériques**.
    
2. Sélectionnez **Gérer les paramètres d’accès des périphériques de l’organisation**.
    
    ![Accéder au centre de conformité \> périphériques et cliquez sur Lier les paramètres d’accès de gérer les périphériques.](media/b9f4da3c-dfa5-4913-8482-42a077cb4f56.png)
  
3. Sélectionnez **Ajouter** pour ajouter le groupe de sécurité qui accueille des utilisateurs que vous souhaitez exclure de l’interdit l’accès à Office 365. Lorsqu’un utilisateur a été ajouté à cette liste, ils serez en mesure d’accéder à leur messagerie Office 365 lors de l’utilisation d’un périphérique non pris en charge. 
    
4. Sélectionnez le groupe de sécurité que vous souhaitez utiliser dans le panneau de configuration **Sélectionnez groupe** . 
    
5. Sélectionnez le nom, puis sur **Ajouter** \> **Enregistrer**.
    
6. Dans le panneau de **l’organisation du périphérique access** , cliquez sur **Enregistrer**.
  
## <a name="what-is-the-impact-of-security-policies-on-different-device-types"></a>Quel est l’impact des stratégies de sécurité sur les différents types d’appareils ?

Lorsque vous appliquez une stratégie à des appareils utilisateur, l’impact sur chaque appareil varie légèrement entre les différents types. Consultez le tableau suivant pour obtenir des exemples de l’impact des stratégies sur les différents appareils.
  


|**Stratégie de sécurité**|**Windows Phone 8.1 +**|**Android 4+**|**Samsung Knox**|**IOS 6 +**|**Remarques**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|Exiger la sauvegarde chiffrée  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |Sauvegarde chiffrée iOS requise.  <br/> |
|Bloquer la sauvegarde sur le cloud  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |Sauvegarde Google bloquée sur Android (grisé), sauvegarde sur le cloud sous iOS.  <br/> |
|Bloquer la synchronisation de documents  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS : bloquer les documents dans le cloud.  <br/> |
|Bloquer la synchronisation de photos  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS (natif) : bloquer le flux de photos.  <br/> |
|Bloquer la capture d’écran  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Bloqué lors de la tentative.  <br/> |
|Bloquer la visioconférence  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |FaceTime bloqué sous iOS, mais pas Skype ou autres.  <br/> |
|Bloquer l’envoi de données de diagnostic  <br/> |✖  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Bloquer l’envoi des rapports d’incident Google sur Android.  <br/> |
|Bloquer l’accès au magasin d’applications  <br/> |✔  <br/> |X  <br/> |✔  <br/> |✔  <br/> |Icône du magasin d’applications manquante sur la page d’accueil Android, désactivée sous Windows, manquante sous iOS.  <br/> |
|Exiger le mot de passe pour le magasin d’applications  <br/> |✖  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |iOS : Mot de passe requis pour les achats iTunes.  <br/> |
|Bloquer la connexion au stockage amovible  <br/> |✔  <br/> |X  <br/> |✔  <br/> |N/A  <br/> |Android : carte SD grisée dans les paramètres, Windows avertit l’utilisateur, les applications qui y sont installées ne sont pas disponibles  <br/> |
|Bloquer la connexion Bluetooth  <br/> |✔  <br/> |\*\*\*  <br/> |\*\*\*  <br/> |✖  <br/> |\*\*\*Nous ne pouvons pas désactiver BlueTooth en tant que paramètre sur Android. Au lieu de cela, nous désactiver toutes les transactions qui requièrent BlueTooth : Distribution Audio avancée, contrôle à distance de Audio/vidéo, périphériques mains libres, casque, accès annuaire et le Port série. Un message de petites toast s’affiche en bas de la page lorsqu’un de ces est utilisé.  <br/> |
   
## <a name="what-happens-when-you-delete-a-policy-or-remove-a-user-from-the-policy"></a>Que se passe-t-il lorsque vous supprimez une stratégie ou un utilisateur de la stratégie ?

Lorsque vous supprimez une stratégie ou supprimez un utilisateur d’un groupe auquel la stratégie a été déployée sur, les paramètres de stratégie, profil de messagerie Office 365 et les messages électroniques mis en cache peuvent être retirés appareil de l’utilisateur. Voir le tableau suivant pour voir ce qui est supprimé pour les différents types de périphériques :
  
|**Éléments supprimés**|**Windows Phone 8.1 +**|**iOS 6 +**|**Android 4 + (y compris le Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|Profils de courrier électronique géré\*  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|Paramètres de stratégie  <br/> |✔  <br/>           Sauf pour **Bloquer l’envoi de données de diagnostic à partir de l’appareil**. <br/> |✔  <br/> |✖  <br/> |
   
> [!NOTE]
> \*Si la stratégie a été déployée avec l’option de **profil de messagerie est géré** sélectionné, puis le profil de messagerie gérés et mis en cache les messages électroniques dans la mesure où profil sera supprimé de l’appareil de l’utilisateur. 
  
La stratégie supprimée appliqués à chaque utilisateur aura la stratégie supprimée de leur appareil lors du prochain que contrôle de leur appareil mobile avec Mobile Device Manager pour Office 365. Si vous déployez une nouvelle stratégie qui s’applique aux périphériques de ces utilisateurs, vous serez invités ils réinscrire Mobile Device Manager pour Office 365.
  
Vous pouvez également [Réinitialiser un appareil](wipe-a-mobile-device.md), soit complètement ou sélective réinitialiser les informations d’organisation de l’appareil.
  
## <a name="related-topics"></a>Voir aussi

[Vue d’ensemble de la gestion des appareils mobiles pour Office 365](overview-of-mdm.md)
  
[Fonctions de gestion des appareils mobiles pour Office 365](capabilities-of-mobile-device-management.md)
  

