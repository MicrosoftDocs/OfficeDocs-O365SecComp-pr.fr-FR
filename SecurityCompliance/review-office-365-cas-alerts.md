---
title: Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Utilisez la page des alertes dans Office 365 Cloud App Security pour afficher les problèmes potentiels et prendre des mesures. Vous pouvez ignorer ou résoudre les alertes et, si nécessaire, suspendre un compte d'utilisateur.
ms.openlocfilehash: 6c2f9788cb238e86abc347a3a118eb08fa84e971
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213164"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Vous pouvez utiliser la page des alertes dans Office 365 Cloud App Security pour afficher les problèmes potentiels et, si nécessaire, prendre des mesures.
  
> [!NOTE]
> Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-to-get-to-the-alerts-page"></a>Comment accéder à la page des alertes?

1. Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.
  
2. Dans la barre de navigation en haut de l'écran, sélectionnez **alertes**.<br/>![Sur la page alertes, vous pouvez voir les alertes déclenchées et toutes les actions entreprises.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a>Examiner et gérer les alertes

Les alertes vous aident à identifier les activités dans votre environnement Cloud Office 365 que vous souhaiterez peut-être approfondir. Vous pouvez également décider de créer de nouvelles stratégies ou de modifier des stratégies existantes en fonction des alertes que vous voyez. Par exemple, si vous voyez un administrateur qui se connecte à partir d'un emplacement étrange, vous pouvez décider de configurer une stratégie qui empêche les administrateurs de se connecter à Office 365 à partir de certains emplacements.
  
> [!TIP]
> Vous pouvez filtrer les alertes par **catégorie** ou par **gravité** afin de gérer les plus importantes en premier. 
  
Pour chaque alerte, examinez ce qui a provoqué cette action afin de décider de l'action à effectuer. Pour afficher plus de détails sur une alerte et agir comme la résolution de l'alerte ou la suspension d'un compte d'utilisateur, choisissez l'alerte pour ouvrir une page de détails. Sur la page détails, vous pouvez consulter le journal d'activité, les comptes et les utilisateurs qui sont associés à l'alerte, et effectuer des actions telles que les suivantes:
  
- **Faire disparaître** Si l'alerte était un faux positif, faites-la disparaître. Vous pouvez éventuellement ajouter un commentaire expliquant la raison pour laquelle vous l'avez rejetée. 
    
- **Résoudre l'alerte** Si l'alerte a été déclenchée par une activité qui n'est pas une menace, résolvez-la. Vous pouvez éventuellement ajouter un commentaire expliquant la raison pour laquelle vous l'avez résolue. 
    
- **Suspendre** Si vous suspectez des signes non autorisés sur un compte, par exemple, une personne se connectant à partir d'un autre pays lorsque vous avez la certitude qu'il s'agit physiquement d'un bureau local, vous pouvez [suspendre le compte](suspend-or-restore-an-account-in-ocas.md) pendant que vous examinez ce qui se passe. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Examiner une activité](investigate-an-activity-in-office-365-cas.md)
    
- [Suspendre ou restaurer un compte d'utilisateur](suspend-or-restore-an-account-in-ocas.md)
    
- Afficher la liste des [journaux de trafic Web et des sources de données](web-traffic-logs-and-data-sources-for-ocas.md) pris en charge
    
- Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

