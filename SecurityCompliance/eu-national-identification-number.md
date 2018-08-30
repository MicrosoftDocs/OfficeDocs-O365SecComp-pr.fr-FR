---
title: Numéro d’Identification nationales de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de l’UE National. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528043"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="f36b1-104">Numéro d’Identification nationales de l’UE</span><span class="sxs-lookup"><span data-stu-id="f36b1-104">EU National Identification Number</span></span>

<span data-ttu-id="f36b1-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de l’UE National. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="f36b1-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="f36b1-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="f36b1-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-108">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-108">Format</span></span>

<span data-ttu-id="f36b1-109">Une combinaison de caractères 24 des lettres, chiffres et caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="f36b1-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-110">Pattern</span></span>

<span data-ttu-id="f36b1-111">24 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-111">24 characters:</span></span>
  
-  <span data-ttu-id="f36b1-112">22 (pas la casse) lettres, chiffres, barres obliques inverses, barres obliques ou signes plus</span><span class="sxs-lookup"><span data-stu-id="f36b1-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="f36b1-113">(Pas la casse) de deux lettres, chiffres, barres obliques inverses, obliques, signes plus ou signe égal</span><span class="sxs-lookup"><span data-stu-id="f36b1-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-114">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-114">Checksum</span></span>

<span data-ttu-id="f36b1-115">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f36b1-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-116">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-116">Definition</span></span>

<span data-ttu-id="f36b1-117">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-118">L’expression régulière `Regex_austria_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-119">Un mot clé à partir de `Keywords_austria_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-120">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="f36b1-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-122">numéro d’identification autrichien</span><span class="sxs-lookup"><span data-stu-id="f36b1-122">austrian identity number</span></span>
  
<span data-ttu-id="f36b1-123">numéro d’identité national</span><span class="sxs-lookup"><span data-stu-id="f36b1-123">national identity number</span></span>
  
<span data-ttu-id="f36b1-124">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="f36b1-124">identity number</span></span>
  
<span data-ttu-id="f36b1-125">
id national</span><span class="sxs-lookup"><span data-stu-id="f36b1-125">national id</span></span>
  
<span data-ttu-id="f36b1-126">personalausweis Slovaquie österreich</span><span class="sxs-lookup"><span data-stu-id="f36b1-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="f36b1-127">Belgique</span><span class="sxs-lookup"><span data-stu-id="f36b1-127">Belgium</span></span>

<span data-ttu-id="f36b1-128">Pour plus d’informations, voir la section « Numéro National Belgique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="f36b1-129">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="f36b1-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-130">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-130">Format</span></span>

<span data-ttu-id="f36b1-131">Dix chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-132">Pattern</span></span>

<span data-ttu-id="f36b1-133">Dix chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="f36b1-134">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f36b1-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f36b1-135">Deux chiffres qui correspondent à l’ordre de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="f36b1-136">Un chiffre correspondant au sexe : un chiffre pair pour masculin et un chiffre impair pour femme</span><span class="sxs-lookup"><span data-stu-id="f36b1-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="f36b1-137">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-138">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-138">Checksum</span></span>

<span data-ttu-id="f36b1-139">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-140">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-140">Definition</span></span>

<span data-ttu-id="f36b1-141">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-142">La fonction `Func_bulgaria_national_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-143">Un mot clé à partir de `Keywords_bulgaria_national_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="f36b1-144">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-145">La fonction `Func_bulgaria_national_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="f36b1-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="f36b1-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="f36b1-148">egn</span><span class="sxs-lookup"><span data-stu-id="f36b1-148">egn</span></span>
  
<span data-ttu-id="f36b1-149">egn #</span><span class="sxs-lookup"><span data-stu-id="f36b1-149">egn#</span></span>
  
<span data-ttu-id="f36b1-150">bulgare numéro national</span><span class="sxs-lookup"><span data-stu-id="f36b1-150">bulgarian national number</span></span>
  
<span data-ttu-id="f36b1-151">numéro national</span><span class="sxs-lookup"><span data-stu-id="f36b1-151">national number</span></span>
  
<span data-ttu-id="f36b1-152">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="f36b1-152">social security number</span></span>
  
<span data-ttu-id="f36b1-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-153">nationalnumber#</span></span>
  
<span data-ttu-id="f36b1-154">ssn #</span><span class="sxs-lookup"><span data-stu-id="f36b1-154">ssn#</span></span>
  
<span data-ttu-id="f36b1-155">ssn</span><span class="sxs-lookup"><span data-stu-id="f36b1-155">ssn</span></span>
  
<span data-ttu-id="f36b1-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="f36b1-156">nationalnumber</span></span>
  
<span data-ttu-id="f36b1-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="f36b1-157">bnn#</span></span>
  
<span data-ttu-id="f36b1-158">bnn</span><span class="sxs-lookup"><span data-stu-id="f36b1-158">bnn</span></span>
  
<span data-ttu-id="f36b1-159">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-159">personal id number</span></span>
  
<span data-ttu-id="f36b1-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-160">personalidnumber#</span></span>
  
<span data-ttu-id="f36b1-161">ЕДИНЕН ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="f36b1-161">единен граждански номер</span></span>
  
<span data-ttu-id="f36b1-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="f36b1-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="f36b1-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="f36b1-163">егн</span></span>
  
<span data-ttu-id="f36b1-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="f36b1-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="f36b1-165">Croatie</span><span class="sxs-lookup"><span data-stu-id="f36b1-165">Croatia</span></span>

<span data-ttu-id="f36b1-166">Pour plus d’informations, consultez la section « Croatie Identity Number » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="f36b1-167">Chypre</span><span class="sxs-lookup"><span data-stu-id="f36b1-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-168">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-168">Format</span></span>

<span data-ttu-id="f36b1-169">Dix chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-170">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-170">Pattern</span></span>

 <span data-ttu-id="f36b1-171">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="f36b1-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="f36b1-172">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-172">Checksum</span></span>

<span data-ttu-id="f36b1-173">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f36b1-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-174">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-174">Definition</span></span>

<span data-ttu-id="f36b1-175">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-176">L’expression régulière `Regex_cyprus_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-177">Un mot clé à partir de `Keywords_cyprus_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-178">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="f36b1-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-180">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="f36b1-180">id card number</span></span>
  
