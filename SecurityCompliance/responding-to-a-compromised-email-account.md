---
title: Réponse à un compte de messagerie compromis dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.custom: TopSMBIssues
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365
ms.openlocfilehash: 4eaabfc65a6d3118dd995a14a1ce0c8e941a77fc
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156856"
---
# <a name="responding-to-a-compromised-email-account-in-office-365"></a>Réponse à un compte de messagerie compromis dans Office 365

**Résumé** Découvrez comment reconnaître et répondre à un compte de messagerie compromis dans Office 365.

## <a name="what-is-a-compromised-email-account-in-office-365"></a>Qu’est un compte de messagerie compromis dans Office 365 ?
L’accès aux boîtes aux lettres, données et autres services Office 365 est contrôlé en utilisant des informations d’identification, par exemple un nom d’utilisateur et un mot de passe ou code confidentiel. Lorsqu’une personne autre que l’utilisateur initial vole ces informations d’identification, les informations d’identification volées sont considérés comme être compromises. Avec ces informations, le pirate peut se connecter en tant qu’utilisateur d’origine et effectuer des actions illicites.
En utilisant les informations d’identification volées, l’utilisateur malveillant peut accéder à la boîte aux lettres Office 365, aux dossiers SharePoint ou aux fichiers enregistrés dans le OneDrive de l’utilisateur. Souvent, les pirate envoient des messages électroniques en tant qu’utilisateur d’origine à des destinataires internes ou externes à l’organisation. Lorsque l’utilisateur malveillant envoie des données par messages électroniques à des destinataires externes, il s’agit « d’exfiltration de données ».

## <a name="symptoms-of-a-compromised-office-365-email-account"></a>Symptômes indiquant un compte de messagerie Office 365 compromis
Les utilisateurs peuvent noter et rapporter des activités inhabituelles dans leur boîte aux lettres Office 365. Voici quelques symptômes courantes :
- Des « activités douteuses », comme des courriers électroniques manquants ou supprimées.
- D’autres utilisateurs peuvent recevoir des messages électroniques du compte compromis sans que ces courriers correspondant n’apparaissent dans le dossier **Éléments envoyés** de l’expéditeur.
- La présence de règles de boîte de réception qui n’ont pas été créées par l’utilisateur initial ou l’administrateur. Ces règles peuvent automatiquement transférer des messages électroniques à des adresses inconnues ou les déplacer vers les dossiers **Notes**, **Courrier indésirable**, ou **Abonnements RSS**.
- Le nom d’affichage de l’utilisateur peut être modifié dans la liste d’adresses globale.
- La boîte aux lettres de l’utilisateur peut se trouver bloquée et ne peut plus envoyer de messages électroniques.
- Les dossiers Éléments envoyés ou Éléments supprimés dans Microsoft Outlook ou Outlook sur le web (anciennement Outlook Web App) contiennent des messages communs aux comptes piratés, comme par exemple « Je suis bloquée à Londres, envoyez-moi de l’argent. »
- Des modifications inhabituelle du profil, telles que le nom, le numéro de téléphone ou le code postal qui ont été mis à jour.
- Des modifications inhabituelle des informations d’identification, comme par exemple plusieurs requêtes de modification du mot de passe.
- La fonctionnalité de transfert du courrier a été ajoutée récemment.
- Une signature inhabituelle a été récemment ajoutée, par exemple, une signature apocryphe prétendant être une banque ou faisant référence à une ordonnance médicale.

Si un utilisateur rapporte un des symptômes ci-dessus, vous devez lancer un examen approfondi. Le centre de sécurité et conformité de Microsoft 365 et le portail Azure proposent des outils pour vous aider à investiguer les activités d’un compte d’utilisateur qui semble avoir été compromis.
- Journaux d’audit unifiés d’Office 365 dans le centre de sécurité et conformité : Passez en revue toutes les activités du compte suspect en filtrant les résultats pour la plage de dates couvrant depuis immédiatement avant une activité suspecte jusqu’à la date du jour. Ne pas filtrer sur les activités au cours de la recherche.
- Utilisez les journaux de connexion Azure AD et autres rapports de risque qui sont disponibles dans le portail Azure AD. Examinez les valeurs de ces colonnes :
    - Examen des adresses IP
    - emplacements de connexion
    - heure de connexion
    - réussite ou échec des connexions

## <a name="how-to-secure-and-restore-email-function-to-a-suspected-compromised-office-365-account-and-mailbox"></a>Comment sécuriser et restaurer la fonction courrier pour un compte Office 365 supposé compromis et ses boîtes aux lettres 

