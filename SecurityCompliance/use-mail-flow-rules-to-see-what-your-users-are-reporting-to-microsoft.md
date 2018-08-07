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
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Vous pouvez créer une règle de Transport Exchange pour empêcher les utilisateurs d’envoyer des messages électroniques à Microsoft pour analyse et de les utiliser dans votre propre processus de sécurité
ms.openlocfilehash: 6c6af23e6a5f345e26c7dc09c898f2978ea51a5f
ms.sourcegitcommit: df1e9590a9fa152fa776f16d9b25c180ba7198f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2018
ms.locfileid: "22122584"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a>Utiliser des règles de transport pour bloquer le signalement des courriers indésirables à Microsoft

Il existe plusieurs façons, vous pouvez envoyer des messages faux positifs et faux négatifs à Microsoft pour analyse. En tant qu’administrateur, vous pouvez utiliser les règles de flux de messagerie pour voir ce que vos utilisateurs sont des rapports à Microsoft en tant que courrier indésirable, non-spam et hameçonnage. Pour plus d’informations, voir [envoi spam, légitimes et des hameçonnage anti-spam à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Inversement, vous pouvez créer une règle de Transport Exchange pour empêcher les utilisateurs d’envoyer des messages électroniques à Microsoft pour analyse et de les utiliser dans votre propre processus de sécurité.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Règles de transport » entrée dans la rubrique [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) et l'entrée « Stratégies de boîte aux lettres Outlook Web App » dans la rubrique [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx). 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a>Utiliser le CAE pour créer une règle de flux de messagerie afin d'afficher le courrier signalé comme indésirable, comme hameçonnage et comme non indésirable par les utilisateurs

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Autres options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **Le destinataire**, puis **l'adresse comprend l'un des mots suivants**.
    
5. Dans la zone **spécifier des mots ou des expressions**, effectuez les opérations suivantes : 
    - Type de `abuse@messaging.microsoft.com` , puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.png), puis tapez `junk@office365.microsoft.com` , puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.png). Ces adresses de messagerie sont utilisés pour envoyer des messages faux négatifs à Microsoft.
    - Type de `phish@office365.microsoft.com` , puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.png). Cette adresse de messagerie est utilisée pour envoyer des messages de hameçonnage manquées à Microsoft.
    - Type de `false_positive@messaging.microsoft.com` , puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.png), puis tapez `not_junk@office365.microsoft.com` , puis cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.png). Ces adresses de messagerie sont utilisés pour envoyer des messages faux positifs à Microsoft.
    - Cliquez sur **OK**.
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Envoyer le message en Cci vers...**, puis sélectionnez les boîtes aux lettres où vous voulez recevoir les messages. 
    
7. Si vous le souhaitez, vous pouvez émettre des sélections d’audit de la règle, test de la règle, activez la règle pendant une période spécifique et des autres sélections. Nous vous recommandons de tester la règle pour une période avant que vous l’appliquez. Voir les [procédures pour les règles de flux de messagerie](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures). 
    
8. Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles. 
    
Une fois la règle créée et appliquée, tous les messages envoyés à partir de votre organisation aux adresses de messagerie spécifiées seront copiés vers la boîte aux lettres spécifiée.
  

