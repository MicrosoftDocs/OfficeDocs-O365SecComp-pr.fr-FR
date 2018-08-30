---
title: Obtenir plus d’informations sur les périphériques gérés par Mobile Device Management (MDM) pour Office 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MBS150
- MET150
ms.assetid: 5602963c-a1f2-4c21-afb9-f66cd7dca1f0
description: Cet article explique comment utiliser Windows PowerShell pour obtenir plus d’informations sur les périphériques de votre organisation que vous avez définie pour la gestion des périphériques mobiles pour Office 365.
ms.openlocfilehash: 2e406d3583e7892531b7c74bef0db374672956c7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272529"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="7c20f-103">Obtenir plus d’informations sur les périphériques gérés par Mobile Device Management (MDM) pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7c20f-103">Get details about devices managed by Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="7c20f-104">Cet article explique comment utiliser Windows PowerShell pour obtenir plus d’informations sur les périphériques de votre organisation que vous avez définie pour la gestion des périphériques mobiles pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="7c20f-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Mobile Device Management for Office 365.</span></span> 
  
## <a name="what-device-details-can-i-get"></a><span data-ttu-id="7c20f-105">Les détails de l’appareil puis-je obtenir ?</span><span class="sxs-lookup"><span data-stu-id="7c20f-105">What device details can I get?</span></span>

<span data-ttu-id="7c20f-106">Voici une répartition.</span><span class="sxs-lookup"><span data-stu-id="7c20f-106">Here's a breakdown.</span></span>
  
