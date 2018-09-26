---
title: Créer, générer des rapports et supprimer plusieurs recherches de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Découvrez comment automatiser les tâches de recherche de contenu à créer des recherches et exécuter des rapports via des scripts PowerShell de sécurité Office 365 &amp; centre de conformité.
ms.openlocfilehash: a32c003dfd9a27ea8c38b29b31001b612368bc4a
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038137"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Créer, générer des rapports et supprimer plusieurs recherches de contenu

 Rapidement de créer et de signaler les recherches de découverte sont souvent une étape importante dans eDiscovery et des investigations lorsque vous essayez d’en savoir plus sur les données sous-jacentes et la plus grande richesse et la qualité de vos recherches. Pour vous aider à cela, la sécurité &amp; centre de conformité propose un ensemble d’applets de commande Windows PowerShell pour automatiser les tâches de recherche de contenu beaucoup de temps. Ces scripts fournissent un moyen simple et rapide pour créer un nombre de recherches et exécuter des rapports de l’estimation des résultats de recherche qui peuvent vous aider à déterminer la quantité de données en question. Vous pouvez également utiliser les scripts pour créer des versions différentes de recherches pour comparer les résultats de que chaque produit. Ces scripts peuvent vous aider à identifier et de vos données de réforme rapidement et efficacement. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter les scripts qui sont décrites dans cette rubrique. 
    
- Pour collecter une liste d’URL pour le OneDrive des sites d’entreprise de votre organisation que vous pouvez ajouter au fichier CSV à l’étape 1, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Veillez à enregistrer tous les fichiers que vous créez dans cette rubrique pour le même dossier. Qui facilitera exécuter les scripts.
    
- Les scripts minimal gestion des erreurs. Leur principal objectif consiste à créer rapidement, rapport et supprimer plusieurs recherches de contenu.
    
- Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Étape 1 : Créer un fichier CSV qui contient des informations sur la recherche que vous souhaitez exécuter

Le fichier (CSV) de valeurs séparées par des virgules que vous créez dans cette étape contient une ligne pour chaque utilisateur que vous souhaitez effectuer une recherche. Vous pouvez rechercher boîte aux lettres Exchange Online le sa (qui inclut la boîte aux lettres d’archivage, si elle est activée) et leur OneDrive pour le site de l’entreprise. Ou vous pouvez rechercher uniquement dans la boîte aux lettres ou OneDrive pour le site de l’entreprise. Vous pouvez également rechercher tous les sites dans votre organisation SharePoint Online. Le script que vous exécutez l’étape 3 crée une recherche distincte pour chaque ligne dans le fichier CSV. 
  
1. Copiez et collez le texte suivant dans un fichier .txt en utilisant le bloc-notes. Enregistrez ce fichier dans un dossier sur votre ordinateur local. Vous allez enregistrer les autres scripts pour ce dossier.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    La première ligne, ou ligne d’en-tête du fichier répertorie les paramètres qui servira à l’applet de commande **New-ComplianceSearch** (dans le script à l’étape 3) pour créer une nouvelle recherche de contenu. Nom de chaque paramètre est séparée par une virgule. Assurez-vous que le document ne contient pas d’espaces dans la ligne d’en-tête. Chaque ligne sous la ligne d’en-tête représente les valeurs de paramètre pour chaque recherche. Veillez à remplacer les données d’espace réservé dans le fichier CSV avec vos données réelles. 
    
