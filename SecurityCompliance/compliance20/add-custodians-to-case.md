---
title: Ajouter des dépositaires à une affaire eDiscovery avancées (Preview)
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
ms.openlocfilehash: 88d2e64f4e1fb519955d8970b34e9670fb18d3f8
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706105"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="1790a-102">Ajouter des dépositaires à une affaire eDiscovery avancées (Preview)</span><span class="sxs-lookup"><span data-stu-id="1790a-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="1790a-p101">À l’aide de la découverte électronique avancée (Preview), vous pouvez utiliser l’outil de gestion intégrés dépositaire pour coordonner votre flux de travail autour de la gestion des dépositaires et identification des sources de données pertinentes, garde au sein d’un cas. Lorsque vous ajoutez un dépositaire, le système peut automatiquement identifier et archives permanentes dans leur boîte aux lettres Exchange principale et de OneDrive pour le site de l’entreprise. Lorsque vous effectuez votre recherche, vous pouvez également découvrir et mapper les autres boîtes aux lettres ou les sites qu’un dépositaire accessible dans le passé ou des équipes qu’un dépositaire est un membre de la journée.</span><span class="sxs-lookup"><span data-stu-id="1790a-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="1790a-106">Utilisez le flux de travail suivante pour ajouter et gérer des dépositaires dans les cas eDiscovery avancées (Preview) dans le centre de conformité de & sécurité.</span><span class="sxs-lookup"><span data-stu-id="1790a-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="1790a-107">Étape 1 : Identifier les éventuels dépositaires</span><span class="sxs-lookup"><span data-stu-id="1790a-107">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="1790a-p102">La première étape consiste à identifier les dépositaires appropriés pour votre question. Pour ajouter des dépositaires à un cas, vous devez être un membre de la découverte électronique responsables ou un groupe de rôles Administrateurs eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="1790a-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

<span data-ttu-id="1790a-110">Pour ajouter des dépositaires à une affaire eDiscovery avancées (Preview) existant :</span><span class="sxs-lookup"><span data-stu-id="1790a-110">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="1790a-111">À partir de la page **Avancé eDiscovery (Preview)** , accédez à votre cas.</span><span class="sxs-lookup"><span data-stu-id="1790a-111">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="1790a-112">Après avoir sélectionné un incident, accédez à l’onglet **dépositaires** , cliquez sur **+ Ajouter dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="1790a-112">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="1790a-p103">Choisissez les dépositaires que vous souhaitez ajouter à la casse. Vous pouvez démarrer en tapant pour rechercher et sélectionner les utilisateurs dans Azure Active Directory votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1790a-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="1790a-115">Une fois que vous avez finalisé la liste des dépositaires, cliquez sur **suivant** pour commencer à identifier les sources de données potentielles.</span><span class="sxs-lookup"><span data-stu-id="1790a-115">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
   
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="1790a-116">(Facultatif) Étape 2 : Sélectionner les sources de données dépositaire</span><span class="sxs-lookup"><span data-stu-id="1790a-116">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="1790a-p104">Une fois que vous avez ajouté dépositaires à un cas, vous pouvez exploiter Office 365 pour vous aider à identifier et conserver les sources de données principale dépositaire. Ce flux de travail la prochaine étape consiste à sélectionner les sources de données détenus par les dépositaires spécifiés à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="1790a-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

<span data-ttu-id="1790a-119">Pour identifier les sources de données dépositaire :</span><span class="sxs-lookup"><span data-stu-id="1790a-119">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="1790a-120">Pour chaque conservateur, sélectionnez **Exchange** si vous souhaitez que le système à identifier et ajouter des boîtes aux lettres Exchange principale du dépositaire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1790a-120">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="1790a-121">Pour chaque conservateur, sélectionnez **OneDrive** si vous souhaitez que le système à identifier et ajoutez principal OneDrive URL du dépositaire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1790a-121">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="1790a-122">Une fois que vous avez effectué vos sélections, ils système essaiera automatiquement identifier les sources de données et les ajouter à votre cas.</span><span class="sxs-lookup"><span data-stu-id="1790a-122">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="1790a-123">Cliquez sur **suivant** pour commencer le mappage des sources de données supplémentaires à votre dépositaire.</span><span class="sxs-lookup"><span data-stu-id="1790a-123">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="1790a-124">(Facultatif) Étape 3 : Mapper des sources de données supplémentaires</span><span class="sxs-lookup"><span data-stu-id="1790a-124">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="1790a-p105">Selon votre cas, vous pouvez également ajouter des boîtes aux lettres qui ont utilisés par le passé, un dépositaire donné groupes où un dépositaire est actuellement un membre, ou des sites qu’un dépositaire avait accès dans le passé. En plus des sources de données principale dépositaire, vous pouvez ajouter des sources de données Office 365 supplémentaires à un dépositaire ou tirer parti d’Office 365 pour vous aider à identifier les sources de données potentiellement pertinentes ainsi.</span><span class="sxs-lookup"><span data-stu-id="1790a-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

