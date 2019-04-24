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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255522"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="c3b42-104">Numéro d'identification fiscale de l'UE</span><span class="sxs-lookup"><span data-stu-id="c3b42-104">EU Tax Identification Number</span></span>

<span data-ttu-id="c3b42-105">Cette rubrique montre ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'il détecte le type d'informations sensibles de l'ID taxe de l'UE (TIN).</span><span class="sxs-lookup"><span data-stu-id="c3b42-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="c3b42-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="c3b42-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="c3b42-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="c3b42-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-108">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-108">Format</span></span>

<span data-ttu-id="c3b42-109">Neuf chiffres avec un trait d'union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="c3b42-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-110">Pattern</span></span>

<span data-ttu-id="c3b42-111">Neuf chiffres avec un trait d'Union et une barre oblique facultatifs:</span><span class="sxs-lookup"><span data-stu-id="c3b42-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="c3b42-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-112">Two digits</span></span> 
    
- <span data-ttu-id="c3b42-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c3b42-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="c3b42-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-114">Three digits</span></span>
    
- <span data-ttu-id="c3b42-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="c3b42-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="c3b42-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-117">Checksum</span></span>

<span data-ttu-id="c3b42-118">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-119">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-119">Definition</span></span>

<span data-ttu-id="c3b42-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-125">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="c3b42-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-127">tax number</span></span>
  
<span data-ttu-id="c3b42-128">number</span><span class="sxs-lookup"><span data-stu-id="c3b42-128">number</span></span>
  
<span data-ttu-id="c3b42-129">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-129">tax registration number</span></span>
  
<span data-ttu-id="c3b42-130">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-130">tax id</span></span>
  
<span data-ttu-id="c3b42-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="c3b42-131">st.nr.</span></span>
  
<span data-ttu-id="c3b42-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="c3b42-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="c3b42-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-134">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-134">Format</span></span>

<span data-ttu-id="c3b42-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-136">Pattern</span></span>

<span data-ttu-id="c3b42-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="c3b42-137">11 digits:</span></span>
  
- <span data-ttu-id="c3b42-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-138">Two digits</span></span>
    
- <span data-ttu-id="c3b42-139">«0» ou «1»</span><span class="sxs-lookup"><span data-stu-id="c3b42-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="c3b42-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="c3b42-140">One digit</span></span>
    
- <span data-ttu-id="c3b42-141">«0» ou «1» ou «2» ou «3»</span><span class="sxs-lookup"><span data-stu-id="c3b42-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="c3b42-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-143">Checksum</span></span>

<span data-ttu-id="c3b42-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-145">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-145">Definition</span></span>

<span data-ttu-id="c3b42-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-147">L'expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-149">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="c3b42-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-151">tax number</span></span>
  
<span data-ttu-id="c3b42-152">Numéro d'enregistrement national</span><span class="sxs-lookup"><span data-stu-id="c3b42-152">national registration number</span></span>
  
<span data-ttu-id="c3b42-153">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-153">tax registration number</span></span>
  
<span data-ttu-id="c3b42-154">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-154">tax id</span></span>
  
<span data-ttu-id="c3b42-155">nPour</span><span class="sxs-lookup"><span data-stu-id="c3b42-155">nif</span></span>
  
<span data-ttu-id="c3b42-156">nPour</span><span class="sxs-lookup"><span data-stu-id="c3b42-156">nif#</span></span>
  
<span data-ttu-id="c3b42-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="c3b42-157">numéro de registre national</span></span>
  
<span data-ttu-id="c3b42-158">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="c3b42-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="c3b42-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-160">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-160">Format</span></span>

<span data-ttu-id="c3b42-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-162">Pattern</span></span>

<span data-ttu-id="c3b42-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-164">Checksum</span></span>

<span data-ttu-id="c3b42-165">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-166">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-166">Definition</span></span>

<span data-ttu-id="c3b42-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-172">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="c3b42-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-174">bucn</span><span class="sxs-lookup"><span data-stu-id="c3b42-174">bucn</span></span>
  
<span data-ttu-id="c3b42-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="c3b42-175">uniform civil number</span></span>
  
<span data-ttu-id="c3b42-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="c3b42-176">bucn#</span></span>
  
<span data-ttu-id="c3b42-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="c3b42-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="c3b42-178">uniform civil id</span></span>
  
<span data-ttu-id="c3b42-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="c3b42-179">uniform civil no</span></span>
  
<span data-ttu-id="c3b42-180">EGN</span><span class="sxs-lookup"><span data-stu-id="c3b42-180">egn</span></span>
  
<span data-ttu-id="c3b42-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="c3b42-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="c3b42-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-182">uniformcivilno#</span></span>
  
<span data-ttu-id="c3b42-183">EGN #</span><span class="sxs-lookup"><span data-stu-id="c3b42-183">egn#</span></span>
  
<span data-ttu-id="c3b42-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="c3b42-184">униформ граждански номер</span></span>
  
<span data-ttu-id="c3b42-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="c3b42-185">униформ id</span></span>
  
<span data-ttu-id="c3b42-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="c3b42-186">униформ граждански id</span></span>
  
<span data-ttu-id="c3b42-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="c3b42-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="c3b42-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="c3b42-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-189">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-189">Format</span></span>

<span data-ttu-id="c3b42-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-191">Pattern</span></span>

<span data-ttu-id="c3b42-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="c3b42-192">11 digits:</span></span>
  
- <span data-ttu-id="c3b42-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="c3b42-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="c3b42-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-195">Checksum</span></span>

<span data-ttu-id="c3b42-196">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-197">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-197">Definition</span></span>

<span data-ttu-id="c3b42-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-203">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="c3b42-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-205">tax number</span></span>
  
<span data-ttu-id="c3b42-206">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-206">tax</span></span>
  
