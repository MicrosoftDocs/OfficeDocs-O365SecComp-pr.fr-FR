---
title: Numéro de téléphone Mobile de l’Union européenne
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles de numéro de téléphone Mobile de l’UE.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528007"
---
# <a name="eu-mobile-phone-number"></a><span data-ttu-id="64998-104">Numéro de téléphone Mobile de l’Union européenne</span><span class="sxs-lookup"><span data-stu-id="64998-104">EU Mobile Phone Number</span></span>

<span data-ttu-id="64998-p102">Prévention des pertes de données (DLP) de sécurité Office 365 &amp; centre de conformité inclut de nombreux types d’informations sensibles qui sont prêts à utiliser dans vos stratégies DLP. Cette rubrique décrit le type d’informations sensibles de numéro de téléphone Mobile de l’UE.</span><span class="sxs-lookup"><span data-stu-id="64998-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Mobile Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="64998-107">Autriche</span><span class="sxs-lookup"><span data-stu-id="64998-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="64998-108">Format</span><span class="sxs-lookup"><span data-stu-id="64998-108">Format</span></span>

<span data-ttu-id="64998-109">Chiffres sans longueur standard</span><span class="sxs-lookup"><span data-stu-id="64998-109">Digits without standard lengths</span></span>
  
### <a name="pattern"></a><span data-ttu-id="64998-110">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-110">Pattern</span></span>

-  <span data-ttu-id="64998-111">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-111">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="64998-112">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-112">Definition</span></span>

<span data-ttu-id="64998-113">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-113">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-114">L’expression régulière `Regex_austria_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-114">The regular expression  `Regex_austria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-115">L’expression régulière `Regex_austria_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-115">The regular expression  `Regex_austria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-116">Un mot clé à partir de `Keywords_austria_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-116">A keyword from  `Keywords_austria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="64998-117">Belgique</span><span class="sxs-lookup"><span data-stu-id="64998-117">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-118">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-118">Pattern</span></span>

-  <span data-ttu-id="64998-119">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-119">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="64998-120">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-120">Definition</span></span>

<span data-ttu-id="64998-121">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-122">L’expression régulière `Regex_belgium_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-122">The regular expression  `Regex_belgium_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-123">L’expression régulière `Regex_belgium_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-123">The regular expression  `Regex_belgium_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-124">Un mot clé à partir de `Keywords_belgium_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-124">A keyword from  `Keywords_belgium_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="64998-125">Bulgarie</span><span class="sxs-lookup"><span data-stu-id="64998-125">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-126">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-126">Pattern</span></span>

-  <span data-ttu-id="64998-127">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-127">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="64998-128">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-128">Definition</span></span>

<span data-ttu-id="64998-129">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-129">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-130">L’expression régulière `Regex_bulgaria_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-130">The regular expression  `Regex_bulgaria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-131">L’expression régulière `Regex_bulgaria_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-131">The regular expression  `Regex_bulgaria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-132">Un mot clé à partir de `Keywords_bulgaria_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-132">A keyword from  `Keywords_bulgaria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="64998-133">Croatie</span><span class="sxs-lookup"><span data-stu-id="64998-133">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-134">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-134">Pattern</span></span>

-  <span data-ttu-id="64998-135">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-135">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="64998-136">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-136">Definition</span></span>

<span data-ttu-id="64998-137">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-138">L’expression régulière `Regex_croatia_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-138">The regular expression  `Regex_croatia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-139">L’expression régulière `Regex_croatia_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-139">The regular expression  `Regex_croatia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-140">Un mot clé à partir de `Keywords_croatia_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-140">A keyword from  `Keywords_croatia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="64998-141">Chypre</span><span class="sxs-lookup"><span data-stu-id="64998-141">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-142">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-142">Pattern</span></span>

-  <span data-ttu-id="64998-143">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-144">Checksum</span></span>

<span data-ttu-id="64998-145">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-146">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-146">Definition</span></span>

