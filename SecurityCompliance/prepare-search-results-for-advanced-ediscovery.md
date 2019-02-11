---
title: Préparation des résultats de recherche pour la découverte électronique avancée Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportWithZoom
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0b6fac2d-8627-4b05-9df0-03609db6248b
description: Découvrez comment préparer les résultats d’une recherche de contenu de sécurité Office 365 &amp; centre de conformité pour une analyse approfondie avec l’outil de découverte électronique avancées.
ms.openlocfilehash: c70eec691359170ae67e431f20e3b8ad389443f3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "27280167"
---
# <a name="prepare-search-results-for-office-365-advanced-ediscovery"></a>Préparation des résultats de recherche pour la découverte électronique avancée Office 365

Après une recherche qui est associé à un cas de découverte électronique de sécurité Office 365 &amp; centre de conformité est exécutée avec succès, vous pouvez préparer les résultats de recherche pour une analyse approfondie avec Office 365 avancée eDiscovery, qui vous permet d’analyser de grande taille, données non structurées définit et réduisent la quantité de données qui s’appliquent à une affaire juridique. Fonctionnalités de découverte électronique avancées sont les suivantes :
  
- **Reconnaissance optique de caractères** - lorsque vous préparez les résultats de la recherche avancée eDiscovery, les fonctionnalités de reconnaissance optique de caractères (OCR) automatiquement extrait le texte à partir d’images et cela inclut avec les résultats de recherche qui sont chargées dans EDiscovery avancée pour l’analyse. Reconnaissance optique de caractères est pris en charge pour les fichiers à part, pièces jointes et des images incorporées. Cela vous permet d’appliquer les fonctionnalités d’analyse texte d’eDiscovery avancée (près de doublons, messagerie threading, thèmes et codage prédictive) au contenu de texte dans des fichiers image. Découverte avancée OCR prend en charge les formats suivants pour les fichiers image :

    - GIF
    - JPEG
    - JPG
    - PNG
    - TIFF
    
- **Détection de proximité double** - vous permet de structurer votre passer en revue les données de manière plus efficace, pour une personne révise un groupe de documents similaires. Cela permet d’éviter que plusieurs relecteurs d’avoir à afficher les différentes versions du même document. 
    
- **Courrier électronique threading** - permet d’identifier les messages dans un thread de messagerie uniques afin de vous concentrer sur les nouvelles informations de chaque message. Dans un thread de messagerie, le deuxième message contient le premier message. De même, les messages ultérieures contiennent tous les messages précédents. Messagerie threading supprime le besoin pour passer en revue chaque message dans son intégralité dans un thread de messagerie. 
    
- **Thèmes** - aider précieuses sur vos données au-delà uniquement les statistiques de recherche de mots clés. Thèmes aident enquêtes en regroupant les documents connexes afin que vous pouvez examiner les documents dans le contexte. Lors de l’utilisation des thèmes, vous pouvez afficher les thèmes associés pour un ensemble de documents, déterminer tout chevauchement et identifier puis coupes de données connexes. 
    
- **Codage une prédictive** - vous permet de former le système sur ce que vous cherchez, en vous permettant de prendre des décisions (si un élément est pertinent ou non) sur un petit jeu de documents. Découverte avancée puis applique cette formation (en fonction de vos conseils) lors de l’analyse tous les documents dans le jeu de données. En fonction de cette formation, eDiscovery avancée fournit un classement de pertinence afin de choisir les documents pour passer en revue basé sur le document sont les plus susceptibles d’être pertinent pour le cas. 
    
- **Exportation de données pour revue les applications** : vous pouvez exporter des données à partir de découverte avancée et Office 365 après avoir terminé votre analyse et réduit le jeu de données. Le package d’exportation inclut un fichier CSV qui contient les propriétés des métadonnées analytique contenu exporté. Ce package d’exportation peut ensuite être importé à une application de passer en revue les eDiscovery. 
    
## <a name="before-you-begin"></a>Avant de commencer

- Pour analyser les données d’un utilisateur à l’aide de la découverte électronique avancée, l’utilisateur (le dépositaire des données) doit être affecté à une licence Office 365 E5. Autrement, les utilisateurs possédant une licence Office 365 E1 ou E3 peuvent être affectés à une licence autonome de découverte avancée. Les administrateurs et des agents de conformité qui sont affectées à des cas et utilisent eDiscovery avancée pour analyser des données inutile d’une licence E5. 
    
- Vous devez être un gestionnaire eDiscovery ou une administrateur de sécurité Office 365 eDiscovery &amp; centre de conformité pour préparer les résultats de la recherche avancée eDiscovery. Un gestionnaire eDiscovery est un membre du groupe de rôles gestionnaire eDiscovery. Une découverte électronique administrateur est également membre du groupe de rôles gestionnaire eDiscovery, mais a été affecté privilèges eDiscovery supplémentaires. Pour obtenir des instructions sur l’attribution d’autorisations d’administrateur eDiscovery, voir Step 1 dans [les cas eDiscovery dans le centre de conformité de & Office 365 sécurité](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).
    
## <a name="step-1-prepare-search-results-for-advanced-ediscovery"></a>Étape 1 : Préparation de résultats pour la découverte avancée de la recherche

