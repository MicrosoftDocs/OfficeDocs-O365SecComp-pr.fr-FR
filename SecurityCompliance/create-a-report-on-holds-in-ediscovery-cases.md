---
title: Création d'un rapport sur les suspensions dans les cas de découverte électronique dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Utilisez le script de cet article pour générer un rapport qui contient des informations sur toutes les conservations associées à des cas eDiscovery dans le centre de conformité dans Office 365 ou Microsoft 365.
ms.openlocfilehash: db5a462087dd20ed71f87efe2fd83b821654f1b9
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000877"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Création d'un rapport sur les suspensions dans les cas de découverte électronique dans Office 365
  
Le script de cet article permet aux administrateurs eDiscovery et aux gestionnaires eDiscovery de générer un rapport contenant des informations sur toutes les suspensions associées à des cas eDiscovery dans le centre de conformité dans Office 365 ou Microsoft 365. Le rapport contient des informations telles que le nom du cas dans lequel une conservation est associée, les emplacements de contenu placés en conservation et si la suspension est basée sur une requête. S'il existe des cas qui n'ont aucune conservation, le script crée un rapport supplémentaire avec une liste de cas sans conservation.

Consultez la section [plus d'informations](#more-information) pour obtenir une description détaillée des informations incluses dans le rapport. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Pour générer un rapport sur tous les cas de découverte électronique dans votre organisation, vous devez être un administrateur de découverte électronique dans votre organisation. Si vous êtes un gestionnaire eDiscovery, le rapport n'inclut que les informations sur les cas accessibles. Pour plus d'informations sur les autorisations de découverte électronique, consultez la rubrique [attribution d'autorisations eDiscovery](assign-ediscovery-permissions.md).
    
- Le script de cet article a une gestion des erreurs minimale. L'objectif principal est de créer rapidement un rapport sur les conservations associées aux cas eDiscovery dans votre organisation.
    
- Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.
    
## <a name="step-1-connect-to-the-security--compliance-center-powershell"></a>Étape 1: Connectez-vous au centre de sécurité & Compliance Center PowerShell

La première étape consiste à vous connecter au centre de sécurité & Compliance pour votre organisation.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, `ConnectSCC.ps1`. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script. 
    
3. Exécutez le script; par exemple:

    ```
    .\ConnectSCC.ps1
    ```
   
4. Lorsque vous êtes invité à entrer vos informations d'identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>Étape 2: exécuter le script pour signaler les suspensions associées à des cas de découverte électronique

Une fois que vous êtes connecté au centre de sécurité & Compliance Center PowerShell, l'étape suivante consiste à créer et exécuter le script qui collecte des informations sur les cas eDiscovery dans votre organisation. 
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide d'un suffixe de nom de fichier. ps1; par exemple, CaseHoldsReport. ps1. 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
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

2. Dans la session Windows PowerShell qui s'est ouverte à l'étape 1, accédez au dossier où vous avez enregistré le script. 
    
3. Exécutez le script; par exemple:

    ```
    .\CaseHoldsReport.ps1
    ```

    Le script vous invite à entrer un dossier cible dans lequel enregistrer le rapport. 
    
4. Tapez le chemin d'accès complet du dossier dans lequel le rapport doit être enregistré, puis appuyez sur **entrée**.
    
    > [!TIP]
    > Pour enregistrer le rapport dans le dossier dans lequel se trouve le script, tapez un point («.») lorsque vous êtes invité à indiquer un dossier cible. Pour enregistrer le rapport dans un sous-dossier du dossier où se trouve le script, tapez simplement le nom du sous-dossier. 
  
    Le script commence à collecter des informations sur tous les cas de découverte électronique dans votre organisation. N'accédez pas au fichier de rapport pendant l'exécution du script. Une fois le script terminé, un message de confirmation s'affiche dans la session Windows PowerShell. Une fois ce message affiché, vous pouvez accéder au rapport dans le dossier que vous avez spécifié à l'étape 4. Le nom de fichier du rapport est `CaseHoldsReport<DateTimeStamp>.csv`.

    Plus, le script crée également un rapport avec une liste de cas qui n'ont aucune conservation. Le nom de fichier de ce rapport `CaseswithNoHolds<DateTimeStamp>.csv`est.
    
    Voici un exemple d'exécution du script CaseHoldsReport. ps1. 
    
    ![Sortie après l'exécution du script CaseHoldsReport. ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>Plus d’informations

Le rapport de suspension de cas qui est créé lorsque vous exécutez le script dans cet article contient les informations suivantes sur chaque blocage. Comme expliqué précédemment, vous devez être un administrateur eDiscovery pour renvoyer des informations pour toutes les suspensions de votre organisation. Pour plus d'informations sur les conservations d'incidents, consultez la rubrique [cas eDiscovery](ediscovery-cases.md).
  
  - Nom de la conservation et nom du cas eDiscovery auquel la conservation est associée.
    
  - Indique si le cas de découverte électronique est actif ou fermé.
    
  - Indique si la conservation est activée ou désactivée.
    
  - Membres du cas eDiscovery auquel est associée la conservation. Les membres de cas peuvent afficher ou gérer un cas, en fonction des autorisations eDiscovery auxquelles ils ont été affectés.
    
  - Date et heure de création de la demande de devis.
    
  - Si une demande de devis est fermée, la personne qui l'a fermée et l'heure et la date de clôture.
    
  - Les emplacements des boîtes aux lettres Exchange et des sites SharePoint en conservation.
    
  - Si la suspension est basée sur une requête, la syntaxe de requête.
    
  - L'heure et la date de création de la conservation et la personne qui l'a créée.
    
  - Date et heure de la dernière modification de la conservation et de la personne qui l'a modifiée.
