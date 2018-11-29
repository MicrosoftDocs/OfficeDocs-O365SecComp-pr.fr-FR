---
title: Nouveautés de la sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.date: 11/28/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d674763c-a4c9-4604-8623-68c1836d27f3
description: Nouveautés dans Office 365 Cloud Application Security
ms.openlocfilehash: a3ca4504d80cbb39b51ecbcf3a5165bc5139e07c
ms.sourcegitcommit: bf628da123a89d9422e8cff02165b1e2d35dfe12
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26872012"
---
# <a name="what-is-new-in-office-365-cloud-app-security"></a>Nouveautés de la sécurité d’application Office 365 dans le nuage

**Résumé** Lisez cet article pour obtenir une vue d’ensemble rapide des mises à jour et nouvelles fonctionnalités dans Office 365 Cloud Application Security (anciennement appelé gestion de la sécurité avancée Office 365), qui repose sur [Microsoft Cloud Application Security](https://aka.ms/whatiscas).
  
Cet article est mis à jour fréquemment, comme les fonctionnalités sont ajoutées ou améliorées. Mises à jour de sécurité des applications dans le nuage Office 365 sont libérées environ deux semaines après Microsoft Cloud application des mises à jour, et pas toutes les mises à jour Microsoft dans le nuage Application Security s’appliquent à la sécurité d’application Office 365 dans le nuage. En outre, les nouvelles fonctionnalités peuvent prendre au moins une semaine après leur date de publication s’affiche dans votre environnement de sécurité d’application Office 365 dans le nuage.

## <a name="office-365-cloud-app-security-release-136"></a>Version de sécurité des applications dans le nuage Office 365 136

*Publication le 25 novembre 2018,*

**Suite [Microsoft Cloud Application Security version 136](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-136)**:

- **Mises à jour de la découverte du cloud** L’Analyseur de journal personnalisé a été amélioré pour prendre en charge supplémentaires et le trafic web plus complexe consigne les formats. Comme partie de ces utilisateurs améliorations peut maintenant entrer des en-têtes personnalisés pour les fichiers journaux CSV sans en-tête, utilisez les délimiteurs spéciaux pour les fichiers de clé-valeur, processus de format de fichier journal système et bien plus encore.

- **Nouvelle stratégie de détection des anomalies : règles de manipulation de boîte de réception suspect** Cette stratégie profiles votre environnement et les alertes de déclencheurs lorsque règles suspects de supprimer ou de déplacement des messages ou des dossiers sont définies dans la boîte de réception d’un utilisateur. Cela peut indiquer que le compte d’utilisateur est compromis, que les messages sont intentionnellement masquées et que la boîte aux lettres est utilisé pour distribuer du courrier indésirable ou des programmes malveillants dans votre organisation.

- **Prise en charge des groupes de stratégies d’autorisation des applications** Nuage application sécurité vous donne désormais la possibilité de définir des stratégies d’autorisation application plus en détail, en fonction de l’appartenance aux groupes d’utilisateurs autorisés les applications. Par exemple, un administrateur peut décider définir une stratégie qui révoque des applications non courantes si elles demandent des autorisations haute, d’uniquement si l’utilisateur qui a autorisé les autorisations est un membre du groupe Administrateurs.


## <a name="office-365-cloud-app-security-releases-133-134-and-135"></a>Versions de sécurité des applications dans le nuage Office 365 133, 134 et 135

*Publié en octobre-novembre, 2018*

**Après la [version de Microsoft Cloud Application Security 133, 134 et 135](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-133-134-135)**:

- **Nouvelles stratégies de détection des anomalies** sont progressivement présentant :
    
    - La nouvelle stratégie **exfiltration de données aux applications non sanctionnées** est automatiquement activée pour vous avertir lorsqu’un utilisateur ou l’adresse IP utilise une application qui est déconseillée pour effectuer une activité qui ressemble à une tentative pour exfiltrate d’informations à partir de votre organisation.
    
    - La nouvelle stratégie **d’activités de machine virtuelle supprimer plusieurs** profils de votre environnement et déclenche des alertes lorsque les utilisateurs de supprimer plusieurs ordinateurs virtuels en une seule session, par rapport à la ligne de base dans votre organisation.

- **Découverte de nuage prennent en charge i - filtre** La fonctionnalité de découverte de nuage sécurité Cloud application bénéficie désormais prise en charge de l’Analyseur de journal système i-filtre.


## <a name="office-365-cloud-app-security-release-131"></a>Version de sécurité des applications dans le nuage Office 365 131

*Publication le 16 septembre 2018,*

**Suite [Microsoft Cloud Application Security version 131](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-131)**:

- **Automatiquement révoquer des autorisations sur les applications OAuth risquées** Vous pouvez désormais contrôler les applications OAuth vos utilisateurs ont accès, par révocation des autorisations d’application pour les applications OAuth sur Office. Lorsque vous créez une stratégie d’autorisation App, vous pouvez désormais définir la stratégie pour révoquer l’autorisation d’une application.

- **Découverte de nuage analyseur intégré supplémentaire pris en charge** Découverte de nuage prend désormais en charge le format de journal Forcepoint Web sécurité Cloud.

  
## <a name="office-365-cloud-app-security-release-130"></a>Version de sécurité des applications dans le nuage Office 365 130

*Publié le 5 septembre 2018*

**Suite [Microsoft Cloud Application Security version 130](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-130)**:

- **Nouvelle barre de menus** Pour fournir une expérience d’administration plus cohérente entre les produits Microsoft 365 et vous permettent de tableau croisé dynamique plus facilement entre les solutions de sécurité Microsoft, la barre de menus de portail de sécurité d’application Cloud a déplacé vers le côté gauche de l’écran. Cette navigation cohérente expérience vous aide à orienter lors du déplacement d’un portail de sécurité de Microsoft à l’autre.<br/>![Barre de menus dans la sécurité d’application Office sur le nuage](media/OCAS-MenuBar.png)<br/>

- **Profil d’application impact OAuth** Vous pouvez maintenant envoyer les commentaires de l’équipe sécurité d’application Cloud pour nous indiquer s’il existe une application OAuth découverte dans votre organisation qui semble malveillante. Cette nouvelle fonctionnalité vous permet de faire partie de la Communauté de la sécurité et améliorer l’analyse et le score de risque d’application OAuth. Pour plus d’informations, voir [Gérer les autorisations d’application](manage-app-permissions-in-ocas.md).

- **Analyseurs de nouvelle découverte dans le nuage** Les analyseurs de découverte dans le nuage prennent désormais en charge iboss passerelle de nuage sécurisé et Sophos XG.


## <a name="office-365-cloud-app-security-release-128"></a>Version de sécurité des applications dans le nuage Office 365 128

*Publié le 5 août 2018* 
  
**Suite [Microsoft Cloud Application Security version 128](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-128)**: 
  
- **Autorisations d’application entre plusieurs applications** Pour les applications qui ont été accordées des autorisations de l’application, vous pouvez maintenant interdire ou approuver les applications multiples en une seule action. Par exemple, vous pouvez passer en revue toutes les applications qui ont été accordées des autorisations par les utilisateurs de votre organisation, sélectionnez toutes les applications que vous souhaitez exclure, puis cliquez sur applications interdiction pour tous les consentement accordé et n’est plus permettra aux utilisateurs d’octroyer des autorisations pour ces applications. 
    
- **Nouvelle requête suggérée : PIBR prêt** Il existe une nouvelle requête suggérée pour vous permettent d’identifier les applications découvertes PIBR prêt. PIBR a détecté récemment une priorité pour les administrateurs de sécurité. Cette requête vous permet de facilement identifier les applications qui sont prêt PIBR et atténuer les menaces à évaluer le risque des applications qui ne sont pas. 
    
## <a name="office-365-cloud-app-security-release-126"></a>Version de sécurité des applications dans le nuage Office 365 126

*Publication le 7 juillet 2018,* 
  
**Suite [Microsoft Cloud Application Security version 126](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-126)**: 
  
- **Correction automatique pour les activités suspectes** Vous pouvez maintenant définir des actions de correction automatique de session suspecte déclenchée par les stratégies de détection des anomalies. Cette amélioration permet d’être averti immédiatement lorsqu’une violation se produit et appliquer automatiquement des actions de la gouvernance, tels que suspendre utilisateur. Pour plus d’informations, voir [stratégies de détection des anomalies dans Office 365 Cloud Application Security](anomaly-detection-policies-in-ocas.md).
    
- **Détection automatique des applications de OAuth risquée** Outre les examiner des applications OAuth connectées à votre environnement existant, sécurité pour application Cloud Microsoft Office 365 vous permet maintenant définir des notifications automatiques pour vous informer lorsqu’une application OAuth répond à certains critères. Par exemple, vous pouvez automatiquement averti lorsqu’il existe des applications qui nécessitent un niveau d’autorisation élevé et ont été autorisés par plus de 50 utilisateurs. Pour plus d’informations, voir [Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage](manage-app-permissions-in-ocas.md).
    
- **Gestion du fournisseur de services de sécurité gérés (MSSP) pris en charge** Office 365 Cloud application sécurité maintenant fournit une meilleure expérience de gestion à MSSPs et permet de configurer les partenaires externes en tant qu’administrateurs avec un des rôles actuellement disponibles dans Office 365 Cloud Application Security. En outre, les administrateurs avec des droits d’accès au plusieurs client maintenant peuvent facilement croisés entre les clients. 
    
## <a name="office-365-cloud-app-security-release-124"></a>Version de sécurité des applications dans le nuage Office 365 124

*Publication le 10 juin 2018,* 
  
**Suite [Microsoft Cloud Application Security version 124](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-124)**: 
  
- **Déploiements d’étendue** Les entreprises peuvent déterminer granulaire pour surveiller et protéger les utilisateurs qui en fonction de l’appartenance au groupe. Cette fonctionnalité vous permet de sélectionner les utilisateurs dont les activités n’apparaîtront pas pour les applications protégées. Surveillance étendue est particulièrement utile pour la conformité et gestion des licences. Certaines réglementations de conformité nécessitent que vous évitez de surveiller les utilisateurs de certains pays en raison des réglementations locales. Et, vous pouvez surveiller le nombre d’utilisateurs de rester dans les limites de vos licences de sécurité d’application Office 365 dans le nuage. 
    
- **Nouveau serveur de messagerie** Le serveur de messagerie Office 365 nuage sécurité des applications a changé et utilise les plages d’adresses IP différentes. Pour vous assurer que vous pouvez obtenir des notifications, ajoutez les nouvelles adresses IP à votre liste d’autorisation de blocage du courrier indésirable. Pour les organisations qui personnalisent leurs notifications, nuage application sécurité permet automatiquement à l’aide de MailChimp, un service de messagerie tiers. Pour la liste des adresses IP de messagerie serveur et des instructions permettant d’utiliser les MailChimp, voir [configuration réseau requise (Microsoft Cloud Application Security)](https://docs.microsoft.com/cloud-app-security/network-requirements) et les [paramètres de messagerie (Microsoft Cloud Application Security)](https://docs.microsoft.com/cloud-app-security/mail-settings).
    
## <a name="office-365-cloud-app-security-release-121"></a>Version de sécurité des applications dans le nuage Office 365 121

*Publié le 6 mai 2018* 
  
**Suite [Microsoft Cloud Application Security version 121](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-121)**: 
  
- **Améliorations de stratégie de détection des anomalies**. Stratégies de détection d’anomalie de sécurité Office 365 Cloud application ont été améliorées pour inclure deux nouveaux types de détection des menaces qui sont progressivement présentant : 
    
  - **Activité logiciels.** Fonctionnalités de détection de logiciels sont étendues avec détection d’anomalie afin de vous fournir une couverture plus complète contre les attaques de logiciels sophistiqués. 
    
  - **Interrompue d’activité de l’utilisateur.** Interrompue permet d’activité utilisateur vous permet de contrôler les comptes d’utilisateurs terminés qui ont peut-être été annulé à partir d’applications d’entreprise, mais qui peuvent encore avez accès à certaines ressources d’entreprise. 
    
    Pour afficher vos [stratégies de détection des anomalies](anomaly-detection-policies-in-ocas.md), dans le portail Office 365 Cloud application sécurité, choisissez **contrôle** \> **stratégies**.
    
## <a name="office-365-cloud-app-security-release-120"></a>Version de sécurité des applications dans le nuage Office 365 120

*Publication le 22 avril 2018,* 
  
**Suite [Microsoft Cloud Application Security version 120](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-120)**: 
  
- **Applications internes en tant que des activités de l’utilisateur**. Pour Office 365 et Azure Active Directory (AD Azure), nous allons maintenant progressivement présentant la capacité de détecter des applications internes en tant qu’activités de compte d’utilisateur effectuées par les applications Office 365 et Azure AD (internes et externes). Cela vous permet de créer des stratégies afin de vous envoyer une alerte si une application effectue des activités inattendues et non autorisées. 
    
- **Exporter des champs dans la liste des autorisations de l’application**. Lors de l’exportation d’une liste des autorisations d’application au format csv, des champs supplémentaires tels que publisher, utilisation des autorisations au niveau et de la Communauté fournis pour faciliter le processus de conformité et d’enquête. 
    
## <a name="office-365-cloud-app-security-release-119"></a>Version de sécurité des applications dans le nuage Office 365 119

*Publication le 1, avril 2018* 
  
**Suite [Microsoft Cloud Application Security version 119](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-119)**: 
  
- **Améliorations apportées à la découverte en nuage**. La découverte du nuage fournit plus d’informations sur les utilisateurs les plus fréquents et des adresses IP, ce qui facilite pour l’affichage des détails d’utilisation d’Office 365 et les autres applications. Pour plus d’informations, voir [conclusions de découverte révision app dans Office 365 Cloud Application Security](review-app-discovery-findings-in-ocas.md).
    
    ![Le tableau de bord dans le nuage découverte a été mis à jour.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
  
## <a name="office-365-cloud-app-security-release-118"></a>Version de sécurité des applications dans le nuage Office 365 118

*Publié le 18 mars 2018* 
  
**Suite [Microsoft Cloud Application Security version 118](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-118)**: 
  
- **Barracuda prennent en charge**. Découverte de nuage prend désormais en charge les pare-feux Barracuda F série et transmettre en continu de série F Barracuda pare-feu web journal. 
    
## <a name="office-365-cloud-app-security-release-117"></a>Version de sécurité des applications dans le nuage Office 365 117

*Publié le 6 mars 2018* 
  
**Suite [Microsoft Cloud Application Security version 117](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-117)**: 
  
- **i-filtre prend en charge**. Découverte de nuage prend désormais en charge i-filtre. 
    
## <a name="office-365-cloud-app-security-release-116"></a>Version de sécurité des applications dans le nuage Office 365 116

*Publié le 18 février 2018* 
  
**Suite [Microsoft Cloud Application Security version 116](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-116)**: 
  
- **Améliorations des stratégies de détection des anomalies**. Stratégies de détection d’anomalie dans Office 365 Cloud application sécurité ont été améliorées avec les nouvelles détections scénario, y compris les déplacements soir, activité à partir d’une adresse IP suspecte et de tentatives de connexion ayant échouée plusieurs. Les nouvelles stratégies sont automatiquement activés, fournissant une détection des menaces out-of-the-box entre votre environnement cloud. En outre, les nouvelles stratégies exposent plus de données à partir du moteur de détection Office 365 Cloud application sécurité, qui peut aider à accélérer le processus d’enquête et contiennent les menaces en cours. Pour plus d’informations, voir l’article Microsoft Cloud Application Security [obtenir analytique comportement instantanée et la détection des anomalies](https://docs.microsoft.com/cloud-app-security/anomaly-detection-policy).
    
- **Prise en charge de journal Analyseur des formats de point de contrôle**. Les analyseurs de journal de détection de nuage prennent désormais en charge les deux autres formats de point de contrôle : XML et KPC. 
    
## <a name="office-365-cloud-app-security-release-114"></a>Version de sécurité des applications dans le nuage Office 365 114

*Publié le 21 janvier 2018* 
  
**Suite [Microsoft Cloud Application Security version 114](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-114)**: 
  
- **État du Service**. Vous pouvez maintenant vérifier l’état du service Office 365 Cloud application sécurité actuelle en accédant à **l’aide de** \> **état du système**. 
    
    ![Cliquez sur Aide \> état du système pour afficher l’état d’intégrité du système](media/2b496dac-ed9d-4480-83b6-85f9510d3aea.png)
  
- **Requêtes personnalisé pour le journal d’activité**. Au début de la version 114, la possibilité de créer et enregistrer des requêtes personnalisées dans le journal d’activité est présentant progressivement. Requêtes personnalisées permettent de créer des modèles de filtre qui peuvent être réutilisées pour examen approfondi. En outre, suggéré requêtes ont été ajoutés pour fournir des modèles d’enquête out-of-the-box pour filtrer vos activités et découverte des applications. Requêtes suggérées incluent des filtres personnalisés pour identifier les risques tels que les activités de l’emprunt d’identité, activités administrateur, applications de stockage risquée nuage non compatibles, les applications d’entreprise avec chiffrement faible et les risques de sécurité. Utilisez les requêtes suggérées comme point de départ, les modifier si nécessaire, puis les enregistrer en tant que nouvelle requête. 
    
## <a name="office-365-cloud-app-security-release-113"></a>Version de sécurité des applications dans le nuage Office 365 113

*Publication le 8 janvier 2018,* 
  
**Suite [Microsoft Cloud Application Security version 113](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-113)**: 
  
- **Prise en charge Analyseur de journal pour les formats génériques**. Les analyseurs de journal de détection de nuage prennent désormais en charge les formats génériques suivants : LEEF et W3C Format CEF. 
    
## <a name="office-365-cloud-app-security-release-112"></a>Version de sécurité des applications dans le nuage Office 365 112

*Publication le 24 décembre 2017* 
  
**Suite [Microsoft Cloud Application Security version 112](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-112)**: 
  
- **Bac d’alimentation insight pertinents**. Dans le journal d’activité, vous pouvez maintenant accéder le bac d’alimentation insight pertinents en cliquant sur une adresse IP ou le nom d’utilisateur. 
    
    ![Cliquez sur un nom d’utilisateur ou l’adresse IP à voir le bac d’alimentation insight pertinents dans le journal d’activité.](media/8e32b3fa-8c0c-4c5e-b248-fe7d7e1b516d.png)
  
- **Possibilité d’afficher plusieurs activités en un clic**. Dans le bac d’alimentation insight pertinent, vous pouvez cliquer pour afficher toutes les activités effectuées dans les 48 heures d’une activité sélectionnée l’icône d’horloge. 
    
    ![Dans le bac d’alimentation insights pertinent, vous pouvez cliquer sur l’icône d’horloge pour voir les activités effectuées dans les 48 heures d’une activité sélectionnée](media/c6c96aa0-98e5-4205-8873-45f8d6fd0843.png)
  
- **Améliorations d’analyseur de journal pour SRX Juniper**. Améliorations apportées à l’Analyseur de journal de découverte dans le nuage pour SRX Juniper. 
    
## <a name="office-365-cloud-app-security-release-111"></a>Version de sécurité des applications dans le nuage Office 365 111

*Publication le 10 décembre 2017* 
  
**Suite [Microsoft Cloud Application Security version 111](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-111)**: 
  
- **Améliorations du filtre heure**. Filtres de temps sont désormais plus faciles à utiliser. Pour accéder à un filtre de temps, dans un affichage, tels que des journaux d’activité, les stratégies, les alertes, à l’aide de la vue avancée, sélectionnez **Date** dans la liste des filtres. Puis choisissez une option, comme avant, après ou entre les deux pour appliquer le filtre de temps. 
    
    ![Utilisez le filtre de Date pour afficher les informations avant, après ou entre les dates.](media/9dbb2a10-f68f-413b-8b4e-88911152cb92.png)
  
## <a name="office-365-cloud-app-security-release-110"></a>Version de sécurité des applications dans le nuage Office 365 110

*Publication le 26 novembre 2017* 
  
**Suite [Microsoft Cloud Application Security version 110](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-110)**: 
  
- **Intégration du serveur SIEM désormais disponible**. Se connecter à votre serveur SIEM à la sécurité d’application Office 365 dans le nuage. Vous pouvez maintenant envoyer du alertes et des activités automatiquement à votre serveur SIEM de choix en configurant des Agents SIEM. Voir [intégrer votre serveur SIEM avec Office 365 Cloud Application Security](integrate-your-siem-server-with-office-365-cas.md).
    
- **Faciliter l’accès au contenu de l’aide**. Nouveau point d’interrogation dans le coin supérieur droit, vous pouvez maintenant accéder le contenu d’aide à partir de dans les pages du portail Office 365 Cloud Application Security. Chaque lien est contextuelle, vous en tenant aux informations dont vous avez besoin, en fonction de la page que vous êtes en. 
    
- **Envoyez-nous vos commentaires**. À l’aide de l’icône dans le coin supérieur droit, vous pouvez maintenant envoyer des commentaires à partir de chaque page du portail Office 365 Cloud Application Security. Cela permet de signaler des bogues, demander de nouvelles fonctionnalités et partager votre expérience directement avec l’équipe de sécurité d’application Office 365 dans le nuage. 
    
## <a name="office-365-cloud-app-security-release-102"></a>Version de sécurité des applications dans le nuage Office 365 102

*Publication le 13 août 2017* 
  
**Suite [Microsoft Cloud Application Security version 102](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-102)**: 
  
- **Nouvelles actions d’enquête utilisateur** activer un niveau de zoom aux enquêtes utilisateur. Dans une page d’examiner, vous pouvez pointer sur une activité, compte d’utilisateur ou appliquer en tant qu’un filtre, et à partir de là, vous pouvez afficher le rapport des activités ou des événements. 
    
## <a name="office-365-cloud-app-security-release-100"></a>Version de sécurité des applications dans le nuage Office 365 100

*Publication le 17 juillet 2017* 
  
**Suite [Microsoft Cloud Application Security version 100](https://docs.microsoft.com/cloud-app-security/release-notes#cloud-app-security-release-100)**: 
  
- **Extensions de sécurité** est un tableau de bord où vous pouvez gérer centralement toutes les extensions de sécurité de votre Office 365 nuage sécurité des applications, y compris les jetons d’API et agents SIEM. Pour afficher le tableau de bord extensions sécurité, procédez comme suit : 
    
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Accédez à des **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.
    
    ![Dans la sécurité &amp; centre de conformité, sélectionnez alertes \> gestion avancée des alertes \> accédez à gestion de la sécurité avancée](media/9792b121-9cd4-4faa-a6e0-81cfab4bf2f2.png)
  
4. Choisir les **paramètres** \> **extensions de sécurité**.
    
    ![Dans le portail ASM, choisissez paramètres \> extensions de sécurité](media/f03d47a1-91ff-41b9-9baf-b514cffe41a8.png)
  
- **Amélioration de l’analyse**. Améliorations ont été apportées dans le journal de détection de nuage mécanisme d’analyse. Erreurs internes sont beaucoup moins susceptibles de se produire. 
    
- **Formats de fichiers journaux attendue**. Le format attendu journal pour les journaux de découverte dans le nuage maintenant fournit des exemples pour les formats de journal système et FTP. 
    
## <a name="related-topics"></a>Voir aussi

[Contenu de l’aide sur le nuage application sécurité Office 365](office-365-cas-help.md)
  
[Activités d’utilisation après avoir déployé la sécurité des applications cloud Office 365](utilization-activities-for-ocas.md)
  
[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

