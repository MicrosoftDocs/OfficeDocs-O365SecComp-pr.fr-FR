---
title: Numéro de téléphone de l’Union européenne
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1c90ca41-1681-46bf-8ad6-6bf4cec5c426
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles de numéro de téléphone de l’UE.
ms.openlocfilehash: 9dd878e3385312982f9f3a4927205e3ebb27aabb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528175"
---
# <a name="eu-phone-number"></a><span data-ttu-id="d05c1-104">Numéro de téléphone de l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="d05c1-104">EU Phone Number</span></span>

<span data-ttu-id="d05c1-p102">Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles de numéro de téléphone de l’UE.</span><span class="sxs-lookup"><span data-stu-id="d05c1-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="d05c1-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="d05c1-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d05c1-108">Format</span><span class="sxs-lookup"><span data-stu-id="d05c1-108">Format</span></span>

<span data-ttu-id="d05c1-109">Aucune longueur standard</span><span class="sxs-lookup"><span data-stu-id="d05c1-109">No standard length</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d05c1-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-110">Pattern</span></span>

- <span data-ttu-id="d05c1-111">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-111">Digits</span></span> 
    
- <span data-ttu-id="d05c1-112">Uniquement les numéros de téléphone mobile commencent par le chiffre « 6 »</span><span class="sxs-lookup"><span data-stu-id="d05c1-112">Only mobile phone numbers begin with the digit "6"</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-113">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-113">Checksum</span></span>

<span data-ttu-id="d05c1-114">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-114">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-115">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-115">Definition</span></span>

<span data-ttu-id="d05c1-116">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-117">L’expression régulière `Regex_austria_eu_telephone_number_1` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-117">The regular expression  `Regex_austria_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-118">Un mot clé à partir de `Keywords_austria_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-118">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-119">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-119">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-120">L’expression régulière `Regex_austria_eu_telephone_number_2` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-120">The regular expression  `Regex_austria_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-121">Un mot clé à partir de `Keywords_austria_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-121">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_1" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_2" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_2" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="d05c1-122">Belgique</span><span class="sxs-lookup"><span data-stu-id="d05c1-122">Belgium</span></span>

### <a name="definition"></a><span data-ttu-id="d05c1-123">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-123">Definition</span></span>

<span data-ttu-id="d05c1-124">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-125">L’expression régulière `Regex_belgium_eu_telephone_number_1` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-125">The regular expression  `Regex_belgium_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-126">Un mot clé à partir de `Keywords_belgium_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-126">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-127">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-127">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-128">L’expression régulière `Regex_belgium_eu_telephone_number_2` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-128">The regular expression  `Regex_belgium_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-129">Un mot clé à partir de `Keywords_belgium_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-129">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_1" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_2" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_2" />
          </Pattern></Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="d05c1-130">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="d05c1-130">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-131">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-131">Pattern</span></span>

- <span data-ttu-id="d05c1-132">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-132">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-133">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-133">Checksum</span></span>

<span data-ttu-id="d05c1-134">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-134">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-135">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-135">Definition</span></span>

<span data-ttu-id="d05c1-136">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-137">L’expression régulière `Regex_bulgaria_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-137">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-138">Un mot clé à partir de `Keywords_bulgaria_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-138">A keyword from  `Keywords_bulgaria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-139">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-139">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-140">L’expression régulière `Regex_bulgaria_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-140">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_telephone_number" />
          <Match idRef="Keywords_bulgaria_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_bulgaria_eu_formatted_telephone_number" />
          </Pattern>
          
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="d05c1-141">Croatie</span><span class="sxs-lookup"><span data-stu-id="d05c1-141">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-142">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-142">Pattern</span></span>

- <span data-ttu-id="d05c1-143">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-144">Checksum</span></span>

<span data-ttu-id="d05c1-145">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-146">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-146">Definition</span></span>

<span data-ttu-id="d05c1-147">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-148">L’expression régulière `Regex_croatia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-148">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-149">Un mot clé à partir de `Keywords_croatia_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-149">A keyword from  `Keywords_croatia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-150">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-150">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-151">L’expression régulière `Regex_croatia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-151">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_telephone_number" />
          <Match idRef="Keywords_croatia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_croatia_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="cyprus"></a><span data-ttu-id="d05c1-152">Chypre</span><span class="sxs-lookup"><span data-stu-id="d05c1-152">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-153">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-153">Pattern</span></span>

- <span data-ttu-id="d05c1-154">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-154">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-155">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-155">Checksum</span></span>

