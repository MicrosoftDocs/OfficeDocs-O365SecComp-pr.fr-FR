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
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a>Obtenir plus d’informations sur les périphériques gérés par Mobile Device Management (MDM) pour Office 365

Cet article explique comment utiliser Windows PowerShell pour obtenir plus d’informations sur les périphériques de votre organisation que vous avez définie pour la gestion des périphériques mobiles pour Office 365. 
  
## <a name="what-device-details-can-i-get"></a>Les détails de l’appareil puis-je obtenir ?

Voici une répartition.
  
|**Détails**|**Ce que vous recherchez dans PowerShell**|
|:-----|:-----|
|Périphérique est [inscrit dans Mobile Device Manager pour Office 365](enroll-your-mobile-device.md) <br/> |La valeur du paramètre *isManaged* est :  <br/> **True** = périphérique est inscrit.  <br/> **False** = périphérique n’est pas inscrit.  <br/> |
|Périphérique est compatible avec vos [stratégies de sécurité des périphériques](https://go.microsoft.com/fwlink/?linkid=615144) <br/> |La valeur du paramètre *isCompliant* est :  <br/> **True** = périphérique est conforme aux stratégies.  <br/> **False** = périphérique n’est pas compatible avec les stratégies.  <br/> |
   
![Flux affichant des valeurs de paramètre Shell DAS pour que les périphériques sont inscrits et réclamation](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> Les commandes et les scripts dans cet article renvoie également plus d’informations sur les périphériques qui sont gérés par [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune). 
  
## <a name="before-you-begin"></a>Avant de commencer

Il existe quelques points que vous devrez configuré pour exécuter les commandes et les scripts décrits dans cet article.
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a>Étape 1 : Télécharger et installer le Azure Active Directory Module pour Windows PowerShell

Pour plus d’informations sur ces étapes, voir [se connecter à Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).
  
1. Accédez à [Microsoft Online Services Assistant de connexion pour les professionnels de l’informatique RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) et cliquez sur **Télécharger** pour l’Assistant de connexion Microsoft Online Services. 
    
2. Installer le Microsoft Azure Active Directory Module pour Windows PowerShell en suivant ces étapes :
    
    1. Ouvrez une invite de commandes PowerShell au niveau administrateur.
        
    2. Exécuter le `Install-Module MSOnline` commande.
        
    3. Si vous y êtes invité à installer le fournisseur NuGet, tapez `Y` et appuyez sur ENTRÉE.
        
    4. Si vous y êtes invité à installer le module de PSGallery, tapez `Y` et appuyez sur ENTRÉE.
        
    5. Après l’installation, fermez la fenêtre de commande PowerShell.
    
### <a name="step-2-connect-to-your-office-365-subscription"></a>Étape 2 : Se connecter à votre abonnement Office 365

1. Dans Windows Azure Active Directory Module pour Windows PowerShell, exécutez la commande suivante.</br>  
  `$UserCredential = Get-Credential`

2. Dans la boîte de dialogue **Demande d’informations d’identification Windows PowerShell** , tapez le nom d’utilisateur et le mot de passe de votre compte d’administrateur global Office 365, puis cliquez sur **OK**.
    
3. Exécutez la commande suivante.</br>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a>Étape 3 : Vérifiez que vous êtes en mesure d’exécuter des scripts PowerShell

> [!NOTE]
> Vous pouvez ignorer cette étape si vous avez déjà configuré pour exécuter des scripts PowerShell. 
  
Pour exécuter le script **Get-MsolUserDeviceComplianceStatus.ps1** , vous devez activer l’exécution de scripts PowerShell. 
  
1. À partir de votre bureau Windows, cliquez sur **Démarrer**, puis tapez Windows PowerShell. Cliquez avec le bouton droit sur **Windows PowerShell**, puis cliquez sur **Exécuter en tant qu’administrateur**.
    
2. Exécutez la commande suivante.</br>
  `Set-ExecutionPolicy RemoteSigned`

3. Lorsque vous y êtes invité, tapez `Y` , puis appuyez sur ENTRÉE. 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a>Exécutez l’applet de commande Get-MsolDevice pour afficher les détails de tous les périphériques de votre organisation

1. Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.
    
2. Exécutez la commande suivante.</br>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

Pour plus d’exemples, voir [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).
  
## <a name="run-a-script-to-get-device-details"></a>Exécuter un script pour obtenir des détails de l’appareil

### <a name="first-save-the-script-to-your-computer"></a>Tout d’abord, enregistrez le script sur votre ordinateur

1. Copiez et collez le texte suivant dans le bloc-notes.</br> 
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

2. Enregistrez-le dans un fichier de script Windows PowerShell à l’aide de l’extension de fichier **.ps1**. </br>Exemple :</br> `Get-MsolUserDeviceComplianceStatus.ps1`.
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a>Exécutez le script pour obtenir des informations de périphérique pour un compte d’utilisateur unique

1. Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.
    
2. Accédez au dossier où vous avez enregistré le script. Par exemple, si vous l’aviez enregistré à C:\PS-Scripts, vous exécuterez la commande suivante.</br>
    `cd C:\PS-Scripts`

3. Exécutez la commande suivante pour identifier l’utilisateur que vous souhaitez obtenir des détails de l’appareil pour. Cet exemple obtient les détails pour bar@example.com.</br>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. Exécutez la commande suivante pour lancer le script.</br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Les informations sont exportées sur votre bureau Windows dans un fichier CSV. Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et chemin d’accès de la CSV.
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a>Exécuter le script pour obtenir des informations sur le périphérique pour un groupe d’utilisateurs

1. Ouvrez le Module Microsoft Azure Active Directory pour Windows PowerShell.
    
2. Accédez au dossier où vous avez enregistré le script. Par exemple, si vous l’aviez enregistré à C:\PS-Scripts, vous exécuterez la commande suivante.</br>
  `cd C:\PS-Scripts`

3. Exécutez la commande suivante pour identifier le groupe que vous souhaitez obtenir des détails de l’appareil pour. Cet exemple obtient les détails pour les utilisateurs dans le groupe FinanceStaff.</br>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. Exécutez la commande suivante pour lancer le script.</br>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Les informations sont exportées sur votre bureau Windows dans un fichier CSV. Vous pouvez utiliser des paramètres supplémentaires pour spécifier le nom de fichier et chemin d’accès de la CSV.
  
## <a name="more-info"></a>Plus d'informations

[Vue d’ensemble de Mobile Device Manager pour Office 365](overview-of-mdm.md)
  
[Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)
  

