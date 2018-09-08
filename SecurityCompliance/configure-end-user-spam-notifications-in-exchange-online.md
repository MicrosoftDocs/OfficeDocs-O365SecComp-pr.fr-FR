---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online
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
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Vous pouvez configurer les notifications de courrier indésirable à l'utilisateur final pour la stratégie de filtrage de contenu par défaut à l'échelle de l'entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines.
ms.openlocfilehash: e29cc850b7f91ed4ec963a8e52e40a0044fa7f6c
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875806"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online

> [!IMPORTANT]
> Cette rubrique est pour les clients Exchange Online qui protègent les boîtes aux lettres hébergées sur le cloud. Les clients autonomes Exchange Online Protection (EOP) qui sont protection des boîtes aux lettres locales doivent lire la rubrique suivante au lieu de cela : [configuration de notifications de courrier indésirable pour l’utilisateur final dans EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Vous pouvez configurer les notifications de courrier indésirable pour l’utilisateur final pour la stratégie de filtrage de contenu par défaut à l’échelle de l’entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines. L’activation des notifications de courrier indésirable à l’utilisateur final permet à vos utilisateurs de gérer eux-mêmes leurs propres messages de courrier indésirable mis en quarantaine. La fonctionnalité ne peut pas être utilisée avec les stratégies appliquées à des utilisateurs ou des groupes, ou à une stratégie comportant des exceptions.
  
Les notifications de courrier indésirable à l’utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l’utilisateur final au cours d’une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.
  
Après avoir reçu un message de notification, les utilisateurs finaux peuvent choisir parmi les options suivantes :

**Aperçu** du message si vous souhaitez afficher un aperçu de l’en-tête avant d’effectuer action ou le contenu.

**Télécharger** le message que vous souhaitez passer en revue les messages et les pièces jointes (le cas échéant) sur votre appareil avant d’effectuer action.

**Version** si le message n’est pas du courrier indésirable et que vous souhaitez qu’Office 365 pour envoyer le message vers votre boîte aux lettres.

**Version & expéditeur autoriser** si le message n’est pas du courrier indésirable et que vous souhaitez qu’Office 365 pour ajouter l’expéditeur à votre expéditeurs fiables et la liste des destinataires pour les courriers électroniques futurs. N’oubliez pas que votre administrateur peut avoir autres configurations d’autoriser/bloquer large organisation qui remplacent votre liste des expéditeurs approuvés.

**Version & rapport**, si le message n’est pas du courrier indésirable et que vous souhaitez envoyer le message vers votre boîte aux lettres et de signaler à Microsoft pour analyse.

**Bloc** de si vous souhaitez que Office 365 pour ajouter l’expéditeur à votre liste des expéditeurs bloqués.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

Durée d'exécution estimée : 2 minutes
  
Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée « Anti-spam » dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Utiliser le Centre d'administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l'utilisateur final

1. Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de contenu**.
    
2. Sélectionnez la stratégie de filtrage de contenu pour laquelle vous voulez activer les notifications de courrier indésirable à l'utilisateur final (elles sont désactivées par défaut).
    
3. Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**. 
    
4. Dans la boîte de dialogue, vous pouvez configurer les options suivantes :
    
1. **Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.) 
    
2. **Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place. 
    
3. **Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. 
    
5. Cliquez sur **Enregistrer**. Un récapitulatif de vos paramètres de stratégie de filtrage de contenu, y compris vos paramètres de notification de courrier indésirable à l'utilisateur final, apparaît dans le volet de droite.
    
> [!NOTE]
>  Les notifications de courrier indésirable à l'utilisateur final ne sont opérationnelles que pour les stratégies de filtrage de contenu activées. >  Les notifications de courrier indésirable pour l'utilisateur final sont envoyées uniquement une fois par jour. Le délai de remise de la notification ne peut pas être garanti pour chaque client et n'est pas configurable. 
  
 **Conseil :** si vous voulez tester les notifications de courrier indésirable destinées aux utilisateurs finals en les envoyant à un ensemble limité d'utilisateurs avant de les implémenter totalement, créez une stratégie de filtrage de contenu personnalisée autorisant ces notifications de courrier indésirable pour les domaines dans lesquels les utilisateurs résident. Ensuite, dans le CAE, sous **Flux de messagerie \> Règles**, créez une règle de transport permettant de bloquer les messages provenant de quarantine@messaging.microsoft.com (l'adresse de messagerie qui envoie les notifications) avec des exceptions pour les utilisateurs qui doivent recevoir les notifications. L'image suivante représente un exemple de création d'exception pour deux utilisateurs (SaraD et AlexD) du domaine Contoso.com : 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Pour plus d'informations

[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
