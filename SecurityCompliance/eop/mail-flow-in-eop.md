---
title: Flux de messagerie dans EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Étant donné que vous êtes client Exchange Online Protection (EOP), tous les messages envoyés à votre organisation transitent par EOP avant que vos collaborateurs ne les voient. Que vous hébergiez l'ensemble de vos boîtes aux lettres dans le nuage avec Exchange Online ou localement (scénario dit autonome) pour éventuellement continuer à tirer parti de votre infrastructure existante, vous avez plusieurs possibilités de router les messages qui transiteront par EOP dans le cadre de leur traitement avant qu'ils ne soient acheminés vers les boîtes de réception de vos collaborateurs.
ms.openlocfilehash: 2081aff8da44244a1476b51eed49e5f23a5a9b9a
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676761"
---
# <a name="mail-flow-in-eop"></a>Flux de messagerie dans EOP

Étant donné que vous êtes client Exchange Online Protection (EOP), tous les messages envoyés à votre organisation transitent par EOP avant que vos collaborateurs ne les voient. Que vous hébergiez l'ensemble de vos boîtes aux lettres dans le nuage avec Exchange Online ou localement (scénario dit autonome) pour éventuellement continuer à tirer parti de votre infrastructure existante, vous avez plusieurs possibilités de router les messages qui transiteront par EOP dans le cadre de leur traitement avant qu'ils ne soient acheminés vers les boîtes de réception de vos collaborateurs.
  
Vous pouvez personnaliser le routage des messages pour que votre messagerie réponde à vos besoins métiers. Par exemple, vous avez la possibilité d'utiliser un équipement de filtrage de stratégie pour tous vos messages sortants.
  
## <a name="working-with-messages-and-message-access-options"></a>Utilisation des messages et des options d’accès aux messages

EOP vous propose plusieurs possibilités de router vos messages en toute flexibilité. Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.
  
[Utiliser le blocage du périmètre basé sur l’annuaire pour rejeter les messages envoyés à des destinataires non valides](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-directory-based-edge-blocking) Décrit la fonctionnalité de blocage du périmètre basée sur l’annuaire, qui vous permet de rejeter les messages pour les destinataires non valides au niveau du périmètre réseau du service. 
  
La rubrique [View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) décrit la façon de gérer les domaines associés à votre service EOP.
  
Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi. Pour en savoir plus sur les sous-domaines, consultez la rubrique [Enable mail Flow for subdomains in Exchange Online](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/enable-mail-flow-for-subdomains).
  
La rubrique [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) présente les connecteurs et explique comment vous pouvez les utiliser pour personnaliser le routage des messages. Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.
  
Vous pouvez vous assurer que le courrier indésirable est correctement routé vers le dossier Courrier indésirable de chaque utilisateur en effectuant quelques opérations de configuration. Ces éléments sont détaillés dans la vérification que le courrier indésirable [est acheminé vers le dossier de courrier indésirable de chaque utilisateur](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Si vous ne souhaitez pas déplacer les messages vers le dossier Courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](../configure-your-spam-filter-policies.md).
  
## <a name="verify-mail-flow"></a>Vérifier le flux de messagerie

Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).
  
[Test du flux de messagerie en validant vos connecteurs Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/test-mail-flow) fournit des instructions pour vérifier que votre flux de messagerie est correctement configuré.
