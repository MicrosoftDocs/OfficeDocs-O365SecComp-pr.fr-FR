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
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Utilisez le script dans cet article pour générer un rapport qui contient des informations sur toutes les suspensions qui sont associés à des cas de découverte de sécurité Office 365 &amp; centre de conformité.
ms.openlocfilehash: b6cef2824002d7e45e4f500bc6c1e9bc880cbd41
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038207"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="8df63-103">Créer un rapport sur les suspensions dans les cas eDiscovery dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8df63-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="8df63-p101">Le script dans cet article permet aux administrateurs de découverte électronique et gestionnaires de découverte électronique génèrent un rapport qui contient des informations sur toutes les suspensions qui sont associés à des cas de découverte de sécurité Office 365 &amp; centre de conformité. Le rapport contient des informations telles que le nom du cas une suspension est associé avec les emplacements de contenu qui sont mis en attente et si la suspension est basée sur une requête. S’il existe des cas qui n’ont pas les suspensions, le script crée un rapport supplémentaire avec une liste des cas sans suspensions.</span><span class="sxs-lookup"><span data-stu-id="8df63-p101">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the Office 365 Security &amp; Compliance Center. The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based. If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="8df63-107">Voir la section [plus d’informations](#more-information) pour une description détaillée des informations incluses dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="8df63-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="8df63-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8df63-108">Before you begin</span></span>

