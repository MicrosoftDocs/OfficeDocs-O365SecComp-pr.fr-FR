---
title: Configuration de stratégies de blocage du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies.
ms.openlocfilehash: 992885a394031e133008f28a455383fc2f3f0616
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260802"
---
# <a name="configure-the-anti-spam-policies"></a>Configuration de stratégies de blocage du courrier indésirable

Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies. 
  
Pour plus d'informations sur la configuration de vos stratégies anti-spam, consultez les rubriques suivantes :
  
[Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md)
  
[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Pour les clients autonomes EOP : par défaut, les filtres de contenu Exchange Online Protection envoient les messages indésirables détectés dans le dossier Courrier indésirable respectif de chaque destinataire. Toutefois, pour vous assurer que l'action **déplacer le message vers le dossier** courrier indésirable fonctionnera avec des boîtes aux lettres locales, vous devez configurer deux règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, voir [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  

