---
title: Utiliser un script pour ajouter des utilisateurs à une conservation dans un cas eDiscovery dans le centre de &amp; sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Exécutez un script pour ajouter rapidement des boîtes aux lettres et des sites OneDrive entreprise à un nouveau blocage associé à un cas eDiscovery dans le centre de sécurité &amp; conformité Office 365.
ms.openlocfilehash: f71c82a830f029f8137a60d8329e30be0e7eeb46
ms.sourcegitcommit: 54a2cbe5d13f448e0c28655bdf88deb9e5434cac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30935239"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Utiliser un script pour ajouter des utilisateurs à une conservation dans un cas eDiscovery dans le centre de &amp; sécurité conformité Office 365

Le centre de sécurité &amp; conformité Office 365 fournit un grand nombre d'applets de commande Windows PowerShell qui vous permettent d'automatiser les tâches fastidieuses liées à la création et à la gestion des cas eDiscovery. Actuellement, l'utilisation de l'outil de cas eDiscovery &amp; dans le centre de conformité et de sécurité pour mettre en attente un grand nombre d'emplacements de contenu de dépositaire prend du temps et une préparation. Par exemple, avant de créer une conservation, vous devez collecter l'URL de chaque site OneDrive entreprise que vous souhaitez mettre en attente. Ensuite, pour chaque utilisateur que vous souhaitez mettre en attente, vous devez ajouter sa boîte aux lettres et son site OneDrive entreprise à la suspension. Dans les versions ultérieures du &amp; Centre de sécurité conformité, cela sera plus facile à réaliser. En attendant, vous pouvez utiliser le script de cet article pour automatiser ce processus.
  
