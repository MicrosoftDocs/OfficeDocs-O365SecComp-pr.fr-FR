---
title: Charger des données de non Office 365 dans un jeu de travail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 427b4c8c9dfffe351827a6869ae26a5356d646d8
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607688"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Charger des données de non Office 365 dans un jeu de travail

Pas de tous les documents que vous devrez peut-être analyser avec Office 365 avancée de découverte électronique résidera dans Office 365. Avec le contenu Non-Office 365 importer la fonctionnalité de découverte avancé, que vous pouvez télécharger des documents qui ne live dans Office 365 dans un jeu de travail afin qu’il est analysé avec eDiscovery avancée. Cette procédure indique comment intégrer vos documents non Office 365 à eDiscovery avancée pour l’analyse.

>[!Note]
>Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5.

## <a name="before-you-begin"></a>Avant de commencer
À l’aide de la fonctionnalité de téléchargement Non-Office 365 comme décrit dans cette procédure suppose que :
* Un Office 365 E3 avec le module complémentaire de conformité avancée ou abonnement E5
* Tous les dépositaires non Office 365 dont le contenu sera téléchargé doivent avoir E3 avec le module complémentaire de conformité avancée ou licences E5
* Un cas de découverte électronique existant
* Tous les fichiers de téléchargement regroupés dans les dossiers où il existe un dossier par dépositaire et nom des dossiers dans ce format *alias@domainname* . *alias@domainname* doit être domaine et l’alias d’utilisateurs Office 365. Vous pouvez regrouper tous les dossiers *alias@domainname* dans un dossier racine. Le dossier racine ne peut contenir les dossiers *alias@domainname* , il ne doit exister aucun fichier libre dans le dossier racine
* Un compte qui est installé sur un ordinateur ayant accès à la structure de dossier contenu Office 365 eDiscovery administrateur Microsoft Azure stockage outils ou un gestionnaire eDiscovery.
* Installer AzCopy, vous pouvez le faire à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Télécharger du contenu d’Office 365 en découverte avancée
1. En tant qu’un gestionnaire eDiscovery ou eDiscovery administrateur, ouvrez eDiscovery avancé, puis le cas pour les données non Office 365 seront téléchargées.  Cliquez sur l’onglet **jeux de travail** , puis sélectionnez le jeu de travail que vous souhaitez charger les données Non-Office 365.  Si vous n’avez pas déjà créé un jeu de travail, vous pouvez le faire maintenant.  Enfin, cliquez sur **Gérer les rouages** puis **téléchargements affichage** dans la section de données Non-Office 365

2. Cliquez sur le bouton **télécharger des fichiers** pour démarrer l’Assistant Importation de données Non-Office 365.

![Télécharger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. La première étape dans l’Assistant prépare simplement un blob Azure sécurisé pour les téléchargement de fichiers.  Une fois la préparation de compelted, cliquez sur le **suivant : télécharger les fichiers** bouton.

![Non Office 365 importer - préparation](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Dans l’étape de **télécharger des fichiers** , spécifiez le **chemin d’accès à l’emplacement des fichiers**, il s’agit où se trouve les données Non-Office 365 que vous prévoyez d’importation.  Définition de l’emplacement correct garantit la AzCopy commande correctement mise à jour.

> [!NOTE]
> Si vous n’avez pas déjà installé AzCopy, vous pouvez effectuer cela à partir d’ici :https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Copiez la commande prédéfinie en cliquant sur le lien **Copier dans le Presse-papiers** . Démarrez une invite de commandes windows, collez la commande et appuyez sur ENTRÉE.  Les fichiers seront téléchargés vers le stockage blob Azure sécurisé pour l’étape suivante.

![Importation non-Office 365 - télécharger des fichiers](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importation non Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. Enfin, renvoyer à la conformité de & sécurité, cliquez sur le **suivant : traitement des fichiers** bouton.  Ceci va démarrer le traitement, extraction de texte et l’indexation des fichiers téléchargés.  Vous pouvez suivre la progression de traitement ici ou dans l’onglet **tâches** .  Une fois terminé, les nouveaux fichiers seront disponibles dans le jeu de travail.  Une fois le traitement est terminé, vous pouvez fermer l’Assistant.

![Importation non-Office 365 - traiter les fichiers](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

