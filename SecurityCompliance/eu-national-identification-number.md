---
title: Numéro d’identification nationale de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente l’aspect d’une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles du numéro d’identification national de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: b784b7509eed899f9f03db96ee5e827b9bf70d2e
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852746"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="d483b-104">Numéro d’identification nationale de l’UE</span><span class="sxs-lookup"><span data-stu-id="d483b-104">EU National Identification Number</span></span>

<span data-ttu-id="d483b-105">Cette rubrique présente l’aspect d’une stratégie de protection contre la perte de données (DLP) lorsqu’elle détecte le type d’informations sensibles du numéro d’identification national de l’UE.</span><span class="sxs-lookup"><span data-stu-id="d483b-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="d483b-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="d483b-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d483b-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d483b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d483b-108">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-108">Format</span></span>

<span data-ttu-id="d483b-109">Combinaison de 24 caractères de lettres, de chiffres et de caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="d483b-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-110">Pattern</span></span>

<span data-ttu-id="d483b-111">24 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-111">24 characters:</span></span>
  
-  <span data-ttu-id="d483b-112">22 lettres (ne respectent pas la casse), chiffres, barres obliques inverses, barres obliques ou signes plus</span><span class="sxs-lookup"><span data-stu-id="d483b-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="d483b-113">Deux lettres (ne respectent pas la casse), des chiffres, des barres obliques inverses, des barres obliques, des signes plus ou des signes égal</span><span class="sxs-lookup"><span data-stu-id="d483b-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-114">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-114">Checksum</span></span>

<span data-ttu-id="d483b-115">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d483b-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-116">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-116">Definition</span></span>

<span data-ttu-id="d483b-117">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-118">L’expression `Regex_austria_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-119">Un mot clé `Keywords_austria_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d483b-120">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-120">Keywords</span></span>

#### <a name="keywords_austria_eu_national_id_card"></a><span data-ttu-id="d483b-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="d483b-122">Numéro d’identité autrichien</span><span class="sxs-lookup"><span data-stu-id="d483b-122">austrian identity number</span></span>
  
<span data-ttu-id="d483b-123">Numéro d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-123">national identity number</span></span>
  
<span data-ttu-id="d483b-124">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="d483b-124">identity number</span></span>
  
<span data-ttu-id="d483b-125">id national</span><span class="sxs-lookup"><span data-stu-id="d483b-125">national id</span></span>
  
<span data-ttu-id="d483b-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="d483b-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="d483b-127">Belgique</span><span class="sxs-lookup"><span data-stu-id="d483b-127">Belgium</span></span>

<span data-ttu-id="d483b-128">Pour plus d’informations, reportez-vous à la section « Belgique numéro national » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="d483b-129">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d483b-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="d483b-130">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-130">Format</span></span>

<span data-ttu-id="d483b-131">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-132">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-132">Pattern</span></span>

<span data-ttu-id="d483b-133">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="d483b-134">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d483b-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="d483b-135">Deux chiffres correspondant à l’ordre de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="d483b-136">Un chiffre correspondant au sexe : un chiffre pair pour le mâle et un chiffre impair pour femelle.</span><span class="sxs-lookup"><span data-stu-id="d483b-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="d483b-137">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-138">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-138">Checksum</span></span>

<span data-ttu-id="d483b-139">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-140">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-140">Definition</span></span>

<span data-ttu-id="d483b-141">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-142">La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-143">Un mot clé `Keywords_bulgaria_national_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="d483b-144">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-145">La fonction `Func_bulgaria_national_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-146">Keywords</span></span>

#### <a name="keywords_bulgaria_national_number"></a><span data-ttu-id="d483b-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="d483b-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="d483b-148">egn</span><span class="sxs-lookup"><span data-stu-id="d483b-148">egn</span></span>
  
<span data-ttu-id="d483b-149">egn #</span><span class="sxs-lookup"><span data-stu-id="d483b-149">egn#</span></span>
  
<span data-ttu-id="d483b-150">numéro national bulgare</span><span class="sxs-lookup"><span data-stu-id="d483b-150">bulgarian national number</span></span>
  
<span data-ttu-id="d483b-151">numéro national</span><span class="sxs-lookup"><span data-stu-id="d483b-151">national number</span></span>
  
<span data-ttu-id="d483b-152">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d483b-152">social security number</span></span>
  
<span data-ttu-id="d483b-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-153">nationalnumber#</span></span>
  
<span data-ttu-id="d483b-154">SSN #</span><span class="sxs-lookup"><span data-stu-id="d483b-154">ssn#</span></span>
  
<span data-ttu-id="d483b-155">SSN</span><span class="sxs-lookup"><span data-stu-id="d483b-155">ssn</span></span>
  
<span data-ttu-id="d483b-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="d483b-156">nationalnumber</span></span>
  
<span data-ttu-id="d483b-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="d483b-157">bnn#</span></span>
  
