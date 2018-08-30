---
title: Fonctionnalités de gestion des appareils mobiles intégrée pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.DevicePolicySupportedDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: a1da44e5-7475-4992-be91-9ccec25905b0
description: Gestion des périphériques mobiles pour Office 365 peut vous aider à sécuriser et gérer des appareils mobiles tels que les iPhone, tablettes, Androïd et Windows Phone utilisés dans votre organisation. Créer des stratégies de gestion de périphériques mobiles avec des paramètres qui peuvent aider à contrôle l’accès à la messagerie Office 365 et des documents pour les appareils mobiles pris en charge et les applications de votre organisation et vous permet de réinitialiser un appareil à distance si elle est volé.
ms.openlocfilehash: b7200eee3b50c2fc6d3e0ea0920236d71837a88b
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272599"
---
# <a name="capabilities-of-built-in-mobile-device-management-for-office-365"></a>Fonctionnalités de gestion des appareils mobiles intégrée pour Office 365

Gestion des périphériques mobiles pour Office 365 peut vous aider à sécuriser et gérer des appareils mobiles tels que les iPhone, tablettes, Androïd et téléphones Windows utilisé par les utilisateurs sous licence Office 365 dans votre organisation. Vous pouvez créer des stratégies de gestion des appareils mobiles avec des paramètres qui peuvent aider à contrôler l’accès à la messagerie de votre organisation Office 365 et des documents pour les applications et les appareils mobiles pris en charge. Si un périphérique est perdu ou volé, vous pouvez réinitialiser à distance le périphérique pour supprimer des informations sensibles d’organisation.
    
Besoin de plus de fonctionnalités est inclus dans Mobile Device Manager pour Office 365 ? Si Microsoft Intune dispose de ce dont vous avez besoin : [choisir entre Mobile Device Manager pour Office 365 et Microsoft Intune](choose-between-mdm-and-intune.md).
  
## <a name="supported-devices"></a>Appareils pris en charge

Vous pouvez utiliser Mobile Device Manager pour Office 365 pour sécuriser et gérer les types suivants d’appareils.
  
- Windows Phone 8.1 +
    
- iOS 7.1 ou versions ultérieures
    
- Android 4 ou versions ultérieures
    
- Windows 8.1\*
    
- Windows 8.1 RT\*
    
- 10 Windows\*\*
    
- Windows 10 Mobile\*\*
    
\*Contrôle d’accès pour les appareils Windows 8.1 et Windows 8.1 RT est limité à Exchange ActiveSync.
  
\*\*Nécessite le périphérique pour être joint au Azure Active Directory et inscrit dans le service de gestion d’appareil mobile de votre organisation.
  
Si les personnes dans votre organisation utilisent des périphériques mobiles qui ne sont pas pris en charge par la gestion des périphériques mobiles pour Office 365, vous souhaitez bloquer l’accès Exchange ActiveSync application pour Office 365 les courriers électroniques de ces périphériques, pour aider à sécuriser les données de votre organisation. Étapes pour le blocage d’Exchange ActiveSync : voir [Gérer les paramètres d’accès au périphérique](manage-device-access-settings.md).
  
## <a name="access-control-for-office-365-email-and-documents"></a>Contrôle d’accès pour la messagerie et les documents Office 365

Les applications pris en charge pour les différents types d’appareils mobiles dans le tableau suivant invitent les utilisateurs à inscrire pour Office 365 où il y a une nouvelle stratégie de gestion d’appareil mobile qui s’applique aux périphériques d’un utilisateur et l’utilisateur n’a pas encore inscrit précédemment l’appareil mobile Device Manager. Si le périphérique d’un utilisateur n’est pas conforme à une stratégie, en fonction de la façon dont vous configurer la stratégie, un utilisateur peut ne pas accéder aux ressources Office 365 dans ces applications, ou ils n’ont pas accès, mais Office 365 signale une violation de stratégie.
  