<span data-ttu-id="64998-147">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-148">L’expression régulière `Regex_cyprus_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-148">The regular expression  `Regex_cyprus_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-149">L’expression régulière `Regex_cyprus_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-149">The regular expression  `Regex_cyprus_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-150">Un mot clé à partir de `Keywords_cyprus_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-150">A keyword from  `Keywords_cyprus_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="64998-151">République tchèque</span><span class="sxs-lookup"><span data-stu-id="64998-151">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-152">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-152">Pattern</span></span>

-  <span data-ttu-id="64998-153">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-153">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-154">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-154">Checksum</span></span>

<span data-ttu-id="64998-155">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-155">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-156">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-156">Definition</span></span>

<span data-ttu-id="64998-157">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-157">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-158">L’expression régulière `Regex_czech_republic_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-158">The regular expression  `Regex_czech_republic_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-159">L’expression régulière `Regex_czech_republic_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-159">The regular expression  `Regex_czech_republic_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-160">Un mot clé à partir de `Keywords_czech_republic_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-160">A keyword from  `Keywords_czech_republic_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="64998-161">Danemark</span><span class="sxs-lookup"><span data-stu-id="64998-161">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-162">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-162">Pattern</span></span>

-  <span data-ttu-id="64998-163">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-163">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-164">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-164">Checksum</span></span>

<span data-ttu-id="64998-165">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-165">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-166">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-166">Definition</span></span>

<span data-ttu-id="64998-167">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-167">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-168">L’expression régulière `Regex_denmark_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-168">The regular expression  `Regex_denmark_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-169">L’expression régulière `Regex_denmark_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-169">The regular expression  `Regex_denmark_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-170">Un mot clé à partir de `Keywords_denmark_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-170">A keyword from  `Keywords_denmark_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="64998-171">Estonie</span><span class="sxs-lookup"><span data-stu-id="64998-171">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-172">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-172">Pattern</span></span>

-  <span data-ttu-id="64998-173">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-173">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-174">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-174">Checksum</span></span>

<span data-ttu-id="64998-175">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-175">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-176">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-176">Definition</span></span>

<span data-ttu-id="64998-177">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-177">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-178">L’expression régulière `Regex_estonia_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-178">The regular expression  `Regex_estonia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-179">L’expression régulière `Regex_estonia_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-179">The regular expression  `Regex_estonia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-180">Un mot clé à partir de `Keywords_estonia_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-180">A keyword from  `Keywords_estonia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="64998-181">Finlande</span><span class="sxs-lookup"><span data-stu-id="64998-181">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-182">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-182">Pattern</span></span>

-  <span data-ttu-id="64998-183">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-183">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-184">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-184">Checksum</span></span>

<span data-ttu-id="64998-185">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-185">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-186">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-186">Definition</span></span>

<span data-ttu-id="64998-187">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-187">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-188">L’expression régulière `Regex_finland_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-188">The regular expression  `Regex_finland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-189">L’expression régulière `Regex_finland_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-189">The regular expression  `Regex_finland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-190">Un mot clé à partir de `Keywords_finland_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-190">A keyword from  `Keywords_finland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="64998-191">France</span><span class="sxs-lookup"><span data-stu-id="64998-191">France</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-192">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-192">Pattern</span></span>

-  <span data-ttu-id="64998-193">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-193">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-194">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-194">Checksum</span></span>

<span data-ttu-id="64998-195">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-195">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-196">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-196">Definition</span></span>

<span data-ttu-id="64998-197">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-198">L’expression régulière `Regex_france_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-198">The regular expression  `Regex_france_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-199">L’expression régulière `Regex_france_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-199">The regular expression  `Regex_france_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-200">Un mot clé à partir de `Keywords_france_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-200">A keyword from  `Keywords_france_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="64998-201">Allemagne</span><span class="sxs-lookup"><span data-stu-id="64998-201">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-202">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-202">Pattern</span></span>

-  <span data-ttu-id="64998-203">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-203">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-204">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-204">Checksum</span></span>

<span data-ttu-id="64998-205">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-205">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-206">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-206">Definition</span></span>

