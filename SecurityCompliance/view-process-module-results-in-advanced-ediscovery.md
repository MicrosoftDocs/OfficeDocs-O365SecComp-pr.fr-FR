---
title: Afficher les résultats du module dans Office 365 avancée de découverte électronique
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Découvrez comment trouver les résultats d’un Module de processus s’exécutent dans Office 365 avancée eDiscovery, y compris l’état de tâche et processus de synthèse.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527517"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Afficher les résultats du module dans Office 365 avancée de découverte électronique

Après la **préparation** \> **processus** est lancé, vous pouvez afficher la progression et les résultats. 
  
> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="process-task-status"></a>État de la tâche de processus

Dans **Prepare** \> **processus** \> de **résultats**, la page affiche l’état actuel (si le processus est en cours d’exécution) ou le dernier état de tâche de statut de processus comme indiqué dans l’exemple suivant.
  
![État de tâche du module de processus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
Les tâches affichées peuvent varier en fonction des options de processus sélectionnées. 
  
- **Inventaire**: découverte avancée parcourt tous les fichiers sélectionnés pour le processus et effectue la collecte de données de base.
    
- **Calculer les signatures**: calcule les signatures numériques MD5.
    
- **Extraction de composés**: extraits internes ou qu’il contient des fichiers de manière récursive à partir des fichiers composés (par exemple, PST, ZIP, MSG). Fichiers extraits sont stockés dans le dossier de cas de la casse.
    
- **Base de données de synchronisation**: processus de base de données interne.
    
- **Copie du fichier**: fichiers de processus de copie. Cette tâche est toujours affichée, même si l’option de fichiers copie avancée est sélectionnée.
    
- **Extraction de texte**: lorsque des fichiers natives, eDiscovery avancée extrait le texte de ces fichiers à l’aide de DTSearch. Le texte extrait de ces fichiers est stocké en tant que fichiers texte dans le dossier de cas.
    
- **Mise à jour des métadonnées**: traite des métadonnées chargées. 
    
- **Finalizing**: traitement interne qui finalise les données de chargée de dossiers (par exemple, identifier les fichiers d’erreur et la réussite). 
    
État de la tâche : affiché après la fin d’une tâche. Lors de l’exécutant des tâches, la durée d’exécution s’affiche.
  
> [!NOTE]
> Les tâches achevées peuvent également inclure les totaux des terminé le traitement des fichiers ou avec des erreurs. 
  
> [!TIP]
> « Annuler » fournit une option de restauration pour arrêter l’exécution des processus et puis restaurer le remplissage de données précédent ou l’enregistrée des données traitées. Restauration efface les données traitées. Si vous ne souhaitez pas les données traitées perte option Sélectionner la « Annuler » dans cette fenêtre pour choisir de ne pas annuler (par exemple, vous souhaitez recharger ces fichiers). 
  
## <a name="process-summary"></a>Résumé du processus

Dans Prepare \> processus \> résultats \> processus synthèse, une répartition des résultats fichier chargé est affichée en fonction des résultats de traitement et des erreurs de fichier réussie.
  
Les volets de présentent un affichage graphique des statistiques du fichier importé, comme suit :
  
- **Processus de synthèse s’accumulent**d : tous les fichiers dans ce cas.
    
- **Procédure de résumé**: les fichiers chargement à partir de la dernière session ou action. 
    
- **Dernière familles**: informations dans le cas (le cas échéant).
    
- Si les fichiers **d’amorçage** ont été ajoutés, le nombre de fichiers d’amorçage est répertorié par le problème a été définie pour les fichiers. 
    
    Si le marquage des fichiers **d’amorçage** a échoué, qui est également observé. 
    
- Si les fichiers **balisés préalables** ont été ajoutés, le nombre de fichiers avec des balises est répertorié par problème qui a été défini pour les fichiers. 
    
    Si le marquage des fichiers **balisés préalable** a échoué, qui est également observé. 
    
![Résumé de module de processus](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>Résumé du processus cumulés et dernière graphiques

La barre de gauche inclut Source + fichiers extraits : c'est-à-dire tous les fichiers trouvés. 
  
Le droit de la barre, traitées, inclut :
  
- Fichiers avec des erreurs de chargement
    
- Fichiers chargés avec succès, qui peuvent inclure : 
    
  - **Existant**: les fichiers qui ont été chargés avant et sont désormais chargés (notamment les doublons).
    
  - **Texte**: fichiers uniques avec du texte.
    
  - **Texte non**: vider les fichiers texte, des fichiers texte native vide, des fichiers non texte natives. 
    
  - **Dupliquer**s: fichiers en double avec du texte.
    
## <a name="last-process-errors"></a>Dernière traiter les erreurs

Dans Prepare \> processus \> résultats \> dernier processus, les détails des erreurs dans la dernière session ou action effectuée s’affichent.
  
![Erreurs de module de processus](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Le module de processus en cours d’exécution et de chargement des données](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

