---
title: Numéro d'identification fiscale de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique montre ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'il détecte le type d'informations sensibles du numéro d'identification fiscale de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410909"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="5273a-104">Numéro d'identification fiscale de l'UE</span><span class="sxs-lookup"><span data-stu-id="5273a-104">EU Tax Identification Number</span></span>

<span data-ttu-id="5273a-105">Cette rubrique montre ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'il détecte le type d'informations sensibles de l'ID taxe de l'UE (TIN).</span><span class="sxs-lookup"><span data-stu-id="5273a-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="5273a-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="5273a-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="5273a-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="5273a-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="5273a-108">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-108">Format</span></span>

<span data-ttu-id="5273a-109">Neuf chiffres avec un trait d'union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="5273a-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-110">Pattern</span></span>

<span data-ttu-id="5273a-111">Neuf chiffres avec un trait d'Union et une barre oblique facultatifs:</span><span class="sxs-lookup"><span data-stu-id="5273a-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="5273a-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-112">Two digits</span></span> 
    
- <span data-ttu-id="5273a-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5273a-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="5273a-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-114">Three digits</span></span>
    
- <span data-ttu-id="5273a-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="5273a-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="5273a-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-117">Checksum</span></span>

<span data-ttu-id="5273a-118">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-119">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-119">Definition</span></span>

<span data-ttu-id="5273a-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-125">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="5273a-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-127">tax number</span></span>
  
<span data-ttu-id="5273a-128">number</span><span class="sxs-lookup"><span data-stu-id="5273a-128">number</span></span>
  
<span data-ttu-id="5273a-129">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-129">tax registration number</span></span>
  
<span data-ttu-id="5273a-130">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-130">tax id</span></span>
  
<span data-ttu-id="5273a-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="5273a-131">st.nr.</span></span>
  
<span data-ttu-id="5273a-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="5273a-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="5273a-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="5273a-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="5273a-134">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-134">Format</span></span>

<span data-ttu-id="5273a-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-136">Pattern</span></span>

<span data-ttu-id="5273a-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5273a-137">11 digits:</span></span>
  
- <span data-ttu-id="5273a-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-138">Two digits</span></span>
    
- <span data-ttu-id="5273a-139">«0» ou «1»</span><span class="sxs-lookup"><span data-stu-id="5273a-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="5273a-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="5273a-140">One digit</span></span>
    
- <span data-ttu-id="5273a-141">«0» ou «1» ou «2» ou «3»</span><span class="sxs-lookup"><span data-stu-id="5273a-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="5273a-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-143">Checksum</span></span>

<span data-ttu-id="5273a-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-145">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-145">Definition</span></span>

<span data-ttu-id="5273a-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-147">L'expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-149">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="5273a-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-151">tax number</span></span>
  
<span data-ttu-id="5273a-152">Numéro d'enregistrement national</span><span class="sxs-lookup"><span data-stu-id="5273a-152">national registration number</span></span>
  
<span data-ttu-id="5273a-153">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-153">tax registration number</span></span>
  
<span data-ttu-id="5273a-154">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-154">tax id</span></span>
  
<span data-ttu-id="5273a-155">nPour</span><span class="sxs-lookup"><span data-stu-id="5273a-155">nif</span></span>
  
<span data-ttu-id="5273a-156">nPour</span><span class="sxs-lookup"><span data-stu-id="5273a-156">nif#</span></span>
  
<span data-ttu-id="5273a-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="5273a-157">numéro de registre national</span></span>
  
<span data-ttu-id="5273a-158">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="5273a-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="5273a-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="5273a-160">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-160">Format</span></span>

<span data-ttu-id="5273a-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-162">Pattern</span></span>

<span data-ttu-id="5273a-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-164">Checksum</span></span>

<span data-ttu-id="5273a-165">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-166">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-166">Definition</span></span>

<span data-ttu-id="5273a-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-172">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="5273a-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-174">bucn</span><span class="sxs-lookup"><span data-stu-id="5273a-174">bucn</span></span>
  
<span data-ttu-id="5273a-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="5273a-175">uniform civil number</span></span>
  
<span data-ttu-id="5273a-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="5273a-176">bucn#</span></span>
  
<span data-ttu-id="5273a-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="5273a-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="5273a-178">uniform civil id</span></span>
  
<span data-ttu-id="5273a-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="5273a-179">uniform civil no</span></span>
  
<span data-ttu-id="5273a-180">EGN</span><span class="sxs-lookup"><span data-stu-id="5273a-180">egn</span></span>
  
<span data-ttu-id="5273a-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="5273a-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="5273a-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="5273a-182">uniformcivilno#</span></span>
  
<span data-ttu-id="5273a-183">EGN #</span><span class="sxs-lookup"><span data-stu-id="5273a-183">egn#</span></span>
  
<span data-ttu-id="5273a-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="5273a-184">униформ граждански номер</span></span>
  
<span data-ttu-id="5273a-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="5273a-185">униформ id</span></span>
  
<span data-ttu-id="5273a-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="5273a-186">униформ граждански id</span></span>
  
<span data-ttu-id="5273a-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="5273a-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="5273a-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="5273a-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="5273a-189">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-189">Format</span></span>

<span data-ttu-id="5273a-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-191">Pattern</span></span>

<span data-ttu-id="5273a-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5273a-192">11 digits:</span></span>
  
- <span data-ttu-id="5273a-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="5273a-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="5273a-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-195">Checksum</span></span>

<span data-ttu-id="5273a-196">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-197">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-197">Definition</span></span>

<span data-ttu-id="5273a-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-203">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="5273a-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-205">tax number</span></span>
  
<span data-ttu-id="5273a-206">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-206">tax</span></span>
  
