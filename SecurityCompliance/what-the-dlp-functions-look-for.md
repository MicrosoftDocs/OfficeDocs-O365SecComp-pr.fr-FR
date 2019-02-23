---
title: Éléments recherchés par les fonctions DLP
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Les types d'informations sensibles recherchent un modèle spécifique et le corroborent en garantissant une mise en forme appropriée, en appliquant des checksums et en recherchant des mots clés pertinents ou d'autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Cette rubrique décrit ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d'informations sensibles prédéfinis.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219354"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="568f4-105">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="568f4-105">What the DLP functions look for</span></span>

<span data-ttu-id="568f4-p102">La protection contre la perte de données (DLP) inclut des types d’informations sensibles, tels que le numéro de carte de crédit et le numéro de carte de débit de l’Union européenne, qui sont prêts à être utilisés dans vos stratégies DLP. Ces types d’informations sensibles recherchent un modèle spécifique et le corroborent en veillant à l’adéquation de la mise en forme, en appliquant des sommes de contrôle et en recherchant des mots clés pertinents ou d’autres informations. Certaines de ces fonctionnalités sont effectuées par des fonctions internes. Par exemple, le type d’informations sensibles de numéro de carte de crédit utilise une fonction pour rechercher des dates mises en forme comme une date d’expiration, pour aider à confirmer qu’un numéro est un numéro de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="568f4-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="568f4-p103">Cette rubrique explique ce que ces fonctions recherchent, pour vous aider à comprendre le fonctionnement des types d’informations sensibles prédéfinis. Pour plus d’informations, voir [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="568f4-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="568f4-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="568f4-112">Func_us_date</span></span>

<span data-ttu-id="568f4-p104">Cette fonction recherche une date au format couramment utilisé aux États-Unis. Cela inclut les formats «mois/jour/année», «mois-jour-année» et «mois de jour du mois». Les noms ou abréviations des mois ne sont pas sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="568f4-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="568f4-115">Exemples :</span><span class="sxs-lookup"><span data-stu-id="568f4-115">Examples:</span></span>
  
- <span data-ttu-id="568f4-116">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-116">December 2, 2016</span></span>
    
- <span data-ttu-id="568f4-117">2 décembre 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="568f4-118">DEC 02 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-118">dec 02 2016</span></span>
    
- <span data-ttu-id="568f4-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="568f4-119">12/2/2016</span></span>
    
- <span data-ttu-id="568f4-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="568f4-120">12/02/16</span></span>
    
- <span data-ttu-id="568f4-121">Déc-2-2016</span><span class="sxs-lookup"><span data-stu-id="568f4-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="568f4-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="568f4-122">12-2-16</span></span>
    
<span data-ttu-id="568f4-123">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="568f4-123">Accepted month names:</span></span>
  
- <span data-ttu-id="568f4-124">Anglais</span><span class="sxs-lookup"><span data-stu-id="568f4-124">English</span></span>
    
  - <span data-ttu-id="568f4-125">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="568f4-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="568f4-126">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="568f4-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="568f4-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="568f4-127">Func_eu_date</span></span>

<span data-ttu-id="568f4-p105">Cette fonction recherche une date au format couramment utilisé dans l’Union européenne (et la plupart des lieux, à l’exception des États-Unis). Cela inclut les formats de « jour/mois/année », « jour-mois-année » et « jour mois année ». Les noms ou les abréviations des mois ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="568f4-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="568f4-132">Exemples :</span><span class="sxs-lookup"><span data-stu-id="568f4-132">Examples:</span></span>
  
- <span data-ttu-id="568f4-133">2 déc 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="568f4-134">02 déc 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-134">02 dec 2016</span></span>
    
- <span data-ttu-id="568f4-135">2 déc 16</span><span class="sxs-lookup"><span data-stu-id="568f4-135">2 Dec 16</span></span>
    
- <span data-ttu-id="568f4-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="568f4-136">2/12/2016</span></span>
    
- <span data-ttu-id="568f4-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="568f4-137">02/12/16</span></span>
    
- <span data-ttu-id="568f4-138">2-déc-2016</span><span class="sxs-lookup"><span data-stu-id="568f4-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="568f4-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="568f4-139">2-12-16</span></span>
    
<span data-ttu-id="568f4-140">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="568f4-140">Accepted month names:</span></span>
  