||**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|
|:-----|:-----|:-----|:-----|
|**Exchange** <br/> Exchange ActiveSync inclut le courrier intégré et les applications de tiers, comme TouchDown, qui utilisent Exchange ActiveSync 14.1 ou Version ultérieure.  <br/> |![Icône ActiveSync Exchange](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Icône de messagerie Exchange mobile](media/5b5312b4-3bfb-4fc7-84ff-d7ab21227c10.png)Messagerie Exchange  <br/> |![Icône ActiveSync Exchange](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Icône iPhone Mail mobile](media/888bdc7a-8354-4013-a0b2-0d4432a9a92e.png)Courrier  <br/> |![Icône ActiveSync Exchange](media/b36e36ba-88a5-4b2e-bd1d-7432b751a60c.png)Exchange ActiveSync  <br/> ![Icône de la messagerie Android](media/20b48492-4adc-40ce-99cf-1b47bd2b389d.png)Courrier électronique  <br/> |
|**Office** et **OneDrive Entreprise** <br/> |Aucune application prise en charge  <br/> |![Icône iPhone Outlook mobile](media/6c63112d-c10c-4040-85cc-feeccc3dd424.png)Outlook  <br/> ![Icône iPhone OneDrive mobile](media/560ec187-82d9-4793-b72f-7ba595972bdc.png)OneDrive  <br/> ![Icône iPhone Word mobile](media/63a3a749-1f98-402f-b211-e46b9224b655.png)Word  <br/> ![Icône iPhone Excel mobile](media/5b8f62c0-96aa-4602-9ed8-f837bbf5fa9e.png)Excel  <br/> ![Icône iPhone PowerPoint mobile](media/17c02dca-f60a-4d13-a610-00d576a40943.png)PowerPoint  <br/> |**Sur les téléphones et tablettes :** <br/> ![Android tablette et téléphonie mobile icône Outlook](media/ed2a813d-f481-46e0-acc9-6422f0d16072.png)Outlook  <br/> ![Icône mobile de téléphone Android OneDrive](media/64855d02-1684-4795-b4c5-863860f18722.png)OneDrive  <br/> ![Android icône mobile Word](media/f618fe83-b163-4680-b924-fcedc06ab4ba.png)Word  <br/> ![Android icône mobile Excel](media/659c7a5f-5797-4b47-a776-4a0c8f784c89.png)Excel  <br/> ![Android icône mobile PowerPoint](media/35b98bce-d7cb-40ce-87e3-07b9764207b1.png)PowerPoint  <br/> **Sur les téléphones uniquement :** <br/> ![Icône mobile Mobile Office](media/1aa9e978-6eb2-40aa-82da-62fb79cee313.png)Office Mobile  <br/> |
   
> [!NOTE]
>  Prise en charge pour iOS 7.1 et versions ultérieures inclut des périphériques iPhone et iPad. > Gestion des appareils BlackBerry n’est pas pris en charge par la gestion des périphériques mobiles pour Office 365. BlackBerry Business Cloud Services (BBCS) à partir de BlackBerry permet de gérer les périphériques BlackBerry. > Les utilisateurs ne sont pas invités à inscrire et ne sont pas bloqués ou signalées pour violation de stratégie s’ils utilisent le navigateur mobile pour accéder aux sites SharePoint Office 365, documents sur Office Online ou messagerie dans Outlook Web App. 
  
Le diagramme suivant illustre ce qui se produit lorsqu’un utilisateur à un nouveau périphérique se connecte à une application que prend en charge contrôle d’accès avec Mobile Device Manager pour Office 365. L’utilisateur ne peut pas accéder à des ressources d’Office 365 dans l’application jusqu'à ce qu’ils s’inscrivent leur appareil.
  
![Illustre le processus d’inscription pour le nouveau périphérique.](media/O365-MDM-Capabilities-EnrollmentExample.png)
  
> [!NOTE]
> Stratégies et règles d’accès créées dans Mobile Device Manager pour Office 365 remplacera les stratégies de boîte aux lettres d’appareil mobile Exchange ActiveSync et les règles d’accès aux périphériques créés dans le centre d’administration Exchange. Une fois un périphérique Mobile Device Manager est inscrit pour Office 365, toute stratégie de boîte aux lettres d’appareil mobile Exchange ActiveSync ou la règle d’accès aux périphériques appliquée au périphérique sera ignoré. Pour plus d’informations sur Exchange ActiveSync, consultez la rubrique [Exchange ActiveSync dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=524380). 
  
