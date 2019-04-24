---
title: Baliser des documents dans un ensemble de travail
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
ms.openlocfilehash: 510a10386ea51c0397408450f9fc700e9ce6db9c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241110"
---
# <a name="tag-documents-in-a-working-set"></a>Baliser des documents dans un ensemble de travail

L'organisation du contenu dans un jeu de travail est importante pour effectuer différents flux de travail dans le processus de découverte électronique. Cela inclut les opérations suivantes :

-  Élimination de contenu inutile

- Identification du contenu pertinent
 
-  Identification du contenu qui doit être révisé par un expert ou un avocat

Lorsque des experts, des avocats ou d'autres utilisateurs consultent du contenu dans un jeu de travail, leurs opinions liées au contenu peuvent être capturées à l'aide de balises. Par exemple, si l'intention est d'effectuer une élimination de contenu inutile, un utilisateur peut marquer des documents avec une balise telle que «non réactif». Une fois que le contenu a été révisé et balisé, une recherche de jeu de travail peut être créée pour exclure le contenu marqué comme «non réactif», ce qui élimine ce contenu des étapes suivantes dans le flux de travail de découverte électronique. Le panneau des balises peut être personnalisé pour chaque cas afin que les balises puissent prendre en charge le flux de travail de révision prévu.

## <a name="tag-types"></a>Types de balises

Advanced eDiscovery (aperçu) fournit deux types de balises:

- **Balises à choix unique** : limite les utilisateurs à la sélection d'une balise unique au sein d'un groupe. Cela peut être utile pour s'assurer que les utilisateurs ne sélectionnent pas les balises conflictuelles telles que «réactif» et «ne répond pas». 

- **Balises Choice multiples** : permet aux utilisateurs de sélectionner plusieurs balises au sein d'un groupe.

## <a name="tag-structure"></a>Structure des balises

En plus des types de balises, la structure de la manière dont les balises sont organisation dans le panneau de balises peut être utilisée pour faciliter l'utilisation de documents de marquage. Les balises sont regroupées par sections. Working Set search prend en charge la fonctionnalité de recherche par balise et par section tag. Cela signifie que vous pouvez créer une recherche de jeu de travail pour récupérer des documents marqués avec une balise dans une section.

![Sections de balise dans le panneau des balises](../media/Tagtypes.png)

Les balises peuvent être organisées de manière plus approfondie en les imbriquant dans une section. Par exemple, si l'intention est d'identifier et de baliser un contenu privilégié, l'imbrication peut être utilisée pour indiquer clairement qu'un utilisateur peut marquer un document comme «privilégié» et sélectionner le type de privilège en vérifiant la balise imbriquée appropriée.

![Balises imbriquées dans une section de balise](../media/Nestingtags.png)

## <a name="applying-tags"></a>Application de balises

Il existe plusieurs façons d'appliquer une balise au contenu.

### <a name="tagging-a-single-document"></a>Marquage d'un document unique

Lors de l'affichage d'un document dans une plage de travail, vous pouvez afficher les balises qu'une révision peut utiliser en cliquant sur **panneau de codage**.

![Cliquez sur panneau des balises pour afficher le panneau Balises.](../media/Singledoctag.png)

Cela vous permet d'appliquer des balises au document affiché dans la visionneuse.

### <a name="bulk-tagging"></a>Balisage en bloc

L'étiquetage en bloc peut être réalisé en sélectionnant plusieurs fichiers dans la grille de résultats, puis en utilisant les balises dans le **panneau codage** de la même manière que pour le marquage des documents uniques. L'annulation de balisage en bloc peut être réalisée en sélectionnant deux fois les balises; le premier clic applique la balise, et la deuxième sélection garantit que la balise est effacée pour tous les fichiers sélectionnés.

![Capture d'écran d'une description de téléphone de cellule générée automatiquement](../media/Bulktag.png)

> [!NOTE]
> Lors de l'étiquetage en bloc, le panneau balisage affiche un nombre de fichiers balisés pour chaque balise dans le panneau.

### <a name="tagging-in-other-review-panels"></a>Balisage dans d'autres panneaux de révision

Lors de l'examen des documents, vous pouvez utiliser les autres panneaux de révision pour examiner les autres caractéristiques des documents dans la grille de résultats. Cela inclut l'examen d'autres documents connexes, des threads de messagerie, des doublons de doublons et des doublons de hachage. Par exemple, lorsque vous consultez des documents connexes (à l'aide du panneau de vérification de la **famille de documents** ), vous pouvez réduire considérablement le temps d'examen en bloc des documents associés. Par exemple, si un message électronique comporte plusieurs pièces jointes et que vous souhaitez vous assurer que toute la famille est marquée de manière cohérente.

Par exemple, voici comment afficher le **panneau codage** lors de l'utilisation du panneau de vérification de la **famille de documents** :

1. Le panneau de vérification étant ouvert pour un document sélectionné (par exemple, affichage de la liste du contenu associé dans le panneau de vérification de la **famille de documents** , cliquez sur **documents de code** en haut du panneau révision actuel.

   Le panneau codage est affiché dans une fenêtre contextuelle.

2. Choisissez une ou plusieurs balises à appliquer au document sélectionné. 

3. Pour marquer tous les documents, sélectionnez tous les documents dans le panneau de la **famille** de documents, cliquez sur **documents de code**, puis sélectionnez les balises à appliquer à l'ensemble de la famille de documents.

![Capture d'écran d'une description de publication de réseau social générée automatiquement](../media/Relatedtag.png)
