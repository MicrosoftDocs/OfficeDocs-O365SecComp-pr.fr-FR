---
title: Charger des données autres qu’Office 365 dans un jeu à réviser
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
ms.openlocfilehash: 60775002d5ebec83aacbec350a044b9d6ffeb461
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834957"
---
# <a name="load-non-office-365-data-into-a-review-set"></a>Charger des données autres qu’Office 365 dans un jeu à réviser

Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365. Avec la fonctionnalité d’importation de contenu autre que Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans un jeu de réexamens afin qu’il soit analysé avec Advanced eDiscovery. Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.

>[!Note]
>Advanced eDiscovery nécessite un abonnement Office 365 E3 avec le complément de conformité avancé ou un abonnement E5 pour votre organisation. Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5.

## <a name="before-you-begin"></a>Avant de commencer

L’utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cet article requiert les éléments suivants:

- Un abonnement Office 365 ou Microsoft 365 E5 ou un abonnement E3 avec l’abonnement de complément de conformité avancé.

- Tous les dépositaires dont le contenu n’est pas Office 365 seront chargés doivent disposer d’une licence E3 avec une licence de complément de conformité avancée ou avoir une licence E5.

- Un cas de découverte électronique avancé existant.

- Les dépositaires doivent être ajoutés à l’incident avant le chargement des données non Office 365 qui leur sont associées.

- Tous les fichiers qui seront téléchargés doivent se trouver dans des dossiers, où chaque dossier est associé à un dépositaire spécifique. Les noms de ces dossiers doivent utiliser le format d’affectation de noms suivant: *alias @ NomDomaine*. L' *alias @ DomainName* doit être l’alias et le domaine Office 365 de l’utilisateur. Vous pouvez collecter tous les dossiers *alias @ NomDomaine* dans un dossier racine. Le dossier racine ne peut contenir que les dossiers *alias @ NomDomaine* ; les fichiers libres ne sont pas autorisés dans le dossier racine.

   Par exemple, la structure de dossiers pour les données non-Office 365 que vous souhaitez télécharger serait semblable à la suivante:

   - c:\nonO365\abraham.mcmahon@contoso.com
   - c:\nonO365\jewell.gordon@contoso.com
   - c:\nonO365\staci.gonzalez@contoso.com

   Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont les adresses SMTP des dépositaires dans le cas.

   ![Structure de dossier de téléchargement de données non Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery

- Outils de stockage Microsoft Azure installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.

- Installez AzCopy en procédant comme suit:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a>Chargement de contenu non-Office 365 dans Advanced eDiscovery

1. En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.  Cliquez sur l’onglet **examiner les ensembles** , puis sélectionnez l’ensemble de révision sur lequel vous souhaitez charger les données Non Office 365.  Si vous n’avez pas encore créé de jeu de révision, vous pouvez le faire maintenant.  Enfin, cliquez sur **gérer le jeu de révision** , puis sur Afficher les **téléchargements** dans la vignette des données * * autres que Office 365.

2. Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l’Assistant importation de données autres que Office 365.

   ![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. La première étape de l’Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.  Une fois la préparation terminée, cliquez sur le bouton **suivant: charger des fichiers** .

   ![Importation-préparation de non-Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. Dans l’étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l’emplacement des fichiers**, c’est ici que se trouvent les données autres que Office 365 que vous prévoyez d’importer.  La définition de l’emplacement correct garantit la mise à jour correcte de la commande AzCopy.

   > [!NOTE]
   > Si vous n’avez pas encore installé AzCopy, vous pouvez le faire à partir de là:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy

5. Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** . Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.  Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l’étape suivante.

   ![Fichiers d’importation/exportation non Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Importation AzCopy non-Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)

6. Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant: traiter les fichiers** .  Cela démarrera le traitement, l’extraction de texte et l’indexation des fichiers téléchargés.  Vous pouvez suivre la progression du traitement ou dans l’onglet **travaux** .  Une fois terminé, les nouveaux fichiers seront disponibles dans l’ensemble de révision.  Une fois le traitement terminé, vous pouvez faire disparaître l’Assistant.

   ![Fichiers de processus d’importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

