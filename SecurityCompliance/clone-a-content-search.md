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
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante dans la sécurité &amp; recherche Compliane centre. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nouveau nom) est créée qui contient les propriétés de même que la recherche d’origine. Vous pouvez modifier la nouvelle recherche (en modifiant la requête de mot clé ou la plage de dates) et exécutez-le.
ms.openlocfilehash: fd2ea0d8fa812d23e7479b664b13c786a62d5a38
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038047"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="5d3b8-105">Cloner une recherche de contenu de la sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="5d3b8-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="5d3b8-p102">Création d’une recherche de contenu de la sécurité Office 365 &amp; centre de conformité qui recherche un grand nombre de boîtes aux lettres ou SharePoint et OneDrive pour les sites de l’entreprise peuvent prendre un certain temps. Spécification des sites pour la recherche peut également être sujet aux erreurs si vous tapez une URL. Pour éviter ces problèmes, vous pouvez utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nom différent) est créée qui contient les mêmes propriétés (tels que les emplacements de contenu et la requête de recherche) que la recherche d’origine. Vous pouvez modifier la nouvelle recherche (en modifiant la requête de mot clé ou la plage de dates) et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="5d3b8-111">Pourquoi cloner les recherches de contenu ?</span><span class="sxs-lookup"><span data-stu-id="5d3b8-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="5d3b8-112">Pour comparer les résultats de mot clé différente requêtes de recherche s’exécuter sur les mêmes emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="5d3b8-113">Pour vous éviter d’avoir à saisir un grand nombre d’emplacements de contenu lorsque vous créez une nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="5d3b8-114">Pour réduire la taille des résultats de recherche ; par exemple, si vous avez une recherche qui retourne trop de résultats à exporter, vous pourrez cloner la recherche et puis ajouter une condition de recherche basée sur une plage de dates pour réduire le nombre de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="5d3b8-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5d3b8-115">Before you begin</span></span>

- <span data-ttu-id="5d3b8-116">Vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="5d3b8-p103">Le script inclut la gestion des erreurs minimale. Le principal objectif du script consiste à cloner rapidement une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="5d3b8-119">Le script crée une nouvelle recherche de contenu, mais ne démarre pas.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="5d3b8-p104">Ce script prend en compte si la recherche de contenu que vous dupliquez est associée à une affaire eDiscovery. Si la recherche est associée à un cas, la nouvelle recherche seront également associée à la casse. Si la recherche existante n’est pas associée à un cas, la nouvelle recherche apparaît dans la page de **recherche de contenu** dans la sécurité &amp; centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="5d3b8-p105">L’exemple de script fourni dans cette rubrique n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="5d3b8-128">Étape 1 : Exécutez le script pour cloner une recherche</span><span class="sxs-lookup"><span data-stu-id="5d3b8-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="5d3b8-p106">Le script dans cette étape crée une nouvelle recherche de contenu en clonant une existante. Lorsque vous exécutez ce script, vous serez invité pour obtenir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="5d3b8-p107">**Vos informations d’identification utilisateur** - le script utiliseront vos informations d’identification pour se connecter à la sécurité &amp; centre de conformité pour votre organisation Office 365 avec Windows PowerShell. Comme indiqué plus haut, vous devez être membre du groupe de rôles eDiscovery responsable de la sécurité &amp; centre de conformité pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="5d3b8-133">**Le nom de la recherche existant** : il s’agit de la recherche de contenu que vous souhaitez cloner.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="5d3b8-134">**Le nom de la nouvelle recherche qui sera créé** - si vous laissez cette valeur vide, le script crée un nom pour la nouvelle recherche basée sur le nom de la recherche que vous dupliquez.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="5d3b8-135">Pour cloner une recherche :</span><span class="sxs-lookup"><span data-stu-id="5d3b8-135">To clone a search:</span></span>
  
1. <span data-ttu-id="5d3b8-136">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="5d3b8-137">Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="5d3b8-138">Exécuter le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="5d3b8-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="5d3b8-139">Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="5d3b8-p108">Entrez les informations lorsque vous y êtes invité par le script suivantes. Tapez chaque élément d’information, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="5d3b8-142">Le nom de la recherche existante.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="5d3b8-143">Le nom de la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-143">The name of the new search.</span></span>
    
    <span data-ttu-id="5d3b8-p109">Le script crée le nouveau contenu de recherche, mais ne démarre pas. Cela vous donne la possibilité de modifier et d’exécuter la recherche à l’étape suivante. Vous pouvez afficher les propriétés de la nouvelle recherche en exécutant l’applet de commande **Get-ComplianceSearch** ou en accédant à la page de **recherche de contenu** ou de **découverte** de la sécurité &amp; centre de conformité, en fonction de la nouvelle recherche est-il associé à un cas.</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="5d3b8-147">Étape 2 : Modifier et exécuter la recherche clonée dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="5d3b8-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="5d3b8-p110">Après l’avoir exécuté le script pour cloner une recherche de contenu existante, l’étape suivante consiste pour accéder à la sécurité &amp; centre de conformité pour modifier et exécuter la recherche. Comme indiqué plus haut, vous pouvez modifier une recherche en modifiant la requête de recherche de mot clé et en ajoutant ou supprimant des conditions de recherche. Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="5d3b8-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="5d3b8-151">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5d3b8-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="5d3b8-152">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="5d3b8-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="5d3b8-153">cas eDiscovery de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="5d3b8-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
