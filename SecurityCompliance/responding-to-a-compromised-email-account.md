---
title: Réponse à un compte de messagerie compromis dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365
ms.openlocfilehash: 6d5bed2172aaade02de617efa1c9c9c8d851e647
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30656050"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Réponse à un compte de messagerie compromis dans Office 365

**Résumé** Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Qu'est-ce qu'un compte de courrier compromis dans Office 365?
L'accès aux boîtes aux lettres, aux données et aux autres services Office 365 est contrôlé par le biais d'informations d'identification, par exemple, un nom d'utilisateur et un mot de passe ou un code confidentiel. Quand une personne autre que l'utilisateur concerné vole ces informations d'identification, les informations d'identification dérobées sont considérées comme compromises. Ils peuvent ainsi se connecter en tant qu'utilisateur d'origine et effectuer des actions illicites.
À l'aide des informations d'identification dérobées, l'agresseur peut accéder à la boîte aux lettres Office 365 de l'utilisateur, à des dossiers SharePoint ou à des fichiers dans le OneDrive de l'utilisateur. L'agresseur envoie des courriers électroniques en tant qu'utilisateur d'origine à des destinataires à l'intérieur et à l'extérieur de l'organisation. Lorsque l'agresseur envoie des données à des destinataires externes, il s'agit de l'exfiltration des données.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Symptômes d'un compte de messagerie Office 365 compromis
Les utilisateurs peuvent remarquer et signaler une activité inhabituelle dans leurs boîtes aux lettres Office 365. Voici quelques symptômes courants:
- Activité suspecte, telle que des e-mails manquants ou supprimés.
- D'autres utilisateurs peuvent recevoir des courriers électroniques du compte compromis sans le message correspondant existant dans le dossier **éléments envoyés** de l'expéditeur.
- La présence de règles de boîte de réception qui n'ont pas été créées par l'utilisateur ou l'administrateur concerné. Ces règles peuvent transférer automatiquement des courriers électroniques vers des adresses inconnues ou les déplacer vers les dossiers **Notes**, courrier indésirable ou **abonnement RSS** . ****
- Le nom d'affichage de l'utilisateur peut être modifié dans la liste d'adresses globale.
- La boîte aux lettres de l'utilisateur est bloquée pour l'envoi de messages électroniques.
- Les dossiers éléments envoyés ou supprimés dans Microsoft Outlook ou Outlook sur le Web (anciennement Outlook Web App) contiennent des messages courants de compte piraté, tels que «je suis bloqué à Londres, envoyer de l'argent».
- Les modifications apportées aux profils inHabituels, telles que le nom, le numéro de téléphone ou le code postal ont été mises à jour.
- Des modifications d'informations d'identification inHabituelles, telles que plusieurs modifications de mot de passe sont requises.
- Le transfert du courrier a récemment été ajouté.
- Une signature inhabituelle a été récemment ajoutée, telle qu'une signature bancaire fictive ou une signature médicamenteuse de prescription.

Si un utilisateur signale l'un des symptômes ci-dessus, vous devez effectuer une nouvelle enquête. Le centre de sécurité & Office 365 et le portail Azure fournissent des outils pour vous aider à examiner l'activité d'un compte d'utilisateur que vous soupçonnez être compromis.
- Journaux d'audit unifiés Office 365 dans le centre de sécurité & Compliance Center-examinez toutes les activités du compte suspect en filtrant les résultats pour la plage de dates comprise entre immédiatement avant que l'activité suspecte ait eu lieu jusqu'à la date actuelle. Ne filtrez pas les activités lors de la recherche.
- Utilisez les journaux de connexion Azure AD et d'autres rapports sur les risques disponibles dans le portail Azure AD. Examinez les valeurs des colonnes suivantes:
    - Vérifier l'adresse IP
    - emplacements de connexion
    - heures de connexion
    - succès ou échec de connexion

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Procédure de sécurisation et de restauration de la fonction de messagerie sur un compte et une boîte aux lettres Office 365 compromis.

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Même si l'accès à votre compte a été rétabli, l'agresseur peut avoir ajouté des entrées de portes dérobées qui permettent à l'agresseur de reprendre le contrôle du compte.

