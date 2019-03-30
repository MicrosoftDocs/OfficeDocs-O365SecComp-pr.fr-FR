---
title: Utiliser l'analyse exPresse dans Office 365 Advanced eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Découvrez comment exécuter le mode d'analyse rapide d'Office 365 Advanced eDiscovery
ms.openlocfilehash: d8457587c9c1a1237ddc076ce803a46382a04ed8
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000957"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a>Utiliser l'analyse exPresse dans Office 365 Advanced eDiscovery

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Vous pouvez utiliser l' **analyse rapide** pour analyser rapidement un cas et exporter les résultats. 
  
Vous pouvez utiliser l'analyse rapide pour calculer des doublons et des fils de messagerie et calculer des thèmes. Vous pouvez également définir certains paramètres pour les thèmes, la similarité des documents et les fichiers d'exportation dans les [Paramètres avancés pour l'analyse rapide](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).
  
## <a name="run-express-analysis"></a>Exécuter l'analyse rapide

1. Dans l'onglet **analyse expresse** (1), sélectionnez un conteneur pour activer les boutons * * Express Analysis * * (2) et **Paramètres avancés** . 
    
    ![Capture d'écran de la page d'analyse exPresse](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. Sous **analyser les paramètres**:
    
  - Pour exécuter l'analyse, cochez la case **calculer les doublons et les fils de messagerie** . Elle est sélectionnée par défaut. 
    
  - Cochez **calculer les thèmes** pour traiter tous les fichiers et leur affecter des thèmes. Elle est sélectionnée par défaut. 
    
3. Sous **destination**de l'exportation:
    
  - Cochez la case **Télécharger sur** l'ordinateur local pour télécharger sur votre ordinateur local. 
    
  - Si vous activez l'option **exportation vers l'objet BLOB Azure défini par l'utilisateur** , vous pouvez également spécifier une URL de conteneur et un jeton SAS. 
    
    > [!NOTE]
    > Une fois qu'un package d'exportation est stocké dans l'objet BLOB Azure défini par l'utilisateur, les données ne sont plus gérées par Advanced eDiscovery. Il est géré par l'objet BLOB Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur le BLOB Azure. 
  
  - **Enregistrer le jeton SAS pour une session d'exportation future**: si cette option est activée, le jeton SAS est chiffré dans la base de données interne avancée eDiscovery pour une utilisation ultérieure.
    
    > [!NOTE]
    > Actuellement, le jeton SAS expire au bout d'un mois. Si vous essayez d'effectuer un téléchargement après plus d'un mois, vous devez annuler la dernière session, puis effectuer une nouvelle exportation. 
  
4. Pour démarrer l'analyse rapide avec les paramètres par défaut, choisissez **analyse rapide**, et la page État de la **tâche** s'affiche. 
    
    Sur la **page État** de la tâche, vous pouvez développer les onglets **processus**, **analyser** et **Exporter** pour afficher les détails relatifs à l'exécution rapide. 
    
    ![Capture d'écran de la page d'état de la tâche d'analyse avancée eDiscovery Express](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. Choisissez la page Résumé de l' **analyse rapide** pour répertorier des informations détaillées sur l'exécution. 
    
    Dans la partie inférieure de la page Résumé de l' **analyse Express** , choisissez **Télécharger la dernière session** pour télécharger les fichiers d'analyse TP votre ordinateur local. Vous devez tout d'abord télécharger l'outil d'exportation eDiscovery et coller la clé d'exportation dans l'outil d'exportation de découverte électronique. 
    
## <a name="advanced-settings-for-express-analysis"></a>Paramètres avancés pour l'analyse rapide
<a name="BK_AdvancedSettings"> </a>

Vous pouvez éventuellement définir des **Paramètres avancés** pour modifier les paramètres d'analyse expresse par défaut. 
  
1. Dans la section **Analyze (analyser** ): 
    
  - Dans les **liens proches des doublons et des fils de messagerie**, entrez la valeur **similarité des documents** ou acceptez la valeur par défaut de 65%. 
    
  - Dans le champ **nombre maximal de thèmes** , entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200. 
    
    > [!NOTE]
    > L'augmentation du nombre de thèmes a une incidence sur les performances, ainsi que sur la capacité d'un thème à généraliser. Plus le nombre de thèmes est élevé, plus il est granulaire. Par exemple, si un jeu de thèmes 50 inclut un thème tel que «basket-ball, Spurs, déToureurs, Lakers»; 300 les thèmes peuvent inclure des thèmes distincts: «Spurs», «Clipper», «Lakers». Si vous n'avez pas conscience du thème «basket» et si vous utilisez cette fonctionnalité pour ECA, voir le thème «basket» peut être utile. Toutefois, si le traitement avait trop de thèmes, il se peut que vous ne trouviez jamais le mot «basket-ball» et que des Spurs et des déCoupages soient des thèmes de basket-ball intéressants à consulter, plutôt que des éléments qui se trouvent sur les bottes et utilisés pour les cheveux. 
  
  - Dans les **thèmes suggérés** , choisissez **modifier** pour suggérer des mots de thème pour contrôler le traitement des thèmes. Advanced eDiscovery se concentrera sur ces suggestions de mots et tentera de créer un ou plusieurs thèmes pertinents, en fonction des paramètres «nombre maximal de thèmes». 
    
    Par exemple, si le mot suggéré est «ordinateur» et que vous avez spécifié «2» comme «nombre maximal de thèmes», Advanced eDiscovery essaiera de générer deux thèmes liés au mot «ordinateur». Les deux thèmes peuvent être «logiciels informatiques» et «matériel informatique», par exemple.
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - **Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** : 
    
  - **Créer et appliquer un modèle**: calcule les thèmes par modèles à partir d'un segment des fichiers, puis distribue les fichiers entre eux.
    
  - **Créer un modèle**: calcule un modèle de thèmes à partir d'un segment des fichiers. Le processus d'application de la Division des fichiers est réalisé séparément à un autre moment.
    
  - **Appliquer le modèle**: cette option n'est visible que si un modèle a été créé précédemment et n'a pas encore été appliqué. Cela permet de diviser les fichiers en fonction des thèmes.
    
2. Dans la section **Exporter** : 
    
1. Dans le **lot sélectionner l'exportation**:
    
  - Dans la liste **Exporter le lot** , sélectionnez le nom du lot ou exportez les résultats vers l'export lot 01 (par défaut). 
    
  - Pour exporter les résultats pour les nouveaux fichiers que vous avez ajoutés à un cas existant, continuez avec votre lot actuel. Pour créer une session dans le lot, sélectionnez le même numéro de lot, puis cliquez sur **créer une session d'exportation** vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle. 
    
  - Pour exporter vers un nouveau lot, cliquez sur **Ajouter** ![une](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icône Ajouter et entrez un nouveau nom dans le **champ nom du lot** (ou acceptez la valeur par défaut) et une description dans **Description du lot**. Cliquez sur **OK**.
    
  - Pour modifier un nom de lot ou une description, sélectionnez le nom dans **Exporter le lot**, cliquez](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)sur **modifier** ![l'icône d'édition, puis modifiez les champs.
    
    > [!NOTE]
    > Une fois que vous avez exécuté des sessions pour un lot d'exportation, il est impossible de les supprimer. De plus, seuls certains paramètres peuvent être modifiés une fois la première session exécutée. 
  
  - Pour créer un lot d'exportation en double, sélectionnez dupliquer un **lot** ![d'exportation en](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) double créez un lot d'exportation en double et entrez un nom et une description pour le lot dupliqué dans le panneau. 
    
  - Pour supprimer un lot d'exportation, sélectionnez **supprimer** ![supprimer une icône](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)exporter un lot.
    
  - Pour afficher l'historique d'un lot, sélectionnez **** ![l'icône](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)historique du lot-afficher l'historique.
    
2. Sous define p **opulation:** sélectionnez **inclure uniquement les fichiers au-dessus du score** de découpage de pertinence et/ou affiner l' **exportation** pour affiner les paramètres de votre lot d'exportation. Si vous sélectionnez **inclure uniquement les fichiers au-dessus du score**de découpAge de pertinence, si le **problème** est activé et si le score de pertinence du fichier est supérieur au score de découpage du problème sélectionné, le fichier est exporté. Le fichier est exporté sauf s'il est exclu par le filtre « **pour révision** ». Si vous sélectionnez **affiner l'exportation**, les cases d'option **de déDuplication** et de **filtrage par «pour révision»** sont activées. Si vous choisissez **** la déduplication, les fichiers dupliqués sont filtrés en fonction de la stratégie définie: [level case (Default): à partir de chaque ensemble de fichiers en double dans le cas entier, tous les fichiers sauf un seront de duped. Niveau des dépositaires: à partir de chaque ensemble de fichiers en double du même dépositaire, tous les fichiers sauf un seront de duped. Un enregistrement de tous les fichiers en double est disponible lors de l'exportation de la sortie. Si vous choisissez **Filtrer par champ de révision** , sélectionnez **modifier sous métadonnées** pour entrer les paramètres de champ **«pour révision»**. Sélectionnez **inclure les fichiers d'entrée**pour inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver cette option pour accélérer le processus d'exportation. Notez que les fichiers natifs seront exportés dans tous les cas.
    
3. Sous **définir**les métadonnées, sélectionnez l'une des options suivantes dans la liste **Exporter le modèle** (une fois par session). 
    
  - **Standard**: ensemble de base des éléments de données, des métadonnées et des propriétés. Utilisez cette option lorsque les données d'importation ont déjà été traitées dans Advanced eDiscovery et que les données d'exportation sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d'exportation sont créées et remplies.
    
  - **All**: ensemble complet de métadonnées standard incluant toutes les données de traitement, ainsi que les scores d'analyse et de pertinence. Ce modèle est requis lorsque Advanced eDiscovery effectue le traitement et que les données de fichier sont téléchargées sur un système externe pour la première fois.
    
  - **Problèmes**: sélectionnez **tous les problèmes** ou sélectionnez un problème particulier que vous avez créé. 
    
Choisissez **OK**pour enregistrer les paramètres avancés, **restaurer** les paramètres par défaut pour utiliser les valeurs par défaut ou **Annuler** pour annuler la définition des paramètres avancés. 
  
## <a name="see-also"></a>Voir aussi
<a name="BK_AdvancedSettings"> </a>

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)

