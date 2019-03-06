---
title: Numéro de permis de conduire de l'UE
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE. Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410749"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="65b10-104">Numéro de permis de conduire de l'UE</span><span class="sxs-lookup"><span data-stu-id="65b10-104">EU Driver's License Number</span></span>

<span data-ttu-id="65b10-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE.</span><span class="sxs-lookup"><span data-stu-id="65b10-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="65b10-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="65b10-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="65b10-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="65b10-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="65b10-108">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-108">Format</span></span>

<span data-ttu-id="65b10-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-110">Pattern</span></span>

<span data-ttu-id="65b10-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-112">Checksum</span></span>

<span data-ttu-id="65b10-113">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-114">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-114">Definition</span></span>

<span data-ttu-id="65b10-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-116">L'expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="65b10-118">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-118">Keywords</span></span>

<span data-ttu-id="65b10-119">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-119"></span></span>
|<span data-ttu-id="65b10-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-121">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-121">dl#</span></span>  <br/> <span data-ttu-id="65b10-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-122">driver license</span></span>  <br/> <span data-ttu-id="65b10-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-123">driver license number</span></span>  <br/> <span data-ttu-id="65b10-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-124">driver licence</span></span>  <br/> <span data-ttu-id="65b10-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-125">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-126">drivers license</span></span>  <br/> <span data-ttu-id="65b10-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-127">driver's licence</span></span>  <br/> <span data-ttu-id="65b10-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-128">driver's license</span></span>  <br/> <span data-ttu-id="65b10-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-129">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="65b10-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-131">driving license number</span></span>  <br/> <span data-ttu-id="65b10-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-132">dlno#</span></span>  <br/> <span data-ttu-id="65b10-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="65b10-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="65b10-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="65b10-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="65b10-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="65b10-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="65b10-136">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-136">Format</span></span>

<span data-ttu-id="65b10-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-138">Pattern</span></span>

<span data-ttu-id="65b10-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-140">Checksum</span></span>

<span data-ttu-id="65b10-141">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-142">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-142">Definition</span></span>

<span data-ttu-id="65b10-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-144">L'expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="65b10-146">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-146">Keywords</span></span>

<span data-ttu-id="65b10-147">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-147"></span></span>
|<span data-ttu-id="65b10-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-149">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-149">dl#</span></span>  <br/> <span data-ttu-id="65b10-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-150">driver license</span></span>  <br/> <span data-ttu-id="65b10-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-151">driver license number</span></span>  <br/> <span data-ttu-id="65b10-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-152">driver licence</span></span>  <br/> <span data-ttu-id="65b10-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-153">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-154">drivers license</span></span>  <br/> <span data-ttu-id="65b10-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-155">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-156">driver's license</span></span>  <br/> <span data-ttu-id="65b10-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-157">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-158">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-159">dlno#</span></span>  <br/> <span data-ttu-id="65b10-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="65b10-160">rijbewijs</span></span>  <br/> <span data-ttu-id="65b10-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="65b10-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="65b10-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="65b10-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="65b10-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="65b10-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="65b10-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="65b10-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="65b10-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="65b10-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="65b10-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="65b10-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="65b10-169">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-169">Format</span></span>

<span data-ttu-id="65b10-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-171">Pattern</span></span>

<span data-ttu-id="65b10-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-173">Checksum</span></span>

<span data-ttu-id="65b10-174">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-175">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-175">Definition</span></span>

<span data-ttu-id="65b10-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-177">L'expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="65b10-179">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-179">Keywords</span></span>

<span data-ttu-id="65b10-180">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-180"></span></span>
|<span data-ttu-id="65b10-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-182">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-182">dl#</span></span>  <br/> <span data-ttu-id="65b10-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-183">driver license</span></span>  <br/> <span data-ttu-id="65b10-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-184">driver license number</span></span>  <br/> <span data-ttu-id="65b10-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-185">driver licence</span></span>  <br/> <span data-ttu-id="65b10-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-186">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-187">drivers license</span></span>  <br/> <span data-ttu-id="65b10-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-188">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-189">driver's license</span></span>  <br/> <span data-ttu-id="65b10-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-190">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-191">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-192">driving license number</span></span>  <br/> <span data-ttu-id="65b10-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-193">dlno#</span></span>  <br/> <span data-ttu-id="65b10-194">свидетелство за Управление на мпс</span><span class="sxs-lookup"><span data-stu-id="65b10-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="65b10-195">свидетелство за Управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="65b10-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="65b10-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="65b10-196">сумпс</span></span>  <br/> <span data-ttu-id="65b10-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="65b10-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="65b10-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="65b10-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="65b10-199">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-199">Format</span></span>

