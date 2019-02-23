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
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="74834-103">Protéger l’accès aux données et services dans Office 365</span><span class="sxs-lookup"><span data-stu-id="74834-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="74834-p101">La protection de l'accès à vos données et services Office 365 est cruciale pour la défense contre les attaques informatiques et la protection contre la perte de données. Les mêmes protections peuvent être appliquées à d'autres applications SaaS dans votre environnement et même aux applications locales publiées avec le proxy d'application Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74834-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="74834-106">Étape 1: passer en revue les recommandations</span><span class="sxs-lookup"><span data-stu-id="74834-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="74834-107">Découvrez les fonctionnalités recommandées relatives à la protection des identités et des appareils qui accèdent à Office 365, aux autres services SaaS et applications locales publiées avec le proxy d’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="74834-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="74834-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="74834-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="74834-109">Étape 2: configuration de l'authentification multiFACTEUR</span><span class="sxs-lookup"><span data-stu-id="74834-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="74834-110">Utilisez ces ressources pour vous orienter vers la MFA, déterminer la version appropriée pour vous, planifier et déployer l'authentification multiFACTEUR pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="74834-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="74834-111">Qu'est-ce que Azure Multi-Factor Authentication?</span><span class="sxs-lookup"><span data-stu-id="74834-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="74834-112">Choisir la solution d'authentification multifacteur Azure pour vous</span><span class="sxs-lookup"><span data-stu-id="74834-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="74834-113">Comment obtenir l'authentification multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="74834-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="74834-114">Planifier l'authentification multifacteur pour les déploiements d'Office 365</span><span class="sxs-lookup"><span data-stu-id="74834-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="74834-115">Configurer l’authentification multifacteur pour les utilisateurs d’Office 365</span><span class="sxs-lookup"><span data-stu-id="74834-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="74834-116">Planifier l'emplacement de déploiement de MFA, Cloud ou local</span><span class="sxs-lookup"><span data-stu-id="74834-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="74834-117">Configurer les paramètres d'authentification multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="74834-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="74834-118">Étape 3: appliquer l'authentification multiFACTEUR avec les règles d'accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="74834-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="74834-119">Si vous utilisez Azure AD MFA, créez une règle d'accès conditionnel pour exiger l'authentification MFA pour l'accès à Office 365 et d'autres applications SaaS dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="74834-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="74834-120">Accès conditionnel dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="74834-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="74834-121">Étape 4: configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="74834-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="74834-p102">La gestion des accès privilégiés permet le contrôle d'accès granulaire sur les tâches d'administration privilégiée dans Office 365.  Elle peut aider à protéger votre organisation contre les violations susceptibles d'utiliser des comptes d'administrateur privilégié existants avec un accès permanent aux données sensibles ou un accès aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="74834-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="74834-124">Vue d'ensemble de la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="74834-124">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="74834-125">Configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="74834-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="74834-126">Étape 5: configurer des stratégies d'accès aux appareils SharePoint</span><span class="sxs-lookup"><span data-stu-id="74834-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="74834-p103">Les stratégies d'accès aux appareils pour SharePoint Online et OneDrive entreprise sont recommandées pour la protection des données sensibles, classifiées et réglementées. Bientôt disponible est la possibilité d'appliquer des stratégies d'accès aux appareils à des sites d'équipe individuels.</span><span class="sxs-lookup"><span data-stu-id="74834-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="74834-129">Contrôler l’accès depuis des appareils enregistrés</span><span class="sxs-lookup"><span data-stu-id="74834-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="74834-130">Étape 6: configuration de l'application et de la protection des données pour les appareils</span><span class="sxs-lookup"><span data-stu-id="74834-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="74834-p104">Vous pouvez gérer des applications sur des appareils mobiles, que les appareils soient ou non déployés pour la gestion des appareils mobiles. Cela protège contre les fuites accidentelles de données dans Office 365, y compris la messagerie et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="74834-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="74834-133">Pour iOS et Android: [protéger les données d'application à l'aide de stratégies de protection des applications avec Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="74834-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="74834-134">Pour Windows 10, configurez la protection des informations Windows (WIP) pour éviter les fuites accidentelles de données.</span><span class="sxs-lookup"><span data-stu-id="74834-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="74834-135">Pour les appareils gérés: [créer une protection des informations Windows avec la stratégie d'enregistrement à l'aide du portail Azure pour Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="74834-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="74834-136">Pour les appareils non gérés: [création et déploiement d'une stratégie de protection des applications pour la protection des informations Windows (WIP) avec Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="74834-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="74834-137">Étape 7: gérer les appareils avec Intune</span><span class="sxs-lookup"><span data-stu-id="74834-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="74834-p105">La gestion des appareils vous permet de vous assurer qu'ils sont intègres et conformes avant de leur accorder l'accès à des ressources dans votre environnement. Les règles d'accès conditionnel basées sur les appareils permettent de s'assurer que les attaquants ne peuvent pas accéder à vos ressources à partir d'appareils non gérés.</span><span class="sxs-lookup"><span data-stu-id="74834-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="74834-140">Inscrire des appareils pour la gestion dans Intune</span><span class="sxs-lookup"><span data-stu-id="74834-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="74834-141">Étape 8: configurer des stratégies Intune et des règles d'accès conditionnels supplémentaires pour votre environnement</span><span class="sxs-lookup"><span data-stu-id="74834-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="74834-142">Utilisez ces configurations recommandées comme point de départ pour les scénarios de sécurité d'accès à l'entreprise ou avancés.</span><span class="sxs-lookup"><span data-stu-id="74834-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="74834-143">Stratégies et configurations de messagerie sécurisées</span><span class="sxs-lookup"><span data-stu-id="74834-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

