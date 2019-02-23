---
title: Numéro de permis de conduire de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: 86be7b52aed7581fd62ab595ac2c4b63ab33aab3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217744"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="484ba-104">Numéro de permis de conduire de l'UE</span><span class="sxs-lookup"><span data-stu-id="484ba-104">EU Driver's License Number</span></span>

<span data-ttu-id="484ba-p102">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="484ba-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="484ba-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="484ba-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="484ba-108">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-108">Format</span></span>

<span data-ttu-id="484ba-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-110">Pattern</span></span>

<span data-ttu-id="484ba-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-112">Checksum</span></span>

<span data-ttu-id="484ba-113">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-114">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-114">Definition</span></span>

<span data-ttu-id="484ba-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-116">L'expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="484ba-118">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-118">Keywords</span></span>

<span data-ttu-id="484ba-119">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-119"></span></span>
|<span data-ttu-id="484ba-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-121">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-121">dl#</span></span>  <br/> <span data-ttu-id="484ba-122">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-122">driver license</span></span>  <br/> <span data-ttu-id="484ba-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-123">driver license number</span></span>  <br/> <span data-ttu-id="484ba-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-124">driver licence</span></span>  <br/> <span data-ttu-id="484ba-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-125">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-126">drivers license</span></span>  <br/> <span data-ttu-id="484ba-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-127">driver's licence</span></span>  <br/> <span data-ttu-id="484ba-128">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-128">driver's license</span></span>  <br/> <span data-ttu-id="484ba-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-129">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="484ba-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-131">driving license number</span></span>  <br/> <span data-ttu-id="484ba-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-132">dlno#</span></span>  <br/> <span data-ttu-id="484ba-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="484ba-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="484ba-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="484ba-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="484ba-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="484ba-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="484ba-136">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-136">Format</span></span>

<span data-ttu-id="484ba-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-138">Pattern</span></span>

<span data-ttu-id="484ba-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-140">Checksum</span></span>

<span data-ttu-id="484ba-141">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-142">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-142">Definition</span></span>

<span data-ttu-id="484ba-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-144">L'expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="484ba-146">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-146">Keywords</span></span>

<span data-ttu-id="484ba-147">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-147"></span></span>
|<span data-ttu-id="484ba-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-149">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-149">dl#</span></span>  <br/> <span data-ttu-id="484ba-150">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-150">driver license</span></span>  <br/> <span data-ttu-id="484ba-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-151">driver license number</span></span>  <br/> <span data-ttu-id="484ba-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-152">driver licence</span></span>  <br/> <span data-ttu-id="484ba-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-153">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-154">drivers license</span></span>  <br/> <span data-ttu-id="484ba-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-155">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-156">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-156">driver's license</span></span>  <br/> <span data-ttu-id="484ba-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-157">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-158">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-159">dlno#</span></span>  <br/> <span data-ttu-id="484ba-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="484ba-160">rijbewijs</span></span>  <br/> <span data-ttu-id="484ba-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="484ba-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="484ba-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="484ba-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="484ba-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="484ba-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="484ba-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="484ba-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="484ba-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="484ba-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="484ba-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="484ba-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="484ba-169">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-169">Format</span></span>

<span data-ttu-id="484ba-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-171">Pattern</span></span>

<span data-ttu-id="484ba-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-173">Checksum</span></span>

<span data-ttu-id="484ba-174">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-175">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-175">Definition</span></span>

<span data-ttu-id="484ba-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-177">L'expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="484ba-179">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-179">Keywords</span></span>

<span data-ttu-id="484ba-180">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-180"></span></span>
|<span data-ttu-id="484ba-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-182">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-182">dl#</span></span>  <br/> <span data-ttu-id="484ba-183">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-183">driver license</span></span>  <br/> <span data-ttu-id="484ba-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-184">driver license number</span></span>  <br/> <span data-ttu-id="484ba-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-185">driver licence</span></span>  <br/> <span data-ttu-id="484ba-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-186">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-187">drivers license</span></span>  <br/> <span data-ttu-id="484ba-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-188">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-189">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-189">driver's license</span></span>  <br/> <span data-ttu-id="484ba-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-190">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-191">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-192">driving license number</span></span>  <br/> <span data-ttu-id="484ba-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-193">dlno#</span></span>  <br/> <span data-ttu-id="484ba-194">свидетелство за Управление на мпс</span><span class="sxs-lookup"><span data-stu-id="484ba-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="484ba-195">свидетелство за Управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="484ba-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="484ba-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="484ba-196">сумпс</span></span>  <br/> <span data-ttu-id="484ba-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="484ba-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="484ba-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="484ba-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="484ba-199">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-199">Format</span></span>

<span data-ttu-id="484ba-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-201">Pattern</span></span>

