---
title: Gestion des dépositaires dans un cas avancé eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 6a21240f71c64f244ee42c3d3a2ed9d75381edaa
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454936"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="6879a-102">Gestion des dépositaires dans un cas avancé eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="6879a-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="6879a-103">L'onglet dépositaires contient une liste triable de tous les dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="6879a-103">The Custodians tab contains a sortable list of all the custodians in the case.</span></span> <span data-ttu-id="6879a-104">Une fois que vous avez ajouté des dépositaires à un cas, les détails de chaque dépositaire seront automatiquement collectés à partir d'Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6879a-104">After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

![Gestion des dépositaires](../media/CustodianDetails.PNG)

## <a name="viewing-custodian-details"></a><span data-ttu-id="6879a-106">Affichage des détails des dépositaires</span><span class="sxs-lookup"><span data-stu-id="6879a-106">Viewing custodian details</span></span>

<span data-ttu-id="6879a-107">La page de menu volant contenant les détails des dépositaires s'affiche une fois que vous avez ajouté un dépositaire à une demande \*\*\*\* de devis et que vous l'avez sélectionné dans la liste de l'onglet dépositaires. À partir de là, vous pouvez afficher tous les détails relatifs à ce dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-107">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian.</span></span> <span data-ttu-id="6879a-108">La page de menu volant contient les champs suivants:</span><span class="sxs-lookup"><span data-stu-id="6879a-108">The flyout page contains the following fields:</span></span>

- <span data-ttu-id="6879a-109">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="6879a-109">Contact information</span></span>

  - <span data-ttu-id="6879a-110">**Nom d'affichage**: nom affiché dans le carnet d'adresses pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-110">**Display Name**: The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="6879a-111">Il s'agit généralement de la combinaison du prénom du dépositaire, de l'initiale du deuxième prénom et du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="6879a-111">This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="6879a-112">**Mail/SMTP**: adresse SMTP du dépositaire, par exemple, Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6879a-112">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="6879a-113">**Titre**: fonction du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-113">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="6879a-114">**Department**: nom du service dans lequel le dépositaire travaille.</span><span class="sxs-lookup"><span data-stu-id="6879a-114">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="6879a-115">**Responsable**: le responsable du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-115">**Manager**: The custodian’s manager.</span></span> <span data-ttu-id="6879a-116">Le responsable désigné recevra toutes les communications d'escalade de ce dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-116">The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="6879a-117">Informations d'emplacement</span><span class="sxs-lookup"><span data-stu-id="6879a-117">Location information</span></span>

  - <span data-ttu-id="6879a-118">**Ville**: ville dans laquelle se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-118">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="6879a-119">**État**: État ou province dans l'adresse du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-119">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="6879a-120">**Pays/région**: pays/région où se trouve le dépositaire; par exemple, «US» ou «UK».</span><span class="sxs-lookup"><span data-stu-id="6879a-120">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="6879a-121">**Office**: l'emplacement du bureau dans le lieu d'activité du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-121">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="6879a-122">Informations sur les cas</span><span class="sxs-lookup"><span data-stu-id="6879a-122">Case information</span></span>

  - <span data-ttu-id="6879a-123">**État de suspension**: indique si le dépositaire a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="6879a-123">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="6879a-124">**Statut**de la communication: indique si un avis de mise en attente a été émis pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-124">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="6879a-125">Si le dépositaire a reçu une notification, celle-ci sera marquée comme étant *publiée*.</span><span class="sxs-lookup"><span data-stu-id="6879a-125">If the custodian has been issued a notice, then this will be marked as *Published*.</span></span> <span data-ttu-id="6879a-126">Si le dépositaire n'a pas reçu de notification, ce statut est *annulé*.</span><span class="sxs-lookup"><span data-stu-id="6879a-126">If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="6879a-127">**État**: état du dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="6879a-127">**Status**: The status of the custodian within the case.</span></span> <span data-ttu-id="6879a-128">Cela sera *actif* si le dépositaire est toujours en conservation pour le cas.</span><span class="sxs-lookup"><span data-stu-id="6879a-128">This will be *Active* if the custodian is still on hold for the case.</span></span> <span data-ttu-id="6879a-129">Si un dépositaire est supprimé d'un incident, son statut passe à *lancé*.</span><span class="sxs-lookup"><span data-stu-id="6879a-129">If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="6879a-130">État de traitement</span><span class="sxs-lookup"><span data-stu-id="6879a-130">Processing status</span></span>

  - <span data-ttu-id="6879a-131">**État**de l'indexation: indique l'état de la tâche d'indexation approfondie.</span><span class="sxs-lookup"><span data-stu-id="6879a-131">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="6879a-132">**Indexation de la dernière heure de mise à jour**: indique l'datestamp de la dernière fois que le travail d'indexation profonde a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="6879a-132">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="6879a-133">**Sources de données**: affiche le nombre de boîtes aux lettres, de sites et d'équipes qui ont été sélectionnées pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-133">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="editing-a-custodian"></a><span data-ttu-id="6879a-134">Modification d'un dépositaire</span><span class="sxs-lookup"><span data-stu-id="6879a-134">Editing a custodian</span></span>

