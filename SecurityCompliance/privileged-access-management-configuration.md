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
ms.openlocfilehash: 13d278c8e8555aa069035c2f03b23db69a475b43
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522255"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="624e4-103">Configuration de la gestion accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="624e4-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="624e4-104">Cette rubrique traite des instructions de déploiement et de configuration pour les fonctionnalités uniquement actuellement disponibles dans Office 365 E5 et références de conformité avancées.</span><span class="sxs-lookup"><span data-stu-id="624e4-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="624e4-p101">Cette rubrique vous guide par le biais de l’activation et la configuration de gestion de l’accès privilégié dans votre organisation Office 365. Vous pouvez utiliser soit le centre d’administration de Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser un accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="624e4-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="624e4-107">Activer et configurer la gestion des accès privilégié</span><span class="sxs-lookup"><span data-stu-id="624e4-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="624e4-108">Suivez ces étapes pour configurer et utiliser un accès privilégié dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="624e4-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="624e4-109">Étape 1 : Créer le groupe d’approbateur</span><span class="sxs-lookup"><span data-stu-id="624e4-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="624e4-p102">Avant de commencer à l’aide de privilège d’accès, déterminer ayant autorité d’approbation pour les demandes entrantes pour l’accès aux tâches avec des privilèges élevés et privilégiés. Tout utilisateur qui fait partie du groupe des approbateurs sera en mesure d’approuver les demandes d’accès. Cette option est activée en créant un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="624e4-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="624e4-113">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="624e4-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="624e4-114">Accès privilégié doit être activé explicitement dans Office 365 avec le groupe d’approbateur par défaut et y compris un ensemble de comptes système que vous souhaitez exclure le contrôle d’accès de gestion des accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="624e4-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="624e4-115">Étape 3 : Créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="624e4-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="624e4-p103">Création d’une stratégie d’approbation vous permet de définir les exigences spécifiques limitées à des tâches spécifiques. Les options de type approbation sont **automatique** ou **manuel**.</span><span class="sxs-lookup"><span data-stu-id="624e4-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="624e4-118">Étape 4 : Envoyer/approuver les demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="624e4-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="624e4-p104">Une fois activée, privilégié access nécessite approbations pour l’exécution de toute tâche qui dispose d’une stratégie d’approbation associé définie. Les utilisateurs qui ont besoin exécuter des tâches incluses dans l’une stratégie d’approbation doit demander et avoir approbation d’accès afin de disposer des autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="624e4-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="624e4-p105">Une fois l’approbation est accordée, l’utilisateur peut exécuter la tâche souhaitée et accès privilégié seront autoriser et exécuter la tâche de la part des utilisateurs. L’approbation restera valide pour le demandé durée (durée par défaut est de 4 heures) pendant laquelle le demandeur peut exécuter la tâche prévue à plusieurs reprises. Toutes ces exécutions sont connectées et mises à disposition pour la sécurité et d’audit de conformité.</span><span class="sxs-lookup"><span data-stu-id="624e4-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="624e4-p106">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l’accès privilégié, suivez les étapes [se connecter à Exchange Online PowerShell à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour se connecter à Exchange Online PowerShell avec Office 365 informations d’identification. Il est inutile d’activer l’authentification multifacteur pour votre organisation Office 365 les étapes permettant d’activer l’accès privilégié lors de la connexion à Exchange Online PowerShell. Établir une connexion avec l’authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.</span><span class="sxs-lookup"><span data-stu-id="624e4-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="624e4-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="624e4-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="624e4-128">Étape 1 : créer le groupe d’approbateur</span><span class="sxs-lookup"><span data-stu-id="624e4-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="624e4-129">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="624e4-130">Dans le centre d’administration, accédez à **groupes** > **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="624e4-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="624e4-131">Sélectionnez le type de groupe du **groupe de sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie de groupe**et **Description** pour le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="624e4-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="624e4-p107">Enregistrez le groupe. Il peut prendre quelques minutes pour le groupe pour être entièrement configuré et apparaissent dans le centre d’administration d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="624e4-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="624e4-134">Sélectionnez groupe de l’approbateur nouveau et sélectionnez **Modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="624e4-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="624e4-135">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="624e4-135">Save the group.</span></span>

