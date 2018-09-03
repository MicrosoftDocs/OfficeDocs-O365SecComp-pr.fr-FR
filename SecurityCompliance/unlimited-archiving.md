---
title: Vue d’ensemble de l’archivage illimité dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: En savoir plus sur Développer automatiquement l’archivage dans Office 365, qui fournit un nombre illimité d’archivage pour les boîtes aux lettres Exchange Online.
ms.openlocfilehash: a762a0fb8295a645957404c1c88881f40329f7a1
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782121"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a>Vue d’ensemble de l’archivage illimité dans Office 365

Dans Office 365, les boîtes aux lettres d’archive fournissent aux utilisateurs d’espace de stockage des boîtes aux lettres supplémentaires. Une fois que la boîte aux lettres de l’utilisateur archive est activé, jusqu'à 100 Go de stockage supplémentaire est disponible. Lorsque le quota de stockage de 100 Go est atteinte, les organisations devaient contacter Microsoft pour une demande d’espace de stockage supplémentaire pour une boîte aux lettres d’archive. Qui n’est plus le cas. La nouvelle fonctionnalité d’archivage illimitée dans Office 365 (appelée *Développer automatiquement l’archivage*) fournit un nombre illimité de stockage de boîtes aux lettres d’archive. Désormais, lorsque le quota de stockage dans la boîte aux lettres d’archive est atteinte, Office 365 augmente automatiquement la taille de l’archive, ce qui signifie que les utilisateurs ne seront pas exécutés en dehors de l’espace de stockage de boîtes aux lettres et les administrateurs ne doivent demander un stockage supplémentaire pour les boîtes aux lettres d’archive .
  
Pour obtenir des instructions pas à pas pour activer la développer automatiquement l’archivage, voir [Activer l’archivage illimité dans Office 365](enable-unlimited-archiving.md).
  
> [!NOTE]
> Développer automatiquement l’archivage également prend en charge les boîtes aux lettres partagées. Pour activer l’archivage pour une boîte aux lettres partagée, une licence Exchange Online Plan 2 ou une licence Exchange Online Plan 1 avec une licence de l’archivage Exchange Online est nécessaire. 
  
## <a name="how-auto-expanding-archiving-works"></a>Fonctionnement de l’archivage comment développer automatiquement

Comme expliqué précédemment, d’autres boîtes aux lettres d’espace de stockage est créé lors de la boîte aux lettres de l’utilisateur archive est activé. Lors de l’extension automatique d’archivage est activé, Office 365 vérifie périodiquement la taille de la boîte aux lettres d’archive. Lorsqu’une boîte aux lettres d’archive obtient a presque atteint sa limite de stockage, Office 365 crée automatiquement espace de stockage supplémentaire pour l’archive. Si l’utilisateur s’exécute en dehors de cet espace de stockage supplémentaire, Office 365 ajoute davantage d’espace de stockage pour l’archivage de l’utilisateur. Ce processus se produit automatiquement, ce qui signifie que les administrateurs ne peuvent pas demander d’archivage supplémentaires ou gérer développer automatiquement l’archivage. 
  
Voici une vue d’ensemble rapide du processus.
  
