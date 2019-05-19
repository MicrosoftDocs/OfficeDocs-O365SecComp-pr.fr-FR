---
title: Préparation des résultats de recherche pour la découverte électronique avancée Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: Découvrez comment préparer les résultats d’une recherche de contenu dans le centre de sécurité & Compliance Center dans Office 365 pour une analyse plus poussée avec l’outil eDiscovery avancé.
ms.openlocfilehash: 244fae317964261ad1eeadbdca2d4dffeda0a23a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157466"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Préparation des résultats de recherche pour la découverte électronique avancée Office 365

Une fois qu’une recherche associée à un cas eDiscovery dans le centre de sécurité & Compliance Center est exécutée correctement, vous pouvez préparer les résultats de la recherche pour une analyse plus poussée avec Office 365 Advanced eDiscovery, qui vous permet d’analyser des jeux de données non structurés volumineux et de réduire la quantité de données correspondant à un cas juridique. Les fonctionnalités avancées de découverte électronique sont les suivantes:
  
- **Reconnaissance optique de caractères** : lorsque vous préparez des résultats de recherche pour Advanced eDiscovery, la fonctionnalité de reconnaissance optique de caractères (OCR) extrait automatiquement le texte des images et inclut cela avec les résultats de recherche chargés dans Advanced eDiscovery pour analyse. La reconnaissance optique de caractères est prise en charge pour les fichiers libres, les pièces jointes et les images incorporées. Cela vous permet d’appliquer les fonctionnalités d’analyse textuelle de la découverte électronique avancée (quasi-doublons, du Threading de messagerie électronique, des thèmes et du codage prédictif) au contenu de texte dans les fichiers image. La reconnaissance optique des caractères eDiscovery avancée prend en charge les formats suivants pour les fichiers image:

    - GIF
    - JPEG
    - JPG
    - PNG
    - TIFF
    
- **Détection** des doublons: permet de structurer votre analyse des données de manière plus efficace, afin qu’une personne révise un groupe de documents similaires. Cela permet d’éviter que plusieurs relecteurs n’aient à afficher différentes versions du même document. 
    
- **Threading de messagerie** : vous permet d’identifier les messages uniques dans un thread de messagerie afin que vous puissiez vous concentrer uniquement sur les nouvelles informations de chaque message. Dans un thread de messagerie, le deuxième message contient le premier message. De même, les autres messages contiennent tous les messages précédents. Le Threading de messagerie supprime la nécessité d’examiner chaque message dans son intégralité dans un fil de messagerie. 
    
- **Themes** : vous aide à obtenir des informations précieuses sur vos données au-delà des statistiques de recherche par mot clé. Les thèmes facilitent les enquêtes en regroupant les documents associés pour vous permettre d’examiner les documents en contexte. Lorsque vous utilisez des thèmes, vous pouvez afficher les thèmes associés à un ensemble de documents, déterminer les chevauchements, puis identifier les sections des données connexes. 
    
- **Codage prédictif** : vous permet de former le système sur ce que vous recherchez, en vous permettant de prendre des décisions (de savoir si un élément est pertinent ou non) sur un petit ensemble de documents. Advanced eDiscovery applique ensuite cette formation (en fonction de vos conseils) lors de l’analyse de tous les documents du jeu de données. En fonction de cette formation, Advanced eDiscovery offre un classement de pertinence afin que vous puissiez décider des documents à examiner en fonction du document le plus susceptible d’être pertinent pour le cas. 
    
- **Exportation de données pour les applications de révision** : vous pouvez exporter des données à partir d’Advanced eDiscovery et d’Office 365 après avoir terminé votre analyse et réduit le jeu de données. Le package d’exportation inclut un fichier CSV qui contient les propriétés des métadonnées de contenu et d’analyse exportées. Ce package d’exportation peut ensuite être importé dans une application de consultation de découverte électronique. 
    
## <a name="before-you-begin"></a>Avant de commencer

- Pour analyser les données d’un utilisateur à l’aide de Advanced eDiscovery, l’utilisateur (le dépositaire des données) doit disposer d’une licence Office 365 E5. Par ailleurs, les utilisateurs disposant d’une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome. Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n’ont pas besoin d’une licence E5. 
    
