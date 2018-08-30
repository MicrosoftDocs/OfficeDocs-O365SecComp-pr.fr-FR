---
title: Utiliser le partage de l’audit dans le journal d’audit de Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Le partage est une activité dans SharePoint Online et OneDrive for Business. Les administrateurs peuvent maintenant utiliser le partage d’audit dans le journal d’audit d’Office 365 pour déterminer comment le partage est utilisé dans leur organisation. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528212"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="dbfd0-104">Utiliser le partage de l’audit dans le journal d’audit de Office 365</span><span class="sxs-lookup"><span data-stu-id="dbfd0-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="dbfd0-p102">Le partage est une activité dans SharePoint Online et OneDrive entreprise et largement utilisé dans les organisations Office 365. Les administrateurs peuvent maintenant utiliser le partage d’audit dans le journal d’audit d’Office 365 pour déterminer comment le partage est utilisé dans leur organisation.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="dbfd0-107">Le schéma de partage SharePoint</span><span class="sxs-lookup"><span data-stu-id="dbfd0-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="dbfd0-p103">Partage des événements (à l’exclusion des stratégie de partage et lier les événements) sont différentes des événements liées aux fichiers et un dossier d’une manière principale : un utilisateur effectue une action qui a des répercussions sur un autre utilisateur. Par exemple, l’utilisateur A donne accès utilisateur B vers un fichier. Dans cet exemple, l’utilisateur A est le *rôle d’utilisateur* et utilisateur B est l' *utilisateur cible*. Dans le schéma de fichier de SharePoint, action de l’utilisateur agissant n’affecte que le fichier proprement dit. Lorsque l’utilisateur A ouvre un fichier, les seules informations nécessaires dans l’événement **FileAccessed** est l’utilisateur agissant. Pour résoudre cette différence, il existe un schéma distinct, appelé le *schéma de partage SharePoint*, qui capture des informations supplémentaires sur le partage des événements. Cela garantit que les administrateurs ont plus de détails sur ayant une ressource partagée et l’utilisateur de la ressource a été partagé avec.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="dbfd0-115">Le schéma de partage fournit deux champs supplémentaires dans le journal d’audit liés au partage des événements :</span><span class="sxs-lookup"><span data-stu-id="dbfd0-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="dbfd0-116">**TargetUserOrGroupName** - stocke l’UPN ou le nom de l’utilisateur ou groupe cible qu’une ressource a été partagée avec (utilisateur B dans l’exemple précédent).</span><span class="sxs-lookup"><span data-stu-id="dbfd0-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="dbfd0-117">**TargetUserOrGroupType** - indique si l’utilisateur ou groupe cible est un membre, invité, groupe ou partenaire.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="dbfd0-118">Ces deux champs, en plus d’autres propriétés à partir d’Office 365 d’audit schéma du journal telle que l’utilisateur, opération et la Date peuvent l’histoire complète sur *la* ressource utilisateur partagé *quel* avec *lesquels* et *quand*.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="dbfd0-p104">Il existe une autre propriété de schéma est importante de l’histoire de partage. La propriété **EventData** stocke des informations supplémentaires sur le partage des événements. Par exemple, lorsqu’un utilisateur partage un site avec un autre utilisateur, cette opération s’effectue en ajoutant l’utilisateur cible à un groupe SharePoint. La propriété **EventData** capture ces informations supplémentaires pour fournir un contexte pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="dbfd0-123">Modèle de partage et événements SharePoint</span><span class="sxs-lookup"><span data-stu-id="dbfd0-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="dbfd0-p105">Partage réellement défini par trois événements distincts : **SharingSet**, **SharingInvitationCreated**et **SharingInvitaitonAccepted**. Voici le flux de travail pour le partage des événements sont consignés dans le journal d’audit de Office 365.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Organigramme du fonctionne de l’audit de partage](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="dbfd0-p106">Lorsqu’un utilisateur (agissant) souhaite partager une ressource avec un autre utilisateur (la cible), SharePoint (ou OneDrive entreprise) commence par vérifier si l’adresse de messagerie de l’utilisateur cible est déjà associé à un compte d’utilisateur dans l’annuaire de l’organisation. Si l’utilisateur cible se trouve dans le répertoire de l’organisation, SharePoint effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="dbfd0-129">Immédiatement attribue les autorisations d’utilisateur cible pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="dbfd0-130">Envoie une notification de partage à l’adresse de messagerie de l’utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="dbfd0-131">Enregistre un événement **SharingSet** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="dbfd0-132">Si un compte d’utilisateur pour l’utilisateur cible n’est pas dans l’annuaire de l’organisation, SharePoint effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbfd0-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="dbfd0-133">Crée une invitation de partage et l’envoie à l’adresse de messagerie de l’utilisateur cible.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="dbfd0-134">Enregistre un événement **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="dbfd0-135">L’événement **SharingInvitationCreated** associée presque toujours externe ou invité partage lors de l’utilisateur cible n’a pas accès à la ressource qui a été partagée.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="dbfd0-p107">Lorsque l’utilisateur cible accepte l’invitation de partage qui lui a envoyé (en cliquant sur le lien dans l’invitation), SharePoint consigne un événement **SharingInvitationAccepted** et attribue les autorisations d’utilisateur cible pour accéder à la ressource. Plus d’informations sur l’utilisateur cible sont également connectés, telles que l’identité de l’utilisateur qui a été envoyée l’invitation et l’utilisateur ayant effectivement accepté l’invitation. Dans certains cas, ces utilisateurs (ou les adresses de messagerie) peuvent être différents.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="dbfd0-139">Comment identifier les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="dbfd0-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="dbfd0-p108">Une exigence courante pour les administrateurs consiste à créer une liste de toutes les ressources qui ont été partagés avec les utilisateurs en dehors de l’organisation. En utilisant le partage de l’audit dans Office 365, les administrateurs peuvent désormais générer cette liste. Voici comment.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="dbfd0-143">Étape 1 : Rechercher des événements de partage et exporter les résultats vers un fichier CSV</span><span class="sxs-lookup"><span data-stu-id="dbfd0-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="dbfd0-p109">La première étape consiste à rechercher dans le journal d’audit Office 365 pour le partage d’événements. Pour plus d’informations (y compris les autorisations requises) sur la recherche dans le journal d’audit, consultez la rubrique [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="dbfd0-146">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="dbfd0-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="dbfd0-147">Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="dbfd0-148">Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête**, puis cliquez sur **Rechercher des journaux d’Audit**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="dbfd0-149">La page de **recherche des journaux d’Audit** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="dbfd0-150">Sous **activités**, cliquez sur **activités de partage** pour rechercher uniquement des événements de partage.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Sous activités, sélectionnez les activités de partage](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="dbfd0-152">Sélectionnez une plage de date et heure pour rechercher les événements de partage s’est produite dans ce délai.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="dbfd0-153">Cliquez sur **Rechercher** pour lancer la recherche.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="dbfd0-154">Lors de la recherche est terminée en cours d’exécution et les résultats sont affichés, cliquez sur **Exporter les résultats** \> **Téléchargez tous les résultats**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="dbfd0-155">Une fois que vous sélectionnez l’option d’exportation, un message s’affiche en bas de la fenêtre qui vous invite à ouvrir ou enregistrer le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="dbfd0-156">Cliquez sur **Enregistrer** \> **Enregistrer sous** et enregistrez le fichier CSV dans un dossier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="dbfd0-157">Étape 2 : Filtrer le fichier CSV pour les ressources partagées avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="dbfd0-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="dbfd0-p110">L’étape suivante consiste à filtrer le CSV pour les événements **SharingSet** et **SharingInvitationCreated** et pour afficher les événements dont la propriété **TargetUserOrGroupType** est **invité**. Vous allez utiliser la fonctionnalité de requête d’alimentation dans Excel pour effectuer cette opération. La procédure suivante est effectuée dans Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="dbfd0-161">Dans Excel, 2016, ouvrez un classeur vierge.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="dbfd0-162">Cliquez sur l’onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="dbfd0-163">Cliquez sur **Nouvelle requête** \> **à partir du fichier** \> **De CSV**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Sous l’onglet données, sélectionnez Nouvelle requête, sélectionnez fichier et sélectionnez CSV à partir de](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="dbfd0-165">Ouvrez le fichier CSV que vous avez téléchargé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="dbfd0-p111">Le fichier CSV est ouvert dans l’éditeur de requête. Notez qu’il existe quatre colonnes : **heure**, **utilisateur**, **Action**et **Détail**. La colonne **Détail** est un champ de propriété à plusieurs. L’étape suivante consiste à créer une nouvelle colonne pour chacune des propriétés dans la colonne de **Détail** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="dbfd0-170">Sélectionnez la colonne **Détail** , puis cliquez sur l’onglet **accueil** , **Colonne fractionnée** \> **Par délimiteur**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Sous l’onglet Accueil, cliquez sur la colonne fractionnée, puis cliquez sur par délimiteur](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="dbfd0-172">Dans la fenêtre de la **Colonne fractionnée par délimiteur** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="dbfd0-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="dbfd0-173">Sous, **Sélectionnez ou entrez délimiteur**, sélectionnez **une virgule**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="dbfd0-174">Sous **Fractionné**, sélectionnez **à chaque occurrence du délimiteur**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="dbfd0-175">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-175">Click **OK**.</span></span>
    
    <span data-ttu-id="dbfd0-p112">La colonne **Détail** est divisée en plusieurs colonnes. Chaque nouvelle colonne est nommé **Detail.1**, **Detail.2**, **Detail.3**et ainsi de suite. Vous constaterez que les valeurs de chacune des cellules dans les colonnes **Detail.n** portent le préfixe du nom de la propriété ; par exemple, **Opération : SharingSet**, **Opération : SharingInvitationAccepted**et **Opération : SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![La colonne détail est divisée en plusieurs colonnes, une pour chaque propriété](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="dbfd0-180">Sous l’onglet **fichier** , cliquez sur **Fermer &amp; charge** pour fermer l’éditeur de requête et ouvrez le fichier dans un classeur Excel.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="dbfd0-181">L’étape suivante consiste à filtrer le fichier pour afficher uniquement les événements **SharingSet** et **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="dbfd0-182">Accédez à l’onglet **accueil** , puis sélectionnez la colonne **Action** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="dbfd0-183">Dans la **tri &amp; Filter** liste déroulante, désactivez toutes les sélections, puis sélectionnez **SharingSet** et **SharingInvitationCreated**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="dbfd0-184">Excel affiche les lignes pour les événements **SharingSet** et **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="dbfd0-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="dbfd0-185">Accédez à la colonne nommée **Detail.17** (ou la colonne contient la propriété **TargetUserOrGroupType** ) et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="dbfd0-186">Dans la **tri &amp; Filter** liste déroulante, désactivez toutes les sélections, sélectionnez **TargetUserOrGroupType:Guest**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="dbfd0-187">Excel affiche maintenant les lignes pour les événements **SharingInvitationCreated** et **SharingSet** et où l’utilisateur cible à l’extérieur de votre organisation, car les utilisateurs externes sont identifiés par la valeur **TargetUserOrGroupType:Guest**.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="dbfd0-188">Le tableau suivant indique tous les utilisateurs dans l’organisation et des ressources partagées avec un utilisateur invité au sein d’une plage de dates spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Journal d’audit de partage d’événements dans Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="dbfd0-190">Bien qu’il n’est pas inclus dans le tableau précédent, la colonne **Detail.10** (ou la colonne contient la propriété **ObjectId** ) identifie la ressource qui a été partagée avec l’utilisateur cible ; par exemple `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="dbfd0-191">Si vous souhaitez identifier quand un utilisateur invité a été réellement affecté des autorisations pour accéder à une ressource (au lieu de simplement les ressources dont partagé avec eux), répétez les étapes 10, 11 et 12 et filtrer les **SharingInvitationAccepted** et **SharingSet **événements à l’étape 10.</span><span class="sxs-lookup"><span data-stu-id="dbfd0-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
