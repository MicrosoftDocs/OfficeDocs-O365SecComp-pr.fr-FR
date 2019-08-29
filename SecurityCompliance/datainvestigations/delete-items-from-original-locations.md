---
title: Supprimer des éléments de leur emplacement d’origine
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article explique comment utiliser l’outil nouvelles enquêtes de données (aperçu) dans le centre de sécurité & conformité pour supprimer des éléments de leur emplacement d’origine.
ms.openlocfilehash: 9c8b7c0707183e9bd0f423790b47f9aa60e35912
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36654129"
---
# <a name="delete-items-from-their-original-location-preview"></a>Supprimer des éléments de leur emplacement d’origine (aperçu)

La fonctionnalité permettant de supprimer des éléments de leur emplacement d’origine est en aperçu.

À l’aide des analyses de données, vous pouvez supprimer des éléments de leur emplacement d’origine. Cela signifie que vous pouvez supprimer des éléments de boîtes aux lettres Exchange, de sites SharePoint et de comptes OneDrive au sein de votre organisation. Étant donné que vous avez collecté des éléments en tant que preuves, vous disposez de copies des éléments conservés dans l’ensemble de preuves pour une meilleure étude ou conserver une référence.

## <a name="before-you-begin"></a>Avant de commencer

- Pour supprimer des éléments, vous devez disposer du rôle de **recherche et de purge** dans le centre de sécurité & conformité. Ce rôle est affecté par défaut au groupe de rôles intégré de l’expérimentation de données. 

- La procédure de cette rubrique suppose que vous avez exécuté une recherche associée à une enquête et ajouté les résultats de la recherche à un jeu de preuves. Une fois que les résultats de la recherche sont dans preuve, vous pouvez sélectionner un ou plusieurs éléments à supprimer. Pour plus d’informations, consultez la rubrique [Rechercher des données dans une enquête](search-for-data.md).

- Il est important de garder à l’esprit que seuls les éléments des emplacements de contenu d’origine (par exemple, les boîtes aux lettres Exchange, les sites SharePoint et les comptes OneDrive) sont supprimés. Ces éléments ne sont pas supprimés de l’ensemble de preuves. Cela est dû au fait que les éléments d’un jeu de preuves sont des copies de l’original. Ces éléments sont copiés lorsque vous avez ajouté les résultats d’une recherche à un ensemble de preuves.

## <a name="delete-items"></a>Supprimer des éléments

Pour supprimer des éléments de leur emplacement d’origine, procédez comme suit:

1. Dans l’outil **enquêtes de données** , ouvrez l’enquête de données qui contient les éléments à supprimer, puis cliquez sur l’onglet **preuve** .

2. Sélectionnez les éléments que vous souhaitez supprimer. Vous pouvez sélectionner tous les éléments de l’ensemble de preuves ou simplement un sous-ensemble d’éléments. 

   > [!NOTE]
   > Si vous sélectionnez les pièces jointes d’un message électronique ou un fichier joint à un document dans SharePoint et OneDrive, l’élément parent est également sélectionné et supprimé lorsque l’élément est supprimé de son emplacement d’origine. De même, si vous sélectionnez un élément qui comporte des pièces jointes, l’élément d’élément parent et toutes les pièces jointes sont supprimés.
 
2. Cliquez sur **action** , puis sur **Supprimer les éléments des emplacements d’origine**.

   ![Cliquez sur action, puis sur supprimer les éléments des emplacements d’origine](../media/DataInvestigationsDeleteItems1.png)

3. Sur la page de menu volant, vérifiez le nombre d’éléments et les documents enfants associés qui seront supprimés, puis cliquez sur **supprimer**.

   ![La page de menu volant affiche le nombre d’éléments et les documents joints sélectionnés pour suppression.](../media/DataInvestigationsDeleteItems2.png)

   > [!NOTE]
   > Dans la capture d’écran précédente, le nombre d’éléments indique le nombre d’éléments sélectionnés pour la suppression. Le nombre de documents indique le nombre total d’éléments, y compris les fichiers joints à un élément parent. Par exemple, si vous sélectionnez un message électronique et que celui-ci contient un document Word joint, le nombre d’éléments et de documents affichés sous **documents sélectionnés seulement** est **1 élément (2 documents)**.

Vous pouvez suivre la progression de la tâche **Supprimer les éléments à partir des emplacements d’origine** dans l’onglet **travaux** . cliquez sur le travail pour afficher la page de menu volant. 

![Page de menu volant pour supprimer des éléments du travail d’origine](../media/DataInvestigationsDeleteItems3.png)

Lorsque les éléments de la tâche sont supprimés, le statut du travail est défini sur **réussi**. L’heure et la date du travail terminé sont également affichées. 

![Tâche de suppression des éléments terminée](../media/DataInvestigationsDeleteItems4.png)

