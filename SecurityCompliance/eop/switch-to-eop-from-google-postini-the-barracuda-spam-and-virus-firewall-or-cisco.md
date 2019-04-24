---
title: Basculement vers EOP à partir de Google Postini, Barracuda Spam and Virus Firewall, ou Cisco IronPort
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 81b75194-3b04-48da-8b81-951afbabedde
description: Le but de cette rubrique est de vous aider à comprendre le processus de passage d'un équipement de protection de messagerie électronique local ou d'un service de protection dans le nuage à Exchange Online Protection (EOP), puis de vous fournir les ressources d'aide nécessaires pour commencer à l'utiliser.
ms.openlocfilehash: 0c33d89be5cb4ebf7719e6742532ebfc7a2e5c20
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256202"
---
# <a name="switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco-ironport"></a>Basculement vers EOP à partir de Google Postini, Barracuda Spam and Virus Firewall, ou Cisco IronPort

 Le but de cette rubrique est de vous aider à comprendre le processus de passage d'un équipement de protection de messagerie électronique local ou d'un service de protection dans le nuage à Exchange Online Protection (EOP), puis de vous fournir les ressources d'aide nécessaires pour commencer à l'utiliser. Il existe de nombreuses solutions de filtrage du courrier indésirable, mais le processus de passage à EOP est généralement similaire.
  
Si vous découvrez EOP et souhaitez avoir un aperçu de ses fonctionnalités avant de vous décider, commencez par lire la rubrique [Vue d'ensemble d'Exchange Online Protection](exchange-online-protection-overview.md) sur TechNet. 
  
