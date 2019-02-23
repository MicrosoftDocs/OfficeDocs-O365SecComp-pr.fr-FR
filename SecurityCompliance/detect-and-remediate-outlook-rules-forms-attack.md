---
title: Détecter et résoudre les attaques d'injections de formulaires personnalisés et de règles Outlook dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Découvrez comment reconnaître et corriger les attaques d'injections de formulaires personnalisés et de règles Outlook dans Office 365
ms.openlocfilehash: 214be3e8492c2896d2a4010c30768e41bc149078
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215234"
---
# <a name="detect-and-remediate-outlook-rules-and-custom-forms-injections-attacks-in-office-365"></a>Détecter et résoudre les attaques par injections sur les règles d’Outlook et les formulaires personnalisés dans Office 365

**Résumé** Découvrez comment reconnaître et corriger les attaques d'injections de formulaires personnalisés et de règles Outlook dans Office 365.

## <a name="what-is-the-outlook-rules-and-custom-forms-injection-attack"></a>Qu'est-ce que les règles Outlook et les attaques par injection de formulaires personnalisés?
Une fois qu'un agresseur a enfreint un compte de votre location et que vous vous trouvez dans, il y a un moyen d'essayer de revenir sur ou de revenir une fois qu'il a été découvert et supprimé. Il s'agit de l'établissement d'un mécanisme de persistance. Il existe deux façons de le faire en exploitant les règles Outlook ou en injectant des formulaires personnalisés dans Outlook. Dans les deux cas, la règle ou le formulaire est synchronisé à partir du service Cloud vers le client de bureau, de sorte qu'un format complet et une réinstallation du logiciel client n'éliminent pas le mécanisme d'injection. Cela est dû au fait que lorsque le logiciel client Outlook se reconnecte à la boîte aux lettres dans le Cloud, il télécharge de nouveau les règles et les formulaires à partir du Cloud. Une fois que les règles et les formulaires sont en place, l'agresseur les utilise pour exécuter du code distant ou personnalisé, généralement pour installer des programmes malveillants sur l'ordinateur local. Le programme malveillant revole ensuite les informations d'identification ou effectue une autre activité illicite. La bonne nouvelle est que si vous maintenez vos clients patchés vers la dernière version, vous n'êtes pas vulnérable à la menace comme les valeurs par défaut du client Outlook bloquent les deux mécanismes. 

Les attaques suivent généralement ces modèles:

Exploitation des règles
1. L'agresseur vole le nom d'utilisateur et le mot de passe de l'un de vos utilisateurs.
2. L'agresseur se connecte ensuite à la boîte aux lettres Exchange de ces utilisateurs. La boîte aux lettres peut être dans Exchange Online ou dans Exchange en local.
3. L'agresseur crée ensuite une règle de transfert dans la boîte aux lettres qui est déclenchée lorsque la boîte aux lettres reçoit un e-mail correspondant aux critères de la règle. Les critères de règle et le contenu du déclencheur de messagerie sont conçus pour les deux.
4. L'agresseur envoie le message du déclencheur à l'utilisateur qui utilise sa boîte aux lettres normalement.
5. Lorsque le message électronique est reçu, la règle est déclenchée. L'action de la règle consiste généralement à lancer une application sur un serveur distant (WebDAV).
6. L'application installe généralement des programmes malveillants, tels que [PowerShell Empire](https://www.powershellempire.com/), localement sur l'ordinateur de l'utilisateur.
7. Le programme malveillant permet à l'agresseur de revoler le nom d'utilisateur et le mot de passe de l'utilisateur ou d'autres informations d'identification à partir de l'ordinateur local et d'effectuer d'autres activités malveillantes.

