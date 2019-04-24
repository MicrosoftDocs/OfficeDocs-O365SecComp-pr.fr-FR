---
title: Numéro d'identification nationale de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente l'aspect d'une stratégie de protection contre la perte de données (DLP) lorsqu'elle détecte le type d'informations sensibles du numéro d'identification national de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: afae2c3fa54fe5fcd93990cdf5797f5517c46202
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255642"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="701b8-104">Numéro d'identification nationale de l'UE</span><span class="sxs-lookup"><span data-stu-id="701b8-104">EU National Identification Number</span></span>

<span data-ttu-id="701b8-105">Cette rubrique présente l'aspect d'une stratégie de protection contre la perte de données (DLP) lorsqu'elle détecte le type d'informations sensibles du numéro d'identification national de l'UE.</span><span class="sxs-lookup"><span data-stu-id="701b8-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="701b8-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="701b8-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="701b8-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="701b8-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="701b8-108">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-108">Format</span></span>

<span data-ttu-id="701b8-109">Combinaison de 24 caractères de lettres, de chiffres et de caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="701b8-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-110">Pattern</span></span>

<span data-ttu-id="701b8-111">24 caractères:</span><span class="sxs-lookup"><span data-stu-id="701b8-111">24 characters:</span></span>
  
-  <span data-ttu-id="701b8-112">22 lettres (ne respectent pas la casse), chiffres, barres obliques inverses, barres obliques ou signes plus</span><span class="sxs-lookup"><span data-stu-id="701b8-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="701b8-113">Deux lettres (ne respectent pas la casse), des chiffres, des barres obliques inverses, des barres obliques, des signes plus ou des signes égal</span><span class="sxs-lookup"><span data-stu-id="701b8-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-114">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-114">Checksum</span></span>

<span data-ttu-id="701b8-115">Non applicable</span><span class="sxs-lookup"><span data-stu-id="701b8-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-116">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-116">Definition</span></span>

<span data-ttu-id="701b8-117">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-118">L'expression `Regex_austria_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-119">Un mot clé `Keywords_austria_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="701b8-120">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="701b8-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="701b8-122">Numéro d'identité autrichien</span><span class="sxs-lookup"><span data-stu-id="701b8-122">austrian identity number</span></span>
  
<span data-ttu-id="701b8-123">Numéro d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-123">national identity number</span></span>
  
<span data-ttu-id="701b8-124">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="701b8-124">identity number</span></span>
  
<span data-ttu-id="701b8-125">id national</span><span class="sxs-lookup"><span data-stu-id="701b8-125">national id</span></span>
  
<span data-ttu-id="701b8-126">Personalausweis Republik Österreich</span><span class="sxs-lookup"><span data-stu-id="701b8-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="701b8-127">Belgique</span><span class="sxs-lookup"><span data-stu-id="701b8-127">Belgium</span></span>

<span data-ttu-id="701b8-128">Pour plus d'informations, reportez-vous à la section «Belgique numéro national» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="701b8-129">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="701b8-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="701b8-130">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-130">Format</span></span>

<span data-ttu-id="701b8-131">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-132">Pattern</span></span>

<span data-ttu-id="701b8-133">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="701b8-134">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="701b8-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="701b8-135">Deux chiffres correspondant à l'ordre de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="701b8-136">Un chiffre correspondant au sexe: un chiffre pair pour le mâle et un chiffre impair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="701b8-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="701b8-137">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-138">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-138">Checksum</span></span>

<span data-ttu-id="701b8-139">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-140">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-140">Definition</span></span>

<span data-ttu-id="701b8-141">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-142">La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-143">Un mot clé `Keywords_bulgaria_national_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="701b8-144">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-145">La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="701b8-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="701b8-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="701b8-148">EGN</span><span class="sxs-lookup"><span data-stu-id="701b8-148">egn</span></span>
  
<span data-ttu-id="701b8-149">EGN #</span><span class="sxs-lookup"><span data-stu-id="701b8-149">egn#</span></span>
  
<span data-ttu-id="701b8-150">numéro national bulgare</span><span class="sxs-lookup"><span data-stu-id="701b8-150">bulgarian national number</span></span>
  
<span data-ttu-id="701b8-151">numéro national</span><span class="sxs-lookup"><span data-stu-id="701b8-151">national number</span></span>
  
<span data-ttu-id="701b8-152">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="701b8-152">social security number</span></span>
  
<span data-ttu-id="701b8-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-153">nationalnumber#</span></span>
  
<span data-ttu-id="701b8-154">SSN</span><span class="sxs-lookup"><span data-stu-id="701b8-154">ssn#</span></span>
  
<span data-ttu-id="701b8-155">SSN</span><span class="sxs-lookup"><span data-stu-id="701b8-155">ssn</span></span>
  