<span data-ttu-id="6879a-135">Lors de l'évolution de votre cas, vous pouvez découvrir qu'il peut y avoir des sources de données supplémentaires pertinentes pour un dépositaire spécifique & votre cas.</span><span class="sxs-lookup"><span data-stu-id="6879a-135">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="6879a-136">Dans d'autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été vérifiées et considérées comme non pertinentes.</span><span class="sxs-lookup"><span data-stu-id="6879a-136">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="6879a-137">Pour mettre à jour un dépositaire et les sources de données sélectionnées:</span><span class="sxs-lookup"><span data-stu-id="6879a-137">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="6879a-138">Sélectionnez un incident existant dans la découverte **électronique avancée _GT_ Advanced eDiscovery (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="6879a-138">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="6879a-139">Dans le cas, cliquez sur \*\*\*\* l'onglet dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6879a-139">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="6879a-140">Sélectionnez le ou les dépositaires dans la liste, puis cliquez sur **modifier les sources**.</span><span class="sxs-lookup"><span data-stu-id="6879a-140">Select the custodian(s) from the list and click **Edit sources**.</span></span>

    ![Modifier des sources de données](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="6879a-142">Mettez à jour les sélections pour les emplacements Exchange et OneDrive en cliquant sur **choisir les sources de données**.</span><span class="sxs-lookup"><span data-stu-id="6879a-142">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="6879a-143">Ajouter ou supprimer des équipes, SharePoint ou des boîtes aux lettres Exchange mappées à l'utilisateur en cliquant pour **Sélectionner des sources de données supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="6879a-143">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**.</span></span> <span data-ttu-id="6879a-144">Pour plus d'informations sur la façon de mapper des sources de données à un dépositaire, consultez la rubrique [Ajouter des dépositaires à un cas](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="6879a-144">For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="6879a-145">Pour mettre à jour l'état de conservation des dépositaires, cliquez sur **Placer**les conservations privatives de Troie et activez ou désactivez la suspension pour les dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6879a-145">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="6879a-146">Vous pouvez sélectionner plusieurs dépositaires pour effectuer des actions en bloc, comme la réindexation, le lancement ou la modification d'un ensemble de dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6879a-146">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="6879a-147">Résolution des erreurs de traitement des dépositaires</span><span class="sxs-lookup"><span data-stu-id="6879a-147">Resolving custodian processing errors</span></span>

<span data-ttu-id="6879a-148">Dans la plupart des flux de travail légaux, après avoir ajouté des dépositaires à une enquête spécifique, un sous-ensemble des données des utilisateurs est recherché.</span><span class="sxs-lookup"><span data-stu-id="6879a-148">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched.</span></span> <span data-ttu-id="6879a-149">En raison de la taille des fichiers volumineux ou d'une altération possible, certains éléments des sources de données des dépositaires peuvent être partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="6879a-149">Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed.</span></span> <span data-ttu-id="6879a-150">À l'aide de la fonctionnalité d'indexation approfondie avancée eDiscovery (aperçu), ces éléments partiellement indexés peuvent être automatiquement corrigés en réanalysant et en réindexant ces éléments à la demande.</span><span class="sxs-lookup"><span data-stu-id="6879a-150">Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="6879a-151">Lorsqu'un dépositaire est ajouté à un cas, ses données sont automatiquement «indexées en profondeur», ce qui permet aux utilisateurs de laisser ces éléments partiellement indexés au lieu de devoir télécharger, corriger et réexécuter les recherches en dehors d'Office 365.</span><span class="sxs-lookup"><span data-stu-id="6879a-151">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365.</span></span> <span data-ttu-id="6879a-152">Pendant le cycle de vie d'un cas, un utilisateur peut corriger des éléments ou ajouter de nouvelles sources de données pour un dépositaire donné.</span><span class="sxs-lookup"><span data-stu-id="6879a-152">During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian.</span></span> <span data-ttu-id="6879a-153">Cela peut nécessiter la mise à jour de l'index des dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6879a-153">This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="6879a-154">Pour déclencher un processus de réindexation afin d'adresser des éléments partiellement indexés:</span><span class="sxs-lookup"><span data-stu-id="6879a-154">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="6879a-155">Accédez à **eDiscovery _GT_ Advanced eDiscovery (Preview)** et sélectionnez un incident existant.</span><span class="sxs-lookup"><span data-stu-id="6879a-155">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="6879a-156">Dans le cas, cliquez sur l' **onglet dépositaires**.</span><span class="sxs-lookup"><span data-stu-id="6879a-156">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="6879a-157">Sélectionnez le ou les dépositaires qui doivent être réindexés, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="6879a-157">Select the custodian(s) that needs to be re-indexed, and then click</span></span> ![Mettre à jour l'index](../media/UpdateIndex.PNG) <span data-ttu-id="6879a-159">sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="6879a-159">on the flyout page.</span></span>

4. <span data-ttu-id="6879a-160">Vérifiez l'état de l'index dépositaire en cliquant sur le lien dans la colonne **État du travail d'indexation** sous l'onglet **dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="6879a-160">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="6879a-161">L'état du processus de réindexation peut également être suivi sous l'onglet **tâches** .</span><span class="sxs-lookup"><span data-stu-id="6879a-161">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="6879a-162">Pour plus d'informations sur la réindexation et la correction des éléments partiellement indexés, voir [Fix Processing Errors](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="6879a-162">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="6879a-163">Libération d'un dépositaire à partir d'un cas</span><span class="sxs-lookup"><span data-stu-id="6879a-163">Releasing a custodian from a case</span></span>

<span data-ttu-id="6879a-164">Un dépositaire est publié dans les situations où un litige est clos, un dépositaire n'est plus tenu de conserver le contenu d'un cas ou lorsqu'un dépositaire est considéré comme n'étant plus pertinent à un cas particulier.</span><span class="sxs-lookup"><span data-stu-id="6879a-164">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="6879a-165">Si vous libérez un dépositaire après la publication d'une notification de mise en attente, un avis de publication est envoyé au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6879a-165">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="6879a-166">En outre, toutes les conservations privatives de Troie attribuées aux dépositaires libérés seront également supprimées.</span><span class="sxs-lookup"><span data-stu-id="6879a-166">In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="6879a-167">Si le dépositaire a été placé sur un blocage automatique, où il n'a pas reçu de notifications de conservation légale, toutes les conservations privatives attribuées aux dépositaires libérés seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="6879a-167">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="6879a-168">Pour libérer un dépositaire:</span><span class="sxs-lookup"><span data-stu-id="6879a-168">To release a custodian:</span></span> 

1.  <span data-ttu-id="6879a-169">Accédez à l' \*\*\*\* onglet dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6879a-169">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="6879a-170">Sélectionnez le dépositaire dans la liste, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="6879a-170">Select the custodian from the list and click</span></span> ![DéBloquer le dépositaire](../media/ReleaseCustodian.PNG) <span data-ttu-id="6879a-172">sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="6879a-172">on the flyout page.</span></span>

    <span data-ttu-id="6879a-173">Le statut du dépositaire sous l'onglet **dépositaires** est défini sur **Released** et le **statut de blocage** sur la page flyout est modifié sur inactive. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6879a-173">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="6879a-174">Un dépositaire peut être impliqué simultanément dans plusieurs questions juridiques.</span><span class="sxs-lookup"><span data-stu-id="6879a-174">A custodian might be simultaneously be involved in several legal hold matters.</span></span> <span data-ttu-id="6879a-175">Lorsqu'un dépositaire est émis à partir d'un cas, les conservations et notifications sur d'autres sujets ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="6879a-175">When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="6879a-176">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="6879a-176">Related information</span></span>

 - [<span data-ttu-id="6879a-177">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="6879a-177">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="6879a-178">Utiliser des communications</span><span class="sxs-lookup"><span data-stu-id="6879a-178">Work with communications</span></span>](managing-custodian-communications.md)