![Vue d’ensemble du processus d’archivage automatique-développement](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. L’archivage est activé pour une boîte aux lettres utilisateur ou d’une boîte aux lettres partagée. Une boîte aux lettres d’archive avec 100 Go d’espace de stockage est créé, et le quota d’avertissement pour la boîte aux lettres d’archive est défini sur 90 Go.
    
2. Un administrateur permet de développer automatiquement l’archivage pour la boîte aux lettres. Puis, lorsque la boîte aux lettres d’archivage (y compris le dossier éléments récupérables) atteint 90 Go, il est converti en une archive développer automatiquement et Office 365 ajoute l’espace de stockage dans l’archive. Notez qu’il peut prendre jusqu'à 30 jours pour l’espace de stockage supplémentaire être mis en service.
    
3. Office 365 ajoute automatiquement l’espace de stockage dans l’archive lorsque cela est nécessaire.
  
> [!IMPORTANT]
> Si une boîte aux lettres est mis en attente ou affecté à une stratégie de rétention d’Office 365, le quota de stockage pour les boîtes aux lettres d’archive est augmenté à 110 Go lorsque développer automatiquement l’archivage est activé. De même, le quota d’avertissement d’archivage est augmenté à 100 Go.

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a>Quel est déplacé vers l’espace de stockage d’archive supplémentaires ?

Pour optimiser l’utilisation du stockage d’archives développer automatiquement, les dossiers peuvent obtenir déplacés. Office 365 détermine quels dossiers sont déplacées lorsque stockage supplémentaire est ajouté à l’archive. Lorsqu’un dossier est déplacé, un sous-dossier est créé sous le dossier d’origine dans la partie de l’archive de la liste des dossiers dans Outlook. Ce nouveau sous-dossier pointe vers les éléments qui ont été déplacés. La convention d’affectation de noms par Office 365 pour nommer ce dossier est ** \<nom du dossier\>_yyyy (imposée mmm jj, aaaa h_mm)**, où : 
  
- **aaaa** est l’année que les messages dans le dossier ont été reçus. 
    
- **mmm jj, aaaa h_m** est la date et l’heure auxquelles le sous-dossier a été créé par Office 365, au format UTC, en fonction du fuseau horaire de l’utilisateur et les paramètres régionaux dans Outlook. 
    
Les captures d’écran suivante affiche une liste de dossiers avant et après que les messages sont déplacés dans une archive développé automatique.
  
 **Avant de stockage supplémentaire est ajouté.**
  
![Liste des dossiers de boîte aux lettres de l’archivage avant de développer automatiquement une archive est mis en service](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 **Après l’ajout d’espace de stockage supplémentaire**
  
![Liste des dossiers de boîte aux lettres de l’archive après que développer automatiquement une archive est mis en service](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a>Conditions requises pour Outlook pour accéder aux éléments dans une archive développé automatique

Pour accéder aux messages qui sont stockés dans une archive développé automatique, les utilisateurs doivent employer un des clients Outlook suivants :
  
- Outlook 2016 pour Windows
    
- Outlook sur le web 
    
- Outlook 2016 pour Mac 
    
> [!NOTE]
> Les utilisateurs Outlook 2013 peuvent uniquement accéder aux éléments qui ont été stockés à l’origine dans leur boîte aux lettres d’archive. Ils ne pourront pour accéder aux éléments qui sont déplacés vers un stockage d’archives supplémentaires. 
  
Voici quelques éléments à prendre en compte lors de l’utilisation d’Outlook ou Outlook sur le web pour accéder aux messages stockés dans une archive développé automatique.
  
- Vous pouvez accéder de n’importe quel dossier dans votre boîte aux lettres archive, y compris celles qui ont été déplacés vers la zone de stockage étendu automatique.
    
- Vous pouvez rechercher des éléments qui ont été déplacés vers une zone de stockage supplémentaire qu’en recherchant le dossier lui-même. Cela signifie que vous devez sélectionner le dossier d’archivage dans la liste des dossiers pour sélectionner l’option de **Dossier actif** en tant que l’étendue de recherche. De même, si un dossier dans une zone de stockage étendu automatique contient des sous-dossiers, vous devez rechercher chaque sous-dossier séparément. 
    
- Élément de compte dans Outlook et lu/des nombres (dans Outlook et Outlook sur le web) dans une archive développé automatique peuvent ne pas être précis.
    
- Vous pouvez supprimer des éléments dans un sous-dossier qui pointe vers une zone de stockage étendu automatique, mais le dossier lui-même ne peut pas être supprimé.
    
- Vous ne pouvez pas utiliser la fonctionnalité récupérer les éléments supprimés pour récupérer un élément a été supprimé d’une zone de stockage étendu automatique.
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a>Développer automatiquement l’archivage et autres fonctionnalités de conformité d’Office 365

Cette section décrit la relation entre développer automatiquement l’archivage conformité Office 365 et autres fonctionnalités de gouvernance des données.
  
- **découverte électronique** - lorsque vous utilisez un outil de découverte électronique Office 365, tels que de la recherche de contenu ou In-Place eDiscovery, les zones de stockage supplémentaire dans une archive développé automatique sont inclus dans la recherche.
    
- **Rétention** - lorsque vous mettre en attente une boîte aux lettres dans Exchange Online à l’aide des outils tels que litige ou en cas de découverte électronique contient et stratégies de rétention de sécurité Office 365 &amp; centre de conformité, le contenu situé dans une archive développé automatique est également mis en attente.
    
- **Messagerie (MRM) de gestion des enregistrements** - si vous utilisez des stratégies de suppression de MRM dans Exchange Online pour supprimer définitivement les éléments de boîte aux lettres ayant expiré, éléments arrivés à expiration situés dans l’archive de développé automatique seront également supprimés.
    
- **Importer le service** - vous pouvez utiliser le service Office 365 importer pour importer des fichiers PST vers l’archive de développé automatique d’un utilisateur. Vous pouvez importer jusqu'à 100 Go de données à partir des fichiers PST boîte aux lettres d’archive de l’utilisateur. 

## <a name="more-information"></a>Plus d'informations

Pour obtenir des informations sur l’extension automatique d’archivage, consultez la rubrique [Office 365 : Forum aux questions des Archives développer automatiquement](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).