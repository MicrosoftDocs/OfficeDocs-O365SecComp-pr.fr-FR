---
title: Flux de messagerie dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/13/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Étant donné que vous êtes client Exchange Online Protection (EOP), tous les messages envoyés à votre organisation transitent par EOP avant que vos collaborateurs ne les voient. Que vous hébergiez l'ensemble de vos boîtes aux lettres dans le nuage avec Exchange Online ou localement (scénario dit autonome) pour éventuellement continuer à tirer parti de votre infrastructure existante, vous avez plusieurs possibilités de router les messages qui transiteront par EOP dans le cadre de leur traitement avant qu'ils ne soient acheminés vers les boîtes de réception de vos collaborateurs.
ms.openlocfilehash: d35e6f2fdbe7bb991ebf3d766fadae34638831ef
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027341"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="ef627-104">Flux de messagerie dans EOP</span><span class="sxs-lookup"><span data-stu-id="ef627-104">Mail flow in EOP</span></span>

<span data-ttu-id="ef627-p102">Étant donné que vous êtes client Exchange Online Protection (EOP), tous les messages envoyés à votre organisation transitent par EOP avant que vos collaborateurs ne les voient. Que vous hébergiez l'ensemble de vos boîtes aux lettres dans le nuage avec Exchange Online ou localement (scénario dit autonome) pour éventuellement continuer à tirer parti de votre infrastructure existante, vous avez plusieurs possibilités de router les messages qui transiteront par EOP dans le cadre de leur traitement avant qu'ils ne soient acheminés vers les boîtes de réception de vos collaborateurs.</span><span class="sxs-lookup"><span data-stu-id="ef627-p102">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>
  
<span data-ttu-id="ef627-p103">Vous pouvez personnaliser le routage des messages pour que votre messagerie réponde à vos besoins métiers. Par exemple, vous avez la possibilité d’utiliser un équipement de filtrage de stratégie pour tous vos messages sortants.</span><span class="sxs-lookup"><span data-stu-id="ef627-p103">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span> 
  
## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="ef627-109">Utilisation des messages et des options d’accès aux messages</span><span class="sxs-lookup"><span data-stu-id="ef627-109">Working with messages and message access options</span></span>

<span data-ttu-id="ef627-p104">EOP vous propose plusieurs possibilités de router vos messages en toute flexibilité. Les rubriques suivantes expliquent les étapes composant le processus de flux de messages.</span><span class="sxs-lookup"><span data-stu-id="ef627-p104">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>
  
<span data-ttu-id="ef627-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Décrit la fonction de blocage du périmètre basé sur l'annuaire, qui permet de rejeter les messages adressés à des destinataires non valides sur le périmètre du réseau de service.</span><span class="sxs-lookup"><span data-stu-id="ef627-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span> 
  
<span data-ttu-id="ef627-113">La rubrique [View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx) décrit la façon de gérer les domaines associés à votre service EOP.</span><span class="sxs-lookup"><span data-stu-id="ef627-113">[View or Edit Managed Domains in EOP](http://technet.microsoft.com/library/69523bec-07ee-46f9-ae08-40437e39b87c.aspx) describes how to manage domains that are associated with your EOP service.</span></span> 
  
<span data-ttu-id="ef627-p105">Si vous ajoutez des sous-domaines dans votre organisation, votre service EOP peut vous aider à les gérer aussi. Pour plus d'informations sur les sous-domaines, voir [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef627-p105">If you add subdomains to your organization, your EOP service can help you manage these too. Learn more about subdomains at [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span></span>
  
<span data-ttu-id="ef627-p106">La rubrique [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) présente les connecteurs et explique comment vous pouvez les utiliser pour personnaliser le routage des messages. Les scénarios décrivent la procédure pour assurer une communication sécurisée avec une organisation partenaire et configurer un hôte actif.</span><span class="sxs-lookup"><span data-stu-id="ef627-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span> 
  
<span data-ttu-id="ef627-p107">Pour vous assurer que le courrier indésirable est routé correctement au dossier de courrier électronique indésirable de chaque utilisateur, vous devez effectuer quelques étapes de configuration. Celles-ci sont détaillées dans [vous assurer que le courrier indésirable est routé vers le dossier courrier indésirable de chaque utilisateur](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Si vous ne souhaitez pas déplacer les messages vers le dossier de courrier électronique indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de filtrage de contenu dans le centre d’administration Exchange. Pour plus d’informations, voir [configurer vos stratégies de filtrage du courrier indésirable](../configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ef627-p107">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps. These are detailed in [Ensure that spam is routed to each user's Junk Email folder](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span></span>
  
## <a name="verify-mail-flow"></a><span data-ttu-id="ef627-122">Vérifier le flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="ef627-122">Verify mail flow</span></span>

<span data-ttu-id="ef627-p108">Pour vérifier que votre configuration d'EOP, y compris celle de votre connecteur, fonctionne correctement, consultez la section « Comment savoir si cette tâche a fonctionné ? » dans la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="ef627-p108">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span> 
  
<span data-ttu-id="ef627-125">La rubrique [Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) propose des instructions pour vérifier que votre flux de messages est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="ef627-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) provides instructions for testing that your mail flow is set up correctly.</span></span> 
  

