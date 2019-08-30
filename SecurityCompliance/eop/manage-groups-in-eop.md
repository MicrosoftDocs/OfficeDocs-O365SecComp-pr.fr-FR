---
title: Gestion des groupes dans Exchange Online Protection (EOP)
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes.
ms.openlocfilehash: 9ce501c5d51561a7be86963ae98b62046995e46f
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676734"
---
# <a name="manage-groups-in-eop"></a>Gestion des groupes dans Exchange Online Protection (EOP)

 Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes. Vous pouvez créer des groupes de distribution et des groupes de sécurité, en fonction de vos besoins. Ces groupes peuvent être créés à l'aide du Centre d'administration Exchange (CAE) ou via Windows PowerShell à distance.
  
## <a name="types-of-mail-enabled-groups"></a>Types de groupe à extension messagerie

Vous pouvez créer deux types de groupes pour votre organisation Exchange :
  
- Les groupes de distribution sont des collections d’utilisateurs de messagerie, tels qu’une équipe ou un autre groupe ad hoc, qui doivent recevoir ou envoyer des courriers électroniques concernant un domaine d’intérêt commun. Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques. Dans EOP, un groupe de distribution fait référence à n'importe quel groupe à extension messagerie, qu'il dispose ou non d'un contexte de sécurité.

- Les groupes de sécurité sont des collections d’utilisateurs de messagerie qui ont besoin d’autorisations d’accès pour les rôles d’administrateur. Par exemple, vous voudrez peut-être accorder à un groupe spécifique d'utilisateurs des autorisations de rôle d'administrateur afin qu'ils puissent configurer des paramètres de blocage du courrier indésirable et des programmes malveillants.

    > [!NOTE]
    > Par défaut, tous les nouveaux groupes de sécurité à extension messagerie exigent que tous les expéditeurs soient identifiés. En procédant de la sorte, les expéditeurs externes ne peuvent pas envoyer de messages aux groupes de sécurité à extension messagerie.
  
## <a name="before-you-begin"></a>Avant de commencer

- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Groupes de distribution et groupes de sécurité » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).

- Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).

- N’oubliez pas que lors de la création et de la gestion des groupes à l’aide des cmdlets PowerShell d’Exchange Online Protection, vous pouvez rencontrer des limitations.

- Les procédures PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.

- Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).

- Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).

> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) . 
  
## <a name="create-a-group-in-the-eac"></a>Créer un groupe dans le CAE

1. Dans le CAE, accédez à **Destinataires** \> **Groupes**.

2. Cliquez sur **nouvelle** ![icône](../media/ITPro-EAC-AddIcon.gif)ajouter, puis sur **groupe de distribution** ou groupe de **sécurité**, en fonction de vos besoins.

3. Sur la page **nouveau groupe de distribution** ou **nouveau groupe de sécurité** , configurez les paramètres suivants:

   - **Nom d’affichage**: tapez un nom d’affichage propre à votre organisation et pertinent pour les utilisateurs EOP. Le nom complet est requis.

   - **Alias**: tapez un alias de groupe de jusqu’à 64 caractères qui sont propres à votre organisation. Les utilisateurs EOP tapent l’alias dans la ligne à: des messages électroniques et l’alias est résolu en nom complet du groupe. Si vous modifiez l’alias, l’adresse SMTP principale du groupe est également modifiée et contiendra le nouvel alias. L'alias est un champ obligatoire. 

   - **Description**: tapez une description du groupe afin que les utilisateurs connaissent l’objectif du groupe. 

   - **Propriétaires**: par défaut, la personne qui crée le groupe est le propriétaire. Vous pouvez ajouter un propriétaire en sélectionnant **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter. Tous les groupes doivent avoir au moins un propriétaire.

     > [!NOTE]
     > Les propriétaires des groupes ne doivent pas nécessairement en être membres.
  
   - **Membres**: utilisez cette section pour ajouter des membres du groupe et pour spécifier si une approbation est requise pour que des personnes puissent rejoindre ou quitter le groupe. Pour ajouter des membres au groupe, cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter.

4. Cliquez sur **OK** pour revenir à la page d'origine.

5. Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe. Le nouveau groupe doit apparaître dans la liste des groupes.

## <a name="edit-or-remove-a-group-in-the-eac"></a>Modifier ou supprimer un groupe dans le CAE

1. Dans le CAE, accédez à **Destinataires** \> **Groupes**.

2. Effectuez l'une des étapes suivantes :

   - Pour modifier un groupe: dans la liste des groupes, cliquez sur le groupe que vous souhaitez afficher ou modifier, puis cliquez sur **modifier** ![l’icône](../media/ITPro-EAC-EditIcon.gif)modifier. Vous pouvez mettre à jour les paramètres généraux, ajouter ou supprimer des propriétaires de groupes, et ajouter ou supprimer des membres du groupe selon vos besoins.

   - Pour supprimer un groupe: sélectionnez le groupe, puis **** ![cliquez sur supprimer](../media/ITPro-EAC-RemoveIcon.gif)l’icône Supprimer.

3. Après avoir effectué toutes les modifications voulues, cliquez sur **Enregistrer**.

## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>Créer, modifier ou supprimer un groupe à l’aide de Windows PowerShell à distance

Cette section fournit des informations sur la création de groupes et la modification de leurs propriétés dans Exchange Online Protection PowerShell. Elle explique également comment supprimer un groupe existant.
  
### <a name="create-a-group-using-remote-windows-powershell"></a>Créer un groupe à l’aide de Windows PowerShell à distance
  
Cet exemple utilise la cmdlet [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/New-EOPDistributionGroup) pour créer un groupe de distribution avec l'alias itadmin et le nom IT Administrators. Il ajoute également des utilisateurs en tant que membres du groupe.
  
```Powershell
New-EOPDistributionGroup -Type Distribution -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy Member1
```

**Remarque**: pour créer un groupe de sécurité au lieu d’un groupe de distribution, `Security` utilisez la valeur pour le paramètre *type* .
  
Pour vérifier que vous avez bien créé le groupe administrateurs informatiques, exécutez la commande suivante pour afficher les informations sur le nouveau groupe:
  
```Powershell
Get-Recipient "IT Administrators" | Format-List
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient).

Pour obtenir la liste des membres du groupe, exécutez la commande suivante:
  
```Powershell
Get-DistributionGroupMember "IT Administrators"
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-distributiongroupmember).

Pour obtenir la liste complète de tous vos groupes, exécutez la commande suivante:
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | Format-Table | more
```

### <a name="change-the-properties-of-a-group-using-remote-windows-powershell"></a>Modifier les propriétés d’un groupe à l’aide de Windows PowerShell à distance
  
L’utilisation de PowerShell au lieu du centre d’administration Exchange permet de modifier les propriétés de plusieurs groupes.
  
Voici quelques exemples d’utilisation d’Exchange Online Protection PowerShell pour modifier les propriétés d’un groupe.
  
Cet exemple utilise la modification de l’adresse SMTP principale (également appelée adresse de réponse) pour le groupe Seattle Employees vers sea.employees@contoso.com.
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopdistributiongroup).

Pour vérifier que vous avez bien modifié les propriétés du groupe, exécutez la commande suivante pour vérifier la nouvelle valeur:
  
```Powershell
Get-Recipient "Seattle Employees" | Format-List "PrimarySmtpAddress"
```

Cet exemple met à jour tous les membres du groupe Seattle Employees. Utilisez des virgules pour séparer tous les membres.
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Update-EOPDistributionGroupMember](https://docs.microsoft.com/en-us/powershell/module/exchange/users-and-groups/update-eopdistributiongroupmember).

Pour obtenir la liste de tous les membres du groupe Seattle Employees, exécutez la commande suivante: 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"
```

### <a name="remove-a-group-using-remote-windows-powershell"></a>Supprimer un groupe à l’aide de Windows PowerShell à distance
  
Cet exemple utilise le groupe de distribution nommé administrateurs informatiques.
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/remove-eopdistributiongroup).

Pour vérifier que le groupe a été supprimé, exécutez la commande suivante et assurez-vous que le groupe (dans ce cas administrateurs informatiques) a été supprimé.
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"
```
