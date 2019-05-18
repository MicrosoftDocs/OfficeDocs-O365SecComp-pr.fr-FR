---
title: Numéro d’identification fiscale de l’UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles du numéro d’identification fiscale de l’UE. Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152956"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="62feb-104">Numéro d’identification fiscale de l’UE</span><span class="sxs-lookup"><span data-stu-id="62feb-104">EU Tax Identification Number</span></span>

<span data-ttu-id="62feb-105">Cette rubrique montre ce qu’une stratégie de protection contre la perte de données (DLP) recherche lorsqu’il détecte le type d’informations sensibles de l’ID taxe de l’UE (TIN).</span><span class="sxs-lookup"><span data-stu-id="62feb-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="62feb-106">Ce type d’informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="62feb-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="62feb-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="62feb-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="62feb-108">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-108">Format</span></span>

<span data-ttu-id="62feb-109">Neuf chiffres avec un trait d’union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="62feb-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-110">Pattern</span></span>

<span data-ttu-id="62feb-111">Neuf chiffres avec un trait d’Union et une barre oblique facultatifs:</span><span class="sxs-lookup"><span data-stu-id="62feb-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="62feb-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-112">Two digits</span></span> 
    
- <span data-ttu-id="62feb-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="62feb-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="62feb-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-114">Three digits</span></span>
    
- <span data-ttu-id="62feb-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="62feb-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="62feb-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-117">Checksum</span></span>

<span data-ttu-id="62feb-118">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-119">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-119">Definition</span></span>

<span data-ttu-id="62feb-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-125">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="62feb-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-127">tax number</span></span>
  
<span data-ttu-id="62feb-128">number</span><span class="sxs-lookup"><span data-stu-id="62feb-128">number</span></span>
  
<span data-ttu-id="62feb-129">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-129">tax registration number</span></span>
  
<span data-ttu-id="62feb-130">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-130">tax id</span></span>
  
<span data-ttu-id="62feb-131">st.nr.</span><span class="sxs-lookup"><span data-stu-id="62feb-131">st.nr.</span></span>
  
<span data-ttu-id="62feb-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="62feb-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="62feb-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="62feb-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="62feb-134">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-134">Format</span></span>

<span data-ttu-id="62feb-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-136">Pattern</span></span>

<span data-ttu-id="62feb-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="62feb-137">11 digits:</span></span>
  
- <span data-ttu-id="62feb-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-138">Two digits</span></span>
    
- <span data-ttu-id="62feb-139">«0» ou «1»</span><span class="sxs-lookup"><span data-stu-id="62feb-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="62feb-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="62feb-140">One digit</span></span>
    
- <span data-ttu-id="62feb-141">«0» ou «1» ou «2» ou «3»</span><span class="sxs-lookup"><span data-stu-id="62feb-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="62feb-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-143">Checksum</span></span>

<span data-ttu-id="62feb-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-145">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-145">Definition</span></span>

<span data-ttu-id="62feb-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-147">L’expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="62feb-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-151">tax number</span></span>
  
<span data-ttu-id="62feb-152">Numéro d’enregistrement national</span><span class="sxs-lookup"><span data-stu-id="62feb-152">national registration number</span></span>
  
<span data-ttu-id="62feb-153">Numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-153">tax registration number</span></span>
  
<span data-ttu-id="62feb-154">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-154">tax id</span></span>
  
<span data-ttu-id="62feb-155">nPour</span><span class="sxs-lookup"><span data-stu-id="62feb-155">nif</span></span>
  
<span data-ttu-id="62feb-156">nPour</span><span class="sxs-lookup"><span data-stu-id="62feb-156">nif#</span></span>
  
<span data-ttu-id="62feb-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="62feb-157">numéro de registre national</span></span>
  
<span data-ttu-id="62feb-158">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="62feb-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="62feb-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="62feb-160">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-160">Format</span></span>

<span data-ttu-id="62feb-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-162">Pattern</span></span>

<span data-ttu-id="62feb-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-164">Checksum</span></span>

<span data-ttu-id="62feb-165">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-166">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-166">Definition</span></span>

<span data-ttu-id="62feb-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-172">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="62feb-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-174">bucn</span><span class="sxs-lookup"><span data-stu-id="62feb-174">bucn</span></span>
  
<span data-ttu-id="62feb-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="62feb-175">uniform civil number</span></span>
  
<span data-ttu-id="62feb-176">bucn#</span><span class="sxs-lookup"><span data-stu-id="62feb-176">bucn#</span></span>
  
<span data-ttu-id="62feb-177">uniformcivilnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="62feb-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="62feb-178">uniform civil id</span></span>
  
<span data-ttu-id="62feb-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="62feb-179">uniform civil no</span></span>
  
<span data-ttu-id="62feb-180">egn</span><span class="sxs-lookup"><span data-stu-id="62feb-180">egn</span></span>
  
<span data-ttu-id="62feb-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="62feb-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="62feb-182">uniformcivilno#</span><span class="sxs-lookup"><span data-stu-id="62feb-182">uniformcivilno#</span></span>
  
<span data-ttu-id="62feb-183">egn#</span><span class="sxs-lookup"><span data-stu-id="62feb-183">egn#</span></span>
  
<span data-ttu-id="62feb-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="62feb-184">униформ граждански номер</span></span>
  
<span data-ttu-id="62feb-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="62feb-185">униформ id</span></span>
  
<span data-ttu-id="62feb-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="62feb-186">униформ граждански id</span></span>
  
<span data-ttu-id="62feb-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="62feb-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="62feb-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="62feb-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="62feb-189">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-189">Format</span></span>

<span data-ttu-id="62feb-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-191">Pattern</span></span>

<span data-ttu-id="62feb-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="62feb-192">11 digits:</span></span>
  
- <span data-ttu-id="62feb-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="62feb-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="62feb-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-195">Checksum</span></span>

<span data-ttu-id="62feb-196">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-197">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-197">Definition</span></span>

