---
title: Audit de partage pour trouver les ressources partagées avec des utilisateurs externes
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise. Les administrateurs peuvent désormais utiliser l’audit de partage dans le journal d’audit Office 365 pour déterminer le mode d’utilisation du partage dans leur organisation. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435237"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="35166-104">Audit de partage pour trouver les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="35166-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="35166-105">Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise, et est largement utilisée dans les organisations Office 365.</span><span class="sxs-lookup"><span data-stu-id="35166-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="35166-106">Les administrateurs peuvent désormais utiliser l’audit de partage dans le journal d’audit Office 365 pour déterminer le mode d’utilisation du partage dans leur organisation.</span><span class="sxs-lookup"><span data-stu-id="35166-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="35166-107">Schéma de partage SharePoint</span><span class="sxs-lookup"><span data-stu-id="35166-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="35166-108">Les événements de partage (à l’exception des événements de liens de partage et de stratégie) sont différents des événements liés aux fichiers et aux dossiers d’une manière principale: un utilisateur effectue une action qui a un certain effet sur un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35166-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="35166-109">Par exemple, l’utilisateur A accorde à l’utilisateur B l’accès à un fichier.</span><span class="sxs-lookup"><span data-stu-id="35166-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="35166-110">Dans cet exemple, l’utilisateur A est \*\* l’utilisateur qui agit et l’utilisateur B est l' *utilisateur cible*.</span><span class="sxs-lookup"><span data-stu-id="35166-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="35166-111">Dans le schéma de fichier SharePoint, l’action de l’utilisateur qui agit n’affecte que le fichier lui-même.</span><span class="sxs-lookup"><span data-stu-id="35166-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="35166-112">Lorsque l’utilisateur A ouvre un fichier, la seule information nécessaire dans l’événement **FileAccessed** est l’utilisateur agissant.</span><span class="sxs-lookup"><span data-stu-id="35166-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="35166-113">Pour résoudre cette différence, il existe un schéma distinct, appelé *schéma de partage SharePoint*, qui capture des informations supplémentaires sur les événements de partage.</span><span class="sxs-lookup"><span data-stu-id="35166-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="35166-114">Cela garantit aux administrateurs un aperçu plus détaillé des personnes qui ont partagé une ressource et de l’utilisateur avec lequel elle a été partagée.</span><span class="sxs-lookup"><span data-stu-id="35166-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="35166-115">Le schéma de partage fournit deux champs supplémentaires dans le journal d’audit concernant les événements de partage:</span><span class="sxs-lookup"><span data-stu-id="35166-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="35166-116">**TargetUserOrGroupName** : stocke l’UPN ou le nom de l’utilisateur ou du groupe cible avec lequel une ressource a été partagée (utilisateur B dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="35166-116">**TargetUserOrGroupName** – Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="35166-117">**TargetUserOrGroupType** : indique si l’utilisateur ou le groupe cible est un membre, un invité, un groupe ou un partenaire.</span><span class="sxs-lookup"><span data-stu-id="35166-117">**TargetUserOrGroupType** – Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="35166-118">Ces deux champs, en plus des autres propriétés du schéma de journal d’audit Office 365, telles que User, Operation et date, peuvent indiquer l’histoire \*\* complète de quel utilisateur a partagé *quelle* ressource avec *qui* et *quand*.</span><span class="sxs-lookup"><span data-stu-id="35166-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="35166-119">Il existe une autre propriété de schéma importante pour l’histoire du partage.</span><span class="sxs-lookup"><span data-stu-id="35166-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="35166-120">La propriété **EventData** stocke des informations supplémentaires sur les événements de partage.</span><span class="sxs-lookup"><span data-stu-id="35166-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="35166-121">Par exemple, lorsqu’un utilisateur partage un site avec un autre utilisateur, l’utilisateur cible est ajouté à un groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="35166-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="35166-122">La propriété **EventData** capture ces informations supplémentaires afin de fournir un contexte aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="35166-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="35166-123">Modèle de partage SharePoint et événements de partage</span><span class="sxs-lookup"><span data-stu-id="35166-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="35166-124">Le partage est défini par trois événements distincts: **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**.</span><span class="sxs-lookup"><span data-stu-id="35166-124">Sharing is defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="35166-125">Voici le flux de travail concernant la façon dont les événements de partage sont consignés dans le journal d’audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="35166-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Organigramme illustrant le fonctionnement du partage d’audit](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="35166-127">Lorsqu’un utilisateur (l’utilisateur agissant) souhaite partager une ressource avec un autre utilisateur (l’utilisateur cible), SharePoint (ou OneDrive entreprise) vérifie d’abord si l’adresse de messagerie de l’utilisateur cible est déjà associée à un compte d’utilisateur dans l’annuaire de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="35166-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="35166-128">Si l’utilisateur cible se trouve dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="35166-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="35166-129">Affecte immédiatement les autorisations de l’utilisateur cible pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="35166-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="35166-130">Envoie une notification de partage à l’adresse de messagerie de l’utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="35166-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="35166-131">Enregistre un événement **SharingSet** .</span><span class="sxs-lookup"><span data-stu-id="35166-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="35166-132">Si un compte d’utilisateur pour l’utilisateur cible ne se trouve pas dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="35166-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="35166-133">Crée une invitation de partage et l’envoie à l’adresse de messagerie de l’utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="35166-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="35166-134">Enregistre un événement **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="35166-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="35166-135">L’événement **SharingInvitationCreated** est le plus souvent associé au partage externe ou invité lorsque l’utilisateur cible n’a pas accès à la ressource qui a été partagée.</span><span class="sxs-lookup"><span data-stu-id="35166-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="35166-136">Lorsque l’utilisateur cible accepte l’invitation de partage qui lui est envoyée (en cliquant sur le lien dans l’invitation), SharePoint consigne un événement **SharingInvitationAccepted** et affecte les autorisations de l’utilisateur cible pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="35166-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="35166-137">Des informations supplémentaires sur l’utilisateur cible sont également consignées, telles que l’identité de l’utilisateur auquel l’invitation a été envoyée et l’utilisateur qui a réellement accepté l’invitation.</span><span class="sxs-lookup"><span data-stu-id="35166-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="35166-138">Dans certains cas, ces utilisateurs (ou adresses de messagerie) peuvent être différents.</span><span class="sxs-lookup"><span data-stu-id="35166-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="35166-139">Comment identifier les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="35166-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="35166-140">Une exigence commune pour les administrateurs est la création d’une liste de toutes les ressources qui ont été partagées avec des utilisateurs extérieurs à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="35166-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="35166-141">À l’aide de l’audit de partage dans Office 365, les administrateurs peuvent désormais générer cette liste.</span><span class="sxs-lookup"><span data-stu-id="35166-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="35166-142">Voici comment procéder.</span><span class="sxs-lookup"><span data-stu-id="35166-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="35166-143">Étape 1: Rechercher des événements de partage et exporter les résultats dans un fichier CSV</span><span class="sxs-lookup"><span data-stu-id="35166-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="35166-144">La première étape consiste à rechercher dans le journal d’audit Office 365 des événements de partage.</span><span class="sxs-lookup"><span data-stu-id="35166-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="35166-145">Pour plus d’informations (y compris les autorisations requises) sur la recherche dans le journal d’audit, voir [Search the audit log dans le centre de sécurité & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="35166-145">For more information (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="35166-146">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="35166-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="35166-147">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="35166-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="35166-148">Dans le volet gauche du centre de sécurité & conformité, cliquez \*\*\*\*  > sur Rechercher dans le**Journal d’audit**.</span><span class="sxs-lookup"><span data-stu-id="35166-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="35166-149">La page **recherche du journal d’audit** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="35166-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="35166-150">Sous **activités**, cliquez sur **activités de partage et d’accès aux requêtes** pour rechercher des événements associés au partage.</span><span class="sxs-lookup"><span data-stu-id="35166-150">Under **Activities**, click **Sharing and access request activities** to search for sharing-related events.</span></span> 
    
    ![Sous activités, sélectionnez activités de partage et d’accès aux demandes.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="35166-152">Sélectionnez une date et une plage horaire pour rechercher les événements de partage qui se sont produits au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="35166-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="35166-153">Cliquez sur **Rechercher** pour exécuter la recherche.</span><span class="sxs-lookup"><span data-stu-id="35166-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="35166-154">Lorsque l’exécution de la recherche est terminée et que les résultats sont affichés, cliquez sur **Exporter les résultats** \> pour **Télécharger tous les résultats**.</span><span class="sxs-lookup"><span data-stu-id="35166-154">When the search is finished running and the results are displayed, click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="35166-155">Une fois que vous avez sélectionné l’option Exporter, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir ou à enregistrer le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="35166-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="35166-156">Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="35166-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="35166-157">Étape 2: filtrage du fichier CSV pour les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="35166-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="35166-158">L’étape suivante consiste à filtrer le fichier CSV pour les événements **SharingSet** et **SharingInvitationCreated** , et à afficher les événements pour lesquels la propriété **TargetUserOrGroupType** est **Guest**.</span><span class="sxs-lookup"><span data-stu-id="35166-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="35166-159">Pour ce faire, utilisez l’outil Éditeur de la requête Power dans Excel.</span><span class="sxs-lookup"><span data-stu-id="35166-159">You use the Power Query Editor tool in Excel to do this.</span></span> <span data-ttu-id="35166-160">Pour obtenir des instructions pas à pas, reportez-vous à la rubrique [Exporter, configurer et afficher les enregistrements du journal d’audit](export-view-audit-log-records.md).</span><span class="sxs-lookup"><span data-stu-id="35166-160">For step-by-step instructions, see [Export, configure, and view audit log records](export-view-audit-log-records.md).</span></span> 

<span data-ttu-id="35166-161">Une fois que vous avez suivi les instructions de la rubrique précédente pour préparer le fichier CSV, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="35166-161">After you've followed the instructions in the previous topic to prepare the CSV file, do the following:</span></span>
    
1. <span data-ttu-id="35166-162">Ouvrez le fichier CSV que vous avez préparé avec l’éditeur de Power Query.</span><span class="sxs-lookup"><span data-stu-id="35166-162">Open the CSV file that you prepared with the Power Query Editor.</span></span> 

2. <span data-ttu-id="35166-163">Sous l’onglet **Accueil** , cliquez sur **Trier & filtrer**, puis sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="35166-163">On the **Home** tab, click **Sort & Filter**, and then click **Filter**.</span></span>
    
3. <span data-ttu-id="35166-164">Dans la liste déroulante **trier & filtre** de la colonne **opérations** , effacez toutes les sélections, sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="35166-164">In the **Sort & Filter** dropdown list on the **Operations** column, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="35166-165">Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="35166-165">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
4. <span data-ttu-id="35166-166">Accédez à la colonne nommée **TargetUserOrGroupType** et sélectionnez-la.</span><span class="sxs-lookup"><span data-stu-id="35166-166">Go to the column named **TargetUserOrGroupType** and select it.</span></span> 
    
5. <span data-ttu-id="35166-167">Dans la liste déroulante **trier & filtre** , effacez toutes les sélections, sélectionnez **TargetUserOrGroupType: invité**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="35166-167">In the **Sort & Filter** dropdown list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="35166-168">À présent, Excel affiche les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et l’emplacement de l’utilisateur cible à l’extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType: Guest**.</span><span class="sxs-lookup"><span data-stu-id="35166-168">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="35166-169">Le tableau suivant présente tous les utilisateurs de l’organisation qui ont partagé des ressources avec un utilisateur invité dans une plage de dates spécifiée.</span><span class="sxs-lookup"><span data-stu-id="35166-169">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Partage d’événements dans le journal d’audit Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="35166-171">Bien qu’elle ne soit pas incluse dans le tableau précédent, la propriété **ObjectID** identifie la ressource qui a été partagée avec l’utilisateur cible; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="35166-171">Although it's not included in the previous table, the **ObjectId** property identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="35166-172">Si vous souhaitez identifier à quel moment un utilisateur invité a reçu des autorisations d’accès à une ressource (par opposition aux ressources partagées avec celles-ci), répétez les étapes 2, 3 et 4, et filtrez sur les **SharingInvitationAccepted** et **SharingSet** événements à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="35166-172">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 2, 3, and 4, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 5.</span></span> 
