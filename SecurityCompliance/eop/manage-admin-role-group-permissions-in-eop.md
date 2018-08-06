---
title: Gérer les autorisations de groupe de rôles d’administrateur dans EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.
ms.openlocfilehash: 5d50c77c97f2c345aa3994e7fa3ecd2eea93a13a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026661"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="f134d-104">Gérer les autorisations de groupe de rôles d’administrateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="f134d-104">Manage admin role group permissions in EOP</span></span>
  
<span data-ttu-id="f134d-p102">Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="f134d-p102">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f134d-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f134d-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="f134d-108">Durée d'exécution estimée : 5 à 10 minutes</span><span class="sxs-lookup"><span data-stu-id="f134d-108">Estimated time to complete: 5-10 minutes</span></span>
    
- <span data-ttu-id="f134d-p103">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="f134d-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="f134d-p104">Certaines autorisations dans Office 365 mappent vers des autorisations du groupe de rôles d'administration EOP. Pour plus d'informations, consultez la colonne « Rôle dans Exchange Online » de la section « À quels services mes autorisations Office 365 s'appliquent-elles ? » dans la rubrique [Affectation de rôles d'administrateur](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span><span class="sxs-lookup"><span data-stu-id="f134d-p104">Certain permissions in Office 365 map to EOP admin role group permissions. For more information, see the "Role in Exchange Online" column in the "Which services do my Office 365 permissions extend to?" section in [Assigning Admin Roles](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span></span>
    
- <span data-ttu-id="f134d-114">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013**Raccourcis clavier dans le Centre d'administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f134d-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="f134d-p105">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="f134d-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="what-do-you-want-to-do"></a><span data-ttu-id="f134d-118">Que souhaitez-vous faire ?</span><span class="sxs-lookup"><span data-stu-id="f134d-118">What do you want to do?</span></span>

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="f134d-119">Utiliser le Centre d'administration Exchange (CAE) pour affecter des membres à des groupes de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="f134d-119">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="f134d-120">Dans le CAE, accédez à **Autorisation**\> **Rôles d'administrateur**, cliquez sur le groupe de rôles dans lequel vous voulez ajouter le ou les utilisateurs, puis cliquez sur **Modifier**![Icône Modifier](../media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="f134d-120">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to add the user or users to, and then click **Edit**![Edit icon](../media/ITPro-EAC-EditIcon.png).</span></span>
    
2. <span data-ttu-id="f134d-p106">Sous Membres, cliquez sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.png). La fenêtre Sélectionner les membres s'affiche.</span><span class="sxs-lookup"><span data-stu-id="f134d-p106">Under Members, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.png). The Select Members window will appear.</span></span>
    
3. <span data-ttu-id="f134d-123">Recherchez le ou les utilisateurs à ajouter, ou sélectionnez-les dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f134d-123">Search for the user or users that you wish to add, or select them from the list.</span></span>
    
4. <span data-ttu-id="f134d-p107">Lorsque vous avez sélectionné les utilisateurs à ajouter, cliquez sur **Ajouter**, puis sur **OK**. La fenêtre Sélectionner les membres se ferme.</span><span class="sxs-lookup"><span data-stu-id="f134d-p107">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>
    
5. <span data-ttu-id="f134d-p108">Vous constatez que les utilisateurs ont été ajoutés au volet **Membres**. Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f134d-p108">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f134d-128">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="f134d-128">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="f134d-129">Utiliser le Centre d'administration Exchange (CAE) pour supprimer des membres de groupes de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="f134d-129">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="f134d-130">Dans le CAE, accédez à **Autorisation**\> **Rôles d'administrateur**, cliquez sur le groupe de rôles duquel vous voulez supprimer le ou les utilisateurs, puis cliquez sur **Modifier**![Icône Modifier](../media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="f134d-130">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit**![Edit icon](../media/ITPro-EAC-EditIcon.png).</span></span>
    
2. <span data-ttu-id="f134d-131">Sous Membres, sélectionnez les utilisateurs à supprimer, puis cliquez sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.png).</span><span class="sxs-lookup"><span data-stu-id="f134d-131">Under Members, select the user or users that you want to remove and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.png).</span></span>
    
3. <span data-ttu-id="f134d-p109">Cliquez sur **Enregistrer** pour enregistrer la modification apportée au groupe de rôles et retourner à la page **Rôles d'administrateur**. Pour vérifier que vous avez supprimé l'utilisateur du groupe de rôles d'administrateur, assurez-vous que le membre n'apparaît plus sous Membres dans le volet Détails relatif au groupe de rôles sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f134d-p109">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f134d-134">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="f134d-134">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="f134d-135">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="f134d-135">For more information</span></span>

[<span data-ttu-id="f134d-136">Autorisations des fonctionnalités dans EOP</span><span class="sxs-lookup"><span data-stu-id="f134d-136">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
  

