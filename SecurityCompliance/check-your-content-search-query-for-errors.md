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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215934"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="62db0-104">Vérifier la présence d’erreurs dans vos requêtes de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="62db0-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="62db0-p102">Lors de la création ou de la modification d'une recherche de contenu, vous pouvez demander à Office 365 de vérifier si votre requête contient des caractères non pris en charge et des opérateurs booléens qui ne peuvent pas être capitalisés. Manière? Cliquez simplement sur **Vérifier la requête pour les fautes de frappe** sur la page de requête d'une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="62db0-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Cliquez sur «Vérifier la requête pour les fautes de frappe» pour vérifier si votre requête de recherche comporte des caractères non pris en charge](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="62db0-p103">Voici une liste des caractères non pris en charge que nous vérifions. Les caractères non pris en charge sont souvent masqués et ils provoquent généralement une erreur de recherche ou renvoient des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="62db0-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="62db0-p104">\*\*\*\* Guillemets typographiques-les guillemets simples et doubles intelligents (également appelés guillemets) ne sont pas pris en charge. Seuls les guillemets droits peuvent être utilisés dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="62db0-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="62db0-p105">**Caractères non imprimables et de contrôle** -les caractères non imprimables et de contrôle ne représentent pas un symbole écrit, tel qu'un caractère alphanumérique. Des exemples de caractères non imprimables et de contrôle incluent des caractères qui formatent du texte ou des lignes de texte distinctes.</span><span class="sxs-lookup"><span data-stu-id="62db0-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="62db0-115">Repères de **gauche à droite et de droite à gauche** : il s'agit de caractères de contrôle permettant d'indiquer l'orientation du texte pour les langues se lisant de gauche à droite (telles que l'anglais et l'espagnol) et les langues se lisant de droite à gauche (comme l'arabe et l'hébreu).</span><span class="sxs-lookup"><span data-stu-id="62db0-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="62db0-p106">**Opérateurs booléens** en minuscules: Si vous utilisez un opérateur booléen, comme **and**, **or**et **not** dans une requête de recherche, il doit être en majuscules. Lorsque nous vérifions une requête pour rechercher des fautes de frappe, la syntaxe de requête indique souvent qu'un opérateur booléen est utilisé même si des opérateurs en minuscules peuvent être utilisés; par exemple, `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="62db0-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="62db0-118">Que se passe-t-il si une requête contient un caractère non pris en charge?</span><span class="sxs-lookup"><span data-stu-id="62db0-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="62db0-p107">Si vous trouvez des caractères non pris en charge dans votre requête, un message d'avertissement s'affiche indiquant les caractères non pris en charge qui ont été trouvés et une suggestion de remplacement. Ensuite, vous pouvez conserver la requête d'origine ou la remplacer par la requête modifiée suggérée. Voici un exemple du message d'avertissement qui s'affiche une fois que vous avez cliqué sur **Vérifier la requête pour** Rechercher les fautes de recherche dans la capture d'écran précédente. Notez que la requête d'origine contient des guillemets typographiques et des opérateurs booléens en minuscules.</span><span class="sxs-lookup"><span data-stu-id="62db0-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Un message d'avertissement s'affiche avec une révision suggérée pour votre requête.](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="62db0-124">Comment empêcher les caractères non pris en charge dans vos requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="62db0-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="62db0-p108">Les caractères non pris en charge sont généralement ajoutés à une requête lorsque vous copiez la requête ou des parties de la requête à partir d'autres applications (telles que Microsoft Word ou Microsoft Excel) et copiez-les dans la zone de mot clé dans la page de requête d'une recherche de contenu. La meilleure façon d'empêcher les caractères non pris en charge est de taper simplement la requête dans la zone mot clé. Vous pouvez également copier une requête à partir de Word ou Excel, puis la coller dans un éditeur de texte brut, tel que le bloc-notes Microsoft. Ensuite, enregistrez le fichier texte et sélectionnez **ANSI** dans la liste déroulante **Encoding** . Cette opération supprime toute mise en forme et tous les caractères non pris en charge. Ensuite, vous pouvez copier et coller la requête à partir du fichier texte vers la zone requête par Mots clés.</span><span class="sxs-lookup"><span data-stu-id="62db0-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
