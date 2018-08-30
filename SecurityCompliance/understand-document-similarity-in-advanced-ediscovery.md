---
title: Comprendre la similarité de document dans Office 365 avancée de découverte électronique
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Passez en revue le document similarité valeur, le niveau minimal de ressemblance pour les deux fichiers à prendre en considération près de doublons, fonctionne dans Office 365 avancée de découverte électronique. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527932"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a><span data-ttu-id="f6b01-103">Comprendre la similarité de document dans Office 365 avancée de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="f6b01-103">Understand document similarity in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="f6b01-p101">Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f6b01-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="f6b01-106">Dans découverte avancée, Document similarité est le niveau minimal de ressemblance requis pour les deux documents considérés comme près de doublons.</span><span class="sxs-lookup"><span data-stu-id="f6b01-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="f6b01-p102">Pour la plupart des applications d’entreprise, il est recommandé d’utiliser une valeur de similarité de 60 à 75 %. Pour les documents de reconnaissance optique de caractères (OCR) de qualité médiocre, les valeurs inférieures similarité peuvent être appliqués.</span><span class="sxs-lookup"><span data-stu-id="f6b01-p102">For most business applications, it is recommended to use a Similarity value of 60%-75%. For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f6b01-109">Une fois qu’il a défini et s’exécuter pour une situation donnée, la valeur de similarité ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="f6b01-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="f6b01-p103">Un ensemble Near en double (e), peuvent être des documents avec un niveau de ressemblance avec inférieur au seuil de similarité. Pour un document à participer à un jeu ND, le ND définie avec un niveau de ressemblance dépassant la similarité doit être au moins un document.</span><span class="sxs-lookup"><span data-stu-id="f6b01-p103">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold. For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="f6b01-112">Par exemple, supposons la similarité est définie sur 80 %, document F1 ressemble au document F2 à un niveau de 85 % et document F2 ressemble au document F3 à un niveau de 90 %.</span><span class="sxs-lookup"><span data-stu-id="f6b01-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="f6b01-p104">Toutefois, les documents F1 peut ressembler à document F3 à un niveau uniquement 70 %, est inférieur au seuil. Néanmoins, dans cet exemple, les documents F1, F2 et F3 apparaissent toutes dans l’une ND valeur. De même, à l’aide d’une valeur de similarité de 80 %, nous pouvons créer deux jeux, EquiSet-1 et 2-EquiSet. EquiSet-1 contient des documents E1 et E2. Equiset-2 contient les documents F1, F2 et F3.</span><span class="sxs-lookup"><span data-stu-id="f6b01-p104">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold. Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set. Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2. EquiSet-1 contains documents E1 and E2. Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="f6b01-118">Les niveaux de ressemblance avec sont illustrées comme suit :</span><span class="sxs-lookup"><span data-stu-id="f6b01-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Similitude du document](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="f6b01-p105">Supposons qu’un autre document, X1, est inséré. La ressemblance entre X1 et E3 est 87 %. De même, la ressemblance entre X1 et F1 est 92 %. Par conséquent, EquiSet -1, EquiSet -2 et X1 sont maintenant combinées en un seul ND défini.</span><span class="sxs-lookup"><span data-stu-id="f6b01-p105">Assume that another document, X1, is now inserted. The resemblance between X1 and E3 is 87%. Similarly, the resemblance between X1 and F1 is 92%. As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Similitude du document](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="f6b01-125">Si les deux documents sont affectés à un seul ensemble ND, ils restent ensemble dans le même ensemble ND, documents même si supplémentaires sont ajoutés à l’ensemble ou si les jeux sont fusionnés.</span><span class="sxs-lookup"><span data-stu-id="f6b01-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="f6b01-126">Une fois ensembles sont fusionnées, le document dynamique peut modifier lorsque de nouveaux documents sont ajoutés à un ensemble.</span><span class="sxs-lookup"><span data-stu-id="f6b01-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6b01-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6b01-127">See also</span></span>

[<span data-ttu-id="f6b01-128">eDiscovery avancée Office 365</span><span class="sxs-lookup"><span data-stu-id="f6b01-128">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f6b01-129">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="f6b01-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f6b01-130">Ignorer le texte du paramètre</span><span class="sxs-lookup"><span data-stu-id="f6b01-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f6b01-131">Analyse de la configuration des paramètres avancés</span><span class="sxs-lookup"><span data-stu-id="f6b01-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f6b01-132">Affichage des résultats d’analyse</span><span class="sxs-lookup"><span data-stu-id="f6b01-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

