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
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="7d2ba-103">Utiliser un script pour ajouter des utilisateurs à une suspension dans un cas de découverte électronique de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="7d2ba-103">Use a script to add users to a hold in an eDiscovery case in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="7d2ba-p101">L’Office 365 Security &amp; centre de conformité fournit beaucoup des applets de commande Windows PowerShell qui vous permettent d’automatiser les tâches longues liées à la création et la gestion des cas eDiscovery. Actuellement, à l’aide de l’outil cas eDiscovery dans la sécurité &amp; centre de conformité pour placer un grand nombre d’emplacements de contenu dépositaire en attente prend la préparation et du temps. Par exemple, avant de créer une suspension, vous devez recueillir l’URL pour chaque site d’entreprise que vous souhaitez mettre en attente OneDrive. Puis pour chaque utilisateur que vous souhaitez mettre en attente, vous devez ajouter leur boîte aux lettres et leur site Business OneDrive à la suspension. Dans les futures versions de la sécurité &amp; centre de conformité, cela obtiendra plus facile à faire. En attendant, vous pouvez utiliser le script dans cet article pour automatiser ce processus.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p101">The Office 365 Security &amp; Compliance Center provides lots of Windows PowerShell cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases. Currently, using the eDiscovery case tool in the Security &amp; Compliance Center to place a large number of custodian content locations on hold takes time and preparation. For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold. Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold. In future releases of the Security &amp; Compliance Center, this will get easier to do. Until then, you can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="7d2ba-p102">Le script vous invite à fournir le nom de domaine du site Mon site dans votre organisation (par exemple, **contoso** dans l’URL https://contoso-my.sharepoint.com), le nom d’un cas de découverte électronique existant, le nom de la nouvelle mise en attente qui associés au cas, une liste d’adresses de messagerie des utilisateurs que vous souhaitez Pour mettre en attente et une requête de recherche à utiliser si vous souhaitez créer une suspension basée sur une requête. Le script obtient ensuite l’URL pour le site de l’entreprise pour chaque utilisateur dans la liste OneDrive, crée la suspension de nouveau, puis ajoute la boîte aux lettres et OneDrive pour le site de l’entreprise pour chaque utilisateur dans la liste à la suspension. Le script génère également des fichiers journaux qui contiennent des informations sur la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p102">The script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold. The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold. The script also generates log files that contain information about the new hold.</span></span> 
  