<span data-ttu-id="d05c1-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-156">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-157">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-157">Definition</span></span>

<span data-ttu-id="d05c1-158">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-159">L’expression régulière `Regex_cyprus_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-159">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-160">Un mot clé à partir de `Keywords_cyprus_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-160">A keyword from  `Keywords_cyprus_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-161">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-161">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-162">L’expression régulière `Regex_cyprus_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-162">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_telephone_number" />
          <Match idRef="Keywords_cyprus_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_cyprus_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="d05c1-163">République tchèque</span><span class="sxs-lookup"><span data-stu-id="d05c1-163">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-164">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-164">Pattern</span></span>

- <span data-ttu-id="d05c1-165">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-165">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-166">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-166">Checksum</span></span>

<span data-ttu-id="d05c1-167">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-167">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-168">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-168">Definition</span></span>

<span data-ttu-id="d05c1-169">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-169">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-170">L’expression régulière `Regex_czech_republic_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-170">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-171">Un mot clé à partir de `Keywords_czech_republic_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-171">A keyword from  `Keywords_czech_republic_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-172">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-172">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-173">L’expression régulière `Regex_czech_republic_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-173">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_telephone_number" />
          <Match idRef="Keywords_czech_republic_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_czech_republic_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="denmark"></a><span data-ttu-id="d05c1-174">Danemark</span><span class="sxs-lookup"><span data-stu-id="d05c1-174">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-175">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-175">Pattern</span></span>

- <span data-ttu-id="d05c1-176">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-176">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-177">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-177">Checksum</span></span>

<span data-ttu-id="d05c1-178">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-178">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-179">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-179">Definition</span></span>

<span data-ttu-id="d05c1-180">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-180">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-181">L’expression régulière `Regex_denmark_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-181">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-182">Un mot clé à partir de `Keywords_denmark_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-182">A keyword from  `Keywords_denmark_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-183">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-184">L’expression régulière `Regex_denmark_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-184">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_telephone_number" />
          <Match idRef="Keywords_denmark_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_denmark_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="estonia"></a><span data-ttu-id="d05c1-185">Estonie</span><span class="sxs-lookup"><span data-stu-id="d05c1-185">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-186">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-186">Pattern</span></span>

- <span data-ttu-id="d05c1-187">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-187">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-188">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-188">Checksum</span></span>

<span data-ttu-id="d05c1-189">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-189">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-190">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-190">Definition</span></span>

<span data-ttu-id="d05c1-191">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-191">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-192">L’expression régulière `Regex_estonia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-192">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-193">Un mot clé à partir de `Keywords_estonia_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-193">A keyword from  `Keywords_estonia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-194">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-195">L’expression régulière `Regex_estonia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-195">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_telephone_number" />
          <Match idRef="Keywords_estonia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_estonia_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="finland"></a><span data-ttu-id="d05c1-196">Finlande</span><span class="sxs-lookup"><span data-stu-id="d05c1-196">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-197">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-197">Pattern</span></span>

- <span data-ttu-id="d05c1-198">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-198">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-199">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-199">Checksum</span></span>

<span data-ttu-id="d05c1-200">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-200">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-201">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-201">Definition</span></span>

<span data-ttu-id="d05c1-202">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-203">L’expression régulière `Regex_finland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-203">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-204">Un mot clé à partir de `Keywords_finland_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-204">A keyword from  `Keywords_finland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-205">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-205">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-206">L’expression régulière `Regex_finland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-206">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_telephone_number" />
          <Match idRef="Keywords_finland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_finland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="d05c1-207">France</span><span class="sxs-lookup"><span data-stu-id="d05c1-207">France</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-208">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-208">Pattern</span></span>

- <span data-ttu-id="d05c1-209">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-209">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-210">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-210">Checksum</span></span>

<span data-ttu-id="d05c1-211">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-211">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-212">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-212">Definition</span></span>

<span data-ttu-id="d05c1-213">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-213">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-214">L’expression régulière `Regex_france_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-214">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-215">Un mot clé à partir de `Keywords_france_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-215">A keyword from  `Keywords_france_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-216">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-217">L’expression régulière `Regex_france_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-217">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_telephone_number" />
          <Match idRef="Keywords_france_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_france_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="germany"></a><span data-ttu-id="d05c1-218">Allemagne</span><span class="sxs-lookup"><span data-stu-id="d05c1-218">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-219">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-219">Pattern</span></span>

