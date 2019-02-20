---
title: Stratégies d'accès dans Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Office 365 Cloud App les stratégies d'accès de sécurité activent la surveillance en temps réel et le contrôle de l'accès aux applications Cloud en fonction de l'utilisateur, de l'emplacement, du périphérique et de l'application. Vous pouvez créer des stratégies d'accès pour n'importe quel appareil, y compris des appareils qui ne sont pas joints à un domaine, et qui ne sont pas gérés par Windows Intune en déployant des certificats clients sur des appareils gérés ou à l'aide de certificats existants, tels que des certificats MDM tiers. Par exemple, vous pouvez déployer des certificats clients sur des appareils gérés, puis bloquer l'accès à partir d'appareils sans certificat.
ms.openlocfilehash: bb4404793647c65ab8addc148e6efe24242f3079
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103309"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a><span data-ttu-id="87842-105">Stratégies d'accès dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="87842-105">Access policies in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="87842-106">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="87842-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="87842-107">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="87842-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="87842-108">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="87842-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="87842-109">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="87842-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="87842-110">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="87842-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="87842-111">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="87842-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="87842-112">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="87842-112">You are here!</span></span>  <br/> [<span data-ttu-id="87842-113">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="87842-113">Next step</span></span>](group-your-ip-addresses-in-ocas.md) <br/> |[<span data-ttu-id="87842-114">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="87842-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="87842-p102">Office 365 Cloud App les stratégies d'accès de sécurité activent la surveillance en temps réel et le contrôle de l'accès aux applications Cloud en fonction de l'utilisateur, de l'emplacement, du périphérique et de l'application. Vous pouvez créer des stratégies d'accès pour n'importe quel appareil, y compris des appareils qui ne sont pas joints à un domaine, et qui ne sont pas gérés par Windows Intune en déployant des certificats clients sur des appareils gérés ou à l'aide de certificats existants, tels que des certificats MDM tiers. Par exemple, vous pouvez déployer des certificats clients sur des appareils gérés, puis bloquer l'accès à partir d'appareils sans certificat.</span><span class="sxs-lookup"><span data-stu-id="87842-p102">Office 365 Cloud App Security access policies enable real-time monitoring and control over access to cloud apps based on user, location, device, and app. You can create access policies for any device, including devices that aren't domain joined, and not managed by Windows Intune by rolling out client certificates to managed devices or by using existing certificates, such as third-party MDM certificates. For example, you can deploy client certificates to managed devices, and then block access from devices without a certificate.</span></span>

<span data-ttu-id="87842-118">Au lieu d'autoriser ou de bloquer entièrement l'accès, avec des [stratégies](ocas-session-policies.md) de session, vous pouvez autoriser l'accès tout en surveillant la session et/ou en limitant les activités de session spécifiques.</span><span class="sxs-lookup"><span data-stu-id="87842-118">Instead of allowing or blocking access completely, with [session policies](ocas-session-policies.md) you can allow access while monitoring the session and/or limit specific session activities.</span></span>

## <a name="prerequisites-to-using-access-policies"></a><span data-ttu-id="87842-119">Conditions préalables à l'utilisation des stratégies d'accès</span><span class="sxs-lookup"><span data-stu-id="87842-119">Prerequisites to using access policies</span></span>

- <span data-ttu-id="87842-120">Licence Azure AD Premium P1</span><span class="sxs-lookup"><span data-stu-id="87842-120">Azure AD Premium P1 license</span></span>

