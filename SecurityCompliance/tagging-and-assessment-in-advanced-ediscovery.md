---
title: Marquage et évaluation d’Office 365 avancée d’eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Passez en revue les étapes nécessaires pour effectuer la formation d’évaluation, y compris le balisage de fichiers et de révision des résultats de l’évaluation d’Office 365 avancée d’eDiscovery. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527971"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a>Marquage et évaluation d’Office 365 avancée d’eDiscovery

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette section décrit la procédure pour le module d’évaluation de la pertinence de la découverte électronique avancées. 
  
## <a name="performing-assessment-training-and-analysis"></a>Effectue l’analyse et formation d’évaluation

1. Dans la **la pertinence \> suivi** , cliquez sur **évaluation** pour démarrer l’évaluation. 
    
    Par exemple, à des fins de cette procédure, un ensemble d’évaluation d’exemples de 500 fichiers est créé et l’onglet **balise** s’affiche, qui contient le balisage de panneau, de contenu du fichier affiché et d’autres options de liaison. 
    
    ![Onglet Balise de pertinence pour l’évaluation](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. Passez en revue chaque fichier dans l’exemple, de déterminer la pertinence du fichier pour chaque problème de cas et le fichier à l’aide de la Relevance (R), ne pas de balise pertinent (NR) et ignorer les boutons dans le volet du **Panneau de configuration de balisage** . 
    
    > [!NOTE]
    >  Évaluation nécessite des fichiers balisés 500. Si les fichiers sont « ignorés », vous recevrez plus de fichiers balise. 
  
3. Après la mise en réseau de tous les fichiers dans l’exemple, cliquez sur **Calculer**. 
    
    La marge d’erreur évaluation actuelle et une plus grande richesse sont calculés et affichés dans l’onglet **Suivi de la pertinence** , avec des détails de développé par le problème, comme illustré ci-dessous. Plus d’informations sur cette boîte de dialogue sont décrits dans la section « Résultats de la révision des évaluations ». 
    
    ![Suivi de pertinence - Évaluation](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > Par défaut, il est recommandé que vous passez à l’étape suivante par défaut à l’issue de l’indicateur de progression d’évaluation pour le problème, indiquant que l’exemple d’évaluation a été révisé et fichiers concernés suffisantes ont été marquées. > Dans le cas contraire, si vous souhaitez afficher les résultats de l’onglet **suivi** et le contrôle de la marge d’erreur et l’étape suivante, cliquez sur **Modifier** adjacent à **l’Étape suivante**, sélectionnez **évaluation continuer**, puis cliquez sur **OK**. 
  
1. Cliquez sur **Modifier** à droite de la case à cocher **Assessment** pour afficher et spécifier les paramètres d’évaluation par le problème. Une boîte de dialogue **niveau d’évaluation** pour chaque problème s’affiche, comme illustré dans l’exemple suivant : 
    
    ![Problème de cas de niveau d’évaluation](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    Les paramètres suivants pour le problème sont calculées et affichées dans la boîte de dialogue **niveau d’évaluation** : 
    
    **Estimations de la marge d’erreur cible pour le rappel**: selon cette valeur, l’estimation du nombre de fichiers supplémentaires nécessaires pour passer en revue est calculé. La marge utilisée pour le rappel est supérieure à 75 % et avec un niveau de confiance de 95 %. 
    
    **Fichiers d’évaluation supplémentaires requis**: indique le nombre de fichiers plus est nécessaire si les conditions requises de la marge d’erreur actuel n’ont pas été respectées. 
    
2. Pour ajuster la marge d’erreur actuel et voir l’effet des marges d’erreur différents (par problème) :
    
1. Dans la liste **Sélectionnez le problème** , sélectionnez un problème. 
    
2. Dans la **marge d’erreur cible pour le rappel estime**, entrez une nouvelle valeur.
    
3. Cliquez sur **mettre à jour des valeurs** pour voir l’impact des ajustements. 
    
3. Cliquez sur **Options avancées** dans la boîte de dialogue **niveau d’évaluation** pour voir les détails des paramètres supplémentaires suivants : 
    
    ![Vue avancée de problème de cas de niveau d’évaluation](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    **Plus grande richesse estimée**: estimée richesse en fonction des résultats de la dernière évaluation
    
    **Pour le rappel supposée**: par défaut, la marge d’erreur cible s’applique pour rappeler supérieur à 75 %. Si vous souhaitez modifier ce paramètre et contrôler la marge d’erreur dans une plage de valeurs de rappel différente, cliquez sur **Modifier** . 
    
    **Niveau de confiance**: par défaut, la marge d’erreur recommandée pour le niveau de confiance est 95 %. Si vous souhaitez modifier ce paramètre, cliquez sur **Modifier** . 
    
    **Marge d’erreur attendue richesse**: étant donné les valeurs mises à jour, ceci est la marge d’erreur de la plus grande richesse, attendue une fois que tous les fichiers d’évaluation supplémentaires sont examinés.
    
    **Fichiers d’évaluation supplémentaires requis**: étant donné les valeurs mises à jour, le nombre d’évaluation supplémentaire des fichiers qui doivent être examinées pour atteindre la cible.
    
    **Fichiers total évaluation requis**: étant donné les valeurs mises à jour, nombre total de fichiers d’évaluation requis pour révision.
    
    **Nombre attendu de fichiers pertinents dans l’évaluation**: étant donné les valeurs mises à jour, le nombre attendu de fichiers appropriés dans l’évaluation une fois que tous les fichiers d’évaluation supplémentaires sont examinés.
    
4. Cliquez sur **Recalculer les valeurs**, si les paramètres sont modifiés. Lorsque vous avez terminé, s’il existe un problème, cliquez sur **OK** pour enregistrer les modifications (ou **suivant** quand il y a plusieurs problèmes pour vérifier ou modifier, puis sur **Terminer**). 
    
    Lorsqu’il existe plusieurs problèmes, une fois que tous les problèmes qui ont été révisées ou ajustées, un **niveau d’évaluation : synthèse** boîte de dialogue s’affiche, comme illustré dans l’exemple suivant. 
    
    ![Résumé de niveau d’évaluation](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    En cas de réussite d’évaluation, passez à l’étape suivante de la formation de pertinence.
    
## <a name="reviewing-assessment-results"></a>Examen des résultats de l’évaluation

Une fois un exemple d’évaluation est marqué, les résultats de l’évaluation sont calculés et affichés dans l’onglet suivi de la pertinence.
  
Les résultats suivants sont affichés dans l’affichage de piste étendue : 
  
- Estimations de la marge d’erreur actuelle évaluation d’un rappel
    
- Plus grande richesse estimée
    
- Fichiers d’évaluation supplémentaires requis (pour révision)
    
La marge d’erreur actuelle évaluation est la marge d’erreur recommandée par eDiscovery avancée. Le numéro affiché pour les « fichiers évaluation supplémentaires requis » correspond à cette recommandation.
  
L’indicateur de progression évaluation indique le niveau d’achèvement de l’évaluation, selon la marge d’erreur en cours. Lors de l’évaluation est en cours, l’utilisateur permet d’identifier un autre exemple d’évaluation.
  
Lorsque l’indicateur de progression évaluation indique évaluation comme étant terminée, cela signifie que l’évaluation d’exemple a été effectuée et fichiers concernés suffisantes ont été marquées. 
  
L’affichage de piste étendue affiche l’étape suivante recommandée, les statistiques d’évaluation et l’accès aux résultats détaillés.
  
Lors de la plus grande richesse est très faible, le nombre de fichiers d’évaluation supplémentaires nécessaires pour atteindre un nombre minimal de fichiers appropriés pour produire des statistiques utiles est très élevé. Découverte avancée recommande à passer à la formation. L’indicateur de progression de l’évaluation sera appliquée, et aucune statistique ne sera disponible. 
  
En l’absence de statistiques en fonction de stabilisation, il sera résultats avec un niveau de précision et la fiabilité de niveau inférieur. Toutefois, ces résultats utilisable pour rechercher les fichiers pertinents lorsque vous n’avez pas besoin de connaître le pourcentage de fichiers appropriés. De même, ce statut peut servir à former des problèmes avec la plus grande richesse faible, où les résultats de la pertinence peuvent accélérer l’accès aux fichiers pertinents pour un problème spécifique.
  
> [!TIP]
> Dans la **la pertinence \> suivi** onglet, problème étendue d’affichage, les options d’affichage suivantes sont disponibles : > étape suivante recommandée, tel que **étape suivante : balisage** peut être ignorée (par problème) en cliquant sur le bouton **Modifier** pour son droite, puis en sélectionnant une autre étape dans l' **étape suivante**. Lorsque l’indicateur de progression d’évaluation n’est pas terminée, évaluation sera l’option recommandée suivante pour ajouter une balise à plusieurs fichiers d’évaluation et d’améliorer la précision des statistiques. > Vous pouvez modifier la marge d’erreur et évaluer l’impact, en cliquant sur **Modifier**et dans la **boîte de dialogue évaluation niveau**et modification de **marge d’erreur cible pour le rappel estime**, en cliquant sur les **valeurs de mise à jour**. En outre, dans cette boîte de dialogue, vous pouvez afficher les options avancées, en cliquant sur **Options avancées**. > Vous pouvez afficher les statistiques de niveau d’évaluation supplémentaires et leur impact en cliquant sur **Afficher**. Dans la boîte de dialogue de résultats détail affichée, les statistiques sont disponibles par le problème, lorsqu’il existe au moins 500 fichiers évaluation avec balise et au moins 18 fichiers marqués comme pertinents pour le problème. 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Test d’analyse de la pertinence](test-relevance-analysis-in-advanced-ediscovery.md)