<span data-ttu-id="64998-207">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-208">L’expression régulière `Regex_germany_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-208">The regular expression  `Regex_germany_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-209">L’expression régulière `Regex_germany_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-209">The regular expression  `Regex_germany_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-210">Un mot clé à partir de `Keywords_germany_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-210">A keyword from  `Keywords_germany_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="64998-211">Grèce</span><span class="sxs-lookup"><span data-stu-id="64998-211">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-212">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-212">Pattern</span></span>

-  <span data-ttu-id="64998-213">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-213">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-214">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-214">Checksum</span></span>

<span data-ttu-id="64998-215">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-215">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-216">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-216">Definition</span></span>

<span data-ttu-id="64998-217">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-217">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-218">L’expression régulière `Regex_greece_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-218">The regular expression  `Regex_greece_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-219">L’expression régulière `Regex_greece_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-219">The regular expression  `Regex_greece_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-220">Un mot clé à partir de `Keywords_greece_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-220">A keyword from  `Keywords_greece_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="64998-221">Hongrie</span><span class="sxs-lookup"><span data-stu-id="64998-221">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-222">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-222">Pattern</span></span>

-  <span data-ttu-id="64998-223">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-223">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-224">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-224">Checksum</span></span>

<span data-ttu-id="64998-225">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-225">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-226">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-226">Definition</span></span>

<span data-ttu-id="64998-227">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-228">L’expression régulière `Regex_hungary_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-228">The regular expression  `Regex_hungary_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-229">L’expression régulière `Regex_hungary_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-229">The regular expression  `Regex_hungary_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-230">Un mot clé à partir de `Keywords_hungary_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-230">A keyword from  `Keywords_hungary_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="64998-231">Irlande</span><span class="sxs-lookup"><span data-stu-id="64998-231">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-232">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-232">Pattern</span></span>

-  <span data-ttu-id="64998-233">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-233">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-234">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-234">Checksum</span></span>

<span data-ttu-id="64998-235">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-236">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-236">Definition</span></span>

<span data-ttu-id="64998-237">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-238">L’expression régulière `Regex_ireland_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-238">The regular expression  `Regex_ireland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-239">L’expression régulière `Regex_ireland_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-239">The regular expression  `Regex_ireland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-240">Un mot clé à partir de `Keywords_ireland_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-240">A keyword from  `Keywords_ireland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="64998-241">Italie</span><span class="sxs-lookup"><span data-stu-id="64998-241">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-242">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-242">Pattern</span></span>

-  <span data-ttu-id="64998-243">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-243">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-244">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-244">Checksum</span></span>

<span data-ttu-id="64998-245">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-245">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-246">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-246">Definition</span></span>

<span data-ttu-id="64998-247">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-248">L’expression régulière `Regex_italy_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-248">The regular expression  `Regex_italy_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-249">L’expression régulière `Regex_italy_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-249">The regular expression  `Regex_italy_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-250">Un mot clé à partir de `Keywords_italy_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-250">A keyword from  `Keywords_italy_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="64998-251">Lettonie</span><span class="sxs-lookup"><span data-stu-id="64998-251">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-252">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-252">Pattern</span></span>

-  <span data-ttu-id="64998-253">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-254">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-254">Checksum</span></span>

<span data-ttu-id="64998-255">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-256">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-256">Definition</span></span>

<span data-ttu-id="64998-257">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-258">L’expression régulière `Regex_latvia_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-258">The regular expression  `Regex_latvia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-259">L’expression régulière `Regex_latvia_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-259">The regular expression  `Regex_latvia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-260">Un mot clé à partir de `Keywords_latvia_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-260">A keyword from  `Keywords_latvia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="64998-261">Lituanie</span><span class="sxs-lookup"><span data-stu-id="64998-261">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-262">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-262">Pattern</span></span>

-  <span data-ttu-id="64998-263">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-263">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-264">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-264">Checksum</span></span>

<span data-ttu-id="64998-265">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-265">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-266">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-266">Definition</span></span>

<span data-ttu-id="64998-267">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-268">L’expression régulière `Regex_lithuania_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-268">The regular expression  `Regex_lithuania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-269">L’expression régulière `Regex_lithuania_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-269">The regular expression  `Regex_lithuania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-270">Un mot clé à partir de `Keywords_lithuania_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-270">A keyword from  `Keywords_lithuania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="64998-271">Luxembourg</span><span class="sxs-lookup"><span data-stu-id="64998-271">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-272">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-272">Pattern</span></span>

