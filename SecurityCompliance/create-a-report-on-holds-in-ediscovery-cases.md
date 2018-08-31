---
title: Créer un rapport sur les suspensions dans les cas eDiscovery dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Utilisez le script dans cet article pour générer un rapport qui contient des informations sur toutes les suspensions qui sont associés à des cas de découverte de sécurité Office 365 &amp; centre de conformité.
ms.openlocfilehash: 8bc1285f776e2b1aa0c0330c06ccffff8ce4585c
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258642"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Créer un rapport sur les suspensions dans les cas eDiscovery dans Office 365
  
Le script dans cet article permet aux administrateurs de découverte électronique et gestionnaires de découverte électronique génèrent un rapport qui contient des informations sur toutes les suspensions qui sont associés à des cas de découverte de sécurité Office 365 &amp; centre de conformité. Le rapport contient des informations telles que le nom du cas une suspension est associé avec les emplacements de contenu qui sont mis en attente et si la suspension est basée sur une requête. S’il existe des cas qui n’ont pas les suspensions, le script crée un rapport supplémentaire avec une liste des cas sans suspensions.

Voir la section [plus d’informations](#more-information) pour une description détaillée des informations incluses dans le rapport. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour générer un rapport sur tous les cas de découverte électronique dans votre organisation, vous devez être une administrateur de découverte électronique dans votre organisation. Si vous êtes un gestionnaire eDiscovery, le rapport inclut uniquement des informations sur les cas auquel vous pouvez accéder. Pour plus d’informations sur les autorisations de découverte électronique, consultez la rubrique [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
    
- Le script dans cet article présente un traitement minimale des erreurs. Le principal objectif consiste à créer rapidement des rapports sur les blocages qui sont associées dans les cas eDiscovery dans votre organisation.
    
- Les exemples de scripts fournis dans cette rubrique ne sont pas pris en charge par n’importe quel programme de prise en charge standard de Microsoft ou le service. Les exemples de scripts sont fournis en l’état sans aucune garantie. Microsoft exclut toute garantie implicite, y compris, sans limitation, une garantie implicite de qualité ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou les performances de la documentation et les exemples de scripts. En aucun cas Microsoft, ses auteurs ou toute autre impliqués dans la création, la production ou la remise des scripts est responsable de tout dommage que ce soit (y compris, sans limitation, pertes de bénéfices, interruption d’activité, la perte de informations professionnelles ou autre perte pécuniaire) résultant de l’utilisation ou l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été averti de la possibilité de tels dommages.
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a>Étape 1 : Connectez-vous à la sécurité &amp; centre de conformité à l’aide de PowerShell à distance

La première étape consiste à connecter Windows PowerShell pour la sécurité &amp; centre de conformité pour votre organisation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `ConnectSCC.ps1`. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script. 
    
3. Exécuter le script ; par exemple :

    ```
    .\ConnectSCC.ps1
    ```
   
4. Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>Étape 2 : Exécuter le script pour créer des rapports sur conserve associé au cas eDiscovery

Une fois que vous avez connecté à la sécurité &amp; centre de conformité avec PowerShell à distance, l’étape suivante consiste à créer et exécuter le script qui rassemble des informations sur les cas eDiscovery dans votre organisation. 
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, CaseHoldsReport.ps1. 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Office 365 Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" " 
#prompt users to specify a path to store the output files
$time=get-date
$Path = Read-Host 'Enter a file path to save the report to a .csv file'
$outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
$noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
#add case details to the csv file
function add-tocasereport{
Param([string]$casename,
[String]$casestatus,
[datetime]$casecreatedtime,
[string]$casemembers,
[datetime]$caseClosedDateTime,
[string]$caseclosedby,
[string]$holdname,
[String]$Holdenabled,
[string]$holdcreatedby,
[string]$holdlastmodifiedby,
[string]$ExchangeLocation,
[string]$sharePointlocation,
[string]$ContentMatchQuery,
[datetime]$holdcreatedtime,
[datetime]$holdchangedtime
)
$addRow = New-Object PSObject 
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
$allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
$allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii 
}
#get information on the cases and pass values to the case report function
" "
write-host "Gathering a list of cases and holds..."
" "
$edc =Get-ComplianceCase -ErrorAction SilentlyContinue
foreach($cc in $edc)
{
write-host "Working on case :" $cc.name
if($cc.status -eq 'Closed')
{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers 
}
else{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
$policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
if ($policies -ne $NULL)
{
foreach ($policy in $policies)
{
$rule=Get-CaseHoldRule -Policy $policy.name
add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
}
}
else{
write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
" "
[string]$cc.name | out-file -filepath $noholdsfilepath -append 
}
}
}

" "
Write-host "Script complete! Report files saved to this folder: '$Path'"
" "
#script end
  ```

2. Dans la session Windows PowerShell qui ouvert à l’étape 1, accédez au dossier où vous avez enregistré le script. 
    
3. Exécuter le script ; par exemple :

    ```
    .\CaseHoldsReport.ps1
    ```

    Le script vous invite à un dossier cible enregistrer l’état. 
    
4. Tapez le nom de chemin d’accès complet du dossier à l’enregistrement de l’état, puis appuyez sur **entrée**.
    
    > [!TIP]
    > Pour enregistrer le rapport dans le même dossier que le script se trouve dans, tapez un point («. ») lorsque vous y êtes invité pour un dossier cible. Pour enregistrer le rapport dans un sous-dossier dans le dossier où se trouve le script, il suffit de taper le nom du sous-dossier. 
  
    Le script commence à collecter des informations sur tous les cas de découverte électronique dans votre organisation. N’accédez pas au fichier de rapport pendant l’exécution du script. Une fois le script est terminé, un message de confirmation s’affiche dans la session Windows PowerShell. Une fois que ce message s’affiche, vous pouvez accéder au rapport dans le dossier que vous avez spécifié à l’étape 4. Est le nom de fichier pour le rapport `CaseHoldsReport<DateTimeStamp>.csv`.

    Plus, le script crée également un rapport avec une liste des cas qui n’ont pas les suspensions. Est le nom de fichier pour ce rapport `CaseswithNoHolds<DateTimeStamp>.csv`.
    
    Voici un exemple d’exécution du script CaseHoldsReport.ps1. 
    
    ![La sortie après avoir exécuté le script CaseHoldsReport.ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>Plus d'informations

Le cas contient l’état qui est créé lorsque vous exécutez le script dans cet article contient les informations suivantes sur chaque suspension. Comme expliqué précédemment, vous devez être une administrateur pour renvoyer des informations pour toutes les suspensions placées dans votre organisation eDiscovery. Pour plus d’informations sur le cas des blocages, voir [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md).
  
  - Nom de la suspension et le nom de la casse de découverte électronique qui est associée à la suspension.
    
  - Si le cas de découverte électronique est actif ou fermé.
    
  - La suspension est ou non activée ou désactivée.
    
  - Les membres de le cas de découverte électronique qui est associée à la suspension. Membres de l’incidents pour afficher ou gérer des cas, en fonction des autorisations eDiscovery qu'ils ont été attribué.
    
  - L’heure et la date de que création de la casse.
    
  - Si un cas est fermé, la personne qui a fermé il et l’heure et date a été fermée.
    
  - Les boîtes aux lettres Exchange et SharePoint sites emplacements qui sont en attente.
    
  - Si la suspension est basée sur les requêtes, la syntaxe de requête.
    
  - L’heure et date de que création de la suspension et la personne qui l’a créé.
    
  - L’heure et date de que dernière modification de la suspension et la personne qui a changé.
