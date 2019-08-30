---
title: Basculement vers EOP à partir de Google Postini, Barracuda Spam and Virus Firewall, ou Cisco IronPort
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: Le but de cette rubrique est de vous aider à comprendre le processus de passage d'un équipement de protection de messagerie électronique local ou d'un service de protection dans le nuage à Exchange Online Protection (EOP), puis de vous fournir les ressources d'aide nécessaires pour commencer à l'utiliser.
ms.openlocfilehash: d7a1f4c281a50a8a835acd848f2c1c0d0407bcf1
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676516"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Basculement vers EOP à partir de Google Postini, Barracuda Spam and Virus Firewall, ou Cisco IronPort

 Le but de cette rubrique est de vous aider à comprendre le processus de passage d'un équipement de protection de messagerie électronique local ou d'un service de protection dans le nuage à Exchange Online Protection (EOP), puis de vous fournir les ressources d'aide nécessaires pour commencer à l'utiliser. Il existe de nombreuses solutions de filtrage du courrier indésirable, mais le processus de passage à EOP est généralement similaire.
  
Si vous débutez avec EOP et que vous souhaitez lire une présentation de ses fonctionnalités avant de choisir de basculer, commencez par la rubrique de présentation de la [protection Exchange Online Protection](exchange-online-protection-overview.md) .
  
