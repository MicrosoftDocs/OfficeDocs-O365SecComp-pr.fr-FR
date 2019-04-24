---
title: "Exécution d’un rapport de groupe de rôles d'administrateur dans EOP "
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Quand un administrateur ajoute ou supprime des membres de groupes de rôles d'administrateur, Microsoft Exchange Online Protection (EOP) consigne chaque occurrence.
ms.openlocfilehash: 752def771d95fcfbb3f7cbe0bc86a33b3967716d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256182"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a><span data-ttu-id="fc7da-103">Exécution d’un rapport de groupe de rôles d'administrateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="fc7da-103">Run an administrator role group report in EOP</span></span> 

 <span data-ttu-id="fc7da-p101">Quand un administrateur ajoute ou supprime des membres de groupes de rôles d'administrateur, Microsoft Exchange Online Protection (EOP) consigne chaque occurrence. Lorsque vous exécutez un rapport de groupe de rôles d'administrateur dans le Centre d'administration Exchange (CAE), les entrées sont affichées comme résultats de la recherche et incluent les groupes de rôles affectés, les personnes ayant modifié l'appartenance au groupe de rôles ainsi que les modifications ayant été apportées à l'appartenance. Utilisez ce rapport pour surveiller les modifications aux autorisations administratives attribuées aux utilisateurs dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p101">When an administrator adds members to or removes members from administrator role groups, Microsoft Exchange Online Protection (EOP) logs each occurrence. When you run an administrator role group report in the Exchange admin center, entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made. Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="fc7da-107">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fc7da-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="fc7da-108">Durée d'exécution estimée : 2 minutes</span><span class="sxs-lookup"><span data-stu-id="fc7da-108">Estimated time to complete: 2 minutes</span></span>
    
- <span data-ttu-id="fc7da-p102">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la section « Rapports » de la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="fc7da-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Reports" section of the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="fc7da-111">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="fc7da-111">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="fc7da-p103">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="fc7da-p103">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="fc7da-115">Utiliser le Centre d'administration Exchange (CAE) pour exécuter un rapport de groupe de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="fc7da-115">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="fc7da-116">Exécutez le rapport de groupe de rôles d'administrateur pour identifier les modifications apportées aux groupes de rôles de gestion dans votre organisation pendant une période donnée.</span><span class="sxs-lookup"><span data-stu-id="fc7da-116">Run the administrator role group report to find the changes to management role groups in your organization within a particular timeframe.</span></span>
  
1. <span data-ttu-id="fc7da-117">Dans le CAE, accédez à **Gestion de la conformité** \> **Audit**, puis sélectionnez **Exécuter un rapport de groupe de rôles d'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="fc7da-117">In the EAC, navigate to **Compliance management** \> **Auditing**, and choose **Run an administrator role group report**.</span></span>
    
2. <span data-ttu-id="fc7da-p104">Sélectionnez la **date de début** et la **date de fin**. Par défaut, le rapport recherche toutes les modifications apportées aux groupes de rôles d'administrateur au cours des deux semaines passées.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p104">Choose the **Start date** and **End date**. By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>
    
3. <span data-ttu-id="fc7da-p105">Pour afficher les modifications apportées à un groupe de rôles précis, cliquez sur **Sélectionnez les groupes de rôles**. Sélectionnez le ou les groupes de rôles dans la boîte de dialogue suivante, puis cliquez sur **OK**. Vous pouvez également laisser le champ vide pour rechercher tous les groupes de rôles qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p105">To view the changes for a specific role group, click **Select role groups**. Select the role group (or groups) in the subsequent dialog box, and click **OK**. You can also leave the field blank to find all changed role groups.</span></span>
    
4. <span data-ttu-id="fc7da-123">Cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="fc7da-123">Click **Search**.</span></span>
    
<span data-ttu-id="fc7da-p106">Si des modifications correspondent aux critères que vous avez spécifiés, elles seront affichées dans le volet des résultats. Cliquez sur un groupe de rôles dans les résultats de la recherche pour afficher les modifications dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p106">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="fc7da-126">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="fc7da-126">How do you know this worked?</span></span>

