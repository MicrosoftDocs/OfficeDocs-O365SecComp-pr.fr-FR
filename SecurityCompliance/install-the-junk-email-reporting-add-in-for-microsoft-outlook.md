---
title: Installation du complément de création de rapports de courrier indésirable pour Microsoft Outlook
ms.author: MSFTTracyP
author: tracyp
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8dcc752f-e22e-44ce-a104-4cc4d7e439f3
ms.collection:
- M365-security-compliance
description: Dans cette articleSupported LanguagesInstall le dossier Junk Email Reporting Add-ununinstall the Junk Email Reporting Add-inFor more information
ms.openlocfilehash: c9211cd71fd82af2b9fc0533435ff27a82cd47be
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152556"
---
# <a name="install-the-junk-email-reporting-add-in-for-microsoft-outlook"></a>Installation du complément de création de rapports de courrier indésirable pour Microsoft Outlook
  
Cette rubrique explique comment installer (et désinstaller) le complément Microsoft de création de rapports de courrier indésirable pour Outlook sur des ordinateurs clients au sein de votre organisation. La version actuelle du complément (janvier 2016) inclut la prise en charge pour Outlook 2016, Outlook 2013, Outlook 2010 et Outlook 2007. 
  
Le complément (pour toutes les langues prises en charge) vous permet de signaler du courrier indésirable directement à partir du ruban Outlook. La version anglaise du complément inclut des options supplémentaires pour signaler des problèmes liés à la messagerie à Microsoft directement à partir du ruban :
  
-  Signaler les messages électroniques de hameçonnage que vous recevez 
    
- Signalez les messages électroniques identifiés à tort comme du courrier indésirable.
    
## <a name="supported-languages"></a>Langues prises en charge
<a name="sectionSection0"> </a>

Le complément Junk Email Reporting prend en charge les langues suivantes : 
  
- Chinois simplifié
    
- Chinois traditionnel
    
- Néerlandais
    
- Anglais
    
- Français
    
- Allemand
    
- Italien
    
- Japonais
    
- Coréen
    
- Portugais
    
- Portugais (Brésil)
    
- Espagnol
    
## <a name="install-the-junk-email-reporting-add-in"></a>Installation du complément Junk Email Reporting
<a name="sectionSection1"> </a>

Vous pouvez installer le complément de création de rapports de courrier indésirable de deux façons :
  
- En exécutant le package Windows Installer comme vous le feriez avec n'importe quel autre fichier .msi. Lorsque vous installez le complément, une interface GUI s'affiche et vous guide au fil des écrans d'installation. Pour plus d'informations, consultez la rubrique relative à [Installation du complément de création de rapports de courrier indésirable à l'aide de l'Assistant Installation](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard).
    
- En exécutant une installation sans assistance, c'est-à-dire sans interface utilisateur d'installation. Au lieu d'utiliser cette dernière, vous spécifiez des options de ligne de commande qui exécutent un script d'installation. Lorsque vous installez le complément, vous disposez d'options de configuration supplémentaires qui sont indisponibles dans l'interface GUI. Pour plus d'informations, consultez la rubrique relative à [Installation du complément de création de rapports de courrier indésirable en mode sans assistance](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode).
    
### <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer

L'installation du complément de création de rapports de courrier indésirable Microsoft pour Microsoft Outlook requiert la configuration suivante :
  
- L'un des systèmes d'exploitation suivants : Windows 10, Windows 8.1, Windows 8, Windows 7 Service Pack 1, Windows 10 Server, Windows Server 2012 R2, Windows Server 2012 ou Windows Server 2008 R2
    
- Outlook 2016, Outlook 2013, Outlook 2010 ou Outlook 2007 (Service Pack 2 ou supérieur)
    
