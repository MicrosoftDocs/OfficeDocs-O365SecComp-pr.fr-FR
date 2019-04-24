---
title: Analyser les données d'une plage de travail dans Advanced eDiscovery (aperçu)
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
ms.openlocfilehash: e3f3e863423fe4312a944eb6f04a58182e11665c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243235"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="97d8a-102">Analyser les données d'une plage de travail dans Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="97d8a-102">Analyze data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="97d8a-103">Lorsque le nombre de documents collectés est important, il peut s'avérer difficile de les examiner tous.</span><span class="sxs-lookup"><span data-stu-id="97d8a-103">When the number of collected documents is large, it can be quite difficult to review them all.</span></span> <span data-ttu-id="97d8a-104">Advanced eDiscovery (aperçu) fournit un certain nombre d'outils pour analyser les documents afin de réduire le volume des documents à examiner sans perte d'informations et pour vous aider à organiser les documents de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="97d8a-104">Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="97d8a-105">Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="97d8a-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="97d8a-106">Détecter des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="97d8a-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="97d8a-107">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="97d8a-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="97d8a-108">Thèmes</span><span class="sxs-lookup"><span data-stu-id="97d8a-108">Themes</span></span>](themes.md)

<span data-ttu-id="97d8a-109">Pour analyser les données d'une plage de travail:</span><span class="sxs-lookup"><span data-stu-id="97d8a-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="97d8a-110">ConFigurez les paramètres d'analyse pour votre cas.</span><span class="sxs-lookup"><span data-stu-id="97d8a-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="97d8a-111">Pour plus d'informations, consultez la rubrique [configurer les paramètres de recherche et d'analyse](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="97d8a-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="97d8a-112">Ouvrez le jeu de travail que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="97d8a-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="97d8a-113">Accédez à «gérer le jeu de travail».</span><span class="sxs-lookup"><span data-stu-id="97d8a-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="97d8a-114">Cliquez sur «analyser».</span><span class="sxs-lookup"><span data-stu-id="97d8a-114">Click "Analyze".</span></span>

<span data-ttu-id="97d8a-115">Vous pouvez vérifier la progression de l'analyse dans l'onglet travaux de votre cas.</span><span class="sxs-lookup"><span data-stu-id="97d8a-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="97d8a-116">Une fois l'analyse terminée, vous pouvez afficher le rapport d'analyse, exécuter des requêtes dans votre jeu de travail sur les sorties de l'analyse (pour plus d'informations, consultez [la rubrique Query dans votre jeu de travail](working-set-search.md)) et afficher les documents connexes d'un document donné (pour plus d'informations, consultez la rubrique [ Examen des données dans le jeu de travail](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="97d8a-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="97d8a-117">Rapport d'analyse</span><span class="sxs-lookup"><span data-stu-id="97d8a-117">Analytics report</span></span>

<span data-ttu-id="97d8a-118">Pour afficher un rapport d'analyse pour votre jeu de travail:</span><span class="sxs-lookup"><span data-stu-id="97d8a-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="97d8a-119">Ouvrez votre jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="97d8a-119">Open your working set.</span></span>
2. <span data-ttu-id="97d8a-120">Accédez à «gérer le jeu de travail».</span><span class="sxs-lookup"><span data-stu-id="97d8a-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="97d8a-121">Cliquez sur «État».</span><span class="sxs-lookup"><span data-stu-id="97d8a-121">Click "Report".</span></span>

<span data-ttu-id="97d8a-122">L'État comprend quatre composants de l'analyse:</span><span class="sxs-lookup"><span data-stu-id="97d8a-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="97d8a-123">**Répartition** : le nombre de messages électroniques, de pièces jointes et de documents en vrac a été trouvé dans le jeu de travail.</span><span class="sxs-lookup"><span data-stu-id="97d8a-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="97d8a-124">**Documents (à l'exception des pièces jointes)** : le nombre de documents en vrac était des tableaux croisés dynamiques, des doublons uniques proches d'un tableau croisé dynamique ou un doublon exact d'un autre document.</span><span class="sxs-lookup"><span data-stu-id="97d8a-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="97d8a-125">**E-mails** : nombre de messages électroniques inclusifs, copies inclusives, déductions inclusives ou aucun des éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="97d8a-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="97d8a-126">**Pièces jointes** : nombre de pièces jointes uniques ou en double d'une pièce jointe différente dans la plage de travail.</span><span class="sxs-lookup"><span data-stu-id="97d8a-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>