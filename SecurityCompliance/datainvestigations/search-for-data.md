---
title: Rechercher des données dans une enquête
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
ms.openlocfilehash: 5f52f26c4443addd0e108794e1d3635a9b8efb98
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030078"
---
# <a name="search-for-data-in-an-investigation"></a>Rechercher des données dans une enquête

Sous l'onglet **Rechercher** dans une enquête de données, vous pouvez rechercher des données déplacées, confidentielles ou sensibles dans les emplacements de contenu dans Office 365 à l'aide de mots clés et de conditions. 

Après avoir exécuté une recherche, vous pouvez afficher des statistiques sur les éléments renvoyés par la recherche, tels que les emplacements de contenu qui ont le plus d'éléments qui correspondent à la requête de recherche. Vous pouvez également afficher un aperçu d'un sous-ensemble des résultats. Une fois que vous avez identifié l'ensemble des documents qui souhaitent approfondir votre enquête, vous pouvez ajouter les résultats de la recherche à un ensemble de preuves afin de poursuivre le processus et l'analyse.

## <a name="create-a-search"></a>Create a search

1. Dans une enquête, cliquez sur l'onglet **recherches** , puis sur **nouvelle recherche**. 

    Un Assistant s'affiche pour vous guider tout au long du processus de création d'une recherche.

2. Entrez un nom de recherche et une description facultative pour la recherche.

3. Définissez vos critères de recherche. Vous pouvez ajouter des conditions pour la recherche à l'aide des cartes de condition prédéfinies ou en utilisant des noms de propriétés de recherche dans la requête par mot clé. Pour plus d'informations, consultez la rubrique [créer des requêtes de recherche](build-search-queries.md).

