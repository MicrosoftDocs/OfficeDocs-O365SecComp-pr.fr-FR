---
title: Donner aux utilisateurs l’accès à la la sécurité d’Office 365 &amp; centre de conformité
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Les utilisateurs doivent être affectées des autorisations de sécurité Office 365 &amp; centre de conformité avant qu’ils peuvent gérer une de ses fonctionnalités de sécurité ou de conformité.
ms.openlocfilehash: 5055c64d914e15a6570c339ade48bb8f7e802ea7
ms.sourcegitcommit: a56fa2e184a2662fd8a7881ccea0891e9a26d497
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "27221065"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Donner aux utilisateurs l’accès à la la sécurité d’Office 365 &amp; centre de conformité

Les utilisateurs doivent être affectées des autorisations de sécurité Office 365 &amp; centre de conformité avant qu’ils peuvent gérer une de ses fonctionnalités de sécurité ou de conformité. En tant qu’administrateur global d’Office 365 ou membre du groupe de rôles de sécurité OrganizationManagement &amp; centre de conformité, vous pouvez attribuer ces autorisations aux utilisateurs. Les utilisateurs ne seront en mesure de gérer les fonctionnalités de sécurité ou de conformité que vous leur accordez l’accès. 
  
Pour plus d’informations sur les différentes autorisations que vous pouvez donner aux utilisateurs de la sécurité &amp; centre de conformité, extraction [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Vous devez être un administrateur global d’Office 365, ou un membre du groupe de rôles de sécurité OrganizationManagement &amp; centre de conformité, pour effectuer les étapes décrites dans cet article.
    
- Groupes de rôles de sécurité &amp; centre de conformité peut avoir des noms similaires pour les groupes de rôles dans Exchange Online, mais ils ne sont pas identiques. 
    
- Appartenances aux groupes de rôles ne sont pas partagés entre Exchange Online et de la sécurité &amp; centre de conformité.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Utiliser le centre d’administration Office 365 pour donner un autre utilisateur l’accès à la sécurité &amp; centre de conformité

1. [Se connecter à Office 365 et accédez au centre d’administration](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
2. Dans le centre d’administration Office 365, ouvrez le **Centre d’administration** , puis sur **sécurité &amp; conformité**. 
    
3. Dans la sécurité &amp; centre de conformité, accédez à **autorisations**.
    
4. Dans la liste, sélectionnez le groupe de rôles que vous souhaitez ajouter l’utilisateur, cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
5. Dans la page de propriétés du groupe de rôles sous **membres**, cliquez sur **Ajouter**![ajouter une icône](media/ITPro-EAC-AddIcon.gif) et sélectionnez le nom de l’utilisateur (ou utilisateurs) que vous souhaitez ajouter. 
    
6. Lorsque vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur **Ajouter-\> ** , puis **OK**.
    
7. Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles. 
    
### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

1. Dans la sécurité &amp; centre de conformité, accédez à **autorisations**.
    
2. Dans la liste, sélectionnez le groupe de rôles pour afficher les membres.
    
3. Sur la droite, dans les détails de groupe de rôles, vous pouvez afficher les membres du groupe de rôles.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Utiliser PowerShell pour donner un autre utilisateur l’accès à la sécurité &amp; centre de conformité

1. [Se connecter à Office 365 sécurité & PowerShell du centre de conformité](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).
    
2. Utilisez la commande **Add-RoleGroupMember** pour ajouter un utilisateur au rôle Gestion de l’organisation, comme illustré dans l’exemple suivant. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Paramètres**
  
- _-Identity_ est le groupe de rôles auquel ajouter un membre. 
    
- _Membre_ est la boîte aux lettres, le groupe de sécurité universel (USG) ou d’ordinateur à ajouter au groupe de rôles. Vous pouvez spécifier qu’un seul membre à la fois. 
    
Pour plus d’informations sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vérifier que vous avez accordé aux utilisateurs accès à la sécurité &amp; centre de conformité, utilisez l’applet de commande **Get-RoleGroupMember** permet d’afficher les membres dans le groupe de rôles de gestion de l’organisation, comme illustré dans l’exemple suivant. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Pour plus d’informations sur la syntaxe et les paramètres, voir [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  