<span data-ttu-id="65b10-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-201">Pattern</span></span>

<span data-ttu-id="65b10-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-203">Checksum</span></span>

<span data-ttu-id="65b10-204">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-205">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-205">Definition</span></span>

<span data-ttu-id="65b10-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-207">L'expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="65b10-209">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-209">Keywords</span></span>

<span data-ttu-id="65b10-210">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-210"></span></span>
|<span data-ttu-id="65b10-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-212">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-212">dl#</span></span>  <br/> <span data-ttu-id="65b10-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-213">driver license</span></span>  <br/> <span data-ttu-id="65b10-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-214">driver license number</span></span>  <br/> <span data-ttu-id="65b10-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-215">driver licence</span></span>  <br/> <span data-ttu-id="65b10-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-216">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-217">drivers license</span></span>  <br/> <span data-ttu-id="65b10-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-218">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-219">driver's license</span></span>  <br/> <span data-ttu-id="65b10-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-220">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-221">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-222">driving license number</span></span>  <br/> <span data-ttu-id="65b10-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-223">dlno#</span></span>  <br/> <span data-ttu-id="65b10-224">vozačka Dozvola</span><span class="sxs-lookup"><span data-stu-id="65b10-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="65b10-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="65b10-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="65b10-226">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-226">Format</span></span>

<span data-ttu-id="65b10-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-228">Pattern</span></span>

<span data-ttu-id="65b10-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-230">Checksum</span></span>

<span data-ttu-id="65b10-231">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-232">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-232">Definition</span></span>

<span data-ttu-id="65b10-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-234">L'expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-236">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-236">Keywords</span></span>

<span data-ttu-id="65b10-237">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-237"></span></span>
|<span data-ttu-id="65b10-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-239">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-239">dl#</span></span>  <br/> <span data-ttu-id="65b10-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-240">driver license</span></span>  <br/> <span data-ttu-id="65b10-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-241">driver license number</span></span>  <br/> <span data-ttu-id="65b10-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-242">driver licence</span></span>  <br/> <span data-ttu-id="65b10-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-243">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-244">drivers license</span></span>  <br/> <span data-ttu-id="65b10-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-245">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-246">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-247">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-248">driving license number</span></span>  <br/> <span data-ttu-id="65b10-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-249">dlno#</span></span>  <br/> <span data-ttu-id="65b10-250">Άδεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="65b10-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="65b10-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="65b10-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="65b10-252">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-252">Format</span></span>

<span data-ttu-id="65b10-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-254">Pattern</span></span>

<span data-ttu-id="65b10-255">Huit lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="65b10-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="65b10-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="65b10-257">A space (optional)</span></span>
    
- <span data-ttu-id="65b10-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-259">Checksum</span></span>

<span data-ttu-id="65b10-260">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-261">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-261">Definition</span></span>

<span data-ttu-id="65b10-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-263">L'expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="65b10-265">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-265">Keywords</span></span>

<span data-ttu-id="65b10-266">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-266"></span></span>
|<span data-ttu-id="65b10-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-268">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-268">dl#</span></span>  <br/> <span data-ttu-id="65b10-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-269">driver license</span></span>  <br/> <span data-ttu-id="65b10-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-270">driver license number</span></span>  <br/> <span data-ttu-id="65b10-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-271">driver licence</span></span>  <br/> <span data-ttu-id="65b10-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-272">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-273">drivers license</span></span>  <br/> <span data-ttu-id="65b10-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-274">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-275">driver's license</span></span>  <br/> <span data-ttu-id="65b10-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-276">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-277">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-278">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-279">driving license number</span></span>  <br/> <span data-ttu-id="65b10-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-280">dlno#</span></span>  <br/> <span data-ttu-id="65b10-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="65b10-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="65b10-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="65b10-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="65b10-283">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-283">Format</span></span>

<span data-ttu-id="65b10-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-285">Pattern</span></span>

<span data-ttu-id="65b10-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-287">Checksum</span></span>

<span data-ttu-id="65b10-288">Oui</span><span class="sxs-lookup"><span data-stu-id="65b10-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-289">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-289">Definition</span></span>

<span data-ttu-id="65b10-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-291">L'expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="65b10-293">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-293">Keywords</span></span>

