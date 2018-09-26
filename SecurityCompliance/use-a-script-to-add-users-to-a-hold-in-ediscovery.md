---
title: Utiliser un script pour ajouter des utilisateurs à une suspension dans un cas de découverte électronique de sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Exécuter un script afin d’ajouter rapidement des boîtes aux lettres et de OneDrive entreprise des sites à une suspension nouveau associé à un cas de découverte électronique de sécurité Office 365 &amp; centre de conformité.
ms.openlocfilehash: 2c93deb14bc8c1f89dab7bb054d2e94db06cfbd5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038257"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Utiliser un script pour ajouter des utilisateurs à une suspension dans un cas de découverte électronique de sécurité Office 365 &amp; centre de conformité

L’Office 365 Security &amp; centre de conformité fournit beaucoup des applets de commande Windows PowerShell qui vous permettent d’automatiser les tâches longues liées à la création et la gestion des cas eDiscovery. Actuellement, à l’aide de l’outil cas eDiscovery dans la sécurité &amp; centre de conformité pour placer un grand nombre d’emplacements de contenu dépositaire en attente prend la préparation et du temps. Par exemple, avant de créer une suspension, vous devez recueillir l’URL pour chaque site d’entreprise que vous souhaitez mettre en attente OneDrive. Puis pour chaque utilisateur que vous souhaitez mettre en attente, vous devez ajouter leur boîte aux lettres et leur site Business OneDrive à la suspension. Dans les futures versions de la sécurité &amp; centre de conformité, cela obtiendra plus facile à faire. En attendant, vous pouvez utiliser le script dans cet article pour automatiser ce processus.
  