<span data-ttu-id="d483b-158">bnn</span><span class="sxs-lookup"><span data-stu-id="d483b-158">bnn</span></span>
  
<span data-ttu-id="d483b-159">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-159">personal id number</span></span>
  
<span data-ttu-id="d483b-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-160">personalidnumber#</span></span>
  
<span data-ttu-id="d483b-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="d483b-161">единен граждански номер</span></span>
  
<span data-ttu-id="d483b-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="d483b-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="d483b-163">егн</span><span class="sxs-lookup"><span data-stu-id="d483b-163">егн</span></span>
  
<span data-ttu-id="d483b-164">егн #</span><span class="sxs-lookup"><span data-stu-id="d483b-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="d483b-165">Croatie</span><span class="sxs-lookup"><span data-stu-id="d483b-165">Croatia</span></span>

<span data-ttu-id="d483b-166">Pour plus d’informations, reportez-vous à la section « Croatie Identity Number » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="d483b-167">Chypre</span><span class="sxs-lookup"><span data-stu-id="d483b-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="d483b-168">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-168">Format</span></span>

<span data-ttu-id="d483b-169">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-170">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-170">Pattern</span></span>

 <span data-ttu-id="d483b-171">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d483b-172">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-172">Checksum</span></span>

<span data-ttu-id="d483b-173">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d483b-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-174">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-174">Definition</span></span>

