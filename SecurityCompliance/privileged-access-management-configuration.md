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
ms.openlocfilehash: e086e93c268fe4de627bef30d3ac7aed8e6b1f98
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265236"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="886fd-103">Configuration de la gestion des accès privilégiés dans Office 365</span><span class="sxs-lookup"><span data-stu-id="886fd-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="886fd-104">Cette rubrique traite des conseils de déploiement et de configuration pour les fonctionnalités uniquement disponibles dans Office 365 E5 et les SKU de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="886fd-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="886fd-105">Cette rubrique vous guide tout au long de l'activation et de la configuration de la gestion des accès privilégiés dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="886fd-105">This topic guides you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="886fd-106">Vous pouvez utiliser le centre d'administration Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser l'accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="886fd-106">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="886fd-107">Activer et configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="886fd-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="886fd-108">Procédez comme suit pour configurer et utiliser l'accès privilégié dans votre organisation Office 365:</span><span class="sxs-lookup"><span data-stu-id="886fd-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="886fd-109">Étape 1: créer un groupe d'approbateurs</span><span class="sxs-lookup"><span data-stu-id="886fd-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="886fd-110">Avant de commencer à utiliser l'accès par privilège, déterminez qui a besoin de l'autorité d'approbation pour les demandes entrantes d'accès à des tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="886fd-110">Before you start using privilege access, determine who needs approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="886fd-111">Tout utilisateur qui fait partie du groupe apProbateurs est en mesure d'approuver les demandes d'accès.</span><span class="sxs-lookup"><span data-stu-id="886fd-111">Any user who is part of the Approvers’ group is able to approve access requests.</span></span> <span data-ttu-id="886fd-112">Pour cela, vous créez un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="886fd-112">This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="886fd-113">Étape 2: activer l'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="886fd-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="886fd-114">L'accès privilégié doit être explicitement activé dans Office 365 avec le groupe d'approbateurs par défaut, y compris un ensemble de comptes système que vous souhaitez exclure du contrôle d'accès gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="886fd-114">Privileged access must be explicitly enabled in Office 365 with the default approver group, including a set of system accounts that you want excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="886fd-115">Étape 3: créer une stratégie d'accès</span><span class="sxs-lookup"><span data-stu-id="886fd-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="886fd-116">La création d'une stratégie d'approbation vous permet de définir les exigences d'approbation spécifiques au niveau des tâches individuelles.</span><span class="sxs-lookup"><span data-stu-id="886fd-116">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="886fd-117">Les options type d'approbation sont **automatique** ou **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="886fd-117">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="886fd-118">Étape 4: soumettre/approuver des demandes d'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="886fd-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="886fd-119">Une fois activé, l'accès privilégié nécessite des approbations pour toutes les tâches auxquelles une stratégie d'approbation associée est définie.</span><span class="sxs-lookup"><span data-stu-id="886fd-119">Once enabled, privileged access requires approvals for any task that has an associated approval policy defined.</span></span> <span data-ttu-id="886fd-120">Pour les tâches comprises dans une stratégie d'approbation, les utilisateurs doivent demander une approbation d'accès et leur accorder les autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="886fd-120">For tasks included in an approval policy, users must request and be granted access approval to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="886fd-121">Une fois que l'approbation est accordée, l'utilisateur qui a effectué la demande peut exécuter la tâche prévue et l'accès privilégié autorise et exécute la tâche au nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="886fd-121">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on behalf of the user.</span></span> <span data-ttu-id="886fd-122">L'approbation reste valide pour la durée demandée (la durée par défaut est de 4 heures), pendant laquelle le demandeur peut exécuter la tâche prévue plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="886fd-122">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="886fd-123">Toutes les exécutions de ce type sont enregistrées et mises à disposition pour l'audit de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="886fd-123">All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="886fd-124">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l'accès privilégié, suivez les étapes de la [page connexion à Exchange Online PowerShell à l'aide de l'authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour vous connecter à Exchange Online PowerShell avec votre Office 365 informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="886fd-124">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="886fd-125">Vous n'avez pas besoin d'activer l'authentification multifacteur pour votre organisation Office 365 pour utiliser les étapes d'activation de l'accès privilégié lors de la connexion à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="886fd-125">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="886fd-126">La connexion avec l'authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.</span><span class="sxs-lookup"><span data-stu-id="886fd-126">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="886fd-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="886fd-127"></span></span>

## <a name="step-1-create-an-approvers-group"></a><span data-ttu-id="886fd-128">Étape 1: créer un groupe d'approbateurs</span><span class="sxs-lookup"><span data-stu-id="886fd-128">Step 1: Create an approver's group</span></span>

1. <span data-ttu-id="886fd-129">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-129">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="886fd-130">Dans le centre d'administration, accédez à **groupes** > **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="886fd-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="886fd-131">Sélectionnez **groupe de sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie du groupe**et **Description** pour le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="886fd-131">Select **mail-enabled security group** and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="886fd-132">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="886fd-132">Save the group.</span></span> <span data-ttu-id="886fd-133">La configuration complète du groupe peut prendre quelques minutes et s'afficher dans le centre d'administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="886fd-133">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="886fd-134">Sélectionnez le nouveau groupe approbateur et sélectionnez **modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="886fd-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="886fd-135">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="886fd-135">Save the group.</span></span>

<span data-ttu-id="886fd-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="886fd-136"></span></span>

## <a name="step-2-enable-privileged-access"></a><span data-ttu-id="886fd-137">Étape 2: activer l'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="886fd-137">Step 2: Enable privileged access</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-138">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-138">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="886fd-139">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-139">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="886fd-140">Dans le centre d'administration, accédez à **paramètres > sécurité & confidentialité** > **accès aux privilèges**.</span><span class="sxs-lookup"><span data-stu-id="886fd-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-141">Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="886fd-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="886fd-142">Affectez le groupe d'approbateurs que vous avez créé à l'étape 1 comme groupe d'approbateurs **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="886fd-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="886fd-143">**Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="886fd-143">**Save** and **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-144">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-144">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-145">Pour activer l'accès privilégié et attribuer le groupe de l'approbateur, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-145">To enable privileged access and to assign the approver's group, run the following command in Exchange Online PowerShell:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="886fd-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="886fd-147">La fonctionnalité comptes système est mise à disposition pour garantir que certaines automations au sein de vos organisations peuvent fonctionner sans dépendance sur l'accès privilégié, mais il est recommandé de faire en sorte que ces exclusions soient exceptionnelles et que celles autorisées soient approuvées et vérifiées. régulièrement.</span><span class="sxs-lookup"><span data-stu-id="886fd-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="886fd-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="886fd-148"></span></span>

## <a name="step-3-create-an-access-policy"></a><span data-ttu-id="886fd-149">Étape 3: créer une stratégie d'accès</span><span class="sxs-lookup"><span data-stu-id="886fd-149">Step 3: Create an access policy</span></span>

<span data-ttu-id="886fd-150">Vous pouvez créer et configurer jusqu'à 30 stratégies d'accès privilégié pour votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="886fd-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-151">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-151">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="886fd-152">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-152">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="886fd-153">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-154">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="886fd-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="886fd-155">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="886fd-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="886fd-156">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:</span><span class="sxs-lookup"><span data-stu-id="886fd-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="886fd-157">**Type de stratégie**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="886fd-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="886fd-158">**Étendue de stratégie**: Exchange</span><span class="sxs-lookup"><span data-stu-id="886fd-158">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="886fd-159">**Nom**de la stratégie: sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="886fd-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="886fd-160">**Type d'approbation**: manuelle ou automatique</span><span class="sxs-lookup"><span data-stu-id="886fd-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="886fd-161">**Groupe d'approbation**: sélectionnez le groupe approbateurs créé à l'étape 1</span><span class="sxs-lookup"><span data-stu-id="886fd-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="886fd-162">Sélectionnez **créer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="886fd-162">Select **Create** and then **Close**.</span></span> <span data-ttu-id="886fd-163">La configuration et l'activation de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="886fd-163">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-164">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-164">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-165">Pour créer et définir une stratégie d'approbation, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-165">To create and define an approval policy, run the following command in Exchange Online PowerShell:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="886fd-166">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="886fd-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="886fd-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="886fd-168">Étape 4: soumettre/approuver des demandes d'accès privilégié</span><span class="sxs-lookup"><span data-stu-id="886fd-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="886fd-169">Demande d'une autorisation d'élévation pour exécuter des tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="886fd-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="886fd-170">Les demandes d'accès privilégié sont valides jusqu'à 24 heures après l'envoi de la demande.</span><span class="sxs-lookup"><span data-stu-id="886fd-170">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="886fd-171">Si elles ne sont pas approuvées ou refusées, les demandes expirent et l'accès n'est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="886fd-171">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-172">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-172">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="886fd-173">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) à l'aide de vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="886fd-173">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="886fd-174">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-175">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="886fd-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="886fd-176">Sélectionnez **nouvelle demande**.</span><span class="sxs-lookup"><span data-stu-id="886fd-176">Select **New request**.</span></span> <span data-ttu-id="886fd-177">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:</span><span class="sxs-lookup"><span data-stu-id="886fd-177">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="886fd-178">**Type de demande**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="886fd-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="886fd-179">**Étendue**de la demande: Exchange</span><span class="sxs-lookup"><span data-stu-id="886fd-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="886fd-180">**Demande**: sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="886fd-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="886fd-181">**Durée (heures)**: nombre d'heures d'accès demandé.</span><span class="sxs-lookup"><span data-stu-id="886fd-181">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="886fd-182">Il n'y a pas de limite sur le nombre d'heures qui peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="886fd-182">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="886fd-183">**Commentaires**: champ de texte pour les commentaires liés à votre demande d'accès</span><span class="sxs-lookup"><span data-stu-id="886fd-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="886fd-184">Sélectionnez **Enregistrer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="886fd-184">Select **Save** and then **Close**.</span></span> <span data-ttu-id="886fd-185">Votre demande sera envoyée au groupe de l'approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="886fd-185">Your request will be sent to the approver's group via email.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-186">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-186">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-187">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d'approbation au groupe de l'approbateur:</span><span class="sxs-lookup"><span data-stu-id="886fd-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="886fd-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="886fd-189">Afficher l'état des demandes d'élévation</span><span class="sxs-lookup"><span data-stu-id="886fd-189">View status of elevation requests</span></span>
<span data-ttu-id="886fd-190">Après la création d'une demande d'approbation, l'état de la demande d'élévation peut être révisé dans le centre d'administration ou dans Exchange Management PowerShell à l'aide de l'ID de demande associé.</span><span class="sxs-lookup"><span data-stu-id="886fd-190">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-191">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-191">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="886fd-192">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="886fd-192">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="886fd-193">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-193">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-194">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="886fd-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="886fd-195">Sélectionnez **affichage** pour filtrer les demandes soumises par état **en attente**, **approuvé**, **refusé**ou **référentiel sécurisé du client** .</span><span class="sxs-lookup"><span data-stu-id="886fd-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-196">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-196">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-197">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher l'état d'une demande d'approbation pour un ID de demande spécifique:</span><span class="sxs-lookup"><span data-stu-id="886fd-197">Run the following command in Exchange Online PowerShell to view an approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="886fd-198">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="886fd-199">Approbation d'une demande d'autorisation d'élévation</span><span class="sxs-lookup"><span data-stu-id="886fd-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="886fd-200">Lorsqu'une demande d'approbation est créée, les membres du groupe d'approbateur approprié reçoivent une notification par courrier électronique et peuvent approuver la demande associée à l'ID de demande.</span><span class="sxs-lookup"><span data-stu-id="886fd-200">When an approval request is created, members of the relevant approver group receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="886fd-201">Le demandeur est informé de la demande d'approbation ou de refus via un message électronique.</span><span class="sxs-lookup"><span data-stu-id="886fd-201">The requestor is notified of the request approval or denial via email message.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-202">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-202">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="886fd-203">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="886fd-203">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="886fd-204">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-204">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-205">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="886fd-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="886fd-206">Sélectionnez une demande répertoriée pour afficher les détails et agir sur la demande.</span><span class="sxs-lookup"><span data-stu-id="886fd-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="886fd-207">Sélectionnez **approuver** pour approuver la demande ou **refuser** pour la refuser.</span><span class="sxs-lookup"><span data-stu-id="886fd-207">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="886fd-208">Les demandes précédemment approuvées peuvent avoir un accès révoqué en sélectionnant **Revoke**.</span><span class="sxs-lookup"><span data-stu-id="886fd-208">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-209">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-209">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-210">Pour approuver une demande d'autorisation d'élévation, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-210">To approve an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="886fd-211">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="886fd-212">Pour refuser une demande d'autorisation d'élévation, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-212">To deny an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="886fd-213">Exemple :</span><span class="sxs-lookup"><span data-stu-id="886fd-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="886fd-214">Supprimer une stratégie d'accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="886fd-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="886fd-215">Si elle n'est plus nécessaire dans votre organisation, vous pouvez supprimer une stratégie d'accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="886fd-215">If it is no longer needed in your organization, you can delete a privileged access policy.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-216">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-216">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="886fd-217">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="886fd-218">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-218">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-219">Sélectionnez **gérer les stratégies d'accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="886fd-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="886fd-220">Sélectionnez **configurer les stratégies**.</span><span class="sxs-lookup"><span data-stu-id="886fd-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="886fd-221">Sélectionnez la stratégie à supprimer, puis **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="886fd-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="886fd-222">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="886fd-222">Select **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-223">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-223">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-224">Pour supprimer une stratégie d'accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-224">To delete a privileged access policy, run the following command in Exchange Online Powershell:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="886fd-225">DésActivation de l'accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="886fd-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="886fd-226">Si nécessaire, vous pouvez désactiver la gestion des accès privilégiés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-226">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="886fd-227">La désActivation de l'accès privilégié ne supprime pas les stratégies d'approbation ou les groupes d'approbateurs associés.</span><span class="sxs-lookup"><span data-stu-id="886fd-227">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="886fd-228">Dans le centre d'administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="886fd-228">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="886fd-229">Connectez-vous au [Centre d'administration Microsoft 365](https://admin.microsoft.com) avec des informations d'identification pour un compte d'administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="886fd-229">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="886fd-230">Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="886fd-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="886fd-231">Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="886fd-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="886fd-232">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="886fd-232">In Exchange Management PowerShell</span></span>

<span data-ttu-id="886fd-233">Pour désactiver l'accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="886fd-233">To disable privileged access, run the following command in Exchange Online Powershell:</span></span>

```
Disable-ElevatedAccessControl
```