---
title: Flux de courrier entrant et sortant
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Les administrateurs peuvent en savoir plus sur le widget flux de messagerie sortant et entrant dans le tableau de bord de flux de messagerie dans le centre de sécurité & de la sécurité d'Office 365.
ms.openlocfilehash: b3e92228506267e674f2f428fab1ef54d5aee38e
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720284"
---
# <a name="outbound-and-inbound-mail-flow"></a>Flux de courrier entrant et sortant

Le widget **flux de messagerie sortant et** entrant combine les informations du rapport du **connecteur** et de l'ancien **rapport de vue d'ensemble TLS** à un emplacement unique.

![Le rapport des flux de messagerie entrants et sortants dans le tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

Les informations contenues dans le widget sont liées aux connecteurs et à la protection des messages TLS dans Office 365. Pour plus d'informations, voir les rubriques suivantes :

- [Configure mail flow using connectors in Office 365](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a>Message protégé en transit (par TLS)

Le widget **flux de messagerie entrant et sortant** affiche le chiffrement TLS utilisé pour la connexion lorsque des messages sont remis à partir de votre organisation Office 365. Les connexions établies avec d'autres services de messagerie sont chiffrées par TLS lorsque TLS est offert par les deux côtés. Le widget offre un instantané de la dernière semaine du flux de messagerie. Lorsque vous cliquez sur **afficher les détails**, le menu volant **message protégé en transit (par TLS)** vous indique la protection TLS pour les messages entrants et sortants de votre organisation.

![Le menu volant messages protégés en transit (par TLS) dans le centre de sécurité & de la sécurité d'Office 365](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

Actuellement, TLS 1,2 est la version la plus sécurisée de TLS offerte par Office 365. En règle générale, vous devez déterminer le chiffrement TLS utilisé pour les audits de conformité. Vous n'avez probablement pas de relation directe avec la plupart des serveurs de messagerie source et de destination (vous n'êtes pas propriétaire, ni Microsoft), de sorte que vous n'avez pas de nombreuses options pour améliorer le chiffrement TLS utilisé par ces serveurs.

Toutefois, vous pouvez utiliser des [connecteurs](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) pour garantir la meilleure protection TLS disponible pour les messages échangés entre vos serveurs de messagerie et Office 365. Le flux de messagerie entre Office 365 et vos propres serveurs de messagerie ou serveurs qui appartiennent à vos partenaires est souvent plus important et plus sensible que les messages normaux, de sorte que vous souhaitez appliquer une sécurité supplémentaire et la vigilance de ces messages. Vous pouvez mettre à niveau ou réparer vos propres serveurs de messagerie pour améliorer le chiffrement TLS utilisé ou contacter vos partenaires pour qu'ils effectuent la même opération. Le **rapport de connecteur** affiche le volume de flux de messagerie et le chiffrement TLS pour les messages qui utilisent vos connecteurs Office 365.

## <a name="connector-report"></a>Rapport de connecteur

Lorsque vous cliquez sur le lien du **rapport de connecteur** à partir de la fenêtre mobile **message protégé en transit (par TLS)** , le rapport affiche des informations sur les messages qui sont remis vers et depuis votre organisation Office 365 à l'aide de connecteurs. Vous utilisez des connecteurs entre vos propres serveurs de messagerie et Office 365 ou les serveurs de votre partenaire et Office 365. Le volume de messages pour chaque connecteur et le chiffrement TLS pour la connexion sont disponibles. En outre, vous pouvez également afficher des données pour les messages qui ont été envoyés ou reçus dans Office 365 sans utiliser de connecteur.

L'affichage **flux de messagerie** indique le volume de messages par le biais du connecteur pour la semaine précédente. Vous pouvez modifier la plage de dates en sélectionnant **Filtrer** où vous pouvez augmenter la plage à un maximum de 30 jours. La vue **tout le flux de messagerie** affiche tout le flux de messagerie vers et depuis votre organisation Office 365 via tous les connecteurs. Vous pouvez sélectionner un connecteur spécifique par nom dans le menu déroulant.

Vous pouvez sélectionner l'affichage **utilisation de TLS** dans la liste déroulante pour afficher la répartition de la protection TLS pour les messages via le connecteur. Comme avec le rapport de **rapport de vue d'ensemble TLS** , cette vue indique le pourcentage des différentes versions de TLS. Pour les connexions 1,0 TLS, vous devez vraiment obtenir votre serveur de messagerie ou le serveur de votre partenaire mis à niveau ou résolu afin d'éviter tout problème lorsque la prise en charge de TLS 1,0 est finalement déconseillée dans Office 365. Pour plus d'informations, voir informations de [référence technique sur le chiffrement dans Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).

Insights pointent vers des connecteurs pour attirer votre attention sur les éventuels problèmes de chiffrement TLS pour le connecteur. Les informations sont les suivantes: le chiffrement **TLS est supérieur à 25%** ou **TLS 1,0 est supérieur à 50%**. Si vous voyez ces informations, vous devez examiner vos serveurs de messagerie qui sont associés au connecteur ou contacter votre organisation partenaire.

## <a name="see-also"></a>Voir aussi

Pour plus d'informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights.md).
