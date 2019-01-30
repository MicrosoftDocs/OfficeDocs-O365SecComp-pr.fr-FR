---
title: Indexation de données dépositaire avancée
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
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607648"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexation de données dépositaire avancée

Lorsqu’un dépositaire est ajouté à une affaire eDiscovery avancées (Preview), n’importe quel contenu dans Office 365 qui était considéré comme partiellement indexé est de transformation pour le rendre entièrement modifiable.  Ce processus est appelé *indexation avancée*. Contenu peut être indexé partiellement pour plusieurs raisons, y compris l’existence des images, des types de fichiers non pris en charge ou lorsque les limites de taille de fichier d’indexation rencontrés.  Pour en savoir plus sur les éléments indexés partiellement, voir [partiellement indexé des éléments de la recherche de contenu dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Affichage des résultats d’indexation avancées

Une fois le processus d’indexation avancé terminé, vous pouvez obtenir une bonne compréhension de l’efficacité de traiter à nouveau.  Dans la vue dépositaire l’indexation, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.  L’index de hybride est où eDiscovery avancée (Preview) stocke le contenu nouveau traité.

Le graphique inclut également le nombre d’éléments qui nécessitent une conversion et une autre graphique d’erreurs par type de fichier. Pour plus d’informations, voir [correction d’erreur lors du traitement des données](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Mise à jour des index avancées pour dépositaires

Lorsqu’un dépositaire est ajouté à une affaire eDiscovery avancées (Preview), tous les éléments indexés partiellement sont nouveau traités. Toutefois, avec le temps, les éléments indexés plus partiellement peuvent être ajoutés à un compte d’utilisateur boîte aux lettres ou OneDrive.  Si nécessaire, vous pouvez mettre à jour les index.

> [!NOTE]
> Mise à jour des index dépositaire est un processus long. Il est recommandé de ne pas mettre index plusieurs fois par jour dans un cas.