<span data-ttu-id="484ba-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-203">Checksum</span></span>

<span data-ttu-id="484ba-204">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-205">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-205">Definition</span></span>

<span data-ttu-id="484ba-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-207">L'expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="484ba-209">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-209">Keywords</span></span>

<span data-ttu-id="484ba-210">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-210"></span></span>
|<span data-ttu-id="484ba-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-212">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-212">dl#</span></span>  <br/> <span data-ttu-id="484ba-213">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-213">driver license</span></span>  <br/> <span data-ttu-id="484ba-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-214">driver license number</span></span>  <br/> <span data-ttu-id="484ba-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-215">driver licence</span></span>  <br/> <span data-ttu-id="484ba-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-216">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-217">drivers license</span></span>  <br/> <span data-ttu-id="484ba-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-218">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-219">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-219">driver's license</span></span>  <br/> <span data-ttu-id="484ba-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-220">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-221">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-222">driving license number</span></span>  <br/> <span data-ttu-id="484ba-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-223">dlno#</span></span>  <br/> <span data-ttu-id="484ba-224">vozačka Dozvola</span><span class="sxs-lookup"><span data-stu-id="484ba-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="484ba-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="484ba-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="484ba-226">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-226">Format</span></span>

<span data-ttu-id="484ba-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-228">Pattern</span></span>

<span data-ttu-id="484ba-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-230">Checksum</span></span>

<span data-ttu-id="484ba-231">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-232">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-232">Definition</span></span>

<span data-ttu-id="484ba-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-234">L'expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-236">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-236">Keywords</span></span>

<span data-ttu-id="484ba-237">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-237"></span></span>
|<span data-ttu-id="484ba-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-239">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-239">dl#</span></span>  <br/> <span data-ttu-id="484ba-240">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-240">driver license</span></span>  <br/> <span data-ttu-id="484ba-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-241">driver license number</span></span>  <br/> <span data-ttu-id="484ba-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-242">driver licence</span></span>  <br/> <span data-ttu-id="484ba-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-243">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-244">drivers license</span></span>  <br/> <span data-ttu-id="484ba-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-245">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-246">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-247">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-248">driving license number</span></span>  <br/> <span data-ttu-id="484ba-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-249">dlno#</span></span>  <br/> <span data-ttu-id="484ba-250">Άδεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="484ba-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="484ba-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="484ba-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="484ba-252">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-252">Format</span></span>

<span data-ttu-id="484ba-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-254">Pattern</span></span>

<span data-ttu-id="484ba-255">Huit lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="484ba-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="484ba-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="484ba-257">A space (optional)</span></span>
    
- <span data-ttu-id="484ba-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-259">Checksum</span></span>

<span data-ttu-id="484ba-260">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-261">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-261">Definition</span></span>

<span data-ttu-id="484ba-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-263">L'expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="484ba-265">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-265">Keywords</span></span>

<span data-ttu-id="484ba-266">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-266"></span></span>
|<span data-ttu-id="484ba-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-268">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-268">dl#</span></span>  <br/> <span data-ttu-id="484ba-269">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-269">driver license</span></span>  <br/> <span data-ttu-id="484ba-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-270">driver license number</span></span>  <br/> <span data-ttu-id="484ba-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-271">driver licence</span></span>  <br/> <span data-ttu-id="484ba-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-272">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-273">drivers license</span></span>  <br/> <span data-ttu-id="484ba-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-274">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-275">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-275">driver's license</span></span>  <br/> <span data-ttu-id="484ba-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-276">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-277">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-278">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-279">driving license number</span></span>  <br/> <span data-ttu-id="484ba-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-280">dlno#</span></span>  <br/> <span data-ttu-id="484ba-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="484ba-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="484ba-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="484ba-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="484ba-283">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-283">Format</span></span>

<span data-ttu-id="484ba-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-285">Pattern</span></span>

<span data-ttu-id="484ba-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-287">Checksum</span></span>

<span data-ttu-id="484ba-288">Oui</span><span class="sxs-lookup"><span data-stu-id="484ba-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-289">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-289">Definition</span></span>

<span data-ttu-id="484ba-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-291">L'expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="484ba-293">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-293">Keywords</span></span>

