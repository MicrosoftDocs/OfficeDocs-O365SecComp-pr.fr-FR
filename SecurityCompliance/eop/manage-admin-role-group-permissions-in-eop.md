---
title: Gérer les autorisations de groupe de rôles d’administrateur dans EOP
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Les administrateurs peuvent apprendre à attribuer ou supprimer des autorisations dans le centre d’administration Exchange dans Exchange Online Protection.
ms.openlocfilehash: 7bd1a6959dd03a118608dfe45faa253fd56539d4
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676724"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a>Gérer les autorisations de groupe de rôles d’administrateur dans EOP
  
Dans Microsoft Exchange Online Protection (EOP), vous pouvez utiliser le Centre d'administration Exchange (CAE) pour inclure un utilisateur en tant que membre d'un ou de plusieurs groupes de rôles afin de lui attribuer des autorisations lui permettant de réaliser des tâches administratives particulières. Le CAE vous permet également de supprimer un utilisateur d'un ou de plusieurs groupes de rôles.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer

- Durée d'exécution estimée : 5 à 10 minutes

- Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).

- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Utilisateurs, contacts et groupes de rôles » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).

- Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).

> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .
  
## <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a>Utiliser le Centre d'administration Exchange (CAE) pour affecter des membres à des groupes de rôles d'administrateur

1. Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles auquel vous souhaitez ajouter l’utilisateur ou les utilisateurs,](../media/ITPro-EAC-EditIcon.gif)puis cliquez sur **modifier** ![l’icône modifier.

2. Sous membres, cliquez sur **Ajouter** ![une](../media/ITPro-EAC-AddIcon.gif)icône Ajouter. La fenêtre Sélectionner les membres s'affiche.

3. Recherchez le ou les utilisateurs à ajouter, ou sélectionnez-les dans la liste.

4. Lorsque vous avez sélectionné les utilisateurs à ajouter, cliquez sur **Ajouter**, puis sur **OK**. La fenêtre Sélectionner les membres se ferme.

5. Vous constatez que les utilisateurs ont été ajoutés au volet **Membres**. Cliquez sur **Enregistrer**.

   > [!NOTE]
   > Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées. 
  
## <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a>Utiliser le Centre d'administration Exchange (CAE) pour supprimer des membres de groupes de rôles d'administrateur

1. Dans le centre d’administration Exchange, accédez à **rôles d’administrateur**des **autorisations** \> , cliquez sur le groupe de rôles duquel vous souhaitez supprimer un ou les utilisateurs, puis](../media/ITPro-EAC-EditIcon.gif)cliquez sur **modifier** ![l’icône de modification.

2. Sous membres, sélectionnez le ou les utilisateurs que vous souhaitez supprimer, puis cliquez sur **supprimer** ![l'](../media/ITPro-EAC-RemoveIcon.gif)icône Supprimer.

3. Cliquez sur **Enregistrer** pour enregistrer la modification apportée au groupe de rôles et retourner à la page **Rôles d'administrateur**. Pour vérifier que vous avez supprimé l'utilisateur du groupe de rôles d'administrateur, assurez-vous que le membre n'apparaît plus sous Membres dans le volet Détails relatif au groupe de rôles sélectionné.

   > [!NOTE]
   > Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.
  
## <a name="for-more-information"></a>Pour plus d’informations

[Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md)
