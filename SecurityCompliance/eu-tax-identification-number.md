---
title: Numéro d’Identification de l’UE taxe
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles numéro d’Identification de taxe de l’UE. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528076"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="e2718-104">Numéro d’Identification de l’UE taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-104">EU Tax Identification Number</span></span>

<span data-ttu-id="e2718-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte le type d’informations sensibles de numéro d’Identification de l’UE taxe (TIN). Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="e2718-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e2718-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="e2718-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e2718-108">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-108">Format</span></span>

<span data-ttu-id="e2718-109">Neuf chiffres avec trait d’union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="e2718-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-110">Pattern</span></span>

<span data-ttu-id="e2718-111">Neuf chiffres avec trait d’union conditionnel et une barre oblique :</span><span class="sxs-lookup"><span data-stu-id="e2718-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="e2718-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-112">Two digits</span></span> 
    
- <span data-ttu-id="e2718-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e2718-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="e2718-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-114">Three digits</span></span>
    
- <span data-ttu-id="e2718-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="e2718-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="e2718-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-117">Checksum</span></span>

<span data-ttu-id="e2718-118">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-119">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-119">Definition</span></span>

<span data-ttu-id="e2718-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-121">La fonction `Func_austria_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-122">Un mot clé à partir de `Keywords_austria_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-124">La fonction `Func_austria_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-125">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="e2718-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-127">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-127">tax number</span></span>
  
<span data-ttu-id="e2718-128">nombre</span><span class="sxs-lookup"><span data-stu-id="e2718-128">number</span></span>
  
<span data-ttu-id="e2718-129">numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-129">tax registration number</span></span>
  
<span data-ttu-id="e2718-130">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-130">tax id</span></span>
  
<span data-ttu-id="e2718-131">St.nr.</span><span class="sxs-lookup"><span data-stu-id="e2718-131">st.nr.</span></span>
  
<span data-ttu-id="e2718-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="e2718-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e2718-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="e2718-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="e2718-134">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-134">Format</span></span>

<span data-ttu-id="e2718-135">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="e2718-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-136">Pattern</span></span>

<span data-ttu-id="e2718-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-137">11 digits:</span></span>
  
- <span data-ttu-id="e2718-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-138">Two digits</span></span>
    
- <span data-ttu-id="e2718-139">Un « 0 » ou « 1 »</span><span class="sxs-lookup"><span data-stu-id="e2718-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="e2718-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="e2718-140">One digit</span></span>
    
- <span data-ttu-id="e2718-141">Un « 0 » ou « 1 » ou « 2 » ou « 3 »</span><span class="sxs-lookup"><span data-stu-id="e2718-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="e2718-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-143">Checksum</span></span>

<span data-ttu-id="e2718-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-145">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-145">Definition</span></span>

<span data-ttu-id="e2718-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-147">L’expression régulière `Regex_belgium_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-148">Un mot clé à partir de `Keywords_belgium_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-149">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="e2718-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-151">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-151">tax number</span></span>
  
<span data-ttu-id="e2718-152">numéro national d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="e2718-152">national registration number</span></span>
  
<span data-ttu-id="e2718-153">numéro d’enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-153">tax registration number</span></span>
  
<span data-ttu-id="e2718-154">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-154">tax id</span></span>
  
<span data-ttu-id="e2718-155">NIF</span><span class="sxs-lookup"><span data-stu-id="e2718-155">nif</span></span>
  
<span data-ttu-id="e2718-156">NIF #</span><span class="sxs-lookup"><span data-stu-id="e2718-156">nif#</span></span>
  
<span data-ttu-id="e2718-157">numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="e2718-157">numéro de registre national</span></span>
  
<span data-ttu-id="e2718-158">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="e2718-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="e2718-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="e2718-160">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-160">Format</span></span>

<span data-ttu-id="e2718-161">Dix chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="e2718-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-162">Pattern</span></span>

<span data-ttu-id="e2718-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-164">Checksum</span></span>

<span data-ttu-id="e2718-165">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-166">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-166">Definition</span></span>

<span data-ttu-id="e2718-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-168">La fonction `Func_bulgaria_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-169">Un mot clé à partir de `Keywords_bulgaria_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-171">La fonction `Func_bulgaria_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-172">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="e2718-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-174">bucn</span><span class="sxs-lookup"><span data-stu-id="e2718-174">bucn</span></span>
  
<span data-ttu-id="e2718-175">nombre civile uniforme</span><span class="sxs-lookup"><span data-stu-id="e2718-175">uniform civil number</span></span>
  
<span data-ttu-id="e2718-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="e2718-176">bucn#</span></span>
  
<span data-ttu-id="e2718-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="e2718-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="e2718-178">id civile uniforme</span><span class="sxs-lookup"><span data-stu-id="e2718-178">uniform civil id</span></span>
  
<span data-ttu-id="e2718-179">no civile uniforme</span><span class="sxs-lookup"><span data-stu-id="e2718-179">uniform civil no</span></span>
  
<span data-ttu-id="e2718-180">egn</span><span class="sxs-lookup"><span data-stu-id="e2718-180">egn</span></span>
  
<span data-ttu-id="e2718-181">nombre de civile uniform bulgare</span><span class="sxs-lookup"><span data-stu-id="e2718-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="e2718-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="e2718-182">uniformcivilno#</span></span>
  
<span data-ttu-id="e2718-183">egn #</span><span class="sxs-lookup"><span data-stu-id="e2718-183">egn#</span></span>
  
<span data-ttu-id="e2718-184">УНИФОРМ ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="e2718-184">униформ граждански номер</span></span>
  
<span data-ttu-id="e2718-185">Id униформ</span><span class="sxs-lookup"><span data-stu-id="e2718-185">униформ id</span></span>
  
<span data-ttu-id="e2718-186">Id граждански униформ</span><span class="sxs-lookup"><span data-stu-id="e2718-186">униформ граждански id</span></span>
  
<span data-ttu-id="e2718-187">УНИФОРМ ГРАЖДАНСКИ НЕ</span><span class="sxs-lookup"><span data-stu-id="e2718-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="e2718-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="e2718-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="e2718-189">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-189">Format</span></span>

<span data-ttu-id="e2718-190">11 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-191">Pattern</span></span>

<span data-ttu-id="e2718-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-192">11 digits:</span></span>
  
- <span data-ttu-id="e2718-193">Dix chiffres, choisis au hasard</span><span class="sxs-lookup"><span data-stu-id="e2718-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="e2718-194">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-195">Checksum</span></span>

<span data-ttu-id="e2718-196">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-197">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-197">Definition</span></span>

<span data-ttu-id="e2718-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-199">La fonction `Func_croatia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-200">Un mot clé à partir de `Keywords_croatia_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-202">La fonction `Func_croatia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-203">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="e2718-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-205">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-205">tax number</span></span>
  
<span data-ttu-id="e2718-206">taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-206">tax</span></span>
  
<span data-ttu-id="e2718-207">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-207">tax id</span></span>
  
<span data-ttu-id="e2718-208">OID</span><span class="sxs-lookup"><span data-stu-id="e2718-208">oid</span></span>
  
<span data-ttu-id="e2718-209">OID #</span><span class="sxs-lookup"><span data-stu-id="e2718-209">oid#</span></span>
  
