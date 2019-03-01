---
title: Seuils de probabilité de courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
ms.openlocfilehash: e7e8e29a7c3d4a3f09d674f72a400d27746e9081
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341245"
---
# <a name="spam-confidence-levels"></a>Seuils de probabilité de courrier indésirable

Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
  
|**Valeur SCL**|**Interprétation de la probabilité de courrier indésirable**|**Action par défaut**|
|:-----|:-----|:-----|
|-1|Non-courrier indésirable provenant d'un expéditeur approuvé, d'un destinataire approuvé ou d'une adresse IP de la zone de sécurité (partenaire approuvé).|Le message est remis dans la boîte aux lettres des destinataires.|
|0, 1|Non-courrier indésirable, car le message a été analysé et déterminé comme étant propre.|Le message est remis dans la boîte aux lettres des destinataires.|
|5, 6|Courrier indésirable|Le message est envoyé vers le dossier Courrier indésirable des destinataires.|
|7, 8, 9|Courrier indésirable à probabilité élevée|Le message est envoyé vers le dossier Courrier indésirable des destinataires.|
   
> [!TIP]
> Les évaluations SCL de 2, 3, 4, 7 et 8 ne sont pas définies par le service. Une valeur SCL de 5 ou 6 est considérée comme suspecte de courrier indésirable, ce qui est moins sûr qu'une valeur SCL de 9, ce qui est considéré comme un courrier indésirable. Des actions différentes pour le courrier indésirable et le courrier indésirable à niveau de confiance peuvent être configurées via vos stratégies de filtrage de contenu dans le centre d'administration Exchange. Pour plus d'informations, consultez [la rubrique Configuration de vos stratégies de filtrage du courrier](configure-your-spam-filter-policies.md)indésirable. Vous pouvez également définir la valeur de contrôle d'accès SCL pour les messages qui correspondent à des conditions spécifiques à l'aide de règles de flux de messagerie (également appelées règles de transport), comme décrit dans [utiliser des règles de flux de messagerie pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Si vous utilisez une règle de flux de messagerie pour définir la valeur SCL de 7, 8 ou 9, le message sera traité comme du courrier indésirable à niveau de confiance élevé. 
  
||
|:-----|
|![Icône rapide pour LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Vous débutez avec Office 365 ?**         Découvrez les cours vidéo gratuits pour **Office 365 admins and IT pros** proposés par LinkedIn Learning.|
   

