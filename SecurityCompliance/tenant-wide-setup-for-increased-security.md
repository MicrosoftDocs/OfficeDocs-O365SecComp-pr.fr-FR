---
title: Configurer votre client Office 365 pour une sécurité accrue
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Vous guide tout au long de la configuration recommandée pour les paramètres à l'échelle du client qui affectent la sécurité de votre environnement Office 365. Vos besoins en matière de sécurité peuvent nécessiter plus ou moins de sécurité. Utilisez ces recommandations comme point de départ.
ms.openlocfilehash: 91471f5e4b16f6950b1f74d747ebce3f802e4890
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260270"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Configurer votre client Office 365 pour une sécurité accrue

Cette rubrique décrit la configuration recommandée pour les paramètres à l'échelle du client qui affectent la sécurité de votre environnement Office 365. Vos besoins en matière de sécurité peuvent nécessiter plus ou moins de sécurité. Utilisez ces recommandations comme point de départ.
  
## <a name="check-office-365-secure-score"></a>Vérifier le score de sécurité d'Office 365

Le score de sécurité d'Office 365 analyse la sécurité de votre organisation Office 365 en fonction de vos activités normales et des paramètres de sécurité et affecte un score. Commencez par prendre note de votre score actuel. L'ajustement de certains paramètres à l'échelle du client augmentera votre score. L'objectif est de ne pas atteindre le score maximal, mais de prendre conscience des possibilités de protection de votre environnement qui n'ont pas d'impact négatif sur la productivité de vos utilisateurs. Consultez [la rubrique Introducing the Office 365 Secure score](office-365-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-microsoft-365-security-center"></a>Réglage des stratégies de gestion des menaces dans le centre de sécurité Microsoft 365

Le centre de sécurité Microsoft 365 inclut des fonctionnalités qui protègent votre environnement. Il inclut également des rapports et des tableaux de bord que vous pouvez utiliser pour surveiller et prendre des mesures. Certaines zones sont dotées de configurations de stratégie par défaut. Certaines zones n'incluent pas de stratégies ou de règles par défaut. Consultez ces stratégies sous gestion des menaces pour ajuster les paramètres de gestion des menaces à un environnement plus sécurisé. 
  
|Zone * * * *|Inclut une stratégie par défaut * * * *|Recommandation * * *|
|:-----|:-----|:-----|
|**Anti-hameçonnage** <br/> |Oui  <br/> | Si vous avez un domaine personnalisé, créez une stratégie anti-hameçonnage pour protéger les comptes de messagerie de vos utilisateurs les plus précieux, comme votre PDG, et pour protéger votre domaine. Consultez la rubrique relative à la [configuration d'une stratégie anti-hameçonnage](set-up-anti-phishing-policies.md) et créez une stratégie en vous reportant à l'exemple: «exemple: stratégie anti-hameçonnage pour protéger un utilisateur et un domaine».|
|**Moteur anti-programme malveillant** <br/> |Oui  <br/> | Modifiez la stratégie par défaut:  <br/> &ensp;&ensp;• Filtre de types de pièces jointes courantes — sélectionnez activé  <br/><br>  Vous pouvez également créer des stratégies de filtrage des programmes malveillants personnalisées et les appliquer à des utilisateurs, des groupes ou des domaines spécifiés dans votre organisation.  <br/> <br> Plus d’informations :  <br/> &ensp;&ensp;• [Protection contre les programmes malveillants](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> &ensp;&ensp;• [Configurer des stratégies anti-programmes malveillants](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Pièces jointes fiables ATP** <br/> |Non  <br/> | Sur la page principale des pièces jointes fiables, protégez les fichiers dans SharePoint, OneDrive et Microsoft teams en activant cette case à cocher:  <br/>  &ensp;&ensp;• Activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams  <br/> <br> Ajoutez une nouvelle stratégie de pièces jointes fiables avec ces paramètres:  <br/>  &ensp;&ensp;• Bloquer: bloquer les e-mails et pièces jointes en cours et à venir avec des programmes malveillants détectés (choisissez cette option)  <br/>  &ensp;&ensp;• Activer la redirection — (activez cette case à coCher et entrez une adresse de messagerie, comme un compte d'administrateur ou de mise en quarantaine)  <br/>  &ensp;&ensp;• Appliquer la sélection ci-dessus si l'analyse anti-programme malveillant pour les pièces jointes expire ou si une erreur se produit (cochez cette case)  <br/>  &ensp;&ensp;• Appliqué à: le domaine du destinataire est (sélectionnez votre domaine)  <br/>  <br>Plus d'informations: [Configuration des stratégies de pièces jointes approuvées pour Office 365 ATP](set-up-atp-safe-attachments-policies.md) <br/> |
|**Liens fiables ATP** <br/> |Oui  <br/> | Ajoutez ce paramètre à la stratégie par défaut pour l'ensemble de l'Organisation:  <br/> &ensp;&ensp;• Utiliser des liens fiables dans: Office 365 proPlus, Office pour iOS et Android (sélectionnez cette option).  <br/> <br>Stratégie recommandée pour des destinataires spécifiques:  <br/>  &ensp;&ensp;• Les URL sont réécrites et vérifiées par rapport à une liste de liens malveillants connus lorsque l'utilisateur clique sur le lien (sélectionnez cette option).  <br/>  &ensp;&ensp;• Utiliser des pièces jointes fiables pour analyser le contenu téléchargeable (activez cette case à cocher).  <br/>  &ensp;&ensp;• Appliqué à: le domaine du destinataire est (sélectionnez votre domaine).  <br/> <br> Plus d'informations: [liens approuvés pour Office 365 ATP](atp-safe-links.md).  <br/> |
|**Blocage du courrier inDésirable (filtrage du courrier)** <br/> |Oui  <br/> | Éléments à surveiller:  <br/>  &ensp;&ensp;• Courrier indésirable trop nombreux: choisissez les paramètres personnalisés et modifiez la stratégie de filtrage du courrier indésirable par défaut.  <br/>  &ensp;&ensp;• Usurpation d'identité: Vérifiez les expéditeurs qui usurpent votre domaine. Bloquer ou autoriser ces expéditeurs.  <br/>  <br>Plus d'informations: protection contre le courrier inDésirable pour [les courriers électroniques Office 365](anti-spam-protection.md).  <br/> |
|***Authentification de messagerie*** <br/> |Oui  <br/> |L'authentification de messagerie utilise un système DNS (Domain Name System) pour ajouter des informations vérifiables aux messages électroniques concernant l'expéditeur d'un message électronique. Office 365 configure l'authentification de messagerie pour son domaine par défaut (onmicrosoft.com), mais les administrateurs d'Office 365 peuvent également utiliser l'authentification de messagerie pour les domaines personnalisés. Trois méthodes d'authentification sont utilisées: <br/> <br> &ensp;&ensp;• Sender Policy Framework (SPF).<br/>&ensp;&ensp;&ensp;&ensp;-Pour le programme d'installation, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l'usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md). <br/> &ensp;&ensp;• DomainKeys Identified Identified Mail (DKIM). <br/> &ensp;&ensp;&ensp;&ensp;-Voir [use DKIM for email in your Custom Domain in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email). <br>&ensp;&ensp;&ensp;&ensp;-Après avoir configuré DKIM, activez-le dans le centre de sécurité.<br/> &ensp;&ensp;• Authentification de message basée sur un domaine, création de rapports et conformité (DMARC). <br/> &ensp;&ensp;&ensp;&ensp;-Pour le programme d'installation d'DMARC, [Utilisez DMARC pour valider le courrier électronique dans Office 365](use-dmarc-to-validate-email.md).<br/>  <br/>
|

> [!NOTE]
> Pour les déploiements non standard de SPF, les déploiements hybrides et la résolution des problèmes: [la manière dont Office 365 utilise SPF (Sender Policy Framework) pour éviter l'usurpation](how-office-365-uses-spf-to-prevent-spoofing.md).

## <a name="view-dashboards-and-reports-in-the-security-and-compliance-centers"></a>Afficher des tableaux de bord et des rapports dans les centres de sécurité et de conformité

Visitez ces rapports et tableaux de bord pour en savoir plus sur l'état de santé de votre environnement. Les données de ces rapports deviennent plus riches lorsque votre organisation utilise les services Office 365. Pour l'instant, familiarisez-vous avec les éléments que vous pouvez surveiller et prendre des mesures. Pour plus d'informations, consultez la rubrique relative aux [rapports dans les centres de sécurité et de conformité Microsoft 365](reports-in-security-and-compliance.md).
  
|Tableau de bord * * * *|****Description****|
|:-----|:-----|
|Tableau de bord de gestion des menaces  <br/> |Dans la section gestion des menaces du centre de sécurité, utilisez ce tableau de bord pour voir les menaces qui ont déjà été gérées, et en tant qu'outil pratique pour le signalement aux décideurs d'entreprise sur les capacités d'enquête et de réponse des menaces déjà effectuées vers Sécurisez votre entreprise.  <br/> |
|Explorateur de menaces  <br/> |Il s'agit également de la section gestion des menaces du centre de sécurité. Si vous recherchez ou rencontrez une attaque contre votre client Office 365, utilisez l'Explorateur de menaces pour analyser les menaces. L'Explorateur de menaces vous montre le volume des attaques au fil du temps et vous pouvez analyser ces données par des familles de menaces, une infrastructure d'agresseur, et bien plus encore. Vous pouvez également marquer tous les messages suspects pour la liste des incidents.  <br/> |
|Rapports — tableau de bord  <br/> |Dans la section rapports du centre de sécurité, affichez les rapports d'audit de vos organisations SharePoint Online et Exchange Online. Vous pouvez également accéder aux rapports de connexion utilisateur Azure Active Directory (Azure AD), aux rapports d'activité de l'utilisateur et au Journal d'audit Azure AD à partir de la page afficher les rapports.  <br/> |
   
![Tableau de bord du centre de sécurité](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Configurer des paramètres supplémentaires à l'échelle du client Exchange Online

De nombreux contrôles de sécurité et de protection dans le centre d'administration Exchange sont également inclus dans le centre de sécurité. Vous n'avez pas besoin de les configurer aux deux emplacements. Voici quelques paramètres supplémentaires qui sont recommandés. 
  
|Zone * * * *|Inclut une stratégie par défaut * * * *|Recommandation * * *|
|:-----|:-----|:-----|
|**Flux de messagerie** (règles de flux de messagerie, également appelées règles de transport)|Non|Ajoutez une règle de flux de messagerie pour vous protéger contre les ransomware. Voir «comment utiliser les règles de transport Exchange pour suivre ou bloquer les courriers électroniques avec des extensions de fichiers utilisées par des ransomware» dans cet article de blog: [Comment traiter les ransomware](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/). <br><br/> Consultez les rubriques suivantes: <br/>•[Protéger contre les ransomware](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data?view=o365-worldwide#ransomware)<br/>•[Protection contre les programmes malveillants et les ransomware dans Office 365](office-365-malware-and-ransomware-protection.md)<br/><br/>  Créez une règle de flux de messagerie pour empêcher le transfert automatique des messages vers des domaines externes. Pour plus d'informations, consultez la rubrique [minimisation des règles de transfert externe des clients avec le score sécurisé](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/). <br/><br/> Plus d'informations: [règles de flux de messagerie (règles de transport) dans Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx)|
|**Activer l'authentification moderne**|Non|L'authentification moderne dans Office 365 est une condition préalable à l'utilisation de l'authentification multifacteur (MFA). L'authentification multiFACTEUR est recommandée pour sécuriser l'accès aux ressources Cloud, y compris la messagerie électronique. <br/><br/> Consultez les rubriques suivantes:  <br/>• [Activer ou désactiver l'authentification moderne dans Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/>• [Skype entreprise Online: activation de votre client pour l'authentification moderne](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/><br/> L'authentification moderne est activée par défaut pour les clients Office 2016, SharePoint Online et OneDrive entreprise. <br/><br/> Plus d'informations: [utilisation de l'authentification moderne office 365 avec les clients Office](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a)|
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Configurer des stratégies de partage à l'échelle du client dans le centre d'administration SharePoint

Recommandations de Microsoft relatives à la configuration des sites d'équipe SharePoint à des niveaux de protection croissants, à partir de la protection de base. Pour plus d'informations, consultez la rubrique sécuriser des [sites et des fichiers SharePoint Online](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
Les sites d'équipe SharePoint configurés au niveau de base autorisent le partage de fichiers avec des utilisateurs externes à l'aide de liens d'accès anonymes. Cette approche est recommandée au lieu d'envoyer des fichiers par courrier électronique. 
  
Pour prendre en charge les objectifs de la protection de base, configurez les stratégies de partage à l'échelle du client comme il est recommandé ici. Les paramètres de partage de sites individuels peuvent être plus restrictifs que cette stratégie à l'échelle du client, mais pas plus permissif. 
  
|Zone * * * *|Inclut une stratégie par défaut * * * *|Recommandation * * *|
|:-----|:-----|:-----|
|**Partage** (SharePoint Online et OneDrive entreprise)|Oui|Le partage externe est activé par défaut. Ces paramètres sont recommandés: <br/>• Autorisez le partage vers les utilisateurs externes authentifiés et l'utilisation des liens d'accès anonyme (paramètre par défaut). <br/>  • Les liens d'accès anonyme expirent dans ce nombre de jours. Entrez un nombre, si vous le souhaitez, par exemple 30 jours. <br/>• Type de lien par défaut — sélectionnez interne (personnes de l'organisation uniquement). Les utilisateurs qui souhaitent partager à l'aide de liens anonymes doivent choisir cette option dans le menu partage. <br/><br/> Plus d'informations: [vue d'ensemble du partage externe](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85)|
   
Le centre d'administration SharePoint et le centre d'administration OneDrive entreprise incluent les mêmes paramètres. Les paramètres dans le centre d'administration s'appliquent aux deux.
  
## <a name="configure-settings-in-azure-active-directory"></a>Configurer les paramètres dans Azure Active Directory

Veillez à visiter ces deux domaines dans Azure Active Directory pour effectuer une configuration à l'échelle du client pour des environnements plus sécurisés.
  
### <a name="configure-named-locations-under-conditional-access"></a>Configurer des emplacements nommés (sous accès conditionnel)

Si votre organisation comprend des bureaux disposant d'un accès réseau sécurisé, ajoutez les plages d'adresses IP approuvées à Azure Active Directory en tant qu'emplacements nommés. Cette fonctionnalité permet de réduire le nombre de faux positifs signalés pour les événements de risque de connexion. 
  
Voir: [locations nommées dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Bloquer les applications qui ne prennent pas en charge l'authentification moderne

L'authentification multifacteur nécessite des applications qui prennent en charge l'authentification moderne. Les applications qui ne prennent pas en charge l'authentification moderne ne peuvent pas être bloquées à l'aide des règles d'accès conditionnel.
  
Pour les environnements sécurisés, veillez à désactiver l'authentification pour les applications qui ne prennent pas en charge l'authentification moderne. Vous pouvez effectuer cette opération dans Azure Active Directory avec un contrôle bientôt disponible.
  
En attendant, utilisez l'une des méthodes suivantes pour effectuer cette commande pour SharePoint Online et OneDrive entreprise:
  
- Utiliser PowerShell, consultez la rubrique [bloquer les applications qui n'utilisent pas l'authentification moderne](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- ConFigurez-le dans le centre d'administration SharePoint sur la page «accès au périphérique» — «contrôler l'accès à partir d'applications qui n'utilisent pas l'authentification moderne». Choisissez bloquer. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Prise en main de la sécurité des applications Cloud ou de la sécurité des applications Cloud Office 365

Utilisez Office 365 Cloud App Security pour évaluer les risques, pour alerter les activités suspectes et pour agir automatiquement. Nécessite Office 365 E5 plan.
  
Vous pouvez également utiliser Microsoft Cloud App Security pour obtenir une visibilité plus poussée, même après avoir accordé un accès, des contrôles complets et une meilleure protection pour toutes vos applications Cloud, y compris Office 365. 
  
Étant donné que cette solution recommande le plan EMS E5, nous vous recommandons de commencer par la sécurité des applications Cloud afin de pouvoir l'utiliser avec d'autres applications SaaS dans votre environnement. Démarrez avec les stratégies et les paramètres par défaut.
  
Plus d’informations :
  
- Rubrique relative au [déploiement de Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- Rubrique relative aux [informations supplémentaires concernant Microsoft Cloud App Security](https://www.microsoft.com/en-us/cloud-platform/cloud-app-security)
    
- [Overview of Office 365 Cloud App Security](office-365-cas-overview.md)
    
![Tableau de bord Cloud App Security](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Ressources supplémentaires

Ces articles et guides fournissent des informations normatives supplémentaires pour la sécurisation de votre environnement Office 365:
  
- [Conseils de sécurité Microsoft pour les campagnes politiques, les organisations à but non lucratif et d'autres organisations agiles](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (vous pouvez utiliser ces recommandations dans n'importe quel environnement, en particulier les environnements uniquement en nuage) 
    
- [Configurations et stratégies de sécurité recommandées pour les identités et les appareils](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (ces recommandations incluent de l'aide pour les environnements AD FS) 
    

