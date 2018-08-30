---
title: Utiliser la recherche de contenu dans Office 365 pour les collections ciblées
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Utiliser la recherche de contenu de sécurité Office 365 &amp; centre de conformité pour effectuer des collections ciblées. Un regroupement cible signifie que vous êtes convaincu qu’articles réactifs à un cas ou privilégié se trouvent dans un dossier de boîte aux lettres ou un site spécifique. Utilisez le script dans cet article pour obtenir l’ID de dossier ou le chemin d’accès pour les dossiers de boîte aux lettres ou des sites spécifiques que vous souhaitez rechercher.
ms.openlocfilehash: 3ff0ca00915bce53e9e932316c5ab47884f346b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527625"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="86489-105">Utiliser la recherche de contenu dans Office 365 pour les collections ciblées</span><span class="sxs-lookup"><span data-stu-id="86489-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="86489-p102">La fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité ne fournit pas un moyen direct dans l’interface utilisateur de rechercher des dossiers spécifiques dans les boîtes aux lettres Exchange ou SharePoint et OneDrive pour les sites de l’entreprise. Toutefois, il est possible de rechercher des dossiers spécifiques (appelés un regroupement cible) en spécifiant l’ID de dossier ou le chemin d’accès dans la syntaxe de requête de recherche. À l’aide de la recherche de contenu pour effectuer un regroupement cible est utile lorsque vous êtes convaincu qu’articles réactifs à un cas ou privilégié se trouvent dans un dossier de boîte aux lettres ou un site spécifique. Vous pouvez utiliser le script dans cet article pour obtenir l’ID de dossier pour les dossiers de boîte aux lettres ou le chemin d’accès pour les dossiers SharePoint et OneDrive pour le site de l’entreprise. Puis vous pouvez utiliser l’ID de dossier ou le chemin d’accès dans une requête de recherche pour renvoyer des éléments situés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="86489-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it is possible to search specific folders (called a targeted collection) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="86489-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="86489-111">Before you begin</span></span>