2. Ouvrez le fichier .txt dans Excel, puis utilisez les informations dans le tableau suivant pour modifier le fichier avec les informations de chaque recherche. 
    
    |**Paramètre**|**Description**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |L’adresse SMTP de boîte aux lettres de l’utilisateur.  <br/> |
    | `SharePointLocation` <br/> |L’URL de OneDrive l’utilisateur pour le site de l’entreprise ou l’URL d’un site dans votre organisation. Pour l’URL de OneDrive pour les sites, utilisez ce format : ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Par exemple, `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.<br/> |
    | `ContentMatchQuery` <br/> |La requête de recherche pour la recherche. Pour plus d’informations sur la création d’une requête de recherche, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).<br/> |
    | `StartDate` <br/> |Pour le courrier électronique, la date ou après un message a été reçue par un destinataire ou envoyée par l’expéditeur. Pour les documents dans SharePoint ou OneDrive pour les sites de l’entreprise, la date ou après un document a été modifiée.  <br/> |
    | `EndDate` <br/> |Pour le courrier électronique, la date ou avant qu’un message a été envoyée par un envoyé par l’utilisateur. Pour les documents dans SharePoint ou OneDrive pour les sites de l’entreprise, la date ou avant un document a été modifiée.  <br/> |
   
3. Enregistrez le fichier Excel dans un fichier CSV dans un dossier sur votre ordinateur local. Le script que vous créez à l’étape 3 utilise les informations dans ce fichier CSV pour créer les recherches. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Étape 2 : Se connecter à PowerShell du centre de conformité et de sécurité

L’étape suivante consiste à connecter Windows PowerShell pour la sécurité &amp; centre de conformité pour votre organisation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `ConnectSCC.ps1`. Enregistrez le fichier dans le même dossier que vous avez enregistré le fichier CSV pour à l’étape 1.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Étape 3 : Exécuter le script pour créer et lancer des recherches

Le script dans cette étape crée une recherche de contenu distincte pour chaque ligne dans le fichier CSV que vous avez créé à l’étape 1. Lorsque vous exécutez ce script, vous serez invité pour deux valeurs :
  
- **ID de groupe de recherche** - ce nom fournit un moyen facile pour organiser les recherches qui sont créés à partir du fichier CSV. Chaque recherche qui est créé est appelée avec l’ID de groupe de recherche, puis un numéro est ajouté au nom de la recherche. Par exemple, si vous entrez **ContosoCase** pour l’ID de groupe de recherche, les recherches sont nommés **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**et ainsi de suite. Notez que le nom que vous tapez respecte la casse. Lorsque vous utilisez l’ID de groupe de recherche dans l’étape 4 et 5 étape, vous devez utiliser la même casse que vous avez effectuées lors de sa création. 
    
- **Fichier CSV** - le nom du fichier CSV que vous avez créé à l’étape 1. Veillez à inclure l’utilisation du nom complet, l’extension de fichier .csv ; par exemple, `ContosoCase.csv`.
    
Pour exécuter le script :

1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `CreateSearches.ps1`. Enregistrez le fichier dans le même dossier où vous avez enregistré les autres fichiers.
    
  ```
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. Dans Windows PowerShell, accédez au dossier où vous avez enregistré le script à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\CreateSearches.ps1
    ```

3. À l’invite de **l’ID de groupe de recherche** , tapez le nom d’un groupe de recherche, puis appuyez sur **entrée**. par exemple, `ContosoCase`. N’oubliez pas que ce nom respecte la casse, afin d’avoir à taper de la même manière dans les étapes suivantes.
    
4. À l’invite de **fichier CSV Source** , tapez le nom du fichier CSV, y compris l’extension de fichier .csv ; par exemple, `ContosoCase.csv`.
    
5. Appuyez sur **entrée** pour poursuivre l’exécution du script. 
    
    Le script affiche la progression de la création et l’exécution de la recherche. Lorsque le script est terminé, il renvoie à l’invite. 
    
    ![Exemple de sortie après exécution du script pour créer plusieurs recherches de la conformité](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Étape 4 : Exécuter le script pour la recherche de rapports estime

Après avoir créé les recherches, l’étape suivante consiste à exécuter un script qui affiche un rapport simple du nombre de résultats de recherche pour chaque recherche qui a été créé à l’étape 3. Le rapport inclut également la taille des résultats pour chaque recherche et le nombre total d’accès et la taille totale de toutes les recherches. Lorsque vous exécutez le script de création de rapports, vous serez invité pour l’ID de groupe de recherche et un nom de fichier CSV si vous souhaitez enregistrer le rapport dans un fichier CSV.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `SearchReport.ps1`. Enregistrez le fichier dans le même dossier où vous avez enregistré les autres fichiers.
    
  ```
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. Dans Windows PowerShell, accédez au dossier où vous avez enregistré le script à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\SearchReport.ps1
    ```

3. À l’invite de **l’ID de groupe de recherche** , tapez le nom d’un groupe de recherche, puis appuyez sur **entrée**. par exemple `ContosoCase`. N’oubliez pas que ce nom respecte la casse, afin que vous devrez entrer la même manière que lorsque vous avez exécuté le script à l’étape 3.
    
4. À l’invite de **chemin d’accès pour enregistrer le rapport dans un fichier CSV (laisser vide pour afficher le rapport) du fichier** , tapez un nom de fichier du chemin d’accès du nom de fichier complet (y compris l’extension de fichier .csv) si vous souhaitez enregistrer le rapport dans un fichier CSV. nom du fichier CSV, y compris l’extension de fichier .csv. Par exemple, vous pouvez taper `ContosoCaseReport.csv` pour l’enregistrer dans le répertoire actif ou vous pouvez taper `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` pour l’enregistrer dans un autre dossier. Vous pouvez également laisser l’invite vide pour afficher le rapport, mais pas l’enregistrer dans un fichier. 
    
5. Appuyez sur **entrée**.
    
    Le script affiche la progression de la création et l’exécution de la recherche. Lorsque le script est terminé, le rapport s’affiche. 
    
    ![Exécutez le rapport de recherche pour afficher les estimations pour le groupe de recherche](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Si la même boîte aux lettres ou du site est spécifié comme un emplacement de la plusieurs recherche dans un groupe de recherche de contenu, l’estimation du nombre total de résultats dans le rapport (pour le nombre d’éléments et la taille totale) peut inclure des résultats pour les mêmes éléments. C’est parce que le même message électronique ou un document est comptabilisée plusieurs fois s’il correspond à la requête pour les différentes recherches dans le groupe de recherche. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Étape 5 : Exécuter le script pour supprimer la recherche

Étant donné que vous pouvez créer un grand nombre de recherches, ce dernier script simplement facilite supprimer rapidement les recherches que vous avez créé à l’étape 3. Comme les autres scripts de celle-ci également vous invite à l’ID du groupe de recherche. Toutes les recherches avec l’ID de groupe de recherche dans le nom de la recherche seront supprimés lorsque vous exécutez ce script. 
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `DeleteSearches.ps1`. Enregistrez le fichier dans le même dossier où vous avez enregistré les autres fichiers.
    
  ```
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. Dans Windows PowerShell, accédez au dossier où vous avez enregistré le script à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\DeleteSearches.ps1
    ```

3. À l’invite de **l’ID de groupe de recherche** , tapez le nom d’un groupe de recherche pour la recherche que vous souhaitez supprimer, puis appuyez sur **entrée**. par exemple, `ContosoCase`. N’oubliez pas que ce nom respecte la casse, afin que vous devrez entrer la même manière que lorsque vous avez exécuté le script à l’étape 3.
    
    Le script affiche le nom de chaque recherche est supprimé.
    
    ![Exécutez le script pour supprimer les recherches dans le groupe de recherche](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