- <span data-ttu-id="d05c1-220">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-220">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-221">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-221">Checksum</span></span>

<span data-ttu-id="d05c1-222">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-222">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-223">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-223">Definition</span></span>

<span data-ttu-id="d05c1-224">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-224">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-225">L’expression régulière `Regex_germany_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-225">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-226">Un mot clé à partir de `Keywords_germany_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-226">A keyword from  `Keywords_germany_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-227">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-228">L’expression régulière `Regex_germany_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-228">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_telephone_number" />
          <Match idRef="Keywords_germany_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_germany_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="greece"></a><span data-ttu-id="d05c1-229">Grèce</span><span class="sxs-lookup"><span data-stu-id="d05c1-229">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-230">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-230">Pattern</span></span>

- <span data-ttu-id="d05c1-231">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-231">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-232">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-232">Checksum</span></span>

<span data-ttu-id="d05c1-233">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-233">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-234">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-234">Definition</span></span>

<span data-ttu-id="d05c1-235">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-236">L’expression régulière `Regex_greece_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-236">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-237">Un mot clé à partir de `Keywords_greece_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-237">A keyword from  `Keywords_greece_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-238">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-238">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-239">L’expression régulière `Regex_greece_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-239">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_telephone_number" />
          <Match idRef="Keywords_greece_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_greece_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="hungary"></a><span data-ttu-id="d05c1-240">Hongrie</span><span class="sxs-lookup"><span data-stu-id="d05c1-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-241">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-241">Pattern</span></span>

- <span data-ttu-id="d05c1-242">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-242">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-243">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-243">Checksum</span></span>

<span data-ttu-id="d05c1-244">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-245">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-245">Definition</span></span>

<span data-ttu-id="d05c1-246">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-247">L’expression régulière `Regex_hungary_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-247">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-248">Un mot clé à partir de `Keywords_hungary_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-248">A keyword from  `Keywords_hungary_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-249">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-250">L’expression régulière `Regex_hungary_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-250">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_telephone_number" />
          <Match idRef="Keywords_hungary_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_hungary_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="ireland"></a><span data-ttu-id="d05c1-251">Irlande</span><span class="sxs-lookup"><span data-stu-id="d05c1-251">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-252">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-252">Pattern</span></span>

- <span data-ttu-id="d05c1-253">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-254">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-254">Checksum</span></span>

<span data-ttu-id="d05c1-255">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-256">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-256">Definition</span></span>

<span data-ttu-id="d05c1-257">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-258">L’expression régulière `Regex_ireland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-258">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-259">Un mot clé à partir de `Keywords_ireland_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-259">A keyword from  `Keywords_ireland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-260">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-261">L’expression régulière `Regex_ireland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-261">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_telephone_number" />
          <Match idRef="Keywords_ireland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_ireland_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="italy"></a><span data-ttu-id="d05c1-262">Italie</span><span class="sxs-lookup"><span data-stu-id="d05c1-262">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-263">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-263">Pattern</span></span>

- <span data-ttu-id="d05c1-264">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-264">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-265">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-265">Checksum</span></span>

<span data-ttu-id="d05c1-266">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-266">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-267">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-267">Definition</span></span>

<span data-ttu-id="d05c1-268">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-268">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-269">L’expression régulière `Regex_italy_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-269">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-270">Un mot clé à partir de `Keywords_italy_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-270">A keyword from  `Keywords_italy_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-271">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-272">L’expression régulière `Regex_italy_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-272">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_telephone_number" />
          <Match idRef="Keywords_italy_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_italy_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="latvia"></a><span data-ttu-id="d05c1-273">Lettonie</span><span class="sxs-lookup"><span data-stu-id="d05c1-273">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-274">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-274">Pattern</span></span>

- <span data-ttu-id="d05c1-275">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-275">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-276">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-276">Checksum</span></span>

<span data-ttu-id="d05c1-277">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-277">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-278">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-278">Definition</span></span>

<span data-ttu-id="d05c1-279">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-279">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-280">L’expression régulière `Regex_latvia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-280">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-281">Un mot clé à partir de `Keywords_latvia_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-281">A keyword from  `Keywords_latvia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-282">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-283">L’expression régulière `Regex_latvia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-283">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_telephone_number" />
          <Match idRef="Keywords_latvia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_latvia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="lithuania"></a><span data-ttu-id="d05c1-284">Lituanie</span><span class="sxs-lookup"><span data-stu-id="d05c1-284">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-285">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-285">Pattern</span></span>

