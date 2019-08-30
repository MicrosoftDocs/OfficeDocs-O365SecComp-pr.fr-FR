---
title: "Exécution d’un rapport de groupe de rôles d'administrateur dans EOP "
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Les administrateurs peuvent apprendre à exécuter un rapport de groupe de rôles d’administrateur dans Exchange Online Protection (EOP). Ce rapport enregistre les journaux lorsqu’un administrateur ajoute ou supprime des membres des groupes de rôles d’administrateur, Microsoft Exchange Online Protection (EOP) journalise chaque occurrence.
ms.openlocfilehash: 6973574ca1eeabee85dd57bd087ba5d0675da084
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676506"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a><span data-ttu-id="25efc-104">Exécution d’un rapport de groupe de rôles d'administrateur dans EOP</span><span class="sxs-lookup"><span data-stu-id="25efc-104">Run an administrator role group report in EOP</span></span>

 <span data-ttu-id="25efc-105">Lorsqu’un administrateur ajoute ou supprime des membres dans les groupes de rôles d’administrateur, Exchange Online Protection (EOP) journalise chaque occurrence.</span><span class="sxs-lookup"><span data-stu-id="25efc-105">When an admin adds members to or removes members from administrator role groups, Exchange Online Protection (EOP) logs each occurrence.</span></span> <span data-ttu-id="25efc-106">Lorsque vous exécutez un rapport de groupe de rôles d’administrateur dans le centre d’administration Exchange, les entrées s’affichent sous la forme de résultats de recherche et incluent les groupes de rôles affectés, la personne qui a modifié l’appartenance au groupe de rôles et le moment, ainsi que les mises à jour d’appartenance.</span><span class="sxs-lookup"><span data-stu-id="25efc-106">When you run an administrator role group report in the Exchange admin center (EAC), entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made.</span></span> <span data-ttu-id="25efc-107">Utilisez ce rapport pour surveiller les modifications aux autorisations administratives attribuées aux utilisateurs dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="25efc-107">Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="25efc-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="25efc-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="25efc-109">Durée d'exécution estimée : 2 minutes</span><span class="sxs-lookup"><span data-stu-id="25efc-109">Estimated time to complete: 2 minutes</span></span>

