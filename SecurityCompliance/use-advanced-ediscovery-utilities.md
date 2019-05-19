---
title: Utiliser les utilitaires eDiscovery avancés d’Office 365
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Découvrez les utilitaires d’Office 365 Advanced eDiscovery, notamment le journal des cas, les données claires, les erreurs de processus, la pertinence et l’analyse de la transparence.  '
ms.openlocfilehash: df769ddddd37284da50bc715444f2bf928307706
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157956"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Utiliser les utilitaires eDiscovery avancés d’Office 365

> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Les utilitaires affichés et disponibles dans Advanced eDiscovery dépendent des rôles de contexte et d’utilisateur.
  
## <a name="case-log"></a>Journal des cas

Le journal des cas fournit une liste détaillée des activités de traitement des applications, qui peuvent être utilisées pour le suivi, la résolution des problèmes et la résolution des erreurs et des avertissements. Le journal peut être généré et stocké localement sur l’hôte ou le serveur, ou envoyé directement à une adresse de messagerie.
  
Le fichier journal peut également être téléchargé sur l’ordinateur du client. L’option de téléchargement de client peut être activée ou désactivée en fonction de la configuration et du rôle d’utilisateur.
  
1. Dans la barre de menus, cliquez sur l’icône **cogwheel** . 
    
2. Dans l’onglet **paramètres et \> ** utilitaires, sélectionnez **configuration du journal \> des incidents**.
    
3. Sélectionnez le **niveau** de journalisation comme suit: 
    
  - **Standard**: inclut les données de journal de base. Cette option est généralement nécessaire pour la surveillance et doit être utilisée sauf indication contraire.
    
  - **Minimal**: utilisé pour les très grandes situations et renvoie uniquement les données les plus récentes.
    
4. Cliquez sur **exécuter le journal des cas**. Le journal est généré et le chemin d’accès est affiché. Les informations d’avancement de la tâche pour les tâches en cours et dernière sont affichées dans le volet État de la tâche.
    
## <a name="clear-data"></a>Effacer les données

S’il est nécessaire de supprimer ou de réinitialiser les données de cas, l’instance de base de données doit être initialisée. L’utilitaire effacer les données supprime toutes les entrées spécifiées de la base de données de cas, des fichiers texte, du dossier case et des résultats accumulés. La fonction peut uniquement être effectuée par un administrateur.
  
> [!IMPORTANT]
> Cette action n’est pas réversible et efface toutes les balises et les analyses de pertinence effectuées par l’expert. Enregistrer une sauvegarde des données, si nécessaire. Utilisez cette option avec une extrême précaution. La suppression des fichiers balisés et classés peut avoir un impact sur les résultats de pertinence. 
  
1. Dans la barre de menus, cliquez sur l’icône **cogwheel** . 
    
2. Dans l’onglet **paramètres et \> ** utilitaires, sélectionnez **effacer la configuration \> des données**.
    
3. Sélectionnez une option pour l’initialisation des informations:
    
  - **Pertinence**: supprime tout le travail réalisé en matière de pertinence, y compris la définition des charges et des associations de fichiers à charger. Il supprime tous les exemples et balisage.
    
  - **Near-Duplicates et threads de messagerie**: supprime toutes les informations d’analyse des liens de proximité et des fils de messagerie.
    
  - **Themes**: supprime les données liées aux thèmes.
    
  - **Historique des exportations**: supprime les informations d’historique des lots d’exportation.
    
4. Cliquez sur **effacer les données**. Les données de cas sont effacées. Les informations d’avancement de la tâche pour les tâches en cours et dernière sont affichées dans le volet État de la **tâche** . 
    
## <a name="modify-relevance"></a>Modifier la pertinence

Cette section décrit comment ignorer ou restaurer un exemple de pertinence.
  
1. Dans la barre de menus, cliquez sur l’icône **cogwheel** . 
    
2. Dans l’onglet **paramètres et \> ** utilitaires, sélectionnez **modifier la pertinence**.
    
3. Sélectionnez l’une des options suivantes: 
    
  - **Ignorer l’exemple actuel: pour l’utilisateur actuel**: cette balise, sous la forme **Ignorer**, tous les fichiers non balisés dans l’exemple de cas d’ouverture de l’utilisateur qui exécute l’utilitaire. Le traitement de pertinence ne sera pas effectué sur les fichiers marqués comme **Skip**.
    
  - **Ignorer l’exemple actuel-tous les exemples ouverts**: cette balise, sous la forme **Ignorer**, tous les fichiers non balisés de tous les exemples ouverts pour tous les utilisateurs. Cette option n’est pas recommandée si les utilisateurs sont actuellement en train de baliser des exemples.
    
  - **Restaurer le dernier exemple**: le dernier exemple de formation à la pertinence terminé sera annulé, qu’il soit ou non avant ou après le processus de «calcul». La restauration d’un exemple de rattrapage n’est pas autorisée.
    
4. Cliquez sur **exécuter** pour exécuter. 
    
## <a name="transparency-analysis"></a>Analyse de la transparence

L’utilitaire d’analyse de transparence active une vue détaillée des fichiers et le score de pertinence qui leur est attribué. Le rapport peut être utilisé en tant que contrôle de validité ou comparer la pertinence d’un fichier défini par un réviseur humain par rapport à la pertinence attribuée par Advanced eDiscovery. 
  
Outre les scores de pertinence, la découverte électronique avancée calcule et affecte des pondérations de mots clés qui envisagent le contexte de mot clé. Le même mot dans un fichier peut se voir attribuer différents poids, selon le contexte et l’emplacement. Chaque mot clé est marqué à l’aide d’une échelle croissante d’intensité de couleur allant de jaune à orange foncé et de différentes nuances de gris. Le codage en couleurs permet d’indiquer visuellement la contribution positive ou négative du mot au score de pertinence. 
  
Dans un scénario de cas à plusieurs problèmes, un rapport d’analyse de transparence peut être généré pour chaque problème.
  
1. Dans la barre de menus, cliquez sur l’icône **cogwheel** . 
    
2. Dans l’onglet **paramètres et \> ** utilitaires, sélectionnez Configuration de l' **analyse \> de transparence**.
    
3. Dans * * ID de fichier * *, entrez l’ID de fichier du fichier à traiter.
    
4. Dans la liste **problème** , sélectionnez le problème pertinent. 
    
5. Cliquez sur **analyse de transparence**. Une fois l’opération terminée, le rapport d’analyse de transparence du fichier s’affiche, qui montre comment les couleurs de mots clés marquées correspondent au score global de pertinence.
    
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Définition des paramètres de cas et de client](define-case-and-tenant-settings-in-advanced-ediscovery.md)

