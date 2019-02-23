---
title: Stratégies d’activité et alertes pour Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Définir des stratégies d'activité avec Office 365 Cloud App Security pour configurer des alertes à déclencher lorsque des activités spécifiques se produisent ou se produisent trop fréquemment. En configurant des stratégies pour déclencher des alertes, vous pouvez être informé et surveiller des activités spécifiques.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219764"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Stratégies d’activité et alertes pour Office 365 Cloud App Security

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](anomaly-detection-policies-in-ocas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Avec la sécurité des applications Cloud d'Office 365, les stratégies de gestion du Cloud avancées déclenchent des alertes pour des activités spécifiques qui se produisent ou se produisent trop fréquemment. Par exemple, supposons qu'un utilisateur tente de se connecter à Office 365 et échoue 70 fois à une minute. Supposons qu'un autre utilisateur télécharge 7 000 fichiers ou qu'il semble être connecté à partir du Canada, lorsque cet utilisateur est censé se trouver dans un autre emplacement. Ou pire, supposons que le compte d'une personne a été compromis, et qu'un agresseur utilise ce compte pour accéder aux applications Cloud et aux données sensibles de votre organisation.
  
Si vous êtes un administrateur [général ou un administrateur de sécurité](permissions-in-the-security-and-compliance-center.md), les alertes d'activité vous avertissent lorsque des événements semblables à ceux-ci se produisent. Vous pouvez ensuite effectuer des actions spécifiques, telles que la suspension d'un compte d'utilisateur jusqu'à ce que vous puissiez examiner ce qui s'est passé.
  
> [!NOTE]
> Les stratégies de sécurité d'application Cloud Office 365 sont différentes des [stratégies d'alerte dans &amp; le centre de sécurité conformité Office 365](alert-policies.md). Les stratégies d'activité décrites dans cet article sont définies dans le portail de sécurité des applications Cloud Office 365 et peuvent vous aider à mieux gérer l'environnement Cloud de votre organisation. 
  
## <a name="before-you-begin"></a>Avant de commencer

Vérifiez que :
  
- Votre organisation dispose de la [sécurité des applications Cloud Office 365](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).
    
- La [journalIsation d'audit](turn-audit-log-search-on-or-off.md) est activée pour votre environnement Office 365. 
    
- Vous êtes un administrateur général ou un administrateur de sécurité pour Office 365.
    
## <a name="create-a-new-activity-policy"></a>Créer une stratégie d'activité

1. En tant qu'administrateur général ou administrateur de sécurité, accédez au portail de sécurité des[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)applications Cloud () et connectez-vous. <br>Cette opération vous amène à la page stratégies de sécurité des applications Cloud Office 365.<br>![Lorsque vous accédez au portail de sécurité des applications Cloud Office 365, vous commencez par la page stratégies.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. Cliquez sur **créer une stratégie**, puis sélectionnez stratégie d' **activité**.<br>![Lorsque vous créez une stratégie dans les autorités de certification O365, vous pouvez choisir entre les stratégies d'activité et les stratégies de détection des anomalies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. Sur la page **créer une stratégie d'activité** , spécifiez le nom et la **Description**de la **stratégie** . Pour baser votre stratégie sur un modèle par défaut, sélectionnez-en un dans la liste **modèle de stratégie** ou créez votre propre stratégie sans utiliser de modèle.<br>![Vous pouvez créer des stratégies d'activité avec Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. Choisissez une **gravité de stratégie** (faible, moyenne ou élevée) qui mesure son sérieux si cette stratégie déclenche une alerte. Cela vous permettra de filtrer les alertes lorsque vous les consulterez plus tard. 
    
5. Choisissez une **catégorie** pour cette stratégie. Cela vous permettra de filtrer et de trier les alertes qui ont été déclenchées, ou de regrouper les stratégies lorsque vous les consultez pour les modifier. 
    
6. Choisissez **filtres d'activité** pour configurer d'autres actions ou mesures qui déclencheront une alerte en fonction de cette stratégie. 
    
7. Sous **paramètres de correspondance des activités**, indiquez si une violation de stratégie est déclenchée lorsqu'une seule activité correspond aux filtres ou si un nombre spécifié d'activités répétées est requis avant l'alerte.<br>Si vous sélectionnez **activité répétée**, spécifiez le nombre d'activités, le délai et le nombre de fois qu'une violation doit être prise en compte pour un utilisateur au sein d'une application spécifique ou pour le même utilisateur avec n'importe quelle application.
    
8. Vous pouvez également sélectionner créer une **alerte** pour créer des alertes supplémentaires pour recevoir des notifications de cette stratégie (par courrier électronique, SMS ou les deux).<br>Assurez-vous **que votre fournisseur de courrier ne bloque pas les courriers électroniques envoyés à partir de `no-reply@cloudappsecurity.com` **. 
  
9. Choisissez les **actions** à effectuer lorsqu'une alerte est déclenchée pour suspendre l'utilisateur ou demander à l'utilisateur de se reconnecter aux applications Office 365. 
    
10. Sélectionnez **créer** pour terminer la création de votre stratégie. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Stratégies de détection des anomalies](anomaly-detection-policies-in-ocas.md)
    
- [Intégration de votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [ReGroupez vos adresses IP pour simplifier la gestion](group-your-ip-addresses-in-ocas.md)
    

