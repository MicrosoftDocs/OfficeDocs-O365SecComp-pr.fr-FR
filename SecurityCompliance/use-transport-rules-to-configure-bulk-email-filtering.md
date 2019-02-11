---
title: Utiliser les règles de flux de messagerie pour configurer des messages électroniques en masse de filtrage dans Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Administrateurs peuvent apprendre à utiliser les règles de flux de messagerie dans Exchange Online Protection pour le filtrage de courrier électronique en bloc.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382805"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a>Utiliser les règles de flux de messagerie pour configurer des messages électroniques en masse de filtrage dans Exchange Online Protection

Vous pouvez définir des filtres de contenu à l'échelle de l'entreprise pour le courrier indésirable et le courrier en masse à l'aide des stratégies de filtrage de contenu du courrier indésirable par défaut. Consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md) et [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) sur la façon de définir les stratégies de filtrage de contenu. 
  
Si vous souhaitez plus d’options pour filtrer les messages en bloc, vous pouvez créer des règles de flux de messagerie (également connu sous les règles de transport) pour rechercher des modèles de texte ou des expressions fréquemment trouvées dans les messages électroniques en masse. Tout message contenant ces caractéristiques sera être marqué comme courrier indésirable. Ces règles permettent de réduire la quantité de courrier indésirable que reçoit votre organisation.
  
**Remarques** :

- Avant de créer des règles de flux de la messagerie documenté cette rubrique, nous vous recommandons de lire tout d’abord [Quelle est la différence entre courrier indésirable et les messages électroniques en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md) et [valeurs au niveau de réclamation en bloc](bulk-complaint-level-values.md). 
  
- Les procédures suivantes permettent de marquer un message comme indésirable à l'échelle de votre organisation toute entière. Toutefois, vous pouvez ajouter une condition afin de n'appliquer ces règles qu'à des destinataires spécifiques de votre organisation. De cette façon, les paramètres de filtrage restrictif des messages électroniques ne s'appliqueront qu'à quelques utilisateurs particulièrement ciblés et le reste de vos utilisateurs (qui reçoivent en général les messages électroniques en masse auxquels ils se sont inscrits) ne seront pas concernés. 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a>Créer des règles de flux de messagerie pour filtrer les messages électroniques en masse basés sur les modèles de texte

1. Dans le Centre d'administration Exchange (CAE), accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une nouvelle règle**.
    
3. Indiquez le nom de la règle.
    
4. Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps correspond à ces modèles de texte**.
    
5. Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions régulières suivantes, qui figurent généralement dans les messages électroniques en masse, puis cliquez sur **OK** lorsque vous avez terminé : 
    
   - Si vous ne parvenez pas à visualiser le contenu de ce message électronique\, veuillez
    
   - \\>(safe )?unsubscribe( here)?\\</a\\>
    
   - Si vous ne souhaitez plus recevoir de communications comme celle-ci\, veuillez
    
   - \\<img height\="?1"? width\="?1"? src\=.?http\://
    
   - Pour ne plus recevoir ces\s+messages\:http\://
    
   - Pour annuler l'abonnement à \w+ (e\-?letter|e?-?mail|bulletin d'informations)
    
   - ne( souhaitez)? plus( que)? recevoir \w+ message électronique
    
   - Si vous ne parvenez pas à visualiser le contenu de ce message\, cliquez ici
    
   - Pour vous assurer que vous recevez (vos offres quotidiennes|nos messages électroniques)\, ajoutez
    
   - Si vous ne souhaitez plus recevoir ces courriers
    
   - pour modifier vos (préférences d'abonnement|préférences ou vous désinscrire)
    
   - cliquez (ici pour|sur le bouton) annuler l'abonnement
    
   **Remarques** :

   - La liste ci-dessus n’est pas un ensemble complet des expressions régulières dans les messages électroniques en masse ; plus d’informations peut être ajouté ou supprimé selon vos besoins. Toutefois, il est un bon point de départ.
    
   - La recherche des mots ou des modèles de texte dans l’objet ou d’autres champs d’en-tête dans le message se produit *une fois que* le message a été décodées du transfert de contenu MIME méthode qui a été utilisé pour transmettre le message entre les serveurs SMTP en texte ASCII binaire de codage. Vous ne pouvez pas utiliser les conditions ou exceptions pour rechercher le texte brut (en règle générale, Base64) codé les valeurs de l’objet ou d’autres champs d’en-tête dans les messages. 
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.
    
7. Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.
    
   La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
    
   > [!NOTE]
   > Si votre action configurée est le message en quarantaine plutôt que d’envoyer à un dossier de courrier indésirable de destinataires, le message est envoyé à la mise en quarantaine administrateur comme une correspondance de règle de flux de messagerie et il ne sera pas disponible dans la quarantaine de l’utilisateur final ou par le biais de l’utilisateur final notifications de courrier indésirable. 
  
   Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).
    
