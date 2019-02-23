---
title: Déploiement d’un site d’équipe SharePoint Online isolé
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 3033614b-e23b-4f68-9701-f62525eafaab
description: 'Résumé : Découvrez comment déployer un nouveau site d’équipe SharePoint Online isolé en suivant ces instructions détaillées.'
ms.openlocfilehash: 6a552e7ce8982f3b7d943136907764385fa33115
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216604"
---
# <a name="deploy-an-isolated-sharepoint-online-team-site"></a>Déploiement d’un site d’équipe SharePoint Online isolé

 **Résumé :** Découvrez comment déployer un nouveau site d’équipe SharePoint Online isolé en suivant ces instructions détaillées.
  
Cet article est un guide de déploiement détaillé pour créer et configurer un site d’équipe SharePoint Online isolé dans Microsoft Office 365. Pour cela, vous devez utiliser les trois groupes SharePoint par défaut et les niveaux d’autorisation correspondants (un groupe d’accès Azure Active Directory (AD) pour chaque niveau d’accès).
  
## <a name="phase-1-create-and-populate-the-team-site-access-groups"></a>Phase 1: création et remplissage des groupes d'accès au site d'équipe

Au cours de cette phase, vous allez créer les trois groupes d’accès basés sur Azure AD pour les trois groupes SharePoint par défaut et les remplir avec les comptes d’utilisateur appropriés.
  
> [!NOTE]
> Pour réaliser les étapes suivantes, vous devez avoir créé tous les comptes d’utilisateur nécessaires et leur avoir affecté les licences appropriées. Dans le cas contraire, ajoutez-les et attribuez-leur des licences avant de passer à l’étape 1. 
  
### <a name="step-1-list-the-sharepoint-online-admins-for-the-site"></a>Étape 1 : liste des administrateurs SharePoint Online du site

Choisissez les comptes d’utilisateur des administrateurs SharePoint Online pour le site d’équipe isolé.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365 et que vous souhaitez utiliser Windows PowerShell, dressez une liste de leurs noms d’utilisateur principaux (UPN) (exemple d’UPN : belindan@contoso.com).
  
### <a name="step-2-list-the-members-for-the-site"></a>Étape 2 : liste des membres du site

Choisissez les comptes d’utilisateur des membres du site d’équipe isolé, c’est-à-dire ceux qui collaboreront sur les ressources stockées sur le site.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365 et que vous souhaitez utiliser PowerShell, dressez une liste de leurs UPN. S’il existe un grand nombre de membres du site, vous pouvez enregistrer la liste de noms UPN dans un fichier texte et tous les ajouter avec une seule commande PowerShell.
  
### <a name="step-3-list-the-viewers-for-the-site"></a>Étape 3 : liste des visiteurs du site

Choisissez les comptes d’utilisateur des visiteurs du site d’équipe isolé, c’est-à-dire ceux qui peuvent afficher les ressources stockées sur le site sans pouvoir les modifier ou collaborer directement sur leur contenu.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365 et que vous souhaitez utiliser PowerShell, dressez une liste de leurs UPN. S’il existe un grand nombre de membres du site, vous pouvez enregistrer la liste de noms UPN dans un fichier texte et tous les ajouter avec une seule commande PowerShell.
  
Les visiteurs du site peuvent comprendre des membres de l’équipe de direction, du service juridique ou de plusieurs services.
  
### <a name="step-4-create-the-three-access-groups-for-the-site-in-azure-ad"></a>Étape 4 : création des trois groupes d’accès du site dans Azure AD

Vous devez créer les groupes d’accès suivants dans Azure AD :
  
- Administrateurs du site (qui contient la liste de l’étape 1)
    
- Membres du site (qui contient la liste de l’étape 2)
    
- Visiteurs du site (qui contient la liste de l’étape 3)
    
