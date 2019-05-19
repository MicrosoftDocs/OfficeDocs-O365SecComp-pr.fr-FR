---
title: Gestion des groupes dans Exchange Online Protection (EOP)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes.
ms.openlocfilehash: 090f76d034dcdcbc774666830fd0cbc54815f8c0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153136"
---
# <a name="manage-groups-in-eop"></a>Gestion des groupes dans Exchange Online Protection (EOP)

 Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes. Vous pouvez créer des groupes de distribution et des groupes de sécurité, en fonction de vos besoins. Ces groupes peuvent être créés à l'aide du Centre d'administration Exchange (CAE) ou via Windows PowerShell à distance. 
  
## <a name="types-of-mail-enabled-groups"></a>Types de groupe à extension messagerie

Vous pouvez créer deux types de groupes pour votre organisation Exchange :
  
- Les [Créer un groupe dans le CAE](manage-groups-in-eop.md) (également appelés groupes de distribution) sont des ensembles d'utilisateurs de messagerie, tels qu'une équipe ou un autre groupe ad hoc, qui ont besoin de recevoir ou d'envoyer des messages électroniques au sujet d'un domaine d'intérêt commun. Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques. Dans EOP, un groupe de distribution fait référence à n'importe quel groupe à extension messagerie, qu'il dispose ou non d'un contexte de sécurité.
    
- Les [Modifier ou supprimer un groupe dans le CAE](manage-groups-in-eop.md) (également appelés groupes de sécurité) sont des ensembles d'utilisateurs de messagerie qui ont besoin d'autorisations d'accès pour les rôles d'administrateur. Par exemple, vous voudrez peut-être accorder à un groupe spécifique d'utilisateurs des autorisations de rôle d'administrateur afin qu'ils puissent configurer des paramètres de blocage du courrier indésirable et des programmes malveillants.
    
    > [!NOTE]
    > Par défaut, tous les nouveaux groupes de sécurité à extension messagerie exigent que tous les expéditeurs soient identifiés. En procédant de la sorte, les expéditeurs externes ne peuvent pas envoyer de messages aux groupes de sécurité à extension messagerie. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Groupes de distribution et groupes de sécurité » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md). 
    
- Sachez que lors de la création et de la gestion des groupes avec les cmdlets PowerShell à distance, vous pouvez être confronté à des limitations.
    
- Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.
    
- Pour découvrir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online Protection à l'aide d'une session PowerShell distante](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="create-a-group-in-the-eac"></a>Créer un groupe dans le CAE

1. Dans le Centre d'administration Exchange (CAE), accédez à **Destinataires** \> **Groupes**.
    
2. Cliquez sur **Nouveau**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif), puis sur **Groupe de distribution** ou sur **Groupe de sécurité**, en fonction de vos besoins. Consultez l'article [Types de groupe à extension messagerie](manage-groups-in-eop.md) pour comprendre la distinction. 
    
3. Sur la page **Nouveau groupe de distribution** ou **Nouveau groupe de sécurité**, renseignez les champs suivants : 
    
  - **Nom complet** Saisissez le nom complet du groupe. Il doit être propre à votre organisation et avoir du sens pour les utilisateurs EOP. Le nom complet est requis. 
    
  - **Alias** Saisissez l'alias du groupe. Il doit comporter 64 caractères maximum et être propre à votre organisation. Les utilisateurs EOP saisissent l'alias dans le champ À : d'un message électronique et l'alias génère le nom complet du groupe. Si vous modifiez l'alias, l'adresse SMTP principale du groupe est également modifiée et contient le nouvel alias. L'alias est obligatoire. 
    
  - **Description** Saisissez la description du groupe afin d'informer d'autres personnes du but du groupe. 
    
  - **Propriétaires** Par défaut, la personne qui crée un groupe en est le propriétaire. Vous pouvez ajouter un propriétaire en cliquant sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif). Tous les groupes doivent avoir au moins un propriétaire.
    
    > [!NOTE]
    > Les propriétaires des groupes ne doivent pas nécessairement en être membres. 
  
  - **Membres** Utilisez cette section pour ajouter des membres au groupe et pour spécifier si une approbation est nécessaire pour que des personnes rejoignent ou quittent le groupe. Pour ajouter des membres au groupe, cliquez sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif).
    
