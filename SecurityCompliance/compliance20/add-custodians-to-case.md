---
title: Ajouter des dépositaires à un cas avancé eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c36e0a2228db042d50361460e2e22f13556e8715
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218214"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="9ad4e-102">Ajouter des dépositaires à un cas avancé eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="9ad4e-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="9ad4e-p101">Advanced eDiscovery (aperçu) vous permet d'utiliser l'outil de gestion des dépositaires intégré pour coordonner vos flux de travail en matière de gestion des dépositaires et d'identification des sources de données appropriées dans un cas. Lorsque vous ajoutez un dépositaire, le système peut automatiquement identifier et placer des suspensions sur sa boîte aux lettres Exchange principale et sur le site OneDrive entreprise. Lors de votre découverte, vous pouvez également dévoiler et mapper des boîtes aux lettres ou des sites supplémentaires auxquels un dépositaire est accédé par le passé ou teams dont le dépositaire est membre.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="9ad4e-106">Utilisez le flux de travail suivant pour ajouter et gérer des dépositaires dans les cas avancés de découverte électronique (préversion) dans le centre de sécurité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="9ad4e-107">Étape 1: identifier les dépositaires potentiels</span><span class="sxs-lookup"><span data-stu-id="9ad4e-107">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="9ad4e-p102">La première étape consiste à identifier les dépositaires appropriés pour votre question. Pour ajouter des dépositaires à un cas, vous devez être membre du groupe de rôles gestionnaires eDiscovery ou administrateurs eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

<span data-ttu-id="9ad4e-110">Pour ajouter des dépositaires à une sacoche eDiscovery (préversion) avancée existante:</span><span class="sxs-lookup"><span data-stu-id="9ad4e-110">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="9ad4e-111">À partir de la page **Advanced eDiscovery (aperçu)** , accédez à votre cas.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-111">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="9ad4e-112">Une fois que vous avez sélectionné un cas, accédez \*\*\*\* à l'onglet dépositaires et cliquez sur **+ Ajouter un dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-112">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="9ad4e-p103">Choisissez les dépositaires que vous souhaitez ajouter à l'incident. Vous pouvez commencer par taper pour rechercher et sélectionner les utilisateurs dans Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="9ad4e-115">Après avoir finalisé la liste des dépositaires, cliquez sur **suivant** pour commencer à identifier les sources de données potentielles.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-115">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
   
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="9ad4e-116">Module Étape 2: sélection des sources de données du dépositaire</span><span class="sxs-lookup"><span data-stu-id="9ad4e-116">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="9ad4e-p104">Une fois que vous avez ajouté des dépositaires à un cas, vous pouvez tirer parti d'Office 365 pour vous aider à identifier et à conserver les sources de données des dépositaires principaux. L'étape suivante de ce flux de travail consiste à sélectionner les sources de données appartenant aux dépositaires spécifiées à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

<span data-ttu-id="9ad4e-119">Pour identifier les sources de données des dépositaires:</span><span class="sxs-lookup"><span data-stu-id="9ad4e-119">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="9ad4e-120">Pour chaque dépositaire, sélectionnez **Exchange** si vous souhaitez que le système identifie automatiquement et ajoute la boîte aux lettres Exchange principale du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-120">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="9ad4e-121">Pour chaque dépositaire, sélectionnez **OneDrive** si vous voulez que le système identifie automatiquement et ajoute l'URL onedrive principale du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-121">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="9ad4e-122">Une fois que vous avez effectué vos sélections, le système tente automatiquement d'identifier les sources de données et de les ajouter à votre cas.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-122">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="9ad4e-123">Cliquez sur **suivant** pour commencer à mapper des sources de données supplémentaires à votre dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-123">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="9ad4e-124">Module Étape 3: mapper des sources de données supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9ad4e-124">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="9ad4e-p105">En fonction de votre cas, vous pouvez également ajouter des boîtes aux lettres qu'un dépositaire donné a peut-être utilisé dans le passé, des groupes pour lesquels un dépositaire est actuellement membre ou des sites auxquels un dépositaire a accès dans le passé. En plus des sources de données des dépositaires principaux, vous pouvez ajouter des sources de données Office 365 supplémentaires à un dépositaire ou utiliser Office 365 pour vous aider à identifier également les sources de données pertinentes.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

<span data-ttu-id="9ad4e-127">Pour mapper des boîtes aux lettres, des sites ou des équipes à un dépositaire spécifique:</span><span class="sxs-lookup"><span data-stu-id="9ad4e-127">To map mailboxes, sites, or teams to a specific custodian:</span></span>