<span data-ttu-id="f36b1-181">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f36b1-181">national identification number</span></span>
  
<span data-ttu-id="f36b1-182">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-182">personal id number</span></span>
  
<span data-ttu-id="f36b1-183">numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="f36b1-183">identity card number</span></span>
  
<span data-ttu-id="f36b1-184">ΤΑΥΤΟΤΗΤΑΣ</span><span class="sxs-lookup"><span data-stu-id="f36b1-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="f36b1-185">République tchèque</span><span class="sxs-lookup"><span data-stu-id="f36b1-185">Czech Republic</span></span>

<span data-ttu-id="f36b1-186">Pour plus d’informations, consultez la section « Numéro d’identité National tchèque » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="f36b1-187">Danemark</span><span class="sxs-lookup"><span data-stu-id="f36b1-187">Denmark</span></span>

<span data-ttu-id="f36b1-188">Pour plus d’informations, consultez la section « Numéro d’Identification personnelle Danemark » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="f36b1-189">Estonie</span><span class="sxs-lookup"><span data-stu-id="f36b1-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-190">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-190">Format</span></span>

<span data-ttu-id="f36b1-191">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-192">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-192">Pattern</span></span>

<span data-ttu-id="f36b1-193">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f36b1-193">11 digits:</span></span>
  
- <span data-ttu-id="f36b1-194">Un chiffre correspondant au sexe et century de naissance (masculin nombre impair, nombre pair féminin ; 1-2 : 19 century ; 3-4 : 20 century ; 5-6 : century 21)</span><span class="sxs-lookup"><span data-stu-id="f36b1-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="f36b1-195">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f36b1-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="f36b1-196">Trois chiffres qui correspondent à un numéro de série en séparant les personnes naissance à la même date</span><span class="sxs-lookup"><span data-stu-id="f36b1-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="f36b1-197">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-198">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-198">Checksum</span></span>

<span data-ttu-id="f36b1-199">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-200">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-200">Definition</span></span>