- <span data-ttu-id="25efc-110">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="25efc-110">To open the Exchange admin center, see [Exchange admin center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="25efc-p103">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la section « Rapports » de la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="25efc-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Reports" section of the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span>

- <span data-ttu-id="25efc-113">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="25efc-113">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="25efc-114">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="25efc-114">Having problems?</span></span> <span data-ttu-id="25efc-115">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="25efc-115">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="25efc-116">Utiliser le Centre d'administration Exchange (CAE) pour exécuter un rapport de groupe de rôles d'administrateur</span><span class="sxs-lookup"><span data-stu-id="25efc-116">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="25efc-117">Exécutez le rapport de groupe de rôles d’administrateur pour rechercher les modifications apportées aux groupes de rôles de gestion dans votre organisation dans un intervalle de temps donné.</span><span class="sxs-lookup"><span data-stu-id="25efc-117">Run the administrator role group report to find the changes to management role groups in your organization within a particular time frame.</span></span>
  
1. <span data-ttu-id="25efc-118">Dans le CAE, accédez à **Gestion de la conformité** \> **Audit**, puis sélectionnez **Exécuter un rapport de groupe de rôles d'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="25efc-118">In the EAC, navigate to **Compliance management** \> **Auditing**, and choose **Run an administrator role group report**.</span></span>

2. <span data-ttu-id="25efc-p105">Sélectionnez la **date de début** et la **date de fin**. Par défaut, le rapport recherche toutes les modifications apportées aux groupes de rôles d'administrateur au cours des deux semaines passées.</span><span class="sxs-lookup"><span data-stu-id="25efc-p105">Choose the **Start date** and **End date**. By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>

3. <span data-ttu-id="25efc-p106">Pour afficher les modifications apportées à un groupe de rôles précis, cliquez sur **Sélectionnez les groupes de rôles**. Sélectionnez le ou les groupes de rôles dans la boîte de dialogue suivante, puis cliquez sur **OK**. Vous pouvez également laisser le champ vide pour rechercher tous les groupes de rôles qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="25efc-p106">To view the changes for a specific role group, click **Select role groups**. Select the role group (or groups) in the subsequent dialog box, and click **OK**. You can also leave the field blank to find all changed role groups.</span></span>

4. <span data-ttu-id="25efc-124">Cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="25efc-124">Click **Search**.</span></span>

<span data-ttu-id="25efc-p107">Si des modifications correspondent aux critères que vous avez spécifiés, elles seront affichées dans le volet des résultats. Cliquez sur un groupe de rôles dans les résultats de la recherche pour afficher les modifications dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="25efc-p107">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="25efc-127">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="25efc-127">How do you know this worked?</span></span>

<span data-ttu-id="25efc-p108">Si vous avez bien exécuté un rapport de groupe de rôles d'administrateur, les groupes de rôles qui ont été modifiés dans la plage de dates s'affichent dans le volet des résultats de la recherche. En cas d'absence de résultats, cela signifie qu'aucune modification aux groupes de rôles n'a eu lieu dans la plage de dates indiquée. Si vous pensez que des résultats devraient apparaître, modifiez la plage de dates et réexécutez le rapport.</span><span class="sxs-lookup"><span data-stu-id="25efc-p108">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>
  
## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="25efc-131">Surveillances des modifications apportées à l'appartenance à des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="25efc-131">Monitor changes to role group membership</span></span>

<span data-ttu-id="25efc-p109">Lorsque des membres sont ajoutés ou supprimés dans groupe de rôles, les résultats de la recherche affichés dans le volet d'informations indiquent que l'appartenance à un groupe de rôles a été mise à jour et répertorient les membres actuels. Les résultats n'indiquent pas explicitement quel utilisateur a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="25efc-p109">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>
  
<span data-ttu-id="25efc-p110">Pour déterminer si un utilisateur a été ajouté ou supprimé, vous devez comparer deux entrées séparées dans le rapport. Par exemple, examinons les entrées de journal suivantes pour le groupe de rôles **Support technique**:</span><span class="sxs-lookup"><span data-stu-id="25efc-p110">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span>
  
> <span data-ttu-id="25efc-136">1/27/2018 4:43 PM</span><span class="sxs-lookup"><span data-stu-id="25efc-136">1/27/2018 4:43 PM</span></span> <br> <span data-ttu-id="25efc-137">Administrateur</span><span class="sxs-lookup"><span data-stu-id="25efc-137">Administrator</span></span> <br> <span data-ttu-id="25efc-138">Membres mis à jour : Administrateur;annb,florencef;pilarp</span><span class="sxs-lookup"><span data-stu-id="25efc-138">Updated members: Administrator;annb,florencef;pilarp</span></span> <br> <span data-ttu-id="25efc-139">2/06/2018 10:09 AM</span><span class="sxs-lookup"><span data-stu-id="25efc-139">2/06/2018 10:09 AM</span></span> <br> <span data-ttu-id="25efc-140">Administrateur</span><span class="sxs-lookup"><span data-stu-id="25efc-140">Administrator</span></span> <br> <span data-ttu-id="25efc-141">Membres mis à jour : Administrator;annb;florencef;pilarp;tonip</span><span class="sxs-lookup"><span data-stu-id="25efc-141">Updated members: Administrator;annb;florencef;pilarp;tonip</span></span> <br> <span data-ttu-id="25efc-142">2/19/2018 2:12 PM</span><span class="sxs-lookup"><span data-stu-id="25efc-142">2/19/2018 2:12 PM</span></span> <br> <span data-ttu-id="25efc-143">Administrateur</span><span class="sxs-lookup"><span data-stu-id="25efc-143">Administrator</span></span> <br> <span data-ttu-id="25efc-144">Membres mis à jour : Administrator;annb;florencef;tonip</span><span class="sxs-lookup"><span data-stu-id="25efc-144">Updated members: Administrator;annb;florencef;tonip</span></span>

<span data-ttu-id="25efc-145">Dans cet exemple, le compte d'utilisateur Administrateur a apporté les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="25efc-145">In this example, the Administrator user account made the following changes:</span></span>
  
- <span data-ttu-id="25efc-146">Le 2/06/2018, il a ajouté l’utilisateur tonip.</span><span class="sxs-lookup"><span data-stu-id="25efc-146">On 2/06/2018, they added the user tonip.</span></span>

- <span data-ttu-id="25efc-147">Le 2/19/2018, il a supprimé l’utilisateur pilarp.</span><span class="sxs-lookup"><span data-stu-id="25efc-147">On 2/19/2018, they removed the user pilarp.</span></span>
