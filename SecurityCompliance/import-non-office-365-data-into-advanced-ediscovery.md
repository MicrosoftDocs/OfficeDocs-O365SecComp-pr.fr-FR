---
title: Importer du contenu Office 365 pour l’analyse de découverte électronique avancées
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Comment les étapes pour importer du contenu qui n’est pas stocké dans O365 dans un Azure blob afin qu’il peut être analysé avec AeD
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528766"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Importer du contenu Office 365 pour l’analyse de découverte électronique avancées

Pas de tous les documents que vous devrez peut-être analyser avec Office 365 avancée de découverte électronique résidera dans Office 365. Avec le contenu Non-Office 365 importer la fonctionnalité eDiscovery avancé, que vous pouvez télécharger des documents qui ne live dans Office 365 (à l’exception des fichiers PST) dans un objet blob cas stockage Azure liées et les analyser avec eDiscovery avancée. Cette procédure indique comment intégrer vos documents non Office 365 à eDiscovery avancée pour l’analyse.
  
> [!NOTE]
> Découverte avancée nécessite un Office 365 E3 avec le module complémentaire de conformité avancée ou un abonnement E5 pour votre organisation. Si vous n’avez qu’un plan d’et essayer eDiscovery avancé, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
> [!NOTE]
> Vous pouvez acheter un abonnement de module complémentaire Office 365 avancée eDiscovery données stockage pour le contenu d’Office 365. Il s’agit exclusivement disponible pour le contenu qui doit être analysées avec eDiscovery avancée. Suivez les étapes décrites dans [acheter ou de modifier et de module complémentaire pour Office 365 pour professionnels](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) et acheter Office 365 avancée eDiscovery stockage module complémentaire. 
  
## <a name="before-you-begin"></a>Avant de commencer

À l’aide de la fonctionnalité de téléchargement Non-Office 365 comme décrit dans cette procédure suppose que :
  
- Un Office 365 E3 avec le module complémentaire de conformité avancée ou abonnement E5
    
- Tous les dépositaires non Office 365 dont le contenu sera téléchargé doivent avoir E3 avec le module complémentaire de conformité avancée ou licences E5
    
- Un cas de découverte électronique existant
    
- Tous les fichiers de téléchargement regroupés dans les dossiers où il existe un dossier par dépositaire et nom des dossiers dans ce format *alias@domainname* . *alias@domainname* doit être domaine et l’alias d’utilisateurs Office 365. Vous pouvez regrouper tous les dossiers *alias@domainname* dans un dossier racine. Le dossier racine ne peut contenir les dossiers *alias@domainname* , il ne doit exister aucun fichier libre dans le dossier racine 
    
- Un compte qui est un gestionnaire eDiscovery ou un administrateur d’eDiscovery
    
- [Outils de stockage Microsoft Azure](https://aka.ms/downloadazcopy) installé sur un ordinateur ayant accès à la structure de dossier contenu Office 365. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Télécharger du contenu d’Office 365 en découverte avancée

1. En tant qu’un gestionnaire eDiscovery ou eDiscovery administrateur, ouvrez **eDiscovery**, puis le cas pour les données non Office 365 seront téléchargées. Si vous avez besoin créer un cas, voir [gérer des affaires eDiscovery de sécurité Office 365 &amp; centre de conformité](manage-ediscovery-cases.md)
    
2. Cliquez sur **Basculer vers eDiscovery avancée**
    
3. Sous **type de Source** , sélectionnez **données Non-Office 365**.
    
4. Cliquez sur **Ajouter conteneur**. Nommez le conteneur et ajouter une description.
    
5. Sélectionnez le conteneur nouvellement ajouté à partir de la liste du conteneur et copiez l’URL qui s’affiche dans le volet de détails du conteneur, puis fermez le volet
    
6. Ouvrez une invite de commandes en tant qu’administrateur et accédez au répertoire au dossier où vous avez installé des AzCopy...
    
7. Construire la ligne de commande AzCopy pour télécharger les fichiers comme suit :
    
    AzCopy /Source : « *chemin d’accès complet au dossier racine sur l’ordinateur local* » /Dest : » *URL conteneur jusqu'à, mais non compris la ?* » /DestSAS : » *reste de l’url de conteneur à partir de la ? à la fin* « / S. 
    
    Par exemple, à l’aide de ces valeurs : 
    
  - dossier racine - données C:\Collected 
    
  - url du conteneur - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;PPS = NonOfficeData15 %7 C 0&amp;sig = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA % 3D
    
    la syntaxe de ligne de commande AzCopy serait :
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Pour plus d’informations sur Azcopy syntaxe voir, [transférer des données avec l’AzCopy sur Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) . 
    
    > [!IMPORTANT]
    > Il doit y avoir un seul dossier racine par utilisateur et le nom du dossier doit être au format *alias@domainname* . 
  
8. Une fois les dossiers de téléchargement, revenez au eDiscovery avancée. Le contenu dans les dossiers que vous avez téléchargé est maintenant prêt à être traitée dans eDiscovery avancée. Sélectionnez le conteneur, cliquez sur le bouton de processus. Pour plus d’informations sur la découverte électronique avancée traitement voir, [exécutez le module de processus et charger des données dans Office 365 avancée de découverte électronique](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > Une fois le conteneur est correctement traité d’eDiscovery avancé, vous serez n’est plus en mesure d’ajouter du contenu à l’espace de stockage SAS dans Azure. Si vous collectez contenu supplémentaire et que vous souhaitez ajouter à la casse pour l’analyse de découverte électronique avancé, vous devez créer un nouveau conteneur de **données Non-Office 365** et répétez cette procédure. 
  
    > [!NOTE]
    > Si le conteneur *ne traite pas correctement en raison de problèmes d’attribution de noms de dossiers* et résoudre les problèmes, vous devez toujours créer un nouveau conteneur et la reconnexion et télécharger en utilisant les procédures décrites dans cet article. 
  

