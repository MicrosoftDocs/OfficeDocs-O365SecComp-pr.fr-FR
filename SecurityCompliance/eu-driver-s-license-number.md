---
title: Numéro de permis de conduire l’Union européenne
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte type d’informations sensibles de l’UE permis de conduire numéro de licence. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528065"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="54369-104">Numéro de permis de conduire l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="54369-104">EU Driver's License Number</span></span>

<span data-ttu-id="54369-p102">Cette rubrique illustre une stratégie de protection contre la perte données lorsqu’il détecte type d’informations sensibles de l’UE permis de conduire numéro de licence. Ce type d’informations sensibles définit différents motifs, mots clés et autres pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="54369-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="54369-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="54369-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="54369-108">Format</span><span class="sxs-lookup"><span data-stu-id="54369-108">Format</span></span>

<span data-ttu-id="54369-109">Huit chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-110">Pattern</span></span>

<span data-ttu-id="54369-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-112">Checksum</span></span>

<span data-ttu-id="54369-113">Non</span><span class="sxs-lookup"><span data-stu-id="54369-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-114">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-114">Definition</span></span>

<span data-ttu-id="54369-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-116">L’expression régulière `Regex_austria_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-117">Un mot clé à partir de `Keywords_austria_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="54369-118">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-118">Keywords</span></span>

<span data-ttu-id="54369-119">| |</span><span class="sxs-lookup"><span data-stu-id="54369-119"></span></span>
|<span data-ttu-id="54369-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-121">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-121">dl#</span></span>  <br/> <span data-ttu-id="54369-122">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-122">driver license</span></span>  <br/> <span data-ttu-id="54369-123">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-123">driver license number</span></span>  <br/> <span data-ttu-id="54369-124">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-124">driver licence</span></span>  <br/> <span data-ttu-id="54369-125">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-125">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-126">drivers license</span></span>  <br/> <span data-ttu-id="54369-127">conduire permis de</span><span class="sxs-lookup"><span data-stu-id="54369-127">driver's licence</span></span>  <br/> <span data-ttu-id="54369-128">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-128">driver's license</span></span>  <br/> <span data-ttu-id="54369-129">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-129">driver's license number</span></span>  <br/> <span data-ttu-id="54369-130">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="54369-131">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-131">driving license number</span></span>  <br/> <span data-ttu-id="54369-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-132">dlno#</span></span>  <br/> <span data-ttu-id="54369-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="54369-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="54369-134">fuhrerschein Slovaquie osterreich</span><span class="sxs-lookup"><span data-stu-id="54369-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="54369-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="54369-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="54369-136">Format</span><span class="sxs-lookup"><span data-stu-id="54369-136">Format</span></span>

<span data-ttu-id="54369-137">10 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-138">Pattern</span></span>

<span data-ttu-id="54369-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-140">Checksum</span></span>

<span data-ttu-id="54369-141">Non</span><span class="sxs-lookup"><span data-stu-id="54369-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-142">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-142">Definition</span></span>

<span data-ttu-id="54369-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-144">L’expression régulière `Regex_belgium_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-145">Un mot clé à partir de `Keywords_belgium_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="54369-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-146">Keywords</span></span>

<span data-ttu-id="54369-147">| |</span><span class="sxs-lookup"><span data-stu-id="54369-147"></span></span>
|<span data-ttu-id="54369-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-149">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-149">dl#</span></span>  <br/> <span data-ttu-id="54369-150">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-150">driver license</span></span>  <br/> <span data-ttu-id="54369-151">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-151">driver license number</span></span>  <br/> <span data-ttu-id="54369-152">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-152">driver licence</span></span>  <br/> <span data-ttu-id="54369-153">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-153">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-154">drivers license</span></span>  <br/> <span data-ttu-id="54369-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-155">drivers licence</span></span>  <br/> <span data-ttu-id="54369-156">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-156">driver's license</span></span>  <br/> <span data-ttu-id="54369-157">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-157">driver's license number</span></span>  <br/> <span data-ttu-id="54369-158">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-158">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-159">dlno#</span></span>  <br/> <span data-ttu-id="54369-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="54369-160">rijbewijs</span></span>  <br/> <span data-ttu-id="54369-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="54369-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="54369-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="54369-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="54369-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="54369-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="54369-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="54369-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="54369-165">führerschein-nr</span><span class="sxs-lookup"><span data-stu-id="54369-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="54369-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="54369-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="54369-167">fuehrerschein-nr</span><span class="sxs-lookup"><span data-stu-id="54369-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="54369-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="54369-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="54369-169">Format</span><span class="sxs-lookup"><span data-stu-id="54369-169">Format</span></span>

<span data-ttu-id="54369-170">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-171">Pattern</span></span>

<span data-ttu-id="54369-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-173">Checksum</span></span>

<span data-ttu-id="54369-174">Non</span><span class="sxs-lookup"><span data-stu-id="54369-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-175">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-175">Definition</span></span>

<span data-ttu-id="54369-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-177">L’expression régulière `Regex_bulgaria_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-178">Un mot clé à partir de `Keywords_bulgaria_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="54369-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-179">Keywords</span></span>

<span data-ttu-id="54369-180">| |</span><span class="sxs-lookup"><span data-stu-id="54369-180"></span></span>
|<span data-ttu-id="54369-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-182">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-182">dl#</span></span>  <br/> <span data-ttu-id="54369-183">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-183">driver license</span></span>  <br/> <span data-ttu-id="54369-184">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-184">driver license number</span></span>  <br/> <span data-ttu-id="54369-185">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-185">driver licence</span></span>  <br/> <span data-ttu-id="54369-186">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-186">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-187">drivers license</span></span>  <br/> <span data-ttu-id="54369-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-188">drivers licence</span></span>  <br/> <span data-ttu-id="54369-189">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-189">driver's license</span></span>  <br/> <span data-ttu-id="54369-190">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-190">driver's license number</span></span>  <br/> <span data-ttu-id="54369-191">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-191">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-192">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-192">driving license number</span></span>  <br/> <span data-ttu-id="54369-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-193">dlno#</span></span>  <br/> <span data-ttu-id="54369-194">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС</span><span class="sxs-lookup"><span data-stu-id="54369-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="54369-195">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО</span><span class="sxs-lookup"><span data-stu-id="54369-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="54369-196">СУМПС</span><span class="sxs-lookup"><span data-stu-id="54369-196">сумпс</span></span>  <br/> <span data-ttu-id="54369-197">ШОФЬОРСКА КНИЖКА</span><span class="sxs-lookup"><span data-stu-id="54369-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="54369-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="54369-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="54369-199">Format</span><span class="sxs-lookup"><span data-stu-id="54369-199">Format</span></span>

