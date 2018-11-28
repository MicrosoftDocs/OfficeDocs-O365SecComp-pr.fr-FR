---
title: Activer le complément Signaler le message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Découvrez comment activer le complément de Message de rapport pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou la totalité de votre organisation.
ms.openlocfilehash: f35899d3f0be9ee07cb6dae5c5fec40395948340
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706368"
---
# <a name="enable-the-report-message-add-in"></a>Activer le complément Signaler le message

## <a name="overview"></a>Vue d’ensemble

Le complément de Message de rapport pour Outlook et Outlook sur le Web permet aux utilisateurs de créer facilement des rapports e-mail mal classé, fiables ou malveillantes, Microsoft et ses filiales pour l’analyse. Microsoft utilise ces envois pour améliorer l’efficacité des technologies de protection de courrier électronique. En outre, si votre organisation utilise [Office 365 avancée protection contre les menaces](office-365-atp.md) ou des [Menaces Office 365](office-365-ti.md), le complément de Message de rapport fournit l’équipe de sécurité de votre organisation des informations utiles, qu'ils peuvent utiliser pour examiner et mettre à jour stratégies de sécurité. 

Par exemple, supposons que personnes signalent un grand nombre de messages phishing. Cette surfaces d’informations dans le [Tableau de bord de sécurité](security-dashboard.md) et autres rapports. L’équipe de sécurité de votre organisation permettre utiliser ces informations comme une indication que les stratégies anti-hameçonnage devront être mis à jour. Ou, si un grand nombre de messages qui ont été marqués comme courrier indésirable comme légitime à l’aide du complément de Message de rapport signalez des personnes, l’équipe de sécurité de votre organisation devront ajuster les [stratégies de blocage du courrier indésirable](configure-the-anti-spam-policies.md). 

Le complément de Message de rapport fonctionne avec votre abonnement Office 365 et les produits suivants :
 - Outlook sur le Web
 - Outlook 2013 SP1
 - Outlook 2016
 - Outlook 2016 pour Mac
 - Outlook inclus avec Office 365 ProPlus
  
