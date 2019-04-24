---
title: Préparer un fichier CSV pour une recherche de contenu de liste d'ID dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Utilisez le fichier results. csv ou unindexed Items. csv à partir d'une recherche de contenu existante pour créer une recherche de liste d'ID qui renvoie un message électronique spécifique. Les recherches de liste d'ID sont généralement utilisées pour renvoyer des éléments de boîte aux lettres partiellement indexés.
ms.openlocfilehash: fc26f8dab11f1121deb11dd93b2cd0c70a1d629c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265448"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>Préparer un fichier CSV pour une recherche de contenu de liste d'ID dans Office 365

Vous pouvez rechercher des messages électroniques de boîte aux lettres spécifiques et d'autres éléments de boîte aux lettres à l'aide d'une liste d'ID Exchange. Pour créer une recherche de liste d'ID (anciennement appelée recherche ciblée), vous devez soumettre un fichier de valeurs séparées par des virgules (CSV) qui identifie les éléments de boîte aux lettres spécifiques à rechercher. Pour ce fichier CSV, vous utilisez le fichier **results. csv** ou le fichier d' **éléments non indexés. csv** qui est inclus lorsque vous exportez les résultats de recherche de contenu ou que vous exportez un rapport de recherche de contenu à partir de et de la recherche de contenu existante. Ensuite, modifiez l'un de ces fichiers pour indiquer les éléments spécifiques à rechercher, puis créez une nouvelle recherche de liste d'ID et soumettez le fichier CSV. 
  
Voici une présentation rapide du processus de création d'une recherche de liste d'ID.
  
1. Créez et exécutez une recherche de contenu sur une nouvelle ou guidée dans le centre de sécurité & Compliance Center.
    
2. ExPortez les résultats de la recherche de contenu ou exportez le rapport de recherche de contenu. Pour plus d'informations, consultez les rubriques suivantes :
    
    - [Exporter les résultats de la recherche de contenu](export-search-results.md)
    
    - [Exporter un rapport de recherche de contenu](export-a-content-search-report.md)
    
3. Modifiez le fichier **results. csv** ou **unindexed Items. csv** et identifiez les éléments de boîte aux lettres spécifiques que vous souhaitez inclure dans la recherche de la liste d'ID. Consultez les [instructions](#prepare-the-csv-file-for-an-id-list-search) relatives à la préparation d'un fichier CSV pour une recherche de liste d'ID. 
    
4. Créez une recherche de liste d'ID (voir les [instructions](#create-an-id-list-search)) et soumettez le fichier CSV que vous avez préparé. La requête de recherche créée ne recherche que les éléments sélectionnés dans le fichier CSV.
    
> [!NOTE]
> Les recherches de liste d'ID sont prises en charge uniquement pour les éléments de boîte aux lettres. Vous ne pouvez pas Rechercher des documents SharePoint et OneDrive dans une recherche de liste d'ID. 
  
 **Pourquoi créer une recherche de liste d'ID?** Si vous ne parvenez pas à déterminer si un élément répond à une demande eDiscovery basée sur les métadonnées dans les fichiers **results. csv** ou **éléments non indexés. csv** , vous pouvez utiliser une recherche de liste d'ID pour rechercher, prévisualiser, puis exporter cet élément afin de déterminer s'il est répondez à l'affaire que vous étudiez. Les recherches de liste d'ID sont généralement utilisées pour rechercher et renvoyer un ensemble spécifique d'éléments non indexés. 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>Préparer le fichier CSV pour une recherche de liste d'ID

Après avoir exporté les résultats de recherche ou le rapport pour une recherche de contenu, vous pouvez effectuer les étapes suivantes pour préparer le fichier CSV à une recherche de liste d'ID. Ce fichier CSV identifiera tous les éléments de la recherche de la liste d'ID.
  
Notez que vous pouvez utiliser un fichier CSV à partir d'une recherche qui inclut des sites SharePoint et des comptes OneDrive, mais vous pouvez sélectionner *uniquement* des éléments de boîte aux lettres pour une recherche de liste d'ID. Si vous sélectionnez un document dans SharePoint ou OneDrive, la validation du fichier CSV échoue lorsque vous créez une recherche de liste d'ID. 
  
1. Ouvrez le fichier **results. csv** ou **éléments non indexés. csv** dans Excel. 
    
2. Insérez une nouvelle colonne et nommez-la **sélectionnée**. L'endroit où vous insérez la colonne n'a pas d'importance. Pour des raisons de commodité, envisagez de l'insérer à gauche de la première colonne.
    
