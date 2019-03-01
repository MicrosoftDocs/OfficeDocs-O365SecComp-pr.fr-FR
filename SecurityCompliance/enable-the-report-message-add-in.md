---
title: Activer le complément Signaler le message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le complément de message de rapport pour Outlook et Outlook sur le Web, pour des utilisateurs individuels ou l'ensemble de votre organisation.
ms.openlocfilehash: c184b7ac1baef297d65e6e93e4e7a085920d87b0
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341425"
---
# <a name="enable-the-report-message-add-in"></a>Activer le complément Signaler le message

## <a name="overview"></a>Vue d’ensemble

Le complément de message de rapport pour Outlook et Outlook sur le Web permet aux utilisateurs de signaler facilement les messages électroniques, qu'ils soient fiables ou malveillants, à Microsoft et à ses filiales pour analyse. Microsoft utilise ces soumissions pour améliorer l'efficacité des technologies de protection de la messagerie. En outre, si votre organisation utilise [office 365 Advanced Threat Protection](office-365-atp.md) ou [Office 365 Threat Intelligence](office-365-ti.md), le complément Report message fournit à l'équipe de sécurité de votre organisation des informations utiles qu'elle peut utiliser pour examiner et mettre à jour stratégies de sécurité. 

Par exemple, supposons que des personnes signalent un grand nombre de messages comme hameçonnage. Ces informations sont rePrésentées dans le [tableau de bord de sécurité](security-dashboard.md) et d'autres rapports. L'équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies de détection d'hameçonnage doivent être mises à jour. Ou bien, si des personnes signalent un grand nombre de messages marqués comme légitimes comme légitimes à l'aide du complément de message de rapport, il se peut que l'équipe de sécurité de votre organisation doive ajuster les [stratégies de blocage du courrier](configure-the-anti-spam-policies.md)indésirable. 

Le complément de message de rapport fonctionne avec votre abonnement Office 365 et les produits suivants:
 - Outlook sur le web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 pour Mac
 - Outlook inclus avec Office 365 proPlus

> [!NOTE]
> Le complément de message de rapport pour Outlook et Outlook sur le Web n'est pas exactement identique au filtre de courrier inDésirable [Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), bien que ces deux types permettent de marquer le courrier comme légitime, non légitime ou une tentative de hameçonnage. Le complément de message de rapport pour Outlook et Outlook sur le Web avertit Microsoft du courrier inDésirable, tandis que le filtre de courrier inDésirable d'Outlook est utilisé pour organiser les messages électroniques dans la boîte aux lettres d'un utilisateur. 
  
