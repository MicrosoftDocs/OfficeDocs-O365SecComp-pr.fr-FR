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
ms.openlocfilehash: 2886d2c1dd4dc2f324e8cc21babc3a9f4bf51e5f
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699202"
---
# <a name="sample-script-for-applying-eop-settings-to-multiple-tenants"></a>Exemple de script pour l’application de paramètres EOP à plusieurs locataires

L'exemple de script suivant permet aux administrateurs Microsoft Exchange Online Protection (EOP) qui gèrent plusieurs locataires (entreprises) d'utiliser Windows PowerShell pour appliquer les paramètres de configuration à leurs locataires.
  
### <a name="to-run-a-script-or-cmdlet-on-multiple-tenants"></a>Pour exécuter un script ou une cmdlet sur plusieurs locataires

1. À l'aide d'une application telle qu'Excel, créez un fichier .csv (par exemple, c:\scripts\inputfile.csv) :

2. Dans le fichier .csv, spécifiez deux noms de colonne : UserName et Cmdlet.

3. Pour chaque ligne dans le fichier .csv, ajouter le nom d'administrateur du locataire dans la colonne Nom d'utilisateur et la cmdlet à exécuter pour ce locataire dans la colonne Cmdlet. Par exemple, utilisez admin@contoso.com et Get-AcceptedDomain.

4. Copiez le script [RunCmdletOnMultipleTenants.ps1](#runcmdletonmultipletenantsps1) dans un éditeur tel que le Bloc-notes, puis enregistrez le fichier dans un emplacement (comme c:\scripts) permettant de trouver facilement les fichiers .ps1.

5. Exécutez le script à l'aide de la syntaxe suivante :

   ```Powershell
   & "<file path>\RunCmdletOnMultipleTenants.ps1" "<file path>\inputfile.csv"
   ```

   Voici un exemple.

   ```Powershell
   & "c:\scripts\RunCmdletOnMultipleTenanats.ps1" "c:\scripts\inputfile.csv"
   ```

6. Chaque client sera connecté et la cmdlet sera exécutée.

## <a name="runcmdletonmultipletenantsps1"></a>RunCmdletOnMultipleTenants. ps1

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
Remove-PsSession -Session $Session
}
```
