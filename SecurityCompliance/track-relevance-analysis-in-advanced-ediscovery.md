---
title: Suivre l’analyse de la pertinence dans Office 365 avancée de découverte électronique
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Découvrez comment afficher et interpréter l’état de la pertinence de la configuration et les résultats de problèmes dans Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528757"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a>Suivre l’analyse de la pertinence dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
D’eDiscovery avancée, l’onglet suivi de la pertinence affiche la validité de la formation de pertinence effectuée dans l’onglet balise calculée et indique l’étape suivante à prendre dans le processus de formation itératif à la pertinence. 
  
## <a name="tracking-relevance-training-status"></a>Suivi de l’état de formation de pertinence

1. Afficher les détails suivants de la pertinence de la piste pour les problèmes, comme illustré dans l’exemple suivant d’une boîte de dialogue **nom du problème** ci-dessous. 
    
  - **Évaluation**: cet indicateur de progression indique dans quelle mesure la pertinence de formation effectuées à ce stade est parvenu à la cible d’évaluation en termes de marge d’erreur. La plus grande richesse des résultats la pertinence de la formation est également affiché. 
    
  - **Formation**: cet affichage d’indicateur et info-bulle sur l’avancement indique la formation de la pertinence des résultats de la stabilité et une échelle numérique indiquant le nombre d’exemples de formation pertinence marqués pour chaque problème. L’expert surveille la progression du processus de formation de pertinence itératif. 
    
  - **Calcul du lot**: cet indicateur de progression fournit des informations sur la réalisation de calcul de lot.
    
  - **Étape suivante**: affiche la recommandation pour la prochaine étape à effectuer. 
    
    Dans l’exemple, une évaluation correctement effectuée pour un problème indiqué par l’indicateur de progression terminé couleur et la coche est affichée. Marquage est en cours, mais celle-ci est considérée comme instable (état de la stabilité apparaissent également dans une info-bulle). La recommandation étape suivante est « formation ». 
    
    ![Formation de suivi de pertinence étape 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    La vue étendue affiche les options et les informations supplémentaires. La marge d’erreur actuel affiché est la marge d’erreur d’un rappel dans l’état actuel de l’évaluation, étant donnée les fichiers d’évaluation (déjà référencé) existant.
    
    > [!NOTE]
    >  La phase d’évaluation peut être ignorée en désactivant la case à cocher **évaluation** par le problème, puis pour « tous les problèmes ». Toutefois, par conséquent, il n’y aura aucuns statistiques pour ce problème. > Si vous décochez la case à cocher **évaluation** uniquement peut être effectuée avant l’évaluation est effectuée. Il existe plusieurs problèmes dans un cas, évaluation est contournée uniquement si la case à cocher est désactivée pour chaque problème 
  
    Lors de l’évaluation n’est pas achevée avec le premier exemple de jeu de fichiers, évaluation peut être l’étape suivante pour marquer le plus de fichiers. 
    
    Dans **la pertinence** \> **le suivi**, l’indicateur de progression de formation et info-bulle indiquent l’estimation du nombre d’échantillons supplémentaires nécessaires pour atteindre la stabilité. Cette estimation fournit des indications pour la formation supplémentaire nécessaire.
    
    ![Formation de suivi de pertinence](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. Lorsque vous avez terminé de marquer et si vous souhaitez continuer de formation, cliquez sur **formation**. Exemple d’ensemble de fichiers est généré à partir du fichier chargé définie pour une formation supplémentaire. Puis, vous revenez à l’onglet balise pour baliser et former plusieurs fichiers.
    
### <a name="reaching-stable-training-levels"></a>Atteindre les niveaux de formation stable

Une fois les fichiers d’évaluation ont atteint un niveau stable de formation, eDiscovery avancée est prêt pour le calcul de lot.
  
> [!NOTE]
> En règle générale, après que trois stable des exemples de formation, l’étape suivante est « Calcul du lot ». Il peut exister des exceptions, par exemple, lorsqu’il y avait des modifications pour le marquage des fichiers à partir des exemples précédents ou lorsque les fichiers d’amorçage ont été ajoutés. 
  
### <a name="performing-batch-calculation"></a>Effectuer le calcul de lot

Calcul du lot est exécuté en tant que l’étape suivante après que la formation est terminée (lorsque l’état stable formation est indiqué par la barre de progression, une coche et l’état stable dans l’info-bulle.) Calcul du lot s’applique à la base de connaissances acquise au cours de la formation de pertinence pour l’intégralité du fichier de la population, pour évaluer la pertinence des fichiers et affecter les résultats de la pertinence.
  
Lorsqu’il existe plusieurs problèmes, calcul du lot s’effectue par le problème. Lors du calcul de lot, l’avancement est analysé lors du traitement de tous les fichiers. 
  
Dans ce cas, l’étape suivante recommandée est « None », qui indique qu’aucune formation pertinence itérative supplémentaire n’est nécessaire à ce stade. La phase suivante est la **la pertinence \> Decide** onglet. 
  
Si vous souhaitez importer de nouveaux fichiers après le calcul de lot, l’administrateur peut ajouter les fichiers importés à une charge de nouveau.
  
> [!NOTE]
> Si vous cliquez sur **Annuler** lors du calcul de lot, le processus enregistre ce qui a déjà été exécuté. Si vous exécutez à nouveau calcul du lot, le processus se poursuit à partir du dernier point exécuté. 
  
### <a name="assessing-tagging-consistency"></a>Évaluation de la cohérence de liaison

S’il existe des incohérences de marquer le fichier, il peut affecter l’analyse. La découverte avancée la cohérence des processus de balisage peut être utilisée lorsque les résultats ne sont pas optimaux ou cohérence est dans le doute. Une liste de fichiers de façon incohérente avec balise possibles est renvoyée, et ils peuvent être consultés et nouveau balisés, si nécessaires.
  
> [!NOTE]
> Après avoir au moins sept arrondit formation évaluation suivante, la cohérence de balisage peut être affichée dans **la pertinence** \> **suivi** \> **problème** \> **résultats détaillés** \> **cours de formation**. Cette révision est effectuée pour un seul problème à la fois. 
  
1. Dans **pertinence \> suivi**, développez la ligne d’un problème.
    
2. À droite de **l’étape suivante**, cliquez sur **Modifier**.
    
3. Sélectionnez l’option de **l’étape suivante** , après sept exemples de formation **incohérences de balise** , cliquez sur **OK**.
    
4. Sélectionnez les **incohérences de la balise**. L’onglet **balise** s’ouvre, affichant une liste des incohérences pour baliser nouveau que nécessaire. 
    
5. Cliquez sur **Calculer** pour valider les modifications. L’étape suivante après que le marquage des incohérences est « formation ». 
    
## <a name="viewing-and-using-relevance-results"></a>Affichage et utilisation des résultats de la pertinence

Dans la **la pertinence \> suivi** onglet, développez la ligne d’un problème et en regard des **résultats détaillés**, cliquez sur **Afficher**. Les volets de résultats détaillés sont affichées, comme indiqué et décrit ci-dessous.
  
![Résultats détaillés de la formation de pertinence](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a>Résumé de liaison

 Dans l’exemple ci-dessous, le **balisage synthèse** affiche des totaux pour chaque fichier rattrapage marquer le processus, de formation et évaluation. 
  
![Résumé du marquage du suivi de pertinence](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a>Keywords

Un mot clé est une chaîne unique, word, une expression ou séquence de mots dans un fichier identifiée par eDiscovery avancée comme un indicateur significatif si un fichier est pertinent. Mot clé et poids en fichiers marqués comme pertinents de liste colonnes « Include », et les colonnes « Exclure » répertorie les mots clés et poids en fichiers marqués comme non pertinents.
  
EDiscovery avancée assigne les valeurs de poids de mot clé positive ou négative. Plus le poids est élevé, plus la probabilité qu’un fichier dans lequel apparaît le mot clé est affecté un score de pertinence plus élevé lors du calcul de lot. 
  
La liste de découverte électronique avancée des mots clés peut servir à compléter une liste générée par un expert ou dans un contrôle de validité indirect à tout moment dans le fichier de processus de révision.
  
### <a name="training-progress"></a>Cours de formation

Le volet **Des cours de formation** inclut un formation affichage en cours de graphique et la qualité indicateur, comme illustré dans l’exemple ci-dessous. 
  
![Avancement de la formation de suivi de pertinence](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 **Indicateur de qualité de formation**: affiche l’évaluation de la cohérence de liaison comme suit :
  
- **Bonne**: fichiers marqués régulièrement. (Vert clair affichées)
    
- **Moyenne**: certains fichiers peuvent être marqués de façon incohérente. (Jaune clair affichées)
    
- **Avertissement**: nombre de fichiers peut-être être marqué de façon incohérente. (Rouge clair affichées)
    
 **Graphique des cours de formation**: indique le degré de stabilité de formation de pertinence après un nombre de cycles de formation de pertinence par rapport à la valeur de mesure-F. Comme nous déplacer de gauche à droite dans le graphique, la permet de réduire intervalle de confiance et est utilisée, ainsi que la mesure F, eDiscovery avancée pertinence afin de déterminer la stabilité lorsque la formation de la pertinence des résultats sont optimisées.
  
> [!NOTE]
> La pertinence utilise une mesure F-mesure où rappel reçoit deux fois plus poids précision F2. Pour les cas avec la plus grande richesse haute (plus de 25 %), utilise la pertinence F1 (rapport 1:1). Le rapport de mesure F peut être configuré dans **le programme d’installation de la pertinence** \> **Paramètres avancés**. 
  
### <a name="batch-calculation-results"></a>Résultats du calcul de lot

Le volet de **résultats de calcul** inclut le nombre de fichiers qui ont été marqués pour la pertinence, comme suit : 
  
- **Opération réussie**
    
- **Vide**: ne contient aucun texte, par exemple, seuls les espaces/onglets
    
- **Échec**: en raison de la taille d’un nombre excessif ou n’a pas pu être lues.
    
- **Ignoré**: en raison de la taille d’un nombre excessif
    
- **Nebulous**: contient du texte sans signification ou aucune fonctionnalité pertinentes pour le problème
    
> [!NOTE]
> Vide, échec, ignoré ou Nebulous reçoit un score de pertinence de -1. 
  
### <a name="training-statistics"></a>Statistiques de formation

Le volet des **statistiques de formation** affiche les statistiques et les graphiques en fonction des résultats à partir de la formation de la pertinence de la découverte électronique avancées. 
  
![Statistiques de la formation de suivi de pertinence](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
Cet affichage montre les points suivants :
  
- **Taux de révision rappel**: comparaison des résultats en fonction de la pertinence de scores dans un examen hypothèse linéaire. Rappel est estimée étant donné la taille de jeu de révision.
    
- **Paramètres**: Cumulative calculé statistiques relatives à la révision par rapport à la population de fichier pour le dossier entier.
    
- **Passez en revue**: pourcentage de fichiers pour passer en revue en fonction de cette limite.
    
- **Rappeler**: pourcentage de pertinents des fichiers dans le jeu de révision. 
    
- **Distribution par score de pertinence**: fichiers dans l’affichage gris foncé vers la gauche sont sous le score de coupure. Une info-bulle affiche le score de pertinence et le pourcentage de fichiers associé dans le fichier de révision défini en fonction du nombre total de fichiers.
    
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Exécution et évaluation de révision](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Effectue la formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Prendre des décisions basées sur les résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