Le script vous invite à fournir le nom de domaine du site Mon site dans votre organisation (par exemple, **contoso** dans l’URL https://contoso-my.sharepoint.com), le nom d’un cas de découverte électronique existant, le nom de la nouvelle mise en attente qui associés au cas, une liste d’adresses de messagerie des utilisateurs que vous souhaitez Pour mettre en attente et une requête de recherche à utiliser si vous souhaitez créer une suspension basée sur une requête. Le script obtient ensuite l’URL pour le site de l’entreprise pour chaque utilisateur dans la liste OneDrive, crée la suspension de nouveau, puis ajoute la boîte aux lettres et OneDrive pour le site de l’entreprise pour chaque utilisateur dans la liste à la suspension. Le script génère également des fichiers journaux qui contiennent des informations sur la mise en attente. 
  
Voici comment procéder :
  
[Étape 1 : installer SharePoint Online Management Shell](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[Étape 2 : Générer une liste d’utilisateurs](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Étape 3 : Exécuter le script pour créer une suspension et ajouter des utilisateurs](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité et un administrateur global de SharePoint Online pour exécuter le script à l’étape 3. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
- Un maximum de 1 000 boîtes aux lettres et 100 sites peut être ajouté à une suspension associé à un cas de découverte électronique dans la sécurité &amp; centre de conformité. En supposant que tous les utilisateurs que vous souhaitez mettre en attente a un OneDrive pour le site de l’entreprise, vous pouvez ajouter un maximum de 100 utilisateurs à une suspension à l’aide du script dans cet article. 
    
- Veillez à enregistrer la liste des utilisateurs que vous créez dans l’étape 2 et le script à l’étape 3 dans le même dossier. Qui facilitera exécuter le script.
    
- Le script ajoute la liste des utilisateurs à une suspension nouveau qui est associée à un cas existant. N’oubliez pas que vous souhaitez associer la suspension avec création avant d’exécuter le script.
    
- Le script inclut la gestion des erreurs minimale. Son objectif principal est rapidement et facilement placer la boîte aux lettres et OneDrive pour le site d’entreprise de chaque utilisateur de blocage.
    
- Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Étape 1 : installer SharePoint Online Management Shell

La première étape consiste à installer SharePoint Online Management Shell s’il n’est pas déjà installé sur votre ordinateur local. Vous n’êtes pas obligé d’utiliser le shell de cette procédure, mais vous devez l’installer, car il contient les conditions préalables requises par le script que vous exécutez l’étape 3. Ces conditions préalables autoriser le script communiquer avec SharePoint Online pour obtenir l’URL pour OneDrive pour les sites.
  
Accédez à [configurer l’environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuer l’étape 1 et l’étape 2 pour installer SharePoint Online Management Shell sur votre ordinateur local. 

## <a name="step-2-generate-a-list-of-users"></a>Étape 2 : Générer une liste d’utilisateurs
<a name="step2"> </a>

Le script à l’étape 3 crée une suspension associé à un cas eDiscovery et ajoutez les boîtes aux lettres et OneDrive pour les sites d’entreprise d’une liste d’utilisateurs à la suspension. Vous pouvez taper les adresses de messagerie dans un fichier texte, ou vous pouvez exécuter une commande de Windows PowerShell pour obtenir une liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier que vous allez enregistrer le script à l’étape 3).
  
Voici une commande PowerShell (que vous exécutez à l’aide de PowerShell à distance connecté à votre organisation Exchange Online) pour obtenir une liste des adresses de messagerie pour tous les utilisateurs de votre organisation et enregistrez-le dans un fichier texte nommé HoldUsers.txt.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

Une fois que vous exécutez cette commande, ouvrez le fichier texte et supprimez l’en-tête qui contient le nom de la propriété `PrimarySmtpAddress`. Supprimez toutes les adresses de messagerie à l’exception de celles pour les utilisateurs que vous souhaitez ajouter à la suspension que vous créerez à l’étape 3. Assurez-vous qu’il n’y aucune ligne vide avant ou après la liste des adresses de messagerie.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Étape 3 : Exécuter le script pour créer une suspension et ajouter des utilisateurs
<a name="step3"> </a>

Lorsque vous exécutez le script dans cette étape, il vous invite à vous pour obtenir les informations suivantes. Veillez à préparer les informations suivantes avant d’exécuter le script.
  
- **Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à la sécurité &amp; centre de conformité avec PowerShell à distance. Il utilise également ces informations d’identification pour accéder à SharePoint Online pour obtenir le OneDrive pour les URL de l’entreprise pour la liste des utilisateurs.
    
- **Nom de votre domaine monsite** - monsite le domaine est le domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation. Par exemple, si l’URL de votre domaine monsite est **https://contoso-my.sharepoint.com**, puis entrez `contoso` lorsque le script vous demande le nom de votre domaine monsite. 
    
- **Nom du dossier** - le nom d’un cas existant. Le script crée une nouvelle suspension qui est associée à ce cas.
    
- **Nom de la suspension** - le nom de la suspension, le script crée et associer la casse spécifiée.
    
- **Blocage de requête de recherche pour basée sur une requête** - vous pouvez créer une suspension basée sur une requête afin qu’uniquement le contenu qui répond aux critères de recherche est mis en attente. Pour placer tous les contenus en attente, appuyez sur **entrée** lorsque vous êtes invité à une requête de recherche. 
    
- **S’il faut activer la suspension** - le script peut être activer la suspension après sa création ou le script peut être créer la suspension sans l’activer. Si vous n’avez pas le script activer la mise en attente, vous pouvez l’activer ultérieurement dans la sécurité &amp; centre de conformité ou en exécutant les commandes PowerShell suivantes : 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **Nom du fichier texte avec la liste des utilisateurs** : le nom du fichier texte à l’étape 2 qui contient la liste des utilisateurs à ajouter à la suspension. Si ce fichier se trouve dans le même dossier que le script, il suffit de taper le nom du fichier (par exemple, HoldUsers.txt). Si le fichier texte est dans un autre dossier, tapez le chemin d’accès complet du fichier.
    
Une fois que vous avez collecté les informations qui vous invite à vous pour le script, l’étape finale consiste à exécuter le script pour créer la nouvelle suspension et ajouter des utilisateurs.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `AddUsersToHold.ps1`.
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Office 365 Security &amp; Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Office 365 Security &amp; Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
      }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to http://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.
    
3. Exécuter le script ; par exemple :
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Entrez les informations qui vous demande le script.
    
    Le script se connecte à la sécurité et conformité centre PowerShell, puis crée la suspension de nouveau dans le cas de découverte électronique et ajoute les boîtes aux lettres et OneDrive entreprise pour les utilisateurs de la liste. Vous pouvez accéder à la casse dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité pour afficher la mise en attente. 
    
Une fois que le script est terminé en cours d’exécution, il crée les fichiers journaux suivants et les enregistre dans le dossier où se trouve le script.
  
- **LocationsOnHold.txt** - contient une liste des boîtes aux lettres et OneDrive pour les sites entreprise le script correctement mis en attente.
    
- **LocationsNotOnHold.txt** - contient une liste des boîtes aux lettres et OneDrive pour les sites d’entreprise qui le script ne pas mettre en attente. Si l’utilisateur a une boîte aux lettres, mais pas OneDrive site de l’entreprise, l’utilisateur doit être inclus dans la liste de OneDrive pour les sites d’entreprise qui n’ont pas été mis en attente.
    
- **GetCaseHoldPolicy.txt** - contient le résultat de l’applet de commande **Get-CaseHoldPolicy** pour la nouvelle suspension, le script s’est exécuté après la création de la nouvelle mise en attente. Les informations renvoyées par cette applet de commande comprend une liste d’utilisateurs dont les boîtes aux lettres et OneDrive pour les sites ont été mis en attente et si la suspension est activée ou désactivée. 
    
- **GetCaseHoldRule.txt** - contient le résultat de l’applet de commande **Get-CaseHoldRule** pour la nouvelle suspension, le script s’est exécuté après la création de la nouvelle mise en attente. Les informations renvoyées par cette applet de commande incluent la requête de recherche si vous avez utilisé le script pour créer une suspension basée sur une requête. 
