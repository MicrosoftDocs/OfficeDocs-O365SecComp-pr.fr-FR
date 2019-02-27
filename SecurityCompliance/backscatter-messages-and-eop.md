---
title: Messages de rétrodiffusion et EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: Les messages rétrodiffusion sont les messages de retour automatique envoyés par les serveurs de messagerie, généralement à la suite de courrier indésirable entrant. Le BACKSCATTERER est une liste d'adresses IP qui envoient des messages rétrodiffusion. Il ne s'agit pas d'une liste de spammeurs, et nous n'essayons pas de supprimer nos serveurs du BACKSCATTERER.
ms.openlocfilehash: 73f8631c50bcfb8a023b2b6007b7ccf48038e16e
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275294"
---
# <a name="backscatter-messages-and-eop"></a>Messages de rétrodiffusion et EOP

La rétrodiffusion désigne l'envoi automatisé de messages non remis par des serveurs de messagerie, généralement à la suite de la détection d'un courrier indésirable entrant. Comme Exchange Online Protection (EOP) est un service de filtrage de courriers indésirables, les messages électroniques envoyés à des destinataires inexistants et vers d'autres destinations suspectes sont rejetés par notre service. Dans ce cas, EOP génère un rapport de non-remise (NDR), qu'il renvoie à l'« émetteur ». Étant donné que les expéditeurs de courriers indésirables utilisent souvent une adresse « De » factice ou non valide dans leurs messages, il est possible que l'adresse de l'expéditeur à qui le rapport NDR est envoyé génère un message de rétrodiffusion. Dans ce cas, les serveurs sortants associés au réseau EOP peuvent être répertoriés sur la liste rouge DNS Backscatterer (DNSBL). La liste rouge DNS Backscatterer est une liste d'adresses IP qui envoient des messages de rétrodiffusion. Il ne s'agit pas d'une liste d'expéditeurs de courriers indésirables et nous n'essayons pas de retirer nos serveurs de la liste rouge DNS Backscatterer. 
  
> [!TIP]
> Selon les instructions figurant sur le site web Backscatterer, l'utilisation du mode de rejet pour tous les messages entrants n'est pas une configuration ou une utilisation recommandée de ce service. Il doit plutôt être utilisé en mode sécurisé. Pour plus d'informations sur la mise en œuvre de la configuration de rétrodiffusion appropriée, consultez le site web [Backscatterer.org](http://www.backscatterer.org/?target=usage). 
  
## <a name="for-more-information"></a>Pour plus d'informations

[Liste d'adresses IP Backscatterer.org](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
Voir l'entrée «NDR rétrodiffusion» dans [Options avancées de filtrage du courrier](advanced-spam-filtering-asf-options.md) indésirable
  

