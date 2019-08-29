---
title: Rechercher des données dans une investigation
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
description: ''
ms.openlocfilehash: bcd7f3f38f53ef22fc50823f3d2e3564af333431
ms.sourcegitcommit: 3962de88a143f0eb416b5cfdfd777d731f560ec8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36649899"
---
# <a name="search-for-data-in-an-investigation"></a>Rechercher des données dans une investigation

Sous l’onglet **Rechercher** dans une enquête de données, vous pouvez rechercher des données déplacées, confidentielles ou sensibles dans les emplacements de contenu dans Office 365 à l’aide de mots clés et de conditions. 

Après avoir exécuté une recherche, vous pouvez afficher des statistiques sur les éléments renvoyés par la recherche, tels que les emplacements de contenu qui ont le plus d’éléments qui correspondent à la requête de recherche. Vous pouvez également afficher un aperçu d’un sous-ensemble des résultats. Une fois que vous avez identifié le jeu de documents à étudier plus en détail, vous pouvez ajouter les résultats de la recherche à un ensemble de preuves afin de poursuivre le processus et l’analyse.

## <a name="create-a-search"></a>Create a search

1. Dans une enquête, cliquez sur l’onglet **recherches** , puis sur **nouvelle recherche**. 

    Un Assistant s’affiche pour vous guider tout au long du processus de création d’une recherche.

2. Entrez un nom de recherche et une description facultative pour la recherche.

3. Définissez vos critères de recherche. Vous pouvez ajouter des conditions pour la recherche à l’aide des cartes de condition prédéfinies ou en utilisant des noms de propriétés de recherche dans la requête par mot clé. Pour plus d’informations, consultez la rubrique [créer des requêtes de recherche](build-search-queries.md).

