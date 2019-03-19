---
title: Créer, générer des rapports et supprimer plusieurs recherches de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Découvrez comment automatiser des tâches de recherche de contenu, telles que la création de recherches et l'exécution de rapports &amp; via des scripts PowerShell dans le centre de sécurité conformité Office 365.
ms.openlocfilehash: 740f3384e5d4f26e09512cc846ad8779bcbc31ef
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670659"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Créer, générer des rapports et supprimer plusieurs recherches de contenu

 La création et la création rapide de rapports de recherches de découverte est souvent une étape importante dans eDiscovery et des investigations lorsque vous essayez d'en savoir plus sur les données sous-jacentes, ainsi que la richesse et la qualité de vos recherches. Pour vous aider, le centre de sécurité &amp; conformité offre un ensemble d'applets de commande Windows PowerShell pour automatiser les tâches de recherche de contenu gourmandes en temps. Ces scripts offrent un moyen rapide et simple de créer plusieurs recherches, puis d'exécuter des rapports sur les résultats de recherche estimés qui peuvent vous aider à déterminer la quantité de données en question. Vous pouvez également utiliser les scripts pour créer différentes versions des recherches afin de comparer les résultats générés par chacun d'entre eux. Ces scripts peuvent vous aider à identifier et à rechercher rapidement vos données. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité &amp; conformité pour exécuter les scripts décrits dans cette rubrique. 
    
- Pour collecter une liste des URL pour les sites OneDrive entreprise de votre organisation que vous pouvez ajouter au fichier CSV à l'étape 1, reportez-vous à la rubrique [créer une liste de tous les emplacements OneDrive de votre organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Veillez à enregistrer tous les fichiers que vous créez dans cette rubrique dans le même dossier. Cela facilitera l'exécution des scripts.
    
- Les scripts incluent une gestion des erreurs minimale. Leur objectif principal est de créer, de générer des rapports et de supprimer rapidement plusieurs recherches de contenu.
    
- Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Étape 1: créer un fichier CSV contenant des informations sur les recherches à exécuter

Le fichier de valeurs séparées par des virgules (CSV) que vous créez dans cette étape contient une ligne pour chaque utilisateur qui souhaite effectuer une recherche. Vous pouvez effectuer une recherche dans la boîte aux lettres Exchange Online de l'utilisateur (qui inclut la boîte aux lettres d'archivage, si elle est activée) et son site OneDrive entreprise. Vous pouvez également rechercher uniquement dans la boîte aux lettres ou dans le site OneDrive entreprise. Vous pouvez également effectuer des recherches dans n'importe quel site de votre organisation SharePoint Online. Le script que vous exécutez à l'étape 3 crée une recherche distincte pour chaque ligne dans le fichier CSV. 
  
1. Copiez et collez le texte suivant dans un fichier. txt à l'aide du bloc-notes. Enregistrez ce fichier dans un dossier sur votre ordinateur local. Vous allez également enregistrer les autres scripts dans ce dossier.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    La première ligne, ou ligne d'en-tête, du fichier répertorie les paramètres qui seront utilisés par la cmdlet **New-ComplianceSearch** (dans le script de l'étape 3) pour créer des recherches de contenu. Les noms des paramètres sont séparés par des virgules. Vérifiez qu'il n'y a pas d'espaces dans la ligne d'en-tête. Chaque ligne sous la ligne d'en-tête représente les valeurs des paramètres de chaque recherche. Veillez à remplacer les données d'espace réservé dans le fichier CSV par vos données réelles. 
    
2. Ouvrez le fichier. txt dans Excel, puis utilisez les informations du tableau suivant pour modifier le fichier avec les informations pour chaque recherche. 
    
    |**Paramètre**|**Description**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |Adresse SMTP de la boîte aux lettres de l'utilisateur.  <br/> |
    | `SharePointLocation` <br/> |L'URL du site OneDrive entreprise de l'utilisateur ou l'URL de n'importe quel site de votre organisation. Pour l'URL des sites OneDrive entreprise, utilisez le format suivant: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Par exemple,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.  <br/> |
    | `ContentMatchQuery` <br/> |Requête de recherche pour la recherche. Pour plus d'informations sur la création d'une requête de recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).  <br/> |
    | `StartDate` <br/> |Pour le courrier électronique, date à laquelle un message a été reçu par un destinataire ou envoyé par l'expéditeur. Pour les documents sur les sites SharePoint ou OneDrive entreprise, date de la dernière modification d'un document.  <br/> |
    | `EndDate` <br/> |Pour le courrier électronique, date à laquelle un message a été envoyé par l'utilisateur ou avant celui-ci. Pour les documents sur les sites SharePoint ou OneDrive entreprise, date de la dernière modification d'un document.  <br/> |
   
3. Enregistrez le fichier Excel en tant que fichier CSV dans un dossier sur votre ordinateur local. Le script que vous créez à l'étape 3 utilise les informations contenues dans ce fichier CSV pour créer les recherches. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Étape 2: Connectez-vous au centre de sécurité & Compliance Center PowerShell

L'étape suivante consiste à connecter Windows PowerShell au centre de &amp; sécurité conformité de votre organisation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `ConnectSCC.ps1`. Enregistrez le fichier dans le dossier dans lequel vous avez enregistré le fichier CSV à l'étape 1.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier dans lequel se trouve le script que vous avez créé à l'étape précédente, puis exécutez le script; par exemple:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Étape 3: exécuter le script pour créer et démarrer les recherches

