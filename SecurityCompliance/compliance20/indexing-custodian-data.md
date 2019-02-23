---
title: Indexation avancée des données des consignataires
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
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218664"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexation avancée des données des consignataires

Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tout contenu dans Office 365 considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.  Ce processus est appelé *indexation avancée*. Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l'existence d'images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d'indexation sont rencontrées.  Pour en savoir plus sur les éléments partiellement indexés, consultez la rubrique [éléments partiellement indexés dans la recherche de contenu dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).

## <a name="viewing-advanced-indexing-results"></a>Affichage des résultats de l'indexation avancée

Une fois le processus d'indexation avancé terminé, vous pouvez comprendre l'efficacité du nouveau traitement.  Dans la vue d'indexation dépositaire, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.  L'index hybride est l'emplacement où Advanced eDiscovery (aperçu) stocke le contenu retraité.

Le graphique inclut également le nombre d'éléments nécessitant une correction et un autre graphique d'erreurs par type de fichier. Pour plus d'informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Mise à jour des index avancés pour les dépositaires

Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tous les éléments partiellement indexés sont ré-traités. Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d'un utilisateur.  Si nécessaire, vous pouvez mettre à jour les index.

> [!NOTE]
> La mise à jour des index de dépositaire est un processus de longue durée. Il est recommandé de ne pas mettre à jour les index plus d'une fois par jour dans un cas.
