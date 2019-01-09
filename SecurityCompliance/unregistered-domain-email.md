---
title: Courrier électronique de domaine non inscrit
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Si vous envoyez un volume élevé de messagerie du domaine ou non, vous courez le risque de votre courrier électronique bloqué. Lisez cet article pour en savoir plus.
ms.openlocfilehash: f632c5f7ab94a200a364828408b13c0026335869
ms.sourcegitcommit: 03e64ead7805f3dfa9149252be8606efe50375df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27769781"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a>Non domaine Email : Ce que vous devez connaître

Permet à Office 365 pour les clients afin de relayer des messages via Exchange Online Protection (EOP). Un exemple pris en charge serait lorsque les utilisateurs ont une boîte aux lettres Office 365 et une personne externe les envoie un courrier électronique mais transfert de messages est configuré afin qu’il repasse à la boîte aux lettres externe. Il s’agit généralement dans les environnements de formation où les participants à tirer parti de leur interface électronique mais toujours obtenir courriels relatifs à l’école. Un autre exemple est lorsque les clients se trouvent dans un scénario hybride et des serveurs locaux envoyer un message électronique s’en déconnecter EOP.

## <a name="problems-with-unregistered-domains"></a>Problèmes liés à des domaines non enregistrés

Le problème est lorsque les serveurs locaux compromises et finissent par le relais d’un volume important de courrier indésirable en dehors d’EOP. Dans la plupart des cas, les connecteurs droite sont-ils mais courrier électronique est envoyé à partir de domaines non enregistrés, également appelé non. Office 365 autorise un montant raisonnable du courrier provenant de domaines ou non, mais un domaine accepté doit être configuré dans le centre d’administration pour chaque domaine que vous envisagez de l’envoi d’absence du bureau.

Une fois compromis, les clients n’est pas autorisées d’envoyer des messages sortants pour les domaines non enregistrés. Les utilisateurs recevront un rapport de remise (NDR) indique :

- 550 5.7.750 Service non disponible. Client bloqué à partir de l’envoi à partir de domaines non enregistrés

## <a name="unblocking-tenant-in-order-to-send-again"></a>Déblocage client afin d’envoyer à nouveau

Il existe plusieurs choses que vous devez faire si vous êtes bloqué pour l’envoi à partir de domaines non enregistrés :

1. Assurez-vous que vous avez enregistré tous vos domaines dans le centre d’administration Office 365. Vous pouvez trouver plus d’informations [ici](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).

2. Recherchez les connecteurs inhabituels. Acteurs malveillants crée souvent nouveaux connecteurs entrants dans votre organisation cliente Office 365 pour envoyer du courrier indésirable. Vous pouvez trouver plus d’informations sur la vérification de vos connecteurs [ici](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps). 

3. Verrouiller vos serveurs sur site et vous assurer qu’ils ne sont pas compromises.

> [!TIP]
> Il existe de nombreux facteurs impliqués ici, particulièrement si ces serveurs tiers. Cependant, vous devez être en mesure de vérifier que tous les messages en laissant vos serveurs sont légitimes.

4. Une fois que vous avez terminé, vous devez appeler le Support de Microsoft et demander à obtenir votre client déblocage pour renvoyer à partir de domaines ou non.  Il est utile de fournir le code d’erreur, mais vous devez prouver que votre environnement est sécurisé et que le courrier indésirable n’est pas envoyé à nouveau. Vous pouvez trouver plus d’informations sur l’ouverture d’un cas de prise en charge [ici](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).
  
## <a name="for-more-information"></a>Pour plus d’informations

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)

[Envoyer les notifications d'échec de remise par courrier électronique dans Office 365](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[Configurer le transfert du courrier pour une boîte aux lettres](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[Comment configurer une application ou un périphérique multi-fonction pour envoyer des courriers électroniques à l’aide d’Office 365](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

[Gérer les domaines acceptés dans Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).
