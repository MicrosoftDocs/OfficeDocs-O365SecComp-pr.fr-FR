---
title: Pour protéger l’accès aux données et aux services dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: page d’accueil pour la protection de l’accès aux services et données O365
ms.openlocfilehash: 6ea617b1a7a7a34492689908d4816a851d58e776
ms.sourcegitcommit: 0ce722533d72fa8dcc1d8a58d3c649cb345b938d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2018
ms.locfileid: "24009100"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Pour protéger l’accès aux données et aux services dans Office 365

Protection de l’accès à vos données d’Office 365 et des services est essentielle pour la défense contre les attaques informatiques et de protection contre la perte de données. Les mêmes protections peuvent être appliquées à d’autres applications SaaS dans votre environnement et même à des applications sur site publié avec un Proxy d’Application Azure Active Directory.
  
## <a name="step-1-review-recommendations"></a>Étape 1 : Revoir les recommandations

Fonctionnalités recommandées pour la protection des identités et des appareils qui accèdent à Office 365, autres services SaaS et applications locales publiées avec le proxy de d’application Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Étape 2 : Configurer MFA

Utilisez ces ressources pour orienter à MFA, décider quelle version vous convient, puis planifier et déployer MFA pour votre environnement.
  
- [Quel est l’authentification multifacteur Azure ?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Choisir la solution d’authentification multifacteur Azure pour vous](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Comment obtenir l’authentification multifacteur Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Planifier l’authentification multifacteur pour les déploiements Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurer l’authentification multifacteur pour les utilisateurs Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planifier l’emplacement de déploiement MFA, nuage ou sur site](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Configurer les paramètres de l’authentification multifacteur Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Étape 3 : Appliquer MFA avec des règles d’accès conditionnel Azure AD

Si vous utilisez Azure AD MFA, créez une règle d’accès conditionnel pour exiger que MFA pour accéder à Office 365 et d’autres applications SaaS dans votre environnement.
  
- [Accès conditionnel dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Étape 4 : Configurer la gestion des accès privilégié

Un accès privilégié gestion permet de contrôle d’accès granulaire sur les tâches d’administration privilégié dans Office 365.  Il permet de protéger votre organisation contre les violations qui peuvent utiliser des comptes d’administration privilégié existants avec accès permanent à des données sensibles ou l’accès aux paramètres de configuration critique.

- [Vue d’ensemble des privilèges accéder à la gestion](privileged-access-managment-overview.md)
- [Configurer la gestion des accès privilégié](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Étape 5 : Configurez les stratégies d’accès de périphérique de SharePoint

Stratégies d’accès de périphérique pour SharePoint Online et OneDrive entreprise sont recommandés pour la protection des données sensibles, confidentielles et régulées. Bientôt disponible est la possibilité d’appliquer des stratégies d’accès de périphérique à des sites d’équipe.
  
- [Contrôler l’accès depuis des appareils enregistrés](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Étape 6 : Configurer l’application et protection des données pour les périphériques

Vous pouvez gérer les applications sur les appareils mobiles indépendamment si les périphériques sont inscrits pour la gestion des appareils mobiles. Cela protège contre la perte accidentelle de données dans Office 365, notamment la messagerie et les fichiers.
  
- Pour iOS et Android : [protéger les données d’application à l’aide de stratégies de protection des applications avec Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Pour Windows 10, configurer la Protection des informations Windows (TEC) pour empêcher les fuites accidentelle de données.
  
- Pour des périphériques gérés : [créer une Protection d’informations Windows (TEC) avec la stratégie d’inscription de l’utilisation du portail pour Intune Microsoft Azure](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Pour les périphériques non gérés : [créer et déployer une stratégie de protection d’application Windows informations Protection travaux avec Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Étape 7 : Gestion des périphériques avec Intune

Gestion des appareils permettent de vous assurer qu’ils sont intègres et conformes avant de leur donner accès à des ressources dans votre environnement. Accès conditionnel règles garantir les pirates ne peuvent pas accéder à vos ressources à partir des périphériques non gérés en fonction de périphérique.
  
- [Inscrire des périphériques pour la gestion de Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Étape 8 : Configurer des stratégies Intune supplémentaires et les règles d’accès conditionnel pour votre environnement

Utilisez ces configurations recommandées comme point de départ pour l’échelle de l’entreprise ou les scénarios de sécurité d’accès complexe.
  
- [Les configurations et les stratégies de messagerie sécurisée](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

