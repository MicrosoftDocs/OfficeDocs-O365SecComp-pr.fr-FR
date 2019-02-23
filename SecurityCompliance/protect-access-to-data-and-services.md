---
title: Protéger l’accès aux données et services dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Page d'accueil pour la protection de l'accès aux données et services O365
ms.openlocfilehash: 95933c5a7bc95f9fd70e8f3470055b57193971d4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213534"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Protéger l’accès aux données et services dans Office 365

La protection de l'accès à vos données et services Office 365 est cruciale pour la défense contre les attaques informatiques et la protection contre la perte de données. Les mêmes protections peuvent être appliquées à d'autres applications SaaS dans votre environnement et même aux applications locales publiées avec le proxy d'application Azure Active Directory.
  
## <a name="step-1-review-recommendations"></a>Étape 1: passer en revue les recommandations

Découvrez les fonctionnalités recommandées relatives à la protection des identités et des appareils qui accèdent à Office 365, aux autres services SaaS et applications locales publiées avec le proxy d’application Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Étape 2: configuration de l'authentification multiFACTEUR

Utilisez ces ressources pour vous orienter vers la MFA, déterminer la version appropriée pour vous, planifier et déployer l'authentification multiFACTEUR pour votre environnement.
  
- [Qu'est-ce que Azure Multi-Factor Authentication?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Choisir la solution d'authentification multifacteur Azure pour vous](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Comment obtenir l'authentification multifacteur Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Planifier l'authentification multifacteur pour les déploiements d'Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planifier l'emplacement de déploiement de MFA, Cloud ou local](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Configurer les paramètres d'authentification multifacteur Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Étape 3: appliquer l'authentification multiFACTEUR avec les règles d'accès conditionnel Azure AD

Si vous utilisez Azure AD MFA, créez une règle d'accès conditionnel pour exiger l'authentification MFA pour l'accès à Office 365 et d'autres applications SaaS dans votre environnement.
  
- [Accès conditionnel dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Étape 4: configurer la gestion des accès privilégiés

La gestion des accès privilégiés permet le contrôle d'accès granulaire sur les tâches d'administration privilégiée dans Office 365.  Elle peut aider à protéger votre organisation contre les violations susceptibles d'utiliser des comptes d'administrateur privilégié existants avec un accès permanent aux données sensibles ou un accès aux paramètres de configuration critiques.

- [Vue d'ensemble de la gestion des accès privilégiés](privileged-access-management-overview.md)
- [Configurer la gestion des accès privilégiés](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Étape 5: configurer des stratégies d'accès aux appareils SharePoint

Les stratégies d'accès aux appareils pour SharePoint Online et OneDrive entreprise sont recommandées pour la protection des données sensibles, classifiées et réglementées. Bientôt disponible est la possibilité d'appliquer des stratégies d'accès aux appareils à des sites d'équipe individuels.
  
- [Contrôler l’accès depuis des appareils enregistrés](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Étape 6: configuration de l'application et de la protection des données pour les appareils

Vous pouvez gérer des applications sur des appareils mobiles, que les appareils soient ou non déployés pour la gestion des appareils mobiles. Cela protège contre les fuites accidentelles de données dans Office 365, y compris la messagerie et les fichiers.
  
- Pour iOS et Android: [protéger les données d'application à l'aide de stratégies de protection des applications avec Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Pour Windows 10, configurez la protection des informations Windows (WIP) pour éviter les fuites accidentelles de données.
  
- Pour les appareils gérés: [créer une protection des informations Windows avec la stratégie d'enregistrement à l'aide du portail Azure pour Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Pour les appareils non gérés: [création et déploiement d'une stratégie de protection des applications pour la protection des informations Windows (WIP) avec Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Étape 7: gérer les appareils avec Intune

La gestion des appareils vous permet de vous assurer qu'ils sont intègres et conformes avant de leur accorder l'accès à des ressources dans votre environnement. Les règles d'accès conditionnel basées sur les appareils permettent de s'assurer que les attaquants ne peuvent pas accéder à vos ressources à partir d'appareils non gérés.
  
- [Inscrire des appareils pour la gestion dans Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Étape 8: configurer des stratégies Intune et des règles d'accès conditionnels supplémentaires pour votre environnement

Utilisez ces configurations recommandées comme point de départ pour les scénarios de sécurité d'accès à l'entreprise ou avancés.
  
- [Stratégies et configurations de messagerie sécurisées](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

