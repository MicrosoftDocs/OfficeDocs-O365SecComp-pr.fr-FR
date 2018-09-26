---
title: Vérifier la présence d’erreurs dans votre requête de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Vérifiez votre requête de mot clé pour la recherche de contenu pour les erreurs et les erreurs typographiques, tels que des caractères non pris en charge et en minuscules les opérateurs booléens, avant d’exécuter la recherche. Si nous trouve une erreur, nous vous suggérons une requête révisée.
ms.openlocfilehash: 6ae14edc29bb7f8bab5dd2306282a69443872633
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038287"
---
# <a name="check-your-content-search-query-for-errors"></a>Vérifier la présence d’erreurs dans votre requête de recherche de contenu

Lorsque vous créez ou modifiez une recherche de contenu, vous pouvez avoir Office 365 pour vérifier votre requête pour les caractères non pris en charge et des opérateurs booléens ne peuvent pas être mise en majuscule. Comment ? Cliquez sur **vérifier la requête pour toute erreur** dans la page de requête d’une recherche de contenu. 
  
![Cliquez sur « Vérifier la requête pour toute erreur » pour vérifier votre requête de recherche pour les caractères non pris en charge](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
Voici une liste des caractères non pris en charge que nous vérifier. Caractères non pris en charge sont souvent masquées, et ils généralement de provoquer une erreur de recherche ou de renvoyer des résultats inattendus.
  
- **Des guillemets** - des uniques et doubles guillemets (également appelés des guillemets) ne sont pas pris en charge. Uniquement des guillemets utilisable dans une requête de recherche. 
    
- **Caractères Non imprimables et contrôle** - Non imprimables et caractères de contrôle ne représentent pas un symbole écrit, par exemple un caractère alphanumérique. Exemples de non imprimables et caractères de contrôle incluent des caractères mise en forme du texte ou des lignes distinctes de texte. 
    
- **Marques de gauche à droite et de droite à gauche** - il s’agit des caractères de contrôle est utilisées pour indiquer l’orientation du texte des langues de droite à gauche (telles que l’anglais et l’espagnol) et les langues de droite à gauche (telles que l’arabe et l’hébreu).
    
- **Opérateurs booléens minuscules** - si vous utilisez un opérateur booléen, tels que **AND**, **OR**et **pas** dans une requête de recherche, il doit être en majuscules. Nous vérifions une requête pour toute erreur, la syntaxe de requête souvent indique qu’un opérateur booléen est utilisé même si les opérateurs minuscules peuvent être utilisés ; par exemple, `(WordA or WordB) and (WordC or WordD)`.
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a>Que se passe-t-il si une requête comporte un caractère non pris en charge ?

Si les caractères non pris en charge sont détectées dans votre requête, un message d’avertissement s’affiche indiquant que les caractères non pris en charge qui ont été détectés et propose une alternative. Vous avez ensuite l’option Conserver la requête d’origine ou remplacez-le par la requête modifiée suggérée. Voici un exemple du message d’avertissement qui s’affiche lorsque vous cliquez sur **vérifier la requête pour toute erreur** de la requête de recherche dans la capture d’écran précédente. Notez que la requête d’origine contienne des guillemets et des opérateurs booléens en minuscules. 
  
![Un message d’avertissement s’affiche avec une révision suggérée pour votre requête](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a>Comment faire pour empêcher que des caractères non pris en charge dans les requêtes de recherche

Caractères non pris en charge sont généralement ajoutés à une requête lorsque vous copiez la requête ou les composants de la requête à partir d’autres applications (tel que Microsoft Word ou Microsoft Excel) et les copiez dans la zone mots clés dans la page requête d’une recherche de contenu. La meilleure façon pour empêcher que des caractères non pris en charge est de taper la requête dans la zone mot clé. Vous pouvez également copier une requête à partir de Word ou Excel et puis collez-le dans le fichier dans un éditeur de texte, tel que Microsoft Notepad. Enregistrez le fichier texte, puis sélectionnez **ANSI** dans la liste déroulante **codage** . Cette action supprime tous les caractères non pris en charge et de mise en forme. Ensuite, vous pouvez copier et coller la requête à partir du fichier texte à la zone de requête de mot clé. 
