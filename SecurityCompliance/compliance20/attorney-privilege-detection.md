---
title: Configuration de la détection des droits du client dans Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835064"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a>Configuration de la détection des privilèges client (préversion) dans Advanced eDiscovery

Un aspect majeur et coûteux de la partie révision de n’importe quel processus de découverte est l’analyse du contenu privilégié. Advanced eDiscovery offre une détection des contenus privilégiés dans votre cas afin que vous puissiez améliorer l’efficacité de ce processus. Dans la mesure où cette fonctionnalité est actuellement en version bêta, un administrateur eDiscovery doit s’abonner à la fonctionnalité pour l’utiliser.

## <a name="how-does-it-work"></a>Comment fonctionne-t-il ?

Lorsque la fonctionnalité est activée, lorsque vous analysez un jeu de révision dans un cas, tous les documents sont exécutés par le biais du modèle de détection des privilèges du client avocat. Le modèle examine les deux éléments suivants:

- Contenu: le modèle ML détermine la probabilité que le contenu du document soit légal.

- Participants: s’il existe une liste d’avocats téléchargés par l’utilisateur pour le client, le modèle compare les participants du document à la liste afin de déterminer si le document a au moins un participant à un avocat.
Le modèle génère trois valeurs pour chaque document, qui seront toutes recherchées dans un ensemble de révision:

- Score de contenu: probabilité que le document soit de nature légale (score compris entre 0 et 1)

- A avocat: true si l’un des participants se trouve dans la liste des avocats chargés, false dans le cas contraire ou s’il n’y a pas de liste d’avocats.

-  Potentiellement privilégié: vrai si le score de contenu est supérieur au seuil ou a un participant à un avocat, faux dans le cas contraire.

## <a name="opting-into-attorney-client-privilege-detection"></a>Préversion de la détection des privilèges client

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a>Étape 1: s’abonner à avocat-détection des privilèges client (administrateur eDiscovery)

Étant donné que la détection des privilèges du client est une fonctionnalité d’aperçu, votre administrateur eDiscovery doit s’abonner pour que la fonctionnalité soit disponible dans vos cas.

- Accédez à «configurer les fonctionnalités expérimentales» à partir de la page Advanced eDiscovery.

- Cliquez sur «gérer la détection de droits client».

- Cliquez sur le bouton bascule pour activer la fonctionnalité.

### <a name="step-2-upload-a-list-of-attorneys-optional"></a>Étape 2: télécharger une liste d’avocats (facultatif)

Pour tirer pleinement parti de la détection des privilèges du client pour les avocats, nous vous recommandons de fournir une liste des adresses de messagerie des avocats ou des personnes morales qui travaillent pour la société. La liste doit être un CSV sans en-tête, avec une adresse de messagerie par ligne.

## <a name="leveraging-attorney-client-privilege-detection"></a>Exploitation de la détection de privilèges client 

### <a name="step-1-analyze-a-review-set"></a>Étape 1: analyser un jeu de révision

Lorsque vous analysez votre jeu de révision, la détection des privilèges du client est également exécutée. Pour en savoir plus sur l’analyse des données dans l’ensemble de révision, reportez-vous à [analyser les données d’un jeu de vérification dans Advanced eDiscovery](analyzing-data-in-review-set.md).

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a>Étape 2: créer un groupe de balises actives avec le modèle de détection de privilège client

L’utilisation d’un groupe de balises actives est l’une des principales façons dont vous pouvez utiliser les résultats de la détection des droits du client dans votre processus de révision. Les groupes de balises actives prennent les résultats d’un modèle ML et affichent les résultats du modèle en ligne en regard des balises, afin que vous puissiez facilement utiliser les résultats du modèle, le cas échéant, et utiliser les balises dans votre processus de révision comme vous le feriez avec d’autres balises dans votre panneau de marquage.

- Dans «gérer les balises», cliquez sur «Ajouter une balise».

- Sélectionnez «avocat-détection des privilèges client». Vous verrez qu’un groupe de balises et deux balises, correspondant aux résultats possibles du modèle, ont été créés.

- Renommez le groupe de balises et les balises comme vous le jugez adapté à votre révision.

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a>Étape 3: utiliser le groupe de balises actives pour la révision des privilèges

Lorsque vous examinez un document, si le modèle a déterminé que le document est potentiellement privilégié, la balise active correspondante expose le résultat:

- Si le contenu du document peut être légal, une étiquette «contenu légal» apparaît en regard de la balise active correspondante.

- Si le document a un participant qui se trouve dans la liste des avocats téléchargés, une étiquette «avocat» apparaît en regard de la balise active correspondante.