<span data-ttu-id="f36b1-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-202">La fonction `Func_estonia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-203">Un mot clé à partir de `Keywords_estonia_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-204">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-205">La fonction `Func_estonia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-206">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="f36b1-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-208">code d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-208">personal identification code</span></span>
  
<span data-ttu-id="f36b1-209">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-209">personal identification number</span></span>
  
<span data-ttu-id="f36b1-210">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f36b1-210">national identification number</span></span>
  
<span data-ttu-id="f36b1-211">numéro national</span><span class="sxs-lookup"><span data-stu-id="f36b1-211">national number</span></span>
  
<span data-ttu-id="f36b1-212">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-212">personal id number</span></span>
  
<span data-ttu-id="f36b1-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-213">personalidnumber#</span></span>
  
<span data-ttu-id="f36b1-214">IK</span><span class="sxs-lookup"><span data-stu-id="f36b1-214">ik</span></span>
  
<span data-ttu-id="f36b1-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="f36b1-215">isikukood</span></span>
  
<span data-ttu-id="f36b1-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="f36b1-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="f36b1-217">Finlande</span><span class="sxs-lookup"><span data-stu-id="f36b1-217">Finland</span></span>

<span data-ttu-id="f36b1-218">Pour plus d’informations, voir la section « ID National Finlande » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="f36b1-219">France</span><span class="sxs-lookup"><span data-stu-id="f36b1-219">France</span></span>

<span data-ttu-id="f36b1-220">Pour plus d’informations, consultez la section « France National carte d’identité (CNI) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="f36b1-221">Allemagne</span><span class="sxs-lookup"><span data-stu-id="f36b1-221">Germany</span></span>

<span data-ttu-id="f36b1-222">Pour plus d’informations, consultez la section « Numéro de carte d’identité Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="f36b1-223">Grèce</span><span class="sxs-lookup"><span data-stu-id="f36b1-223">Greece</span></span>

<span data-ttu-id="f36b1-224">Pour plus d’informations, consultez la section « Grèce carte » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="f36b1-225">Hongrie</span><span class="sxs-lookup"><span data-stu-id="f36b1-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-226">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-226">Format</span></span>

<span data-ttu-id="f36b1-227">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="f36b1-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-228">Pattern</span></span>

<span data-ttu-id="f36b1-229">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="f36b1-229">11 digits:</span></span>
  
-  <span data-ttu-id="f36b1-230">Un chiffre correspondant au sexe (masculin-1, 2-femme, autres numéros sont également possibles pour les citoyens naissance 1900 ou aux citoyens citoyenneté double)</span><span class="sxs-lookup"><span data-stu-id="f36b1-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="f36b1-231">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f36b1-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="f36b1-232">Trois chiffres qui correspondent à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="f36b1-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="f36b1-233">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-234">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-234">Checksum</span></span>

<span data-ttu-id="f36b1-235">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-236">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-236">Definition</span></span>

<span data-ttu-id="f36b1-237">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-238">La fonction `Func_hungary_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-239">Un mot clé à partir de `Keywords_hungary_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-240">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-241">La fonction `Func_hungary_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-242">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="f36b1-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-244">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-244">personal identification number</span></span>
  
<span data-ttu-id="f36b1-245">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="f36b1-245">identification number</span></span>
  
<span data-ttu-id="f36b1-246">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-246">personal id number</span></span>
  
<span data-ttu-id="f36b1-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="f36b1-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="f36b1-248">Irlande</span><span class="sxs-lookup"><span data-stu-id="f36b1-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-249">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-249">Format</span></span>

<span data-ttu-id="f36b1-250">Une combinaison de caractères neuf des lettres, chiffres et un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f36b1-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-251">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-251">Pattern</span></span>

<span data-ttu-id="f36b1-252">Une combinaison de caractères neuf des lettres, chiffres et un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f36b1-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="f36b1-253">À partir du 01 janvier 2013 jusqu'à maintenant :</span><span class="sxs-lookup"><span data-stu-id="f36b1-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="f36b1-254">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f36b1-254">Seven digits</span></span> 
    
- <span data-ttu-id="f36b1-255">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-255">One check digit</span></span>
    
- <span data-ttu-id="f36b1-256">Un espace ou la lettre « W » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f36b1-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="f36b1-257">Avant de janvier 2013 01 :</span><span class="sxs-lookup"><span data-stu-id="f36b1-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="f36b1-258">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f36b1-258">Seven digits</span></span> 
    
- <span data-ttu-id="f36b1-259">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-259">One check digit</span></span>
    
- <span data-ttu-id="f36b1-260">Un espace ou une lettre majuscule (respecter la casse)</span><span class="sxs-lookup"><span data-stu-id="f36b1-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-261">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-261">Checksum</span></span>

<span data-ttu-id="f36b1-262">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-263">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-263">Definition</span></span>

<span data-ttu-id="f36b1-264">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-265">La fonction de recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="f36b1-266">Un mot clé à partir d’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f36b1-266">A keyword from is found.</span></span>
    
<span data-ttu-id="f36b1-267">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-268">La fonction de recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-268">The function finds content that matches the pattern.</span></span>
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-269">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="f36b1-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-271">numéro personnel service public</span><span class="sxs-lookup"><span data-stu-id="f36b1-271">personal public service number</span></span>
  
<span data-ttu-id="f36b1-272">PPS aucune</span><span class="sxs-lookup"><span data-stu-id="f36b1-272">pps no</span></span>
  
<span data-ttu-id="f36b1-273">numéro d’assurance sociale et de chiffre d’affaires</span><span class="sxs-lookup"><span data-stu-id="f36b1-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="f36b1-274">RSI aucune</span><span class="sxs-lookup"><span data-stu-id="f36b1-274">rsi no</span></span>
  
<span data-ttu-id="f36b1-275">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-275">personal identification number</span></span>
  
<span data-ttu-id="f36b1-276">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="f36b1-276">identification number</span></span>
  
<span data-ttu-id="f36b1-277">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-277">personal id number</span></span>
  
<span data-ttu-id="f36b1-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="f36b1-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="f36b1-p103">uimh. PSP</span><span class="sxs-lookup"><span data-stu-id="f36b1-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="f36b1-281">Italie</span><span class="sxs-lookup"><span data-stu-id="f36b1-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-282">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-282">Format</span></span>

<span data-ttu-id="f36b1-283">Une combinaison de 16 caractères de lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="f36b1-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-284">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-284">Pattern</span></span>