4. Cliquez sur **OK** pour revenir à la page d'origine. 
    
5. Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe. Le nouveau groupe doit apparaître dans la liste des groupes. 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a>Modifier ou supprimer un groupe dans le CAE

1. Dans le CAE, accédez à **Destinataires** \> **Groupes**.
    
2. Effectuez l'une des opérations suivantes :
    
  - Pour modifier un groupe: dans la liste des groupes, cliquez sur le groupe de distribution ou de sécurité que vous souhaitez afficher ou modifier, puis **** ![cliquez sur modifier](../media/ITPro-EAC-EditIcon.gif)l’icône de modification. Vous pouvez mettre à jour les paramètres généraux, ajouter ou supprimer des propriétaires du groupe, et ajouter ou supprimer des membres du groupe, selon vos besoins.
    
  - Pour supprimer un groupe : Sélectionnez le groupe et cliquez sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif).
    
3. Après avoir effectué toutes les modifications voulues, cliquez sur **Enregistrer**.
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a>Créer, modifier ou supprimer un groupe à l’aide de Windows PowerShell à distance

Cette section fournit des informations sur la création de groupes et la modification de leurs propriétés à l’aide de Windows PowerShell à distance. Elle explique également comment supprimer un groupe existant. 
  
 **Pour créer un groupe à l'aide de Windows PowerShell à distance**
  
Cet exemple utilise la cmdlet [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) pour créer un groupe de distribution avec l'alias itadmin et le nom IT Administrators. Il ajoute également des utilisateurs en tant que membres du groupe. 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

Pour créer un groupe de sécurité et non un groupe de distribution, spécifiez  `-Type "Security"` à la place. 
  
Pour vérifier que vous avez créé avec succès le groupe IT Administrators, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour afficher les informations sur le nouveau groupe : 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

Pour obtenir la liste des membres du groupe, exécutez la cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) comme suit : 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

Pour obtenir la liste complète de tous vos groupes, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit : 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 **Pour modifier les propriétés d'un groupe à l'aide de Windows PowerShell à distance**
  
Utilisez les cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) et [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) pour afficher et modifier les propriétés des groupes. L'utilisation de PowerShell à distance, contrairement au CAE, vous permet de modifier les propriétés de plusieurs groupes. 
  
Voici quelques exemples d'utilisation de Windows PowerShell à distance pour modifier les propriétés de groupe.
  
Cet exemple utilise la cmdlet [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) pour modifier l'adresse SMTP principale (également appelée l'adresse de réponse) pour le groupe Seattle Employees en sea.employees@contoso.com. 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

Pour vérifier que vous avez modifié avec succès les propriétés d'un groupe, utilisez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour contrôler les modifications. L'utilisation de PowerShell à distance présente l'avantage de pouvoir afficher plusieurs propriétés de plusieurs groupes. Dans l'exemple ci-dessus, où le groupe d'adresses SMTP principal a été modifié, exécutez la commande suivante pour vérifier la nouvelle valeur : 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

Cet exemple utilise la cmdlet [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) pour mettre à jour tous les membres du groupe Seattle Employees. Utilisez des virgules pour séparer tous les membres. 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

Pour obtenir la liste de tous les membres du groupe Seattle Employees, utilisez la cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) comme suit : 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 **Pour supprimer un groupe à l'aide de Windows PowerShell à distance**
  
Cet exemple utilise la cmdlet [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) pour supprimer un groupe de distribution nommé IT Administrators. 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

Pour vérifier que le groupe a été supprimé, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit, et confirmez que le groupe (dans ce cas, IT Administrators) a été supprimé. 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