<span data-ttu-id="d483b-175">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-176">L’expression `Regex_cyprus_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-177">Un mot clé `Keywords_cyprus_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d483b-178">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-178">Keywords</span></span>

#### <a name="keywords_cyprus_eu_national_id_card"></a><span data-ttu-id="d483b-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="d483b-180">Numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d483b-180">id card number</span></span>
  
<span data-ttu-id="d483b-181">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-181">national identification number</span></span>
  
<span data-ttu-id="d483b-182">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-182">personal id number</span></span>
  
<span data-ttu-id="d483b-183">Numéro de carte d’identité</span><span class="sxs-lookup"><span data-stu-id="d483b-183">identity card number</span></span>
  
<span data-ttu-id="d483b-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="d483b-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="d483b-185">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d483b-185">Czech Republic</span></span>

<span data-ttu-id="d483b-186">Pour plus d’informations, consultez la section « numéro d’identité nationale tchèque » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="d483b-187">Danemark</span><span class="sxs-lookup"><span data-stu-id="d483b-187">Denmark</span></span>

<span data-ttu-id="d483b-188">Pour plus d’informations, reportez-vous à la section « numéro d’identification personnel Danemark » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="d483b-189">Estonie</span><span class="sxs-lookup"><span data-stu-id="d483b-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="d483b-190">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-190">Format</span></span>

<span data-ttu-id="d483b-191">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-192">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-192">Pattern</span></span>

<span data-ttu-id="d483b-193">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d483b-193">11 digits:</span></span>
  
- <span data-ttu-id="d483b-194">Un chiffre correspondant au sexe et au siècle de naissance (nombre impair mâle, numéro pair femelle ; 1-2:19 siècle ; 3-4:20ème siècle ; 5-6:21ème siècle)</span><span class="sxs-lookup"><span data-stu-id="d483b-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="d483b-195">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d483b-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="d483b-196">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="d483b-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="d483b-197">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-198">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-198">Checksum</span></span>

<span data-ttu-id="d483b-199">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-200">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-200">Definition</span></span>

<span data-ttu-id="d483b-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-202">La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-203">Un mot clé `Keywords_estonia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-204">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-205">La fonction `Func_estonia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-206">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-206">Keywords</span></span>

#### <a name="keywords_estonia_eu_national_id_card"></a><span data-ttu-id="d483b-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="d483b-208">code d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-208">personal identification code</span></span>
  
<span data-ttu-id="d483b-209">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-209">personal identification number</span></span>
  
<span data-ttu-id="d483b-210">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-210">national identification number</span></span>
  
<span data-ttu-id="d483b-211">numéro national</span><span class="sxs-lookup"><span data-stu-id="d483b-211">national number</span></span>
  
<span data-ttu-id="d483b-212">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-212">personal id number</span></span>
  
<span data-ttu-id="d483b-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-213">personalidnumber#</span></span>
  
<span data-ttu-id="d483b-214">inverse</span><span class="sxs-lookup"><span data-stu-id="d483b-214">ik</span></span>
  
<span data-ttu-id="d483b-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="d483b-215">isikukood</span></span>
  
<span data-ttu-id="d483b-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="d483b-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="d483b-217">Finlande</span><span class="sxs-lookup"><span data-stu-id="d483b-217">Finland</span></span>

<span data-ttu-id="d483b-218">Pour plus d’informations, reportez-vous à la section « ID national de Finlande » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="d483b-219">France</span><span class="sxs-lookup"><span data-stu-id="d483b-219">France</span></span>

<span data-ttu-id="d483b-220">Pour plus d’informations, reportez-vous à la section « carte d’identité nationale France (CNI) » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="d483b-221">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d483b-221">Germany</span></span>

<span data-ttu-id="d483b-222">Pour plus d’informations, reportez-vous à la section « Germany Identity Card Number » dans les [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="d483b-223">Grèce</span><span class="sxs-lookup"><span data-stu-id="d483b-223">Greece</span></span>

<span data-ttu-id="d483b-224">Pour plus d’informations, reportez-vous à la section « carte d’identité nationale Grèce » dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="d483b-225">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d483b-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d483b-226">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-226">Format</span></span>

<span data-ttu-id="d483b-227">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-228">Pattern</span></span>

<span data-ttu-id="d483b-229">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d483b-229">11 digits:</span></span>
  
-  <span data-ttu-id="d483b-230">Un chiffre correspondant au sexe (1-mâle, 2 femelles), d’autres numéros sont également possibles pour les citoyens nés avant 1900 ou les citoyens ayant une double citoyenneté.</span><span class="sxs-lookup"><span data-stu-id="d483b-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="d483b-231">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d483b-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="d483b-232">Trois chiffres correspondant à un numéro de série</span><span class="sxs-lookup"><span data-stu-id="d483b-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="d483b-233">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-234">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-234">Checksum</span></span>

<span data-ttu-id="d483b-235">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-236">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-236">Definition</span></span>

<span data-ttu-id="d483b-237">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-238">La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-239">Un mot clé `Keywords_hungary_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-240">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-241">La fonction `Func_hungary_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-242">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-242">Keywords</span></span>

#### <a name="keywords_hungary_eu_national_id_card"></a><span data-ttu-id="d483b-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="d483b-244">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-244">personal identification number</span></span>
  
<span data-ttu-id="d483b-245">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d483b-245">identification number</span></span>
  
<span data-ttu-id="d483b-246">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-246">personal id number</span></span>
  
<span data-ttu-id="d483b-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="d483b-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="d483b-248">Irlande</span><span class="sxs-lookup"><span data-stu-id="d483b-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="d483b-249">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-249">Format</span></span>

<span data-ttu-id="d483b-250">Combinaison de neuf caractères de lettres, de chiffres et d’un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d483b-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-251">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-251">Pattern</span></span>

<span data-ttu-id="d483b-252">Combinaison de neuf caractères de lettres, de chiffres et d’un espace dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d483b-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="d483b-253">Du 01 janvier 2013 au maintenant :</span><span class="sxs-lookup"><span data-stu-id="d483b-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="d483b-254">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d483b-254">Seven digits</span></span> 
    
- <span data-ttu-id="d483b-255">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-255">One check digit</span></span>
    
- <span data-ttu-id="d483b-256">Un espace ou la lettre majuscule « W » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d483b-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="d483b-257">Avant le 1er janvier 2013 :</span><span class="sxs-lookup"><span data-stu-id="d483b-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="d483b-258">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d483b-258">Seven digits</span></span> 
    
- <span data-ttu-id="d483b-259">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-259">One check digit</span></span>
    
- <span data-ttu-id="d483b-260">Un espace ou une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d483b-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-261">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-261">Checksum</span></span>

<span data-ttu-id="d483b-262">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-263">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-263">Definition</span></span>

<span data-ttu-id="d483b-264">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-265">La fonction trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="d483b-266">Un mot clé from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-266">A keyword from is found.</span></span>
    
<span data-ttu-id="d483b-267">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-268">La fonction trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-269">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-269">Keywords</span></span>

#### <a name="keywords_ireland_eu_national_id_card"></a><span data-ttu-id="d483b-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="d483b-271">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="d483b-271">personal public service number</span></span>
  
<span data-ttu-id="d483b-272">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="d483b-272">pps no</span></span>
  
<span data-ttu-id="d483b-273">Numéro de produit et d’assurance sociale</span><span class="sxs-lookup"><span data-stu-id="d483b-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="d483b-274">RSI non</span><span class="sxs-lookup"><span data-stu-id="d483b-274">rsi no</span></span>
  
<span data-ttu-id="d483b-275">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-275">personal identification number</span></span>
  
<span data-ttu-id="d483b-276">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="d483b-276">identification number</span></span>
  
<span data-ttu-id="d483b-277">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-277">personal id number</span></span>
  
<span data-ttu-id="d483b-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="d483b-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="d483b-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="d483b-279">uimh.</span></span> <span data-ttu-id="d483b-280">toxine</span><span class="sxs-lookup"><span data-stu-id="d483b-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="d483b-281">Italie</span><span class="sxs-lookup"><span data-stu-id="d483b-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="d483b-282">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-282">Format</span></span>

<span data-ttu-id="d483b-283">Combinaison de 16 caractères de lettres et de chiffres dans le modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="d483b-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-284">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-284">Pattern</span></span>

<span data-ttu-id="d483b-285">Combinaison de lettres et de chiffres de 16 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="d483b-286">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="d483b-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="d483b-287">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="d483b-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="d483b-288">Deux chiffres correspondant aux derniers chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="d483b-289">Une lettre correspondant à la lettre du mois de naissance : les lettres sont utilisées dans l’ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (par conséquent, le mois de janvier est A et le mois d’octobre est R).</span><span class="sxs-lookup"><span data-stu-id="d483b-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="d483b-290">Deux chiffres correspondant au jour du mois de naissance — afin de différencier les hommes, 40 est ajouté au jour de naissance pour les femmes</span><span class="sxs-lookup"><span data-stu-id="d483b-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="d483b-291">Quatre chiffres correspondant à l’indicatif régional propre à la municipalité où la personne est né (des codes pays sont utilisés pour les pays étrangers)</span><span class="sxs-lookup"><span data-stu-id="d483b-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="d483b-292">Un chiffre de parité</span><span class="sxs-lookup"><span data-stu-id="d483b-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-293">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-293">Checksum</span></span>

<span data-ttu-id="d483b-294">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-295">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-295">Definition</span></span>

<span data-ttu-id="d483b-296">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-297">La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-298">Un mot clé `Keywords_italy_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-299">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-300">La fonction `Func_italy_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-301">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-301">Keywords</span></span>

#### <a name="keywords_italy_eu_national_id_card"></a><span data-ttu-id="d483b-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="d483b-303">code personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-303">personal code</span></span>
  
<span data-ttu-id="d483b-304">Numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-304">personal code number</span></span>
  
<span data-ttu-id="d483b-305">Numéro de certificat personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-305">personal certificate number</span></span>
  
<span data-ttu-id="d483b-306">code fiscal</span><span class="sxs-lookup"><span data-stu-id="d483b-306">fiscal code</span></span>
  
<span data-ttu-id="d483b-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="d483b-307">personalcodeno#</span></span>
  
<span data-ttu-id="d483b-308">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-308">personal id number</span></span>
  
<span data-ttu-id="d483b-309">code d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-309">personal id code</span></span>
  
<span data-ttu-id="d483b-310">codice Personal</span><span class="sxs-lookup"><span data-stu-id="d483b-310">codice personale</span></span>
  
<span data-ttu-id="d483b-311">numération Certificate-personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-311">numero certificato personale</span></span>
  
<span data-ttu-id="d483b-312">numération personnelle</span><span class="sxs-lookup"><span data-stu-id="d483b-312">numero personale</span></span>
  
<span data-ttu-id="d483b-313">ID de numérotation personnelle</span><span class="sxs-lookup"><span data-stu-id="d483b-313">numero id personale</span></span>
  
<span data-ttu-id="d483b-314">codice ID personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-314">codice id personale</span></span>
  
<span data-ttu-id="d483b-315">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="d483b-315">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="d483b-316">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d483b-316">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="d483b-317">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-317">Format</span></span>

<span data-ttu-id="d483b-318">11 chiffres et un trait d’Union dans le format spécifié</span><span class="sxs-lookup"><span data-stu-id="d483b-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-319">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-319">Pattern</span></span>

<span data-ttu-id="d483b-320">11 chiffres et un trait d’Union :</span><span class="sxs-lookup"><span data-stu-id="d483b-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="d483b-321">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="d483b-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="d483b-322">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d483b-322">A hyphen</span></span>
    
- <span data-ttu-id="d483b-323">Un chiffre correspondant au siècle de naissance (« 0 » pour le 19 siècle, « 1 » pour le vingtième siècle et « 2 » pour le 21ème siècle).</span><span class="sxs-lookup"><span data-stu-id="d483b-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="d483b-324">Quatre chiffres, généré de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="d483b-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-325">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-325">Checksum</span></span>

<span data-ttu-id="d483b-326">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-327">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-327">Definition</span></span>

<span data-ttu-id="d483b-328">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-329">La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-330">Un mot clé `Keywords_latvia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-331">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-332">La fonction `Func_latvia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-333">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-333">Keywords</span></span>

#### <a name="keywords_latvia_eu_national_id_card"></a><span data-ttu-id="d483b-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="d483b-335">code personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-335">personal code</span></span>
  
<span data-ttu-id="d483b-336">Numéro de code personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-336">personal code number</span></span>
  
<span data-ttu-id="d483b-337">Numéro de certificat personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-337">personal certificate number</span></span>
  
<span data-ttu-id="d483b-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="d483b-338">personalcodeno#</span></span>
  
<span data-ttu-id="d483b-339">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-339">personal id number</span></span>
  
<span data-ttu-id="d483b-340">code d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-340">personal id code</span></span>
  
<span data-ttu-id="d483b-341">Personas kods</span><span class="sxs-lookup"><span data-stu-id="d483b-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="d483b-342">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d483b-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="d483b-343">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-343">Format</span></span>

<span data-ttu-id="d483b-344">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-345">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-345">Pattern</span></span>

<span data-ttu-id="d483b-346">11 chiffres sans espaces ni délimiteurs :</span><span class="sxs-lookup"><span data-stu-id="d483b-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="d483b-347">Un chiffre correspondant au sexe et au siècle de la personne</span><span class="sxs-lookup"><span data-stu-id="d483b-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="d483b-348">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d483b-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="d483b-349">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="d483b-350">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-351">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-351">Checksum</span></span>

<span data-ttu-id="d483b-352">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-353">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-353">Definition</span></span>

<span data-ttu-id="d483b-354">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-355">La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-356">Un mot clé `Keywords_lithuania_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-357">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-358">La fonction `Func_lithuania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-359">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-359">Keywords</span></span>

#### <a name="keywords_lithuania_eu_national_id_card"></a><span data-ttu-id="d483b-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="d483b-361">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-361">personal numeric code</span></span>
  
<span data-ttu-id="d483b-362">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-362">unique identification number</span></span>
  
<span data-ttu-id="d483b-363">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="d483b-363">citizen service number</span></span>
  
<span data-ttu-id="d483b-364">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-364">unique identity number</span></span>
  
<span data-ttu-id="d483b-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="d483b-366">code personnel.</span><span class="sxs-lookup"><span data-stu-id="d483b-366">personal code.</span></span>
  
<span data-ttu-id="d483b-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="d483b-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="d483b-368">unikalus identifikavimo</span><span class="sxs-lookup"><span data-stu-id="d483b-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="d483b-369">piliečio paslaugos</span><span class="sxs-lookup"><span data-stu-id="d483b-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="d483b-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="d483b-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="d483b-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="d483b-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="d483b-372">Relatif</span><span class="sxs-lookup"><span data-stu-id="d483b-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="d483b-373">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-373">Format</span></span>

<span data-ttu-id="d483b-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-375">Pattern</span></span>

<span data-ttu-id="d483b-376">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-376">11 digits</span></span>
  
- <span data-ttu-id="d483b-377">Un chiffre correspondant au sexe et au siècle de la personne</span><span class="sxs-lookup"><span data-stu-id="d483b-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="d483b-378">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d483b-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="d483b-379">Trois chiffres correspondant au numéro de série de la date de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="d483b-380">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-381">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-381">Checksum</span></span>

<span data-ttu-id="d483b-382">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d483b-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-383">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-383">Definition</span></span>

<span data-ttu-id="d483b-384">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-385">L’expression `Regex_luxemburg_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-386">Un mot clé `Keywords_luxemburg_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d483b-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-387">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_national_id_card"></a><span data-ttu-id="d483b-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="d483b-389">ID personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-389">personal id</span></span>
  
