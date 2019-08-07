---
title: Conception d’un site d’équipe SharePoint Online isolé
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Résumé : Découvrez comment concevoir des sites d’équipe SharePoint Online.'
ms.openlocfilehash: 19f030f5210fb6742098543ae91117a90d583242
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "36053121"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a>Conception d’un site d’équipe SharePoint Online isolé

 **Résumé :** Découvrez comment concevoir des sites d’équipe SharePoint Online.
  
Cet article vous aide à faire les bons choix de conception avant de créer un site d’équipe SharePoint Online isolé.
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a>Phase 1 : choix des groupes SharePoint et des niveaux d’autorisation

Chaque site d’équipe SharePoint Online par défaut est créé avec les groupes SharePoint suivants :
  
- \<nom du site> membres
    
- \<nom du site> visiteurs
    
- \<Propriétaires de nom de site>
    
Ces groupes sont différents des groupes Office 365 et Azure Active Directory (AD), et permettent d’attribuer des autorisations pour l’utilisation des ressources du site.
  
L’ensemble des autorisations qui déterminent ce que le membre d’un groupe SharePoint peut faire dans un site est un niveau d’autorisation. Il existe trois niveaux d’autorisation par défaut pour un site d’équipe SharePoint Online : Modification, Lecture et Contrôle total. Le tableau suivant indique la corrélation par défaut des groupes SharePoint et les niveaux d’autorisation affectés :
  
|**Groupe SharePoint**|**Niveau d’autorisation**|
|:-----|:-----|
|\<nom du site> membres  <br/> |Edit  <br/> |
|\<nom du site> visiteurs  <br/> |Lecture  <br/> |
|\<Propriétaires de nom de site>  <br/> |Contrôle total  <br/> |
   
 **Conseil :** vous pouvez créer des groupes SharePoint et des niveaux d’autorisation supplémentaires. Cependant, nous vous recommandons d’utiliser les groupes SharePoint par défaut et les niveaux d’autorisation pour votre site SharePoint Online isolé.
  
Voici les groupes et les niveaux d’autorisation SharePoint par défaut.
  
