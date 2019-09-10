---
title: Configurer les notifications de stratégie de courrier indésirable sortant dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à modifier les paramètres de notification pour les détections de courrier indésirable sortant dans Office 365.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822514"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a><span data-ttu-id="fdef1-103">Configurer les notifications de stratégie de courrier indésirable sortant dans Office 365</span><span class="sxs-lookup"><span data-stu-id="fdef1-103">Configure outbound spam policy notifications in Office 365</span></span>

<span data-ttu-id="fdef1-104">Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l’envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="fdef1-104">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients.</span></span> <span data-ttu-id="fdef1-105">À l’instar du filtrage des messages entrants, le filtrage du courrier indésirable sortant est composé du filtrage des connexions et du filtrage du contenu, mais les paramètres du filtre sortant ne sont pas configurables.</span><span class="sxs-lookup"><span data-stu-id="fdef1-105">Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable.</span></span> <span data-ttu-id="fdef1-106">Si un message sortant est considéré comme du courrier indésirable, il est routé via le pool de remise à risque plus élevé, ce qui réduit la probabilité que le pool IP sortant normal soit ajouté à une liste rouge.</span><span class="sxs-lookup"><span data-stu-id="fdef1-106">If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span> <span data-ttu-id="fdef1-107">Si un client continue à envoyer du courrier indésirable sortant via le service, il ne sera pas autorisé à envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="fdef1-107">If a customer continues to send outbound spam through the service, they will be blocked from sending messages.</span></span>

<span data-ttu-id="fdef1-108">Bien que vous ne puissiez pas désactiver ou modifier le filtrage du courrier indésirable sortant, vous pouvez configurer les paramètres de notification de courrier indésirable sortants suivants :</span><span class="sxs-lookup"><span data-stu-id="fdef1-108">Although you can't disable or change outbound spam filtering, you can configure the following outbound spam notification settings:</span></span>

- <span data-ttu-id="fdef1-109">**Envoyer des copies des messages suspects**: ces messages sont marqués comme courrier indésirable (quelle que soit la valeur de contrôle d’accès SCL) et ne sont pas rejetés par le filtre, mais sont acheminés via le pool de remise à risque plus élevé.</span><span class="sxs-lookup"><span data-stu-id="fdef1-109">**Send copies of suspicious messages**: These messages are marked as spam (regardless of the SCL rating) and are not rejected by the filter, but are routed through the higher risk delivery pool.</span></span> <span data-ttu-id="fdef1-110">Vous pouvez utiliser le centre d’administration Exchange ou les \*\* \*\*\* applets de commande-HostedOutboundSpamFilterPolicy dans Exchange Online PowerShell ou Exchange Online Protection PowerShell pour spécifier des destinataires d’ajout pour ces messages détectés.</span><span class="sxs-lookup"><span data-stu-id="fdef1-110">You can use the Exchange admin center (EAC) or the **\*-HostedOutboundSpamFilterPolicy** cmdlets in Exchange Online PowerShell or Exchange Online Protection PowerShell to specify addition recipients for these detected messages.</span></span> <span data-ttu-id="fdef1-111">Notez que les destinataires sont ajoutés en tant que destinataires **CCI** (les champs **de** et **à** sont les expéditeurs et destinataires d’origine).</span><span class="sxs-lookup"><span data-stu-id="fdef1-111">Note that the recipients are added as **Bcc** recipients (the **From** and **To** fields are the original sender and recipient).</span></span>

