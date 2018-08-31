---
title: Préparer des données pour la découverte Office 365 avancée
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
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Découvrez comment utiliser le Office 365 Security &amp; centre de conformité pour préparer des données d’Office 365 pour l’analyse avec Office 365 avancée de découverte électronique. '
ms.openlocfilehash: cf0c76b0c274121da435de7829c769abf5111cab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528496"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a>Préparer des données pour la découverte Office 365 avancée

Cette rubrique décrit comment charger les résultats d’une recherche de contenu à un cas de découverte électronique avancée dans. 
  
> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a>Étape 1 : Préparer des données d’Office 365 pour la découverte avancée

Pour analyser les données avec eDiscovery avancé, vous pouvez utiliser les résultats d’une recherche de contenu que vous exécutez dans l’Office 365 Security &amp; centre de conformité (répertoriés dans la page de **recherche de contenu** de sécurité Office 365 &amp; centre de conformité) ou une recherche associé à un cas de découverte électronique (répertoriés dans la page de **découverte électronique** dans la sécurité &amp; centre de conformité). 
  
Pour obtenir les étapes détaillées sur la préparation des résultats de recherche pour l’analyse d’eDiscovery avancée, voir [préparer les résultats de recherche pour la découverte Office 365 avancés](prepare-search-results-for-advanced-ediscovery.md).
  
> [!NOTE]
> Si vous avez des données en dehors d’Office 365 et à importer vers Office 365 afin que vous puissiez préparer et analyser de découverte avancée, une, voir [vue d’ensemble de l’importation de fichiers PST vers Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) et [d’archivage des données tierces dans Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918). 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a>Étape 2 : Charge les données obtenues dans à un cas de découverte électronique avancée

Après avoir préparé les résultats de recherche dans la sécurité &amp; centre de conformité pour l’analyse, l’étape suivante consiste à charger les résultats de recherche dans un cas de découverte électronique avancée. Pour plus d’informations, voir [exécuter le module de processus](run-the-process-module-in-advanced-ediscovery.md).
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l’aide de votre compte professionnel ou de l’école.
    
3. Dans la sécurité &amp; centre de conformité, cliquez sur **recherche &amp; enquête** \> **eDiscovery** vous permet d’afficher la liste des incidents dans votre organisation. 
    
4. En regard de la casse que vous souhaitez charger des données dans eDiscovery avancée, cliquez sur **Ouvrir** . 
    
5. Dans la page **d’accueil** pour le cas, cliquez sur **Avancé eDiscovery**. 
    
    ![Cliquez sur Basculer en découverte avancée pour ouvrir le cas de découverte électronique avancée](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    La barre de progression **se connectant à la découverte électronique avancé** s’affiche. Lorsque vous êtes connecté à la découverte électronique avancée, une liste de conteneurs s’affiche dans la page du programme d’installation pour le cas. 
    
    ![Le cas est affiché dans la découverte électronique avancée](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Ces conteneurs représentent les résultats de recherche que vous avez préparé pour l’analyse d’eDiscovery avancé à l’étape 1. Notez que le nom du conteneur a le même nom que la recherche de contenu dans le cas de la sécurité &amp; centre de conformité. Les conteneurs dans la liste sont ceux que vous avez préparé. Si un autre utilisateur préparé les résultats de la recherche avancée eDiscovery, les conteneurs correspondants ne sont pas inclus dans la liste. 
    
6. Pour charger les données de résultats de recherche à partir d’un conteneur pour le cas d’eDiscovery avancée, sélectionnez un conteneur, puis cliquez sur **le processus**.
    
Une fois les résultats de recherche à partir de la sécurité &amp; centre de conformité sont ajoutés au cas de découverte électronique avancée, l’étape suivante consiste à utiliser les outils d’eDiscovery avancée pour analyser et éliminez les données qui sont pertinentes pour le cas. 
  
## <a name="see-also"></a>Voir aussi

[eDiscovery avancée Office 365](office-365-advanced-ediscovery.md)
  
[Configurer les utilisateurs et les cas](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[Analyse des données de dossiers](analyze-case-data-with-advanced-ediscovery.md)
  
[Gestion des paramètres de pertinence](manage-relevance-setup-in-advanced-ediscovery.md)
  
[À l’aide du module de la pertinence](use-relevance-in-advanced-ediscovery.md)
  
[Exportation des données de cas](export-case-data-in-advanced-ediscovery.md)