1. <span data-ttu-id="9ad4e-128">Sélectionnez **mettre à jour** pour affecter des emplacements de contenu, comme des boîtes aux lettres, des sites et des équipes à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-128">Select **Update** to assign content locations, like mailboxes, sites, and Teams to a specific custodian.</span></span> 

2. <span data-ttu-id="9ad4e-129">Dans le menu volant, spécifiez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9ad4e-129">In the flyout, specify the following:</span></span>
   
  -  <span data-ttu-id="9ad4e-p106">**Boîtes aux lettres Exchange** : cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez à nouveau sur **choisir les utilisateurs, les groupes ou les équipes** . Pour spécifier les boîtes aux lettres à affecter au dépositaire sélectionné, utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également affecter la boîte aux lettres associée pour un groupe Office 365 ou une équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="9ad4e-p107">Lorsque vous cliquez sur choisir les utilisateurs, les groupes ou les équipes pour spécifier des boîtes aux lettres, le sélecteur de boîtes aux lettres affiché est vide. Il s'agit d'une conception qui améliore les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
   - <span data-ttu-id="9ad4e-p108">**Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez sur choisir de nouveau les **sites** pour spécifier d'autres sites SharePoint et OneDrive entreprise que vous souhaitez affecter au dépositaire sélectionné. Vous pouvez également ajouter l'URL du site SharePoint pour un groupe Office 365 ou une équipe Microsoft. Tapez l'URL de chaque site que vous souhaitez attribuer. Cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
   - <span data-ttu-id="9ad4e-p109">**Microsoft** teams – cliquez sur **choisir teams** , puis cliquez sur **choisir les équipes** pour afficher la liste des groupes d'équipes Microsoft dont le dépositaire est membre. Sélectionnez les équipes que vous souhaitez ajouter à votre dépositaire. Une fois sélectionné, le système identifie automatiquement & sélectionnez le site SharePoint et la boîte aux lettres de groupe associés associés à cette équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="9ad4e-145">Pour ajouter des Microsoft teams supplémentaires, vous devez ajouter séparément la boîte aux lettres et le site SharePoint, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-145">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="9ad4e-p110">Une fois que vous avez terminé le mappage de vos sources, vous pouvez afficher le nombre total de boîtes aux lettres, de sites et d'équipes pour les dépositaires que vous venez d'ajouter. Une fois que vous avez finalisé les sources de données pertinentes pour un dépositaire spécifique, ce mappage est maintenu et étendu aux flux de travail de collecte, de traitement et de révision de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="9ad4e-148">Module Étape 4: placer des dépositaires en conservation</span><span class="sxs-lookup"><span data-stu-id="9ad4e-148">(Optional) Step 4: Place custodians on hold</span></span>

 <span data-ttu-id="9ad4e-p111">Une fois que vous avez finalisé les dépositaires et les sources de données que vous souhaitez ajouter à votre cas, vous pouvez éventuellement placer une partie ou la totalité de vos dépositaires en conservation. Lorsque vous mettez un dépositaire en conservation, le contenu mappé sur cet utilisateur est conservé jusqu'à ce que vous relâchiez le déblocage du dépositaire ou jusqu'à ce que vous supprimiez le blocage. Dans certains cas, vous souhaiterez peut-être ajouter des dépositaires à un cas sans les mettre en attente.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="9ad4e-152">Pour placer les dépositaires et les sources de données sélectionnés en conservation:</span><span class="sxs-lookup"><span data-stu-id="9ad4e-152">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="9ad4e-p112">Vérifiez vos sélections de dépositaire et activez la case à cocher pour placer chaque dépositaire en conservation. Une fois qu'un dépositaire est mis en attente, une stratégie de blocage des dépositaires contenant toutes les sources privatives de temps est automatiquement créée. Si cette option n'est pas cochée, le dépositaire & les sources de données sélectionnées seront ajoutées à la casse, mais le contenu ne sera pas préservé.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-p112">Verify your custodian selections and select the checkbox to place each custodian on hold.Once a custodian is placed on hold, a custodian hold policy containing all custodial sources will automatically be created. If the option is not checked, the custodian & selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="9ad4e-155">Accédez à l' \*\*\*\* onglet suspensions et sélectionnez la **stratégie de blocage**des dépositaires.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-155">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="9ad4e-156">Cliquez sur **modifier** pour afficher toutes les sources de données de dépositaire sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="9ad4e-156">Click **Edit** to view all the selected custodian data sources.</span></span>
