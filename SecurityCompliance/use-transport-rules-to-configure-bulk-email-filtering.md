---
title: Utiliser des règles de flux de messagerie pour configurer le filtrage du courrier en nombre dans Exchange Online Protection
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser des règles de flux de messagerie dans Exchange Online Protection pour le filtrage de courrier en nombre.
ms.openlocfilehash: 185a1174ba3e0d400926b03c073feb100f8e812d
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600787"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a>Utiliser des règles de flux de messagerie pour configurer le filtrage du courrier en nombre dans Exchange Online Protection

Vous pouvez définir des filtres de contenu à l'échelle de l'entreprise pour le courrier indésirable et le courrier en masse à l'aide des stratégies de filtrage de contenu du courrier indésirable par défaut. Consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md) et [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) sur la façon de définir les stratégies de filtrage de contenu. 
  
Si vous souhaitez utiliser davantage d’options pour filtrer les messages en masse, vous pouvez créer des règles de flux de messagerie (également appelées règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvées dans les messages électroniques en masse. Tout message contenant ces caractéristiques sera marqué comme courrier indésirable. L'utilisation de ces règles peut aider à réduire la quantité de messages électroniques indésirables que reçoit votre organisation.

> [!IMPORTANT]
> Avant de créer les règles de flux de messagerie décrites dans cette rubrique, nous vous recommandons de lire [d’abord la différence entre le courrier indésirable et le courrier électronique en](what-s-the-difference-between-junk-email-and-bulk-email.md) masse, ainsi que les [valeurs de niveau de réclamation en bloc](bulk-complaint-level-values.md).<br>Les procédures suivantes permettent de marquer un message comme indésirable à l'échelle de votre organisation toute entière. Toutefois, vous pouvez ajouter une condition afin de n'appliquer ces règles qu'à des destinataires spécifiques de votre organisation. De cette façon, les paramètres de filtrage restrictif des messages électroniques ne s'appliqueront qu'à quelques utilisateurs particulièrement ciblés et le reste de vos utilisateurs (qui reçoivent en général les messages électroniques en masse auxquels ils se sont inscrits) ne seront pas concernés. 
  
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des modèles de texte

1. Dans le Centre d’administration Exchange, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Ajouter** ![une](media/ITPro-EAC-AddIcon.gif) icône Ajouter, puis sélectionnez **créer une nouvelle règle**.
    
3. Indiquez le nom de la règle.
    
4. Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps correspond à ces modèles de texte**.
    
5. Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions régulières suivantes, qui figurent généralement dans les messages électroniques en masse, puis cliquez sur **OK** lorsque vous avez terminé : 
    
   - `If you are unable to view the content of this email\, please`
    
   - `\>(safe )?unsubscribe( here)?\</a\>`
    
   - `If you do not wish to receive further communications like this\, please`
    
   - `\<img height\="?1"? width\="?1"? sr\c=.?http\://`
    
   - `To stop receiving these+emails\:http\://`
    
   - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`
    
   - `no longer (wish )?(to )?(be sent|receive) w+ email`
    
   - `If you are unable to view the content of this email\, please click here`
    
   - `To ensure you receive (your daily deals|our e-?mails)\, add`
    
   - `If you no longer wish to receive these emails`
    
   - `to change your (subscription preferences|preferences or unsubscribe)`
    
   - `click (here to|the) unsubscribe`
    
   La liste ci-dessus n’est pas un ensemble exhaustif d’expressions régulières trouvées dans les messages électroniques en masse; vous pouvez en ajouter ou en supprimer autant que nécessaire. Toutefois, ils constituent un bon point de départ.<br>La recherche de mots ou de modèles de texte dans l’objet ou les autres champs d’en-tête du message se produit *après* que le message a été décodé à partir de la méthode de codage de transfert de contenu MIME qui a été utilisée pour transmettre le message binaire entre les serveurs SMTP dans le texte ASCII. Vous ne pouvez pas utiliser de conditions ou d’exceptions pour rechercher les valeurs codées brutes (en règle générale, en base 64) dans l’objet ou d’autres champs d’en-tête des messages. 
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.
    
7. Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.
    
   La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
    
   Si votre action configurée consiste à mettre le message en quarantaine au lieu de l’envoyer au dossier de courrier indésirable des destinataires, le message est envoyé à la mise en quarantaine de l’administrateur en tant que correspondance de règle de flux de messagerie et n’est pas disponible dans le cadre de la mise en quarantaine du courrier indésirable de l’utilisateur final ou via l’utilisateur final notifications de courrier indésirable. 
  
   Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).
    
8. Enregistrez la règle.
    
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a>Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des expressions

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Ajouter** ![une](media/ITPro-EAC-AddIcon.gif) icône Ajouter, puis sélectionnez **créer une nouvelle règle**.
    
3. Indiquez le nom de la règle.
    
4. Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps inclut l'un de ces mots**.
    
5. Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions suivantes, qui figurent généralement dans les messages électroniques en masse, et cliquez sur **OK** lorsque vous avez terminé : 
    
   - `to change your preferences or unsubscribe`
    
   - `Modify email preferences or unsubscribe`
    
   - `This is a promotional email`
    
   - `You are receiving this email because you requested a subscription`
    
   - `click here to unsubscribe`
    
   - `You have received this email because you are subscribed`
    
   - `If you no longer wish to receive our email newsletter`
    
   - `to unsubscribe from this newsletter`
    
   - `If you have trouble viewing this email`
    
   - `This is an advertisement`
    
   - `you would like to unsubscribe or change your`
    
   - `view this email as a webpage`
    
   - `You are receiving this email because you are subscribed`
    
   Cette liste n’est pas un ensemble exhaustif d’expressions trouvées dans les messages électroniques en masse; vous pouvez en ajouter ou en supprimer autant que nécessaire. Toutefois, ils constituent un bon point de départ.
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.
    
7. Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.
    
   La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
    
   Si votre action configurée consiste à mettre le message en quarantaine au lieu de l’envoyer au dossier de courrier indésirable des destinataires, le message est envoyé à la mise en quarantaine de l’administrateur en tant que correspondance de règle de flux de messagerie et n’est pas disponible dans le cadre de la mise en quarantaine du courrier indésirable de l’utilisateur final ou via l’utilisateur final notifications de courrier indésirable. 
  
   Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).

8. Enregistrez la règle.

## <a name="for-more-information"></a>Pour plus d’informations

[Quelle est la différence entre courrier indésirable et message électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)

[Valeurs BCL](bulk-complaint-level-values.md)

[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)

[Options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md)
