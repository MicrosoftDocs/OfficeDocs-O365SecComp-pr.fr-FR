---
title: Gestion des groupes dans Exchange Online Protection (EOP)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes.
ms.openlocfilehash: 2e747dc9a26cbbc1ce214107235ccea62f175dd0
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670459"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="99237-104">Gestion des groupes dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="99237-104">Manage groups in EOP</span></span>

 <span data-ttu-id="99237-p102">Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes. Vous pouvez créer des groupes de distribution et des groupes de sécurité, en fonction de vos besoins. Ces groupes peuvent être créés à l'aide du Centre d'administration Exchange (CAE) ou via Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="99237-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span> 
  
## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="99237-109">Types de groupe à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="99237-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="99237-110">Vous pouvez créer deux types de groupes pour votre organisation Exchange :</span><span class="sxs-lookup"><span data-stu-id="99237-110">You can create two types of groups for your Exchange organization:</span></span>
  
- <span data-ttu-id="99237-p103">Les [Créer un groupe dans le CAE](manage-groups-in-eop.md) (également appelés groupes de distribution) sont des ensembles d'utilisateurs de messagerie, tels qu'une équipe ou un autre groupe ad hoc, qui ont besoin de recevoir ou d'envoyer des messages électroniques au sujet d'un domaine d'intérêt commun. Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques. Dans EOP, un groupe de distribution fait référence à n'importe quel groupe à extension messagerie, qu'il dispose ou non d'un contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="99237-p103">[Create a group in the EAC](manage-groups-in-eop.md) (also known as distribution groups) are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest. Distribution groups are exclusively for distributing email messages. In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>
    
- <span data-ttu-id="99237-p104">Les [Modifier ou supprimer un groupe dans le CAE](manage-groups-in-eop.md) (également appelés groupes de sécurité) sont des ensembles d'utilisateurs de messagerie qui ont besoin d'autorisations d'accès pour les rôles d'administrateur. Par exemple, vous voudrez peut-être accorder à un groupe spécifique d'utilisateurs des autorisations de rôle d'administrateur afin qu'ils puissent configurer des paramètres de blocage du courrier indésirable et des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="99237-p104">[Edit or remove a group in the EAC](manage-groups-in-eop.md) (also known as security groups) are collections of email users who need access permissions for Admin roles. For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="99237-p105">Par défaut, tous les nouveaux groupes de sécurité à extension messagerie exigent que tous les expéditeurs soient identifiés. En procédant de la sorte, les expéditeurs externes ne peuvent pas envoyer de messages aux groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="99237-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="99237-118">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="99237-118">Before you begin</span></span>

- <span data-ttu-id="99237-p106">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Groupes de distribution et groupes de sécurité » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="99237-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="99237-121">Sachez que lors de la création et de la gestion des groupes avec les cmdlets PowerShell à distance, vous pouvez être confronté à des limitations.</span><span class="sxs-lookup"><span data-stu-id="99237-121">Be aware that when creating and managing groups by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="99237-122">Cette cmdlet utilise une méthode de traitement par lots qui se traduit par un retard de propagation de quelques minutes avant que les résultats de la cmdlet ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="99237-122">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="99237-123">Pour découvrir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online Protection à l'aide d'une session PowerShell distante](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="99237-123">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
    
- <span data-ttu-id="99237-124">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="99237-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="99237-p107">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="99237-p107">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="99237-128">Créer un groupe dans le CAE</span><span class="sxs-lookup"><span data-stu-id="99237-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="99237-129">Dans le Centre d'administration Exchange (CAE), accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="99237-129">In the Exchange admin center (EAC), go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="99237-p108">Cliquez sur **Nouveau**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif), puis sur **Groupe de distribution** ou sur **Groupe de sécurité**, en fonction de vos besoins. Consultez l'article [Types de groupe à extension messagerie](manage-groups-in-eop.md) pour comprendre la distinction.</span><span class="sxs-lookup"><span data-stu-id="99237-p108">Click **New**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **Distribution group** or **Security group**, depending on your needs. See [Types of mail-enabled groups](manage-groups-in-eop.md) for the distinction.</span></span> 
    