<span data-ttu-id="f36b1-285">Une combinaison de 16 caractères de lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="f36b1-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="f36b1-286">Trois lettres qui correspondent aux trois premiers consonnes suivantes dans le nom de famille</span><span class="sxs-lookup"><span data-stu-id="f36b1-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="f36b1-287">Trois lettres qui correspondent à la première, troisième et quatrième consonnes dans le premier nom</span><span class="sxs-lookup"><span data-stu-id="f36b1-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="f36b1-288">Deux chiffres qui correspondent à la dernière chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="f36b1-289">Une lettre qui correspond à la lettre pour le mois de naissance — lettres sont utilisés dans l’ordre alphabétique, mais que les lettres A à E, H, L, M, P, R t sont utilisés (par conséquent, janvier correspond à un et octobre est R)</span><span class="sxs-lookup"><span data-stu-id="f36b1-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="f36b1-290">Deux chiffres correspondant au jour du mois de naissance — afin de différencier sexe, 40 est ajouté à la journée de naissance pour femme</span><span class="sxs-lookup"><span data-stu-id="f36b1-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="f36b1-291">Quatre chiffres qui correspond à l’indicatif régional spécifique à la commune où naissance de la personne (codes de pays échelle sont utilisés pour étranger)</span><span class="sxs-lookup"><span data-stu-id="f36b1-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="f36b1-292">Un chiffre parité</span><span class="sxs-lookup"><span data-stu-id="f36b1-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-293">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-293">Checksum</span></span>

<span data-ttu-id="f36b1-294">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-295">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-295">Definition</span></span>

<span data-ttu-id="f36b1-296">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-297">La fonction `Func_italy_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-298">Un mot clé à partir de `Keywords_italy_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-299">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-300">La fonction `Func_italy_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-301">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="f36b1-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-303">code personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-303">personal code</span></span>
  
<span data-ttu-id="f36b1-304">numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-304">personal code number</span></span>
  
<span data-ttu-id="f36b1-305">nombre de certificats personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-305">personal certificate number</span></span>
  
<span data-ttu-id="f36b1-306">code fiscal</span><span class="sxs-lookup"><span data-stu-id="f36b1-306">fiscal code</span></span>
  
<span data-ttu-id="f36b1-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-307">personalcodeno#</span></span>
  
<span data-ttu-id="f36b1-308">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-308">personal id number</span></span>
  
<span data-ttu-id="f36b1-309">code d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-309">personal id code</span></span>
  
<span data-ttu-id="f36b1-310">numéro d’identification personale</span><span class="sxs-lookup"><span data-stu-id="f36b1-310">codice personale</span></span>
  
<span data-ttu-id="f36b1-311">NUMERO certificato personale</span><span class="sxs-lookup"><span data-stu-id="f36b1-311">numero certificato personale</span></span>
  
<span data-ttu-id="f36b1-312">NUMERO personale</span><span class="sxs-lookup"><span data-stu-id="f36b1-312">numero personale</span></span>
  
<span data-ttu-id="f36b1-313">NUMERO id personale</span><span class="sxs-lookup"><span data-stu-id="f36b1-313">numero id personale</span></span>
  
<span data-ttu-id="f36b1-314">numéro d’identification id personale</span><span class="sxs-lookup"><span data-stu-id="f36b1-314">codice id personale</span></span>
  
<span data-ttu-id="f36b1-315">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="f36b1-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="f36b1-316">Italie</span><span class="sxs-lookup"><span data-stu-id="f36b1-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-317">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-317">Format</span></span>

<span data-ttu-id="f36b1-318">11 chiffres et un trait d’union dans le format spécifié</span><span class="sxs-lookup"><span data-stu-id="f36b1-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-319">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-319">Pattern</span></span>

<span data-ttu-id="f36b1-320">11 chiffres et un trait d’union :</span><span class="sxs-lookup"><span data-stu-id="f36b1-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="f36b1-321">Six chiffres qui correspondent à la date de naissance (jjmmaa)</span><span class="sxs-lookup"><span data-stu-id="f36b1-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="f36b1-322">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="f36b1-322">A hyphen</span></span>
    
- <span data-ttu-id="f36b1-323">Un chiffre qui correspond à la century de naissance (« 0 » pour century 19, « 1 » pour le vingtième century et « 2 » pour century 21)</span><span class="sxs-lookup"><span data-stu-id="f36b1-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="f36b1-324">Quatre chiffres, générées de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="f36b1-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-325">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-325">Checksum</span></span>

<span data-ttu-id="f36b1-326">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-327">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-327">Definition</span></span>

<span data-ttu-id="f36b1-328">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-329">La fonction `Func_latvia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-330">Un mot clé à partir de `Keywords_latvia_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-331">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-332">La fonction `Func_latvia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-333">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="f36b1-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-335">code personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-335">personal code</span></span>
  
<span data-ttu-id="f36b1-336">numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-336">personal code number</span></span>
  
