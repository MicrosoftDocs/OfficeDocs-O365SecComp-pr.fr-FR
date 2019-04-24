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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255772"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="847f3-104">Numéro de permis de conduire de l'UE</span><span class="sxs-lookup"><span data-stu-id="847f3-104">EU Driver's License Number</span></span>

<span data-ttu-id="847f3-105">Cette rubrique présente ce qu'une stratégie de protection contre la perte de données (DLP) recherche lorsqu'elle détecte le type d'informations sensibles du pilote de l'UE.</span><span class="sxs-lookup"><span data-stu-id="847f3-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="847f3-106">Ce type d'informations sensibles définit différents modèles, Mots clés et autres preuves pour chaque pays.</span><span class="sxs-lookup"><span data-stu-id="847f3-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="847f3-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="847f3-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="847f3-108">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-108">Format</span></span>

<span data-ttu-id="847f3-109">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-110">Pattern</span></span>

<span data-ttu-id="847f3-111">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-112">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-112">Checksum</span></span>

<span data-ttu-id="847f3-113">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-114">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-114">Definition</span></span>

<span data-ttu-id="847f3-115">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-116">L'expression `Regex_austria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-117">Un mot clé `Keywords_austria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="847f3-118">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-118">Keywords</span></span>

<span data-ttu-id="847f3-119">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-119"></span></span>
|<span data-ttu-id="847f3-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-121">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-121">dl#</span></span>  <br/> <span data-ttu-id="847f3-122">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-122">driver license</span></span>  <br/> <span data-ttu-id="847f3-123">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-123">driver license number</span></span>  <br/> <span data-ttu-id="847f3-124">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-124">driver licence</span></span>  <br/> <span data-ttu-id="847f3-125">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-125">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-126">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-126">drivers license</span></span>  <br/> <span data-ttu-id="847f3-127">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-127">driver's licence</span></span>  <br/> <span data-ttu-id="847f3-128">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-128">driver's license</span></span>  <br/> <span data-ttu-id="847f3-129">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-129">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-130">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="847f3-131">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-131">driving license number</span></span>  <br/> <span data-ttu-id="847f3-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-132">dlno#</span></span>  <br/> <span data-ttu-id="847f3-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="847f3-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="847f3-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="847f3-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="847f3-135">Belgique</span><span class="sxs-lookup"><span data-stu-id="847f3-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="847f3-136">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-136">Format</span></span>

<span data-ttu-id="847f3-137">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-138">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-138">Pattern</span></span>

<span data-ttu-id="847f3-139">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-140">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-140">Checksum</span></span>

<span data-ttu-id="847f3-141">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-142">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-142">Definition</span></span>

<span data-ttu-id="847f3-143">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-144">L'expression `Regex_belgium_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-145">Un mot clé `Keywords_belgium_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="847f3-146">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-146">Keywords</span></span>

<span data-ttu-id="847f3-147">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-147"></span></span>
|<span data-ttu-id="847f3-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-149">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-149">dl#</span></span>  <br/> <span data-ttu-id="847f3-150">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-150">driver license</span></span>  <br/> <span data-ttu-id="847f3-151">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-151">driver license number</span></span>  <br/> <span data-ttu-id="847f3-152">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-152">driver licence</span></span>  <br/> <span data-ttu-id="847f3-153">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-153">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-154">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-154">drivers license</span></span>  <br/> <span data-ttu-id="847f3-155">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-155">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-156">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-156">driver's license</span></span>  <br/> <span data-ttu-id="847f3-157">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-157">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-158">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-158">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-159">dlno#</span></span>  <br/> <span data-ttu-id="847f3-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="847f3-160">rijbewijs</span></span>  <br/> <span data-ttu-id="847f3-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="847f3-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="847f3-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="847f3-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="847f3-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="847f3-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="847f3-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="847f3-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="847f3-167">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="847f3-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="847f3-168">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="847f3-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="847f3-169">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-169">Format</span></span>

<span data-ttu-id="847f3-170">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-171">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-171">Pattern</span></span>

<span data-ttu-id="847f3-172">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-173">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-173">Checksum</span></span>

<span data-ttu-id="847f3-174">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-175">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-175">Definition</span></span>

<span data-ttu-id="847f3-176">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-177">L'expression `Regex_bulgaria_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-178">Un mot clé `Keywords_bulgaria_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="847f3-179">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-179">Keywords</span></span>

<span data-ttu-id="847f3-180">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-180"></span></span>
|<span data-ttu-id="847f3-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-182">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-182">dl#</span></span>  <br/> <span data-ttu-id="847f3-183">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-183">driver license</span></span>  <br/> <span data-ttu-id="847f3-184">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-184">driver license number</span></span>  <br/> <span data-ttu-id="847f3-185">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-185">driver licence</span></span>  <br/> <span data-ttu-id="847f3-186">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-186">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-187">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-187">drivers license</span></span>  <br/> <span data-ttu-id="847f3-188">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-188">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-189">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-189">driver's license</span></span>  <br/> <span data-ttu-id="847f3-190">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-190">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-191">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-191">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-192">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-192">driving license number</span></span>  <br/> <span data-ttu-id="847f3-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-193">dlno#</span></span>  <br/> <span data-ttu-id="847f3-194">свидетелство за Управление на мпс</span><span class="sxs-lookup"><span data-stu-id="847f3-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="847f3-195">свидетелство за Управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="847f3-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="847f3-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="847f3-196">сумпс</span></span>  <br/> <span data-ttu-id="847f3-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="847f3-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="847f3-198">Croatie</span><span class="sxs-lookup"><span data-stu-id="847f3-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="847f3-199">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-199">Format</span></span>

<span data-ttu-id="847f3-200">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-201">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-201">Pattern</span></span>

<span data-ttu-id="847f3-202">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-203">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-203">Checksum</span></span>

<span data-ttu-id="847f3-204">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-205">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-205">Definition</span></span>

<span data-ttu-id="847f3-206">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-207">L'expression `Regex_croatia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-208">Un mot clé `Keywords_croatia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="847f3-209">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-209">Keywords</span></span>