<span data-ttu-id="62feb-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-203">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="62feb-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-205">tax number</span></span>
  
<span data-ttu-id="62feb-206">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-206">tax</span></span>
  
<span data-ttu-id="62feb-207">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-207">tax id</span></span>
  
<span data-ttu-id="62feb-208">oid</span><span class="sxs-lookup"><span data-stu-id="62feb-208">oid</span></span>
  
<span data-ttu-id="62feb-209">OID</span><span class="sxs-lookup"><span data-stu-id="62feb-209">oid#</span></span>
  
<span data-ttu-id="62feb-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="62feb-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="62feb-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="62feb-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="62feb-212">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-212">Format</span></span>

<span data-ttu-id="62feb-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-214">Pattern</span></span>

<span data-ttu-id="62feb-215">Huit chiffres et une lettre:</span><span class="sxs-lookup"><span data-stu-id="62feb-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="62feb-216">«0»</span><span class="sxs-lookup"><span data-stu-id="62feb-216">A "0"</span></span> 
    
- <span data-ttu-id="62feb-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-217">Seven digits</span></span>
    
- <span data-ttu-id="62feb-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-219">Checksum</span></span>

<span data-ttu-id="62feb-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-221">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-221">Definition</span></span>

<span data-ttu-id="62feb-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="62feb-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-229">tax number</span></span>
  
<span data-ttu-id="62feb-230">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-230">tax</span></span>
  
<span data-ttu-id="62feb-231">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-231">tax id</span></span>
  
<span data-ttu-id="62feb-232">code d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-232">tax identification code</span></span>
  
<span data-ttu-id="62feb-233">graduation</span><span class="sxs-lookup"><span data-stu-id="62feb-233">tic</span></span>
  
<span data-ttu-id="62feb-234">graduation</span><span class="sxs-lookup"><span data-stu-id="62feb-234">tic#</span></span>
  
<span data-ttu-id="62feb-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="62feb-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="62feb-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="62feb-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="62feb-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="62feb-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="62feb-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="62feb-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="62feb-239">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-239">Format</span></span>

<span data-ttu-id="62feb-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="62feb-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-241">Pattern</span></span>

<span data-ttu-id="62feb-242">Neuf ou dix chiffres avec une barre oblique inverse facultative:</span><span class="sxs-lookup"><span data-stu-id="62feb-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="62feb-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-243">Six digits</span></span> 
    
- <span data-ttu-id="62feb-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="62feb-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="62feb-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-246">Checksum</span></span>

<span data-ttu-id="62feb-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-248">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-248">Definition</span></span>

<span data-ttu-id="62feb-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-250">L’expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="62feb-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-254">tax number</span></span>
  
<span data-ttu-id="62feb-255">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-255">tax</span></span>
  
<span data-ttu-id="62feb-256">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-256">tax id</span></span>
  
<span data-ttu-id="62feb-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-257">personal number</span></span>
  
<span data-ttu-id="62feb-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="62feb-258">daňové číslo</span></span>
  
<span data-ttu-id="62feb-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="62feb-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="62feb-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="62feb-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="62feb-261">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-261">Format</span></span>

<span data-ttu-id="62feb-262">Dix chiffres contenant un trait d’Union</span><span class="sxs-lookup"><span data-stu-id="62feb-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-263">Pattern</span></span>

<span data-ttu-id="62feb-264">Dix chiffres contenant un trait d’Union:</span><span class="sxs-lookup"><span data-stu-id="62feb-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="62feb-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="62feb-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="62feb-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="62feb-266">A hyphen</span></span>
    
- <span data-ttu-id="62feb-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l’individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="62feb-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-268">Checksum</span></span>

<span data-ttu-id="62feb-269">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-270">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-270">Definition</span></span>

<span data-ttu-id="62feb-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-276">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="62feb-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-278">tax number</span></span>
  
<span data-ttu-id="62feb-279">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-279">tax</span></span>
  
<span data-ttu-id="62feb-280">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-280">tax id</span></span>
  
<span data-ttu-id="62feb-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="62feb-281">cpr number</span></span>
  
<span data-ttu-id="62feb-282">cardio</span><span class="sxs-lookup"><span data-stu-id="62feb-282">cpr#</span></span>
  
<span data-ttu-id="62feb-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="62feb-283">skat nummer</span></span>
  
<span data-ttu-id="62feb-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="62feb-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="62feb-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="62feb-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="62feb-286">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-286">Format</span></span>

<span data-ttu-id="62feb-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-288">Pattern</span></span>

<span data-ttu-id="62feb-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="62feb-289">11 digits:</span></span>
  
-  <span data-ttu-id="62feb-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit: 1,2 pour le 19 siècle; 3, 4 pour le vingtième siècle; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="62feb-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="62feb-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="62feb-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="62feb-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="62feb-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="62feb-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-294">Checksum</span></span>

<span data-ttu-id="62feb-295">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-296">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-296">Definition</span></span>

<span data-ttu-id="62feb-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-302">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="62feb-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-304">tax number</span></span>
  
<span data-ttu-id="62feb-305">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-305">tax</span></span>
  
<span data-ttu-id="62feb-306">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-306">tax id</span></span>
  
<span data-ttu-id="62feb-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-307">personal code</span></span>
  
<span data-ttu-id="62feb-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="62feb-308">maksunumber</span></span>
  
<span data-ttu-id="62feb-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="62feb-309">maksu id</span></span>
  
<span data-ttu-id="62feb-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="62feb-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="62feb-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="62feb-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="62feb-312">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-312">Format</span></span>

<span data-ttu-id="62feb-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="62feb-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-314">Pattern</span></span>

<span data-ttu-id="62feb-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins:</span><span class="sxs-lookup"><span data-stu-id="62feb-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="62feb-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-316">Six digits</span></span>
    