<span data-ttu-id="f36b1-337">nombre de certificats personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-337">personal certificate number</span></span>
  
<span data-ttu-id="f36b1-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-338">personalcodeno#</span></span>
  
<span data-ttu-id="f36b1-339">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-339">personal id number</span></span>
  
<span data-ttu-id="f36b1-340">code d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-340">personal id code</span></span>
  
<span data-ttu-id="f36b1-341">personnages kods</span><span class="sxs-lookup"><span data-stu-id="f36b1-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="f36b1-342">Lituanie</span><span class="sxs-lookup"><span data-stu-id="f36b1-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-343">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-343">Format</span></span>

<span data-ttu-id="f36b1-344">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-345">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-345">Pattern</span></span>

<span data-ttu-id="f36b1-346">11 chiffres sans espaces et les séparateurs :</span><span class="sxs-lookup"><span data-stu-id="f36b1-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="f36b1-347">Un chiffre qui correspond à la personne sexe et century de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="f36b1-348">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f36b1-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f36b1-349">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="f36b1-350">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-351">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-351">Checksum</span></span>

<span data-ttu-id="f36b1-352">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-353">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-353">Definition</span></span>

<span data-ttu-id="f36b1-354">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-355">La fonction `Func_lithuania_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-356">Un mot clé à partir de `Keywords_lithuania_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-357">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-358">La fonction `Func_lithuania_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-359">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="f36b1-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-361">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-361">personal numeric code</span></span>
  
<span data-ttu-id="f36b1-362">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-362">unique identification number</span></span>
  
<span data-ttu-id="f36b1-363">numéro de service citoyens</span><span class="sxs-lookup"><span data-stu-id="f36b1-363">citizen service number</span></span>
  
<span data-ttu-id="f36b1-364">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-364">unique identity number</span></span>
  
<span data-ttu-id="f36b1-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="f36b1-366">code personnel.</span><span class="sxs-lookup"><span data-stu-id="f36b1-366">personal code.</span></span>
  
<span data-ttu-id="f36b1-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="f36b1-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="f36b1-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="f36b1-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="f36b1-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="f36b1-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="f36b1-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="f36b1-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="f36b1-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="f36b1-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="f36b1-372">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="f36b1-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-373">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-373">Format</span></span>

<span data-ttu-id="f36b1-374">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-375">Pattern</span></span>

<span data-ttu-id="f36b1-376">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="f36b1-376">11 digits</span></span>
  
- <span data-ttu-id="f36b1-377">Un chiffre qui correspond à la personne sexe et century de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="f36b1-378">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="f36b1-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="f36b1-379">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="f36b1-380">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-381">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-381">Checksum</span></span>

<span data-ttu-id="f36b1-382">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f36b1-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-383">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-383">Definition</span></span>

<span data-ttu-id="f36b1-384">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-385">L’expression régulière `Regex_luxemburg_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-386">Un mot clé à partir de `Keywords_luxemburg_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="f36b1-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-389">identifiant personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-389">personal id</span></span>
  
<span data-ttu-id="f36b1-390">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-390">personal id number</span></span>
  
<span data-ttu-id="f36b1-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-391">personalidno#</span></span>
  
<span data-ttu-id="f36b1-392">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-392">unique id number</span></span>
  
<span data-ttu-id="f36b1-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-393">personalidnumber#</span></span>
  
<span data-ttu-id="f36b1-394">clé de l’id unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-394">unique id key</span></span>
  
<span data-ttu-id="f36b1-395">code d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-395">personal id code</span></span>
  
<span data-ttu-id="f36b1-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="f36b1-396">uniqueidkey#</span></span>
  
<span data-ttu-id="f36b1-397">code individuels</span><span class="sxs-lookup"><span data-stu-id="f36b1-397">individual code</span></span>
  
<span data-ttu-id="f36b1-398">id individuel</span><span class="sxs-lookup"><span data-stu-id="f36b1-398">individual id</span></span>
  
<span data-ttu-id="f36b1-399">id d’eindeutige-nummer</span><span class="sxs-lookup"><span data-stu-id="f36b1-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="f36b1-400">id eindeutige</span><span class="sxs-lookup"><span data-stu-id="f36b1-400">eindeutige id</span></span>
  
<span data-ttu-id="f36b1-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-401">id personnelle</span></span>
  
<span data-ttu-id="f36b1-402">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="f36b1-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="f36b1-403">idpersonnelle#</span></span>
  
<span data-ttu-id="f36b1-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="f36b1-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="f36b1-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="f36b1-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="f36b1-406">Malte</span><span class="sxs-lookup"><span data-stu-id="f36b1-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-407">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-407">Format</span></span>

<span data-ttu-id="f36b1-408">Sept chiffres suivies d’une lettre</span><span class="sxs-lookup"><span data-stu-id="f36b1-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-409">Pattern</span></span>

<span data-ttu-id="f36b1-410">Sept chiffres suivies d’une lettre :</span><span class="sxs-lookup"><span data-stu-id="f36b1-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="f36b1-411">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f36b1-411">Seven digits</span></span> 
    
- <span data-ttu-id="f36b1-412">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="f36b1-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-413">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-413">Checksum</span></span>

<span data-ttu-id="f36b1-414">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f36b1-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-415">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-415">Definition</span></span>

<span data-ttu-id="f36b1-416">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-417">L’expression régulière `Regex_malta_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-418">Un mot clé à partir de `Keywords_malta_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-419">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-420">L’expression régulière `Regex_malta_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-421">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="f36b1-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-423">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-423">personal numeric code</span></span>
  