<span data-ttu-id="847f3-210">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-210"></span></span>
|<span data-ttu-id="847f3-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-212">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-212">dl#</span></span>  <br/> <span data-ttu-id="847f3-213">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-213">driver license</span></span>  <br/> <span data-ttu-id="847f3-214">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-214">driver license number</span></span>  <br/> <span data-ttu-id="847f3-215">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-215">driver licence</span></span>  <br/> <span data-ttu-id="847f3-216">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-216">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-217">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-217">drivers license</span></span>  <br/> <span data-ttu-id="847f3-218">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-218">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-219">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-219">driver's license</span></span>  <br/> <span data-ttu-id="847f3-220">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-220">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-221">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-221">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-222">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-222">driving license number</span></span>  <br/> <span data-ttu-id="847f3-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-223">dlno#</span></span>  <br/> <span data-ttu-id="847f3-224">vozačka Dozvola</span><span class="sxs-lookup"><span data-stu-id="847f3-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="847f3-225">Chypre</span><span class="sxs-lookup"><span data-stu-id="847f3-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="847f3-226">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-226">Format</span></span>

<span data-ttu-id="847f3-227">12 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-228">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-228">Pattern</span></span>

<span data-ttu-id="847f3-229">12 chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-230">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-230">Checksum</span></span>

<span data-ttu-id="847f3-231">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-232">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-232">Definition</span></span>

<span data-ttu-id="847f3-233">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-234">L'expression `Regex_cyprus_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-235">Un mot clé `Keywords_cyprus_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-236">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-236">Keywords</span></span>

<span data-ttu-id="847f3-237">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-237"></span></span>
|<span data-ttu-id="847f3-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-239">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-239">dl#</span></span>  <br/> <span data-ttu-id="847f3-240">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-240">driver license</span></span>  <br/> <span data-ttu-id="847f3-241">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-241">driver license number</span></span>  <br/> <span data-ttu-id="847f3-242">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-242">driver licence</span></span>  <br/> <span data-ttu-id="847f3-243">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-243">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-244">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-244">drivers license</span></span>  <br/> <span data-ttu-id="847f3-245">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-245">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-246">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-246">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-247">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-247">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-248">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-248">driving license number</span></span>  <br/> <span data-ttu-id="847f3-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-249">dlno#</span></span>  <br/> <span data-ttu-id="847f3-250">Άδεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="847f3-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="847f3-251">République tchèque</span><span class="sxs-lookup"><span data-stu-id="847f3-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="847f3-252">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-252">Format</span></span>

<span data-ttu-id="847f3-253">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-254">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-254">Pattern</span></span>

<span data-ttu-id="847f3-255">Huit lettres et chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="847f3-256">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="847f3-257">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="847f3-257">A space (optional)</span></span>
    
- <span data-ttu-id="847f3-258">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-259">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-259">Checksum</span></span>

<span data-ttu-id="847f3-260">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-261">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-261">Definition</span></span>

<span data-ttu-id="847f3-262">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-263">L'expression `Regex_czech_republic_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-264">Un mot clé `Keywords_czech_republic_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="847f3-265">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-265">Keywords</span></span>

<span data-ttu-id="847f3-266">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-266"></span></span>
|<span data-ttu-id="847f3-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-268">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-268">dl#</span></span>  <br/> <span data-ttu-id="847f3-269">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-269">driver license</span></span>  <br/> <span data-ttu-id="847f3-270">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-270">driver license number</span></span>  <br/> <span data-ttu-id="847f3-271">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-271">driver licence</span></span>  <br/> <span data-ttu-id="847f3-272">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-272">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-273">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-273">drivers license</span></span>  <br/> <span data-ttu-id="847f3-274">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-274">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-275">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-275">driver's license</span></span>  <br/> <span data-ttu-id="847f3-276">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-276">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-277">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-277">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-278">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-278">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-279">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-279">driving license number</span></span>  <br/> <span data-ttu-id="847f3-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-280">dlno#</span></span>  <br/> <span data-ttu-id="847f3-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="847f3-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="847f3-282">Danemark</span><span class="sxs-lookup"><span data-stu-id="847f3-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="847f3-283">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-283">Format</span></span>

<span data-ttu-id="847f3-284">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-285">Pattern</span></span>

<span data-ttu-id="847f3-286">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-287">Checksum</span></span>

<span data-ttu-id="847f3-288">Oui</span><span class="sxs-lookup"><span data-stu-id="847f3-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-289">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-289">Definition</span></span>

<span data-ttu-id="847f3-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-291">L'expression `Regex_denmark_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-292">Un mot clé `Keywords_denmark_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="847f3-293">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-293">Keywords</span></span>

<span data-ttu-id="847f3-294">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-294"></span></span>
|<span data-ttu-id="847f3-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-296">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-296">dl#</span></span>  <br/> <span data-ttu-id="847f3-297">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-297">driver license</span></span>  <br/> <span data-ttu-id="847f3-298">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-298">driver license number</span></span>  <br/> <span data-ttu-id="847f3-299">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-299">driver licence</span></span>  <br/> <span data-ttu-id="847f3-300">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-300">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-301">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-301">drivers license</span></span>  <br/> <span data-ttu-id="847f3-302">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-302">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-303">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-303">driver's license</span></span>  <br/> <span data-ttu-id="847f3-304">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-304">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-305">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-305">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-306">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-306">driving license number</span></span>  <br/> <span data-ttu-id="847f3-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-307">dlno#</span></span>  <br/> <span data-ttu-id="847f3-308">Kørekort</span><span class="sxs-lookup"><span data-stu-id="847f3-308">kørekort</span></span>  <br/> <span data-ttu-id="847f3-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="847f3-310">Estonie</span><span class="sxs-lookup"><span data-stu-id="847f3-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="847f3-311">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-311">Format</span></span>

