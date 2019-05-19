---
title: Exemple de script pour l'application de paramètres EOP à plusieurs locataires
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e87e84e1-7be0-44bf-a414-d91d60ed8817
description: L'exemple de script suivant permet aux administrateurs Microsoft Exchange Online Protection (EOP) qui gèrent plusieurs locataires (entreprises) d'utiliser Windows PowerShell pour appliquer les paramètres de configuration à leurs locataires.
ms.openlocfilehash: f064a44722d165711543e5a15ec6a19d70af4b25
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154556"
---
# <a name="sample-script-for-applying-eop-settings-to-multiple-tenants"></a>Exemple de script pour l’application de paramètres EOP à plusieurs locataires

L'exemple de script suivant permet aux administrateurs Microsoft Exchange Online Protection (EOP) qui gèrent plusieurs locataires (entreprises) d'utiliser Windows PowerShell pour appliquer les paramètres de configuration à leurs locataires.
  
### <a name="to-run-a-script-or-cmdlet-on-multiple-tenants"></a>Pour exécuter un script ou une cmdlet sur plusieurs locataires

1. À l'aide d'une application telle qu'Excel, créez un fichier .csv (par exemple, c:\scripts\inputfile.csv) :
    
1. Dans le fichier .csv, spécifiez deux noms de colonne : UserName et Cmdlet.
    
2. Pour chaque ligne dans le fichier .csv, ajouter le nom d'administrateur du locataire dans la colonne Nom d'utilisateur et la cmdlet à exécuter pour ce locataire dans la colonne Cmdlet. Par exemple, utilisez admin@contoso.com et Get-AcceptedDomain.
    
2. Copiez le script [RunCmdletOnMultipleTenants.ps1](sample-script-for-applying-eop-settings-to-multiple-tenants.md#RunCmdletOnMultipleTenants.ps1) dans un éditeur tel que le Bloc-notes, puis enregistrez le fichier dans un emplacement (comme c:\scripts) permettant de trouver facilement les fichiers .ps1. 
    
3. Exécutez le script à l'aide de la syntaxe suivante :
    ```Powershell
     & "<file path>\RunCmdletOnMultipleTenants.ps1" "<file path>\inputfile.csv"
    ```
    
    Voici un exemple. 
    
    ```Powershell
    & "c:\scripts\RunCmdletOnMultipleTenanats.ps1" "c:\scripts\inputfile.csv"
    ```

4. Chaque client sera connecté et la cmdlet sera exécutée.
    
## <a name="runcmdletonmultipletenantsps1"></a>RunCmdletOnMultipleTenants. ps1
<a name="RunCmdletOnMultipleTenants.ps1"> </a>

```Powershell
# This script runs Windows PowerShell cmdlets on multiple tenants.
# Usage: RunCmdletOnMultipleTenants.ps1 inputfile.csv
#  
# .csv input file sample: 
# UserName,Cmdlet
# admin@contoso.com,Get-AcceptedDomain | ft Name
# URI for connecting to remote Windows PowerShell
$URI = "https://ps.protection.outlook.com/powershell-liveid/"
# Get the .csv file name as an argument to this script.
$FilePath = $args[0]
# Import the UserName and Cmdlet values from the .csv file.
$CompanyList = Import-CSV $FilePath
# Loop through each entry from the .csv file.
ForEach ($Company in $CompanyList) {
# Get the current entry's UserName.
$UserName = $Company.UserName
# Get the current entry's Cmdlet.
$Cmdlet = $Company.Cmdlet
# Create a PowerShell credential object by using the current entry's UserName. Prompt for the password.
$UserCredential = Get-Credential -username $UserName
# Log on to a new Windows PowerShell session.
$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri $URI -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $Session
# Here's where the script to be run on the tenant goes.
# In this example, the cmdlet in the .csv file runs.
Invoke-Expression $Cmdlet
# End the current PowerShell session.
remove-pssession -session $Session
}

```


