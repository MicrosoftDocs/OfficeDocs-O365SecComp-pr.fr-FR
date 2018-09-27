---
title: Réponse à un compte de messagerie compromis dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365
ms.openlocfilehash: b10bf58aaebc46938e3962494ff30dfb1e226130
ms.sourcegitcommit: 411713004251ee62d29b550eabea04c08a87e41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25341419"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Réponse à un compte de messagerie compromis dans Office 365

**Résumé** Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Qu’est un compte de messagerie compromise dans Office 365 ?
Accès aux boîtes aux lettres, les données et les autres services Office 365, est contrôlé par l’utilisation des informations d’identification, telles qu’un nom d’utilisateur et mot de passe ou code confidentiel. Lorsqu’une personne autre que l’utilisateur concerné vol ces informations d’identification, les informations d’identification volées sont considérés comme d’être compromis. Avec eux, l’intrus peut se connecter en tant que l’utilisateur d’origine et effectuer les actions illicites. Utilisant les informations d’identification volées, l’intrus peut accéder à boîte aux lettres Office 365, les dossiers SharePoint ou les fichiers OneDrive de l’utilisateur de l’utilisateur. Une seule action communément est l’intrus l’envoi de messages électroniques en tant que l’utilisateur d’origine aux destinataires à l’intérieur et à l’extérieur de l’organisation. Lorsque l’intrus envoie des données à des destinataires externes, il s’agit d’exfiltration de données.

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Symptômes d’un compte de messagerie compromis Office 365
Les utilisateurs peuvent remarquer et signaler une activité inhabituelle dans leurs boîtes aux lettres Office 365. Voici quelques symptômes courants :
- Activités suspectes, telles que les messages électroniques manquants ou supprimés.
- Les autres utilisateurs peuvent recevoir les messages électroniques à partir du compte compromis sans l’e-mail correspondante existants dans le dossier **Éléments envoyés** de l’expéditeur.
- La présence de règles de boîte de réception qui n’ont pas été créées par l’utilisateur concerné ou l’administrateur. Ces règles peuvent automatiquement transférer les messages électroniques à des adresses inconnues ou déplacez-les vers le dossier **Notes**, **Courrier indésirable**ou **Abonnements RSS** .
- Nom complet de l’utilisateur peut être modifié dans la liste d’adresses globale.
- Boîte aux lettres de l’utilisateur est bloqué à partir de l’envoi de courrier électronique.
- Le dossier éléments envoyés ou éléments supprimés dans Microsoft Outlook ou dans Microsoft Outlook Web App contiennent des messages compte piraté courants, tels que « Je suis bloqué à Londres, envoi d’argent ».
- Modifications du profil inhabituelle, telles que le nom, le numéro de téléphone ou le code postal ont été mis à jour.
- Modifications inhabituel d’informations d’identification, telles que plusieurs modifications de mot de passe sont requises.
- Transfert de messages a été récemment ajouté.
- Une signature inhabituelle a été récemment ajoutée, par exemple une signature bancaires faux ou une signature de la Drug Enforcement il convient.

Si un utilisateur signale les problèmes ci-dessus, vous devez effectuer davantage enquête. L’Office 365 Security & centre de conformité et le portail Azure offrent des outils pour vous aider à étudier l’activité d’un compte d’utilisateur que vous pensez peut être compromis.
- Office 365 unifiée les journaux d’Audit de la sécurité et le centre de conformité - passez en revue toutes les activités du compte suspect en filtrant les résultats pour la date plage allant d’immédiatement avant l’activité suspecte s’est produite à la date actuelle. Ne pas filtrer sur les activités lors de la recherche.
- Utilisez les journaux de connexion dans Azure AD et d’autres rapports risque qui sont disponibles dans le portail Azure AD. Examiner les valeurs de ces colonnes :
    - Passez en revue les adresses IP
    - emplacements de connexion
    - temps de connexion
    - connexion de réussite ou Échec



## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Comment sécuriser et restaurer la fonction de courrier électronique à potentiel compromise compte Office 365 et boîte aux lettres

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Même une fois que vous avez récupéré l’accès à votre compte, l’intrus peut avoir ajouté les entrées de porte permettant l’intrus peut reprendre le contrôle du compte.

Vous devez effectuer toutes les étapes suivantes pour accéder à votre compte rapidement afin de vous assurer que le pirate ne redémarre pas contrôler votre compte. Ces étapes vous aident à supprimer les entrées de porte le pirate peut avoir ajouté à votre compte. Après avoir effectué ces étapes, nous vous recommandons d’exécuter une analyse antivirus pour vous assurer que votre ordinateur n’est pas compromise.

### <a name="step-1-reset-the-users-password"></a>Étape 1 réinitialiser le mot de passe
> [!WARNING]
> N’envoyez pas le nouveau mot de passe pour l’utilisateur concerné par courrier électronique que l’intrus toujours a accès à la boîte aux lettres à ce stade.

1. Suivez le mot de passe réinitialiser un Office 365 entreprise d’une personne autres procédures dans [administrateurs : les mots de passe réinitialiser Office 365 entreprise](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Remarques :**
- Assurez-vous que le mot de passe est fort et qu’il contient des lettres majuscules et minuscules, au moins un chiffre et au moins un caractère spécial. 
- Ne pas réutiliser votre cinq derniers mots de passe. Bien que l’exigence de l’historique du mot de passe vous permet de réutiliser un mot de passe plus récente, vous devez sélectionner quelque chose que l’intrus ne peuvent pas deviner.
- Si votre identité locale est fédérée avec Office 365, vous devez modifier votre mot de passe local, puis vous devez en informer le compromis à votre administrateur.

> [!TIP]
> Il est vivement recommandé d’activer l’authentification multifacteur (MFA) afin d’empêcher les compromis, notamment pour les comptes disposant de privilèges d’administration.  Vous en apprendrez plus [ici](https://support.office.com/en-us/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Étape 2 Supprimez les adresses de transfert d’e-mail suspects
1. Ouvrir le **Centre d’administration Office 365 > utilisateurs actifs**.
2. Recherchez le compte d’utilisateur en question et développez les **Paramètres de messagerie**.
3. Pour le **transfert de courrier électronique**, cliquez sur **Modifier**.
4. Supprimez toute adresse de transfert suspects.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Étape 3 désactiver toutes les règles de boîte de réception suspectes
1. Connectez-vous à la boîte aux lettres de l’utilisateur à l’aide d’Outlook Web App (OWA).
2. Cliquez sur l’icône représentant un engrenage, cliquez sur **messagerie**.
3. Cliquez sur **règles de boîte de réception et adopte** et passez en revue les règles.
4. Désactiver ou supprimer des règles suspects.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Étape 4 débloquer l’utilisateur d’envoyer du courrier
Si la boîte aux lettres compromis soupçonnés d’être utilisé de façon illicite pour envoyer un courrier électronique indésirable, il est probable que la boîte aux lettres a été bloqué à partir de l’envoi du courrier.
1. Pour débloquer une boîte aux lettres à partir de l’envoi du courrier, suivez les procédures de [suppression d’un utilisateur, le domaine ou l’adresse IP d’une liste rouge après l’envoi de courrier indésirable](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Étape 5 facultatif : Bloquer le compte d’utilisateur d’ouverture de session
> [!IMPORTANT]
> Vous pouvez bloquer le compte soupçonnés d’être compromis à partir de signature jusqu'à ce que vous pensez qu’il est recommandé d’activer de nouveau l’accès.

1. Accédez au Centre d’administration Office 365.
2. Dans le centre d’administration Office 365, sélectionnez **les utilisateurs**.
3. Sélectionnez l’employé que vous souhaitez bloquer, puis cliquez sur **Modifier** en regard de **l’état de connexion** dans le volet de l’utilisateur
4. Dans le volet **d’état de connexion** , choisissez **connexion bloqué** , puis sur **Enregistrer**. 
5. Dans le centre d’administration Office 365, dans le volet de navigation inférieur gauche, développez **Centres d’administration** et sélectionnez **Exchange**.
6. Dans le centre d’administration Exchange, accédez à **destinataires > boîtes aux lettres**.
7. Sélectionnez l’utilisateur, dans la page de propriétés utilisateur, sous **Appareils mobiles**, cliquez sur **Désactiver le ActivcSync Exchange** et **Désactiver l’OWA pour périphériques** et répondez **Oui** à deux.
8. Sous **Connectivité de messagerie**, de **désactiver** et de réponse **Oui**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Facultatif étape 6 : Supprimer le compte soupçonnés d’être compromis de tous les groupes de rôles d’administration
> [!NOTE]
> Appartenance au rôle d’administration de groupe peut être restauré une fois que le compte a été sécurisé.

1. Se connecter au centre d’administration Office 365 avec un compte d’administrateur global et ouvrez **Utilisateurs actifs**.
2. Recherchez le soupçonnés d’être compromis compte et vérifier manuellement pour voir s’il existe des rôles d’administration affectés au compte.
3. Ouvrez le **Centre de conformité et de sécurité**.
4. Cliquez sur **autorisations**.
5. Passer en revue les groupes de rôles pour voir si le soupçonnés d’être compromis compte est un membre d’un d'entre eux manuellement.  S’il s’agit : a. Cliquez sur le groupe de rôles, cliquez sur **Modifier le groupe de rôles**.  b. Cliquez sur **Choisissez des membres** et **Modifier** pour supprimer l’utilisateur du groupe de rôles.
6. Ouvrir le **Centre d’administration Exchange**
7. Cliquez sur **autorisations**.
8. Passer en revue les groupes de rôles pour voir si le soupçonnés d’être compromis compte est un membre d’un d'entre eux manuellement. S’il s’agit : a. Cliquez sur le groupe de rôles, cliquez sur **Modifier**.  b. Utilisez la section **membres** pour supprimer l’utilisateur du groupe de rôles.

### <a name="step-7-optional-additional-precautionary-steps"></a>Facultatif étape 7 : Mesures de précaution supplémentaires
1. Assurez-vous que vous vérifiez vos éléments envoyés. Vous devrez informer les personnes de votre liste de contacts que votre compte a été compromis. L’intrus peut ont demandé les money, l’usurpation d’identité, par exemple, que vous ont été bloqués dans un autre pays et nécessaires money ou l’intrus peut envoyer les un virus également détourner leur ordinateur.
2. Aucun autre service utilisés ce compte Exchange en tant que son compte de messagerie de remplacement a été compromise. Tout d’abord, effectuez ces étapes pour votre abonnement à Office 365, puis procédez comme suit pour vos autres comptes.
3. Assurez-vous que vos informations de contact, telles que les numéros de téléphone et des adresses, soient correctes.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sécuriser Office 365 comme une sécurité pro
Votre abonnement Office 365 est fourni avec un ensemble de fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos données et vos utilisateurs puissantes.  Utiliser le [Guide de sécurité Office 365 : principaux des priorités pour les 30 premiers jours, 90 jours et au-delà](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) à mettre en œuvre les meilleures pratiques pour la sécurisation de votre client Office 365 de Microsoft.
- Tâches à accomplir dans les 30 jours.  Ces ont une incidence immédiate et sont faible impact à vos utilisateurs.
- Tâches à accomplir dans 90 jours. Ces prennent un peu plus de temps pour planifier et implémenter mais sensiblement améliorer votre sécurité.
- Au-delà de 90 jours. Ces améliorations créer votre premier travail 90 jours.

## <a name="see-also"></a>Voir aussi :
- [Meilleures pratiques de sécurité pour Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Centre de réclamation délits Internet](http://www.ic3.gov/preventiontips.aspx)
- [Securities and Exchange Commission - fraude « Phishing »](http://www.sec.gov/investor/pubs/phishing.htm)