<span data-ttu-id="f36b1-424">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-424">unique identification number</span></span>
  
<span data-ttu-id="f36b1-425">numéro de service citoyens</span><span class="sxs-lookup"><span data-stu-id="f36b1-425">citizen service number</span></span>
  
<span data-ttu-id="f36b1-426">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-426">unique identity number</span></span>
  
<span data-ttu-id="f36b1-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="f36b1-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="f36b1-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="f36b1-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="f36b1-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="f36b1-430">numru tas-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="f36b1-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="f36b1-431">numru ta' identità uniku</span><span class="sxs-lookup"><span data-stu-id="f36b1-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="f36b1-432">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="f36b1-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-433">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-433">Format</span></span>

<span data-ttu-id="f36b1-434">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-435">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-435">Pattern</span></span>

<span data-ttu-id="f36b1-436">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="f36b1-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f36b1-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-437">Checksum</span></span>

<span data-ttu-id="f36b1-438">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-439">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-439">Definition</span></span>

<span data-ttu-id="f36b1-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-441">La fonction `Func_netherlands_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-442">Un mot clé à partir d’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="f36b1-442">A keyword from is found.</span></span>
    
<span data-ttu-id="f36b1-443">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-444">La fonction `Func_netherlands_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-445">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="f36b1-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-447">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-447">personal numeric code</span></span>
  
<span data-ttu-id="f36b1-448">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-448">unique identification number</span></span>
  
<span data-ttu-id="f36b1-449">numéro de service citoyens</span><span class="sxs-lookup"><span data-stu-id="f36b1-449">citizen service number</span></span>
  
<span data-ttu-id="f36b1-450">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-450">unique identity number</span></span>
  
<span data-ttu-id="f36b1-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="f36b1-452">bsn</span><span class="sxs-lookup"><span data-stu-id="f36b1-452">bsn</span></span>
  
<span data-ttu-id="f36b1-453">bsn #</span><span class="sxs-lookup"><span data-stu-id="f36b1-453">bsn#</span></span>
  
<span data-ttu-id="f36b1-454">code de numerieke persoonlijke</span><span class="sxs-lookup"><span data-stu-id="f36b1-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="f36b1-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="f36b1-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="f36b1-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="f36b1-456">burgerservicenummer</span></span>
  
<span data-ttu-id="f36b1-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="f36b1-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="f36b1-458">Pologne</span><span class="sxs-lookup"><span data-stu-id="f36b1-458">Poland</span></span>

<span data-ttu-id="f36b1-459">Pour plus d’informations, consultez la section « Pologne National ID (PESEL) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="f36b1-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="f36b1-460">Portugal</span></span>

<span data-ttu-id="f36b1-461">Pour plus d’informations, consultez la section « Portugal citoyens carte numéro » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="f36b1-462">Roumanie</span><span class="sxs-lookup"><span data-stu-id="f36b1-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-463">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-463">Format</span></span>

<span data-ttu-id="f36b1-464">13 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-465">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-465">Pattern</span></span>

<span data-ttu-id="f36b1-466">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="f36b1-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f36b1-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-467">Checksum</span></span>

<span data-ttu-id="f36b1-468">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-469">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-469">Definition</span></span>

<span data-ttu-id="f36b1-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-471">La fonction `Func_romania_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-472">Un mot clé à partir de `Keywords_romania_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-474">La fonction `Func_romania_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-475">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="f36b1-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-477">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-477">personal numeric code</span></span>
  
<span data-ttu-id="f36b1-478">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-478">unique identification number</span></span>
  
<span data-ttu-id="f36b1-479">cnp</span><span class="sxs-lookup"><span data-stu-id="f36b1-479">cnp</span></span>
  
<span data-ttu-id="f36b1-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="f36b1-480">cnp#</span></span>
  
<span data-ttu-id="f36b1-481">épingler</span><span class="sxs-lookup"><span data-stu-id="f36b1-481">pin</span></span>
  
<span data-ttu-id="f36b1-482">code confidentiel #</span><span class="sxs-lookup"><span data-stu-id="f36b1-482">pin#</span></span>
  
<span data-ttu-id="f36b1-483">numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="f36b1-483">insurance number</span></span>
  
<span data-ttu-id="f36b1-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-484">insurancenumber#</span></span>
  
