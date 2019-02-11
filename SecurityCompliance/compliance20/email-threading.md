---
title: Threading de messagerie
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d4328971a6b13c60c4d8b9f5b6db310d72a5b215
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29705995"
---
# <a name="email-threading"></a>Threading de messagerie

Envisagez une conversation électronique qui a été passer un certain temps. Dans la plupart des cas, le dernier e-mail sur le thread inclut le contenu de tous les messages ci-dessus. consulter le dernier e-mail donnera un contexte complet de la conversation qui s’est produite dans le thread. Messagerie threading identifie ces e-mails afin que les réviseurs peuvent consulter une fraction des documents collectées sans perdre le contexte de le.

## <a name="what-does-email-threading-do"></a>À quoi threading du courrier électronique ?

Messagerie threading analyse chaque desconstructs et messagerie pour des messages individuels ; chaque e-mail est une chaîne de messages individuels. Ensuite, il analyse tous les messages électroniques dans le jeu de travail pour déterminer si un message électronique comporte un contenu unique ou si la chaîne est entièrement contenue dans une autre adresse e-mail. À la fin des messages électroniques sont divisées en quatre catégories :

- **Comprises**: le dernier message dans le courrier électronique comporte un contenu unique et le courrier électronique a toutes les pièces jointes qui ont été inclus dans les autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.


- **Comprises moins**: le dernier message dans le courrier électronique comporte un contenu unique, mais le courrier électronique ne contient-elle pas certaines pièces jointes qui ont été inclus dans les autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.

- **Copie inclus**: une copie exacte d’un inclus/inclus moins de courrier électronique

- **Aucun**: le contenu de ce message est entièrement contenu dans au moins un message électronique qui est marquée comme étant moins (inclus) / (inclus).

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Quelle est la différence des conversations dans Outlook ?
En un coup de œil, cela similaire aux groupes de conversation dans Outlook. Toutefois, il existe certaines différences importantes. Prendre en compte une conversation électronique qui a été répliquée dans les deux conversation ; par exemple, une personne a répondu à un message électronique qui n’est pas la plus récente de la conversation donc les deux dernières courriers électroniques dans la conversation à la fois un contenu unique.

Outlook regroupera toujours les courriers électroniques dans une même conversation ; lecture uniquement le dernier e-mail signifie pas le contexte du message de la dernière seconde, qui contient également un contenu unique. Messagerie threading analyse chaque e-mail dans des composants individuels et les compare, messagerie threading serait marquer les deux de ces deux dernières e-mails comme inclusives, en vous assurant que vous ne manquez pas le contexte de le tant que lire tous les messages marqués comme inclus.