<span data-ttu-id="5273a-207">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-207">tax id</span></span>
  
<span data-ttu-id="5273a-208">oid</span><span class="sxs-lookup"><span data-stu-id="5273a-208">oid</span></span>
  
<span data-ttu-id="5273a-209">OID</span><span class="sxs-lookup"><span data-stu-id="5273a-209">oid#</span></span>
  
<span data-ttu-id="5273a-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="5273a-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="5273a-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="5273a-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="5273a-212">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-212">Format</span></span>

<span data-ttu-id="5273a-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-214">Pattern</span></span>

<span data-ttu-id="5273a-215">Huit chiffres et une lettre:</span><span class="sxs-lookup"><span data-stu-id="5273a-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="5273a-216">«0»</span><span class="sxs-lookup"><span data-stu-id="5273a-216">A "0"</span></span> 
    
- <span data-ttu-id="5273a-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-217">Seven digits</span></span>
    
- <span data-ttu-id="5273a-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-219">Checksum</span></span>

<span data-ttu-id="5273a-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-221">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-221">Definition</span></span>

<span data-ttu-id="5273a-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-227">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="5273a-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-229">tax number</span></span>
  
<span data-ttu-id="5273a-230">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-230">tax</span></span>
  
<span data-ttu-id="5273a-231">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-231">tax id</span></span>
  
<span data-ttu-id="5273a-232">code d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-232">tax identification code</span></span>
  
<span data-ttu-id="5273a-233">graduation</span><span class="sxs-lookup"><span data-stu-id="5273a-233">tic</span></span>
  
<span data-ttu-id="5273a-234">graduation</span><span class="sxs-lookup"><span data-stu-id="5273a-234">tic#</span></span>
  
<span data-ttu-id="5273a-235">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="5273a-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="5273a-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="5273a-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="5273a-237">Κωδικός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="5273a-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="5273a-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="5273a-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="5273a-239">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-239">Format</span></span>

<span data-ttu-id="5273a-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="5273a-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-241">Pattern</span></span>

<span data-ttu-id="5273a-242">Neuf ou dix chiffres avec une barre oblique inverse facultative:</span><span class="sxs-lookup"><span data-stu-id="5273a-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="5273a-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-243">Six digits</span></span> 
    
- <span data-ttu-id="5273a-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5273a-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="5273a-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-246">Checksum</span></span>

<span data-ttu-id="5273a-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-248">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-248">Definition</span></span>

<span data-ttu-id="5273a-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-250">L'expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-252">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="5273a-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-254">tax number</span></span>
  
<span data-ttu-id="5273a-255">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-255">tax</span></span>
  
<span data-ttu-id="5273a-256">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-256">tax id</span></span>
  
<span data-ttu-id="5273a-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-257">personal number</span></span>
  
<span data-ttu-id="5273a-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="5273a-258">daňové číslo</span></span>
  
<span data-ttu-id="5273a-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="5273a-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="5273a-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="5273a-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="5273a-261">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-261">Format</span></span>

<span data-ttu-id="5273a-262">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="5273a-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-263">Pattern</span></span>

<span data-ttu-id="5273a-264">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="5273a-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="5273a-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="5273a-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="5273a-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="5273a-266">A hyphen</span></span>
    
- <span data-ttu-id="5273a-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l'individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="5273a-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-268">Checksum</span></span>

<span data-ttu-id="5273a-269">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-270">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-270">Definition</span></span>

<span data-ttu-id="5273a-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-276">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="5273a-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-278">tax number</span></span>
  
<span data-ttu-id="5273a-279">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-279">tax</span></span>
  
<span data-ttu-id="5273a-280">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-280">tax id</span></span>
  
<span data-ttu-id="5273a-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="5273a-281">cpr number</span></span>
  
<span data-ttu-id="5273a-282">cardio</span><span class="sxs-lookup"><span data-stu-id="5273a-282">cpr#</span></span>
  
<span data-ttu-id="5273a-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="5273a-283">skat nummer</span></span>
  
<span data-ttu-id="5273a-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="5273a-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="5273a-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="5273a-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="5273a-286">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-286">Format</span></span>

<span data-ttu-id="5273a-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-288">Pattern</span></span>

<span data-ttu-id="5273a-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5273a-289">11 digits:</span></span>
  
-  <span data-ttu-id="5273a-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit: 1,2 pour le 19 siècle; 3, 4 pour le vingtième siècle; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="5273a-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="5273a-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="5273a-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="5273a-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="5273a-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="5273a-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-294">Checksum</span></span>

<span data-ttu-id="5273a-295">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-296">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-296">Definition</span></span>

<span data-ttu-id="5273a-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-302">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="5273a-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-304">tax number</span></span>
  
<span data-ttu-id="5273a-305">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-305">tax</span></span>
  
<span data-ttu-id="5273a-306">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-306">tax id</span></span>
  
<span data-ttu-id="5273a-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-307">personal code</span></span>
  
<span data-ttu-id="5273a-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="5273a-308">maksunumber</span></span>
  
<span data-ttu-id="5273a-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="5273a-309">maksu id</span></span>
  
<span data-ttu-id="5273a-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="5273a-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="5273a-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="5273a-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="5273a-312">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-312">Format</span></span>

<span data-ttu-id="5273a-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="5273a-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-314">Pattern</span></span>

<span data-ttu-id="5273a-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins:</span><span class="sxs-lookup"><span data-stu-id="5273a-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="5273a-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-316">Six digits</span></span>
    
- <span data-ttu-id="5273a-317">L'une des options suivantes: un signe plus, un signe moins ou la lettre «A» (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et «A» désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="5273a-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="5273a-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-318">Three digits</span></span>
    
