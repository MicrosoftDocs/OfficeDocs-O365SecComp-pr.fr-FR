---
title: Attribuer des autorisations de découverte électronique aux sites OneDrive Entreprise
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Vous pouvez utiliser le centre eDiscovery dans SharePoint Online pour rechercher toutes les OneDrive pour les sites dans votre organisation pour certains mots clés, les informations sensibles et autres critères de recherche. Chaque utilisateur de votre organisation est le propriétaire de leur site Business, qui se trouve dans la collection de sites nommée OneDrive https://domain-my.sharepoint.com. Par défaut, un administrateur général Office 365 ou un gestionnaire de conformité ne peuvent pas utiliser le centre eDiscovery dans SharePoint Online pour rechercher les sites de Commerce OneDrive. Pour rechercher un site, les administrateurs ou les responsables de la conformité Business OneDrive doit être un administrateur de collection de sites pour ce site Business OneDrive.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528124"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a><span data-ttu-id="ff1bf-106">Attribuer des autorisations de découverte électronique aux sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="ff1bf-106">Assign eDiscovery permissions to OneDrive for Business sites</span></span>

<span data-ttu-id="ff1bf-p102">Vous pouvez utiliser le centre eDiscovery dans SharePoint Online pour rechercher toutes les OneDrive pour les sites dans votre organisation pour certains mots clés, les informations sensibles et autres critères de recherche. Chaque utilisateur de votre organisation est le propriétaire de leur site Business, qui se trouve dans la collection de sites nommée OneDrive https://domain-my.sharepoint.com. Par défaut, un administrateur général Office 365 ou un gestionnaire de conformité ne peuvent pas utiliser le centre eDiscovery dans SharePoint Online pour rechercher les sites de Commerce OneDrive. Pour rechercher un site, les administrateurs ou les responsables de la conformité Business OneDrive doit être un administrateur de collection de sites pour ce site Business OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p102">You can use the eDiscovery Center in SharePoint Online to search all OneDrive for Business sites in your organization for certain keywords, sensitive information, and other search criteria. Each user in your organization is the owner of their OneDrive for Business site, which is located in the site collection named https://domain-my.sharepoint.com. By default, an Office 365 global administrator or compliance manager can't use the eDiscovery Center in SharePoint Online to search any OneDrive for Business sites. To search a OneDrive for Business site, administrators or compliance managers must be a site collection administrator for that OneDrive for Business site.</span></span> 
  
<span data-ttu-id="ff1bf-111">Cet article vous guide dans les étapes pour effectuer un administrateur ou conformité gestionnaire un administrateur de collection de sites pour chaque site de l’entreprise OneDrive dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-111">This article guides you through the steps to make an administrator or compliance manager a site collection administrator for every OneDrive for Business site in your organization.</span></span> 
  