![Les groupes et les niveaux d’autorisation SharePoint par défaut pour un site SharePoint Online.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a>Phase 2 : attribution des autorisations aux utilisateurs membres de groupes d’accès

Vous pouvez attribuer des autorisations aux utilisateurs en ajoutant leur compte d’utilisateur, ou un groupe Office 365 ou Azure AD dont est membre le compte d’utilisateur, aux groupes SharePoint. Une fois ajoutés, les comptes d’utilisateur Office 365 reçoivent, directement ou indirectement via l’appartenance à un groupe Office 365 ou Azure AD, le niveau d’autorisation associé au groupe SharePoint.
  
En prenant l’exemple des groupes SharePoint par défaut :
  
- Les membres du ** \<nom du site>** groupe SharePoint membres, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **modifier**
    
- Les membres du ** \<nom du site>** groupe SharePoint visiteurs, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **lecture**
    
- Les membres du ** \<nom du site>** groupe SharePoint propriétaires, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **contrôle total** .
    
 **Conseil :** même si vous pouvez gérer les autorisations dans chaque compte d’utilisateur, nous vous recommandons plutôt d’utiliser un seul groupe Azure AD, appelé groupe d’accès. Cela simplifie la gestion des autorisations via l’appartenance au groupe d’accès, plutôt que via la gestion de la liste des comptes d’utilisateur pour chaque groupe SharePoint.
  
Les groupes Azure AD pour Office 365 sont différents des groupes Office 365. Les groupes Azure AD apparaissent dans le centre d’administration 365 de Microsoft, dont le **type** est défini sur **sécurité** et n’ont pas d’adresse de messagerie. Les groupes Azure AD peuvent être gérés dans les éléments suivants:
  
- Services de domaine Active Directory (AD DS)
    
    Il s’agit de groupes qui ont été créés dans votre infrastructure AD DS sur site et synchronisés avec votre abonnement Office 365. Dans le centre d’administration 365 de Microsoft, ces groupes ont l' **État** **synchronisé avec Active Directory**.
    
- Office 365
    
    Il s’agit de groupes qui ont été créés à l’aide du centre d’administration Microsoft 365, du portail Azure ou de Microsoft PowerShell. Dans le centre d’administration 365 de Microsoft, ces groupes ont l' **État** **Cloud**.
    
 **Meilleure pratique:** Si vous utilisez AD DS en local et que vous vous synchronisez avec votre abonnement Office 365, effectuez votre gestion des utilisateurs et des groupes avec AD DS.
  
Pour les sites d’équipe SharePoint Online isolés, voici à quoi ressemble la structure recommandée du groupe :
  
|**Groupe SharePoint**|**Groupe d’accès basé sur Azure AD**|**Niveau d’autorisation**|
|:-----|:-----|:-----|
|\<nom du site> membres  <br/> |\<nom du site> membres  <br/> |Edit  <br/> |
|\<nom du site> visiteurs  <br/> |\<Visionneuse de nom de site>  <br/> |Lecture  <br/> |
|\<Propriétaires de nom de site>  <br/> |\<nom du site> administrateurs  <br/> |Contrôle total  <br/> |
   
 **Meilleure pratique:** Bien que vous puissiez utiliser les groupes Office 365 ou Azure AD comme membres des groupes SharePoint, nous vous recommandons d’utiliser les groupes Azure AD. Les groupes Azure AD, gérés via AD DS ou Office 365, offrent davantage de flexibilité pour l’utilisation de groupes imbriqués pour attribuer des autorisations.
  
Voici les groupes SharePoint par défaut configurés pour utiliser les groupes d’accès basé sur Azure AD.
  
![Utilisation de groupes d’accès en tant que membres des groupes de sites SharePoint Online par défaut.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
Lorsque vous concevez les trois groupes d’accès, rappelez-vous de ceci :
  
- Le ** \<nom du site>** groupe d’accès administrateurs ne doit contenir que quelques membres, ce qui correspond à un petit nombre d’administrateurs SharePoint Online qui gèrent le site d’équipe.
    
- La plupart des membres de votre site figurent dans le ** \<nom du site> les membres** ou ** \<le nom du site> les utilisateurs** accèdent aux groupes. Étant donné que les membres du site dans le groupe d’accès ** \<nom du site> membres** ont la possibilité de supprimer ou de modifier les ressources du site, il est préférable de prendre en compte son appartenance. En cas de doute, ajoutez le membre du site au ** \<nom du site>** groupe d’accès observateurs.
    
Voici un exemple des groupes SharePoint et des groupes d’accès pour un site isolé nommé ProjectX.
  
![Exemple d’utilisation de groupes d’accès pour un site SharePoint Online nommé ProjectX.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a>Phase 3: utiliser des groupes Azure AD imbriqués

Pour un projet impliquant un petit nombre d’utilisateurs, vous pouvez ajouter, dans la plupart des cas, un seul niveau de groupes d’accès basés sur Azure AD aux groupes SharePoint du site. Toutefois, si vous avez un grand nombre de personnes et que ces personnes sont déjà membres de groupes Azure AD établis, vous pouvez plus facilement attribuer des autorisations SharePoint à l’aide de groupes imbriqués ou de groupes qui contiennent d’autres groupes en tant que membres.
  
Par exemple, vous souhaitez créer un site d’équipe SharePoint Online isolé pour favoriser la collaboration entre les responsables des services ventes, marketing, ingénierie, juridique et support technique, mais ils ont déjà leur propre groupe de comptes de responsable. Au lieu de créer un groupe pour les nouveaux membres du site et d’y placer tous les comptes de responsable un par un, placez les groupes de responsables existants pour chaque service dans le nouveau groupe.
  
  Si vous partagez un abonnement Office 365 avec d’autres organisations, il peut s’avérer difficile de gérer un seul niveau de groupe pour le site isolé d’une organisation en raison du nombre important de comptes d’utilisateur. Dans ce cas, vous pouvez utiliser les groupes Azure AD imbriqués pour chaque organisation dont les groupes gèrent les autorisations.
  
Pour utiliser les groupes Azure AD imbriqués, procédez comme suit :
  
1. Identifiez ou créez les groupes Azure AD qui contiendront les comptes d’utilisateur et ajoutez les comptes d’utilisateur en tant que membres.
    
2. Créez le groupe d’accès basé sur Azure AD conteneur qui contiendra les autres groupes Azure AD et ajoutez ces groupes en tant que membres.
    
3.   Pour définir le niveau d’accès approprié pour le groupe d’accès conteneur, identifiez le groupe SharePoint et définissez le niveau d’autorisation correspondant.
    
> [!NOTE]
> Vous ne pouvez pas utiliser des groupes Office 365 imbriqués. 
  
Voici un exemple de groupes Azure AD imbriqués pour le groupe d’accès au membre ProjectX.
  
![Un exemple d’utilisation de groupes d’accès imbriqués pour le groupe d’accès membres pour le site ProjectX.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
Étant donné que tous les comptes d’utilisateur dans les équipes de recherche, d’ingénierie et de projet sont destinés à être membres de site, il est plus facile d’ajouter leurs groupes Azure AD au groupe d’accès membres ProjectX.
  
## <a name="next-step"></a>Étape suivante

Lorsque vous êtes prêt à créer et à configurer un site isolé en production, consultez la rubrique [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>Voir aussi

[Sites d'équipe SharePoint Online isolés](isolated-sharepoint-online-team-sites.md)
  
[Gestion d’un site d’équipe SharePoint Online isolé](manage-an-isolated-sharepoint-online-team-site.md)

[Déploiement d’un site d’équipe SharePoint Online isolé](deploy-an-isolated-sharepoint-online-team-site.md)



