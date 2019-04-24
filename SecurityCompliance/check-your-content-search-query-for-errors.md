---
title: Vérifier la présence d’erreurs dans vos requêtes de recherche de contenu
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Vérifiez votre requête par mot clé pour la recherche de contenu pour les erreurs et les fautes de frappe, telles que les caractères non pris en charge et les opérateurs booléens en minuscules, avant d'exécuter la recherche. Si nous trouvons une erreur, nous vous suggérons une requête révisée.
ms.openlocfilehash: 00612116f345e2a01471d5c83df77f4bc8db9ce5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243657"
---
# <a name="check-your-content-search-query-for-errors"></a>Vérifier la présence d’erreurs dans vos requêtes de recherche de contenu

Lors de la création ou de la modification d'une recherche de contenu, vous pouvez demander à Office 365 de vérifier si votre requête contient des caractères non pris en charge et des opérateurs booléens qui ne peuvent pas être capitalisés. Comment ? Cliquez simplement sur **Vérifier la requête pour les fautes de frappe** sur la page de requête d'une recherche de contenu. 
  
![Cliquez sur «Vérifier la requête pour les fautes de frappe» pour vérifier si votre requête de recherche comporte des caractères non pris en charge](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
Voici une liste des caractères non pris en charge que nous vérifions. Les caractères non pris en charge sont souvent masqués et ils provoquent généralement une erreur de recherche ou renvoient des résultats inattendus.
  
- **** Guillemets typographiques-les guillemets simples et doubles intelligents (également appelés guillemets) ne sont pas pris en charge. Seuls les guillemets droits peuvent être utilisés dans une requête de recherche. 
    
- **Caractères non imprimables et de contrôle** -les caractères non imprimables et de contrôle ne représentent pas un symbole écrit, tel qu'un caractère alphanumérique. Il peut s'agir de caractères servant à mettre en forme le texte ou à séparer des lignes. 
    
- Repères de **gauche à droite et de droite à gauche** : il s'agit de caractères de contrôle permettant d'indiquer l'orientation du texte pour les langues se lisant de gauche à droite (telles que l'anglais et l'espagnol) et les langues se lisant de droite à gauche (comme l'arabe et l'hébreu).
    
- **Opérateurs booléens** en minuscules: Si vous utilisez un opérateur booléen, comme **and**, **or**et **not** dans une requête de recherche, il doit être en majuscules. Lorsque nous vérifions une requête pour rechercher des fautes de frappe, la syntaxe de requête indique souvent qu'un opérateur booléen est utilisé même si des opérateurs en minuscules peuvent être utilisés; par exemple, `(WordA or WordB) and (WordC or WordD)`.
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a>Que se passe-t-il si une requête contient un caractère non pris en charge?

Si vous trouvez des caractères non pris en charge dans votre requête, un message d'avertissement s'affiche indiquant les caractères non pris en charge qui ont été trouvés et une suggestion de remplacement. Ensuite, vous pouvez conserver la requête d'origine ou la remplacer par la requête modifiée suggérée. Voici un exemple du message d'avertissement qui s'affiche une fois que vous avez cliqué sur **Vérifier la requête pour** Rechercher les fautes de recherche dans la capture d'écran précédente. Notez que la requête d'origine contient des guillemets typographiques et des opérateurs booléens en minuscules. 
  
![Un message d'avertissement s'affiche avec une révision suggérée pour votre requête.](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a>Comment empêcher les caractères non pris en charge dans vos requêtes de recherche

Les caractères non pris en charge sont généralement ajoutés à une requête lorsque vous copiez la requête ou des parties de la requête à partir d'autres applications (telles que Microsoft Word ou Microsoft Excel) et copiez-les dans la zone de mot clé dans la page de requête d'une recherche de contenu. Le meilleur moyen d'éviter les caractères non pris en charge est de saisir la requête dans la zone de mot clé. Vous pouvez aussi copier votre requête à partir de Word ou d'Excel, puis la coller dans un éditeur de texte brut, comme le Bloc-notes Microsoft. Enregistrez ensuite le fichier texte, puis sélectionnez **ANSI** dans la liste déroulante **Encodage**. Cette action supprime tout le formatage et tous les caractères non pris en charge. Vous pouvez ensuite copier la requête du fichier texte vers la zone de mot clé de la requête. 