<span data-ttu-id="701b8-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="701b8-156">nationalnumber</span></span>
  
<span data-ttu-id="701b8-157">BNN #</span><span class="sxs-lookup"><span data-stu-id="701b8-157">bnn#</span></span>
  
<span data-ttu-id="701b8-158">BNN</span><span class="sxs-lookup"><span data-stu-id="701b8-158">bnn</span></span>
  
<span data-ttu-id="701b8-159">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-159">personal id number</span></span>
  
<span data-ttu-id="701b8-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-160">personalidnumber#</span></span>
  
<span data-ttu-id="701b8-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="701b8-161">единен граждански номер</span></span>
  
<span data-ttu-id="701b8-162">edinen grazhdanski Nomer</span><span class="sxs-lookup"><span data-stu-id="701b8-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="701b8-163">егн</span><span class="sxs-lookup"><span data-stu-id="701b8-163">егн</span></span>
  
<span data-ttu-id="701b8-164">егн #</span><span class="sxs-lookup"><span data-stu-id="701b8-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="701b8-165">Croatie</span><span class="sxs-lookup"><span data-stu-id="701b8-165">Croatia</span></span>

<span data-ttu-id="701b8-166">Pour plus d'informations, reportez-vous à la section «Croatie Identity Number» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="701b8-167">Chypre</span><span class="sxs-lookup"><span data-stu-id="701b8-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="701b8-168">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-168">Format</span></span>

<span data-ttu-id="701b8-169">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-170">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-170">Pattern</span></span>

 <span data-ttu-id="701b8-171">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="701b8-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="701b8-172">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-172">Checksum</span></span>

<span data-ttu-id="701b8-173">Non applicable</span><span class="sxs-lookup"><span data-stu-id="701b8-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-174">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-174">Definition</span></span>

<span data-ttu-id="701b8-175">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-176">L'expression `Regex_cyprus_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-177">Un mot clé `Keywords_cyprus_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="701b8-178">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="701b8-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="701b8-180">Numéro de carte d'identité</span><span class="sxs-lookup"><span data-stu-id="701b8-180">id card number</span></span>
  
<span data-ttu-id="701b8-181">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-181">national identification number</span></span>
  
<span data-ttu-id="701b8-182">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-182">personal id number</span></span>
  
<span data-ttu-id="701b8-183">Numéro de carte d'identité</span><span class="sxs-lookup"><span data-stu-id="701b8-183">identity card number</span></span>
  
<span data-ttu-id="701b8-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="701b8-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="701b8-185">République tchèque</span><span class="sxs-lookup"><span data-stu-id="701b8-185">Czech Republic</span></span>

<span data-ttu-id="701b8-186">Pour plus d'informations, consultez la section «numéro d'identité nationale tchèque» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="701b8-187">Danemark</span><span class="sxs-lookup"><span data-stu-id="701b8-187">Denmark</span></span>

<span data-ttu-id="701b8-188">Pour plus d'informations, reportez-vous à la section «numéro d'identification personnel Danemark» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="701b8-189">Estonie</span><span class="sxs-lookup"><span data-stu-id="701b8-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="701b8-190">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-190">Format</span></span>

<span data-ttu-id="701b8-191">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-192">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-192">Pattern</span></span>

<span data-ttu-id="701b8-193">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="701b8-193">11 digits:</span></span>
  
- <span data-ttu-id="701b8-194">Un chiffre correspondant au sexe et au siècle de naissance (nombre impair mâle, numéro pair femelle; 1-2:19 siècle; 3-4:20ème siècle; 5-6:21ème siècle)</span><span class="sxs-lookup"><span data-stu-id="701b8-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="701b8-195">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="701b8-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="701b8-196">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="701b8-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="701b8-197">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-198">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-198">Checksum</span></span>

<span data-ttu-id="701b8-199">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-200">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-200">Definition</span></span>

<span data-ttu-id="701b8-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-202">La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-203">Un mot clé `Keywords_estonia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-204">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-205">La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-206">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="701b8-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="701b8-208">code d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-208">personal identification code</span></span>
  
<span data-ttu-id="701b8-209">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-209">personal identification number</span></span>
  
<span data-ttu-id="701b8-210">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-210">national identification number</span></span>
  
<span data-ttu-id="701b8-211">numéro national</span><span class="sxs-lookup"><span data-stu-id="701b8-211">national number</span></span>
  
<span data-ttu-id="701b8-212">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-212">personal id number</span></span>
  
<span data-ttu-id="701b8-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-213">personalidnumber#</span></span>
  
<span data-ttu-id="701b8-214">inverse</span><span class="sxs-lookup"><span data-stu-id="701b8-214">ik</span></span>
  
<span data-ttu-id="701b8-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="701b8-215">isikukood</span></span>
  
