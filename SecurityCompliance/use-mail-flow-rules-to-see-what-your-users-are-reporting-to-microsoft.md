---
title: Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Vous pouvez créer une règle de transport Exchange pour empêcher vos utilisateurs d'envoyer des messages électroniques à Microsoft à des fins d'analyse et de les utiliser dans vos propres processus de sécurité.
ms.openlocfilehash: 7ee8fb2bca1071ccd4080379485c1670a5e66a73
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206407"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft

Il existe plusieurs façons d'envoyer des messages faux positifs et faux négatifs à Microsoft pour analyse. En tant qu'administrateur, vous pouvez utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs signalent à Microsoft comme courrier indésirable, non-courrier indésirable et hameçonnage. Pour plus d'informations, consultez la rubrique soumettre des courriers indésirables, des courriers indésirables [et des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). À l'inverse, vous pouvez créer une règle de transport Exchange pour empêcher vos utilisateurs d'envoyer des messages électroniques à Microsoft à des fins d'analyse et de les utiliser dans vos propres processus de sécurité.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée «règles de transport» dans la rubrique [stratégie de messagerie et autorisations de conformité](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) , ainsi que l'entrée «stratégies de boîte aux lettres Outlook sur le Web» dans la rubrique [clients and Mobile](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) Devices Permissions. 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Utiliser le CAE pour créer une règle de flux de messagerie afin d'afficher le courrier signalé comme indésirable, comme hameçonnage et comme non indésirable par les utilisateurs

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Autres options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **Le destinataire**, puis **l'adresse comprend l'un des mots suivants**.
    
5. Dans la zone **spécifier des mots ou des expressions**, effectuez les opérations suivantes : 
    - Tapez `abuse@messaging.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis tapez `junk@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Ces adresses de messagerie sont utilisées pour envoyer des messages faux négatifs à Microsoft.
    - Tapez `phish@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Cette adresse de messagerie est utilisée pour envoyer les messages hameçons manqués à Microsoft.
    - Tapez `false_positive@messaging.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis tapez `not_junk@office365.microsoft.com` , puis cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter. Ces adresses de messagerie sont utilisées pour envoyer des messages faux positifs à Microsoft.
    - Cliquez sur **OK**.
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Envoyer le message en Cci vers...**, puis sélectionnez les boîtes aux lettres où vous voulez recevoir les messages. 
    
7. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d'autres sélections. Nous vous recommandons de tester la règle pendant une période avant de l'appliquer. Voir [les procédures pour les règles de flux de messagerie](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures). 
    
8. Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles. 
    
Une fois la règle créée et appliquée, tous les messages envoyés à partir de votre organisation aux adresses de messagerie spécifiées seront copiés vers la boîte aux lettres spécifiée.
  