3. <span data-ttu-id="99237-132">Sur la page **Nouveau groupe de distribution** ou **Nouveau groupe de sécurité**, renseignez les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="99237-132">On the **New distribution group** or **New security group** page, complete the following fields:</span></span> 
    
  - <span data-ttu-id="99237-p109">**Nom complet** Saisissez le nom complet du groupe. Il doit être propre à votre organisation et avoir du sens pour les utilisateurs EOP. Le nom complet est requis.</span><span class="sxs-lookup"><span data-stu-id="99237-p109">**Display name** Type a display name that's unique to your organization and meaningful to EOP users. The display name is required.</span></span> 
    
  - <span data-ttu-id="99237-p110">**Alias** Saisissez l'alias du groupe. Il doit comporter 64 caractères maximum et être propre à votre organisation. Les utilisateurs EOP saisissent l'alias dans le champ À : d'un message électronique et l'alias génère le nom complet du groupe. Si vous modifiez l'alias, l'adresse SMTP principale du groupe est également modifiée et contient le nouvel alias. L'alias est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="99237-p110">**Alias** Type a group alias of up to 64 characters that's unique to your organization. EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name. If you change the alias, the primary SMTP address for the group also changes and will contain the new alias. The alias is required.</span></span> 
    
  - <span data-ttu-id="99237-139">**Description** Saisissez la description du groupe afin d'informer d'autres personnes du but du groupe.</span><span class="sxs-lookup"><span data-stu-id="99237-139">**Description** Type a description of the group so that people will know the purpose of the group.</span></span> 
    
  - <span data-ttu-id="99237-p111">**Propriétaires** Par défaut, la personne qui crée un groupe en est le propriétaire. Vous pouvez ajouter un propriétaire en cliquant sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif). Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="99237-p111">**Owners** By default, the person who creates the group is the owner. You can add an owner by choosing **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). All groups must have at least one owner.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="99237-143">Les propriétaires des groupes ne doivent pas nécessairement en être membres.</span><span class="sxs-lookup"><span data-stu-id="99237-143">Owners don't have to be members of the group.</span></span> 
  
  - <span data-ttu-id="99237-p112">**Membres** Utilisez cette section pour ajouter des membres au groupe et pour spécifier si une approbation est nécessaire pour que des personnes rejoignent ou quittent le groupe. Pour ajouter des membres au groupe, cliquez sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="99237-p112">**Members** Use this section to add group members and to specify whether approval is required for people to join or leave the group. To add members to the group, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="99237-146">Cliquez sur **OK** pour revenir à la page d'origine.</span><span class="sxs-lookup"><span data-stu-id="99237-146">Click **OK** to return to the original page.</span></span> 
    
5. <span data-ttu-id="99237-p113">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe. Le nouveau groupe doit apparaître dans la liste des groupes.</span><span class="sxs-lookup"><span data-stu-id="99237-p113">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span> 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="99237-149">Modifier ou supprimer un groupe dans le CAE</span><span class="sxs-lookup"><span data-stu-id="99237-149">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="99237-150">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="99237-150">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="99237-151">Effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="99237-151">Do one of the following:</span></span>
    
  - <span data-ttu-id="99237-152">Pour modifier un groupe: dans la liste des groupes, cliquez sur le groupe de distribution ou de sécurité que vous souhaitez afficher ou modifier, puis \*\*\*\* ![cliquez sur modifier](../media/ITPro-EAC-EditIcon.gif)l'icône de modification.</span><span class="sxs-lookup"><span data-stu-id="99237-152">To edit a group: In the list of groups, click the distribution or security group that you want to view or change, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span> <span data-ttu-id="99237-153">Vous pouvez mettre à jour les paramètres généraux, ajouter ou supprimer des propriétaires du groupe, et ajouter ou supprimer des membres du groupe, selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="99237-153">You can update general settings, add or remove group owners, and add or remove group members, as needed.</span></span>
    
  - <span data-ttu-id="99237-154">Pour supprimer un groupe : Sélectionnez le groupe et cliquez sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="99237-154">To remove a group: Select the group and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="99237-155">Après avoir effectué toutes les modifications voulues, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="99237-155">When you're finished making your changes, click **Save**.</span></span>
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="99237-156">Créer, modifier ou supprimer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="99237-156">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="99237-p115">Cette section fournit des informations sur la création de groupes et la modification de leurs propriétés à l’aide de Windows PowerShell à distance. Elle explique également comment supprimer un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="99237-p115">This section provides information about creating groups and changing their properties by using remote Windows PowerShell. It also shows how to remove an existing group.</span></span> 
  
 <span data-ttu-id="99237-159">**Pour créer un groupe à l'aide de Windows PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="99237-159">**To create a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="99237-p116">Cet exemple utilise la cmdlet [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) pour créer un groupe de distribution avec l'alias itadmin et le nom IT Administrators. Il ajoute également des utilisateurs en tant que membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="99237-p116">This example uses the [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span> 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

<span data-ttu-id="99237-162">Pour créer un groupe de sécurité et non un groupe de distribution, spécifiez  `-Type "Security"` à la place.</span><span class="sxs-lookup"><span data-stu-id="99237-162">To create a security group instead of a distribution group, specify  `-Type "Security"` instead.</span></span> 
  
<span data-ttu-id="99237-163">Pour vérifier que vous avez créé avec succès le groupe IT Administrators, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour afficher les informations sur le nouveau groupe :</span><span class="sxs-lookup"><span data-stu-id="99237-163">To verify that you've successfully created the IT Administrators group, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to display information about the new group:</span></span> 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

<span data-ttu-id="99237-164">Pour obtenir la liste des membres du groupe, exécutez la cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) comme suit :</span><span class="sxs-lookup"><span data-stu-id="99237-164">To get a list of members in the group, run the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

