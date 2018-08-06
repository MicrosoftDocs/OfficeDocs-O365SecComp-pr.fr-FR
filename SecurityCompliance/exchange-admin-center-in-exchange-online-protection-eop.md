---
title: 'Centre d’administration Exchange dans Exchange Online Protection '
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
description: Le Centre d'administration Exchange (CAE) est la console de gestion basée sur le web pour Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 99640e561b41e47a74e7c22f0bbdcacd0dd80bd7
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026311"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="e3c1f-103">Centre d’administration Exchange dans Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="e3c1f-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="e3c1f-104">Le Centre d'administration Exchange (CAE) est la console de gestion basée sur le web pour Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="e3c1f-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="e3c1f-p101">Vous recherchez la version Exchange 2013 de cette rubrique ? Consultez la rubrique [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="e3c1f-p102">Vous recherchez la version Exchange Online de cette rubrique ? Consultez la rubrique [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="e3c1f-109">Accès au CAE</span><span class="sxs-lookup"><span data-stu-id="e3c1f-109">Accessing the EAC</span></span>

<span data-ttu-id="e3c1f-p103">Dans la plupart des cas, les clients EOP accèdent au CAE via le Centre d'administration Office 365. Un lien vers EOP est disponible dans le menu déroulant de la vignette **Administrateur**, située près de la vignette **Moi**. Cliquez sur la vignette **Administrateur** et sélectionnez **Exchange Online Protection** dans le menu déroulant pour accéder au CAE.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="e3c1f-p104">Vous pouvez également accéder à la page de connexion du CAE directement via l'URL suivante : https://admin.protection.outlook.com/ecp/\<companydomain\>. Par exemple, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. Après avoir indiqué vos informations de connexion d'utilisateur, vous être envoyé directement dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="e3c1f-116">Éléments d'interface utilisateur communs dans le CAE</span><span class="sxs-lookup"><span data-stu-id="e3c1f-116">Common user interface elements in the EAC</span></span>
<span data-ttu-id="e3c1f-117"><a name="BKMK_CommonUserInterfaceElements"> </a></span><span class="sxs-lookup"><span data-stu-id="e3c1f-117"></span></span>

<span data-ttu-id="e3c1f-118">Cette section décrit les éléments d'interface utilisateur disponibles dans le CAE.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-118">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="e3c1f-120">Volet des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e3c1f-120">Feature Pane</span></span>

<span data-ttu-id="e3c1f-p105">Il s'agit du premier niveau de navigation pour la plupart des tâches que vous effectuez au sein du CAE. Le volet des fonctionnalités est organisé par domaines de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="e3c1f-123">**Destinataires** C'est ici que les utilisateurs internes et les contacts externes s'affichent.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-123">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="e3c1f-124">**Autorisations** C'est ici que vous gérez les rôles d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-124">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="e3c1f-125">**Gestion de la conformité** C'est ici que se trouvent les journaux et les rapports d'audit, tels que le rapport de groupe de rôles d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-125">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="e3c1f-126">**Protection** C'est ici que vous gérez la protection anti-courrier indésirable et anti-programme malveillant pour votre organisation, ainsi que les messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-126">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="e3c1f-127">**Flux de messagerie** C'est ici que vous gérez les règles, les domaines acceptés et les connecteurs, et que vous pouvez effectuer un suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-127">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="e3c1f-128">Onglets</span><span class="sxs-lookup"><span data-stu-id="e3c1f-128">Tabs</span></span>

<span data-ttu-id="e3c1f-p106">Les onglets constituent votre deuxième niveau de navigation. Chaque domaine de fonctionnalités contient différents onglets, chacun représentant une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="e3c1f-131">Barre d'outils</span><span class="sxs-lookup"><span data-stu-id="e3c1f-131">Toolbar</span></span>

