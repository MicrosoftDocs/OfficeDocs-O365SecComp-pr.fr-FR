---
title: Nouvelle tentative d’une recherche de contenu pour corriger une erreur d’emplacement de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez le bouton Réessayer pour résoudre les recherches de contenu contenant des erreurs de l’emplacement du contenu.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210183"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a>Nouvelle tentative d’une recherche de contenu pour corriger une erreur d’emplacement de contenu

Lorsque vous utilisez la recherche de contenu de la sécurité pour Microsoft Office 365 et le centre de conformité pour rechercher un très grand nombre de boîtes aux lettres (par exemple, la recherche au moins 100 000 boîtes aux lettres en une seule recherche de contenu), vous obtiendrez des erreurs de recherche qui sont similaires à ce qui suit :

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

Ces erreurs (avec les codes d’erreur de CS008-009 et CS012-002) indiquent que la recherche de contenu a échoué rechercher les emplacements de contenu spécifiques ; Dans cet exemple, deux boîtes aux lettres n’ont pas été exclus. Ces erreurs s’affichent dans la page de flottant état détails de la recherche de contenu.

## <a name="cause-of-content-location-errors"></a>Cause des erreurs de l’emplacement du contenu

Lorsque vous recherchez un grand nombre de boîtes aux lettres, la recherche est distribuée sur des milliers de serveurs dans un centre de données Microsoft. À tout moment, des serveurs spécifiques peuvent être dans l’état de redémarrage ou en cours de basculement pour les copies redondantes. Dans ces cas, la requête de recherche de contenu pour récupérer des données expire. Dans l’exemple précédent, les erreurs pour les boîtes aux lettres ayant échoué ont été le résultat de l’expiration de recherche.

## <a name="resolving-content-location-errors"></a>Résolution des erreurs de l’emplacement du contenu

Redémarrer la recherche entraînent souvent des erreurs similaires sur différents serveurs. Au lieu de redémarrer la recherche, cliquez sur le bouton **Réessayer** qui s’affiche en haut de la page de résultats de recherche.

![Cliquez sur Réessayer pour résoudre les erreurs de l’emplacement du contenu](media/retrycontentsearch3.png)

Ainsi, la nouvelle tentative de la recherche uniquement pour les boîtes aux lettres ayant échoué. Lorsque vous relancez la recherche, les autres résultats ont été correctement renvoyées sont conservés.

## <a name="tips-to-avoid-content-location-errors"></a>Conseils pour éviter les erreurs de l’emplacement du contenu

Voici quelques causes Ajout d’erreurs de l’emplacement du contenu et des conseils pour vous aider à éviter lors de la recherche de grandes quantités de boîtes aux lettres.

- La boîte aux lettres en cours de recherche peut être occupé en raison de l’activité de l’utilisateur. Dans ce cas, le service de recherche peut limiter elle-même pour empêcher l’indisponibilité de la boîte aux lettres. Pour éviter ce problème, essayez d’exécuter des recherches pendant les heures creuses.

- La requête de recherche peut être récupération trop de contenu à partir de la boîte aux lettres. Si possible, essayez de limiter l’étendue de la recherche à l’aide de mots clés, des plages de dates et des conditions de recherche.

- Trop de mots clés ou expressions lorsque vous créez une requête de recherche à l’aide de la [liste des mots clés](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Lorsque vous exécutez une requête de recherche qui utilise la liste des mots clés, le service exécute essentiellement une recherche distincte pour chaque ligne dans la liste des mots clés afin que les statistiques peuvent être générées. Si vous utilisez la liste des mots clés dans les requêtes de recherche, réduisez le nombre de lignes dans la liste des mots clés ou divisez les mots clés numéros en plus petits listes et créer une nouvelle recherche pour chaque liste de mots clés.

  > [!NOTE]
  > Pour réduire les problèmes causés par mot clé grandes listes, vous êtes limité à un maximum de 20 lignes dans la liste des mots clés d’une requête de recherche.

- Trop de recherche est en cours sur la même boîte aux lettres en même temps. Si possible, essayez d’exécuter une recherche à la fois sur n’importe quel une boîte aux lettres.

- Recherche trop grand nombre de boîtes aux lettres en une seule recherche. La probabilité d’erreurs de l’emplacement du contenu augmente lorsque vous recherchez un très grand nombre de boîtes aux lettres. Si possible, essayez d’exécuter plusieurs recherches afin que chaque recherche inclut un sous-ensemble de boîtes aux lettres dans votre organisation.

- Maintenance requis est en cours d’exécution sur la boîte aux lettres. Si ce problème se produit probablement rarement, attendre un peu alors que lorsqu’il reçoit l’erreur d’emplacement de contenu, puis relancez la recherche.
