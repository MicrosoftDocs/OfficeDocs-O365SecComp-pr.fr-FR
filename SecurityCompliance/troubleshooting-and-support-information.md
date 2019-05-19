---
title: Dépannage et informations relatives au support
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5d9f75f5-bb7f-458c-ad30-5c8eae0b0e4e
ms.collection:
- M365-security-compliance
description: Cette rubrique décrit les étapes de résolution des problèmes pour les utilisateurs finaux et les administrateurs, et fournit des informations sur la manière de contacter le support technique pour obtenir de l'aide.
ms.openlocfilehash: baf8761ca4ce55695c2def74a39d3ca9a6de79ff
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156336"
---
# <a name="troubleshooting-and-support-information"></a>Dépannage et informations relatives au support

Cette rubrique décrit les étapes de résolution des problèmes pour les utilisateurs finaux et les administrateurs, et fournit des informations sur la manière de contacter le support technique pour obtenir de l'aide.
  
## <a name="troubleshooting-for-users"></a>Résolution des problèmes pour les utilisateurs

Parfois, vous pouvez rencontrez des difficultés après l'ajout du complément Junk Email Reporting (signalement des courriers indésirables) dans Microsoft Office Outlook. Voici certains problèmes que vous pouvez rencontrer ainsi que des conseils pour les résoudre. 
  
- Rien ne se passe quand vous cliquez sur **Signaler le courrier indésirable**.
    
- Outlook cesse de répondre après avoir sélectionné un message électronique
    
- Le courrier indésirable signalé ne peut pas être remis en raison d'une réponse « Non remis ».
    
### <a name="troubleshooting-tip"></a>Conseil de dépannage

1. Fermez et redémarrez Microsoft Office Outlook.
    
2. Vérifiez que vous êtes en mesure de créer et d'envoyer un message de test. Pour ce faire, vous pouvez envoyer un message de test à un autre compte de messagerie que vous gérez, puis vérifiez que ce message électronique vous est remis.
    
Si le problème persiste, contactez votre administrateur informatique.
  
> [!TIP]
> Vous pouvez également envoyer directement des messages de courrier indésirable à Microsoft, à l'adresse électronique [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com), et des messages faux positifs à l'adresse électronique [not_junk@office365.microsoft.com](mailto: not_junk@office365.microsoft.com). Pour plus d'informations, consultez la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). 
  
## <a name="troubleshooting-for-administrators"></a>Résolution des problèmes pour les administrateurs

En tant qu'administrateur, vous pouvez rencontrer des problèmes avec des utilisateurs qui se servent du complément Junk Email Reporting (signalement des courriers indésirables) pour Microsoft Office Outlook. Voici quelques conseils pour résoudre les problèmes que vous pourriez rencontrer. 
  
 **Problème :** un message d'erreur demandant aux utilisateurs de contacter leur administrateur système apparaît sans cesse. 
  
### <a name="troubleshooting-tip"></a>Conseil de dépannage

1. Définissez la valeur de la clé de Registre suivante sur « Verbose » :
    
  - **Outlook 32 bits installé sur un système d'exploitation 32 bits :**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **Outlook 32 bits installé sur un système d'exploitation 64 bits :**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
  - **Outlook 64 bits (toujours installé sur un système d'exploitation 64 bits) :**
    
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel
    
2. Redémarrez Microsoft Office Outlook et demandez aux utilisateurs de vous avertir dès qu'ils reçoivent le message d'erreur.
    
3. Collectez les informations de journal se trouvant à l'emplacement suivant : 
    
    %LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt
    
4. Contactez les techniciens du support Exchange Online Protection et fournissez-leur les informations du journal. 
    
 **Problème :** les utilisateurs décident de ne pas recevoir de confirmation quand ils signalent un message électronique comme courrier indésirable, mais ils souhaitent maintenant réactiver cette option. 
  
### <a name="troubleshooting-tip"></a>Conseil de dépannage

1. Définissez la valeur de la clé de Registre suivante sur « True » : HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences\ConfirmReportJunk
    
2. Redémarrez Microsoft Office Outlook.
    
## <a name="support-information"></a>Informations concernant le support

Si vous avez besoin d’aide pour l’installation, la configuration ou la désinstallation du complément, veuillez contacter le support technique à l’aide du lien nouvelle demande de service sur la page support dans le centre d’administration 365 de Microsoft. Pour obtenir des options supplémentaires, notamment la soumission d’une demande de service via les options de téléphone et d’auto-assistance, consultez [l’aide et le support pour EOP](eop/help-and-support-for-eop.md).
  
## <a name="for-more-information"></a>Pour plus d’informations

[Activer le complément Signaler le message](https://support.office.com/article/4250c4bc-6102-420b-9e0a-a95064837676)
  
[Signaler les messages de courrier indésirable à Microsoft](report-junk-email-messages-to-microsoft.md)
  

