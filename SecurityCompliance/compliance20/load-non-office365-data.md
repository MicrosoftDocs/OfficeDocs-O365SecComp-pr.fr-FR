---
title: Charger les données ne provenant pas d’Office 365 dans un ensemble de travail
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b177fc292c748f21907621196dc28d6b8fe17959
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296787"
---
# <a name="load-non-office-365-data-into-a-working-set"></a>Charger les données ne provenant pas d’Office 365 dans un ensemble de travail

Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365. Avec la fonctionnalité d'importation de contenu autre que Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans un jeu de travail afin de les analyser avec Advanced eDiscovery. Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.

>[!Note]
>Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5.

## <a name="before-you-begin"></a>Avant de commencer
L'utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants:

- Un Office 365 E3 avec le complément de conformité avancé ou l'abonnement E5.

- Tous les dépositaires dont le contenu n'est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.

- Un cas eDiscovery existant.

- Tous les fichiers de téléchargement rassemblé dans des dossiers contenant un dossier par dépositaire et le nom de ces dossiers se présente à l'alias de format *@ nomdomaine* . L' *alias @ NomDomaine* doit être l'alias et le domaine Office 365 des utilisateurs. Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine. Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* , il ne doit pas y avoir de fichiers libres dans le dossier racine.

- Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery outils de stockage Microsoft Azure installé sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.

- Installez AzCopy en procédant comme suit:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Chargement de contenu non-Office 365 dans Advanced eDiscovery

1. En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.  Cliquez sur l'onglet **jeux de travail** , puis sélectionnez la plage de travail que vous souhaitez utiliser pour charger les données Non Office 365.  Si vous n'avez pas encore créé de jeu de travail, vous pouvez le faire maintenant.  Enfin, cliquez sur **gérer les tâches définies** , puis **afficher les téléchargements** dans la section données non-Office 365

2. Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l'Assistant importation de données autres que Office 365.

![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. La première étape de l'Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.  Une fois que la préparation est comfaite, cliquez sur le bouton **suivant: charger des fichiers** .

![Importation-préparation de non-Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Dans l'étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l'emplacement des fichiers**, c'est ici que se trouvent les données autres que Office 365 que vous prévoyez d'importer.  La définition de l'emplacement correct garantit la mise à jour correcte de la commande AzCopy.

> [!NOTE]
> Si vous n'avez pas encore installé AzCopy, vous pouvez le faire à partir de là:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** . Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.  Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l'étape suivante.

![Fichiers d'importation/exportation non Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Importation AzCopy non-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant: traiter les fichiers** .  Cela démarrera le traitement, l'extraction de texte et l'indexation des fichiers téléchargés.  Vous pouvez suivre la progression du traitement ou dans l'onglet **travaux** .  Une fois terminé, les nouveaux fichiers seront disponibles dans le jeu de travail.  Une fois le traitement terminé, vous pouvez faire disparaître l'Assistant.

![Fichiers de processus d'importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

