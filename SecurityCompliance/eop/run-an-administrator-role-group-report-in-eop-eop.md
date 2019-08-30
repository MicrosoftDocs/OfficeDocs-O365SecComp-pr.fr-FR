---
title: "Exécution d’un rapport de groupe de rôles d'administrateur dans EOP "
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Les administrateurs peuvent apprendre à exécuter un rapport de groupe de rôles d’administrateur dans Exchange Online Protection (EOP). Ce rapport enregistre les journaux lorsqu’un administrateur ajoute ou supprime des membres des groupes de rôles d’administrateur, Microsoft Exchange Online Protection (EOP) journalise chaque occurrence.
ms.openlocfilehash: 6973574ca1eeabee85dd57bd087ba5d0675da084
ms.sourcegitcommit: 361aab46b1bb295ed2dcc1a417ac81f699b8ff78
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2019
ms.locfileid: "36676506"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a>Exécution d’un rapport de groupe de rôles d'administrateur dans EOP

 Lorsqu’un administrateur ajoute ou supprime des membres dans les groupes de rôles d’administrateur, Exchange Online Protection (EOP) journalise chaque occurrence. Lorsque vous exécutez un rapport de groupe de rôles d’administrateur dans le centre d’administration Exchange, les entrées s’affichent sous la forme de résultats de recherche et incluent les groupes de rôles affectés, la personne qui a modifié l’appartenance au groupe de rôles et le moment, ainsi que les mises à jour d’appartenance. Utilisez ce rapport pour surveiller les modifications aux autorisations administratives attribuées aux utilisateurs dans votre organisation.
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Durée d'exécution estimée : 2 minutes

- Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](../exchange-admin-center-in-exchange-online-protection-eop.md).

- Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez la section « Rapports » de la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).

- Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).

> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a>Utiliser le Centre d'administration Exchange (CAE) pour exécuter un rapport de groupe de rôles d'administrateur

Exécutez le rapport de groupe de rôles d’administrateur pour rechercher les modifications apportées aux groupes de rôles de gestion dans votre organisation dans un intervalle de temps donné.
  
1. Dans le CAE, accédez à **Gestion de la conformité** \> **Audit**, puis sélectionnez **Exécuter un rapport de groupe de rôles d'administrateur**.

2. Sélectionnez la **date de début** et la **date de fin**. Par défaut, le rapport recherche toutes les modifications apportées aux groupes de rôles d'administrateur au cours des deux semaines passées.

3. Pour afficher les modifications apportées à un groupe de rôles précis, cliquez sur **Sélectionnez les groupes de rôles**. Sélectionnez le ou les groupes de rôles dans la boîte de dialogue suivante, puis cliquez sur **OK**. Vous pouvez également laisser le champ vide pour rechercher tous les groupes de rôles qui ont été modifiés.

4. Cliquez sur **Rechercher**.

Si des modifications correspondent aux critères que vous avez spécifiés, elles seront affichées dans le volet des résultats. Cliquez sur un groupe de rôles dans les résultats de la recherche pour afficher les modifications dans le volet d'informations.
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Si vous avez bien exécuté un rapport de groupe de rôles d'administrateur, les groupes de rôles qui ont été modifiés dans la plage de dates s'affichent dans le volet des résultats de la recherche. En cas d'absence de résultats, cela signifie qu'aucune modification aux groupes de rôles n'a eu lieu dans la plage de dates indiquée. Si vous pensez que des résultats devraient apparaître, modifiez la plage de dates et réexécutez le rapport.
  
## <a name="monitor-changes-to-role-group-membership"></a>Surveillances des modifications apportées à l'appartenance à des groupes de rôles

Lorsque des membres sont ajoutés ou supprimés dans groupe de rôles, les résultats de la recherche affichés dans le volet d'informations indiquent que l'appartenance à un groupe de rôles a été mise à jour et répertorient les membres actuels. Les résultats n'indiquent pas explicitement quel utilisateur a été ajouté ou supprimé.
  
Pour déterminer si un utilisateur a été ajouté ou supprimé, vous devez comparer deux entrées séparées dans le rapport. Par exemple, examinons les entrées de journal suivantes pour le groupe de rôles **Support technique**:
  
> 1/27/2018 4:43 PM <br> Administrateur <br> Membres mis à jour : Administrateur;annb,florencef;pilarp <br> 2/06/2018 10:09 AM <br> Administrateur <br> Membres mis à jour : Administrator;annb;florencef;pilarp;tonip <br> 2/19/2018 2:12 PM <br> Administrateur <br> Membres mis à jour : Administrator;annb;florencef;tonip

Dans cet exemple, le compte d'utilisateur Administrateur a apporté les modifications suivantes :
  
- Le 2/06/2018, il a ajouté l’utilisateur tonip.

- Le 2/19/2018, il a supprimé l’utilisateur pilarp.
