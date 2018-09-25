---
title: Prise en main des recommandations en matière de stratégie DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea4459b-cb13-4ce2-b9d1-0619316df88c
description: Cette recommandation pilotée par un aperçu permet à votre organisation de protéger les contenus sensibles lorsqu’il est stocké et partagée dans Office 365 par pour vous informer lorsqu’il est possible la couverture de stratégie DLP. Cette recommandation s’affiche sur la page d’accueil de la sécurité &amp; centre de conformité, si vos documents contiennent les types les plus courants haut-cinq d’informations sensibles, mais ne sont pas protégés par une stratégie DLP.
ms.openlocfilehash: fcd3a5a3a12932b22c310938c12f71fb01019411
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002627"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>Prise en main des recommandations en matière de stratégie DLP

Cette recommandation pilotée par un aperçu permet à votre organisation de protéger les contenus sensibles lorsqu’il est stocké et partagée dans Office 365 par pour vous informer lorsqu’il est possible la couverture de stratégie DLP. Cette recommandation s’affiche sur la page **d’accueil** de la sécurité &amp; centre de conformité, si vos documents contiennent les types les plus courants haut-cinq d’informations sensibles, mais ne sont pas protégées par une stratégie de protection contre la perte données. 
  
Vous pouvez utiliser ce widget pour créer rapidement une stratégie DLP personnalisée dans un simple clic ou les deux, et après avoir créé cette stratégie DLP, il est entièrement personnalisable. Notez que si vous ne voyez pas la recommandation en premier lieu, essayez de cliquer sur **+ plus** en bas de la section **recommandé pour vous** . 
  
![Utilisation du widget nommé des informations sensibles non protégées](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>Créer la stratégie DLP recommandée

Lorsque le widget affiche que vous sans protection des informations sensibles, choisissez **Démarrer** au bas pour créer rapidement une stratégie DLP. 
  
Pour protéger les informations sensibles, cette stratégie DLP :
  
- Détecte lorsque le contenu de Exchange, SharePoint et OneDrive qui contient un des types d’informations sensibles non protégés est partagé avec des personnes extérieures à votre organisation.
    
- Génère des rapports d’activité détaillées afin que vous pouvez suivre des éléments comme ayant le contenu partagé avec des personnes extérieures à votre organisation et lorsque que. Vous pouvez utiliser les [rapports DLP](view-the-dlp-reports.md) et [des données du journal d’audit](search-the-audit-log-in-security-and-compliance.md) (où **activité** = **DLP**) pour afficher ces informations.
    
Vous pouvez également choisir la stratégie DLP :
  
- Vous envoyer un message électronique de rapport d’incident lorsque des utilisateurs partagent un grand nombre de ces informations sensibles avec des personnes extérieures à votre organisation.
    
- Ajouter d’autres utilisateurs pour le rapport d’incident e-mail.
    
- Afficher un Conseil de stratégie et d’envoyer une notification par courrier électronique aux utilisateurs lorsqu’ils essaient de partager ces informations sensibles avec des personnes extérieures à votre organisation. Pour plus d’informations sur ces options, voir [Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md).
    
Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la stratégie DLP après sa création. Par exemple, vous pouvez faire la stratégie de plus restrictif par des personnes même blocage de partage de contenu qui contient des informations sensibles en premier lieu - consultez la section suivante.
  
![Paramètres pour le widget nommé des informations sensibles non protégées](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>Modifier la stratégie DLP recommandée

Une fois que vous utilisez le widget pour créer une stratégie DLP, la stratégie s’affiche sous la **prévention des pertes de données** dans la page **stratégie** de la sécurité &amp; centre de conformité. 
  
Par défaut, la stratégie est nommée **La stratégie système recommandé pour le partage des informations sensibles**. Cette stratégie est entièrement personnalisable, identique à toute stratégie DLP que vous avez créés à partir de zéro. Par exemple, si vous avez décidé ne pas activer les rapports d’incidents et conseils de stratégie lors de l’utilisation du widget, vous pouvez toujours modifier la stratégie d’et activer ces options à tout moment.
  
![Système recommandé de stratégie pour le partage des informations sensibles](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Lorsque le widget et n’apparaît pas

Le widget nommé **Des informations sensibles non protégé** apparaît dans la section **recommandé pour vous** de la page **d’accueil** de la sécurité &amp; centre de conformité. 
  
Ce widget s’affiche uniquement lorsque :
  
- Nouveaux documents contenant l’un des cinq types les plus courants d’informations sensibles détectés dans SharePoint ou OneDrive au cours des 30 derniers jours.
    
- Ces informations sensibles ne sont pas déjà protégées par une stratégie DLP existante.
    
Contrairement aux stratégies DLP qui analysent en permanence vos données, cette recommandation analyse des lacunes dans la couverture de stratégie DLP à peu près toutes les 48 heures, une fois que le nouveau contenu est téléchargé, il peut prendre jusqu'à deux jours de la recommandation apparaisse.
  
Enfin, après avoir utilisé le widget pour créer une stratégie DLP recommandée, le widget disparaît de la page **d’accueil** . 
  

