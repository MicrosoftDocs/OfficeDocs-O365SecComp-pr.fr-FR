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
description: Vous pouvez configurer les notifications de courrier indésirable de l’utilisateur final pour la stratégie de filtrage du courrier indésirable de l’entreprise par défaut ou les stratégies de filtrage anti-spam personnalisés qui sont appliqués aux domaines.
ms.openlocfilehash: 77ca32224cecaca2f558119db909ad74fdb6e858
ms.sourcegitcommit: cc8550452d099b4c5852c6559f6ca94a77f1d93b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2018
ms.locfileid: "27134768"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a>Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online

> [!IMPORTANT]
> Cette rubrique est pour les clients Exchange Online qui protègent les boîtes aux lettres hébergées sur le cloud. Les clients autonomes Exchange Online Protection (EOP) qui sont protection des boîtes aux lettres locales doivent lire la rubrique suivante au lieu de cela : [configuration de notifications de courrier indésirable pour l’utilisateur final dans EOP](configure-end-user-spam-notifications-in-eop.md). 
  
Vous pouvez configurer les notifications de courrier indésirable de l’utilisateur final pour la stratégie de filtrage du courrier indésirable de l’entreprise par défaut ou les stratégies de filtrage anti-spam personnalisés qui sont appliqués aux domaines. Activation des messages de notification de courrier indésirable de l’utilisateur final permet à vos utilisateurs finaux de gérer eux-mêmes leurs propres messages mis en quarantaine du courrier indésirable. Notifications de courrier indésirable de l’utilisateur final ne peut pas être utilisées avec les stratégies appliquées à des utilisateurs ou groupes, ou à une stratégie avec des exceptions.
  
Les notifications de courrier indésirable à l'utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l'utilisateur final au cours d'une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.
  
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

1. Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de courrier indésirable**.
    
2. Sélectionnez la stratégie de filtrage du courrier indésirable pour lequel vous souhaitez activer les notifications de courrier indésirable de l’utilisateur final (elles sont désactivées par défaut).
    
3. Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**. 
    
4. Dans la boîte de dialogue, vous pouvez configurer les options suivantes :
    
1. **Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.) 
    
2. **Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place. 
    
3. **Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. 
    
5. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie de filtrage du courrier indésirable, notamment vos paramètres de notification de courrier indésirable de l’utilisateur final, s’affiche dans le volet droit.
    
> [!NOTE]
>  Notifications de courrier indésirable de l’utilisateur final ne seront fonctionnelles pour les stratégies de filtrage du courrier indésirable sont activés. > Notifications de courrier indésirable de l’utilisateur final sont envoyées uniquement une fois par jour. L’heure de remise de la notification ne peut pas être garanti pour un client spécifique et n’est pas configurable. 
  
 **Conseil :** Si vous souhaitez tester les notifications de courrier indésirable de l’utilisateur final en lui envoyant un ensemble limité d’utilisateurs avant de les implémenter entièrement, créez une stratégie de filtrage du courrier indésirable personnalisé qui permet à des notifications de courrier indésirable pour l’utilisateur final pour les domaines où résident les utilisateurs. Puis, dans le centre d’administration Exchange, sous **flux de messagerie \> règles**, créer une règle de transport pour bloquer les messages à partir de quarantine@messaging.microsoft.com (l’adresse de messagerie qui envoie des notifications) avec des exceptions pour les utilisateurs que vous souhaitez recevoir des notifications. L’image suivante est un exemple de création d’une exception pour deux utilisateurs (SaraD et AlexD) à partir du domaine Contoso.com : 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Pour plus d'informations

[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