- <span data-ttu-id="5273a-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="5273a-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-320">Checksum</span></span>

<span data-ttu-id="5273a-321">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-322">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-322">Definition</span></span>

<span data-ttu-id="5273a-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-328">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="5273a-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-330">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="5273a-330">identification number</span></span>
  
<span data-ttu-id="5273a-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-331">personal id</span></span>
  
<span data-ttu-id="5273a-332">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="5273a-332">identity number</span></span>
  
<span data-ttu-id="5273a-333">Numéro d'identification national finnois</span><span class="sxs-lookup"><span data-stu-id="5273a-333">finnish national id number</span></span>
  
<span data-ttu-id="5273a-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-334">personalidnumber#</span></span>
  
<span data-ttu-id="5273a-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="5273a-335">national identification number</span></span>
  
<span data-ttu-id="5273a-336">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="5273a-336">id number</span></span>
  
<span data-ttu-id="5273a-337">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="5273a-337">national id no.</span></span>
  
<span data-ttu-id="5273a-338">Numéro d'identification national</span><span class="sxs-lookup"><span data-stu-id="5273a-338">national id number</span></span>
  
<span data-ttu-id="5273a-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="5273a-339">id no</span></span>
  
<span data-ttu-id="5273a-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5273a-340">tunnistenumero</span></span>
  
<span data-ttu-id="5273a-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5273a-341">henkilötunnus</span></span>
  
<span data-ttu-id="5273a-342">Yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5273a-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="5273a-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="5273a-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="5273a-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="5273a-344">identiteetti numero</span></span>
  
<span data-ttu-id="5273a-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5273a-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="5273a-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="5273a-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="5273a-347">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5273a-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="5273a-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="5273a-348">tunnusnumero</span></span>
  
<span data-ttu-id="5273a-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="5273a-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="5273a-350">France</span><span class="sxs-lookup"><span data-stu-id="5273a-350">France</span></span>

### <a name="format"></a><span data-ttu-id="5273a-351">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-351">Format</span></span>

<span data-ttu-id="5273a-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="5273a-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-353">Pattern</span></span>

<span data-ttu-id="5273a-354">13 chiffres pour les personnes:</span><span class="sxs-lookup"><span data-stu-id="5273a-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="5273a-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="5273a-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="5273a-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-356">12 digits</span></span>
    
<span data-ttu-id="5273a-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="5273a-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-358">Checksum</span></span>

<span data-ttu-id="5273a-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-360">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-360">Definition</span></span>

<span data-ttu-id="5273a-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-366">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="5273a-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-368">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-368">tax identification number</span></span>
  
<span data-ttu-id="5273a-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-369">tax number</span></span>
  
<span data-ttu-id="5273a-370">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-370">tax id</span></span>
  
<span data-ttu-id="5273a-371">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="5273a-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="5273a-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="5273a-373">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-373">Format</span></span>

<span data-ttu-id="5273a-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-375">Pattern</span></span>

<span data-ttu-id="5273a-376">11 chiffres:</span><span class="sxs-lookup"><span data-stu-id="5273a-376">11 digits :</span></span>
  
-  <span data-ttu-id="5273a-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-377">Ten digits</span></span> 
    
- <span data-ttu-id="5273a-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-379">Checksum</span></span>

<span data-ttu-id="5273a-380">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-381">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-381">Definition</span></span>

<span data-ttu-id="5273a-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-387">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="5273a-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-389">tax number</span></span>
  
<span data-ttu-id="5273a-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-390">tax no.</span></span>
  
<span data-ttu-id="5273a-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-391">taxno#</span></span>
  
<span data-ttu-id="5273a-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-392">taxnumber#</span></span>
  
<span data-ttu-id="5273a-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-393">taxnumber</span></span>
  
<span data-ttu-id="5273a-394">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-394">tax id</span></span>
  
<span data-ttu-id="5273a-395">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-395">taxid#</span></span>
  
<span data-ttu-id="5273a-396">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-396">tax identification number</span></span>
  
<span data-ttu-id="5273a-397">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-397">tax identification no.</span></span>
  
<span data-ttu-id="5273a-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="5273a-398">steuernummer</span></span>
  
<span data-ttu-id="5273a-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="5273a-399">steuer id</span></span>
  
<span data-ttu-id="5273a-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5273a-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="5273a-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="5273a-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="5273a-402">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-402">Format</span></span>

<span data-ttu-id="5273a-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-404">Pattern</span></span>

<span data-ttu-id="5273a-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-406">Checksum</span></span>

<span data-ttu-id="5273a-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-408">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-408">Definition</span></span>

<span data-ttu-id="5273a-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-410">L'expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-412">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="5273a-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-414">financement</span><span class="sxs-lookup"><span data-stu-id="5273a-414">afm</span></span>
  
<span data-ttu-id="5273a-415">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-415">tin</span></span>
  
<span data-ttu-id="5273a-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-416">tax id no.</span></span>
  
<span data-ttu-id="5273a-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-417">tax id no</span></span>
  
<span data-ttu-id="5273a-418">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-418">tax identification number</span></span>
  
<span data-ttu-id="5273a-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="5273a-419">tax registry number</span></span>
  
<span data-ttu-id="5273a-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-420">tax registry no.</span></span>
  
<span data-ttu-id="5273a-421">financement</span><span class="sxs-lookup"><span data-stu-id="5273a-421">afm#</span></span>
  
<span data-ttu-id="5273a-422">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-422">tin#</span></span>
  
<span data-ttu-id="5273a-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="5273a-423">taxidno#</span></span>
  
<span data-ttu-id="5273a-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="5273a-424">taxregistryno#</span></span>
  
<span data-ttu-id="5273a-425">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="5273a-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="5273a-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="5273a-426">aφμ</span></span>
  
