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
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Recherche de contenu permet de rechercher les boîtes aux lettres et OneDrive pour le site de l’entreprise pour une liste d’utilisateurs

L’Office 365 Security &amp; centre de conformité fournit un certain nombre de cmdlets Windows PowerShell qui vous permettent d’automatiser des tâches liées à la découverte du temps. Actuellement, création d’une recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher un grand nombre d’emplacements de contenu dépositaire prend la préparation et du temps. Avant de créer une recherche, vous devez recueillir l’URL pour chaque site Business OneDrive, puis ajoutez chaque boîte aux lettres et O neDrive pour le site de l’entreprise pour la recherche. Dans les futures versions précédentes, il sera plus facile de la sécurité &amp; centre de conformité. En attendant, vous pouvez utiliser le script dans cet article pour automatiser ce processus. Ce script vous invite à fournir le nom de domaine du site Mon site dans votre organisation (par exemple, **contoso** dans l’URL https://contoso-my.sharepoint.com), répond à une liste de messages, le nom de la recherche de contenu nouveau et la requête de recherche à utiliser. Le script obtient OneDrive pour l’URL de l’entreprise pour chaque utilisateur dans la liste, puis crée et démarre une recherche de contenu qui recherche dans la boîte aux lettres et OneDrive pour le site de l’entreprise pour chaque utilisateur dans la liste, à l’aide de la requête de recherche que vous fournissez. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité et un administrateur global de SharePoint Online pour exécuter le script à l’étape 3.
    
- Veillez à enregistrer la liste des utilisateurs que vous créez dans l’étape 2 et le script à l’étape 3 dans le même dossier. Qui facilitera exécuter le script.
    
- Le script inclut la gestion des erreurs minimale. Son objectif principal consiste à rechercher rapidement et facilement la boîte aux lettres et OneDrive pour le site de l’entreprise de chaque utilisateur.
    
- Les exemples de scripts fournis dans cette rubrique ne sont pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. Les exemples de scripts sont fournis en l’état sans aucune garantie. Microsoft exclut toutes les i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)garanties implicites, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et les exemples de scripts. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Étape 1 : installer SharePoint Online Management Shell
<a name="step1"> </a>

La première étape consiste à installer SharePoint Online Management Shell. Vous n’êtes pas obligé d’utiliser le shell de cette procédure, mais vous devez l’installer, car il contient les conditions préalables requises par le script que vous exécutez l’étape 3. Ces conditions préalables autoriser le script communiquer avec SharePoint Online pour obtenir l’URL pour OneDrive pour les sites.
  
Accédez à [configurer l’environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuer l’étape 1 et l’étape 2 pour installer SharePoint Online Management Shell.
  
## <a name="step-2-generate-a-list-of-users"></a>Étape 2 : Générer une liste d’utilisateurs
<a name="step2"> </a>

Le script à l’étape 3 crée une recherche de contenu pour rechercher les boîtes aux lettres et les comptes de OneDrive pour une liste d’utilisateurs. Vous pouvez taper les adresses de messagerie dans un fichier texte, ou vous pouvez exécuter une commande de Windows PowerShell pour obtenir une liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier que vous allez enregistrer le script à l’étape 3).
  
Voici une commande [d’Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) que vous pouvez afficher pour obtenir une liste des adresses de messagerie pour tous les utilisateurs de votre organisation et enregistrez-le dans un fichier texte nommé `Users.txt`. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

Après avoir exécuté cette commande, veillez à ouvrir le fichier et supprimer l’en-tête qui contient le nom de la propriété `PrimarySmtpAddress`. Le fichier texte doit contenir uniquement une liste d’adresses de messagerie et rien d’autre. Assurez-vous qu’il n’y aucune ligne vide avant ou après la liste des adresses de messagerie.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Étape 3 : Exécuter le script pour créer et lancer la recherche

Lorsque vous exécutez le script dans cette étape, il vous invite à vous pour obtenir les informations suivantes. Veillez à préparer les informations suivantes avant d’exécuter le script.
  
- **Vos informations d’identification utilisateur** - le script utilisera vos informations d’identification pour accéder à SharePoint Online pour obtenir le OneDrive pour les URL de l’entreprise et se connecter à la sécurité &amp; centre de conformité avec PowerShell à distance. 
    
- **Nom de votre domaine monsite** - monsite le domaine est le domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation. Par exemple, si l’URL de votre domaine monsite est **https://contoso-my.sharepoint.com**, puis entrez `contoso` lorsque le script vous demande le nom de votre domaine monsite. 
    
- **Chemin d’accès du fichier texte à l’étape 2** : le chemin d’accès du fichier texte que vous avez créé à l’étape 2. Si le fichier texte et le script se trouvent dans le même dossier, puis entrez le nom du fichier texte. Sinon, entrez le chemin complet du fichier texte. 
    
- **Nom de la recherche de contenu** : le nom de la recherche de contenu seront créées par le script. 
    
- **Requête de recherche** - la requête de recherche qui sera utilisée avec la recherche de contenu est créé et exécuté. Pour plus d’informations sur les requêtes de recherche, voir [conditions de recherche pour la recherche de contenu et les requêtes de mot clé](keyword-queries-and-search-conditions.md).


**Pour exécuter le script :**
    
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `SearchEXOOD4B.ps1`. Enregistrez le fichier dans le même dossier où vous avez enregistré la liste des utilisateurs à l’étape 2.
    
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

2. Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script et la liste des utilisateurs à l’étape 2.
    
3. Démarrez le script ; par exemple :
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**. 
    
5. Entrez les informations lorsque vous y êtes invité par le script suivantes. Tapez chaque élément d’information, puis appuyez sur **entrée**.
    
    - Le nom de votre domaine monsite. 
    
    - Le chemin d’accès du fichier texte qui contient la liste des utilisateurs.
    
    - Un nom pour la recherche de contenu.
    
    - La requête de recherche (laissez ce vide pour renvoyer tous les éléments dans les emplacements de contenu).
    
    Le script obtient l’URL pour chaque site de l’entreprise OneDrive et crée et démarre la recherche. Vous pouvez soit exécuter l’applet de commande **Get-ComplianceSearch** dans PowerShell du centre de conformité et de sécurité pour afficher les résultats et les statistiques de la recherche, ou vous pouvez accéder à la page de **recherche de contenu** de la sécurité &amp; centre de conformité pour afficher plus d’informations sur la recherche. 
