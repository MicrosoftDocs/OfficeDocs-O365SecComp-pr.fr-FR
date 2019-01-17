---
title: Flux des messages entrants et sortants
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Administrateurs peuvent en savoir plus sur les widget de flux de messages entrants dans le tableau de bord du flux de messagerie dans le centre de conformité de & Office 365 sécurité sortante.
ms.openlocfilehash: 57792c0347490b40f97a8b92945a9c809484ba4f
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685424"
---
# <a name="outbound-and-inbound-mail-flow"></a>Flux des messages entrants et sortants

Le widget **sortant et flux de messages entrants** combine les informations de l' **État du connecteur** et l' ancien **TLS vue d’ensemble du rapport** à un seul endroit.

![L’état de flux de messagerie sortant et entrant dans le tableau de bord du flux de messagerie dans le centre de conformité de & Office 365 sécurité](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

Les informations contenues dans le widget sont liées à des connecteurs et la protection des messages TLS dans Office 365. Pour plus d’informations, voir les rubriques suivantes :

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Message protégé en transit (par TLS)

Le widget **sortant et flux de messages entrants** affiche le chiffrement TLS qui est utilisé pour la connexion lorsque les messages sont remis vers et depuis votre organisation Office 365. Les connexions sont établies avec d’autres services de messagerie sont chiffrées par TLS lors de TLS est fourni par les deux côtés. Le widget offre un instantané de la dernière semaine du flux de messagerie. Lorsque vous cliquez sur **Afficher les détails**, le **Message est protégé en transit (par TLS)** flottant montre la protection TLS pour les messages entrants et sortants de votre organisation.

![Les Messages protégés en transit (par TLS) flottant dans le centre de conformité de & Office 365 sécurité](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Actuellement, TLS 1.2 est la version la plus sécurisée de TLS est proposé par Office 365. Souvent, vous devrez connaître le chiffrement TLS qui est utilisé pour des audits de conformité. Ne présentent pas un lien direct avec la plupart des serveurs e-mail source et de destination (vous ne possédez pas les et ni ne Microsoft), ce qui évite de nombreuses options pour améliorer le chiffrement TLS qui est utilisé par ces serveurs.

Mais, vous pouvez utiliser des [connecteurs](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) pour assurer la meilleure TLS protection disponibles pour les messages envoyés entre les serveurs de messagerie Office 365. Flux de messagerie entre Office 365 et vos propres serveurs de messagerie ou les serveurs qui appartiennent à vos partenaires est souvent plus importante et sensibles que des messages ordinaires, et il vous faudra appliquer une sécurité accrue et vigilance à ces messages. Vous pouvez mettre à niveau ou corriger vos propres serveurs de messagerie pour améliorer le chiffrement TLS est utilisé, ou en contact avec vos partenaires à faire de même. Le **Connecteur de rapport** affiche volume de flux de messagerie et le chiffrement TLS pour les messages qui utilisent des connecteurs Office 365.

## <a name="connector-report"></a>Rapport de connecteur

Lorsque vous cliquez sur le lien **Rapport du connecteur** à partir de la fenêtre de **Message est protégé en transit (par TLS)** mobile, le rapport affiche des informations sur les messages sont remis vers et depuis votre organisation Office 365 à l’aide de connecteurs. Vous utilisez des connecteurs entre vos propres serveurs de messagerie et Office 365 ou de votre partenaire les serveurs et Office 365. Le volume de message pour chaque connecteur et le chiffrement TLS pour la connexion sont disponibles. En outre, vous pouvez également afficher les données pour les messages qui ont été envoyés ou reçus dans Office 365 sans l’aide d’un connecteur.

Le **Flux de messagerie** affiche le volume des messages via le connecteur pour la semaine. Vous pouvez modifier la plage de dates en sélectionnant **filtre** où vous pouvez augmenter la plage pour un maximum de 30 jours. L’affichage de **Tous les flux de messagerie** affiche flux de messages vers et depuis votre organisation Office 365 par le biais de tous les connecteurs. Vous pouvez sélectionner un connecteur spécifique par un nom dans le menu déroulant.

Vous pouvez sélectionner l’affichage de **l’utilisation TLS** dans la liste déroulante pour afficher la répartition de protection TLS pour les messages via le connecteur. Comme avec le rapport **d’État de vue d’ensemble de TLS** , cet affichage indique le pourcentage de différentes versions TLS. Pour les connexions TLS 1.0, vous devez vraiment obtenir votre serveur de messagerie ou le serveur de votre partenaire mis à niveau ou fixe éviter des problèmes lors de la prise en charge TLS 1.0 est finalement déconseillé dans Office 365. Pour plus d’informations, voir [informations de référence technique de chiffrement dans Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

Insights pointent sur connecteurs pour attirer votre attention sur les problèmes potentiels de chiffrement TLS pour le connecteur. Les analyses sont : **No TLS est plus de 25 %** ou **TLS 1.0 est supérieure à 50 %**. Si vous voyez ces informations, vous devez examiner les serveurs de messagerie qui sont associés avec le connecteur ou en contact avec votre organisation partenaire.