Vous devez effectuer toutes les étapes suivantes pour accéder à nouveau à votre compte plus rapidement, afin de vous assurer que le pirate ne reprend pas le contrôle de votre compte. Ces étapes vous aident à supprimer les entrées de porte d'arrière que le pirate a pu ajouter à votre compte. Après avoir effectué ces étapes, nous vous recommandons d'exécuter une analyse antivirus afin de vous assurer que votre ordinateur n'est pas compromis.

### <a name="step-1-reset-the-users-password"></a>Étape 1 réinitialiser le mot de passe de l'utilisateur
> [!WARNING]
> N'envoyez pas le nouveau mot de passe à l'utilisateur prévu par courrier électronique, car l'agresseur a toujours accès à la boîte aux lettres à ce stade.

1. Suivez les procédures de réInitialisation d'un mot de passe Office 365 Business pour quelqu'un d'autre dans [administrateurs: Reset office 365 Business passwords](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Remarques :**
- Assurez-vous que le mot de passe est fort et qu'il contient des lettres majuscules et minuscules, au moins un chiffre et au moins un caractère spécial. 
- Ne réutilisez pas vos cinq derniers mots de passe. Même si l'utilisation de l'historique des mots de passe vous permet de réutiliser un mot de passe plus récent, vous devez sélectionner un élément que l'agresseur ne peut pas deviner.
- Si votre identité sur site est fédérée avec Office 365, vous devez modifier votre mot de passe local, puis informer votre administrateur du compromis.

> [!TIP]
> Il est vivement recommandé d'activer l'authentification multiFacteur (MFA) afin d'éviter toute compromission, en particulier pour les comptes disposant de privilèges d'administration.  Pour plus d'informations, consultez la [rubrique](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Étape 2 supprimer les adresses de transfert de messages suspectes
1. Ouvrez le **Centre d'administration Office 365 _GT_ utilisateurs actifs**.
2. Recherchez le compte d'utilisateur en question et développez **paramètres de messagerie**.
3. Pour le **transfert du courrier**, cliquez sur **modifier**.
4. Supprimez toutes les adresses de transfert suspectes.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Étape 3 désactiver toutes les règles de boîte de réception suspectes
1. Connectez-vous à la boîte aux lettres de l'utilisateur à l'aide d'Outlook sur le Web.
2. Cliquez sur l'icône d'engrenage, puis sur **courrier**.
3. Cliquez sur **règles de boîte de réception et de nettoyage** , puis passez en revue les règles.
4. DésActivez ou supprimez les règles suspectes.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Étape 4 déBloquer l'envoi du courrier électronique à l'utilisateur
Si la boîte aux lettres compromise suspecte a été utilisée de façon illicite pour envoyer du courrier indésirable, il est probable que la boîte aux lettres a été bloquée.
1. Pour débloquer une boîte aux lettres d'envoi de messages, suivez les procédures de [Suppression d'un utilisateur, d'un domaine ou d'une adresse IP d'une liste rouge après l'envoi du courrier](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email )indésirable.

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Étape 5 facultative: empêcher le compte d'utilisateur de se connecter
> [!IMPORTANT]
> Vous pouvez bloquer la connexion à un compte compromis jusqu'à ce qu'il soit sûr de pouvoir réactiver l'accès.

