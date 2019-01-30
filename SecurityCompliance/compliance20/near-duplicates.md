---
title: Près de la détection des doublons
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607666"
---
# <a name="near-duplicate-detection"></a>Près de la détection des doublons

Envisagez un ensemble de documents à réviser dans lequel un sous-ensemble basé sur le même modèle et a principalement le même réutilisable dans un langage, avec quelques différences ici et là. Si un réviseur peut identifier ce sous-ensemble, passez en revue minutieusement un d'entre eux et passez en revue les différences pour le reste, ils ne seraient pas ont manqué aucune information unique tandis que prendre qu’une fraction de temps qui auraient à lire tous les documents garde à la page de garde. Détection des doublons NEAR regroupe les documents textuelle similaires ensemble pour vous aider à améliorer l’efficacité de votre processus de révision.

## <a name="how-does-it-work"></a>Comment fonctionne-t-il ?

Lorsque près de détection des doublons est exécuté, le système analyse tous les documents avec du texte. Ensuite, il compare tous les documents par rapport aux autres pour déterminer si leur similarité est supérieure au seuil d’ensemble. S’il s’agit, les documents sont regroupés. Une fois que tous les documents ont été comparées et regroupées, chaque groupe d’un document est marqué comme « pivot » ; en examinant vos documents, vous pouvez consulter un tableau croisé dynamique tout d’abord et passez en revue les autres documents dans la même près de jeu en double, en mettant l’accent sur la différence entre le tableau croisé dynamique et le document est en cours de révision.