<span data-ttu-id="5273a-427">aφμ Αριθμός</span><span class="sxs-lookup"><span data-stu-id="5273a-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="5273a-428">φορολογικού Μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="5273a-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="5273a-429">τον αριθμό φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="5273a-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="5273a-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="5273a-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="5273a-431">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-431">Format</span></span>

<span data-ttu-id="5273a-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-433">Pattern</span></span>

<span data-ttu-id="5273a-434">Dix chiffres:</span><span class="sxs-lookup"><span data-stu-id="5273a-434">Ten digits:</span></span>
  
-  <span data-ttu-id="5273a-435">Un chiffre qui doit être «8»</span><span class="sxs-lookup"><span data-stu-id="5273a-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="5273a-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="5273a-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="5273a-437">Trois chiffres correspondant au nombre généré par l'opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="5273a-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="5273a-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-439">Checksum</span></span>

<span data-ttu-id="5273a-440">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-441">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-441">Definition</span></span>

<span data-ttu-id="5273a-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-447">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="5273a-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-449">Numéro d'identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="5273a-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="5273a-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="5273a-450">hungarian tin</span></span>
  
<span data-ttu-id="5273a-451">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-451">tax id number</span></span>
  
<span data-ttu-id="5273a-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="5273a-452">vat number</span></span>
  
<span data-ttu-id="5273a-453">Numéro de l'autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-453">tax authority no</span></span>
  
<span data-ttu-id="5273a-454">Numéro d'identité fiscale de l'ID taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-454">tax id tax identity number</span></span>
  
<span data-ttu-id="5273a-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-455">taxidnumber#</span></span>
  
<span data-ttu-id="5273a-456">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-456">tin#</span></span>
  
<span data-ttu-id="5273a-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="5273a-457">hungatiantin#</span></span>
  
<span data-ttu-id="5273a-458">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-458">tax identification no</span></span>
  
<span data-ttu-id="5273a-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="5273a-459">taxidno#</span></span>
  
<span data-ttu-id="5273a-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="5273a-460">adóazonosító szám</span></span>
  
<span data-ttu-id="5273a-461">adószám</span><span class="sxs-lookup"><span data-stu-id="5273a-461">adószám</span></span>
  
<span data-ttu-id="5273a-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="5273a-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="5273a-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="5273a-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="5273a-464">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-464">Format</span></span>

<span data-ttu-id="5273a-465">Sept chiffres suivis d'une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-466">Pattern</span></span>

<span data-ttu-id="5273a-467">Sept chiffres suivis d'une lettre:</span><span class="sxs-lookup"><span data-stu-id="5273a-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="5273a-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-468">Seven digits</span></span> 
    
- <span data-ttu-id="5273a-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-470">Checksum</span></span>

<span data-ttu-id="5273a-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-472">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-472">Definition</span></span>

<span data-ttu-id="5273a-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-478">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="5273a-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="5273a-480">public service no</span></span>
  
<span data-ttu-id="5273a-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-481">personal public service no</span></span>
  
<span data-ttu-id="5273a-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="5273a-482">pps no</span></span>
  
<span data-ttu-id="5273a-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-483">personal service no</span></span>
  
<span data-ttu-id="5273a-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="5273a-484">pps service no</span></span>
  
<span data-ttu-id="5273a-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="5273a-485">ppsno#</span></span>
  
<span data-ttu-id="5273a-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="5273a-486">irish pps no</span></span>
  
<span data-ttu-id="5273a-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="5273a-487">publicserviceno#</span></span>
  
<span data-ttu-id="5273a-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="5273a-488">personal public service number</span></span>
  
<span data-ttu-id="5273a-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="5273a-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="5273a-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="5273a-490">pps uimh</span></span>
  
<span data-ttu-id="5273a-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="5273a-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="5273a-492">Italie</span><span class="sxs-lookup"><span data-stu-id="5273a-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="5273a-493">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-493">Format</span></span>

<span data-ttu-id="5273a-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-495">Pattern</span></span>

<span data-ttu-id="5273a-496">16 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="5273a-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="5273a-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="5273a-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="5273a-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="5273a-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="5273a-499">Deux chiffres correspondant aux derniers chiffres de l'année de naissance</span><span class="sxs-lookup"><span data-stu-id="5273a-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="5273a-500">Un chiffre correspondant au mois de naissance: les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="5273a-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="5273a-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="5273a-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="5273a-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="5273a-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="5273a-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-504">Checksum</span></span>

<span data-ttu-id="5273a-505">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-506">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-506">Definition</span></span>

<span data-ttu-id="5273a-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-512">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="5273a-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-514">tax number</span></span>
  
<span data-ttu-id="5273a-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-515">tax no.</span></span>
  
<span data-ttu-id="5273a-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-516">taxno#</span></span>
  
<span data-ttu-id="5273a-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-517">taxnumber#</span></span>
  
<span data-ttu-id="5273a-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-518">taxnumber</span></span>
  
<span data-ttu-id="5273a-519">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-519">tax id</span></span>
  
<span data-ttu-id="5273a-520">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-520">taxid#</span></span>
  
<span data-ttu-id="5273a-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-521">fiscal code</span></span>
  
<span data-ttu-id="5273a-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="5273a-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="5273a-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="5273a-524">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-524">Format</span></span>

<span data-ttu-id="5273a-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-526">Pattern</span></span>

<span data-ttu-id="5273a-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="5273a-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="5273a-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="5273a-529">Un chiffre correspondant au siècle de naissance où «0» correspond à 19 siècle, «1» correspond au vingtième siècle et «2» au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="5273a-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="5273a-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-531">Checksum</span></span>

