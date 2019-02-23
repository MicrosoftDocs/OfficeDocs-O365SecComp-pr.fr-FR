---
title: Gestion des dépositaires dans un cas avancé eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 0c33335ecc103a97090dacaa769315ad9413b3c6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214974"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a>Gestion des dépositaires dans un cas avancé eDiscovery (aperçu)

L'onglet dépositaires contient une liste triable de tous les dépositaires dans le cas. Une fois que vous avez ajouté des dépositaires à un cas, les détails de chaque dépositaire seront automatiquement collectés à partir d'Azure Active Directory.

## <a name="viewing-custodian-details"></a>Affichage des détails des dépositaires

La page de menu volant contenant les détails des dépositaires s'affiche une fois que vous avez ajouté un dépositaire à une demande **** de devis et que vous l'avez sélectionné dans la liste de l'onglet dépositaires. À partir de là, vous pouvez afficher tous les détails relatifs à ce dépositaire. La page de menu volant contient les champs suivants:

- Informations de contact

  - **Nom d'affichage**: nom affiché dans le carnet d'adresses pour le dépositaire. Il s'agit généralement de la combinaison du prénom du dépositaire, de l'initiale du deuxième prénom et du nom de famille.
  - **Mail/SMTP**: adresse SMTP du dépositaire, par exemple, Jeff@contoso.onmicrosoft.com.  
  - **Titre**: fonction du dépositaire.
  - **Department**: nom du service dans lequel le dépositaire travaille.
  - **Responsable**: le responsable du dépositaire. Le responsable désigné recevra toutes les communications d'escalade de ce dépositaire.
  
- Informations d’emplacement

  - **Ville**: ville dans laquelle se trouve le dépositaire.
  - **État**: État ou province dans l'adresse du dépositaire.
  - **Pays/région**: pays/région où se trouve le dépositaire; par exemple, «US» ou «UK».
  - **Office**: l'emplacement du bureau dans le lieu d'activité du dépositaire.

- Informations sur les cas

  - **État de suspension**: indique si le dépositaire a été mis en attente. 
  - **Statut**de la communication: indique si un avis de mise en attente a été émis pour le dépositaire. Si le dépositaire a reçu une notification, celle-ci sera marquée comme étant *publiée*. Si le dépositaire n'a pas reçu de notification, ce statut est *annulé*. 
  - **État**: état du dépositaire dans le cas. Cela sera *actif* si le dépositaire est toujours en conservation pour le cas. Si un dépositaire est supprimé d'un incident, son statut passe à *lancé*. 

- État de traitement

  - **État**de l'indexation: indique l'état de la tâche d'indexation approfondie.  
  - **Indexation de la dernière heure de mise à jour**: indique l'datestamp de la dernière fois que le travail d'indexation profonde a été déclenché.
  - **Sources de données**: affiche le nombre de boîtes aux lettres, de sites et d'équipes qui ont été sélectionnées pour le dépositaire.

## <a name="updating-a-custodian"></a>Mise à jour d'un dépositaire

Lors de l'évolution de votre cas, vous pouvez découvrir qu'il peut y avoir des sources de données supplémentaires pertinentes pour un dépositaire spécifique & votre cas. Dans d'autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été vérifiées et considérées comme non pertinentes.

Pour mettre à jour un dépositaire et les sources de données sélectionnées:

1. Sélectionnez un incident existant dans la découverte **électronique avancée _GT_ Advanced eDiscovery (aperçu)**.
  
2. Dans le cas, cliquez sur **** l'onglet dépositaires.
  
3. Sélectionnez le ou les dépositaires dans la liste, puis cliquez sur **modifier les sources**.
  
4. Mettez à jour les sélections pour les emplacements Exchange et OneDrive en cliquant sur **choisir les sources de données**.
  
5. Ajouter ou supprimer des équipes, SharePoint ou des boîtes aux lettres Exchange mappées à l'utilisateur en cliquant pour **Sélectionner des sources de données supplémentaires**. Pour plus d'informations sur la façon de mapper des sources de données à un dépositaire, consultez la rubrique [Ajouter des dépositaires à un cas](add-custodians-to-case.md).
  
