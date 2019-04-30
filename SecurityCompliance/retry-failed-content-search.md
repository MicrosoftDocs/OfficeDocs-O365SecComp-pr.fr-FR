---
title: Nouvelle tentative de recherche de contenu pour résoudre une erreur d'emplacement de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez le bouton nouvelle tentative pour résoudre les recherches de contenu présentant des erreurs d'emplacement de contenu.
ms.openlocfilehash: 0963bccfe88a74b82ec3155469ca6d892bf2f7d8
ms.sourcegitcommit: 72e8a74b55fe7f56b50e30ff10a635734b5a3220
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33472379"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Nouvelle tentative de recherche de contenu pour résoudre une erreur d'emplacement de contenu

Lorsque vous utilisez la recherche de contenu dans le centre de sécurité et de conformité pour rechercher un grand nombre de boîtes aux lettres, vous pouvez obtenir des erreurs de recherche semblables à celles-ci:

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Ces erreurs (avec les codes d'erreur CS008-009 et CS012-002) indiquent que la recherche de contenu n'a pas pu Rechercher des emplacements de contenu spécifiques; dans cet exemple, deux boîtes aux lettres n'ont pas été recherchées. Ces erreurs s'affichent sur la page de menu volant des détails de l'état de la recherche de contenu.

## <a name="cause-of-content-location-errors"></a>Cause des erreurs d'emplacement de contenu

Lors de la recherche d'un grand nombre de boîtes aux lettres, la recherche est répartie entre des milliers de serveurs dans un centre de contenu Microsoft. À tout moment, des serveurs spécifiques peuvent être en état de redémarrage ou en cours de basculement vers des copies redondantes. Dans l'un ou l'autre de ces cas, la demande de récupération de données de la recherche de contenu expire. Dans l'exemple précédent, les erreurs des boîtes aux lettres qui ont échoué étaient le résultat du dépassement du délai de la recherche.

## <a name="resolving-content-location-errors"></a>Résolution des erreurs d'emplacement de contenu

Le redémarrage de la recherche entraîne souvent des erreurs similaires sur différents serveurs. Au lieu de relancer la recherche, cliquez sur **** le bouton Réessayer qui s'affiche en haut de la page des résultats de la recherche.

![Cliquez sur le bouton réEssayer pour résoudre les erreurs d'emplacement de contenu](media/retrycontentsearch3.png)

Cela entraînera la nouvelle tentative de recherche uniquement pour les boîtes aux lettres qui ont échoué. Lorsque vous effectuez une nouvelle tentative de recherche, les autres résultats renvoyés avec succès sont conservés.

## <a name="tips-to-avoid-content-location-errors"></a>Conseils pour éviter les erreurs d'emplacement de contenu

Voici quelques causes supplémentaires des erreurs d'emplacement de contenu et des conseils pour vous aider à les éviter lors de la recherche d'un grand nombre de boîtes aux lettres.

- La boîte aux lettres recherchée est peut-être occupée en raison de l'activité de l'utilisateur. Dans ce cas, le service de recherche peut limiter lui-même pour empêcher la boîte aux lettres de devenir indisponible. Pour éviter cela, essayez d'exécuter des recherches en dehors des heures d'ouverture.

- La requête de recherche peut extraire trop de contenu de la boîte aux lettres. Dans la mesure du possible, essayez de limiter l'étendue de la recherche à l'aide de mots clés, de plages de dates et de conditions de recherche.

- Trop de mots clés ou d'expressions de mots clés lorsque vous créez une requête de recherche à l'aide de la [liste des mots clés](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Lorsque vous exécutez une requête de recherche qui utilise la liste de mots-clés, le service exécute essentiellement une recherche distincte pour chaque ligne de la liste de mots clés afin de pouvoir générer des statistiques. Si vous utilisez la liste de mots-clés dans les requêtes de recherche, réduisez le nombre de lignes dans la liste de mots clés ou divisez les mots clés en listes plus petites et créez une recherche différente pour chaque liste de mots clés.

  > [!NOTE]
  > Pour vous aider à réduire les problèmes causés par des listes de mots clés volumineux, vous êtes désormais limité à un maximum de 20 lignes dans la liste de mots clés d'une requête de recherche.

- Trop de recherches sont effectuées simultanément sur la même boîte aux lettres. Si possible, essayez d'exécuter une recherche à la fois sur une seule boîte aux lettres.

- Recherche d'un trop grand nombre de boîtes aux lettres dans une seule recherche. La probabilité d'erreurs d'emplacement de contenu augmente lors de la recherche d'un très grand nombre de boîtes aux lettres. Si possible, essayez d'exécuter plusieurs recherches de sorte que chaque recherche comprenne un sous-ensemble de boîtes aux lettres dans votre organisation.

- La maintenance requise est effectuée sur la boîte aux lettres. Bien que cette cause se produise probablement rarement, patientez quelques instants après avoir reçu l'erreur d'emplacement de contenu, puis recommencez la recherche.