<span data-ttu-id="5273a-532">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-533">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-533">Definition</span></span>

<span data-ttu-id="5273a-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-539">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="5273a-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-541">tax number</span></span>
  
<span data-ttu-id="5273a-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-542">tax no.</span></span>
  
<span data-ttu-id="5273a-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-543">taxno#</span></span>
  
<span data-ttu-id="5273a-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-544">taxnumber#</span></span>
  
<span data-ttu-id="5273a-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-545">taxnumber</span></span>
  
<span data-ttu-id="5273a-546">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-546">tax id</span></span>
  
<span data-ttu-id="5273a-547">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-547">taxid#</span></span>
  
<span data-ttu-id="5273a-548">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-548">tax identification number</span></span>
  
<span data-ttu-id="5273a-549">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-549">tax identification no.</span></span>
  
<span data-ttu-id="5273a-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="5273a-550">nodokļa numurs</span></span>
  
<span data-ttu-id="5273a-551">nodokļu IDENTIFIKĀCIJAS numurs</span><span class="sxs-lookup"><span data-stu-id="5273a-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="5273a-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="5273a-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="5273a-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="5273a-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="5273a-554">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-554">Format</span></span>

<span data-ttu-id="5273a-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-556">Pattern</span></span>

<span data-ttu-id="5273a-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-558">Checksum</span></span>

<span data-ttu-id="5273a-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-560">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-560">Definition</span></span>

<span data-ttu-id="5273a-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-566">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="5273a-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-568">tax number</span></span>
  
<span data-ttu-id="5273a-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-569">tax no.</span></span>
  
<span data-ttu-id="5273a-570">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="5273a-570">tax no#</span></span>
  
<span data-ttu-id="5273a-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-571">taxnumber#</span></span>
  
<span data-ttu-id="5273a-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-572">taxnumber</span></span>
  
<span data-ttu-id="5273a-573">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-573">tax id</span></span>
  
<span data-ttu-id="5273a-574">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-574">taxid#</span></span>
  
<span data-ttu-id="5273a-575">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-575">tax identification number</span></span>
  
<span data-ttu-id="5273a-576">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-576">tax identification no.</span></span>
  
<span data-ttu-id="5273a-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="5273a-577">mokesčių id</span></span>
  
<span data-ttu-id="5273a-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-578">mokesčių numeris</span></span>
  
<span data-ttu-id="5273a-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="5273a-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="5273a-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="5273a-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="5273a-581">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-581">Format</span></span>

<span data-ttu-id="5273a-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-583">Pattern</span></span>

<span data-ttu-id="5273a-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="5273a-584">13 digits:</span></span>
  
-  <span data-ttu-id="5273a-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-585">11 digits</span></span> 
    
- <span data-ttu-id="5273a-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-587">Checksum</span></span>

<span data-ttu-id="5273a-588">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-589">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-589">Definition</span></span>

<span data-ttu-id="5273a-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-595">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="5273a-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-597">tax number</span></span>
  
<span data-ttu-id="5273a-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-598">tax no.</span></span>
  
<span data-ttu-id="5273a-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-599">taxno#</span></span>
  
<span data-ttu-id="5273a-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-600">taxnumber#</span></span>
  
<span data-ttu-id="5273a-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-601">taxnumber</span></span>
  
<span data-ttu-id="5273a-602">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-602">tax id</span></span>
  
<span data-ttu-id="5273a-603">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-603">taxid#</span></span>
  
<span data-ttu-id="5273a-604">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-604">tax identification number</span></span>
  
<span data-ttu-id="5273a-605">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-605">tax identification no.</span></span>
  
<span data-ttu-id="5273a-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="5273a-606">steuernummer</span></span>
  
<span data-ttu-id="5273a-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="5273a-607">steuer id</span></span>
  
<span data-ttu-id="5273a-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5273a-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="5273a-609">Malte</span><span class="sxs-lookup"><span data-stu-id="5273a-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="5273a-610">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-610">Format</span></span>

<span data-ttu-id="5273a-611">Pour les ressortissants maltais: 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="5273a-612">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-613">Pattern</span></span>

<span data-ttu-id="5273a-614">Ressortissants maltaises: 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="5273a-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="5273a-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-615">Seven digits</span></span> 
    
- <span data-ttu-id="5273a-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="5273a-617">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="5273a-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="5273a-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-619">Checksum</span></span>

<span data-ttu-id="5273a-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-621">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-621">Definition</span></span>

<span data-ttu-id="5273a-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-627">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="5273a-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-629">tax number</span></span>
  
<span data-ttu-id="5273a-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-630">tax no.</span></span>
  
<span data-ttu-id="5273a-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-631">taxno#</span></span>
  
<span data-ttu-id="5273a-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-632">taxnumber#</span></span>
  
<span data-ttu-id="5273a-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-633">taxnumber</span></span>
  
<span data-ttu-id="5273a-634">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-634">tax id</span></span>
  
<span data-ttu-id="5273a-635">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-635">taxid#</span></span>
  
<span data-ttu-id="5273a-636">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-636">tax identification number</span></span>
  
<span data-ttu-id="5273a-637">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-637">tax identification no.</span></span>
  
<span data-ttu-id="5273a-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="5273a-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="5273a-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="5273a-639">id tat-taxxa</span></span>
  
<span data-ttu-id="5273a-640">numru ta'IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="5273a-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="5273a-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="5273a-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="5273a-642">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-642">Format</span></span>

<span data-ttu-id="5273a-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-644">Pattern</span></span>

<span data-ttu-id="5273a-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="5273a-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-646">Checksum</span></span>

<span data-ttu-id="5273a-647">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-648">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-648">Definition</span></span>