<span data-ttu-id="c3b42-207">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-207">tax id</span></span>
  
<span data-ttu-id="c3b42-208">oid</span><span class="sxs-lookup"><span data-stu-id="c3b42-208">oid</span></span>
  
<span data-ttu-id="c3b42-209">OID</span><span class="sxs-lookup"><span data-stu-id="c3b42-209">oid#</span></span>
  
<span data-ttu-id="c3b42-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="c3b42-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="c3b42-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="c3b42-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-212">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-212">Format</span></span>

<span data-ttu-id="c3b42-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-214">Pattern</span></span>

<span data-ttu-id="c3b42-215">Huit chiffres et une lettre:</span><span class="sxs-lookup"><span data-stu-id="c3b42-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="c3b42-216">«0»</span><span class="sxs-lookup"><span data-stu-id="c3b42-216">A "0"</span></span> 
    
- <span data-ttu-id="c3b42-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-217">Seven digits</span></span>
    
- <span data-ttu-id="c3b42-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-219">Checksum</span></span>

<span data-ttu-id="c3b42-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-221">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-221">Definition</span></span>

<span data-ttu-id="c3b42-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-227">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="c3b42-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-229">tax number</span></span>
  
<span data-ttu-id="c3b42-230">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-230">tax</span></span>
  
<span data-ttu-id="c3b42-231">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-231">tax id</span></span>
  
<span data-ttu-id="c3b42-232">code d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-232">tax identification code</span></span>
  
<span data-ttu-id="c3b42-233">graduation</span><span class="sxs-lookup"><span data-stu-id="c3b42-233">tic</span></span>
  
<span data-ttu-id="c3b42-234">graduation</span><span class="sxs-lookup"><span data-stu-id="c3b42-234">tic#</span></span>
  
<span data-ttu-id="c3b42-235">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="c3b42-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="c3b42-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="c3b42-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="c3b42-237">Κωδικός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="c3b42-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="c3b42-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="c3b42-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-239">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-239">Format</span></span>

<span data-ttu-id="c3b42-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="c3b42-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-241">Pattern</span></span>

<span data-ttu-id="c3b42-242">Neuf ou dix chiffres avec une barre oblique inverse facultative:</span><span class="sxs-lookup"><span data-stu-id="c3b42-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="c3b42-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-243">Six digits</span></span> 
    
- <span data-ttu-id="c3b42-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c3b42-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="c3b42-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-246">Checksum</span></span>

<span data-ttu-id="c3b42-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-248">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-248">Definition</span></span>

<span data-ttu-id="c3b42-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-250">L'expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-252">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="c3b42-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-254">tax number</span></span>
  
<span data-ttu-id="c3b42-255">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-255">tax</span></span>
  
<span data-ttu-id="c3b42-256">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-256">tax id</span></span>
  
<span data-ttu-id="c3b42-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-257">personal number</span></span>
  
<span data-ttu-id="c3b42-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="c3b42-258">daňové číslo</span></span>
  
<span data-ttu-id="c3b42-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="c3b42-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="c3b42-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="c3b42-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-261">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-261">Format</span></span>

<span data-ttu-id="c3b42-262">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="c3b42-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-263">Pattern</span></span>

<span data-ttu-id="c3b42-264">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="c3b42-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="c3b42-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="c3b42-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="c3b42-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="c3b42-266">A hyphen</span></span>
    
- <span data-ttu-id="c3b42-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l'individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="c3b42-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-268">Checksum</span></span>

<span data-ttu-id="c3b42-269">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-270">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-270">Definition</span></span>

<span data-ttu-id="c3b42-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-276">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="c3b42-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-278">tax number</span></span>
  
<span data-ttu-id="c3b42-279">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-279">tax</span></span>
  
<span data-ttu-id="c3b42-280">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-280">tax id</span></span>
  
<span data-ttu-id="c3b42-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="c3b42-281">cpr number</span></span>
  
<span data-ttu-id="c3b42-282">cardio</span><span class="sxs-lookup"><span data-stu-id="c3b42-282">cpr#</span></span>
  
<span data-ttu-id="c3b42-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-283">skat nummer</span></span>
  
<span data-ttu-id="c3b42-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="c3b42-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="c3b42-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="c3b42-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-286">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-286">Format</span></span>

<span data-ttu-id="c3b42-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-288">Pattern</span></span>

<span data-ttu-id="c3b42-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="c3b42-289">11 digits:</span></span>
  
-  <span data-ttu-id="c3b42-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit: 1,2 pour le 19 siècle; 3, 4 pour le vingtième siècle; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="c3b42-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="c3b42-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="c3b42-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="c3b42-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="c3b42-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="c3b42-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-294">Checksum</span></span>

<span data-ttu-id="c3b42-295">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-296">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-296">Definition</span></span>

<span data-ttu-id="c3b42-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-302">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="c3b42-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-304">tax number</span></span>
  
<span data-ttu-id="c3b42-305">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-305">tax</span></span>
  
<span data-ttu-id="c3b42-306">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-306">tax id</span></span>
  
<span data-ttu-id="c3b42-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-307">personal code</span></span>
  
<span data-ttu-id="c3b42-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-308">maksunumber</span></span>
  
<span data-ttu-id="c3b42-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="c3b42-309">maksu id</span></span>
  
<span data-ttu-id="c3b42-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="c3b42-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="c3b42-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="c3b42-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-312">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-312">Format</span></span>

<span data-ttu-id="c3b42-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="c3b42-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-314">Pattern</span></span>

<span data-ttu-id="c3b42-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins:</span><span class="sxs-lookup"><span data-stu-id="c3b42-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="c3b42-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-316">Six digits</span></span>
    
