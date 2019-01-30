---
title: Configurer les paramètres de recherche et analytique
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
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607673"
---
# <a name="configure-search-and-analytics-settings"></a>Configurer les paramètres de recherche et analytique


## <a name="near-duplicates-and-email-threading"></a>Proximité des doublons et messagerie threading

Dans cette section, vous pouvez définir des paramètres pour la détection des doublons, près de la détection des doublons et des threads de messagerie.

- Activer/désactiver : inclure la détection des doublons, près de la détection des doublons et messagerie threading dans le cadre du flux analytique si activé. Car ils reposent sur l’autre, vous devez tous les activer ou désactiver tous les.

- Seuil : si le niveau de similarité de deux documents est dépasse le seuil, ils seront placés dans le même près de jeu en double.

- Masquer les doublons par défaut : Si ce paramètre est activé, un filtre pour masquer les documents en double sera appliqué dans le jeu par défaut de travail. Le filtre peut être supprimé manuellement dans le jeu si nécessaire de travail.

- Nombre minimum/maximum de mots : près de messagerie et les doublons threading s’exécute uniquement sur les documents qui ont au moins le nombre minimal de mots et au plus le nombre maximal de mots. Pour plus d’informations, voir [près de détection des doublons](near-duplicates.md) et les [threads de courrier électronique](email-threading.md).

## <a name="themes"></a>Thèmes

Dans cette section, vous pouvez définir les paramètres des thèmes.

- Activer/désactiver : inclure des thèmes clusters dans le cadre du flux analytique si activé.
- Ajuster le nombre maximal de thèmes dynamiquement dynamiquement : dans certains cas, il n’existe pas suffisamment de documents pour générer le nombre de thèmes souhaité. Si ce paramètre est activé, puis plutôt que vous essayez de forcer le nombre maximal de votre choix de thèmes, le système ajuste nombre maximal de thèmes dynamique.
- Nombre maximal de thèmes : nombre souhaité de thèmes
- Inclure les numéros de thèmes : lorsqu’il est activé, il inclut les numéros dans lors de la génération des thèmes.  

## <a name="optical-character-recognition-ocr"></a>Reconnaissance optique de caractères (OCR)

Lorsque ce paramètre est activé, OCR doit s’exécuter sur les images qui sont ingérés dans des groupes de travail afin qu’elles puissent être utilisables dans une requête.

## <a name="ignore-text"></a>Ignorer le texte

Il existe des instances où certains textes peuvent diminuer la qualité d’analytique, tels que des exclusions longues qui sont ajoutées à certains messages électroniques indépendamment du contenu du courrier électronique. Si vous avez pris connaissance de ces cas, vous pouvez exclure ce texte analytique en spécifiant le texte (RegEx est pris en charge) et qui doit être exclu de texte pour les modules.