<span data-ttu-id="5273a-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-654">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="5273a-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-656">Numéro d'identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="5273a-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="5273a-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="5273a-657">netherlands tax identification</span></span>
  
<span data-ttu-id="5273a-658">Numéro d'identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="5273a-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="5273a-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="5273a-659">netherland's tax identification</span></span>
  
<span data-ttu-id="5273a-660">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-660">tax identification number</span></span>
  
<span data-ttu-id="5273a-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="5273a-661">dutch tax id</span></span>
  
<span data-ttu-id="5273a-662">Numéro d'identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="5273a-662">dutch tax identification number</span></span>
  
<span data-ttu-id="5273a-663">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-663">tax id</span></span>
  
<span data-ttu-id="5273a-664">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-664">tax id#</span></span>
  
<span data-ttu-id="5273a-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-665">tax number</span></span>
  
<span data-ttu-id="5273a-666">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="5273a-666">tax no#</span></span>
  
<span data-ttu-id="5273a-667">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-667">tax#</span></span>
  
<span data-ttu-id="5273a-668">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-668">tin</span></span>
  
<span data-ttu-id="5273a-669">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-669">tin#</span></span>
  
<span data-ttu-id="5273a-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="5273a-670">netherlands tin</span></span>
  
<span data-ttu-id="5273a-671">Netherland d'étain</span><span class="sxs-lookup"><span data-stu-id="5273a-671">netherland's tin</span></span>
  
<span data-ttu-id="5273a-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="5273a-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="5273a-673">identificatienummer van à l'avant-dernière</span><span class="sxs-lookup"><span data-stu-id="5273a-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="5273a-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="5273a-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="5273a-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="5273a-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="5273a-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="5273a-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="5273a-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="5273a-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="5273a-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="5273a-678">btw nummer</span></span>
  
<span data-ttu-id="5273a-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="5273a-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="5273a-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="5273a-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="5273a-681">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-681">Format</span></span>

<span data-ttu-id="5273a-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-683">Pattern</span></span>

<span data-ttu-id="5273a-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-685">Checksum</span></span>

<span data-ttu-id="5273a-686">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-687">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-687">Definition</span></span>

<span data-ttu-id="5273a-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-693">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="5273a-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-695">tax number</span></span>
  
<span data-ttu-id="5273a-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-696">tax no.</span></span>
  
<span data-ttu-id="5273a-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-697">taxno#</span></span>
  
<span data-ttu-id="5273a-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-698">taxnumber#</span></span>
  
<span data-ttu-id="5273a-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-699">taxnumber</span></span>
  
<span data-ttu-id="5273a-700">pince</span><span class="sxs-lookup"><span data-stu-id="5273a-700">nip</span></span>
  
<span data-ttu-id="5273a-701">pince</span><span class="sxs-lookup"><span data-stu-id="5273a-701">nip#</span></span>
  
<span data-ttu-id="5273a-702">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-702">tax id</span></span>
  
<span data-ttu-id="5273a-703">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-703">tax id#</span></span>
  
<span data-ttu-id="5273a-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="5273a-704">nip id</span></span>
  
<span data-ttu-id="5273a-705">n ° de NIP</span><span class="sxs-lookup"><span data-stu-id="5273a-705">nip id#</span></span>
  
<span data-ttu-id="5273a-706">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-706">tax identification number</span></span>
  
<span data-ttu-id="5273a-707">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-707">tax identification no.</span></span>
  
<span data-ttu-id="5273a-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="5273a-708">vat number</span></span>
  
<span data-ttu-id="5273a-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="5273a-709">vat no.</span></span>
  
<span data-ttu-id="5273a-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="5273a-710">vatno#</span></span>
  
<span data-ttu-id="5273a-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="5273a-711">vat id</span></span>
  
<span data-ttu-id="5273a-712">n ° de TVA</span><span class="sxs-lookup"><span data-stu-id="5273a-712">vat id#</span></span>
  
<span data-ttu-id="5273a-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="5273a-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="5273a-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="5273a-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="5273a-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="5273a-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="5273a-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="5273a-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="5273a-717">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-717">Format</span></span>

<span data-ttu-id="5273a-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-719">Pattern</span></span>

<span data-ttu-id="5273a-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-721">Checksum</span></span>

<span data-ttu-id="5273a-722">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-723">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-723">Definition</span></span>

<span data-ttu-id="5273a-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-729">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="5273a-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-731">tax number</span></span>
  
<span data-ttu-id="5273a-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-732">tax no.</span></span>
  
<span data-ttu-id="5273a-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-733">taxno#</span></span>
  
<span data-ttu-id="5273a-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="5273a-734">taxnumber#</span></span>
  
<span data-ttu-id="5273a-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="5273a-735">taxnumber</span></span>
  
<span data-ttu-id="5273a-736">nPour</span><span class="sxs-lookup"><span data-stu-id="5273a-736">nif</span></span>
  
<span data-ttu-id="5273a-737">nPour</span><span class="sxs-lookup"><span data-stu-id="5273a-737">nif#</span></span>
  
<span data-ttu-id="5273a-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="5273a-738">numero fiscal</span></span>
  
<span data-ttu-id="5273a-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="5273a-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="5273a-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="5273a-741">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-741">Format</span></span>

<span data-ttu-id="5273a-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-743">Pattern</span></span>

<span data-ttu-id="5273a-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-745">Checksum</span></span>

<span data-ttu-id="5273a-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-747">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-747">Definition</span></span>

<span data-ttu-id="5273a-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-749">L'expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-751">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="5273a-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-753">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-753">tax id</span></span>
  
<span data-ttu-id="5273a-754">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-754">tax id number</span></span>
  
<span data-ttu-id="5273a-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-755">tax file no</span></span>
  