Le script vous invite à indiquer le nom du domaine mon site de votre organisation (par exemple, **contoso** dans l' https://contoso-my.sharepoint.com)URL, le nom d'un cas eDiscovery existant, le nom du nouveau blocage associé au cas, une liste des adresses de messagerie des utilisateurs de votre choix à mettre en attente et une requête de recherche à utiliser si vous souhaitez créer une conservation basée sur une requête. Le script obtient ensuite l'URL du site OneDrive entreprise pour chaque utilisateur de la liste, crée la nouvelle conservation, puis ajoute la boîte aux lettres et le site OneDrive entreprise pour chaque utilisateur de la liste à la suspension. Le script génère également des fichiers journaux qui contiennent des informations sur la nouvelle conservation. 
  
Voici la procédure à suivre:
  
[Étape 1 : installer SharePoint Online Management Shell](#step-1-install-the-sharepoint-online-management-shell)
  
[Étape 2: générer une liste d'utilisateurs](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Étape 3: exécuter le script pour créer une conservation et ajouter des utilisateurs](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité &amp; conformité et d'un administrateur global SharePoint Online pour exécuter le script à l'étape 3. Pour plus d'informations, consultez [la rubrique attribution d'autorisations eDiscovery dans &amp; le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).
    
- Un maximum de 1 000 boîtes aux lettres et de 100 sites peuvent être ajoutés à une conservation qui est associée à un cas de découverte &amp; électronique dans le centre de sécurité conformité. En supposant que chaque utilisateur que vous souhaitez mettre en attente dispose d'un site OneDrive entreprise, vous pouvez ajouter un maximum de 100 utilisateurs à une conservation à l'aide du script de cet article. 
    
- Veillez à enregistrer la liste des utilisateurs que vous créez à l'étape 2 et le script de l'étape 3 dans le même dossier. Cela facilitera l'exécution du script.
    
- Le script ajoute la liste des utilisateurs à une nouvelle conservation associée à un cas existant. Assurez-vous que le cas où vous souhaitez associer le blocage est créé avant d'exécuter le script.
    
- Le script inclut une gestion des erreurs minimale. Son objectif principal est de placer rapidement et facilement la boîte aux lettres et le site OneDrive entreprise de chaque utilisateur en conservation.
    
- Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Étape 1 : installer SharePoint Online Management Shell

La première étape consiste à installer SharePoint Online Management Shell s'il n'est pas déjà installé sur votre ordinateur local. Vous n'avez pas besoin d'utiliser l'environnement de commande Exchange Management Shell dans cette procédure, mais vous devez l'installer car il contient les conditions préalables requises par le script exécuté à l'étape 3. Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive entreprise.
  
Accédez à [la configuration de l'environnement Windows PowerShell de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuez les étapes 1 et 2 pour installer SharePoint Online Management Shell sur votre ordinateur local. 

## <a name="step-2-generate-a-list-of-users"></a>Étape 2: générer une liste d'utilisateurs
<a name="step2"> </a>

Le script de l'étape 3 crée une conservation associée à un cas de découverte électronique, ainsi que les sites ajouter les boîtes aux lettres et OneDrive entreprise d'une liste d'utilisateurs à la suspension. Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir la liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier dans lequel vous enregistrerez le script à l'étape 3).
  
Voici une commande PowerShell (que vous exécutez à l'aide de PowerShell distant connecté à votre organisation Exchange Online) pour obtenir une liste d'adresses de messagerie pour tous les utilisateurs de votre organisation et l'enregistrer dans un fichier texte nommé HoldUsers. txt.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

Après avoir exécuté cette commande, ouvrez le fichier texte et supprimez l'en-tête qui contient le `PrimarySmtpAddress`nom de la propriété,. Ensuite, supprimez toutes les adresses de messagerie sauf celles des utilisateurs que vous souhaitez ajouter à la suspension que vous allez créer à l'étape 3. Assurez-vous qu'il n'y a pas de ligne vide avant ou après la liste des adresses de messagerie.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Étape 3: exécuter le script pour créer une conservation et ajouter des utilisateurs
<a name="step3"> </a>

Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes. Assurez-vous que vous disposez de ces informations avant d'exécuter le script.
  
- **Vos informations d'identification utilisateur** : le script utilisera vos informations d'identification pour se connecter &amp; au centre de sécurité conformité avec PowerShell à distance. Il utilisera également ces informations d'identification pour accéder à SharePoint Online afin d'obtenir les URL OneDrive entreprise pour la liste des utilisateurs.
    
- **Nom de votre domaine mon** site: le domaine mon site est celui qui contient tous les sites OneDrive entreprise de votre organisation. Par exemple, si l'URL de votre domaine mon site **https://contoso-my.sharepoint.com**mon site est, entrez `contoso` alors lorsque le script vous invite à indiquer le nom de votre domaine mon site. 
    
- **Nom de la casse** : nom d'un incident existant. Le script crée une nouvelle conservation qui est associée à ce cas.
    
- **Nom du blocage** : nom du blocage que le script crée et associe à la casse spécifiée.
    
- **Requête de recherche pour une conservation basée sur une requête** : vous pouvez créer une conservation basée sur une requête de sorte que seul le contenu correspondant aux critères de recherche spécifiés soit placé en conservation. Pour placer tout le contenu en conservation, appuyez simplement sur **entrée** lorsque vous êtes invité à entrer une requête de recherche. 
    
- **Indique si le blocage doit** être activé: vous pouvez faire en sorte que le script désactive le blocage une fois qu'il a été créé ou que le script peut créer la conservation sans l'activer. Si le script n'est pas activé, vous pouvez l'activer ultérieurement dans le centre de sécurité &amp; conformité ou en exécutant les commandes PowerShell suivantes: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **Nom du fichier texte avec la liste d'utilisateurs** : le nom du fichier texte de l'étape 2 qui contient la liste des utilisateurs à ajouter à la suspension. Si ce fichier se trouve dans le même dossier que le script, il vous suffit de taper le nom du fichier (par exemple, HoldUsers. txt). Si le fichier texte se trouve dans un autre dossier, tapez le chemin d'accès complet du fichier.
    
Une fois que vous avez collecté les informations que le script vous demande, la dernière étape consiste à exécuter le script pour créer la nouvelle conservation et y ajouter des utilisateurs.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `AddUsersToHold.ps1`.
    
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
    
3. Exécutez le script; par exemple:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Entrez les informations que le script vous demande.
    
    Le script se connecte au centre de sécurité & Compliance Center PowerShell, puis crée la nouvelle conservation dans le cas de découverte électronique et ajoute les boîtes aux lettres et OneDrive entreprise pour les utilisateurs de la liste. Vous pouvez accéder à l'incident sur la page **eDiscovery** dans le centre &amp; de sécurité conformité pour afficher la nouvelle conservation. 
    
Une fois l'exécution du script terminée, les fichiers journaux suivants sont créés et enregistrés dans le dossier où se trouve le script.
  
- **LocationsOnHold. txt** : contient la liste des boîtes aux lettres et des sites OneDrive entreprise que le script a mis en attente.
    
- **LocationsNotOnHold. txt** : contient la liste des boîtes aux lettres et des sites OneDrive entreprise que le script n'a pas suspendu. Si un utilisateur dispose d'une boîte aux lettres, mais pas d'un site OneDrive entreprise, l'utilisateur est inclus dans la liste des sites OneDrive entreprise qui n'ont pas été mis en attente.
    
- **GetCaseHoldPolicy. txt** -contient la sortie de la cmdlet **Get-CaseHoldPolicy** pour le nouveau blocage, que le script a exécuté après avoir créé la nouvelle conservation. Les informations renvoyées par cette cmdlet incluent une liste d'utilisateurs dont les boîtes aux lettres et les sites OneDrive entreprise ont été mis en attente et indique si la conservation est activée ou désactivée. 
    
- **GetCaseHoldRule. txt** -contient la sortie de la cmdlet **Get-CaseHoldRule** pour le nouveau blocage, que le script a exécuté après avoir créé la nouvelle conservation. Les informations renvoyées par cette cmdlet incluent la requête de recherche si vous avez utilisé le script pour créer une conservation basée sur une requête. 
