---
title: Site d’équipe SharePoint Online isolé dans votre environnement de développement/test
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: "Résumé: conFigurez un site d'équipe SharePoint Online isolé du reste de l'organisation dans votre environnement de développement/test Office 365."
ms.openlocfilehash: 56c10b1a3871014f26a4d2fd98d9b4139d19ac47
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000227"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a>Site d’équipe SharePoint Online isolé dans votre environnement de développement/test

 **Résumé:** ConFigurez un site d'équipe SharePoint Online isolé du reste de l'organisation dans votre environnement de développement/test Office 365.
  
Les sites d'équipe SharePoint Online dans Office 365 sont des emplacements de collaboration à l'aide d'une bibliothèque de documents commune, d'un bloc-notes OneNote et d'autres services. Dans de nombreux cas, vous souhaitez bénéficier d’un large accès et d’une collaboration entre les départements ou organisations. Toutefois, dans certains cas, vous souhaitez contrôler étroitement l'accès et les autorisations de collaboration entre un petit groupe de personnes.
  
L'accès aux sites d'équipe SharePoint Online et ce que les utilisateurs peuvent faire sont contrôlés par les groupes SharePoint et les niveaux d'autorisation. Par défaut, les sites SharePoint Online comportent trois niveaux d’accès :
  
- Les **membres** peuvent afficher, créer et modifier des ressources sur le site.
    
- Les **propriétaires** ont un contrôle total sur le site, et peuvent même modifier les autorisations.
    
- Les **Visiteurs** peuvent uniquement afficher les ressources du site.
    
Cet article décrit la configuration d'un site d'équipe SharePoint Online isolé pour un projet de recherche secrète nommé ProjectX. Les conditions d'accès sont les suivantes:
  
- Seuls les membres du projet peuvent accéder au site et à son contenu (documents, bloc-notes OneNote, pages), avec des niveaux d’autorisation SharePoint pour éditer et afficher contrôlés via l’appartenance au groupe.
    
- Seuls le créateur du site et les membres d’un groupe d’administrateurs du site peuvent effectuer l’administration du site, y compris la modification des autorisations au niveau du site.
    
Il existe trois phases de configuration d'un site d'équipe SharePoint Online isolé dans votre environnement de développement/test Office 365:
  
1. Créez l’environnement de développement/test Office 365.
    
2. Créez les utilisateurs et groupes pour ProjectX.
    
3. Créez un site d'équipe SharePoint Online ProjectX et isolez-le.
    