<span data-ttu-id="5273a-756">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-756">tax file number</span></span>
  
<span data-ttu-id="5273a-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-757">tax no</span></span>
  
<span data-ttu-id="5273a-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-758">tax number</span></span>
  
<span data-ttu-id="5273a-759">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-759">taxid#</span></span>
  
<span data-ttu-id="5273a-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-760">taxno#</span></span>
  
<span data-ttu-id="5273a-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="5273a-761">id-ul taxei</span></span>
  
<span data-ttu-id="5273a-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="5273a-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="5273a-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="5273a-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="5273a-764">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-764">Format</span></span>

<span data-ttu-id="5273a-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-766">Pattern</span></span>

<span data-ttu-id="5273a-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-768">Checksum</span></span>

<span data-ttu-id="5273a-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5273a-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-770">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-770">Definition</span></span>

<span data-ttu-id="5273a-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-772">L'expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-774">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="5273a-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-776">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-776">tax id</span></span>
  
<span data-ttu-id="5273a-777">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-777">tax id number</span></span>
  
<span data-ttu-id="5273a-778">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="5273a-778">tin id</span></span>
  
<span data-ttu-id="5273a-779">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="5273a-779">tin no</span></span>
  
<span data-ttu-id="5273a-780">ID d'étain slovaque</span><span class="sxs-lookup"><span data-stu-id="5273a-780">slovakian tin id</span></span>
  
<span data-ttu-id="5273a-781">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-781">tin</span></span>
  
<span data-ttu-id="5273a-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-782">tax file no</span></span>
  
<span data-ttu-id="5273a-783">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-783">tax file number</span></span>
  
<span data-ttu-id="5273a-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-784">tax no</span></span>
  
<span data-ttu-id="5273a-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-785">tax number</span></span>
  
<span data-ttu-id="5273a-786">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-786">taxid#</span></span>
  
<span data-ttu-id="5273a-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-787">taxno#</span></span>
  
<span data-ttu-id="5273a-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="5273a-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="5273a-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="5273a-789">daňové číslo</span></span>
  
<span data-ttu-id="5273a-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="5273a-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="5273a-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="5273a-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="5273a-792">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-792">Format</span></span>

<span data-ttu-id="5273a-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-794">Pattern</span></span>

<span data-ttu-id="5273a-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-796">Checksum</span></span>

<span data-ttu-id="5273a-797">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-798">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-798">Definition</span></span>

<span data-ttu-id="5273a-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-804">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="5273a-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-806">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-806">tax id</span></span>
  
<span data-ttu-id="5273a-807">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-807">tax id number</span></span>
  
<span data-ttu-id="5273a-808">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="5273a-808">tin id</span></span>
  
<span data-ttu-id="5273a-809">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="5273a-809">tin no</span></span>
  
<span data-ttu-id="5273a-810">ID d'étain slovène</span><span class="sxs-lookup"><span data-stu-id="5273a-810">slovenian tin id</span></span>
  
<span data-ttu-id="5273a-811">Etain</span><span class="sxs-lookup"><span data-stu-id="5273a-811">tin</span></span>
  
<span data-ttu-id="5273a-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-812">tax file no</span></span>
  
<span data-ttu-id="5273a-813">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-813">tax file number</span></span>
  
<span data-ttu-id="5273a-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-814">tax no</span></span>
  
<span data-ttu-id="5273a-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-815">tax number</span></span>
  
<span data-ttu-id="5273a-816">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-816">taxid#</span></span>
  
<span data-ttu-id="5273a-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-817">taxno#</span></span>
  
<span data-ttu-id="5273a-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="5273a-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="5273a-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="5273a-819">davčna številka</span></span>
  
<span data-ttu-id="5273a-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="5273a-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="5273a-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="5273a-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="5273a-822">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-822">Format</span></span>

<span data-ttu-id="5273a-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-824">Pattern</span></span>

<span data-ttu-id="5273a-825">Personnes physiques espagnoles avec une carte d'identité nationale d'Espagne:</span><span class="sxs-lookup"><span data-stu-id="5273a-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="5273a-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-826">Eight digits</span></span> 
    
- <span data-ttu-id="5273a-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="5273a-828">Spaniards non résident sans carte d'identité nationale d'Espagne</span><span class="sxs-lookup"><span data-stu-id="5273a-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="5273a-829">Une lettre majuscule «L» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="5273a-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-830">Seven digits</span></span>
    
- <span data-ttu-id="5273a-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="5273a-832">Spaniards résident de moins de 14 ans sans carte d'identité nationale (Espagne):</span><span class="sxs-lookup"><span data-stu-id="5273a-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="5273a-833">Une lettre majuscule «K» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="5273a-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-834">Seven digits</span></span> 
    
- <span data-ttu-id="5273a-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="5273a-836">Foreigners avec le numéro d'identification d'un étranger</span><span class="sxs-lookup"><span data-stu-id="5273a-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="5273a-837">Une lettre majuscule qui est «X», «Y» ou «Z» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="5273a-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-838">Seven digits</span></span>
    
- <span data-ttu-id="5273a-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="5273a-840">Foreigners sans numéro d'identification étranger</span><span class="sxs-lookup"><span data-stu-id="5273a-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="5273a-841">Une lettre majuscule qui est «M» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="5273a-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="5273a-842">Seven digits</span></span>
    
- <span data-ttu-id="5273a-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="5273a-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="5273a-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-844">Checksum</span></span>

<span data-ttu-id="5273a-845">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-846">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-846">Definition</span></span>

<span data-ttu-id="5273a-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-852">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="5273a-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-854">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-854">tax id</span></span>
  
<span data-ttu-id="5273a-855">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-855">tax id number</span></span>
  