<span data-ttu-id="484ba-294">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-294"></span></span>
|<span data-ttu-id="484ba-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-296">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-296">dl#</span></span>  <br/> <span data-ttu-id="484ba-297">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-297">driver license</span></span>  <br/> <span data-ttu-id="484ba-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-298">driver license number</span></span>  <br/> <span data-ttu-id="484ba-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-299">driver licence</span></span>  <br/> <span data-ttu-id="484ba-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-300">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-301">drivers license</span></span>  <br/> <span data-ttu-id="484ba-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-302">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-303">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-303">driver's license</span></span>  <br/> <span data-ttu-id="484ba-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-304">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-305">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-306">driving license number</span></span>  <br/> <span data-ttu-id="484ba-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-307">dlno#</span></span>  <br/> <span data-ttu-id="484ba-308">Kørekort</span><span class="sxs-lookup"><span data-stu-id="484ba-308">kørekort</span></span>  <br/> <span data-ttu-id="484ba-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="484ba-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="484ba-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="484ba-311">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-311">Format</span></span>

<span data-ttu-id="484ba-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-313">Pattern</span></span>

<span data-ttu-id="484ba-314">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="484ba-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="484ba-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-317">Checksum</span></span>

<span data-ttu-id="484ba-318">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-319">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-319">Definition</span></span>

<span data-ttu-id="484ba-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-321">L'expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-323">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-323">Keywords</span></span>

<span data-ttu-id="484ba-324">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-324"></span></span>
|<span data-ttu-id="484ba-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-326">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-326">dl#</span></span>  <br/> <span data-ttu-id="484ba-327">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-327">driver license</span></span>  <br/> <span data-ttu-id="484ba-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-328">driver license number</span></span>  <br/> <span data-ttu-id="484ba-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-329">driver license number</span></span>  <br/> <span data-ttu-id="484ba-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-330">driver licence</span></span>  <br/> <span data-ttu-id="484ba-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-331">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-332">drivers license</span></span>  <br/> <span data-ttu-id="484ba-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-333">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-334">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-334">driver's license</span></span>  <br/> <span data-ttu-id="484ba-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-335">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-336">driving license number</span></span>  <br/> <span data-ttu-id="484ba-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-337">dlno#</span></span>  <br/> <span data-ttu-id="484ba-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="484ba-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="484ba-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="484ba-340">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-340">Format</span></span>

<span data-ttu-id="484ba-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="484ba-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-342">Pattern</span></span>

<span data-ttu-id="484ba-343">10 chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="484ba-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="484ba-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-344">Six digits</span></span> 
    
- <span data-ttu-id="484ba-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="484ba-345">A hyphen</span></span>
    
-  <span data-ttu-id="484ba-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="484ba-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-347">Checksum</span></span>

<span data-ttu-id="484ba-348">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-349">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-349">Definition</span></span>

<span data-ttu-id="484ba-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-351">L'expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-353">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-353">Keywords</span></span>

<span data-ttu-id="484ba-354">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-354"></span></span>
|<span data-ttu-id="484ba-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-356">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-356">dl#</span></span>  <br/> <span data-ttu-id="484ba-357">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-357">driver license</span></span>  <br/> <span data-ttu-id="484ba-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-358">driver license number</span></span>  <br/> <span data-ttu-id="484ba-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-359">driver licence</span></span>  <br/> <span data-ttu-id="484ba-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-360">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-361">drivers license</span></span>  <br/> <span data-ttu-id="484ba-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-362">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-363">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-363">driver's license</span></span>  <br/> <span data-ttu-id="484ba-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-364">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-365">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-366">driving license number</span></span>  <br/> <span data-ttu-id="484ba-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-367">dlno#</span></span>  <br/> <span data-ttu-id="484ba-368">Ajokortti</span><span class="sxs-lookup"><span data-stu-id="484ba-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="484ba-369">France</span><span class="sxs-lookup"><span data-stu-id="484ba-369">France</span></span>

<span data-ttu-id="484ba-370">Pour plus d'informations, reportez-vous à la section «numéro de permis de conduire France» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="484ba-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="484ba-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="484ba-371">Germany</span></span>

<span data-ttu-id="484ba-372">Pour plus d'informations, consultez la section «numéro de permis de conduire allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="484ba-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="484ba-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="484ba-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="484ba-374">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-374">Format</span></span>

<span data-ttu-id="484ba-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-376">Pattern</span></span>

 <span data-ttu-id="484ba-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="484ba-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-378">Checksum</span></span>

<span data-ttu-id="484ba-379">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-380">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-380">Definition</span></span>

<span data-ttu-id="484ba-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-382">L'expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-384">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-384">Keywords</span></span>

<span data-ttu-id="484ba-385">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-385"></span></span>
|<span data-ttu-id="484ba-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-387">Fichier</span><span class="sxs-lookup"><span data-stu-id="484ba-387">dlL#</span></span>  <br/> <span data-ttu-id="484ba-388">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-388">driver license</span></span>  <br/> <span data-ttu-id="484ba-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-389">driver license number</span></span>  <br/> <span data-ttu-id="484ba-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-390">driver licence</span></span>  <br/> <span data-ttu-id="484ba-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-391">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-392">drivers license</span></span>  <br/> <span data-ttu-id="484ba-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-393">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-394">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-394">driver's license</span></span>  <br/> <span data-ttu-id="484ba-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-395">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-396">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-397">driving license number</span></span>  <br/> <span data-ttu-id="484ba-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-398">dlno#</span></span>  <br/> <span data-ttu-id="484ba-399">δεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="484ba-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="484ba-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="484ba-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="484ba-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="484ba-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="484ba-402">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-402">Format</span></span>

