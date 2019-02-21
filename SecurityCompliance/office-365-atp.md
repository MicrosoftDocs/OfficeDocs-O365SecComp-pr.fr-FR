---
title: Office 365 - Protection avancée contre les menaces
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/20/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection inclut des pièces jointes sûres, des liens fiables, des outils anti-hameçonnage avancés, des outils de création de rapports et des fonctionnalités d'aide à la décision.
ms.openlocfilehash: 5db4c5ff5ae7e536bba1f8730c724d151f367b54
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123925"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 - Protection avancée contre les menaces

> [!IMPORTANT]
> Cet article est destiné aux clients Office 365 entreprise. Si vous utilisez Outlook.com, Office 365 Home ou Office 365 Personal, et que vous recherchez des informations sur les liens fiables dans Outlook, consultez [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Vue d'ensemble

Office 365 Advanced Threat Protection (ATP) protège votre organisation contre les menaces malveillantes posées par les messages électroniques, les liens (URL) et les outils de collaboration. La protection avancée contre les menaces inclut:

- [Stratégies de protection contre les menaces](#configure-atp-policies): définissez des stratégies de protection contre les menaces pour définir le niveau de protection approprié pour votre organisation. 

- [Rapports](#view-atp-reports): afficher des rapports en temps réel pour surveiller les performances ATP de votre organisation. 

- [Fonctionnalités](#utilize-threat-intelligence-capabilities)d'aide à la décision: utiliser des outils de pointe pour examiner, comprendre, simuler et prévenir les menaces. 
 

## <a name="configure-atp-policies"></a>Configurer des stratégies ATP

Office 365 ATP fournit de nombreux outils permettant de définir un niveau de protection approprié pour votre organisation. 

L'équipe de sécurité de votre organisation doit définir des stratégies pour chaque outil ATP dans le centre de sécurité & conformité Office 365. Accédez à la**stratégie** de **gestion** > des menaces pour accéder aux options de stratégie. 

Les stratégies définies pour votre organisation déterminent le comportement et le niveau de protection des menaces prédéfinies. Les options de stratégie sont extrêmement flexibles. Par exemple, l'équipe de sécurité de votre organisation peut définir une protection affinée contre les menaces au niveau des utilisateurs, des organisations, des destinataires et des domaines. Il est important de revoir vos stratégies régulièrement, car les nouvelles menaces et les nouveaux défis apparaissent quotidiennement.  

- [Pièces jointEs sécurisées](atp-safe-attachments.md)pour la protection avancée contre les menaces: permet de protéger votre système de messagerie en vérifiant les pièces jointes de courrier électronique. Il achemine tous les messages et les pièces jointes qui n'ont pas de signature de virus/programme malveillant dans un environnement spécial, puis utilise des techniques d'analyse et d'analyse de machine pour détecter les intentions malveillantes. Si aucune activité suspecte n'est trouvée, le message est transféré vers la boîte aux lettres. Pour en savoir plus, consultez la rubrique [configurer des stratégies de pièces jointEs approuvéEs pour Office 365 ATP](set-up-atp-safe-attachments-policies.md).

- [Liens fiables ATP](atp-safe-links.md): permet de vérifier les URL dans les messages électroniques et les fichiers Office avec un temps de clic. La protection est continue et s'applique à votre environnement de messagerie et de bureau. Les liens sont analysés pour chaque clic: les liens fiables restent accessibles et les liens malveillants sont bloqués de manière dynamique. Pour plus d'informations, reportez-vous à la rubrique [set up Office 365 ATP Safe Links Policies](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md): protège votre organisation quand les utilisateurs collaborent et partagent des fichiers en identifiant et en bloquant les fichiers malveillants dans les sites d'équipe et les bibliothèques de documents. Pour plus d'informations, reportez-vous à [activer l'ATP Office 365 pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [Protection contre le hameçonnage (ATP)](atp-anti-phishing.md): détecte les tentatives d'emprunt d'identité de vos utilisateurs et domaines personnalisés. Il applique des modèles d'apprentissage automatique et des algorithmes de détection d'usurpation d'identité avancés aux attaques de hameçonnage AVERT. Pour en savoir plus, consultez la rubrique [configurer les stratégies anti-hameçonnage et anti-hameçonnage d'Office 365 ATP](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Afficher les rapports ATP

La protection avancée contre les menaces Office 365 inclut un [tableau de bord de rapports](view-reports-for-atp.md) avancé pour surveiller vos performances ATP. Vous pouvez y accéder via le **tableau de bord rapports >** dans le centre de sécurité _AMP_ Compliance Center. 

La mise à jour des rapports en temps réel vous fournit les dernières informations. Ces rapports fournissent également des recommandations et vous signalent les menaces imminentes. Les rapports prédéfinis incluent le rapport d' [État de protection contre les menaces](view-reports-for-atp.md#threat-protection-status-report), le [rapport de types de fichiers ATP](view-reports-for-atp.md#atp-file-types-report), le [rapport de disposition de messages ATP](view-reports-for-atp.md#atp-message-disposition-report) , etc. 

## <a name="utilize-threat-intelligence-capabilities"></a>Utiliser les fonctionnalités d'aide à la décision

Office 365 ATP inclut des outils d'aide à la [décision](office-365-ti.md) qui permettent à l'équipe de sécurité de votre organisation d'anticiper, de comprendre et de prévenir les attaques malveillantes. 

- Les analyseurs de [menace](threat-trackers.md) fournissent la dernière intelligence sur les problèmes Cybersecurity en vigueur. Par exemple, vous pouvez afficher des informations sur le dernier programme malveillant et prendre des contre-mesures avant qu'il ne devienne une véritable menace pour votre organisation. Les suivis disponibles [](threat-trackers.md#noteworthy-trackers)incluent les suivis remarquables, les suivis des [tendances](threat-trackers.md#trending-trackers), les [requêtes suivies](threat-trackers.md#tracked-queries)et les [requêtes enregistrées](threat-trackers.md#saved-queries).

- [Explorateur](use-explorer-in-security-and-compliance.md) (également appelé «Explorateur de menaces») est un rapport en temps réel qui vous permet d'identifier et d'analyser les menaces récentes. Vous pouvez configurer l'Explorateur de sorte qu'il affiche les données pour les périodes personnalisées.

- Le simulateur d' [attaque](attack-simulator.md) vous permet d'exécuter des scénarios d'attaque réaliste dans votre organisation pour identifier les vulnérabilités. Les simulations des types d'attaques actuels sont disponibles, y compris une attaque [par hameçonnage de nom d'affichage](attack-simulator.md#display-name-spear-phishing-attack), une attaque [par pulvérisation](attack-simulator.md#password-spray-attack)de mot de passe, une [attaque de mot de passe en force](attack-simulator.md#brute-force-password-attack), et bien plus encore.
    
## <a name="permissions-required-to-use-atp-features"></a>Autorisations requises pour utiliser les fonctionnalités ATP

Pour accéder aux fonctionnalités ATP dans le centre de sécurité & conformité, vous devez disposer d'un rôle approprié. Le tableau suivant contient des exemples:

|Rôle ou groupe de rôles  |Ressources pour en savoir plus  |
|---------|---------|
|Administrateur général Office 365 |[À propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Administrateur de sécurité |[Autorisations de rôle d'administrateur dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Gestion de l'organisation Exchange Online |[Autorisations dans Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>et<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Voir aussi:
- [Autorisations dans le centre de sécurité & de sécurité Office 365](permissions-in-the-security-and-compliance-center.md) 

- [Donner aux utilisateurs l'accès au centre de sécurité & de sécurité Office 365](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Obtenir l'ATP Office 365

La protection avancée contre les menaces Office 365 est incluse dans Office 365 entreprise E5, Office 365 éducation a5 et Microsoft 365 Business. Si votre abonnement n'inclut pas l'ATP Office 365, vous pouvez acheter ATP en tant que module complémentaire. Pour en savoir plus, consultez les ressources suivantes:

- Consultez la rubrique disponibilité de la [protection avancée contre les menaces pour Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) pour obtenir la liste des abonnements incluant des plans ATP.

- Consultez la rubrique relative à la disponibilité des fonctionnalités dans les [offres de protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) pour obtenir la liste des fonctionnalités incluses dans les plans 1 et 2.

- Consultez [la rubrique obtenir la protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) pour comparer des offres et acheter Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Nouvelles fonctionnalités dans Office 365 ATP

De nouvelles fonctionnalités sont ajoutées à la protection avancée contre les menaces Office 365. Pour en savoir plus, consultez les ressources suivantes:

- La feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) fournit une liste des nouvelles fonctionnalités de développement et de déploiement.

- La [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) décrit les fonctionnalités et la disponibilité dans les plans ATP.