Exploit des formulaires
1. L'agresseur vole le nom d'utilisateur et le mot de passe de l'un de vos utilisateurs.
2. L'agresseur se connecte ensuite à la boîte aux lettres Exchange de ces utilisateurs. La boîte aux lettres peut être dans Exchange Online ou dans Exchange en local.
3. L'agresseur crée ensuite un modèle de formulaire de messagerie personnalisé et l'insère dans la boîte aux lettres de l'utilisateur.  Le formulaire personnalisé est déclenché lorsque la boîte aux lettres reçoit un message électronique qui exige que la boîte aux lettres charge le formulaire personnalisé. Le formulaire personnalisé et le format des courriers électroniques sont conçus pour les deux.
4. L'agresseur envoie le message de déclenchement à l'utilisateur qui utilise normalement sa boîte aux lettres.
5. Lorsque le message électronique est reçu, le formulaire est chargé. Le formulaire lance une application sur un serveur distant (WebDAV).
6. L'application installe généralement des programmes malveillants, tels que [PowerShell Empire](https://www.powershellempire.com/), localement sur l'ordinateur de l'utilisateur.
7. Le programme malveillant permet à l'agresseur de revoler le nom d'utilisateur et le mot de passe de l'utilisateur ou d'autres informations d'identification à partir de l'ordinateur local et d'effectuer d'autres activités malveillantes.


## <a name="what-a-rules-and-custom-forms-injection-attack-might-look-like-office-365"></a>Quelles sont les règles et les attaques par injection de formulaires personnalisés qui peuvent ressembler à Office 365?

Il est peu probable que ces mécanismes de persistance soient remarqués par vos utilisateurs et, dans certains cas, ils ne soient pas visibles.  Cet article vous indique comment rechercher les sept signes (indicateurs de compromis) ci-dessous. Si vous trouvez l'un de ces éléments, vous devez prendre des mesures de correction.

- Indicateurs des règles compromis
    - L'action de la règle consiste à démarrer une application.
    - La règle fait référence à un EXE, un ZIP ou une URL.
    - Sur l'ordinateur local, recherchez les démarrages de nouveau processus issus du PID Outlook.
- Indicateurs des formulaires personnalisés compromis 
    - Formulaire personnalisé présent enregistré comme sa propre classe de message.
    - La classe de message contient du code exécutable.
    - Généralement stocké dans les dossiers de la boîte de réception ou de la bibliothèque des formulaires personnels.
    - Le formulaire est appelé IPM. Note. [nom personnalisé].

## <a name="steps-for-finding-signs-of-this-attack-and-confirming-it"></a>Étapes permettant de trouver des signes de cette attaque et de la confirmer
Vous pouvez utiliser l'une ou l'autre de ces deux méthodes pour confirmer l'attaque.
- Examinez manuellement les règles et les formulaires de chaque boîte aux lettres à l'aide du client Outlook.  Cette méthode est exhaustive, mais vous pouvez vérifier uniquement l'utilisateur de boîte aux lettres à la fois, ce qui peut prendre beaucoup de temps si vous avez un grand nombre d'utilisateurs à vérifier.  Cela peut également entraîner une violation de l'ordinateur à partir duquel vous exécutez la vérification.
- Utilisez le script PowerShell [Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) pour vider automatiquement toutes les règles de transfert de courrier et les formulaires personnalisés pour tous les utilisateurs de votre client. Il s'agit de la méthode la plus rapide et la plus sécurisée avec la charge minimale.


