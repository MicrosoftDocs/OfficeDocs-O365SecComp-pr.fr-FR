---
title: Définir les options d’analyse dans Office 365 avancée de découverte électronique
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Passez en revue les étapes pour configurer les options pour le processus d’analyse d’Office 365 avancée eDiscovery, y compris près de doublons, les threads de messagerie et des thèmes.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528093"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Définir les options d’analyse dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Dans Paramètres avancés eDiscovery, définissez les options d’analyse avant d’exécuter l’analyse.
  
## <a name="set-analyze-options"></a>Définir les options d’analyse

Open **préparer \> analyser** \> **le programme d’installation**. La fenêtre suivante s’affiche.
  
![Options Définir l’analyse](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **Près de doublons et les threads de messagerie** Cette case à cocher si vous souhaitez exécuter l’analyse. Il est sélectionné par défaut. 
  
 **Similarité de document** Entrez la valeur de seuil des doublons Near ou acceptez la valeur par défaut de 65 %. 
  
 **Thèmes** Cochez cette case pour traiter tous les fichiers et leur attribuer des thèmes. Par défaut, cette case à cocher n’est pas sélectionnée. Entrez les options suivantes si vous souhaitez effectuer des thèmes de traitement.
  
- **Nombre maximal de thèmes** Entrez ou sélectionnez une valeur pour le nombre de thèmes à créer. La valeur par défaut est 200. 
    
    > [!NOTE]
    > Augmentation du nombre de thèmes affecte les performances, ainsi que la capacité d’un thème pour généraliser. Plus le nombre de thèmes, le plus granulaires, ils se trouvent. Par exemple, si un ensemble de 50 thèmes include un thème tels que « Basketball, rapide, pince, Lakers » ; 300 thèmes peuvent inclure des thèmes distincts : « Incite », « TONDEUSE », « Lakers ». Si vous n’avez aucune prise de conscience du thème « Basketball » et que vous utilisez cette fonctionnalité pour ECA, voir le thème « Basketball » peut être utile. Mais, si le traitement a un trop grand nombre de thèmes, vous visualiserez jamais le mot « Basketball » et peut ne pas savez que rapide et tondeuse est bonnes thèmes Basketball pour passer en revue, au lieu d’articles qui passent sur démarre et utilisés pour cheveux. 
  
- **Thèmes suggérés** Vous pouvez proposer des mots de thème pour contrôler le traitement des thèmes. Découverte avancée sera se concentrer sur ces mots suggérés et essayez de créer un ou plusieurs thèmes pertinents, en fonction des paramètres « Max nombre de thèmes ». 
    
    Par exemple, si le mot suggéré est « computer », et vous avez spécifié « 2 » comme « nombre maximal de thèmes », eDiscovery avancée essaiera générer des thèmes de deux qui sont associées au mot « computer ». Les deux thèmes est « logiciel » et « matériel informatique », par exemple. 
    
    ![Ajouter une suggestion de thème](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. Pour afficher, ajouter ou modifier des thèmes suggérées, cliquez sur **Modifier**.
    
2. Dans le panneau de configuration **des thèmes suggérés** , cliquez sur **Ajouter**![icône Ajouter](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icône pour ajouter un thème. Dans le volet **Ajouter suggérée thème** , ajoutez les mots, séparés par des virgules. 
    
3. Dans **nombre de thèmes**, sélectionnez une valeur pour déterminer le nombre de thèmes eDiscovery avancée essaieront de générer ces termes (valeur par défaut est 1 thème).
    
4. Cliquez sur **Enregistrer** , puis fermez la boîte de dialogue. 
    
    > [!NOTE]
    > Le nombre total de thèmes inclut des thèmes suggéré. Les thèmes suggérés total ne peut pas dépasser les thèmes total. S’il existe de nombreux thèmes suggérée par rapport aux thèmes total, uniquement quelques thèmes de « nouveau » seront détectés par le système, car la plupart des thèmes sera consacrée aux thèmes suggéré. 
  
- **Mode** Dans la liste déroulante, sélectionnez une option de **thèmes** : 
    
  - **Créer et appliquer le modèle**: calcule des thèmes par les modèles d’un segment des fichiers et puis distribue les fichiers entre eux.
    
  - **Créer un modèle**: calcule un modèle de thèmes à partir d’un segment des fichiers. Le processus d’appliquer de la division de fichiers s’effectue séparément à un autre moment.
    
  - **Appliquer modèle**: cette option ne s’affiche que si un modèle a été créé précédemment et n’est pas encore appliqué. Il divise les fichiers selon les thèmes.
    
Vous pouvez également [définir ignorer le texte](set-ignore-text-in-advanced-ediscovery.md) et [définir Analyze paramètres avancé](set-analyze-advanced-settings-in-advanced-ediscovery.md) pour l’analyse. 
  
Une fois que vous avez défini ces options, cliquez sur **analyse** à exécuter. [Affichage analyser les résultats](view-analyze-results-in-advanced-ediscovery.md) sont affichés. 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Présentation de similarité de document](understand-document-similarity-in-advanced-ediscovery.md)
  
[Définir le texte de la case à cocher Ignorer](set-ignore-text-in-advanced-ediscovery.md)
  
[Paramètres avancés Définir l’analyse](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Afficher les résultats d’analyse](view-analyze-results-in-advanced-ediscovery.md)