<span data-ttu-id="484ba-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-404">Pattern</span></span>

<span data-ttu-id="484ba-405">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="484ba-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="484ba-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-408">Checksum</span></span>

<span data-ttu-id="484ba-409">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-410">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-410">Definition</span></span>

<span data-ttu-id="484ba-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-412">L'expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-414">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-414">Keywords</span></span>

<span data-ttu-id="484ba-415">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-415"></span></span>
|<span data-ttu-id="484ba-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-417">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-417">dl#</span></span>  <br/> <span data-ttu-id="484ba-418">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-418">driver license</span></span>  <br/> <span data-ttu-id="484ba-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-419">driver license number</span></span>  <br/> <span data-ttu-id="484ba-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-420">driver licence</span></span>  <br/> <span data-ttu-id="484ba-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-421">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-422">drivers license</span></span>  <br/> <span data-ttu-id="484ba-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-423">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-424">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-424">driver's license</span></span>  <br/> <span data-ttu-id="484ba-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-425">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-426">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-427">driving license number</span></span>  <br/> <span data-ttu-id="484ba-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-428">dlno#</span></span>  <br/> <span data-ttu-id="484ba-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="484ba-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="484ba-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="484ba-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="484ba-431">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-431">Format</span></span>

<span data-ttu-id="484ba-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="484ba-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-433">Pattern</span></span>

<span data-ttu-id="484ba-434">Six chiffres et quatre lettres:</span><span class="sxs-lookup"><span data-stu-id="484ba-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="484ba-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-435">Six digits</span></span>
    
- <span data-ttu-id="484ba-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-437">Checksum</span></span>

<span data-ttu-id="484ba-438">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-439">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-439">Definition</span></span>

<span data-ttu-id="484ba-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-441">L'expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-443">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-443">Keywords</span></span>

<span data-ttu-id="484ba-444">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-444"></span></span>
|<span data-ttu-id="484ba-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-446">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-446">dl#</span></span>  <br/> <span data-ttu-id="484ba-447">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-447">driver license</span></span>  <br/> <span data-ttu-id="484ba-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-448">driver license number</span></span>  <br/> <span data-ttu-id="484ba-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-449">driver licence</span></span>  <br/> <span data-ttu-id="484ba-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-450">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-451">drivers license</span></span>  <br/> <span data-ttu-id="484ba-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-452">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-453">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-453">driver's license</span></span>  <br/> <span data-ttu-id="484ba-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-454">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-455">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-456">driving license number</span></span>  <br/> <span data-ttu-id="484ba-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-457">dlno#</span></span>  <br/> <span data-ttu-id="484ba-458">Ceadúnas Tiomána</span><span class="sxs-lookup"><span data-stu-id="484ba-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="484ba-459">Italie</span><span class="sxs-lookup"><span data-stu-id="484ba-459">Italy</span></span>

<span data-ttu-id="484ba-460">Pour plus d'informations, reportez-vous à la section «Italie numéro de permis de conduire» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="484ba-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="484ba-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="484ba-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="484ba-462">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-462">Format</span></span>

<span data-ttu-id="484ba-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-464">Pattern</span></span>

<span data-ttu-id="484ba-465">Trois lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="484ba-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="484ba-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-468">Checksum</span></span>

<span data-ttu-id="484ba-469">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-470">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-470">Definition</span></span>

<span data-ttu-id="484ba-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-472">L'expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-474">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-474">Keywords</span></span>

<span data-ttu-id="484ba-475">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-475"></span></span>
|<span data-ttu-id="484ba-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-477">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-477">dl#</span></span>  <br/> <span data-ttu-id="484ba-478">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-478">driver license</span></span>  <br/> <span data-ttu-id="484ba-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-479">driver license number</span></span>  <br/> <span data-ttu-id="484ba-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-480">driver licence</span></span>  <br/> <span data-ttu-id="484ba-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-481">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-482">drivers license</span></span>  <br/> <span data-ttu-id="484ba-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-483">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-484">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-484">driver's license</span></span>  <br/> <span data-ttu-id="484ba-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-485">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-486">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-487">driving license number</span></span>  <br/> <span data-ttu-id="484ba-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-488">dlno#</span></span>  <br/> <span data-ttu-id="484ba-489">autovadītāja APLIECĪBA</span><span class="sxs-lookup"><span data-stu-id="484ba-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="484ba-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="484ba-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="484ba-491">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-491">Format</span></span>