<span data-ttu-id="ff1bf-112">Voir la section [plus d’informations](#more-information) pour obtenir des conseils sur l’utilisation du script dans cet article, notamment en le script à l’étape 3 pour supprimer un utilisateur comme administrateur de collection de sites à partir de OneDrive pour les sites de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-112">See the [More information](#more-information) section for tips about using the script in this article, including revising the script in Step 3 to remove a user as a site collection administrator from OneDrive for Business sites.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="ff1bf-113">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ff1bf-113">Before you begin</span></span>

- <span data-ttu-id="ff1bf-p103">Installez SharePoint Online Management Shell. Pour plus d'informations, voir [Configurer l'environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p103">Install the SharePoint Online Management Shell. For information, see [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span></span>
    
- <span data-ttu-id="ff1bf-116">Exécutez le script à l’étape 3, chaque fois que vous souhaitez affecter un utilisateur comme administrateur de collection de sites à n’importe quel OneDrive pour les sites d’entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-116">Run the script in Step 3 each time you want to assign a user as a site collection administrator to any OneDrive for Business sites in your organization.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="ff1bf-p104">Un administrateur ou conformité responsable qui est un administrateur de collection de sites pour OneDrive pour les sites peuvent ouvrir OneDrive des utilisateurs pour les bibliothèques de documents métiers et effectuer les mêmes tâches que le propriétaire. Il est important de contrôle et contrôler les personnes qui attribué des autorisations de découverte électronique à OneDrive pour les sites d’entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p104">An administrator or compliance manager who is a site collection administrator for OneDrive for Business sites can open users' OneDrive for Business document libraries and perform the same tasks as the owner. It's important to control and monitor who has been assigned eDiscovery permissions to OneDrive for Business sites in your organization.</span></span> 
  
- <span data-ttu-id="ff1bf-p105">L’exemple de script fournie dans cet article n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise du script est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser l’exemple de script ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p105">The sample script provided in this article isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a><span data-ttu-id="ff1bf-124">Étape 1 : Collecter une liste de tous les OneDrive pour les sites de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="ff1bf-124">Step 1: Collect a list of all OneDrive for Business sites</span></span>

<span data-ttu-id="ff1bf-p106">La première étape consiste à créer une liste de tous les OneDrive pour les sites au sein de votre organisation. Pour plus d’informations, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Le script que vous exécutez l’étape 3 assigne un utilisateur spécifié en tant qu’administrateur de collection de sites pour chaque site de l’entreprise répertorié dans le fichier texte qui est créé dans cette étape OneDrive. Le texte suivant fournit un exemple de mode de mise en forme de la liste des sites dans ce fichier. Vous pouvez supprimer les sites de ce fichier si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p106">The first step is to create a list of all OneDrive for Business sites in your organization. For instructions, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. The script that you run in Step 3 assigns a specified user as a site collection administrator to each OneDrive for Business site listed in the text file that's created in this step. The following text provides an example of how the list of sites in this file should be formatted. You can remove sites from this file if necessary.</span></span>

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a><span data-ttu-id="ff1bf-131">Étape 2 : Se connecter à SharePoint Online Management Shell pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="ff1bf-131">Step 2: Connect SharePoint Online Management Shell to your organization</span></span>

1. <span data-ttu-id="ff1bf-132">Sur votre ordinateur local, ouvrez SharePoint Online Management Shell et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-132">On your local computer, open the SharePoint Online Management Shell, and run the following command:</span></span>

    ```
    $credentials = Get-Credential
    ```

2. <span data-ttu-id="ff1bf-133">Dans la boîte de dialogue **Demande d'informations d'identification Windows PowerShell**, saisissez le nom d'utilisateur et le mot de passe associés à votre compte d'administrateur global Office 365, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-133">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global administrator account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="ff1bf-134">Exécutez la commande suivante pour connecter le Shell à votre organisation SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-134">Run the following command to connect the Shell to your SharePoint Online organization:</span></span>
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. <span data-ttu-id="ff1bf-135">Pour vérifier que vous êtes connecté à votre organisation SharePoint Online, exécutez la commande suivante pour obtenir la liste de tous les sites de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-135">To verify that you are connected to your SharePoint Online organization, run the following command to get a list of all the sites in your organization:</span></span>
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a><span data-ttu-id="ff1bf-136">Étape 3 : Attribuer à un utilisateur le rôle d’administrateur de collection de sites pour les sites OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="ff1bf-136">Step 3: Assign a user as a site collection administrator to OneDrive for Business sites</span></span>

<span data-ttu-id="ff1bf-p107">L’étape suivante consiste à exécuter un script qui affecte un utilisateur spécifié en tant qu’un administrateur de collection de sites dans chaque site de l’entreprise dans votre organisation OneDrive. Ce script utilise la liste de OneDrive pour les sites d’entreprise que vous avez créé à l’étape 1. Comme indiqué précédemment, vous devez exécuter ce script chaque fois que vous souhaitez affecter à un utilisateur en tant qu’administrateur de collection de sites vers OneDrive pour les sites de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p107">The next step is to run a script that assigns a specified user as a site collection administrator in every OneDrive for Business site in your organization. This script uses the list of OneDrive for Business sites that you created in Step 1. As previously stated, you have to run this script each time that you want to assign a user as a site collection administrator to OneDrive for Business sites.</span></span>
  
1. <span data-ttu-id="ff1bf-p108">Enregistrez le texte suivant dans un fichier texte. Par exemple, vous pouvez l’enregistrer dans un fichier nommé OD4BAssignSCA.txt.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p108">Save the following text to a text file. For example, you could save it to a file named OD4BAssignSCA.txt.</span></span>

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. <span data-ttu-id="ff1bf-p109">Modifier les variables suivantes au début du fichier de script et utilisez des informations spécifiques à votre organisation. Les exemples suivants supposent que le nom de domaine de votre organisation est contoso.onmicrosoft.com. Veillez à entourer les valeurs pour les variables avec des guillemets (« »).</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p109">Edit the following variables in the beginning of the script file, and use information that's specific to your organization. The following examples assume that the domain name of your organization is contoso.onmicrosoft.com. Be sure to surround the values for the variables with double-quotation marks (" ").</span></span>
    
    - <span data-ttu-id="ff1bf-145">**$AdminURI** - Spécifie l’URI de votre service d’administration SharePoint Online, par exemple, `"https://contoso-admin.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-145">**$AdminURI** - This specifies the URI for your SharePoint Online admin service, for example,  `"https://contoso-admin.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="ff1bf-146">**$AdminAccount** - spécifie un compte d’administrateur global dans votre organisation Office 365, par exemple, `"admin@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-146">**$AdminAccount** - This specifies a global administrator account in your Office 365 organization, for example,  `"admin@contoso.onmicrosoft.com"`.</span></span>
    
    - <span data-ttu-id="ff1bf-147">**$eDiscoveryUser** - Spécifie le compte d’utilisateur d’un administrateur ou du Gestionnaire de conformité qui sera attribué par exemple, en tant qu’administrateur de collection de sites pour chaque site de l’entreprise dans votre organisation, OneDrive `"annb@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-147">**$eDiscoveryUser** - This specifies the user account of an administrator or compliance manager who will be assigned as a site collection administrator for every OneDrive for Business site in your organization, for example,  `"annb@contoso.onmicrosoft.com"`.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="ff1bf-148">Modifier le compte d’utilisateur spécifié par la variable **$eDiscoveryUser** et réexécutez le script pour affecter un autre utilisateur comme administrateur de collection de sites pour le sites d’entreprise qui sont spécifiés par la variable **$MySiteListFile** OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-148">Change the user account specified by the **$eDiscoveryUser** variable and re-run the script to assign a different user as a site collection administrator to the OneDrive for Business sites that are specified by the **$MySiteListFile** variable.</span></span> 
  
    - <span data-ttu-id="ff1bf-p110">**$MySitePrefix** Spécifie l’URL de domaine du site Mon site dans votre organisation. Il s’agit du domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation, par exemple, `"https://contoso-my.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p110">**$MySitePrefix**This specifies the URL for your organization's MySite domain. This is the domain that contains all the OneDrive for Business sites in your organization, for example,  `"https://contoso-my.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="ff1bf-p111">**$MySiteListFile** Spécifie le chemin d’accès complet du fichier texte que vous avez créé à l’étape 1. Ce fichier contient une liste de OneDrive pour les sites d’entreprise dans votre organisation, par exemple, `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Veillez à mettre la valeur de cette variable avec des guillemets simples (' '). Notez que vous devez spécifier l’emplacement que vous avez enregistré le fichier texte à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p111">**$MySiteListFile**This specifies the full path of the text file that you created in Step 1. This file contains a list of OneDrive for Business sites in your organization, for example,  `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Be sure to surround the value for this variable with single-quotation marks (' '). Note that you should specify the location that you saved the text file to in Step 1.</span></span>
    
3. <span data-ttu-id="ff1bf-p112">Enregistrez le fichier texte en tant que fichier de script PowerShell en remplaçant le suffixe du nom de fichier par .ps1. Par exemple, enregistrez le fichier OD4BAssignSCA.txt sous OD4BAssignSCA.ps1.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p112">Save the text file as a PowerShell script file by changing the file name suffix to .ps1. For example, save the file OD4BAssignSCA.txt as OD4BAssignSCA.ps1.</span></span>
    
4. <span data-ttu-id="ff1bf-157">Dans SharePoint Online Management Shell, accédez au dossier qui contient le script PowerShell que vous avez créé à l’étape précédente, puis exécutez le script, par exemple :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-157">In SharePoint Online Management Shell, go to the folder that contains the PowerShell script that you created in the previous step, and then run the script, for example:</span></span>
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    <span data-ttu-id="ff1bf-p113">Vous serez invité à entrer le mot de passe pour le compte d’administrateur que vous avez spécifié dans le script. Si le script s’exécute correctement, le message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` est affichée pour chaque site d’entreprise est répertorié dans le fichier d’entrée spécifié par **$MySiteListFile**OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p113">You will be prompted to enter the password for the administrator account that you specified in the script. If the script runs successfully, the message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` is displayed for each OneDrive for Business site that's listed in the input file specified by **$MySiteListFile**.</span></span>

## <a name="more-information"></a><span data-ttu-id="ff1bf-160">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="ff1bf-160">More information</span></span>

- <span data-ttu-id="ff1bf-p114">Le script que vous avez exécuté l’étape 3 utilise la cmdlet **Set-SPOUser** pour assigner l’utilisateur spécifié en tant qu’administrateur de collection de sites pour chaque OneDrive entreprise est répertorié dans le fichier spécifié par la variable **$MySiteListFile** . Si vous avez une très grande entreprise avec des milliers d’utilisateurs, suivez les recommandations suivantes pour la rendre plus facile de gérer l’affectation d’autorisations eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p114">The script that you ran in Step 3 uses the **Set-SPOUser** cmdlet to assign the specified user as a site collection administrator to every OneDrive for Business that's listed in the file specified by the **$MySiteListFile** variable. If you have a very large organization with thousands of users, consider doing the following to make it easier to manage assigning eDiscovery permissions.</span></span> 
    
  - <span data-ttu-id="ff1bf-163">Modifiez le fichier que vous avez créé à l’étape 1 qui contient la liste de OneDrive pour les sites de l’entreprise afin qu’elle inclut uniquement les sites pour les utilisateurs qui sont impliqués dans les cas juridiques actives.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-163">Edit the file that you created in Step 1 that contains the list of OneDrive for Business sites so that it includes only the sites for users are that are involved in active legal cases.</span></span>
    
  - <span data-ttu-id="ff1bf-p115">Affecter des autorisations à OneDrive pas plus de 2 500 sites de commerce par jour. Par exemple, supposons que vous avez 10 000 OneDrive pour les sites au sein de votre organisation. Vous pouvez créer la liste à l’étape 1 pour collecter tous les sites. Ensuite, vous pouvez utiliser ce fichier pour créer les quatre fichiers contenant chacun 2 500 utilisateurs. Le premier jour, exécuter le script à l’étape 3 pour attribuer des autorisations sur OneDrive tout d’abord 2 500 sites d’entreprise. Le deuxième jour, vous souhaiteriez exécuter le script pour OneDrive ensuite 2 500 pour les sites et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p115">Assign permissions to no more than 2,500 OneDrive for Business sites per day. For example, let's say you have 10,000 OneDrive for Business sites in your organization. You could create the list in Step 1 to collect all the sites. Then you could use that file to create four files that each contain 2,500 users. On the first day, you would run the script in Step 3 to assign permissions to the first 2,500 OneDrive for Business sites. On the second day, you would run the script for the next 2,500 OneDrive for Business sites, and so on.</span></span>
    
- <span data-ttu-id="ff1bf-p116">Conserver un enregistrement de OneDrive pour les sites d’entreprise qui ont été affectées des autorisations de découverte électronique et de l’utilisateur auquel est affectée en tant qu’administrateur de collection de sites. Par exemple, une fois que vous assignez les autorisations, vous pourrez enregistrer le fichier texte qui contient la liste de OneDrive pour les sites et ajouter une ligne qui identifie l’utilisateur qui est affectée en tant qu’administrateur de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p116">Keep a record of the OneDrive for Business sites that were assigned eDiscovery permissions and the user who is assigned as the site collection administrator. For example, after you assign permissions, you can save the text file that contains the list of OneDrive for Business sites and add a line to it that identifies the user who is assigned as the site collection administrator.</span></span>
    
- <span data-ttu-id="ff1bf-p117">Les utilisateurs peuvent afficher la liste des administrateurs de collection de sites pour leur site Business OneDrive. Les utilisateurs étant administrateur de collection de sites pour leur propre site Business OneDrive, ils peuvent supprimer des administrateurs de collection de sites. Suivez les recommandations suivantes afin d’atténuer les risques de suppression de l’utilisateur qui est attribué des autorisations de découverte électronique vers OneDrive pour les sites des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p117">Users can view the list of site collection administators for their OneDrive for Business site. Because users are site collection administrator for their own OneDrive for Business site, they can remove site collection administrators. Consider doing the following to mitigate the chance of users removing the user who is assigned eDiscovery permissions to OneDrive for Business sites.</span></span>
    
  - <span data-ttu-id="ff1bf-175">Communiquer avec les utilisateurs qu’à des fins de découverte et de conformité, un responsable de la conformité a été affecté comme un administrateur de collection de sites vers OneDrive pour les sites d’entreprise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-175">Communicate to users that for eDiscovery and compliance purposes, a compliance officer has been assigned as a site collection administrator to OneDrive for Business sites in your organization.</span></span>
    
  - <span data-ttu-id="ff1bf-176">Réexécutez le script à l’étape 3, si nécessaire, pour réattribuer un utilisateur en tant que l’administrateur de collection de sites pour OneDrive pour les sites de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-176">Re-run the script in Step 3, if necessary, to re-assign a user as the site collection administrator for OneDrive for Business sites.</span></span>
    
- <span data-ttu-id="ff1bf-p118">Vous pouvez également utiliser le script que vous avez exécuté l’étape 3 pour supprimer un utilisateur en tant qu’administrateur de collection de sites à partir de OneDrive pour les sites de l’entreprise. Pour supprimer un utilisateur comme administrateur de collection de sites, vous devez modifier la commande suivante (vers la fin du script) à partir de :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-p118">You can also use the script that you ran in Step 3 to remove a user as the site collection administrator from OneDrive for Business sites. To remove a user as a site collection administrator, you have to change the following command (near the end of the script) from:</span></span> 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    <span data-ttu-id="ff1bf-179">par :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-179">to:</span></span>
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    <span data-ttu-id="ff1bf-180">Vous pouvez également remplacer la ligne suivante dans le script :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-180">You can also change the following line in the script from:</span></span>

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    <span data-ttu-id="ff1bf-181">par :</span><span class="sxs-lookup"><span data-stu-id="ff1bf-181">to:</span></span>
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    <span data-ttu-id="ff1bf-182">Après avoir apporté les modifications, enregistrez le script avec un nom différent, tel que OD4BRemoveSCA.ps1 et puis l’utiliser pour supprimer un utilisateur comme administrateur de collection de sites à partir d’un groupe de OneDrive pour les sites de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-182">After you make these changes, save the script with a different name, such as OD4BRemoveSCA.ps1, and then use it to remove a user as a site collection administrator from a group of OneDrive for Business sites.</span></span>