- <span data-ttu-id="8df63-p102">Pour générer un rapport sur tous les cas de découverte électronique dans votre organisation, vous devez être une administrateur de découverte électronique dans votre organisation. Si vous êtes un gestionnaire eDiscovery, le rapport inclut uniquement des informations sur les cas auquel vous pouvez accéder. Pour plus d’informations sur les autorisations de découverte électronique, consultez la rubrique [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8df63-p102">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization. If you are an eDiscovery Manager, the report will only include information about the cases that you can access. For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="8df63-p103">Le script dans cet article présente un traitement minimale des erreurs. Le principal objectif consiste à créer rapidement des rapports sur les blocages qui sont associées dans les cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8df63-p103">The script in this article has minimal error handling. The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="8df63-p104">Les exemples de script fournis dans cette rubrique ne sont pris en charge dans aucun programme de support ou service standard de Microsoft. Les exemples de scripts sont fournis en l’état, sans garantie d’aucune sorte. Microsoft exclut toute garantie implicite, y compris, sans limitation, les garanties implicites de qualité marchande ou d’adéquation à un usage particulier. Vous assumez tous les risques liés à l’utilisation ou à l’exécution des exemples de scripts et de la documentation. En aucun cas, Microsoft, ses auteurs ou toute personne impliquée dans la création, la production ou la livraison des scripts ne sont responsables de dommages quelconques (y compris, sans limitation, pertes de bénéfices, interruption d’activité, perte d’informations commerciales ou toute autre perte pécuniaire) découlant de l’utilisation ou de l’impossibilité d’utiliser les exemples de scripts ou la documentation, même si Microsoft a été informé de la possibilité de tels dommages.</span><span class="sxs-lookup"><span data-stu-id="8df63-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a><span data-ttu-id="8df63-119">Étape 1 : Connectez-vous à la sécurité &amp; centre de conformité à l’aide de PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="8df63-119">Step 1: Connect to the Security &amp; Compliance Center using Remote PowerShell</span></span>

<span data-ttu-id="8df63-120">La première étape consiste à connecter Windows PowerShell pour la sécurité &amp; centre de conformité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8df63-120">The first step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="8df63-121">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="8df63-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="8df63-122">Sur votre ordinateur local, ouvrez Windows PowerShell et accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="8df63-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="8df63-123">Exécuter le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="8df63-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="8df63-124">Lorsque vous y êtes invité vos informations d’identification, entrez votre adresse de messagerie et votre mot de passe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8df63-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="8df63-125">Étape 2 : Exécuter le script pour créer des rapports sur conserve associé au cas eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8df63-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="8df63-126">Une fois que vous avez connecté à la sécurité &amp; centre de conformité avec PowerShell à distance, l’étape suivante consiste à créer et exécuter le script qui rassemble des informations sur les cas eDiscovery dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8df63-126">After you've connected to the Security &amp; Compliance Center with remote PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="8df63-127">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1 ; par exemple, CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="8df63-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
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

2. <span data-ttu-id="8df63-128">Dans la session Windows PowerShell qui ouvert à l’étape 1, accédez au dossier où vous avez enregistré le script.</span><span class="sxs-lookup"><span data-stu-id="8df63-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="8df63-129">Exécuter le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="8df63-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="8df63-130">Le script vous invite à un dossier cible enregistrer l’état.</span><span class="sxs-lookup"><span data-stu-id="8df63-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="8df63-131">Tapez le nom de chemin d’accès complet du dossier à l’enregistrement de l’état, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="8df63-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="8df63-p105">Pour enregistrer le rapport dans le même dossier que le script se trouve dans, tapez un point («. ») lorsque vous y êtes invité pour un dossier cible. Pour enregistrer le rapport dans un sous-dossier dans le dossier où se trouve le script, il suffit de taper le nom du sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="8df63-p105">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder. To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="8df63-p106">Le script commence à collecter des informations sur tous les cas de découverte électronique dans votre organisation. N’accédez pas au fichier de rapport pendant l’exécution du script. Une fois le script est terminé, un message de confirmation s’affiche dans la session Windows PowerShell. Une fois que ce message s’affiche, vous pouvez accéder au rapport dans le dossier que vous avez spécifié à l’étape 4. Est le nom de fichier pour le rapport `CaseHoldsReport<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="8df63-p106">The script starts to collect information about all the eDiscovery cases in your organization. Don't access the report file while the script is running. After the script is complete, a confirmation message is displayed in the Windows PowerShell session. After this message is displayed, you can access the report in the folder that you specified in Step 4. The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="8df63-p107">Plus, le script crée également un rapport avec une liste des cas qui n’ont pas les suspensions. Est le nom de fichier pour ce rapport `CaseswithNoHolds<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="8df63-p107">Addtionally, the script also creates a report with a list of cases that don't have any holds. The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="8df63-141">Voici un exemple d’exécution du script CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="8df63-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![La sortie après avoir exécuté le script CaseHoldsReport.ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="8df63-143">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="8df63-143">More information</span></span>

<span data-ttu-id="8df63-p108">Le cas contient l’état qui est créé lorsque vous exécutez le script dans cet article contient les informations suivantes sur chaque suspension. Comme expliqué précédemment, vous devez être une administrateur pour renvoyer des informations pour toutes les suspensions placées dans votre organisation eDiscovery. Pour plus d’informations sur le cas des blocages, voir [cas eDiscovery de sécurité Office 365 &amp; centre de conformité](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="8df63-p108">The case holds report that's created when you run the script in this article contains the following information about each hold. As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization. For more information about case holds, see [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="8df63-147">Nom de la suspension et le nom de la casse de découverte électronique qui est associée à la suspension.</span><span class="sxs-lookup"><span data-stu-id="8df63-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="8df63-148">Si le cas de découverte électronique est actif ou fermé.</span><span class="sxs-lookup"><span data-stu-id="8df63-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="8df63-149">La suspension est ou non activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="8df63-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="8df63-p109">Les membres de le cas de découverte électronique qui est associée à la suspension. Membres de l’incidents pour afficher ou gérer des cas, en fonction des autorisations eDiscovery qu'ils ont été attribué.</span><span class="sxs-lookup"><span data-stu-id="8df63-p109">The members of the eDiscovery case that the hold is associated with. Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="8df63-152">L’heure et la date de que création de la casse.</span><span class="sxs-lookup"><span data-stu-id="8df63-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="8df63-153">Si un cas est fermé, la personne qui a fermé il et l’heure et date a été fermée.</span><span class="sxs-lookup"><span data-stu-id="8df63-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="8df63-154">Les boîtes aux lettres Exchange et SharePoint sites emplacements qui sont en attente.</span><span class="sxs-lookup"><span data-stu-id="8df63-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="8df63-155">Si la suspension est basée sur les requêtes, la syntaxe de requête.</span><span class="sxs-lookup"><span data-stu-id="8df63-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="8df63-156">L’heure et date de que création de la suspension et la personne qui l’a créé.</span><span class="sxs-lookup"><span data-stu-id="8df63-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="8df63-157">L’heure et date de que dernière modification de la suspension et la personne qui a changé.</span><span class="sxs-lookup"><span data-stu-id="8df63-157">The time and date the hold was last changed and the person who changed it.</span></span>
