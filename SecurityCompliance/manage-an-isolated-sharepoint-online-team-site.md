---
title: Gestion d'un site d'équipe SharePoint Online isolé
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: "Résumé : Découvrez comment gérer votre site d'équipe SharePoint Online isolé."
ms.openlocfilehash: e6ed86421ec199ce785e2daff5e9c5447939e69b
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36053079"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a>Gestion d’un site d’équipe SharePoint Online isolé

 **Résumé :** Découvrez comment gérer votre site d'équipe SharePoint Online isolé.
  
Cet article vous explique comment gérer un site d’équipe SharePoint Online isolé.
  
## <a name="add-a-new-user"></a>Ajouter un nouvel utilisateur

Lorsqu’un nouvel utilisateur rejoint le site, vous devez choisir son niveau de participation :
  
- Administration : ajoutez le compte du nouvel utilisateur au groupe d'accès Administrateurs du site
    
- Collaboration active : ajoutez le compte de l'utilisateur au groupe d'accès Membres du site
    
- Consultation : ajoutez le compte de l'utilisateur au groupe d'accès Visiteurs du site
    
Si vous gérez des comptes d’utilisateur et des groupes par le biais des services de domaine Active Directory (AD DS), ajoutez les utilisateurs appropriés aux groupes d’accès appropriés en utilisant vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou Microsoft PowerShell:
  
- Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les utilisateurs appropriés aux groupes d’accès appropriés.
    
- Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module). Pour ajouter un compte d'utilisateur à un groupe d'accès en utilisant son nom d'utilisateur principal (UPN), exécutez le bloc de commandes PowerShell suivant :
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> Pour un fichier texte qui contient toutes les commandes PowerShell et une feuille de calcul de configuration Excel qui génère des commandes PowerShell en fonction des noms de compte de vos utilisateurs et groupes, téléchargez le [kit de déploiement du site d'équipe SharePoint Online isolé](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907). 

Pour ajouter un compte d’utilisateur à un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a>Ajouter un nouveau groupe

Pour ajouter un accès à un groupe, vous devez choisir le niveau de participation de tous les membres du groupe sur le site :
  
- Administration : ajoutez le groupe d'utilisateurs au groupe d'accès Administrateurs du site
    
- Collaboration active : ajoutez le groupe d'utilisateurs au groupe d'accès Membres du site
    
- Consultation : ajoutez le groupe d'utilisateurs au groupe d'accès Visiteurs du site
    
Si vous gérez des comptes d’utilisateur et des groupes via AD DS, ajoutez les groupes appropriés aux groupes appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:
  
- Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les groupes appropriés aux groupes d’accès appropriés.
    
- Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).
 Ensuite, utilisez les commandes PowerShell suivantes :
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a>Supprimer un utilisateur

Lorsque l'accès d'un utilisateur doit être supprimé du site, supprimez-le du groupe d'accès dont il est membre en fonction de sa participation sur le site :
  
- Administration : supprimez le compte d'utilisateur du groupe d'accès Administrateurs du site
    
- Collaboration active : supprimez le compte d'utilisateur du groupe d'accès Membres du site
    
- Consultation : supprimez le compte d'utilisateur du groupe d'accès Visiteurs du site
    
Si vous gérez des comptes d’utilisateur et des groupes via AD DS, supprimez les utilisateurs appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:
  
- Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les utilisateurs appropriés des groupes d’accès appropriés.
    
- Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).
Pour supprimer un compte d'utilisateur d'un groupe d'accès en utilisant son UPN, exécutez le bloc de commandes PowerShell suivant :
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

Pour supprimer un compte d’utilisateur d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a>Supprimer un groupe

Pour supprimer l’accès d’un groupe, supprimez le groupe du groupe d’accès dont il est membre en fonction de sa participation sur le site :
  
- Administration : supprimez le groupe du groupe d'accès Administrateurs du site
    
- Collaboration active : supprimez le groupe du groupe d'accès Membres du site
    
- Consultation : supprimez le groupe du groupe d'accès Visiteurs du site
    
Si vous gérez des comptes d’utilisateur et des groupes par le biais de Windows Server Active Directory, supprimez les groupes appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell:
  
- Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les groupes appropriés des groupes d’accès appropriés.
    
- Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).    
Pour supprimer un groupe d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a>Création d’un sous-dossier de documents avec des autorisations personnalisées

Il arrive que des utilisateurs travaillant dans un site isolé aient besoin d'un espace privé pour travailler en équipe. Pour les sites SharePoint Online, vous pouvez créer un sous-dossier dans le dossier Documents du site et affecter des autorisations personnalisées. Les personnes non autorisées ne verront pas ce sous-dossier.
  
Pour créer un sous-dossier de documents avec des autorisations personnalisées, procédez comme suit :
  
1. Connectez-vous à Office 365 avec un compte membre du groupe d'accès Administrateurs du site. Pour plus d'informations, consultez la rubrique [Se connecter à Office 365 pour les entreprises](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).
    
2. Accédez au site d'équipe isolé, puis cliquez sur **Documents**.
    
3. Accédez au dossier dans le dossier de documents qui contiendra le sous-dossier bénéficiant d’autorisations personnalisées, créez le dossier, puis ouvrez-le.
    
4. Cliquez sur **Partager**.
    
5. Cliquez sur **Partagé avec > Avancé**.
    
6. Cliquez sur **Arrêter l'héritage des autorisations**, puis cliquez sur **OK**.
    
7. Cliquez sur **Partager**.
    
8. Cliquez sur **Partagé avec > Avancé**.
    
9. Cliquez sur **Accorder des autorisations > Partagé avec > Avancé**.
    
10. Sur la page Autorisations, cliquez sur Membres de **\<nom du site> dans la liste**.
    
11. Sur la page Membres de **\<nom du site>**, cochez la case en regard du groupe d’accès Membres du site, cliquez sur **Actions**, sur **Supprimer des utilisateurs du groupe**, puis sur **OK**.
    
12. Pour ajouter des membres à ce sous-dossier, cliquez sur **Nouveau > Ajouter des utilisateurs**.
    
13. Dans la boîte de dialogue **Partager**, saisissez les noms des comptes d'utilisateur qui peuvent collaborer sur des fichiers du sous-dossier, puis cliquez sur **Partager**.
    
14. Actualisez la page web pour afficher les nouveaux résultats.
    
15. Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Visiteurs de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent afficher les fichiers du sous-dossier (selon vos besoins).
    
16. Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Propriétaires de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent gérer les autorisations du sous-dossier (selon vos besoins).
    
17. Fermez l’onglet **Utilisateurs et groupes** dans votre navigateur.
    
## <a name="see-also"></a>Voir aussi

[Sites d’équipe SharePoint Online isolés](isolated-sharepoint-online-team-sites.md)
  
[Conception d’un site d’équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md)

[Déploiement d’un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md)



