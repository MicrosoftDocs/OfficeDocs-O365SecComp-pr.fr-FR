---
title: Définir les options d’analyse dans Office 365 Advanced eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Passez en revue les étapes de configuration des options pour le processus Analyze dans Office 365 Advanced eDiscovery, y compris les thèmes de quasi-duplication, les threads de messagerie et les thèmes.  '
ms.openlocfilehash: 6d853d701613fcbe61c6e98b3bf55ae99eefd901
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156666"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Définir les options d’analyse dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Advanced eDiscovery, définissez les options d’analyse avant d’exécuter Analyze.
  
## <a name="set-analyze-options"></a>Définir les options d’analyse

Ouvrez **Prepare prepare \> prepare** **** \> Setup. La fenêtre suivante s’affiche.
  
![Options Définir l’analyse](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **Quasi-doublons et threads de messagerie** Activez cette case à cocher si vous souhaitez exécuter l’analyse. Elle est sélectionnée par défaut. 
  
 **Similarité des documents** Entrez la valeur de seuil des quasi-doublons ou acceptez la valeur par défaut de 65%. 
  
 **Thèmes** Activez cette case à cocher pour traiter tous les fichiers et leur affecter des thèmes. Par défaut, cette case à cocher n’est pas activée. Entrez les options suivantes si vous souhaitez effectuer le traitement des thèmes.
  
- **Nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200. 
    
    > [!NOTE]
    > L’augmentation du nombre de thèmes a une incidence sur les performances, ainsi que sur la capacité d’un thème à généraliser. Plus le nombre de thèmes est élevé, plus il est granulaire. Par exemple, si un jeu de thèmes 50 inclut un thème tel que «basket-ball, Spurs, détoureurs, Lakers»; 300 les thèmes peuvent inclure des thèmes distincts: «Spurs», «Clipper», «Lakers». Si vous n’avez pas conscience du thème «basket» et si vous utilisez cette fonctionnalité pour ECA, voir le thème «basket» peut être utile. Toutefois, si le traitement avait trop de thèmes, il se peut que vous ne trouviez jamais le mot «basket-ball» et que des Spurs et des découpages soient des thèmes de basket-ball intéressants à consulter, plutôt que des éléments qui se trouvent sur les bottes et utilisés pour les cheveux. 
  
- **Thèmes suggérés** Vous pouvez suggérer des mots de thème pour contrôler le traitement des thèmes. Advanced eDiscovery se concentrera sur ces suggestions de mots et tentera de créer un ou plusieurs thèmes pertinents, en fonction des paramètres «nombre maximal de thèmes». 
    
    Par exemple, si le mot suggéré est «ordinateur» et que vous avez spécifié «2» comme «nombre maximal de thèmes», Advanced eDiscovery essaiera de générer deux thèmes liés au mot «ordinateur». Les deux thèmes peuvent être «logiciels informatiques» et «matériel informatique», par exemple. 
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. Pour afficher, ajouter ou modifier des thèmes suggérés, cliquez sur **modifier**.
    
2. Dans le panneau **thèmes suggérés** , cliquez sur l’icône](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) **Ajouter** ![une icône Ajouter pour ajouter un thème. Dans le panneau **Ajouter un thème suggéré** , ajoutez les mots, séparés par des virgules. 
    
3. Dans **nombre de thèmes**, sélectionnez une valeur pour déterminer le nombre de thèmes que la fonctionnalité eDiscovery avancée essaiera de générer pour ces mots (la valeur par défaut est 1 thème).
    
4. Cliquez sur **Enregistrer** , puis fermez la boîte de dialogue. 
    
    > [!NOTE]
    > Le nombre total de thèmes inclut les thèmes suggérés. Le total des thèmes suggérés ne peut pas dépasser le nombre total de thèmes. S’il existe de nombreux thèmes suggérés par rapport au nombre total de thèmes, seuls quelques «nouveaux» thèmes seront détectés par le système, car la plupart des thèmes seront dédiés aux thèmes suggérés. 
  
- **Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** : 
    
  - **Créer et appliquer un modèle**: calcule les thèmes par modèles à partir d’un segment des fichiers, puis distribue les fichiers entre eux.
    
  - **Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers. Le processus d’application de la Division des fichiers est réalisé séparément à un autre moment.
    
  - **Appliquer le modèle**: cette option n’est visible que si un modèle a été créé précédemment et n’a pas encore été appliqué. Cela permet de diviser les fichiers en fonction des thèmes.
    
Vous pouvez également [définir ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) et [définir les paramètres avancés](set-analyze-advanced-settings-in-advanced-ediscovery.md) d’analyse pour l’analyse. 
  
Après avoir défini ces options, cliquez sur **analyser** pour exécuter. [Afficher les résultats](view-analyze-results-in-advanced-ediscovery.md) de l’analyse sont affichés. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Présentation de la similarité des documents](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définir le texte ignoré](set-ignore-text-in-advanced-ediscovery.md)
  
[Paramètres avancés Définir l’analyse](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Afficher les résultats de l’analyse](view-analyze-results-in-advanced-ediscovery.md)

