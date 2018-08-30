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
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a>Attribuer des autorisations de découverte électronique aux sites OneDrive Entreprise

Vous pouvez utiliser le centre eDiscovery dans SharePoint Online pour rechercher toutes les OneDrive pour les sites dans votre organisation pour certains mots clés, les informations sensibles et autres critères de recherche. Chaque utilisateur de votre organisation est le propriétaire de leur site Business, qui se trouve dans la collection de sites nommée OneDrive https://domain-my.sharepoint.com. Par défaut, un administrateur général Office 365 ou un gestionnaire de conformité ne peuvent pas utiliser le centre eDiscovery dans SharePoint Online pour rechercher les sites de Commerce OneDrive. Pour rechercher un site, les administrateurs ou les responsables de la conformité Business OneDrive doit être un administrateur de collection de sites pour ce site Business OneDrive. 
  
Cet article vous guide dans les étapes pour effectuer un administrateur ou conformité gestionnaire un administrateur de collection de sites pour chaque site de l’entreprise OneDrive dans votre organisation. 
  
Voir la section [plus d’informations](#more-information) pour obtenir des conseils sur l’utilisation du script dans cet article, notamment en le script à l’étape 3 pour supprimer un utilisateur comme administrateur de collection de sites à partir de OneDrive pour les sites de l’entreprise. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Installez SharePoint Online Management Shell. Pour plus d'informations, voir [Configurer l'environnement SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318).
    
- Exécutez le script à l’étape 3, chaque fois que vous souhaitez affecter un utilisateur comme administrateur de collection de sites à n’importe quel OneDrive pour les sites d’entreprise dans votre organisation. 
    
    > [!IMPORTANT]
    > Un administrateur ou conformité responsable qui est un administrateur de collection de sites pour OneDrive pour les sites peuvent ouvrir OneDrive des utilisateurs pour les bibliothèques de documents métiers et effectuer les mêmes tâches que le propriétaire. Il est important de contrôle et contrôler les personnes qui attribué des autorisations de découverte électronique à OneDrive pour les sites d’entreprise dans votre organisation. 
  
- L’exemple de script fournie dans cet article n’est pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. L’exemple de script est fourni en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et un exemple de script. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise du script est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser l’exemple de script ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a>Étape 1 : Collecter une liste de tous les OneDrive pour les sites de l’entreprise

La première étape consiste à créer une liste de tous les OneDrive pour les sites au sein de votre organisation. Pour plus d’informations, voir [créer une liste de tous les emplacements de OneDrive dans votre organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Ce script dans cet article crée un fichier texte qui contient une liste de tous les sites OneDrive. Le script que vous exécutez l’étape 3 assigne un utilisateur spécifié en tant qu’administrateur de collection de sites pour chaque site de l’entreprise répertorié dans le fichier texte qui est créé dans cette étape OneDrive. Le texte suivant fournit un exemple de mode de mise en forme de la liste des sites dans ce fichier. Vous pouvez supprimer les sites de ce fichier si nécessaire.

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a>Étape 2 : Se connecter à SharePoint Online Management Shell pour votre organisation

1. Sur votre ordinateur local, ouvrez SharePoint Online Management Shell et exécutez la commande suivante :

    ```
    $credentials = Get-Credential
    ```

2. Dans la boîte de dialogue **Demande d'informations d'identification Windows PowerShell**, saisissez le nom d'utilisateur et le mot de passe associés à votre compte d'administrateur global Office 365, puis cliquez sur **OK**.
    
3. Exécutez la commande suivante pour connecter le Shell à votre organisation SharePoint Online :
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. Pour vérifier que vous êtes connecté à votre organisation SharePoint Online, exécutez la commande suivante pour obtenir la liste de tous les sites de votre organisation :
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a>Étape 3 : Attribuer à un utilisateur le rôle d’administrateur de collection de sites pour les sites OneDrive Entreprise

L’étape suivante consiste à exécuter un script qui affecte un utilisateur spécifié en tant qu’un administrateur de collection de sites dans chaque site de l’entreprise dans votre organisation OneDrive. Ce script utilise la liste de OneDrive pour les sites d’entreprise que vous avez créé à l’étape 1. Comme indiqué précédemment, vous devez exécuter ce script chaque fois que vous souhaitez affecter à un utilisateur en tant qu’administrateur de collection de sites vers OneDrive pour les sites de l’entreprise.
  
1. Enregistrez le texte suivant dans un fichier texte. Par exemple, vous pouvez l’enregistrer dans un fichier nommé OD4BAssignSCA.txt.

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

2. Modifier les variables suivantes au début du fichier de script et utilisez des informations spécifiques à votre organisation. Les exemples suivants supposent que le nom de domaine de votre organisation est contoso.onmicrosoft.com. Veillez à entourer les valeurs pour les variables avec des guillemets (« »).
    
    - **$AdminURI** - Spécifie l’URI de votre service d’administration SharePoint Online, par exemple, `"https://contoso-admin.sharepoint.com"`.
    
    - **$AdminAccount** - spécifie un compte d’administrateur global dans votre organisation Office 365, par exemple, `"admin@contoso.onmicrosoft.com"`.
    
    - **$eDiscoveryUser** - Spécifie le compte d’utilisateur d’un administrateur ou du Gestionnaire de conformité qui sera attribué par exemple, en tant qu’administrateur de collection de sites pour chaque site de l’entreprise dans votre organisation, OneDrive `"annb@contoso.onmicrosoft.com"`.
    
      > [!NOTE]
      > Modifier le compte d’utilisateur spécifié par la variable **$eDiscoveryUser** et réexécutez le script pour affecter un autre utilisateur comme administrateur de collection de sites pour le sites d’entreprise qui sont spécifiés par la variable **$MySiteListFile** OneDrive. 
  
    - **$MySitePrefix** Spécifie l’URL de domaine du site Mon site dans votre organisation. Il s’agit du domaine qui contient tous les OneDrive pour les sites d’entreprise dans votre organisation, par exemple, `"https://contoso-my.sharepoint.com"`.
    
    - **$MySiteListFile** Spécifie le chemin d’accès complet du fichier texte que vous avez créé à l’étape 1. Ce fichier contient une liste de OneDrive pour les sites d’entreprise dans votre organisation, par exemple, `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Veillez à mettre la valeur de cette variable avec des guillemets simples (' '). Notez que vous devez spécifier l’emplacement que vous avez enregistré le fichier texte à l’étape 1.
    
3. Enregistrez le fichier texte en tant que fichier de script PowerShell en remplaçant le suffixe du nom de fichier par .ps1. Par exemple, enregistrez le fichier OD4BAssignSCA.txt sous OD4BAssignSCA.ps1.
    
4. Dans SharePoint Online Management Shell, accédez au dossier qui contient le script PowerShell que vous avez créé à l’étape précédente, puis exécutez le script, par exemple :
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    Vous serez invité à entrer le mot de passe pour le compte d’administrateur que vous avez spécifié dans le script. Si le script s’exécute correctement, le message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` est affichée pour chaque site d’entreprise est répertorié dans le fichier d’entrée spécifié par **$MySiteListFile**OneDrive.

## <a name="more-information"></a>Plus d'informations

- Le script que vous avez exécuté l’étape 3 utilise la cmdlet **Set-SPOUser** pour assigner l’utilisateur spécifié en tant qu’administrateur de collection de sites pour chaque OneDrive entreprise est répertorié dans le fichier spécifié par la variable **$MySiteListFile** . Si vous avez une très grande entreprise avec des milliers d’utilisateurs, suivez les recommandations suivantes pour la rendre plus facile de gérer l’affectation d’autorisations eDiscovery. 
    
  - Modifiez le fichier que vous avez créé à l’étape 1 qui contient la liste de OneDrive pour les sites de l’entreprise afin qu’elle inclut uniquement les sites pour les utilisateurs qui sont impliqués dans les cas juridiques actives.
    
  - Affecter des autorisations à OneDrive pas plus de 2 500 sites de commerce par jour. Par exemple, supposons que vous avez 10 000 OneDrive pour les sites au sein de votre organisation. Vous pouvez créer la liste à l’étape 1 pour collecter tous les sites. Ensuite, vous pouvez utiliser ce fichier pour créer les quatre fichiers contenant chacun 2 500 utilisateurs. Le premier jour, exécuter le script à l’étape 3 pour attribuer des autorisations sur OneDrive tout d’abord 2 500 sites d’entreprise. Le deuxième jour, vous souhaiteriez exécuter le script pour OneDrive ensuite 2 500 pour les sites et ainsi de suite.
    
- Conserver un enregistrement de OneDrive pour les sites d’entreprise qui ont été affectées des autorisations de découverte électronique et de l’utilisateur auquel est affectée en tant qu’administrateur de collection de sites. Par exemple, une fois que vous assignez les autorisations, vous pourrez enregistrer le fichier texte qui contient la liste de OneDrive pour les sites et ajouter une ligne qui identifie l’utilisateur qui est affectée en tant qu’administrateur de collection de sites.
    
- Les utilisateurs peuvent afficher la liste des administrateurs de collection de sites pour leur site Business OneDrive. Les utilisateurs étant administrateur de collection de sites pour leur propre site Business OneDrive, ils peuvent supprimer des administrateurs de collection de sites. Suivez les recommandations suivantes afin d’atténuer les risques de suppression de l’utilisateur qui est attribué des autorisations de découverte électronique vers OneDrive pour les sites des utilisateurs.
    
  - Communiquer avec les utilisateurs qu’à des fins de découverte et de conformité, un responsable de la conformité a été affecté comme un administrateur de collection de sites vers OneDrive pour les sites d’entreprise dans votre organisation.
    
  - Réexécutez le script à l’étape 3, si nécessaire, pour réattribuer un utilisateur en tant que l’administrateur de collection de sites pour OneDrive pour les sites de l’entreprise.
    
- Vous pouvez également utiliser le script que vous avez exécuté l’étape 3 pour supprimer un utilisateur en tant qu’administrateur de collection de sites à partir de OneDrive pour les sites de l’entreprise. Pour supprimer un utilisateur comme administrateur de collection de sites, vous devez modifier la commande suivante (vers la fin du script) à partir de : 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    par :
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    Vous pouvez également remplacer la ligne suivante dans le script :

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    par :
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    Après avoir apporté les modifications, enregistrez le script avec un nom différent, tel que OD4BRemoveSCA.ps1 et puis l’utiliser pour supprimer un utilisateur comme administrateur de collection de sites à partir d’un groupe de OneDrive pour les sites de l’entreprise.