<span data-ttu-id="65b10-294">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-294"></span></span>
|<span data-ttu-id="65b10-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-296">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-296">dl#</span></span>  <br/> <span data-ttu-id="65b10-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-297">driver license</span></span>  <br/> <span data-ttu-id="65b10-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-298">driver license number</span></span>  <br/> <span data-ttu-id="65b10-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-299">driver licence</span></span>  <br/> <span data-ttu-id="65b10-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-300">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-301">drivers license</span></span>  <br/> <span data-ttu-id="65b10-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-302">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-303">driver's license</span></span>  <br/> <span data-ttu-id="65b10-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-304">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-305">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-306">driving license number</span></span>  <br/> <span data-ttu-id="65b10-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-307">dlno#</span></span>  <br/> <span data-ttu-id="65b10-308">Kørekort</span><span class="sxs-lookup"><span data-stu-id="65b10-308">kørekort</span></span>  <br/> <span data-ttu-id="65b10-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="65b10-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="65b10-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="65b10-311">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-311">Format</span></span>

<span data-ttu-id="65b10-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-313">Pattern</span></span>

<span data-ttu-id="65b10-314">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="65b10-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="65b10-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-317">Checksum</span></span>

<span data-ttu-id="65b10-318">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-319">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-319">Definition</span></span>

<span data-ttu-id="65b10-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-321">L'expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-323">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-323">Keywords</span></span>

<span data-ttu-id="65b10-324">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-324"></span></span>
|<span data-ttu-id="65b10-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-326">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-326">dl#</span></span>  <br/> <span data-ttu-id="65b10-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-327">driver license</span></span>  <br/> <span data-ttu-id="65b10-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-328">driver license number</span></span>  <br/> <span data-ttu-id="65b10-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-329">driver license number</span></span>  <br/> <span data-ttu-id="65b10-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-330">driver licence</span></span>  <br/> <span data-ttu-id="65b10-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-331">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-332">drivers license</span></span>  <br/> <span data-ttu-id="65b10-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-333">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-334">driver's license</span></span>  <br/> <span data-ttu-id="65b10-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-335">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-336">driving license number</span></span>  <br/> <span data-ttu-id="65b10-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-337">dlno#</span></span>  <br/> <span data-ttu-id="65b10-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="65b10-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="65b10-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="65b10-340">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-340">Format</span></span>

<span data-ttu-id="65b10-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="65b10-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-342">Pattern</span></span>

<span data-ttu-id="65b10-343">10 chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="65b10-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="65b10-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-344">Six digits</span></span> 
    
- <span data-ttu-id="65b10-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="65b10-345">A hyphen</span></span>
    
-  <span data-ttu-id="65b10-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="65b10-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-347">Checksum</span></span>

<span data-ttu-id="65b10-348">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-349">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-349">Definition</span></span>

<span data-ttu-id="65b10-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-351">L'expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-353">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-353">Keywords</span></span>

<span data-ttu-id="65b10-354">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-354"></span></span>
|<span data-ttu-id="65b10-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-356">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-356">dl#</span></span>  <br/> <span data-ttu-id="65b10-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-357">driver license</span></span>  <br/> <span data-ttu-id="65b10-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-358">driver license number</span></span>  <br/> <span data-ttu-id="65b10-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-359">driver licence</span></span>  <br/> <span data-ttu-id="65b10-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-360">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-361">drivers license</span></span>  <br/> <span data-ttu-id="65b10-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-362">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-363">driver's license</span></span>  <br/> <span data-ttu-id="65b10-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-364">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-365">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-366">driving license number</span></span>  <br/> <span data-ttu-id="65b10-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-367">dlno#</span></span>  <br/> <span data-ttu-id="65b10-368">Ajokortti</span><span class="sxs-lookup"><span data-stu-id="65b10-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="65b10-369">France</span><span class="sxs-lookup"><span data-stu-id="65b10-369">France</span></span>

<span data-ttu-id="65b10-370">Pour plus d'informations, reportez-vous à la section «numéro de permis de conduire France» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65b10-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="65b10-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="65b10-371">Germany</span></span>

<span data-ttu-id="65b10-372">Pour plus d'informations, consultez la section «numéro de permis de conduire allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65b10-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="65b10-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="65b10-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="65b10-374">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-374">Format</span></span>

<span data-ttu-id="65b10-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-376">Pattern</span></span>

 <span data-ttu-id="65b10-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65b10-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-378">Checksum</span></span>

<span data-ttu-id="65b10-379">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-380">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-380">Definition</span></span>

<span data-ttu-id="65b10-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-382">L'expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-384">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-384">Keywords</span></span>