<span data-ttu-id="e2718-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="e2718-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="e2718-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="e2718-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="e2718-212">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-212">Format</span></span>

<span data-ttu-id="e2718-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-214">Pattern</span></span>

<span data-ttu-id="e2718-215">Huit chiffres et une lettre :</span><span class="sxs-lookup"><span data-stu-id="e2718-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="e2718-216">UN « 0 »</span><span class="sxs-lookup"><span data-stu-id="e2718-216">A "0"</span></span> 
    
- <span data-ttu-id="e2718-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-217">Seven digits</span></span>
    
- <span data-ttu-id="e2718-218">Une lettre (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-219">Checksum</span></span>

<span data-ttu-id="e2718-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-221">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-221">Definition</span></span>

<span data-ttu-id="e2718-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-223">La fonction `Func_cyprus_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-224">Un mot clé à partir de `Keywords_cyprus_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-226">La fonction `Func_cyprus_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-227">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="e2718-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-229">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-229">tax number</span></span>
  
<span data-ttu-id="e2718-230">taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-230">tax</span></span>
  
<span data-ttu-id="e2718-231">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-231">tax id</span></span>
  
<span data-ttu-id="e2718-232">codes d’identification</span><span class="sxs-lookup"><span data-stu-id="e2718-232">tax identification code</span></span>
  
<span data-ttu-id="e2718-233">TIC</span><span class="sxs-lookup"><span data-stu-id="e2718-233">tic</span></span>
  
<span data-ttu-id="e2718-234">TIC #</span><span class="sxs-lookup"><span data-stu-id="e2718-234">tic#</span></span>
  
<span data-ttu-id="e2718-235">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="e2718-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="e2718-236">ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ</span><span class="sxs-lookup"><span data-stu-id="e2718-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="e2718-237">ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="e2718-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="e2718-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="e2718-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="e2718-239">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-239">Format</span></span>

<span data-ttu-id="e2718-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="e2718-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-241">Pattern</span></span>

<span data-ttu-id="e2718-242">Neuf ou dix chiffres avec un backslashl facultatif :</span><span class="sxs-lookup"><span data-stu-id="e2718-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="e2718-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-243">Six digits</span></span> 
    
- <span data-ttu-id="e2718-244">Une barre oblique inverse (facultative)</span><span class="sxs-lookup"><span data-stu-id="e2718-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="e2718-245">Trois ou quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-246">Checksum</span></span>

<span data-ttu-id="e2718-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-248">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-248">Definition</span></span>

<span data-ttu-id="e2718-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-250">L’expression régulière `Regex_czech_republic_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-251">Un mot clé à partir de `Keywords_czech_republic_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-252">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="e2718-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-254">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-254">tax number</span></span>
  
<span data-ttu-id="e2718-255">taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-255">tax</span></span>
  
<span data-ttu-id="e2718-256">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-256">tax id</span></span>
  
<span data-ttu-id="e2718-257">numéro de téléphone personnel</span><span class="sxs-lookup"><span data-stu-id="e2718-257">personal number</span></span>
  
<span data-ttu-id="e2718-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="e2718-258">daňové číslo</span></span>
  
<span data-ttu-id="e2718-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="e2718-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="e2718-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="e2718-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="e2718-261">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-261">Format</span></span>

<span data-ttu-id="e2718-262">Dix chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="e2718-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-263">Pattern</span></span>

<span data-ttu-id="e2718-264">Dix chiffres contenant un hyphenl :</span><span class="sxs-lookup"><span data-stu-id="e2718-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="e2718-265">Six chiffres qui correspondent à la date de naissance (jjmmaa)</span><span class="sxs-lookup"><span data-stu-id="e2718-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="e2718-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="e2718-266">A hyphen</span></span>
    
- <span data-ttu-id="e2718-267">Quatre chiffres qui correspondent à un numéro de séquence où le premier chiffre correspond à la century de naissance et le dernier chiffre correspond au sexe de la personne (impaire pour masculin et même femme)</span><span class="sxs-lookup"><span data-stu-id="e2718-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-268">Checksum</span></span>

<span data-ttu-id="e2718-269">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-270">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-270">Definition</span></span>

<span data-ttu-id="e2718-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-272">La fonction `Func_denmark_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-273">Un mot clé à partir de `Keywords_denmark_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-275">La fonction `Func_denmark_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-276">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="e2718-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-278">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-278">tax number</span></span>
  
<span data-ttu-id="e2718-279">taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-279">tax</span></span>
  
<span data-ttu-id="e2718-280">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-280">tax id</span></span>
  
<span data-ttu-id="e2718-281">nombre de CPR</span><span class="sxs-lookup"><span data-stu-id="e2718-281">cpr number</span></span>
  
<span data-ttu-id="e2718-282">CPR #</span><span class="sxs-lookup"><span data-stu-id="e2718-282">cpr#</span></span>
  
<span data-ttu-id="e2718-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="e2718-283">skat nummer</span></span>
  
<span data-ttu-id="e2718-284">id skat</span><span class="sxs-lookup"><span data-stu-id="e2718-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="e2718-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="e2718-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="e2718-286">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-286">Format</span></span>

<span data-ttu-id="e2718-287">11 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-288">Pattern</span></span>

<span data-ttu-id="e2718-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-289">11 digits:</span></span>
  
-  <span data-ttu-id="e2718-290">Un chiffre correspondant au sexe et century de naissance où un nombre impair indique masculin et le nombre pair femme comme suit : 1, 2 pour le 19 century ; 3, 4 pour le vingtième century ; 5 et 6 pour le century 21</span><span class="sxs-lookup"><span data-stu-id="e2718-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="e2718-291">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e2718-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="e2718-292">Trois chiffres qui correspondent à un numéro de série en séparant les personnes naissance à la même date</span><span class="sxs-lookup"><span data-stu-id="e2718-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="e2718-293">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-294">Checksum</span></span>

<span data-ttu-id="e2718-295">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-296">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-296">Definition</span></span>

<span data-ttu-id="e2718-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-298">La fonction `Func_estonia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-299">Un mot clé à partir de `Keywords_estonia_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-301">La fonction `Func_estonia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-302">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="e2718-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-304">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-304">tax number</span></span>
  
<span data-ttu-id="e2718-305">taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-305">tax</span></span>
  
<span data-ttu-id="e2718-306">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-306">tax id</span></span>
  
<span data-ttu-id="e2718-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="e2718-307">personal code</span></span>
  
<span data-ttu-id="e2718-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="e2718-308">maksunumber</span></span>
  
<span data-ttu-id="e2718-309">id maksu</span><span class="sxs-lookup"><span data-stu-id="e2718-309">maksu id</span></span>
  
<span data-ttu-id="e2718-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="e2718-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="e2718-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="e2718-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="e2718-312">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-312">Format</span></span>

<span data-ttu-id="e2718-313">Une combinaison de caractères 11 chiffres, des lettres, et plus et moins</span><span class="sxs-lookup"><span data-stu-id="e2718-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-314">Pattern</span></span>

<span data-ttu-id="e2718-315">Une combinaison de caractères 11 chiffres, des lettres, et plus et moins :</span><span class="sxs-lookup"><span data-stu-id="e2718-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="e2718-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-316">Six digits</span></span>
    
- <span data-ttu-id="e2718-317">Un des éléments suivants : un signe plus, un signe moins ou la lettre « A » (pas la casse) où le signe signifie naissance entre 1800-1899, le signe moins signer signifie naissance entre 1900 à 1999 et « A » signifie naissance 2000 et après</span><span class="sxs-lookup"><span data-stu-id="e2718-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="e2718-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-318">Three digits</span></span>
    
- <span data-ttu-id="e2718-319">Une lettre ou un numéro</span><span class="sxs-lookup"><span data-stu-id="e2718-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-320">Checksum</span></span>

<span data-ttu-id="e2718-321">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-322">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-322">Definition</span></span>

<span data-ttu-id="e2718-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-324">La fonction `Func_finland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-325">Un mot clé à partir de `Keywords_finland_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-327">La fonction `Func_finland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-328">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="e2718-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-330">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="e2718-330">identification number</span></span>
  
<span data-ttu-id="e2718-331">identifiant personnel</span><span class="sxs-lookup"><span data-stu-id="e2718-331">personal id</span></span>
  
<span data-ttu-id="e2718-332">numéro d’identité</span><span class="sxs-lookup"><span data-stu-id="e2718-332">identity number</span></span>
  
<span data-ttu-id="e2718-333">numéro d’id national Finlande</span><span class="sxs-lookup"><span data-stu-id="e2718-333">finnish national id number</span></span>
  
<span data-ttu-id="e2718-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e2718-334">personalidnumber#</span></span>
  
<span data-ttu-id="e2718-335">numéro d’identification nationale</span><span class="sxs-lookup"><span data-stu-id="e2718-335">national identification number</span></span>
  
<span data-ttu-id="e2718-336">numéro d’identification</span><span class="sxs-lookup"><span data-stu-id="e2718-336">id number</span></span>
  
<span data-ttu-id="e2718-337">id national aucun.</span><span class="sxs-lookup"><span data-stu-id="e2718-337">national id no.</span></span>
  
<span data-ttu-id="e2718-338">numéro national</span><span class="sxs-lookup"><span data-stu-id="e2718-338">national id number</span></span>
  
<span data-ttu-id="e2718-339">ID d’aucun</span><span class="sxs-lookup"><span data-stu-id="e2718-339">id no</span></span>
  
<span data-ttu-id="e2718-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e2718-340">tunnistenumero</span></span>
  
<span data-ttu-id="e2718-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e2718-341">henkilötunnus</span></span>
  
<span data-ttu-id="e2718-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e2718-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="e2718-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="e2718-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="e2718-344">numero identiteetti</span><span class="sxs-lookup"><span data-stu-id="e2718-344">identiteetti numero</span></span>
  
<span data-ttu-id="e2718-345">Suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e2718-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="e2718-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="e2718-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="e2718-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e2718-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="e2718-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="e2718-348">tunnusnumero</span></span>
  
<span data-ttu-id="e2718-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="e2718-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="e2718-350">France</span><span class="sxs-lookup"><span data-stu-id="e2718-350">France</span></span>

### <a name="format"></a><span data-ttu-id="e2718-351">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-351">Format</span></span>

<span data-ttu-id="e2718-352">13 chiffres pour les particuliers et les neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="e2718-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-353">Pattern</span></span>

<span data-ttu-id="e2718-354">13 chiffres pour les personnes :</span><span class="sxs-lookup"><span data-stu-id="e2718-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="e2718-355">Un chiffre doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="e2718-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="e2718-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-356">12 digits</span></span>
    
<span data-ttu-id="e2718-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="e2718-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-358">Checksum</span></span>

<span data-ttu-id="e2718-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-360">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-360">Definition</span></span>

<span data-ttu-id="e2718-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-362">La fonction `Func_france_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-363">Un mot clé à partir de `Keywords_france_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-365">La fonction `Func_france_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-366">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="e2718-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-368">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-368">tax identification number</span></span>
  
<span data-ttu-id="e2718-369">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-369">tax number</span></span>
  
<span data-ttu-id="e2718-370">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-370">tax id</span></span>
  
<span data-ttu-id="e2718-371">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="e2718-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="e2718-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="e2718-373">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-373">Format</span></span>

<span data-ttu-id="e2718-374">11 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="e2718-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-375">Pattern</span></span>

<span data-ttu-id="e2718-376">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-376">11 digits :</span></span>
  
-  <span data-ttu-id="e2718-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-377">Ten digits</span></span> 
    
- <span data-ttu-id="e2718-378">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-379">Checksum</span></span>

<span data-ttu-id="e2718-380">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-381">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-381">Definition</span></span>

<span data-ttu-id="e2718-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-383">La fonction `Func_germany_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-384">Un mot clé à partir de `Keywords_germany_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-386">La fonction `Func_germany_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="e2718-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-389">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-389">tax number</span></span>
  
<span data-ttu-id="e2718-390">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-390">tax no.</span></span>
  
<span data-ttu-id="e2718-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-391">taxno#</span></span>
  
<span data-ttu-id="e2718-392">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-392">taxnumber#</span></span>
  
<span data-ttu-id="e2718-393">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-393">taxnumber</span></span>
  
<span data-ttu-id="e2718-394">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-394">tax id</span></span>
  
<span data-ttu-id="e2718-395">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-395">taxid#</span></span>
  
<span data-ttu-id="e2718-396">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-396">tax identification number</span></span>
  
<span data-ttu-id="e2718-397">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-397">tax identification no.</span></span>
  
<span data-ttu-id="e2718-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="e2718-398">steuernummer</span></span>
  
<span data-ttu-id="e2718-399">id steuer</span><span class="sxs-lookup"><span data-stu-id="e2718-399">steuer id</span></span>
  
<span data-ttu-id="e2718-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e2718-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="e2718-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="e2718-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="e2718-402">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-402">Format</span></span>

<span data-ttu-id="e2718-403">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="e2718-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-404">Pattern</span></span>

<span data-ttu-id="e2718-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-406">Checksum</span></span>

<span data-ttu-id="e2718-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-408">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-408">Definition</span></span>

<span data-ttu-id="e2718-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-410">L’expression régulière `Regex_greece_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-411">Un mot clé à partir de `Keywords_greece_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-412">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="e2718-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-414">AFM</span><span class="sxs-lookup"><span data-stu-id="e2718-414">afm</span></span>
  
<span data-ttu-id="e2718-415">tin
</span><span class="sxs-lookup"><span data-stu-id="e2718-415">tin</span></span>
  
<span data-ttu-id="e2718-416">id de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-416">tax id no.</span></span>
  
<span data-ttu-id="e2718-417">id de taxe ne</span><span class="sxs-lookup"><span data-stu-id="e2718-417">tax id no</span></span>
  
<span data-ttu-id="e2718-418">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-418">tax identification number</span></span>
  
<span data-ttu-id="e2718-419">numéro de Registre de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-419">tax registry number</span></span>
  
<span data-ttu-id="e2718-420">taxe non dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="e2718-420">tax registry no.</span></span>
  
<span data-ttu-id="e2718-421">AFM #</span><span class="sxs-lookup"><span data-stu-id="e2718-421">afm#</span></span>
  
<span data-ttu-id="e2718-422">numéro d’identification #</span><span class="sxs-lookup"><span data-stu-id="e2718-422">tin#</span></span>
  
<span data-ttu-id="e2718-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="e2718-423">taxidno#</span></span>
  
<span data-ttu-id="e2718-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="e2718-424">taxregistryno#</span></span>
  
<span data-ttu-id="e2718-425">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="e2718-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="e2718-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="e2718-426">aφμ</span></span>
  
<span data-ttu-id="e2718-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="e2718-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="e2718-428">ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.</span><span class="sxs-lookup"><span data-stu-id="e2718-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="e2718-429">ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="e2718-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="e2718-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="e2718-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e2718-431">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-431">Format</span></span>

<span data-ttu-id="e2718-432">Dix chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-433">Pattern</span></span>

<span data-ttu-id="e2718-434">Dix chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-434">Ten digits:</span></span>
  
-  <span data-ttu-id="e2718-435">Un chiffre doit être « 8 »</span><span class="sxs-lookup"><span data-stu-id="e2718-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="e2718-436">Cinq chiffres qui correspondent au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="e2718-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="e2718-437">Trois chiffres correspondant au numéro généré par hasard pour différencier les personnes naissance le même jour</span><span class="sxs-lookup"><span data-stu-id="e2718-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="e2718-438">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-439">Checksum</span></span>

<span data-ttu-id="e2718-440">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-441">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-441">Definition</span></span>

<span data-ttu-id="e2718-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-443">La fonction `Func_hungary_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-444">Un mot clé à partir de `Keywords_hungary_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-446">La fonction `Func_hungary_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-447">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="e2718-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-449">numéro d’identification fiscale hongrois</span><span class="sxs-lookup"><span data-stu-id="e2718-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="e2718-450">numéro d’identification hongrois</span><span class="sxs-lookup"><span data-stu-id="e2718-450">hungarian tin</span></span>
  
<span data-ttu-id="e2718-451">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-451">tax id number</span></span>
  
<span data-ttu-id="e2718-452">numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="e2718-452">vat number</span></span>
  
<span data-ttu-id="e2718-453">fiscale ne</span><span class="sxs-lookup"><span data-stu-id="e2718-453">tax authority no</span></span>
  
<span data-ttu-id="e2718-454">numéro d’identité Tax id taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-454">tax id tax identity number</span></span>
  
<span data-ttu-id="e2718-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="e2718-455">taxidnumber#</span></span>
  
<span data-ttu-id="e2718-456">numéro d’identification #</span><span class="sxs-lookup"><span data-stu-id="e2718-456">tin#</span></span>
  
<span data-ttu-id="e2718-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="e2718-457">hungatiantin#</span></span>
  
<span data-ttu-id="e2718-458">identification de taxe ne</span><span class="sxs-lookup"><span data-stu-id="e2718-458">tax identification no</span></span>
  
<span data-ttu-id="e2718-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="e2718-459">taxidno#</span></span>
  
<span data-ttu-id="e2718-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="e2718-460">adóazonosító szám</span></span>
  
<span data-ttu-id="e2718-461">adószám</span><span class="sxs-lookup"><span data-stu-id="e2718-461">adószám</span></span>
  
<span data-ttu-id="e2718-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="e2718-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="e2718-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="e2718-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="e2718-464">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-464">Format</span></span>

<span data-ttu-id="e2718-465">Sept chiffres suivies d’une lettre sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-466">Pattern</span></span>

<span data-ttu-id="e2718-467">Sept chiffres suivies d’une lettre :</span><span class="sxs-lookup"><span data-stu-id="e2718-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="e2718-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-468">Seven digits</span></span> 
    
- <span data-ttu-id="e2718-469">Une lettre (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-470">Checksum</span></span>

<span data-ttu-id="e2718-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-472">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-472">Definition</span></span>

<span data-ttu-id="e2718-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-474">La fonction `Func_ireland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-475">Un mot clé à partir de `Keywords_ireland_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-477">La fonction `Func_ireland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="e2718-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-480">service public aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-480">public service no</span></span>
  
<span data-ttu-id="e2718-481">service public personnel aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-481">personal public service no</span></span>
  
<span data-ttu-id="e2718-482">PPS aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-482">pps no</span></span>
  
<span data-ttu-id="e2718-483">personnel n° de service</span><span class="sxs-lookup"><span data-stu-id="e2718-483">personal service no</span></span>
  
<span data-ttu-id="e2718-484">n° du service PPS</span><span class="sxs-lookup"><span data-stu-id="e2718-484">pps service no</span></span>
  
<span data-ttu-id="e2718-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="e2718-485">ppsno#</span></span>
  
<span data-ttu-id="e2718-486">irlandais pps aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-486">irish pps no</span></span>
  
<span data-ttu-id="e2718-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="e2718-487">publicserviceno#</span></span>
  
<span data-ttu-id="e2718-488">numéro personnel service public</span><span class="sxs-lookup"><span data-stu-id="e2718-488">personal public service number</span></span>
  
<span data-ttu-id="e2718-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="e2718-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="e2718-490">uimh PPS</span><span class="sxs-lookup"><span data-stu-id="e2718-490">pps uimh</span></span>
  
<span data-ttu-id="e2718-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="e2718-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="e2718-492">Italie</span><span class="sxs-lookup"><span data-stu-id="e2718-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="e2718-493">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-493">Format</span></span>

<span data-ttu-id="e2718-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-495">Pattern</span></span>

<span data-ttu-id="e2718-496">16 lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="e2718-497">Trois lettres qui correspondent aux trois premiers consonnes suivantes dans le nom de famille</span><span class="sxs-lookup"><span data-stu-id="e2718-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="e2718-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes dans le premier nom</span><span class="sxs-lookup"><span data-stu-id="e2718-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="e2718-499">Deux chiffres qui correspondent à la dernière chiffres de l’année de naissance</span><span class="sxs-lookup"><span data-stu-id="e2718-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="e2718-500">Un chiffre qui correspond au mois de naissance — lettres sont utilisés dans l’ordre alphabétique, mais que les lettres A à E, H, L, M, P, R t sont utilisés (par conséquent, janvier correspond à un et octobre est R)</span><span class="sxs-lookup"><span data-stu-id="e2718-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="e2718-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté à la journée de naissance pour femelles différencier les mâles</span><span class="sxs-lookup"><span data-stu-id="e2718-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="e2718-502">Quatre chiffres qui correspondent à un code de zone spécifique à la commune où naissance de la personne, les codes de pays échelle sont utilisés pour étranger</span><span class="sxs-lookup"><span data-stu-id="e2718-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="e2718-503">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-504">Checksum</span></span>

<span data-ttu-id="e2718-505">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-506">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-506">Definition</span></span>

<span data-ttu-id="e2718-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-508">La fonction `Func_italy_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-509">Un mot clé à partir de `Keywords_italy_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-511">La fonction `Func_italy_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-512">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="e2718-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-514">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-514">tax number</span></span>
  
<span data-ttu-id="e2718-515">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-515">tax no.</span></span>
  
<span data-ttu-id="e2718-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-516">taxno#</span></span>
  
<span data-ttu-id="e2718-517">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-517">taxnumber#</span></span>
  
<span data-ttu-id="e2718-518">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-518">taxnumber</span></span>
  
<span data-ttu-id="e2718-519">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-519">tax id</span></span>
  
<span data-ttu-id="e2718-520">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-520">taxid#</span></span>
  
<span data-ttu-id="e2718-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-521">fiscal code</span></span>
  
<span data-ttu-id="e2718-522">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="e2718-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="e2718-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="e2718-524">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-524">Format</span></span>

<span data-ttu-id="e2718-525">11 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-526">Pattern</span></span>

<span data-ttu-id="e2718-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="e2718-528">Six chiffres qui correspondent à la date de naissance (jjmmaa)</span><span class="sxs-lookup"><span data-stu-id="e2718-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="e2718-529">Un chiffre qui correspond à la century de naissance où « 0 » correspond à 19 century, « 1 » correspond à 20 century et « 2 » correspond à century 21</span><span class="sxs-lookup"><span data-stu-id="e2718-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="e2718-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-531">Checksum</span></span>

<span data-ttu-id="e2718-532">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-533">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-533">Definition</span></span>

<span data-ttu-id="e2718-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-535">La fonction `Func_latvia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-536">Un mot clé à partir de `Keywords_latvia_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-538">La fonction `Func_latvia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-539">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="e2718-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-541">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-541">tax number</span></span>
  
<span data-ttu-id="e2718-542">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-542">tax no.</span></span>
  
<span data-ttu-id="e2718-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-543">taxno#</span></span>
  
<span data-ttu-id="e2718-544">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-544">taxnumber#</span></span>
  
<span data-ttu-id="e2718-545">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-545">taxnumber</span></span>
  
<span data-ttu-id="e2718-546">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-546">tax id</span></span>
  
<span data-ttu-id="e2718-547">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-547">taxid#</span></span>
  
<span data-ttu-id="e2718-548">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-548">tax identification number</span></span>
  
<span data-ttu-id="e2718-549">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-549">tax identification no.</span></span>
  
<span data-ttu-id="e2718-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="e2718-550">nodokļa numurs</span></span>
  
<span data-ttu-id="e2718-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="e2718-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="e2718-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="e2718-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="e2718-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="e2718-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="e2718-554">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-554">Format</span></span>

<span data-ttu-id="e2718-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-556">Pattern</span></span>

<span data-ttu-id="e2718-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-558">Checksum</span></span>

<span data-ttu-id="e2718-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-560">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-560">Definition</span></span>

<span data-ttu-id="e2718-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-562">La fonction `Func_lithuania_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-563">Un mot clé à partir de `Keywords_lithuania_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-565">La fonction `Func_lithuania_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="e2718-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-568">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-568">tax number</span></span>
  
<span data-ttu-id="e2718-569">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-569">tax no.</span></span>
  
<span data-ttu-id="e2718-570">fiscales no #</span><span class="sxs-lookup"><span data-stu-id="e2718-570">tax no#</span></span>
  
<span data-ttu-id="e2718-571">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-571">taxnumber#</span></span>
  
<span data-ttu-id="e2718-572">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-572">taxnumber</span></span>
  
<span data-ttu-id="e2718-573">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-573">tax id</span></span>
  
<span data-ttu-id="e2718-574">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-574">taxid#</span></span>
  
<span data-ttu-id="e2718-575">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-575">tax identification number</span></span>
  
<span data-ttu-id="e2718-576">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-576">tax identification no.</span></span>
  
<span data-ttu-id="e2718-577">id mokesčių</span><span class="sxs-lookup"><span data-stu-id="e2718-577">mokesčių id</span></span>
  
<span data-ttu-id="e2718-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="e2718-578">mokesčių numeris</span></span>
  
<span data-ttu-id="e2718-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="e2718-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="e2718-580">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="e2718-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="e2718-581">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-581">Format</span></span>

<span data-ttu-id="e2718-582">13 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-583">Pattern</span></span>

<span data-ttu-id="e2718-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="e2718-584">13 digits:</span></span>
  
-  <span data-ttu-id="e2718-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-585">11 digits</span></span> 
    
- <span data-ttu-id="e2718-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-587">Checksum</span></span>

<span data-ttu-id="e2718-588">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-589">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-589">Definition</span></span>

<span data-ttu-id="e2718-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-591">La fonction `Func_luxemburg_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-592">Un mot clé à partir de `Keywords_luxemburg_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-594">La fonction `Func_luxemburg_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-595">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="e2718-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-597">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-597">tax number</span></span>
  
<span data-ttu-id="e2718-598">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-598">tax no.</span></span>
  
<span data-ttu-id="e2718-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-599">taxno#</span></span>
  
<span data-ttu-id="e2718-600">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-600">taxnumber#</span></span>
  
<span data-ttu-id="e2718-601">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-601">taxnumber</span></span>
  
<span data-ttu-id="e2718-602">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-602">tax id</span></span>
  
<span data-ttu-id="e2718-603">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-603">taxid#</span></span>
  
<span data-ttu-id="e2718-604">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-604">tax identification number</span></span>
  
<span data-ttu-id="e2718-605">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-605">tax identification no.</span></span>
  
<span data-ttu-id="e2718-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="e2718-606">steuernummer</span></span>
  
<span data-ttu-id="e2718-607">id steuer</span><span class="sxs-lookup"><span data-stu-id="e2718-607">steuer id</span></span>
  
<span data-ttu-id="e2718-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e2718-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="e2718-609">Malte</span><span class="sxs-lookup"><span data-stu-id="e2718-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="e2718-610">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-610">Format</span></span>

<span data-ttu-id="e2718-611">Pour maltaise nationaux : 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="e2718-612">Non-maltaise nationaux et les entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-613">Pattern</span></span>

<span data-ttu-id="e2718-614">Maltais nationaux : 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="e2718-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="e2718-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-615">Seven digits</span></span> 
    
- <span data-ttu-id="e2718-616">Une lettre (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="e2718-617">Non-maltaise nationaux et les entités maltaises : 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="e2718-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e2718-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-619">Checksum</span></span>

<span data-ttu-id="e2718-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-621">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-621">Definition</span></span>

<span data-ttu-id="e2718-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-623">La fonction `Func_malta_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-624">Un mot clé à partir de `Keywords_malta_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-626">La fonction `Func_malta_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-627">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="e2718-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-629">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-629">tax number</span></span>
  
<span data-ttu-id="e2718-630">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-630">tax no.</span></span>
  
<span data-ttu-id="e2718-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-631">taxno#</span></span>
  
<span data-ttu-id="e2718-632">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-632">taxnumber#</span></span>
  
<span data-ttu-id="e2718-633">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-633">taxnumber</span></span>
  
<span data-ttu-id="e2718-634">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-634">tax id</span></span>
  
<span data-ttu-id="e2718-635">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-635">taxid#</span></span>
  
<span data-ttu-id="e2718-636">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-636">tax identification number</span></span>
  
<span data-ttu-id="e2718-637">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-637">tax identification no.</span></span>
  
<span data-ttu-id="e2718-638">tat-taxxa numru</span><span class="sxs-lookup"><span data-stu-id="e2718-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="e2718-639">ID tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="e2718-639">id tat-taxxa</span></span>
  
<span data-ttu-id="e2718-640">numru ta ' identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="e2718-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="e2718-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="e2718-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="e2718-642">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-642">Format</span></span>

<span data-ttu-id="e2718-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-644">Pattern</span></span>

<span data-ttu-id="e2718-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="e2718-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-646">Checksum</span></span>

<span data-ttu-id="e2718-647">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-648">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-648">Definition</span></span>

<span data-ttu-id="e2718-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-650">La fonction `Func_netherlands_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-651">Un mot clé à partir de `Keywords_netherlands_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-653">La fonction `Func_netherlands_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-654">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="e2718-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-656">numéro d’identification fiscale pays-bas</span><span class="sxs-lookup"><span data-stu-id="e2718-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="e2718-657">identification de taxe pays-bas</span><span class="sxs-lookup"><span data-stu-id="e2718-657">netherlands tax identification</span></span>
  
<span data-ttu-id="e2718-658">numéro d’identification du Antilles taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="e2718-659">identification de taxe du Antilles</span><span class="sxs-lookup"><span data-stu-id="e2718-659">netherland's tax identification</span></span>
  
<span data-ttu-id="e2718-660">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-660">tax identification number</span></span>
  
<span data-ttu-id="e2718-661">id de taxe néerlandais</span><span class="sxs-lookup"><span data-stu-id="e2718-661">dutch tax id</span></span>
  
<span data-ttu-id="e2718-662">numéro d’identification fiscale néerlandais</span><span class="sxs-lookup"><span data-stu-id="e2718-662">dutch tax identification number</span></span>
  
<span data-ttu-id="e2718-663">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-663">tax id</span></span>
  
<span data-ttu-id="e2718-664">n° de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e2718-664">tax id#</span></span>
  
<span data-ttu-id="e2718-665">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-665">tax number</span></span>
  
<span data-ttu-id="e2718-666">fiscales no #</span><span class="sxs-lookup"><span data-stu-id="e2718-666">tax no#</span></span>
  
<span data-ttu-id="e2718-667">taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-667">tax#</span></span>
  
<span data-ttu-id="e2718-668">tin
</span><span class="sxs-lookup"><span data-stu-id="e2718-668">tin</span></span>
  
<span data-ttu-id="e2718-669">numéro d’identification #</span><span class="sxs-lookup"><span data-stu-id="e2718-669">tin#</span></span>
  
<span data-ttu-id="e2718-670">numéro d’identification pays-bas</span><span class="sxs-lookup"><span data-stu-id="e2718-670">netherlands tin</span></span>
  
<span data-ttu-id="e2718-671">numéro d’identification du Antilles</span><span class="sxs-lookup"><span data-stu-id="e2718-671">netherland's tin</span></span>
  
<span data-ttu-id="e2718-672">néerlandais Omzetbelasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="e2718-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="e2718-673">identificatienummer van Omzetbelasting</span><span class="sxs-lookup"><span data-stu-id="e2718-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="e2718-674">Omzetbelasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="e2718-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="e2718-675">néerlandais Omzetbelasting identificatie</span><span class="sxs-lookup"><span data-stu-id="e2718-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="e2718-676">néerlandais Omzetbelasting id nummer</span><span class="sxs-lookup"><span data-stu-id="e2718-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="e2718-677">néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="e2718-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="e2718-678">BTW nummer</span><span class="sxs-lookup"><span data-stu-id="e2718-678">btw nummer</span></span>
  
<span data-ttu-id="e2718-679">Nederlandse Omzetbelasting identificatie</span><span class="sxs-lookup"><span data-stu-id="e2718-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="e2718-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="e2718-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="e2718-681">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-681">Format</span></span>

<span data-ttu-id="e2718-682">Onze chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-683">Pattern</span></span>

<span data-ttu-id="e2718-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-685">Checksum</span></span>

<span data-ttu-id="e2718-686">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-687">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-687">Definition</span></span>

<span data-ttu-id="e2718-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-689">La fonction `Func_poland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-690">Un mot clé à partir de `Keywords_poland_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-692">La fonction `Func_poland_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-693">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="e2718-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-695">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-695">tax number</span></span>
  
<span data-ttu-id="e2718-696">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-696">tax no.</span></span>
  
<span data-ttu-id="e2718-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-697">taxno#</span></span>
  
<span data-ttu-id="e2718-698">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-698">taxnumber#</span></span>
  
<span data-ttu-id="e2718-699">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-699">taxnumber</span></span>
  
<span data-ttu-id="e2718-700">point de contact</span><span class="sxs-lookup"><span data-stu-id="e2718-700">nip</span></span>
  
<span data-ttu-id="e2718-701">point de contact #</span><span class="sxs-lookup"><span data-stu-id="e2718-701">nip#</span></span>
  
<span data-ttu-id="e2718-702">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-702">tax id</span></span>
  
<span data-ttu-id="e2718-703">n° de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e2718-703">tax id#</span></span>
  
<span data-ttu-id="e2718-704">id du point de contact</span><span class="sxs-lookup"><span data-stu-id="e2718-704">nip id</span></span>
  
<span data-ttu-id="e2718-705">numéro d’identification de point de contact</span><span class="sxs-lookup"><span data-stu-id="e2718-705">nip id#</span></span>
  
<span data-ttu-id="e2718-706">numéro d’identification fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-706">tax identification number</span></span>
  
<span data-ttu-id="e2718-707">identification de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-707">tax identification no.</span></span>
  
<span data-ttu-id="e2718-708">numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="e2718-708">vat number</span></span>
  
<span data-ttu-id="e2718-709">taxe non.</span><span class="sxs-lookup"><span data-stu-id="e2718-709">vat no.</span></span>
  
<span data-ttu-id="e2718-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="e2718-710">vatno#</span></span>
  
<span data-ttu-id="e2718-711">code de taxes</span><span class="sxs-lookup"><span data-stu-id="e2718-711">vat id</span></span>
  
<span data-ttu-id="e2718-712">numéro d’identification de TVA</span><span class="sxs-lookup"><span data-stu-id="e2718-712">vat id#</span></span>
  
<span data-ttu-id="e2718-713">nombre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="e2718-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="e2718-714">polski nombre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="e2718-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="e2718-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="e2718-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="e2718-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="e2718-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="e2718-717">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-717">Format</span></span>

<span data-ttu-id="e2718-718">Neuf chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-719">Pattern</span></span>

<span data-ttu-id="e2718-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-721">Checksum</span></span>

<span data-ttu-id="e2718-722">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-723">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-723">Definition</span></span>

<span data-ttu-id="e2718-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-725">La fonction `Func_portugal_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-726">Un mot clé à partir de `Keywords_portugal_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-728">La fonction `Func_portugal_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-729">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="e2718-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-731">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-731">tax number</span></span>
  
<span data-ttu-id="e2718-732">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-732">tax no.</span></span>
  
<span data-ttu-id="e2718-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-733">taxno#</span></span>
  
<span data-ttu-id="e2718-734">Numéro taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-734">taxnumber#</span></span>
  
<span data-ttu-id="e2718-735">Numéro taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-735">taxnumber</span></span>
  
<span data-ttu-id="e2718-736">NIF</span><span class="sxs-lookup"><span data-stu-id="e2718-736">nif</span></span>
  
<span data-ttu-id="e2718-737">NIF #</span><span class="sxs-lookup"><span data-stu-id="e2718-737">nif#</span></span>
  
<span data-ttu-id="e2718-738">NUMERO fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-738">numero fiscal</span></span>
  
<span data-ttu-id="e2718-739">Número de identificação fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="e2718-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="e2718-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="e2718-741">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-741">Format</span></span>

<span data-ttu-id="e2718-742">13 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-743">Pattern</span></span>

<span data-ttu-id="e2718-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-745">Checksum</span></span>

<span data-ttu-id="e2718-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-747">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-747">Definition</span></span>

<span data-ttu-id="e2718-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-749">L’expression régulière `Regex_romania_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-750">Un mot clé à partir de `Keywords_romania_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-751">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="e2718-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-753">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-753">tax id</span></span>
  
<span data-ttu-id="e2718-754">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-754">tax id number</span></span>
  
<span data-ttu-id="e2718-755">Aucun fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-755">tax file no</span></span>
  
<span data-ttu-id="e2718-756">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-756">tax file number</span></span>
  
<span data-ttu-id="e2718-757">n° de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-757">tax no</span></span>
  
<span data-ttu-id="e2718-758">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-758">tax number</span></span>
  
<span data-ttu-id="e2718-759">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-759">taxid#</span></span>
  
<span data-ttu-id="e2718-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-760">taxno#</span></span>
  
<span data-ttu-id="e2718-761">ID-ul taxei</span><span class="sxs-lookup"><span data-stu-id="e2718-761">id-ul taxei</span></span>
  
<span data-ttu-id="e2718-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="e2718-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="e2718-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="e2718-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="e2718-764">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-764">Format</span></span>

<span data-ttu-id="e2718-765">10 chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-766">Pattern</span></span>

<span data-ttu-id="e2718-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-768">Checksum</span></span>

<span data-ttu-id="e2718-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="e2718-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-770">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-770">Definition</span></span>

<span data-ttu-id="e2718-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-772">L’expression régulière `Regex_slovakia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-773">Un mot clé à partir de `Keywords_slovakia_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-774">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="e2718-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-776">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-776">tax id</span></span>
  
<span data-ttu-id="e2718-777">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-777">tax id number</span></span>
  
<span data-ttu-id="e2718-778">id d’étain</span><span class="sxs-lookup"><span data-stu-id="e2718-778">tin id</span></span>
  
<span data-ttu-id="e2718-779">no étain</span><span class="sxs-lookup"><span data-stu-id="e2718-779">tin no</span></span>
  
<span data-ttu-id="e2718-780">id d’étain slovaque</span><span class="sxs-lookup"><span data-stu-id="e2718-780">slovakian tin id</span></span>
  
<span data-ttu-id="e2718-781">tin
</span><span class="sxs-lookup"><span data-stu-id="e2718-781">tin</span></span>
  
<span data-ttu-id="e2718-782">Aucun fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-782">tax file no</span></span>
  
<span data-ttu-id="e2718-783">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-783">tax file number</span></span>
  
<span data-ttu-id="e2718-784">n° de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-784">tax no</span></span>
  
<span data-ttu-id="e2718-785">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-785">tax number</span></span>
  
<span data-ttu-id="e2718-786">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-786">taxid#</span></span>
  
<span data-ttu-id="e2718-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-787">taxno#</span></span>
  
<span data-ttu-id="e2718-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="e2718-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="e2718-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="e2718-789">daňové číslo</span></span>
  
<span data-ttu-id="e2718-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="e2718-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="e2718-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="e2718-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="e2718-792">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-792">Format</span></span>

<span data-ttu-id="e2718-793">Huit chiffres sans espaces ni les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="e2718-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-794">Pattern</span></span>

<span data-ttu-id="e2718-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-796">Checksum</span></span>

<span data-ttu-id="e2718-797">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-798">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-798">Definition</span></span>

<span data-ttu-id="e2718-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-800">La fonction `Func_slovenia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-801">Un mot clé à partir de `Keywords_slovenia_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-803">La fonction `Func_slovenia_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-804">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="e2718-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-806">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-806">tax id</span></span>
  
<span data-ttu-id="e2718-807">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-807">tax id number</span></span>
  
<span data-ttu-id="e2718-808">id d’étain</span><span class="sxs-lookup"><span data-stu-id="e2718-808">tin id</span></span>
  
<span data-ttu-id="e2718-809">no étain</span><span class="sxs-lookup"><span data-stu-id="e2718-809">tin no</span></span>
  
<span data-ttu-id="e2718-810">id d’étain slovène</span><span class="sxs-lookup"><span data-stu-id="e2718-810">slovenian tin id</span></span>
  
<span data-ttu-id="e2718-811">tin
</span><span class="sxs-lookup"><span data-stu-id="e2718-811">tin</span></span>
  
<span data-ttu-id="e2718-812">Aucun fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-812">tax file no</span></span>
  
<span data-ttu-id="e2718-813">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-813">tax file number</span></span>
  
<span data-ttu-id="e2718-814">n° de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-814">tax no</span></span>
  
<span data-ttu-id="e2718-815">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-815">tax number</span></span>
  
<span data-ttu-id="e2718-816">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-816">taxid#</span></span>
  
<span data-ttu-id="e2718-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-817">taxno#</span></span>
  
<span data-ttu-id="e2718-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="e2718-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="e2718-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="e2718-819">davčna številka</span></span>
  
<span data-ttu-id="e2718-820">Številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="e2718-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="e2718-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="e2718-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="e2718-822">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-822">Format</span></span>

<span data-ttu-id="e2718-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-824">Pattern</span></span>

<span data-ttu-id="e2718-825">Espagnols personnes physiques avec une carte d’identité National Espagne :</span><span class="sxs-lookup"><span data-stu-id="e2718-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="e2718-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-826">Eight digits</span></span> 
    
- <span data-ttu-id="e2718-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="e2718-828">Spaniards non résident sans une carte d’identité National Espagne</span><span class="sxs-lookup"><span data-stu-id="e2718-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="e2718-829">Une lettre majuscule « L » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="e2718-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-830">Seven digits</span></span>
    
- <span data-ttu-id="e2718-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="e2718-832">Spaniards résident sous l’âge de 14 ans sans un Espagne National carte d’identité :</span><span class="sxs-lookup"><span data-stu-id="e2718-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="e2718-833">Une lettre majuscule « K » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="e2718-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-834">Seven digits</span></span> 
    
- <span data-ttu-id="e2718-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="e2718-836">Étrangers avec numéro d’Identification d’un étranger</span><span class="sxs-lookup"><span data-stu-id="e2718-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="e2718-837">Majuscules une lettre qui est « X », « Y » ou « Z » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="e2718-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-838">Seven digits</span></span>
    
- <span data-ttu-id="e2718-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="e2718-840">Étrangers sans numéro d’Identification d’un étranger</span><span class="sxs-lookup"><span data-stu-id="e2718-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="e2718-841">Une lettre est « M » (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="e2718-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="e2718-842">Seven digits</span></span>
    
- <span data-ttu-id="e2718-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="e2718-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e2718-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-844">Checksum</span></span>

<span data-ttu-id="e2718-845">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-846">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-846">Definition</span></span>

<span data-ttu-id="e2718-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-848">La fonction `Func_spain_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-849">Un mot clé à partir de `Keywords_spain_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-851">La fonction `Func_spain_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-852">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="e2718-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-854">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-854">tax id</span></span>
  
<span data-ttu-id="e2718-855">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-855">tax id number</span></span>
  
<span data-ttu-id="e2718-856">id CIF</span><span class="sxs-lookup"><span data-stu-id="e2718-856">cif id</span></span>
  
<span data-ttu-id="e2718-857">CIF aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-857">cif no</span></span>
  
<span data-ttu-id="e2718-858">id cif espagnol</span><span class="sxs-lookup"><span data-stu-id="e2718-858">spanish cif id</span></span>
  
<span data-ttu-id="e2718-859">CIF</span><span class="sxs-lookup"><span data-stu-id="e2718-859">cif</span></span>
  
<span data-ttu-id="e2718-860">Aucun fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-860">tax file no</span></span>
  
<span data-ttu-id="e2718-861">nombre cif espagnol</span><span class="sxs-lookup"><span data-stu-id="e2718-861">spanish cif number</span></span>
  
<span data-ttu-id="e2718-862">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="e2718-862">tax file number</span></span>
  
<span data-ttu-id="e2718-863">Espagnol cif aucune</span><span class="sxs-lookup"><span data-stu-id="e2718-863">spanish cif no</span></span>
  
<span data-ttu-id="e2718-864">n° de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-864">tax no</span></span>
  
<span data-ttu-id="e2718-865">numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-865">tax number</span></span>
  
<span data-ttu-id="e2718-866">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-866">taxid#</span></span>
  
<span data-ttu-id="e2718-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="e2718-867">taxno#</span></span>
  
<span data-ttu-id="e2718-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="e2718-868">cifid#</span></span>
  
<span data-ttu-id="e2718-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="e2718-869">spanishcifid#</span></span>
  
<span data-ttu-id="e2718-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="e2718-870">spanishcifno#</span></span>
  
<span data-ttu-id="e2718-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="e2718-871">número de contribuyente</span></span>
  
<span data-ttu-id="e2718-872">Número de impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="e2718-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="e2718-873">Número de identificación fiscale</span><span class="sxs-lookup"><span data-stu-id="e2718-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="e2718-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="e2718-874">cif número</span></span>
  
<span data-ttu-id="e2718-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="e2718-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="e2718-876">Suède</span><span class="sxs-lookup"><span data-stu-id="e2718-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="e2718-877">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-877">Format</span></span>

<span data-ttu-id="e2718-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="e2718-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-879">Pattern</span></span>

<span data-ttu-id="e2718-880">Dix chiffres et un symbole :</span><span class="sxs-lookup"><span data-stu-id="e2718-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="e2718-881">Six chiffres qui correspondent à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e2718-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="e2718-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="e2718-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="e2718-883">Trois chiffres qui permettent l’identification numéro unique emplacement :</span><span class="sxs-lookup"><span data-stu-id="e2718-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="e2718-884">Pour les numéros émis avant 1990, le chiffre septième et huitième identifier la région de naissance ou personnes foreign-born</span><span class="sxs-lookup"><span data-stu-id="e2718-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="e2718-885">Indique le chiffre en neuvième position sexe soit impair pour masculin ou même pour femme</span><span class="sxs-lookup"><span data-stu-id="e2718-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="e2718-886">Chiffre un contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e2718-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-887">Checksum</span></span>

<span data-ttu-id="e2718-888">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-889">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-889">Definition</span></span>

<span data-ttu-id="e2718-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-891">La fonction `Func_sweden_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-892">Un mot clé à partir de `Keywords_sweden_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="e2718-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-894">La fonction `Func_sweden_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e2718-895">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="e2718-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-897">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-897">tax id</span></span>
  
<span data-ttu-id="e2718-898">id de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-898">tax id no.</span></span>
  
<span data-ttu-id="e2718-899">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-899">tax id number</span></span>
  
<span data-ttu-id="e2718-900">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="e2718-900">tax identification</span></span>
  
<span data-ttu-id="e2718-901">identification Tax #</span><span class="sxs-lookup"><span data-stu-id="e2718-901">tax identification#</span></span>
  
<span data-ttu-id="e2718-902">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-902">tax no.</span></span>
  
<span data-ttu-id="e2718-903">taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-903">tax#</span></span>
  
<span data-ttu-id="e2718-904">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-904">taxid#</span></span>
  
<span data-ttu-id="e2718-905">fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-905">tax file</span></span>
  
<span data-ttu-id="e2718-906">fiscales aucun fichier.</span><span class="sxs-lookup"><span data-stu-id="e2718-906">tax file no.</span></span>
  
<span data-ttu-id="e2718-907">numéro d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="e2718-907">personal id number</span></span>
  
<span data-ttu-id="e2718-908">skatt id nummer</span><span class="sxs-lookup"><span data-stu-id="e2718-908">skatt id nummer</span></span>
  
<span data-ttu-id="e2718-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="e2718-909">skatt identifikation</span></span>
  
<span data-ttu-id="e2718-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="e2718-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="e2718-911">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="e2718-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="e2718-912">Format</span><span class="sxs-lookup"><span data-stu-id="e2718-912">Format</span></span>

<span data-ttu-id="e2718-913">Référence de contribuable unique (UTR) : 10 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="e2718-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="e2718-p103">Numéro de sécurité sociale (NINO) : Pour plus d’informations, voir la section « britannique assurance nationale nombre (NINO) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e2718-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e2718-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="e2718-916">Pattern</span></span>

<span data-ttu-id="e2718-917">Référence de contribuable unique (UTR) : 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="e2718-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="e2718-p104">Numéro de sécurité sociale (NINO) : Pour plus d’informations, voir la section « britannique assurance nationale nombre (NINO) » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e2718-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e2718-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="e2718-920">Checksum</span></span>

<span data-ttu-id="e2718-921">Oui</span><span class="sxs-lookup"><span data-stu-id="e2718-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e2718-922">Définition</span><span class="sxs-lookup"><span data-stu-id="e2718-922">Definition</span></span>

<span data-ttu-id="e2718-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="e2718-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e2718-924">La fonction `Func_uk_eu_tax_file_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="e2718-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e2718-925">Un mot clé à partir de `Keywords_uk_eu_tax_file_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="e2718-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e2718-926">Keywords</span><span class="sxs-lookup"><span data-stu-id="e2718-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="e2718-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="e2718-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="e2718-928">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="e2718-928">tax id</span></span>
  
<span data-ttu-id="e2718-929">id de taxe ne.</span><span class="sxs-lookup"><span data-stu-id="e2718-929">tax id no.</span></span>
  
<span data-ttu-id="e2718-930">numéro d’identification de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-930">tax id number</span></span>
  
<span data-ttu-id="e2718-931">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="e2718-931">tax identification</span></span>
  
<span data-ttu-id="e2718-932">identification Tax #</span><span class="sxs-lookup"><span data-stu-id="e2718-932">tax identification#</span></span>
  
<span data-ttu-id="e2718-933">n° de taxe.</span><span class="sxs-lookup"><span data-stu-id="e2718-933">tax no.</span></span>
  
<span data-ttu-id="e2718-934">taxe #</span><span class="sxs-lookup"><span data-stu-id="e2718-934">tax#</span></span>
  
<span data-ttu-id="e2718-935">taxid #</span><span class="sxs-lookup"><span data-stu-id="e2718-935">taxid#</span></span>
  
<span data-ttu-id="e2718-936">fichier de taxe</span><span class="sxs-lookup"><span data-stu-id="e2718-936">tax file</span></span>
  
<span data-ttu-id="e2718-937">fiscales aucun fichier.</span><span class="sxs-lookup"><span data-stu-id="e2718-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2718-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2718-938">See also</span></span>

[<span data-ttu-id="e2718-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="e2718-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

