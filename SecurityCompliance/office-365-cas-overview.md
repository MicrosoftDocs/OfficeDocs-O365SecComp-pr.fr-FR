---
title: Vue d’ensemble de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: "Office 365 Cloud App Security vous donne des informations sur les activités suspectes dans Office 365 pour vous permettre d'analyser les situations susceptibles de poser problème et, si nécessaire, de prendre des mesures pour résoudre les problèmes de sécurité. "
ms.openlocfilehash: 974858a547d9af2db600f9856efbce619a3b38e4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220174"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Vue d’ensemble de la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|Vous êtes là!  <br/> [Étape suivante](get-ready-for-office-365-cas.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Office 365 Cloud App Security est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement entreprise 365 Enterprise, Office 365 Cloud App Security peut être acheté en tant que module complémentaire. (en tant qu'administrateur général, dans le centre d'administration Office 365, sélectionnez **facturation** \> : **ajouter**des abonnements.) Pour plus d'informations, reportez-vous à [la rubrique office &amp; 365 Platform Service Description: Office 365 Security Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) et [acheter ou modifier un composant additionnel pour Office 365 pour les entreprises](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on). 
  
Office 365 Cloud App Security vous donne un aperçu de l'activité suspecte dans Office 365 pour vous permettre d'analyser les situations susceptibles de poser problème et, si nécessaire, de prendre des mesures pour résoudre les problèmes de sécurité. Avec la sécurité des applications Cloud d'Office 365, vous pouvez recevoir des notifications d'alertes déclenchées pour des activités atypiques ou suspectes, voir la façon dont les données de votre organisation dans Office 365 sont consultées et utilisées, suspendre les comptes d'utilisateur présentant une activité suspecte et exiger aux utilisateurs de se reconnecter aux applications Office 365 une fois qu'une alerte a été déclenchée. Lisez cet article pour obtenir une vue d'ensemble des fonctionnalités et fonctionnalités de sécurité de l'application Cloud Office 365.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Comment trouver le portail de sécurité des applications Cloud Office 365

> [!NOTE]
> Pour accéder au portail de sécurité des applications Cloud Office 365, vous devez être un administrateur général d'Office 365, un administrateur de sécurité ou un lecteur de sécurité. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
Vous pouvez accéder au portail de sécurité des applications Cloud Office 365 en accédant à [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) et en vous connectant. 

Vous pouvez également y accéder à partir du centre de &amp; sécurité conformité Office 365. Voici une excellente façon de procéder:
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l'aide de votre compte professionnel ou scolaire pour Office 365. (Vous accédez au centre de sécurité &amp; conformité.)
    
2. Dans le centre &amp; de sécurité conformité, sélectionnez **alertes** \> **gérer les alertes avancées**. <br/>![Choisissez gérer les alertes avancées pour accéder à la sécurité des applications Cloud Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Si la sécurité des applications Cloud Office 365 n'est pas encore activée et que vous êtes un administrateur global, [activez la sécurité de l'application Cloud pour office 365](turn-on-office-365-cas.md).)
    
3. Sélectionnez **accéder à la sécurité des applications Cloud Office 365**. 
    
## <a name="policies"></a>Policies

La sécurité des applications Cloud Office 365 fonctionne avec les stratégies définies pour votre organisation. Avec la sécurité des applications Cloud d'Office 365, votre organisation obtient de nombreuses stratégies de détection d'anomalies prédéfinies et plusieurs modèles pour les stratégies d'activité. Ces stratégies sont conçues pour détecter les anomalies générales, identifier les utilisateurs qui se connectent à partir d'une adresse IP à risque, détecter les activités de ransomware, détecter les activités de l'administrateur à partir d'adresses IP non professionnelles, et bien plus encore.
  
![Dans le portail CAS, choisissez modèles \> de contrôle pour afficher ou créer des modèles de stratégie.](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
pour afficher/utiliser des modèles de stratégie, dans le portail de sécurité des applications Cloud Office 365, accédez à **modèles**de **contrôle** \> . 
  
![Dans le portail CAS O365, sélectionnez contrôle.](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Pour en savoir plus sur les stratégies, consultez les ressources suivantes:
  
- [Stratégies d’activité et alertes pour Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Alertes

Lorsque des stratégies sont définies, les alertes vous avertissent des activités suspectes ou atypiques détectées. Pour afficher les alertes pour votre organisation, sélectionnez **alertes** dans la barre de navigation en haut de l'écran. 
  
![Sur la page alertes, vous pouvez voir les alertes déclenchées et toutes les actions entreprises.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
Comme les alertes sont déclenchées, vous pouvez les consulter pour en savoir plus sur ce qui se passe. Ensuite, si l'activité est toujours suspecte, vous pouvez prendre une mesure. Par exemple, vous pouvez informer un utilisateur d'un problème, suspendre la connexion d'un utilisateur à Office 365 ou demander à un utilisateur de se connecter à Office 365 applications.
  
Pour en savoir plus sur les alertes, consultez les ressources suivantes:
  
- [Stratégies d’activité et alertes pour Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](anomaly-detection-policies-in-ocas.md)
    
- [Examiner et effectuer des actions sur les alertes de sécurité d'application Cloud Office 365](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Journaux d'activité

Affichez des informations sur les activités de l'utilisateur dans votre page journal des activités dans Office 365 Cloud App Security.
  
![Dans le portail CAS d'O365, sélectionnez \> analyser le journal d'activité](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
pour accéder à cette page, dans le portail sécurité des applications Cloud Office 365, accédez à la page **examiner** \> le **journal d'activité**. 
  
![Dans le portail CAS d'O365, sélectionnez enquête.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Vous pouvez également utiliser les journaux de votre trafic Web avec la sécurité des applications Cloud d'Office 365. Plus le nombre de détails inclus dans ces fichiers journaux est important, plus l'activité de l'utilisateur est meilleure. Vous pouvez utiliser des fichiers journaux à partir de Barracuda, des couches bleues, des points de contrôle, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, et bien plus encore.
  
[En savoir plus sur les journaux de trafic Web et les sources de données pour Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a>Applications OAuth

Avec la sécurité des applications Cloud Office 365, vous pouvez autoriser ou empêcher des personnes de votre organisation d'utiliser des applications tierces qui accèdent à des données dans Office 365.
  
![Dans les autorités de certification O365, vous pouvez accéder à la page gérer les applications OAuth à partir du menu examiner.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Pour accéder à cette page, consultez la page **examiner** \> les **applications OAuth**. 
  
![Dans le portail CAS d'O365, sélectionnez enquête.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Tableau de bord de découverte du Cloud

Le **tableau de bord de découverte du Cloud**, également appelé **découverte d'application de productivité**, affiche des informations sur l'utilisation des applications Cloud au sein de votre organisation. Ce tableau de bord vous permet d'afficher des informations sur les applications, les utilisateurs, le trafic, les transactions et plus encore. Le tableau de bord de découverte du Cloud ressemble à l'image suivante: 
  
![Dans le portail Office 365 CAS, sélectionnez découvrir \> le tableau de bord de découverte Cloud](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
pour accéder à ce tableau de bord, dans le portail de sécurité des applications cloud Office 365, accédez à l'offre **Discover** \> **cloud discovery dashboard**. 
  
![Dans le portail Office 365 CAS, sélectionnez découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Étapes suivantes

- Obtenir les [exemples d'utilisation et le Guide d'utilisation de la sécurité des applications Cloud d'Office 365](https://aka.ms/O365CASGuide)
    
- [Se préparer pour la sécurité des applications cloud Office 365](get-ready-for-office-365-cas.md)
    

