---
title: Exécuter le module de processus et charger des données dans Office 365 avancée de découverte électronique
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Découvrez comment utiliser le Office 365 Security &amp; centre de conformité pour accéder à Office 365 avancée de découverte électronique et exécuter le module de processus pour un cas.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528113"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Exécuter le module de processus et charger des données dans Office 365 avancée de découverte électronique

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Cette section décrit les fonctionnalités du module processus eDiscovery avancées. 
  
En plus des données de fichiers, des métadonnées telles que le type de fichier, extension, emplacement ou chemin d’accès, date de création et heure, auteur, dépositaire et subject, peuvent être chargée dans avancée eDiscovery et enregistré pour chaque cas. Certaines métadonnées sont calculée en découverte avancée, par exemple, lors du chargement de fichiers natifs. 
  
Découverte avancée fournit système des valeurs de métadonnées, telles que les regroupements en double ou les résultats de la pertinence. Autres métadonnées, telles que des annotations de fichier, peuvent être ajoutée par l’administrateur. 
  
## <a name="running-process"></a>Processus en cours d’exécution

> [!NOTE]
> Numéros de lot sont affectés à un fichier au cours du processus permettant d’assurer le suivi des fichiers. Le numéro de lot permet également d’identification de traitement par lots d’options retraitement. Filtres supplémentaires sont disponibles pour le filtrage des sessions et le numéro de lot. 
  
Effectuez les étapes suivantes pour exécuter la procédure.
  
1. [Ouvrir la sécurité Office 365 &amp; centre de conformité](go-to-the-securitycompliance-center.md) . 
    
2. Accédez à **recherche &amp; enquête** \> **eDiscovery** , puis cliquez sur **Aller à la découverte électronique avancée**.
    
3. Découverte électronique avancée, sélectionnez le cas échéant dans la page en **cas** et cliquez sur **Atteindre la casse**.
    
4. Dans **Prepare** \> **processus** \> **le programme d’installation**, sélectionnez un conteneur de la liste des conteneurs disponibles.
    
    ![Cliquez sur le processus pour ajouter les résultats de recherche à la casse](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. Si vous souhaitez ajouter le conteneur en tant que fichiers de départ ou en tant que fichiers balisés préalable, cliquez sur **paramètres... avancés** . 
    
    Utiliser les fichiers d’amorçage pour accélérer la formation pour les problèmes avec la plus grande richesse faible (généralement 2 % ou moins). Pour les fichiers d’amorçage, il est recommandé que vous sélectionnez plusieurs fichiers inclut-elle pertinents et traiter sur 20 et 50 graines par problème (trop de fichiers d’amorçage pouvant incliner les résultats de la pertinence). Fichiers d’amorçage doivent être examinées par la personne qui sera former le problème.
    
    Fichiers balisés préalable permet d’automatiser la formation de pertinence. Vous devez ajouter une balise au moins 1 500 fichiers et conserver la proportion d’aux fichiers non pertinents identique à celle de la collection à ajouter à la pertinence. Ces fichiers doivent être marqués manuellement, et vous devez être assuré de la qualité de la liaison de.
    
    ![Capture d’écran d’avancée de page de paramètres de traitement par lot les fichiers](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - Dans la section **valeur de départ** : 
    
    Choisissez **Marquer en tant que fichiers d’amorçage** pour marquer le conteneur en tant que fichiers d’amorçage. Vous devez également affecter par un problème dans la **problème** liste déroulante. À partir de la **balise de** liste déroulante, choisissez **pertinent** ou **non pertinents** . 
    
    > [!NOTE]
    > Une fois que vous définissez des fichiers en tant que **valeur de départ**, vous ne peut pas les marquer comme **préalable avec balise**. 
  
  - Dans la section **fichiers balisés préalable** : 
    
    Choisissez **Marquer en tant que fichiers préalable avec balise** pour marquer le conteneur en tant que fichiers préalable avec balise. Vous devez également affecter par un problème dans la **problème** liste déroulante. À partir de la **balise de** liste déroulante, choisissez **pertinent** ou **non pertinents** . 
    
    > [!NOTE]
    > Une fois que vous définissez fichiers **préalable avec balise**, vous ne peut pas les marquer comme **valeur de départ**. 
  
  - Dans la section **Marquer le courrier électronique** . ensemble de quelle partie d’un message électronique traité doivent être marquées comme semences ou préalable avec balise. 
    
6. Pour commencer, cliquez sur **le processus**. Une fois terminé, les résultats de processus sont affichés.
    
7. (Facultatif) Si vous avez besoin affecter des sources de données à un dépositaire spécifique, vous pouvez ajouter ou modifier les noms de dépositaire dans **dépositaires** \> dépositaires **Gérer** et attribuer dans **dépositaires** \> **affecter**. 
    
Si vous ajoutez à la casse, vous pouvez traiter à nouveau.
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Affichage des résultats de module de processus](view-process-module-results-in-advanced-ediscovery.md)

