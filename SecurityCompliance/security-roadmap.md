---
title: Feuille de route de sécurité Office 365-priorités principales des 30 premiers jours, 90 jours et au-delà
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: "Principales recommandations de l'équipe Cybersecurity de Microsoft pour la mise en œuvre de fonctionnalités de sécurité pour protéger votre environnement Office 365. "
ms.openlocfilehash: ba74827c34a869ee11553f02d9085b6f015b2d9d
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30955167"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Feuille de route de sécurité Office 365-priorités principales des 30 premiers jours, 90 jours et au-delà

Cet article présente les principales recommandations de l'équipe Cybersecurity de Microsoft pour la mise en œuvre de fonctionnalités de sécurité pour protéger votre environnement Office 365. Cet article est adapté à partir d'une session Microsoft enFlamme, [Secure Office 365 comme un Cybersecurity Pro: principales priorités pour les 30 jours, 90 jours et plus](https://www.youtube.com/watch?v=luignzNyR-o). Cette session a été développée et présentée par Mark Simos et Matt Kemelhar, Enterprise Cybersecurity Architects.
  
Contenu de cet article :
  
- [Résultats de la feuille de route](security-roadmap.md#Roadmap)
    
- [30 jours — un succès rapide puissant](security-roadmap.md#Thirdaydays)
    
- [90 jours — amélioration des protections](security-roadmap.md#Ninetydays)
    
- [Après](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Résultats de la feuille de route
<a name="Roadmap"> </a>

Ces recommandations de feuille de route sont échelonnées sur trois phases dans un ordre logique avec les objectifs suivants.

|||
|:-----|:-----|
| |Résultats
|30 jours|Configuration rapide:  <br/> • Protections d'administration de base  <br/> • Journalisation et analyse  <br/> • Protections d'identité de base  <br/> Configuration du client  <br/>  Préparation des parties prenantes  <br/> |
|90 jours|Protections avancées:  <br/> • Comptes d'administrateur  <br/>  • Comptes &amp; d'utilisateur de données  <br/>  Visibilité des besoins en matière de conformité, de menace et d'utilisateur  <br/>  Adapter et implémenter les stratégies et les protections par défaut  <br/> |
|Après|Ajuster et affiner les stratégies et les contrôles clés  <br/> Étendre les protections aux dépendances locales  <br/> Intégration aux processus métier et de sécurité (menace légale, Insider, etc.)  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 jours — un succès rapide puissant
<a name="Thirdaydays"> </a>

Ces tâches peuvent être accomplies rapidement et ont un faible impact sur les utilisateurs.
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâches  <br/> |
|Gestion de la sécurité  <br/> |• Vérifier le score sécurisé et noter votre score actuel ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Activez la journalisation d'audit pour Office 365. Consultez [la rubrique Rechercher dans le journal d'audit](search-the-audit-log-in-security-and-compliance.md).  <br/> • [Configurez votre client Office 365 pour renforcer la sécurité](tenant-wide-setup-for-increased-security.md) .  <br/>  • Examen régulier des tableaux de bord et des rapports dans le centre de sécurité Microsoft 365 et la sécurité des applications Cloud.  <br/> |
|Protection contre les menaces  <br/> |[Connectez Office 365 à Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) pour démarrer la surveillance à l'aide des stratégies de détection des menaces par défaut pour les comportements anormaux. Il faut sept jours pour créer une ligne de base pour la détection des anomalies.  <br><br/>  Implémenter la protection pour les comptes d'administrateur:  <br/> • Utilisez des comptes d'administration dédiés pour l'activité d'administration.  <br/>  • Appliquer l'authentification multifacteur (MFA) pour les comptes d'administrateur.  <br/>  • Utilisez un [appareil Windows 10 hautement sécurisé](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) pour l'activité de l'administrateur.  <br/> |
|Gestion des identités et des accès  <br/> |• [Activer la protection des identités Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Pour les environnements d'identité fédérée, appliquez la sécurité des comptes (longueur du mot de passe, âge, complexité, etc.).  <br/> |
|Protection des informations  <br/> | Consultez l'exemple de recommandations pour la protection des informations. La protection des informations nécessite une coordination au sein de votre organisation. Commencez à utiliser ces ressources :  <br/> • [Protection des informations Office 365 pour RGPD](http://aka.ms/o365gdpr) <br/> • [Sécuriser les sites et les fichiers SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (y compris le partage, la classification, la protection contre la perte de données et Azure information protection)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 jours — amélioration des protections
<a name="Ninetydays"> </a>

Ces tâches prennent un peu plus de temps à planifier et à implémenter, mais augmentent considérablement votre posture de sécurité. 
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâche  <br/> |
|Gestion de la sécurité  <br/> | • Vérifier le score de sécurité pour les actions recommandées [https://securescore.office.com](https://securescore.office.com)pour votre environnement ().  <br/>  • Poursuivez régulièrement l'examen des tableaux de bord et des rapports dans le centre de sécurité Microsoft 365, dans la sécurité des applications Cloud et dans les outils SIEM.  <br/>  • Recherchez et mettez en œuvre des mises à jour logicielles.  <br/>  • Effectuez des simulations d'attaque pour le Spear Phishing, le vaporisation des mots de passe et les attaques de mot de passe en force à l'aide d'un simulateur d' [attaque](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) (inclus avec [Office 365 Threat Intelligence](office-365-ti.md)).  <br/>  • Recherchez le risque de partage en examinant la sécurité des rapports intégrés dans Cloud App Security (sous l'onglet examiner).  <br/>  • Consultez le [Gestionnaire de conformité](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) pour vérifier l'état des réglementations qui s'appliquent à votre organisation (par exemple, RGPD, NIST 800-171).  <br/> |
|Protection contre les menaces  <br/> | Implémenter des protections améliorées pour les comptes d'administrateur:  <br/>  • ConFigurez les [stations de travail d'accès privilégié](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (pattes) pour l'activité d'administration.  <br/>  • ConFigurez [Azure ad Privileged identIty Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • ConFigurez un outil de gestion des événements et des informations sur la sécurité (SIEM) pour collecter les données de journalisation à partir d'Office 365, de la sécurité des applications Cloud et d'autres services, y compris AD FS. Le journal d'audit Office 365 stocke les données de 90 jours seulement. La capture de ces données dans l'outil SIEM vous permet de stocker des données pendant une période plus longue.  <br/> |
|Gestion des identités et des accès  <br/> | • Activer et appliquer l'authentification multiFACTEUR pour tous les utilisateurs.  <br/>  • Implémentez un ensemble d' [accès conditionnel et de stratégies associées](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Protection des informations  <br/> | Adaptez et implémentez les stratégies de protection des informations. Ces ressources incluent des exemples:  <br/> • [Protection des informations Office 365 pour RGPD](http://aka.ms/o365gdpr) <br/> • [Sécuriser les sites et les fichiers SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Utilisez les stratégies de protection contre la perte de données et les outils de surveillance dans Office 365 pour les données stockées dans Office 365 (au lieu de la sécurité des applications Cloud). <br><br>Utilisez la sécurité des applications Cloud avec Office 365 pour les fonctionnalités d'alerte avancées (autres que la protection contre la perte de données).  <br/> |
   
## <a name="beyond"></a>Après
<a name="Beyond"> </a>

Il s'agit de mesures de sécurité importantes qui s'appuient sur le travail précédent. 
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâche  <br/> |
|Gestion de la sécurité  <br/> |• Poursuivez la planification des actions suivantes à l' [https://securescore.office.com](https://securescore.office.com)aide du score de sécurité ().  <br/>  • Poursuivez régulièrement l'examen des tableaux de bord et des rapports dans le centre de sécurité Microsoft 365, dans la sécurité des applications Cloud et dans les outils SIEM.  <br/>  • Recherchez et mettez en œuvre des mises à jour logicielles.  <br/>  • Intégrez eDiscovery à vos processus de réponse légale et de menace.  <br/> |
|Protection contre les menaces  <br/> | • Implémentez un [accès privilégié sécurisé](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (Spa) pour les composants d'identité sur site (AD, AD FS).  <br/>  • Utilisez Cloud App Security pour surveiller les menaces d'Insiders.  <br/>  • Découvrez comment utiliser le service de sécurité de l'application Cloud.  <br/> |
|Gestion des identités et des accès  <br/> | • Affiner les stratégies de protection des informations:  <br/>  • Protection des données d'informations Azure et protection contre la perte de données (DLP) pour Office 365.  <br/>  • Stratégies et alertes de sécurité des applications Cloud.  <br/> |
|Protection des informations  <br/> | • Affinez les stratégies et les processus opérationnels.  <br/>  • Utilisez Azure AD Identity Protection pour identifier les menaces d'Insiders.  <br/> |
   
Voir aussi: [Comment limiter les cyberattaques rapides telles que Petya et WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  