<span data-ttu-id="d483b-390">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-390">personal id number</span></span>
  
<span data-ttu-id="d483b-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="d483b-391">personalidno#</span></span>
  
<span data-ttu-id="d483b-392">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-392">unique id number</span></span>
  
<span data-ttu-id="d483b-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-393">personalidnumber#</span></span>
  
<span data-ttu-id="d483b-394">clé d’ID unique</span><span class="sxs-lookup"><span data-stu-id="d483b-394">unique id key</span></span>
  
<span data-ttu-id="d483b-395">code d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-395">personal id code</span></span>
  
<span data-ttu-id="d483b-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="d483b-396">uniqueidkey#</span></span>
  
<span data-ttu-id="d483b-397">code individuel</span><span class="sxs-lookup"><span data-stu-id="d483b-397">individual code</span></span>
  
<span data-ttu-id="d483b-398">ID individuel</span><span class="sxs-lookup"><span data-stu-id="d483b-398">individual id</span></span>
  
<span data-ttu-id="d483b-399">ID eindeutige-Nummer</span><span class="sxs-lookup"><span data-stu-id="d483b-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="d483b-400">ID eindeutige</span><span class="sxs-lookup"><span data-stu-id="d483b-400">eindeutige id</span></span>
  
<span data-ttu-id="d483b-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="d483b-401">id personnelle</span></span>
  
