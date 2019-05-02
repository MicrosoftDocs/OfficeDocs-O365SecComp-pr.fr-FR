---
title: Ajouter des données d’un ensemble de révision à un autre ensemble de révision
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
description: ''
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527162"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a>Ajouter des données à un jeu de révision à partir d’un autre ensemble de révision

Dans certains cas, il peut s’avérer nécessaire de supprimer une partie des documents d’un ensemble de révision et de les utiliser individuellement dans un autre ensemble de révision.  Ceci est particulièrement utile si vous avez consulté du contenu dans un jeu de révision et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.

Utilisez le flux de travail suivant pour ajouter du contenu d’un jeu de révision à un autre.

## <a name="before-you-begin"></a>Avant de commencer

Avant de commencer, vous devez créer un nouveau jeu de révision auquel ajouter les données.  Un nouvel ensemble de révision peut être ajouté sous l’onglet **ensembles de révision** de la case. Pour plus d’informations, consultez la rubrique [Manage Review sets](managing-review-sets.md).

## <a name="step-1-identify-content-to-add-to-another-review-set"></a>Étape 1: identifier le contenu à ajouter à un autre ensemble de validation

Vous pouvez ajouter du contenu à un jeu de vérification en sélectionnant des e-mails et des documents dans la grille du document ou tous les éléments d’un résultat de recherche.  Si vous choisissez d’ajouter des éléments sélectionnés, sélectionnez les éléments, cliquez sur **action**, puis sur **Ajouter à un autre ensemble de réexamen**.

![Ajouter à un autre ensemble de révision](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a>Étape 2: spécification des options d’ajout à un autre ensemble de réexamen

Dans la page **Ajouter à un autre jeu de réexamen** , choisissez l’ensemble de révision auquel vous souhaitez ajouter les éléments. Indiquez si vous souhaitez ajouter **tous les résultats de recherche ou les** **éléments sélectionnés**.  Informations supplémentaires fournit des options pour inclure toutes les métadonnées des éléments et pour finir si les balises de document doivent être incluses dans le nouveau jeu de révision.  Une fois que vous avez cliqué sur **OK** , un nouveau travail est créé pour ajouter le contenu à un jeu de révision; vous pouvez surveiller la progression de cette tâche dans l’onglet **travail** . Pour plus d’informations, consultez la rubrique [Manage Jobs](managing-jobs-ediscovery20.md).

![Ajouter à un autre ensemble de révision](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
