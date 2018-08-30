---
title: Préparez-vous pour la sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Mise en route à l’aide de la sécurité d’application Office 365 dans le nuage
ms.openlocfilehash: 906570c6607c70b63fa9d2059d56b50f7807124a
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229986"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a>Préparez-vous pour la sécurité d’application Office 365 dans le nuage
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |Vous êtes ici !  <br/> [Étape suivante](turn-on-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Lorsque vous préparez à activer et à implémenter la sécurité d’application Office 365 dans le nuage (anciennement appelé gestion de la sécurité avancée) pour votre organisation, il existe quelques éléments à prendre en compte. Utilisez cet article comme un guide pour planifier la sécurité d’application Office 365 dans le nuage.
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a>Étape 1 : Identifier et protéger vos comptes d’administrateur globales et sécurité

Les administrateurs globaux, les administrateurs de sécurité et les lecteurs de sécurité peuvent accéder au portail de sécurité d’application Office 365 dans le nuage pour afficher les stratégies, passez en revue les alertes et utiliser les rapports. Les administrateurs globaux et les administrateurs de sécurité peuvent définir des stratégies et exécuter d’autres actions pour protéger votre organisation. (Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).) Passez en revue les comptes d’utilisateurs de votre organisation qui ont des autorisations élevées par mesure de précaution. 
  
 **[Comptes d’administrateur global Protect Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**. 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a>Étape 2 : Activer l’enregistrement d’audit pour votre organisation

Dans l’ordre Office 365 nuage sécurité des applications fonctionnent correcte, l’enregistrement d’audit doit être activée. Cela est généralement effectuée par un administrateur Exchange Online ou un administrateur global.
  
 **[Recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md)**. 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a>Étape 3 : Accéder au portail Office 365 Cloud Application Security

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Accédez à des **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage** pour accéder au portail Office 365 Cloud Application Security. 
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    Lorsque vous accédez au portail Office 365 Cloud Application Security, la première page que vous voyez est la page de stratégies, qui ressemble à l’image suivante :
    
    ![Lorsque vous accédez au portail Office 365 Cloud Application Security, vous démarrez avec la page de stratégies](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a>Étape 4 : Définir des stratégies et définir des alertes &amp; actions

Les administrateurs globaux et les administrateurs de sécurité définissent des stratégies de sécurité d’application Office 365 dans le nuage. Au cours du processus de définition de stratégies, alertes et des actions sont également définies. Une alerte est une notification basée sur les critères qui s’affiche dans une vue ou est envoyée par courrier électronique. 
  
Il existe deux types d’alertes de sécurité d’application Office 365 dans le nuage : les alertes de détection des anomalies que détectent les activités suspectes et alertes d’activité, qui sont définies pour les activités qui peuvent être atypiques pour votre organisation. Les alertes avertissent les administrateurs globaux et les administrateurs de sécurité lorsqu’il existe une activité dans votre environnement Office 365 est inhabituelle pour votre organisation.
  
Voir les ressources suivantes pour en savoir plus :
  
- [Stratégies d’activité et les alertes de sécurité pour application Cloud Microsoft Office 365](activity-policies-and-alerts.md)
    
- [Stratégies de détection des anomalies dans Office 365 Cloud Application Security](anomaly-detection-policies-in-ocas.md)
    
- [Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a>Étape 5 : En savoir plus sur l’utilisation du cloud de votre organisation

En tant qu’un administrateur global, un administrateur de sécurité ou un lecteur de sécurité, vous pouvez découvrir l’utilisation du cloud de votre organisation par le biais de rapports et un tableau de bord de découverte dans le nuage (également appelée détection d’application de la productivité). Ce tableau de bord présente des informations sur les utilisateurs, les applications, le trafic web et des niveaux de risques.
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir \> tableau de bord de découverte dans le nuage](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
Pour accéder au tableau de bord de détection d’application de la productivité, dans le portail Office 365 Cloud application sécurité, choisissez **découvrir** \> **tableau de bord de découverte dans le nuage**.
  
![Dans le portail Office 365 autorités de certification, cliquez sur découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
Pour remplir des rapports avec les informations que nécessaires, télécharger vos fichiers journaux de pare-feu et des proxys de votre organisation. Pour plus d’informations, voir les ressources suivantes :
  
- [Créer des rapports de détection d’application dans Office 365 Cloud Application Security](create-app-discovery-reports-in-ocas.md)
    
- [Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a>Étape 6 : Gérer les applications à l’aide de votre organisation à access Office 365

En tant qu’un administrateur global ou administrateur de sécurité, vous pouvez gérer les applications, telles que les applications personnalisées ou les applications de tiers, utilisant des personnes dans votre organisation sur leurs appareils avec Office 365. Par exemple, supposons que quelqu'un a téléchargé une application personnalisée à utiliser avec Office 365. Vous pouvez consulter les applications à l’aide de personnes, interdire les applications non fiables ou marquer les applications approuvées à vos besoins de suivi. [Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage](manage-app-permissions-in-ocas.md).
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a>Étape 7 : Utiliser votre serveur SIEM avec Office 365 Cloud application sécurité

Votre organisation utilise un serveur de gestion (SIEM) des informations et des événements de sécurité ? Office 365 Cloud application sécurité peut maintenant intégrer à votre serveur SIEM pour activer la surveillance centralisée des alertes. Intégration avec un service SIEM vous permet de mieux protéger vos applications en nuage lors de la maintenance de votre flux de travail habituelles de sécurité, l’automatisation des procédures de sécurité et corrélation entre en nuage et événements locale. L’agent SIEM s’exécute sur votre serveur extrait les alertes de sécurité d’application Office 365 dans le nuage et transmet les alertes dans votre serveur SIEM. Consultez [l’intégration avec Office 365 Cloud application sécurité SIEM](integrate-your-siem-server-with-office-365-cas.md).
  
## <a name="next-steps"></a>Étapes suivantes

- [Activer la sécurité d’application Office 365 dans le nuage](turn-on-office-365-cas.md)
    
- Essayez notre [Guide de laboratoire de Test](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) pour une expérience pratique qui illustrent les puissantes fonctionnalités de sécurité d’application Office 365 dans le nuage et créer une preuve de concept. 
    

