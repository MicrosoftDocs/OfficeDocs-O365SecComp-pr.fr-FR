---
title: Réinitialiser un appareil mobile dans Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Vous pouvez utiliser la gestion intégrée des périphériques mobiles pour Office 365 pour effectuer une réinitialisation à sélective pour supprimer uniquement les informations d’organisation, ou une réinitialisation à distance complet pour supprimer toutes les informations à partir d’un appareil mobile et la restaurer dans ses paramètres d’usine.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272499"
---
# <a name="wipe-a-mobile-device-in-office-365"></a>Réinitialiser un appareil mobile dans Office 365
  
Vous pouvez utiliser la gestion intégrée des périphériques mobiles pour Office 365 pour effectuer une réinitialisation à sélective pour supprimer uniquement les informations d’organisation, ou une réinitialisation à distance complet pour supprimer toutes les informations à partir d’un appareil mobile et la restaurer dans ses paramètres d’usine.
  
## <a name="what-to-know-before-you-begin"></a>Éléments à connaître avant de commencer

- Appareils mobiles peuvent stocker des informations sensibles d’organisation et de fournir un accès aux ressources de votre organisation Office 365. Pour protéger les informations de votre organisation, vous pouvez effectuer une réinitialisation à distance complet ou une réinitialisation sélective à :
    
  - **Réinitialisation à distance complet**: supprime toutes les données sur l’appareil mobile d’un utilisateur, y compris les applications installées, des photos et des informations personnelles. Lors de la transition est terminée, le périphérique est restauré à ses paramètres par défaut. 
    
  - **Balayage sélective**: supprime uniquement les données d’entreprise et applications laisse installé, photos et des informations personnelles sur l’appareil mobile d’un utilisateur. 
    
- Lorsqu’un périphérique est effacé (réinitialisation à distance complète ou sélective réinitialisation à distance), le périphérique est supprimé de la liste des périphériques gérés.
    
- Vous pouvez configurer une stratégie de gestion des appareils mobiles qui efface automatiquement (réinitialisation à distance complet) un périphérique une fois que l’utilisateur ne parvient pas à entrer le mot de passe du périphérique un certain nombre de fois. Suivez les étapes de [créer et déployer des stratégies de sécurité des périphériques](create-device-security-policies.md).
    
- Si vous souhaitez en savoir qu’un utilisateur fera l’expérience lorsque vous réinitialiser leur appareil, voir [Quel est l’impact des utilisateurs et des périphériques ?](wipe-a-mobile-device.md#BKMK_Impact).
    
## <a name="wipe-a-mobile-device"></a>Réinitialiser un appareil mobile

1. Accédez à la [ ![cliquez ici pour accéder au centre d’administration Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).

2. Accédez à [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **prévention des pertes de données** \> **Gestion des périphériques**.
    
3. Sélectionnez le périphérique que vous souhaitez effacer.
    
4. Sélectionnez le type de réinitialisation à distance, que vous souhaitez effectuer.
    
  - Pour effectuer une réinitialisation à sélective et de supprimer uniquement Office 365 informations sur l’organisation, dans le volet droit, sélectionnez **balayage sélective**.
    
  - Pour effectuer une réinitialisation à distance complet et restaurer le périphérique ses paramètres, dans le volet droit, sélectionnez **complète réinitialisation à distance**.
    
![Sélectionnez un périphérique, puis choisissez le type de réinitialisation à faire.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. Sélectionnez **Oui** pour confirmer. 
    
Avant la fin de la transition, l' **état du périphérique** affiche **RetirePending** ou **RetireIssued**.
  
### <a name="how-do-i-know-it-worked"></a>Comment savoir si qu'elle a fonctionné ?

Vous verrez n’est plus l’appareil mobile dans la liste des périphériques gérés.
  
## <a name="why-would-you-want-to-wipe-a-device"></a>Pourquoi vous souhaitez réinitialiser un appareil ?

Il existe plusieurs raisons pour le nettoyage des périphériques :
  
- Les appareils mobiles tels que les smartphones et tablettes sont de plus en plus complètes tout le temps. Cela signifie qu’il est plus facile pour vos utilisateurs de stocker des informations sensibles d’entreprise (tels que les données d’identification personnelle ou communications confidentielles) et y accéder en déplacement. Si une de ces appareils mobiles est perdue ou volée, effacement le périphérique immédiatement permet d’éviter les informations de votre organisation à partir de la fin de compte les mains.
    
- Lorsqu’un utilisateur quitte l’organisation avec un périphérique personnel qui est inscrit dans Mobile Device Manager pour Office 365, vous pouvez empêcher d’organisation des informations avec les utilisateurs en effectuant une réinitialisation à sélective.
    
- Si votre organisation fournit les appareils mobiles pour les utilisateurs, vous devrez peut-être réaffecter des périphériques à tout moment. Une réinitialisation à distance complet sur un appareil avant de l’assigner à un nouveau permet d’utilisateur ainsi que des informations sensibles à partir du propriétaire précédent sont supprimées.
    
## <a name="whats-the-user-and-device-impact"></a>Quel est l’utilisateur et l’impact de l’appareil ?

La réinitialisation à distance est immédiatement envoyée à l’appareil mobile. Le périphérique est également marqué comme n’est pas compatible dans DAS.
  
Le tableau suivant décrit le contenu est supprimé pour chaque type de périphérique lorsqu’un périphérique est effacé de manière sélective.
  
|**Impact de contenu**|**Windows Phone 8.1**|**iOS 7.1+**|**Android 4+**|
|:-----|:-----|:-----|:-----|
|Application de portail d’entreprise\* est désinstallé.  <br/> |S/O  <br/> |✔  <br/> |S/O  <br/> |
|Données d’application Office 365 hébergées par les applications où le contrôle d’accès est pris en charge par Mobile Device Manager pour Office 365 sont supprimé (actuellement Outlook et OneDrive entreprise). Les applications ne sont pas supprimées.  <br/> Outlook pour Android ne supprime pas les messages électroniques mis en cache.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Paramètres de stratégie qui ont été appliquées par Mobile Device Manager pour Office 365 pour les périphériques ne s’appliquent plus sur l’appareil et que les utilisateurs peuvent modifier les paramètres.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Profils de messagerie créés par Mobile Device Manager pour Office 365 sont supprimés et messagerie mis en cache sur le périphérique est supprimé.  <br/> |S/O  <br/> |✔  <br/> |S/O  <br/> |
   
> [!NOTE]
> \*Application de portail d’entreprise est disponible au niveau de l’App Store pour iOS et le magasin de lecture pour les appareils Android. 
  
## <a name="related-content"></a>Contenu connexe

[Gérer les appareils mobiles dans Office 365](set-up-mobile-device-management.md)
  