<span data-ttu-id="fc7da-p107">Si vous avez bien exécuté un rapport de groupe de rôles d'administrateur, les groupes de rôles qui ont été modifiés dans la plage de dates s'affichent dans le volet des résultats de la recherche. En cas d'absence de résultats, cela signifie qu'aucune modification aux groupes de rôles n'a eu lieu dans la plage de dates indiquée. Si vous pensez que des résultats devraient apparaître, modifiez la plage de dates et réexécutez le rapport.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p107">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>
  
## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="fc7da-130">Surveillances des modifications apportées à l'appartenance à des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fc7da-130">Monitor changes to role group membership</span></span>

<span data-ttu-id="fc7da-p108">Lorsque des membres sont ajoutés ou supprimés dans groupe de rôles, les résultats de la recherche affichés dans le volet d'informations indiquent que l'appartenance à un groupe de rôles a été mise à jour et répertorient les membres actuels. Les résultats n'indiquent pas explicitement quel utilisateur a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="fc7da-p108">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>
  
<span data-ttu-id="fc7da-p109">Pour déterminer si un utilisateur a été ajouté ou supprimé, vous devez comparer deux entrées séparées dans le rapport. Par exemple, examinons les entrées de journal suivantes pour le groupe de rôles **Support technique**:</span><span class="sxs-lookup"><span data-stu-id="fc7da-p109">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span> 
  
 <span data-ttu-id="fc7da-135">**27/01/2013 16h43**</span><span class="sxs-lookup"><span data-stu-id="fc7da-135">**1/27/2013 4:43 PM**</span></span>
  
 <span data-ttu-id="fc7da-136">**Administrateur**</span><span class="sxs-lookup"><span data-stu-id="fc7da-136">**Administrator**</span></span>
  
 <span data-ttu-id="fc7da-137">**Membres mis à jour : Administrateur;annb,florencef;pilarp**</span><span class="sxs-lookup"><span data-stu-id="fc7da-137">**Updated members: Administrator;annb,florencef;pilarp**</span></span>
  
 <span data-ttu-id="fc7da-138">**06/02/2013 10h09**</span><span class="sxs-lookup"><span data-stu-id="fc7da-138">**2/06/2013 10:09 AM**</span></span>
  
 <span data-ttu-id="fc7da-139">**Administrateur**</span><span class="sxs-lookup"><span data-stu-id="fc7da-139">**Administrator**</span></span>
  
 <span data-ttu-id="fc7da-140">**Membres mis à jour : Administrator;annb;florencef;pilarp;tonip**</span><span class="sxs-lookup"><span data-stu-id="fc7da-140">**Updated members: Administrator;annb;florencef;pilarp;tonip**</span></span>
  
 <span data-ttu-id="fc7da-141">**19/02/2013 14h12**</span><span class="sxs-lookup"><span data-stu-id="fc7da-141">**2/19/2013 2:12 PM**</span></span>
  
 <span data-ttu-id="fc7da-142">**Administrateur**</span><span class="sxs-lookup"><span data-stu-id="fc7da-142">**Administrator**</span></span>
  
 <span data-ttu-id="fc7da-143">**Membres mis à jour : Administrator;annb;florencef;tonip**</span><span class="sxs-lookup"><span data-stu-id="fc7da-143">**Updated members: Administrator;annb;florencef;tonip**</span></span>
  
<span data-ttu-id="fc7da-144">Dans cet exemple, le compte d'utilisateur Administrateur a apporté les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc7da-144">In this example, the Administrator user account made the following changes:</span></span>
  
- <span data-ttu-id="fc7da-145">Le 06/02/2013, il a ajouté l'utilisateur tonip.</span><span class="sxs-lookup"><span data-stu-id="fc7da-145">On 2/06/2013, it added the user tonip.</span></span>
    
- <span data-ttu-id="fc7da-146">Le 19/02/2013, il a supprimé l'utilisateur pilarp.</span><span class="sxs-lookup"><span data-stu-id="fc7da-146">On 2/19/2013, it removed the user pilarp.</span></span>
    