- Vous devez être un gestionnaire eDiscovery ou un administrateur eDiscovery dans le centre de sécurité & Compliance Center pour préparer les résultats de recherche pour Advanced eDiscovery. Un gestionnaire de découverte électronique est membre du groupe de rôles Gestionnaire de découverte électronique. Un administrateur de découverte électronique est également membre du groupe de rôles Gestionnaire de découverte électronique, mais il bénéficie de privilèges de découverte électronique supplémentaires. Pour obtenir des instructions sur l’attribution d’autorisations d’administrateur eDiscovery, consultez l’étape 1 dans les [cas de découverte électronique](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>Étape 1: préparer les résultats de recherche pour Advanced eDiscovery

Vous pouvez préparer les résultats d’une recherche associée à un cas de découverte électronique. Lorsque vous préparez des résultats de recherche pour Advanced eDiscovery, les données sont téléchargées et stockées temporairement dans une zone de stockage Windows Azure unique dans le Cloud Microsoft. À ce stade, la fonctionnalité OCR extrait le texte des images dans les résultats de la recherche. À l' [étape 2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery), ce texte et les autres données de résultats de recherche sont chargés dans le cas de Advanced eDiscovery.
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas pour lequel vous souhaitez préparer les résultats de recherche pour l’analyse dans Advanced eDiscovery. 
    
3. Sur la page d' **Accueil** du cas, cliquez sur **Rechercher**, puis sélectionnez la recherche.
    
4. Dans le volet d’informations, sous **analyser les résultats avec Advanced eDiscovery**, cliquez sur **préparer les résultats pour l’analyse**.
    
    > [!NOTE]
    > Si les résultats de recherche datent d’il y a plus de 7 jours, vous serez invité à mettre à jour les résultats. 
  
5. Sur la page **Préparer les résultats pour analyse**, procédez comme suit :  
    
    - Choisissez de préparer des éléments indexés, des éléments indexés et non indexés, ou uniquement des éléments non indexés pour l’analyse dans Advanced eDiscovery.
    
    - Indiquez si vous souhaitez inclure toutes les versions des documents trouvés sur SharePoint qui répondent aux critères de recherche. Cette option apparaît uniquement si les sources de contenu pour la recherche incluent les sites.
    
    - Indiquez si vous souhaitez qu’un message de notification soit envoyé (ou copié) à une personne lorsque le processus de préparation est terminé et que les données sont prêtes à être traitées dans Advanced eDiscovery.
    
6. Cliquez sur **Préparer**.
    
    Les résultats de la recherche sont préparés pour analyse avec Advanced eDiscovery.
    
7. Dans le volet d’informations, cliquez sur **vérifier l’état de préparation** pour afficher des informations sur le processus de préparation. Une fois le processus de préparation terminé, vous pouvez passer à la case dans Advanced eDiscovery pour traiter les données pour analyse. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>Étape 2: ajouter les données de résultats de recherche au cas dans Advanced eDiscovery
<a name="step2"> </a>

Une fois la préparation terminée, l’étape suivante consiste à accéder à Advanced eDiscovery et à charger les données de résultats de recherche (qui ont été téléchargées vers une zone de stockage Azure dans le Cloud Microsoft) vers le cas dans Advanced eDiscovery. Comme expliqué précédemment, pour accéder à la découverte électronique avancée, vous devez être un administrateur eDiscovery dans le centre de sécurité & Compliance Center ou un administrateur dans Advanced eDiscovery.
  
> [!NOTE]
> Le temps nécessaire pour que les données du centre de sécurité Security & soient disponibles pour l’ajouter à un cas dans Advanced eDiscovery varie, en fonction de la taille des résultats de la recherche de découverte électronique. 
  
1. Dans le centre de sécurité & Compliance Center **** \> **** , cliquez sur eDiscovery eDiscovery pour afficher la liste des incidents de votre organisation. 
    
2. Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez charger les données dans Advanced eDiscovery. 
    
3. Sur la page **Accueil** du cas, cliquez sur **Advanced eDiscovery**. 
    
    ![Cliquez sur basculer vers Advanced eDiscovery pour ouvrir le cas dans Advanced eDiscovery](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    La barre **de progression de la connexion à Advanced eDiscovery** s’affiche. Lorsque vous êtes connecté à Advanced eDiscovery, une liste de conteneurs apparaît dans la page de configuration de l’incident. 
    
    ![Le cas est affiché dans Advanced eDiscovery](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Ces conteneurs représentent les résultats de recherche que vous avez préparés pour l’analyse dans Advanced eDiscovery à l’étape 1. Notez que le nom du conteneur porte le même nom que la recherche dans le cas dans le centre de sécurité & Compliance Center. Les conteneurs de la liste sont ceux que vous avez préparés. Si un autre utilisateur a préparé des résultats de recherche pour Advanced eDiscovery, les conteneurs correspondants ne seront pas inclus dans la liste. 
    
4. Pour charger les données de résultats de recherche à partir d’un conteneur dans le cas dans Advanced eDiscovery, sélectionnez un conteneur, puis cliquez sur **traiter**.
    
## <a name="next-steps"></a>Étapes suivantes

Une fois que les résultats d’une recherche de découverte électronique sont ajoutés à un cas, l’étape suivante consiste à utiliser les outils avancés de découverte électronique pour analyser les données et identifier le contenu réactif à un cas juridique spécifique. Pour plus d’informations sur l’utilisation d’Advanced eDiscovery, voir [Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md).
  
## <a name="more-information"></a>Plus d’informations

Tous les messages électroniques chiffrés RMS inclus dans les résultats de la recherche seront déchiffrés lors de leur préparation pour analyse dans Advanced eDiscovery. Cette fonctionnalité de déchiffrement est activée par défaut pour les membres du groupe de rôles gestionnaire de découverte électronique. Cela est dû au fait que le rôle de gestion de déchiffrement RMS est affecté à ce groupe de rôles. Gardez les points suivants à l’esprit concernant le déchiffrement des messages électroniques:
  
- Actuellement, cette fonctionnalité de déchiffrement n’inclut pas le contenu chiffré de sites SharePoint et OneDrive entreprise. Seuls les messages électroniques chiffrés RMS seront déchiffrés lors de leur exportation.
    
- Si un message électronique chiffré RMS comporte une pièce jointe (par exemple, un document ou un autre message électronique) qui est également chiffrée, seul le message électronique de niveau supérieur est déchiffré.
    
- Si vous devez empêcher quelqu’un de déchiffrer des messages chiffrés RMS lors de la préparation des résultats de recherche pour analyse dans Advanced eDiscovery, vous devez créer un groupe de rôles personnalisé (en copiant le groupe de rôles intégré du gestionnaire eDiscovery), puis supprimer le RMS Déchiffrer le rôle de gestion du groupe de rôles personnalisé. Ajoutez ensuite la personne dont vous ne voulez pas déchiffrer les messages en tant que membre du groupe de rôles personnalisé.
