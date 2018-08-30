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
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Comprendre la similarité de document dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans découverte avancée, Document similarité est le niveau minimal de ressemblance requis pour les deux documents considérés comme près de doublons.
  
> [!TIP]
> Pour la plupart des applications d’entreprise, il est recommandé d’utiliser une valeur de similarité de 60 à 75 %. Pour les documents de reconnaissance optique de caractères (OCR) de qualité médiocre, les valeurs inférieures similarité peuvent être appliqués. 
  
> [!NOTE]
> Une fois qu’il a défini et s’exécuter pour une situation donnée, la valeur de similarité ne peut pas être modifiée. 
  
Un ensemble Near en double (e), peuvent être des documents avec un niveau de ressemblance avec inférieur au seuil de similarité. Pour un document à participer à un jeu ND, le ND définie avec un niveau de ressemblance dépassant la similarité doit être au moins un document. 
  
Par exemple, supposons la similarité est définie sur 80 %, document F1 ressemble au document F2 à un niveau de 85 % et document F2 ressemble au document F3 à un niveau de 90 %. 
  
Toutefois, les documents F1 peut ressembler à document F3 à un niveau uniquement 70 %, est inférieur au seuil. Néanmoins, dans cet exemple, les documents F1, F2 et F3 apparaissent toutes dans l’une ND valeur. De même, à l’aide d’une valeur de similarité de 80 %, nous pouvons créer deux jeux, EquiSet-1 et 2-EquiSet. EquiSet-1 contient des documents E1 et E2. Equiset-2 contient les documents F1, F2 et F3. 
  
Les niveaux de ressemblance avec sont illustrées comme suit :
  
![Similitude du document](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Supposons qu’un autre document, X1, est inséré. La ressemblance entre X1 et E3 est 87 %. De même, la ressemblance entre X1 et F1 est 92 %. Par conséquent, EquiSet -1, EquiSet -2 et X1 sont maintenant combinées en un seul ND défini.
  
![Similitude du document](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Si les deux documents sont affectés à un seul ensemble ND, ils restent ensemble dans le même ensemble ND, documents même si supplémentaires sont ajoutés à l’ensemble ou si les jeux sont fusionnés. 
  
Une fois ensembles sont fusionnées, le document dynamique peut modifier lorsque de nouveaux documents sont ajoutés à un ensemble. 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Définition des options d’analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Ignorer le texte du paramètre](set-ignore-text-in-advanced-ediscovery.md)
  
[Analyse de la configuration des paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Affichage des résultats d’analyse](view-analyze-results-in-advanced-ediscovery.md)

