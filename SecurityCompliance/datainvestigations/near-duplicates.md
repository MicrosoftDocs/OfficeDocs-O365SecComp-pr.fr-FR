---
title: Détection des quasi-duplicatas
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
ms.openlocfilehash: 941809193a3342d8c7b9de991370848aee4af070
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257662"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="5f729-102">Détection des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="5f729-102">Near duplicate detection</span></span>

<span data-ttu-id="5f729-103">Considérez un ensemble de documents à examiner dans lequel un sous-ensemble est basé sur le même modèle et qui possède essentiellement le même langage, avec quelques différences ici et là.</span><span class="sxs-lookup"><span data-stu-id="5f729-103">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there.</span></span> <span data-ttu-id="5f729-104">Si un réviseur peut identifier ce sous-ensemble, passer en revue l'une d'entre elles de façon approfondie et passer en revue les différences pour le reste, il n'aurait pas manqué d'informations uniques pendant une période de temps qui aurait été utilisée pour lire tous les documents.</span><span class="sxs-lookup"><span data-stu-id="5f729-104">If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover.</span></span> <span data-ttu-id="5f729-105">Les groupes de détection near-duplicate regroupent des documents textuellement similaires pour vous aider à améliorer l'efficacité de votre processus de révision.</span><span class="sxs-lookup"><span data-stu-id="5f729-105">Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="5f729-106">Comment fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="5f729-106">How does it work?</span></span>

<span data-ttu-id="5f729-107">Lorsque l'exécution de la détection de doublons est exécutée, le système analyse tous les documents avec du texte.</span><span class="sxs-lookup"><span data-stu-id="5f729-107">When near duplicate detection is run, the system parses every document with text.</span></span> <span data-ttu-id="5f729-108">Ensuite, il compare chaque document aux autres pour déterminer si leur similarité est supérieure au seuil défini.</span><span class="sxs-lookup"><span data-stu-id="5f729-108">Then, it compares every document against each other to determine whether their similarity is greater than the set threshold.</span></span> <span data-ttu-id="5f729-109">Si c'est le cas, les documents sont regroupés.</span><span class="sxs-lookup"><span data-stu-id="5f729-109">If it is, the documents are grouped together.</span></span> <span data-ttu-id="5f729-110">Une fois que tous les documents ont été comparés et regroupés, un document de chaque groupe est marqué comme «tableau croisé dynamique»; lors de l'examen de vos documents, vous pouvez commencer par examiner un tableau croisé dynamique et passer en revue les autres documents dans le même jeu presque en double, en vous concentrant sur la différence entre le tableau croisé dynamique et le document en cours de révision.</span><span class="sxs-lookup"><span data-stu-id="5f729-110">Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>