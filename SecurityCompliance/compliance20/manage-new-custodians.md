---
title: Gestion des dépositaires dans un cas eDiscovery avancées (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607717"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="6f350-102">Gestion des dépositaires dans un cas eDiscovery avancées (Preview)</span><span class="sxs-lookup"><span data-stu-id="6f350-102">Managing custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="6f350-p101">L’onglet dépositaires contient une liste triable de tous les dépositaires dans ce cas. Après avoir ajouté dépositaires à un cas, plus d’informations sur chaque dépositaire seront automatiquement collectées d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6f350-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="6f350-105">Affichage des détails dépositaire</span><span class="sxs-lookup"><span data-stu-id="6f350-105">Viewing custodian details</span></span>

<span data-ttu-id="6f350-p102">La page flottant qui contient des détails dépositaire s’affiche après avoir ajouté un dépositaire à un cas et que vous les sélectionnez dans la liste sous l’onglet **dépositaires** . À partir de là, vous pouvez afficher tous les détails associés à ce dépositaire. La page flottant contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="6f350-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="6f350-108">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="6f350-108">Contact information</span></span>

  - <span data-ttu-id="6f350-p103">**Nom complet**: le nom affiché dans le carnet d’adresses pour le dépositaire. Il s’agit généralement de la combinaison du prénom de le dépositaire, initiale et le nom du milieu.</span><span class="sxs-lookup"><span data-stu-id="6f350-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="6f350-111">**/ SMTP Mail**: adresse SMTP le pour le dépositaire, par exemple, jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6f350-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="6f350-112">**Titre**: la fonction du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6f350-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="6f350-113">**Service**: le nom du service dans lequel fonctionne le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6f350-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="6f350-p104">**Responsable**: responsable du dépositaire. Le responsable désigné reçoit toutes les communications pour cet dépositaire escalade.</span><span class="sxs-lookup"><span data-stu-id="6f350-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="6f350-116">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="6f350-116">Location information</span></span>

  - <span data-ttu-id="6f350-117">**Ville**: la ville dans laquelle se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6f350-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="6f350-118">**State**: état ou province dans l’adresse du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6f350-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="6f350-119">**Pays/région**: la pays/la région dans laquelle se trouve le dépositaire ; par exemple, « US » ou « Royaume-Uni ».</span><span class="sxs-lookup"><span data-stu-id="6f350-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="6f350-120">**Office**: l’emplacement de bureau en place du dépositaire de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6f350-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="6f350-121">Informations d’un incident</span><span class="sxs-lookup"><span data-stu-id="6f350-121">Case information</span></span>

  - <span data-ttu-id="6f350-122">**État de blocage**: indique si le dépositaire a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="6f350-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="6f350-p105">**État de communication**: indique si le dépositaire a reçu un avis de suspension. Si le dépositaire a reçu un avis, ce sera marqué comme étant *publiée*. Si le dépositaire n’a pas été émis un avis, puis ce statut sera *non publié*.</span><span class="sxs-lookup"><span data-stu-id="6f350-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="6f350-p106">**État**: l’état de la dépositaire dans le cas. Il s’agit *Active* si le dépositaire est toujours en attente pour le cas. Si un dépositaire est supprimé à partir d’un cas, leur statut devient *lancé*.</span><span class="sxs-lookup"><span data-stu-id="6f350-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="6f350-129">Statut de traitement</span><span class="sxs-lookup"><span data-stu-id="6f350-129">Processing status</span></span>

  - <span data-ttu-id="6f350-130">**État de l’indexation**: indique l’état de la tâche d’indexation en profondeur.</span><span class="sxs-lookup"><span data-stu-id="6f350-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="6f350-131">**Heure de mise à jour de la dernière indexation**: indique le datestamp de lorsque la tâche d’indexation approfondie a été déclenchée pour la dernière.</span><span class="sxs-lookup"><span data-stu-id="6f350-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="6f350-132">**Sources de données**: indique le nombre de boîtes aux lettres, les sites et les équipes qui ont été sélectionnées pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6f350-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="6f350-133">Mise à jour un dépositaire</span><span class="sxs-lookup"><span data-stu-id="6f350-133">Updating a custodian</span></span>

<span data-ttu-id="6f350-p107">Fur et à votre cas, vous pouvez constater qu’il peuvent exister des sources de données supplémentaires pertinents pour un & spécifique dépositaire votre cas. Dans d’autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été révisées et considérés comme non pertinents.</span><span class="sxs-lookup"><span data-stu-id="6f350-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="6f350-136">Pour mettre à jour un dépositaire et les sources de données sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="6f350-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="6f350-137">Sélectionnez un incident existant à partir de **découverte électronique > eDiscovery avancées (Preview)**.</span><span class="sxs-lookup"><span data-stu-id="6f350-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="6f350-138">Dans ce cas, cliquez sur l’onglet **dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="6f350-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="6f350-139">Sélectionnez le custodian(s) dans la liste, cliquez sur **Modifier les sources**.</span><span class="sxs-lookup"><span data-stu-id="6f350-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="6f350-140">Mettre à jour les sélections pour Exchange et OneDrive les emplacements en cliquant sur **Choisir des sources de données**.</span><span class="sxs-lookup"><span data-stu-id="6f350-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="6f350-p108">Ajouter ou supprimer des équipes, SharePoint ou Exchange boîtes aux lettres mappées l’utilisateur en cliquant sur Sélectionner les **sources de données supplémentaires**. Pour plus d’informations sur la façon dont vous permettent de mapper les données sources pour un dépositaire, voir [Ajouter dépositaires à une découverte électronique avancée (Preview) cas](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="6f350-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to an Advanced eDiscovery (Preview) Case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="6f350-143">Pour mettre à jour l’état de conservation dépositaire, cliquez sur **garde archives permanentes**et activer ou désactiver la suspension pour dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6f350-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="6f350-144">Vous pouvez sélectionner plusieurs dépositaires pour effectuer les actions en bloc, telles que la réindexation, l’annulation ou modification d’un jeu de dépositaires.</span><span class="sxs-lookup"><span data-stu-id="6f350-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="6f350-145">Résolution des erreurs de traitement dépositaire</span><span class="sxs-lookup"><span data-stu-id="6f350-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="6f350-p109">Dans la plupart des flux de travail juridique, après que dépositaires sont ajoutés à une enquête spécifique, un sous-ensemble de données d’utilisateurs est recherché. En raison de fichiers volumineux ou l’endommagement possible, certains éléments dans des sources de données des dépositaires peuvent être partiellement indexées. À l’aide de la fonctionnalité d’indexation approfondie eDiscovery avancées (Preview), ces éléments indexés partiellement peuvent être automatiquement convertis en nouvelle analyse et une réindexation de ces éléments à la demande.</span><span class="sxs-lookup"><span data-stu-id="6f350-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="6f350-p110">Lorsqu’un dépositaire est ajouté à un cas, leurs données seront automatiquement « profondeur indexées », qui permet aux utilisateurs de laisser ces partiellement indexée éléments place au lieu de devoir télécharger, corriger et exécutez de nouveau les recherches en dehors d’Office 365. Pendant le cycle de vie d’un incident, un utilisateur peut résoudre les éléments ou ajouter de nouvelles sources de données pour un dépositaire donné. Cela peut nécessiter l’Index dépositaire à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="6f350-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="6f350-152">Pour déclencher un processus de renouvellement d’indexation adresse partiellement des éléments indexés :</span><span class="sxs-lookup"><span data-stu-id="6f350-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="6f350-153">Accédez à la **découverte électronique > avancée découverte électronique (Preview)** et sélectionnez un incident existant.</span><span class="sxs-lookup"><span data-stu-id="6f350-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="6f350-154">Dans ce cas, cliquez sur à **onglet dépositaires**.</span><span class="sxs-lookup"><span data-stu-id="6f350-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="6f350-155">Sélectionnez le custodian(s) devant réindexation, puis cliquez sur **index de la mise à jour** dans la page mobile.</span><span class="sxs-lookup"><span data-stu-id="6f350-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="6f350-156">Vérifier l’état de l’index de dépositaire en cliquant sur le lien dans la colonne **travail indexation état** sous l’onglet **dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="6f350-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="6f350-157">L’état pour le processus de renouvellement d’indexation peut être suivi également dans l’onglet **tâches** .</span><span class="sxs-lookup"><span data-stu-id="6f350-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="6f350-158">Pour plus d’informations sur les éléments indexés partiellement nouveau indexation et correction, voir [fixation de traitement des erreurs d’eDiscovery avancée (Preview)](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="6f350-158">For more information about re-indexing and remediating partially indexed items, see [Fixing processing errors in Advanced eDiscovery (Preview)](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="6f350-159">Libération d’un dépositaire à partir d’un cas</span><span class="sxs-lookup"><span data-stu-id="6f350-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="6f350-160">Un dépositaire est publié dans les situations de cas où un incident est fermé, un dépositaire n’est plus tenu de conserver le contenu d’un cas ou lorsqu’un dépositaire est considéré comme pas plus être pertinentes à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="6f350-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="6f350-p111">Si vous relâchez un dépositaire après qu’un avis de suspension a été publié, une note de version est envoyé vers le dépositaire. En outre, les suspensions garde attribuées aux version finale dépositaires seront également supprimées.</span><span class="sxs-lookup"><span data-stu-id="6f350-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="6f350-163">Si le dépositaire a été placé sur une suspension en mode silencieux, où ils ont été délivrés pas les notifications de conservation légale, alors les suspensions garde attribuées aux version finale dépositaires seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="6f350-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="6f350-164">Pour libérer un dépositaire :</span><span class="sxs-lookup"><span data-stu-id="6f350-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="6f350-165">Accédez à l’onglet **dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="6f350-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="6f350-166">Sélectionnez le dépositaire dans la liste et cliquez sur **dépositaires version** dans la page mobile.</span><span class="sxs-lookup"><span data-stu-id="6f350-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="6f350-167">L’état de la dépositaire sous l’onglet **dépositaires** est défini sur **lancé** et l' **état de blocage** sur la page flottant est modifiée à **inactif/Inactive**.</span><span class="sxs-lookup"><span data-stu-id="6f350-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="6f350-p112">Un dépositaire peut être simultanément être impliqués dans plusieurs domaines de conservation légale. Lorsque l’utilisateur relâche un dépositaire à partir d’un cas, les suspensions et les notifications entre autres questions ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="6f350-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="6f350-170">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="6f350-170">Related information</span></span>

 - <span data-ttu-id="6f350-171">Attributs de l’utilisateur dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="6f350-171">User Attributes in Active Directory</span></span> 
 - [<span data-ttu-id="6f350-172">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="6f350-172">Error remediation when processing data</span></span>](error-remediation.md) 
 - [<span data-ttu-id="6f350-173">Utilisation des communications</span><span class="sxs-lookup"><span data-stu-id="6f350-173">Working with communications</span></span>](managing-custodian-communications.md)