<span data-ttu-id="65b10-385">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-385"></span></span>
|<span data-ttu-id="65b10-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-387">Fichier</span><span class="sxs-lookup"><span data-stu-id="65b10-387">dlL#</span></span>  <br/> <span data-ttu-id="65b10-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-388">driver license</span></span>  <br/> <span data-ttu-id="65b10-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-389">driver license number</span></span>  <br/> <span data-ttu-id="65b10-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-390">driver licence</span></span>  <br/> <span data-ttu-id="65b10-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-391">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-392">drivers license</span></span>  <br/> <span data-ttu-id="65b10-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-393">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-394">driver's license</span></span>  <br/> <span data-ttu-id="65b10-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-395">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-396">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-397">driving license number</span></span>  <br/> <span data-ttu-id="65b10-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-398">dlno#</span></span>  <br/> <span data-ttu-id="65b10-399">δεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="65b10-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="65b10-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="65b10-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="65b10-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="65b10-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="65b10-402">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-402">Format</span></span>

<span data-ttu-id="65b10-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-404">Pattern</span></span>

<span data-ttu-id="65b10-405">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="65b10-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="65b10-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-408">Checksum</span></span>

<span data-ttu-id="65b10-409">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-410">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-410">Definition</span></span>

<span data-ttu-id="65b10-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-412">L'expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-414">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-414">Keywords</span></span>

<span data-ttu-id="65b10-415">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-415"></span></span>
|<span data-ttu-id="65b10-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-417">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-417">dl#</span></span>  <br/> <span data-ttu-id="65b10-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-418">driver license</span></span>  <br/> <span data-ttu-id="65b10-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-419">driver license number</span></span>  <br/> <span data-ttu-id="65b10-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-420">driver licence</span></span>  <br/> <span data-ttu-id="65b10-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-421">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-422">drivers license</span></span>  <br/> <span data-ttu-id="65b10-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-423">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-424">driver's license</span></span>  <br/> <span data-ttu-id="65b10-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-425">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-426">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-427">driving license number</span></span>  <br/> <span data-ttu-id="65b10-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-428">dlno#</span></span>  <br/> <span data-ttu-id="65b10-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="65b10-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="65b10-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="65b10-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="65b10-431">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-431">Format</span></span>

<span data-ttu-id="65b10-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="65b10-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-433">Pattern</span></span>

<span data-ttu-id="65b10-434">Six chiffres et quatre lettres:</span><span class="sxs-lookup"><span data-stu-id="65b10-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="65b10-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-435">Six digits</span></span>
    
- <span data-ttu-id="65b10-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-437">Checksum</span></span>

<span data-ttu-id="65b10-438">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-439">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-439">Definition</span></span>

<span data-ttu-id="65b10-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-441">L'expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-443">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-443">Keywords</span></span>

<span data-ttu-id="65b10-444">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-444"></span></span>
|<span data-ttu-id="65b10-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-446">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-446">dl#</span></span>  <br/> <span data-ttu-id="65b10-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-447">driver license</span></span>  <br/> <span data-ttu-id="65b10-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-448">driver license number</span></span>  <br/> <span data-ttu-id="65b10-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-449">driver licence</span></span>  <br/> <span data-ttu-id="65b10-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-450">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-451">drivers license</span></span>  <br/> <span data-ttu-id="65b10-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-452">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-453">driver's license</span></span>  <br/> <span data-ttu-id="65b10-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-454">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-455">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-456">driving license number</span></span>  <br/> <span data-ttu-id="65b10-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-457">dlno#</span></span>  <br/> <span data-ttu-id="65b10-458">Ceadúnas Tiomána</span><span class="sxs-lookup"><span data-stu-id="65b10-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="65b10-459">Italie</span><span class="sxs-lookup"><span data-stu-id="65b10-459">Italy</span></span>

<span data-ttu-id="65b10-460">Pour plus d'informations, reportez-vous à la section «Italie numéro de permis de conduire» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65b10-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="65b10-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="65b10-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="65b10-462">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-462">Format</span></span>

<span data-ttu-id="65b10-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-464">Pattern</span></span>

<span data-ttu-id="65b10-465">Trois lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="65b10-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="65b10-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-468">Checksum</span></span>

<span data-ttu-id="65b10-469">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-470">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-470">Definition</span></span>

<span data-ttu-id="65b10-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-472">L'expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-474">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-474">Keywords</span></span>

<span data-ttu-id="65b10-475">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-475"></span></span>
|<span data-ttu-id="65b10-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-477">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-477">dl#</span></span>  <br/> <span data-ttu-id="65b10-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-478">driver license</span></span>  <br/> <span data-ttu-id="65b10-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-479">driver license number</span></span>  <br/> <span data-ttu-id="65b10-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-480">driver licence</span></span>  <br/> <span data-ttu-id="65b10-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-481">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-482">drivers license</span></span>  <br/> <span data-ttu-id="65b10-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-483">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-484">driver's license</span></span>  <br/> <span data-ttu-id="65b10-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-485">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-486">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-487">driving license number</span></span>  <br/> <span data-ttu-id="65b10-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-488">dlno#</span></span>  <br/> <span data-ttu-id="65b10-489">autovadītāja APLIECĪBA</span><span class="sxs-lookup"><span data-stu-id="65b10-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="65b10-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="65b10-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="65b10-491">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-491">Format</span></span>

