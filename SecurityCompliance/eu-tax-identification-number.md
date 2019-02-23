---
title: Numéro d'identification fiscale de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: Cette rubrique montre ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'il détecte le type d'informations sensibles du numéro d'identification fiscale de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: f851cce4be70fd41c24a7876d97c452f0a738eda
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213824"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="d68a9-104">Numéro d'identification fiscale de l'UE</span><span class="sxs-lookup"><span data-stu-id="d68a9-104">EU Tax Identification Number</span></span>

<span data-ttu-id="d68a9-p102">Cette rubrique montre ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'il détecte le type d'informations sensibles de l'ID taxe de l'UE (TIN). Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="d68a9-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d68a9-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d68a9-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-108">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-108">Format</span></span>

<span data-ttu-id="d68a9-109">Neuf chiffres avec un trait d'union conditionnel et une barre oblique</span><span class="sxs-lookup"><span data-stu-id="d68a9-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-110">Pattern</span></span>

<span data-ttu-id="d68a9-111">Neuf chiffres avec un trait d'Union et une barre oblique facultatifs:</span><span class="sxs-lookup"><span data-stu-id="d68a9-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="d68a9-112">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-112">Two digits</span></span> 
    
- <span data-ttu-id="d68a9-113">Un trait d’union (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d68a9-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="d68a9-114">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-114">Three digits</span></span>
    
- <span data-ttu-id="d68a9-115">Une barre oblique (facultative)</span><span class="sxs-lookup"><span data-stu-id="d68a9-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="d68a9-116">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-117">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-117">Checksum</span></span>

<span data-ttu-id="d68a9-118">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-119">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-119">Definition</span></span>

<span data-ttu-id="d68a9-120">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-121">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-122">Un mot clé `Keywords_austria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-123">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-124">La fonction `Func_austria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-125">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="d68a9-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-127">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-127">tax number</span></span>
  
<span data-ttu-id="d68a9-128">valeur</span><span class="sxs-lookup"><span data-stu-id="d68a9-128">number</span></span>
  
<span data-ttu-id="d68a9-129">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-129">tax registration number</span></span>
  
<span data-ttu-id="d68a9-130">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-130">tax id</span></span>
  
<span data-ttu-id="d68a9-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="d68a9-131">st.nr.</span></span>
  
<span data-ttu-id="d68a9-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="d68a9-133">Belgique</span><span class="sxs-lookup"><span data-stu-id="d68a9-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-134">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-134">Format</span></span>

<span data-ttu-id="d68a9-135">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-136">Pattern</span></span>

<span data-ttu-id="d68a9-137">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d68a9-137">11 digits:</span></span>
  
- <span data-ttu-id="d68a9-138">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-138">Two digits</span></span>
    
- <span data-ttu-id="d68a9-139">«0» ou «1»</span><span class="sxs-lookup"><span data-stu-id="d68a9-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="d68a9-140">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="d68a9-140">One digit</span></span>
    
- <span data-ttu-id="d68a9-141">«0» ou «1» ou «2» ou «3»</span><span class="sxs-lookup"><span data-stu-id="d68a9-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="d68a9-142">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-143">Checksum</span></span>

<span data-ttu-id="d68a9-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-145">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-145">Definition</span></span>

<span data-ttu-id="d68a9-146">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-147">L'expression `Regex_belgium_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-148">Un mot clé `Keywords_belgium_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-149">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="d68a9-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-151">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-151">tax number</span></span>
  
<span data-ttu-id="d68a9-152">Numéro d'enregistrement national</span><span class="sxs-lookup"><span data-stu-id="d68a9-152">national registration number</span></span>
  
<span data-ttu-id="d68a9-153">Numéro d'enregistrement taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-153">tax registration number</span></span>
  
<span data-ttu-id="d68a9-154">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-154">tax id</span></span>
  
<span data-ttu-id="d68a9-155">nPour</span><span class="sxs-lookup"><span data-stu-id="d68a9-155">nif</span></span>
  
<span data-ttu-id="d68a9-156">nPour</span><span class="sxs-lookup"><span data-stu-id="d68a9-156">nif#</span></span>
  
<span data-ttu-id="d68a9-157">Numéro de registre national</span><span class="sxs-lookup"><span data-stu-id="d68a9-157">numéro de registre national</span></span>
  
<span data-ttu-id="d68a9-158">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="d68a9-159">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d68a9-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-160">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-160">Format</span></span>

<span data-ttu-id="d68a9-161">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-162">Pattern</span></span>

<span data-ttu-id="d68a9-163">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-164">Checksum</span></span>

<span data-ttu-id="d68a9-165">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-166">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-166">Definition</span></span>

<span data-ttu-id="d68a9-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-168">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-169">Un mot clé `Keywords_bulgaria_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-170">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-171">La fonction `Func_bulgaria_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-172">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="d68a9-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-174">bucn</span><span class="sxs-lookup"><span data-stu-id="d68a9-174">bucn</span></span>
  
<span data-ttu-id="d68a9-175">numéro civil uniforme</span><span class="sxs-lookup"><span data-stu-id="d68a9-175">uniform civil number</span></span>
  
<span data-ttu-id="d68a9-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="d68a9-176">bucn#</span></span>
  
<span data-ttu-id="d68a9-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="d68a9-178">ID civil uniforme</span><span class="sxs-lookup"><span data-stu-id="d68a9-178">uniform civil id</span></span>
  
<span data-ttu-id="d68a9-179">non civil uniforme</span><span class="sxs-lookup"><span data-stu-id="d68a9-179">uniform civil no</span></span>
  
<span data-ttu-id="d68a9-180">EGN</span><span class="sxs-lookup"><span data-stu-id="d68a9-180">egn</span></span>
  
<span data-ttu-id="d68a9-181">numéro civil uniforme bulgare</span><span class="sxs-lookup"><span data-stu-id="d68a9-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="d68a9-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-182">uniformcivilno#</span></span>
  
<span data-ttu-id="d68a9-183">EGN #</span><span class="sxs-lookup"><span data-stu-id="d68a9-183">egn#</span></span>
  
<span data-ttu-id="d68a9-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="d68a9-184">униформ граждански номер</span></span>
  
<span data-ttu-id="d68a9-185">ID униформ</span><span class="sxs-lookup"><span data-stu-id="d68a9-185">униформ id</span></span>
  
<span data-ttu-id="d68a9-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="d68a9-186">униформ граждански id</span></span>
  
<span data-ttu-id="d68a9-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="d68a9-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="d68a9-188">Croatie</span><span class="sxs-lookup"><span data-stu-id="d68a9-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-189">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-189">Format</span></span>

<span data-ttu-id="d68a9-190">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-191">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-191">Pattern</span></span>

<span data-ttu-id="d68a9-192">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d68a9-192">11 digits:</span></span>
  
- <span data-ttu-id="d68a9-193">Dix chiffres, choisis de manière aléatoire</span><span class="sxs-lookup"><span data-stu-id="d68a9-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="d68a9-194">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-195">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-195">Checksum</span></span>

<span data-ttu-id="d68a9-196">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-197">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-197">Definition</span></span>

<span data-ttu-id="d68a9-198">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-199">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-200">Un mot clé `Keywords_croatia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-201">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-202">La fonction `Func_croatia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-203">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="d68a9-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-205">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-205">tax number</span></span>
  
<span data-ttu-id="d68a9-206">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-206">tax</span></span>
  
<span data-ttu-id="d68a9-207">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-207">tax id</span></span>
  
<span data-ttu-id="d68a9-208">OID</span><span class="sxs-lookup"><span data-stu-id="d68a9-208">oid</span></span>
  
<span data-ttu-id="d68a9-209">OID</span><span class="sxs-lookup"><span data-stu-id="d68a9-209">oid#</span></span>
  
<span data-ttu-id="d68a9-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="d68a9-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="d68a9-211">Chypre</span><span class="sxs-lookup"><span data-stu-id="d68a9-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-212">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-212">Format</span></span>

<span data-ttu-id="d68a9-213">Huit chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-214">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-214">Pattern</span></span>

<span data-ttu-id="d68a9-215">Huit chiffres et une lettre:</span><span class="sxs-lookup"><span data-stu-id="d68a9-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="d68a9-216">«0»</span><span class="sxs-lookup"><span data-stu-id="d68a9-216">A "0"</span></span> 
    
- <span data-ttu-id="d68a9-217">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-217">Seven digits</span></span>
    
- <span data-ttu-id="d68a9-218">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-219">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-219">Checksum</span></span>

<span data-ttu-id="d68a9-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-221">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-221">Definition</span></span>

<span data-ttu-id="d68a9-222">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-223">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-224">Un mot clé `Keywords_cyprus_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-225">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-226">La fonction `Func_cyprus_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-227">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="d68a9-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-229">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-229">tax number</span></span>
  
<span data-ttu-id="d68a9-230">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-230">tax</span></span>
  
<span data-ttu-id="d68a9-231">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-231">tax id</span></span>
  
<span data-ttu-id="d68a9-232">code d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-232">tax identification code</span></span>
  
<span data-ttu-id="d68a9-233">graduation</span><span class="sxs-lookup"><span data-stu-id="d68a9-233">tic</span></span>
  
<span data-ttu-id="d68a9-234">graduation</span><span class="sxs-lookup"><span data-stu-id="d68a9-234">tic#</span></span>
  
<span data-ttu-id="d68a9-235">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="d68a9-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="d68a9-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="d68a9-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="d68a9-237">Κωδικός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="d68a9-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="d68a9-238">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d68a9-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-239">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-239">Format</span></span>

<span data-ttu-id="d68a9-240">Neuf ou dix chiffres avec une barre oblique inverse facultative</span><span class="sxs-lookup"><span data-stu-id="d68a9-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-241">Pattern</span></span>

<span data-ttu-id="d68a9-242">Neuf ou dix chiffres avec une barre oblique inverse facultative:</span><span class="sxs-lookup"><span data-stu-id="d68a9-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="d68a9-243">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-243">Six digits</span></span> 
    
- <span data-ttu-id="d68a9-244">Une barre oblique inverse (facultatif)</span><span class="sxs-lookup"><span data-stu-id="d68a9-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="d68a9-245">3 ou 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-246">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-246">Checksum</span></span>

<span data-ttu-id="d68a9-247">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-248">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-248">Definition</span></span>

<span data-ttu-id="d68a9-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-250">L'expression `Regex_czech_republic_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-251">Un mot clé `Keywords_czech_republic_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-252">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="d68a9-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-254">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-254">tax number</span></span>
  
<span data-ttu-id="d68a9-255">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-255">tax</span></span>
  
<span data-ttu-id="d68a9-256">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-256">tax id</span></span>
  
<span data-ttu-id="d68a9-257">numéro personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-257">personal number</span></span>
  
<span data-ttu-id="d68a9-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="d68a9-258">daňové číslo</span></span>
  
<span data-ttu-id="d68a9-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="d68a9-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="d68a9-260">Danemark</span><span class="sxs-lookup"><span data-stu-id="d68a9-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-261">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-261">Format</span></span>

<span data-ttu-id="d68a9-262">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="d68a9-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-263">Pattern</span></span>

<span data-ttu-id="d68a9-264">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="d68a9-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="d68a9-265">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="d68a9-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="d68a9-266">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="d68a9-266">A hyphen</span></span>
    
- <span data-ttu-id="d68a9-267">Quatre chiffres correspondant à un numéro de séquence où le premier chiffre correspond au siècle de naissance et le dernier chiffre correspond au sexe de l'individu (impair pour les hommes et les femmes)</span><span class="sxs-lookup"><span data-stu-id="d68a9-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-268">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-268">Checksum</span></span>

<span data-ttu-id="d68a9-269">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-270">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-270">Definition</span></span>

<span data-ttu-id="d68a9-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-272">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-273">Un mot clé `Keywords_denmark_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-274">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-275">La fonction `Func_denmark_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-276">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="d68a9-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-278">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-278">tax number</span></span>
  
<span data-ttu-id="d68a9-279">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-279">tax</span></span>
  
<span data-ttu-id="d68a9-280">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-280">tax id</span></span>
  
<span data-ttu-id="d68a9-281">numéro CPR</span><span class="sxs-lookup"><span data-stu-id="d68a9-281">cpr number</span></span>
  
<span data-ttu-id="d68a9-282">cardio</span><span class="sxs-lookup"><span data-stu-id="d68a9-282">cpr#</span></span>
  
<span data-ttu-id="d68a9-283">Skat Nummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-283">skat nummer</span></span>
  
<span data-ttu-id="d68a9-284">ID Skat</span><span class="sxs-lookup"><span data-stu-id="d68a9-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="d68a9-285">Estonie</span><span class="sxs-lookup"><span data-stu-id="d68a9-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-286">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-286">Format</span></span>

<span data-ttu-id="d68a9-287">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-288">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-288">Pattern</span></span>

<span data-ttu-id="d68a9-289">11 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d68a9-289">11 digits:</span></span>
  
-  <span data-ttu-id="d68a9-290">Un chiffre correspondant au sexe et au siècle de naissance, où un nombre impair indique le mâle et le nombre pair, la femme comme suit: 1,2 pour le 19 siècle; 3, 4 pour le vingtième siècle; et 5, 6 pour le 21ème siècle</span><span class="sxs-lookup"><span data-stu-id="d68a9-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="d68a9-291">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d68a9-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="d68a9-292">Trois chiffres correspondant à un numéro de série séparant les personnes nés à la même date</span><span class="sxs-lookup"><span data-stu-id="d68a9-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="d68a9-293">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-294">Checksum</span></span>

<span data-ttu-id="d68a9-295">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-296">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-296">Definition</span></span>

<span data-ttu-id="d68a9-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-298">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-299">Un mot clé `Keywords_estonia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-300">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-301">La fonction `Func_estonia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-302">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="d68a9-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-304">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-304">tax number</span></span>
  
<span data-ttu-id="d68a9-305">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-305">tax</span></span>
  
<span data-ttu-id="d68a9-306">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-306">tax id</span></span>
  
<span data-ttu-id="d68a9-307">code personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-307">personal code</span></span>
  
<span data-ttu-id="d68a9-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-308">maksunumber</span></span>
  
<span data-ttu-id="d68a9-309">ID maksu</span><span class="sxs-lookup"><span data-stu-id="d68a9-309">maksu id</span></span>
  
<span data-ttu-id="d68a9-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="d68a9-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="d68a9-311">Finlande</span><span class="sxs-lookup"><span data-stu-id="d68a9-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-312">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-312">Format</span></span>

<span data-ttu-id="d68a9-313">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins</span><span class="sxs-lookup"><span data-stu-id="d68a9-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-314">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-314">Pattern</span></span>

<span data-ttu-id="d68a9-315">Combinaison de 11 caractères chiffres, lettres, et signe plus et moins:</span><span class="sxs-lookup"><span data-stu-id="d68a9-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="d68a9-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-316">Six digits</span></span>
    
- <span data-ttu-id="d68a9-317">L'une des options suivantes: un signe plus, un signe moins ou la lettre «A» (ne respectant pas la casse), où le signe plus est né entre 1800-1899, le signe moins est né entre 1900-1999, et «A» désigne né 2000 et after</span><span class="sxs-lookup"><span data-stu-id="d68a9-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="d68a9-318">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-318">Three digits</span></span>
    
- <span data-ttu-id="d68a9-319">Une lettre ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="d68a9-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-320">Checksum</span></span>

<span data-ttu-id="d68a9-321">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-322">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-322">Definition</span></span>

<span data-ttu-id="d68a9-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-324">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-325">Un mot clé `Keywords_finland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-327">La fonction `Func_finland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-328">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="d68a9-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-330">numéro d’identification
</span><span class="sxs-lookup"><span data-stu-id="d68a9-330">identification number</span></span>
  
<span data-ttu-id="d68a9-331">ID personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-331">personal id</span></span>
  
<span data-ttu-id="d68a9-332">Numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="d68a9-332">identity number</span></span>
  
<span data-ttu-id="d68a9-333">Numéro d'identification national finnois</span><span class="sxs-lookup"><span data-stu-id="d68a9-333">finnish national id number</span></span>
  
<span data-ttu-id="d68a9-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-334">personalidnumber#</span></span>
  
<span data-ttu-id="d68a9-335">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="d68a9-335">national identification number</span></span>
  
<span data-ttu-id="d68a9-336">Numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="d68a9-336">id number</span></span>
  
<span data-ttu-id="d68a9-337">Numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="d68a9-337">national id no.</span></span>
  
<span data-ttu-id="d68a9-338">Numéro d'identification national</span><span class="sxs-lookup"><span data-stu-id="d68a9-338">national id number</span></span>
  
<span data-ttu-id="d68a9-339">n ° ID</span><span class="sxs-lookup"><span data-stu-id="d68a9-339">id no</span></span>
  
<span data-ttu-id="d68a9-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="d68a9-340">tunnistenumero</span></span>
  
<span data-ttu-id="d68a9-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="d68a9-341">henkilötunnus</span></span>
  
<span data-ttu-id="d68a9-342">Yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="d68a9-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="d68a9-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="d68a9-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="d68a9-344">identiteetti numérique</span><span class="sxs-lookup"><span data-stu-id="d68a9-344">identiteetti numero</span></span>
  
<span data-ttu-id="d68a9-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="d68a9-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="d68a9-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="d68a9-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="d68a9-347">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="d68a9-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="d68a9-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="d68a9-348">tunnusnumero</span></span>
  
<span data-ttu-id="d68a9-349">Kansallinen tunnus numérique</span><span class="sxs-lookup"><span data-stu-id="d68a9-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="d68a9-350">France</span><span class="sxs-lookup"><span data-stu-id="d68a9-350">France</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-351">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-351">Format</span></span>

<span data-ttu-id="d68a9-352">13 chiffres pour les personnes et neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="d68a9-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-353">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-353">Pattern</span></span>

<span data-ttu-id="d68a9-354">13 chiffres pour les personnes:</span><span class="sxs-lookup"><span data-stu-id="d68a9-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="d68a9-355">Un chiffre qui doit être 0, 1, 2 ou 3</span><span class="sxs-lookup"><span data-stu-id="d68a9-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="d68a9-356">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-356">12 digits</span></span>
    
<span data-ttu-id="d68a9-357">Neuf chiffres pour les entités</span><span class="sxs-lookup"><span data-stu-id="d68a9-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-358">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-358">Checksum</span></span>

<span data-ttu-id="d68a9-359">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-360">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-360">Definition</span></span>

<span data-ttu-id="d68a9-361">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-362">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-363">Un mot clé `Keywords_france_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-364">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-365">La fonction `Func_france_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-366">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="d68a9-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-368">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-368">tax identification number</span></span>
  
<span data-ttu-id="d68a9-369">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-369">tax number</span></span>
  
<span data-ttu-id="d68a9-370">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-370">tax id</span></span>
  
<span data-ttu-id="d68a9-371">Numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="d68a9-372">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d68a9-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-373">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-373">Format</span></span>

<span data-ttu-id="d68a9-374">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-375">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-375">Pattern</span></span>

<span data-ttu-id="d68a9-376">11 chiffres:</span><span class="sxs-lookup"><span data-stu-id="d68a9-376">11 digits :</span></span>
  
-  <span data-ttu-id="d68a9-377">Dix chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-377">Ten digits</span></span> 
    
- <span data-ttu-id="d68a9-378">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-379">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-379">Checksum</span></span>

<span data-ttu-id="d68a9-380">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-381">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-381">Definition</span></span>

<span data-ttu-id="d68a9-382">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-383">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-384">Un mot clé `Keywords_germany_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-385">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-386">La fonction `Func_germany_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-387">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="d68a9-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-389">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-389">tax number</span></span>
  
<span data-ttu-id="d68a9-390">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-390">tax no.</span></span>
  
<span data-ttu-id="d68a9-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-391">taxno#</span></span>
  
<span data-ttu-id="d68a9-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-392">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-393">taxnumber</span></span>
  
<span data-ttu-id="d68a9-394">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-394">tax id</span></span>
  
<span data-ttu-id="d68a9-395">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-395">taxid#</span></span>
  
<span data-ttu-id="d68a9-396">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-396">tax identification number</span></span>
  
<span data-ttu-id="d68a9-397">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-397">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-398">steuernummer</span></span>
  
<span data-ttu-id="d68a9-399">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="d68a9-399">steuer id</span></span>
  
<span data-ttu-id="d68a9-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="d68a9-401">Grèce</span><span class="sxs-lookup"><span data-stu-id="d68a9-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-402">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-402">Format</span></span>

<span data-ttu-id="d68a9-403">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-404">Pattern</span></span>

<span data-ttu-id="d68a9-405">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-406">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-406">Checksum</span></span>

<span data-ttu-id="d68a9-407">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-408">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-408">Definition</span></span>

<span data-ttu-id="d68a9-409">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-410">L'expression `Regex_greece_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-411">Un mot clé `Keywords_greece_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-412">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="d68a9-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-414">financement</span><span class="sxs-lookup"><span data-stu-id="d68a9-414">afm</span></span>
  
<span data-ttu-id="d68a9-415">tin
</span><span class="sxs-lookup"><span data-stu-id="d68a9-415">tin</span></span>
  
<span data-ttu-id="d68a9-416">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-416">tax id no.</span></span>
  
<span data-ttu-id="d68a9-417">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-417">tax id no</span></span>
  
<span data-ttu-id="d68a9-418">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-418">tax identification number</span></span>
  
<span data-ttu-id="d68a9-419">Numéro de registre des taxes</span><span class="sxs-lookup"><span data-stu-id="d68a9-419">tax registry number</span></span>
  
<span data-ttu-id="d68a9-420">n ° de Registre taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-420">tax registry no.</span></span>
  
<span data-ttu-id="d68a9-421">financement</span><span class="sxs-lookup"><span data-stu-id="d68a9-421">afm#</span></span>
  
<span data-ttu-id="d68a9-422">Etain</span><span class="sxs-lookup"><span data-stu-id="d68a9-422">tin#</span></span>
  
<span data-ttu-id="d68a9-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-423">taxidno#</span></span>
  
<span data-ttu-id="d68a9-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-424">taxregistryno#</span></span>
  
<span data-ttu-id="d68a9-425">Αριθμός φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="d68a9-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="d68a9-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="d68a9-426">aφμ</span></span>
  
<span data-ttu-id="d68a9-427">aφμ Αριθμός</span><span class="sxs-lookup"><span data-stu-id="d68a9-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="d68a9-428">φορολογικού Μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="d68a9-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="d68a9-429">τον αριθμό φορολογικού Μητρώου</span><span class="sxs-lookup"><span data-stu-id="d68a9-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="d68a9-430">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d68a9-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-431">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-431">Format</span></span>

<span data-ttu-id="d68a9-432">Dix chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-433">Pattern</span></span>

<span data-ttu-id="d68a9-434">Dix chiffres:</span><span class="sxs-lookup"><span data-stu-id="d68a9-434">Ten digits:</span></span>
  
-  <span data-ttu-id="d68a9-435">Un chiffre qui doit être «8»</span><span class="sxs-lookup"><span data-stu-id="d68a9-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="d68a9-436">Cinq chiffres correspondant au nombre de jours entre la date 01/01/1867 et la date de naissance de la personne</span><span class="sxs-lookup"><span data-stu-id="d68a9-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="d68a9-437">Trois chiffres correspondant au nombre généré par l'opportunité pour différencier les individus nés le même jour</span><span class="sxs-lookup"><span data-stu-id="d68a9-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="d68a9-438">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-439">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-439">Checksum</span></span>

<span data-ttu-id="d68a9-440">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-441">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-441">Definition</span></span>

<span data-ttu-id="d68a9-442">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-443">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-444">Un mot clé `Keywords_hungary_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-445">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-446">La fonction `Func_hungary_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-447">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="d68a9-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-449">Numéro d'identification de taxe hongrois</span><span class="sxs-lookup"><span data-stu-id="d68a9-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="d68a9-450">étain hongrois</span><span class="sxs-lookup"><span data-stu-id="d68a9-450">hungarian tin</span></span>
  
<span data-ttu-id="d68a9-451">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-451">tax id number</span></span>
  
<span data-ttu-id="d68a9-452">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="d68a9-452">vat number</span></span>
  
<span data-ttu-id="d68a9-453">Numéro de l'autorité fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-453">tax authority no</span></span>
  
<span data-ttu-id="d68a9-454">Numéro d'identité fiscale de l'ID taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-454">tax id tax identity number</span></span>
  
<span data-ttu-id="d68a9-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-455">taxidnumber#</span></span>
  
<span data-ttu-id="d68a9-456">Etain</span><span class="sxs-lookup"><span data-stu-id="d68a9-456">tin#</span></span>
  
<span data-ttu-id="d68a9-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="d68a9-457">hungatiantin#</span></span>
  
<span data-ttu-id="d68a9-458">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-458">tax identification no</span></span>
  
<span data-ttu-id="d68a9-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-459">taxidno#</span></span>
  
<span data-ttu-id="d68a9-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="d68a9-460">adóazonosító szám</span></span>
  
<span data-ttu-id="d68a9-461">adószám</span><span class="sxs-lookup"><span data-stu-id="d68a9-461">adószám</span></span>
  
<span data-ttu-id="d68a9-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="d68a9-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="d68a9-463">Irlande</span><span class="sxs-lookup"><span data-stu-id="d68a9-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-464">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-464">Format</span></span>

<span data-ttu-id="d68a9-465">Sept chiffres suivis d'une lettre sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-466">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-466">Pattern</span></span>

<span data-ttu-id="d68a9-467">Sept chiffres suivis d'une lettre:</span><span class="sxs-lookup"><span data-stu-id="d68a9-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="d68a9-468">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-468">Seven digits</span></span> 
    
- <span data-ttu-id="d68a9-469">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-470">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-470">Checksum</span></span>

<span data-ttu-id="d68a9-471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-472">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-472">Definition</span></span>

<span data-ttu-id="d68a9-473">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-474">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-475">Un mot clé `Keywords_ireland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-476">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-477">La fonction `Func_ireland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-478">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="d68a9-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-480">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="d68a9-480">public service no</span></span>
  
<span data-ttu-id="d68a9-481">service public personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-481">personal public service no</span></span>
  
<span data-ttu-id="d68a9-482">n ° PPS</span><span class="sxs-lookup"><span data-stu-id="d68a9-482">pps no</span></span>
  
<span data-ttu-id="d68a9-483">Numéro de service personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-483">personal service no</span></span>
  
<span data-ttu-id="d68a9-484">n ° de Service PPS</span><span class="sxs-lookup"><span data-stu-id="d68a9-484">pps service no</span></span>
  
<span data-ttu-id="d68a9-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-485">ppsno#</span></span>
  
<span data-ttu-id="d68a9-486">n ° PPS irlandais</span><span class="sxs-lookup"><span data-stu-id="d68a9-486">irish pps no</span></span>
  
<span data-ttu-id="d68a9-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-487">publicserviceno#</span></span>
  
<span data-ttu-id="d68a9-488">Numéro de service public</span><span class="sxs-lookup"><span data-stu-id="d68a9-488">personal public service number</span></span>
  
<span data-ttu-id="d68a9-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="d68a9-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="d68a9-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="d68a9-490">pps uimh</span></span>
  
<span data-ttu-id="d68a9-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="d68a9-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="d68a9-492">Italie</span><span class="sxs-lookup"><span data-stu-id="d68a9-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-493">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-493">Format</span></span>

<span data-ttu-id="d68a9-494">16 lettres et chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-495">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-495">Pattern</span></span>

<span data-ttu-id="d68a9-496">16 lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="d68a9-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="d68a9-497">Trois lettres qui correspondent aux trois premières consonnes du nom de la famille</span><span class="sxs-lookup"><span data-stu-id="d68a9-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="d68a9-498">Trois lettres qui correspondent à la première, troisième et quatrième consonnes du prénom</span><span class="sxs-lookup"><span data-stu-id="d68a9-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="d68a9-499">Deux chiffres correspondant aux derniers chiffres de l'année de naissance</span><span class="sxs-lookup"><span data-stu-id="d68a9-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="d68a9-500">Un chiffre correspondant au mois de naissance: les lettres sont utilisées par ordre alphabétique, mais seules les lettres de A à E, H, L, M, P, R à T sont utilisées (en janvier, A et octobre est R).</span><span class="sxs-lookup"><span data-stu-id="d68a9-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="d68a9-501">Deux chiffres correspondant au jour du mois de naissance où 40 est ajouté au jour de naissance pour que les femmes différencient les hommes</span><span class="sxs-lookup"><span data-stu-id="d68a9-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="d68a9-502">Quatre chiffres correspondant à un indicatif régional spécifique à la municipalité où la personne est né — des codes nationaux sont utilisés pour les pays étrangers</span><span class="sxs-lookup"><span data-stu-id="d68a9-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="d68a9-503">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-504">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-504">Checksum</span></span>

<span data-ttu-id="d68a9-505">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-506">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-506">Definition</span></span>

<span data-ttu-id="d68a9-507">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-508">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-509">Un mot clé `Keywords_italy_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-510">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-511">La fonction `Func_italy_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-512">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="d68a9-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-514">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-514">tax number</span></span>
  
<span data-ttu-id="d68a9-515">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-515">tax no.</span></span>
  
<span data-ttu-id="d68a9-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-516">taxno#</span></span>
  
<span data-ttu-id="d68a9-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-517">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-518">taxnumber</span></span>
  
<span data-ttu-id="d68a9-519">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-519">tax id</span></span>
  
<span data-ttu-id="d68a9-520">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-520">taxid#</span></span>
  
<span data-ttu-id="d68a9-521">code fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-521">fiscal code</span></span>
  
<span data-ttu-id="d68a9-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="d68a9-523">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d68a9-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-524">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-524">Format</span></span>

<span data-ttu-id="d68a9-525">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-526">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-526">Pattern</span></span>

<span data-ttu-id="d68a9-527">11 chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="d68a9-528">Six chiffres correspondant à la date de naissance (JJMMAA)</span><span class="sxs-lookup"><span data-stu-id="d68a9-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="d68a9-529">Un chiffre correspondant au siècle de naissance où «0» correspond à 19 siècle, «1» correspond au vingtième siècle et «2» au 21ème siècle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="d68a9-530">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-531">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-531">Checksum</span></span>

<span data-ttu-id="d68a9-532">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-533">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-533">Definition</span></span>

<span data-ttu-id="d68a9-534">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-535">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-536">Un mot clé `Keywords_latvia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-537">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-538">La fonction `Func_latvia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-539">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="d68a9-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-541">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-541">tax number</span></span>
  
<span data-ttu-id="d68a9-542">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-542">tax no.</span></span>
  
<span data-ttu-id="d68a9-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-543">taxno#</span></span>
  
<span data-ttu-id="d68a9-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-544">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-545">taxnumber</span></span>
  
<span data-ttu-id="d68a9-546">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-546">tax id</span></span>
  
<span data-ttu-id="d68a9-547">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-547">taxid#</span></span>
  
<span data-ttu-id="d68a9-548">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-548">tax identification number</span></span>
  
<span data-ttu-id="d68a9-549">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-549">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-550">nodokļa numurs</span></span>
  
<span data-ttu-id="d68a9-551">nodokļu IDENTIFIKĀCIJAS numurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="d68a9-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="d68a9-553">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d68a9-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-554">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-554">Format</span></span>

<span data-ttu-id="d68a9-555">11 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-556">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-556">Pattern</span></span>

<span data-ttu-id="d68a9-557">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-558">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-558">Checksum</span></span>

<span data-ttu-id="d68a9-559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-560">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-560">Definition</span></span>

<span data-ttu-id="d68a9-561">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-562">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-563">Un mot clé `Keywords_lithuania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-564">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-565">La fonction `Func_lithuania_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-566">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="d68a9-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-568">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-568">tax number</span></span>
  
<span data-ttu-id="d68a9-569">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-569">tax no.</span></span>
  
<span data-ttu-id="d68a9-570">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="d68a9-570">tax no#</span></span>
  
<span data-ttu-id="d68a9-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-571">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-572">taxnumber</span></span>
  
<span data-ttu-id="d68a9-573">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-573">tax id</span></span>
  
<span data-ttu-id="d68a9-574">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-574">taxid#</span></span>
  
<span data-ttu-id="d68a9-575">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-575">tax identification number</span></span>
  
<span data-ttu-id="d68a9-576">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-576">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-577">ID mokesčių</span><span class="sxs-lookup"><span data-stu-id="d68a9-577">mokesčių id</span></span>
  
<span data-ttu-id="d68a9-578">mokesčių chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-578">mokesčių numeris</span></span>
  
<span data-ttu-id="d68a9-579">mokesčių identifikavimas</span><span class="sxs-lookup"><span data-stu-id="d68a9-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="d68a9-580">Relatif</span><span class="sxs-lookup"><span data-stu-id="d68a9-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-581">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-581">Format</span></span>

<span data-ttu-id="d68a9-582">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-583">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-583">Pattern</span></span>

<span data-ttu-id="d68a9-584">13 chiffres :</span><span class="sxs-lookup"><span data-stu-id="d68a9-584">13 digits:</span></span>
  
-  <span data-ttu-id="d68a9-585">11 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-585">11 digits</span></span> 
    
- <span data-ttu-id="d68a9-586">Deux chiffres de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-587">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-587">Checksum</span></span>

<span data-ttu-id="d68a9-588">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-589">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-589">Definition</span></span>

<span data-ttu-id="d68a9-590">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-591">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-592">Un mot clé `Keywords_luxemburg_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-593">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-594">La fonction `Func_luxemburg_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-595">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="d68a9-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-597">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-597">tax number</span></span>
  
<span data-ttu-id="d68a9-598">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-598">tax no.</span></span>
  
<span data-ttu-id="d68a9-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-599">taxno#</span></span>
  
<span data-ttu-id="d68a9-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-600">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-601">taxnumber</span></span>
  
<span data-ttu-id="d68a9-602">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-602">tax id</span></span>
  
<span data-ttu-id="d68a9-603">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-603">taxid#</span></span>
  
<span data-ttu-id="d68a9-604">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-604">tax identification number</span></span>
  
<span data-ttu-id="d68a9-605">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-605">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-606">steuernummer</span></span>
  
<span data-ttu-id="d68a9-607">ID Steuer</span><span class="sxs-lookup"><span data-stu-id="d68a9-607">steuer id</span></span>
  
<span data-ttu-id="d68a9-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="d68a9-609">Malte</span><span class="sxs-lookup"><span data-stu-id="d68a9-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-610">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-610">Format</span></span>

<span data-ttu-id="d68a9-611">Pour les ressortissants maltais: 7 chiffres et une lettre dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="d68a9-612">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-613">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-613">Pattern</span></span>

<span data-ttu-id="d68a9-614">Ressortissants maltaises: 7 chiffres et une lettre</span><span class="sxs-lookup"><span data-stu-id="d68a9-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="d68a9-615">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-615">Seven digits</span></span> 
    
- <span data-ttu-id="d68a9-616">Une lettre (ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="d68a9-617">Ressortissants non maltaises et entités maltaises: 9 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="d68a9-618">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d68a9-619">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-619">Checksum</span></span>

<span data-ttu-id="d68a9-620">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-621">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-621">Definition</span></span>

<span data-ttu-id="d68a9-622">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-623">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-624">Un mot clé `Keywords_malta_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-625">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 65 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-626">La fonction `Func_malta_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-627">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="d68a9-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-629">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-629">tax number</span></span>
  
<span data-ttu-id="d68a9-630">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-630">tax no.</span></span>
  
<span data-ttu-id="d68a9-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-631">taxno#</span></span>
  
<span data-ttu-id="d68a9-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-632">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-633">taxnumber</span></span>
  
<span data-ttu-id="d68a9-634">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-634">tax id</span></span>
  
<span data-ttu-id="d68a9-635">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-635">taxid#</span></span>
  
<span data-ttu-id="d68a9-636">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-636">tax identification number</span></span>
  
<span data-ttu-id="d68a9-637">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-637">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="d68a9-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="d68a9-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="d68a9-639">id tat-taxxa</span></span>
  
<span data-ttu-id="d68a9-640">numru ta'IDENTIFIKAZZJONI tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="d68a9-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="d68a9-641">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d68a9-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-642">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-642">Format</span></span>

<span data-ttu-id="d68a9-643">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-644">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-644">Pattern</span></span>

<span data-ttu-id="d68a9-645">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="d68a9-646">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-646">Checksum</span></span>

<span data-ttu-id="d68a9-647">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-648">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-648">Definition</span></span>

<span data-ttu-id="d68a9-649">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-650">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-651">Un mot clé `Keywords_netherlands_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-652">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-653">La fonction `Func_netherlands_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-654">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="d68a9-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-656">Numéro d'identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="d68a9-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="d68a9-657">identification fiscale néerlandaise</span><span class="sxs-lookup"><span data-stu-id="d68a9-657">netherlands tax identification</span></span>
  
<span data-ttu-id="d68a9-658">Numéro d'identification de taxe de Netherland</span><span class="sxs-lookup"><span data-stu-id="d68a9-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="d68a9-659">identification fiscale de Netherland</span><span class="sxs-lookup"><span data-stu-id="d68a9-659">netherland's tax identification</span></span>
  
<span data-ttu-id="d68a9-660">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-660">tax identification number</span></span>
  
<span data-ttu-id="d68a9-661">ID de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="d68a9-661">dutch tax id</span></span>
  
<span data-ttu-id="d68a9-662">Numéro d'identification de taxe néerlandaise</span><span class="sxs-lookup"><span data-stu-id="d68a9-662">dutch tax identification number</span></span>
  
<span data-ttu-id="d68a9-663">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-663">tax id</span></span>
  
<span data-ttu-id="d68a9-664">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-664">tax id#</span></span>
  
<span data-ttu-id="d68a9-665">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-665">tax number</span></span>
  
<span data-ttu-id="d68a9-666">n ° de taxe n °</span><span class="sxs-lookup"><span data-stu-id="d68a9-666">tax no#</span></span>
  
<span data-ttu-id="d68a9-667">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-667">tax#</span></span>
  
<span data-ttu-id="d68a9-668">tin
</span><span class="sxs-lookup"><span data-stu-id="d68a9-668">tin</span></span>
  
<span data-ttu-id="d68a9-669">Etain</span><span class="sxs-lookup"><span data-stu-id="d68a9-669">tin#</span></span>
  
<span data-ttu-id="d68a9-670">étain (Pays-Bas)</span><span class="sxs-lookup"><span data-stu-id="d68a9-670">netherlands tin</span></span>
  
<span data-ttu-id="d68a9-671">Netherland d'étain</span><span class="sxs-lookup"><span data-stu-id="d68a9-671">netherland's tin</span></span>
  
<span data-ttu-id="d68a9-672">néerlandais qui a identificatienummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="d68a9-673">identificatienummer van à l'avant-dernière</span><span class="sxs-lookup"><span data-stu-id="d68a9-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="d68a9-674">identificatienummer qui a été modifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="d68a9-675">néerlandais qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="d68a9-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="d68a9-676">néerlandais qui a pour ID Nummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="d68a9-677">Néerlandais belastingnummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="d68a9-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-678">btw nummer</span></span>
  
<span data-ttu-id="d68a9-679">Nederlandse qui a identificatie</span><span class="sxs-lookup"><span data-stu-id="d68a9-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="d68a9-680">Pologne</span><span class="sxs-lookup"><span data-stu-id="d68a9-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-681">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-681">Format</span></span>

<span data-ttu-id="d68a9-682">Onze chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-683">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-683">Pattern</span></span>

<span data-ttu-id="d68a9-684">Onze chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-685">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-685">Checksum</span></span>

<span data-ttu-id="d68a9-686">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-687">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-687">Definition</span></span>

<span data-ttu-id="d68a9-688">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-689">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-690">Un mot clé `Keywords_poland_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-691">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-692">La fonction `Func_poland_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-693">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="d68a9-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-695">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-695">tax number</span></span>
  
<span data-ttu-id="d68a9-696">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-696">tax no.</span></span>
  
<span data-ttu-id="d68a9-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-697">taxno#</span></span>
  
<span data-ttu-id="d68a9-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-698">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-699">taxnumber</span></span>
  
<span data-ttu-id="d68a9-700">pince</span><span class="sxs-lookup"><span data-stu-id="d68a9-700">nip</span></span>
  
<span data-ttu-id="d68a9-701">pince</span><span class="sxs-lookup"><span data-stu-id="d68a9-701">nip#</span></span>
  
<span data-ttu-id="d68a9-702">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-702">tax id</span></span>
  
<span data-ttu-id="d68a9-703">n ° de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-703">tax id#</span></span>
  
<span data-ttu-id="d68a9-704">ID du NIP</span><span class="sxs-lookup"><span data-stu-id="d68a9-704">nip id</span></span>
  
<span data-ttu-id="d68a9-705">n ° de NIP</span><span class="sxs-lookup"><span data-stu-id="d68a9-705">nip id#</span></span>
  
<span data-ttu-id="d68a9-706">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-706">tax identification number</span></span>
  
<span data-ttu-id="d68a9-707">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-707">tax identification no.</span></span>
  
<span data-ttu-id="d68a9-708">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="d68a9-708">vat number</span></span>
  
<span data-ttu-id="d68a9-709">n ° TVA</span><span class="sxs-lookup"><span data-stu-id="d68a9-709">vat no.</span></span>
  
<span data-ttu-id="d68a9-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-710">vatno#</span></span>
  
<span data-ttu-id="d68a9-711">Numéro de TVA</span><span class="sxs-lookup"><span data-stu-id="d68a9-711">vat id</span></span>
  
<span data-ttu-id="d68a9-712">n ° de TVA</span><span class="sxs-lookup"><span data-stu-id="d68a9-712">vat id#</span></span>
  
<span data-ttu-id="d68a9-713">chiffre identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="d68a9-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="d68a9-714">Polski identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="d68a9-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="d68a9-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="d68a9-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d68a9-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="d68a9-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-717">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-717">Format</span></span>

<span data-ttu-id="d68a9-718">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-719">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-719">Pattern</span></span>

<span data-ttu-id="d68a9-720">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-721">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-721">Checksum</span></span>

<span data-ttu-id="d68a9-722">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-723">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-723">Definition</span></span>

<span data-ttu-id="d68a9-724">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-725">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-726">Un mot clé `Keywords_portugal_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-727">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-728">La fonction `Func_portugal_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-729">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="d68a9-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-731">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-731">tax number</span></span>
  
<span data-ttu-id="d68a9-732">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-732">tax no.</span></span>
  
<span data-ttu-id="d68a9-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-733">taxno#</span></span>
  
<span data-ttu-id="d68a9-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="d68a9-734">taxnumber#</span></span>
  
<span data-ttu-id="d68a9-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="d68a9-735">taxnumber</span></span>
  
<span data-ttu-id="d68a9-736">nPour</span><span class="sxs-lookup"><span data-stu-id="d68a9-736">nif</span></span>
  
<span data-ttu-id="d68a9-737">nPour</span><span class="sxs-lookup"><span data-stu-id="d68a9-737">nif#</span></span>
  
<span data-ttu-id="d68a9-738">chiffres fiscaux</span><span class="sxs-lookup"><span data-stu-id="d68a9-738">numero fiscal</span></span>
  
<span data-ttu-id="d68a9-739">Número de identificação fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="d68a9-740">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d68a9-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-741">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-741">Format</span></span>

<span data-ttu-id="d68a9-742">13 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-743">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-743">Pattern</span></span>

<span data-ttu-id="d68a9-744">13 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-745">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-745">Checksum</span></span>

<span data-ttu-id="d68a9-746">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-747">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-747">Definition</span></span>

<span data-ttu-id="d68a9-748">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-749">L'expression `Regex_romania_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-750">Un mot clé `Keywords_romania_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-751">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="d68a9-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-753">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-753">tax id</span></span>
  
<span data-ttu-id="d68a9-754">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-754">tax id number</span></span>
  
<span data-ttu-id="d68a9-755">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-755">tax file no</span></span>
  
<span data-ttu-id="d68a9-756">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-756">tax file number</span></span>
  
<span data-ttu-id="d68a9-757">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-757">tax no</span></span>
  
<span data-ttu-id="d68a9-758">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-758">tax number</span></span>
  
<span data-ttu-id="d68a9-759">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-759">taxid#</span></span>
  
<span data-ttu-id="d68a9-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-760">taxno#</span></span>
  
<span data-ttu-id="d68a9-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="d68a9-761">id-ul taxei</span></span>
  
<span data-ttu-id="d68a9-762">numărul de IDENTIFICARE fiscală</span><span class="sxs-lookup"><span data-stu-id="d68a9-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="d68a9-763">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d68a9-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-764">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-764">Format</span></span>

<span data-ttu-id="d68a9-765">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-766">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-766">Pattern</span></span>

<span data-ttu-id="d68a9-767">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-768">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-768">Checksum</span></span>

<span data-ttu-id="d68a9-769">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d68a9-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-770">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-770">Definition</span></span>

<span data-ttu-id="d68a9-771">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-772">L'expression `Regex_slovakia_eu_tax_file_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-773">Un mot clé `Keywords_slovakia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-774">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="d68a9-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-776">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-776">tax id</span></span>
  
<span data-ttu-id="d68a9-777">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-777">tax id number</span></span>
  
<span data-ttu-id="d68a9-778">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="d68a9-778">tin id</span></span>
  
<span data-ttu-id="d68a9-779">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="d68a9-779">tin no</span></span>
  
<span data-ttu-id="d68a9-780">ID d'étain slovaque</span><span class="sxs-lookup"><span data-stu-id="d68a9-780">slovakian tin id</span></span>
  
<span data-ttu-id="d68a9-781">tin
</span><span class="sxs-lookup"><span data-stu-id="d68a9-781">tin</span></span>
  
<span data-ttu-id="d68a9-782">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-782">tax file no</span></span>
  
<span data-ttu-id="d68a9-783">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-783">tax file number</span></span>
  
<span data-ttu-id="d68a9-784">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-784">tax no</span></span>
  
<span data-ttu-id="d68a9-785">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-785">tax number</span></span>
  
<span data-ttu-id="d68a9-786">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-786">taxid#</span></span>
  
<span data-ttu-id="d68a9-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-787">taxno#</span></span>
  
<span data-ttu-id="d68a9-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="d68a9-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="d68a9-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="d68a9-789">daňové číslo</span></span>
  
<span data-ttu-id="d68a9-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="d68a9-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="d68a9-791">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d68a9-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-792">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-792">Format</span></span>

<span data-ttu-id="d68a9-793">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-794">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-794">Pattern</span></span>

<span data-ttu-id="d68a9-795">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-796">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-796">Checksum</span></span>

<span data-ttu-id="d68a9-797">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-798">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-798">Definition</span></span>

<span data-ttu-id="d68a9-799">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-800">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-801">Un mot clé `Keywords_slovenia_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-802">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-803">La fonction `Func_slovenia_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-804">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="d68a9-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-806">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-806">tax id</span></span>
  
<span data-ttu-id="d68a9-807">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-807">tax id number</span></span>
  
<span data-ttu-id="d68a9-808">ID d'étain</span><span class="sxs-lookup"><span data-stu-id="d68a9-808">tin id</span></span>
  
<span data-ttu-id="d68a9-809">n ° d'étain</span><span class="sxs-lookup"><span data-stu-id="d68a9-809">tin no</span></span>
  
<span data-ttu-id="d68a9-810">ID d'étain slovène</span><span class="sxs-lookup"><span data-stu-id="d68a9-810">slovenian tin id</span></span>
  
<span data-ttu-id="d68a9-811">tin
</span><span class="sxs-lookup"><span data-stu-id="d68a9-811">tin</span></span>
  
<span data-ttu-id="d68a9-812">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-812">tax file no</span></span>
  
<span data-ttu-id="d68a9-813">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-813">tax file number</span></span>
  
<span data-ttu-id="d68a9-814">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-814">tax no</span></span>
  
<span data-ttu-id="d68a9-815">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-815">tax number</span></span>
  
<span data-ttu-id="d68a9-816">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-816">taxid#</span></span>
  
<span data-ttu-id="d68a9-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-817">taxno#</span></span>
  
<span data-ttu-id="d68a9-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="d68a9-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="d68a9-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="d68a9-819">davčna številka</span></span>
  
<span data-ttu-id="d68a9-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="d68a9-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="d68a9-821">Espagne</span><span class="sxs-lookup"><span data-stu-id="d68a9-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-822">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-822">Format</span></span>

<span data-ttu-id="d68a9-823">Sept ou huit chiffres et une ou deux lettres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-824">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-824">Pattern</span></span>

<span data-ttu-id="d68a9-825">Personnes physiques espagnoles avec une carte d'identité nationale d'Espagne:</span><span class="sxs-lookup"><span data-stu-id="d68a9-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="d68a9-826">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-826">Eight digits</span></span> 
    
- <span data-ttu-id="d68a9-827">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="d68a9-828">Spaniards non résident sans carte d'identité nationale d'Espagne</span><span class="sxs-lookup"><span data-stu-id="d68a9-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="d68a9-829">Une lettre majuscule «L» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="d68a9-830">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-830">Seven digits</span></span>
    
- <span data-ttu-id="d68a9-831">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="d68a9-832">Spaniards résident de moins de 14 ans sans carte d'identité nationale (Espagne):</span><span class="sxs-lookup"><span data-stu-id="d68a9-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="d68a9-833">Une lettre majuscule «K» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="d68a9-834">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-834">Seven digits</span></span> 
    
- <span data-ttu-id="d68a9-835">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="d68a9-836">Foreigners avec le numéro d'identification d'un étranger</span><span class="sxs-lookup"><span data-stu-id="d68a9-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="d68a9-837">Une lettre majuscule qui est «X», «Y» ou «Z» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="d68a9-838">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-838">Seven digits</span></span>
    
- <span data-ttu-id="d68a9-839">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="d68a9-840">Foreigners sans numéro d'identification étranger</span><span class="sxs-lookup"><span data-stu-id="d68a9-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="d68a9-841">Une lettre majuscule qui est «M» (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="d68a9-842">Sept chiffres </span><span class="sxs-lookup"><span data-stu-id="d68a9-842">Seven digits</span></span>
    
- <span data-ttu-id="d68a9-843">Une lettre majuscule (respecte la casse)</span><span class="sxs-lookup"><span data-stu-id="d68a9-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d68a9-844">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-844">Checksum</span></span>

<span data-ttu-id="d68a9-845">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-846">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-846">Definition</span></span>

<span data-ttu-id="d68a9-847">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-848">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-849">Un mot clé `Keywords_spain_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-850">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-851">La fonction `Func_spain_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-852">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="d68a9-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-854">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-854">tax id</span></span>
  
<span data-ttu-id="d68a9-855">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-855">tax id number</span></span>
  
<span data-ttu-id="d68a9-856">identifiant CAF</span><span class="sxs-lookup"><span data-stu-id="d68a9-856">cif id</span></span>
  
<span data-ttu-id="d68a9-857">CAF non</span><span class="sxs-lookup"><span data-stu-id="d68a9-857">cif no</span></span>
  
<span data-ttu-id="d68a9-858">ID CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="d68a9-858">spanish cif id</span></span>
  
<span data-ttu-id="d68a9-859">importation</span><span class="sxs-lookup"><span data-stu-id="d68a9-859">cif</span></span>
  
<span data-ttu-id="d68a9-860">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-860">tax file no</span></span>
  
<span data-ttu-id="d68a9-861">numéro CAF espagnol</span><span class="sxs-lookup"><span data-stu-id="d68a9-861">spanish cif number</span></span>
  
<span data-ttu-id="d68a9-862">

numéro de dossier fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-862">tax file number</span></span>
  
<span data-ttu-id="d68a9-863">espagnol (CAF)</span><span class="sxs-lookup"><span data-stu-id="d68a9-863">spanish cif no</span></span>
  
<span data-ttu-id="d68a9-864">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-864">tax no</span></span>
  
<span data-ttu-id="d68a9-865">Numéro de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-865">tax number</span></span>
  
<span data-ttu-id="d68a9-866">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-866">taxid#</span></span>
  
<span data-ttu-id="d68a9-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-867">taxno#</span></span>
  
<span data-ttu-id="d68a9-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="d68a9-868">cifid#</span></span>
  
<span data-ttu-id="d68a9-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="d68a9-869">spanishcifid#</span></span>
  
<span data-ttu-id="d68a9-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="d68a9-870">spanishcifno#</span></span>
  
<span data-ttu-id="d68a9-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="d68a9-871">número de contribuyente</span></span>
  
<span data-ttu-id="d68a9-872">Número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="d68a9-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="d68a9-873">Número de Identificación fiscal</span><span class="sxs-lookup"><span data-stu-id="d68a9-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="d68a9-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="d68a9-874">cif número</span></span>
  
<span data-ttu-id="d68a9-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="d68a9-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="d68a9-876">Suède</span><span class="sxs-lookup"><span data-stu-id="d68a9-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-877">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-877">Format</span></span>

<span data-ttu-id="d68a9-878">Dix chiffres et un symbole dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="d68a9-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-879">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-879">Pattern</span></span>

<span data-ttu-id="d68a9-880">Dix chiffres et un symbole:</span><span class="sxs-lookup"><span data-stu-id="d68a9-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="d68a9-881">Six chiffres correspondant à la date de naissance (AAMMJJ)</span><span class="sxs-lookup"><span data-stu-id="d68a9-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="d68a9-882">Un signe plus, un signe moins ou une barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="d68a9-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="d68a9-883">Trois chiffres qui permettent de définir le numéro d'identification unique:</span><span class="sxs-lookup"><span data-stu-id="d68a9-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="d68a9-884">Pour les numéros émis avant le 1990, le septième et le huitième chiffre identifient le comté de naissance ou les personnes nées à l'étranger.</span><span class="sxs-lookup"><span data-stu-id="d68a9-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="d68a9-885">Le chiffre de la neuvième position indique le sexe soit impair, soit pair pour femme.</span><span class="sxs-lookup"><span data-stu-id="d68a9-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="d68a9-886">Un chiffre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d68a9-887">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-887">Checksum</span></span>

<span data-ttu-id="d68a9-888">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-889">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-889">Definition</span></span>

<span data-ttu-id="d68a9-890">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 85 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-891">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-892">Un mot clé `Keywords_sweden_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="d68a9-893">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-894">La fonction `Func_sweden_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d68a9-895">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="d68a9-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-897">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-897">tax id</span></span>
  
<span data-ttu-id="d68a9-898">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-898">tax id no.</span></span>
  
<span data-ttu-id="d68a9-899">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-899">tax id number</span></span>
  
<span data-ttu-id="d68a9-900">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="d68a9-900">tax identification</span></span>
  
<span data-ttu-id="d68a9-901">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-901">tax identification#</span></span>
  
<span data-ttu-id="d68a9-902">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-902">tax no.</span></span>
  
<span data-ttu-id="d68a9-903">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-903">tax#</span></span>
  
<span data-ttu-id="d68a9-904">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-904">taxid#</span></span>
  
<span data-ttu-id="d68a9-905">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-905">tax file</span></span>
  
<span data-ttu-id="d68a9-906">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-906">tax file no.</span></span>
  
<span data-ttu-id="d68a9-907">Numéro d'identification personnel</span><span class="sxs-lookup"><span data-stu-id="d68a9-907">personal id number</span></span>
  
<span data-ttu-id="d68a9-908">skatt ID Nummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-908">skatt id nummer</span></span>
  
<span data-ttu-id="d68a9-909">skatt Identifikation</span><span class="sxs-lookup"><span data-stu-id="d68a9-909">skatt identifikation</span></span>
  
<span data-ttu-id="d68a9-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="d68a9-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="d68a9-911">R.U.</span><span class="sxs-lookup"><span data-stu-id="d68a9-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="d68a9-912">Format</span><span class="sxs-lookup"><span data-stu-id="d68a9-912">Format</span></span>

<span data-ttu-id="d68a9-913">Référence de conTribuable unique (UTR): 10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="d68a9-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="d68a9-p103">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «numéro d'assurance nationale britannique (NINO)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d68a9-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d68a9-916">Modèle</span><span class="sxs-lookup"><span data-stu-id="d68a9-916">Pattern</span></span>

<span data-ttu-id="d68a9-917">Référence de conTribuable unique (UTR): 10 chiffres</span><span class="sxs-lookup"><span data-stu-id="d68a9-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="d68a9-p104">Numéro d'assurance nationale (NINO): pour plus d'informations, reportez-vous à la section «numéro d'assurance nationale britannique (NINO)» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d68a9-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d68a9-920">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d68a9-920">Checksum</span></span>

<span data-ttu-id="d68a9-921">Oui</span><span class="sxs-lookup"><span data-stu-id="d68a9-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d68a9-922">Définition</span><span class="sxs-lookup"><span data-stu-id="d68a9-922">Definition</span></span>

<span data-ttu-id="d68a9-923">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d68a9-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d68a9-924">La fonction `Func_uk_eu_tax_file_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d68a9-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d68a9-925">Un mot clé `Keywords_uk_eu_tax_file_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="d68a9-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="d68a9-926">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="d68a9-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="d68a9-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="d68a9-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="d68a9-928">id fiscal
</span><span class="sxs-lookup"><span data-stu-id="d68a9-928">tax id</span></span>
  
<span data-ttu-id="d68a9-929">n ° ID taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-929">tax id no.</span></span>
  
<span data-ttu-id="d68a9-930">Numéro d'identification de taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-930">tax id number</span></span>
  
<span data-ttu-id="d68a9-931">identification fiscale
</span><span class="sxs-lookup"><span data-stu-id="d68a9-931">tax identification</span></span>
  
<span data-ttu-id="d68a9-932">n ° d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="d68a9-932">tax identification#</span></span>
  
<span data-ttu-id="d68a9-933">n ° taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-933">tax no.</span></span>
  
<span data-ttu-id="d68a9-934">codes</span><span class="sxs-lookup"><span data-stu-id="d68a9-934">tax#</span></span>
  
<span data-ttu-id="d68a9-935">n ° de taxi</span><span class="sxs-lookup"><span data-stu-id="d68a9-935">taxid#</span></span>
  
<span data-ttu-id="d68a9-936">fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-936">tax file</span></span>
  
<span data-ttu-id="d68a9-937">n ° fichier taxe</span><span class="sxs-lookup"><span data-stu-id="d68a9-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d68a9-938">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d68a9-938">See also</span></span>

[<span data-ttu-id="d68a9-939">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d68a9-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