<span data-ttu-id="701b8-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="701b8-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="701b8-217">Finlande</span><span class="sxs-lookup"><span data-stu-id="701b8-217">Finland</span></span>

<span data-ttu-id="701b8-218">Pour plus d'informations, reportez-vous à la section «ID national de Finlande» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="701b8-219">France</span><span class="sxs-lookup"><span data-stu-id="701b8-219">France</span></span>

<span data-ttu-id="701b8-220">Pour plus d'informations, reportez-vous à la section «carte d'identité nationale France (CNI)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="701b8-221">Allemagne</span><span class="sxs-lookup"><span data-stu-id="701b8-221">Germany</span></span>

<span data-ttu-id="701b8-222">Pour plus d'informations, reportez-vous à la section «Germany Identity Card Number» dans les [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="701b8-223">Grèce</span><span class="sxs-lookup"><span data-stu-id="701b8-223">Greece</span></span>

<span data-ttu-id="701b8-224">Pour plus d'informations, reportez-vous à la section «carte d'identité nationale Grèce» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="701b8-225">Hongrie</span><span class="sxs-lookup"><span data-stu-id="701b8-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="701b8-226">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-226">Format</span></span>

<span data-ttu-id="701b8-227">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="701b8-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-228">Pattern</span></span>

<span data-ttu-id="701b8-229">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="701b8-229">11 digits:</span></span>
  
-  <span data-ttu-id="701b8-230">Un chiffre correspondant au sexe (1-mâle, 2 femelles), d'autres numéros sont également possibles pour les citoyens nés avant 1900 ou les citoyens ayant une double citoyenneté.</span><span class="sxs-lookup"><span data-stu-id="701b8-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="701b8-231">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="701b8-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="701b8-232">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="701b8-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="701b8-233">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-234">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-234">Checksum</span></span>

<span data-ttu-id="701b8-235">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-236">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-236">Definition</span></span>

<span data-ttu-id="701b8-237">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-238">La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-239">Un mot clé `Keywords_hungary_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-240">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-241">La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-242">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="701b8-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="701b8-244">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-244">personal identification number</span></span>
  
<span data-ttu-id="701b8-245">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="701b8-245">identification number</span></span>
  
<span data-ttu-id="701b8-246">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-246">personal id number</span></span>
  
<span data-ttu-id="701b8-247">személyazonosító Igazolvány</span><span class="sxs-lookup"><span data-stu-id="701b8-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="701b8-248">Irlande</span><span class="sxs-lookup"><span data-stu-id="701b8-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="701b8-249">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-249">Format</span></span>

<span data-ttu-id="701b8-250">Combinaison de neuf caractères de lettres, de chiffres et d'un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="701b8-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-251">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-251">Pattern</span></span>

<span data-ttu-id="701b8-252">Combinaison de neuf caractères de lettres, de chiffres et d'un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="701b8-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="701b8-253">Du 01 janvier 2013 au maintenant:</span><span class="sxs-lookup"><span data-stu-id="701b8-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="701b8-254">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="701b8-254">Seven digits</span></span> 
    
- <span data-ttu-id="701b8-255">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-255">One check digit</span></span>
    
- <span data-ttu-id="701b8-256">Un espace ou la lettre majuscule «W» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="701b8-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="701b8-257">Avant le 1er janvier 2013:</span><span class="sxs-lookup"><span data-stu-id="701b8-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="701b8-258">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="701b8-258">Seven digits</span></span> 
    
- <span data-ttu-id="701b8-259">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-259">One check digit</span></span>
    
- <span data-ttu-id="701b8-260">Un espace ou une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="701b8-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-261">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-261">Checksum</span></span>

<span data-ttu-id="701b8-262">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-263">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-263">Definition</span></span>

<span data-ttu-id="701b8-264">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-265">La fonction trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="701b8-266">Un mot clé from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-266">A keyword from is found.</span></span>
    
<span data-ttu-id="701b8-267">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-268">La fonction trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-269">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="701b8-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="701b8-271">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="701b8-271">personal public service number</span></span>
  
<span data-ttu-id="701b8-272">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="701b8-272">pps no</span></span>
  
<span data-ttu-id="701b8-273">Numéro de produit et d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="701b8-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="701b8-274">RSI non</span><span class="sxs-lookup"><span data-stu-id="701b8-274">rsi no</span></span>
  
<span data-ttu-id="701b8-275">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-275">personal identification number</span></span>
  
<span data-ttu-id="701b8-276">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="701b8-276">identification number</span></span>
  
<span data-ttu-id="701b8-277">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-277">personal id number</span></span>
  
<span data-ttu-id="701b8-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="701b8-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="701b8-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="701b8-279">uimh.</span></span> <span data-ttu-id="701b8-280">toxine</span><span class="sxs-lookup"><span data-stu-id="701b8-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="701b8-281">Italie</span><span class="sxs-lookup"><span data-stu-id="701b8-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="701b8-282">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-282">Format</span></span>

<span data-ttu-id="701b8-283">Combinaison de 16 caractères de lettres et de chiffres dans le modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="701b8-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-284">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-284">Pattern</span></span>

<span data-ttu-id="701b8-285">Combinaison de lettres et de chiffres de 16 caractères:</span><span class="sxs-lookup"><span data-stu-id="701b8-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="701b8-286">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="701b8-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="701b8-287">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="701b8-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="701b8-288">Deux chiffres correspondant aux derniers chiffres de l'année de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="701b8-289">Une lettre correspondant à la lettre du mois de naissance: les lettres sont utilisées dans l'ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (par conséquent, le mois de janvier est A et le mois d'octobre est R).</span><span class="sxs-lookup"><span data-stu-id="701b8-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="701b8-290">Deux chiffres correspondant au jour du mois de naissance — afin de différencier les hommes, 40 est ajouté au jour de naissance pour les femmes</span><span class="sxs-lookup"><span data-stu-id="701b8-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="701b8-291">Quatre chiffres correspondant à l'indicatif régional propre à la municipalité où la personne est né (des codes pays sont utilisés pour les pays étrangers)</span><span class="sxs-lookup"><span data-stu-id="701b8-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="701b8-292">Un chiffre de parité</span><span class="sxs-lookup"><span data-stu-id="701b8-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-293">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-293">Checksum</span></span>

<span data-ttu-id="701b8-294">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-295">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-295">Definition</span></span>

<span data-ttu-id="701b8-296">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-297">La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-298">Un mot clé `Keywords_italy_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-299">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-300">La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-301">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="701b8-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="701b8-303">code personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-303">personal code</span></span>
  
