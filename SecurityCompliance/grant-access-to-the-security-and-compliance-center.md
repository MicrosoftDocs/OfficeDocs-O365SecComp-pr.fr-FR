---
title: Donner aux utilisateurs l'accès au centre de &amp; sécurité conformité Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Les utilisateurs doivent disposer d'autorisations dans le centre de sécurité &amp; conformité Office 365 avant de pouvoir gérer les fonctionnalités de sécurité ou de conformité.
ms.openlocfilehash: 0a3f0d1ddde7d269a0f8f9596c5c3de14e94429d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216304"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a>Donner aux utilisateurs l'accès au centre de &amp; sécurité conformité Office 365

Les utilisateurs doivent disposer d'autorisations dans le centre de sécurité &amp; conformité Office 365 avant de pouvoir gérer les fonctionnalités de sécurité ou de conformité. En tant qu'administrateur général Office 365 ou membre du groupe de rôles OrganizationManagement dans le &amp; Centre de sécurité conformité, vous pouvez accorder ces autorisations aux utilisateurs. Les utilisateurs pourront uniquement gérer les fonctionnalités de sécurité ou de conformité auxquelles vous leur accordez accès. 
  
Pour plus d'informations sur les différentes autorisations que vous pouvez accorder aux utilisateurs dans &amp; le centre de sécurité conformité, consultez [la rubrique autorisations dans &amp; le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Vous devez être un administrateur général Office 365 ou un membre du groupe de rôles OrganizationManagement dans le centre de sécurité &amp; conformité pour effectuer les étapes décrites dans cet article.
    
- Les groupes de rôles pour &amp; le centre de sécurité conformité peuvent avoir des noms similaires aux groupes de rôles dans Exchange Online, mais ils ne sont pas identiques. 
    
- Les appartenances aux groupes de rôles ne sont pas partagées &amp; entre Exchange Online et le centre de sécurité conformité.
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Utiliser le centre d'administration Office 365 pour donner à un autre utilisateur l' &amp; accès au centre de sécurité conformité

1. [Connectez-vous à Office 365 et accédez au centre d'administration](https://go.microsoft.com/fwlink/p/?LinkId=525275).
    
2. Dans le centre d'administration Office 365, ouvrez **centres** d'administration, puis cliquez sur **conformité de sécurité &amp; **. 
    
3. Dans le centre &amp; de sécurité conformité, accédez à **autorisations**.
    
4. Dans la liste, choisissez le groupe de rôles auquel vous souhaitez ajouter l'utilisateur, puis cliquez sur **modifier** ![l'](media/O365_MDM_CreatePolicy_EditIcon.gif)icône modifier.
    
5. Dans la page des propriétés du groupe de rôles sous **membres**, cliquez sur](media/ITPro-EAC-AddIcon.gif) **Ajouter**![une icône et sélectionnez le nom de l'utilisateur (ou des utilisateurs) que vous souhaitez ajouter. 
    
6. Une fois que vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur **ajouter-\> ** puis sur **OK**.
    
7. Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles. 
    
### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

1. Dans le centre &amp; de sécurité conformité, accédez à **autorisations**.
    
2. Dans la liste, sélectionnez le groupe de rôles pour afficher les membres.
    
3. À droite, dans les détails du groupe de rôles, vous pouvez afficher les membres du groupe de rôles.
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a>Utiliser PowerShell pour donner à un autre utilisateur l'accès &amp; au centre de sécurité conformité

1. [Connectez-vous au centre de sécurité & de la sécurité d'Office 365 PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).
    
2. Utilisez la commande **Add-RoleGroupMember** pour ajouter un utilisateur au rôle Gestion de l’organisation, comme illustré dans l’exemple suivant. 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 **Paramètres**
  
- _-Identity_ est le groupe de rôles auquel ajouter un membre. 
    
- _Membre_ est la boîte aux lettres, le groupe de sécurité universel ou l'ordinateur à ajouter au groupe de rôles. Vous ne pouvez spécifier qu'un seul membre à la fois. 
    
Pour plus d'informations sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vérifier que vous avez accordé aux utilisateurs l'accès au &amp; Centre de sécurité conformité, utilisez la cmdlet **Get-RoleGroupMember** pour afficher les membres du groupe de rôles gestion de l'organisation, comme illustré dans l'exemple suivant. 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

Pour plus d'informations sur la syntaxe et les paramètres, consultez la rubrique [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
  

