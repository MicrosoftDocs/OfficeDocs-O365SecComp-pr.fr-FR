---
title: Télécharger l’exportation des travaux
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Installez et utilisez l’Explorateur de stockage Azure pour télécharger des documents qui ont été exportés à partir d’un jeu de vérification dans Advanced eDiscovery.
ms.openlocfilehash: f236f53be9dda88fe5b8448011aa651603e38182
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230999"
---
# <a name="download-export-jobs"></a>Télécharger l’exportation des travaux

Lorsque vous exportez des documents à partir d’un jeu de réexamen dans un cas avancé de découverte électronique, les documents sont téléchargés vers un emplacement de stockage Azure fourni par Microsoft ou vers un emplacement de stockage Azure géré par votre organisation. Le type d’emplacement de stockage Azure utilisé dépend de l’option sélectionnée lors de l’exportation des documents. 

Cet article fournit des instructions sur l’utilisation de l’Explorateur de stockage Microsoft Azure pour se connecter à un emplacement de stockage Azure afin de parcourir et télécharger les documents exportés. Pour plus d’informations sur l’Explorateur de stockage Azure, voir [démarrage rapide: utiliser l’Explorateur de stockage Azure](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer).

## <a name="step-1-install-the-azure-storage-explorer"></a>Étape 1: installer l’Explorateur de stockage Azure