<span data-ttu-id="1790a-127">Pour mapper des boîtes aux lettres, des sites ou des équipes à un dépositaire spécifique :</span><span class="sxs-lookup"><span data-stu-id="1790a-127">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="1790a-128">Sélectionnez **mise à jour** pour affecter des emplacements de contenu, tels que les boîtes aux lettres, les sites et les équipes, à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="1790a-128">Select **Update** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="1790a-129">Dans la fenêtre mobile, spécifiez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1790a-129">In the flyout, specify the following:</span></span>
   
  -  <span data-ttu-id="1790a-p106">**Boîtes aux lettres Exchange** - cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** , puis sur **Choisir des utilisateurs, des équipes ou des groupes** . Pour spécifier les boîtes aux lettres à affecter à la dépositaire sélectionné, utilisez la zone Rechercher pour rechercher les boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également assigner la boîte aux lettres associée pour un groupe d’Office 365 ou un Team Microsoft. Sélectionnez l’utilisateur, le groupe, la case à cocher de l’équipe, cliquez sur **Choisir**, puis cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="1790a-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="1790a-p107">Lorsque vous cliquez sur Choisir des utilisateurs, des groupes ou équipes pour spécifier les boîtes aux lettres, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.</span><span class="sxs-lookup"><span data-stu-id="1790a-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
   - <span data-ttu-id="1790a-p108">**Sites SharePoint** : cliquez sur **Choisir les sites** , puis sur **Choisir les sites** pour spécifier supplémentaires SharePoint et OneDrive pour les sites entreprise que vous souhaitez attribuer à la dépositaire sélectionné. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe d’Office 365 ou un Team Microsoft. Tapez l’URL pour chaque site que vous voulez affecter. Cliquez sur **Choisir**, puis cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="1790a-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
   - <span data-ttu-id="1790a-p109">**Les équipes Microsoft** – **Choisissez les équipes** et cliquez sur **Choisir des équipes** pour afficher une liste de groupes Microsoft Team que le dépositaire est un membre de la journée. Sélectionnez les équipes que vous souhaitez ajouter à votre dépositaire. Une fois sélectionné, le système identifie automatiquement & sélectionner que le site SharePoint et les boîtes aux lettres de groupe associé associé à ce Microsoft Team. Cliquez sur **Choisir**, puis cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="1790a-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="1790a-145">Pour ajouter d’autres Teams Microsoft, vous devrez ajouter séparément les boîtes aux lettres et un site SharePoint comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1790a-145">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="1790a-p110">Une fois que vous avez terminé le mappage des sources de votre, vous pouvez afficher le total boîtes aux lettres, les sites et les équipes pour les dépositaires que vous venez d’ajouter. Lorsque vous avez finalisé les sources de données pertinentes pour un dépositaire spécifique, ce mappage sera être conservé et étendu pour la collection de découverte électronique, le traitement et passer en revue les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="1790a-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="1790a-148">(Facultatif) Étape 4 : Suspendre dépositaires sur</span><span class="sxs-lookup"><span data-stu-id="1790a-148">(Optional) Step 4: Place custodians on hold</span></span>

 <span data-ttu-id="1790a-p111">Une fois que vous avez finalisé la dépositaires et sources de données que vous souhaitez ajouter à votre cas, vous pouvez éventuellement placer certains ou tous vos dépositaires sur mise en suspens. Lorsque vous bloquez un dépositaire, le contenu mappé à cet utilisateur est conservé jusqu'à ce que vous relâchiez la dépositaire à partir de la casse ou jusqu'à ce que vous supprimez la suspension. Dans certains cas, vous souhaiterez peut-être ajouter dépositaires à un cas sans les placer en attente.</span><span class="sxs-lookup"><span data-stu-id="1790a-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="1790a-152">Pour placer les sélectionné dépositaires et sources de données sur contiennent :</span><span class="sxs-lookup"><span data-stu-id="1790a-152">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="1790a-p112">Vérifiez vos sélections dépositaire et sélectionnez le checkox placer chaque dépositaire en attente. Une fois qu’un dépositaire est mis en attente, une stratégie de blocage dépositaire contenant les sources de toutes les garde sera créée automatiquement. Si l’option n’est pas activée, les sources de données dépositaire & sélectionné seront ajoutés à la casse, mais le contenu n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="1790a-p112">Verify your custodian selections and select the checkox to place each custodian on hold.Once a custodian is placed on hold, a custodian hold policy containing all custodial sources will automatically be created. If the option is not checked, the custodian & selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="1790a-155">Accédez à l’onglet **contient** et sélectionnez la **Stratégie de blocage de dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="1790a-155">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="1790a-156">Cliquez sur **Modifier** pour afficher toutes les sources de données dépositaire sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1790a-156">Click **Edit** to view all the selected custodian data sources.</span></span>
