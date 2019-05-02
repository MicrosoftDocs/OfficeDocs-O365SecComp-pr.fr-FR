---
title: Identifier les messages suspects dans Outlook.com et Outlook sur le Web
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Pour empêcher les messages de hameçonnage d'atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l'expéditeur est bien ce qu'il dit, et marquez les messages suspects comme courrier indésirable.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345894"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a>Identifier les messages suspects dans Outlook.com et Outlook sur le Web

Pour empêcher les messages de hameçonnage d'atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l'expéditeur est bien ce qu'il dit, et marquez les messages suspects comme courrier indésirable.

> [!IMPORTANT]
> Lorsqu'un message est marqué comme frauduleux de hameçonnage, Outlook.com et Outlook sur le Web affichent un avertissement en haut de la page, mais vous pouvez toujours ouvrir les liens figurant dans le message.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Comment puis-je identifier un message suspect dans ma boîte de réception?

Outlook.com et Outlook sur le Web affichent des indicateurs lorsque l'expéditeur d'un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l'adresse de l'expéditeur.

### <a name="you-see-a--in-the-sender-image"></a>Un «?» apparaît dans l'image de l'expéditeur

Lorsque Outlook.com et Outlook sur le Web ne peuvent pas vérifier l'identité de l'expéditeur à l'aide des techniques d'authentification de messagerie, ils affichent un «?» dans la photo de l'expéditeur.

![Le message n'a pas passé la vérification](media/message-did-not-pass-verification.jpg)

Les messages qui ne parvient pas à s'authentifier ne sont pas tous malveillants. Toutefois, vous devez être prudent quant à l'interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l'expéditeur. Ou, si vous reconnaissez un expéditeur qui ne possède pas de «?» normalement dans l'image de l'expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l'expéditeur est usurpé.

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a>L'adresse de l'expéditeur est différente de celle qui apparaît dans l'adresse de l'expéditeur

Bien souvent, l'adresse de messagerie que vous voyez dans un message est différente de celle que vous voyez dans l'adresse de l'adresse. Parfois, les auteurs de phishing essaient de vous tromper en pensant que l'expéditeur est une personne qui n'est pas vraiment.

Lorsque Outlook.com et Outlook sur le Web détectent une différence entre l'adresse réelle de l'expéditeur et l'adresse de l'adresse de, ils affichent l'expéditeur réel à l'aide de la balise via, qui est soulignée.

![texte de remplacement de l'expéditeur non vérifié](media/unverified-sender-feature1.png)

Dans cet exemple, le domaine `suspicious.com` d'envoi est authentifié, mais celui-ci est `unknown@contoso.com` placé dans l'adresse de l'expéditeur.

Tous les messages avec une balise via ne sont pas suspects. Toutefois, si vous ne reconnaissez pas un message avec une balise via, soyez prudent lors de l'interaction avec celui-ci.

Dans Outlook.com et le nouveau Outlook sur le Web, vous pouvez placer le curseur sur le nom ou l'adresse de l'expéditeur dans la liste des messages pour voir son adresse de messagerie, sans avoir à ouvrir le message.

![Prise en main de OneDrive](media/get-started-with-onedrive-message.png)

Comment savoir si vous utilisez le nouveau Outlook sur le Web? Consultez les exemples suivants:

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Quels critères les Outlook.com et Outlook sur le Web utilisent-ils pour ajouter les propriétés «?» et «via»?

Pour le «?» de l'image de l'expéditeur: Outlook.com requiert que le message passe l'authentification SPF ou DKIM. Pour plus d'informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l'usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).

Pour la balise via: si le domaine de l'adresse de l'expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l'un de ces deux champs (en préférant la signature DKIM).

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a>Puis-je remplacer ces propriétés par le biais de l'IP autorisé, la règle de transport Exchange autorise ou les expéditeurs approuvés?

Vous ne pouvez pas remplacer ces propriétés.

### <a name="how-do-i-remove-these-properties"></a>Comment puis-je supprimer ces propriétés?

Pour le «?» de l'image de l'expéditeur: en tant qu'expéditeur, vous devez authentifier votre message avec SPF ou DKIM.

Pour la balise via: en tant qu'expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l'adresse de provenance ou qu'il s'agit d'un sous-domaine de celui-ci.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Est-ce que Outlook.com et Outlook sur le Web s'affichent pour chaque message qui ne passe pas l'authentification?

Pas nécessairement. Outlook.com et Outlook sur le Web peuvent avoir d'autres propriétés dans le message pour authentifier l'expéditeur.

## <a name="related-topics"></a>Voir aussi

[Protéger votre compte de messagerie Outlook.com](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Gérer les abus, le hameçonnage ou l'usurpation d'identité dans Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)