Avant de passer à EOP, il est important que vous déterminiez si vous voulez héberger vos boîtes aux lettres protégées par EOP dans le nuage avec Exchange Online, localement ou dans un scénario hybride (hybride signifie que certaines boîtes aux lettres sont hébergées localement, et d'autres avec Exchange Online). Chacun de ces scénarios d'hébergement (en nuage, local et hybride) est possible, mais les étapes de configuration peuvent varier. Voici quelques considérations pour vous aider à choisir le déploiement approprié :
  
- **Protection EOP avec des boîtes aux lettres locales**: ce scénario est approprié si vous avez une infrastructure d’hébergement de messagerie existante que vous souhaitez utiliser, ou si vous avez besoin de conserver des boîtes aux lettres en local et que vous souhaitez protéger la protection de messagerie basée sur le Cloud d’EOP. . Pour plus d'informations sur ce scénario, consultez la rubrique [Passage à EOP autonome](#switch-to-eop-standalone).

- **Protection EOP avec des boîtes aux lettres Exchange Online**: ce scénario est approprié si vous voulez que la protection EOP et toutes vos boîtes aux lettres soient hébergées dans le Cloud. Il peut s'avérer plus simple, car il ne nécessite pas le maintien de serveurs de messagerie locaux. La rubrique [Passage à Exchange Online](#switch-to-exchange-online) décrit ce scénario.

- **Protection EOP avec des boîtes aux lettres hybrides**: vous souhaitez peut-être utiliser des boîtes aux lettres en nuage, mais vous devez conserver des boîtes aux lettres pour certains utilisateurs en local. Ce scénario est approprié si vous voulez conserver certaines boîtes aux lettres localement, et héberger les autres avec Exchange Online. [Passage à une solution hybride](#switch-to-a-hybrid-solution) décrit ce scénario.

## <a name="switch-to-eop-standalone"></a>Passage à EOP autonome

Si vous hébergez actuellement vos boîtes aux lettres localement et utilisez un équipement de protection local ou un service de protection de messagerie dans le nuage, vous pouvez passer à EOP pour bénéficier de ses fonctionnalités de protection et sa disponibilité. Pour configurer EOP dans un scénario autonome, c'est-à-dire consistant à héberger vos boîtes aux lettres localement et à utiliser EOP pour assurer la protection du courrier électronique, vous pouvez procéder de la manière décrite dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md). Cette rubrique décrit les étapes de configuration de la protection EOP, qui incluent l'inscription, l'ajout de votre domaine et la configuration de votre flux de messagerie avec des connecteurs.
  
## <a name="switch-to-exchange-online"></a>Passage à Exchange Online

Peut-être avez-vous des boîtes aux lettres locales protégées par un équipement local, et souhaitez-vous passer à des boîtes aux lettres Exchange Online hébergées dans le nuage et à la protection EOP pour bénéficier des fonctionnalités de messagerie et de protection d'Office 365. Pour commencer, vous pouvez vous inscrire à Office 365, puis ajouter votre domaine. Ce scénario ne requiert aucune configuration de connecteurs, car il n'y a aucun routage vers des boîtes aux lettres locales. Commencez à la [page d'inscription à Office 365](https://www.microsoft.com/office365/online-software.aspx). [Prise en main d’Office 365](https://go.microsoft.com/fwlink/p/?LinkId=275407) fournit des ressources pour vous familiariser avec ses fonctionnalités.
  
Durant le processus de configuration d'Office 365, vous allez créer vos utilisateurs de boîtes aux lettres en nuage.
  
## <a name="switch-to-a-hybrid-solution"></a>Passage à une solution hybride

Il se peut que vous vouliez déplacer uniquement une partie de vos boîtes aux lettres vers le nuage en raison d'exigences propres à votre organisation ou de considérations réglementaires. Lorsque vous déployez un scénario hybride, vous pouvez déplacer des boîtes aux lettres vers le nuage conformément aux exigences de votre organisation. Une migration vers un environnement hybride avec protection EOP est plus compliquée qu'un scénario de déplacement complet dans le nuage. Toutefois, Microsoft offre une prise en charge complète du scénario hybride et de nombreuses ressources pour faciliter le déplacement hybride.
  
Pour commencer, si vous envisagez d’utiliser un déploiement hybride, il s’agit de [déploiements hybrides Exchange Server](https://docs.microsoft.com/exchange/exchange-hybrid). De plus, il existe quelques façons différentes de router le courrier dans un scénario hybride que vous devez comprendre. Le [routage de transport dans les déploiements hybrides Exchange](https://docs.microsoft.com/exchange/transport-routing) explique chaque type, de sorte que vous pouvez choisir le meilleur scénario de routage, en fonction des besoins de votre entreprise.
  
## <a name="migration-planning"></a>Planification de la migration

Si vous décidez de passer à EOP, soyez particulièrement attentif aux aspects suivants :
  
- **Règles de filtrage personnalisées**: Si vous avez des règles de filtrage ou de stratégie d’entreprise personnalisées pour intercepter des courriers indésirables spécifiques, nous vous recommandons d’essayer EOP avec les paramètres par défaut pour une période, avant de migrer vos règles. EOP offre une protection contre le courrier indésirable au niveau de l’entreprise avec les paramètres par défaut, il se peut que vous n’ayez pas besoin de migrer certaines de vos règles vers EOP. Bien entendu, si vous avez des règles en place qui appliquent des stratégies d’entreprise personnalisées spécifiques, vous pouvez les créer. Les [règles de flux de messagerie (règles de transport) dans Exchange Online Protection](mail-flow-rules-transport-rules-0.md) fournissent des instructions détaillées sur la création de règles de flux de messagerie dans EOP.

- Listes d' **adresses IP autorisées et listes d’adresses IP bloquées**: Si vous avez des listes d’autorisation par utilisateur et des listes rouges, prévoyez un certain temps pour copier les listes vers EOP dans le cadre de votre processus de configuration. Pour plus d’informations sur les listes d’adresses IP autorisées et les listes d’adresses IP bloquées, consultez [la rubrique Configure the connection filter Policy](../configure-the-connection-filter-policy.md).

- **Communication sécurisée**: Si vous avez un partenaire qui requiert une messagerie chiffrée, nous vous recommandons de le configurer dans le centre d’administration Exchange. Pour configurer ce scénario, consultez la rubrique [set up Connectors for Secure Mail Flow with a Partner Organization](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-for-secure-mail-flow-with-a-partner).

> [!TIP]
> Lorsque vous passez d'un équipement local à EOP, vous pouvez conserver votre équipement ou un serveur pour effectuer les contrôles de règle d'entreprise. Par exemple, si votre appliance effectue un filtrage personnalisé sur le courrier sortant et que vous souhaitez qu’elle continue à le faire, vous pouvez configurer EOP pour envoyer des messages directement à l’appliance pour un filtrage supplémentaire, avant qu’elle ne soit routée vers Internet.
