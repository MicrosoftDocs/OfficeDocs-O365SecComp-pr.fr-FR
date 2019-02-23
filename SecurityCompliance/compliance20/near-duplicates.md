---
title: Détecter des quasi-duplicatas
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
ms.openlocfilehash: 40270fa1e3a6f7cdf0dd2a83650aa36a935d9a6d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213124"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="6a2d6-102">Détecter des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="6a2d6-102">Near duplicate detection</span></span>

<span data-ttu-id="6a2d6-p101">Considérez un ensemble de documents à examiner dans lequel un sous-ensemble est basé sur le même modèle et qui possède essentiellement le même langage, avec quelques différences ici et là. Si un réviseur peut identifier ce sous-ensemble, passer en revue l'une d'entre elles de façon approfondie et passer en revue les différences pour le reste, il n'aurait pas manqué d'informations uniques pendant une période de temps qui aurait été utilisée pour lire tous les documents. Les groupes de détection near-duplicate regroupent des documents textuellement similaires pour vous aider à améliorer l'efficacité de votre processus de révision.</span><span class="sxs-lookup"><span data-stu-id="6a2d6-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="6a2d6-106">Comment fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="6a2d6-106">How does it work?</span></span>

<span data-ttu-id="6a2d6-p102">Lorsque l'exécution de la détection de doublons est exécutée, le système analyse tous les documents avec du texte. Ensuite, il compare chaque document aux autres pour déterminer si leur similarité est supérieure au seuil défini. Si c'est le cas, les documents sont regroupés. Une fois que tous les documents ont été comparés et regroupés, un document de chaque groupe est marqué comme «tableau croisé dynamique»; lors de l'examen de vos documents, vous pouvez commencer par examiner un tableau croisé dynamique et passer en revue les autres documents dans le même jeu presque en double, en vous concentrant sur la différence entre le tableau croisé dynamique et le document en cours de révision.</span><span class="sxs-lookup"><span data-stu-id="6a2d6-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>