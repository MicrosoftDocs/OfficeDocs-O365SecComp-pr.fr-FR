---
title: Guide de sécurité Office 365 - priorités pour les 30 premiers jours, 90 jours et au-delà
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Recommandations de l’équipe de sécurité de Microsoft d’implémenter les fonctionnalités de sécurité pour protéger votre environnement Office 365. '
ms.openlocfilehash: 58767ea9a2b825d1583d9135f9d8edcb0d20d7c2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "25450079"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Guide de sécurité Office 365 - priorités pour les 30 premiers jours, 90 jours et au-delà

Cet article contient des recommandations de l’équipe de sécurité de Microsoft d’implémenter les fonctionnalités de sécurité pour protéger votre environnement Office 365. Cet article est adapté à partir d’une session Microsoft Ignite : [Secure Office 365 comme une sécurité pro : principaux des priorités pour les 30 premiers jours, 90 jours et au-delà de](https://www.youtube.com/watch?v=luignzNyR-o). Cette session a été développée et présentée par Mark Simos et Matt Kemelhar, architectes de sécurité.
  
Contenu de cet article :
  
- [Résultats de la feuille de route](security-roadmap.md#Roadmap)
    
- [30 derniers jours : puissants wins rapides](security-roadmap.md#Thirdaydays)
    
- [90 jours — enhanced protections](security-roadmap.md#Ninetydays)
    
- [Au-delà de](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Résultats de la feuille de route
<a name="Roadmap"> </a>

Ces recommandations de feuille de route sont transférées entre les trois phases dans un ordre logique avec les objectifs suivants.

|||
|:-----|:-----|
| |Résultats
|30 jours|Configuration rapide :  <br/> • Des protections de base d’administration  <br/> Analytique et journalisation •  <br/> • Des protections identité de base  <br/> Configuration du client  <br/>  Préparer les parties prenantes  <br/> |
|90 jours|Protections avancées :  <br/> • Les comptes d’administration  <br/>  • Données &amp; comptes d’utilisateurs  <br/>  Visibilité des besoins en matière de conformité, des menaces et utilisateur  <br/>  Adapter et mettre en œuvre des protections et des stratégies par défaut  <br/> |
|Au-delà de|Ajuster et affiner les contrôles et stratégies de clé  <br/> Étendre les protections aux dépendances sur site  <br/> Intégration des processus métiers et de sécurité (juridiques, menaces internes, etc.).  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 derniers jours : puissants wins rapides
<a name="Thirdaydays"> </a>

Ces tâches peuvent être accomplies rapidement et ont un faible impact sur les utilisateurs.
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâches  <br/> |
|Gestion de la sécurité  <br/> |• Vérifier le Score d’informations sécurisé et prenez note de votre score actuel ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Activer l’enregistrement d’audit pour Office 365. Voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).<br/> • [Configurer votre client Office 365 pour accroître la sécurité](tenant-wide-setup-for-increased-security.md) .  <br/>  • Vérifier régulièrement des tableaux de bord et des rapports dans le Office 365 sécurité et centre de conformité et nuage application.  <br/> |
|Protection contre les menaces  <br/> |[Connecter Office 365 à la sécurité d’application Cloud Microsoft](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) pour démarrer l’analyse en utilisant les stratégies de détection de menace par défaut des comportements anormales. Elle prend sept jours pour créer une planification pour détecter une anomalie.<br><br/>  Implémenter la protection pour les comptes d’administration :  <br/> • Utiliser dédiée admin des comptes pour l’activité d’administration.  <br/>  • Mise en œuvre l’authentification multifacteur (MFA) pour les comptes d’administration.  <br/>  • Utiliser un [hautement sécurisés périphérique Windows 10](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) pour l’activité d’administration.  <br/> |
|Gestion des identités et des accès  <br/> |• [Activer la Protection d’identité Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Pour les environnements d’identités fédérées, appliquer la sécurité de compte (longueur de mot de passe, âge, complexité, etc.).  <br/> |
|Protection des informations  <br/> | Passez en revue les recommandations de protection des informations exemple. Protection des informations nécessite une coordination au sein de votre organisation. Mise en route avec les ressources suivantes :<br/> • [Office 365 Information Protection pour PIBR](http://aka.ms/o365gdpr) <br/> • [Fichiers et des sites d’informations sécurisé SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (inclut le partage, classification, prévention des pertes de données et la Protection des informations Azure)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 jours — enhanced protections
<a name="Ninetydays"> </a>

Ces tâches prennent un peu plus de temps à planifier et à implémenter, mais augmentent considérablement votre posture de sécurité. 
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâche  <br/> |
|Gestion de la sécurité  <br/> | • Vérifier le Score d’informations sécurisé pour les mesures recommandées pour votre environnement ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Continuer à consulter régulièrement des tableaux de bord et rapports de la sécurité pour Microsoft Office 365 et centre de conformité, nuage application outils de sécurité et SIEM.  <br/>  • Rechercher et d’implémenter des mises à jour logicielles.  <br/>  • Réaliser des simulations attaque pour sonde-hameçonnage, refroidissement par mot de passe et les attaques en force brute de mot de passe [Attaque Simulator](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) (inclus avec [Office 365 Threat Intelligence](office-365-ti.md)).  <br/>  • Apparence pour le partage des risques en examinant les rapports intégrés dans le nuage Application Security (sur l’onglet examiner).  <br/>  • Vérifiez le [Gestionnaire de conformité](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) pour consulter le statut des réglementations qui s’appliquent à votre organisation (par exemple, PIBR, NIST 800-171).  <br/> |
|Protection contre les menaces  <br/> | Implémenter des protections améliorées pour les comptes d’administration :  <br/>  • Configurer [Des stations de travail accès privilégié](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (PAWs) pour l’activité d’administration.  <br/>  • Configurer [la gestion des identités Azure AD privilégié](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • Configurer un outil sécurité de gestion (SIEM) des informations et des événements à collecter les données de journalisation d’Office 365, la sécurité d’application dans le nuage et les autres services, y compris les services AD FS. Le journal d’Audit de Office 365 stocke les données que 90 jours. Capturer ces données dans l’outil SIEM vous permet de stocker les données pour une période plus longue.<br/> |
|Gestion des identités et des accès  <br/> | • Activer et appliquer MFA pour tous les utilisateurs.  <br/>  • Implémenter un ensemble [d’accès conditionnel et les stratégies associées](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Protection des informations  <br/> | Adapter et implémenter des stratégies de protection des informations. Ces ressources incluent des exemples :<br/> • [Office 365 Information Protection pour PIBR](http://aka.ms/o365gdpr) <br/> • [Fichiers et des sites d’informations sécurisé SharePoint Online](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Utiliser des stratégies de protection contre la perte de données et les outils d’analyse dans Office 365 pour les données stockées dans Office 365 (au lieu de nuage Application Security). <br><br>Utiliser le nuage application sécurité avec Office 365 avancé d’alerte de fonctionnalités (autre que la prévention des pertes de données).  <br/> |
   
## <a name="beyond"></a>Au-delà de
<a name="Beyond"> </a>

Il s’agit des mesures de sécurité importantes qui s’appuient sur le travail précédent. 
  
|||
|:-----|:-----|
|Domaine  <br/> |Tâche  <br/> |
|Gestion de la sécurité  <br/> |• Continuer la planification des actions suivantes à l’aide de Score d’informations sécurisé ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Continuer à consulter régulièrement des tableaux de bord et rapports de la sécurité pour Microsoft Office 365 et centre de conformité, nuage application outils de sécurité et SIEM.  <br/>  • Continuer à rechercher et d’implémenter des mises à jour logicielles.  <br/>  • Intégrer eDiscovery dans votre juridiques et des processus de réponse de menace.  <br/> |
|Protection contre les menaces  <br/> | • Mettre en œuvre l' [Accès privilégié d’informations sécurisé](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA) pour les composants d’identité dans les locaux (AD, AD FS).  <br/>  • Utiliser la sécurité dans le nuage application à surveiller pour les menaces internes.  <br/>  • Découvrir l’utilisation de clichés instantanés SaaS IT à l’aide de sécurité d’application dans le nuage.  <br/> |
|Gestion des identités et des accès  <br/> | • Affiner des stratégies de protection des informations :  <br/>  • Protection des informations azure et Office 365 prévention de perte de données (DLP).  <br/>  • Des politiques de sécurité de l’application dans le nuage et alertes.  <br/> |
|Protection des informations  <br/> | • Affiner stratégies et les processus opérationnels.  <br/>  • Protection d’identité utiliser Azure AD pour identifier les menaces internes.  <br/> |
   
Voir aussi : [comment atténuer cyberattaques rapide tels que Petya et WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  

