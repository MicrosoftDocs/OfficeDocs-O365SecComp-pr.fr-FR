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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 1521aadca42c8119ae341065865b227fb16ffcf3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251942"
---
# <a name="advanced-indexing-of-custodian-data"></a>Indexation avancée des données des consignataires

Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tout contenu dans Office 365 considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.  Ce processus est appelé *indexation avancée*. Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l'existence d'images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d'indexation sont rencontrées.

Pour en savoir plus sur le traitement de la prise en charge dans Office 365 et les éléments partiellement indexés, voir:

- [Types de fichiers pris en charge dans Advanced eDiscovery](supported-filetypes-ediscovery20.md)
- [Éléments partiellement indexés dans la recherche de contenu dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [Formats de fichier indexés par le service de recherche Exchange](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Affichage des résultats de l'indexation avancée

Une fois le processus d'indexation avancé terminé, vous pouvez comprendre l'efficacité du nouveau traitement.  Dans la vue d'indexation dépositaire, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.  L'index hybride est l'emplacement où Advanced eDiscovery (aperçu) stocke le contenu retraité.

Le graphique inclut également le nombre d'éléments nécessitant une correction et un autre graphique d'erreurs par type de fichier. Pour plus d'informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Mise à jour des index avancés pour les dépositaires

Lorsqu'un dépositaire est ajouté à un cas avancé eDiscovery (aperçu), tous les éléments partiellement indexés sont ré-traités. Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d'un utilisateur.  Si nécessaire, vous pouvez mettre à jour les index.

> [!NOTE]
> La mise à jour des index de dépositaire est un processus de longue durée. Il est recommandé de ne pas mettre à jour les index plus d'une fois par jour dans un cas.
