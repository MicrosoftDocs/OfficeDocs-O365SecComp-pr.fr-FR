---
title: Comprendre les similitudes entre documents dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Examinez la valeur de similarité des documents, le niveau de ressemblance minimal entre deux fichiers devant être considérés comme étant des doublons, fonctionne dans Office 365 Advanced eDiscovery. '
ms.openlocfilehash: eb8f07ceedb10bd0152693dd1e82a28797d86a5a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220424"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a>Comprendre les similitudes entre documents dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Advanced eDiscovery, la similarité des documents est le niveau minimal de ressemblance nécessaire pour que deux documents soient considérés comme des doublons.
  
> [!TIP]
> Pour la plupart des applications d'entreprise, il est recommandé d'utiliser une valeur de similarité de 60%-75%. Pour une grande qualité de la reconnaissance optique des caractères (OCR), il est possible d'appliquer des valeurs inférieures. 
  
> [!NOTE]
> Après avoir été définie et exécutée pour un cas donné, la valeur de similarité ne peut pas être modifiée. 
  
Dans un jeu near-Duplicate (ND), il peut y avoir des documents avec un niveau de ressemblance sous le seuil de similarité. Pour qu'un document rejoigne un jeu de type ND, il doit y avoir au moins un document dans le paramètre ND avec un niveau de ressemblance dépassant la similarité. 
  
Par exemple, supposons que la similarité est définie sur 80%, le document F1 ressemble au document F2 à un niveau de 85% et le document F2 ressemble à un document F3 de 90%. 
  
Toutefois, le document F1 peut ressembler à un document de F3 dont le niveau est de seulement 70%, ce qui est inférieur au seuil. Néanmoins, dans cet exemple, les documents F1, F2 et F3 s'affichent dans la plage ND. De même, à l'aide d'une valeur de similarité de 80%, nous pouvons avoir créé deux jeux, EquiSet-1 et EquiSet-2. EquiSet-1 contient les documents E1 et E2. Equiset-2 contient les documents F1, F2 et F3. 
  
Les niveaux de ressemblance sont illustrés comme suit:
  
![Similitude du document](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
Supposons qu'un autre document, x1, est maintenant inséré. La ressemblance entre x1 et E3 est de 87%. De même, la ressemblance entre x1 et F1 est de 92%. Par conséquent, EquiSet-1, EquiSet-2 et x1 sont désormais combinés en un seul jeu ND.
  
![Similitude du document](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> Si deux documents sont affectés à un seul jeu, ils restent ensemble dans le même ensemble ND, même si des documents supplémentaires sont ajoutés à l'ensemble ou si les jeux sont fusionnés. 
  
Une fois les ensembles fusionnés, le document croisé dynamique peut changer lorsque de nouveaux documents sont ajoutés à un jeu. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Définition des options d'analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Définition d'un texte ignoré](set-ignore-text-in-advanced-ediscovery.md)
  
[Définition des paramètres avancés d'analyse](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Affichage des résultats de l'analyse](view-analyze-results-in-advanced-ediscovery.md)