<span data-ttu-id="65b10-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-493">Pattern</span></span>

 <span data-ttu-id="65b10-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65b10-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-495">Checksum</span></span>

<span data-ttu-id="65b10-496">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-497">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-497">Definition</span></span>

<span data-ttu-id="65b10-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-499">L'expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-501">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-501">Keywords</span></span>

<span data-ttu-id="65b10-502">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-502"></span></span>
|<span data-ttu-id="65b10-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-504">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-504">dl#</span></span>  <br/> <span data-ttu-id="65b10-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-505">driver license</span></span>  <br/> <span data-ttu-id="65b10-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-506">driver license number</span></span>  <br/> <span data-ttu-id="65b10-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-507">driver licence</span></span>  <br/> <span data-ttu-id="65b10-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-508">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-509">drivers license</span></span>  <br/> <span data-ttu-id="65b10-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-510">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-511">driver's license</span></span>  <br/> <span data-ttu-id="65b10-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-512">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-513">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-514">driving license number</span></span>  <br/> <span data-ttu-id="65b10-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-515">dlno#</span></span>  <br/> <span data-ttu-id="65b10-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="65b10-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="65b10-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="65b10-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="65b10-518">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-518">Format</span></span>

<span data-ttu-id="65b10-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-520">Pattern</span></span>

 <span data-ttu-id="65b10-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="65b10-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-522">Checksum</span></span>

<span data-ttu-id="65b10-523">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-524">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-524">Definition</span></span>

<span data-ttu-id="65b10-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-526">L'expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-528">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-528">Keywords</span></span>

<span data-ttu-id="65b10-529">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-529"></span></span>
|<span data-ttu-id="65b10-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-531">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-531">dl#</span></span>  <br/> <span data-ttu-id="65b10-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-532">driver license</span></span>  <br/> <span data-ttu-id="65b10-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-533">driver license number</span></span>  <br/> <span data-ttu-id="65b10-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-534">driver licence</span></span>  <br/> <span data-ttu-id="65b10-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-535">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-536">drivers license</span></span>  <br/> <span data-ttu-id="65b10-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-537">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-538">driver's license</span></span>  <br/> <span data-ttu-id="65b10-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-539">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-540">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-541">driving license number</span></span>  <br/> <span data-ttu-id="65b10-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-542">dlno#</span></span>  <br/> <span data-ttu-id="65b10-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="65b10-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="65b10-544">Malte</span><span class="sxs-lookup"><span data-stu-id="65b10-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="65b10-545">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-545">Format</span></span>

<span data-ttu-id="65b10-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="65b10-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-547">Pattern</span></span>

<span data-ttu-id="65b10-548">Combinaison de deux caractères et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="65b10-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="65b10-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="65b10-550">A space (optional)</span></span>
    
- <span data-ttu-id="65b10-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-551">Three digits</span></span>
    
- <span data-ttu-id="65b10-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="65b10-552">A space (optional)</span></span>
    
- <span data-ttu-id="65b10-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-554">Checksum</span></span>

<span data-ttu-id="65b10-555">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-556">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-556">Definition</span></span>

<span data-ttu-id="65b10-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-558">L'expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-560">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-560">Keywords</span></span>

<span data-ttu-id="65b10-561">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-561"></span></span>
|<span data-ttu-id="65b10-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-563">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-563">dl#</span></span>  <br/> <span data-ttu-id="65b10-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-564">driver license</span></span>  <br/> <span data-ttu-id="65b10-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-565">driver license number</span></span>  <br/> <span data-ttu-id="65b10-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-566">driver licence</span></span>  <br/> <span data-ttu-id="65b10-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-567">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-568">drivers license</span></span>  <br/> <span data-ttu-id="65b10-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-569">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-570">driver's license</span></span>  <br/> <span data-ttu-id="65b10-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-571">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-572">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-573">driving license number</span></span>  <br/> <span data-ttu-id="65b10-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-574">dlno#</span></span>  <br/> <span data-ttu-id="65b10-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="65b10-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="65b10-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="65b10-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="65b10-577">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-577">Format</span></span>

<span data-ttu-id="65b10-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-579">Pattern</span></span>

<span data-ttu-id="65b10-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-581">Checksum</span></span>

<span data-ttu-id="65b10-582">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-583">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-583">Definition</span></span>

<span data-ttu-id="65b10-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-585">L'expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-587">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-587">Keywords</span></span>

