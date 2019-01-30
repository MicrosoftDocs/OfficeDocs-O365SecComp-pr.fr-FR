---
title: Près de la détection des doublons
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607666"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="6379c-102">Près de la détection des doublons</span><span class="sxs-lookup"><span data-stu-id="6379c-102">Near duplicate detection</span></span>

<span data-ttu-id="6379c-p101">Envisagez un ensemble de documents à réviser dans lequel un sous-ensemble basé sur le même modèle et a principalement le même réutilisable dans un langage, avec quelques différences ici et là. Si un réviseur peut identifier ce sous-ensemble, passez en revue minutieusement un d'entre eux et passez en revue les différences pour le reste, ils ne seraient pas ont manqué aucune information unique tandis que prendre qu’une fraction de temps qui auraient à lire tous les documents garde à la page de garde. Détection des doublons NEAR regroupe les documents textuelle similaires ensemble pour vous aider à améliorer l’efficacité de votre processus de révision.</span><span class="sxs-lookup"><span data-stu-id="6379c-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="6379c-106">Comment fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="6379c-106">How does it work?</span></span>

<span data-ttu-id="6379c-p102">Lorsque près de détection des doublons est exécuté, le système analyse tous les documents avec du texte. Ensuite, il compare tous les documents par rapport aux autres pour déterminer si leur similarité est supérieure au seuil d’ensemble. S’il s’agit, les documents sont regroupés. Une fois que tous les documents ont été comparées et regroupées, chaque groupe d’un document est marqué comme « pivot » ; en examinant vos documents, vous pouvez consulter un tableau croisé dynamique tout d’abord et passez en revue les autres documents dans la même près de jeu en double, en mettant l’accent sur la différence entre le tableau croisé dynamique et le document est en cours de révision.</span><span class="sxs-lookup"><span data-stu-id="6379c-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>