Si vous êtes un utilisateur individuel, vous pouvez [activer le complément de rapport de message pour vous-même](#get-the-report-message-add-in-for-yourself). 
  
Si vous êtes un administrateur général Office 365 ou un administrateur Exchange Online et qu'Exchange est configuré pour utiliser l'authentification OAuth, vous pouvez [activer le complément de message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization). Le complément de message de rapport est désormais disponible via un [déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenir le complément de message de rapport pour vous-même

1. Dans [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), recherchez le [complément Report message](https://appsource.microsoft.com/product/office/wa104381180).
    
2. Choisissez **obtenir maintenant**.<br/>![Message de rapport-Get it](media/ReportMessageGETITNOW.png)<br/> 
    
3. Passez en revue les conditions d'utilisation et la politique de confidentialité. Ensuite, cliquez sur **Continuer**. 
    
4. Connectez-vous à Office 365 à l'aide de votre compte professionnel ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour une utilisation personnelle).
    
Une fois le complément installé et activé, les icônes suivantes s'affichent: 

- Dans Outlook, l'icône se présente comme suit: <br/> ![Icône de complément de rapport de message pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- Dans Outlook sur le Web (anciennement appelé Outlook Web App), l'icône se présente comme suit:<br/>![Icône de complément de message de rapport Web Outlook sur le Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> En guise d'étape suivante, Découvrez comment [utiliser le complément Report message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obtenir et activer le complément de message de rapport pour votre organisation

> [!IMPORTANT]
> Vous devez être un administrateur général Office 365 ou un administrateur Exchange Online pour effectuer cette tâche. De plus, Exchange doit être configuré pour utiliser l'authentification OAuth pour en savoir plus, consultez la rubrique [Exchange Requirements (déploiement centralisé des compléments)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements). 

1. Accédez à la [page des compléments & de services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d'administration Microsoft 365.<br/>![Page services et compléments dans le nouveau centre d'administration Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Choisissez **+ déployer le complément**.<br/>![Choisir déployer le complément](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Dans l'écran **nouveau complément** , passez en revue les informations, puis cliquez sur **suivant**.<br/>![Détails sur les nouveaux compléments](media/NewAddInScreen1.png)<br/>
    
4. Sélectionnez **je veux ajouter un complément à partir de l'Office Store**, puis cliquez sur **suivant**.<br/>![Je veux ajouter un nouveau complément](media/NewAddInScreen2.png)<br/> 
    
5. Recherchez **message de rapport**, et dans la liste des résultats, en regard du **complément de message de rapport**, choisissez **Ajouter**.<br/>![Recherchez message de rapport, puis cliquez sur Ajouter.](media/NewAddInScreen3.png)<br/>
    
6. Dans l'écran du **rapport** , passez en revue les informations, puis cliquez sur **suivant**.<br/>![Signaler les détails du message](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Spécifiez les paramètres par défaut de l'utilisateur pour Outlook, puis cliquez sur **suivant**.<br/>![Paramètres par défaut des messages de rapport pour Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Spécifiez qui reçoit le complément de message de rapport, puis cliquez sur **Enregistrer**. <br/>![Qui obtient le complément de message de rapport](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Nous vous recommandons de [configurer une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).

En fonction de ce que vous avez sélectionné lors de la configuration du complément (étapes 7-8 ci-dessus), le complément de message de [rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) sera disponible pour les personnes de votre organisation. Les personnes de votre organisation verront les icônes suivantes: 

- Dans Outlook, l'icône se présente comme suit: <br/> ![Icône de complément de rapport de message pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- Dans Outlook sur le Web, l'icône se présente comme suit:<br/>![Icône de complément de message de rapport Web Outlook sur le Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> Lorsque vous informez les utilisateurs du complément Report message, incluez un lien permettant d' [utiliser le complément Report message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Configurer une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs

> [!IMPORTANT]
> Vous devez être un administrateur Exchange Online pour effectuer cette tâche.
  
Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation. Vous effectuez cette opération après avoir téléchargé et activé le complément de message de rapport pour votre organisation.
  
1. Dans le centre d'administration Exchange, sélectionnez **règles**de **flux** \> de messagerie. 
    
2. Sélectionnez **+** \> **créer une nouvelle règle**. 
    
3. Dans la zone **nom** , tapez un nom, tel que des envois.
    
4. Dans la liste **appliquer cette règle si** , choisissez **l'adresse du destinataire inclut...**. 
    
5. Dans l' **écran spécifier des mots ou** des expressions `junk@office365.microsoft.com` , `phish@office365.microsoft.com`ajoutez et, puis choisissez **OK**.<br/>![Spécifier les adresses de messagerie de courrier indésirable et de hameçonnage pour la règle](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Dans la liste **effectuer les opérations suivantes...** , choisissez **CCI le message à..**.. 
    
7. Ajoutez un administrateur général, un administrateur de sécurité et/ou un lecteur de sécurité qui doit recevoir une copie de chaque message électronique que les personnes signalent à Microsoft, puis choisissez **OK**.<br/>![Ajoutez un administrateur général ou un administrateur de sécurité pour recevoir une copie de chaque message signalé.](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Sélectionnez **auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**. 
    
9. Sous **choisir un mode pour cette règle**, choisissez **appliquer**.<br/>![Configurer une règle pour obtenir une copie de chaque message signalé](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Sélectionnez **Save (Enregistrer)**. 
    
Avec cette règle en place, chaque fois que quelqu'un de votre organisation signale un message électronique à l'aide du complément de message de rapport, votre administrateur général, votre administrateur de sécurité et/ou votre lecteur de sécurité recevront une copie de ce message. Ces informations vous permettent de configurer ou d'ajuster des stratégies, telles que [des stratégies de liens approuvés Office 365 ATP](atp-safe-links.md) ou vos paramètres de [blocage du courrier](anti-spam-protection.md) indésirable. 

## <a name="learn-how-to-use-the-report-message-add-in"></a>En savoir plus sur l'utilisation du complément de message de rapport

Voir [use the Report message Add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Vérifier ou modifier les paramètres du complément de message de rapport

Vous pouvez consulter et modifier les paramètres par défaut du complément de message de rapport sur la [page des compléments & de services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns). 

> [!IMPORTANT]
> Vous devez être un administrateur général Office 365 ou un administrateur Exchange Online pour effectuer cette tâche.
    
1. Accédez à la [page des compléments & de services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d'administration Microsoft 365.<br/>![Page services et compléments dans le nouveau centre d'administration Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Recherchez et sélectionnez le complément Report message.<br/>![Rechercher et sélectionner le complément de message de rapport](media/FindReportMessageAddIn.png)<br/> 
    
3. Dans l'écran signaler un message, vérifiez et modifiez les paramètres en fonction de votre organisation.<br/>![Paramètres du complément de message de rapport](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a>Voir aussi

[Utiliser le complément de message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité](view-email-security-reports.md)

[Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)

[Utiliser l'Explorateur dans le &amp; Centre de sécurité conformité](use-explorer-in-security-and-compliance.md)
  

