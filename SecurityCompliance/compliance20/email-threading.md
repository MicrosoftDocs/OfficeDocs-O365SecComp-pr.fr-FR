---
title: Threading de messagerie
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ca4823ecfc06ddc0ef6f6840ad55fec492ac472c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243805"
---
# <a name="email-threading"></a>Threading de messagerie

Considérez une conversation par courrier électronique qui s'est en cours pendant un certain temps. Dans la plupart des cas, le dernier courrier électronique sur le thread inclura le contenu de tous les messages électroniques précédents; en examinant le dernier courrier électronique, vous obtiendrez un contexte complet de la conversation qui s'est produite dans le fil de discussion. Le Threading de messagerie identifie ces messages afin que les réviseurs puissent examiner une partie des documents collectés sans perdre de contexte.

## <a name="what-does-email-threading-do"></a>Qu'est-ce que le Threading du courrier électronique?

Le Threading de messagerie analyse chaque message électronique et les desconstructs à des messages individuels; chaque message électronique est une chaîne de messages individuels. Ensuite, il analyse tous les messages électroniques du jeu de travail afin de déterminer si un e-mail a un contenu unique ou si la chaîne est entièrement contenue dans un autre message électronique. Dans les messages électroniques finaux se répartissent en quatre catégories:

- **Inclus**: le dernier message de l'e-mail a un contenu unique, et le courrier électronique contient toutes les pièces jointes incluses dans d'autres messages électroniques dont le contenu est entièrement contenu dans cet e-mail.


- **Inclusif**: le dernier message de l'e-mail a un contenu unique, mais le courrier électronique ne contient pas certaines pièces jointes incluses dans d'autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.

- **Copie inclusive**: une copie exacte d'un message électronique inclusif/inclusif

- **None**: le contenu de ce message électronique est entièrement contenu dans au moins un e-mail marqué comme inclusif/inclusif.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Quelle est la différence entre les conversations dans Outlook?
En un clin d'œil, cela semble très semblable aux groupements de conversation dans Outlook. Toutefois, il existe des distinctions importantes. Considérez une conversation par courrier électronique qui a été divisée en deux conversations; par exemple, quelqu'un a répondu à un message électronique qui n'est pas le dernier de la conversation, les deux derniers messages de la conversation ont un contenu unique.

Outlook regroupera les messages électroniques en une seule conversation; la lecture du dernier courrier électronique ne signifie pas qu'il manque le contexte de l'avant-dernier e-mail, qui contient également du contenu unique. Étant donné que le Threading de messagerie analyse chaque courrier électronique dans des composants individuels et les compare, le Threading de courrier électronique marque les deux derniers courriers électroniques comme étant inclusifs, ce qui vous permettra de ne pas manquer de contexte tant que vous lisez tous les messages électroniques marqués comme inclus.