<span data-ttu-id="e3c1f-p107">Lorsque vous cliquez sur la plupart des onglets, vous devez voir une barre d'outils. La barre d'outils contient des icônes qui correspondent à une action spécifique. Le tableau suivant décrit les icônes et leurs actions.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="e3c1f-135">**Icône**</span><span class="sxs-lookup"><span data-stu-id="e3c1f-135">**Icon**</span></span>|<span data-ttu-id="e3c1f-136">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e3c1f-136">**Name**</span></span>|<span data-ttu-id="e3c1f-137">**Action**</span><span class="sxs-lookup"><span data-stu-id="e3c1f-137">**Action**</span></span>|
|:-----|:-----|:-----|
|![Icône Ajouter](media/ITPro-EAC-AddIcon.png)           <br/> |<span data-ttu-id="e3c1f-139">Ajouter, Nouveau</span><span class="sxs-lookup"><span data-stu-id="e3c1f-139">Add, New</span></span>  <br/> |<span data-ttu-id="e3c1f-p108">Permet de créer un objet. Certaines de ces icônes comportent une flèche vers le bas associée, sur laquelle vous pouvez cliquer pour afficher des objets supplémentaires que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Icône Modifier](media/ITPro-EAC-EditIcon.png)           <br/> |<span data-ttu-id="e3c1f-143">Modifier</span><span class="sxs-lookup"><span data-stu-id="e3c1f-143">Edit</span></span>  <br/> |<span data-ttu-id="e3c1f-144">Permet de modifier un objet.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-144">Use this icon to edit an object.</span></span>  <br/> |
|![Icône Supprimer](media/ITPro-EAC-DeleteIcon.png)           <br/> |<span data-ttu-id="e3c1f-146">Supprimer</span><span class="sxs-lookup"><span data-stu-id="e3c1f-146">Delete</span></span>  <br/> |<span data-ttu-id="e3c1f-p109">Permet de supprimer un objet. Certaines des icônes de suppression comportent une flèche vers le bas, sur laquelle vous pouvez cliquer pour afficher des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![Icône Recherche](media/ITPro-EAC-.png)           <br/> |<span data-ttu-id="e3c1f-150">Rechercher</span><span class="sxs-lookup"><span data-stu-id="e3c1f-150">Search</span></span>  <br/> |<span data-ttu-id="e3c1f-151">Permet d'ouvrir une zone de recherche dans laquelle vous pouvez entrer une expression pour rechercher un objet.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-151">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Icône Actualiser](media/ITPro-EAC-RefreshIcon.png)           <br/> |<span data-ttu-id="e3c1f-153">Actualiser</span><span class="sxs-lookup"><span data-stu-id="e3c1f-153">Refresh</span></span>  <br/> |<span data-ttu-id="e3c1f-154">Permet d'actualiser l'affichage Liste.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-154">Use this icon to refresh the list view.</span></span>  <br/> |
|![Icône Options supplémentaires](media/ITPro-EAC-MoreOptionsIcon.png)           <br/> |<span data-ttu-id="e3c1f-156">Plus d'options</span><span class="sxs-lookup"><span data-stu-id="e3c1f-156">More options</span></span>  <br/> |<span data-ttu-id="e3c1f-p110">Utilisez cette icône pour afficher d'autres actions que vous pouvez effectuer pour les objets figurant sous cet onglet. Par exemple, dans **Destinataires \> Utilisateurs**, le fait de cliquer sur cette icône affiche l'option de **Recherche avancée**.  </span><span class="sxs-lookup"><span data-stu-id="e3c1f-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![Icône flèche vers le haut](media/ITPro-EAC-UpArrowIcon.png)![Icône de flèche vers le bas](media/ITPro-EAC-DownArrowIcon.png)           <br/> |<span data-ttu-id="e3c1f-161">Flèche Haut et flèche Bas</span><span class="sxs-lookup"><span data-stu-id="e3c1f-161">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="e3c1f-162">Utilisez ces icônes pour relever ou abaisser la priorité d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-162">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![Icône Suppression](media/ITPro-EAC-RemoveIcon.png)           <br/> |<span data-ttu-id="e3c1f-164">Supprimer</span><span class="sxs-lookup"><span data-stu-id="e3c1f-164">Remove</span></span>  <br/> |<span data-ttu-id="e3c1f-165">Permet de supprimer des objets d'une liste.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-165">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="e3c1f-166">Affichage Liste</span><span class="sxs-lookup"><span data-stu-id="e3c1f-166">List View</span></span>