- <span data-ttu-id="fdef1-112">**Envoyer des notifications lorsqu’un expéditeur est bloqué**: lorsqu’une quantité importante de courrier indésirable provient d’un utilisateur particulier, l’utilisateur est désactivé pour l’envoi de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="fdef1-112">**Send notifications when a sender is blocked**: When a significant amount of spam is coming from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="fdef1-113">Les administrateurs sont avertis par défaut, mais vous pouvez utiliser l’option l’utilisateur ne peut pas envoyer de [stratégie d’alerte](alert-policies.md) par **courrier électronique** dans le centre de conformité Office 365 Security & pour configurer des destinataires de notification supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fdef1-113">Admins are notified by default, but you can use the **User restricted from sending email** [alert policy](alert-policies.md) in the Office 365 Security & Compliance Center to configure additional notification recipients.</span></span>

  <span data-ttu-id="fdef1-114">Pour savoir à quoi ressemble cette notification, voir [Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span><span class="sxs-lookup"><span data-stu-id="fdef1-114">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="fdef1-115">Pour plus d'informations sur le mode de réactivaction, consultez la rubrique [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdef1-115">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="fdef1-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fdef1-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="fdef1-117">Durée d’exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="fdef1-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="fdef1-118">Pour ouvrir le Centre de conformité et sécurité, consultez la rubrique [Accéder au centre de conformité et sécurité d’Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fdef1-118">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="fdef1-119">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) ou [Centre d’administration Exchange dans Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="fdef1-119">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="fdef1-120">Pour ouvrir Exchange Online PowerShell, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="fdef1-120">To open Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="fdef1-121">Pour ouvrir Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="fdef1-121">To open Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="fdef1-122">Votre compte doit disposer d’autorisations pour pouvoir effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="fdef1-122">Your account needs to be assigned permissions before you can perform this procedure.</span></span> <span data-ttu-id="fdef1-123">Pour voir les autorisations qui vous sont nécessaires, consultez l’entrée de rôle « gérer les alertes » dans [autorisations dans le centre de conformité Office 365 Security &](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fdef1-123">To see what permissions you need, see the "Manage Alerts" role entry in [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="fdef1-124">Utiliser le centre d’administration Exchange pour configurer des destinataires supplémentaires pour les messages indésirables sortants</span><span class="sxs-lookup"><span data-stu-id="fdef1-124">Use the EAC to configure additional recipients for outbound spam messages</span></span>

1. <span data-ttu-id="fdef1-125">Dans le centre d’administration Exchange, accédez à **protection** \> contre le **courrier indésirable sortant**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-125">In the EAC, go to **Protection** \> **Outbound spam**.</span></span>

2. <span data-ttu-id="fdef1-126">Sélectionnez la stratégie nommée **par défaut**, puis cliquez sur **modifier** ![l'](media/ITPro-EAC-EditIcon.png)icône modifier.</span><span class="sxs-lookup"><span data-stu-id="fdef1-126">Select the policy named **Default**, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>

3. <span data-ttu-id="fdef1-127">Dans la page de propriétés qui s’ouvre, vérifiez que l’onglet **Préférences de courrier indésirable sortant** est sélectionné, puis configurez le paramètre suivant :</span><span class="sxs-lookup"><span data-stu-id="fdef1-127">In the properties page that opens, verify that the **Outbound spam preferences** tab is selected, and then configure the following setting:</span></span>

   <span data-ttu-id="fdef1-128">**Envoyer une copie de tous les messages électroniques sortants suspects à l’adresse ou aux adresses de messagerie suivantes**: activez la case à cocher et entrez les adresses de messagerie d’un ou plusieurs administrateurs devant être ajoutés au champ **CCI** des messages détectés.</span><span class="sxs-lookup"><span data-stu-id="fdef1-128">**Send a copy of all suspicious outbound email messages to the following email address or addresses**: Select the check box and enter the email addresses of one or more administrators who should be added to the **Bcc** field of detected messages.</span></span> <span data-ttu-id="fdef1-129">Séparez les adresses de messagerie par un point-virgule (;).</span><span class="sxs-lookup"><span data-stu-id="fdef1-129">Separate multiple email addresses with a semicolon ( ; ).</span></span>

   <span data-ttu-id="fdef1-130">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-130">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="fdef1-131">Utiliser Exchange Online PowerShell ou Exchange Online Protection PowerShell pour configurer des destinataires supplémentaires pour les messages de courrier indésirable sortants</span><span class="sxs-lookup"><span data-stu-id="fdef1-131">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure additional recipients for outbound spam messages</span></span>

<span data-ttu-id="fdef1-132">Pour activer et configurer des destinataires supplémentaires pour les messages de courrier indésirable sortants, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fdef1-132">To enable and configure additional recipients for outbound spam messages, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- <span data-ttu-id="fdef1-133">Pour spécifier les destinataires qui remplacent toutes les valeurs existantes, `emailaddress1,emailaddress2,...emailaddressN`utilisez la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="fdef1-133">To specify recipients that overwrite all existing values, use the syntax `emailaddress1,emailaddress2,...emailaddressN`.</span></span>

- <span data-ttu-id="fdef1-134">Pour ajouter ou supprimer des destinataires de manière sélective sans affecter les autres entrées, `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`utilisez la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="fdef1-134">To selectively add or remove recipients without affecting the other entries, use the syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span></span>

<span data-ttu-id="fdef1-135">Cet exemple active et configure chris@contoso.com, laura@contoso.com et julia@contoso.com comme destinataires CCI pour les messages indésirables sortants.</span><span class="sxs-lookup"><span data-stu-id="fdef1-135">This example enables and configures chris@contoso.com, laura@contoso.com and julia@contoso.com as Bcc recipients for outbound spam messages.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

<span data-ttu-id="fdef1-136">Cet exemple montre comment ajouter michelle@contoso.com en tant que destinataire CCI supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="fdef1-136">This example adds michelle@contoso.com as an additional Bcc recipient.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

<span data-ttu-id="fdef1-137">Cet exemple montre comment supprimer chris@contoso.com et julia@contoso.com de la liste des destinataires en copie carbone invisible.</span><span class="sxs-lookup"><span data-stu-id="fdef1-137">This example removes chris@contoso.com and julia@contoso.com from the list of Bcc recipients.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

<span data-ttu-id="fdef1-138">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="fdef1-138">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

<span data-ttu-id="fdef1-139">**Remarque**: exécutez la commande `Get-HostedOutboundSpamFilterPolicy | Format-List` pour afficher les valeurs actuelles des propriétés *BccSuspiciousOutboundMail* et *BccSuspiciousOutboundAdditionalRecipients* .</span><span class="sxs-lookup"><span data-stu-id="fdef1-139">**Note**: Run the command `Get-HostedOutboundSpamFilterPolicy | Format-List` to see the current values of the *BccSuspiciousOutboundMail* and *BccSuspiciousOutboundAdditionalRecipients* properties.</span></span>

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a><span data-ttu-id="fdef1-140">Utiliser le centre de sécurité & conformité pour configurer les notifications lorsqu’un expéditeur est bloqué</span><span class="sxs-lookup"><span data-stu-id="fdef1-140">Use the Security & Compliance Center to configure notifications when a sender is blocked</span></span>

1. <span data-ttu-id="fdef1-141">Dans le **Centre de sécurité** \> & conformité, accédez à alerts **Alert Policies**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-141">In the Security & Compliance Center, go to **Alerts** \> **Alert Policies**.</span></span>

2. <span data-ttu-id="fdef1-142">Recherchez et sélectionnez la stratégie appelée **utilisateur restreint de l’envoi de courrier électronique**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-142">Find and select the policy named **User restricted from sending email**.</span></span>

3. <span data-ttu-id="fdef1-143">Dans le survol qui s’ouvre, cliquez sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-143">In the fly out that opens, click **Edit policy**.</span></span>

4. <span data-ttu-id="fdef1-144">Dans la page **modifier les destinataires** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="fdef1-144">In the **Edit recipients** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="fdef1-145">**Envoyer des notifications par courrier électronique**: Vérifiez que **activé** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fdef1-145">**Send email notifications**: Verify that **On** is selected.</span></span>

   - <span data-ttu-id="fdef1-146">**Destinataires du message électronique**: par défaut, **TenantAdmins** est la seule valeur ici.</span><span class="sxs-lookup"><span data-stu-id="fdef1-146">**Email recipients**: By default **TenantAdmins** is the only value here.</span></span> <span data-ttu-id="fdef1-147">Pour ajouter des destinataires supplémentaires, cliquez sur un emplacement vide dans cette zone, commencez à taper le destinataire, puis sélectionnez le destinataire lorsque son nom est résolu.</span><span class="sxs-lookup"><span data-stu-id="fdef1-147">To add additional recipients, click in an empty spot in this box, start typing the recipient, and select the recipient when their name resolves.</span></span> <span data-ttu-id="fdef1-148">Pour supprimer des destinataires, cliquez sur **X** en regard de leur nom.</span><span class="sxs-lookup"><span data-stu-id="fdef1-148">To remove recipients, click on the **X** next to their names.</span></span>

   - <span data-ttu-id="fdef1-149">**Limite quotidienne des notifications**: la valeur par défaut est **illimitée**, mais vous pouvez configurer différentes limites entre 1 et 200.</span><span class="sxs-lookup"><span data-stu-id="fdef1-149">**Daily notification limit**: The default value is **No limit**, but you can configure various limits from 1 to 200.</span></span>

   <span data-ttu-id="fdef1-150">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fdef1-150">When you're finished, click **Save**.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="fdef1-151">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="fdef1-151">For more information</span></span>

[<span data-ttu-id="fdef1-152">Pool de remise à risque élevé pour les messages sortants</span><span class="sxs-lookup"><span data-stu-id="fdef1-152">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="fdef1-153">FAQ sur la protection contre le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="fdef1-153">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
