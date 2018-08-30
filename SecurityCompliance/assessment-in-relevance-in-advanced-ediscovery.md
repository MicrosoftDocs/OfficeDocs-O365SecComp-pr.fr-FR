---
title: Comprendre l’évaluation dans la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Obtenir une vue d’ensemble de la phase d’évaluation et de son rôle dans la détermination de la plus grande richesse des problèmes au cours de formation de la pertinence dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528112"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Comprendre l’évaluation dans la pertinence dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
EDiscovery avancé permet d’évaluation au plus tôt, par exemple, pour les problèmes définis et les données importées pour un cas. Découverte avancée permet l’expert pour prendre des décisions relatives à une approche à adopter et de les appliquer au projet de révision de document.
  
## <a name="understanding-assessment"></a>Évaluation de la présentation

Évaluation, l’expert examine un ensemble aléatoire de fichiers au moins 500, qui sont utilisées pour déterminer la plus grande richesse des problèmes et pour produire des statistiques qui reflètent les résultats de la formation. Évaluation réussit cas assez de fichiers pertinents pour atteindre un niveau statistique qui aide eDiscovery avancé pour fournir des statistiques exactes et déterminer efficacement la stabilisation point dans le processus de formation de pertinence. 
  
Plus que le nombre de pertinents fichiers dans le jeu d’évaluation, plus précis les statistiques et l’efficacité de l’algorithme de la stabilité. Le nombre de fichiers appropriées dans les fichiers d’évaluation dépend du problème. Plus grande richesse est le pourcentage estimé de fichiers appropriés dans le jeu de pertinent pour un problème. Problèmes avec une plus grande richesse atteindra un nombre de fichiers concernés plus rapidement que les problèmes avec la plus grande richesse inférieur. Problèmes avec la plus grande richesse très faible (par exemple, 2 % ou moins) nécessite une évaluation de très grande taille définie pour atteindre un nombre important de fichiers concernés.
  
Statistiques, qui sont présentées dans les onglets de suivi et de décider au cours de formation et après le calcul de lot, incluent les estimations de rappel pour passer en revue les différents ensembles. Statistiques, estimations sont basées sur un échantillon définir (dans ce cas, les fichiers d’évaluation) incluent la marge d’erreur et le niveau de confiance de cette marge d’erreur. Par exemple, rappel estimée à 80 % peut-être une marge d’erreur de plus ou moins de 5 % avec un niveau de confiance de 95 %. Cela signifie que le rappel estimé est réellement 75-85 % et cette estimation a 95 % de confiance. Plus le jeu d’évaluation, la marge d’erreur devient plus petite et les statistiques sont plus précis. 
  
Une fois l’expert examine un ensemble d’évaluation initiale de 500 fichiers, la pertinence est en mesure de déterminer la marge d’erreur des valeurs de rappel en cours. La pertinence définit également une marge par défaut d’erreur indiquant qu’il est recommandé d’atteindre pour optimiser l’ensemble de l’évaluation. Voici quelques exemples :
  
- Si l’évaluation déjà définie a engendré une marge d’erreur de plus ou moins 10 %, la pertinence recommande à passer à la formation (aucune évaluation supplémentaire n’est nécessaire). 
    
- Si le jeu d’évaluation a engendré une marge d’erreur de plus ou moins 13 %, la pertinence peut vous recommandons de la révision d’un autre ensemble de fichiers d’évaluation pour atteindre une marge inférieure. 
    
- Si plus grande richesse est très faible, la pertinence est recommandé d’arrêt évaluation même si la marge d’erreur est importante (sans statistiques difficile), car l’ensemble de l’évaluation nécessaire atteindre une marge d’erreur utile est trop importante.
    
Chaque problème a son propre richesse, la marge actuelle d’erreur et par conséquent, une estimation du nombre de fichiers d’évaluation supplémentaires. L’ensemble suivant d’évaluation est créée en fonction du nombre maximal de fichiers (jusqu'à 1 000 dans un jeu unique).
  
Vous pouvez accepter les recommandations de la pertinence ou la marge d’erreur actuelle en fonction de vos besoins. La marge actuelle par défaut d’erreur est déterminée pour le rappel à égale ou supérieure à 75 %.
  
> [!NOTE]
> La phase d’évaluation peut être ignorée, dans le **la pertinence \> suivi** onglet dans l’affichage pour un problème, en désactivant la case à cocher **évaluation** par le problème, puis pour « tous les problèmes ». Toutefois, par conséquent, il n’y aura aucuns statistiques pour ce problème. > Si vous décochez la case à cocher **évaluation** uniquement peut être effectuée avant l’évaluation est effectuée. Il existe plusieurs problèmes dans un cas, évaluation est contournée uniquement si la case à cocher est désactivée pour chaque problème 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

