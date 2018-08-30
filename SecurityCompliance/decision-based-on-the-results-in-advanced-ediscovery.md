---
title: En se basant sur les résultats dans Office 365 avancée de découverte électronique
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Découvrez comment l’onglet décider d’eDiscovery avancée de Office 365 fournit les données qui peuvent vous aider à déterminent la taille adéquate de l’ensemble de la révision de dossiers. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527817"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a>En se basant sur les résultats dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
 Dans découverte avancée, l’onglet Decide fournit des informations supplémentaires pour l’affichage et utilisation des statistiques d’aide à la décision pour déterminer la taille de l’ensemble de la révision de dossiers. 
  
## <a name="using-the-decide-tab"></a>À l’aide de l’onglet décider

![Décision de pertinence](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
Cet onglet comprend les éléments suivants :
  
- **Problème**: à partir de là, vous pouvez sélectionner le problème d’intérêt dans la liste. 
    
- **Rapport de rappel de la révision**: comparaison des avancées de révision eDiscovery en fonction des résultats de la pertinence. Le point de limite dans le graphique représente le pourcentage de fichiers pour passer en revue, mappé à un score de pertinence. Il est utilisé dans la phase de Test de la pertinence et en tant qu’un seuil d’exportation pour élimination. Le point de coupure par défaut, le nombre de fichiers pour passer en revue est au niveau du point dans lequel l’équilibre entre la précision et de rappel est optimal. Le point de coupure réel doit être déterminé par l’utilisateur en fonction des objectifs et les compromis de coût (révision %) et les risques (rappel %). À l’aide du curseur, vous pouvez régler le point de coupure et l’impact sur le graphique et les paramètres, consultez la rubrique lorsque vous ajustez le pourcentage de fichiers appropriés doivent être récupérées et avant de valider une décision.
    
- **Paramètres**: passez en revue, rappelez-vous, paramètres pertinents et Total coût suivante sont les statistiques calculées cumulatives se rapporte à la révision par rapport à la collection pour le cas de toute. Définitions de ces paramètres sont les suivantes :
    
    **Passez en revue**: pourcentage de fichiers pour passer en revue en fonction de cette limite. 
    
    **Rappeler**: pourcentage de fichiers appropriés dans le jeu de révision. 
    
    **Suivant pertinents**: coût d’examiner et d’identifier un fichier pertinent supplémentaire qui n’est pas actuellement à la révision défini. 
    
    **Coût total**: coût pour l’examen de ce pourcentage des fichiers de dossiers. Paramètres coût peuvent être définis par le Gestionnaire d’incident.
    
- **Distribution par score de pertinence**: fichiers dans l’affichage gris foncé vers la gauche sont sous le score de coupure. Une info-bulle affiche le score de pertinence et le pourcentage de fichiers associé dans le fichier de révision défini en fonction du nombre total de fichiers.
    
Le volet de détails étendu affiche des détails supplémentaires. Fichiers dans les illustrations de la collection n’incluent pas de fichiers vides ou confus. Illustrations de fichiers famille représentent les fichiers qui ne sont pas chargés dans la pertinence encore prise en compte dans le cadre de la famille.
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Effectue la formation de pertinence](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