### <a name="confirm-the-rules-attack-using-the-outlook-client"></a>Confirmer l'attaque des règles à l'aide du client Outlook
1. Ouvrez le client Outlook utilisateurs en tant qu'utilisateur.  L'utilisateur peut avoir besoin de votre aide pour examiner les règles de sa boîte aux lettres.
2. RePortez-vous à l'article [gérer les messages électroniques à l'aide des règles](https://support.office.com/article/manage-email-messages-by-using-rules-c24f5dea-9465-4df4-ad17-a50704d66c59#ID0EAABAAA=2010) pour les procédures relatives à l'ouverture de l'interface des règles dans les versions 2007, 2010 ou 2013 d'Outlook.
3. Recherchez les règles que l'utilisateur n'a pas créées, ou toute règle ou règle inattendue avec des noms suspects.
4. Recherchez dans la description de règle les actions de règle qui commencent et application ou font référence à un. EXE,. Fichier ZIP ou pour lancer une URL.
5. Recherchez les nouveaux processus qui commencent à utiliser l'ID de processus Outlook.  RePortez-vous à [Rechercher l'ID de processus](https://docs.microsoft.com/windows-hardware/drivers/debugger/finding-the-process-id).

### <a name="steps-to-confirm-the-forms-attack-using-the-outlook-client"></a>Étapes pour confirmer l'attaque de formulaires à l'aide du client Outlook
1. Ouvrez le client Outlook utilisateur en tant qu'utilisateur.
2. Suivez les étapes décrites dans, [afficher l'onglet Développeur](https://support.office.com/article/show-the-developer-tab-e1192344-5e56-4d45-931b-e5fd9bea2d45) pour la version des utilisateurs d'Outlook.
3. Ouvrez l'onglet Développeur maintenant visible dans Outlook, puis cliquez sur **créer un formulaire**.
4. Sélectionnez la **boîte de réception** dans la liste **regarder dans** . Recherchez les formulaires personnalisés.  Les formulaires personnalisés sont assez rares pour que si vous avez du tout des formulaires personnalisés, l'aspect est plus approfondi.
5. Examinez les formulaires personnalisés, en particulier ceux marqués comme masqués.
6. Ouvrez tous les formulaires personnalisés et, dans le groupe **formulaire** , cliquez sur **afficher le code** pour afficher les éléments exécutés lors du chargement du formulaire.

### <a name="steps-to-confirm-the-rules-and-forms-attack-using-powershell"></a>Étapes à suivre pour vérifier les règles et les attaques de formulaires à l'aide de PowerShell
Le moyen le plus simple de vérifier une attaque de règles ou de formulaires personnalisés consiste à exécuter le script PowerShell [Get-AllTenantRulesAndForms. ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/Get-AllTenantRulesAndForms.ps1) .  Ce script se connecte à chaque boîte aux lettres de votre client et transfère toutes les règles et les formulaires dans deux fichiers. csv.

#### <a name="pre-requisites"></a>Conditions préalables
Vous devez disposer des droits d'administrateur général pour exécuter le script, car le script se connecte à chaque boîte aux lettres dans le client pour lire les règles et les formulaires.

1. Connectez-vous à l'ordinateur à partir duquel vous allez exécuter le script avec des droits d'administrateur local.
2. Téléchargez ou copiez le script Get-AllTenantRulesAndForms. ps1 depuis GitHub vers un dossier à partir duquel vous allez l'exécuter.  Le script crée deux fichiers de date marqués dans ce dossier, MailboxFormsExport-yyyy-mm-dd. csv et MailboxRulesExport-yyyy-mm-dd. csv.
3. Ouvrez une instance PowerShell en tant qu'administrateur et ouvrez le dossier dans lequel vous avez enregistré le script.
4. Exécutez cette ligne de commande PowerShell comme `.\Get-AllTenantRulesAndForms.ps1`suit .\Get-AllTenantRulesAndForms.ps1

#### <a name="interpreting-the-output"></a>Interprétation de la sortie

MailboxRulesExport-*yyyy-mm-dd*. csv – examinez les règles (une par ligne) pour les conditions d'action qui incluent des applications ou des exécutables.
- ActionType (colonne A): Si vous voyez la valeur «ID_ACTION_CUSTOM», la règle est probablement malveillante.
- IsPotentiallyMalicious (colonne D): si cette valeur est «TRUE», la règle est probablement malveillante.
- ActionCommand (colonne G): si cette énumération répertorie une application ou un fichier avec une extension. exe,. zip ou une entrée qui fait référence à une URL qui n'est pas censée exister, la règle est probablement malveillante.

MailboxFormsExport-*yyyy-mm-dd*. csv – en général, l'utilisation de formulaires personnalisés est très rare.  Si vous en trouvez dans ce classeur, vous ouvrez la boîte aux lettres de cet utilisateur et examinez le formulaire lui-même.  Si votre organisation ne l'a pas placée intentionnellement, elle est probablement malveillante.



## <a name="how-to-stop-and-remediate-the-outlook-rules-and-forms-attack"></a>Comment arrêter et corriger les attaques de formulaires et de formulaires Outlook
Si vous trouvez des preuves de l'une de ces attaques, la correction est simple, supprimez simplement la règle ou le formulaire de la boîte aux lettres. Vous pouvez effectuer cette opération avec le client Outlook ou à l'aide de PowerShell à distance pour supprimer des règles.

### <a name="using-outlook"></a>Utilisation d'Outlook
1. Identifier tous les appareils utilisés par l'utilisateur avec Outlook.  Ils devront tous être nettoyés du programme malveillant potentiel.  Ne pas autoriser l'utilisateur à se connecter et à utiliser le courrier électronique jusqu'à ce que tous les appareils soient nettoyés.
2. Suivez les étapes de la procédure [supprimer une règle](https://support.office.com/article/Delete-a-rule-2F0E7139-F696-4422-8498-44846DB9067F) pour chaque appareil.
3. Si vous n'êtes pas sûr de la présence d'autres programmes malveillants, vous pouvez formater et réinstaller tous les logiciels sur l'appareil.  Pour les appareils mobiles, vous pouvez suivre les étapes des constructeurs pour réinitialiser l'appareil à l'image installée en usine.
4. Installez les versions les plus à jour d'Outlook.  N'oubliez pas que la version actuelle d'Outlook bloque les deux types de cette attaque par défaut.
5. Une fois que toutes les copies hors connexion de la boîte aux lettres ont été supprimées, réinitialisez le mot de passe de l'utilisateur (utilisez une qualité élevée) et suivez les étapes décrites dans [setup multi-Factor Authentication for Office 365 Users](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6) si MFA n'a pas encore été activé. Cela permet de s'assurer que les informations d'identification de l'utilisateur ne sont pas exposées par d'autres moyens (par exemple, le hameçonnage ou la réutilisation du mot de passe).

### <a name="using-powershell"></a>Utilisation de PowerShell
Il existe deux cmdlets PowerShell à distance que vous pouvez utiliser pour supprimer ou désactiver les règles dangereuses. Suivez simplement les étapes.
 
Étapes pour les boîtes aux lettres qui se trouvent sur un serveur Exchange

1. Connectez-vous au serveur Exchange à l'aide de PowerShell à distance. Suivez les étapes de la procédure [connexion à des serveurs Exchange à l'aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/exchange-server/connect-to-exchange-servers-using-remote-powershell?view=exchange-ps).
2. Si vous souhaitez supprimer entièrement une seule règle, plusieurs règles ou toutes les règles d'une boîte aux lettres, utilisez la [cmdlet Remove-Inbox Rule ](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps): utilisez cette commande pour supprimer complètement une, plusieurs ou toutes les règles de la boîte aux lettres.
3. Si vous souhaitez conserver la règle et son contenu à des fins d'aide, utilisez la [cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

Étapes pour les boîtes aux lettres dans Exchange Online
1. Suivez les étapes de la procédure [connexion à Exchange Online à l'aide de PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
2.  Si vous souhaitez supprimer entièrement une seule règle, plusieurs règles ou toutes les règles d'une boîte aux lettres, utilisez la [cmdlet Remove-Inbox Rule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Remove-InboxRule?view=exchange-ps).
3.  Si vous souhaitez conserver la règle et son contenu à des fins d'aide, utilisez la [cmdlet Disable-InboxRule](https://technet.microsoft.com/en-us/library/dd298120(v=exchg.160).aspx). 

## <a name="how-to-minimize-future-attacks"></a>Comment limiter les attaques futures

### <a name="first-protect-your-accounts"></a>Tout d'abord: Protégez vos comptes

Les attaques de formulaires et de règles sont utilisées uniquement par un agresseur après avoir volé ou enfreint un des comptes de vos utilisateurs. Par conséquent, la première étape pour empêcher l'utilisation de ces exploits auprès de votre organisation consiste à protéger activement vos comptes d'utilisateur.  Les attaques par hameçonnage ou par [pulvérisation de mot de passe](http://www.dabcc.com/microsoft-defending-against-password-spray-attacks/) constituent certaines des méthodes de violation des comptes les plus courantes.



La meilleure façon de protéger vos comptes d'utilisateur, et en particulier vos comptes administrateur, est de [configurer l'authentification multifacteur pour les utilisateurs d'Office 365](https://support.office.com/article/set-up-multi-factor-authentication-for-office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).  Vous devez également:
<ol>
    <li>SurVeillez le mode d' <a href="https://docs.microsoft.com/azure/active-directory/active-directory-view-access-usage-reports">accès et d'utilisation</a>de vos comptes d'utilisateur. Vous n'êtes pas autorisé à empêcher la violation initiale, mais vous réduisez la durée et l'impact de la violation en la détectant plus tôt. Vous pouvez utiliser les <a href="https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475">stratégies de sécurité d'application Cloud d'Office 365</a> pour surveiller les comptes et alerter les activités inhabituelles.<ol type="a">
            <li><b>Plusieurs tentatives de connexion ayant échoué</b> Cette stratégie Profile votre environnement et déclenche des alertes lorsque les utilisateurs effectuent plusieurs activités de connexion ayant échoué au cours d'une session unique en ce qui concerne la planification d'expérience utilisateur, ce qui peut indiquer une tentative de violation.</li>
            <li><b>Déplacement impossible</b> - Cette stratégie Profile votre environnement et déclenche des alertes lorsque des activités sont détectées à partir du même utilisateur dans des emplacements différents pendant une période de temps qui est plus courte que le temps de trajet prévu entre les deux emplacements. Cela peut indiquer qu'un autre utilisateur utilise les mêmes informations d'identification. La détection de ce comportement anormal nécessite une période d'apprentissage initiale de sept jours pendant laquelle il apprend le modèle d'activité d'un nouvel utilisateur.</li>
            <li><b>Activité usurpée inhabituelle (par utilisateur)</b> - Cette stratégie Profile votre environnement et déclenche des alertes lorsque les utilisateurs effectuent plusieurs activités empruntées dans une session unique en ce qui concerne la base de référence apprise, ce qui peut indiquer une tentative de violation.</li>
        </ol>
    </li>
    <li>Utilisez un outil tel que le <a href="https://securescore.office.com/">score de sécurité Office 365</a> pour gérer les configurations et les comportements de sécurité des comptes. 
    </li>
</ol> 

### <a name="second-keep-your-outlook-clients-current"></a>Seconde: conserver vos clients Outlook à jour
Les versions entièrement mises à jour et corrigées d'Outlook 2013 et 2016 désactivent par défaut l'action «démarrer l'application».  Ainsi, même si un agresseur enfreint le compte, les actions de la règle et du formulaire sont bloquées.  Vous pouvez installer les mises à jour les plus récentes et les correctifs de sécurité en suivant les étapes décrites dans [install Office updates](https://support.office.com/article/Install-Office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5).

Voici les versions de correctifs pour vos clients Outlook 2013 et 2016:
- Outlook 2013:15.0.4937.1000 ou version ultérieure
- Outlook 2016:16.0.4534.1001 ou version ultérieure

Pour plus d'informations sur les correctifs de sécurité individuels, voir:

- [Correctif de sécurité Outlook 2013](https://support.microsoft.com/en-us/help/3191938) 
- [Correctif de sécurité Outlook 2016](https://support.microsoft.com/en-us/help/3191883)

### <a name="third-monitor-your-outlook-clients"></a>Troisième: surveiller vos clients Outlook
Notez que même avec les correctifs et mises à jour installés, il est possible pour un agresseur de modifier la configuration de l'ordinateur local pour réactiver le comportement «démarrer l'application». Vous pouvez utiliser la [gestion de stratégie de groupe avancée](https://docs.microsoft.com/microsoft-desktop-optimization-pack/agpm/) pour surveiller et appliquer des stratégies d'ordinateur local sur vos clients.  
Vous pouvez voir si «démarrer l'application» a été réactivé via une substitution dans le registre à l'aide des informations de la rubrique [How to View the System Registry by using 64-bit versions of Windows](https://support.microsoft.com/en-us/help/305097/how-to-view-the-system-registry-by-using-64-bit-versions-of-windows).  Vérifiez les sous-clés suivantes: 

- Outlook 2016: HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Security\
- Outlook 2013: HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Security\

Recherchez la clé EnableUnsafeClientMailRules. S'il est présent et qu'il est défini sur 1, le correctif de sécurité Outlook a été remplacé et l'ordinateur est vulnérable à l'attaque de formulaire/de règles. Si la valeur est égale à 0, l'action «démarrer l'application» est désactivée.  Si la version mise à jour et corrigée d'Outlook est installée et que cette clé de Registre n'est pas présente, un système n'est pas vulnérable à ces attaques.

Les clients disposant d'installations Exchange locales doivent envisager de bloquer les anciennes versions d'Outlook qui n'ont pas de correctifs disponibles. Pour plus d'informations sur ce processus, voir l'article [configurer le blocage du client Outlook](https://technet.microsoft.com/en-us/library/dd335207(v=exchg.150).aspx).

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sécuriser Office 365 comme un Cybersecurity Pro
Votre abonnement Office 365 est fourni avec un ensemble de fonctionnalités de sécurité puissantes que vous pouvez utiliser pour protéger vos données et vos utilisateurs.  Utilisez la feuille de [route de sécurité Office 365: les principales priorités pour les 30 jours, 90 jours et au-delà](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) pour implémenter les meilleures pratiques recommandées par Microsoft pour la sécurisation de votre client Office 365.
- Tâches à accomplir dans les 30 premiers jours.  Ceux-ci ont des effets immédiats et ont un faible impact sur vos utilisateurs.
- Tâches à effectuer dans les 90 jours. La planification et l'implémentation de ces deux éléments prennent un peu plus de temps, mais améliorent grandement votre position de sécurité.
- Au-delà de 90 jours. Ces améliorations s'appuient sur vos premiers 90 jours de travail.

## <a name="see-also"></a>Voir aussi:
- [Règles Outlook malveillantes](https://silentbreaksecurity.com/malicious-outlook-rules/) par SilentBreak Security post à propos des règles le vecteur fournit une analyse détaillée de la façon dont les règles Outlook sont définies. 
- [MAPI sur http et Mailrule Pwnage](https://sensepost.com/blog/2016/mapi-over-http-and-mailrule-pwnage/) sur le blog Sensepost sur Mailrule Pwnage aborde un outil appelé Ruler qui vous permet d'exploiter les boîtes aux lettres par le biais de règles Outlook.
- [Formulaires et coques Outlook](https://sensepost.com/blog/2017/outlook-forms-and-shells/) sur le blog Sensepost sur le vecteur de menace de formulaires. 
- [CodeBase de règle](https://github.com/sensepost/ruler)
- [Indicateurs de règle compromis](https://github.com/sensepost/notruler/blob/master/iocs.md)