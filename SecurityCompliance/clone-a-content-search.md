---
title: Cloner une recherche de contenu de la sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante dans la sécurité &amp; recherche Compliane centre. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nouveau nom) est créée qui contient les propriétés de même que la recherche d’origine. Vous pouvez modifier la nouvelle recherche (en modifiant la requête de mot clé ou la plage de dates) et exécutez-le.
ms.openlocfilehash: a4f801e3de281e8caf8aeb7d1c2bd48f0facb77c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527974"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Cloner une recherche de contenu de la sécurité Office 365 &amp; centre de conformité

Création d’une recherche de contenu de la sécurité Office 365 &amp; centre de conformité qui recherche un grand nombre de boîtes aux lettres ou SharePoint et OneDrive pour les sites de l’entreprise peuvent prendre un certain temps. Spécification des sites pour la recherche peut également être sujet aux erreurs si vous tapez une URL. Pour éviter ces problèmes, vous pouvez utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nom différent) est créée qui contient les mêmes propriétés (tels que les emplacements de contenu et la requête de recherche) que la recherche d’origine. Vous pouvez modifier la nouvelle recherche (en modifiant la requête de mot clé ou la plage de dates) et exécutez-le.
  
Pourquoi cloner les recherches de contenu ?
  
- Pour comparer les résultats de mot clé différente requêtes de recherche s’exécuter sur les mêmes emplacements de contenu.
    
- Pour vous éviter d’avoir à saisir un grand nombre d’emplacements de contenu lorsque vous créez une nouvelle recherche.
    
- Pour réduire la taille des résultats de recherche ; par exemple, si vous avez une recherche qui retourne trop de résultats à exporter, vous pourrez cloner la recherche et puis ajouter une condition de recherche basée sur une plage de dates pour réduire le nombre de résultats de recherche.
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script décrit dans cette rubrique.
    
- Le script inclut la gestion des erreurs minimale. Le principal objectif du script consiste à cloner rapidement une recherche de contenu.
    
- Le script crée une nouvelle recherche de contenu, mais ne démarre pas.
    
- Ce script prend en compte si la recherche de contenu que vous dupliquez est associée à une affaire eDiscovery. Si la recherche est associée à un cas, la nouvelle recherche seront également associée à la casse. Si la recherche existante n’est pas associée à un cas, la nouvelle recherche apparaît dans la page de **recherche de contenu** dans la sécurité &amp; centre de conformité. 
    
- L’exemple de script fourni dans cette rubrique n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>Étape 1 : Exécutez le script pour cloner une recherche

Le script dans cette étape crée une nouvelle recherche de contenu en clonant une existante. Lorsque vous exécutez ce script, vous serez invité pour obtenir les informations suivantes :
  
- **Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à la sécurité &amp; centre de conformité pour votre organisation Office 365 avec Windows PowerShell. Comme indiqué plus haut, vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script. 
    
- **Le nom de la recherche existant** : il s’agit de la recherche de contenu que vous souhaitez cloner. 
    
- **Le nom de la nouvelle recherche qui sera créé** - si vous laissez cette valeur vide, le script crée un nom pour la nouvelle recherche basée sur le nom de la recherche que vous dupliquez. 
    
Pour cloner une recherche :
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `CloneSearch.ps1`.
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.
    
3. Exécuter le script ; par exemple :
    
    ```
    .\CloneSearch.ps1
    ```

4. Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.
    
5. Entrez les informations lorsque vous y êtes invité par le script suivantes. Tapez chaque élément d’information, puis appuyez sur **entrée**.
    
    - Le nom de la recherche existante.
    
    - Le nom de la nouvelle recherche.
    
    Le script crée le nouveau contenu de recherche, mais ne démarre pas. Cela vous donne la possibilité de modifier et d’exécuter la recherche à l’étape suivante. Vous pouvez afficher les propriétés de la nouvelle recherche en exécutant l’applet de commande **Get-ComplianceSearch** ou en accédant à la page de **recherche de contenu** ou de **découverte** de la sécurité &amp; centre de conformité, en fonction de la nouvelle recherche est-il associé à un cas. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a>Étape 2 : Modifier et exécuter la recherche clonée dans la sécurité &amp; centre de conformité

Après l’avoir exécuté le script pour cloner une recherche de contenu existante, l’étape suivante consiste pour accéder à la sécurité &amp; centre de conformité pour modifier et exécuter la recherche. Comme indiqué plus haut, vous pouvez modifier une recherche en modifiant la requête de recherche de mot clé et en ajoutant ou supprimant des conditions de recherche. Pour plus d’informations, voir :
  
- [Recherche de contenu dans Office 365](content-search.md)
    
- [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md)
    
- [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md)
