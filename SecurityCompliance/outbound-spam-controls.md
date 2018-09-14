---
title: Contrôle du courrier indésirable sortant dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: Si votre organisation envoie un grand nombre de courrier en nombre qui a été marqué comme courrier indésirable, vous pourriez être bloqué à partir de l’envoi de courrier électronique avec Office 365. Lisez cet article pour en savoir plus sur ce comportement et ce que vous pouvez faire parler.
ms.openlocfilehash: 916a062d08e01954e7736b6f22d297aea04baf28
ms.sourcegitcommit: 17dda7ece5c9e884944a92ac0f842cf1e62ec506
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "23977579"
---
# <a name="controlling-outbound-spam-in-office-365"></a>Contrôle du courrier indésirable sortant dans Office 365

Nous prenons la gestion du courrier indésirable sortant sérieusement, car nous sont un service partagé.  Il existe de nombreux clients derrière un pool partagé de ressources, où si un client envoie un courrier indésirable sortant, il peut nuire à la réputation d’IP sortante du service et affecte la remise réussie du courrier électronique pour les autres clients. Il est tranchée au client A client B véhiculés et différents noires IP 3ème partie liste l’adresse IP qu’il utilise.

## <a name="what-admins-can-do-to-control-outbound-spam"></a>Les administrateurs peuvent faire à contrôler le courrier indésirable sortant

- **Activer les notifications lors de l’envoi de courrier indésirable est un compte ou d’arrêter**. Les administrateurs peuvent obtenir en copie carbone cachée chaque fois qu’un message est marqué comme courrier indésirable sortant et envoyé par le biais du pool risque élevé. En surveillant cette boîte aux lettres, un administrateur peut détecter si elles ont un compte compromis dans leur réseau ou si le filtre de courrier indésirable est marquage par erreur leur messagerie électronique comme courrier indésirable.  Vous pouvez trouver plus d’informations sur la configuration de la stratégie de courrier indésirable sortant [ici](configure-the-outbound-spam-policy.md).
 
- **Passer en revue manuellement réclamations fournisseurs de messagerie 3ème partie du courrier indésirable**. De nombreux services de messagerie tiers 3e tels que Outlook.com, Yahoo! et AOL fournissent une boucle de commentaires où si tous les utilisateurs de leur service marque un message électronique à partir de notre service comme courrier indésirable, le message est préparé et envoyé à nous pour révision. Pour en savoir plus sur la prise en charge de l’expéditeur pour Outlook.com, cliquez [ici](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).

## <a name="what-eop-does-to-control-outbound-spam"></a>Ce que fait EOP pour contrôler le courrier indésirable sortant 

1. **Séparation du trafic sortant dans des pools distincts d’adresses IP**. Chaque message clients envoient sortants via le service est analysé pour le courrier indésirable. Si le message est le courrier indésirable, il est acheminé via le pool de remise de risque élevé. Ce pool IP contient le courrier indésirable et les notifications d’état non remis. Remise au destinataire n’est pas garanti que nombreux tiers n’accepte pas courrier électronique, car la qualité des courriers électroniques, il émet.

Fractionnement du trafic de cette manière garantit que l’e-mail qualité inférieure (spam, rapports de non-remise RÉTRODIFFUSION) ne pas glisser vers le bas la réputation des pools régulièrement du courrier sortant. Le risque élevé du pool est généralement réputation faible à plusieurs destinataires autour d’Internet, bien que cela ne soit pas universel. 

2. **Réputation d’IP de surveillance**. Office 365 interroge différentes noires d’IP tiers 3e et génère des alertes si un des nos IP sortant sont répertorié dans les. Cela nous permet de réagir rapidement lorsque le courrier indésirable a provoqué notre réputation à se dégrader. Lorsqu’une alerte est générée, nous avons documentation interne excentrée les étapes à suivre pour obtenir delisted. 