Avant de passer à EOP, il est important que vous déterminiez si vous voulez héberger vos boîtes aux lettres protégées par EOP dans le nuage avec Exchange Online, localement ou dans un scénario hybride (hybride signifie que certaines boîtes aux lettres sont hébergées localement, et d'autres avec Exchange Online). Chacun de ces scénarios d'hébergement (en nuage, local et hybride) est possible, mais les étapes de configuration peuvent varier. Voici quelques considérations pour vous aider à choisir le déploiement approprié :
  
- **Protection EOP avec boîtes aux lettres locales** Ce scénario est approprié si vous disposez d'une infrastructure d'hébergement de messagerie que vous souhaitez utiliser, ou si votre organisation exige la conservation des boîtes aux lettres localement, et si vous souhaitez bénéficier de la protection du courrier électronique en nuage offerte par EOP. Pour plus d'informations sur ce scénario, consultez la rubrique [Passage à EOP autonome](#switch-to-eop-standalone). 
    
- **Protection EOP avec boîtes aux lettres Exchange Online** Ce scénario est approprié si vous voulez une protection EOP avec hébergement de toutes vos boîtes aux lettres dans le nuage. Il peut s'avérer plus simple, car il ne nécessite pas le maintien de serveurs de messagerie locaux. La rubrique [Passage à Exchange Online](switch-to-eop-from-google-postini-the-barracuda-spam-and-virus-firewall-or-cisco.md#BKMK_SwitchEXO) décrit ce scénario. 
    
- **Protection EOP avec boîtes aux lettres hybride** Vous voulez des boîtes aux lettres en nuage, mais vous devez conserver des boîtes aux lettres locales pour certains utilisateurs. Ce scénario est approprié si vous voulez conserver certaines boîtes aux lettres localement, et héberger les autres avec Exchange Online. [Passage à une solution hybride](#switch-to-a-hybrid-solution) décrit ce scénario. 
    
## <a name="switch-to-eop-standalone"></a>Passage à EOP autonome

Si vous hébergez actuellement vos boîtes aux lettres localement et utilisez un équipement de protection local ou un service de protection de messagerie dans le nuage, vous pouvez passer à EOP pour bénéficier de ses fonctionnalités de protection et sa disponibilité. Pour configurer EOP dans un scénario autonome, c'est-à-dire consistant à héberger vos boîtes aux lettres localement et à utiliser EOP pour assurer la protection du courrier électronique, vous pouvez procéder de la manière décrite dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md). Cette rubrique décrit les étapes de configuration de la protection EOP, qui incluent l'inscription, l'ajout de votre domaine et la configuration de votre flux de messagerie avec des connecteurs.
  
## <a name="switch-to-exchange-online"></a>Passage à Exchange Online
<a name="BKMK_SwitchEXO"> </a>

Peut-être avez-vous des boîtes aux lettres locales protégées par un équipement local, et souhaitez-vous passer à des boîtes aux lettres Exchange Online hébergées dans le nuage et à la protection EOP pour bénéficier des fonctionnalités de messagerie et de protection d'Office 365. Pour commencer, vous pouvez vous inscrire à Office 365, puis ajouter votre domaine. Ce scénario ne requiert aucune configuration de connecteurs, car il n'y a aucun routage vers des boîtes aux lettres locales. Commencez à la [page d'inscription à Office 365](https://www.microsoft.com/en-us/office365/online-software.aspx). (La rubrique [Prise en main d'Office 365](https://go.microsoft.com/fwlink/p/?LinkId=275407) vous permettra de découvrir ses fonctionnalités.) 
  
Durant le processus de configuration d'Office 365, vous allez créer vos utilisateurs de boîtes aux lettres en nuage.
  
## <a name="switch-to-a-hybrid-solution"></a>Passage à une solution hybride
<a name="BKMK_SwitchHybrid"> </a>

Il se peut que vous vouliez déplacer uniquement une partie de vos boîtes aux lettres vers le nuage en raison d'exigences propres à votre organisation ou de considérations réglementaires. Lorsque vous déployez un scénario hybride, vous pouvez déplacer des boîtes aux lettres vers le nuage conformément aux exigences de votre organisation. Une migration vers un environnement hybride avec protection EOP est plus compliquée qu'un scénario de déplacement complet dans le nuage. Toutefois, Microsoft offre une prise en charge complète du scénario hybride et de nombreuses ressources pour faciliter le déplacement hybride.
  
Si vous envisagez un déploiement hybride, nous vous recommandons de commencer par lire la rubrique [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx). En outre, il y a plusieurs façons d'acheminer du courrier électronique dans un scénario hybride. Il est important de les comprendre. La rubrique [Transport Routing in Exchange 2013 Hybrid Deployments](http://technet.microsoft.com/library/36c2cea3-2e2f-40ac-88bd-7e1b6bd27828.aspx) décrit les différentes possibilités pour vous permettre de choisir le meilleur scénario de routage en fonction des exigences de votre organisation. 
  
## <a name="migration-planning"></a>Planification de la migration
<a name="sectionSection3"> </a>

Si vous décidez de passer à EOP, soyez particulièrement attentif aux aspects suivants :
  
- **Règles de filtrage personnalisées** Si vous avez des règles de filtrage ou de stratégie d'entreprise personnalisées pour intercepter des courriers indésirables spécifiques, nous vous recommandons d'essayer EOP avec les paramètres par défaut pour une période, avant de migrer vos règles. EOP offre une protection contre le courrier indésirable au niveau de l'entreprise avec les paramètres par défaut, il se peut que vous n'ayez pas besoin de migrer certaines de vos règles vers EOP. Bien entendu, si vous avez des règles en place qui appliquent des stratégies d'entreprise personnalisées spécifiques, vous pouvez les créer. Les [règles de flux de messagerie (règles de transport) dans Exchange Online Protection](mail-flow-rules-transport-rules-0.md) fournissent des instructions détaillées sur la création de règles de flux de messagerie dans EOP. 
    
- **Listes vertes IP et listes rouges IP** Si vous avez des listes vertes et rouges basées sur les utilisateurs, dans le cadre du processus de configuration, prévoyez un peu de temps pour la copie de ces dernières vers EOP. Pour plus d'informations sur les listes d'adresses IP autorisées et les listes d'adresses IP bloquées, consultez [la rubrique Configure the connection filter Policy](../configure-the-connection-filter-policy.md).
    
- **Communication sécurisée** Si vous avez un partenaire exigeant une messagerie chiffrée, nous vous recommandons de configurer la communication sécurisée dans le Centre d'administration Exchange. Pour configurer ce scénario, consultez la rubrique [Create connectors for a secure mail channel using transport layer security (TLS)](http://technet.microsoft.com/library/1ce4d6a4-41ba-4d1e-9ca9-e826252c1041.aspx).
    
> [!TIP]
> Lorsque vous passez d'un équipement local à EOP, vous pouvez conserver votre équipement ou un serveur pour effectuer les contrôles de règle d'entreprise. Par exemple, si votre équipement effectue un filtrage personnalisé du courrier sortant et si vous souhaitez qu'il continue à le faire, vous pouvez configurer EOP pour envoyer le courrier directement à l'équipement afin d'effectuer un filtrage supplémentaire avant son routage vers Internet. La rubrique [Exchange Online Protection Connectors - Outbound Smart Host Scenario](http://technet.microsoft.com/library/431b3f02-4efd-4bd3-94e7-eecd03f8ef5e.aspx) décrit comment configurer le flux de messagerie dans ce cas. 
  