<span data-ttu-id="701b8-304">Numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-304">personal code number</span></span>
  
<span data-ttu-id="701b8-305">Numéro de certificat personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-305">personal certificate number</span></span>
  
<span data-ttu-id="701b8-306">code fiscal</span><span class="sxs-lookup"><span data-stu-id="701b8-306">fiscal code</span></span>
  
<span data-ttu-id="701b8-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="701b8-307">personalcodeno#</span></span>
  
<span data-ttu-id="701b8-308">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-308">personal id number</span></span>
  
<span data-ttu-id="701b8-309">code d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-309">personal id code</span></span>
  
<span data-ttu-id="701b8-310">codice Personal</span><span class="sxs-lookup"><span data-stu-id="701b8-310">codice personale</span></span>
  
<span data-ttu-id="701b8-311">numération Certificate-personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-311">numero certificato personale</span></span>
  
<span data-ttu-id="701b8-312">numération personnelle</span><span class="sxs-lookup"><span data-stu-id="701b8-312">numero personale</span></span>
  
<span data-ttu-id="701b8-313">ID de numérotation personnelle</span><span class="sxs-lookup"><span data-stu-id="701b8-313">numero id personale</span></span>
  
<span data-ttu-id="701b8-314">codice ID personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-314">codice id personale</span></span>
  
<span data-ttu-id="701b8-315">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="701b8-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="701b8-316">Italie</span><span class="sxs-lookup"><span data-stu-id="701b8-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="701b8-317">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-317">Format</span></span>

<span data-ttu-id="701b8-318">11 chiffres et un trait d'Union dans le format spécifié</span><span class="sxs-lookup"><span data-stu-id="701b8-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-319">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-319">Pattern</span></span>

<span data-ttu-id="701b8-320">11 chiffres et un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="701b8-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="701b8-321">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="701b8-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="701b8-322">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="701b8-322">A hyphen</span></span>
    
- <span data-ttu-id="701b8-323">Un chiffre correspondant au siècle de naissance («0» pour le 19 siècle, «1» pour le vingtième siècle et «2» pour le 21ème siècle).</span><span class="sxs-lookup"><span data-stu-id="701b8-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="701b8-324">Quatre chiffres, généré de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="701b8-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-325">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-325">Checksum</span></span>

<span data-ttu-id="701b8-326">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-327">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-327">Definition</span></span>

