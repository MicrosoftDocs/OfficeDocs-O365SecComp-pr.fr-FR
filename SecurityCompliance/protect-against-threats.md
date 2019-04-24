---
title: Se protéger contre les menaces dans Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Utilisez cet article pour configurer vos fonctionnalités de protection contre les menaces dès maintenant.
ms.openlocfilehash: 065071999130f209d63bcafc09ad72daceceac04
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261632"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="c4436-103">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="c4436-104">Office 365 inclut diverses fonctionnalités de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="c4436-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="c4436-105">Voici un guide de démarrage rapide que vous pouvez utiliser comme liste de vérification pour vous assurer que les fonctionnalités de protection contre les menaces sont configurées pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c4436-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="c4436-106">Si vous ne connaissez pas les fonctionnalités de protection contre les menaces dans Office 365, ou si vous n'êtes pas sûr de savoir où commencer, utilisez les instructions suivantes comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="c4436-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c4436-107">Les **paramètres recommandés initiaux sont inclus pour chaque type de stratégie; Toutefois, de nombreuses options sont disponibles et vous pouvez ajuster vos paramètres afin de répondre aux besoins spécifiques de votre organisation**.</span><span class="sxs-lookup"><span data-stu-id="c4436-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="c4436-108">Accordez environ 30 minutes à vos stratégies ou modifications pour qu'elles fonctionnent dans votre centre de centres de travail.</span><span class="sxs-lookup"><span data-stu-id="c4436-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4436-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4436-109">Requirements</span></span>

### <a name="licenses"></a><span data-ttu-id="c4436-110">Licences</span><span class="sxs-lookup"><span data-stu-id="c4436-110">Licenses</span></span>

<span data-ttu-id="c4436-111">Les fonctionnalités de protection contre les menaces sont incluses dans tous les abonnements Office 365; Toutefois, certains abonnements incluent des fonctionnalités plus avancées, telles que celles d'Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="c4436-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features, such as those in Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="c4436-112">Dans cet article, nous incluons les conditions d'abonnement requises pour chaque zone de protection.</span><span class="sxs-lookup"><span data-stu-id="c4436-112">In this article we include subscription requirements for each protection area.</span></span>

