---
title: Configuration des balises actives dans Advanced eDiscovery
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
description: Les balises actives vous permettent d’appliquer les fonctionnalités d’apprentissage automatique lors de la révision du contenu dans un cas avancé de découverte électronique. Utilisez des groupes de balises actives pour afficher les résultats des modèles de détection d’apprentissage automatique, tels que le modèle de privilège avocat-client.
ms.openlocfilehash: 68b558cc2282cc388387f8d61825b9ee569ff32a
ms.sourcegitcommit: e323610df2df71c84f536e8a38650d33d8069e41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34703827"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a>Configuration des balises actives dans Advanced eDiscovery

Les fonctionnalités machine learning (ML) dans Advanced eDiscovery peuvent vous aider à améliorer l’efficacité du processus de décision lors de la révision de documents de cas dans un jeu de révision. Les balises actives permettent de mettre en place les capacités de ML des décisions enregistrées: lors du marquage des documents lors de la révision. Lorsque vous créez un groupe de balises actives, les décisions qui sont le résultat du modèle ML que vous avez associé au groupe de balises actives s’affichent en ligne avec les balises dans le groupe de balises. Cela permet d’afficher les informations de résultats ML en ligne lorsque vous examinez des documents spécifiques.

## <a name="how-to-set-up-a-smart-tag-group"></a>Procédure de configuration d’un groupe de balises actives

1. Dans un jeu de révision, cliquez sur **gérer le jeu de révision** , puis sur gérer les **balises**.

2. Cliquez sur **Ajouter un groupe** de balises, puis sélectionnez **Ajouter un groupe de balises actives**.

3. Sélectionnez le modèle ML que vous souhaitez associer au groupe de balises.
    
   Cette méthode crée un groupe de balises et *n* balises enfants, où *n* représente le nombre de sorties possibles du modèle. Par exemple, le [modèle de détection des privilèges du client avocat](attorney-privilege-detection.md) a deux sorties possibles: 

   - **Positif** : permet de baliser des documents qui contiennent du contenu privilégié par le client.
   
   - **Négatif** : permet de marquer des documents qui ne contiennent pas de contenu privilégié par le client.
    
    Si vous sélectionnez ce modèle, un groupe de balises avec deux balises enfant est créé (une balise enfant nommée **positive** et l’autre appelée **négatif**) pour l’ensemble de révision. Dans cet exemple, chaque balise enfant correspond à l’une des sorties possibles du modèle de détection des privilèges du client avocat.

4. Vous pouvez également renommer le groupe de balises et les balises enfants. Par exemple, vous pouvez renommer la balise **positive** en **Privilege** et la balise **négative** pour **ne pas**obtenir de privilèges.

## <a name="how-to-use-smart-tags"></a>Utilisation des balises actives

Lors de l’examen d’un document, les résultats du modèle sont affichés en regard de la balise enfant appropriée. Par exemple, si vous disposez d’un groupe de balises actives pour la détection des privilèges du client et que vous révisez un document potentiellement privilégié, la raison de cette conclusion s’affiche en regard de la balise appropriée. Il est important de noter que la balise n’est pas automatiquement appliquée au document. Le relecteur prend la décision de baliser le document.