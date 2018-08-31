---
title: Configurer votre client Office 365 pour accroître la sécurité
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 6/27/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Vous guide dans la configuration recommandée pour les paramètres au niveau du client qui affectent la sécurité de votre environnement Office 365. Vos besoins en matière de sécurité peuvent nécessiter plus ou moins de sécurité. Utilisez ces recommandations comme point de départ.
ms.openlocfilehash: e81c3e18bccc9ccaab7c6f018c6f40b5ea796e14
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013868"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Configurer votre client Office 365 pour accroître la sécurité

Cette rubrique vous guide tout au long de la configuration recommandée pour les paramètres au niveau du client qui affectent la sécurité de votre environnement Office 365. Vos besoins en matière de sécurité peuvent nécessiter plus ou moins de sécurité. Utilisez ces recommandations comme point de départ.
  
## <a name="check-office-365-secure-score"></a>Vérifier le Score sécurisé Office 365

Office 365 Score Secure analyse la sécurité de votre organisation Office 365 basée sur les activités normales et les paramètres de sécurité et attribue une note. Commencez en notant votre score actuel. Ajustement des paramètres au niveau du client augmentera votre score. L’objectif est de ne pas atteindre le score maximum, mais pour connaître les opportunités pour protéger votre environnement qui n’affectent pas négativement la productivité pour vos utilisateurs. Voir [Présentation de la note sécurisé Office 365](office-365-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-office-365-security-amp-compliance-center"></a>Paramétrer les stratégies de gestion des menaces de sécurité Office 365 &amp; centre de conformité

L’Office 365 Security &amp; centre de conformité inclut des fonctionnalités qui protègent votre environnement. Il inclut également des rapports et des tableaux de bord que vous pouvez utiliser pour surveiller et effectuer une action. Certaines zones sont fournies avec les configurations de stratégie par défaut. Certaines zones n’incluent pas de stratégies par défaut ou règles. Visitez le site de ces stratégies, sous gestion des menaces pour régler les paramètres de gestion des menaces pour un environnement plus sécurisé. 
  
|Zone ***|Inclut une stratégie par défaut ***|Recommandation ***|
|:-----|:-----|:-----|
|**DAV anti-hameçonnage** <br/> |Non  <br/> | Si vous avez un domaine personnalisé, créez une stratégie anti-hameçonnage pour protéger les comptes de messagerie de vos utilisateurs plus importantes, telles que votre PDG et pour protéger votre domaine. Passez en revue la [définir une stratégie d’anti-hameçonnage DAV](set-up-atp-anti-phishing-policies.md) et créer une stratégie à l’aide de l’exemple comme guide : « exemple : Anti-hameçonnage stratégie pour protéger un utilisateur et un domaine. »|
|**Moteur anti-programme malveillant** <br/> |Oui  <br/> | Modifier la stratégie par défaut :  <br/> • Des pièces jointes courantes de Types de filtre, sélectionnez sur  <br/><br>  Vous pouvez également créer des stratégies de filtrage de programmes malveillants personnalisée et les appliquer à des utilisateurs, groupes ou domaines dans votre organisation.  <br/> <br> Plus d’informations :  <br/> • [Protection contre les programmes malveillants](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> • [Configurer les stratégies anti-programme malveillant](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Pièces jointes DAV fiable** <br/> |Non  <br/> | Dans la page principale pour les pièces jointes fiables, protéger les fichiers de SharePoint, OneDrive et Microsoft Teams en activant cette case :  <br/>  • Activer DAV pour SharePoint, OneDrive et les équipes de Microsoft  <br/> <br> Ajouter une nouvelle stratégie de pièces jointes sécurisées avec ces paramètres :  <br/>  • Bloc — blocage actuelles et futures de courriers électroniques et les pièces jointes par un programme malveillant détecté (choisir cette option)  <br/>  • Activer redirection — (cette case à cocher et entrez une adresse de messagerie, par exemple un compte d’administration ou mise en quarantaine)  <br/>  • Appliquer la sélection ci-dessus si les logiciels malveillants analyse les pièces jointes arrive à expiration ou erreur se produit (cochez cette case)  <br/>  • Appliqué à — le domaine du destinataire est (sélectionnez votre domaine)  <br/>  <br>Plus d’informations : [définir des stratégies de pièces jointes sûres Office 365 DAV](set-up-atp-safe-attachments-policies.md) <br/> |
|**Liens DAV fiable** <br/> |Oui  <br/> | Ajoutez ce paramètre à la stratégie par défaut pour toute l’organisation :  <br/> • Utiliser les liens sécurisés dans : Office 365 ProPlus, Office pour iOS et Android (sélectionnez cette option).  <br/> <br>Stratégie recommandée pour des destinataires spécifiques :  <br/>  • URL seront réécrites et comparées à une liste de liens malveillants connus lorsque l’utilisateur clique sur le lien (sélectionnez cette option).  <br/>  • Les pièces jointes fiables à utiliser pour analyser le contenu téléchargeable (cochez cette case).  <br/>  • Appliqué à — le domaine du destinataire est (sélectionnez votre domaine).  <br/> <br> Plus d’informations : [les liens sans échec Office 365 DAV](atp-safe-links.md).  <br/> |
|**Blocage du courrier indésirable (filtrage de messagerie)** <br/> |Oui  <br/> | Les points à surveiller pour :  <br/>  • Trop de courrier indésirable, choisissez les paramètres personnalisés et de modifier la stratégie de filtrage du courrier indésirable par défaut.  <br/>  Aide à la décision de • usurpation d’identité, passez en revue les expéditeurs sont l’usurpation de votre domaine. Bloquer ou autoriser les expéditeurs.<br/>  <br>Plus d’informations : [Protection de blocage du courrier indésirable messagerie Office 365](anti-spam-protection.md).  <br/> |
|**DKIM (DomainKeys identifié messagerie)** <br/> |Oui  <br/> |DKIM est un processus d’authentification qui peuvent aider à protéger les expéditeurs et destinataires de falsifié (usurpés) et au courrier électronique de phishing. Votre client inclut une signature par défaut pour votre domaine. Créer une signature DKIM supplémentaire si vous ajoutez des domaines à votre client.<br/> <br>Plus d’informations : [DKIM utilisés pour valider le courrier sortant envoyé à partir de votre domaine personnalisé dans Office 365](https://technet.microsoft.com/en-us/library/mt695945%28v=exchg.150%29.aspx) <br/> |
   
## <a name="view-dashboards-and-reports-in-the-security-amp-compliance-center"></a>Afficher les rapports et tableaux de bord de la sécurité &amp; centre de conformité

Visitez le site de ces rapports et des tableaux de bord pour en savoir plus sur l’intégrité de votre environnement. Les données de ces rapports sera plus riches que votre organisation utilise des services Office 365. À ce stade, vous familiariser avec ce que vous pouvez surveiller et effectuer une action. Pour plus d’informations, voir : [rapports de sécurité Office 365 &amp; centre de conformité](reports-in-security-and-compliance.md).
  
|Tableau de bord ***|****Description****|
|:-----|:-----|
|Tableau de bord de gestion des menaces  <br/> |Dans la section Gestion des menaces de sécurité &amp; conformité center, utiliser ce tableau de bord pour voir les menaces qui ont déjà été gérés et comme un outil pratique pour la création de rapports pour les décideurs sur ce qui aide à la décision de menace a déjà fait pour sécuriser votre Business.  <br/> |
|Explorer des menaces  <br/> |C’est également dans la section Gestion des menaces de sécurité &amp; centre de conformité. Si vous êtes étude ou rencontre une attaque par rapport à votre client Office 365, utilisez l’Explorateur de menace pour l’analyse des menaces. Threat explorer affiche le volume des attaques au fil du temps, et vous pouvez analyser ces données par les familles de menaces et infrastructure intrus. Vous pouvez aussi marquer tout le courrier suspect pour la liste des Incidents.  <br/> |
|Rapports — tableau de bord  <br/> |Dans la section rapports de sécurité &amp; centre de conformité, les rapports de contrôle d’affichage pour vos organisations Exchange Online et SharePoint Online. Vous pouvez également accéder Azure Active Directory (AD) utilisateur connexion rapports, rapports d’activité de l’utilisateur, et ouvrir une session à partir de la page d’affichage des rapports d’audit de l’Azure AD.  <br/> |
   
![Sécurité &amp; tableau de bord de centre de conformité](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Configurer d’autres paramètres au niveau du client Exchange Online

La plupart des contrôles de sécurité et protection dans le centre d’administration Exchange sont également incluses dans le centre de conformité et de sécurité. Il est inutile de configurer ces deux emplacements. Voici quelques paramètres supplémentaires qui sont recommandées. 
  
|Zone ***|Inclut une stratégie par défaut ***|Recommandation ***|
|:-----|:-----|:-----|
|**Flux de messagerie** (Règles de transport)  <br/> |Non  <br/> | Ajouter une règle de flux de messagerie pour vous protéger contre les logiciels. Voir « Comment utiliser des règles de Transport Exchange pour suivre ou bloquer les messages électroniques avec des extensions de fichier utilisées par les logiciels » dans cet article de blog : [comment traiter les logiciels](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/).<br><br/> Créer une règle de transport pour empêcher le transfert automatique des courriers électroniques à des domaines externes. Pour plus d’informations, voir [Atténuation Client transfert règles externes dont le Score d’informations sécurisé](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).<br/> <br>Plus d’informations : [flux de messagerie (règles de transport) dans Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx) <br/> |
|**Activer l’authentification moderne** <br/> |Non  <br/> | L’authentification moderne dans Office 365 est une condition préalable à l’aide de l’authentification multifacteur (MFA). MFA est recommandée pour sécuriser l’accès aux ressources de cloud, y compris le courrier électronique.<br/>  <br>Consultez les rubriques suivantes :  <br/> • [Activer ou désactiver l’authentification moderne dans Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/> • [Skype pour Business Online : activer votre client pour l’authentification moderne](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/>  <br>Authentification moderne est activée par défaut pour Office 2016 clients SharePoint Online et OneDrive for Business.  <br/>  <br>Plus d’informations : [l’authentification moderne avec les clients Office à l’aide Office 365](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a) <br/> |
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Configurer des stratégies de partage à l’échelle du client dans le centre d’administration SharePoint

Recommandations de Microsoft pour la configuration des sites d’équipe SharePoint à l’augmentation des niveaux de protection, en commençant par la protection de la ligne de base. Pour plus d’informations, voir [fichiers et des sites d’informations sécurisé SharePoint Online](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
Sites d’équipe SharePoint configurés au niveau de la ligne de base autorisent le partage de fichiers avec des utilisateurs externes à l’aide de liens de l’accès anonyme. Cette approche est recommandée au lieu de l’envoi de fichiers dans le message électronique. 
  
Pour prendre en charge les objectifs de protection de base, configurer des stratégies de partage de client à l’échelle comme indiqué ici. Partage des paramètres pour des sites spécifiques peut être plus restrictif que cette stratégie de client à l’échelle, mais pas plus permissif. 
  
|Zone ***|Inclut une stratégie par défaut ***|Recommandation ***|
|:-----|:-----|:-----|
|**Le partage** (SharePoint Online et OneDrive entreprise)  <br/> |Oui  <br/> | Partage externe est activé par défaut. Ces paramètres sont recommandées :<br/>  • Autoriser le partage à des utilisateurs externes authentifiés et l’utilisation de liens de l’accès anonyme (paramètre par défaut).  <br/>  • Des liens de l’accès anonyme à expiration dans ce nombre de jours. Entrez un nombre, si vous le souhaitez, tels que des 30 derniers jours.<br/>  Type de lien • par défaut, sélectionnez interne (personnes dans l’organisation uniquement). Les utilisateurs qui souhaitent partager à l’aide de liens anonyme doivent choisir cette option dans le menu partage.<br/>  <br>Plus d’informations : [vue d’ensemble du partage externe](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85) <br/> |
   
Centre d’administration SharePoint et OneDrive entreprise centre d’administration incluent les mêmes paramètres. Les paramètres dans un centre d’administration s’appliquent aux deux.
  
## <a name="configure-settings-in-azure-active-directory"></a>Configurer les paramètres dans Azure Active Directory

Veillez à consulter ces deux zones dans Azure Active Directory pour terminer l’installation du client à l’échelle pour les environnements plus sécurisés.
  
### <a name="configure-named-locations-under-conditional-access"></a>Configurer des emplacements nommés (sous accès conditionnel)

Si votre organisation comprend des bureaux avec un accès réseau sécurisé, ajoutez les plages d’adresses IP approuvées pour Azure Active Directory en tant qu’emplacements nommés. Cette fonctionnalité permet de réduire le nombre de signalée faux positifs pour les événements de connexion de risque. 
  
Voir : [emplacements nommés dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Bloquer les applications qui ne prennent pas en charge l’authentification moderne

L’authentification multifacteur nécessite des applications qui prennent en charge l’authentification moderne. Les applications qui ne prennent pas en charge l’authentification moderne ne peuvent pas être bloquées à l’aide de règles d’accès conditionnel.
  
Pour les environnements sécurisés, veillez à désactiver l’authentification pour les applications qui ne prennent pas en charge l’authentification moderne. Vous pouvez procéder ainsi dans Azure Active Directory avec un contrôle qui seront prochainement disponibles.
  
En attendant, utilisez une des méthodes suivantes pour effectuer cette opération pour SharePoint Online et OneDrive entreprise :
  
- Utiliser PowerShell, voir [bloquer les applications qui n’utilisent pas l’authentification moderne](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- Configurer cette option dans le centre d’administration SharePoint sur le « page d’accès aux appareils — « Contrôler l’accès à partir d’applications qui n’utilisent pas l’authentification moderne ». Choisissez le bloc. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Prendre en main Cloud application sécurité ou de sécurité d’application Office 365 dans le nuage

Utilisez Office 365 Cloud application sécurité pour évaluer les risques, à l’alerte sur les activités suspectes et d’effectuer automatiquement une action. Nécessite un plan Office 365 E5.
  
Ou bien, Microsoft Cloud Application Security permet d’obtenir la visibilité plus profonde même une fois que l’accès est accordé, les contrôles complètes et une meilleure protection pour toutes les applications dans le cloud, notamment Office 365. 
  
Étant donné que cette solution recommande le plan E5 EMS, nous vous recommandons de que commencer avec la sécurité d’application Cloud afin que vous pouvez utiliser cette avec d’autres applications SaaS dans votre environnement. Démarrer avec les paramètres et les stratégies par défaut.
  
Plus d’informations :
  
- Rubrique relative au [déploiement de Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- Rubrique relative aux [informations supplémentaires concernant Microsoft Cloud App Security](https://www.microsoft.com/en-us/cloud-platform/cloud-app-security)
    
- [Vue d’ensemble de la sécurité d’application Office 365 dans le nuage](office-365-cas-overview.md)
    
![Tableau de bord Cloud App Security](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Ressources supplémentaires

Ces articles et ces guides fournissent des informations précises supplémentaires pour la sécurisation de votre environnement Office 365 :
  
- [Instructions de sécurité de Microsoft pour campagnes politiques, les organismes sans but lucratif et les autres organisations agiles](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (vous pouvez utiliser ces recommandations dans tout environnement, en particulier les environnements en nuage uniquement) 
    
- [Stratégies de sécurité recommandées et les configurations des identités et des périphériques](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (ces recommandations incluent l’aide pour les environnements AD FS) 
    

