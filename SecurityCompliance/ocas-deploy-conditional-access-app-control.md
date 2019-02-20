---
title: Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Procédez comme suit pour configurer les applications Azure AD Office 365 qui seront contrôlées par le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.
ms.openlocfilehash: ba3980615815fa45b1385a67560cc635506e2c22
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103289"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a><span data-ttu-id="cdc11-103">Déployer le contrôle d'application d'accès conditionnel pour les applications Office 365</span><span class="sxs-lookup"><span data-stu-id="cdc11-103">Deploy Conditional Access App Control for Office 365 apps</span></span>

|<span data-ttu-id="cdc11-104">Évaluation \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="cdc11-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="cdc11-105">Planification \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="cdc11-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="cdc11-106">Déploiement \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="cdc11-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="cdc11-107">Utilisation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cdc11-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cdc11-108">Commencer l'évaluation</span><span class="sxs-lookup"><span data-stu-id="cdc11-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="cdc11-109">Commencer la planification</span><span class="sxs-lookup"><span data-stu-id="cdc11-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="cdc11-110">Vous êtes là!</span><span class="sxs-lookup"><span data-stu-id="cdc11-110">You are here!</span></span>  <br/> [<span data-ttu-id="cdc11-111">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="cdc11-111">Next step</span></span>](ocas-session-policies.md) <br/> |[<span data-ttu-id="cdc11-112">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="cdc11-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="cdc11-113">Procédez comme suit pour configurer les applications Azure AD Office 365 qui seront contrôlées par le contrôle d'application d'accès conditionnel à Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="cdc11-113">Follow these steps to configure Azure AD Office 365 apps to be controlled by Office 365 Cloud App Security Conditional Access App Control.</span></span>

