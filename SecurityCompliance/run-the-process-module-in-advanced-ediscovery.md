---
title: Exécuter le module de processus d’eDiscovery Office 365 avancée
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Découvrez les instructions pour la préparation des fichiers cas de données Office 365 pour l’analyse avec Office 365 avancée de découverte électronique.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528653"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a>Exécuter le module de processus d’eDiscovery Office 365 avancée

Dossiers sont chargés dans la découverte électronique avancée lors de la **préparation** \> **processus**. 
  
> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a>Conseils : Préparation des données pour la découverte avancée

- **Qualité**: clairement identifier la population dossier pertinente à la casse.
    
- **Charges**: charger les fichiers dans un emplacement accessible à la découverte électronique avancée.
    
- **ID du fichier**: un identificateur de fichier unique d’eDiscovery avancée. Si aucun identificateur de fichier n’est importé, eDiscovery avancé génère automatiquement l’ID. Si vous mappez l’ID une charge de processus suivante et mappez un chemin d’accès autre que de la charge de travail initial, eDiscovery avancée sera remplacer le chemin d’accès (plutôt qu’ajouter une nouvelle entrée de fichier). L’ID peut être utilisé comme une référence dans le processus d’exportation. La valeur d’ID ne doit pas être « -1 ».
    
- **MD5**: cette signature est utilisée pour différencier les fichiers (deux fichiers sont considérées comme identiques, sauf si elles ont le même MD5). Par défaut, eDiscovery avancée calcule MD5 des fichiers. Lorsque les fichiers chargés sont des fichiers texte, il est recommandé pour charger et mapper la valeur MD5 d’origine plutôt que le calcul d’eDiscovery avancée.
    
- **Nom et type de fichier**:
    
  - Découverte avancée peut traiter les fichiers de différents formats et extraire les fichiers natifs chargés dans un format standard, telles que \*. TXT, HTML ou. XML. le traitement des fichiers texte est plus rapide que les fichiers natifs. Texte extrait les fichiers sont stockés dans le dossier de cas.
    
  - Ne pas charger les fichiers qui ne peuvent pas être extraites, telles que les fichiers système ou les images graphiques. Ces fichiers peuvent différer le traitement.
    
  - Vérifiez que les noms de fichiers sont considérablement nommés et des chemins d’accès sont corrects.
    
- **Chemin d’accès du fichier**: découverte avancée peut charger des fichiers avec des longueurs de chemin d’accès jusqu'à 400 caractères.
    
- **Extraction de texte**: lors de l’extraction de texte à partir des fichiers natives, en plus du texte normal, les éléments suivants sont également extraits : colonnes de texte masqué (Excel et .doc), masqué (Excel), le suivi des modifications (.doc), objets de notes (.ppt), incorporées haut-parleur (par exemple, Objets Excel dans un .ppt). Ils peuvent être affichés dans l’éditeur de texte.
    
- **Ignorer le texte**: cette fonctionnalité facultative est définie après l’exécution de processus et avant l’analyse. Ignorer texte doit être utilisé avec précaution, car son utilisation peut réduire les performances de l’analyse des fichiers.
    
- **Texte multilingue**: eDiscovery avancée ne gère pas actuellement noms multilingues pour les balises, dépositaire et problèmes.
    
- **Métadonnées**: déterminer s’il existe des métadonnées que vous souhaitez enregistrer dans la base de données de dossier pour servir ultérieurement de référence, telles que la plage de dates, taille de fichier, le type de fichier, dépositaire et de l’objet. Métadonnées peuvent être chargée une fois que les fichiers ont été déjà chargés sans réexécuter l’inventaire ou l’ajout de nouveau traitement une surcharge. 
    
  - Si les fichiers ont été initialement chargés par le chemin d’accès, mappez la colonne chemin d’accès lorsque vous importez des métadonnées ultérieurement. Il est possible pour faire référence au fichier par ID et de mapper un autre chemin d’accès. Il s’agit d’un scénario utile lorsque vous modifiez les chemins d’accès de fichier.
    
  - Si les fichiers ont été initialement chargées par ID de fichier, mappez la colonne ID lors du chargement des métadonnées. Référence au fichier par le chemin d’accès (au lieu d’ID) entraînera fichiers recharger avec un autre code. Découverte avancée crée des copies des fichiers plutôt que du chargement des métadonnées des fichiers existants.
    
- **Familles**: il n’est pas possible de charger une famille sans parent (chef de famille). 
    
- **Taille du fichier**: il n’existe aucune limitation de la taille des fichiers chargés à la découverte électronique avancée. Pour l’analyse (analyse, la pertinence, etc.), la limite est 5,242,880 caractères du texte extrait. Fichiers de grande taille sont ignorés (par exemple, dans la pertinence, fichiers ne participe pas le processus de la pertinence de la formation et ne reçoivent pas un score de pertinence après le calcul du lot).
    
- **Quantité de fichiers**: il n’existe aucune limite sur le nombre de fichiers qui peuvent être gérés dans un seul cas recommandée. Les performances dépendent les ressources de votre système. 
    
## <a name="filtering-files"></a>Filtrage des fichiers

Une étiquette définie par l’utilisateur peut être associée à un ensemble de fichiers pour les exclure des processus ou d’autres tâches. Chaque session de processus est associée à un code de lot. Bien que le code de lot n’est pas visible à l’expert de la pertinence, il est possible à l’aide d’un utilitaire de recherche, en ajoutant un filtre pour le lot en cours et de marquer tous les fichiers appropriés avec une étiquette définie par l’utilisateur. 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Le module de processus en cours d’exécution et de chargement des données](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[Affichage des résultats de module de processus](view-process-module-results-in-advanced-ediscovery.md)