<span data-ttu-id="d483b-402">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="d483b-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="d483b-403">idpersonnelle#</span></span>
  
<span data-ttu-id="d483b-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="d483b-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="d483b-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="d483b-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="d483b-406">Malte</span><span class="sxs-lookup"><span data-stu-id="d483b-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="d483b-407">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-407">Format</span></span>

<span data-ttu-id="d483b-408">Sept chiffres suivis d’une lettre</span><span class="sxs-lookup"><span data-stu-id="d483b-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-409">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-409">Pattern</span></span>

<span data-ttu-id="d483b-410">Sept chiffres suivis d’une lettre :</span><span class="sxs-lookup"><span data-stu-id="d483b-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="d483b-411">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d483b-411">Seven digits</span></span> 
    
- <span data-ttu-id="d483b-412">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d483b-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-413">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-413">Checksum</span></span>

<span data-ttu-id="d483b-414">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d483b-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-415">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-415">Definition</span></span>

<span data-ttu-id="d483b-416">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-417">L’expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-418">Un mot clé `Keywords_malta_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-419">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-420">L’expression `Regex_malta_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-421">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-421">Keywords</span></span>

#### <a name="keywords_malta_eu_national_id_card"></a><span data-ttu-id="d483b-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="d483b-423">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-423">personal numeric code</span></span>
  