<span data-ttu-id="701b8-328">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-329">La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-330">Un mot clé `Keywords_latvia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-331">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-332">La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-333">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="701b8-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="701b8-335">code personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-335">personal code</span></span>
  
<span data-ttu-id="701b8-336">Numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-336">personal code number</span></span>
  
<span data-ttu-id="701b8-337">Numéro de certificat personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-337">personal certificate number</span></span>
  
<span data-ttu-id="701b8-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="701b8-338">personalcodeno#</span></span>
  
<span data-ttu-id="701b8-339">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-339">personal id number</span></span>
  
<span data-ttu-id="701b8-340">code d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-340">personal id code</span></span>
  
<span data-ttu-id="701b8-341">Personas kods</span><span class="sxs-lookup"><span data-stu-id="701b8-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="701b8-342">Lituanie</span><span class="sxs-lookup"><span data-stu-id="701b8-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="701b8-343">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-343">Format</span></span>

<span data-ttu-id="701b8-344">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-345">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-345">Pattern</span></span>

<span data-ttu-id="701b8-346">11 chiffres sans espaces ni délimiteurs:</span><span class="sxs-lookup"><span data-stu-id="701b8-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="701b8-347">Un chiffre correspondant au sexe et au siècle de la personne</span><span class="sxs-lookup"><span data-stu-id="701b8-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="701b8-348">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="701b8-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="701b8-349">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="701b8-350">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-351">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-351">Checksum</span></span>

<span data-ttu-id="701b8-352">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-353">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-353">Definition</span></span>

<span data-ttu-id="701b8-354">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-355">La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-356">Un mot clé `Keywords_lithuania_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-357">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-358">La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-359">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="701b8-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="701b8-361">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-361">personal numeric code</span></span>
  
<span data-ttu-id="701b8-362">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-362">unique identification number</span></span>
  
<span data-ttu-id="701b8-363">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="701b8-363">citizen service number</span></span>
  
<span data-ttu-id="701b8-364">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-364">unique identity number</span></span>
  
<span data-ttu-id="701b8-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="701b8-366">code personnel.</span><span class="sxs-lookup"><span data-stu-id="701b8-366">personal code.</span></span>
  
<span data-ttu-id="701b8-367">Asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="701b8-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="701b8-368">unikalus identifikavimo</span><span class="sxs-lookup"><span data-stu-id="701b8-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="701b8-369">piliečio paslaugos</span><span class="sxs-lookup"><span data-stu-id="701b8-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="701b8-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="701b8-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="701b8-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="701b8-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="701b8-372">Relatif</span><span class="sxs-lookup"><span data-stu-id="701b8-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="701b8-373">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-373">Format</span></span>

<span data-ttu-id="701b8-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-375">Pattern</span></span>

<span data-ttu-id="701b8-376">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="701b8-376">11 digits</span></span>
  
- <span data-ttu-id="701b8-377">Un chiffre correspondant au sexe et au siècle de la personne</span><span class="sxs-lookup"><span data-stu-id="701b8-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="701b8-378">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="701b8-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="701b8-379">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="701b8-380">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-381">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-381">Checksum</span></span>

<span data-ttu-id="701b8-382">Non applicable</span><span class="sxs-lookup"><span data-stu-id="701b8-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-383">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-383">Definition</span></span>

<span data-ttu-id="701b8-384">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-385">L'expression `Regex_luxemburg_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-386">Un mot clé `Keywords_luxemburg_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="701b8-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="701b8-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="701b8-389">ID personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-389">personal id</span></span>
  
<span data-ttu-id="701b8-390">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-390">personal id number</span></span>
  
<span data-ttu-id="701b8-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="701b8-391">personalidno#</span></span>
  
<span data-ttu-id="701b8-392">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-392">unique id number</span></span>
  
<span data-ttu-id="701b8-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-393">personalidnumber#</span></span>
  
<span data-ttu-id="701b8-394">clé d'ID unique</span><span class="sxs-lookup"><span data-stu-id="701b8-394">unique id key</span></span>
  
<span data-ttu-id="701b8-395">code d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-395">personal id code</span></span>
  
<span data-ttu-id="701b8-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="701b8-396">uniqueidkey#</span></span>
  
<span data-ttu-id="701b8-397">code individuel</span><span class="sxs-lookup"><span data-stu-id="701b8-397">individual code</span></span>
  
<span data-ttu-id="701b8-398">ID individuel</span><span class="sxs-lookup"><span data-stu-id="701b8-398">individual id</span></span>
  
<span data-ttu-id="701b8-399">ID eindeutige-Nummer</span><span class="sxs-lookup"><span data-stu-id="701b8-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="701b8-400">ID eindeutige</span><span class="sxs-lookup"><span data-stu-id="701b8-400">eindeutige id</span></span>
  
<span data-ttu-id="701b8-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="701b8-401">id personnelle</span></span>
  
<span data-ttu-id="701b8-402">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="701b8-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="701b8-403">idpersonnelle#</span></span>
  
<span data-ttu-id="701b8-404">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="701b8-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="701b8-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="701b8-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="701b8-406">Malte</span><span class="sxs-lookup"><span data-stu-id="701b8-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="701b8-407">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-407">Format</span></span>

<span data-ttu-id="701b8-408">Sept chiffres suivis d'une lettre</span><span class="sxs-lookup"><span data-stu-id="701b8-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-409">Pattern</span></span>

<span data-ttu-id="701b8-410">Sept chiffres suivis d'une lettre:</span><span class="sxs-lookup"><span data-stu-id="701b8-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="701b8-411">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="701b8-411">Seven digits</span></span> 
    
- <span data-ttu-id="701b8-412">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="701b8-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-413">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-413">Checksum</span></span>

<span data-ttu-id="701b8-414">Non applicable</span><span class="sxs-lookup"><span data-stu-id="701b8-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-415">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-415">Definition</span></span>

<span data-ttu-id="701b8-416">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-417">L'expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-418">Un mot clé `Keywords_malta_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-419">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-420">L'expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-421">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="701b8-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="701b8-423">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-423">personal numeric code</span></span>
  