<span data-ttu-id="c4436-113">Pour en savoir plus sur les fonctionnalités de protection contre les menaces et subsriptions, consultez les ressources suivantes:</span><span class="sxs-lookup"><span data-stu-id="c4436-113">To learn more about threat protection features and subsriptions, see the following resources:</span></span>
- [<span data-ttu-id="c4436-114">Description du service Office 365 - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c4436-114">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
- [<span data-ttu-id="c4436-115">Description du service Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="c4436-115">Exchange Online Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-service-description)
- [<span data-ttu-id="c4436-116">Centre de sécurité et conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-116">Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)

### <a name="roles-and-permissions"></a><span data-ttu-id="c4436-117">Rôles et autorisations</span><span class="sxs-lookup"><span data-stu-id="c4436-117">Roles and permissions</span></span>

<span data-ttu-id="c4436-118">Vous devez disposer d'un rôle approprié pour configurer les stratégies dans le [Centre de sécurité _AMP_ Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span><span class="sxs-lookup"><span data-stu-id="c4436-118">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="c4436-119">Le tableau suivant contient des exemples:</span><span class="sxs-lookup"><span data-stu-id="c4436-119">The following table includes some examples:</span></span> 

|<span data-ttu-id="c4436-120">Rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="c4436-120">Role or role group</span></span>  |<span data-ttu-id="c4436-121">Où en savoir plus</span><span class="sxs-lookup"><span data-stu-id="c4436-121">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="c4436-122">Administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-122">Office 365 Global Administrator</span></span> |[<span data-ttu-id="c4436-123">À propos des rôles d'administrateur Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-123">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="c4436-124">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="c4436-124">Security Administrator</span></span> |[<span data-ttu-id="c4436-125">Autorisations de rôle d'administrateur dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c4436-125">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="c4436-126">Gestion de l'organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c4436-126">Exchange Online Organization Management</span></span> |[<span data-ttu-id="c4436-127">Autorisations dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c4436-127">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="c4436-128">et</span><span class="sxs-lookup"><span data-stu-id="c4436-128">and</span></span><br> [<span data-ttu-id="c4436-129">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4436-129">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="c4436-130">Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-130">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="c4436-131">Partie 1: anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="c4436-131">Part 1 - Anti-malware</span></span>

<span data-ttu-id="c4436-132">La [protection contre les programmes malveillants](anti-malware-protection.md) est disponible dans les abonnements qui incluent [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EoP).</span><span class="sxs-lookup"><span data-stu-id="c4436-132">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="c4436-133">Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre les programmes malveillants**pour la**stratégie** > de **gestion** > des menaces.</span><span class="sxs-lookup"><span data-stu-id="c4436-133">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="c4436-134">Double-cliquez sur la stratégie **par défaut** , puis sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="c4436-134">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="c4436-135">Spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-135">Specify the following settings:</span></span>
    
    - <span data-ttu-id="c4436-136">Dans la section réponse à la **détection de programmes malveillants** , conservez le paramètre par défaut **non**.</span><span class="sxs-lookup"><span data-stu-id="c4436-136">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
   
    - <span data-ttu-id="c4436-137">Dans la section **filtre de types de pièces jointEs courantes** , choisissez **activé**.</span><span class="sxs-lookup"><span data-stu-id="c4436-137">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="c4436-138">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-138">Click **Save**.</span></span>

<span data-ttu-id="c4436-139">Pour en savoir plus sur les options de stratégie anti-programme malveillant, consultez la rubrique [configure anti-malware Policies](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-139">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="c4436-140">Partie 2-protection Zero-Day</span><span class="sxs-lookup"><span data-stu-id="c4436-140">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="c4436-141">La protection «Zero-Day» est disponible dans les abonnements incluant [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP) et est configurée par le biais de [pièces jointEs approuvées ATP](atp-safe-attachments.md) et des stratégies de [liens fiables ATP](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="c4436-141">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="c4436-142">Stratégies de pièces jointes approuvées ATP</span><span class="sxs-lookup"><span data-stu-id="c4436-142">ATP Safe Attachments policies</span></span>

<span data-ttu-id="c4436-143">Pour configurer des [pièces jointEs sûres ATP](atp-safe-attachments.md), vous devez définir au moins une stratégie de pièces jointes approuvées ATP.</span><span class="sxs-lookup"><span data-stu-id="c4436-143">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="c4436-144">Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), choisissez protection\*\*\*\* > **contre les** **menaces** > pièces jointes ATP.</span><span class="sxs-lookup"><span data-stu-id="c4436-144">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="c4436-145">Sélectionnez l'option Activer la protection avancée contre **les menaces pour SharePoint, OneDrive et Microsoft teams**.</span><span class="sxs-lookup"><span data-stu-id="c4436-145">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="c4436-146">Dans la section **protéger les pièces jointes** , cliquez sur le**+** signe plus ().</span><span class="sxs-lookup"><span data-stu-id="c4436-146">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="c4436-147">Spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-147">Specify the following settings:</span></span>

    - <span data-ttu-id="c4436-148">Dans la zone **nom** , tapez `Block malware`.</span><span class="sxs-lookup"><span data-stu-id="c4436-148">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="c4436-149">Dans la section réponse, sélectionnez **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-149">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="c4436-150">Dans la section **pièce jointe** de redirection, sélectionnez l'option Activer la redirection, puis spécifiez l'adresse de messagerie de l'administrateur ou de l'opérateur de sécurité de votre organisation qui analysera les fichiers détectés. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c4436-150">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="c4436-151">Dans la section **appliqué à** , choisissez **le domaine du destinataire**.</span><span class="sxs-lookup"><span data-stu-id="c4436-151">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="c4436-152">Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4436-152">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="c4436-153">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-153">Click **Save**.</span></span>

6. <span data-ttu-id="c4436-154">(**Étape supplémentaire recommandée**) En tant qu'administrateur général ou administrateur SharePoint Online, exécutez la cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** avec le paramètre **DisallowInfectedFileDownload** défini sur *true* pour votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="c4436-154">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="c4436-155">(Cela empêche les personnes d'ouvrir, de transférer, de copier ou de partager des fichiers détectés comme malveillants.)</span><span class="sxs-lookup"><span data-stu-id="c4436-155">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="c4436-156">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="c4436-156">To learn more, see:</span></span> 
- [<span data-ttu-id="c4436-157">Configuration des stratégies de pièces jointes approuvées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-157">Set up Office 365 ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md)
- [<span data-ttu-id="c4436-158">Activer la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="c4436-158">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)

### <a name="atp-safe-links-policies"></a><span data-ttu-id="c4436-159">Stratégies de liens fiables ATP</span><span class="sxs-lookup"><span data-stu-id="c4436-159">ATP Safe Links policies</span></span>

<span data-ttu-id="c4436-160">Pour configurer [des liens approuvés ATP](atp-safe-links.md), vérifiez et modifiez votre stratégie par défaut, puis ajoutez une stratégie pour des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c4436-160">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="c4436-161">Dans le [Centre de sécurité & conformité](https://protection.office.com), **sélectionnez gestion** > \*\*\*\* > **des menaces-liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="c4436-161">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="c4436-162">Double-cliquez sur la stratégie **par défaut** .</span><span class="sxs-lookup"><span data-stu-id="c4436-162">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="c4436-163">Dans la section **utiliser les liens approuvés dans** , sélectionnez l'option **Office 365 ProPlus, Office pour iOS et Android**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-163">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="c4436-164">Dans la section **stratégies qui s'appliquent à des destinataires spécifiques** , cliquez**+** sur le signe plus ().</span><span class="sxs-lookup"><span data-stu-id="c4436-164">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="c4436-165">Spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-165">Specify the following settings:</span></span>

    - <span data-ttu-id="c4436-166">Dans la zone **nom** , tapez un nom, tel que `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="c4436-166">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="c4436-167">Dans la section **Sélectionnez l'action** , choisissez **activé**.</span><span class="sxs-lookup"><span data-stu-id="c4436-167">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="c4436-168">Sélectionnez les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="c4436-168">Select these options:</span></span>

        - <span data-ttu-id="c4436-169">**Utiliser les pièces jointes fiables pour analyser le contenu téléchargeable**</span><span class="sxs-lookup"><span data-stu-id="c4436-169">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="c4436-170">**Appliquer des liens fiables aux messages électroniques envoyés au sein de l'Organisation**</span><span class="sxs-lookup"><span data-stu-id="c4436-170">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="c4436-171">**Ne pas autoriser les utilisateurs à cliquer sur les liens fiables vers l'URL d'origine**</span><span class="sxs-lookup"><span data-stu-id="c4436-171">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="c4436-172">Dans la section **appliqué à** , choisissez **le domaine du destinataire**.</span><span class="sxs-lookup"><span data-stu-id="c4436-172">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="c4436-173">Sélectionnez votre domaine, choisissez **Ajouter**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4436-173">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="c4436-174">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-174">Click **Save**.</span></span>

<span data-ttu-id="c4436-175">Pour plus d'informations, reportez-vous à la rubrique [set up Office 365 ATP Safe Links Policies](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-175">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="c4436-176">Partie 3: anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="c4436-176">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="c4436-177">La [protection anti-hameçonnage](anti-phishing-protection.md) est disponible dans les abonnements incluant [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="c4436-177">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="c4436-178">La protection avancée contre le hameçonnage est disponible dans [](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="c4436-178">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="c4436-179">La procédure suivante décrit comment configurer une stratégie anti-hameçonnage ATP.</span><span class="sxs-lookup"><span data-stu-id="c4436-179">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="c4436-180">Les étapes sont similaires pour la configuration d'une stratégie anti-hameçonnage (sans ATP).</span><span class="sxs-lookup"><span data-stu-id="c4436-180">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="c4436-181">Dans le [Centre de sécurité & Compliance Center](https://protection.office.com), sélectionnez **Threat Management** > **Policy** > **protection contre le hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="c4436-181">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="c4436-182">Cliquez sur **stratégie par défaut**.</span><span class="sxs-lookup"><span data-stu-id="c4436-182">Click **Default policy**.</span></span>

3. <span data-ttu-id="c4436-183">Dans la section **emprunt d'identité** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-183">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    -  <span data-ttu-id="c4436-184">Sous l'onglet **Ajouter des utilisateurs à protéger** , activez la protection.</span><span class="sxs-lookup"><span data-stu-id="c4436-184">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="c4436-185">Ajoutez ensuite des utilisateurs, tels que les membres du tableau de bord de votre organisation, votre directeur général, votre directeur financier et d'autres dirigeants.</span><span class="sxs-lookup"><span data-stu-id="c4436-185">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="c4436-186">(Vous pouvez taper une adresse de messagerie individuelle ou cliquer pour afficher une liste.)</span><span class="sxs-lookup"><span data-stu-id="c4436-186">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="c4436-187">Dans l'onglet **Ajouter des domaines à protéger** , activez **la fonction inclure automatiquement les domaines dont je suis propriétaire**.</span><span class="sxs-lookup"><span data-stu-id="c4436-187">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="c4436-188">Si vous avez des domaines personnalisés, ajoutez-les également.</span><span class="sxs-lookup"><span data-stu-id="c4436-188">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="c4436-189">Sous l'onglet **actions** , sélectionnez **déplacer le message vers les dossiers** de courrier indésirable des destinataires pour les utilisateurs empruntés et les domaines empruntés, puis activez les conseils de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c4436-189">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="c4436-190">Sous l'onglet **intelligence des boîtes aux lettres** , assurez-vous que l'intelligence des boîtes aux lettres est activée.</span><span class="sxs-lookup"><span data-stu-id="c4436-190">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="c4436-191">Dans l'onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-191">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="c4436-192">Dans la section **usurpation** , cliquez sur **modifier**, puis spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-192">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="c4436-193">Dans l'onglet **paramètres du filtre d'usurpation d'identité** , assurez-vous que la protection contre l'usurpation d'identité est activée.</span><span class="sxs-lookup"><span data-stu-id="c4436-193">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="c4436-194">Sous l'onglet **actions** , choisissez déplacer le message vers les dossiers de courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c4436-194">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="c4436-195">Dans l'onglet **vérifier vos paramètres** , une fois que vous avez vérifié vos paramètres, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-195">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="c4436-196">(Si vous n'avez apporté aucune modification, cliquez sur **Annuler**.)</span><span class="sxs-lookup"><span data-stu-id="c4436-196">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="c4436-197">Fermez la page Paramètres de stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4436-197">Close the default policy settings page.</span></span>

<span data-ttu-id="c4436-198">Pour en savoir plus sur les options de stratégie anti-hameçonnage, consultez la rubrique [configurer des stratégies anti-hameçonnage](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-198">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="c4436-199">Partie 4: blocage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="c4436-199">Part 4 - Anti-spam</span></span>

<span data-ttu-id="c4436-200">La [protection contre le courrier](anti-spam-protection.md) indésirable est disponible dans les abonnements incluant [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="c4436-200">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="c4436-201">Dans le [Centre de sécurité & conformité](https://protection.office.com), choisissez**protection contre le courrier**indésirable pour la**stratégie** > de **gestion** > des menaces.</span><span class="sxs-lookup"><span data-stu-id="c4436-201">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="c4436-202">Sous l'onglet **personnalisé** , activez les **paramètres personnalisés** .</span><span class="sxs-lookup"><span data-stu-id="c4436-202">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="c4436-203">Développez **stratégie de filtrage du courrier indésirAble par défaut**, cliquez sur **modifier la stratégie**, puis spécifiez les paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="c4436-203">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="c4436-204">Dans la section **actions de courrier indésirable et en bloc** , définissez le seuil sur une valeur de 5 ou 6.</span><span class="sxs-lookup"><span data-stu-id="c4436-204">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="c4436-205">Dans la section **autoriser les listes** , vérifiez (et si nécessaire, modifiez) vos expéditeurs et domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="c4436-205">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="c4436-206">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c4436-206">Click **Save**.</span></span>

<span data-ttu-id="c4436-207">Pour en savoir plus sur les options de votre stratégie de blocage du courrier indésirable, consultez [la rubrique Configurer les stratégies anti-courrier](configure-the-anti-spam-policies.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="c4436-207">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="c4436-208">Partie 5-paramètres à l'échelle du service</span><span class="sxs-lookup"><span data-stu-id="c4436-208">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="c4436-209">Purge automatique avec zéro heure</span><span class="sxs-lookup"><span data-stu-id="c4436-209">Zero-hour auto purge</span></span>

<span data-ttu-id="c4436-210">[Purge automatique avec zéro heure](zero-hour-auto-purge.md) (ZAP) est disponible dans les abonnements qui incluent [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="c4436-210">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="c4436-211">Cette protection est activée par défaut; Toutefois, les conditions suivantes doivent être remplies pour que la protection soit appliquée:</span><span class="sxs-lookup"><span data-stu-id="c4436-211">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="c4436-212">Les actions de courrier indésirable sont définies pour **déplacer le message vers le dossier** courrier indésirable des [stratégies de blocage du courrier](anti-spam-protection.md)indésirable.</span><span class="sxs-lookup"><span data-stu-id="c4436-212">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="c4436-213">Les utilisateurs ont conservé leurs [paramètres](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)de courrier indésirable par défaut et n'ont pas désactivé la protection contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c4436-213">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="c4436-214">Pour en savoir plus, consultez la rubrique [Zero-Hour auto-protection-protection contre le courrier indésirable et les programmes malveillants](zero-hour-auto-purge.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-214">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="c4436-215">Journalisation d'audit</span><span class="sxs-lookup"><span data-stu-id="c4436-215">Audit logging</span></span>

<span data-ttu-id="c4436-216">La journalisation d'audit est disponible dans les abonnements qui incluent [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span><span class="sxs-lookup"><span data-stu-id="c4436-216">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="c4436-217">Pour afficher les données des rapports de protection contre les menaces, tels que le [tableau de bord de sécurité](security-dashboard.md), les rapports de sécurité de [messagerie](view-email-security-reports.md)et l' [Explorateur](use-explorer-in-security-and-compliance.md), la journalisation d'audit doit être activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c4436-217">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="c4436-218">Pour en savoir plus, consultez la rubrique [activer ou désactiver la recherche dans le journal d'audit Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="c4436-218">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="c4436-219">Tâches consécutives à l'installation</span><span class="sxs-lookup"><span data-stu-id="c4436-219">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="c4436-220">SurVeillez les nouvelles fonctionnalités et les mises à jour de service</span><span class="sxs-lookup"><span data-stu-id="c4436-220">Watch for new features and service updates</span></span>

- [<span data-ttu-id="c4436-221">Configurer les options de publication standard ou ciblée</span><span class="sxs-lookup"><span data-stu-id="c4436-221">Set up the Standard or Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)

- [<span data-ttu-id="c4436-222">Accédez à votre centre de messages pour afficher les annonces de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c4436-222">Go to your Message center to view feature announcements</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide) 

- [<span data-ttu-id="c4436-223">Consultez la feuille de route Microsoft 365 pour afficher l'état des nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c4436-223">Visit the Microsoft 365 Roadmap to see status of new features</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="c4436-224">Consulter les descriptions de service Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-224">Review the Office 365 Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)

### <a name="see-how-threat-protection-features-are-working-for-your-organization"></a><span data-ttu-id="c4436-225">Voir comment les fonctionnalités de protection contre les menaces fonctionnent pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="c4436-225">See how threat protection features are working for your organization</span></span>

- [<span data-ttu-id="c4436-226">Visiter votre tableau de bord de sécurité</span><span class="sxs-lookup"><span data-stu-id="c4436-226">Visit your security dashboard</span></span>](security-dashboard.md)

- <span data-ttu-id="c4436-227">[Afficher les rapports pour la](view-reports-for-atp.md)protection avancée contre les menaces Office 365, y compris l' [Explorateur](use-explorer-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="c4436-227">[View the reports for Office 365 ATP](view-reports-for-atp.md), including [Explorer](use-explorer-in-security-and-compliance.md)</span></span>

- [<span data-ttu-id="c4436-228">Afficher vos rapports de sécurité de messagerie</span><span class="sxs-lookup"><span data-stu-id="c4436-228">View your email security reports</span></span>](view-email-security-reports.md)

### <a name="periodically-review-and-revise-your-threat-protection-policies"></a><span data-ttu-id="c4436-229">Vérifier et réviser régulièrement vos stratégies de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c4436-229">Periodically review and revise your threat protection policies</span></span>

- [<span data-ttu-id="c4436-230">Vérifier votre score de sécurité</span><span class="sxs-lookup"><span data-stu-id="c4436-230">Review your Secure Score</span></span>](microsoft-secure-score.md)

- [<span data-ttu-id="c4436-231">Utilisation de vos rapports intelligents et de vos connaissances dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c4436-231">Use your smart reports and insights in the Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 

- [<span data-ttu-id="c4436-232">Assurer la sécurité des utilisateurs grâce aux fonctionnalités d'enquête et de réponse aux menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="c4436-232">Keep users safe with Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md) 
 