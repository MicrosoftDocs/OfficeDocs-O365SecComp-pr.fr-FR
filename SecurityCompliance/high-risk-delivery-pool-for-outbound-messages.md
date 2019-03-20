---
title: Pool de remise à risque élevé pour les messages sortants
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
ms.collection:
- M365-security-compliance
description: Lorsque le système de courrier d'un client a été compromis par un programme malveillant ou une attaque de courrier indésirable malveillant, et qu'il envoie du courrier indésirable sortant via le service de filtrage hébergé, les adresses IP des serveurs du centre de données Office 365 sont peut-être référencées dans un bloc tiers. établit.
ms.openlocfilehash: b3c0aecd45dd01d407712af2e3945e1cff521710
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692083"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a>Pool de remise à risque élevé pour les messages sortants

Quand l'intégrité du système de messagerie d'un client a été compromise par un programme malveillant ou une attaque malveillante de courriers indésirables, et que ce système envoie du courrier indésirable via le service de filtrage hébergé, les adresses IP des serveurs du centre de données Office 365 peuvent alors être répertoriées sur des listes rouges tierces. Les serveurs de destination qui utilisent ces listes rouges à la place du service de filtrage hébergé rejettent tous les messages électroniques envoyés à partir des adresses IP de filtrage hébergées qui ont été ajoutées à ces listes. Pour éviter cela, tous les messages sortants qui dépassent le seuil de courrier indésirable sont envoyés via un pool de remise à risque élevé. Ce pool de messages électroniques sortants secondaire est utilisé uniquement pour envoyer des messages pouvant être de qualité médiocre, ce qui permet ainsi de protéger le reste du réseau contre l'envoi de messages plus susceptibles d'entraîner le blocage de l'adresse IP d'expédition.
  
L'utilisation d'un pool de remise à risque élevé dédié permet de garantir que le pool sortant normal n'envoie que des messages réputés de bonne qualité. Ce pool d'adresses IP secondaire permet de réduire la probabilité que le pool d'adresses IP sortantes normal soit ajouté à une liste rouge. La possibilité qu'un pool de remise à risque élevé soit placé sur une liste rouge est toujours présente. Il s'agit du comportement par défaut.
  
Les messages pour lesquels le domaine d'envoi n'a ni enregistrement d'adresse (enregistrement A), qui vous permet de récupérer l'adresse IP du domaine, ni enregistrement MX, qui permet de diriger le message électronique vers les serveurs censés recevoir le message pour un domaine particulier dans le DNS, sont toujours acheminés via le pool de remise à risque élevé qu'elle que soit leur inclination à être du courrier indésirable.
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a>Présentation des messages de notification d'état de remise (DSN)

Le pool de remise à risque élevé sortant gère la remise de tous les messages de notification d'état de remise (DSN) « rejetés » ou « en échec ».
  
Voici quelques causes possibles à une augmentation subite du nombre de messages DSN :
  
- Une campagne de falsification affectant l'un des clients qui utilisent le service.
    
- Une attaque DHA (Directory Harvest Attack).
    
- Une attaque par courrier indésirable.
    
- Un serveur SMTP non autorisé.
    
Tous ces problèmes peuvent entraîner une augmentation subite du nombre de messages DSN traités par le service. Souvent, ces messages DSN sont considérés comme des courriers indésirables auprès des autres serveurs de messagerie et services.
  
## <a name="for-more-information"></a>Pour plus d'informations

[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[FAQ sur la protection contre le courrier indésirable](anti-spam-protection-faq.md)
  