## <a name="policy-settings-for-mobile-devices"></a>Paramètres de stratégie pour les appareils mobiles

Si vous créez une stratégie pour bloquer l’accès à certains paramètres activées, les utilisateurs seront bloquées d’accéder aux ressources Office 365 lors de l’utilisation d’une application pris en charge qui est répertoriée dans le [contrôle d’accès pour les documents et de messagerie Office 365](#access-control-for-office-365-email-and-documents). Les paramètres que vous pouvant empêcher les utilisateurs d’accéder aux ressources Office 365 sont dans les sections suivantes :
  
- Sécurité
    
- Chiffrement
    
- Débridage
    
- Profil de messagerie géré
    
Par exemple, le diagramme suivant illustre ce qui se produit lorsqu’un utilisateur disposant d’un périphérique inscrit n’est pas compatible avec un paramètre de sécurité dans une stratégie de gestion d’appareil mobile qui s’applique à leur appareil. L’utilisateur se connecte à une application que prend en charge contrôle d’accès avec Mobile Device Manager pour Office 365. Ils ne peuvent pas accéder à des ressources d’Office 365 dans l’application jusqu'à ce que leur appareil est conforme avec le paramètre de sécurité.
  
![Indique que l’utilisateur est bloqué lorsque le périphérique n’est pas conforme.](media/O365-MDM-Capabilities-ComplianceExample.png)
  
Les sections suivantes répertorient les paramètres de stratégie que vous pouvez utiliser pour sécuriser et gérer les périphériques mobiles qui se connectent à des ressources d’Office 365 de votre organisation. 
  
### <a name="security-settings"></a>Paramètres de sécurité

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exiger un mot de passe  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Empêcher l’utilisation de mots de passe simples  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Exiger un mot de passe alphanumérique  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Longueur minimale du mot de passe  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Nombre d’échecs de connexion avant la réinitialisation de l’appareil  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Durée d’inactivité (en minutes) avant le verrouillage de l’appareil  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Expiration du mot de passe (jours)  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Conserver l’historique des mots de passe et empêcher leur réutilisation  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="encryption-settings"></a>Paramètres de chiffrement

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exiger le chiffrement des données sur les appareils  <br/> |Windows Phone 8.1 est déjà chiffré et ne peut pas être déchiffré  <br/> |✖  <br/> |✔  <br/> |✔\*  <br/> |
   
\*Avec Samsung Knox, vous pouvez également exiger le chiffrement sur les cartes de stockage.
  
### <a name="jail-broken-setting"></a>Paramètre de débridage

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Impossible de débrider l’appareil ou de l’associer à une racine  <br/> |✖  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
   
### <a name="managed-email-profile-option"></a>Option de profil de messagerie géré

L’option suivante peut empêcher les utilisateurs d’accéder à leur messagerie électronique Office 365 s’il utilise un profil de messagerie créé manuellement. Les utilisateurs sur des appareils iOS doivent supprimer leur profil de messagerie créé manuellement avant de pouvoir accéder à leur messagerie électronique. Après avoir supprimé le profil, un nouveau profil est automatiquement créé sur l’appareil.
  
|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Le profil de messagerie est géré  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="cloud-settings"></a>Paramètres de cloud

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Exiger la sauvegarde chiffrée  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquer la sauvegarde sur le cloud  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquer la synchronisation de documents  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquer la synchronisation de photos  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Permettre la sauvegarde de Google  <br/> |N/D  <br/> |S/O  <br/> |✖  <br/> |✔  <br/> |
|Autoriser la synchronisation automatique de compte Google  <br/> |N/D  <br/> |S/O  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="system-settings"></a>Paramètres système

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquer la capture d’écran  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Empêcher l’envoi de données de diagnostic à partir de l’appareil  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="application-settings"></a>Paramètres d’application

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquer la visioconférence sur l'appareil  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
|Bloquer l'accès au magasin d'applications  <br/> |✔  <br/> |✔  <br/> |✖  <br/> |✔  <br/> |
|Exiger un mot de passe en cas d'accès au magasin d'applications  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="device-capabilities-settings"></a>Paramètres de fonctionnalités d’appareil

|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4+**|**Samsung Knox**|
|:-----|:-----|:-----|:-----|:-----|
|Bloquer la connexion au stockage amovible  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|Bloquer la connexion Bluetooth  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
   
### <a name="additional-settings"></a>Paramètres supplémentaires

Vous pouvez définir les paramètres de stratégie supplémentaires à l’aide des applets de commande PowerShell. Pour plus d’informations, voir [Office 365 sécurité &amp; centre de conformité des applets de commande](https://go.microsoft.com/fwlink/p/?LinkId=827804).
  
|**Nom du paramètre**|**Windows Phone 8.1 +**|**iOS 7.1+**|**Android 4 + (y compris le Samsung Knox)**|
|:-----|:-----|:-----|:-----|
|CameraEnabled  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|RegionRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MoviesRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|TVShowsRating  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AppsRatings  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceDialing  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowVoiceAssistant  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowAssistantWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|AllowPassbookWhileLocked  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|MaxPasswordGracePeriod  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|PasswordQuality  <br/> |✖  <br/> |✖  <br/> |✔  <br/> |
|SystemSecurityTLS  <br/> |✖  <br/> |✔  <br/> |✖  <br/> |
|WLANEnabled  <br/> |✔  <br/> |✖  <br/> |✖  <br/> |
   
### <a name="settings-supported-by-windows"></a>Pris en charge par Windows

Vous pouvez gérer les périphériques Windows 8.1 et 10 Windows par leur inscription en tant que les appareils mobiles. Après avoir déployé une stratégie applicable, les utilisateurs de périphériques Windows 8.1 RT et Windows 10 RT devront s’inscrire à Mobile Device Manager pour Office 365 la première fois qu’ils utilisent l’application de messagerie électronique intégrés pour accéder à leur messagerie électronique Office 365. 
  
Les paramètres suivants sont pris en charge pour les périphériques Windows 8.1 et 10 Windows qui sont inscrits en tant que les appareils mobiles. Ces paramètres ne sont pas empêcher les utilisateurs d’accéder aux ressources d’Office 365.
  
 **Paramètres de sécurité**
  
- Exiger un mot de passe alphanumérique
    
- Longueur minimale du mot de passe
    
- Nombre d’échecs de connexion avant la réinitialisation de l’appareil
    
- Durée d’inactivité (en minutes) avant le verrouillage de l’appareil
    
- Expiration du mot de passe (jours)
    
- Conserver l’historique des mots de passe et empêcher leur réutilisation
    
 **Paramètres système**
  
Empêcher l’envoi de données de diagnostic à partir de l’appareil
  
 **Paramètres supplémentaires**
  
Vous pouvez définir les paramètres de stratégie supplémentaires suivants à l’aide des cmdlets PowerShell :
  
- AllowConvenienceLogon
    
- UserAccountControlStatus
    
- FirewallStatus
    
- AutoUpdateStatus
    
- AntiVirusStatus
    
- AntiVirusSignatureStatus
    
- SmartScreenEnabled
    
- WorkFoldersSyncUrl
    
## <a name="remotely-wipe-a-mobile-device"></a>Réinitialiser un appareil mobile à distance

 Si un périphérique est perdu ou volé, vous pouvez supprimer les données sensibles d’organisation et aider à empêcher l’accès à des ressources d’Office 365 de votre organisation en effectuant une réinitialisation à distance à partir de **sécurité &amp; centre de conformité\>prévention des pertes de données\>périphérique gestion des**. Vous pouvez effectuer une réinitialisation sélective à supprimer uniquement les données d’organisation ou une réinitialisation à distance complet pour supprimer toutes les informations à partir d’un périphérique et la restaurer dans ses paramètres d’usine.
  
Pour plus d’informations, consultez la rubrique [Réinitialiser un appareil mobile dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=518157).
  
## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la gestion des appareils mobiles pour Office 365](overview-of-mdm.md)
  
[Créer et déployer des stratégies de sécurité des appareils](create-device-security-policies.md)