<span data-ttu-id="484ba-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-493">Pattern</span></span>

 <span data-ttu-id="484ba-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="484ba-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-495">Checksum</span></span>

<span data-ttu-id="484ba-496">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-497">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-497">Definition</span></span>

<span data-ttu-id="484ba-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-499">L'expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-501">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-501">Keywords</span></span>

<span data-ttu-id="484ba-502">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-502"></span></span>
|<span data-ttu-id="484ba-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-504">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-504">dl#</span></span>  <br/> <span data-ttu-id="484ba-505">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-505">driver license</span></span>  <br/> <span data-ttu-id="484ba-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-506">driver license number</span></span>  <br/> <span data-ttu-id="484ba-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-507">driver licence</span></span>  <br/> <span data-ttu-id="484ba-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-508">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-509">drivers license</span></span>  <br/> <span data-ttu-id="484ba-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-510">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-511">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-511">driver's license</span></span>  <br/> <span data-ttu-id="484ba-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-512">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-513">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-514">driving license number</span></span>  <br/> <span data-ttu-id="484ba-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-515">dlno#</span></span>  <br/> <span data-ttu-id="484ba-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="484ba-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="484ba-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="484ba-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="484ba-518">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-518">Format</span></span>

<span data-ttu-id="484ba-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-520">Pattern</span></span>

 <span data-ttu-id="484ba-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="484ba-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-522">Checksum</span></span>

<span data-ttu-id="484ba-523">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-524">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-524">Definition</span></span>

<span data-ttu-id="484ba-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-526">L'expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-528">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-528">Keywords</span></span>

<span data-ttu-id="484ba-529">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-529"></span></span>
|<span data-ttu-id="484ba-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-531">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-531">dl#</span></span>  <br/> <span data-ttu-id="484ba-532">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-532">driver license</span></span>  <br/> <span data-ttu-id="484ba-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-533">driver license number</span></span>  <br/> <span data-ttu-id="484ba-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-534">driver licence</span></span>  <br/> <span data-ttu-id="484ba-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-535">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-536">drivers license</span></span>  <br/> <span data-ttu-id="484ba-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-537">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-538">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-538">driver's license</span></span>  <br/> <span data-ttu-id="484ba-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-539">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-540">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-541">driving license number</span></span>  <br/> <span data-ttu-id="484ba-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-542">dlno#</span></span>  <br/> <span data-ttu-id="484ba-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="484ba-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="484ba-544">Malte</span><span class="sxs-lookup"><span data-stu-id="484ba-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="484ba-545">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-545">Format</span></span>

<span data-ttu-id="484ba-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="484ba-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-547">Pattern</span></span>

<span data-ttu-id="484ba-548">Combinaison de deux caractères et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="484ba-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="484ba-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="484ba-550">A space (optional)</span></span>
    
- <span data-ttu-id="484ba-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-551">Three digits</span></span>
    
- <span data-ttu-id="484ba-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="484ba-552">A space (optional)</span></span>
    
- <span data-ttu-id="484ba-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-554">Checksum</span></span>

<span data-ttu-id="484ba-555">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-556">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-556">Definition</span></span>

<span data-ttu-id="484ba-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-558">L'expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-560">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-560">Keywords</span></span>

<span data-ttu-id="484ba-561">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-561"></span></span>
|<span data-ttu-id="484ba-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-563">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-563">dl#</span></span>  <br/> <span data-ttu-id="484ba-564">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-564">driver license</span></span>  <br/> <span data-ttu-id="484ba-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-565">driver license number</span></span>  <br/> <span data-ttu-id="484ba-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-566">driver licence</span></span>  <br/> <span data-ttu-id="484ba-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-567">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-568">drivers license</span></span>  <br/> <span data-ttu-id="484ba-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-569">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-570">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-570">driver's license</span></span>  <br/> <span data-ttu-id="484ba-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-571">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-572">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-573">driving license number</span></span>  <br/> <span data-ttu-id="484ba-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-574">dlno#</span></span>  <br/> <span data-ttu-id="484ba-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="484ba-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="484ba-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="484ba-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="484ba-577">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-577">Format</span></span>

<span data-ttu-id="484ba-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-579">Pattern</span></span>

<span data-ttu-id="484ba-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-581">Checksum</span></span>

<span data-ttu-id="484ba-582">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-583">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-583">Definition</span></span>

<span data-ttu-id="484ba-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-585">L'expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-587">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-587">Keywords</span></span>