> [!TIP]
> Cliquez [ici](http://aka.ms/catlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft Cloud.
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a>Phase 1 : Créer votre environnement de développement/test Office 365 en mode léger ou pour entreprise simulée

Si vous souhaitez simplement créer un site d'équipe SharePoint Online isolé avec la configuration minimale requise, suivez les instructions des phases 2 et 3 de l'environnement de [développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).
  
Si vous souhaitez créer un site d'équipe SharePoint Online isolé dans une configuration d'entreprise simulée, suivez les instructions de [DirSync pour votre environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).
  
> [!NOTE]
> La création d’un site SharePoint Online isolé ne requiert pas l’environnement de développement/test en entreprise simulée, qui utilise un intranet simulé connecté à Internet et la synchronisation d’annuaire pour une forêt Windows Server AD. Il est proposé comme option dans cet article afin que vous puissiez tester un site SharePoint Online isolé et faire des essais dans un environnement qui représente une organisation classique. 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a>Phase 2: créer des comptes d'utilisateurs et des groupes d'accès

Utilisez les instructions de [connexion à office 365 PowerShell](https://technet.microsoft.com/library/dn975125.aspx) pour vous connecter à votre abonnement final Office 365 avec votre compte d'administrateur général à partir de:
  
- Votre ordinateur (pour l’environnement de développement/test Office 365 léger).
    
- La machine virtuelle CLIENT1 (pour l’environnement de développement/test Office 365 d’entreprise simulé).
    
Pour créer les nouveaux groupes d'accès pour le site d'équipe SharePoint Online ProjectX, exécutez les commandes suivantes à partir de l'invite du module Windows Azure Active Directory pour Windows PowerShell:
  
```
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

> [!TIP]
> Cliquez [ici](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) pour obtenir un fichier texte qui contient toutes les commandes PowerShell de cet article.
  
Entrez le nom de votre organisation (exemple : contosotoycompany) et le code de pays à deux caractères pour indiquer votre emplacement, puis exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la conception et enregistrez-le dans un emplacement sécurisé.
  
Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte Responsable de la recherche et enregistrez-le dans un emplacement sécurisé.
  
Exécutez les commandes suivantes à partir de l’invite Module Windows Azure Active Directory pour Windows PowerShell :
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

À partir de la zone de la commande **New-MsolUser**, notez le mot de passe généré pour le compte VP du développement et enregistrez-le dans un emplacement sécurisé.
  
Ensuite, pour ajouter les nouveaux comptes aux nouveaux groupes d'accès, exécutez les commandes PowerShell suivantes à partir de l'invite du module Windows Azure Active Directory pour Windows PowerShell:
  
```
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

Résultats
  
- Le groupe d'accès ProjectX-membres contient les comptes d'utilisateur concepteur de prospects et chercheur de prospect
    
- Le groupe d'accès ProjectX-administrateurs contient le compte d'administrateur général pour votre abonnement à la version d'évaluation
    
- Le groupe d'accès ProjectX-visualisers contient le compte d'utilisateur VP du développement.
    
La figure 1 présente les groupes d'accès et leur appartenance.
  
**Figure 1**

![Les groupes Office 365 et leur appartenance pour un site de groupe SharePoint Online isolé](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a>Phase 3: créer un nouveau site d'équipe ProjectX SharePoint Online et l'isoler

Pour créer un site d'équipe SharePoint Online pour ProjectX, procédez comme suit:
  
1. À l'aide d'un navigateur sur votre ordinateur local (configuration légère) ou sur CLIENT1 (configuration d'entreprise simulée), connectez-vous au portail[https://admin.microsoft.com](https://admin.microsoft.com)Office 365 () à l'aide de votre compte d'administrateur général.
    
2. Dans la liste des vignettes, cliquez sur **SharePoint**.
    
3. Dans le nouvel onglet SharePoint de votre navigateur, cliquez sur **+ Créer un site**.
    
4. Dans **Nom du site d’équipe**, saisissez **ProjectX**. Dans **paramètres de confidentialité**, sélectionnez **privé-seuls les membres peuvent accéder à ce site**.
    
5. Dans **Description du site d’équipe**, saisissez **Site SharePoint pour ProjectX**, puis cliquez sur **Suivant**.
    
6. Dans le volet **Qui voulez-vous ajouter ?**, cliquez sur **Terminer**.
    
7. Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, dans la barre d’outils, cliquez sur l’icône des paramètres, puis sur **Autorisations du site**.
    
8. Dans le volet **Autorisations du site**, cliquez sur **Paramètres d’autorisations avancés**.
    
9. Dans le nouvel onglet **Autorisations : Projet X** de votre navigateur, cliquez sur **Paramètres de demande d’accès**.
    
10. Dans la boîte de dialogue **Paramètres de demande d’accès**, désactivez les cases à cocher **Autoriser les membres à partager le site et les fichiers et dossiers individuels** et **Autoriser les demandes d’accès** (afin que les trois cases à cocher soient désactivées), puis cliquez sur **OK**.
    
11. Cliquez sur **Membres de ProjectX** dans la liste.
    
12. Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.
    
13. Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Membres**, sélectionnez-le, puis cliquez sur **Partager**.
    
14. Cliquez sur le bouton de retour de votre navigateur.
    
15. Cliquez sur **Propriétaires de ProjectX** dans la liste.
    
16. Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.
    
17. Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Administrateurs**, sélectionnez-le, puis cliquez sur **Partager**.
    
18. Cliquez sur le bouton de retour de votre navigateur.
    
19. Cliquez sur **Visiteurs de ProjectX** dans la liste.
    
20. Dans la page **Personnes et groupes**, cliquez sur **Nouveau**.
    
21. Dans la boîte de dialogue **Partager**, saisissez **ProjectX-Utilisateurs**, sélectionnez-le, puis cliquez sur **Partager**.
    
22. Fermez l’onglet **Personnes et groupes** de votre navigateur, cliquez sur l’onglet **ProjectX-Accueil** de votre navigateur, puis fermez le volet **Autorisations du site**.
    
Voici les résultats de la configuration des autorisations :
  
- Le groupe SharePoint membres de ProjectX contient uniquement le groupe d'accès ProjectX membres (qui contient uniquement les comptes d'utilisateur de concepteur de prospect et de chercheur de Prospect) et le groupe ProjectX (qui contient uniquement le compte d'utilisateur d'administrateur général).
    
- Le groupe SharePoint propriétaires ProjectX contient uniquement le groupe d'accès ProjectX-administrateurs (qui contient uniquement le compte d'utilisateur de l'administrateur général).
    
- Le groupe SharePoint visiteurs ProjectX contient uniquement le groupe d'accès ProjectX-affiche (qui contient uniquement le compte d'utilisateur VP du développement).
    
- Les membres ne peuvent pas modifier les autorisations au niveau du site (cette opération peut être uniquement effectuée par les membres du groupe ProjectX-Administrateurs).
    
- Les autres comptes d’utilisateurs ne peuvent pas accéder au site ni à ses ressources, ni demander l’accès au site.
    
La figure 2 présente les groupes SharePoint et leur appartenance.
  
**Figure 2**

![Groupes SharePoint Online et leur appartenance pour un site de groupe SharePoint Online isolé](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
Nous allons maintenant illustrer l'accès à l'aide du compte d'utilisateur du Concepteur sénior:
  
1. Fermez l’onglet **ProjectX-Accueil** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office** du navigateur.
    
2. Cliquez sur le nom de votre administrateur général, puis cliquez sur **Déconnexion**.
    
3. Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l'aide du nom de compte du concepteur de prospect et de son mot de passe.
    
4. Dans la liste des vignettes, cliquez sur **SharePoint**.
    
5. Dans le nouvel onglet **SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d'équipe **ProjectX** . Un nouvel onglet doit apparaître dans votre navigateur pour le site d'équipe ProjectX.
    
6. Cliquez sur l’icône des paramètres. Notez qu’il n’existe pas d’option pour **Autorisations du site**. Cela est correct puisque seuls les membres du groupe ProjectX-Administrateurs peuvent modifier les autorisations sur le site
    
7. Ouvrez le bloc-notes ou un éditeur de texte de votre choix.
    
8. Copiez l'URL du site d'équipe ProjectX et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte.
    
9. Dans le nouvel onglet **ProjectX-Accueil** de votre navigateur, cliquez sur **Documents**.
    
10. Copiez l’URL du dossier de documents ProjectX et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte.
    
11. Dans le nouvel onglet **ProjectX-Documents** de votre navigateur, cliquez sur **Nouveau > Document Word**.
    
12. Saisissez du texte dans la page **Word Online**, attendez que l’état indique **Enregistré**et cliquez sur le bouton de retour de votre navigateur, puis actualisez la page. Vous devriez voir un nouveau **Document.docx** dans le dossier **Documents**.
    
13. Cliquez sur les points de suspension du document **Document.docx**, puis sur **Obtenir un lien**.
    
14. Copiez l'URL dans la boîte de dialogue **partager «document. docx»** et collez-la dans une nouvelle ligne dans le bloc-notes ou dans votre éditeur de texte, puis fermez la boîte de dialogue **«document. docx» de partage** .
    
15. Fermez les onglets **ProjectX-Documents** et **SharePoint** dans votre navigateur, puis cliquez sur l’onglet **Accueil Microsoft Office**.
    
16. Cliquez sur le nom **Responsable de la conception**, puis cliquez sur **Déconnexion**.
    
Nous allons maintenant illustrer l'accès à l'aide du compte d'utilisateur VP du développement:
  
1. Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l'aide du nom de compte VP du développement et de son mot de passe.
    
2. Dans la liste des vignettes, cliquez sur **SharePoint**.
    
3. Dans le nouvel onglet **SharePoint** de votre navigateur, tapez **ProjectX** dans la zone de recherche, activez la recherche, puis cliquez sur le site d'équipe **ProjectX** . Un nouvel onglet doit apparaître dans votre navigateur pour le site d'équipe ProjectX.
    
4. Cliquez sur **Documents**, puis sur le fichier **Document.docx**.
    
5. Dans l’onglet **Document.docx** de votre navigateur, essayez de modifier le texte. Vous devriez voir un message indiquant **Ce document est en lecture seule.** Ceci est dû au fait que le compte d’utilisateur VP du développement comporte seulement des autorisations d’affichage pour le site.
    
6. Fermer les onglets **Document.docx**, **ProjectX-Documents** et **SharePoint** de votre navigateur.
    
7. Cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **VP du développement**, puis sur **Déconnexion**.
    
À présent, nous allons illustrer l'accès à un compte d'utilisateur qui n'a pas d'autorisations:
  
1. Connectez-vous au portail Office 365 ([https://admin.microsoft.com](https://admin.microsoft.com)) à l'aide du nom de compte utilisateur 3 et de son mot de passe.
    
2. Dans la liste des mosaïques, cliquez sur **SharePoint**.
    
3. 	Dans le nouvel onglet **SharePoint** de votre navigateur, saisissez **ProjectX** dans la zone de recherche, puis activez la recherche. Vous devriez voir le message **Aucun résultat ne correspond à votre recherche.**
    
4. À partir de l’instance ouverte du bloc-notes ou de votre éditeur de texte, copiez l’URL du site ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.
    
5. À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du dossier Documents ProjectX dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.
    
6. À partir du bloc-notes ou votre éditeur de texte, copiez l’URL du fichier Documents.docx dans la barre d’adresses de votre navigateur, puis appuyez sur **Entrée**. Vous devriez voir une page **Accès refusé**.
    
7. Fermez l’onglet **SharePoint** de votre navigateur, cliquez sur l’onglet **Accueil Microsoft Office**, sur le nom **Utilisateur 3**, puis sur **Déconnexion**.
    
Votre site SharePoint Online isolé est maintenant prêt pour votre expérience supplémentaire.
  
## <a name="next-step"></a>Étape suivante

Lorsque vous souhaitez déployer un site d'équipe SharePoint Online isolé en production, lisez la procédure détaillée dans la rubrique [Conception d'un site d'équipe SharePoint Online isolé](design-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Voir aussi

[Sites d'équipe SharePoint Online isolés](isolated-sharepoint-online-team-sites.md)
  
[Guides de laboratoire de test d’adoption cloud](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[Environnement de développement/test de configuration de base](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[Environnement de développement/test Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[Adoption du cloud et solutions hybrides](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




