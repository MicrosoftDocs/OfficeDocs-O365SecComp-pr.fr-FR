---
title: Vidéos pour commencer à protéger votre courrier électronique
ms.author: tracyp
author: msfttracyp
ms.reviewer: andypunt
manager: laurawi
ms.date: 2/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 393b0050-7c7e-49e6-a03d-b1e09fe4de9e
description: Ce document de présentation vous aidera à comprendre Exchange Online Protection (EOP) et quelques termes importants. Ceci s'applique aux clients Office 365 qui protègent les boîtes aux lettres Exchange Online hébergées dans le Cloud et les clients autonomes EOP qui protègent les boîtes aux lettres locales telles qu'Exchange Server 2016.
ms.openlocfilehash: f9c966fd2e4ca4788b6400aba337019c49f56b84
ms.sourcegitcommit: 9403f8f038a9940f1b6299fc7d5c560bb7fbcc41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2019
ms.locfileid: "30310004"
---
## <a name="what-is-exchange-online-protection-eop"></a>Qu'est-ce qu'Exchange Online Protection (EOP)

Exchange Online Protection (EOP) est un service de filtrage du courrier basé sur le Cloud qui permet de protéger votre organisation contre le courrier indésirable et les programmes malveillants. Si vous avez des boîtes aux lettres dans Office 365, elles sont automatiquement protégées par EOP depuis qu'elle fait partie du service. Cela inclut les organisations qui ont des boîtes aux lettres dans Office 365 et sur site, généralement appelé scénario hybride. EOP standalone est également disponible pour les clients qui n'ont pas de boîtes aux lettres dans le Cloud, mais qui souhaitent protéger leurs boîtes aux lettres locales. 

EOP tente de filtrer les courriers indésirables, ce qui permet d'effacer le contenu que les utilisateurs ne veulent pas voir. Normalement, le courrier indésirable est remis dans le dossier courrier inDésirable. Certains utilisateurs aiment s'assurer que le filtrage fait ce qu'ils veulent, afin que le dossier courrier inDésirable soit un moyen facile pour les utilisateurs de s'en assurer.  

> [!TIP]
> Il s'agit d'une bonne chose lorsque le courrier indésirable est placé automatiquement dans le dossier courrier inDésirable. Le service effectue les opérations nécessaires en fonction de l'état des paramètres d'administration par défaut ou personnalisé. En d'autres termes, les utilisateurs ne doivent pas se soucier de voir un grand nombre de courriers indésirables dans le dossier courrier inDésirable. Si les administrateurs préfèrent déplacer tous les courriers indésirables sortants, la mise en quarantaine doit être configurée. Pour plus d'informations, consultez l'article relatif à la [mise en quarantaine des messages électroniques dans Office 365](quarantine-email-messages.md) .

## <a name="important-terms"></a>Conditions importantes

**Entrant:** Messages entrant dans Office 365.

**Trafic sortant:** Messages sortants d'Office 365.

**Internal:** Messages provenant d'une personne au sein de l'organisation à une personne au sein de l'organisation. Cela inclut les clients qui se trouvent dans des scénarios hybrides et une boîte aux lettres peut être locale et l'autre dans le Cloud.

**Faux négatif (FN):** Courrier indésirable et autre courrier indésirable qui est envoyé de manière incorrecte dans la boîte de réception.

**Faux positif (FP):** Messages légitimes identifiés de manière incorrecte comme courrier indésirable et placés dans le dossier courrier inDésirable ou mis en quarantaine.

Courrier inDésirable **, également appelé courrier indésirable:** Cela prend la forme d'une publicité commerciale, de lettres en chaîne, de publipostages politiques, etc. Il s'agit d'un message électronique indiquant que les utilisateurs ne s'inscrivent pas auprès des expéditeurs de courrier indésirable qui tentent de solliciter des produits ou tentent de valider des fraudes.

**Hameçonnage:** Le hameçonnage est un type spécial de courrier indésirable destiné à vous inciter à donner des informations personnelles dans le but de valider le vol d'identité ou la fraude. Ce type de message contient généralement un lien malveillant ou une pièce jointe, mais pas toujours.

**Spoof:** L'usurpation se fait lorsque des expéditeurs de courrier indésirable falsifient l'en-tête FROM de sorte que les messages semblent provenir de quelqu'un ou d'un autre emplacement que la source réelle. Il peut s'agir d'un courrier indésirable, mais généralement couramment utilisé pour les utilisateurs hameçons.

**Emprunt d'identité:** Ce type de courrier indésirable constitue également un moyen de falsifier l'adresse de l'expéditeur, mais elle est réalisée en modifiant une partie du nom ou du domaine afin qu'elle ressemble à la source réelle. Par exemple, Bi11@micr0s0ft.com, où le «l» de Bill était en fait le nombre onze et «o» dans Microsoft a été remplacé par le chiffre zéro.

**En bloc:** Le courrier en nombre est généralement sollicité par les utilisateurs, bien que parfois indirectement lorsque les sociétés vendent des informations à d'autres sociétés. Il est courant que les utilisateurs s'inscrivent intentionnellement pour le courrier en nombre (par exemple, newletters), mais ils l'oublient plus tard et pensent qu'il s'agit de courrier indésirable. Le courrier en nombre devient un courrier indésirable lorsque les expéditeurs de courriers électroniques envoient plus de utilisateurs et que les niveaux de réclamation deviennent trop élevés.