- <span data-ttu-id="62feb-317">L’une des options suivantes: un signe plus, un signe moins ou la lettre «A» (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et «A» désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="62feb-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="62feb-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-318">Three digits</span></span>
    
- <span data-ttu-id="62feb-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="62feb-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-320">Checksum</span></span>

<span data-ttu-id="62feb-321">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-322">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-322">Definition</span></span>

<span data-ttu-id="62feb-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-328">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="62feb-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-330">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="62feb-330">identification number</span></span>
  
<span data-ttu-id="62feb-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-331">personal id</span></span>
  
<span data-ttu-id="62feb-332">Numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="62feb-332">identity number</span></span>
  
<span data-ttu-id="62feb-333">Numéro d’identification national finnois</span><span class="sxs-lookup"><span data-stu-id="62feb-333">finnish national id number</span></span>
  
<span data-ttu-id="62feb-334">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-334">personalidnumber#</span></span>
  
<span data-ttu-id="62feb-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="62feb-335">national identification number</span></span>
  
<span data-ttu-id="62feb-336">Numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="62feb-336">id number</span></span>
  
<span data-ttu-id="62feb-337">Numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="62feb-337">national id no.</span></span>
  
<span data-ttu-id="62feb-338">Numéro d’identification national</span><span class="sxs-lookup"><span data-stu-id="62feb-338">national id number</span></span>
  
<span data-ttu-id="62feb-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="62feb-339">id no</span></span>
  
<span data-ttu-id="62feb-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="62feb-340">tunnistenumero</span></span>
  
<span data-ttu-id="62feb-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="62feb-341">henkilötunnus</span></span>
  
<span data-ttu-id="62feb-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="62feb-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="62feb-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="62feb-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="62feb-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="62feb-344">identiteetti numero</span></span>
  
<span data-ttu-id="62feb-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="62feb-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="62feb-346">henkilötunnusnumero#</span><span class="sxs-lookup"><span data-stu-id="62feb-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="62feb-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="62feb-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="62feb-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="62feb-348">tunnusnumero</span></span>
  
<span data-ttu-id="62feb-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="62feb-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="62feb-350">France</span><span class="sxs-lookup"><span data-stu-id="62feb-350">France</span></span>

### <a name="format"></a><span data-ttu-id="62feb-351">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-351">Format</span></span>

<span data-ttu-id="62feb-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="62feb-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-353">Pattern</span></span>

<span data-ttu-id="62feb-354">13 chiffres pour les personnes:</span><span class="sxs-lookup"><span data-stu-id="62feb-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="62feb-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="62feb-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="62feb-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-356">12 digits</span></span>
    
<span data-ttu-id="62feb-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="62feb-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-358">Checksum</span></span>

<span data-ttu-id="62feb-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-360">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-360">Definition</span></span>

<span data-ttu-id="62feb-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="62feb-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-368">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-368">tax identification number</span></span>
  
<span data-ttu-id="62feb-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-369">tax number</span></span>
  
<span data-ttu-id="62feb-370">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-370">tax id</span></span>
  
<span data-ttu-id="62feb-371">Numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="62feb-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="62feb-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="62feb-373">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-373">Format</span></span>

<span data-ttu-id="62feb-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-375">Pattern</span></span>

<span data-ttu-id="62feb-376">11 chiffres:</span><span class="sxs-lookup"><span data-stu-id="62feb-376">11 digits :</span></span>
  
-  <span data-ttu-id="62feb-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-377">Ten digits</span></span> 
    
- <span data-ttu-id="62feb-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-379">Checksum</span></span>

<span data-ttu-id="62feb-380">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-381">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-381">Definition</span></span>

<span data-ttu-id="62feb-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="62feb-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-389">tax number</span></span>
  
<span data-ttu-id="62feb-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-390">tax no.</span></span>
  
<span data-ttu-id="62feb-391">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-391">taxno#</span></span>
  
<span data-ttu-id="62feb-392">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-392">taxnumber#</span></span>
  
<span data-ttu-id="62feb-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-393">taxnumber</span></span>
  
<span data-ttu-id="62feb-394">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-394">tax id</span></span>
  
<span data-ttu-id="62feb-395">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-395">taxid#</span></span>
  
<span data-ttu-id="62feb-396">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-396">tax identification number</span></span>
  
<span data-ttu-id="62feb-397">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-397">tax identification no.</span></span>
  
<span data-ttu-id="62feb-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="62feb-398">steuernummer</span></span>
  
<span data-ttu-id="62feb-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="62feb-399">steuer id</span></span>
  
<span data-ttu-id="62feb-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62feb-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="62feb-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="62feb-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="62feb-402">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-402">Format</span></span>

<span data-ttu-id="62feb-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-404">Pattern</span></span>

<span data-ttu-id="62feb-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-406">Checksum</span></span>

<span data-ttu-id="62feb-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-408">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-408">Definition</span></span>

<span data-ttu-id="62feb-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-410">L’expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-412">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="62feb-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-414">financement</span><span class="sxs-lookup"><span data-stu-id="62feb-414">afm</span></span>
  
<span data-ttu-id="62feb-415">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-415">tin</span></span>
  
<span data-ttu-id="62feb-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-416">tax id no.</span></span>
  
<span data-ttu-id="62feb-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-417">tax id no</span></span>
  
<span data-ttu-id="62feb-418">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-418">tax identification number</span></span>
  
<span data-ttu-id="62feb-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="62feb-419">tax registry number</span></span>
  
<span data-ttu-id="62feb-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-420">tax registry no.</span></span>
  
<span data-ttu-id="62feb-421">financement</span><span class="sxs-lookup"><span data-stu-id="62feb-421">afm#</span></span>
  
<span data-ttu-id="62feb-422">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-422">tin#</span></span>
  
<span data-ttu-id="62feb-423">taxidno#</span><span class="sxs-lookup"><span data-stu-id="62feb-423">taxidno#</span></span>
  
<span data-ttu-id="62feb-424">taxregistryno#</span><span class="sxs-lookup"><span data-stu-id="62feb-424">taxregistryno#</span></span>
  
<span data-ttu-id="62feb-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="62feb-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="62feb-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="62feb-426">aφμ</span></span>
  
<span data-ttu-id="62feb-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="62feb-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="62feb-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="62feb-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="62feb-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="62feb-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="62feb-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="62feb-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="62feb-431">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-431">Format</span></span>

<span data-ttu-id="62feb-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-433">Pattern</span></span>

<span data-ttu-id="62feb-434">Dix chiffres:</span><span class="sxs-lookup"><span data-stu-id="62feb-434">Ten digits:</span></span>
  
-  <span data-ttu-id="62feb-435">Un chiffre qui doit être «8»</span><span class="sxs-lookup"><span data-stu-id="62feb-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="62feb-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="62feb-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="62feb-437">Trois chiffres correspondant au nombre généré par l’opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="62feb-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="62feb-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-439">Checksum</span></span>

<span data-ttu-id="62feb-440">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-441">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-441">Definition</span></span>

<span data-ttu-id="62feb-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-447">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="62feb-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-449">Numéro d’identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="62feb-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="62feb-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="62feb-450">hungarian tin</span></span>
  
<span data-ttu-id="62feb-451">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-451">tax id number</span></span>
  
<span data-ttu-id="62feb-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="62feb-452">vat number</span></span>
  
<span data-ttu-id="62feb-453">Numéro de l’autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-453">tax authority no</span></span>
  
<span data-ttu-id="62feb-454">Numéro d’identité fiscale de l’ID taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-454">tax id tax identity number</span></span>
  
<span data-ttu-id="62feb-455">taxidnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-455">taxidnumber#</span></span>
  
<span data-ttu-id="62feb-456">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-456">tin#</span></span>
  
<span data-ttu-id="62feb-457">hungatiantin#</span><span class="sxs-lookup"><span data-stu-id="62feb-457">hungatiantin#</span></span>
  
<span data-ttu-id="62feb-458">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-458">tax identification no</span></span>
  
<span data-ttu-id="62feb-459">taxidno#</span><span class="sxs-lookup"><span data-stu-id="62feb-459">taxidno#</span></span>
  
<span data-ttu-id="62feb-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="62feb-460">adóazonosító szám</span></span>
  
<span data-ttu-id="62feb-461">adószám</span><span class="sxs-lookup"><span data-stu-id="62feb-461">adószám</span></span>
  
<span data-ttu-id="62feb-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="62feb-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="62feb-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="62feb-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="62feb-464">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-464">Format</span></span>

<span data-ttu-id="62feb-465">Sept chiffres suivis d’une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-466">Pattern</span></span>

<span data-ttu-id="62feb-467">Sept chiffres suivis d’une lettre:</span><span class="sxs-lookup"><span data-stu-id="62feb-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="62feb-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-468">Seven digits</span></span> 
    
- <span data-ttu-id="62feb-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-470">Checksum</span></span>

<span data-ttu-id="62feb-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-472">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-472">Definition</span></span>

<span data-ttu-id="62feb-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="62feb-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="62feb-480">public service no</span></span>
  
<span data-ttu-id="62feb-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-481">personal public service no</span></span>
  
<span data-ttu-id="62feb-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="62feb-482">pps no</span></span>
  
<span data-ttu-id="62feb-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-483">personal service no</span></span>
  
<span data-ttu-id="62feb-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="62feb-484">pps service no</span></span>
  
<span data-ttu-id="62feb-485">ppsno#</span><span class="sxs-lookup"><span data-stu-id="62feb-485">ppsno#</span></span>
  
<span data-ttu-id="62feb-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="62feb-486">irish pps no</span></span>
  
<span data-ttu-id="62feb-487">publicserviceno#</span><span class="sxs-lookup"><span data-stu-id="62feb-487">publicserviceno#</span></span>
  
<span data-ttu-id="62feb-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="62feb-488">personal public service number</span></span>
  
<span data-ttu-id="62feb-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="62feb-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="62feb-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="62feb-490">pps uimh</span></span>
  
<span data-ttu-id="62feb-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="62feb-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="62feb-492">Italie</span><span class="sxs-lookup"><span data-stu-id="62feb-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="62feb-493">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-493">Format</span></span>

<span data-ttu-id="62feb-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-495">Pattern</span></span>

<span data-ttu-id="62feb-496">16 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="62feb-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="62feb-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="62feb-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="62feb-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="62feb-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="62feb-499">Deux chiffres correspondant aux derniers chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="62feb-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="62feb-500">Un chiffre correspondant au mois de naissance: les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="62feb-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="62feb-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="62feb-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="62feb-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="62feb-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="62feb-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-504">Checksum</span></span>

<span data-ttu-id="62feb-505">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-506">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-506">Definition</span></span>

<span data-ttu-id="62feb-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-512">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="62feb-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-514">tax number</span></span>
  
<span data-ttu-id="62feb-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-515">tax no.</span></span>
  
<span data-ttu-id="62feb-516">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-516">taxno#</span></span>
  
<span data-ttu-id="62feb-517">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-517">taxnumber#</span></span>
  
<span data-ttu-id="62feb-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-518">taxnumber</span></span>
  
<span data-ttu-id="62feb-519">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-519">tax id</span></span>
  
<span data-ttu-id="62feb-520">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-520">taxid#</span></span>
  
<span data-ttu-id="62feb-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-521">fiscal code</span></span>
  
<span data-ttu-id="62feb-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="62feb-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="62feb-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="62feb-524">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-524">Format</span></span>

<span data-ttu-id="62feb-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-526">Pattern</span></span>

<span data-ttu-id="62feb-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="62feb-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="62feb-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="62feb-529">Un chiffre correspondant au siècle de naissance où «0» correspond à 19 siècle, «1» correspond au vingtième siècle et «2» au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="62feb-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="62feb-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-531">Checksum</span></span>

<span data-ttu-id="62feb-532">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-533">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-533">Definition</span></span>

<span data-ttu-id="62feb-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-539">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="62feb-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-541">tax number</span></span>
  
<span data-ttu-id="62feb-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-542">tax no.</span></span>
  
<span data-ttu-id="62feb-543">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-543">taxno#</span></span>
  
<span data-ttu-id="62feb-544">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-544">taxnumber#</span></span>
  
<span data-ttu-id="62feb-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-545">taxnumber</span></span>
  
<span data-ttu-id="62feb-546">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-546">tax id</span></span>
  
<span data-ttu-id="62feb-547">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-547">taxid#</span></span>
  
<span data-ttu-id="62feb-548">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-548">tax identification number</span></span>
  
<span data-ttu-id="62feb-549">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-549">tax identification no.</span></span>
  
<span data-ttu-id="62feb-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="62feb-550">nodokļa numurs</span></span>
  
<span data-ttu-id="62feb-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="62feb-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="62feb-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="62feb-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="62feb-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="62feb-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="62feb-554">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-554">Format</span></span>

<span data-ttu-id="62feb-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-556">Pattern</span></span>

<span data-ttu-id="62feb-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-558">Checksum</span></span>

<span data-ttu-id="62feb-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-560">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-560">Definition</span></span>

<span data-ttu-id="62feb-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="62feb-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-568">tax number</span></span>
  
<span data-ttu-id="62feb-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-569">tax no.</span></span>
  
<span data-ttu-id="62feb-570">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="62feb-570">tax no#</span></span>
  
<span data-ttu-id="62feb-571">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-571">taxnumber#</span></span>
  
<span data-ttu-id="62feb-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-572">taxnumber</span></span>
  
<span data-ttu-id="62feb-573">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-573">tax id</span></span>
  
<span data-ttu-id="62feb-574">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-574">taxid#</span></span>
  
<span data-ttu-id="62feb-575">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-575">tax identification number</span></span>
  
<span data-ttu-id="62feb-576">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-576">tax identification no.</span></span>
  
<span data-ttu-id="62feb-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="62feb-577">mokesčių id</span></span>
  
<span data-ttu-id="62feb-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-578">mokesčių numeris</span></span>
  
<span data-ttu-id="62feb-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="62feb-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="62feb-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="62feb-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="62feb-581">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-581">Format</span></span>

<span data-ttu-id="62feb-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-583">Pattern</span></span>

<span data-ttu-id="62feb-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="62feb-584">13 digits:</span></span>
  
-  <span data-ttu-id="62feb-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-585">11 digits</span></span> 
    
- <span data-ttu-id="62feb-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-587">Checksum</span></span>

<span data-ttu-id="62feb-588">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-589">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-589">Definition</span></span>

<span data-ttu-id="62feb-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-595">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="62feb-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-597">tax number</span></span>
  
<span data-ttu-id="62feb-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-598">tax no.</span></span>
  
<span data-ttu-id="62feb-599">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-599">taxno#</span></span>
  
<span data-ttu-id="62feb-600">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-600">taxnumber#</span></span>
  
<span data-ttu-id="62feb-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-601">taxnumber</span></span>
  
<span data-ttu-id="62feb-602">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-602">tax id</span></span>
  
<span data-ttu-id="62feb-603">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-603">taxid#</span></span>
  
<span data-ttu-id="62feb-604">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-604">tax identification number</span></span>
  
<span data-ttu-id="62feb-605">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-605">tax identification no.</span></span>
  
<span data-ttu-id="62feb-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="62feb-606">steuernummer</span></span>
  
<span data-ttu-id="62feb-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="62feb-607">steuer id</span></span>
  
<span data-ttu-id="62feb-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62feb-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="62feb-609">Malte</span><span class="sxs-lookup"><span data-stu-id="62feb-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="62feb-610">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-610">Format</span></span>

<span data-ttu-id="62feb-611">Pour les ressortissants maltais: 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="62feb-612">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-613">Pattern</span></span>

<span data-ttu-id="62feb-614">Ressortissants maltaises: 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="62feb-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="62feb-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-615">Seven digits</span></span> 
    
- <span data-ttu-id="62feb-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="62feb-617">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="62feb-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="62feb-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-619">Checksum</span></span>

<span data-ttu-id="62feb-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-621">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-621">Definition</span></span>

<span data-ttu-id="62feb-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-627">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="62feb-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-629">tax number</span></span>
  
<span data-ttu-id="62feb-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-630">tax no.</span></span>
  
<span data-ttu-id="62feb-631">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-631">taxno#</span></span>
  
<span data-ttu-id="62feb-632">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-632">taxnumber#</span></span>
  
<span data-ttu-id="62feb-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-633">taxnumber</span></span>
  
<span data-ttu-id="62feb-634">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-634">tax id</span></span>
  
<span data-ttu-id="62feb-635">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-635">taxid#</span></span>
  
<span data-ttu-id="62feb-636">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-636">tax identification number</span></span>
  
<span data-ttu-id="62feb-637">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-637">tax identification no.</span></span>
  
<span data-ttu-id="62feb-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="62feb-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="62feb-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="62feb-639">id tat-taxxa</span></span>
  
<span data-ttu-id="62feb-640">numru ta’IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="62feb-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="62feb-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="62feb-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="62feb-642">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-642">Format</span></span>

<span data-ttu-id="62feb-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-644">Pattern</span></span>

<span data-ttu-id="62feb-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="62feb-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-646">Checksum</span></span>

<span data-ttu-id="62feb-647">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-648">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-648">Definition</span></span>

<span data-ttu-id="62feb-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-654">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="62feb-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-656">Numéro d’identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="62feb-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="62feb-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="62feb-657">netherlands tax identification</span></span>
  
<span data-ttu-id="62feb-658">Numéro d’identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="62feb-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="62feb-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="62feb-659">netherland's tax identification</span></span>
  
<span data-ttu-id="62feb-660">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-660">tax identification number</span></span>
  
<span data-ttu-id="62feb-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="62feb-661">dutch tax id</span></span>
  
<span data-ttu-id="62feb-662">Numéro d’identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="62feb-662">dutch tax identification number</span></span>
  
<span data-ttu-id="62feb-663">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-663">tax id</span></span>
  
<span data-ttu-id="62feb-664">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-664">tax id#</span></span>
  
<span data-ttu-id="62feb-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-665">tax number</span></span>
  
<span data-ttu-id="62feb-666">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="62feb-666">tax no#</span></span>
  
<span data-ttu-id="62feb-667">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-667">tax#</span></span>
  
<span data-ttu-id="62feb-668">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-668">tin</span></span>
  
<span data-ttu-id="62feb-669">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-669">tin#</span></span>
  
<span data-ttu-id="62feb-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="62feb-670">netherlands tin</span></span>
  
<span data-ttu-id="62feb-671">Netherland d’étain</span><span class="sxs-lookup"><span data-stu-id="62feb-671">netherland's tin</span></span>
  
<span data-ttu-id="62feb-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="62feb-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="62feb-673">identificatienummer van à l’avant-dernière</span><span class="sxs-lookup"><span data-stu-id="62feb-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="62feb-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="62feb-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="62feb-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="62feb-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="62feb-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="62feb-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="62feb-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="62feb-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="62feb-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="62feb-678">btw nummer</span></span>
  
<span data-ttu-id="62feb-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="62feb-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="62feb-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="62feb-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="62feb-681">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-681">Format</span></span>

<span data-ttu-id="62feb-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-683">Pattern</span></span>

<span data-ttu-id="62feb-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-685">Checksum</span></span>

<span data-ttu-id="62feb-686">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-687">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-687">Definition</span></span>

<span data-ttu-id="62feb-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-693">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="62feb-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-695">tax number</span></span>
  
<span data-ttu-id="62feb-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-696">tax no.</span></span>
  
<span data-ttu-id="62feb-697">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-697">taxno#</span></span>
  
<span data-ttu-id="62feb-698">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-698">taxnumber#</span></span>
  
<span data-ttu-id="62feb-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-699">taxnumber</span></span>
  
<span data-ttu-id="62feb-700">pince</span><span class="sxs-lookup"><span data-stu-id="62feb-700">nip</span></span>
  
<span data-ttu-id="62feb-701">pince</span><span class="sxs-lookup"><span data-stu-id="62feb-701">nip#</span></span>
  
<span data-ttu-id="62feb-702">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-702">tax id</span></span>
  
<span data-ttu-id="62feb-703">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-703">tax id#</span></span>
  
<span data-ttu-id="62feb-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="62feb-704">nip id</span></span>
  
<span data-ttu-id="62feb-705">n ° de NIP</span><span class="sxs-lookup"><span data-stu-id="62feb-705">nip id#</span></span>
  
<span data-ttu-id="62feb-706">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-706">tax identification number</span></span>
  
<span data-ttu-id="62feb-707">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-707">tax identification no.</span></span>
  
<span data-ttu-id="62feb-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="62feb-708">vat number</span></span>
  
<span data-ttu-id="62feb-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="62feb-709">vat no.</span></span>
  
<span data-ttu-id="62feb-710">vatno#</span><span class="sxs-lookup"><span data-stu-id="62feb-710">vatno#</span></span>
  
<span data-ttu-id="62feb-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="62feb-711">vat id</span></span>
  
<span data-ttu-id="62feb-712">n ° de TVA</span><span class="sxs-lookup"><span data-stu-id="62feb-712">vat id#</span></span>
  
<span data-ttu-id="62feb-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="62feb-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="62feb-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="62feb-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="62feb-715">numeridentyfikacjipodatkowej#</span><span class="sxs-lookup"><span data-stu-id="62feb-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="62feb-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="62feb-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="62feb-717">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-717">Format</span></span>

<span data-ttu-id="62feb-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-719">Pattern</span></span>

<span data-ttu-id="62feb-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-721">Checksum</span></span>

<span data-ttu-id="62feb-722">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-723">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-723">Definition</span></span>

<span data-ttu-id="62feb-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-729">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="62feb-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-731">tax number</span></span>
  
<span data-ttu-id="62feb-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-732">tax no.</span></span>
  
<span data-ttu-id="62feb-733">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-733">taxno#</span></span>
  
<span data-ttu-id="62feb-734">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="62feb-734">taxnumber#</span></span>
  
<span data-ttu-id="62feb-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="62feb-735">taxnumber</span></span>
  
<span data-ttu-id="62feb-736">nPour</span><span class="sxs-lookup"><span data-stu-id="62feb-736">nif</span></span>
  
<span data-ttu-id="62feb-737">nPour</span><span class="sxs-lookup"><span data-stu-id="62feb-737">nif#</span></span>
  
<span data-ttu-id="62feb-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="62feb-738">numero fiscal</span></span>
  
<span data-ttu-id="62feb-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="62feb-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="62feb-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="62feb-741">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-741">Format</span></span>

<span data-ttu-id="62feb-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-743">Pattern</span></span>

<span data-ttu-id="62feb-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-745">Checksum</span></span>

<span data-ttu-id="62feb-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-747">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-747">Definition</span></span>

<span data-ttu-id="62feb-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-749">L’expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-751">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="62feb-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-753">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-753">tax id</span></span>
  
<span data-ttu-id="62feb-754">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-754">tax id number</span></span>
  
<span data-ttu-id="62feb-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-755">tax file no</span></span>
  
<span data-ttu-id="62feb-756">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-756">tax file number</span></span>
  
<span data-ttu-id="62feb-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-757">tax no</span></span>
  
<span data-ttu-id="62feb-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-758">tax number</span></span>
  
<span data-ttu-id="62feb-759">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-759">taxid#</span></span>
  
<span data-ttu-id="62feb-760">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-760">taxno#</span></span>
  
<span data-ttu-id="62feb-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="62feb-761">id-ul taxei</span></span>
  
<span data-ttu-id="62feb-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="62feb-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="62feb-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="62feb-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="62feb-764">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-764">Format</span></span>

<span data-ttu-id="62feb-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-766">Pattern</span></span>

<span data-ttu-id="62feb-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-768">Checksum</span></span>

<span data-ttu-id="62feb-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="62feb-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-770">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-770">Definition</span></span>

<span data-ttu-id="62feb-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-772">L’expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-774">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="62feb-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-776">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-776">tax id</span></span>
  
<span data-ttu-id="62feb-777">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-777">tax id number</span></span>
  
<span data-ttu-id="62feb-778">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="62feb-778">tin id</span></span>
  
<span data-ttu-id="62feb-779">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="62feb-779">tin no</span></span>
  
<span data-ttu-id="62feb-780">ID d’étain slovaque</span><span class="sxs-lookup"><span data-stu-id="62feb-780">slovakian tin id</span></span>
  
<span data-ttu-id="62feb-781">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-781">tin</span></span>
  
<span data-ttu-id="62feb-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-782">tax file no</span></span>
  
<span data-ttu-id="62feb-783">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-783">tax file number</span></span>
  
<span data-ttu-id="62feb-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-784">tax no</span></span>
  
<span data-ttu-id="62feb-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-785">tax number</span></span>
  
<span data-ttu-id="62feb-786">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-786">taxid#</span></span>
  
<span data-ttu-id="62feb-787">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-787">taxno#</span></span>
  
<span data-ttu-id="62feb-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="62feb-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="62feb-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="62feb-789">daňové číslo</span></span>
  
<span data-ttu-id="62feb-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="62feb-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="62feb-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="62feb-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="62feb-792">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-792">Format</span></span>

<span data-ttu-id="62feb-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-794">Pattern</span></span>

<span data-ttu-id="62feb-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-796">Checksum</span></span>

<span data-ttu-id="62feb-797">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-798">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-798">Definition</span></span>

<span data-ttu-id="62feb-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-804">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="62feb-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-806">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-806">tax id</span></span>
  
<span data-ttu-id="62feb-807">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-807">tax id number</span></span>
  
<span data-ttu-id="62feb-808">ID d’étain</span><span class="sxs-lookup"><span data-stu-id="62feb-808">tin id</span></span>
  
<span data-ttu-id="62feb-809">n ° d’étain</span><span class="sxs-lookup"><span data-stu-id="62feb-809">tin no</span></span>
  
<span data-ttu-id="62feb-810">ID d’étain slovène</span><span class="sxs-lookup"><span data-stu-id="62feb-810">slovenian tin id</span></span>
  
<span data-ttu-id="62feb-811">Etain</span><span class="sxs-lookup"><span data-stu-id="62feb-811">tin</span></span>
  
<span data-ttu-id="62feb-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-812">tax file no</span></span>
  
<span data-ttu-id="62feb-813">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-813">tax file number</span></span>
  
<span data-ttu-id="62feb-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-814">tax no</span></span>
  
<span data-ttu-id="62feb-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-815">tax number</span></span>
  
<span data-ttu-id="62feb-816">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-816">taxid#</span></span>
  
<span data-ttu-id="62feb-817">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-817">taxno#</span></span>
  
<span data-ttu-id="62feb-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="62feb-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="62feb-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="62feb-819">davčna številka</span></span>
  
<span data-ttu-id="62feb-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="62feb-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="62feb-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="62feb-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="62feb-822">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-822">Format</span></span>

<span data-ttu-id="62feb-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-824">Pattern</span></span>

<span data-ttu-id="62feb-825">Personnes physiques espagnoles avec une carte d’identité nationale d’Espagne:</span><span class="sxs-lookup"><span data-stu-id="62feb-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="62feb-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-826">Eight digits</span></span> 
    
- <span data-ttu-id="62feb-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="62feb-828">Spaniards non résident sans carte d’identité nationale d’Espagne</span><span class="sxs-lookup"><span data-stu-id="62feb-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="62feb-829">Une lettre majuscule «L» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="62feb-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-830">Seven digits</span></span>
    
- <span data-ttu-id="62feb-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="62feb-832">Spaniards résident de moins de 14 ans sans carte d’identité nationale (Espagne):</span><span class="sxs-lookup"><span data-stu-id="62feb-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="62feb-833">Une lettre majuscule «K» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="62feb-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-834">Seven digits</span></span> 
    
- <span data-ttu-id="62feb-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="62feb-836">Foreigners avec le numéro d’identification d’un étranger</span><span class="sxs-lookup"><span data-stu-id="62feb-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="62feb-837">Une lettre majuscule qui est «X», «Y» ou «Z» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="62feb-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-838">Seven digits</span></span>
    
- <span data-ttu-id="62feb-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="62feb-840">Foreigners sans numéro d’identification étranger</span><span class="sxs-lookup"><span data-stu-id="62feb-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="62feb-841">Une lettre majuscule qui est «M» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="62feb-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="62feb-842">Seven digits</span></span>
    
- <span data-ttu-id="62feb-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="62feb-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="62feb-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-844">Checksum</span></span>

<span data-ttu-id="62feb-845">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-846">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-846">Definition</span></span>

<span data-ttu-id="62feb-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-852">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="62feb-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-854">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-854">tax id</span></span>
  
<span data-ttu-id="62feb-855">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-855">tax id number</span></span>
  
<span data-ttu-id="62feb-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="62feb-856">cif id</span></span>
  
<span data-ttu-id="62feb-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="62feb-857">cif no</span></span>
  
<span data-ttu-id="62feb-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="62feb-858">spanish cif id</span></span>
  
<span data-ttu-id="62feb-859">importation</span><span class="sxs-lookup"><span data-stu-id="62feb-859">cif</span></span>
  
<span data-ttu-id="62feb-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-860">tax file no</span></span>
  
<span data-ttu-id="62feb-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="62feb-861">spanish cif number</span></span>
  
<span data-ttu-id="62feb-862">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-862">tax file number</span></span>
  
<span data-ttu-id="62feb-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="62feb-863">spanish cif no</span></span>
  
<span data-ttu-id="62feb-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-864">tax no</span></span>
  
<span data-ttu-id="62feb-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-865">tax number</span></span>
  
<span data-ttu-id="62feb-866">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-866">taxid#</span></span>
  
<span data-ttu-id="62feb-867">taxno#</span><span class="sxs-lookup"><span data-stu-id="62feb-867">taxno#</span></span>
  
<span data-ttu-id="62feb-868">cifid#</span><span class="sxs-lookup"><span data-stu-id="62feb-868">cifid#</span></span>
  
<span data-ttu-id="62feb-869">spanishcifid#</span><span class="sxs-lookup"><span data-stu-id="62feb-869">spanishcifid#</span></span>
  
<span data-ttu-id="62feb-870">spanishcifno#</span><span class="sxs-lookup"><span data-stu-id="62feb-870">spanishcifno#</span></span>
  
<span data-ttu-id="62feb-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="62feb-871">número de contribuyente</span></span>
  
<span data-ttu-id="62feb-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="62feb-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="62feb-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="62feb-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="62feb-874">cif número</span></span>
  
<span data-ttu-id="62feb-875">cifnúmero#</span><span class="sxs-lookup"><span data-stu-id="62feb-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="62feb-876">Suède</span><span class="sxs-lookup"><span data-stu-id="62feb-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="62feb-877">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-877">Format</span></span>

<span data-ttu-id="62feb-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="62feb-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-879">Pattern</span></span>

<span data-ttu-id="62feb-880">Dix chiffres et un symbole:</span><span class="sxs-lookup"><span data-stu-id="62feb-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="62feb-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="62feb-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="62feb-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="62feb-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="62feb-883">Trois chiffres qui permettent de définir le numéro d’identification unique:</span><span class="sxs-lookup"><span data-stu-id="62feb-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="62feb-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l’étranger.</span><span class="sxs-lookup"><span data-stu-id="62feb-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="62feb-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="62feb-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="62feb-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="62feb-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-887">Checksum</span></span>

<span data-ttu-id="62feb-888">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-889">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-889">Definition</span></span>

<span data-ttu-id="62feb-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="62feb-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="62feb-895">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="62feb-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-897">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-897">tax id</span></span>
  
<span data-ttu-id="62feb-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-898">tax id no.</span></span>
  
<span data-ttu-id="62feb-899">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-899">tax id number</span></span>
  
<span data-ttu-id="62feb-900">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-900">tax identification</span></span>
  
<span data-ttu-id="62feb-901">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-901">tax identification#</span></span>
  
<span data-ttu-id="62feb-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-902">tax no.</span></span>
  
<span data-ttu-id="62feb-903">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-903">tax#</span></span>
  
<span data-ttu-id="62feb-904">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-904">taxid#</span></span>
  
<span data-ttu-id="62feb-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-905">tax file</span></span>
  
<span data-ttu-id="62feb-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-906">tax file no.</span></span>
  
<span data-ttu-id="62feb-907">Numéro d’identification personnel</span><span class="sxs-lookup"><span data-stu-id="62feb-907">personal id number</span></span>
  
<span data-ttu-id="62feb-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="62feb-908">skatt id nummer</span></span>
  
<span data-ttu-id="62feb-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="62feb-909">skatt identifikation</span></span>
  
<span data-ttu-id="62feb-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="62feb-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="62feb-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="62feb-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="62feb-912">Format</span><span class="sxs-lookup"><span data-stu-id="62feb-912">Format</span></span>

<span data-ttu-id="62feb-913">Référence de contribuable unique (UTR): 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="62feb-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="62feb-914">Numéro d’assurance nationale (NINO): pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="62feb-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="62feb-915">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="62feb-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="62feb-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="62feb-916">Pattern</span></span>

<span data-ttu-id="62feb-917">Référence de contribuable unique (UTR): 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="62feb-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="62feb-918">Numéro d’assurance nationale (NINO): pour plus d’informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="62feb-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="62feb-919">National Insurance Number (NINO)» dans [ce que recherche les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="62feb-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="62feb-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="62feb-920">Checksum</span></span>

<span data-ttu-id="62feb-921">Oui</span><span class="sxs-lookup"><span data-stu-id="62feb-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="62feb-922">Définition</span><span class="sxs-lookup"><span data-stu-id="62feb-922">Definition</span></span>

<span data-ttu-id="62feb-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="62feb-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="62feb-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="62feb-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="62feb-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="62feb-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62feb-926">Mots clés</span><span class="sxs-lookup"><span data-stu-id="62feb-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="62feb-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="62feb-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="62feb-928">id fiscal</span><span class="sxs-lookup"><span data-stu-id="62feb-928">tax id</span></span>
  
<span data-ttu-id="62feb-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-929">tax id no.</span></span>
  
<span data-ttu-id="62feb-930">Numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-930">tax id number</span></span>
  
<span data-ttu-id="62feb-931">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-931">tax identification</span></span>
  
<span data-ttu-id="62feb-932">n ° d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="62feb-932">tax identification#</span></span>
  
<span data-ttu-id="62feb-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-933">tax no.</span></span>
  
<span data-ttu-id="62feb-934">codes</span><span class="sxs-lookup"><span data-stu-id="62feb-934">tax#</span></span>
  
<span data-ttu-id="62feb-935">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="62feb-935">taxid#</span></span>
  
<span data-ttu-id="62feb-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-936">tax file</span></span>
  
<span data-ttu-id="62feb-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="62feb-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62feb-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62feb-938">See also</span></span>

[<span data-ttu-id="62feb-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="62feb-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

