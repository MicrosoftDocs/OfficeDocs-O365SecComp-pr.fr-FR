---
title: Configuration de la gestion accès privilégié dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Utilisez cette rubrique pour en savoir plus sur la configuration de gestion de l’accès privilégié dans Office 365
ms.openlocfilehash: 6494505554a02f005df8f45839c9575094acbf1a
ms.sourcegitcommit: d31904e81f81d0fba75309a2bc8bbfb05565a0b4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "24055249"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="8857c-103">Configuration de la gestion accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8857c-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8857c-104">Cette rubrique traite des instructions de déploiement et de configuration pour les fonctionnalités uniquement actuellement disponibles dans Office 365 E5 et références de conformité avancées.</span><span class="sxs-lookup"><span data-stu-id="8857c-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="8857c-p101">Cette rubrique vous guide par le biais de l’activation et la configuration de gestion de l’accès privilégié dans votre organisation Office 365. Vous pouvez utiliser le centre d’administration de Microsoft 365 les Exchange Management PowerShell pour gérer et utiliser un accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="8857c-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="8857c-107">Activer et configurer la gestion des accès privilégié</span><span class="sxs-lookup"><span data-stu-id="8857c-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="8857c-108">Suivez ces étapes pour configurer et utiliser un accès privilégié dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="8857c-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="8857c-109">Étape 1 : Créer le groupe d’approbateur</span><span class="sxs-lookup"><span data-stu-id="8857c-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="8857c-p102">Avant de commencer à l’aide de privilège d’accès, déterminer ayant autorité d’approbation pour les demandes entrantes pour l’accès aux tâches avec des privilèges élevés et privilégiés. Tout utilisateur qui fait partie du groupe des approbateurs sera en mesure d’approuver les demandes d’accès. Cette option est activée en créant un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="8857c-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="8857c-113">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="8857c-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="8857c-114">Accès privilégié doit être activé explicitement dans Office 365 avec le groupe d’approbateur par défaut et y compris un ensemble de comptes système que vous souhaitez exclure le contrôle d’accès de gestion des accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="8857c-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="8857c-115">Étape 3 : Créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="8857c-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="8857c-p103">Création d’une stratégie d’approbation vous permet de définir les exigences spécifiques limitées à des tâches spécifiques. Les options de type approbation sont **automatique** ou **manuel**.</span><span class="sxs-lookup"><span data-stu-id="8857c-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="8857c-118">Étape 4 : Envoyer/approuver les demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="8857c-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="8857c-p104">Une fois activée, privilégié access nécessite approbations pour l’exécution de toute tâche qui dispose d’une stratégie d’approbation associé définie. Les utilisateurs qui ont besoin exécuter des tâches incluses dans l’une stratégie d’approbation doit demander et avoir approbation d’accès afin de disposer des autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="8857c-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="8857c-p105">Une fois l’approbation est accordée, l’utilisateur peut exécuter la tâche souhaitée et accès privilégié seront autoriser et exécuter la tâche de la part des utilisateurs. L’approbation restera valide pour le demandé durée (durée par défaut est de 4 heures) pendant laquelle le demandeur peut exécuter la tâche prévue à plusieurs reprises. Toutes ces exécutions sont connectées et mises à disposition pour la sécurité et d’audit de conformité.</span><span class="sxs-lookup"><span data-stu-id="8857c-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="8857c-p106">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l’accès privilégié, suivez les étapes [se connecter à Exchange Online PowerShell à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour se connecter à Exchange Online PowerShell avec Office 365 informations d’identification. Il est inutile d’activer l’authentification multifacteur pour votre organisation Office 365 les étapes permettant d’activer l’accès privilégié lors de la connexion à Exchange Online PowerShell. Établir une connexion avec l’authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.</span><span class="sxs-lookup"><span data-stu-id="8857c-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="8857c-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="8857c-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="8857c-128">Étape 1 : créer le groupe d’approbateur</span><span class="sxs-lookup"><span data-stu-id="8857c-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="8857c-129">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8857c-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="8857c-130">Dans le centre d’administration, accédez à **groupes** > **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="8857c-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="8857c-131">Sélectionnez le type de groupe du **groupe de sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie de groupe**et **Description** pour le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="8857c-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="8857c-p107">Enregistrez le groupe. Il peut prendre quelques minutes pour le groupe pour être entièrement configuré et apparaissent dans le centre d’administration d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="8857c-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="8857c-134">Sélectionnez groupe de l’approbateur nouveau et sélectionnez **Modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="8857c-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="8857c-135">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="8857c-135">Save the group.</span></span>

<span data-ttu-id="8857c-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="8857c-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="8857c-137">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="8857c-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-138">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-139">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8857c-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="8857c-140">Dans le centre d’administration, accédez à **Paramètres > sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-141">Activer le contrôle **nécessitent des autorisations d’accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="8857c-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="8857c-142">Affectez groupe de l’approbateur que vous avez créé à l’étape 1 en tant qu' **approbateurs groupe par défaut**.</span><span class="sxs-lookup"><span data-stu-id="8857c-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="8857c-143">**Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8857c-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-144">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-145">Exécutez la commande suivante dans Exchange Online PowerShell pour activer l’accès privilégié et à affecter à groupe de l’approbateur :</span><span class="sxs-lookup"><span data-stu-id="8857c-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="8857c-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="8857c-147">Comptes système fonctionnalité sera disponible pour s’assurer de certains automatisations au sein de votre organisation peuvent travailler sans dépendance sur un accès privilégié, mais il est recommandé que ces exclusions exceptionnelles et ceux autorisés doivent être approuvés et audit régulièrement.</span><span class="sxs-lookup"><span data-stu-id="8857c-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="8857c-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="8857c-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="8857c-149">Étape 3 : créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="8857c-149">Step 3 - Create an access policy</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-150">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-150">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-151">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8857c-151">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="8857c-152">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-152">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-153">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="8857c-153">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="8857c-154">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="8857c-154">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="8857c-155">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="8857c-155">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="8857c-156">**Type de stratégie**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="8857c-156">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="8857c-157">**Étendue de la stratégie**: Exchange ou Office 365</span><span class="sxs-lookup"><span data-stu-id="8857c-157">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="8857c-158">**Nom de la stratégie**: sélectionnez dans les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="8857c-158">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="8857c-159">**Type d’approbation**: manuelle ou automatique</span><span class="sxs-lookup"><span data-stu-id="8857c-159">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="8857c-160">**Groupe d’approbation**: sélectionnez le groupe approbateurs créé à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="8857c-160">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="8857c-p108">Sélectionnez **créer** , puis sur **Fermer**. Il peut prendre quelques minutes pour la stratégie soit entièrement configuré et activé.</span><span class="sxs-lookup"><span data-stu-id="8857c-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-163">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-163">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-164">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et définir une stratégie d’approbation :</span><span class="sxs-lookup"><span data-stu-id="8857c-164">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="8857c-165">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-165">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="8857c-166"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="8857c-166"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="8857c-167">Étape 4 : Envoyer/approuver les demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="8857c-167">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="8857c-168">Demande d’autorisation élévation pour exécuter des tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="8857c-168">Requesting elevation authorization to execute privileged tasks</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-169">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-169">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-170">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8857c-170">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="8857c-171">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-172">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="8857c-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="8857c-p109">Sélectionnez **nouvelle demande**. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="8857c-p109">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="8857c-175">**Type de demande**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="8857c-175">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="8857c-176">**Étendue de demande**: Exchange</span><span class="sxs-lookup"><span data-stu-id="8857c-176">**Request scope**: Exchange</span></span>

    <span data-ttu-id="8857c-177">**Demande de**: sélectionnez dans les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="8857c-177">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="8857c-178">**Durée (en heures)**: nombre d’heures d’accès demandé</span><span class="sxs-lookup"><span data-stu-id="8857c-178">**Duration (hours)**: Number of hours of requested access</span></span>

    <span data-ttu-id="8857c-179">**Commentaires**: champ de texte pour les commentaires relatifs à votre demande d’accès</span><span class="sxs-lookup"><span data-stu-id="8857c-179">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="8857c-p110">Sélectionnez **Enregistrer** , puis sur **Fermer**. Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8857c-p110">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-182">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-182">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-183">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d’approbation au groupe de l’approbateur :</span><span class="sxs-lookup"><span data-stu-id="8857c-183">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="8857c-184">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-184">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="8857c-185">Afficher l’état des demandes d’élévation</span><span class="sxs-lookup"><span data-stu-id="8857c-185">View status of elevation requests</span></span>
<span data-ttu-id="8857c-186">Après la création d’une demande d’approbation, état de la demande l’élévation peut être consulté dans le centre d’administration ou dans Exchange Management PowerShell à l’aide d’associé avec demande de code.</span><span class="sxs-lookup"><span data-stu-id="8857c-186">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-187">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-187">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-188">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8857c-188">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="8857c-189">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-189">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-190">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="8857c-190">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="8857c-191">Sélectionnez **Afficher** demandes soumises à l’état **en attente**, **approuvé**, **refusé**ou **Zone de sécurité client** .</span><span class="sxs-lookup"><span data-stu-id="8857c-191">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-192">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-192">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-193">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher un état de la demande d’approbation pour un ID de demande spécifique :</span><span class="sxs-lookup"><span data-stu-id="8857c-193">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="8857c-194">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-194">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="8857c-195">L’approbation d’une demande d’autorisation de l’élévation</span><span class="sxs-lookup"><span data-stu-id="8857c-195">Approving an elevation authorization request</span></span>
<span data-ttu-id="8857c-p111">Lors de la création d’une demande d’approbation, les membres du groupe pertinents approbateur reçoivent une notification par courrier électronique et peuvent approuver la requête associée à l’ID de demande. Le demandeur sera averti de l’approbation de la demande ou de refus via le message électronique.</span><span class="sxs-lookup"><span data-stu-id="8857c-p111">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-198">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-198">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-199">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8857c-199">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="8857c-200">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-200">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-201">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="8857c-201">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="8857c-202">Sélectionnez une demande de liste pour afficher les détails et d’effectuer une action sur la demande.</span><span class="sxs-lookup"><span data-stu-id="8857c-202">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="8857c-p112">Sélectionnez **Approuver** pour approuver la demande ou **Refuser** pour refuser la demande. Précédemment demandes approuvées peuvent avoir accès révoqué en sélectionnant **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="8857c-p112">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-205">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-205">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-206">Exécutez la commande suivante dans Exchange Online PowerShell pour approuver une demande d’autorisation élévation :</span><span class="sxs-lookup"><span data-stu-id="8857c-206">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="8857c-207">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-207">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="8857c-208">Exécutez la commande suivante dans Exchange Online PowerShell pour refuser une demande d’autorisation élévation :</span><span class="sxs-lookup"><span data-stu-id="8857c-208">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="8857c-209">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8857c-209">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="8857c-210">Désactiver l’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8857c-210">Disable privileged access in Office 365</span></span>

<span data-ttu-id="8857c-p113">Si nécessaire, vous pouvez désactiver la gestion de l’accès privilégié pour votre organisation. Désactivation des privilèges access ne supprime pas des stratégies d’approbation associées ou des groupes de l’approbateur.</span><span class="sxs-lookup"><span data-stu-id="8857c-p113">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="8857c-213">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8857c-213">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="8857c-214">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8857c-214">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="8857c-215">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="8857c-215">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="8857c-216">Activer le contrôle **nécessitent des autorisations d’accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="8857c-216">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="8857c-217">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="8857c-217">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="8857c-218">Exécutez la commande suivante dans Exchange Online Powershell pour désactiver l’accès privilégié :</span><span class="sxs-lookup"><span data-stu-id="8857c-218">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```