> [!VIDEO https://videoplayercdn.osi.office.net/hub/?csid=ux-cms-en-us-msoffice&uuid=RE2jvOb&AutoPlayVideo=false]

Même après avoir récupéré l’accès à votre compte, l’utilisateur malveillant peut avoir ajouté des portes d’entrée malveillantes (back-door) qui lui permettront de reprendre le contrôle du compte.

Vous devez effectuer au plus vite toutes les étapes suivantes pour récupérer l’accès à votre compte, pour vous assurer que l’utilisateur malveillant ne reprenne pas le contrôle de votre compte. Ces étapes permettent de supprimer les portes d’entrée malveillantes que le pirate peut avoir ajouté à votre compte. Une fois ces étapes effectuées, nous vous recommandons d’exécuter une analyse antivirus pour vous assurer que votre ordinateur n’est pas compromis.

### <a name="step-1-reset-the-users-password"></a>Étape 1 : Réinitialisez le mot de passe de l’utilisateur.
> [!WARNING]
> Ne pas envoyer de nouveau mot de passe à l’utilisateur initial par courrier électronique, car l’utilisateur malveillant a toujours accès à la boîte aux lettres à ce stade.

1. Suivez les procédures de réinitialisation du mot de passe Office 365 Entreprise pour quelqu’un d’autre décrites dans [Administrateurs : réinitialiser les mots de passe Office 365 Entreprise](https://support.office.com/article/admins-reset-office-365-business-passwords-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c)

**Remarques :**
- Assurez-vous que le mot de passe est robuste et qu’il contient des lettres majuscules et minuscules, au moins un chiffre et au moins un caractère spécial. 
- Ne pas réutiliser un de vos cinq derniers mots de passe. Même si l’exigence de l’historique de mot de passe vous permet de réutiliser un mot de passe plus récent, vous devez en sélectionner un que l’utilisateur malveillant ne peut pas deviner.
- Si votre identité sur site est fédérée avec Office 365, vous devez modifier votre mot de passe sur site, puis vous devez informer votre administrateur de l’attaque.

> [!TIP]
> Il est vivement recommandé d’activer l’authentification multifacteur (MFA) pour éviter les compromissions, en particulier pour les comptes avec des privilèges d’administration.  Vous en apprendrez plus [ici](https://support.office.com/fr-FR/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).

### <a name="step-2-remove-suspicious-email-forwarding-addresses"></a>Étape 2 : Supprimer des adresses de transfert de courrier suspectes
1. Ouvrez le **Centre d’administration Microsoft 365 > Utilisateurs actifs**.
2. Recherchez le compte d’utilisateur en question et développez les **paramètres de courrier**.
3. Pour **transfert des courriers électroniques**, cliquez sur **Modifier**.
4. Supprimer des adresses de transfert suspectes.

### <a name="step-3-disable-any-suspicious-inbox-rules"></a>Étape 3 : Désactiver toutes règles de boîte de réception suspectes
1. Ouvrez la boîte aux lettres d’archivage avec Outlook sur le web.
2. Cliquez sur l’icône en forme d’engrenage, puis **Courrier**.
3. Cliquez sur **Règles de boîte de réception et de rangement** et passer en revue les règles.
4. Désactiver ou supprimer des règles suspectes.

### <a name="step-4-unblock-the-user-from-sending-mail"></a>Étape 4 : Redonner à l’utilisateur l’autorisation d’envoyer des messages électroniques
Si la boîte aux lettres soupçonnée d'avoir été compromise a été utilisée illicitement pour envoyer des pourriels, il est probable que la boîte aux lettres ne peut plus envoyer de messages électroniques.
1. Pour débloquer la boîte aux lettres et permettre l’envoi de messages électroniques, suivez les procédures décrites dans [Suppression d’un utilisateur, du domaine ou adresse IP d’une liste rouge après l’envoi de courrier indésirable](https://docs.microsoft.com/Office365/SecurityCompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email ).

### <a name="step-5-optional-block-the-user-account-from-signing-in"></a>Étape 5 (facultatif) : Empêcher le compte d’utilisateur de se connecter
> [!IMPORTANT]
> Vous pouvez bloquer le compte soupçonné d'avoir été compromis et l’empêcher de se connecter jusqu'à ce qu’à votre avis, il est sûr de réactiver l’accès.

1. Aller au Centre d’administration Microsoft 365.
2. Dans le centre d’administration Microsoft 365, sélectionnez **Utilisateurs**.
3. Sélectionnez l'employé que vous voulez bloquer, puis choisissez **Modifier** en regard d' **État de la connexion** dans le volet de l'utilisateur
4. Dans le volet **État de la connexion**, choisissez **Connexion bloquée**, puis **Enregistrer**. 
5. Dans le Centre d'administration, dans le volet de navigation en bas à gauche, développez **Centres d'administration**, puis sélectionnez **Exchange**.
6. Dans le Centre d’administration Exchange, accédez à **Destinataires > Boîtes aux lettres**.
7. Sélectionnez l'utilisateur. Dans la page des propriétés de l'utilisateur, sous **Périphériques mobiles**, cliquez sur **Désactiver ActiveSync Exchange** et sur **Désactiver OWA pour les appareils**, puis répondez **oui** à chaque fois.
8. Sous **Connectivité de courrier**, **Désactiver**, puis répondez **oui**. 

### <a name="step-6-optional-remove-the-suspected-compromised-account-from-all-administrative-role-groups"></a>Étape 6 (facultatif) : Supprimer le compte soupçonné d'avoir été compromis de tous les groupes de rôles d’administration
> [!NOTE]
> L’appartenance au groupe de rôles d’administration peut être restaurée une fois que le compte a été sécurisé.

1. Connectez-vous au Centre d’administration Microsoft 365 avec votre compte d’administrateur général et ouvrez **Utilisateurs actifs**.
2. Trouvez le compte soupçonné d'avoir été compromis et vérifiez manuellement si des rôles d’administration sont attribués au compte.
3. Ouvrir le **Centre de sécurité et conformité**.
4. Cliquez sur **Autorisations**.
5. Passer en revue manuellement les groupes de rôles pour déterminer si le compte soupçonné d'avoir été compromis est membre de l’un des groupes.  Si c’est le cas : a. Cliquez sur le groupe de rôles, puis sur **Modifier un groupe de rôles**.
    b. Cliquez sur **Choisir les membres** et **Modifier** pour supprimer l’utilisateur du groupe de rôles.
6. Ouvrez le **Centre d’administration Exchange**
7. Cliquez sur **Autorisations**.
8. Passer en revue manuellement les groupes de rôles pour déterminer si le compte soupçonné d'avoir été compromis est membre de l’un des groupes. Si c’est le cas : a. Cliquez sur le groupe de rôles, puis sur **Modifier**.
    b. Utilisez la section **Membres** pour supprimer l’utilisateur du groupe de rôles.

### <a name="step-7-optional-additional-precautionary-steps"></a>Étape 7 (facultatif) : Mesures de précaution supplémentaires
1. Vérifiez vos éléments envoyés. Vous devriez peut-être informer les membres de votre liste de contacts que votre compte a été compromis. L’utilisateur malveillant les a peut-être contacté pour demander de l’argent ou tenter d’usurper leur identité, par exemple, a déclaré que vous étiez bloqué dans un pays étranger et que vous aviez besoin d'argent, ou leur a peut-être envoyé un virus pour pirater leur ordinateur.
2. Tout autre service qui utilise ce compte Exchange en tant que compte de courrier en alternative a pu être compromis. Tout d’abord, effectuez ces étapes pour votre abonnement Office 365, puis effectuez ces étapes pour vos autres comptes.
3. Assurez-vous que vos informations de contact, tels que les numéros de téléphone et adresses, sont correctes.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sécuriser Office 365 comme un pro de la cyber-sécurité
Votre abonnement Office 365 inclut un ensemble puissant de fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos données et vos utilisateurs.  Utilisez la [Feuille de route pour sécuriser Office 365 : principales priorités pour les 30 premiers jours, 90 premiers jours et au-delà](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352), pour implémenter les meilleures pratiques recommandées par Microsoft pour sécuriser votre client Office 365.
- Tâches à effectuer lors des 30 premiers jours.  Elle ont un effet immédiat et n’ont qu’un faible impact négatif sur vos utilisateurs.
- Tâches à accomplir dans les 90 premiers jours. Ces tâches prennent un peu plus de temps à planifier et à implémenter, mais augmentent considérablement votre sécurité.
- Au-delà de 90 jours. Ces améliorations sont à mettre en place pendant les 90 premiers jours.

## <a name="see-also"></a>Voir aussi :
- [Meilleures pratiques de sécurité pour Office 365](https://support.office.com/article/Security-best-practices-for-Office-365-9295e396-e53d-49b9-ae9b-0b5828cdedc3)
- [Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Office 365](detect-and-remediate-outlook-rules-forms-attack.md)
- [Centre de plaintes contre la criminalité sur Internet ](http://www.ic3.gov/preventiontips.aspx)
- [Securities and Exchange Commission (SEC) : fraude à « l’hameçonnage » (phishing)](http://www.sec.gov/investor/pubs/phishing.htm)
- Pour signaler un courrier électronique indésirable directement à Microsoft et à votre administrateur [Utiliser le complément Message de Rapport](https://support.office.com/fr-FR/article/Use-the-Report-Message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
