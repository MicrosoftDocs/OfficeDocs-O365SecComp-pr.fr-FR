---
title: Configuration de la détection des droits du client dans Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: Abonnez-vous et utilisez le modèle de détection des privilèges du client avocat pour utiliser la détection basée sur l’apprentissage automatique du contenu privilégié lors de l’examen du contenu dans un cas avancé de découverte électronique.
ms.openlocfilehash: 16a6a215484c35d20fbe071cac033133270b7ea6
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703868"
---
# <a name="set-up-attorney-client-privilege-detection-in-advanced-ediscovery"></a>Configuration de la détection des droits du client dans Advanced eDiscovery

Un aspect majeur et coûteux de la phase de révision d’un processus eDiscovery consiste à examiner des documents pour le contenu privilégié. Advanced eDiscovery offre une fonctionnalité de détection de contenu privilégié basée sur l’apprentissage d’un ordinateur pour améliorer l’efficacité de ce processus. Cette fonctionnalité est appelée *détection des privilèges client*.

> [!NOTE]
> Vous devez vous inscrire au modèle de détection des privilèges du client avocat avant de pouvoir l’utiliser. Reportez-vous à l' [étape 1](#step-1-opt-in-to-attorney-client-privilege-detection) pour obtenir des instructions.

## <a name="how-does-it-work"></a>Comment fonctionne-t-il ?

Lorsque la détection de privilèges client est activée, tous les documents d’un ensemble de révision sont traités par le modèle de détection de privilège du client avocat lors de l' [analyse des données](analyzing-data-in-review-set.md) dans l’ensemble de révision. Le modèle recherche deux éléments:

- Contenu privilégié: le modèle utilise l’apprentissage automatique d’ordinateur pour déterminer si le document contient du contenu juridique.

- Participants: dans le cadre de la configuration de la détection des privilèges client, vous devez soumettre une liste d’avocats pour votre organisation. Le modèle compare ensuite les participants du document à la liste des avocats afin de déterminer si un document a au moins un participant à un avocat.

Le modèle produit les trois propriétés suivantes pour chaque document:

- **AttorneyClientPrivilegeScore** – la probabilité que le document soit juridique; les valeurs du score sont comprises entre **0** et **1**.

- **HasAttorney** : cette propriété est définie sur **true** si l’un des participants du document est répertorié dans la liste des avocats; Sinon, la valeur **** est false. La valeur est également définie sur **false** si votre organisation n’a pas téléchargé de liste d’avocats.

- **IsPrivilege** : cette propriété est définie sur **true** si la valeur de **AttorneyClientPrivilegeScore** est supérieure au seuil *ou* si le document a un participant à un avocat; Sinon, la valeur est définie **** sur false.

Ces propriétés (et leurs valeurs correspondantes) sont ajoutées aux métadonnées de fichier des documents dans un jeu de révision, comme illustré dans la capture d’écran suivante:

![Avocat-propriétés du privilège client affichées dans les métadonnées de fichier](../media/AeDAttorneyClientPrivilegeMetadata.png)

Ces trois propriétés peuvent également faire l’objet d’une recherche dans un jeu de révision. Pour plus d’informations, reportez-vous à [la rubrique Query the Data in a Review Set](review-set-search.md).

## <a name="set-up-the-attorney-client-privilege-detection-model"></a>Configurer le modèle de détection de privilèges client pour les avocats

Pour activer le modèle de détection des privilèges du client avocat, votre organisation doit s’abonner, puis télécharger une liste d’avocats.

### <a name="step-1-opt-in-to-attorney-client-privilege-detection"></a>Étape 1: Abonnez-vous à avocat-détection des privilèges client

Comme indiqué précédemment, le modèle de détection des privilèges du client avocat est en préversion. Par conséquent, une personne de votre administrateur eDiscovery de votre organisation (membre du sous-groupe administrateur eDiscovery dans le groupe de rôles gestionnaire eDiscovery) doit s’inscrire pour que le modèle soit disponible dans vos cas de découverte électronique avancée.

1. Dans le centre de sécurité & conformité, accédez à **ediscovery > Advanced eDiscovery**.

2. Sur la page d’accueil de la **découverte électronique avancée** , dans la vignette **paramètres** , cliquez sur **configurer les fonctionnalités expérimentales**.

   ![Cliquez sur «configurer les fonctionnalités expérimentales»](../media/AeDExperimentalFeatures.png)

3. Sous l’onglet **fonctionnalités expérimentales** , cliquez sur **gérer le paramètre de privilège du client**.

4. Sur la page menu **déroulant avocat-client** , cliquez sur le bouton bascule pour activer la fonctionnalité, puis cliquez sur **Enregistrer**.

### <a name="step-2-upload-a-list-of-attorneys-optional"></a>Étape 2: télécharger une liste d’avocats (facultatif)

Pour tirer pleinement parti du modèle de détection des privilèges du client avocat et utiliser les résultats de l’offre d’un **avocat** ou d’une détection **potentiellement privilégiée** qui a été décrite précédemment, nous vous recommandons de télécharger une liste d’adresses de messagerie pour le les avocats et le personnel juridique qui travaillent pour votre organisation. 

Pour télécharger une liste d’avocats à utiliser par le modèle de détection de privilège du client:

1. Créez un fichier. csv (sans ligne d’en-tête) et ajoutez l’adresse de messagerie de chaque personne appropriée sur une ligne distincte. Enregistrez ce fichier sur votre ordinateur local.

2. Sur la page d’accueil de la **découverte électronique avancée** , dans la vignette **paramètres** , cliquez sur **configurer les fonctionnalités expérimentales**, puis cliquez sur **gérer le paramètre de privilège du client**.

   La page de **privilège avocat-client** s’affiche et le bouton bascule de **détection de privilège client** est activé.

   ![Page de menu déroulant avocat-privilège client](../media/AeDUploadAttorneyList.png)

3. Cliquez sur **Parcourir** , puis recherchez et sélectionnez le fichier. csv que vous avez créé à l’étape 1.

4. Cliquez sur **Enregistrer** pour télécharger la liste des avocats.

## <a name="use-the-attorney-client-privilege-detection-model"></a>Utiliser le modèle de détection des privilèges du client avocat

Suivez les étapes de cette section pour utiliser la détection des privilèges du client avocat pour les documents dans un ensemble de révision.

### <a name="step-1-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a>Étape 1: créer un groupe de balises actives avec le modèle de détection de privilège client

L’utilisation d’un groupe de balises actives est l’une des principales façons de voir les résultats de la détection des droits du client dans votre processus de révision. Un groupe de balises actives indique les résultats de la détection de privilège au client et affiche les résultats en ligne en regard des balises dans un groupe de balises actives. Cela vous permet d’identifier rapidement des documents potentiellement privilégiés lors de la révision d’un document. En outre, vous pouvez également utiliser les balises dans le groupe de balises actives pour marquer des documents comme étant privilégiés ou non privilégiés. Pour plus d’informations sur les balises actives, voir [configurer les balises actives dans Advanced eDiscovery](smart-tags.md).

1. Dans l’ensemble de révision qui contient les documents que vous avez analysés à l’étape 1, cliquez sur **gérer le jeu** de réexamens, puis sur **gérer**les balises.
 
2. Sous **balises**, cliquez sur le menu déroulant en regard de **Ajouter un groupe** , puis cliquez sur Ajouter un groupe de **balises actives**.

   ![Cliquez sur Ajouter un groupe de balises actives.](../media/AeDCreateSmartTag.png)

3. Sur la page **choisir un modèle pour la balise active** , cliquez sur Sélectionner en regard de l' **option** **avocat-privilège client**.

   Un groupe de balises nommé **avocat-le privilège client** s’affiche. Il contient deux balises enfants nommées **positive** et **Negative**, qui correspondent aux résultats possibles produits par le modèle.

   ![Groupe de balises actives de privilège de client pour les avocats](../media/AeDAttorneyClientSmartTagGroup.png)

3. Renommez le groupe de balises et les balises en fonction de votre révision. Par exemple, vous pouvez renommer **positif** sur **privilégié** et **négatif** sur **non privilégié**.

### <a name="step-2-analyze-a-review-set"></a>Étape 2: analyser un jeu de révision

Lorsque vous analysez les documents dans un ensemble de vérification, le modèle de détection des privilèges du client avocat est également exécuté et les propriétés correspondantes (décrites dans[How do it Work?](#how-does-it-work) sont ajoutées à chaque document dans l’ensemble de révision. Pour plus d’informations sur l’analyse des données dans l’ensemble de validation, voir [analyze Data in a Review Set in Advanced eDiscovery](analyzing-data-in-review-set.md).

### <a name="step-3-use-the-smart-tag-group-for-review-of-privileged-content"></a>Étape 3: utiliser le groupe de balises actives pour vérifier le contenu privilégié

Après avoir analysé l’ensemble de révision et configuré les balises actives, l’étape suivante consiste à passer en revue les documents. Si le modèle a déterminé que le document est potentiellement privilégié, la balise active correspondante dans le **panneau balisage** indique les résultats suivants générés par la détection des privilèges du client avocat:

- Si le contenu du document peut être légal, le **contenu légal** de l’étiquette est affiché en regard de la balise active correspondante (dans ce cas, il s’agit de la balise **positive** par défaut).

- Si le document a un participant trouvé dans la liste des avocats de votre organisation, le **juriste** est affiché en regard de la balise active correspondante (dans ce cas, il s’agit également de la balise **positive** par défaut).

- Si le document a un contenu qui peut être légal *et* qui a un participant trouvé dans la liste des avocats, les étiquettes de **contenu juridique** et d' **avocat** sont affichées. 

Si le modèle détermine qu’un document ne contient pas de contenu légal ou qu’il ne contient pas de participant à partir de la liste des avocats, aucune étiquette n’est affichée dans le panneau balisage.

Par exemple, les captures d’écran suivantes illustrent deux documents; le premier contient un contenu légal et un participant figurant dans la liste des avocats;. la seconde ne contient pas et, par conséquent, n’affiche aucune étiquette.

![Document avec les étiquettes d’avocat et de contenu juridique](../media/AeDTaggingPanelLegalContentAttorney.png)

![Document sans étiquette](../media/AeDTaggingPanelNegative.png)

Après avoir examiné un document pour voir s’il contient du contenu privilégié, vous pouvez le marquer avec la balise appropriée.