<span data-ttu-id="484ba-588">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-588"></span></span>
|<span data-ttu-id="484ba-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-590">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-590">dl#</span></span>  <br/> <span data-ttu-id="484ba-591">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-591">driver license</span></span>  <br/> <span data-ttu-id="484ba-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-592">driver license number</span></span>  <br/> <span data-ttu-id="484ba-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-593">driver licence</span></span>  <br/> <span data-ttu-id="484ba-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-594">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-595">drivers license</span></span>  <br/> <span data-ttu-id="484ba-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-596">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-597">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-597">driver's license</span></span>  <br/> <span data-ttu-id="484ba-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-598">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-599">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-600">driving license number</span></span>  <br/> <span data-ttu-id="484ba-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-601">dlno#</span></span>  <br/> <span data-ttu-id="484ba-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-602">permis de conduire</span></span>  <br/> <span data-ttu-id="484ba-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="484ba-603">rijbewijs</span></span>  <br/> <span data-ttu-id="484ba-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="484ba-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="484ba-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="484ba-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="484ba-606">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-606">Format</span></span>

<span data-ttu-id="484ba-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="484ba-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-608">Pattern</span></span>

<span data-ttu-id="484ba-609">14 chiffres et 2 barres obliques:</span><span class="sxs-lookup"><span data-stu-id="484ba-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="484ba-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-610">Five digits</span></span> 
    
- <span data-ttu-id="484ba-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="484ba-611">A forward slash</span></span>
    
- <span data-ttu-id="484ba-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-612">Two digits</span></span>
    
- <span data-ttu-id="484ba-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="484ba-613">A forward slash</span></span>
    
- <span data-ttu-id="484ba-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-615">Checksum</span></span>

<span data-ttu-id="484ba-616">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-617">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-617">Definition</span></span>

<span data-ttu-id="484ba-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-619">L'expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-621">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-621">Keywords</span></span>

<span data-ttu-id="484ba-622">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-622"></span></span>
|<span data-ttu-id="484ba-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-624">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-624">dl#</span></span>  <br/> <span data-ttu-id="484ba-625">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-625">driver license</span></span>  <br/> <span data-ttu-id="484ba-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-626">driver license number</span></span>  <br/> <span data-ttu-id="484ba-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-627">driver licence</span></span>  <br/> <span data-ttu-id="484ba-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-628">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-629">drivers license</span></span>  <br/> <span data-ttu-id="484ba-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-630">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-631">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-631">driver's license</span></span>  <br/> <span data-ttu-id="484ba-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-632">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-633">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-634">driving license number</span></span>  <br/> <span data-ttu-id="484ba-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-635">dlno#</span></span>  <br/> <span data-ttu-id="484ba-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="484ba-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="484ba-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="484ba-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="484ba-638">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-638">Format</span></span>

<span data-ttu-id="484ba-639">Deux lettres suivies d'un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="484ba-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-640">Pattern</span></span>

<span data-ttu-id="484ba-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux:</span><span class="sxs-lookup"><span data-stu-id="484ba-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="484ba-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="484ba-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="484ba-643">A hyphen</span></span>
    
- <span data-ttu-id="484ba-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-644">Six digits</span></span>
    
- <span data-ttu-id="484ba-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="484ba-645">A space</span></span>
    
- <span data-ttu-id="484ba-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="484ba-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-647">Checksum</span></span>

<span data-ttu-id="484ba-648">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-649">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-649">Definition</span></span>

<span data-ttu-id="484ba-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-651">L'expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-653">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-653">Keywords</span></span>

<span data-ttu-id="484ba-654">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-654"></span></span>
|<span data-ttu-id="484ba-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-656">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-656">dl#</span></span>  <br/> <span data-ttu-id="484ba-657">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-657">driver license</span></span>  <br/> <span data-ttu-id="484ba-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-658">driver license number</span></span>  <br/> <span data-ttu-id="484ba-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-659">driver licence</span></span>  <br/> <span data-ttu-id="484ba-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-660">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-661">drivers license</span></span>  <br/> <span data-ttu-id="484ba-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-662">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-663">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-663">driver's license</span></span>  <br/> <span data-ttu-id="484ba-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-664">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-665">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-666">driving license number</span></span>  <br/> <span data-ttu-id="484ba-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-667">dlno#</span></span>  <br/> <span data-ttu-id="484ba-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="484ba-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="484ba-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="484ba-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="484ba-670">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-670">Format</span></span>

<span data-ttu-id="484ba-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-672">Pattern</span></span>

<span data-ttu-id="484ba-673">Un caractère suivi de huit chiffres:</span><span class="sxs-lookup"><span data-stu-id="484ba-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="484ba-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="484ba-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="484ba-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-676">Checksum</span></span>

<span data-ttu-id="484ba-677">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-678">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-678">Definition</span></span>

