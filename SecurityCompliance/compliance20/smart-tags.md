---
title: Configuration des balises actives pour l’identification de la détection des privilèges client dans Advanced eDiscovery
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
ms.openlocfilehash: 721426f23aec862bcefbd13b8e61415dac3aeb27
ms.sourcegitcommit: aa8ea45d5854f8906714e0a407937585ec7993ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33951697"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a>Configuration des balises actives pour une révision assistée par ML dans Advanced eDiscovery

Les fonctionnalités d’apprentissage automatique dans Advanced eDiscovery sont destinées à faciliter le processus de décision sur les documents. Les balises actives permettent de mettre en place les fonctionnalités d’apprentissage automatique dans l’emplacement où sont enregistrées les décisions: les balises et les groupes de balises. Lorsque vous créez un groupe de balises actives, les décisions du modèle ML mappées sur le groupe sont affichées en ligne avec les balises dans le groupe pour vous aider à afficher les informations en ligne, où elles sont le plus logiques.

## <a name="how-to-set-up-a-smart-tag-group"></a>Procédure de configuration d’un groupe de balises actives

1. Dans un jeu de révision, accédez à **Manage Review Set** -> **Manage Tags**.

2. Cliquez sur le menu déroulant en regard d' **Ajouter un groupe** de balises et sélectionnez **Ajouter un groupe de balises actives**.

3. Sélectionnez le modèle que vous souhaitez mapper à ce groupe. Cette opération crée une section de balise et N balises enfants, où N représente le nombre de sorties possibles du modèle. Par exemple, le modèle de détection des privilèges du client avocat a deux sorties possibles: privilégié et non privilégié; la sélection de ce modèle crée deux balises enfants dans l’ensemble de révision, chacune correspondant à l’une des sorties possibles.

4. Renommez le groupe de balises et les balises en fonction de vos besoins.

## <a name="how-to-use-a-smart-tag-group"></a>Utilisation d’un groupe de balises actives

Lors de l’examen d’un document, les résultats du modèle seront exposés en regard de la valeur de balise appropriée. Par exemple, si vous disposez d’un groupe de balises actives pour la détection des privilèges du client et que vous révisez un document que le modèle a décidé est potentiellement privilégié, vous verrez le motif de cette balise en regard de la balise appropriée. Il est important de noter que la balise n’est pas automatiquement appliquée; pour toutes les opérations et les objectifs, les balises d’un groupe de balises actives agissent de la même manière que les balises normales, à l’exception du fait qu’ils exposent les résultats du modèle en regard de ces derniers, le cas échéant