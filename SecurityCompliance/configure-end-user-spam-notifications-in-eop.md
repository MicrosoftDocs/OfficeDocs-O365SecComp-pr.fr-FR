---
title: Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP
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
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: Vous pouvez configurer les notifications de courrier indésirable à l'utilisateur final pour la stratégie de filtrage de contenu par défaut à l'échelle de l'entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines.
ms.openlocfilehash: 2cab65347c726cab482eb127f5068586f4f3afd3
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222973"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="691d2-103">Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP</span><span class="sxs-lookup"><span data-stu-id="691d2-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="691d2-p101">Cette rubrique est destinée aux clients autonomes Exchange Online Protection (EOP) qui protègent les boîtes aux lettres locales. Les clients Exchange Online qui protègent les boîtes aux lettres hébergées dans le Cloud doivent plutôt lire la rubrique suivante: [configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="691d2-p101">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes. Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="691d2-p102">Vous pouvez configurer les notifications de courrier indésirable pour l’utilisateur final pour la stratégie de filtrage de contenu par défaut à l’échelle de l’entreprise, ou pour les stratégies de filtrage de contenu personnalisées appliquées à des domaines. L’activation des notifications de courrier indésirable à l’utilisateur final permet à vos utilisateurs de gérer eux-mêmes leurs propres messages de courrier indésirable mis en quarantaine. La fonctionnalité ne peut pas être utilisée avec les stratégies appliquées à des utilisateurs ou des groupes, ou à une stratégie comportant des exceptions.</span><span class="sxs-lookup"><span data-stu-id="691d2-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="691d2-p103">Les notifications de courrier indésirable à l’utilisateur final contiennent la liste de tous les messages de courrier indésirable mis en quarantaine reçus par l’utilisateur final au cours d’une période que vous configurez (vous pouvez spécifier une valeur comprise entre 1 et 15 jours). Vous pouvez également configurer la langue dans laquelle est écrit le message de notification.</span><span class="sxs-lookup"><span data-stu-id="691d2-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="691d2-111">Après la réception d'un message de notification, les utilisateurs finaux peuvent choisir l'une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="691d2-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="691d2-112">**Affichez un aperçu** du message si vous souhaitez afficher un aperçu du contenu ou de l'en-tête avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="691d2-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="691d2-113">**Téléchargez** le message si vous souhaitez consulter le message et les pièces jointes (le cas échéant) sur votre appareil avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="691d2-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="691d2-114">**Release** si le message n'est pas un courrier indésirable et que vous souhaitez qu'Office 365 envoie le message à votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="691d2-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="691d2-p104">**Release _AMP_ autoriser l'expéditeur** si le message n'est pas un courrier indésirable et que vous voulez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs et destinataires approuvés pour les futurs courriers électroniques. Gardez à l'esprit que votre administrateur peut avoir d'autres configurations autoriser/bloquer des organisations qui remplacent votre liste d'expéditeurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="691d2-p104">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails. Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="691d2-117">**Release _AMP_ Report**, si le message n'est pas indésirable et que vous voulez envoyer le message à votre boîte aux lettres et le signaler à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="691d2-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="691d2-118">**Bloquer** si vous souhaitez qu'Office 365 ajoute l'expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="691d2-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="691d2-119">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="691d2-119">What do you need to know before you begin?</span></span>
<span data-ttu-id="691d2-120"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="691d2-120"></span></span>

<span data-ttu-id="691d2-121">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="691d2-121">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="691d2-p105">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Blocage du courrier indésirable » dans la rubrique [Autorisations des fonctionnalités dans EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="691d2-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](eop/feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="691d2-124">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="691d2-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="691d2-125">Utiliser le Centre d'administration Exchange (CAE) pour configurer les notifications de courrier indésirable à l'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="691d2-125">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="691d2-126">Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de contenu**.</span><span class="sxs-lookup"><span data-stu-id="691d2-126">In the Exchange admin center (EAC), navigate to **Protection** \> **Content filter**.</span></span>
    
2. <span data-ttu-id="691d2-127">Sélectionnez la stratégie de filtrage de contenu pour laquelle vous voulez activer les notifications de courrier indésirable à l'utilisateur final (elles sont désactivées par défaut).</span><span class="sxs-lookup"><span data-stu-id="691d2-127">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="691d2-128">Dans le volet de droite, dans lequel apparaissent des informations récapitulatives sur votre stratégie, cliquez sur le lien **Configurer les notifications de courrier indésirable à l'utilisateur final**.</span><span class="sxs-lookup"><span data-stu-id="691d2-128">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="691d2-129">Dans la boîte de dialogue, vous pouvez configurer les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="691d2-129">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="691d2-p106">**Activer les notifications de courrier indésirable à l'utilisateur final** Cochez cette case pour activer les notifications de courrier indésirable à l'utilisateur final pour cette stratégie. (À l'inverse, si la stratégie est activée, vous pouvez décocher cette case pour désactiver les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.)</span><span class="sxs-lookup"><span data-stu-id="691d2-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="691d2-p107">**Envoyer des notifications de courrier indésirable à l'utilisateur final tous les (jours)** Spécifiez la fréquence d'envoi des notifications de courrier indésirable à l'utilisateur final. La valeur par défaut est 3 jours. Vous pouvez indiquer une valeur comprise entre 1 et 15 jours. Par exemple, si vous spécifiez 7 jours, la notification inclura la liste de tous les messages destinés à cet utilisateur au cours des 7 derniers jours qui ont été mis en quarantaine à la place.</span><span class="sxs-lookup"><span data-stu-id="691d2-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="691d2-136">**Langue de la notification** Dans la liste déroulante, sélectionnez la langue dans laquelle écrire les notifications de courrier indésirable à l'utilisateur final pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="691d2-136">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="691d2-p108">Cliquez sur **Enregistrer**. Un récapitulatif de vos paramètres de stratégie de filtrage de contenu, y compris vos paramètres de notification de courrier indésirable à l'utilisateur final, apparaît dans le volet de droite.</span><span class="sxs-lookup"><span data-stu-id="691d2-p108">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="691d2-p109">Les notifications de courrier indésirable à l'utilisateur final ne sont opérationnelles que pour les stratégies de filtrage de contenu activées. >  Les notifications de courrier indésirable pour l'utilisateur final sont envoyées uniquement une fois par jour. Le délai de remise de la notification ne peut pas être garanti pour chaque client et n'est pas configurable.</span><span class="sxs-lookup"><span data-stu-id="691d2-p109">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="691d2-p110">**Conseil :** si vous voulez tester les notifications de courrier indésirable destinées aux utilisateurs finals en les envoyant à un ensemble limité d'utilisateurs avant de les implémenter totalement, créez une stratégie de filtrage de contenu personnalisée autorisant ces notifications de courrier indésirable pour les domaines dans lesquels les utilisateurs résident. Ensuite, dans le CAE, sous **Flux de messagerie \> Règles**, créez une règle de transport permettant de bloquer les messages provenant de quarantine@messaging.microsoft.com (l'adresse de messagerie qui envoie les notifications) avec des exceptions pour les utilisateurs qui doivent recevoir les notifications. L'image suivante représente un exemple de création d'exception pour deux utilisateurs (SaraD et AlexD) du domaine Contoso.com :</span><span class="sxs-lookup"><span data-stu-id="691d2-p110">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Règle de transport pour tester les notifications de courrier indésirable de l'utilisateur final](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="691d2-146">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="691d2-146">For more information</span></span>

[<span data-ttu-id="691d2-147">Configuration de vos stratégies de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="691d2-147">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
