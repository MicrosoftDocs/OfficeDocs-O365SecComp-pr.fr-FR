---
title: Cloner une recherche de contenu dans le centre &amp; de sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Utilisez le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante dans &amp; la recherche de centre de Compliane de sécurité. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nouveau nom) est créée et contient les mêmes propriétés que la recherche d'origine. Vous pouvez ensuite modifier la nouvelle recherche (en changeant la requête par mot clé ou la plage de dates), puis l'exécuter.
ms.openlocfilehash: 15f1ca5d00f03f510745fef7ae8418192a9eb448
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213544"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="a2959-105">Cloner une recherche de contenu dans le centre &amp; de sécurité conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="a2959-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="a2959-p102">La création d'une recherche de contenu dans &amp; le centre de sécurité conformité Office 365 qui recherche un grand nombre de boîtes aux lettres ou de sites SharePoint et OneDrive entreprise peut prendre un certain temps. La spécification des sites à rechercher peut également être sujette à des erreurs si vous entrez une URL erronée. Pour éviter ces problèmes, vous pouvez utiliser le script Windows PowerShell dans cet article pour cloner rapidement une recherche de contenu existante. Lorsque vous clonez une recherche, une nouvelle recherche (avec un nom différent) est créée et contient les mêmes propriétés (telles que les emplacements de contenu et la requête de recherche) que la recherche d'origine. Vous pouvez ensuite modifier la nouvelle recherche (en changeant la requête par mot clé ou la plage de dates) et l'exécuter.</span><span class="sxs-lookup"><span data-stu-id="a2959-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="a2959-111">Pourquoi le clonage du contenu effectue des recherches?</span><span class="sxs-lookup"><span data-stu-id="a2959-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="a2959-112">Pour comparer les résultats de différentes requêtes de recherche par mot clé exécutées sur les mêmes emplacements de contenu.</span><span class="sxs-lookup"><span data-stu-id="a2959-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="a2959-113">Pour éviter d'avoir à saisir de nouveau un grand nombre d'emplacements de contenu lorsque vous créez une recherche.</span><span class="sxs-lookup"><span data-stu-id="a2959-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="a2959-114">Pour réduire la taille des résultats de la recherche; par exemple, si vous avez une recherche qui renvoie un trop grand nombre de résultats à exporter, vous pouvez cloner la recherche, puis ajouter une condition de recherche basée sur une plage de dates pour réduire le nombre de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="a2959-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="a2959-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a2959-115">Before you begin</span></span>

- <span data-ttu-id="a2959-116">Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité &amp; conformité pour exécuter le script décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a2959-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="a2959-p103">Le script inclut une gestion des erreurs minimale. Le principal objectif du script est de cloner rapidement une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="a2959-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="a2959-119">Le script crée une recherche de contenu, mais ne le démarre pas.</span><span class="sxs-lookup"><span data-stu-id="a2959-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="a2959-p104">Ce script prend en compte si la recherche de contenu que vous clonez est associée à un cas de découverte électronique. Si la recherche est associée à un cas, la nouvelle recherche est également associée à la même casse. Si la recherche existante n'est pas associée à un cas, la nouvelle recherche est indiquée sur la page **recherche de contenu** dans &amp; le centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="a2959-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="a2959-p105">L'exemple de script fourni dans cette rubrique n'est pas pris en charge dans le cadre d'un service ou d'un programme de support standard Microsoft. L'exemple de script est fourni en l'État sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, toute garantie implicite de qualité marchande ou d'adéquation à un usage particulier. L'ensemble des risques liés à l'utilisation ou aux performances de l'exemple de script et de la documentation reste avec vous. En aucun cas Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de quelque dommage que ce soit (y compris, sans s'y limiter, les dommages pour les pertes de bénéfices, les interruptions d'entreprise, la perte de les informations professionnelles, ou toute autre perte de façon pécuniaire, découlant de l'utilisation ou de l'impossibilité d'utiliser les scripts ou la documentation, même si Microsoft a été avisé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="a2959-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="a2959-128">Étape 1: exécuter le script pour cloner une recherche</span><span class="sxs-lookup"><span data-stu-id="a2959-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="a2959-p106">Le script de cette étape crée une recherche de contenu en clonant une recherche existante. Lorsque vous exécutez ce script, vous êtes invité à fournir les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="a2959-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="a2959-p107">**Vos informations d'identification utilisateur** : le script utilisera vos informations d'identification pour vous connecter &amp; au centre de sécurité conformité de votre organisation Office 365 avec Windows PowerShell. Comme indiqué précédemment, vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre &amp; de sécurité conformité pour exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="a2959-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="a2959-133">**Nom de la recherche existante** : il s'agit de la recherche de contenu que vous souhaitez Cloner.</span><span class="sxs-lookup"><span data-stu-id="a2959-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="a2959-134">**Nom de la nouvelle recherche qui sera créée** : Si vous laissez cette valeur vide, le script crée un nom pour la nouvelle recherche basée sur le nom de la recherche que vous clonez.</span><span class="sxs-lookup"><span data-stu-id="a2959-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="a2959-135">Pour cloner une recherche:</span><span class="sxs-lookup"><span data-stu-id="a2959-135">To clone a search:</span></span>
  
1. <span data-ttu-id="a2959-136">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="a2959-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="a2959-137">Ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="a2959-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="a2959-138">Exécutez le script; par exemple:</span><span class="sxs-lookup"><span data-stu-id="a2959-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="a2959-139">Lorsque vous êtes invité à entrer vos informations d'identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2959-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="a2959-p108">Entrez les informations suivantes lorsque le script vous y invite. Tapez chaque information, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="a2959-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="a2959-142">Nom de la recherche existante.</span><span class="sxs-lookup"><span data-stu-id="a2959-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="a2959-143">Nom de la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="a2959-143">The name of the new search.</span></span>
    
    <span data-ttu-id="a2959-p109">Le script crée la recherche de contenu, mais ne le démarre pas. Cela vous permet de modifier et d'exécuter la recherche à l'étape suivante. Vous pouvez afficher les propriétés de la nouvelle recherche en exécutant la cmdlet **Get-ComplianceSearch** ou en accédant à la page **recherche de contenu** ou **EDiscovery** dans &amp; le centre de sécurité conformité, selon que la nouvelle recherche est ou non associé à un cas.</span><span class="sxs-lookup"><span data-stu-id="a2959-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="a2959-147">Étape 2: modifier et exécuter la recherche clonée dans le centre &amp; de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="a2959-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="a2959-p110">Une fois que vous avez exécuté le script pour cloner une recherche de contenu existante, l'étape suivante consiste à accéder &amp; au centre de sécurité conformité afin de modifier et d'exécuter la nouvelle recherche. Comme indiqué précédemment, vous pouvez modifier une recherche en modifiant la requête de recherche par mot clé et en ajoutant ou supprimant des conditions de recherche. Pour plus d'informations, voir:</span><span class="sxs-lookup"><span data-stu-id="a2959-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="a2959-151">Recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a2959-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="a2959-152">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="a2959-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="a2959-153">cas de découverte électronique dans le centre &amp; de sécurité conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="a2959-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