<span data-ttu-id="5273a-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="5273a-856">cif id</span></span>
  
<span data-ttu-id="5273a-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="5273a-857">cif no</span></span>
  
<span data-ttu-id="5273a-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="5273a-858">spanish cif id</span></span>
  
<span data-ttu-id="5273a-859">importation</span><span class="sxs-lookup"><span data-stu-id="5273a-859">cif</span></span>
  
<span data-ttu-id="5273a-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-860">tax file no</span></span>
  
<span data-ttu-id="5273a-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="5273a-861">spanish cif number</span></span>
  
<span data-ttu-id="5273a-862">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-862">tax file number</span></span>
  
<span data-ttu-id="5273a-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="5273a-863">spanish cif no</span></span>
  
<span data-ttu-id="5273a-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-864">tax no</span></span>
  
<span data-ttu-id="5273a-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-865">tax number</span></span>
  
<span data-ttu-id="5273a-866">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-866">taxid#</span></span>
  
<span data-ttu-id="5273a-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="5273a-867">taxno#</span></span>
  
<span data-ttu-id="5273a-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="5273a-868">cifid#</span></span>
  
<span data-ttu-id="5273a-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="5273a-869">spanishcifid#</span></span>
  
<span data-ttu-id="5273a-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="5273a-870">spanishcifno#</span></span>
  
<span data-ttu-id="5273a-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="5273a-871">número de contribuyente</span></span>
  
<span data-ttu-id="5273a-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="5273a-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="5273a-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="5273a-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="5273a-874">cif número</span></span>
  
<span data-ttu-id="5273a-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="5273a-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="5273a-876">Suède</span><span class="sxs-lookup"><span data-stu-id="5273a-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="5273a-877">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-877">Format</span></span>

<span data-ttu-id="5273a-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="5273a-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-879">Pattern</span></span>

<span data-ttu-id="5273a-880">Dix chiffres et un symbole:</span><span class="sxs-lookup"><span data-stu-id="5273a-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="5273a-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="5273a-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="5273a-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="5273a-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="5273a-883">Trois chiffres qui permettent de définir le numéro d'identification unique:</span><span class="sxs-lookup"><span data-stu-id="5273a-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="5273a-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l'étranger.</span><span class="sxs-lookup"><span data-stu-id="5273a-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="5273a-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="5273a-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="5273a-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5273a-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-887">Checksum</span></span>

<span data-ttu-id="5273a-888">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-889">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-889">Definition</span></span>

<span data-ttu-id="5273a-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="5273a-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-895">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="5273a-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-897">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-897">tax id</span></span>
  
<span data-ttu-id="5273a-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-898">tax id no.</span></span>
  
<span data-ttu-id="5273a-899">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-899">tax id number</span></span>
  
<span data-ttu-id="5273a-900">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-900">tax identification</span></span>
  
<span data-ttu-id="5273a-901">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-901">tax identification#</span></span>
  
<span data-ttu-id="5273a-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-902">tax no.</span></span>
  
<span data-ttu-id="5273a-903">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-903">tax#</span></span>
  
<span data-ttu-id="5273a-904">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-904">taxid#</span></span>
  
<span data-ttu-id="5273a-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-905">tax file</span></span>
  
<span data-ttu-id="5273a-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-906">tax file no.</span></span>
  
<span data-ttu-id="5273a-907">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="5273a-907">personal id number</span></span>
  
<span data-ttu-id="5273a-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="5273a-908">skatt id nummer</span></span>
  
<span data-ttu-id="5273a-909">skatt Identifikation</span><span class="sxs-lookup"><span data-stu-id="5273a-909">skatt identifikation</span></span>
  
<span data-ttu-id="5273a-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="5273a-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="5273a-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="5273a-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="5273a-912">Format</span><span class="sxs-lookup"><span data-stu-id="5273a-912">Format</span></span>

<span data-ttu-id="5273a-913">Référence de conTribuable unique (UTR): 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="5273a-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="5273a-914">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="5273a-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="5273a-915">National Insurance Number (NINO)» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5273a-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5273a-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="5273a-916">Pattern</span></span>

<span data-ttu-id="5273a-917">Référence de conTribuable unique (UTR): 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="5273a-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="5273a-918">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="5273a-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="5273a-919">National Insurance Number (NINO)» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5273a-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5273a-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="5273a-920">Checksum</span></span>

<span data-ttu-id="5273a-921">Oui</span><span class="sxs-lookup"><span data-stu-id="5273a-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5273a-922">Définition</span><span class="sxs-lookup"><span data-stu-id="5273a-922">Definition</span></span>

<span data-ttu-id="5273a-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="5273a-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5273a-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="5273a-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5273a-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="5273a-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5273a-926">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="5273a-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="5273a-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="5273a-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="5273a-928">id fiscal</span><span class="sxs-lookup"><span data-stu-id="5273a-928">tax id</span></span>
  
<span data-ttu-id="5273a-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-929">tax id no.</span></span>
  
<span data-ttu-id="5273a-930">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-930">tax id number</span></span>
  
<span data-ttu-id="5273a-931">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-931">tax identification</span></span>
  
<span data-ttu-id="5273a-932">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="5273a-932">tax identification#</span></span>
  
<span data-ttu-id="5273a-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-933">tax no.</span></span>
  
<span data-ttu-id="5273a-934">codes</span><span class="sxs-lookup"><span data-stu-id="5273a-934">tax#</span></span>
  
<span data-ttu-id="5273a-935">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="5273a-935">taxid#</span></span>
  
<span data-ttu-id="5273a-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-936">tax file</span></span>
  
<span data-ttu-id="5273a-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="5273a-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5273a-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5273a-938">See also</span></span>

[<span data-ttu-id="5273a-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="5273a-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

