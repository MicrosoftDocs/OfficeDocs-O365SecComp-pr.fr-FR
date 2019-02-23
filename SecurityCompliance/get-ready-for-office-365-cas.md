---
title: Se préparer pour la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.date: 02/15/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Prise en main de la sécurité des applications Cloud Office 365
ms.openlocfilehash: d6049bb1a36a078c6e5e33c60928bd3ae872c33f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219894"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Se préparer pour la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |Vous êtes là!  <br/> [Étape suivante](turn-on-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Lors de la préparation de l'activation et de l'implémentation de la sécurité des applications Cloud Office 365 pour votre organisation, il existe quelques éléments à prendre en compte. Utilisez cet article pour planifier la sécurité des applications Cloud Office 365.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>Étape 1: identifier et protéger vos comptes d'administrateur général et de sécurité

Les administrateurs généraux, les administrateurs de la sécurité et les lecteurs de sécurité peuvent accéder au portail de sécurité des applications Cloud Office 365 pour afficher des stratégies, examiner les alertes et utiliser des rapports. Les administrateurs globaux et les administrateurs de sécurité peuvent définir des stratégies et prendre d'autres mesures pour protéger votre organisation. (Pour plus d'informations, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).) Examinez les comptes d'utilisateur de votre organisation qui ont des autorisations élevées par mesure de précaution. 
  
 **[Protégez vos comptes d'administrateur général Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>Étape 2: activation de la journalisation d'audit pour votre organisation

Pour que la sécurité des applications Cloud Office 365 fonctionne correctement, la journalisation d'audit doit être activée. Cette opération est généralement réalisée par un administrateur Exchange Online ou un administrateur général.
  
 **[Activer ou désactiver la recherche dans le journal d'audit Office 365](turn-audit-log-search-on-or-off.md)**. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>Étape 3: accéder au portail de sécurité des applications Cloud Office 365

Vous pouvez accéder au portail de sécurité des applications Cloud Office 365 en accédant à [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) et en vous connectant. 

Vous pouvez également y accéder à partir du centre de &amp; sécurité conformité Office 365. Voici une excellente façon de procéder:

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous. (vous accédez au centre de &amp; sécurité conformité.)
    
2. Accédez à **alertes** \> : **gérer les alertes avancées**.
    
3. Sélectionnez **accéder à la sécurité des applications Cloud office 365** pour accéder au portail de sécurité Office 365 Cloud App.<br> ![Choisissez gérer les alertes avancées pour accéder à la sécurité des applications Cloud Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br>Lorsque vous accédez au portail de sécurité des applications Cloud Office 365, la première page que vous voyez est la page stratégies, qui ressemble à l'image suivante:<br>![Lorsque vous accédez au portail de sécurité des applications Cloud Office 365, vous commencez par la page stratégies.](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)<br>
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>Étape 4: définir des stratégies et configurer des &amp; actions d'alerte

Les administrateurs généraux et les administrateurs de sécurité définissent des stratégies dans Office 365 Cloud App Security. Lors du processus de définition des stratégies, les alertes et les actions sont également définies. Une alerte est une notification basée sur des critères qui apparaît dans un affichage ou qui est envoyée par courrier électronique. 
  
Il existe deux types d'alertes dans Office 365 Cloud App Security: alertes de détection d'anomalies détectant les activités suspectes, ainsi que les alertes d'activité, qui sont définies pour les activités susceptibles d'être atypiques pour votre organisation. Les alertes informent les administrateurs généraux et les administrateurs de la sécurité lorsqu'une activité de votre environnement Office 365 est inhabituelle pour votre organisation.
  
Pour en savoir plus, consultez les ressources suivantes:
  
- [Stratégies d’activité et alertes pour Office 365 Cloud App Security](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](anomaly-detection-policies-in-ocas.md)
    
- [Examiner et effectuer des actions sur les alertes de sécurité d'application Cloud Office 365](review-office-365-cas-alerts.md)
    

## <a name="step-5-set-up-conditional-access-app-control"></a>Étape 5: configurer le contrôle d'application d'accès conditionnel

ConFigurez et appliquez des contrôles aux applications de votre organisation, en fonction de certaines conditions, par exemple les utilisateurs qui peuvent utiliser quelles applications, et où. Définir les stratégies d'accès et de session de l'utilisateur pour déterminer si des documents sensibles peuvent être téléchargés et chiffrés, bloquer l'accès à certaines applications, configurer le mode lecture seule pour certaines applications et restreindre les sessions des utilisateurs de réseaux non professionnels.

Pour en savoir plus, consultez les ressources suivantes:

- [Protéger les applications avec le contrôle d’accès conditionnel aux applications d’Office 365 Cloud App Security](ocas-conditional-access-app-control.md)

- [Déployer le contrôle d’accès conditionnel aux applications pour les applications Office 365](ocas-deploy-conditional-access-app-control.md)

## <a name="step-6-learn-about-your-organizations-cloud-usage"></a>Étape 6: en savoir plus sur l'utilisation du Cloud de votre organisation

En tant qu'administrateur général, administrateur de sécurité ou lecteur de sécurité, vous pouvez en savoir plus sur l'utilisation du Cloud de votre organisation via des rapports et un tableau de bord de découverte dans le Cloud (également appelé découverte d'application de productivité). Ce tableau de bord affiche des informations sur les utilisateurs, les applications, le trafic Web et les niveaux de risque.
  
![Dans le portail Office 365 CAS, sélectionnez découvrir \> le tableau de bord de découverte Cloud](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
pour accéder au tableau de bord de découverte de l'application de productivité, dans le portail de sécurité des applications cloud Office 365, sélectionnez **découvrir** \> le **tableau de bord de découverte cloud**.
  
![Dans le portail Office 365 CAS, sélectionnez découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
Pour remplir des rapports avec les informations dont vous avez besoin, téléchargez vos fichiers journaux à partir des proxys et pare-feu de votre organisation. Pour en savoir plus, consultez les ressources suivantes:
  
- [Créer des rapports de découverte d'application dans Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md)
    
- [Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-7-manage-apps-that-your-organization-is-using-to-access-office-365"></a>Étape 7: gérer les applications que votre organisation utilise pour accéder à Office 365

En tant qu'administrateur général ou administrateur de sécurité, vous pouvez gérer des applications, telles que des applications personnalisées ou des applications tierces, que les personnes de votre organisation utilisent sur leurs appareils avec Office 365. Par exemple, supposons qu'une personne a téléchargé une application personnalisée qu'elle souhaite utiliser avec Office 365. Vous pouvez passer en revue les applications que les utilisateurs utilisent, interdire les applications non approuvées ou marquer les applications comme étant approuvées à des fins de suivi. [Gérer les applications OAuth à l'aide de la sécurité des applications Cloud Office 365](manage-app-permissions-in-ocas.md).
  
## <a name="step-8-create-a-maintenance-plan"></a>Étape 8: créer un plan de maintenance

Une fois que vous avez configuré et configuré Office 365 Cloud App Security, vous pouvez effectuer certaines tâches d'utilisation en tant qu'administrateur général ou administrateur de sécurité Office 365 pour votre organisation. En effectuant ces tâches, vous vous assurerez que la sécurité des applications Cloud d'Office 365 est correctement configurée, que vos stratégies sont à jour, et que votre organisation réalise la valeur à partir d'Office 365. Utilisez cet article pour vous aider à planifier ces tâches. Consultez la rubrique [utilisation des activités après le déploiement de la sécurité des applications Cloud Office 365](utilization-activities-for-ocas.md).

## <a name="optional-step-9-use-your-siem-server-with-office-365-cloud-app-security"></a>Module Étape 9: utiliser votre serveur SIEM avec la sécurité des applications Cloud Office 365

Votre organisation utilise-t-elle un serveur de gestion des événements et des informations de sécurité (SIEM)? Office 365 Cloud App Security peut désormais s'intégrer à votre serveur SIEM pour permettre une surveillance centralisée des alertes. L'intégration à un service SIEM vous permet de mieux protéger vos applications Cloud tout en conservant votre flux de travail de sécurité habituel, en automatisant les procédures de sécurité et en corréler les événements sur site et en nuage. L'agent SIEM s'exécute sur votre serveur, extrait les alertes de la sécurité des applications Cloud Office 365 et diffuse ces alertes sur votre serveur SIEM. Voir [intégration Siem avec Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md).
  
## <a name="next-steps"></a>Étapes suivantes

- [Activer la sécurité des applications cloud Office 365](turn-on-office-365-cas.md)
    
- Essayez notre [Guide de laboratoire de test](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) pour une expérience pratique où vous pouvez présenter les fonctionnalités puissantes d'Office 365 Cloud App Security et créer une preuve de concept. 
    