Si vous êtes un utilisateur individuel, vous pouvez [Activer le complément de Message de rapport par vous-même](#get-the-report-message-add-in-for-yourself). 
  
Si vous êtes un administrateur global d’Office 365 ou un administrateur Exchange Online et Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez [Activer le complément de Message de rapport pour votre organisation](#get-and-enable-the-report-message-add-in-for-your-organization). Le rapport de Message Add-In est désormais disponible par le biais de [Déploiement centralisé](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).
    
## <a name="get-the-report-message-add-in-for-yourself"></a>Obtenez le Message de rapport de complément pour vous-même

1. Dans [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), recherchez le [complément de Message de rapport](https://appsource.microsoft.com/product/office/wa104381180).
    
2. Choisissez **obtenir maintenant IT**.<br/>![Déclaration de Message - maintenant](media/ReportMessageGETITNOW.png)<br/> 
    
3. Passez en revue les termes du contrat de stratégie de confidentialité et d’utilisation. Puis cliquez sur **Continuer**. 
    
4. Connectez-vous à votre messagerie électronique Office 365 à l’aide de votre travail compte école (pour une utilisation professionnelle) ou votre compte Microsoft (pour une utilisation personnelle).
    
Une fois que le complément est installé et activé, vous verrez les icônes suivantes : 

- Dans Outlook, l’icône ressemble à ceci : <br/> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- Dans Outlook Web App, l’icône ressemble à ceci :<br/>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

Étape suivante, découvrez comment [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a>Obtenir et activer le complément de Message de rapport pour votre organisation

> [!IMPORTANT]
> Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche. En outre, Exchange doit être configuré pour utiliser l’authentification OAuth pour plus d’informations, voir [Configuration requise pour Exchange (centralisée le déploiement des compléments)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements). 

1. Accédez à la [page des compléments et des Services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365 nouveau.<br/>![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)<br/> 
    
2. Choisissez **+ déployer le complément**.<br/>![Cliquez sur déployer le complément](media/ServicesAddIns-ChooseDeployAddIn.png)<br/> 
    
3. Dans l’écran nouveau complément, passez en revue les informations, puis cliquez sur **suivant**.<br/>![Nouveau complément plus d’informations](media/NewAddInScreen1.png)<br/>
    
4. Sélectionnez **Ajouter un complément à partir de l’Office Store**, puis cliquez sur **suivant**.<br/>![Vous voulez ajouter un nouveau complément](media/NewAddInScreen2.png)<br/> 
    
5. Pour un Message de rapport et dans la liste des résultats, en regard du complément Message d’état de la recherche, cliquez sur Ajouter.<br/>![Rechercher un Message de rapport, puis choisissez Ajouter](media/NewAddInScreen3.png)<br/>
    
6. Dans l’écran de Message de rapport, passez en revue les informations, puis cliquez sur **suivant**.<br/>![Détails du Message](media/ReportMessageAdd-InNewScreen4.png)<br/>

7. Spécifier les paramètres utilisateur par défaut pour Outlook, puis cliquez sur **suivant**.<br/>![Signaler les paramètres par défaut des messages pour Outlook](media/ReportMessageOptionsScreen5.png)<br/>

8. Spécifier qui obtient le Message de rapport Add-in, puis cliquez sur **Enregistrer**. <br/>![Qui obtient le Message de rapport complément](media/ReportMessageOptionsScreen6.png)<br/>

> [!TIP]
> Nous vous recommandons de [paramétrage d’une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)

Selon ce que vous sélectionné à l’aide de l’Assistant, les personnes de votre organisation auront le [complément de Message d’état](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) disponibles. Les personnes dans votre organisation, voient les icônes suivantes : 

- Dans Outlook, l’icône ressemble à ceci : <br/> ![Icône Message Add-in rapport pour Outlook](media/OutlookReportMessageIcon.png)<br/>
- Dans Outlook Web App, l’icône ressemble à ceci :<br/>![Outlook sur l’icône Ajouter dans un Message de rapport Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a>Définir une règle pour obtenir une copie des messages électroniques signalés par vos utilisateurs

> [!IMPORTANT]
> Vous devez être administrateur Exchange Online pour effectuer cette tâche.
  
Vous pouvez configurer une règle pour obtenir une copie des messages électroniques signalés par les utilisateurs de votre organisation. Cela après avoir téléchargé et activé le complément de Message de rapport pour votre organisation.
  
1. Dans le centre d’administration Exchange, choisissez **flux de messagerie** \> **règles**. 
    
2. Choisissez **+** \> **créer une nouvelle règle**. 
    
3. Dans la zone **nom** , tapez un nom, tel que des envois.
    
4. Dans la liste **appliquer cette règle si** , sélectionnez **l’adresse du destinataire inclut...**. 
    
5. Dans l’écran **spécifier les mots ou expressions** , ajoutez `junk@office365.microsoft.com` et `phish@office365.microsoft.com`, puis cliquez sur **OK**.<br/>![Spécifier les adresses de courrier indésirable et de phishing pour la règle](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)<br/>
  
6. Dans la liste **effectuer les opérations suivantes** , choisissez **Cci du message pour...**. 
    
7. Ajouter un administrateur global, un administrateur de sécurité et/ou lecteur de sécurité qui doit recevoir une copie de chaque message électronique qui signalent à Microsoft les personnes, puis cliquez sur **OK**.<br/>![Ajouter un administrateur global ou de sécurité pour recevoir une copie de chaque message signalé](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)<br/>
  
8. Sélectionnez **Auditer cette règle avec le niveau de gravité**, puis choisissez **moyenne**. 
    
9. Sous **Choisir un mode de cette règle**, cliquez sur **Appliquer**.<br/>![Définir une règle pour obtenir une copie de chaque message signalé](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)<br/>
  
10. Sélectionnez **Save (Enregistrer)**. 
    
À cette règle en place, chaque fois qu’une personne de votre organisation signale un message électronique à l’aide du complément Message de rapport, votre administrateur général, administrateur de sécurité et/ou lecteur sécurité reçoit une copie de ce message. Ces informations permettent de vous permet de définir ou ajuster les stratégies, telles que les stratégies de [Liaisons sans échec de Office 365 DAV](atp-safe-links.md) . 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Vérifier ou modifier les paramètres pour le complément de Message de rapport

Vous pouvez consulter et modifier les paramètres par défaut pour le rapport de Message complément dans la [page Services et compléments](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns). 

> [!IMPORTANT]
> Vous devez être un administrateur global d’Office 365 ou Exchange Online administrateur pour effectuer cette tâche.
    
1. Accédez à la [page des compléments et des Services](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) dans le centre d’administration Microsoft 365 nouveau.<br/>![Page Services et compléments dans le nouveau centre d’administration de 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)<br/>

2. Recherchez et sélectionnez le rapport de Message Add-In.<br/>![Recherchez et sélectionnez le complément de Message de rapport](media/FindReportMessageAddIn.png)<br/> 
    
3. Dans l’écran de Message de rapport, passez en revue et modifier les paramètres comme il convient pour votre organisation.<br/>![Complément de paramètres pour le Message d’état](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a>Découvrez comment utiliser le complément de Message de rapport

Consultez la rubrique [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).
  
## <a name="related-topics"></a>Voir aussi

[Utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité](view-email-security-reports.md)

[Afficher les rapports de Protection de menace avancées d’Office 365](view-reports-for-atp.md)

[Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité](use-explorer-in-security-and-compliance.md)
  

