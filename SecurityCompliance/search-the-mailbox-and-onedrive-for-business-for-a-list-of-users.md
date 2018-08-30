---
title: Recherche de contenu permet de rechercher les boîtes aux lettres et OneDrive pour le site de l’entreprise pour une liste d’utilisateurs
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Utilisez la recherche de contenu et le script dans cet article pour rechercher les boîtes aux lettres et OneDrive pour les sites d’entreprise pour un groupe d’utilisateurs.
ms.openlocfilehash: cc88f8e81a9883b8d392965db14994691878748d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527959"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="27e26-103">Recherche de contenu permet de rechercher les boîtes aux lettres et OneDrive pour le site de l’entreprise pour une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="27e26-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="27e26-p101">L’Office 365 Security &amp; centre de conformité fournit un certain nombre de cmdlets Windows PowerShell qui vous permettent d’automatiser des tâches liées à la découverte du temps. Actuellement, création d’une recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher un grand nombre d’emplacements de contenu dépositaire prend la préparation et du temps. Avant de créer une recherche, vous devez recueillir l’URL pour chaque site Business OneDrive, puis ajoutez chaque boîte aux lettres et O neDrive pour le site de l’entreprise pour la recherche. Dans les futures versions précédentes, il sera plus facile de la sécurité &amp; centre de conformité. En attendant, vous pouvez utiliser le script dans cet article pour automatiser ce processus. Ce script vous invite à fournir le nom de domaine du site Mon site dans votre organisation (par exemple, **contoso** dans l’URL https://contoso-my.sharepoint.com), répond à une liste de messages, le nom de la recherche de contenu nouveau et la requête de recherche à utiliser. Le script obtient OneDrive pour l’URL de l’entreprise pour chaque utilisateur dans la liste, puis crée et démarre une recherche de contenu qui recherche dans la boîte aux lettres et OneDrive pour le site de l’entreprise pour chaque utilisateur dans la liste, à l’aide de la requête de recherche que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="27e26-p101">The Office 365 Security &amp; Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks. Currently, creating a Content Search in the Security &amp; Compliance Center to search a large number of custodian content locations takes time and preparation. Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and O neDrive for Business site to the search. In future releases, this will be easier to do in the Security &amp; Compliance Center. Until then, you can use the script in this article to automate this process. This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), a list of user email addresses, the name of the new Content Search, and the search query to use. The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="27e26-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="27e26-111">Before you begin</span></span>

- <span data-ttu-id="27e26-112">Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité et un administrateur global de SharePoint Online pour exécuter le script à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="27e26-112">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>
    
- <span data-ttu-id="27e26-p102">Veillez à enregistrer la liste des utilisateurs que vous créez dans l’étape 2 et le script à l’étape 3 dans le même dossier. Qui facilitera exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="27e26-p102">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="27e26-p103">Le script inclut la gestion des erreurs minimale. Son objectif principal consiste à rechercher rapidement et facilement la boîte aux lettres et OneDrive pour le site de l’entreprise de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27e26-p103">The script includes minimal error handling. It's primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>
    
- <span data-ttu-id="27e26-p104">Les exemples de scripts fournis dans cette rubrique ne sont pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. Les exemples de scripts sont fournis en l’état sans aucune garantie. Microsoft exclut toutes les i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)garanties implicites, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et les exemples de scripts. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="27e26-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="27e26-122">Étape 1 : installer SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="27e26-122">Step 1: Install the SharePoint Online Management Shell</span></span>
<span data-ttu-id="27e26-123"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="27e26-123"></span></span>