<span data-ttu-id="701b8-424">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-424">unique identification number</span></span>
  
<span data-ttu-id="701b8-425">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="701b8-425">citizen service number</span></span>
  
<span data-ttu-id="701b8-426">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-426">unique identity number</span></span>
  
<span data-ttu-id="701b8-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="701b8-428">Kodiċi numerali</span><span class="sxs-lookup"><span data-stu-id="701b8-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="701b8-429">numru ta'IDENTIFIKAZZJONI uniku</span><span class="sxs-lookup"><span data-stu-id="701b8-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="701b8-430">numru-Servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="701b8-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="701b8-431">numru ta'identità uniku</span><span class="sxs-lookup"><span data-stu-id="701b8-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="701b8-432">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="701b8-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="701b8-433">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-433">Format</span></span>

<span data-ttu-id="701b8-434">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-435">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-435">Pattern</span></span>

<span data-ttu-id="701b8-436">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="701b8-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="701b8-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-437">Checksum</span></span>

<span data-ttu-id="701b8-438">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-439">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-439">Definition</span></span>

<span data-ttu-id="701b8-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-441">La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-442">Un mot clé from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-442">A keyword from is found.</span></span>
    
<span data-ttu-id="701b8-443">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-444">La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-445">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="701b8-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="701b8-447">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-447">personal numeric code</span></span>
  
<span data-ttu-id="701b8-448">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-448">unique identification number</span></span>
  
<span data-ttu-id="701b8-449">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="701b8-449">citizen service number</span></span>
  
<span data-ttu-id="701b8-450">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-450">unique identity number</span></span>
  
<span data-ttu-id="701b8-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="701b8-452">BSN</span><span class="sxs-lookup"><span data-stu-id="701b8-452">bsn</span></span>
  
<span data-ttu-id="701b8-453">BSN</span><span class="sxs-lookup"><span data-stu-id="701b8-453">bsn#</span></span>
  
<span data-ttu-id="701b8-454">persoonlijke Numerieke de code</span><span class="sxs-lookup"><span data-stu-id="701b8-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="701b8-455">Uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="701b8-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="701b8-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="701b8-456">burgerservicenummer</span></span>
  
<span data-ttu-id="701b8-457">Uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="701b8-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="701b8-458">Pologne</span><span class="sxs-lookup"><span data-stu-id="701b8-458">Poland</span></span>

<span data-ttu-id="701b8-459">Pour plus d'informations, reportez-vous à la section «Pologne national ID (PESEL)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="701b8-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="701b8-460">Portugal</span></span>

<span data-ttu-id="701b8-461">Pour plus d'informations, reportez-vous à la section «numéro de carte de citoyen Portugal» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="701b8-462">Roumanie</span><span class="sxs-lookup"><span data-stu-id="701b8-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="701b8-463">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-463">Format</span></span>

<span data-ttu-id="701b8-464">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-465">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-465">Pattern</span></span>

<span data-ttu-id="701b8-466">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="701b8-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="701b8-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-467">Checksum</span></span>

<span data-ttu-id="701b8-468">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-469">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-469">Definition</span></span>

<span data-ttu-id="701b8-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-471">La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-472">Un mot clé `Keywords_romania_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-474">La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-475">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="701b8-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="701b8-477">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-477">personal numeric code</span></span>
  
<span data-ttu-id="701b8-478">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-478">unique identification number</span></span>
  
<span data-ttu-id="701b8-479">CNP</span><span class="sxs-lookup"><span data-stu-id="701b8-479">cnp</span></span>
  
<span data-ttu-id="701b8-480">CNP #</span><span class="sxs-lookup"><span data-stu-id="701b8-480">cnp#</span></span>
  
<span data-ttu-id="701b8-481">ancre</span><span class="sxs-lookup"><span data-stu-id="701b8-481">pin</span></span>
  
<span data-ttu-id="701b8-482">ancre</span><span class="sxs-lookup"><span data-stu-id="701b8-482">pin#</span></span>
  
<span data-ttu-id="701b8-483">Numéro d'assurance</span><span class="sxs-lookup"><span data-stu-id="701b8-483">insurance number</span></span>
  
<span data-ttu-id="701b8-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-484">insurancenumber#</span></span>
  
