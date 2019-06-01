---
title: Résolution des problèmes liés aux informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez cet article pour résoudre les problèmes liés aux barrières relatives aux informations.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668293"
---
# <a name="troubleshooting-information-barriers-preview"></a><span data-ttu-id="5100f-103">Dépannage des barrières relatives aux informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="5100f-103">Troubleshooting information barriers (Preview)</span></span>

<span data-ttu-id="5100f-104">Les barrières d’informations peuvent aider votre organisation à rester conforme aux exigences légales et aux réglementations sectorielles.</span><span class="sxs-lookup"><span data-stu-id="5100f-104">Information barriers can help your organization remain compliant with legal requirements and industry regulations.</span></span> <span data-ttu-id="5100f-105">Par exemple, avec des barrières d’informations, vous pouvez restreindre la communication entre des groupes spécifiques d’utilisateurs afin d’éviter un conflit d’intérêt ou d’autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="5100f-105">For example, with information barriers, you can restrict communication between specific groups of users to avoid a conflict of interest or other issues.</span></span> <span data-ttu-id="5100f-106">Pour en savoir plus, consultez la rubrique barrières de l' [information (aperçu)](information-barriers.md).</span><span class="sxs-lookup"><span data-stu-id="5100f-106">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span>

<span data-ttu-id="5100f-107">Cet article fournit des instructions que vous pouvez utiliser pour obtenir des réponses à des questions ou résoudre des problèmes qui peuvent survenir avec des barrières d’information.</span><span class="sxs-lookup"><span data-stu-id="5100f-107">This article provides guidance you can use to get answers to questions or resolve issues that may arise with information barriers.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="5100f-108">Avant de commencer...</span><span class="sxs-lookup"><span data-stu-id="5100f-108">Before you begin...</span></span>

<span data-ttu-id="5100f-109">Pour effectuer les tâches décrites dans cet article, vous devez disposer d’un rôle approprié, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5100f-109">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span>
- <span data-ttu-id="5100f-110">Administrateur global Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="5100f-110">Microsoft 365 Enterprise Global Administrator</span></span>
- <span data-ttu-id="5100f-111">Administrateur général Office 365</span><span class="sxs-lookup"><span data-stu-id="5100f-111">Office 365 Global Administrator</span></span>
- <span data-ttu-id="5100f-112">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="5100f-112">Compliance Administrator</span></span>
- <span data-ttu-id="5100f-113">IB gestion de la conformité (il s’agit d’un nouveau rôle!)</span><span class="sxs-lookup"><span data-stu-id="5100f-113">IB Compliance Management (this is a new role!)</span></span>

