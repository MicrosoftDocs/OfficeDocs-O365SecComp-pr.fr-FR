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
# <a name="configuring-privileged-access-management-in-office-365"></a>Configuration de la gestion des accès privilégiés dans Office 365

> [!IMPORTANT]
> Cette rubrique traite des conseils de déploiement et de configuration pour les fonctionnalités uniquement disponibles dans Office 365 E5 et les SKU de conformité avancée.

Cette rubrique vous guidera tout au long de l'activation et de la configuration de la gestion des accès privilégiés dans votre organisation Office 365. Vous pouvez utiliser le centre d'administration Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser l'accès privilégié. 

## <a name="enable-and-configure-privileged-access-management"></a>Activer et configurer la gestion des accès privilégiés

Procédez comme suit pour configurer et utiliser l'accès privilégié dans votre organisation Office 365:

- [Étape 1: créer un groupe d'approbateurs](privileged-access-management-configuration.md#step1)

    Avant de commencer à utiliser l'accès aux privilèges, déterminez qui disposera de l'autorité d'approbation pour les demandes entrantes d'accès à des tâches élevées et privilégiées. Tout utilisateur qui fait partie du groupe apProbateurs est en mesure d'approuver les demandes d'accès. Pour cela, vous créez un groupe de sécurité à extension messagerie dans Office 365.

- [Étape 2: activer l'accès privilégié](privileged-access-management-configuration.md#step2)

    L'accès privilégié doit être activé de manière explicite dans Office 365 avec le groupe d'approbateurs par défaut et inclure un ensemble de comptes système que vous souhaitez exclure du contrôle d'accès gestion des accès privilégiés.

- [Étape 3: créer une stratégie d'accès](privileged-access-management-configuration.md#step3)

    La création d'une stratégie d'approbation vous permet de définir les exigences d'approbation spécifiques au niveau des tâches individuelles. Les options type d'approbation sont **automatique** ou **Manuel**.

- [Étape 4: soumettre/approuver des demandes d'accès privilégié](privileged-access-management-configuration.md#step4)

    Une fois activé, l'accès privilégié nécessite des approbations pour l'exécution de n'importe quelle tâche à laquelle une stratégie d'approbation associée est définie. Les utilisateurs qui ont besoin d'exécuter des tâches incluses dans une stratégie d'approbation doivent demander l'approbation de l'accès et disposer des autorisations nécessaires pour exécuter la tâche.

Une fois que l'approbation est accordée, l'utilisateur qui a effectué la demande peut exécuter la tâche prévue et l'accès privilégié autorise et exécute la tâche au nom des utilisateurs. L'approbation reste valide pour la durée demandée (la durée par défaut est de 4 heures), pendant laquelle le demandeur peut exécuter la tâche prévue plusieurs fois. Toutes les exécutions de ce type sont enregistrées et mises à disposition pour l'audit de sécurité et de conformité. 

> [!NOTE]
> Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l'accès privilégié, suivez les étapes de la [page connexion à Exchange Online PowerShell à l'aide de l'authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour vous connecter à Exchange Online PowerShell avec votre Office 365 informations d'identification. Vous n'avez pas besoin d'activer l'authentification multifacteur pour votre organisation Office 365 pour utiliser les étapes d'activation de l'accès privilégié lors de la connexion à Exchange Online PowerShell. La connexion avec l'authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Étape 1: créer un groupe d'approbateurs

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.

2. Dans le centre d'administration, accédez à **groupes** > **Ajouter un groupe**.

3. Sélectionnez le groupe Groupe de **sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie du groupe**et **Description** pour le nouveau groupe.

4. Enregistrez le groupe. La configuration complète du groupe peut prendre quelques minutes et s'afficher dans le centre d'administration Office 365.

5. Sélectionnez le nouveau groupe approbateur et sélectionnez **modifier** pour ajouter des utilisateurs au groupe.

6. Enregistrez le groupe.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Étape 2: activation de l'accès privilégié

### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.

2. Dans le centre d'administration, accédez à **paramètres > sécurité & confidentialité** > **accès aux privilèges**.

3. Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .

4. Affectez le groupe d'approbateurs que vous avez créé à l'étape 1 comme groupe d'approbateurs **par défaut**.

5. **Enregistrer** et **Fermer**.

### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour activer l'accès privilégié et pour affecter le groupe de l'approbateur:
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
Exemple :
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> La fonctionnalité comptes système est mise à disposition pour garantir que certaines automations au sein de vos organisations peuvent fonctionner sans dépendance sur l'accès privilégié, mais il est recommandé de faire en sorte que ces exclusions soient exceptionnelles et que celles autorisées soient approuvées et vérifiées. régulièrement.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Étape 3: créer une stratégie d'accès

Vous pouvez créer et configurer jusqu'à 30 stratégies d'accès privilégié pour votre organisation Office 365.

### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Sélectionnez **gérer les stratégies d'accès et les demandes**.

4. Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.

5. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:
    
    **Type de stratégie**: tâche, rôle ou groupe de rôles

    **Étendue de stratégie**: Exchange

    **Nom**de la stratégie: sélectionnez parmi les stratégies disponibles.

    **Type d'approbation**: manuelle ou automatique

    **Groupe d'approbation**: sélectionnez le groupe approbateurs créé à l'étape 1

6. Sélectionnez **créer** , puis **Fermer**. La configuration et l'activation de la stratégie peuvent prendre quelques minutes.

### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour créer et définir une stratégie d'approbation:

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Exemple :
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Étape 4: soumettre/approuver des demandes d'accès privilégié

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Demande d'une autorisation d'élévation pour exécuter des tâches privilégiées

Les demandes d'accès privilégié sont valides jusqu'à 24 heures après l'envoi de la demande. Si elles ne sont pas approuvées ou refusées, les demandes expirent et l'accès n'est pas approuvé.

#### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Sélectionnez **gérer les stratégies d'accès et les demandes**.

4. Sélectionnez **nouvelle demande**. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation:

    **Type de demande**: tâche, rôle ou groupe de rôles

    **Étendue**de la demande: Exchange

    **Demande**: sélectionnez parmi les stratégies disponibles.

    **Durée (heures)**: nombre d'heures d'accès demandé. Il n'y a pas de limite sur le nombre d'heures qui peuvent être demandées.

    **Commentaires**: champ de texte pour les commentaires liés à votre demande d'accès

5. Sélectionnez **Enregistrer** , puis **Fermer**. Votre demande sera envoyée au groupe de l'approbateur par courrier électronique.

#### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d'approbation au groupe de l'approbateur:
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Exemple :
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Afficher l'état des demandes d'élévation
Après la création d'une demande d'approbation, l'état de la demande d'élévation peut être révisé dans le centre d'administration ou dans Exchange Management PowerShell à l'aide de l'ID de demande associé.

#### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Sélectionnez **gérer les stratégies d'accès et les demandes**.

4. Sélectionnez **affichage** pour filtrer les demandes soumises par état **en attente**, **approuvé**, **refusé**ou **référentiel sécurisé du client** .

#### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour afficher l'état d'une demande d'approbation pour un ID de demande spécifique:
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Exemple :
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>Approbation d'une demande d'autorisation d'élévation
Lorsqu'une demande d'approbation est créée, les membres du groupe d'approbateur approprié reçoivent une notification par courrier électronique et peuvent approuver la demande associée à l'ID de demande. Le demandeur est informé de l'approbation ou du refus de la demande via un message électronique.

#### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide de vos informations d'identification.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Sélectionnez **gérer les stratégies d'accès et les demandes**.

4. Sélectionnez une demande répertoriée pour afficher les détails et agir sur la demande.

5. Sélectionnez **approuver** pour approuver la demande ou **refuser** pour la refuser. Les demandes précédemment approuvées peuvent avoir un accès révoqué en sélectionnant **Revoke**.

#### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour approuver une demande d'autorisation d'élévation:

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Exemple :
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Exécutez la commande suivante dans Exchange Online PowerShell pour refuser une demande d'autorisation d'élévation:

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Exemple :
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a>Supprimer une stratégie d'accès privilégié dans Office 365
Vous pouvez supprimer une stratégie d'accès privilégié si elle n'est plus nécessaire dans votre organisation.

### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Sélectionnez **gérer les stratégies d'accès et les demandes**.

4. Sélectionnez **configurer les stratégies**.

5. Sélectionnez la stratégie à supprimer, puis **Supprimer la stratégie**.

6. Sélectionnez **Fermer**.

### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour supprimer une stratégie d'accès privilégié:

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a>DésActivation de l'accès privilégié dans Office 365

Si nécessaire, vous pouvez désactiver la gestion des accès privilégiés pour votre organisation. La désActivation de l'accès privilégié ne supprime pas les stratégies d'approbation ou les groupes d'approbateurs associés.

### <a name="using-the-microsoft-365-admin-center"></a>Utilisation du centre d'administration Microsoft 365

1. Connectez-vous au [Centre d'administration Microsoft 365](https://portal.office.com) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation.

2. Dans le centre d'administration, accédez à **paramètres** > de**sécurité & confidentialité** > des**accès privilégiés**.

3. Activez l' **autorisation exiger des approbations pour le contrôle d'accès privilégié** .

### <a name="using-exchange-management-powershell"></a>Utilisation d'Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour désactiver l'accès privilégié:

```
Disable-ElevatedAccessControl
```