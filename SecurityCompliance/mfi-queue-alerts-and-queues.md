---
title: Alertes de file d’attente et des files d’attente
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Administrateurs peuvent en savoir plus sur les alertes de file d’attente et des files d’attente dans le tableau de bord du flux de messagerie dans le centre de conformité de & Office 365 sécurité.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685425"
---
# <a name="queue-alerts-and-queues"></a>Alertes de file d’attente et des files d’attente

## <a name="queue-alerts"></a>Alertes de file d’attente

Lorsque les messages ne peuvent pas être envoyés à partir de votre organisation Office 365 à votre site ou les serveurs de messagerie de partenaire à l’aide de connecteurs, les messages sont en file d’attente dans Office 365. Des exemples courants qui provoquent cette condition sont les suivants :

- Le connecteur est correctement configuré.

- Dans votre environnement local a été apportée au réseau ou d’un pare-feu.

Office 365 continuera d’essayer de livraison de 48 heures. Après 48 heures, les messages vont expirer et seront renvoyés à l’expéditeur dans les rapports de non-remise (également appelé une NDR ou les messages de rebond).

Si le volume de courrier en file d’attente dépasse le seuil prédéfini (la valeur par défaut est 2000 messages), les alertes seront disponibles dans le tableau de bord de flux de messagerie à **l’historique des alertes**et administrateurs recevront une notification par courrier électronique (adresse e-mail sujet) . Pour configurer le seuil d’alerte, la limite quotidienne de notification et/ou destinataires de l’alerte, voir la section **alertes de file d’attente de personnaliser** ci-dessous.

![Alertes de file d’attente dans la zone alertes récents du tableau de bord de flux de messagerie dans le centre de conformité de & Office 365 sécurité](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a>Personnaliser des alertes de file d’attente

Détails de flux de messagerie créer une stratégie de l’alerte nommée **Messages ont été retardées** ( **Envoyer des notifications électroniques** la case dans l’exemple capture d’écran ci-dessous) trouvé dans les **alertes** \> **Stratégies d’alerte**. Vous pouvez modifier les destinataires de l’alerte et le seuil en cliquant sur la stratégie.

![Navigation alertes](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

Vous verrez une nouvelle lame d’informations de stratégie, vous pouvez cliquer sur **Modifier la stratégie**.

![Modifier la stratégie ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

Le serveur lame informations devient la **Modifier la stratégie**. Vous pouvez maintenant modifier les destinataires du courrier électronique d’alerte, la limite du nombre de notifications envoyées par jour et le seuil minimum déclenche une alerte (200 ou plus).

![Modifier la carte de stratégie](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a>Détails de l’alerte de file d’attente

Lorsque vous cliquez sur l’alerte, les détails de l’alerte s’affichent dans un volet flottant.

![Sélectionnez une alerte de file d’attente dans la zone alertes récents du tableau de bord de flux de messagerie dans le centre de conformité de & sécurité pour Microsoft Office 365](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Le Lanceur de détails de l’alerte en file d’attente dans le centre de conformité de & Office 365 sécurité](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

Vous pouvez cliquer sur **file d’attente de l’affichage** dans les détails de l’alerte pour voir les détails de la file d’attente, des problèmes et des liens vers les correctifs disponibles dans un nouveau volet flottant.

![Le Lanceur de détails de l’alerte en file d’attente dans le centre de conformité de & Office 365 sécurité](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![File d’attente de l’affichage dans les détails de l’alerte](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a>Files d’attente

Même si le volume des messages en file d’attente n’a pas dépassé le seuil, vous pouvez toujours utiliser la zone **files d’attente** du tableau de bord de flux de messagerie pour afficher les messages en file d’attente au moins une heure. Vous pouvez utiliser la zone **files d’attente** pour surveiller le nombre de messages en file d’attente (la valeur 0 indique le flux de messagerie est OK) et effectuer une action avant que le nombre de messages en file d’attente devient trop volumineux.

![Files d’attente dans le tableau de bord du flux de messagerie dans le centre de conformité de & Office 365 sécurité](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

Lorsque vous cliquez sur le nombre de messages en file d’attente dans les **files d’attente**, les détails de la file d’attente et des instructions pour corriger le problème apparaît dans un volet flottant (le Lanceur qui s’affiche lorsque vous cliquez sur **file d’attente Afficher** les détails d’une alerte de file d’attente).

![Détails de la file d’attente](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