<span data-ttu-id="d483b-424">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-424">unique identification number</span></span>
  
<span data-ttu-id="d483b-425">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="d483b-425">citizen service number</span></span>
  
<span data-ttu-id="d483b-426">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-426">unique identity number</span></span>
  
<span data-ttu-id="d483b-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="d483b-428">Kodiċi numerali</span><span class="sxs-lookup"><span data-stu-id="d483b-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="d483b-429">numru ta’IDENTIFIKAZZJONI uniku</span><span class="sxs-lookup"><span data-stu-id="d483b-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="d483b-430">numru-Servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="d483b-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="d483b-431">numru ta’identità uniku</span><span class="sxs-lookup"><span data-stu-id="d483b-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="d483b-432">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d483b-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="d483b-433">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-433">Format</span></span>

<span data-ttu-id="d483b-434">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-435">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-435">Pattern</span></span>

<span data-ttu-id="d483b-436">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d483b-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-437">Checksum</span></span>

<span data-ttu-id="d483b-438">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-439">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-439">Definition</span></span>

<span data-ttu-id="d483b-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-441">La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-442">Un mot clé from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-442">A keyword from is found.</span></span>
    
<span data-ttu-id="d483b-443">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-444">La fonction `Func_netherlands_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-445">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-445">Keywords</span></span>

#### <a name="keywords_netherlands_eu_national_id_card"></a><span data-ttu-id="d483b-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="d483b-447">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-447">personal numeric code</span></span>
  
<span data-ttu-id="d483b-448">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-448">unique identification number</span></span>
  
<span data-ttu-id="d483b-449">Numéro de service du citoyen</span><span class="sxs-lookup"><span data-stu-id="d483b-449">citizen service number</span></span>
  
<span data-ttu-id="d483b-450">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-450">unique identity number</span></span>
  
<span data-ttu-id="d483b-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="d483b-452">BSN</span><span class="sxs-lookup"><span data-stu-id="d483b-452">bsn</span></span>
  
<span data-ttu-id="d483b-453">BSN #</span><span class="sxs-lookup"><span data-stu-id="d483b-453">bsn#</span></span>
  
<span data-ttu-id="d483b-454">persoonlijke Numerieke de code</span><span class="sxs-lookup"><span data-stu-id="d483b-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="d483b-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="d483b-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="d483b-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="d483b-456">burgerservicenummer</span></span>
  
<span data-ttu-id="d483b-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="d483b-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="d483b-458">Pologne</span><span class="sxs-lookup"><span data-stu-id="d483b-458">Poland</span></span>

<span data-ttu-id="d483b-459">Pour plus d’informations, reportez-vous à la section « Pologne national ID (PESEL) » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d483b-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="d483b-460">Portugal</span></span>

<span data-ttu-id="d483b-461">Pour plus d’informations, reportez-vous à la section « numéro de carte de citoyen Portugal » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="d483b-462">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d483b-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="d483b-463">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-463">Format</span></span>

<span data-ttu-id="d483b-464">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-465">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-465">Pattern</span></span>

<span data-ttu-id="d483b-466">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d483b-467">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-467">Checksum</span></span>

<span data-ttu-id="d483b-468">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-469">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-469">Definition</span></span>

<span data-ttu-id="d483b-470">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-471">La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-472">Un mot clé `Keywords_romania_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-474">La fonction `Func_romania_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-475">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-475">Keywords</span></span>

#### <a name="keywords_romania_eu_national_id_card"></a><span data-ttu-id="d483b-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="d483b-477">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-477">personal numeric code</span></span>
  
<span data-ttu-id="d483b-478">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-478">unique identification number</span></span>
  
<span data-ttu-id="d483b-479">cnp</span><span class="sxs-lookup"><span data-stu-id="d483b-479">cnp</span></span>
  
<span data-ttu-id="d483b-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="d483b-480">cnp#</span></span>
  
<span data-ttu-id="d483b-481">ancre</span><span class="sxs-lookup"><span data-stu-id="d483b-481">pin</span></span>
  
<span data-ttu-id="d483b-482">ancre #</span><span class="sxs-lookup"><span data-stu-id="d483b-482">pin#</span></span>
  
<span data-ttu-id="d483b-483">Numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="d483b-483">insurance number</span></span>
  
<span data-ttu-id="d483b-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-484">insurancenumber#</span></span>
  