- <span data-ttu-id="568f4-141">Anglais</span><span class="sxs-lookup"><span data-stu-id="568f4-141">English</span></span>
    
  - <span data-ttu-id="568f4-142">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="568f4-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="568f4-143">Jan. fév. Mar. mai du 1er juillet aoû. septembre. Oct. nov. déc</span><span class="sxs-lookup"><span data-stu-id="568f4-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="568f4-144">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="568f4-144">Dutch</span></span>
    
  - <span data-ttu-id="568f4-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="568f4-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="568f4-146">Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="568f4-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="568f4-147">Français</span><span class="sxs-lookup"><span data-stu-id="568f4-147">French</span></span>
    
  - <span data-ttu-id="568f4-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="568f4-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="568f4-p106">janv. févr. mars avril Maï juin juil. août sept. oct. nov. déc.</span><span class="sxs-lookup"><span data-stu-id="568f4-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="568f4-156">Allemand</span><span class="sxs-lookup"><span data-stu-id="568f4-156">German</span></span>
    
  - <span data-ttu-id="568f4-157">jänuar, Februar, März, avril, mai, Juni Juli, août, septembre, oktober, novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="568f4-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="568f4-p107">Jan./Jän. Fév. März avr. Maï Juni Juli aoû. sept. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="568f4-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="568f4-161">Italien</span><span class="sxs-lookup"><span data-stu-id="568f4-161">Italian</span></span>
    
  - <span data-ttu-id="568f4-162">gennaio, febbraio, marzo, Aprile, Maggio, Giugno, luglio, Agosto, Settembre, Ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="568f4-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="568f4-p108">Genn. febbr. détériore. avancé. Magg. giugno luglio AG. Sett. Verlag. novembre. DIC.</span><span class="sxs-lookup"><span data-stu-id="568f4-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="568f4-173">Portugais</span><span class="sxs-lookup"><span data-stu-id="568f4-173">Portuguese</span></span>
    
  - <span data-ttu-id="568f4-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="568f4-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="568f4-175">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="568f4-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="568f4-176">Espagnol</span><span class="sxs-lookup"><span data-stu-id="568f4-176">Spanish</span></span>
    
  - <span data-ttu-id="568f4-177">Enero, febrero, marzo, Abril, Mayo, junio, Julio, Agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="568f4-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="568f4-p109">enero fév. marzo abr. Mayo Jun. Jul. agosto sept./Set. oct. nov. DIC.</span><span class="sxs-lookup"><span data-stu-id="568f4-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="568f4-186">Func_eu_date1 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="568f4-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="568f4-187">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois portugais, `Func_eu_date` qui sont désormais inclus dans la fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="568f4-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="568f4-p110">Cette fonction recherche une date dans le format couramment utilisé en Portugais. Le format de cette fonction est le même que `Func_eu_date`, qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="568f4-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="568f4-190">Exemples :</span><span class="sxs-lookup"><span data-stu-id="568f4-190">Examples:</span></span>
  
- <span data-ttu-id="568f4-191">2 dez 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="568f4-192">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-192">02 dez 2016</span></span>
    
- <span data-ttu-id="568f4-193">2 dez 16</span><span class="sxs-lookup"><span data-stu-id="568f4-193">2 Dez 16</span></span>
    
- <span data-ttu-id="568f4-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="568f4-194">2/12/2016</span></span>
    
- <span data-ttu-id="568f4-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="568f4-195">02/12/16</span></span>
    
- <span data-ttu-id="568f4-196">2-dez-2016</span><span class="sxs-lookup"><span data-stu-id="568f4-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="568f4-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="568f4-197">2-12-16</span></span>
    
<span data-ttu-id="568f4-198">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="568f4-198">Accepted month names:</span></span>
  
- <span data-ttu-id="568f4-199">Portugais</span><span class="sxs-lookup"><span data-stu-id="568f4-199">Portuguese</span></span>
    
  - <span data-ttu-id="568f4-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="568f4-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="568f4-201">Jan Fev Mar Abr mai Jun Jul a été défini sur le mois de novembre dez</span><span class="sxs-lookup"><span data-stu-id="568f4-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="568f4-202">Func_eu_date2 (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="568f4-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="568f4-203">Cette fonction est déconseillée, car elle prend en charge uniquement les noms de mois néerlandais, `Func_eu_date` qui sont désormais inclus dans la fonction ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="568f4-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="568f4-p111">Cette fonction recherche une date dans le format couramment utilisé en Néerlandais. Le format de cette fonction est le même que `Func_eu_date`, qui diffère uniquement dans la langue utilisée.</span><span class="sxs-lookup"><span data-stu-id="568f4-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="568f4-206">Exemples :</span><span class="sxs-lookup"><span data-stu-id="568f4-206">Examples:</span></span>
  
- <span data-ttu-id="568f4-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="568f4-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="568f4-208">02 mei 2016</span></span>
    
