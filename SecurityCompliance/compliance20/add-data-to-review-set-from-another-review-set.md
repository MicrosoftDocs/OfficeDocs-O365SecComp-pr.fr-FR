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
ms.openlocfilehash: 3a4d0d309daa5af9830f98215ca09321429785ee
ms.sourcegitcommit: 25595bc8fae96bc23b7b6d7102a22f37878987c0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33641648"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a>Ajouter des données à un jeu de révision à partir d’un autre ensemble de révision

Dans certains cas, il peut s’avérer nécessaire de supprimer une partie des documents d’un ensemble de révision et de les utiliser individuellement dans un autre ensemble de révision.  Ceci est particulièrement utile si vous avez consulté du contenu dans un jeu de révision et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.

Suivez le flux de travail de cet article pour ajouter du contenu d’un jeu de révision à un autre.

## <a name="before-you-begin"></a>Avant de commencer

Avant de commencer, vous devez créer un nouveau jeu de révision auquel ajouter les données.  Un nouvel ensemble de révision peut être ajouté sous l’onglet **ensembles de révision** de la case. Pour plus d’informations, consultez [la rubrique Create a Review Set](managing-review-sets.md#create-a-review-set).

## <a name="step-1-identify-content-to-add-to-another-review-set"></a>Étape 1: identifier le contenu à ajouter à un autre ensemble de validation

Vous pouvez ajouter du contenu d’un jeu de réexamen à un autre en sélectionnant des documents spécifiques dans le jeu de révision source ou b seleting tous les éléments renvoyés par la requête Set Review.  Si vous ajoutez des éléments sélectionnés, sélectionnez-les, cliquez sur **action**, puis sur **Ajouter à un autre ensemble de réexamen**.

![Ajouter à un autre ensemble de révision](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a>Étape 2: spécification des options d’ajout à un autre ensemble de réexamen

Dans la page de menu **Ajouter à un autre jeu de réviseur options** , choisissez l’ensemble de révision auquel vous souhaitez ajouter les éléments. Indiquez si vous souhaitez ajouter **tous les résultats de recherche ou les** **éléments sélectionnés**.  Informations supplémentaires fournit des options permettant d’inclure toutes les métadonnées des éléments et d’inclure les balises (en activant la case à cocher **étiquettes** ) à partir de l’ensemble de révision source lorsque les documents sont ajoutés au nouvel ensemble de révision.  

![Ajouter à un autre ensemble de révision](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

Une fois que vous avez cliqué sur **OK**, un nouveau travail (nommé **Ajout de données à un autre ensemble de vérification**) est créé pour ajouter le contenu à un autre ensemble de révision.  Vous pouvez accéder à l’onglet **travaux** et surveiller la progression de ce travail. Pour plus d’informations, consultez la rubrique [Manage Jobs](managing-jobs-ediscovery20.md).