<span data-ttu-id="d483b-485">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-485">unique identity number</span></span>
  
<span data-ttu-id="d483b-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="d483b-487">COD numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-487">cod numeric personal</span></span>
  
<span data-ttu-id="d483b-488">COD IDENTIFICARE personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-488">cod identificare personal</span></span>
  
<span data-ttu-id="d483b-489">COD UNIC IDENTIFICARE</span><span class="sxs-lookup"><span data-stu-id="d483b-489">cod unic identificare</span></span>
  
<span data-ttu-id="d483b-490">UNIC personnel număr</span><span class="sxs-lookup"><span data-stu-id="d483b-490">număr personal unic</span></span>
  
<span data-ttu-id="d483b-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="d483b-491">număr identitate</span></span>
  
<span data-ttu-id="d483b-492">număr IDENTIFICARE personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-492">număr identificare personal</span></span>
  
<span data-ttu-id="d483b-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="d483b-493">număridentitate#</span></span>
  
<span data-ttu-id="d483b-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="d483b-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="d483b-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="d483b-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="d483b-496">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d483b-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="d483b-497">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-497">Format</span></span>

<span data-ttu-id="d483b-498">Dix chiffres contenant une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="d483b-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-499">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-499">Pattern</span></span>

<span data-ttu-id="d483b-500">Dix chiffres contenant une barre oblique inverse :</span><span class="sxs-lookup"><span data-stu-id="d483b-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d483b-501">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-501">Checksum</span></span>

<span data-ttu-id="d483b-502">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-503">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-503">Definition</span></span>

<span data-ttu-id="d483b-504">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-505">La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-506">Un mot clé `Keywords_slovakia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-508">La fonction `Func_slovakia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-509">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-509">Keywords</span></span>

#### <a name="keywords_slovakia_eu_national_id_card"></a><span data-ttu-id="d483b-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="d483b-511">Numéro de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-511">birth number</span></span>
  
<span data-ttu-id="d483b-512">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-512">national identification number</span></span>
  
<span data-ttu-id="d483b-513">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-513">personal identification number</span></span>
  
<span data-ttu-id="d483b-514">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="d483b-514">social security number</span></span>
  
<span data-ttu-id="d483b-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-515">nationalnumber#</span></span>
  
<span data-ttu-id="d483b-516">SSN #</span><span class="sxs-lookup"><span data-stu-id="d483b-516">ssn#</span></span>
  
<span data-ttu-id="d483b-517">SSN</span><span class="sxs-lookup"><span data-stu-id="d483b-517">ssn</span></span>
  
<span data-ttu-id="d483b-518">numéro national</span><span class="sxs-lookup"><span data-stu-id="d483b-518">national number</span></span>
  
<span data-ttu-id="d483b-519">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-519">personal id number</span></span>
  
<span data-ttu-id="d483b-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="d483b-520">personalidnumber#</span></span>
  
<span data-ttu-id="d483b-521">rč</span><span class="sxs-lookup"><span data-stu-id="d483b-521">rč</span></span>
  
<span data-ttu-id="d483b-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="d483b-522">rodné číslo</span></span>
  
<span data-ttu-id="d483b-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="d483b-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="d483b-524">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d483b-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="d483b-525">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-525">Format</span></span>

<span data-ttu-id="d483b-526">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d483b-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-527">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-527">Pattern</span></span>

<span data-ttu-id="d483b-528">13 chiffres dans le modèle spécifié :</span><span class="sxs-lookup"><span data-stu-id="d483b-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="d483b-529">Sept chiffres correspondant à la date de naissance (DDMMLLL) où « LLL » correspond aux trois derniers chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="d483b-530">Deux chiffres correspondant à la zone de naissance</span><span class="sxs-lookup"><span data-stu-id="d483b-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="d483b-531">Trois chiffres correspondant à une combinaison de sexe et de numéro de série pour les personnes nées le même jour (000-499 pour les mâles et les 500-999 pour les femelles)</span><span class="sxs-lookup"><span data-stu-id="d483b-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="d483b-532">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-533">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-533">Checksum</span></span>

<span data-ttu-id="d483b-534">Oui</span><span class="sxs-lookup"><span data-stu-id="d483b-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-535">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-535">Definition</span></span>

<span data-ttu-id="d483b-536">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-537">La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-538">Un mot clé `Keywords_slovenia_eu_national_id_card` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="d483b-539">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-540">La fonction `Func_slovenia_eu_national_id_card` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d483b-541">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-541">Keywords</span></span>

#### <a name="keywords_slovenia_eu_national_id_card"></a><span data-ttu-id="d483b-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="d483b-543">code numérique personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-543">personal numeric code</span></span>
  
<span data-ttu-id="d483b-544">Numéro d’identification unique</span><span class="sxs-lookup"><span data-stu-id="d483b-544">unique identification number</span></span>
  
