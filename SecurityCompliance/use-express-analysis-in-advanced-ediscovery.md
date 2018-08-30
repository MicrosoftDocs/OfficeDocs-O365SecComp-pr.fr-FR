---
title: Utiliser l’analyse Express dans Office 365 avancée de découverte électronique
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Découvrez comment exécuter le mode d’analyse Express d’eDiscovery Office 365 avancée
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527966"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a>Utiliser l’analyse Express dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Vous pouvez utiliser **Express analyse** pour analyser rapidement un cas et exporter les résultats. 
  
Vous pouvez utiliser une analyse rapide pour calculer la proximité des doublons et les threads de messagerie et calculer des thèmes. Vous pouvez également définir certains paramètres de similarité de documents, des thèmes et des fichiers d’exportation dans les [Paramètres avancés pour l’analyse Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).
  
## <a name="run-express-analysis"></a>Exécuter l’analyse Express

1. Dans l’onglet **analyse Express** (1), sélectionnez un conteneur pour activer la ** Express analyse ** (2) et les boutons **Paramètres avancés** . 
    
    ![Capture d’écran de la page analyse Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. Sous l’onglet **paramètres d’analyse**:
    
  - Vérifiez **calculer la proximité des doublons et threads de messagerie** si vous souhaitez exécuter l’analyse. Il est sélectionné par défaut. 
    
  - Vérifiez les **Thèmes calculer** pour traiter tous les fichiers et leur attribuer des thèmes. Il est sélectionné par défaut. 
    
3. Sous **destination d’exportation**:
    
  - Vérifiez le **télécharger sur l’ordinateur local** à télécharger sur votre ordinateur local. 
    
  - Si vous l’activez **Exporter vers définies par l’utilisateur de blob Azure** vous pouvez également spécifier un jeton d’URL et les associations de conteneur. 
    
    > [!NOTE]
    > Une fois qu’un package d’exportation est stocké dans blob Azure définis par l’utilisateur, les données ne sont plus gérées par eDiscovery avancée. Il est géré par l’objet blob Azure. Cela signifie que si vous supprimez le cas, les fichiers exportés resteront toujours sur l’objet blob Azure. 
  
  - **Jeton de session exportation futurs SAS enregistrer**: s’il est activé, le jeton SAS sera chiffré dans la base de données interne de découverte électronique avancées pour une utilisation future.
    
    > [!NOTE]
    > Actuellement, le jeton SAS expire après un mois. Si vous essayez de télécharger après plus d’un mois, que vous devez annuler la dernière session, puis l’exporter à nouveau. 
  
4. Pour démarrer l’analyse express avec par défaut les paramètres, choisissez **Express analyse**et affiche la page **état de la tâche** 
    
    Dans la page **état de la tâche** , vous pouvez développer les **processus**, **analyser** et **exporter des** onglets pour afficher plus d’informations sur l’exécution expresse. 
    
    ![Capture d’écran d’avancée eDiscovery Express analyse tâche page d’état](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. Sélectionnez la page **Résumé de l’analyse de Express** pour répertorier des informations détaillées sur l’exécution. 
    
    Au bas de la page **Résumé de l’analyse de Express** , sélectionnez **Télécharger la dernière session** pour télécharger le tp de fichiers analyse votre ordinateur local. Vous devez tout d’abord télécharger l’outil d’exportation eDiscovery et collez la clé d’exportation à l’outil d’exportation de découverte électronique. 
    
## <a name="advanced-settings-for-express-analysis"></a>Paramètres avancés pour l’analyse Express
<a name="BK_AdvancedSettings"> </a>

Vous pouvez également définir des **Paramètres avancés** pour modifier les paramètres d’analyse par défaut Express. 
  
1. Dans la section **analyse** : 
    
  - Dans la **proximité des doublons et threads de messagerie**, entrez la valeur de **similarité de Document** , ou acceptez la valeur par défaut de 65 %. 
    
  - Le **nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200. 
    
    > [!NOTE]
    > Augmentation du nombre de thèmes affecte les performances, ainsi que la capacité d’un thème pour généraliser. Plus le nombre de thèmes, le plus granulaires, ils se trouvent. Par exemple, si un ensemble de 50 thèmes include un thème tels que « Basketball, rapide, pince, Lakers » ; 300 thèmes peuvent inclure des thèmes distincts : « Incite », « TONDEUSE », « Lakers ». Si vous n’avez aucune prise de conscience du thème « Basketball » et que vous utilisez cette fonctionnalité pour ECA, voir le thème « Basketball » peut être utile. Mais, si le traitement a un trop grand nombre de thèmes, vous visualiserez jamais le mot « Basketball » et peut ne pas savez que rapide et tondeuse est bonnes thèmes Basketball pour passer en revue, au lieu d’articles qui passent sur démarre et utilisés pour cheveux. 
  
  - Dans les **thèmes suggérés** choisissez **Modifier** pour nous transmettre vos suggestions de mots de thème pour contrôler le traitement des thèmes. Découverte avancée sera se concentrer sur ces mots suggérés et essayez de créer un ou plusieurs thèmes pertinents, en fonction des paramètres « Max nombre de thèmes ». 
    
    Par exemple, si le mot suggéré est « computer », et vous avez spécifié « 2 » comme « nombre maximal de thèmes », eDiscovery avancée essaiera générer des thèmes de deux qui sont associées au mot « computer ». Les deux thèmes est « logiciel » et « matériel informatique », par exemple.
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - **Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** : 
    
  - **Créer et appliquer le modèle**: calcule des thèmes par les modèles d’un segment des fichiers et puis distribue les fichiers entre eux.
    
  - **Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers. Le processus d’appliquer de la division de fichiers s’effectue séparément à un autre moment.
    
  - **Appliquer modèle**: cette option ne s’affiche que si un modèle a été créé précédemment et n’est pas encore appliqué. Il divise les fichiers selon les thèmes.
    
2. Dans la section **Exporter** : 
    
1. Dans le **lot sélectionnez Exporter**:
    
  - Dans la liste **Exporter le lot** , sélectionnez le nom ou exporter les résultats dans un lot d’exportation 01, (la feuille par défaut). 
    
  - Pour exporter les résultats pour les nouveaux fichiers ajoutés à un cas existant, continuez avec votre lot en cours. Pour créer une session dans le lot, sélectionnez le même numéro de traitement par lots et cliquez sur **créer exporter la session** , vous pouvez utiliser cette option pour exporter les mêmes paramètres que le lot précédent, de manière incrémentielle. 
    
  - Pour exporter vers un nouveau lot, cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) et entrez un nouveau nom dans **nom de la feuille** (ou acceptez celui par défaut) et une description dans la **description de lot**. Cliquez sur **OK**.
    
  - Pour modifier un nom ou une description, sélectionnez le nom de **l’exportation de lot**, cliquez sur **Modifier** ![icône Modifier](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), puis modifiez les champs.
    
    > [!NOTE]
    > Après avoir exécuté les sessions pour un lot d’exportation, ils ne peuvent pas être supprimés. En outre, les seuls certains paramètres peuvent être modifiés une fois que la première session est exécutée. 
  
  - Pour créer un lot d’exportation en double, choisissez le **lot d’exportation en double**![créer une icône de lot d’exportation en double](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) et entrez un nom et une description pour le lot en double dans le panneau de configuration. 
    
  - Pour supprimer un lot d’exportation, cliquez sur **Supprimer**![supprimer une icône d’exportation de lot](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
  - Pour afficher l’historique d’un lot, cliquez sur **historique de lot**![icône historique d’affichage](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Sous Définir p **opulation :** sélectionnez **inclure uniquement les fichiers au-dessus note coupure** et/ou de **lot d’exportation affiner** si vous souhaitez ajuster les paramètres de votre lot d’exportation. Si vous sélectionnez **inclure uniquement les fichiers au-dessus note coupure**, le **problème** est activée, et si le score de pertinence du fichier est supérieure au score de limite pour le problème sélectionné, le fichier est exporté. Le fichier doit être exporté, sauf si elle est exclu par le ' filtre **pour révision** . Si vous sélectionnez **lot d’exportation affiner**, la **déduplication** et **Filter by « Pour passer en revue les » champ** cases d’option sont activées. Si vous choisissez **la déduplication**, puis fichiers doublons seront être filtrées mise en fonction de la stratégie définie : [cas niveau (valeur par défaut) : à partir de chaque ensemble de fichiers en double dans le cas d’entier, un seul fichier sera déduplication duped. Niveau dépositaire : à partir de chaque ensemble de fichiers en double de la même dépositaire, un seul fichier sera duped retrait. Un enregistrement de tous les fichiers en double est disponible dans la sortie de l’exportation. Si vous choisissez champ **Filter by « pour passer en revue les'** , sélectionnez **Modifier sous métadonnées** pour entrer vos paramètres de champ **« pour révision »**. Sélectionnez **inclure les fichiers d’entrée**à inclure les fichiers sources dans le contenu du package. Vous pouvez désactiver cette option pour accélérer le processus d’exportation. Notez que les fichiers natifs seront exportés dans tous les cas.
    
3. Sous **définir métadonnées**, sélectionnez parmi les options suivantes dans la liste **Exporter le modèle** (une seule fois par session). 
    
  - **Standard**: ensemble de base des éléments de données, les métadonnées et les propriétés. Utilisez cette option lorsque importer des données a déjà été traitées dans découverte avancée et d’exporter des données sont téléchargées vers un système qui contient déjà les fichiers. Par défaut, les colonnes de modèle d’exportation sont créés et remplis.
    
  - **Tous les**: ensemble de toutes les données de traitement, ainsi que les scores d’analyser et de la pertinence de métadonnées standard. Ce modèle est requis lors de la découverte électronique avancée effectue le traitement et des données de fichier sont téléchargées vers un système externe pour la première fois.
    
  - **Problèmes**: sélectionnez **Tous les problèmes** ou un problème spécifique que vous avez créé. 
    
Cliquez sur **OK**pour enregistrer les paramètres avancés, **restauration par défaut** à utiliser les valeurs par défaut, ou **Annuler** pour annuler la configuration des paramètres avancés. 
  
## <a name="see-also"></a>Voir aussi
<a name="BK_AdvancedSettings"> </a>

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)