<span data-ttu-id="484ba-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-680">L'expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-682">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-682">Keywords</span></span>

<span data-ttu-id="484ba-683">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-683"></span></span>
|<span data-ttu-id="484ba-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-685">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-685">dl#</span></span>  <br/> <span data-ttu-id="484ba-686">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-686">driver license</span></span>  <br/> <span data-ttu-id="484ba-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-687">driver license number</span></span>  <br/> <span data-ttu-id="484ba-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-688">driver licence</span></span>  <br/> <span data-ttu-id="484ba-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-689">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-690">drivers license</span></span>  <br/> <span data-ttu-id="484ba-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-691">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-692">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-692">driver's license</span></span>  <br/> <span data-ttu-id="484ba-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-693">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-694">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-695">driving license number</span></span>  <br/> <span data-ttu-id="484ba-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-696">dlno#</span></span>  <br/> <span data-ttu-id="484ba-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="484ba-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="484ba-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="484ba-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="484ba-699">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-699">Format</span></span>

<span data-ttu-id="484ba-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-701">Pattern</span></span>

<span data-ttu-id="484ba-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="484ba-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="484ba-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="484ba-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="484ba-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-705">Checksum</span></span>

<span data-ttu-id="484ba-706">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-707">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-707">Definition</span></span>

<span data-ttu-id="484ba-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-709">L'expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-711">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-711">Keywords</span></span>

<span data-ttu-id="484ba-712">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-712"></span></span>
|<span data-ttu-id="484ba-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-714">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-714">dl#</span></span>  <br/> <span data-ttu-id="484ba-715">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-715">driver license</span></span>  <br/> <span data-ttu-id="484ba-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-716">driver license number</span></span>  <br/> <span data-ttu-id="484ba-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-717">driver licence</span></span>  <br/> <span data-ttu-id="484ba-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-718">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-719">drivers license</span></span>  <br/> <span data-ttu-id="484ba-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-720">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-721">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-721">driver's license</span></span>  <br/> <span data-ttu-id="484ba-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-722">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-723">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-724">driving license number</span></span>  <br/> <span data-ttu-id="484ba-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-725">dlno#</span></span>  <br/> <span data-ttu-id="484ba-726">vodičský PREUKAZ</span><span class="sxs-lookup"><span data-stu-id="484ba-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="484ba-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="484ba-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="484ba-728">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-728">Format</span></span>

<span data-ttu-id="484ba-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="484ba-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-730">Pattern</span></span>

<span data-ttu-id="484ba-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="484ba-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-732">Checksum</span></span>

<span data-ttu-id="484ba-733">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-734">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-734">Definition</span></span>

<span data-ttu-id="484ba-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-736">L'expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-738">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-738">Keywords</span></span>

<span data-ttu-id="484ba-739">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-739"></span></span>
|<span data-ttu-id="484ba-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-741">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-741">dl#</span></span>  <br/> <span data-ttu-id="484ba-742">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-742">driver license</span></span>  <br/> <span data-ttu-id="484ba-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-743">driver license number</span></span>  <br/> <span data-ttu-id="484ba-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-744">driver licence</span></span>  <br/> <span data-ttu-id="484ba-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-745">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-746">drivers license</span></span>  <br/> <span data-ttu-id="484ba-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-747">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-748">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-748">driver's license</span></span>  <br/> <span data-ttu-id="484ba-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-749">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-750">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-751">driving license number</span></span>  <br/> <span data-ttu-id="484ba-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-752">dlno#</span></span>  <br/> <span data-ttu-id="484ba-753">vozniško Dovoljenje</span><span class="sxs-lookup"><span data-stu-id="484ba-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="484ba-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="484ba-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="484ba-755">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-755">Format</span></span>

<span data-ttu-id="484ba-756">Huit chiffres suivis d'un caractère</span><span class="sxs-lookup"><span data-stu-id="484ba-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-757">Pattern</span></span>

<span data-ttu-id="484ba-758">Huit chiffres suivis d'un caractère:</span><span class="sxs-lookup"><span data-stu-id="484ba-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="484ba-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-759">Eight digits</span></span> 
    
- <span data-ttu-id="484ba-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="484ba-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-761">Checksum</span></span>

<span data-ttu-id="484ba-762">Oui</span><span class="sxs-lookup"><span data-stu-id="484ba-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-763">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-763">Definition</span></span>

<span data-ttu-id="484ba-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="484ba-767">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-767">Keywords</span></span>

