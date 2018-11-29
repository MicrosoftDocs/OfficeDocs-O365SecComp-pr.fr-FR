---
title: Vue d’ensemble de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Sécurité d’application Office 365 Cloud vous donne des informations sur les activités suspectes dans Office 365 afin que vous pouvez examiner les situations qui sont susceptibles de poser problème et, si nécessaire, prennent des mesures pour résoudre les problèmes de sécurité. '
ms.openlocfilehash: 722c305288798b38ac125a693d9d150446458324
ms.sourcegitcommit: cd452513d8761b2e50b4f9b6cf29422d146307ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26864555"
---
# <a name="overview-of-office-365-cloud-app-security"></a>Vue d’ensemble de la sécurité des applications cloud Office 365
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|Vous êtes ici !  <br/> [Étape suivante](get-ready-for-office-365-cas.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> Sécurité d’application Office 365 dans le nuage est disponible dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, Office 365 Cloud application sécurité peut être achetée comme module complémentaire. (En tant qu’administrateur global, dans le centre d’administration Office 365, choisissez **facturation** \> **abonnements Add**.) Pour plus d’informations, voir [Office 365 Platform Service Description : Office 365 sécurité &amp; centre de conformité](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un module complémentaire pour Office 365 pour entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
Sécurité d’application Office 365 dans le nuage donne un aperçu des activités suspectes dans Office 365 afin que vous pouvez examiner les situations qui sont susceptibles de poser problème et, si nécessaire, prennent des mesures pour résoudre les problèmes de sécurité. Avec Office 365 de sécurité App dans le nuage, vous pouvez recevoir des notifications d’alertes déclenchées pour les activités suspectes ou atypiques, voir comment les données de votre organisation dans Office 365 sont accessible et utilisées, suspendre des comptes d’utilisateur présentant une activité suspecte et nécessitent utilisateurs à se reconnecter pour les applications Office 365 après le déclenchement d’une alerte. Lisez cet article pour obtenir une vue d’ensemble des fonctionnalités de sécurité d’application Office 365 dans le nuage et des capacités.
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a>Comment trouver le portail Office 365 Cloud Application Security

> [!NOTE]
> Pour accéder au portail Office 365 Cloud application sécurité, vous devez être un administrateur global, un administrateur de sécurité ou un lecteur de sécurité. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
Vous pouvez obtenir au portail Office 365 Cloud application sécurité par le biais de la sécurité de 365 Office &amp; centre de conformité. Voici un excellent moyen de le faire :
  
1. Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**. <br/>![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>(Si Office 365 Cloud application sécurité n’est pas encore activée, et vous êtes un administrateur global, [Activer la sécurité d’application Office 365 dans le nuage](turn-on-office-365-cas.md).)
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**. 
    
## <a name="policies"></a>Policies

Office 365 Cloud application sécurité fonctionne avec les stratégies définies pour votre organisation. Avec Office 365 de sécurité application Cloud, votre organisation obtient plusieurs stratégies de détection d’anomalie prédéfinis et plusieurs modèles de stratégies de l’activité. Ces stratégies sont conçues pour détecter les anomalies générales, identifier les utilisateurs de se connecter à partir d’une adresse IP risquée, détecter des activités de logiciels, détecter des activités administrateur de non entreprise des adresses IP et bien plus encore.
  
![Dans le portail d’autorités de certification, choisissez contrôle \> modèles permet d’afficher ou de créer des modèles de stratégie](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
Pour afficher / l’utilisation des modèles de stratégie, dans le portail Office 365 Cloud Application Security, accédez au **contrôle** \> **modèles**. 
  
![Dans le portail O365 autorités de certification, choisissez contrôle](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
Pour plus d’informations sur les stratégies, voir les ressources suivantes :
  
- [Stratégies d’activité et alertes pour Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a>Alertes

Lorsque les stratégies sont définies, les alertes vous informent sur les activités suspectes ou atypiques qui ont été détectées. Pour afficher les alertes pour votre organisation, choisissez **alertes** dans la barre de navigation dans la partie supérieure de l’écran. 
  
![Dans la page alertes, vous pouvez voir des alertes déclenchées et toutes les actions effectuées.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
Comme les alertes sont déclenchées vous pouvez les consulter pour en savoir plus sur ce qui se passe. Puis, si l’activité est toujours suspecte, vous pouvez effectuer une action. Par exemple, vous pouvez signaler un utilisateur sur un problème, suspendre un utilisateur de se connecter à Office 365 ou demander à un utilisateur pour vous reconnecter aux applications Office 365.
  
Pour plus d’informations sur les alertes, voir les ressources suivantes :
  
- [Stratégies d’activité et alertes pour Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](anomaly-detection-policies-in-ocas.md)
    
- [Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a>Journaux d’activité

Afficher des informations sur les activités de l’utilisateur dans la page de journal de l’activité dans Office 365 Cloud Application Security.
  
![Dans le portail O365 autorités de certification, cliquez sur examiner \> le journal d’activité](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
Pour accéder à cette page, dans le portail Office 365 Cloud application sécurité, accédez à **examiner** \> **le journal d’activité**. 
  
![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
Vous pouvez utiliser les journaux du trafic web avec Office 365 de sécurité application Cloud, trop. Plus de détails qui sont inclus dans ces journaux, la meilleure visibilité vous avez en activité de l’utilisateur. Vous pouvez utiliser les fichiers de journal de Barracuda, bleu revêtement, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, encornets, Websence, Zscaler et plus.
  
[En savoir plus sur les sources de données et les journaux du trafic web Office 365 nuage sécurité des applications](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="app-permissions"></a>Autorisations d’application

Avec Office 365 de sécurité App dans le nuage, vous pouvez autoriser ou empêcher les utilisateurs de votre organisation d’utiliser des applications de tiers qui accèdent aux données dans Office 365.
  
![Dans O365 autorités de certification, vous pouvez accéder la page Gérer les autorisations d’application dans le menu examiner.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
Pour accéder à cette page, accédez à **examiner** \> **autorisations d’application**. 
  
![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[Gérer les autorisations des applications à l’aide de la sécurité des applications cloud Office 365](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a>Tableau de bord de découverte dans le nuage

Le **Tableau de bord de découverte dans le nuage**, également appelé **Détection d’application de la productivité**, présente des informations sur l’utilisation des applications dans le nuage au sein de votre organisation. Vous pouvez afficher des informations sur les applications, les utilisateurs, le trafic, les transactions et plus d’informations à l’aide de ce tableau de bord. Le tableau de bord de découverte dans le nuage ressemble à l’image suivante : 
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir \> tableau de bord de découverte dans le nuage](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Pour accéder à ce tableau de bord, dans le portail Office 365 Cloud application sécurité, accédez à **découvrir** \> **tableau de bord de découverte dans le nuage**. 
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a>Étapes suivantes

- Obtenir des [exemples d’utilisation de sécurité Office 365 Cloud application et le Guide d’utilisation](https://aka.ms/O365CASGuide)
    
- [Se préparer pour Office 365 Cloud App Security](get-ready-for-office-365-cas.md)
    

