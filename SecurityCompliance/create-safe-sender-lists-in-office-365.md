---
title: Créer des listes d’expéditeurs approuvés dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150s
ms.assetid: 9721b46d-cbea-4121-be51-542395e6fd21
description: Si vous souhaitez être sûr de recevoir des messages d’un expéditeur particulier, étant donné que vous les approuvez et leurs messages, vous pouvez ajuster votre liste verte dans une stratégie de filtrage du courrier indésirable dans le centre d’administration Exchange.
ms.openlocfilehash: b97767a3ee4882b1a9b052bc845e8758a6402534
ms.sourcegitcommit: e834d4168f584f2efb22479aec108497eea267f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34709112"
---
# <a name="create-safe-sender-lists-in-office-365"></a>Créer des listes d’expéditeurs approuvés dans Office 365

Si vous souhaitez vous assurer que les utilisateurs reçoivent des courriers électroniques provenant d’expéditeurs ou d’expéditeurs spécifiques, car vous les approuvez et leurs messages, vous pouvez choisir parmi plusieurs méthodes. Ces options incluent les règles de transport Exchange (ETR), les expéditeurs approuvés Outlook, les listes d’adresses IP autorisées, les listes vertes d’expéditeurs/de domaines de courrier indésirable.

> [!IMPORTANT]
> Bien que les listes d’adresses autorisées de l’organisation puissent être utilisées pour résoudre les faux positifs, elle doit être considérée comme une solution temporaire et éviter, dans la mesure du possible. La gestion des faux positifs à l’aide de listes d’autorisation n’est pas recommandée car elle peut accidentellement ouvrir votre organisation à des usurpateurs d’identité, des emprunts d’identité et d’autres attaques. Si vous souhaitez utiliser une liste verte à cette fin, vous devez être vigilant et conserver l’article pour l’envoi de messages indésirables, [non indésirables et de hameçonnage à Microsoft pour analyse](https://docs.microsoft.com/en-us/office365/SecurityCompliance/submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis), à l’adresse.

La méthode recommandée pour configurer une liste d’expéditeurs approuvés consiste à utiliser des règles de transport Exchange (ETR), car cela offre la plus grande flexibilité pour garantir que seuls les messages corrects sont autorisés. Les listes d’adresses de *messagerie des stratégies de blocage du courrier* indésirable et de *domaine* ne sont pas aussi sécurisées que les *listes basées sur les adresses IP* , car les domaines peuvent facilement être falsifiés. Cependant, les listes d’adresses IP autorisées de stratégie de blocage du courrier indésirable présentent également des risques car ils autorisent les domaines envoyés via cette adresse IP à contourner le filtrage du courrier indésirable. Faites attention et surveillez *toutes les* exceptions effectuées, avec précaution.

> [!IMPORTANT]
> Vous [trouverez ici](create-block-sender-lists-in-office-365.md)des informations sur la création d’une **liste** d’expéditeurs bloqués.

## <a name="options-from-most-to-least-recommended"></a>Options du plus ou moins recommandé

Vous devez toujours limiter vos listes d’autorisation, car elles contournent de nombreuses mesures de sécurité. Vous devez revérifier toutes les listes d’autorisation dans le cadre de votre maintenance standard, afin de connaître les personnes autorisées à contourner. Il est recommandé d’utiliser des ETR restrictives lorsque cela est possible.

- Règles de transport Exchange (ETR également appelées règles de flux de messagerie)
- Expéditeurs approuvés Outlook
- Stratégie anti-courrier indésirable: listes d’adresses IP autorisées
- Stratégie anti-courrier indésirable: listes vertes de l’expéditeur/du domaine

## <a name="using-exchange-transport-rules-etrs-to-allow-specific-senders-recommended"></a>Utilisation des règles de transport Exchange (ETR) pour autoriser des expéditeurs spécifiques (recommandé)

Pour vous assurer que seuls les messages légitimes sont autorisés dans votre organisation, la condition doit être l’une des suivantes:

- Utilisez l’état d’authentification de l’expéditeur du domaine d’envoi. Pour ce faire, vérifiez l’en-tête Authentication-Results afin de vous assurer qu’il contient «dMarc = passe» ou «dMarc = bestguesspass». Cela garantit que le domaine d’envoi a été authentifié et qu’il n’est pas usurpé. Cliquez pour plus d’informations sur [SPF](https://docs.microsoft.com/en-us/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)et l’authentification de messagerie [DMARC](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-dmarc-to-validate-email) .

- Si le domaine d’envoi n’a pas d’authentification, utilisez le domaine d’envoi *plus* une adresse IP d’envoi (ou une plage d’adresses IP). Assurez-vous que vous êtes *aussi restrictif que possible*, l’objectif étant que vous effectuez cette opération aussi efficacement que possible. Une plage d’adresses IP supérieure à/24 n’est *pas* recommandée. Évitez d’ajouter des plages d’adresses IP qui appartiennent à des services grand public ou à des infrastructures partagées.

> [!IMPORTANT]
> Si vous autorisez une adresse IP NATted, vous devez déterminer les ordinateurs impliqués dans ce pool NAT afin de déterminer l’étendue de votre autorisation. N’oubliez pas que les adresses IP peuvent varier, et les participants NAT peuvent également l’être. Vous devez revérifier toutes les listes d’autorisation, y compris le protocole IP autorisé dans le cadre de votre maintenance standard.

- Ajoutez *éventuellement*une condition dont le message provient de l’extérieur de l’organisation (Ceci est implicite, mais il convient de l’ajouter en tant que condition pour tenir compte des serveurs sur site qui ne sont peut-être pas correctement configurés).

- ** Si vous le souhaitez, si vous pouvez identifier des mots clés ou des expressions uniques dans l’objet ou le corps du message, utilisez ces informations comme condition supplémentaire pour limiter davantage les messages électroniques autorisés par la règle de flux de messagerie.

L’action sur la règle doit respecter ce modèle:

1. Définissez le seuil de probabilité de courrier indésirable sur-1 (ignorer le filtrage du courrier indésirable).

2. Ajoutez un en-tête X pour indiquer l’action de la règle. Dans l’exemple ci-dessous, vous pouvez ajouter un simple en-tête «X-ETR: contourner le filtrage `contoso.com`du courrier indésirable pour l’expéditeur authentifié». Si cette règle comporte plusieurs domaines, vous pouvez modifier le texte d’en-tête en fonction de vos besoins. **Lorsqu’un message ignore le filtrage en raison d’un ETR, il marque SFV: SKN dans l’en-tête X-Forefront-antispam-Report** (**s’il s’agit d’une liste d’adresses IP autorisées, il marque également IPV: CAL**). Cela vous aidera à résoudre les problèmes.

![Interface utilisateur graphique permettant de contourner le filtrage du courrier indésirable.](media/1_AllowList_SkipFilteringFromContoso.png)

> [!CAUTION]
> Ne configurez pas les règles de flux de messagerie avec *le domaine de l’expéditeur* comme condition d’ignorer le filtrage du courrier indésirable. Cette méthode augmente considérablement le risque que les spammeurs usurpent le domaine d’envoi (ou empruntent l’identité de l’adresse de messagerie complète) ignorez le filtrage du courrier indésirable, les vérifications d’authentification de l’expéditeur et le message arrivera dans la boîte de réception d’une personne.

![Comment définir la valeur SCL sur moins un.](media/2_AllowList_SetsSCLMinus1.png)

N’ajoutez pas de domaines que vous possédez ou des domaines populaires ( `microsoft.com`par exemple,) à la règle de flux de messagerie en tant que condition. Ceci est considéré comme un risque élevé, car il permet aux acteurs incorrects de vous envoyer des messages qui seraient autrement filtrés.

[Veuillez cliquer pour connaître les étapes de création d’une ETR, également appelées règles de flux de messagerie](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages).

## <a name="use-outlook-safe-senders-end-user-managed"></a>Utiliser des expéditeurs approuvés Outlook (géré par l’utilisateur final)

Au lieu d’autoriser une adresse, un domaine ou une adresse IP de manière globale, les utilisateurs finaux peuvent également autoriser l’envoi d’adresses via des expéditeurs approuvés Outlook. Les étapes à suivre pour configurer cette configuration diffèrent entre [Outlook Web App](https://support.office.com/en-us/article/block-or-allow-junk-email-settings-48c9f6f7-2309-4f95-9a4d-de987e880e46) et le [client Outlook](https://support.office.com/en-us/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). **Lorsque les messages sont autorisés en raison des expéditeurs approuvés, vous verrez SFV: SFE dans le X-Forefront-antispam-Report,** ce qui indique que le filtrage du courrier indésirable/de l’usurpation/hameçonnage est contourné.

## <a name="use-anti-spam-policy-ip-allow-lists"></a>Utiliser la stratégie de blocage du courrier indésirable listes d’adresses IP autorisées

Lorsqu’il n’est pas possible d’utiliser ETR pour autoriser globalement un expéditeur spécifique lors de la validation de l’authentification de l’expéditeur, ou en liant un domaine et l’adresse IP, la meilleure option est d’ajouter l’expéditeur à la *liste d’adresses IP autorisées de la stratégie anti-courrier*indésirable. [Les étapes détaillées sont disponibles dans configurer le document de stratégie de filtrage des connexions](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-the-connection-filter-policy). Il est important de conserver la liste des adresses IP autorisées au minimum et d’éviter d’utiliser des plages d’adresses IP. Évitez d’ajouter des plages d’adresses IP qui appartiennent à des services grand public ou des infrastructures partagées, et *Assurez-* vous que vous examinez régulièrement la liste des adresses IP autorisées et supprimez celles qui ne sont plus nécessaires.

> [!CAUTION]
> La configuration des stratégies de blocage du courrier indésirable en fonction de l’adresse IP de l’expéditeur uniquement entraîne le blocage du filtrage du courrier indésirable pour tous les messages provenant de cette adresse IP dans la règle d’autorisation. Cela crée un risque élevé que des acteurs défectueux vous envoient des messages qui seraient autrement filtrés. Cette méthode ignore également le filtrage du courrier indésirable, les vérifications d’authentification de l’expéditeur et le message dans la boîte de réception d’un utilisateur, ce qui augmente les risques.

## <a name="use-anti-spam-policy-senderdomain-allow-lists"></a>Utilisation de la stratégie de blocage du courrier indésirable listes des expéditeurs/domaines autorisés

L’option la moins intéressante consiste à autoriser l’expéditeur/domaine. Cette option doit être évitée si cela est *possible* car elle contourne totalement le courrier indésirable/frauduleux/frauduleux et n’évalue pas l’authentification de l’expéditeur. Cette méthode augmente le risque de recevoir des messages à partir d’acteurs incorrects et est recommandé temporairement et uniquement lors des tests. Les étapes détaillées sont disponibles dans la documentation [configurer vos stratégies de filtrage du courrier](https://docs.microsoft.com/en-us/office365/securitycompliance/configure-your-spam-filter-policies) indésirable.

> [!CAUTION]
> La configuration des stratégies de blocage du courrier indésirable pour autoriser le domaine de l' *expéditeur/* de l’autorisation entraînera l’ignorance du filtrage du courrier indésirable pour un des messages provenant d’expéditeurs figurant dans la liste verte, ou b) de tous les expéditeurs d’un domaine autorisé. Cette méthode augmente considérablement le risque que les spammeurs usurpent le domaine d’envoi (ou empruntent l’identité de l’adresse de messagerie complète), ce qui ignore le filtrage du courrier indésirable, les vérifications d’authentification de l’expéditeur et envoie le message directement dans la boîte de réception d’une personne.
> 
> N’ajoutez pas de domaines que vous possédez ou des domaines populaires `microsoft.com`(par exemple,) à la règle de flux de messagerie en tant que condition. Cette méthode est considérée comme un risque élevé, car elle permet aux acteurs incorrects de vous envoyer des messages qui seraient autrement filtrés, ce qui augmente le risque.

> [!IMPORTANT]
> Vous [trouverez ici](create-block-sender-lists-in-office-365.md)des informations sur la création d’une **liste** d’expéditeurs bloqués.