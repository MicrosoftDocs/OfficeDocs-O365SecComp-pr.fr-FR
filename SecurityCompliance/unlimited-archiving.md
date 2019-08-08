---
title: Vue d’ensemble d’un archivage illimité dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Découvrez la croissance automatique de l’archivage dans Office 365, qui offre un stockage d’archive illimité pour les boîtes aux lettres Exchange Online.
ms.openlocfilehash: 21489683bbb9f3e2addb5e95a38d8f8a418639de
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231078"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Vue d’ensemble d’un archivage illimité dans Office 365

Dans Office 365, les boîtes aux lettres d’archivage fournissent aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire. Une fois la boîte aux lettres d’archivage d’un utilisateur activée, jusqu’à 100 Go d’espace de stockage supplémentaire est disponible. Dans le passé, lorsque le quota de stockage de 100 Go était atteint, les organisations devaient contacter Microsoft pour demander un espace de stockage supplémentaire pour une boîte aux lettres d’archivage. Cela n’est plus le cas.

La fonctionnalité d’archivage illimité d’Office 365 (appelée *archivage à extension automatique*) fournit un espace illimité de stockage dans les boîtes aux lettres d’archivage. À présent, lorsque le quota de stockage dans la boîte aux lettres d’archivage est atteint, Office 365 augmente automatiquement la taille de l’archive, ce qui signifie que les utilisateurs ne peuvent pas manquer d’espace de stockage de boîte aux lettres et que les administrateurs n’ont pas à demander un stockage supplémentaire pour les boîtes aux lettres d’archivage. .
  
