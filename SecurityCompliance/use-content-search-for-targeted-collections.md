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
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Utiliser la recherche de contenu dans Office 365 pour les collections ciblées

La fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité ne fournit pas un moyen direct dans l’interface utilisateur de rechercher des dossiers spécifiques dans les boîtes aux lettres Exchange ou SharePoint et OneDrive pour les sites de l’entreprise. Toutefois, il est possible de rechercher des dossiers spécifiques (appelés un regroupement cible) en spécifiant l’ID de dossier ou le chemin d’accès dans la syntaxe de requête de recherche. À l’aide de la recherche de contenu pour effectuer un regroupement cible est utile lorsque vous êtes convaincu qu’articles réactifs à un cas ou privilégié se trouvent dans un dossier de boîte aux lettres ou un site spécifique. Vous pouvez utiliser le script dans cet article pour obtenir l’ID de dossier pour les dossiers de boîte aux lettres ou le chemin d’accès pour les dossiers SharePoint et OneDrive pour le site de l’entreprise. Puis vous pouvez utiliser l’ID de dossier ou le chemin d’accès dans une requête de recherche pour renvoyer des éléments situés dans le dossier.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script à l’étape 1. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
    En outre, vous devez attribuer le rôle destinataires de messagerie dans votre organisation Exchange Online. Cela est nécessaire pour exécuter l’applet de commande **Get-MailboxFolderStatistics** , qui est inclus dans le script à l’étape 1. Par défaut, le rôle destinataires de messagerie est assigné pour les groupes de rôles gestion de l’organisation et la gestion des destinataires dans Exchange Online. Pour plus d’informations sur l’attribution d’autorisations dans Exchange Online, voir [Gérer les membres du groupe de rôles](https://go.microsoft.com/fwlink/p/?linkid=692102). Vous pourriez également créer un groupe de rôles personnalisé, lui affecter le rôle destinataires de messagerie, puis ajoutez les membres qui ont besoin pour exécuter le script à l’étape 1. Pour plus d’informations, voir [Gérer les groupes de rôles](https://go.microsoft.com/fwlink/p/?linkid=730688).
    
- Chaque fois que vous exécutez le script à l’étape 1, une nouvelle session PowerShell distante est créée. Ainsi, vous pouvez utiliser des toutes les sessions à distance PowerShell disponibles. Pour éviter cette situation, vous pouvez exécuter la commande suivante pour vous déconnecter de vos sessions PowerShell distantes actives.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    Pour plus d'informations, reportez-vous à [Connexion à Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Le script inclut la gestion des erreurs minimale. Le principal objectif du script doit rapidement afficher la liste des ID de dossier de boîte aux lettres de site ou chemins d’accès qui peuvent être utilisés dans la syntaxe de requête de recherche d’une recherche de contenu pour effectuer un regroupement cible.
    
- L’exemple de script fourni dans cette rubrique n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>Étape 1 : Exécuter le script pour obtenir une liste de dossiers pour un site ou une boîte aux lettres

Le script que vous exécutez dans cette première étape renverra une liste de dossiers de boîte aux lettres ou SharePoint ou OneDrive pour les dossiers de l’entreprise et l’ID du dossier correspondant ou chemin d’accès pour chaque dossier. Lorsque vous exécutez ce script, il vous invite à vous pour obtenir les informations suivantes.
  
- **URL de site ou adresse de messagerie** Tapez une adresse de messagerie de le dépositaire pour renvoyer une liste de dossiers de boîte aux lettres Exchange et pliez ID. Ou tapez l’URL pour un site SharePoint ou un site de l’entreprise OneDrive pour retourner une liste de chemins d’accès pour le site spécifié. Voici quelques exemples : 
    
  - **Exchange** - stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **OneDrive entreprise** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à Exchange Online et de la sécurité &amp; centre de conformité avec PowerShell à distance. Comme expliqué précédemment, vous avez attribué les autorisations appropriées pour exécuter ce script.
    
Pour afficher la liste des dossiers de boîte aux lettres ou les noms de chemin d’accès du site :
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `GetFolderSearchParameters.ps1`.
    
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

2. Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.
    
3. Exécuter le script ; par exemple :
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. Entrez les informations qui vous demande le script.
    
    Le script affiche une liste des dossiers de boîte aux lettres ou un dossier de site pour l’utilisateur spécifié. Laissez cette fenêtre Ouvrir afin que vous pouvez copier un nom de dossier ID ou le chemin d’accès et le coller dans une requête de recherche à l’étape 2.
    
    > [!TIP]
    > Au lieu de l’affichage d’une liste de dossiers dans l’écran d’ordinateur, vous pouvez réorienter la sortie du script dans un fichier texte. Ce fichier sera enregistré dans le dossier où se trouve le script. Par exemple, pour rediriger le script de sortie dans un fichier texte, exécutez la commande suivante à l’étape 3 : `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` puis vous pouvez copier un ID de dossier ou un chemin d’accès du fichier à utiliser dans une requête de recherche.
  
### <a name="script-output-for-mailbox-folders"></a>Sortie du script pour les dossiers de boîte aux lettres

Si vous recevez un ID de dossier de boîte aux lettres, le script se connecte à Exchange Online à l’aide de PowerShell à distance, exécute l’applet de commande **Get-MailboxFolderStatisics** , puis affiche la liste des dossiers à partir de la boîte aux lettres spécifiée. Pour chaque dossier dans la boîte aux lettres, le script affiche le nom du dossier dans la colonne **FolderPath** et l’ID du dossier dans la colonne **FolderQuery** . En outre, le script ajoute le préfixe de **folderId** (qui est le nom de la propriété de la boîte aux lettres) à l’ID de dossier. Étant donné que la propriété **folderid** est une propriété disponible pour la recherche, vous allez utiliser `folderid:<folderid>` dans une requête de recherche à l’étape 2 pour rechercher ce dossier. 
  
Voici un exemple de sortie renvoyée par le script pour les dossiers de boîte aux lettres.
  
![Exemple de la liste des dossiers de boîte aux lettres et identificateurs renvoyés par le script de dossier](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
L’exemple à l’étape 2 montre la requête utilisée pour rechercher le sous-dossier vide dans le dossier éléments récupérables de l’utilisateur.
  
### <a name="script-output-for-site-folders"></a>Sortie du script pour les dossiers de site

Si vous recevez des chemins d’accès à partir de SharePoint ou OneDrive pour les sites de l’entreprise, le script se connecte à la sécurité &amp; centre de conformité à l’aide de PowerShell à distance, crée une recherche de contenu de recherche dans le site pour les dossiers, et puis affiche la liste des dossiers situé dans le site spécifié. Le script affiche le nom de chaque dossier et ajoute le préfixe du **chemin d’accès** (qui est le nom de la propriété site) à l’URL du dossier. Étant donné que la propriété **path** est une propriété disponible pour la recherche, vous allez utiliser `path:<path>` dans une requête de recherche à l’étape 2 pour rechercher ce dossier. 
  
Voici un exemple de sortie renvoyée par le script pour les dossiers de site.
  
![Exemple de la liste des chemins d’accès pour les dossiers site renvoyées par le script](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a>Étape 2 : Utiliser un ID de dossier ou un chemin d’accès pour effectuer un regroupement cible

Après avoir exécuté le script pour collecter une liste d’ID de dossier ou chemins d’accès pour un utilisateur spécifique, la prochaine étape pour accéder à la sécurité &amp; centre de conformité et créer une recherche de contenu pour rechercher un dossier spécifique. Vous allez utiliser le `folderid:<folderid>` ou `path:<path>` propriété dans la requête de recherche que vous configurez dans la zone mots clés de recherche de contenu (ou en tant que la valeur du paramètre *ContentMatchQuery* si vous utilisez l’applet de commande **New-ComplianceSearch** ). Vous pouvez combiner les `folderid` ou `path` propriété avec les autres paramètres de recherche ou de conditions de recherche. Si vous incluez uniquement la `folderid` ou `path` propriété dans la requête, la recherche retourne tous les éléments situés dans le dossier spécifié. 
  
> [!NOTE]
> À l’aide de la `path` propriété pour rechercher les emplacements de OneDrive ne renvoie des fichiers multimédias, tels que les fichiers .wav, .png et .tiff, dans les résultats de recherche. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide du compte et les informations d’identification que vous avez utilisé pour exécuter le script à l’étape 1.
    
3. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête** \> **recherche de contenu**, puis cliquez sur **Nouveau** ![icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
4. Sur la page **Nouvelle recherche**, entrez un nom pour la recherche de contenu. Ce nom doit être unique dans votre organisation. 
    
5. Sous **où souhaitez-vous rechercher**, effectuez l’une des valeurs suivantes, selon que votre recherche dans un dossier de boîte aux lettres ou un dossier de site :
    
    - Cliquez sur **Choisir les boîtes aux lettres spécifiques à rechercher** , puis ajoutez la même boîte aux lettres que vous avez spécifié lorsque vous avez exécuté le script à l’étape 1. 
    
      Ou
    
    - Cliquez sur **Choisir des sites spécifiques à rechercher** pour rechercher, puis ajoutez la même URL de site que vous avez spécifié lorsque vous avez exécuté le script à l’étape 1. 
    
6. Cliquez sur **Suivant**.
    
7. Dans la zone mots clés dans la page **que voulez-vous rechercher les** , collez la `folderid:<folderid>` ou `path:<path>` valeur qui a été renvoyée par le script à l’étape 1. 
    
    Par exemple, la requête dans la capture d’écran suivante recherche de tout élément dans le sous-dossier vide dans le dossier éléments récupérables de l’utilisateur (la valeur de la `folderid` propriété pour le sous-dossier purge est illustrée dans la capture d’écran à l’étape 1) :
    
    ![Collez le folderid ou le chemin d’accès dans la zone mots clés de la requête de recherche](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. Cliquez sur **Rechercher** pour lancer la recherche de regroupement cible. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>Exemples de requêtes de recherche pour les collections ciblées

Voici quelques exemples d’utilisation de la `folderid` et `path` propriétés dans une requête de recherche pour effectuer un regroupement cible. Notez que les espaces réservés sont utilisés pour `folderid:<folderid>` et `path:<path>` pour économiser de l’espace. 
  
- Cet exemple recherche trois dossiers de boîtes aux lettres différente. Vous pouvez utiliser la syntaxe de requête similaire pour rechercher les dossiers cachés dans le dossier des éléments récupérables d’un utilisateur.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- Cet exemple montre comment rechercher un dossier de boîte aux lettres pour les éléments qui contiennent une expression exacte.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- Cet exemple recherche un dossier de site (et ses sous-dossiers) pour les documents qui contiennent les lettres « Accord de confidentialité » dans le titre.
    
  ```
  path:<path> AND filename:nda
  ```

- Cet exemple recherche dans un dossier de site (et ses sous-dossiers) pour les documents ont été modifiées dans une plage de dates.
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>Plus d'informations

Gardez les éléments suivants à l’esprit lorsque vous utilisez le script dans cet article et effectue ciblés collections.
  
- Le script ne supprime pas tous les dossiers à partir des résultats. Pour certains dossiers répertoriés dans les résultats peuvent être impossibles à rechercher (ou renvoyer des éléments de zéro), car elles contiennent le contenu généré par le système.
    
- Ce script renvoie uniquement des informations de dossier de boîte aux lettres principale de l’utilisateur. Elle ne renvoie aucune information sur les dossiers de boîte aux lettres de l’utilisateur archive.
    
- Lors de la recherche dans les dossiers de boîte aux lettres, uniquement dans le dossier spécifié (identifié par son `folderid` propriété) portera. Les sous-dossiers ne sont pas être recherchés. Pour rechercher des sous-dossiers, vous devez utiliser le `folderid` pour le dossier que vous souhaitez rechercher. 
    
- Lors de la recherche des dossiers du site, le dossier (identifiée par son `path` propriété) et tous les sous-dossiers sont recherchées. 
    
- Comme indiqué précédemment, vous ne pouvez pas utiliser `path` propriété pour rechercher des fichiers multimédias, tels que .png, .tiff ou les fichiers .wav, situés dans des emplacements de OneDrive. Une autre [propriété site](keyword-queries-and-search-conditions.md#searchable-site-properties) permet de rechercher des fichiers multimédias dans les dossiers OneDrive. 
