---
title: Détecter des quasi-duplicatas
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 40270fa1e3a6f7cdf0dd2a83650aa36a935d9a6d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213124"
---
# <a name="near-duplicate-detection"></a>Détecter des quasi-duplicatas

Considérez un ensemble de documents à examiner dans lequel un sous-ensemble est basé sur le même modèle et qui possède essentiellement le même langage, avec quelques différences ici et là. Si un réviseur peut identifier ce sous-ensemble, passer en revue l'une d'entre elles de façon approfondie et passer en revue les différences pour le reste, il n'aurait pas manqué d'informations uniques pendant une période de temps qui aurait été utilisée pour lire tous les documents. Les groupes de détection near-duplicate regroupent des documents textuellement similaires pour vous aider à améliorer l'efficacité de votre processus de révision.

## <a name="how-does-it-work"></a>Comment fonctionne-t-il ?

Lorsque l'exécution de la détection de doublons est exécutée, le système analyse tous les documents avec du texte. Ensuite, il compare chaque document aux autres pour déterminer si leur similarité est supérieure au seuil défini. Si c'est le cas, les documents sont regroupés. Une fois que tous les documents ont été comparés et regroupés, un document de chaque groupe est marqué comme «tableau croisé dynamique»; lors de l'examen de vos documents, vous pouvez commencer par examiner un tableau croisé dynamique et passer en revue les autres documents dans le même jeu presque en double, en vous concentrant sur la différence entre le tableau croisé dynamique et le document en cours de révision.