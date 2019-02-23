---
title: Alertes de files d’attente et files d’attente
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Les administrateurs peuvent en savoir plus sur les alertes de files d'attente et les files d'attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & Office 365 Security.
ms.openlocfilehash: 45c03ae8d5f646c4514b19669ca83b3eac561f68
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220794"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="7a0d0-103">Alertes de files d’attente et files d’attente</span><span class="sxs-lookup"><span data-stu-id="7a0d0-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="7a0d0-104">Alertes de file d'attente</span><span class="sxs-lookup"><span data-stu-id="7a0d0-104">Queue alerts</span></span>

<span data-ttu-id="7a0d0-p101">Lorsque des messages ne peuvent pas être envoyés de votre organisation Office 365 à vos serveurs de messagerie locaux ou partenaires à l'aide de connecteurs, les messages sont mis en file d'attente dans Office 365. Les exemples courants qui génèrent cette condition sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="7a0d0-107">Le connecteur est configuré de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="7a0d0-108">Des modifications de mise en réseau ou de pare-feu ont été apportées dans votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="7a0d0-p102">Office 365 continuera à nouvelle tentative de remise pendant 48 heures. Après 48 heures, les messages arriveront à expiration et seront renvoyés aux expéditeurs dans les notifications d'échec de remise (également appelées notifications de non-remise).</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="7a0d0-p103">Si le volume de messagerie en file d'attente dépasse le seuil prédéfini (la valeur par défaut est 2000 messages), les alertes seront disponibles dans le tableau de bord du flux de messagerie dans les **alertes récentes**, et les administrateurs recevront une notification par courrier électronique (à leur adresse de messagerie alternative). . Pour configurer le seuil d'alerte, la limite de notification quotidienne et/ou les destinataires de l'alerte, consultez la section **personnaliser les alertes de file d'attente** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Mise en file d'attente des alertes dans la zone alertes récentes du tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="7a0d0-114">Personnaliser les alertes de file d'attente</span><span class="sxs-lookup"><span data-stu-id="7a0d0-114">Customize queue alerts</span></span>

<span data-ttu-id="7a0d0-p104">Informations sur le flux de messagerie créer une stratégie d'alerte nommée les **messages ont été** retardées (la case à cocher **Envoyer des notifications par courrier électronique** dans la capture d'écran d'exemple ci-dessous) figurant dans **stratégies d'alerte**des **alertes** \> . Vous pouvez modifier les destinataires du seuil et des alertes en cliquant sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Navigation des alertes](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="7a0d0-118">Vous verrez une nouvelle Blade d'informations de stratégie, vous pouvez maintenant cliquer sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Modifier la stratégie ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="7a0d0-p105">Le panneau d'informations passe à la **stratégie de modification**. Vous pouvez désormais modifier les destinataires du message d'alerte, la limite du nombre de notifications envoyées par jour et le seuil minimal de déclenchement de l'alerte (200 ou plus).</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Modifier la Blade de stratégie](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="7a0d0-123">Détails des alertes en file d'attente</span><span class="sxs-lookup"><span data-stu-id="7a0d0-123">Queue alert details</span></span>

<span data-ttu-id="7a0d0-124">Lorsque vous cliquez sur l'alerte, les détails de l'alerte s'affichent dans un volet flyout.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Sélectionnez une alerte de file d'attente dans la zone alertes récentes du tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Fenêtre mobile des détails des alertes en file d'attente dans le centre de sécurité & de sécurité Office 365](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="7a0d0-127">Vous pouvez cliquer sur **afficher la file d'attente** dans les détails de l'alerte pour voir les détails de la file d'attente, les problèmes et les liens vers les correctifs disponibles dans un nouveau volet flyout.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Fenêtre mobile des détails des alertes en file d'attente dans le centre de sécurité & de sécurité Office 365](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Afficher la file d'attente dans les détails de l'alerte](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="7a0d0-130">Files d’attente</span><span class="sxs-lookup"><span data-stu-id="7a0d0-130">Queues</span></span>

<span data-ttu-id="7a0d0-p106">Même si le volume des messages mis en file d'attente n'a pas dépassé le seuil, vous pouvez toujours utiliser la zone **files d'attente** du tableau de bord du flux de messagerie pour afficher les messages qui ont été mis en file d'attente pendant plus d'une heure. Vous pouvez utiliser la zone **files d'attente** pour surveiller le nombre de messages en file d'attente (la valeur 0 indique que le flux de messagerie est correct) et prendre des mesures avant que le nombre de messages en file d'attente devienne trop important.</span><span class="sxs-lookup"><span data-stu-id="7a0d0-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Files d'attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="7a0d0-134">Lorsque vous cliquez sur le nombre de messages en file d'attente dans les **files d'attente**, les détails de la file d'attente et des instructions sur la résolution du problème apparaissent dans un volet flyout (le même menu volant qui s'affiche une fois que vous avez cliqué sur **afficher la file d'attente** dans les détails d'une alerte de file d'attente).</span><span class="sxs-lookup"><span data-stu-id="7a0d0-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Détails de la file d'attente](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