<span data-ttu-id="e3c1f-p111">Dans la plupart des cas, vous devez voir un affichage Liste lorsque vous sélectionnez un onglet. La limite d'affichage de l'affichage Liste du CAE est d'environ 10 000 objets. En outre, la pagination est incluse pour vous permettre de paginer les résultats.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="e3c1f-170">Volet d'informations</span><span class="sxs-lookup"><span data-stu-id="e3c1f-170">Details Pane</span></span>

<span data-ttu-id="e3c1f-p112">Quand vous sélectionnez un objet de l'affichage Liste, les informations relatives à cet objet apparaissent dans le volet d'informations. Dans certains cas, le volet d'informations inclut les tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="e3c1f-173">Vignette de l'utilisateur en cours et Aide</span><span class="sxs-lookup"><span data-stu-id="e3c1f-173">Me tile and Help</span></span>

<span data-ttu-id="e3c1f-p113">La vignette **Moi** vous permet de fermer votre session du Centre d'administration Exchange (CAE) pour ouvrir ensuite une session en tant qu'utilisateur différent. Dans le menu déroulant **Aide**![Icône d'aide](media/ITPro-EAC-HelpIcon.png), vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.png) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="e3c1f-176">**Aide** Cliquez sur ![Icône d'aide](media/ITPro-EAC-HelpIcon.png) pour afficher le contenu de l'aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-176">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.png) to view the online help content.</span></span> 
    
2. <span data-ttu-id="e3c1f-p114">**Désactiver la bulle d'aide** La bulle d'aide affiche une aide contextuelle pour des champs spécifiques quand vous créez ou modifiez un objet. Vous pouvez activer ou désactiver la bulle d'aide.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="e3c1f-179">**Copyright** Cliquez sur ce lien pour lire le copyright pour Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-179">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="e3c1f-180">**Confidentialité** Cliquez pour lire la politique de confidentialité pour Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-180">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="e3c1f-181">Navigateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3c1f-181">Supported Browsers</span></span>
<span data-ttu-id="e3c1f-182"><a name="BKMK_SupportedBrowsers"> </a></span><span class="sxs-lookup"><span data-stu-id="e3c1f-182"></span></span>

<span data-ttu-id="e3c1f-p115">Pour bénéficier d'une meilleure expérience d'utilisation du CAE, nous vous recommandons de toujours utiliser les navigateurs, clients Office et applications les plus récents. Nous vous recommandons également d'installer les mises à jour logicielles lorsqu'elles sont disponibles. Pour plus d'informations sur les navigateurs pris en charge et la configuration requise pour le service, voir [Configuration requise pour Office 365](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="e3c1f-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="e3c1f-186">Langues prises en charge dans EOP</span><span class="sxs-lookup"><span data-stu-id="e3c1f-186">Supported languages in EOP</span></span>
<span data-ttu-id="e3c1f-187"><a name="BKMK_SupportedLanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="e3c1f-187"></span></span>

<span data-ttu-id="e3c1f-188">Les langues suivantes sont prises en charge et disponibles dans Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-188">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="e3c1f-189">Amharique</span><span class="sxs-lookup"><span data-stu-id="e3c1f-189">Amharic</span></span>
    
- <span data-ttu-id="e3c1f-190">Arabe</span><span class="sxs-lookup"><span data-stu-id="e3c1f-190">Arabic</span></span>
    
- <span data-ttu-id="e3c1f-191">basque (Basque)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-191">Basque (Basque)</span></span>
    