- <span data-ttu-id="86489-p103">Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script à l’étape 1. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="86489-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="86489-p104">En outre, vous devez attribuer le rôle destinataires de messagerie dans votre organisation Exchange Online. Cela est nécessaire pour exécuter l’applet de commande **Get-MailboxFolderStatistics** , qui est inclus dans le script à l’étape 1. Par défaut, le rôle destinataires de messagerie est assigné pour les groupes de rôles gestion de l’organisation et la gestion des destinataires dans Exchange Online. Pour plus d’informations sur l’attribution d’autorisations dans Exchange Online, voir [Gérer les membres du groupe de rôles](https://go.microsoft.com/fwlink/p/?linkid=692102). Vous pourriez également créer un groupe de rôles personnalisé, lui affecter le rôle destinataires de messagerie, puis ajoutez les membres qui ont besoin pour exécuter le script à l’étape 1. Pour plus d’informations, voir [Gérer les groupes de rôles](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="86489-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="86489-p105">Chaque fois que vous exécutez le script à l’étape 1, une nouvelle session PowerShell distante est créée. Ainsi, vous pouvez utiliser des toutes les sessions à distance PowerShell disponibles. Pour éviter cette situation, vous pouvez exécuter la commande suivante pour vous déconnecter de vos sessions PowerShell distantes actives.</span><span class="sxs-lookup"><span data-stu-id="86489-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="86489-123">Pour plus d'informations, reportez-vous à [Connexion à Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="86489-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="86489-p106">Le script inclut la gestion des erreurs minimale. Le principal objectif du script doit rapidement afficher la liste des ID de dossier de boîte aux lettres de site ou chemins d’accès qui peuvent être utilisés dans la syntaxe de requête de recherche d’une recherche de contenu pour effectuer un regroupement cible.</span><span class="sxs-lookup"><span data-stu-id="86489-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="86489-p107">L’exemple de script fourni dans cette rubrique n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="86489-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="86489-131">Étape 1 : Exécuter le script pour obtenir une liste de dossiers pour un site ou une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="86489-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="86489-p108">Le script que vous exécutez dans cette première étape renverra une liste de dossiers de boîte aux lettres ou SharePoint ou OneDrive pour les dossiers de l’entreprise et l’ID du dossier correspondant ou chemin d’accès pour chaque dossier. Lorsque vous exécutez ce script, il vous invite à vous pour obtenir les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="86489-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="86489-p109">**URL de site ou adresse de messagerie** Tapez une adresse de messagerie de le dépositaire pour renvoyer une liste de dossiers de boîte aux lettres Exchange et pliez ID. Ou tapez l’URL pour un site SharePoint ou un site de l’entreprise OneDrive pour retourner une liste de chemins d’accès pour le site spécifié. Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="86489-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and fold IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="86489-137">**Exchange** - stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="86489-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="86489-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="86489-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="86489-139">**OneDrive entreprise** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="86489-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="86489-p110">**Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à Exchange Online et de la sécurité &amp; centre de conformité avec PowerShell à distance. Comme expliqué précédemment, vous avez attribué les autorisations appropriées pour exécuter ce script.</span><span class="sxs-lookup"><span data-stu-id="86489-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="86489-142">Pour afficher la liste des dossiers de boîte aux lettres ou les noms de chemin d’accès du site :</span><span class="sxs-lookup"><span data-stu-id="86489-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="86489-143">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="86489-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appeneded to the folder ID or path ID to use in a Content Search.              #
  # Notes:                                              #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the   #
  #      the current folder and all sub-folders are searched.                       #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                               #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.       #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security &amp; Complaince Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security &amp; Complaince Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Complinace Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "path:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. <span data-ttu-id="86489-144">Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="86489-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="86489-145">Exécuter le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="86489-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="86489-146">Entrez les informations qui vous demande le script.</span><span class="sxs-lookup"><span data-stu-id="86489-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="86489-p111">Le script affiche une liste des dossiers de boîte aux lettres ou un dossier de site pour l’utilisateur spécifié. Laissez cette fenêtre Ouvrir afin que vous pouvez copier un nom de dossier ID ou le chemin d’accès et le coller dans une requête de recherche à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="86489-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="86489-p112">Au lieu de l’affichage d’une liste de dossiers dans l’écran d’ordinateur, vous pouvez réorienter la sortie du script dans un fichier texte. Ce fichier sera enregistré dans le dossier où se trouve le script. Par exemple, pour rediriger le script de sortie dans un fichier texte, exécutez la commande suivante à l’étape 3 : `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` puis vous pouvez copier un ID de dossier ou un chemin d’accès du fichier à utiliser dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="86489-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="86489-152">Sortie du script pour les dossiers de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="86489-152">Script output for mailbox folders</span></span>

