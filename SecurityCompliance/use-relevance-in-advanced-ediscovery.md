---
title: Utilisez le module de la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Découvrez le module de la pertinence dans Office 365 avancée eDiscovery, y compris un flux de travail et les instructions et les étapes pour passer en revue les fichiers et de formation.  '
ms.openlocfilehash: 2cf75ef95291c5393367ce01fb0cd660f9b99145
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527863"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a>Utilisez le module de la pertinence dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans découverte avancée, le module de la pertinence inclut la formation de la pertinence et la vérification des fichiers associés à un cas. Le flux de travail de pertinence est affichée et décrite comme suit :
  
![Flux de travail de pertinence](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Cycles d’évaluation et de suivi**:
    
  - **Évaluation**: découverte avancée permet au plus tôt évaluation basée sur un échantillon aléatoire des fichiers et utilise cette évaluation pour appliquer les décisions pour déterminer les performances du processus de codage prédictif. 
    
  - **Suivi**: eDiscovery avancée calcule et affiche les résultats intermédiaires de l’évaluation lors de l’analyse statistique validité du processus. 
    
- **Cycles de formation et de suivi**:
    
  - **Balise**: découverte avancée prend connaissance des critères de pertinence spécifiques à chaque problème basée sur l’expert itératif et liaison de fichiers individuels.
    
  - **Suivi**: eDiscovery avancée calcule et affiche les résultats intermédiaires de la formation de pertinence lors de l’analyse statistique validité du processus. 
    
- **Calcul du lot**: découverte avancée prend les critères de la pertinence cumulés et enregistrés, s’applique à la collection de l’intégralité du fichier et génère des résultats de la pertinence pour chaque fichier.
    
- **Décider**: eDiscovery Avancé affiche les résultats de l’analyse appliquée au cas entière après le calcul du lot et affiche les données pour prendre des décisions de révision de document.
    
- **Test**: résultats eDiscovery avancées peuvent être testées pour vérifier la validité et l’efficacité du traitement avancé eDiscovery.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Recommandations pour la formation de la pertinence et passer en revue les

Voici une vue d’ensemble d’instructions pour la formation de la pertinence et passer en revue les :
  
- **Erreurs et les incohérences**: si des erreurs de liaison sont effectuées au cours de formation, revenir aux exemples de fichier précédente pour y remédier. S’il y trop grand nombre d’erreurs à corriger ou il existe un nouveau point de vue de l’incident ou un problème, les critères de la pertinence doivent être redéfinis par l’administrateur et redémarré la formation de pertinence.
    
- **Balisage et formation**: 
    
  - Les fichiers doivent être référencées en fonction du contenu uniquement. Ne pas tenir compte des métadonnées, telles que les dépositaires, la date ou chemin d’accès du fichier. 
    
  - Considérez date indications plage du texte pour marquer les fichiers.
    
  - Considérez les images graphiques incorporés pour marquer les fichiers.
    
  - Si l’affichage d’un fichier à l’aide de l’icône de **mise en forme de texte** lors de la liaison, considérez la mise en forme de texte. Par exemple, un mot barré (une ligne horizontale par le biais de son centre de suppression) est considéré comme toujours par pertinence dans le cadre du texte analysé. 
    
  - Ignorer le texte appliqué à la pertinence (tel que défini par le Gestionnaire d’incidents ou d’un administrateur) sera supprimé dans le contenu du fichier affiché dans l’affichage de texte dans la pertinence. Si les valeurs de texte de la case à cocher Ignorer ont été définies après la pertinence de la formation déjà démarré, le nouveau texte ignoré sera appliqué à des exemples de fichiers créés à partir du point dans lequel il a été défini. La fonctionnalité d’ignorer le texte doit être utilisée avec précaution, comme son utilisation peut réduire les performances de l’analyse des fichiers
    
  - Utilisez l’option **Ignorer le balisage** uniquement lorsque cela est nécessaire. EDiscovery avancée ne pas former basé sur les fichiers ignorés. Évaluation, s’il est difficile de déterminer si un fichier est pertinent, il est préférable de balise en tant que Relevant (R) ou non pertinent (NR) chaque fois que possible au lieu de sélectionner **Ignorer**. Lors de la découverte avancée évalue la formation, il sera visible bien ces types de fichiers ont été traités.
    
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
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

