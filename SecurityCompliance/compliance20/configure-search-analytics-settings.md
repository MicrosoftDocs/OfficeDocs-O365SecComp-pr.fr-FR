---
title: Configurer les paramètres de recherche et d’analyse
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
description: ''
ms.openlocfilehash: 0f5a98a7ba7a62e3b77794b38e444006a340cb49
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243189"
---
# <a name="configure-search-and-analytics-settings"></a>Configurer les paramètres de recherche et d’analyse

## <a name="near-duplicates-and-email-threading"></a>Quasi-doublons et Threading de courrier électronique

Dans cette section, vous pouvez définir des paramètres pour la détection des doublons, la détection des doublons et le Threading de messagerie.

- Activer/désactiver: inclut la détection des doublons, la détection à proximité des doublons et le Threading du courrier électronique dans le cadre du flux d'analyse s'il est activé. Étant donné qu'ils sont générés les uns sur les autres, vous devez tous les activer ou les désactiver tous.

- Seuil: si le niveau de similarité de deux documents est supérieur au seuil, ils seront placés dans le même ensemble presque en double.

- Masquer les doublons par défaut: si ce paramètre est activé, un filtre permettant de masquer les doublons de documents est appliqué par défaut dans le jeu de travail. Si nécessaire, le filtre peut être supprimé manuellement dans le jeu de travail.

- Nombre minimal/maximum de mots: les doublons et les threads de courrier électronique s'exécutent uniquement sur les documents qui contiennent au moins le nombre minimal de mots et le nombre maximal de mots.
Pour plus d'informations, consultez la rubrique [near Detection Detection](near-duplicates.md) and [email Threading](email-threading.md).

## <a name="themes"></a>Thèmes

Dans cette section, vous pouvez définir des paramètres pour les thèmes.

- Activer/désactiver: inclut le clustering thèmes dans le cadre du flux d'analyse s'il est activé.
- Ajustez dynamiquement le nombre maximal de thèmes de façon dynamique: dans certains cas, il n'y a pas assez de documents pour produire le nombre souhaité de thèmes. Si ce paramètre est activé, au lieu d'essayer de forcer le nombre maximal de thèmes souhaités, le système ajuste le nombre maximal de thèmes de manière dynamique.
- Nombre maximal de thèmes: nombre souhaité de thèmes
- Inclure les numéros dans les thèmes: lorsque ce dernier est activé, il inclut des numéros dans lors de la génération de thèmes.  

## <a name="optical-character-recognition-ocr"></a>Reconnaissance optique de caractères (OCR)

Lorsque ce paramètre est activé, la reconnaissance optique de caractères est exécutée sur les images qui sont ingérées dans les jeux de travail afin qu'ils puissent être recherchés.

## <a name="ignore-text"></a>Ignorer le texte

Il existe des situations dans lesquelles certains textes réduisent la qualité de l'analyse, tels que des clauses de responsabilité longues qui sont ajoutées à certains courriers électroniques indépendamment du contenu du message. Si vous avez conscience de ces cas, vous pouvez exclure ce texte de l'analyse en spécifiant le texte (RegEx est pris en charge) et les modules pour lesquels le texte doit être exclu.