|<span data-ttu-id="7c20f-107">**Détails**</span><span class="sxs-lookup"><span data-stu-id="7c20f-107">**Detail**</span></span>|<span data-ttu-id="7c20f-108">**Ce que vous recherchez dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="7c20f-108">**What to look for in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c20f-109">Périphérique est [inscrit dans Mobile Device Manager pour Office 365](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="7c20f-109">Device is [enrolled in MDM for Office 365](enroll-your-mobile-device.md)</span></span> <br/> |<span data-ttu-id="7c20f-110">La valeur du paramètre *isManaged* est :</span><span class="sxs-lookup"><span data-stu-id="7c20f-110">The value of the  *isManaged*  parameter is:</span></span>  <br/> <span data-ttu-id="7c20f-111">**True** = périphérique est inscrit.</span><span class="sxs-lookup"><span data-stu-id="7c20f-111">**True** = device is enrolled.</span></span>  <br/> <span data-ttu-id="7c20f-112">**False** = périphérique n’est pas inscrit.</span><span class="sxs-lookup"><span data-stu-id="7c20f-112">**False** = device is not enrolled.</span></span>  <br/> |
|<span data-ttu-id="7c20f-113">Périphérique est compatible avec vos [stratégies de sécurité des périphériques](https://go.microsoft.com/fwlink/?linkid=615144)</span><span class="sxs-lookup"><span data-stu-id="7c20f-113">Device is compliant with your [device security policies](https://go.microsoft.com/fwlink/?linkid=615144)</span></span> <br/> |<span data-ttu-id="7c20f-114">La valeur du paramètre *isCompliant* est :</span><span class="sxs-lookup"><span data-stu-id="7c20f-114">The value of the  *isCompliant*  parameter is:</span></span>  <br/> <span data-ttu-id="7c20f-115">**True** = périphérique est conforme aux stratégies.</span><span class="sxs-lookup"><span data-stu-id="7c20f-115">**True** = device is compliant with policies.</span></span>  <br/> <span data-ttu-id="7c20f-116">**False** = périphérique n’est pas compatible avec les stratégies.</span><span class="sxs-lookup"><span data-stu-id="7c20f-116">**False** = device is not compliant with policies.</span></span>  <br/> |
   
![Flux affichant des valeurs de paramètre Shell DAS pour que les périphériques sont inscrits et réclamation](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> <span data-ttu-id="7c20f-118">Les commandes et les scripts dans cet article renvoie également plus d’informations sur les périphériques qui sont gérés par [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="7c20f-118">The commands and scripts in this article will also return details about any devices that are managed by [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="7c20f-119">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7c20f-119">Before you begin</span></span>

<span data-ttu-id="7c20f-120">Il existe quelques points que vous devrez configuré pour exécuter les commandes et les scripts décrits dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7c20f-120">There are a few things you'll need to set up to run the commands and scripts described in this article.</span></span>
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="7c20f-121">Étape 1 : Télécharger et installer le Azure Active Directory Module pour Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c20f-121">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="7c20f-122">Pour plus d’informations sur ces étapes, voir [se connecter à Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="7c20f-122">For more info on these steps, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>
  
1. <span data-ttu-id="7c20f-123">Accédez à [Microsoft Online Services Assistant de connexion pour les professionnels de l’informatique RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) et cliquez sur **Télécharger** pour l’Assistant de connexion Microsoft Online Services.</span><span class="sxs-lookup"><span data-stu-id="7c20f-123">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) and click **Download** for Microsoft Online Services Sign-in Assistant.</span></span> 
    
2. <span data-ttu-id="7c20f-124">Installer le Microsoft Azure Active Directory Module pour Windows PowerShell en suivant ces étapes :</span><span class="sxs-lookup"><span data-stu-id="7c20f-124">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>
    
    1. <span data-ttu-id="7c20f-125">Ouvrez une invite de commandes PowerShell au niveau administrateur.</span><span class="sxs-lookup"><span data-stu-id="7c20f-125">Open an administrator-level PowerShell command prompt.</span></span>
        
    2. <span data-ttu-id="7c20f-126">Exécuter le `Install-Module MSOnline` commande.</span><span class="sxs-lookup"><span data-stu-id="7c20f-126">Run the `Install-Module MSOnline` command.</span></span>
        
    3. <span data-ttu-id="7c20f-127">Si vous y êtes invité à installer le fournisseur NuGet, tapez `Y` et appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="7c20f-127">If prompted to install the NuGet provider, type `Y` and press ENTER.</span></span>
        
    4. <span data-ttu-id="7c20f-128">Si vous y êtes invité à installer le module de PSGallery, tapez `Y` et appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="7c20f-128">If prompted to install the module from PSGallery, type `Y` and press ENTER.</span></span>
        
    5. <span data-ttu-id="7c20f-129">Après l’installation, fermez la fenêtre de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-129">After installation, close the PowerShell command window.</span></span>
    
### <a name="step-2-connect-to-your-office-365-subscription"></a><span data-ttu-id="7c20f-130">Étape 2 : Se connecter à votre abonnement Office 365</span><span class="sxs-lookup"><span data-stu-id="7c20f-130">Step 2: Connect to your Office 365 subscription</span></span>

1. <span data-ttu-id="7c20f-131">Dans Windows Azure Active Directory Module pour Windows PowerShell, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-131">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span></br>  
  `$UserCredential = Get-Credential`

2. <span data-ttu-id="7c20f-132">Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell** , tapez le nom d’utilisateur et le mot de passe de votre compte d’administrateur global Office 365, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c20f-132">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="7c20f-133">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-133">Run the following command.</span></span></br>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="7c20f-134">Étape 3 : Vérifiez que vous êtes en mesure d’exécuter des scripts PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c20f-134">Step 3: Make sure you're able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="7c20f-135">Vous pouvez ignorer cette étape si vous avez déjà configuré pour exécuter des scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-135">You can skip this step if you're already set up to run PowerShell scripts.</span></span> 
  
<span data-ttu-id="7c20f-136">Pour exécuter le script **Get-MsolUserDeviceComplianceStatus.ps1** , vous devez activer l’exécution de scripts PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-136">To run the **Get-MsolUserDeviceComplianceStatus.ps1** script, you need to enable the running of PowerShell scripts.</span></span> 
  
1. <span data-ttu-id="7c20f-p101">À partir de votre bureau Windows, cliquez sur **Démarrer**, puis tapez Windows PowerShell. Cliquez avec le bouton droit sur **Windows PowerShell**, puis cliquez sur **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p101">From your Windows Desktop, click **Start**, and then type Windows PowerShell. Right click **Windows PowerShell**, and then click **Run as administrator**.</span></span>
    
2. <span data-ttu-id="7c20f-139">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-139">Run the following command.</span></span></br>
  `Set-ExecutionPolicy RemoteSigned`

3. <span data-ttu-id="7c20f-140">Lorsque vous y êtes invité, tapez `Y` , puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="7c20f-140">When prompted, type `Y` and then press Enter.</span></span> 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="7c20f-141">Exécutez l’applet de commande Get-MsolDevice pour afficher les détails de tous les périphériques de votre organisation</span><span class="sxs-lookup"><span data-stu-id="7c20f-141">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="7c20f-142">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-142">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="7c20f-143">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-143">Run the following command.</span></span></br>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

<span data-ttu-id="7c20f-144">Pour plus d’exemples, voir [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span><span class="sxs-lookup"><span data-stu-id="7c20f-144">For more examples, see [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span></span>
  
## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="7c20f-145">Exécuter un script pour obtenir des détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="7c20f-145">Run a script to get device details</span></span>

### <a name="first-save-the-script-to-your-computer"></a><span data-ttu-id="7c20f-146">Tout d’abord, enregistrez le script sur votre ordinateur</span><span class="sxs-lookup"><span data-stu-id="7c20f-146">First, save the script to your computer</span></span>

1. <span data-ttu-id="7c20f-147">Copiez et collez le texte suivant dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="7c20f-147">Copy and paste the following text into Notepad.</span></span></br> 
  ```
  param (
      [PSObject[]]$users = @(),
      [Switch]$export,
      [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
      [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
  [System.Collections.IDictionary]$script:schema = @{
      
      DeviceId = ''
      DeviceOSType = ''
      DeviceOSVersion = ''
      DeviceTrustLevel = ''
      DisplayName = ''
      IsCompliant = ''
      IsManaged = ''
      ApproximateLastLogonTimestamp = ''
      DeviceObjectId = ''    
      RegisteredOwnerUpn = ''
      RegisteredOwnerObjectId = ''
      RegisteredOwnerDisplayName = ''
  }
  function createResultObject
  {
      [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
      return $resultObject
  }
  If ($users.Count -eq 0)
  {
      $users = Get-MsolUser
  }
  [PSObject[]]$result = foreach ($u in $users)
  {
      
      [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
      foreach ($d in $devices)
      {
          [PSObject]$deviceResult = createResultObject
          $deviceResult.DeviceId = $d.DeviceId 
          $deviceResult.DeviceOSType = $d.DeviceOSType 
          $deviceResult.DeviceOSVersion = $d.DeviceOSVersion 
          $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
          $deviceResult.DisplayName = $d.DisplayName
          $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
          $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
          $deviceResult.DeviceObjectId = $d.ObjectId
          $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
          $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
          $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
          $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
          $deviceResult
      }
  }
  If ($export)
  {
      $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
  }
  Else
  {
      $result
  }
  
  ```

2. <span data-ttu-id="7c20f-148">Enregistrez-le dans un fichier de script Windows PowerShell à l’aide de l’extension de fichier **.ps1**.</span><span class="sxs-lookup"><span data-stu-id="7c20f-148">Save it as a Windows PowerShell script file by using the file extension **.ps1**.</span></span> </br><span data-ttu-id="7c20f-149">Exemple :</span><span class="sxs-lookup"><span data-stu-id="7c20f-149">Example:</span></span></br> <span data-ttu-id="7c20f-150">`Get-MsolUserDeviceComplianceStatus.ps1`.</span><span class="sxs-lookup"><span data-stu-id="7c20f-150"></span></span>
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="7c20f-151">Exécutez le script pour obtenir des informations de périphérique pour un compte d’utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="7c20f-151">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="7c20f-152">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-152">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="7c20f-p102">Accédez au dossier où vous avez enregistré le script. Par exemple, si vous l’aviez enregistré à C:\PS-Scripts, vous exécuterez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p102">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
    `cd C:\PS-Scripts`

3. <span data-ttu-id="7c20f-p103">Exécutez la commande suivante pour identifier l’utilisateur que vous souhaitez obtenir des détails de l’appareil pour. Cet exemple obtient les détails pour bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p103">Run the following command to identify the user you want to get device details for. This example gets details for bar@example.com.</span></span></br>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. <span data-ttu-id="7c20f-157">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="7c20f-157">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="7c20f-p104">Les informations sont exportées sur votre bureau Windows dans un fichier CSV. Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et chemin d’accès de la CSV.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p104">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="7c20f-160">Exécuter le script pour obtenir des informations sur le périphérique pour un groupe d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7c20f-160">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="7c20f-161">Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c20f-161">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="7c20f-p105">Accédez au dossier où vous avez enregistré le script. Par exemple, si vous l’aviez enregistré à C:\PS-Scripts, vous exécuterez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p105">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span></br>
  `cd C:\PS-Scripts`

3. <span data-ttu-id="7c20f-p106">Exécutez la commande suivante pour identifier le groupe que vous souhaitez obtenir des détails de l’appareil pour. Cet exemple obtient les détails pour les utilisateurs dans le groupe FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p106">Run the following command to identify the group you want to get device details for. This example gets details for users in the FinanceStaff group.</span></span></br>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. <span data-ttu-id="7c20f-166">Exécutez la commande suivante pour lancer le script.</span><span class="sxs-lookup"><span data-stu-id="7c20f-166">Run the following command to initiate the script.</span></span></br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="7c20f-p107">Les informations sont exportées sur votre bureau Windows dans un fichier CSV. Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et chemin d’accès de la CSV.</span><span class="sxs-lookup"><span data-stu-id="7c20f-p107">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
## <a name="more-info"></a><span data-ttu-id="7c20f-169">Plus d'informations</span><span class="sxs-lookup"><span data-stu-id="7c20f-169">More info</span></span>

[<span data-ttu-id="7c20f-170">Vue d’ensemble de Mobile Device Manager pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7c20f-170">Overview of MDM for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="7c20f-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="7c20f-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=841721)
  

