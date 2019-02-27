---
title: Quelle est la différence entre courrier indésirable et message électronique en masse ?
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
ms.collection:
- M365-security-compliance
description: Les clients askwhat parfois la différence entre le courrier indésirable et les messages électroniques en masse? L'objectif de cette rubrique est d'expliquer la différence et de fournir des informations sur les différentes options disponibles dans Exchange Online et Exchange Online Protection (EOP).
ms.openlocfilehash: 877912c94af5d4b399769759189d091c62d50075
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275714"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a>Quelle est la différence entre courrier indésirable et message électronique en masse ?

Les clients s'interrogent parfois sur la différence entre le courrier indésirable et les messages électroniques en masse. Cette rubrique a pour but d'expliquer cette différence et de fournir des informations sur les différentes options disponibles dans Exchange Online et Exchange Online Protection (EOP).
  
 **Qu'est-ce que le courrier indésirable ?**
  
Il s'agit de messages électroniques non sollicités (et généralement non désirés) filtrés par le service, aussi appelés « spam ». Par défaut, le service rejettera le message indésirable sur la base de la réputation de l'adresse IP d'expédition. Toutefois, s'il n'est pas détecté lors de l'inspection de l'adresse IP mais qu'il est classé comme indésirable par les filtres de contenu, le message est envoyé vers le dossier Courrier indésirable des destinataires. 
  
> [!NOTE]
> L'action appliquée aux messages dont le contenu est filtré peut être configurée à l'aide de stratégies de filtre de contenu dans le Centre d'administration Exchange (EAC), comme décrit dans la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). En outre, si vous estimez que le courrier indésirable n'est pas classé correctement, vous pouvez signaler les messages que vous considérez indésirables ou non à Microsoft de plusieurs façons, comme décrit dans la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). 
  
 **Que sont les messages électroniques en masse ?**
  
Les messages électroniques en masse, aussi appelés « messages gris » (graymail), sont plus difficiles à classer. Tandis que le courrier indésirable constitue une menace constante, les messages électroniques en masse contiennent généralement une annonce ou un message publicitaire qui ne sera normalement pas envoyé à plusieurs reprises. Certains utilisateurs considèrent les messages électroniques en masse comme indésirables, mais d'autres les sollicitent et se sont d'ailleurs peut-être volontairement inscrits pour les recevoir. Par exemple, certains utilisateurs souhaiteront recevoir des messages publicitaires de la société Contoso ou des invitations à une conférence à venir sur la cybersécurité, tandis que d'autres considèreront ces messages comme indésirables.
  
## <a name="how-to-manage-bulk-email"></a>Gestion des messages électroniques en masse

La gestion des messages électroniques en masse n'est pas facile, car s'ils sont tous sont classés comme indésirables, les utilisateurs qui les sollicitent peuvent se plaindre et les soumettre comme des faux positif, identifiés à tort comme courrier indésirable. À l'inverse, si tous les messages électroniques en masse sont autorisés à passer, les utilisateurs qui ne les ont pas sollicités peuvent se plaindre et les soumettre comme des faux négatifs, arrivés à tort dans leur boîte de réception.
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a>Activer le contrôle de sensibilité des messages électroniques en masse dans la stratégie de filtrage de contenu

En fonction de la stratégie de votre entreprise en matière de messages électroniques en nombre, les administrateurs peuvent sélectionner un seuil pour affecter le courrier en masse. Le paramètre est configurable via stratégies de filtrage de contenu dans le centre d'administration Exchange. Consultez la [configuration de vos stratégies de filtrage du courrier](configure-your-spam-filter-policies.md) indésirable pour les étapes. Vous pouvez choisir un paramètre de seuil de 1-9, où 1 marque la plupart des messages électroniques en masse comme courrier indésirable, et 9 la plupart des messages électroniques en nombre à être remis. Le service effectue ensuite l'action configurée, telle que l'envoi du message au dossier de courrier inDésirable du destinataire. 
  

