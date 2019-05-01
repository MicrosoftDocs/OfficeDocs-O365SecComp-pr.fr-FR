---
title: Définir une date d'expiration pour les messages chiffrés par le chiffrement de messages avancé Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Avec les fonctionnalités de chiffrement de messages avancé Office 365 sur Office 365 message enCryption (OME), vous pouvez étendre votre sécurité de messagerie en définissant une date d'expiration pour les e-mails via un modèle personnalisé.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506714"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a>Définir une date d'expiration pour les messages chiffrés par le chiffrement de messages avancé Office 365

Le chiffrement de messages avancé Office 365 est disponible en haut du chiffrement des messages Office 365 dans certains abonnements. Le chiffrement de messages avancé est inclus dans [Microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 entreprise E5 et Office 365 éducation a5. Si votre organisation possède un abonnement Office 365 qui n'inclut pas le chiffrement de messages avancé Office 365, vous pouvez acheter le chiffrement de messages avancé comme module complémentaire avec E5 conformité de la référence SKU de conformité avancée.

Vous pouvez utiliser l'expiration des messages envoyés par vos utilisateurs à des destinataires externes qui utilisent le portail OME pour accéder à des e-mails chiffrés. Vous obligez les destinataires à utiliser le portail OME pour afficher et répondre à des messages électroniques chiffrés envoyés par votre organisation à l'aide d'un modèle personnalisé qui spécifie une date d'expiration dans Windows PowerShell.

En tant qu'administrateur général d'Office 365, lorsque vous appliquez la personnalisation de votre entreprise pour personnaliser l'apparence des messages électroniques de votre organisation Office 365, vous pouvez également spécifier une expiration pour ces messages électroniques. Avec le chiffrement de messages avancé Office 365, vous pouvez créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation. À l'aide d'un modèle, vous pouvez contrôler la durée pendant laquelle les destinataires ont accès aux messages envoyés par vos utilisateurs.

Lorsqu'un utilisateur final reçoit un message dont la date d'expiration est définie, l'utilisateur voit la date d'expiration dans le message du wrapper. Si un utilisateur tente d'ouvrir un message expiré, une erreur s'affiche dans le portail OME.

Seuls les courriers électroniques adressés à des destinataires externes sont Expires.

Avec le chiffrement de messages avancé Office 365, chaque fois que vous appliquez une personnalisation personnalisée, Office 365 applique le wrapper aux messages électroniques correspondant à la règle de flux de messagerie à laquelle vous appliquez le modèle. De plus, l'expiration ne peut être utilisée que si la personnalisation personnalisée est utilisée.

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a>Créer un modèle de personnalisation pour forcer l'expiration du courrier à l'aide de PowerShell

1. [Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l'aide d'un compte disposant d'autorisations d'administrateur général dans votre client Office 365.

2. Exécutez la cmdlet New-OMEConfiguration.

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

Où :

- Identity est le nom du modèle personnalisé.

- ExternalMailExpiryInDays identifie le nombre de jours pendant lesquels vous souhaitez que les destinataires puissent conserver le courrier avant qu'il n'expire. Vous pouvez utiliser n'importe quelle valeur comprise entre 1 et 730 jours.

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Plus d'informations sur le chiffrement de messages avancé Office 365

- [Chiffrement avancé des messages Office 365](ome-advanced-message-encryption.md)

- [Révoquer le courrier électronique chiffré par le chiffrement de messages avancé Office 365](revoke-ome-encrypted-mail.md)

- [Description du service de conformité et de stratégie de message](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)