<span data-ttu-id="27e26-p105">La première étape consiste à installer SharePoint Online Management Shell. Vous n’êtes pas obligé d’utiliser le shell de cette procédure, mais vous devez l’installer, car il contient les conditions préalables requises par le script que vous exécutez l’étape 3. Ces conditions préalables autoriser le script communiquer avec SharePoint Online pour obtenir l’URL pour OneDrive pour les sites.</span><span class="sxs-lookup"><span data-stu-id="27e26-p105">The first step is to install the SharePoint Online Management Shell. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="27e26-127">Accédez à [configurer l’environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuer l’étape 1 et l’étape 2 pour installer SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="27e26-127">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="27e26-128">Étape 2 : Générer une liste d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="27e26-128">Step 2: Generate a list of users</span></span>
<span data-ttu-id="27e26-129"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="27e26-129"></span></span>

<span data-ttu-id="27e26-p106">Le script à l’étape 3 crée une recherche de contenu pour rechercher les boîtes aux lettres et les comptes de OneDrive pour une liste d’utilisateurs. Vous pouvez taper les adresses de messagerie dans un fichier texte, ou vous pouvez exécuter une commande de Windows PowerShell pour obtenir une liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier que vous allez enregistrer le script à l’étape 3).</span><span class="sxs-lookup"><span data-stu-id="27e26-p106">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="27e26-132">Voici une commande [d’Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) que vous pouvez afficher pour obtenir une liste des adresses de messagerie pour tous les utilisateurs de votre organisation et enregistrez-le dans un fichier texte nommé `Users.txt`.</span><span class="sxs-lookup"><span data-stu-id="27e26-132">Here's an [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="27e26-p107">Après avoir exécuté cette commande, veillez à ouvrir le fichier et supprimer l’en-tête qui contient le nom de la propriété `PrimarySmtpAddress`. Le fichier texte doit contenir uniquement une liste d’adresses de messagerie et rien d’autre. Assurez-vous qu’il n’y aucune ligne vide avant ou après la liste des adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="27e26-p107">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`. The text file should just contain a list of email addresses, and nothing else. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="27e26-136">Étape 3 : Exécuter le script pour créer et lancer la recherche</span><span class="sxs-lookup"><span data-stu-id="27e26-136">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="27e26-p108">Lorsque vous exécutez le script dans cette étape, il vous invite à vous pour obtenir les informations suivantes. Veillez à préparer les informations suivantes avant d’exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="27e26-p108">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="27e26-139">**Vos informations d’identification utilisateur** - le script utilisera vos informations d’identification pour accéder à SharePoint Online pour obtenir le OneDrive pour les URL de l’entreprise et se connecter à la sécurité &amp; centre de conformité avec PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="27e26-139">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security &amp; Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="27e26-p109">**Nom de votre domaine monsite** - monsite le domaine est le domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation. Par exemple, si l’URL de votre domaine monsite est **https://contoso-my.sharepoint.com**, puis entrez `contoso` lorsque le script vous demande le nom de votre domaine monsite.</span><span class="sxs-lookup"><span data-stu-id="27e26-p109">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="27e26-p110">**Chemin d’accès du fichier texte à l’étape 2** : le chemin d’accès du fichier texte que vous avez créé à l’étape 2. Si le fichier texte et le script se trouvent dans le même dossier, puis entrez le nom du fichier texte. Sinon, entrez le chemin complet du fichier texte.</span><span class="sxs-lookup"><span data-stu-id="27e26-p110">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2. If the text file and the script are located in the same folder, then enter the name of the text file. Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="27e26-145">**Nom de la recherche de contenu** : le nom de la recherche de contenu seront créées par le script.</span><span class="sxs-lookup"><span data-stu-id="27e26-145">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="27e26-p111">**Requête de recherche** - la requête de recherche qui sera utilisée avec la recherche de contenu est créé et exécuté. Pour plus d’informations sur les requêtes de recherche, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="27e26-p111">**Search query** - The search query that will be used with the Content Search is created and run. For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="27e26-148">**Pour exécuter le script :**</span><span class="sxs-lookup"><span data-stu-id="27e26-148">**To run the script:**</span></span>
    
1. <span data-ttu-id="27e26-p112">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `SearchEXOOD4B.ps1`. Enregistrez le fichier dans le même dossier où vous avez enregistré la liste des utilisateurs à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="27e26-p112">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`. Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
  ```
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
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
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
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
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. <span data-ttu-id="27e26-151">Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script et la liste des utilisateurs à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="27e26-151">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="27e26-152">Démarrez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="27e26-152">Start the script; for example:</span></span>
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="27e26-153">Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="27e26-153">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="27e26-p113">Entrez les informations lorsque vous y êtes invité par le script suivantes. Tapez chaque élément d’information, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="27e26-p113">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="27e26-156">Le nom de votre domaine monsite.</span><span class="sxs-lookup"><span data-stu-id="27e26-156">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="27e26-157">Le chemin d’accès du fichier texte qui contient la liste des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="27e26-157">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="27e26-158">Un nom pour la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="27e26-158">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="27e26-159">La requête de recherche (laissez ce vide pour renvoyer tous les éléments dans les emplacements de contenu).</span><span class="sxs-lookup"><span data-stu-id="27e26-159">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="27e26-p114">Le script obtient l’URL pour chaque site de l’entreprise OneDrive et crée et démarre la recherche. Vous pouvez soit exécuter l’applet de commande **Get-ComplianceSearch** dans PowerShell du centre de conformité et de sécurité pour afficher les résultats et les statistiques de la recherche, ou vous pouvez accéder à la page de **recherche de contenu** de la sécurité &amp; centre de conformité pour afficher plus d’informations sur la recherche.</span><span class="sxs-lookup"><span data-stu-id="27e26-p114">The script gets the URLs for each OneDrive for Business site and then creates and starts the search. You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security &amp; Compliance Center to view information about the search.</span></span> 