<span data-ttu-id="7d2ba-113">Voici comment procéder :</span><span class="sxs-lookup"><span data-stu-id="7d2ba-113">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="7d2ba-114">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="7d2ba-114">Step 1: Install the SharePoint Online Management Shell</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[<span data-ttu-id="7d2ba-115">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7d2ba-115">Step 2: Generate a list of users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[<span data-ttu-id="7d2ba-116">Étape 3 : Exécuter le script pour créer une suspension et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7d2ba-116">Step 3: Run the script to create a hold and add users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a><span data-ttu-id="7d2ba-117">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7d2ba-117">Before you begin</span></span>

- <span data-ttu-id="7d2ba-p103">Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité et un administrateur global de SharePoint Online pour exécuter le script à l’étape 3. Pour plus d’informations, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="7d2ba-p104">Un maximum de 1 000 boîtes aux lettres et 100 sites peut être ajouté à une suspension associé à un cas de découverte électronique dans la sécurité &amp; centre de conformité. En supposant que tous les utilisateurs que vous souhaitez mettre en attente a un OneDrive pour le site de l’entreprise, vous pouvez ajouter un maximum de 100 utilisateurs à une suspension à l’aide du script dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p104">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security &amp; Compliance Center. Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span> 
    
- <span data-ttu-id="7d2ba-p105">Veillez à enregistrer la liste des utilisateurs que vous créez dans l’étape 2 et le script à l’étape 3 dans le même dossier. Qui facilitera exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p105">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="7d2ba-p106">Le script ajoute la liste des utilisateurs à une suspension nouveau qui est associée à un cas existant. N’oubliez pas que vous souhaitez associer la suspension avec création avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p106">The script adds the list of users to a new hold that is associated with an existing case. Be sure the case that you want to associate the hold with is created before you run the script.</span></span>
    
- <span data-ttu-id="7d2ba-p107">Le script inclut la gestion des erreurs minimale. Son objectif principal est rapidement et facilement placer la boîte aux lettres et OneDrive pour le site d’entreprise de chaque utilisateur de blocage.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p107">The script includes minimal error handling. Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>
    
- <span data-ttu-id="7d2ba-p108">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p108">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="7d2ba-133">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="7d2ba-133">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="7d2ba-p109">La première étape consiste à installer SharePoint Online Management Shell s’il n’est pas déjà installé sur votre ordinateur local. Vous n’êtes pas obligé d’utiliser le shell de cette procédure, mais vous devez l’installer, car il contient les conditions préalables requises par le script que vous exécutez l’étape 3. Ces conditions préalables autoriser le script communiquer avec SharePoint Online pour obtenir l’URL pour OneDrive pour les sites.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p109">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="7d2ba-137">Accédez à [configurer l’environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuer l’étape 1 et l’étape 2 pour installer SharePoint Online Management Shell sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-137">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span> 

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="7d2ba-138">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7d2ba-138">Step 2: Generate a list of users</span></span>
<span data-ttu-id="7d2ba-139"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="7d2ba-139"></span></span>

<span data-ttu-id="7d2ba-p110">Le script à l’étape 3 crée une suspension associé à un cas eDiscovery et ajoutez les boîtes aux lettres et OneDrive pour les sites d’entreprise d’une liste d’utilisateurs à la suspension. Vous pouvez taper les adresses de messagerie dans un fichier texte, ou vous pouvez exécuter une commande de Windows PowerShell pour obtenir une liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier que vous allez enregistrer le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p110">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="7d2ba-142">Voici une commande PowerShell (que vous exécutez à l’aide de PowerShell à distance connecté à votre organisation Exchange Online) pour obtenir une liste des adresses de messagerie pour tous les utilisateurs de votre organisation et enregistrez-le dans un fichier texte nommé HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-142">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="7d2ba-p111">Une fois que vous exécutez cette commande, ouvrez le fichier texte et supprimez l’en-tête qui contient le nom de la propriété `PrimarySmtpAddress`. Supprimez toutes les adresses de messagerie à l’exception de celles pour les utilisateurs que vous souhaitez ajouter à la suspension que vous créerez à l’étape 3. Assurez-vous qu’il n’y aucune ligne vide avant ou après la liste des adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p111">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`. Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="7d2ba-146">Étape 3 : Exécuter le script pour créer une suspension et ajouter des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7d2ba-146">Step 3: Run the script to create a hold and add users</span></span>
<span data-ttu-id="7d2ba-147"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="7d2ba-147"></span></span>

<span data-ttu-id="7d2ba-p112">Lorsque vous exécutez le script dans cette étape, il vous invite à vous pour obtenir les informations suivantes. Veillez à préparer les informations suivantes avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p112">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="7d2ba-p113">**Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à la sécurité &amp; centre de conformité avec PowerShell à distance. Il utilise également ces informations d’identification pour accéder à SharePoint Online pour obtenir le OneDrive pour les URL de l’entreprise pour la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p113">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center with remote PowerShell. It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>
    
- <span data-ttu-id="7d2ba-p114">**Nom de votre domaine monsite** - monsite le domaine est le domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation. Par exemple, si l’URL de votre domaine monsite est **https://contoso-my.sharepoint.com**, puis entrez `contoso` lorsque le script vous demande le nom de votre domaine monsite.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p114">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="7d2ba-p115">**Nom du dossier** - le nom d’un cas existant. Le script crée une nouvelle suspension qui est associée à ce cas.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p115">**Name of the case** - The name of an existing case. The script will create a new hold that is associated with this case.</span></span>
    
- <span data-ttu-id="7d2ba-156">**Nom de la suspension** - le nom de la suspension, le script crée et associer la casse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-156">**Name of the hold** - The name of the hold the script will create and associate with the specified case.</span></span>
    
- <span data-ttu-id="7d2ba-p116">**Blocage de requête de recherche pour basée sur une requête** - vous pouvez créer une suspension basée sur une requête afin qu’uniquement le contenu qui répond aux critères de recherche est mis en attente. Pour placer tous les contenus en attente, appuyez sur **entrée** lorsque vous êtes invité à une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p116">**Search query for a query-based hold** - You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold. To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span> 
    
- <span data-ttu-id="7d2ba-p117">**S’il faut activer la suspension** - le script peut être activer la suspension après sa création ou le script peut être créer la suspension sans l’activer. Si vous n’avez pas le script activer la mise en attente, vous pouvez l’activer ultérieurement dans la sécurité &amp; centre de conformité ou en exécutant les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p117">**Whether or not to turn the hold on** - You can have the script turn the hold on after it's created or you can have the script create the hold without enabling it. If you don't have the script turn on the hold, you can turn it on later in the Security &amp; Compliance Center or by running the following PowerShell commands:</span></span> 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="7d2ba-p118">**Nom du fichier texte avec la liste des utilisateurs** : le nom du fichier texte à l’étape 2 qui contient la liste des utilisateurs à ajouter à la suspension. Si ce fichier se trouve dans le même dossier que le script, il suffit de taper le nom du fichier (par exemple, HoldUsers.txt). Si le fichier texte est dans un autre dossier, tapez le chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p118">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold. If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt). If the text file is in another folder, type the full pathname of the file.</span></span>
    
<span data-ttu-id="7d2ba-164">Une fois que vous avez collecté les informations qui vous invite à vous pour le script, l’étape finale consiste à exécuter le script pour créer la nouvelle suspension et ajouter des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-164">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="7d2ba-165">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `AddUsersToHold.ps1`.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-165">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `AddUsersToHold.ps1`.</span></span>
    
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

2. <span data-ttu-id="7d2ba-166">Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-166">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="7d2ba-167">Exécuter le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="7d2ba-167">Run the script; for example:</span></span>
    
      ```
    .\AddUsersToHold.ps1
      ```

4. <span data-ttu-id="7d2ba-168">Entrez les informations qui vous demande le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-168">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="7d2ba-p119">Le script se connecte à la sécurité et conformité centre PowerShell, puis crée la suspension de nouveau dans le cas de découverte électronique et ajoute les boîtes aux lettres et OneDrive entreprise pour les utilisateurs de la liste. Vous pouvez accéder à la casse dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité pour afficher la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p119">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list. You can go to the case on the **eDiscovery** page in the Security &amp; Compliance Center to view the new hold.</span></span> 
    
<span data-ttu-id="7d2ba-171">Une fois que le script est terminé en cours d’exécution, il crée les fichiers journaux suivants et les enregistre dans le dossier où se trouve le script.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-171">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="7d2ba-172">**LocationsOnHold.txt** - contient une liste des boîtes aux lettres et OneDrive pour les sites entreprise le script correctement mis en attente.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-172">**LocationsOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>
    
- <span data-ttu-id="7d2ba-p120">**LocationsNotOnHold.txt** - contient une liste des boîtes aux lettres et OneDrive pour les sites d’entreprise qui le script ne pas mettre en attente. Si l’utilisateur a une boîte aux lettres, mais pas OneDrive site de l’entreprise, l’utilisateur doit être inclus dans la liste de OneDrive pour les sites d’entreprise qui n’ont pas été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p120">**LocationsNotOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold. If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>
    
- <span data-ttu-id="7d2ba-p121">**GetCaseHoldPolicy.txt** - contient le résultat de l’applet de commande **Get-CaseHoldPolicy** pour la nouvelle suspension, le script s’est exécuté après la création de la nouvelle mise en attente. Les informations renvoyées par cette applet de commande comprend une liste d’utilisateurs dont les boîtes aux lettres et OneDrive pour les sites ont été mis en attente et si la suspension est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p121">**GetCaseHoldPolicy.txt** - Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 
    
- <span data-ttu-id="7d2ba-p122">**GetCaseHoldRule.txt** - contient le résultat de l’applet de commande **Get-CaseHoldRule** pour la nouvelle suspension, le script s’est exécuté après la création de la nouvelle mise en attente. Les informations renvoyées par cette applet de commande incluent la requête de recherche si vous avez utilisé le script pour créer une suspension basée sur une requête.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-p122">**GetCaseHoldRule.txt** - Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span> 