1. Dans votre navigateur, accédez au portail Azure [https://portal.azure.com](https://portal.azure.com) et connectez-vous avec les informations d'identification d'un compte qui a été affecté au rôle administrateur de gestion des utilisateurs ou administrateur de la société.
    
2. Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes**.
    
3. Dans le panneau **Groupes - Tous les groupes**, cliquez sur **+ Nouveau groupe**.
    
4. Dans le panneau **Groupe** :
    
  - Sélectionnez **Office 365** dans **Type de groupe**.
    
  - Tapez le nom du groupe dans **nom**.
    
  - Tapez une description du groupe dans **Description du groupe**.
    
  - Sélectionnez **Affecté** dans le champ **Type d’appartenance**.
    
5. Cliquez sur **Créer** et fermez le panneau **Groupe**.
    
6. Répétez les étapes 3-5 pour vos autres groupes.
    
> [!NOTE]
> Vous devez utiliser le portail Azure pour créer les groupes afin que les fonctionnalités Office soient activées. Si un site SharePoint Online isolé est par la suite configuré comme un site hautement confidentiel avec une étiquette Azure information protection (AIP) pour chiffrer les fichiers et attribuer des autorisations à des groupes spécifiques, les groupes autorisés doivent avoir été créés avec des fonctionnalités Office. activé. Vous ne pouvez pas modifier le paramètre fonctionnalités Office d'un groupe Azure AD une fois qu'il a été créé. 
  
Voici la configuration obtenue avec les trois groupes d'accès au site.
  
![Trois groupes d’accès pour le déploiement d’un site SharePoint Online isolé.](media/c2557f61-478b-4494-95e9-d79fe5909e8b.png)
  
### <a name="step-5-add-the-user-accounts-to-the-access-groups"></a>Étape 5. Ajouter les comptes d'utilisateur aux groupes d'accès

Procédez comme suit :
  
1. Ajoutez la liste des utilisateurs de l’étape 1 au groupe d’accès Administrateurs du site
    
2. Ajoutez la liste des utilisateurs de l’étape 2 au groupe d’accès Membres du site
    
3. Ajoutez la liste des utilisateurs de l’étape 3 au groupe d’accès Visiteurs du site
    
Si vous gérez des comptes d’utilisateur et des groupes via Windows Server AD, ajoutez les utilisateurs aux groupes d’accès appropriés en suivant les procédures classiques de gestion des utilisateurs et des groupes Windows Server AD, puis attendez la synchronisation avec votre abonnement Office 365.
  
Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le Centre d’administration Office ou PowerShell. Si plusieurs groupes d’accès portent le même nom, utilisez le Centre d’administration Office.
  
Pour le centre d'administration Office, connectez-vous à l'aide d'un compte d'utilisateur auquel a été attribué le rôle administrateur de compte d'utilisateur ou administrateur de société et utilisez des groupes pour ajouter les comptes d'utilisateur et les groupes appropriés aux groupes d'accès appropriés.
  
Pour PowerShell, consultez la rubrique [Se connecter à Office 365 PowerShell](https://go.microsoft.com/fwlink/?linkid=842218).
  
Ensuite, utilisez le bloc de commandes suivant pour ajouter un compte d'utilisateur individuel à un groupe d'accès:
  
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> Pour un fichier texte qui contient toutes les commandes PowerShell et une feuille de calcul de configuration Excel qui génère des commandes PowerShell en fonction des noms de compte de vos utilisateurs et groupes, téléchargez le [kit de déploiement du site d'équipe SharePoint Online isolé](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907). 
  
Si vous avez stocké les UPN des comptes d’utilisateur des groupes d’accès dans un fichier texte, vous pouvez exécuter le bloc de commandes PowerShell suivant pour les ajouter tous en même temps :
  
```
$grpName="<display name of the access group>"
$fileName="<path and name of the file containing the list of account UPNs>"
$grpID=(Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
Get-Content $fileName | ForEach { $userUPN=$_; Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID $grpID }
```

Pour PowerShell, utilisez le bloc de commandes suivant pour ajouter un groupe individuel à un groupe d'accès:
  
```
$nestedGrpName="<display name of the group to add to the access group>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $nestedGrpName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID

```

Voici les résultats que vous devriez obtenir :
  
- Le groupe Azure AD administrateurs du site contient les comptes d'utilisateur ou les groupes d'administrateurs de site
    
- Le groupe Azure AD membres du site contient les comptes d'utilisateur ou les groupes de membres du site.
    
- Le groupe Azure AD visiteurs du site contient les comptes d'utilisateur ou les groupes qui peuvent uniquement afficher le contenu du site.
    
Validez la liste des membres de chaque groupe d’accès avec le Centre d’administration Office ou le bloc de commandes PowerShell suivant :
  
```
$grpName="<display name of the access group>"
Get-AzureADGroupMember -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID | Sort UserPrincipalName | Select UserPrincipalName,DisplayName,UserType
```

Voici la configuration obtenue avec les trois groupes d'accès au site renseignés avec des comptes d'utilisateur ou des groupes.
  
![Les trois groupes d’accès renseignés avec les comptes d’utilisateurs.](media/2320107c-dad6-4c8f-94e5-f6427c125e71.png)
  
## <a name="phase-2-create-and-configure-the-isolated-team-site"></a>Phase 2 : création et configuration du site d’équipe isolé

Au cours de cette phase, vous allez créer le site SharePoint Online isolé et configurer les niveaux d’autorisation SharePoint Online par défaut pour utiliser vos nouveaux groupes d’accès Azure AD.
  
Commencez par créer le site d’équipe SharePoint Online en suivant ces étapes.
  
1. Connectez-vous au portail Office 365 avec un compte qui sera également utilisé pour administrer le site d’équipe SharePoint Online (un administrateur SharePoint Online). Pour obtenir de l’aide, consultez [Où se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).
    
2. Dans la liste des vignettes, cliquez sur **SharePoint**.
    
3. Sous le nouvel onglet **SharePoint** de votre navigateur, cliquez sur **+ Créer un site**.
    
4. Dans la page **Créer un site**, cliquez sur **Site d’équipe**.
    
5. Dans **nom du site**, tapez un nom pour le site d'équipe. 
    
6. Dans **Description du site d'équipe,** tapez une description facultative de l'objectif du site.
    
7. Dans **Paramètres de confidentialité**, sélectionnez **Privé - Seuls les membres peuvent accéder à ce site**, puis cliquez sur **Suivant**.
    
8. Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.
    
Ensuite, dans le nouveau site d’équipe SharePoint Online, configurez les autorisations.
  
1. Dans la barre d’outils, cliquez sur l’icône Paramètres, puis cliquez sur **Paramètres du site**.
    
2. Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.
    
3. Sous le nouvel onglet **Autorisations** dans votre navigateur, cliquez sur **Paramètres des demandes d’accès**.
    
4. Dans la boîte de dialogue **paramètres des demandes d'accès** , désélectionnez **autoriser le membre pour partager le site et les fichiers et dossiers individuels** et **autoriser les demandes d'accès** (de sorte que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.
    
5. Dans l'onglet **autorisations** de votre navigateur, cliquez sur ** \<name> de site** dans la liste.
    
6. Dans **Personnes et groupes**, cliquez sur **Nouveau**.
    
7. Dans la boîte de dialogue **Partager**, saisissez le nom du groupe d’accès Membres du site, sélectionnez-le, puis cliquez sur **Partager**.
    
8. Cliquez sur le bouton de retour de votre navigateur.
    
9. Cliquez sur ** \<propriétaires de sites name>** dans la liste.
    
10. Dans **Personnes et groupes**, cliquez sur **Nouveau**.
    
11. Dans la boîte de dialogue **Partager**, saisissez le nom du groupe d’accès Administrateurs du site, sélectionnez-le, puis cliquez sur **Partager**.
    
12. Cliquez sur le bouton de retour de votre navigateur.
    
13. Cliquez sur ** \<sites name> visiteurs** de la liste.
    
14. Dans **Personnes et groupes**, cliquez sur **Nouveau**.
    
15. Dans la boîte de dialogue **Partager**, saisissez le nom du groupe d’accès Visiteurs du site, sélectionnez-le, puis cliquez sur **Partager**.
    
16. Fermez l’onglet **Autorisations** de votre navigateur.
    
Voici les résultats que vous devez escompter :
  
- Le ** \<groupe SharePoint name> propriétaires de sites** contient le groupe d'accès administrateurs du site, dans lequel tous les membres ont le niveau d'autorisation **contrôle total** .
    
- Le ** \<groupe SharePoint name> membres du site** contient le groupe d'accès membres du site, dans lequel tous les membres ont le niveau d'autorisation **modifier** .
    
- Le ** \<groupe SharePoint name> visiteurs du site** contient le groupe d'accès visiteurs du site, dans lequel tous les membres ont le niveau d'autorisation **lecture** .
    
- L’option permettant aux membres d’inviter d’autres membres ou non membres à demander l’accès au site est désactivée.

    
Voici la configuration obtenue avec les trois groupes SharePoint pour le site configuré pour utiliser les trois groupes d'accès, qui sont renseignés avec les comptes d'utilisateur ou les groupes Azure AD.
  
![Configuration finale de votre site SharePoint Online isolé avec des comptes d’utilisateurs et groupes d’accès.](media/e7618971-06ab-447b-90ff-d8be3790fe63.png)
  
Comme vous êtes membres de l’un des groupes d’accès, vous et les membres du site pouvez désormais collaborer sur les ressources du site.
  
## <a name="next-step"></a>Étape suivante

Si vous avez besoin de modifier les membres du groupe d’accès du site ou de créer un dossier de documents avec des autorisations personnalisées, consultez la rubrique [Manage an isolated SharePoint Online team site](manage-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Voir aussi

[Sites d'équipe SharePoint Online isolés](isolated-sharepoint-online-team-sites.md)
  
[Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md)
  
[Gestion d’un site d’équipe SharePoint Online isolé](manage-an-isolated-sharepoint-online-team-site.md)
  