<span data-ttu-id="5100f-114">Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de sécurité & conformité d’Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="5100f-114">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="5100f-115">Pour en savoir plus sur les conditions préalables pour les barrières d’informations, reportez-vous à la rubrique [conditions préalables (pour les stratégies de barrière des informations)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="5100f-115">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span>

<span data-ttu-id="5100f-116">Assurez-vous également de [vous connecter au centre de sécurité Office 365 Security & PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5100f-116">Also, make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a><span data-ttu-id="5100f-117">Problème: les personnes sont bloquées de manière inattendue dans Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="5100f-117">Issue: People are unexpectedly blocked from communicating in Microsoft Teams</span></span> 

<span data-ttu-id="5100f-118">Dans ce cas, les personnes signalent des problèmes inattendus de communication dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5100f-118">In this case, people are reporting unexpected issues communicating in Microsoft Teams.</span></span> <span data-ttu-id="5100f-119">Exemples :</span><span class="sxs-lookup"><span data-stu-id="5100f-119">Examples:</span></span>
- <span data-ttu-id="5100f-120">Un utilisateur ne peut pas trouver ou communiquer avec un autre utilisateur dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5100f-120">A user is unable to find or communicate with another user in Microsoft Teams.</span></span>
- <span data-ttu-id="5100f-121">Un utilisateur ne peut pas voir ou sélectionner un autre utilisateur dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5100f-121">A user cannot see or select another user in Microsoft Teams.</span></span>
- <span data-ttu-id="5100f-122">Un utilisateur peut voir, mais ne peut pas envoyer de messages à un autre utilisateur de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5100f-122">A user can see, but cannot send messages to, another user in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="5100f-123">Procédure</span><span class="sxs-lookup"><span data-stu-id="5100f-123">What to do</span></span>

1. <span data-ttu-id="5100f-124">Déterminez si les utilisateurs sont affectés par une stratégie de barrière des informations.</span><span class="sxs-lookup"><span data-stu-id="5100f-124">Determine whether the users are affected by an information barrier policy.</span></span> <span data-ttu-id="5100f-125">Pour ce faire, utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec le paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="5100f-125">To do this, use the **Get-InformationBarrierRecipientStatus** cmdlet with the Identity parameter.</span></span> 

    <span data-ttu-id="5100f-126">La syntaxe est`Get-InformationBarrierRecipientStatus -Identity`</span><span class="sxs-lookup"><span data-stu-id="5100f-126">The syntax is `Get-InformationBarrierRecipientStatus -Identity`</span></span>

    <span data-ttu-id="5100f-127">Vous pouvez utiliser n’importe quelle valeur d’identité qui identifie de façon unique chaque destinataire, comme le nom, l’alias, le nom unique (DN), le DN canonique, l’adresse de messagerie ou le GUID.</span><span class="sxs-lookup"><span data-stu-id="5100f-127">You can use any identity value that uniquely identifies each recipient, such as Name, Alias, Distinguished name (DN), Canonical DN, Email address, or GUID.</span></span>

    <span data-ttu-id="5100f-128">Exemple : `Get-InformationBarrierRecipientStatus -Identity meganb`</span><span class="sxs-lookup"><span data-stu-id="5100f-128">Example: `Get-InformationBarrierRecipientStatus -Identity meganb`</span></span>

    <span data-ttu-id="5100f-129">Dans cet exemple, nous utilisons un alias (*meganb*) pour le paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="5100f-129">In this example, we are using an alias (*meganb*) for the Identity parameter.</span></span> <span data-ttu-id="5100f-130">Cette applet de commande renvoie des informations qui indiquent si l’utilisateur est concerné par une stratégie de barrière des informations.</span><span class="sxs-lookup"><span data-stu-id="5100f-130">This cmdlet will return information that indicates whether the user is affected by an information barrier policy.</span></span> <span data-ttu-id="5100f-131">(Recherchez \* ExoPolicyId: \<GUID>.)</span><span class="sxs-lookup"><span data-stu-id="5100f-131">(Look for \*ExoPolicyId: \<GUID>.)</span></span>

    <span data-ttu-id="5100f-132">Si les utilisateurs ne sont pas inclus dans les stratégies de barrière des informations, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="5100f-132">If the users are not included in information barrier policies, contact support.</span></span> <span data-ttu-id="5100f-133">Sinon, passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="5100f-133">Otherwise, proceed to the next step.</span></span>

2. <span data-ttu-id="5100f-134">Découvrez quels segments sont inclus dans une stratégie de barrière des informations.</span><span class="sxs-lookup"><span data-stu-id="5100f-134">Find out which segments are included in an information barrier policy.</span></span> <span data-ttu-id="5100f-135">Pour ce faire, utilisez l' `Get-InformationBarrierPolicy` applet de commande avec le paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="5100f-135">To do this, use the `Get-InformationBarrierPolicy` cmdlet with the Identity parameter.</span></span> <span data-ttu-id="5100f-136">Utilisez des détails, tels que le GUID de stratégie (ExoPolicyId) que vous avez reçu au cours de l’étape précédente, en tant que valeur d’identité.</span><span class="sxs-lookup"><span data-stu-id="5100f-136">Use details, such as the policy GUID (ExoPolicyId) you received during the previous step, as an identity value.</span></span>

    <span data-ttu-id="5100f-137">Exemple : `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span><span class="sxs-lookup"><span data-stu-id="5100f-137">Example: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span></span>

    <span data-ttu-id="5100f-138">Dans cet exemple, nous obtenons des informations détaillées sur la stratégie de barrière des informations qui comporte ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span><span class="sxs-lookup"><span data-stu-id="5100f-138">In this example, we are getting detailed information about the information barrier policy that has ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span></span>
    
    <span data-ttu-id="5100f-139">Une fois que vous avez exécuté l’applet de commande, recherchez les valeurs **AssignedSegment**, **SegmentsAllowed**et **SegmentsBlocked** dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="5100f-139">After you run the cmdlet, in the results, look for **AssignedSegment**, **SegmentsAllowed**, and **SegmentsBlocked** values.</span></span>

    <span data-ttu-id="5100f-140">Exemple: après avoir exécuté `Get-InformationBarrierPolicy` l’applet de commande, nous avons vu les éléments suivants dans notre liste de résultats:</span><span class="sxs-lookup"><span data-stu-id="5100f-140">Example: After running the `Get-InformationBarrierPolicy` cmdlet, we saw the following in our list of results:</span></span>

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    <span data-ttu-id="5100f-141">Dans ce cas, nous pouvons voir qu’une stratégie de barrière des informations affecte les personnes qui se trouvent dans les segments de ventes et de recherche.</span><span class="sxs-lookup"><span data-stu-id="5100f-141">In this case, we can see that an information barrier policy affects people who are in the Sales and Research segments.</span></span> <span data-ttu-id="5100f-142">Dans ce cas, les personnes dans les ventes ne peuvent pas communiquer avec les personnes de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5100f-142">In this case, people in Sales are prevented from communicating with people in Research.</span></span> <span data-ttu-id="5100f-143">Si cela semble correct, les barrières de l’information fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="5100f-143">If this seems correct, then information barriers are working as expected.</span></span> <span data-ttu-id="5100f-144">Si ce n’est pas le cas, passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="5100f-144">If not, proceed to the next step.</span></span>

4. <span data-ttu-id="5100f-145">Assurez-vous que vos segments sont correctement définis.</span><span class="sxs-lookup"><span data-stu-id="5100f-145">Make sure your segments are defined correctly.</span></span> <span data-ttu-id="5100f-146">Pour ce faire, utilisez l' `Get-OrganizationSegment` applet de commande et passez en revue la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="5100f-146">To do this, use the `Get-OrganizationSegment` cmdlet, and review the list of results.</span></span> 

    <span data-ttu-id="5100f-147">Pour afficher les détails d’un segment spécifique, utilisez `Get-OrganizationSegment` l’applet de commande avec un paramètre Identity.</span><span class="sxs-lookup"><span data-stu-id="5100f-147">To view details for a specific segment, use the `Get-OrganizationSegment` cmdlet with an Identity parameter.</span></span> 

    <span data-ttu-id="5100f-148">Exemple : `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span><span class="sxs-lookup"><span data-stu-id="5100f-148">Example: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span></span>

    <span data-ttu-id="5100f-149">Dans cet exemple, nous obtenons des informations sur le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*.</span><span class="sxs-lookup"><span data-stu-id="5100f-149">In this example, we are getting information about the segment that has GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span></span>

    <span data-ttu-id="5100f-150">Passez en revue les détails du segment.</span><span class="sxs-lookup"><span data-stu-id="5100f-150">Review the details for the segment.</span></span> <span data-ttu-id="5100f-151">Si nécessaire, [modifiez un segment](information-barriers-policies.md#edit-a-segment), puis réutilisez l' `Start-InformationBarrierPoliciesApplication` applet de commande.</span><span class="sxs-lookup"><span data-stu-id="5100f-151">If necessary, [edit a segment](information-barriers-policies.md#edit-a-segment), and then re-use the `Start-InformationBarrierPoliciesApplication` cmdlet.</span></span>

    <span data-ttu-id="5100f-152">Si vous rencontrez toujours des problèmes avec votre stratégie de barrière des informations, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="5100f-152">If you are still having issues with your information barrier policy, contact support.</span></span>
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a><span data-ttu-id="5100f-153">Problème: le processus de l’application de barrière des informations prend trop de temps</span><span class="sxs-lookup"><span data-stu-id="5100f-153">Issue: The information barrier application process is taking too long</span></span>

<span data-ttu-id="5100f-154">Après avoir exécuté l’applet de commande **Start-InformationBarrierPoliciesApplication** , le processus prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="5100f-154">After running the **Start-InformationBarrierPoliciesApplication** cmdlet, the process is taking a really long time to finish.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="5100f-155">Procédure</span><span class="sxs-lookup"><span data-stu-id="5100f-155">What to do</span></span>

1. <span data-ttu-id="5100f-156">Gardez à l’esprit que lorsque vous exécutez la cmdlet application de stratégie, les stratégies de barrière des informations sont appliquées (ou supprimées), utilisateur par utilisateur, pour tous les comptes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5100f-156">Keep in mind that when you run the policy application cmdlet, information barrier policies are being applied (or removed), user by user, for all accounts in your organization.</span></span> <span data-ttu-id="5100f-157">Si vous avez un grand nombre d’utilisateurs, le traitement peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="5100f-157">If you have a lot of users, it will take a while to process.</span></span> <span data-ttu-id="5100f-158">(En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)</span><span class="sxs-lookup"><span data-stu-id="5100f-158">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span> 

2. <span data-ttu-id="5100f-159">Utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** pour vérifier l’État.</span><span class="sxs-lookup"><span data-stu-id="5100f-159">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet to verify status.</span></span>

    <span data-ttu-id="5100f-160">Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="5100f-160">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="5100f-161">Pour afficher l’état de toutes les applications de stratégie de barrière des informations, utilisez`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="5100f-161">To display status for all information barrier policy applications, use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span>

    <span data-ttu-id="5100f-162">Cela permet d’afficher des informations indiquant si l’application de stratégie a été exécutée, si elle a échoué ou est en cours d’exécution...</span><span class="sxs-lookup"><span data-stu-id="5100f-162">This will display information about whether policy application completed, failed, or is in progress..</span></span>

3. <span data-ttu-id="5100f-163">En fonction des résultats de l’étape 2, effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="5100f-163">Depending on the results of step 2, take one of the following steps:</span></span>

    - <span data-ttu-id="5100f-164">Si l’application n’a pas démarré et qu’elle a été supérieure à 45 minutes depuis l’exécution de la cmdlet **Start-InformationBarrierPoliciesApplication** , passez en revue votre journal d’audit pour voir s’il existe des erreurs dans les définitions de stratégie, ou pour toute autre raison pour laquelle le l’application n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="5100f-164">If the application has not started, and it has been more than 45 minutes since the **Start-InformationBarrierPoliciesApplication** cmdlet has been run, review your audit log to see if there are any errors in policy definitions, or some other reason why the application has not started.</span></span>

    - <span data-ttu-id="5100f-165">Si l’application a échoué, passez en revue vos segments et stratégies.</span><span class="sxs-lookup"><span data-stu-id="5100f-165">If the application has failed, review your segments and policies.</span></span> <span data-ttu-id="5100f-166">Si nécessaire, [modifiez des segments](information-barriers-policies.md#edit-a-segment) et/ou [modifiez des stratégies](information-barriers-policies.md#edit-a-policy), puis exécutez à nouveau l’applet de commande **Start-InformationBarrierPoliciesApplication** .</span><span class="sxs-lookup"><span data-stu-id="5100f-166">If necessary, [edit segments](information-barriers-policies.md#edit-a-segment) and/or [edit policies](information-barriers-policies.md#edit-a-policy), and then run the **Start-InformationBarrierPoliciesApplication** cmdlet again.</span></span>

    - <span data-ttu-id="5100f-167">Si l’application est toujours en cours d’exécution, patientez plus de temps pour qu’elle se termine.</span><span class="sxs-lookup"><span data-stu-id="5100f-167">If the application is still in progress, allow more time for it to complete.</span></span> <span data-ttu-id="5100f-168">S’il y a eu plusieurs jours, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="5100f-168">If it has been several days, contact support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5100f-169">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="5100f-169">Related topics</span></span>

[<span data-ttu-id="5100f-170">Définir des stratégies pour les barrières d’informations dans Microsoft Teams (aperçu)</span><span class="sxs-lookup"><span data-stu-id="5100f-170">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="5100f-171">Barrières des informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="5100f-171">Information barriers (Preview)</span></span>](information-barriers.md)



