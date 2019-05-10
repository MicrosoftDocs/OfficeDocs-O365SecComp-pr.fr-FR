---
title: Corriger l’adresse de domaine de l’expéditeur
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent en savoir plus sur la rubrique Fix sender Domain Insight dans le tableau de bord du flux de messagerie dans le centre de sécurité & Compliance Center.
ms.openlocfilehash: a285a1c744ca540cc58b9408b4ee31e768f89479
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868562"
---
# <a name="fix-sender-domain-insight"></a>Corriger l’adresse de domaine de l’expéditeur

Office 365 nécessite des messages envoyés depuis des environnements de messagerie internes locaux vers Office 365 pour répondre à certains critères de sécurité:

- Vous avez créé un connecteur entrant dans Office 365 pour authentifier les connexions SMTP à partir de votre serveur de messagerie local à l’aide de l’adresse IP source ou d’un certificat.

- Vous avez configuré votre serveur de messagerie local de sorte qu’il relaie le courrier électronique via Office 365 vers un environnement externe.

- Dans votre configuration, l’une des affirmations suivantes est vraie:

  - Le domaine de messagerie de l’expéditeur est enregistré dans votre organisation Office 365. Pour plus d’informations, consultez la rubrique ajouter des domaines dans Office 365.

  - Votre serveur de messagerie local est configuré pour utiliser un certificat pour envoyer des courriers électroniques à Office 365, le certificat contient ou correspond exactement à un nom de domaine que vous avez enregistré dans Office 365 et vous avez créé un connecteur basé sur un certificat dans Office 365 avec ce domaine. 

Les messages qui ne répondent pas aux critères ne sont pas attribués à l’organisation et peuvent être rejetés.

La fonction **Fix sender Domain** Insight affiche les messages électroniques provenant de votre environnement local qui ne répondent pas aux critères, vous permet d’identifier les ordinateurs et les comptes d’utilisateur potentiellement compromis dans votre environnement de messagerie local et vous aide à prendre actions de correction.

![La fonction Fix sender Domain Insight dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center](media/sender-domain-insight-selected.png)

Lorsque vous cliquez sur **afficher les détails**, vous êtes dirigé vers un autre widget avec plus de détails, comme illustré dans le diagramme suivant:

![Le widget détails de la solution Fix sender Domain Insight](media/sender-domain-view-details.png)

Vous verrez le connecteur entrant qui a été utilisé pour livrer les messages à Office 365. Vous pouvez également cliquer sur **afficher un exemple d’ID de message** pour afficher les détails des messages qui ont été envoyés à partir de votre environnement de messagerie local. Étant donné que ces messages ont été rejetés par Office 365, vous ne pouvez pas utiliser le suivi des messages, mais vous pouvez utiliser l’exemple d’ID de message pour suivre les messages dans votre environnement de messagerie local.

![Afficher des exemples d’ID de message dans la fenêtre Fix sender Domain Insight](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a>Voir aussi

Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights-v2.md).