<span data-ttu-id="cdc11-114">**Étape 1: [créer une stratégie de test d'accès conditionnel Azure ad](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span><span class="sxs-lookup"><span data-stu-id="cdc11-114">**Step 1: [Create an Azure AD conditional access test policy](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span></span>

<span data-ttu-id="cdc11-115">**Étape 2: [se connecter avec un utilisateur étendu à la stratégie dans les applications](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span><span class="sxs-lookup"><span data-stu-id="cdc11-115">**Step 2: [Sign in with a user scoped to the policy in the apps](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span></span>

<span data-ttu-id="cdc11-116">**Étape 3: Si vous n'avez pas sélectionné de stratégie de sécurité d'application Cloud intégrée dans Azure AD ou si vous souhaitez appliquer la stratégie à une application non proposée, conFigurez les [contrôles avancés dans le portail de sécurité des applications Cloud](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal) .**</span><span class="sxs-lookup"><span data-stu-id="cdc11-116">**Step 3: If you did not select a built-in Cloud App Security policy in Azure AD or if you want to apply the policy to a non-featured app, [Configure advanced controls in the Cloud App Security portal](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span></span>

<span data-ttu-id="cdc11-117">**Étape 4: [tester le déploiement](#step-4-test-the-deployment)**</span><span class="sxs-lookup"><span data-stu-id="cdc11-117">**Step 4: [Test the deployment](#step-4-test-the-deployment)**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdc11-118">pour déployer le contrôle d'application d'accès conditionnel pour les applications office 365, vous avez besoin d'une [licence valide pour Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) , ainsi qu'une licence de sécurité d'application Cloud office 365.</span><span class="sxs-lookup"><span data-stu-id="cdc11-118">To deploy Conditional Access App Control for Office 365 apps, you need a valid [license for Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) as well as a Office 365 Cloud App Security license.</span></span>

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a><span data-ttu-id="cdc11-119">Étape 1: créer une stratégie de test d'accès conditionnel Azure AD</span><span class="sxs-lookup"><span data-stu-id="cdc11-119">Step 1: Create an Azure AD conditional access test policy</span></span> 

1. <span data-ttu-id="cdc11-120">Dans Azure Active Directory, sous **sécurité**, cliquez sur **accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="cdc11-120">In Azure Active Directory, under **Security**, click on **Conditional access**.</span></span>

2. <span data-ttu-id="cdc11-121">Cliquez sur **nouvelle stratégie** et créez une stratégie.</span><span class="sxs-lookup"><span data-stu-id="cdc11-121">Click **New policy** and create a new policy.</span></span>

3. <span data-ttu-id="cdc11-122">Dans la stratégie de TEST, sous **utilisateurs**, affectez un utilisateur ou un utilisateur test qui peut être utilisé pour une authentification et une vérification initiales.</span><span class="sxs-lookup"><span data-stu-id="cdc11-122">In the TEST policy, under **Users**, assign a test user or user that can be used for an initial sign-on and verification.</span></span>

4. <span data-ttu-id="cdc11-123">Dans la stratégie de TEST, sous **application Cloud**, affectez les applications que vous souhaitez contrôler avec le contrôle d'application d'accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="cdc11-123">In the TEST policy, under **Cloud app**, assign the apps you want to control with Conditional Access App Control.</span></span>

5. <span data-ttu-id="cdc11-p101">Sous **session**, définissez la stratégie pour qu'elle utilise l'une des stratégies intégrées, **analyse uniquement** ou **bloquer les téléchargements**. Ou sélectionnez **utiliser une stratégie** personnalisée pour définir une stratégie avancée dans le portail de sécurité des applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="cdc11-p101">Under **Session**, set the policy to use either of the built-in policies, **Monitor only** or **Block downloads**. Or select **Use custom policy** to set an advanced policy in the Cloud App Security portal.</span></span>

6. <span data-ttu-id="cdc11-126">Ajoutez les attributions de **condition**applicables ou les **contrôles** d'octroi (facultatif).</span><span class="sxs-lookup"><span data-stu-id="cdc11-126">Add any applicable **Condition assignments** or **Grant controls** (optional).</span></span>

> ![Accès conditionnel Azure AD](media/image1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a><span data-ttu-id="cdc11-128">Étape 2: se connecter avec un utilisateur étendu à la stratégie dans les applications</span><span class="sxs-lookup"><span data-stu-id="cdc11-128">Step 2: Sign in with a user scoped to the policy in the apps</span></span> 

<span data-ttu-id="cdc11-p102">Une fois que vous avez créé la stratégie, connectez-vous à chaque application configurée dans cette stratégie. Vérifiez que vous vous connectez à l'aide d'un utilisateur configuré dans la stratégie. Veillez à vous déconnecter d'abord des sessions existantes.</span><span class="sxs-lookup"><span data-stu-id="cdc11-p102">After you've created the policy, sign in to each app configured in that policy. Make sure you sign in using a user configured in the policy. Make sure to first sign out of existing sessions.</span></span>

<span data-ttu-id="cdc11-p103">La sécurité des applications Cloud synchronisera les détails de votre stratégie avec ses serveurs pour chaque nouvelle application à laquelle vous vous connectez. Cette opération peut prendre jusqu'à une minute.</span><span class="sxs-lookup"><span data-stu-id="cdc11-p103">Cloud App Security will sync your policy details to its servers for each new app you log in to. This may take up to one minute.</span></span>

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a><span data-ttu-id="cdc11-134">Étape 3: configurer des contrôles avancés dans le portail de sécurité des applications Cloud</span><span class="sxs-lookup"><span data-stu-id="cdc11-134">Step 3: Configure advanced controls in the Cloud App Security portal</span></span> 

<span data-ttu-id="cdc11-135">Les instructions ci-dessus vous ont permis de créer une stratégie de sécurité d'application Cloud intégrée pour les applications proposées directement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cdc11-135">The instructions above helped you create a built-in Cloud App Security policy for featured apps directly in Azure AD.</span></span>

<span data-ttu-id="cdc11-136">pour configurer une stratégie avancée, créez une stratégie d' [accès](ocas-access-policies.md) ou une [stratégie](ocas-session-policies.md) de session dans le portail de sécurité des applications Cloud Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdc11-136">To configure an advanced policy, create an [access policy](ocas-access-policies.md) or a [session policy](ocas-session-policies.md) in the Office 365 Cloud App Security portal.</span></span>

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a><span data-ttu-id="cdc11-137">Pour identifier les appareils utilisant des certificats clients (facultatif):</span><span class="sxs-lookup"><span data-stu-id="cdc11-137">To identify devices using client certificates (this is optional):</span></span>

1. <span data-ttu-id="cdc11-138">Accédez à l'COG paramètres, puis choisissez identification de l' **appareil**.</span><span class="sxs-lookup"><span data-stu-id="cdc11-138">Go to the settings cog and choose **Device identification**.</span></span>

2. <span data-ttu-id="cdc11-139">Téléchargez un ou plusieurs certificats racines ou intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="cdc11-139">Upload one or more root or intermediate certificates.</span></span>

3. <span data-ttu-id="cdc11-140">Une fois le certificat téléchargé, vous pouvez créer des stratégies d'accès et des stratégies de session basées sur la **baliSe Device** et le **certificat client valide**.</span><span class="sxs-lookup"><span data-stu-id="cdc11-140">After the certificate is uploaded, you can create access policies and session policies based on **Device tag** and **Valid client certificate**.</span></span>

![ID de périphérique de contrôle d'application d'accès conditionnel](media/image2.png)

> [!NOTE]
> <span data-ttu-id="cdc11-142">Un certificat est uniquement demandé à un utilisateur si la session correspond à une stratégie qui utilise le filtre de certificat client valide.</span><span class="sxs-lookup"><span data-stu-id="cdc11-142">A certificate is only requested from a user if the session matches a policy that uses the valid client certificate filter.</span></span>
> 
## <a name="step-4-test-the-deployment"></a><span data-ttu-id="cdc11-143">Étape 4: tester le déploiement</span><span class="sxs-lookup"><span data-stu-id="cdc11-143">Step 4: Test the deployment</span></span> 

1. <span data-ttu-id="cdc11-p104">Première déconnexion des sessions existantes. Ensuite, essayez de vous connecter à chaque application qui a été déployée avec succès. Connectez-vous à l'aide d'un utilisateur correspondant à la stratégie configurée dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cdc11-p104">First sign out of any existing sessions. Then, try to sign in to each app that was successfully deployed. Sign in using a user that matches the policy configured in Azure AD.</span></span>

2. <span data-ttu-id="cdc11-147">Dans le portail de sécurité des applications Cloud, sous **examiner**, sélectionnez **Journal d'activité**, puis assurez-vous que les activités de connexion sont capturées pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="cdc11-147">In the Cloud App Security portal, under **Investigate**, select **Activity log**, and make sure the login activities are captured for each app.</span></span>

3. <span data-ttu-id="cdc11-148">Vous pouvez filtrer en cliquant sur **avancé**, puis le filtrage à l'aide de la **source est égal à contrôle d'accès**.</span><span class="sxs-lookup"><span data-stu-id="cdc11-148">You can filter by clicking on **Advanced**, and then filtering using **Source equals Access control**.</span></span>

4. <span data-ttu-id="cdc11-p105">Il est recommandé de vous connecter à des applications mobiles et de bureau à partir d'appareils gérés et non gérés. Cela permet de s'assurer que les activités sont correctement capturées dans le journal d'activité. Pour vérifier que l'activité est correctement capturée, cliquez sur une activité d'ouverture de session unique pour qu'elle ouvre le tiroir d'activité. Assurez-vous que la balise de l' **agent utilisateur**reflète correctement si le périphérique est un client natif (c'est-à-dire une application mobile ou de bureau) ou si l'appareil est un appareil géré (conforme, joint à un domaine ou un certificat client valide).</span><span class="sxs-lookup"><span data-stu-id="cdc11-p105">It's recommended that you sign into mobile and desktop apps from managed and unmanaged devices. This is to make sure that the activities are properly captured in the activity log. To verify that the activity is properly captured, click on a single sign-on log on activity so that it opens the activity drawer. Make sure the **User agent tag** properly reflects whether the device is a native client (meaning either a mobile or desktop app) or the device is a managed device (compliant, domain joined, or valid client certificate).</span></span>

> [!NOTE]
> <span data-ttu-id="cdc11-p106">Une fois déployée, vous ne pouvez pas supprimer une application à partir de la page de contrôle d'application Access conditionnelle. Tant que vous ne définissez pas une session ou une stratégie d'accès sur l'application, le contrôle d'application d'accès conditionnel ne modifie aucun comportement pour l'application.</span><span class="sxs-lookup"><span data-stu-id="cdc11-p106">After it is deployed, you can't remove an app from the Conditional Access App Control page. As long as you don't set a session or access policy on the app, the Conditional Access App Control won't change any behavior for the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cdc11-155">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cdc11-155">Next steps</span></span>

- [<span data-ttu-id="cdc11-156">En savoir plus sur les stratégies de session dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cdc11-156">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="cdc11-157">En savoir plus sur les stratégies d'accès dans Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cdc11-157">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 

- [<span data-ttu-id="cdc11-158">Grouper vos adresses IP pour simplifier la gestion dans la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="cdc11-158">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)