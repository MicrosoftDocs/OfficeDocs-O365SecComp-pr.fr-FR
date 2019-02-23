---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
ms.collection:
- M365-security-compliance
description: Vous pouvez configurer les notifications de courrier indésirable de l'utilisateur final pour la stratégie de filtrage du courrier indésirable par défaut à l'échelle de l'entreprise ou pour les stratégies de filtrage du courrier indésirable personnalisées appliquées
ms.openlocfilehash: ea2994a3f772b407a35be2d64e8afcc639d24f31
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214494"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="bec78-103">Configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="bec78-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bec78-p101">Cette rubrique est destinée aux clients Exchange Online qui protègent les boîtes aux lettres hébergées dans le Cloud. Les clients autonomes Exchange Online Protection (EOP) qui protègent les boîtes aux lettres locales doivent plutôt lire la rubrique suivante: [configurer les notifications de courrier indésirable de l'utilisateur final dans EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="bec78-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="bec78-p102">Vous pouvez configurer les notifications de courrier indésirable de l'utilisateur final pour la stratégie de filtrage du courrier indésirable par défaut à l'échelle de l'entreprise ou pour les stratégies de filtrage du courrier indésirable personnalisées appliquées L'activation des messages de notification de courrier indésirable de l'utilisateur final permet aux utilisateurs finaux de gérer eux-mêmes leurs messages de courrier indésirable mis en quarantaine. Les notifications de courrier indésirable de l'utilisateur final ne peuvent pas être utilisées avec des stratégies appliquées à des utilisateurs ou à des groupes, ou à une stratégie avec des exceptions.</span><span class="sxs-lookup"><span data-stu-id="bec78-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="bec78-p103">Les notifications de courrier indésirable à l'utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l'utilisateur final au cours d'une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.</span><span class="sxs-lookup"><span data-stu-id="bec78-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="bec78-111">Après la réception d'un message de notification, les utilisateurs finaux peuvent choisir l'une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="bec78-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="bec78-112">**Affichez un aperçu** du message si vous souhaitez afficher un aperçu du contenu ou de l'en-tête avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="bec78-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="bec78-113">**Téléchargez** le message si vous souhaitez consulter le message et les pièces jointes (le cas échéant) sur votre appareil avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="bec78-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="bec78-114">**Release** si le message n'est pas un courrier indésirable et que vous souhaitez qu'Office 365 envoie le message à votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bec78-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="bec78-p104">**Release _AMP_ autoriser l'expéditeur** si le message n'est pas un courrier indésirable et que vous voulez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs et destinataires approuvés pour les futurs courriers électroniques. Gardez à l'esprit que votre administrateur peut avoir d'autres configurations autoriser/bloquer des organisations qui remplacent votre liste d'expéditeurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="bec78-p104">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails. Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="bec78-117">**Release _AMP_ Report**, si le message n'est pas indésirable et que vous voulez envoyer le message à votre boîte aux lettres et le signaler à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="bec78-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="bec78-118">**Bloquer** si vous souhaitez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="bec78-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="bec78-119">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="bec78-119">What do you need to know before you begin?</span></span>

<span data-ttu-id="bec78-120">Durée d'exécution estimée : 2 minutes</span><span class="sxs-lookup"><span data-stu-id="bec78-120">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="bec78-p105">Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée «blocage du courrier indésirable» dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bec78-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="bec78-123">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="bec78-123">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="bec78-124">Utiliser le Centre d'administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="bec78-124">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="bec78-125">Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="bec78-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="bec78-126">Sélectionnez la stratégie de filtrage du courrier indésirable pour laquelle vous souhaitez activer les notifications de courrier indésirable pour l'utilisateur final (elles sont désactivées par défaut).</span><span class="sxs-lookup"><span data-stu-id="bec78-126">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="bec78-127">Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**.</span><span class="sxs-lookup"><span data-stu-id="bec78-127">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="bec78-128">Dans la boîte de dialogue, vous pouvez configurer les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="bec78-128">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="bec78-p106">**Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.)</span><span class="sxs-lookup"><span data-stu-id="bec78-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="bec78-p107">**Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place.</span><span class="sxs-lookup"><span data-stu-id="bec78-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="bec78-135">**Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="bec78-135">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="bec78-p108">Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie de filtrage du courrier indésirable, y compris les paramètres de notification de courrier indésirable de l'utilisateur final, apparaît dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="bec78-p108">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="bec78-p109">Les notifications de courrier indésirable de l'utilisateur final ne seront fonctionnelles que pour les stratégies de filtrage du courrier indésirable activées. > les notifications de courrier indésirable de l'utilisateur final sont envoyées uniquement une fois par jour. Le délai de remise de la notification ne peut pas être garanti pour un client spécifique et n'est pas configurable.</span><span class="sxs-lookup"><span data-stu-id="bec78-p109">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="bec78-p110">**Conseil:** Si vous souhaitez tester les notifications de courrier indésirable de l'utilisateur final en les envoyant à un ensemble limité d'utilisateurs avant de les implémenter complètement, créez une stratégie de filtrage du courrier indésirable personnalisée qui active les notifications de courrier indésirable à l'utilisateur final pour les domaines dans lesquels les utilisateurs résident. Ensuite, dans le centre d'administration Exchange, sous **règles de flux \> de messagerie**, créez une règle de transport pour bloquer les messages de Quarantine@messaging.microsoft.com (l'adresse de messagerie qui envoie les notifications) avec des exceptions pour les utilisateurs qui doivent recevoir les notifications. L'image suivante est un exemple de création d'une exception pour deux utilisateurs (Sarad et alexd) du domaine Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="bec78-p110">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="bec78-145">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="bec78-145">For more information</span></span>

[<span data-ttu-id="bec78-146">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="bec78-146">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
