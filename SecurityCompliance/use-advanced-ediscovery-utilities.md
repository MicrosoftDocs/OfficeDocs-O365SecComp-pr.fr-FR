---
title: Utilisez les utilitaires de découverte électronique Office 365 avancée
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'En savoir plus sur les utilitaires d’Office 365 avancée eDiscovery, y compris le journal d’événements, effacer les données, traiter les erreurs, modifiez la pertinence et l’analyse de transparence.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527585"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Utilisez les utilitaires de découverte électronique Office 365 avancée

> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Les utilitaires sont affichés et disponibles dans eDiscovery avancée dépendent des rôles de contexte et d’utilisateur.
  
## <a name="case-log"></a>Journal d’événements

Le journal des cas fournit une liste détaillée des activités de traitement de l’application, qui peut être utilisé pour le suivi, résoudre les problèmes et pour le traitement des erreurs et avertissements. Le journal peut être généré et stocké localement sur l’hôte ou le serveur ou envoyé directement à une adresse de messagerie.
  
Le fichier journal peut également être téléchargé à l’ordinateur client. L’option de téléchargement du client peut être activée ou désactivée en fonction du rôle d’utilisateur et de configuration.
  
1. Dans la barre de menus, cliquez sur l’icône **pignon** . 
    
2. Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **journal des cas \> le programme d’installation**.
    
3. Sélectionnez le **niveau de journalisation** comme suit : 
    
  - **Standard**: inclut les données du journal de base. Cette option n’est généralement nécessaire pour la surveillance et doit être utilisée à moins que recommandé dans le cas contraire.
    
  - **Minimum**: utilisée dans le cas de très grande taille et renvoie uniquement les données les plus récentes.
    
4. Cliquez sur **journal d’exécuter les cas**. Le journal est généré et le chemin d’accès est affiché. Les informations de l’avancement des tâches pour la tâche en cours et le dernier s’affiche dans le volet d’état.
    
## <a name="clear-data"></a>Effacer les données

S’il est nécessaire de supprimer ou réinitialiser les données de cas, l’instance de base de données doit être initialisé. L’utilitaire d’effacement des données supprime spécifiées toutes les entrées de la casse de la base de données, fichiers texte, dossier de cas et résultats cumulés. La fonction peut uniquement être effectuée par un administrateur.
  
> [!IMPORTANT]
> Cette action n’est pas réversible et efface toutes les marquer la pertinence et analyse effectuée par l’expert. Enregistrer une sauvegarde de données, si nécessaire. Utilisez cette option avec précaution. Suppression des fichiers balisés et classés peut avoir un impact sur les résultats de la pertinence. 
  
1. Dans la barre de menus, cliquez sur l’icône **pignon** . 
    
2. Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **Effacer les données \> le programme d’installation**.
    
3. Sélectionnez une option pour obtenir les informations d’initialisation :
    
  - **Pertinence**: supprime tous les, dans la pertinence, y compris la définition de la charge et l’association de fichiers à des charges de travail. Il supprime tous les exemples et marquage.
    
  - **Près de doublons et les threads de messagerie**: supprime toutes les informations d’analyse de proximité des doublons et les threads de messagerie.
    
  - **Thèmes**: supprime les données liées à des thèmes.
    
  - **Exporter l’historique**: supprime les informations d’historique des lots de l’exportation.
    
4. Cliquez sur **Effacer les données**. Les données des dossiers sont désactivées. Les informations de progression de la tâche en cours et la dernière tâche sont affichées dans le volet **d’état de la tâche** . 
    
## <a name="modify-relevance"></a>Modifier la pertinence

Cette section décrit comment ignorer ou annuler un exemple de la pertinence.
  
1. Dans la barre de menus, cliquez sur l’icône **pignon** . 
    
2. Dans la **utilitaires et les paramètres \> utilitaires** , sélectionnez **la pertinence de la modifier**.
    
3. Sélectionnez l’une des options : 
    
  - **Exemple actuel ignorer - utilisateur actif**: Cela permet d’identifier, comme à **Ignorer**, tous les fichiers non balisés dans l’exemple de cas open de l’utilisateur qui exécute l’utilitaire. Traitement de la pertinence pas sera effectuée sur les fichiers marqués comme à **Ignorer**.
    
  - **Exemple actuel ignorer - tous les exemples d’ouvrir**: Cela permet d’identifier, comme à **Ignorer**, tous les fichiers non balisés dans tous les exemples pour tous les utilisateurs. Cette option n’est pas recommandée si les utilisateurs sont balisage actuellement exemples.
    
  - **Annuler la dernière exemple**: le dernier réalisé la pertinence de la formation sera restaurée, qu’elle soit avant ou après le processus de « Calculer ». Restauration d’un exemple de rattrapage n’est pas autorisée.
    
4. Cliquez sur **exécuter** pour exécuter. 
    
## <a name="transparency-analysis"></a>Analyse de transparence

L’utilitaire d’analyse de transparence permet une vue détaillée des fichiers et leurs score de pertinence affecté. Le rapport utilisable comme un contrôle de validité ou pour comparer la pertinence d’un fichier défini par un réviseur humain par rapport à la pertinence attribué par eDiscovery avancée. 
  
En plus des résultats de la pertinence, découverte avancée calcule et affecte le poids de mot clé que prendre en compte le contexte du mot clé. Poids différents, selon le contexte et l’emplacement peut être affecté à la même mot dans un fichier. Chaque mot clé est marqué à l’aide d’une échelle augmentation de l’intensité de couleur allant de jaune à orange foncé et différentes nuances de gris. Codage en couleurs est utilisé pour indiquer visuellement la famille du mot contribution positive ou négative pour le score de pertinence. 
  
Dans un scénario de plusieurs problèmes, un rapport d’analyse de transparence peut être généré pour chaque problème.
  
1. Dans la barre de menus, cliquez sur l’icône **pignon** . 
    
2. Dans la **utilitaires et les paramètres \> utilitaires** onglet, sélectionnez **analyse transparence \> le programme d’installation**.
    
3. Dans ** ID du fichier **, entrez l’ID de fichier du fichier à traiter.
    
4. Dans la liste des **problèmes** , sélectionnez le problème pertinent. 
    
5. Cliquez sur **analyse de transparence**. Une fois terminé, le rapport d’analyse de transparence pour le fichier s’affiche, qui indique la façon dont les couleurs de mot clé marqués correspondent au score de pertinence.
    
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Définir les paramètres de la casse et client](define-case-and-tenant-settings-in-advanced-ediscovery.md)

