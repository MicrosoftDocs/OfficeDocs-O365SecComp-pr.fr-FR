---
title: Préparation des données pour Office 365 Advanced eDiscovery
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
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Découvrez comment utiliser le centre de sécurité &amp; conformité Microsoft 365 pour préparer les données Office 365 pour analyse avec Office 365 Advanced eDiscovery. '
ms.openlocfilehash: d9d81c145a86075affd76761eb6dcff0f84a1eac
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265506"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Préparation des données pour Office 365 Advanced eDiscovery

Cette rubrique décrit comment charger les résultats d'une recherche de contenu dans dans un cas dans Advanced eDiscovery. 
  
> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>Étape 1: préparer les données Office 365 pour Advanced eDiscovery

Pour analyser les données avec Advanced eDiscovery, vous pouvez utiliser les résultats d'une recherche de contenu que vous exécutez dans le centre &amp; de sécurité conformité Microsoft 365 (mentionné sur la page **recherche de contenu** dans &amp; le centre de sécurité conformité Microsoft 365) ou un recherche associée à un cas eDiscovery (figurant sur la page **eDiscovery** du centre de &amp; sécurité conformité). 
  
Pour obtenir la procédure détaillée sur la préparation des résultats de recherche pour analyse dans Advanced eDiscovery, voir [Prepare Search Results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).
  
> [!NOTE]
> Si vous disposez de données en dehors d'Office 365 et que vous souhaitez les importer dans Office 365 de manière à pouvoir les préparer et les analyser dans Advanced eDiscovery, voir [Overview of Import PST Files to office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) et [Archiving tiers data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918). 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>Étape 2: chargement des données de résultats de recherche dans dans un cas dans Advanced eDiscovery

Une fois que vous avez préparé les résultats de &amp; la recherche dans le centre de sécurité conformité pour analyse, l'étape suivante consiste à charger les résultats de la recherche dans un cas dans Advanced eDiscovery. Pour plus d'informations, consultez [la rubrique exécuter le module de processus](run-the-process-module-in-advanced-ediscovery.md).
  
1. Accédez à la page [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte scolaire ou professionnel.
    
3. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
4. Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez charger les données dans Advanced eDiscovery. 
    
5. Sur la page **Accueil** du cas, cliquez sur **Advanced eDiscovery**. 
    
    ![Cliquez sur basculer vers Advanced eDiscovery pour ouvrir le cas dans Advanced eDiscovery](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    La barre **de progression de la connexion à Advanced eDiscovery** s'affiche. Lorsque vous êtes connecté à Advanced eDiscovery, une liste de conteneurs apparaît dans la page de configuration de l'incident. 
    
    ![Le cas est affiché dans Advanced eDiscovery](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Ces conteneurs représentent les résultats de recherche que vous avez préparés pour l'analyse dans Advanced eDiscovery à l'étape 1. Notez que le nom du conteneur porte le même nom que la recherche de contenu dans le centre de sécurité &amp; conformité. Les conteneurs de la liste sont ceux que vous avez préparés. Si un autre utilisateur a préparé des résultats de recherche pour Advanced eDiscovery, les conteneurs correspondants ne seront pas inclus dans la liste. 
    
6. Pour charger les données de résultats de recherche à partir d'un conteneur dans le cas dans Advanced eDiscovery, sélectionnez un conteneur, puis cliquez sur **traiter**.
    
Une fois que les résultats de la &amp; recherche du centre de sécurité conformité sont ajoutés à l'incident dans Advanced eDiscovery, l'étape suivante consiste à utiliser les outils dans Advanced eDiscovery pour analyser et rechercher les données pertinentes pour le cas. 
  
## <a name="see-also"></a>Voir aussi

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Configurer des utilisateurs et des cas](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[Analyse des données d’un cas](analyze-case-data-with-advanced-ediscovery.md)
  
[Gestion de la configuration de la pertinence](manage-relevance-setup-in-advanced-ediscovery.md)
  
[Utilisation du module de pertinence](use-relevance-in-advanced-ediscovery.md)
  
[Exportation des données d’un cas](export-case-data-in-advanced-ediscovery.md)

