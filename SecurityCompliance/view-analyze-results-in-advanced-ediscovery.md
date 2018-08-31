---
title: Afficher les résultats d’analyse dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Comprendre où afficher les résultats du processus d’analyse dans Office 365 avancée eDiscovery, y compris les définitions des options de la tâche affichée.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528488"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d73ad-103">Afficher les résultats d’analyse dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="d73ad-103">View Analyze results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="d73ad-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d73ad-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="d73ad-106">Dans découverte avancée, progression et les résultats pour le processus d’analyse peuvent être affichés dans une variété d’affiche comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d73ad-106">In Advanced eDiscovery, progress and results for the Analyze process can be viewed in a variety of displays as described below.</span></span>
  
## <a name="view-analyze-task-status"></a><span data-ttu-id="d73ad-107">Afficher l’état de tâche d’analyse</span><span class="sxs-lookup"><span data-stu-id="d73ad-107">View Analyze task status</span></span>

<span data-ttu-id="d73ad-108">Dans **Prepare \> analyse \> résultats \> état de la tâche**, l’état est affiché pendant et après l’exécution de processus d’analyse.</span><span class="sxs-lookup"><span data-stu-id="d73ad-108">In **Prepare \> Analyze \> Results \> Task status**, the status is displayed during and after Analyze process execution.</span></span> 
  
