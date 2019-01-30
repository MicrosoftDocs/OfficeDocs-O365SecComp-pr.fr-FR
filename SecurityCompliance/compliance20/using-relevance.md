---
title: À l’aide du module de pertinence pour analyser des données d’eDiscovery avancée (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5e30a7f6919f50d2d73606fae3b53f21ef33e223
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607657"
---
# <a name="using-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a>À l’aide du module de pertinence pour analyser des données d’eDiscovery avancée (Preview)

Dans découverte avancée (Preview), le module de la pertinence inclut la formation de la pertinence et la vérification des fichiers associés à un cas. Le flux de travail de pertinence est affichée et décrite comme suit :
  
![Flux de travail de pertinence](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Cycles d’évaluation et de suivi**:
    
  - **Évaluation**: permet au plus tôt évaluation basée sur un échantillon aléatoire des fichiers et utilise cette évaluation pour appliquer les décisions pour déterminer les performances du processus de codage prédictif. 
    
  - **Suivi**: calculer et afficher les résultats intermédiaires de l’évaluation lors de l’analyse statistique validité du processus. 
    
- **Cycles de formation et de suivi**
    
  - **Balise**: eDiscovery avancée (Preview) prend connaissance des critères de pertinence spécifiques à chaque problème basée sur l’expert itératif et liaison de fichiers individuels.
    
  - **Suivi**: calculer et afficher les résultats intermédiaires de la formation de pertinence lors de l’analyse statistique validité du processus. 
    
- **Calcul de lot**: le critère de pertinence cumulé et appris est appliqué à la collection de l’intégralité du fichier et un score de pertinence est généré pour chaque fichier.
    
- **Décider**: les résultats de l’analyse appliquée au cas entière s’affiche après le calcul de lot, et permet de prendre des décisions de passer en revue les documents sont affichés.
    
- **Test**: résultats peuvent être testées pour vérifier la validité et l’efficacité du traitement eDiscovery avancées (Preview).

- **Recherche**: une fois que le flux de travail de pertinence est terminée, vous pouvez utiliser la sortie de centile de lecture d’un document pour votre problème lorsque vous exécutez une requête au sein de votre jeu de travail.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Recommandations pour la formation de la pertinence et passer en revue les

Voici une vue d’ensemble d’instructions pour la formation de la pertinence et passer en revue les :
  
- **Erreurs et les incohérences**: si des erreurs de liaison sont effectuées au cours de formation, revenir aux exemples de fichier précédente pour y remédier. S’il y trop grand nombre d’erreurs à corriger ou il existe un nouveau point de vue de l’incident ou un problème, les critères de la pertinence doivent être redéfinis par l’administrateur et redémarré la formation de pertinence.
    
- **Balisage et formation**: 
    
  - Les fichiers doivent être référencées en fonction du contenu uniquement. Ne pas tenir compte des métadonnées, telles que les dépositaires, la date ou chemin d’accès du fichier. 
    
  - Considérez date indications plage du texte pour marquer les fichiers.
    
  - Considérez les images graphiques incorporés pour marquer les fichiers.
     
  - Ignorer la texte appliqué à la pertinence sera supprimé dans le contenu du fichier affiché dans l’affichage de texte dans la pertinence. Si les valeurs de texte de la case à cocher Ignorer ont été définies après la pertinence de la formation déjà démarré, le nouveau texte ignoré sera appliqué à des exemples de fichiers créés à partir du point dans lequel il a été défini. La fonctionnalité d’ignorer le texte doit être utilisée avec précaution, comme son utilisation peut réduire les performances de l’analyse des fichiers
    
  - Utilisez l’option **Ignorer le balisage** uniquement lorsque cela est nécessaire. EDiscovery avancée (Preview) ne pas former basé sur les fichiers ignorés. Évaluation, s’il est difficile de déterminer si un fichier est pertinent, il est préférable de balise en tant que Relevant (R) ou non pertinent (NR) chaque fois que possible au lieu de sélectionner **Ignorer**. Lors de la découverte avancée (Preview) évalue la formation, il sera visible bien ces types de fichiers ont été traités.
    
  - Même avec une petite quantité de texte extrait les fichiers doit être référencées en formation R/NR, plutôt que « Ignorer », lorsque cela est possible. 
    
  - Marquage peut avoir un impact sur le classifieur tant que le fichier est accessible en lecture et peut être marqué comme R/NR.
    
  - Le numéro de séquence de fichier dans la liste de fichiers exemple affichée sous l’onglet **balise** permet à l’utilisateur revenir à la commande affichée d’origine des fichiers. 
    
  - Vous pouvez revenir en arrière à n’importe quel échantillon et modifier le balisage de l’évaluation et de formation définie des fichiers. Les modifications seront appliquées lors de la création de l’exemple suivant.
    
  - Excel analysé les fichiers au format PDF doivent être traitées comme des fichiers Excel natifs pour marquer les fichiers.
    
  - En cas de doute concernant le balisage de la pertinence d’un fichier, contactez un expert. Liaison incorrecte au cours de la formation de pertinence peut entraîner la perte de temps plus loin dans le processus et peut également avoir un impact négatif sur la qualité globales des résultats de la.
    
  - Mots clés qui ont été définis dans le mot clé listes seront affichera dans les couleurs pour aider l’utilisateur à identifier les fichiers appropriés lors de la liaison.
    
- **Calcul du lot**: les fichiers qui ont été marquées comme R/NR par l’expert reçoit un score de 0 ou 100. Cela s’applique au balisage avant le calcul de lot. Si l’expert basculer le problème inactif après le calcul du lot et suite marquage ce problème, les notes nouvellement balisés ne sera pas 100/0, mais plutôt le score d’origine.
    
- **Problèmes et échantillonnage mode**: problèmes sont généralement désactivées lors de leur travail est terminé (la stabilisation de formation de la pertinence et calcul de lot a été effectuée), lorsque les problèmes sont annulées, ou lorsqu’un autre utilisateur travaille sur les problèmes.
    
## <a name="steps-in-relevance-training"></a>Étapes de la formation de pertinence

Dans la **la pertinence \> suivi** onglet, eDiscovery avancée fournit des recommandations sur la façon de procéder de la transformation, avec les étapes suivantes. Les implications sont décrits ci-dessous lors de chacune des étapes suivantes est recommandé dans le processus de formation de pertinence. 
  
- Marquer / continuer balisage : passer en revue les fichiers et la pertinence de la liaison effectuée par un expert pour chaque fichier et émettre au sein d’un échantillon.
    
  - Implication : Un exemple existant doit être marqué.
    
- Évaluation / continuer d’évaluation : permet de validation au plus tôt de la pertinence des cas de problème et un aperçu de la pertinence de la population fichier importée pour le dossier actif.
    
  - Implication : Plus d’évaluation est requis ou recommandée.
    
- Formation / continuer de formation : processus pendant les options avancées eDiscovery étudient l’expert qui est marquer les fichiers exemples et acquiert la possibilité d’identifier les critères de la pertinence pertinentes pour chaque problème dans le contexte de chaque cas.
    
  - Implication : Le problème a besoin de plus de formations ; l’exemple suivant doit être créé et avec balise. 
    
- Calcul du lot : processus de pertinence dans les paramètres avancés eDiscovery prend les connaissances acquises au cours de la phase de formation et s’applique à la population entière de fichier. Tous les fichiers dans le groupe de fichiers pertinentes sont évalués pour la pertinence et reçoivent un score de pertinence.
    
  - Implication : Le problème a stabilisation et calcul de lot peut être effectuée.
    
- Rattrapage : Pertinence indique quand un expert passe en revue et balises d’un échantillon de fichiers sélectionnés à partir d’une charge de fichiers supplémentaires pendant un scénario de déploiement charge.
    
  - Implication : Un nouveau chargement a été ajouté et rattrapage est nécessaire pour continuer à travailler.
    
- Ajouter une balise à des incohérences : processus identifie via un algorithme de découverte électronique avancées, des incohérences dans le fichier de balisage processus ayant un impact négatif sur l’analyse.
    
  - Implication : L’exemple suivant inclut les fichiers qui ont été marquées dans les exemples précédents, et leur marquage doit être rétablie.
    
- Mettre à jour de classifieur : permet à l’utilisateur à appliquer le marquage ou de l’amorçage des modifications.
    
  - Implication : Liaison et l’amorçage des modifications peuvent être appliquées sans avoir à exécuter manuellement un autre exemple de la pertinence.
    
- En attente : la pertinence de la formation processus est terminée.
    
  - Implication : Aucune formation de pertinence n’est requise à ce stade.
    
Bien qu’eDiscovery avancée vous guide à travers le processus, avec recommandé de suivre les étapes ci-après à différents stades, il vous permet également de naviguer entre les onglets et les pages et faites des choix de répondre à des situations qui peuvent être pertinentes à votre cas, le problème, ou processus de révision de documents. 
  
Il est possible d’accepter ou de remplacer l’étape suivante eDiscovery avancées choix de traitement. Si vous souhaitez effectuer une étape de l’étape suivante recommandée, cliquez sur l' **étape suivante** répertoriées dans l’affichage de l’étendue de problème dans la boîte de dialogue et cliquez sur le bouton **Modifier** en regard de l’étape suivante, sélectionnez une autre option étape suivante. 
  
> [!NOTE]
> Certaines options peuvent rester désactivées après déverrouillage comme ils ne sont pas pris en charge pour une utilisation à ce stade du processus. 
  
## <a name="more-information"></a>Plus d’informations

[Évaluation de la présentation de la pertinence](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](../test-relevance-analysis-in-advanced-ediscovery.md)

[Effectuer des requêtes dans le jeu de travail](working-set-search.md)
