---
title: Modifier ou supprimer des stratégies de barrière des informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Découvrez comment modifier ou supprimer des stratégies pour les barrières d’informations.
ms.openlocfilehash: e6bed4df2329d426f86bd4cde07bdc7d1a2792cd
ms.sourcegitcommit: 7c48ce016fa9f45a3813467f7c5a2fd72f9b8f49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2019
ms.locfileid: "35215647"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="173c4-103">Modifier ou supprimer des stratégies de barrière des informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="173c4-103">Edit or remove information barrier policies (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="173c4-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="173c4-104">Overview</span></span>

<span data-ttu-id="173c4-105">Une fois que vous avez [défini des stratégies de barrière des informations](information-barriers-policies.md), vous devrez peut-être modifier ces stratégies ou vos segments d’utilisateur, dans le cadre de la [résolution des problèmes](information-barriers-troubleshooting.md) ou de la maintenance normale.</span><span class="sxs-lookup"><span data-stu-id="173c4-105">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="173c4-106">Utilisez cet article comme guide.</span><span class="sxs-lookup"><span data-stu-id="173c4-106">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="173c4-107">Pour effectuer les tâches décrites dans cet article, vous devez disposer d’un rôle approprié, par exemple:</span><span class="sxs-lookup"><span data-stu-id="173c4-107">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="173c4-108">-Administrateur général de Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="173c4-108">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="173c4-109">-Administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="173c4-109">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="173c4-110">-Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="173c4-110">- Compliance Administrator</span></span><br/><span data-ttu-id="173c4-111">-IB gestion de la conformité (il s’agit d’un nouveau rôle!)</span><span class="sxs-lookup"><span data-stu-id="173c4-111">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="173c4-112">Pour en savoir plus sur les conditions préalables pour les barrières d’informations, reportez-vous à la rubrique [conditions préalables (pour les stratégies de barrière des informations)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="173c4-112">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="173c4-113">Assurez [-vous de vous connecter au centre de sécurité & de sécurité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="173c4-113">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="173c4-114">Modifier les attributs de compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="173c4-114">Edit user account attributes</span></span>

<span data-ttu-id="173c4-115">Utilisez cette procédure pour modifier les attributs utilisés pour segmenter les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="173c4-115">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="173c4-116">Par exemple, si vous utilisez un attribut de service et qu’un ou plusieurs comptes d’utilisateur n’ont pas de valeurs répertoriées pour le service, vous devez modifier ces comptes d’utilisateur pour inclure les informations de service.</span><span class="sxs-lookup"><span data-stu-id="173c4-116">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="173c4-117">Les attributs de compte d’utilisateur sont utilisés pour définir des segments afin que les stratégies de barrière des informations puissent être affectées.</span><span class="sxs-lookup"><span data-stu-id="173c4-117">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="173c4-118">Pour afficher les détails d’un compte d’utilisateur spécifique, tels que les valeurs d’attribut et les segments affectés, utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec les paramètres d’identité.</span><span class="sxs-lookup"><span data-stu-id="173c4-118">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

   <span data-ttu-id="173c4-119">Syntaxe`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="173c4-119">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 
    
   <span data-ttu-id="173c4-120">Vous pouvez utiliser n’importe quelle valeur qui identifie de façon unique chaque utilisateur, comme le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID.</span><span class="sxs-lookup"><span data-stu-id="173c4-120">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 
    
   <span data-ttu-id="173c4-121">Exemple : `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="173c4-121">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 
    
   <span data-ttu-id="173c4-122">Dans cet exemple, nous faisons référence à deux comptes d’utilisateur dans Office 365: *meganb* pour *Megan*, et *Alexw* pour *Alex*.</span><span class="sxs-lookup"><span data-stu-id="173c4-122">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
   <span data-ttu-id="173c4-123">(Vous pouvez également utiliser cette applet de commande pour un seul `Get-InformationBarrierRecipientStatus -Identity <value>`utilisateur:)</span><span class="sxs-lookup"><span data-stu-id="173c4-123">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> 
    
2. <span data-ttu-id="173c4-124">Déterminez l’attribut que vous souhaitez modifier pour vos profils de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="173c4-124">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="173c4-125">Pour plus d’informations, reportez-vous à la rubrique [attributs pour les stratégies de barrière des informations (aperçu)](information-barriers-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="173c4-125">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="173c4-126">Modifiez un ou plusieurs comptes d’utilisateur pour inclure des valeurs pour l’attribut que vous avez sélectionné à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="173c4-126">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="173c4-127">Pour ce faire, utilisez l’une des procédures suivantes:</span><span class="sxs-lookup"><span data-stu-id="173c4-127">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="173c4-128">Pour modifier un seul compte, voir [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="173c4-128">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="173c4-129">Pour modifier plusieurs comptes (ou utiliser PowerShell pour modifier un seul compte), voir [configure User Account Properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="173c4-129">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="173c4-130">Modifier un segment</span><span class="sxs-lookup"><span data-stu-id="173c4-130">Edit a segment</span></span>

<span data-ttu-id="173c4-131">Utilisez cette procédure pour modifier la définition d’un segment d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="173c4-131">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="173c4-132">Par exemple, vous pouvez modifier le nom d’un segment ou le filtre utilisé pour déterminer qui est inclus dans le segment.</span><span class="sxs-lookup"><span data-stu-id="173c4-132">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="173c4-133">Pour afficher tous les segments existants, utilisez la cmdlet **Get-OrganizationSegment** .</span><span class="sxs-lookup"><span data-stu-id="173c4-133">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="173c4-134">Syntaxe`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="173c4-134">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="173c4-135">Vous verrez une liste de segments et des détails pour chacune d’elles, comme le type de segment, sa valeur UserGroupFilter, l’auteur ou la dernière modification, GUID, etc.</span><span class="sxs-lookup"><span data-stu-id="173c4-135">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="173c4-136">Imprimez ou enregistrez votre liste de segments pour référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="173c4-136">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="173c4-137">Par exemple, si vous souhaitez modifier un segment, vous devez connaître son nom ou identifier la valeur (utilisée avec le paramètre Identity).</span><span class="sxs-lookup"><span data-stu-id="173c4-137">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="173c4-138">Pour modifier un segment, utilisez la cmdlet **Set-OrganizationSegment** avec le paramètre **Identity** et les détails pertinents.</span><span class="sxs-lookup"><span data-stu-id="173c4-138">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="173c4-139">Syntaxe`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="173c4-139">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="173c4-140">Exemple : `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="173c4-140">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="173c4-141">Dans cet exemple, pour le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*, nous avons mis à jour le nom du service en «hrdept».</span><span class="sxs-lookup"><span data-stu-id="173c4-141">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="173c4-142">Une fois que vous avez terminé de modifier les segments de votre organisation, vous pouvez [définir](information-barriers-policies.md#part-2-define-information-barrier-policies) ou [modifier](#edit-a-policy) des stratégies de barrière des informations.</span><span class="sxs-lookup"><span data-stu-id="173c4-142">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="173c4-143">Modifier une stratégie</span><span class="sxs-lookup"><span data-stu-id="173c4-143">Edit a policy</span></span>

1. <span data-ttu-id="173c4-144">Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="173c4-144">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="173c4-145">Syntaxe`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="173c4-145">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="173c4-146">Dans la liste des résultats, identifiez la stratégie à modifier.</span><span class="sxs-lookup"><span data-stu-id="173c4-146">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="173c4-147">Notez le GUID et le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="173c4-147">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="173c4-148">Utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre **Identity** et spécifiez les modifications que vous souhaitez effectuer.</span><span class="sxs-lookup"><span data-stu-id="173c4-148">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="173c4-149">Exemple: Supposons qu’une stratégie a été définie pour empêcher le segment de *recherche* de communiquer avec les segments de *ventes* et de *marketing* .</span><span class="sxs-lookup"><span data-stu-id="173c4-149">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="173c4-150">La stratégie a été définie à l’aide de cette applet de commande:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="173c4-150">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="173c4-151">Supposons que nous voulons la modifier afin que les membres du segment de *recherche* puissent uniquement communiquer avec des personnes dans le segment *RH* .</span><span class="sxs-lookup"><span data-stu-id="173c4-151">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="173c4-152">Pour effectuer cette modification, nous utilisons cette applet de commande:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="173c4-152">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="173c4-153">Dans cet exemple, nous avons modifié «SegmentsBlocked» en «SegmentsAllowed» et spécifié le segment *HR* .</span><span class="sxs-lookup"><span data-stu-id="173c4-153">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="173c4-154">Lorsque vous avez terminé de modifier une stratégie, veillez à appliquer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="173c4-154">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="173c4-155">(Voir [appliquer des stratégies de barrière des informations](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span><span class="sxs-lookup"><span data-stu-id="173c4-155">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="173c4-156">Définir une stratégie sur état inactif</span><span class="sxs-lookup"><span data-stu-id="173c4-156">Set a policy to inactive status</span></span>

1. <span data-ttu-id="173c4-157">Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="173c4-157">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="173c4-158">Syntaxe`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="173c4-158">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="173c4-159">Dans la liste des résultats, identifiez la stratégie que vous souhaitez modifier (ou supprimer).</span><span class="sxs-lookup"><span data-stu-id="173c4-159">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="173c4-160">Notez le GUID et le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="173c4-160">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="173c4-161">Pour définir l’état de la stratégie sur inactive, utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre Identity et le paramètre State défini sur inactive.</span><span class="sxs-lookup"><span data-stu-id="173c4-161">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="173c4-162">Syntaxe`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="173c4-162">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="173c4-163">Dans cet exemple, nous définissons une stratégie de barrière des informations qui a un GUID *43c37853-EA10-4b90-A23D-ab8c9377247* à un état inactif.</span><span class="sxs-lookup"><span data-stu-id="173c4-163">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="173c4-164">Pour appliquer vos modifications, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="173c4-164">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="173c4-165">Syntaxe`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="173c4-165">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="173c4-166">Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="173c4-166">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="173c4-167">Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus).</span><span class="sxs-lookup"><span data-stu-id="173c4-167">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="173c4-168">(En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)</span><span class="sxs-lookup"><span data-stu-id="173c4-168">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="173c4-169">À ce stade, une ou plusieurs stratégies de barrière des informations sont définies sur l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="173c4-169">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="173c4-170">À partir de là, vous pouvez effectuer l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="173c4-170">From here, you can do any of the following:</span></span>
- <span data-ttu-id="173c4-171">Conservez-la telle quelle (une stratégie définie sur l’état inactif n’a aucun effet sur les utilisateurs)</span><span class="sxs-lookup"><span data-stu-id="173c4-171">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="173c4-172">Modifier une stratégie</span><span class="sxs-lookup"><span data-stu-id="173c4-172">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="173c4-173">Supprimer une stratégie</span><span class="sxs-lookup"><span data-stu-id="173c4-173">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="173c4-174">Supprimer une stratégie</span><span class="sxs-lookup"><span data-stu-id="173c4-174">Remove a policy</span></span>

1. <span data-ttu-id="173c4-175">Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .</span><span class="sxs-lookup"><span data-stu-id="173c4-175">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="173c4-176">Syntaxe`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="173c4-176">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="173c4-177">Dans la liste des résultats, identifiez la stratégie à supprimer.</span><span class="sxs-lookup"><span data-stu-id="173c4-177">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="173c4-178">Notez le GUID et le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="173c4-178">Note the policy's GUID and name.</span></span> <span data-ttu-id="173c4-179">Assurez-vous que la stratégie est définie sur état inactif.</span><span class="sxs-lookup"><span data-stu-id="173c4-179">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="173c4-180">Utilisez la cmdlet **Remove-InformationBarrierPolicy** avec un paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="173c4-180">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="173c4-181">Syntaxe`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="173c4-181">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="173c4-182">Exemple: Supposons que nous voulons supprimer une stratégie qui a le GUID *43c37853-EA10-4b90-A23D-ab8c93772471*.</span><span class="sxs-lookup"><span data-stu-id="173c4-182">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="173c4-183">Pour ce faire, nous utilisons cette applet de commande:</span><span class="sxs-lookup"><span data-stu-id="173c4-183">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="173c4-184">Lorsque vous y êtes invité, confirmez la modification.</span><span class="sxs-lookup"><span data-stu-id="173c4-184">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="173c4-185">Répétez les étapes 1-2 pour chaque stratégie que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="173c4-185">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="173c4-186">Lorsque vous avez terminé de supprimer des stratégies, appliquez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="173c4-186">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="173c4-187">Pour ce faire, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="173c4-187">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="173c4-188">Syntaxe`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="173c4-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="173c4-189">Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="173c4-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="173c4-190">Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus).</span><span class="sxs-lookup"><span data-stu-id="173c4-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="173c4-191">Arrêter une application de stratégie</span><span class="sxs-lookup"><span data-stu-id="173c4-191">Stop a policy application</span></span>

<span data-ttu-id="173c4-192">Si, après avoir commencé à appliquer des stratégies de barrière des informations, vous souhaitez arrêter l’application de ces stratégies, utilisez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="173c4-192">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="173c4-193">N’oubliez pas que le processus doit durer environ 30-35 minutes.</span><span class="sxs-lookup"><span data-stu-id="173c4-193">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="173c4-194">Pour afficher l’état de l’application de stratégie de barrière des informations la plus récente, utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** .</span><span class="sxs-lookup"><span data-stu-id="173c4-194">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="173c4-195">Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="173c4-195">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="173c4-196">Notez le GUID de l’application.</span><span class="sxs-lookup"><span data-stu-id="173c4-196">Note the application's GUID.</span></span>

2. <span data-ttu-id="173c4-197">Utilisez la cmdlet **Stop-InformationBarrierPoliciesApplication** avec un paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="173c4-197">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="173c4-198">Syntaxe`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="173c4-198">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="173c4-199">Exemple : `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="173c4-199">Example: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

    <span data-ttu-id="173c4-200">Dans cet exemple, nous arrêtons l’application des stratégies de barrière des informations.</span><span class="sxs-lookup"><span data-stu-id="173c4-200">In this example, we are stopping information barrier policies from being applied.</span></span>

## <a name="related-articles"></a><span data-ttu-id="173c4-201">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="173c4-201">Related articles</span></span>

[<span data-ttu-id="173c4-202">Obtenir une vue d’ensemble des barrières d’informations</span><span class="sxs-lookup"><span data-stu-id="173c4-202">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="173c4-203">Définir des stratégies pour les barrières d’information (aperçu)</span><span class="sxs-lookup"><span data-stu-id="173c4-203">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="173c4-204">En savoir plus sur les barrières d’informations dans Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="173c4-204">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="173c4-205">Attributs des stratégies de barrière des informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="173c4-205">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="173c4-206">Dépannage des barrières relatives aux informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="173c4-206">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