> [!NOTE]
> Il se peut que vous receviez un état de **réussite partielle** pour le travail **supprimer des éléments de l’emplacement d’origine** . Il existe un certain nombre de situations qui entraînent cet état de travail. Pour plus d’informations, reportez-vous à la section [suppressions partiellement terminées](#partially-successful-deletions) de cet article.

## <a name="what-happens-when-you-delete-items"></a>Que se passe-t-il lorsque vous supprimez des éléments?

Pour l’instant, lorsque vous supprimez des éléments de leur emplacement de contenu d’origine, les éléments sont supprimés de manière *récupérable*. Cela signifie que les éléments sont déplacés vers un emplacement spécial et conservés jusqu’à l’expiration de la période de rétention des éléments supprimés et qu’un élément est marqué pour suppression définitive d’Office 365. Les éléments supprimés de manière récupérable signifient que les utilisateurs peuvent toujours récupérer ces éléments jusqu’à l’expiration de la période de rétention. Voici des descriptions de ce qui se produit lorsque des éléments sont supprimés de manière récupérable des boîtes aux lettres Exchange et des sites SharePoint et OneDrive entreprise, et ce que les utilisateurs peuvent faire après la suppression des éléments de leur emplacement d’origine.

- **Boîtes aux lettres:** Lorsqu’un élément de boîte aux lettres est supprimé de manière récupérable, il est déplacé vers le dossier éléments récupérables dans la boîte aux lettres. Ce comportement est semblable à celui où un utilisateur supprime un élément du dossier éléments supprimés ou supprime définitivement un élément en appuyant sur Maj + Suppr. À ce stade, l’utilisateur peut récupérer l’élément jusqu’à l’expiration de la période de rétention des éléments supprimés. Dans Office 365, la période de rétention des éléments supprimés est de 14 jours par défaut, mais un administrateur peut augmenter la période de rétention à 30 jours. Une fois la période de rétention expirée, l’élément est déplacé vers un dossier ** masqué (appelé le dossier purges). L’élément est définitivement supprimé d’Office 365 la prochaine fois que la boîte aux lettres est traitée. Les boîtes aux lettres sont traitées une fois tous les sept jours).

- **Sites SharePoint et OneDrive:** Lorsqu’un fichier ou un document sur un site est supprimé de manière récupérable, il est déplacé vers la corbeille du site (également appelée corbeille du *premier niveau* ). L’élément reste dans la corbeille pendant 93 jours (la période de rétention des éléments supprimés pour les sites dans Office 365). Pendant la période de 93 jours, les éléments supprimés peuvent toujours être récupérés par un administrateur de collection de sites dans SharePoint ou par l’utilisateur ou l’administrateur dans OneDrive. Les éléments peuvent également être supprimés de la corbeille First-stage. Lorsque cela se produit, les éléments sont déplacés vers la corbeille de la collection de sites, appelée corbeille *secondaire* . La période de rétention est de 93 jours pour les corbeilles de première et deuxième étape. Cela signifie que la rétention de la Corbeille secondaire commence lors de la suppression initiale de l’élément. Cela signifie que le temps de rétention maximal total est de 93 jours pour les deux Corbeilles. Si un élément est supprimé de la Corbeille secondaire (manuellement par un administrateur ou automatiquement à l’expiration de la période de rétention), il n’est plus accessible par un administrateur.

## <a name="what-happens-if-a-content-location-is-on-hold"></a>Que se passe-t-il si un emplacement de contenu est en conservation?

Dans Office 365, les boîtes aux lettres et les sites peuvent être placés en conservation ou affectés à une stratégie de rétention. Cela signifie que rien n’est définitivement supprimé jusqu’à ce que la période de rétention d’un élément expire ou jusqu’à ce que la conservation soit supprimée. Même si vous supprimez un élément de son emplacement d’origine, il se peut que l’élément ne soit pas supprimé définitivement d’Office 365. Par exemple, si une boîte aux lettres est en attente, les éléments supprimés de manière récupérable finissent par être déplacés vers purges ou DiscoveryHold sous-dossiers dans le dossier éléments récupérables et conservés jusqu’à l’expiration de la durée ou de la période de rétention. Pour les sites, une copie de l’élément qui est déplacée vers la corbeille est copiée dans la bibliothèque de conservation de conservation qui est créée lorsqu’une stratégie de conservation ou de rétention est placée sur un site.

## <a name="partially-successful-deletions"></a>Suppressions partiellement réussies

Une fois que l’exécution de la tâche **Supprimer les éléments de l’emplacement d’origine** est terminée, vous pouvez recevoir un état de travail **partiellement réussi**. En règle générale, cet État indique que le travail a été exécuté correctement, mais que tous les éléments n’ont pas été supprimés de manière récupérable. Voici une liste des raisons qui entraînent des suppressions partiellement réussies:

- Un élément de boîte aux lettres était déjà situé dans le dossier éléments récupérables dans la boîte aux lettres source.

- Un élément de boîte aux lettres a été purgé du dossier éléments récupérables dans la boîte aux lettres source.

- Un document se trouvait déjà dans la corbeille première étape d’un site SharePoint ou OneDrive.

- Un document a été déplacé vers un autre site SharePoint après avoir été ajouté à l’ensemble de preuves. Dans ce cas, le document n’est pas déplacé vers la corbeille du site vers lequel il a été déplacé.

- Un document a été définitivement supprimé dans SharePoint ou OneDrive (déplacé vers la Corbeille secondaire) après avoir été ajouté à l’ensemble de preuves.