<span data-ttu-id="65b10-588">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-588"></span></span>
|<span data-ttu-id="65b10-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-590">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-590">dl#</span></span>  <br/> <span data-ttu-id="65b10-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-591">driver license</span></span>  <br/> <span data-ttu-id="65b10-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-592">driver license number</span></span>  <br/> <span data-ttu-id="65b10-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-593">driver licence</span></span>  <br/> <span data-ttu-id="65b10-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-594">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-595">drivers license</span></span>  <br/> <span data-ttu-id="65b10-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-596">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-597">driver's license</span></span>  <br/> <span data-ttu-id="65b10-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-598">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-599">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-600">driving license number</span></span>  <br/> <span data-ttu-id="65b10-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-601">dlno#</span></span>  <br/> <span data-ttu-id="65b10-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-602">permis de conduire</span></span>  <br/> <span data-ttu-id="65b10-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="65b10-603">rijbewijs</span></span>  <br/> <span data-ttu-id="65b10-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="65b10-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="65b10-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="65b10-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="65b10-606">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-606">Format</span></span>

<span data-ttu-id="65b10-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="65b10-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-608">Pattern</span></span>

<span data-ttu-id="65b10-609">14 chiffres et 2 barres obliques:</span><span class="sxs-lookup"><span data-stu-id="65b10-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="65b10-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-610">Five digits</span></span> 
    
- <span data-ttu-id="65b10-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="65b10-611">A forward slash</span></span>
    
- <span data-ttu-id="65b10-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-612">Two digits</span></span>
    
- <span data-ttu-id="65b10-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="65b10-613">A forward slash</span></span>
    
- <span data-ttu-id="65b10-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-615">Checksum</span></span>

<span data-ttu-id="65b10-616">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-617">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-617">Definition</span></span>

<span data-ttu-id="65b10-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-619">L'expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-621">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-621">Keywords</span></span>

<span data-ttu-id="65b10-622">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-622"></span></span>
|<span data-ttu-id="65b10-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-624">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-624">dl#</span></span>  <br/> <span data-ttu-id="65b10-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-625">driver license</span></span>  <br/> <span data-ttu-id="65b10-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-626">driver license number</span></span>  <br/> <span data-ttu-id="65b10-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-627">driver licence</span></span>  <br/> <span data-ttu-id="65b10-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-628">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-629">drivers license</span></span>  <br/> <span data-ttu-id="65b10-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-630">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-631">driver's license</span></span>  <br/> <span data-ttu-id="65b10-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-632">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-633">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-634">driving license number</span></span>  <br/> <span data-ttu-id="65b10-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-635">dlno#</span></span>  <br/> <span data-ttu-id="65b10-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="65b10-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="65b10-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="65b10-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="65b10-638">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-638">Format</span></span>

<span data-ttu-id="65b10-639">Deux lettres suivies d'un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="65b10-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-640">Pattern</span></span>

<span data-ttu-id="65b10-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux:</span><span class="sxs-lookup"><span data-stu-id="65b10-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="65b10-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="65b10-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="65b10-643">A hyphen</span></span>
    
- <span data-ttu-id="65b10-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-644">Six digits</span></span>
    
- <span data-ttu-id="65b10-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="65b10-645">A space</span></span>
    
- <span data-ttu-id="65b10-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="65b10-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-647">Checksum</span></span>

<span data-ttu-id="65b10-648">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-649">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-649">Definition</span></span>

<span data-ttu-id="65b10-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-651">L'expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-653">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-653">Keywords</span></span>

<span data-ttu-id="65b10-654">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-654"></span></span>
|<span data-ttu-id="65b10-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-656">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-656">dl#</span></span>  <br/> <span data-ttu-id="65b10-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-657">driver license</span></span>  <br/> <span data-ttu-id="65b10-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-658">driver license number</span></span>  <br/> <span data-ttu-id="65b10-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-659">driver licence</span></span>  <br/> <span data-ttu-id="65b10-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-660">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-661">drivers license</span></span>  <br/> <span data-ttu-id="65b10-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-662">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-663">driver's license</span></span>  <br/> <span data-ttu-id="65b10-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-664">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-665">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-666">driving license number</span></span>  <br/> <span data-ttu-id="65b10-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-667">dlno#</span></span>  <br/> <span data-ttu-id="65b10-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="65b10-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="65b10-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="65b10-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="65b10-670">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-670">Format</span></span>

<span data-ttu-id="65b10-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-672">Pattern</span></span>

<span data-ttu-id="65b10-673">Un caractère suivi de huit chiffres:</span><span class="sxs-lookup"><span data-stu-id="65b10-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="65b10-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="65b10-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="65b10-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-676">Checksum</span></span>

