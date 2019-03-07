---
title: Prise en main des recommandations en matière de stratégie DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/7/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
description: Cette recommandation orientée analyse permet à votre organisation de maintenir le contenu sensible sécurisé lorsqu'il est stocké et partagé dans Office 365 en vous informant lorsqu'il existe un manque d'espace dans votre couverture de stratégie DLP. Cette recommandation s'affiche sur la page d'accueil du centre de &amp; sécurité conformité, si vos documents contiennent l'un des cinq types d'informations sensibles les plus courants, mais ne sont pas protégés par une stratégie DLP.
ms.openlocfilehash: aabd1e6b3ce8ea4754192bd7b6f80262d9e83cf7
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455116"
---
# <a name="get-started-with-dlp-policy-recommendations"></a>Prise en main des recommandations en matière de stratégie DLP

Cette recommandation orientée analyse permet à votre organisation de maintenir le contenu sensible sécurisé lorsqu'il est stocké et partagé dans Office 365 en vous informant lorsqu'il existe un manque d'espace dans votre couverture de stratégie DLP. Cette recommandation s'affiche sur la page d' **Accueil** du centre de &amp; sécurité conformité, si vos documents contiennent l'un des cinq types d'informations sensibles les plus courants, mais ne sont pas protégés par une stratégie de protection contre la perte de données (DLP). 
  
Vous pouvez utiliser ce widget pour créer rapidement une stratégie DLP personnalisée en un clic ou deux, et après avoir créé cette stratégie DLP, elle est entièrement personnalisable. Notez que si vous ne voyez pas la recommandation, essayez de cliquer sur **+ autres** en bas de la section **recommandé pour vous** . 
  
![Widget nommé informations sensibles non protégées](media/91bc04d2-6eff-4294-8b73-b2d56d26ffc4.png)
  
## <a name="create-the-recommended-dlp-policy"></a>Créer la stratégie DLP recommandée

Lorsque le widget vous présente des informations sensibles non protégées, choisissez **prise en main** en bas pour créer rapidement une stratégie DLP. 
  
Pour protéger les informations sensibles, cette stratégie DLP:
  
- Détecte quand le contenu dans Exchange, SharePoint et OneDrive qui contient l'un des types d'informations sensibles non protégés est partagé avec des personnes extérieures à votre organisation.
    
- Génère des rapports d'activité détaillés pour vous permettre d'effectuer le suivi des éléments tels que le partage du contenu avec des personnes extérieures à votre organisation et à quel moment. Vous pouvez utiliser les [données du journal d'audit](search-the-audit-log-in-security-and-compliance.md) et des [rapports DLP](view-the-dlp-reports.md) (where **** = **DLP**) pour afficher ces informations.
    
Vous pouvez également choisir d'utiliser la stratégie DLP:
  
- Vous envoyer un rapport d'incident par courrier électronique lorsque les utilisateurs partagent un grand nombre de ces informations sensibles avec des personnes extérieures à votre organisation.
    
- Ajouter d'autres utilisateurs au rapport d'incident de courrier électronique.
    
- Afficher un Conseil de stratégie et envoyer une notification par courrier électronique aux utilisateurs lorsqu'ils essaient de partager ces informations sensibles avec des personnes extérieures à votre organisation. Pour plus d'informations sur ces options, consultez la rubrique [Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md).
    
Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la stratégie DLP après sa création. Par exemple, vous pouvez faire en sorte que la stratégie soit plus restrictive en bloquant même les personnes de partager du contenu qui contient des informations sensibles dans le premier cas, consultez la section suivante.
  
![Paramètres du widget nommé informations sensibles non protégées](media/b6106cbd-1bed-4582-aaef-b678de470c9b.png)
  
## <a name="edit-the-recommended-dlp-policy"></a>Modifier la stratégie DLP recommandée

Une fois que vous avez utilisé le widget pour créer une stratégie DLP, la stratégie apparaît sous **protection contre la perte de données** dans &amp; la page **stratégie** du centre de sécurité et de conformité. 
  
Par défaut, la stratégie est nommée **stratégie système recommandée pour le partage d'informations sensibles**. Cette stratégie est entièrement personnalisable, comme n'importe quelle stratégie DLP que vous créez vous-même de toutes pièces. Par exemple, si vous avez décidé de ne pas activer les rapports d'incident et les conseils de stratégie lorsque vous avez utilisé le widget, vous pouvez toujours modifier la stratégie et activer ces options à tout moment.
  
![Stratégie système recommandée pour le partage d'informations sensibles](media/2fc49f25-ec25-4433-add4-d60f73888f13.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Lorsque le widget n'apparaît pas

Le widget nommé **informations sensibles non protégées** apparaît dans la section **recommandé pour vous** de la page d' **Accueil** du centre de &amp; sécurité et de conformité. 
  
Ce widget apparaît uniquement dans les cas suivants:
  
- Les nouveaux documents contenant l'un des cinq types d'informations sensibles les plus courants sont détectés dans SharePoint ou OneDrive au cours des 30 derniers jours.
    
- Ces informations sensibles ne sont pas déjà protégées par une stratégie DLP existante.
    
Contrairement aux stratégies DLP qui analysent constamment vos données, cette recommandation analyse les lacunes de votre couverture de stratégie DLP environ toutes les 48 heures, de sorte qu'après le chargement du nouveau contenu, il peut falloir jusqu'à deux jours pour que la recommandation s'affiche.
  
Enfin, une fois que vous avez utilisé le widget pour créer une stratégie DLP recommandée, le widget disparaît de la page d' **Accueil** . 
  

