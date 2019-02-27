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
ms.openlocfilehash: 95a1bcbbc279ad4e476fc479e701b0f8a921c83b
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295677"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="ed5d4-102">Gestion des dépositaires dans un cas avancé eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="ed5d4-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="ed5d4-p101">L'onglet dépositaires contient une liste triable de tous les dépositaires dans le cas. Une fois que vous avez ajouté des dépositaires à un cas, les détails de chaque dépositaire seront automatiquement collectés à partir d'Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="ed5d4-105">Affichage des détails des dépositaires</span><span class="sxs-lookup"><span data-stu-id="ed5d4-105">Viewing custodian details</span></span>

<span data-ttu-id="ed5d4-p102">La page de menu volant contenant les détails des dépositaires s'affiche une fois que vous avez ajouté un dépositaire à une demande \*\*\*\* de devis et que vous l'avez sélectionné dans la liste de l'onglet dépositaires. À partir de là, vous pouvez afficher tous les détails relatifs à ce dépositaire. La page de menu volant contient les champs suivants:</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="ed5d4-108">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="ed5d4-108">Contact information</span></span>

  - <span data-ttu-id="ed5d4-p103">**Nom d'affichage**: nom affiché dans le carnet d'adresses pour le dépositaire. Il s'agit généralement de la combinaison du prénom du dépositaire, de l'initiale du deuxième prénom et du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="ed5d4-111">**Mail/SMTP**: adresse SMTP du dépositaire, par exemple, Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="ed5d4-112">**Titre**: fonction du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="ed5d4-113">**Department**: nom du service dans lequel le dépositaire travaille.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="ed5d4-p104">**Responsable**: le responsable du dépositaire. Le responsable désigné recevra toutes les communications d'escalade de ce dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="ed5d4-116">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="ed5d4-116">Location information</span></span>

  - <span data-ttu-id="ed5d4-117">**Ville**: ville dans laquelle se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="ed5d4-118">**État**: État ou province dans l'adresse du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="ed5d4-119">**Pays/région**: pays/région où se trouve le dépositaire; par exemple, «US» ou «UK».</span><span class="sxs-lookup"><span data-stu-id="ed5d4-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="ed5d4-120">**Office**: l'emplacement du bureau dans le lieu d'activité du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="ed5d4-121">Informations sur les cas</span><span class="sxs-lookup"><span data-stu-id="ed5d4-121">Case information</span></span>

  - <span data-ttu-id="ed5d4-122">**État de suspension**: indique si le dépositaire a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="ed5d4-p105">**Statut**de la communication: indique si un avis de mise en attente a été émis pour le dépositaire. Si le dépositaire a reçu une notification, celle-ci sera marquée comme étant *publiée*. Si le dépositaire n'a pas reçu de notification, ce statut est *annulé*.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="ed5d4-p106">**État**: état du dépositaire dans le cas. Cela sera *actif* si le dépositaire est toujours en conservation pour le cas. Si un dépositaire est supprimé d'un incident, son statut passe à *lancé*.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="ed5d4-129">État de traitement</span><span class="sxs-lookup"><span data-stu-id="ed5d4-129">Processing status</span></span>

  - <span data-ttu-id="ed5d4-130">**État**de l'indexation: indique l'état de la tâche d'indexation approfondie.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="ed5d4-131">**Indexation de la dernière heure de mise à jour**: indique l'datestamp de la dernière fois que le travail d'indexation profonde a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="ed5d4-132">**Sources de données**: affiche le nombre de boîtes aux lettres, de sites et d'équipes qui ont été sélectionnées pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="ed5d4-133">Mise à jour d'un dépositaire</span><span class="sxs-lookup"><span data-stu-id="ed5d4-133">Updating a custodian</span></span>

