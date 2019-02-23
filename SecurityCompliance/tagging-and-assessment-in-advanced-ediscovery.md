---
title: Marquage et évaluation dans Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: "Examinez les étapes pour effectuer une formation à l'évaluation, notamment des fichiers de marquage, et en examinant les résultats de l'évaluation dans Office 365 Advanced eDiscovery. "
ms.openlocfilehash: 02dae23b6489b40243272beea1d79e871ca6a911
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217934"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a>Marquage et évaluation dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette section décrit la procédure pour le module d'évaluation de la pertinence eDiscovery avancée. 
  
## <a name="performing-assessment-training-and-analysis"></a>Exécution de la formation et de l'analyse de l'évaluation

1. Sous l' **onglet \> suivi de pertinence** , cliquez sur **évaluation** pour démarrer l'évaluation de cas. 
    
    Dans le cadre de cette procédure, un exemple d'ensemble d'évaluation de 500 fichiers est créé **** et l'onglet balise s'affiche, qui contient le panneau balisage, le contenu du fichier et d'autres options de marquage. 
    
    ![Onglet Balise de pertinence pour l’évaluation](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. Examinez chaque fichier dans l'exemple, déterminez la pertinence du fichier pour chaque problème de cas, et marquez le fichier à l'aide des boutons pertinence (R), non pertinent (NR) et ignorer dans le volet de **marquage** . 
    
    > [!NOTE]
    >  L'évaluation requiert 500 fichiers balisés. Si les fichiers sont «ignorés», vous recevrez plus de fichiers à balise. 
  
3. Après avoir balisé tous les fichiers de l'exemple, cliquez sur **calculer**. 
    
    La marge d'erreur et la richesse de l'évaluation actuelle sont calculées et affichées sous l'onglet de **suivi de pertinence** , avec des détails détaillés par problème, comme illustré ci-dessous. Plus de détails sur cette boîte de dialogue sont décrits dans la section «examen des résultats des évaluations» plus loin. 
    
    ![Suivi de pertinence - Évaluation](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > Par défaut, nous vous recommandons de passer à l'étape suivante par défaut lorsque l'indicateur de progression de l'évaluation du problème est terminé, indiquant que l'exemple d'évaluation a été révisé et que des fichiers appropriés ont été marqués. > sinon, si vous voulez afficher les résultats de l'onglet de **suivi** et contrôler la marge d'erreur et l'étape suivante, cliquez sur **modifier** en regard de l' **étape suivante**, sélectionnez **continuer l'évaluation**, puis cliquez sur **OK**. 
  
1. Cliquez sur **modifier** à droite de la case à cocher **évaluation** pour afficher et spécifier les paramètres d'évaluation par problème. Une boîte de dialogue de **niveau d'évaluation** s'affiche pour chaque problème, comme illustré dans l'exemple suivant: 
    
    ![Problème de cas de niveau d’évaluation](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    Les paramètres suivants du problème sont calculés et affichés dans la boîte de dialogue **niveau d'évaluation** : 
    
    **Marge d'erreur cible pour les estimations de rappel**: en fonction de cette valeur, le nombre estimé de fichiers supplémentaires nécessaires à la révision est calculé. La marge utilisée pour le rappel est supérieure à 75% et avec un niveau de confiance de 95%. 
    
    **Fichiers d'évaluation supplémentaires requis**: indique le nombre de fichiers nécessaires si les exigences actuelles de marge d'erreur n'ont pas été respectées. 
    
2. Pour ajuster la marge d'erreur actuelle et observer l'effet de différentes marges d'erreur (par problème):
    
1. Dans la liste **Sélectionner un problème** , sélectionnez un problème. 
    
2. Dans **marge d'erreur cible pour les estimations de rappel**, entrez une nouvelle valeur.
    
3. Cliquez sur **mettre à jour les valeurs** pour voir l'impact des ajustements. 
    
3. Cliquez sur **avancé** dans la boîte de dialogue **niveau d'évaluation** pour voir les paramètres et détails supplémentaires suivants: 
    
    ![Vue avancée de problème de cas de niveau d’évaluation](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    **Richesse estimée**: richesse estimée en fonction des résultats de l'évaluation actuelle
    
    **Pour le rappel présumé**: par défaut, la marge d'erreur cible s'applique au rappel supérieur à 75%. Cliquez sur **modifier** si vous souhaitez modifier ce paramètre et contrôler la marge d'erreur sur une plage de valeurs de rappel différente. 
    
    **Niveau de confiance**: par défaut, la marge d'erreur recommandée pour la confiance est de 95%. Cliquez sur **modifier** si vous souhaitez modifier ce paramètre. 
    
    **Marge d'erreur de richesse attendue**: en fonction des valeurs mises à jour, il s'agit de la marge d'erreur attendue de la richesse, après examen de tous les fichiers d'évaluation supplémentaires.
    
    **Fichiers d'évaluation supplémentaires requis**: étant donné les valeurs mises à jour, le nombre de fichiers d'évaluation supplémentaires qui doivent être vérifiés pour atteindre la cible.
    
    **Nombre total de fichiers d'évaluation requis**: étant donné les valeurs mises à jour, le nombre total de fichiers d'évaluation requis pour la révision.
    
    **Nombre prévu de fichiers pertinents lors de l'évaluation**: étant donné les valeurs mises à jour, le nombre prévu de fichiers pertinents dans l'intégralité de l'évaluation une fois que tous les fichiers d'évaluation supplémentaires sont examinés.
    
4. Cliquez sur recalculer les **valeurs**si les paramètres sont modifiés. Lorsque vous avez terminé, cliquez sur **OK** pour enregistrer les modifications (ou **suivant** lorsqu'il y a plusieurs problèmes à consulter ou modifier, puis **Terminer**). 
    
    Lorsqu'il existe plusieurs problèmes, une fois que tous les problèmes ont été vérifiés ou ajustés, un **niveau d'évaluation: Résumé** s'affiche, comme illustré dans l'exemple suivant. 
    
    ![Résumé de niveau d’évaluation](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    Une fois l'évaluation terminée, passez à l'étape suivante de la formation pertinente.
    
## <a name="reviewing-assessment-results"></a>Examen des résultats de l'évaluation

Une fois qu'un exemple d'évaluation est balisé, les résultats de l'évaluation sont calculés et affichés sous l'onglet suivi de pertinence.
  
Les résultats suivants s'affichent dans l'affichage de suivi étendu: 
  
- Évaluation de la marge d'erreur actuelle pour les estimations de rappel
    
- Richesse estimée
    
- Fichiers d'évaluation supplémentaires requis (pour révision)
    
L'évaluation de la marge d'erreur actuelle est la marge d'erreur recommandée par Advanced eDiscovery. Le numéro affiché pour le «fichiers d'évaluation supplémentaires requis» correspond à cette recommandation.
  
L'indicateur de progression de l'évaluation indique le niveau d'exécution de l'évaluation, en fonction de la marge d'erreur actuelle. Lorsque l'évaluation est en cours, l'utilisateur balise un autre exemple d'évaluation.
  
Lorsque l'indicateur de progression de l'évaluation indique l'évaluation terminée, cela signifie que la révision de l'exemple d'évaluation a été effectuée et que des fichiers appropriés ont été marqués. 
  
L'affichage de suivi étendu présente l'étape suivante recommandée, les statistiques d'évaluation et l'accès aux résultats détaillés.
  
Lorsque la richesse est très faible, le nombre de fichiers d'évaluation supplémentaires nécessaires pour atteindre un nombre minimal de fichiers pertinents pour produire des statistiques utiles est très élevé. Advanced eDiscovery vous recommande de passer à la formation. L'indicateur de progression de l'évaluation est ombré et aucune statistique n'est disponible. 
  
En l'absence de stabilisation statistiquement basée statistiquement, les résultats seront moins élevés. Toutefois, ces résultats peuvent être utilisés pour rechercher des fichiers pertinents lorsque vous n'avez pas besoin de connaître le pourcentage de fichiers pertinents trouvés. De même, cet État peut être utilisé pour former des problèmes avec une faible richesse, où les scores de pertinence peuvent accélérer l'accès aux fichiers pertinents à un problème spécifique.
  
> [!TIP]
> Dans l' **onglet \> suivi de pertinence** , affichage des problèmes étendus, les options d'affichage suivantes sont disponibles: > l'étape suivante recommandée, telle que l' **étape suivante: le marquage** peut être contourné (par problème) en cliquant sur le bouton **modifier** pour son à droite, puis en sélectionnant une autre étape dans l' **étape suivante**. Lorsque l'indicateur de progression de l'évaluation n'est pas terminé, l'option évaluation est recommandée suivant, pour baliser les fichiers d'évaluation et augmenter la précision des statistiques. > vous pouvez modifier la marge d'erreur et évaluer son impact en cliquant sur **modifier**, puis dans la **boîte de dialogue niveau d'évaluation**, en modifiant la **marge d'erreur cible pour les estimations de rappel**, et en cliquant sur **mettre à jour les valeurs**. De plus, dans cette boîte de dialogue, vous pouvez afficher les options avancées en cliquant sur **avancé**. > vous pouvez afficher des statistiques supplémentaires sur le niveau d'évaluation et leur impact en cliquant sur **affichage**. Dans la boîte de dialogue résultats détaillés affichés, les statistiques sont disponibles par problème, lorsqu'il y a au moins 500 fichiers d'évaluation marqués et que 18 fichiers sont balisés comme pertinents pour le problème. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de l'évaluation en matière de pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Étiquetage et formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Évaluation de l'analyse de pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

