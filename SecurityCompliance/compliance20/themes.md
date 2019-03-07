---
title: Thèmes
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
ms.openlocfilehash: 7c9d1a52acef48d96816fefbb1c836032d262b93
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454676"
---
# <a name="themes"></a><span data-ttu-id="c27b0-102">Thèmes</span><span class="sxs-lookup"><span data-stu-id="c27b0-102">Themes</span></span>
<span data-ttu-id="c27b0-103">Comment une personne écrit-t-elle un document?</span><span class="sxs-lookup"><span data-stu-id="c27b0-103">How does a person write a document?</span></span> <span data-ttu-id="c27b0-104">Elles commencent généralement par une ou plusieurs idées qu'elles souhaitent transférer dans le document, et composent des mots qui s'alignent sur les idées.</span><span class="sxs-lookup"><span data-stu-id="c27b0-104">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="c27b0-105">Plus l'idée est fréquente, plus le nombre de mots liés à cette idée est important.</span><span class="sxs-lookup"><span data-stu-id="c27b0-105">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="c27b0-106">Cela indique le mode d'utilisation des documents par les utilisateurs; l'essentiel de la lecture d'un document est l'idée des idées que le document tente de transmettre, et les idées qui apparaissent où et les relations entre les idées.</span><span class="sxs-lookup"><span data-stu-id="c27b0-106">This informs how people consume documents as well; the important thing to get from reading a document is the ideas that the document is trying to convey, and which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="c27b0-107">Cela peut être étendu à la manière dont une personne souhaite utiliser un ensemble de documents.</span><span class="sxs-lookup"><span data-stu-id="c27b0-107">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="c27b0-108">Ils veulent voir quelles idées sont présentes dans les ensembles et quels documents parlent de ces idées.</span><span class="sxs-lookup"><span data-stu-id="c27b0-108">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="c27b0-109">En outre, si elle trouve un document d'intérêt particulier, elle souhaite pouvoir consulter des documents qui abordent des idées similaires.</span><span class="sxs-lookup"><span data-stu-id="c27b0-109">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="c27b0-110">Le module themes tente de reproduire la raison pour les êtres humains des documents en analysant les «thèmes» présentés dans un jeu de travail et en les affectant à des documents.</span><span class="sxs-lookup"><span data-stu-id="c27b0-110">Themes module tries to mimic how humans reason about documents, by analyzing the "themes" that are discussed in a working set and assigning them to documents.</span></span> <span data-ttu-id="c27b0-111">Les thèmes se déplacent d'une étape et identifient par document le «thème dominant»; autrement dit, le thème qui apparaît le plus.</span><span class="sxs-lookup"><span data-stu-id="c27b0-111">Themes goes one step further and identifies per document the "dominant theme"; i.e. the theme that appears the most.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="c27b0-112">Comment fonctionne le thème?</span><span class="sxs-lookup"><span data-stu-id="c27b0-112">How does Themes work?</span></span>
<span data-ttu-id="c27b0-113">Themes analyse les documents avec du texte dans une plage de travail pour analyser les thèmes communs qui apparaissent dans les documents.</span><span class="sxs-lookup"><span data-stu-id="c27b0-113">Themes analyzes documents with text in a working set to parse out common themes that appear accross the documents.</span></span> <span data-ttu-id="c27b0-114">Ensuite, il affecte ces thèmes aux documents dans lesquels ils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="c27b0-114">Then, it assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="c27b0-115">Il s'étiquette également avec des mots utilisés dans les documents représentatifs du thème.</span><span class="sxs-lookup"><span data-stu-id="c27b0-115">It also labels each with words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="c27b0-116">Dans la mesure où un document peut être associé à plusieurs sujets, dans de nombreux cas, un document comporte plusieurs thèmes.</span><span class="sxs-lookup"><span data-stu-id="c27b0-116">Since a document can be about more than one subject matter, in many cases a document has more than one themes assigned to it.</span></span> <span data-ttu-id="c27b0-117">Le thème qui apparaît le plus en évidence dans un document est désigné comme son thème dominant.</span><span class="sxs-lookup"><span data-stu-id="c27b0-117">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>