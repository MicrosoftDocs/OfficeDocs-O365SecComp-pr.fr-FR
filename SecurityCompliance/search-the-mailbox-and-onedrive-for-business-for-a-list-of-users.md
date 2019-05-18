---
title: Utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et OneDrive Entreprise
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Utilisez la recherche de contenu et le script dans cet article pour effectuer des recherches dans les boîtes aux lettres et les sites OneDrive entreprise pour un groupe d’utilisateurs.
ms.openlocfilehash: 7be1494f7a69c5865974a6c4ee0be65a6acb49d4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158766"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Utiliser la recherche de contenu pour rechercher une liste d’utilisateurs dans la boîte aux lettres et OneDrive Entreprise

Le centre de sécurité & Compliance Center fournit un certain nombre d’applets de commande Windows PowerShell qui vous permettent d’automatiser des tâches de découverte électronique fastidieuses. Actuellement, la création d’une recherche de contenu dans le centre de sécurité & Compliance Center pour rechercher un grand nombre d’emplacements de contenu de dépositaire nécessite du temps et une préparation. Avant de créer une recherche, vous devez collecter l’URL de chaque site OneDrive entreprise, puis ajouter chaque boîte aux lettres et le site O neDrive for Business à la recherche. Dans les prochaines versions, cette opération sera plus facile à réaliser dans le centre de sécurité & Compliance Center. En attendant, vous pouvez utiliser le script de cet article pour automatiser ce processus. Ce script vous invite à indiquer le nom du domaine mon site de votre organisation (par exemple, **contoso** dans l' https://contoso-my.sharepoint.com)URL, une liste des adresses de messagerie des utilisateurs, le nom de la nouvelle recherche de contenu et la requête de recherche à utiliser. Le script obtient l’URL de OneDrive entreprise pour chaque utilisateur dans la liste, puis il crée et démarre une recherche de contenu qui recherche dans la boîte aux lettres et le site OneDrive entreprise pour chaque utilisateur de la liste, à l’aide de la requête de recherche que vous fournissez. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité & Compliance Center et d’un administrateur global SharePoint Online pour exécuter le script à l’étape 3.
    
- Veillez à enregistrer la liste des utilisateurs que vous créez à l’étape 2 et le script de l’étape 3 dans le même dossier. Cela facilitera l’exécution du script.
    
- Le script inclut une gestion des erreurs minimale. Son objectif principal est de rechercher rapidement et facilement la boîte aux lettres et le site OneDrive entreprise de chaque utilisateur.
    
- Les exemples de scripts fournis dans cette rubrique ne sont pas pris en charge dans n’importe quel programme ou service de support standard Microsoft. Les exemples de scripts sont fournis en l'état, sans garantie d'aucune sorte. Microsoft exclut encore toutes les garanties[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied, y compris, sans limitation, toute garantie implicite de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l'utilisation ou à l'exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d'activité, perte d'informations commerciales ou toute autre perte pécuniaire) découlant de l'utilisation ou de l'impossibilité d'utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Étape 1 : installer SharePoint Online Management Shell
<a name="step1"> </a>

La première étape consiste à installer SharePoint Online Management Shell. Vous n’avez pas besoin d’utiliser l’environnement de commande Exchange Management Shell dans cette procédure, mais vous devez l’installer car il contient les conditions préalables requises par le script exécuté à l’étape 3. Ces conditions préalables permettent au script de communiquer avec SharePoint Online pour obtenir les URL des sites OneDrive entreprise.
  
Accédez à [la configuration de l’environnement Windows PowerShell de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkID=286318) et effectuez les étapes 1 et 2 pour installer SharePoint Online Management Shell.
  
## <a name="step-2-generate-a-list-of-users"></a>Étape 2: générer une liste d’utilisateurs
<a name="step2"> </a>

Le script de l’étape 3 crée une recherche de contenu pour rechercher dans les boîtes aux lettres et les comptes OneDrive une liste d’utilisateurs. Vous pouvez simplement taper les adresses de messagerie dans un fichier texte ou exécuter une commande dans Windows PowerShell pour obtenir la liste des adresses de messagerie et les enregistrer dans un fichier (situé dans le même dossier dans lequel vous enregistrerez le script à l’étape 3).
  
Voici une commande [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) que vous pouvez Runt pour obtenir une liste d’adresses de messagerie pour tous les utilisateurs de votre organisation et l’enregistrer dans un fichier texte `Users.txt`nommé. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

Après avoir exécuté cette commande, veillez à ouvrir le fichier et à supprimer l’en-tête qui contient le `PrimarySmtpAddress`nom de la propriété,. Le fichier texte doit contenir uniquement une liste d’adresses de messagerie et rien d’autre. Assurez-vous qu’il n’y a pas de ligne vide avant ou après la liste des adresses de messagerie.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Étape 3: exécuter le script pour créer et démarrer la recherche

Lorsque vous exécutez le script dans cette étape, il vous invite à fournir les informations suivantes. Assurez-vous que vous disposez de ces informations avant d’exécuter le script.
  
- **Vos informations d’identification utilisateur** : le script utilisera vos informations d’identification pour accéder à SharePoint Online afin d’obtenir les URL OneDrive entreprise et se connecter au centre de sécurité _AMP_ Compliance Center avec PowerShell à distance. 
    
- **Nom de votre domaine mon** site: le domaine mon site est celui qui contient tous les sites OneDrive entreprise de votre organisation. Par exemple, si l’URL de votre domaine mon site **https://contoso-my.sharepoint.com**mon site est, entrez `contoso` alors lorsque le script vous invite à indiquer le nom de votre domaine mon site. 
    
- **Chemin d’accès du fichier texte à partir de l’étape 2** : le nom de chemin du fichier texte que vous avez créé à l’étape 2. Si le fichier texte et le script se trouvent dans le même dossier, entrez le nom du fichier texte. Dans le cas contraire, entrez le chemin d’accès complet au fichier texte. 
    
- **Nom de la recherche de contenu** : nom de la recherche de contenu qui sera créée par le script. 
    
- **Requête de recherche** : la requête de recherche qui sera utilisée avec la recherche de contenu est créée et exécutée. Pour plus d’informations sur les requêtes de recherche, consultez la rubrique [requêtes de mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).


**Pour exécuter le script :**
    
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier. ps1; par exemple, `SearchEXOOD4B.ps1`. Enregistrez le fichier dans le dossier où vous avez enregistré la liste des utilisateurs à l’étape 2.
    
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

2. Ouvrez Windows PowerShell et accédez au dossier dans lequel vous avez enregistré le script et la liste des utilisateurs de l’étape 2.
    
3. Démarrez le script; par exemple:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Lorsque vous êtes invité à entrer vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**. 
    
5. Entrez les informations suivantes lorsque le script vous y invite. Tapez chaque information, puis appuyez sur **entrée**.
    
    - Nom de votre domaine mon site. 
    
    - Chemin d’accès du fichier texte qui contient la liste des utilisateurs.
    
    - Nom de la recherche de contenu.
    
    - La requête de recherche (laissez ce champ vide pour renvoyer tous les éléments dans les emplacements de contenu).
    
    Le script obtient les URL de chaque site OneDrive entreprise, puis crée et démarre la recherche. Vous pouvez exécuter la cmdlet **Get-ComplianceSearch** dans le centre de sécurité _AMP_ Compliance Center PowerShell pour afficher les statistiques et les résultats de la recherche, ou vous pouvez accéder à la page de **recherche de contenu** dans le centre de conformité de la sécurité & pour afficher des informations à propos de la recherche. 
