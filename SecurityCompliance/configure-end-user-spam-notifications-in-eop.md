---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: Vous pouvez configurer les notifications de courrier indésirable à l'utilisateur final pour la stratégie de filtrage de contenu par défaut à l'échelle de l'entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines.
ms.openlocfilehash: 09ddd7fd2800e4038e354e53da53320184da3e77
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692573"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a>Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP
  
> [!IMPORTANT]
> Cette rubrique s'adresse aux clients autonomes Exchange Online Protection (EOP) qui protègent les boîtes aux lettres sur site. Les clients Exchange Online qui protègent les boîtes aux lettres hébergées dans le Cloud doivent plutôt lire la rubrique suivante: [configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
Vous pouvez configurer les notifications de courrier indésirable à l'utilisateur final pour la stratégie de filtrage de contenu par défaut à l'échelle de l'entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines. L'activation des notifications de courrier indésirable à l'utilisateur final permet à vos utilisateurs de gérer eux-mêmes leurs propres messages de courrier indésirable mis en quarantaine. La fonctionnalité ne peut pas être utilisée avec les stratégies appliquées à des utilisateurs ou des groupes, ou à une stratégie comportant des exceptions.
  
Les notifications de courrier indésirable à l'utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l'utilisateur final au cours d'une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.
  
Après la réception d'un message de notification, les utilisateurs finaux peuvent choisir l'une des options suivantes:

**Affichez un aperçu** du message si vous souhaitez afficher un aperçu du contenu ou de l'en-tête avant de prendre une mesure.

**Téléchargez** le message si vous souhaitez consulter le message et les pièces jointes (le cas échéant) sur votre appareil avant de prendre une mesure.

**Release** si le message n'est pas un courrier indésirable et que vous souhaitez qu'Office 365 envoie le message à votre boîte aux lettres.

**Release _AMP_ autoriser l'expéditeur** si le message n'est pas un courrier indésirable et que vous voulez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs et destinataires approuvés pour les futurs courriers électroniques. Gardez à l'esprit que votre administrateur peut avoir d'autres configurations autoriser/bloquer des organisations qui remplacent votre liste d'expéditeurs autorisés.

**Release _AMP_ Report**, si le message n'est pas indésirable et que vous voulez envoyer le message à votre boîte aux lettres et le signaler à Microsoft pour analyse.

**Bloquer** si vous souhaitez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs bloqués.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer
<a name="sectionSection0"> </a>

Durée d'exécution estimée : 5 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Blocage du courrier indésirable » dans la rubrique [Autorisations des fonctionnalités dans EOP](eop/feature-permissions-in-eop.md). 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a>Utiliser le Centre d’administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l’utilisateur final

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
  
 **Conseil :** si vous voulez tester les notifications de courrier indésirable destinées aux utilisateurs finals en les envoyant à un ensemble limité d'utilisateurs avant de les implémenter totalement, créez une stratégie de filtrage de contenu personnalisée autorisant ces notifications de courrier indésirable pour les domaines dans lesquels les utilisateurs résident. Ensuite, dans le centre d'administration Exchange, sous **règles de flux \> de messagerie**, créez une règle de flux de messagerie (également appelée règle de transport) pour bloquer les messages de Quarantine@messaging.microsoft.com (adresse de messagerie qui envoie des notifications) avec des exceptions pour les utilisateurs de votre choix. pour recevoir les notifications. L'image suivante représente un exemple de création d'exception pour deux utilisateurs (SaraD et AlexD) du domaine Contoso.com : 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a>Pour plus d'informations

[Configurer vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