<span data-ttu-id="701b8-485">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-485">unique identity number</span></span>
  
<span data-ttu-id="701b8-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="701b8-487">COD numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-487">cod numeric personal</span></span>
  
<span data-ttu-id="701b8-488">COD IDENTIFICARE personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-488">cod identificare personal</span></span>
  
<span data-ttu-id="701b8-489">COD UNIC IDENTIFICARE</span><span class="sxs-lookup"><span data-stu-id="701b8-489">cod unic identificare</span></span>
  
<span data-ttu-id="701b8-490">UNIC personnel număr</span><span class="sxs-lookup"><span data-stu-id="701b8-490">număr personal unic</span></span>
  
<span data-ttu-id="701b8-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="701b8-491">număr identitate</span></span>
  
<span data-ttu-id="701b8-492">număr IDENTIFICARE personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-492">număr identificare personal</span></span>
  
<span data-ttu-id="701b8-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="701b8-493">număridentitate#</span></span>
  
<span data-ttu-id="701b8-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="701b8-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="701b8-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="701b8-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="701b8-496">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="701b8-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="701b8-497">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-497">Format</span></span>

<span data-ttu-id="701b8-498">Dix chiffres contenant une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="701b8-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-499">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-499">Pattern</span></span>

<span data-ttu-id="701b8-500">Dix chiffres contenant une barre oblique inverse:</span><span class="sxs-lookup"><span data-stu-id="701b8-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="701b8-501">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-501">Checksum</span></span>

<span data-ttu-id="701b8-502">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-503">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-503">Definition</span></span>

<span data-ttu-id="701b8-504">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-505">La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-506">Un mot clé `Keywords_slovakia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-508">La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-509">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="701b8-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="701b8-511">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-511">birth number</span></span>
  
<span data-ttu-id="701b8-512">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-512">national identification number</span></span>
  
<span data-ttu-id="701b8-513">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-513">personal identification number</span></span>
  
<span data-ttu-id="701b8-514">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="701b8-514">social security number</span></span>
  
<span data-ttu-id="701b8-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-515">nationalnumber#</span></span>
  
<span data-ttu-id="701b8-516">SSN</span><span class="sxs-lookup"><span data-stu-id="701b8-516">ssn#</span></span>
  
<span data-ttu-id="701b8-517">SSN</span><span class="sxs-lookup"><span data-stu-id="701b8-517">ssn</span></span>
  
<span data-ttu-id="701b8-518">numéro national</span><span class="sxs-lookup"><span data-stu-id="701b8-518">national number</span></span>
  
<span data-ttu-id="701b8-519">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-519">personal id number</span></span>
  
<span data-ttu-id="701b8-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="701b8-520">personalidnumber#</span></span>
  
<span data-ttu-id="701b8-521">rč</span><span class="sxs-lookup"><span data-stu-id="701b8-521">rč</span></span>
  
<span data-ttu-id="701b8-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="701b8-522">rodné číslo</span></span>
  
<span data-ttu-id="701b8-523">Rodne Cislo</span><span class="sxs-lookup"><span data-stu-id="701b8-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="701b8-524">Slovénie</span><span class="sxs-lookup"><span data-stu-id="701b8-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="701b8-525">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-525">Format</span></span>

<span data-ttu-id="701b8-526">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="701b8-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-527">Pattern</span></span>

<span data-ttu-id="701b8-528">13 chiffres dans le modèle spécifié:</span><span class="sxs-lookup"><span data-stu-id="701b8-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="701b8-529">Sept chiffres correspondant à la date de naissance (DDMMLLL) où «LLL» correspond aux trois derniers chiffres de l'année de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="701b8-530">Deux chiffres correspondant à la zone de naissance</span><span class="sxs-lookup"><span data-stu-id="701b8-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="701b8-531">Trois chiffres correspondant à une combinaison de sexe et de numéro de série pour les personnes nées le même jour (000-499 pour les mâles et les 500-999 pour les femelles)</span><span class="sxs-lookup"><span data-stu-id="701b8-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="701b8-532">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-533">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-533">Checksum</span></span>

<span data-ttu-id="701b8-534">Oui</span><span class="sxs-lookup"><span data-stu-id="701b8-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-535">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-535">Definition</span></span>

<span data-ttu-id="701b8-536">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-537">La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-538">Un mot clé `Keywords_slovenia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="701b8-539">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-540">La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="701b8-541">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="701b8-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="701b8-543">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-543">personal numeric code</span></span>
  
<span data-ttu-id="701b8-544">Numéro d'identification unique</span><span class="sxs-lookup"><span data-stu-id="701b8-544">unique identification number</span></span>
  
<span data-ttu-id="701b8-545">Numéro d'enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="701b8-545">unique registration number</span></span>
  
<span data-ttu-id="701b8-546">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-546">unique identity number</span></span>
  
