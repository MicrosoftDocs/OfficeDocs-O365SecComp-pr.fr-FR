---
title: Octroi de l’accès au Centre de conformité et sécurité Office 365 aux utilisateurs
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Les utilisateurs doivent disposer d’autorisations dans le centre de conformité Office 365 Security & pour pouvoir gérer les fonctionnalités de sécurité ou de conformité.
ms.openlocfilehash: ea774648efcfe80461eae937f80856acaf1db224
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35792010"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a><span data-ttu-id="2acc7-103">Octroi de l’accès au Centre de conformité et sécurité Office 365 aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2acc7-103">Give users access to the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="2acc7-104">Les utilisateurs doivent disposer d’autorisations dans le centre de conformité Office 365 Security & pour pouvoir gérer les fonctionnalités de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="2acc7-104">Users need to be assigned permissions in the Office 365 Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="2acc7-105">En tant qu’administrateur général Office 365 ou membre du groupe de rôles OrganizationManagement dans le centre de sécurité & conformité, vous pouvez accorder ces autorisations aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2acc7-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="2acc7-106">Ceux-ci pourront uniquement gérer les fonctionnalités de sécurité ou de conformité auxquelles vous leur donnez accès.</span><span class="sxs-lookup"><span data-stu-id="2acc7-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="2acc7-107">Pour plus d’informations sur les différentes autorisations que vous pouvez accorder aux utilisateurs dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2acc7-107">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="2acc7-108">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2acc7-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="2acc7-109">Vous devez être un administrateur général Office 365 ou un membre du groupe de rôles OrganizationManagement dans le centre de sécurité & Compliance Center pour effectuer les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2acc7-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="2acc7-110">Les groupes de rôles pour le centre de sécurité & conformité peuvent avoir des noms similaires aux groupes de rôles dans Exchange Online, mais ils ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="2acc7-110">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="2acc7-111">Les appartenances aux groupes de rôles ne sont pas partagées entre Exchange Online et le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="2acc7-111">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="2acc7-112">Les autorisations des partenaires DAP (Delegated Access permission) avec administrer de la part de (administrateur) ne peuvent pas accéder au centre de conformité &.</span><span class="sxs-lookup"><span data-stu-id="2acc7-112">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="2acc7-113">Utiliser le centre d’administration pour accorder à un autre utilisateur l’accès au centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="2acc7-113">Use the admin center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="2acc7-114">[Connectez-vous à Office 365 et accédez au centre d’administration](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="2acc7-114">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>

2. <span data-ttu-id="2acc7-115">Dans le centre d’administration 365 de Microsoft, ouvrez **centres d’administration** , puis cliquez sur **sécurité & conformité**.</span><span class="sxs-lookup"><span data-stu-id="2acc7-115">In the Microsoft 365 admin center, open **Admin centers** and then click **Security & Compliance**.</span></span>

3. <span data-ttu-id="2acc7-116">Dans le centre de sécurité & conformité, accédez à **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="2acc7-116">In the Security & Compliance Center, go to **Permissions**.</span></span>

4. <span data-ttu-id="2acc7-117">Dans la liste, choisissez le groupe de rôles auquel vous souhaitez ajouter l’utilisateur, puis cliquez sur **modifier** ![l'](media/O365-MDM-CreatePolicy-EditIcon.gif)icône modifier.</span><span class="sxs-lookup"><span data-stu-id="2acc7-117">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

5. <span data-ttu-id="2acc7-118">Dans la page des propriétés du groupe de rôles sous **membres**, cliquez sur](media/ITPro-EAC-AddIcon.gif) **Ajouter**![une icône et sélectionnez le nom de l’utilisateur (ou des utilisateurs) que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="2acc7-118">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

6. <span data-ttu-id="2acc7-119">Une fois que vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur \*\*ajouter-\> \*\* puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2acc7-119">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

7. <span data-ttu-id="2acc7-120">Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="2acc7-120">Click **Save** to save the changes to the role group.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="2acc7-121">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="2acc7-121">How do you know this worked?</span></span>

1. <span data-ttu-id="2acc7-122">Dans le centre de sécurité & conformité, accédez à **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="2acc7-122">In the Security & Compliance Center, go to **Permissions**.</span></span>

2. <span data-ttu-id="2acc7-123">Dans la liste, sélectionnez le groupe de rôles pour afficher les membres.</span><span class="sxs-lookup"><span data-stu-id="2acc7-123">From the list, select the role group to view the members.</span></span>

3. <span data-ttu-id="2acc7-124">À droite, dans les détails du groupe de rôles, vous pouvez afficher les membres du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="2acc7-124">On the right, in the role group details, you can view the members of the role group.</span></span>

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="2acc7-125">Utiliser PowerShell pour donner à un autre utilisateur l’accès au centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="2acc7-125">Use PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="2acc7-126">[Connectez-vous au centre de sécurité & conformité d’Office 365 PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="2acc7-126">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="2acc7-127">Utilisez la commande **Add-RoleGroupMember** pour ajouter un utilisateur au rôle Gestion de l’organisation, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2acc7-127">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span>

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   <span data-ttu-id="2acc7-128">**Paramètres**:</span><span class="sxs-lookup"><span data-stu-id="2acc7-128">**Parameters**:</span></span>
  
   - <span data-ttu-id="2acc7-129">_Identity_ est le groupe de rôles auquel ajouter un membre.</span><span class="sxs-lookup"><span data-stu-id="2acc7-129">_Identity_ is the role group to add a member to.</span></span>

   - <span data-ttu-id="2acc7-130">_Membre_ est la boîte aux lettres, le groupe de sécurité universel ou l’ordinateur à ajouter au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="2acc7-130">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="2acc7-131">Vous ne pouvez spécifier qu’un membre à la fois.</span><span class="sxs-lookup"><span data-stu-id="2acc7-131">You can specify only one member at a time.</span></span>

<span data-ttu-id="2acc7-132">Pour plus d’informations sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="2acc7-132">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="2acc7-133">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="2acc7-133">How do you know this worked?</span></span>

<span data-ttu-id="2acc7-134">Pour vérifier que vous avez accordé aux utilisateurs l’accès au centre de sécurité & conformité, utilisez la cmdlet **Get-RoleGroupMember** pour afficher les membres du groupe de rôles gestion de l’organisation, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2acc7-134">To verify that you've given users access to the Security & Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span>
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

<span data-ttu-id="2acc7-135">Pour plus d’informations sur la syntaxe et les paramètres, consultez la rubrique [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="2acc7-135">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
