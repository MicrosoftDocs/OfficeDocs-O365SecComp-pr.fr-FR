---
title: Analyse de la pertinence de test dans Office 365 avancée de découverte électronique
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Découvrez comment utiliser l’onglet Test après le calcul de lot dans Office 365 avancée de découverte électronique à tester, comparer et valider la qualité globale de traitement.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528121"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a>Analyse de la pertinence de test dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
L’onglet Test d’eDiscovery avancée vous permet de test, comparer et valider la qualité globale de traitement. Ces tests sont effectuées après le calcul de lot. En les balisant les fichiers de la collection, à un expert rend le jugement final si chaque fichier avec balise est réellement pertinent pour le cas. 
  
Dans les scénarios uniques et plusieurs problèmes, tests sont généralement effectuées par le problème. Les résultats sont affichés après chaque test, et peuvent être réorganisation des résultats des tests avec spécifié d’exemples de fichiers de test.
  
## <a name="testing-the-rest"></a>Test du reste

Le test « Tester le reste » est utilisé pour valider les décisions élimination, par exemple, pour consulter uniquement les fichiers ci-dessus un score démarcation la pertinence spécifique en fonction des résultats final eDiscovery avancées. L’expert examine un échantillon de fichiers sous un score limite sélectionné à évaluer le nombre de fichiers appropriés dans cet ensemble.
  
Ce test fournit des statistiques et une comparaison entre l’ensemble de la révision et le Test de la population Rest. Les résultats de l’ensemble de révision sont ceux calculés par pertinence au cours de formation. Les résultats incluent des calculs, en fonction des paramètres et des paramètres d’entrée, tels que :
  
- Tester les statistiques du nombre de fichiers d’exemple dans un exemple et identifié les fichiers appropriés. 
    
- Tabulaire comparaison des paramètres de remplissage de l’ensemble de la révision et le reste, par exemple, le nombre de fichiers, une estimation du nombre de fichiers concernés, richesse estimé et le coût moyen de trouver un fichier pertinent supplémentaire. Paramètres coût peuvent être définis par l’administrateur.
    
1. Ouvrir le **pertinence \> Test** onglet. 
    
2. Dans l’onglet **Test** , cliquez sur **Nouveau test**. La boîte de dialogue **créer de test** s’affiche, comme illustré dans l’exemple suivant. 
    
    ![Résultats de pertinence du test Tester les éléments restants](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. Dans **nom du Test**et **Description**, tapez le nom et la description.
    
4. Dans la liste **type de Test** , sélectionnez **le reste de Test**
    
5. Dans la **problème / catégorie** , sélectionnez le nom du problème. 
    
6. Dans la liste **de charge** , sélectionnez la charge. 
    
7. Dans **% lecture**, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence de la coupure. 
    
8. Dans **définir la taille**, ou acceptez la valeur par défaut. Notez que les icônes de restauration restaure les valeurs par défaut.
    
9. Cliquez sur **Démarrer la liaison**. Un exemple de test est généré.
    
10. Passez en revue et ajouter une balise à chacun des fichiers dans le **la pertinence \> balise** onglet et lorsque vous avez terminé, cliquez sur **Calculer**.
    
11. Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour voir les résultats des tests. Un exemple est illustré dans la figure suivante. 
    
    ![Résultats du test Tester les éléments restants](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
Dans la figure ci-dessus, la section **paramètres de l’exemple** de la table contient plus d’informations sur le nombre de fichiers dans l’exemple par l’expert et le nombre de fichiers pertinents trouvés dans cet exemple. 
  
La section **paramètres de remplissage** de la table contient les résultats des tests, y compris la population set passer en revue les fichiers avec une note inférieure à la limite sélectionné et population « Le reste » des fichiers dont le score au-dessus de la limite sélectionnée. Pour chaque type de remplissage, les résultats suivants sont affichés : 
  
- Inclut des fichiers avec % lecture - limite indiquée
    
- Le nombre total de fichiers 
    
- Estimation du nombre de fichiers concernés 
    
- La plus grande richesse estimée 
    
- Le coût moyen de révision de recherche d’un autre fichier pertinent
    
## <a name="testing-the-slice"></a>Test de la section

Le « tester le secteur « test exécute le test similaire à « Tester le reste » de test, mais à un segment du fichier définie comme spécifié par la pertinence de la lecture %.
  
1. Ouvrir le **pertinence \> Test** onglet. 
    
2. Dans l’onglet **Test** , cliquez sur **Nouveau test**. La boîte de dialogue **créer de test** s’affiche. 
    
3. Dans **nom du Test** et **Description**, tapez les informations.
    
4. Dans la liste **type de Test** , sélectionnez **Test le secteur**.
    
5. Dans la liste de **problème** , sélectionnez le nom du problème. 
    
6. Dans la liste **de charge** , sélectionnez la charge. 
    
7. Dans **% lecture entre**, acceptez les valeurs de la plage minimale et maximale par défaut ou sélectionnez des valeurs pour les résultats de la pertinence de la coupure. 
    
8. Dans **définir la taille**, sélectionnez une valeur, ou acceptez la valeur par défaut.
    
    Les icônes de restauration permet de restaurer la valeur par défaut.
    
9. Cliquez sur **Démarrer la liaison**. Un exemple de test est généré.
    
10. Passez en revue et ajouter une balise à chacun des fichiers dans le **la pertinence \> balise** onglet et lorsque vous avez terminé, cliquez sur **Calculer**. 
    
11. Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour voir les résultats des tests. 
    
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Évaluation de la présentation de la pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Marquage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Marquage et formation de pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence de suivi](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Selon les résultats de la sélection du conteneur](decision-based-on-the-results-in-advanced-ediscovery.md)