<span data-ttu-id="847f3-312">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-313">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-313">Pattern</span></span>

<span data-ttu-id="847f3-314">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="847f3-315">Les lettres "ET" (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="847f3-316">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-317">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-317">Checksum</span></span>

<span data-ttu-id="847f3-318">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-319">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-319">Definition</span></span>

<span data-ttu-id="847f3-320">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-321">L'expression `Regex_estonia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-322">Un mot clé `Keywords_estonia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-323">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-323">Keywords</span></span>

<span data-ttu-id="847f3-324">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-324"></span></span>
|<span data-ttu-id="847f3-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-326">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-326">dl#</span></span>  <br/> <span data-ttu-id="847f3-327">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-327">driver license</span></span>  <br/> <span data-ttu-id="847f3-328">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-328">driver license number</span></span>  <br/> <span data-ttu-id="847f3-329">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-329">driver license number</span></span>  <br/> <span data-ttu-id="847f3-330">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-330">driver licence</span></span>  <br/> <span data-ttu-id="847f3-331">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-331">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-332">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-332">drivers license</span></span>  <br/> <span data-ttu-id="847f3-333">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-333">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-334">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-334">driver's license</span></span>  <br/> <span data-ttu-id="847f3-335">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-335">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-336">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-336">driving license number</span></span>  <br/> <span data-ttu-id="847f3-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-337">dlno#</span></span>  <br/> <span data-ttu-id="847f3-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="847f3-339">Finlande</span><span class="sxs-lookup"><span data-stu-id="847f3-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="847f3-340">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-340">Format</span></span>

<span data-ttu-id="847f3-341">10 chiffres contenant un trait d’union</span><span class="sxs-lookup"><span data-stu-id="847f3-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-342">Pattern</span></span>

<span data-ttu-id="847f3-343">10 chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="847f3-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="847f3-344">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-344">Six digits</span></span> 
    
- <span data-ttu-id="847f3-345">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="847f3-345">A hyphen</span></span>
    
-  <span data-ttu-id="847f3-346">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="847f3-347">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-347">Checksum</span></span>

<span data-ttu-id="847f3-348">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-349">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-349">Definition</span></span>

<span data-ttu-id="847f3-350">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-351">L'expression `Regex_finland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-352">Un mot clé `Keywords_finland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-353">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-353">Keywords</span></span>

<span data-ttu-id="847f3-354">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-354"></span></span>
|<span data-ttu-id="847f3-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-356">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-356">dl#</span></span>  <br/> <span data-ttu-id="847f3-357">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-357">driver license</span></span>  <br/> <span data-ttu-id="847f3-358">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-358">driver license number</span></span>  <br/> <span data-ttu-id="847f3-359">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-359">driver licence</span></span>  <br/> <span data-ttu-id="847f3-360">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-360">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-361">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-361">drivers license</span></span>  <br/> <span data-ttu-id="847f3-362">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-362">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-363">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-363">driver's license</span></span>  <br/> <span data-ttu-id="847f3-364">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-364">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-365">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-365">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-366">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-366">driving license number</span></span>  <br/> <span data-ttu-id="847f3-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-367">dlno#</span></span>  <br/> <span data-ttu-id="847f3-368">Ajokortti</span><span class="sxs-lookup"><span data-stu-id="847f3-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="847f3-369">France</span><span class="sxs-lookup"><span data-stu-id="847f3-369">France</span></span>

<span data-ttu-id="847f3-370">Pour plus d'informations, reportez-vous à la section «numéro de permis de conduire France» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="847f3-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="847f3-371">Allemagne</span><span class="sxs-lookup"><span data-stu-id="847f3-371">Germany</span></span>

<span data-ttu-id="847f3-372">Pour plus d'informations, consultez la section «numéro de permis de conduire allemand» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="847f3-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="847f3-373">Grèce</span><span class="sxs-lookup"><span data-stu-id="847f3-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="847f3-374">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-374">Format</span></span>

<span data-ttu-id="847f3-375">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-376">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-376">Pattern</span></span>

 <span data-ttu-id="847f3-377">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="847f3-378">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-378">Checksum</span></span>

<span data-ttu-id="847f3-379">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-380">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-380">Definition</span></span>

<span data-ttu-id="847f3-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-382">L'expression `Regex_greece_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-383">Un mot clé `Keywords_greece_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-384">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-384">Keywords</span></span>

<span data-ttu-id="847f3-385">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-385"></span></span>
|<span data-ttu-id="847f3-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-387">Fichier</span><span class="sxs-lookup"><span data-stu-id="847f3-387">dlL#</span></span>  <br/> <span data-ttu-id="847f3-388">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-388">driver license</span></span>  <br/> <span data-ttu-id="847f3-389">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-389">driver license number</span></span>  <br/> <span data-ttu-id="847f3-390">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-390">driver licence</span></span>  <br/> <span data-ttu-id="847f3-391">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-391">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-392">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-392">drivers license</span></span>  <br/> <span data-ttu-id="847f3-393">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-393">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-394">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-394">driver's license</span></span>  <br/> <span data-ttu-id="847f3-395">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-395">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-396">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-396">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-397">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-397">driving license number</span></span>  <br/> <span data-ttu-id="847f3-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-398">dlno#</span></span>  <br/> <span data-ttu-id="847f3-399">δεια Οδήγησης</span><span class="sxs-lookup"><span data-stu-id="847f3-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="847f3-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="847f3-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="847f3-401">Hongrie</span><span class="sxs-lookup"><span data-stu-id="847f3-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="847f3-402">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-402">Format</span></span>

<span data-ttu-id="847f3-403">Deux lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-404">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-404">Pattern</span></span>

<span data-ttu-id="847f3-405">Deux lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="847f3-406">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="847f3-407">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-408">Checksum</span></span>

<span data-ttu-id="847f3-409">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-410">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-410">Definition</span></span>

<span data-ttu-id="847f3-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-412">L'expression `Regex_hungary_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-413">Un mot clé `Keywords_hungary_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-414">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-414">Keywords</span></span>

<span data-ttu-id="847f3-415">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-415"></span></span>
|<span data-ttu-id="847f3-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-417">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-417">dl#</span></span>  <br/> <span data-ttu-id="847f3-418">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-418">driver license</span></span>  <br/> <span data-ttu-id="847f3-419">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-419">driver license number</span></span>  <br/> <span data-ttu-id="847f3-420">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-420">driver licence</span></span>  <br/> <span data-ttu-id="847f3-421">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-421">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-422">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-422">drivers license</span></span>  <br/> <span data-ttu-id="847f3-423">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-423">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-424">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-424">driver's license</span></span>  <br/> <span data-ttu-id="847f3-425">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-425">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-426">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-426">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-427">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-427">driving license number</span></span>  <br/> <span data-ttu-id="847f3-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-428">dlno#</span></span>  <br/> <span data-ttu-id="847f3-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="847f3-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="847f3-430">Irlande</span><span class="sxs-lookup"><span data-stu-id="847f3-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="847f3-431">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-431">Format</span></span>

<span data-ttu-id="847f3-432">Six chiffres suivis de quatre lettres</span><span class="sxs-lookup"><span data-stu-id="847f3-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-433">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-433">Pattern</span></span>

<span data-ttu-id="847f3-434">Six chiffres et quatre lettres:</span><span class="sxs-lookup"><span data-stu-id="847f3-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="847f3-435">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-435">Six digits</span></span>
    
- <span data-ttu-id="847f3-436">Quatre lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-437">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-437">Checksum</span></span>

<span data-ttu-id="847f3-438">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-439">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-439">Definition</span></span>

<span data-ttu-id="847f3-440">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-441">L'expression `Regex_ireland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-442">Un mot clé `Keywords_ireland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-443">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-443">Keywords</span></span>

<span data-ttu-id="847f3-444">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-444"></span></span>
|<span data-ttu-id="847f3-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-446">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-446">dl#</span></span>  <br/> <span data-ttu-id="847f3-447">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-447">driver license</span></span>  <br/> <span data-ttu-id="847f3-448">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-448">driver license number</span></span>  <br/> <span data-ttu-id="847f3-449">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-449">driver licence</span></span>  <br/> <span data-ttu-id="847f3-450">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-450">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-451">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-451">drivers license</span></span>  <br/> <span data-ttu-id="847f3-452">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-452">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-453">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-453">driver's license</span></span>  <br/> <span data-ttu-id="847f3-454">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-454">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-455">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-455">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-456">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-456">driving license number</span></span>  <br/> <span data-ttu-id="847f3-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-457">dlno#</span></span>  <br/> <span data-ttu-id="847f3-458">Ceadúnas Tiomána</span><span class="sxs-lookup"><span data-stu-id="847f3-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="847f3-459">Italie</span><span class="sxs-lookup"><span data-stu-id="847f3-459">Italy</span></span>

<span data-ttu-id="847f3-460">Pour plus d'informations, reportez-vous à la section «Italie numéro de permis de conduire» dans [la recherche des types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="847f3-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="847f3-461">Lettonie</span><span class="sxs-lookup"><span data-stu-id="847f3-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="847f3-462">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-462">Format</span></span>

<span data-ttu-id="847f3-463">Trois lettres suivies de six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-464">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-464">Pattern</span></span>

<span data-ttu-id="847f3-465">Trois lettres et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="847f3-466">Trois lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="847f3-467">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-468">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-468">Checksum</span></span>

<span data-ttu-id="847f3-469">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-470">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-470">Definition</span></span>

<span data-ttu-id="847f3-471">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-472">L'expression `Regex_latvia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-473">Un mot clé `Keywords_latvia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-474">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-474">Keywords</span></span>

<span data-ttu-id="847f3-475">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-475"></span></span>
|<span data-ttu-id="847f3-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-477">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-477">dl#</span></span>  <br/> <span data-ttu-id="847f3-478">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-478">driver license</span></span>  <br/> <span data-ttu-id="847f3-479">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-479">driver license number</span></span>  <br/> <span data-ttu-id="847f3-480">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-480">driver licence</span></span>  <br/> <span data-ttu-id="847f3-481">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-481">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-482">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-482">drivers license</span></span>  <br/> <span data-ttu-id="847f3-483">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-483">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-484">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-484">driver's license</span></span>  <br/> <span data-ttu-id="847f3-485">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-485">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-486">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-486">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-487">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-487">driving license number</span></span>  <br/> <span data-ttu-id="847f3-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-488">dlno#</span></span>  <br/> <span data-ttu-id="847f3-489">autovadītāja APLIECĪBA</span><span class="sxs-lookup"><span data-stu-id="847f3-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="847f3-490">Lituanie</span><span class="sxs-lookup"><span data-stu-id="847f3-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="847f3-491">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-491">Format</span></span>

<span data-ttu-id="847f3-492">Huit chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-493">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-493">Pattern</span></span>

 <span data-ttu-id="847f3-494">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="847f3-495">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-495">Checksum</span></span>

<span data-ttu-id="847f3-496">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-497">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-497">Definition</span></span>

<span data-ttu-id="847f3-498">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-499">L'expression `Regex_lithuania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-500">Un mot clé `Keywords_lithuania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-501">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-501">Keywords</span></span>

<span data-ttu-id="847f3-502">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-502"></span></span>
|<span data-ttu-id="847f3-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-504">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-504">dl#</span></span>  <br/> <span data-ttu-id="847f3-505">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-505">driver license</span></span>  <br/> <span data-ttu-id="847f3-506">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-506">driver license number</span></span>  <br/> <span data-ttu-id="847f3-507">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-507">driver licence</span></span>  <br/> <span data-ttu-id="847f3-508">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-508">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-509">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-509">drivers license</span></span>  <br/> <span data-ttu-id="847f3-510">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-510">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-511">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-511">driver's license</span></span>  <br/> <span data-ttu-id="847f3-512">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-512">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-513">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-513">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-514">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-514">driving license number</span></span>  <br/> <span data-ttu-id="847f3-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-515">dlno#</span></span>  <br/> <span data-ttu-id="847f3-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="847f3-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="847f3-517">Relatif</span><span class="sxs-lookup"><span data-stu-id="847f3-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="847f3-518">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-518">Format</span></span>

<span data-ttu-id="847f3-519">Six chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-520">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-520">Pattern</span></span>

 <span data-ttu-id="847f3-521">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="847f3-522">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-522">Checksum</span></span>

<span data-ttu-id="847f3-523">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-524">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-524">Definition</span></span>

<span data-ttu-id="847f3-525">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-526">L'expression `Regex_luxemburg_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-527">Un mot clé `Keywords_luxemburg_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-528">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-528">Keywords</span></span>

<span data-ttu-id="847f3-529">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-529"></span></span>
|<span data-ttu-id="847f3-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-531">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-531">dl#</span></span>  <br/> <span data-ttu-id="847f3-532">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-532">driver license</span></span>  <br/> <span data-ttu-id="847f3-533">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-533">driver license number</span></span>  <br/> <span data-ttu-id="847f3-534">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-534">driver licence</span></span>  <br/> <span data-ttu-id="847f3-535">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-535">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-536">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-536">drivers license</span></span>  <br/> <span data-ttu-id="847f3-537">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-537">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-538">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-538">driver's license</span></span>  <br/> <span data-ttu-id="847f3-539">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-539">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-540">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-540">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-541">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-541">driving license number</span></span>  <br/> <span data-ttu-id="847f3-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-542">dlno#</span></span>  <br/> <span data-ttu-id="847f3-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="847f3-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="847f3-544">Malte</span><span class="sxs-lookup"><span data-stu-id="847f3-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="847f3-545">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-545">Format</span></span>

<span data-ttu-id="847f3-546">Combinaison de deux caractères et six chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="847f3-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-547">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-547">Pattern</span></span>

<span data-ttu-id="847f3-548">Combinaison de deux caractères et six chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="847f3-549">Deux caractères (chiffres ou lettres, ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="847f3-550">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="847f3-550">A space (optional)</span></span>
    
- <span data-ttu-id="847f3-551">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-551">Three digits</span></span>
    
- <span data-ttu-id="847f3-552">Un espace (facultatif) </span><span class="sxs-lookup"><span data-stu-id="847f3-552">A space (optional)</span></span>
    
- <span data-ttu-id="847f3-553">Trois chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-554">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-554">Checksum</span></span>

<span data-ttu-id="847f3-555">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-556">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-556">Definition</span></span>

<span data-ttu-id="847f3-557">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-558">L'expression `Regex_malta_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-559">Un mot clé `Keywords_malta_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-560">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-560">Keywords</span></span>

<span data-ttu-id="847f3-561">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-561"></span></span>
|<span data-ttu-id="847f3-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-563">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-563">dl#</span></span>  <br/> <span data-ttu-id="847f3-564">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-564">driver license</span></span>  <br/> <span data-ttu-id="847f3-565">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-565">driver license number</span></span>  <br/> <span data-ttu-id="847f3-566">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-566">driver licence</span></span>  <br/> <span data-ttu-id="847f3-567">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-567">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-568">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-568">drivers license</span></span>  <br/> <span data-ttu-id="847f3-569">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-569">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-570">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-570">driver's license</span></span>  <br/> <span data-ttu-id="847f3-571">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-571">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-572">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-572">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-573">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-573">driving license number</span></span>  <br/> <span data-ttu-id="847f3-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-574">dlno#</span></span>  <br/> <span data-ttu-id="847f3-575">Liċenzja-sewqan</span><span class="sxs-lookup"><span data-stu-id="847f3-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="847f3-576">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="847f3-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="847f3-577">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-577">Format</span></span>

<span data-ttu-id="847f3-578">10 chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-579">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-579">Pattern</span></span>

<span data-ttu-id="847f3-580">10 chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-581">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-581">Checksum</span></span>

<span data-ttu-id="847f3-582">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-583">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-583">Definition</span></span>

<span data-ttu-id="847f3-584">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-585">L'expression `Regex_netherlands_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-586">Un mot clé `Keywords_netherlands_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-587">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-587">Keywords</span></span>

<span data-ttu-id="847f3-588">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-588"></span></span>
|<span data-ttu-id="847f3-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-590">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-590">dl#</span></span>  <br/> <span data-ttu-id="847f3-591">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-591">driver license</span></span>  <br/> <span data-ttu-id="847f3-592">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-592">driver license number</span></span>  <br/> <span data-ttu-id="847f3-593">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-593">driver licence</span></span>  <br/> <span data-ttu-id="847f3-594">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-594">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-595">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-595">drivers license</span></span>  <br/> <span data-ttu-id="847f3-596">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-596">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-597">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-597">driver's license</span></span>  <br/> <span data-ttu-id="847f3-598">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-598">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-599">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-599">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-600">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-600">driving license number</span></span>  <br/> <span data-ttu-id="847f3-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-601">dlno#</span></span>  <br/> <span data-ttu-id="847f3-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-602">permis de conduire</span></span>  <br/> <span data-ttu-id="847f3-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="847f3-603">rijbewijs</span></span>  <br/> <span data-ttu-id="847f3-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="847f3-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="847f3-605">Pologne</span><span class="sxs-lookup"><span data-stu-id="847f3-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="847f3-606">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-606">Format</span></span>

<span data-ttu-id="847f3-607">14 chiffres contenant 2 barres obliques</span><span class="sxs-lookup"><span data-stu-id="847f3-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-608">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-608">Pattern</span></span>

<span data-ttu-id="847f3-609">14 chiffres et 2 barres obliques:</span><span class="sxs-lookup"><span data-stu-id="847f3-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="847f3-610">Cinq chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-610">Five digits</span></span> 
    
- <span data-ttu-id="847f3-611">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="847f3-611">A forward slash</span></span>
    
- <span data-ttu-id="847f3-612">Deux chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-612">Two digits</span></span>
    
- <span data-ttu-id="847f3-613">Une barre oblique </span><span class="sxs-lookup"><span data-stu-id="847f3-613">A forward slash</span></span>
    
- <span data-ttu-id="847f3-614">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-615">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-615">Checksum</span></span>

<span data-ttu-id="847f3-616">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-617">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-617">Definition</span></span>

<span data-ttu-id="847f3-618">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-619">L'expression `Regex_poland_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-620">Un mot clé `Keywords_poland_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-621">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-621">Keywords</span></span>

<span data-ttu-id="847f3-622">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-622"></span></span>
|<span data-ttu-id="847f3-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-624">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-624">dl#</span></span>  <br/> <span data-ttu-id="847f3-625">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-625">driver license</span></span>  <br/> <span data-ttu-id="847f3-626">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-626">driver license number</span></span>  <br/> <span data-ttu-id="847f3-627">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-627">driver licence</span></span>  <br/> <span data-ttu-id="847f3-628">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-628">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-629">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-629">drivers license</span></span>  <br/> <span data-ttu-id="847f3-630">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-630">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-631">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-631">driver's license</span></span>  <br/> <span data-ttu-id="847f3-632">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-632">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-633">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-633">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-634">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-634">driving license number</span></span>  <br/> <span data-ttu-id="847f3-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-635">dlno#</span></span>  <br/> <span data-ttu-id="847f3-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="847f3-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="847f3-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="847f3-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="847f3-638">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-638">Format</span></span>

<span data-ttu-id="847f3-639">Deux lettres suivies d'un nombre de sept chiffres dans le modèle spécifié</span><span class="sxs-lookup"><span data-stu-id="847f3-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-640">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-640">Pattern</span></span>

<span data-ttu-id="847f3-641">Deux lettres suivies de sept chiffres avec des caractères spéciaux:</span><span class="sxs-lookup"><span data-stu-id="847f3-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="847f3-642">Deux lettres (ne respectent pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="847f3-643">Un trait d’union </span><span class="sxs-lookup"><span data-stu-id="847f3-643">A hyphen</span></span>
    
- <span data-ttu-id="847f3-644">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-644">Six digits</span></span>
    
- <span data-ttu-id="847f3-645">Un espace</span><span class="sxs-lookup"><span data-stu-id="847f3-645">A space</span></span>
    
- <span data-ttu-id="847f3-646">Un chiffre</span><span class="sxs-lookup"><span data-stu-id="847f3-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-647">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-647">Checksum</span></span>

<span data-ttu-id="847f3-648">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-649">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-649">Definition</span></span>

<span data-ttu-id="847f3-650">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-651">L'expression `Regex_portugal_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-652">Un mot clé `Keywords_portugal_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-653">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-653">Keywords</span></span>

<span data-ttu-id="847f3-654">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-654"></span></span>
|<span data-ttu-id="847f3-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-656">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-656">dl#</span></span>  <br/> <span data-ttu-id="847f3-657">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-657">driver license</span></span>  <br/> <span data-ttu-id="847f3-658">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-658">driver license number</span></span>  <br/> <span data-ttu-id="847f3-659">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-659">driver licence</span></span>  <br/> <span data-ttu-id="847f3-660">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-660">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-661">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-661">drivers license</span></span>  <br/> <span data-ttu-id="847f3-662">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-662">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-663">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-663">driver's license</span></span>  <br/> <span data-ttu-id="847f3-664">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-664">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-665">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-665">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-666">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-666">driving license number</span></span>  <br/> <span data-ttu-id="847f3-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-667">dlno#</span></span>  <br/> <span data-ttu-id="847f3-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="847f3-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="847f3-669">Roumanie</span><span class="sxs-lookup"><span data-stu-id="847f3-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="847f3-670">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-670">Format</span></span>

<span data-ttu-id="847f3-671">Un caractère suivi de huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-672">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-672">Pattern</span></span>

<span data-ttu-id="847f3-673">Un caractère suivi de huit chiffres:</span><span class="sxs-lookup"><span data-stu-id="847f3-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="847f3-674">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="847f3-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="847f3-675">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-676">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-676">Checksum</span></span>

<span data-ttu-id="847f3-677">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-678">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-678">Definition</span></span>

<span data-ttu-id="847f3-679">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-680">L'expression `Regex_romania_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-681">Un mot clé `Keywords_romania_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-682">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-682">Keywords</span></span>

<span data-ttu-id="847f3-683">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-683"></span></span>
|<span data-ttu-id="847f3-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-685">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-685">dl#</span></span>  <br/> <span data-ttu-id="847f3-686">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-686">driver license</span></span>  <br/> <span data-ttu-id="847f3-687">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-687">driver license number</span></span>  <br/> <span data-ttu-id="847f3-688">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-688">driver licence</span></span>  <br/> <span data-ttu-id="847f3-689">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-689">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-690">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-690">drivers license</span></span>  <br/> <span data-ttu-id="847f3-691">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-691">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-692">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-692">driver's license</span></span>  <br/> <span data-ttu-id="847f3-693">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-693">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-694">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-694">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-695">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-695">driving license number</span></span>  <br/> <span data-ttu-id="847f3-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-696">dlno#</span></span>  <br/> <span data-ttu-id="847f3-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="847f3-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="847f3-698">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="847f3-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="847f3-699">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-699">Format</span></span>

<span data-ttu-id="847f3-700">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-701">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-701">Pattern</span></span>

<span data-ttu-id="847f3-702">Un caractère suivi de sept chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="847f3-703">Une lettre (ne respecte pas la casse) ou un chiffre</span><span class="sxs-lookup"><span data-stu-id="847f3-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="847f3-704">Sept chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="847f3-705">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-705">Checksum</span></span>

<span data-ttu-id="847f3-706">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-707">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-707">Definition</span></span>

<span data-ttu-id="847f3-708">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-709">L'expression `Regex_slovakia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-710">Un mot clé `Keywords_slovakia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-711">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-711">Keywords</span></span>

<span data-ttu-id="847f3-712">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-712"></span></span>
|<span data-ttu-id="847f3-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-714">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-714">dl#</span></span>  <br/> <span data-ttu-id="847f3-715">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-715">driver license</span></span>  <br/> <span data-ttu-id="847f3-716">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-716">driver license number</span></span>  <br/> <span data-ttu-id="847f3-717">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-717">driver licence</span></span>  <br/> <span data-ttu-id="847f3-718">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-718">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-719">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-719">drivers license</span></span>  <br/> <span data-ttu-id="847f3-720">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-720">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-721">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-721">driver's license</span></span>  <br/> <span data-ttu-id="847f3-722">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-722">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-723">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-723">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-724">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-724">driving license number</span></span>  <br/> <span data-ttu-id="847f3-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-725">dlno#</span></span>  <br/> <span data-ttu-id="847f3-726">vodičský PREUKAZ</span><span class="sxs-lookup"><span data-stu-id="847f3-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="847f3-727">Slovénie</span><span class="sxs-lookup"><span data-stu-id="847f3-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="847f3-728">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-728">Format</span></span>

<span data-ttu-id="847f3-729">Neuf chiffres sans espaces ni délimiteurs</span><span class="sxs-lookup"><span data-stu-id="847f3-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-730">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-730">Pattern</span></span>

<span data-ttu-id="847f3-731">Neuf chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="847f3-732">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-732">Checksum</span></span>

<span data-ttu-id="847f3-733">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-734">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-734">Definition</span></span>

<span data-ttu-id="847f3-735">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-736">L'expression `Regex_slovenia_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-737">Un mot clé `Keywords_slovenia_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-738">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-738">Keywords</span></span>

<span data-ttu-id="847f3-739">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-739"></span></span>
|<span data-ttu-id="847f3-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-741">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-741">dl#</span></span>  <br/> <span data-ttu-id="847f3-742">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-742">driver license</span></span>  <br/> <span data-ttu-id="847f3-743">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-743">driver license number</span></span>  <br/> <span data-ttu-id="847f3-744">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-744">driver licence</span></span>  <br/> <span data-ttu-id="847f3-745">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-745">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-746">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-746">drivers license</span></span>  <br/> <span data-ttu-id="847f3-747">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-747">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-748">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-748">driver's license</span></span>  <br/> <span data-ttu-id="847f3-749">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-749">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-750">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-750">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-751">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-751">driving license number</span></span>  <br/> <span data-ttu-id="847f3-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-752">dlno#</span></span>  <br/> <span data-ttu-id="847f3-753">vozniško Dovoljenje</span><span class="sxs-lookup"><span data-stu-id="847f3-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="847f3-754">Espagne</span><span class="sxs-lookup"><span data-stu-id="847f3-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="847f3-755">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-755">Format</span></span>

<span data-ttu-id="847f3-756">Huit chiffres suivis d'un caractère</span><span class="sxs-lookup"><span data-stu-id="847f3-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-757">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-757">Pattern</span></span>

<span data-ttu-id="847f3-758">Huit chiffres suivis d'un caractère:</span><span class="sxs-lookup"><span data-stu-id="847f3-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="847f3-759">Huit chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-759">Eight digits</span></span> 
    
- <span data-ttu-id="847f3-760">Un chiffre ou une lettre (ne respectant pas la casse)</span><span class="sxs-lookup"><span data-stu-id="847f3-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-761">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-761">Checksum</span></span>

<span data-ttu-id="847f3-762">Oui</span><span class="sxs-lookup"><span data-stu-id="847f3-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-763">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-763">Definition</span></span>

<span data-ttu-id="847f3-764">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-765">La fonction `Func_spain_eu_driver's_license_number` trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-766">Un mot clé `Keywords_spain_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="847f3-767">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-767">Keywords</span></span>

<span data-ttu-id="847f3-768">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-768"></span></span>
|<span data-ttu-id="847f3-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-770">dlno#</span></span>  <br/> <span data-ttu-id="847f3-771">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-771">dl#</span></span>  <br/> <span data-ttu-id="847f3-772">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-772">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-773">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-773">driver licence</span></span>  <br/> <span data-ttu-id="847f3-774">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-774">driver license</span></span>  <br/> <span data-ttu-id="847f3-775">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-775">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-776">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-776">drivers license</span></span>  <br/> <span data-ttu-id="847f3-777">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-777">driver's licence</span></span>  <br/> <span data-ttu-id="847f3-778">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-778">driver's license</span></span>  <br/> <span data-ttu-id="847f3-779">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-779">driving licence</span></span>  <br/> <span data-ttu-id="847f3-780">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-780">driving license</span></span>  <br/> <span data-ttu-id="847f3-781">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-781">driver licence number</span></span>  <br/> <span data-ttu-id="847f3-782">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-782">driver license number</span></span>  <br/> <span data-ttu-id="847f3-783">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-783">drivers licence number</span></span>  <br/> <span data-ttu-id="847f3-784">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-784">drivers license number</span></span>  <br/> <span data-ttu-id="847f3-785">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-785">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-786">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-786">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-787">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-787">driving licence number</span></span>  <br/> <span data-ttu-id="847f3-788">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-788">driving license number</span></span>  <br/> <span data-ttu-id="847f3-789">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-789">driving permit</span></span>  <br/> <span data-ttu-id="847f3-790">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-790">driving permit number</span></span>  <br/> <span data-ttu-id="847f3-791">permiso de Conducción</span><span class="sxs-lookup"><span data-stu-id="847f3-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="847f3-792">permiso Conducción</span><span class="sxs-lookup"><span data-stu-id="847f3-792">permiso conducción</span></span>  <br/> <span data-ttu-id="847f3-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="847f3-794">Número de carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="847f3-795">conducir de carnet número</span><span class="sxs-lookup"><span data-stu-id="847f3-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="847f3-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-796">licencia conducir</span></span>  <br/> <span data-ttu-id="847f3-797">Número de permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="847f3-798">Número de permiso conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="847f3-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="847f3-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-800">permiso conducir</span></span>  <br/> <span data-ttu-id="847f3-801">licencia de manejo</span><span class="sxs-lookup"><span data-stu-id="847f3-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="847f3-802">carnet El de conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="847f3-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="847f3-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="847f3-804">Suède</span><span class="sxs-lookup"><span data-stu-id="847f3-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="847f3-805">Format</span><span class="sxs-lookup"><span data-stu-id="847f3-805">Format</span></span>

<span data-ttu-id="847f3-806">Dix chiffres contenant un trait d'Union</span><span class="sxs-lookup"><span data-stu-id="847f3-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="847f3-807">Modèle</span><span class="sxs-lookup"><span data-stu-id="847f3-807">Pattern</span></span>

<span data-ttu-id="847f3-808">Dix chiffres contenant un trait d'Union:</span><span class="sxs-lookup"><span data-stu-id="847f3-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="847f3-809">Six chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-809">Six digits</span></span> 
    
- <span data-ttu-id="847f3-810">Un trait d’union</span><span class="sxs-lookup"><span data-stu-id="847f3-810">A hyphen</span></span>
    
- <span data-ttu-id="847f3-811">Quatre chiffres</span><span class="sxs-lookup"><span data-stu-id="847f3-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="847f3-812">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="847f3-812">Checksum</span></span>

<span data-ttu-id="847f3-813">Non</span><span class="sxs-lookup"><span data-stu-id="847f3-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="847f3-814">Définition</span><span class="sxs-lookup"><span data-stu-id="847f3-814">Definition</span></span>

<span data-ttu-id="847f3-815">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="847f3-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="847f3-816">L'expression `Regex_sweden_eu_driver's_license_number` régulière trouve le contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="847f3-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="847f3-817">Un mot clé `Keywords_sweden_eu_driver's_license_number` from est trouvé.</span><span class="sxs-lookup"><span data-stu-id="847f3-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="847f3-818">Mots clés</span><span class="sxs-lookup"><span data-stu-id="847f3-818">Keywords</span></span>

<span data-ttu-id="847f3-819">| |</span><span class="sxs-lookup"><span data-stu-id="847f3-819"></span></span>
|<span data-ttu-id="847f3-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="847f3-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="847f3-821">LD</span><span class="sxs-lookup"><span data-stu-id="847f3-821">dl#</span></span>  <br/> <span data-ttu-id="847f3-822">Permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-822">driver license</span></span>  <br/> <span data-ttu-id="847f3-823">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-823">driver license number</span></span>  <br/> <span data-ttu-id="847f3-824">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-824">driver licence</span></span>  <br/> <span data-ttu-id="847f3-825">pilotes.</span><span class="sxs-lookup"><span data-stu-id="847f3-825">drivers lic.</span></span>  <br/> <span data-ttu-id="847f3-826">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-826">drivers license</span></span>  <br/> <span data-ttu-id="847f3-827">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-827">drivers licence</span></span>  <br/> <span data-ttu-id="847f3-828">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-828">driver's license</span></span>  <br/> <span data-ttu-id="847f3-829">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-829">driver's license number</span></span>  <br/> <span data-ttu-id="847f3-830">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-830">driver's licence number</span></span>  <br/> <span data-ttu-id="847f3-831">Numéro de permis de conduire</span><span class="sxs-lookup"><span data-stu-id="847f3-831">driving license number</span></span>  <br/> <span data-ttu-id="847f3-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="847f3-832">dlno#</span></span>  <br/> <span data-ttu-id="847f3-833">körkort</span><span class="sxs-lookup"><span data-stu-id="847f3-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="847f3-834">R.U.</span><span class="sxs-lookup"><span data-stu-id="847f3-834">UK</span></span>

<span data-ttu-id="847f3-835">Pour plus d'informations, reportez-vous à la section «Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="847f3-835">For details, see the section "U.K.</span></span> <span data-ttu-id="847f3-836">Numéro de permis de conduire» dans [ce que recherche les types d'informations sensibles](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="847f3-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="847f3-837">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="847f3-837">See also</span></span>

[<span data-ttu-id="847f3-838">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="847f3-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