-  <span data-ttu-id="64998-273">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-273">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-274">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-274">Checksum</span></span>

<span data-ttu-id="64998-275">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-275">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-276">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-276">Definition</span></span>

<span data-ttu-id="64998-277">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-277">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-278">L’expression régulière `Regex_luxumburg_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-278">The regular expression  `Regex_luxumburg_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-279">L’expression régulière `Regex_luxumburg_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-279">The regular expression  `Regex_luxumburg_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-280">Un mot clé à partir de `Keywords_luxumburg_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-280">A keyword from  `Keywords_luxumburg_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="64998-281">Malte</span><span class="sxs-lookup"><span data-stu-id="64998-281">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-282">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-282">Pattern</span></span>

-  <span data-ttu-id="64998-283">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-283">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-284">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-284">Checksum</span></span>

<span data-ttu-id="64998-285">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-285">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-286">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-286">Definition</span></span>

<span data-ttu-id="64998-287">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-288">L’expression régulière `Regex_malta_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-288">The regular expression  `Regex_malta_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-289">L’expression régulière `Regex_malta_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-289">The regular expression  `Regex_malta_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-290">Un mot clé à partir de `Keywords_malta_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-290">A keyword from  `Keywords_malta_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="64998-291">Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="64998-291">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-292">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-292">Pattern</span></span>

-  <span data-ttu-id="64998-293">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-293">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-294">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-294">Checksum</span></span>

<span data-ttu-id="64998-295">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-295">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-296">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-296">Definition</span></span>

<span data-ttu-id="64998-297">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-297">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-298">L’expression régulière `Regex_netherlands_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-298">The regular expression  `Regex_netherlands_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-299">L’expression régulière `Regex_netherlands_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-299">The regular expression  `Regex_netherlands_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-300">Un mot clé à partir de `Keywords_netherlands_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-300">A keyword from  `Keywords_netherlands_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="64998-301">Pologne</span><span class="sxs-lookup"><span data-stu-id="64998-301">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-302">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-302">Pattern</span></span>

-  <span data-ttu-id="64998-303">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-303">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-304">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-304">Checksum</span></span>

<span data-ttu-id="64998-305">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-305">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-306">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-306">Definition</span></span>

<span data-ttu-id="64998-307">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-308">L’expression régulière `Regex_poland_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-308">The regular expression  `Regex_poland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-309">L’expression régulière `Regex_poland_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-309">The regular expression  `Regex_poland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-310">Un mot clé à partir de `Keywords_poland_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-310">A keyword from  `Keywords_poland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="64998-311">Portugal</span><span class="sxs-lookup"><span data-stu-id="64998-311">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-312">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-312">Pattern</span></span>

-  <span data-ttu-id="64998-313">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-313">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-314">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-314">Checksum</span></span>

<span data-ttu-id="64998-315">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-315">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-316">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-316">Definition</span></span>

<span data-ttu-id="64998-317">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-317">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-318">L’expression régulière `Regex_portugal_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-318">The regular expression  `Regex_portugal_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-319">L’expression régulière `Regex_portugal_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-319">The regular expression  `Regex_portugal_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-320">Un mot clé à partir de `Keywords_portugal_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-320">A keyword from  `Keywords_portugal_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="64998-321">Roumanie</span><span class="sxs-lookup"><span data-stu-id="64998-321">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-322">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-322">Pattern</span></span>

-  <span data-ttu-id="64998-323">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-323">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-324">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-324">Checksum</span></span>

<span data-ttu-id="64998-325">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-326">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-326">Definition</span></span>

<span data-ttu-id="64998-327">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-328">L’expression régulière `Regex_romania_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-328">The regular expression  `Regex_romania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-329">L’expression régulière `Regex_romania_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-329">The regular expression  `Regex_romania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-330">Un mot clé à partir de `Keywords_romania_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-330">A keyword from  `Keywords_romania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="64998-331">République de Slovaquie</span><span class="sxs-lookup"><span data-stu-id="64998-331">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-332">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-332">Pattern</span></span>