6. Pour mettre à jour l'état de conservation des dépositaires, cliquez sur **Placer**les conservations privatives de Troie et activez ou désactivez la suspension pour les dépositaires.

> [!TIP]
> Vous pouvez sélectionner plusieurs dépositaires pour effectuer des actions en bloc, comme la réindexation, le lancement ou la modification d'un ensemble de dépositaires.

## <a name="resolving-custodian-processing-errors"></a>Résolution des erreurs de traitement des dépositaires

Dans la plupart des flux de travail légaux, après avoir ajouté des dépositaires à une enquête spécifique, un sous-ensemble des données des utilisateurs est recherché. En raison de la taille des fichiers volumineux ou d'une altération possible, certains éléments des sources de données des dépositaires peuvent être partiellement indexés. À l'aide de la fonctionnalité d'indexation approfondie avancée eDiscovery (aperçu), ces éléments partiellement indexés peuvent être automatiquement corrigés en réanalysant et en réindexant ces éléments à la demande. 

Lorsqu'un dépositaire est ajouté à un cas, ses données sont automatiquement «indexées en profondeur», ce qui permet aux utilisateurs de laisser ces éléments partiellement indexés au lieu de devoir télécharger, corriger et réexécuter les recherches en dehors d'Office 365. Pendant le cycle de vie d'un cas, un utilisateur peut corriger des éléments ou ajouter de nouvelles sources de données pour un dépositaire donné. Cela peut nécessiter la mise à jour de l'index des dépositaires. 

Pour déclencher un processus de réindexation afin d'adresser des éléments partiellement indexés:

1. Accédez à **eDiscovery _GT_ Advanced eDiscovery (Preview)** et sélectionnez un incident existant.

2. Dans le cas, cliquez sur l' **onglet dépositaires**. 

3. Sélectionnez le ou les dépositaires qui doivent être réindexés, puis cliquez sur **mettre à jour l'index** sur la page de menu volant.

4. Vérifiez l'état de l'index dépositaire en cliquant sur le lien dans la colonne **État du travail d'indexation** sous l'onglet **dépositaires** .  

5. L'état du processus de réindexation peut également être suivi sous l'onglet **tâches** .

Pour plus d'informations sur la réindexation et la correction des éléments partiellement indexés, voir [Fix Processing Errors](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Libération d'un dépositaire à partir d'un cas

Un dépositaire est publié dans les situations où un litige est clos, un dépositaire n'est plus tenu de conserver le contenu d'un cas ou lorsqu'un dépositaire est considéré comme n'étant plus pertinent à un cas particulier. 

Si vous libérez un dépositaire après la publication d'une notification de mise en attente, un avis de publication est envoyé au dépositaire. En outre, toutes les conservations privatives de Troie attribuées aux dépositaires libérés seront également supprimées.

Si le dépositaire a été placé sur un blocage automatique, où il n'a pas reçu de notifications de conservation légale, toutes les conservations privatives attribuées aux dépositaires libérés seront supprimées.  

Pour libérer un dépositaire: 

1.  Accédez à l' **** onglet dépositaires.

2.  Sélectionnez le dépositaire dans la liste, puis cliquez sur **libérer** les dépositaires sur la page de menu volant.

    Le statut du dépositaire sous l'onglet **dépositaires** est défini sur **Released** et le **statut de blocage** sur la page flyout est modifié sur inactive. **** 

> [!TIP]
> Un dépositaire peut être impliqué simultanément dans plusieurs questions juridiques. Lorsqu'un dépositaire est émis à partir d'un cas, les conservations et notifications sur d'autres sujets ne seront pas affectées.

## <a name="related-information"></a>Informations connexes

 - [Correction d’erreur lors du traitement des données](error-remediation.md) 
- [Utiliser des communications](managing-custodian-communications.md)
