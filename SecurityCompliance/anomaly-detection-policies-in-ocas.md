---
title: Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 88935b4e-dcb1-47f1-8aca-1bf8fb069db6
description: 'Stratégies de détection des anomalies dans Office 365 Cloud application sécurité utilisent algorithmes intégrés pour découvrir des problèmes potentiels. Vous devez disposer de stratégie de détection au moins une anomalie, vous pouvez régler (lors de sa création) à l’aide de filtres. '
ms.openlocfilehash: 7a1cb795531df168f0a5c425e7555ae6b1412d2b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29604415"
---
# <a name="anomaly-detection-policies-in-office-365-cloud-app-security"></a>Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365

Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étape suivante](integrate-your-siem-server-with-office-365-cas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
Commençant par [Microsoft Cloud Application Security version 116](new-in-office-365-cas-2018.md#office-365-cloud-app-security-release-116-3), Office 365 Cloud Application Security inclut plusieurs anomalies prédéfinis des stratégies de détection (« l’emploi ») qui incluent des utilisateurs analytique comportement entité (UEBA) et apprentissage (ML) de l’ordinateur.
  
![Pour afficher vos stratégies de détection des anomalies, choisissez contrôle \> stratégies.](media/9663baa5-98bf-45e0-9458-6e572b43ec72.png)
  
Ces stratégies de détection des anomalies fournissent des résultats de l’exécution en fournissant des détections immédiates, ciblage de nombreuses anomalies de comportement entre vos utilisateurs et les ordinateurs et périphériques connectés à votre réseau. En outre, les nouvelles stratégies exposent plus de données à partir du moteur de détection de sécurité des applications dans le nuage pour vous aider à accélérer le processus d’enquête et contiennent les menaces en cours.
  
En tant qu’un administrateur général Office 365 ou un administrateur de sécurité, vous pouvez consulter et si nécessaire, modifier les stratégies par défaut qui sont disponibles avec Office 365 Cloud Application Security.
  
 > [!IMPORTANT]
> Il existe une période de formation initiale de sept (7) jours au cours de laquelle les alertes de comportement anormal ne sont pas déclenchés. L’algorithme de détection des anomalies est optimisée pour réduire le nombre de faux positifs. 
  
## <a name="before-you-begin"></a>Avant de commencer

Vérifiez que :
  
- Votre organisation dispose de [Sécurité d’application Office 365 dans le nuage](office-365-cas-overview.md)et le service est [activé](turn-on-office-365-cas.md).
    
- [L’enregistrement d’audit](turn-audit-log-search-on-or-off.md) est activé pour votre environnement Office 365. 
    
- Vous êtes un administrateur global ou un administrateur de sécurité pour Office 365.
    
## <a name="view-your-anomaly-detection-policies"></a>Afficher vos stratégies de détection des anomalies

1. En tant qu’un administrateur global ou administrateur de sécurité, accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter.<br>Vous accédez à la page de stratégies de sécurité des applications Office 365 dans le nuage.
    
2. Dans la liste **TYPE** , sélectionnez la **stratégie de détection des anomalies**.<br>Votre organisation (ou) par défaut existant des stratégies de détection des anomalies sont affichés.<br>![Stratégies de détection des anomalies dans la sécurité des applications cloud Office 365](media/2e0ee770-787a-4d4a-bea8-389dc765d4c6.png)
  
3. Sélectionnez une stratégie pour consulter ou modifier ses paramètres.
    
4. Choisissez **Update** (Mettre à jour) pour enregistrer vos modifications. 
    
## <a name="learn-more-about-anomaly-detection-policies"></a>Pour plus d’informations sur les stratégies de détection des anomalies

Stratégies de détection des anomalies sont activées automatiquement ; Toutefois, Office 365 Cloud application sécurité a une période de formation initiale de sept jours pendant les anomalies pas toutes les alertes de détection sont déclenchés. Après cela, chaque session est comparée à l’activité, lorsque les utilisateurs ont été actives, des adresses IP, appareils, etc. détectées au cours du dernier mois et le niveau de risque de ces activités. Ces détections font partie du moteur de détection heuristique anomalie que les profils de votre environnement et déclenche des alertes par rapport à une ligne de base qui a été appris sur l’activité de votre organisation. Ces détections également tirer parti des algorithmes d’apprentissage machine conçus pour les utilisateurs et les modèles de journal pour réduire les faux positifs de profil.
  
Anomalies sont détectés par l’analyse d’activité de l’utilisateur. Le risque est évalué en regardant plus de 30 indicateurs de risques différents, regroupées par plusieurs facteurs comme adresse IP risquée, échecs de connexion, activité d’administration, comptes inactifs, emplacement, déplacement impossible, appareil et agent utilisateur et taux d’activité.
  
Alertes de sécurité en fonction des résultats de la stratégie, sont déclenchées. Office 365 Cloud application sécurité ressemble à chaque session dans Office 365 et vous avertit chaque fois qu’un problème survient différent à partir de la ligne de base de votre organisation ou d’une activité régulière d’un utilisateur.
  
Le tableau suivant décrit les stratégies de détection des anomalies par défaut, leur et leur fonctionnement.
  
|**Nom de stratégie de détection des anomalies**|**Fonctionnement**|
|:-----|:-----|
|Déplacement Impossible  <br/> |Identifie les deux activités utilisateur (est une ou plusieurs sessions) d’origine à partir d’emplacements géographiquement distants dans une période inférieure au temps il auraient l’utilisateur pour parvenir à partir de l’emplacement du premier à la seconde, indiquant qu’un autre utilise les mêmes informations d’identification utilisateur. Cette détection s’appuie sur une machine de formation algorithme qui ignore évidentes « faux positifs » qui contribuent à la condition de déplacement impossible, telles que les réseaux privés virtuels et emplacements régulièrement utilisés par d’autres utilisateurs dans l’organisation. La détection a une période de formation initiale de sept jours au cours de laquelle il a eu le modèle d’activité d’un nouvel utilisateur.  <br/> |
|Activité de pays peu fréquente  <br/> |Estime au-delà des emplacements d’activité pour déterminer les emplacements de nouveau et rarement utilisées. Le moteur de détection des anomalies stocke des informations sur les emplacements précédents utilisé par les utilisateurs dans l’organisation. Une alerte est déclenchée lorsqu’une activité se produit à partir d’un emplacement qui a été pas récemment ou ne jamais visité par l’utilisateur ou par un utilisateur dans l’organisation.  <br/> |
|Activité des adresses IP anonyme  <br/> |Identifie que les utilisateurs ont été actives d’une adresse IP qui a été identifiée comme une adresse IP de proxy anonymes. Les proxys sont utilisés par des personnes want masquer l’adresse IP de leur périphérique et peuvent être utilisés pour malveillantes. Cette détection s’appuie sur une machine de formation algorithme qui réduit les « faux positifs », tels que des adresses IP mal balisés sont couramment utilisées par les utilisateurs dans l’organisation.  <br/> |
|Activité d’adresses IP suspectes  <br/> |Identifie que les utilisateurs ont été actives d’une adresse IP qui a été identifiée comme risquée par Microsoft Threat Intelligence. Ces adresses IP sont impliqués dans malveillants, telles que C Botnet&amp;C et qui peut indiquer compte compromis. Cette détection s’appuie sur une machine de formation algorithme qui réduit les « faux positifs », tels que des adresses IP mal balisés sont couramment utilisées par les utilisateurs dans l’organisation.  <br/> |
|Activités inhabituelles (par utilisateur)  <br/> | Identifie les utilisateurs qui effectuent des activités inhabituelles, telles que :  <br/>  --Plusieurs téléchargements de fichiers  <br/>  --Activités de partage de fichiers  <br/>  : Activités de suppression de fichier  <br/>  --Activités l’emprunt d’identité  <br/>  --Activités d’administration  <br/>  Ces stratégies rechercher les activités au sein d’une seule session par rapport à la ligne de base appris, qui pourraient indiquer sur une tentative de violation. Ces détections de tirer parti d’un ordinateur algorithme qui profils utilisateurs ouvrent une session sur le modèle de formation et réduire les faux positifs. Ces détections font partie du moteur de détection heuristique anomalie que les profils de votre environnement et déclenche des alertes par rapport à une ligne de base qui a été appris sur l’activité de votre organisation.  <br/> |
|Plusieurs tentatives de connexion ayant échoué  <br/> |Identifie les utilisateurs qui ont échoué plusieurs tentatives de connexion en une seule session par rapport à la ligne de base par des professionnels qui pourraient indiquer sur une tentative de violation.  <br/> |
   
## <a name="triage-anomaly-detection-alerts"></a>Alertes de détection d’anomalie triage

Comme les alertes qui se vous pouvez trier ces alertes rapidement et déterminer ceux à gérer tout d’abord. Ayant le contexte d’une alerte vous permet de voir une image plus grande et de déterminer si un élément malveillant en effet se produit. Utilisez la procédure suivante pour commencer l’exploration d’une alerte :
  
1. En tant qu’un administrateur global ou administrateur de sécurité, accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter. 
    
2. Choisissez les **alertes** pour afficher vos alertes. 
    
3. Pour obtenir le contexte d’une alerte, procédez comme suit :
    
4. Cliquez sur **examiner** \> **le journal d’activité**.
    
5. Sélectionnez un élément, tel qu’un utilisateur ou l’adresse IP. Le bac d’alimentation insights pertinents s’ouvre.<br>![Dans le journal d’activité, vous pouvez rechercher une adresse IP.](media/32a727c5-e406-4fe2-9443-c1a7fb6628fc.png)
  
6. Dans le bac d’alimentation insights approprié, cliquez sur une commande disponible, par exemple une icône dans la section **Afficher les éléments similaires** .<br> ![Cliquez sur l’icône d’horloge pour voir les activités effectuées dans les 48 heures d’une activité sélectionnée](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
7. Mieux sur l’élément sélectionné en continuant à Explorer les détails de cet élément.
    
Une alerte sur plusieurs échecs de connexion peut-être être en effet suspecte et peut indiquer une attaque potentielle contre les attaques en force. Toutefois, une telle alerte peut également être un problème de configuration d’application, à l’origine de l’alerte d’un faible positif true. Si vous voyez une alerte plusieurs Échec de connexions avec d’autres activités suspectes, il est une probabilité qu’un compte est compromis. Par exemple, supposons qu’une alerte plusieurs Échec de la connexion est suivie d’activité à partir d’une adresse IP de TOR et l’activité de déplacement impossible, les deux indicateurs forts de compromis. Vous pouvez même voir que le même utilisateur effectué une activité de téléchargement en masse, qui est souvent un indicateur de l’intrus effectue d’exfiltration de données. Il s’agit de choses comme que vous pouvez Explorer dans Office 365 Cloud application sécurité pour afficher et trier vos alertes et effectuer une action si nécessaire.
  
## <a name="next-steps"></a>Étapes suivantes

- [Intégrer votre serveur SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Vos adresses IP pour simplifier la gestion de groupe](group-your-ip-addresses-in-ocas.md)
    