4. Choisissez les emplacements de contenu (sources de données) à rechercher. Vous pouvez étendre la recherche en sélectionnant les emplacements de contenu de personnes intéressantes (si vous en avez ajouté à l'enquête). Si vous avez ajouté des personnes intéressantes pour l'enquête, vous pouvez les ajouter en suivant les étapes décrites dans [Manage People of Interest](manage-people-of-interest.md#add-people-of-interest).
 
    Dans certains cas, vous devrez peut-être commencer par rechercher tous les emplacements de contenu de votre organisation; par ailleurs, vous pouvez avoir besoin de rechercher des emplacements qui ne sont pas détenues par une personne spécifique. Dans ce scénario, vous pouvez choisir d'effectuer une recherche dans l'ensemble de votre organisation ou tous les emplacements pour des services Office 365 spécifiques (par exemple, Exchange, SharePoint, OneDrive entreprise ou Teams.

5. Enregistrez et exécutez la recherche.

Une fois la recherche créée, une page de menu volant s'affiche avec des détails sur la recherche. Notez que les **statistiques** et les boutons d' **Aperçu** sont initialement estompés car la recherche n'a pas été effectuée. Vous pouvez suivre la progression de en surveillant la colonne **État** de l'onglet **recherches** .

## <a name="view-statistics-and-search-results"></a>Afficher les statistiques et les résultats de la recherche

Une fois que vous avez créé et démarré une recherche d'enquête de données, l'outil utilise les critères de recherche (les emplacements de contenu et de requête de recherche) que vous avez définis et recherche dans le service actif des éléments correspondant à vos critères de recherche. Trois composants d'une recherche sont renvoyés lorsque la recherche est terminée: 

- **Estimate** : étant donné que la recherche ne recherche qu'un index (plutôt que les emplacements de contenu réels), les résultats d'une recherche sont une estimation (en fonction de ce qui a été trouvé dans l'index qui correspond aux résultats de la recherche). Un résumé de l'estimation s'affiche sur la page mobile de recherche sous **État**. Notez que l'état du processus d'estimation pour une recherche s'affiche sous l'onglet **recherches** dans la colonne État de l' **estimation** . Lorsque l'estimation de la recherche est terminée, cet État est défini sur **réussi**.

- **Statistics** -Statistics fournit des informations plus détaillées sur les résultats de la recherche. Les voici :

    - Résumé: statistiques similaires aux résultats d'estimation de recherche affichés sur la page de menu volant.
    - Emplacements les plus fréquents: statistiques sur le nombre d'éléments qui correspondent à la requête de recherche dans chaque emplacement de contenu recherché. 
    - Requêtes-statistiques détaillées sur la requête de recherche, y compris le nombre d'éléments qui correspondent à chaque condition dans une requête de recherche.

    Cliquez sur **statistiques** sur la page de menu volant pour afficher ces statistiques. Notez que ce bouton est inactif jusqu'à ce que la valeur de l' **État d'estimation** sur l'onglet **recherches** soit définie sur **réussite**. Pour plus d'informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).

- **Aperçu** : lorsque la recherche est terminée, vous pouvez afficher les éléments réels à partir d'un sous-ensemble des résultats de la recherche renvoyés par la recherche. Vous pouvez afficher dans l'affichage natif du type d'élément, mais vous pouvez également afficher les métadonnées relatives à l'élément. Il s'agit d'un moyen efficace pour déterminer rapidement si les résultats de la recherche sont ceux que vous attendiez ou si vous devez modifier la recherche et la réexécuter. Cliquez sur **Aperçu** sur la page de menu volant pour afficher les éléments des résultats de la recherche. Notez que ce bouton est inactif jusqu'à ce que la valeur de l' **État aperçu** sur l'onglet **recherches** soit définie sur **réussite**.
 
> [!NOTE]
> Les valeurs d'état des colonnes **État** de l'estimation et état de l' **Aperçu** de l'onglet **recherches** sont **envoyées**, **en cours**et **réussies**. S'il y a une erreur avec la recherche, l'état **échec** est affiché.

## <a name="add-search-results-to-evidence"></a>Ajouter des résultats de recherche à des preuves

Lorsque vous êtes satisfait des résultats d'une recherche et que vous êtes prêt à analyser et à corriger ces résultats de recherche, vous pouvez les ajouter à un ensemble de preuves lors de l'enquête. Lorsque vous ajoutez des éléments à un ensemble de preuves sur l'onglet **preuve** , les deux événements suivants se produisent:

- Tous les éléments des résultats de la recherche sont copiés à partir de la source de données dans le service actif et copiés dans un emplacement de stockage Azure sécurisé dans le Cloud Microsoft.

- Tous les éléments (y compris le contenu et les métadonnées) sont réindexés de sorte que toutes les données du jeu de preuves soient entièrement utilisables lors de votre enquête. La réindexation des données permet d'effectuer des recherches complètes et très rapides lorsque vous recherchez des données dans l'ensemble de preuves lors de votre enquête.

L'un des avantages de la copie des données actives dans un ensemble de preuves dans Azure est que pour les incidents urgents ou critiques, vous pouvez rapidement contenir les dommages en supprimant immédiatement le contenu suspect de la source de données d'origine dans le service actif, puis en examinant l'incident en analysant les preuves qui ont été copiées dans l'environnement en quarantaine de l'emplacement de stockage Azure. 

La copie des données d'origine dans l'ensemble de preuves facilite également votre enquête en vous fournissant des outils d'analyse avancés, tels que la détection de thèmes, la détection de proximité et l'identification des threads de messagerie.

Si nécessaire, vous pouvez également ajouter des données provenant de sources de données autres que Office 365 à un jeu de preuves afin qu'il soit stocké avec les données que vous collectez à partir d'Office 365.

Pour ajouter des données à un ensemble de preuves, sélectionnez une recherche dans l'onglet **recherches** , puis cliquez sur **Ajouter des résultats aux preuves** sur la page de menu volant. Notez que vous pouvez ajouter des données à un ensemble de preuves existant ou créer un ensemble de preuves à la volée.

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a>Suivi de la progression de l'ajout de résultats de recherche à des preuves

L'ajout de données à un jeu de preuves est un processus de longue durée. Le processus inclut la collecte des éléments de la source de données d'origine à partir d'Office 365 (par exemple, à partir de boîtes aux lettres et de sites), en les copiant vers ** l'emplacement de stockage Azure (ce processus de copie est également appelé «ingestion»), puis la réindexation des éléments. Vous pouvez suivre la progression sous l'onglet **travaux** ou sur l'onglet **recherches** dans la colonne **données ajoutées à la preuve** . Une fois le traitement du traitement des preuves terminé, vous pouvez accéder à l'onglet **preuve** , cliquer sur l'ensemble de preuves, puis lancer votre enquête en recherchant, examiner, Baliser et exporter les données pertinentes selon vos besoins.