<span data-ttu-id="54369-200">Huit chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-201">Pattern</span></span>

<span data-ttu-id="54369-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-203">Checksum</span></span>

<span data-ttu-id="54369-204">Non</span><span class="sxs-lookup"><span data-stu-id="54369-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-205">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-205">Definition</span></span>

<span data-ttu-id="54369-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-207">L’expression régulière `Regex_croatia_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-208">Un mot clé à partir de `Keywords_croatia_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="54369-209">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-209">Keywords</span></span>

<span data-ttu-id="54369-210">| |</span><span class="sxs-lookup"><span data-stu-id="54369-210"></span></span>
|<span data-ttu-id="54369-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-212">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-212">dl#</span></span>  <br/> <span data-ttu-id="54369-213">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-213">driver license</span></span>  <br/> <span data-ttu-id="54369-214">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-214">driver license number</span></span>  <br/> <span data-ttu-id="54369-215">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-215">driver licence</span></span>  <br/> <span data-ttu-id="54369-216">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-216">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-217">drivers license</span></span>  <br/> <span data-ttu-id="54369-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-218">drivers licence</span></span>  <br/> <span data-ttu-id="54369-219">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-219">driver's license</span></span>  <br/> <span data-ttu-id="54369-220">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-220">driver's license number</span></span>  <br/> <span data-ttu-id="54369-221">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-221">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-222">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-222">driving license number</span></span>  <br/> <span data-ttu-id="54369-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-223">dlno#</span></span>  <br/> <span data-ttu-id="54369-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="54369-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="54369-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="54369-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="54369-226">Format</span><span class="sxs-lookup"><span data-stu-id="54369-226">Format</span></span>

<span data-ttu-id="54369-227">12 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-228">Pattern</span></span>

<span data-ttu-id="54369-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-230">Checksum</span></span>

<span data-ttu-id="54369-231">Non</span><span class="sxs-lookup"><span data-stu-id="54369-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-232">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-232">Definition</span></span>

<span data-ttu-id="54369-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-234">L’expression régulière `Regex_cyprus_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-235">Un mot clé à partir de `Keywords_cyprus_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-236">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-236">Keywords</span></span>

<span data-ttu-id="54369-237">| |</span><span class="sxs-lookup"><span data-stu-id="54369-237"></span></span>
|<span data-ttu-id="54369-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-239">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-239">dl#</span></span>  <br/> <span data-ttu-id="54369-240">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-240">driver license</span></span>  <br/> <span data-ttu-id="54369-241">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-241">driver license number</span></span>  <br/> <span data-ttu-id="54369-242">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-242">driver licence</span></span>  <br/> <span data-ttu-id="54369-243">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-243">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-244">drivers license</span></span>  <br/> <span data-ttu-id="54369-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-245">drivers licence</span></span>  <br/> <span data-ttu-id="54369-246">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-246">driver's license number</span></span>  <br/> <span data-ttu-id="54369-247">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-247">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-248">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-248">driving license number</span></span>  <br/> <span data-ttu-id="54369-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-249">dlno#</span></span>  <br/> <span data-ttu-id="54369-250">ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="54369-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="54369-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="54369-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="54369-252">Format</span><span class="sxs-lookup"><span data-stu-id="54369-252">Format</span></span>

<span data-ttu-id="54369-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-254">Pattern</span></span>