8. Enregistrez la règle.
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a>Créer une règle de flux de messagerie pour filtrer les messages électroniques en masse en fonction des phrases

1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une nouvelle règle**.
    
3. Indiquez le nom de la règle.
    
4. Cliquez sur **Plus d'options**. Sous **Appliquer cette règle si**, sélectionnez **L'objet ou le corps** \> **l'objet ou le corps inclut l'un de ces mots**.
    
5. Dans la boîte de dialogue **spécifier des mots ou des expressions**, ajoutez une par une les expressions suivantes, qui figurent généralement dans les messages électroniques en masse, et cliquez sur **OK** lorsque vous avez terminé : 
    
   - pour modifier vos préférences ou annuler votre abonnement
    
   - Modifier les préférences de messagerie ou annuler l'abonnement
    
   - Ceci est un message promotionnel
    
   - Ce message vous a été envoyé suite à votre demande d'abonnement
    
   - cliquez ici pour vous désinscrire
    
   - Ce message vous a été envoyé car vous êtes abonné
    
   - Si vous ne souhaitez plus recevoir notre bulletin d'informations
    
   - pour vous désinscrire de ce bulletin d'informations
    
   - Si ce message ne s'affiche pas correctement
    
   - Ceci est un message publicitaire
    
   - vous souhaitez annuler l'abonnement ou modifier votre
    
   - afficher ce message électronique sous forme de page web
    
   - Vous recevez ce message car vous êtes abonné
    
   **Remarque**: une fois encore, cette liste n’est pas un ensemble complet des phrases présentes dans les messages électroniques en masse ; plus d’informations peut être ajouté ou supprimé selon vos besoins. Toutefois, il est un bon point de départ.
    
6. Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.
    
7. Dans la boîte de dialogue **spécifier la valeur SCL**, définissez la valeur SCL sur **5**, **6** ou **9**, puis cliquez sur **OK**.
    
   La définition du SCL sur 5 ou 6 déclenche l'action **Courrier indésirable**, tandis qu'une définition sur 9 déclenche l'action **Courrier indésirable à niveau de confiance élevé**, comme configuré dans la stratégie de filtrage du contenu. Le service effectue l'action définie dans la stratégie de filtrage de contenu. L'action par défaut consiste à placer le message dans le dossier Courrier indésirable des destinataires, mais différentes actions peuvent être configurées, comme décrit dans [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
    
   > [!NOTE]
   > Si votre action configurée est le message en quarantaine plutôt que d’envoyer à un dossier de courrier indésirable de destinataires, le message est envoyé à la mise en quarantaine administrateur comme une correspondance de règle de flux de messagerie et il ne sera pas disponible dans la quarantaine de l’utilisateur final ou par le biais de l’utilisateur final notifications de courrier indésirable. 
  
   Pour plus d'informations sur les valeurs SCL, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).

8. Enregistrez la règle.

## <a name="for-more-information"></a>Pour plus d'informations

[Quelle est la différence entre courrier indésirable et message électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)

[Valeurs BCL](bulk-complaint-level-values.md)

[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)

[Options de filtrage avancé](advanced-spam-filtering-asf-options.md)
