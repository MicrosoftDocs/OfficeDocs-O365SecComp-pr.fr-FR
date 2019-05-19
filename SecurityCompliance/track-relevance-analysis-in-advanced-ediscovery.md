---
title: Suivi de l’analyse de pertinence dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Découvrez comment afficher et interpréter la pertinence état de formation et résultats pour les problèmes de cas dans Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 1018b414d0192491feebfbec25d865d4463fa26a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158326"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a>Suivi de l’analyse de pertinence dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Advanced eDiscovery, l’onglet suivi de pertinence affiche la validité calculée de la formation à la pertinence effectuée dans l’onglet balise et indique l’étape suivante à effectuer dans le processus de formation itérative en matière de pertinence. 
  
## <a name="tracking-relevance-training-status"></a>Suivi de l’état de formation à la pertinence

1. Consultez les détails suivants dans le suivi de pertinence pour les problèmes de cas, comme indiqué dans l’exemple suivant d’une boîte de dialogue **nom du problème** ci-dessous. 
    
  - **Évaluation**: cet indicateur de progression indique dans quelle mesure la formation pertinente effectuée à ce stade a atteint la cible de l’évaluation en termes de marge d’erreur. La richesse des résultats d’apprentissage de pertinence est également affichée. 
    
  - **Formation**: cet indicateur de progression codé en couleur et l’affichage de l’info-bulle indiquent la pertinence des résultats de formation pertinents et une balance numérique illustrant le nombre d’exemples d’apprentissage de pertinence marqués pour chaque problème. L’expert surveille la progression du processus de formation à la pertinence itératif. 
    
  - **Calcul par lot**: cet indicateur de progression fournit des informations sur la fin du calcul du lot.
    
  - **Étape suivante**: affiche la recommandation pour l’étape suivante à effectuer. 
    
    Dans l’exemple, une évaluation réussie pour un problème est illustrée par l’indicateur de progression des couleurs terminées et la coche. Le marquage est en cours, mais le cas est toujours considéré comme instable (l’état de stabilité apparaît également dans une info-bulle). La recommandation suivante est la «formation». 
    
    ![Formation de suivi de pertinence étape 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    L’affichage développé affiche des informations et des options supplémentaires. La marge d’erreur actuelle affichée est la marge d’erreur du rappel dans l’état actuel de l’évaluation, étant donné les fichiers d’évaluation existants (déjà balisés).
    
    > [!NOTE]
    >  La phase d’évaluation peut être ignorée en désactivant la case à cocher **évaluation** par problème, puis pour «tous les problèmes». Toutefois, il n’y aura pas de statistiques pour ce problème. > la désactivation de la case à cocher **évaluation** ne peut être effectuée qu’avant l’évaluation. Dans le cas où plusieurs problèmes existent, l’évaluation est ignorée uniquement si la case à cocher est désactivée pour chaque problème. 
  
    Lorsque l’évaluation n’est pas effectuée avec le premier ensemble de fichiers, l’évaluation peut être la prochaine étape de marquage de fichiers supplémentaires. 
    
    Dans le **suivi**de **pertinence** \> , l’indicateur de progression de formation et le Conseil d’outils indiquent le nombre estimé d’échantillons supplémentaires nécessaires pour atteindre la stabilité. Cette estimation fournit une indication pour la formation supplémentaire requise.
    
    ![Formation de suivi de pertinence](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. Lorsque vous avez fini d’étiqueter et si vous devez poursuivre la formation, cliquez sur **formation**. Un autre exemple de jeu de fichiers est généré à partir du jeu de fichiers chargé pour une formation supplémentaire. Vous revenez ensuite à l’onglet balise pour marquer et former davantage de fichiers.
    
### <a name="reaching-stable-training-levels"></a>Atteindre des niveaux de formation stables

Une fois que les fichiers d’évaluation ont atteint un niveau de formation stable, Advanced eDiscovery est prêt pour le calcul par lot.
  
> [!NOTE]
> En règle générale, après trois exemples de formation stables, l’étape suivante est «calcul par lot». Il peut y avoir des exceptions, par exemple, lorsque des modifications ont été apportées au balisage des fichiers provenant d’exemples précédents ou lors de l’ajout de fichiers Seed. 
  
### <a name="performing-batch-calculation"></a>Exécution du calcul par lot

Le calcul du lot est exécuté en tant que prochaine étape une fois la formation terminée (lorsqu’un état de formation stable est affiché dans la barre de progression, un état de coche et de stabilité dans le Conseil d’outils). Le calcul par lot applique les connaissances acquises lors de la formation à la pertinence à l’ensemble du remplissage du fichier, afin d’évaluer la pertinence des fichiers et d’affecter des scores de pertinence.
  
Lorsqu’il y a plusieurs problèmes, le calcul du lot est effectué par problème. Pendant le calcul du lot, la progression est surveillée lors du traitement de tous les fichiers. 
  
Ici, l’étape suivante recommandée est «None», ce qui indique qu’aucune formation de pertinence itérative supplémentaire n’est requise à ce stade. La phase suivante est l' **onglet \> décider** de la pertinence. 
  
Si vous souhaitez importer de nouveaux fichiers après le calcul par lot, l’administrateur peut ajouter les fichiers importés à une nouvelle charge.
  
> [!NOTE]
> Si vous cliquez sur **Annuler** pendant le calcul du lot, le processus enregistre ce qui a déjà été exécuté. Si vous réexécutez le calcul du lot, le processus se poursuit depuis le dernier point exécuté. 
  
### <a name="assessing-tagging-consistency"></a>Évaluation de la cohérence des marquages

S’il existe des incohérences dans le balisage de fichier, cela peut avoir une incidence sur l’analyse. Le processus avancé de cohérence des balises eDiscovery peut être utilisé lorsque les résultats ne sont pas optimaux ou si la cohérence est incertaine. Une liste de fichiers susceptibles d’être balisés de manière incohérente est renvoyée et peuvent être révisées et ré-balisage, si nécessaire.
  
> [!NOTE]
> Après l’évaluation de sept ou plusieurs arrondis de formation, la cohérence du **** \> marquage peut être affichée dans la **formation**sur **le suivi** \> **** \> des **résultats** \> détaillés. Cette révision est réalisée pour un problème à la fois. 
  
1. Dans **le \> suivi de pertinence**, développez la ligne d’un problème.
    
2. À droite de l' **étape suivante**, cliquez sur **modifier**.
    
3. Sélectionnez **** incohérences de balise comme **étape suivante** , après sept exemples de formation, puis cliquez sur **OK**.
    
4. Sélectionnez **** incohérences de balise. L' **** onglet balise s’ouvre et affiche la liste des incohérences à réactiver. 
    
5. Cliquez sur **calculer** pour envoyer les modifications. L’étape suivante, après le marquage des incohérences, est «formation». 
    
## <a name="viewing-and-using-relevance-results"></a>Affichage et utilisation des résultats de pertinence

Dans l' **onglet \> suivi de pertinence** , développez la ligne d’un problème, puis en regard de **résultats détaillés**, cliquez sur **Afficher**. Les volets de résultats détaillés sont affichés, comme illustré ci-dessous.
  
![Résultats détaillés de la formation de pertinence](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a>Synthèse des marquages

 Dans l’exemple ci-dessous, le **Résumé de marquage** affiche les totaux pour chaque processus d’évaluation, de formation et de marquage de fichier de rattrapage. 
  
![Résumé du marquage du suivi de pertinence](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a>Mots clés

Un mot clé est une chaîne, un mot, une phrase ou une séquence de mots unique identifiée par Advanced eDiscovery comme un indicateur significatif de la pertinence d’un fichier. Le mot clé de liste de colonnes «include» et les pondérations dans les fichiers marqués comme pertinents et les colonnes «Exclude» répertorient les mots clés et les pondérations dans les fichiers marqués comme non pertinents.
  
Advanced eDiscovery affecte des valeurs de pondération de mots clés négatives ou positives. Plus le poids est élevé, plus le score de pertinence d’un fichier dans lequel apparaît le mot clé est élevé pendant le calcul du lot. 
  
La liste de mots-clés eDiscovery avancée peut être utilisée pour compléter une liste créée par un expert ou comme un contrôle de validité indirect à tout moment du processus de révision de fichier.
  
### <a name="training-progress"></a>Progression de la formation

Le volet progression de la **formation** inclut un graphique de progression de formation et un affichage d’indicateur de qualité, comme illustré dans l’exemple ci-dessous. 
  
![Avancement de la formation de suivi de pertinence](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 **Indicateur de qualité de formation**: affiche l’évaluation de la cohérence des balises comme suit:
  
- **Approprié**: les fichiers sont balisés de manière cohérente. (Voyant vert affiché)
    
- **Moyen**: certains fichiers peuvent être balisés de manière incohérente. (Jaune clair affiché)
    
- **Avertissement**: de nombreux fichiers peuvent être balisés de manière incohérente. (Lumière rouge affichée)
    
 **Graphique de progression de formation**: indique le degré de stabilité de la formation à la pertinence après un certain nombre de cycles de formation pertinents par rapport à la valeur de la mesure F. À mesure que nous passons de la gauche vers la droite sur le graphique, l’intervalle de confiance réduit et est utilisé, ainsi que la mesure F, par rapport à l’intérêt eDiscovery avancé afin de déterminer la stabilité lorsque les résultats d’apprentissage pertinents sont optimisés.
  
> [!NOTE]
> La pertinence utilise F2, une mesure F-Measure où le rappel reçoit deux fois plus de poids que la précision. Pour les cas de grande richesse (plus de 25%), la pertinence utilise F1 (ratio 1:1). Le rapport de mesure F peut être configuré dans **** \> **Paramètres avancés**de configuration de pertinence. 
  
### <a name="batch-calculation-results"></a>Résultats du calcul par lots

Le volet **résultats du calcul par lots** inclut le nombre de fichiers dont la pertinence a été évaluée, comme suit: 
  
- **Success**
    
- **Empty**: ne contient pas de texte, par exemple, uniquement des espaces/tabulations
    
- **Échec**: en raison d’une taille excessive ou n’a pas pu être lu
    
- **Ignoré**: en raison d’une taille excessive
    
- **Nebulous**: contient un texte inutile ou aucune fonctionnalité pertinente pour le problème
    
> [!NOTE]
> Empty, failed, ignored ou nebulous recevront un score de pertinence de-1. 
  
### <a name="training-statistics"></a>Statistiques de formation

Le volet **statistiques de formation** affiche les statistiques et les graphiques basés sur les résultats de la formation avancée eDiscovery. 
  
![Statistiques de la formation de suivi de pertinence](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
Cet affichage montre les éléments suivants:
  
- **Review-ratio de rappel**: comparaison des résultats selon les scores de pertinence dans une révision hypothétique. Le rappel est estimé en fonction de la définition de la taille de l’ensemble de révision.
    
- **Paramètres**: statistiques calculées cumulatives relatives au jeu de révision en relation avec le remplissage du fichier pour l’ensemble du cas.
    
- **Révision**: pourcentage de fichiers à vérifier en fonction de ce seuil de troncature.
    
- **Rappel**: pourcentage de fichiers pertinents dans l’ensemble de révision. 
    
- **Répartition par score de pertinence**: les fichiers dans l’affichage gris foncé vers la gauche sont en dessous du score de coupure. Une info-bulle affiche le score de pertinence et le pourcentage de fichiers correspondant dans le jeu de fichiers de révision en relation avec le nombre total de fichiers.
    
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de l’évaluation en matière de pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Exécution et examen de l’évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Prise de décisions en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l’analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