- <span data-ttu-id="c3b42-317">L'une des options suivantes: un signe plus, un signe moins ou la lettre «A» (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et «A» désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="c3b42-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="c3b42-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-318">Three digits</span></span>
    
- <span data-ttu-id="c3b42-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="c3b42-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-320">Checksum</span></span>

<span data-ttu-id="c3b42-321">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-322">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-322">Definition</span></span>

<span data-ttu-id="c3b42-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-328">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="c3b42-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-330">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="c3b42-330">identification number</span></span>
  
<span data-ttu-id="c3b42-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-331">personal id</span></span>
  
<span data-ttu-id="c3b42-332">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="c3b42-332">identity number</span></span>
  
<span data-ttu-id="c3b42-333">Numéro d'identification national finnois</span><span class="sxs-lookup"><span data-stu-id="c3b42-333">finnish national id number</span></span>
  
<span data-ttu-id="c3b42-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-334">personalidnumber#</span></span>
  
<span data-ttu-id="c3b42-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="c3b42-335">national identification number</span></span>
  
<span data-ttu-id="c3b42-336">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="c3b42-336">id number</span></span>
  
<span data-ttu-id="c3b42-337">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="c3b42-337">national id no.</span></span>
  
<span data-ttu-id="c3b42-338">Numéro d'identification national</span><span class="sxs-lookup"><span data-stu-id="c3b42-338">national id number</span></span>
  
<span data-ttu-id="c3b42-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="c3b42-339">id no</span></span>
  
<span data-ttu-id="c3b42-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="c3b42-340">tunnistenumero</span></span>
  
<span data-ttu-id="c3b42-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="c3b42-341">henkilötunnus</span></span>
  
<span data-ttu-id="c3b42-342">Yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="c3b42-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="c3b42-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="c3b42-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="c3b42-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="c3b42-344">identiteetti numero</span></span>
  
<span data-ttu-id="c3b42-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="c3b42-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="c3b42-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="c3b42-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="c3b42-347">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="c3b42-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="c3b42-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="c3b42-348">tunnusnumero</span></span>
  
<span data-ttu-id="c3b42-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="c3b42-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="c3b42-350">France</span><span class="sxs-lookup"><span data-stu-id="c3b42-350">France</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-351">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-351">Format</span></span>

<span data-ttu-id="c3b42-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="c3b42-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-353">Pattern</span></span>

<span data-ttu-id="c3b42-354">13 chiffres pour les personnes:</span><span class="sxs-lookup"><span data-stu-id="c3b42-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="c3b42-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="c3b42-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="c3b42-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-356">12 digits</span></span>
    
<span data-ttu-id="c3b42-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="c3b42-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-358">Checksum</span></span>

<span data-ttu-id="c3b42-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-360">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-360">Definition</span></span>

<span data-ttu-id="c3b42-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-366">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="c3b42-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-368">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-368">tax identification number</span></span>
  
<span data-ttu-id="c3b42-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-369">tax number</span></span>
  
<span data-ttu-id="c3b42-370">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-370">tax id</span></span>
  
<span data-ttu-id="c3b42-371">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="c3b42-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="c3b42-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-373">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-373">Format</span></span>

<span data-ttu-id="c3b42-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-375">Pattern</span></span>

<span data-ttu-id="c3b42-376">11 chiffres:</span><span class="sxs-lookup"><span data-stu-id="c3b42-376">11 digits :</span></span>
  
-  <span data-ttu-id="c3b42-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-377">Ten digits</span></span> 
    
- <span data-ttu-id="c3b42-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-379">Checksum</span></span>

<span data-ttu-id="c3b42-380">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-381">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-381">Definition</span></span>

<span data-ttu-id="c3b42-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-387">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="c3b42-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-389">tax number</span></span>
  
<span data-ttu-id="c3b42-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-390">tax no.</span></span>
  
<span data-ttu-id="c3b42-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-391">taxno#</span></span>
  
<span data-ttu-id="c3b42-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-392">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-393">taxnumber</span></span>
  
<span data-ttu-id="c3b42-394">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-394">tax id</span></span>
  
<span data-ttu-id="c3b42-395">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-395">taxid#</span></span>
  
<span data-ttu-id="c3b42-396">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-396">tax identification number</span></span>
  
<span data-ttu-id="c3b42-397">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-397">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-398">steuernummer</span></span>
  
<span data-ttu-id="c3b42-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="c3b42-399">steuer id</span></span>
  
<span data-ttu-id="c3b42-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="c3b42-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="c3b42-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-402">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-402">Format</span></span>

<span data-ttu-id="c3b42-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-404">Pattern</span></span>

<span data-ttu-id="c3b42-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-406">Checksum</span></span>

<span data-ttu-id="c3b42-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-408">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-408">Definition</span></span>

<span data-ttu-id="c3b42-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-410">L'expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-412">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="c3b42-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-414">financement</span><span class="sxs-lookup"><span data-stu-id="c3b42-414">afm</span></span>
  
<span data-ttu-id="c3b42-415">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-415">tin</span></span>
  
<span data-ttu-id="c3b42-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-416">tax id no.</span></span>
  
<span data-ttu-id="c3b42-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-417">tax id no</span></span>
  
<span data-ttu-id="c3b42-418">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-418">tax identification number</span></span>
  
<span data-ttu-id="c3b42-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="c3b42-419">tax registry number</span></span>
  
<span data-ttu-id="c3b42-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-420">tax registry no.</span></span>
  
<span data-ttu-id="c3b42-421">financement</span><span class="sxs-lookup"><span data-stu-id="c3b42-421">afm#</span></span>
  
<span data-ttu-id="c3b42-422">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-422">tin#</span></span>
  
<span data-ttu-id="c3b42-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-423">taxidno#</span></span>
  
<span data-ttu-id="c3b42-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-424">taxregistryno#</span></span>
  
