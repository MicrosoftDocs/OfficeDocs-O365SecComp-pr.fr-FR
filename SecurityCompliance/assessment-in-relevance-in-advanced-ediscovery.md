---
title: Comprendre l’Évaluation dans le module Pertinence dans Office 365 Advanced eDiscovery
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
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Obtenez une vue d'ensemble de la phase d'évaluation et de son rôle dans la détermination de la richesse des problèmes lors de la formation à la pertinence dans Office 365 Advanced eDiscovery.
ms.openlocfilehash: 1ddaa7ef37f762d7b63bb6c0c51193ff382b8d6b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212974"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Comprendre l’Évaluation dans le module Pertinence dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Advanced eDiscovery permet une évaluation anticipée, par exemple, pour les problèmes définis et les données importées pour un cas. Advanced eDiscovery permet à l'expert de prendre des décisions concernant une approche adoptée et de l'appliquer au projet de révision de document.
  
## <a name="understanding-assessment"></a>Présentation de l'évaluation

Dans l'évaluation, l'expert examine un ensemble aléatoire d'au moins 500 fichiers, qui permettent de déterminer la richesse des problèmes et de produire des statistiques reflétant les résultats de la formation. L'évaluation réussit lorsqu'un nombre suffisant de fichiers pertinents est trouvé pour atteindre un niveau statistique qui aidera à améliorer la pertinence eDiscovery afin de fournir des statistiques précises et de déterminer efficacement le point de stabilisation dans le processus de formation. 
  
Plus le nombre de fichiers appropriés est élevé dans l'ensemble d'évaluation, plus les statistiques et l'efficacité de l'algorithme de stabilité sont précises. Le nombre de fichiers appropriés dans les fichiers d'évaluation dépend de la richesse du problème. Richesse est le pourcentage estimé de fichiers pertinents dans le jeu correspondant à un problème. Les problèmes avec une richesse plus élevée atteindront un nombre plus élevé de fichiers pertinents plus rapidement que les problèmes avec une richesse plus faible. Les problèmes avec une richesse extrêmement faible (par exemple, 2% ou moins) nécessitent un ensemble d'évaluation très important pour atteindre un nombre significatif de fichiers pertinents.
  
Les statistiques, présentées dans les onglets suivi et décision lors de la formation et après le calcul par lots, incluent les estimations de rappel pour différents ensembles de révision. Dans statistiques, les estimations basées sur un échantillon défini (dans ce cas, les fichiers d'évaluation) incluent la marge d'erreur et le niveau de confiance de cette marge d'erreur. Par exemple, le rappel estimé de 80% peut avoir une marge d'erreur de plus ou moins 5% avec un niveau de confiance de 95%. Cela signifie que le rappel estimé est en fait de 75% 85% et que cette estimation a une confiance de 95%. Plus l'ensemble d'évaluation est grand, plus la marge d'erreur est faible et plus les statistiques sont précises. 
  
Une fois que l'expert a examiné un ensemble d'évaluation initiale de 500 fichiers, la pertinence est en mesure de déterminer la marge d'erreur actuelle des valeurs de rappel. La pertinence définit également une marge d'erreur par défaut qu'elle recommande d'atteindre pour optimiser l'ensemble d'évaluation. Voici quelques exemples:
  
- Si l'ensemble d'évaluation a déjà généré une marge d'erreur de plus ou moins 10%, la pertinence recommande de passer à la formation (aucune révision d'évaluation supplémentaire n'est nécessaire). 
    
- Si l'ensemble d'évaluation a généré une marge d'erreur de plus ou moins 13%, la pertinence peut recommander la révision d'un autre ensemble de fichiers d'évaluation pour atteindre une marge plus petite. 
    
- Si la richesse est extrêmement faible, la pertinence peut recommander d'arrêter l'évaluation même si la marge d'erreur est importante (rendant les statistiques incommodes), car l'ensemble d'évaluation nécessaire pour atteindre une marge d'erreur utile est trop important.
    
Chaque problème a sa propre richesse, sa marge d'erreur actuelle et, par conséquent, le nombre estimé de fichiers d'évaluation supplémentaires. Le prochain ensemble d'évaluation est créé en fonction du nombre maximal de fichiers (jusqu'à 1 000 dans un seul ensemble).
  
Vous pouvez accepter les recommandations de pertinence ou ajuster la marge actuelle d'erreur en fonction de vos besoins. La marge d'erreur actuelle par défaut est déterminée pour rappel à une valeur égale ou supérieure à 75%.
  
> [!NOTE]
> La phase d'évaluation peut être ignorée, sous l'onglet de **suivi de pertinence \> ** de l'affichage développé d'un problème, en désactivant la case à cocher **évaluation** par problème, puis «tous les problèmes». Toutefois, il n'y aura pas de statistiques pour ce problème. > la désActivation de la case à cocher **évaluation** ne peut être effectuée qu'avant l'évaluation. Dans le cas où plusieurs problèmes existent, l'évaluation est ignorée uniquement si la case à cocher est désactivée pour chaque problème. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Balisage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Étiquetage et formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l'analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