<span data-ttu-id="d483b-545">Numéro d’enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="d483b-545">unique registration number</span></span>
  
<span data-ttu-id="d483b-546">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-546">unique identity number</span></span>
  
<span data-ttu-id="d483b-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="d483b-548">Numéro de citoyen principal unique</span><span class="sxs-lookup"><span data-stu-id="d483b-548">unique master citizen number</span></span>
  
<span data-ttu-id="d483b-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="d483b-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="d483b-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="d483b-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="d483b-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="d483b-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="d483b-552">emšo</span><span class="sxs-lookup"><span data-stu-id="d483b-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="d483b-553">Espagne</span><span class="sxs-lookup"><span data-stu-id="d483b-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="d483b-554">Format</span><span class="sxs-lookup"><span data-stu-id="d483b-554">Format</span></span>

<span data-ttu-id="d483b-555">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="d483b-555">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d483b-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="d483b-556">Pattern</span></span>

<span data-ttu-id="d483b-557">Huit chiffres suivis d’un caractère</span><span class="sxs-lookup"><span data-stu-id="d483b-557">Eight digits followed by one character</span></span>
  
- <span data-ttu-id="d483b-558">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d483b-558">Eight digits</span></span>
    
- <span data-ttu-id="d483b-559">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d483b-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d483b-560">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d483b-560">Checksum</span></span>

<span data-ttu-id="d483b-561">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d483b-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d483b-562">Définition</span><span class="sxs-lookup"><span data-stu-id="d483b-562">Definition</span></span>

<span data-ttu-id="d483b-563">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d483b-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d483b-564">L’expression `Regex_spain_eu_national_id_card` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d483b-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d483b-565">Un mot clé `Keywords_spain_eu_national_id_card"` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d483b-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d483b-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d483b-566">Keywords</span></span>

#### <a name="keywords_spain_eu_national_id_card"></a><span data-ttu-id="d483b-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="d483b-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="d483b-568">DNI</span><span class="sxs-lookup"><span data-stu-id="d483b-568">dni</span></span>
  
<span data-ttu-id="d483b-569">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-569">national identification number</span></span>
  
<span data-ttu-id="d483b-570">Numéro d’identité nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-570">national identity number</span></span>
  
<span data-ttu-id="d483b-571">Numéro d’assurance</span><span class="sxs-lookup"><span data-stu-id="d483b-571">insurance number</span></span>
  
<span data-ttu-id="d483b-572">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="d483b-572">personal identification number</span></span>
  
<span data-ttu-id="d483b-573">identité nationale</span><span class="sxs-lookup"><span data-stu-id="d483b-573">national identity</span></span>
  
<span data-ttu-id="d483b-574">n ° d’identité personnelle</span><span class="sxs-lookup"><span data-stu-id="d483b-574">personal identity no</span></span>
  
<span data-ttu-id="d483b-575">Numéro d’identité unique</span><span class="sxs-lookup"><span data-stu-id="d483b-575">unique identity number</span></span>
  
<span data-ttu-id="d483b-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="d483b-576">nationalidno#</span></span>
  
<span data-ttu-id="d483b-577">quei #</span><span class="sxs-lookup"><span data-stu-id="d483b-577">uniqueid#</span></span>
  
<span data-ttu-id="d483b-578">DNI #</span><span class="sxs-lookup"><span data-stu-id="d483b-578">dni#</span></span>
  
<span data-ttu-id="d483b-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="d483b-579">nationalid#</span></span>
  
<span data-ttu-id="d483b-580">nie #</span><span class="sxs-lookup"><span data-stu-id="d483b-580">nie#</span></span>
  
<span data-ttu-id="d483b-581">nie</span><span class="sxs-lookup"><span data-stu-id="d483b-581">nie</span></span>
  
<span data-ttu-id="d483b-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="d483b-582">nienúmero#</span></span>
  
<span data-ttu-id="d483b-583">nie número</span><span class="sxs-lookup"><span data-stu-id="d483b-583">nie número</span></span>
  
<span data-ttu-id="d483b-584">Documento Nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="d483b-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="d483b-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="d483b-585">identidad único</span></span>
  
<span data-ttu-id="d483b-586">número Nacional identidad</span><span class="sxs-lookup"><span data-stu-id="d483b-586">número nacional identidad</span></span>
  
<span data-ttu-id="d483b-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="d483b-587">dni número</span></span>
  
<span data-ttu-id="d483b-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="d483b-588">dninúmero#</span></span>
  
<span data-ttu-id="d483b-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="d483b-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="d483b-590">Suède</span><span class="sxs-lookup"><span data-stu-id="d483b-590">Sweden</span></span>

<span data-ttu-id="d483b-591">Pour plus d’informations, reportez-vous à la section « ID national Suède » dans [la recherche des types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d483b-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d483b-592">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d483b-592">See also</span></span>

[<span data-ttu-id="d483b-593">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d483b-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