Vous pouvez préparer les résultats de recherche qui est associé à une affaire eDiscovery. Lorsque vous préparez des résultats de la recherche avancée eDiscovery, les données sont téléchargées et temporairement stockées dans une zone de stockage unique Windows Azure dans le nuage Microsoft. Il est à ce stade que la fonctionnalité de reconnaissance optique de caractères extrait le texte à partir d’images dans les résultats de recherche. Dans [l’étape 2](#step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery), ce texte et l’autre recherche résultats chargement des données dans le cas d’eDiscovery avancée.
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez préparer des résultats de recherche pour l’analyse d’eDiscovery avancée, cliquez sur **Ouvrir** . 
    
3. Dans la page **d’accueil** pour le cas, cliquez sur **Rechercher**, puis sélectionnez la recherche.
    
4. Dans le volet de détails, sous **analyse les résultats avec eDiscovery avancée**, cliquez sur **préparer les résultats d’analyse**.
    
    > [!NOTE]
    > Si les résultats de recherche datent d’il y a plus de 7 jours, vous serez invité à mettre à jour les résultats. 
  
5. Sur la page **Préparer les résultats pour analyse**, procédez comme suit :  
    
    - Choisissez cette option préparer les éléments indexés, les éléments indexés et non indexés ou uniquement les éléments non indexés pour l’analyse d’eDiscovery avancée.
    
    - Choisissez s’il faut inclure toutes les versions des documents que qui se trouvés dans SharePoint qui répondait aux critères de recherche. Cette option apparaît uniquement si les sources de contenu pour la recherche inclut les sites.
    
    - Spécifiez si un message de notification envoyé (ou copié) à une personne lorsque le processus de préparation terminé et les données sont prêtes à être traitée d’eDiscovery avancée.
    
6. Cliquez sur **Préparer**.
    
    Les résultats de recherche sont préparés pour l’analyse de découverte électronique avancée.
    
7. Dans le volet détails, cliquez sur **vérifier l’état de préparation** pour afficher des informations sur le processus de préparation. Une fois le processus de préparation terminé, vous pouvez passer au cas d’eDiscovery avancée pour traiter les données d’analyse. 
    
## <a name="step-2-add-the-search-results-data-to-the-case-in-advanced-ediscovery"></a>Étape 2 : Ajouter des données de résultats de recherche pour le cas d’eDiscovery avancée
<a name="step2"> </a>

Une fois la préparation terminée, l’étape suivante consiste accéder à eDiscovery avancée et charger les données de résultats de recherche (qui ont été téléchargées dans une zone de stockage Azure dans le cloud Microsoft) pour le cas d’eDiscovery avancée. Expliqué précédemment, pour accéder aux eDiscovery avancé, vous devez être une administrateur de la sécurité eDiscovery &amp; centre de conformité ou un administrateur d’eDiscovery avancée.
  
> [!NOTE]
> Le temps nécessaire pour les données à partir de la sécurité &amp; centre de conformité soit disponible pour l’ajouter à un cas de découverte électronique avancée varie selon la taille des résultats de la recherche de découverte électronique. 
  
1. Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation. 
    
2. En regard de la casse que vous souhaitez charger des données dans eDiscovery avancée, cliquez sur **Ouvrir** . 
    
3. Sur la page **Accueil** du cas, cliquez sur **Advanced eDiscovery**. 
    
    ![Cliquez sur Basculer en découverte avancée pour ouvrir le cas de découverte électronique avancée](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    La barre de progression **se connectant à la découverte électronique avancé** s’affiche. Lorsque vous êtes connecté à la découverte électronique avancée, une liste de conteneurs s’affiche dans la page du programme d’installation pour le cas. 
    
    ![Le cas est affiché dans la découverte électronique avancée](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     Ces conteneurs représentent les résultats de recherche que vous avez préparé pour l’analyse d’eDiscovery avancé à l’étape 1. Notez que le nom du conteneur a le même nom que la recherche dans le cas de la sécurité &amp; centre de conformité. Les conteneurs dans la liste sont ceux que vous avez préparé. Si un autre utilisateur préparé les résultats de la recherche avancée eDiscovery, les conteneurs correspondants ne sont pas inclus dans la liste. 
    
4. Pour charger les données de résultats de recherche à partir d’un conteneur pour le cas d’eDiscovery avancée, sélectionnez un conteneur, puis cliquez sur **le processus**.
    
## <a name="next-steps"></a>Étapes suivantes

Une fois les résultats d’une découverte électronique recherche sont ajoutés à un cas, l’étape suivante consiste à utiliser les outils de découverte électronique avancées pour analyser les données et d’identifier le contenu qui répond à une affaire juridique spécifique. Pour plus d’informations sur l’utilisation de découverte électronique avancée, voir [eDiscovery Office 365 avancés](office-365-advanced-ediscovery.md).
  
## <a name="more-information"></a>Plus d’informations

Tous les messages électroniques chiffrés RMS qui sont inclus dans les résultats de recherche sont déchiffrées lorsque les préparer pour l’analyse d’eDiscovery avancée. Cette fonctionnalité de déchiffrement est activée par défaut pour les membres du groupe de rôles gestionnaire eDiscovery. Il s’agit, car le rôle de gestion de déchiffrement RMS est affecté à ce groupe de rôles. Gardez les éléments suivants à l’esprit déchiffrement des messages électroniques :
  
- Actuellement, cette fonctionnalité de déchiffrement n’inclut pas le contenu chiffré à partir de SharePoint et OneDrive pour les sites. Seuls les messages électroniques chiffrés RMS sont déchiffrées lorsque vous exportez les.
    
- Si un message électronique chiffré RMS comporte une pièce jointe (comme un document ou un autre message électronique) qui est également chiffrée, est déchiffré uniquement le premier message.
    
- Si vous devez empêcher quelqu'un de le déchiffrement des messages chiffrés RMS lors de la préparation des résultats de recherche pour l’analyse d’eDiscovery avancé, vous devrez créer un groupe de rôles personnalisés (en copiant l’eDiscovery intégrée groupe de rôle de gestionnaire), puis supprimer le serveur RMS Déchiffrer le rôle de gestion du groupe de rôles personnalisé. Puis ajoutez la personne que vous ne souhaitez pas déchiffrer des messages en tant que membre du groupe de rôles personnalisé.
