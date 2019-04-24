---
title: Alertes de files d’attente et files d’attente
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Les administrateurs peuvent en savoir plus sur les alertes de files d'attente et les files d'attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité.
ms.openlocfilehash: 490665bb6b062c5a0b93c988adea9eeb9827cb86
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267664"
---
# <a name="queue-alerts-and-queues"></a>Alertes de files d’attente et files d’attente

## <a name="queue-alerts"></a>Alertes de file d'attente

Lorsque des messages ne peuvent pas être envoyés de votre organisation Office 365 à vos serveurs de messagerie locaux ou partenaires à l'aide de connecteurs, les messages sont mis en file d'attente dans Office 365. Les exemples courants qui génèrent cette condition sont les suivants:

- Le connecteur est configuré de manière incorrecte.

- Des modifications de mise en réseau ou de pare-feu ont été apportées dans votre environnement local.

Office 365 continuera à nouvelle tentative de remise pendant 48 heures. Après 48 heures, les messages arriveront à expiration et seront renvoyés aux expéditeurs dans les notifications d'échec de remise (également appelées notifications de non-remise).

Si le volume de messagerie en file d'attente dépasse le seuil prédéfini (la valeur par défaut est 2000 messages), les alertes seront disponibles dans le tableau de bord du flux de messagerie dans les **alertes récentes**, et les administrateurs recevront une notification par courrier électronique (à leur adresse de messagerie alternative). . Pour configurer le seuil d'alerte, la limite de notification quotidienne et/ou les destinataires de l'alerte, consultez la section **personnaliser les alertes de file d'attente** ci-dessous.

![Alertes de file d'attente dans la zone alertes récentes du tableau de bord de flux de messagerie dans le centre de sécurité & conformité](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a>Personnaliser les alertes de file d'attente

Informations sur le flux de messagerie créer une stratégie d'alerte nommée les **messages ont été** retardées (la case à cocher **Envoyer des notifications par courrier électronique** dans la capture d'écran d'exemple ci-dessous) figurant dans **stratégies d'alerte**des **alertes** \> . Vous pouvez modifier les destinataires du seuil et des alertes en cliquant sur la stratégie.

![Navigation des alertes](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

Vous verrez une nouvelle Blade d'informations de stratégie, vous pouvez maintenant cliquer sur **modifier la stratégie**.

![Modifier la stratégie ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

Le panneau d'informations passe à la **stratégie de modification**. Vous pouvez désormais modifier les destinataires du message d'alerte, la limite du nombre de notifications envoyées par jour et le seuil minimal de déclenchement de l'alerte (200 ou plus).

![Modifier la Blade de stratégie](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a>Détails des alertes en file d'attente

Lorsque vous cliquez sur l'alerte, les détails de l'alerte s'affichent dans un volet flyout.

![Sélectionnez une alerte de file d'attente dans la zone alertes récentes du tableau de bord de flux de messagerie dans le centre de sécurité & conformité](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Fenêtre mobile des détails des alertes de la file d'attente dans le centre de sécurité & conformité](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

Vous pouvez cliquer sur **afficher la file d'attente** dans les détails de l'alerte pour voir les détails de la file d'attente, les problèmes et les liens vers les correctifs disponibles dans un nouveau volet flyout.

![Fenêtre mobile des détails des alertes de la file d'attente dans le centre de sécurité & conformité](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Afficher la file d'attente dans les détails de l'alerte](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a>Files d’attente

Même si le volume des messages mis en file d'attente n'a pas dépassé le seuil, vous pouvez toujours utiliser la zone **files d'attente** du tableau de bord du flux de messagerie pour afficher les messages qui ont été mis en file d'attente pendant plus d'une heure. Vous pouvez utiliser la zone **files d'attente** pour surveiller le nombre de messages en file d'attente (la valeur 0 indique que le flux de messagerie est correct) et prendre des mesures avant que le nombre de messages en file d'attente devienne trop important.

![Files d'attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

Lorsque vous cliquez sur le nombre de messages en file d'attente dans les **files d'attente**, les détails de la file d'attente et des instructions sur la résolution du problème apparaissent dans un volet flyout (le même menu volant qui s'affiche une fois que vous avez cliqué sur **afficher la file d'attente** dans les détails d'une alerte de file d'attente).

![Détails de la file d'attente](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="see-also"></a>Voir aussi

Pour plus d'informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights.md).
