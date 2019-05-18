---
title: Gérer les autorisations de groupe de rôles d’administrateur dans EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.
ms.openlocfilehash: 35f248bce26d28c8ab7465ff983629eb01db407b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150156"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a>Gérer les autorisations de groupe de rôles d’administrateur dans EOP
  
Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer

- Durée d'exécution estimée : 5 à 10 minutes
    
- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md). 
    
- Certaines autorisations dans Office 365 mappent vers des autorisations du groupe de rôles d'administration EOP. Pour plus d'informations, consultez la colonne « Rôle dans Exchange Online » de la section « À quels services mes autorisations Office 365 s'appliquent-elles ? » dans la rubrique [Affectation de rôles d'administrateur](https://go.microsoft.com/fwlink/p/?LinkId=286708).
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="what-do-you-want-to-do"></a>Que souhaitez-vous faire ?

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a>Utiliser le Centre d'administration Exchange (CAE) pour affecter des membres à des groupes de rôles d'administrateur

1. Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles auquel vous souhaitez ajouter l’utilisateur ou les utilisateurs,](../media/ITPro-EAC-EditIcon.gif)puis cliquez sur **modifier** ![l’icône modifier.
    
2. Sous Membres, cliquez sur **Ajouter**![Icône Ajouter](../media/ITPro-EAC-AddIcon.gif). La fenêtre Sélectionner les membres s'affiche.
    
3. Recherchez le ou les utilisateurs à ajouter, ou sélectionnez-les dans la liste.
    
4. Lorsque vous avez sélectionné les utilisateurs à ajouter, cliquez sur **Ajouter**, puis sur **OK**. La fenêtre Sélectionner les membres se ferme.
    
5. Vous constatez que les utilisateurs ont été ajoutés au volet **Membres**. Cliquez sur **Enregistrer**.
    
    > [!NOTE]
    > Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées. 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a>Utiliser le Centre d'administration Exchange (CAE) pour supprimer des membres de groupes de rôles d'administrateur

1. Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles duquel vous souhaitez supprimer un ou les utilisateurs, puis](../media/ITPro-EAC-EditIcon.gif)cliquez sur **modifier** ![l’icône de modification.
    
2. Sous Membres, sélectionnez les utilisateurs à supprimer, puis cliquez sur **Supprimer**![Icône Suppression](../media/ITPro-EAC-RemoveIcon.gif).
    
3. Cliquez sur **Enregistrer** pour enregistrer la modification apportée au groupe de rôles et retourner à la page **Rôles d'administrateur**. Pour vérifier que vous avez supprimé l'utilisateur du groupe de rôles d'administrateur, assurez-vous que le membre n'apparaît plus sous Membres dans le volet Détails relatif au groupe de rôles sélectionné. 
    
    > [!NOTE]
    > Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées. 
  
## <a name="for-more-information"></a>Pour plus d’informations

[Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md)
  