<span data-ttu-id="701b8-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="701b8-548">Numéro de citoyen principal unique</span><span class="sxs-lookup"><span data-stu-id="701b8-548">unique master citizen number</span></span>
  
<span data-ttu-id="701b8-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="701b8-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="701b8-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="701b8-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="701b8-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="701b8-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="701b8-552">emšo</span><span class="sxs-lookup"><span data-stu-id="701b8-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="701b8-553">Espagne</span><span class="sxs-lookup"><span data-stu-id="701b8-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="701b8-554">Format</span><span class="sxs-lookup"><span data-stu-id="701b8-554">Format</span></span>

<span data-ttu-id="701b8-555">Sept chiffres suivis d'un caractère</span><span class="sxs-lookup"><span data-stu-id="701b8-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="701b8-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="701b8-556">Pattern</span></span>

<span data-ttu-id="701b8-557">Sept chiffres suivis d'un caractère</span><span class="sxs-lookup"><span data-stu-id="701b8-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="701b8-558">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="701b8-558">Seven digits</span></span>
    
- <span data-ttu-id="701b8-559">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="701b8-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="701b8-560">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="701b8-560">Checksum</span></span>

<span data-ttu-id="701b8-561">Non applicable</span><span class="sxs-lookup"><span data-stu-id="701b8-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="701b8-562">Définition</span><span class="sxs-lookup"><span data-stu-id="701b8-562">Definition</span></span>

<span data-ttu-id="701b8-563">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="701b8-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="701b8-564">L'expression `Regex_spain_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="701b8-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="701b8-565">Un mot clé `Keywords_spain_eu_national_id_card"` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="701b8-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="701b8-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="701b8-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="701b8-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="701b8-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="701b8-568">DNI</span><span class="sxs-lookup"><span data-stu-id="701b8-568">dni</span></span>
  
<span data-ttu-id="701b8-569">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-569">national identification number</span></span>
  
<span data-ttu-id="701b8-570">Numéro d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-570">national identity number</span></span>
  
<span data-ttu-id="701b8-571">Numéro d'assurance</span><span class="sxs-lookup"><span data-stu-id="701b8-571">insurance number</span></span>
  
<span data-ttu-id="701b8-572">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="701b8-572">personal identification number</span></span>
  
<span data-ttu-id="701b8-573">identité nationale</span><span class="sxs-lookup"><span data-stu-id="701b8-573">national identity</span></span>
  
<span data-ttu-id="701b8-574">n ° d'identité personnelle</span><span class="sxs-lookup"><span data-stu-id="701b8-574">personal identity no</span></span>
  
<span data-ttu-id="701b8-575">Numéro d'identité unique</span><span class="sxs-lookup"><span data-stu-id="701b8-575">unique identity number</span></span>
  
<span data-ttu-id="701b8-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="701b8-576">nationalidno#</span></span>
  
<span data-ttu-id="701b8-577">quei</span><span class="sxs-lookup"><span data-stu-id="701b8-577">uniqueid#</span></span>
  
<span data-ttu-id="701b8-578">DNI</span><span class="sxs-lookup"><span data-stu-id="701b8-578">dni#</span></span>
  
<span data-ttu-id="701b8-579">nationalID #</span><span class="sxs-lookup"><span data-stu-id="701b8-579">nationalid#</span></span>
  
<span data-ttu-id="701b8-580">nie</span><span class="sxs-lookup"><span data-stu-id="701b8-580">nie#</span></span>
  
<span data-ttu-id="701b8-581">nie</span><span class="sxs-lookup"><span data-stu-id="701b8-581">nie</span></span>
  
<span data-ttu-id="701b8-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="701b8-582">nienúmero#</span></span>
  
<span data-ttu-id="701b8-583">nie número</span><span class="sxs-lookup"><span data-stu-id="701b8-583">nie número</span></span>
  
<span data-ttu-id="701b8-584">Documento Nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="701b8-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="701b8-585">identidad Único</span><span class="sxs-lookup"><span data-stu-id="701b8-585">identidad único</span></span>
  
<span data-ttu-id="701b8-586">número Nacional identidad</span><span class="sxs-lookup"><span data-stu-id="701b8-586">número nacional identidad</span></span>
  
<span data-ttu-id="701b8-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="701b8-587">dni número</span></span>
  
<span data-ttu-id="701b8-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="701b8-588">dninúmero#</span></span>
  
<span data-ttu-id="701b8-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="701b8-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="701b8-590">Suède</span><span class="sxs-lookup"><span data-stu-id="701b8-590">Sweden</span></span>

<span data-ttu-id="701b8-591">Pour plus d'informations, reportez-vous à la section «ID national Suède» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="701b8-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="701b8-592">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="701b8-592">See also</span></span>

[<span data-ttu-id="701b8-593">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="701b8-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