<span data-ttu-id="54369-255">Huit lettres et chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="54369-256">Deux lettres (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="54369-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="54369-257">A space (optional)</span></span>
    
- <span data-ttu-id="54369-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-259">Checksum</span></span>

<span data-ttu-id="54369-260">Non</span><span class="sxs-lookup"><span data-stu-id="54369-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-261">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-261">Definition</span></span>

<span data-ttu-id="54369-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-263">L’expression régulière `Regex_czech_republic_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-264">Un mot clé à partir de `Keywords_czech_republic_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="54369-265">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-265">Keywords</span></span>

<span data-ttu-id="54369-266">| |</span><span class="sxs-lookup"><span data-stu-id="54369-266"></span></span>
|<span data-ttu-id="54369-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-268">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-268">dl#</span></span>  <br/> <span data-ttu-id="54369-269">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-269">driver license</span></span>  <br/> <span data-ttu-id="54369-270">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-270">driver license number</span></span>  <br/> <span data-ttu-id="54369-271">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-271">driver licence</span></span>  <br/> <span data-ttu-id="54369-272">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-272">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-273">drivers license</span></span>  <br/> <span data-ttu-id="54369-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-274">drivers licence</span></span>  <br/> <span data-ttu-id="54369-275">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-275">driver's license</span></span>  <br/> <span data-ttu-id="54369-276">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-276">driver's license number</span></span>  <br/> <span data-ttu-id="54369-277">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-277">driver's license number</span></span>  <br/> <span data-ttu-id="54369-278">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-278">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-279">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-279">driving license number</span></span>  <br/> <span data-ttu-id="54369-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-280">dlno#</span></span>  <br/> <span data-ttu-id="54369-281">Řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="54369-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="54369-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="54369-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="54369-283">Format</span><span class="sxs-lookup"><span data-stu-id="54369-283">Format</span></span>

<span data-ttu-id="54369-284">Huit chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-285">Pattern</span></span>

<span data-ttu-id="54369-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-287">Checksum</span></span>

<span data-ttu-id="54369-288">Oui</span><span class="sxs-lookup"><span data-stu-id="54369-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-289">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-289">Definition</span></span>

<span data-ttu-id="54369-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-291">L’expression régulière `Regex_denmark_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-292">Un mot clé à partir de `Keywords_denmark_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="54369-293">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-293">Keywords</span></span>

<span data-ttu-id="54369-294">| |</span><span class="sxs-lookup"><span data-stu-id="54369-294"></span></span>
|<span data-ttu-id="54369-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-296">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-296">dl#</span></span>  <br/> <span data-ttu-id="54369-297">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-297">driver license</span></span>  <br/> <span data-ttu-id="54369-298">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-298">driver license number</span></span>  <br/> <span data-ttu-id="54369-299">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-299">driver licence</span></span>  <br/> <span data-ttu-id="54369-300">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-300">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-301">drivers license</span></span>  <br/> <span data-ttu-id="54369-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-302">drivers licence</span></span>  <br/> <span data-ttu-id="54369-303">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-303">driver's license</span></span>  <br/> <span data-ttu-id="54369-304">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-304">driver's license number</span></span>  <br/> <span data-ttu-id="54369-305">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-305">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-306">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-306">driving license number</span></span>  <br/> <span data-ttu-id="54369-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-307">dlno#</span></span>  <br/> <span data-ttu-id="54369-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="54369-308">kørekort</span></span>  <br/> <span data-ttu-id="54369-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="54369-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="54369-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="54369-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="54369-311">Format</span><span class="sxs-lookup"><span data-stu-id="54369-311">Format</span></span>

<span data-ttu-id="54369-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-313">Pattern</span></span>

<span data-ttu-id="54369-314">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="54369-315">Les lettres « ET « (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="54369-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-317">Checksum</span></span>

<span data-ttu-id="54369-318">Non</span><span class="sxs-lookup"><span data-stu-id="54369-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-319">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-319">Definition</span></span>

<span data-ttu-id="54369-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-321">L’expression régulière `Regex_estonia_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-322">Un mot clé à partir de `Keywords_estonia_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-323">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-323">Keywords</span></span>

<span data-ttu-id="54369-324">| |</span><span class="sxs-lookup"><span data-stu-id="54369-324"></span></span>
|<span data-ttu-id="54369-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-326">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-326">dl#</span></span>  <br/> <span data-ttu-id="54369-327">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-327">driver license</span></span>  <br/> <span data-ttu-id="54369-328">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-328">driver license number</span></span>  <br/> <span data-ttu-id="54369-329">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-329">driver license number</span></span>  <br/> <span data-ttu-id="54369-330">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-330">driver licence</span></span>  <br/> <span data-ttu-id="54369-331">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-331">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-332">drivers license</span></span>  <br/> <span data-ttu-id="54369-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-333">drivers licence</span></span>  <br/> <span data-ttu-id="54369-334">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-334">driver's license</span></span>  <br/> <span data-ttu-id="54369-335">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-335">driver's license number</span></span>  <br/> <span data-ttu-id="54369-336">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-336">driving license number</span></span>  <br/> <span data-ttu-id="54369-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-337">dlno#</span></span>  <br/> <span data-ttu-id="54369-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="54369-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="54369-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="54369-340">Format</span><span class="sxs-lookup"><span data-stu-id="54369-340">Format</span></span>

<span data-ttu-id="54369-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="54369-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-342">Pattern</span></span>

<span data-ttu-id="54369-343">10 chiffres contenant un trait d’union :</span><span class="sxs-lookup"><span data-stu-id="54369-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="54369-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-344">Six digits</span></span> 
    
- <span data-ttu-id="54369-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="54369-345">A hyphen</span></span>
    
-  <span data-ttu-id="54369-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="54369-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-347">Checksum</span></span>

<span data-ttu-id="54369-348">Non</span><span class="sxs-lookup"><span data-stu-id="54369-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-349">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-349">Definition</span></span>

<span data-ttu-id="54369-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-351">L’expression régulière `Regex_finland_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-352">Un mot clé à partir de `Keywords_finland_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-353">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-353">Keywords</span></span>

<span data-ttu-id="54369-354">| |</span><span class="sxs-lookup"><span data-stu-id="54369-354"></span></span>
|<span data-ttu-id="54369-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-356">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-356">dl#</span></span>  <br/> <span data-ttu-id="54369-357">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-357">driver license</span></span>  <br/> <span data-ttu-id="54369-358">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-358">driver license number</span></span>  <br/> <span data-ttu-id="54369-359">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-359">driver licence</span></span>  <br/> <span data-ttu-id="54369-360">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-360">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-361">drivers license</span></span>  <br/> <span data-ttu-id="54369-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-362">drivers licence</span></span>  <br/> <span data-ttu-id="54369-363">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-363">driver's license</span></span>  <br/> <span data-ttu-id="54369-364">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-364">driver's license number</span></span>  <br/> <span data-ttu-id="54369-365">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-365">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-366">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-366">driving license number</span></span>  <br/> <span data-ttu-id="54369-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-367">dlno#</span></span>  <br/> <span data-ttu-id="54369-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="54369-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="54369-369">France</span><span class="sxs-lookup"><span data-stu-id="54369-369">France</span></span>

<span data-ttu-id="54369-370">Pour plus d’informations, voir la section « Numéro de permis de conduire France » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="54369-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="54369-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="54369-371">Germany</span></span>

<span data-ttu-id="54369-372">Pour plus d’informations, voir la section « Numéro de permis de conduire Allemagne » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="54369-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="54369-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="54369-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="54369-374">Format</span><span class="sxs-lookup"><span data-stu-id="54369-374">Format</span></span>

<span data-ttu-id="54369-375">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-376">Pattern</span></span>

 <span data-ttu-id="54369-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="54369-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-378">Checksum</span></span>

<span data-ttu-id="54369-379">Non</span><span class="sxs-lookup"><span data-stu-id="54369-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-380">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-380">Definition</span></span>

<span data-ttu-id="54369-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-382">L’expression régulière `Regex_greece_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-383">Un mot clé à partir de `Keywords_greece_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-384">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-384">Keywords</span></span>

<span data-ttu-id="54369-385">| |</span><span class="sxs-lookup"><span data-stu-id="54369-385"></span></span>
|<span data-ttu-id="54369-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-387">dlL #</span><span class="sxs-lookup"><span data-stu-id="54369-387">dlL#</span></span>  <br/> <span data-ttu-id="54369-388">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-388">driver license</span></span>  <br/> <span data-ttu-id="54369-389">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-389">driver license number</span></span>  <br/> <span data-ttu-id="54369-390">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-390">driver licence</span></span>  <br/> <span data-ttu-id="54369-391">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-391">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-392">drivers license</span></span>  <br/> <span data-ttu-id="54369-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-393">drivers licence</span></span>  <br/> <span data-ttu-id="54369-394">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-394">driver's license</span></span>  <br/> <span data-ttu-id="54369-395">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-395">driver's license number</span></span>  <br/> <span data-ttu-id="54369-396">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-396">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-397">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-397">driving license number</span></span>  <br/> <span data-ttu-id="54369-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-398">dlno#</span></span>  <br/> <span data-ttu-id="54369-399">ΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="54369-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="54369-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="54369-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="54369-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="54369-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="54369-402">Format</span><span class="sxs-lookup"><span data-stu-id="54369-402">Format</span></span>

<span data-ttu-id="54369-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-404">Pattern</span></span>

<span data-ttu-id="54369-405">Deux lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="54369-406">Deux lettres (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="54369-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-408">Checksum</span></span>

<span data-ttu-id="54369-409">Non</span><span class="sxs-lookup"><span data-stu-id="54369-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-410">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-410">Definition</span></span>

<span data-ttu-id="54369-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-412">L’expression régulière `Regex_hungary_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-413">Un mot clé à partir de `Keywords_hungary_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-414">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-414">Keywords</span></span>

<span data-ttu-id="54369-415">| |</span><span class="sxs-lookup"><span data-stu-id="54369-415"></span></span>
|<span data-ttu-id="54369-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-417">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-417">dl#</span></span>  <br/> <span data-ttu-id="54369-418">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-418">driver license</span></span>  <br/> <span data-ttu-id="54369-419">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-419">driver license number</span></span>  <br/> <span data-ttu-id="54369-420">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-420">driver licence</span></span>  <br/> <span data-ttu-id="54369-421">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-421">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-422">drivers license</span></span>  <br/> <span data-ttu-id="54369-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-423">drivers licence</span></span>  <br/> <span data-ttu-id="54369-424">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-424">driver's license</span></span>  <br/> <span data-ttu-id="54369-425">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-425">driver's license number</span></span>  <br/> <span data-ttu-id="54369-426">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-426">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-427">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-427">driving license number</span></span>  <br/> <span data-ttu-id="54369-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-428">dlno#</span></span>  <br/> <span data-ttu-id="54369-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="54369-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="54369-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="54369-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="54369-431">Format</span><span class="sxs-lookup"><span data-stu-id="54369-431">Format</span></span>

<span data-ttu-id="54369-432">Six chiffres suivies de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="54369-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-433">Pattern</span></span>

<span data-ttu-id="54369-434">Six chiffres et quatre lettres :</span><span class="sxs-lookup"><span data-stu-id="54369-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="54369-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-435">Six digits</span></span>
    
- <span data-ttu-id="54369-436">Quatre lettres (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-437">Checksum</span></span>

<span data-ttu-id="54369-438">Non</span><span class="sxs-lookup"><span data-stu-id="54369-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-439">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-439">Definition</span></span>

<span data-ttu-id="54369-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-441">L’expression régulière `Regex_ireland_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-442">Un mot clé à partir de `Keywords_ireland_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-443">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-443">Keywords</span></span>

<span data-ttu-id="54369-444">| |</span><span class="sxs-lookup"><span data-stu-id="54369-444"></span></span>
|<span data-ttu-id="54369-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-446">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-446">dl#</span></span>  <br/> <span data-ttu-id="54369-447">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-447">driver license</span></span>  <br/> <span data-ttu-id="54369-448">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-448">driver license number</span></span>  <br/> <span data-ttu-id="54369-449">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-449">driver licence</span></span>  <br/> <span data-ttu-id="54369-450">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-450">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-451">drivers license</span></span>  <br/> <span data-ttu-id="54369-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-452">drivers licence</span></span>  <br/> <span data-ttu-id="54369-453">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-453">driver's license</span></span>  <br/> <span data-ttu-id="54369-454">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-454">driver's license number</span></span>  <br/> <span data-ttu-id="54369-455">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-455">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-456">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-456">driving license number</span></span>  <br/> <span data-ttu-id="54369-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-457">dlno#</span></span>  <br/> <span data-ttu-id="54369-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="54369-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="54369-459">Italie</span><span class="sxs-lookup"><span data-stu-id="54369-459">Italy</span></span>

<span data-ttu-id="54369-460">Pour plus d’informations, voir la section « Numéro de permis de conduire Italie » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="54369-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="54369-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="54369-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="54369-462">Format</span><span class="sxs-lookup"><span data-stu-id="54369-462">Format</span></span>

<span data-ttu-id="54369-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-464">Pattern</span></span>

<span data-ttu-id="54369-465">Trois lettres et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="54369-466">Trois lettres (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="54369-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-468">Checksum</span></span>

<span data-ttu-id="54369-469">Non</span><span class="sxs-lookup"><span data-stu-id="54369-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-470">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-470">Definition</span></span>

<span data-ttu-id="54369-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-472">L’expression régulière `Regex_latvia_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-473">Un mot clé à partir de `Keywords_latvia_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-474">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-474">Keywords</span></span>

<span data-ttu-id="54369-475">| |</span><span class="sxs-lookup"><span data-stu-id="54369-475"></span></span>
|<span data-ttu-id="54369-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-477">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-477">dl#</span></span>  <br/> <span data-ttu-id="54369-478">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-478">driver license</span></span>  <br/> <span data-ttu-id="54369-479">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-479">driver license number</span></span>  <br/> <span data-ttu-id="54369-480">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-480">driver licence</span></span>  <br/> <span data-ttu-id="54369-481">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-481">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-482">drivers license</span></span>  <br/> <span data-ttu-id="54369-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-483">drivers licence</span></span>  <br/> <span data-ttu-id="54369-484">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-484">driver's license</span></span>  <br/> <span data-ttu-id="54369-485">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-485">driver's license number</span></span>  <br/> <span data-ttu-id="54369-486">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-486">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-487">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-487">driving license number</span></span>  <br/> <span data-ttu-id="54369-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-488">dlno#</span></span>  <br/> <span data-ttu-id="54369-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="54369-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="54369-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="54369-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="54369-491">Format</span><span class="sxs-lookup"><span data-stu-id="54369-491">Format</span></span>

<span data-ttu-id="54369-492">Huit chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-493">Pattern</span></span>

 <span data-ttu-id="54369-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="54369-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-495">Checksum</span></span>

<span data-ttu-id="54369-496">Non</span><span class="sxs-lookup"><span data-stu-id="54369-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-497">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-497">Definition</span></span>

<span data-ttu-id="54369-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-499">L’expression régulière `Regex_lithuania_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-500">Un mot clé à partir de `Keywords_lithuania_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-501">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-501">Keywords</span></span>

<span data-ttu-id="54369-502">| |</span><span class="sxs-lookup"><span data-stu-id="54369-502"></span></span>
|<span data-ttu-id="54369-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-504">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-504">dl#</span></span>  <br/> <span data-ttu-id="54369-505">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-505">driver license</span></span>  <br/> <span data-ttu-id="54369-506">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-506">driver license number</span></span>  <br/> <span data-ttu-id="54369-507">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-507">driver licence</span></span>  <br/> <span data-ttu-id="54369-508">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-508">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-509">drivers license</span></span>  <br/> <span data-ttu-id="54369-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-510">drivers licence</span></span>  <br/> <span data-ttu-id="54369-511">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-511">driver's license</span></span>  <br/> <span data-ttu-id="54369-512">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-512">driver's license number</span></span>  <br/> <span data-ttu-id="54369-513">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-513">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-514">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-514">driving license number</span></span>  <br/> <span data-ttu-id="54369-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-515">dlno#</span></span>  <br/> <span data-ttu-id="54369-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="54369-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="54369-517">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="54369-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="54369-518">Format</span><span class="sxs-lookup"><span data-stu-id="54369-518">Format</span></span>

<span data-ttu-id="54369-519">Six chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-520">Pattern</span></span>

 <span data-ttu-id="54369-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="54369-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-522">Checksum</span></span>

<span data-ttu-id="54369-523">Non</span><span class="sxs-lookup"><span data-stu-id="54369-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-524">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-524">Definition</span></span>

<span data-ttu-id="54369-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-526">L’expression régulière `Regex_luxemburg_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-527">Un mot clé à partir de `Keywords_luxemburg_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-528">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-528">Keywords</span></span>

<span data-ttu-id="54369-529">| |</span><span class="sxs-lookup"><span data-stu-id="54369-529"></span></span>
|<span data-ttu-id="54369-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-531">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-531">dl#</span></span>  <br/> <span data-ttu-id="54369-532">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-532">driver license</span></span>  <br/> <span data-ttu-id="54369-533">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-533">driver license number</span></span>  <br/> <span data-ttu-id="54369-534">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-534">driver licence</span></span>  <br/> <span data-ttu-id="54369-535">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-535">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-536">drivers license</span></span>  <br/> <span data-ttu-id="54369-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-537">drivers licence</span></span>  <br/> <span data-ttu-id="54369-538">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-538">driver's license</span></span>  <br/> <span data-ttu-id="54369-539">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-539">driver's license number</span></span>  <br/> <span data-ttu-id="54369-540">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-540">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-541">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-541">driving license number</span></span>  <br/> <span data-ttu-id="54369-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-542">dlno#</span></span>  <br/> <span data-ttu-id="54369-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="54369-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="54369-544">Malte</span><span class="sxs-lookup"><span data-stu-id="54369-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="54369-545">Format</span><span class="sxs-lookup"><span data-stu-id="54369-545">Format</span></span>

<span data-ttu-id="54369-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="54369-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-547">Pattern</span></span>

<span data-ttu-id="54369-548">Combinaison de deux caractères et six chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="54369-549">Deux caractères (chiffres ou lettres, qui ne respecte pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="54369-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="54369-550">A space (optional)</span></span>
    
- <span data-ttu-id="54369-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-551">Three digits</span></span>
    
- <span data-ttu-id="54369-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="54369-552">A space (optional)</span></span>
    
- <span data-ttu-id="54369-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-554">Checksum</span></span>

<span data-ttu-id="54369-555">Non</span><span class="sxs-lookup"><span data-stu-id="54369-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-556">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-556">Definition</span></span>

<span data-ttu-id="54369-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-558">L’expression régulière `Regex_malta_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-559">Un mot clé à partir de `Keywords_malta_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-560">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-560">Keywords</span></span>

<span data-ttu-id="54369-561">| |</span><span class="sxs-lookup"><span data-stu-id="54369-561"></span></span>
|<span data-ttu-id="54369-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-563">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-563">dl#</span></span>  <br/> <span data-ttu-id="54369-564">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-564">driver license</span></span>  <br/> <span data-ttu-id="54369-565">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-565">driver license number</span></span>  <br/> <span data-ttu-id="54369-566">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-566">driver licence</span></span>  <br/> <span data-ttu-id="54369-567">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-567">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-568">drivers license</span></span>  <br/> <span data-ttu-id="54369-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-569">drivers licence</span></span>  <br/> <span data-ttu-id="54369-570">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-570">driver's license</span></span>  <br/> <span data-ttu-id="54369-571">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-571">driver's license number</span></span>  <br/> <span data-ttu-id="54369-572">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-572">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-573">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-573">driving license number</span></span>  <br/> <span data-ttu-id="54369-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-574">dlno#</span></span>  <br/> <span data-ttu-id="54369-575">tâches liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="54369-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="54369-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="54369-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="54369-577">Format</span><span class="sxs-lookup"><span data-stu-id="54369-577">Format</span></span>

<span data-ttu-id="54369-578">10 chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-579">Pattern</span></span>

<span data-ttu-id="54369-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-581">Checksum</span></span>

<span data-ttu-id="54369-582">Non</span><span class="sxs-lookup"><span data-stu-id="54369-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-583">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-583">Definition</span></span>

<span data-ttu-id="54369-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-585">L’expression régulière `Regex_netherlands_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-586">Un mot clé à partir de `Keywords_netherlands_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-587">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-587">Keywords</span></span>

<span data-ttu-id="54369-588">| |</span><span class="sxs-lookup"><span data-stu-id="54369-588"></span></span>
|<span data-ttu-id="54369-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-590">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-590">dl#</span></span>  <br/> <span data-ttu-id="54369-591">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-591">driver license</span></span>  <br/> <span data-ttu-id="54369-592">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-592">driver license number</span></span>  <br/> <span data-ttu-id="54369-593">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-593">driver licence</span></span>  <br/> <span data-ttu-id="54369-594">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-594">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-595">drivers license</span></span>  <br/> <span data-ttu-id="54369-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-596">drivers licence</span></span>  <br/> <span data-ttu-id="54369-597">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-597">driver's license</span></span>  <br/> <span data-ttu-id="54369-598">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-598">driver's license number</span></span>  <br/> <span data-ttu-id="54369-599">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-599">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-600">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-600">driving license number</span></span>  <br/> <span data-ttu-id="54369-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-601">dlno#</span></span>  <br/> <span data-ttu-id="54369-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-602">permis de conduire</span></span>  <br/> <span data-ttu-id="54369-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="54369-603">rijbewijs</span></span>  <br/> <span data-ttu-id="54369-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="54369-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="54369-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="54369-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="54369-606">Format</span><span class="sxs-lookup"><span data-stu-id="54369-606">Format</span></span>

<span data-ttu-id="54369-607">14 chiffres contenant des barres 2 obliques</span><span class="sxs-lookup"><span data-stu-id="54369-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-608">Pattern</span></span>

<span data-ttu-id="54369-609">14 chiffres et des barres 2 obliques :</span><span class="sxs-lookup"><span data-stu-id="54369-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="54369-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-610">Five digits</span></span> 
    
- <span data-ttu-id="54369-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="54369-611">A forward slash</span></span>
    
- <span data-ttu-id="54369-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-612">Two digits</span></span>
    
- <span data-ttu-id="54369-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="54369-613">A forward slash</span></span>
    
- <span data-ttu-id="54369-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-615">Checksum</span></span>

<span data-ttu-id="54369-616">Non</span><span class="sxs-lookup"><span data-stu-id="54369-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-617">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-617">Definition</span></span>

<span data-ttu-id="54369-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-619">L’expression régulière `Regex_poland_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-620">Un mot clé à partir de `Keywords_poland_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-621">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-621">Keywords</span></span>

<span data-ttu-id="54369-622">| |</span><span class="sxs-lookup"><span data-stu-id="54369-622"></span></span>
|<span data-ttu-id="54369-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-624">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-624">dl#</span></span>  <br/> <span data-ttu-id="54369-625">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-625">driver license</span></span>  <br/> <span data-ttu-id="54369-626">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-626">driver license number</span></span>  <br/> <span data-ttu-id="54369-627">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-627">driver licence</span></span>  <br/> <span data-ttu-id="54369-628">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-628">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-629">drivers license</span></span>  <br/> <span data-ttu-id="54369-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-630">drivers licence</span></span>  <br/> <span data-ttu-id="54369-631">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-631">driver's license</span></span>  <br/> <span data-ttu-id="54369-632">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-632">driver's license number</span></span>  <br/> <span data-ttu-id="54369-633">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-633">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-634">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-634">driving license number</span></span>  <br/> <span data-ttu-id="54369-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-635">dlno#</span></span>  <br/> <span data-ttu-id="54369-636">uzyskać jazdy</span><span class="sxs-lookup"><span data-stu-id="54369-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="54369-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="54369-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="54369-638">Format</span><span class="sxs-lookup"><span data-stu-id="54369-638">Format</span></span>

<span data-ttu-id="54369-639">Deux lettres suivies un sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="54369-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-640">Pattern</span></span>

<span data-ttu-id="54369-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux :</span><span class="sxs-lookup"><span data-stu-id="54369-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="54369-642">Deux lettres (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="54369-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="54369-643">A hyphen</span></span>
    
- <span data-ttu-id="54369-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-644">Six digits</span></span>
    
- <span data-ttu-id="54369-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="54369-645">A space</span></span>
    
- <span data-ttu-id="54369-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="54369-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-647">Checksum</span></span>

<span data-ttu-id="54369-648">Non</span><span class="sxs-lookup"><span data-stu-id="54369-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-649">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-649">Definition</span></span>

<span data-ttu-id="54369-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-651">L’expression régulière `Regex_portugal_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-652">Un mot clé à partir de `Keywords_portugal_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-653">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-653">Keywords</span></span>

<span data-ttu-id="54369-654">| |</span><span class="sxs-lookup"><span data-stu-id="54369-654"></span></span>
|<span data-ttu-id="54369-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-656">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-656">dl#</span></span>  <br/> <span data-ttu-id="54369-657">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-657">driver license</span></span>  <br/> <span data-ttu-id="54369-658">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-658">driver license number</span></span>  <br/> <span data-ttu-id="54369-659">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-659">driver licence</span></span>  <br/> <span data-ttu-id="54369-660">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-660">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-661">drivers license</span></span>  <br/> <span data-ttu-id="54369-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-662">drivers licence</span></span>  <br/> <span data-ttu-id="54369-663">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-663">driver's license</span></span>  <br/> <span data-ttu-id="54369-664">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-664">driver's license number</span></span>  <br/> <span data-ttu-id="54369-665">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-665">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-666">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-666">driving license number</span></span>  <br/> <span data-ttu-id="54369-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-667">dlno#</span></span>  <br/> <span data-ttu-id="54369-668">carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="54369-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="54369-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="54369-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="54369-670">Format</span><span class="sxs-lookup"><span data-stu-id="54369-670">Format</span></span>

<span data-ttu-id="54369-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-672">Pattern</span></span>

<span data-ttu-id="54369-673">Un caractère suivi de huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="54369-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="54369-674">Une lettre (pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="54369-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="54369-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-676">Checksum</span></span>

<span data-ttu-id="54369-677">Non</span><span class="sxs-lookup"><span data-stu-id="54369-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-678">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-678">Definition</span></span>

<span data-ttu-id="54369-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-680">L’expression régulière `Regex_romania_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-681">Un mot clé à partir de `Keywords_romania_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-682">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-682">Keywords</span></span>

<span data-ttu-id="54369-683">| |</span><span class="sxs-lookup"><span data-stu-id="54369-683"></span></span>
|<span data-ttu-id="54369-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-685">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-685">dl#</span></span>  <br/> <span data-ttu-id="54369-686">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-686">driver license</span></span>  <br/> <span data-ttu-id="54369-687">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-687">driver license number</span></span>  <br/> <span data-ttu-id="54369-688">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-688">driver licence</span></span>  <br/> <span data-ttu-id="54369-689">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-689">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-690">drivers license</span></span>  <br/> <span data-ttu-id="54369-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-691">drivers licence</span></span>  <br/> <span data-ttu-id="54369-692">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-692">driver's license</span></span>  <br/> <span data-ttu-id="54369-693">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-693">driver's license number</span></span>  <br/> <span data-ttu-id="54369-694">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-694">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-695">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-695">driving license number</span></span>  <br/> <span data-ttu-id="54369-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-696">dlno#</span></span>  <br/> <span data-ttu-id="54369-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="54369-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="54369-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="54369-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="54369-699">Format</span><span class="sxs-lookup"><span data-stu-id="54369-699">Format</span></span>

<span data-ttu-id="54369-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-701">Pattern</span></span>

<span data-ttu-id="54369-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="54369-703">Une lettre (pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="54369-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="54369-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="54369-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-705">Checksum</span></span>

<span data-ttu-id="54369-706">Non</span><span class="sxs-lookup"><span data-stu-id="54369-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-707">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-707">Definition</span></span>

<span data-ttu-id="54369-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-709">L’expression régulière `Regex_slovakia_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-710">Un mot clé à partir de `Keywords_slovakia_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-711">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-711">Keywords</span></span>

<span data-ttu-id="54369-712">| |</span><span class="sxs-lookup"><span data-stu-id="54369-712"></span></span>
|<span data-ttu-id="54369-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-714">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-714">dl#</span></span>  <br/> <span data-ttu-id="54369-715">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-715">driver license</span></span>  <br/> <span data-ttu-id="54369-716">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-716">driver license number</span></span>  <br/> <span data-ttu-id="54369-717">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-717">driver licence</span></span>  <br/> <span data-ttu-id="54369-718">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-718">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-719">drivers license</span></span>  <br/> <span data-ttu-id="54369-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-720">drivers licence</span></span>  <br/> <span data-ttu-id="54369-721">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-721">driver's license</span></span>  <br/> <span data-ttu-id="54369-722">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-722">driver's license number</span></span>  <br/> <span data-ttu-id="54369-723">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-723">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-724">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-724">driving license number</span></span>  <br/> <span data-ttu-id="54369-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-725">dlno#</span></span>  <br/> <span data-ttu-id="54369-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="54369-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="54369-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="54369-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="54369-728">Format</span><span class="sxs-lookup"><span data-stu-id="54369-728">Format</span></span>

<span data-ttu-id="54369-729">Neuf chiffres sans espaces et les séparateurs</span><span class="sxs-lookup"><span data-stu-id="54369-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-730">Pattern</span></span>

<span data-ttu-id="54369-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="54369-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-732">Checksum</span></span>

<span data-ttu-id="54369-733">Non</span><span class="sxs-lookup"><span data-stu-id="54369-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-734">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-734">Definition</span></span>

<span data-ttu-id="54369-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-736">L’expression régulière `Regex_slovenia_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-737">Un mot clé à partir de `Keywords_slovenia_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-738">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-738">Keywords</span></span>

<span data-ttu-id="54369-739">| |</span><span class="sxs-lookup"><span data-stu-id="54369-739"></span></span>
|<span data-ttu-id="54369-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-741">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-741">dl#</span></span>  <br/> <span data-ttu-id="54369-742">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-742">driver license</span></span>  <br/> <span data-ttu-id="54369-743">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-743">driver license number</span></span>  <br/> <span data-ttu-id="54369-744">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-744">driver licence</span></span>  <br/> <span data-ttu-id="54369-745">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-745">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-746">drivers license</span></span>  <br/> <span data-ttu-id="54369-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-747">drivers licence</span></span>  <br/> <span data-ttu-id="54369-748">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-748">driver's license</span></span>  <br/> <span data-ttu-id="54369-749">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-749">driver's license number</span></span>  <br/> <span data-ttu-id="54369-750">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-750">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-751">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-751">driving license number</span></span>  <br/> <span data-ttu-id="54369-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-752">dlno#</span></span>  <br/> <span data-ttu-id="54369-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="54369-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="54369-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="54369-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="54369-755">Format</span><span class="sxs-lookup"><span data-stu-id="54369-755">Format</span></span>

<span data-ttu-id="54369-756">Huit chiffres suivies d’un caractère</span><span class="sxs-lookup"><span data-stu-id="54369-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-757">Pattern</span></span>

<span data-ttu-id="54369-758">Huit chiffres suivies d’un caractère :</span><span class="sxs-lookup"><span data-stu-id="54369-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="54369-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-759">Eight digits</span></span> 
    
- <span data-ttu-id="54369-760">Un chiffre ou une lettre (pas la casse)</span><span class="sxs-lookup"><span data-stu-id="54369-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-761">Checksum</span></span>

<span data-ttu-id="54369-762">Oui</span><span class="sxs-lookup"><span data-stu-id="54369-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-763">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-763">Definition</span></span>

<span data-ttu-id="54369-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-765">La fonction `Func_spain_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-766">Un mot clé à partir de `Keywords_spain_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="54369-767">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-767">Keywords</span></span>

<span data-ttu-id="54369-768">| |</span><span class="sxs-lookup"><span data-stu-id="54369-768"></span></span>
|<span data-ttu-id="54369-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-770">dlno#</span></span>  <br/> <span data-ttu-id="54369-771">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-771">dl#</span></span>  <br/> <span data-ttu-id="54369-772">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-772">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-773">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-773">driver licence</span></span>  <br/> <span data-ttu-id="54369-774">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-774">driver license</span></span>  <br/> <span data-ttu-id="54369-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-775">drivers licence</span></span>  <br/> <span data-ttu-id="54369-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-776">drivers license</span></span>  <br/> <span data-ttu-id="54369-777">conduire permis de</span><span class="sxs-lookup"><span data-stu-id="54369-777">driver's licence</span></span>  <br/> <span data-ttu-id="54369-778">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-778">driver's license</span></span>  <br/> <span data-ttu-id="54369-779">permis de conduire
</span><span class="sxs-lookup"><span data-stu-id="54369-779">driving licence</span></span>  <br/> <span data-ttu-id="54369-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-780">driving license</span></span>  <br/> <span data-ttu-id="54369-781">numéro de licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-781">driver licence number</span></span>  <br/> <span data-ttu-id="54369-782">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-782">driver license number</span></span>  <br/> <span data-ttu-id="54369-783">nombre de pilotes de licence</span><span class="sxs-lookup"><span data-stu-id="54369-783">drivers licence number</span></span>  <br/> <span data-ttu-id="54369-784">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-784">drivers license number</span></span>  <br/> <span data-ttu-id="54369-785">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-785">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-786">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-786">driver's license number</span></span>  <br/> <span data-ttu-id="54369-787">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-787">driving licence number</span></span>  <br/> <span data-ttu-id="54369-788">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-788">driving license number</span></span>  <br/> <span data-ttu-id="54369-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-789">driving permit</span></span>  <br/> <span data-ttu-id="54369-790">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-790">driving permit number</span></span>  <br/> <span data-ttu-id="54369-791">permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="54369-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="54369-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="54369-792">permiso conducción</span></span>  <br/> <span data-ttu-id="54369-793">Número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="54369-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="54369-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="54369-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="54369-795">Número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="54369-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="54369-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="54369-796">licencia conducir</span></span>  <br/> <span data-ttu-id="54369-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="54369-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="54369-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="54369-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="54369-799">Número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="54369-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="54369-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="54369-800">permiso conducir</span></span>  <br/> <span data-ttu-id="54369-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="54369-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="54369-802">EL carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="54369-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="54369-803">Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="54369-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="54369-804">Suède</span><span class="sxs-lookup"><span data-stu-id="54369-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="54369-805">Format</span><span class="sxs-lookup"><span data-stu-id="54369-805">Format</span></span>

<span data-ttu-id="54369-806">Dix chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="54369-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="54369-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="54369-807">Pattern</span></span>

<span data-ttu-id="54369-808">Dix chiffres contenant un trait d’union :</span><span class="sxs-lookup"><span data-stu-id="54369-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="54369-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-809">Six digits</span></span> 
    
- <span data-ttu-id="54369-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="54369-810">A hyphen</span></span>
    
- <span data-ttu-id="54369-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="54369-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="54369-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="54369-812">Checksum</span></span>

<span data-ttu-id="54369-813">Non</span><span class="sxs-lookup"><span data-stu-id="54369-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="54369-814">Définition</span><span class="sxs-lookup"><span data-stu-id="54369-814">Definition</span></span>

<span data-ttu-id="54369-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="54369-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="54369-816">L’expression régulière `Regex_sweden_eu_driver's_license_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="54369-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="54369-817">Un mot clé à partir de `Keywords_sweden_eu_driver's_license_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="54369-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="54369-818">Keywords</span><span class="sxs-lookup"><span data-stu-id="54369-818">Keywords</span></span>

<span data-ttu-id="54369-819">| |</span><span class="sxs-lookup"><span data-stu-id="54369-819"></span></span>
|<span data-ttu-id="54369-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="54369-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="54369-821">dl#</span><span class="sxs-lookup"><span data-stu-id="54369-821">dl#</span></span>  <br/> <span data-ttu-id="54369-822">driver license</span><span class="sxs-lookup"><span data-stu-id="54369-822">driver license</span></span>  <br/> <span data-ttu-id="54369-823">numéro de permis conduire</span><span class="sxs-lookup"><span data-stu-id="54369-823">driver license number</span></span>  <br/> <span data-ttu-id="54369-824">licence pilote</span><span class="sxs-lookup"><span data-stu-id="54369-824">driver licence</span></span>  <br/> <span data-ttu-id="54369-825">lic pilotes.</span><span class="sxs-lookup"><span data-stu-id="54369-825">drivers lic.</span></span>  <br/> <span data-ttu-id="54369-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="54369-826">drivers license</span></span>  <br/> <span data-ttu-id="54369-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-827">drivers licence</span></span>  <br/> <span data-ttu-id="54369-828">driver’s license</span><span class="sxs-lookup"><span data-stu-id="54369-828">driver's license</span></span>  <br/> <span data-ttu-id="54369-829">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-829">driver's license number</span></span>  <br/> <span data-ttu-id="54369-830">numéro de permis de conduire licence</span><span class="sxs-lookup"><span data-stu-id="54369-830">driver's licence number</span></span>  <br/> <span data-ttu-id="54369-831">numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="54369-831">driving license number</span></span>  <br/> <span data-ttu-id="54369-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="54369-832">dlno#</span></span>  <br/> <span data-ttu-id="54369-833">körkort</span><span class="sxs-lookup"><span data-stu-id="54369-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="54369-834">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="54369-834">UK</span></span>

<span data-ttu-id="54369-p103">Pour plus d’informations, voir la section « Numéro de permis de conduire britannique » dans [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="54369-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54369-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54369-837">See also</span></span>

[<span data-ttu-id="54369-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="54369-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