<span data-ttu-id="c3b42-425">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="c3b42-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="c3b42-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="c3b42-426">aφμ</span></span>
  
<span data-ttu-id="c3b42-427">aφμ Αριθμός</span><span class="sxs-lookup"><span data-stu-id="c3b42-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="c3b42-428">φορολογικού Μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="c3b42-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="c3b42-429">τον αριθμό φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="c3b42-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="c3b42-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="c3b42-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-431">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-431">Format</span></span>

<span data-ttu-id="c3b42-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-433">Pattern</span></span>

<span data-ttu-id="c3b42-434">Dix chiffres:</span><span class="sxs-lookup"><span data-stu-id="c3b42-434">Ten digits:</span></span>
  
-  <span data-ttu-id="c3b42-435">Un chiffre qui doit être «8»</span><span class="sxs-lookup"><span data-stu-id="c3b42-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="c3b42-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="c3b42-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="c3b42-437">Trois chiffres correspondant au nombre généré par l'opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="c3b42-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="c3b42-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-439">Checksum</span></span>

<span data-ttu-id="c3b42-440">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-441">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-441">Definition</span></span>

<span data-ttu-id="c3b42-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-447">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="c3b42-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-449">Numéro d'identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="c3b42-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="c3b42-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="c3b42-450">hungarian tin</span></span>
  
<span data-ttu-id="c3b42-451">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-451">tax id number</span></span>
  
<span data-ttu-id="c3b42-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="c3b42-452">vat number</span></span>
  
<span data-ttu-id="c3b42-453">Numéro de l'autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-453">tax authority no</span></span>
  
<span data-ttu-id="c3b42-454">Numéro d'identité fiscale de l'ID taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-454">tax id tax identity number</span></span>
  
<span data-ttu-id="c3b42-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-455">taxidnumber#</span></span>
  
<span data-ttu-id="c3b42-456">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-456">tin#</span></span>
  
<span data-ttu-id="c3b42-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="c3b42-457">hungatiantin#</span></span>
  
<span data-ttu-id="c3b42-458">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-458">tax identification no</span></span>
  
<span data-ttu-id="c3b42-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-459">taxidno#</span></span>
  
<span data-ttu-id="c3b42-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="c3b42-460">adóazonosító szám</span></span>
  
<span data-ttu-id="c3b42-461">adószám</span><span class="sxs-lookup"><span data-stu-id="c3b42-461">adószám</span></span>
  
<span data-ttu-id="c3b42-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="c3b42-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="c3b42-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="c3b42-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-464">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-464">Format</span></span>

<span data-ttu-id="c3b42-465">Sept chiffres suivis d'une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-466">Pattern</span></span>

<span data-ttu-id="c3b42-467">Sept chiffres suivis d'une lettre:</span><span class="sxs-lookup"><span data-stu-id="c3b42-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="c3b42-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-468">Seven digits</span></span> 
    
- <span data-ttu-id="c3b42-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-470">Checksum</span></span>

<span data-ttu-id="c3b42-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-472">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-472">Definition</span></span>

<span data-ttu-id="c3b42-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-478">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="c3b42-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="c3b42-480">public service no</span></span>
  
<span data-ttu-id="c3b42-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-481">personal public service no</span></span>
  
<span data-ttu-id="c3b42-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="c3b42-482">pps no</span></span>
  
<span data-ttu-id="c3b42-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-483">personal service no</span></span>
  
<span data-ttu-id="c3b42-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="c3b42-484">pps service no</span></span>
  
<span data-ttu-id="c3b42-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-485">ppsno#</span></span>
  
<span data-ttu-id="c3b42-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="c3b42-486">irish pps no</span></span>
  
<span data-ttu-id="c3b42-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-487">publicserviceno#</span></span>
  
<span data-ttu-id="c3b42-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="c3b42-488">personal public service number</span></span>
  
<span data-ttu-id="c3b42-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="c3b42-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="c3b42-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="c3b42-490">pps uimh</span></span>
  
<span data-ttu-id="c3b42-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="c3b42-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="c3b42-492">Italie</span><span class="sxs-lookup"><span data-stu-id="c3b42-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-493">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-493">Format</span></span>

<span data-ttu-id="c3b42-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-495">Pattern</span></span>

<span data-ttu-id="c3b42-496">16 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="c3b42-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="c3b42-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="c3b42-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="c3b42-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="c3b42-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="c3b42-499">Deux chiffres correspondant aux derniers chiffres de l'année de naissance</span><span class="sxs-lookup"><span data-stu-id="c3b42-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="c3b42-500">Un chiffre correspondant au mois de naissance: les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="c3b42-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="c3b42-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="c3b42-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="c3b42-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="c3b42-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="c3b42-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-504">Checksum</span></span>

<span data-ttu-id="c3b42-505">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-506">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-506">Definition</span></span>

<span data-ttu-id="c3b42-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-512">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="c3b42-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-514">tax number</span></span>
  
<span data-ttu-id="c3b42-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-515">tax no.</span></span>
  
<span data-ttu-id="c3b42-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-516">taxno#</span></span>
  
<span data-ttu-id="c3b42-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-517">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-518">taxnumber</span></span>
  
<span data-ttu-id="c3b42-519">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-519">tax id</span></span>
  
<span data-ttu-id="c3b42-520">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-520">taxid#</span></span>
  
<span data-ttu-id="c3b42-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-521">fiscal code</span></span>
  
<span data-ttu-id="c3b42-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="c3b42-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="c3b42-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-524">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-524">Format</span></span>

<span data-ttu-id="c3b42-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-526">Pattern</span></span>

<span data-ttu-id="c3b42-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="c3b42-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="c3b42-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="c3b42-529">Un chiffre correspondant au siècle de naissance où «0» correspond à 19 siècle, «1» correspond au vingtième siècle et «2» au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="c3b42-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-531">Checksum</span></span>