<span data-ttu-id="f36b1-485">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-485">unique identity number</span></span>
  
<span data-ttu-id="f36b1-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="f36b1-487">remboursement numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-487">cod numeric personal</span></span>
  
<span data-ttu-id="f36b1-488">cabillaud identificare personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-488">cod identificare personal</span></span>
  
<span data-ttu-id="f36b1-489">remboursement unic identificare</span><span class="sxs-lookup"><span data-stu-id="f36b1-489">cod unic identificare</span></span>
  
<span data-ttu-id="f36b1-490">unic personnel număr</span><span class="sxs-lookup"><span data-stu-id="f36b1-490">număr personal unic</span></span>
  
<span data-ttu-id="f36b1-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="f36b1-491">număr identitate</span></span>
  
<span data-ttu-id="f36b1-492">identificare număr personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-492">număr identificare personal</span></span>
  
<span data-ttu-id="f36b1-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="f36b1-493">număridentitate#</span></span>
  
<span data-ttu-id="f36b1-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="f36b1-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="f36b1-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="f36b1-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="f36b1-496">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="f36b1-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-497">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-497">Format</span></span>

<span data-ttu-id="f36b1-498">Dix chiffres contenant une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="f36b1-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-499">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-499">Pattern</span></span>

<span data-ttu-id="f36b1-500">Dix chiffres contenant une barre oblique inverse :</span><span class="sxs-lookup"><span data-stu-id="f36b1-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="f36b1-501">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-501">Checksum</span></span>

<span data-ttu-id="f36b1-502">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-503">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-503">Definition</span></span>

<span data-ttu-id="f36b1-504">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-505">La fonction `Func_slovakia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-506">Un mot clé à partir de `Keywords_slovakia_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-508">La fonction `Func_slovakia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-509">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="f36b1-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-511">nombre de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-511">birth number</span></span>
  
<span data-ttu-id="f36b1-512">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f36b1-512">national identification number</span></span>
  
<span data-ttu-id="f36b1-513">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-513">personal identification number</span></span>
  
<span data-ttu-id="f36b1-514">numéro de sécurité sociale
</span><span class="sxs-lookup"><span data-stu-id="f36b1-514">social security number</span></span>
  
<span data-ttu-id="f36b1-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-515">nationalnumber#</span></span>
  
<span data-ttu-id="f36b1-516">ssn #</span><span class="sxs-lookup"><span data-stu-id="f36b1-516">ssn#</span></span>
  
<span data-ttu-id="f36b1-517">ssn</span><span class="sxs-lookup"><span data-stu-id="f36b1-517">ssn</span></span>
  
<span data-ttu-id="f36b1-518">numéro national</span><span class="sxs-lookup"><span data-stu-id="f36b1-518">national number</span></span>
  
<span data-ttu-id="f36b1-519">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="f36b1-519">personal id number</span></span>
  
<span data-ttu-id="f36b1-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="f36b1-520">personalidnumber#</span></span>
  
<span data-ttu-id="f36b1-521">rč</span><span class="sxs-lookup"><span data-stu-id="f36b1-521">rč</span></span>
  
<span data-ttu-id="f36b1-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="f36b1-522">rodné číslo</span></span>
  
<span data-ttu-id="f36b1-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="f36b1-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="f36b1-524">Slovénie</span><span class="sxs-lookup"><span data-stu-id="f36b1-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-525">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-525">Format</span></span>

<span data-ttu-id="f36b1-526">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="f36b1-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-527">Pattern</span></span>

<span data-ttu-id="f36b1-528">13 chiffres dans le modèle spécifié :</span><span class="sxs-lookup"><span data-stu-id="f36b1-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="f36b1-529">Sept chiffres qui correspondent à la date de naissance (DDMMLLL) où « LLL » correspond à la dernière trois chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="f36b1-530">Deux chiffres qui correspondent à la zone de naissance</span><span class="sxs-lookup"><span data-stu-id="f36b1-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="f36b1-531">Trois chiffres qui correspondent à une combinaison de sexe et le numéro de série pour les personnes naissance le même jour (000-499 pour masculin) et 500-999 pour femme</span><span class="sxs-lookup"><span data-stu-id="f36b1-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="f36b1-532">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-533">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-533">Checksum</span></span>

<span data-ttu-id="f36b1-534">Oui</span><span class="sxs-lookup"><span data-stu-id="f36b1-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-535">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-535">Definition</span></span>

<span data-ttu-id="f36b1-536">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-537">La fonction `Func_slovenia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-538">Un mot clé à partir de `Keywords_slovenia_eu_national_id_card` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="f36b1-539">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-540">La fonction `Func_slovenia_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-541">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="f36b1-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-543">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-543">personal numeric code</span></span>
  
<span data-ttu-id="f36b1-544">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-544">unique identification number</span></span>
  
<span data-ttu-id="f36b1-545">numéro d’enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-545">unique registration number</span></span>
  
