---
title: Audit de partage pour trouver les ressources partagées avec des utilisateurs externes
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: "Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise. Les administrateurs peuvent désormais utiliser l'audit de partage dans le journal d'audit Office 365 pour déterminer le mode d'utilisation du partage dans leur organisation. "
ms.openlocfilehash: 919592bff43379b552b83258c7b22b7eddb14e7a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219884"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="ecbf3-104">Audit de partage pour trouver les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="ecbf3-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="ecbf3-p102">Le partage est une activité essentielle dans SharePoint Online et OneDrive entreprise, et est largement utilisée dans les organisations Office 365. Les administrateurs peuvent désormais utiliser l'audit de partage dans le journal d'audit Office 365 pour déterminer le mode d'utilisation du partage dans leur organisation.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="ecbf3-107">Schéma de partage SharePoint</span><span class="sxs-lookup"><span data-stu-id="ecbf3-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="ecbf3-p103">Les événements de partage (à l'exception des événements de liens de partage et de stratégie) sont différents des événements liés aux fichiers et aux dossiers d'une manière principale: un utilisateur effectue une action qui a un certain effet sur un autre utilisateur. Par exemple, l'utilisateur A accorde à l'utilisateur B l'accès à un fichier. Dans cet exemple, l'utilisateur A est \*\* l'utilisateur qui agit et l'utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier SharePoint, l'action de l'utilisateur qui agit n'affecte que le fichier lui-même. Lorsque l'utilisateur A ouvre un fichier, la seule information nécessaire dans l'événement **FileAccessed** est l'utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé *schéma de partage SharePoint*, qui capture des informations supplémentaires sur les événements de partage. Cela garantit aux administrateurs un aperçu plus détaillé des personnes qui ont partagé une ressource et de l'utilisateur avec lequel elle a été partagée.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="ecbf3-115">Le schéma de partage fournit deux champs supplémentaires dans le journal d'audit concernant les événements de partage:</span><span class="sxs-lookup"><span data-stu-id="ecbf3-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="ecbf3-116">**TargetUserOrGroupName** : stocke l'UPN ou le nom de l'utilisateur ou du groupe cible avec lequel une ressource a été partagée (utilisateur B dans l'exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="ecbf3-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="ecbf3-117">**TargetUserOrGroupType** : indique si l'utilisateur ou le groupe cible est un membre, un invité, un groupe ou un partenaire.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="ecbf3-118">Ces deux champs, en plus des autres propriétés du schéma de journal d'audit Office 365, telles que User, Operation et date, peuvent indiquer l'histoire \*\* complète de quel utilisateur a partagé *quelle* ressource avec *qui* et *quand*.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="ecbf3-p104">Il existe une autre propriété de schéma importante pour l'histoire du partage. La propriété **EventData** stocke des informations supplémentaires sur les événements de partage. Par exemple, lorsqu'un utilisateur partage un site avec un autre utilisateur, l'utilisateur cible est ajouté à un groupe SharePoint. La propriété **EventData** capture ces informations supplémentaires afin de fournir un contexte aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="ecbf3-123">Modèle de partage SharePoint et événements de partage</span><span class="sxs-lookup"><span data-stu-id="ecbf3-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="ecbf3-p105">Le partage est en fait défini par trois événements distincts: **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**. Voici le flux de travail concernant la façon dont les événements de partage sont consignés dans le journal d'audit Office 365.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Organigramme illustrant le fonctionnement du partage d'audit](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="ecbf3-p106">Lorsqu'un utilisateur (l'utilisateur agissant) souhaite partager une ressource avec un autre utilisateur (l'utilisateur cible), SharePoint (ou OneDrive entreprise) vérifie d'abord si l'adresse de messagerie de l'utilisateur cible est déjà associée à un compte d'utilisateur dans l'annuaire de l'organisation. Si l'utilisateur cible se trouve dans l'annuaire de l'organisation, SharePoint effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="ecbf3-129">Affecte immédiatement les autorisations de l'utilisateur cible pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="ecbf3-130">Envoie une notification de partage à l'adresse de messagerie de l'utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="ecbf3-131">Enregistre un événement **SharingSet** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="ecbf3-132">Si un compte d'utilisateur pour l'utilisateur cible ne se trouve pas dans l'annuaire de l'organisation, SharePoint effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ecbf3-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="ecbf3-133">Crée une invitation de partage et l'envoie à l'adresse de messagerie de l'utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="ecbf3-134">Enregistre un événement **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ecbf3-135">L'événement **SharingInvitationCreated** est le plus souvent associé au partage externe ou invité lorsque l'utilisateur cible n'a pas accès à la ressource qui a été partagée.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="ecbf3-p107">Lorsque l'utilisateur cible accepte l'invitation de partage qui lui est envoyée (en cliquant sur le lien dans l'invitation), SharePoint consigne un événement **SharingInvitationAccepted** et affecte les autorisations de l'utilisateur cible pour accéder à la ressource. Des informations supplémentaires sur l'utilisateur cible sont également consignées, telles que l'identité de l'utilisateur auquel l'invitation a été envoyée et l'utilisateur qui a réellement accepté l'invitation. Dans certains cas, ces utilisateurs (ou adresses de messagerie) peuvent être différents.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="ecbf3-139">Comment identifier les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="ecbf3-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="ecbf3-p108">Une exigence commune pour les administrateurs est la création d'une liste de toutes les ressources qui ont été partagées avec des utilisateurs extérieurs à l'organisation. À l'aide de l'audit de partage dans Office 365, les administrateurs peuvent désormais générer cette liste. Voici comment procéder.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="ecbf3-143">Étape 1: Rechercher des événements de partage et exporter les résultats dans un fichier CSV</span><span class="sxs-lookup"><span data-stu-id="ecbf3-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="ecbf3-p109">La première étape consiste à rechercher dans le journal d'audit Office 365 des événements de partage. Pour plus d'informations (y compris les autorisations requises) sur la recherche dans le journal d'audit, voir [Search the audit log &amp; dans le centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="ecbf3-146">Accédez à la page [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="ecbf3-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ecbf3-147">Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ecbf3-148">Dans le volet gauche du centre de &amp; sécurité conformité, cliquez sur recherches de \*\*recherche &amp; \*\*, puis sur **recherche de journal d'audit**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="ecbf3-149">La page **recherche du journal d'audit** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="ecbf3-150">Sous **activités**, cliquez sur **activités de partage** pour rechercher uniquement les événements de partage.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Sous activités, sélectionnez activités de partage](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="ecbf3-152">Sélectionnez une date et une plage horaire pour rechercher les événements de partage qui se sont produits au cours de cette période.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="ecbf3-153">Cliquez sur **Rechercher** pour exécuter la recherche.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="ecbf3-154">Lorsque l'exécution de la recherche est terminée et que les résultats sont affichés, cliquez sur **Exporter les résultats** \> pour **Télécharger tous les résultats**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="ecbf3-155">Une fois que vous avez sélectionné l'option Exporter, un message s'affiche en bas de la fenêtre qui vous invite à ouvrir ou à enregistrer le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="ecbf3-156">Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="ecbf3-157">Étape 2: filtrage du fichier CSV pour les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="ecbf3-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="ecbf3-p110">L'étape suivante consiste à filtrer le fichier CSV pour les événements **SharingSet** et **SharingInvitationCreated** , et à afficher les événements pour lesquels la propriété **TargetUserOrGroupType** est **Guest**. Pour ce faire, utilisez la fonctionnalité Power Query dans Excel. La procédure suivante est effectuée dans Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="ecbf3-161">Dans Excel 2016, ouvrez un classeur vide.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="ecbf3-162">Cliquez sur l’onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="ecbf3-163">Cliquez sur **nouvelle requête** \> **à partir d'un fichier** \> **CSV**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Sous l'onglet données, sélectionnez nouvelle requête, sélectionnez à partir du fichier, puis à partir de CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="ecbf3-165">Ouvrez le fichier CSV que vous avez téléchargé à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="ecbf3-p111">Le fichier CSV s'ouvre dans l'éditeur de requête. Notez qu'il y a quatre colonnes: **heure**, **utilisateur**, **action**et **détail**. La colonne de **détail** est un champ à plusieurs propriétés. L'étape suivante consiste à créer une nouvelle colonne pour chacune des propriétés dans la colonne de **détail** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="ecbf3-170">Sélectionnez la **colonne détail** , puis, sous l'onglet **Accueil** , cliquez sur Fractionner les **colonnes** \> **par**délimiteur.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Sous l'onglet Accueil, cliquez sur Fractionner la colonne, puis sur par déLimiteur.](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="ecbf3-172">Dans la fenêtre fractionner les **colonnes par** délimiteur, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ecbf3-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="ecbf3-173">Sous **Sélectionner ou entrer le séparateur**, sélectionnez **virgule**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="ecbf3-174">Sous **fractionnement**, sélectionnez **à chaque occurrence du**délimiteur.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="ecbf3-175">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-175">Click **OK**.</span></span>
    
    <span data-ttu-id="ecbf3-p112">La colonne de **détail** est divisée en plusieurs colonnes. Chaque nouvelle colonne est nommée **Detail. 1**, **Detail. 2**, **Detail. 3**, etc. Vous remarquerez les valeurs de chaque cellule dans le **détail. n** les colonnes sont précédées du nom de la propriété; par exemple, **operation: SharingSet**, **operation: SharingInvitationAccepted**et **operation: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![La colonne de détail est divisée en plusieurs colonnes, une pour chaque propriété](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="ecbf3-180">Sous l'onglet **fichier** , cliquez sur **fermer &amp; la charge** pour fermer l'éditeur de requête et ouvrez le fichier dans un classeur Excel.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="ecbf3-181">L'étape suivante consiste à filtrer le fichier pour n'afficher que les événements **SharingSet** et **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="ecbf3-182">Accédez à l'onglet **Accueil** , puis sélectionnez la colonne **action** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="ecbf3-183">Dans la liste déroulante \*\* &amp; filtre de tri\*\* , effacez toutes les sélections, sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="ecbf3-184">Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ecbf3-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="ecbf3-185">Accédez à la colonne nommée **Detail. 17** (ou quelle que soit la colonne qui contient la propriété **TargetUserOrGroupType** ) et sélectionnez-la.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="ecbf3-186">Dans la liste déroulante \*\*filtre de tri &amp; \*\* , effacez toutes les sélections, sélectionnez **TargetUserOrGroupType: invité**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="ecbf3-187">À présent, Excel affiche les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et l'emplacement de l'utilisateur cible à l'extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType: Guest**.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="ecbf3-188">Le tableau suivant présente tous les utilisateurs de l'organisation qui ont partagé des ressources avec un utilisateur invité dans une plage de dates spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Partage d'événements dans le journal d'audit Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="ecbf3-190">Bien qu'elle ne soit pas incluse dans le tableau précédent, la colonne **Detail. 10** (ou la colonne contenant la propriété **ObjectID** ) identifie la ressource qui a été partagée avec l'utilisateur cible; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="ecbf3-191">Si vous souhaitez identifier à quel moment un utilisateur invité a reçu des autorisations d'accès à une ressource (par opposition aux ressources partagées avec celles-ci), répétez les étapes 10, 11 et 12 et filtrez sur le **SharingInvitationAccepted** et \*\*SharingSet \*\*événements à l'étape 10.</span><span class="sxs-lookup"><span data-stu-id="ecbf3-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