<span data-ttu-id="c3b42-532">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-533">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-533">Definition</span></span>

<span data-ttu-id="c3b42-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-539">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="c3b42-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-541">tax number</span></span>
  
<span data-ttu-id="c3b42-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-542">tax no.</span></span>
  
<span data-ttu-id="c3b42-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-543">taxno#</span></span>
  
<span data-ttu-id="c3b42-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-544">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-545">taxnumber</span></span>
  
<span data-ttu-id="c3b42-546">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-546">tax id</span></span>
  
<span data-ttu-id="c3b42-547">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-547">taxid#</span></span>
  
<span data-ttu-id="c3b42-548">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-548">tax identification number</span></span>
  
<span data-ttu-id="c3b42-549">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-549">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-550">nodokļa numurs</span></span>
  
<span data-ttu-id="c3b42-551">nodokļu IDENTIFIKĀCIJAS numurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="c3b42-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="c3b42-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="c3b42-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-554">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-554">Format</span></span>

<span data-ttu-id="c3b42-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-556">Pattern</span></span>

<span data-ttu-id="c3b42-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-558">Checksum</span></span>

<span data-ttu-id="c3b42-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-560">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-560">Definition</span></span>

<span data-ttu-id="c3b42-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-566">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="c3b42-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-568">tax number</span></span>
  
<span data-ttu-id="c3b42-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-569">tax no.</span></span>
  
<span data-ttu-id="c3b42-570">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="c3b42-570">tax no#</span></span>
  
<span data-ttu-id="c3b42-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-571">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-572">taxnumber</span></span>
  
<span data-ttu-id="c3b42-573">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-573">tax id</span></span>
  
<span data-ttu-id="c3b42-574">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-574">taxid#</span></span>
  
<span data-ttu-id="c3b42-575">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-575">tax identification number</span></span>
  
<span data-ttu-id="c3b42-576">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-576">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="c3b42-577">mokesčių id</span></span>
  
<span data-ttu-id="c3b42-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-578">mokesčių numeris</span></span>
  
<span data-ttu-id="c3b42-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="c3b42-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="c3b42-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="c3b42-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-581">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-581">Format</span></span>

<span data-ttu-id="c3b42-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-583">Pattern</span></span>

<span data-ttu-id="c3b42-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="c3b42-584">13 digits:</span></span>
  
-  <span data-ttu-id="c3b42-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-585">11 digits</span></span> 
    
- <span data-ttu-id="c3b42-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-587">Checksum</span></span>

<span data-ttu-id="c3b42-588">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-589">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-589">Definition</span></span>

<span data-ttu-id="c3b42-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-595">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="c3b42-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-597">tax number</span></span>
  
<span data-ttu-id="c3b42-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-598">tax no.</span></span>
  
<span data-ttu-id="c3b42-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-599">taxno#</span></span>
  
<span data-ttu-id="c3b42-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-600">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-601">taxnumber</span></span>
  
<span data-ttu-id="c3b42-602">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-602">tax id</span></span>
  
<span data-ttu-id="c3b42-603">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-603">taxid#</span></span>
  
<span data-ttu-id="c3b42-604">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-604">tax identification number</span></span>
  
<span data-ttu-id="c3b42-605">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-605">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-606">steuernummer</span></span>
  
<span data-ttu-id="c3b42-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="c3b42-607">steuer id</span></span>
  
<span data-ttu-id="c3b42-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="c3b42-609">Malte</span><span class="sxs-lookup"><span data-stu-id="c3b42-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-610">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-610">Format</span></span>

<span data-ttu-id="c3b42-611">Pour les ressortissants maltais: 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="c3b42-612">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-613">Pattern</span></span>

<span data-ttu-id="c3b42-614">Ressortissants maltaises: 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="c3b42-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="c3b42-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-615">Seven digits</span></span> 
    
- <span data-ttu-id="c3b42-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="c3b42-617">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="c3b42-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="c3b42-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-619">Checksum</span></span>

<span data-ttu-id="c3b42-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-621">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-621">Definition</span></span>

<span data-ttu-id="c3b42-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-627">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="c3b42-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-629">tax number</span></span>
  
<span data-ttu-id="c3b42-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-630">tax no.</span></span>
  
<span data-ttu-id="c3b42-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-631">taxno#</span></span>
  
<span data-ttu-id="c3b42-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-632">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-633">taxnumber</span></span>
  
<span data-ttu-id="c3b42-634">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-634">tax id</span></span>
  
<span data-ttu-id="c3b42-635">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-635">taxid#</span></span>
  
<span data-ttu-id="c3b42-636">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-636">tax identification number</span></span>
  
<span data-ttu-id="c3b42-637">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-637">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="c3b42-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="c3b42-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="c3b42-639">id tat-taxxa</span></span>
  
<span data-ttu-id="c3b42-640">numru ta'IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="c3b42-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="c3b42-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="c3b42-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-642">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-642">Format</span></span>

<span data-ttu-id="c3b42-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-644">Pattern</span></span>

<span data-ttu-id="c3b42-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="c3b42-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-646">Checksum</span></span>

<span data-ttu-id="c3b42-647">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-648">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-648">Definition</span></span>

<span data-ttu-id="c3b42-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-654">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="c3b42-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-656">Numéro d'identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="c3b42-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="c3b42-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="c3b42-657">netherlands tax identification</span></span>
  
<span data-ttu-id="c3b42-658">Numéro d'identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="c3b42-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="c3b42-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="c3b42-659">netherland's tax identification</span></span>
  
<span data-ttu-id="c3b42-660">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-660">tax identification number</span></span>
  
