---
title: Chiffrement avancé des messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Le chiffrement de messages avancé dans Office 365 aide les organisations à respecter leurs obligations de conformité en permettant aux administrateurs d'expirer et de révoquer l'accès par le biais d'un portail Web Office 365 à des e-mails chiffrés.
ms.openlocfilehash: a775803a8d2678441f319c0145e96e7d19c26f7e
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506715"
---
# <a name="office-365-advanced-message-encryption"></a>Chiffrement avancé des messages Office 365

Le chiffrement de messages avancé Office 365 est disponible en haut du chiffrement des messages Office 365 dans certains abonnements. Le chiffrement de messages avancé est inclus dans [Microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 entreprise E5 et Office 365 éducation a5. Si votre organisation possède un abonnement Office 365 qui n'inclut pas le chiffrement de messages avancé Office 365, vous pouvez acheter le chiffrement de messages avancé comme module complémentaire avec E5 conformité de la référence SKU de conformité avancée.

Cet article fait partie d'une série d'articles plus large sur le chiffrement de [messages Office 365](ome.md).

Le chiffrement de messages avancé dans Office 365 aide les clients à respecter les obligations de conformité nécessitant des contrôles plus flexibles pour les destinataires externes et leur accès aux e-mails chiffrés. Avec le chiffrement de messages avancé dans Office 365, vous pouvez contrôler les e-mails sensibles partagés hors de l'organisation à l'aide de stratégies automatiques. Vous configurez ces stratégies pour identifier les types d'informations sensibles tels que les informations personnelles, les ID financiers ou les ID d'intégrité, ou vous pouvez utiliser des mots clés pour améliorer la protection. Une fois que vous avez configuré les stratégies, vous associez des stratégies à des modèles de courrier personnalisés personnalisés, puis vous ajoutez une date d'expiration pour un contrôle supplémentaire pour les courriers électroniques correspondant à la stratégie. En outre, les administrateurs peuvent contrôler les messages électroniques chiffrés accessibles en externe via un portail Web sécurisé en révoquant l'accès au courrier à tout moment.

Vous pouvez uniquement définir une date d'expiration pour les messages électroniques envoyés à des destinataires externes et les révoquer.

Avec le chiffrement de messages avancé Office 365, chaque fois que vous appliquez une personnalisation personnalisée, Office 365 applique le wrapper aux messages électroniques correspondant à la règle de flux de messagerie à laquelle vous appliquez le modèle. De plus, l'expiration ne peut être utilisée que si la personnalisation personnalisée est utilisée. Vous pouvez uniquement révoquer les messages reçus via le portail.

## <a name="get-started-with-office-365-advanced-message-encryption"></a>Prise en main du chiffrement avancé des messages Office 365

Les rubriques suivantes décrivent comment configurer et utiliser le chiffrement de messages avancé.

Votre organisation doit disposer d'un abonnement qui inclut le chiffrement de messages avancé Office 365. Pour plus d'informations sur les abonnements pris en charge, voir la description de la [stratégie de message et du service de conformité](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance).

ConFigurez les nouvelles fonctionnalités de chiffrement de messages Office 365 si elles ne sont pas déjà configurées pour tirer parti des fonctionnalités de chiffrement de messages avancées qui offrent une protection supplémentaire par-dessus les messages chiffrés partagés en externe. Si vous n'avez pas configuré le chiffrement de messages Office 365, consultez la rubrique [set up New office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).

[Définir une date d'expiration pour les messages chiffrés par le chiffrement de messages avancé Office 365](ome-advanced-expiration.md). Contrôlez les messages électroniques sensibles partagés en dehors de l'organisation à l'aide de stratégies automatiques qui améliorent la protection en arrivant à expiration de l'accès via un portail Web sécurisé aux messages chiffrés.

[Révoquer le courrier électronique chiffré par le chiffrement de messages avancé Office 365](revoke-ome-encrypted-mail.md). Contrôlez les messages électroniques sensibles partagés hors de l'organisation et améliorez la protection en révoquant l'accès via un portail Web sécurisé à des e-mails chiffrés.  