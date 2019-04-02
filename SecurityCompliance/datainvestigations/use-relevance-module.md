---
title: Utiliser le module de pertinence pour analyser les données dans les preuves
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
ms.openlocfilehash: 3aa37a6778947934759eb652a9367559b9ef838b
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030080"
---
# <a name="use-the-relevance-module-to-analyze-data-in-evidence"></a>Utiliser le module de pertinence pour analyser les données dans les preuves

Dans les enquêtes de données (préversion), le module de pertinence inclut la formation pertinente et la révision des fichiers liés à une enquête. Le flux de travail de pertinence est illustré et décrit comme suit:
  
![Flux de travail de pertinence](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Cycles d'évaluation et de suivi**:
    
  - **Évaluation**: permet une évaluation précoce basée sur un échantillon aléatoire de fichiers et utilise cette évaluation pour appliquer des décisions afin de déterminer les performances du processus de codage prédictif. 
    
  - **Track**: calculer et afficher les résultats intermédiaires de l'évaluation tout en surveillant la validité statistique du processus. 
    
- **Cycles de formation et de suivi**
    
  - **Tag**: enquêtes sur les données (préversion) apprend des critères de pertinence spécifiques à chaque problème en fonction de la révision itérative et du balisage des fichiers individuels d'un expert.
    
  - **Track**: calculer et afficher les résultats intermédiaires de la formation à la pertinence tout en surveillant la validité statistique du processus. 
    
- **Calcul par lots**: les critères de pertinence accumulés et appris sont appliqués à l'ensemble de la collection de fichiers et un score de pertinence est généré pour chaque fichier.
    
- **Décider**: les résultats de l'analyse appliquée à l'ensemble de la casse sont affichés après le calcul du lot, et les données utilisées pour prendre des décisions de révision de document sont affichées.
    
- **Test**: les résultats peuvent être testés pour vérifier la validité et l'efficacité du traitement des analyses de données (aperçu).

- **Recherche**: une fois le flux de travail de pertinence terminé, vous pouvez utiliser la sortie telle que le centile de lecture d'un document pour votre problème lors de l'exécution d'une requête dans votre plage de travail.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Instructions pour la formation et la révision de pertinence

Vous trouverez ci-dessous une vue d'ensemble des directives de formation et de révision:
  
- **Erreurs et**incohérences: si des erreurs de marquage sont effectuées pendant l'apprentissage, revenez aux exemples de fichiers précédents pour les corriger. S'il y a trop d'erreurs à corriger ou qu'il existe une nouvelle perspective ou un problème, les critères de pertinence doivent être redéfinis par l'administrateur et l'apprentissage de pertinence doit être redémarré.
    
- **Balisage et formation**: 
    
  - Les fichiers doivent être balisés en fonction du contenu uniquement. Ne considérez pas les métadonnées, telles que le dépositaire, la date ou le chemin d'accès au fichier. 
    
  - Ne pas tenir compte des indications de plage de dates dans le texte lors du marquage des fichiers.
    
  - Ne considérez pas les images graphiques incorporées lors du balisage des fichiers.
     
  - Ignorer le texte appliqué à la pertinence sera supprimé dans le contenu du fichier affiché dans l'affichage de texte en pertinence. Si les valeurs pour ignorer le texte ont été définies après l'apprentissage de pertinence déjà démarré, le nouveau texte ignoré est appliqué aux fichiers d'exemple créés à partir du point dans lequel ils ont été définis. La fonctionnalité ignorer le texte doit être utilisée avec précaution, car son utilisation peut réduire les performances de l'analyse des fichiers.
    
  - Utilisez l'option **Ignorer** le balisage uniquement lorsque cela est nécessaire. Les enquêtes de données (préversion) ne sont pas basées sur les fichiers ignorés. Dans l'évaluation, s'il est difficile de déterminer si un fichier est pertinent, il est préférable de baliser comme pertinentes (R) ou non pertinente (NR) autant que possible, au lieu de sélectionner **Ignorer**. Lorsque les enquêtes sur les données (aperçu) évaluent la formation, il est possible que ces types de fichiers aient été traités.
    
  - Même les fichiers avec une très petite quantité de texte extrait doivent être balisés en formation sous la forme R/NR, plutôt qu'en tant que «Skip», lorsque cela est possible. 
    
  - Le marquage peut avoir un impact sur le classifieur tant que le fichier est lisible et peut être marqué comme R/NR.
    
  - Le numéro de séquence de fichier de la liste des fichiers d' **** exemple affichés sous l'onglet balise permet à l'utilisateur de revenir à l'ordre d'affichage d'origine des fichiers. 
    
  - Vous pouvez revenir à n'importe quel exemple et modifier le balisage des fichiers d'évaluation et de jeu de formation. Les modifications seront appliquées lors de la création de l'exemple suivant.
    
  - Les fichiers Excel numérisés au format PDF doivent être traités de la même manière que les fichiers Excel natifs lors du balisage des fichiers.
    
  - En cas de doute sur le balisage de pertinence d'un fichier, consultez un expert. Un balisage inCorrect lors de la formation sur la pertinence peut entraîner un manque de temps dans le processus et peut également avoir un impact négatif sur la qualité des résultats globaux.
    
  - Les mots clés définis dans les listes de mots clés s'affichent dans des couleurs pour aider l'utilisateur à identifier les fichiers appropriés lors du marquage.
    
- **Calcul par lots**: les fichiers marqués comme R/NR par l'expert recevront un score de 0 ou de 100. Cela s'applique au marquage effectué avant le calcul du lot. Si l'expert a activé le problème sur inActif après le calcul par lot et a continué à marquer ce problème, les scores nouvellement marqués ne seront pas 100/0 mais plutôt le score d'origine.
    
- **Problèmes et mode d'échantillonnage**: les problèmes sont généralement désactivés lorsqu'ils sont terminés (la formation à la pertinence est stabilisée et le calcul par lot a été effectué), lors de l'annulation des problèmes ou lorsqu'un autre utilisateur travaille sur les problèmes.
    
## <a name="steps-in-relevance-training"></a>Étapes de la formation pertinente

Dans l' **onglet \> suivi de pertinence** , les enquêtes de données fournissent des recommandations sur la façon de procéder au traitement, avec les étapes suivantes. Les implications sont décrites ci-dessous quand chacune des étapes suivantes est recommandée dans le processus de formation à la pertinence. 
  
- Balisage/continuer le balisage: révision de fichier et balisage de pertinence effectuée par un expert pour chaque fichier et problème au sein d'un exemple.
    
  - Implication: un échantillon existant doit être balisé.
    
- Évaluation/continue Assessment: permet une validation précoce de la pertinence du problème et une vue préliminaire de la pertinence du remplissage du fichier importés pour le cas en cours.
    
  - Implication: une évaluation plus grande est requise ou recommandée.
    
- Formation/poursuivez la formation: processus au cours duquel les enquêtes sur les données sont apprises auprès de l'expert qui balise les échantillons de fichiers et qui permettent d'identifier les critères de pertinence pertinents pour chaque problème dans le contexte de chaque cas.
    
  - Implication: le problème nécessite une formation supplémentaire; l'exemple suivant doit être créé et balisé. 
    
- Calcul par lot: processus de pertinence dans lequel les enquêtes de données prennent les connaissances acquises pendant l'étape de formation et les appliquent à l'ensemble du remplissage du fichier. Tous les fichiers du groupe de fichiers pertinent sont évalués à des fins de pertinence et reçoivent un score de pertinence.
    
  - Implication: le problème est stabilisé et le calcul par lot peut être effectué.
    
- Rattrapage: pertinence indique quand un expert examine et marque un échantillon de fichiers sélectionnés à partir d'une charge de fichier supplémentaire lors d'un scénario de charge en continu.
    
  - Implication: une nouvelle charge a été ajoutée et l'interCeption est nécessaire pour continuer à travailler.
    
- Incohérences de balise: le processus identifie, via un algorithme d'analyse des données, des incohérences dans le processus de marquage de fichiers susceptibles d'avoir un impact négatif sur l'analyse.
    
  - Implication: l'exemple suivant inclut des fichiers qui ont été balisés dans les exemples précédents, et leur balisage doit être rétablie.
    
- Mettre à jour le classifieur: permet à l'utilisateur d'appliquer des balises ou des modifications.
    
  - Implication: les modifications de marquage et d'amorçage peuvent être appliquées sans avoir à exécuter manuellement un autre exemple de pertinence.
    
- En attente: le processus d'apprentissage de pertinence est terminé.
    
  - Implication: aucune formation pertinente n'est requise à ce stade.
    
Bien que les enquêtes de données vous guident tout au long du processus, avec les étapes suivantes recommandées à différentes étapes, il vous permet également de naviguer entre les onglets et les pages, et de faire des choix pour répondre aux situations susceptibles de concerner votre cas, problème ou processus de révision de documents. 
  
Il est possible d'accepter ou de remplacer les analyses de données par les choix de traitement de l'étape suivante. Si vous souhaitez effectuer une étape différente de l'étape suivante recommandée, cliquez sur l' **étape suivante** figurant dans la boîte de dialogue Affichage du problème développé dans la boîte de dialogue, cliquez sur le bouton **modifier** en regard de l'étape suivante, puis sélectionnez une autre étape suivante. 
  
> [!NOTE]
> Certaines options peuvent rester désactivées après un déverrouillage, car elles ne sont pas prises en charge à ce stade du processus. 
  
## <a name="more-information"></a>Plus d’informations

[Présentation de l'évaluation en matière de pertinence](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[Balisage et évaluation](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[Étiquetage et formation à la pertinence](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l'analyse de pertinence](../test-relevance-analysis-in-advanced-ediscovery.md)

[InterRoger les données dans les preuves](evidence-query.md)