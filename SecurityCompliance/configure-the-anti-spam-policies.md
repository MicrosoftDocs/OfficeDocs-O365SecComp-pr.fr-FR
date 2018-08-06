---
title: Configuration de stratégies de blocage du courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
description: Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies.
ms.openlocfilehash: b96620705b0a62b8e8f7804f518651a10e0a63c1
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026251"
---
# <a name="configure-the-anti-spam-policies"></a>Configuration de stratégies de blocage du courrier indésirable

Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies. 
  
Pour plus d'informations sur la configuration de vos stratégies anti-spam, consultez les rubriques suivantes :
  
[Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md)
  
[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Pour les clients autonomes EOP : par défaut, les filtres de contenu Exchange Online Protection envoient les messages indésirables détectés dans le dossier Courrier indésirable respectif de chaque destinataire. Cependant, pour que l'action **Déplacer le message vers le dossier Courrier indésirable** fonctionne avec des boîtes aux lettres locales, vous devez configurer deux règles de transport Exchange sur vos serveurs locaux, de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, voir [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  