<span data-ttu-id="65b10-677">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-678">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-678">Definition</span></span>

<span data-ttu-id="65b10-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-680">L'expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-682">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-682">Keywords</span></span>

<span data-ttu-id="65b10-683">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-683"></span></span>
|<span data-ttu-id="65b10-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-685">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-685">dl#</span></span>  <br/> <span data-ttu-id="65b10-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-686">driver license</span></span>  <br/> <span data-ttu-id="65b10-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-687">driver license number</span></span>  <br/> <span data-ttu-id="65b10-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-688">driver licence</span></span>  <br/> <span data-ttu-id="65b10-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-689">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-690">drivers license</span></span>  <br/> <span data-ttu-id="65b10-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-691">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-692">driver's license</span></span>  <br/> <span data-ttu-id="65b10-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-693">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-694">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-695">driving license number</span></span>  <br/> <span data-ttu-id="65b10-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-696">dlno#</span></span>  <br/> <span data-ttu-id="65b10-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="65b10-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="65b10-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="65b10-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="65b10-699">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-699">Format</span></span>

<span data-ttu-id="65b10-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-701">Pattern</span></span>

<span data-ttu-id="65b10-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="65b10-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="65b10-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="65b10-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="65b10-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-705">Checksum</span></span>

<span data-ttu-id="65b10-706">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-707">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-707">Definition</span></span>

<span data-ttu-id="65b10-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-709">L'expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-711">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-711">Keywords</span></span>

<span data-ttu-id="65b10-712">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-712"></span></span>
|<span data-ttu-id="65b10-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-714">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-714">dl#</span></span>  <br/> <span data-ttu-id="65b10-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-715">driver license</span></span>  <br/> <span data-ttu-id="65b10-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-716">driver license number</span></span>  <br/> <span data-ttu-id="65b10-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-717">driver licence</span></span>  <br/> <span data-ttu-id="65b10-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-718">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-719">drivers license</span></span>  <br/> <span data-ttu-id="65b10-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-720">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-721">driver's license</span></span>  <br/> <span data-ttu-id="65b10-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-722">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-723">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-724">driving license number</span></span>  <br/> <span data-ttu-id="65b10-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-725">dlno#</span></span>  <br/> <span data-ttu-id="65b10-726">vodičský PREUKAZ</span><span class="sxs-lookup"><span data-stu-id="65b10-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="65b10-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="65b10-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="65b10-728">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-728">Format</span></span>

<span data-ttu-id="65b10-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="65b10-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-730">Pattern</span></span>

<span data-ttu-id="65b10-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="65b10-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-732">Checksum</span></span>

<span data-ttu-id="65b10-733">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-734">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-734">Definition</span></span>

<span data-ttu-id="65b10-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-736">L'expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-738">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-738">Keywords</span></span>

<span data-ttu-id="65b10-739">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-739"></span></span>
|<span data-ttu-id="65b10-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-741">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-741">dl#</span></span>  <br/> <span data-ttu-id="65b10-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-742">driver license</span></span>  <br/> <span data-ttu-id="65b10-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-743">driver license number</span></span>  <br/> <span data-ttu-id="65b10-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-744">driver licence</span></span>  <br/> <span data-ttu-id="65b10-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-745">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-746">drivers license</span></span>  <br/> <span data-ttu-id="65b10-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-747">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-748">driver's license</span></span>  <br/> <span data-ttu-id="65b10-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-749">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-750">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-751">driving license number</span></span>  <br/> <span data-ttu-id="65b10-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-752">dlno#</span></span>  <br/> <span data-ttu-id="65b10-753">vozniško Dovoljenje</span><span class="sxs-lookup"><span data-stu-id="65b10-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="65b10-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="65b10-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="65b10-755">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-755">Format</span></span>

<span data-ttu-id="65b10-756">Huit chiffres suivis d'un caractère</span><span class="sxs-lookup"><span data-stu-id="65b10-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-757">Pattern</span></span>

<span data-ttu-id="65b10-758">Huit chiffres suivis d'un caractère:</span><span class="sxs-lookup"><span data-stu-id="65b10-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="65b10-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-759">Eight digits</span></span> 
    
- <span data-ttu-id="65b10-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="65b10-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-761">Checksum</span></span>

<span data-ttu-id="65b10-762">Oui</span><span class="sxs-lookup"><span data-stu-id="65b10-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-763">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-763">Definition</span></span>

<span data-ttu-id="65b10-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="65b10-767">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-767">Keywords</span></span>

