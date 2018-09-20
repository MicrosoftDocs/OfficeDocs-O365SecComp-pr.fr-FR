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
ms.openlocfilehash: b2b6ab18687617c0da3425f4ee60cf81074f6f69
ms.sourcegitcommit: 15dfa0c83aa88816c18e30a44a49e36e733d952c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2018
ms.locfileid: "24021399"
---
# <a name="configuring-privileged-access-management-in-office-365"></a>Configuration de la gestion accès privilégié dans Office 365

> [!IMPORTANT]
> Cette rubrique traite des instructions de déploiement et de configuration pour les fonctionnalités uniquement actuellement disponibles dans Office 365 E5 et références de conformité avancées.

Cette rubrique vous guide par le biais de l’activation et la configuration de gestion de l’accès privilégié dans votre organisation Office 365. Vous pouvez utiliser le centre d’administration de Microsoft 365 les Exchange Management PowerShell pour gérer et utiliser un accès privilégié. 

## <a name="enable-and-configure-privileged-access-management"></a>Activer et configurer la gestion des accès privilégié

Suivez ces étapes pour configurer et utiliser un accès privilégié dans votre organisation Office 365 :

- [Étape 1 : Créer le groupe d’approbateur](privileged-access-management-configuration.md#step1)

    Avant de commencer à l’aide de privilège d’accès, déterminer ayant autorité d’approbation pour les demandes entrantes pour l’accès aux tâches avec des privilèges élevés et privilégiés. Tout utilisateur qui fait partie du groupe des approbateurs sera en mesure d’approuver les demandes d’accès. Cette option est activée en créant un groupe de sécurité à extension messagerie dans Office 365.

- [Étape 2 : Activer l’accès privilégié](privileged-access-management-configuration.md#step2)

    Accès privilégié doit être activé explicitement dans Office 365 avec le groupe d’approbateur par défaut et y compris un ensemble de comptes système que vous souhaitez exclure le contrôle d’accès de gestion des accès privilégié.

- [Étape 3 : Créer une stratégie d’accès](privileged-access-management-configuration.md#step3)

    Création d’une stratégie d’approbation vous permet de définir les exigences spécifiques limitées à des tâches spécifiques. Les options de type approbation sont **automatique** ou **manuel**.

- [Étape 4 : Envoyer/approuver les demandes d’accès privilégié](privileged-access-management-configuration.md#step4)

    Une fois activée, privilégié access nécessite approbations pour l’exécution de toute tâche qui dispose d’une stratégie d’approbation associé définie. Les utilisateurs qui ont besoin exécuter des tâches incluses dans l’une stratégie d’approbation doit demander et avoir approbation d’accès afin de disposer des autorisations nécessaires pour exécuter la tâche.

Une fois l’approbation est accordée, l’utilisateur peut exécuter la tâche souhaitée et accès privilégié seront autoriser et exécuter la tâche de la part des utilisateurs. L’approbation restera valide pour le demandé durée (durée par défaut est de 4 heures) pendant laquelle le demandeur peut exécuter la tâche prévue à plusieurs reprises. Toutes ces exécutions sont connectées et mises à disposition pour la sécurité et d’audit de conformité. 

> [!NOTE]
> Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l’accès privilégié, suivez les étapes [se connecter à Exchange Online PowerShell à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour se connecter à Exchange Online PowerShell avec Office 365 informations d’identification. Il est inutile d’activer l’authentification multifacteur pour votre organisation Office 365 les étapes permettant d’activer l’accès privilégié lors de la connexion à Exchange Online PowerShell. Établir une connexion avec l’authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.

<a name="step1"> </a>

## <a name="step-1---create-an-approvers-group"></a>Étape 1 : créer le groupe d’approbateur

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.

2. Dans le centre d’administration, accédez à **groupes** > **Ajouter un groupe**.

3. Sélectionnez le type de groupe du **groupe de sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie de groupe**et **Description** pour le nouveau groupe.

4. Enregistrez le groupe. Il peut prendre quelques minutes pour le groupe pour être entièrement configuré et apparaissent dans le centre d’administration d’Office 365.

5. Sélectionnez groupe de l’approbateur nouveau et sélectionnez **Modifier** pour ajouter des utilisateurs au groupe.

6. Enregistrez le groupe.

<a name="step2"> </a>

## <a name="step-2---enable-privileged-access"></a>Étape 2 : activer l’accès privilégié

### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.

2. Dans le centre d’administration, accédez à **Paramètres > sécurité et confidentialité** > **accès privilégié**.

3. Activer le contrôle **nécessitent des autorisations d’accès privilégié** .

4. Affectez groupe de l’approbateur que vous avez créé à l’étape 1 en tant qu' **approbateurs groupe par défaut**.

5. **Enregistrer** et **Fermer**.

### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour activer l’accès privilégié et à affecter à groupe de l’approbateur :
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
Exemple :
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> Comptes système fonctionnalité sera disponible pour s’assurer de certains automatisations au sein de votre organisation peuvent travailler sans dépendance sur un accès privilégié, mais il est recommandé que ces exclusions exceptionnelles et ceux autorisés doivent être approuvés et audit régulièrement.

<a name="step3"> </a>

## <a name="step-3---create-an-access-policy"></a>Étape 3 : créer une stratégie d’accès

### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.

2. Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.

3. Sélectionnez **Gérer les stratégies d’accès et les demandes**.

4. Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.

5. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :
    
    **Type de stratégie**: tâche, rôle ou groupe de rôles

    **Étendue de la stratégie**: Exchange ou Office 365

    **Nom de la stratégie**: sélectionnez dans les stratégies disponibles

    **Type d’approbation**: manuelle ou automatique

    **Groupe d’approbation**: sélectionnez le groupe approbateurs créé à l’étape 1

6. Sélectionnez **créer** , puis sur **Fermer**. Il peut prendre quelques minutes pour la stratégie soit entièrement configuré et activé.

### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour créer et définir une stratégie d’approbation :

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
Exemple :
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<a name="step4"> </a>

## <a name="step-4-submitapprove-privileged-access-requests"></a>Étape 4 : Envoyer/approuver les demandes d’accès privilégié

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a>Demande d’autorisation élévation pour exécuter des tâches privilégiées

#### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.

2. Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.

3. Sélectionnez **Gérer les stratégies d’accès et les demandes**.

4. Sélectionnez **nouvelle demande**. Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :

    **Type de demande**: tâche, rôle ou groupe de rôles

    **Étendue de demande**: Exchange

    **Demande de**: sélectionnez dans les stratégies disponibles

    **Durée (en heures)**: nombre d’heures d’accès demandé

    **Commentaires**: champ de texte pour les commentaires relatifs à votre demande d’accès

5. Sélectionnez **Enregistrer** , puis sur **Fermer**. Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.

#### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d’approbation au groupe de l’approbateur :
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
Exemple :
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a>Afficher l’état des demandes d’élévation
Après la création d’une demande d’approbation, état de la demande l’élévation peut être consulté dans le centre d’administration ou dans Exchange Management PowerShell à l’aide d’associé avec demande de code.

#### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.

2. Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.

3. Sélectionnez **Gérer les stratégies d’accès et les demandes**.

4. Sélectionnez **Afficher** demandes soumises à l’état **en attente**, **approuvé**, **refusé**ou **Zone de sécurité client** .

#### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour afficher un état de la demande d’approbation pour un ID de demande spécifique :
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
Exemple :
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a>L’approbation d’une demande d’autorisation de l’élévation
Lors de la création d’une demande d’approbation, les membres du groupe pertinents approbateur reçoivent une notification par courrier électronique et peuvent approuver la requête associée à l’ID de demande.

#### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide de vos informations d’identification.

2. Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.

3. Sélectionnez **Gérer les stratégies d’accès et les demandes**.

4. Sélectionnez une demande de liste pour afficher les détails et d’effectuer une action sur la demande.

5. Sélectionnez **Approuver** pour approuver la demande ou **Refuser** pour refuser la demande. Précédemment demandes approuvées peuvent avoir accès révoqué en sélectionnant **Annuler**.

#### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online PowerShell pour approuver une demande d’autorisation élévation :

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
Exemple :
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

Exécutez la commande suivante dans Exchange Online PowerShell pour refuser une demande d’autorisation élévation :

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
Exemple :
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a>Désactiver l’accès privilégié dans Office 365

Si nécessaire, vous pouvez désactiver la gestion de l’accès privilégié pour votre organisation. Désactivation des privilèges access ne supprime pas des stratégies d’approbation associées ou des groupes de l’approbateur.

### <a name="using-the-microsoft-365-admin-center"></a>À l’aide du centre d’administration Microsoft 365

1. Connectez-vous au [Centre d’administration de Microsoft 365](https://portal.office.com) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation.

2. Dans le centre d’administration, cliquez sur **paramètres** > **sécurité et confidentialité** > **accès privilégié**.

3. Activer le contrôle **nécessitent des autorisations d’accès privilégié** .

### <a name="using-exchange-management-powershell"></a>À l’aide d’Exchange Management PowerShell

Exécutez la commande suivante dans Exchange Online Powershell pour désactiver l’accès privilégié :

```
Disable-ElevatedAccessControl
```