<span data-ttu-id="c3b42-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="c3b42-661">dutch tax id</span></span>
  
<span data-ttu-id="c3b42-662">Numéro d'identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="c3b42-662">dutch tax identification number</span></span>
  
<span data-ttu-id="c3b42-663">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-663">tax id</span></span>
  
<span data-ttu-id="c3b42-664">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-664">tax id#</span></span>
  
<span data-ttu-id="c3b42-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-665">tax number</span></span>
  
<span data-ttu-id="c3b42-666">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="c3b42-666">tax no#</span></span>
  
<span data-ttu-id="c3b42-667">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-667">tax#</span></span>
  
<span data-ttu-id="c3b42-668">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-668">tin</span></span>
  
<span data-ttu-id="c3b42-669">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-669">tin#</span></span>
  
<span data-ttu-id="c3b42-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="c3b42-670">netherlands tin</span></span>
  
<span data-ttu-id="c3b42-671">Netherland d'étain</span><span class="sxs-lookup"><span data-stu-id="c3b42-671">netherland's tin</span></span>
  
<span data-ttu-id="c3b42-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="c3b42-673">identificatienummer van à l'avant-dernière</span><span class="sxs-lookup"><span data-stu-id="c3b42-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="c3b42-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="c3b42-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="c3b42-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="c3b42-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="c3b42-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="c3b42-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-678">btw nummer</span></span>
  
<span data-ttu-id="c3b42-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="c3b42-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="c3b42-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="c3b42-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-681">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-681">Format</span></span>

<span data-ttu-id="c3b42-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-683">Pattern</span></span>

<span data-ttu-id="c3b42-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-685">Checksum</span></span>

<span data-ttu-id="c3b42-686">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-687">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-687">Definition</span></span>

<span data-ttu-id="c3b42-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-693">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="c3b42-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-695">tax number</span></span>
  
<span data-ttu-id="c3b42-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-696">tax no.</span></span>
  
<span data-ttu-id="c3b42-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-697">taxno#</span></span>
  
<span data-ttu-id="c3b42-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-698">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-699">taxnumber</span></span>
  
<span data-ttu-id="c3b42-700">pince</span><span class="sxs-lookup"><span data-stu-id="c3b42-700">nip</span></span>
  
<span data-ttu-id="c3b42-701">pince</span><span class="sxs-lookup"><span data-stu-id="c3b42-701">nip#</span></span>
  
<span data-ttu-id="c3b42-702">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-702">tax id</span></span>
  
<span data-ttu-id="c3b42-703">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-703">tax id#</span></span>
  
<span data-ttu-id="c3b42-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="c3b42-704">nip id</span></span>
  
<span data-ttu-id="c3b42-705">n ° de NIP</span><span class="sxs-lookup"><span data-stu-id="c3b42-705">nip id#</span></span>
  
<span data-ttu-id="c3b42-706">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-706">tax identification number</span></span>
  
<span data-ttu-id="c3b42-707">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-707">tax identification no.</span></span>
  
<span data-ttu-id="c3b42-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="c3b42-708">vat number</span></span>
  
<span data-ttu-id="c3b42-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="c3b42-709">vat no.</span></span>
  
<span data-ttu-id="c3b42-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-710">vatno#</span></span>
  
<span data-ttu-id="c3b42-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="c3b42-711">vat id</span></span>
  
<span data-ttu-id="c3b42-712">n ° de TVA</span><span class="sxs-lookup"><span data-stu-id="c3b42-712">vat id#</span></span>
  
<span data-ttu-id="c3b42-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="c3b42-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="c3b42-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="c3b42-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="c3b42-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="c3b42-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="c3b42-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="c3b42-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-717">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-717">Format</span></span>

<span data-ttu-id="c3b42-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-719">Pattern</span></span>

<span data-ttu-id="c3b42-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-721">Checksum</span></span>

<span data-ttu-id="c3b42-722">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-723">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-723">Definition</span></span>

<span data-ttu-id="c3b42-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-729">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="c3b42-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-731">tax number</span></span>
  
<span data-ttu-id="c3b42-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-732">tax no.</span></span>
  
<span data-ttu-id="c3b42-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-733">taxno#</span></span>
  
<span data-ttu-id="c3b42-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="c3b42-734">taxnumber#</span></span>
  
<span data-ttu-id="c3b42-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="c3b42-735">taxnumber</span></span>
  
<span data-ttu-id="c3b42-736">nPour</span><span class="sxs-lookup"><span data-stu-id="c3b42-736">nif</span></span>
  
<span data-ttu-id="c3b42-737">nPour</span><span class="sxs-lookup"><span data-stu-id="c3b42-737">nif#</span></span>
  
<span data-ttu-id="c3b42-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="c3b42-738">numero fiscal</span></span>
  
<span data-ttu-id="c3b42-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="c3b42-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="c3b42-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-741">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-741">Format</span></span>

<span data-ttu-id="c3b42-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-743">Pattern</span></span>

<span data-ttu-id="c3b42-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-745">Checksum</span></span>

<span data-ttu-id="c3b42-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-747">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-747">Definition</span></span>

<span data-ttu-id="c3b42-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-749">L'expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-751">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="c3b42-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-753">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-753">tax id</span></span>
  
<span data-ttu-id="c3b42-754">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-754">tax id number</span></span>
  
<span data-ttu-id="c3b42-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-755">tax file no</span></span>
  
<span data-ttu-id="c3b42-756">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-756">tax file number</span></span>
  
<span data-ttu-id="c3b42-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-757">tax no</span></span>
  
<span data-ttu-id="c3b42-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-758">tax number</span></span>
  
<span data-ttu-id="c3b42-759">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-759">taxid#</span></span>
  
<span data-ttu-id="c3b42-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-760">taxno#</span></span>
  
