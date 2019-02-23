---
title: Fonctionnement de DLP entre le centre &amp; de sécurité et le centre d'administration Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans le centre &amp; de sécurité conformité fonctionne avec DLP et les règles de transport dans le centre d'administration Exchange.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215644"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>Fonctionnement de DLP entre le centre &amp; de sécurité et le centre d'administration Exchange

Dans Office 365, vous pouvez créer une stratégie de protection contre la perte de données (DLP) dans deux centres d'administration différents:
  
- Dans le **Centre &amp; de sécurité conformité**, vous pouvez créer une stratégie DLP unique pour protéger le contenu dans SharePoint, OneDrive et Exchange. Dans la mesure du possible, nous vous recommandons de créer une stratégie DLP ici. Pour plus d'informations, reportez-vous [à la rubrique DLP dans le centre de sécurité &amp; conformité](data-loss-prevention-policies.md).
    
- Dans le **Centre d'administration Exchange**, vous pouvez créer une stratégie DLP pour protéger le contenu uniquement dans Exchange. Cette stratégie peut utiliser des règles de transport Exchange, de sorte qu'elle dispose de plus d'options spécifiques pour gérer le courrier électronique. Pour plus d'informations, consultez [la rubrique DLP dans le centre d'administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).
    
Les stratégies DLP créées dans ces centres d'administration fonctionnent côte à côte-cette rubrique explique comment procéder.
  
![Pages DLP dans le centre de sécurité et de conformité et centre d'administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>Fonctionnement de DLP dans le &amp; Centre de sécurité conformité avec DLP et les règles de transport dans le centre d'administration Exchange

Une fois que vous avez créé une stratégie DLP &amp; dans le centre de sécurité conformité, la stratégie est déployée sur tous les emplacements inclus dans la stratégie. Si la stratégie inclut Exchange Online, la stratégie est synchronisée et appliquée exactement de la même manière qu'une stratégie DLP créée dans le centre d'administration Exchange. 
  
Si vous avez créé des stratégies DLP dans le centre d'administration Exchange, ces stratégies continueront à fonctionner côte à côte avec n'importe quelle stratégie pour le courrier électronique &amp; que vous créez dans le centre de sécurité et de conformité. Toutefois, Notez que les règles créées dans le centre d'administration Exchange ont priorité. Toutes les règles de transport Exchange sont traitées en premier, puis les règles DLP du &amp; Centre de sécurité conformité sont traitées.
  
Cela signifie que:
  
- Les messages bloqués par les règles de transport Exchange ne sont pas analysés par les règles DLP &amp; créées dans le centre de sécurité conformité.
    
- Si une règle de transport Exchange modifie un message de manière à ce qu'elle corresponde à une stratégie DLP dans le &amp; Centre de sécurité conformité, comme l'ajout d'utilisateurs externes, les règles DLP le détectera et appliqueront la stratégie si nécessaire.
    
Notez également que les règles de transport Exchange qui utilisent l'action «arrêter le traitement» n'affectent pas le traitement des règles &amp; DLP dans le centre de sécurité conformité.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>Conseils de stratégie dans le &amp; Centre de sécurité conformité et dans le centre d'administration Exchange

Les conseils de stratégie peuvent fonctionner soit avec les stratégies DLP et les règles de flux de messagerie créées dans le centre d'administration Exchange, soit &amp; avec les stratégies DLP créées dans le centre de sécurité conformité, mais pas dans les deux. Cela est dû au fait que ces stratégies sont stockées à des emplacements différents, mais que les conseils de stratégie ne peuvent tirer qu'à partir d'un seul emplacement.
  
Si vous avez configuré des conseils de stratégie dans le centre d'administration Exchange, tous les conseils de stratégie que &amp; vous configurez dans le centre de sécurité conformité ne s'afficheront pas aux utilisateurs dans Outlook sur le Web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils dans le centre d'administration Exchange. Cela garantit que vos règles de transport Exchange actuelles continueront de fonctionner jusqu'à ce que vous choisissiez de &amp; basculer vers le centre de sécurité conformité.
  
Notez que si les conseils de stratégie ne peuvent être tracés qu'à partir d'un seul emplacement, les notifications par courrier électronique sont toujours envoyées, &amp; même si vous utilisez des stratégies DLP dans le centre d'administration et Exchange.
  

