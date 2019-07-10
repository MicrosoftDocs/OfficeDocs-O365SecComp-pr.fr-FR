---
title: Informations sur les règles de flux de messagerie lent
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 5/3/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Les administrateurs peuvent en savoir plus sur les règles de flux de messagerie lentes du tableau de bord de flux de messagerie dans le centre de sécurité & conformité.
ms.openlocfilehash: 4477b388df321ee774ec7916a695cbfc69fc8e87
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598070"
---
# <a name="slow-mail-flow-rules-insight"></a>Informations sur les règles de flux de messagerie lent

Des règles inefficaces de flux de messagerie (également appelées règles de transport) peuvent entraîner des retards de flux de messagerie pour votre organisation. Cette vue d’État indique les règles de flux de messagerie qui ont un impact sur le flux de messagerie de votre organisation. Voici des exemples de ces types de règles:

- Conditions utilisées par **est membre de** pour les grands groupes.

- Conditions qui utilisent des critères de correspondance des expressions régulières complexes (Regex).

- Conditions d’utilisation de l’archivage de contenu dans les pièces jointes.

Le centre d’analyse vous aidera à identifier et à ajuster les règles de flux de messagerie afin de réduire les délais de flux de messagerie.

![Des règles de flux de messagerie lentes dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

Lorsque vous cliquez sur **afficher les détails**, un volet flyout apparaît dans lequel vous pouvez examiner la règle. Dans le volet flyout, peut également cliquer sur **afficher les exemples de messages** pour voir les types de messages concernés par la règle.

![Volet flyout après avoir cliqué sur Afficher les détails dans une règle de flux de messagerie lente vue d’ensemble du tableau de bord de flux de messagerie](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

## <a name="see-also"></a>Voir aussi

Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security & Compliance Center](mail-flow-insights.md).