<span data-ttu-id="c3b42-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="c3b42-761">id-ul taxei</span></span>
  
<span data-ttu-id="c3b42-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="c3b42-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="c3b42-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="c3b42-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-764">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-764">Format</span></span>

<span data-ttu-id="c3b42-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-766">Pattern</span></span>

<span data-ttu-id="c3b42-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-768">Checksum</span></span>

<span data-ttu-id="c3b42-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c3b42-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-770">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-770">Definition</span></span>

<span data-ttu-id="c3b42-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-772">L'expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-774">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="c3b42-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-776">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-776">tax id</span></span>
  
<span data-ttu-id="c3b42-777">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-777">tax id number</span></span>
  
<span data-ttu-id="c3b42-778">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="c3b42-778">tin id</span></span>
  
<span data-ttu-id="c3b42-779">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="c3b42-779">tin no</span></span>
  
<span data-ttu-id="c3b42-780">ID d'étain slovaque</span><span class="sxs-lookup"><span data-stu-id="c3b42-780">slovakian tin id</span></span>
  
<span data-ttu-id="c3b42-781">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-781">tin</span></span>
  
<span data-ttu-id="c3b42-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-782">tax file no</span></span>
  
<span data-ttu-id="c3b42-783">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-783">tax file number</span></span>
  
<span data-ttu-id="c3b42-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-784">tax no</span></span>
  
<span data-ttu-id="c3b42-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-785">tax number</span></span>
  
<span data-ttu-id="c3b42-786">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-786">taxid#</span></span>
  
<span data-ttu-id="c3b42-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-787">taxno#</span></span>
  
<span data-ttu-id="c3b42-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="c3b42-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="c3b42-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="c3b42-789">daňové číslo</span></span>
  
<span data-ttu-id="c3b42-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="c3b42-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="c3b42-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="c3b42-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-792">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-792">Format</span></span>

<span data-ttu-id="c3b42-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-794">Pattern</span></span>

<span data-ttu-id="c3b42-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-796">Checksum</span></span>

<span data-ttu-id="c3b42-797">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-798">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-798">Definition</span></span>

<span data-ttu-id="c3b42-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-804">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="c3b42-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-806">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-806">tax id</span></span>
  
<span data-ttu-id="c3b42-807">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-807">tax id number</span></span>
  
<span data-ttu-id="c3b42-808">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="c3b42-808">tin id</span></span>
  
<span data-ttu-id="c3b42-809">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="c3b42-809">tin no</span></span>
  
<span data-ttu-id="c3b42-810">ID d'étain slovène</span><span class="sxs-lookup"><span data-stu-id="c3b42-810">slovenian tin id</span></span>
  
<span data-ttu-id="c3b42-811">Etain</span><span class="sxs-lookup"><span data-stu-id="c3b42-811">tin</span></span>
  
<span data-ttu-id="c3b42-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-812">tax file no</span></span>
  
<span data-ttu-id="c3b42-813">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-813">tax file number</span></span>
  
<span data-ttu-id="c3b42-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-814">tax no</span></span>
  
<span data-ttu-id="c3b42-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-815">tax number</span></span>
  
<span data-ttu-id="c3b42-816">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-816">taxid#</span></span>
  
<span data-ttu-id="c3b42-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-817">taxno#</span></span>
  
<span data-ttu-id="c3b42-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="c3b42-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="c3b42-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="c3b42-819">davčna številka</span></span>
  
<span data-ttu-id="c3b42-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="c3b42-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="c3b42-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="c3b42-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-822">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-822">Format</span></span>

<span data-ttu-id="c3b42-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-824">Pattern</span></span>

<span data-ttu-id="c3b42-825">Personnes physiques espagnoles avec une carte d'identité nationale d'Espagne:</span><span class="sxs-lookup"><span data-stu-id="c3b42-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="c3b42-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-826">Eight digits</span></span> 
    
- <span data-ttu-id="c3b42-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="c3b42-828">Spaniards non résident sans carte d'identité nationale d'Espagne</span><span class="sxs-lookup"><span data-stu-id="c3b42-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="c3b42-829">Une lettre majuscule «L» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="c3b42-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-830">Seven digits</span></span>
    
- <span data-ttu-id="c3b42-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="c3b42-832">Spaniards résident de moins de 14 ans sans carte d'identité nationale (Espagne):</span><span class="sxs-lookup"><span data-stu-id="c3b42-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="c3b42-833">Une lettre majuscule «K» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="c3b42-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-834">Seven digits</span></span> 
    
- <span data-ttu-id="c3b42-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="c3b42-836">Foreigners avec le numéro d'identification d'un étranger</span><span class="sxs-lookup"><span data-stu-id="c3b42-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="c3b42-837">Une lettre majuscule qui est «X», «Y» ou «Z» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="c3b42-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-838">Seven digits</span></span>
    
- <span data-ttu-id="c3b42-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="c3b42-840">Foreigners sans numéro d'identification étranger</span><span class="sxs-lookup"><span data-stu-id="c3b42-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="c3b42-841">Une lettre majuscule qui est «M» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="c3b42-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="c3b42-842">Seven digits</span></span>
    
- <span data-ttu-id="c3b42-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="c3b42-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="c3b42-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-844">Checksum</span></span>

<span data-ttu-id="c3b42-845">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-846">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-846">Definition</span></span>

<span data-ttu-id="c3b42-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-852">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="c3b42-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-854">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-854">tax id</span></span>
  
<span data-ttu-id="c3b42-855">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-855">tax id number</span></span>
  
<span data-ttu-id="c3b42-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="c3b42-856">cif id</span></span>
  
<span data-ttu-id="c3b42-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="c3b42-857">cif no</span></span>
  
<span data-ttu-id="c3b42-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="c3b42-858">spanish cif id</span></span>
  
