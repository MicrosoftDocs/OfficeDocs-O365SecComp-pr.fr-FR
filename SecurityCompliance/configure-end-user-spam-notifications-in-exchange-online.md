---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Vous pouvez configurer les notifications de courrier indésirable de l’utilisateur final pour la stratégie de filtrage du courrier indésirable de l’entreprise par défaut ou les stratégies de filtrage anti-spam personnalisés qui sont appliqués aux domaines.
ms.openlocfilehash: 4a4c7c6b139fe0f8b0a1f6b69c1b95e321293af5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027531"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="945fa-103">Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="945fa-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="945fa-p101">Cette rubrique est pour les clients Exchange Online qui protègent les boîtes aux lettres hébergées sur le cloud. Les clients autonomes Exchange Online Protection (EOP) qui sont protection des boîtes aux lettres locales doivent lire la rubrique suivante au lieu de cela : [configuration de notifications de courrier indésirable pour l’utilisateur final dans EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="945fa-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="945fa-p102">Vous pouvez configurer les notifications de courrier indésirable de l’utilisateur final pour la stratégie de filtrage du courrier indésirable de l’entreprise par défaut ou les stratégies de filtrage anti-spam personnalisés qui sont appliqués aux domaines. Activation des messages de notification de courrier indésirable de l’utilisateur final permet à vos utilisateurs finaux de gérer eux-mêmes leurs propres messages mis en quarantaine du courrier indésirable. Notifications de courrier indésirable de l’utilisateur final ne peut pas être utilisées avec les stratégies appliquées à des utilisateurs ou groupes, ou à une stratégie avec des exceptions.</span><span class="sxs-lookup"><span data-stu-id="945fa-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="945fa-p103">Les notifications de courrier indésirable à l'utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l'utilisateur final au cours d'une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.</span><span class="sxs-lookup"><span data-stu-id="945fa-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="945fa-111">Une fois que les utilisateurs finaux ont reçu un message de notification, ils peuvent cliquer pour déplacer un message indésirable vers leur boîte de réception ou le signaler comme Légitime, auquel cas il sera envoyé à l'équipe d'analyse de courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="945fa-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="945fa-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="945fa-112">What do you need to know before you begin?</span></span>

<span data-ttu-id="945fa-113">Durée d'exécution estimée : 2 minutes</span><span class="sxs-lookup"><span data-stu-id="945fa-113">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="945fa-p104">Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée « Anti-spam » dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="945fa-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="945fa-116">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="945fa-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="945fa-117">Utiliser le Centre d'administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="945fa-117">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="945fa-118">Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="945fa-118">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="945fa-119">Sélectionnez la stratégie de filtrage du courrier indésirable pour lequel vous souhaitez activer les notifications de courrier indésirable de l’utilisateur final (elles sont désactivées par défaut).</span><span class="sxs-lookup"><span data-stu-id="945fa-119">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="945fa-120">Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**.</span><span class="sxs-lookup"><span data-stu-id="945fa-120">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="945fa-121">Dans la boîte de dialogue, vous pouvez configurer les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="945fa-121">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="945fa-p105">**Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.)</span><span class="sxs-lookup"><span data-stu-id="945fa-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="945fa-p106">**Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place.</span><span class="sxs-lookup"><span data-stu-id="945fa-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="945fa-128">**Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="945fa-128">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="945fa-p107">Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie de filtrage du courrier indésirable, notamment vos paramètres de notification de courrier indésirable de l’utilisateur final, s’affiche dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="945fa-p107">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="945fa-p108">Notifications de courrier indésirable de l’utilisateur final ne seront fonctionnelles pour les stratégies de filtrage du courrier indésirable sont activés. > Notifications de courrier indésirable de l’utilisateur final sont envoyées uniquement une fois par jour. L’heure de remise de la notification ne peut pas être garanti pour un client spécifique et n’est pas configurable.</span><span class="sxs-lookup"><span data-stu-id="945fa-p108">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="945fa-p109">**Conseil :** Si vous souhaitez tester les notifications de courrier indésirable de l’utilisateur final en lui envoyant un ensemble limité d’utilisateurs avant de les implémenter entièrement, créez une stratégie de filtrage du courrier indésirable personnalisé qui permet à des notifications de courrier indésirable pour l’utilisateur final pour les domaines où résident les utilisateurs. Puis, dans le centre d’administration Exchange, sous **flux de messagerie \> règles**, créer une règle de transport pour bloquer les messages à partir de quarantine@messaging.microsoft.com (l’adresse de messagerie qui envoie des notifications) avec des exceptions pour les utilisateurs que vous souhaitez recevoir des notifications. L’image suivante est un exemple de création d’une exception pour deux utilisateurs (SaraD et AlexD) à partir du domaine Contoso.com :</span><span class="sxs-lookup"><span data-stu-id="945fa-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="945fa-138">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="945fa-138">For more information</span></span>

[<span data-ttu-id="945fa-139">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="945fa-139">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
