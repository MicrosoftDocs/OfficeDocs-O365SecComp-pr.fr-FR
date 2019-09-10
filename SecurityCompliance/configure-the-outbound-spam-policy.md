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
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a>Configurer les notifications de stratégie de courrier indésirable sortant dans Office 365

Le filtrage du courrier indésirable sortant est toujours activé si vous utilisez le service pour l’envoi de messages sortants, ce qui permet de protéger les organisations utilisant le service ainsi que leurs destinataires. À l’instar du filtrage des messages entrants, le filtrage du courrier indésirable sortant est composé du filtrage des connexions et du filtrage du contenu, mais les paramètres du filtre sortant ne sont pas configurables. Si un message sortant est considéré comme du courrier indésirable, il est routé via le pool de remise à risque plus élevé, ce qui réduit la probabilité que le pool IP sortant normal soit ajouté à une liste rouge. Si un client continue à envoyer du courrier indésirable sortant via le service, il ne sera pas autorisé à envoyer des messages.

Bien que vous ne puissiez pas désactiver ou modifier le filtrage du courrier indésirable sortant, vous pouvez configurer les paramètres de notification de courrier indésirable sortants suivants :

- **Envoyer des copies des messages suspects**: ces messages sont marqués comme courrier indésirable (quelle que soit la valeur de contrôle d’accès SCL) et ne sont pas rejetés par le filtre, mais sont acheminés via le pool de remise à risque plus élevé. Vous pouvez utiliser le centre d’administration Exchange ou les ** \*** applets de commande-HostedOutboundSpamFilterPolicy dans Exchange Online PowerShell ou Exchange Online Protection PowerShell pour spécifier des destinataires d’ajout pour ces messages détectés. Notez que les destinataires sont ajoutés en tant que destinataires **CCI** (les champs **de** et **à** sont les expéditeurs et destinataires d’origine).

- **Envoyer des notifications lorsqu’un expéditeur est bloqué**: lorsqu’une quantité importante de courrier indésirable provient d’un utilisateur particulier, l’utilisateur est désactivé pour l’envoi de messages électroniques. Les administrateurs sont avertis par défaut, mais vous pouvez utiliser l’option l’utilisateur ne peut pas envoyer de [stratégie d’alerte](alert-policies.md) par **courrier électronique** dans le centre de conformité Office 365 Security & pour configurer des destinataires de notification supplémentaires.

  Pour savoir à quoi ressemble cette notification, voir [Exemple de notification lorsqu'un expéditeur est bloqué en raison de l'envoi de courrier indésirable sortant](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Pour plus d'informations sur le mode de réactivaction, consultez la rubrique [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Durée d’exécution estimée : 5 minutes

- Pour ouvrir le Centre de conformité et sécurité, consultez la rubrique [Accéder au centre de conformité et sécurité d’Office 365](go-to-the-securitycompliance-center.md).

- Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) ou [Centre d’administration Exchange dans Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).

- Pour ouvrir Exchange Online PowerShell, consultez la rubrique [connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Pour ouvrir Exchange Online Protection PowerShell, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).

- Votre compte doit disposer d’autorisations pour pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l’entrée de rôle « gérer les alertes » dans [autorisations dans le centre de conformité Office 365 Security &](permissions-in-the-security-and-compliance-center.md).

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a>Utiliser le centre d’administration Exchange pour configurer des destinataires supplémentaires pour les messages indésirables sortants

1. Dans le centre d’administration Exchange, accédez à **protection** \> contre le **courrier indésirable sortant**.

2. Sélectionnez la stratégie nommée **par défaut**, puis cliquez sur **modifier** ![l'](media/ITPro-EAC-EditIcon.png)icône modifier.

3. Dans la page de propriétés qui s’ouvre, vérifiez que l’onglet **Préférences de courrier indésirable sortant** est sélectionné, puis configurez le paramètre suivant :

   **Envoyer une copie de tous les messages électroniques sortants suspects à l’adresse ou aux adresses de messagerie suivantes**: activez la case à cocher et entrez les adresses de messagerie d’un ou plusieurs administrateurs devant être ajoutés au champ **CCI** des messages détectés. Séparez les adresses de messagerie par un point-virgule (;).

   Lorsque vous avez terminé, cliquez sur **Enregistrer**.

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a>Utiliser Exchange Online PowerShell ou Exchange Online Protection PowerShell pour configurer des destinataires supplémentaires pour les messages de courrier indésirable sortants

Pour activer et configurer des destinataires supplémentaires pour les messages de courrier indésirable sortants, utilisez la syntaxe suivante :

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- Pour spécifier les destinataires qui remplacent toutes les valeurs existantes, `emailaddress1,emailaddress2,...emailaddressN`utilisez la syntaxe.

- Pour ajouter ou supprimer des destinataires de manière sélective sans affecter les autres entrées, `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`utilisez la syntaxe.

Cet exemple active et configure chris@contoso.com, laura@contoso.com et julia@contoso.com comme destinataires CCI pour les messages indésirables sortants.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

Cet exemple montre comment ajouter michelle@contoso.com en tant que destinataire CCI supplémentaire.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

Cet exemple montre comment supprimer chris@contoso.com et julia@contoso.com de la liste des destinataires en copie carbone invisible.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).

**Remarque**: exécutez la commande `Get-HostedOutboundSpamFilterPolicy | Format-List` pour afficher les valeurs actuelles des propriétés *BccSuspiciousOutboundMail* et *BccSuspiciousOutboundAdditionalRecipients* .

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a>Utiliser le centre de sécurité & conformité pour configurer les notifications lorsqu’un expéditeur est bloqué

1. Dans le **Centre de sécurité** \> & conformité, accédez à alerts **Alert Policies**.

2. Recherchez et sélectionnez la stratégie appelée **utilisateur restreint de l’envoi de courrier électronique**.

3. Dans le survol qui s’ouvre, cliquez sur **modifier la stratégie**.

4. Dans la page **modifier les destinataires** qui s’affiche, configurez les paramètres suivants :

   - **Envoyer des notifications par courrier électronique**: Vérifiez que **activé** est sélectionné.

   - **Destinataires du message électronique**: par défaut, **TenantAdmins** est la seule valeur ici. Pour ajouter des destinataires supplémentaires, cliquez sur un emplacement vide dans cette zone, commencez à taper le destinataire, puis sélectionnez le destinataire lorsque son nom est résolu. Pour supprimer des destinataires, cliquez sur **X** en regard de leur nom.

   - **Limite quotidienne des notifications**: la valeur par défaut est **illimitée**, mais vous pouvez configurer différentes limites entre 1 et 200.

   Lorsque vous avez terminé, cliquez sur **Enregistrer**.

## <a name="for-more-information"></a>Pour plus d’informations

[Pool de remise à risque élevé pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md)

[FAQ sur la protection contre le courrier indésirable](anti-spam-protection-faq.md)