Le script de cette étape crée une recherche de contenu distincte pour chaque ligne dans le fichier CSV que vous avez créé à l'étape 1. Lorsque vous exécutez ce script, vous êtes invité à indiquer deux valeurs:
  
- **ID de groupe de recherche** : ce nom permet d'organiser facilement les recherches créées à partir du fichier CSV. Chaque recherche créée est nommée avec l'ID de groupe de recherche, puis un numéro est ajouté au nom de la recherche. Par exemple, si vous entrez **ContosoCase** pour l'ID de groupe de recherche, les recherches sont nommées **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, etc. Notez que le nom que vous tapez est sensible à la casse. Lorsque vous utilisez l'ID de groupe de recherche à l'étape 4 et à l'étape 5, vous devez utiliser la même casse que celle que vous avez utilisée lors de sa création. 
    
- **Fichier CSV** : nom du fichier CSV que vous avez créé à l'étape 1. Veillez à inclure le nom de fichier complet, en incluant l'extension de fichier. csv; par exemple, `ContosoCase.csv`.
    
Pour exécuter le script :

1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `CreateSearches.ps1`. Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.
    
  ```Powershell
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

2. Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l'étape précédente, puis exécutez le script. par exemple:
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. À l'invite **ID de groupe de recherche** , tapez un nom de groupe de recherche, puis appuyez sur **entrée**; par exemple, `ContosoCase`. N'oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière dans les étapes suivantes.
    
4. À l'invite **fichier csv source** , tapez le nom du fichier CSV, y compris l'extension de fichier. csv; par exemple, `ContosoCase.csv`.
    
5. Appuyez sur **entrée** pour poursuivre l'exécution du script. 
    
    Le script affiche la progression de la création et de l'exécution des recherches. Une fois le script terminé, il revient à l'invite. 
    
    ![Exemple de sortie après exécution du script pour créer plusieurs recherches de la conformité](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Étape 4: exécuter le script pour signaler les estimations de recherche

Une fois que vous avez créé les recherches, l'étape suivante consiste à exécuter un script qui affiche un rapport simple du nombre d'accès de recherche pour chaque recherche créée à l'étape 3. Le rapport inclut également la taille des résultats pour chaque recherche, ainsi que le nombre total d'accès et la taille totale de toutes les recherches. Lorsque vous exécutez le script de création de rapports, vous êtes invité à entrer l'ID de groupe de recherche et un nom de fichier CSV Si vous voulez enregistrer le rapport dans un fichier CSV.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `SearchReport.ps1`. Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.
    
  ```Powershell
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

2. Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l'étape précédente, puis exécutez le script. par exemple:
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. À l'invite **ID de groupe de recherche** , tapez un nom de groupe de recherche, puis appuyez sur **entrée**; par exemple `ContosoCase`. N'oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière que lorsque vous avez exécuté le script à l'étape 3.
    
4. Dans le **chemin d'accès du fichier pour enregistrer le rapport dans un fichier CSV (laissez vide pour afficher l'État)** , tapez le chemin d'accès complet du nom de fichier (y compris l'extension. csv) si vous souhaitez enregistrer le rapport dans un fichier CSV. nom du fichier CSV, y compris l'extension de fichier. csv. Par exemple, vous pouvez taper `ContosoCaseReport.csv` pour l'enregistrer dans le répertoire actif ou taper `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` pour l'enregistrer dans un autre dossier. Vous pouvez également laisser l'invite vide pour afficher le rapport sans l'enregistrer dans un fichier. 
    
5. Appuyez sur **Entrée**.
    
    Le script affiche la progression de la création et de l'exécution des recherches. Une fois le script terminé, le rapport est affiché. 
    
    ![Exécutez le rapport de recherche pour afficher les estimations pour le groupe de recherche](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Si la même boîte aux lettres ou le même site est spécifié en tant qu'emplacement de contenu dans plusieurs recherches dans un groupe de recherche, le nombre total d'estimations de résultats dans le rapport (pour le nombre d'éléments et la taille totale) peut inclure les résultats pour les mêmes éléments. Cela est dû au fait que le même message électronique ou document est comptabilisé plusieurs fois s'il correspond à la requête pour différentes recherches dans le groupe de recherche. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Étape 5: exécuter le script pour supprimer les recherches

Étant donné que vous pouvez créer un grand nombre de recherches, ce dernier script facilite la suppression rapide des recherches que vous avez créées à l'étape 3. Comme les autres scripts, il vous invite également à indiquer l'ID de groupe de recherche. Toutes les recherches avec l'ID de groupe de recherche dans le nom de recherche seront supprimées lorsque vous exécuterez ce script. 
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `DeleteSearches.ps1`. Enregistrez le fichier dans le dossier où vous avez enregistré les autres fichiers.
    
  ```Powershell
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

2. Dans Windows PowerShell, accédez au dossier dans lequel vous avez enregistré le script à l'étape précédente, puis exécutez le script. par exemple:
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. À l'invite **ID de groupe de recherche** , tapez un nom de groupe de recherche pour les recherches que vous souhaitez supprimer, puis appuyez sur **entrée**; par exemple, `ContosoCase`. N'oubliez pas que ce nom est sensible à la casse, de sorte que vous devez le taper de la même manière que lorsque vous avez exécuté le script à l'étape 3.
    
    Le script affiche le nom de chaque recherche qui a été supprimée.
    
    ![Exécutez le script pour supprimer les recherches dans le groupe de recherche](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
