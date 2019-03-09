---
title: Configuration de la gestion des accès privilégiés dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: Utilisez cette rubrique pour en savoir plus sur la configuration de la gestion des accès privilégiés dans Office 365
ms.openlocfilehash: 3d186998006dd3cc59877b1571f50314af5bbce8
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492823"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="3acd7-103">Configuration de la gestion des accès privilégiés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3acd7-104">Cette rubrique traite des conseils de déploiement et de configuration pour les fonctionnalités uniquement disponibles dans Office 365 E5 et les SKU de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="3acd7-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="3acd7-105">Cette rubrique vous guidera tout au long de l'activation et de la configuration de la gestion des accès privilégiés dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="3acd7-105">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="3acd7-106">Vous pouvez utiliser le centre d'administration Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser l'accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="3acd7-106">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="3acd7-107">Activer et configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="3acd7-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="3acd7-108">Procédez comme suit pour configurer et utiliser l'accès privilégié dans votre organisation Office 365:</span><span class="sxs-lookup"><span data-stu-id="3acd7-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="3acd7-109">Étape 1: créer un groupe d'approbateurs</span><span class="sxs-lookup"><span data-stu-id="3acd7-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="3acd7-110">Avant de commencer à utiliser l'accès aux privilèges, déterminez qui disposera de l'autorité d'approbation pour les demandes entrantes d'accès à des tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="3acd7-110">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="3acd7-111">Tout utilisateur qui fait partie du groupe apProbateurs est en mesure d'approuver les demandes d'accès.</span><span class="sxs-lookup"><span data-stu-id="3acd7-111">Any user who is part of the Approvers’ group will be able to approve access requests.</span></span> <span data-ttu-id="3acd7-112">Pour cela, vous créez un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="3acd7-112">This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="3acd7-113">Étape 2: activer l'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3acd7-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="3acd7-114">L'accès privilégié doit être activé de manière explicite dans Office 365 avec le groupe d'approbateurs par défaut et inclure un ensemble de comptes système que vous souhaitez exclure du contrôle d'accès gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="3acd7-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="3acd7-115">Étape 3: créer une stratégie d'accès</span><span class="sxs-lookup"><span data-stu-id="3acd7-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="3acd7-116">La création d'une stratégie d'approbation vous permet de définir les exigences d'approbation spécifiques au niveau des tâches individuelles.</span><span class="sxs-lookup"><span data-stu-id="3acd7-116">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="3acd7-117">Les options type d'approbation sont **automatique** ou **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-117">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="3acd7-118">Étape 4: soumettre/approuver des demandes d'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3acd7-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="3acd7-119">Une fois activé, l'accès privilégié nécessite des approbations pour l'exécution de n'importe quelle tâche à laquelle une stratégie d'approbation associée est définie.</span><span class="sxs-lookup"><span data-stu-id="3acd7-119">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined.</span></span> <span data-ttu-id="3acd7-120">Les utilisateurs qui ont besoin d'exécuter des tâches incluses dans une stratégie d'approbation doivent demander l'approbation de l'accès et disposer des autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="3acd7-120">Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="3acd7-121">Une fois que l'approbation est accordée, l'utilisateur qui a effectué la demande peut exécuter la tâche prévue et l'accès privilégié autorise et exécute la tâche au nom des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3acd7-121">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf.</span></span> <span data-ttu-id="3acd7-122">L'approbation reste valide pour la durée demandée (la durée par défaut est de 4 heures), pendant laquelle le demandeur peut exécuter la tâche prévue plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="3acd7-122">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="3acd7-123">Toutes les exécutions de ce type sont enregistrées et mises à disposition pour l'audit de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="3acd7-123">All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="3acd7-124">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l'accès privilégié, suivez les étapes de la [page connexion à Exchange Online PowerShell à l'aide de l'authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour vous connecter à Exchange Online PowerShell avec votre Office 365 informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="3acd7-124">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="3acd7-125">Vous n'avez pas besoin d'activer l'authentification multifacteur pour votre organisation Office 365 pour utiliser les étapes d'activation de l'accès privilégié lors de la connexion à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3acd7-125">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="3acd7-126">La connexion avec l'authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.</span><span class="sxs-lookup"><span data-stu-id="3acd7-126">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="3acd7-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="3acd7-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="3acd7-128">Étape 1: créer un groupe d'approbateurs</span><span class="sxs-lookup"><span data-stu-id="3acd7-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="3acd7-129">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="3acd7-130">Dans le centre d'administration, accédez à **groupes** > **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="3acd7-131">Sélectionnez le groupe Groupe de **sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie du groupe**et **Description** pour le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="3acd7-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="3acd7-132">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="3acd7-132">Save the group.</span></span> <span data-ttu-id="3acd7-133">La configuration complète du groupe peut prendre quelques minutes et s'afficher dans le centre d'administration Office 365.</span><span class="sxs-lookup"><span data-stu-id="3acd7-133">It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="3acd7-134">Sélectionnez le nouveau groupe approbateur et sélectionnez **modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="3acd7-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="3acd7-135">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="3acd7-135">Save the group.</span></span>

<span data-ttu-id="3acd7-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="3acd7-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="3acd7-137">Étape 2: activation de l'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3acd7-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-138">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-139">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="3acd7-140">Dans le centre d'administration, accédez à **paramètres > sécurité & confidentialité** > **accès aux privilèges**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-141">Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="3acd7-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="3acd7-142">Affectez le groupe d'approbateurs que vous avez créé à l'étape 1 comme groupe d'approbateurs **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="3acd7-143">**Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-144">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-145">Exécutez la commande suivante dans Exchange Online PowerShell pour activer l'accès privilégié et pour affecter le groupe de l'approbateur:</span><span class="sxs-lookup"><span data-stu-id="3acd7-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="3acd7-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="3acd7-147">La fonctionnalité comptes système est mise à disposition pour garantir que certaines automations au sein de vos organisations peuvent fonctionner sans dépendance sur l'accès privilégié, mais il est recommandé de faire en sorte que ces exclusions soient exceptionnelles et que celles autorisées soient approuvées et vérifiées. régulièrement.</span><span class="sxs-lookup"><span data-stu-id="3acd7-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="3acd7-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="3acd7-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="3acd7-149">Étape 3: créer une stratégie d'accès</span><span class="sxs-lookup"><span data-stu-id="3acd7-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="3acd7-150">Vous pouvez créer et configurer jusqu'à 30 stratégies d'accès privilégié pour votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="3acd7-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-151">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-152">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="3acd7-153">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-154">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3acd7-155">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="3acd7-156">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:</span><span class="sxs-lookup"><span data-stu-id="3acd7-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="3acd7-157">**Type de stratégie**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="3acd7-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="3acd7-158">**Étendue de stratégie**: Exchange</span><span class="sxs-lookup"><span data-stu-id="3acd7-158">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="3acd7-159">**Nom**de la stratégie: sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="3acd7-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="3acd7-160">**Type d'approbation**: manuelle ou automatique</span><span class="sxs-lookup"><span data-stu-id="3acd7-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="3acd7-161">**Groupe d'approbation**: sélectionnez le groupe approbateurs créé à l'étape 1</span><span class="sxs-lookup"><span data-stu-id="3acd7-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="3acd7-162">Sélectionnez **créer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-162">Select **Create** and then **Close**.</span></span> <span data-ttu-id="3acd7-163">La configuration et l'activation de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="3acd7-163">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-164">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-165">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et définir une stratégie d'approbation:</span><span class="sxs-lookup"><span data-stu-id="3acd7-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="3acd7-166">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="3acd7-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="3acd7-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="3acd7-168">Étape 4: soumettre/approuver des demandes d'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="3acd7-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="3acd7-169">Demande d'une autorisation d'élévation pour exécuter des tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="3acd7-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="3acd7-170">Les demandes d'accès privilégié sont valides jusqu'à 24 heures après l'envoi de la demande.</span><span class="sxs-lookup"><span data-stu-id="3acd7-170">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="3acd7-171">Si elles ne sont pas approuvées ou refusées, les demandes expirent et l'accès n'est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="3acd7-171">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-172">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-173">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="3acd7-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="3acd7-174">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-175">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3acd7-176">Sélectionnez **nouvelle demande**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-176">Select **New request**.</span></span> <span data-ttu-id="3acd7-177">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:</span><span class="sxs-lookup"><span data-stu-id="3acd7-177">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="3acd7-178">**Type de demande**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="3acd7-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="3acd7-179">**Étendue**de la demande: Exchange</span><span class="sxs-lookup"><span data-stu-id="3acd7-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="3acd7-180">**Demande**: sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="3acd7-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="3acd7-181">**Durée (heures)**: nombre d'heures d'accès demandé.</span><span class="sxs-lookup"><span data-stu-id="3acd7-181">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="3acd7-182">Il n'y a pas de limite sur le nombre d'heures qui peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="3acd7-182">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="3acd7-183">**Commentaires**: champ de texte pour les commentaires liés à votre demande d'accès</span><span class="sxs-lookup"><span data-stu-id="3acd7-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="3acd7-184">Sélectionnez **Enregistrer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-184">Select **Save** and then **Close**.</span></span> <span data-ttu-id="3acd7-185">Votre demande sera envoyée au groupe de l'approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="3acd7-185">Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-186">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-187">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d'approbation au groupe de l'approbateur:</span><span class="sxs-lookup"><span data-stu-id="3acd7-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="3acd7-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="3acd7-189">Afficher l'état des demandes d'élévation</span><span class="sxs-lookup"><span data-stu-id="3acd7-189">View status of elevation requests</span></span>
<span data-ttu-id="3acd7-190">Après la création d'une demande d'approbation, l'état de la demande d'élévation peut être révisé dans le centre d'administration ou dans Exchange Management PowerShell à l'aide de l'ID de demande associé.</span><span class="sxs-lookup"><span data-stu-id="3acd7-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-191">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-192">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="3acd7-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="3acd7-193">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-194">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3acd7-195">Sélectionnez **affichage** pour filtrer les demandes soumises par état **en attente**, **approuvé**, **refusé**ou **référentiel sécurisé du client** .</span><span class="sxs-lookup"><span data-stu-id="3acd7-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-196">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-197">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher l'état d'une demande d'approbation pour un ID de demande spécifique:</span><span class="sxs-lookup"><span data-stu-id="3acd7-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="3acd7-198">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="3acd7-199">Approbation d'une demande d'autorisation d'élévation</span><span class="sxs-lookup"><span data-stu-id="3acd7-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="3acd7-200">Lorsqu'une demande d'approbation est créée, les membres du groupe d'approbateur approprié reçoivent une notification par courrier électronique et peuvent approuver la demande associée à l'ID de demande.</span><span class="sxs-lookup"><span data-stu-id="3acd7-200">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="3acd7-201">Le demandeur est informé de l'approbation ou du refus de la demande via un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3acd7-201">The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-202">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-203">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="3acd7-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="3acd7-204">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-205">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3acd7-206">Sélectionnez une demande répertoriée pour afficher les détails et agir sur la demande.</span><span class="sxs-lookup"><span data-stu-id="3acd7-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="3acd7-207">Sélectionnez **approuver** pour approuver la demande ou **refuser** pour la refuser.</span><span class="sxs-lookup"><span data-stu-id="3acd7-207">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="3acd7-208">Les demandes précédemment approuvées peuvent avoir un accès révoqué en sélectionnant **Revoke**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-208">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-209">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-210">Exécutez la commande suivante dans Exchange Online PowerShell pour approuver une demande d'autorisation d'élévation:</span><span class="sxs-lookup"><span data-stu-id="3acd7-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="3acd7-211">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="3acd7-212">Exécutez la commande suivante dans Exchange Online PowerShell pour refuser une demande d'autorisation d'élévation:</span><span class="sxs-lookup"><span data-stu-id="3acd7-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="3acd7-213">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3acd7-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="3acd7-214">Supprimer une stratégie d'accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="3acd7-215">Vous pouvez supprimer une stratégie d'accès privilégié si elle n'est plus nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-216">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-217">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="3acd7-218">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-219">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="3acd7-220">Sélectionnez **configurer les stratégies**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="3acd7-221">Sélectionnez la stratégie à supprimer, puis **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="3acd7-222">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-223">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-224">Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer une stratégie d'accès privilégié:</span><span class="sxs-lookup"><span data-stu-id="3acd7-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="3acd7-225">DésActivation de l'accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="3acd7-226">Si nécessaire, vous pouvez désactiver la gestion des accès privilégiés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-226">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="3acd7-227">La désActivation de l'accès privilégié ne supprime pas les stratégies d'approbation ou les groupes d'approbateurs associés.</span><span class="sxs-lookup"><span data-stu-id="3acd7-227">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="3acd7-228">Utilisation du centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3acd7-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="3acd7-229">Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3acd7-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="3acd7-230">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="3acd7-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="3acd7-231">Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="3acd7-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="3acd7-232">Utilisation d'Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="3acd7-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="3acd7-233">Exécutez la commande suivante dans Exchange Online PowerShell pour désactiver l'accès privilégié:</span><span class="sxs-lookup"><span data-stu-id="3acd7-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```