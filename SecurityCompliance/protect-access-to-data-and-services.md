---
title: Protéger l’accès aux données et services dans Office 365
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
ms.openlocfilehash: e6e2d8d3ba6482d4b80593bd9e09d49d6120af80
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528362"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="3bbf0-103">Protéger l’accès aux données et services dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3bbf0-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="3bbf0-p101">Protection de l’accès à vos données d’Office 365 et des services est essentielle pour la défense contre les attaques informatiques et de protection contre la perte de données. Les mêmes protections peuvent être appliquées à d’autres applications SaaS dans votre environnement et même à des applications sur site publié avec un Proxy d’Application Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="3bbf0-106">Étape 1 : Revoir les recommandations</span><span class="sxs-lookup"><span data-stu-id="3bbf0-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="3bbf0-107">Fonctionnalités recommandées pour la protection des identités et des appareils qui accèdent à Office 365, autres services SaaS et applications locales publiées avec le proxy de d’application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="3bbf0-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Plus de langues](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="3bbf0-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="3bbf0-109">Étape 2 : Configurer MFA</span><span class="sxs-lookup"><span data-stu-id="3bbf0-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="3bbf0-110">Utilisez ces ressources pour orienter à MFA, décider quelle version vous convient, puis planifier et déployer MFA pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="3bbf0-111">Quel est l’authentification multifacteur Azure ?</span><span class="sxs-lookup"><span data-stu-id="3bbf0-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="3bbf0-112">Choisir la solution d’authentification multifacteur Azure pour vous</span><span class="sxs-lookup"><span data-stu-id="3bbf0-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="3bbf0-113">Comment obtenir l’authentification multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="3bbf0-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="3bbf0-114">Planifier l’authentification multifacteur pour les déploiements Office 365</span><span class="sxs-lookup"><span data-stu-id="3bbf0-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="3bbf0-115">Configurer l’authentification multifacteur pour les utilisateurs Office 365</span><span class="sxs-lookup"><span data-stu-id="3bbf0-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="3bbf0-116">Planifier l’emplacement de déploiement MFA, nuage ou sur site</span><span class="sxs-lookup"><span data-stu-id="3bbf0-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="3bbf0-117">Configurer les paramètres de l’authentification multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="3bbf0-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="3bbf0-118">Étape 3 : Appliquer MFA avec des règles d’accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="3bbf0-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="3bbf0-119">Si vous utilisez Azure AD MFA, créez une règle d’accès conditionnel pour exiger que MFA pour accéder à Office 365 et d’autres applications SaaS dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="3bbf0-120">Accès conditionnel dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3bbf0-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-sharepoint-device-access-policies"></a><span data-ttu-id="3bbf0-121">Étape 4 : Configurer des stratégies d’accès périphérique SharePoint</span><span class="sxs-lookup"><span data-stu-id="3bbf0-121">Step 4: Configure SharePoint device access policies</span></span>

<span data-ttu-id="3bbf0-p102">Stratégies d’accès de périphérique pour SharePoint Online et OneDrive entreprise sont recommandés pour la protection des données sensibles, confidentielles et régulées. Bientôt disponible est la possibilité d’appliquer des stratégies d’accès de périphérique à des sites d’équipe.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-p102">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="3bbf0-124">Contrôler l’accès depuis des appareils enregistrés</span><span class="sxs-lookup"><span data-stu-id="3bbf0-124">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-5-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="3bbf0-125">Étape 5 : Configurer l’application et protection des données pour les périphériques</span><span class="sxs-lookup"><span data-stu-id="3bbf0-125">Step 5: Configure app and data protection for devices</span></span>

<span data-ttu-id="3bbf0-p103">Vous pouvez gérer les applications sur les appareils mobiles indépendamment si les périphériques sont inscrits pour la gestion des appareils mobiles. Cela protège contre la perte accidentelle de données dans Office 365, notamment la messagerie et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-p103">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="3bbf0-128">Pour iOS et Android : [protéger les données d’application à l’aide de stratégies de protection des applications avec Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="3bbf0-128">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="3bbf0-129">Pour Windows 10, configurer la Protection des informations Windows (TEC) pour empêcher les fuites accidentelle de données.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-129">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="3bbf0-130">Pour des périphériques gérés : [créer une Protection d’informations Windows (TEC) avec la stratégie d’inscription de l’utilisation du portail pour Intune Microsoft Azure](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="3bbf0-130">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="3bbf0-131">Pour les périphériques non gérés : [créer et déployer une stratégie de protection d’application Windows informations Protection travaux avec Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="3bbf0-131">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-6-manage-devices-with-intune"></a><span data-ttu-id="3bbf0-132">Étape 6 : Gestion des périphériques avec Intune</span><span class="sxs-lookup"><span data-stu-id="3bbf0-132">Step 6: Manage devices with Intune</span></span>

<span data-ttu-id="3bbf0-p104">Gestion des appareils permettent de vous assurer qu’ils sont intègres et conformes avant de leur donner accès à des ressources dans votre environnement. Accès conditionnel règles garantir les pirates ne peuvent pas accéder à vos ressources à partir des périphériques non gérés en fonction de périphérique.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-p104">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="3bbf0-135">Inscrire des périphériques pour la gestion de Intune</span><span class="sxs-lookup"><span data-stu-id="3bbf0-135">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-7-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="3bbf0-136">Étape 7 : Configurer des stratégies Intune supplémentaires et les règles d’accès conditionnel pour votre environnement</span><span class="sxs-lookup"><span data-stu-id="3bbf0-136">Step 7: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="3bbf0-137">Utilisez ces configurations recommandées comme point de départ pour l’échelle de l’entreprise ou les scénarios de sécurité d’accès complexe.</span><span class="sxs-lookup"><span data-stu-id="3bbf0-137">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="3bbf0-138">Les configurations et les stratégies de messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="3bbf0-138">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

