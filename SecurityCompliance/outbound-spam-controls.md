---
title: Contrôle du courrier indésirable sortant dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Si votre organisation envoie un grand nombre de messages marqués comme courrier indésirable, vous pouvez être bloqué pour l’envoi de messages électroniques avec Office 365. Lisez cet article pour en savoir plus sur les raisons de cette situation et sur ce que vous pouvez faire.
ms.openlocfilehash: 09aa71cd8b273a3235bc2673d3d17c3decf71da5
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601131"
---
# <a name="controlling-outbound-spam-in-office-365"></a>Contrôle du courrier indésirable sortant dans Office 365

Nous prévoyons la gestion du courrier indésirable sortant, car le nôtre est un service partagé.  Il existe de nombreux clients derrière un pool de ressources partagé, où si un client envoie du courrier indésirable sortant, il peut dégrader la réputation IP sortante du service et affecte la remise des messages électroniques pour d’autres clients.

> [!IMPORTANT]
> La notification d’un expéditeur restreint fait désormais partie de la plateforme d’alerte SCC (Security & Compliance Center). Au lieu d’utiliser les méthodes décrites ci-dessous pour envoyer des notifications, la liste des utilisateurs à alerter se trouve dans l’alerte «utilisateur restreint de l’envoi de courrier électronique». Commencez à utiliser la [page stratégies d’alerte](https://sip.protection.office.com/alertpolicies) dans le centre de sécurité & conformité pour configurer l’alerte, car la méthode précédente sera supprimée à l’avenir. Découvrez la nouvelle [expérience utilisateur restreint](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/removing-user-from-restricted-users-portal-after-spam). "

## <a name="what-admins-can-do-to-control-outbound-spam"></a>Ce que les administrateurs peuvent faire pour contrôler le courrier indésirable sortant

- **Activer les notifications lorsqu’un compte envoie du courrier indésirable ou est arrêté**. Les administrateurs peuvent obtenir envoyé chaque fois qu’un message est marqué comme courrier indésirable sortant et qu’il est envoyé par le biais du pool à risque élevé. En surveillant cette boîte aux lettres, un administrateur peut détecter s’il dispose d’un compte compromis dans son réseau ou si le filtre de courrier indésirable marque par erreur son courrier électronique comme courrier indésirable.  Vous trouverez plus d’informations sur la configuration de la stratégie de courrier indésirable sortant [ici](configure-the-outbound-spam-policy.md).
 
- **Passez en revue manuellement les plaintes de courrier indésirable des fournisseurs de messagerie**tiers. De nombreux services de messagerie tiers comme Outlook.com, Yahoo et AOL fournissent une boucle de commentaires où, si un utilisateur de son service marque un e-mail de notre service comme courrier indésirable, le message est empaqueté et est renvoyé à nous pour révision. Pour en savoir plus sur la prise en charge de l’expéditeur pour Outlook.com, cliquez [ici](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).

## <a name="what-eop-does-to-control-outbound-spam"></a>Ce que EOP fait pour contrôler le courrier indésirable sortant 

1. **Répartition du trafic sortant dans des pools de systèmes d’adresses IP distincts**. Chaque message envoyé par des clients sortant via le service est analysé pour rechercher des courriers indésirables. Si le message est un courrier indésirable, il est routé via le pool de remise à haut risque. Ce pool IP contient des notifications d’état de non-remise et du courrier indésirable. La remise au destinataire concerné n’est pas garantie car un grand nombre de tiers n’accepteront pas de courrier électronique, car la qualité du courrier électronique qu’il émet.

Le fractionnement du trafic garantit ainsi que le courrier électronique de qualité inférieure (courrier indésirable, rétrodiffusion NDR) ne fait pas descendre la réputation des pools de messages sortants normaux. Le pool à risque élevé a généralement une réputation faible pour de nombreux récepteurs sur Internet, bien que ce ne soit pas universel. 

2. **Surveillance de la réputation IP**. Office 365 interroge plusieurs listes noires IP tierces et génère des alertes si l’une de nos adresses IP sortantes y est répertoriée. Cela nous permet de réagir rapidement quand le courrier indésirable a provoqué une dégradation de notre réputation. Lorsqu’une alerte est générée, nous disposons d’une documentation interne sur les étapes à suivre pour obtenir la liste dérépertoriée. 

3. **Désactivation des comptes incriminés lorsqu’ils envoient trop de courriers électroniques marqués comme courrier**indésirable. Même si nous définissons le courrier indésirable et le courrier non indésirable dans deux pools IP sortants distincts, les comptes de messagerie ne peuvent pas envoyer de courrier indésirable indéfiniment. Nous contrôlons quels comptes envoient du courrier indésirable et, s’ils dépassent une limite non divulguée, le compte ne peut pas envoyer de courrier indésirable.

Un message unique marqué comme courrier indésirable peut être incorrect par le moteur de courrier indésirable et également connu sous le nom de faux positif. Nous les envoyons via le pool à risque élevé afin de les autoriser à sortir; Toutefois, un grand nombre de messages dans un court laps de temps indique un problème et lorsque cela se produit, nous bloquons le compte de l’envoi de courriers électroniques. Il existe des seuils différents pour les comptes de messagerie, ainsi que pour l’ensemble du client.

4. **Désactivation des comptes incriminés lorsqu’ils envoient trop peu de courriers électroniques à un intervalle de temps**. Outre les limites ci-dessus, recherchent une proportion de messages marqués comme courrier indésirable, il existe également des limites qui bloquent les comptes lorsqu’ils atteignent une limite globale, que les messages soient marqués ou non comme courrier indésirable. La raison de cette limite réside dans le fait qu’un compte compromis peut envoyer du courrier indésirable nul par le filtre de courrier indésirable. Étant donné qu’il est difficile, voire impossible, de dire parfois la différence entre une campagne de publipostage légitime et une campagne de courrier indésirable massive, ces limites s’activent pour limiter les dommages potentiels.

> [!NOTE]
> Pour les #3 et les #4, nous ne publiez pas les limites exactes.  Cela permet d’empêcher les expéditeurs de courrier indésirable de jouer au système et de s’assurer que nous pouvons modifier les limites quand nous en avons besoin. Les limites sont suffisamment élevées pour qu’un utilisateur professionnel moyen ne puisse jamais s’en servir et qu’il contienne la plupart des dommages qu’un expéditeur de courrier indésirable peut faire. 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a>Solutions recommandées pour les clients qui souhaitent envoyer un grand nombre de messages sortants via EOP

Il est difficile de trouver un équilibre entre les clients qui souhaitent envoyer un grand nombre de messages électroniques et la protection du service des comptes compromis et des courriers électroniques en masse avec des pratiques d’acquisition de liste médiocres. Encore une fois, le coût d’un atterrissage sur IP sortant sur une sélection de blocage tierce est plus élevé que le blocage d’un client pour l’envoi de messages sortants. Comme décrit dans la [Description du service Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits), l’utilisation d’EOP pour envoyer des messages en masse n’est pas une utilisation prise en charge du service et n’est autorisée que sur la base du «meilleur effort». Pour les clients qui souhaitent envoyer des courriers électroniques en masse, nous vous recommandons d’effectuer les opérations suivantes:

a. **Envoyer les messages électroniques en masse via ses propres serveurs de messagerie locaux**. Cela signifie que le client devra maintenir sa propre infrastructure de messagerie pour ce type de courrier électronique.

b. **Utilisez un courrier électronique en masse tiers pour envoyer la communication de masse**. Il existe plusieurs expéditeurs de courriers électroniques en masse dont la seule entreprise est d’envoyer du courrier en nombre. Ils peuvent collaborer avec les clients pour s’assurer qu’ils disposent de bonnes pratiques en matière de messagerie et qu’ils disposent de ressources dédiées à leur application. 

Le groupe de travail de messagerie, mobile, anti-abus de programmes malveillants (MAAWG) publie sa liste d’appartenance [ici](http://www.maawg.org/about/roster). Plusieurs fournisseurs de courrier en masse figurent dans la liste et sont appelés citoyens Internet responsables. 
  
## <a name="for-more-information"></a>Pour plus d’informations

[Exemple de notification lorsqu’un expéditeur est bloqué en cas d’envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)

[Protection anti-usurpation dans Office 365](anti-spoofing-protection.md)

[Seuils de probabilité de courrier indésirable](spam-confidence-levels.md)
