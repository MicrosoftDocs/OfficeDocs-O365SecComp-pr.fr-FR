---
title: Fonctionnement du DLP entre le Centre de sécurité et conformité et le Centre d’administration Exchange
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/19/2019
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans le centre de sécurité & conformité fonctionne avec DLP et les règles de flux de messagerie (règles de transport) dans le centre d’administration Exchange.
ms.openlocfilehash: 65df871361eca66dca543cd2a6dcb0a529446169
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230618"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a>Fonctionnement du DLP entre le Centre de sécurité et conformité et le Centre d’administration Exchange

Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d’administration différents:
  
- Dans le **Centre de sécurité & conformité**, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive, Exchange et Microsoft Teams. Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici. Pour plus d’informations, reportez-vous [à la rubrique DLP dans le centre de sécurité & conformité](data-loss-prevention-policies.md).
    
- Dans le **Centre d’administration Exchange**, vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange. Cette stratégie peut utiliser des règles de flux de messagerie Exchange (également appelées règles de transport), de sorte qu’elle dispose de plus d’options spécifiques pour gérer le courrier électronique. Pour plus d’informations, consultez [la rubrique DLP dans le centre d’administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).
    
Les stratégies DLP créées dans ces centres d’administration fonctionnent côte à côte-cette rubrique explique comment procéder.
  
![Pages DLP dans le centre de sécurité et de conformité et centre d’administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a>Fonctionnement de DLP dans le centre de sécurité & conformité avec DLP et les règles de flux de messagerie dans le centre d’administration Exchange

Une fois que vous avez créé une stratégie DLP dans le centre de sécurité & conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie. Si la stratégie inclut Exchange Online, la stratégie est synchronisée et appliquée exactement de la même manière qu’une stratégie DLP créée dans le centre d’administration Exchange. 
  
Si vous avez créé des stratégies DLP dans le centre d’administration Exchange, ces stratégies continueront à fonctionner côte à côte avec des stratégies pour les messages électroniques que vous créez dans le centre de sécurité & Compliance Center. Toutefois, Notez que les règles créées dans le centre d’administration Exchange ont priorité. Toutes les règles de flux de messagerie Exchange sont traitées en premier, puis les règles DLP du centre de sécurité & conformité sont traitées.
  
Cela signifie que:
  
- Les messages bloqués par les règles de flux de messagerie Exchange ne sont pas analysés par les règles DLP créées dans le centre de sécurité & conformité.
    
- Si une règle de flux de messagerie Exchange modifie un message de manière à ce qu’il corresponde à une stratégie DLP dans le centre de conformité & de sécurité, comme l’ajout d’utilisateurs externes, les règles DLP les détectent et appliquent la stratégie si nécessaire.
    
Notez également que les règles de flux de messagerie Exchange qui utilisent l’action «arrêter le traitement» n’ont pas d’impact sur le traitement des règles DLP dans le centre de sécurité & conformité.
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a>Conseils de stratégie dans le centre de sécurité & conformité et au centre d’administration Exchange

Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d’administration Exchange, soit avec les stratégies DLP créées dans le centre de sécurité & conformité, mais pas dans les deux. Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu’à partir d’un seul emplacement.
  
Si vous avez configuré des conseils de stratégie dans le centre d’administration Exchange, tous les conseils de stratégie que vous configurez dans le centre de sécurité & les utilisateurs ne s’afficheront pas dans Outlook sur le Web et Outlook 2013 et les versions ultérieures jusqu’à ce que vous désactiviez les conseils dans le centre d’administration Exchange. Cela permet de s’assurer que vos règles de flux de messagerie Exchange actuelles continueront de fonctionner jusqu’à ce que vous choisissiez de basculer vers le centre de conformité & sécurité.
  
Notez que si les conseils de stratégie ne peuvent être tracés qu’à partir d’un seul emplacement, les notifications par courrier électronique sont toujours envoyées, même si vous utilisez les stratégies DLP dans le centre de sécurité & conformité et dans le centre d’administration Exchange.
  

