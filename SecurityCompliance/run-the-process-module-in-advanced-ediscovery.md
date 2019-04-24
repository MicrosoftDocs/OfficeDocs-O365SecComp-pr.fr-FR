---
title: Exécuter le module de processus dans Office 365 Advanced eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Découvrez les instructions relatives à la préparation des fichiers de cas des données Office 365 pour analyse avec Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261032"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a>Exécuter le module de processus dans Office 365 Advanced eDiscovery

Les fichiers case sont chargés dans la découverte électronique avancée lors de la **préparation** \> ****. 
  
> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a>Recommandations: préparation des données pour Advanced eDiscovery

- **Qualité**: Identifiez clairement la population de fichiers de cas pertinente pour le cas.
    
- **Charge**: charge les fichiers dans un emplacement accessible à la découverte électronique avancée.
    
- **ID de fichier**: identificateur de fichier unique dans Advanced eDiscovery. Si aucun identificateur de fichier n'est importé, Advanced eDiscovery génère automatiquement l'ID. Si vous mappez l'ID dans une charge de processus ultérieure et que vous mappez un chemin d'accès différent de celui de la charge de processus initiale, Advanced eDiscovery remplace le chemin d'accès (au lieu d'ajouter une nouvelle entrée de fichier). L'ID peut être utilisé comme référence dans le processus d'exportation. La valeur ID ne doit pas être «-1».
    
- **MD5**: cette signature est utilisée pour différencier les fichiers (deux fichiers ne sont pas considérés comme des doublons exactes, sauf s'ils ont le même MD5). Par défaut, Advanced eDiscovery calcule le MD5 des fichiers. Lorsque les fichiers chargés sont des fichiers texte, il est recommandé de charger et de mapper la valeur MD5 d'origine au lieu de la calculer dans Advanced eDiscovery.
    
- **Nom et type de fichier**:
    
  - Advanced eDiscovery peut traiter des fichiers de différents formats et extraire les fichiers natifs chargés dans un format standard \*, comme. TXT, HTML ou. Langage. Le traitement des fichiers texte est plus rapide que les fichiers natifs. Les fichiers texte extraits sont stockés dans le dossier case.
    
  - Ne chargez pas les fichiers qui ne peuvent pas être extraits, tels que les fichiers système ou les images graphiques. Ces fichiers peuvent retarder le traitement.
    
  - Vérifiez que les noms de fichiers sont beaucoup nommés et que les chemins d'accès sont corrects.
    
- **Chemin d'accès de fichier**: Advanced eDiscovery peut charger des fichiers avec des longueurs de chemin d'accès allant jusqu'à 400 caractères.
    
- **Extraction de texte**: lors de l'extraction de texte à partir de fichiers natifs, en plus du texte normal, les éléments suivants sont également extraits: texte masqué (Excel et. doc), colonnes masquées (Excel), suivi des modifications (. doc), notes du présentateur (. ppt), objets incorporés (par exemple, Objets Excel dans un. ppt). Ces éléments peuvent être affichés dans l'éditeur de texte.
    
- **Ignorer le texte**: cette fonctionnalité facultative est définie après l'exécution du processus et avant l'analyse. Ignorer le texte doit être utilisé avec précaution car son utilisation peut réduire les performances de l'analyse des fichiers.
    
- **Texte multilingue**: Advanced eDiscovery ne gère actuellement pas les noms multilingues pour les balises, les dépositaires et les problèmes.
    
- **Métadonnées**: Déterminez s'il existe des métadonnées que vous souhaitez enregistrer dans la base de données de cas pour référence ultérieure, comme la plage de dates, la taille de fichier, le type de fichier, le dépositaire et l'objet. Les métadonnées peuvent être chargées après que les fichiers ont déjà été chargés sans réexécuter l'inventaire ou ajouter une charge de retraitement. 
    
  - Si les fichiers ont été chargés par chemin d'accès, mappez la colonne chemin d'accès lors de l'importation des métadonnées. Il est possible de faire référence au fichier par son ID et de mapper un autre chemin d'accès. Il s'agit d'un scénario utile lorsque les chemins d'accès de fichiers changent.
    
  - Si les fichiers ont été initialement chargés par ID de fichier, mappez la colonne ID lors du chargement des métadonnées. Faire référence au fichier par chemin d'accès (au lieu d'ID) entraîne le chargement des fichiers avec un ID différent. Advanced eDiscovery crée des copies des fichiers au lieu de charger les métadonnées des fichiers existants.
    
- **Familles**: il n'est pas possible de charger une famille sans son parent (en-tête de famille). 
    
- **Taille du fichier**: il n'existe aucune limite quant à la taille des fichiers chargés vers Advanced eDiscovery. Pour l'analyse (analyse, pertinence, etc.), la limite est de 5 242 880 caractères du texte extrait. Les fichiers plus volumineux sont ignorés (par exemple, à des fins de pertinence, les fichiers ne participent pas au processus d'apprentissage de pertinence et ne reçoivent pas de score de pertinence après le calcul par lot).
    
- **Quantité de fichiers**: il n'y a pas de limite recommandée quant au nombre de fichiers qui peuvent être gérés dans un seul cas. Les performances dépendent des ressources de votre système. 
    
## <a name="filtering-files"></a>Filtrage des fichiers

Une étiquette définie par l'utilisateur peut être associée à un ensemble de fichiers pour les exclure du processus ou d'autres tâches. Chaque session de processus est associée à un ID de lot. Bien que l'ID de lot ne soit pas visible par l'expert en matière de pertinence, vous pouvez le faire à l'aide d'un utilitaire de recherche en ajoutant un filtre pour le lot actuel et en marquant tous les fichiers appropriés avec une étiquette définie par l'utilisateur. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Exécution du module de processus et chargement des données](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[Affichage des résultats de module de processus](view-process-module-results-in-advanced-ediscovery.md)

