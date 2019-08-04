---
title: Octroi de l’accès au Centre de conformité et sécurité Office 365 aux utilisateurs
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
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
description: Les utilisateurs doivent disposer d’autorisations dans le centre de conformité Office 365 Security & pour pouvoir gérer les fonctionnalités de sécurité ou de conformité.
ms.openlocfilehash: ea774648efcfe80461eae937f80856acaf1db224
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35792010"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a>Octroi de l’accès au Centre de conformité et sécurité Office 365 aux utilisateurs

Les utilisateurs doivent disposer d’autorisations dans le centre de conformité Office 365 Security & pour pouvoir gérer les fonctionnalités de sécurité ou de conformité. En tant qu’administrateur général Office 365 ou membre du groupe de rôles OrganizationManagement dans le centre de sécurité & conformité, vous pouvez accorder ces autorisations aux utilisateurs. Ceux-ci pourront uniquement gérer les fonctionnalités de sécurité ou de conformité auxquelles vous leur donnez accès. 
  
Pour plus d’informations sur les différentes autorisations que vous pouvez accorder aux utilisateurs dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité Office 365](permissions-in-the-security-and-compliance-center.md).
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer

- Vous devez être un administrateur général Office 365 ou un membre du groupe de rôles OrganizationManagement dans le centre de sécurité & Compliance Center pour effectuer les étapes décrites dans cet article.

- Les groupes de rôles pour le centre de sécurité & conformité peuvent avoir des noms similaires aux groupes de rôles dans Exchange Online, mais ils ne sont pas identiques.

- Les appartenances aux groupes de rôles ne sont pas partagées entre Exchange Online et le centre de sécurité & conformité.

- Les autorisations des partenaires DAP (Delegated Access permission) avec administrer de la part de (administrateur) ne peuvent pas accéder au centre de conformité &.

## <a name="use-the-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a>Utiliser le centre d’administration pour accorder à un autre utilisateur l’accès au centre de sécurité & conformité

1. [Connectez-vous à Office 365 et accédez au centre d’administration](https://go.microsoft.com/fwlink/p/?LinkId=525275).

2. Dans le centre d’administration 365 de Microsoft, ouvrez **centres d’administration** , puis cliquez sur **sécurité & conformité**.

3. Dans le centre de sécurité & conformité, accédez à **autorisations**.

4. Dans la liste, choisissez le groupe de rôles auquel vous souhaitez ajouter l’utilisateur, puis cliquez sur **modifier** ![l'](media/O365-MDM-CreatePolicy-EditIcon.gif)icône modifier.

5. Dans la page des propriétés du groupe de rôles sous **membres**, cliquez sur](media/ITPro-EAC-AddIcon.gif) **Ajouter**![une icône et sélectionnez le nom de l’utilisateur (ou des utilisateurs) que vous souhaitez ajouter.

6. Une fois que vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur **ajouter-\> ** puis sur **OK**.

7. Cliquez sur **Enregistrer** pour enregistrer les modifications apportées au groupe de rôles.

### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

1. Dans le centre de sécurité & conformité, accédez à **autorisations**.

2. Dans la liste, sélectionnez le groupe de rôles pour afficher les membres.

3. À droite, dans les détails du groupe de rôles, vous pouvez afficher les membres du groupe de rôles.

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a>Utiliser PowerShell pour donner à un autre utilisateur l’accès au centre de sécurité & conformité

1. [Connectez-vous au centre de sécurité & conformité d’Office 365 PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Utilisez la commande **Add-RoleGroupMember** pour ajouter un utilisateur au rôle Gestion de l’organisation, comme illustré dans l’exemple suivant.

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   **Paramètres**:
  
   - _Identity_ est le groupe de rôles auquel ajouter un membre.

   - _Membre_ est la boîte aux lettres, le groupe de sécurité universel ou l’ordinateur à ajouter au groupe de rôles. Vous ne pouvez spécifier qu’un membre à la fois.

Pour plus d’informations sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).
  
### <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vérifier que vous avez accordé aux utilisateurs l’accès au centre de sécurité & conformité, utilisez la cmdlet **Get-RoleGroupMember** pour afficher les membres du groupe de rôles gestion de l’organisation, comme illustré dans l’exemple suivant.
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

Pour plus d’informations sur la syntaxe et les paramètres, consultez la rubrique [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).
