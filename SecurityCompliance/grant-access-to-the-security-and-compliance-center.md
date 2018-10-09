---
title: Donner aux utilisateurs l’accès à la la sécurité d’Office 365 &amp; centre de conformité
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Les utilisateurs doivent être affectées des autorisations de sécurité Office 365 &amp; centre de conformité avant qu’ils peuvent gérer une de ses fonctionnalités de sécurité ou de conformité.
ms.openlocfilehash: e0c8b655b1b3300e4ffa9aba1d94e65a9ef26121
ms.sourcegitcommit: 2e41cc24ad92005084f2ba432e724bdcc4e295ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25450739"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="49cf5-103">Donner aux utilisateurs l’accès à la la sécurité d’Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="49cf5-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="49cf5-p101">Les utilisateurs doivent être affectées des autorisations de sécurité Office 365 &amp; centre de conformité avant qu’ils peuvent gérer une de ses fonctionnalités de sécurité ou de conformité. En tant qu’administrateur global d’Office 365 ou membre du groupe de rôles de sécurité OrganizationManagement &amp; centre de conformité, vous pouvez attribuer ces autorisations aux utilisateurs. Les utilisateurs ne seront en mesure de gérer les fonctionnalités de sécurité ou de conformité que vous leur accordez l’accès.</span><span class="sxs-lookup"><span data-stu-id="49cf5-p101">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features. As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users. Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="49cf5-107">Pour plus d’informations sur les différentes autorisations que vous pouvez donner aux utilisateurs de la sécurité &amp; centre de conformité, extraction [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="49cf5-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="49cf5-108">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="49cf5-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="49cf5-109">Vous devez être un administrateur global d’Office 365, ou un membre du groupe de rôles de sécurité OrganizationManagement &amp; centre de conformité, pour effectuer les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="49cf5-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="49cf5-110">Groupes de rôles de sécurité &amp; centre de conformité peut avoir des noms similaires pour les groupes de rôles dans Exchange Online, mais ils ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="49cf5-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="49cf5-111">Appartenances aux groupes de rôles ne sont pas partagés entre Exchange Online et de la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="49cf5-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="49cf5-112">Utiliser le centre d’administration Office 365 pour donner un autre utilisateur l’accès à la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="49cf5-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="49cf5-113">[Se connecter à Office 365 et accédez au centre d’administration](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="49cf5-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
2. <span data-ttu-id="49cf5-114">Dans le centre d’administration Office 365, ouvrez le **Centre d’administration** , puis sur **sécurité &amp; conformité**.</span><span class="sxs-lookup"><span data-stu-id="49cf5-114">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
    
3. <span data-ttu-id="49cf5-115">Dans la sécurité &amp; centre de conformité, accédez à **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="49cf5-115">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="49cf5-116">Dans la liste, sélectionnez le groupe de rôles que vous souhaitez ajouter l’utilisateur, cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="49cf5-116">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="49cf5-117">Dans la page de propriétés du groupe de rôles sous **membres**, cliquez sur **Ajouter**![ajouter une icône](media/ITPro-EAC-AddIcon.gif) et sélectionnez le nom de l’utilisateur (ou utilisateurs) que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="49cf5-117">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="49cf5-118">Lorsque vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur \*\*Ajouter-\> \*\* , puis **OK**.</span><span class="sxs-lookup"><span data-stu-id="49cf5-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="49cf5-119">Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="49cf5-119">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="49cf5-120">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="49cf5-120">How do you know this worked?</span></span>

1. <span data-ttu-id="49cf5-121">Dans la sécurité &amp; centre de conformité, accédez à **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="49cf5-121">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="49cf5-122">Dans la liste, sélectionnez le groupe de rôles pour afficher les membres.</span><span class="sxs-lookup"><span data-stu-id="49cf5-122">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="49cf5-123">Sur la droite, dans les détails de groupe de rôles, vous pouvez afficher les membres du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="49cf5-123">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="49cf5-124">Utiliser PowerShell pour donner un autre utilisateur l’accès à la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="49cf5-124">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="49cf5-125">[Se connecter à l’Office 365 Security &amp; centre de conformité à l’aide de PowerShell à distance](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="49cf5-125">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
    
2. <span data-ttu-id="49cf5-126">Utilisez la commande **Add-RoleGroupMember** pour ajouter un utilisateur au rôle Gestion de l’organisation, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="49cf5-126">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="49cf5-127">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="49cf5-127">**Parameters**</span></span>
  
-  <span data-ttu-id="49cf5-128">_-Identity_ est le groupe de rôles auquel ajouter un membre.</span><span class="sxs-lookup"><span data-stu-id="49cf5-128">_-Identity_ is the role group to add a member to.</span></span> 
    
- - <span data-ttu-id="49cf5-p102">_Membre_ est la boîte aux lettres, le groupe de sécurité universel (USG) ou d’ordinateur à ajouter au groupe de rôles. Vous pouvez spécifier qu’un seul membre à la fois.</span><span class="sxs-lookup"><span data-stu-id="49cf5-p102">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group. You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="49cf5-131">Pour plus d’informations sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="49cf5-131">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="49cf5-132">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="49cf5-132">How do you know this worked?</span></span>

<span data-ttu-id="49cf5-133">Pour vérifier que vous avez accordé aux utilisateurs accès à la sécurité &amp; centre de conformité, utilisez l’applet de commande **Get-RoleGroupMember** permet d’afficher les membres dans le groupe de rôles de gestion de l’organisation, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="49cf5-133">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="49cf5-134">Pour plus d’informations sur la syntaxe et les paramètres, voir [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="49cf5-134">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  