![Analyser l’état des tâches](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
<span data-ttu-id="d73ad-110">Les tâches affichées peuvent varier selon les options sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="d73ad-110">The tasks displayed may vary depending on the options selected.</span></span> 
  
- <span data-ttu-id="d73ad-111">**ND/ET : le programme d’installation**: prépare pour l’exécution, par exemple, définit les paramètres d’exécution et cas.</span><span class="sxs-lookup"><span data-stu-id="d73ad-111">**ND/ET: setup**: Prepares for the run, for example, sets run and case parameters.</span></span>
    
- <span data-ttu-id="d73ad-112">**ND/ET : calcul ND**: l’analyse des processus près de copie des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d73ad-112">**ND/ET: ND calculation**: Processes Near-duplicate analysis of files.</span></span>
    
- <span data-ttu-id="d73ad-113">**ND/ET : calcul ET**: analyse des effectue un Thread de messagerie sur l’ensemble de messagerie entière.</span><span class="sxs-lookup"><span data-stu-id="d73ad-113">**ND/ET: ET calculation**: Performs Email Thread analysis on the entire email set.</span></span>
    
- <span data-ttu-id="d73ad-114">**ND/ET : tableaux croisés dynamiques et similitudes**: effectue le tableau croisé dynamique et traitement des fichiers similarité.</span><span class="sxs-lookup"><span data-stu-id="d73ad-114">**ND/ET: pivots and similarities**: Performs pivot and file similarity processing.</span></span>
    
- <span data-ttu-id="d73ad-115">**ND/ET : mise à jour des métadonnées**: finalise les nouvelles données recueillies sur les fichiers dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d73ad-115">**ND/ET: metadata update**: Finalizes the new data collected on the files in the database.</span></span>
    
- <span data-ttu-id="d73ad-p102">**Thèmes : calcul des thèmes**: exécute l’analyse des thèmes. (Affiché uniquement si sélectionné).</span><span class="sxs-lookup"><span data-stu-id="d73ad-p102">**Themes: themes calculation**: Runs themes analysis. (Displayed only if selected.)</span></span>
    
- <span data-ttu-id="d73ad-p103">**État de la tâche**: cette ligne est affichée après la fin d’une tâche. Lors de l’exécutant des tâches, la durée d’exécution s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p103">**Task status**: This line is displayed after task completion. While tasks are running, run duration is displayed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d73ad-p104">Les résultats d’analyse de proximité des doublons et les Threads de courrier électronique (ND et ED) s’applique au nombre de documents à traiter. Il n’inclut pas les fichiers en double exactes.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p104">The Analyze results of Near-duplicates and Email Threads (ND and ED) applies to the number of documents to be processed. It does not include Exact duplicate files.</span></span> 
  
## <a name="view-near-duplicates-and-email-threads-status"></a><span data-ttu-id="d73ad-122">Afficher l’état près de doublons et les Threads de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="d73ad-122">View Near-duplicates and Email Threads status</span></span>

<span data-ttu-id="d73ad-123">Les résultats de la population **cible** affichent le nombre de documents, messages électroniques, pièces jointes et les erreurs dans la population cible.</span><span class="sxs-lookup"><span data-stu-id="d73ad-123">The **Target** population results display the number of documents, emails, attachments, and errors in the target population.</span></span> 
  
<span data-ttu-id="d73ad-124">Les résultats de **Documents** affichent le nombre de tableaux croisés dynamiques, près de doublons uniques et les fichiers en double exactes.</span><span class="sxs-lookup"><span data-stu-id="d73ad-124">The **Documents** results display the number of pivots, unique near-duplicates, and exact duplicate files.</span></span> 
  
<span data-ttu-id="d73ad-p105">Les **messages électroniques** de résultats affichent le nombre d’inclus et inclusif moins uniques copies (inclus) et le reste des messages électroniques. Les différents types de résultats de la messagerie sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d73ad-p105">The **Emails** results display the number of inclusive, inclusive minus, unique inclusive copies, and the rest of the email messages. The different types of email results are:</span></span> 
  
- <span data-ttu-id="d73ad-p106">**Comprises**: un message électronique (inclus) est le nœud de fin dans un thread de messagerie et contient tous les l’historique de ce thread. Par conséquent, le réviseur peut se concentrer en toute sécurité sur le courrier électronique (inclus), sans avoir besoin de lire les messages précédents dans le thread.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p106">**Inclusive**: An inclusive email is the terminating node in an email thread and contains all the previous history of that thread. As a result, the reviewer can safely focus on the inclusive email, without the need to read the previous messages in the thread.</span></span> 
    
- <span data-ttu-id="d73ad-p107">**Comprises moins**: un message électronique inclus est désigné comme moins inclus s’il y a au moins une autre les pièces jointes associées parents du message (inclus). Dans ce contexte, le terme que parent est utilisé pour les messages vers le haut situés sur le thread de messagerie ou des conversations inclus dans l’e-mail spécifique (inclus). Un réviseur peut utiliser le moins indication comme un signal que bien qu’il ne soit pas nécessaire consulter le contenu des parents messagerie inclus, il peut être utile de consulter les pièces jointes associées les parents du chemin d’accès inclus inclus.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p107">**Inclusive minus**: An inclusive email is designated as inclusive minus if there are one or more different attachments associated with the parents of the inclusive message. In this context, the term Parent is used for messages located upwards on the email thread or conversations included in that specific inclusive email. A reviewer can use the inclusive minus indication as a signal that although it might not be necessary to review the content of the inclusive email parents, it may be useful to review the attachments associated with the inclusive path parents.</span></span> 
    
- <span data-ttu-id="d73ad-p108">**Copie (inclus)**: un message électronique (inclus) est désigné comme copie inclus s’il s’agit de la copie d’un autre message marqué comme inclus ou inclus moins. En d’autres termes, ce message a le même objet et corps en tant qu’un autre message inclus et, en tant que telles, CO-réside dans le même nœud. Inclus copier des messages contenant le même contenu, ils peuvent généralement être ignorés dans le processus de révision.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p108">**Inclusive copy**: An inclusive email is designated as inclusive copy if it's the copy of another message marked as inclusive or inclusive minus. In other words, this message has the same subject and body as another inclusive message and, as such, co-resides in the same node. Because inclusive copy messages contain the same content, they can usually be skipped in the review process.</span></span> 
    
- <span data-ttu-id="d73ad-p109">**Le reste**: cela indique le courrier électronique qui ne contient pas de contenu unique et par conséquent, ne peuvent être classées dans une des trois catégories précédentes. Ces messages électroniques n’avez pas besoin être révisé. Si un message contient une pièce jointe qui ne figure pas dans un message électronique inclus ultérieurement, la pièce jointe devront être révisé. Cela est indiqué par l’existence d’un inclus moins de messagerie dans le thread.</span><span class="sxs-lookup"><span data-stu-id="d73ad-p109">**The rest**: This indicates email that doesn't contain any unique content, and therefore doesn't fall into any of the previous three categories. These email messages don't need to be reviewed. If a message contains an attachment that isn't on a later inclusive email, then the attachment might need to be reviewed. This is indicated by the existence of an inclusive minus email within the thread.</span></span>
    
<span data-ttu-id="d73ad-139">Les résultats de **pièces jointes** affichent le nombre de pièces jointes, en fonction de ce type de manière unique et les doublons.</span><span class="sxs-lookup"><span data-stu-id="d73ad-139">The **Attachments** results display the number of attachments, according to such type as unique and duplicates.</span></span> 
  
![Doublons à proximité et Threads de messagerie](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a><span data-ttu-id="d73ad-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d73ad-141">See also</span></span>

[<span data-ttu-id="d73ad-142">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="d73ad-142">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d73ad-143">Présentation de similarité de document</span><span class="sxs-lookup"><span data-stu-id="d73ad-143">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d73ad-144">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="d73ad-144">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d73ad-145">Ignorer le texte du paramètre</span><span class="sxs-lookup"><span data-stu-id="d73ad-145">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d73ad-146">Analyse de la configuration des paramètres avancés</span><span class="sxs-lookup"><span data-stu-id="d73ad-146">Setting Analyze advanced settings</span></span>](view-analyze-results-in-advanced-ediscovery.md)

