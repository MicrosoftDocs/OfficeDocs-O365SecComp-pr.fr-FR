---
title: Messages de rétrodiffusion et EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: La rétrodiffusion désigne l’envoi automatisé de messages non remis par des serveurs de messagerie, généralement à la suite de la détection d’un courrier indésirable entrant. La liste rouge DNS Backscatterer est une liste d'adresses IP qui envoient des messages de rétrodiffusion. Il ne s'agit pas d'une liste d'expéditeurs de courriers indésirables et nous n'essayons pas de retirer nos serveurs de la liste rouge DNS Backscatterer.
ms.openlocfilehash: 11e8909e5cb72eb4e46b392d13f0f11483555aeb
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155606"
---
# <a name="backscatter-messages-and-eop"></a>Messages de rétrodiffusion et EOP

La rétrodiffusion désigne l'envoi automatisé de messages non remis par des serveurs de messagerie, généralement à la suite de la détection d'un courrier indésirable entrant. Comme Exchange Online Protection (EOP) est un service de filtrage de courriers indésirables, les messages électroniques envoyés à des destinataires inexistants et vers d'autres destinations suspectes sont rejetés par notre service. Dans ce cas, EOP génère un rapport de non-remise (NDR), qu'il renvoie à l'« émetteur ». Étant donné que les expéditeurs de courriers indésirables utilisent souvent une adresse « De » factice ou non valide dans leurs messages, il est possible que l'adresse de l'expéditeur à qui le rapport NDR est envoyé génère un message de rétrodiffusion. Dans ce cas, les serveurs sortants associés au réseau EOP peuvent être répertoriés sur la liste rouge DNS Backscatterer (DNSBL). La liste rouge DNS Backscatterer est une liste d'adresses IP qui envoient des messages de rétrodiffusion. Il ne s'agit pas d'une liste d'expéditeurs de courriers indésirables et nous n'essayons pas de retirer nos serveurs de la liste rouge DNS Backscatterer. 
  
> [!TIP]
> Selon les instructions figurant sur le site web Backscatterer, l'utilisation du mode de rejet pour tous les messages entrants n'est pas une configuration ou une utilisation recommandée de ce service. Il doit plutôt être utilisé en mode sécurisé. Pour plus d'informations sur la mise en œuvre de la configuration de rétrodiffusion appropriée, consultez le site web [Backscatterer.org](http://www.backscatterer.org/?target=usage). 
  
## <a name="related-topics"></a>Sujets associés
  
[Options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md)
  