- <span data-ttu-id="87842-121">Les applications appropriées doivent être [déployées avec le contrôle d'application d'accès conditionnel](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span><span class="sxs-lookup"><span data-stu-id="87842-121">The relevant apps should be [deployed with Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span></span>

- <span data-ttu-id="87842-122"> une [stratégie d'accès conditionnel Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)doit être mise en place pour rediriger les utilisateurs vers Office 365 Cloud App Security, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="87842-122">An [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) should be in place that redirects users to Office 365 Cloud App Security, as described below.</span></span>

## <a name="create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="87842-123">Créer une stratégie d'accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="87842-123">Create an Azure AD conditional access policy</span></span>

<span data-ttu-id="87842-p103">Les stratégies d'accès conditionnel Azure Active Directory et les stratégies de session de sécurité des applications Cloud fonctionnent en tandem pour examiner chaque session utilisateur et prendre des décisions de stratégie pour chaque application. Pour configurer une stratégie d'accès conditionnel dans Azure AD, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="87842-p103">Azure Active Directory conditional access policies and Cloud App Security session policies work in tandem to examine each user session and make policy decisions for each app. To set up a conditional access policy in Azure AD, follow this procedure:</span></span>

1. <span data-ttu-id="87842-126">Configurez une  [stratégie d'accès conditionnel Azure ad](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)avec des affectations pour un utilisateur ou un groupe d'utilisateurs et l'application que vous souhaitez contrôler avec un contrôle d'application d'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="87842-126">Configure an [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) with assignments for user or group of users and the app you want to control with Conditional Access App Control.</span></span><br><span data-ttu-id="87842-127">Remarque: seules les applications qui ont été déployées  [avec le contrôle d'application d'accès conditionnel](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad)seront affectées par cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="87842-127">NOTE: Only apps that were [deployed with Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) will be affected by this policy.</span></span>

2. <span data-ttu-id="87842-128">acheminer les utilisateurs vers Office 365 Cloud app Security en sélectionnant les  **restrictions utiliser le contrôle d'application d'accès conditionnel**sous **Session**.</span><span class="sxs-lookup"><span data-stu-id="87842-128">Route users to Office 365 Cloud App Security by selecting the **Use Conditional Access App Control enforced restrictions** under **Session**.</span></span>

## <a name="create-a-cloud-app-security-access-policy"></a><span data-ttu-id="87842-129">Créer une stratégie d'accès de sécurité d'application Cloud</span><span class="sxs-lookup"><span data-stu-id="87842-129">Create a Cloud App Security access policy</span></span>

<span data-ttu-id="87842-130">Pour créer une stratégie d'accès, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="87842-130">To create a new access policy, follow this procedure:</span></span>

1. <span data-ttu-id="87842-131">Dans le portail, sélectionnez **contrôle** suivi de **stratégies**.</span><span class="sxs-lookup"><span data-stu-id="87842-131">In the portal, select **Control** followed by **Policies**.</span></span>

2. <span data-ttu-id="87842-132">Dans la page **stratégies** , cliquez sur **créer une stratégie** , puis sélectionnez **stratégie d'accès**.</span><span class="sxs-lookup"><span data-stu-id="87842-132">In the **Policies** page, click **Create policy** and select **Access policy**.</span></span>

3. <span data-ttu-id="87842-133">Dans la fenêtre **stratégie** d'accès, attribuez un nom à votre stratégie, par exemple *bloquer l'accès à partir d'appareils non gérés*.</span><span class="sxs-lookup"><span data-stu-id="87842-133">In the **Access policy** window, assign a name for your policy, such as *Block access from unmanaged devices*.</span></span>

4. <span data-ttu-id="87842-p104">Dans les **activités correspondant à toutes les sections suivantes** , sous **source d'activité**, sélectionnez filtres d'activité supplémentaires à appliquer à la stratégie. Les filtres incluent les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="87842-p104">In the **Activities matching all of the following** section, Under **Activity source**, select additional activity filters to apply to the policy. Filters include the following options:</span></span>
    
    - <span data-ttu-id="87842-136">**Balises de périphérique**: utilisez ce filtre pour identifier les appareils non gérés.</span><span class="sxs-lookup"><span data-stu-id="87842-136">**Device tags**: Use this filter to identify unmanaged devices.</span></span>
    
    - <span data-ttu-id="87842-137">**Emplacement**: utilisez ce filtre pour identifier les emplacements inconnus (et par conséquent).</span><span class="sxs-lookup"><span data-stu-id="87842-137">**Location**: Use this filter to identify unknown (and therefore risky) locations.</span></span>
    
    - <span data-ttu-id="87842-138">**Adresse IP**: utilisez ce filtre pour filtrer par adresse IP ou utiliser les balises d'adresses IP précédemment attribuées.</span><span class="sxs-lookup"><span data-stu-id="87842-138">**IP address**: Use this filter to filter per IP addresses or use previously assigned IP address tags.</span></span>
    
    - <span data-ttu-id="87842-p105">**Balise de l'agent utilisateur**: utilisez ce filtre pour activer l'heuristique afin d'identifier les applications mobiles et de bureau. Ce filtre peut être défini sur égal ou différent de. Les valeurs doivent être testées par rapport à vos applications mobiles et de bureau pour chaque application Cloud.</span><span class="sxs-lookup"><span data-stu-id="87842-p105">**User agent tag**: Use this filter to enable the heuristic to identify mobile and desktop apps. This filter can be set to equals or does not equal. The values should be tested against your mobile and desktop apps for each cloud app.</span></span>

5. <span data-ttu-id="87842-142">Sous **actions**, sélectionnez l'une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="87842-142">Under **Actions**, select one of the following options:</span></span>
    
    - <span data-ttu-id="87842-143">**Autoriser**: définissez cette action pour autoriser l'accès de manière explicite en fonction des filtres de stratégie que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="87842-143">**Allow**: Set this action to explicitly allow access according to the policy filters you set.</span></span>
    
    - <span data-ttu-id="87842-144">**Bloquer**: définissez cette action pour bloquer explicitement l'accès en fonction des filtres de stratégie que vous avez définis.</span><span class="sxs-lookup"><span data-stu-id="87842-144">**Block**: Set this action to explicitly block access according to the policy filters you set.</span></span>

6. <span data-ttu-id="87842-145">Vous pouvez **créer une alerte pour chaque événement correspondant à l'aide de la gravité de la stratégie**et définir une limite d'alerte, puis indiquer si vous souhaitez l'alerte sous forme de message électronique, de texte ou les deux.</span><span class="sxs-lookup"><span data-stu-id="87842-145">You can **Create an alert for each matching event with the policy's severity** and set an alert limit and select whether you want the alert as an email, a text message or both.</span></span>

## <a name="next-steps"></a><span data-ttu-id="87842-146">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="87842-146">Next steps</span></span>

- [<span data-ttu-id="87842-147">Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="87842-147">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)