- <span data-ttu-id="568f4-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="568f4-209">2 Mei 16</span></span>
    
- <span data-ttu-id="568f4-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="568f4-210">2/12/2016</span></span>
    
- <span data-ttu-id="568f4-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="568f4-211">02/12/16</span></span>
    
- <span data-ttu-id="568f4-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="568f4-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="568f4-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="568f4-213">2-12-16</span></span>
    
<span data-ttu-id="568f4-214">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="568f4-214">Accepted month names:</span></span>
  
- <span data-ttu-id="568f4-215">Néerlandais</span><span class="sxs-lookup"><span data-stu-id="568f4-215">Dutch</span></span>
    
  - <span data-ttu-id="568f4-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="568f4-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="568f4-217">Jan fév maart avr Mei Jun Jul aoû Sep sept oct OKT nov déc</span><span class="sxs-lookup"><span data-stu-id="568f4-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="568f4-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="568f4-218">Func_expiration_date</span></span>

<span data-ttu-id="568f4-p112">Cette fonction recherche une date dans les formats couramment utilisés par les cartes de crédit et de débit, ce qui exclut les jours en faveur des mois. Cette fonction correspond aux dates au format «mois/année», «mois-année», «[nom du mois] année» et «[abréviation mois-année]». Les noms ou abréviations des mois ne sont pas sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="568f4-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="568f4-222">Exemples</span><span class="sxs-lookup"><span data-stu-id="568f4-222">Examples:</span></span>
  
- <span data-ttu-id="568f4-223">MM/AA, par exemple, 01/11 ou 1/11</span><span class="sxs-lookup"><span data-stu-id="568f4-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="568f4-224">MM/AAAA, par exemple, 01/2011 ou 1/2011</span><span class="sxs-lookup"><span data-stu-id="568f4-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="568f4-225">MM-AA, par exemple, 01-22 ou 1-11</span><span class="sxs-lookup"><span data-stu-id="568f4-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="568f4-226">MM-AAAA, par exemple, 01-2000 ou 1-2000</span><span class="sxs-lookup"><span data-stu-id="568f4-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="568f4-227">Les formats suivants prennent en charge AA ou AAAA :</span><span class="sxs-lookup"><span data-stu-id="568f4-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="568f4-228">Mois-AAAA, par exemple, jan-2010, janvier-2010, jan-10 ou janvier-10</span><span class="sxs-lookup"><span data-stu-id="568f4-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="568f4-229">Mois AAAA, par exemple, « janvier 2010 », « jan 2010 », « janvier 10 » ou « jan 10 »</span><span class="sxs-lookup"><span data-stu-id="568f4-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="568f4-230">MoisAAAA, par exemple, « janvier2010 », « jan2010 », « janvier10 » ou « jan10 »</span><span class="sxs-lookup"><span data-stu-id="568f4-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="568f4-231">Mois/aaaa--par exemple, «janvier/2010» ou «Jan/2010», «janvier/10» ou «Jan/10»</span><span class="sxs-lookup"><span data-stu-id="568f4-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="568f4-232">Noms de mois acceptés :</span><span class="sxs-lookup"><span data-stu-id="568f4-232">Accepted month names:</span></span>
  
- <span data-ttu-id="568f4-233">Anglais</span><span class="sxs-lookup"><span data-stu-id="568f4-233">English</span></span>
    
  - <span data-ttu-id="568f4-234">Janvier, février, mars, avril, mai, juin, juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="568f4-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="568f4-235">Jan Fév Mar Avr mai juin septembre sept octobre déc</span><span class="sxs-lookup"><span data-stu-id="568f4-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="568f4-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="568f4-236">Func_us_address</span></span>

<span data-ttu-id="568f4-p113">Cette fonction recherche un nom d’état américain ou son abréviation postale, suivi d’un code postal valide, au format utilisé dans les adresses postales. Le code postal doit être l’un des codes postaux corrects qui sont associés au nom de l’état américain ou à son abréviation. Le nom de l’état américain et le code postal ne doivent pas être séparés par des signes de ponctuation ou des lettres.</span><span class="sxs-lookup"><span data-stu-id="568f4-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="568f4-240">Exemples :</span><span class="sxs-lookup"><span data-stu-id="568f4-240">Examples:</span></span>
  
- <span data-ttu-id="568f4-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="568f4-241">Washington 98052</span></span>
    
- <span data-ttu-id="568f4-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="568f4-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="568f4-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="568f4-243">WA 98052</span></span>
    
- <span data-ttu-id="568f4-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="568f4-244">WA 98052-9998</span></span>
    