- <span data-ttu-id="e3c1f-192">Bengla (Inde)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-192">Bengali (India)</span></span>
    
- <span data-ttu-id="e3c1f-193">Bulgare</span><span class="sxs-lookup"><span data-stu-id="e3c1f-193">Bulgarian</span></span>
    
- <span data-ttu-id="e3c1f-194">Catalan</span><span class="sxs-lookup"><span data-stu-id="e3c1f-194">Catalan</span></span>
    
- <span data-ttu-id="e3c1f-195">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-195">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="e3c1f-196">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-196">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="e3c1f-197">Croate</span><span class="sxs-lookup"><span data-stu-id="e3c1f-197">Croatian</span></span>
    
- <span data-ttu-id="e3c1f-198">Tchèque</span><span class="sxs-lookup"><span data-stu-id="e3c1f-198">Czech</span></span>
    
- <span data-ttu-id="e3c1f-199">Danois</span><span class="sxs-lookup"><span data-stu-id="e3c1f-199">Danish</span></span>
    
- <span data-ttu-id="e3c1f-200">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-200">Dutch</span></span>
    
- <span data-ttu-id="e3c1f-201">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-201">Dutch</span></span>
    
- <span data-ttu-id="e3c1f-202">Anglais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-202">English</span></span>
    
- <span data-ttu-id="e3c1f-203">Estonien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-203">Estonian</span></span>
    
- <span data-ttu-id="e3c1f-204">Filipino (Philippines)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-204">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="e3c1f-205">Finnois</span><span class="sxs-lookup"><span data-stu-id="e3c1f-205">Finnish</span></span>
    
- <span data-ttu-id="e3c1f-206">Français</span><span class="sxs-lookup"><span data-stu-id="e3c1f-206">French</span></span>
    
- <span data-ttu-id="e3c1f-207">Galicien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-207">Galician</span></span>
    
- <span data-ttu-id="e3c1f-208">Allemand</span><span class="sxs-lookup"><span data-stu-id="e3c1f-208">German</span></span>
    
- <span data-ttu-id="e3c1f-209">Grec</span><span class="sxs-lookup"><span data-stu-id="e3c1f-209">Greek</span></span>
    
- <span data-ttu-id="e3c1f-210">Goudjrati</span><span class="sxs-lookup"><span data-stu-id="e3c1f-210">Gujarati</span></span>
    
- <span data-ttu-id="e3c1f-211">Hébreu</span><span class="sxs-lookup"><span data-stu-id="e3c1f-211">Hebrew</span></span>
    
- <span data-ttu-id="e3c1f-212">Hindi</span><span class="sxs-lookup"><span data-stu-id="e3c1f-212">Hindi</span></span>
    
- <span data-ttu-id="e3c1f-213">Hongrois</span><span class="sxs-lookup"><span data-stu-id="e3c1f-213">Hungarian</span></span>
    
- <span data-ttu-id="e3c1f-214">Islandais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-214">Icelandic</span></span>
    
- <span data-ttu-id="e3c1f-215">Indonésien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-215">Indonesian</span></span>
    
- <span data-ttu-id="e3c1f-216">Italien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-216">Italian</span></span>
    
- <span data-ttu-id="e3c1f-217">Japonais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-217">Japanese</span></span>
    
- <span data-ttu-id="e3c1f-218">Kannada</span><span class="sxs-lookup"><span data-stu-id="e3c1f-218">Kannada</span></span>
    
- <span data-ttu-id="e3c1f-219">Kazakh</span><span class="sxs-lookup"><span data-stu-id="e3c1f-219">Kazakh</span></span>
    
- <span data-ttu-id="e3c1f-220">Kiswahili</span><span class="sxs-lookup"><span data-stu-id="e3c1f-220">Kiswahili</span></span>
    
- <span data-ttu-id="e3c1f-221">Coréen</span><span class="sxs-lookup"><span data-stu-id="e3c1f-221">Korean</span></span>
    