<span data-ttu-id="65b10-768">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-768"></span></span>
|<span data-ttu-id="65b10-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-770">dlno#</span></span>  <br/> <span data-ttu-id="65b10-771">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-771">dl#</span></span>  <br/> <span data-ttu-id="65b10-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-772">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-773">driver licence</span></span>  <br/> <span data-ttu-id="65b10-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-774">driver license</span></span>  <br/> <span data-ttu-id="65b10-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-775">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-776">drivers license</span></span>  <br/> <span data-ttu-id="65b10-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-777">driver's licence</span></span>  <br/> <span data-ttu-id="65b10-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-778">driver's license</span></span>  <br/> <span data-ttu-id="65b10-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-779">driving licence</span></span>  <br/> <span data-ttu-id="65b10-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-780">driving license</span></span>  <br/> <span data-ttu-id="65b10-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-781">driver licence number</span></span>  <br/> <span data-ttu-id="65b10-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-782">driver license number</span></span>  <br/> <span data-ttu-id="65b10-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-783">drivers licence number</span></span>  <br/> <span data-ttu-id="65b10-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-784">drivers license number</span></span>  <br/> <span data-ttu-id="65b10-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-785">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-786">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-787">driving licence number</span></span>  <br/> <span data-ttu-id="65b10-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-788">driving license number</span></span>  <br/> <span data-ttu-id="65b10-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-789">driving permit</span></span>  <br/> <span data-ttu-id="65b10-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-790">driving permit number</span></span>  <br/> <span data-ttu-id="65b10-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="65b10-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="65b10-792">permiso Conducción</span><span class="sxs-lookup"><span data-stu-id="65b10-792">permiso conducción</span></span>  <br/> <span data-ttu-id="65b10-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="65b10-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="65b10-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="65b10-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="65b10-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-796">licencia conducir</span></span>  <br/> <span data-ttu-id="65b10-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="65b10-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="65b10-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="65b10-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-800">permiso conducir</span></span>  <br/> <span data-ttu-id="65b10-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="65b10-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="65b10-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="65b10-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="65b10-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="65b10-804">Suède</span><span class="sxs-lookup"><span data-stu-id="65b10-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="65b10-805">Format</span><span class="sxs-lookup"><span data-stu-id="65b10-805">Format</span></span>

<span data-ttu-id="65b10-806">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="65b10-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="65b10-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="65b10-807">Pattern</span></span>

<span data-ttu-id="65b10-808">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="65b10-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="65b10-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-809">Six digits</span></span> 
    
- <span data-ttu-id="65b10-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="65b10-810">A hyphen</span></span>
    
- <span data-ttu-id="65b10-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="65b10-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="65b10-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="65b10-812">Checksum</span></span>

<span data-ttu-id="65b10-813">Non</span><span class="sxs-lookup"><span data-stu-id="65b10-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="65b10-814">Définition</span><span class="sxs-lookup"><span data-stu-id="65b10-814">Definition</span></span>

<span data-ttu-id="65b10-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="65b10-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="65b10-816">L'expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="65b10-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="65b10-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="65b10-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="65b10-818">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="65b10-818">Keywords</span></span>

<span data-ttu-id="65b10-819">| |</span><span class="sxs-lookup"><span data-stu-id="65b10-819"></span></span>
|<span data-ttu-id="65b10-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="65b10-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="65b10-821">LD</span><span class="sxs-lookup"><span data-stu-id="65b10-821">dl#</span></span>  <br/> <span data-ttu-id="65b10-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-822">driver license</span></span>  <br/> <span data-ttu-id="65b10-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-823">driver license number</span></span>  <br/> <span data-ttu-id="65b10-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-824">driver licence</span></span>  <br/> <span data-ttu-id="65b10-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="65b10-825">drivers lic.</span></span>  <br/> <span data-ttu-id="65b10-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-826">drivers license</span></span>  <br/> <span data-ttu-id="65b10-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-827">drivers licence</span></span>  <br/> <span data-ttu-id="65b10-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-828">driver's license</span></span>  <br/> <span data-ttu-id="65b10-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-829">driver's license number</span></span>  <br/> <span data-ttu-id="65b10-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-830">driver's licence number</span></span>  <br/> <span data-ttu-id="65b10-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="65b10-831">driving license number</span></span>  <br/> <span data-ttu-id="65b10-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="65b10-832">dlno#</span></span>  <br/> <span data-ttu-id="65b10-833">körkort</span><span class="sxs-lookup"><span data-stu-id="65b10-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="65b10-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="65b10-834">UK</span></span>

<span data-ttu-id="65b10-835">Pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="65b10-835">For details, see the section "U.K.</span></span> <span data-ttu-id="65b10-836">Numéro de permis de conduire» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="65b10-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65b10-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65b10-837">See also</span></span>

[<span data-ttu-id="65b10-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="65b10-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

