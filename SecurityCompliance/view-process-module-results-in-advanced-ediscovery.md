---
title: Afficher les résultats du module de processus dans Office 365 Advanced eDiscovery
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Découvrez comment trouver les résultats d’un module de processus exécuté dans Office 365 Advanced eDiscovery, y compris l’état de la tâche et le résumé des processus.  '
ms.openlocfilehash: 4bbdbf68f71e3459ff2ddcd8ba3fb33e52f16825
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157796"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Afficher les résultats du module de processus dans Office 365 Advanced eDiscovery

Une fois le **processus** de **préparation** \> initié, vous pouvez afficher l’avancement et les résultats. 
  
> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="process-task-status"></a>État de tâche de processus

Dans **préparer** \> les **résultats**du **processus** \> , la page affiche l’état actuel (si le processus est en cours d’exécution) ou l’état de la dernière tâche d’État du processus, comme illustré dans l’exemple suivant.
  
![État de tâche du module de processus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
Les tâches affichées peuvent varier en fonction des options de processus sélectionnées. 
  
- **Inventory**: Advanced eDiscovery effectue une itération dans tous les fichiers sélectionnés pour le processus et effectue une collecte de données de base.
    
- **Calculer les signatures**: calcule les signatures numériques MD5.
    
- **Extraction de composés**: extrait les fichiers internes ou contenus de manière récursive des fichiers composés (par exemple, PST, zip, MSG). Les fichiers extraits sont stockés dans le dossier case du cas.
    
- **Synchronisation de la base de données**: processus de base de données interne.
    
- **Copie**de fichiers: copie les fichiers du processus. Cette tâche est toujours affichée, même lorsque l’option copie avancée des fichiers est sélectionnée.
    
- **Extraction de texte**: lorsqu’il existe des fichiers natifs, Advanced eDiscovery extrait le texte de ces fichiers à l’aide de DTSearch. Le texte extrait de ces fichiers est stocké sous forme de fichiers texte dans le dossier case.
    
- **Mise à jour**des métadonnées: traite les métadonnées chargées. 
    
- **Finalisation**: traitement interne qui finalise les données des fichiers de casse chargés (par exemple, identifier les fichiers d’erreur et de réussite). 
    
État de la tâche: affiché une fois la tâche terminée. Pendant l’exécution des tâches, la durée de l’exécution s’affiche.
  
> [!NOTE]
> Les tâches achevées peuvent également inclure des totaux pour les fichiers ayant terminé le traitement ou des fichiers contenant des erreurs. 
  
> [!TIP]
> «Annuler» fournit une option de restauration pour arrêter l’exécution du processus, puis restaurer le remplissage de données précédent ou les données traitées enregistrées. La restauration efface toutes les données traitées. Si vous ne souhaitez pas que les données traitées soient perdues (par exemple, si vous envisagez de recharger ces fichiers), sélectionnez l’option «Annuler» dans cette fenêtre pour choisir de ne pas restaurer. 
  
## <a name="process-summary"></a>Résumé du processus

Dans la \> synthèse \> du \> processus de préparation des résultats du processus, une répartition des résultats des fichiers chargés est affichée en fonction du traitement réussi des fichiers et des résultats de l’erreur.
  
Les volets présentent un affichage graphique des statistiques sur les fichiers importés, comme suit:
  
- Le **Résumé des processus accumule**d: tous les fichiers dans le cas.
    
- **Dernier processus-Résumé**: fichiers chargés à partir de la dernière session ou action. 
    
- **** Famille: informations sur la famille dans le cas (le cas échéant).
    
- Si des fichiers de **départ** ont été ajoutés, le nombre de fichiers de départ est indiqué par problème qui a été défini pour les fichiers. 
    
    Si le marquage des fichiers de **départ** a échoué, cela est également indiqué. 
    
- Si des fichiers **pré-balisés** ont été ajoutés, le nombre de fichiers pré-balisés est indiqué par problème qui a été défini pour les fichiers. 
    
    Si le marquage des fichiers **pré-balisés** a échoué, cela est également indiqué. 
    
![Résumé de module de processus](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>Processus récapitulatif de processus accumulés et derniers graphiques

La barre de gauche inclut les fichiers sources et extraits: tous les fichiers trouvés. 
  
La barre de droite, traitée, inclut les éléments suivants:
  
- Fichiers avec des erreurs de chargement
    
- Fichiers correctement chargés, qui peuvent inclure les éléments suivants: 
    
  - **Existant**: les fichiers qui ont été chargés précédemment et sont à nouveau chargés (y compris les doublons).
    
  - **Text**: fichiers uniques avec texte.
    
  - **Non-texte**: fichiers texte vides, fichiers texte natif vides, fichiers non-texte natifs. 
    
  - **Duplicate**s: fichiers en double avec texte.
    
## <a name="last-process-errors"></a>Erreurs du dernier processus

Dans \> prepare \> process \> Results Last process Errors, les détails des erreurs de la dernière session ou action effectuée sont affichés.
  
![Erreurs de module de processus](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Exécution du module de processus et chargement des données](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

