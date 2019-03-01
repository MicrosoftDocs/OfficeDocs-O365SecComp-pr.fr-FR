---
title: Configuration de stratégies de blocage du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 31279431-828d-48bd-b979-20b6de15fa4a
ms.collection:
- M365-security-compliance
description: Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies.
ms.openlocfilehash: 3e972a150b70f1081cb4c3b5e3672a3acba34785
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30340965"
---
# <a name="configure-the-anti-spam-policies"></a>Configuration de stratégies de blocage du courrier indésirable

Le filtrage du courrier indésirable est automatiquement activé à l'échelle de l'entreprise selon les stratégies anti-spam par défaut (filtre de connexion, filtre du courrier indésirable et courrier indésirable sortant). En qualité d'administrateur, vous pouvez afficher et modifier, mais pas supprimer, les stratégies anti-spam par défaut pour les adapter parfaitement aux besoins de votre organisation. Pour une précision accrue, vous pouvez également créer des stratégies de filtrage de contenu personnalisées et les appliquer à des utilisateurs, à des groupes ou à des domaines spécifiés dans votre organisation. Par défaut, les stratégies personnalisées priment sur la stratégie par défaut. Vous pouvez cependant modifier la priorité de vos stratégies. 
  
Pour plus d'informations sur la configuration de vos stratégies anti-spam, consultez les rubriques suivantes :
  
[Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md)
  
[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
> [!IMPORTANT]
> Pour les clients autonomes EOP: par défaut, les filtres de contenu EOP envoient des messages détectés par courrier indésirable dans le dossier de courrier inDésirable de chaque destinataire. Toutefois, pour vous assurer que l'action **déplacer le message vers le dossier** courrier indésirable fonctionnera avec des boîtes aux lettres locales, vous devez configurer deux règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, consultez [la rubrique s'assurer que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  

