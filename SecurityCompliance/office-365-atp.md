---
title: Office 365 – Protection avancée contre les menaces
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 03/28/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 – Protection avancée contre les menaces inclut des pièces jointes sécurisées, des liens sûrs, des outils anti-hameçonnage avancés, des outils de création de rapports et des fonctionnalités d’intelligence contre les menaces.
ms.openlocfilehash: d9dda9b19f601e26d01a18f7602f4fae3e0a0cb4
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761720"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 – Protection avancée contre les menaces

> [!IMPORTANT]
> Cet article est destiné aux entreprises qui ont [Office 365 – Protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Si vous utilisez Outlook.com, Office 365 Famille ou Office 365 Personnel et que vous recherchez des informations sur les liens fiables dans Outlook, reportez-vous à [Sécurité d’Outlook.com renforcée](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Vue d'ensemble

Office 365 – Protection avancée contre les menaces (ATP) protège votre organisation contre les menaces malveillantes posées par les messages électroniques, les liens (URL) et les outils de collaboration. ATP inclut :

- [Stratégies de protection contre les menaces](#configure-atp-policies) : définissez des stratégies de protection contre les menaces pour définir le niveau de protection approprié pour votre organisation. 

- [Rapports](#view-atp-reports) : affichez des rapports en temps réel pour contrôler les performances d’ATP au sein de votre organisation. 

- [Fonctionnalités de recherche et de réponse aux menaces](#use-threat-investigation-and-response-capabilities) : utilisez des outils de pointe pour étudier, comprendre, simuler et prévenir les menaces. 

- [Fonctionnalités automatisées d’investigation et de réponse](#save-time-with-automated-investigation-and-response) : gagnez du temps pour investiguer et atténuer les menaces.

## <a name="office-365-atp-plan-1-and-plan-2"></a>Office 365 – Protection avancée contre les menaces Plan 1 et Plan 2

ATP est inclus dans Office 365 E5 ; toutefois, les plans ATP 1 et ATP 2 sont disponibles en tant que complément pour certains abonnements. Pour plus d’informations, reportez-vous à [Disponibilité des fonctionnalités pour les différents plans ATP](https://docs.microsoft.com/fr-FR/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).

## <a name="configure-atp-policies"></a>Configurer des stratégies ATP

Office 365 – Protection avancée contre les menaces fournit de nombreux outils permettant de déterminer un niveau de protection approprié pour votre organisation. 

L’équipe de sécurité de votre organisation doit définir des stratégies pour chaque outil ATP dans le Centre de sécurité et conformité Office 365. Accédez à **Stratégie de gestion** > **menaces** pour accéder aux options de stratégie. (Pour obtenir de l’aide sur ce point, reportez-vous à [Guide de démarrage rapide : configurer Office 365 – Protection avancée contre les menaces](checklist-atp-setup.md).)

Les stratégies définies pour votre organisation déterminent le comportement et le niveau de protection des menaces prédéfinies. Les options de stratégie sont extrêmement flexibles. Par exemple, l’équipe de sécurité de votre organisation peut affecter une protection affinée contre les menaces au niveau de l’utilisateur, de l’organisation, du destinataire et du domaine. Il est important de revoir vos stratégies régulièrement, car de nouvelles menaces et défis apparaissent quotidiennement.  

- [Pièces jointes fiables ATP](atp-safe-attachments.md) : fournit une protection dès le premier jour pour protéger votre système de messagerie, en vérifiant les pièces jointes pour du contenu malveillant. Il achemine les messages et les pièces jointes qui ne comportent pas de signature de virus/programme malveillant vers un environnement spécial, puis utilise les techniques de machine learning et d’analyse pour détecter les intentions malveillantes. Si aucune activité suspecte n’est détectée, le message est transféré vers la boîte aux lettres. Pour plus d’informations, reportez-vous à [Définir des stratégies de pièces jointes fiables Office 365 – Protection avancée contre les menaces](set-up-atp-safe-attachments-policies.md).

- [Liens fiables ATP](atp-safe-links.md) : permet de vérifier les URL au moment du clic, par exemple, dans les messages électroniques et les fichiers Office. La protection est continue et s’applique à l’ensemble de votre environnement de messagerie et Office. Les liens sont numérisés pour chaque clic : les liens fiables restent accessibles et les liens malveillants sont bloqués de façon dynamique. Pour plus d’informations, reportez-vous à [Configurer les stratégies de liens fiables Office 365 – Protection avancée contre les menaces](https://docs.microsoft.com/fr-FR/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP pour SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) : protège votre organisation lorsque les utilisateurs collaborent et partagent des fichiers, en identifiant et en bloquant les fichiers malveillants dans les sites d’équipe et les bibliothèques de documents. Pour obtenir plus d’informations, consultez l’article [Activer Office 365 ATP pour SharePoint, OneDrive et Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [Protection anti-hameçonnage ATP](atp-anti-phishing.md) : détecte les tentatives d’usurpation d’identité entre vos utilisateurs et les domaines personnalisés. Cela permet d’appliquer des modèles de machine learning et des algorithmes avancés de détection de l’emprunt d’identité pour contrer des attaques par hameçonnage. Pour en savoir plus, reportez-vous à [Configuration de l’anti-hameçonnage d’Office 365 – Protection avancée contre les menaces et des stratégies anti-hameçonnage](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Afficher les rapports ATP

Office 365 – Protection avancée contre les menaces inclut un [tableau de bord de création de rapports](view-reports-for-atp.md) avancé pour contrôler vos performances ATP. Vous pouvez y accéder via **Rapports > Tableau de bord** dans le centre de sécurité et conformité. 

Les rapports sont mis à jour en temps réel, ce qui vous fournit les informations les plus récentes. Ces rapports fournissent également des recommandations et vous informent contre les menaces imminentes. Les rapports prédéfinis incluent les données suivantes : 

- [Threat Explorer (et détections en temps réel)](threat-explorer.md)

- [Rapport sur l’état de la protection contre les menaces](view-reports-for-atp.md#threat-protection-status-report)

- [Rapport sur les types de fichiers ATP](view-reports-for-atp.md#atp-file-types-report)

- [Rapport de destruction de message ATP](view-reports-for-atp.md#atp-message-disposition-report)

- ... et bien plus encore. 

## <a name="use-threat-investigation-and-response-capabilities"></a>Utilisation de l’examen des menaces et des fonctionnalités de réponse

Office 365 – Protection avancée contre les menaces Plan 2 inclut des [outils examen des menaces et des fonctionnalités de réponse](office-365-ti.md) qui permettent à l’équipe de sécurité de votre organisation d’anticiper, de comprendre et de prévenir les attaques malveillantes. 

- [Les suivis de menace](threat-trackers.md) fournissent la dernière intelligence sur les problèmes de sécurité sur Internet. Par exemple, vous pouvez afficher des informations sur les derniers programmes malveillants et prendre des contre-mesures avant qu’ils ne deviennent réellement une menace pour votre organisation. Les suivis disponibles incluent des [suivis important](threat-trackers.md#noteworthy-trackers), des [suivis de tendances](threat-trackers.md#trending-trackers),des [requêtes suivies](threat-trackers.md#tracked-queries) et des [requêtes enregistrées](threat-trackers.md#saved-queries).

- [Threat Explorer (ou détections en temps réel)](threat-explorer.md) (également appelé Explorer) est un rapport en temps réel qui vous permet d’identifier et d’analyser les menaces récentes. Vous pouvez configurer Explorer pour afficher des données pour les périodes personnalisées.

- [Simulateur d’attaques](attack-simulator.md) vous permet d’exécuter des scénarios d’attaques réalistes au sein de votre organisation afin d’identifier les vulnérabilités. Des simulations de types actuels d’attaques sont disponibles, notamment une [attaque par hameçonnage du nom d’affichage](attack-simulator.md#display-name-spear-phishing-attack), une [attaque par pulvérisation de mot de passe](attack-simulator.md#password-spray-attack), une [attaque de mot de passe par force brute](attack-simulator.md#brute-force-password-attack), et bien plus encore.
    
## <a name="save-time-with-automated-investigation-and-response"></a>Gagner du temps avec l’examen et la réponse automatisé

(**NOUVEAU !**) Lorsque vous effectuez des recherches sur une attaque potentielle de sécurité sur Internet, le temps est essentiel. Plus vous pourrez identifier et atténuer les menaces rapidement, mieux votre organisation se portera. Office 365 – Protection avancée contre les menaces Plan 2 inclut désormais des fonctionnalités d’[examen et de réponse automatisés](automated-investigation-response-office.md). (Si vous n’avez pas encore ces fonctionnalités, vous les aurez bientôt avec ATP Plan 2.)

Examen et réponse automatisés inclut un ensemble de règles de sécurité qui peuvent être lancées automatiquement, par exemple lorsqu’une alerte est déclenchée, ou manuellement, par exemple à partir d’un affichage dans Explorer. Examen et réponse automatisés permet à votre équipe des opérations de sécurité d’économiser du temps et des efforts pour atténuer les menaces efficacement. Pour en savoir plus, voir [Examen et réponse automatisés avec Office 365](automated-investigation-response-office.md).

## <a name="permissions-required-to-use-atp-features"></a>Autorisations requises pour utiliser les fonctionnalités ATP

Pour accéder aux fonctionnalités ATP dans le Centre de sécurité et conformité, vous devez disposer d’un rôle approprié. Le tableau ci-après inclut des exemples :

|Rôle ou groupe de rôles  |Ressources pour en savoir plus  |
|---------|---------|
|Administrateur général Office 365 |[À propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Administrateur de sécurité |[Autorisations des rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/fr-FR/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Gestion d’Organisation Exchange Online |[Autorisations dans Exchange Online](https://docs.microsoft.com/fr-FR/exchange/permissions-exo/permissions-exo) <br>et<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Pour plus d’informations, voir :

- [Autorisations dans le centre de conformité et de sécurité](permissions-in-the-security-and-compliance-center.md) 

- [Octroi de l’accès au Centre de conformité et de sécurité aux utilisateurs](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Obtenir Office 365 – Protection avancée contre les menaces

Office 365 – Protection avancée contre les menaces Plan 2 est inclus dans Office 365 Entreprise E5, Office 365 Éducation A5 et Microsoft 365 Entreprise. Si votre abonnement n’inclut pas Office 365 – Protection avancée contre les menaces, vous pouvez acheter ATP Plan 1 ou ATP Plan 2 en tant que composant additionnel de certains abonnements. Pour en savoir plus, consultez les ressources suivantes :

- Consultez [Disponibilité d’Office 365 – Protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) pour une liste des abonnements qui incluent les plants ATP.

- Consultez [Disponibilité des fonctionnalités pour les différents plans Protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) pour une liste des fonctionnalités incluses dans Plan 1 et 2.

- Consultez [Obtenir la bonne version d’Office 365 – Protection avancée contre les menaces](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) pour comparer les plans et acheter Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Nouvelles fonctionnalités d’Office 365 – Protection avancée contre les menaces

Les nouvelles fonctionnalités sont ajoutées à Office 365 – Protection avancée contre les menaces en continu. Pour en savoir plus, consultez les ressources suivantes :

- La [feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) fournit une liste des nouvelles fonctionnalités de développement et de déploiement.

- La [description du service Office 365 – Protection avancée contre les menaces](https://docs.microsoft.com/fr-FR/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) décrit les fonctionnalités et la disponibilité des plans ATP.
