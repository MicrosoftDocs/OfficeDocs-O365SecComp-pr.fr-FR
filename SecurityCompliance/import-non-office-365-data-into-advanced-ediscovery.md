---
title: Importer du contenu non-Office 365 pour une analyse Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Procédure d'importation de contenu qui n'est pas stocké dans O365 dans un objet BLOB Azure afin qu'il puisse être analysé avec AeD
ms.openlocfilehash: 1019fa2e2429aeff8bd20bc3dfb266ab5fb25eaf
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217064"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a>Importer du contenu non-Office 365 pour une analyse Advanced eDiscovery

Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365. Avec la fonctionnalité d'importation de contenu non-Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne sont pas en ligne dans Office 365 (à l'exception des fichiers PST) dans un blob de stockage associé à une casse, et les analyser avec Advanced eDiscovery. Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.
  
> [!NOTE]
> Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
> [!NOTE]
> Vous pouvez acheter un abonnement de complément de stockage de données eDiscovery Office 365 Advanced eDiscovery pour votre contenu non-Office 365. Cette fonctionnalité est exclusivement disponible pour le contenu qui doit être analysé avec Advanced eDiscovery. Suivez les étapes de l'achat ou de la [modification et du complément pour office 365 pour les entreprises](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) et achetez le complément de stockage Office 365 Advanced eDiscovery Storage. 
  
## <a name="before-you-begin"></a>Avant de commencer

L'utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants:
  
- Une application Office 365 E3 avec un complément de conformité avancé ou un abonnement E5
    
- Tous les dépositaires dont le contenu n'est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.
    
- Un cas eDiscovery existant
    
- Tous les fichiers de téléchargement rassemblé dans des dossiers contenant un dossier par dépositaire et le nom de ces dossiers se présente à l'alias de format *@ nomdomaine* . L' *alias @ NomDomaine* doit être l'alias et le domaine Office 365 des utilisateurs. Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine. Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* , il ne doit pas y avoir de fichiers libres dans le dossier racine. 
    
- Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery
    
- [Outils de stockage Microsoft Azure](https://aka.ms/downloadazcopy) installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365. 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Chargement de contenu non-Office 365 dans Advanced eDiscovery

1. En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez **eDiscovery**et ouvrez le cas où les données non Office 365 seront téléchargées vers. Si vous devez créer un cas, voir [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)
    
2. Cliquer sur **basculer vers Advanced eDiscovery**
    
3. Sous **type** de source **, sélectionnez données non Office 365**.
    
4. Cliquez sur **Ajouter un conteneur**. Nommez le conteneur et ajoutez une description.
    
5. Sélectionnez le conteneur nouvellement ajouté dans la liste du conteneur et copiez l'URL qui apparaît dans le volet d'informations du conteneur, puis fermez le volet.
    
6. Ouvrez une invite de commandes en tant qu'administrateur et accédez au répertoire dans lequel vous avez installé AzCopy..
    
7. Construisez la ligne de commande AzCopy pour télécharger les fichiers comme suit:
    
    AzCopy/source: " *chemin d'accès complet au dossier racine sur l'ordinateur local* "/dest: " *URL de conteneur jusqu'au* "/DestSAS: ", qui inclut le *reste de l'URL du conteneur à partir du? jusqu'à la fin* «/S. 
    
    Par exemple, à l'aide des valeurs suivantes: 
    
  - dossier racine-données C:\Collected 
    
  - URL du conteneur https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp-; SR =&amp;c si = NonOfficeData15%&amp;7C0 SIG = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA% 3D
    
    la syntaxe de la ligne de commande AzCopy est la suivante:
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    Pour plus d'informations sur la syntaxe Azcopy, reportez-vous à [la rubrique transférer des données avec le Azcopy sur Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) . 
    
    > [!IMPORTANT]
    > Il doit y avoir un dossier racine par utilisateur et le nom du dossier doit être au format *alias @ NomDomaine* . 
  
8. Une fois le téléchargement des dossiers terminé, revenez à Advanced eDiscovery. Le contenu des dossiers téléchargés est maintenant prêt à être traité dans Advanced eDiscovery. Sélectionnez le conteneur, puis cliquez sur le bouton processus. Pour plus d'informations sur le traitement de la découverte électronique avancée, consultez [la rubrique exécuter le module de processus et charger des données dans Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
    
    > [!IMPORTANT]
    > Une fois que le conteneur a été traité avec succès dans Advanced eDiscovery, vous ne pourrez plus ajouter de nouveau contenu au stockage SAS dans Azure. Si vous recueillez du contenu supplémentaire et que vous souhaitez l'ajouter à la demande d'analyse avancée de la découverte électronique, vous devez créer un conteneur de **données non-Office 365** et répéter cette procédure. 
  
    > [!NOTE]
    > Si le conteneur *ne traite pas correctement en raison de problèmes d'attribution de nom de dossier* et que vous résolvez les problèmes, vous devrez tout de même créer un nouveau conteneur et reconnecter et télécharger à nouveau à l'aide des procédures décrites dans cet article. 
  

