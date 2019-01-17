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
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="7f6c7-103">Alertes de file d’attente et des files d’attente</span><span class="sxs-lookup"><span data-stu-id="7f6c7-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="7f6c7-104">Alertes de file d’attente</span><span class="sxs-lookup"><span data-stu-id="7f6c7-104">Queue alerts</span></span>

<span data-ttu-id="7f6c7-p101">Lorsque les messages ne peuvent pas être envoyés à partir de votre organisation Office 365 à votre site ou les serveurs de messagerie de partenaire à l’aide de connecteurs, les messages sont en file d’attente dans Office 365. Des exemples courants qui provoquent cette condition sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="7f6c7-107">Le connecteur est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="7f6c7-108">Dans votre environnement local a été apportée au réseau ou d’un pare-feu.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="7f6c7-p102">Office 365 continuera d’essayer de livraison de 48 heures. Après 48 heures, les messages vont expirer et seront renvoyés à l’expéditeur dans les rapports de non-remise (également appelé une NDR ou les messages de rebond).</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="7f6c7-p103">Si le volume de courrier en file d’attente dépasse le seuil prédéfini (la valeur par défaut est 2000 messages), les alertes seront disponibles dans le tableau de bord de flux de messagerie à **l’historique des alertes**et administrateurs recevront une notification par courrier électronique (adresse e-mail sujet) . Pour configurer le seuil d’alerte, la limite quotidienne de notification et/ou destinataires de l’alerte, voir la section **alertes de file d’attente de personnaliser** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Alertes de file d’attente dans la zone alertes récents du tableau de bord de flux de messagerie dans le centre de conformité de & Office 365 sécurité](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="7f6c7-114">Personnaliser des alertes de file d’attente</span><span class="sxs-lookup"><span data-stu-id="7f6c7-114">Customize queue alerts</span></span>

<span data-ttu-id="7f6c7-p104">Détails de flux de messagerie créer une stratégie de l’alerte nommée **Messages ont été retardées** ( **Envoyer des notifications électroniques** la case dans l’exemple capture d’écran ci-dessous) trouvé dans les **alertes** \> **Stratégies d’alerte**. Vous pouvez modifier les destinataires de l’alerte et le seuil en cliquant sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Navigation alertes](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="7f6c7-118">Vous verrez une nouvelle lame d’informations de stratégie, vous pouvez cliquer sur **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Modifier la stratégie ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="7f6c7-p105">Le serveur lame informations devient la **Modifier la stratégie**. Vous pouvez maintenant modifier les destinataires du courrier électronique d’alerte, la limite du nombre de notifications envoyées par jour et le seuil minimum déclenche une alerte (200 ou plus).</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Modifier la carte de stratégie](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="7f6c7-123">Détails de l’alerte de file d’attente</span><span class="sxs-lookup"><span data-stu-id="7f6c7-123">Queue alert details</span></span>

<span data-ttu-id="7f6c7-124">Lorsque vous cliquez sur l’alerte, les détails de l’alerte s’affichent dans un volet flottant.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Sélectionnez une alerte de file d’attente dans la zone alertes récents du tableau de bord de flux de messagerie dans le centre de conformité de & sécurité pour Microsoft Office 365](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Le Lanceur de détails de l’alerte en file d’attente dans le centre de conformité de & Office 365 sécurité](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="7f6c7-127">Vous pouvez cliquer sur **file d’attente de l’affichage** dans les détails de l’alerte pour voir les détails de la file d’attente, des problèmes et des liens vers les correctifs disponibles dans un nouveau volet flottant.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Le Lanceur de détails de l’alerte en file d’attente dans le centre de conformité de & Office 365 sécurité](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![File d’attente de l’affichage dans les détails de l’alerte](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="7f6c7-130">Files d’attente</span><span class="sxs-lookup"><span data-stu-id="7f6c7-130">Queues</span></span>

<span data-ttu-id="7f6c7-p106">Même si le volume des messages en file d’attente n’a pas dépassé le seuil, vous pouvez toujours utiliser la zone **files d’attente** du tableau de bord de flux de messagerie pour afficher les messages en file d’attente au moins une heure. Vous pouvez utiliser la zone **files d’attente** pour surveiller le nombre de messages en file d’attente (la valeur 0 indique le flux de messagerie est OK) et effectuer une action avant que le nombre de messages en file d’attente devient trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="7f6c7-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Files d’attente dans le tableau de bord du flux de messagerie dans le centre de conformité de & Office 365 sécurité](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="7f6c7-134">Lorsque vous cliquez sur le nombre de messages en file d’attente dans les **files d’attente**, les détails de la file d’attente et des instructions pour corriger le problème apparaît dans un volet flottant (le Lanceur qui s’affiche lorsque vous cliquez sur **file d’attente Afficher** les détails d’une alerte de file d’attente).</span><span class="sxs-lookup"><span data-stu-id="7f6c7-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Détails de la file d’attente](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