<span data-ttu-id="99237-165">Pour obtenir la liste complète de tous vos groupes, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit :</span><span class="sxs-lookup"><span data-stu-id="99237-165">To get a full list of all your groups, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 <span data-ttu-id="99237-166">**Pour modifier les propriétés d'un groupe à l'aide de Windows PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="99237-166">**To change the properties of a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="99237-p117">Utilisez les cmdlets [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) et [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) pour afficher et modifier les propriétés des groupes. L'utilisation de PowerShell à distance, contrairement au CAE, vous permet de modifier les propriétés de plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="99237-p117">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlets to view and change properties for groups. An advantage of using remote PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span> 
  
<span data-ttu-id="99237-169">Voici quelques exemples d'utilisation de Windows PowerShell à distance pour modifier les propriétés de groupe.</span><span class="sxs-lookup"><span data-stu-id="99237-169">Here are some examples of using remote Windows PowerShell to change group properties.</span></span>
  
<span data-ttu-id="99237-170">Cet exemple utilise la cmdlet [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) pour modifier l'adresse SMTP principale (également appelée l'adresse de réponse) pour le groupe Seattle Employees en sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="99237-170">This example uses the [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet to change the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span> 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

<span data-ttu-id="99237-p118">Pour vérifier que vous avez modifié avec succès les propriétés d'un groupe, utilisez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) pour contrôler les modifications. L'utilisation de PowerShell à distance présente l'avantage de pouvoir afficher plusieurs propriétés de plusieurs groupes. Dans l'exemple ci-dessus, où le groupe d'adresses SMTP principal a été modifié, exécutez la commande suivante pour vérifier la nouvelle valeur :</span><span class="sxs-lookup"><span data-stu-id="99237-p118">To verify that you've successfully changed the properties for a group, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. One advantage of using remote PowerShell is that you can view multiple properties for multiple groups. In the previous example where the primary SMTP address group was changed, run the following command to verify the new value:</span></span> 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

<span data-ttu-id="99237-p119">Cet exemple utilise la cmdlet [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) pour mettre à jour tous les membres du groupe Seattle Employees. Utilisez des virgules pour séparer tous les membres.</span><span class="sxs-lookup"><span data-stu-id="99237-p119">This example uses the [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet to update all the members of the Seattle Employees group. Use a comma to separate all members.</span></span> 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

<span data-ttu-id="99237-176">Pour obtenir la liste de tous les membres du groupe Seattle Employees, utilisez la cmdlet [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) comme suit :</span><span class="sxs-lookup"><span data-stu-id="99237-176">To get the list of all the members in the group Seattle Employees, use the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 <span data-ttu-id="99237-177">**Pour supprimer un groupe à l'aide de Windows PowerShell à distance**</span><span class="sxs-lookup"><span data-stu-id="99237-177">**To remove a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="99237-178">Cet exemple utilise la cmdlet [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) pour supprimer un groupe de distribution nommé IT Administrators.</span><span class="sxs-lookup"><span data-stu-id="99237-178">This example uses the [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet to remove a distribution group named IT Administrators.</span></span> 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

<span data-ttu-id="99237-179">Pour vérifier que le groupe a été supprimé, exécutez la cmdlet [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) comme suit, et confirmez que le groupe (dans ce cas, IT Administrators) a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="99237-179">To verify that the group was removed, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows, and confirm that the group (in this case "It Administrators") was deleted.</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