La première étape consiste à télécharger et à installer l’Explorateur de stockage Azure. Pour obtenir des instructions, consultez la rubrique [outil Explorateur de stockage Azure](https://go.microsoft.com/fwlink/p/?LinkId=544842). Utilisez cet outil pour vous connecter aux documents exportés et les télécharger à l’étape 3.

## <a name="step-2-obtain-the-sas-url-from-the-export-job"></a>Étape 2: obtenir l’URL SAS à partir de la tâche d’exportation

L’étape suivante consiste à obtenir l’URL de signature d’accès partagé (SAS) générée lorsque vous avez créé le travail d’exportation pour [exporter des documents à partir d’un jeu de révision](export-documents-from-review-set.md). Vous pouvez copier l’URL SAS des documents téléchargés vers un emplacement de stockage Azure fourni par Microsoft ou un emplacement de stockage Azure géré par votre organisation. Dans les deux cas, vous utilisez l’URL SAS pour vous connecter à l’emplacement de stockage Azure à l’étape 3.

1. Sur la page **Advanced eDiscovery** , accédez au cas, puis cliquez sur l’onglet **** exports.

2. Sous l’onglet **exportations** , cliquez sur le travail d’exportation que vous souhaitez télécharger.

3. Sur la page de menu volant, sous **emplacements**, copiez l’URL de la version SAS affichée. Si nécessaire, vous pouvez l’enregistrer dans un fichier pour pouvoir y accéder à l’étape 3.
 
   ![Copier l’URL SAS affichée sous locations](../media/eDiscoExportJob.png)

## <a name="step-3-connect-to-the-azure-storage-location"></a>Étape 3: Connectez-vous à l’emplacement de stockage Azure

La dernière étape consiste à utiliser l’Explorateur de stockage Azure et l’URL SAS pour se connecter à l’emplacement de stockage Azure et télécharger les documents que vous avez exportés vers un ordinateur local.

1.  Ouvrez l’Explorateur de stockage Azure que vous avez installé à l’étape 1.

2. Cliquez sur l’icône **Ajouter un compte** . Vous pouvez également cliquer avec le bouton droit sur **comptes de stockage**.

   ![Cliquez sur l’icône Ajouter un compte](../media/AzureStorageConnect.png)

3.  Sur la page **connexion à Azure Storage** , cliquez sur **utiliser un URI de signature d’accès partagé (SAS)** , puis cliquez sur **suivant**.

    ![Cliquez sur utiliser un URI de signature d’accès partagé (SAS), puis sur suivant.](../media/AzureStorageConnect2.png)

4.  Dans la page **attacher avec l’URI SAS** , cliquez dans la zone URI, puis collez l’URL SAS que vous avez obtenue à l’étape 2. 

    ![Coller l’URL SAS dans la zone URI](../media/AzureStorageConnect3.png)

    Notez qu’une partie de l’URL SAS apparaît dans la zone **nom d’affichage** . Il sera utilisé comme nom d’affichage du conteneur créé sous les **comptes de stockage** une fois que vous vous êtes connecté à l’emplacement de stockage. Ce nom se compose de l’ID du cas de découverte électronique avancée, de et d’un identificateur unique. Vous pouvez conserver le nom d’affichage par défaut ou le modifier. Si vous le modifiez, le nom d’affichage doit être unique.

5.  Cliquez sur **Suivant**.

    La page **Résumé de connexion** s’affiche.
   
    ![Cliquez sur se connecter sur la page de résumé de connexion pour vous connecter à l’emplacement de stockage Azure.](../media/AzureStorageConnect4.png)

6. Sur la page **Résumé de connexion** , passez en revue les informations de connexion, puis cliquez sur **se connecter**. 

    Le nœud **conteneurs BLOB** (sous **comptes** > **de stockage (conteneurs associés)** \> est ouvert. 

    ![](../media/AzureStorageConnect5.png)

    Il contient un conteneur nommé avec le nom d’affichage de l’étape 4. Ce conteneur contient un dossier pour chaque tâche d’exportation que vous avez créée. Ces dossiers sont nommés avec un ID correspondant à l’ID de la tâche d’exportation. Vous trouverez ces ID d’exportation (et le nom de l’exportation) sous **informations de support** sur la page de menu volant pour chaque tâche **de préparation des données pour l’exportation** , dans l’onglet **travaux** .

7. Double-cliquez sur le dossier exporter le travail pour l’ouvrir.

   Une liste des dossiers et des rapports d’exportation s’affiche.
   
    ![Le dossier d’exportation contient des fichiers exportés et des rapports d’exportation](../media/AzureStorageConnect6.png)

   Le dossier exporter le travail contient les éléments suivants. Les éléments réels dans le dossier d’exportation sont déterminés par les options d’exportation configurées lors de la création du travail d’exportation. Pour plus d’informations, consultez [la rubrique exporter des documents à partir d’un jeu de révision](export-documents-from-review-set.md).

    - Export_load_file. csv: ce fichier CSV est un rapport d’exportation détaillé qui contient des informations sur chaque document exporté. Le fichier se compose d’une colonne pour chaque propriété de métadonnées d’un document. Pour obtenir la liste et la description des métadonnées incluses dans ce rapport, reportez-vous à la colonne **nom du champ exporté** du tableau dans les [champs de métadonnées de document dans Advanced eDiscovery](document-metadata-fields.md).
    
    - Summary. txt: fichier texte contenant un résumé de l’exportation, y compris les statistiques d’exportation.
    
    - Extracted_text_files: ce dossier contient une version de fichier texte de chaque document exporté.
     
    - NativeFiles: ce dossier contient une version de fichier native de chaque document exporté.
    
    - Error_files: ce dossier inclut les éléments suivants lorsque le travail d’exportation contient des fichiers d’erreur: 
        
      - ExtractionError. csv: ce fichier CSV contient les métadonnées disponibles pour les fichiers qui n’ont pas été correctement extraits de leur élément parent.
        
      - ProcessingError: ce dossier contient des documents contenant des erreurs de traitement. Ce contenu se trouve au niveau de l’élément, ce qui signifie qu’en cas d’erreur de traitement d’une pièce jointe, le document contenant la pièce jointe est également inclus dans ce dossier.
 
8. Pour exporter tout le contenu de l’exportation, sélectionnez le dossier exporter, puis cliquez sur **Télécharger**.

9. Spécifiez l’emplacement où vous souhaitez télécharger les fichiers exportés, puis cliquez sur Sélectionner un dossier.

    L’Explorateur de stockage Azure démarre le processus d’exportation. L’état de téléchargement des éléments exportés est affiché dans le volet **activités** . Un message s’affiche lorsque le téléchargement est terminé.

    ![Un message s’affiche lorsque le téléchargement est terminé.](../media/AzureStorageConnect8.png)

> [!NOTE]
> Au lieu de télécharger l’intégralité du travail d’exportation, vous pouvez sélectionner des éléments spécifiques à télécharger. Et au lieu de télécharger des éléments, vous pouvez double-cliquer sur un élément pour l’afficher.