<span data-ttu-id="86489-p113">Si vous recevez un ID de dossier de boîte aux lettres, le script se connecte à Exchange Online à l’aide de PowerShell à distance, exécute l’applet de commande **Get-MailboxFolderStatisics** , puis affiche la liste des dossiers à partir de la boîte aux lettres spécifiée. Pour chaque dossier dans la boîte aux lettres, le script affiche le nom du dossier dans la colonne **FolderPath** et l’ID du dossier dans la colonne **FolderQuery** . En outre, le script ajoute le préfixe de **folderId** (qui est le nom de la propriété de la boîte aux lettres) à l’ID de dossier. Étant donné que la propriété **folderid** est une propriété disponible pour la recherche, vous allez utiliser `folderid:<folderid>` dans une requête de recherche à l’étape 2 pour rechercher ce dossier.</span><span class="sxs-lookup"><span data-stu-id="86489-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="86489-157">Voici un exemple de sortie renvoyée par le script pour les dossiers de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="86489-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Exemple de la liste des dossiers de boîte aux lettres et identificateurs renvoyés par le script de dossier](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="86489-159">L’exemple à l’étape 2 montre la requête utilisée pour rechercher le sous-dossier vide dans le dossier éléments récupérables de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86489-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="86489-160">Sortie du script pour les dossiers de site</span><span class="sxs-lookup"><span data-stu-id="86489-160">Script output for site folders</span></span>

<span data-ttu-id="86489-p114">Si vous recevez des chemins d’accès à partir de SharePoint ou OneDrive pour les sites de l’entreprise, le script se connecte à la sécurité &amp; centre de conformité à l’aide de PowerShell à distance, crée une recherche de contenu de recherche dans le site pour les dossiers, et puis affiche la liste des dossiers situé dans le site spécifié. Le script affiche le nom de chaque dossier et ajoute le préfixe du **chemin d’accès** (qui est le nom de la propriété site) à l’URL du dossier. Étant donné que la propriété **path** est une propriété disponible pour la recherche, vous allez utiliser `path:<path>` dans une requête de recherche à l’étape 2 pour rechercher ce dossier.</span><span class="sxs-lookup"><span data-stu-id="86489-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="86489-164">Voici un exemple de sortie renvoyée par le script pour les dossiers de site.</span><span class="sxs-lookup"><span data-stu-id="86489-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![Exemple de la liste des chemins d’accès pour les dossiers site renvoyées par le script](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="86489-166">Étape 2 : Utiliser un ID de dossier ou un chemin d’accès pour effectuer un regroupement cible</span><span class="sxs-lookup"><span data-stu-id="86489-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="86489-p115">Après avoir exécuté le script pour collecter une liste d’ID de dossier ou chemins d’accès pour un utilisateur spécifique, la prochaine étape pour accéder à la sécurité &amp; centre de conformité et créer une recherche de contenu pour rechercher un dossier spécifique. Vous allez utiliser le `folderid:<folderid>` ou `path:<path>` propriété dans la requête de recherche que vous configurez dans la zone mots clés de recherche de contenu (ou en tant que la valeur du paramètre *ContentMatchQuery* si vous utilisez l’applet de commande **New-ComplianceSearch** ). Vous pouvez combiner les `folderid` ou `path` propriété avec les autres paramètres de recherche ou de conditions de recherche. Si vous incluez uniquement la `folderid` ou `path` propriété dans la requête, la recherche retourne tous les éléments situés dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="86489-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="86489-171">À l’aide de la `path` propriété pour rechercher les emplacements de OneDrive ne renvoie des fichiers multimédias, tels que les fichiers .wav, .png et .tiff, dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="86489-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="86489-172">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="86489-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="86489-173">Connectez-vous à Office 365 à l’aide du compte et les informations d’identification que vous avez utilisé pour exécuter le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="86489-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="86489-174">Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête** \> **recherche de contenu**, puis cliquez sur **Nouveau** ![icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="86489-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="86489-p116">Sur la page **Nouvelle recherche**, entrez un nom pour la recherche de contenu. Ce nom doit être unique dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="86489-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="86489-177">Sous **où souhaitez-vous rechercher**, effectuez l’une des valeurs suivantes, selon que votre recherche dans un dossier de boîte aux lettres ou un dossier de site :</span><span class="sxs-lookup"><span data-stu-id="86489-177">Under **Where do you want us to look**, do one of the following, based on whether your searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="86489-178">Cliquez sur **Choisir les boîtes aux lettres spécifiques à rechercher** , puis ajoutez la même boîte aux lettres que vous avez spécifié lorsque vous avez exécuté le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="86489-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="86489-179">Ou</span><span class="sxs-lookup"><span data-stu-id="86489-179">Or</span></span>
    
    - <span data-ttu-id="86489-180">Cliquez sur **Choisir des sites spécifiques à rechercher** pour rechercher, puis ajoutez la même URL de site que vous avez spécifié lorsque vous avez exécuté le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="86489-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="86489-181">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="86489-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="86489-182">Dans la zone mots clés dans la page **que voulez-vous rechercher les** , collez la `folderid:<folderid>` ou `path:<path>` valeur qui a été renvoyée par le script à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="86489-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="86489-183">Par exemple, la requête dans la capture d’écran suivante recherche de tout élément dans le sous-dossier vide dans le dossier éléments récupérables de l’utilisateur (la valeur de la `folderid` propriété pour le sous-dossier purge est illustrée dans la capture d’écran à l’étape 1) :</span><span class="sxs-lookup"><span data-stu-id="86489-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Collez le folderid ou le chemin d’accès dans la zone mots clés de la requête de recherche](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="86489-185">Cliquez sur **Rechercher** pour lancer la recherche de regroupement cible.</span><span class="sxs-lookup"><span data-stu-id="86489-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="86489-186">Exemples de requêtes de recherche pour les collections ciblées</span><span class="sxs-lookup"><span data-stu-id="86489-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="86489-p117">Voici quelques exemples d’utilisation de la `folderid` et `path` propriétés dans une requête de recherche pour effectuer un regroupement cible. Notez que les espaces réservés sont utilisés pour `folderid:<folderid>` et `path:<path>` pour économiser de l’espace.</span><span class="sxs-lookup"><span data-stu-id="86489-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="86489-p118">Cet exemple recherche trois dossiers de boîtes aux lettres différente. Vous pouvez utiliser la syntaxe de requête similaire pour rechercher les dossiers cachés dans le dossier des éléments récupérables d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86489-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="86489-191">Cet exemple montre comment rechercher un dossier de boîte aux lettres pour les éléments qui contiennent une expression exacte.</span><span class="sxs-lookup"><span data-stu-id="86489-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="86489-192">Cet exemple recherche un dossier de site (et ses sous-dossiers) pour les documents qui contiennent les lettres « Accord de confidentialité » dans le titre.</span><span class="sxs-lookup"><span data-stu-id="86489-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="86489-193">Cet exemple recherche dans un dossier de site (et ses sous-dossiers) pour les documents ont été modifiées dans une plage de dates.</span><span class="sxs-lookup"><span data-stu-id="86489-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="86489-194">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="86489-194">More information</span></span>

<span data-ttu-id="86489-195">Gardez les éléments suivants à l’esprit lorsque vous utilisez le script dans cet article et effectue ciblés collections.</span><span class="sxs-lookup"><span data-stu-id="86489-195">Keep the following things in mind when using the script in this article and performing targeted collections.</span></span>
  
- <span data-ttu-id="86489-p119">Le script ne supprime pas tous les dossiers à partir des résultats. Pour certains dossiers répertoriés dans les résultats peuvent être impossibles à rechercher (ou renvoyer des éléments de zéro), car elles contiennent le contenu généré par le système.</span><span class="sxs-lookup"><span data-stu-id="86489-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="86489-p120">Ce script renvoie uniquement des informations de dossier de boîte aux lettres principale de l’utilisateur. Elle ne renvoie aucune information sur les dossiers de boîte aux lettres de l’utilisateur archive.</span><span class="sxs-lookup"><span data-stu-id="86489-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="86489-p121">Lors de la recherche dans les dossiers de boîte aux lettres, uniquement dans le dossier spécifié (identifié par son `folderid` propriété) portera. Les sous-dossiers ne sont pas être recherchés. Pour rechercher des sous-dossiers, vous devez utiliser le `folderid` pour le dossier que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="86489-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  `folderid` for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="86489-203">Lors de la recherche des dossiers du site, le dossier (identifiée par son `path` propriété) et tous les sous-dossiers sont recherchées.</span><span class="sxs-lookup"><span data-stu-id="86489-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="86489-p122">Comme indiqué précédemment, vous ne pouvez pas utiliser `path` propriété pour rechercher des fichiers multimédias, tels que .png, .tiff ou les fichiers .wav, situés dans des emplacements de OneDrive. Une autre [propriété site](keyword-queries-and-search-conditions.md#searchable-site-properties) permet de rechercher des fichiers multimédias dans les dossiers OneDrive.</span><span class="sxs-lookup"><span data-stu-id="86489-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 