-  <span data-ttu-id="64998-333">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-333">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-334">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-334">Checksum</span></span>

<span data-ttu-id="64998-335">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-335">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-336">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-336">Definition</span></span>

<span data-ttu-id="64998-337">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-338">L’expression régulière `Regex_slovakia_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-338">The regular expression  `Regex_slovakia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-339">L’expression régulière `Regex_slovakia_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-339">The regular expression  `Regex_slovakia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-340">Un mot clé à partir de `Keywords_slovakia_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-340">A keyword from  `Keywords_slovakia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="64998-341">Slovénie</span><span class="sxs-lookup"><span data-stu-id="64998-341">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-342">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-342">Pattern</span></span>

-  <span data-ttu-id="64998-343">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-343">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-344">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-344">Checksum</span></span>

<span data-ttu-id="64998-345">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-345">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-346">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-346">Definition</span></span>

<span data-ttu-id="64998-347">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-347">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-348">L’expression régulière `Regex_slovenia_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-348">The regular expression  `Regex_slovenia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-349">L’expression régulière `Regex_slovenia_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-349">The regular expression  `Regex_slovenia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-350">Un mot clé à partir de `Keywords_slovenia_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-350">A keyword from  `Keywords_slovenia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="64998-351">Espagne</span><span class="sxs-lookup"><span data-stu-id="64998-351">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-352">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-352">Pattern</span></span>

-  <span data-ttu-id="64998-353">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-353">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-354">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-354">Checksum</span></span>

<span data-ttu-id="64998-355">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-355">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-356">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-356">Definition</span></span>

<span data-ttu-id="64998-357">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-358">L’expression régulière `Regex_spain_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-358">The regular expression  `Regex_spain_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-359">L’expression régulière `Regex_spain_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-359">The regular expression  `Regex_spain_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-360">Un mot clé à partir de `Keywords_spain_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-360">A keyword from  `Keywords_spain_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="64998-361">Suède</span><span class="sxs-lookup"><span data-stu-id="64998-361">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-362">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-362">Pattern</span></span>

-  <span data-ttu-id="64998-363">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-364">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-364">Checksum</span></span>

<span data-ttu-id="64998-365">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-366">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-366">Definition</span></span>

<span data-ttu-id="64998-367">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-368">L’expression régulière `Regex_sweden_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-368">The regular expression  `Regex_sweden_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-369">L’expression régulière `Regex_sweden_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-369">The regular expression  `Regex_sweden_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-370">Un mot clé à partir de `Keywords_sweden_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-370">A keyword from  `Keywords_sweden_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="64998-371">ROYAUME-UNI</span><span class="sxs-lookup"><span data-stu-id="64998-371">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="64998-372">Modèle</span><span class="sxs-lookup"><span data-stu-id="64998-372">Pattern</span></span>

-  <span data-ttu-id="64998-373">Chiffres</span><span class="sxs-lookup"><span data-stu-id="64998-373">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="64998-374">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="64998-374">Checksum</span></span>

<span data-ttu-id="64998-375">Non applicable</span><span class="sxs-lookup"><span data-stu-id="64998-375">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="64998-376">Définition</span><span class="sxs-lookup"><span data-stu-id="64998-376">Definition</span></span>

<span data-ttu-id="64998-377">Le pourcentage de confiance d’une stratégie DLP ayant détecté ce type d’informations sensibles est de 75 % si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="64998-377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="64998-378">L’expression régulière `Regex_uk_eu_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-378">The regular expression  `Regex_uk_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-379">L’expression régulière `Regex_uk_eu_formatted_mobile_number` recherche de contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="64998-379">The regular expression  `Regex_uk_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="64998-380">Un mot clé à partir de `Keywords_uk_eu_mobile_number` est trouvée.</span><span class="sxs-lookup"><span data-stu-id="64998-380">A keyword from  `Keywords_uk_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="64998-381">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64998-381">See also</span></span>

[<span data-ttu-id="64998-382">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="64998-382">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