- <span data-ttu-id="d05c1-286">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-286">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-287">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-287">Checksum</span></span>

<span data-ttu-id="d05c1-288">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-288">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-289">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-289">Definition</span></span>

<span data-ttu-id="d05c1-290">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-291">L’expression régulière `Regex_lithuania_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-291">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-292">Un mot clé à partir de `Keywords_lithuania_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-292">A keyword from  `Keywords_lithuania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-293">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-293">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-294">L’expression régulière `Regex_lithuania_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-294">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_telephone_number" />
          <Match idRef="Keywords_lithuania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_lithuania_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="d05c1-295">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="d05c1-295">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-296">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-296">Pattern</span></span>

- <span data-ttu-id="d05c1-297">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-297">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-298">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-298">Checksum</span></span>

<span data-ttu-id="d05c1-299">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-299">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-300">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-300">Definition</span></span>

<span data-ttu-id="d05c1-301">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-302">L’expression régulière `Regex_luxemburg_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-302">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-303">Un mot clé à partir de `Keywords_luxemburg_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-303">A keyword from  `Keywords_luxemburg_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-304">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-304">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-305">L’expression régulière `Regex_luxemburg_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-305">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_telephone_number" />
          <Match idRef="Keywords_luxemburg_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_luxemburg_eu_formatted_telephone_number" />
                  </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="d05c1-306">Malte</span><span class="sxs-lookup"><span data-stu-id="d05c1-306">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-307">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-307">Pattern</span></span>

- <span data-ttu-id="d05c1-308">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-308">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-309">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-309">Checksum</span></span>

<span data-ttu-id="d05c1-310">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-310">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-311">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-311">Definition</span></span>

<span data-ttu-id="d05c1-312">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-313">L’expression régulière `Regex_malta_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-313">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-314">Un mot clé à partir de `Keywords_malta_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-314">A keyword from  `Keywords_malta_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-315">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-316">L’expression régulière `Regex_malta_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-316">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_telephone_number" />
          <Match idRef="Keywords_malta_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_malta_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="d05c1-317">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="d05c1-317">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-318">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-318">Pattern</span></span>

- <span data-ttu-id="d05c1-319">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-319">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-320">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-320">Checksum</span></span>

<span data-ttu-id="d05c1-321">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-321">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-322">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-322">Definition</span></span>

<span data-ttu-id="d05c1-323">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-323">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-324">L’expression régulière `Regex_netherlands_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-324">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-325">Un mot clé à partir de `Keywords_netherlands_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-325">A keyword from  `Keywords_netherlands_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-326">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-327">L’expression régulière `Regex_netherlands_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-327">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_telephone_number" />
          <Match idRef="Keywords_netherlands_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_netherlands_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="d05c1-328">Pologne</span><span class="sxs-lookup"><span data-stu-id="d05c1-328">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-329">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-329">Pattern</span></span>

- <span data-ttu-id="d05c1-330">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-330">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-331">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-331">Checksum</span></span>

<span data-ttu-id="d05c1-332">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-332">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-333">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-333">Definition</span></span>

<span data-ttu-id="d05c1-334">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-334">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-335">L’expression régulière `Regex_poland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-335">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-336">Un mot clé à partir de `Keywords_poland_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-336">A keyword from  `Keywords_poland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-337">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-338">L’expression régulière `Regex_poland_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-338">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_telephone_number" />
          <Match idRef="Keywords_poland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_poland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="d05c1-339">Portugal</span><span class="sxs-lookup"><span data-stu-id="d05c1-339">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-340">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-340">Pattern</span></span>

- <span data-ttu-id="d05c1-341">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-341">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-342">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-342">Checksum</span></span>

<span data-ttu-id="d05c1-343">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-344">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-344">Definition</span></span>

<span data-ttu-id="d05c1-345">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-346">L’expression régulière `Regex_portugal_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-346">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-347">Un mot clé à partir de `Keywords_portugal_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-347">A keyword from  `Keywords_portugal_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-348">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-349">L’expression régulière `Regex_portugal_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-349">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_telephone_number" />
          <Match idRef="Keywords_portugal_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_portugal_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="romania"></a><span data-ttu-id="d05c1-350">Roumanie</span><span class="sxs-lookup"><span data-stu-id="d05c1-350">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-351">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-351">Pattern</span></span>

- <span data-ttu-id="d05c1-352">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-352">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-353">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-353">Checksum</span></span>

<span data-ttu-id="d05c1-354">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-354">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-355">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-355">Definition</span></span>

