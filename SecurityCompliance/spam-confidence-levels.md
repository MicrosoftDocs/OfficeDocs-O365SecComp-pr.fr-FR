---
title: Seuils de probabilité de courrier indésirable
ms.author: krowley
author: kccross
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
description: Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
ms.openlocfilehash: 4b8eea798bc46396e06da2c6ba0573c019d7a9b7
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002903"
---
# <a name="spam-confidence-levels"></a>Seuils de probabilité de courrier indésirable

Un message électronique qui passe à travers le filtrage anti-spam reçoit un score de mise en quarantaine. Ce score est mappé à une valeur de seuil de probabilité de courrier indésirable (SCL) individuelle et marqué dans un en-tête X. Le service entreprend des actions sur les messages en fonction de l'interprétation de la probabilité de courrier indésirable de la valeur SCL. Le tableau suivant indique comment sont interprétées les différentes valeurs SCL par les filtres ainsi que l'action par défaut entreprise sur les messages entrants pour chaque valeur.
  
|**Valeur SCL**|**Interprétation de la probabilité de courrier indésirable**|**Action par défaut**|
|:-----|:-----|:-----|
|-1  <br/> |Courrier non indésirable provenant d'un expéditeur sûr, un destinataire sûr ou une adresse IP inscrite sur une liste sûre (partenaire approuvé)  <br/> |Le message est remis dans la boîte aux lettres des destinataires.  <br/> |
|0, 1  <br/> |Courrier non indésirable car le message a été analysé et identifié comme sûr  <br/> |Le message est remis dans la boîte aux lettres des destinataires.  <br/> |
|5, 6  <br/> | Courrier indésirable  <br/> |Le message est envoyé vers le dossier Courrier indésirable des destinataires.  <br/> |
|7, 8, 9  <br/> |Courrier indésirable à probabilité élevée  <br/> |Le message est envoyé vers le dossier Courrier indésirable des destinataires.  <br/> |
   
> [!TIP]
> Contrôles d’accès SCL de 2, 3, 4, 7 et 8 ne sont pas définies par le service. Un classement de 5 ou 6 est considéré comme du courrier indésirable suspecté, est moins certain comme courrier indésirable à une SCL de 9, qui est considéré comme certain du courrier indésirable. Des actions différentes pour le courrier indésirable et le courrier indésirable de niveau de confiance élevé peuvent être configurées par le biais de vos stratégies de filtrage de contenu dans le centre d’administration Exchange. Pour plus d’informations, voir [configurer vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Vous pouvez également définir la valeur SCL pour les messages qui correspondent aux conditions spécifiques à l’aide de règles de Transport, comme décrit dans les [règles de flux de messagerie utilisés pour définir le niveau de confiance du courrier indésirable (SCL) dans les messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Si vous utilisez une règle de transport pour la valeur SCL de 7, 8, 9 ou de message est considéré comme du courrier indésirable de niveau de confiance élevé. 
  
||
|:-----|
|![Icône rapide pour LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Vous débutez avec Office 365 ?**         Découvrez les cours vidéo gratuits pour **Office 365 admins and IT pros** proposés par LinkedIn Learning. |
   