- Assemblys PIA de Microsoft Office : 
    
  - Pour télécharger les assemblies PIA de Microsoft Office 2010 ou version ultérieure, accédez au [entre de téléchargement Microsoft](https://go.microsoft.com/fwlink/?LinkID=166026).
    
  - Pour télécharger les assemblies PIA de Microsoft Office 2007, accédez au [centre de téléchargement Microsoft](https://go.microsoft.com/fwlink/?LinkId=72637).
    
- Microsoft .NET Framework [Version 2.0](https://go.microsoft.com/fwlink/?LinkID=208706).
    
> [!NOTE]
> Vous devez disposer de droits d'administrateur sur l'ordinateur sur lequel vous installez le complément. 
  
### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a>Installation du complément de création de rapports de courrier indésirable à l'aide de l'Assistant Installation
<a name="BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard"> </a>

1. Sur votre ordinateur, fermez Outlook.
    
2. Accédez à la page du centre de téléchargement Microsoft pour le complément Outil de signalement de courrier indésirable Microsoft pour Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkID=147248](https://go.microsoft.com/fwlink/?LinkID=147248), puis téléchargez le fichier .msi. 
    
3. Double-cliquez sur le fichier .msi. 
    
4. Dans la page **Bienvenue à la configuration du complément Microsoft Junk Email Reporting**, cliquez sur **Suivant**. 
    
5. Lisez le contrat de licence, puis, si vous consentez aux conditions d'installation, cliquez sur **J'accepte les termes du contrat de licence** (obligatoire pour continuer l'installation). Cliquez sur **Suivant** pour continuer. 
    
6. Une fois l'exécution de l'Assistant terminée, cliquez sur **Terminer**. 
    
7. Lancez Outlook.
    
8. Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**. 
    
9. Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable. 
    
### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a>Installation du complément de création de rapports de courrier indésirable en mode sans assistance
<a name="BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode"> </a>

1. Sur votre ordinateur, fermez Outlook.
    
2. Ouvrez une invite de commandes.
    
3. Pour effectuer une installation simple du complément, sans paramètre facultatif, spécifiez ce qui suit :
    
  - Ordinateurs exécutant x86 Outlook :  `msiexec /qn /i JunkReportingAdd-in.x86-en.msi`
    
  - Ordinateurs exécutant x64 Outlook :  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`
    
    Vous pouvez également spécifier les paramètres facultatifs MaxMessageSelection et BccEmailAddress :
    
  - MaxMessageSelection Permet aux administrateurs de définir le nombre maximal de messages que les utilisateurs peuvent sélectionner pour soumission en un seul clic. La plage s'étend de 1 à 50 messages, et la valeur par défaut est de 10 messages.
    
    Exemple : Si vous voulez définir le nombre maximal de messages qu'un utilisateur peut sélectionner pour soumission en un seul clic sur 16, utilisez l'option suivante dans la commande d'installation :  `MaxMessageSelection=16`
    
  - BccEmailAddress Permet aux administrateurs de configurer une boîte aux lettres pour recevoir une copie de toutes les soumissions de leurs utilisateurs en définissant une adresse de messagerie Cci. Après configuration de la boîte aux lettres, une copie des tous les messages électroniques soumis est envoyée à l'adresse BccEmailAddress. Autrement, le paramètre par défaut est « pas d'adresse de messagerie Cci ».
    
    Exemple : Si vous voulez utiliser junkReports@contoso.com comme adresse de messagerie Cci pour toutes les soumissions, utilisez la commande suivante :  `BccEmailAddress="junkReports@contoso.com"`
    
    > [!NOTE]
    > Vous pouvez entrer plusieurs adresses de messagerie Cci en les séparant par des points-virgules. Exemple :  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`
  
    Pour ajouter ces deux paramètres facultatifs sur la base des exemples ci-dessus, sur un ordinateur exécutant x86 Outlook, vous devez spécifier ce qui suit : 
    
  ```
  msiexec /qn /i JunkReportingAdd-in.x86-en.msi. MaxMessageSelection=16 BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"
  ```

4. Une fois l'installation terminée, lancez Outlook.
    
5. Consultez le bouton **Courrier indésirable** sur votre ruban Outlook. Vous pouvez à présent signaler des messages de courrier indésirable à Microsoft en les sélectionnant dans votre boîte de réception, puis en cliquant sur le bouton permettant de **signaler le courrier indésirable**. 
    
6. Cliquez sur la flèche vers le bas en regard du bouton **Courrier indésirable** pour plus d'options, telles que le **signalement en tant que hameçonnage** si vous souhaitez signaler des messages électroniques d'hameçonnage à Microsoft. Dans votre dossier de courrier indésirable, vous pouvez également sélectionner l'option de **signalement en tant que courrier non indésirable** si un message électronique a été identifié à tort comme courrier indésirable. 
    
## <a name="uninstall-the-junk-email-reporting-add-in"></a>Désinstallation du complément Junk Email Reporting
<a name="sectionSection2"> </a>

Utilisez l'une des options suivantes pour désinstaller le complément de création de rapports de courrier indésirable :
  
- Supprimez le complément à l'aide du Panneau de configuration Windows. Pour plus d'informations, consultez la rubrique relative à la [Désinstallation du complément Junk Email Reporting à partir du Panneau de configuration](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel).
    
- Exécutez le package Windows Installer, puis sélectionnez l'option de désinstallation. Pour plus d'informations, consultez la rubrique relative à la [Désinstallation du complément Junk Email Reporting en exécutant le package Windows Installer](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage).
    
- Exécutez une installation à l'aide de l'option de désinstallation. Pour plus d'informations, consultez la rubrique relative à la [Désinstallation du complément Junk Email Reporting en mode sans assistance](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#MK_UninstalltheJunkEmailReportingAdd-ininSilentMode).
    
> [!NOTE]
> Vous devez disposer de droits d'administrateur sur l'ordinateur sur lequel vous désinstallez le complément. 
  
### <a name="uninstall-the-junk-email-reporting-add-in-from-control-panel"></a>Désinstallation du complément Junk Email Reporting à partir du Panneau de configuration
<a name="BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel"> </a>

1. Sur votre ordinateur, fermez Outlook.
    
2. Dans le menu Démarrer de votre ordinateur, sélectionnez **Panneau de configuration**.
    
3. Sélectionnez **Programmes et fonctionnalités**.
    
4. Sélectionnez **Complément Microsoft Junk E-mail Reporting pour Microsoft Office Outlook**.
    
5. Sélectionnez **Désinstaller**.
    
6. Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.
    
### <a name="uninstall-the-junk-email-reporting-add-in-by-running-the-windows-installer-package"></a>Désinstallation du complément Junk Email Reporting en exécutant le package Windows Installer
<a name="BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage"> </a>

1. Sur votre ordinateur, fermez Outlook.
    
    > [!NOTE]
    > Si Outlook est en cours d'exécution durant le processus de désinstallation, vous devrez le redémarrer pour achever la désinstallation du complément. 
  
2. Réexécutez le fichier .msi que vous avez précédemment exécuté pour installer le complément. 
    
    (Accédez à la page du centre de téléchargement Microsoft pour le complément Outil de signalement de courrier indésirable Microsoft pour Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkId=147248](https://go.microsoft.com/fwlink/?LinkId=147248), téléchargez le fichier .msi, puis double-cliquez dessus.) 
    
3. Suivez les invites pour désinstaller le complément.
    
4. Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.
    
### <a name="uninstall-the-junk-email-reporting-add-in-in-silent-mode"></a>Désinstallation du complément Junk Email Reporting en mode sans assistance
<a name="MK_UninstalltheJunkEmailReportingAdd-ininSilentMode"> </a>

1. Sur votre ordinateur, fermez Outlook.
    
    > [!NOTE]
    > Si Outlook est en cours d'exécution durant le processus de désinstallation, vous devrez le redémarrer pour achever la désinstallation du complément. 
  
2. Ouvrez une invite de commandes.
    
3. Spécifiez le paramètre de ligne de commande suivant :
    
    Ordinateurs exécutant x86 Outlook :  `msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
    Ordinateurs exécutant x64 Outlook :  `msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`
    
4. Redémarrez Outlook pour vérifier que le complément ne s'affiche plus dans le ruban Outlook.
    
## <a name="for-more-information"></a>Pour plus d’informations
<a name="sectionSection3"> </a>

[Signaler les messages de courrier indésirable à Microsoft](report-junk-email-messages-to-microsoft.md)
  
[Résolution des problèmes et informations de support technique](troubleshooting-and-support-information.md)
  

