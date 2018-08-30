---
title: Fonctionne de DLP entre la sécurité &amp; centre de conformité et le centre d’administration Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Découvrez comment DLP dans la sécurité &amp; centre de conformité fonctionne avec des règles DLP et de transport dans le centre d’administration Exchange.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528379"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a>Fonctionne de DLP entre la sécurité &amp; centre de conformité et le centre d’administration Exchange

Dans Office 365, vous pouvez créer une stratégie de protection contre la perte données dans deux centres d’administration différentes :
  
- Dans la **sécurité &amp; centre de conformité**, vous pouvez créer une seule stratégie DLP pour vous aider à protéger le contenu dans SharePoint, OneDrive et Exchange. Lorsque cela est possible, nous vous conseillons de créer une stratégie DLP ici. Pour plus d’informations, voir [DLP dans la sécurité &amp; centre de conformité](data-loss-prevention-policies.md).
    
- Dans le **Centre d’administration Exchange**, vous pouvez créer une stratégie DLP pour vous aider à protéger le contenu uniquement dans Exchange. Cette stratégie permet de règles de transport Exchange, il n’a plus d’options spécifiques à la gestion du courrier électronique. Pour plus d’informations, voir [DLP dans le centre d’administration Exchange](https://go.microsoft.com/fwlink/?linkid=852311).
    
Les stratégies DLP créé dans l’administration ces centres de fonctionnent côte à côte - cette rubrique explique comment.
  
![Pages DLP de sécurité et de centre de conformité et de centre d’administration Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a>Comment DLP dans la sécurité &amp; centre de conformité fonctionne avec des règles DLP et de transport dans le centre d’administration Exchange

Après avoir créé une stratégie DLP dans la sécurité &amp; centre de conformité, la stratégie est déployée sur tous les sites inclus dans la stratégie. Si la stratégie inclut Exchange Online, de la stratégie synchronisé il et appliqués dans exactement comme une stratégie DLP créée dans le centre d’administration Exchange. 
  
Si vous avez créé des stratégies DLP dans le centre d’administration Exchange, les stratégies continueront de fonctionner côte à côte avec toutes les stratégies pour le courrier électronique que vous créez dans la sécurité &amp; centre de conformité. Mais, notez que les règles créées dans le centre d’administration Exchange sont prioritaires. Toutes les règles de transport Exchange sont traités en premier, puis le DLP à partir de la sécurité des règles &amp; centre de conformité sont traitées.
  
Cela signifie que :
  
- Messages bloqués par les règles de transport Exchange ne sont analysés par les règles DLP créées dans la sécurité &amp; centre de conformité.
    
- Si une règle de transport Exchange modifie un message d’une manière qui entraîne sa correspondent à une stratégie DLP dans la sécurité &amp; centre de conformité - tels que l’ajout d’utilisateurs externes - puis les règles DLP détecte cela et appliquer la stratégie selon vos besoins.
    
Également note que le traitement de DLP n’affectent pas les règles de transport Exchange qui utilisent l’action « arrêter le traitement » règles de la sécurité &amp; centre de conformité - allez encore être traitées.
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a>Conseils de stratégie de sécurité &amp; centre de conformité et le centre d’administration Exchange

Conseils de stratégie peuvent travailler avec les stratégies DLP et créés dans le centre d’administration Exchange, ou avec des stratégies DLP créées dans la sécurité des règles de flux de messagerie &amp; centre de conformité, mais pas les deux. Il s’agit, car ces stratégies sont stockées dans des emplacements différents, mais les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement.
  
Si vous avez configuré les conseils de stratégie dans le centre d’administration Exchange, les conseils de stratégie que vous configurez dans la sécurité &amp; centre de conformité n’apparaîtra pas aux utilisateurs dans Outlook sur le web et Outlook 2013 et versions ultérieures jusqu'à ce que vous désactiviez les conseils fournis dans le centre d’administration Exchange. Cela garantit que vos règles de transport Exchange en cours continue à fonctionner jusqu'à ce que vous choisissez de basculer vers la sécurité &amp; centre de conformité.
  
Notez que les notifications de messagerie pendant que les conseils de stratégie peuvent tracer uniquement à partir d’un seul emplacement, sont toujours envoyés, même si vous utilisez des stratégies DLP dans la sécurité &amp; centre de conformité et le centre d’administration Exchange.
  