4. Choisissez les emplacements de contenu (sources de données) à rechercher. Vous pouvez étendre la recherche en sélectionnant les emplacements de contenu de personnes intéressantes (si vous en avez ajouté à l’enquête). Si vous avez ajouté des personnes intéressantes pour l’enquête, vous pouvez les ajouter en suivant les étapes décrites dans [Manage People of Interest](manage-people-of-interest.md#add-people-of-interest).
 
   Parfois, vous devrez peut-être commencer par rechercher tous les emplacements de contenu dans votre organisation. Par ailleurs, vous pouvez avoir besoin de rechercher des emplacements qui ne sont pas détenues par une personne spécifique. Dans ce scénario, vous pouvez choisir d’effectuer une recherche dans l’ensemble de votre organisation ou tous les emplacements pour des services Office 365 spécifiques (par exemple, Exchange, SharePoint, OneDrive entreprise ou Teams.

5. Enregistrez et exécutez la recherche.

Une fois la recherche créée, une page de menu volant s’affiche avec des détails sur la recherche. Les **statistiques** et les boutons d' **Aperçu** sont initialement estompés car la recherche n’a pas été effectuée. Vous pouvez suivre la progression de la recherche en surveillant la colonne **État** de l’onglet **recherches** .

## <a name="view-statistics-and-search-results"></a>Afficher les statistiques et les résultats de la recherche

Une fois que vous avez créé et démarré une recherche d’enquête de données, l’outil utilise les critères de recherche (les emplacements de contenu et de requête de recherche) que vous avez définis et recherche dans le service actif des éléments correspondant à vos critères de recherche. Trois composants d’une recherche sont renvoyés lorsque la recherche est terminée: 

- **Estimation** : étant donné que la recherche ne recherche qu’un index (plutôt que l’emplacement de contenu réel), les résultats d’une recherche sont une estimation (en fonction de ce qui a été trouvé dans l’index qui correspond aux résultats de la recherche). Un résumé de l’estimation s’affiche sur la page mobile de recherche sous **État**. L’état du processus d’estimation pour une recherche s’affiche sous l’onglet **recherches** dans la colonne État de l' **estimation** . Lorsque l’estimation de la recherche est terminée, cet État est défini sur **réussi**.

- **Statistiques** : les statistiques fournissent des informations plus détaillées sur les résultats de la recherche. Les voici :

    - Résumé: statistiques similaires aux résultats d’estimation de recherche affichés sur la page de menu volant.
    - Emplacements les plus fréquents: statistiques sur le nombre d’éléments qui correspondent à la requête de recherche dans chaque emplacement de contenu recherché. 
    - Requêtes: statistiques détaillées sur la requête de recherche, y compris le nombre d’éléments qui correspondent à chaque condition dans une requête de recherche.

    Cliquez sur **statistiques** sur la page de menu volant pour afficher ces statistiques. Ce bouton est inactif jusqu’à ce que la valeur de l' **État d’estimation** sur l’onglet **recherches** soit définie sur **réussite**. Pour plus d’informations sur les statistiques de recherche, voir statistiques de la [recherche](search-statistics.md).

- **Aperçu** : lorsque la recherche est terminée, vous pouvez afficher les éléments réels à partir d’un sous-ensemble des résultats de la recherche renvoyés par la recherche. Vous pouvez afficher dans l’affichage natif du type d’élément, mais vous pouvez également afficher les métadonnées relatives à l’élément. Il s’agit d’un moyen efficace pour déterminer rapidement si les résultats de la recherche sont ceux que vous attendiez ou si vous devez modifier la recherche et l’exécuter à nouveau. Cliquez sur **Aperçu** sur la page de menu volant pour afficher les éléments des résultats de la recherche. Ce bouton est inactif jusqu’à ce que la valeur de l' **État aperçu** sur l’onglet **recherches** soit définie sur **réussite**.
 
> [!NOTE]
> Les valeurs d’état des colonnes **État** de l’estimation et état de l' **Aperçu** de l’onglet **recherches** sont **envoyées**, **en cours**et **réussies**. S’il y a une erreur avec la recherche, l’état **échec** est affiché.

## <a name="add-search-results-to-evidence"></a>Ajouter des résultats de recherche à des preuves

Lorsque vous êtes satisfait des résultats d’une recherche et que vous êtes prêt à analyser et à corriger ces résultats de recherche, vous pouvez les ajouter à un ensemble de preuves lors de l’enquête. Lorsque vous ajoutez des éléments à un jeu de preuves sur l’onglet **preuve** , les trois événements suivants se produisent:

- La recherche est réexécutée et les derniers résultats de la recherche sont ajoutés à l’ensemble de preuves. Cela signifie que les éléments ajoutés à la preuve peuvent être différents des résultats de recherche estimés affichés sur la page flyout de recherche. Cela peut se produire si un certain temps s’est écoulé entre la dernière exécution de la recherche et le moment où vous avez ajouté les résultats de la recherche aux preuves.

- Tous les éléments des résultats de la recherche sont copiés à partir de la source de données dans le service actif et copiés dans un emplacement de stockage Azure sécurisé dans le Cloud Microsoft.

- Tous les éléments (y compris le contenu et les métadonnées) sont réindexés de sorte que toutes les données du jeu de preuves soient entièrement utilisables lors de votre enquête. La réindexation des données entraîne des recherches rapides et rapides lors de la recherche des données dans l’ensemble de preuves lors de votre enquête.

L’un des avantages de la copie des données actives dans un ensemble de preuves dans Azure est que pour les incidents urgents ou critiques, vous pouvez rapidement contenir les dommages en supprimant immédiatement le contenu suspect de la source de données d’origine dans le service actif, puis en examinant l’incident en analysant les preuves qui ont été copiées dans l’environnement en quarantaine de l’emplacement de stockage Azure. 

La copie des données d’origine dans l’ensemble de preuves facilite également votre enquête en vous fournissant des outils d’analyse avancés, tels que la détection de thèmes, la détection de proximité et l’identification des threads de messagerie.

Si nécessaire, vous pouvez également ajouter des données provenant de sources de données autres que Office 365 à un jeu de preuves afin qu’il soit stocké avec les données que vous collectez à partir d’Office 365.

Pour ajouter des données à un jeu de preuves, sélectionnez une recherche dans l’onglet **recherches** , puis cliquez sur **Ajouter des résultats à des preuves** sur la page de menu volant. Vous pouvez ajouter des données à un ensemble de preuves existant ou créer un ensemble de preuves à la volée.

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a>Suivi de la progression de l’ajout de résultats de recherche à des preuves

L’ajout de données à un jeu de preuves est un processus de longue durée. Le processus inclut la collecte des éléments de la source de données d’origine à partir d’Office 365 (par exemple, à partir de boîtes aux lettres et de sites), en les copiant vers ** l’emplacement de stockage Azure (ce processus de copie est également appelé «ingestion»), puis la réindexation des éléments. Vous pouvez suivre la progression sous l’onglet **travaux** ou sur l’onglet **recherches** dans la colonne **données ajoutées à la preuve** . Une fois le traitement du traitement des preuves terminé, vous pouvez accéder à l’onglet **preuve** , cliquer sur l’ensemble de preuves, puis lancer votre enquête en recherchant, examiner, Baliser et exporter les données pertinentes selon vos besoins.