<span data-ttu-id="f36b1-546">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-546">unique identity number</span></span>
  
<span data-ttu-id="f36b1-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="f36b1-548">numéro unique citoyens maître</span><span class="sxs-lookup"><span data-stu-id="f36b1-548">unique master citizen number</span></span>
  
<span data-ttu-id="f36b1-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="f36b1-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="f36b1-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="f36b1-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="f36b1-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="f36b1-552">emšo</span><span class="sxs-lookup"><span data-stu-id="f36b1-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="f36b1-553">Espagne</span><span class="sxs-lookup"><span data-stu-id="f36b1-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="f36b1-554">Format</span><span class="sxs-lookup"><span data-stu-id="f36b1-554">Format</span></span>

<span data-ttu-id="f36b1-555">Sept chiffres suivies d’un caractère</span><span class="sxs-lookup"><span data-stu-id="f36b1-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="f36b1-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="f36b1-556">Pattern</span></span>

<span data-ttu-id="f36b1-557">Sept chiffres suivies d’un caractère</span><span class="sxs-lookup"><span data-stu-id="f36b1-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="f36b1-558">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="f36b1-558">Seven digits</span></span>
    
- <span data-ttu-id="f36b1-559">Un chiffre ou une lettre (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="f36b1-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="f36b1-560">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="f36b1-560">Checksum</span></span>

<span data-ttu-id="f36b1-561">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f36b1-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="f36b1-562">Définition</span><span class="sxs-lookup"><span data-stu-id="f36b1-562">Definition</span></span>

<span data-ttu-id="f36b1-563">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="f36b1-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="f36b1-564">L’expression régulière `Regex_spain_eu_national_id_card` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="f36b1-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="f36b1-565">Un mot clé à partir de `Keywords_spain_eu_national_id_card"` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="f36b1-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="f36b1-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="f36b1-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="f36b1-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="f36b1-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="f36b1-568">DNI</span><span class="sxs-lookup"><span data-stu-id="f36b1-568">dni</span></span>
  
<span data-ttu-id="f36b1-569">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="f36b1-569">national identification number</span></span>
  
<span data-ttu-id="f36b1-570">numéro d’identité national</span><span class="sxs-lookup"><span data-stu-id="f36b1-570">national identity number</span></span>
  
<span data-ttu-id="f36b1-571">numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="f36b1-571">insurance number</span></span>
  
<span data-ttu-id="f36b1-572">numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="f36b1-572">personal identification number</span></span>
  
<span data-ttu-id="f36b1-573">identité nationale</span><span class="sxs-lookup"><span data-stu-id="f36b1-573">national identity</span></span>
  
<span data-ttu-id="f36b1-574">identité personnelle aucune</span><span class="sxs-lookup"><span data-stu-id="f36b1-574">personal identity no</span></span>
  
<span data-ttu-id="f36b1-575">numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="f36b1-575">unique identity number</span></span>
  
<span data-ttu-id="f36b1-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="f36b1-576">nationalidno#</span></span>
  
<span data-ttu-id="f36b1-577">UniqueID #</span><span class="sxs-lookup"><span data-stu-id="f36b1-577">uniqueid#</span></span>
  
<span data-ttu-id="f36b1-578">DNI #</span><span class="sxs-lookup"><span data-stu-id="f36b1-578">dni#</span></span>
  
<span data-ttu-id="f36b1-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="f36b1-579">nationalid#</span></span>
  
<span data-ttu-id="f36b1-580">NIE #</span><span class="sxs-lookup"><span data-stu-id="f36b1-580">nie#</span></span>
  
<span data-ttu-id="f36b1-581">NIE</span><span class="sxs-lookup"><span data-stu-id="f36b1-581">nie</span></span>
  
<span data-ttu-id="f36b1-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="f36b1-582">nienúmero#</span></span>
  
<span data-ttu-id="f36b1-583">NIE número</span><span class="sxs-lookup"><span data-stu-id="f36b1-583">nie número</span></span>
  
<span data-ttu-id="f36b1-584">documento nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="f36b1-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="f36b1-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="f36b1-585">identidad único</span></span>
  
<span data-ttu-id="f36b1-586">Número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="f36b1-586">número nacional identidad</span></span>
  
<span data-ttu-id="f36b1-587">número DNI</span><span class="sxs-lookup"><span data-stu-id="f36b1-587">dni número</span></span>
  
<span data-ttu-id="f36b1-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="f36b1-588">dninúmero#</span></span>
  
<span data-ttu-id="f36b1-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="f36b1-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="f36b1-590">Suède</span><span class="sxs-lookup"><span data-stu-id="f36b1-590">Sweden</span></span>

<span data-ttu-id="f36b1-591">Pour plus d’informations, voir la section « ID National Suède » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="f36b1-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f36b1-592">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f36b1-592">See also</span></span>

[<span data-ttu-id="f36b1-593">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="f36b1-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