3. Dans la colonne **sélectionné** , tapez **Oui** dans la cellule correspondant à l'élément que vous souhaitez rechercher. Répétez cette étape pour chaque élément que vous souhaitez rechercher. 
    
    > [!IMPORTANT]
    > Lorsque vous ouvrez le fichier CSV dans Excel, le format de données de la colonne **ID de document** est modifié en **général**. Cela entraîne l'affichage de l'ID de document pour un élément en notation scientifique. Par exemple, l'ID de document «481037338205» est affiché sous la forme «4.81037 E + 11», vous devez effectuer les étapes suivantes pour modifier le format de données de la colonne d' **ID de document** sur **Number** afin de restaurer le format correct pour l'ID de document. Si vous ne le faites pas, la recherche de liste d'ID qui utilise le fichier CSV échouera. 
  
4. Cliquez avec le bouton droit sur toute la colonne **ID de document** et sélectionnez mettre en **forme les cellules**.
    
5. Dans la zone **catégorie** , cliquez sur **nombre**.
    
6. Modifiez le nombre de décimales en **0**, puis cliquez sur **OK** pour enregistrer vos modifications. Notez que les valeurs de la colonne ID de document sont remplacées par des numéros. 
    
    Voici un exemple de fichier CSV qui est prêt à être soumis pour une recherche de contenu de liste d'ID.
    
    ![Exemple de fichier CSV pour une recherche de contenu ciblée](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. Enregistrez le fichier CSV ou utilisez la **fonction Enregistrer sous** pour enregistrer le fichier sous un autre nom. Dans les deux cas, veillez à enregistrer le fichier au format CSV. 
  
## <a name="create-an-id-list-search"></a>Créer une recherche de liste d'ID

L'étape suivante consiste à créer une nouvelle recherche de contenu de liste d'ID et à envoyer le fichier CSV que vous avez préparé à l'étape précédente.
  
> [!IMPORTANT]
> Vous devez créer une recherche de liste d'ID au plus 2 jours après avoir exporté les résultats ou le rapport à partir d'une recherche de contenu. Si les résultats de la recherche ou le rapport exportés depuis plus de 2 jours, vous devez réexporter les résultats de la recherche ou le rapport pour générer des fichiers CSV mis à jour. Vous pouvez ensuite préparer l'un des fichiers CSV mis à jour et l'utiliser pour créer une recherche de liste d'ID. 
  
1. Dans le centre de sécurité & conformité, accédez à recherche de **contenu**de **recherche** \> .
    
2. Sur la **page recherche** , cliquez sur la flèche en ![regard de](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) ajouter une icône **nouvelle recherche**, puis cliquez sur **Rechercher par ID**.
    
    ![Cliquez sur Rechercher par ID dans la liste déroulante nouvelle recherche.](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. Dans le menu démenu de **recherche par ID** , nommez la recherche (et éventuellement la Décrivez), puis cliquez sur **Parcourir** et sélectionnez le fichier CSV que vous avez préparé à l'étape précédente. 
    
    Office 365 tente de valider le fichier CSV. Si la validation échoue, un message d'erreur s'affiche pour vous aider à résoudre les erreurs de validation. Le fichier CSV doit être validé correctement pour créer une recherche de liste d'ID.
    
4. Une fois le fichier CSV correctement validé, cliquez sur **Rechercher** pour créer la recherche de liste d'ID. 
    
    Voici un exemple des résultats de recherche estimés et de la requête générée pour une recherche de liste d'ID.
    
    ![Requête de recherche pour une recherche de contenu ciblé dans le volet d'informations](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    Notez que le nombre d'éléments estimés affichés dans les statistiques pour la recherche d'ID doit correspondre au nombre d'éléments que vous avez sélectionnés dans le fichier CSV.
    
5. PréVisualisez ou exportez les éléments renvoyés par la recherche de liste d'ID.
    
> [!NOTE]
> Si vous déplacez une boîte aux lettres après avoir créé une recherche de liste d'ID, la requête de la recherche ne renverra pas les éléments spécifiés. En effet, la propriété **DocumentID** pour les éléments de boîte aux lettres est modifiée lorsqu'une boîte aux lettres est déplacée. Dans l'instance rare lorsqu'une boîte aux lettres est déplacée après la création d'une recherche de liste d'ID, vous devez créer une nouvelle recherche de contenu (ou mettre à jour les résultats de recherche pour la recherche de contenu existante), puis exporter les résultats de la recherche ou le rapport pour générer des fichiers CSV mis à jour pouvant être utilisés  pour créer une recherche de liste d'ID. 