Pour obtenir des instructions détaillées sur l’activation de l’archivage à extension automatique, consultez la rubrique [activation de l’archivage illimité dans Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> L’archivage à extension automatique prend aussi en charge les boîtes aux lettres partagées. Pour activer l’archivage pour une boîte aux lettres partagée, une licence Exchange Online plan 2 ou une licence Exchange Online plan 1 avec une licence d’archivage Exchange Online est requise. 
  
## <a name="how-auto-expanding-archiving-works"></a>Fonctionnement de l’archivage en développement automatique

Comme expliqué précédemment, un espace de stockage de boîte aux lettres supplémentaire est créé lorsque la boîte aux lettres d’archivage d’un utilisateur est activée. Lorsque l’archivage à extension automatique est activé, Office 365 vérifie régulièrement la taille de la boîte aux lettres d’archivage. Lorsqu’une boîte aux lettres d’archivage est proche de sa limite de stockage, Office 365 crée automatiquement un espace de stockage supplémentaire pour l’archive. Si l’utilisateur manque d’espace de stockage supplémentaire, Office 365 ajoute davantage d’espace de stockage à l’archive de l’utilisateur. Ce processus se produit automatiquement, ce qui signifie que les administrateurs n’ont pas besoin de demander un stockage d’archivage supplémentaire ou de gérer l’archivage à extension automatique. 
  
Voici une présentation rapide du processus.
  
![Vue d’ensemble du processus d’archivage à extension automatique](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. L’archivage est activé pour une boîte aux lettres d’utilisateur ou une boîte aux lettres partagée. Une boîte aux lettres d’archivage de 100 Go d’espace de stockage est créée et le quota d’avertissement pour la boîte aux lettres d’archivage est défini sur 90 Go.
    
2. Un administrateur permet l’archivage à extension automatique pour la boîte aux lettres. Ensuite, lorsque la boîte aux lettres d’archivage (y compris le dossier éléments récupérables) atteint 90 Go, elle est convertie en une archive à extension automatique et Office 365 ajoute de l’espace de stockage à l’archive. Notez que le temps de mise en service de l’espace de stockage supplémentaire peut prendre jusqu’à 30 jours.
    
3. Office 365 ajoute automatiquement davantage d’espace de stockage à l’archive lorsque cela est nécessaire.
  
> [!IMPORTANT]
> Si une boîte aux lettres est placée en conservation ou affectée à une stratégie de rétention Office 365, le quota de stockage du maibox d’archivage est augmenté de 110 Go lorsque l’archivage à extension automatique est activé. De même, le quota d’avertissement d’archivage est porté à 100 Go.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>Qu’est-ce qui est déplacé vers l’espace de stockage d’archive supplémentaire?

Pour utiliser efficacement le stockage d’archives à extension automatique, les dossiers peuvent être déplacés. Office 365 détermine quels dossiers sont déplacés lorsque du stockage supplémentaire est ajouté à l’archive. Lorsqu’un dossier est déplacé, un sous-dossier est automatiquement créé sous le dossier d’origine dans la partie Archive de la liste des dossiers dans Outlook. Ce nouveau sous-dossier pointe vers les éléments qui ont été déplacés. La Convention d’affectation de noms utilisée par Office 365 pour nommer ce dossier est ** \<le nom\>de dossier _yyyy (créé sur MMM DD, yyyy h_mm)**, où: 
  
- **yyyy** est l’année de réception des messages dans le dossier. 
    
- **MMM DD, yyyy h_m** est la date et l’heure auxquelles le sous-dossier a été créé par Office 365, au format UTC, basé sur le fuseau horaire et les paramètres régionaux de l’utilisateur dans Outlook. 
    
Les captures d’écran suivantes montrent une liste des dossiers avant et après le déplacement des messages dans une archive étendue automatiquement.
  
 **Avant l’ajout d’un espace de stockage supplémentaire**
  
![Liste des dossiers de la boîte aux lettres d’archivage avant la mise en service de l’archive à extension automatique](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Après l’ajout d’un espace de stockage supplémentaire**
  
![Liste des dossiers de la boîte aux lettres d’archivage après mise en service de l’archive à extension automatique](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Conditions requises par Outlook pour accéder aux éléments dans une archive étendue automatiquement

Pour accéder aux messages stockés dans une archive étendue automatiquement, les utilisateurs doivent utiliser l’un des clients Outlook suivants:
  
- Outlook 2016 ou Outlook 2019 pour Windows
    
- Outlook sur le web 
    
- Outlook 2016 ou Outlook 2019 pour Mac 
    
> [!NOTE]
> Les utilisateurs d’Outlook 2013 peuvent uniquement accéder aux éléments qui étaient initialement stockés dans leur boîte aux lettres d’archivage. Ils ne pourront pas accéder aux éléments déplacés vers un stockage d’archivage supplémentaire. 
  
Voici quelques éléments à prendre en compte lors de l’utilisation d’Outlook ou d’Outlook sur le Web pour accéder aux messages stockés dans un archivage développé automatiquement.
  
- Vous pouvez accéder à n’importe quel dossier de votre boîte aux lettres d’archivage, y compris ceux qui ont été déplacés vers la zone de stockage étendu automatiquement.
    
- Vous pouvez rechercher des éléments qui ont été déplacés vers une zone de stockage supplémentaire uniquement en effectuant une recherche dans le dossier proprement dit. Cela signifie que vous devez sélectionner le dossier d’archivage dans la liste des dossiers pour sélectionner l’option **dossier actif** comme étendue de recherche. De même, si un dossier d’une zone de stockage à extension automatique contient des sous-dossiers, vous devez effectuer une recherche dans chaque sous-dossier séparément. 
    
- Le nombre d’éléments dans Outlook et le nombre de lectures/non de lectures (dans Outlook et Outlook sur le Web) dans une archive étendue automatiquement peuvent ne pas être précis.
    
- Vous pouvez supprimer des éléments dans un sous-dossier qui pointe vers une zone de stockage à extension automatique, mais le dossier proprement dit ne peut pas être supprimé.
    
- Vous ne pouvez pas utiliser la fonctionnalité récupérer les éléments supprimés pour récupérer un élément qui a été supprimé d’une zone de stockage à extension automatique.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Extension de l’archivage et autres fonctionnalités de conformité Office 365

Cette section décrit la fonctionnalité entre l’archivage et les autres fonctionnalités de conformité et de gouvernance des données Office 365.
  
- **découverte électronique** : lorsque vous utilisez un outil ediscovery Office 365, tel que la recherche de contenu ou la découverte électronique inaltérable, les zones de stockage supplémentaires dans une archive étendue automatiquement sont également recherchées.
    
- **** Rétention: lorsque vous placez une boîte aux lettres en conservation à l’aide d’outils comme la conservation pour litige dans Exchange Online ou la stratégie de rétention et les stratégies de rétention dans le centre de sécurité et de conformité, le contenu situé dans un archivage développé automatiquement est également placé en conservation.
    
- **Gestion des enregistrements de messagerie (MRM)** : Si vous utilisez des stratégies de suppression MRM dans Exchange Online pour supprimer définitivement des éléments de boîte aux lettres expirés, les éléments expirés situés dans l’archive étendue automatiquement seront également supprimés.
    
- **Import service** : vous pouvez utiliser le service d’importation Office 365 pour importer des fichiers PST dans l’archive étendue automatiquement. Vous pouvez importer jusqu’à 100 Go de données à partir de fichiers PST vers la boîte aux lettres d’archivage de l’utilisateur. 

## <a name="more-information"></a>Plus d’informations

Pour plus d’informations techniques sur l’archivage à extension automatique, consultez la rubrique [Office 365: Forum aux questions](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/)sur les archives.