<span data-ttu-id="c3b42-859">importation</span><span class="sxs-lookup"><span data-stu-id="c3b42-859">cif</span></span>
  
<span data-ttu-id="c3b42-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-860">tax file no</span></span>
  
<span data-ttu-id="c3b42-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="c3b42-861">spanish cif number</span></span>
  
<span data-ttu-id="c3b42-862">numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-862">tax file number</span></span>
  
<span data-ttu-id="c3b42-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="c3b42-863">spanish cif no</span></span>
  
<span data-ttu-id="c3b42-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-864">tax no</span></span>
  
<span data-ttu-id="c3b42-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-865">tax number</span></span>
  
<span data-ttu-id="c3b42-866">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-866">taxid#</span></span>
  
<span data-ttu-id="c3b42-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-867">taxno#</span></span>
  
<span data-ttu-id="c3b42-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="c3b42-868">cifid#</span></span>
  
<span data-ttu-id="c3b42-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="c3b42-869">spanishcifid#</span></span>
  
<span data-ttu-id="c3b42-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="c3b42-870">spanishcifno#</span></span>
  
<span data-ttu-id="c3b42-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="c3b42-871">número de contribuyente</span></span>
  
<span data-ttu-id="c3b42-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="c3b42-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="c3b42-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="c3b42-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="c3b42-874">cif número</span></span>
  
<span data-ttu-id="c3b42-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="c3b42-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="c3b42-876">Suède</span><span class="sxs-lookup"><span data-stu-id="c3b42-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-877">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-877">Format</span></span>

<span data-ttu-id="c3b42-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="c3b42-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-879">Pattern</span></span>

<span data-ttu-id="c3b42-880">Dix chiffres et un symbole:</span><span class="sxs-lookup"><span data-stu-id="c3b42-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="c3b42-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="c3b42-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="c3b42-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="c3b42-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="c3b42-883">Trois chiffres qui permettent de définir le numéro d'identification unique:</span><span class="sxs-lookup"><span data-stu-id="c3b42-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="c3b42-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l'étranger.</span><span class="sxs-lookup"><span data-stu-id="c3b42-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="c3b42-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="c3b42-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="c3b42-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="c3b42-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-887">Checksum</span></span>

<span data-ttu-id="c3b42-888">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-889">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-889">Definition</span></span>

<span data-ttu-id="c3b42-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="c3b42-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="c3b42-895">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="c3b42-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-897">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-897">tax id</span></span>
  
<span data-ttu-id="c3b42-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-898">tax id no.</span></span>
  
<span data-ttu-id="c3b42-899">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-899">tax id number</span></span>
  
<span data-ttu-id="c3b42-900">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-900">tax identification</span></span>
  
<span data-ttu-id="c3b42-901">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-901">tax identification#</span></span>
  
<span data-ttu-id="c3b42-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-902">tax no.</span></span>
  
<span data-ttu-id="c3b42-903">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-903">tax#</span></span>
  
<span data-ttu-id="c3b42-904">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-904">taxid#</span></span>
  
<span data-ttu-id="c3b42-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-905">tax file</span></span>
  
<span data-ttu-id="c3b42-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-906">tax file no.</span></span>
  
<span data-ttu-id="c3b42-907">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="c3b42-907">personal id number</span></span>
  
<span data-ttu-id="c3b42-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-908">skatt id nummer</span></span>
  
<span data-ttu-id="c3b42-909">skatt Identifikation</span><span class="sxs-lookup"><span data-stu-id="c3b42-909">skatt identifikation</span></span>
  
<span data-ttu-id="c3b42-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="c3b42-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="c3b42-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="c3b42-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="c3b42-912">Format</span><span class="sxs-lookup"><span data-stu-id="c3b42-912">Format</span></span>

<span data-ttu-id="c3b42-913">Référence de conTribuable unique (UTR): 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="c3b42-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="c3b42-914">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="c3b42-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="c3b42-915">National Insurance Number (NINO)» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="c3b42-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="c3b42-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="c3b42-916">Pattern</span></span>

<span data-ttu-id="c3b42-917">Référence de conTribuable unique (UTR): 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="c3b42-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="c3b42-918">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="c3b42-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="c3b42-919">National Insurance Number (NINO)» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="c3b42-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="c3b42-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c3b42-920">Checksum</span></span>

<span data-ttu-id="c3b42-921">Oui</span><span class="sxs-lookup"><span data-stu-id="c3b42-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="c3b42-922">Définition</span><span class="sxs-lookup"><span data-stu-id="c3b42-922">Definition</span></span>

<span data-ttu-id="c3b42-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c3b42-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="c3b42-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c3b42-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="c3b42-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3b42-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c3b42-926">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c3b42-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="c3b42-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="c3b42-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="c3b42-928">id fiscal</span><span class="sxs-lookup"><span data-stu-id="c3b42-928">tax id</span></span>
  
<span data-ttu-id="c3b42-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-929">tax id no.</span></span>
  
<span data-ttu-id="c3b42-930">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-930">tax id number</span></span>
  
<span data-ttu-id="c3b42-931">identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-931">tax identification</span></span>
  
<span data-ttu-id="c3b42-932">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="c3b42-932">tax identification#</span></span>
  
<span data-ttu-id="c3b42-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-933">tax no.</span></span>
  
<span data-ttu-id="c3b42-934">codes</span><span class="sxs-lookup"><span data-stu-id="c3b42-934">tax#</span></span>
  
<span data-ttu-id="c3b42-935">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="c3b42-935">taxid#</span></span>
  
<span data-ttu-id="c3b42-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-936">tax file</span></span>
  
<span data-ttu-id="c3b42-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="c3b42-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3b42-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3b42-938">See also</span></span>

[<span data-ttu-id="c3b42-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c3b42-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

