---
title: Combinaison des stratégies et des protections lorsque le courrier est marqué par un indicateur rouge
description: Les stratégies appliquées et les actions à effectuer, quand le courrier électronique est marqué comme programme malveillant, courrier indésirable, courrier indésirable à confiance élevée, hameçonnage et en bloc par EOP et/ou ATP.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, ATP, Windows Defender ATP, Office 365 ATP, Azure ATP
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 03/26/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.openlocfilehash: 73f44e747581664f075608d972ee80c8381ca7fd
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30994844"
---
# <a name="what-policy-applies-when-multiple-protection-methods-and-detection-scans-run-on-your-email"></a>Quelle stratégie s'applique lorsque plusieurs méthodes de protection et analyses de détection s'exécutent sur votre courrier électronique

Éventuellement, votre courrier entrant peut être marqué par plusieurs formes de protection (par exemple, EOP *et* ATP) et plusieurs analyses de détection (comme le courrier indésirable *et* le hameçonnage). Cela est possible, car il existe des stratégies anti-hameçonnage ATP pour les clients ATP et des stratégies anti-hameçonnage EOP pour les clients EOP. Cela signifie également que le message peut parcourir plusieurs analyses de détection pour les programmes malveillants, le hameçonnage et l'emprunt d'identité de l'utilisateur, par exemple. Étant donné toutes ces activités, il peut y avoir une certaine confusion quant à la stratégie qui s'applique.

En règle générale, une stratégie appliquée à un message est identifiée dans l'en-tête **X-Forefront-antispam-Report** de la propriété **Cat (Category)** . Si vous avez plusieurs stratégies de détection d'hameçonnage, la priorité la plus élevée s'applique.

Les stratégies ci-dessous s'appliquent à _toutes les organisations_.

|Priorité |Stratégie  |Catégorie  |Où maNaged |
|---------|---------|---------|---------|
|0,1     | Programme malveillant      | MALW      | Stratégie anti-programme malveillant   |
|n°2     | Hameçonnage     | PHSH     | Configuration de vos stratégies de filtrage du courrier indésirable     |
|3     | Courrier fortement suspecté d’être indésirable      | HSPM        | Configuration de vos stratégies de filtrage du courrier indésirable        |
|4     | Usurpation        | SPOOF        | Stratégie anti-hameçonnage, aide à l'usurpation d'identité        |
|disque     | Courrier indésirable         | SPM         | Configuration de vos stratégies de filtrage du courrier indésirable         |
|6.x     | Courrier en nombre         | BULK        | Configuration de vos stratégies de filtrage du courrier indésirable         |

En outre, ces stratégies s'appliquent aux _organisations avec ATP_.

|Priorité |Stratégie  |Catégorie  |Où maNaged |
|---------|---------|---------|---------|
|7j/7     | Emprunt d’identité de domaine         | DIMP         | Configuration de l’anti-hameçonnage d’Office 365 – Protection avancée contre les menaces et des stratégies anti-hameçonnage        |
|8bits     | Emprunt d’identité d’utilisateur        | UIMP         | Configuration de l’anti-hameçonnage d’Office 365 – Protection avancée contre les menaces et des stratégies anti-hameçonnage         |

Par exemple, si vous avez deux stratégies avec leurs priorités respectives:

|Stratégie  |Priorité  |Emprunt d’identité d’utilisateur/de domaine  |Détection d’usurpation d’identité  |
|---------|---------|---------|---------|
|A     | 0,1        | Activé        |Désactivé         |
|B     | n°2        | Désactivé        | Activé        |

Si un message est identifié à la fois comme _emprunt d'identité d'utilisateur_ et _usurpation_ (reportez-vous à la rubrique anti-usurpationing dans le tableau ci-dessus), et que le même ensemble d'utilisateurs étendu à la stratégie a est inclus dans la stratégie B, le message est marqué et traité comme une _usurpation_. Toutefois, aucune action n'est appliquée, car si l'usurpation d'identité a une priorité plus élevée (4) que l'emprunt d'identité d'utilisateur (8), la détection d'usurpation d'identité est désactivée.

N'oubliez pas que les administrateurs peuvent créer une liste de stratégies classées par ordre de priorité (voir le champ priorité ci-dessus), mais une seule stratégie s'exécutera et appliquera ses actions. Cela signifie qu'un utilisateur de la stratégie A et B disposera de la stratégie de priorité supérieure (a est #1), et le message ne sera pas filtré via les autres stratégies. Si l'anti-spoofiing est désactivé, aucune action n'est exécutée.

Étant donné qu'il est possible d'avoir plusieurs groupes d'utilisateurs dans de nombreuses stratégies, les administrateurs peuvent behoove envisager d'utiliser moins de stratégies avec davantage de fonctionnalités. Il est également important de s'assurer que tous les utilisateurs sont couverts par une stratégie complète.

Pour appliquer d'autres types de stratégies de hameçonnage, vous devrez ajuster les paramètres auxquels les différentes stratégies s'appliquent.