1. Go to the Office 365 admin center.
2. Dans le Centre d'administration Office 365, sélectionnez **Utilisateurs**.
3. Sélectionnez l'employé que vous voulez bloquer, puis cliquez sur **modifier** en regard de l' **État de connexion** dans le volet utilisateur.
4. Dans le volet **État de la connexion**, choisissez **Connexion bloquée**, puis **Enregistrer**. 
5. Dans le centre d'administration Office 365, dans le volet de navigation en bas à gauche, développez **centres d'administration** et sélectionnez **Exchange**.
6. Dans le centre d'administration Exchange, accédez à **destinataires _GT_ boîtes aux lettres**.
7. Sélectionnez l'utilisateur, puis dans la page Propriétés de l'utilisateur, sous **appareils mobiles**, cliquez sur **Désactiver Exchange ACTIVCSYNC** et **Désactiver OWA pour les périphériques** , puis répondez **Oui** aux deux.
8. Sous **connectivité de messagerie**, désactivez et répondez **Oui**. **** 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Étape 6 (facultatif): supprimer le compte suspect compromis de tous les groupes de rôles d'administration
> [!NOTE]
> L'appartenance au groupe de rôles d'administration peut être restaurée une fois que le compte a été sécurisé.

1. Connectez-vous au centre d'administration Office 365 avec un compte d'administrateur général et ouvrez **utilisateurs actifs**.
2. Recherchez le compte compromis suspect et vérifiez manuellement s'il existe des rôles d'administration attribués au compte.
3. Ouvrez le **Centre de sécurité _AMP_ Compliance Center**.
4. Cliquez sur **Autorisations**.
5. Passez en revue manuellement les groupes de rôles pour voir si le compte suspect compromis est membre de l'un d'entre eux.  S'il s'agit de: a. Cliquez sur le groupe de rôles, puis sur **modifier le groupe de rôles**.
    b. Cliquez sur **choisir les membres** , puis sur **modifier** pour supprimer l'utilisateur du groupe de rôles.
6. Ouvrir le **Centre d'administration Exchange**
7. Cliquez sur **Autorisations**.
8. Passez en revue manuellement les groupes de rôles pour voir si le compte suspect compromis est membre de l'un d'entre eux. S'il s'agit de: a. Cliquez sur le groupe de rôles, puis cliquez sur **modifier**.
    b. Utilisez la section **membres** pour supprimer l'utilisateur du groupe de rôles.

### <a name="step-7-optional-additional-precautionary-steps"></a>Étape 7 facultative: étapes de précaution supplémentaires
1. Vérifiez que vous avez bien vérifié vos éléments envoyés. Vous devrez peut-être informer les personnes de votre liste de contacts que votre compte a été compromis. L'agresseur peut être invité à le faire, par exemple, une usurpation d'identité, par exemple, que vous étiez bloqué dans un autre pays et que vous avez besoin d'argent, ou que l'agresseur puisse lui envoyer un virus pour détourner les ordinateurs.
2. Tout autre service qui utilisait ce compte Exchange comme autre compte de messagerie a peut-être été compromis. Tout d'abord, effectuez ces étapes pour votre abonnement Office 365, puis effectuez ces étapes pour vos autres comptes.
3. Assurez-vous que les informations de contact, telles que les numéros de téléphone et les adresses, sont correctes.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sécuriser Office 365 comme un Cybersecurity Pro
Votre abonnement Office 365 est fourni avec un ensemble de fonctionnalités de sécurité puissantes que vous pouvez utiliser pour protéger vos données et vos utilisateurs.  Utilisez la feuille de [route de sécurité Office 365: les principales priorités pour les 30 jours, 90 jours et au-delà](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) pour implémenter les meilleures pratiques recommandées par Microsoft pour la sécurisation de votre client Office 365.
- Tâches à accomplir dans les 30 premiers jours.  Ceux-ci ont des effets immédiats et ont un faible impact sur vos utilisateurs.
- Tâches à effectuer dans les 90 jours. La planification et l'implémentation de ces deux éléments prennent un peu plus de temps, mais améliorent grandement votre position de sécurité.
- Au-delà de 90 jours. Ces améliorations s'appuient sur vos premiers 90 jours de travail.

## <a name="see-also"></a>Voir aussi :
- [Meilleures pratiques en matière de sécurité pour Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Internet Crime Complaint Center](http://www.ic3.gov/preventiontips.aspx)
- [Securities and Exchange Commission-fraude de hameçonnage](http://www.sec.gov/investor/pubs/phishing.htm)