3. **Désactivation de comptes incriminées lorsqu’ils envoient trop courrier marqué comme courrier indésirable**. Même si nous séparer notre du courrier indésirable et les légitimes dans deux pools distincts d’IP sortants, les comptes de messagerie ne peuvent pas envoyer du courrier indésirable indéfiniment. Nous surveiller dont les comptes sont l’envoi du courrier indésirable et s’il dépasse une limite divulguer, le compte est bloqué à partir de l’envoi du courrier indésirable.

Un seul message marqué comme courrier indésirable peut être une erreur de classement par le moteur de courrier indésirable et également appelé un faux positif. Nous envoyer via le pool risque élevé à l’occasion de sortir ; Toutefois, un grand nombre de messages dans un court délai est indicatif d’un problème et qui se produit, nous bloquer le compte d’envoyer les messages plus. Il existe différents seuils qui existent pour les comptes de messagerie individuelles ainsi comme agrégat pour le client entière.

4. **Désactivation de comptes incriminées lorsqu’ils envoient trop courrier dans trop court un laps de temps**. Outre les limites ci-dessus recherchent une proportion des messages marqués comme courrier indésirable, il existe des limites qui bloquent les comptes lorsqu’ils atteignent une limite globale, quel que soit ou non les messages sont marqués comme courrier indésirable. La raison pour laquelle qu'il existe cette limite est, car un compte compromis peut envoyer du courrier indésirable zéro jour qui n’est pas respectée par le filtre de courrier indésirable. Car il est difficile, voire impossible, parfois indiquer la différence entre une campagne de publipostage légitime et une campagne de spam massive, ces limites activer pour limiter les dommages potentiels.

> [!NOTE]
> #3 et 4 #, nous ne pas publier les limites exactes.  Il s’agit afin d’éviter les expéditeurs de courrier indésirable à partir du système de jeu et pour s’assurer que nous pouvons modifier les limites lorsque nous devons. Les limites sont suffisamment élevé tels qu’un utilisateur d’entreprise ne sera jamais atteint les et suffisamment faible pour qu’il contient la plupart des dommages que spammeur peut faire. 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a>Solutions recommandées pour les clients qui souhaitent dans l’envoi d’un grand nombre de courriers électroniques via EOP

Il est difficile de trouver un équilibre entre les clients qui souhaitent envoyer un volume important de courrier électronique et la protection du service de comptes compromis et emailers en bloc avec les pratiques d’acquisition de liste médiocre. Là encore, le coût d’une IP sortant d’arrivée sur une liste de blocage 3ème partie est supérieur du blocage d’un client d’envoyer des messages électroniques sortants. Comme décrit dans la [Description du Service Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits), à l’aide d’EOP pour envoyer des messages électroniques en masse n’est pas pris en charge utilisez du service et n’est autorisée sur une base « au mieux ». Pour les clients qui ne souhaitent pas envoyer de messages électroniques en masse, nous vous recommandons les éléments suivants :

a. **Envoyer les messages électroniques en masse par le biais de ses serveurs de messagerie sur site**. Cela signifie que le client devra mettre à jour sa propre infrastructure de messagerie pour ce type de courrier électronique.

b. **emailer d’en bloc utiliser un 3ème partie pour envoyer la communication de masse**. Il existe plusieurs emailers d’en bloc partie 3 dont l’activité exclusive il consiste à envoyer des messages électroniques en masse. Ils peuvent travailler avec les clients pour vous assurer qu’ils disposent des bonnes pratiques e-mail et qu’ils disposent de ressources dédiées à appliquer. 

La messagerie, Mobile, les logiciels malveillants anti-abus groupe de travail (MAAWG) publie une liste de son appartenance [ici](http://www.maawg.org/about/roster). Plusieurs fournisseurs de messagerie en bloc figurant dans la liste et connues pour être chargés citoyens Internet. 
  
## <a name="for-more-information"></a>Pour plus d’informations

[Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)

[Protection contre l’usurpation dans Office 365](anti-spoofing-protection.md)

[Seuils de probabilité de courrier indésirable](spam-confidence-levels.md)