- <span data-ttu-id="e3c1f-222">Letton</span><span class="sxs-lookup"><span data-stu-id="e3c1f-222">Latvian</span></span>
    
- <span data-ttu-id="e3c1f-223">Lituanien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-223">Lithuanian</span></span>
    
- <span data-ttu-id="e3c1f-224">Malais (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-224">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="e3c1f-225">Malais (Malaisie)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-225">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="e3c1f-226">Malayalam</span><span class="sxs-lookup"><span data-stu-id="e3c1f-226">Malayalam</span></span>
    
- <span data-ttu-id="e3c1f-227">Marathe</span><span class="sxs-lookup"><span data-stu-id="e3c1f-227">Marathi</span></span>
    
- <span data-ttu-id="e3c1f-228">Norvégien (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-228">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="e3c1f-229">Norvégien (nynorsk)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-229">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="e3c1f-230">Odia</span><span class="sxs-lookup"><span data-stu-id="e3c1f-230">Oriya</span></span>
    
- <span data-ttu-id="e3c1f-231">Perse</span><span class="sxs-lookup"><span data-stu-id="e3c1f-231">Persian</span></span>
    
- <span data-ttu-id="e3c1f-232">Polonais</span><span class="sxs-lookup"><span data-stu-id="e3c1f-232">Polish</span></span>
    
- <span data-ttu-id="e3c1f-233">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-233">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="e3c1f-234">Portugais (Portugal)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-234">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="e3c1f-235">Roumain</span><span class="sxs-lookup"><span data-stu-id="e3c1f-235">Romanian</span></span>
    
- <span data-ttu-id="e3c1f-236">Russe</span><span class="sxs-lookup"><span data-stu-id="e3c1f-236">Russian</span></span>
    
- <span data-ttu-id="e3c1f-237">Serbe (cyrillique, Serbie)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-237">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="e3c1f-238">Serbe (latin)</span><span class="sxs-lookup"><span data-stu-id="e3c1f-238">Serbian (Latin)</span></span>
    
- <span data-ttu-id="e3c1f-239">Slovaque</span><span class="sxs-lookup"><span data-stu-id="e3c1f-239">Slovak</span></span>
    
- <span data-ttu-id="e3c1f-240">Slovène</span><span class="sxs-lookup"><span data-stu-id="e3c1f-240">Slovenian</span></span>
    
- <span data-ttu-id="e3c1f-241">Espagnol</span><span class="sxs-lookup"><span data-stu-id="e3c1f-241">Spanish</span></span>
    
- <span data-ttu-id="e3c1f-242">Suédois</span><span class="sxs-lookup"><span data-stu-id="e3c1f-242">Swedish</span></span>
    
- <span data-ttu-id="e3c1f-243">Tamoul</span><span class="sxs-lookup"><span data-stu-id="e3c1f-243">Tamil</span></span>
    
- <span data-ttu-id="e3c1f-244">Télougou</span><span class="sxs-lookup"><span data-stu-id="e3c1f-244">Telugu</span></span>
    
- <span data-ttu-id="e3c1f-245">Thaï</span><span class="sxs-lookup"><span data-stu-id="e3c1f-245">Thai</span></span>
    
- <span data-ttu-id="e3c1f-246">Turc</span><span class="sxs-lookup"><span data-stu-id="e3c1f-246">Turkish</span></span>
    
- <span data-ttu-id="e3c1f-247">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-247">Ukrainian</span></span>
    
- <span data-ttu-id="e3c1f-248">Ourdou</span><span class="sxs-lookup"><span data-stu-id="e3c1f-248">Urdu</span></span>
    
- <span data-ttu-id="e3c1f-249">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="e3c1f-249">Vietnamese</span></span>
    
- <span data-ttu-id="e3c1f-250">Gallois</span><span class="sxs-lookup"><span data-stu-id="e3c1f-250">Welsh</span></span>
    