<span data-ttu-id="484ba-768">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-768"></span></span>
|<span data-ttu-id="484ba-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-770">dlno#</span></span>  <br/> <span data-ttu-id="484ba-771">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-771">dl#</span></span>  <br/> <span data-ttu-id="484ba-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-772">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-773">driver licence</span></span>  <br/> <span data-ttu-id="484ba-774">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-774">driver license</span></span>  <br/> <span data-ttu-id="484ba-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-775">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-776">drivers license</span></span>  <br/> <span data-ttu-id="484ba-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-777">driver's licence</span></span>  <br/> <span data-ttu-id="484ba-778">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-778">driver's license</span></span>  <br/> <span data-ttu-id="484ba-779">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="484ba-779">driving licence</span></span>  <br/> <span data-ttu-id="484ba-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-780">driving license</span></span>  <br/> <span data-ttu-id="484ba-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-781">driver licence number</span></span>  <br/> <span data-ttu-id="484ba-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-782">driver license number</span></span>  <br/> <span data-ttu-id="484ba-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-783">drivers licence number</span></span>  <br/> <span data-ttu-id="484ba-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-784">drivers license number</span></span>  <br/> <span data-ttu-id="484ba-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-785">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-786">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-787">driving licence number</span></span>  <br/> <span data-ttu-id="484ba-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-788">driving license number</span></span>  <br/> <span data-ttu-id="484ba-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-789">driving permit</span></span>  <br/> <span data-ttu-id="484ba-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-790">driving permit number</span></span>  <br/> <span data-ttu-id="484ba-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="484ba-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="484ba-792">permiso Conducción</span><span class="sxs-lookup"><span data-stu-id="484ba-792">permiso conducción</span></span>  <br/> <span data-ttu-id="484ba-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="484ba-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="484ba-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="484ba-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="484ba-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-796">licencia conducir</span></span>  <br/> <span data-ttu-id="484ba-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="484ba-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="484ba-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="484ba-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-800">permiso conducir</span></span>  <br/> <span data-ttu-id="484ba-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="484ba-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="484ba-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="484ba-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="484ba-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="484ba-804">Suède</span><span class="sxs-lookup"><span data-stu-id="484ba-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="484ba-805">Format</span><span class="sxs-lookup"><span data-stu-id="484ba-805">Format</span></span>

<span data-ttu-id="484ba-806">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="484ba-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="484ba-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="484ba-807">Pattern</span></span>

<span data-ttu-id="484ba-808">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="484ba-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="484ba-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-809">Six digits</span></span> 
    
- <span data-ttu-id="484ba-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="484ba-810">A hyphen</span></span>
    
- <span data-ttu-id="484ba-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="484ba-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="484ba-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="484ba-812">Checksum</span></span>

<span data-ttu-id="484ba-813">Non</span><span class="sxs-lookup"><span data-stu-id="484ba-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="484ba-814">Définition</span><span class="sxs-lookup"><span data-stu-id="484ba-814">Definition</span></span>

<span data-ttu-id="484ba-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="484ba-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="484ba-816">L'expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="484ba-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="484ba-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="484ba-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="484ba-818">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="484ba-818">Keywords</span></span>

<span data-ttu-id="484ba-819">| |</span><span class="sxs-lookup"><span data-stu-id="484ba-819"></span></span>
|<span data-ttu-id="484ba-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="484ba-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="484ba-821">dl#</span><span class="sxs-lookup"><span data-stu-id="484ba-821">dl#</span></span>  <br/> <span data-ttu-id="484ba-822">driver license</span><span class="sxs-lookup"><span data-stu-id="484ba-822">driver license</span></span>  <br/> <span data-ttu-id="484ba-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-823">driver license number</span></span>  <br/> <span data-ttu-id="484ba-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-824">driver licence</span></span>  <br/> <span data-ttu-id="484ba-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="484ba-825">drivers lic.</span></span>  <br/> <span data-ttu-id="484ba-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="484ba-826">drivers license</span></span>  <br/> <span data-ttu-id="484ba-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-827">drivers licence</span></span>  <br/> <span data-ttu-id="484ba-828">driver’s license</span><span class="sxs-lookup"><span data-stu-id="484ba-828">driver's license</span></span>  <br/> <span data-ttu-id="484ba-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-829">driver's license number</span></span>  <br/> <span data-ttu-id="484ba-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-830">driver's licence number</span></span>  <br/> <span data-ttu-id="484ba-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="484ba-831">driving license number</span></span>  <br/> <span data-ttu-id="484ba-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="484ba-832">dlno#</span></span>  <br/> <span data-ttu-id="484ba-833">körkort</span><span class="sxs-lookup"><span data-stu-id="484ba-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="484ba-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="484ba-834">UK</span></span>

<span data-ttu-id="484ba-p103">Pour plus d'informations, reportez-vous à la section «numéro de permis de conduire britannique» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="484ba-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="484ba-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="484ba-837">See also</span></span>

[<span data-ttu-id="484ba-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="484ba-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

