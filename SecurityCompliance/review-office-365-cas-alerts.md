---
title: Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Utilisez la page alertes dans Office 365 Cloud application sécurité pour afficher les problèmes potentiels et effectuer une action. Vous pouvez faire disparaître ou résoudre les alertes et si nécessaire, suspendre un compte d’utilisateur.
ms.openlocfilehash: 2665f4ebc9c5c24b95da64954a606dfc0df99082
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014826"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a>Passer en revue et effectuer une action sur les alertes dans la sécurité des applications cloud Office 365
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Vous pouvez utiliser la page alertes de sécurité pour application Cloud Microsoft Office 365 pour afficher les problèmes potentiels et, si nécessaire, effectuer une action.
  
> [!NOTE]
> Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer les tâches dans cet article. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-to-get-to-the-alerts-page"></a>Comment accéder à la page alertes

1. En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. 
    
2. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.<br/>![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Dans la barre de navigation dans la partie supérieure de l’écran, cliquez sur **alertes**.<br/>![Dans la page alertes, vous pouvez voir des alertes déclenchées et toutes les actions effectuées.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
## <a name="review-and-handle-alerts"></a>Révision et gérer des alertes

Alertes de vous aider à identifier les activités dans votre environnement en nuage Office 365 que vous pouvez examiner en détail. Vous pouvez également décider de créer de nouvelles stratégies ou modifier des stratégies existantes basées sur les alertes que vous voyez. Par exemple, si vous voyez un administrateur de se connecter à partir d’un emplacement étrange, vous pouvez décider de définir une stratégie qui empêche les administrateurs de se connecter à Office 365 à partir de certains emplacements.
  
> [!TIP]
> Vous pouvez filtrer les alertes par **catégorie** ou par **gravité** afin de gérer les plus importants. 
  
Pour chaque alerte, découvrez ce qui a provoqué son afin de décider quelle action effectuer. Pour plus d’informations sur une alerte et d’effectuer une action, telles que la résolution de l’alerte ou la suspension d’un compte d’utilisateurs, choisissez Ouvrir une page de détails de l’alerte. Dans la page de détails, vous pouvez consulter le journal d’activité, les comptes et les utilisateurs associés à l’alerte et effectuer des actions telles que les suivantes :
  
- **Faire disparaître** Si l’alerte a été un faux positif, fermer. Vous pouvez éventuellement ajouter un commentaire expliquant pourquoi vous avez fait disparaître. 
    
- **Résolution d’alerte** Si l’alerte a été déclenchée par une activité dont vous savez qu’il n’est pas une menace, le résoudre. Vous pouvez éventuellement ajouter un commentaire expliquant pourquoi vous résolu. 
    
- **Suspendre** Si vous pensez que connexion non autorisée ins sur un compte, par exemple, une personne la signature d’un autre pays lorsque vous savez que cette personne est physiquement auprès d’un bureau local, vous pouvez [Suspendre le compte](suspend-or-restore-an-account-in-ocas.md) lorsque vous examinez ce qui se passe. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Rechercher une activité](investigate-an-activity-in-office-365-cas.md)
    
- [Suspendre ou restaurer un compte d’utilisateur](suspend-or-restore-an-account-in-ocas.md)
    
- Afficher la liste des [sources de données et journaux de trafic Web](web-traffic-logs-and-data-sources-for-ocas.md) pris en charge
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

