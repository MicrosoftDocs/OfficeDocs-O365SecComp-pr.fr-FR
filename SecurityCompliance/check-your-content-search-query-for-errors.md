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
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="ccac2-104">Vérifier la présence d’erreurs dans votre requête de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="ccac2-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="ccac2-p102">Lorsque vous créez ou modifiez une recherche de contenu, vous pouvez avoir Office 365 pour vérifier votre requête pour les caractères non pris en charge et des opérateurs booléens ne peuvent pas être mise en majuscule. Comment ? Cliquez sur **vérifier la requête pour toute erreur** dans la page de requête d’une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Cliquez sur « Vérifier la requête pour toute erreur » pour vérifier votre requête de recherche pour les caractères non pris en charge](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="ccac2-p103">Voici une liste des caractères non pris en charge que nous vérifier. Caractères non pris en charge sont souvent masquées, et ils généralement de provoquer une erreur de recherche ou de renvoyer des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="ccac2-p104">**Des guillemets** - des uniques et doubles guillemets (également appelés des guillemets) ne sont pas pris en charge. Uniquement des guillemets utilisable dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="ccac2-p105">**Caractères Non imprimables et contrôle** - Non imprimables et caractères de contrôle ne représentent pas un symbole écrit, par exemple un caractère alphanumérique. Exemples de non imprimables et caractères de contrôle incluent des caractères mise en forme du texte ou des lignes distinctes de texte.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="ccac2-115">**Marques de gauche à droite et de droite à gauche** - il s’agit des caractères de contrôle est utilisées pour indiquer l’orientation du texte des langues de droite à gauche (telles que l’anglais et l’espagnol) et les langues de droite à gauche (telles que l’arabe et l’hébreu).</span><span class="sxs-lookup"><span data-stu-id="ccac2-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="ccac2-p106">**Opérateurs booléens minuscules** - si vous utilisez un opérateur booléen, tels que **AND**, **OR**et **pas** dans une requête de recherche, il doit être en majuscules. Nous vérifions une requête pour toute erreur, la syntaxe de requête souvent indique qu’un opérateur booléen est utilisé même si les opérateurs minuscules peuvent être utilisés ; par exemple, `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="ccac2-118">Que se passe-t-il si une requête comporte un caractère non pris en charge ?</span><span class="sxs-lookup"><span data-stu-id="ccac2-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="ccac2-p107">Si les caractères non pris en charge sont détectées dans votre requête, un message d’avertissement s’affiche indiquant que les caractères non pris en charge qui ont été détectés et propose une alternative. Vous avez ensuite l’option Conserver la requête d’origine ou remplacez-le par la requête modifiée suggérée. Voici un exemple du message d’avertissement qui s’affiche lorsque vous cliquez sur **vérifier la requête pour toute erreur** de la requête de recherche dans la capture d’écran précédente. Notez que la requête d’origine contienne des guillemets et des opérateurs booléens en minuscules.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Un message d’avertissement s’affiche avec une révision suggérée pour votre requête](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="ccac2-124">Comment faire pour empêcher que des caractères non pris en charge dans les requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="ccac2-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="ccac2-p108">Caractères non pris en charge sont généralement ajoutés à une requête lorsque vous copiez la requête ou les composants de la requête à partir d’autres applications (tel que Microsoft Word ou Microsoft Excel) et les copiez dans la zone mots clés dans la page requête d’une recherche de contenu. La meilleure façon pour empêcher que des caractères non pris en charge est de taper la requête dans la zone mot clé. Vous pouvez également copier une requête à partir de Word ou Excel et puis collez-le dans le fichier dans un éditeur de texte, tel que Microsoft Notepad. Enregistrez le fichier texte, puis sélectionnez **ANSI** dans la liste déroulante **codage** . Cette action supprime tous les caractères non pris en charge et de mise en forme. Ensuite, vous pouvez copier et coller la requête à partir du fichier texte à la zone de requête de mot clé.</span><span class="sxs-lookup"><span data-stu-id="ccac2-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