<span data-ttu-id="ed5d4-p107">Lors de l'évolution de votre cas, vous pouvez découvrir qu'il peut y avoir des sources de données supplémentaires pertinentes pour un dépositaire spécifique & votre cas. Dans d'autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été vérifiées et considérées comme non pertinentes.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="ed5d4-136">Pour mettre à jour un dépositaire et les sources de données sélectionnées:</span><span class="sxs-lookup"><span data-stu-id="ed5d4-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="ed5d4-137">Sélectionnez un incident existant dans la découverte **électronique avancée _GT_ Advanced eDiscovery (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="ed5d4-138">Dans le cas, cliquez sur \*\*\*\* l'onglet dépositaires.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="ed5d4-139">Sélectionnez le ou les dépositaires dans la liste, puis cliquez sur **modifier les sources**.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="ed5d4-140">Mettez à jour les sélections pour les emplacements Exchange et OneDrive en cliquant sur **choisir les sources de données**.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="ed5d4-p108">Ajouter ou supprimer des équipes, SharePoint ou des boîtes aux lettres Exchange mappées à l'utilisateur en cliquant pour **Sélectionner des sources de données supplémentaires**. Pour plus d'informations sur la façon de mapper des sources de données à un dépositaire, consultez la rubrique [Ajouter des dépositaires à un cas](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="ed5d4-143">Pour mettre à jour l'état de conservation des dépositaires, cliquez sur **Placer**les conservations privatives de Troie et activez ou désactivez la suspension pour les dépositaires.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="ed5d4-144">Vous pouvez sélectionner plusieurs dépositaires pour effectuer des actions en bloc, comme la réindexation, le lancement ou la modification d'un ensemble de dépositaires.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="ed5d4-145">Résolution des erreurs de traitement des dépositaires</span><span class="sxs-lookup"><span data-stu-id="ed5d4-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="ed5d4-p109">Dans la plupart des flux de travail légaux, après avoir ajouté des dépositaires à une enquête spécifique, un sous-ensemble des données des utilisateurs est recherché. En raison de la taille des fichiers volumineux ou d'une altération possible, certains éléments des sources de données des dépositaires peuvent être partiellement indexés. À l'aide de la fonctionnalité d'indexation approfondie avancée eDiscovery (aperçu), ces éléments partiellement indexés peuvent être automatiquement corrigés en réanalysant et en réindexant ces éléments à la demande.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="ed5d4-p110">Lorsqu'un dépositaire est ajouté à un cas, ses données sont automatiquement «indexées en profondeur», ce qui permet aux utilisateurs de laisser ces éléments partiellement indexés au lieu de devoir télécharger, corriger et réexécuter les recherches en dehors d'Office 365. Pendant le cycle de vie d'un cas, un utilisateur peut corriger des éléments ou ajouter de nouvelles sources de données pour un dépositaire donné. Cela peut nécessiter la mise à jour de l'index des dépositaires.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="ed5d4-152">Pour déclencher un processus de réindexation afin d'adresser des éléments partiellement indexés:</span><span class="sxs-lookup"><span data-stu-id="ed5d4-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="ed5d4-153">Accédez à **eDiscovery _GT_ Advanced eDiscovery (Preview)** et sélectionnez un incident existant.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="ed5d4-154">Dans le cas, cliquez sur l' **onglet dépositaires**.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="ed5d4-155">Sélectionnez le ou les dépositaires qui doivent être réindexés, puis cliquez sur **mettre à jour l'index** sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="ed5d4-156">Vérifiez l'état de l'index dépositaire en cliquant sur le lien dans la colonne **État du travail d'indexation** sous l'onglet **dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="ed5d4-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="ed5d4-157">L'état du processus de réindexation peut également être suivi sous l'onglet **tâches** .</span><span class="sxs-lookup"><span data-stu-id="ed5d4-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="ed5d4-158">Pour plus d'informations sur la réindexation et la correction des éléments partiellement indexés, voir [Fix Processing Errors](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="ed5d4-158">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="ed5d4-159">Libération d'un dépositaire à partir d'un cas</span><span class="sxs-lookup"><span data-stu-id="ed5d4-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="ed5d4-160">Un dépositaire est publié dans les situations où un litige est clos, un dépositaire n'est plus tenu de conserver le contenu d'un cas ou lorsqu'un dépositaire est considéré comme n'étant plus pertinent à un cas particulier.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="ed5d4-p111">Si vous libérez un dépositaire après la publication d'une notification de mise en attente, un avis de publication est envoyé au dépositaire. En outre, toutes les conservations privatives de Troie attribuées aux dépositaires libérés seront également supprimées.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="ed5d4-163">Si le dépositaire a été placé sur un blocage automatique, où il n'a pas reçu de notifications de conservation légale, toutes les conservations privatives attribuées aux dépositaires libérés seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="ed5d4-164">Pour libérer un dépositaire:</span><span class="sxs-lookup"><span data-stu-id="ed5d4-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="ed5d4-165">Accédez à l' \*\*\*\* onglet dépositaires.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="ed5d4-166">Sélectionnez le dépositaire dans la liste, puis cliquez sur **libérer** les dépositaires sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="ed5d4-167">Le statut du dépositaire sous l'onglet **dépositaires** est défini sur **Released** et le **statut de blocage** sur la page flyout est modifié sur inactive. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ed5d4-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="ed5d4-p112">Un dépositaire peut être impliqué simultanément dans plusieurs questions juridiques. Lorsqu'un dépositaire est émis à partir d'un cas, les conservations et notifications sur d'autres sujets ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="ed5d4-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="ed5d4-170">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="ed5d4-170">Related information</span></span>

 - [<span data-ttu-id="ed5d4-171">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="ed5d4-171">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="ed5d4-172">Utiliser des communications</span><span class="sxs-lookup"><span data-stu-id="ed5d4-172">Work with communications</span></span>](managing-custodian-communications.md)
