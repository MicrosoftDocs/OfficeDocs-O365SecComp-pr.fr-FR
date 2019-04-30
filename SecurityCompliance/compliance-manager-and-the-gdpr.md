---
title: Gestionnaire de conformité Microsoft et RGPD
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Le gestionnaire de conformité Microsoft est un outil d'évaluation des risques gratuit basé sur un flux de travail dans le portail d'approbation de service Microsoft. Le gestionnaire de conformité vous permet de suivre, d'affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.
ms.openlocfilehash: 10579edea5a36686b8b19cafd9d3d6e148cfdcd3
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473066"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a>Gestionnaire de conformité Microsoft et RGPD

Le règlement général sur la protection des données (RGPD) mis en oeuvre par l'Union européenne peut influer sur la stratégie de conformité et les actions requises pour gérer les informations utilisateur et client utilisées dans le gestionnaire de conformité.

## <a name="user-privacy-settings"></a>Paramètres de confidentialité de l’utilisateur

Dans certaines réglementations, une organisation doit être en mesure de supprimer les données d'historique de l'utilisateur. Le gestionnaire de conformité fournit des fonctions de **paramètres de confidentialité** de l'utilisateur qui permettent aux administrateurs:
  
- [Rechercher un utilisateur](#search-for-a-user)
- [Exporter le rapport de l’historique des données d’un compte](#export-a-report-of-account-data-history)
- [Supprimer l’historique des données d’un utilisateur](#delete-user-data-history)
  
## <a name="search-for-a-user"></a>Rechercher un utilisateur

Pour rechercher un compte d’utilisateur :
  
1. Entrez l'alias de messagerie de l'utilisateur (les informations à gauche du symbole @) et choisissez le nom de domaine dans la liste de suffixe de domaine à droite. Pour les organisations disposant de plusieurs domaines inscrits, vérifiez que le suffixe du nom de domaine est correct.

2. Une fois le nom d'utilisateur correctement entré, sélectionnez **recherche**.

3. Pour les comptes d'utilisateur qui ne sont pas renvoyés, le message «utilisateur introuvable» s'affiche sur la page. Vérifiez les informations de l'adresse de messagerie de l'utilisateur et effectuez les corrections nécessaires. Pour réessayer, sélectionnez **recherche**.

4. Pour les comptes d'utilisateur renvoyés, le texte du bouton passe de la **recherche** à **Effacer**. Cela indique que le compte d'utilisateur renvoyé est le contexte d'exploitation pour les fonctions supplémentaires et que ces fonctions s'appliquent à ce compte d'utilisateur.

5. Pour effacer les résultats de la recherche et Rechercher un autre utilisateur, sélectionnez **Effacer**.

## <a name="export-a-report-of-account-data-history"></a>Exporter le rapport de l’historique des données d’un compte

Pour chaque compte d'utilisateur identifié, vous pouvez générer un rapport des dépendances liées à ce compte. Ces informations vous permettent de réaffecter des éléments d'action ouverts ou de vous assurer de l'accès à des preuves précédemment téléchargées.
  
 Pour générer et exporter un rapport :
  
1. Sélectionnez **Exporter** pour générer et télécharger un rapport des éléments d'action de contrôle du gestionnaire de conformité actuellement attribués au compte d'utilisateur renvoyé, ainsi que la liste des documents téléchargés par cet utilisateur. S'il n'y a pas d'actions affectées ou de documents téléchargés, un message d'erreur indique «pas de données pour cet utilisateur».

2. Le rapport est téléchargé en arrière-plan de la fenêtre active du navigateur — si vous ne voyez pas de menu contextuel de téléchargement dans lequel vous souhaitez vérifier l'historique de téléchargement de votre navigateur.

3. Ouvrez le document pour consulter les données du rapport.

> [!IMPORTANT]
> Il ne s'agit pas d'un rapport d'historique qui conserve et affiche les modifications d'État apportées à l'historique des affectations d'éléments d'action. Le rapport généré est une capture instantanée des éléments d'action de contrôle affectés lors de l'exécution du rapport (horodatage écrit dans le rapport). Par exemple, toute réaffectation ultérieure d'éléments d'action entraîne des données de rapport de capture instantanée différentes si ce rapport est de nouveau généré pour le même utilisateur.
  
## <a name="delete-user-data-history"></a>Supprimer l’historique des données d’un utilisateur

Définit tous les éléments d'action de contrôle affectés à l'utilisateur renvoyé comme étant «non attribué». Définit la valeur **chargée par** pour tous les documents téléchargés par l'utilisateur retourné sur «utilisateur supprimé».
  
Pour supprimer l'élément d'action du compte d'utilisateur et l'historique de chargement des documents:
  
1. Sélectionnez **supprimer**.

    Une boîte de dialogue de confirmation s'affiche: «*cette option supprime toutes les affectations d'éléments d'action de contrôle et l'historique de téléchargement de documents de l'utilisateur sélectionné. Cette action est permanente. Êtes-vous sûr de vouloir continuer?*

2. Pour continuer, sélectionnez **OK**, sinon cliquez sur **Annuler**.