<span data-ttu-id="d05c1-356">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-356">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-357">L’expression régulière `Regex_romania_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-357">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-358">Un mot clé à partir de `Keywords_romania_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-358">A keyword from  `Keywords_romania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-359">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-359">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-360">L’expression régulière `Regex_romania_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-360">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_telephone_number" />
          <Match idRef="Keywords_romania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_romania_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="d05c1-361">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="d05c1-361">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-362">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-362">Pattern</span></span>

- <span data-ttu-id="d05c1-363">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-364">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-364">Checksum</span></span>

<span data-ttu-id="d05c1-365">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-366">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-366">Definition</span></span>

<span data-ttu-id="d05c1-367">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-368">L’expression régulière `Regex_slovakia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-368">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-369">Un mot clé à partir de `Keywords_slovakia_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-369">A keyword from  `Keywords_slovakia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-370">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-370">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-371">L’expression régulière `Regex_slovakia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-371">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_telephone_number" />
          <Match idRef="Keywords_slovakia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovakia_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="d05c1-372">Slovénie</span><span class="sxs-lookup"><span data-stu-id="d05c1-372">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-373">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-373">Pattern</span></span>

- <span data-ttu-id="d05c1-374">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-374">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-375">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-375">Checksum</span></span>

<span data-ttu-id="d05c1-376">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-377">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-377">Definition</span></span>

<span data-ttu-id="d05c1-378">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-379">L’expression régulière `Regex_slovenia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-379">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-380">Un mot clé à partir de `Keywords_slovenia_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-380">A keyword from  `Keywords_slovenia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-381">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-382">L’expression régulière `Regex_slovenia_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-382">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_telephone_number" />
          <Match idRef="Keywords_slovenia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovenia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="spain"></a><span data-ttu-id="d05c1-383">Espagne</span><span class="sxs-lookup"><span data-stu-id="d05c1-383">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-384">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-384">Pattern</span></span>

- <span data-ttu-id="d05c1-385">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-385">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-386">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-386">Checksum</span></span>

<span data-ttu-id="d05c1-387">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-387">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-388">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-388">Definition</span></span>

<span data-ttu-id="d05c1-389">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-390">L’expression régulière `Regex_spain_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-390">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-391">Un mot clé à partir de `Keywords_spain_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-391">A keyword from  `Keywords_spain_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-392">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-392">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-393">L’expression régulière `Regex_spain_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-393">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_telephone_number" />
          <Match idRef="Keywords_spain_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_spain_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="sweden"></a><span data-ttu-id="d05c1-394">Suède</span><span class="sxs-lookup"><span data-stu-id="d05c1-394">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-395">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-395">Pattern</span></span>

- <span data-ttu-id="d05c1-396">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-396">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-397">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-397">Checksum</span></span>

<span data-ttu-id="d05c1-398">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-398">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-399">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-399">Definition</span></span>

<span data-ttu-id="d05c1-400">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-400">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-401">L’expression régulière `Regex_sweden_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-401">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-402">Un mot clé à partir de `Keywords_sweden_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-402">A keyword from  `Keywords_sweden_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-403">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-404">L’expression régulière `Regex_sweden_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-404">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_telephone_number" />
          <Match idRef="Keywords_sweden_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_sweden_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="uk"></a><span data-ttu-id="d05c1-405">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="d05c1-405">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="d05c1-406">Modèle</span><span class="sxs-lookup"><span data-stu-id="d05c1-406">Pattern</span></span>

- <span data-ttu-id="d05c1-407">Chiffres</span><span class="sxs-lookup"><span data-stu-id="d05c1-407">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="d05c1-408">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="d05c1-408">Checksum</span></span>

<span data-ttu-id="d05c1-409">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d05c1-409">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="d05c1-410">Définition</span><span class="sxs-lookup"><span data-stu-id="d05c1-410">Definition</span></span>

<span data-ttu-id="d05c1-411">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-412">L’expression régulière `Regex_uk_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-412">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d05c1-413">Un mot clé à partir de `Keywords_uk_eu_telephone_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="d05c1-413">A keyword from  `Keywords_uk_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="d05c1-414">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="d05c1-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d05c1-415">L’expression régulière `Regex_uk_eu_telephone_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="d05c1-415">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_telephone_number" />
          <Match idRef="Keywords_uk_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_uk_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="d05c1-416">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d05c1-416">See also</span></span>

[<span data-ttu-id="d05c1-417">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d05c1-417">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