<span data-ttu-id="624e4-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="624e4-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="624e4-137">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="624e4-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-138">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-139">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="624e4-140">Dans le centre d’administration, accédez à **Paramètres > sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-141">Activer le contrôle **nécessitent des autorisations d’accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="624e4-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="624e4-142">Affectez groupe de l’approbateur que vous avez créé à l’étape 1 en tant qu' **approbateurs groupe par défaut**.</span><span class="sxs-lookup"><span data-stu-id="624e4-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="624e4-143">**Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="624e4-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-144">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-145">Exécutez la commande suivante dans Exchange Online PowerShell pour activer l’accès privilégié et à affecter à groupe de l’approbateur :</span><span class="sxs-lookup"><span data-stu-id="624e4-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="624e4-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="624e4-147">Comptes système fonctionnalité sera disponible pour s’assurer de certains automatisations au sein de votre organisation peuvent travailler sans dépendance sur un accès privilégié, mais il est recommandé que ces exclusions exceptionnelles et ceux autorisés doivent être approuvés et audit régulièrement.</span><span class="sxs-lookup"><span data-stu-id="624e4-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="624e4-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="624e4-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="624e4-149">Étape 3 : créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="624e4-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="624e4-150">Vous pouvez créer et configurer des stratégies d’accès privilégié jusqu'à 30 pour votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="624e4-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-151">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-152">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="624e4-153">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-154">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="624e4-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="624e4-155">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="624e4-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="624e4-156">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="624e4-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="624e4-157">**Type de stratégie**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="624e4-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="624e4-158">**Étendue de la stratégie**: Exchange ou Office 365</span><span class="sxs-lookup"><span data-stu-id="624e4-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="624e4-159">**Nom de la stratégie**: sélectionnez dans les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="624e4-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="624e4-160">**Type d’approbation**: manuelle ou automatique</span><span class="sxs-lookup"><span data-stu-id="624e4-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="624e4-161">**Groupe d’approbation**: sélectionnez le groupe approbateurs créé à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="624e4-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="624e4-p108">Sélectionnez **créer** , puis sur **Fermer**. Il peut prendre quelques minutes pour la stratégie soit entièrement configuré et activé.</span><span class="sxs-lookup"><span data-stu-id="624e4-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-164">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-165">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et définir une stratégie d’approbation :</span><span class="sxs-lookup"><span data-stu-id="624e4-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="624e4-166">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="624e4-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="624e4-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="624e4-168">Étape 4 : Envoyer/approuver les demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="624e4-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="624e4-169">Demande d’autorisation élévation pour exécuter des tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="624e4-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="624e4-p109">Demandes d’accès privilégié valent jusqu'à 24 heures après que la demande est envoyée. Si non approuvé ou refusé, les demandes d’expirent et access n’est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="624e4-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-172">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-173">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="624e4-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="624e4-174">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-175">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="624e4-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="624e4-p110">Sélectionnez **nouvelle demande**. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="624e4-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="624e4-178">**Type de demande**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="624e4-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="624e4-179">**Étendue de demande**: Exchange</span><span class="sxs-lookup"><span data-stu-id="624e4-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="624e4-180">**Demande de**: sélectionnez dans les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="624e4-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="624e4-p111">**Durée (en heures)**: nombre d’heures d’accès demandé. Il n’est pas une limite sur le nombre d’heures qui peut être demandée.</span><span class="sxs-lookup"><span data-stu-id="624e4-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="624e4-183">**Commentaires**: champ de texte pour les commentaires relatifs à votre demande d’accès</span><span class="sxs-lookup"><span data-stu-id="624e4-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="624e4-p112">Sélectionnez **Enregistrer** , puis sur **Fermer**. Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="624e4-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-186">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-187">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d’approbation au groupe de l’approbateur :</span><span class="sxs-lookup"><span data-stu-id="624e4-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="624e4-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="624e4-189">Afficher l’état des demandes d’élévation</span><span class="sxs-lookup"><span data-stu-id="624e4-189">View status of elevation requests</span></span>
<span data-ttu-id="624e4-190">Après la création d’une demande d’approbation, état de la demande l’élévation peut être consulté dans le centre d’administration ou dans Exchange Management PowerShell à l’aide d’associé avec demande de code.</span><span class="sxs-lookup"><span data-stu-id="624e4-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-191">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-192">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="624e4-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="624e4-193">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-194">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="624e4-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="624e4-195">Sélectionnez **Afficher** demandes soumises à l’état **en attente**, **approuvé**, **refusé**ou **Zone de sécurité client** .</span><span class="sxs-lookup"><span data-stu-id="624e4-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-196">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-197">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher un état de la demande d’approbation pour un ID de demande spécifique :</span><span class="sxs-lookup"><span data-stu-id="624e4-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="624e4-198">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="624e4-199">L’approbation d’une demande d’autorisation de l’élévation</span><span class="sxs-lookup"><span data-stu-id="624e4-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="624e4-p113">Lors de la création d’une demande d’approbation, les membres du groupe pertinents approbateur reçoivent une notification par courrier électronique et peuvent approuver la requête associée à l’ID de demande. Le demandeur sera averti de l’approbation de la demande ou de refus via le message électronique.</span><span class="sxs-lookup"><span data-stu-id="624e4-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-202">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-203">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="624e4-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="624e4-204">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-205">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="624e4-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="624e4-206">Sélectionnez une demande de liste pour afficher les détails et d’effectuer une action sur la demande.</span><span class="sxs-lookup"><span data-stu-id="624e4-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="624e4-p114">Sélectionnez **Approuver** pour approuver la demande ou **Refuser** pour refuser la demande. Précédemment demandes approuvées peuvent avoir accès révoqué en sélectionnant **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="624e4-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-209">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-210">Exécutez la commande suivante dans Exchange Online PowerShell pour approuver une demande d’autorisation élévation :</span><span class="sxs-lookup"><span data-stu-id="624e4-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="624e4-211">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="624e4-212">Exécutez la commande suivante dans Exchange Online PowerShell pour refuser une demande d’autorisation élévation :</span><span class="sxs-lookup"><span data-stu-id="624e4-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="624e4-213">Exemple :</span><span class="sxs-lookup"><span data-stu-id="624e4-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="624e4-214">Supprimer une stratégie d’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="624e4-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="624e4-215">Vous pouvez supprimer une stratégie d’accès privilégié si elle n’est plus nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-216">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-217">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="624e4-218">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-219">Sélectionnez **Gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="624e4-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="624e4-220">Sélectionnez **la configuration des stratégies**.</span><span class="sxs-lookup"><span data-stu-id="624e4-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="624e4-221">Sélectionnez la stratégie que vous souhaitez supprimer, puis sélectionnez **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="624e4-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="624e4-222">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="624e4-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-223">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-224">Exécutez la commande suivante dans Exchange Online Powershell pour supprimer une stratégie d’accès privilégié :</span><span class="sxs-lookup"><span data-stu-id="624e4-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="624e4-225">Désactiver l’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="624e4-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="624e4-p115">Si nécessaire, vous pouvez désactiver la gestion de l’accès privilégié pour votre organisation. Désactivation des privilèges access ne supprime pas des stratégies d’approbation associées ou des groupes de l’approbateur.</span><span class="sxs-lookup"><span data-stu-id="624e4-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="624e4-228">À l’aide du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="624e4-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="624e4-229">Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="624e4-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="624e4-230">Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.</span><span class="sxs-lookup"><span data-stu-id="624e4-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="624e4-231">Activer le contrôle **nécessitent des autorisations d’accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="624e4-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="624e4-232">À l’aide d’Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="624e4-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="624e4-233">Exécutez la commande suivante dans Exchange Online Powershell pour désactiver l’accès privilégié :</span><span class="sxs-lookup"><span data-stu-id="624e4-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```