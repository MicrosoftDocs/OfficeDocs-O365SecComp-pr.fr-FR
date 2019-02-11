---
title: Stratégies d’activité et alertes pour Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Définir des stratégies d’activité avec Office 365 Cloud application sécurité pour définir des alertes se déclenche lorsque des activités spécifiques se produire ou se produire trop souvent. En définissant des stratégies pour déclencher les alertes, vous pourrez être averti et surveiller les activités spécifiques.
ms.openlocfilehash: af364e7ff96f6d18b60d3267c5992d4c5533ea8c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29604091"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a>Stratégies d’activité et alertes pour Office 365 Cloud App Security

Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étape suivante](anomaly-detection-policies-in-ocas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Avec Office 365 Cloud application sécurité, des stratégies de gestion avancée sur le nuage déclenchent des alertes pour des actions spécifiques se produire ou se produire trop souvent. Par exemple, supposons qu’un utilisateur tente de se connecter à Office 365 et échoue 70 heures dans une minute. Supposons qu’un autre utilisateur télécharge 7 000 fichiers ou semble être connecté à partir du Canada, lorsque cet utilisateur est supposé pour être dans un autre emplacement. Ou pire, supposons que le compte d’une personne a été compromis et une personne malveillante utilise ce compte pour accéder aux applications de cloud de votre organisation et les données sensibles.
  
Si vous êtes un [administrateur global ou administrateur de la sécurité](permissions-in-the-security-and-compliance-center.md), activité alertes lorsque les événements tels que ceux-ci se produisent. Vous pouvez ensuite effectuer des actions spécifiques, telles que la suspension d’un compte d’utilisateur jusqu'à ce que vous pouvez vérifier qu’en est-il de.
  
> [!NOTE]
> Stratégies de sécurité des applications dans le nuage Office 365 sont différents de [stratégies de sécurité Office 365 d’alerte &amp; centre de conformité](alert-policies.md). L’activité politiques décrites dans cet article sont définis dans le portail Office 365 Cloud Application Security et peuvent vous aider à mieux gérer l’environnement de votre organisation en nuage. 
  
## <a name="before-you-begin"></a>Avant de commencer

Vérifiez que :
  
- Votre organisation dispose de [Sécurité d’application Office 365 dans le nuage](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).
    
- [L’enregistrement d’audit](turn-audit-log-search-on-or-off.md) est activé pour votre environnement Office 365. 
    
- Vous êtes un administrateur global ou un administrateur de sécurité pour Office 365.
    
## <a name="create-a-new-activity-policy"></a>Créer une nouvelle stratégie d’activité

1. En tant qu’un administrateur global ou administrateur de sécurité, accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter. <br>Vous accédez à la page de stratégies de sécurité des applications Office 365 dans le nuage.<br>![Lorsque vous accédez au portail Office 365 Cloud Application Security, vous démarrez avec la page de stratégies](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
2. Cliquez sur **créer une stratégie**, puis sélectionnez la **stratégie de l’activité**.<br>![Lorsque vous créez une stratégie dans O365 autorités de certification, vous pouvez choisir entre les stratégies de l’activité et de détection des anomalies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
3. Dans la page **créer une stratégie activité** , spécifiez le **nom de la stratégie** et la **Description**. Pour baser votre stratégie sur un modèle par défaut, choisissez dans la liste **modèle de stratégie** , ou créer votre propre stratégie sans utiliser de modèle.<br>![Vous pouvez créer des stratégies de l’activité avec Office 365 Cloud Application Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
4. Choisissez une **gravité stratégie** (faible, moyen ou élevé) qui mesure grave comment il doit vous si cette stratégie déclenche une alerte. Cela vous permettra de filtrer les alertes lorsque vous êtes de les consulter ultérieurement. 
    
5. Choisissez une **catégorie** pour cette stratégie. Cela vous permettra de filtrer et trier les alertes qui ont été déclenchés, ou aux stratégies de groupe, lorsque vous êtes en examinant les apporter des modifications. 
    
6. Choisissez **filtres d’activité** pour configurer d’autres actions ou les mesures qui déclenchent une alerte basée sur cette stratégie. 
    
7. Sous l' **activité correspondent aux paramètres**, spécifiez si une violation de stratégie sera déclenchée lorsqu’une activité unique établit une correspondance avec les filtres, ou si un nombre spécifié d’activités est requise avant les déclencheurs de l’alerte.<br>Si vous sélectionnez **activité répétée**, spécifiez le nombre d’activités, le critère de temps, et si une violation de compte pour un utilisateur au sein d’une application spécifique ou pour le même utilisateur avec n’importe quelle application.
    
8. Si vous le souhaitez, vous pouvez sélectionner **alerte créer** pour créer des alertes supplémentaires pour recevoir des notifications de cette stratégie (via le courrier électronique, message texte ou les deux).<br>**Vous assurer que votre fournisseur de messagerie électronique ne bloque pas les messages électroniques envoyés à partir de `no-reply@cloudappsecurity.com` **. 
  
9. Choisissez les **Actions** à entreprendre lors du déclenche d’une alerte de suspendre l’utilisateur ou de l’utilisateur doit se reconnecter pour que les applications Office 365. 
    
10. Cliquez sur **créer** pour terminer la création de votre stratégie. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Stratégies de détection des anomalies](anomaly-detection-policies-in-ocas.md)
    
- [Intégrer votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Vos adresses IP pour simplifier la gestion de groupe](group-your-ip-addresses-in-ocas.md)
    

