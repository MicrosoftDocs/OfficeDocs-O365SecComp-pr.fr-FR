---
title: Créer des listes d’expéditeurs bloqués dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/6/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
description: Les options de liste d’expéditeurs de blocs incluent les expéditeurs bloqués Outlook, les listes rouges d’expéditeurs de domaine, les listes d’adresses IP bloquées et les règles de transport Exchange (ETR), également appelées règles de flux de messagerie.
ms.openlocfilehash: 9933cb79b7dce949384815a7b2ed8a9ac8a7824b
ms.sourcegitcommit: f96029928a6cdd141783026d57bc2179d7963af6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35017686"
---
# <a name="create-block-sender-lists-in-office-365"></a>Créer des listes d’expéditeurs bloqués dans Office 365

Parfois, il est nécessaire de bloquer le courrier indésirable des expéditeurs. Vous pouvez choisir parmi plusieurs méthodes. Ces options incluent les expéditeurs bloqués Outlook, les listes de blocage du courrier indésirable, les listes d’adresses IP bloquées et les règles de transport Exchange (ETR, qui sont également appelées règles de flux de messagerie).

> [!NOTE]
> Alors que les listes d’adresses bloquées peuvent être utilisées pour résoudre les faux négatifs (courrier indésirable manqué), ces candidats doivent également être soumis à Microsoft pour analyse. La gestion des faux négatifs à l’aide de listes rouges augmente considérablement votre charge administrative. Si vous utilisez une liste rouge à cet effet, vous devez également conserver l’article pour l’envoi de courrier indésirable, de courrier [non indésirable et de tentatives de hameçonnage à Microsoft pour analyse](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis), à l’aide du prêt.

La bonne méthode de configuration des listes d’expéditeurs bloqués varie en fonction de l’étendue de l’impact. Pour un impact sur un seul utilisateur, la solution appropriée pourrait être d’utiliser des expéditeurs bloqués Outlook, mais si plusieurs utilisateurs ou tous les utilisateurs sont affectés, l’une des autres options serait plus appropriée.

## <a name="options-from-least-to-broadest-scope"></a>Options du moins à l’étendue la plus large

Lors de la création d’une liste rouge, il est important de choisir la méthode appropriée en fonction de l’étendue de l’impact (combien de personnes seront affectées), afin qu’elle corresponde à la largeur de la méthode de blocage. Les options répertoriées ci-dessous sont classées par portée et par étendue. La liste passe de étroite à large, mais *lit les détails* pour obtenir des recommandations complètes.

- Expéditeurs bloqués Outlook
- Stratégie anti-courrier indésirable: listes de blocage des expéditeurs et des domaines
- Règles de transport Exchange (ETR également appelées règles de flux de messagerie)
- Stratégie anti-courrier indésirable: listes d’adresses IP bloquées

## <a name="use-outlook-blocked-senders"></a>Utiliser les expéditeurs bloqués d’Outlook

Lorsque seul un petit nombre d’utilisateurs sont affectés, c’est le cas lorsque des expéditeurs bloqués d’Outlook doivent être utilisés, car cela n’a d’impact que les messages qui leur sont envoyés.

> [!IMPORTANT]
> Si les messages indésirables sont des bulletins d’informations provenant d’une source digne de réputation et reconnaissables, l’annulation de l’abonnement au courrier électronique est une autre option permettant d’empêcher l’utilisateur d’envoyer des messages à l’avenir.

Les étapes à suivre pour la configuration diffèrent entre [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) et le [client Outlook](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). **Lorsque les messages sont bloqués en raison des expéditeurs bloqués, vous verrez SFV: BLK dans le X-Forefront-antispam-Report,** ce qui indique que le message est bloqué.

## <a name="use-anti-spam-policy-senderdomain-block-lists"></a>Utiliser les listes rouge de l’expéditeur/du domaine du courrier indésirable

Lorsque plusieurs utilisateurs sont affectés, l’étendue est plus large et vous devez utiliser une stratégie de blocage du courrier indésirable des expéditeurs et des domaines dans l’ensemble de l’entreprise. Les étapes détaillées sont disponibles dans la documentation [configurer vos stratégies de filtrage du courrier](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) indésirable. Tous les messages bloqués via cette méthode suivent l’action de courrier indésirable, comme configuré dans la stratégie.

## <a name="use-exchange-transport-rules-etrs-to-block-specific-senders"></a>Utiliser les règles de transport Exchange (ETR) pour bloquer des expéditeurs spécifiques

S’il est nécessaire de bloquer les messages envoyés à des utilisateurs spécifiques ou à l’ensemble de l’organisation, ETR (également appelés règles de flux de messagerie) peuvent être utilisés. Les ETR sont plus flexibles, car ils peuvent déclencher l’adresse de messagerie ou le domaine de l’expéditeur, ainsi que des mots clés et d’autres propriétés dans le message. Cette souplesse vous permettra de créer des blocs partiels. [Veuillez cliquer pour connaître les étapes de création d’une ETR, également appelées règles de flux de messagerie](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages).

> [!IMPORTANT]
> Il est facile de créer des règles qui ** sont excessivement agressives, par conséquent, il est important que les critères utilisés soient aussi spécifiques que possible. Assurez-vous également que vous activez l’audit sur la règle que vous créez et effectuez des tests pour vous assurer que tout fonctionne comme prévu.

## <a name="use-anti-spam-policy-ip-block-lists"></a>Utiliser les listes d’adresses IP bloquées de la stratégie anti-courrier indésirable

Lorsqu’il n’est pas possible d’utiliser l’une des autres options pour bloquer un expéditeur, ** la liste d’adresses IP bloquées de la stratégie anti-courrier indésirable peut être utilisée. Vous trouverez [des étapes détaillées dans l’article configure the connection filter Policy](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy). Il est important de conserver la liste des adresses IP bloquées à un *minimum* et de *ne pas* utiliser les plages d’adresses IP ici.

Vous devez *particulièrement* éviter d’ajouter des plages d’adresses IP qui appartiennent à des services grand public ou des infrastructures partagées, et vérifiez également que vous examinez la liste des adresses IP autorisées dans le cadre de la maintenance normale. **Étant donné que l’autorisation-entrées peut ouvrir des itinéraires pour une attaque, vous devez gérer cette liste de manière étroite et supprimer régulièrement les entrées autorisées qui ne sont plus nécessaires.** De plus, si vous allez autoriser une liste d’expéditeurs approuvés, lisez et comprenez les risques et les précautions à prendre dans la rubrique *[créer des listes d’expéditeurs approuvés dans Office 365](create-safe-sender-lists-in-office-365.md)*.