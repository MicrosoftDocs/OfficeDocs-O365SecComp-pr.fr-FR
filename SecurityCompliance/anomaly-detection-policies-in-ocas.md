---
title: Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/15/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: "Les stratégies de détection des anomalies dans Office 365 Cloud App Security utilisent des algorithmes intégrés pour vous aider à identifier les problèmes potentiels. Vous devez disposer d'au moins une stratégie de détection d'anomalies, que vous pouvez régler (lorsque vous la créez) à l'aide de filtres. "
ms.openlocfilehash: 5308af139a46dad0793ed7eedacab0aee62dcc6c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220674"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](ocas-conditional-access-app-control.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
À partir de [Microsoft Cloud App Security version 116](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116), Office 365 Cloud App Security inclut plusieurs stratégies de détection d'anomalies prédéfinies («prédéfinies») qui incluent les analyses comportementales (UEBA) et machine learning (ml).
  
![Pour afficher vos stratégies de détection des anomalies, \> sélectionnez contrôler les stratégies.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Ces stratégies de détection des anomalies fournissent des résultats immédiats en fournissant des détections immédiates, ciblant de nombreuses anomalies comportementales entre vos utilisateurs et les machines et appareils connectés à votre réseau. En outre, les nouvelles stratégies exposent davantage de données à partir du moteur de détection de sécurité des applications Cloud pour vous aider à accélérer le processus d'enquête et à contenir des menaces en cours.
  
En tant qu'administrateur général ou administrateur de sécurité Office 365, vous pouvez consulter et, si nécessaire, réviser les stratégies par défaut disponibles avec Office 365 Cloud App Security.
  
 > [!IMPORTANT]
> Il existe une période d'apprentissage initiale de sept (7) jours pendant laquelle les alertes de comportement anormal ne sont pas déclenchées. L'algorithme de détection des anomalies est optimisé pour réduire le nombre d'alertes fausses. 
  
## <a name="before-you-begin"></a>Avant de commencer

Vérifiez que :
  
- Votre organisation dispose de la [sécurité des applications Cloud Office 365](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).
    
- La [journalIsation d'audit](turn-audit-log-search-on-or-off.md) est activée pour votre environnement Office 365. 
    
- Vous êtes un administrateur général ou un administrateur de sécurité pour Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Afficher vos stratégies de détection des anomalies

1. En tant qu'administrateur général ou administrateur de sécurité, accédez au portail de sécurité des[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)applications Cloud () et connectez-vous.<br>Cette opération vous amène à la page stratégies de sécurité des applications Cloud Office 365.
    
2. Dans la liste **type** , choisissez **stratégie de détection**des anomalies.<br>Les stratégies de détection des anomalies par défaut (ou existantes) de votre organisation sont affichées.<br>![Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. Sélectionnez une stratégie pour vérifier ou modifier ses paramètres.
    
4. Choisissez **Update** (Mettre à jour) pour enregistrer vos modifications. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>En savoir plus sur les stratégies de détection des anomalies

Les stratégies de détection des anomalies sont automatiquement activées; Toutefois, la sécurité des applications Cloud Office 365 dispose d'une période d'apprentissage initiale de sept jours pendant laquelle les alertes de détection d'anomalies ne sont pas toutes générées. Après cela, chaque session est comparée à l'activité, lorsque les utilisateurs étaient actifs, des adresses IP, des appareils, etc. détectés au cours du mois précédent et le score de risque de ces activités. Ces détections font partie du moteur de détection heuristique des anomalies qui Profile votre environnement et déclenche des alertes par rapport à une ligne de base qui a été appris sur l'activité de votre organisation. Ces détections utilisent également les algorithmes d'apprentissage automatique conçus pour profiler les utilisateurs et les modèles de connexion afin de réduire les faux positifs.
  
Les anomalies sont détectées en analysant l'activité de l'utilisateur. Le risque est évalué en examinant plus de 30 indicateurs de risque différents, regroupés en plusieurs facteurs de risque, tels que l'adresse IP à risque, les échecs de connexion, l'activité d'administration, les comptes inactifs, l'emplacement, le déplacement impossible, le périphérique et l'agent utilisateur, et le taux d'activité.
  
En fonction des résultats de la stratégie, des alertes de sécurité sont déclenchées. Office 365 Cloud App Security examine chaque session d'un utilisateur dans Office 365, et vous avertit en cas de problème qui diffère de la base de référence de votre organisation ou de l'activité normale d'un utilisateur.
  
Le tableau suivant décrit les stratégies de détection des anomalies par défaut, leur fonction et leur fonctionnement.
  
|**Nom de la stratégie de détection des anomalies**|**Fonctionnement**|
|:-----|:-----|
|Déplacement impossible  <br/> |Identifie deux activités utilisateur (une ou plusieurs sessions) provenant d'emplacements éloignés géographiquement pendant une période de temps inférieure à la durée pendant laquelle l'utilisateur a effectué un déplacement depuis le premier emplacement vers le second, indiquant ainsi qu'un autre l'utilisateur utilise les mêmes informations d'identification. Cette détection exploite un algorithme d'apprentissage automatique qui ignore les «faux positifs» évidents qui contribuent à la condition de voyage impossible, tels que les VPN et les emplacements régulièrement utilisés par d'autres utilisateurs au sein de l'organisation. La détection dispose d'une période d'apprentissage initiale de sept jours pendant laquelle elle apprend le modèle d'activité d'un nouvel utilisateur.  <br/> |
|Activité du pays peu fréquent  <br/> |Prend en compte les emplacements d'activité passés pour déterminer les emplacements nouveaux et peu fréquents. Le moteur de détection des anomalies stocke des informations sur les emplacements précédents utilisés par les utilisateurs au sein de l'organisation. Une alerte est déclenchée lorsqu'une activité se produit à partir d'un emplacement qui n'a pas été récemment visité par l'utilisateur ou par un utilisateur de l'organisation.  <br/> |
|Activité à partir d'adresses IP anonymes  <br/> |Identifie que les utilisateurs étaient actifs à partir d'une adresse IP qui a été identifiée comme une adresse IP de proxy anonyme. Ces proxys sont utilisés par les personnes qui souhaitent masquer l'adresse IP de leur appareil et peuvent être utilisés à des fins malveillantes. Cette détection tire parti d'un algorithme d'apprentissage automatique qui réduit les «faux positifs», tels que les adresses IP mal balisées qui sont largement utilisées par les utilisateurs au sein de l'organisation.  <br/> |
|Activité provenant d'adresses IP suspectes  <br/> |Identifie que les utilisateurs étaient actifs à partir d'une adresse IP qui a été identifiée comme risquée par Microsoft Threat Intelligence. Ces adresses IP sont impliquées dans des activités malveillantes, telles que&amp;le botnet c c, et peuvent indiquer un compte compromis. Cette détection tire parti d'un algorithme d'apprentissage automatique qui réduit les «faux positifs», tels que les adresses IP mal balisées qui sont largement utilisées par les utilisateurs au sein de l'organisation.  <br/> |
|Activités inHabituelles (par utilisateur)  <br/> | Identifie les utilisateurs qui effectuent des activités inhabituelles, telles que:  <br/>  --Téléchargements de plusieurs fichiers  <br/>  --Activités de partage de fichiers  <br/>  --Activités de suppression de fichiers  <br/>  --Activités d'emprunt d'identité  <br/>  --Activités administratives  <br/>  Ces stratégies recherchent des activités au sein d'une seule session par rapport à la ligne de base apprise, qui pourrait indiquer une tentative de violation. Ces détections exploitent un algorithme d'apprentissage automatique qui Profile les utilisateurs se connectent au modèle et réduit les faux positifs. Ces détections font partie du moteur de détection heuristique des anomalies qui Profile votre environnement et déclenche des alertes par rapport à une ligne de base qui a été appris sur l'activité de votre organisation.  <br/> |
|Plusieurs tentatives de connexion ayant échoué  <br/> |Identifie les utilisateurs qui ont échoué plusieurs tentatives de connexion dans une session unique en ce qui concerne la ligne de base appris, ce qui peut indiquer une tentative de violation.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Alertes de détection des anomalies de triage

Au fur et à mesure de l'arrivée des alertes, vous pouvez trier ces alertes rapidement et déterminer celles à traiter en premier. Le contexte d'une alerte vous permet d'afficher l'image la plus grande et de déterminer si un problème malveillant se produit. Utilisez la procédure suivante pour commencer à explorer une alerte:
  
1. En tant qu'administrateur général ou administrateur de sécurité, accédez au portail de sécurité des[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)applications Cloud () et connectez-vous. 
    
2. Sélectionnez **alertes** pour afficher vos alertes. 
    
3. Pour obtenir le contexte d'une alerte, procédez comme suit:
    
4. Choisissez **analyser** \> le **Journal d'activité**.
    
5. Sélectionnez un élément, tel qu'un utilisateur ou une adresse IP. Le tiroir Insights approprié s'ouvre.<br>![Dans le journal d'activité, vous pouvez examiner une adresse IP.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. Dans le tiroir Insights approprié, cliquez sur une commande disponible, telle qu'une icône dans la section **Afficher** un exemple similaire.<br> ![Cliquez sur l'icône d'horloge pour afficher les activités réalisées dans les 48 heures après l'activité sélectionnée.](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. Obtenir des informations sur l'élément sélectionné en continuant à explorer les détails de cet élément.
    
Une alerte sur plusieurs échecs de connexion peut être suspecte et peut indiquer une attaque en force brute potentielle. Toutefois, une telle alerte peut également être une erreur de configuration de l'application, ce qui entraîne un vrai positif. Si vous voyez une alerte plusieurs échecs de connexion avec des activités suspectes supplémentaires, il existe une probabilité plus élevée qu'un compte soit compromis. Par exemple, supposons qu'une alerte à plusieurs échecs de connexion est suivie d'une activité à partir d'une adresse IP et d'une activité de voyage impossibles, les deux indicateurs de compromission. Vous pouvez même voir que le même utilisateur a effectué une activité de téléchargement en masse, ce qui est souvent un indicateur de l'agresseur qui effectue l'exfiltration des données. Il s'agit des choses que vous pouvez explorer dans Office 365 Cloud App Security pour afficher et trier vos alertes, et prendre des mesures lorsque cela est nécessaire.
  
## <a name="next-steps"></a>Étapes suivantes

- [Déployer le contrôle d’accès conditionnel aux applications pour les applications Office 365](ocas-deploy-conditional-access-app-control.md)

- [ReGroupez vos adresses IP pour simplifier la gestion](group-your-ip-addresses-in-ocas.md)

- [Intégration de votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
    

