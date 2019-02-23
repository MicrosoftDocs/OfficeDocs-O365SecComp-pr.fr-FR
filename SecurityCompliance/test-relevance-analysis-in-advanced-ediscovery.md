---
title: Tester l’analyse du module Pertinence dans Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: "Découvrez comment utiliser l'onglet test après le calcul par lot dans Office 365 Advanced eDiscovery pour tester, comparer et valider la qualité globale du traitement.  "
ms.openlocfilehash: 735a6d8088b4696e2ebc348db435a11914bd0b10
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215834"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a>Tester l’analyse du module Pertinence dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
L'onglet test dans Advanced eDiscovery vous permet de tester, de comparer et de valider la qualité globale du traitement. Ces tests sont effectués après le calcul par lots. En marquant les fichiers dans la collection, un expert détermine si chaque fichier balisé est pertinent pour le cas. 
  
Dans les scénarios à un ou plusieurs problèmes, les tests sont généralement effectués par problème. Les résultats peuvent être affichés après chaque test, et les résultats des tests peuvent être retravaillés avec les exemples de fichiers de test spécifiés.
  
## <a name="testing-the-rest"></a>Test du reste

Le test «tester le reste» permet de valider les décisions de Culling, par exemple, pour examiner uniquement les fichiers situés au-dessus d'un score de pertinence spécifique basé sur les résultats avancés avancés de découverte électronique. L'expert examine un échantillon de fichiers sous un score de démarcation sélectionné pour évaluer le nombre de fichiers appropriés dans cet ensemble.
  
Ce test fournit des statistiques et une comparaison entre l'ensemble de révision et le test la population Rest. Les résultats du jeu de révision sont ceux calculés par pertinence lors de la formation. Les résultats incluent des calculs en fonction des paramètres et des paramètres d'entrée, tels que:
  
- Tester des statistiques sur le nombre de fichiers dans un exemple et identifier les fichiers appropriés. 
    
- Comparaison tabulaire des paramètres de population du jeu de révision et des autres, par exemple, le nombre de fichiers, le nombre estimé de fichiers pertinents, la richesse estimée et le coût moyen de la recherche d'un fichier supplémentaire pertinent. Les paramètres de coût des paramètres peuvent être définis par l'administrateur.
    
1. Ouvrez l' **onglet \> test de pertinence** . 
    
2. Dans l'onglet **test** , cliquez sur **nouveau test**. La boîte de dialogue **créer un test** s'affiche, comme illustré dans l'exemple suivant. 
    
    ![Résultats de pertinence du test Tester les éléments restants](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. Dans **nom du test**et **Description**, tapez le nom et la description.
    
4. Dans la liste **type de test** , sélectionnez **tester le reste**
    
5. Dans la liste **problème/catégorie** , sélectionnez le nom du problème. 
    
6. Dans la liste **charge** , sélectionnez la charge. 
    
7. En **lecture%**, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence de la limite. 
    
8. Dans **définir la taille**, ou acceptez la valeur par défaut. Notez que les icônes de restauration restaureront les valeurs par défaut.
    
9. Cliquez sur **Démarrer**le balisage. Un échantillon de test est généré.
    
10. Examinez et marquez chacun des fichiers dans l'onglet de la balise de **pertinence \> ** et, lorsque vous avez fini, cliquez sur **calculer**.
    
11. Sous l'onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests. Un exemple est illustré dans la figure suivante. 
    
    ![Résultats du test Tester les éléments restants](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
Dans la figure ci-dessus, la section **exemple de paramètres** du tableau contient des détails sur le nombre de fichiers dans l'exemple marqué par l'expert, ainsi que le nombre de fichiers pertinents trouvés dans cet exemple. 
  
La section **paramètres de remplissage** du tableau contient les résultats des tests, y compris le remplissage de l'ensemble des fichiers dont le score est inférieur à la limite sélectionnée et la population de fichiers Rest dont le score est supérieur à la limite sélectionnée. Pour chaque population, les résultats suivants s'affichent: 
  
- Inclut des fichiers dont la limite de lecture est% indiquée
    
- Nombre total de fichiers 
    
- Estimation du nombre de fichiers pertinents 
    
- La richesse estimée 
    
- Coût moyen de la recherche d'un autre fichier pertinent
    
## <a name="testing-the-slice"></a>Test du secteur

Le test «test the Slice» effectue un test semblable au test «test the Rest», mais à un segment de l'ensemble de fichiers, tel que spécifié par la pertinence% de lecture.
  
1. Ouvrez l' **onglet \> test de pertinence** . 
    
2. Dans l'onglet **test** , cliquez sur **nouveau test**. La boîte de dialogue **créer un test** s'affiche. 
    
3. Dans **nom** et **Description**du test, entrez les informations.
    
4. Dans la liste **type de test** , sélectionnez **tester la section**.
    
5. Dans la liste **problème** , sélectionnez le nom du problème. 
    
6. Dans la liste **charge** , sélectionnez la charge. 
    
7. En **lecture% entre**, acceptez les valeurs par défaut de plage basse et haute ou sélectionnez des valeurs pour les scores de pertinence de la limite. 
    
8. Dans **définir la taille**, sélectionnez une valeur ou acceptez la valeur par défaut.
    
    Les icônes de restauration restaureront la valeur par défaut.
    
9. Cliquez sur **Démarrer**le balisage. Un échantillon de test est généré.
    
10. Examinez et marquez chacun des fichiers dans l'onglet de la balise de **pertinence \> ** et, lorsque vous avez fini, cliquez sur **calculer**. 
    
11. Sous l'onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests. 
    
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de l'évaluation en matière de pertinence](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Balisage et évaluation](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Étiquetage et formation à la pertinence](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Analyse de la pertinence](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Choix en fonction des résultats](decision-based-on-the-results-in-advanced-ediscovery.md)

