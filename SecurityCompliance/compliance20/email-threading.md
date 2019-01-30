---
title: Threads de courrier électronique
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
ms.openlocfilehash: 2340128f508a3be389afce86596f7e6395a0bb7e
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607695"
---
# <a name="email-threading"></a><span data-ttu-id="f38c8-102">Threads de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f38c8-102">Email threading</span></span>
<span data-ttu-id="f38c8-p101">Envisagez une conversation électronique qui a été passer un certain temps. Dans la plupart des cas, le dernier e-mail sur le thread inclut le contenu de tous les messages ci-dessus. consulter le dernier e-mail donnera un contexte complet de la conversation qui s’est produite dans le thread. Messagerie threading identifie ces e-mails afin que les réviseurs peuvent consulter une fraction des documents collectées sans perdre le contexte de le.</span><span class="sxs-lookup"><span data-stu-id="f38c8-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="f38c8-106">À quoi threading du courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="f38c8-106">What does email threading do?</span></span>
<span data-ttu-id="f38c8-p102">Messagerie threading analyse chaque desconstructs et messagerie pour des messages individuels ; chaque e-mail est une chaîne de messages individuels. Ensuite, il analyse tous les messages électroniques dans le jeu de travail pour déterminer si un message électronique comporte un contenu unique ou si la chaîne est entièrement contenue dans une autre adresse e-mail. À la fin des messages électroniques sont divisées en quatre catégories :</span><span class="sxs-lookup"><span data-stu-id="f38c8-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>
- <span data-ttu-id="f38c8-110">Inclusives : le dernier message dans le courrier électronique comporte un contenu unique et le courrier électronique a toutes les pièces jointes qui ont été inclus dans les autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.</span><span class="sxs-lookup"><span data-stu-id="f38c8-110">Inclusives: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="f38c8-111">Inclus moins : le dernier message dans le courrier électronique comporte un contenu unique, mais le courrier électronique ne contient-elle pas certaines pièces jointes qui ont été inclus dans les autres messages électroniques dont le contenu est entièrement contenu dans ce message électronique.</span><span class="sxs-lookup"><span data-stu-id="f38c8-111">Inclusive minus: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>
- <span data-ttu-id="f38c8-112">Copie inclus : une copie exacte d’un inclus/inclus moins de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f38c8-112">Inclusive copy: an exact copy of an inclusive/inclusive minus email</span></span>
- <span data-ttu-id="f38c8-113">Aucun : Le contenu de ce message est entièrement contenu dans au moins un message électronique qui est marquée comme étant moins (inclus) / (inclus).</span><span class="sxs-lookup"><span data-stu-id="f38c8-113">None: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="f38c8-114">Quelle est la différence des conversations dans Outlook ?</span><span class="sxs-lookup"><span data-stu-id="f38c8-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="f38c8-p103">En un coup de œil, cela similaire aux groupes de conversation dans Outlook. Toutefois, il existe certaines différences importantes. Prendre en compte une conversation électronique qui a été répliquée dans les deux conversation ; par exemple, une personne a répondu à un message électronique qui n’est pas la plus récente de la conversation donc les deux dernières courriers électroniques dans la conversation à la fois un contenu unique.</span><span class="sxs-lookup"><span data-stu-id="f38c8-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="f38c8-p104">Outlook regroupera toujours les courriers électroniques dans une même conversation ; lecture uniquement le dernier e-mail signifie pas le contexte du message de la dernière seconde, qui contient également un contenu unique. Messagerie threading analyse chaque e-mail dans des composants individuels et les compare, messagerie threading serait marquer les deux de ces deux dernières e-mails comme inclusives, en vous assurant que vous ne manquez pas le contexte de le tant que lire tous les messages marqués comme inclus.</span><span class="sxs-lookup"><span data-stu-id="f38c8-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>